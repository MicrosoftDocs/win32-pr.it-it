---
title: Struttura IPX_NEXT_HOP_ADDRESS (RTM. h)
description: La \_ struttura dell' \_ indirizzo hop successivo IPX \_ contiene l'indirizzo del router di hop successivo per una route IPX.
ms.assetid: 079e3284-6238-4bcf-a17f-68ff86775f18
keywords:
- RAS struttura IPX_NEXT_HOP_ADDRESS
- RAS puntatore alla struttura PIPX_NEXT_HOP_ADDRESS
topic_type:
- apiref
api_name:
- IPX_NEXT_HOP_ADDRESS
api_location:
- Rtm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99c3eb135f1d87050cd190fe47d0088fd1ab86f6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475058"
---
# <a name="ipx_next_hop_address-structure"></a>\_Struttura dell' \_ indirizzo hop successivo \_ IPX

\[Questa API è stata sostituita dall'API di [Gestione tabelle di routing versione 2](about-routing-table-manager-version-2.md) e non sarà disponibile oltre Windows Server 2003. Le applicazioni devono usare l'API di Routing Table Manager versione 2.\]

La struttura dell' **\_ \_ \_ indirizzo hop successivo IPX** contiene l'indirizzo del router di hop successivo per una route IPX.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _IPX_NEXT_HOP_ADDRESS {
  BYTE NHA_Mac[6];
} IPX_NEXT_HOP_ADDRESS, *PIPX_NEXT_HOP_ADDRESS;
```



## <a name="members"></a>Members

<dl> <dt>

**\_Mac Nha**
</dt> <dd>

Specifica l'indirizzo MAC del router di hop successivo.

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

[**\_Route IPX \_ RTM**](rtm-ipx-route.md)
</dt> </dl>

 

 





