---
description: Imposta un valore BOOL.
ms.assetid: 0d3c1f3a-f497-4e92-81e9-8647006910e1
title: 'Metodo ID3DXTextureShader:: SetValue (D3DX9Shader. h)'
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
ms.openlocfilehash: 49fbc2d2841957e75a8bc3adaf40ce0fdf5e2a1f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762251"
---
# <a name="id3dxtextureshadersetbool-method"></a><span data-ttu-id="e2234-103">Metodo ID3DXTextureShader:: SetValue</span><span class="sxs-lookup"><span data-stu-id="e2234-103">ID3DXTextureShader::SetBool method</span></span>

<span data-ttu-id="e2234-104">Imposta un valore BOOL.</span><span class="sxs-lookup"><span data-stu-id="e2234-104">Sets a BOOL value.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2234-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e2234-105">Syntax</span></span>


```C++
HRESULT SetBool(
  [in] D3DXHANDLE hConstant,
  [in] BOOL       b
);
```



## <a name="parameters"></a><span data-ttu-id="e2234-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e2234-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2234-107">*hConstant* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e2234-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2234-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="e2234-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="e2234-109">Identificatore univoco della costante.</span><span class="sxs-lookup"><span data-stu-id="e2234-109">Unique identifier to the constant.</span></span> <span data-ttu-id="e2234-110">Vedere [D3DXHANDLE](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="e2234-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="e2234-111">*b* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e2234-111">*b* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2234-112">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e2234-112">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e2234-113">Valore BOOL.</span><span class="sxs-lookup"><span data-stu-id="e2234-113">BOOL value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2234-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e2234-114">Return value</span></span>

<span data-ttu-id="e2234-115">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e2234-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e2234-116">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e2234-116">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="e2234-117">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="e2234-117">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2234-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e2234-118">Requirements</span></span>



| <span data-ttu-id="e2234-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="e2234-119">Requirement</span></span> | <span data-ttu-id="e2234-120">Valore</span><span class="sxs-lookup"><span data-stu-id="e2234-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2234-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e2234-121">Header</span></span><br/>  | <dl> <span data-ttu-id="e2234-122"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="e2234-122"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="e2234-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="e2234-123">Library</span></span><br/> | <dl> <span data-ttu-id="e2234-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e2234-124"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="e2234-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e2234-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2234-126">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="e2234-126">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 
