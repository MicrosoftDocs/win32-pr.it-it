---
description: Imposta un vettore.
ms.assetid: 7dae88fc-d5d3-4751-859a-fa1bde4d0ce8
title: 'Metodo ID3DXBaseEffect:: sevector (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetVector
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 5d6fccc24410e06dd9bb4e6b0b1f1c36b03dd355
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323633"
---
# <a name="id3dxbaseeffectsetvector-method"></a><span data-ttu-id="1855a-103">Metodo ID3DXBaseEffect:: sevector</span><span class="sxs-lookup"><span data-stu-id="1855a-103">ID3DXBaseEffect::SetVector method</span></span>

<span data-ttu-id="1855a-104">Imposta un vettore.</span><span class="sxs-lookup"><span data-stu-id="1855a-104">Sets a vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="1855a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1855a-105">Syntax</span></span>


```C++
HRESULT SetVector(
  [in]       D3DXHANDLE  hParameter,
  [in] const D3DXVECTOR4 *pVector
);
```



## <a name="parameters"></a><span data-ttu-id="1855a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="1855a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1855a-107">*hParameter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1855a-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1855a-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="1855a-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="1855a-109">Identificatore univoco.</span><span class="sxs-lookup"><span data-stu-id="1855a-109">Unique identifier.</span></span> <span data-ttu-id="1855a-110">Vedere [handle (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="1855a-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="1855a-111">*pVector* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1855a-111">*pVector* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1855a-112">Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="1855a-112">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="1855a-113">Puntatore a un vettore 4D.</span><span class="sxs-lookup"><span data-stu-id="1855a-113">Pointer to a 4D vector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1855a-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1855a-114">Return value</span></span>

<span data-ttu-id="1855a-115">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1855a-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1855a-116">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="1855a-116">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="1855a-117">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="1855a-117">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="1855a-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="1855a-118">Remarks</span></span>

<span data-ttu-id="1855a-119">Se il vettore di destinazione è inferiore al vettore di origine, i componenti aggiuntivi del vettore di origine verranno ignorati.</span><span class="sxs-lookup"><span data-stu-id="1855a-119">If the destination vector is smaller than the source vector, the additional components of the source vector will be ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="1855a-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1855a-120">Requirements</span></span>



| <span data-ttu-id="1855a-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="1855a-121">Requirement</span></span> | <span data-ttu-id="1855a-122">Valore</span><span class="sxs-lookup"><span data-stu-id="1855a-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="1855a-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1855a-123">Header</span></span><br/>  | <dl> <span data-ttu-id="1855a-124"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="1855a-124"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="1855a-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="1855a-125">Library</span></span><br/> | <dl> <span data-ttu-id="1855a-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1855a-126"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="1855a-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1855a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1855a-128">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="1855a-128">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="1855a-129">**Getvector**</span><span class="sxs-lookup"><span data-stu-id="1855a-129">**GetVector**</span></span>](id3dxbaseeffect--getvector.md)
</dt> </dl>

 

 




