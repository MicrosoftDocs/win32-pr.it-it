---
description: 'Metodo ID3DXTextureShader::GetConstantByName : ottiene una costante cercandone il nome.'
ms.assetid: 0c57f6ce-ea81-4b34-9251-c385bfe6ebe7
title: Metodo ID3DXTextureShader::GetConstantByName (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.GetConstantByName
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 825aca3f3227a340952092985f4730018fe316e5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117659"
---
# <a name="id3dxtextureshadergetconstantbyname-method"></a><span data-ttu-id="7637b-103">Metodo ID3DXTextureShader::GetConstantByName</span><span class="sxs-lookup"><span data-stu-id="7637b-103">ID3DXTextureShader::GetConstantByName method</span></span>

<span data-ttu-id="7637b-104">Ottiene una costante cercandone il nome.</span><span class="sxs-lookup"><span data-stu-id="7637b-104">Gets a constant by looking up its name.</span></span>

## <a name="syntax"></a><span data-ttu-id="7637b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7637b-105">Syntax</span></span>


```C++
D3DXHANDLE GetConstantByName(
  [in] D3DXHANDLE hConstant,
  [in] LPCSTR     pName
);
```



## <a name="parameters"></a><span data-ttu-id="7637b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="7637b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7637b-107">*hConstant* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="7637b-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7637b-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="7637b-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="7637b-109">Handle [per](handles.md) la struttura dei dati padre.</span><span class="sxs-lookup"><span data-stu-id="7637b-109">A [handle](handles.md) to the parent data structure.</span></span> <span data-ttu-id="7637b-110">Se la costante è un parametro di primo livello (non esiste una struttura di dati padre), usare **NULL.**</span><span class="sxs-lookup"><span data-stu-id="7637b-110">If the constant is a top-level parameter (there is no parent data structure), use **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="7637b-111">*pName* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="7637b-111">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7637b-112">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7637b-112">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7637b-113">Stringa contenente il nome della costante.</span><span class="sxs-lookup"><span data-stu-id="7637b-113">A string containing the name of the constant.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7637b-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7637b-114">Return value</span></span>

<span data-ttu-id="7637b-115">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="7637b-115">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="7637b-116">Restituisce un identificatore univoco alla costante.</span><span class="sxs-lookup"><span data-stu-id="7637b-116">Returns a unique identifier to the constant.</span></span>

## <a name="requirements"></a><span data-ttu-id="7637b-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7637b-117">Requirements</span></span>



| <span data-ttu-id="7637b-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="7637b-118">Requirement</span></span> | <span data-ttu-id="7637b-119">Valore</span><span class="sxs-lookup"><span data-stu-id="7637b-119">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="7637b-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7637b-120">Header</span></span><br/>  | <dl> <span data-ttu-id="7637b-121"><dt>D3DX9Shader.h</dt></span><span class="sxs-lookup"><span data-stu-id="7637b-121"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="7637b-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="7637b-122">Library</span></span><br/> | <dl> <span data-ttu-id="7637b-123"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="7637b-123"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="7637b-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7637b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7637b-125">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="7637b-125">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 
