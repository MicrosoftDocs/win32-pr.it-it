---
description: 'UdpIp_Fail classe: questa classe è la classe del tipo di evento per gli eventi di errore TCP/IP. La sintassi seguente è semplificata dal codice MOF.'
ms.assetid: 552e63ef-70e4-4bc4-be33-bd77bd5acd61
title: UdpIp_Fail classe
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
ms.openlocfilehash: 3cb58c7262e46dde761d1494bc26b5a5701489f7e5aed167e1edf85bd9789f94
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117813803"
---
# <a name="udpip_fail-class"></a>Classe UdpIp \_ Fail

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

La **classe UdpIp \_ Fail** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe UdpIp \_ Fail** ha queste proprietà.

<dl> <dt>

**FailureCode**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Motivo dell'errore. Può essere uno dei codici seguenti:

<dl> <dt>

<span id="ERROR_INSUFFICIENT_RESOURCES"></span><span id="error_insufficient_resources"></span>**ERRORE \_ RISORSE \_ INSUFFICIENTI** (1)
</dt> <dt>

<span id="ERROR_TOO_MANY_ADDRESSES"></span><span id="error_too_many_addresses"></span>**ERRORE \_ TROPPI \_ \_ INDIRIZZI** (2)
</dt> <dt>

<span id="ERROR_ADDRESS_EXISTS"></span><span id="error_address_exists"></span>**ERRORE \_ \_L'INDIRIZZO ESISTE** (3)
</dt> <dt>

<span id="ERROR_INVALID_ADDRESS"></span><span id="error_invalid_address"></span>**ERRORE \_ INDIRIZZO \_ NON VALIDO** (4)
</dt> <dt>

<span id="ERROR_OTHER"></span><span id="error_other"></span>**ERRORE \_ OTHER** (5)
</dt> <dt>

<span id="ERROR_TIMEWAIT_ADDRESS_EXIST"></span><span id="error_timewait_address_exist"></span>**ERRORE \_ L'INDIRIZZO \_ \_ TIMEWAIT ESISTE** (6)
</dt> </dl>

</dd> <dt>

**Proto**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Identifica il protocollo. I possibili valori sono i seguenti:



| Valore                                                                                                                                                                                                  | Significato                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <span id="AF_INET"></span><span id="af_inet"></span><dl> <dt>**AF \_ INET**</dt> <dt>2</dt> </dl>     | Famiglia protocollo IP versione 4 di indirizzi (IPv4).<br/>  |
| <span id="AF_INET6"></span><span id="af_inet6"></span><dl> <dt>**AF \_ INET6**</dt> <dt>23</dt> </dl> | Famiglia di indirizzi IPv6 (Internet Protocol versione 6).<br/> |



 

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**UdpIp**](udpip.md)
</dt> </dl>

 

 




