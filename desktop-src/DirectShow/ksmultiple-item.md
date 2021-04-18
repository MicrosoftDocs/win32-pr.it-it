---
description: La \_ struttura dell'elemento KSMULTIPLE descrive le dimensioni e il numero di proprietà a lunghezza variabile nei pin della modalità kernel.
ms.assetid: aedbf7bc-393d-4ab5-afcd-d8822b925f07
title: Struttura KSMULTIPLE_ITEM (KS. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KSMULTIPLE_ITEM
api_type:
- HeaderDef
api_location:
- ks.h
ms.openlocfilehash: 62e26b1aa8804514588e66c1d02e1f0643e97bcb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330393"
---
# <a name="ksmultiple_item-structure"></a>\_Struttura dell'elemento KSMULTIPLE

La `KSMULTIPLE_ITEM` struttura descrive le dimensioni e il numero di proprietà a lunghezza variabile nei pin della modalità kernel.

## <a name="syntax"></a>Sintassi


```C++
typedef struct {
  ULONG Size;
  ULONG Count;
} KSMULTIPLE_ITEM, *PKSMULTIPLE_ITEM;
```



## <a name="members"></a>Members

<dl> <dt>

**Dimensioni**
</dt> <dd>

Dimensioni in byte del blocco di memoria restituito. La dimensione include la struttura dell' **\_ elemento KSMULTIPLE** e gli elementi che lo seguono.

</dd> <dt>

**Count**
</dt> <dd>

Specifica il numero totale di elementi che seguono la struttura.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>KS. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture DirectShow](directshow-structures.md)
</dt> <dt>

[**IKsPin::KsQueryMediums**](ikspin-ksquerymediums.md)
</dt> <dt>

[**REGPINMEDIUM**](/windows/desktop/api/strmif/ns-strmif-regpinmedium)
</dt> </dl>

 

 




