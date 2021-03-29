---
description: Questa classe è la classe del tipo di evento per gli eventi TCP/IP. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: 007f0744-8b74-4c57-85bc-f6bdb20bffa7
title: Classe TcpIp_V0_TypeGroup1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TcpIp_V0_TypeGroup1
- TcpIp_V0_TypeGroup1.daddr
- TcpIp_V0_TypeGroup1.saddr
- TcpIp_V0_TypeGroup1.dport
- TcpIp_V0_TypeGroup1.sport
- TcpIp_V0_TypeGroup1.size
- TcpIp_V0_TypeGroup1.PID
api_type:
- NA
api_location: ''
ms.openlocfilehash: c21025990fe3e21cd5322b651e543472fa8d48c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344551"
---
# <a name="tcpip_v0_typegroup1-class"></a>\_ \_ Classe TypeGroup1 Tcpip V0

Questa classe è la classe del tipo di evento per gli eventi TCP/IP.

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[EventType{10, 11, 12, 13, 14, 15}, EventTypeName{"Send", "Recv", "Connect", "Disconnect", "Retransmit", "Accept"}]
class TcpIp_V0_TypeGroup1 : TcpIp_V0
{
  object daddr;
  object saddr;
  object dport;
  object sport;
  uint32 size;
  uint32 PID;
};
```

## <a name="members"></a>Members

La classe **TCPIP \_ V0 \_ TypeGroup1** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **TCPIP \_ V0 \_ TypeGroup1** ha queste proprietà.

<dl> <dt>

daddr
</dt> <dd> <dl> <dt>

Tipo di dati: **Object**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (1), Extension ("IPAddr")
</dt> </dl>

Indirizzo IP di destinazione.

</dd> <dt>

dport
</dt> <dd> <dl> <dt>

Tipo di dati: **Object**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (3), Extension ("Port")
</dt> </dl>

Numero di porta di destinazione.

</dd> <dt>

PID
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (6)
</dt> </dl>

Identificatore del processo associato alla richiesta.

</dd> <dt>

saddr
</dt> <dd> <dl> <dt>

Tipo di dati: **Object**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (2), Extension ("IPAddr")
</dt> </dl>

Indirizzo IP di origine.

</dd> <dt>

size
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (5)
</dt> </dl>

Dimensioni del pacchetto.

</dd> <dt>

Sport
</dt> <dd> <dl> <dt>

Tipo di dati: **Object**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (4), Extension ("Port")
</dt> </dl>

Numero di porta di origine.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/> |
| Server minimo supportato<br/> | Nessuno supportato<br/>                   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**TcpIp \_ V0**](tcpip-v0.md)
</dt> </dl>

 

 




