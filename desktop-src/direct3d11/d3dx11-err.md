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
# <a name="d3dx11_err-enumeration"></a>\_Enumerazione D3DX11 Err

> [!Note]  
> La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.

 

Gli errori sono rappresentati da valori negativi e non possono essere combinati. Di seguito è riportato un elenco di valori che possono essere restituiti dai metodi inclusi nella libreria dell'utilità D3DX. Vedere le descrizioni dei singoli metodi per gli elenchi dei valori che ognuno può restituire. Questi elenchi non sono necessariamente completi.

## <a name="syntax"></a>Sintassi


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



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="D3DX11_ERR_CANNOT_MODIFY_INDEX_BUFFER"></span><span id="d3dx11_err_cannot_modify_index_buffer"></span>**D3DX11 \_ Err \_ non può \_ modificare il \_ buffer di indice \_**
</dt> <dd>

Il buffer dell'indice non può essere modificato.

</dd> <dt>

<span id="D3DX11_ERR_INVALID_MESH"></span><span id="d3dx11_err_invalid_mesh"></span>**\_Mesh D3DX11 ERR \_ non valida \_**
</dt> <dd>

Mesh non valido.

</dd> <dt>

<span id="D3DX11_ERR_CANNOT_ATTR_SORT"></span><span id="d3dx11_err_cannot_attr_sort"></span>**D3DX11 \_ Err \_ non può eseguire l' \_ \_ ordinamento attr**
</dt> <dd>

L'ordinamento degli attributi (D3DXMESHOPT \_ ATTRSORT) non è supportato come tecnica di ottimizzazione.

</dd> <dt>

<span id="D3DX11_ERR_SKINNING_NOT_SUPPORTED"></span><span id="d3dx11_err_skinning_not_supported"></span>**D3DX11 \_ errore di \_ Skinning \_ non \_ supportato**
</dt> <dd>

La skining non è supportata.

</dd> <dt>

<span id="D3DX11_ERR_TOO_MANY_INFLUENCES"></span><span id="d3dx11_err_too_many_influences"></span>**D3DX11 \_ Err \_ troppe \_ \_ influenze**
</dt> <dd>

Troppe influenze specificate.

</dd> <dt>

<span id="D3DX11_ERR_INVALID_DATA"></span><span id="d3dx11_err_invalid_data"></span>**D3DX11 \_ Err \_ dati non validi \_**
</dt> <dd>

I dati non sono validi.

</dd> <dt>

<span id="D3DX11_ERR_LOADED_MESH_HAS_NO_DATA"></span><span id="d3dx11_err_loaded_mesh_has_no_data"></span>**La \_ \_ mesh D3DX11 \_ con caricamento ERR \_ \_ non contiene \_ dati**
</dt> <dd>

La mesh non contiene dati.

</dd> <dt>

<span id="D3DX11_ERR_DUPLICATE_NAMED_FRAGMENT"></span><span id="d3dx11_err_duplicate_named_fragment"></span>**\_ \_ Frammento denominato D3DX11 Err duplicato \_ \_**
</dt> <dd>

Un frammento con lo stesso nome esiste già.

</dd> <dt>

<span id="D3DX11_ERR_CANNOT_REMOVE_LAST_ITEM"></span><span id="d3dx11_err_cannot_remove_last_item"></span>**D3DX11 \_ Err \_ non può \_ rimuovere \_ l'ultimo \_ elemento**
</dt> <dd>

Non è possibile eliminare l'ultimo elemento.

</dd> </dl>

## <a name="remarks"></a>Commenti

Il codice \_ di struttura FACDD viene usato per generare codici di errore, come nelle macro seguenti.


```
#define _FACDD                  0x876
#define MAKE_DDHRESULT( code )  MAKE_HRESULT( 1, _FACDD, code )
enum _D3DXERR {
    D3DXERR_CANNOTMODIFYINDEXBUFFER = MAKE_DDHRESULT(2900),
    D3DXERR_INVALIDMESH             = MAKE_DDHRESULT(2901),
    ...
    };
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3DX11. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Enumerazioni D3DX](d3d11-graphics-reference-d3dx11-enums.md)
</dt> </dl>

 

 





