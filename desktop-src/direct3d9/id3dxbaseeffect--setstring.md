---
description: Imposta una stringa.
ms.assetid: 7e8eef70-85ee-461d-bf8c-44cda5f184cd
title: 'Metodo ID3DXBaseEffect:: sestring (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetString
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 1a7c4f86c6b7fa78c869eb1d5bd49634ec4b496d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322071"
---
# <a name="id3dxbaseeffectsetstring-method"></a><span data-ttu-id="6d4c6-103">Metodo ID3DXBaseEffect:: sestring</span><span class="sxs-lookup"><span data-stu-id="6d4c6-103">ID3DXBaseEffect::SetString method</span></span>

<span data-ttu-id="6d4c6-104">Imposta una stringa.</span><span class="sxs-lookup"><span data-stu-id="6d4c6-104">Sets a string.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d4c6-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6d4c6-105">Syntax</span></span>


```C++
HRESULT SetString(
  [in] D3DXHANDLE hParameter,
  [in] LPCSTR     pString
);
```



## <a name="parameters"></a><span data-ttu-id="6d4c6-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="6d4c6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d4c6-107">*hParameter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6d4c6-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d4c6-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="6d4c6-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="6d4c6-109">Identificatore univoco.</span><span class="sxs-lookup"><span data-stu-id="6d4c6-109">Unique identifier.</span></span> <span data-ttu-id="6d4c6-110">Vedere [handle (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="6d4c6-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="6d4c6-111">*pString* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6d4c6-111">*pString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d4c6-112">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6d4c6-112">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6d4c6-113">Stringa da impostare.</span><span class="sxs-lookup"><span data-stu-id="6d4c6-113">String to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6d4c6-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6d4c6-114">Return value</span></span>

<span data-ttu-id="6d4c6-115">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6d4c6-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6d4c6-116">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="6d4c6-116">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="6d4c6-117">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="6d4c6-117">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d4c6-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6d4c6-118">Requirements</span></span>



| <span data-ttu-id="6d4c6-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="6d4c6-119">Requirement</span></span> | <span data-ttu-id="6d4c6-120">Valore</span><span class="sxs-lookup"><span data-stu-id="6d4c6-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d4c6-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6d4c6-121">Header</span></span><br/>  | <dl> <span data-ttu-id="6d4c6-122"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="6d4c6-122"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="6d4c6-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="6d4c6-123">Library</span></span><br/> | <dl> <span data-ttu-id="6d4c6-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6d4c6-124"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="6d4c6-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6d4c6-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d4c6-126">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="6d4c6-126">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="6d4c6-127">**GetString**</span><span class="sxs-lookup"><span data-stu-id="6d4c6-127">**GetString**</span></span>](id3dxbaseeffect--getstring.md)
</dt> </dl>

 

 
