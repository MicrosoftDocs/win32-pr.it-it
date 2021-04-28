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
ms.openlocfilehash: 897c42a1c2530d3e41d1f937d5d59356a2913e2b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105849"
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
| <span id="AF_INET"></span><span id="af_inet"></span><dl> <dt>**Af \_ INET**</dt> <dt>2</dt> </dl>     | Famiglia protocollo IP versione 4 indirizzi di rete (IPv4).<br/>  |
| <span id="AF_INET6"></span><span id="af_inet6"></span><dl> <dt>**Af \_ INET6**</dt> <dt>23</dt> </dl> | Famiglia di indirizzi IPv6 (Internet Protocol versione 6).<br/> |



 

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop di Windows Vista \[\]<br/>       |
| Server minimo supportato<br/> | Solo app desktop di Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Tcpip**](tcpip.md)
</dt> </dl>

 

 




