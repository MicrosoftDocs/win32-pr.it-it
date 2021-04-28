---
description: 'UdpIp_V1_TypeGroup1 classe: questa classe è la classe del tipo di evento per gli eventi UDP/IP. La sintassi seguente è semplificata dal codice MOF.'
ms.assetid: c0ef6679-3852-4992-9fc2-114620eae14e
title: UdpIp_V1_TypeGroup1 classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UdpIp_V1_TypeGroup1
- UdpIp_V1_TypeGroup1.PID
- UdpIp_V1_TypeGroup1.size
- UdpIp_V1_TypeGroup1.daddr
- UdpIp_V1_TypeGroup1.saddr
- UdpIp_V1_TypeGroup1.dport
- UdpIp_V1_TypeGroup1.sport
api_type:
- NA
api_location: ''
ms.openlocfilehash: d7dadaac3d418d2351f9e27c694309deb373615e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105409"
---
# <a name="udpip_v1_typegroup1-class"></a>Classe \_ \_ TypeGroup1 UdpIp V1

Questa classe è la classe del tipo di evento per gli eventi UDP/IP.

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[EventType{10, 11}, EventTypeName{"Send", "Recv"}]
class UdpIp_V1_TypeGroup1 : UdpIp_V1
{
  uint32 PID;
  uint32 size;
  object daddr;
  object saddr;
  object dport;
  object sport;
};
```

## <a name="members"></a>Members

La **classe \_ \_ TypeGroup1 UdpIp V1** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ \_ TypeGroup1 UdpIp V1** ha queste proprietà.

<dl> <dt>

daddr
</dt> <dd> <dl> <dt>

Tipo di dati: **object**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId(3), Extension("IPAddr")
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

Qualificatori: WmiDataId(4), Extension("IPAddr")
</dt> </dl>

Indirizzo IP di origine.

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
| Client minimo supportato<br/> | Solo app desktop di Windows XP \[\]<br/>          |
| Server minimo supportato<br/> | Solo app desktop di Windows Server 2003 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**UdpIp \_ V1**](udpip-v1.md)
</dt> <dt>

[**UdpIp**](udpip.md)
</dt> </dl>

 

 




