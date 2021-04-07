---
description: Descrive i codici di errore 9000-11999 definiti nel file di intestazione WinError. h ed è destinato agli sviluppatori.
ms.assetid: 27fe3fee-4ae3-43f1-a1f2-91c935e9851b
title: Codici di errore di sistema (9000-11999) (WinError. h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: 01eb071962d8d0f5beb801067ce1d72adc796bad
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748378"
---
# <a name="system-error-codes-9000-11999"></a><span data-ttu-id="6b3a1-103">Codici di errore di sistema (9000-11999)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-103">System Error Codes (9000-11999)</span></span>

> [!NOTE]
> <span data-ttu-id="6b3a1-104">Queste informazioni sono destinate agli sviluppatori che effettuano il debug degli errori di sistema.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-104">This information is intended for developers debugging system errors.</span></span> <span data-ttu-id="6b3a1-105">Per altri errori, ad esempio problemi con Windows Update, è disponibile un elenco di risorse nella pagina [codici di errore](system-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="6b3a1-105">For other errors, such as issues with Windows Update, there is a list of resources on the [Error codes](system-error-codes.md) page.</span></span>

<span data-ttu-id="6b3a1-106">Nell'elenco seguente vengono descritti i [codici di errore di sistema](system-error-codes.md) (errori da 9000 a 11999).</span><span class="sxs-lookup"><span data-stu-id="6b3a1-106">The following list describes [system error codes](system-error-codes.md) (errors 9000 to 11999).</span></span> <span data-ttu-id="6b3a1-107">Vengono restituiti dalla funzione [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) quando molte funzioni hanno esito negativo.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-107">They are returned by the [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function when many functions fail.</span></span> <span data-ttu-id="6b3a1-108">Per recuperare il testo della descrizione dell'errore nell'applicazione, usare la funzione [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) con il **formato \_ Message from flag \_ di \_ sistema** .</span><span class="sxs-lookup"><span data-stu-id="6b3a1-108">To retrieve the description text for the error in your application, use the [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) function with the **FORMAT\_MESSAGE\_FROM\_SYSTEM** flag.</span></span>

<dl> <dt>

<span data-ttu-id="6b3a1-109"><span id="DNS_ERROR_RCODE_FORMAT_ERROR"></span><span id="dns_error_rcode_format_error"></span>**errore \_ di \_ formato RCODE errore \_ DNS \_**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-109"><span id="DNS_ERROR_RCODE_FORMAT_ERROR"></span><span id="dns_error_rcode_format_error"></span>**DNS\_ERROR\_RCODE\_FORMAT\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-110">9001 (0x2329)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-110">9001 (0x2329)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-111">Il server DNS non riesce a interpretare il formato.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-111">DNS server unable to interpret format.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-112"><span id="DNS_ERROR_RCODE_SERVER_FAILURE"></span><span id="dns_error_rcode_server_failure"></span>**\_errore del \_ \_ Server RCODE errore DNS \_**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-112"><span id="DNS_ERROR_RCODE_SERVER_FAILURE"></span><span id="dns_error_rcode_server_failure"></span>**DNS\_ERROR\_RCODE\_SERVER\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-113">9002 (0x232A)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-113">9002 (0x232A)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-114">Errore del server DNS.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-114">DNS server failure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-115"><span id="DNS_ERROR_RCODE_NAME_ERROR"></span><span id="dns_error_rcode_name_error"></span>**errore \_ DNS \_ RCODE \_ nome \_ errore**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-115"><span id="DNS_ERROR_RCODE_NAME_ERROR"></span><span id="dns_error_rcode_name_error"></span>**DNS\_ERROR\_RCODE\_NAME\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-116">9003 (0x232B)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-116">9003 (0x232B)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-117">Nome DNS inesistente.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-117">DNS name does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-118"><span id="DNS_ERROR_RCODE_NOT_IMPLEMENTED"></span><span id="dns_error_rcode_not_implemented"></span>**\_errore DNS \_ RCODE \_ non \_ implementato**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-118"><span id="DNS_ERROR_RCODE_NOT_IMPLEMENTED"></span><span id="dns_error_rcode_not_implemented"></span>**DNS\_ERROR\_RCODE\_NOT\_IMPLEMENTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-119">9004 (0x232C)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-119">9004 (0x232C)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-120">Richiesta DNS non supportata dal server dei nomi.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-120">DNS request not supported by name server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-121"><span id="DNS_ERROR_RCODE_REFUSED"></span><span id="dns_error_rcode_refused"></span>**\_errore DNS \_ RCODE \_ rifiutato**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-121"><span id="DNS_ERROR_RCODE_REFUSED"></span><span id="dns_error_rcode_refused"></span>**DNS\_ERROR\_RCODE\_REFUSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-122">9005 (0x232D)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-122">9005 (0x232D)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-123">Operazione DNS rifiutata.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-123">DNS operation refused.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-124"><span id="DNS_ERROR_RCODE_YXDOMAIN"></span><span id="dns_error_rcode_yxdomain"></span>**\_errore DNS \_ RCODE \_ YXDOMAIN**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-124"><span id="DNS_ERROR_RCODE_YXDOMAIN"></span><span id="dns_error_rcode_yxdomain"></span>**DNS\_ERROR\_RCODE\_YXDOMAIN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-125">9006 (0x232E)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-125">9006 (0x232E)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-126">Il nome DNS che non esiste, esiste.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-126">DNS name that ought not exist, does exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-127"><span id="DNS_ERROR_RCODE_YXRRSET"></span><span id="dns_error_rcode_yxrrset"></span>**\_errore DNS \_ RCODE \_ YXRRSET**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-127"><span id="DNS_ERROR_RCODE_YXRRSET"></span><span id="dns_error_rcode_yxrrset"></span>**DNS\_ERROR\_RCODE\_YXRRSET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-128">9007 (0x232F)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-128">9007 (0x232F)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-129">Il set di RR DNS che non esiste, esiste.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-129">DNS RR set that ought not exist, does exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-130"><span id="DNS_ERROR_RCODE_NXRRSET"></span><span id="dns_error_rcode_nxrrset"></span>**\_errore DNS \_ RCODE \_ NXRRSET**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-130"><span id="DNS_ERROR_RCODE_NXRRSET"></span><span id="dns_error_rcode_nxrrset"></span>**DNS\_ERROR\_RCODE\_NXRRSET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-131">9008 (0x2330)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-131">9008 (0x2330)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-132">Il set di RR DNS che deve esistere non esiste.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-132">DNS RR set that ought to exist, does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-133"><span id="DNS_ERROR_RCODE_NOTAUTH"></span><span id="dns_error_rcode_notauth"></span>**\_errore DNS \_ RCODE \_ NOTAUTH**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-133"><span id="DNS_ERROR_RCODE_NOTAUTH"></span><span id="dns_error_rcode_notauth"></span>**DNS\_ERROR\_RCODE\_NOTAUTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-134">9009 (0x2331)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-134">9009 (0x2331)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-135">Server DNS non autorevole per la zona.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-135">DNS server not authoritative for zone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-136"><span id="DNS_ERROR_RCODE_NOTZONE"></span><span id="dns_error_rcode_notzone"></span>**\_errore DNS \_ RCODE \_ NOTZONE**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-136"><span id="DNS_ERROR_RCODE_NOTZONE"></span><span id="dns_error_rcode_notzone"></span>**DNS\_ERROR\_RCODE\_NOTZONE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-137">9010 (0x2332)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-137">9010 (0x2332)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-138">Il nome DNS in Update o prereq non è nell'area.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-138">DNS name in update or prereq is not in zone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-139"><span id="DNS_ERROR_RCODE_BADSIG"></span><span id="dns_error_rcode_badsig"></span>**\_errore DNS \_ RCODE \_ BADSIG**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-139"><span id="DNS_ERROR_RCODE_BADSIG"></span><span id="dns_error_rcode_badsig"></span>**DNS\_ERROR\_RCODE\_BADSIG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-140">9016 (0x2338)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-140">9016 (0x2338)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-141">Impossibile verificare la firma DNS.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-141">DNS signature failed to verify.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-142"><span id="DNS_ERROR_RCODE_BADKEY"></span><span id="dns_error_rcode_badkey"></span>**\_errore DNS \_ RCODE \_ BADKEY**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-142"><span id="DNS_ERROR_RCODE_BADKEY"></span><span id="dns_error_rcode_badkey"></span>**DNS\_ERROR\_RCODE\_BADKEY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-143">9017 (0x2339)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-143">9017 (0x2339)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-144">Chiave DNS non valida.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-144">DNS bad key.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-145"><span id="DNS_ERROR_RCODE_BADTIME"></span><span id="dns_error_rcode_badtime"></span>**\_errore DNS \_ RCODE \_ BADTIME**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-145"><span id="DNS_ERROR_RCODE_BADTIME"></span><span id="dns_error_rcode_badtime"></span>**DNS\_ERROR\_RCODE\_BADTIME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-146">9018 (0x233A)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-146">9018 (0x233A)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-147">Validità della firma DNS scaduta.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-147">DNS signature validity expired.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-148"><span id="DNS_ERROR_KEYMASTER_REQUIRED"></span><span id="dns_error_keymaster_required"></span>**errore DNS necessario per il \_ \_ master \_**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-148"><span id="DNS_ERROR_KEYMASTER_REQUIRED"></span><span id="dns_error_keymaster_required"></span>**DNS\_ERROR\_KEYMASTER\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-149">9101 (0x238D)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-149">9101 (0x238D)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-150">Questa operazione può essere eseguita solo dal server DNS che funge da Master chiavi per la zona.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-150">Only the DNS server acting as the key master for the zone may perform this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-151"><span id="DNS_ERROR_NOT_ALLOWED_ON_SIGNED_ZONE"></span><span id="dns_error_not_allowed_on_signed_zone"></span>**\_errore DNS \_ non \_ consentito \_ nell' \_ area firmata \_**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-151"><span id="DNS_ERROR_NOT_ALLOWED_ON_SIGNED_ZONE"></span><span id="dns_error_not_allowed_on_signed_zone"></span>**DNS\_ERROR\_NOT\_ALLOWED\_ON\_SIGNED\_ZONE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-152">9102 (0x238E)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-152">9102 (0x238E)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-153">Questa operazione non è consentita in una zona firmata o con chiavi di firma.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-153">This operation is not allowed on a zone that is signed or has signing keys.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-154"><span id="DNS_ERROR_NSEC3_INCOMPATIBLE_WITH_RSA_SHA1"></span><span id="dns_error_nsec3_incompatible_with_rsa_sha1"></span>**\_Errore DNS \_ NSEC3 \_ incompatibile \_ con \_ RSA \_ SHA1**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-154"><span id="DNS_ERROR_NSEC3_INCOMPATIBLE_WITH_RSA_SHA1"></span><span id="dns_error_nsec3_incompatible_with_rsa_sha1"></span>**DNS\_ERROR\_NSEC3\_INCOMPATIBLE\_WITH\_RSA\_SHA1**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-155">9103 (0x238F)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-155">9103 (0x238F)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-156">NSEC3 non è compatibile con l'algoritmo RSA-SHA-1.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-156">NSEC3 is not compatible with the RSA-SHA-1 algorithm.</span></span> <span data-ttu-id="6b3a1-157">Scegliere un algoritmo diverso o usare NSEC.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-157">Choose a different algorithm or use NSEC.</span></span>

<span data-ttu-id="6b3a1-158">Questo valore è stato anche **denominato \_ errore \_ DNS \_ \_ parametri NSEC3 non validi**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-158">This value was also named **DNS\_ERROR\_INVALID\_NSEC3\_PARAMETERS**</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-159"><span id="DNS_ERROR_NOT_ENOUGH_SIGNING_KEY_DESCRIPTORS"></span><span id="dns_error_not_enough_signing_key_descriptors"></span>**\_errore DNS \_ non sufficiente per i \_ \_ \_ \_ descrittori chiave di firma**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-159"><span id="DNS_ERROR_NOT_ENOUGH_SIGNING_KEY_DESCRIPTORS"></span><span id="dns_error_not_enough_signing_key_descriptors"></span>**DNS\_ERROR\_NOT\_ENOUGH\_SIGNING\_KEY\_DESCRIPTORS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-160">9104 (0x2390)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-160">9104 (0x2390)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-161">Il numero di chiavi di firma non è sufficiente per la zona.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-161">The zone does not have enough signing keys.</span></span> <span data-ttu-id="6b3a1-162">Deve essere presente almeno una chiave di firma della chiave (KSK) e almeno una chiave di firma della zona (ZSK).</span><span class="sxs-lookup"><span data-stu-id="6b3a1-162">There must be at least one key signing key (KSK) and at least one zone signing key (ZSK).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-163"><span id="DNS_ERROR_UNSUPPORTED_ALGORITHM"></span><span id="dns_error_unsupported_algorithm"></span>**\_errore DNS \_ algoritmo non supportato \_**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-163"><span id="DNS_ERROR_UNSUPPORTED_ALGORITHM"></span><span id="dns_error_unsupported_algorithm"></span>**DNS\_ERROR\_UNSUPPORTED\_ALGORITHM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-164">9105 (0x2391)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-164">9105 (0x2391)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-165">L'algoritmo specificato non è supportato.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-165">The specified algorithm is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-166"><span id="DNS_ERROR_INVALID_KEY_SIZE"></span><span id="dns_error_invalid_key_size"></span>**\_errore DNS \_ \_ dimensione chiave non valida \_**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-166"><span id="DNS_ERROR_INVALID_KEY_SIZE"></span><span id="dns_error_invalid_key_size"></span>**DNS\_ERROR\_INVALID\_KEY\_SIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-167">9106 (0x2392)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-167">9106 (0x2392)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-168">La dimensione della chiave specificata non è supportata.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-168">The specified key size is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-169"><span id="DNS_ERROR_SIGNING_KEY_NOT_ACCESSIBLE"></span><span id="dns_error_signing_key_not_accessible"></span>**\_chiave di firma degli errori DNS \_ \_ \_ non \_ accessibile**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-169"><span id="DNS_ERROR_SIGNING_KEY_NOT_ACCESSIBLE"></span><span id="dns_error_signing_key_not_accessible"></span>**DNS\_ERROR\_SIGNING\_KEY\_NOT\_ACCESSIBLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-170">9107 (0x2393)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-170">9107 (0x2393)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-171">Una o più chiavi di firma per una zona non sono accessibili al server DNS.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-171">One or more of the signing keys for a zone are not accessible to the DNS server.</span></span> <span data-ttu-id="6b3a1-172">La firma della zona non sarà operativa fino a quando l'errore non viene risolto.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-172">Zone signing will not be operational until this error is resolved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-173"><span id="DNS_ERROR_KSP_DOES_NOT_SUPPORT_PROTECTION"></span><span id="dns_error_ksp_does_not_support_protection"></span>**\_il KSP dell'errore DNS non \_ \_ \_ supporta la \_ \_ protezione**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-173"><span id="DNS_ERROR_KSP_DOES_NOT_SUPPORT_PROTECTION"></span><span id="dns_error_ksp_does_not_support_protection"></span>**DNS\_ERROR\_KSP\_DOES\_NOT\_SUPPORT\_PROTECTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-174">9108 (0x2394)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-174">9108 (0x2394)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-175">Il provider di archiviazione chiavi specificato non supporta la protezione dei dati DPAPI + +.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-175">The specified key storage provider does not support DPAPI++ data protection.</span></span> <span data-ttu-id="6b3a1-176">La firma della zona non sarà operativa fino a quando l'errore non viene risolto.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-176">Zone signing will not be operational until this error is resolved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-177"><span id="DNS_ERROR_UNEXPECTED_DATA_PROTECTION_ERROR"></span><span id="dns_error_unexpected_data_protection_error"></span>**errore DNS \_ errore di \_ \_ \_ protezione \_ dati imprevisto**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-177"><span id="DNS_ERROR_UNEXPECTED_DATA_PROTECTION_ERROR"></span><span id="dns_error_unexpected_data_protection_error"></span>**DNS\_ERROR\_UNEXPECTED\_DATA\_PROTECTION\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-178">9109 (0x2395)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-178">9109 (0x2395)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-179">Si è verificato un errore di DPAPI + + imprevisto.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-179">An unexpected DPAPI++ error was encountered.</span></span> <span data-ttu-id="6b3a1-180">La firma della zona non sarà operativa fino a quando l'errore non viene risolto.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-180">Zone signing will not be operational until this error is resolved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-181"><span id="DNS_ERROR_UNEXPECTED_CNG_ERROR"></span><span id="dns_error_unexpected_cng_error"></span>**errore \_ errore \_ CNG imprevisto del \_ DNS \_**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-181"><span id="DNS_ERROR_UNEXPECTED_CNG_ERROR"></span><span id="dns_error_unexpected_cng_error"></span>**DNS\_ERROR\_UNEXPECTED\_CNG\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-182">9110 (0x2396)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-182">9110 (0x2396)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-183">Si è verificato un errore di crittografia imprevisto.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-183">An unexpected crypto error was encountered.</span></span> <span data-ttu-id="6b3a1-184">La firma della zona potrebbe non essere operativa fino a quando l'errore non viene risolto.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-184">Zone signing may not be operational until this error is resolved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-185"><span id="DNS_ERROR_UNKNOWN_SIGNING_PARAMETER_VERSION"></span><span id="dns_error_unknown_signing_parameter_version"></span>**\_versione del \_ \_ parametro di firma sconosciuta con errore \_ DNS \_**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-185"><span id="DNS_ERROR_UNKNOWN_SIGNING_PARAMETER_VERSION"></span><span id="dns_error_unknown_signing_parameter_version"></span>**DNS\_ERROR\_UNKNOWN\_SIGNING\_PARAMETER\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-186">9111 (0x2397)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-186">9111 (0x2397)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-187">Il server DNS ha rilevato una chiave di firma con una versione sconosciuta.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-187">The DNS server encountered a signing key with an unknown version.</span></span> <span data-ttu-id="6b3a1-188">La firma della zona non sarà operativa fino a quando l'errore non viene risolto.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-188">Zone signing will not be operational until this error is resolved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-189"><span id="DNS_ERROR_KSP_NOT_ACCESSIBLE"></span><span id="dns_error_ksp_not_accessible"></span>**\_errore DNS \_ KSP \_ non \_ accessibile**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-189"><span id="DNS_ERROR_KSP_NOT_ACCESSIBLE"></span><span id="dns_error_ksp_not_accessible"></span>**DNS\_ERROR\_KSP\_NOT\_ACCESSIBLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-190">9112 (0x2398)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-190">9112 (0x2398)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-191">Il provider di servizi chiave specificato non può essere aperto dal server DNS.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-191">The specified key service provider cannot be opened by the DNS server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-192"><span id="DNS_ERROR_TOO_MANY_SKDS"></span><span id="dns_error_too_many_skds"></span>**\_errore DNS \_ troppi \_ \_ SKDS**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-192"><span id="DNS_ERROR_TOO_MANY_SKDS"></span><span id="dns_error_too_many_skds"></span>**DNS\_ERROR\_TOO\_MANY\_SKDS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-193">9113 (0x2399)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-193">9113 (0x2399)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-194">Il server DNS non è in grado di accettare altre chiavi di firma con l'algoritmo e il valore del flag KSK specificati per questa zona.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-194">The DNS server cannot accept any more signing keys with the specified algorithm and KSK flag value for this zone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-195"><span id="DNS_ERROR_INVALID_ROLLOVER_PERIOD"></span><span id="dns_error_invalid_rollover_period"></span>**errore DNS- \_ \_ periodo di rollover non valido \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-195"><span id="DNS_ERROR_INVALID_ROLLOVER_PERIOD"></span><span id="dns_error_invalid_rollover_period"></span>**DNS\_ERROR\_INVALID\_ROLLOVER\_PERIOD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-196">9114 (0x239A)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-196">9114 (0x239A)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-197">Il periodo di rollover specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-197">The specified rollover period is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-198"><span id="DNS_ERROR_INVALID_INITIAL_ROLLOVER_OFFSET"></span><span id="dns_error_invalid_initial_rollover_offset"></span>**errore DNS con \_ \_ \_ offset di rollover iniziale non valido \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-198"><span id="DNS_ERROR_INVALID_INITIAL_ROLLOVER_OFFSET"></span><span id="dns_error_invalid_initial_rollover_offset"></span>**DNS\_ERROR\_INVALID\_INITIAL\_ROLLOVER\_OFFSET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-199">9115 (0x239B)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-199">9115 (0x239B)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-200">L'offset di rollover iniziale specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-200">The specified initial rollover offset is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-201"><span id="DNS_ERROR_ROLLOVER_IN_PROGRESS"></span><span id="dns_error_rollover_in_progress"></span>**\_rollover degli errori DNS \_ \_ in \_ corso**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-201"><span id="DNS_ERROR_ROLLOVER_IN_PROGRESS"></span><span id="dns_error_rollover_in_progress"></span>**DNS\_ERROR\_ROLLOVER\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-202">9116 (0x239C)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-202">9116 (0x239C)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-203">La chiave di firma specificata è già in corso di rollup delle chiavi.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-203">The specified signing key is already in process of rolling over keys.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-204"><span id="DNS_ERROR_STANDBY_KEY_NOT_PRESENT"></span><span id="dns_error_standby_key_not_present"></span>**\_ \_ chiave standby errore \_ DNS \_ non \_ presente**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-204"><span id="DNS_ERROR_STANDBY_KEY_NOT_PRESENT"></span><span id="dns_error_standby_key_not_present"></span>**DNS\_ERROR\_STANDBY\_KEY\_NOT\_PRESENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-205">9117 (0x239D)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-205">9117 (0x239D)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-206">La chiave di firma specificata non dispone di una chiave standby da revocare.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-206">The specified signing key does not have a standby key to revoke.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-207"><span id="DNS_ERROR_NOT_ALLOWED_ON_ZSK"></span><span id="dns_error_not_allowed_on_zsk"></span>**\_errore DNS \_ non \_ consentito \_ in \_ ZSK**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-207"><span id="DNS_ERROR_NOT_ALLOWED_ON_ZSK"></span><span id="dns_error_not_allowed_on_zsk"></span>**DNS\_ERROR\_NOT\_ALLOWED\_ON\_ZSK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-208">9118 (0x239E)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-208">9118 (0x239E)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-209">Questa operazione non è consentita in una chiave di firma della zona (ZSK).</span><span class="sxs-lookup"><span data-stu-id="6b3a1-209">This operation is not allowed on a zone signing key (ZSK).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-210"><span id="DNS_ERROR_NOT_ALLOWED_ON_ACTIVE_SKD"></span><span id="dns_error_not_allowed_on_active_skd"></span>**\_errore DNS \_ non \_ consentito \_ in \_ \_ SKD attivo**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-210"><span id="DNS_ERROR_NOT_ALLOWED_ON_ACTIVE_SKD"></span><span id="dns_error_not_allowed_on_active_skd"></span>**DNS\_ERROR\_NOT\_ALLOWED\_ON\_ACTIVE\_SKD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-211">9119 (0x239F)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-211">9119 (0x239F)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-212">Questa operazione non è consentita su una chiave di firma attiva.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-212">This operation is not allowed on an active signing key.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-213"><span id="DNS_ERROR_ROLLOVER_ALREADY_QUEUED"></span><span id="dns_error_rollover_already_queued"></span>**\_rollover degli errori DNS \_ \_ già \_ accodato**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-213"><span id="DNS_ERROR_ROLLOVER_ALREADY_QUEUED"></span><span id="dns_error_rollover_already_queued"></span>**DNS\_ERROR\_ROLLOVER\_ALREADY\_QUEUED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-214">9120 (0x23A0)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-214">9120 (0x23A0)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-215">La chiave di firma specificata è già accodata per il rollover.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-215">The specified signing key is already queued for rollover.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-216"><span id="DNS_ERROR_NOT_ALLOWED_ON_UNSIGNED_ZONE"></span><span id="dns_error_not_allowed_on_unsigned_zone"></span>**\_errore DNS \_ non \_ consentito \_ in una \_ zona non firmata \_**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-216"><span id="DNS_ERROR_NOT_ALLOWED_ON_UNSIGNED_ZONE"></span><span id="dns_error_not_allowed_on_unsigned_zone"></span>**DNS\_ERROR\_NOT\_ALLOWED\_ON\_UNSIGNED\_ZONE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-217">9121 (0x23A1)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-217">9121 (0x23A1)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-218">Questa operazione non è consentita in una zona non firmata.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-218">This operation is not allowed on an unsigned zone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-219"><span id="DNS_ERROR_BAD_KEYMASTER"></span><span id="dns_error_bad_keymaster"></span>**\_errore DNS \_ errore \_ Master**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-219"><span id="DNS_ERROR_BAD_KEYMASTER"></span><span id="dns_error_bad_keymaster"></span>**DNS\_ERROR\_BAD\_KEYMASTER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-220">9122 (0x23A2)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-220">9122 (0x23A2)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-221">Non è stato possibile completare l'operazione perché il server DNS elencato come Master chiavi corrente per questa zona è inattivo o non è configurato correttamente.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-221">This operation could not be completed because the DNS server listed as the current key master for this zone is down or misconfigured.</span></span> <span data-ttu-id="6b3a1-222">Risolvere il problema nel Master chiavi corrente per questa zona oppure utilizzare un altro server DNS per requisire il ruolo di Master chiavi.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-222">Resolve the problem on the current key master for this zone or use another DNS server to seize the key master role.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-223"><span id="DNS_ERROR_INVALID_SIGNATURE_VALIDITY_PERIOD"></span><span id="dns_error_invalid_signature_validity_period"></span>**\_errore DNS \_ \_ periodo di validità della firma non valido \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-223"><span id="DNS_ERROR_INVALID_SIGNATURE_VALIDITY_PERIOD"></span><span id="dns_error_invalid_signature_validity_period"></span>**DNS\_ERROR\_INVALID\_SIGNATURE\_VALIDITY\_PERIOD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-224">9123 (0x23A3)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-224">9123 (0x23A3)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-225">Il periodo di validità della firma specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-225">The specified signature validity period is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-226"><span id="DNS_ERROR_INVALID_NSEC3_ITERATION_COUNT"></span><span id="dns_error_invalid_nsec3_iteration_count"></span>**Errore DNS il \_ \_ \_ numero di \_ iterazioni NSEC3 non è valido \_**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-226"><span id="DNS_ERROR_INVALID_NSEC3_ITERATION_COUNT"></span><span id="dns_error_invalid_nsec3_iteration_count"></span>**DNS\_ERROR\_INVALID\_NSEC3\_ITERATION\_COUNT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-227">9124 (0x23A4)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-227">9124 (0x23A4)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-228">Il numero di iterazioni NSEC3 specificato è superiore a quello consentito dalla lunghezza minima della chiave usata nella zona.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-228">The specified NSEC3 iteration count is higher than allowed by the minimum key length used in the zone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-229"><span id="DNS_ERROR_DNSSEC_IS_DISABLED"></span><span id="dns_error_dnssec_is_disabled"></span>**\_errore DNS \_ DNSSEC \_ \_ disabilitato**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-229"><span id="DNS_ERROR_DNSSEC_IS_DISABLED"></span><span id="dns_error_dnssec_is_disabled"></span>**DNS\_ERROR\_DNSSEC\_IS\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-230">9125 (0x23A5)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-230">9125 (0x23A5)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-231">Non è stato possibile completare l'operazione perché il server DNS è stato configurato con le funzionalità DNSSEC disabilitate.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-231">This operation could not be completed because the DNS server has been configured with DNSSEC features disabled.</span></span> <span data-ttu-id="6b3a1-232">Abilitare DNSSEC sul server DNS.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-232">Enable DNSSEC on the DNS server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-233"><span id="DNS_ERROR_INVALID_XML"></span><span id="dns_error_invalid_xml"></span>**\_errore DNS \_ XML non valido \_**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-233"><span id="DNS_ERROR_INVALID_XML"></span><span id="dns_error_invalid_xml"></span>**DNS\_ERROR\_INVALID\_XML**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-234">9126 (0x23A6)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-234">9126 (0x23A6)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-235">Non è stato possibile completare l'operazione perché il flusso XML ricevuto è vuoto o sintatticamente non valido.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-235">This operation could not be completed because the XML stream received is empty or syntactically invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-236"><span id="DNS_ERROR_NO_VALID_TRUST_ANCHORS"></span><span id="dns_error_no_valid_trust_anchors"></span>**\_errore DNS \_ nessun \_ \_ trust \_ Anchor valido**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-236"><span id="DNS_ERROR_NO_VALID_TRUST_ANCHORS"></span><span id="dns_error_no_valid_trust_anchors"></span>**DNS\_ERROR\_NO\_VALID\_TRUST\_ANCHORS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-237">9127 (0x23A7)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-237">9127 (0x23A7)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-238">Questa operazione è stata completata, ma non sono stati aggiunti Trust Anchor perché tutti i trust anchor ricevuti non sono validi, non sono supportati, sono scaduti o non diventano validi in meno di 30 giorni.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-238">This operation completed, but no trust anchors were added because all of the trust anchors received were either invalid, unsupported, expired, or would not become valid in less than 30 days.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-239"><span id="DNS_ERROR_ROLLOVER_NOT_POKEABLE"></span><span id="dns_error_rollover_not_pokeable"></span>**\_rollover degli errori DNS \_ \_ non \_ pokeable**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-239"><span id="DNS_ERROR_ROLLOVER_NOT_POKEABLE"></span><span id="dns_error_rollover_not_pokeable"></span>**DNS\_ERROR\_ROLLOVER\_NOT\_POKEABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-240">9128 (0x23A8)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-240">9128 (0x23A8)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-241">La chiave di firma specificata non è in attesa dell'aggiornamento DS padre.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-241">The specified signing key is not waiting for parental DS update.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-242"><span id="DNS_ERROR_NSEC3_NAME_COLLISION"></span><span id="dns_error_nsec3_name_collision"></span>**\_ \_ \_ Conflitto nome NSEC3 errore \_ DNS**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-242"><span id="DNS_ERROR_NSEC3_NAME_COLLISION"></span><span id="dns_error_nsec3_name_collision"></span>**DNS\_ERROR\_NSEC3\_NAME\_COLLISION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-243">9129 (0x23A9)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-243">9129 (0x23A9)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-244">Collisione hash rilevata durante la firma NSEC3.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-244">Hash collision detected during NSEC3 signing.</span></span> <span data-ttu-id="6b3a1-245">Specificare un Salt fornito dall'utente diverso o usare un salt generato in modo casuale e tentare nuovamente di firmare la zona.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-245">Specify a different user-provided salt, or use a randomly generated salt, and attempt to sign the zone again.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-246"><span id="DNS_ERROR_NSEC_INCOMPATIBLE_WITH_NSEC3_RSA_SHA1"></span><span id="dns_error_nsec_incompatible_with_nsec3_rsa_sha1"></span>**\_Errore DNS \_ nsec \_ incompatibile \_ con \_ NSEC3 \_ RSA \_ SHA1**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-246"><span id="DNS_ERROR_NSEC_INCOMPATIBLE_WITH_NSEC3_RSA_SHA1"></span><span id="dns_error_nsec_incompatible_with_nsec3_rsa_sha1"></span>**DNS\_ERROR\_NSEC\_INCOMPATIBLE\_WITH\_NSEC3\_RSA\_SHA1**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-247">9130 (0x23AA)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-247">9130 (0x23AA)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-248">NSEC non è compatibile con l'algoritmo NSEC3-RSA-SHA-1.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-248">NSEC is not compatible with the NSEC3-RSA-SHA-1 algorithm.</span></span> <span data-ttu-id="6b3a1-249">Scegliere un algoritmo diverso o usare NSEC3.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-249">Choose a different algorithm or use NSEC3.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-250"><span id="DNS_INFO_NO_RECORDS"></span><span id="dns_info_no_records"></span>**\_informazioni DNS \_ nessun \_ record**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-250"><span id="DNS_INFO_NO_RECORDS"></span><span id="dns_info_no_records"></span>**DNS\_INFO\_NO\_RECORDS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-251">9501 (0x251D)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-251">9501 (0x251D)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-252">Nessun record trovato per la query DNS specificata.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-252">No records found for given DNS query.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-253"><span id="DNS_ERROR_BAD_PACKET"></span><span id="dns_error_bad_packet"></span>**\_errore DNS \_ \_ pacchetto errato**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-253"><span id="DNS_ERROR_BAD_PACKET"></span><span id="dns_error_bad_packet"></span>**DNS\_ERROR\_BAD\_PACKET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-254">9502 (0x251E)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-254">9502 (0x251E)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-255">Pacchetto DNS non valido.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-255">Bad DNS packet.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-256"><span id="DNS_ERROR_NO_PACKET"></span><span id="dns_error_no_packet"></span>**\_errore DNS \_ senza \_ pacchetti**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-256"><span id="DNS_ERROR_NO_PACKET"></span><span id="dns_error_no_packet"></span>**DNS\_ERROR\_NO\_PACKET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-257">9503 (0x251F)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-257">9503 (0x251F)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-258">Nessun pacchetto DNS.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-258">No DNS packet.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-259"><span id="DNS_ERROR_RCODE"></span><span id="dns_error_rcode"></span>**\_errore DNS \_ RCODE**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-259"><span id="DNS_ERROR_RCODE"></span><span id="dns_error_rcode"></span>**DNS\_ERROR\_RCODE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-260">9504 (0x2520)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-260">9504 (0x2520)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-261">Errore DNS, controllare RCODE.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-261">DNS error, check rcode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-262"><span id="DNS_ERROR_UNSECURE_PACKET"></span><span id="dns_error_unsecure_packet"></span>**errore DNS non \_ \_ protetto \_ pacchetto**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-262"><span id="DNS_ERROR_UNSECURE_PACKET"></span><span id="dns_error_unsecure_packet"></span>**DNS\_ERROR\_UNSECURE\_PACKET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-263">9505 (0x2521)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-263">9505 (0x2521)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-264">Pacchetto DNS non protetto.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-264">Unsecured DNS packet.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-265"><span id="DNS_REQUEST_PENDING"></span><span id="dns_request_pending"></span>**\_richiesta DNS \_ in sospeso**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-265"><span id="DNS_REQUEST_PENDING"></span><span id="dns_request_pending"></span>**DNS\_REQUEST\_PENDING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-266">9506 (0x2522)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-266">9506 (0x2522)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-267">La richiesta di query DNS è in sospeso.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-267">DNS query request is pending.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-268"><span id="DNS_ERROR_INVALID_TYPE"></span><span id="dns_error_invalid_type"></span>**\_tipo di errore DNS \_ non valido \_**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-268"><span id="DNS_ERROR_INVALID_TYPE"></span><span id="dns_error_invalid_type"></span>**DNS\_ERROR\_INVALID\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-269">9551 (0x254F)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-269">9551 (0x254F)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-270">Tipo DNS non valido.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-270">Invalid DNS type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-271"><span id="DNS_ERROR_INVALID_IP_ADDRESS"></span><span id="dns_error_invalid_ip_address"></span>**\_errore DNS \_ \_ indirizzo IP non valido \_**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-271"><span id="DNS_ERROR_INVALID_IP_ADDRESS"></span><span id="dns_error_invalid_ip_address"></span>**DNS\_ERROR\_INVALID\_IP\_ADDRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-272">9552 (0x2550)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-272">9552 (0x2550)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-273">Indirizzo IP non valido.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-273">Invalid IP address.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-274"><span id="DNS_ERROR_INVALID_PROPERTY"></span><span id="dns_error_invalid_property"></span>**\_Proprietà errore DNS \_ non valida \_**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-274"><span id="DNS_ERROR_INVALID_PROPERTY"></span><span id="dns_error_invalid_property"></span>**DNS\_ERROR\_INVALID\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-275">9553 (0x2551)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-275">9553 (0x2551)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-276">Proprietà non valida.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-276">Invalid property.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-277"><span id="DNS_ERROR_TRY_AGAIN_LATER"></span><span id="dns_error_try_again_later"></span>**\_errore DNS \_ riprovare \_ \_ più tardi**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-277"><span id="DNS_ERROR_TRY_AGAIN_LATER"></span><span id="dns_error_try_again_later"></span>**DNS\_ERROR\_TRY\_AGAIN\_LATER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-278">9554 (0x2552)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-278">9554 (0x2552)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-279">Ripetere l'operazione DNS in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-279">Try DNS operation again later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-280"><span id="DNS_ERROR_NOT_UNIQUE"></span><span id="dns_error_not_unique"></span>**\_errore DNS \_ non \_ univoco**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-280"><span id="DNS_ERROR_NOT_UNIQUE"></span><span id="dns_error_not_unique"></span>**DNS\_ERROR\_NOT\_UNIQUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-281">9555 (0x2553)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-281">9555 (0x2553)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-282">Il record per il nome e il tipo specificati non è univoco.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-282">Record for given name and type is not unique.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-283"><span id="DNS_ERROR_NON_RFC_NAME"></span><span id="dns_error_non_rfc_name"></span>**\_ \_ \_ nome non RFC \_ dell'errore DNS**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-283"><span id="DNS_ERROR_NON_RFC_NAME"></span><span id="dns_error_non_rfc_name"></span>**DNS\_ERROR\_NON\_RFC\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-284">9556 (0x2554)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-284">9556 (0x2554)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-285">Il nome DNS non è conforme alle specifiche RFC.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-285">DNS name does not comply with RFC specifications.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-286"><span id="DNS_STATUS_FQDN"></span><span id="dns_status_fqdn"></span>**\_FQDN stato \_ DNS**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-286"><span id="DNS_STATUS_FQDN"></span><span id="dns_status_fqdn"></span>**DNS\_STATUS\_FQDN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-287">9557 (0x2555)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-287">9557 (0x2555)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-288">Il nome DNS è un nome DNS completo.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-288">DNS name is a fully-qualified DNS name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-289"><span id="DNS_STATUS_DOTTED_NAME"></span><span id="dns_status_dotted_name"></span>**\_ \_ nome punteggiato stato \_ DNS**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-289"><span id="DNS_STATUS_DOTTED_NAME"></span><span id="dns_status_dotted_name"></span>**DNS\_STATUS\_DOTTED\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-290">9558 (0x2556)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-290">9558 (0x2556)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-291">Il nome DNS è punteggiato (più etichette).</span><span class="sxs-lookup"><span data-stu-id="6b3a1-291">DNS name is dotted (multi-label).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-292"><span id="DNS_STATUS_SINGLE_PART_NAME"></span><span id="dns_status_single_part_name"></span>**\_ \_ \_ nome singola parte \_ stato DNS**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-292"><span id="DNS_STATUS_SINGLE_PART_NAME"></span><span id="dns_status_single_part_name"></span>**DNS\_STATUS\_SINGLE\_PART\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-293">9559 (0x2557)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-293">9559 (0x2557)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-294">Il nome DNS è un nome in una sola parte.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-294">DNS name is a single-part name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-295"><span id="DNS_ERROR_INVALID_NAME_CHAR"></span><span id="dns_error_invalid_name_char"></span>**\_errore DNS \_ non valido \_ nome \_ Char**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-295"><span id="DNS_ERROR_INVALID_NAME_CHAR"></span><span id="dns_error_invalid_name_char"></span>**DNS\_ERROR\_INVALID\_NAME\_CHAR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-296">9560 (0x2558)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-296">9560 (0x2558)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-297">Il nome DNS contiene un carattere non valido.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-297">DNS name contains an invalid character.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-298"><span id="DNS_ERROR_NUMERIC_NAME"></span><span id="dns_error_numeric_name"></span>**\_ \_ nome numerico errore \_ DNS**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-298"><span id="DNS_ERROR_NUMERIC_NAME"></span><span id="dns_error_numeric_name"></span>**DNS\_ERROR\_NUMERIC\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-299">9561 (0x2559)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-299">9561 (0x2559)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-300">Il nome DNS è interamente numerico.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-300">DNS name is entirely numeric.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-301"><span id="DNS_ERROR_NOT_ALLOWED_ON_ROOT_SERVER"></span><span id="dns_error_not_allowed_on_root_server"></span>**\_errore DNS \_ non \_ consentito \_ nel \_ \_ server radice**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-301"><span id="DNS_ERROR_NOT_ALLOWED_ON_ROOT_SERVER"></span><span id="dns_error_not_allowed_on_root_server"></span>**DNS\_ERROR\_NOT\_ALLOWED\_ON\_ROOT\_SERVER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-302">9562 (0x255A)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-302">9562 (0x255A)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-303">L'operazione richiesta non è consentita in un server radice DNS.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-303">The operation requested is not permitted on a DNS root server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-304"><span id="DNS_ERROR_NOT_ALLOWED_UNDER_DELEGATION"></span><span id="dns_error_not_allowed_under_delegation"></span>**\_errore DNS \_ non \_ consentito \_ nella \_ delega**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-304"><span id="DNS_ERROR_NOT_ALLOWED_UNDER_DELEGATION"></span><span id="dns_error_not_allowed_under_delegation"></span>**DNS\_ERROR\_NOT\_ALLOWED\_UNDER\_DELEGATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-305">9563 (0x255B)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-305">9563 (0x255B)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-306">Non è stato possibile creare il record perché questa parte dello spazio dei nomi DNS è stata delegata a un altro server.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-306">The record could not be created because this part of the DNS namespace has been delegated to another server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-307"><span id="DNS_ERROR_CANNOT_FIND_ROOT_HINTS"></span><span id="dns_error_cannot_find_root_hints"></span>**\_errore DNS \_ non è in grado di \_ trovare i \_ \_ parametri radice**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-307"><span id="DNS_ERROR_CANNOT_FIND_ROOT_HINTS"></span><span id="dns_error_cannot_find_root_hints"></span>**DNS\_ERROR\_CANNOT\_FIND\_ROOT\_HINTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-308">9564 (0x255C)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-308">9564 (0x255C)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-309">Il server DNS non è riuscito a trovare un set di parametri radice.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-309">The DNS server could not find a set of root hints.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-310"><span id="DNS_ERROR_INCONSISTENT_ROOT_HINTS"></span><span id="dns_error_inconsistent_root_hints"></span>**\_ \_ parametri radice incoerenti degli errori \_ DNS \_**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-310"><span id="DNS_ERROR_INCONSISTENT_ROOT_HINTS"></span><span id="dns_error_inconsistent_root_hints"></span>**DNS\_ERROR\_INCONSISTENT\_ROOT\_HINTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-311">9565 (0x255D)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-311">9565 (0x255D)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-312">Il server DNS ha rilevato parametri radice ma non è coerente in tutte le schede.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-312">The DNS server found root hints but they were not consistent across all adapters.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-313"><span id="DNS_ERROR_DWORD_VALUE_TOO_SMALL"></span><span id="dns_error_dword_value_too_small"></span>**\_errore DNS \_ \_ valore DWORD \_ troppo \_ piccolo**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-313"><span id="DNS_ERROR_DWORD_VALUE_TOO_SMALL"></span><span id="dns_error_dword_value_too_small"></span>**DNS\_ERROR\_DWORD\_VALUE\_TOO\_SMALL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-314">9566 (0x255E)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-314">9566 (0x255E)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-315">Il valore specificato è troppo piccolo per questo parametro.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-315">The specified value is too small for this parameter.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-316"><span id="DNS_ERROR_DWORD_VALUE_TOO_LARGE"></span><span id="dns_error_dword_value_too_large"></span>**\_errore DNS \_ \_ valore DWORD \_ troppo \_ grande**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-316"><span id="DNS_ERROR_DWORD_VALUE_TOO_LARGE"></span><span id="dns_error_dword_value_too_large"></span>**DNS\_ERROR\_DWORD\_VALUE\_TOO\_LARGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-317">9567 (0x255F)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-317">9567 (0x255F)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-318">Il valore specificato è troppo grande per questo parametro.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-318">The specified value is too large for this parameter.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-319"><span id="DNS_ERROR_BACKGROUND_LOADING"></span><span id="dns_error_background_loading"></span>**\_caricamento in \_ background degli errori DNS \_**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-319"><span id="DNS_ERROR_BACKGROUND_LOADING"></span><span id="dns_error_background_loading"></span>**DNS\_ERROR\_BACKGROUND\_LOADING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-320">9568 (0x2560)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-320">9568 (0x2560)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-321">Questa operazione non è consentita mentre il server DNS carica le zone in background.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-321">This operation is not allowed while the DNS server is loading zones in the background.</span></span> <span data-ttu-id="6b3a1-322">Riprova più tardi.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-322">Please try again later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-323"><span id="DNS_ERROR_NOT_ALLOWED_ON_RODC"></span><span id="dns_error_not_allowed_on_rodc"></span>**\_errore DNS \_ non \_ consentito \_ nel controller di dominio di \_ sola lettura**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-323"><span id="DNS_ERROR_NOT_ALLOWED_ON_RODC"></span><span id="dns_error_not_allowed_on_rodc"></span>**DNS\_ERROR\_NOT\_ALLOWED\_ON\_RODC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-324">9569 (0x2561)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-324">9569 (0x2561)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-325">L'operazione richiesta non è consentita su un server DNS in esecuzione in un controller di dominio di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-325">The operation requested is not permitted on against a DNS server running on a read-only DC.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-326"><span id="DNS_ERROR_NOT_ALLOWED_UNDER_DNAME"></span><span id="dns_error_not_allowed_under_dname"></span>**\_errore DNS \_ non \_ consentito \_ in \_ DNAME**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-326"><span id="DNS_ERROR_NOT_ALLOWED_UNDER_DNAME"></span><span id="dns_error_not_allowed_under_dname"></span>**DNS\_ERROR\_NOT\_ALLOWED\_UNDER\_DNAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-327">9570 (0x2562)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-327">9570 (0x2562)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-328">Nessun dato può esistere sotto un record DNAME.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-328">No data is allowed to exist underneath a DNAME record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-329"><span id="DNS_ERROR_DELEGATION_REQUIRED"></span><span id="dns_error_delegation_required"></span>**\_delega degli errori DNS \_ \_ obbligatoria**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-329"><span id="DNS_ERROR_DELEGATION_REQUIRED"></span><span id="dns_error_delegation_required"></span>**DNS\_ERROR\_DELEGATION\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-330">9571 (0x2563)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-330">9571 (0x2563)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-331">Questa operazione richiede la delega delle credenziali.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-331">This operation requires credentials delegation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-332"><span id="DNS_ERROR_INVALID_POLICY_TABLE"></span><span id="dns_error_invalid_policy_table"></span>**\_tabella dei \_ criteri non valida per errore \_ DNS \_**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-332"><span id="DNS_ERROR_INVALID_POLICY_TABLE"></span><span id="dns_error_invalid_policy_table"></span>**DNS\_ERROR\_INVALID\_POLICY\_TABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-333">9572 (0x2564)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-333">9572 (0x2564)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-334">La tabella dei criteri di risoluzione dei nomi è danneggiata.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-334">Name resolution policy table has been corrupted.</span></span> <span data-ttu-id="6b3a1-335">La risoluzione DNS non riuscirà fino a quando non sarà corretta.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-335">DNS resolution will fail until it is fixed.</span></span> <span data-ttu-id="6b3a1-336">Contattare l'amministratore di rete.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-336">Contact your network administrator.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-337"><span id="DNS_ERROR_ZONE_DOES_NOT_EXIST"></span><span id="dns_error_zone_does_not_exist"></span>**\_la zona di errore DNS non \_ \_ \_ \_ esiste**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-337"><span id="DNS_ERROR_ZONE_DOES_NOT_EXIST"></span><span id="dns_error_zone_does_not_exist"></span>**DNS\_ERROR\_ZONE\_DOES\_NOT\_EXIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-338">9601 (0x2581)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-338">9601 (0x2581)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-339">La zona DNS non esiste.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-339">DNS zone does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-340"><span id="DNS_ERROR_NO_ZONE_INFO"></span><span id="dns_error_no_zone_info"></span>**\_errore DNS \_ senza \_ informazioni sulla zona \_**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-340"><span id="DNS_ERROR_NO_ZONE_INFO"></span><span id="dns_error_no_zone_info"></span>**DNS\_ERROR\_NO\_ZONE\_INFO**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-341">9602 (0x2582)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-341">9602 (0x2582)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-342">Informazioni sulla zona DNS non disponibili.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-342">DNS zone information not available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-343"><span id="DNS_ERROR_INVALID_ZONE_OPERATION"></span><span id="dns_error_invalid_zone_operation"></span>**\_operazione di \_ zona non valida nell'errore \_ DNS \_**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-343"><span id="DNS_ERROR_INVALID_ZONE_OPERATION"></span><span id="dns_error_invalid_zone_operation"></span>**DNS\_ERROR\_INVALID\_ZONE\_OPERATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-344">9603 (0x2583)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-344">9603 (0x2583)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-345">Operazione non valida per la zona DNS.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-345">Invalid operation for DNS zone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-346"><span id="DNS_ERROR_ZONE_CONFIGURATION_ERROR"></span><span id="dns_error_zone_configuration_error"></span>**\_errore di \_ configurazione della zona di errore DNS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-346"><span id="DNS_ERROR_ZONE_CONFIGURATION_ERROR"></span><span id="dns_error_zone_configuration_error"></span>**DNS\_ERROR\_ZONE\_CONFIGURATION\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-347">9604 (0x2584)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-347">9604 (0x2584)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-348">Configurazione della zona DNS non valida.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-348">Invalid DNS zone configuration.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-349"><span id="DNS_ERROR_ZONE_HAS_NO_SOA_RECORD"></span><span id="dns_error_zone_has_no_soa_record"></span>**la \_ zona di errore DNS \_ \_ \_ non ha \_ \_ record SOA**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-349"><span id="DNS_ERROR_ZONE_HAS_NO_SOA_RECORD"></span><span id="dns_error_zone_has_no_soa_record"></span>**DNS\_ERROR\_ZONE\_HAS\_NO\_SOA\_RECORD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-350">9605 (0x2585)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-350">9605 (0x2585)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-351">La zona DNS non dispone di un record di inizio di autorità (SOA).</span><span class="sxs-lookup"><span data-stu-id="6b3a1-351">DNS zone has no start of authority (SOA) record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-352"><span id="DNS_ERROR_ZONE_HAS_NO_NS_RECORDS"></span><span id="dns_error_zone_has_no_ns_records"></span>**la \_ zona di errore DNS \_ \_ \_ non contiene \_ \_ record NS**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-352"><span id="DNS_ERROR_ZONE_HAS_NO_NS_RECORDS"></span><span id="dns_error_zone_has_no_ns_records"></span>**DNS\_ERROR\_ZONE\_HAS\_NO\_NS\_RECORDS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-353">9606 (0x2586)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-353">9606 (0x2586)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-354">Per la zona DNS non è presente alcun record server nome (NS).</span><span class="sxs-lookup"><span data-stu-id="6b3a1-354">DNS zone has no Name Server (NS) record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-355"><span id="DNS_ERROR_ZONE_LOCKED"></span><span id="dns_error_zone_locked"></span>**\_zona di errore DNS \_ \_ bloccata**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-355"><span id="DNS_ERROR_ZONE_LOCKED"></span><span id="dns_error_zone_locked"></span>**DNS\_ERROR\_ZONE\_LOCKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-356">9607 (0x2587)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-356">9607 (0x2587)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-357">La zona DNS è bloccata.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-357">DNS zone is locked.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-358"><span id="DNS_ERROR_ZONE_CREATION_FAILED"></span><span id="dns_error_zone_creation_failed"></span>**\_creazione della zona di errore DNS \_ \_ \_ non riuscita**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-358"><span id="DNS_ERROR_ZONE_CREATION_FAILED"></span><span id="dns_error_zone_creation_failed"></span>**DNS\_ERROR\_ZONE\_CREATION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-359">9608 (0x2588)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-359">9608 (0x2588)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-360">Creazione della zona DNS non riuscita.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-360">DNS zone creation failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-361"><span id="DNS_ERROR_ZONE_ALREADY_EXISTS"></span><span id="dns_error_zone_already_exists"></span>**la \_ zona di errore DNS \_ \_ \_ esiste già**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-361"><span id="DNS_ERROR_ZONE_ALREADY_EXISTS"></span><span id="dns_error_zone_already_exists"></span>**DNS\_ERROR\_ZONE\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-362">9609 (0x2589)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-362">9609 (0x2589)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-363">Zona DNS già esistente.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-363">DNS zone already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-364"><span id="DNS_ERROR_AUTOZONE_ALREADY_EXISTS"></span><span id="dns_error_autozone_already_exists"></span>**la \_ zona di errore DNS è \_ \_ già \_ esistente**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-364"><span id="DNS_ERROR_AUTOZONE_ALREADY_EXISTS"></span><span id="dns_error_autozone_already_exists"></span>**DNS\_ERROR\_AUTOZONE\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-365">9610 (0x258A)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-365">9610 (0x258A)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-366">La zona DNS automatica esiste già.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-366">DNS automatic zone already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-367"><span id="DNS_ERROR_INVALID_ZONE_TYPE"></span><span id="dns_error_invalid_zone_type"></span>**\_tipo di \_ zona non valido per l'errore DNS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-367"><span id="DNS_ERROR_INVALID_ZONE_TYPE"></span><span id="dns_error_invalid_zone_type"></span>**DNS\_ERROR\_INVALID\_ZONE\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-368">9611 (0x258B)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-368">9611 (0x258B)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-369">Tipo di zona DNS non valido.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-369">Invalid DNS zone type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-370"><span id="DNS_ERROR_SECONDARY_REQUIRES_MASTER_IP"></span><span id="dns_error_secondary_requires_master_ip"></span>**l' \_ errore DNS \_ secondario \_ richiede l' \_ \_ indirizzo IP master**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-370"><span id="DNS_ERROR_SECONDARY_REQUIRES_MASTER_IP"></span><span id="dns_error_secondary_requires_master_ip"></span>**DNS\_ERROR\_SECONDARY\_REQUIRES\_MASTER\_IP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-371">9612 (0x258C)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-371">9612 (0x258C)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-372">La zona DNS secondaria richiede l'indirizzo IP master.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-372">Secondary DNS zone requires master IP address.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-373"><span id="DNS_ERROR_ZONE_NOT_SECONDARY"></span><span id="dns_error_zone_not_secondary"></span>**\_zona di errore DNS \_ \_ non \_ secondaria**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-373"><span id="DNS_ERROR_ZONE_NOT_SECONDARY"></span><span id="dns_error_zone_not_secondary"></span>**DNS\_ERROR\_ZONE\_NOT\_SECONDARY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-374">9613 (0x258D)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-374">9613 (0x258D)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-375">Zona DNS non secondaria.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-375">DNS zone not secondary.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-376"><span id="DNS_ERROR_NEED_SECONDARY_ADDRESSES"></span><span id="dns_error_need_secondary_addresses"></span>**\_errore DNS \_ necessario \_ per \_ gli indirizzi secondari**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-376"><span id="DNS_ERROR_NEED_SECONDARY_ADDRESSES"></span><span id="dns_error_need_secondary_addresses"></span>**DNS\_ERROR\_NEED\_SECONDARY\_ADDRESSES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-377">9614 (0x258E)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-377">9614 (0x258E)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-378">Sono necessari indirizzi IP secondari.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-378">Need secondary IP address.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-379"><span id="DNS_ERROR_WINS_INIT_FAILED"></span><span id="dns_error_wins_init_failed"></span>**\_errore DNS \_ WINS \_ inizializzazione \_ non riuscito**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-379"><span id="DNS_ERROR_WINS_INIT_FAILED"></span><span id="dns_error_wins_init_failed"></span>**DNS\_ERROR\_WINS\_INIT\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-380">9615 (0x258F)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-380">9615 (0x258F)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-381">Inizializzazione WINS non riuscita.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-381">WINS initialization failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-382"><span id="DNS_ERROR_NEED_WINS_SERVERS"></span><span id="dns_error_need_wins_servers"></span>**errore DNS necessario per i \_ \_ \_ \_ server WINS**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-382"><span id="DNS_ERROR_NEED_WINS_SERVERS"></span><span id="dns_error_need_wins_servers"></span>**DNS\_ERROR\_NEED\_WINS\_SERVERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-383">9616 (0x2590)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-383">9616 (0x2590)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-384">Sono necessari server WINS.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-384">Need WINS servers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-385"><span id="DNS_ERROR_NBSTAT_INIT_FAILED"></span><span id="dns_error_nbstat_init_failed"></span>**\_errore DNS \_ NBSTAT \_ init \_ non riuscita**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-385"><span id="DNS_ERROR_NBSTAT_INIT_FAILED"></span><span id="dns_error_nbstat_init_failed"></span>**DNS\_ERROR\_NBSTAT\_INIT\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-386">9617 (0x2591)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-386">9617 (0x2591)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-387">Chiamata di inizializzazione NBTSTAT non riuscita.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-387">NBTSTAT initialization call failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-388"><span id="DNS_ERROR_SOA_DELETE_INVALID"></span><span id="dns_error_soa_delete_invalid"></span>**errore DNS- \_ \_ \_ eliminazione SOA \_ non valida**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-388"><span id="DNS_ERROR_SOA_DELETE_INVALID"></span><span id="dns_error_soa_delete_invalid"></span>**DNS\_ERROR\_SOA\_DELETE\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-389">9618 (0x2592)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-389">9618 (0x2592)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-390">Eliminazione dell'inizio dell'autorità (SOA) non valida.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-390">Invalid delete of start of authority (SOA).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-391"><span id="DNS_ERROR_FORWARDER_ALREADY_EXISTS"></span><span id="dns_error_forwarder_already_exists"></span>**il \_ server d'invio degli errori DNS \_ \_ \_ esiste già**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-391"><span id="DNS_ERROR_FORWARDER_ALREADY_EXISTS"></span><span id="dns_error_forwarder_already_exists"></span>**DNS\_ERROR\_FORWARDER\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-392">9619 (0x2593)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-392">9619 (0x2593)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-393">Esiste già un'area di trasmissione condizionale per quel nome.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-393">A conditional forwarding zone already exists for that name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-394"><span id="DNS_ERROR_ZONE_REQUIRES_MASTER_IP"></span><span id="dns_error_zone_requires_master_ip"></span>**la \_ zona di errore DNS \_ richiede l' \_ \_ \_ indirizzo IP master**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-394"><span id="DNS_ERROR_ZONE_REQUIRES_MASTER_IP"></span><span id="dns_error_zone_requires_master_ip"></span>**DNS\_ERROR\_ZONE\_REQUIRES\_MASTER\_IP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-395">9620 (0x2594)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-395">9620 (0x2594)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-396">Questa zona deve essere configurata con uno o più indirizzi IP del server DNS master.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-396">This zone must be configured with one or more master DNS server IP addresses.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-397"><span id="DNS_ERROR_ZONE_IS_SHUTDOWN"></span><span id="dns_error_zone_is_shutdown"></span>**\_la zona di errore DNS \_ è stata \_ \_ arrestata**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-397"><span id="DNS_ERROR_ZONE_IS_SHUTDOWN"></span><span id="dns_error_zone_is_shutdown"></span>**DNS\_ERROR\_ZONE\_IS\_SHUTDOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-398">9621 (0x2595)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-398">9621 (0x2595)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-399">Non è possibile eseguire l'operazione perché questa zona è stata arrestata.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-399">The operation cannot be performed because this zone is shut down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-400"><span id="DNS_ERROR_ZONE_LOCKED_FOR_SIGNING"></span><span id="dns_error_zone_locked_for_signing"></span>**\_ \_ zona di errore DNS \_ bloccata \_ per la \_ firma**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-400"><span id="DNS_ERROR_ZONE_LOCKED_FOR_SIGNING"></span><span id="dns_error_zone_locked_for_signing"></span>**DNS\_ERROR\_ZONE\_LOCKED\_FOR\_SIGNING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-401">9622 (0x2596)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-401">9622 (0x2596)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-402">Impossibile eseguire l'operazione perché la zona è attualmente in fase di firma.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-402">This operation cannot be performed because the zone is currently being signed.</span></span> <span data-ttu-id="6b3a1-403">Riprova più tardi.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-403">Please try again later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-404"><span id="DNS_ERROR_PRIMARY_REQUIRES_DATAFILE"></span><span id="dns_error_primary_requires_datafile"></span>**l' \_ errore DNS \_ primario \_ richiede \_ un file di file**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-404"><span id="DNS_ERROR_PRIMARY_REQUIRES_DATAFILE"></span><span id="dns_error_primary_requires_datafile"></span>**DNS\_ERROR\_PRIMARY\_REQUIRES\_DATAFILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-405">9651 (0x25B3)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-405">9651 (0x25B3)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-406">La zona DNS primaria richiede DataFile.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-406">Primary DNS zone requires datafile.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-407"><span id="DNS_ERROR_INVALID_DATAFILE_NAME"></span><span id="dns_error_invalid_datafile_name"></span>**\_ \_ \_ nome DataFile non valido \_ per l'errore DNS**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-407"><span id="DNS_ERROR_INVALID_DATAFILE_NAME"></span><span id="dns_error_invalid_datafile_name"></span>**DNS\_ERROR\_INVALID\_DATAFILE\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-408">9652 (0x25B4)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-408">9652 (0x25B4)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-409">Nome di file di DataFile non valido per la zona DNS.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-409">Invalid datafile name for DNS zone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-410"><span id="DNS_ERROR_DATAFILE_OPEN_FAILURE"></span><span id="dns_error_datafile_open_failure"></span>**errore di apertura del file di \_ errore DNS \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-410"><span id="DNS_ERROR_DATAFILE_OPEN_FAILURE"></span><span id="dns_error_datafile_open_failure"></span>**DNS\_ERROR\_DATAFILE\_OPEN\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-411">9653 (0x25B5)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-411">9653 (0x25B5)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-412">Non è stato possibile aprire il file DataFile per la zona DNS.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-412">Failed to open datafile for DNS zone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-413"><span id="DNS_ERROR_FILE_WRITEBACK_FAILED"></span><span id="dns_error_file_writeback_failed"></span>**il \_ WRITEBACK del file degli errori DNS \_ \_ \_ non è riuscito**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-413"><span id="DNS_ERROR_FILE_WRITEBACK_FAILED"></span><span id="dns_error_file_writeback_failed"></span>**DNS\_ERROR\_FILE\_WRITEBACK\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-414">9654 (0x25B6)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-414">9654 (0x25B6)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-415">Non è stato possibile scrivere DataFile per la zona DNS.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-415">Failed to write datafile for DNS zone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-416"><span id="DNS_ERROR_DATAFILE_PARSING"></span><span id="dns_error_datafile_parsing"></span>**analisi dei file di \_ errore DNS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-416"><span id="DNS_ERROR_DATAFILE_PARSING"></span><span id="dns_error_datafile_parsing"></span>**DNS\_ERROR\_DATAFILE\_PARSING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-417">9655 (0x25B7)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-417">9655 (0x25B7)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-418">Errore durante la lettura di DataFile per la zona DNS.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-418">Failure while reading datafile for DNS zone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-419"><span id="DNS_ERROR_RECORD_DOES_NOT_EXIST"></span><span id="dns_error_record_does_not_exist"></span>**\_il record di errore DNS non \_ \_ \_ \_ esiste**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-419"><span id="DNS_ERROR_RECORD_DOES_NOT_EXIST"></span><span id="dns_error_record_does_not_exist"></span>**DNS\_ERROR\_RECORD\_DOES\_NOT\_EXIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-420">9701 (0x25E5)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-420">9701 (0x25E5)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-421">Il record DNS non esiste.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-421">DNS record does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-422"><span id="DNS_ERROR_RECORD_FORMAT"></span><span id="dns_error_record_format"></span>**\_ \_ formato record degli errori DNS \_**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-422"><span id="DNS_ERROR_RECORD_FORMAT"></span><span id="dns_error_record_format"></span>**DNS\_ERROR\_RECORD\_FORMAT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-423">9702 (0x25E6)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-423">9702 (0x25E6)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-424">Errore di formato del record DNS.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-424">DNS record format error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-425"><span id="DNS_ERROR_NODE_CREATION_FAILED"></span><span id="dns_error_node_creation_failed"></span>**\_ \_ creazione nodo errore \_ DNS \_ non riuscita**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-425"><span id="DNS_ERROR_NODE_CREATION_FAILED"></span><span id="dns_error_node_creation_failed"></span>**DNS\_ERROR\_NODE\_CREATION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-426">9703 (0x25E7)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-426">9703 (0x25E7)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-427">Errore di creazione del nodo in DNS.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-427">Node creation failure in DNS.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-428"><span id="DNS_ERROR_UNKNOWN_RECORD_TYPE"></span><span id="dns_error_unknown_record_type"></span>**\_tipo di \_ \_ record sconosciuto di errore \_ DNS**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-428"><span id="DNS_ERROR_UNKNOWN_RECORD_TYPE"></span><span id="dns_error_unknown_record_type"></span>**DNS\_ERROR\_UNKNOWN\_RECORD\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-429">9704 (0x25E8)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-429">9704 (0x25E8)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-430">Tipo di record DNS sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-430">Unknown DNS record type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-431"><span id="DNS_ERROR_RECORD_TIMED_OUT"></span><span id="dns_error_record_timed_out"></span>**\_timeout del \_ record di errore \_ DNS \_**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-431"><span id="DNS_ERROR_RECORD_TIMED_OUT"></span><span id="dns_error_record_timed_out"></span>**DNS\_ERROR\_RECORD\_TIMED\_OUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-432">9705 (0x25E9)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-432">9705 (0x25E9)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-433">Timeout del record DNS.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-433">DNS record timed out.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-434"><span id="DNS_ERROR_NAME_NOT_IN_ZONE"></span><span id="dns_error_name_not_in_zone"></span>**\_nome errore \_ DNS \_ non \_ nella \_ zona**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-434"><span id="DNS_ERROR_NAME_NOT_IN_ZONE"></span><span id="dns_error_name_not_in_zone"></span>**DNS\_ERROR\_NAME\_NOT\_IN\_ZONE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-435">9706 (0x25EA)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-435">9706 (0x25EA)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-436">Nome non nella zona DNS.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-436">Name not in DNS zone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-437"><span id="DNS_ERROR_CNAME_LOOP"></span><span id="dns_error_cname_loop"></span>**\_errore DNS \_ \_ ciclo CNAME**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-437"><span id="DNS_ERROR_CNAME_LOOP"></span><span id="dns_error_cname_loop"></span>**DNS\_ERROR\_CNAME\_LOOP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-438">9707 (0x25EB)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-438">9707 (0x25EB)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-439">Rilevato ciclo CNAME.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-439">CNAME loop detected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-440"><span id="DNS_ERROR_NODE_IS_CNAME"></span><span id="dns_error_node_is_cname"></span>**il \_ nodo errore DNS \_ \_ è \_ CNAME**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-440"><span id="DNS_ERROR_NODE_IS_CNAME"></span><span id="dns_error_node_is_cname"></span>**DNS\_ERROR\_NODE\_IS\_CNAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-441">9708 (0x25EC)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-441">9708 (0x25EC)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-442">Node è un record DNS CNAME.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-442">Node is a CNAME DNS record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-443"><span id="DNS_ERROR_CNAME_COLLISION"></span><span id="dns_error_cname_collision"></span>**\_ \_ collisione CNAME errore DNS \_**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-443"><span id="DNS_ERROR_CNAME_COLLISION"></span><span id="dns_error_cname_collision"></span>**DNS\_ERROR\_CNAME\_COLLISION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-444">9709 (0x25ED)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-444">9709 (0x25ED)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-445">Un record CNAME esiste già per il nome specificato.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-445">A CNAME record already exists for given name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-446"><span id="DNS_ERROR_RECORD_ONLY_AT_ZONE_ROOT"></span><span id="dns_error_record_only_at_zone_root"></span>**\_record degli errori DNS \_ \_ solo \_ nella \_ radice della zona \_**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-446"><span id="DNS_ERROR_RECORD_ONLY_AT_ZONE_ROOT"></span><span id="dns_error_record_only_at_zone_root"></span>**DNS\_ERROR\_RECORD\_ONLY\_AT\_ZONE\_ROOT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-447">9710 (0x25EE)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-447">9710 (0x25EE)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-448">Registra solo nella radice della zona DNS.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-448">Record only at DNS zone root.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-449"><span id="DNS_ERROR_RECORD_ALREADY_EXISTS"></span><span id="dns_error_record_already_exists"></span>**il \_ record di errore DNS \_ \_ \_ esiste già**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-449"><span id="DNS_ERROR_RECORD_ALREADY_EXISTS"></span><span id="dns_error_record_already_exists"></span>**DNS\_ERROR\_RECORD\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-450">9711 (0x25EF)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-450">9711 (0x25EF)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-451">Il record DNS esiste già.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-451">DNS record already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-452"><span id="DNS_ERROR_SECONDARY_DATA"></span><span id="dns_error_secondary_data"></span>**\_ \_ dati secondari degli errori DNS \_**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-452"><span id="DNS_ERROR_SECONDARY_DATA"></span><span id="dns_error_secondary_data"></span>**DNS\_ERROR\_SECONDARY\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-453">9712 (0x25F0)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-453">9712 (0x25F0)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-454">Errore dati zona DNS secondaria.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-454">Secondary DNS zone data error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-455"><span id="DNS_ERROR_NO_CREATE_CACHE_DATA"></span><span id="dns_error_no_create_cache_data"></span>**\_errore DNS \_ senza \_ creare \_ dati della cache \_**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-455"><span id="DNS_ERROR_NO_CREATE_CACHE_DATA"></span><span id="dns_error_no_create_cache_data"></span>**DNS\_ERROR\_NO\_CREATE\_CACHE\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-456">9713 (0x25F1)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-456">9713 (0x25F1)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-457">Non è stato possibile creare i dati della cache DNS.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-457">Could not create DNS cache data.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-458"><span id="DNS_ERROR_NAME_DOES_NOT_EXIST"></span><span id="dns_error_name_does_not_exist"></span>**\_il nome dell'errore DNS non \_ \_ \_ \_ esiste**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-458"><span id="DNS_ERROR_NAME_DOES_NOT_EXIST"></span><span id="dns_error_name_does_not_exist"></span>**DNS\_ERROR\_NAME\_DOES\_NOT\_EXIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-459">9714 (0x25F2)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-459">9714 (0x25F2)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-460">Nome DNS inesistente.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-460">DNS name does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-461"><span id="DNS_WARNING_PTR_CREATE_FAILED"></span><span id="dns_warning_ptr_create_failed"></span>**\_errore di \_ creazione PTR avviso DNS \_ \_ non riuscito**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-461"><span id="DNS_WARNING_PTR_CREATE_FAILED"></span><span id="dns_warning_ptr_create_failed"></span>**DNS\_WARNING\_PTR\_CREATE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-462">9715 (0x25F3)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-462">9715 (0x25F3)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-463">Non è stato possibile creare il record puntatore (PTR).</span><span class="sxs-lookup"><span data-stu-id="6b3a1-463">Could not create pointer (PTR) record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-464"><span id="DNS_WARNING_DOMAIN_UNDELETED"></span><span id="dns_warning_domain_undeleted"></span>**dominio di avviso DNS non \_ \_ \_ eliminato**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-464"><span id="DNS_WARNING_DOMAIN_UNDELETED"></span><span id="dns_warning_domain_undeleted"></span>**DNS\_WARNING\_DOMAIN\_UNDELETED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-465">9716 (0x25F4)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-465">9716 (0x25F4)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-466">Il dominio DNS non è stato eliminato.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-466">DNS domain was undeleted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-467"><span id="DNS_ERROR_DS_UNAVAILABLE"></span><span id="dns_error_ds_unavailable"></span>**\_errore DNS \_ DS non \_ disponibile**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-467"><span id="DNS_ERROR_DS_UNAVAILABLE"></span><span id="dns_error_ds_unavailable"></span>**DNS\_ERROR\_DS\_UNAVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-468">9717 (0x25F5)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-468">9717 (0x25F5)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-469">Il servizio directory non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-469">The directory service is unavailable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-470"><span id="DNS_ERROR_DS_ZONE_ALREADY_EXISTS"></span><span id="dns_error_ds_zone_already_exists"></span>**la \_ zona DS per gli errori DNS \_ \_ \_ \_ esiste già**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-470"><span id="DNS_ERROR_DS_ZONE_ALREADY_EXISTS"></span><span id="dns_error_ds_zone_already_exists"></span>**DNS\_ERROR\_DS\_ZONE\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-471">9718 (0x25F6)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-471">9718 (0x25F6)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-472">La zona DNS esiste già nel servizio directory.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-472">DNS zone already exists in the directory service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-473"><span id="DNS_ERROR_NO_BOOTFILE_IF_DS_ZONE"></span><span id="dns_error_no_bootfile_if_ds_zone"></span>**\_errore DNS \_ senza \_ BOOTFILE \_ se \_ la \_ zona DS**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-473"><span id="DNS_ERROR_NO_BOOTFILE_IF_DS_ZONE"></span><span id="dns_error_no_bootfile_if_ds_zone"></span>**DNS\_ERROR\_NO\_BOOTFILE\_IF\_DS\_ZONE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-474">9719 (0x25F7)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-474">9719 (0x25F7)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-475">Il server DNS non sta creando o leggendo il file di avvio per la zona DNS integrata del servizio directory.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-475">DNS server not creating or reading the boot file for the directory service integrated DNS zone.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-476"><span id="DNS_ERROR_NODE_IS_DNAME"></span><span id="dns_error_node_is_dname"></span>**il \_ nodo di errore DNS \_ \_ è \_ DNAME**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-476"><span id="DNS_ERROR_NODE_IS_DNAME"></span><span id="dns_error_node_is_dname"></span>**DNS\_ERROR\_NODE\_IS\_DNAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-477">9720 (0x25F8)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-477">9720 (0x25F8)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-478">Il nodo è un record DNS DNAME.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-478">Node is a DNAME DNS record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-479"><span id="DNS_ERROR_DNAME_COLLISION"></span><span id="dns_error_dname_collision"></span>**\_ \_ conflitto DNAME errore \_ DNS**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-479"><span id="DNS_ERROR_DNAME_COLLISION"></span><span id="dns_error_dname_collision"></span>**DNS\_ERROR\_DNAME\_COLLISION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-480">9721 (0x25F9)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-480">9721 (0x25F9)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-481">Un record DNAME esiste già per il nome specificato.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-481">A DNAME record already exists for given name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-482"><span id="DNS_ERROR_ALIAS_LOOP"></span><span id="dns_error_alias_loop"></span>**\_ciclo di \_ alias degli errori DNS \_**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-482"><span id="DNS_ERROR_ALIAS_LOOP"></span><span id="dns_error_alias_loop"></span>**DNS\_ERROR\_ALIAS\_LOOP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-483">9722 (0x25FA)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-483">9722 (0x25FA)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-484">È stato rilevato un ciclo alias con record CNAME o DNAME.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-484">An alias loop has been detected with either CNAME or DNAME records.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-485"><span id="DNS_INFO_AXFR_COMPLETE"></span><span id="dns_info_axfr_complete"></span>**\_informazioni DNS \_ AXFR \_ completate**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-485"><span id="DNS_INFO_AXFR_COMPLETE"></span><span id="dns_info_axfr_complete"></span>**DNS\_INFO\_AXFR\_COMPLETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-486">9751 (0x2617)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-486">9751 (0x2617)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-487">AXFR DNS (trasferimento di zona) completato.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-487">DNS AXFR (zone transfer) complete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-488"><span id="DNS_ERROR_AXFR"></span><span id="dns_error_axfr"></span>**\_errore DNS \_ AXFR**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-488"><span id="DNS_ERROR_AXFR"></span><span id="dns_error_axfr"></span>**DNS\_ERROR\_AXFR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-489">9752 (0x2618)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-489">9752 (0x2618)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-490">Trasferimento di zona DNS non riuscito.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-490">DNS zone transfer failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-491"><span id="DNS_INFO_ADDED_LOCAL_WINS"></span><span id="dns_info_added_local_wins"></span>**le \_ informazioni DNS hanno \_ aggiunto \_ \_ WINS locale**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-491"><span id="DNS_INFO_ADDED_LOCAL_WINS"></span><span id="dns_info_added_local_wins"></span>**DNS\_INFO\_ADDED\_LOCAL\_WINS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-492">9753 (0x2619)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-492">9753 (0x2619)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-493">Aggiunto server WINS locale.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-493">Added local WINS server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-494"><span id="DNS_STATUS_CONTINUE_NEEDED"></span><span id="dns_status_continue_needed"></span>**\_stato DNS \_ continua \_ necessario**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-494"><span id="DNS_STATUS_CONTINUE_NEEDED"></span><span id="dns_status_continue_needed"></span>**DNS\_STATUS\_CONTINUE\_NEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-495">9801 (0x2649)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-495">9801 (0x2649)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-496">Per la chiamata di aggiornamento sicuro è necessario continuare la richiesta di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-496">Secure update call needs to continue update request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-497"><span id="DNS_ERROR_NO_TCPIP"></span><span id="dns_error_no_tcpip"></span>**\_errore DNS \_ senza \_ Tcpip**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-497"><span id="DNS_ERROR_NO_TCPIP"></span><span id="dns_error_no_tcpip"></span>**DNS\_ERROR\_NO\_TCPIP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-498">9851 (0x267B)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-498">9851 (0x267B)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-499">Il protocollo di rete TCP/IP non è installato.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-499">TCP/IP network protocol not installed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-500"><span id="DNS_ERROR_NO_DNS_SERVERS"></span><span id="dns_error_no_dns_servers"></span>**\_errore DNS \_ nessun \_ \_ server DNS**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-500"><span id="DNS_ERROR_NO_DNS_SERVERS"></span><span id="dns_error_no_dns_servers"></span>**DNS\_ERROR\_NO\_DNS\_SERVERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-501">9852 (0x267C)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-501">9852 (0x267C)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-502">Nessun server DNS configurato per il sistema locale.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-502">No DNS servers configured for local system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-503"><span id="DNS_ERROR_DP_DOES_NOT_EXIST"></span><span id="dns_error_dp_does_not_exist"></span>**\_il DP di errore DNS non \_ \_ \_ \_ esiste**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-503"><span id="DNS_ERROR_DP_DOES_NOT_EXIST"></span><span id="dns_error_dp_does_not_exist"></span>**DNS\_ERROR\_DP\_DOES\_NOT\_EXIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-504">9901 (0x26AD)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-504">9901 (0x26AD)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-505">La partizione di directory specificata non esiste.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-505">The specified directory partition does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-506"><span id="DNS_ERROR_DP_ALREADY_EXISTS"></span><span id="dns_error_dp_already_exists"></span>**il \_ DP degli errori DNS \_ \_ \_ esiste già**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-506"><span id="DNS_ERROR_DP_ALREADY_EXISTS"></span><span id="dns_error_dp_already_exists"></span>**DNS\_ERROR\_DP\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-507">9902 (0x26AE)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-507">9902 (0x26AE)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-508">La partizione di directory specificata esiste già.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-508">The specified directory partition already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-509"><span id="DNS_ERROR_DP_NOT_ENLISTED"></span><span id="dns_error_dp_not_enlisted"></span>**\_errore DNS \_ DP \_ non \_ integrato**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-509"><span id="DNS_ERROR_DP_NOT_ENLISTED"></span><span id="dns_error_dp_not_enlisted"></span>**DNS\_ERROR\_DP\_NOT\_ENLISTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-510">9903 (0x26AF)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-510">9903 (0x26AF)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-511">Questo server DNS non è integrato nella partizione di directory specificata.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-511">This DNS server is not enlisted in the specified directory partition.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-512"><span id="DNS_ERROR_DP_ALREADY_ENLISTED"></span><span id="dns_error_dp_already_enlisted"></span>**il \_ DP degli errori DNS è \_ \_ già \_ integrato**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-512"><span id="DNS_ERROR_DP_ALREADY_ENLISTED"></span><span id="dns_error_dp_already_enlisted"></span>**DNS\_ERROR\_DP\_ALREADY\_ENLISTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-513">9904 (0x26B0)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-513">9904 (0x26B0)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-514">Questo server DNS è già integrato nella partizione di directory specificata.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-514">This DNS server is already enlisted in the specified directory partition.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-515"><span id="DNS_ERROR_DP_NOT_AVAILABLE"></span><span id="dns_error_dp_not_available"></span>**\_errore DNS \_ DP \_ non \_ disponibile**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-515"><span id="DNS_ERROR_DP_NOT_AVAILABLE"></span><span id="dns_error_dp_not_available"></span>**DNS\_ERROR\_DP\_NOT\_AVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-516">9905 (0x26B1)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-516">9905 (0x26B1)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-517">La partizione di directory non è disponibile in questo momento.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-517">The directory partition is not available at this time.</span></span> <span data-ttu-id="6b3a1-518">Attendere qualche minuto e riprovare più tardi.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-518">Please wait a few minutes and try again.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-519"><span id="DNS_ERROR_DP_FSMO_ERROR"></span><span id="dns_error_dp_fsmo_error"></span>**\_ \_ \_ errore FSMO DP errore \_ DNS**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-519"><span id="DNS_ERROR_DP_FSMO_ERROR"></span><span id="dns_error_dp_fsmo_error"></span>**DNS\_ERROR\_DP\_FSMO\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-520">9906 (0x26B2)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-520">9906 (0x26B2)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-521">Operazione non riuscita perché non è stato possibile raggiungere il ruolo FSMO master per la denominazione dei domini.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-521">The operation failed because the domain naming master FSMO role could not be reached.</span></span> <span data-ttu-id="6b3a1-522">Il controller di dominio che contiene il ruolo FSMO master per la denominazione dei domini non è attivo o non è in grado di gestire la richiesta o non è in esecuzione Windows Server 2003 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-522">The domain controller holding the domain naming master FSMO role is down or unable to service the request or is not running Windows Server 2003 or later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-523"><span id="WSAEINTR"></span><span id="wsaeintr"></span>**WSAEINTR**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-523"><span id="WSAEINTR"></span><span id="wsaeintr"></span>**WSAEINTR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-524">10004 (0x2714)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-524">10004 (0x2714)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-525">Un'operazione di blocco è stata interrotta da una chiamata a WSACancelBlockingCall.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-525">A blocking operation was interrupted by a call to WSACancelBlockingCall.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-526"><span id="WSAEBADF"></span><span id="wsaebadf"></span>**WSAEBADF**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-526"><span id="WSAEBADF"></span><span id="wsaebadf"></span>**WSAEBADF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-527">10009 (0x2719)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-527">10009 (0x2719)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-528">L'handle di file specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-528">The file handle supplied is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-529"><span id="WSAEACCES"></span><span id="wsaeacces"></span>**WSAEACCES**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-529"><span id="WSAEACCES"></span><span id="wsaeacces"></span>**WSAEACCES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-530">10013 (0x271D)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-530">10013 (0x271D)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-531">È stato effettuato un tentativo di accesso a un socket in modo non consentito dalle autorizzazioni di accesso.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-531">An attempt was made to access a socket in a way forbidden by its access permissions.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-532"><span id="WSAEFAULT"></span><span id="wsaefault"></span>**WSAEFAULT**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-532"><span id="WSAEFAULT"></span><span id="wsaefault"></span>**WSAEFAULT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-533">10014 (0x271E)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-533">10014 (0x271E)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-534">Il sistema ha rilevato un indirizzo puntatore non valido durante il tentativo di usare un argomento puntatore in una chiamata.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-534">The system detected an invalid pointer address in attempting to use a pointer argument in a call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-535"><span id="WSAEINVAL"></span><span id="wsaeinval"></span>**WSAEINVAL**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-535"><span id="WSAEINVAL"></span><span id="wsaeinval"></span>**WSAEINVAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-536">10022 (0x2726)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-536">10022 (0x2726)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-537">Argomento fornito non valido.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-537">An invalid argument was supplied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-538"><span id="WSAEMFILE"></span><span id="wsaemfile"></span>**WSAEMFILE**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-538"><span id="WSAEMFILE"></span><span id="wsaemfile"></span>**WSAEMFILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-539">10024 (0x2728)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-539">10024 (0x2728)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-540">Troppi socket aperti.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-540">Too many open sockets.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-541"><span id="WSAEWOULDBLOCK"></span><span id="wsaewouldblock"></span>**WSAEWOULDBLOCK**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-541"><span id="WSAEWOULDBLOCK"></span><span id="wsaewouldblock"></span>**WSAEWOULDBLOCK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-542">10035 (0x2733)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-542">10035 (0x2733)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-543">Non è stato possibile completare immediatamente un'operazione socket non bloccante.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-543">A non-blocking socket operation could not be completed immediately.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-544"><span id="WSAEINPROGRESS"></span><span id="wsaeinprogress"></span>**WSAEINPROGRESS**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-544"><span id="WSAEINPROGRESS"></span><span id="wsaeinprogress"></span>**WSAEINPROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-545">10036 (0x2734)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-545">10036 (0x2734)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-546">È in corso un'operazione di blocco.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-546">A blocking operation is currently executing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-547"><span id="WSAEALREADY"></span><span id="wsaealready"></span>**WSAEALREADY**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-547"><span id="WSAEALREADY"></span><span id="wsaealready"></span>**WSAEALREADY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-548">10037 (0x2735)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-548">10037 (0x2735)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-549">Si è tentato di eseguire un'operazione su un socket non bloccato sul quale era già in corso un'operazione.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-549">An operation was attempted on a non-blocking socket that already had an operation in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-550"><span id="WSAENOTSOCK"></span><span id="wsaenotsock"></span>**WSAENOTSOCK**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-550"><span id="WSAENOTSOCK"></span><span id="wsaenotsock"></span>**WSAENOTSOCK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-551">10038 (0x2736)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-551">10038 (0x2736)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-552">Si è tentato di eseguire un'operazione su un elemento che non è un socket.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-552">An operation was attempted on something that is not a socket.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-553"><span id="WSAEDESTADDRREQ"></span><span id="wsaedestaddrreq"></span>**WSAEDESTADDRREQ**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-553"><span id="WSAEDESTADDRREQ"></span><span id="wsaedestaddrreq"></span>**WSAEDESTADDRREQ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-554">10039 (0x2737)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-554">10039 (0x2737)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-555">Un indirizzo obbligatorio è stato omesso da un'operazione su un socket.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-555">A required address was omitted from an operation on a socket.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-556"><span id="WSAEMSGSIZE"></span><span id="wsaemsgsize"></span>**WSAEMSGSIZE**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-556"><span id="WSAEMSGSIZE"></span><span id="wsaemsgsize"></span>**WSAEMSGSIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-557">10040 (0x2738)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-557">10040 (0x2738)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-558">Le dimensioni di un messaggio inviato su un socket di datagramma erano maggiori del buffer del messaggio interno, erano presenti altri limiti di rete oppure le dimensioni del buffer utilizzato per ricevere un datagramma erano inferiori al datagramma stesso.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-558">A message sent on a datagram socket was larger than the internal message buffer or some other network limit, or the buffer used to receive a datagram into was smaller than the datagram itself.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-559"><span id="WSAEPROTOTYPE"></span><span id="wsaeprototype"></span>**WSAEPROTOTYPE**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-559"><span id="WSAEPROTOTYPE"></span><span id="wsaeprototype"></span>**WSAEPROTOTYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-560">10041 (0x2739)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-560">10041 (0x2739)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-561">Un protocollo è stato specificato nella chiamata di funzione socket che non supporta la semantica del tipo di socket richiesto.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-561">A protocol was specified in the socket function call that does not support the semantics of the socket type requested.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-562"><span id="WSAENOPROTOOPT"></span><span id="wsaenoprotoopt"></span>**WSAENOPROTOOPT**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-562"><span id="WSAENOPROTOOPT"></span><span id="wsaenoprotoopt"></span>**WSAENOPROTOOPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-563">10042 (0x273A)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-563">10042 (0x273A)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-564">È stata specificata un'opzione o un livello sconosciuto, non valido o non supportato in una chiamata a getsockopt o setsockopt.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-564">An unknown, invalid, or unsupported option or level was specified in a getsockopt or setsockopt call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-565"><span id="WSAEPROTONOSUPPORT"></span><span id="wsaeprotonosupport"></span>**WSAEPROTONOSUPPORT**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-565"><span id="WSAEPROTONOSUPPORT"></span><span id="wsaeprotonosupport"></span>**WSAEPROTONOSUPPORT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-566">10043 (0x273B)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-566">10043 (0x273B)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-567">Il protocollo richiesto non è stato configurato nel sistema o non ne esiste alcuna implementazione.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-567">The requested protocol has not been configured into the system, or no implementation for it exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-568"><span id="WSAESOCKTNOSUPPORT"></span><span id="wsaesocktnosupport"></span>**WSAESOCKTNOSUPPORT**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-568"><span id="WSAESOCKTNOSUPPORT"></span><span id="wsaesocktnosupport"></span>**WSAESOCKTNOSUPPORT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-569">10044 (0x273C)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-569">10044 (0x273C)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-570">Il supporto per il tipo di socket specificato non esiste in questa famiglia di indirizzi.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-570">The support for the specified socket type does not exist in this address family.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-571"><span id="WSAEOPNOTSUPP"></span><span id="wsaeopnotsupp"></span>**ILWSAEOPNOTSUPP**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-571"><span id="WSAEOPNOTSUPP"></span><span id="wsaeopnotsupp"></span>**WSAEOPNOTSUPP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-572">10045 (0x273D)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-572">10045 (0x273D)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-573">L'operazione tentata non è supportata per il tipo di oggetto a cui si fa riferimento.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-573">The attempted operation is not supported for the type of object referenced.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-574"><span id="WSAEPFNOSUPPORT"></span><span id="wsaepfnosupport"></span>**WSAEPFNOSUPPORT**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-574"><span id="WSAEPFNOSUPPORT"></span><span id="wsaepfnosupport"></span>**WSAEPFNOSUPPORT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-575">10046 (0x273E)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-575">10046 (0x273E)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-576">La famiglia di protocolli non è stata configurata nel sistema o non ne esiste alcuna implementazione.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-576">The protocol family has not been configured into the system or no implementation for it exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-577"><span id="WSAEAFNOSUPPORT"></span><span id="wsaeafnosupport"></span>**WSAEAFNOSUPPORT**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-577"><span id="WSAEAFNOSUPPORT"></span><span id="wsaeafnosupport"></span>**WSAEAFNOSUPPORT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-578">10047 (0x273F)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-578">10047 (0x273F)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-579">È stato usato un indirizzo incompatibile con il protocollo richiesto.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-579">An address incompatible with the requested protocol was used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-580"><span id="WSAEADDRINUSE"></span><span id="wsaeaddrinuse"></span>**WSAEADDRINUSE**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-580"><span id="WSAEADDRINUSE"></span><span id="wsaeaddrinuse"></span>**WSAEADDRINUSE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-581">10048 (0x2740)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-581">10048 (0x2740)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-582">Only one usage of each socket address (protocol/network address/port) is normally permitted.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-582">Only one usage of each socket address (protocol/network address/port) is normally permitted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-583"><span id="WSAEADDRNOTAVAIL"></span><span id="wsaeaddrnotavail"></span>**WSAEADDRNOTAVAIL**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-583"><span id="WSAEADDRNOTAVAIL"></span><span id="wsaeaddrnotavail"></span>**WSAEADDRNOTAVAIL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-584">10049 (0x2741)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-584">10049 (0x2741)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-585">L'indirizzo richiesto non è valido nel contesto.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-585">The requested address is not valid in its context.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-586"><span id="WSAENETDOWN"></span><span id="wsaenetdown"></span>**WSAENETDOWN**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-586"><span id="WSAENETDOWN"></span><span id="wsaenetdown"></span>**WSAENETDOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-587">10050 (0x2742)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-587">10050 (0x2742)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-588">Rete inattiva rilevata durante l'operazione del socket.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-588">A socket operation encountered a dead network.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-589"><span id="WSAENETUNREACH"></span><span id="wsaenetunreach"></span>**WSAENETUNREACH**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-589"><span id="WSAENETUNREACH"></span><span id="wsaenetunreach"></span>**WSAENETUNREACH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-590">10051 (0x2743)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-590">10051 (0x2743)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-591">Si è tentato di eseguire un'operazione socket in una rete irraggiungibile.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-591">A socket operation was attempted to an unreachable network.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-592"><span id="WSAENETRESET"></span><span id="wsaenetreset"></span>**WSAENETRESET**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-592"><span id="WSAENETRESET"></span><span id="wsaenetreset"></span>**WSAENETRESET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-593">10052 (0x2744)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-593">10052 (0x2744)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-594">La connessione è stata interrotta a causa di un'attività keep-alive che rileva un errore durante l'esecuzione dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-594">The connection has been broken due to keep-alive activity detecting a failure while the operation was in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-595"><span id="WSAECONNABORTED"></span><span id="wsaeconnaborted"></span>**WSAECONNABORTED**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-595"><span id="WSAECONNABORTED"></span><span id="wsaeconnaborted"></span>**WSAECONNABORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-596">10053 (0x2745)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-596">10053 (0x2745)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-597">Connessione interrotta dal software del computer host.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-597">An established connection was aborted by the software in your host machine.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-598"><span id="WSAECONNRESET"></span><span id="wsaeconnreset"></span>**WSAECONNRESET**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-598"><span id="WSAECONNRESET"></span><span id="wsaeconnreset"></span>**WSAECONNRESET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-599">10054 (0x2746)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-599">10054 (0x2746)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-600">Connessione in corso interrotta forzatamente dall'host remoto.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-600">An existing connection was forcibly closed by the remote host.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-601"><span id="WSAENOBUFS"></span><span id="wsaenobufs"></span>**WSAENOBUFS**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-601"><span id="WSAENOBUFS"></span><span id="wsaenobufs"></span>**WSAENOBUFS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-602">10055 (0x2747)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-602">10055 (0x2747)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-603">Non è stato possibile eseguire un'operazione su un socket perché il sistema non dispone di spazio sufficiente per il buffer o perché una coda era piena.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-603">An operation on a socket could not be performed because the system lacked sufficient buffer space or because a queue was full.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-604"><span id="WSAEISCONN"></span><span id="wsaeisconn"></span>**WSAEISCONN**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-604"><span id="WSAEISCONN"></span><span id="wsaeisconn"></span>**WSAEISCONN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-605">10056 (0x2748)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-605">10056 (0x2748)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-606">È stata effettuata una richiesta di connessione su un socket già connesso.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-606">A connect request was made on an already connected socket.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-607"><span id="WSAENOTCONN"></span><span id="wsaenotconn"></span>**WSAENOTCONN**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-607"><span id="WSAENOTCONN"></span><span id="wsaenotconn"></span>**WSAENOTCONN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-608">10057 (0x2749)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-608">10057 (0x2749)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-609">Socket non connesso e indirizzo non fornito durante l'invio su un socket di datagramma che utilizza una chiamata sendto. Richiesta di invio o ricezione di dati annullata.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-609">A request to send or receive data was disallowed because the socket is not connected and (when sending on a datagram socket using a sendto call) no address was supplied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-610"><span id="WSAESHUTDOWN"></span><span id="wsaeshutdown"></span>**WSAESHUTDOWN**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-610"><span id="WSAESHUTDOWN"></span><span id="wsaeshutdown"></span>**WSAESHUTDOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-611">10058 (0x274A)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-611">10058 (0x274A)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-612">Socket chiuso nella direzione specificata da una precedente chiamata di arresto. Richiesta di invio o ricezione dati annullata.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-612">A request to send or receive data was disallowed because the socket had already been shut down in that direction with a previous shutdown call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-613"><span id="WSAETOOMANYREFS"></span><span id="wsaetoomanyrefs"></span>**WSAETOOMANYREFS**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-613"><span id="WSAETOOMANYREFS"></span><span id="wsaetoomanyrefs"></span>**WSAETOOMANYREFS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-614">10059 (0x274B)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-614">10059 (0x274B)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-615">Troppi riferimenti a un oggetto kernel.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-615">Too many references to some kernel object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-616"><span id="WSAETIMEDOUT"></span><span id="wsaetimedout"></span>**WSAETIMEDOUT**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-616"><span id="WSAETIMEDOUT"></span><span id="wsaetimedout"></span>**WSAETIMEDOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-617">10060 (0x274C)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-617">10060 (0x274C)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-618">Tentativo di connessione non riuscito perché l'entità connessa non ha risposto correttamente dopo un periodo di tempo o la connessione stabilita non è riuscita perché l'host connesso non ha risposto.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-618">A connection attempt failed because the connected party did not properly respond after a period of time, or established connection failed because connected host has failed to respond.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-619"><span id="WSAECONNREFUSED"></span><span id="wsaeconnrefused"></span>**WSAECONNREFUSED**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-619"><span id="WSAECONNREFUSED"></span><span id="wsaeconnrefused"></span>**WSAECONNREFUSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-620">10061 (0x274D)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-620">10061 (0x274D)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-621">Non è stato possibile connettersi perché il computer di destinazione lo ha rifiutato attivamente.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-621">No connection could be made because the target machine actively refused it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-622"><span id="WSAELOOP"></span><span id="wsaeloop"></span>**WSAELOOP**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-622"><span id="WSAELOOP"></span><span id="wsaeloop"></span>**WSAELOOP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-623">10062 (0x274E)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-623">10062 (0x274E)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-624">Impossibile tradurre il nome.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-624">Cannot translate name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-625"><span id="WSAENAMETOOLONG"></span><span id="wsaenametoolong"></span>**WSAENAMETOOLONG**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-625"><span id="WSAENAMETOOLONG"></span><span id="wsaenametoolong"></span>**WSAENAMETOOLONG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-626">10063 (0x274F)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-626">10063 (0x274F)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-627">Il nome o il componente del nome è troppo lungo.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-627">Name component or name was too long.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-628"><span id="WSAEHOSTDOWN"></span><span id="wsaehostdown"></span>**WSAEHOSTDOWN**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-628"><span id="WSAEHOSTDOWN"></span><span id="wsaehostdown"></span>**WSAEHOSTDOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-629">10064 (0x2750)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-629">10064 (0x2750)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-630">Un'operazione socket non è riuscita perché l'host di destinazione è inattivo.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-630">A socket operation failed because the destination host was down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-631"><span id="WSAEHOSTUNREACH"></span><span id="wsaehostunreach"></span>**WSAEHOSTUNREACH**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-631"><span id="WSAEHOSTUNREACH"></span><span id="wsaehostunreach"></span>**WSAEHOSTUNREACH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-632">10065 (0x2751)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-632">10065 (0x2751)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-633">Tentativo di operazione del socket verso un host non raggiungibile.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-633">A socket operation was attempted to an unreachable host.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-634"><span id="WSAENOTEMPTY"></span><span id="wsaenotempty"></span>**WSAENOTEMPTY**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-634"><span id="WSAENOTEMPTY"></span><span id="wsaenotempty"></span>**WSAENOTEMPTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-635">10066 (0x2752)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-635">10066 (0x2752)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-636">Non è possibile rimuovere una directory che non è vuota.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-636">Cannot remove a directory that is not empty.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-637"><span id="WSAEPROCLIM"></span><span id="wsaeproclim"></span>**WSAEPROCLIM**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-637"><span id="WSAEPROCLIM"></span><span id="wsaeproclim"></span>**WSAEPROCLIM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-638">10067 (0x2753)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-638">10067 (0x2753)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-639">Un'implementazione di Windows Sockets può avere un limite al numero di applicazioni che possono utilizzarlo simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-639">A Windows Sockets implementation may have a limit on the number of applications that may use it simultaneously.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-640"><span id="WSAEUSERS"></span><span id="wsaeusers"></span>**WSAEUSERS**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-640"><span id="WSAEUSERS"></span><span id="wsaeusers"></span>**WSAEUSERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-641">10068 (0x2754)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-641">10068 (0x2754)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-642">Quota esaurita.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-642">Ran out of quota.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-643"><span id="WSAEDQUOT"></span><span id="wsaedquot"></span>**WSAEDQUOT**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-643"><span id="WSAEDQUOT"></span><span id="wsaedquot"></span>**WSAEDQUOT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-644">10069 (0x2755)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-644">10069 (0x2755)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-645">Quota del disco esaurita.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-645">Ran out of disk quota.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-646"><span id="WSAESTALE"></span><span id="wsaestale"></span>**WSAESTALE**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-646"><span id="WSAESTALE"></span><span id="wsaestale"></span>**WSAESTALE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-647">10070 (0x2756)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-647">10070 (0x2756)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-648">Il riferimento all'handle di file non è più disponibile.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-648">File handle reference is no longer available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-649"><span id="WSAEREMOTE"></span><span id="wsaeremote"></span>**WSAEREMOTE**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-649"><span id="WSAEREMOTE"></span><span id="wsaeremote"></span>**WSAEREMOTE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-650">10071 (0x2757)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-650">10071 (0x2757)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-651">Elemento non disponibile localmente.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-651">Item is not available locally.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-652"><span id="WSASYSNOTREADY"></span><span id="wsasysnotready"></span>**WSASYSNOTREADY**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-652"><span id="WSASYSNOTREADY"></span><span id="wsasysnotready"></span>**WSASYSNOTREADY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-653">10091 (0x276B)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-653">10091 (0x276B)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-654">WSAStartup non può funzionare in questo momento perché il sistema sottostante usato per fornire servizi di rete non è attualmente disponibile.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-654">WSAStartup cannot function at this time because the underlying system it uses to provide network services is currently unavailable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-655"><span id="WSAVERNOTSUPPORTED"></span><span id="wsavernotsupported"></span>**WSAVERNOTSUPPORTED**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-655"><span id="WSAVERNOTSUPPORTED"></span><span id="wsavernotsupported"></span>**WSAVERNOTSUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-656">10092 (0x276C)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-656">10092 (0x276C)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-657">La versione richiesta di Windows Sockets non è supportata.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-657">The Windows Sockets version requested is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-658"><span id="WSANOTINITIALISED"></span><span id="wsanotinitialised"></span>**WSANOTINITIALISED**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-658"><span id="WSANOTINITIALISED"></span><span id="wsanotinitialised"></span>**WSANOTINITIALISED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-659">10093 (0x276D)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-659">10093 (0x276D)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-660">L'applicazione non ha chiamato WSAStartup o WSAStartup non è riuscito.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-660">Either the application has not called WSAStartup, or WSAStartup failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-661"><span id="WSAEDISCON"></span><span id="wsaediscon"></span>**WSAEDISCON nativo**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-661"><span id="WSAEDISCON"></span><span id="wsaediscon"></span>**WSAEDISCON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-662">10101 (0x2775)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-662">10101 (0x2775)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-663">Restituito da WSARecv o WSARecvFrom per indicare che la parte remota ha avviato una sequenza di arresto normale.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-663">Returned by WSARecv or WSARecvFrom to indicate the remote party has initiated a graceful shutdown sequence.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-664"><span id="WSAENOMORE"></span><span id="wsaenomore"></span>**WSAENOMORE**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-664"><span id="WSAENOMORE"></span><span id="wsaenomore"></span>**WSAENOMORE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-665">10102 (0x2776)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-665">10102 (0x2776)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-666">WSALookupServiceNext non può restituire altri risultati.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-666">No more results can be returned by WSALookupServiceNext.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-667"><span id="WSAECANCELLED"></span><span id="wsaecancelled"></span>**WSAECANCELLED**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-667"><span id="WSAECANCELLED"></span><span id="wsaecancelled"></span>**WSAECANCELLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-668">10103 (0x2777)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-668">10103 (0x2777)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-669">È stata effettuata una chiamata a WSALookupServiceEnd mentre la chiamata era ancora in fase di elaborazione.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-669">A call to WSALookupServiceEnd was made while this call was still processing.</span></span> <span data-ttu-id="6b3a1-670">La chiamata è stata annullata.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-670">The call has been canceled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-671"><span id="WSAEINVALIDPROCTABLE"></span><span id="wsaeinvalidproctable"></span>**WSAEINVALIDPROCTABLE**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-671"><span id="WSAEINVALIDPROCTABLE"></span><span id="wsaeinvalidproctable"></span>**WSAEINVALIDPROCTABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-672">10104 (0x2778)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-672">10104 (0x2778)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-673">La tabella delle chiamate di procedura non è valida.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-673">The procedure call table is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-674"><span id="WSAEINVALIDPROVIDER"></span><span id="wsaeinvalidprovider"></span>**WSAEINVALIDPROVIDER**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-674"><span id="WSAEINVALIDPROVIDER"></span><span id="wsaeinvalidprovider"></span>**WSAEINVALIDPROVIDER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-675">10105 (0x2779)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-675">10105 (0x2779)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-676">Il provider di servizi richiesto non è valido.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-676">The requested service provider is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-677"><span id="WSAEPROVIDERFAILEDINIT"></span><span id="wsaeproviderfailedinit"></span>**WSAEPROVIDERFAILEDINIT**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-677"><span id="WSAEPROVIDERFAILEDINIT"></span><span id="wsaeproviderfailedinit"></span>**WSAEPROVIDERFAILEDINIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-678">10106 (0x277A)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-678">10106 (0x277A)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-679">Non è stato possibile caricare o inizializzare il provider di servizi richiesto.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-679">The requested service provider could not be loaded or initialized.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-680"><span id="WSASYSCALLFAILURE"></span><span id="wsasyscallfailure"></span>**WSASYSCALLFAILURE**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-680"><span id="WSASYSCALLFAILURE"></span><span id="wsasyscallfailure"></span>**WSASYSCALLFAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-681">10107 (0x277B)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-681">10107 (0x277B)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-682">Una chiamata di sistema non è riuscita.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-682">A system call has failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-683"><span id="WSASERVICE_NOT_FOUND"></span><span id="wsaservice_not_found"></span>**WSASERVICE \_ non \_ trovato**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-683"><span id="WSASERVICE_NOT_FOUND"></span><span id="wsaservice_not_found"></span>**WSASERVICE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-684">10108 (0x277C)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-684">10108 (0x277C)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-685">Nessun servizio di questo tipo è noto.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-685">No such service is known.</span></span> <span data-ttu-id="6b3a1-686">Il servizio non è stato trovato nello spazio dei nomi specificato.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-686">The service cannot be found in the specified name space.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-687"><span id="WSATYPE_NOT_FOUND"></span><span id="wsatype_not_found"></span>**WSATYPE \_ non \_ trovato**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-687"><span id="WSATYPE_NOT_FOUND"></span><span id="wsatype_not_found"></span>**WSATYPE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-688">10109 (0x277D)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-688">10109 (0x277D)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-689">La classe specificata non è stata trovata.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-689">The specified class was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-690"><span id="WSA_E_NO_MORE"></span><span id="wsa_e_no_more"></span>**WSA \_ E \_ nient' \_ altro**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-690"><span id="WSA_E_NO_MORE"></span><span id="wsa_e_no_more"></span>**WSA\_E\_NO\_MORE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-691">10110 (0x277E)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-691">10110 (0x277E)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-692">WSALookupServiceNext non può restituire altri risultati.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-692">No more results can be returned by WSALookupServiceNext.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-693"><span id="WSA_E_CANCELLED"></span><span id="wsa_e_cancelled"></span>**WSA \_ E \_ annullato**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-693"><span id="WSA_E_CANCELLED"></span><span id="wsa_e_cancelled"></span>**WSA\_E\_CANCELLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-694">10111 (0x277F)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-694">10111 (0x277F)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-695">È stata effettuata una chiamata a WSALookupServiceEnd mentre la chiamata era ancora in fase di elaborazione.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-695">A call to WSALookupServiceEnd was made while this call was still processing.</span></span> <span data-ttu-id="6b3a1-696">La chiamata è stata annullata.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-696">The call has been canceled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-697"><span id="WSAEREFUSED"></span><span id="wsaerefused"></span>**WSAEREFUSED**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-697"><span id="WSAEREFUSED"></span><span id="wsaerefused"></span>**WSAEREFUSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-698">10112 (0x2780)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-698">10112 (0x2780)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-699">Una query sul database non è riuscita perché è stata rifiutata attivamente.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-699">A database query failed because it was actively refused.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-700"><span id="WSAHOST_NOT_FOUND"></span><span id="wsahost_not_found"></span>**WSAHOST \_ non \_ trovato**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-700"><span id="WSAHOST_NOT_FOUND"></span><span id="wsahost_not_found"></span>**WSAHOST\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-701">11001 (0x2AF9)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-701">11001 (0x2AF9)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-702">L'host è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-702">No such host is known.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-703"><span id="WSATRY_AGAIN"></span><span id="wsatry_again"></span>**WSATRY di \_ nuovo**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-703"><span id="WSATRY_AGAIN"></span><span id="wsatry_again"></span>**WSATRY\_AGAIN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-704">11002 (0x2AFA)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-704">11002 (0x2AFA)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-705">Generalmente, questo è un errore temporaneo che si verifica durante la risoluzione dei nomi host e significa che il server locale non ha ricevuto una risposta da un server autorevole.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-705">This is usually a temporary error during hostname resolution and means that the local server did not receive a response from an authoritative server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-706"><span id="WSANO_RECOVERY"></span><span id="wsano_recovery"></span>**\_ripristino WSANO**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-706"><span id="WSANO_RECOVERY"></span><span id="wsano_recovery"></span>**WSANO\_RECOVERY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-707">11003 (0x2AFB)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-707">11003 (0x2AFB)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-708">Si è verificato un errore irreversibile durante la ricerca nel database.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-708">A non-recoverable error occurred during a database lookup.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-709"><span id="WSANO_DATA"></span><span id="wsano_data"></span>**\_dati WSANO**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-709"><span id="WSANO_DATA"></span><span id="wsano_data"></span>**WSANO\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-710">11004 (0x2AFC)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-710">11004 (0x2AFC)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-711">Il nome richiesto è valido, ma non sono stati trovati dati del tipo richiesto.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-711">The requested name is valid, but no data of the requested type was found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-712"><span id="WSA_QOS_RECEIVERS"></span><span id="wsa_qos_receivers"></span>**\_ricevitori QoS di WSA \_**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-712"><span id="WSA_QOS_RECEIVERS"></span><span id="wsa_qos_receivers"></span>**WSA\_QOS\_RECEIVERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-713">11005 (0x2AFD)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-713">11005 (0x2AFD)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-714">È arrivata almeno una riserva.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-714">At least one reserve has arrived.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-715"><span id="WSA_QOS_SENDERS"></span><span id="wsa_qos_senders"></span>**\_mittenti QoS per WSA \_**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-715"><span id="WSA_QOS_SENDERS"></span><span id="wsa_qos_senders"></span>**WSA\_QOS\_SENDERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-716">11006 (0x2AFE)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-716">11006 (0x2AFE)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-717">È arrivato almeno un percorso.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-717">At least one path has arrived.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-718"><span id="WSA_QOS_NO_SENDERS"></span><span id="wsa_qos_no_senders"></span>**\_QoS \_ non disponibile \_ per WSA**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-718"><span id="WSA_QOS_NO_SENDERS"></span><span id="wsa_qos_no_senders"></span>**WSA\_QOS\_NO\_SENDERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-719">11007 (0x2AFF)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-719">11007 (0x2AFF)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-720">Nessun mittenti.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-720">There are no senders.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-721"><span id="WSA_QOS_NO_RECEIVERS"></span><span id="wsa_qos_no_receivers"></span>**\_ \_ nessun ricevitore di QoS per WSA \_**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-721"><span id="WSA_QOS_NO_RECEIVERS"></span><span id="wsa_qos_no_receivers"></span>**WSA\_QOS\_NO\_RECEIVERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-722">11008 (0x2B00)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-722">11008 (0x2B00)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-723">Nessun ricevitore.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-723">There are no receivers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-724"><span id="WSA_QOS_REQUEST_CONFIRMED"></span><span id="wsa_qos_request_confirmed"></span>**\_richiesta QoS per WSA \_ \_ confermata**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-724"><span id="WSA_QOS_REQUEST_CONFIRMED"></span><span id="wsa_qos_request_confirmed"></span>**WSA\_QOS\_REQUEST\_CONFIRMED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-725">11009 (0x2B01)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-725">11009 (0x2B01)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-726">La riserva è stata confermata.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-726">Reserve has been confirmed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-727"><span id="WSA_QOS_ADMISSION_FAILURE"></span><span id="wsa_qos_admission_failure"></span>**\_errore di \_ ammissione \_ QoS di WSA**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-727"><span id="WSA_QOS_ADMISSION_FAILURE"></span><span id="wsa_qos_admission_failure"></span>**WSA\_QOS\_ADMISSION\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-728">11010 (0x2B02)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-728">11010 (0x2B02)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-729">Errore dovuto a risorse insufficienti.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-729">Error due to lack of resources.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-730"><span id="WSA_QOS_POLICY_FAILURE"></span><span id="wsa_qos_policy_failure"></span>**\_errore dei \_ criteri \_ QoS di WSA**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-730"><span id="WSA_QOS_POLICY_FAILURE"></span><span id="wsa_qos_policy_failure"></span>**WSA\_QOS\_POLICY\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-731">11011 (0x2B03)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-731">11011 (0x2B03)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-732">Rifiutato per motivi amministrativi: credenziali non valide.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-732">Rejected for administrative reasons - bad credentials.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-733"><span id="WSA_QOS_BAD_STYLE"></span><span id="wsa_qos_bad_style"></span>**\_stile non \_ valido \_ QoS per WSA**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-733"><span id="WSA_QOS_BAD_STYLE"></span><span id="wsa_qos_bad_style"></span>**WSA\_QOS\_BAD\_STYLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-734">11012 (0x2B04)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-734">11012 (0x2B04)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-735">Stile sconosciuto o in conflitto.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-735">Unknown or conflicting style.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-736"><span id="WSA_QOS_BAD_OBJECT"></span><span id="wsa_qos_bad_object"></span>**\_oggetto non \_ valido \_ QoS di WSA**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-736"><span id="WSA_QOS_BAD_OBJECT"></span><span id="wsa_qos_bad_object"></span>**WSA\_QOS\_BAD\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-737">11013 (0x2B05)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-737">11013 (0x2B05)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-738">Problema con una parte del buffer filterspec o providerspecific in generale.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-738">Problem with some part of the filterspec or providerspecific buffer in general.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-739"><span id="WSA_QOS_TRAFFIC_CTRL_ERROR"></span><span id="wsa_qos_traffic_ctrl_error"></span>**\_errore di \_ traffico QoS WSA \_ CTRL \_**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-739"><span id="WSA_QOS_TRAFFIC_CTRL_ERROR"></span><span id="wsa_qos_traffic_ctrl_error"></span>**WSA\_QOS\_TRAFFIC\_CTRL\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-740">11014 (0x2B06)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-740">11014 (0x2B06)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-741">Problemi con alcune parti del flowspec.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-741">Problem with some part of the flowspec.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-742"><span id="WSA_QOS_GENERIC_ERROR"></span><span id="wsa_qos_generic_error"></span>**\_ \_ errore generico di QoS WSA \_**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-742"><span id="WSA_QOS_GENERIC_ERROR"></span><span id="wsa_qos_generic_error"></span>**WSA\_QOS\_GENERIC\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-743">11015 (0x2B07)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-743">11015 (0x2B07)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-744">Errore QOS generale.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-744">General QOS error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-745"><span id="WSA_QOS_ESERVICETYPE"></span><span id="wsa_qos_eservicetype"></span>**\_ESERVICETYPE QoS per WSA \_**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-745"><span id="WSA_QOS_ESERVICETYPE"></span><span id="wsa_qos_eservicetype"></span>**WSA\_QOS\_ESERVICETYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-746">11016 (0x2B08)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-746">11016 (0x2B08)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-747">È stato trovato un tipo di servizio non valido o non riconosciuto in flowspec.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-747">An invalid or unrecognized service type was found in the flowspec.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-748"><span id="WSA_QOS_EFLOWSPEC"></span><span id="wsa_qos_eflowspec"></span>**\_EFLOWSPEC QoS per WSA \_**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-748"><span id="WSA_QOS_EFLOWSPEC"></span><span id="wsa_qos_eflowspec"></span>**WSA\_QOS\_EFLOWSPEC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-749">11017 (0x2B09)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-749">11017 (0x2B09)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-750">Flowspec non valido o incoerente trovato nella struttura QOS.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-750">An invalid or inconsistent flowspec was found in the QOS structure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-751"><span id="WSA_QOS_EPROVSPECBUF"></span><span id="wsa_qos_eprovspecbuf"></span>**\_EPROVSPECBUF QoS per WSA \_**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-751"><span id="WSA_QOS_EPROVSPECBUF"></span><span id="wsa_qos_eprovspecbuf"></span>**WSA\_QOS\_EPROVSPECBUF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-752">11018 (0x2B0A)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-752">11018 (0x2B0A)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-753">Buffer specifico del provider QOS non valido.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-753">Invalid QOS provider-specific buffer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-754"><span id="WSA_QOS_EFILTERSTYLE"></span><span id="wsa_qos_efilterstyle"></span>**\_EFILTERSTYLE QoS per WSA \_**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-754"><span id="WSA_QOS_EFILTERSTYLE"></span><span id="wsa_qos_efilterstyle"></span>**WSA\_QOS\_EFILTERSTYLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-755">11019 (0x2B0B)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-755">11019 (0x2B0B)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-756">È stato usato uno stile di filtro QOS non valido.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-756">An invalid QOS filter style was used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-757"><span id="WSA_QOS_EFILTERTYPE"></span><span id="wsa_qos_efiltertype"></span>**\_EFILTERTYPE QoS per WSA \_**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-757"><span id="WSA_QOS_EFILTERTYPE"></span><span id="wsa_qos_efiltertype"></span>**WSA\_QOS\_EFILTERTYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-758">11020 (0x2B0C)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-758">11020 (0x2B0C)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-759">È stato usato un tipo di filtro QOS non valido.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-759">An invalid QOS filter type was used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-760"><span id="WSA_QOS_EFILTERCOUNT"></span><span id="wsa_qos_efiltercount"></span>**\_EFILTERCOUNT QoS per WSA \_**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-760"><span id="WSA_QOS_EFILTERCOUNT"></span><span id="wsa_qos_efiltercount"></span>**WSA\_QOS\_EFILTERCOUNT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-761">11021 (0x2B0D)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-761">11021 (0x2B0D)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-762">Nel FLOWDESCRIPTOR è stato specificato un numero non corretto di FILTERSPECs QOS.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-762">An incorrect number of QOS FILTERSPECs were specified in the FLOWDESCRIPTOR.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-763"><span id="WSA_QOS_EOBJLENGTH"></span><span id="wsa_qos_eobjlength"></span>**\_EOBJLENGTH QoS per WSA \_**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-763"><span id="WSA_QOS_EOBJLENGTH"></span><span id="wsa_qos_eobjlength"></span>**WSA\_QOS\_EOBJLENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-764">11022 (0x2B0E)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-764">11022 (0x2B0E)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-765">In un buffer specifico del provider QOS è stato specificato un oggetto con un campo ObjectLength non valido.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-765">An object with an invalid ObjectLength field was specified in the QOS provider-specific buffer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-766"><span id="WSA_QOS_EFLOWCOUNT"></span><span id="wsa_qos_eflowcount"></span>**\_EFLOWCOUNT QoS per WSA \_**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-766"><span id="WSA_QOS_EFLOWCOUNT"></span><span id="wsa_qos_eflowcount"></span>**WSA\_QOS\_EFLOWCOUNT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-767">11023 (0x2B0F)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-767">11023 (0x2B0F)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-768">Nella struttura QOS è stato specificato un numero errato di descrittori di flusso.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-768">An incorrect number of flow descriptors was specified in the QOS structure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-769"><span id="WSA_QOS_EUNKOWNPSOBJ"></span><span id="wsa_qos_eunkownpsobj"></span>**\_EUNKOWNPSOBJ QoS per WSA \_**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-769"><span id="WSA_QOS_EUNKOWNPSOBJ"></span><span id="wsa_qos_eunkownpsobj"></span>**WSA\_QOS\_EUNKOWNPSOBJ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-770">11024 (0x2B10)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-770">11024 (0x2B10)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-771">Trovato oggetto non riconosciuto nel buffer di QOS specifico del provider.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-771">An unrecognized object was found in the QOS provider-specific buffer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-772"><span id="WSA_QOS_EPOLICYOBJ"></span><span id="wsa_qos_epolicyobj"></span>**\_EPOLICYOBJ QoS per WSA \_**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-772"><span id="WSA_QOS_EPOLICYOBJ"></span><span id="wsa_qos_epolicyobj"></span>**WSA\_QOS\_EPOLICYOBJ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-773">11025 (0x2B11)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-773">11025 (0x2B11)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-774">Trovato oggetto criteri non valido nel buffer specifico del provider QOS.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-774">An invalid policy object was found in the QOS provider-specific buffer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-775"><span id="WSA_QOS_EFLOWDESC"></span><span id="wsa_qos_eflowdesc"></span>**\_EFLOWDESC QoS per WSA \_**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-775"><span id="WSA_QOS_EFLOWDESC"></span><span id="wsa_qos_eflowdesc"></span>**WSA\_QOS\_EFLOWDESC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-776">11026 (0x2B12)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-776">11026 (0x2B12)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-777">Descrittore di flusso QOS non valido trovato nell'elenco dei descrittori di flusso.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-777">An invalid QOS flow descriptor was found in the flow descriptor list.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-778"><span id="WSA_QOS_EPSFLOWSPEC"></span><span id="wsa_qos_epsflowspec"></span>**\_EPSFLOWSPEC QoS per WSA \_**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-778"><span id="WSA_QOS_EPSFLOWSPEC"></span><span id="wsa_qos_epsflowspec"></span>**WSA\_QOS\_EPSFLOWSPEC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-779">11027 (0x2B13)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-779">11027 (0x2B13)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-780">Flowspec non valido o incoerente trovato nel buffer del provider QOS specifico.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-780">An invalid or inconsistent flowspec was found in the QOS provider specific buffer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-781"><span id="WSA_QOS_EPSFILTERSPEC"></span><span id="wsa_qos_epsfilterspec"></span>**\_EPSFILTERSPEC QoS per WSA \_**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-781"><span id="WSA_QOS_EPSFILTERSPEC"></span><span id="wsa_qos_epsfilterspec"></span>**WSA\_QOS\_EPSFILTERSPEC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-782">11028 (0x2B14)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-782">11028 (0x2B14)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-783">Trovato FILTERSPEC non valido nel buffer specifico del provider QOS.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-783">An invalid FILTERSPEC was found in the QOS provider-specific buffer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-784"><span id="WSA_QOS_ESDMODEOBJ"></span><span id="wsa_qos_esdmodeobj"></span>**\_ESDMODEOBJ QoS per WSA \_**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-784"><span id="WSA_QOS_ESDMODEOBJ"></span><span id="wsa_qos_esdmodeobj"></span>**WSA\_QOS\_ESDMODEOBJ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-785">11029 (0x2B15)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-785">11029 (0x2B15)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-786">Trovato oggetto modalità di scarto di forma non valido nel buffer del provider QOS specifico.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-786">An invalid shape discard mode object was found in the QOS provider specific buffer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-787"><span id="WSA_QOS_ESHAPERATEOBJ"></span><span id="wsa_qos_eshaperateobj"></span>**\_ESHAPERATEOBJ QoS per WSA \_**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-787"><span id="WSA_QOS_ESHAPERATEOBJ"></span><span id="wsa_qos_eshaperateobj"></span>**WSA\_QOS\_ESHAPERATEOBJ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-788">11030 (0x2B16)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-788">11030 (0x2B16)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-789">Trovato oggetto frequenza di shaping non valido nel buffer di QOS specifico del provider.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-789">An invalid shaping rate object was found in the QOS provider-specific buffer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-790"><span id="WSA_QOS_RESERVED_PETYPE"></span><span id="wsa_qos_reserved_petype"></span>**\_ \_ PETYPE riservato WSA \_ QoS**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-790"><span id="WSA_QOS_RESERVED_PETYPE"></span><span id="wsa_qos_reserved_petype"></span>**WSA\_QOS\_RESERVED\_PETYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-791">11031 (0x2B17)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-791">11031 (0x2B17)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-792">Un elemento dei criteri riservato è stato trovato nel buffer specifico del provider QOS.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-792">A reserved policy element was found in the QOS provider-specific buffer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-793"><span id="WSA_SECURE_HOST_NOT_FOUND"></span><span id="wsa_secure_host_not_found"></span>**\_host sicuro \_ WSA \_ non \_ trovato**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-793"><span id="WSA_SECURE_HOST_NOT_FOUND"></span><span id="wsa_secure_host_not_found"></span>**WSA\_SECURE\_HOST\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-794">11032 (0x2B18)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-794">11032 (0x2B18)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-795">Questo host non è noto in modo sicuro.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-795">No such host is known securely.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6b3a1-796"><span id="WSA_IPSEC_NAME_POLICY_ERROR"></span><span id="wsa_ipsec_name_policy_error"></span>**\_ \_ \_ errore criterio nome IPSec \_ WSA**</span><span class="sxs-lookup"><span data-stu-id="6b3a1-796"><span id="WSA_IPSEC_NAME_POLICY_ERROR"></span><span id="wsa_ipsec_name_policy_error"></span>**WSA\_IPSEC\_NAME\_POLICY\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b3a1-797">11033 (0x2B19)</span><span class="sxs-lookup"><span data-stu-id="6b3a1-797">11033 (0x2B19)</span></span>
</dt> <dt>



<span data-ttu-id="6b3a1-798">Non è stato possibile aggiungere i criteri IPSEC basati su nome.</span><span class="sxs-lookup"><span data-stu-id="6b3a1-798">Name based IPSEC policy could not be added.</span></span>


</dt> </dl> </dd> </dl>


## <a name="requirements"></a><span data-ttu-id="6b3a1-799">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6b3a1-799">Requirements</span></span>



| <span data-ttu-id="6b3a1-800">Requisito</span><span class="sxs-lookup"><span data-stu-id="6b3a1-800">Requirement</span></span> | <span data-ttu-id="6b3a1-801">Valore</span><span class="sxs-lookup"><span data-stu-id="6b3a1-801">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6b3a1-802">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6b3a1-802">Minimum supported client</span></span><br/> | <span data-ttu-id="6b3a1-803">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="6b3a1-803">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="6b3a1-804">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6b3a1-804">Minimum supported server</span></span><br/> | <span data-ttu-id="6b3a1-805">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6b3a1-805">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6b3a1-806">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6b3a1-806">Header</span></span><br/>                   | <dl> <span data-ttu-id="6b3a1-807"><dt>WinError. h</dt></span><span class="sxs-lookup"><span data-stu-id="6b3a1-807"><dt>WinError.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b3a1-808">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6b3a1-808">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b3a1-809">Codici di errore di sistema</span><span class="sxs-lookup"><span data-stu-id="6b3a1-809">System Error Codes</span></span>](system-error-codes.md)
</dt> </dl>

 

 




