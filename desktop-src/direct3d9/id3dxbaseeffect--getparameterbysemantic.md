---
description: Ottiene l'handle di un parametro di primo livello o di un parametro del membro della struttura cercando la relativa semantica con una ricerca senza distinzione tra maiuscole e minuscole.
ms.assetid: 3de3791a-fe09-4a39-bd6f-0e20a641dd32
title: 'Metodo ID3DXBaseEffect:: GetParameterBySemantic (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetParameterBySemantic
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: c70d30d68d73d6c4dd33d483747be4293a255693
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355879"
---
# <a name="id3dxbaseeffectgetparameterbysemantic-method"></a><span data-ttu-id="70f3a-103">Metodo ID3DXBaseEffect:: GetParameterBySemantic</span><span class="sxs-lookup"><span data-stu-id="70f3a-103">ID3DXBaseEffect::GetParameterBySemantic method</span></span>

<span data-ttu-id="70f3a-104">Ottiene l'handle di un parametro di primo livello o di un parametro del membro della struttura cercando la relativa semantica con una ricerca senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="70f3a-104">Gets the handle of a top-level parameter or a structure member parameter by looking up its semantic with a case-insensitive search.</span></span>

## <a name="syntax"></a><span data-ttu-id="70f3a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="70f3a-105">Syntax</span></span>


```C++
D3DXHANDLE GetParameterBySemantic(
  [in] D3DXHANDLE hParameter,
  [in] LPCSTR     pSemantic
);
```



## <a name="parameters"></a><span data-ttu-id="70f3a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="70f3a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="70f3a-107">*hParameter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="70f3a-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70f3a-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="70f3a-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="70f3a-109">Handle del parametro o **null** per i parametri di primo livello.</span><span class="sxs-lookup"><span data-stu-id="70f3a-109">Handle of the parameter, or **NULL** for top-level parameters.</span></span> <span data-ttu-id="70f3a-110">Vedere [handle (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="70f3a-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="70f3a-111">*pSemantic* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="70f3a-111">*pSemantic* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70f3a-112">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="70f3a-112">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="70f3a-113">Stringa contenente il nome semantico.</span><span class="sxs-lookup"><span data-stu-id="70f3a-113">String containing the semantic name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="70f3a-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="70f3a-114">Return value</span></span>

<span data-ttu-id="70f3a-115">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="70f3a-115">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="70f3a-116">Restituisce l'handle del primo parametro che corrisponde alla semantica specificata o **null** se la semantica non è stata trovata.</span><span class="sxs-lookup"><span data-stu-id="70f3a-116">Returns the handle of the first parameter that matches the specified semantic, or **NULL** if the semantic was not found.</span></span> <span data-ttu-id="70f3a-117">Vedere [handle (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="70f3a-117">See [Handles (Direct3D 9)](handles.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="70f3a-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="70f3a-118">Requirements</span></span>



| <span data-ttu-id="70f3a-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="70f3a-119">Requirement</span></span> | <span data-ttu-id="70f3a-120">Valore</span><span class="sxs-lookup"><span data-stu-id="70f3a-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="70f3a-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="70f3a-121">Header</span></span><br/>  | <dl> <span data-ttu-id="70f3a-122"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="70f3a-122"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="70f3a-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="70f3a-123">Library</span></span><br/> | <dl> <span data-ttu-id="70f3a-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="70f3a-124"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="70f3a-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="70f3a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70f3a-126">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="70f3a-126">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 
