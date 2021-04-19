---
description: Ottiene l'handle di una tecnica cercandone il nome.
ms.assetid: 34871229-ad63-4575-8c60-f27d7f7dddce
title: 'Metodo ID3DXBaseEffect:: GetTechniqueByName (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetTechniqueByName
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 5827527bf5151b121958c3f5803ef8a7e74f8d60
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323587"
---
# <a name="id3dxbaseeffectgettechniquebyname-method"></a><span data-ttu-id="a204e-103">Metodo ID3DXBaseEffect:: GetTechniqueByName</span><span class="sxs-lookup"><span data-stu-id="a204e-103">ID3DXBaseEffect::GetTechniqueByName method</span></span>

<span data-ttu-id="a204e-104">Ottiene l'handle di una tecnica cercandone il nome.</span><span class="sxs-lookup"><span data-stu-id="a204e-104">Gets the handle of a technique by looking up its name.</span></span>

## <a name="syntax"></a><span data-ttu-id="a204e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a204e-105">Syntax</span></span>


```C++
D3DXHANDLE GetTechniqueByName(
  [in] LPCSTR pName
);
```



## <a name="parameters"></a><span data-ttu-id="a204e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a204e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a204e-107">*pname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a204e-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a204e-108">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a204e-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a204e-109">Stringa contenente il nome della tecnica.</span><span class="sxs-lookup"><span data-stu-id="a204e-109">String containing the technique name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a204e-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a204e-110">Return value</span></span>

<span data-ttu-id="a204e-111">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="a204e-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="a204e-112">Restituisce l'handle della prima tecnica con il nome specificato o **null** se il nome non è stato trovato.</span><span class="sxs-lookup"><span data-stu-id="a204e-112">Returns the handle of the first technique that has the specified name, or **NULL** if the name was not found.</span></span> <span data-ttu-id="a204e-113">Vedere [handle (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="a204e-113">See [Handles (Direct3D 9)](handles.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a204e-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a204e-114">Requirements</span></span>



| <span data-ttu-id="a204e-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="a204e-115">Requirement</span></span> | <span data-ttu-id="a204e-116">Valore</span><span class="sxs-lookup"><span data-stu-id="a204e-116">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a204e-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a204e-117">Header</span></span><br/>  | <dl> <span data-ttu-id="a204e-118"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="a204e-118"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="a204e-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="a204e-119">Library</span></span><br/> | <dl> <span data-ttu-id="a204e-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a204e-120"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="a204e-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a204e-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a204e-122">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="a204e-122">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 
