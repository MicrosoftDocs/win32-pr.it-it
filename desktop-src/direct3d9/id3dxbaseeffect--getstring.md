---
description: Ottiene una stringa.
ms.assetid: 49388582-a110-4aa2-90ab-2282b59da951
title: 'Metodo ID3DXBaseEffect:: GetString (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetString
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 74c82bb80603dc4519e717d86297f6529ad36193
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323588"
---
# <a name="id3dxbaseeffectgetstring-method"></a><span data-ttu-id="17b15-103">Metodo ID3DXBaseEffect:: GetString</span><span class="sxs-lookup"><span data-stu-id="17b15-103">ID3DXBaseEffect::GetString method</span></span>

<span data-ttu-id="17b15-104">Ottiene una stringa.</span><span class="sxs-lookup"><span data-stu-id="17b15-104">Gets a string.</span></span>

## <a name="syntax"></a><span data-ttu-id="17b15-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="17b15-105">Syntax</span></span>


```C++
HRESULT GetString(
  [in]  D3DXHANDLE hParameter,
  [out] LPCSTR     *ppString
);
```



## <a name="parameters"></a><span data-ttu-id="17b15-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="17b15-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17b15-107">*hParameter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="17b15-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17b15-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="17b15-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="17b15-109">Identificatore univoco.</span><span class="sxs-lookup"><span data-stu-id="17b15-109">Unique identifier.</span></span> <span data-ttu-id="17b15-110">Vedere [handle (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="17b15-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="17b15-111">*ppString* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="17b15-111">*ppString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="17b15-112">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="17b15-112">Type: **[**LPCSTR**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="17b15-113">Restituisce una stringa identificata da hParameter.</span><span class="sxs-lookup"><span data-stu-id="17b15-113">Returns a string identified by hParameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17b15-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="17b15-114">Return value</span></span>

<span data-ttu-id="17b15-115">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="17b15-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="17b15-116">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="17b15-116">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="17b15-117">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="17b15-117">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="17b15-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="17b15-118">Requirements</span></span>



| <span data-ttu-id="17b15-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="17b15-119">Requirement</span></span> | <span data-ttu-id="17b15-120">Valore</span><span class="sxs-lookup"><span data-stu-id="17b15-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="17b15-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="17b15-121">Header</span></span><br/>  | <dl> <span data-ttu-id="17b15-122"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="17b15-122"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="17b15-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="17b15-123">Library</span></span><br/> | <dl> <span data-ttu-id="17b15-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="17b15-124"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="17b15-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="17b15-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17b15-126">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="17b15-126">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="17b15-127">**SetString**</span><span class="sxs-lookup"><span data-stu-id="17b15-127">**SetString**</span></span>](id3dxbaseeffect--setstring.md)
</dt> </dl>

 

 
