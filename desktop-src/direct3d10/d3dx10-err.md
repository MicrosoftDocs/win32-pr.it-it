---
description: 'D3DX10_ERR enumerazione: gli errori sono rappresentati da valori negativi e non possono essere combinati.'
ms.assetid: 4149ce6d-e87a-4003-b123-5555c6b3b086
title: D3DX10_ERR enumerazione (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_ERR
api_type:
- HeaderDef
api_location:
- D3DX10.h
ms.openlocfilehash: 520abae0409dd4214106363d7ffde0cfb5c81ff1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094355"
---
# <a name="d3dx10_err-enumeration"></a><span data-ttu-id="83e5d-103">Enumerazione ERR D3DX10 \_</span><span class="sxs-lookup"><span data-stu-id="83e5d-103">D3DX10\_ERR enumeration</span></span>

<span data-ttu-id="83e5d-104">Gli errori sono rappresentati da valori negativi e non possono essere combinati.</span><span class="sxs-lookup"><span data-stu-id="83e5d-104">Errors are represented by negative values and cannot be combined.</span></span> <span data-ttu-id="83e5d-105">Di seguito è riportato un elenco di valori che possono essere restituiti dai metodi inclusi nella libreria di utilità D3DX.</span><span class="sxs-lookup"><span data-stu-id="83e5d-105">The following is a list of values that can be returned by methods included with the D3DX utility library.</span></span> <span data-ttu-id="83e5d-106">Vedere le descrizioni dei singoli metodi per gli elenchi dei valori che possono essere restituiti da ognuno di essi.</span><span class="sxs-lookup"><span data-stu-id="83e5d-106">See the individual method descriptions for lists of the values that each can return.</span></span> <span data-ttu-id="83e5d-107">Questi elenchi non sono necessariamente completi.</span><span class="sxs-lookup"><span data-stu-id="83e5d-107">These lists are not necessarily comprehensive.</span></span>

## <a name="syntax"></a><span data-ttu-id="83e5d-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="83e5d-108">Syntax</span></span>


```C++
typedef enum D3DX10_ERR { 
  D3DX10_ERR_CANNOT_MODIFY_INDEX_BUFFER  = MAKE_DDHRESULT(2900),
  D3DX10_ERR_INVALID_MESH                = MAKE_DDHRESULT(2901),
  D3DX10_ERR_CANNOT_ATTR_SORT            = MAKE_DDHRESULT(2902),
  D3DX10_ERR_SKINNING_NOT_SUPPORTED      = MAKE_DDHRESULT(2903),
  D3DX10_ERR_TOO_MANY_INFLUENCES         = MAKE_DDHRESULT(2904),
  D3DX10_ERR_INVALID_DATA                = MAKE_DDHRESULT(2905),
  D3DX10_ERR_LOADED_MESH_HAS_NO_DATA     = MAKE_DDHRESULT(2906),
  D3DX10_ERR_DUPLICATE_NAMED_FRAGMENT    = MAKE_DDHRESULT(2907),
  D3DX10_ERR_CANNOT_REMOVE_LAST_ITEM     = MAKE_DDHRESULT(2908)
} D3DX10_ERR, *LPD3DX10_ERR;
```



## <a name="constants"></a><span data-ttu-id="83e5d-109">Costanti</span><span class="sxs-lookup"><span data-stu-id="83e5d-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="83e5d-110"><span id="D3DX10_ERR_CANNOT_MODIFY_INDEX_BUFFER"></span><span id="d3dx10_err_cannot_modify_index_buffer"></span>**D3DX10 \_ ERR \_ NON PUÒ MODIFICARE IL BUFFER \_ \_ \_ DELL'INDICE**</span><span class="sxs-lookup"><span data-stu-id="83e5d-110"><span id="D3DX10_ERR_CANNOT_MODIFY_INDEX_BUFFER"></span><span id="d3dx10_err_cannot_modify_index_buffer"></span>**D3DX10\_ERR\_CANNOT\_MODIFY\_INDEX\_BUFFER**</span></span>
</dt> <dd>

<span data-ttu-id="83e5d-111">Il index buffer non può essere modificato.</span><span class="sxs-lookup"><span data-stu-id="83e5d-111">The index buffer cannot be modified.</span></span>

</dd> <dt>

<span data-ttu-id="83e5d-112"><span id="D3DX10_ERR_INVALID_MESH"></span><span id="d3dx10_err_invalid_mesh"></span>**MESH NON VALIDA D3DX10 \_ ERR \_ \_**</span><span class="sxs-lookup"><span data-stu-id="83e5d-112"><span id="D3DX10_ERR_INVALID_MESH"></span><span id="d3dx10_err_invalid_mesh"></span>**D3DX10\_ERR\_INVALID\_MESH**</span></span>
</dt> <dd>

<span data-ttu-id="83e5d-113">La mesh non è valida.</span><span class="sxs-lookup"><span data-stu-id="83e5d-113">The mesh is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="83e5d-114"><span id="D3DX10_ERR_CANNOT_ATTR_SORT"></span><span id="d3dx10_err_cannot_attr_sort"></span>**D3DX10 \_ ERR \_ NON PUÒ \_ ATTR \_ SORT**</span><span class="sxs-lookup"><span data-stu-id="83e5d-114"><span id="D3DX10_ERR_CANNOT_ATTR_SORT"></span><span id="d3dx10_err_cannot_attr_sort"></span>**D3DX10\_ERR\_CANNOT\_ATTR\_SORT**</span></span>
</dt> <dd>

<span data-ttu-id="83e5d-115">L'ordinamento degli attributi (D3DXMESHOPT \_ ATTRSORT) non è supportato come tecnica di ottimizzazione.</span><span class="sxs-lookup"><span data-stu-id="83e5d-115">Attribute sort (D3DXMESHOPT\_ATTRSORT) is not supported as an optimization technique.</span></span>

</dd> <dt>

<span data-ttu-id="83e5d-116"><span id="D3DX10_ERR_SKINNING_NOT_SUPPORTED"></span><span id="d3dx10_err_skinning_not_supported"></span>**INTERFACCIA ERR D3DX10 \_ \_ NON \_ \_ SUPPORTATA**</span><span class="sxs-lookup"><span data-stu-id="83e5d-116"><span id="D3DX10_ERR_SKINNING_NOT_SUPPORTED"></span><span id="d3dx10_err_skinning_not_supported"></span>**D3DX10\_ERR\_SKINNING\_NOT\_SUPPORTED**</span></span>
</dt> <dd>

<span data-ttu-id="83e5d-117">La skinning non è supportata.</span><span class="sxs-lookup"><span data-stu-id="83e5d-117">Skinning is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="83e5d-118"><span id="D3DX10_ERR_TOO_MANY_INFLUENCES"></span><span id="d3dx10_err_too_many_influences"></span>**D3DX10 \_ ERR \_ TROPPE \_ \_ INFLUENZE**</span><span class="sxs-lookup"><span data-stu-id="83e5d-118"><span id="D3DX10_ERR_TOO_MANY_INFLUENCES"></span><span id="d3dx10_err_too_many_influences"></span>**D3DX10\_ERR\_TOO\_MANY\_INFLUENCES**</span></span>
</dt> <dd>

<span data-ttu-id="83e5d-119">Troppi fattori di influenza specificati.</span><span class="sxs-lookup"><span data-stu-id="83e5d-119">Too many influences specified.</span></span>

</dd> <dt>

<span data-ttu-id="83e5d-120"><span id="D3DX10_ERR_INVALID_DATA"></span><span id="d3dx10_err_invalid_data"></span>**DATI NON VALIDI D3DX10 \_ ERR \_ \_**</span><span class="sxs-lookup"><span data-stu-id="83e5d-120"><span id="D3DX10_ERR_INVALID_DATA"></span><span id="d3dx10_err_invalid_data"></span>**D3DX10\_ERR\_INVALID\_DATA**</span></span>
</dt> <dd>

<span data-ttu-id="83e5d-121">I dati non sono validi.</span><span class="sxs-lookup"><span data-stu-id="83e5d-121">The data is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="83e5d-122"><span id="D3DX10_ERR_LOADED_MESH_HAS_NO_DATA"></span><span id="d3dx10_err_loaded_mesh_has_no_data"></span>**LA MESH CARICATA D3DX10 \_ ERR \_ NON CONTIENE \_ \_ \_ \_ DATI**</span><span class="sxs-lookup"><span data-stu-id="83e5d-122"><span id="D3DX10_ERR_LOADED_MESH_HAS_NO_DATA"></span><span id="d3dx10_err_loaded_mesh_has_no_data"></span>**D3DX10\_ERR\_LOADED\_MESH\_HAS\_NO\_DATA**</span></span>
</dt> <dd>

<span data-ttu-id="83e5d-123">La mesh non contiene dati.</span><span class="sxs-lookup"><span data-stu-id="83e5d-123">The mesh has no data.</span></span>

</dd> <dt>

<span data-ttu-id="83e5d-124"><span id="D3DX10_ERR_DUPLICATE_NAMED_FRAGMENT"></span><span id="d3dx10_err_duplicate_named_fragment"></span>**D3DX10 \_ ERR \_ DUPLICATE \_ NAMED \_ FRAGMENT**</span><span class="sxs-lookup"><span data-stu-id="83e5d-124"><span id="D3DX10_ERR_DUPLICATE_NAMED_FRAGMENT"></span><span id="d3dx10_err_duplicate_named_fragment"></span>**D3DX10\_ERR\_DUPLICATE\_NAMED\_FRAGMENT**</span></span>
</dt> <dd>

<span data-ttu-id="83e5d-125">Esiste già un frammento con tale nome.</span><span class="sxs-lookup"><span data-stu-id="83e5d-125">A fragment with that name already exists.</span></span>

</dd> <dt>

<span data-ttu-id="83e5d-126"><span id="D3DX10_ERR_CANNOT_REMOVE_LAST_ITEM"></span><span id="d3dx10_err_cannot_remove_last_item"></span>**D3DX10 \_ ERR \_ NON PUÒ RIMUOVERE \_ \_ L'ULTIMO \_ ELEMENTO**</span><span class="sxs-lookup"><span data-stu-id="83e5d-126"><span id="D3DX10_ERR_CANNOT_REMOVE_LAST_ITEM"></span><span id="d3dx10_err_cannot_remove_last_item"></span>**D3DX10\_ERR\_CANNOT\_REMOVE\_LAST\_ITEM**</span></span>
</dt> <dd>

<span data-ttu-id="83e5d-127">L'ultimo elemento non può essere eliminato.</span><span class="sxs-lookup"><span data-stu-id="83e5d-127">The last item cannot be deleted.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="83e5d-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="83e5d-128">Remarks</span></span>

<span data-ttu-id="83e5d-129">Il codice \_ di struttura FACDD viene usato per generare i codici di errore, come nelle macro seguenti.</span><span class="sxs-lookup"><span data-stu-id="83e5d-129">The facility code \_FACDD is used to generate error codes, as in the following macros.</span></span>


```
#define _FACDD                  0x876
#define MAKE_DDHRESULT( code )  MAKE_HRESULT( 1, _FACDD, code )
enum _D3DXERR {
    D3DXERR_CANNOTMODIFYINDEXBUFFER = MAKE_DDHRESULT(2900),
    D3DXERR_INVALIDMESH             = MAKE_DDHRESULT(2901),
    ...
    };
```



## <a name="requirements"></a><span data-ttu-id="83e5d-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="83e5d-130">Requirements</span></span>



| <span data-ttu-id="83e5d-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="83e5d-131">Requirement</span></span> | <span data-ttu-id="83e5d-132">Valore</span><span class="sxs-lookup"><span data-stu-id="83e5d-132">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="83e5d-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="83e5d-133">Header</span></span><br/> | <dl> <span data-ttu-id="83e5d-134"><dt>D3DX10.h</dt></span><span class="sxs-lookup"><span data-stu-id="83e5d-134"><dt>D3DX10.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="83e5d-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="83e5d-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83e5d-136">Enumerazioni D3DX</span><span class="sxs-lookup"><span data-stu-id="83e5d-136">D3DX Enumerations</span></span>](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 




