---
description: Ottiene una descrizione della funzione.
ms.assetid: a1a0ccf4-2428-4e60-9af0-07dc2132a367
title: 'Metodo ID3DXBaseEffect:: GetFunctionDesc (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetFunctionDesc
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 718960da7ff73f24f865fdacc09dfe55ff09a466
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323602"
---
# <a name="id3dxbaseeffectgetfunctiondesc-method"></a><span data-ttu-id="6f0d2-103">Metodo ID3DXBaseEffect:: GetFunctionDesc</span><span class="sxs-lookup"><span data-stu-id="6f0d2-103">ID3DXBaseEffect::GetFunctionDesc method</span></span>

<span data-ttu-id="6f0d2-104">Ottiene una descrizione della funzione.</span><span class="sxs-lookup"><span data-stu-id="6f0d2-104">Gets a function description.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f0d2-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6f0d2-105">Syntax</span></span>


```C++
HRESULT GetFunctionDesc(
  [in]  D3DXHANDLE        hFunction,
  [out] D3DXFUNCTION_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="6f0d2-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="6f0d2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f0d2-107">*hFunction* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6f0d2-107">*hFunction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f0d2-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="6f0d2-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="6f0d2-109">Handle di funzione.</span><span class="sxs-lookup"><span data-stu-id="6f0d2-109">Function handle.</span></span> <span data-ttu-id="6f0d2-110">Vedere [handle (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="6f0d2-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="6f0d2-111">*pDesc* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="6f0d2-111">*pDesc* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6f0d2-112">Tipo: **[ **D3DXFUNCTION \_ desc**](d3dxfunction-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="6f0d2-112">Type: **[**D3DXFUNCTION\_DESC**](d3dxfunction-desc.md)\***</span></span>

<span data-ttu-id="6f0d2-113">Restituisce una descrizione della funzione.</span><span class="sxs-lookup"><span data-stu-id="6f0d2-113">Returns a description of the function.</span></span> <span data-ttu-id="6f0d2-114">Vedere [**D3DXFUNCTION \_ desc**](d3dxfunction-desc.md).</span><span class="sxs-lookup"><span data-stu-id="6f0d2-114">See [**D3DXFUNCTION\_DESC**](d3dxfunction-desc.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6f0d2-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6f0d2-115">Return value</span></span>

<span data-ttu-id="6f0d2-116">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6f0d2-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6f0d2-117">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="6f0d2-117">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="6f0d2-118">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="6f0d2-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="6f0d2-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6f0d2-119">Requirements</span></span>



| <span data-ttu-id="6f0d2-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="6f0d2-120">Requirement</span></span> | <span data-ttu-id="6f0d2-121">Valore</span><span class="sxs-lookup"><span data-stu-id="6f0d2-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f0d2-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6f0d2-122">Header</span></span><br/>  | <dl> <span data-ttu-id="6f0d2-123"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="6f0d2-123"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="6f0d2-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="6f0d2-124">Library</span></span><br/> | <dl> <span data-ttu-id="6f0d2-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6f0d2-125"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="6f0d2-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6f0d2-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f0d2-127">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="6f0d2-127">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 




