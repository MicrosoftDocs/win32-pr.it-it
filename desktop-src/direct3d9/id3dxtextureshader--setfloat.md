---
description: Imposta un numero a virgola mobile.
ms.assetid: 69bb9b15-5d66-4b1a-9559-29bcb38a965f
title: 'Metodo ID3DXTextureShader:: sefloat (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetFloat
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 85923fe20731b4482f70c439cb9df75712ab09f5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323350"
---
# <a name="id3dxtextureshadersetfloat-method"></a><span data-ttu-id="e5368-103">Metodo ID3DXTextureShader:: sefloat</span><span class="sxs-lookup"><span data-stu-id="e5368-103">ID3DXTextureShader::SetFloat method</span></span>

<span data-ttu-id="e5368-104">Imposta un numero a virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="e5368-104">Sets a floating-point number.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5368-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e5368-105">Syntax</span></span>


```C++
HRESULT SetFloat(
  [in] D3DXHANDLE hConstant,
  [in] FLOAT      f
);
```



## <a name="parameters"></a><span data-ttu-id="e5368-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e5368-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5368-107">*hConstant* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e5368-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5368-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="e5368-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="e5368-109">Identificatore univoco della costante.</span><span class="sxs-lookup"><span data-stu-id="e5368-109">Unique identifier to the constant.</span></span> <span data-ttu-id="e5368-110">Vedere [D3DXHANDLE](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="e5368-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="e5368-111">*f* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e5368-111">*f* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5368-112">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e5368-112">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e5368-113">Numero a virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="e5368-113">Floating-point number.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e5368-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e5368-114">Return value</span></span>

<span data-ttu-id="e5368-115">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e5368-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e5368-116">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e5368-116">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="e5368-117">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="e5368-117">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="e5368-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e5368-118">Requirements</span></span>



| <span data-ttu-id="e5368-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="e5368-119">Requirement</span></span> | <span data-ttu-id="e5368-120">Valore</span><span class="sxs-lookup"><span data-stu-id="e5368-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e5368-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e5368-121">Header</span></span><br/>  | <dl> <span data-ttu-id="e5368-122"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="e5368-122"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="e5368-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="e5368-123">Library</span></span><br/> | <dl> <span data-ttu-id="e5368-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e5368-124"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="e5368-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e5368-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5368-126">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="e5368-126">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 
