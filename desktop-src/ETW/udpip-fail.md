---
description: Questa classe è la classe del tipo di evento per gli eventi di errore TCP/IP. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: 552e63ef-70e4-4bc4-be33-bd77bd5acd61
title: Classe UdpIp_Fail
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UdpIp_Fail
- UdpIp_Fail.Proto
- UdpIp_Fail.FailureCode
api_type:
- NA
api_location: ''
ms.openlocfilehash: aef0194d296395501500022bf4cae8b9c8a8f188
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980903"
---
# <a name="udpip_fail-class"></a>\_Classe UdpIp Fail

Questa classe è la classe del tipo di evento per gli eventi di errore TCP/IP.

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[EventType{17}, EventTypeName{"Fail"}]
class UdpIp_Fail : UdpIp
{
  uint16 Proto;
  uint16 FailureCode;
};
```

## <a name="members"></a>Members

La classe **UdpIp \_ Fail** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **UdpIp \_ Fail** presenta queste proprietà.

<dl> <dt>

**FailureCode**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Motivo dell'errore. Può essere uno dei seguenti codici:

<dl> <dt>

<span id="ERROR_INSUFFICIENT_RESOURCES"></span><span id="error_insufficient_resources"></span>**Errore \_ \_Risorse insufficienti** (1)
</dt> <dt>

<span id="ERROR_TOO_MANY_ADDRESSES"></span><span id="error_too_many_addresses"></span>**Errore \_ TROPPi \_ \_ indirizzi** (2)
</dt> <dt>

<span id="ERROR_ADDRESS_EXISTS"></span><span id="error_address_exists"></span>**Errore \_ INDIRIZZO \_ esistente** (3)
</dt> <dt>

<span id="ERROR_INVALID_ADDRESS"></span><span id="error_invalid_address"></span>**Errore \_ \_Indirizzo non valido** (4)
</dt> <dt>

<span id="ERROR_OTHER"></span><span id="error_other"></span>**Errore \_ ALTRO** (5)
</dt> <dt>

<span id="ERROR_TIMEWAIT_ADDRESS_EXIST"></span><span id="error_timewait_address_exist"></span>**Errore \_ \_Indirizzo TIMEWAIT \_ esistente** (6)
</dt> </dl>

</dd> <dt>

**Proto**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Identifica il protocollo. I possibili valori sono i seguenti:



| Valore                                                                                                                                                                                                  | Significato                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <span id="AF_INET"></span><span id="af_inet"></span><dl> <dt>**AF \_ INET**</dt> <dt>2</dt> </dl>     | Famiglia di indirizzi protocollo Internet versione 4 (IPv4).<br/>  |
| <span id="AF_INET6"></span><span id="af_inet6"></span><dl> <dt>**AF \_ INET6**</dt> <dt>23</dt> </dl> | Famiglia di indirizzi protocollo Internet versione 6 (IPv6).<br/> |



 

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

 

 




