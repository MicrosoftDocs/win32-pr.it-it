---
description: Alcune applicazioni forniscono funzionalità che riflettono gli oggetti (o mirror) disegnati nell'area client.
ms.assetid: 2205dc3c-ca4b-4a0a-be3e-0332ce8467a0
title: Reflection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d8e327af098a4e232e2a6734b37a17a1ac85f19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978354"
---
# <a name="reflection"></a><span data-ttu-id="44f59-103">Reflection</span><span class="sxs-lookup"><span data-stu-id="44f59-103">Reflection</span></span>

<span data-ttu-id="44f59-104">Alcune applicazioni forniscono funzionalità che riflettono gli oggetti (o mirror) disegnati nell'area client.</span><span class="sxs-lookup"><span data-stu-id="44f59-104">Some applications provide features that reflect (or mirror) objects drawn in the client area.</span></span> <span data-ttu-id="44f59-105">Le applicazioni che contengono funzionalità di Reflection usano la funzione [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) per impostare i valori appropriati nello spazio globale sulla trasformazione dello spazio pagina.</span><span class="sxs-lookup"><span data-stu-id="44f59-105">Applications that contain reflection capabilities use the [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) function to set the appropriate values in the world-space to page-space transformation.</span></span> <span data-ttu-id="44f59-106">Questa funzione [**riceve un puntatore a una struttura che**](/windows/win32/api/wingdi/ns-wingdi-xform) contiene i valori appropriati.</span><span class="sxs-lookup"><span data-stu-id="44f59-106">This function receives a pointer to an [**XFORM**](/windows/win32/api/wingdi/ns-wingdi-xform) structure containing the appropriate values.</span></span> <span data-ttu-id="44f59-107">I membri eM11 e eM22 di l'oggetto di controllo di stato specificano rispettivamente i componenti di Reflection orizzontale e verticale.</span><span class="sxs-lookup"><span data-stu-id="44f59-107">The eM11 and eM22 members of XFORM specify the horizontal and vertical reflection components, respectively.</span></span>

<span data-ttu-id="44f59-108">La *trasformazione Reflection* crea un'immagine speculare di un oggetto in relazione all'asse x o y.</span><span class="sxs-lookup"><span data-stu-id="44f59-108">The *reflection transformation* creates a mirror image of an object with respect to either the x- or y-axis.</span></span> <span data-ttu-id="44f59-109">In breve, la reflection è solo una scala negativa.</span><span class="sxs-lookup"><span data-stu-id="44f59-109">In short, reflection is just negative scaling.</span></span> <span data-ttu-id="44f59-110">Per produrre una reflection orizzontale, le coordinate x vengono moltiplicate per 1.</span><span class="sxs-lookup"><span data-stu-id="44f59-110">To produce a horizontal reflection, x-coordinates are multiplied by 1.</span></span> <span data-ttu-id="44f59-111">Per produrre una reflection verticale, le coordinate y vengono moltiplicate per 1.</span><span class="sxs-lookup"><span data-stu-id="44f59-111">To produce a vertical reflection, y-coordinates are multiplied by 1.</span></span>

<span data-ttu-id="44f59-112">La reflection orizzontale può essere rappresentata dall'algoritmo seguente:</span><span class="sxs-lookup"><span data-stu-id="44f59-112">Horizontal reflection can be represented by the following algorithm:</span></span>

``` syntax
x' = -x 
```

<span data-ttu-id="44f59-113">dove x è la coordinata x e x ' è il risultato della reflection.</span><span class="sxs-lookup"><span data-stu-id="44f59-113">where x is the x-coordinate and x' is the result of the reflection.</span></span>

<span data-ttu-id="44f59-114">La matrice 2 per 2 che ha prodotto la reflection orizzontale contiene i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="44f59-114">The 2-by-2 matrix that produced horizontal reflection contains the following values:</span></span>

``` syntax
|-1    0| 
|0     1| 
```

<span data-ttu-id="44f59-115">La reflection verticale può essere rappresentata dall'algoritmo seguente:</span><span class="sxs-lookup"><span data-stu-id="44f59-115">Vertical reflection can be represented by the following algorithm:</span></span>

``` syntax
y' = -y 
```

<span data-ttu-id="44f59-116">dove y è la coordinata y e y "è il risultato della reflection.</span><span class="sxs-lookup"><span data-stu-id="44f59-116">where y is the y-coordinate and y' is the result of the reflection.</span></span>

<span data-ttu-id="44f59-117">La matrice 2 per 2 che ha prodotto la reflection verticale contiene i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="44f59-117">The 2-by-2 matrix that produced vertical reflection contains the following values:</span></span>

``` syntax
|1    0| 
|0   -1| 
```

<span data-ttu-id="44f59-118">Le operazioni di Reflection orizzontale e verticale possono essere combinate in una singola operazione usando la matrice 2-by-2 seguente:</span><span class="sxs-lookup"><span data-stu-id="44f59-118">The horizontal-reflection and vertical-reflection operations can be combined into a single operation by using the following 2-by-2 matrix:</span></span>

``` syntax
|-1    0| 
|0    -1| 
```

 

 



