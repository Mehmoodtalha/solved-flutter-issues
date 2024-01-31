# wiseUp_TV
WiseUp TV application for movies and live TV shows

## solved 1st time runing issues
### 1st issue 
remove or comment this line in or project android/app/src/main/AndroidManifest.xml file
        android:icon="@mipmap/launcher_icon"

### 2nd issue
replace these code in your pub cache package_info_plus_windows-2.1.0/lib/src/file_version_info.dart
    class _LANGANDCODEPAGE extends Struct {
      @Uint16()
      external int? wLanguage;
      @Uint16()
      external int? wCodePage;
    }
to
    class _LANGANDCODEPAGE extends Struct {
      @Uint16()
      external int wLanguage;
      @Uint16()
      external int wCodePage;
    }
### 3rd issue

replace these code in your pub cache package_info_plus_windows-2.1.0/lib/src/file_version_info.dart
    import 'package:flutter/material.dart';
replace to
    import 'package:flutter/material.dart' hide ModalBottomSheetRoute;
in this file modal_bottom_sheet-2.1.2/lib/src/material_with_modal_page_route.dart search ModalBottomSheetRoute where found
