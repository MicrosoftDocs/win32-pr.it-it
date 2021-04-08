---
description: Il controllo SelectionTree usa l'evento SelectionPath per pubblicare il percorso per l'elemento evidenziato.
ms.assetid: 755e5bf2-42c4-4213-9bb7-4f15ad22041f
title: ControlEvent SelectionPath
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8314b12d14e10ccf96c7db9db32e63172050c0bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967677"
---
# <a name="selectionpath-controlevent"></a>ControlEvent SelectionPath

Il [controllo SelectionTree](selectiontree-control.md) usa l'evento SelectionPath per pubblicare il percorso per l'elemento evidenziato. Se l'elemento è selezionato per l'esecuzione dall'origine, questo è il percorso dell'origine. Se l'elemento è selezionato come assente, la stringa è la stringa **AbsentPath** dalla [tabella UIText](uitext-table.md). Questo evento deve essere creato nella [tabella EventMapping](eventmapping-table.md).

Questo ControlEvent richiede l'esecuzione dell'interfaccia utente a livello di [*interfaccia utente completo*](f-gly.md) . Questo evento non funzionerà con un'interfaccia utente [*ridotta*](r-gly.md) o un' [*interfaccia utente di base*](b-gly.md). Per informazioni, vedere [livelli di interfaccia utente](user-interface-levels.md).

Questo evento può influire solo sui controlli che si trovano nella stessa finestra di dialogo del controllo SelectionTree.

## <a name="published-by"></a>Pubblicato da

[SelectionTree](selectiontree-control.md)

## <a name="argument"></a>Argomento

Nessuna.

## <a name="action-on-subscribers"></a>Azione sui sottoscrittori

Nessuna.

## <a name="typical-use"></a>Utilizzo tipico

Un controllo di [testo](text-control.md) nella stessa finestra di dialogo modale del SelectionTree deve sottoscrivere l'evento tramite la [tabella EventMapping](eventmapping-table.md). Il controllo testo Visualizza il percorso dell'elemento evidenziato.

 

 



