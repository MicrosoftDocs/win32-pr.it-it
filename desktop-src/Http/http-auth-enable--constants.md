---
title: Costanti HTTP_AUTH_ENABLE_ (http. h)
description: Definire schemi di autenticazione che possono essere abilitati in un gruppo di URL.
ms.assetid: db22645f-c9e4-427e-b3d5-91d568aec7c5
topic_type:
- apiref
api_name:
- HTTP_AUTH_ENABLE_BASIC
- HTTP_AUTH_ENABLE_DIGEST
- HTTP_AUTH_ENABLE_KERBEROS
- HTTP_AUTH_EX_FLAG_ENABLE_KERBEROS_CREDENTIAL_CACHING
- HTTP_AUTH_EX_FLAG_CAPTURE_CREDENTIAL
- HTTP_AUTH_ENABLE_NTLM
- HTTP_AUTH_ENABLE_NEGOTIATE
- HTTP_AUTH_ENABLE_ALL
api_location:
- http.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6462a4f9d884244f460c4bf7714b45d3e17600c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478940"
---
# <a name="http_auth_enable_-constants"></a>\_Costanti di \_ Abilitazione dell'autenticazione HTTP \_

Le costanti di **\_ \_ Abilitazione http auth** definiscono gli schemi di autenticazione che possono essere abilitati in un gruppo di URL.

Queste costanti vengono utilizzate nella struttura delle [**\_ informazioni di \_ autenticazione \_ del server http**](/windows/desktop/api/Http/ns-http-http_server_authentication_info) .

<dl> <dt>

<span id="HTTP_AUTH_ENABLE_BASIC"></span><span id="http_auth_enable_basic"></span>**\_autenticazione HTTP \_ Abilita \_ Basic**
</dt> <dd> <dl> <dt>



Lo schema di autenticazione di base è abilitato.


</dt> </dl> </dd> <dt>

<span id="HTTP_AUTH_ENABLE_DIGEST"></span><span id="http_auth_enable_digest"></span>**\_autenticazione HTTP \_ Abilita \_ digest**
</dt> <dd> <dl> <dt>



Lo schema di autenticazione del digest è abilitato.


</dt> </dl> </dd> <dt>

<span id="HTTP_AUTH_ENABLE_KERBEROS"></span><span id="http_auth_enable_kerberos"></span>**\_autenticazione HTTP \_ Abilita \_ Kerberos**
</dt> <dd> <dl> <dt>



Lo schema di autenticazione Kerberos è abilitato.


</dt> </dl> </dd> <dt>

<span id="HTTP_AUTH_EX_FLAG_ENABLE_KERBEROS_CREDENTIAL_CACHING"></span><span id="http_auth_ex_flag_enable_kerberos_credential_caching"></span>**\_ \_ \_ \_ Abilitazione della \_ \_ \_ memorizzazione nella cache delle credenziali Kerberos tramite il contrassegno http auth**
</dt> <dd> <dl> <dt>



La memorizzazione nella cache delle credenziali Kerberos è abilitata.

**Windows Server 2003 e precedenti:** Non disponibile.


</dt> </dl> </dd> <dt>

<span id="HTTP_AUTH_EX_FLAG_CAPTURE_CREDENTIAL"></span><span id="http_auth_ex_flag_capture_credential"></span>**\_credenziali di \_ \_ acquisizione del flag http auth ex \_ \_**
</dt> <dd> <dl> <dt>



L'API server HTTP acquisisce l'identità del chiamante e la usa per l'autenticazione solo per gli schemi Negotiate e Kerberos.

**Windows Server 2003 e precedenti:** Non disponibile.


</dt> </dl> </dd> <dt>

<span id="HTTP_AUTH_ENABLE_NTLM"></span><span id="http_auth_enable_ntlm"></span>**\_autenticazione HTTP \_ Abilita \_ NTLM**
</dt> <dd> <dl> <dt>



Lo schema di autenticazione NTLM è abilitato.


</dt> </dl> </dd> <dt>

<span id="HTTP_AUTH_ENABLE_NEGOTIATE"></span><span id="http_auth_enable_negotiate"></span>**\_ \_ Abilita negoziazione http \_ AUTH**
</dt> <dd> <dl> <dt>



Lo schema di autenticazione Negotiate è abilitato.


</dt> </dl> </dd> <dt>

<span id="HTTP_AUTH_ENABLE_ALL"></span><span id="http_auth_enable_all"></span>**\_ \_ Abilita \_ tutti gli http auth**
</dt> <dd> <dl> <dt>



Tutti gli schemi di autenticazione sono abilitati.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                    |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                              |
| Intestazione<br/>                   | <dl> <dt>Http. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Costanti API server HTTP versione 2,0](http-server-api-version-2-0-constants.md)
</dt> <dt>

[**\_informazioni di \_ autenticazione \_ Server http**](/windows/desktop/api/Http/ns-http-http_server_authentication_info)
</dt> <dt>

[**HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty)
</dt> <dt>

[**HttpSetServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty)
</dt> <dt>

[**HttpQueryUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpqueryurlgroupproperty)
</dt> <dt>

[**HttpQueryServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpqueryserversessionproperty)
</dt> </dl>

 

 





