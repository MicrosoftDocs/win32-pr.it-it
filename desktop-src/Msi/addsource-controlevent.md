---
description: Questo evento notifica al programma di installazione, mantenendo la finestra di dialogo in esecuzione, che una funzionalità o tutte le funzionalità devono essere eseguite dall'origine.
ms.assetid: fd8d6433-87cc-4544-9f4f-57a90e5f2ea5
title: AddSource ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b0adff72ac14376c7084d6c3c005a77b2891019947cd22e8d73e58bfa09ad64
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145954"
---
# <a name="addsource-controlevent"></a>AddSource ControlEvent

Questo evento notifica al programma di installazione, mantenendo la finestra di dialogo in esecuzione, che una funzionalità o tutte le funzionalità devono essere eseguite dall'origine. Questo evento può essere pubblicato da un controllo [PushButton](pushbutton-control.md), [un controllo Checkbox](checkbox-control.md)o un controllo [SelectionTree](selectiontree-control.md). Questo evento deve essere creato nella tabella [ControlEvent](controlevent-table.md).

Questo ControlEvent richiede che l'interfaccia utente sia eseguita a livello [*completo dell'interfaccia*](f-gly.md) utente. Questo evento non funzionerà con un'interfaccia utente [*ridotta o*](r-gly.md) un'interfaccia utente [*di base.*](b-gly.md) Per informazioni, vedere [Livelli Interfaccia utente.](user-interface-levels.md)

## <a name="published-by"></a>Pubblicato da

Questo ControlEvent viene pubblicato dal programma di installazione.

## <a name="argument"></a>Argomento

Stringa, il nome della funzionalità o "ALL".

## <a name="action-on-subscribers"></a>Azione nei Sottoscrittori

Questo ControlEvent non esegue un'azione sui sottoscrittori.

## <a name="typical-use"></a>Utilizzo tipico

Un [controllo PushButton](pushbutton-control.md) in una finestra di dialogo modale è associato a questo evento e viene usato per inviare una notifica al programma di installazione senza arrestare la finestra di dialogo.

 

 



