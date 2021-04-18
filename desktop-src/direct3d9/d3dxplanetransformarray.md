---
description: Trasforma una matrice di piani in base a una matrice. È necessario normalizzare i vettori che descrivono ogni piano.
ms.assetid: e82e830b-efbb-4bdc-b370-7bfa4326a669
title: Funzione D3DXPlaneTransformArray (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a9a213b17aca9999ef0028fdceb4bb4321d47660
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322095"
---
# <a name="d3dxplanetransformarray-function-d3dx9mathh"></a><span data-ttu-id="26d13-104">Funzione D3DXPlaneTransformArray (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="26d13-104">D3DXPlaneTransformArray function (D3dx9math.h)</span></span>

<span data-ttu-id="26d13-105">Trasforma una matrice di piani in base a una matrice.</span><span class="sxs-lookup"><span data-stu-id="26d13-105">Transforms an array of planes by a matrix.</span></span> <span data-ttu-id="26d13-106">È necessario normalizzare i vettori che descrivono ogni piano.</span><span class="sxs-lookup"><span data-stu-id="26d13-106">The vectors that describe each plane must be normalized.</span></span>

## <a name="syntax"></a><span data-ttu-id="26d13-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="26d13-107">Syntax</span></span>


```C++
D3DXPLANE* D3DXPlaneTransformArray(
  _Inout_       D3DXPLANE  *pOut,
  _Out_         UINT       OutStride,
  _In_    const D3DXPLANE  *pP,
  _In_          UINT       PStride,
  _In_    const D3DXMATRIX *pM,
  _In_          UINT       n
);
```



## <a name="parameters"></a><span data-ttu-id="26d13-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="26d13-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26d13-109">*broncio* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="26d13-109">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="26d13-110">Tipo: **[ **D3DXPLANE**](d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="26d13-110">Type: **[**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="26d13-111">Puntatore alla struttura [**D3DXPLANE**](d3dxplane.md) che contiene il piano trasformato risultante.</span><span class="sxs-lookup"><span data-stu-id="26d13-111">Pointer to the [**D3DXPLANE**](d3dxplane.md) structure that contains the resulting transformed plane.</span></span> <span data-ttu-id="26d13-112">Vedere l'esempio.</span><span class="sxs-lookup"><span data-stu-id="26d13-112">See Example.</span></span>

</dd> <dt>

<span data-ttu-id="26d13-113">*Outstride* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="26d13-113">*OutStride* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="26d13-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="26d13-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="26d13-115">Stride di ogni piano trasformato.</span><span class="sxs-lookup"><span data-stu-id="26d13-115">The stride of each transformed plane.</span></span>

</dd> <dt>

<span data-ttu-id="26d13-116">*PP* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="26d13-116">*pP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26d13-117">Tipo: **const [**D3DXPLANE**](d3dxplane.md) \***</span><span class="sxs-lookup"><span data-stu-id="26d13-117">Type: **const [**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="26d13-118">Puntatore alla struttura di input [**D3DXPLANE**](d3dxplane.md) , che contiene la matrice di piani da trasformare.</span><span class="sxs-lookup"><span data-stu-id="26d13-118">Pointer to the input [**D3DXPLANE**](d3dxplane.md) structure, which contains the array of planes to transform.</span></span> <span data-ttu-id="26d13-119">Il vettore (a, b, c) che descrive il piano deve essere normalizzato prima che questa funzione venga chiamata.</span><span class="sxs-lookup"><span data-stu-id="26d13-119">The vector (a,b,c) that describes the plane must be normalized before this function is called.</span></span> <span data-ttu-id="26d13-120">Vedere l'esempio.</span><span class="sxs-lookup"><span data-stu-id="26d13-120">See Example.</span></span>

</dd> <dt>

<span data-ttu-id="26d13-121">*PStride* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="26d13-121">*PStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26d13-122">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="26d13-122">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="26d13-123">Stride di ogni piano non trasformato.</span><span class="sxs-lookup"><span data-stu-id="26d13-123">The stride of each non-transformed plane.</span></span>

</dd> <dt>

<span data-ttu-id="26d13-124">*PM* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="26d13-124">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26d13-125">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="26d13-125">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="26d13-126">Puntatore alla struttura [**D3DXMATRIX**](d3dxmatrix.md) di origine, che contiene la trasposta inversa dei valori della trasformazione.</span><span class="sxs-lookup"><span data-stu-id="26d13-126">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure, which contains the inverse transpose of the transformation values.</span></span>

</dd> <dt>

<span data-ttu-id="26d13-127">*n* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="26d13-127">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26d13-128">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="26d13-128">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="26d13-129">Numero di piani da trasformare.</span><span class="sxs-lookup"><span data-stu-id="26d13-129">The number of planes to transform.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26d13-130">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="26d13-130">Return value</span></span>

<span data-ttu-id="26d13-131">Tipo: **[ **D3DXPLANE**](d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="26d13-131">Type: **[**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="26d13-132">Puntatore a una struttura [**D3DXPLANE**](d3dxplane.md) che rappresenta il piano trasformato.</span><span class="sxs-lookup"><span data-stu-id="26d13-132">Pointer to a [**D3DXPLANE**](d3dxplane.md) structure, representing the transformed plane.</span></span> <span data-ttu-id="26d13-133">Si tratta dello stesso valore restituito nel parametro *broncio* , in modo che questa funzione possa essere utilizzata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="26d13-133">This is the same value returned in the *pOut* parameter so that this function can be used as a parameter for another function.</span></span>

## <a name="remarks"></a><span data-ttu-id="26d13-134">Commenti</span><span class="sxs-lookup"><span data-stu-id="26d13-134">Remarks</span></span>

<span data-ttu-id="26d13-135">Questo esempio trasforma un piano applicando una scala non uniforme.</span><span class="sxs-lookup"><span data-stu-id="26d13-135">This example transforms one plane by applying a non-uniform scale.</span></span>


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



<span data-ttu-id="26d13-136">Un piano è descritto da AX + + + CZ + DW = 0.</span><span class="sxs-lookup"><span data-stu-id="26d13-136">A plane is described by ax + by + cz + dw = 0.</span></span> <span data-ttu-id="26d13-137">Il primo piano viene creato con (a, b, c, d) = (0, 1, 1, 0), che è un piano descritto da y + z = 0.</span><span class="sxs-lookup"><span data-stu-id="26d13-137">The first plane is created with (a,b,c,d) = (0,1,1,0), which is a plane described by y + z = 0.</span></span> <span data-ttu-id="26d13-138">Dopo la scalabilità, il nuovo piano contiene (a, b, c, d) = (0, 0.353 f, 0.235 f,0), che mostra il nuovo piano da descrivere con 0.353 y + 0.235 z = 0.</span><span class="sxs-lookup"><span data-stu-id="26d13-138">After scaling, the new plane contains (a,b,c,d) = (0, 0.353f, 0.235f, 0), which shows the new plane to be described by 0.353y + 0.235z = 0.</span></span>

<span data-ttu-id="26d13-139">Il parametro *PM* contiene la trasposta inversa della matrice di trasformazione.</span><span class="sxs-lookup"><span data-stu-id="26d13-139">The parameter *pM* contains the inverse transpose of the transformation matrix.</span></span> <span data-ttu-id="26d13-140">La trasposta inversa è richiesta da questo metodo, in modo che sia possibile trasformare correttamente anche il vettore normale del piano trasformato.</span><span class="sxs-lookup"><span data-stu-id="26d13-140">The inverse transpose is required by this method so that the normal vector of the transformed plane can be correctly transformed as well.</span></span>

## <a name="requirements"></a><span data-ttu-id="26d13-141">Requisiti</span><span class="sxs-lookup"><span data-stu-id="26d13-141">Requirements</span></span>



| <span data-ttu-id="26d13-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="26d13-142">Requirement</span></span> | <span data-ttu-id="26d13-143">Valore</span><span class="sxs-lookup"><span data-stu-id="26d13-143">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="26d13-144">Intestazione</span><span class="sxs-lookup"><span data-stu-id="26d13-144">Header</span></span><br/>  | <dl> <span data-ttu-id="26d13-145"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="26d13-145"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="26d13-146">Libreria</span><span class="sxs-lookup"><span data-stu-id="26d13-146">Library</span></span><br/> | <dl> <span data-ttu-id="26d13-147"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="26d13-147"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="26d13-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="26d13-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26d13-149">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="26d13-149">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="26d13-150">**D3DXPlaneNormalize**</span><span class="sxs-lookup"><span data-stu-id="26d13-150">**D3DXPlaneNormalize**</span></span>](d3dxplanenormalize.md)
</dt> <dt>

[<span data-ttu-id="26d13-151">**D3DXMatrixRotationX**</span><span class="sxs-lookup"><span data-stu-id="26d13-151">**D3DXMatrixRotationX**</span></span>](d3dxmatrixrotationx.md)
</dt> <dt>

[<span data-ttu-id="26d13-152">**D3DXMatrixRotationY**</span><span class="sxs-lookup"><span data-stu-id="26d13-152">**D3DXMatrixRotationY**</span></span>](d3dxmatrixrotationy.md)
</dt> <dt>

[<span data-ttu-id="26d13-153">**D3DXMatrixRotationZ**</span><span class="sxs-lookup"><span data-stu-id="26d13-153">**D3DXMatrixRotationZ**</span></span>](d3dxmatrixrotationz.md)
</dt> <dt>

[<span data-ttu-id="26d13-154">**D3DXMatrixInverse**</span><span class="sxs-lookup"><span data-stu-id="26d13-154">**D3DXMatrixInverse**</span></span>](d3dxmatrixinverse.md)
</dt> <dt>

[<span data-ttu-id="26d13-155">**D3DXMatrixTranspose**</span><span class="sxs-lookup"><span data-stu-id="26d13-155">**D3DXMatrixTranspose**</span></span>](d3dxmatrixtranspose.md)
</dt> </dl>

 

 
