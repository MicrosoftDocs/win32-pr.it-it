---
description: Alcune applicazioni forniscono funzionalità che consentono di disegnare oggetti di taglio nell'area client.
ms.assetid: e5b82013-f6b9-460d-9f53-1b50dee2064f
title: Taglio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c641ee0275828a7552251b0f8901c1ea41280b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232551"
---
# <a name="shear"></a><span data-ttu-id="646df-103">Taglio</span><span class="sxs-lookup"><span data-stu-id="646df-103">Shear</span></span>

<span data-ttu-id="646df-104">Alcune applicazioni forniscono funzionalità che consentono di disegnare oggetti di taglio nell'area client.</span><span class="sxs-lookup"><span data-stu-id="646df-104">Some applications provide features that shear objects drawn in the client area.</span></span> <span data-ttu-id="646df-105">Le applicazioni che usano le funzionalità di taglio usano la funzione [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) per impostare i valori appropriati nella trasformazione spazio globale nella pagina.</span><span class="sxs-lookup"><span data-stu-id="646df-105">Applications that use shear capabilities use the [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) function to set appropriate values in the world-space to page-space transformation.</span></span> <span data-ttu-id="646df-106">Questa funzione [**riceve un puntatore a una struttura che**](/windows/win32/api/wingdi/ns-wingdi-xform) contiene i valori appropriati.</span><span class="sxs-lookup"><span data-stu-id="646df-106">This function receives a pointer to an [**XFORM**](/windows/win32/api/wingdi/ns-wingdi-xform) structure containing the appropriate values.</span></span> <span data-ttu-id="646df-107">I membri eM12 e eM21 di l'oggetto di controllo di stato specificano rispettivamente le costanti di proporzionalità orizzontale e verticale.</span><span class="sxs-lookup"><span data-stu-id="646df-107">The eM12 and eM21 members of XFORM specify the horizontal and vertical proportionality constants, respectively.</span></span>

<span data-ttu-id="646df-108">Sono disponibili due componenti per la *trasformazione di taglio*.</span><span class="sxs-lookup"><span data-stu-id="646df-108">There are two components of the *shear transformation*.</span></span> <span data-ttu-id="646df-109">Il primo modifica le linee verticali in un oggetto; il secondo modifica le linee orizzontali.</span><span class="sxs-lookup"><span data-stu-id="646df-109">The first alters the vertical lines in an object; the second alters the horizontal lines.</span></span> <span data-ttu-id="646df-110">Nell'illustrazione seguente viene mostrato un rettangolo di 20 unità, con tranciatura orizzontale quando viene copiato dallo spazio globale allo spazio della pagina.</span><span class="sxs-lookup"><span data-stu-id="646df-110">The following illustration shows a 20-by-20-unit rectangle sheared horizontally when copied from world space to page space.</span></span>

![illustrazione che mostra un rettangolo nello spazio globale e un trapeziod nello spazio della pagina](images/cstrn-13.png)

<span data-ttu-id="646df-112">Una cesoia orizzontale può essere rappresentata dall'algoritmo seguente:</span><span class="sxs-lookup"><span data-stu-id="646df-112">A horizontal shear can be represented by the following algorithm:</span></span>

``` syntax
x' = x + (Sx * y) 
```

<span data-ttu-id="646df-113">dove x è la coordinata x originale, SX è la costante di proporzionalità e x ' è il risultato della trasformazione di taglio.</span><span class="sxs-lookup"><span data-stu-id="646df-113">where x is the original x-coordinate, Sx is the proportionality constant, and x' is the result of the shear transformation.</span></span>

<span data-ttu-id="646df-114">Una cesoia verticale può essere rappresentata dall'algoritmo seguente:</span><span class="sxs-lookup"><span data-stu-id="646df-114">A vertical shear can be represented by the following algorithm:</span></span>

``` syntax
y' = y + (Sy * x) 
```

<span data-ttu-id="646df-115">dove y è la coordinata y originale, Sy è la costante di proporzionalità e y è il risultato della trasformazione di taglio.</span><span class="sxs-lookup"><span data-stu-id="646df-115">where y is the original y-coordinate, Sy is the proportionality constant, and y' is the result of the shear transformation.</span></span>

<span data-ttu-id="646df-116">Le trasformazioni orizzontali e a taglio verticale possono essere combinate in una singola operazione usando una matrice 2 per 2.</span><span class="sxs-lookup"><span data-stu-id="646df-116">The horizontal-shear and vertical-shear transformations can be combined into a single operation using a 2-by-2 matrix.</span></span>

``` syntax
|x' y'| == |x y| * |  1   Sx| 
                   | Sy    1| 
```

<span data-ttu-id="646df-117">La matrice 2 per 2 che ha prodotto la distorsione contiene i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="646df-117">The 2-by-2 matrix that produced the shear contains the following values:</span></span>

``` syntax
|1    1| 
|0    1| 
```

 

 



