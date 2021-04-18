---
description: Il controllo SelectionTree usa l'evento SelectionPathOn per pubblicare un valore booleano che indica se è presente un percorso di selezione associato alla funzionalità attualmente selezionata. Questo evento deve essere creato nella tabella EventMapping.
ms.assetid: 441b9416-066a-429b-92d2-555584a20fa2
title: ControlEvent SelectionPathOn
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9882ea534a0d4c91a0107ce3949363350a17fbea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319428"
---
# <a name="selectionpathon-controlevent"></a>ControlEvent SelectionPathOn

Il [controllo SelectionTree](selectiontree-control.md) usa l'evento SelectionPathOn per pubblicare un valore booleano che indica se è presente un percorso di selezione associato alla funzionalità attualmente selezionata. Questo evento deve essere creato nella [tabella EventMapping](eventmapping-table.md).

Questo evento può influire solo sui controlli che si trovano nella stessa finestra di dialogo del controllo SelectionTree.

Questo ControlEvent richiede l'esecuzione dell'interfaccia utente a livello di [*interfaccia utente completo*](f-gly.md) . Questo evento non funzionerà con un'interfaccia utente [*ridotta*](r-gly.md) o un' [*interfaccia utente di base*](b-gly.md). Per informazioni, vedere [livelli di interfaccia utente](user-interface-levels.md).

Il ControlEvent SelectionPathOn non viene mai pubblicato durante un' [installazione di manutenzione](maintenance-installation.md).

## <a name="published-by"></a>Pubblicato da

[SelectionTree](selectiontree-control.md)

## <a name="argument"></a>Argomento

Nessuna.

## <a name="action-on-subscribers"></a>Azione sui sottoscrittori

Nessuna.

## <a name="typical-use"></a>Utilizzo tipico

Un controllo di [testo](text-control.md) nella stessa finestra di dialogo modale del SelectionTree deve sottoscrivere l'evento tramite la [tabella EventMapping](eventmapping-table.md). Il controllo testo Visualizza la didascalia del percorso di selezione. Questo controllo testo è visibile o nascosto a seconda dell'evento.

 

 



