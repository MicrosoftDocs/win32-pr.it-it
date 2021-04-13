---
description: Trasforma un piano in base a una matrice. La matrice di input è la trasposta inversa della trasformazione effettiva.
ms.assetid: ded06eac-4086-47e8-bc55-c37959afc22d
title: Funzione D3DXPlaneTransform (D3DX10Math. h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 1b3c3390d84cd0d9c876afac6243ab90ca515e11
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355594"
---
# <a name="d3dxplanetransform-function-d3dx10mathh"></a><span data-ttu-id="d2ce5-104">Funzione D3DXPlaneTransform (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="d2ce5-104">D3DXPlaneTransform function (D3DX10Math.h)</span></span>

<span data-ttu-id="d2ce5-105">Trasforma un piano in base a una matrice.</span><span class="sxs-lookup"><span data-stu-id="d2ce5-105">Transforms a plane by a matrix.</span></span> <span data-ttu-id="d2ce5-106">La matrice di input è la trasposta inversa della trasformazione effettiva.</span><span class="sxs-lookup"><span data-stu-id="d2ce5-106">The input matrix is the inverse transpose of the actual transformation.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2ce5-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d2ce5-107">Syntax</span></span>


```C++
D3DXPLANE* D3DXPlaneTransform(
  _Inout_       D3DXPLANE  *pOut,
  _In_    const D3DXPLANE  *pP,
  _In_    const D3DXMATRIX *pM
);
```



## <a name="parameters"></a><span data-ttu-id="d2ce5-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="d2ce5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2ce5-109">*broncio* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="d2ce5-109">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d2ce5-110">Tipo: **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="d2ce5-110">Type: **[**D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span></span>

<span data-ttu-id="d2ce5-111">Puntatore a [**D3DXPLANE**](d3d10-d3dxplane.md) che contiene il piano trasformato risultante.</span><span class="sxs-lookup"><span data-stu-id="d2ce5-111">Pointer to the [**D3DXPLANE**](d3d10-d3dxplane.md) that contains the resulting transformed plane.</span></span> <span data-ttu-id="d2ce5-112">Vedere l'esempio.</span><span class="sxs-lookup"><span data-stu-id="d2ce5-112">See example.</span></span>

</dd> <dt>

<span data-ttu-id="d2ce5-113">*PP* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d2ce5-113">*pP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2ce5-114">Tipo: **const [**D3DXPLANE**](../direct3d9/d3dxplane.md) \***</span><span class="sxs-lookup"><span data-stu-id="d2ce5-114">Type: **const [**D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span></span>

<span data-ttu-id="d2ce5-115">Puntatore alla struttura di input D3DXPLANE, che contiene il piano che verrà trasformato.</span><span class="sxs-lookup"><span data-stu-id="d2ce5-115">Pointer to the input D3DXPLANE structure, which contains the plane that will be transformed.</span></span> <span data-ttu-id="d2ce5-116">Il vettore (a, b, c) che descrive il piano deve essere normalizzato prima che questa funzione venga chiamata.</span><span class="sxs-lookup"><span data-stu-id="d2ce5-116">The vector (a,b,c) that describes the plane must be normalized before this function is called.</span></span> <span data-ttu-id="d2ce5-117">Vedere l'esempio.</span><span class="sxs-lookup"><span data-stu-id="d2ce5-117">See example.</span></span>

</dd> <dt>

<span data-ttu-id="d2ce5-118">*PM* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d2ce5-118">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2ce5-119">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="d2ce5-119">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="d2ce5-120">Puntatore alla struttura [**D3DXMATRIX**](d3d10-d3dxmatrix.md) di origine, che contiene i valori della trasformazione.</span><span class="sxs-lookup"><span data-stu-id="d2ce5-120">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure, which contains the transformation values.</span></span> <span data-ttu-id="d2ce5-121">Questa matrice deve contenere la trasposta inversa dei valori della trasformazione.</span><span class="sxs-lookup"><span data-stu-id="d2ce5-121">This matrix must contain the inverse transpose of the transformation values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2ce5-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d2ce5-122">Return value</span></span>

<span data-ttu-id="d2ce5-123">Tipo: **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="d2ce5-123">Type: **[**D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span></span>

<span data-ttu-id="d2ce5-124">Puntatore a una struttura D3DXPLANE che rappresenta il piano trasformato.</span><span class="sxs-lookup"><span data-stu-id="d2ce5-124">Pointer to a D3DXPLANE structure, representing the transformed plane.</span></span> <span data-ttu-id="d2ce5-125">Si tratta dello stesso valore restituito nel parametro broncio, in modo che questa funzione possa essere utilizzata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="d2ce5-125">This is the same value returned in the pOut parameter so that this function can be used as a parameter for another function.</span></span>

## <a name="remarks"></a><span data-ttu-id="d2ce5-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="d2ce5-126">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="d2ce5-127">Esempi</span><span class="sxs-lookup"><span data-stu-id="d2ce5-127">Examples</span></span>

<span data-ttu-id="d2ce5-128">Questo esempio trasforma un piano applicando una scala non uniforme.</span><span class="sxs-lookup"><span data-stu-id="d2ce5-128">This example transforms a plane by applying a non-uniform scale.</span></span>


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



<span data-ttu-id="d2ce5-129">Un piano è descritto da AX + + + CZ + DW = 0.</span><span class="sxs-lookup"><span data-stu-id="d2ce5-129">A plane is described by ax + by + cz + dw = 0.</span></span> <span data-ttu-id="d2ce5-130">Il primo piano viene creato con (a, b, c, d) = (0, 1, 1, 0), che è un piano descritto da y + z = 0.</span><span class="sxs-lookup"><span data-stu-id="d2ce5-130">The first plane is created with (a,b,c,d) = (0,1,1,0), which is a plane described by y + z = 0.</span></span> <span data-ttu-id="d2ce5-131">Dopo la scalabilità, il nuovo piano contiene (a, b, c, d) = (0, 0.353 f, 0.235 f,0), che mostra il nuovo piano da descrivere con 0.353 y + 0.235 z = 0.</span><span class="sxs-lookup"><span data-stu-id="d2ce5-131">After scaling, the new plane contains (a,b,c,d) = (0, 0.353f, 0.235f, 0), which shows the new plane to be described by 0.353y + 0.235z = 0.</span></span>

<span data-ttu-id="d2ce5-132">Il parametro pM contiene la trasposta inversa della matrice di trasformazione.</span><span class="sxs-lookup"><span data-stu-id="d2ce5-132">The parameter pM contains the inverse transpose of the transformation matrix.</span></span> <span data-ttu-id="d2ce5-133">La trasposta inversa è richiesta da questo metodo, in modo che sia possibile trasformare correttamente anche il vettore normale del piano trasformato.</span><span class="sxs-lookup"><span data-stu-id="d2ce5-133">The inverse transpose is required by this method so that the normal vector of the transformed plane can be correctly transformed as well.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2ce5-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d2ce5-134">Requirements</span></span>



| <span data-ttu-id="d2ce5-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="d2ce5-135">Requirement</span></span> | <span data-ttu-id="d2ce5-136">Valore</span><span class="sxs-lookup"><span data-stu-id="d2ce5-136">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d2ce5-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d2ce5-137">Header</span></span><br/>  | <dl> <span data-ttu-id="d2ce5-138"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="d2ce5-138"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="d2ce5-139">Libreria</span><span class="sxs-lookup"><span data-stu-id="d2ce5-139">Library</span></span><br/> | <dl> <span data-ttu-id="d2ce5-140"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d2ce5-140"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d2ce5-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d2ce5-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2ce5-142">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="d2ce5-142">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
