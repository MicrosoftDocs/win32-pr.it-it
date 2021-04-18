---
description: Restituisce l'indice del campionatore.
ms.assetid: vs|directx_sdk|~\id3dxconstanttable__getsamplerindex.htm
title: 'Metodo ID3DXConstantTable:: GetSamplerIndex (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.GetSamplerIndex
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f803b6e129ac20b8a22ed2393ab941698c02d3d1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322821"
---
# <a name="id3dxconstanttablegetsamplerindex-method"></a><span data-ttu-id="5c9ad-103">Metodo ID3DXConstantTable:: GetSamplerIndex</span><span class="sxs-lookup"><span data-stu-id="5c9ad-103">ID3DXConstantTable::GetSamplerIndex method</span></span>

<span data-ttu-id="5c9ad-104">Restituisce l'indice del campionatore.</span><span class="sxs-lookup"><span data-stu-id="5c9ad-104">Returns the sampler index.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c9ad-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5c9ad-105">Syntax</span></span>


```C++
UINT GetSamplerIndex(
  [out] D3DXHANDLE hConstant
);
```



## <a name="parameters"></a><span data-ttu-id="5c9ad-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="5c9ad-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c9ad-107">*hConstant* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="5c9ad-107">*hConstant* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5c9ad-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="5c9ad-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="5c9ad-109">Handle del campionatore.</span><span class="sxs-lookup"><span data-stu-id="5c9ad-109">The sampler handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5c9ad-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5c9ad-110">Return value</span></span>

<span data-ttu-id="5c9ad-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5c9ad-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5c9ad-112">Restituisce il numero di indice del campionatore dalla tabella delle costanti.</span><span class="sxs-lookup"><span data-stu-id="5c9ad-112">Returns the sampler index number from the constant table.</span></span>

## <a name="requirements"></a><span data-ttu-id="5c9ad-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5c9ad-113">Requirements</span></span>



| <span data-ttu-id="5c9ad-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="5c9ad-114">Requirement</span></span> | <span data-ttu-id="5c9ad-115">Valore</span><span class="sxs-lookup"><span data-stu-id="5c9ad-115">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c9ad-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5c9ad-116">Header</span></span><br/>  | <dl> <span data-ttu-id="5c9ad-117"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="5c9ad-117"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="5c9ad-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="5c9ad-118">Library</span></span><br/> | <dl> <span data-ttu-id="5c9ad-119"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5c9ad-119"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="5c9ad-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5c9ad-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c9ad-121">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="5c9ad-121">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
