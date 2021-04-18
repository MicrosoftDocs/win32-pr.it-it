---
description: La struttura ADDRESSPAIR costruisce un filtro di acquisizione.
ms.assetid: 0dd2bcaa-5e0f-448f-969e-14b923a01a2f
title: Struttura ADDRESSPAIR (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ADDRESSPAIR
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 7960a8bb1c3ed1b2fc86c93f371b2f05d299b97b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314187"
---
# <a name="addresspair-structure"></a>Struttura ADDRESSPAIR

La struttura **ADDRESSPAIR** costruisce un filtro di acquisizione.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _ADDRESSPAIR {
  WORD    AddressFlags;
  WORD    NalReserved;
  ADDRESS DstAddress;
  ADDRESS SrcAddress;
} ADDRESSPAIR, *LPADDRESSPAIR;
```



## <a name="members"></a>Members

<dl> <dt>

**AddressFlags**
</dt> <dd>

Flag che descrivono gli indirizzi utilizzati da un filtro di acquisizione. Per ulteriori informazioni, vedere la sezione Osservazioni.



| Valore                                                                                                                                                                                                         | Significato                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <span id="ADDRESS_FLAGS_MATCH_DST"></span><span id="address_flags_match_dst"></span><dl> <dt>**flag di indirizzo \_ \_ corrispondenti all' \_ ora legale**</dt> </dl>                 | Corrisponde all'indirizzo di destinazione.<br/>                              |
| <span id="ADDRESS_FLAGS_MATCH_SRC"></span><span id="address_flags_match_src"></span><dl> <dt>**flag di indirizzo \_ \_ corrispondenti a \_ src**</dt> </dl>                 | Corrisponde all'indirizzo di origine.<br/>                                   |
| <span id="ADDRESS_FLAGS_EXCLUDED"></span><span id="address_flags_excluded"></span><dl> <dt>**flag di indirizzo \_ \_ esclusi**</dt> </dl>                     | Esclude il frame se viene trovato questo indirizzo.<br/>                  |
| <span id="ADDRESS_FLAGS_DST_GROUP_ADDR"></span><span id="address_flags_dst_group_addr"></span><dl> <dt>**INDIRIZZI \_ flag \_ del \_ gruppo \_ di indirizzi DST**</dt> </dl> | Corrisponde solo al bit del gruppo. Usare questa per i messaggi di tipo broadcast.<br/> |
| <span id="ADDRESS_FLAGS_MATCH_BOTH"></span><span id="address_flags_match_both"></span><dl> <dt>**i \_ flag di indirizzo \_ corrispondono a \_ entrambi**</dt> </dl>              | Corrisponde a indirizzi di destinazione e di origine.<br/>                     |



 

</dd> <dt>

**NalReserved**
</dt> <dd>

Questa operazione è riservata.

</dd> <dt>

**DstAddress**
</dt> <dd>

Indirizzo di destinazione dell'elemento della coppia di indirizzi.

</dd> <dt>

**SrcAddress**
</dt> <dd>

Indirizzo di origine dell'elemento della coppia di indirizzi.

</dd> </dl>

## <a name="remarks"></a>Commenti

I flag del membro **AddressFlags** possono essere combinati. Ad esempio, l'impostazione seguente esclude il frame se viene rilevato l'indirizzo di origine specificato.

``` syntax
ADDRESS_FLAGS_MATCH_SOURCE|ADDRESS_FLAGS_EXCLUDED
```

Per ulteriori informazioni sull'implementazione di questa struttura, vedere [Capture filters](capture-filters.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[CAPTUREFILTER](capturefilter.md)
</dt> </dl>

 

 




