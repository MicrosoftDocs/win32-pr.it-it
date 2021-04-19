---
description: L'azione MsiConfigureServices configura un servizio per il sistema. Questa azione esegue una query sulle tabelle MsiServiceConfig e MsiServiceConfigFailureActions.
ms.assetid: 63bd4690-0649-4e23-a8cd-527b3c517dae
title: Azione MsiConfigureServices
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21f2321bcdfaeede8e80d7f4c341f5a099690952
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319965"
---
# <a name="msiconfigureservices-action"></a>Azione MsiConfigureServices

L'azione MsiConfigureServices configura un servizio per il sistema. Questa azione esegue una query sulle tabelle [MsiServiceConfig](msiserviceconfig-table.md) e [MsiServiceConfigFailureActions](msiserviceconfigfailureactions-table.md) .

**[Windows Installer 4,5 o versioni precedenti](not-supported-in-windows-installer-4-5.md):** Non supportato. Questa azione è disponibile a partire da Windows Installer 5,0.

> [!IMPORTANT]
>
> Servizi Windows offre la possibilità di eseguire automaticamente azioni predefinite in risposta a un errore in un servizio. Per supportare l'impostazione a livello di codice di queste **azioni di ripristino** in caso di errore di un servizio, [MsiServiceConfigFailureActions](msiserviceconfigfailureactions-table.md) è stato aggiunto a msi nella versione MSI 5,0. Tuttavia, questa funzionalità non funziona come previsto.
>
> Per aggirare questo problema, uno sviluppatore di applicazioni deve utilizzare la funzionalità **azione personalizzata** in MSI per eseguire **sc.exe** e impostare le **Opzioni di ripristino** in modo appropriato.

 

## <a name="sequence-restrictions"></a>Restrizioni sequenza

Questa azione standard deve essere utilizzata nella sequenza seguente.

[StopServices](stopservices-action.md)

[DeleteServices](deleteservices-action.md)

Una delle azioni seguenti: [InstallFiles](installfiles-action.md), [RemoveFiles](removefiles-action.md), [DuplicateFiles](duplicatefiles-action.md), [MoveFiles](movefiles-action.md), [PatchFiles](patchfiles-action.md)e [RemoveDuplicateFiles](removeduplicatefiles-action.md) .

[InstallServices](installservices-action.md)

MsiConfigureServices

[StartServices](startservices-action.md)

## <a name="actiondata-messages"></a>Messaggi ActionData

Nessun messaggio ActionData.

## <a name="remarks"></a>Commenti

Per questa azione è necessario che l'utente sia un amministratore o disponga di privilegi elevati con l'autorizzazione per installare i servizi o che l'applicazione faccia parte di un'installazione gestita.

 

 



