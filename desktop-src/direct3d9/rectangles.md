---
description: Durante la programmazione di Direct3D e finestre, gli oggetti sullo schermo vengono definiti in termini di rettangoli di delimitazione.
ms.assetid: 9e271652-1673-42ea-b1f4-31ac63c397c5
title: Rettangoli (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd74538e81482061452382de3123243c3dffe7a8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104123435"
---
# <a name="rectangles-direct3d-9"></a><span data-ttu-id="71489-103">Rettangoli (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="71489-103">Rectangles (Direct3D 9)</span></span>

<span data-ttu-id="71489-104">Durante la programmazione di Direct3D e finestre, gli oggetti sullo schermo vengono definiti in termini di rettangoli di delimitazione.</span><span class="sxs-lookup"><span data-stu-id="71489-104">Throughout Direct3D and Window programming, objects on the screen are referred to in terms of bounding rectangles.</span></span> <span data-ttu-id="71489-105">I lati di un rettangolo di delimitazione sono sempre paralleli ai lati dello schermo, quindi il rettangolo può essere descritto da due punti, dall'angolo superiore sinistro e dall'angolo inferiore destro.</span><span class="sxs-lookup"><span data-stu-id="71489-105">The sides of a bounding rectangle are always parallel to the sides of the screen, so the rectangle can be described by two points, the upper-left corner and lower-right corner.</span></span> <span data-ttu-id="71489-106">La maggior parte delle applicazioni usa la struttura [**Rect**](/previous-versions//dd162897(v=vs.85)) per includere informazioni su un rettangolo di delimitazione da usare quando blitting sullo schermo o eseguendo il rilevamento dei riscontri.</span><span class="sxs-lookup"><span data-stu-id="71489-106">Most applications use the [**RECT**](/previous-versions//dd162897(v=vs.85)) structure to carry information about a bounding rectangle to use when blitting to the screen or performing hit detection.</span></span>

<span data-ttu-id="71489-107">In C++, la struttura [**Rect**](/previous-versions//dd162897(v=vs.85)) presenta la definizione seguente.</span><span class="sxs-lookup"><span data-stu-id="71489-107">In C++, the [**RECT**](/previous-versions//dd162897(v=vs.85)) structure has the following definition.</span></span>


```
typedef struct tagRECT { 
    LONG    left;    // This is the upper-left corner x-coordinate.
    LONG    top;     // The upper-left corner y-coordinate.
    LONG    right;   // The lower-right corner x-coordinate.
    LONG    bottom;  // The lower-right corner y-coordinate.
} RECT, *PRECT, NEAR *NPRECT, FAR *LPRECT; 
```



<span data-ttu-id="71489-108">Nell'esempio precedente i membri Left e Top sono le coordinate x e y dell'angolo superiore sinistro di un rettangolo di delimitazione.</span><span class="sxs-lookup"><span data-stu-id="71489-108">In the preceding example, the left and top members are the x- and y-coordinates of a bounding rectangle's upper-left corner.</span></span> <span data-ttu-id="71489-109">Analogamente, i membri destro e inferiore costituiscono le coordinate dell'angolo inferiore destro.</span><span class="sxs-lookup"><span data-stu-id="71489-109">Similarly, the right and bottom members make up the coordinates of the lower-right corner.</span></span> <span data-ttu-id="71489-110">Nella figura seguente viene illustrato come è possibile visualizzare questi valori.</span><span class="sxs-lookup"><span data-stu-id="71489-110">The following illustration shows how you can visualize these values.</span></span>

![illustrazione del rettangolo delimitato dai valori sinistro, superiore, destro e inferiore](images/rect.png)

<span data-ttu-id="71489-112">La colonna di pixel sul bordo destro e la riga di pixel sul bordo inferiore non sono inclusi in RECT.</span><span class="sxs-lookup"><span data-stu-id="71489-112">The column of pixels at the right edge and the row of pixels at the bottom edge are not included in the RECT.</span></span> <span data-ttu-id="71489-113">Ad esempio, il blocco di un oggetto RECT con i membri {10, 10, 138, 138} restituisce un oggetto 128 pixel in larghezza e altezza.</span><span class="sxs-lookup"><span data-stu-id="71489-113">For example, locking a RECT with members {10, 10, 138, 138} results in an object 128 pixels in width and height.</span></span>

<span data-ttu-id="71489-114">Per l'efficienza, la coerenza e la semplicità d'uso, tutte le funzioni di presentazione Direct3D funzionano con i rettangoli.</span><span class="sxs-lookup"><span data-stu-id="71489-114">In the interest of efficiency, consistency, and ease of use, all Direct3D presentation functions work with rectangles.</span></span>

## <a name="related-topics"></a><span data-ttu-id="71489-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="71489-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="71489-116">Sistemi di coordinate e geometria</span><span class="sxs-lookup"><span data-stu-id="71489-116">Coordinate Systems and Geometry</span></span>](coordinate-systems-and-geometry.md)
</dt> </dl>

 

 
