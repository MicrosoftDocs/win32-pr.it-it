---
description: Sebbene le applicazioni esercitino la maggior parte delle operazioni di disegno durante l'elaborazione del messaggio WM PAINT, talvolta è più efficiente per un'applicazione disegnare direttamente in una finestra senza basarsi sul \_ messaggio WM \_ PAINT.
ms.assetid: 2d015879-58d2-4cbe-b1cc-445f2e8fd316
title: Disegno senza il WM_PAINT messaggio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36ff9a18e923feceb33f961c9427852b2c2daddfcfc4e093809e24cd42f32869
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118250340"
---
# <a name="drawing-without-the-wm_paint-message"></a>Disegno senza il messaggio WM \_ PAINT

Sebbene le applicazioni esercitino la maggior parte delle operazioni di disegno durante l'elaborazione del messaggio [**WM \_ PAINT,**](wm-paint.md) talvolta è più efficiente per un'applicazione disegnare direttamente in una finestra senza basarsi sul **messaggio WM \_ PAINT.** Ciò può essere utile quando l'utente necessita di un feedback immediato, ad esempio quando si seleziona il testo e si trascina o si ridimensiona un oggetto. In questi casi, l'applicazione in genere disegna durante l'elaborazione dei messaggi della tastiera o del mouse.

Per disegnare in una finestra senza usare un messaggio [**WM \_ PAINT,**](wm-paint.md) l'applicazione usa la [**funzione GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) o [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex) per recuperare un contesto di dispositivo di visualizzazione per la finestra. Con il contesto di dispositivo di visualizzazione, l'applicazione può disegnare nella finestra ed evitare l'intrusione in altre finestre. Al termine del disegno, l'applicazione chiama la [**funzione ReleaseDC**](/windows/desktop/api/Winuser/nf-winuser-releasedc) per rilasciare il contesto di periferica di visualizzazione per l'uso da parte di altre applicazioni.

Quando si disegna senza usare [**un messaggio WM \_ PAINT,**](wm-paint.md) l'applicazione in genere non invalida la finestra. Al contrario, disegna in modo tale da poter ripristinare facilmente la finestra e rimuovere il disegno. Ad esempio, quando l'utente seleziona testo o un oggetto, l'applicazione in genere disegna la selezione invertendo qualsiasi elemento già presente nella finestra. L'applicazione può rimuovere la selezione e ripristinare il contenuto originale della finestra semplicemente invertendo nuovamente.

L'applicazione è responsabile della gestione attentamente delle modifiche apportate alla finestra. In particolare, se un'applicazione disegna una selezione e si verifica un messaggio [**WM \_ PAINT**](wm-paint.md) che interviene, l'applicazione deve assicurarsi che qualsiasi disegno eseguito durante il messaggio non danneggia la selezione. Per evitare questo problema, molte applicazioni rimuovono la selezione, e svolgono le normali operazioni di disegno e quindi ripristinano la selezione al termine del disegno.

 

 



