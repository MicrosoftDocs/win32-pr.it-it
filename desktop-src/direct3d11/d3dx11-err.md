---
title: Enumerazione D3DX11_ERR (D3DX11. h)
description: Nota la libreria dell'utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store. Gli errori sono rappresentati da valori negativi e non possono essere combinati.
ms.assetid: d042621d-a20b-4945-b6aa-714a451aa88a
keywords:
- Enumerazione D3DX11_ERR Direct3D 11
- Puntatore di enumerazione LPD3DX11_ERR Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_ERR
api_location:
- D3DX11.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0607bd495bad4bdeacf66ae593670dbe3ad0d2e2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996201"
---
# <a name="d3dx11_err-enumeration"></a><span data-ttu-id="f761c-106">\_Enumerazione D3DX11 Err</span><span class="sxs-lookup"><span data-stu-id="f761c-106">D3DX11\_ERR enumeration</span></span>

> [!Note]  
> <span data-ttu-id="f761c-107">La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.</span><span class="sxs-lookup"><span data-stu-id="f761c-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="f761c-108">Gli errori sono rappresentati da valori negativi e non possono essere combinati.</span><span class="sxs-lookup"><span data-stu-id="f761c-108">Errors are represented by negative values and cannot be combined.</span></span> <span data-ttu-id="f761c-109">Di seguito è riportato un elenco di valori che possono essere restituiti dai metodi inclusi nella libreria dell'utilità D3DX.</span><span class="sxs-lookup"><span data-stu-id="f761c-109">The following is a list of values that can be returned by methods included with the D3DX utility library.</span></span> <span data-ttu-id="f761c-110">Vedere le descrizioni dei singoli metodi per gli elenchi dei valori che ognuno può restituire.</span><span class="sxs-lookup"><span data-stu-id="f761c-110">See the individual method descriptions for lists of the values that each can return.</span></span> <span data-ttu-id="f761c-111">Questi elenchi non sono necessariamente completi.</span><span class="sxs-lookup"><span data-stu-id="f761c-111">These lists are not necessarily comprehensive.</span></span>

## <a name="syntax"></a><span data-ttu-id="f761c-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f761c-112">Syntax</span></span>


```C++
typedef enum D3DX11_ERR { 
  D3DX11_ERR_CANNOT_MODIFY_INDEX_BUFFER  = MAKE_DDHRESULT(2900),
  D3DX11_ERR_INVALID_MESH                = MAKE_DDHRESULT(2901),
  D3DX11_ERR_CANNOT_ATTR_SORT            = MAKE_DDHRESULT(2902),
  D3DX11_ERR_SKINNING_NOT_SUPPORTED      = MAKE_DDHRESULT(2903),
  D3DX11_ERR_TOO_MANY_INFLUENCES         = MAKE_DDHRESULT(2904),
  D3DX11_ERR_INVALID_DATA                = MAKE_DDHRESULT(2905),
  D3DX11_ERR_LOADED_MESH_HAS_NO_DATA     = MAKE_DDHRESULT(2906),
  D3DX11_ERR_DUPLICATE_NAMED_FRAGMENT    = MAKE_DDHRESULT(2907),
  D3DX11_ERR_CANNOT_REMOVE_LAST_ITEM     = MAKE_DDHRESULT(2908)
} D3DX11_ERR, *LPD3DX11_ERR;
```



## <a name="constants"></a><span data-ttu-id="f761c-113">Costanti</span><span class="sxs-lookup"><span data-stu-id="f761c-113">Constants</span></span>

<dl> <dt>

<span data-ttu-id="f761c-114"><span id="D3DX11_ERR_CANNOT_MODIFY_INDEX_BUFFER"></span><span id="d3dx11_err_cannot_modify_index_buffer"></span>**D3DX11 \_ Err \_ non può \_ modificare il \_ buffer di indice \_**</span><span class="sxs-lookup"><span data-stu-id="f761c-114"><span id="D3DX11_ERR_CANNOT_MODIFY_INDEX_BUFFER"></span><span id="d3dx11_err_cannot_modify_index_buffer"></span>**D3DX11\_ERR\_CANNOT\_MODIFY\_INDEX\_BUFFER**</span></span>
</dt> <dd>

