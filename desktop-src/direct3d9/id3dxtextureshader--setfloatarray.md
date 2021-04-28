---
description: 'Metodo ID3DXTextureShader::SetFloatArray: imposta una matrice di numeri a virgola mobile.'
ms.assetid: 8e64b569-a6bf-4925-9d21-4df0b6661ee2
title: Metodo ID3DXTextureShader::SetFloatArray (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.SetFloatArray
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: bd42455e16cbfc203f76de868a82935e0e25401f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090249"
---
# <a name="id3dxtextureshadersetfloatarray-method"></a><span data-ttu-id="a709a-103">Metodo ID3DXTextureShader::SetFloatArray</span><span class="sxs-lookup"><span data-stu-id="a709a-103">ID3DXTextureShader::SetFloatArray method</span></span>

<span data-ttu-id="a709a-104">Imposta una matrice di numeri a virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="a709a-104">Sets an array of floating-point numbers.</span></span>

## <a name="syntax"></a><span data-ttu-id="a709a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a709a-105">Syntax</span></span>


```C++
HRESULT SetFloatArray(
  [in]       D3DXHANDLE hConstant,
  [in] const FLOAT      *pf,
  [in]       UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="a709a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a709a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a709a-107">*hConstant* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="a709a-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a709a-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="a709a-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="a709a-109">Identificatore univoco della matrice di costanti.</span><span class="sxs-lookup"><span data-stu-id="a709a-109">Unique identifier to the array of constants.</span></span> <span data-ttu-id="a709a-110">Vedere [D3DXHANDLE](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="a709a-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="a709a-111">*pf* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="a709a-111">*pf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a709a-112">Tipo: **const [**FLOAT**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="a709a-112">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="a709a-113">Matrice di numeri a virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="a709a-113">Array of floating-point numbers.</span></span>

</dd> <dt>

<span data-ttu-id="a709a-114">*Conteggio* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="a709a-114">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a709a-115">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a709a-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a709a-116">Numero di valori a virgola mobile nella matrice.</span><span class="sxs-lookup"><span data-stu-id="a709a-116">Number of floating-point values in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a709a-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a709a-117">Return value</span></span>

<span data-ttu-id="a709a-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a709a-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a709a-119">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a709a-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="a709a-120">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="a709a-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="a709a-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a709a-121">Requirements</span></span>



| <span data-ttu-id="a709a-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="a709a-122">Requirement</span></span> | <span data-ttu-id="a709a-123">Valore</span><span class="sxs-lookup"><span data-stu-id="a709a-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a709a-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a709a-124">Header</span></span><br/>  | <dl> <span data-ttu-id="a709a-125"><dt>D3DX9Shader.h</dt></span><span class="sxs-lookup"><span data-stu-id="a709a-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="a709a-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="a709a-126">Library</span></span><br/> | <dl> <span data-ttu-id="a709a-127"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="a709a-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="a709a-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a709a-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a709a-129">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="a709a-129">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 
