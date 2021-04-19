---
description: Ottiene l'handle di un oggetto pass cercandone il nome.
ms.assetid: 24d043a2-5c87-4a59-80d4-0c81bd7a0b3e
title: 'Metodo ID3DXBaseEffect:: GetPassByName (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetPassByName
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 2cd96a9d91f0e822b3e869bd8f0c965f0f951f44
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323591"
---
# <a name="id3dxbaseeffectgetpassbyname-method"></a><span data-ttu-id="43a3a-103">Metodo ID3DXBaseEffect:: GetPassByName</span><span class="sxs-lookup"><span data-stu-id="43a3a-103">ID3DXBaseEffect::GetPassByName method</span></span>

<span data-ttu-id="43a3a-104">Ottiene l'handle di un oggetto pass cercandone il nome.</span><span class="sxs-lookup"><span data-stu-id="43a3a-104">Gets the handle of a pass by looking up its name.</span></span>

## <a name="syntax"></a><span data-ttu-id="43a3a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="43a3a-105">Syntax</span></span>


```C++
D3DXHANDLE GetPassByName(
  [in] D3DXHANDLE hTechnique,
  [in] LPCSTR     pName
);
```



## <a name="parameters"></a><span data-ttu-id="43a3a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="43a3a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43a3a-107">*hTechnique* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="43a3a-107">*hTechnique* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43a3a-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="43a3a-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="43a3a-109">Handle della tecnica padre.</span><span class="sxs-lookup"><span data-stu-id="43a3a-109">Handle of the parent technique.</span></span> <span data-ttu-id="43a3a-110">Vedere [handle (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="43a3a-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="43a3a-111">*pname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="43a3a-111">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43a3a-112">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="43a3a-112">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="43a3a-113">Stringa contenente il nome del passaggio.</span><span class="sxs-lookup"><span data-stu-id="43a3a-113">String containing the pass name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43a3a-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="43a3a-114">Return value</span></span>

<span data-ttu-id="43a3a-115">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="43a3a-115">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="43a3a-116">Restituisce l'handle del primo passaggio all'interno della tecnica specificata con il nome specificato o **null** se il nome non è stato trovato.</span><span class="sxs-lookup"><span data-stu-id="43a3a-116">Returns the handle of the first pass inside the specified technique that has the specified name, or **NULL** if the name was not found.</span></span> <span data-ttu-id="43a3a-117">Vedere [handle (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="43a3a-117">See [Handles (Direct3D 9)](handles.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="43a3a-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="43a3a-118">Requirements</span></span>



| <span data-ttu-id="43a3a-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="43a3a-119">Requirement</span></span> | <span data-ttu-id="43a3a-120">Valore</span><span class="sxs-lookup"><span data-stu-id="43a3a-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="43a3a-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="43a3a-121">Header</span></span><br/>  | <dl> <span data-ttu-id="43a3a-122"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="43a3a-122"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="43a3a-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="43a3a-123">Library</span></span><br/> | <dl> <span data-ttu-id="43a3a-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="43a3a-124"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="43a3a-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="43a3a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43a3a-126">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="43a3a-126">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 
