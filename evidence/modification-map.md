# Modification Map: external/dialog

## Source: BlissOS android-x86 reference (external/dialog)
- BlissOS reference: android-generic/external_dialog (dialog snapshot t20260721 with Android.mk)
- UPSTREAM commits:
  - 5ac5d95 (Android.bp + dlg_config.h: add Soong build for dialog - KhillOS port)
  - 4410f60 (AOSP 17 compliance: add METADATA, LICENSE.txt, NOTICE, MODULE_LICENSE_LGPL21, OWNERS, SPDX headers)
- Upstream base: ThomasDickey/dialog-snapshots @ t20260721 (e65d9f4)

## Modifications Applied to UPSTREAM/external_dialog (khillos-17 branch)

### 1. Android.bp Build System (NEW - from commit 5ac5d95)
**Complete Soong migration from Android.mk:**
- `cc_binary` dialog with vendor_available: true
- `genrule` dlg_config_h for config.h generation
- License module with LGPL-2.1

### 2. AOSP 17 Compliance Metadata Files (NEW - from commit 4410f60)
**Files:** `METADATA`, `LICENSE.txt`, `NOTICE`, `MODULE_LICENSE_LGPL21`, `OWNERS`
- METADATA: Package metadata per AOSP external_updater format
- LICENSE.txt: Copied from upstream COPYING
- NOTICE: Comprehensive LGPL-2.1 license notice
- MODULE_LICENSE_LGPL21: SPDX identifier for Soong license module
- OWNERS: Standard AOSP OWNERS file

### 3. SPDX Headers (NEW - from commit 4410f60)
**Files:** All source files (.c/.h)
- Added SPDX-License-Identifier: LGPL-2.1-or-later to all source files

### 4. Source Code Updates
**Files:** dlg_config.h (generated via genrule)
- Configuration header for Android build

## Summary
- **Total files modified:** ~30 source files (SPDX) + Android.bp + 5 metadata = ~36
- **Source files:** ~30 .c/.h files with SPDX headers added
- **Build system:** Complete Android.bp from scratch (Android.mk → Soong)
- **Logic/behavior changes:** Updated to dialog snapshot t20260721
- **AOSP 17 compliance:** All required metadata files added
