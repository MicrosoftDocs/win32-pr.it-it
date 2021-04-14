---
description: Il controllo SelectionTree usa l'evento SelectionBrowse per generare una finestra di dialogo di esplorazione che consente di modificare il percorso dell'elemento evidenziato.
ms.assetid: 10a5af2e-3144-4b51-8295-294e56cdf801
title: ControlEvent SelectionBrowse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 754f69f939f7c90dca705a2669a37af1fce0e79a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104350226"
---
# <a name="selectionbrowse-controlevent"></a>ControlEvent SelectionBrowse

Il [controllo SelectionTree](selectiontree-control.md) usa l'evento SelectionBrowse per generare una finestra di dialogo di **esplorazione** che consente di modificare il percorso dell'elemento evidenziato.

Questo evento deve essere pubblicato da un [controllo pulsante](pushbutton-control.md) che si trova nella stessa finestra di dialogo del controllo che sottoscrive questo evento. L'evento deve essere creato nella [tabella ControlEvent](controlevent-table.md).

Questo ControlEvent richiede l'esecuzione dell'interfaccia utente a livello di [*interfaccia utente completo*](f-gly.md) . Questo evento non funzionerà con un'interfaccia utente [*ridotta*](r-gly.md) o un' [*interfaccia utente di base*](b-gly.md). Per informazioni, vedere [livelli di interfaccia utente](user-interface-levels.md).

Tutti i controlli che pubblicano un evento SelectionBrowse diventano disabilitati se è stata selezionata una funzionalità già installata, non configurabile o non selezionata per l'installazione locale. Per poter essere configurata, la funzionalità deve avere una [proprietà pubblica](public-properties.md) immessa nel \_ campo Directory della [tabella delle funzionalità](feature-table.md).

## <a name="published-by"></a>Pubblicato da

[SelectionTree](selectiontree-control.md)

## <a name="argument"></a>Argomento

Nome della finestra di dialogo da generare.

## <a name="action-on-subscribers"></a>Azione sui sottoscrittori

Nessuna.

## <a name="typical-use"></a>Utilizzo tipico

Un controllo [pulsante](pushbutton-control.md) nella stessa finestra di dialogo modale del SelectionTree utilizza questo evento per attivare la finestra di dialogo **Sfoglia** .

 

 



