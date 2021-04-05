---
description: Trasforma una matrice di piani in base a una matrice. È necessario normalizzare i vettori che descrivono ogni piano.
ms.assetid: 9529b06a-0575-4115-8d35-fc35a7bfb0bd
title: Funzione D3DXPlaneTransformArray (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneTransformArray
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 128b9c8c73db81faa877295e993504a7a510cd4a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104058646"
---
# <a name="d3dxplanetransformarray-function-d3dx10mathh"></a><span data-ttu-id="7c605-104">Funzione D3DXPlaneTransformArray (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="7c605-104">D3DXPlaneTransformArray function (D3DX10Math.h)</span></span>

<span data-ttu-id="7c605-105">Trasforma una matrice di piani in base a una matrice.</span><span class="sxs-lookup"><span data-stu-id="7c605-105">Transforms an array of planes by a matrix.</span></span> <span data-ttu-id="7c605-106">È necessario normalizzare i vettori che descrivono ogni piano.</span><span class="sxs-lookup"><span data-stu-id="7c605-106">The vectors that describe each plane must be normalized.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c605-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7c605-107">Syntax</span></span>


```C++
D3DXPLANE* D3DXPlaneTransformArray(
  _Inout_       D3DXPLANE  *pOut,
  _In_          UINT       OutStride,
  _In_    const D3DXPLANE  *pP,
  _In_          UINT       PStride,
  _In_    const D3DXMATRIX *pM,
  _In_          UINT       n
);
```



## <a name="parameters"></a><span data-ttu-id="7c605-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="7c605-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c605-109">*broncio* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="7c605-109">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="7c605-110">Tipo: **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="7c605-110">Type: **[**D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span></span>

<span data-ttu-id="7c605-111">Puntatore alla struttura [**D3DXPLANE**](d3d10-d3dxplane.md) che contiene il piano trasformato risultante.</span><span class="sxs-lookup"><span data-stu-id="7c605-111">Pointer to the [**D3DXPLANE**](d3d10-d3dxplane.md) structure that contains the resulting transformed plane.</span></span> <span data-ttu-id="7c605-112">Vedere l'esempio.</span><span class="sxs-lookup"><span data-stu-id="7c605-112">See Example.</span></span>

</dd> <dt>

<span data-ttu-id="7c605-113">*Outstride* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7c605-113">*OutStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c605-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7c605-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7c605-115">Stride di ogni piano trasformato.</span><span class="sxs-lookup"><span data-stu-id="7c605-115">The stride of each transformed plane.</span></span>

</dd> <dt>

<span data-ttu-id="7c605-116">*PP* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7c605-116">*pP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c605-117">Tipo: **const [**D3DXPLANE**](../direct3d9/d3dxplane.md) \***</span><span class="sxs-lookup"><span data-stu-id="7c605-117">Type: **const [**D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span></span>

<span data-ttu-id="7c605-118">Puntatore alla struttura di input D3DXPLANE, che contiene la matrice di piani da trasformare.</span><span class="sxs-lookup"><span data-stu-id="7c605-118">Pointer to the input D3DXPLANE structure, which contains the array of planes to transform.</span></span> <span data-ttu-id="7c605-119">Il vettore (a, b, c) che descrive il piano deve essere normalizzato prima che questa funzione venga chiamata.</span><span class="sxs-lookup"><span data-stu-id="7c605-119">The vector (a, b, c) that describes the plane must be normalized before this function is called.</span></span> <span data-ttu-id="7c605-120">Vedere l'esempio.</span><span class="sxs-lookup"><span data-stu-id="7c605-120">See Example.</span></span>

</dd> <dt>

<span data-ttu-id="7c605-121">*PStride* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7c605-121">*PStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c605-122">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7c605-122">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7c605-123">Stride di ogni piano non trasformato.</span><span class="sxs-lookup"><span data-stu-id="7c605-123">The stride of each non-transformed plane.</span></span>

</dd> <dt>

<span data-ttu-id="7c605-124">*PM* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7c605-124">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c605-125">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="7c605-125">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="7c605-126">Puntatore alla struttura [**D3DXMATRIX**](d3d10-d3dxmatrix.md) di origine, che contiene la trasposta inversa dei valori della trasformazione.</span><span class="sxs-lookup"><span data-stu-id="7c605-126">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure, which contains the inverse transpose of the transformation values.</span></span>

</dd> <dt>

<span data-ttu-id="7c605-127">*n* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7c605-127">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c605-128">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7c605-128">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7c605-129">Numero di piani da trasformare.</span><span class="sxs-lookup"><span data-stu-id="7c605-129">The number of planes to transform.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c605-130">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7c605-130">Return value</span></span>

<span data-ttu-id="7c605-131">Tipo: **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="7c605-131">Type: **[**D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span></span>

<span data-ttu-id="7c605-132">Puntatore a una struttura D3DXPLANE che rappresenta il piano trasformato.</span><span class="sxs-lookup"><span data-stu-id="7c605-132">Pointer to a D3DXPLANE structure, representing the transformed plane.</span></span> <span data-ttu-id="7c605-133">Si tratta dello stesso valore restituito nel parametro broncio, in modo che questa funzione possa essere utilizzata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="7c605-133">This is the same value returned in the pOut parameter so that this function can be used as a parameter for another function.</span></span>

## <a name="remarks"></a><span data-ttu-id="7c605-134">Commenti</span><span class="sxs-lookup"><span data-stu-id="7c605-134">Remarks</span></span>

<span data-ttu-id="7c605-135">Questo esempio trasforma un piano applicando una scala non uniforme.</span><span class="sxs-lookup"><span data-stu-id="7c605-135">This example transforms one plane by applying a non-uniform scale.</span></span>


```
#define ARRAYSIZE 4
D3DXPLANE planeNew[ARRAYSIZE];
D3DXPLANE plane[ARRAYSIZE];

for(int i = 0; i < ARRAYSIZE; i++)
{
    plane = D3DXPLANE( 0.0f, 1.0f, 1.0f, 0.0f );
    D3DXPlaneNormalize( &plane[i], &plane[i] );
}

D3DXMATRIX  matrix;
D3DXMatrixScaling( &matrix, 1.0f, 2.0f, 3.0f ); 
D3DXMatrixInverse( &matrix, NULL, &matrix );
D3DXMatrixTranspose( &matrix, &matrix );
D3DXPlaneTransformArray( &planeNew, sizeof (D3DXPLANE), &plane, 
                         sizeof (D3DXPLANE), &matrix, ARRAYSIZE );
```



<span data-ttu-id="7c605-136">Un piano è descritto da AX + + + CZ + DW = 0.</span><span class="sxs-lookup"><span data-stu-id="7c605-136">A plane is described by ax + by + cz + dw = 0.</span></span> <span data-ttu-id="7c605-137">Il primo piano viene creato con (a, b, c, d) = (0, 1, 1, 0), che è un piano descritto da y + z = 0.</span><span class="sxs-lookup"><span data-stu-id="7c605-137">The first plane is created with (a,b,c,d) = (0,1,1,0), which is a plane described by y + z = 0.</span></span> <span data-ttu-id="7c605-138">Dopo la scalabilità, il nuovo piano contiene (a, b, c, d) = (0, 0.353 f, 0.235 f,0), che mostra il nuovo piano da descrivere con 0.353 y + 0.235 z = 0.</span><span class="sxs-lookup"><span data-stu-id="7c605-138">After scaling, the new plane contains (a,b,c,d) = (0, 0.353f, 0.235f, 0), which shows the new plane to be described by 0.353y + 0.235z = 0.</span></span>

<span data-ttu-id="7c605-139">Il parametro pM contiene la trasformazione inversa della matrice di trasformazione.</span><span class="sxs-lookup"><span data-stu-id="7c605-139">The parameter pM, contains the inverse transpose of the transformation matrix.</span></span> <span data-ttu-id="7c605-140">La trasposta inversa è richiesta da questo metodo, in modo che sia possibile trasformare correttamente anche il vettore normale del piano trasformato.</span><span class="sxs-lookup"><span data-stu-id="7c605-140">The inverse transpose is required by this method so that the normal vector of the transformed plane can be correctly transformed as well.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c605-141">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7c605-141">Requirements</span></span>



| <span data-ttu-id="7c605-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="7c605-142">Requirement</span></span> | <span data-ttu-id="7c605-143">Valore</span><span class="sxs-lookup"><span data-stu-id="7c605-143">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7c605-144">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7c605-144">Header</span></span><br/>  | <dl> <span data-ttu-id="7c605-145"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="7c605-145"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="7c605-146">Libreria</span><span class="sxs-lookup"><span data-stu-id="7c605-146">Library</span></span><br/> | <dl> <span data-ttu-id="7c605-147"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7c605-147"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="7c605-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7c605-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c605-149">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="7c605-149">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
