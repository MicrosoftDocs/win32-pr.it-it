---
description: "Metodo ID3DXTextureShader::GetConstant: ottiene una costante cercandone l'indice."
ms.assetid: 7d3ab655-b50d-41ab-a4ca-c7b534e00e3f
title: Metodo ID3DXTextureShader::GetConstant (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.GetConstant
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: edcc4b6a7f34c12be7013f2ae1e0b2e6d991a5d6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117669"
---
# <a name="id3dxtextureshadergetconstant-method"></a><span data-ttu-id="6f201-103">Metodo ID3DXTextureShader::GetConstant</span><span class="sxs-lookup"><span data-stu-id="6f201-103">ID3DXTextureShader::GetConstant method</span></span>

<span data-ttu-id="6f201-104">Ottiene una costante cercandone l'indice.</span><span class="sxs-lookup"><span data-stu-id="6f201-104">Gets a constant by looking up its index.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f201-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6f201-105">Syntax</span></span>


```C++
D3DXHANDLE GetConstant(
  [in] D3DXHANDLE hConstant,
  [in] UINT       Index
);
```



## <a name="parameters"></a><span data-ttu-id="6f201-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="6f201-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f201-107">*hConstant* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="6f201-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f201-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="6f201-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="6f201-109">Handle [per](handles.md) la struttura dei dati padre.</span><span class="sxs-lookup"><span data-stu-id="6f201-109">A [handle](handles.md) to the parent data structure.</span></span> <span data-ttu-id="6f201-110">Se la costante è un parametro di primo livello (non è presente alcuna struttura di dati padre), usare **NULL.**</span><span class="sxs-lookup"><span data-stu-id="6f201-110">If the constant is a top-level parameter (there is no parent data structure), use **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="6f201-111">*Indice* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="6f201-111">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f201-112">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6f201-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6f201-113">Indice in base zero della costante.</span><span class="sxs-lookup"><span data-stu-id="6f201-113">Zero-based index of the constant.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6f201-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6f201-114">Return value</span></span>

<span data-ttu-id="6f201-115">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="6f201-115">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="6f201-116">Restituisce un identificatore univoco per la costante.</span><span class="sxs-lookup"><span data-stu-id="6f201-116">Returns a unique identifier to the constant.</span></span>

## <a name="remarks"></a><span data-ttu-id="6f201-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="6f201-117">Remarks</span></span>

<span data-ttu-id="6f201-118">Per ottenere una costante da una matrice di costanti, usare [**ID3DXTextureShader::GetConstantElement**](id3dxtextureshader--getconstantelement.md).</span><span class="sxs-lookup"><span data-stu-id="6f201-118">To get a constant from an array of constants, use [**ID3DXTextureShader::GetConstantElement**](id3dxtextureshader--getconstantelement.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6f201-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6f201-119">Requirements</span></span>



| <span data-ttu-id="6f201-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="6f201-120">Requirement</span></span> | <span data-ttu-id="6f201-121">Valore</span><span class="sxs-lookup"><span data-stu-id="6f201-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f201-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6f201-122">Header</span></span><br/>  | <dl> <span data-ttu-id="6f201-123"><dt>D3DX9Shader.h</dt></span><span class="sxs-lookup"><span data-stu-id="6f201-123"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="6f201-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="6f201-124">Library</span></span><br/> | <dl> <span data-ttu-id="6f201-125"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="6f201-125"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="6f201-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6f201-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f201-127">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="6f201-127">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 
