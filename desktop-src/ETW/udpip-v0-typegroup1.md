---
description: Questa classe è la classe del tipo di evento per gli eventi UDP/IP. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: 834a761a-089b-4b93-9a6a-a1edf752b582
title: Classe UdpIp_V0_TypeGroup1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UdpIp_V0_TypeGroup1
- UdpIp_V0_TypeGroup1.context
- UdpIp_V0_TypeGroup1.saddr
- UdpIp_V0_TypeGroup1.sport
- UdpIp_V0_TypeGroup1.size
- UdpIp_V0_TypeGroup1.daddr
- UdpIp_V0_TypeGroup1.dport
- UdpIp_V0_TypeGroup1.dsize
api_type:
- NA
api_location: ''
ms.openlocfilehash: 2813476bc2c820d1872e787dc047fafccd3b7d52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968111"
---
# <a name="udpip_v0_typegroup1-class"></a>\_Classe UdpIp V0 \_ TypeGroup1

Questa classe è la classe del tipo di evento per gli eventi UDP/IP.

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[EventType{10, 11}, EventTypeName{"Send", "Recv"}]
class UdpIp_V0_TypeGroup1 : UdpIp_V0
{
  uint32 context;
  object saddr;
  object sport;
  uint16 size;
  object daddr;
  object dport;
  uint16 dsize;
};
```

## <a name="members"></a>Members

La classe **UdpIp \_ V0 \_ TypeGroup1** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **UdpIp \_ V0 \_ TypeGroup1** ha queste proprietà.

<dl> <dt>

contesto
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (1), puntatore
</dt> </dl>

Identificatore del processo per l'oggetto Address che ha effettuato o ricevuto la richiesta.

</dd> <dt>

daddr
</dt> <dd> <dl> <dt>

Tipo di dati: **Object**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (5), Extension ("IPAddr")
</dt> </dl>

Indirizzo IP di destinazione.

</dd> <dt>

dport
</dt> <dd> <dl> <dt>

Tipo di dati: **Object**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (6), Extension ("Port")
</dt> </dl>

Numero di porta di destinazione.

</dd> <dt>

dsize
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (7)
</dt> </dl>

Dimensioni del pacchetto di destinazione.

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

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (4)
</dt> </dl>

Dimensioni del pacchetto di origine.

</dd> <dt>

Sport
</dt> <dd> <dl> <dt>

Tipo di dati: **Object**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (3), Extension ("Port")
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

[**UdpIp \_ V0**](udpip-v0.md)
</dt> </dl>

 

 




