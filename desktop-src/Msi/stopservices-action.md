---
description: L'azione StopServices arresta i servizi di sistema. Questa azione esegue una query sulla tabella ServiceControl.
ms.assetid: 1ad01205-f8b6-400f-be1d-c00a5b71ccfd
title: Azione StopServices
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fee0082d1588c3a1486b51bd4f06869374e1f6babfa71d309d65512e1ff1b0b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119627381"
---
# <a name="stopservices-action"></a>Azione StopServices

L'azione StopServices arresta i servizi di sistema. Questa azione esegue una query [sulla tabella ServiceControl](servicecontrol-table.md).

## <a name="sequence-restrictions"></a>Restrizioni relative alle sequenze

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

Questa azione richiede che l'utente sia un amministratore o abbia privilegi elevati con l'autorizzazione per controllare i servizi o che l'applicazione sia parte di un'installazione gestita.

 

 



