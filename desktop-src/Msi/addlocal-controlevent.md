---
description: Questo evento notifica al programma di installazione, mantenendo la finestra di dialogo in esecuzione, che una funzionalità o tutte le funzionalità devono essere eseguite in locale.
ms.assetid: 074f347e-37d3-4365-a25d-caa0392a0dbc
title: AddLocal ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfb2db93bea39d167d5b8f08af2cdecfcb07194fb68d4c1e39f5511e2a09f8c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118639564"
---
# <a name="addlocal-controlevent"></a>AddLocal ControlEvent

Questo evento notifica al programma di installazione, mantenendo la finestra di dialogo in esecuzione, che una funzionalità o tutte le funzionalità devono essere eseguite in locale. Questo evento può essere pubblicato da un controllo [PushButton](pushbutton-control.md), [un controllo Checkbox](checkbox-control.md)o un controllo [SelectionTree](selectiontree-control.md). Questo evento deve essere creato nella tabella [ControlEvent](controlevent-table.md).

Questo ControlEvent richiede che l'interfaccia utente sia eseguita a livello [*completo dell'interfaccia*](f-gly.md) utente. Questo evento non funzionerà con un'interfaccia utente [*ridotta o*](r-gly.md) un'interfaccia utente [*di base.*](b-gly.md) Per informazioni, vedere [Interfaccia utente Levels.](user-interface-levels.md)

## <a name="published-by"></a>Pubblicato da

Questo ControlEvent viene pubblicato dal programma di installazione.

## <a name="argument"></a>Argomento

Stringa, il nome della funzionalità o "ALL".

## <a name="action-on-subscribers"></a>Azione nei Sottoscrittori

Questo ControlEvent non esegue un'azione sui sottoscrittori.

## <a name="typical-use"></a>Utilizzo tipico

Un [controllo PushButton](pushbutton-control.md) in una finestra di dialogo modale è associato a questo evento e viene usato per inviare una notifica al programma di installazione senza arrestare la finestra di dialogo.

 

 



