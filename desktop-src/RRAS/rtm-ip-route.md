---
title: Struttura RTM_IP_ROUTE (RTM. h)
description: La \_ struttura della \_ route IP RTM contiene informazioni che descrivono una route di proprietà della famiglia di protocolli IP.
ms.assetid: e752a4ae-a6bf-4cd3-9638-7615ff3901b7
keywords:
- RAS struttura RTM_IP_ROUTE
- RAS puntatore alla struttura PRTM_IP_ROUTE
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
ms.openlocfilehash: 1978503a3ec37e0c39716569030d5ea6599e19d9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302704"
---
# <a name="rtm_ip_route-structure"></a>\_Struttura della \_ route IP RTM

\[Questa API è stata sostituita dall'API di [Gestione tabelle di routing versione 2](about-routing-table-manager-version-2.md) e non sarà disponibile oltre Windows Server 2003. Le applicazioni devono usare l'API di Routing Table Manager versione 2.\]

La struttura della **\_ \_ route IP RTM** contiene informazioni che descrivono una route di proprietà della famiglia di protocolli IP.

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

**\_Timestamp RR**
</dt> <dd>

Specifica l'ora di creazione o dell'ultimo aggiornamento della voce della route. Questo membro viene impostato da Gestione tabelle di routing. Il tempo viene espresso come una struttura FILETIME.

</dd> <dt>

**\_ROUTINGPROTOCOL RR**
</dt> <dd>

Specifica il protocollo di routing che ha aggiunto la route.

</dd> <dt>

**\_INTERFACEID RR**
</dt> <dd>

Specifica l'interfaccia tramite la quale è stata ottenuta la route.

</dd> <dt>

**\_PROTOCOLSPECIFICDATA RR**
</dt> <dd>

Specifica una struttura di [**\_ \_ dati specifica del protocollo**](protocol-specific-data.md) che contiene memoria riservata per i dati specifici del protocollo di routing.

</dd> <dt>

**\_Rete RR**
</dt> <dd>

Specifica una struttura di [**\_ rete IP**](ip-network.md) che contiene un indirizzo di rete IP.

</dd> <dt>

**\_NEXTHOPADDRESS RR**
</dt> <dd>

Specifica una struttura dell' [**\_ \_ \_ indirizzo di hop successivo IP**](ip-next-hop-address.md) che contiene l'indirizzo del router di hop successivo.

</dd> <dt>

**\_FAMILYSPECIFICDATA RR**
</dt> <dd>

Specifica una struttura di [**\_ \_ dati specifica dell'IP**](ip-specific-data.md) che contiene dati specifici della famiglia di protocolli IP.

</dd> </dl>

## <a name="remarks"></a>Commenti

I membri della struttura **della \_ \_ route IP RTM** sono tutti allineati a **DWORD** .

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

[**\_ \_ indirizzo hop successivo \_ IP**](ip-next-hop-address.md)
</dt> <dt>

[**\_dati specifici \_ IP**](ip-specific-data.md)
</dt> </dl>

 

 





