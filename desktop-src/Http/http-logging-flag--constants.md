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
# <a name="http_logging_flag_-constants"></a><span data-ttu-id="553af-103">\_ \_ Costanti flag di registrazione http \_</span><span class="sxs-lookup"><span data-stu-id="553af-103">HTTP\_LOGGING\_FLAG\_ Constants</span></span>

<span data-ttu-id="553af-104">Le costanti del **\_ \_ flag \_ di registrazione http** definiscono le opzioni per configurare la registrazione nell'API del server http.</span><span class="sxs-lookup"><span data-stu-id="553af-104">The **HTTP\_LOGGING\_FLAG\_** constants define the options to configure logging on the HTTP Server API.</span></span>

<span data-ttu-id="553af-105">Queste costanti vengono utilizzate nella struttura di [**\_ \_ informazioni di registrazione http**](/windows/desktop/api/Http/ns-http-http_logging_info) .</span><span class="sxs-lookup"><span data-stu-id="553af-105">These constants are used in the [**HTTP\_LOGGING\_INFO**](/windows/desktop/api/Http/ns-http-http_logging_info) structure.</span></span>

<dl> <dt>

<span data-ttu-id="553af-106"><span id="HTTP_LOGGING_FLAG_LOCAL_TIME_ROLLOVER"></span><span id="http_logging_flag_local_time_rollover"></span>**\_rollover dell' \_ \_ ora locale del flag \_ di \_ registrazione http**</span><span class="sxs-lookup"><span data-stu-id="553af-106"><span id="HTTP_LOGGING_FLAG_LOCAL_TIME_ROLLOVER"></span><span id="http_logging_flag_local_time_rollover"></span>**HTTP\_LOGGING\_FLAG\_LOCAL\_TIME\_ROLLOVER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="553af-107">Il rollover dei file di log è basato sull'ora locale.</span><span class="sxs-lookup"><span data-stu-id="553af-107">The log file rollover is based on local time.</span></span> <span data-ttu-id="553af-108">Per impostazione predefinita, il rollover dei file di log è basato sull'ora UTC (Coordinated Universal Time).</span><span class="sxs-lookup"><span data-stu-id="553af-108">By default, log file rollovers is based on coordinated universal time (UTC).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="553af-109"><span id="_HTTP_LOGGING_FLAG_USE_UTF8_CONVERSION"></span><span id="_http_logging_flag_use_utf8_conversion"></span>**Http \_ FLAG di registrazione \_ \_ usare la \_ \_ conversione UTF8**</span><span class="sxs-lookup"><span data-stu-id="553af-109"><span id="_HTTP_LOGGING_FLAG_USE_UTF8_CONVERSION"></span><span id="_http_logging_flag_use_utf8_conversion"></span> **HTTP\_LOGGING\_FLAG\_USE\_UTF8\_CONVERSION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="553af-110">I campi Unicode vengono convertiti in multibyte UTF8 durante la scrittura nei file di log.</span><span class="sxs-lookup"><span data-stu-id="553af-110">The unicode fields are converted to UTF8 multibytes when writting to the log files.</span></span> <span data-ttu-id="553af-111">Per impostazione predefinita, i file di log vengono scritti con la conversione della tabella codici locale.</span><span class="sxs-lookup"><span data-stu-id="553af-111">By default, the log files are written with the local code page conversion.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="553af-112"><span id="HTTP_LOGGING_FLAG_LOG_ERRORS_ONLY"></span><span id="http_logging_flag_log_errors_only"></span>**\_ \_ \_ solo errori di log del flag \_ di registrazione http \_**</span><span class="sxs-lookup"><span data-stu-id="553af-112"><span id="HTTP_LOGGING_FLAG_LOG_ERRORS_ONLY"></span><span id="http_logging_flag_log_errors_only"></span>**HTTP\_LOGGING\_FLAG\_LOG\_ERRORS\_ONLY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="553af-113">I file di log includono solo le informazioni sugli errori.</span><span class="sxs-lookup"><span data-stu-id="553af-113">The log files include error information only.</span></span> <span data-ttu-id="553af-114">Per impostazione predefinita, vengono registrate sia la risposta di errore che quella di esito positivo.</span><span class="sxs-lookup"><span data-stu-id="553af-114">By default, both error and success responses are logged.</span></span> <span data-ttu-id="553af-115">Se il **flag di \_ registrazione http non \_ \_ Registra \_ \_ solo errori** o se è impostato il **\_ \_ \_ \_ \_ solo log di registrazione http** , viene registrato l'errore e le informazioni di esito positivo.</span><span class="sxs-lookup"><span data-stu-id="553af-115">If neither the **HTTP\_LOGGING\_FLAG\_LOG\_ERRORS\_ONLY** or the **HTTP\_LOGGING\_FLAG\_LOG\_SUCCESS\_ONLY** is set, both error and success information is logged.</span></span>

