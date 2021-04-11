---
description: Determina se un parametro viene utilizzato dalla tecnica.
ms.assetid: ac50c0d3-93d9-4477-a854-d0b53df28c90
title: 'Metodo ID3DXEffect:: IsParameterUsed (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.IsParameterUsed
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 6cbe4783a9ad5b618f05941eae08af4c15be0512
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104132302"
---
# <a name="id3dxeffectisparameterused-method"></a><span data-ttu-id="79e8d-103">Metodo ID3DXEffect:: IsParameterUsed</span><span class="sxs-lookup"><span data-stu-id="79e8d-103">ID3DXEffect::IsParameterUsed method</span></span>

<span data-ttu-id="79e8d-104">Determina se un parametro viene utilizzato dalla tecnica.</span><span class="sxs-lookup"><span data-stu-id="79e8d-104">Determines if a parameter is used by the technique.</span></span>

## <a name="syntax"></a><span data-ttu-id="79e8d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="79e8d-105">Syntax</span></span>


```C++
BOOL IsParameterUsed(
  [in] D3DXHANDLE hParameter,
  [in] D3DXHANDLE hTechnique
);
```



## <a name="parameters"></a><span data-ttu-id="79e8d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="79e8d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79e8d-107">*hParameter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="79e8d-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79e8d-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="79e8d-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="79e8d-109">Identificatore univoco per il parametro.</span><span class="sxs-lookup"><span data-stu-id="79e8d-109">Unique identifier for the parameter.</span></span> <span data-ttu-id="79e8d-110">Vedere [handle (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="79e8d-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="79e8d-111">*hTechnique* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="79e8d-111">*hTechnique* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79e8d-112">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="79e8d-112">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="79e8d-113">Identificatore univoco per la tecnica.</span><span class="sxs-lookup"><span data-stu-id="79e8d-113">Unique identifier for the technique.</span></span> <span data-ttu-id="79e8d-114">Vedere [handle (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="79e8d-114">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="79e8d-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="79e8d-115">Return value</span></span>

<span data-ttu-id="79e8d-116">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="79e8d-116">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="79e8d-117">Restituisce **true** se viene utilizzato il parametro e restituisce **false** se il parametro non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="79e8d-117">Returns **TRUE** if the parameter is being used and returns **FALSE** if the parameter is not being used.</span></span>

## <a name="requirements"></a><span data-ttu-id="79e8d-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="79e8d-118">Requirements</span></span>



| <span data-ttu-id="79e8d-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="79e8d-119">Requirement</span></span> | <span data-ttu-id="79e8d-120">Valore</span><span class="sxs-lookup"><span data-stu-id="79e8d-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="79e8d-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="79e8d-121">Header</span></span><br/>  | <dl> <span data-ttu-id="79e8d-122"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="79e8d-122"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="79e8d-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="79e8d-123">Library</span></span><br/> | <dl> <span data-ttu-id="79e8d-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="79e8d-124"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="79e8d-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="79e8d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79e8d-126">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="79e8d-126">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> </dl>

 

 
