---
description: 'Funzione D3DXPlaneTransform (D3DX10Math.h): trasforma un piano in base a una matrice. La matrice di input è il trasposto inverso della trasformazione effettiva.'
ms.assetid: ded06eac-4086-47e8-bc55-c37959afc22d
title: Funzione D3DXPlaneTransform (D3DX10Math.h)
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
ms.openlocfilehash: 9b1d16ba2a29d42614c388a6207503ad32dd5e0f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108789"
---
# <a name="d3dxplanetransform-function-d3dx10mathh"></a><span data-ttu-id="4cfa0-104">Funzione D3DXPlaneTransform (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="4cfa0-104">D3DXPlaneTransform function (D3DX10Math.h)</span></span>

<span data-ttu-id="4cfa0-105">Trasforma un piano in base a una matrice.</span><span class="sxs-lookup"><span data-stu-id="4cfa0-105">Transforms a plane by a matrix.</span></span> <span data-ttu-id="4cfa0-106">La matrice di input è il trasposto inverso della trasformazione effettiva.</span><span class="sxs-lookup"><span data-stu-id="4cfa0-106">The input matrix is the inverse transpose of the actual transformation.</span></span>

## <a name="syntax"></a><span data-ttu-id="4cfa0-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4cfa0-107">Syntax</span></span>


```C++
D3DXPLANE* D3DXPlaneTransform(
  _Inout_       D3DXPLANE  *pOut,
  _In_    const D3DXPLANE  *pP,
  _In_    const D3DXMATRIX *pM
);
```



## <a name="parameters"></a><span data-ttu-id="4cfa0-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="4cfa0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4cfa0-109">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="4cfa0-109">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="4cfa0-110">Tipo: **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="4cfa0-110">Type: **[**D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span></span>

