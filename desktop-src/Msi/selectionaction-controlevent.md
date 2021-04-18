---
description: Il controllo SelectionTree usa questo evento per pubblicare una stringa che descrive l'elemento evidenziato. La stringa è uno dei &\# 0034; SEL \* & \# 0034; stringhe della tabella UIText. Questo evento deve essere creato nella tabella EventMapping.
ms.assetid: 7770b46f-21c7-459f-9778-a86de70d467f
title: ControlEvent SelectionAction
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eda06826f6ac649e2278441c944cdea0332689af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319432"
---
# <a name="selectionaction-controlevent"></a>ControlEvent SelectionAction

Il [controllo SelectionTree](selectiontree-control.md) usa questo evento per pubblicare una stringa che descrive l'elemento evidenziato. La stringa è una delle stringhe "SEL \* " della [tabella UIText](uitext-table.md). Questo evento deve essere creato nella [tabella EventMapping](eventmapping-table.md).

Questo ControlEvent richiede l'esecuzione dell'interfaccia utente a livello di [*interfaccia utente completo*](f-gly.md) . Questo evento non funzionerà con un'interfaccia utente [*ridotta*](r-gly.md) o un' [*interfaccia utente di base*](b-gly.md). Per informazioni, vedere [livelli di interfaccia utente](user-interface-levels.md).

Questo evento può influire solo sui controlli che si trovano nella stessa finestra di dialogo del controllo SelectionTree.

## <a name="published-by"></a>Pubblicato da

[SelectionTree](selectiontree-control.md)

## <a name="argument"></a>Argomento

Nessuna.

## <a name="action-on-subscribers"></a>Azione sui sottoscrittori

Nessuna.

## <a name="typical-use"></a>Utilizzo tipico

Un controllo di [testo](text-control.md) nella stessa finestra di dialogo modale del SelectionTree deve sottoscrivere questo evento tramite la [tabella EventMapping](eventmapping-table.md). Il controllo testo Visualizza la spiegazione dell'elemento selezionato.

 

 



