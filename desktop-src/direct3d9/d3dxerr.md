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
# <a name="d3dxerr-enumeration"></a>Enumerazione D3DXERR

Gli errori sono rappresentati da valori negativi e non possono essere combinati. Di seguito è riportato un elenco di valori che possono essere restituiti dai metodi inclusi nella libreria dell'utilità D3DX. Vedere le descrizioni dei singoli metodi per gli elenchi dei valori che ognuno può restituire. Questi elenchi non sono necessariamente completi.

## <a name="syntax"></a>Sintassi


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



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="D3DXERR_CANNOTMODIFYINDEXBUFFER"></span><span id="d3dxerr_cannotmodifyindexbuffer"></span>**\_CANNOTMODIFYINDEXBUFFER D3DXERR**
</dt> <dd>

Il buffer dell'indice non può essere modificato.

</dd> <dt>

<span id="D3DXERR_INVALIDMESH"></span><span id="d3dxerr_invalidmesh"></span>**\_INVALIDMESH D3DXERR**
</dt> <dd>

Mesh non valido.

</dd> <dt>

<span id="D3DXERR_CANNOTATTRSORT"></span><span id="d3dxerr_cannotattrsort"></span>**\_CANNOTATTRSORT D3DXERR**
</dt> <dd>

L'ordinamento degli attributi (D3DXMESHOPT \_ ATTRSORT) non è supportato come tecnica di ottimizzazione.

</dd> <dt>

<span id="D3DXERR_SKINNINGNOTSUPPORTED"></span><span id="d3dxerr_skinningnotsupported"></span>**\_SKINNINGNOTSUPPORTED D3DXERR**
</dt> <dd>

La skining non è supportata.

</dd> <dt>

<span id="D3DXERR_TOOMANYINFLUENCES"></span><span id="d3dxerr_toomanyinfluences"></span>**\_TOOMANYINFLUENCES D3DXERR**
</dt> <dd>

Troppe influenze specificate.

</dd> <dt>

<span id="D3DXERR_INVALIDDATA"></span><span id="d3dxerr_invaliddata"></span>**\_INVALIDDATA D3DXERR**
</dt> <dd>

I dati non sono validi.

</dd> <dt>

<span id="D3DXERR_LOADEDMESHASNODATA"></span><span id="d3dxerr_loadedmeshasnodata"></span>**\_LOADEDMESHASNODATA D3DXERR**
</dt> <dd>

La mesh non contiene dati.

</dd> <dt>

<span id="D3DXERR_DUPLICATENAMEDFRAGMENT"></span><span id="d3dxerr_duplicatenamedfragment"></span>**\_DUPLICATENAMEDFRAGMENT D3DXERR**
</dt> <dd>

Un frammento con lo stesso nome esiste già.

</dd> <dt>

<span id="D3DXERR_CANNOTREMOVELASTITEM"></span><span id="d3dxerr_cannotremovelastitem"></span>**\_CANNOTREMOVELASTITEM D3DXERR**
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
|-------------------|------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx9. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Enumerazioni D3DX](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