<span data-ttu-id="4cfa0-111">Puntatore [**all'oggetto D3DXPLANE**](d3d10-d3dxplane.md) che contiene il piano trasformato risultante.</span><span class="sxs-lookup"><span data-stu-id="4cfa0-111">Pointer to the [**D3DXPLANE**](d3d10-d3dxplane.md) that contains the resulting transformed plane.</span></span> <span data-ttu-id="4cfa0-112">Vedere l'esempio.</span><span class="sxs-lookup"><span data-stu-id="4cfa0-112">See example.</span></span>

</dd> <dt>

<span data-ttu-id="4cfa0-113">*pP* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="4cfa0-113">*pP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4cfa0-114">Tipo: **const [**D3DXPLANE**](../direct3d9/d3dxplane.md) \***</span><span class="sxs-lookup"><span data-stu-id="4cfa0-114">Type: **const [**D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span></span>

<span data-ttu-id="4cfa0-115">Puntatore alla struttura D3DXPLANE di input che contiene il piano che verrà trasformato.</span><span class="sxs-lookup"><span data-stu-id="4cfa0-115">Pointer to the input D3DXPLANE structure, which contains the plane that will be transformed.</span></span> <span data-ttu-id="4cfa0-116">Il vettore (a,b,c) che descrive il piano deve essere normalizzato prima che venga chiamata questa funzione.</span><span class="sxs-lookup"><span data-stu-id="4cfa0-116">The vector (a,b,c) that describes the plane must be normalized before this function is called.</span></span> <span data-ttu-id="4cfa0-117">Vedere l'esempio.</span><span class="sxs-lookup"><span data-stu-id="4cfa0-117">See example.</span></span>

</dd> <dt>

<span data-ttu-id="4cfa0-118">*pM* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="4cfa0-118">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4cfa0-119">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="4cfa0-119">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="4cfa0-120">Puntatore alla struttura [**D3DXMATRIX di**](d3d10-d3dxmatrix.md) origine, che contiene i valori di trasformazione.</span><span class="sxs-lookup"><span data-stu-id="4cfa0-120">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure, which contains the transformation values.</span></span> <span data-ttu-id="4cfa0-121">Questa matrice deve contenere il traspose inverso dei valori di trasformazione.</span><span class="sxs-lookup"><span data-stu-id="4cfa0-121">This matrix must contain the inverse transpose of the transformation values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4cfa0-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4cfa0-122">Return value</span></span>

<span data-ttu-id="4cfa0-123">Tipo: **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="4cfa0-123">Type: **[**D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span></span>

<span data-ttu-id="4cfa0-124">Puntatore a una struttura D3DXPLANE che rappresenta il piano trasformato.</span><span class="sxs-lookup"><span data-stu-id="4cfa0-124">Pointer to a D3DXPLANE structure, representing the transformed plane.</span></span> <span data-ttu-id="4cfa0-125">Si tratta dello stesso valore restituito nel parametro pOut in modo che questa funzione possa essere usata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="4cfa0-125">This is the same value returned in the pOut parameter so that this function can be used as a parameter for another function.</span></span>

## <a name="remarks"></a><span data-ttu-id="4cfa0-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="4cfa0-126">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="4cfa0-127">Esempi</span><span class="sxs-lookup"><span data-stu-id="4cfa0-127">Examples</span></span>

<span data-ttu-id="4cfa0-128">Questo esempio trasforma un piano applicando una scala non uniforme.</span><span class="sxs-lookup"><span data-stu-id="4cfa0-128">This example transforms a plane by applying a non-uniform scale.</span></span>


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



<span data-ttu-id="4cfa0-129">Un piano è descritto da ax + by + cz + dw = 0.</span><span class="sxs-lookup"><span data-stu-id="4cfa0-129">A plane is described by ax + by + cz + dw = 0.</span></span> <span data-ttu-id="4cfa0-130">Il primo piano viene creato con (a,b,c,d) = (0,1,1,0), ovvero un piano descritto da y + z = 0.</span><span class="sxs-lookup"><span data-stu-id="4cfa0-130">The first plane is created with (a,b,c,d) = (0,1,1,0), which is a plane described by y + z = 0.</span></span> <span data-ttu-id="4cfa0-131">Dopo il ridimensionamento, il nuovo piano contiene (a,b,c,d) = (0, 0,353f, 0,235f, 0), che mostra il nuovo piano descritto da 0,353y + 0,235z = 0.</span><span class="sxs-lookup"><span data-stu-id="4cfa0-131">After scaling, the new plane contains (a,b,c,d) = (0, 0.353f, 0.235f, 0), which shows the new plane to be described by 0.353y + 0.235z = 0.</span></span>

<span data-ttu-id="4cfa0-132">Il parametro pM contiene la trasposizione inversa della matrice di trasformazione.</span><span class="sxs-lookup"><span data-stu-id="4cfa0-132">The parameter pM contains the inverse transpose of the transformation matrix.</span></span> <span data-ttu-id="4cfa0-133">La trasposizione inversa è richiesta da questo metodo in modo che anche il vettore normale del piano trasformato possa essere trasformato correttamente.</span><span class="sxs-lookup"><span data-stu-id="4cfa0-133">The inverse transpose is required by this method so that the normal vector of the transformed plane can be correctly transformed as well.</span></span>

## <a name="requirements"></a><span data-ttu-id="4cfa0-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4cfa0-134">Requirements</span></span>



| <span data-ttu-id="4cfa0-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="4cfa0-135">Requirement</span></span> | <span data-ttu-id="4cfa0-136">Valore</span><span class="sxs-lookup"><span data-stu-id="4cfa0-136">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4cfa0-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4cfa0-137">Header</span></span><br/>  | <dl> <span data-ttu-id="4cfa0-138"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="4cfa0-138"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="4cfa0-139">Libreria</span><span class="sxs-lookup"><span data-stu-id="4cfa0-139">Library</span></span><br/> | <dl> <span data-ttu-id="4cfa0-140"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="4cfa0-140"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="4cfa0-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4cfa0-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4cfa0-142">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="4cfa0-142">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
