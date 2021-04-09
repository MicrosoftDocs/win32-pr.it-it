---
description: Windows Installer possibile ottimizzare l'applicazione di patch per ridurre il tempo necessario per applicare le patch alle applicazioni installate.
ms.assetid: 2bb1c94a-55b6-4aee-b86d-ee9e1f8ed290
title: Ottimizzazione patch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86215855bb02314d7eb54c774541b0a2086c7c99
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880722"
---
# <a name="patch-optimization"></a>Ottimizzazione patch

Windows Installer possibile ottimizzare l'applicazione di patch per ridurre il tempo necessario per applicare le patch alle applicazioni installate.

**Windows Installer 2,0:** Non supportato. Per le versioni di Windows Installer rilasciate prima Windows Installer 3,0, l'applicazione di patch esegue un'installazione completa del ripristino dell'applicazione, che può richiedere molto più tempo.

**Windows Installer 3,0 e versioni successive:** Il processo di applicazione delle patch modifica solo le parti di un'applicazione modificate da una patch.

**Windows Installer 3,1 e versioni successive:** A partire da Windows Installer 3,1, per l'ottimizzazione della patch è necessario che in tutte le patch della transazione la proprietà OptimizedInstallMode sia impostata su 1 (una) nella [tabella MsiPatchMetadata](msipatchmetadata-table.md).

Se una patch modifica solo le tabelle seguenti, Windows Installer 3,0 o versioni successive ignora le azioni associate a tutte le altre tabelle, anche se tali azioni sono elencate nelle tabelle di sequenza del pacchetto di installazione dell'applicazione originale (file con estensione msi).

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
-   [PacchettoPatch](patchpackage-table.md)
-   [Proprietà](property-table.md)
-   [Registro](registry-table.md)
-   [SFPCatalog](sfpcatalog-table.md)
-   [TypeLib](typelib-table.md)
-   [\_Colonne](-columns-table.md)
-   [\_Depositi](-storages-table.md)
-   [\_Flussi](-streams-table.md)
-   [\_Tabelle](-tables-table.md)
-   [\_Tabella transformview](-transformview-table.md)
-   [\_Convalida](-validation-table.md)

Per disattivare l'opzione di ottimizzazione della patch, usare il criterio [DisableFlyWeightPatching](disableflyweightpatching.md) .

 

 



