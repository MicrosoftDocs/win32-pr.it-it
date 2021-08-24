---
description: Oltre all'area di aggiornamento, ogni finestra ha un'area visibile che definisce la parte della finestra visibile all'utente.
ms.assetid: 9d8beba1-93c0-437d-a138-76880a40bc79
title: Aree della finestra
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac3f751303d8a971d010ea7dabf7604c24db892f88d9a4029f0189d303cf5a80
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119727411"
---
# <a name="window-regions"></a>Aree della finestra

Oltre all'area di aggiornamento, ogni finestra ha *un'area visibile* che definisce la parte della finestra visibile all'utente. Il sistema modifica l'area visibile per la finestra ogni volta che le dimensioni della finestra cambiano o ogni volta che viene spostata un'altra finestra in modo da nascondere o esporre una parte della finestra. Le applicazioni non possono modificare direttamente l'area visibile, ma il sistema usa automaticamente l'area visibile per creare l'area di ritaglio per qualsiasi contesto di dispositivo di visualizzazione recuperato per la finestra.

*L'area di ritaglio* determina dove il sistema consente il disegno. Quando l'applicazione recupera un contesto di dispositivo di visualizzazione usando la funzione [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint), [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc)o [**GetDCEx,**](/windows/desktop/api/Winuser/nf-winuser-getdcex) il sistema imposta l'area di ritaglio per il contesto di dispositivo sull'intersezione tra l'area visibile e l'area di aggiornamento. Le applicazioni possono modificare l'area di ritaglio usando funzioni come [**SetWindowRgn**](/windows/desktop/api/Winuser/nf-winuser-setwindowrgn), [**SelectClipPath**](/windows/desktop/api/Wingdi/nf-wingdi-selectclippath) e [**SelectClipRgn**](/windows/desktop/api/Wingdi/nf-wingdi-selectcliprgn)per limitare ulteriormente il disegno a una determinata parte dell'area di aggiornamento.

Gli stili WS CLIPCHILDREN e WS CLIPSIBLINGS specificano ulteriormente il modo in cui il sistema calcola \_ \_ l'area visibile per una finestra. Se una finestra ha uno o entrambi questi stili, l'area visibile esclude qualsiasi finestra figlio o finestra di pari livello (finestre con la stessa finestra padre). Di conseguenza, il disegno che altrimenti verrebbe intruso in queste finestre verrà sempre ritagliato.

 

 



