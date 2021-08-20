---
description: L'azione DeleteServices arresta un servizio e rimuove la registrazione dal sistema. Questa azione esegue una query sulla tabella ServiceControl.
ms.assetid: c7976de9-65f4-4552-8f8c-e7a32ef4821d
title: Azione DeleteServices
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bd00b9d077239402817bdf40dc10ee1de9bdbff4b52998742434933c3e9dd8a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118379117"
---
# <a name="deleteservices-action"></a>Azione DeleteServices

L'azione DeleteServices arresta un servizio e rimuove la registrazione dal sistema. Questa azione esegue una query [sulla tabella ServiceControl](servicecontrol-table.md).

## <a name="sequence-restrictions"></a>Restrizioni relative alle sequenze

Le azioni dei servizi devono essere usate nella sequenza seguente:

1.  [StopServices](stopservices-action.md)
2.  DeleteServices
3.  Una delle azioni seguenti: [InstallFiles,](installfiles-action.md) [RemoveFiles,](removefiles-action.md) [DuplicateFiles,](duplicatefiles-action.md) [MoveFiles,](movefiles-action.md) [PatchFiles](patchfiles-action.md)e [RemoveDuplicateFiles.](removeduplicatefiles-action.md)
4.  [Azione InstallServices](installservices-action.md)
5.  [StartServices](startservices-action.md)

## <a name="actiondata-messages"></a>Messaggi ActionData



| Campo | Descrizione dei dati dell'azione |
|-------|----------------------------|
| \[1\] | Nome visualizzato del servizio.      |
| \[2\] | Nome del servizio.              |



 

## <a name="remarks"></a>Commenti

Questa azione richiede che l'utente sia un amministratore o abbia privilegi elevati con l'autorizzazione per eliminare i servizi o che l'applicazione sia parte di un'installazione gestita.

 

 



