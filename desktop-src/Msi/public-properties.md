---
description: Le proprietà pubbliche possono essere scritte nel database di installazione nello stesso modo delle proprietà private.
ms.assetid: 032aa55f-d97a-4455-bd32-571b0e05763b
title: Proprietà pubbliche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0138db2fcbe664ac9a4064379486c42c3d52a6896fc53a608b99192a8d70c75
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119828431"
---
# <a name="public-properties"></a>Proprietà pubbliche

Le proprietà pubbliche possono essere scritte nel database di installazione nello stesso modo delle [proprietà private](private-properties.md). Inoltre, i valori delle proprietà pubbliche possono essere modificati da un utente o da un amministratore di sistema impostando la proprietà nella riga di comando, applicando una trasformazione o interagendo con un'interfaccia utente personalizzata. I nomi delle proprietà pubbliche non possono contenere lettere minuscole. Vedere [Restrizioni sui nomi delle proprietà](restrictions-on-property-names.md).

Le proprietà pubbliche vengono in genere impostate dagli utenti durante l'installazione. Ad esempio, la proprietà pubblica [**INSTALLLEVEL**](installlevel.md) può essere specificata nella riga di comando usata per avviare l'installazione o scelta tramite un'interfaccia utente personalizzata.

I valori delle proprietà pubbliche possono essere sostituiti da [](custom-actions.md) una riga di comando, tramite un'azione [standard](standard-actions.md) o personalizzata, applicando una trasformazione o facendo in modo che l'utente interagisca con un'interfaccia utente personalizzata. Per cancellare una proprietà pubblica nella tabella delle proprietà, lasciarla fuori dalla tabella. Le proprietà che devono essere impostate dall'interfaccia utente durante l'installazione e quindi passate alla fase di esecuzione dell'installazione devono essere pubbliche.

Per un elenco delle proprietà pubbliche standard usate dal programma di installazione, vedere [Informazioni di riferimento sulla proprietà](property-reference.md). Un autore può anche definire una proprietà pubblica personalizzata immettendo il nome della proprietà e un valore iniziale nella [tabella Proprietà](property-table.md). Tutte le proprietà pubbliche possono essere sottoposte a override da tutti gli utenti se si verifica una delle condizioni seguenti.

-   L'utente è un amministratore di sistema.
-   Il criterio EnableUserControl per computer è impostato su 1. Vedere [Criteri di sistema](system-policy.md).
-   La [**proprietà EnableUserControl**](-enableusercontrol.md) è impostata su 1.
-   Si tratta di un'installazione non gestita che non viene eseguita con privilegi elevati.

Se nessuna delle condizioni precedenti è vera, per impostazione predefinita il programma di installazione limita le proprietà pubbliche che possono essere sostituite da un utente che non è un amministratore di sistema. Vedere [**Proprietà pubbliche con restrizioni**](restricted-public-properties.md).

 

 



