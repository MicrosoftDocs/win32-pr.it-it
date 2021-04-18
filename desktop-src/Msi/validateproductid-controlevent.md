---
description: L'evento ValidateProductID imposta la proprietà ProductID sull'ID prodotto completo. Se la convalida ha esito negativo, questo evento inserisce un messaggio di errore e una finestra di dialogo modale per una voce utente dell'ID prodotto.
ms.assetid: 44002cae-154a-4938-a15c-456c293e94fb
title: ControlEvent ValidateProductID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b86cacfc4561fe9e4d94436724b42a78d3d8792
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308172"
---
# <a name="validateproductid-controlevent"></a>ControlEvent ValidateProductID

L'evento ValidateProductID imposta la proprietà [**ProductID**](productid.md) sull'ID prodotto completo. Se la convalida ha esito negativo, questo evento inserisce un messaggio di errore e una finestra di dialogo modale per una voce utente dell'ID prodotto.

Questo evento può essere pubblicato da un [controllo pulsante](pushbutton-control.md)o da un [controllo SelectionTree](selectiontree-control.md). Questo evento deve essere creato nella [tabella ControlEvent](controlevent-table.md).

Questo ControlEvent richiede l'esecuzione dell'interfaccia utente a livello di [*interfaccia utente completo*](f-gly.md) . Questo evento non funzionerà con un'interfaccia utente [*ridotta*](r-gly.md) o un' [*interfaccia utente di base*](b-gly.md). Per informazioni, vedere [livelli di interfaccia utente](user-interface-levels.md).

## <a name="published-by"></a>Pubblicato da

Questo ControlEvent viene pubblicato dal programma di installazione.

## <a name="argument"></a>Argomento

Nessuna.

## <a name="action-on-subscribers"></a>Azione sui sottoscrittori

Nessuna.

## <a name="typical-use"></a>Utilizzo tipico

Un controllo [pulsante](pushbutton-control.md) in una finestra di dialogo modale è associato a questo evento e viene usato per controllare la voce dell'utente dell'ID prodotto. Se la voce dell'utente è valida, verrà visualizzata la finestra di dialogo successiva.

 

 



