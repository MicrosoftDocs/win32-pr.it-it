---
description: 'D3DX10_ERR enumerazione : gli errori sono rappresentati da valori negativi e non possono essere combinati.'
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
ms.openlocfilehash: b2611bb343801bbe2bd6572f250a7f0eb6d9df7b9980445f1045ee89bee23203
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119753571"
---
# <a name="d3dx10_err-enumeration"></a>Enumerazione D3DX10 \_ ERR

Gli errori sono rappresentati da valori negativi e non possono essere combinati. Di seguito è riportato un elenco di valori che possono essere restituiti dai metodi inclusi nella libreria di utilità D3DX. Vedere le descrizioni dei singoli metodi per gli elenchi dei valori che ognuno può restituire. Questi elenchi non sono necessariamente completi.

## <a name="syntax"></a>Sintassi


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



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="D3DX10_ERR_CANNOT_MODIFY_INDEX_BUFFER"></span><span id="d3dx10_err_cannot_modify_index_buffer"></span>**D3DX10 \_ ERR \_ NON PUÒ MODIFICARE IL BUFFER \_ \_ \_ DELL'INDICE**
</dt> <dd>

Il index buffer non può essere modificato.

</dd> <dt>

<span id="D3DX10_ERR_INVALID_MESH"></span><span id="d3dx10_err_invalid_mesh"></span>**MESH D3DX10 \_ ERR \_ NON \_ VALIDA**
</dt> <dd>

La mesh non è valida.

</dd> <dt>

<span id="D3DX10_ERR_CANNOT_ATTR_SORT"></span><span id="d3dx10_err_cannot_attr_sort"></span>**D3DX10 \_ ERR \_ NON PUÒ \_ ORDINARE \_ ATTR**
</dt> <dd>

L'ordinamento degli attributi (D3DXMESHOPT \_ ATTRSORT) non è supportato come tecnica di ottimizzazione.

</dd> <dt>

<span id="D3DX10_ERR_SKINNING_NOT_SUPPORTED"></span><span id="d3dx10_err_skinning_not_supported"></span>**INTERFACCIA D3DX10 \_ ERR \_ NON \_ \_ SUPPORTATA**
</dt> <dd>

L'interfaccia non è supportata.

</dd> <dt>

<span id="D3DX10_ERR_TOO_MANY_INFLUENCES"></span><span id="d3dx10_err_too_many_influences"></span>**D3DX10 ERR TOO MANY INFLUENCES (D3DX10 \_ ERR \_ TROPPI FATTORI \_ DI \_ INFLUENZA)**
</dt> <dd>

Troppi fattori specificati.

</dd> <dt>

<span id="D3DX10_ERR_INVALID_DATA"></span><span id="d3dx10_err_invalid_data"></span>**DATI NON VALIDI D3DX10 \_ ERR \_ \_**
</dt> <dd>

I dati non sono validi.

</dd> <dt>

<span id="D3DX10_ERR_LOADED_MESH_HAS_NO_DATA"></span><span id="d3dx10_err_loaded_mesh_has_no_data"></span>**LA MESH CARICATA D3DX10 \_ ERR \_ NON CONTIENE \_ \_ \_ \_ DATI**
</dt> <dd>

La mesh non contiene dati.

</dd> <dt>

<span id="D3DX10_ERR_DUPLICATE_NAMED_FRAGMENT"></span><span id="d3dx10_err_duplicate_named_fragment"></span>**D3DX10 \_ ERR \_ DUPLICATE \_ NAMED \_ FRAGMENT**
</dt> <dd>

Esiste già un frammento con tale nome.

</dd> <dt>

<span id="D3DX10_ERR_CANNOT_REMOVE_LAST_ITEM"></span><span id="d3dx10_err_cannot_remove_last_item"></span>**D3DX10 \_ ERR \_ NON PUÒ RIMUOVERE \_ \_ L'ULTIMO \_ ELEMENTO**
</dt> <dd>

L'ultimo elemento non può essere eliminato.

</dd> </dl>

## <a name="remarks"></a>Commenti

Il codice \_ di struttura FACDD viene usato per generare i codici di errore, come nelle macro seguenti.


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
| Intestazione<br/> | <dl> <dt>D3DX10.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Enumerazioni D3DX](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 




