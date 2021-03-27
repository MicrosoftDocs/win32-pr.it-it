---
description: Molte applicazioni CAD forniscono funzionalità che ruotano gli oggetti disegnati nell'area client.
ms.assetid: 85d8fe2c-5ad9-4e98-b6ff-ca0a78abeee5
title: Rotazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17be42f2826cbad09333b2c37b607dc50c7c9d0c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980679"
---
# <a name="rotation"></a><span data-ttu-id="684d6-103">Rotazione</span><span class="sxs-lookup"><span data-stu-id="684d6-103">Rotation</span></span>

<span data-ttu-id="684d6-104">Molte applicazioni CAD forniscono funzionalità che ruotano gli oggetti disegnati nell'area client.</span><span class="sxs-lookup"><span data-stu-id="684d6-104">Many CAD applications provide features that rotate objects drawn in the client area.</span></span> <span data-ttu-id="684d6-105">Le applicazioni che includono le funzionalità di rotazione usano la funzione [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) per impostare la trasformazione dello spazio globale nella pagina appropriata.</span><span class="sxs-lookup"><span data-stu-id="684d6-105">Applications that include rotation capabilities use the [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) function to set the appropriate world-space to page-space transformation.</span></span> <span data-ttu-id="684d6-106">Questa funzione [**riceve un puntatore a una struttura che**](/windows/win32/api/wingdi/ns-wingdi-xform) contiene i valori appropriati.</span><span class="sxs-lookup"><span data-stu-id="684d6-106">This function receives a pointer to an [**XFORM**](/windows/win32/api/wingdi/ns-wingdi-xform) structure containing the appropriate values.</span></span> <span data-ttu-id="684d6-107">I membri eM11, eM12, eM21 e eM22 di specificano rispettivamente il coseno, il seno, il seno negativo e il coseno dell'angolo di rotazione.</span><span class="sxs-lookup"><span data-stu-id="684d6-107">The eM11, eM12, eM21, and eM22 members of XFORM specify respectively, the cosine, sine, negative sine, and cosine of the angle of rotation.</span></span>

<span data-ttu-id="684d6-108">Quando si verifica la *rotazione* , i punti che costituiscono un oggetto vengono ruotati rispetto all'origine dello spazio delle coordinate.</span><span class="sxs-lookup"><span data-stu-id="684d6-108">When *rotation* occurs, the points that constitute an object are rotated with respect to the coordinate-space origin.</span></span> <span data-ttu-id="684d6-109">La figura seguente mostra un rettangolo di 20 unità ruotato di 30 gradi quando viene copiato dallo spazio delle coordinate internazionali allo spazio delle coordinate di pagina.</span><span class="sxs-lookup"><span data-stu-id="684d6-109">The following illustration shows a 20-by-20-unit rectangle rotated 30 degrees when copied from world-coordinate space to page-coordinate space.</span></span>

![illustrazione che mostra due spazi delle coordinate. ogni ha un rectange in una posizione diversa e con una rotazione diversa](images/cstrn-11.png)

<span data-ttu-id="684d6-111">Nell'illustrazione precedente ogni punto nel rettangolo è stato ruotato di 30 gradi rispetto all'origine dello spazio delle coordinate.</span><span class="sxs-lookup"><span data-stu-id="684d6-111">In the preceding illustration, each point in the rectangle was rotated 30 degrees with respect to the coordinate-space origin.</span></span>

<span data-ttu-id="684d6-112">Nell'algoritmo seguente viene calcolata la nuova coordinata x (x) per un punto (x, y) ruotato dell'angolo A rispetto all'origine dello spazio delle coordinate.</span><span class="sxs-lookup"><span data-stu-id="684d6-112">The following algorithm computes the new x-coordinate (x ') for a point (x,y ) that is rotated by angle A with respect to the coordinate-space origin.</span></span>

``` syntax
x' = (x * cos A) - (y * sin A) 
```

<span data-ttu-id="684d6-113">Nell'algoritmo seguente viene calcolata la coordinata y (y) per un punto (x, y) ruotato dall'angolo A rispetto all'origine.</span><span class="sxs-lookup"><span data-stu-id="684d6-113">The following algorithm computes the y-coordinate (y ') for a point (x,y ) that is rotated by the angle A with respect to the origin.</span></span>

``` syntax
y' = (x * sin A) + (y * cos A) 
```

<span data-ttu-id="684d6-114">Le due trasformazioni di rotazione possono essere combinate in una matrice 2 per 2 come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="684d6-114">The two rotation transformations can be combined in a 2-by-2 matrix as follows.</span></span>

``` syntax
|x' y'| == |x y| * | cos A   sin A| 
                   |-sin A   cos A| 
```

<span data-ttu-id="684d6-115">La matrice 2 per 2 che ha prodotto la rotazione contiene i valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="684d6-115">The 2-by-2 matrix that produced the rotation contains the following values.</span></span>

