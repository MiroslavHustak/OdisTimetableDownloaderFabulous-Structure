**Bulk downloader of ODIS timetables, Android 11+**

************************************************************

**The actual solution structure, revealing unidirectional F# project dependencies (as GitHub distorts the reality by displaying only an alphabetical order), is shown in the chart below:**

```
EmbeddedTP/
├── EmbeddedTP.fsproj
├── EmbeddedTP.fs
└── KODISJson/
    ├── kodisMHDTotal.json
    └── kodisMHDTotal2_0.json
```
```
OdisTimetableDownloaderMAUI (Solution)
├── OdisTimetableDownloaderMAUI.fsproj
├── Educational code.txt
├── AssemblyInfo/
│   └── AssemblyInfo.fs
├── NativeCode/
│   └── NativeCode.fs
├── Types/
│   ├── TDD.fs
│   ├── ErrorTypes.fs
│   ├── Types.fs
│   └── IsomorphismAndCardinality.fs
├── Settings/
│   ├── Messages.fs
│   ├── SettingsGeneral.fs
│   ├── SettingsDPO.fs
│   ├── SettingsKODIS.fs
│   └── SettingsMDPO.fs
├── ApplicativeFunctors/
│   └── Applicatives.fs
├── CEBuilders/
│   └── CEBuilders.fs
├── OptionResultExtensions/
│   ├── ResultExtensions.fs
│   └── OptionExtensions.fs
├── Helpers/
│   ├── IO_Monad_Experiments/
│   │   └── IO_Monad.fs
│   ├── Helpers.fs
│   ├── Serialization.fs
│   └── Parsers.fs
├── ProgressTrackers/
│   └── ProgressTrackers.fs
├── DotNetInteroperabilityCode/
│   └── DotNetInteroperabilityCode.fs
├── JavaInteroperabilityCode/
│   ├── RealInternetChecker.fs
│   └── SSL_TLS_handling.fs
├── Libraries/
│   ├── CopyOrMoveDir.fs
│   └── ListParallel.fs
├── Monads/
│   ├── FreeMonads/
│   │   ├── CmdLineWorkflows.fs
│   │   └── FreeMonad.fs
│   └── StateMonads/
│       └── StateMonad.fs
├── Connectivity/
│   └── Connectivity.fs
├── Secrets/
│   ├── ApiKeys.fs
│   └── Secrets.json
├── Logging/
│   ├── DataModelling/
│   │   ├── DataModels.fs
│   │   ├── DataTransferModels.fs
│   │   └── TransformationLayers.fs
│   ├── LogEntries.fs
│   └── Logging.fs
├── ExceptionHandling/
│   └── ExceptionHandlers.fs
├── BusinessLogic/
│   ├── AndroidSpecificCodeBL/
│   │   ├── DataModelling/
│   │   │   ├── DataModels.fs
│   │   │   ├── DataTransferModels.fs
│   │   │   └── TransformationLayers.fs
│   │   ├── AndroidClientActivation.fs
│   │   └── AndroidMediaStore.fs
│   ├── DataManipulation/
│   │   ├── DataModelling/
│   │   │   └── DataModels.fs
│   │   ├── DataModellingApi/
│   │   │   ├── DataModels.fs
│   │   │   ├── DataTransferModels.fs
│   │   │   └── TransformationLayers.fs
│   │   ├── PureFunctions/
│   │   │   └── ParseRecordData.fs
│   │   └── ImpureFunctions/
│   │       ├── JsonDataParser.fs
│   │       ├── TimetableLinksParser.fs
│   │       ├── RestApiLinks.fs
│   │       └── ConcurrencyGuard.fs
│   ├── IO_Operations/
│   │   ├── PureHelpers/
│   │   │   └── CreatePathsAndNames.fs
│   │   └── ImpureFunctions/
│   │       ├── DataModelling/
│   │       │   ├── DataModels.fs
│   │       │   ├── DataTransferModels.fs
│   │       │   └── TransformationLayers.fs
│   │       └── IO_Operations.fs
│   └── MainBusinessLogic_R/
│       ├── KodisJsonTP/
│       │   ├── KODIS_BL_Record_R_Json.fs
│       │   └── KODIS_BL_Record_R.fs
│       ├── KodisCanopy/
│       │   ├── KODIS_BL_Record4_R_Json.fs
│       │   └── KODIS_BL_Record4_R.fs
│       ├── Dpo/
│       │   └── DPO_BL_R.fs
│       ├── Mdpo/
│       │   ├── MDPO_BL_R_Json.fs
│       │   └── MDPO_BL_R.fs
│       └── TP_Canopy_Difference_R.fs
├── ApplicationDesign_R/
│   ├── DPO_R.fs
│   ├── MDPO_R.fs
│   ├── KodisCanopy/
│   │   └── KODIS_Record4_R.fs
│   └── KodisJsonTP/
│       └── KODIS_Record_R.fs
├── XElmish/
│   ├── Infrastructure/
│   │   ├── AndroidSpecificCode/
│   │   │   ├── AndroidSpecificCode.fs
│   │   │   ├── AndroidStorageBridge.fs
│   │   │   └── AndroidSAF.fs
│   │   ├── FileManagerLauncher.fs
│   │   ├── ComparisonResultFileLauncher.fs
│   │   ├── HardRestart.fs
│   │   ├── Counters.fs
│   │   └── ActorModels.fs
│   ├── ViewHelpers/
│   │   ├── ScreenHelpers.fs
│   │   └── ProgressWidgets.fs
│   ├── Engines/
│   │   ├── Upload.fs
│   │   ├── KodisTP.fs
│   │   ├── KodisCanopy.fs
│   │   ├── Dpo.fs
│   │   └── Mdpo.fs
│   └── App_New_UX.fs
├── Platforms/
│   ├── Android/
│   │   ├── Resources/
│   │   │   ├── Fonts/
│   │   │   ├── Images/
│   │   │   ├── AppIcon/
│   │   │   │   ├── appicon.svg
│   │   │   │   └── appiconfg.svg
│   │   │   ├── Splash/
│   │   │   │   └── splash.svg
│   │   │   ├── Raw/
│   │   │   ├── drawable/
│   │   │   │   └── ic_download.xml
│   │   │   ├── xml/
│   │   │   │   ├── file_paths.xml
│   │   │   │   └── network_security_config.xml
│   │   │   └── values/
│   │   │       └── colors.xml
│   │   ├── Assets/
│   │   ├── AndroidManifest.xml
│   │   ├── MainApplication.fs
│   │   └── MainActivity.fs
│   └── Windows/
│       ├── app.manifest
│       ├── App.fs
│       └── Main.fs
├── Resources/
│   ├── Fonts/
│   ├── Images/
│   ├── AppIcon/
│   │   ├── appicon.svg
│   │   └── appiconfg.svg
│   ├── Splash/
│   │   └── splash.svg
│   └── Raw/
├── MauiProgram.fs
└── Secrets/
    └── Secrets.json
```
