---
description: Le funzioni seguenti vengono utilizzate con i rettangoli.
ms.assetid: b03da8c9-ee6d-4045-8d90-8beceb09ead5
title: Funzioni Rectangle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a5c72812363185217e5cf30ae88447f82edc42b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226670"
---
# <a name="rectangle-functions"></a><span data-ttu-id="e684d-103">Funzioni Rectangle</span><span class="sxs-lookup"><span data-stu-id="e684d-103">Rectangle Functions</span></span>

<span data-ttu-id="e684d-104">Le funzioni seguenti vengono utilizzate con i rettangoli.</span><span class="sxs-lookup"><span data-stu-id="e684d-104">The following functions are used with rectangles.</span></span>



| <span data-ttu-id="e684d-105">Funzione</span><span class="sxs-lookup"><span data-stu-id="e684d-105">Function</span></span>                               | <span data-ttu-id="e684d-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e684d-106">Description</span></span>                                                                                                                                   |
|----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e684d-107">**CopyRect**</span><span class="sxs-lookup"><span data-stu-id="e684d-107">**CopyRect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-copyrect)           | <span data-ttu-id="e684d-108">Copia le coordinate di un rettangolo in un altro.</span><span class="sxs-lookup"><span data-stu-id="e684d-108">Copies the coordinates of one rectangle to another.</span></span>                                                                                           |
| [<span data-ttu-id="e684d-109">**EqualRect**</span><span class="sxs-lookup"><span data-stu-id="e684d-109">**EqualRect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-equalrect)         | <span data-ttu-id="e684d-110">Determina se i due rettangoli specificati sono uguali confrontando le coordinate degli angoli superiore sinistro e inferiore destro.</span><span class="sxs-lookup"><span data-stu-id="e684d-110">Determines whether the two specified rectangles are equal by comparing the coordinates of their upper-left and lower-right corners.</span></span>           |
| [<span data-ttu-id="e684d-111">**InflateRect**</span><span class="sxs-lookup"><span data-stu-id="e684d-111">**InflateRect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-inflaterect)     | <span data-ttu-id="e684d-112">Aumenta o diminuisce la larghezza e l'altezza del rettangolo specificato.</span><span class="sxs-lookup"><span data-stu-id="e684d-112">Increases or decreases the width and height of the specified rectangle.</span></span>                                                                       |
| [<span data-ttu-id="e684d-113">**IntersectRect**</span><span class="sxs-lookup"><span data-stu-id="e684d-113">**IntersectRect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-intersectrect) | <span data-ttu-id="e684d-114">Calcola l'intersezione di due rettangoli di origine e inserisce le coordinate del rettangolo di intersezione nel rettangolo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="e684d-114">Calculates the intersection of two source rectangles and places the coordinates of the intersection rectangle into the destination rectangle.</span></span> |
| [<span data-ttu-id="e684d-115">**IsRectEmpty**</span><span class="sxs-lookup"><span data-stu-id="e684d-115">**IsRectEmpty**</span></span>](/windows/desktop/api/Winuser/nf-winuser-isrectempty)     | <span data-ttu-id="e684d-116">Determina se il rettangolo specificato è vuoto.</span><span class="sxs-lookup"><span data-stu-id="e684d-116">Determines whether the specified rectangle is empty.</span></span>                                                                                          |
| [<span data-ttu-id="e684d-117">**OffsetRect**</span><span class="sxs-lookup"><span data-stu-id="e684d-117">**OffsetRect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-offsetrect)       | <span data-ttu-id="e684d-118">Sposta il rettangolo specificato in base agli offset specificati.</span><span class="sxs-lookup"><span data-stu-id="e684d-118">Moves the specified rectangle by the specified offsets.</span></span>                                                                                       |
| [<span data-ttu-id="e684d-119">**PtInRect**</span><span class="sxs-lookup"><span data-stu-id="e684d-119">**PtInRect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-ptinrect)           | <span data-ttu-id="e684d-120">Determina se il punto specificato si trova all'interno del rettangolo specificato.</span><span class="sxs-lookup"><span data-stu-id="e684d-120">Determines whether the specified point lies within the specified rectangle.</span></span>                                                                   |
| [<span data-ttu-id="e684d-121">**SetRect**</span><span class="sxs-lookup"><span data-stu-id="e684d-121">**SetRect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-setrect)             | <span data-ttu-id="e684d-122">Imposta le coordinate del rettangolo specificato.</span><span class="sxs-lookup"><span data-stu-id="e684d-122">Sets the coordinates of the specified rectangle.</span></span>                                                                                              |
| [<span data-ttu-id="e684d-123">**SetRectEmpty**</span><span class="sxs-lookup"><span data-stu-id="e684d-123">**SetRectEmpty**</span></span>](/windows/desktop/api/Winuser/nf-winuser-setrectempty)   | <span data-ttu-id="e684d-124">Crea un rettangolo vuoto in cui tutte le coordinate sono impostate su zero.</span><span class="sxs-lookup"><span data-stu-id="e684d-124">Creates an empty rectangle in which all coordinates are set to zero.</span></span>                                                                          |
| [<span data-ttu-id="e684d-125">**SubtractRect**</span><span class="sxs-lookup"><span data-stu-id="e684d-125">**SubtractRect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-subtractrect)   | <span data-ttu-id="e684d-126">Determina le coordinate di un rettangolo formato sottraendo un rettangolo da un altro.</span><span class="sxs-lookup"><span data-stu-id="e684d-126">Determines the coordinates of a rectangle formed by subtracting one rectangle from another.</span></span>                                                   |
| [<span data-ttu-id="e684d-127">**UnionRect**</span><span class="sxs-lookup"><span data-stu-id="e684d-127">**UnionRect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-unionrect)         | <span data-ttu-id="e684d-128">Crea l'Unione di due rettangoli.</span><span class="sxs-lookup"><span data-stu-id="e684d-128">Creates the union of two rectangles.</span></span>                                                                                                          |



 

 

 



