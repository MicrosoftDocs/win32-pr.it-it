---
description: Il programma di installazione usa questo evento per pubblicare il nome dell'azione presente. Il nome può essere visualizzato in una finestra di dialogo da un controllo di testo che sottoscrive questo ControlEvent. Questo evento deve essere creato nella tabella EventMapping.
ms.assetid: 2b4928fe-2d5c-46c1-8a31-cbebbc78d304
title: ActionText ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a216cb30dbcaa0be9972f12f7a83c8e45e5bb5686d93ce210bf96087aa3c4552
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119927381"
---
# <a name="actiontext-controlevent"></a>ActionText ControlEvent

Il programma di installazione usa questo evento per pubblicare il nome dell'azione presente. Il nome può essere visualizzato in una finestra di dialogo da un [controllo di testo](text-control.md) che sottoscrive questo ControlEvent. Questo evento deve essere creato nella [tabella EventMapping](eventmapping-table.md).

Questo ControlEvent può essere gestito da un'interfaccia utente eseguita a livello di interfaccia utente di [*base,*](b-gly.md)interfaccia [*utente*](r-gly.md)ridotta [*o interfaccia utente*](f-gly.md) completa. Per informazioni sui livelli dell'interfaccia utente, [vedere Interfaccia utente Livelli.](user-interface-levels.md)

## <a name="published-by"></a>Pubblicato da

Questo ControlEvent viene pubblicato dal programma di installazione.

## <a name="argument"></a>Argomento

Questo ControlEvent non usa un argomento.

## <a name="action-on-subscribers"></a>Azione nei Sottoscrittori

I sottoscrittori vengono visualizzati quando un nuovo stato di avanzamento arriva dal programma di installazione.

## <a name="typical-use"></a>Utilizzo tipico

Un [controllo di testo](text-control.md) in una finestra di dialogo non modali sottoscrive questo evento tramite la tabella [EventMapping](eventmapping-table.md). [L'attributo text control](text-control-attribute.md) deve essere elencato nel campo Attributi di questa tabella per ricevere il nome dell'azione corrente.

 

 



