# Camera Card Demo

English | [简体中文](README.zh-CN.md)

A static OctoScript L0 camera screen demonstrating local artwork, Chinese labels and App Hub publishing. Its camera-style controls do not take photos or change settings. It requests no capabilities, contacts no network host and has no assistant.

The exported layout comes from the camera storyboard's photo scene in the historical Octoscript-AppCard image-to-card flow. This edition fixes its font paths to use portable built-in Chinese fonts.

## Source and releases

The editable app lives in bundle/. PRIVACY.md describes its data boundary; review/ holds acceptance evidence outside the app. The new identity is io.github.ymote.cameracard. Historical camera-card releases remain unchanged and separate; this is not an update to an existing installation.

The initial target is macOS. Android and other platforms require separate acceptance before being added to the listing.

## Publishing

Open an [App Hub issue](https://github.com/OctoSense-org/OctoSense-App-Hub/issues) following the [submission guide](https://github.com/OctoSense-org/OctoSense-App-Hub/blob/main/docs/SUBMITTING.md). The issue can precede the release; include repository, version, permissions, screenshots and current validation status.

The workflow installed by tools/octo publish-github checks and attests a new vVERSION tag, then creates app.bundle.pack.json and a release receipt. No developer signing key or repository signing secret is needed. Keep source editable and use the sealed release pack for review and installation. Never restamp it or move an existing tag.

A successful release is not Hub admission. Add its evidence to the issue; an administrator reviews the exact candidate before catalog publication. Installation requires a compatible OctoSense host supporting publisher-github-v1 (contract 1.8.0).

## Validation status

The unsigned bundle passes admission. Native macOS captures at 406 by 776 and 900 by 800 logical points were inspected with system fonts disabled. Invalid font paths and half-scale export geometry are corrected. This remains a fixed-artboard static demo; wider windows leave unused space.

The genuine GitHub-attested 1.1.0 release passed [nine installed native checks](review/1.1.0/INSTALLED-NATIVE.json) on a compatible source host, with a temporary local Hub. Testing exposed a host placement and scrolling bug, fixed in [App Hub #162](https://github.com/OctoSense-org/OctoSense-App-Hub/pull/162). [Original captures and visual review](review/1.1.0/VISUAL-REVIEW.json) confirm Chinese labels, pane-relative placement, wheel scrolling to the complete shutter, a static control click and reopening after restart. The receipt names the exact host source and binary.

Public catalog admission and install/update checks remain pending. This test is separate from a versioned host release. See [review answers](review/ANSWERS.md); no working camera or account connection is claimed.
