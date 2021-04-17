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
# <a name="http_auth_enable_-constants"></a><span data-ttu-id="b9a25-103">\_Costanti di \_ Abilitazione dell'autenticazione HTTP \_</span><span class="sxs-lookup"><span data-stu-id="b9a25-103">HTTP\_AUTH\_ENABLE\_ Constants</span></span>

<span data-ttu-id="b9a25-104">Le costanti di **\_ \_ Abilitazione http auth** definiscono gli schemi di autenticazione che possono essere abilitati in un gruppo di URL.</span><span class="sxs-lookup"><span data-stu-id="b9a25-104">The **HTTP\_AUTH\_ENABLE** constants define authentication schemes that can be enabled on a URL Group.</span></span>

<span data-ttu-id="b9a25-105">Queste costanti vengono utilizzate nella struttura delle [**\_ informazioni di \_ autenticazione \_ del server http**](/windows/desktop/api/Http/ns-http-http_server_authentication_info) .</span><span class="sxs-lookup"><span data-stu-id="b9a25-105">These constants are used in the [**HTTP\_SERVER\_AUTHENTICATION\_INFO**](/windows/desktop/api/Http/ns-http-http_server_authentication_info) structure.</span></span>

<dl> <dt>

<span data-ttu-id="b9a25-106"><span id="HTTP_AUTH_ENABLE_BASIC"></span><span id="http_auth_enable_basic"></span>**\_autenticazione HTTP \_ Abilita \_ Basic**</span><span class="sxs-lookup"><span data-stu-id="b9a25-106"><span id="HTTP_AUTH_ENABLE_BASIC"></span><span id="http_auth_enable_basic"></span>**HTTP\_AUTH\_ENABLE\_BASIC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b9a25-107">Lo schema di autenticazione di base è abilitato.</span><span class="sxs-lookup"><span data-stu-id="b9a25-107">The Basic authentication scheme is enabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b9a25-108"><span id="HTTP_AUTH_ENABLE_DIGEST"></span><span id="http_auth_enable_digest"></span>**\_autenticazione HTTP \_ Abilita \_ digest**</span><span class="sxs-lookup"><span data-stu-id="b9a25-108"><span id="HTTP_AUTH_ENABLE_DIGEST"></span><span id="http_auth_enable_digest"></span>**HTTP\_AUTH\_ENABLE\_DIGEST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b9a25-109">Lo schema di autenticazione del digest è abilitato.</span><span class="sxs-lookup"><span data-stu-id="b9a25-109">The Digest authentication scheme is enabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b9a25-110"><span id="HTTP_AUTH_ENABLE_KERBEROS"></span><span id="http_auth_enable_kerberos"></span>**\_autenticazione HTTP \_ Abilita \_ Kerberos**</span><span class="sxs-lookup"><span data-stu-id="b9a25-110"><span id="HTTP_AUTH_ENABLE_KERBEROS"></span><span id="http_auth_enable_kerberos"></span>**HTTP\_AUTH\_ENABLE\_KERBEROS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b9a25-111">Lo schema di autenticazione Kerberos è abilitato.</span><span class="sxs-lookup"><span data-stu-id="b9a25-111">The Kerberos authentication scheme is enabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b9a25-112"><span id="HTTP_AUTH_EX_FLAG_ENABLE_KERBEROS_CREDENTIAL_CACHING"></span><span id="http_auth_ex_flag_enable_kerberos_credential_caching"></span>**\_ \_ \_ \_ Abilitazione della \_ \_ \_ memorizzazione nella cache delle credenziali Kerberos tramite il contrassegno http auth**</span><span class="sxs-lookup"><span data-stu-id="b9a25-112"><span id="HTTP_AUTH_EX_FLAG_ENABLE_KERBEROS_CREDENTIAL_CACHING"></span><span id="http_auth_ex_flag_enable_kerberos_credential_caching"></span>**HTTP\_AUTH\_EX\_FLAG\_ENABLE\_KERBEROS\_CREDENTIAL\_CACHING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b9a25-113">La memorizzazione nella cache delle credenziali Kerberos è abilitata.</span><span class="sxs-lookup"><span data-stu-id="b9a25-113">Kerberos credential caching is enabled.</span></span>

<span data-ttu-id="b9a25-114">**Windows Server 2003 e precedenti:** Non disponibile.</span><span class="sxs-lookup"><span data-stu-id="b9a25-114">**Windows Server 2003 and before:** Not available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b9a25-115"><span id="HTTP_AUTH_EX_FLAG_CAPTURE_CREDENTIAL"></span><span id="http_auth_ex_flag_capture_credential"></span>**\_credenziali di \_ \_ acquisizione del flag http auth ex \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b9a25-115"><span id="HTTP_AUTH_EX_FLAG_CAPTURE_CREDENTIAL"></span><span id="http_auth_ex_flag_capture_credential"></span>**HTTP\_AUTH\_EX\_FLAG\_CAPTURE\_CREDENTIAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b9a25-116">L'API server HTTP acquisisce l'identità del chiamante e la usa per l'autenticazione solo per gli schemi Negotiate e Kerberos.</span><span class="sxs-lookup"><span data-stu-id="b9a25-116">The HTTP Server API captures the caller identity and uses it for authentication for Negotiate and Kerberos schemes only.</span></span>

