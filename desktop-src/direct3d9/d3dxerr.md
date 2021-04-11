---
description: Gli errori sono rappresentati da valori negativi e non possono essere combinati.
ms.assetid: 2318278e-e1e1-4cd8-a5ce-5c99f3bc47ba
title: Enumerazione D3DXERR (D3dx9. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _D3DXERR
api_type:
- HeaderDef
api_location:
- d3dx9.h
ms.openlocfilehash: 0d4ef0fddf70effd63a0fcdc42b46889a879c13a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235021"
---
# <a name="d3dxerr-enumeration"></a><span data-ttu-id="278a1-103">Enumerazione D3DXERR</span><span class="sxs-lookup"><span data-stu-id="278a1-103">D3DXERR enumeration</span></span>

<span data-ttu-id="278a1-104">Gli errori sono rappresentati da valori negativi e non possono essere combinati.</span><span class="sxs-lookup"><span data-stu-id="278a1-104">Errors are represented by negative values and cannot be combined.</span></span> <span data-ttu-id="278a1-105">Di seguito è riportato un elenco di valori che possono essere restituiti dai metodi inclusi nella libreria dell'utilità D3DX.</span><span class="sxs-lookup"><span data-stu-id="278a1-105">The following is a list of values that can be returned by methods included with the D3DX utility library.</span></span> <span data-ttu-id="278a1-106">Vedere le descrizioni dei singoli metodi per gli elenchi dei valori che ognuno può restituire.</span><span class="sxs-lookup"><span data-stu-id="278a1-106">See the individual method descriptions for lists of the values that each can return.</span></span> <span data-ttu-id="278a1-107">Questi elenchi non sono necessariamente completi.</span><span class="sxs-lookup"><span data-stu-id="278a1-107">These lists are not necessarily comprehensive.</span></span>

## <a name="syntax"></a><span data-ttu-id="278a1-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="278a1-108">Syntax</span></span>


```C++
enum _D3DXERR {
  D3DXERR_CANNOTMODIFYINDEXBUFFER, 
  D3DXERR_INVALIDMESH, 
  D3DXERR_CANNOTATTRSORT, 
  D3DXERR_SKINNINGNOTSUPPORTED, 
  D3DXERR_TOOMANYINFLUENCES, 
  D3DXERR_INVALIDDATA, 
  D3DXERR_LOADEDMESHASNODATA, 
  D3DXERR_DUPLICATENAMEDFRAGMENT, 
  D3DXERR_CANNOTREMOVELASTITEM 

};
```



## <a name="constants"></a><span data-ttu-id="278a1-109">Costanti</span><span class="sxs-lookup"><span data-stu-id="278a1-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="278a1-110"><span id="D3DXERR_CANNOTMODIFYINDEXBUFFER"></span><span id="d3dxerr_cannotmodifyindexbuffer"></span>**\_CANNOTMODIFYINDEXBUFFER D3DXERR**</span><span class="sxs-lookup"><span data-stu-id="278a1-110"><span id="D3DXERR_CANNOTMODIFYINDEXBUFFER"></span><span id="d3dxerr_cannotmodifyindexbuffer"></span>**D3DXERR\_CANNOTMODIFYINDEXBUFFER**</span></span>
</dt> <dd>

<span data-ttu-id="278a1-111">Il buffer dell'indice non può essere modificato.</span><span class="sxs-lookup"><span data-stu-id="278a1-111">The index buffer cannot be modified.</span></span>

</dd> <dt>

<span data-ttu-id="278a1-112"><span id="D3DXERR_INVALIDMESH"></span><span id="d3dxerr_invalidmesh"></span>**\_INVALIDMESH D3DXERR**</span><span class="sxs-lookup"><span data-stu-id="278a1-112"><span id="D3DXERR_INVALIDMESH"></span><span id="d3dxerr_invalidmesh"></span>**D3DXERR\_INVALIDMESH**</span></span>
</dt> <dd>

<span data-ttu-id="278a1-113">Mesh non valido.</span><span class="sxs-lookup"><span data-stu-id="278a1-113">The mesh is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="278a1-114"><span id="D3DXERR_CANNOTATTRSORT"></span><span id="d3dxerr_cannotattrsort"></span>**\_CANNOTATTRSORT D3DXERR**</span><span class="sxs-lookup"><span data-stu-id="278a1-114"><span id="D3DXERR_CANNOTATTRSORT"></span><span id="d3dxerr_cannotattrsort"></span>**D3DXERR\_CANNOTATTRSORT**</span></span>
</dt> <dd>

<span data-ttu-id="278a1-115">L'ordinamento degli attributi (D3DXMESHOPT \_ ATTRSORT) non è supportato come tecnica di ottimizzazione.</span><span class="sxs-lookup"><span data-stu-id="278a1-115">Attribute sort (D3DXMESHOPT\_ATTRSORT) is not supported as an optimization technique.</span></span>

</dd> <dt>

<span data-ttu-id="278a1-116"><span id="D3DXERR_SKINNINGNOTSUPPORTED"></span><span id="d3dxerr_skinningnotsupported"></span>**\_SKINNINGNOTSUPPORTED D3DXERR**</span><span class="sxs-lookup"><span data-stu-id="278a1-116"><span id="D3DXERR_SKINNINGNOTSUPPORTED"></span><span id="d3dxerr_skinningnotsupported"></span>**D3DXERR\_SKINNINGNOTSUPPORTED**</span></span>
</dt> <dd>

<span data-ttu-id="278a1-117">La skining non è supportata.</span><span class="sxs-lookup"><span data-stu-id="278a1-117">Skinning is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="278a1-118"><span id="D3DXERR_TOOMANYINFLUENCES"></span><span id="d3dxerr_toomanyinfluences"></span>**\_TOOMANYINFLUENCES D3DXERR**</span><span class="sxs-lookup"><span data-stu-id="278a1-118"><span id="D3DXERR_TOOMANYINFLUENCES"></span><span id="d3dxerr_toomanyinfluences"></span>**D3DXERR\_TOOMANYINFLUENCES**</span></span>
</dt> <dd>

<span data-ttu-id="278a1-119">Troppe influenze specificate.</span><span class="sxs-lookup"><span data-stu-id="278a1-119">Too many influences specified.</span></span>

</dd> <dt>

<span data-ttu-id="278a1-120"><span id="D3DXERR_INVALIDDATA"></span><span id="d3dxerr_invaliddata"></span>**\_INVALIDDATA D3DXERR**</span><span class="sxs-lookup"><span data-stu-id="278a1-120"><span id="D3DXERR_INVALIDDATA"></span><span id="d3dxerr_invaliddata"></span>**D3DXERR\_INVALIDDATA**</span></span>
</dt> <dd>

<span data-ttu-id="278a1-121">I dati non sono validi.</span><span class="sxs-lookup"><span data-stu-id="278a1-121">The data is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="278a1-122"><span id="D3DXERR_LOADEDMESHASNODATA"></span><span id="d3dxerr_loadedmeshasnodata"></span>**\_LOADEDMESHASNODATA D3DXERR**</span><span class="sxs-lookup"><span data-stu-id="278a1-122"><span id="D3DXERR_LOADEDMESHASNODATA"></span><span id="d3dxerr_loadedmeshasnodata"></span>**D3DXERR\_LOADEDMESHASNODATA**</span></span>
</dt> <dd>

<span data-ttu-id="278a1-123">La mesh non contiene dati.</span><span class="sxs-lookup"><span data-stu-id="278a1-123">The mesh has no data.</span></span>

</dd> <dt>

<span data-ttu-id="278a1-124"><span id="D3DXERR_DUPLICATENAMEDFRAGMENT"></span><span id="d3dxerr_duplicatenamedfragment"></span>**\_DUPLICATENAMEDFRAGMENT D3DXERR**</span><span class="sxs-lookup"><span data-stu-id="278a1-124"><span id="D3DXERR_DUPLICATENAMEDFRAGMENT"></span><span id="d3dxerr_duplicatenamedfragment"></span>**D3DXERR\_DUPLICATENAMEDFRAGMENT**</span></span>
</dt> <dd>

<span data-ttu-id="278a1-125">Un frammento con lo stesso nome esiste già.</span><span class="sxs-lookup"><span data-stu-id="278a1-125">A fragment with that name already exists.</span></span>

</dd> <dt>

<span data-ttu-id="278a1-126"><span id="D3DXERR_CANNOTREMOVELASTITEM"></span><span id="d3dxerr_cannotremovelastitem"></span>**\_CANNOTREMOVELASTITEM D3DXERR**</span><span class="sxs-lookup"><span data-stu-id="278a1-126"><span id="D3DXERR_CANNOTREMOVELASTITEM"></span><span id="d3dxerr_cannotremovelastitem"></span>**D3DXERR\_CANNOTREMOVELASTITEM**</span></span>
</dt> <dd>

<span data-ttu-id="278a1-127">Non è possibile eliminare l'ultimo elemento.</span><span class="sxs-lookup"><span data-stu-id="278a1-127">The last item cannot be deleted.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="278a1-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="278a1-128">Remarks</span></span>

<span data-ttu-id="278a1-129">Il codice \_ di struttura FACDD viene usato per generare codici di errore, come nelle macro seguenti.</span><span class="sxs-lookup"><span data-stu-id="278a1-129">The facility code \_FACDD is used to generate error codes, as in the following macros.</span></span>


```
#define _FACDD                  0x876
#define MAKE_DDHRESULT( code )  MAKE_HRESULT( 1, _FACDD, code )
enum _D3DXERR {
    D3DXERR_CANNOTMODIFYINDEXBUFFER = MAKE_DDHRESULT(2900),
    D3DXERR_INVALIDMESH             = MAKE_DDHRESULT(2901),
    ...
    };
```



## <a name="requirements"></a><span data-ttu-id="278a1-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="278a1-130">Requirements</span></span>



| <span data-ttu-id="278a1-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="278a1-131">Requirement</span></span> | <span data-ttu-id="278a1-132">Valore</span><span class="sxs-lookup"><span data-stu-id="278a1-132">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="278a1-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="278a1-133">Header</span></span><br/> | <dl> <span data-ttu-id="278a1-134"><dt>D3dx9. h</dt></span><span class="sxs-lookup"><span data-stu-id="278a1-134"><dt>D3dx9.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="278a1-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="278a1-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="278a1-136">Enumerazioni D3DX</span><span class="sxs-lookup"><span data-stu-id="278a1-136">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




