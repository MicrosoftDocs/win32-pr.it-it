---
description: Imposta una matrice di numeri interi.
ms.assetid: 1ceb8bb0-d168-49cf-8964-8ae582b5ec2e
title: 'Metodo ID3DXTextureShader:: SetIntArray (D3DX9Shader. h)'
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
ms.openlocfilehash: d2e43ac1451ec776339d7aba1a4b0288e948f43d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322784"
---
# <a name="id3dxtextureshadersetintarray-method"></a><span data-ttu-id="2ff97-103">Metodo ID3DXTextureShader:: SetIntArray</span><span class="sxs-lookup"><span data-stu-id="2ff97-103">ID3DXTextureShader::SetIntArray method</span></span>

<span data-ttu-id="2ff97-104">Imposta una matrice di numeri interi.</span><span class="sxs-lookup"><span data-stu-id="2ff97-104">Sets an array of integers.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ff97-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2ff97-105">Syntax</span></span>


```C++
HRESULT SetIntArray(
  [in]       D3DXHANDLE hConstant,
  [in] const INT        *pn,
  [in]       UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="2ff97-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="2ff97-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ff97-107">*hConstant* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2ff97-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ff97-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="2ff97-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="2ff97-109">Identificatore univoco della matrice di costanti.</span><span class="sxs-lookup"><span data-stu-id="2ff97-109">Unique identifier to the array of constants.</span></span> <span data-ttu-id="2ff97-110">Vedere [D3DXHANDLE](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="2ff97-110">See [D3DXHANDLE](d3dxfx.md).</span></span>

</dd> <dt>

<span data-ttu-id="2ff97-111">*PN* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2ff97-111">*pn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ff97-112">Tipo: **const [**int**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="2ff97-112">Type: **const [**INT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="2ff97-113">Matrice di numeri interi.</span><span class="sxs-lookup"><span data-stu-id="2ff97-113">Array of integers.</span></span>

</dd> <dt>

<span data-ttu-id="2ff97-114">*Numero* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="2ff97-114">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ff97-115">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2ff97-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2ff97-116">Numero di numeri interi nella matrice.</span><span class="sxs-lookup"><span data-stu-id="2ff97-116">Number of integers in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ff97-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2ff97-117">Return value</span></span>

<span data-ttu-id="2ff97-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2ff97-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2ff97-119">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="2ff97-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="2ff97-120">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="2ff97-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ff97-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2ff97-121">Requirements</span></span>



| <span data-ttu-id="2ff97-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="2ff97-122">Requirement</span></span> | <span data-ttu-id="2ff97-123">Valore</span><span class="sxs-lookup"><span data-stu-id="2ff97-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ff97-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2ff97-124">Header</span></span><br/>  | <dl> <span data-ttu-id="2ff97-125"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="2ff97-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="2ff97-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="2ff97-126">Library</span></span><br/> | <dl> <span data-ttu-id="2ff97-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2ff97-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="2ff97-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2ff97-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ff97-129">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="2ff97-129">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 
