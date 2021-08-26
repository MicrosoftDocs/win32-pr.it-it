---
description: Il controllo SelectionTree usa l'evento SelectionPathOn per pubblicare un valore booleano che indica se è presente un percorso di selezione associato alla funzionalità attualmente selezionata. Questo evento deve essere creato nella tabella EventMapping.
ms.assetid: 441b9416-066a-429b-92d2-555584a20fa2
title: SelectionPathOn ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fea32926117c200f466bd2c40ac611e7ccbc47fb6a231a5dcf93ffa2ee0446b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120040431"
---
# <a name="selectionpathon-controlevent"></a>SelectionPathOn ControlEvent

Il [controllo SelectionTree usa](selectiontree-control.md) l'evento SelectionPathOn per pubblicare un valore booleano che indica se è presente un percorso di selezione associato alla funzionalità attualmente selezionata. Questo evento deve essere creato nella [tabella EventMapping](eventmapping-table.md).

Questo evento può influire solo sui controlli che si trovano nella stessa finestra di dialogo del controllo SelectionTree.

Questo ControlEvent richiede che l'interfaccia utente sia eseguita a livello [*completo dell'interfaccia*](f-gly.md) utente. Questo evento non funzionerà con un'interfaccia [*utente ridotta*](r-gly.md) o un'interfaccia utente [*di base.*](b-gly.md) Per informazioni, vedere Livelli [Interfaccia utente.](user-interface-levels.md)

SelectionPathOn ControlEvent non viene mai pubblicato durante [un'installazione di manutenzione.](maintenance-installation.md)

## <a name="published-by"></a>Pubblicato da

[SelectionTree](selectiontree-control.md)

## <a name="argument"></a>Argomento

Nessuno.

## <a name="action-on-subscribers"></a>Azione nei Sottoscrittori

Nessuno.

## <a name="typical-use"></a>Utilizzo tipico

Un [controllo Text](text-control.md) nella stessa finestra di dialogo modale di SelectionTree deve sottoscrivere l'evento tramite la tabella [EventMapping](eventmapping-table.md). Il controllo Text visualizza la didascalia del percorso di selezione. Questo controllo di testo è visibile o nascosto a seconda dell'evento .

 

 



