---
description: Ottenere una costante dalla tabella delle costanti.
ms.assetid: ebb05a09-af20-4c71-8594-940fce3a97e7
title: 'Metodo ID3DXTextureShader:: getconstantelement (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.GetConstantElement
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 44b5089b6e539a8104586e27b58388a324462b37
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235045"
---
# <a name="id3dxtextureshadergetconstantelement-method"></a><span data-ttu-id="d23ed-103">Metodo ID3DXTextureShader:: getconstantelement</span><span class="sxs-lookup"><span data-stu-id="d23ed-103">ID3DXTextureShader::GetConstantElement method</span></span>

<span data-ttu-id="d23ed-104">Ottenere una costante dalla tabella delle costanti.</span><span class="sxs-lookup"><span data-stu-id="d23ed-104">Get a constant from the constant table.</span></span>

## <a name="syntax"></a><span data-ttu-id="d23ed-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d23ed-105">Syntax</span></span>


```C++
D3DXHANDLE GetConstantElement(
  [in] D3DXHANDLE hConstant,
  [in] UINT       Index
);
```



## <a name="parameters"></a><span data-ttu-id="d23ed-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d23ed-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d23ed-107">*hConstant* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d23ed-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d23ed-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="d23ed-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="d23ed-109">[Handle](handles.md) per la matrice di costanti.</span><span class="sxs-lookup"><span data-stu-id="d23ed-109">A [handle](handles.md) to the array of constants.</span></span> <span data-ttu-id="d23ed-110">Questo valore non può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="d23ed-110">This value may not be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="d23ed-111">*Indice* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="d23ed-111">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d23ed-112">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d23ed-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d23ed-113">Indice in base zero dell'elemento nella tabella Constant.</span><span class="sxs-lookup"><span data-stu-id="d23ed-113">Zero-based index of the element in the constant table.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d23ed-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d23ed-114">Return value</span></span>

<span data-ttu-id="d23ed-115">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="d23ed-115">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="d23ed-116">Restituisce un identificatore univoco alla costante.</span><span class="sxs-lookup"><span data-stu-id="d23ed-116">Returns a unique identifier to the constant.</span></span>

## <a name="remarks"></a><span data-ttu-id="d23ed-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="d23ed-117">Remarks</span></span>

<span data-ttu-id="d23ed-118">Per ottenere una costante che non fa parte di una matrice, usare [**ID3DXTextureShader:: getconstant**](id3dxtextureshader--getconstant.md) o [**ID3DXTextureShader:: GetConstantByName**](id3dxtextureshader--getconstantbyname.md).</span><span class="sxs-lookup"><span data-stu-id="d23ed-118">To get a constant that is not part of an array, use [**ID3DXTextureShader::GetConstant**](id3dxtextureshader--getconstant.md) or [**ID3DXTextureShader::GetConstantByName**](id3dxtextureshader--getconstantbyname.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d23ed-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d23ed-119">Requirements</span></span>



| <span data-ttu-id="d23ed-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="d23ed-120">Requirement</span></span> | <span data-ttu-id="d23ed-121">Valore</span><span class="sxs-lookup"><span data-stu-id="d23ed-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d23ed-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d23ed-122">Header</span></span><br/>  | <dl> <span data-ttu-id="d23ed-123"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="d23ed-123"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="d23ed-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="d23ed-124">Library</span></span><br/> | <dl> <span data-ttu-id="d23ed-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d23ed-125"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="d23ed-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d23ed-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d23ed-127">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="d23ed-127">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 
