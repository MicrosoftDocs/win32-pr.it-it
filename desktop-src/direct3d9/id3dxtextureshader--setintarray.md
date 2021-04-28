---
description: 'Metodo ID3DXTextureShader::SetIntArray : imposta una matrice di numeri interi.'
ms.assetid: 1ceb8bb0-d168-49cf-8964-8ae582b5ec2e
title: Metodo ID3DXTextureShader::SetIntArray (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetIntArray
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0ddc00637bddf2810e73be7755a9dcfb8696053e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097489"
---
# <a name="id3dxtextureshadersetintarray-method"></a><span data-ttu-id="a6b84-103">Metodo ID3DXTextureShader::SetIntArray</span><span class="sxs-lookup"><span data-stu-id="a6b84-103">ID3DXTextureShader::SetIntArray method</span></span>

<span data-ttu-id="a6b84-104">Imposta una matrice di numeri interi.</span><span class="sxs-lookup"><span data-stu-id="a6b84-104">Sets an array of integers.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6b84-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a6b84-105">Syntax</span></span>


```C++
HRESULT SetIntArray(
  [in]       D3DXHANDLE hConstant,
  [in] const INT        *pn,
  [in]       UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="a6b84-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a6b84-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6b84-107">*hConstant* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="a6b84-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a6b84-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="a6b84-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="a6b84-109">Identificatore univoco della matrice di costanti.</span><span class="sxs-lookup"><span data-stu-id="a6b84-109">Unique identifier to the array of constants.</span></span> <span data-ttu-id="a6b84-110">Vedere [D3DXHANDLE](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="a6b84-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="a6b84-111">*pn* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="a6b84-111">*pn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a6b84-112">Tipo: **const [**INT**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="a6b84-112">Type: **const [**INT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="a6b84-113">Matrice di numeri interi.</span><span class="sxs-lookup"><span data-stu-id="a6b84-113">Array of integers.</span></span>

</dd> <dt>

<span data-ttu-id="a6b84-114">*Conteggio* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="a6b84-114">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a6b84-115">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a6b84-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a6b84-116">Numero di numeri interi nella matrice.</span><span class="sxs-lookup"><span data-stu-id="a6b84-116">Number of integers in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a6b84-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a6b84-117">Return value</span></span>

<span data-ttu-id="a6b84-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a6b84-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a6b84-119">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a6b84-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="a6b84-120">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="a6b84-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="a6b84-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a6b84-121">Requirements</span></span>



| <span data-ttu-id="a6b84-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="a6b84-122">Requirement</span></span> | <span data-ttu-id="a6b84-123">Valore</span><span class="sxs-lookup"><span data-stu-id="a6b84-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6b84-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a6b84-124">Header</span></span><br/>  | <dl> <span data-ttu-id="a6b84-125"><dt>D3DX9Shader.h</dt></span><span class="sxs-lookup"><span data-stu-id="a6b84-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="a6b84-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="a6b84-126">Library</span></span><br/> | <dl> <span data-ttu-id="a6b84-127"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="a6b84-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="a6b84-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a6b84-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6b84-129">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="a6b84-129">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 
