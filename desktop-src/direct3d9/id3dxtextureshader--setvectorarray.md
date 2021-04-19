---
description: Imposta una matrice di vettori 4D.
ms.assetid: 45bc5cb1-b44a-468b-8c80-a639da8a033f
title: 'Metodo ID3DXTextureShader:: SetVectorArray (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetVectorArray
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c91a012cda9d1aa992682b5cb5aa769bf41de180
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322546"
---
# <a name="id3dxtextureshadersetvectorarray-method"></a><span data-ttu-id="20af7-103">Metodo ID3DXTextureShader:: SetVectorArray</span><span class="sxs-lookup"><span data-stu-id="20af7-103">ID3DXTextureShader::SetVectorArray method</span></span>

<span data-ttu-id="20af7-104">Imposta una matrice di vettori 4D.</span><span class="sxs-lookup"><span data-stu-id="20af7-104">Sets an array of 4D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="20af7-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="20af7-105">Syntax</span></span>


```C++
HRESULT SetVectorArray(
  [in]       D3DXHANDLE  hConstant,
  [in] const D3DXVECTOR4 *pVector,
  [in]       UINT        Count
);
```



## <a name="parameters"></a><span data-ttu-id="20af7-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="20af7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="20af7-107">*hConstant* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="20af7-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20af7-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="20af7-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="20af7-109">Identificatore univoco della matrice di costanti vettoriali.</span><span class="sxs-lookup"><span data-stu-id="20af7-109">Unique identifier to the array of vector constants.</span></span> <span data-ttu-id="20af7-110">Vedere [D3DXHANDLE](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="20af7-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="20af7-111">*pVector* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="20af7-111">*pVector* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20af7-112">Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="20af7-112">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="20af7-113">Matrice di vettori 4D.</span><span class="sxs-lookup"><span data-stu-id="20af7-113">Array of 4D vectors.</span></span> <span data-ttu-id="20af7-114">Vedere [**D3DXVECTOR4**](d3dxvector4.md).</span><span class="sxs-lookup"><span data-stu-id="20af7-114">See [**D3DXVECTOR4**](d3dxvector4.md).</span></span>

</dd> <dt>

<span data-ttu-id="20af7-115">*Numero* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="20af7-115">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20af7-116">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="20af7-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="20af7-117">Numero di vettori nella matrice.</span><span class="sxs-lookup"><span data-stu-id="20af7-117">Number of vectors in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="20af7-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="20af7-118">Return value</span></span>

<span data-ttu-id="20af7-119">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="20af7-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="20af7-120">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="20af7-120">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="20af7-121">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="20af7-121">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="20af7-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="20af7-122">Requirements</span></span>



| <span data-ttu-id="20af7-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="20af7-123">Requirement</span></span> | <span data-ttu-id="20af7-124">Valore</span><span class="sxs-lookup"><span data-stu-id="20af7-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="20af7-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="20af7-125">Header</span></span><br/>  | <dl> <span data-ttu-id="20af7-126"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="20af7-126"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="20af7-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="20af7-127">Library</span></span><br/> | <dl> <span data-ttu-id="20af7-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="20af7-128"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="20af7-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="20af7-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20af7-130">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="20af7-130">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 
