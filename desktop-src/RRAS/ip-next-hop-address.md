---
title: IP_NEXT_HOP_ADDRESS (Rtm.h)
description: La struttura \_ INDIRIZZO HOP SUCCESSIVO IP contiene \_ \_ l'indirizzo per il router dell'hop successivo per una route IP.
ms.assetid: a97b3995-dfaa-4e53-be86-3ad46b8be691
keywords:
- IP_NEXT_HOP_ADDRESS struttura RAS
- PIP_NEXT_HOP_ADDRESS struttura RAS
topic_type:
- apiref
api_name:
- IP_NEXT_HOP_ADDRESS
api_location:
- Rtm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94f79b850c7d5f48e5f409e5380ad7345288187b8939b752b4f282b2274a99cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117790965"
---
# <a name="ip_next_hop_address-structure"></a>Struttura \_ IP NEXT HOP \_ \_ ADDRESS

\[Questa API è stata sostituita dall'API di Gestione tabelle di routing versione [2](about-routing-table-manager-version-2.md) e non sarà disponibile oltre Windows Server 2003. Le applicazioni devono usare l'API gestione tabelle di routing versione 2.\]

La **struttura INDIRIZZO HOP SUCCESSIVO \_ \_ \_ IP** contiene l'indirizzo per il router dell'hop successivo per una route IP.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _IP_NEXT_HOP_ADDRESS {
  DWORD N_NetNumber;
  DWORD N_NetMask;
} IP_NEXT_HOP_ADDRESS, *PIP_NEXT_HOP_ADDRESS;
```



## <a name="members"></a>Members

<dl> <dt>

**N \_ NetNumber**
</dt> <dd>

Specifica l'indirizzo di rete IP espresso come indirizzo IP nell'ordine dei byte del computer.

</dd> <dt>

**N \_ NetMask**
</dt> <dd>

Specifica la network mask. Applicare questa maschera all'indirizzo IP per estrarre l'indirizzo di rete. Il network mask è nell'ordine dei byte del computer.

</dd> </dl>

## <a name="remarks"></a>Commenti

La **struttura IP NEXT HOP \_ \_ \_ ADDRESS** è un typedef della [**struttura IP \_ NETWORK.**](ip-network.md) Il typedef si trova in Rtm.h.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                        |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Fine del supporto server<br/>    | Windows Server 2003<br/>                                                   |
| Intestazione<br/>                   | <dl> <dt>Rtm.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Informazioni di riferimento su Gestione tabelle di routing versione 1](routing-table-manager-version-1-reference.md)
</dt> <dt>

[Strutture di Gestione tabelle di routing versione 1](routing-table-manager-version-1-structures.md)
</dt> <dt>

[**RETE \_ IP**](ip-network.md)
</dt> <dt>

[**RTM \_ IP \_ ROUTE**](rtm-ip-route.md)
</dt> </dl>

 

 





