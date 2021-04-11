---
description: Ottiene un vertex shader.
ms.assetid: ab58b465-7b10-46eb-88c0-c5229cb09481
title: 'Metodo ID3DXBaseEffect:: GetVertexShader (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetVertexShader
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: ad6bb7cbf7c483ccaffa83b0e828c867026957fa
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104132287"
---
# <a name="id3dxbaseeffectgetvertexshader-method"></a><span data-ttu-id="d01ff-103">Metodo ID3DXBaseEffect:: GetVertexShader</span><span class="sxs-lookup"><span data-stu-id="d01ff-103">ID3DXBaseEffect::GetVertexShader method</span></span>

<span data-ttu-id="d01ff-104">Ottiene un vertex shader.</span><span class="sxs-lookup"><span data-stu-id="d01ff-104">Gets a vertex shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="d01ff-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d01ff-105">Syntax</span></span>


```C++
HRESULT GetVertexShader(
  [in]  D3DXHANDLE              hParameter,
  [out] LPDIRECT3DVERTEXSHADER9 *ppVShader
);
```



## <a name="parameters"></a><span data-ttu-id="d01ff-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d01ff-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d01ff-107">*hParameter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d01ff-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d01ff-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="d01ff-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="d01ff-109">Identificatore univoco.</span><span class="sxs-lookup"><span data-stu-id="d01ff-109">Unique identifier.</span></span> <span data-ttu-id="d01ff-110">Vedere [handle (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="d01ff-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="d01ff-111">*ppVShader* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="d01ff-111">*ppVShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d01ff-112">Tipo: **[ **LPDIRECT3DVERTEXSHADER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexshader9)\***</span><span class="sxs-lookup"><span data-stu-id="d01ff-112">Type: **[**LPDIRECT3DVERTEXSHADER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexshader9)\***</span></span>

<span data-ttu-id="d01ff-113">Restituisce un oggetto vertex shader.</span><span class="sxs-lookup"><span data-stu-id="d01ff-113">Returns a vertex shader object.</span></span> <span data-ttu-id="d01ff-114">Vedere [**IDirect3DVertexShader9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexshader9).</span><span class="sxs-lookup"><span data-stu-id="d01ff-114">See [**IDirect3DVertexShader9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexshader9).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d01ff-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d01ff-115">Return value</span></span>

<span data-ttu-id="d01ff-116">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d01ff-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d01ff-117">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d01ff-117">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="d01ff-118">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="d01ff-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="d01ff-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d01ff-119">Requirements</span></span>



| <span data-ttu-id="d01ff-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="d01ff-120">Requirement</span></span> | <span data-ttu-id="d01ff-121">Valore</span><span class="sxs-lookup"><span data-stu-id="d01ff-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d01ff-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d01ff-122">Header</span></span><br/>  | <dl> <span data-ttu-id="d01ff-123"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="d01ff-123"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="d01ff-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="d01ff-124">Library</span></span><br/> | <dl> <span data-ttu-id="d01ff-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d01ff-125"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="d01ff-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d01ff-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d01ff-127">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="d01ff-127">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 
