---
description: Imposta una trama.
ms.assetid: edf5bf61-508a-4417-bdf8-c36e6ba7ab30
title: 'Metodo ID3DXBaseEffect:: setexture (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetTexture
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 398dcc2f3d61ad32c08b67735a9ec7ed1a192acf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322070"
---
# <a name="id3dxbaseeffectsettexture-method"></a><span data-ttu-id="88025-103">Metodo ID3DXBaseEffect:: setexture</span><span class="sxs-lookup"><span data-stu-id="88025-103">ID3DXBaseEffect::SetTexture method</span></span>

<span data-ttu-id="88025-104">Imposta una trama.</span><span class="sxs-lookup"><span data-stu-id="88025-104">Sets a texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="88025-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="88025-105">Syntax</span></span>


```C++
HRESULT SetTexture(
  [in] D3DXHANDLE             hParameter,
  [in] LPDIRECT3DBASETEXTURE9 pTexture
);
```



## <a name="parameters"></a><span data-ttu-id="88025-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="88025-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88025-107">*hParameter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="88025-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="88025-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="88025-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="88025-109">Identificatore univoco.</span><span class="sxs-lookup"><span data-stu-id="88025-109">Unique identifier.</span></span> <span data-ttu-id="88025-110">Vedere [handle (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="88025-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="88025-111">*pTexture* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="88025-111">*pTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="88025-112">Tipo: **[ **LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)**</span><span class="sxs-lookup"><span data-stu-id="88025-112">Type: **[**LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)**</span></span>

<span data-ttu-id="88025-113">Oggetto texture.</span><span class="sxs-lookup"><span data-stu-id="88025-113">Texture object.</span></span> <span data-ttu-id="88025-114">Vedere [**IDirect3DBaseTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9).</span><span class="sxs-lookup"><span data-stu-id="88025-114">See [**IDirect3DBaseTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="88025-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="88025-115">Return value</span></span>

<span data-ttu-id="88025-116">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="88025-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="88025-117">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="88025-117">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="88025-118">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="88025-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="88025-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="88025-119">Requirements</span></span>



| <span data-ttu-id="88025-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="88025-120">Requirement</span></span> | <span data-ttu-id="88025-121">Valore</span><span class="sxs-lookup"><span data-stu-id="88025-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="88025-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="88025-122">Header</span></span><br/>  | <dl> <span data-ttu-id="88025-123"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="88025-123"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="88025-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="88025-124">Library</span></span><br/> | <dl> <span data-ttu-id="88025-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="88025-125"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="88025-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="88025-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88025-127">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="88025-127">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="88025-128">**GetTexture**</span><span class="sxs-lookup"><span data-stu-id="88025-128">**GetTexture**</span></span>](id3dxbaseeffect--gettexture.md)
</dt> </dl>

 

 
