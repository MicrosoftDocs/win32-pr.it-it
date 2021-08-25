---
description: Il tipo di indirizzo identifica il formato dell'indirizzo, ad esempio il numero di telefono standard o l'indirizzo di posta elettronica. Solo le applicazioni che negoziano TAPI versione 3.0 o successiva possono usare i tipi di indirizzo.
ms.assetid: 2c32eda1-e510-40eb-ae75-fc7b9e9953cd
title: LINEADDRESSTYPE_ costanti (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6555ff934ffb8c1b40b8f35d279a2071cad32b80b754af19672108f5e318a17
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119873334"
---
# <a name="lineaddresstype_-constants"></a>Costanti \_ LINEADDRESSTYPE

Il tipo di indirizzo identifica il formato dell'indirizzo, ad esempio il numero di telefono standard o l'indirizzo di posta elettronica. Solo le applicazioni che negoziano TAPI versione 3.0 o successiva possono usare i tipi di indirizzo.

<dl> <dt>

<span id="LINEADDRESSTYPE_PHONENUMBER"></span><span id="lineaddresstype_phonenumber"></span>**LINEADDRESSTYPE \_ PHONENUMBER**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



Il tipo di indirizzo è un numero di telefono standard.


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSTYPE_SDP"></span><span id="lineaddresstype_sdp"></span>**LINEADDRESSTYPE \_ SDP**
</dt> <dd> <dl> <dt>

0x00000002
</dt> <dt>



Il tipo di indirizzo è Session Description Protocol (SDP).


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSTYPE_EMAILNAME"></span><span id="lineaddresstype_emailname"></span>**LINEADDRESSTYPE \_ EMAILNAME**
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



Il tipo di indirizzo è un nome di posta elettronica.


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSTYPE_DOMAINNAME"></span><span id="lineaddresstype_domainname"></span>**LINEADDRESSTYPE \_ DOMAINNAME**
</dt> <dd> <dl> <dt>

0x00000008
</dt> <dt>



Il tipo di indirizzo è un nome di dominio.


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSTYPE_IPADDRESS"></span><span id="lineaddresstype_ipaddress"></span>**LINEADDRESSTYPE \_ IPADDRESS**
</dt> <dd> <dl> <dt>

0x00000010
</dt> <dt>



Il tipo di indirizzo è un indirizzo IP.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3.0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




