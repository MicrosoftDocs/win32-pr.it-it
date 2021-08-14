---
description: Per riprodurre il pacchetto di patch di esempio, è necessario uno strumento software in grado di creare e modificare un pacchetto di patch Windows programma di installazione.
ms.assetid: 0653d8f6-89b0-4c56-ae51-3c7cb7df2909
title: Creazione di un file delle proprietà di creazione delle patch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50873fd508aa9f31435bd401284d38d13310991e150b28f4e24e5ec27f505dc8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118379406"
---
# <a name="creating-a-patch-creation-properties-file"></a>Creazione di un file delle proprietà di creazione delle patch

Per riprodurre il pacchetto di patch di esempio, è necessario uno strumento software in grado di creare e modificare un pacchetto di patch Windows programma di installazione. Diversi strumenti per la creazione di pacchetti di patch sono disponibili da fornitori di software indipendenti. L'esempio illustrato nelle sezioni seguenti usa un editor di database Windows Installer denominato Orca per creare un file delle proprietà di creazione della patch (estensione pcp). Il file con estensione pcp [](msimsp-exe.md) può essere usato con le utilitàMsimsp.exee [Patchwiz.dll](patchwiz-dll.md) per generare un pacchetto di patch Windows Installer (estensione msp). Orca, Msimsp.exe e Patchwiz.dll sono disponibili in Windows [SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).

Con l'SDK viene fornito anche un file di proprietà vuoto per la creazione di patch, template.pcp. Creare una copia di template.pcp e rinominare questa copia MNP2000.pcp. Usare Orca o un altro editor di database per immettere i dati seguenti nella tabella Properties di MNP2000.pcp. La tabella Proprietà contiene le impostazioni globali per il pacchetto di patch.

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
| Guida alla patch                          | {5406B219-A1AC-4BC4-8695-72292C8195AC} |
| PatchOutputPath                    | c: \\ output.msp                         |
| PatchSourceList                    | PatchSourceList                        |



 

Usare l'editor di database per immettere i dati seguenti nella tabella ImageFamilies di MNP2000.pcp. La tabella ImageFamilies contiene informazioni da aggiungere alla tabella [Media durante](media-table.md) l'applicazione di patch.

[Tabella ImageFamilies](imagefamilies-table-patchwiz-dll-.md)



| Famiglia  | MediaSrcPropName | MediaDiskId | FileSequenceStart | DiskPrompt | VolumeLabel |
|---------|------------------|-------------|-------------------|------------|-------------|
| App MNP | MNPSrcPropName   | 2           | 1000              |            |             |



 

Immettere i dati seguenti nella tabella UpgradedImages di MNP2000.pcp. La tabella UpgradedImages contiene informazioni sull'immagine aggiornata creata in [Pianificazione di una patch di aggiornamento di piccole dimensioni.](planning-a-small-update-patch.md)

[Tabella UpgradedImages](upgradedimages-table-patchwiz-dll-.md)



| Aggiornato   | MsiPath                                           | PatchMsiPath | Percorsi dei simboli | Famiglia  |
|------------|---------------------------------------------------|--------------|-------------|---------|
| MNP \_ fisso | C: \\ Nota: \_ Aggiornamento della patch del programma di installazione \\ \\ \\MNP2000.msi |              |             | App MNP |



 

Immettere i dati seguenti nella tabella TargetImages di MNP2000.pcp. La tabella TargetImages contiene informazioni sull'immagine di destinazione.

[Tabella TargetImages](targetimages-table-patchwiz-dll-.md)



| Destinazione     | MsiPath                                         | Percorsi dei simboli | Aggiornato   | JSON | ProductValidateFlags | IgnoreMissingSrcFiles |
|------------|-------------------------------------------------|-------------|------------|-------|----------------------|-----------------------|
| Errore \_ MNP | C: \\ Nota: Programma \_ di installazione Patch Target \\ \\ \\MNP2000.msi |             | MNP \_ fisso | 1     |                      | 0                     |



 

Per il pacchetto patch di esempio, lasciare vuote le tabelle seguenti in MNP2000.pcp.

[Tabella OptionalData di \_ UpgradedFiles](upgradedfiles-optionaldata-table-patchwiz-dll-.md)

[Tabella FamilyFileRanges](familyfileranges-table-patchwiz-dll-.md)

[Tabella TargetFiles \_ OptionalData](targetfiles-optionaldata-table-patchwiz-dll-.md)

[Tabella ExternalFiles](externalfiles-table-patchwiz-dll-.md)

[Tabella UpgradedFilesToIgnore](upgradedfilestoignore-table-patchwiz-dll-.md)

[Continua](generating-a-patch-package.md)

 

 



