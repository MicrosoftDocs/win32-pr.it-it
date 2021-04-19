---
description: La struttura PF followt \_ definisce i protocolli che possono precedere o seguire un protocollo.
ms.assetid: ef444af9-edae-4547-9548-8a682c279f08
title: Struttura PF_FOLLOWSET (Netmon. h)
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
ms.openlocfilehash: f5c286d3b137df24f7da7f0fc5ae269a7a3d946d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314173"
---
# <a name="pf_followset-structure"></a>\_Struttura PF follower

La **struttura \_ PF** followt definisce i protocolli che possono precedere o seguire un protocollo.

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

Matrice di strutture [PF \_ FOLLOWENTRY](pf-followentry.md) che descrivono ogni protocollo.

</dd> </dl>

## <a name="remarks"></a>Commenti

La struttura [PF \_ PARSERINFO](pf-parserinfo.md) usa la struttura **PF \_ follower** per elencare i protocolli che possono precedere o seguire il protocollo rilevato dal parser.

Network Monitor usa le informazioni contenute nella **struttura \_ PF** follower per aggiornare i set di parser specifici. La struttura **PF \_ followt** deve essere allocata mediante **HeapAlloc**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[PF \_ FOLLOWENTRY](pf-followentry.md)
</dt> <dt>

[PF \_ PARSERINFO](pf-parserinfo.md)
</dt> </dl>

 

 




