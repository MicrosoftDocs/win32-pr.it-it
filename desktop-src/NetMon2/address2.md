---
description: Contiene un singolo indirizzo di qualsiasi tipo di indirizzi supportati.
ms.assetid: 3f840842-8992-4fab-8820-cbbfc63242b8
title: Struttura ADDRESS2 (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ADDRESS
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 95716e7d593bdf655960bfd64901fa09c1020bc4e7d1b6ec850964311a80ca52
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012369"
---
# <a name="address2-structure"></a>Struttura ADDRESS2

La **struttura ADDRESS** contiene un singolo indirizzo di qualsiasi tipo di indirizzi supportati.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _ADDRESS {
  DWORD Type;
  union {
    BYTE                  MACAddress[MAC_ADDRESS_SIZE];
    BYTE                  IPAddress[IP_ADDRESS_SIZE];
    BYTE                  IP6Address[IP6_ADDRESS_SIZE];
    BYTE                  IPXRawAddress[IPX_ADDRESS_SIZE];
    IPX_ADDRESS           IPXAddress;
    BYTE                  VinesIPRawAddress[VINES_IP_ADDRESS_SIZE];
    VINES_IP_ADDRESS      VinesIPAddress;
    ETHERNET_SRC_ADDRESS  EthernetSrcAddress;
    ETHERNET_DST_ADDRESS  EthernetDstAddress;
    TOKENRING_SRC_ADDRESS TokenringSrcAddress;
    TOKENRING_DST_ADDRESS TokenringDstAddress;
    FDDI_SRC_ADDRESS      FddiSrcAddress;
    FDDI_DST_ADDRESS      FddiDstAddress;
  };
  WORD  Flags;
} ADDRESS, *LPADDRESS;
```



## <a name="members"></a>Members

<dl> <dt>

**Tipo**
</dt> <dd>

Tipo di indirizzo. I valori possibili sono i seguenti:

<dl> <dd>ADDRESS_TYPE_ETHERNET</dd> <dd>ADDRESS_TYPE_IP</dd> <dd>ADDRESS_TYPE_IP6</dd> <dd>ADDRESS_TYPE_IPX</dd> <dd>ADDRESS_TYPE_TOKENRING</dd> <dd>ADDRESS_TYPE_FDDI</dd> <dd>ADDRESS_TYPE_XNS</dd> <dd>ADDRESS_TYPE_ANY</dd> <dd>ADDRESS_TYPE_ANY_GROUP</dd> <dd>ADDRESS_TYPE_FIND_HIGHEST</dd> <dd>ADDRESS_TYPE_VINES_IP</dd> <dd>ADDRESS_TYPE_LOCAL_ONLY</dd> <dd>ADDRESS_TYPE_ATM</dd> <dd>ADDRESS_TYPE_1394</dd> </dl> </dd> <dt>

**Macaddress**
</dt> <dd>

Visualizzazione dei dati espressi come indirizzo MAC non elaborato.

</dd> <dt>

**IPAddress**
</dt> <dd>

Visualizzazione dei dati espressi come indirizzo IP non elaborato.

</dd> <dt>

**IP6Address**
</dt> <dd>

Visualizzazione dei dati espressi come indirizzo IP non elaborato versione 6.

</dd> <dt>

**IPXRawAddress**
</dt> <dd>

Visualizzazione dei dati espressi come indirizzo IPX non elaborato.

</dd> <dt>

**IPXAddress**
</dt> <dd>

Visualizzazione dei dati espressi come valore di indirizzo IPX decodificato.

</dd> <dt>

**VinesIPRawAddress**
</dt> <dd>

Visualizzazione dei dati espressi come indirizzo IP vines non elaborato.

</dd> <dt>

**VinesIPAddress**
</dt> <dd>

Visualizzazione dei dati espressi come indirizzo IP di Vines decodificato.

</dd> <dt>

**EthernetSrcAddress**
</dt> <dd>

Visualizzazione dei dati espressi come indirizzo di origine Ethernet.

</dd> <dt>

**EthernetDstAddress**
</dt> <dd>

Visualizzazione dei dati espressi come indirizzo di destinazione Ethernet.

</dd> <dt>

**TokenringSrcAddress**
</dt> <dd>

Visualizzazione dei dati come indirizzo di origine del token ring.

</dd> <dt>

**TokenringDstAddress**
</dt> <dd>

Visualizzazione dei dati come indirizzo di destinazione del token ring.

</dd> <dt>

**FddiSrcAddress**
</dt> <dd>

Visualizzazione dei dati espressi come indirizzo di origine FDDI.

</dd> <dt>

**FddiDstAddress**
</dt> <dd>

Visualizzazione dei dati espressi come indirizzo di destinazione FDDI.

</dd> <dt>

**Flag**
</dt> <dd></dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



 

 




