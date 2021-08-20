---
description: Questa classe è la classe del tipo di evento per gli eventi di invio TCP/IP IPv4. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: 51a61257-fcbf-4724-80e4-12bdf45b359e
title: TcpIp_SendIPV4 classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TcpIp_SendIPV4
- TcpIp_SendIPV4.PID
- TcpIp_SendIPV4.size
- TcpIp_SendIPV4.daddr
- TcpIp_SendIPV4.saddr
- TcpIp_SendIPV4.dport
- TcpIp_SendIPV4.sport
- TcpIp_SendIPV4.startime
- TcpIp_SendIPV4.endtime
- TcpIp_SendIPV4.seqnum
- TcpIp_SendIPV4.connid
api_type:
- NA
api_location: ''
ms.openlocfilehash: 425c785c885152349c4ffddc503fc36c1ec751ead6a35c63f17ec9f26d6d2fdd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118151110"
---
# <a name="tcpip_sendipv4-class"></a>Classe \_ TcpIp SendIPV4

Questa classe è la classe del tipo di evento per gli eventi di invio TCP/IP IPv4.

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[EventType{10}, EventTypeName{"SendIPV4"}]
class TcpIp_SendIPV4 : TcpIp
{
  uint32 PID;
  uint32 size;
  object daddr;
  object saddr;
  object dport;
  object sport;
  uint32 startime;
  uint32 endtime;
  uint32 seqnum;
  uint32 connid;
};
```

## <a name="members"></a>Members

La **classe TcpIp \_ SendIPV4** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe TcpIp \_ SendIPV4** ha queste proprietà.

<dl> <dt>

connid
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId(10), Puntatore
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

**Endtime**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId(8)
</dt> </dl>

Ora di fine della richiesta di invio.

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

Qualificatori: WmiDataId(9)
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

</dd> <dt>

**startime**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId(7)
</dt> </dl>

Ora di inizio dell'invio della richiesta.

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

 

 




