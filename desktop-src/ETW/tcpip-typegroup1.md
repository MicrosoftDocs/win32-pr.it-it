---
description: Questa classe è la classe del tipo di evento per gli eventi TCP/IP IPv4. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: ed835df8-6f53-46a3-abf2-c66a1f13f987
title: TcpIp_TypeGroup1 classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TcpIp_TypeGroup1
- TcpIp_TypeGroup1.PID
- TcpIp_TypeGroup1.size
- TcpIp_TypeGroup1.daddr
- TcpIp_TypeGroup1.saddr
- TcpIp_TypeGroup1.dport
- TcpIp_TypeGroup1.sport
- TcpIp_TypeGroup1.seqnum
- TcpIp_TypeGroup1.connid
api_type:
- NA
api_location: ''
ms.openlocfilehash: 89c8947296a889ecb2297982ae96db7c0c73c243f917b276391d7f7b627fc3ba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120075231"
---
# <a name="tcpip_typegroup1-class"></a>Classe \_ TypeGroup1 TcpIp

Questa classe è la classe del tipo di evento per gli eventi TCP/IP IPv4.

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[EventType{11, 13, 14, 16, 18}, EventTypeName{"RecvIPV4", "DisconnectIPV4", "RetransmitIPV4", "ReconnectIPV4", "TCPCopyIPV4"}]
class TcpIp_TypeGroup1 : TcpIp
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

La **classe \_ TcpIp TypeGroup1** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ TcpIp TypeGroup1** ha queste proprietà.

<dl> <dt>

connid
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId(8), Puntatore
</dt> </dl>

Identificatore di connessione univoco per correlare gli eventi appartenenti alla stessa connessione.

</dd> <dt>

daddr
</dt> <dd> <dl> <dt>

Tipo di dati: **object**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId(3), Extension("IPAddrV4")
</dt> </dl>

Indirizzo IP di destinazione.

</dd> <dt>

dport
</dt> <dd> <dl> <dt>

Tipo di dati: **object**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId(5), Extension("Port")
</dt> </dl>

Numero di porta di destinazione.

</dd> <dt>

PID
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId(1)
</dt> </dl>

Identificatore del processo associato alla richiesta.

</dd> <dt>

saddr
</dt> <dd> <dl> <dt>

Tipo di dati: **object**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId(4), Extension("IPAddrV4")
</dt> </dl>

Indirizzo IP di origine.

</dd> <dt>

seqnum
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId(7)
</dt> </dl>

Numero di sequenza.

</dd> <dt>

size
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId(2)
</dt> </dl>

Dimensioni del pacchetto.

</dd> <dt>

sport
</dt> <dd> <dl> <dt>

Tipo di dati: **object**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId(6), Extension("Port")
</dt> </dl>

Numero di porta di origine.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Tcpip**](tcpip.md)
</dt> </dl>

 

 




