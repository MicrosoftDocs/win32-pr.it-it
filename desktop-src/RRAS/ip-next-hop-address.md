---
title: Struttura IP_NEXT_HOP_ADDRESS (RTM. h)
description: La \_ struttura dell' \_ indirizzo di hop successivo IP \_ contiene l'indirizzo del router di hop successivo per una route IP.
ms.assetid: a97b3995-dfaa-4e53-be86-3ad46b8be691
keywords:
- RAS struttura IP_NEXT_HOP_ADDRESS
- RAS struttura PIP_NEXT_HOP_ADDRESS
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
ms.openlocfilehash: 1818a49e7977dbb4dfa31ebac1dae7651adb8d45
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302187"
---
# <a name="ip_next_hop_address-structure"></a>\_ \_ Struttura indirizzo hop successivo IP \_

\[Questa API è stata sostituita dall'API di [Gestione tabelle di routing versione 2](about-routing-table-manager-version-2.md) e non sarà disponibile oltre Windows Server 2003. Le applicazioni devono usare l'API di Routing Table Manager versione 2.\]

La struttura dell' **\_ \_ \_ indirizzo di hop successivo IP** contiene l'indirizzo del router di hop successivo per una route IP.

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

**Netmask N \_**
</dt> <dd>

Specifica il network mask. Applicare questa maschera all'indirizzo IP per estrarre l'indirizzo di rete. Il network mask è nell'ordine dei byte del computer.

</dd> </dl>

## <a name="remarks"></a>Commenti

La struttura dell' **\_ \_ \_ indirizzo di hop successivo IP** è un typedef della struttura di [**\_ rete IP**](ip-network.md) . Il typedef è in RTM. h.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                        |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Fine del supporto server<br/>    | Windows Server 2003<br/>                                                   |
| Intestazione<br/>                   | <dl> <dt>RTM. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Riferimento di gestione tabelle di routing versione 1](routing-table-manager-version-1-reference.md)
</dt> <dt>

[Strutture di gestione tabelle di routing versione 1](routing-table-manager-version-1-structures.md)
</dt> <dt>

[**\_rete IP**](ip-network.md)
</dt> <dt>

[**\_route IP \_ RTM**](rtm-ip-route.md)
</dt> </dl>

 

 





