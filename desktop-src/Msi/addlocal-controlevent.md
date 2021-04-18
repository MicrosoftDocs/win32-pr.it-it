---
description: Questo evento invia una notifica al programma di installazione, mantenendo la finestra di dialogo attualmente in esecuzione, che una funzionalità o tutte le funzionalità devono essere eseguite localmente.
ms.assetid: 074f347e-37d3-4365-a25d-caa0392a0dbc
title: ControlEvent AddLocal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 112975d31e341c06a21609b173b9682283e71610
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311074"
---
# <a name="addlocal-controlevent"></a>ControlEvent AddLocal

Questo evento invia una notifica al programma di installazione, mantenendo la finestra di dialogo attualmente in esecuzione, che una funzionalità o tutte le funzionalità devono essere eseguite localmente. Questo evento può essere pubblicato tramite un controllo [pulsante](pushbutton-control.md), un [controllo CheckBox](checkbox-control.md)o un [controllo SelectionTree](selectiontree-control.md). Questo evento deve essere creato nella [tabella ControlEvent](controlevent-table.md).

Questo ControlEvent richiede l'esecuzione dell'interfaccia utente a livello di [*interfaccia utente completo*](f-gly.md) . Questo evento non funzionerà con un'interfaccia utente [*ridotta*](r-gly.md) o un' [*interfaccia utente di base*](b-gly.md). Per informazioni, vedere [livelli di interfaccia utente](user-interface-levels.md).

## <a name="published-by"></a>Pubblicato da

Questo ControlEvent viene pubblicato dal programma di installazione.

## <a name="argument"></a>Argomento

Stringa, ovvero il nome della funzionalità o "ALL".

## <a name="action-on-subscribers"></a>Azione sui sottoscrittori

Questo ControlEvent non esegue un'azione sui sottoscrittori.

## <a name="typical-use"></a>Utilizzo tipico

Un controllo [pulsante](pushbutton-control.md) in una finestra di dialogo modale è associato a questo evento e utilizzato per notificare al programma di installazione senza arrestare la finestra di dialogo.

 

 



