---
description: La maggior parte delle applicazioni di disegno e CAD fornisce funzionalità per la scalabilità dell'output creato dall'utente.
ms.assetid: 819d2026-dd5c-48d3-8af1-e96364acae72
title: Scalabilità
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f3c1ba409abda6e9c6b471a4d0a143b28d4c08e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980303"
---
# <a name="scaling"></a><span data-ttu-id="182ec-103">Scalabilità</span><span class="sxs-lookup"><span data-stu-id="182ec-103">Scaling</span></span>

<span data-ttu-id="182ec-104">La maggior parte delle applicazioni di disegno e CAD fornisce funzionalità per la scalabilità dell'output creato dall'utente.</span><span class="sxs-lookup"><span data-stu-id="182ec-104">Most CAD and drawing applications provide features that scale output created by the user.</span></span> <span data-ttu-id="182ec-105">Le applicazioni che includono funzionalità di scalabilità (o zoom) chiamano la funzione [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) per impostare lo spazio globale appropriato sulla trasformazione dello spazio pagina.</span><span class="sxs-lookup"><span data-stu-id="182ec-105">Applications that include scaling (or zoom) capabilities call the [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) function to set the appropriate world-space to page-space transformation.</span></span> <span data-ttu-id="182ec-106">Questa funzione [**riceve un puntatore a una struttura che**](/windows/win32/api/wingdi/ns-wingdi-xform) contiene i valori appropriati.</span><span class="sxs-lookup"><span data-stu-id="182ec-106">This function receives a pointer to an [**XFORM**](/windows/win32/api/wingdi/ns-wingdi-xform) structure containing the appropriate values.</span></span> <span data-ttu-id="182ec-107">I membri eM11 e eM22 di l'oggetto di controllo di stato specificano rispettivamente i componenti di scalabilità orizzontale e verticale.</span><span class="sxs-lookup"><span data-stu-id="182ec-107">The eM11 and eM22 members of XFORM specify the horizontal and vertical scaling components, respectively.</span></span>

<span data-ttu-id="182ec-108">Quando si verifica il *ridimensionamento* , le linee verticali e orizzontali (o vettori), che costituiscono un oggetto, sono allungate o compresse rispetto all'asse x o y.</span><span class="sxs-lookup"><span data-stu-id="182ec-108">When *scaling* occurs, the vertical and horizontal lines (or vectors), that constitute an object, are stretched or compressed with respect to the x- or y-axis.</span></span> <span data-ttu-id="182ec-109">La figura seguente mostra un rettangolo di 20 unità, ridimensionato verticalmente, al doppio dell'altezza originale quando viene copiato dallo spazio delle coordinate internazionali allo spazio delle coordinate di pagina.</span><span class="sxs-lookup"><span data-stu-id="182ec-109">The following illustration shows a 20-by-20-unit rectangle scaled vertically to twice its original height when copied from world-coordinate space to page-coordinate space.</span></span>

![illustrazione che mostra un piccolo rettangolo nello spazio globale e uno più alto nello spazio della pagina](images/cstrn-10.png)

<span data-ttu-id="182ec-111">Nell'illustrazione precedente, le linee verticali che definiscono la misura laterale del rettangolo originale 20 unità, mentre le linee verticali che definiscono i lati del rettangolo ridimensionato misurano 40 unità.</span><span class="sxs-lookup"><span data-stu-id="182ec-111">In the preceding illustration, the vertical lines that define the original rectangle's side measure 20 units, while the vertical lines that define the scaled rectangle's sides measure 40 units.</span></span>

<span data-ttu-id="182ec-112">La scalabilità verticale può essere rappresentata dall'algoritmo seguente.</span><span class="sxs-lookup"><span data-stu-id="182ec-112">Vertical scaling can be represented by the following algorithm.</span></span>

``` syntax
y' = y * Dy 
```

<span data-ttu-id="182ec-113">Dove y è la nuova lunghezza, y è la lunghezza originale e dy è il fattore di scala verticale.</span><span class="sxs-lookup"><span data-stu-id="182ec-113">Where y' is the new length, y is the original length, and Dy is the vertical scaling factor.</span></span>

<span data-ttu-id="182ec-114">La scalabilità orizzontale può essere rappresentata dall'algoritmo seguente.</span><span class="sxs-lookup"><span data-stu-id="182ec-114">Horizontal scaling can be represented by the following algorithm.</span></span>

``` syntax
x' = x * Dx 
```

<span data-ttu-id="182ec-115">Dove x ' è la nuova lunghezza, x è la lunghezza originale e DX è il fattore di scala orizzontale.</span><span class="sxs-lookup"><span data-stu-id="182ec-115">Where x' is the new length, x is the original length, and Dx is the horizontal scaling factor.</span></span>

<span data-ttu-id="182ec-116">Le trasformazioni di scala verticale e orizzontale possono essere combinate in una singola operazione usando una matrice 2 per 2.</span><span class="sxs-lookup"><span data-stu-id="182ec-116">The vertical and horizontal scaling transformations can be combined into a single operation by using a 2-by-2 matrix.</span></span>

``` syntax
|x' y'|  =  |Dx   0|  *  |x y| 
            |0   Dy| 
```

<span data-ttu-id="182ec-117">La matrice 2 per 2 che ha prodotto la trasformazione di ridimensionamento contiene i valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="182ec-117">The 2-by-2 matrix that produced the scaling transformation contains the following values.</span></span>

``` syntax
|1    0| 
|0    2| 
```

 

 



