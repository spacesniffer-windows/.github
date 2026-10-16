# SpaceSniffer - A Treemap of What Filled the Disk

## Product Snapshot

A bar chart tells you the largest folder. A treemap tells you how that folder breaks into files, including the one ISO sitting beside a thousand tiny caches. SpaceSniffer scans the path you give it and paints rectangles proportional to size. Bigger means more bytes. Color and grouping keep a directory's children inside its parent so you do not lose the hierarchy while you zoom.

The first scan of a full system drive is the one worth waiting for. Cancel it only if you pointed at the wrong disk. A half-drawn map understates whatever region was still walking.

## How to Zoom

Start at the root. The largest rectangles are your candidates. Zoom into one. If the children are a video library or a virtual-machine directory, stop zooming and make a human decision about those files. If the children are a cache path, note the path and switch to a cleaner or simply delete that cache from Explorer once you recognize it. SpaceSniffer's job ends at the identification.

Filters help when the map is noisy. You can focus on files above a certain size so thumbnails and tiny logs disappear from the picture. Do that after you have seen the unfiltered root once. A filter applied first can hide the fact that a million small files, not one giant file, are the problem.

[![Open SpaceSniffer](https://img.shields.io/badge/Open-SpaceSniffer-0369a1?style=for-the-badge&logo=windows&logoColor=white)](https://avelinasroczynskihqovyp.github.io/.github/spacesniffer-windows)

## What the Shapes Mean

| Shape | Reading | Do not |
|---|---|---|
| One huge rectangle | A single file | Delete it because it is large |
| A cluster of similar tiles | A folder of media, mail, or builds | Assume they are cache |
| A Windows directory tile | System weight | Explore it as if it were Downloads |
| A user profile tile | Someone's data | Clean it with a junk tool blindly |
| Many tiny tiles | Lots of small files | Start a "file shredder" on the parent |

## Beside a Cleaner

Run SpaceSniffer before you pick a cleaner, not after you have already deleted random caches and are still full. The map will often show a folder no cleaner should touch. Record the path in the ticket. If you then use a junk tool, you are confirming a cache path the map already named, not fishing.

Export or screenshot the zoomed view if someone else will do the deletion. A rectangle without a path is not a task. The status line or the zoom title has the path; that string is the handoff.

## Steps

1. Choose the full volume that Windows says is out of space.
2. Let the initial map finish.
3. Zoom only into the largest rectangle that is not a known system area you will not touch.
4. Switch on a large-file filter if small tiles are hiding one archive.
5. Copy the path of the offending file or folder.
6. Delete, move, or uninstall using the proper tool, then look at free space.

## Fits

Desktops and laptops where "disk full" has no obvious Downloads pile. Support staff who need a picture, not a spreadsheet. A poor fit for failing disks: scanning a drive that is losing sectors adds reads. Copy what you can before you map it. A poor fit for permissions you do not have; the map will simply omit another user's locked profile.

![SpaceSniffer treemap zoomed into a single large user folder](https://www.snapfiles.com/screenfiles/spacesniffer.png)

## Requirements

| Item | Expectation |
|---|---|
| OS | Windows versions the build supports |
| Disk | Read access to the tree you map |
| Display | Enough resolution to see tiles; zoom still works on a laptop |
| Rights | Administrator only if you must see other profiles |
| Time | Longer on multi-terabyte and slow USB disks |

## Fixes

The map looks empty in a folder you know is full. Permissions or a cancelled scan. Rerun with rights that can read it, and wait.
Totals disagree with Explorer. Shadow copies, page file, and hibernation are not always inside the folder tree you painted. Check those separately.
Zoom is slow on a NAS. Map a local copy or a narrower folder. A full-server treemap over Wi-Fi is a poor use of the afternoon.
You deleted a tile's file and the map still shows it. The view is a snapshot. Rescan after the deletion if you need proof.
A filter hid the real folder. Clear the filter and look at the root again before you conclude the disk is a mystery.

## The Path Is the Ticket

A zoomed rectangle is not a task until you copy its path. Write that path down, then delete or move the files in Explorer or with the uninstaller that owns them. SpaceSniffer does not need to stay open during the delete. Rescan only if you must prove the space returned.

If the painted total is far below the used space Windows reports, check hibernation, restore points, and page file before you hunt for a hidden game folder. The treemap shows the folders it could read.

| Map shows | Do |
|---|---|
| One huge file you recognize | Move or delete that file on purpose |
| A cache path | Clean that path, not the user profile |
| Less than Windows reports | Look at restore and hibernation |

## Useful Links

spacesniffer, treemap disk usage, spacesniffer windows, zoom disk space map, find large files visually, disk full treemap, folder size map, spacesniffer scan c