<span data-ttu-id="f761c-115">Il buffer dell'indice non può essere modificato.</span><span class="sxs-lookup"><span data-stu-id="f761c-115">The index buffer cannot be modified.</span></span>

</dd> <dt>

<span data-ttu-id="f761c-116"><span id="D3DX11_ERR_INVALID_MESH"></span><span id="d3dx11_err_invalid_mesh"></span>**\_Mesh D3DX11 ERR \_ non valida \_**</span><span class="sxs-lookup"><span data-stu-id="f761c-116"><span id="D3DX11_ERR_INVALID_MESH"></span><span id="d3dx11_err_invalid_mesh"></span>**D3DX11\_ERR\_INVALID\_MESH**</span></span>
</dt> <dd>

<span data-ttu-id="f761c-117">Mesh non valido.</span><span class="sxs-lookup"><span data-stu-id="f761c-117">The mesh is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="f761c-118"><span id="D3DX11_ERR_CANNOT_ATTR_SORT"></span><span id="d3dx11_err_cannot_attr_sort"></span>**D3DX11 \_ Err \_ non può eseguire l' \_ \_ ordinamento attr**</span><span class="sxs-lookup"><span data-stu-id="f761c-118"><span id="D3DX11_ERR_CANNOT_ATTR_SORT"></span><span id="d3dx11_err_cannot_attr_sort"></span>**D3DX11\_ERR\_CANNOT\_ATTR\_SORT**</span></span>
</dt> <dd>

<span data-ttu-id="f761c-119">L'ordinamento degli attributi (D3DXMESHOPT \_ ATTRSORT) non è supportato come tecnica di ottimizzazione.</span><span class="sxs-lookup"><span data-stu-id="f761c-119">Attribute sort (D3DXMESHOPT\_ATTRSORT) is not supported as an optimization technique.</span></span>

</dd> <dt>

<span data-ttu-id="f761c-120"><span id="D3DX11_ERR_SKINNING_NOT_SUPPORTED"></span><span id="d3dx11_err_skinning_not_supported"></span>**D3DX11 \_ errore di \_ Skinning \_ non \_ supportato**</span><span class="sxs-lookup"><span data-stu-id="f761c-120"><span id="D3DX11_ERR_SKINNING_NOT_SUPPORTED"></span><span id="d3dx11_err_skinning_not_supported"></span>**D3DX11\_ERR\_SKINNING\_NOT\_SUPPORTED**</span></span>
</dt> <dd>

<span data-ttu-id="f761c-121">La skining non è supportata.</span><span class="sxs-lookup"><span data-stu-id="f761c-121">Skinning is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="f761c-122"><span id="D3DX11_ERR_TOO_MANY_INFLUENCES"></span><span id="d3dx11_err_too_many_influences"></span>**D3DX11 \_ Err \_ troppe \_ \_ influenze**</span><span class="sxs-lookup"><span data-stu-id="f761c-122"><span id="D3DX11_ERR_TOO_MANY_INFLUENCES"></span><span id="d3dx11_err_too_many_influences"></span>**D3DX11\_ERR\_TOO\_MANY\_INFLUENCES**</span></span>
</dt> <dd>

<span data-ttu-id="f761c-123">Troppe influenze specificate.</span><span class="sxs-lookup"><span data-stu-id="f761c-123">Too many influences specified.</span></span>

</dd> <dt>

<span data-ttu-id="f761c-124"><span id="D3DX11_ERR_INVALID_DATA"></span><span id="d3dx11_err_invalid_data"></span>**D3DX11 \_ Err \_ dati non validi \_**</span><span class="sxs-lookup"><span data-stu-id="f761c-124"><span id="D3DX11_ERR_INVALID_DATA"></span><span id="d3dx11_err_invalid_data"></span>**D3DX11\_ERR\_INVALID\_DATA**</span></span>
</dt> <dd>

