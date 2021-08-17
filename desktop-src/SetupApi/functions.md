---
description: "Le funzioni seguenti fanno parte dell'API di installazione:"
ms.assetid: 0a9518b7-f231-48f2-ba50-5b802f8ccaed
title: Funzioni (API di installazione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e2bf2b8797faa22576fc78deb58e46fd1f2a140721b0d71df469812fabab314
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118886881"
---
# <a name="functions-setup-api"></a>Funzioni (API di installazione)

\[Queste funzioni sono disponibili per l'uso nei sistemi operativi indicati nelle sezioni Requisiti. Possono essere modificati o non disponibili nelle versioni successive. SetupAPI non deve più essere usato per l'installazione di applicazioni. Usare invece il programma di installazione Windows per lo sviluppo di programmi di installazione delle applicazioni. SetupAPI continua a essere usato per l'installazione dei driver di dispositivo.\]

Le funzioni seguenti fanno parte dell'API di installazione:

-   [**InstallHinfSection**](/windows/desktop/api/Setupapi/nf-setupapi-installhinfsectiona)
-   [**SetupAddInstallSectionToDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupaddinstallsectiontodiskspacelista)
-   [**SetupAddSectionToDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupaddsectiontodiskspacelista)
-   [**SetupAddToDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupaddtodiskspacelista)
-   [**SetupAddToSourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupaddtosourcelista)
-   [**SetupAdjustDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupadjustdiskspacelista)
-   [**SetupBackupError**](/windows/desktop/api/Setupapi/nf-setupapi-setupbackuperrora)
-   [**SetupCancelTemporarySourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupcanceltemporarysourcelist)
-   [**SetupCloseFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupclosefilequeue)
-   [**SetupCloseInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupcloseinffile)
-   [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
-   [**SetupConfigureWmiFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupconfigurewmifrominfsectiona)
-   [**SetupCopyError**](/windows/desktop/api/Setupapi/nf-setupapi-setupcopyerrora)
-   [**SetupCopyOEMInf**](/windows/desktop/api/Setupapi/nf-setupapi-setupcopyoeminfa)
-   [**SetupCreateDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupcreatediskspacelista)
-   [**SetupDecompressOrCopyFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupdecompressorcopyfilea)
-   [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
-   [**SetupDeleteError**](/windows/desktop/api/Setupapi/nf-setupapi-setupdeleteerrora)
-   [**SetupDestroyDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupdestroydiskspacelist)
-   [**SetupDuplicateDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupduplicatediskspacelista)
-   [**SetupEnumInfSections**](/windows/desktop/api/Setupapi/nf-setupapi-setupenuminfsectionsa)
-   [**SetupFindFirstLine**](/windows/desktop/api/Setupapi/nf-setupapi-setupfindfirstlinea)
-   [**SetupFindNextLine**](/windows/desktop/api/Setupapi/nf-setupapi-setupfindnextline)
-   [**SetupFindNextMatchLine**](/windows/desktop/api/Setupapi/nf-setupapi-setupfindnextmatchlinea)
-   [**SetupFreeSourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupfreesourcelista)
-   [**SetupGetBinaryField**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetbinaryfield)
-   [**SetupGetFieldCount**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetfieldcount)
-   [**SetupGetFileCompressionInfo**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetfilecompressioninfoa)
-   [**SetupGetFileCompressionInfoEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetfilecompressioninfoexa)
-   [**SetupGetFileQueueCount**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetfilequeuecount)
-   [**SetupGetFileQueueFlags**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetfilequeueflags)
-   [**SetupGetInfFileList**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetinffilelista)
-   [**SetupGetInfInformation**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetinfinformationa)
-   [**SetupGetIntField**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetintfield)
-   [**SetupGetLineByIndex**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetlinebyindexa)
-   [**SetupGetLineCount**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetlinecounta)
-   [**SetupGetLineText**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetlinetexta)
-   [**SetupGetMultiSzField**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetmultiszfielda)
-   [**SetupGetSourceFileLocation**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetsourcefilelocationa)
-   [**SetupGetSourceFileSize**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetsourcefilesizea)
-   [**SetupGetSourceInfo**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetsourceinfoa)
-   [**SetupGetStringField**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetstringfielda)
-   [**SetupGetTargetPath**](/windows/desktop/api/Setupapi/nf-setupapi-setupgettargetpatha)
-   [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback)
-   [**SetupInitDefaultQueueCallbackEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallbackex)
-   [**SetupInitializeFileLog**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitializefileloga)
-   [**SetupInstallFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilea)
-   [**SetupInstallFileEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfileexa)
-   [**SetupInstallFilesFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilesfrominfsectiona)
-   [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona)
-   [**SetupInstallServicesFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallservicesfrominfsectiona)
-   [**SetupInstallServicesFromInfSectionEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallservicesfrominfsectionexa)
-   [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta)
-   [**SetupLogFile**](/windows/desktop/api/Setupapi/nf-setupapi-setuplogfilea)
-   [**SetupLogError**](/windows/desktop/api/Setupapi/nf-setupapi-setuplogerrora)
-   [**SetupOpenAppendInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenappendinffilea)
-   [**SetupOpenFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue)
-   [**SetupOpenInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopeninffilea)
-   [**SetupOpenMasterInf**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenmasterinf)
-   [**SetupPromptForDisk**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptfordiska)
-   [**SetupPromptReboot**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptreboot)
-   [**SetupQueryDrivesInDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupquerydrivesindiskspacelista)
-   [**SetupQueryFileLog**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryfileloga)
-   [**SetupQueryInfFileInformation**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryinffileinformationa)
-   [**SetupQueryInfOriginalFileInformation**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryinforiginalfileinformationa)
-   [**SetupQueryInfVersionInformation**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryinfversioninformationa)
-   [**SetupQuerySourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupquerysourcelista)
-   [**SetupQuerySpaceRequiredOnDrive**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryspacerequiredondrivea)
-   [**SetupQueueCopy**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopya)
-   [**SetupQueueCopyIndirect**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopyindirecta)
-   [**SetupQueueCopySection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopysectiona)
-   [**SetupQueueDefaultCopy**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedefaultcopya)
-   [**SetupQueueDelete**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedeletea)
-   [**SetupQueueDeleteSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedeletesectiona)
-   [**SetupQueueRename**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuerenamea)
-   [**SetupQueueRenameSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuerenamesectiona)
-   [**SetupRemoveFileLogEntry**](/windows/desktop/api/Setupapi/nf-setupapi-setupremovefilelogentrya)
-   [**SetupRemoveFromDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupremovefromdiskspacelista)
-   [**SetupRemoveFromSourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupremovefromsourcelista)
-   [**SetupRemoveInstallSectionFromDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupremoveinstallsectionfromdiskspacelista)
-   [**SetupRemoveSectionFromDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupremovesectionfromdiskspacelista)
-   [**SetupRenameError**](/windows/desktop/api/Setupapi/nf-setupapi-setuprenameerrora)
-   [**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea)
-   [**SetupSetDirectoryId**](/windows/desktop/api/Setupapi/nf-setupapi-setupsetdirectoryida)
-   [**SetupSetDirectoryIdEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupsetdirectoryidexa)
-   [**SetupSetFileQueueAlternatePlatform**](/windows/desktop/api/Setupapi/nf-setupapi-setupsetfilequeuealternateplatforma)
-   [**SetupSetFileQueueFlags**](/windows/desktop/api/Setupapi/nf-setupapi-setupsetfilequeueflags)
-   [**SetupSetPlatformPathOverride**](/windows/desktop/api/Setupapi/nf-setupapi-setupsetplatformpathoverridea)
-   [**SetupSetSourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupsetsourcelista)
-   [**SetupTermDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setuptermdefaultqueuecallback)
-   [**SetupTerminateFileLog**](/windows/desktop/api/Setupapi/nf-setupapi-setupterminatefilelog)
-   [**SetupUninstallNewlyCopiedInfs**](/windows/desktop/api/Setupapi/nf-setupapi-setupuninstallnewlycopiedinfs)
-   [**SetupUninstallOEMInf**](/windows/desktop/api/Setupapi/nf-setupapi-setupuninstalloeminfa)
-   [**SetupVerifyInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupverifyinffilea)

 

 



