---
description: La funzione serect crea un rettangolo, la funzione CopyRect esegue una copia di un rettangolo specificato e la funzione SetRectEmpty crea un rettangolo vuoto.
ms.assetid: 982d6283-673b-41a1-abc7-10ef87ff3c6f
title: Operazioni Rectangle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3117fda697000e92258c99cf90af470e8815e237
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344641"
---
# <a name="rectangle-operations"></a><span data-ttu-id="14739-103">Operazioni Rectangle</span><span class="sxs-lookup"><span data-stu-id="14739-103">Rectangle Operations</span></span>

<span data-ttu-id="14739-104">La funzione [**serect**](/windows/desktop/api/Winuser/nf-winuser-setrect) crea un rettangolo, la funzione [**CopyRect**](/windows/desktop/api/Winuser/nf-winuser-copyrect) esegue una copia di un rettangolo specificato e la funzione [**SetRectEmpty**](/windows/desktop/api/Winuser/nf-winuser-setrectempty) crea un rettangolo vuoto.</span><span class="sxs-lookup"><span data-stu-id="14739-104">The [**SetRect**](/windows/desktop/api/Winuser/nf-winuser-setrect) function creates a rectangle, the [**CopyRect**](/windows/desktop/api/Winuser/nf-winuser-copyrect) function makes a copy of a given rectangle, and the [**SetRectEmpty**](/windows/desktop/api/Winuser/nf-winuser-setrectempty) function creates an empty rectangle.</span></span> <span data-ttu-id="14739-105">Un rettangolo vuoto è qualsiasi rettangolo con larghezza zero, altezza zero o entrambi.</span><span class="sxs-lookup"><span data-stu-id="14739-105">An empty rectangle is any rectangle that has zero width, zero height, or both.</span></span> <span data-ttu-id="14739-106">La funzione [**IsRectEmpty**](/windows/desktop/api/Winuser/nf-winuser-isrectempty) determina se un rettangolo specificato è vuoto.</span><span class="sxs-lookup"><span data-stu-id="14739-106">The [**IsRectEmpty**](/windows/desktop/api/Winuser/nf-winuser-isrectempty) function determines whether a given rectangle is empty.</span></span> <span data-ttu-id="14739-107">La funzione [**EqualRect**](/windows/desktop/api/Winuser/nf-winuser-equalrect) determina se due rettangoli sono identici, ovvero se hanno le stesse coordinate.</span><span class="sxs-lookup"><span data-stu-id="14739-107">The [**EqualRect**](/windows/desktop/api/Winuser/nf-winuser-equalrect) function determines whether two rectangles are identical that is, whether they have the same coordinates.</span></span>

<span data-ttu-id="14739-108">La funzione [**InflateRect**](/windows/desktop/api/Winuser/nf-winuser-inflaterect) aumenta o diminuisce la larghezza o l'altezza di un rettangolo o di entrambi.</span><span class="sxs-lookup"><span data-stu-id="14739-108">The [**InflateRect**](/windows/desktop/api/Winuser/nf-winuser-inflaterect) function increases or decreases the width or height of a rectangle, or both.</span></span> <span data-ttu-id="14739-109">Consente di aggiungere o rimuovere larghezza da entrambe le estremità del rettangolo. è possibile aggiungere o rimuovere l'altezza sia dalla parte superiore che dalla parte inferiore del rettangolo.</span><span class="sxs-lookup"><span data-stu-id="14739-109">It can add or remove width from both ends of the rectangle; it can add or remove height from both the top and bottom of the rectangle.</span></span>

<span data-ttu-id="14739-110">La funzione [**OffsetRect**](/windows/desktop/api/Winuser/nf-winuser-offsetrect) sposta un rettangolo di una determinata quantità.</span><span class="sxs-lookup"><span data-stu-id="14739-110">The [**OffsetRect**](/windows/desktop/api/Winuser/nf-winuser-offsetrect) function moves a rectangle by a given amount.</span></span> <span data-ttu-id="14739-111">Sposta il rettangolo aggiungendo gli importi x-amount, y-amount o x-e y delle coordinate d'angolo.</span><span class="sxs-lookup"><span data-stu-id="14739-111">It moves the rectangle by adding the given x-amount, y-amount, or x- and y-amounts to the corner coordinates.</span></span>

<span data-ttu-id="14739-112">La funzione [**PtInRect**](/windows/desktop/api/Winuser/nf-winuser-ptinrect) determina se un punto specificato si trova all'interno di un rettangolo specificato.</span><span class="sxs-lookup"><span data-stu-id="14739-112">The [**PtInRect**](/windows/desktop/api/Winuser/nf-winuser-ptinrect) function determines whether a given point lies within a given rectangle.</span></span> <span data-ttu-id="14739-113">Il punto si trova nel rettangolo se si trova sul lato sinistro o superiore oppure è completamente all'interno del rettangolo.</span><span class="sxs-lookup"><span data-stu-id="14739-113">The point is in the rectangle if it lies on the left or top side or is completely within the rectangle.</span></span> <span data-ttu-id="14739-114">Il punto non si trova nel rettangolo se si trova sul lato destro o inferiore.</span><span class="sxs-lookup"><span data-stu-id="14739-114">The point is not in the rectangle if it lies on the right or bottom side.</span></span>

<span data-ttu-id="14739-115">La funzione [**IntersectRect**](/windows/desktop/api/Winuser/nf-winuser-intersectrect) crea un nuovo rettangolo che rappresenta l'intersezione di due rettangoli esistenti, come illustrato nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="14739-115">The [**IntersectRect**](/windows/desktop/api/Winuser/nf-winuser-intersectrect) function creates a new rectangle that is the intersection of two existing rectangles, as shown in the following figure.</span></span>

![<span data-ttu-id="14739-116">illustrazione che mostra due rettangoli sovrapposti, con ombreggiatura più scura per indicare l'intersezione</span><span class="sxs-lookup"><span data-stu-id="14739-116">illustration showing two overlapping rectangles, with darker shading to indicate the intersection</span></span> ](images/csrec-01.png)

<span data-ttu-id="14739-117">La funzione [**UnionRect**](/windows/desktop/api/Winuser/nf-winuser-unionrect) crea un nuovo rettangolo che rappresenta l'Unione di due rettangoli esistenti, come illustrato nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="14739-117">The [**UnionRect**](/windows/desktop/api/Winuser/nf-winuser-unionrect) function creates a new rectangle that is the union of two existing rectangles, as shown in the following figure.</span></span>

![illustrazione di due rettangoli sovrapposti, con ombreggiatura più scura che indica le aree all'interno dell'Unione, ma non all'interno di uno dei due rettangoli](images/csrec-02.png)

<span data-ttu-id="14739-119">Per informazioni sulle funzioni che delineano ellissi e poligoni, vedere [forme compilate](filled-shapes.md).</span><span class="sxs-lookup"><span data-stu-id="14739-119">For information about functions that draw ellipses and polygons, see [Filled Shapes](filled-shapes.md).</span></span>

 

 



