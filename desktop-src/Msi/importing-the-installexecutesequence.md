---
description: La tabella InstallExecuteSequence elenca le azioni eseguite quando il programma di installazione esegue l'azione INSTALL di primo livello. Vedere Installation Procedure Tables Group, Using a Sequence Table (Gruppo di tabelle delle procedure di installazione), Using a Sequence Table (Uso di una tabella di sequenza) e Sequence Table Detailed Example (Esempio dettagliato della tabella sequence).
ms.assetid: cdd4f02a-cfe6-4a23-9fc2-f4cb810379aa
title: Importazione di InstallExecuteSequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 586557130c6aa9af197d5d28f6bd750f4de736feb6982f3b7f12ce73ccf41c83
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119430771"
---
# <a name="importing-the-installexecutesequence"></a>Importazione di InstallExecuteSequence

La [tabella InstallExecuteSequence](installexecutesequence-table.md) elenca le azioni eseguite quando il programma di installazione esegue l'azione [INSTALL di primo livello.](install-action.md) Vedere [Installation Procedure Tables Group](installation-procedure-tables-group.md), Using a Sequence [Table](using-a-sequence-table.md)e Sequence [Table Detailed Example](sequence-table-detailed-example.md).

Se nella sezione Importazione di un [database](importing-a-blank-database.md) vuoto è stato usato uisample.msi da Windows Installer SDK, le tabelle di sequenza nella copia di MNP2000.msi contengono già le sequenze di azione suggerite descritte in [Uso](using-a-sequence-table.md)di una tabella di sequenza . Non sono necessarie modifiche a queste sequenze per creare il Blocco note di installazione.

Usare l'editor di database per MNP2000.msi e immettere i dati seguenti nella tabella InstallExecuteSequence.

[Tabella InstallExecuteSequence](installexecutesequence-table.md)



| Azione                   | Condition     | Sequenza |
|--------------------------|---------------|----------|
| AllocateRegistrySpace    | NON installato | 1550     |
| Appsearch                |               | 400      |
| BindImage                |               | 4300     |
| CCPSearch                | NON installato | 500      |
| CostFinalize             |               | 1000     |
| CostInitialize           |               | 800      |
| CreateFolders            |               | 3700     |
| CreateShortcuts          |               | 4500     |
| DeleteServices           | VersionNT     | 2000     |
| DuplicateFiles           |               | 4210     |
| FileCost                 |               | 900      |
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
| WriteRegistryValues      |               | 5000     |



 

[Continua](importing-the-installuisequence.md)

 

 



