---
description: La funzione ExcludeUpdateRgn esclude l'area di aggiornamento dall'area di visualizzazione del contesto del dispositivo di visualizzazione.
ms.assetid: e652122b-a3b7-4d1b-8afd-9648d5ee3d42
title: Esclusione dell'area di aggiornamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7be39b948e61fc06c7f7005d15c1163cef0068f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049726"
---
# <a name="excluding-the-update-region"></a><span data-ttu-id="4984e-103">Esclusione dell'area di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="4984e-103">Excluding the Update Region</span></span>

<span data-ttu-id="4984e-104">La funzione [**ExcludeUpdateRgn**](/windows/desktop/api/Winuser/nf-winuser-excludeupdatergn) esclude l'area di aggiornamento dall'area di visualizzazione del contesto del dispositivo di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="4984e-104">The [**ExcludeUpdateRgn**](/windows/desktop/api/Winuser/nf-winuser-excludeupdatergn) function excludes the update region from the clipping region for the display device context.</span></span> <span data-ttu-id="4984e-105">Questa funzione è utile quando si disegna in una finestra diversa da quando viene elaborato un messaggio di disegno WM \_ .</span><span class="sxs-lookup"><span data-stu-id="4984e-105">This function is useful when drawing in a window other than when a WM\_PAINT message is processing.</span></span> <span data-ttu-id="4984e-106">Impedisce il disegno nelle aree che verranno aggiornate durante il successivo messaggio di disegno WM \_ .</span><span class="sxs-lookup"><span data-stu-id="4984e-106">It prevents drawing in the areas that will be updated during the next WM\_PAINT message.</span></span>

 

 



