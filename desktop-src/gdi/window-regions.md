---
description: Oltre all'area di aggiornamento, ogni finestra dispone di un'area visibile che definisce la parte della finestra visibile all'utente.
ms.assetid: 9d8beba1-93c0-437d-a138-76880a40bc79
title: Aree della finestra
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02555339412c604f79f69294febbab524fc92a70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104057922"
---
# <a name="window-regions"></a>Aree della finestra

Oltre all'area di aggiornamento, ogni finestra dispone di un' *area visibile* che definisce la parte della finestra visibile all'utente. Il sistema modifica l'area visibile per la finestra ogni volta che la finestra viene modificata o quando un'altra finestra viene spostata in modo da nascondere o esporre una parte della finestra. Le applicazioni non possono modificare direttamente l'area visibile, ma il sistema usa automaticamente l'area visibile per creare l'area di ridimensionamento per qualsiasi contesto di periferica di visualizzazione recuperato per la finestra.

L' *area di visualizzazione* determina la posizione in cui il sistema consente il disegno. Quando l'applicazione recupera un contesto di dispositivo di visualizzazione usando la funzione [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint), [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc)o [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex) , il sistema imposta l'area di ridimensionamento per il contesto di dispositivo sull'intersezione tra l'area visibile e l'area di aggiornamento. Le applicazioni possono modificare l'area di visualizzazione utilizzando funzioni come [**SetWindowRgn**](/windows/desktop/api/Winuser/nf-winuser-setwindowrgn), [**SelectClipPath**](/windows/desktop/api/Wingdi/nf-wingdi-selectclippath) e [**SelectClipRgn**](/windows/desktop/api/Wingdi/nf-wingdi-selectcliprgn), per limitare ulteriormente il disegno a una parte specifica dell'area di aggiornamento.

Gli \_ stili WS CLIPCHILDREN e WS \_ CLIPSIBLINGS specificano ulteriormente il modo in cui il sistema calcola l'area visibile per una finestra. Se una finestra ha uno o entrambi gli stili, l'area visibile esclude qualsiasi finestra figlio o Windows di pari livello (Windows con la stessa finestra padre). Pertanto, il disegno che altrimenti sarebbe intruso in queste finestre verrà sempre ritagliato.

 

 



