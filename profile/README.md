# RogueKiller - On-Demand Scan for PUPs and Hidden Hooks

## Product Intent

Some unwanted software survives "uninstall" because a second piece reinstalls it, or because a component hides from the normal process list. RogueKiller's scan looks for those patterns: PUP files, hijacked settings, and hooks that do not belong to a product you installed. The report is meant to be read. Removing every line without looking is how a legitimate security driver gets swept up with a toolbar.

Run it elevated, with browsers closed, and with one other antivirus left enabled for real-time coverage. Two on-demand scanners are fine in sequence. Two products deleting the same file at the same time are not.

## What the Report Is Divided Into

| Area | Why it is there | How to treat a hit |
|---|---|---|
| PUP or adware files | The installer you did not want | Remove after you confirm you do not use it |
| Browser settings | Homepage, search, extensions | Remove, then check the profile by hand |
| Hosts or proxy changes | Traffic steered aside | Remove if you did not make them for a lab |
| Drivers and hooks | Hiding or injection | Remove only if the publisher is not a tool you installed |
| Startup leftovers | The relaunch path | Remove and reboot |

A hit on a known remote-admin tool or a known antivirus can be a detection of something you installed on purpose. Read the path. If it is under the vendor directory of software you trust, investigate before you delete. If it is under a temporary folder or a randomly named directory, the detection is doing the job you opened the tool for.

[![Open RogueKiller](https://img.shields.io/badge/Open-RogueKiller-7f1d1d?style=for-the-badge&logo=windows&logoColor=white)](https://dedemaylone.github.io/.github/adlice-roguekiller)

## Sequence

1. Update the scanner if the build offers updates, so the visit is not on a stale set.
2. Close browsers and pause any other on-demand scan.
3. Run a full scan rather than a rushed quick pass when the symptom is a hijack.
4. Read each detection's path and publisher.
5. Remove the set you accept and reboot if the tool asks.
6. Open the browser and confirm homepage, search, and extensions.

If the desktop still redirects after a clean reboot, check other Windows accounts and any proxy set at the system level. A scanner cannot fix a router that injects ads. That is outside the PC, and another scan will look "successful" while the network keeps misbehaving.

## Beside a Normal Uninstaller

If the PUP has a real uninstall entry, you may run that first and then scan for the pieces the uninstaller leaves. If there is no entry, the scanner is the removal path. Do not delete random Program Files folders because a detection named a similar publisher. Use the paths in the report.

Keep the quarantine or backup the product offers until the PC has been normal for a day. A false positive on a VPN filter is easier to undo from quarantine than from memory.

## Who It Fits

Machines with toolbars, replaced shortcuts, or a suspicion that something reinstalls itself after removal. A poor fit for routine junk cleaning, for driver updates, and for a PC that will not boot. A scanner that needs Windows running cannot repair a boot loop. A poor fit as well when company policy already runs a managed detection stack and a second remover will fight it.

![RogueKiller detection list with paths visible before removal](https://adlice.com/brand/aprotect2.png)

## Requirements

| Item | Expectation |
|---|---|
| OS | Windows versions Adlice currently supports |
| Rights | Administrator |
| Disk | Room for logs and quarantine |
| Network | For updates before the scan |
| Time | A full scan on a large disk is not a one-minute popup |

## Fixes

Detections return after reboot. A dropper is still launching, or another user is affected. Check startup and scan the other profile.
A trusted tool was flagged. Confirm the file path and signature, restore if it is genuine, and update both products.
The browser is clean and ads remain on one site. That can be the site. Test a second site before you reinstall Windows.
The scan will not start. Another security product is blocking it. Allow the on-demand scan or run it from a simpler boot if you have a known procedure.
Nothing is found and the shortcut is still wrong. The shortcut may be a user file the scan did not classify. Recreate the shortcut after you verify the target.

## One Scanner, Then a Day

Leave quarantine in place overnight. A browser that stays on the right homepage is the result you wanted. Restoring a detection an hour later because the name looked familiar is reasonable only when you recognize the publisher and the path. Emptying quarantine immediately removes the way back.

If the same PUP returns, something is launching it. Look at startup and other Windows users before you install a second remover beside RogueKiller. Two tools deleting files at once make the log useless.

| Next day | Meaning |
|---|---|
| Homepage stays | Leave quarantine as it is |
| A tool you need is gone | Restore that one path |
| The PUP is back | Find what relaunches it |

## Further Reading

roguekiller, adlice roguekiller, pup rootkit scan, roguekiller windows, browser hijack scanner, on demand pup removal, quarantine startup hook, roguekiller reboot