<span data-ttu-id="f761c-125">I dati non sono validi.</span><span class="sxs-lookup"><span data-stu-id="f761c-125">The data is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="f761c-126"><span id="D3DX11_ERR_LOADED_MESH_HAS_NO_DATA"></span><span id="d3dx11_err_loaded_mesh_has_no_data"></span>**La \_ \_ mesh D3DX11 \_ con caricamento ERR \_ \_ non contiene \_ dati**</span><span class="sxs-lookup"><span data-stu-id="f761c-126"><span id="D3DX11_ERR_LOADED_MESH_HAS_NO_DATA"></span><span id="d3dx11_err_loaded_mesh_has_no_data"></span>**D3DX11\_ERR\_LOADED\_MESH\_HAS\_NO\_DATA**</span></span>
</dt> <dd>

<span data-ttu-id="f761c-127">La mesh non contiene dati.</span><span class="sxs-lookup"><span data-stu-id="f761c-127">The mesh has no data.</span></span>

</dd> <dt>

<span data-ttu-id="f761c-128"><span id="D3DX11_ERR_DUPLICATE_NAMED_FRAGMENT"></span><span id="d3dx11_err_duplicate_named_fragment"></span>**\_ \_ Frammento denominato D3DX11 Err duplicato \_ \_**</span><span class="sxs-lookup"><span data-stu-id="f761c-128"><span id="D3DX11_ERR_DUPLICATE_NAMED_FRAGMENT"></span><span id="d3dx11_err_duplicate_named_fragment"></span>**D3DX11\_ERR\_DUPLICATE\_NAMED\_FRAGMENT**</span></span>
</dt> <dd>

<span data-ttu-id="f761c-129">Un frammento con lo stesso nome esiste già.</span><span class="sxs-lookup"><span data-stu-id="f761c-129">A fragment with that name already exists.</span></span>

</dd> <dt>

<span data-ttu-id="f761c-130"><span id="D3DX11_ERR_CANNOT_REMOVE_LAST_ITEM"></span><span id="d3dx11_err_cannot_remove_last_item"></span>**D3DX11 \_ Err \_ non può \_ rimuovere \_ l'ultimo \_ elemento**</span><span class="sxs-lookup"><span data-stu-id="f761c-130"><span id="D3DX11_ERR_CANNOT_REMOVE_LAST_ITEM"></span><span id="d3dx11_err_cannot_remove_last_item"></span>**D3DX11\_ERR\_CANNOT\_REMOVE\_LAST\_ITEM**</span></span>
</dt> <dd>

<span data-ttu-id="f761c-131">Non è possibile eliminare l'ultimo elemento.</span><span class="sxs-lookup"><span data-stu-id="f761c-131">The last item cannot be deleted.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f761c-132">Commenti</span><span class="sxs-lookup"><span data-stu-id="f761c-132">Remarks</span></span>

<span data-ttu-id="f761c-133">Il codice \_ di struttura FACDD viene usato per generare codici di errore, come nelle macro seguenti.</span><span class="sxs-lookup"><span data-stu-id="f761c-133">The facility code \_FACDD is used to generate error codes, as in the following macros.</span></span>


```
#define _FACDD                  0x876
#define MAKE_DDHRESULT( code )  MAKE_HRESULT( 1, _FACDD, code )
enum _D3DXERR {
    D3DXERR_CANNOTMODIFYINDEXBUFFER = MAKE_DDHRESULT(2900),
    D3DXERR_INVALIDMESH             = MAKE_DDHRESULT(2901),
    ...
    };
```



## <a name="requirements"></a><span data-ttu-id="f761c-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f761c-134">Requirements</span></span>



| <span data-ttu-id="f761c-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="f761c-135">Requirement</span></span> | <span data-ttu-id="f761c-136">Valore</span><span class="sxs-lookup"><span data-stu-id="f761c-136">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="f761c-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f761c-137">Header</span></span><br/> | <dl> <span data-ttu-id="f761c-138"><dt>D3DX11. h</dt></span><span class="sxs-lookup"><span data-stu-id="f761c-138"><dt>D3DX11.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f761c-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f761c-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f761c-140">Enumerazioni D3DX</span><span class="sxs-lookup"><span data-stu-id="f761c-140">D3DX Enumerations</span></span>](d3d11-graphics-reference-d3dx11-enums.md)
</dt> </dl>

 

 





