---
description: Alcune applicazioni traducono o spostano oggetti disegnati nell'area client.
ms.assetid: e319a5c6-a045-42b1-a83e-3a978172b52c
title: Traduzione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 699ec4c75ebb79e440fbc9b01231fe83feb942dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104987655"
---
# <a name="translation"></a><span data-ttu-id="48dea-103">Traduzione</span><span class="sxs-lookup"><span data-stu-id="48dea-103">Translation</span></span>

<span data-ttu-id="48dea-104">Alcune applicazioni traducono o spostano oggetti disegnati nell'area client.</span><span class="sxs-lookup"><span data-stu-id="48dea-104">Some applications translate (or shift) objects drawn in the client area.</span></span> <span data-ttu-id="48dea-105">chiamando la funzione [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) per impostare lo spazio globale appropriato sulla trasformazione dello spazio pagina.</span><span class="sxs-lookup"><span data-stu-id="48dea-105">by calling the [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) function to set the appropriate world-space to page-space transformation.</span></span> <span data-ttu-id="48dea-106">La funzione SetWorldTransform [**riceve un puntatore a una struttura che**](/windows/win32/api/wingdi/ns-wingdi-xform) contiene i valori appropriati.</span><span class="sxs-lookup"><span data-stu-id="48dea-106">The SetWorldTransform function receives a pointer to an [**XFORM**](/windows/win32/api/wingdi/ns-wingdi-xform) structure containing the appropriate values.</span></span> <span data-ttu-id="48dea-107">I membri di eDx e eDy del controllo di stato specificano rispettivamente i componenti di traduzione orizzontale e verticale.</span><span class="sxs-lookup"><span data-stu-id="48dea-107">The eDx and eDy members of XFORM specify the horizontal and vertical translation components, respectively.</span></span>

<span data-ttu-id="48dea-108">Quando si verifica la *conversione* , ogni punto in un oggetto viene spostato verticalmente, orizzontalmente o entrambi, in base a una quantità specificata.</span><span class="sxs-lookup"><span data-stu-id="48dea-108">When *translation* occurs, each point in an object is shifted vertically, horizontally, or both, by a specified amount.</span></span> <span data-ttu-id="48dea-109">Nella figura seguente viene illustrato un rettangolo di 20 unità che è stato convertito a destra di 10 unità quando viene copiato dallo spazio delle coordinate internazionali allo spazio delle coordinate di pagina.</span><span class="sxs-lookup"><span data-stu-id="48dea-109">The following illustration shows a 20- by 20-unit rectangle that was translated to the right by 10 units when copied from world-coordinate space to page-coordinate space.</span></span>

![illustrazione che mostra un rettangolo in una posizione nello spazio globale e in una posizione diversa nello spazio della pagina](images/cstrn-09.png)

<span data-ttu-id="48dea-111">Nell'illustrazione precedente, la coordinata x di ogni punto nel rettangolo è 10 unità maggiore della coordinata x originale.</span><span class="sxs-lookup"><span data-stu-id="48dea-111">In the preceding illustration, the x-coordinate of each point in the rectangle is 10 units greater than the original x-coordinate.</span></span>

<span data-ttu-id="48dea-112">La traduzione orizzontale può essere rappresentata dall'algoritmo seguente.</span><span class="sxs-lookup"><span data-stu-id="48dea-112">Horizontal translation can be represented by the following algorithm.</span></span>

``` syntax
x' = x + Dx 
```

<span data-ttu-id="48dea-113">Dove x è la nuova coordinata x, x è la coordinata x originale e DX è la distanza orizzontale spostata.</span><span class="sxs-lookup"><span data-stu-id="48dea-113">Where x' is the new x-coordinate, x is the original x-coordinate, and Dx is the horizontal distance moved.</span></span>

<span data-ttu-id="48dea-114">La conversione verticale può essere rappresentata dall'algoritmo seguente.</span><span class="sxs-lookup"><span data-stu-id="48dea-114">Vertical translation can be represented by the following algorithm.</span></span>

``` syntax
y' = y + Dy 
```

<span data-ttu-id="48dea-115">Dove y è la nuova coordinata y, y è la coordinata y originale e dy è la distanza verticale spostata.</span><span class="sxs-lookup"><span data-stu-id="48dea-115">Where y' is the new y-coordinate, y is the original y-coordinate, and Dy is the vertical distance moved.</span></span>

<span data-ttu-id="48dea-116">Le trasformazioni di traslazione orizzontali e verticali possono essere combinate in una singola operazione usando una matrice 3 per 3.</span><span class="sxs-lookup"><span data-stu-id="48dea-116">The horizontal and vertical translation transformations can be combined into a single operation by using a 3-by-3 matrix.</span></span>

``` syntax
                      |1   0   0| 
|x' y' 1| = |x y 1| * |0   1   0| 
                      |Dx  Dy  1| 
```

<span data-ttu-id="48dea-117">(Regole dello stato di moltiplicazione della matrice in cui il numero di righe di una matrice deve essere uguale al numero di colonne nell'altro.</span><span class="sxs-lookup"><span data-stu-id="48dea-117">(The rules of matrix multiplication state that the number of rows in one matrix must equal the number of columns in the other.</span></span> <span data-ttu-id="48dea-118">Il numero intero 1 nella matrice \| x y 1 \| è un segnaposto che è stato aggiunto per soddisfare questo requisito.</span><span class="sxs-lookup"><span data-stu-id="48dea-118">The integer 1 in the matrix \|x y 1\| is a placeholder that was added to meet this requirement.)</span></span>

<span data-ttu-id="48dea-119">La matrice 3 per 3 che ha prodotto la trasformazione di conversione illustrata contiene i valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="48dea-119">The 3-by-3 matrix that produced the illustrated translation transformation contains the following values.</span></span>

``` syntax
|1  0  0| 
|0  1  0| 
|10 0  1| 
```

 

 



