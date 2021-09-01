## Introduction
This is a project inspired by goindex, suitable for deployment in cloudflare worker, and has the following features compared to the original version:
- Full search (including personal disks and all authorized team disks, you can click the link in the search results to jump to the corresponding google drive official website)
- Paging browsing (the number of files per page can be customized, and each page can be sorted according to file name and size)
- More beautiful UI (thanks to ant design)
- Anti-crawler, for all directories and files, only the administrator has the permission to read and download (the original goindex can set a read password for the directory by preventing .password in the directory, but it cannot restrict the download of a single file)
- It can generate a download link, which is convenient for third-party download tools to download. For streaming media files, you can use players such as potplayer to directly open and play (you can customize the validity period)
- A sharing link with extraction code can be generated to facilitate sharing to others for browsing and downloading (also supports custom validity period)

## changelog
### 2020-08-12
- Display a list of team disks on the homepage (up to 100 entries), click the corresponding name to enter
- Add the function of obtaining direct links in batches (you can choose by yourself, or get the direct links of all direct sub-files in the current directory with one click)
- Add arouse external player function (support IINA/PotPlayer/VLC/nPlayer/MXPlayer)
- Add a search function within a specified range (you can search on the directory list page. Due to Google API limitations, you can only search for direct sub-files of the current directory, and cannot search for the contents of recursive subdirectories. If the current directory is the root directory of the team, then Support whole disk search)
- The "Show Path" button can correctly identify the name of the team drive (it would return "Drive" before)
- Added failure retry mechanism to the back-end search interface

## tips
- This tool can also be used as goindex, just add the directory ID to `https://your.website.com/ls/`.
For example, to browse the content of the team disk, you can directly visit `https://your.website.com/ls/your team disk ID`
Browsing the root directory of the personal disk can directly visit `https://your.website.com/ls/root`
