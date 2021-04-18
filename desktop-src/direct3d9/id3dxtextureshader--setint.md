---
description: Imposta un valore integer.
ms.assetid: e7dcf3f4-1d0c-432a-85fc-0473c49956ff
title: 'Metodo ID3DXTextureShader:: setInt (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetInt
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3b440811123935f279b0c4c1661c2a39aa86669f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323349"
---
# <a name="id3dxtextureshadersetint-method"></a><span data-ttu-id="04f5d-103">Metodo ID3DXTextureShader:: setInt</span><span class="sxs-lookup"><span data-stu-id="04f5d-103">ID3DXTextureShader::SetInt method</span></span>

<span data-ttu-id="04f5d-104">Imposta un valore integer.</span><span class="sxs-lookup"><span data-stu-id="04f5d-104">Sets an integer value.</span></span>

## <a name="syntax"></a><span data-ttu-id="04f5d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="04f5d-105">Syntax</span></span>


```C++
HRESULT SetInt(
  [in] D3DXHANDLE hConstant,
  [in] INT        n
);
```



## <a name="parameters"></a><span data-ttu-id="04f5d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="04f5d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04f5d-107">*hConstant* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="04f5d-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04f5d-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="04f5d-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="04f5d-109">Identificatore univoco della costante.</span><span class="sxs-lookup"><span data-stu-id="04f5d-109">Unique identifier to the constant.</span></span> <span data-ttu-id="04f5d-110">Vedere [D3DXHANDLE](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="04f5d-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="04f5d-111">*n* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="04f5d-111">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04f5d-112">Tipo: **[ **int**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="04f5d-112">Type: **[**INT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="04f5d-113">Valore intero.</span><span class="sxs-lookup"><span data-stu-id="04f5d-113">Integer value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04f5d-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="04f5d-114">Return value</span></span>

<span data-ttu-id="04f5d-115">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="04f5d-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="04f5d-116">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="04f5d-116">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="04f5d-117">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="04f5d-117">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="04f5d-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="04f5d-118">Requirements</span></span>



| <span data-ttu-id="04f5d-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="04f5d-119">Requirement</span></span> | <span data-ttu-id="04f5d-120">Valore</span><span class="sxs-lookup"><span data-stu-id="04f5d-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="04f5d-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="04f5d-121">Header</span></span><br/>  | <dl> <span data-ttu-id="04f5d-122"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="04f5d-122"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="04f5d-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="04f5d-123">Library</span></span><br/> | <dl> <span data-ttu-id="04f5d-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="04f5d-124"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="04f5d-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="04f5d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04f5d-126">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="04f5d-126">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 
