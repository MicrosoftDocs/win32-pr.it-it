---
description: Il tipo di indirizzo identifica il formato dell'indirizzo, ad esempio il numero di telefono standard o l'indirizzo di posta elettronica. Solo le applicazioni che negoziano la versione 3,0 o successiva di TAPI possono usare i tipi di indirizzo.
ms.assetid: 2c32eda1-e510-40eb-ae75-fc7b9e9953cd
title: Costanti LINEADDRESSTYPE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6d0a46eff2a7a0c38fa17aed4b831ef8701c565
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327786"
---
# <a name="lineaddresstype_-constants"></a>\_Costanti LINEADDRESSTYPE

Il tipo di indirizzo identifica il formato dell'indirizzo, ad esempio il numero di telefono standard o l'indirizzo di posta elettronica. Solo le applicazioni che negoziano la versione 3,0 o successiva di TAPI possono usare i tipi di indirizzo.

<dl> <dt>

<span id="LINEADDRESSTYPE_PHONENUMBER"></span><span id="lineaddresstype_phonenumber"></span>**\_PhoneNumber LINEADDRESSTYPE**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



Tipo di indirizzo è un numero di telefono standard.


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSTYPE_SDP"></span><span id="lineaddresstype_sdp"></span>**\_SDP LINEADDRESSTYPE**
</dt> <dd> <dl> <dt>

0x00000002
</dt> <dt>



Tipo di indirizzo è la conferenza SDP (Session Description Protocol).


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSTYPE_EMAILNAME"></span><span id="lineaddresstype_emailname"></span>**LINEADDRESSTYPE \_ EmailName**
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



Tipo di indirizzo è un nome di posta elettronica.


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSTYPE_DOMAINNAME"></span><span id="lineaddresstype_domainname"></span>**LINEADDRESSTYPE \_ DomainName**
</dt> <dd> <dl> <dt>

0x00000008
</dt> <dt>



Tipo di indirizzo è un nome di dominio.


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSTYPE_IPADDRESS"></span><span id="lineaddresstype_ipaddress"></span>**LINEADDRESSTYPE \_ IPAddress**
</dt> <dd> <dl> <dt>

0x00000010
</dt> <dt>



Il tipo di indirizzo è un indirizzo IP.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3,0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




