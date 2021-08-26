---
description: La struttura PF \_ FOLLOWSET definisce i protocolli che possono precedere o seguire un protocollo.
ms.assetid: ef444af9-edae-4547-9548-8a682c279f08
title: PF_FOLLOWSET struttura (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PF_FOLLOWSET
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: d404e602e78452a38343a6e62fce8c5b16941270eaa2825de8339f583c064a8b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120036831"
---
# <a name="pf_followset-structure"></a>Struttura PF \_ FOLLOWSET

La **struttura PF \_ FOLLOWSET** definisce i protocolli che possono precedere o seguire un protocollo.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _PF_FOLLOWSET {
  DWORD          nEntries;
  PF_FOLLOWENTRY Entry[];
} PF_FOLLOWSET, *PPF_FOLLOWSET;
```



## <a name="members"></a>Members

<dl> <dt>

**nEntries**
</dt> <dd>

Numero di protocolli nell'elenco.

</dd> <dt>

**Voce**
</dt> <dd>

Matrice di [strutture PF \_ FOLLOWENTRY](pf-followentry.md) che descrivono ogni protocollo.

</dd> </dl>

## <a name="remarks"></a>Commenti

La [struttura PF \_ PARSERINFO](pf-parserinfo.md) usa la struttura **PF \_ FOLLOWSET** per elencare i protocolli che possono precedere o seguire il protocollo rilevato dal parser.

Network Monitor usa le informazioni nella struttura **PF \_ FOLLOWSET** per aggiornare i set di parser specifici. La **struttura PF \_ FOLLOWSET** deve essere allocata usando **HeapAlloc**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[PF \_ FOLLOWENTRY](pf-followentry.md)
</dt> <dt>

[PF \_ PARSERINFO](pf-parserinfo.md)
</dt> </dl>

 

 




