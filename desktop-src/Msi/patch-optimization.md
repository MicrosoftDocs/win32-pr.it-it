---
description: Windows Il programma di installazione può ottimizzare l'applicazione delle patch per ridurre il tempo necessario per applicare le patch alle applicazioni installate.
ms.assetid: 2bb1c94a-55b6-4aee-b86d-ee9e1f8ed290
title: Ottimizzazione delle patch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fee37ba48764f6249410a6dfc2512245aa6ca6dfca68cff09ec15e06a42f9156
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118627644"
---
# <a name="patch-optimization"></a>Ottimizzazione delle patch

Windows Il programma di installazione può ottimizzare l'applicazione delle patch per ridurre il tempo necessario per applicare le patch alle applicazioni installate.

**Windows Installer 2.0:** Non supportato. Per le versioni di Windows Installer rilasciate prima di Windows Installer 3.0, l'applicazione di patch esegue un'installazione di ripristino completa dell'applicazione, che può richiedere molto più tempo.

**Windows Installer 3.0 e versioni successive:** Il processo di applicazione delle patch modifica solo le parti di un'applicazione modificate da una patch.

**Windows Installer 3.1 e versioni successive:** A partire da Windows Installer 3.1, l'ottimizzazione delle patch richiede che per tutte le patch nella transazione la proprietà OptimizedInstallMode sia impostata su 1 (uno) nella tabella [MsiPatchMetadata](msipatchmetadata-table.md).

Se una patch modifica solo le tabelle seguenti, Windows Installer 3.0 o versione successiva ignora le azioni associate a tutte le altre tabelle, anche se tali azioni sono elencate nelle tabelle di sequenza del pacchetto di installazione dell'applicazione originale (file .msi).

-   [AdminExecuteSequence](adminexecutesequence-table.md)
-   [AdminUISequence](adminuisequence-table.md)
-   [Condition](condition-table.md)
-   [CustomAction](customaction-table.md)
-   [File](file-table.md)
-   [FileSFPCatalog](filesfpcatalog-table.md)
-   [InstallExecuteSequence](installexecutesequence-table.md)
-   [InstallUISequence](installuisequence-table.md)
-   [Supporti](media-table.md)
-   [MoveFile](movefile-table.md)
-   [MsiAssembly](msiassembly-table.md)
-   [MsiDigitalCertificate](msidigitalcertificate-table.md)
-   [MsiDigitalSignature](msidigitalsignature-table.md)
-   [MsiFileHash](msifilehash-table.md)
-   [MsiPatchHeaders](msipatchheaders-table.md)
-   [Patch](patch-table.md)
-   [PatchPackage](patchpackage-table.md)
-   [Proprietà](property-table.md)
-   [Registro](registry-table.md)
-   [SFPCatalog](sfpcatalog-table.md)
-   [Typelib](typelib-table.md)
-   [\_Colonne](-columns-table.md)
-   [\_Depositi](-storages-table.md)
-   [\_Flussi](-streams-table.md)
-   [\_Tabelle](-tables-table.md)
-   [\_Tabella TransformView](-transformview-table.md)
-   [\_Convalida](-validation-table.md)

Per disattivare l'opzione di ottimizzazione della patch, usare il [criterio DisableFlyWeightPatching.](disableflyweightpatching.md)

 

 



