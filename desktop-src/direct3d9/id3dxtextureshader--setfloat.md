---
description: 'Metodo ID3DXTextureShader::SetFloat: imposta un numero a virgola mobile.'
ms.assetid: 69bb9b15-5d66-4b1a-9559-29bcb38a965f
title: Metodo ID3DXTextureShader::SetFloat (D3DX9Shader.h)
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
ms.openlocfilehash: 6230b0736cb3bc623b0413f7b5a1cb9635f00e07
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107169"
---
# <a name="id3dxtextureshadersetfloat-method"></a><span data-ttu-id="21c19-103">Metodo ID3DXTextureShader::SetFloat</span><span class="sxs-lookup"><span data-stu-id="21c19-103">ID3DXTextureShader::SetFloat method</span></span>

<span data-ttu-id="21c19-104">Imposta un numero a virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="21c19-104">Sets a floating-point number.</span></span>

## <a name="syntax"></a><span data-ttu-id="21c19-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="21c19-105">Syntax</span></span>


```C++
HRESULT SetFloat(
  [in] D3DXHANDLE hConstant,
  [in] FLOAT      f
);
```



## <a name="parameters"></a><span data-ttu-id="21c19-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="21c19-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21c19-107">*hConstant* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="21c19-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21c19-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="21c19-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="21c19-109">Identificatore univoco della costante.</span><span class="sxs-lookup"><span data-stu-id="21c19-109">Unique identifier to the constant.</span></span> <span data-ttu-id="21c19-110">Vedere [D3DXHANDLE](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="21c19-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="21c19-111">*f* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="21c19-111">*f* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21c19-112">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="21c19-112">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="21c19-113">Numero a virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="21c19-113">Floating-point number.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21c19-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="21c19-114">Return value</span></span>

<span data-ttu-id="21c19-115">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="21c19-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="21c19-116">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="21c19-116">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="21c19-117">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="21c19-117">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="21c19-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="21c19-118">Requirements</span></span>



| <span data-ttu-id="21c19-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="21c19-119">Requirement</span></span> | <span data-ttu-id="21c19-120">Valore</span><span class="sxs-lookup"><span data-stu-id="21c19-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="21c19-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="21c19-121">Header</span></span><br/>  | <dl> <span data-ttu-id="21c19-122"><dt>D3DX9Shader.h</dt></span><span class="sxs-lookup"><span data-stu-id="21c19-122"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="21c19-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="21c19-123">Library</span></span><br/> | <dl> <span data-ttu-id="21c19-124"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="21c19-124"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="21c19-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="21c19-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21c19-126">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="21c19-126">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 
