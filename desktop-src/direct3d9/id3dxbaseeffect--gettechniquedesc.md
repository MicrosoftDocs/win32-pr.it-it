---
description: Ottiene una descrizione di tecnica.
ms.assetid: 12122858-1e54-446c-8f12-20cc62499d74
title: 'Metodo ID3DXBaseEffect:: GetTechniqueDesc (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetTechniqueDesc
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 6027cf24576a29a1f447e5c20f99634c42adf00d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235197"
---
# <a name="id3dxbaseeffectgettechniquedesc-method"></a><span data-ttu-id="2e92c-103">Metodo ID3DXBaseEffect:: GetTechniqueDesc</span><span class="sxs-lookup"><span data-stu-id="2e92c-103">ID3DXBaseEffect::GetTechniqueDesc method</span></span>

<span data-ttu-id="2e92c-104">Ottiene una descrizione di tecnica.</span><span class="sxs-lookup"><span data-stu-id="2e92c-104">Gets a technique description.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e92c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2e92c-105">Syntax</span></span>


```C++
HRESULT GetTechniqueDesc(
  [in]  D3DXHANDLE         hTechnique,
  [out] D3DXTECHNIQUE_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="2e92c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="2e92c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e92c-107">*hTechnique* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2e92c-107">*hTechnique* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e92c-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="2e92c-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="2e92c-109">Handle di tecnica.</span><span class="sxs-lookup"><span data-stu-id="2e92c-109">Technique handle.</span></span> <span data-ttu-id="2e92c-110">Vedere [handle (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="2e92c-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="2e92c-111">*pDesc* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="2e92c-111">*pDesc* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2e92c-112">Tipo: **[ **D3DXTECHNIQUE \_ desc**](d3dxtechnique-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="2e92c-112">Type: **[**D3DXTECHNIQUE\_DESC**](d3dxtechnique-desc.md)\***</span></span>

<span data-ttu-id="2e92c-113">Restituisce una descrizione della tecnica.</span><span class="sxs-lookup"><span data-stu-id="2e92c-113">Returns a description of the technique.</span></span> <span data-ttu-id="2e92c-114">Vedere [**D3DXTECHNIQUE \_ desc**](d3dxtechnique-desc.md).</span><span class="sxs-lookup"><span data-stu-id="2e92c-114">See [**D3DXTECHNIQUE\_DESC**](d3dxtechnique-desc.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e92c-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2e92c-115">Return value</span></span>

<span data-ttu-id="2e92c-116">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2e92c-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2e92c-117">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="2e92c-117">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="2e92c-118">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="2e92c-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e92c-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2e92c-119">Requirements</span></span>



| <span data-ttu-id="2e92c-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e92c-120">Requirement</span></span> | <span data-ttu-id="2e92c-121">Valore</span><span class="sxs-lookup"><span data-stu-id="2e92c-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e92c-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2e92c-122">Header</span></span><br/>  | <dl> <span data-ttu-id="2e92c-123"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="2e92c-123"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="2e92c-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="2e92c-124">Library</span></span><br/> | <dl> <span data-ttu-id="2e92c-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2e92c-125"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="2e92c-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2e92c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e92c-127">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="2e92c-127">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 