<span data-ttu-id="553af-116">Non è possibile impostare questo flag se viene impostato anche il flag di **\_ \_ \_ log \_ \_ di registrazione http** .</span><span class="sxs-lookup"><span data-stu-id="553af-116">This flag cannot be set if the **HTTP\_LOGGING\_FLAG\_LOG\_SUCCESS\_ONLY** flag is also set.</span></span> <span data-ttu-id="553af-117">Questi due flag si escludono a vicenda.</span><span class="sxs-lookup"><span data-stu-id="553af-117">These two flags are mutually exclusive.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="553af-118"><span id="_HTTP_LOGGING_FLAG_LOG_SUCCESS_ONLY"></span><span id="_http_logging_flag_log_success_only"></span>**Http \_ REGISTRAZIONE \_ \_ \_ \_ solo log di flag riusciti**</span><span class="sxs-lookup"><span data-stu-id="553af-118"><span id="_HTTP_LOGGING_FLAG_LOG_SUCCESS_ONLY"></span><span id="_http_logging_flag_log_success_only"></span> **HTTP\_LOGGING\_FLAG\_LOG\_SUCCESS\_ONLY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="553af-119">I file di log includono solo le informazioni di esito positivo.</span><span class="sxs-lookup"><span data-stu-id="553af-119">The log files include success information only.</span></span> <span data-ttu-id="553af-120">Per impostazione predefinita, vengono registrati sia gli errori che le transazioni con esito positivo.</span><span class="sxs-lookup"><span data-stu-id="553af-120">By default, both errors and success transactions are logged.</span></span> <span data-ttu-id="553af-121">Se il **flag di \_ registrazione http non \_ \_ Registra \_ \_ solo errori** o se è impostato il **\_ \_ \_ \_ \_ solo log di registrazione http** , viene registrato l'errore e le informazioni di esito positivo.</span><span class="sxs-lookup"><span data-stu-id="553af-121">If neither the **HTTP\_LOGGING\_FLAG\_LOG\_ERRORS\_ONLY** or the **HTTP\_LOGGING\_FLAG\_LOG\_SUCCESS\_ONLY** is set, both error and success information is logged.</span></span>

<span data-ttu-id="553af-122">Impossibile impostare questo flag se viene impostato anche il flag di **\_ registrazione del flag di registrazione \_ \_ \_ \_ http** .</span><span class="sxs-lookup"><span data-stu-id="553af-122">This flag cannot be set if the **HTTP\_LOGGING\_FLAG\_LOG\_ERRORS\_ONLY** flag is also set.</span></span> <span data-ttu-id="553af-123">Questi due flag si escludono a vicenda.</span><span class="sxs-lookup"><span data-stu-id="553af-123">These two flags are mutually exclusive.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="553af-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="553af-124">Requirements</span></span>



| <span data-ttu-id="553af-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="553af-125">Requirement</span></span> | <span data-ttu-id="553af-126">Valore</span><span class="sxs-lookup"><span data-stu-id="553af-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="553af-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="553af-127">Minimum supported client</span></span><br/> | <span data-ttu-id="553af-128">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="553af-128">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="553af-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="553af-129">Minimum supported server</span></span><br/> | <span data-ttu-id="553af-130">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="553af-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="553af-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="553af-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="553af-132"><dt>Http. h</dt></span><span class="sxs-lookup"><span data-stu-id="553af-132"><dt>Http.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="553af-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="553af-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="553af-134">Costanti API server HTTP versione 2,0</span><span class="sxs-lookup"><span data-stu-id="553af-134">HTTP Server API Version 2.0 Constants</span></span>](http-server-api-version-2-0-constants.md)
</dt> <dt>

[<span data-ttu-id="553af-135">**\_informazioni di registrazione http \_**</span><span class="sxs-lookup"><span data-stu-id="553af-135">**HTTP\_LOGGING\_INFO**</span></span>](/windows/desktop/api/Http/ns-http-http_logging_info)
</dt> <dt>

[<span data-ttu-id="553af-136">**HttpSetUrlGroupProperty**</span><span class="sxs-lookup"><span data-stu-id="553af-136">**HttpSetUrlGroupProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty)
</dt> <dt>

[<span data-ttu-id="553af-137">**HttpSetServerSessionProperty**</span><span class="sxs-lookup"><span data-stu-id="553af-137">**HttpSetServerSessionProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty)
</dt> <dt>

[<span data-ttu-id="553af-138">**HttpQueryUrlGroupProperty**</span><span class="sxs-lookup"><span data-stu-id="553af-138">**HttpQueryUrlGroupProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpqueryurlgroupproperty)
</dt> <dt>

[<span data-ttu-id="553af-139">**HttpQueryServerSessionProperty**</span><span class="sxs-lookup"><span data-stu-id="553af-139">**HttpQueryServerSessionProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpqueryserversessionproperty)
</dt> </dl>

 

 





