---
title: RTM_IP_ROUTE struttura (Rtm.h)
description: La struttura RTM \_ IP ROUTE contiene informazioni che \_ descrivono una route di proprietà della famiglia di protocolli IP.
ms.assetid: e752a4ae-a6bf-4cd3-9638-7615ff3901b7
keywords:
- RTM_IP_ROUTE struttura RAS
- PRTM_IP_ROUTE puntatore alla struttura RAS
topic_type:
- apiref
api_name:
- RTM_IP_ROUTE
api_location:
- Rtm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0fd854864dcc61397fa52df7af9419a38ac829a81382be6b6190e4cb3db41d7c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120026731"
---
# <a name="rtm_ip_route-structure"></a>Struttura DI \_ ROUTE IP \_ RTM

\[Questa API è stata sostituita dall'API Gestione tabelle di [routing versione 2](about-routing-table-manager-version-2.md) e non sarà disponibile oltre Windows Server 2003. Le applicazioni devono usare l'API Gestione tabelle di routing versione 2.\]

La **struttura RTM \_ IP \_ ROUTE** contiene informazioni che descrivono una route di proprietà della famiglia di protocolli IP.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _RTM_IP_ROUTE {
  FILETIME               RR_TimeStamp;
  DWORD                  RR_RoutingProtocol;
  DWORD                  RR_InterfaceID;
  PROTOCOL_SPECIFIC_DATA RR_ProtocolSpecificData;
  IP_NETWORK             RR_Network;
  IP_NEXT_HOP_ADDRESS    RR_NextHopAddress;
  IP_SPECIFIC_DATA       RR_FamilySpecificData;
} RTM_IP_ROUTE, *PRTM_IP_ROUTE;
```



## <a name="members"></a>Members

<dl> <dt>

**RR \_ TimeStamp**
</dt> <dd>

Specifica l'ora di creazione o ultimo aggiornamento della voce di route. Questo membro viene impostato dal gestore tabelle di routing. L'ora viene espressa come struttura FILETIME.

</dd> <dt>

**Routing \_ RRProtocol**
</dt> <dd>

Specifica il protocollo di routing che ha aggiunto la route.

</dd> <dt>

**RR \_ InterfaceID**
</dt> <dd>

Specifica l'interfaccia tramite cui è stata ottenuta la route.

</dd> <dt>

**Protocollo \_ RRSpecificData**
</dt> <dd>

Specifica una struttura [**PROTOCOL \_ SPECIFIC \_ DATA**](protocol-specific-data.md) che contiene memoria riservata ai dati specifici del protocollo di routing.

</dd> <dt>

**Rete \_ RR**
</dt> <dd>

Specifica una struttura [**DI \_ RETE IP**](ip-network.md) che contiene un indirizzo di rete IP.

</dd> <dt>

**RR \_ NextHopAddress**
</dt> <dd>

Specifica una struttura [**IP \_ NEXT HOP \_ \_ ADDRESS**](ip-next-hop-address.md) che contiene l'indirizzo del router dell'hop successivo.

</dd> <dt>

**RR \_ FamilySpecificData**
</dt> <dd>

Specifica una struttura [**IP \_ SPECIFIC \_ DATA**](ip-specific-data.md) che contiene dati specifici del protocollo IP.

</dd> </dl>

## <a name="remarks"></a>Commenti

I membri della struttura **RTM \_ IP \_ ROUTE** sono tutti **allineati con DWORD.**

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

[**INDIRIZZO \_ \_ HOP SUCCESSIVO \_ IP**](ip-next-hop-address.md)
</dt> <dt>

[**DATI \_ SPECIFICI \_ DELL'INDIRIZZO IP**](ip-specific-data.md)
</dt> </dl>

 

 





