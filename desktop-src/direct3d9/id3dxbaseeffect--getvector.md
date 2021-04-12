---
description: Ottiene un vettore.
ms.assetid: 55f5512f-42f2-4588-abd4-1cdea530b9bf
title: 'Metodo ID3DXBaseEffect:: getvector (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetVector
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: ea50cb6bf8c3f5b08d408539eba6c9f7cb09efc1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354129"
---
# <a name="id3dxbaseeffectgetvector-method"></a><span data-ttu-id="04a16-103">Metodo ID3DXBaseEffect:: getvector</span><span class="sxs-lookup"><span data-stu-id="04a16-103">ID3DXBaseEffect::GetVector method</span></span>

<span data-ttu-id="04a16-104">Ottiene un vettore.</span><span class="sxs-lookup"><span data-stu-id="04a16-104">Gets a vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="04a16-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="04a16-105">Syntax</span></span>


```C++
HRESULT GetVector(
  [in]  D3DXHANDLE  hParameter,
  [out] D3DXVECTOR4 *pVector
);
```



## <a name="parameters"></a><span data-ttu-id="04a16-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="04a16-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04a16-107">*hParameter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="04a16-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04a16-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="04a16-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="04a16-109">Identificatore univoco.</span><span class="sxs-lookup"><span data-stu-id="04a16-109">Unique identifier.</span></span> <span data-ttu-id="04a16-110">Vedere [handle (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="04a16-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="04a16-111">*pVector* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="04a16-111">*pVector* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="04a16-112">Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="04a16-112">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="04a16-113">Restituisce un vettore 4D.</span><span class="sxs-lookup"><span data-stu-id="04a16-113">Returns a 4D vector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04a16-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="04a16-114">Return value</span></span>

<span data-ttu-id="04a16-115">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="04a16-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="04a16-116">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="04a16-116">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="04a16-117">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="04a16-117">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="04a16-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="04a16-118">Remarks</span></span>

<span data-ttu-id="04a16-119">Se il vettore di destinazione è più grande del vettore di origine, verranno riempiti solo i componenti iniziali del vettore di destinazione e i componenti rimanenti verranno impostati su zero.</span><span class="sxs-lookup"><span data-stu-id="04a16-119">If the destination vector is larger than the source vector, only the initial components of the destination vector will be filled, and the remaining components will be set to zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="04a16-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="04a16-120">Requirements</span></span>



| <span data-ttu-id="04a16-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="04a16-121">Requirement</span></span> | <span data-ttu-id="04a16-122">Valore</span><span class="sxs-lookup"><span data-stu-id="04a16-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="04a16-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="04a16-123">Header</span></span><br/>  | <dl> <span data-ttu-id="04a16-124"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="04a16-124"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="04a16-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="04a16-125">Library</span></span><br/> | <dl> <span data-ttu-id="04a16-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="04a16-126"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="04a16-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="04a16-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04a16-128">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="04a16-128">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="04a16-129">**Sevector**</span><span class="sxs-lookup"><span data-stu-id="04a16-129">**SetVector**</span></span>](id3dxbaseeffect--setvector.md)
</dt> </dl>

 

 




