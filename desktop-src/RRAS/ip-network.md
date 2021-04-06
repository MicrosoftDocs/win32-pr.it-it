---
title: Struttura IP_NETWORK (RTM. h)
description: La \_ struttura di rete IP descrive un indirizzo di rete IP.
ms.assetid: 5dcc733f-c86f-407e-8727-64f3ae71dd48
keywords:
- RAS struttura IP_NETWORK
- RAS puntatore alla struttura PIP_NETWORK
topic_type:
- apiref
api_name:
- IP_NETWORK
api_location:
- Rtm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2541c493b1b2e3805e3705c71e890c6a6aaa98ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742479"
---
# <a name="ip_network-structure"></a>\_Struttura di rete IP

\[Questa API è stata sostituita dall'API di [Gestione tabelle di routing versione 2](about-routing-table-manager-version-2.md) e non sarà disponibile oltre Windows Server 2003. Le applicazioni devono usare l'API di Routing Table Manager versione 2.\]

La struttura di **\_ rete IP** descrive un indirizzo di rete IP.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _IP_NETWORK {
  DWORD N_NetNumber;
  DWORD N_NetMask;
} IP_NETWORK, *PIP_NETWORK;
```



## <a name="members"></a>Members

<dl> <dt>

**N \_ NetNumber**
</dt> <dd>

Specifica il numero di rete IP espresso come indirizzo IP nell'ordine dei byte del computer.

</dd> <dt>

**Netmask N \_**
</dt> <dd>

Specifica il network mask. Applicare questa maschera all'indirizzo IP per estrarre l'indirizzo di rete. Il network mask è nell'ordine dei byte del computer.

</dd> </dl>

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

[**\_route IP \_ RTM**](rtm-ip-route.md)
</dt> </dl>

 

 





