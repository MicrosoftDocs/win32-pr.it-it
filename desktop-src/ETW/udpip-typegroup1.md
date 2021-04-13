---
description: Questa classe è la classe del tipo di evento per gli eventi di trasmissione e ricezione IPv4 UDP/IP. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: f04e0b4c-6a2b-4452-9bdf-38c08b487863
title: Classe UdpIp_TypeGroup1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UdpIp_TypeGroup1
- UdpIp_TypeGroup1.PID
- UdpIp_TypeGroup1.size
- UdpIp_TypeGroup1.daddr
- UdpIp_TypeGroup1.saddr
- UdpIp_TypeGroup1.dport
- UdpIp_TypeGroup1.sport
- UdpIp_TypeGroup1.seqnum
- UdpIp_TypeGroup1.connid
api_type:
- NA
api_location: ''
ms.openlocfilehash: 8d977841cbfe9a88d14056d77a9b943f4d5d4a3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978871"
---
# <a name="udpip_typegroup1-class"></a>\_Classe UdpIp TypeGroup1

Questa classe è la classe del tipo di evento per gli eventi di trasmissione e ricezione IPv4 UDP/IP.

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[EventType{10, 11}, EventTypeName{"SendIPV4", "RecvIPV4"}]
class UdpIp_TypeGroup1 : UdpIp
{
  uint32 PID;
  uint32 size;
  object daddr;
  object saddr;
  object dport;
  object sport;
  uint32 seqnum;
  uint32 connid;
};
```

## <a name="members"></a>Members

La **classe \_ TypeGroup1 di UdpIp** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ TypeGroup1 di UdpIp** dispone di queste proprietà.

<dl> <dt>

ConnID
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (8), puntatore
</dt> </dl>

Identificatore di connessione univoco per correlare gli eventi che appartengono alla stessa connessione.

</dd> <dt>

daddr
</dt> <dd> <dl> <dt>

Tipo di dati: **Object**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (3), Extension ("IPAddrV4")
</dt> </dl>

Indirizzo IP di destinazione.

</dd> <dt>

dport
</dt> <dd> <dl> <dt>

Tipo di dati: **Object**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (5), Extension ("Port")
</dt> </dl>

Numero di porta di destinazione.

</dd> <dt>

PID
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (1)
</dt> </dl>

Identificatore del processo associato alla richiesta.

</dd> <dt>

saddr
</dt> <dd> <dl> <dt>

Tipo di dati: **Object**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (4), Extension ("IPAddrV4")
</dt> </dl>

Indirizzo IP di origine.

</dd> <dt>

SeqNum
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (7)
</dt> </dl>

Numero di sequenza.

</dd> <dt>

size
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (2)
</dt> </dl>

Dimensioni del pacchetto.

</dd> <dt>

Sport
</dt> <dd> <dl> <dt>

Tipo di dati: **Object**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (6), Extension ("Port")
</dt> </dl>

Numero di porta di origine.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**UdpIp**](udpip.md)
</dt> </dl>

 

 




