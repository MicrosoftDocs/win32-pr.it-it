---
description: 'Enumerazione D3DXERR: gli errori sono rappresentati da valori negativi e non possono essere combinati.'
ms.assetid: 2318278e-e1e1-4cd8-a5ce-5c99f3bc47ba
title: Enumerazione D3DXERR (D3dx9.h)
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
ms.openlocfilehash: 1c1dd03500a493b30d7c1d3bfdfdf800b65a6d82
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094306"
---
# <a name="d3dxerr-enumeration"></a><span data-ttu-id="6bb7e-103">Enumerazione D3DXERR</span><span class="sxs-lookup"><span data-stu-id="6bb7e-103">D3DXERR enumeration</span></span>

<span data-ttu-id="6bb7e-104">Gli errori sono rappresentati da valori negativi e non possono essere combinati.</span><span class="sxs-lookup"><span data-stu-id="6bb7e-104">Errors are represented by negative values and cannot be combined.</span></span> <span data-ttu-id="6bb7e-105">Di seguito è riportato un elenco di valori che possono essere restituiti dai metodi inclusi nella libreria di utilità D3DX.</span><span class="sxs-lookup"><span data-stu-id="6bb7e-105">The following is a list of values that can be returned by methods included with the D3DX utility library.</span></span> <span data-ttu-id="6bb7e-106">Vedere le descrizioni dei singoli metodi per gli elenchi dei valori che possono essere restituiti da ognuno di essi.</span><span class="sxs-lookup"><span data-stu-id="6bb7e-106">See the individual method descriptions for lists of the values that each can return.</span></span> <span data-ttu-id="6bb7e-107">Questi elenchi non sono necessariamente completi.</span><span class="sxs-lookup"><span data-stu-id="6bb7e-107">These lists are not necessarily comprehensive.</span></span>

## <a name="syntax"></a><span data-ttu-id="6bb7e-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6bb7e-108">Syntax</span></span>


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



## <a name="constants"></a><span data-ttu-id="6bb7e-109">Costanti</span><span class="sxs-lookup"><span data-stu-id="6bb7e-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="6bb7e-110"><span id="D3DXERR_CANNOTMODIFYINDEXBUFFER"></span><span id="d3dxerr_cannotmodifyindexbuffer"></span>**D3DXERR \_ CANNOTMODIFYINDEXBUFFER**</span><span class="sxs-lookup"><span data-stu-id="6bb7e-110"><span id="D3DXERR_CANNOTMODIFYINDEXBUFFER"></span><span id="d3dxerr_cannotmodifyindexbuffer"></span>**D3DXERR\_CANNOTMODIFYINDEXBUFFER**</span></span>
</dt> <dd>

<span data-ttu-id="6bb7e-111">Il index buffer non può essere modificato.</span><span class="sxs-lookup"><span data-stu-id="6bb7e-111">The index buffer cannot be modified.</span></span>

</dd> <dt>

<span data-ttu-id="6bb7e-112"><span id="D3DXERR_INVALIDMESH"></span><span id="d3dxerr_invalidmesh"></span>**D3DXERR \_ INVALIDMESH**</span><span class="sxs-lookup"><span data-stu-id="6bb7e-112"><span id="D3DXERR_INVALIDMESH"></span><span id="d3dxerr_invalidmesh"></span>**D3DXERR\_INVALIDMESH**</span></span>
</dt> <dd>

<span data-ttu-id="6bb7e-113">La mesh non è valida.</span><span class="sxs-lookup"><span data-stu-id="6bb7e-113">The mesh is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="6bb7e-114"><span id="D3DXERR_CANNOTATTRSORT"></span><span id="d3dxerr_cannotattrsort"></span>**D3DXERR \_ CANNOTATTRSORT**</span><span class="sxs-lookup"><span data-stu-id="6bb7e-114"><span id="D3DXERR_CANNOTATTRSORT"></span><span id="d3dxerr_cannotattrsort"></span>**D3DXERR\_CANNOTATTRSORT**</span></span>
</dt> <dd>

<span data-ttu-id="6bb7e-115">L'ordinamento degli attributi (D3DXMESHOPT \_ ATTRSORT) non è supportato come tecnica di ottimizzazione.</span><span class="sxs-lookup"><span data-stu-id="6bb7e-115">Attribute sort (D3DXMESHOPT\_ATTRSORT) is not supported as an optimization technique.</span></span>

</dd> <dt>

<span data-ttu-id="6bb7e-116"><span id="D3DXERR_SKINNINGNOTSUPPORTED"></span><span id="d3dxerr_skinningnotsupported"></span>**INTERFACCIA D3DXERRNOTSUPPORTED \_**</span><span class="sxs-lookup"><span data-stu-id="6bb7e-116"><span id="D3DXERR_SKINNINGNOTSUPPORTED"></span><span id="d3dxerr_skinningnotsupported"></span>**D3DXERR\_SKINNINGNOTSUPPORTED**</span></span>
</dt> <dd>

