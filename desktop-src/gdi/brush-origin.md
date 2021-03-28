---
description: Quando un'applicazione chiama una funzione di disegno per disegnare una forma, il sistema posiziona un pennello all'inizio dell'operazione di disegno ed esegue il mapping di un pixel nella bitmap del pennello all'area client all'origine della finestra, che rappresenta l'angolo superiore sinistro della finestra.
ms.assetid: b951fd9a-1e87-4b17-9be8-263896c73922
title: Origine pennello
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 016237b97a52da6fd7fa14a3b6ba2dc25b03b96e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104553165"
---
# <a name="brush-origin"></a><span data-ttu-id="c05bc-103">Origine pennello</span><span class="sxs-lookup"><span data-stu-id="c05bc-103">Brush Origin</span></span>

<span data-ttu-id="c05bc-104">Quando un'applicazione chiama una funzione di disegno per disegnare una forma, il sistema posiziona un pennello all'inizio dell'operazione di disegno ed esegue il mapping di un pixel nella bitmap del pennello all'area client all' *origine della finestra*, che rappresenta l'angolo superiore sinistro della finestra.</span><span class="sxs-lookup"><span data-stu-id="c05bc-104">When an application calls a drawing function to paint a shape, the system positions a brush at the start of the paint operation and maps a pixel in the brush bitmap to the client area at the *window origin*, which is the upper-left corner of the window.</span></span> <span data-ttu-id="c05bc-105">Le coordinate del pixel mappato dal sistema sono denominate *origine pennello*.</span><span class="sxs-lookup"><span data-stu-id="c05bc-105">The coordinates of the pixel that the system maps are called the *brush origin*.</span></span> <span data-ttu-id="c05bc-106">L'origine del pennello predefinita si trova nell'angolo superiore sinistro della bitmap del pennello, in corrispondenza delle coordinate (0, 0).</span><span class="sxs-lookup"><span data-stu-id="c05bc-106">The default brush origin is located in the upper-left corner of the brush bitmap, at the coordinates (0,0).</span></span> <span data-ttu-id="c05bc-107">Il sistema copia quindi il pennello sull'area client, formando un modello con altezza pari alla bitmap.</span><span class="sxs-lookup"><span data-stu-id="c05bc-107">The system then copies the brush across the client area, forming a pattern that is as tall as the bitmap.</span></span> <span data-ttu-id="c05bc-108">L'operazione di copia continua, riga per riga, fino a quando non viene riempita l'intera area client.</span><span class="sxs-lookup"><span data-stu-id="c05bc-108">The copy operation continues, row by row, until the entire client area is filled.</span></span> <span data-ttu-id="c05bc-109">Tuttavia, il modello di pennello è visibile solo entro i limiti della forma specificata.</span><span class="sxs-lookup"><span data-stu-id="c05bc-109">However, the brush pattern is visible only within the boundaries of the specified shape.</span></span>

<span data-ttu-id="c05bc-110">Sono presenti istanze in cui l'origine del pennello predefinita non deve essere utilizzata.</span><span class="sxs-lookup"><span data-stu-id="c05bc-110">There are instances when the default brush origin should not be used.</span></span> <span data-ttu-id="c05bc-111">Ad esempio, potrebbe essere necessario che un'applicazione utilizzi lo stesso pennello per disegnare gli sfondi delle finestre padre e figlio e fondere lo sfondo di una finestra figlio con quella della finestra padre.</span><span class="sxs-lookup"><span data-stu-id="c05bc-111">For example, it may be necessary for an application to use the same brush to paint the backgrounds of its parent and child windows and blend a child window's background with that of the parent window.</span></span> <span data-ttu-id="c05bc-112">A tale scopo, l'applicazione deve reimpostare l'origine del pennello chiamando la funzione [**SetBrushOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-setbrushorgex) e spostando l'origine sul numero di pixel richiesto.</span><span class="sxs-lookup"><span data-stu-id="c05bc-112">To do this, the application should reset the brush origin by calling the [**SetBrushOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-setbrushorgex) function and shifting the origin the required number of pixels.</span></span> <span data-ttu-id="c05bc-113">Un'applicazione può recuperare l'origine del pennello corrente chiamando la funzione [**GetBrushOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-getbrushorgex) .</span><span class="sxs-lookup"><span data-stu-id="c05bc-113">(An application can retrieve the current brush origin by calling the [**GetBrushOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-getbrushorgex) function.)</span></span>

<span data-ttu-id="c05bc-114">Nella figura seguente viene illustrata una stella a cinque punte riempita utilizzando un pennello definito dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c05bc-114">The following illustration shows a five-pointed star filled by using an application-defined brush.</span></span> <span data-ttu-id="c05bc-115">Nell'illustrazione viene mostrata un'immagine con zoom del pennello, nonché la posizione in cui è stato eseguito il mapping all'inizio dell'operazione di disegno.</span><span class="sxs-lookup"><span data-stu-id="c05bc-115">The illustration shows a zoomed image of the brush, as well as the location to which it was mapped at the beginning of the paint operation.</span></span>

![illustrazione che mostra che l'origine del pennello è mappata all'origine della finestra](images/csbru-01.png)

 

 