``` syntax
| .8660    .5000| 
|-.5000    .8660| 
```

## <a name="rotation-algorithm-derivation"></a><span data-ttu-id="684d6-116">Derivazione dell'algoritmo di rotazione</span><span class="sxs-lookup"><span data-stu-id="684d6-116">Rotation Algorithm Derivation</span></span>

<span data-ttu-id="684d6-117">Gli algoritmi di rotazione sono basati sul teorema di addizione di trigonometria che informa che la funzione trigonometrica di una somma di due angoli (a1 e a2) può essere espressa in termini di funzioni trigonometriche dei due angoli.</span><span class="sxs-lookup"><span data-stu-id="684d6-117">Rotation algorithms are based on trigonometry's addition theorem stating that the trigonometric function of a sum of two angles (A1 and A2 ) can be expressed in terms of the trigonometric functions of the two angles.</span></span>

``` syntax
sin(A1 + A2) = (sin A1 * cos A2) + (cos A1 * sin A2) 
cos(A1 + A2) = (cos A1 * cos A2) - (sin A1 * sin A2) 
```

<span data-ttu-id="684d6-118">Nella figura seguente viene mostrato un punto p ruotato in senso antiorario a una nuova posizione p '.</span><span class="sxs-lookup"><span data-stu-id="684d6-118">The following illustration shows a point p rotated counterclockwise to a new position p'.</span></span> <span data-ttu-id="684d6-119">Inoltre, vengono visualizzati due triangoli formati da una linea disegnata dall'origine dello spazio delle coordinate a ogni punto e una linea disegnata da ogni punto attraverso l'asse x.</span><span class="sxs-lookup"><span data-stu-id="684d6-119">In addition, it shows two triangles formed by a line drawn from the coordinate-space origin to each point and a line drawn from each point through the x-axis.</span></span>

![diagramma che mostra l'origine, p e p ' e due triangoli](images/cstrn-12.png)

<span data-ttu-id="684d6-121">Con la trigonometria, è possibile ottenere la coordinata x del punto p moltiplicando la lunghezza dell'ipotenusa h per il coseno di a1.</span><span class="sxs-lookup"><span data-stu-id="684d6-121">Using trigonometry, the x-coordinate of point p can be obtained by multiplying the length of the hypotenuse h by the cosine of A1.</span></span>

``` syntax
x = h * cos A1 
```

<span data-ttu-id="684d6-122">La coordinata y del punto p può essere ottenuta moltiplicando la lunghezza dell'ipotenusa h per il seno di a1.</span><span class="sxs-lookup"><span data-stu-id="684d6-122">The y-coordinate of point p can be obtained by multiplying the length of the hypotenuse h by the sine of A1.</span></span>

``` syntax
y = h * sin A1 
```

<span data-ttu-id="684d6-123">Analogamente, la coordinata x del punto p ' può essere ottenuta moltiplicando la lunghezza dell'ipotenusa h per il coseno di (a1 + a2).</span><span class="sxs-lookup"><span data-stu-id="684d6-123">Likewise, the x-coordinate of point p' can be obtained by multiplying the length of the hypotenuse h by the cosine of (A1 +A2 ).</span></span>

``` syntax
x' = h * cos (A1 + A2) 
```

<span data-ttu-id="684d6-124">Infine, la coordinata y del punto p ' può essere ottenuta moltiplicando la lunghezza dell'ipotenusa h per il seno di (a1 + a2).</span><span class="sxs-lookup"><span data-stu-id="684d6-124">Finally, the y-coordinate of point p' can be obtained by multiplying the length of the hypotenuse h by the sine of (A1 +A2 ).</span></span>

``` syntax
y' = h * sin (A1 + A2) 
```

<span data-ttu-id="684d6-125">Utilizzando il teorema di aggiunta, gli algoritmi precedenti diventano gli elementi seguenti:</span><span class="sxs-lookup"><span data-stu-id="684d6-125">Using the addition theorem, the preceding algorithms become the following:</span></span>

``` syntax
x' = (h * cos A1 * cos A2) - (h * sin A1 * sin A2) 
y' = (h * cos A1 * sin A2) + (h * sin A1 * cos A2) 
```

<span data-ttu-id="684d6-126">Gli algoritmi di rotazione per un determinato punto ruotato dell'angolo a2 possono essere ottenuti sostituendo x per ogni occorrenza di (h \* cos a1) e sostituendo y per ogni occorrenza di (h \* sin a1).</span><span class="sxs-lookup"><span data-stu-id="684d6-126">The rotation algorithms for a given point rotated by angle A2 can be obtained by substituting x for each occurrence of (h \* cos A1 ) and by substituting y for each occurrence of (h \* sin A1 ).</span></span>

``` syntax
x' = (x * cos A2) - (y * sin A2) 
y' = (x * sin A2) + (y * cos A2) 
```

 

 



