---
description: Ottiene una costante cercandone il nome.
ms.assetid: 0c57f6ce-ea81-4b34-9251-c385bfe6ebe7
title: 'Metodo ID3DXTextureShader:: GetConstantByName (D3DX9Shader. h)'
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
ms.openlocfilehash: a285da2fa3179f91d34eda8d9ce1f622c86df15b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323360"
---
# <a name="id3dxtextureshadergetconstantbyname-method"></a><span data-ttu-id="bc8cc-103">Metodo ID3DXTextureShader:: GetConstantByName</span><span class="sxs-lookup"><span data-stu-id="bc8cc-103">ID3DXTextureShader::GetConstantByName method</span></span>

<span data-ttu-id="bc8cc-104">Ottiene una costante cercandone il nome.</span><span class="sxs-lookup"><span data-stu-id="bc8cc-104">Gets a constant by looking up its name.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc8cc-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bc8cc-105">Syntax</span></span>


```C++
D3DXHANDLE GetConstantByName(
  [in] D3DXHANDLE hConstant,
  [in] LPCSTR     pName
);
```



## <a name="parameters"></a><span data-ttu-id="bc8cc-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="bc8cc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc8cc-107">*hConstant* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bc8cc-107">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc8cc-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="bc8cc-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="bc8cc-109">[Handle](handles.md) per la struttura dei dati padre.</span><span class="sxs-lookup"><span data-stu-id="bc8cc-109">A [handle](handles.md) to the parent data structure.</span></span> <span data-ttu-id="bc8cc-110">Se la costante è un parametro di primo livello (non esiste una struttura di dati padre), usare **null**.</span><span class="sxs-lookup"><span data-stu-id="bc8cc-110">If the constant is a top-level parameter (there is no parent data structure), use **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="bc8cc-111">*pname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bc8cc-111">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc8cc-112">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bc8cc-112">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bc8cc-113">Stringa che contiene il nome della costante.</span><span class="sxs-lookup"><span data-stu-id="bc8cc-113">A string containing the name of the constant.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc8cc-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bc8cc-114">Return value</span></span>

<span data-ttu-id="bc8cc-115">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="bc8cc-115">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="bc8cc-116">Restituisce un identificatore univoco alla costante.</span><span class="sxs-lookup"><span data-stu-id="bc8cc-116">Returns a unique identifier to the constant.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc8cc-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bc8cc-117">Requirements</span></span>



| <span data-ttu-id="bc8cc-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="bc8cc-118">Requirement</span></span> | <span data-ttu-id="bc8cc-119">Valore</span><span class="sxs-lookup"><span data-stu-id="bc8cc-119">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc8cc-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bc8cc-120">Header</span></span><br/>  | <dl> <span data-ttu-id="bc8cc-121"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="bc8cc-121"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="bc8cc-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="bc8cc-122">Library</span></span><br/> | <dl> <span data-ttu-id="bc8cc-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bc8cc-123"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="bc8cc-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bc8cc-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc8cc-125">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="bc8cc-125">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 
