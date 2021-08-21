---
description: L'azione StartServices avvia i servizi di sistema. Questa azione esegue una query sulla tabella ServiceControl.
ms.assetid: 53791b1c-5fd5-45d8-817b-098566ab4f9c
title: Azione StartServices
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 100ff7b927eb4bc157530cebe9767ef7a434d92f0b72f9e6c799b02a2969f5b6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119627531"
---
# <a name="startservices-action"></a>Azione StartServices

L'azione StartServices avvia i servizi di sistema. Questa azione esegue una query [sulla tabella ServiceControl](servicecontrol-table.md).

## <a name="sequence-restrictions"></a>Restrizioni di sequenza

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

Questa azione richiede che l'utente sia un amministratore o abbia privilegi elevati con autorizzazione per controllare i servizi o che l'applicazione sia parte di un'installazione gestita.

 

 



