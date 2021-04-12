---
title: Metodi IPaper
description: Fornisce oggetti della cocarta controllati principalmente dall'interfaccia IPaper nativa.
ms.assetid: 3b77a6b3-8ec3-4a91-82cd-1f08d10fbf73
keywords:
- IPaper
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f84153c9fcec021d9084807d73d46198e3a56482
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221972"
---
# <a name="ipaper-methods"></a>Metodi IPaper

**StoServe** fornisce oggetti della cocarta controllati principalmente dall'interfaccia **iPaper** nativa.

La tabella seguente elenca i metodi **iPaper** da iPaper. H nella directory di pari livello \\ Inc.



| Metodo    | Descrizione                                                         |
|-----------|---------------------------------------------------------------------|
| InitPaper | Inizializza l'oggetto paper e crea una matrice di dati Ink.                 |
| Lock      | Fornisce il controllo client del documento e blocca altri client.      |
| Sblocca    | Cede il controllo client del documento.                           |
| Caricamento      | Carica il contenuto della carta dal file composto del client e invia notifiche ai sink. |
| Salva      | Salva il contenuto della carta nel file composto del client.                      |
| InkStart  | Avvia il disegno dell'input penna sulla superficie della carta.                      |
| InkDraw   | Inserisce i punti dati dell'input penna sull'area della carta elettronica.               |
| InkStop   | Arresta il disegno dell'input penna sull'area della carta.                             |
| Cancellazione     | Cancellare il contenuto della carta corrente e notificare i sink.                 |
| Ridimensionamento    | Ridimensiona le dimensioni del rettangolo della carta di disegno e invia notifiche ai sink.        |
| Nuovo disegno    | Ritrae il contenuto dell'oggetto carta e notifica i sink.                |



 

I metodi di interesse per questo esempio di codice sui file composti sono [**Load**](ipaper--load.md), [**Save**](ipaper--save.md)e reload [**.**](ipaper--redraw.md)

[**InkStart**](inkstart-method.md), [**InkDraw**](inkdraw-method.md)e [**InkStop**](cguipaper-methods.md) sono metodi usati dai client per eseguire il comando di un foglio di lavoro per registrare le sequenze di disegno input penna. Il client risponde in genere a un \_ messaggio WM LBUTTONDOWN come inizio di una sequenza di disegno dell'input penna chiamando **InkStart** su un documento. Quando l'utente sposta il mouse o la penna da creare tenendo premuto il pulsante sinistro, il client risponderà ai messaggi di WM MOUSEMOVE ripetuti \_ con le chiamate corrispondenti a **InkDraw**. Quando l'utente rilascia il pulsante sinistro del mouse, il client risponderà a un \_ messaggio WM LBUTTONUP con una chiamata a **InkStop**, che contrassegna la fine della sequenza di disegno dell'input penna.

[**InkStart**](inkstart-method.md) indica al documento la posizione iniziale per la sequenza di disegno nelle coordinate della finestra client. Passa anche il colore e la larghezza dell'inchiostro attualmente selezionato. Il client gestisce queste selezioni; Il formato del documento viene semplicemente registrato quando viene effettuata la chiamata **InkStart** . [**InkDraw**](inkdraw-method.md) viene chiamato ripetutamente per indicare al documento la successione delle coordinate della finestra che rappresentano il movimento del disegno del mouse o della penna. [**InkStop**](cguipaper-methods.md) indica a Copaper di contrassegnare la fine di una sequenza di disegno.

 

 




