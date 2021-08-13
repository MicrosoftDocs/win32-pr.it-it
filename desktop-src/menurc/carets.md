---
title: Caret
description: In questa sezione vengono illustrati i cursori che lampeggiano su righe, blocchi o bitmap nell'area client di una finestra.
ms.assetid: vs|winui|~\winui\windowsuserinterface\resources\carets.htm
keywords:
- risorse, caret
- carets,about
- linee lampeggianti
- blocchi lampeggianti
- bitmap lampeggianti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ed77a9d7fe315f5cef1be501c6392cce5fcfc3e79c5994f197a9fe6e254d8f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118734857"
---
# <a name="carets"></a>Caret

Un *cursore* è una riga lampeggiante, un blocco o una bitmap nell'area client di una finestra. Il punto di inserimento indica in genere la posizione in cui verrà inserito testo o grafica.

La figura seguente illustra alcune variazioni comuni nell'aspetto del caret.

![Mostra 5 modi diversi per visualizzare un punto di controllo.](images/cscrt-01.png)

Le applicazioni possono creare un cursore, modificarne l'ora di lampeggiamento e visualizzare, nascondere o spostare il cursore.

### <a name="in-this-section"></a>Contenuto della sezione



| Nome                                   | Descrizione                                                               |
|----------------------------------------|---------------------------------------------------------------------------|
| [Informazioni sui caret](about-carets.md)       | Vengono illustrati i caret.<br/>                                              |
| [Uso dei caret](using-carets.md)       | Esempi di codice che illustrano come eseguire attività correlate ai caret.<br/> |
| [Informazioni di riferimento sul punto di riferimento](caret-reference.md) | Contiene il riferimento all'API.<br/>                                    |



 

### <a name="caret-functions"></a>Funzioni di caret



| Nome                                           | Descrizione                                                                                                                                                                                                                                                   |
|------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateCaret**](/windows/desktop/api/Winuser/nf-winuser-createcaret)             | Crea una nuova forma per il punto di controllo di sistema e assegna la proprietà del punto di accesso alla finestra specificata. La forma del punto di caret può essere una linea, un blocco o una bitmap. <br/>                                                                                         |
| [**DestroyCaret**](/windows/desktop/api/Winuser/nf-winuser-destroycaret)           | Elimina la forma corrente del punto di selezione, libera il punto di selezione dalla finestra e lo rimuove dallo schermo. <br/>                                                                                                                                       |
| [**GetCaretBlinkTime**](/windows/desktop/api/Winuser/nf-winuser-getcaretblinktime) | Recupera il tempo necessario per invertire i pixel del caret. L'utente può impostare questo valore. <br/>                                                                                                                                                            |
| [**GetCaretPos**](/windows/desktop/api/Winuser/nf-winuser-getcaretpos)             | Copia la posizione del cursore nella struttura [**POINT**](/previous-versions//dd162805(v=vs.85)) specificata. <br/>                                                                                                                                                                    |
| [**HideCaret**](/windows/desktop/api/Winuser/nf-winuser-hidecaret)                 | Rimuove il caret dalla schermata. Nascondere un cursore non elimina la forma corrente o invalida il punto di inserimento. <br/>                                                                                                                           |
| [**SetCaretBlinkTime**](/windows/desktop/api/Winuser/nf-winuser-setcaretblinktime) | Imposta l'ora di lampeggiamento del cursore sul numero di millisecondi specificato. Il tempo di lampeggiamento è il tempo trascorso, in millisecondi, necessario per invertire i pixel del cursore. <br/>                                                                                    |
| [**SetCaretPos**](/windows/desktop/api/Winuser/nf-winuser-setcaretpos)             | Sposta il cursore nelle coordinate specificate. Se la finestra proprietaria del punto di selezione è stata creata con lo stile di classe **CS \_ OWNDC,** le coordinate specificate sono soggette alla modalità di mapping del contesto di dispositivo associato a tale finestra. <br/> |
| [**ShowCaret**](/windows/desktop/api/Winuser/nf-winuser-showcaret)                 | Rende visibile il cursore sullo schermo nella posizione corrente del cursore. Quando il punto di accesso diventa visibile, inizia a lampeggiare automaticamente. <br/>                                                                                                          |



 

 

