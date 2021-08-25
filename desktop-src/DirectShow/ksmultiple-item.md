---
description: La struttura KSMULTIPLE ITEM descrive le dimensioni e il conteggio delle proprietà a lunghezza variabile \_ nei pin in modalità kernel.
ms.assetid: aedbf7bc-393d-4ab5-afcd-d8822b925f07
title: KSMULTIPLE_ITEM struttura (Ks.h)
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
ms.openlocfilehash: 2e1cdf3d8edcea88fbcfb260d87d3e79d62eb2aebc57144ae38defb018065f1a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119823311"
---
# <a name="ksmultiple_item-structure"></a>Struttura ITEM KSMULTIPLE \_

La `KSMULTIPLE_ITEM` struttura descrive le dimensioni e il conteggio delle proprietà a lunghezza variabile nei pin in modalità kernel.

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

Dimensioni del blocco di memoria restituito, in byte. Le dimensioni includono la **struttura KSMULTIPLE \_ ITEM** e gli elementi che la seguono.

</dd> <dt>

**Count**
</dt> <dd>

Specifica il numero totale di elementi che seguono questa struttura.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Ks.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[DirectShow Strutture](directshow-structures.md)
</dt> <dt>

[**IKsPin::KsQueryMediums**](ikspin-ksquerymediums.md)
</dt> <dt>

[**REGPINMEDIUM**](/windows/desktop/api/strmif/ns-strmif-regpinmedium)
</dt> </dl>

 

 




