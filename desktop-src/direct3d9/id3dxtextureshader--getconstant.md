---
description: Ottiene una costante cercando il relativo indice.
ms.assetid: 7d3ab655-b50d-41ab-a4ca-c7b534e00e3f
title: 'Metodo ID3DXTextureShader:: getconstant (D3DX9Shader. h)'
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
ms.openlocfilehash: 24f3f78d5970d5e3beda119ca40a565f45d0d950
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323362"
---
# <a name="id3dxtextureshadergetconstant-method"></a><span data-ttu-id="d333e-103">Metodo ID3DXTextureShader:: getconstant</span><span class="sxs-lookup"><span data-stu-id="d333e-103">ID3DXTextureShader::GetConstant method</span></span>

<span data-ttu-id="d333e-104">Ottiene una costante cercando il relativo indice.</span><span class="sxs-lookup"><span data-stu-id="d333e-104">Gets a constant by looking up its index.</span></span>

## <a name="syntax"></a><span data-ttu-id="d333e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d333e-105">Syntax</span></span>


```C++
D3DXHANDLE GetConstant(
  [in] D3DXHANDLE hConstant,
  [in] UINT       Index
);
```



## <a name="parameters"></a><span data-ttu-id="d333e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d333e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d333e-107">*hConstant* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d333e-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d333e-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="d333e-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="d333e-109">[Handle](handles.md) per la struttura dei dati padre.</span><span class="sxs-lookup"><span data-stu-id="d333e-109">A [handle](handles.md) to the parent data structure.</span></span> <span data-ttu-id="d333e-110">Se la costante è un parametro di primo livello (non esiste una struttura di dati padre), usare **null**.</span><span class="sxs-lookup"><span data-stu-id="d333e-110">If the constant is a top-level parameter (there is no parent data structure), use **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="d333e-111">*Indice* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="d333e-111">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d333e-112">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d333e-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d333e-113">Indice in base zero della costante.</span><span class="sxs-lookup"><span data-stu-id="d333e-113">Zero-based index of the constant.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d333e-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d333e-114">Return value</span></span>

<span data-ttu-id="d333e-115">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="d333e-115">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="d333e-116">Restituisce un identificatore univoco alla costante.</span><span class="sxs-lookup"><span data-stu-id="d333e-116">Returns a unique identifier to the constant.</span></span>

## <a name="remarks"></a><span data-ttu-id="d333e-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="d333e-117">Remarks</span></span>

<span data-ttu-id="d333e-118">Per ottenere una costante da una matrice di costanti, usare [**ID3DXTextureShader:: Getconstantelement**](id3dxtextureshader--getconstantelement.md).</span><span class="sxs-lookup"><span data-stu-id="d333e-118">To get a constant from an array of constants, use [**ID3DXTextureShader::GetConstantElement**](id3dxtextureshader--getconstantelement.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d333e-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d333e-119">Requirements</span></span>



| <span data-ttu-id="d333e-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="d333e-120">Requirement</span></span> | <span data-ttu-id="d333e-121">Valore</span><span class="sxs-lookup"><span data-stu-id="d333e-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d333e-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d333e-122">Header</span></span><br/>  | <dl> <span data-ttu-id="d333e-123"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="d333e-123"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="d333e-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="d333e-124">Library</span></span><br/> | <dl> <span data-ttu-id="d333e-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d333e-125"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="d333e-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d333e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d333e-127">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="d333e-127">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 
