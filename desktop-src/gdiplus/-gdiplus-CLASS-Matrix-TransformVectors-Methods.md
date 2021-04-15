---
description: In questo argomento vengono elencati i metodi TransformVectors della classe Matrix. Per un elenco completo dei metodi per la classe Matrix, vedere Metodi Matrix.
ms.assetid: 6a2ed6a7-825a-422b-b035-b88746f3ab5d
title: Metodi Matrix. TransformVectors (Gdiplusmatrix. h)
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 3bdb67d839163ffe2d26623a01fc186f8e885ca2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "104982899"
---
# <a name="matrixtransformvectors-methods"></a><span data-ttu-id="92b64-104">Metodi Matrix. TransformVectors</span><span class="sxs-lookup"><span data-stu-id="92b64-104">Matrix.TransformVectors methods</span></span>

<span data-ttu-id="92b64-105">In questo argomento vengono elencati i metodi TransformVectors della classe [**Matrix**](/windows/win32/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) .</span><span class="sxs-lookup"><span data-stu-id="92b64-105">This topic lists the TransformVectors methods of the [**Matrix**](/windows/win32/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) class.</span></span> <span data-ttu-id="92b64-106">Per un elenco completo dei metodi per la classe **Matrix** , vedere [Metodi Matrix](-gdiplus-class-matrix-methods.md).</span><span class="sxs-lookup"><span data-stu-id="92b64-106">For a complete list of methods for the **Matrix** class, see [Matrix Methods](-gdiplus-class-matrix-methods.md).</span></span>

### <a name="overload-list"></a><span data-ttu-id="92b64-107">Elenco di overload</span><span class="sxs-lookup"><span data-stu-id="92b64-107">Overload list</span></span>



| <span data-ttu-id="92b64-108">Metodo</span><span class="sxs-lookup"><span data-stu-id="92b64-108">Method</span></span>                                                                                                 | <span data-ttu-id="92b64-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="92b64-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                      |
|:-------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="92b64-110">[**TransformVectors (Point \* , int)**](/windows/win32/api/gdiplusmatrix/nf-gdiplusmatrix-matrix-transformvectors(inoutpoint_inint))</span><span class="sxs-lookup"><span data-stu-id="92b64-110">[**TransformVectors(Point\*,INT)**](/windows/win32/api/gdiplusmatrix/nf-gdiplusmatrix-matrix-transformvectors(inoutpoint_inint))</span></span>   | <span data-ttu-id="92b64-111">Il metodo [**Matrix:: TransformVectors**](/windows/win32/api/gdiplusmatrix/nf-gdiplusmatrix-matrix-transformvectors(inoutpoint_inint)) moltiplica ogni vettore in una matrice da questa matrice.</span><span class="sxs-lookup"><span data-stu-id="92b64-111">The [**Matrix::TransformVectors**](/windows/win32/api/gdiplusmatrix/nf-gdiplusmatrix-matrix-transformvectors(inoutpoint_inint)) method multiplies each vector in an array by this matrix.</span></span> <span data-ttu-id="92b64-112">Gli elementi di traslazione di questa matrice (terza riga) vengono ignorati.</span><span class="sxs-lookup"><span data-stu-id="92b64-112">The translation elements of this matrix (third row) are ignored.</span></span> <span data-ttu-id="92b64-113">Ogni vettore viene considerato come una matrice di righe.</span><span class="sxs-lookup"><span data-stu-id="92b64-113">Each vector is treated as a row matrix.</span></span> <span data-ttu-id="92b64-114">La moltiplicazione viene eseguita con la matrice di riga a sinistra e questa matrice a destra.</span><span class="sxs-lookup"><span data-stu-id="92b64-114">The multiplication is performed with the row matrix on the left and this matrix on the right.</span></span><br/>  |
| <span data-ttu-id="92b64-115">[**TransformVectors (PointF \* , int)**](/previous-versions//ms535319(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="92b64-115">[**TransformVectors(PointF\*,INT)**](/previous-versions//ms535319(v=vs.85))</span></span> | <span data-ttu-id="92b64-116">Il metodo [**Matrix:: TransformVectors**](/previous-versions//ms535319(v=vs.85)) moltiplica ogni vettore in una matrice da questa matrice.</span><span class="sxs-lookup"><span data-stu-id="92b64-116">The [**Matrix::TransformVectors**](/previous-versions//ms535319(v=vs.85)) method multiplies each vector in an array by this matrix.</span></span> <span data-ttu-id="92b64-117">Gli elementi di traslazione di questa matrice (terza riga) vengono ignorati.</span><span class="sxs-lookup"><span data-stu-id="92b64-117">The translation elements of this matrix (third row) are ignored.</span></span> <span data-ttu-id="92b64-118">Ogni vettore viene considerato come una matrice di righe.</span><span class="sxs-lookup"><span data-stu-id="92b64-118">Each vector is treated as a row matrix.</span></span> <span data-ttu-id="92b64-119">La moltiplicazione viene eseguita con la matrice di riga a sinistra e questa matrice a destra.</span><span class="sxs-lookup"><span data-stu-id="92b64-119">The multiplication is performed with the row matrix on the left and this matrix on the right.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="92b64-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="92b64-120">Requirements</span></span>



| <span data-ttu-id="92b64-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="92b64-121">Requirement</span></span> | <span data-ttu-id="92b64-122">Valore</span><span class="sxs-lookup"><span data-stu-id="92b64-122">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="92b64-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="92b64-123">Header</span></span><br/> | <dl> <span data-ttu-id="92b64-124"><dt>Gdiplusmatrix. h</dt></span><span class="sxs-lookup"><span data-stu-id="92b64-124"><dt>Gdiplusmatrix.h</dt></span></span> </dl> |



 

 
