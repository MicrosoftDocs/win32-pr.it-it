---
title: RTM_IPX_ROUTE struttura (Rtm.h)
description: La struttura RTM \_ IPX \_ ROUTE contiene informazioni che descrivono una route per la famiglia di protocolli IPX.
ms.assetid: ffa0637c-2197-4ebd-a5ef-e174dd0ccb15
keywords:
- RTM_IPX_ROUTE struttura RAS
- PRTM_IPX_ROUTE puntatore alla struttura RAS
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
ms.openlocfilehash: 1e3d14de623fe8d0b3a85118b39d764baa00d2ca5930cfe711be21a91057b6db
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120101831"
---
# <a name="rtm_ipx_route-structure"></a>Struttura DI \_ ROUTE IPX \_ RTM

\[Questa API è stata sostituita dall'API Gestione tabelle di [routing versione 2](about-routing-table-manager-version-2.md) e non sarà disponibile oltre Windows Server 2003. Le applicazioni devono usare l'API Gestione tabelle di routing versione 2.\]

La **struttura RTM \_ IPX \_ ROUTE** contiene informazioni che descrivono una route per la famiglia di protocolli IPX.

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

Specifica una struttura [**PROTOCOL \_ SPECIFIC \_ DATA**](protocol-specific-data.md) contenente la memoria riservata ai dati specifici dei protocolli di routing.

</dd> <dt>

**Rete \_ RR**
</dt> <dd>

Specifica una struttura [**IPX \_ NETWORK**](ipx-network.md) che contiene un indirizzo di rete IP.

</dd> <dt>

**RR \_ NextHopAddress**
</dt> <dd>

Specifica una struttura [**IPX \_ NEXT HOP \_ \_ ADDRESS**](ipx-next-hop-address.md) che contiene l'indirizzo del router dell'hop successivo.

</dd> <dt>

**RR \_ FamilySpecificData**
</dt> <dd>

Specifica una struttura [**IPX \_ SPECIFIC \_ DATA**](ipx-specific-data.md) che contiene dati specifici della famiglia di protocolli IPX.

</dd> </dl>

## <a name="remarks"></a>Commenti

I membri della struttura **RTM \_ IPX \_ ROUTE** sono tutti **allineati con DWORD.**

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

[Strutture di Gestione tabelle di \_ routing versione 1 \_](routing-table-manager-version-1-structures.md)
</dt> <dt>

[**RETE \_ IPX**](ipx-network.md)
</dt> <dt>

[**INDIRIZZO HOP \_ \_ \_ SUCCESSIVO IPX**](ipx-next-hop-address.md)
</dt> <dt>

[**DATI SPECIFICI \_ \_ IPX**](ipx-specific-data.md)
</dt> </dl>

 

 





