---
description: L'azione StartServices avvia i servizi di sistema. Questa azione esegue una query sulla tabella ServiceControl.
ms.assetid: 53791b1c-5fd5-45d8-817b-098566ab4f9c
title: Azione StartServices
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9c150a8970c5852d9cfc53581290e792c00b628
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310512"
---
# <a name="startservices-action"></a>Azione StartServices

L'azione StartServices avvia i servizi di sistema. Questa azione esegue una query sulla [tabella ServiceControl](servicecontrol-table.md).

## <a name="sequence-restrictions"></a>Restrizioni sequenza

Le azioni dei servizi devono essere usate nella sequenza seguente:

-   [StopServices](stopservices-action.md)
-   [DeleteServices](deleteservices-action.md)

Una delle azioni seguenti:

-   [InstallFiles](installfiles-action.md)
-   [RemoveFiles](removefiles-action.md)
-   [DuplicateFiles](duplicatefiles-action.md)
-   [MoveFiles](movefiles-action.md)
-   [PatchFiles](patchfiles-action.md)
-   [RemoveDuplicateFiles](removeduplicatefiles-action.md)
-   [InstallServices](installservices-action.md)
-   StartServices

## <a name="actiondata-messages"></a>Messaggi ActionData



| Campo | Descrizione dei dati dell'azione |
|-------|----------------------------|
| \[1\] | Nome visualizzato del servizio.      |
| \[2\] | Nome del servizio.              |



 

## <a name="remarks"></a>Commenti

Per questa azione è necessario che l'utente sia un amministratore o disponga di privilegi elevati con l'autorizzazione per controllare i servizi o che l'applicazione faccia parte di un'installazione gestita.

 

 



