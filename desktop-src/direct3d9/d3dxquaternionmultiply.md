---
description: 'Funzione D3DXQuaternionMultiply (D3dx9math.h): moltiplica due quaternioni.'
ms.assetid: 11072fc9-dae8-4f63-b07d-b709eed381df
title: Funzione D3DXQuaternionMultiply (D3dx9math.h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7250484e4943e8b077a63e35951c17a44eaf2de3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118039"
---
# <a name="d3dxquaternionmultiply-function-d3dx9mathh"></a><span data-ttu-id="352a1-103">Funzione D3DXQuaternionMultiply (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="352a1-103">D3DXQuaternionMultiply function (D3dx9math.h)</span></span>

<span data-ttu-id="352a1-104">Moltiplica due quaternioni.</span><span class="sxs-lookup"><span data-stu-id="352a1-104">Multiplies two quaternions.</span></span>

## <a name="syntax"></a><span data-ttu-id="352a1-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="352a1-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionMultiply(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ1,
  _In_    const D3DXQUATERNION *pQ2
);
```



## <a name="parameters"></a><span data-ttu-id="352a1-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="352a1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="352a1-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="352a1-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="352a1-108">Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="352a1-108">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="352a1-109">Puntatore alla [**struttura D3DXQUATERNION**](d3dxquaternion.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="352a1-109">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="352a1-110">*pQ1* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="352a1-110">*pQ1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="352a1-111">Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="352a1-111">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="352a1-112">Puntatore a una [**struttura D3DXQUATERNION di**](d3dxquaternion.md) origine.</span><span class="sxs-lookup"><span data-stu-id="352a1-112">Pointer to a source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="352a1-113">*pQ2* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="352a1-113">*pQ2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="352a1-114">Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="352a1-114">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="352a1-115">Puntatore a una [**struttura D3DXQUATERNION di**](d3dxquaternion.md) origine.</span><span class="sxs-lookup"><span data-stu-id="352a1-115">Pointer to a source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="352a1-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="352a1-116">Return value</span></span>

<span data-ttu-id="352a1-117">Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="352a1-117">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="352a1-118">Puntatore a [**una struttura D3DXQUATERNION**](d3dxquaternion.md) prodotto da due quaternioni.</span><span class="sxs-lookup"><span data-stu-id="352a1-118">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the product of two quaternions.</span></span>

## <a name="remarks"></a><span data-ttu-id="352a1-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="352a1-119">Remarks</span></span>

<span data-ttu-id="352a1-120">Il risultato rappresenta la rotazione Q1 seguita dalla rotazione Q2 (Out = Q2 \* Q1).</span><span class="sxs-lookup"><span data-stu-id="352a1-120">The result represents the rotation Q1 followed by the rotation Q2 (Out = Q2 \* Q1).</span></span> <span data-ttu-id="352a1-121">Questa operazione viene eseguita in modo che **D3DXQuaternionMultiply** mantenga la stessa semantica di [**D3DXMatrixMultiply**](d3dxmatrixmultiply.md) perché i quaternioni di unità possono essere considerati come un altro modo per rappresentare le matrici di rotazione.</span><span class="sxs-lookup"><span data-stu-id="352a1-121">This is done so that **D3DXQuaternionMultiply** maintain the same semantics as [**D3DXMatrixMultiply**](d3dxmatrixmultiply.md) because unit quaternions can be considered as another way to represent rotation matrices.</span></span>

<span data-ttu-id="352a1-122">Le trasformazioni vengono concatenate nello stesso ordine per entrambe le funzioni **D3DXQuaternionMultiply** e [**D3DXMatrixMultiply.**](d3dxmatrixmultiply.md)</span><span class="sxs-lookup"><span data-stu-id="352a1-122">Transformations are concatenated in the same order for both the **D3DXQuaternionMultiply** and [**D3DXMatrixMultiply**](d3dxmatrixmultiply.md) functions.</span></span> <span data-ttu-id="352a1-123">Ad esempio, supponendo che mX e mY rappresentino le stesse rotazioni di qX e qY, sia m che q rappresenteranno le stesse rotazioni.</span><span class="sxs-lookup"><span data-stu-id="352a1-123">For example, assuming mX and mY represent the same rotations as qX and qY, both m and q will represent the same rotations.</span></span>


```
D3DXMatrixMultiply(&m, &mX, &mY);
D3DXQuaternionMultiply(&q, &qX, &qY);
```



<span data-ttu-id="352a1-124">La moltiplicazione dei quaternioni non è commutativa.</span><span class="sxs-lookup"><span data-stu-id="352a1-124">The multiplication of quaternions is not commutative.</span></span>

<span data-ttu-id="352a1-125">Il valore restituito per questa funzione è lo stesso valore restituito nel *parametro pOut.*</span><span class="sxs-lookup"><span data-stu-id="352a1-125">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="352a1-126">In questo modo, la **funzione D3DXQuaternionMultiply** può essere usata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="352a1-126">In this way, the **D3DXQuaternionMultiply** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="352a1-127">Usare [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) per qualsiasi input quaternione non ancora normalizzato.</span><span class="sxs-lookup"><span data-stu-id="352a1-127">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="352a1-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="352a1-128">Requirements</span></span>



| <span data-ttu-id="352a1-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="352a1-129">Requirement</span></span> | <span data-ttu-id="352a1-130">Valore</span><span class="sxs-lookup"><span data-stu-id="352a1-130">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="352a1-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="352a1-131">Header</span></span><br/>  | <dl> <span data-ttu-id="352a1-132"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="352a1-132"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="352a1-133">Libreria</span><span class="sxs-lookup"><span data-stu-id="352a1-133">Library</span></span><br/> | <dl> <span data-ttu-id="352a1-134"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="352a1-134"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="352a1-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="352a1-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="352a1-136">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="352a1-136">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="352a1-137">**D3DXMatrixMultiply**</span><span class="sxs-lookup"><span data-stu-id="352a1-137">**D3DXMatrixMultiply**</span></span>](d3dxmatrixmultiply.md)
</dt> </dl>

 

 




