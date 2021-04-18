---
description: Questo evento notifica al programma di installazione che deve verificare che il percorso selezionato sia valido. Se il percorso non è valido, questo evento blocca ulteriormente ControlEvents associati al controllo.
ms.assetid: b7c1de6e-5738-4ecb-a033-9379d79dddb9
title: ControlEvent CheckTargetPath
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49301dbe1fcc6becc1bc757a0fe487061e1dcdbd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310983"
---
# <a name="checktargetpath-controlevent"></a>ControlEvent CheckTargetPath

Questo evento notifica al programma di installazione che deve verificare che il percorso selezionato sia valido. Se il percorso non è valido, questo evento blocca ulteriormente ControlEvents associati al controllo.

Questo evento può essere pubblicato da un [controllo pulsante](pushbutton-control.md)o da un [controllo SelectionTree](selectiontree-control.md). Questo evento deve essere creato nella [tabella ControlEvent](controlevent-table.md).

Questo ControlEvent richiede l'esecuzione dell'interfaccia utente a livello di [*interfaccia utente completo*](f-gly.md) . Questo evento non funzionerà con un'interfaccia utente [*ridotta*](r-gly.md) o un' [*interfaccia utente di base*](b-gly.md). Per informazioni, vedere [livelli di interfaccia utente](user-interface-levels.md).

## <a name="published-by"></a>Pubblicato da

Questo ControlEvent viene pubblicato dal programma di installazione.

## <a name="argument"></a>Argomento

Nome della proprietà che contiene il percorso. Se la proprietà è indiretta, il nome della proprietà è racchiuso tra parentesi quadre.

## <a name="action-on-subscribers"></a>Azione sui sottoscrittori

Questo ControlEvent non esegue un'azione sui sottoscrittori.

## <a name="typical-use"></a>Utilizzo tipico

Un controllo [pulsante](pushbutton-control.md) in una finestra di dialogo Sfoglia è associato a questo evento nella tabella [ControlEvent](controlevent-table.md) per controllare il percorso selezionato prima di tornare alla finestra di dialogo di selezione.

 

 



