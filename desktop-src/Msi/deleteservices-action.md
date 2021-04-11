---
description: L'azione DeleteServices arresta un servizio e ne rimuove la registrazione dal sistema. Questa azione esegue una query sulla tabella ServiceControl.
ms.assetid: c7976de9-65f4-4552-8f8c-e7a32ef4821d
title: Azione DeleteServices
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c5fc22bbb0c11cd546f1ffbb9f3ad98e06efae3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346346"
---
# <a name="deleteservices-action"></a>Azione DeleteServices

L'azione DeleteServices arresta un servizio e ne rimuove la registrazione dal sistema. Questa azione esegue una query sulla [tabella ServiceControl](servicecontrol-table.md).

## <a name="sequence-restrictions"></a>Restrizioni sequenza

Le azioni dei servizi devono essere usate nella sequenza seguente:

1.  [StopServices](stopservices-action.md)
2.  DeleteServices
3.  Una delle azioni seguenti: [InstallFiles](installfiles-action.md), [RemoveFiles](removefiles-action.md), [DuplicateFiles](duplicatefiles-action.md), [MoveFiles](movefiles-action.md), [PatchFiles](patchfiles-action.md)e [RemoveDuplicateFiles](removeduplicatefiles-action.md) .
4.  [Azione InstallServices](installservices-action.md)
5.  [StartServices](startservices-action.md)

## <a name="actiondata-messages"></a>Messaggi ActionData



| Campo | Descrizione dei dati dell'azione |
|-------|----------------------------|
| \[1\] | Nome visualizzato del servizio.      |
| \[2\] | Nome del servizio.              |



 

## <a name="remarks"></a>Commenti

Questa azione richiede che l'utente sia un amministratore o disponga di privilegi elevati con l'autorizzazione per eliminare i servizi o che l'applicazione faccia parte di un'installazione gestita.

 

 



