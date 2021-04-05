---
description: È possibile creare proprietà pubbliche nel database di installazione in modo analogo alle proprietà private.
ms.assetid: 032aa55f-d97a-4455-bd32-571b0e05763b
title: Proprietà pubbliche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 822dfc55e0ab659e5580580edd04eb156540cb61
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881498"
---
# <a name="public-properties"></a>Proprietà pubbliche

È possibile creare proprietà pubbliche nel database di installazione in modo analogo alle [proprietà private](private-properties.md). Inoltre, i valori delle proprietà pubbliche possono essere modificati da un utente o da un amministratore di sistema impostando la proprietà nella riga di comando, applicando una trasformazione o interagendo con un'interfaccia utente creata. I nomi di proprietà pubbliche non possono contenere lettere minuscole. Vedere [restrizioni sui nomi di proprietà](restrictions-on-property-names.md).

Le proprietà pubbliche vengono generalmente impostate dagli utenti durante l'installazione. Ad esempio, la proprietà Public Property [**INSTALLLEVEL**](installlevel.md) può essere specificata nella riga di comando usata per avviare l'installazione o scelta mediante un'interfaccia utente creata.

È possibile eseguire l'override dei valori delle proprietà pubbliche in una riga di comando, usando un'azione [standard](standard-actions.md) o [personalizzata](custom-actions.md) , applicando una trasformazione o facendo in modo che l'utente interagisca con un'interfaccia utente creata. Per cancellare una proprietà pubblica nella tabella delle proprietà, lasciarla fuori dalla tabella. Le proprietà che devono essere impostate dall'interfaccia utente durante l'installazione e quindi passate alla fase di esecuzione dell'installazione devono essere pubbliche.

Per un elenco delle proprietà pubbliche standard usate dal programma di installazione, vedere [riferimento alle proprietà](property-reference.md). Un autore può anche definire una proprietà pubblica personalizzata immettendo il nome della proprietà e un valore iniziale nella [tabella delle proprietà](property-table.md). Tutti gli utenti possono eseguire l'override di tutte le proprietà pubbliche se si verifica una delle condizioni seguenti.

-   L'utente è un amministratore di sistema.
-   Il criterio EnableUserControl per computer è impostato su 1. Vedere [criteri di sistema](system-policy.md).
-   La proprietà [**EnableUserControl**](-enableusercontrol.md) è impostata su 1.
-   Si tratta di un'installazione non gestita che non viene eseguita con privilegi elevati.

Se nessuna delle condizioni precedenti è true, per impostazione predefinita il programma di installazione limita le proprietà pubbliche di cui è possibile eseguire l'override da un utente che non è un amministratore di sistema. Vedere [**proprietà pubbliche limitate**](restricted-public-properties.md).

 

 



