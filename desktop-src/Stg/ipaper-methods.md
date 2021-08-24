---
title: Metodi IPaper
description: Fornisce oggetti COPaper controllati principalmente dalla relativa interfaccia IPaper nativa.
ms.assetid: 3b77a6b3-8ec3-4a91-82cd-1f08d10fbf73
keywords:
- IPaper
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91a45322e35f07a6f136e76ecaad6ae237891a741dfb44a6b5db0702c87bda33
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119662721"
---
# <a name="ipaper-methods"></a>Metodi IPaper

**StoServe fornisce** oggetti COPaper controllati principalmente dalla relativa **interfaccia IPaper** nativa.

La tabella seguente elenca i **metodi IPaper** di IPAPER. H nella directory inc di \\ pari livello.



| Metodo    | Descrizione                                                         |
|-----------|---------------------------------------------------------------------|
| InitPaper | Inizializza l'oggetto paper e crea una matrice di dati dell'input penna.                 |
| Lock      | Fornisce al client il controllo della carta e blocca altri client.      |
| Sblocca    | Consente di rinunciare al controllo client della carta.                           |
| Caricamento      | Carica il contenuto cartaceo dal file composto del client e invia una notifica ai sink. |
| Salva      | Salva il contenuto cartaceo nel file composto del client.                      |
| InkStart  | Avvia il disegno dell'input penna a colori sulla superficie della carta.                      |
| InkDraw   | Posiziona i punti dati dell'input penna sulla superficie della carta elettronica.               |
| InkStop   | Arresta il disegno a penna sulla superficie della carta.                             |
| Cancellazione     | Cancella il contenuto della carta corrente e invia una notifica ai sink.                 |
| Ridimensionamento    | Ridimensiona le dimensioni del rettangolo della carta da disegno e invia una notifica ai sink.        |
| Ridisegnare    | Ridisegna il contenuto dell'oggetto paper e invia una notifica ai sink.                |



 

I metodi di interesse per questo esempio di codice nei file composti sono [**Load,**](ipaper--load.md) [**Save**](ipaper--save.md)e [**Redraw.**](ipaper--redraw.md)

[**InkStart,**](inkstart-method.md) [**InkDraw**](inkdraw-method.md)e [**InkStop**](cguipaper-methods.md) sono metodi usati dai client per eseguire il comando COPaper per registrare le sequenze di disegno a penna. Il client risponde in genere a un messaggio LBUTTONDOWN WM come inizio di una sequenza di disegno tramite input penna chiamando \_ **InkStart** in COPaper. Quando l'utente sposta il mouse o la penna per disegnare tenendo premuto il pulsante sinistro, il client risponderà ai messaggi WM MOUSEMOVE ripetuti con chiamate corrispondenti \_ **a InkDraw.** Quando l'utente rilascia il pulsante sinistro del mouse, il client risponderà a un messaggio WM LBUTTONUP con una chiamata \_ a **InkStop,** che contrassegna la fine della sequenza di disegno a penna.

[**InkStart**](inkstart-method.md) indica a COPaper la posizione iniziale per la sequenza di disegno nelle coordinate della finestra client. Passa anche il colore e la larghezza dell'input penna attualmente selezionati. Il client gestisce queste selezioni. COPaper li registra semplicemente quando viene **effettuata la chiamata InkStart.** [**InkDraw viene**](inkdraw-method.md) chiamato ripetutamente per indicare a COPaper la successione delle coordinate della finestra che rappresentano il movimento di disegno del mouse o della penna. [**InkStop**](cguipaper-methods.md) indica a COPaper di contrassegnare la fine di una sequenza di disegno.

 

 




