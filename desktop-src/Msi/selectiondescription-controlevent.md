---
description: Il controllo SelectionTree usa l'evento SelectionDescription per pubblicare una stringa che contiene la descrizione dell'elemento evidenziato. Questa stringa è il campo della descrizione della tabella delle funzionalità. Questo evento deve essere creato nella tabella EventMapping.
ms.assetid: 29ae9aec-764f-4ff2-9c08-805538130cb1
title: ControlEvent SelectionDescription
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 901db4efbed03341243d1b978dab0b8759fbc02c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313332"
---
# <a name="selectiondescription-controlevent"></a>ControlEvent SelectionDescription

Il [controllo SelectionTree](selectiontree-control.md) usa l'evento SelectionDescription per pubblicare una stringa che contiene la descrizione dell'elemento evidenziato. Questa stringa è il campo della **Descrizione** della [tabella delle funzionalità](feature-table.md). Questo evento deve essere creato nella [tabella EventMapping](eventmapping-table.md).

Questo evento può influire solo sui controlli che si trovano nella stessa finestra di dialogo del [controllo SelectionTree](selectiontree-control.md).

Questo ControlEvent richiede l'esecuzione dell'interfaccia utente a livello di [*interfaccia utente completo*](f-gly.md) . Questo evento non funzionerà con un'interfaccia utente [*ridotta*](r-gly.md) o un' [*interfaccia utente di base*](b-gly.md). Per ulteriori informazioni, vedere [livelli di interfaccia utente](user-interface-levels.md).

## <a name="published-by"></a>Pubblicato da

[SelectionTree](selectiontree-control.md)

## <a name="argument"></a>Argomento

Nessuna.

## <a name="action-on-subscribers"></a>Azione sui sottoscrittori

Nessuna.

## <a name="typical-use"></a>Utilizzo tipico

Un controllo di [testo](text-control.md) nella stessa finestra di dialogo modale del SelectionTree sottoscrive questo ControlEvent tramite la [tabella EventMapping](eventmapping-table.md). Il controllo testo usa questo evento per visualizzare la descrizione dell'elemento evidenziato.

 

 



