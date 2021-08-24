---
title: D3DX11_ERR enumerazione (D3DX11.h)
description: Nota La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store. Gli errori sono rappresentati da valori negativi e non possono essere combinati.
ms.assetid: d042621d-a20b-4945-b6aa-714a451aa88a
keywords:
- D3DX11_ERR enumerazione Direct3D 11
- LPD3DX11_ERR puntatore di enumerazione Direct3D 11
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
ms.openlocfilehash: d80b906b5b95693458eeea353f40fe446a22e8e33a6011b7851cf6d9663b3ed4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119729321"
---
# <a name="d3dx11_err-enumeration"></a>Enumerazione ERR D3DX11 \_

> [!Note]  
> La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.

 

Gli errori sono rappresentati da valori negativi e non possono essere combinati. Di seguito è riportato un elenco di valori che possono essere restituiti dai metodi inclusi nella libreria di utilità D3DX. Vedere le descrizioni dei singoli metodi per gli elenchi dei valori che ognuno può restituire. Questi elenchi non sono necessariamente completi.

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

<span id="D3DX11_ERR_CANNOT_MODIFY_INDEX_BUFFER"></span><span id="d3dx11_err_cannot_modify_index_buffer"></span>**D3DX11 \_ ERR NON PUÒ \_ MODIFICARE IL BUFFER \_ \_ \_ DELL'INDICE**
</dt> <dd>

Il index buffer non può essere modificato.

</dd> <dt>

<span id="D3DX11_ERR_INVALID_MESH"></span><span id="d3dx11_err_invalid_mesh"></span>**D3DX11 \_ ERR \_ MESH NON \_ VALIDA**
</dt> <dd>

La mesh non è valida.

</dd> <dt>

<span id="D3DX11_ERR_CANNOT_ATTR_SORT"></span><span id="d3dx11_err_cannot_attr_sort"></span>**D3DX11 \_ ERR \_ NON PUÒ \_ ATTR \_ SORT**
</dt> <dd>

L'ordinamento degli attributi (D3DXMESHOPT \_ ATTRSORT) non è supportato come tecnica di ottimizzazione.

</dd> <dt>

<span id="D3DX11_ERR_SKINNING_NOT_SUPPORTED"></span><span id="d3dx11_err_skinning_not_supported"></span>**INTERFACCIA ERR D3DX11 \_ \_ NON \_ \_ SUPPORTATA**
</dt> <dd>

La skinning non è supportata.

</dd> <dt>

<span id="D3DX11_ERR_TOO_MANY_INFLUENCES"></span><span id="d3dx11_err_too_many_influences"></span>**D3DX11 \_ ERR \_ TROPPE \_ \_ INFLUENZE**
</dt> <dd>

Troppi fattori di influenza specificati.

</dd> <dt>

<span id="D3DX11_ERR_INVALID_DATA"></span><span id="d3dx11_err_invalid_data"></span>**DATI D3DX11 \_ ERR \_ NON \_ VALIDI**
</dt> <dd>

I dati non sono validi.

</dd> <dt>

<span id="D3DX11_ERR_LOADED_MESH_HAS_NO_DATA"></span><span id="d3dx11_err_loaded_mesh_has_no_data"></span>**LA MESH CARICATA ERR D3DX11 \_ \_ NON CONTIENE \_ \_ \_ \_ DATI**
</dt> <dd>

La mesh non contiene dati.

</dd> <dt>

<span id="D3DX11_ERR_DUPLICATE_NAMED_FRAGMENT"></span><span id="d3dx11_err_duplicate_named_fragment"></span>**FRAMMENTO DENOMINATO \_ DUPLICATO D3DX11 ERR \_ \_ \_**
</dt> <dd>

Esiste già un frammento con tale nome.

</dd> <dt>

<span id="D3DX11_ERR_CANNOT_REMOVE_LAST_ITEM"></span><span id="d3dx11_err_cannot_remove_last_item"></span>**D3DX11 \_ ERR \_ NON PUÒ RIMUOVERE \_ \_ L'ULTIMO \_ ELEMENTO**
</dt> <dd>

L'ultimo elemento non può essere eliminato.

</dd> </dl>

## <a name="remarks"></a>Commenti

Il codice di struttura \_ FACDD viene usato per generare codici di errore, come nelle macro seguenti.


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
| Intestazione<br/> | <dl> <dt>D3DX11.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Enumerazioni D3DX](d3d11-graphics-reference-d3dx11-enums.md)
</dt> </dl>

 

 





