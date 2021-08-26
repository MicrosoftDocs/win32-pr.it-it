---
title: HTTP_LOGGING_FLAG_ costanti (Http.h)
description: Definire le opzioni per configurare la registrazione nell'API del server HTTP.
ms.assetid: b6afef7a-5426-4ccd-9785-169e83812c07
topic_type:
- apiref
api_name:
- HTTP_LOGGING_FLAG_LOCAL_TIME_ROLLOVER
- HTTP_LOGGING_FLAG_USE_UTF8_CONVERSION
- HTTP_LOGGING_FLAG_LOG_ERRORS_ONLY
- HTTP_LOGGING_FLAG_LOG_SUCCESS_ONLY
api_location:
- http.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ae84697d84295d137f929bcf0d65c2e49fc6754aa7c1110d3b341bb471cbcb8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119981441"
---
# <a name="http_logging_flag_-constants"></a>Costanti \_ FLAG DI REGISTRAZIONE \_ \_ HTTP

Le **costanti HTTP LOGGING \_ \_ FLAG \_** definiscono le opzioni per configurare la registrazione nell'API del server HTTP.

Queste costanti vengono usate nella struttura [**HTTP \_ LOGGING \_ INFO.**](/windows/desktop/api/Http/ns-http-http_logging_info)

<dl> <dt>

<span id="HTTP_LOGGING_FLAG_LOCAL_TIME_ROLLOVER"></span><span id="http_logging_flag_local_time_rollover"></span>**\_ROLLOVER \_ \_ DELL'ORA LOCALE DEL FLAG DI \_ \_ REGISTRAZIONE HTTP**
</dt> <dd> <dl> <dt>



Il rollover del file di log è basato sull'ora locale. Per impostazione predefinita, il rollover dei file di log è basato sull'ora UTC (Coordinated Universal Time).


</dt> </dl> </dd> <dt>

<span id="_HTTP_LOGGING_FLAG_USE_UTF8_CONVERSION"></span><span id="_http_logging_flag_use_utf8_conversion"></span>**HTTP \_ FLAG \_ DI REGISTRAZIONE USA \_ \_ CONVERSIONE \_ UTF8**
</dt> <dd> <dl> <dt>



I campi Unicode vengono convertiti in multibyte UTF8 durante la scrittura nei file di log. Per impostazione predefinita, i file di log vengono scritti con la conversione della tabella codici locale.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOGGING_FLAG_LOG_ERRORS_ONLY"></span><span id="http_logging_flag_log_errors_only"></span>**SOLO ERRORI \_ DEL LOG DEL FLAG DI REGISTRAZIONE \_ \_ \_ \_ HTTP**
</dt> <dd> <dl> <dt>



I file di log includono solo informazioni sugli errori. Per impostazione predefinita, vengono registrate sia le risposte di errore che le risposte riuscite. Se né **l'opzione HTTP LOGGING FLAG LOG ERRORS \_ \_ \_ \_ \_ ONLY** o **HTTP LOGGING FLAG LOG SUCCESS \_ \_ \_ \_ \_ ONLY** è impostata, vengono registrate sia le informazioni relative agli errori che alle operazioni riuscite.

Questo flag non può essere impostato se è impostato anche il flag **HTTP LOGGING FLAG LOG SUCCESS \_ \_ \_ \_ \_ ONLY.** Questi due flag si escludono a vicenda.


</dt> </dl> </dd> <dt>

<span id="_HTTP_LOGGING_FLAG_LOG_SUCCESS_ONLY"></span><span id="_http_logging_flag_log_success_only"></span>**HTTP \_ REGISTRAZIONE \_ DEL FLAG DI REGISTRAZIONE SOLO \_ \_ RIUSCITA \_**
</dt> <dd> <dl> <dt>



I file di log includono solo informazioni sull'esito positivo. Per impostazione predefinita, vengono registrati sia gli errori che le transazioni riuscite. Se né **l'opzione HTTP LOGGING FLAG LOG ERRORS \_ \_ \_ \_ \_ ONLY** o **HTTP LOGGING FLAG LOG SUCCESS \_ \_ \_ \_ \_ ONLY** è impostata, vengono registrate sia le informazioni relative agli errori che alle operazioni riuscite.

Questo flag non può essere impostato se è impostato anche il flag **HTTP LOGGING FLAG LOG ERRORS \_ \_ \_ \_ \_ ONLY.** Questi due flag si escludono a vicenda.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                    |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                              |
| Intestazione<br/>                   | <dl> <dt>Http.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Costanti dell'API server HTTP versione 2.0](http-server-api-version-2-0-constants.md)
</dt> <dt>

[**INFORMAZIONI \_ DI REGISTRAZIONE \_ HTTP**](/windows/desktop/api/Http/ns-http-http_logging_info)
</dt> <dt>

[**HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty)
</dt> <dt>

[**HttpSetServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty)
</dt> <dt>

[**Proprietà HttpQueryUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpqueryurlgroupproperty)
</dt> <dt>

[**HttpQueryServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpqueryserversessionproperty)
</dt> </dl>

 

 





