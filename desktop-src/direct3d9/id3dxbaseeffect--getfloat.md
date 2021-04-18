---
description: Ottiene un valore a virgola mobile.
ms.assetid: 239dd29c-092a-4b9f-ba24-eb6181e91461
title: 'Metodo ID3DXBaseEffect:: GetFloat (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetFloat
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 51edaa1872223727abdc396766552720cd34d726
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323607"
---
# <a name="id3dxbaseeffectgetfloat-method"></a><span data-ttu-id="fc7a8-103">Metodo ID3DXBaseEffect:: GetFloat</span><span class="sxs-lookup"><span data-stu-id="fc7a8-103">ID3DXBaseEffect::GetFloat method</span></span>

<span data-ttu-id="fc7a8-104">Ottiene un valore a virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="fc7a8-104">Gets a floating point value.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc7a8-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fc7a8-105">Syntax</span></span>


```C++
HRESULT GetFloat(
  [in]  D3DXHANDLE hParameter,
  [out] FLOAT      *pf
);
```



## <a name="parameters"></a><span data-ttu-id="fc7a8-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="fc7a8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc7a8-107">*hParameter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fc7a8-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc7a8-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="fc7a8-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="fc7a8-109">Identificatore univoco.</span><span class="sxs-lookup"><span data-stu-id="fc7a8-109">Unique identifier.</span></span> <span data-ttu-id="fc7a8-110">Vedere [handle (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="fc7a8-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="fc7a8-111">*PF* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="fc7a8-111">*pf* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fc7a8-112">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="fc7a8-112">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="fc7a8-113">Restituisce un valore a virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="fc7a8-113">Returns a floating point value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fc7a8-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fc7a8-114">Return value</span></span>

<span data-ttu-id="fc7a8-115">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="fc7a8-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="fc7a8-116">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="fc7a8-116">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="fc7a8-117">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="fc7a8-117">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc7a8-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fc7a8-118">Requirements</span></span>



| <span data-ttu-id="fc7a8-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc7a8-119">Requirement</span></span> | <span data-ttu-id="fc7a8-120">Valore</span><span class="sxs-lookup"><span data-stu-id="fc7a8-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc7a8-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fc7a8-121">Header</span></span><br/>  | <dl> <span data-ttu-id="fc7a8-122"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="fc7a8-122"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="fc7a8-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="fc7a8-123">Library</span></span><br/> | <dl> <span data-ttu-id="fc7a8-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fc7a8-124"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="fc7a8-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fc7a8-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc7a8-126">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="fc7a8-126">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="fc7a8-127">**SetFloat**</span><span class="sxs-lookup"><span data-stu-id="fc7a8-127">**SetFloat**</span></span>](id3dxbaseeffect--setfloat.md)
</dt> </dl>

 

 
