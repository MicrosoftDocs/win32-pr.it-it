---
description: 'Funzione D3DXPlaneTransformArray (D3DX10Math.h): trasforma una matrice di piani in base a una matrice. I vettori che descrivono ogni piano devono essere normalizzati.'
ms.assetid: 9529b06a-0575-4115-8d35-fc35a7bfb0bd
title: Funzione D3DXPlaneTransformArray (D3DX10Math.h)
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
ms.openlocfilehash: d8b02b64fd13e7466980340056fceccc1da784cf
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103259"
---
# <a name="d3dxplanetransformarray-function-d3dx10mathh"></a><span data-ttu-id="c89a1-104">Funzione D3DXPlaneTransformArray (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="c89a1-104">D3DXPlaneTransformArray function (D3DX10Math.h)</span></span>

<span data-ttu-id="c89a1-105">Trasforma una matrice di piani in base a una matrice.</span><span class="sxs-lookup"><span data-stu-id="c89a1-105">Transforms an array of planes by a matrix.</span></span> <span data-ttu-id="c89a1-106">I vettori che descrivono ogni piano devono essere normalizzati.</span><span class="sxs-lookup"><span data-stu-id="c89a1-106">The vectors that describe each plane must be normalized.</span></span>

## <a name="syntax"></a><span data-ttu-id="c89a1-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c89a1-107">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="c89a1-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="c89a1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c89a1-109">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="c89a1-109">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c89a1-110">Tipo: **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="c89a1-110">Type: **[**D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span></span>

<span data-ttu-id="c89a1-111">Puntatore alla [**struttura D3DXPLANE**](d3d10-d3dxplane.md) che contiene il piano trasformato risultante.</span><span class="sxs-lookup"><span data-stu-id="c89a1-111">Pointer to the [**D3DXPLANE**](d3d10-d3dxplane.md) structure that contains the resulting transformed plane.</span></span> <span data-ttu-id="c89a1-112">Vedere Esempio.</span><span class="sxs-lookup"><span data-stu-id="c89a1-112">See Example.</span></span>

</dd> <dt>

<span data-ttu-id="c89a1-113">*OutStride* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="c89a1-113">*OutStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c89a1-114">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c89a1-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c89a1-115">Passo di ogni piano trasformato.</span><span class="sxs-lookup"><span data-stu-id="c89a1-115">The stride of each transformed plane.</span></span>

</dd> <dt>

<span data-ttu-id="c89a1-116">*pP* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="c89a1-116">*pP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c89a1-117">Tipo: **const [**D3DXPLANE**](../direct3d9/d3dxplane.md) \***</span><span class="sxs-lookup"><span data-stu-id="c89a1-117">Type: **const [**D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span></span>

<span data-ttu-id="c89a1-118">Puntatore alla struttura D3DXPLANE di input, che contiene la matrice di piani da trasformare.</span><span class="sxs-lookup"><span data-stu-id="c89a1-118">Pointer to the input D3DXPLANE structure, which contains the array of planes to transform.</span></span> <span data-ttu-id="c89a1-119">Il vettore (a, b, c) che descrive il piano deve essere normalizzato prima che venga chiamata questa funzione.</span><span class="sxs-lookup"><span data-stu-id="c89a1-119">The vector (a, b, c) that describes the plane must be normalized before this function is called.</span></span> <span data-ttu-id="c89a1-120">Vedere Esempio.</span><span class="sxs-lookup"><span data-stu-id="c89a1-120">See Example.</span></span>

</dd> <dt>

<span data-ttu-id="c89a1-121">*PStride* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="c89a1-121">*PStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c89a1-122">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c89a1-122">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c89a1-123">Stride di ogni piano non trasformato.</span><span class="sxs-lookup"><span data-stu-id="c89a1-123">The stride of each non-transformed plane.</span></span>

</dd> <dt>

<span data-ttu-id="c89a1-124">*pM* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="c89a1-124">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c89a1-125">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="c89a1-125">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="c89a1-126">Puntatore alla struttura [**D3DXMATRIX**](d3d10-d3dxmatrix.md) di origine, che contiene il traspose inverso dei valori della trasformazione.</span><span class="sxs-lookup"><span data-stu-id="c89a1-126">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure, which contains the inverse transpose of the transformation values.</span></span>

