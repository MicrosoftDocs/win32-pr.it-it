---
description: Ottiene una descrizione del parametro o dell'annotazione.
ms.assetid: fd54eb08-a7e4-4106-b0ed-49a4da7fcadc
title: 'Metodo ID3DXBaseEffect:: GetParameterDesc (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetParameterDesc
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 8c3a52c06ebed764b3ab1718488c2dbc55ceda41
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323595"
---
# <a name="id3dxbaseeffectgetparameterdesc-method"></a><span data-ttu-id="b6c74-103">Metodo ID3DXBaseEffect:: GetParameterDesc</span><span class="sxs-lookup"><span data-stu-id="b6c74-103">ID3DXBaseEffect::GetParameterDesc method</span></span>

<span data-ttu-id="b6c74-104">Ottiene una descrizione del parametro o dell'annotazione.</span><span class="sxs-lookup"><span data-stu-id="b6c74-104">Gets a parameter or annotation description.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6c74-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b6c74-105">Syntax</span></span>


```C++
HRESULT GetParameterDesc(
  [in]  D3DXHANDLE         hParameter,
  [out] D3DXPARAMETER_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="b6c74-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b6c74-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6c74-107">*hParameter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b6c74-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6c74-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="b6c74-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="b6c74-109">Parametro o handle di annotazione.</span><span class="sxs-lookup"><span data-stu-id="b6c74-109">Parameter or annotation handle.</span></span> <span data-ttu-id="b6c74-110">Vedere [handle (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="b6c74-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="b6c74-111">*pDesc* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="b6c74-111">*pDesc* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b6c74-112">Tipo: **[ **D3DXPARAMETER \_ desc**](d3dxparameter-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="b6c74-112">Type: **[**D3DXPARAMETER\_DESC**](d3dxparameter-desc.md)\***</span></span>

<span data-ttu-id="b6c74-113">Restituisce una descrizione del parametro o dell'annotazione specificato.</span><span class="sxs-lookup"><span data-stu-id="b6c74-113">Returns a description of the specified parameter or annotation.</span></span> <span data-ttu-id="b6c74-114">Vedere [**D3DXPARAMETER \_ desc**](d3dxparameter-desc.md).</span><span class="sxs-lookup"><span data-stu-id="b6c74-114">See [**D3DXPARAMETER\_DESC**](d3dxparameter-desc.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6c74-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b6c74-115">Return value</span></span>

<span data-ttu-id="b6c74-116">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b6c74-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b6c74-117">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b6c74-117">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="b6c74-118">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="b6c74-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6c74-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b6c74-119">Requirements</span></span>



| <span data-ttu-id="b6c74-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="b6c74-120">Requirement</span></span> | <span data-ttu-id="b6c74-121">Valore</span><span class="sxs-lookup"><span data-stu-id="b6c74-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6c74-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b6c74-122">Header</span></span><br/>  | <dl> <span data-ttu-id="b6c74-123"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="b6c74-123"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="b6c74-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="b6c74-124">Library</span></span><br/> | <dl> <span data-ttu-id="b6c74-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b6c74-125"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="b6c74-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b6c74-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6c74-127">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="b6c74-127">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 




