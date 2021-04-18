---
description: Per riprodurre il pacchetto di patch di esempio, è necessario uno strumento software in grado di creare e modificare un pacchetto di patch Windows Installer.
ms.assetid: 0653d8f6-89b0-4c56-ae51-3c7cb7df2909
title: Creazione di un file delle proprietà di creazione patch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2775f8521731b43264df315ae05a874e37dd3ffc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319439"
---
# <a name="creating-a-patch-creation-properties-file"></a>Creazione di un file delle proprietà di creazione patch

Per riprodurre il pacchetto di patch di esempio, è necessario uno strumento software in grado di creare e modificare un pacchetto di patch Windows Installer. Sono disponibili diversi strumenti per la creazione di pacchetti di patch da fornitori di software indipendenti. Nell'esempio descritto nelle sezioni seguenti viene usato un editor di database Windows Installer denominato ORCA per creare un file delle proprietà di creazione patch (estensione PCP). Il file. PCP può essere usato con le utilità [Msimsp.exe](msimsp-exe.md) e [Patchwiz.dll](patchwiz-dll.md) per generare un pacchetto di patch Windows Installer (estensione msp). Orca, Msimsp.exe e Patchwiz.dll sono disponibili nei [componenti di Windows SDK per gli sviluppatori Windows Installer](platform-sdk-components-for-windows-installer-developers.md).

Con l'SDK viene fornito anche un file di proprietà di creazione patch vuota, template. PCP. Creare una copia di template. PCP e rinominare la copia MNP2000. PCP. Utilizzare Orca o un altro editor di database per immettere i dati seguenti nella tabella Properties di MNP2000. PCP. La tabella Properties contiene le impostazioni globali per il pacchetto di patch.

[Tabella delle proprietà](properties-table-patchwiz-dll-.md)



| Nome                               | Valore                                  |
|------------------------------------|----------------------------------------|
| AllowProductCodeMismatches         | 1                                      |
| AllowProductVersionMajorMismatches | 1                                      |
| ApiPatchingSymbolFlags             | 0x00000000                             |
| DontRemoveTempFolderWhenFinished   | 1                                      |
| IncludeWholeFilesOnly              | 0                                      |
| ListOfPatchGUIDsToReplace          |                                        |
| ListOfTargetProductCodes           | \*                                     |
| PatchGUID                          | {5406B219-A1AC-4BC4-8695-72292C8195AC} |
| PatchOutputPath                    | c: \\ output. msp                         |
| PatchSourceList                    | PatchSourceList                        |



 

Utilizzare l'editor di database per immettere i dati seguenti nella tabella ImageFamilies di MNP2000. PCP. La tabella ImageFamilies contiene informazioni da aggiungere alla [tabella media](media-table.md) durante l'applicazione di patch.

[Tabella ImageFamilies](imagefamilies-table-patchwiz-dll-.md)



| Famiglia  | MediaSrcPropName | MediaDiskId | FileSequenceStart | DiskPrompt | VolumeLabel |
|---------|------------------|-------------|-------------------|------------|-------------|
| MNPapps | MNPSrcPropName   | 2           | 1000              |            |             |



 

Immettere i dati seguenti nella tabella UpgradedImages di MNP2000. PCP. La tabella UpgradedImages contiene informazioni sull'immagine aggiornata creata durante la [pianificazione di una patch di aggiornamento di piccole dimensioni](planning-a-small-update-patch.md).

[Tabella UpgradedImages](upgradedimages-table-patchwiz-dll-.md)



| Aggiornato   | PercorsoMSI                                           | PatchMsiPath | SymbolPaths | Famiglia  |
|------------|---------------------------------------------------|--------------|-------------|---------|
| MNP \_ fisso | C: \\ Nota \_ patch del programma di installazione \\ \\ aggiornata \\MNP2000.msi |              |             | MNPapps |



 

Immettere i dati seguenti nella tabella TargetImages di MNP2000. PCP. La tabella TargetImages contiene informazioni sull'immagine di destinazione.

[Tabella TargetImages](targetimages-table-patchwiz-dll-.md)



| Destinazione     | PercorsoMSI                                         | SymbolPaths | Aggiornato   | JSON | ProductValidateFlags | IgnoreMissingSrcFiles |
|------------|-------------------------------------------------|-------------|------------|-------|----------------------|-----------------------|
| \_Errore MNP | C: \\ Nota la \_ destinazione della patch del programma di installazione \\ \\ \\MNP2000.msi |             | MNP \_ fisso | 1     |                      | 0                     |



 

Per il pacchetto di patch di esempio, lasciare vuote le seguenti tabelle in MNP2000. PCP.

[\_Tabella UpgradedFiles OptionalData](upgradedfiles-optionaldata-table-patchwiz-dll-.md)

[Tabella FamilyFileRanges](familyfileranges-table-patchwiz-dll-.md)

[\_Tabella TargetFiles OptionalData](targetfiles-optionaldata-table-patchwiz-dll-.md)

[Tabella ExternalFiles](externalfiles-table-patchwiz-dll-.md)

[Tabella UpgradedFilesToIgnore](upgradedfilestoignore-table-patchwiz-dll-.md)

[Continua](generating-a-patch-package.md)

 

 



