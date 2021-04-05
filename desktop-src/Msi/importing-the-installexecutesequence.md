---
description: Nella tabella InstallExecuteSequence sono elencate le azioni che vengono eseguite quando il programma di installazione esegue l'azione di installazione di primo livello. Vedere il gruppo di tabelle delle procedure di installazione, usando una tabella di sequenza e l'esempio dettagliato della tabella di sequenza.
ms.assetid: cdd4f02a-cfe6-4a23-9fc2-f4cb810379aa
title: Importazione del InstallExecuteSequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8e4728b0a59c92dcc0d007fc816fd298455e049
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967907"
---
# <a name="importing-the-installexecutesequence"></a>Importazione del InstallExecuteSequence

Nella [tabella InstallExecuteSequence](installexecutesequence-table.md) sono elencate le azioni che vengono eseguite quando il programma di installazione esegue l' [azione di installazione](install-action.md)di primo livello. Vedere il [gruppo di tabelle delle procedure di installazione](installation-procedure-tables-group.md), [usando una tabella di sequenza](using-a-sequence-table.md)e l' [esempio dettagliato della tabella di sequenza](sequence-table-detailed-example.md).

Se nella sezione [importazione di un database vuoto](importing-a-blank-database.md) utilizzato uisample.msi da Windows Installer SDK, le tabelle di sequenza nella copia di MNP2000.msi contengono già le sequenze di azioni suggerite descritte in [utilizzo di una tabella di sequenza](using-a-sequence-table.md). Per creare il pacchetto di installazione del blocco note non è necessario apportare modifiche a tali sequenze.

Utilizzare l'editor di database per aprire MNP2000.msi e immettere i dati seguenti nella tabella InstallExecuteSequence.

[Tabella InstallExecuteSequence](installexecutesequence-table.md)



| Azione                   | Condizione     | Sequenza |
|--------------------------|---------------|----------|
| AllocateRegistrySpace    | NON installato | 1550     |
| AppSearch                |               | 400      |
| Azione BindImage sul                |               | 4300     |
| CCPSearch                | NON installato | 500      |
| CostFinalize secondo             |               | 1000     |
| CostInitialize           |               | 800      |
| CreateFolders            |               | 3700     |
| CreateShortcuts          |               | 4500     |
| DeleteServices           | VersionNT     | 2000     |
| DuplicateFiles           |               | 4210     |
| Filecost                 |               | 900      |
| FindRelatedProducts      |               | 200      |
| InstallFiles             |               | 4000     |
| InstallFinalize          |               | 6600     |
| InstallInitialize        |               | 1500     |
| InstallODBC              |               | 5400     |
| InstallServices          | VersionNT     | 5800     |
| InstallValidate          |               | 1400     |
| LaunchConditions         |               | 100      |
| MigrateFeatureStates     |               | 1200     |
| MoveFiles                |               | 3800     |
| PatchFiles               |               | 4090     |
| ProcessComponents        |               | 1600     |
| PublishComponents        |               | 6200     |
| PublishFeatures          |               | 6300     |
| PublishProduct           |               | 6400     |
| RegisterClassInfo        |               | 4600     |
| RegisterComPlus          |               | 5700     |
| RegisterExtensionInfo    |               | 4700     |
| RegisterFonts            |               | 5300     |
| RegisterMIMEInfo         |               | 4900     |
| RegisterProduct          |               | 6100     |
| RegisterProgIdInfo       |               | 4800     |
| RegisterTypeLibraries    |               | 5500     |
| RegisterUser             |               | 6000     |
| RemoveDuplicateFiles     |               | 3400     |
| RemoveEnvironmentStrings |               | 3300     |
| RemoveExistingProducts   |               | 6700     |
| RemoveFiles              |               | 3500     |
| RemoveFolders            |               | 3600     |
| RemoveIniValues          |               | 3100     |
| RemoveODBC               |               | 2400     |
| RemoveRegistryValues     |               | 2600     |
| RemoveShortcuts          |               | 3200     |
| RMCCPSearch              | NON installato | 600      |
| SelfRegModules           |               | 5600     |
| SelfUnregModules         |               | 2200     |
| SetODBCFolders           |               | 1100     |
| StartServices            | VersionNT     | 5900     |
| StopServices             | VersionNT     | 1900     |
| UnpublishComponents      |               | 1700     |
| UnpublishFeatures        |               | 1800     |
| UnregisterClassInfo      |               | 2700     |
| UnregisterComPlus        |               | 2100     |
| UnregisterExtensionInfo  |               | 2800     |
| UnregisterFonts          |               | 2500     |
| UnregisterMIMEInfo       |               | 3000     |
| UnregisterProgIdInfo     |               | 2900     |
| UnregisterTypeLibraries  |               | 2300     |
| ValidateProductID        |               | 700      |
| WriteEnvironmentStrings  |               | 5200     |
| WriteIniValues           |               | 5100     |
| WriteRegistryValori consente      |               | 5000     |



 

[Continua](importing-the-installuisequence.md)

 

 



