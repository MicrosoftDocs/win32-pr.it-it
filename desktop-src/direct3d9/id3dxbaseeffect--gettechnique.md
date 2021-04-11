---
description: Ottiene l'handle di una tecnica.
ms.assetid: da139706-734b-4d5e-896d-52f045942218
title: 'Metodo ID3DXBaseEffect:: gettechnique (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetTechnique
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 4f0c82c301a48eb939d182062240c4dba6d3fc63
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104132406"
---
# <a name="id3dxbaseeffectgettechnique-method"></a><span data-ttu-id="ae84a-103">Metodo ID3DXBaseEffect:: gettechnique</span><span class="sxs-lookup"><span data-stu-id="ae84a-103">ID3DXBaseEffect::GetTechnique method</span></span>

<span data-ttu-id="ae84a-104">Ottiene l'handle di una tecnica.</span><span class="sxs-lookup"><span data-stu-id="ae84a-104">Gets the handle of a technique.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae84a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ae84a-105">Syntax</span></span>


```C++
D3DXHANDLE GetTechnique(
  [in] UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="ae84a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ae84a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae84a-107">*Indice* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="ae84a-107">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae84a-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ae84a-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ae84a-109">Indice di tecnica.</span><span class="sxs-lookup"><span data-stu-id="ae84a-109">Technique index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ae84a-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ae84a-110">Return value</span></span>

<span data-ttu-id="ae84a-111">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="ae84a-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="ae84a-112">Restituisce l'handle della tecnica specificata o **null** se l'indice non è valido.</span><span class="sxs-lookup"><span data-stu-id="ae84a-112">Returns the handle of the specified technique, or **NULL** if the index was invalid.</span></span> <span data-ttu-id="ae84a-113">Vedere [handle (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="ae84a-113">See [Handles (Direct3D 9)](handles.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ae84a-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ae84a-114">Requirements</span></span>



| <span data-ttu-id="ae84a-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="ae84a-115">Requirement</span></span> | <span data-ttu-id="ae84a-116">Valore</span><span class="sxs-lookup"><span data-stu-id="ae84a-116">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae84a-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ae84a-117">Header</span></span><br/>  | <dl> <span data-ttu-id="ae84a-118"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="ae84a-118"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="ae84a-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="ae84a-119">Library</span></span><br/> | <dl> <span data-ttu-id="ae84a-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ae84a-120"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="ae84a-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ae84a-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae84a-122">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="ae84a-122">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 