<span data-ttu-id="b9a25-117">**Windows Server 2003 e precedenti:** Non disponibile.</span><span class="sxs-lookup"><span data-stu-id="b9a25-117">**Windows Server 2003 and before:** Not available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b9a25-118"><span id="HTTP_AUTH_ENABLE_NTLM"></span><span id="http_auth_enable_ntlm"></span>**\_autenticazione HTTP \_ Abilita \_ NTLM**</span><span class="sxs-lookup"><span data-stu-id="b9a25-118"><span id="HTTP_AUTH_ENABLE_NTLM"></span><span id="http_auth_enable_ntlm"></span>**HTTP\_AUTH\_ENABLE\_NTLM**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b9a25-119">Lo schema di autenticazione NTLM è abilitato.</span><span class="sxs-lookup"><span data-stu-id="b9a25-119">The NTLM authentication scheme is enabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b9a25-120"><span id="HTTP_AUTH_ENABLE_NEGOTIATE"></span><span id="http_auth_enable_negotiate"></span>**\_ \_ Abilita negoziazione http \_ AUTH**</span><span class="sxs-lookup"><span data-stu-id="b9a25-120"><span id="HTTP_AUTH_ENABLE_NEGOTIATE"></span><span id="http_auth_enable_negotiate"></span>**HTTP\_AUTH\_ENABLE\_NEGOTIATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b9a25-121">Lo schema di autenticazione Negotiate è abilitato.</span><span class="sxs-lookup"><span data-stu-id="b9a25-121">The Negotiate authentication scheme is enabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b9a25-122"><span id="HTTP_AUTH_ENABLE_ALL"></span><span id="http_auth_enable_all"></span>**\_ \_ Abilita \_ tutti gli http auth**</span><span class="sxs-lookup"><span data-stu-id="b9a25-122"><span id="HTTP_AUTH_ENABLE_ALL"></span><span id="http_auth_enable_all"></span>**HTTP\_AUTH\_ENABLE\_ALL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b9a25-123">Tutti gli schemi di autenticazione sono abilitati.</span><span class="sxs-lookup"><span data-stu-id="b9a25-123">All authentication schemes are enabled.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b9a25-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b9a25-124">Requirements</span></span>



| <span data-ttu-id="b9a25-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="b9a25-125">Requirement</span></span> | <span data-ttu-id="b9a25-126">Valore</span><span class="sxs-lookup"><span data-stu-id="b9a25-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="b9a25-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b9a25-127">Minimum supported client</span></span><br/> | <span data-ttu-id="b9a25-128">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b9a25-128">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b9a25-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b9a25-129">Minimum supported server</span></span><br/> | <span data-ttu-id="b9a25-130">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b9a25-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="b9a25-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b9a25-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="b9a25-132"><dt>Http. h</dt></span><span class="sxs-lookup"><span data-stu-id="b9a25-132"><dt>Http.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b9a25-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b9a25-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9a25-134">Costanti API server HTTP versione 2,0</span><span class="sxs-lookup"><span data-stu-id="b9a25-134">HTTP Server API Version 2.0 Constants</span></span>](http-server-api-version-2-0-constants.md)
</dt> <dt>

[<span data-ttu-id="b9a25-135">**\_informazioni di \_ autenticazione \_ Server http**</span><span class="sxs-lookup"><span data-stu-id="b9a25-135">**HTTP\_SERVER\_AUTHENTICATION\_INFO**</span></span>](/windows/desktop/api/Http/ns-http-http_server_authentication_info)
</dt> <dt>

[<span data-ttu-id="b9a25-136">**HttpSetUrlGroupProperty**</span><span class="sxs-lookup"><span data-stu-id="b9a25-136">**HttpSetUrlGroupProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty)
</dt> <dt>

[<span data-ttu-id="b9a25-137">**HttpSetServerSessionProperty**</span><span class="sxs-lookup"><span data-stu-id="b9a25-137">**HttpSetServerSessionProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty)
</dt> <dt>

[<span data-ttu-id="b9a25-138">**HttpQueryUrlGroupProperty**</span><span class="sxs-lookup"><span data-stu-id="b9a25-138">**HttpQueryUrlGroupProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpqueryurlgroupproperty)
</dt> <dt>

[<span data-ttu-id="b9a25-139">**HttpQueryServerSessionProperty**</span><span class="sxs-lookup"><span data-stu-id="b9a25-139">**HttpQueryServerSessionProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpqueryserversessionproperty)
</dt> </dl>

 

 





