---
description: 'Metodo ID3DXTextureShader::SetBool: imposta un valore BOOL.'
ms.assetid: 0d3c1f3a-f497-4e92-81e9-8647006910e1
title: Metodo ID3DXTextureShader::SetBool (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetBool
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 512daf7e770c72fe038622877d1756a5fd3532bf
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117629"
---
# <a name="id3dxtextureshadersetbool-method"></a><span data-ttu-id="e45ad-103">Metodo ID3DXTextureShader::SetBool</span><span class="sxs-lookup"><span data-stu-id="e45ad-103">ID3DXTextureShader::SetBool method</span></span>

<span data-ttu-id="e45ad-104">Imposta un valore BOOL.</span><span class="sxs-lookup"><span data-stu-id="e45ad-104">Sets a BOOL value.</span></span>

## <a name="syntax"></a><span data-ttu-id="e45ad-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e45ad-105">Syntax</span></span>


```C++
HRESULT SetBool(
  [in] D3DXHANDLE hConstant,
  [in] BOOL       b
);
```



## <a name="parameters"></a><span data-ttu-id="e45ad-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e45ad-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e45ad-107">*hConstant* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="e45ad-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e45ad-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="e45ad-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="e45ad-109">Identificatore univoco della costante.</span><span class="sxs-lookup"><span data-stu-id="e45ad-109">Unique identifier to the constant.</span></span> <span data-ttu-id="e45ad-110">Vedere [D3DXHANDLE](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="e45ad-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="e45ad-111">*b* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e45ad-111">*b* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e45ad-112">Tipo: **[ **BOOL**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e45ad-112">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e45ad-113">Valore BOOL.</span><span class="sxs-lookup"><span data-stu-id="e45ad-113">BOOL value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e45ad-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e45ad-114">Return value</span></span>

<span data-ttu-id="e45ad-115">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e45ad-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e45ad-116">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e45ad-116">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="e45ad-117">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="e45ad-117">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="e45ad-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e45ad-118">Requirements</span></span>



| <span data-ttu-id="e45ad-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="e45ad-119">Requirement</span></span> | <span data-ttu-id="e45ad-120">Valore</span><span class="sxs-lookup"><span data-stu-id="e45ad-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e45ad-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e45ad-121">Header</span></span><br/>  | <dl> <span data-ttu-id="e45ad-122"><dt>D3DX9Shader.h</dt></span><span class="sxs-lookup"><span data-stu-id="e45ad-122"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="e45ad-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="e45ad-123">Library</span></span><br/> | <dl> <span data-ttu-id="e45ad-124"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="e45ad-124"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="e45ad-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e45ad-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e45ad-126">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="e45ad-126">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 
