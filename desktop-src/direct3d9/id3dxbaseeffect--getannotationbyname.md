---
description: Ottiene l'handle di un'annotazione cercandone il nome.
ms.assetid: da4e2805-5f06-4a9b-836f-85a8c154c502
title: 'Metodo ID3DXBaseEffect:: GetAnnotationByName (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetAnnotationByName
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 00698030488b8f4ae788367f87b8d569476292ca
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323613"
---
# <a name="id3dxbaseeffectgetannotationbyname-method"></a><span data-ttu-id="2163a-103">Metodo ID3DXBaseEffect:: GetAnnotationByName</span><span class="sxs-lookup"><span data-stu-id="2163a-103">ID3DXBaseEffect::GetAnnotationByName method</span></span>

<span data-ttu-id="2163a-104">Ottiene l'handle di un'annotazione cercandone il nome.</span><span class="sxs-lookup"><span data-stu-id="2163a-104">Gets the handle of an annotation by looking up its name.</span></span>

## <a name="syntax"></a><span data-ttu-id="2163a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2163a-105">Syntax</span></span>


```C++
D3DXHANDLE GetAnnotationByName(
  [in] D3DXHANDLE hObject,
  [in] LPCSTR     pName
);
```



## <a name="parameters"></a><span data-ttu-id="2163a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="2163a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2163a-107">*hObject* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2163a-107">*hObject* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2163a-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="2163a-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="2163a-109">Handle di una tecnica, un passaggio o un parametro di primo livello.</span><span class="sxs-lookup"><span data-stu-id="2163a-109">Handle of a technique, pass, or top-level parameter.</span></span> <span data-ttu-id="2163a-110">Vedere [handle (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="2163a-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="2163a-111">*pname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2163a-111">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2163a-112">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2163a-112">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2163a-113">Stringa contenente il nome dell'annotazione.</span><span class="sxs-lookup"><span data-stu-id="2163a-113">String containing the annotation name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2163a-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2163a-114">Return value</span></span>

<span data-ttu-id="2163a-115">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="2163a-115">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="2163a-116">Restituisce l'handle dell'annotazione specificata o **null** se il nome non è stato trovato.</span><span class="sxs-lookup"><span data-stu-id="2163a-116">Returns the handle of the specified annotation, or **NULL** if the name was not found.</span></span> <span data-ttu-id="2163a-117">Vedere [handle (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="2163a-117">See [Handles (Direct3D 9)](handles.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2163a-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2163a-118">Requirements</span></span>



| <span data-ttu-id="2163a-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="2163a-119">Requirement</span></span> | <span data-ttu-id="2163a-120">Valore</span><span class="sxs-lookup"><span data-stu-id="2163a-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2163a-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2163a-121">Header</span></span><br/>  | <dl> <span data-ttu-id="2163a-122"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="2163a-122"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="2163a-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="2163a-123">Library</span></span><br/> | <dl> <span data-ttu-id="2163a-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2163a-124"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="2163a-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2163a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2163a-126">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="2163a-126">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 
