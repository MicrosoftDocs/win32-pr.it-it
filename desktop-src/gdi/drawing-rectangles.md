---
description: Un rettangolo è un poligono a quattro lati i cui lati opposti sono paralleli e di lunghezza uguale.
ms.assetid: 77d29981-032e-45ba-a06b-c9c992236803
title: Disegno di rettangoli
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec1c5908ff989f7534536b3a6e84bad2095c096e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880294"
---
# <a name="drawing-rectangles"></a><span data-ttu-id="aa529-103">Disegno di rettangoli</span><span class="sxs-lookup"><span data-stu-id="aa529-103">Drawing Rectangles</span></span>

<span data-ttu-id="aa529-104">Un rettangolo è un poligono a quattro lati i cui lati opposti sono paralleli e di lunghezza uguale.</span><span class="sxs-lookup"><span data-stu-id="aa529-104">A rectangle is a four-sided polygon whose opposing sides are parallel and equal in length.</span></span> <span data-ttu-id="aa529-105">Sebbene un'applicazione possa creare un rettangolo chiamando la funzione [**Polygon**](/windows/desktop/api/Wingdi/nf-wingdi-polygon) , fornendo le coordinate di ogni angolo, la funzione [**Rectangle**](/windows/desktop/api/Wingdi/nf-wingdi-rectangle) fornisce un metodo più semplice.</span><span class="sxs-lookup"><span data-stu-id="aa529-105">Although an application can draw a rectangle by calling the [**Polygon**](/windows/desktop/api/Wingdi/nf-wingdi-polygon) function, supplying the coordinates of each corner, the [**Rectangle**](/windows/desktop/api/Wingdi/nf-wingdi-rectangle) function provides a simpler method.</span></span> <span data-ttu-id="aa529-106">Questa funzione richiede solo le coordinate per gli angoli superiore sinistro e inferiore destro.</span><span class="sxs-lookup"><span data-stu-id="aa529-106">This function requires only the coordinates for the upper-left and the lower-right corners.</span></span> <span data-ttu-id="aa529-107">Quando un'applicazione chiama la funzione [**Rectangle**](/windows/win32/api/wingdi/nf-wingdi-rectangle) , il sistema disegna il rettangolo, esclusi i lati destro e inferiore se non è impostata alcuna trasformazione globale per il contesto di dispositivo specificato.</span><span class="sxs-lookup"><span data-stu-id="aa529-107">When an application calls the [**Rectangle**](/windows/win32/api/wingdi/nf-wingdi-rectangle) function, the system draws the rectangle, excluding the right and lower sides if no world transformation is set for the given device context.</span></span>

<span data-ttu-id="aa529-108">Se è stata impostata una trasformazione globale tramite la funzione [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) o [**ModifyWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-modifyworldtransform) , il sistema include i bordi destro e inferiore.</span><span class="sxs-lookup"><span data-stu-id="aa529-108">If a world transformation has been set by using the [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) or [**ModifyWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-modifyworldtransform) function, the system includes the right and lower edges.</span></span>

<span data-ttu-id="aa529-109">Oltre a disegnare un rettangolo tradizionale, è possibile disegnare rettangoli con angoli arrotondati.</span><span class="sxs-lookup"><span data-stu-id="aa529-109">In addition to drawing a traditional rectangle, you can draw rectangles with rounded corners.</span></span> <span data-ttu-id="aa529-110">Per la funzione [**RoundRect**](/windows/desktop/api/Wingdi/nf-wingdi-roundrect) è necessario che l'applicazione fornisca le coordinate degli angoli inferiore sinistro e superiore destro, nonché la larghezza e l'altezza dell'ellisse utilizzata per arrotondare ogni angolo.</span><span class="sxs-lookup"><span data-stu-id="aa529-110">The [**RoundRect**](/windows/desktop/api/Wingdi/nf-wingdi-roundrect) function requires that the application supply the coordinates of the lower-left and upper-right corners, as well as the width and height of the ellipse used to round each corner.</span></span>

<span data-ttu-id="aa529-111">Per modificare i rettangoli, le applicazioni possono utilizzare le funzioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="aa529-111">Applications can use the following functions to manipulate rectangles.</span></span>



| <span data-ttu-id="aa529-112">Funzione</span><span class="sxs-lookup"><span data-stu-id="aa529-112">Function</span></span>                         | <span data-ttu-id="aa529-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="aa529-113">Description</span></span>                                                        |
|----------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="aa529-114">**FillRect**</span><span class="sxs-lookup"><span data-stu-id="aa529-114">**FillRect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-fillrect)     | <span data-ttu-id="aa529-115">Ridisegna l'interno di un rettangolo.</span><span class="sxs-lookup"><span data-stu-id="aa529-115">Repaints the interior of a rectangle.</span></span>                              |
| [<span data-ttu-id="aa529-116">**FrameRect**</span><span class="sxs-lookup"><span data-stu-id="aa529-116">**FrameRect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-framerect)   | <span data-ttu-id="aa529-117">Ridisegnato i lati di un rettangolo.</span><span class="sxs-lookup"><span data-stu-id="aa529-117">Redraws the sides of a rectangle.</span></span>                                  |
| [<span data-ttu-id="aa529-118">**InvertRect**</span><span class="sxs-lookup"><span data-stu-id="aa529-118">**InvertRect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-invertrect) | <span data-ttu-id="aa529-119">Inverte i colori visualizzati all'interno di un rettangolo.</span><span class="sxs-lookup"><span data-stu-id="aa529-119">Inverts the colors that appear within the interior of a rectangle.</span></span> |



 

 

 
