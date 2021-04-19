---
description: Ottiene l'handle di un'annotazione.
ms.assetid: 433d73b7-9371-4d76-8b34-a64c608eb1a3
title: 'Metodo ID3DXBaseEffect:: GetAnnotation (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetAnnotation
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: aad446e436478c8c7673a1919879983437fd9602
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323614"
---
# <a name="id3dxbaseeffectgetannotation-method"></a><span data-ttu-id="b18c8-103">Metodo ID3DXBaseEffect:: GetAnnotation</span><span class="sxs-lookup"><span data-stu-id="b18c8-103">ID3DXBaseEffect::GetAnnotation method</span></span>

<span data-ttu-id="b18c8-104">Ottiene l'handle di un'annotazione.</span><span class="sxs-lookup"><span data-stu-id="b18c8-104">Gets the handle of an annotation.</span></span>

## <a name="syntax"></a><span data-ttu-id="b18c8-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b18c8-105">Syntax</span></span>


```C++
D3DXHANDLE GetAnnotation(
  [in] D3DXHANDLE hObject,
  [in] UINT       Index
);
```



## <a name="parameters"></a><span data-ttu-id="b18c8-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b18c8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b18c8-107">*hObject* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b18c8-107">*hObject* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b18c8-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="b18c8-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="b18c8-109">Handle di una tecnica, un passaggio o un parametro di primo livello.</span><span class="sxs-lookup"><span data-stu-id="b18c8-109">Handle of a technique, pass, or top-level parameter.</span></span> <span data-ttu-id="b18c8-110">Vedere [handle (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="b18c8-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="b18c8-111">*Indice* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="b18c8-111">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b18c8-112">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b18c8-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b18c8-113">Indice delle annotazioni.</span><span class="sxs-lookup"><span data-stu-id="b18c8-113">Annotation index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b18c8-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b18c8-114">Return value</span></span>

<span data-ttu-id="b18c8-115">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="b18c8-115">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="b18c8-116">Restituisce l'handle dell'annotazione specificata o **null** se l'indice non è valido.</span><span class="sxs-lookup"><span data-stu-id="b18c8-116">Returns the handle of the specified annotation, or **NULL** if the index was invalid.</span></span> <span data-ttu-id="b18c8-117">Vedere [handle (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="b18c8-117">See [Handles (Direct3D 9)](handles.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b18c8-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="b18c8-118">Remarks</span></span>

<span data-ttu-id="b18c8-119">Le annotazioni sono dati specifici dell'utente che possono essere collegati a qualsiasi tecnica, passaggio o parametro.</span><span class="sxs-lookup"><span data-stu-id="b18c8-119">Annotations are user-specific data that can be attached to any technique, pass, or parameter.</span></span> <span data-ttu-id="b18c8-120">Vedere [handle (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="b18c8-120">See [Handles (Direct3D 9)](handles.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b18c8-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b18c8-121">Requirements</span></span>



| <span data-ttu-id="b18c8-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="b18c8-122">Requirement</span></span> | <span data-ttu-id="b18c8-123">Valore</span><span class="sxs-lookup"><span data-stu-id="b18c8-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b18c8-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b18c8-124">Header</span></span><br/>  | <dl> <span data-ttu-id="b18c8-125"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="b18c8-125"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="b18c8-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="b18c8-126">Library</span></span><br/> | <dl> <span data-ttu-id="b18c8-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b18c8-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="b18c8-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b18c8-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b18c8-129">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="b18c8-129">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 
