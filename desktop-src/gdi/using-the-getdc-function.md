---
description: È possibile usare la funzione GetDC per eseguire il disegno che deve essere eseguito immediatamente anziché quando è in corso l'elaborazione di un messaggio WM \_ PAINT.
ms.assetid: 75525e26-72f5-4a58-a663-0bbdc2034759
title: Utilizzo della funzione GetDC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 407f494cb551137b3d900f098ca7a836232eab08628c1a2d2fcd339588e9db0f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117885632"
---
# <a name="using-the-getdc-function"></a>Utilizzo della funzione GetDC

È possibile usare [**la funzione GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) per eseguire il disegno che deve essere eseguito immediatamente anziché quando è in corso l'elaborazione di un messaggio [**WM \_ PAINT.**](wm-paint.md) Tale disegno è in genere in risposta a un'azione dell'utente, ad esempio per effettuare una selezione o disegnare con il mouse. In questi casi, l'utente deve ricevere commenti e suggerimenti immediati e non deve essere obbligato a interrompere la selezione o il disegno per consentire all'applicazione di visualizzare il risultato. Le sezioni seguenti illustrano come usare GetDC per disegnare in una finestra:

-   [Disegno con il mouse](drawing-with-the-mouse.md)
-   [Disegno a intervalli temporati](drawing-at-timed-intervals.md)

 

 



