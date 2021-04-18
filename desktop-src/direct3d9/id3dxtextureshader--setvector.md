---
description: Imposta un vettore 4D.
ms.assetid: befed2a8-7695-4f06-a6ee-aff466d1940a
title: 'Metodo ID3DXTextureShader:: sevector (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetVector
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b7bc7e3b7f4920c21c52111410c626090e452fa7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322548"
---
# <a name="id3dxtextureshadersetvector-method"></a><span data-ttu-id="46c5e-103">Metodo ID3DXTextureShader:: sevector</span><span class="sxs-lookup"><span data-stu-id="46c5e-103">ID3DXTextureShader::SetVector method</span></span>

<span data-ttu-id="46c5e-104">Imposta un vettore 4D.</span><span class="sxs-lookup"><span data-stu-id="46c5e-104">Sets a 4D vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="46c5e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="46c5e-105">Syntax</span></span>


```C++
HRESULT SetVector(
  [in]       D3DXHANDLE  hConstant,
  [in] const D3DXVECTOR4 *pVector
);
```



## <a name="parameters"></a><span data-ttu-id="46c5e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="46c5e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46c5e-107">*hConstant* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="46c5e-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46c5e-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="46c5e-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="46c5e-109">Identificatore univoco della costante Vector.</span><span class="sxs-lookup"><span data-stu-id="46c5e-109">Unique identifier to the vector constant.</span></span> <span data-ttu-id="46c5e-110">Vedere [D3DXHANDLE](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="46c5e-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="46c5e-111">*pVector* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="46c5e-111">*pVector* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46c5e-112">Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="46c5e-112">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="46c5e-113">Puntatore a un vettore 4D.</span><span class="sxs-lookup"><span data-stu-id="46c5e-113">Pointer to a 4D vector.</span></span> <span data-ttu-id="46c5e-114">Vedere [**D3DXVECTOR4**](d3dxvector4.md).</span><span class="sxs-lookup"><span data-stu-id="46c5e-114">See [**D3DXVECTOR4**](d3dxvector4.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46c5e-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="46c5e-115">Return value</span></span>

<span data-ttu-id="46c5e-116">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="46c5e-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="46c5e-117">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="46c5e-117">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="46c5e-118">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="46c5e-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="46c5e-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="46c5e-119">Requirements</span></span>



| <span data-ttu-id="46c5e-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="46c5e-120">Requirement</span></span> | <span data-ttu-id="46c5e-121">Valore</span><span class="sxs-lookup"><span data-stu-id="46c5e-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="46c5e-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="46c5e-122">Header</span></span><br/>  | <dl> <span data-ttu-id="46c5e-123"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="46c5e-123"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="46c5e-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="46c5e-124">Library</span></span><br/> | <dl> <span data-ttu-id="46c5e-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="46c5e-125"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="46c5e-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="46c5e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46c5e-127">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="46c5e-127">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 




