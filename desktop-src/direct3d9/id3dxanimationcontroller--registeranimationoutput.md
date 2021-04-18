---
description: Aggiunge un output di animazione al controller di animazione e registra i puntatori per le trasformazioni di scala, rotazione e conversione (SRT).
ms.assetid: 8c3197bc-9d03-40ba-869b-151f9c8e96ba
title: 'Metodo ID3DXAnimationController:: RegisterAnimationOutput (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.RegisterAnimationOutput
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7670f8b311532d096b9957ebbefcf1f6fb15d952
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323290"
---
# <a name="id3dxanimationcontrollerregisteranimationoutput-method"></a><span data-ttu-id="dbf12-103">Metodo ID3DXAnimationController:: RegisterAnimationOutput</span><span class="sxs-lookup"><span data-stu-id="dbf12-103">ID3DXAnimationController::RegisterAnimationOutput method</span></span>

<span data-ttu-id="dbf12-104">Aggiunge un output di animazione al controller di animazione e registra i puntatori per le trasformazioni di scala, rotazione e conversione (SRT).</span><span class="sxs-lookup"><span data-stu-id="dbf12-104">Adds an animation output to the animation controller and registers pointers for scale, rotate, and translate (SRT) transformations.</span></span>

## <a name="syntax"></a><span data-ttu-id="dbf12-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dbf12-105">Syntax</span></span>


```C++
HRESULT RegisterAnimationOutput(
  [in] LPCSTR         Name,
  [in] D3DXMATRIX     *pMatrix,
  [in] D3DXVECTOR3    *pScale,
  [in] D3DXQUATERNION *pRotation,
  [in] D3DXVECTOR3    *pTranslation
);
```



## <a name="parameters"></a><span data-ttu-id="dbf12-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="dbf12-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dbf12-107">*Nome* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dbf12-107">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dbf12-108">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dbf12-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="dbf12-109">Nome dell'output dell'animazione.</span><span class="sxs-lookup"><span data-stu-id="dbf12-109">Name of the animation output.</span></span>

</dd> <dt>

<span data-ttu-id="dbf12-110">*pmatrix* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dbf12-110">*pMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dbf12-111">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="dbf12-111">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="dbf12-112">Puntatore a una struttura [**D3DXMATRIX**](d3dxmatrix.md) contenente dati di trasformazione SRT.</span><span class="sxs-lookup"><span data-stu-id="dbf12-112">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure containing SRT transformation data.</span></span> <span data-ttu-id="dbf12-113">Può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="dbf12-113">Can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="dbf12-114">*pScale* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dbf12-114">*pScale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dbf12-115">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="dbf12-115">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="dbf12-116">Puntatore a un vettore [**D3DXVECTOR3**](d3dxvector3.md) che descrive la scala del set di animazioni.</span><span class="sxs-lookup"><span data-stu-id="dbf12-116">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) vector that describes the scale of the animation set.</span></span> <span data-ttu-id="dbf12-117">Può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="dbf12-117">Can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="dbf12-118">*protazione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dbf12-118">*pRotation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dbf12-119">Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="dbf12-119">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="dbf12-120">Puntatore a un quaternione [**D3DXQUATERNION**](d3dxquaternion.md) che descrive la rotazione del set di animazioni.</span><span class="sxs-lookup"><span data-stu-id="dbf12-120">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) quaternion that describes the rotation of the animation set.</span></span> <span data-ttu-id="dbf12-121">Può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="dbf12-121">Can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="dbf12-122">*pTranslation* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dbf12-122">*pTranslation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dbf12-123">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="dbf12-123">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="dbf12-124">Puntatore a un vettore [**D3DXVECTOR3**](d3dxvector3.md) che descrive la traduzione del set di animazioni.</span><span class="sxs-lookup"><span data-stu-id="dbf12-124">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) vector that describes the translation of the animation set.</span></span> <span data-ttu-id="dbf12-125">Può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="dbf12-125">Can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dbf12-126">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="dbf12-126">Return value</span></span>

<span data-ttu-id="dbf12-127">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="dbf12-127">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="dbf12-128">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="dbf12-128">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="dbf12-129">Se il metodo ha esito negativo, il valore restituito può essere uno dei valori seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="dbf12-129">If the method fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="dbf12-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="dbf12-130">Remarks</span></span>

<span data-ttu-id="dbf12-131">Se l'output di animazione è già registrato, pMatrix verrà riempito con i dati di trasformazione di input.</span><span class="sxs-lookup"><span data-stu-id="dbf12-131">If the animation output is already registered, pMatrix will be filled with the input transformation data.</span></span>

<span data-ttu-id="dbf12-132">I set di animazioni creati con [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) registrano automaticamente tutti i set di animazioni caricati.</span><span class="sxs-lookup"><span data-stu-id="dbf12-132">Animation sets created with [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) automatically register all loaded animation sets.</span></span>

## <a name="requirements"></a><span data-ttu-id="dbf12-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dbf12-133">Requirements</span></span>



| <span data-ttu-id="dbf12-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="dbf12-134">Requirement</span></span> | <span data-ttu-id="dbf12-135">Valore</span><span class="sxs-lookup"><span data-stu-id="dbf12-135">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="dbf12-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="dbf12-136">Header</span></span><br/>  | <dl> <span data-ttu-id="dbf12-137"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="dbf12-137"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="dbf12-138">Libreria</span><span class="sxs-lookup"><span data-stu-id="dbf12-138">Library</span></span><br/> | <dl> <span data-ttu-id="dbf12-139"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dbf12-139"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="dbf12-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dbf12-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbf12-141">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="dbf12-141">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
