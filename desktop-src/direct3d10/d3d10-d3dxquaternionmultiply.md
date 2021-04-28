---
description: 'Funzione D3DXQuaternionMultiply (D3DX10Math.h): moltiplica due quaternioni.'
ms.assetid: f549e383-9c39-47a9-84e4-82365bdf1155
title: Funzione D3DXQuaternionMultiply (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionMultiply
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 4f84ecac1eb910f4b3c97aba6ed42691c70b5b1f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103159"
---
# <a name="d3dxquaternionmultiply-function-d3dx10mathh"></a><span data-ttu-id="2e8dd-103">Funzione D3DXQuaternionMultiply (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="2e8dd-103">D3DXQuaternionMultiply function (D3DX10Math.h)</span></span>

<span data-ttu-id="2e8dd-104">Moltiplica due quaternioni.</span><span class="sxs-lookup"><span data-stu-id="2e8dd-104">Multiplies two quaternions.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e8dd-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2e8dd-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionMultiply(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ1,
  _In_    const D3DXQUATERNION *pQ2
);
```



## <a name="parameters"></a><span data-ttu-id="2e8dd-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="2e8dd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e8dd-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="2e8dd-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="2e8dd-108">Tipo: **[ **D3DXQUATERNION**](d3d10-d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="2e8dd-108">Type: **[**D3DXQUATERNION**](d3d10-d3dxquaternion.md)\***</span></span>

<span data-ttu-id="2e8dd-109">Puntatore [**all'oggetto D3DXQUATERNION**](d3d10-d3dxquaternion.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="2e8dd-109">Pointer to the [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="2e8dd-110">*pQ1* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="2e8dd-110">*pQ1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e8dd-111">Tipo: **const [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="2e8dd-111">Type: **const [**D3DXQUATERNION**](d3d10-d3dxquaternion.md)\***</span></span>

<span data-ttu-id="2e8dd-112">Puntatore a una [**struttura D3DXQUATERNION di**](d3d10-d3dxquaternion.md) origine.</span><span class="sxs-lookup"><span data-stu-id="2e8dd-112">Pointer to a source [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="2e8dd-113">*pQ2* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="2e8dd-113">*pQ2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e8dd-114">Tipo: **const [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="2e8dd-114">Type: **const [**D3DXQUATERNION**](d3d10-d3dxquaternion.md)\***</span></span>

<span data-ttu-id="2e8dd-115">Puntatore a una [**struttura D3DXQUATERNION di**](d3d10-d3dxquaternion.md) origine.</span><span class="sxs-lookup"><span data-stu-id="2e8dd-115">Pointer to a source [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e8dd-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2e8dd-116">Return value</span></span>

<span data-ttu-id="2e8dd-117">Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="2e8dd-117">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="2e8dd-118">Puntatore a [**una struttura D3DXQUATERNION**](d3d10-d3dxquaternion.md) che è il prodotto di due quaternioni.</span><span class="sxs-lookup"><span data-stu-id="2e8dd-118">Pointer to a [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) structure that is the product of two quaternions.</span></span>

## <a name="remarks"></a><span data-ttu-id="2e8dd-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="2e8dd-119">Remarks</span></span>

<span data-ttu-id="2e8dd-120">Il risultato rappresenta la rotazione Q1 seguita dalla rotazione Q2 (Out = Q2 \* Q1).</span><span class="sxs-lookup"><span data-stu-id="2e8dd-120">The result represents the rotation Q1 followed by the rotation Q2 (Out = Q2 \* Q1).</span></span> <span data-ttu-id="2e8dd-121">Questa operazione viene eseguita in modo che **D3DXQuaternionMultiply** mantenga la stessa semantica di [**D3DXMatrixMultiply**](d3d10-d3dxmatrixmultiply.md) perché i quaternioni unità possono essere considerati come un altro modo per rappresentare le matrici di rotazione.</span><span class="sxs-lookup"><span data-stu-id="2e8dd-121">This is done so that **D3DXQuaternionMultiply** maintain the same semantics as [**D3DXMatrixMultiply**](d3d10-d3dxmatrixmultiply.md) because unit quaternions can be considered as another way to represent rotation matrices.</span></span>

<span data-ttu-id="2e8dd-122">Le trasformazioni vengono concatenate nello stesso ordine per le funzioni **D3DXQuaternionMultiply** e [**D3DXMatrixMultiply.**](d3d10-d3dxmatrixmultiply.md)</span><span class="sxs-lookup"><span data-stu-id="2e8dd-122">Transformations are concatenated in the same order for both the **D3DXQuaternionMultiply** and [**D3DXMatrixMultiply**](d3d10-d3dxmatrixmultiply.md) Functions.</span></span> <span data-ttu-id="2e8dd-123">Ad esempio, supponendo che mX e mY rappresentino le stesse rotazioni di qX e qY, sia m che q rappresenteranno le stesse rotazioni.</span><span class="sxs-lookup"><span data-stu-id="2e8dd-123">For example, assuming mX and mY represent the same rotations as qX and qY, both m and q will represent the same rotations.</span></span>


```
D3DXMatrixMultiply(&m, &mX, &mY);
D3DXQuaternionMultiply(&q, &qX, &qY);
```



<span data-ttu-id="2e8dd-124">La moltiplicazione dei quaternioni non è commutativa.</span><span class="sxs-lookup"><span data-stu-id="2e8dd-124">The multiplication of quaternions is not commutative.</span></span>

<span data-ttu-id="2e8dd-125">Il valore restituito per questa funzione è lo stesso valore restituito nel parametro pOut.</span><span class="sxs-lookup"><span data-stu-id="2e8dd-125">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="2e8dd-126">In questo modo, la **funzione D3DXQuaternionMultiply** può essere usata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="2e8dd-126">In this way, the **D3DXQuaternionMultiply** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="2e8dd-127">Usare [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) per qualsiasi input quaternione non ancora normalizzato.</span><span class="sxs-lookup"><span data-stu-id="2e8dd-127">Use [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e8dd-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2e8dd-128">Requirements</span></span>



| <span data-ttu-id="2e8dd-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e8dd-129">Requirement</span></span> | <span data-ttu-id="2e8dd-130">Valore</span><span class="sxs-lookup"><span data-stu-id="2e8dd-130">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2e8dd-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2e8dd-131">Header</span></span><br/>  | <dl> <span data-ttu-id="2e8dd-132"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="2e8dd-132"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="2e8dd-133">Libreria</span><span class="sxs-lookup"><span data-stu-id="2e8dd-133">Library</span></span><br/> | <dl> <span data-ttu-id="2e8dd-134"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="2e8dd-134"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2e8dd-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2e8dd-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e8dd-136">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="2e8dd-136">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
