---
description: L'evento ValidateProductID imposta la proprietà ProductID sull'ID prodotto completo. Se la convalida non riesce, questo evento inserisce un messaggio di errore e una finestra di dialogo modale per una voce utente dell'ID prodotto.
ms.assetid: 44002cae-154a-4938-a15c-456c293e94fb
title: ValidateProductID ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68ae9ae5747deb9995c2e33a5c44541793442be8844b224c28c8a91e412cb188
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119786661"
---
# <a name="validateproductid-controlevent"></a>ValidateProductID ControlEvent

L'evento ValidateProductID imposta la [**proprietà ProductID**](productid.md) sull'ID prodotto completo. Se la convalida non riesce, questo evento inserisce un messaggio di errore e una finestra di dialogo modale per una voce utente dell'ID prodotto.

Questo evento può essere pubblicato da un [controllo PushButton o](pushbutton-control.md) [selectionTree](selectiontree-control.md). Questo evento deve essere creato nella [tabella ControlEvent](controlevent-table.md).

Questo ControlEvent richiede che l'interfaccia utente sia eseguita a livello [*completo dell'interfaccia*](f-gly.md) utente. Questo evento non funzionerà con un'interfaccia [*utente ridotta*](r-gly.md) o un'interfaccia utente [*di base.*](b-gly.md) Per informazioni, vedere Livelli [Interfaccia utente.](user-interface-levels.md)

## <a name="published-by"></a>Pubblicato da

Questo ControlEvent viene pubblicato dal programma di installazione.

## <a name="argument"></a>Argomento

Nessuno.

## <a name="action-on-subscribers"></a>Azione nei Sottoscrittori

Nessuno.

## <a name="typical-use"></a>Utilizzo tipico

Un [controllo PushButton](pushbutton-control.md) in una finestra di dialogo modale è associato a questo evento e viene usato per controllare la voce dell'ID prodotto dell'utente. Se la voce dell'utente è valida, verrà aperta la finestra di dialogo successiva.

 

 



