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
# <a name="using-the-getdc-function"></a><span data-ttu-id="8ce53-103">Uso della funzione GetDC</span><span class="sxs-lookup"><span data-stu-id="8ce53-103">Using the GetDC Function</span></span>

<span data-ttu-id="8ce53-104">Usare la funzione [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) per eseguire il disegno che deve verificarsi immediatamente anziché quando un messaggio di [**disegno \_ WM**](wm-paint.md) viene elaborato.</span><span class="sxs-lookup"><span data-stu-id="8ce53-104">You use the [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) function to carry out drawing that must occur instantly rather than when a [**WM\_PAINT**](wm-paint.md) message is processing.</span></span> <span data-ttu-id="8ce53-105">Tale disegno è in genere in risposta a un'azione da parte dell'utente, ad esempio l'esecuzione di una selezione o di un disegno con il mouse.</span><span class="sxs-lookup"><span data-stu-id="8ce53-105">Such drawing is usually in response to an action by the user, such as making a selection or drawing with the mouse.</span></span> <span data-ttu-id="8ce53-106">In questi casi, l'utente deve ricevere feedback istantaneo e non deve essere forzato a interrompere la selezione o il disegno per consentire all'applicazione di visualizzare il risultato.</span><span class="sxs-lookup"><span data-stu-id="8ce53-106">In such cases, the user should receive instant feedback and must not be forced to stop selecting or drawing in order for the application to display the result.</span></span> <span data-ttu-id="8ce53-107">Le sezioni seguenti illustrano come usare GetDC per creare una finestra:</span><span class="sxs-lookup"><span data-stu-id="8ce53-107">The following sections show how to use GetDC to draw in a window:</span></span>

-   [<span data-ttu-id="8ce53-108">Disegno con il mouse</span><span class="sxs-lookup"><span data-stu-id="8ce53-108">Drawing with the Mouse</span></span>](drawing-with-the-mouse.md)
-   [<span data-ttu-id="8ce53-109">Disegno a intervalli temporizzati</span><span class="sxs-lookup"><span data-stu-id="8ce53-109">Drawing at Timed Intervals</span></span>](drawing-at-timed-intervals.md)

 

 



