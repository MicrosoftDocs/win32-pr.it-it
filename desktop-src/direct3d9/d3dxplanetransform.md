---
description: Trasforma un piano in base a una matrice. La matrice di input è la trasposta inversa della trasformazione effettiva.
ms.assetid: 3581b397-cbd8-4aed-80dd-1841f331a367
title: Funzione D3DXPlaneTransform (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneTransform
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: fd82478d9fb1f08bb0320a8c84357efcdf20be26
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322096"
---
# <a name="d3dxplanetransform-function-d3dx9mathh"></a><span data-ttu-id="e2b0d-104">Funzione D3DXPlaneTransform (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="e2b0d-104">D3DXPlaneTransform function (D3dx9math.h)</span></span>

<span data-ttu-id="e2b0d-105">Trasforma un piano in base a una matrice.</span><span class="sxs-lookup"><span data-stu-id="e2b0d-105">Transforms a plane by a matrix.</span></span> <span data-ttu-id="e2b0d-106">La matrice di input è la trasposta inversa della trasformazione effettiva.</span><span class="sxs-lookup"><span data-stu-id="e2b0d-106">The input matrix is the inverse transpose of the actual transformation.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2b0d-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e2b0d-107">Syntax</span></span>


```C++
D3DXPLANE* D3DXPlaneTransform(
  _Inout_       D3DXPLANE  *pOut,
  _In_    const D3DXPLANE  *pP,
  _In_    const D3DXMATRIX *pM
);
```



## <a name="parameters"></a><span data-ttu-id="e2b0d-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="e2b0d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2b0d-109">*broncio* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="e2b0d-109">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e2b0d-110">Tipo: **[ **D3DXPLANE**](d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="e2b0d-110">Type: **[**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="e2b0d-111">Puntatore alla struttura [**D3DXPLANE**](d3dxplane.md) che contiene il piano trasformato risultante.</span><span class="sxs-lookup"><span data-stu-id="e2b0d-111">Pointer to the [**D3DXPLANE**](d3dxplane.md) structure that contains the resulting transformed plane.</span></span> <span data-ttu-id="e2b0d-112">Vedere l'esempio.</span><span class="sxs-lookup"><span data-stu-id="e2b0d-112">See example.</span></span>

</dd> <dt>

<span data-ttu-id="e2b0d-113">*PP* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e2b0d-113">*pP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2b0d-114">Tipo: **const [**D3DXPLANE**](d3dxplane.md) \***</span><span class="sxs-lookup"><span data-stu-id="e2b0d-114">Type: **const [**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="e2b0d-115">Puntatore alla struttura di input [**D3DXPLANE**](d3dxplane.md) , che contiene il piano che verrà trasformato.</span><span class="sxs-lookup"><span data-stu-id="e2b0d-115">Pointer to the input [**D3DXPLANE**](d3dxplane.md) structure, which contains the plane that will be transformed.</span></span> <span data-ttu-id="e2b0d-116">Il vettore (a, b, c) che descrive il piano deve essere normalizzato prima che questa funzione venga chiamata.</span><span class="sxs-lookup"><span data-stu-id="e2b0d-116">The vector (a,b,c) that describes the plane must be normalized before this function is called.</span></span> <span data-ttu-id="e2b0d-117">Vedere l'esempio.</span><span class="sxs-lookup"><span data-stu-id="e2b0d-117">See example.</span></span>

</dd> <dt>

<span data-ttu-id="e2b0d-118">*PM* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e2b0d-118">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2b0d-119">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="e2b0d-119">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="e2b0d-120">Puntatore alla struttura [**D3DXMATRIX**](d3dxmatrix.md) di origine, che contiene i valori della trasformazione.</span><span class="sxs-lookup"><span data-stu-id="e2b0d-120">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure, which contains the transformation values.</span></span> <span data-ttu-id="e2b0d-121">Questa matrice deve contenere la trasposta inversa dei valori della trasformazione.</span><span class="sxs-lookup"><span data-stu-id="e2b0d-121">This matrix must contain the inverse transpose of the transformation values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2b0d-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e2b0d-122">Return value</span></span>

<span data-ttu-id="e2b0d-123">Tipo: **[ **D3DXPLANE**](d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="e2b0d-123">Type: **[**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="e2b0d-124">Puntatore a una struttura [**D3DXPLANE**](d3dxplane.md) che rappresenta il piano trasformato.</span><span class="sxs-lookup"><span data-stu-id="e2b0d-124">Pointer to a [**D3DXPLANE**](d3dxplane.md) structure, representing the transformed plane.</span></span> <span data-ttu-id="e2b0d-125">Si tratta dello stesso valore restituito nel parametro broncio, in modo che questa funzione possa essere utilizzata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="e2b0d-125">This is the same value returned in the pOut parameter so that this function can be used as a parameter for another function.</span></span>

## <a name="remarks"></a><span data-ttu-id="e2b0d-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="e2b0d-126">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="e2b0d-127">Esempi</span><span class="sxs-lookup"><span data-stu-id="e2b0d-127">Examples</span></span>

<span data-ttu-id="e2b0d-128">Questo esempio trasforma un piano applicando una scala non uniforme.</span><span class="sxs-lookup"><span data-stu-id="e2b0d-128">This example transforms a plane by applying a non-uniform scale.</span></span>


```
D3DXPLANE   planeNew;
D3DXPLANE   plane(0,1,1,0);
D3DXPlaneNormalize(&plane, &plane);

D3DXMATRIX  matrix;
D3DXMatrixScaling(&matrix, 1.0f,2.0f,3.0f); 
D3DXMatrixInverse(&matrix, NULL, &matrix);
D3DXMatrixTranspose(&matrix, &matrix);
D3DXPlaneTransform(&planeNew, &plane, &matrix);
```



<span data-ttu-id="e2b0d-129">Un piano è descritto da AX + + + CZ + DW = 0.</span><span class="sxs-lookup"><span data-stu-id="e2b0d-129">A plane is described by ax + by + cz + dw = 0.</span></span> <span data-ttu-id="e2b0d-130">Il primo piano viene creato con (a, b, c, d) = (0, 1, 1, 0), che è un piano descritto da y + z = 0.</span><span class="sxs-lookup"><span data-stu-id="e2b0d-130">The first plane is created with (a,b,c,d) = (0,1,1,0), which is a plane described by y + z = 0.</span></span> <span data-ttu-id="e2b0d-131">Dopo la scalabilità, il nuovo piano contiene (a, b, c, d) = (0, 0.353 f, 0.235 f,0), che mostra il nuovo piano da descrivere con 0.353 y + 0.235 z = 0.</span><span class="sxs-lookup"><span data-stu-id="e2b0d-131">After scaling, the new plane contains (a,b,c,d) = (0, 0.353f, 0.235f, 0), which shows the new plane to be described by 0.353y + 0.235z = 0.</span></span>

<span data-ttu-id="e2b0d-132">Il parametro pM contiene la trasposta inversa della matrice di trasformazione.</span><span class="sxs-lookup"><span data-stu-id="e2b0d-132">The parameter pM contains the inverse transpose of the transformation matrix.</span></span> <span data-ttu-id="e2b0d-133">La trasposta inversa è richiesta da questo metodo, in modo che sia possibile trasformare correttamente anche il vettore normale del piano trasformato.</span><span class="sxs-lookup"><span data-stu-id="e2b0d-133">The inverse transpose is required by this method so that the normal vector of the transformed plane can be correctly transformed as well.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2b0d-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e2b0d-134">Requirements</span></span>



| <span data-ttu-id="e2b0d-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="e2b0d-135">Requirement</span></span> | <span data-ttu-id="e2b0d-136">Valore</span><span class="sxs-lookup"><span data-stu-id="e2b0d-136">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e2b0d-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e2b0d-137">Header</span></span><br/>  | <dl> <span data-ttu-id="e2b0d-138"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="e2b0d-138"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="e2b0d-139">Libreria</span><span class="sxs-lookup"><span data-stu-id="e2b0d-139">Library</span></span><br/> | <dl> <span data-ttu-id="e2b0d-140"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e2b0d-140"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e2b0d-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e2b0d-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2b0d-142">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="e2b0d-142">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="e2b0d-143">**D3DXPlaneNormalize**</span><span class="sxs-lookup"><span data-stu-id="e2b0d-143">**D3DXPlaneNormalize**</span></span>](d3dxplanenormalize.md)
</dt> <dt>

[<span data-ttu-id="e2b0d-144">**D3DXMatrixRotationX**</span><span class="sxs-lookup"><span data-stu-id="e2b0d-144">**D3DXMatrixRotationX**</span></span>](d3dxmatrixrotationx.md)
</dt> <dt>

[<span data-ttu-id="e2b0d-145">**D3DXMatrixRotationY**</span><span class="sxs-lookup"><span data-stu-id="e2b0d-145">**D3DXMatrixRotationY**</span></span>](d3dxmatrixrotationy.md)
</dt> <dt>

[<span data-ttu-id="e2b0d-146">**D3DXMatrixRotationZ**</span><span class="sxs-lookup"><span data-stu-id="e2b0d-146">**D3DXMatrixRotationZ**</span></span>](d3dxmatrixrotationz.md)
</dt> <dt>

[<span data-ttu-id="e2b0d-147">**D3DXMatrixInverse**</span><span class="sxs-lookup"><span data-stu-id="e2b0d-147">**D3DXMatrixInverse**</span></span>](d3dxmatrixinverse.md)
</dt> <dt>

[<span data-ttu-id="e2b0d-148">**D3DXMatrixTranspose**</span><span class="sxs-lookup"><span data-stu-id="e2b0d-148">**D3DXMatrixTranspose**</span></span>](d3dxmatrixtranspose.md)
</dt> </dl>

 

 




