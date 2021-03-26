---
description: Usare la funzione GetDC per eseguire il disegno che deve verificarsi immediatamente anziché quando un messaggio di disegno WM \_ viene elaborato.
ms.assetid: 75525e26-72f5-4a58-a663-0bbdc2034759
title: Uso della funzione GetDC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98c018228eccbce7b487444341481165e24214b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979375"
---
# <a name="using-the-getdc-function"></a>Uso della funzione GetDC

Usare la funzione [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) per eseguire il disegno che deve verificarsi immediatamente anziché quando un messaggio di [**disegno \_ WM**](wm-paint.md) viene elaborato. Tale disegno è in genere in risposta a un'azione da parte dell'utente, ad esempio l'esecuzione di una selezione o di un disegno con il mouse. In questi casi, l'utente deve ricevere feedback istantaneo e non deve essere forzato a interrompere la selezione o il disegno per consentire all'applicazione di visualizzare il risultato. Le sezioni seguenti illustrano come usare GetDC per creare una finestra:

-   [Disegno con il mouse](drawing-with-the-mouse.md)
-   [Disegno a intervalli temporizzati](drawing-at-timed-intervals.md)

 

 



