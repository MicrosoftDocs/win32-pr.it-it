---
description: Il rettangolo di delimitazione accumulato è il rettangolo più piccolo che racchiude la parte di una finestra o di un'area client interessata dalle operazioni di disegno recenti.
ms.assetid: 8ae13486-a9e2-4841-ada3-c70d30450ac8
title: Rettangolo di delimitazione accumulato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5ae3237304af68a4b8ff447b7ea2d64d3f81053
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528399"
---
# <a name="accumulated-bounding-rectangle"></a><span data-ttu-id="7f73a-103">Rettangolo di delimitazione accumulato</span><span class="sxs-lookup"><span data-stu-id="7f73a-103">Accumulated Bounding Rectangle</span></span>

<span data-ttu-id="7f73a-104">Il *rettangolo di delimitazione accumulato* è il rettangolo più piccolo che racchiude la parte di una finestra o di un'area client interessata dalle operazioni di disegno recenti.</span><span class="sxs-lookup"><span data-stu-id="7f73a-104">The *accumulated bounding rectangle* is the smallest rectangle enclosing the portion of a window or client area affected by recent drawing operations.</span></span> <span data-ttu-id="7f73a-105">Un'applicazione può utilizzare questo rettangolo per determinare agevolmente l'entità delle modifiche causate dalle operazioni di disegno.</span><span class="sxs-lookup"><span data-stu-id="7f73a-105">An application can use this rectangle to conveniently determine the extent of changes caused by drawing operations.</span></span> <span data-ttu-id="7f73a-106">Viene talvolta utilizzata insieme a [**LockWindowUpdate**](/windows/desktop/api/Winuser/nf-winuser-lockwindowupdate) per determinare quale parte dell'area client deve essere ridisegnato dopo che il blocco di aggiornamento è stato cancellato.</span><span class="sxs-lookup"><span data-stu-id="7f73a-106">It is sometimes used in conjunction with [**LockWindowUpdate**](/windows/desktop/api/Winuser/nf-winuser-lockwindowupdate) to determine which portion of the client area must be redrawn after the update lock is cleared.</span></span>

<span data-ttu-id="7f73a-107">Un'applicazione usa la funzione [**SetBoundsRect**](/windows/desktop/api/Wingdi/nf-wingdi-setboundsrect) (specificando DCB \_ Enable) per iniziare a accumulare il rettangolo di delimitazione.</span><span class="sxs-lookup"><span data-stu-id="7f73a-107">An application uses the [**SetBoundsRect**](/windows/desktop/api/Wingdi/nf-wingdi-setboundsrect) function (specifying DCB\_ENABLE) to begin accumulating the bounding rectangle.</span></span> <span data-ttu-id="7f73a-108">Il sistema accumula quindi punti per il rettangolo di delimitazione perché l'applicazione usa il contesto del dispositivo di visualizzazione specificato.</span><span class="sxs-lookup"><span data-stu-id="7f73a-108">The system subsequently accumulates points for the bounding rectangle as the application uses the specified display device context.</span></span> <span data-ttu-id="7f73a-109">L'applicazione può recuperare il rettangolo di delimitazione corrente in qualsiasi momento tramite la funzione [**GetBoundsRect**](/windows/desktop/api/Wingdi/nf-wingdi-getboundsrect) .</span><span class="sxs-lookup"><span data-stu-id="7f73a-109">The application can retrieve the current bounding rectangle at any time by using the [**GetBoundsRect**](/windows/desktop/api/Wingdi/nf-wingdi-getboundsrect) function.</span></span> <span data-ttu-id="7f73a-110">L'applicazione interrompe l'accumulo chiamando di nuovo **SetBoundsRect** , specificando il \_ valore di disabilitazione di DCB.</span><span class="sxs-lookup"><span data-stu-id="7f73a-110">The application stops the accumulation by calling **SetBoundsRect** again, specifying the DCB\_DISABLE value.</span></span>

 

 



