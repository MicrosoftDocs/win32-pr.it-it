---
description: 'TcpIp_Fail: questa classe è la classe del tipo di evento per gli eventi di errore TCP/IP. La sintassi seguente è semplificata dal codice MOF.'
ms.assetid: 1fe20b8c-b8f1-4db0-af78-1ebfc40b2bbd
title: TcpIp_Fail classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TcpIp_Fail
- TcpIp_Fail.Proto
- TcpIp_Fail.FailureCode
api_type:
- NA
api_location: ''
ms.openlocfilehash: cd637db3f509e8c23de764eb82cc35b49cb435a7772a14adbe2954d292696e55
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117814531"
---
# <a name="tcpip_fail-class"></a>Classe TcpIp \_ Fail

Questa classe è la classe del tipo di evento per gli eventi di errore TCP/IP.

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[EventType{17}, EventTypeName{"Fail"}]
class TcpIp_Fail : TcpIp
{
  uint16 Proto;
  uint16 FailureCode;
};
```

## <a name="members"></a>Members

La **classe TcpIp \_ Fail** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe TcpIp \_ Fail** ha queste proprietà.

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

<span id="ERROR_ADDRESS_EXISTS"></span><span id="error_address_exists"></span>**ERRORE \_ ADDRESS \_ EXISTS** (3)
</dt> <dt>

<span id="ERROR_INVALID_ADDRESS"></span><span id="error_invalid_address"></span>**ERRORE \_ INDIRIZZO \_ NON VALIDO** (4)
</dt> <dt>

<span id="ERROR_OTHER"></span><span id="error_other"></span>**ERRORE \_ OTHER** (5)
</dt> <dt>

<span id="ERROR_TIMEWAIT_ADDRESS_EXIST"></span><span id="error_timewait_address_exist"></span>**ERRORE \_ TIMEWAIT \_ ADDRESS \_ EXIST** (6)
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
| <span id="AF_INET"></span><span id="af_inet"></span><dl> <dt>**Af \_ INET**</dt> <dt>2</dt> </dl>     | Famiglia di protocollo IP versione 4 (IPv4).<br/>  |
| <span id="AF_INET6"></span><span id="af_inet6"></span><dl> <dt>**Af \_ INET6**</dt> <dt>23</dt> </dl> | Famiglia di indirizzi IPv6 (Internet Protocol versione 6).<br/> |



 

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Tcpip**](tcpip.md)
</dt> </dl>

 

 




