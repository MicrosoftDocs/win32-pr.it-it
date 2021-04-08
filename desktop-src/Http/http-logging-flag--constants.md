---
title: Costanti HTTP_LOGGING_FLAG_ (http. h)
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
ms.openlocfilehash: c501fc3ab646ab65fa039a5ff5e7d2dc0578002a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742503"
---
# <a name="http_logging_flag_-constants"></a>\_ \_ Costanti flag di registrazione http \_

Le costanti del **\_ \_ flag \_ di registrazione http** definiscono le opzioni per configurare la registrazione nell'API del server http.

Queste costanti vengono utilizzate nella struttura di [**\_ \_ informazioni di registrazione http**](/windows/desktop/api/Http/ns-http-http_logging_info) .

<dl> <dt>

<span id="HTTP_LOGGING_FLAG_LOCAL_TIME_ROLLOVER"></span><span id="http_logging_flag_local_time_rollover"></span>**\_rollover dell' \_ \_ ora locale del flag \_ di \_ registrazione http**
</dt> <dd> <dl> <dt>



Il rollover dei file di log è basato sull'ora locale. Per impostazione predefinita, il rollover dei file di log è basato sull'ora UTC (Coordinated Universal Time).


</dt> </dl> </dd> <dt>

<span id="_HTTP_LOGGING_FLAG_USE_UTF8_CONVERSION"></span><span id="_http_logging_flag_use_utf8_conversion"></span>**Http \_ FLAG di registrazione \_ \_ usare la \_ \_ conversione UTF8**
</dt> <dd> <dl> <dt>



I campi Unicode vengono convertiti in multibyte UTF8 durante la scrittura nei file di log. Per impostazione predefinita, i file di log vengono scritti con la conversione della tabella codici locale.


</dt> </dl> </dd> <dt>

<span id="HTTP_LOGGING_FLAG_LOG_ERRORS_ONLY"></span><span id="http_logging_flag_log_errors_only"></span>**\_ \_ \_ solo errori di log del flag \_ di registrazione http \_**
</dt> <dd> <dl> <dt>



I file di log includono solo le informazioni sugli errori. Per impostazione predefinita, vengono registrate sia la risposta di errore che quella di esito positivo. Se il **flag di \_ registrazione http non \_ \_ Registra \_ \_ solo errori** o se è impostato il **\_ \_ \_ \_ \_ solo log di registrazione http** , viene registrato l'errore e le informazioni di esito positivo.

Non è possibile impostare questo flag se viene impostato anche il flag di **\_ \_ \_ log \_ \_ di registrazione http** . Questi due flag si escludono a vicenda.


</dt> </dl> </dd> <dt>

<span id="_HTTP_LOGGING_FLAG_LOG_SUCCESS_ONLY"></span><span id="_http_logging_flag_log_success_only"></span>**Http \_ REGISTRAZIONE \_ \_ \_ \_ solo log di flag riusciti**
</dt> <dd> <dl> <dt>



I file di log includono solo le informazioni di esito positivo. Per impostazione predefinita, vengono registrati sia gli errori che le transazioni con esito positivo. Se il **flag di \_ registrazione http non \_ \_ Registra \_ \_ solo errori** o se è impostato il **\_ \_ \_ \_ \_ solo log di registrazione http** , viene registrato l'errore e le informazioni di esito positivo.

Impossibile impostare questo flag se viene impostato anche il flag di **\_ registrazione del flag di registrazione \_ \_ \_ \_ http** . Questi due flag si escludono a vicenda.


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

[**\_informazioni di registrazione http \_**](/windows/desktop/api/Http/ns-http-http_logging_info)
</dt> <dt>

[**HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty)
</dt> <dt>

[**HttpSetServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty)
</dt> <dt>

[**HttpQueryUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpqueryurlgroupproperty)
</dt> <dt>

[**HttpQueryServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpqueryserversessionproperty)
</dt> </dl>

 

 





