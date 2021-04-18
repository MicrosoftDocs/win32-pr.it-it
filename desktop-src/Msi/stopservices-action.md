---
description: L'azione StopServices interrompe i servizi di sistema. Questa azione esegue una query sulla tabella ServiceControl.
ms.assetid: 1ad01205-f8b6-400f-be1d-c00a5b71ccfd
title: Azione StopServices
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31cb271b99c434a1ac54ab9744697b991e9e1fcc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308680"
---
# <a name="stopservices-action"></a>Azione StopServices

L'azione StopServices interrompe i servizi di sistema. Questa azione esegue una query sulla [tabella ServiceControl](servicecontrol-table.md).

## <a name="sequence-restrictions"></a>Restrizioni sequenza

Le azioni dei servizi devono essere usate nella sequenza seguente:

-   StopServices
-   [DeleteServices](deleteservices-action.md)

Una delle azioni seguenti:

-   [InstallFiles](installfiles-action.md)
-   [RemoveFiles](removefiles-action.md)
-   [DuplicateFiles](duplicatefiles-action.md)
-   [MoveFiles](movefiles-action.md)
-   [PatchFiles](patchfiles-action.md)
-   [RemoveDuplicateFiles](removeduplicatefiles-action.md)
-   [InstallServices](installservices-action.md)
-   [StartServices](startservices-action.md)

## <a name="actiondata-messages"></a>Messaggi ActionData



| Campo | Descrizione dei dati dell'azione |
|-------|----------------------------|
| \[1\] | Nome visualizzato del servizio.      |
| \[2\] | Nome del servizio.              |



 

## <a name="remarks"></a>Commenti

Per questa azione è necessario che l'utente sia un amministratore o disponga di privilegi elevati con l'autorizzazione per controllare i servizi o che l'applicazione faccia parte di un'installazione gestita.

 

 



