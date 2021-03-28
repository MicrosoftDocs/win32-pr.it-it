---
description: Un'applicazione combina due aree chiamando la funzione CombineRgn.
ms.assetid: d16f9ca5-33e2-4752-900e-743245838377
title: Combinazione di aree
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f51db22daea448acfb02120844ca2859a5ba11e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104566839"
---
# <a name="combining-regions"></a><span data-ttu-id="0ff66-103">Combinazione di aree</span><span class="sxs-lookup"><span data-stu-id="0ff66-103">Combining Regions</span></span>

<span data-ttu-id="0ff66-104">Un'applicazione combina due aree chiamando la funzione [**CombineRgn**](/windows/desktop/api/Wingdi/nf-wingdi-combinergn) .</span><span class="sxs-lookup"><span data-stu-id="0ff66-104">An application combines two regions by calling the [**CombineRgn**](/windows/desktop/api/Wingdi/nf-wingdi-combinergn) function.</span></span> <span data-ttu-id="0ff66-105">Utilizzando questa funzione, un'applicazione può combinare le parti intersecanti di due aree, tutte tranne le parti intersecanti di due aree, le due aree originali e così via.</span><span class="sxs-lookup"><span data-stu-id="0ff66-105">Using this function, an application can combine the intersecting parts of two regions, all but the intersecting parts of two regions, the two original regions in their entirety, and so on.</span></span> <span data-ttu-id="0ff66-106">Di seguito sono riportati cinque valori che definiscono le combinazioni di aree.</span><span class="sxs-lookup"><span data-stu-id="0ff66-106">Following are five values that define the region combinations.</span></span>



| <span data-ttu-id="0ff66-107">Valore</span><span class="sxs-lookup"><span data-stu-id="0ff66-107">Value</span></span>     | <span data-ttu-id="0ff66-108">Significato</span><span class="sxs-lookup"><span data-stu-id="0ff66-108">Meaning</span></span>                                                                               |
|-----------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0ff66-109">RGN \_ e</span><span class="sxs-lookup"><span data-stu-id="0ff66-109">RGN\_AND</span></span>  | <span data-ttu-id="0ff66-110">Le parti che intersecano due aree originali definiscono una nuova regione.</span><span class="sxs-lookup"><span data-stu-id="0ff66-110">The intersecting parts of two original regions define a new region.</span></span>                   |
| <span data-ttu-id="0ff66-111">copia di RGN \_</span><span class="sxs-lookup"><span data-stu-id="0ff66-111">RGN\_COPY</span></span> | <span data-ttu-id="0ff66-112">Una copia della prima (delle due aree originali) definisce una nuova area.</span><span class="sxs-lookup"><span data-stu-id="0ff66-112">A copy of the first (of the two original regions) defines a new region.</span></span>               |
| <span data-ttu-id="0ff66-113">\_diff RGN</span><span class="sxs-lookup"><span data-stu-id="0ff66-113">RGN\_DIFF</span></span> | <span data-ttu-id="0ff66-114">La parte della prima area che non interseca la seconda definisce una nuova area.</span><span class="sxs-lookup"><span data-stu-id="0ff66-114">The part of the first region that does not intersect the second defines a new region.</span></span> |
| <span data-ttu-id="0ff66-115">RGN \_ o</span><span class="sxs-lookup"><span data-stu-id="0ff66-115">RGN\_OR</span></span>   | <span data-ttu-id="0ff66-116">Le due aree originali definiscono una nuova area.</span><span class="sxs-lookup"><span data-stu-id="0ff66-116">The two original regions define a new region.</span></span>                                         |
| <span data-ttu-id="0ff66-117">\_Xor RGN</span><span class="sxs-lookup"><span data-stu-id="0ff66-117">RGN\_XOR</span></span>  | <span data-ttu-id="0ff66-118">Le parti delle due aree originali che non si sovrappongono definiscono una nuova area.</span><span class="sxs-lookup"><span data-stu-id="0ff66-118">Those parts of the two original regions that do not overlap define a new region.</span></span>      |



 

<span data-ttu-id="0ff66-119">Nella figura seguente sono illustrate le cinque combinazioni possibili di un quadrato e di un'area circolare risultante da una chiamata a [**CombineRgn**](/windows/desktop/api/Wingdi/nf-wingdi-combinergn).</span><span class="sxs-lookup"><span data-stu-id="0ff66-119">The following illustration shows the five possible combinations of a square and a circular region resulting from a call to [**CombineRgn**](/windows/desktop/api/Wingdi/nf-wingdi-combinergn).</span></span>

![illustrazione che illustra i risultati descritti nella tabella precedente](images/csrgn-02.png)

 

 



