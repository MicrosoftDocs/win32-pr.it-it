---
description: Sebbene le applicazioni effettuino la maggior parte delle operazioni di disegno durante l'elaborazione del messaggio di disegno WM \_ , a volte è più efficiente che un'applicazione venga disegnata direttamente in una finestra senza basarsi sul messaggio di disegno WM \_ .
ms.assetid: 2d015879-58d2-4cbe-b1cc-445f2e8fd316
title: Disegno senza messaggio di WM_PAINT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66695e85b700de6f62366dedb6fe082f410d4385
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880290"
---
# <a name="drawing-without-the-wm_paint-message"></a>Disegno senza il messaggio di disegno WM \_

Sebbene le applicazioni effettuino la maggior parte delle operazioni di disegno durante l'elaborazione del messaggio di disegno [**WM \_**](wm-paint.md) , a volte è più efficiente che un'applicazione venga disegnata direttamente in una finestra senza basarsi sul messaggio di disegno **WM \_** . Questa operazione può essere utile quando l'utente necessita di un feedback immediato, ad esempio quando si seleziona il testo e si trascina o ridimensiona un oggetto. In questi casi, l'applicazione in genere disegna durante l'elaborazione dei messaggi della tastiera o del mouse.

Per disegnare in una finestra senza usare un messaggio di [**\_ disegno WM**](wm-paint.md) , l'applicazione usa la funzione [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) o [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex) per recuperare un contesto di dispositivo di visualizzazione per la finestra. Con il contesto del dispositivo di visualizzazione, l'applicazione è in grado di creare la finestra ed evitare intrusioni in altre finestre. Al termine del disegno, l'applicazione chiama la funzione [**ReleaseDC**](/windows/desktop/api/Winuser/nf-winuser-releasedc) per rilasciare il contesto del dispositivo di visualizzazione per l'uso da parte di altre applicazioni.

Quando si disegna senza usare un messaggio di disegno [**WM \_**](wm-paint.md) , l'applicazione in genere non invalida la finestra. Viene invece disegnato in modo tale da poter ripristinare facilmente la finestra e rimuovere il disegno. Ad esempio, quando l'utente seleziona un testo o un oggetto, l'applicazione in genere disegna la selezione invertendo tutto ciò che è già presente nella finestra. L'applicazione può rimuovere la selezione e ripristinare il contenuto originale della finestra semplicemente invertendo di nuovo.

L'applicazione ha la responsabilità di gestire con attenzione le modifiche apportate alla finestra. In particolare, se un'applicazione disegna una selezione e viene visualizzato un [**messaggio \_ di disegno WM**](wm-paint.md) corrispondente, l'applicazione deve garantire che il disegno eseguito durante il messaggio non danneggi la selezione. Per evitare questo problema, molte applicazioni rimuovono la selezione, eseguono le normali operazioni di disegno e quindi ripristinano la selezione al termine del disegno.

 

 