</dd> <dt>

<span data-ttu-id="c89a1-127">*n* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c89a1-127">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c89a1-128">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c89a1-128">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c89a1-129">Numero di piani da trasformare.</span><span class="sxs-lookup"><span data-stu-id="c89a1-129">The number of planes to transform.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c89a1-130">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c89a1-130">Return value</span></span>

<span data-ttu-id="c89a1-131">Tipo: **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="c89a1-131">Type: **[**D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span></span>

<span data-ttu-id="c89a1-132">Puntatore a una struttura D3DXPLANE, che rappresenta il piano trasformato.</span><span class="sxs-lookup"><span data-stu-id="c89a1-132">Pointer to a D3DXPLANE structure, representing the transformed plane.</span></span> <span data-ttu-id="c89a1-133">Si tratta dello stesso valore restituito nel parametro pOut in modo che questa funzione possa essere usata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="c89a1-133">This is the same value returned in the pOut parameter so that this function can be used as a parameter for another function.</span></span>

## <a name="remarks"></a><span data-ttu-id="c89a1-134">Commenti</span><span class="sxs-lookup"><span data-stu-id="c89a1-134">Remarks</span></span>

<span data-ttu-id="c89a1-135">Questo esempio trasforma un piano applicando una scala non uniforme.</span><span class="sxs-lookup"><span data-stu-id="c89a1-135">This example transforms one plane by applying a non-uniform scale.</span></span>


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



<span data-ttu-id="c89a1-136">Un piano è descritto da ax + by + cz + dw = 0.</span><span class="sxs-lookup"><span data-stu-id="c89a1-136">A plane is described by ax + by + cz + dw = 0.</span></span> <span data-ttu-id="c89a1-137">Il primo piano viene creato con (a,b,c,d) = (0,1,1,0), ovvero un piano descritto da y + z = 0.</span><span class="sxs-lookup"><span data-stu-id="c89a1-137">The first plane is created with (a,b,c,d) = (0,1,1,0), which is a plane described by y + z = 0.</span></span> <span data-ttu-id="c89a1-138">Dopo il ridimensionamento, il nuovo piano contiene (a,b,c,d) = (0, 0,353f, 0,235f, 0), che mostra il nuovo piano descritto da 0,353y + 0,235z = 0.</span><span class="sxs-lookup"><span data-stu-id="c89a1-138">After scaling, the new plane contains (a,b,c,d) = (0, 0.353f, 0.235f, 0), which shows the new plane to be described by 0.353y + 0.235z = 0.</span></span>

<span data-ttu-id="c89a1-139">Il parametro pM contiene il traspose inverso della matrice di trasformazione.</span><span class="sxs-lookup"><span data-stu-id="c89a1-139">The parameter pM, contains the inverse transpose of the transformation matrix.</span></span> <span data-ttu-id="c89a1-140">La trasposizione inversa è richiesta da questo metodo in modo che anche il vettore normale del piano trasformato possa essere trasformato correttamente.</span><span class="sxs-lookup"><span data-stu-id="c89a1-140">The inverse transpose is required by this method so that the normal vector of the transformed plane can be correctly transformed as well.</span></span>

## <a name="requirements"></a><span data-ttu-id="c89a1-141">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c89a1-141">Requirements</span></span>



| <span data-ttu-id="c89a1-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="c89a1-142">Requirement</span></span> | <span data-ttu-id="c89a1-143">Valore</span><span class="sxs-lookup"><span data-stu-id="c89a1-143">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c89a1-144">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c89a1-144">Header</span></span><br/>  | <dl> <span data-ttu-id="c89a1-145"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="c89a1-145"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="c89a1-146">Libreria</span><span class="sxs-lookup"><span data-stu-id="c89a1-146">Library</span></span><br/> | <dl> <span data-ttu-id="c89a1-147"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="c89a1-147"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c89a1-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c89a1-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c89a1-149">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="c89a1-149">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
