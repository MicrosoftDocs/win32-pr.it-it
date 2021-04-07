---
title: Struttura RTM_IPX_ROUTE (RTM. h)
description: La \_ \_ struttura Route IPX RTM contiene informazioni che descrivono una route per la famiglia di protocolli IPX.
ms.assetid: ffa0637c-2197-4ebd-a5ef-e174dd0ccb15
keywords:
- RAS struttura RTM_IPX_ROUTE
- RAS puntatore alla struttura PRTM_IPX_ROUTE
topic_type:
- apiref
api_name:
- RTM_IPX_ROUTE
api_location:
- Rtm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d32333dd6a6b53ee4600dda388a318bdf9404b6d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963995"
---
# <a name="rtm_ipx_route-structure"></a>\_ \_ Struttura Route IPX RTM

\[Questa API è stata sostituita dall'API di [Gestione tabelle di routing versione 2](about-routing-table-manager-version-2.md) e non sarà disponibile oltre Windows Server 2003. Le applicazioni devono usare l'API di Routing Table Manager versione 2.\]

La **struttura \_ \_ Route IPX RTM** contiene informazioni che descrivono una route per la famiglia di protocolli IPX.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _RTM_IPX_ROUTE {
  FILETIME               RR_TimeStamp;
  DWORD                  RR_RoutingProtocol;
  DWORD                  RR_InterfaceID;
  PROTOCOL_SPECIFIC_DATA RR_ProtocolSpecificData;
  IPX_NETWORK            RR_Network;
  IPX_NEXT_HOP_ADDRESS   RR_NextHopAddress;
  IPX_SPECIFIC_DATA      RR_FamilySpecificData;
} RTM_IPX_ROUTE, *PRTM_IPX_ROUTE;
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

Specifica una struttura di [**\_ \_ dati specifica del protocollo**](protocol-specific-data.md) contenente memoria riservata ai dati specifici dei protocolli di routing.

</dd> <dt>

**\_Rete RR**
</dt> <dd>

Specifica una struttura di [**\_ rete IPX**](ipx-network.md) che contiene un indirizzo di rete IP.

</dd> <dt>

**\_NEXTHOPADDRESS RR**
</dt> <dd>

Specifica una struttura dell'indirizzo di un [**\_ \_ hop \_ successivo IPX**](ipx-next-hop-address.md) che contiene l'indirizzo del router di hop successivo.

</dd> <dt>

**\_FAMILYSPECIFICDATA RR**
</dt> <dd>

Specifica una struttura di [**\_ \_ dati specifica di IPX**](ipx-specific-data.md) che contiene dati specifici della famiglia di protocolli IPX.

</dd> </dl>

## <a name="remarks"></a>Commenti

I membri della struttura **di \_ \_ Route IPX RTM** sono tutti allineati a **DWORD** .

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

[Strutture di gestione tabelle di routing versione \_ 1 \_](routing-table-manager-version-1-structures.md)
</dt> <dt>

[**\_rete IPX**](ipx-network.md)
</dt> <dt>

[**\_ \_ indirizzo hop successivo \_ IPX**](ipx-next-hop-address.md)
</dt> <dt>

[**\_dati specifici di IPX \_**](ipx-specific-data.md)
</dt> </dl>

 

 