<span data-ttu-id="6bb7e-117">La skinning non è supportata.</span><span class="sxs-lookup"><span data-stu-id="6bb7e-117">Skinning is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="6bb7e-118"><span id="D3DXERR_TOOMANYINFLUENCES"></span><span id="d3dxerr_toomanyinfluences"></span>**D3DXERR \_ TOOMANYINFLUENCES**</span><span class="sxs-lookup"><span data-stu-id="6bb7e-118"><span id="D3DXERR_TOOMANYINFLUENCES"></span><span id="d3dxerr_toomanyinfluences"></span>**D3DXERR\_TOOMANYINFLUENCES**</span></span>
</dt> <dd>

<span data-ttu-id="6bb7e-119">Troppi fattori di influenza specificati.</span><span class="sxs-lookup"><span data-stu-id="6bb7e-119">Too many influences specified.</span></span>

</dd> <dt>

<span data-ttu-id="6bb7e-120"><span id="D3DXERR_INVALIDDATA"></span><span id="d3dxerr_invaliddata"></span>**D3DXERR \_ INVALIDDATA**</span><span class="sxs-lookup"><span data-stu-id="6bb7e-120"><span id="D3DXERR_INVALIDDATA"></span><span id="d3dxerr_invaliddata"></span>**D3DXERR\_INVALIDDATA**</span></span>
</dt> <dd>

<span data-ttu-id="6bb7e-121">I dati non sono validi.</span><span class="sxs-lookup"><span data-stu-id="6bb7e-121">The data is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="6bb7e-122"><span id="D3DXERR_LOADEDMESHASNODATA"></span><span id="d3dxerr_loadedmeshasnodata"></span>**D3DXERR \_ LOADEDMESHASNODATA**</span><span class="sxs-lookup"><span data-stu-id="6bb7e-122"><span id="D3DXERR_LOADEDMESHASNODATA"></span><span id="d3dxerr_loadedmeshasnodata"></span>**D3DXERR\_LOADEDMESHASNODATA**</span></span>
</dt> <dd>

<span data-ttu-id="6bb7e-123">La mesh non contiene dati.</span><span class="sxs-lookup"><span data-stu-id="6bb7e-123">The mesh has no data.</span></span>

</dd> <dt>

<span data-ttu-id="6bb7e-124"><span id="D3DXERR_DUPLICATENAMEDFRAGMENT"></span><span id="d3dxerr_duplicatenamedfragment"></span>**D3DXERR \_ DUPLICATENAMEDFRAGMENT**</span><span class="sxs-lookup"><span data-stu-id="6bb7e-124"><span id="D3DXERR_DUPLICATENAMEDFRAGMENT"></span><span id="d3dxerr_duplicatenamedfragment"></span>**D3DXERR\_DUPLICATENAMEDFRAGMENT**</span></span>
</dt> <dd>

<span data-ttu-id="6bb7e-125">Esiste già un frammento con tale nome.</span><span class="sxs-lookup"><span data-stu-id="6bb7e-125">A fragment with that name already exists.</span></span>

</dd> <dt>

<span data-ttu-id="6bb7e-126"><span id="D3DXERR_CANNOTREMOVELASTITEM"></span><span id="d3dxerr_cannotremovelastitem"></span>**D3DXERR \_ CANNOTREMOVELASTITEM**</span><span class="sxs-lookup"><span data-stu-id="6bb7e-126"><span id="D3DXERR_CANNOTREMOVELASTITEM"></span><span id="d3dxerr_cannotremovelastitem"></span>**D3DXERR\_CANNOTREMOVELASTITEM**</span></span>
</dt> <dd>

<span data-ttu-id="6bb7e-127">L'ultimo elemento non può essere eliminato.</span><span class="sxs-lookup"><span data-stu-id="6bb7e-127">The last item cannot be deleted.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6bb7e-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="6bb7e-128">Remarks</span></span>

<span data-ttu-id="6bb7e-129">Il codice \_ di struttura FACDD viene usato per generare i codici di errore, come nelle macro seguenti.</span><span class="sxs-lookup"><span data-stu-id="6bb7e-129">The facility code \_FACDD is used to generate error codes, as in the following macros.</span></span>


```
#define _FACDD                  0x876
#define MAKE_DDHRESULT( code )  MAKE_HRESULT( 1, _FACDD, code )
enum _D3DXERR {
    D3DXERR_CANNOTMODIFYINDEXBUFFER = MAKE_DDHRESULT(2900),
    D3DXERR_INVALIDMESH             = MAKE_DDHRESULT(2901),
    ...
    };
```



## <a name="requirements"></a><span data-ttu-id="6bb7e-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6bb7e-130">Requirements</span></span>



| <span data-ttu-id="6bb7e-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="6bb7e-131">Requirement</span></span> | <span data-ttu-id="6bb7e-132">Valore</span><span class="sxs-lookup"><span data-stu-id="6bb7e-132">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6bb7e-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6bb7e-133">Header</span></span><br/> | <dl> <span data-ttu-id="6bb7e-134"><dt>D3dx9.h</dt></span><span class="sxs-lookup"><span data-stu-id="6bb7e-134"><dt>D3dx9.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6bb7e-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6bb7e-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6bb7e-136">Enumerazioni D3DX</span><span class="sxs-lookup"><span data-stu-id="6bb7e-136">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




