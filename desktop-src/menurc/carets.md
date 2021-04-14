---
title: CARETS
description: In questa sezione vengono illustrati i passaggi che lampeggiano a linee, blocchi o bitmap nell'area client di una finestra.
ms.assetid: vs|winui|~\winui\windowsuserinterface\resources\carets.htm
keywords:
- risorse, punto di inserimento
- occupazioni, informazioni
- righe lampeggianti
- blocchi lampeggianti
- bitmap intermittenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50cb99dfc324aa039924fa26683ab0a7674706ea
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/04/2021
ms.locfileid: "104401812"
---
# <a name="carets"></a>CARETS

Un *accento circonflesso* è una linea, un blocco o una bitmap lampeggiante nell'area client di una finestra. Il cursore indica in genere la posizione in cui verrà inserito il testo o la grafica.

Nella figura seguente vengono illustrate alcune variazioni comuni nell'aspetto del cursore.

![Mostra 5 diversi modi in cui può essere visualizzato un punto di inserimento.](images/cscrt-01.png)

Le applicazioni possono creare un accento circonflesso, modificare il tempo di lampeggio e visualizzare, nascondere o spostare il punto di inserimento.

### <a name="in-this-section"></a>Contenuto della sezione



| Nome                                   | Descrizione                                                               |
|----------------------------------------|---------------------------------------------------------------------------|
| [Informazioni sui Carrier](about-carets.md)       | Vengono illustrati i punto di inserimento.<br/>                                              |
| [Uso del punto di inserimento](using-carets.md)       | Esempi di codice che illustrano come eseguire attività correlate ai carrier.<br/> |
| [Riferimento al punto di inserimento](caret-reference.md) | Contiene il riferimento all'API.<br/>                                    |



 

### <a name="caret-functions"></a>Funzioni del cursore



| Nome                                           | Descrizione                                                                                                                                                                                                                                                   |
|------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateCaret**](/windows/desktop/api/Winuser/nf-winuser-createcaret)             | Crea una nuova forma per il punto di inserimento del sistema e assegna la proprietà del punto di inserimento alla finestra specificata. La forma del cursore può essere una linea, un blocco o una bitmap. <br/>                                                                                         |
| [**DestroyCaret**](/windows/desktop/api/Winuser/nf-winuser-destroycaret)           | Elimina la forma corrente del cursore, libera il punto di inserimento dalla finestra e rimuove il punto di inserimento dallo schermo. <br/>                                                                                                                                       |
| [**GetCaretBlinkTime**](/windows/desktop/api/Winuser/nf-winuser-getcaretblinktime) | Recupera il tempo necessario per invertire i pixel del punto di inserimento. L'utente può impostare questo valore. <br/>                                                                                                                                                            |
| [**GetCaretPos**](/windows/desktop/api/Winuser/nf-winuser-getcaretpos)             | Copia la posizione del punto di inserimento nella struttura del [**punto**](/previous-versions//dd162805(v=vs.85)) specificata. <br/>                                                                                                                                                                    |
| [**HideCaret**](/windows/desktop/api/Winuser/nf-winuser-hidecaret)                 | Rimuove il punto di inserimento dallo schermo. Nascondendo un cursore, non viene eliminata la forma corrente né viene invalidato il punto di inserimento. <br/>                                                                                                                           |
| [**SetCaretBlinkTime**](/windows/desktop/api/Winuser/nf-winuser-setcaretblinktime) | Imposta il tempo di lampeggio del punto di inserimento sul numero di millisecondi specificato. Il tempo di lampeggio è il tempo trascorso, in millisecondi, necessario per invertire i pixel del cursore. <br/>                                                                                    |
| [**SetCaretPos**](/windows/desktop/api/Winuser/nf-winuser-setcaretpos)             | Sposta il punto di inserimento alle coordinate specificate. Se la finestra proprietaria del punto di inserimento è stata creata con lo stile della classe **cs \_ OWNDC** , le coordinate specificate sono soggette alla modalità di mapping del contesto di dispositivo associato a tale finestra. <br/> |
| [**ShowCaret**](/windows/desktop/api/Winuser/nf-winuser-showcaret)                 | Rende visibile il cursore sullo schermo in corrispondenza della posizione corrente del punto di inserimento. Quando il punto di inserimento diventa visibile, inizia a lampeggiare automaticamente. <br/>                                                                                                          |



 

 

