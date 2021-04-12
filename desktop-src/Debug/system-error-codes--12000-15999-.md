---
description: Descrive i codici di errore 12000-1599 definiti nel file di intestazione WinError. h ed è destinato agli sviluppatori.
ms.assetid: bb3c658d-96db-495a-a0dc-e93949c3835d
title: Codici di errore di sistema (12000-15999) (WinError. h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: 8cac8adf6d8a4cf8f60fe978eb6f99f5efc1b9fe
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483324"
---
# <a name="system-error-codes-12000-15999"></a><span data-ttu-id="6415e-103">Codici di errore di sistema (12000-15999)</span><span class="sxs-lookup"><span data-stu-id="6415e-103">System Error Codes (12000-15999)</span></span>

> [!NOTE]
> <span data-ttu-id="6415e-104">Queste informazioni sono destinate agli sviluppatori che effettuano il debug degli errori di sistema.</span><span class="sxs-lookup"><span data-stu-id="6415e-104">This information is intended for developers debugging system errors.</span></span> <span data-ttu-id="6415e-105">Per altri errori, ad esempio problemi con Windows Update, è disponibile un elenco di risorse nella pagina [codici di errore](system-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="6415e-105">For other errors, such as issues with Windows Update, there is a list of resources on the [Error codes](system-error-codes.md) page.</span></span>

<span data-ttu-id="6415e-106">Nell'elenco seguente vengono descritti i [codici di errore di sistema](system-error-codes.md) (errori da 12000 a 15999).</span><span class="sxs-lookup"><span data-stu-id="6415e-106">The following list describes [system error codes](system-error-codes.md) (errors 12000 to 15999).</span></span> <span data-ttu-id="6415e-107">Vengono restituiti dalla funzione [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) quando molte funzioni hanno esito negativo.</span><span class="sxs-lookup"><span data-stu-id="6415e-107">They are returned by the [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function when many functions fail.</span></span> <span data-ttu-id="6415e-108">Per recuperare il testo della descrizione dell'errore nell'applicazione, usare la funzione [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) con il **formato \_ Message from flag \_ di \_ sistema** .</span><span class="sxs-lookup"><span data-stu-id="6415e-108">To retrieve the description text for the error in your application, use the [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) function with the **FORMAT\_MESSAGE\_FROM\_SYSTEM** flag.</span></span>

<dl> <dt>

<span data-ttu-id="6415e-109"><span id="ERROR_INTERNET__"></span><span id="error_internet__"></span>\**Errore \_ \_Internet \** _</span><span class="sxs-lookup"><span data-stu-id="6415e-109"><span id="ERROR_INTERNET__"></span><span id="error_internet__"></span>\**ERROR\_INTERNET\_\** _</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-110">12000-12175 (0x2EE0)</span><span class="sxs-lookup"><span data-stu-id="6415e-110">12000 - 12175 (0x2EE0)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-111">Vedere [codici di errore Internet](../wininet/wininet-errors.md) e Wininet. h.</span><span class="sxs-lookup"><span data-stu-id="6415e-111">See [Internet Error Codes](../wininet/wininet-errors.md) and WinInet.h.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-112"><span id="ERROR_IPSEC_QM_POLICY_EXISTS"></span><span id="error_ipsec_qm_policy_exists"></span>_ errore per il criterio di criteri di verifica *\_ IPSec \_ \_ \_ esistente*\*</span><span class="sxs-lookup"><span data-stu-id="6415e-112"><span id="ERROR_IPSEC_QM_POLICY_EXISTS"></span><span id="error_ipsec_qm_policy_exists"></span>_ *ERROR\_IPSEC\_QM\_POLICY\_EXISTS*\*</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-113">13000 (0x32C8)</span><span class="sxs-lookup"><span data-stu-id="6415e-113">13000 (0x32C8)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-114">Il criterio in modalità rapida specificato esiste già.</span><span class="sxs-lookup"><span data-stu-id="6415e-114">The specified quick mode policy already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-115"><span id="ERROR_IPSEC_QM_POLICY_NOT_FOUND"></span><span id="error_ipsec_qm_policy_not_found"></span>**\_ \_ \_ \_ Impossibile trovare il criterio \_ della linea di errore IPSec**</span><span class="sxs-lookup"><span data-stu-id="6415e-115"><span id="ERROR_IPSEC_QM_POLICY_NOT_FOUND"></span><span id="error_ipsec_qm_policy_not_found"></span>**ERROR\_IPSEC\_QM\_POLICY\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-116">13001 (0x32C9)</span><span class="sxs-lookup"><span data-stu-id="6415e-116">13001 (0x32C9)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-117">Impossibile trovare i criteri in modalità rapida specificati.</span><span class="sxs-lookup"><span data-stu-id="6415e-117">The specified quick mode policy was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-118"><span id="ERROR_IPSEC_QM_POLICY_IN_USE"></span><span id="error_ipsec_qm_policy_in_use"></span>**ERRORE \_ \_ per il \_ criterio \_ di \_ utilizzo criteri di errore IPSec**</span><span class="sxs-lookup"><span data-stu-id="6415e-118"><span id="ERROR_IPSEC_QM_POLICY_IN_USE"></span><span id="error_ipsec_qm_policy_in_use"></span>**ERROR\_IPSEC\_QM\_POLICY\_IN\_USE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-119">13002 (0x32CA)</span><span class="sxs-lookup"><span data-stu-id="6415e-119">13002 (0x32CA)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-120">Vengono utilizzati i criteri in modalità rapida specificati.</span><span class="sxs-lookup"><span data-stu-id="6415e-120">The specified quick mode policy is being used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-121"><span id="ERROR_IPSEC_MM_POLICY_EXISTS"></span><span id="error_ipsec_mm_policy_exists"></span>**il \_ criterio di errore IPSec \_ mm \_ \_ esiste**</span><span class="sxs-lookup"><span data-stu-id="6415e-121"><span id="ERROR_IPSEC_MM_POLICY_EXISTS"></span><span id="error_ipsec_mm_policy_exists"></span>**ERROR\_IPSEC\_MM\_POLICY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-122">13003 (0x32CB)</span><span class="sxs-lookup"><span data-stu-id="6415e-122">13003 (0x32CB)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-123">Il criterio della modalità principale specificato esiste già.</span><span class="sxs-lookup"><span data-stu-id="6415e-123">The specified main mode policy already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-124"><span id="ERROR_IPSEC_MM_POLICY_NOT_FOUND"></span><span id="error_ipsec_mm_policy_not_found"></span>**ERRORE \_ IPSec \_ mm \_ criterio \_ non \_ trovato**</span><span class="sxs-lookup"><span data-stu-id="6415e-124"><span id="ERROR_IPSEC_MM_POLICY_NOT_FOUND"></span><span id="error_ipsec_mm_policy_not_found"></span>**ERROR\_IPSEC\_MM\_POLICY\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-125">13004 (0x32CC)</span><span class="sxs-lookup"><span data-stu-id="6415e-125">13004 (0x32CC)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-126">Il criterio della modalità principale specificato non è stato trovato.</span><span class="sxs-lookup"><span data-stu-id="6415e-126">The specified main mode policy was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-127"><span id="ERROR_IPSEC_MM_POLICY_IN_USE"></span><span id="error_ipsec_mm_policy_in_use"></span>**\_ \_ criterio di errore IPSec mm \_ \_ in \_ uso**</span><span class="sxs-lookup"><span data-stu-id="6415e-127"><span id="ERROR_IPSEC_MM_POLICY_IN_USE"></span><span id="error_ipsec_mm_policy_in_use"></span>**ERROR\_IPSEC\_MM\_POLICY\_IN\_USE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-128">13005 (0x32CD)</span><span class="sxs-lookup"><span data-stu-id="6415e-128">13005 (0x32CD)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-129">Viene utilizzato il criterio della modalità principale specificato.</span><span class="sxs-lookup"><span data-stu-id="6415e-129">The specified main mode policy is being used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-130"><span id="ERROR_IPSEC_MM_FILTER_EXISTS"></span><span id="error_ipsec_mm_filter_exists"></span>**ERRORE \_ IPSec \_ mm \_ filtro \_ esistente**</span><span class="sxs-lookup"><span data-stu-id="6415e-130"><span id="ERROR_IPSEC_MM_FILTER_EXISTS"></span><span id="error_ipsec_mm_filter_exists"></span>**ERROR\_IPSEC\_MM\_FILTER\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-131">13006 (0x32CE)</span><span class="sxs-lookup"><span data-stu-id="6415e-131">13006 (0x32CE)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-132">Il filtro della modalità principale specificato esiste già.</span><span class="sxs-lookup"><span data-stu-id="6415e-132">The specified main mode filter already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-133"><span id="ERROR_IPSEC_MM_FILTER_NOT_FOUND"></span><span id="error_ipsec_mm_filter_not_found"></span>**ERRORE \_ di \_ filtro IPSec mm \_ \_ non \_ trovato**</span><span class="sxs-lookup"><span data-stu-id="6415e-133"><span id="ERROR_IPSEC_MM_FILTER_NOT_FOUND"></span><span id="error_ipsec_mm_filter_not_found"></span>**ERROR\_IPSEC\_MM\_FILTER\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-134">13007 (0x32CF)</span><span class="sxs-lookup"><span data-stu-id="6415e-134">13007 (0x32CF)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-135">Il filtro in modalità principale specificato non è stato trovato.</span><span class="sxs-lookup"><span data-stu-id="6415e-135">The specified main mode filter was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-136"><span id="ERROR_IPSEC_TRANSPORT_FILTER_EXISTS"></span><span id="error_ipsec_transport_filter_exists"></span>**ERRORE \_ \_ filtro trasporto \_ IPSec \_ esistente**</span><span class="sxs-lookup"><span data-stu-id="6415e-136"><span id="ERROR_IPSEC_TRANSPORT_FILTER_EXISTS"></span><span id="error_ipsec_transport_filter_exists"></span>**ERROR\_IPSEC\_TRANSPORT\_FILTER\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-137">13008 (0x32D0)</span><span class="sxs-lookup"><span data-stu-id="6415e-137">13008 (0x32D0)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-138">Il filtro della modalità di trasporto specificato esiste già.</span><span class="sxs-lookup"><span data-stu-id="6415e-138">The specified transport mode filter already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-139"><span id="ERROR_IPSEC_TRANSPORT_FILTER_NOT_FOUND"></span><span id="error_ipsec_transport_filter_not_found"></span>**ERRORE \_ di \_ filtro trasporto IPSec \_ \_ non \_ trovato**</span><span class="sxs-lookup"><span data-stu-id="6415e-139"><span id="ERROR_IPSEC_TRANSPORT_FILTER_NOT_FOUND"></span><span id="error_ipsec_transport_filter_not_found"></span>**ERROR\_IPSEC\_TRANSPORT\_FILTER\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-140">13009 (0x32D1)</span><span class="sxs-lookup"><span data-stu-id="6415e-140">13009 (0x32D1)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-141">Il filtro della modalità di trasporto specificato non esiste.</span><span class="sxs-lookup"><span data-stu-id="6415e-141">The specified transport mode filter does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-142"><span id="ERROR_IPSEC_MM_AUTH_EXISTS"></span><span id="error_ipsec_mm_auth_exists"></span>**ERRORE \_ \_ autenticazione IPSec \_ mm \_ esistente**</span><span class="sxs-lookup"><span data-stu-id="6415e-142"><span id="ERROR_IPSEC_MM_AUTH_EXISTS"></span><span id="error_ipsec_mm_auth_exists"></span>**ERROR\_IPSEC\_MM\_AUTH\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-143">13010 (0x32D2)</span><span class="sxs-lookup"><span data-stu-id="6415e-143">13010 (0x32D2)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-144">L'elenco di autenticazione in modalità principale specificato esiste.</span><span class="sxs-lookup"><span data-stu-id="6415e-144">The specified main mode authentication list exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-145"><span id="ERROR_IPSEC_MM_AUTH_NOT_FOUND"></span><span id="error_ipsec_mm_auth_not_found"></span>**ERRORE \_ IPSec \_ mm \_ auth \_ non \_ trovato**</span><span class="sxs-lookup"><span data-stu-id="6415e-145"><span id="ERROR_IPSEC_MM_AUTH_NOT_FOUND"></span><span id="error_ipsec_mm_auth_not_found"></span>**ERROR\_IPSEC\_MM\_AUTH\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-146">13011 (0x32D3)</span><span class="sxs-lookup"><span data-stu-id="6415e-146">13011 (0x32D3)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-147">L'elenco di autenticazione in modalità principale specificato non è stato trovato.</span><span class="sxs-lookup"><span data-stu-id="6415e-147">The specified main mode authentication list was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-148"><span id="ERROR_IPSEC_MM_AUTH_IN_USE"></span><span id="error_ipsec_mm_auth_in_use"></span>**ERRORE \_ \_ \_ di autenticazione IPSec mm \_ in \_ uso**</span><span class="sxs-lookup"><span data-stu-id="6415e-148"><span id="ERROR_IPSEC_MM_AUTH_IN_USE"></span><span id="error_ipsec_mm_auth_in_use"></span>**ERROR\_IPSEC\_MM\_AUTH\_IN\_USE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-149">13012 (0x32D4)</span><span class="sxs-lookup"><span data-stu-id="6415e-149">13012 (0x32D4)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-150">Viene utilizzato l'elenco di autenticazione in modalità principale specificato.</span><span class="sxs-lookup"><span data-stu-id="6415e-150">The specified main mode authentication list is being used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-151"><span id="ERROR_IPSEC_DEFAULT_MM_POLICY_NOT_FOUND"></span><span id="error_ipsec_default_mm_policy_not_found"></span>**errore \_ errore \_ IPSec \_ predefinito \_ mm \_ non \_ trovato**</span><span class="sxs-lookup"><span data-stu-id="6415e-151"><span id="ERROR_IPSEC_DEFAULT_MM_POLICY_NOT_FOUND"></span><span id="error_ipsec_default_mm_policy_not_found"></span>**ERROR\_IPSEC\_DEFAULT\_MM\_POLICY\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-152">13013 (0x32D5)</span><span class="sxs-lookup"><span data-stu-id="6415e-152">13013 (0x32D5)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-153">Il criterio della modalità principale predefinito specificato non è stato trovato.</span><span class="sxs-lookup"><span data-stu-id="6415e-153">The specified default main mode policy was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-154"><span id="ERROR_IPSEC_DEFAULT_MM_AUTH_NOT_FOUND"></span><span id="error_ipsec_default_mm_auth_not_found"></span>**ERRORE \_ di \_ autenticazione predefinita IPSec \_ mm \_ \_ non \_ trovato**</span><span class="sxs-lookup"><span data-stu-id="6415e-154"><span id="ERROR_IPSEC_DEFAULT_MM_AUTH_NOT_FOUND"></span><span id="error_ipsec_default_mm_auth_not_found"></span>**ERROR\_IPSEC\_DEFAULT\_MM\_AUTH\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-155">13014 (0x32D6)</span><span class="sxs-lookup"><span data-stu-id="6415e-155">13014 (0x32D6)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-156">L'elenco di autenticazione in modalità principale predefinito specificato non è stato trovato.</span><span class="sxs-lookup"><span data-stu-id="6415e-156">The specified default main mode authentication list was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-157"><span id="ERROR_IPSEC_DEFAULT_QM_POLICY_NOT_FOUND"></span><span id="error_ipsec_default_qm_policy_not_found"></span>**ERRORE \_ \_ \_ \_ \_ Impossibile trovare criteri mq predefiniti \_ IPSec**</span><span class="sxs-lookup"><span data-stu-id="6415e-157"><span id="ERROR_IPSEC_DEFAULT_QM_POLICY_NOT_FOUND"></span><span id="error_ipsec_default_qm_policy_not_found"></span>**ERROR\_IPSEC\_DEFAULT\_QM\_POLICY\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-158">13015 (0x32D7)</span><span class="sxs-lookup"><span data-stu-id="6415e-158">13015 (0x32D7)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-159">Impossibile trovare i criteri in modalità rapida predefiniti specificati.</span><span class="sxs-lookup"><span data-stu-id="6415e-159">The specified default quick mode policy was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-160"><span id="ERROR_IPSEC_TUNNEL_FILTER_EXISTS"></span><span id="error_ipsec_tunnel_filter_exists"></span>**ERRORE \_ \_ filtro tunnel \_ IPSec \_ esistente**</span><span class="sxs-lookup"><span data-stu-id="6415e-160"><span id="ERROR_IPSEC_TUNNEL_FILTER_EXISTS"></span><span id="error_ipsec_tunnel_filter_exists"></span>**ERROR\_IPSEC\_TUNNEL\_FILTER\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-161">13016 (0x32D8)</span><span class="sxs-lookup"><span data-stu-id="6415e-161">13016 (0x32D8)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-162">Il filtro in modalità tunnel specificato esiste.</span><span class="sxs-lookup"><span data-stu-id="6415e-162">The specified tunnel mode filter exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-163"><span id="ERROR_IPSEC_TUNNEL_FILTER_NOT_FOUND"></span><span id="error_ipsec_tunnel_filter_not_found"></span>**\_ \_ \_ \_ Impossibile trovare il filtro del tunnel IPSec di errore \_**</span><span class="sxs-lookup"><span data-stu-id="6415e-163"><span id="ERROR_IPSEC_TUNNEL_FILTER_NOT_FOUND"></span><span id="error_ipsec_tunnel_filter_not_found"></span>**ERROR\_IPSEC\_TUNNEL\_FILTER\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-164">13017 (0x32D9)</span><span class="sxs-lookup"><span data-stu-id="6415e-164">13017 (0x32D9)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-165">Il filtro in modalità tunnel specificato non è stato trovato.</span><span class="sxs-lookup"><span data-stu-id="6415e-165">The specified tunnel mode filter was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-166"><span id="ERROR_IPSEC_MM_FILTER_PENDING_DELETION"></span><span id="error_ipsec_mm_filter_pending_deletion"></span>**ERRORE \_ di \_ \_ eliminazione del filtro IPSec \_ in sospeso \_**</span><span class="sxs-lookup"><span data-stu-id="6415e-166"><span id="ERROR_IPSEC_MM_FILTER_PENDING_DELETION"></span><span id="error_ipsec_mm_filter_pending_deletion"></span>**ERROR\_IPSEC\_MM\_FILTER\_PENDING\_DELETION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-167">13018 (0x32DA)</span><span class="sxs-lookup"><span data-stu-id="6415e-167">13018 (0x32DA)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-168">Il filtro in modalità principale è in attesa di eliminazione.</span><span class="sxs-lookup"><span data-stu-id="6415e-168">The Main Mode filter is pending deletion.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-169"><span id="ERROR_IPSEC_TRANSPORT_FILTER_PENDING_DELETION"></span><span id="error_ipsec_transport_filter_pending_deletion"></span>**errore durante l' \_ \_ \_ \_ eliminazione in sospeso del filtro trasporto \_ IPSec**</span><span class="sxs-lookup"><span data-stu-id="6415e-169"><span id="ERROR_IPSEC_TRANSPORT_FILTER_PENDING_DELETION"></span><span id="error_ipsec_transport_filter_pending_deletion"></span>**ERROR\_IPSEC\_TRANSPORT\_FILTER\_PENDING\_DELETION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-170">13019 (0x32DB)</span><span class="sxs-lookup"><span data-stu-id="6415e-170">13019 (0x32DB)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-171">Il filtro di trasporto è in attesa di eliminazione.</span><span class="sxs-lookup"><span data-stu-id="6415e-171">The transport filter is pending deletion.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-172"><span id="ERROR_IPSEC_TUNNEL_FILTER_PENDING_DELETION"></span><span id="error_ipsec_tunnel_filter_pending_deletion"></span>**errore durante l' \_ \_ \_ \_ eliminazione in sospeso del filtro tunnel \_ IPSec**</span><span class="sxs-lookup"><span data-stu-id="6415e-172"><span id="ERROR_IPSEC_TUNNEL_FILTER_PENDING_DELETION"></span><span id="error_ipsec_tunnel_filter_pending_deletion"></span>**ERROR\_IPSEC\_TUNNEL\_FILTER\_PENDING\_DELETION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-173">13020 (0x32DC)</span><span class="sxs-lookup"><span data-stu-id="6415e-173">13020 (0x32DC)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-174">L'eliminazione del filtro del tunnel è in sospeso.</span><span class="sxs-lookup"><span data-stu-id="6415e-174">The tunnel filter is pending deletion.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-175"><span id="ERROR_IPSEC_MM_POLICY_PENDING_DELETION"></span><span id="error_ipsec_mm_policy_pending_deletion"></span>**ERRORE \_ del \_ criterio IPSec mm \_ \_ eliminazione in sospeso \_**</span><span class="sxs-lookup"><span data-stu-id="6415e-175"><span id="ERROR_IPSEC_MM_POLICY_PENDING_DELETION"></span><span id="error_ipsec_mm_policy_pending_deletion"></span>**ERROR\_IPSEC\_MM\_POLICY\_PENDING\_DELETION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-176">13021 (0x32DD)</span><span class="sxs-lookup"><span data-stu-id="6415e-176">13021 (0x32DD)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-177">Il criterio della modalità principale è in attesa di eliminazione.</span><span class="sxs-lookup"><span data-stu-id="6415e-177">The Main Mode policy is pending deletion.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-178"><span id="ERROR_IPSEC_MM_AUTH_PENDING_DELETION"></span><span id="error_ipsec_mm_auth_pending_deletion"></span>**ERRORE \_ di \_ autenticazione IPSec mm- \_ \_ eliminazione in sospeso \_**</span><span class="sxs-lookup"><span data-stu-id="6415e-178"><span id="ERROR_IPSEC_MM_AUTH_PENDING_DELETION"></span><span id="error_ipsec_mm_auth_pending_deletion"></span>**ERROR\_IPSEC\_MM\_AUTH\_PENDING\_DELETION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-179">13022 (0x32DE)</span><span class="sxs-lookup"><span data-stu-id="6415e-179">13022 (0x32DE)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-180">Il bundle di autenticazione in modalità principale è in attesa di eliminazione.</span><span class="sxs-lookup"><span data-stu-id="6415e-180">The Main Mode authentication bundle is pending deletion.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-181"><span id="ERROR_IPSEC_QM_POLICY_PENDING_DELETION"></span><span id="error_ipsec_qm_policy_pending_deletion"></span>**errore durante l' \_ \_ \_ \_ eliminazione in sospeso del criterio \_ per l'IPSec**</span><span class="sxs-lookup"><span data-stu-id="6415e-181"><span id="ERROR_IPSEC_QM_POLICY_PENDING_DELETION"></span><span id="error_ipsec_qm_policy_pending_deletion"></span>**ERROR\_IPSEC\_QM\_POLICY\_PENDING\_DELETION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-182">13023 (0x32DF)</span><span class="sxs-lookup"><span data-stu-id="6415e-182">13023 (0x32DF)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-183">L'eliminazione dei criteri in modalità rapida è in sospeso.</span><span class="sxs-lookup"><span data-stu-id="6415e-183">The Quick Mode policy is pending deletion.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-184"><span id="WARNING_IPSEC_MM_POLICY_PRUNED"></span><span id="warning_ipsec_mm_policy_pruned"></span>**AVVISO \_ \_ criteri IPSec \_ mm \_ eliminati**</span><span class="sxs-lookup"><span data-stu-id="6415e-184"><span id="WARNING_IPSEC_MM_POLICY_PRUNED"></span><span id="warning_ipsec_mm_policy_pruned"></span>**WARNING\_IPSEC\_MM\_POLICY\_PRUNED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-185">13024 (0x32E0)</span><span class="sxs-lookup"><span data-stu-id="6415e-185">13024 (0x32E0)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-186">Il criterio della modalità principale è stato aggiunto correttamente, ma alcune delle offerte richieste non sono supportate.</span><span class="sxs-lookup"><span data-stu-id="6415e-186">The Main Mode policy was successfully added, but some of the requested offers are not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-187"><span id="WARNING_IPSEC_QM_POLICY_PRUNED"></span><span id="warning_ipsec_qm_policy_pruned"></span>**AVVISO \_ di \_ criteri di mq IPSec \_ \_ eliminati**</span><span class="sxs-lookup"><span data-stu-id="6415e-187"><span id="WARNING_IPSEC_QM_POLICY_PRUNED"></span><span id="warning_ipsec_qm_policy_pruned"></span>**WARNING\_IPSEC\_QM\_POLICY\_PRUNED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-188">13025 (0x32E1)</span><span class="sxs-lookup"><span data-stu-id="6415e-188">13025 (0x32E1)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-189">Il criterio della modalità rapida è stato aggiunto correttamente, ma alcune delle offerte richieste non sono supportate.</span><span class="sxs-lookup"><span data-stu-id="6415e-189">The Quick Mode policy was successfully added, but some of the requested offers are not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-190"><span id="ERROR_IPSEC_IKE_NEG_STATUS_BEGIN"></span><span id="error_ipsec_ike_neg_status_begin"></span>**ERRORE \_ di \_ stato negativo IPSec IKE- \_ \_ \_ inizio**</span><span class="sxs-lookup"><span data-stu-id="6415e-190"><span id="ERROR_IPSEC_IKE_NEG_STATUS_BEGIN"></span><span id="error_ipsec_ike_neg_status_begin"></span>**ERROR\_IPSEC\_IKE\_NEG\_STATUS\_BEGIN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-191">13800 (0x35E8)</span><span class="sxs-lookup"><span data-stu-id="6415e-191">13800 (0x35E8)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-192">ERRORE \_ di \_ stato negativo IPSec IKE- \_ \_ \_ inizio</span><span class="sxs-lookup"><span data-stu-id="6415e-192">ERROR\_IPSEC\_IKE\_NEG\_STATUS\_BEGIN</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-193"><span id="ERROR_IPSEC_IKE_AUTH_FAIL"></span><span id="error_ipsec_ike_auth_fail"></span>**ERRORE \_ \_ autenticazione IKE \_ IPSec \_ non riuscita**</span><span class="sxs-lookup"><span data-stu-id="6415e-193"><span id="ERROR_IPSEC_IKE_AUTH_FAIL"></span><span id="error_ipsec_ike_auth_fail"></span>**ERROR\_IPSEC\_IKE\_AUTH\_FAIL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-194">13801 (0x35E9)</span><span class="sxs-lookup"><span data-stu-id="6415e-194">13801 (0x35E9)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-195">Le credenziali di autenticazione IKE sono inaccettabili.</span><span class="sxs-lookup"><span data-stu-id="6415e-195">IKE authentication credentials are unacceptable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-196"><span id="ERROR_IPSEC_IKE_ATTRIB_FAIL"></span><span id="error_ipsec_ike_attrib_fail"></span>**ERRORE \_ \_ attrib IKE \_ IPSec \_ non riuscita**</span><span class="sxs-lookup"><span data-stu-id="6415e-196"><span id="ERROR_IPSEC_IKE_ATTRIB_FAIL"></span><span id="error_ipsec_ike_attrib_fail"></span>**ERROR\_IPSEC\_IKE\_ATTRIB\_FAIL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-197">13802 (0x35EA)</span><span class="sxs-lookup"><span data-stu-id="6415e-197">13802 (0x35EA)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-198">Gli attributi di sicurezza IKE sono inaccettabili.</span><span class="sxs-lookup"><span data-stu-id="6415e-198">IKE security attributes are unacceptable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-199"><span id="ERROR_IPSEC_IKE_NEGOTIATION_PENDING"></span><span id="error_ipsec_ike_negotiation_pending"></span>**ERRORE \_ di \_ negoziazione IKE IPSec \_ \_ in sospeso**</span><span class="sxs-lookup"><span data-stu-id="6415e-199"><span id="ERROR_IPSEC_IKE_NEGOTIATION_PENDING"></span><span id="error_ipsec_ike_negotiation_pending"></span>**ERROR\_IPSEC\_IKE\_NEGOTIATION\_PENDING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-200">13803 (0x35EB)</span><span class="sxs-lookup"><span data-stu-id="6415e-200">13803 (0x35EB)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-201">Negoziazione IKE in corso.</span><span class="sxs-lookup"><span data-stu-id="6415e-201">IKE Negotiation in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-202"><span id="ERROR_IPSEC_IKE_GENERAL_PROCESSING_ERROR"></span><span id="error_ipsec_ike_general_processing_error"></span>**errore \_ di \_ \_ elaborazione generale \_ IKE \_ IPSec errore**</span><span class="sxs-lookup"><span data-stu-id="6415e-202"><span id="ERROR_IPSEC_IKE_GENERAL_PROCESSING_ERROR"></span><span id="error_ipsec_ike_general_processing_error"></span>**ERROR\_IPSEC\_IKE\_GENERAL\_PROCESSING\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-203">13804 (0x35EC)</span><span class="sxs-lookup"><span data-stu-id="6415e-203">13804 (0x35EC)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-204">Errore di elaborazione generale.</span><span class="sxs-lookup"><span data-stu-id="6415e-204">General processing error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-205"><span id="ERROR_IPSEC_IKE_TIMED_OUT"></span><span id="error_ipsec_ike_timed_out"></span>**\_ \_ Timeout IKE IPSec \_ errore \_**</span><span class="sxs-lookup"><span data-stu-id="6415e-205"><span id="ERROR_IPSEC_IKE_TIMED_OUT"></span><span id="error_ipsec_ike_timed_out"></span>**ERROR\_IPSEC\_IKE\_TIMED\_OUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-206">13805 (0x35ED)</span><span class="sxs-lookup"><span data-stu-id="6415e-206">13805 (0x35ED)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-207">Timeout della negoziazione.</span><span class="sxs-lookup"><span data-stu-id="6415e-207">Negotiation timed out.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-208"><span id="ERROR_IPSEC_IKE_NO_CERT"></span><span id="error_ipsec_ike_no_cert"></span>**ERRORE \_ IPSec \_ IKE \_ nessun \_ certificato**</span><span class="sxs-lookup"><span data-stu-id="6415e-208"><span id="ERROR_IPSEC_IKE_NO_CERT"></span><span id="error_ipsec_ike_no_cert"></span>**ERROR\_IPSEC\_IKE\_NO\_CERT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-209">13806 (0x35EE)</span><span class="sxs-lookup"><span data-stu-id="6415e-209">13806 (0x35EE)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-210">IKE non è riuscito a trovare il certificato del computer valido.</span><span class="sxs-lookup"><span data-stu-id="6415e-210">IKE failed to find valid machine certificate.</span></span> <span data-ttu-id="6415e-211">Contattare l'amministratore della sicurezza di rete per informazioni sull'installazione di un certificato valido nell'archivio certificati appropriato.</span><span class="sxs-lookup"><span data-stu-id="6415e-211">Contact your Network Security Administrator about installing a valid certificate in the appropriate Certificate Store.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-212"><span id="ERROR_IPSEC_IKE_SA_DELETED"></span><span id="error_ipsec_ike_sa_deleted"></span>**ERRORE \_ \_ SA IPSec \_ IKE \_ eliminato**</span><span class="sxs-lookup"><span data-stu-id="6415e-212"><span id="ERROR_IPSEC_IKE_SA_DELETED"></span><span id="error_ipsec_ike_sa_deleted"></span>**ERROR\_IPSEC\_IKE\_SA\_DELETED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-213">13807 (0x35EF)</span><span class="sxs-lookup"><span data-stu-id="6415e-213">13807 (0x35EF)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-214">La SA IKE è stata eliminata dal peer prima del completamento dell'installazione.</span><span class="sxs-lookup"><span data-stu-id="6415e-214">IKE SA deleted by peer before establishment completed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-215"><span id="ERROR_IPSEC_IKE_SA_REAPED"></span><span id="error_ipsec_ike_sa_reaped"></span>**ERRORE \_ \_ SA IPSec \_ IKE \_ raccolto**</span><span class="sxs-lookup"><span data-stu-id="6415e-215"><span id="ERROR_IPSEC_IKE_SA_REAPED"></span><span id="error_ipsec_ike_sa_reaped"></span>**ERROR\_IPSEC\_IKE\_SA\_REAPED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-216">13808 (0x35F0)</span><span class="sxs-lookup"><span data-stu-id="6415e-216">13808 (0x35F0)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-217">Il SA IKE è stato eliminato prima del completamento dell'installazione.</span><span class="sxs-lookup"><span data-stu-id="6415e-217">IKE SA deleted before establishment completed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-218"><span id="ERROR_IPSEC_IKE_MM_ACQUIRE_DROP"></span><span id="error_ipsec_ike_mm_acquire_drop"></span>**errore durante l' \_ \_ \_ \_ acquisizione \_ del protocollo IPSec**</span><span class="sxs-lookup"><span data-stu-id="6415e-218"><span id="ERROR_IPSEC_IKE_MM_ACQUIRE_DROP"></span><span id="error_ipsec_ike_mm_acquire_drop"></span>**ERROR\_IPSEC\_IKE\_MM\_ACQUIRE\_DROP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-219">13809 (0x35F1)</span><span class="sxs-lookup"><span data-stu-id="6415e-219">13809 (0x35F1)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-220">La richiesta di negoziazione è rimasta in coda troppo a lungo.</span><span class="sxs-lookup"><span data-stu-id="6415e-220">Negotiation request sat in Queue too long.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-221"><span id="ERROR_IPSEC_IKE_QM_ACQUIRE_DROP"></span><span id="error_ipsec_ike_qm_acquire_drop"></span>**errore durante l' \_ \_ acquisizione dell' \_ \_ \_ istruzione IPSec**</span><span class="sxs-lookup"><span data-stu-id="6415e-221"><span id="ERROR_IPSEC_IKE_QM_ACQUIRE_DROP"></span><span id="error_ipsec_ike_qm_acquire_drop"></span>**ERROR\_IPSEC\_IKE\_QM\_ACQUIRE\_DROP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-222">13810 (0x35F2)</span><span class="sxs-lookup"><span data-stu-id="6415e-222">13810 (0x35F2)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-223">La richiesta di negoziazione è rimasta in coda troppo a lungo.</span><span class="sxs-lookup"><span data-stu-id="6415e-223">Negotiation request sat in Queue too long.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-224"><span id="ERROR_IPSEC_IKE_QUEUE_DROP_MM"></span><span id="error_ipsec_ike_queue_drop_mm"></span>**ERRORE \_ di \_ \_ ricezione coda \_ IKE \_ IPSec**</span><span class="sxs-lookup"><span data-stu-id="6415e-224"><span id="ERROR_IPSEC_IKE_QUEUE_DROP_MM"></span><span id="error_ipsec_ike_queue_drop_mm"></span>**ERROR\_IPSEC\_IKE\_QUEUE\_DROP\_MM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-225">13811 (0x35F3)</span><span class="sxs-lookup"><span data-stu-id="6415e-225">13811 (0x35F3)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-226">La richiesta di negoziazione è rimasta in coda troppo a lungo.</span><span class="sxs-lookup"><span data-stu-id="6415e-226">Negotiation request sat in Queue too long.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-227"><span id="ERROR_IPSEC_IKE_QUEUE_DROP_NO_MM"></span><span id="error_ipsec_ike_queue_drop_no_mm"></span>**errore durante la coda di messaggi \_ \_ IKE IPSec \_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6415e-227"><span id="ERROR_IPSEC_IKE_QUEUE_DROP_NO_MM"></span><span id="error_ipsec_ike_queue_drop_no_mm"></span>**ERROR\_IPSEC\_IKE\_QUEUE\_DROP\_NO\_MM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-228">13812 (0x35F4)</span><span class="sxs-lookup"><span data-stu-id="6415e-228">13812 (0x35F4)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-229">La richiesta di negoziazione è rimasta in coda troppo a lungo.</span><span class="sxs-lookup"><span data-stu-id="6415e-229">Negotiation request sat in Queue too long.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-230"><span id="ERROR_IPSEC_IKE_DROP_NO_RESPONSE"></span><span id="error_ipsec_ike_drop_no_response"></span>**ERRORE \_ di \_ \_ eliminazione \_ Nessuna \_ risposta IKE IPSec**</span><span class="sxs-lookup"><span data-stu-id="6415e-230"><span id="ERROR_IPSEC_IKE_DROP_NO_RESPONSE"></span><span id="error_ipsec_ike_drop_no_response"></span>**ERROR\_IPSEC\_IKE\_DROP\_NO\_RESPONSE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-231">13813 (0x35F5)</span><span class="sxs-lookup"><span data-stu-id="6415e-231">13813 (0x35F5)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-232">Nessuna risposta da peer.</span><span class="sxs-lookup"><span data-stu-id="6415e-232">No response from peer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-233"><span id="ERROR_IPSEC_IKE_MM_DELAY_DROP"></span><span id="error_ipsec_ike_mm_delay_drop"></span>**errore errore \_ IPSec \_ IKE \_ mm \_ ritardo \_**</span><span class="sxs-lookup"><span data-stu-id="6415e-233"><span id="ERROR_IPSEC_IKE_MM_DELAY_DROP"></span><span id="error_ipsec_ike_mm_delay_drop"></span>**ERROR\_IPSEC\_IKE\_MM\_DELAY\_DROP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-234">13814 (0x35F6)</span><span class="sxs-lookup"><span data-stu-id="6415e-234">13814 (0x35F6)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-235">La negoziazione ha impiegato troppo tempo.</span><span class="sxs-lookup"><span data-stu-id="6415e-235">Negotiation took too long.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-236"><span id="ERROR_IPSEC_IKE_QM_DELAY_DROP"></span><span id="error_ipsec_ike_qm_delay_drop"></span>**errore durante la rimozione del \_ \_ \_ \_ ritardo IKE \_ .**</span><span class="sxs-lookup"><span data-stu-id="6415e-236"><span id="ERROR_IPSEC_IKE_QM_DELAY_DROP"></span><span id="error_ipsec_ike_qm_delay_drop"></span>**ERROR\_IPSEC\_IKE\_QM\_DELAY\_DROP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-237">13815 (0x35F7)</span><span class="sxs-lookup"><span data-stu-id="6415e-237">13815 (0x35F7)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-238">La negoziazione ha impiegato troppo tempo.</span><span class="sxs-lookup"><span data-stu-id="6415e-238">Negotiation took too long.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-239"><span id="ERROR_IPSEC_IKE_ERROR"></span><span id="error_ipsec_ike_error"></span>**errore \_ IKE IPSec errore \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6415e-239"><span id="ERROR_IPSEC_IKE_ERROR"></span><span id="error_ipsec_ike_error"></span>**ERROR\_IPSEC\_IKE\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-240">13816 (0x35F8)</span><span class="sxs-lookup"><span data-stu-id="6415e-240">13816 (0x35F8)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-241">Si è verificato un errore sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="6415e-241">Unknown error occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-242"><span id="ERROR_IPSEC_IKE_CRL_FAILED"></span><span id="error_ipsec_ike_crl_failed"></span>**ERRORE \_ \_ CRL IKE \_ IPSec \_ non riuscito**</span><span class="sxs-lookup"><span data-stu-id="6415e-242"><span id="ERROR_IPSEC_IKE_CRL_FAILED"></span><span id="error_ipsec_ike_crl_failed"></span>**ERROR\_IPSEC\_IKE\_CRL\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-243">13817 (0x35F9)</span><span class="sxs-lookup"><span data-stu-id="6415e-243">13817 (0x35F9)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-244">Verifica revoca certificato non riuscita.</span><span class="sxs-lookup"><span data-stu-id="6415e-244">Certificate Revocation Check failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-245"><span id="ERROR_IPSEC_IKE_INVALID_KEY_USAGE"></span><span id="error_ipsec_ike_invalid_key_usage"></span>**ERRORE \_ di \_ utilizzo della chiave IKE IPSec \_ non valido \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6415e-245"><span id="ERROR_IPSEC_IKE_INVALID_KEY_USAGE"></span><span id="error_ipsec_ike_invalid_key_usage"></span>**ERROR\_IPSEC\_IKE\_INVALID\_KEY\_USAGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-246">13818 (0x35FA)</span><span class="sxs-lookup"><span data-stu-id="6415e-246">13818 (0x35FA)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-247">Utilizzo chiave del certificato non valido.</span><span class="sxs-lookup"><span data-stu-id="6415e-247">Invalid certificate key usage.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-248"><span id="ERROR_IPSEC_IKE_INVALID_CERT_TYPE"></span><span id="error_ipsec_ike_invalid_cert_type"></span>**ERRORE \_ IPSec \_ IKE \_ \_ tipo di certificato non valido \_**</span><span class="sxs-lookup"><span data-stu-id="6415e-248"><span id="ERROR_IPSEC_IKE_INVALID_CERT_TYPE"></span><span id="error_ipsec_ike_invalid_cert_type"></span>**ERROR\_IPSEC\_IKE\_INVALID\_CERT\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-249">13819 (0x35FB)</span><span class="sxs-lookup"><span data-stu-id="6415e-249">13819 (0x35FB)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-250">Tipo di certificato non valido.</span><span class="sxs-lookup"><span data-stu-id="6415e-250">Invalid certificate type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-251"><span id="ERROR_IPSEC_IKE_NO_PRIVATE_KEY"></span><span id="error_ipsec_ike_no_private_key"></span>**ERRORE \_ IPSec \_ IKE \_ Nessuna \_ \_ chiave privata**</span><span class="sxs-lookup"><span data-stu-id="6415e-251"><span id="ERROR_IPSEC_IKE_NO_PRIVATE_KEY"></span><span id="error_ipsec_ike_no_private_key"></span>**ERROR\_IPSEC\_IKE\_NO\_PRIVATE\_KEY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-252">13820 (0x35FC)</span><span class="sxs-lookup"><span data-stu-id="6415e-252">13820 (0x35FC)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-253">Negoziazione IKE non riuscita perché il certificato del computer utilizzato non dispone di una chiave privata.</span><span class="sxs-lookup"><span data-stu-id="6415e-253">IKE negotiation failed because the machine certificate used does not have a private key.</span></span> <span data-ttu-id="6415e-254">I certificati IPsec richiedono una chiave privata.</span><span class="sxs-lookup"><span data-stu-id="6415e-254">IPsec certificates require a private key.</span></span> <span data-ttu-id="6415e-255">Contattare l'amministratore della sicurezza di rete per la sostituzione con un certificato con una chiave privata.</span><span class="sxs-lookup"><span data-stu-id="6415e-255">Contact your Network Security administrator about replacing with a certificate that has a private key.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-256"><span id="ERROR_IPSEC_IKE_SIMULTANEOUS_REKEY"></span><span id="error_ipsec_ike_simultaneous_rekey"></span>**ERRORE \_ \_ \_ REKEY simultaneo IKE IPSec \_**</span><span class="sxs-lookup"><span data-stu-id="6415e-256"><span id="ERROR_IPSEC_IKE_SIMULTANEOUS_REKEY"></span><span id="error_ipsec_ike_simultaneous_rekey"></span>**ERROR\_IPSEC\_IKE\_SIMULTANEOUS\_REKEY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-257">13821 (0x35FD)</span><span class="sxs-lookup"><span data-stu-id="6415e-257">13821 (0x35FD)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-258">Sono state rilevate richiavi simultanee.</span><span class="sxs-lookup"><span data-stu-id="6415e-258">Simultaneous rekeys were detected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-259"><span id="ERROR_IPSEC_IKE_DH_FAIL"></span><span id="error_ipsec_ike_dh_fail"></span>**errore \_ errore \_ IPSec \_ DH \_**</span><span class="sxs-lookup"><span data-stu-id="6415e-259"><span id="ERROR_IPSEC_IKE_DH_FAIL"></span><span id="error_ipsec_ike_dh_fail"></span>**ERROR\_IPSEC\_IKE\_DH\_FAIL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-260">13822 (0x35FE)</span><span class="sxs-lookup"><span data-stu-id="6415e-260">13822 (0x35FE)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-261">Errore nel calcolo Diffie-Hellman.</span><span class="sxs-lookup"><span data-stu-id="6415e-261">Failure in Diffie-Hellman computation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-262"><span id="ERROR_IPSEC_IKE_CRITICAL_PAYLOAD_NOT_RECOGNIZED"></span><span id="error_ipsec_ike_critical_payload_not_recognized"></span>**ERRORE \_ \_ \_ payload critico IKE \_ IPSec \_ non \_ riconosciuto**</span><span class="sxs-lookup"><span data-stu-id="6415e-262"><span id="ERROR_IPSEC_IKE_CRITICAL_PAYLOAD_NOT_RECOGNIZED"></span><span id="error_ipsec_ike_critical_payload_not_recognized"></span>**ERROR\_IPSEC\_IKE\_CRITICAL\_PAYLOAD\_NOT\_RECOGNIZED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-263">13823 (0x35FF)</span><span class="sxs-lookup"><span data-stu-id="6415e-263">13823 (0x35FF)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-264">Non si sa come elaborare il payload critico.</span><span class="sxs-lookup"><span data-stu-id="6415e-264">Don't know how to process critical payload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-265"><span id="ERROR_IPSEC_IKE_INVALID_HEADER"></span><span id="error_ipsec_ike_invalid_header"></span>**ERRORE \_ dell' \_ intestazione IKE IPSec \_ non valida \_**</span><span class="sxs-lookup"><span data-stu-id="6415e-265"><span id="ERROR_IPSEC_IKE_INVALID_HEADER"></span><span id="error_ipsec_ike_invalid_header"></span>**ERROR\_IPSEC\_IKE\_INVALID\_HEADER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-266">13824 (0x3600)</span><span class="sxs-lookup"><span data-stu-id="6415e-266">13824 (0x3600)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-267">Intestazione non valida.</span><span class="sxs-lookup"><span data-stu-id="6415e-267">Invalid header.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-268"><span id="ERROR_IPSEC_IKE_NO_POLICY"></span><span id="error_ipsec_ike_no_policy"></span>**ERRORE \_ IPSec \_ IKE \_ nessun \_ criterio**</span><span class="sxs-lookup"><span data-stu-id="6415e-268"><span id="ERROR_IPSEC_IKE_NO_POLICY"></span><span id="error_ipsec_ike_no_policy"></span>**ERROR\_IPSEC\_IKE\_NO\_POLICY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-269">13825 (0x3601)</span><span class="sxs-lookup"><span data-stu-id="6415e-269">13825 (0x3601)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-270">Nessun criterio configurato.</span><span class="sxs-lookup"><span data-stu-id="6415e-270">No policy configured.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-271"><span id="ERROR_IPSEC_IKE_INVALID_SIGNATURE"></span><span id="error_ipsec_ike_invalid_signature"></span>**ERRORE \_ di \_ firma IKE IPSec \_ non valida \_**</span><span class="sxs-lookup"><span data-stu-id="6415e-271"><span id="ERROR_IPSEC_IKE_INVALID_SIGNATURE"></span><span id="error_ipsec_ike_invalid_signature"></span>**ERROR\_IPSEC\_IKE\_INVALID\_SIGNATURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-272">13826 (0x3602)</span><span class="sxs-lookup"><span data-stu-id="6415e-272">13826 (0x3602)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-273">Impossibile verificare la firma.</span><span class="sxs-lookup"><span data-stu-id="6415e-273">Failed to verify signature.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-274"><span id="ERROR_IPSEC_IKE_KERBEROS_ERROR"></span><span id="error_ipsec_ike_kerberos_error"></span>**errore \_ \_ \_ errore Kerberos IKE \_ IPSec**</span><span class="sxs-lookup"><span data-stu-id="6415e-274"><span id="ERROR_IPSEC_IKE_KERBEROS_ERROR"></span><span id="error_ipsec_ike_kerberos_error"></span>**ERROR\_IPSEC\_IKE\_KERBEROS\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-275">13827 (0x3603)</span><span class="sxs-lookup"><span data-stu-id="6415e-275">13827 (0x3603)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-276">Non è stato possibile eseguire l'autenticazione tramite Kerberos.</span><span class="sxs-lookup"><span data-stu-id="6415e-276">Failed to authenticate using Kerberos.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-277"><span id="ERROR_IPSEC_IKE_NO_PUBLIC_KEY"></span><span id="error_ipsec_ike_no_public_key"></span>**ERRORE \_ \_ IKE IPSec \_ Nessuna \_ \_ chiave pubblica**</span><span class="sxs-lookup"><span data-stu-id="6415e-277"><span id="ERROR_IPSEC_IKE_NO_PUBLIC_KEY"></span><span id="error_ipsec_ike_no_public_key"></span>**ERROR\_IPSEC\_IKE\_NO\_PUBLIC\_KEY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-278">13828 (0x3604)</span><span class="sxs-lookup"><span data-stu-id="6415e-278">13828 (0x3604)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-279">Il certificato del peer non ha una chiave pubblica.</span><span class="sxs-lookup"><span data-stu-id="6415e-279">Peer's certificate did not have a public key.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-280"><span id="ERROR_IPSEC_IKE_PROCESS_ERR"></span><span id="error_ipsec_ike_process_err"></span>**ERRORE \_ \_ processo IKE \_ IPSec \_ errore**</span><span class="sxs-lookup"><span data-stu-id="6415e-280"><span id="ERROR_IPSEC_IKE_PROCESS_ERR"></span><span id="error_ipsec_ike_process_err"></span>**ERROR\_IPSEC\_IKE\_PROCESS\_ERR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-281">13829 (0x3605)</span><span class="sxs-lookup"><span data-stu-id="6415e-281">13829 (0x3605)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-282">Errore durante l'elaborazione del payload degli errori.</span><span class="sxs-lookup"><span data-stu-id="6415e-282">Error processing error payload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-283"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_SA"></span><span id="error_ipsec_ike_process_err_sa"></span>**ERRORE \_ del \_ processo IKE IPSec \_ \_ Err \_ sa**</span><span class="sxs-lookup"><span data-stu-id="6415e-283"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_SA"></span><span id="error_ipsec_ike_process_err_sa"></span>**ERROR\_IPSEC\_IKE\_PROCESS\_ERR\_SA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-284">13830 (0x3606)</span><span class="sxs-lookup"><span data-stu-id="6415e-284">13830 (0x3606)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-285">Errore durante l'elaborazione del payload SA.</span><span class="sxs-lookup"><span data-stu-id="6415e-285">Error processing SA payload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-286"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_PROP"></span><span id="error_ipsec_ike_process_err_prop"></span>**ERRORE \_ \_ processo IKE IPSec \_ processo \_ Err \_ prop**</span><span class="sxs-lookup"><span data-stu-id="6415e-286"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_PROP"></span><span id="error_ipsec_ike_process_err_prop"></span>**ERROR\_IPSEC\_IKE\_PROCESS\_ERR\_PROP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-287">13831 (0x3607)</span><span class="sxs-lookup"><span data-stu-id="6415e-287">13831 (0x3607)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-288">Errore durante l'elaborazione del payload della proposta.</span><span class="sxs-lookup"><span data-stu-id="6415e-288">Error processing Proposal payload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-289"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_TRANS"></span><span id="error_ipsec_ike_process_err_trans"></span>**ERRORE \_ \_ processo IKE \_ IPSec \_ \_ transazione**</span><span class="sxs-lookup"><span data-stu-id="6415e-289"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_TRANS"></span><span id="error_ipsec_ike_process_err_trans"></span>**ERROR\_IPSEC\_IKE\_PROCESS\_ERR\_TRANS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-290">13832 (0x3608)</span><span class="sxs-lookup"><span data-stu-id="6415e-290">13832 (0x3608)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-291">Errore durante l'elaborazione del payload di trasformazione.</span><span class="sxs-lookup"><span data-stu-id="6415e-291">Error processing Transform payload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-292"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_KE"></span><span id="error_ipsec_ike_process_err_ke"></span>**ERRORE \_ il \_ processo IKE IPSec \_ \_ Err \_ ke**</span><span class="sxs-lookup"><span data-stu-id="6415e-292"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_KE"></span><span id="error_ipsec_ike_process_err_ke"></span>**ERROR\_IPSEC\_IKE\_PROCESS\_ERR\_KE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-293">13833 (0x3609)</span><span class="sxs-lookup"><span data-stu-id="6415e-293">13833 (0x3609)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-294">Errore durante l'elaborazione del payload KE.</span><span class="sxs-lookup"><span data-stu-id="6415e-294">Error processing KE payload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-295"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_ID"></span><span id="error_ipsec_ike_process_err_id"></span>**errore \_ errore \_ IPSec \_ processo \_ IKE \_ ID**</span><span class="sxs-lookup"><span data-stu-id="6415e-295"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_ID"></span><span id="error_ipsec_ike_process_err_id"></span>**ERROR\_IPSEC\_IKE\_PROCESS\_ERR\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-296">13834 (0x360A)</span><span class="sxs-lookup"><span data-stu-id="6415e-296">13834 (0x360A)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-297">Errore durante l'elaborazione del payload dell'ID.</span><span class="sxs-lookup"><span data-stu-id="6415e-297">Error processing ID payload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-298"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_CERT"></span><span id="error_ipsec_ike_process_err_cert"></span>**ERRORE \_ \_ processo IKE IPSec \_ processo \_ Err \_ certificato**</span><span class="sxs-lookup"><span data-stu-id="6415e-298"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_CERT"></span><span id="error_ipsec_ike_process_err_cert"></span>**ERROR\_IPSEC\_IKE\_PROCESS\_ERR\_CERT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-299">13835 (0x360B)</span><span class="sxs-lookup"><span data-stu-id="6415e-299">13835 (0x360B)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-300">Errore durante l'elaborazione del payload del certificato.</span><span class="sxs-lookup"><span data-stu-id="6415e-300">Error processing Cert payload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-301"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_CERT_REQ"></span><span id="error_ipsec_ike_process_err_cert_req"></span>**ERRORE \_ \_ processo IKE \_ IPSec \_ Err \_ CERT \_ req**</span><span class="sxs-lookup"><span data-stu-id="6415e-301"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_CERT_REQ"></span><span id="error_ipsec_ike_process_err_cert_req"></span>**ERROR\_IPSEC\_IKE\_PROCESS\_ERR\_CERT\_REQ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-302">13836 (0x360C)</span><span class="sxs-lookup"><span data-stu-id="6415e-302">13836 (0x360C)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-303">Errore durante l'elaborazione del payload della richiesta di certificato.</span><span class="sxs-lookup"><span data-stu-id="6415e-303">Error processing Certificate Request payload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-304"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_HASH"></span><span id="error_ipsec_ike_process_err_hash"></span>**ERRORE \_ dell' \_ \_ \_ hash Err del processo IKE IPSec \_**</span><span class="sxs-lookup"><span data-stu-id="6415e-304"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_HASH"></span><span id="error_ipsec_ike_process_err_hash"></span>**ERROR\_IPSEC\_IKE\_PROCESS\_ERR\_HASH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-305">13837 (0x360D)</span><span class="sxs-lookup"><span data-stu-id="6415e-305">13837 (0x360D)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-306">Errore durante l'elaborazione del payload hash.</span><span class="sxs-lookup"><span data-stu-id="6415e-306">Error processing Hash payload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-307"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_SIG"></span><span id="error_ipsec_ike_process_err_sig"></span>**ERRORE \_ \_ processo IKE \_ IPSec \_ Err \_ sig**</span><span class="sxs-lookup"><span data-stu-id="6415e-307"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_SIG"></span><span id="error_ipsec_ike_process_err_sig"></span>**ERROR\_IPSEC\_IKE\_PROCESS\_ERR\_SIG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-308">13838 (0x360E)</span><span class="sxs-lookup"><span data-stu-id="6415e-308">13838 (0x360E)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-309">Errore durante l'elaborazione del payload della firma.</span><span class="sxs-lookup"><span data-stu-id="6415e-309">Error processing Signature payload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-310"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_NONCE"></span><span id="error_ipsec_ike_process_err_nonce"></span>**ERRORE \_ \_ nonce del \_ processo \_ IKE \_ IPSec**</span><span class="sxs-lookup"><span data-stu-id="6415e-310"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_NONCE"></span><span id="error_ipsec_ike_process_err_nonce"></span>**ERROR\_IPSEC\_IKE\_PROCESS\_ERR\_NONCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-311">13839 (0x360F)</span><span class="sxs-lookup"><span data-stu-id="6415e-311">13839 (0x360F)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-312">Errore durante l'elaborazione del payload nonce.</span><span class="sxs-lookup"><span data-stu-id="6415e-312">Error processing Nonce payload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-313"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_NOTIFY"></span><span id="error_ipsec_ike_process_err_notify"></span>**errore \_ errore \_ IPSec \_ processo \_ IKE \_ notifica**</span><span class="sxs-lookup"><span data-stu-id="6415e-313"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_NOTIFY"></span><span id="error_ipsec_ike_process_err_notify"></span>**ERROR\_IPSEC\_IKE\_PROCESS\_ERR\_NOTIFY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-314">13840 (0x3610)</span><span class="sxs-lookup"><span data-stu-id="6415e-314">13840 (0x3610)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-315">Errore durante l'elaborazione del payload di notifica.</span><span class="sxs-lookup"><span data-stu-id="6415e-315">Error processing Notify payload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-316"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_DELETE"></span><span id="error_ipsec_ike_process_err_delete"></span>**errore \_ errore \_ IPSec \_ processo \_ IKE \_ Delete**</span><span class="sxs-lookup"><span data-stu-id="6415e-316"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_DELETE"></span><span id="error_ipsec_ike_process_err_delete"></span>**ERROR\_IPSEC\_IKE\_PROCESS\_ERR\_DELETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-317">13841 (0x3611)</span><span class="sxs-lookup"><span data-stu-id="6415e-317">13841 (0x3611)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-318">Errore durante l'elaborazione del payload Delete.</span><span class="sxs-lookup"><span data-stu-id="6415e-318">Error processing Delete Payload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-319"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_VENDOR"></span><span id="error_ipsec_ike_process_err_vendor"></span>**ERRORE \_ del \_ \_ \_ Fornitore Err del processo IKE IPSec \_**</span><span class="sxs-lookup"><span data-stu-id="6415e-319"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_VENDOR"></span><span id="error_ipsec_ike_process_err_vendor"></span>**ERROR\_IPSEC\_IKE\_PROCESS\_ERR\_VENDOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-320">13842 (0x3612)</span><span class="sxs-lookup"><span data-stu-id="6415e-320">13842 (0x3612)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-321">Errore durante l'elaborazione del payload VendorId.</span><span class="sxs-lookup"><span data-stu-id="6415e-321">Error processing VendorId payload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-322"><span id="ERROR_IPSEC_IKE_INVALID_PAYLOAD"></span><span id="error_ipsec_ike_invalid_payload"></span>**ERRORE \_ \_ payload IKE \_ non valido \_**</span><span class="sxs-lookup"><span data-stu-id="6415e-322"><span id="ERROR_IPSEC_IKE_INVALID_PAYLOAD"></span><span id="error_ipsec_ike_invalid_payload"></span>**ERROR\_IPSEC\_IKE\_INVALID\_PAYLOAD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-323">13843 (0x3613)</span><span class="sxs-lookup"><span data-stu-id="6415e-323">13843 (0x3613)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-324">Ricevuto payload non valido.</span><span class="sxs-lookup"><span data-stu-id="6415e-324">Invalid payload received.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-325"><span id="ERROR_IPSEC_IKE_LOAD_SOFT_SA"></span><span id="error_ipsec_ike_load_soft_sa"></span>**ERRORE \_ di \_ \_ caricamento \_ software IKE \_ IPSec**</span><span class="sxs-lookup"><span data-stu-id="6415e-325"><span id="ERROR_IPSEC_IKE_LOAD_SOFT_SA"></span><span id="error_ipsec_ike_load_soft_sa"></span>**ERROR\_IPSEC\_IKE\_LOAD\_SOFT\_SA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-326">13844 (0x3614)</span><span class="sxs-lookup"><span data-stu-id="6415e-326">13844 (0x3614)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-327">Il SA è stato caricato.</span><span class="sxs-lookup"><span data-stu-id="6415e-327">Soft SA loaded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-328"><span id="ERROR_IPSEC_IKE_SOFT_SA_TORN_DOWN"></span><span id="error_ipsec_ike_soft_sa_torn_down"></span>**ERRORE dell'amministratore di \_ \_ \_ software IKE Soft \_ sa \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6415e-328"><span id="ERROR_IPSEC_IKE_SOFT_SA_TORN_DOWN"></span><span id="error_ipsec_ike_soft_sa_torn_down"></span>**ERROR\_IPSEC\_IKE\_SOFT\_SA\_TORN\_DOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-329">13845 (0x3615)</span><span class="sxs-lookup"><span data-stu-id="6415e-329">13845 (0x3615)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-330">Abbassamento di SA soft.</span><span class="sxs-lookup"><span data-stu-id="6415e-330">Soft SA torn down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-331"><span id="ERROR_IPSEC_IKE_INVALID_COOKIE"></span><span id="error_ipsec_ike_invalid_cookie"></span>**ERRORE \_ \_ IKE IPSec \_ non valido \_**</span><span class="sxs-lookup"><span data-stu-id="6415e-331"><span id="ERROR_IPSEC_IKE_INVALID_COOKIE"></span><span id="error_ipsec_ike_invalid_cookie"></span>**ERROR\_IPSEC\_IKE\_INVALID\_COOKIE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-332">13846 (0x3616)</span><span class="sxs-lookup"><span data-stu-id="6415e-332">13846 (0x3616)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-333">Ricevuto cookie non valido.</span><span class="sxs-lookup"><span data-stu-id="6415e-333">Invalid cookie received.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-334"><span id="ERROR_IPSEC_IKE_NO_PEER_CERT"></span><span id="error_ipsec_ike_no_peer_cert"></span>**ERRORE \_ IPSec \_ \_ non IKE \_ nessun \_ certificato peer**</span><span class="sxs-lookup"><span data-stu-id="6415e-334"><span id="ERROR_IPSEC_IKE_NO_PEER_CERT"></span><span id="error_ipsec_ike_no_peer_cert"></span>**ERROR\_IPSEC\_IKE\_NO\_PEER\_CERT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-335">13847 (0x3617)</span><span class="sxs-lookup"><span data-stu-id="6415e-335">13847 (0x3617)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-336">Il peer non è riuscito a inviare un certificato macchina valido.</span><span class="sxs-lookup"><span data-stu-id="6415e-336">Peer failed to send valid machine certificate.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-337"><span id="ERROR_IPSEC_IKE_PEER_CRL_FAILED"></span><span id="error_ipsec_ike_peer_crl_failed"></span>**ERRORE \_ del \_ \_ peer CRL IKE IPSec \_ \_ non riuscito**</span><span class="sxs-lookup"><span data-stu-id="6415e-337"><span id="ERROR_IPSEC_IKE_PEER_CRL_FAILED"></span><span id="error_ipsec_ike_peer_crl_failed"></span>**ERROR\_IPSEC\_IKE\_PEER\_CRL\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-338">13848 (0x3618)</span><span class="sxs-lookup"><span data-stu-id="6415e-338">13848 (0x3618)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-339">Verifica revoca certificati del certificato del peer non riuscita.</span><span class="sxs-lookup"><span data-stu-id="6415e-339">Certification Revocation check of peer's certificate failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-340"><span id="ERROR_IPSEC_IKE_POLICY_CHANGE"></span><span id="error_ipsec_ike_policy_change"></span>**errore durante la \_ \_ modifica dei criteri IKE IPSec \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6415e-340"><span id="ERROR_IPSEC_IKE_POLICY_CHANGE"></span><span id="error_ipsec_ike_policy_change"></span>**ERROR\_IPSEC\_IKE\_POLICY\_CHANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-341">13849 (0x3619)</span><span class="sxs-lookup"><span data-stu-id="6415e-341">13849 (0x3619)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-342">Il nuovo criterio è stato invalidato con firma di accesso condiviso con criteri obsoleti.</span><span class="sxs-lookup"><span data-stu-id="6415e-342">New policy invalidated SAs formed with old policy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-343"><span id="ERROR_IPSEC_IKE_NO_MM_POLICY"></span><span id="error_ipsec_ike_no_mm_policy"></span>**\_ \_ criterio IKE errore IPSec \_ No \_ mm \_**</span><span class="sxs-lookup"><span data-stu-id="6415e-343"><span id="ERROR_IPSEC_IKE_NO_MM_POLICY"></span><span id="error_ipsec_ike_no_mm_policy"></span>**ERROR\_IPSEC\_IKE\_NO\_MM\_POLICY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-344">13850 (0x361A)</span><span class="sxs-lookup"><span data-stu-id="6415e-344">13850 (0x361A)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-345">Non sono disponibili criteri IKE in modalità principale.</span><span class="sxs-lookup"><span data-stu-id="6415e-345">There is no available Main Mode IKE policy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-346"><span id="ERROR_IPSEC_IKE_NOTCBPRIV"></span><span id="error_ipsec_ike_notcbpriv"></span>**ERRORE \_ IPSec \_ \_ NOTCBPRIV IKE**</span><span class="sxs-lookup"><span data-stu-id="6415e-346"><span id="ERROR_IPSEC_IKE_NOTCBPRIV"></span><span id="error_ipsec_ike_notcbpriv"></span>**ERROR\_IPSEC\_IKE\_NOTCBPRIV**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-347">13851 (0x361B)</span><span class="sxs-lookup"><span data-stu-id="6415e-347">13851 (0x361B)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-348">Non è stato possibile abilitare il privilegio TCB.</span><span class="sxs-lookup"><span data-stu-id="6415e-348">Failed to enabled TCB privilege.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-349"><span id="ERROR_IPSEC_IKE_SECLOADFAIL"></span><span id="error_ipsec_ike_secloadfail"></span>**ERRORE \_ IPSec \_ \_ SECLOADFAIL IKE**</span><span class="sxs-lookup"><span data-stu-id="6415e-349"><span id="ERROR_IPSEC_IKE_SECLOADFAIL"></span><span id="error_ipsec_ike_secloadfail"></span>**ERROR\_IPSEC\_IKE\_SECLOADFAIL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-350">13852 (0x361C)</span><span class="sxs-lookup"><span data-stu-id="6415e-350">13852 (0x361C)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-351">Non è stato possibile caricare SECURITY.DLL.</span><span class="sxs-lookup"><span data-stu-id="6415e-351">Failed to load SECURITY.DLL.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-352"><span id="ERROR_IPSEC_IKE_FAILSSPINIT"></span><span id="error_ipsec_ike_failsspinit"></span>**ERRORE \_ IPSec \_ \_ FAILSSPINIT IKE**</span><span class="sxs-lookup"><span data-stu-id="6415e-352"><span id="ERROR_IPSEC_IKE_FAILSSPINIT"></span><span id="error_ipsec_ike_failsspinit"></span>**ERROR\_IPSEC\_IKE\_FAILSSPINIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-353">13853 (0x361D)</span><span class="sxs-lookup"><span data-stu-id="6415e-353">13853 (0x361D)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-354">Non è stato possibile ottenere l'indirizzo di invio della tabella della funzione di sicurezza da SSPI.</span><span class="sxs-lookup"><span data-stu-id="6415e-354">Failed to obtain security function table dispatch address from SSPI.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-355"><span id="ERROR_IPSEC_IKE_FAILQUERYSSP"></span><span id="error_ipsec_ike_failqueryssp"></span>**ERRORE \_ IPSec \_ \_ FAILQUERYSSP IKE**</span><span class="sxs-lookup"><span data-stu-id="6415e-355"><span id="ERROR_IPSEC_IKE_FAILQUERYSSP"></span><span id="error_ipsec_ike_failqueryssp"></span>**ERROR\_IPSEC\_IKE\_FAILQUERYSSP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-356">13854 (0x361E)</span><span class="sxs-lookup"><span data-stu-id="6415e-356">13854 (0x361E)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-357">Impossibile eseguire una query sul pacchetto Kerberos per ottenere le dimensioni massime del token.</span><span class="sxs-lookup"><span data-stu-id="6415e-357">Failed to query Kerberos package to obtain max token size.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-358"><span id="ERROR_IPSEC_IKE_SRVACQFAIL"></span><span id="error_ipsec_ike_srvacqfail"></span>**ERRORE \_ IPSec \_ \_ SRVACQFAIL IKE**</span><span class="sxs-lookup"><span data-stu-id="6415e-358"><span id="ERROR_IPSEC_IKE_SRVACQFAIL"></span><span id="error_ipsec_ike_srvacqfail"></span>**ERROR\_IPSEC\_IKE\_SRVACQFAIL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-359">13855 (0x361F)</span><span class="sxs-lookup"><span data-stu-id="6415e-359">13855 (0x361F)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-360">Non è stato possibile ottenere le credenziali del server Kerberos per il servizio IKE ISAKMP/ERROR \_ IPSec \_ .</span><span class="sxs-lookup"><span data-stu-id="6415e-360">Failed to obtain Kerberos server credentials for ISAKMP/ERROR\_IPSEC\_IKE service.</span></span> <span data-ttu-id="6415e-361">L'autenticazione Kerberos non funzionerà.</span><span class="sxs-lookup"><span data-stu-id="6415e-361">Kerberos authentication will not function.</span></span> <span data-ttu-id="6415e-362">La causa più probabile di questo problema è la mancanza di appartenenza al dominio.</span><span class="sxs-lookup"><span data-stu-id="6415e-362">The most likely reason for this is lack of domain membership.</span></span> <span data-ttu-id="6415e-363">Questo comportamento è normale se il computer è membro di un gruppo di lavoro.</span><span class="sxs-lookup"><span data-stu-id="6415e-363">This is normal if your computer is a member of a workgroup.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-364"><span id="ERROR_IPSEC_IKE_SRVQUERYCRED"></span><span id="error_ipsec_ike_srvquerycred"></span>**ERRORE \_ IPSec \_ \_ SRVQUERYCRED IKE**</span><span class="sxs-lookup"><span data-stu-id="6415e-364"><span id="ERROR_IPSEC_IKE_SRVQUERYCRED"></span><span id="error_ipsec_ike_srvquerycred"></span>**ERROR\_IPSEC\_IKE\_SRVQUERYCRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-365">13856 (0x3620)</span><span class="sxs-lookup"><span data-stu-id="6415e-365">13856 (0x3620)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-366">Impossibile determinare il nome dell'entità SSPI per il \_ servizio IKE IPSec/errore \_ ([**QueryCredentialsAttributes**](/windows/win32/api/sspi/nf-sspi-querycredentialsattributesa)).</span><span class="sxs-lookup"><span data-stu-id="6415e-366">Failed to determine SSPI principal name for ISAKMP/ERROR\_IPSEC\_IKE service ([**QueryCredentialsAttributes**](/windows/win32/api/sspi/nf-sspi-querycredentialsattributesa)).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-367"><span id="ERROR_IPSEC_IKE_GETSPIFAIL"></span><span id="error_ipsec_ike_getspifail"></span>**ERRORE \_ IPSec \_ \_ GETSPIFAIL IKE**</span><span class="sxs-lookup"><span data-stu-id="6415e-367"><span id="ERROR_IPSEC_IKE_GETSPIFAIL"></span><span id="error_ipsec_ike_getspifail"></span>**ERROR\_IPSEC\_IKE\_GETSPIFAIL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-368">13857 (0x3621)</span><span class="sxs-lookup"><span data-stu-id="6415e-368">13857 (0x3621)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-369">Non è stato possibile ottenere il nuovo SPI per la SA in ingresso dal driver IPsec.</span><span class="sxs-lookup"><span data-stu-id="6415e-369">Failed to obtain new SPI for the inbound SA from IPsec driver.</span></span> <span data-ttu-id="6415e-370">La ragione più comune è che il driver non dispone del filtro corretto.</span><span class="sxs-lookup"><span data-stu-id="6415e-370">The most common cause for this is that the driver does not have the correct filter.</span></span> <span data-ttu-id="6415e-371">Verificare i criteri per verificare i filtri.</span><span class="sxs-lookup"><span data-stu-id="6415e-371">Check your policy to verify the filters.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-372"><span id="ERROR_IPSEC_IKE_INVALID_FILTER"></span><span id="error_ipsec_ike_invalid_filter"></span>**ERRORE \_ del \_ filtro IKE IPSec \_ non valido \_**</span><span class="sxs-lookup"><span data-stu-id="6415e-372"><span id="ERROR_IPSEC_IKE_INVALID_FILTER"></span><span id="error_ipsec_ike_invalid_filter"></span>**ERROR\_IPSEC\_IKE\_INVALID\_FILTER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-373">13858 (0x3622)</span><span class="sxs-lookup"><span data-stu-id="6415e-373">13858 (0x3622)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-374">Il filtro specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="6415e-374">Given filter is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-375"><span id="ERROR_IPSEC_IKE_OUT_OF_MEMORY"></span><span id="error_ipsec_ike_out_of_memory"></span>**ERRORE \_ \_ \_ \_ di \_ memoria IKE IPSec**</span><span class="sxs-lookup"><span data-stu-id="6415e-375"><span id="ERROR_IPSEC_IKE_OUT_OF_MEMORY"></span><span id="error_ipsec_ike_out_of_memory"></span>**ERROR\_IPSEC\_IKE\_OUT\_OF\_MEMORY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-376">13859 (0x3623)</span><span class="sxs-lookup"><span data-stu-id="6415e-376">13859 (0x3623)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-377">L'allocazione di memoria ha avuto esito negativo.</span><span class="sxs-lookup"><span data-stu-id="6415e-377">Memory allocation failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-378"><span id="ERROR_IPSEC_IKE_ADD_UPDATE_KEY_FAILED"></span><span id="error_ipsec_ike_add_update_key_failed"></span>**ERRORE \_ di \_ aggiunta della chiave di aggiornamento IKE IPSec \_ \_ \_ \_ non riuscita**</span><span class="sxs-lookup"><span data-stu-id="6415e-378"><span id="ERROR_IPSEC_IKE_ADD_UPDATE_KEY_FAILED"></span><span id="error_ipsec_ike_add_update_key_failed"></span>**ERROR\_IPSEC\_IKE\_ADD\_UPDATE\_KEY\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-379">13860 (0x3624)</span><span class="sxs-lookup"><span data-stu-id="6415e-379">13860 (0x3624)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-380">Non è stato possibile aggiungere l'associazione di sicurezza al driver IPsec.</span><span class="sxs-lookup"><span data-stu-id="6415e-380">Failed to add Security Association to IPsec Driver.</span></span> <span data-ttu-id="6415e-381">La ragione più comune è rappresentata dal fatto che la negoziazione IKE ha impiegato troppo tempo per il completamento.</span><span class="sxs-lookup"><span data-stu-id="6415e-381">The most common cause for this is if the IKE negotiation took too long to complete.</span></span> <span data-ttu-id="6415e-382">Se il problema persiste, ridurre il carico sul computer che ha generato l'errore.</span><span class="sxs-lookup"><span data-stu-id="6415e-382">If the problem persists, reduce the load on the faulting machine.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-383"><span id="ERROR_IPSEC_IKE_INVALID_POLICY"></span><span id="error_ipsec_ike_invalid_policy"></span>**ERRORE \_ del \_ criterio IKE IPSec \_ non valido \_**</span><span class="sxs-lookup"><span data-stu-id="6415e-383"><span id="ERROR_IPSEC_IKE_INVALID_POLICY"></span><span id="error_ipsec_ike_invalid_policy"></span>**ERROR\_IPSEC\_IKE\_INVALID\_POLICY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-384">13861 (0x3625)</span><span class="sxs-lookup"><span data-stu-id="6415e-384">13861 (0x3625)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-385">Criterio non valido.</span><span class="sxs-lookup"><span data-stu-id="6415e-385">Invalid policy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-386"><span id="ERROR_IPSEC_IKE_UNKNOWN_DOI"></span><span id="error_ipsec_ike_unknown_doi"></span>**ERRORE \_ IPSec \_ \_ sconosciuto IKE \_**</span><span class="sxs-lookup"><span data-stu-id="6415e-386"><span id="ERROR_IPSEC_IKE_UNKNOWN_DOI"></span><span id="error_ipsec_ike_unknown_doi"></span>**ERROR\_IPSEC\_IKE\_UNKNOWN\_DOI**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-387">13862 (0x3626)</span><span class="sxs-lookup"><span data-stu-id="6415e-387">13862 (0x3626)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-388">DOI non valido.</span><span class="sxs-lookup"><span data-stu-id="6415e-388">Invalid DOI.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-389"><span id="ERROR_IPSEC_IKE_INVALID_SITUATION"></span><span id="error_ipsec_ike_invalid_situation"></span>**situazione di errore \_ \_ IKE IPSec \_ non valida \_**</span><span class="sxs-lookup"><span data-stu-id="6415e-389"><span id="ERROR_IPSEC_IKE_INVALID_SITUATION"></span><span id="error_ipsec_ike_invalid_situation"></span>**ERROR\_IPSEC\_IKE\_INVALID\_SITUATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-390">13863 (0x3627)</span><span class="sxs-lookup"><span data-stu-id="6415e-390">13863 (0x3627)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-391">Situazione non valida.</span><span class="sxs-lookup"><span data-stu-id="6415e-391">Invalid situation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-392"><span id="ERROR_IPSEC_IKE_DH_FAILURE"></span><span id="error_ipsec_ike_dh_failure"></span>**errore \_ errore \_ DH IKE IPSec \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6415e-392"><span id="ERROR_IPSEC_IKE_DH_FAILURE"></span><span id="error_ipsec_ike_dh_failure"></span>**ERROR\_IPSEC\_IKE\_DH\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-393">13864 (0x3628)</span><span class="sxs-lookup"><span data-stu-id="6415e-393">13864 (0x3628)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-394">Errore Diffie-Hellman.</span><span class="sxs-lookup"><span data-stu-id="6415e-394">Diffie-Hellman failure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-395"><span id="ERROR_IPSEC_IKE_INVALID_GROUP"></span><span id="error_ipsec_ike_invalid_group"></span>**ERRORE \_ del \_ gruppo IKE IPSec \_ non valido \_**</span><span class="sxs-lookup"><span data-stu-id="6415e-395"><span id="ERROR_IPSEC_IKE_INVALID_GROUP"></span><span id="error_ipsec_ike_invalid_group"></span>**ERROR\_IPSEC\_IKE\_INVALID\_GROUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-396">13865 (0x3629)</span><span class="sxs-lookup"><span data-stu-id="6415e-396">13865 (0x3629)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-397">Gruppo di Diffie-Hellman non valido.</span><span class="sxs-lookup"><span data-stu-id="6415e-397">Invalid Diffie-Hellman group.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-398"><span id="ERROR_IPSEC_IKE_ENCRYPT"></span><span id="error_ipsec_ike_encrypt"></span>**ERRORE \_ di \_ crittografia IKE IPSec \_**</span><span class="sxs-lookup"><span data-stu-id="6415e-398"><span id="ERROR_IPSEC_IKE_ENCRYPT"></span><span id="error_ipsec_ike_encrypt"></span>**ERROR\_IPSEC\_IKE\_ENCRYPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-399">13866 (0x362A)</span><span class="sxs-lookup"><span data-stu-id="6415e-399">13866 (0x362A)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-400">Errore durante la crittografia del payload.</span><span class="sxs-lookup"><span data-stu-id="6415e-400">Error encrypting payload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-401"><span id="ERROR_IPSEC_IKE_DECRYPT"></span><span id="error_ipsec_ike_decrypt"></span>**ERRORE \_ di \_ \_ decrittografia IKE IPSec**</span><span class="sxs-lookup"><span data-stu-id="6415e-401"><span id="ERROR_IPSEC_IKE_DECRYPT"></span><span id="error_ipsec_ike_decrypt"></span>**ERROR\_IPSEC\_IKE\_DECRYPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-402">13867 (0x362B)</span><span class="sxs-lookup"><span data-stu-id="6415e-402">13867 (0x362B)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-403">Errore durante la decrittografia del payload.</span><span class="sxs-lookup"><span data-stu-id="6415e-403">Error decrypting payload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-404"><span id="ERROR_IPSEC_IKE_POLICY_MATCH"></span><span id="error_ipsec_ike_policy_match"></span>**ERRORE \_ \_ criterio IKE \_ IPSec \_ corrispondente**</span><span class="sxs-lookup"><span data-stu-id="6415e-404"><span id="ERROR_IPSEC_IKE_POLICY_MATCH"></span><span id="error_ipsec_ike_policy_match"></span>**ERROR\_IPSEC\_IKE\_POLICY\_MATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-405">13868 (0x362C)</span><span class="sxs-lookup"><span data-stu-id="6415e-405">13868 (0x362C)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-406">Errore di corrispondenza dei criteri.</span><span class="sxs-lookup"><span data-stu-id="6415e-406">Policy match error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-407"><span id="ERROR_IPSEC_IKE_UNSUPPORTED_ID"></span><span id="error_ipsec_ike_unsupported_id"></span>**ERRORE \_ di \_ ID IKE IPSec non \_ supportato \_**</span><span class="sxs-lookup"><span data-stu-id="6415e-407"><span id="ERROR_IPSEC_IKE_UNSUPPORTED_ID"></span><span id="error_ipsec_ike_unsupported_id"></span>**ERROR\_IPSEC\_IKE\_UNSUPPORTED\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-408">13869 (0x362D)</span><span class="sxs-lookup"><span data-stu-id="6415e-408">13869 (0x362D)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-409">ID non supportato.</span><span class="sxs-lookup"><span data-stu-id="6415e-409">Unsupported ID.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-410"><span id="ERROR_IPSEC_IKE_INVALID_HASH"></span><span id="error_ipsec_ike_invalid_hash"></span>**ERRORE \_ di \_ \_ hash IKE non valido \_**</span><span class="sxs-lookup"><span data-stu-id="6415e-410"><span id="ERROR_IPSEC_IKE_INVALID_HASH"></span><span id="error_ipsec_ike_invalid_hash"></span>**ERROR\_IPSEC\_IKE\_INVALID\_HASH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-411">13870 (0x362E)</span><span class="sxs-lookup"><span data-stu-id="6415e-411">13870 (0x362E)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-412">Verifica hash non riuscita.</span><span class="sxs-lookup"><span data-stu-id="6415e-412">Hash verification failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-413"><span id="ERROR_IPSEC_IKE_INVALID_HASH_ALG"></span><span id="error_ipsec_ike_invalid_hash_alg"></span>**ERRORE \_ dell' \_ \_ \_ hash ALG non \_ valido per IPSec**</span><span class="sxs-lookup"><span data-stu-id="6415e-413"><span id="ERROR_IPSEC_IKE_INVALID_HASH_ALG"></span><span id="error_ipsec_ike_invalid_hash_alg"></span>**ERROR\_IPSEC\_IKE\_INVALID\_HASH\_ALG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-414">13871 (0x362F)</span><span class="sxs-lookup"><span data-stu-id="6415e-414">13871 (0x362F)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-415">Algoritmo hash non valido.</span><span class="sxs-lookup"><span data-stu-id="6415e-415">Invalid hash algorithm.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-416"><span id="ERROR_IPSEC_IKE_INVALID_HASH_SIZE"></span><span id="error_ipsec_ike_invalid_hash_size"></span>**ERRORE \_ della \_ dimensione hash IKE IPSec \_ non valida \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6415e-416"><span id="ERROR_IPSEC_IKE_INVALID_HASH_SIZE"></span><span id="error_ipsec_ike_invalid_hash_size"></span>**ERROR\_IPSEC\_IKE\_INVALID\_HASH\_SIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-417">13872 (0x3630)</span><span class="sxs-lookup"><span data-stu-id="6415e-417">13872 (0x3630)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-418">Dimensioni hash non valide.</span><span class="sxs-lookup"><span data-stu-id="6415e-418">Invalid hash size.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-419"><span id="ERROR_IPSEC_IKE_INVALID_ENCRYPT_ALG"></span><span id="error_ipsec_ike_invalid_encrypt_alg"></span>**ERRORE \_ \_ IKE IPSec \_ non valido \_ crittografare \_ ALG**</span><span class="sxs-lookup"><span data-stu-id="6415e-419"><span id="ERROR_IPSEC_IKE_INVALID_ENCRYPT_ALG"></span><span id="error_ipsec_ike_invalid_encrypt_alg"></span>**ERROR\_IPSEC\_IKE\_INVALID\_ENCRYPT\_ALG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-420">13873 (0x3631)</span><span class="sxs-lookup"><span data-stu-id="6415e-420">13873 (0x3631)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-421">Algoritmo di crittografia non valido.</span><span class="sxs-lookup"><span data-stu-id="6415e-421">Invalid encryption algorithm.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-422"><span id="ERROR_IPSEC_IKE_INVALID_AUTH_ALG"></span><span id="error_ipsec_ike_invalid_auth_alg"></span>**ERRORE \_ \_ AUTH IPSec \_ non \_ valido \_**</span><span class="sxs-lookup"><span data-stu-id="6415e-422"><span id="ERROR_IPSEC_IKE_INVALID_AUTH_ALG"></span><span id="error_ipsec_ike_invalid_auth_alg"></span>**ERROR\_IPSEC\_IKE\_INVALID\_AUTH\_ALG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-423">13874 (0x3632)</span><span class="sxs-lookup"><span data-stu-id="6415e-423">13874 (0x3632)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-424">Algoritmo di autenticazione non valido.</span><span class="sxs-lookup"><span data-stu-id="6415e-424">Invalid authentication algorithm.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-425"><span id="ERROR_IPSEC_IKE_INVALID_SIG"></span><span id="error_ipsec_ike_invalid_sig"></span>**ERRORE \_ del \_ sig IPSec IKE \_ non valido \_**</span><span class="sxs-lookup"><span data-stu-id="6415e-425"><span id="ERROR_IPSEC_IKE_INVALID_SIG"></span><span id="error_ipsec_ike_invalid_sig"></span>**ERROR\_IPSEC\_IKE\_INVALID\_SIG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-426">13875 (0x3633)</span><span class="sxs-lookup"><span data-stu-id="6415e-426">13875 (0x3633)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-427">Firma del certificato non valida.</span><span class="sxs-lookup"><span data-stu-id="6415e-427">Invalid certificate signature.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-428"><span id="ERROR_IPSEC_IKE_LOAD_FAILED"></span><span id="error_ipsec_ike_load_failed"></span>**ERRORE \_ di \_ caricamento IKE IPSec \_ \_ non riuscito**</span><span class="sxs-lookup"><span data-stu-id="6415e-428"><span id="ERROR_IPSEC_IKE_LOAD_FAILED"></span><span id="error_ipsec_ike_load_failed"></span>**ERROR\_IPSEC\_IKE\_LOAD\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-429">13876 (0x3634)</span><span class="sxs-lookup"><span data-stu-id="6415e-429">13876 (0x3634)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-430">Il caricamento non è riuscito.</span><span class="sxs-lookup"><span data-stu-id="6415e-430">Load failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-431"><span id="ERROR_IPSEC_IKE_RPC_DELETE"></span><span id="error_ipsec_ike_rpc_delete"></span>**ERRORE \_ IPSec \_ IKE \_ \_ Delete RPC**</span><span class="sxs-lookup"><span data-stu-id="6415e-431"><span id="ERROR_IPSEC_IKE_RPC_DELETE"></span><span id="error_ipsec_ike_rpc_delete"></span>**ERROR\_IPSEC\_IKE\_RPC\_DELETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-432">13877 (0x3635)</span><span class="sxs-lookup"><span data-stu-id="6415e-432">13877 (0x3635)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-433">Eliminato tramite la chiamata RPC.</span><span class="sxs-lookup"><span data-stu-id="6415e-433">Deleted via RPC call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-434"><span id="ERROR_IPSEC_IKE_BENIGN_REINIT"></span><span id="error_ipsec_ike_benign_reinit"></span>**ERRORE \_ IPSec \_ IKE \_ BENIGNo \_ reinit**</span><span class="sxs-lookup"><span data-stu-id="6415e-434"><span id="ERROR_IPSEC_IKE_BENIGN_REINIT"></span><span id="error_ipsec_ike_benign_reinit"></span>**ERROR\_IPSEC\_IKE\_BENIGN\_REINIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-435">13878 (0x3636)</span><span class="sxs-lookup"><span data-stu-id="6415e-435">13878 (0x3636)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-436">Stato temporaneo creato per eseguire la reinizializzazione.</span><span class="sxs-lookup"><span data-stu-id="6415e-436">Temporary state created to perform reinitialization.</span></span> <span data-ttu-id="6415e-437">Non si tratta di un errore reale.</span><span class="sxs-lookup"><span data-stu-id="6415e-437">This is not a real failure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-438"><span id="ERROR_IPSEC_IKE_INVALID_RESPONDER_LIFETIME_NOTIFY"></span><span id="error_ipsec_ike_invalid_responder_lifetime_notify"></span>**ERRORE \_ di \_ \_ notifica della \_ durata del risponditore IKE IPSec non valido \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6415e-438"><span id="ERROR_IPSEC_IKE_INVALID_RESPONDER_LIFETIME_NOTIFY"></span><span id="error_ipsec_ike_invalid_responder_lifetime_notify"></span>**ERROR\_IPSEC\_IKE\_INVALID\_RESPONDER\_LIFETIME\_NOTIFY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-439">13879 (0x3637)</span><span class="sxs-lookup"><span data-stu-id="6415e-439">13879 (0x3637)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-440">Il valore di durata ricevuto nella notifica di durata del risponditore è inferiore al valore minimo di Windows 2000 configurato.</span><span class="sxs-lookup"><span data-stu-id="6415e-440">The lifetime value received in the Responder Lifetime Notify is below the Windows 2000 configured minimum value.</span></span> <span data-ttu-id="6415e-441">Correggere i criteri nel computer peer.</span><span class="sxs-lookup"><span data-stu-id="6415e-441">Please fix the policy on the peer machine.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-442"><span id="ERROR_IPSEC_IKE_INVALID_MAJOR_VERSION"></span><span id="error_ipsec_ike_invalid_major_version"></span>**ERRORE \_ della \_ \_ \_ versione principale IKE non valida IPSec \_**</span><span class="sxs-lookup"><span data-stu-id="6415e-442"><span id="ERROR_IPSEC_IKE_INVALID_MAJOR_VERSION"></span><span id="error_ipsec_ike_invalid_major_version"></span>**ERROR\_IPSEC\_IKE\_INVALID\_MAJOR\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-443">13880 (0x3638)</span><span class="sxs-lookup"><span data-stu-id="6415e-443">13880 (0x3638)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-444">Il destinatario non è in grado di gestire la versione di IKE specificata nell'intestazione.</span><span class="sxs-lookup"><span data-stu-id="6415e-444">The recipient cannot handle version of IKE specified in the header.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-445"><span id="ERROR_IPSEC_IKE_INVALID_CERT_KEYLEN"></span><span id="error_ipsec_ike_invalid_cert_keylen"></span>**ERRORE \_ IPSec \_ IKE \_ non \_ valido \_ KEYLEN**</span><span class="sxs-lookup"><span data-stu-id="6415e-445"><span id="ERROR_IPSEC_IKE_INVALID_CERT_KEYLEN"></span><span id="error_ipsec_ike_invalid_cert_keylen"></span>**ERROR\_IPSEC\_IKE\_INVALID\_CERT\_KEYLEN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-446">13881 (0x3639)</span><span class="sxs-lookup"><span data-stu-id="6415e-446">13881 (0x3639)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-447">La lunghezza della chiave nel certificato è troppo piccola per i requisiti di sicurezza configurati.</span><span class="sxs-lookup"><span data-stu-id="6415e-447">Key length in certificate is too small for configured security requirements.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-448"><span id="ERROR_IPSEC_IKE_MM_LIMIT"></span><span id="error_ipsec_ike_mm_limit"></span>**limite di errore \_ IKE per IPSec \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6415e-448"><span id="ERROR_IPSEC_IKE_MM_LIMIT"></span><span id="error_ipsec_ike_mm_limit"></span>**ERROR\_IPSEC\_IKE\_MM\_LIMIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-449">13882 (0x363A)</span><span class="sxs-lookup"><span data-stu-id="6415e-449">13882 (0x363A)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-450">Superato il numero massimo di SAs MM stabilite al peer.</span><span class="sxs-lookup"><span data-stu-id="6415e-450">Max number of established MM SAs to peer exceeded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-451"><span id="ERROR_IPSEC_IKE_NEGOTIATION_DISABLED"></span><span id="error_ipsec_ike_negotiation_disabled"></span>**ERRORE \_ di \_ negoziazione IKE IPSec \_ \_ disabilitato**</span><span class="sxs-lookup"><span data-stu-id="6415e-451"><span id="ERROR_IPSEC_IKE_NEGOTIATION_DISABLED"></span><span id="error_ipsec_ike_negotiation_disabled"></span>**ERROR\_IPSEC\_IKE\_NEGOTIATION\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-452">13883 (0x363B)</span><span class="sxs-lookup"><span data-stu-id="6415e-452">13883 (0x363B)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-453">IKE ha ricevuto un criterio che disabilita la negoziazione.</span><span class="sxs-lookup"><span data-stu-id="6415e-453">IKE received a policy that disables negotiation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-454"><span id="ERROR_IPSEC_IKE_QM_LIMIT"></span><span id="error_ipsec_ike_qm_limit"></span>**limite per l'errore \_ IPSec \_ IKE \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6415e-454"><span id="ERROR_IPSEC_IKE_QM_LIMIT"></span><span id="error_ipsec_ike_qm_limit"></span>**ERROR\_IPSEC\_IKE\_QM\_LIMIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-455">13884 (0x363C)</span><span class="sxs-lookup"><span data-stu-id="6415e-455">13884 (0x363C)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-456">È stato raggiunto il limite massimo della modalità rapida per la modalità principale.</span><span class="sxs-lookup"><span data-stu-id="6415e-456">Reached maximum quick mode limit for the main mode.</span></span> <span data-ttu-id="6415e-457">Verrà avviata la nuova modalità principale.</span><span class="sxs-lookup"><span data-stu-id="6415e-457">New main mode will be started.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-458"><span id="ERROR_IPSEC_IKE_MM_EXPIRED"></span><span id="error_ipsec_ike_mm_expired"></span>**ERRORE \_ IPSec \_ IKE \_ mm \_ scaduto**</span><span class="sxs-lookup"><span data-stu-id="6415e-458"><span id="ERROR_IPSEC_IKE_MM_EXPIRED"></span><span id="error_ipsec_ike_mm_expired"></span>**ERROR\_IPSEC\_IKE\_MM\_EXPIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-459">13885 (0x363D)</span><span class="sxs-lookup"><span data-stu-id="6415e-459">13885 (0x363D)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-460">Durata SA della modalità principale scaduta o peer inviato un'eliminazione in modalità principale.</span><span class="sxs-lookup"><span data-stu-id="6415e-460">Main mode SA lifetime expired or peer sent a main mode delete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-461"><span id="ERROR_IPSEC_IKE_PEER_MM_ASSUMED_INVALID"></span><span id="error_ipsec_ike_peer_mm_assumed_invalid"></span>**errore \_ del \_ peer IKE IPSec \_ \_ \_ in \_ errore**</span><span class="sxs-lookup"><span data-stu-id="6415e-461"><span id="ERROR_IPSEC_IKE_PEER_MM_ASSUMED_INVALID"></span><span id="error_ipsec_ike_peer_mm_assumed_invalid"></span>**ERROR\_IPSEC\_IKE\_PEER\_MM\_ASSUMED\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-462">13886 (0x363E)</span><span class="sxs-lookup"><span data-stu-id="6415e-462">13886 (0x363E)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-463">Si presuppone che l'associazione di modalità principale non sia valida perché il peer ha smesso di rispondere.</span><span class="sxs-lookup"><span data-stu-id="6415e-463">Main mode SA assumed to be invalid because peer stopped responding.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-464"><span id="ERROR_IPSEC_IKE_CERT_CHAIN_POLICY_MISMATCH"></span><span id="error_ipsec_ike_cert_chain_policy_mismatch"></span>**ERRORE \_ di \_ criteri catena di certificati IKE IPSec non \_ \_ \_ \_ corrispondenti**</span><span class="sxs-lookup"><span data-stu-id="6415e-464"><span id="ERROR_IPSEC_IKE_CERT_CHAIN_POLICY_MISMATCH"></span><span id="error_ipsec_ike_cert_chain_policy_mismatch"></span>**ERROR\_IPSEC\_IKE\_CERT\_CHAIN\_POLICY\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-465">13887 (0x363F)</span><span class="sxs-lookup"><span data-stu-id="6415e-465">13887 (0x363F)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-466">Il certificato non viene concatenato a una radice attendibile nei criteri IPsec.</span><span class="sxs-lookup"><span data-stu-id="6415e-466">Certificate doesn't chain to a trusted root in IPsec policy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-467"><span id="ERROR_IPSEC_IKE_UNEXPECTED_MESSAGE_ID"></span><span id="error_ipsec_ike_unexpected_message_id"></span>**ERRORE \_ \_ \_ ID messaggio imprevisto IKE IPSec \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6415e-467"><span id="ERROR_IPSEC_IKE_UNEXPECTED_MESSAGE_ID"></span><span id="error_ipsec_ike_unexpected_message_id"></span>**ERROR\_IPSEC\_IKE\_UNEXPECTED\_MESSAGE\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-468">13888 (0x3640)</span><span class="sxs-lookup"><span data-stu-id="6415e-468">13888 (0x3640)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-469">ID messaggio imprevisto ricevuto.</span><span class="sxs-lookup"><span data-stu-id="6415e-469">Received unexpected message ID.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-470"><span id="ERROR_IPSEC_IKE_INVALID_AUTH_PAYLOAD"></span><span id="error_ipsec_ike_invalid_auth_payload"></span>**ERRORE \_ IPSec \_ IKE \_ non \_ valido \_ payload di autenticazione**</span><span class="sxs-lookup"><span data-stu-id="6415e-470"><span id="ERROR_IPSEC_IKE_INVALID_AUTH_PAYLOAD"></span><span id="error_ipsec_ike_invalid_auth_payload"></span>**ERROR\_IPSEC\_IKE\_INVALID\_AUTH\_PAYLOAD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-471">13889 (0x3641)</span><span class="sxs-lookup"><span data-stu-id="6415e-471">13889 (0x3641)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-472">Sono state ricevute offerte di autenticazione non valide.</span><span class="sxs-lookup"><span data-stu-id="6415e-472">Received invalid authentication offers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-473"><span id="ERROR_IPSEC_IKE_DOS_COOKIE_SENT"></span><span id="error_ipsec_ike_dos_cookie_sent"></span>**ERRORE \_ del \_ \_ cookie DOS IKE IPSec \_ \_ inviato**</span><span class="sxs-lookup"><span data-stu-id="6415e-473"><span id="ERROR_IPSEC_IKE_DOS_COOKIE_SENT"></span><span id="error_ipsec_ike_dos_cookie_sent"></span>**ERROR\_IPSEC\_IKE\_DOS\_COOKIE\_SENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-474">13890 (0x3642)</span><span class="sxs-lookup"><span data-stu-id="6415e-474">13890 (0x3642)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-475">Notifica del cookie DoS inviata all'initiator.</span><span class="sxs-lookup"><span data-stu-id="6415e-475">Sent DoS cookie notify to initiator.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-476"><span id="ERROR_IPSEC_IKE_SHUTTING_DOWN"></span><span id="error_ipsec_ike_shutting_down"></span>**ERRORE \_ di \_ \_ arresto IKE IPSec \_**</span><span class="sxs-lookup"><span data-stu-id="6415e-476"><span id="ERROR_IPSEC_IKE_SHUTTING_DOWN"></span><span id="error_ipsec_ike_shutting_down"></span>**ERROR\_IPSEC\_IKE\_SHUTTING\_DOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-477">13891 (0x3643)</span><span class="sxs-lookup"><span data-stu-id="6415e-477">13891 (0x3643)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-478">Arresto del servizio IKE in corso.</span><span class="sxs-lookup"><span data-stu-id="6415e-478">IKE service is shutting down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-479"><span id="ERROR_IPSEC_IKE_CGA_AUTH_FAILED"></span><span id="error_ipsec_ike_cga_auth_failed"></span>**ERRORE \_ di \_ autenticazione di IKE CGA per IPSec \_ \_ \_ non riuscita**</span><span class="sxs-lookup"><span data-stu-id="6415e-479"><span id="ERROR_IPSEC_IKE_CGA_AUTH_FAILED"></span><span id="error_ipsec_ike_cga_auth_failed"></span>**ERROR\_IPSEC\_IKE\_CGA\_AUTH\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-480">13892 (0x3644)</span><span class="sxs-lookup"><span data-stu-id="6415e-480">13892 (0x3644)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-481">Impossibile verificare l'associazione tra l'indirizzo CGA e il certificato.</span><span class="sxs-lookup"><span data-stu-id="6415e-481">Could not verify binding between CGA address and certificate.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-482"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_NATOA"></span><span id="error_ipsec_ike_process_err_natoa"></span>**ERRORE \_ \_ processo IKE \_ IPSec \_ Err \_ Nato**</span><span class="sxs-lookup"><span data-stu-id="6415e-482"><span id="ERROR_IPSEC_IKE_PROCESS_ERR_NATOA"></span><span id="error_ipsec_ike_process_err_natoa"></span>**ERROR\_IPSEC\_IKE\_PROCESS\_ERR\_NATOA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-483">13893 (0x3645)</span><span class="sxs-lookup"><span data-stu-id="6415e-483">13893 (0x3645)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-484">Errore durante l'elaborazione del payload NatO.</span><span class="sxs-lookup"><span data-stu-id="6415e-484">Error processing NatOA payload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-485"><span id="ERROR_IPSEC_IKE_INVALID_MM_FOR_QM"></span><span id="error_ipsec_ike_invalid_mm_for_qm"></span>**ERRORE \_ \_ IKE IPSec \_ non valido \_ mm \_ per \_ QM**</span><span class="sxs-lookup"><span data-stu-id="6415e-485"><span id="ERROR_IPSEC_IKE_INVALID_MM_FOR_QM"></span><span id="error_ipsec_ike_invalid_mm_for_qm"></span>**ERROR\_IPSEC\_IKE\_INVALID\_MM\_FOR\_QM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-486">13894 (0x3646)</span><span class="sxs-lookup"><span data-stu-id="6415e-486">13894 (0x3646)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-487">I parametri della modalità principale non sono validi per questa modalità rapida.</span><span class="sxs-lookup"><span data-stu-id="6415e-487">Parameters of the main mode are invalid for this quick mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-488"><span id="ERROR_IPSEC_IKE_QM_EXPIRED"></span><span id="error_ipsec_ike_qm_expired"></span>**errore per IPSec di IKE per errore \_ \_ \_ \_ scaduto**</span><span class="sxs-lookup"><span data-stu-id="6415e-488"><span id="ERROR_IPSEC_IKE_QM_EXPIRED"></span><span id="error_ipsec_ike_qm_expired"></span>**ERROR\_IPSEC\_IKE\_QM\_EXPIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-489">13895 (0x3647)</span><span class="sxs-lookup"><span data-stu-id="6415e-489">13895 (0x3647)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-490">La modalità rapida SA è scaduta dal driver IPsec.</span><span class="sxs-lookup"><span data-stu-id="6415e-490">Quick mode SA was expired by IPsec driver.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-491"><span id="ERROR_IPSEC_IKE_TOO_MANY_FILTERS"></span><span id="error_ipsec_ike_too_many_filters"></span>**ERRORI \_ di \_ IKE IPSec \_ troppi \_ \_ filtri**</span><span class="sxs-lookup"><span data-stu-id="6415e-491"><span id="ERROR_IPSEC_IKE_TOO_MANY_FILTERS"></span><span id="error_ipsec_ike_too_many_filters"></span>**ERROR\_IPSEC\_IKE\_TOO\_MANY\_FILTERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-492">13896 (0x3648)</span><span class="sxs-lookup"><span data-stu-id="6415e-492">13896 (0x3648)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-493">Sono stati rilevati troppi filtri IKEEXT aggiunti dinamicamente.</span><span class="sxs-lookup"><span data-stu-id="6415e-493">Too many dynamically added IKEEXT filters were detected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-494"><span id="ERROR_IPSEC_IKE_NEG_STATUS_END"></span><span id="error_ipsec_ike_neg_status_end"></span>**ERRORE \_ di \_ stato neg IPSec IKE- \_ \_ \_ fine**</span><span class="sxs-lookup"><span data-stu-id="6415e-494"><span id="ERROR_IPSEC_IKE_NEG_STATUS_END"></span><span id="error_ipsec_ike_neg_status_end"></span>**ERROR\_IPSEC\_IKE\_NEG\_STATUS\_END**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-495">13897 (0x3649)</span><span class="sxs-lookup"><span data-stu-id="6415e-495">13897 (0x3649)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-496">ERRORE \_ di \_ stato neg IPSec IKE- \_ \_ \_ fine</span><span class="sxs-lookup"><span data-stu-id="6415e-496">ERROR\_IPSEC\_IKE\_NEG\_STATUS\_END</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-497"><span id="ERROR_IPSEC_IKE_KILL_DUMMY_NAP_TUNNEL"></span><span id="error_ipsec_ike_kill_dummy_nap_tunnel"></span>**ERRORE \_ di \_ IPSec \_ Killing \_ \_ NAP del \_ tunnel**</span><span class="sxs-lookup"><span data-stu-id="6415e-497"><span id="ERROR_IPSEC_IKE_KILL_DUMMY_NAP_TUNNEL"></span><span id="error_ipsec_ike_kill_dummy_nap_tunnel"></span>**ERROR\_IPSEC\_IKE\_KILL\_DUMMY\_NAP\_TUNNEL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-498">13898 (0x364A)</span><span class="sxs-lookup"><span data-stu-id="6415e-498">13898 (0x364A)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-499">La riautenticazione NAP è stata completata ed è necessario eliminare il tunnel IKEv2 del NAP fittizio.</span><span class="sxs-lookup"><span data-stu-id="6415e-499">NAP reauth succeeded and must delete the dummy NAP IKEv2 tunnel.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-500"><span id="ERROR_IPSEC_IKE_INNER_IP_ASSIGNMENT_FAILURE"></span><span id="error_ipsec_ike_inner_ip_assignment_failure"></span>**errore \_ di \_ \_ \_ assegnazione IP interno \_ IKE errore IPSec \_**</span><span class="sxs-lookup"><span data-stu-id="6415e-500"><span id="ERROR_IPSEC_IKE_INNER_IP_ASSIGNMENT_FAILURE"></span><span id="error_ipsec_ike_inner_ip_assignment_failure"></span>**ERROR\_IPSEC\_IKE\_INNER\_IP\_ASSIGNMENT\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-501">13899 (0x364B)</span><span class="sxs-lookup"><span data-stu-id="6415e-501">13899 (0x364B)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-502">Errore durante l'assegnazione dell'indirizzo IP interno all'initiator in modalità tunnel.</span><span class="sxs-lookup"><span data-stu-id="6415e-502">Error in assigning inner IP address to initiator in tunnel mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-503"><span id="ERROR_IPSEC_IKE_REQUIRE_CP_PAYLOAD_MISSING"></span><span id="error_ipsec_ike_require_cp_payload_missing"></span>**ERRORE \_ IKE IPSec che \_ \_ richiede il \_ \_ payload CP \_ mancante**</span><span class="sxs-lookup"><span data-stu-id="6415e-503"><span id="ERROR_IPSEC_IKE_REQUIRE_CP_PAYLOAD_MISSING"></span><span id="error_ipsec_ike_require_cp_payload_missing"></span>**ERROR\_IPSEC\_IKE\_REQUIRE\_CP\_PAYLOAD\_MISSING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-504">13900 (0x364C)</span><span class="sxs-lookup"><span data-stu-id="6415e-504">13900 (0x364C)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-505">Richiede il payload della configurazione mancante.</span><span class="sxs-lookup"><span data-stu-id="6415e-505">Require configuration payload missing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-506"><span id="ERROR_IPSEC_KEY_MODULE_IMPERSONATION_NEGOTIATION_PENDING"></span><span id="error_ipsec_key_module_impersonation_negotiation_pending"></span>**ERRORE \_ di \_ negoziazione della rappresentazione del modulo della chiave IPsec \_ \_ \_ \_ in sospeso**</span><span class="sxs-lookup"><span data-stu-id="6415e-506"><span id="ERROR_IPSEC_KEY_MODULE_IMPERSONATION_NEGOTIATION_PENDING"></span><span id="error_ipsec_key_module_impersonation_negotiation_pending"></span>**ERROR\_IPSEC\_KEY\_MODULE\_IMPERSONATION\_NEGOTIATION\_PENDING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-507">13901 (0x364D)</span><span class="sxs-lookup"><span data-stu-id="6415e-507">13901 (0x364D)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-508">Una negoziazione eseguita come principio di sicurezza che ha emesso la connessione è in corso.</span><span class="sxs-lookup"><span data-stu-id="6415e-508">A negotiation running as the security principle who issued the connection is in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-509"><span id="ERROR_IPSEC_IKE_COEXISTENCE_SUPPRESS"></span><span id="error_ipsec_ike_coexistence_suppress"></span>**ERRORE \_ di \_ \_ coesistenza IKE IPSec \_**</span><span class="sxs-lookup"><span data-stu-id="6415e-509"><span id="ERROR_IPSEC_IKE_COEXISTENCE_SUPPRESS"></span><span id="error_ipsec_ike_coexistence_suppress"></span>**ERROR\_IPSEC\_IKE\_COEXISTENCE\_SUPPRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-510">13902 (0x364E)</span><span class="sxs-lookup"><span data-stu-id="6415e-510">13902 (0x364E)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-511">Il SA è stato eliminato a causa di una coesistenza IKEv1/AuthIP non è possibile verificare.</span><span class="sxs-lookup"><span data-stu-id="6415e-511">SA was deleted due to IKEv1/AuthIP co-existence suppress check.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-512"><span id="ERROR_IPSEC_IKE_RATELIMIT_DROP"></span><span id="error_ipsec_ike_ratelimit_drop"></span>**ERRORE \_ \_ \_ eliminazione RATELIMIT IKE \_ IPSec**</span><span class="sxs-lookup"><span data-stu-id="6415e-512"><span id="ERROR_IPSEC_IKE_RATELIMIT_DROP"></span><span id="error_ipsec_ike_ratelimit_drop"></span>**ERROR\_IPSEC\_IKE\_RATELIMIT\_DROP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-513">13903 (0x364F)</span><span class="sxs-lookup"><span data-stu-id="6415e-513">13903 (0x364F)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-514">La richiesta SA in ingresso è stata eliminata a causa della limitazione della frequenza degli indirizzi IP peer.</span><span class="sxs-lookup"><span data-stu-id="6415e-514">Incoming SA request was dropped due to peer IP address rate limiting.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-515"><span id="ERROR_IPSEC_IKE_PEER_DOESNT_SUPPORT_MOBIKE"></span><span id="error_ipsec_ike_peer_doesnt_support_mobike"></span>**ERRORE \_ il \_ peer IKE IPSec non \_ \_ \_ supporta \_ MOBIKE**</span><span class="sxs-lookup"><span data-stu-id="6415e-515"><span id="ERROR_IPSEC_IKE_PEER_DOESNT_SUPPORT_MOBIKE"></span><span id="error_ipsec_ike_peer_doesnt_support_mobike"></span>**ERROR\_IPSEC\_IKE\_PEER\_DOESNT\_SUPPORT\_MOBIKE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-516">13904 (0x3650)</span><span class="sxs-lookup"><span data-stu-id="6415e-516">13904 (0x3650)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-517">Il peer non supporta MOBIKE.</span><span class="sxs-lookup"><span data-stu-id="6415e-517">Peer does not support MOBIKE.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-518"><span id="ERROR_IPSEC_IKE_AUTHORIZATION_FAILURE"></span><span id="error_ipsec_ike_authorization_failure"></span>**ERRORE \_ di \_ autorizzazione IKE IPSec \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6415e-518"><span id="ERROR_IPSEC_IKE_AUTHORIZATION_FAILURE"></span><span id="error_ipsec_ike_authorization_failure"></span>**ERROR\_IPSEC\_IKE\_AUTHORIZATION\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-519">13905 (0x3651)</span><span class="sxs-lookup"><span data-stu-id="6415e-519">13905 (0x3651)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-520">Associazione di sicurezza non autorizzata.</span><span class="sxs-lookup"><span data-stu-id="6415e-520">SA establishment is not authorized.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-521"><span id="ERROR_IPSEC_IKE_STRONG_CRED_AUTHORIZATION_FAILURE"></span><span id="error_ipsec_ike_strong_cred_authorization_failure"></span>**ERRORE \_ di \_ \_ \_ autorizzazione creda \_ IKE con errore \_ IPSec**</span><span class="sxs-lookup"><span data-stu-id="6415e-521"><span id="ERROR_IPSEC_IKE_STRONG_CRED_AUTHORIZATION_FAILURE"></span><span id="error_ipsec_ike_strong_cred_authorization_failure"></span>**ERROR\_IPSEC\_IKE\_STRONG\_CRED\_AUTHORIZATION\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-522">13906 (0x3652)</span><span class="sxs-lookup"><span data-stu-id="6415e-522">13906 (0x3652)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-523">Lo stabilimento SA non è autorizzato perché non sono presenti credenziali basate su PKINIT sufficientemente complesse.</span><span class="sxs-lookup"><span data-stu-id="6415e-523">SA establishment is not authorized because there is not a sufficiently strong PKINIT-based credential.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-524"><span id="ERROR_IPSEC_IKE_AUTHORIZATION_FAILURE_WITH_OPTIONAL_RETRY"></span><span id="error_ipsec_ike_authorization_failure_with_optional_retry"></span>**ERRORE \_ \_ di autorizzazione IKE IPSec errore \_ \_ \_ con \_ ripetizione facoltativa \_**</span><span class="sxs-lookup"><span data-stu-id="6415e-524"><span id="ERROR_IPSEC_IKE_AUTHORIZATION_FAILURE_WITH_OPTIONAL_RETRY"></span><span id="error_ipsec_ike_authorization_failure_with_optional_retry"></span>**ERROR\_IPSEC\_IKE\_AUTHORIZATION\_FAILURE\_WITH\_OPTIONAL\_RETRY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-525">13907 (0x3653)</span><span class="sxs-lookup"><span data-stu-id="6415e-525">13907 (0x3653)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-526">Associazione di sicurezza non autorizzata.</span><span class="sxs-lookup"><span data-stu-id="6415e-526">SA establishment is not authorized.</span></span> <span data-ttu-id="6415e-527">Potrebbe essere necessario immettere credenziali aggiornate o diverse, ad esempio una smart card.</span><span class="sxs-lookup"><span data-stu-id="6415e-527">You may need to enter updated or different credentials such as a smartcard.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-528"><span id="ERROR_IPSEC_IKE_STRONG_CRED_AUTHORIZATION_AND_CERTMAP_FAILURE"></span><span id="error_ipsec_ike_strong_cred_authorization_and_certmap_failure"></span>**errore \_ IPSec attendibile \_ IKE \_ \_ \_ \_ e \_ CERTMAP \_ errore**</span><span class="sxs-lookup"><span data-stu-id="6415e-528"><span id="ERROR_IPSEC_IKE_STRONG_CRED_AUTHORIZATION_AND_CERTMAP_FAILURE"></span><span id="error_ipsec_ike_strong_cred_authorization_and_certmap_failure"></span>**ERROR\_IPSEC\_IKE\_STRONG\_CRED\_AUTHORIZATION\_AND\_CERTMAP\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-529">13908 (0x3654)</span><span class="sxs-lookup"><span data-stu-id="6415e-529">13908 (0x3654)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-530">Lo stabilimento SA non è autorizzato perché non sono presenti credenziali basate su PKINIT sufficientemente complesse.</span><span class="sxs-lookup"><span data-stu-id="6415e-530">SA establishment is not authorized because there is not a sufficiently strong PKINIT-based credential.</span></span> <span data-ttu-id="6415e-531">Questo potrebbe essere correlato a un errore di mapping da certificato a account per il SA.</span><span class="sxs-lookup"><span data-stu-id="6415e-531">This might be related to certificate-to-account mapping failure for the SA.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-532"><span id="ERROR_IPSEC_IKE_NEG_STATUS_EXTENDED_END"></span><span id="error_ipsec_ike_neg_status_extended_end"></span>**ERRORE \_ di \_ \_ stato neg IPSec IKE \_ stato \_ esteso \_**</span><span class="sxs-lookup"><span data-stu-id="6415e-532"><span id="ERROR_IPSEC_IKE_NEG_STATUS_EXTENDED_END"></span><span id="error_ipsec_ike_neg_status_extended_end"></span>**ERROR\_IPSEC\_IKE\_NEG\_STATUS\_EXTENDED\_END**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-533">13909 (0x3655)</span><span class="sxs-lookup"><span data-stu-id="6415e-533">13909 (0x3655)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-534">ERRORE \_ di \_ \_ stato neg IPSec IKE \_ stato \_ esteso \_</span><span class="sxs-lookup"><span data-stu-id="6415e-534">ERROR\_IPSEC\_IKE\_NEG\_STATUS\_EXTENDED\_END</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-535"><span id="ERROR_IPSEC_BAD_SPI"></span><span id="error_ipsec_bad_spi"></span>**ERRORE \_ SPI IPSec non \_ valido \_**</span><span class="sxs-lookup"><span data-stu-id="6415e-535"><span id="ERROR_IPSEC_BAD_SPI"></span><span id="error_ipsec_bad_spi"></span>**ERROR\_IPSEC\_BAD\_SPI**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-536">13910 (0x3656)</span><span class="sxs-lookup"><span data-stu-id="6415e-536">13910 (0x3656)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-537">Il valore SPI nel pacchetto non corrisponde a un SA IPsec valido.</span><span class="sxs-lookup"><span data-stu-id="6415e-537">The SPI in the packet does not match a valid IPsec SA.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-538"><span id="ERROR_IPSEC_SA_LIFETIME_EXPIRED"></span><span id="error_ipsec_sa_lifetime_expired"></span>**\_ \_ Durata SA IPSec \_ errore \_ scaduta**</span><span class="sxs-lookup"><span data-stu-id="6415e-538"><span id="ERROR_IPSEC_SA_LIFETIME_EXPIRED"></span><span id="error_ipsec_sa_lifetime_expired"></span>**ERROR\_IPSEC\_SA\_LIFETIME\_EXPIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-539">13911 (0x3657)</span><span class="sxs-lookup"><span data-stu-id="6415e-539">13911 (0x3657)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-540">Il pacchetto è stato ricevuto su un SA IPsec la cui durata è scaduta.</span><span class="sxs-lookup"><span data-stu-id="6415e-540">Packet was received on an IPsec SA whose lifetime has expired.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-541"><span id="ERROR_IPSEC_WRONG_SA"></span><span id="error_ipsec_wrong_sa"></span>**ERRORE \_ IPSec \_ errato del \_ sa**</span><span class="sxs-lookup"><span data-stu-id="6415e-541"><span id="ERROR_IPSEC_WRONG_SA"></span><span id="error_ipsec_wrong_sa"></span>**ERROR\_IPSEC\_WRONG\_SA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-542">13912 (0x3658)</span><span class="sxs-lookup"><span data-stu-id="6415e-542">13912 (0x3658)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-543">Il pacchetto è stato ricevuto su un SA IPsec che non corrisponde alle caratteristiche del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="6415e-543">Packet was received on an IPsec SA that does not match the packet characteristics.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-544"><span id="ERROR_IPSEC_REPLAY_CHECK_FAILED"></span><span id="error_ipsec_replay_check_failed"></span>**ERRORE \_ di \_ Verifica riproduzione \_ IPSec \_ non riuscita**</span><span class="sxs-lookup"><span data-stu-id="6415e-544"><span id="ERROR_IPSEC_REPLAY_CHECK_FAILED"></span><span id="error_ipsec_replay_check_failed"></span>**ERROR\_IPSEC\_REPLAY\_CHECK\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-545">13913 (0x3659)</span><span class="sxs-lookup"><span data-stu-id="6415e-545">13913 (0x3659)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-546">Controllo riproduzione numero di sequenza del pacchetto non riuscito.</span><span class="sxs-lookup"><span data-stu-id="6415e-546">Packet sequence number replay check failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-547"><span id="ERROR_IPSEC_INVALID_PACKET"></span><span id="error_ipsec_invalid_packet"></span>**ERRORE \_ del \_ pacchetto IPSec non valido \_**</span><span class="sxs-lookup"><span data-stu-id="6415e-547"><span id="ERROR_IPSEC_INVALID_PACKET"></span><span id="error_ipsec_invalid_packet"></span>**ERROR\_IPSEC\_INVALID\_PACKET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-548">13914 (0x365A)</span><span class="sxs-lookup"><span data-stu-id="6415e-548">13914 (0x365A)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-549">L'intestazione IPsec e/o il trailer nel pacchetto non è valido.</span><span class="sxs-lookup"><span data-stu-id="6415e-549">IPsec header and/or trailer in the packet is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-550"><span id="ERROR_IPSEC_INTEGRITY_CHECK_FAILED"></span><span id="error_ipsec_integrity_check_failed"></span>**errore durante il \_ \_ controllo di integrità IPSec \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6415e-550"><span id="ERROR_IPSEC_INTEGRITY_CHECK_FAILED"></span><span id="error_ipsec_integrity_check_failed"></span>**ERROR\_IPSEC\_INTEGRITY\_CHECK\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-551">13915 (0x365B)</span><span class="sxs-lookup"><span data-stu-id="6415e-551">13915 (0x365B)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-552">Controllo integrità IPsec non riuscito.</span><span class="sxs-lookup"><span data-stu-id="6415e-552">IPsec integrity check failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-553"><span id="ERROR_IPSEC_CLEAR_TEXT_DROP"></span><span id="error_ipsec_clear_text_drop"></span>**\_eliminazione del \_ testo non crittografato IPsec \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6415e-553"><span id="ERROR_IPSEC_CLEAR_TEXT_DROP"></span><span id="error_ipsec_clear_text_drop"></span>**ERROR\_IPSEC\_CLEAR\_TEXT\_DROP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-554">13916 (0x365C)</span><span class="sxs-lookup"><span data-stu-id="6415e-554">13916 (0x365C)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-555">IPsec ha eliminato un pacchetto di testo non crittografato.</span><span class="sxs-lookup"><span data-stu-id="6415e-555">IPsec dropped a clear text packet.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-556"><span id="ERROR_IPSEC_AUTH_FIREWALL_DROP"></span><span id="error_ipsec_auth_firewall_drop"></span>**ERRORE \_ \_ \_ eliminazione firewall autenticazione \_ IPSec**</span><span class="sxs-lookup"><span data-stu-id="6415e-556"><span id="ERROR_IPSEC_AUTH_FIREWALL_DROP"></span><span id="error_ipsec_auth_firewall_drop"></span>**ERROR\_IPSEC\_AUTH\_FIREWALL\_DROP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-557">13917 (0x365D)</span><span class="sxs-lookup"><span data-stu-id="6415e-557">13917 (0x365D)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-558">IPsec ha eliminato un pacchetto ESP in ingresso in modalità firewall autenticato.</span><span class="sxs-lookup"><span data-stu-id="6415e-558">IPsec dropped an incoming ESP packet in authenticated firewall mode.</span></span> <span data-ttu-id="6415e-559">Questa eliminazione è benigna.</span><span class="sxs-lookup"><span data-stu-id="6415e-559">This drop is benign.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-560"><span id="ERROR_IPSEC_THROTTLE_DROP"></span><span id="error_ipsec_throttle_drop"></span>**ERRORE \_ di \_ eliminazione della limitazione IPSec \_**</span><span class="sxs-lookup"><span data-stu-id="6415e-560"><span id="ERROR_IPSEC_THROTTLE_DROP"></span><span id="error_ipsec_throttle_drop"></span>**ERROR\_IPSEC\_THROTTLE\_DROP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-561">13918 (0x365E)</span><span class="sxs-lookup"><span data-stu-id="6415e-561">13918 (0x365E)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-562">IPsec ha eliminato un pacchetto a causa della limitazione delle richieste DoS.</span><span class="sxs-lookup"><span data-stu-id="6415e-562">IPsec dropped a packet due to DoS throttling.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-563"><span id="ERROR_IPSEC_DOSP_BLOCK"></span><span id="error_ipsec_dosp_block"></span>**ERRORE \_ \_ blocco DoSP \_ IPSec**</span><span class="sxs-lookup"><span data-stu-id="6415e-563"><span id="ERROR_IPSEC_DOSP_BLOCK"></span><span id="error_ipsec_dosp_block"></span>**ERROR\_IPSEC\_DOSP\_BLOCK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-564">13925 (0x3665)</span><span class="sxs-lookup"><span data-stu-id="6415e-564">13925 (0x3665)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-565">La protezione DoS IPsec corrisponde a una regola di blocco esplicita.</span><span class="sxs-lookup"><span data-stu-id="6415e-565">IPsec DoS Protection matched an explicit block rule.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-566"><span id="ERROR_IPSEC_DOSP_RECEIVED_MULTICAST"></span><span id="error_ipsec_dosp_received_multicast"></span>**ERRORE \_ \_ DoSP IPSec \_ ricevuto dal \_ multicast**</span><span class="sxs-lookup"><span data-stu-id="6415e-566"><span id="ERROR_IPSEC_DOSP_RECEIVED_MULTICAST"></span><span id="error_ipsec_dosp_received_multicast"></span>**ERROR\_IPSEC\_DOSP\_RECEIVED\_MULTICAST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-567">13926 (0x3666)</span><span class="sxs-lookup"><span data-stu-id="6415e-567">13926 (0x3666)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-568">La protezione DoS IPsec ha ricevuto un pacchetto multicast specifico per IPsec che non è consentito.</span><span class="sxs-lookup"><span data-stu-id="6415e-568">IPsec DoS Protection received an IPsec specific multicast packet which is not allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-569"><span id="ERROR_IPSEC_DOSP_INVALID_PACKET"></span><span id="error_ipsec_dosp_invalid_packet"></span>**ERRORE \_ del \_ pacchetto DoSP IPSec \_ non valido \_**</span><span class="sxs-lookup"><span data-stu-id="6415e-569"><span id="ERROR_IPSEC_DOSP_INVALID_PACKET"></span><span id="error_ipsec_dosp_invalid_packet"></span>**ERROR\_IPSEC\_DOSP\_INVALID\_PACKET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-570">13927 (0x3667)</span><span class="sxs-lookup"><span data-stu-id="6415e-570">13927 (0x3667)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-571">La protezione DoS IPsec ha ricevuto un pacchetto formattato in modo errato.</span><span class="sxs-lookup"><span data-stu-id="6415e-571">IPsec DoS Protection received an incorrectly formatted packet.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-572"><span id="ERROR_IPSEC_DOSP_STATE_LOOKUP_FAILED"></span><span id="error_ipsec_dosp_state_lookup_failed"></span>**errore durante la \_ \_ \_ ricerca dello stato DoSP \_ IPSec \_**</span><span class="sxs-lookup"><span data-stu-id="6415e-572"><span id="ERROR_IPSEC_DOSP_STATE_LOOKUP_FAILED"></span><span id="error_ipsec_dosp_state_lookup_failed"></span>**ERROR\_IPSEC\_DOSP\_STATE\_LOOKUP\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-573">13928 (0x3668)</span><span class="sxs-lookup"><span data-stu-id="6415e-573">13928 (0x3668)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-574">La protezione DoS IPsec non è riuscita a cercare lo stato.</span><span class="sxs-lookup"><span data-stu-id="6415e-574">IPsec DoS Protection failed to look up state.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-575"><span id="ERROR_IPSEC_DOSP_MAX_ENTRIES"></span><span id="error_ipsec_dosp_max_entries"></span>**\_ \_ \_ numero massimo di \_ voci DoSP IPSec**</span><span class="sxs-lookup"><span data-stu-id="6415e-575"><span id="ERROR_IPSEC_DOSP_MAX_ENTRIES"></span><span id="error_ipsec_dosp_max_entries"></span>**ERROR\_IPSEC\_DOSP\_MAX\_ENTRIES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-576">13929 (0x3669)</span><span class="sxs-lookup"><span data-stu-id="6415e-576">13929 (0x3669)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-577">La protezione DoS IPsec non è riuscita a creare lo stato perché è stato raggiunto il numero massimo di voci consentite dai criteri.</span><span class="sxs-lookup"><span data-stu-id="6415e-577">IPsec DoS Protection failed to create state because the maximum number of entries allowed by policy has been reached.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-578"><span id="ERROR_IPSEC_DOSP_KEYMOD_NOT_ALLOWED"></span><span id="error_ipsec_dosp_keymod_not_allowed"></span>**ERRORE \_ IPSec \_ DoSP \_ KEYMOD \_ non \_ consentito**</span><span class="sxs-lookup"><span data-stu-id="6415e-578"><span id="ERROR_IPSEC_DOSP_KEYMOD_NOT_ALLOWED"></span><span id="error_ipsec_dosp_keymod_not_allowed"></span>**ERROR\_IPSEC\_DOSP\_KEYMOD\_NOT\_ALLOWED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-579">13930 (0x366A)</span><span class="sxs-lookup"><span data-stu-id="6415e-579">13930 (0x366A)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-580">La protezione DoS IPsec ha ricevuto un pacchetto di negoziazione IPsec per un modulo di chiavi non consentito dai criteri.</span><span class="sxs-lookup"><span data-stu-id="6415e-580">IPsec DoS Protection received an IPsec negotiation packet for a keying module which is not allowed by policy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-581"><span id="ERROR_IPSEC_DOSP_NOT_INSTALLED"></span><span id="error_ipsec_dosp_not_installed"></span>**ERRORE \_ \_ DoSP IPSec \_ non \_ installato**</span><span class="sxs-lookup"><span data-stu-id="6415e-581"><span id="ERROR_IPSEC_DOSP_NOT_INSTALLED"></span><span id="error_ipsec_dosp_not_installed"></span>**ERROR\_IPSEC\_DOSP\_NOT\_INSTALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-582">13931 (0x366B)</span><span class="sxs-lookup"><span data-stu-id="6415e-582">13931 (0x366B)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-583">La protezione DoS IPsec non è stata abilitata.</span><span class="sxs-lookup"><span data-stu-id="6415e-583">IPsec DoS Protection has not been enabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-584"><span id="ERROR_IPSEC_DOSP_MAX_PER_IP_RATELIMIT_QUEUES"></span><span id="error_ipsec_dosp_max_per_ip_ratelimit_queues"></span>**ERRORE \_ IPSec \_ DoSP \_ Max \_ per \_ IP \_ RATELIMIT \_ code**</span><span class="sxs-lookup"><span data-stu-id="6415e-584"><span id="ERROR_IPSEC_DOSP_MAX_PER_IP_RATELIMIT_QUEUES"></span><span id="error_ipsec_dosp_max_per_ip_ratelimit_queues"></span>**ERROR\_IPSEC\_DOSP\_MAX\_PER\_IP\_RATELIMIT\_QUEUES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-585">13932 (0x366C)</span><span class="sxs-lookup"><span data-stu-id="6415e-585">13932 (0x366C)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-586">La protezione DoS IPsec non è riuscita a creare una coda per il limite di frequenza IP interno perché è stato raggiunto il numero massimo di code consentite dai criteri.</span><span class="sxs-lookup"><span data-stu-id="6415e-586">IPsec DoS Protection failed to create a per internal IP rate limit queue because the maximum number of queues allowed by policy has been reached.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-587"><span id="ERROR_SXS_SECTION_NOT_FOUND"></span><span id="error_sxs_section_not_found"></span>**\_sezione errore \_ SxS \_ non \_ trovata**</span><span class="sxs-lookup"><span data-stu-id="6415e-587"><span id="ERROR_SXS_SECTION_NOT_FOUND"></span><span id="error_sxs_section_not_found"></span>**ERROR\_SXS\_SECTION\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-588">14000 (0x36B0)</span><span class="sxs-lookup"><span data-stu-id="6415e-588">14000 (0x36B0)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-589">La sezione richiesta non è presente nel contesto di attivazione.</span><span class="sxs-lookup"><span data-stu-id="6415e-589">The requested section was not present in the activation context.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-590"><span id="ERROR_SXS_CANT_GEN_ACTCTX"></span><span id="error_sxs_cant_gen_actctx"></span>**ERRORE \_ SxS \_ \_ ACTCTX generazione \_ non riuscita**</span><span class="sxs-lookup"><span data-stu-id="6415e-590"><span id="ERROR_SXS_CANT_GEN_ACTCTX"></span><span id="error_sxs_cant_gen_actctx"></span>**ERROR\_SXS\_CANT\_GEN\_ACTCTX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-591">14001 (0x36B1)</span><span class="sxs-lookup"><span data-stu-id="6415e-591">14001 (0x36B1)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-592">Non è stato possibile avviare l'applicazione perché la configurazione affiancata non è corretta.</span><span class="sxs-lookup"><span data-stu-id="6415e-592">The application has failed to start because its side-by-side configuration is incorrect.</span></span> <span data-ttu-id="6415e-593">Per informazioni dettagliate, vedere il registro eventi dell'applicazione o usare lo strumento della riga di comando sxstrace.exe.</span><span class="sxs-lookup"><span data-stu-id="6415e-593">Please see the application event log or use the command-line sxstrace.exe tool for more detail.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-594"><span id="ERROR_SXS_INVALID_ACTCTXDATA_FORMAT"></span><span id="error_sxs_invalid_actctxdata_format"></span>**ERRORE \_ SxS \_ non \_ valido \_ formato ACTCTXDATA**</span><span class="sxs-lookup"><span data-stu-id="6415e-594"><span id="ERROR_SXS_INVALID_ACTCTXDATA_FORMAT"></span><span id="error_sxs_invalid_actctxdata_format"></span>**ERROR\_SXS\_INVALID\_ACTCTXDATA\_FORMAT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-595">14002 (0x36B2)</span><span class="sxs-lookup"><span data-stu-id="6415e-595">14002 (0x36B2)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-596">Il formato dei dati di associazione dell'applicazione non è valido.</span><span class="sxs-lookup"><span data-stu-id="6415e-596">The application binding data format is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-597"><span id="ERROR_SXS_ASSEMBLY_NOT_FOUND"></span><span id="error_sxs_assembly_not_found"></span>**ERRORE \_ dell' \_ assembly SxS \_ non \_ trovato**</span><span class="sxs-lookup"><span data-stu-id="6415e-597"><span id="ERROR_SXS_ASSEMBLY_NOT_FOUND"></span><span id="error_sxs_assembly_not_found"></span>**ERROR\_SXS\_ASSEMBLY\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-598">14003 (0x36B3)</span><span class="sxs-lookup"><span data-stu-id="6415e-598">14003 (0x36B3)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-599">L'assembly a cui si fa riferimento non è installato nel sistema.</span><span class="sxs-lookup"><span data-stu-id="6415e-599">The referenced assembly is not installed on your system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-600"><span id="ERROR_SXS_MANIFEST_FORMAT_ERROR"></span><span id="error_sxs_manifest_format_error"></span>**\_errore di \_ \_ formato manifesto SxS errore \_**</span><span class="sxs-lookup"><span data-stu-id="6415e-600"><span id="ERROR_SXS_MANIFEST_FORMAT_ERROR"></span><span id="error_sxs_manifest_format_error"></span>**ERROR\_SXS\_MANIFEST\_FORMAT\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-601">14004 (0x36B4)</span><span class="sxs-lookup"><span data-stu-id="6415e-601">14004 (0x36B4)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-602">Il file manifesto non inizia con il tag e le informazioni di formato richiesti.</span><span class="sxs-lookup"><span data-stu-id="6415e-602">The manifest file does not begin with the required tag and format information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-603"><span id="ERROR_SXS_MANIFEST_PARSE_ERROR"></span><span id="error_sxs_manifest_parse_error"></span>**errore \_ di \_ analisi del manifesto SxS \_ errore \_**</span><span class="sxs-lookup"><span data-stu-id="6415e-603"><span id="ERROR_SXS_MANIFEST_PARSE_ERROR"></span><span id="error_sxs_manifest_parse_error"></span>**ERROR\_SXS\_MANIFEST\_PARSE\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-604">14005 (0x36B5)</span><span class="sxs-lookup"><span data-stu-id="6415e-604">14005 (0x36B5)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-605">Il file manifesto contiene uno o più errori di sintassi.</span><span class="sxs-lookup"><span data-stu-id="6415e-605">The manifest file contains one or more syntax errors.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-606"><span id="ERROR_SXS_ACTIVATION_CONTEXT_DISABLED"></span><span id="error_sxs_activation_context_disabled"></span>**\_contesto di attivazione SxS di errore \_ \_ \_ disabilitato**</span><span class="sxs-lookup"><span data-stu-id="6415e-606"><span id="ERROR_SXS_ACTIVATION_CONTEXT_DISABLED"></span><span id="error_sxs_activation_context_disabled"></span>**ERROR\_SXS\_ACTIVATION\_CONTEXT\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-607">14006 (0x36B6)</span><span class="sxs-lookup"><span data-stu-id="6415e-607">14006 (0x36B6)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-608">L'applicazione ha tentato di attivare un contesto di attivazione disabilitato.</span><span class="sxs-lookup"><span data-stu-id="6415e-608">The application attempted to activate a disabled activation context.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-609"><span id="ERROR_SXS_KEY_NOT_FOUND"></span><span id="error_sxs_key_not_found"></span>**\_chiave SxS di errore \_ \_ non \_ trovata**</span><span class="sxs-lookup"><span data-stu-id="6415e-609"><span id="ERROR_SXS_KEY_NOT_FOUND"></span><span id="error_sxs_key_not_found"></span>**ERROR\_SXS\_KEY\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-610">14007 (0x36B7)</span><span class="sxs-lookup"><span data-stu-id="6415e-610">14007 (0x36B7)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-611">La chiave di ricerca richiesta non è stata trovata in alcun contesto di attivazione attiva.</span><span class="sxs-lookup"><span data-stu-id="6415e-611">The requested lookup key was not found in any active activation context.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-612"><span id="ERROR_SXS_VERSION_CONFLICT"></span><span id="error_sxs_version_conflict"></span>**\_ \_ conflitto versione SxS \_ errore**</span><span class="sxs-lookup"><span data-stu-id="6415e-612"><span id="ERROR_SXS_VERSION_CONFLICT"></span><span id="error_sxs_version_conflict"></span>**ERROR\_SXS\_VERSION\_CONFLICT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-613">14008 (0x36B8)</span><span class="sxs-lookup"><span data-stu-id="6415e-613">14008 (0x36B8)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-614">Una versione del componente richiesta dall'applicazione è in conflitto con un'altra versione del componente già attiva.</span><span class="sxs-lookup"><span data-stu-id="6415e-614">A component version required by the application conflicts with another component version already active.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-615"><span id="ERROR_SXS_WRONG_SECTION_TYPE"></span><span id="error_sxs_wrong_section_type"></span>**ERRORE \_ SxS \_ \_ tipo di sezione errato \_**</span><span class="sxs-lookup"><span data-stu-id="6415e-615"><span id="ERROR_SXS_WRONG_SECTION_TYPE"></span><span id="error_sxs_wrong_section_type"></span>**ERROR\_SXS\_WRONG\_SECTION\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-616">14009 (0x36B9)</span><span class="sxs-lookup"><span data-stu-id="6415e-616">14009 (0x36B9)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-617">Il tipo della sezione del contesto di attivazione richiesta non corrisponde all'API di query usata.</span><span class="sxs-lookup"><span data-stu-id="6415e-617">The type requested activation context section does not match the query API used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-618"><span id="ERROR_SXS_THREAD_QUERIES_DISABLED"></span><span id="error_sxs_thread_queries_disabled"></span>**\_ \_ query thread SxS \_ errore \_ disabilitata**</span><span class="sxs-lookup"><span data-stu-id="6415e-618"><span id="ERROR_SXS_THREAD_QUERIES_DISABLED"></span><span id="error_sxs_thread_queries_disabled"></span>**ERROR\_SXS\_THREAD\_QUERIES\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-619">14010 (0x36BA)</span><span class="sxs-lookup"><span data-stu-id="6415e-619">14010 (0x36BA)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-620">La mancanza di risorse di sistema ha richiesto l'attivazione isolata per essere disabilitata per il thread di esecuzione corrente.</span><span class="sxs-lookup"><span data-stu-id="6415e-620">Lack of system resources has required isolated activation to be disabled for the current thread of execution.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-621"><span id="ERROR_SXS_PROCESS_DEFAULT_ALREADY_SET"></span><span id="error_sxs_process_default_already_set"></span>**ERRORE \_ SxS \_ processo \_ predefinito \_ già \_ impostato**</span><span class="sxs-lookup"><span data-stu-id="6415e-621"><span id="ERROR_SXS_PROCESS_DEFAULT_ALREADY_SET"></span><span id="error_sxs_process_default_already_set"></span>**ERROR\_SXS\_PROCESS\_DEFAULT\_ALREADY\_SET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-622">14011 (0x36BB)</span><span class="sxs-lookup"><span data-stu-id="6415e-622">14011 (0x36BB)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-623">Tentativo di impostazione del contesto di attivazione predefinito del processo non riuscito perché il contesto di attivazione predefinito del processo è già stato impostato.</span><span class="sxs-lookup"><span data-stu-id="6415e-623">An attempt to set the process default activation context failed because the process default activation context was already set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-624"><span id="ERROR_SXS_UNKNOWN_ENCODING_GROUP"></span><span id="error_sxs_unknown_encoding_group"></span>**ERRORE \_ SxS \_ \_ gruppo di codifica sconosciuto \_**</span><span class="sxs-lookup"><span data-stu-id="6415e-624"><span id="ERROR_SXS_UNKNOWN_ENCODING_GROUP"></span><span id="error_sxs_unknown_encoding_group"></span>**ERROR\_SXS\_UNKNOWN\_ENCODING\_GROUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-625">14012 (0x36BC)</span><span class="sxs-lookup"><span data-stu-id="6415e-625">14012 (0x36BC)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-626">L'identificatore del gruppo di codifica specificato non è riconosciuto.</span><span class="sxs-lookup"><span data-stu-id="6415e-626">The encoding group identifier specified is not recognized.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-627"><span id="ERROR_SXS_UNKNOWN_ENCODING"></span><span id="error_sxs_unknown_encoding"></span>**ERRORE \_ SxS \_ \_ codifica sconosciuta**</span><span class="sxs-lookup"><span data-stu-id="6415e-627"><span id="ERROR_SXS_UNKNOWN_ENCODING"></span><span id="error_sxs_unknown_encoding"></span>**ERROR\_SXS\_UNKNOWN\_ENCODING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-628">14013 (0x36BD)</span><span class="sxs-lookup"><span data-stu-id="6415e-628">14013 (0x36BD)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-629">La codifica richiesta non è riconosciuta.</span><span class="sxs-lookup"><span data-stu-id="6415e-629">The encoding requested is not recognized.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-630"><span id="ERROR_SXS_INVALID_XML_NAMESPACE_URI"></span><span id="error_sxs_invalid_xml_namespace_uri"></span>**ERRORE \_ SxS \_ non \_ valido \_ URI dello spazio dei nomi XML \_**</span><span class="sxs-lookup"><span data-stu-id="6415e-630"><span id="ERROR_SXS_INVALID_XML_NAMESPACE_URI"></span><span id="error_sxs_invalid_xml_namespace_uri"></span>**ERROR\_SXS\_INVALID\_XML\_NAMESPACE\_URI**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-631">14014 (0x36BE)</span><span class="sxs-lookup"><span data-stu-id="6415e-631">14014 (0x36BE)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-632">Il manifesto contiene un riferimento a un URI non valido.</span><span class="sxs-lookup"><span data-stu-id="6415e-632">The manifest contains a reference to an invalid URI.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-633"><span id="ERROR_SXS_ROOT_MANIFEST_DEPENDENCY_NOT_INSTALLED"></span><span id="error_sxs_root_manifest_dependency_not_installed"></span>**\_ \_ dipendenza manifesto radice errore SxS \_ \_ \_ non \_ installata**</span><span class="sxs-lookup"><span data-stu-id="6415e-633"><span id="ERROR_SXS_ROOT_MANIFEST_DEPENDENCY_NOT_INSTALLED"></span><span id="error_sxs_root_manifest_dependency_not_installed"></span>**ERROR\_SXS\_ROOT\_MANIFEST\_DEPENDENCY\_NOT\_INSTALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-634">14015 (0x36BF)</span><span class="sxs-lookup"><span data-stu-id="6415e-634">14015 (0x36BF)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-635">Il manifesto dell'applicazione contiene un riferimento a un assembly dipendente che non è installato.</span><span class="sxs-lookup"><span data-stu-id="6415e-635">The application manifest contains a reference to a dependent assembly which is not installed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-636"><span id="ERROR_SXS_LEAF_MANIFEST_DEPENDENCY_NOT_INSTALLED"></span><span id="error_sxs_leaf_manifest_dependency_not_installed"></span>**\_ \_ dipendenza manifesto foglia errore SxS \_ \_ \_ non \_ installata**</span><span class="sxs-lookup"><span data-stu-id="6415e-636"><span id="ERROR_SXS_LEAF_MANIFEST_DEPENDENCY_NOT_INSTALLED"></span><span id="error_sxs_leaf_manifest_dependency_not_installed"></span>**ERROR\_SXS\_LEAF\_MANIFEST\_DEPENDENCY\_NOT\_INSTALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-637">14016 (0x36C0)</span><span class="sxs-lookup"><span data-stu-id="6415e-637">14016 (0x36C0)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-638">Il manifesto di un assembly utilizzato dall'applicazione contiene un riferimento a un assembly dipendente che non è installato.</span><span class="sxs-lookup"><span data-stu-id="6415e-638">The manifest for an assembly used by the application has a reference to a dependent assembly which is not installed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-639"><span id="ERROR_SXS_INVALID_ASSEMBLY_IDENTITY_ATTRIBUTE"></span><span id="error_sxs_invalid_assembly_identity_attribute"></span>**ERRORE \_ SxS \_ \_ \_ attributo identità assembly non valido \_**</span><span class="sxs-lookup"><span data-stu-id="6415e-639"><span id="ERROR_SXS_INVALID_ASSEMBLY_IDENTITY_ATTRIBUTE"></span><span id="error_sxs_invalid_assembly_identity_attribute"></span>**ERROR\_SXS\_INVALID\_ASSEMBLY\_IDENTITY\_ATTRIBUTE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-640">14017 (0x36C1)</span><span class="sxs-lookup"><span data-stu-id="6415e-640">14017 (0x36C1)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-641">Il manifesto contiene un attributo per l'identità dell'assembly non valido.</span><span class="sxs-lookup"><span data-stu-id="6415e-641">The manifest contains an attribute for the assembly identity which is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-642"><span id="ERROR_SXS_MANIFEST_MISSING_REQUIRED_DEFAULT_NAMESPACE"></span><span id="error_sxs_manifest_missing_required_default_namespace"></span>**il \_ manifesto SxS errore \_ \_ manca \_ \_ \_ lo spazio dei nomi predefinito obbligatorio**</span><span class="sxs-lookup"><span data-stu-id="6415e-642"><span id="ERROR_SXS_MANIFEST_MISSING_REQUIRED_DEFAULT_NAMESPACE"></span><span id="error_sxs_manifest_missing_required_default_namespace"></span>**ERROR\_SXS\_MANIFEST\_MISSING\_REQUIRED\_DEFAULT\_NAMESPACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-643">14018 (0x36C2)</span><span class="sxs-lookup"><span data-stu-id="6415e-643">14018 (0x36C2)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-644">Nel manifesto manca la specifica dello spazio dei nomi predefinita richiesta nell'elemento assembly.</span><span class="sxs-lookup"><span data-stu-id="6415e-644">The manifest is missing the required default namespace specification on the assembly element.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-645"><span id="ERROR_SXS_MANIFEST_INVALID_REQUIRED_DEFAULT_NAMESPACE"></span><span id="error_sxs_manifest_invalid_required_default_namespace"></span>**ERRORE \_ del \_ manifesto SxS \_ non valido. \_ \_ \_ spazio dei nomi predefinito obbligatorio**</span><span class="sxs-lookup"><span data-stu-id="6415e-645"><span id="ERROR_SXS_MANIFEST_INVALID_REQUIRED_DEFAULT_NAMESPACE"></span><span id="error_sxs_manifest_invalid_required_default_namespace"></span>**ERROR\_SXS\_MANIFEST\_INVALID\_REQUIRED\_DEFAULT\_NAMESPACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-646">14019 (0x36C3)</span><span class="sxs-lookup"><span data-stu-id="6415e-646">14019 (0x36C3)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-647">Per il manifesto è stato specificato uno spazio dei nomi predefinito nell'elemento assembly, ma il relativo valore non è "urn: schemas-microsoft-com: ASM. V1".</span><span class="sxs-lookup"><span data-stu-id="6415e-647">The manifest has a default namespace specified on the assembly element but its value is not "urn:schemas-microsoft-com:asm.v1".</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-648"><span id="ERROR_SXS_PRIVATE_MANIFEST_CROSS_PATH_WITH_REPARSE_POINT"></span><span id="error_sxs_private_manifest_cross_path_with_reparse_point"></span>**ERRORE \_ SxS \_ privato del \_ manifesto privato \_ \_ \_ con \_ punto di analisi \_**</span><span class="sxs-lookup"><span data-stu-id="6415e-648"><span id="ERROR_SXS_PRIVATE_MANIFEST_CROSS_PATH_WITH_REPARSE_POINT"></span><span id="error_sxs_private_manifest_cross_path_with_reparse_point"></span>**ERROR\_SXS\_PRIVATE\_MANIFEST\_CROSS\_PATH\_WITH\_REPARSE\_POINT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-649">14020 (0x36C4)</span><span class="sxs-lookup"><span data-stu-id="6415e-649">14020 (0x36C4)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-650">Il manifesto privato Probe ha superato un percorso con un reparse point non supportato.</span><span class="sxs-lookup"><span data-stu-id="6415e-650">The private manifest probed has crossed a path with an unsupported reparse point.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-651"><span id="ERROR_SXS_DUPLICATE_DLL_NAME"></span><span id="error_sxs_duplicate_dll_name"></span>**ERRORE \_ SxS \_ \_ nome dll duplicato \_**</span><span class="sxs-lookup"><span data-stu-id="6415e-651"><span id="ERROR_SXS_DUPLICATE_DLL_NAME"></span><span id="error_sxs_duplicate_dll_name"></span>**ERROR\_SXS\_DUPLICATE\_DLL\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-652">14021 (0x36C5)</span><span class="sxs-lookup"><span data-stu-id="6415e-652">14021 (0x36C5)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-653">Due o più componenti a cui viene fatto riferimento direttamente o indirettamente dal manifesto dell'applicazione hanno file con lo stesso nome.</span><span class="sxs-lookup"><span data-stu-id="6415e-653">Two or more components referenced directly or indirectly by the application manifest have files by the same name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-654"><span id="ERROR_SXS_DUPLICATE_WINDOWCLASS_NAME"></span><span id="error_sxs_duplicate_windowclass_name"></span>**ERRORE \_ SxS \_ duplicato \_ WINDOWCLASS \_ nome**</span><span class="sxs-lookup"><span data-stu-id="6415e-654"><span id="ERROR_SXS_DUPLICATE_WINDOWCLASS_NAME"></span><span id="error_sxs_duplicate_windowclass_name"></span>**ERROR\_SXS\_DUPLICATE\_WINDOWCLASS\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-655">14022 (0x36C6)</span><span class="sxs-lookup"><span data-stu-id="6415e-655">14022 (0x36C6)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-656">Due o più componenti a cui viene fatto riferimento direttamente o indirettamente dal manifesto dell'applicazione hanno classi finestra con lo stesso nome.</span><span class="sxs-lookup"><span data-stu-id="6415e-656">Two or more components referenced directly or indirectly by the application manifest have window classes with the same name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-657"><span id="ERROR_SXS_DUPLICATE_CLSID"></span><span id="error_sxs_duplicate_clsid"></span>**\_ \_ CLSID duplicato errore SxS \_**</span><span class="sxs-lookup"><span data-stu-id="6415e-657"><span id="ERROR_SXS_DUPLICATE_CLSID"></span><span id="error_sxs_duplicate_clsid"></span>**ERROR\_SXS\_DUPLICATE\_CLSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-658">14023 (0x36C7)</span><span class="sxs-lookup"><span data-stu-id="6415e-658">14023 (0x36C7)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-659">Due o più componenti a cui viene fatto riferimento in modo diretto o indiretto dal manifesto dell'applicazione hanno gli stessi CLSID del server COM.</span><span class="sxs-lookup"><span data-stu-id="6415e-659">Two or more components referenced directly or indirectly by the application manifest have the same COM server CLSIDs.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-660"><span id="ERROR_SXS_DUPLICATE_IID"></span><span id="error_sxs_duplicate_iid"></span>**\_ \_ IID duplicato errore SxS \_**</span><span class="sxs-lookup"><span data-stu-id="6415e-660"><span id="ERROR_SXS_DUPLICATE_IID"></span><span id="error_sxs_duplicate_iid"></span>**ERROR\_SXS\_DUPLICATE\_IID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-661">14024 (0x36C8)</span><span class="sxs-lookup"><span data-stu-id="6415e-661">14024 (0x36C8)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-662">Due o più componenti a cui viene fatto riferimento direttamente o indirettamente dal manifesto dell'applicazione hanno proxy per la stessa interfaccia COM IID.</span><span class="sxs-lookup"><span data-stu-id="6415e-662">Two or more components referenced directly or indirectly by the application manifest have proxies for the same COM interface IIDs.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-663"><span id="ERROR_SXS_DUPLICATE_TLBID"></span><span id="error_sxs_duplicate_tlbid"></span>**ERRORE \_ SxS \_ duplicato \_ TLBID**</span><span class="sxs-lookup"><span data-stu-id="6415e-663"><span id="ERROR_SXS_DUPLICATE_TLBID"></span><span id="error_sxs_duplicate_tlbid"></span>**ERROR\_SXS\_DUPLICATE\_TLBID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-664">14025 (0x36C9)</span><span class="sxs-lookup"><span data-stu-id="6415e-664">14025 (0x36C9)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-665">Due o più componenti a cui viene fatto riferimento direttamente o indirettamente dal manifesto dell'applicazione hanno lo stesso TLBIDs della libreria dei tipi COM.</span><span class="sxs-lookup"><span data-stu-id="6415e-665">Two or more components referenced directly or indirectly by the application manifest have the same COM type library TLBIDs.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-666"><span id="ERROR_SXS_DUPLICATE_PROGID"></span><span id="error_sxs_duplicate_progid"></span>**\_ \_ ProgID duplicato errore SxS \_**</span><span class="sxs-lookup"><span data-stu-id="6415e-666"><span id="ERROR_SXS_DUPLICATE_PROGID"></span><span id="error_sxs_duplicate_progid"></span>**ERROR\_SXS\_DUPLICATE\_PROGID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-667">14026 (0x36CA)</span><span class="sxs-lookup"><span data-stu-id="6415e-667">14026 (0x36CA)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-668">Due o più componenti a cui viene fatto riferimento in modo diretto o indiretto dal manifesto dell'applicazione hanno gli stessi ProgID COM.</span><span class="sxs-lookup"><span data-stu-id="6415e-668">Two or more components referenced directly or indirectly by the application manifest have the same COM ProgIDs.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-669"><span id="ERROR_SXS_DUPLICATE_ASSEMBLY_NAME"></span><span id="error_sxs_duplicate_assembly_name"></span>**ERRORE \_ SxS \_ duplicato \_ \_ nome assembly**</span><span class="sxs-lookup"><span data-stu-id="6415e-669"><span id="ERROR_SXS_DUPLICATE_ASSEMBLY_NAME"></span><span id="error_sxs_duplicate_assembly_name"></span>**ERROR\_SXS\_DUPLICATE\_ASSEMBLY\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-670">14027 (0x36CB)</span><span class="sxs-lookup"><span data-stu-id="6415e-670">14027 (0x36CB)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-671">Due o più componenti a cui viene fatto riferimento in modo diretto o indiretto dal manifesto dell'applicazione sono versioni diverse dello stesso componente. questa operazione non è consentita.</span><span class="sxs-lookup"><span data-stu-id="6415e-671">Two or more components referenced directly or indirectly by the application manifest are different versions of the same component which is not permitted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-672"><span id="ERROR_SXS_FILE_HASH_MISMATCH"></span><span id="error_sxs_file_hash_mismatch"></span>**ERRORE \_ di \_ hash file SxS non \_ \_ corrispondente**</span><span class="sxs-lookup"><span data-stu-id="6415e-672"><span id="ERROR_SXS_FILE_HASH_MISMATCH"></span><span id="error_sxs_file_hash_mismatch"></span>**ERROR\_SXS\_FILE\_HASH\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-673">14028 (0x36CC)</span><span class="sxs-lookup"><span data-stu-id="6415e-673">14028 (0x36CC)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-674">Il file di un componente non corrisponde alle informazioni di verifica presenti nel manifesto del componente.</span><span class="sxs-lookup"><span data-stu-id="6415e-674">A component's file does not match the verification information present in the component manifest.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-675"><span id="ERROR_SXS_POLICY_PARSE_ERROR"></span><span id="error_sxs_policy_parse_error"></span>**errore \_ di \_ analisi criteri SxS \_ errore \_**</span><span class="sxs-lookup"><span data-stu-id="6415e-675"><span id="ERROR_SXS_POLICY_PARSE_ERROR"></span><span id="error_sxs_policy_parse_error"></span>**ERROR\_SXS\_POLICY\_PARSE\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-676">14029 (0x36CD)</span><span class="sxs-lookup"><span data-stu-id="6415e-676">14029 (0x36CD)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-677">Il manifesto dei criteri contiene uno o più errori di sintassi.</span><span class="sxs-lookup"><span data-stu-id="6415e-677">The policy manifest contains one or more syntax errors.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-678"><span id="ERROR_SXS_XML_E_MISSINGQUOTE"></span><span id="error_sxs_xml_e_missingquote"></span>**ERRORE \_ SxS \_ XML \_ E \_ MISSINGQUOTE**</span><span class="sxs-lookup"><span data-stu-id="6415e-678"><span id="ERROR_SXS_XML_E_MISSINGQUOTE"></span><span id="error_sxs_xml_e_missingquote"></span>**ERROR\_SXS\_XML\_E\_MISSINGQUOTE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-679">14030 (0x36CE)</span><span class="sxs-lookup"><span data-stu-id="6415e-679">14030 (0x36CE)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-680">Errore di analisi del manifesto: è previsto un valore letterale stringa, ma non è stato trovato alcun carattere virgolette di apertura.</span><span class="sxs-lookup"><span data-stu-id="6415e-680">Manifest Parse Error : A string literal was expected, but no opening quote character was found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-681"><span id="ERROR_SXS_XML_E_COMMENTSYNTAX"></span><span id="error_sxs_xml_e_commentsyntax"></span>**ERRORE \_ SxS \_ XML \_ E \_ COMMENTSYNTAX**</span><span class="sxs-lookup"><span data-stu-id="6415e-681"><span id="ERROR_SXS_XML_E_COMMENTSYNTAX"></span><span id="error_sxs_xml_e_commentsyntax"></span>**ERROR\_SXS\_XML\_E\_COMMENTSYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-682">14031 (0x36CF)</span><span class="sxs-lookup"><span data-stu-id="6415e-682">14031 (0x36CF)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-683">Errore di analisi del manifesto: sintassi non corretta in un commento.</span><span class="sxs-lookup"><span data-stu-id="6415e-683">Manifest Parse Error : Incorrect syntax was used in a comment.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-684"><span id="ERROR_SXS_XML_E_BADSTARTNAMECHAR"></span><span id="error_sxs_xml_e_badstartnamechar"></span>**ERRORE \_ SxS \_ XML \_ E \_ BADSTARTNAMECHAR**</span><span class="sxs-lookup"><span data-stu-id="6415e-684"><span id="ERROR_SXS_XML_E_BADSTARTNAMECHAR"></span><span id="error_sxs_xml_e_badstartnamechar"></span>**ERROR\_SXS\_XML\_E\_BADSTARTNAMECHAR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-685">14032 (0x36D0)</span><span class="sxs-lookup"><span data-stu-id="6415e-685">14032 (0x36D0)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-686">Errore di analisi del manifesto: è stato avviato un nome con un carattere non valido.</span><span class="sxs-lookup"><span data-stu-id="6415e-686">Manifest Parse Error : A name was started with an invalid character.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-687"><span id="ERROR_SXS_XML_E_BADNAMECHAR"></span><span id="error_sxs_xml_e_badnamechar"></span>**ERRORE \_ SxS \_ XML \_ E \_ BADNAMECHAR**</span><span class="sxs-lookup"><span data-stu-id="6415e-687"><span id="ERROR_SXS_XML_E_BADNAMECHAR"></span><span id="error_sxs_xml_e_badnamechar"></span>**ERROR\_SXS\_XML\_E\_BADNAMECHAR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-688">14033 (0x36D1)</span><span class="sxs-lookup"><span data-stu-id="6415e-688">14033 (0x36D1)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-689">Errore di analisi del manifesto: un nome contiene un carattere non valido.</span><span class="sxs-lookup"><span data-stu-id="6415e-689">Manifest Parse Error : A name contained an invalid character.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-690"><span id="ERROR_SXS_XML_E_BADCHARINSTRING"></span><span id="error_sxs_xml_e_badcharinstring"></span>**ERRORE \_ SxS \_ XML \_ E \_ BADCHARINSTRING**</span><span class="sxs-lookup"><span data-stu-id="6415e-690"><span id="ERROR_SXS_XML_E_BADCHARINSTRING"></span><span id="error_sxs_xml_e_badcharinstring"></span>**ERROR\_SXS\_XML\_E\_BADCHARINSTRING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-691">14034 (0x36D2)</span><span class="sxs-lookup"><span data-stu-id="6415e-691">14034 (0x36D2)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-692">Errore di analisi del manifesto: un valore letterale stringa contiene un carattere non valido.</span><span class="sxs-lookup"><span data-stu-id="6415e-692">Manifest Parse Error : A string literal contained an invalid character.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-693"><span id="ERROR_SXS_XML_E_XMLDECLSYNTAX"></span><span id="error_sxs_xml_e_xmldeclsyntax"></span>**ERRORE \_ SxS \_ XML \_ E \_ XMLDECLSYNTAX**</span><span class="sxs-lookup"><span data-stu-id="6415e-693"><span id="ERROR_SXS_XML_E_XMLDECLSYNTAX"></span><span id="error_sxs_xml_e_xmldeclsyntax"></span>**ERROR\_SXS\_XML\_E\_XMLDECLSYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-694">14035 (0x36D3)</span><span class="sxs-lookup"><span data-stu-id="6415e-694">14035 (0x36D3)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-695">Errore di analisi del manifesto: sintassi non valida per una dichiarazione XML.</span><span class="sxs-lookup"><span data-stu-id="6415e-695">Manifest Parse Error : Invalid syntax for an xml declaration.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-696"><span id="ERROR_SXS_XML_E_BADCHARDATA"></span><span id="error_sxs_xml_e_badchardata"></span>**ERRORE \_ SxS \_ XML \_ E \_ BADCHARDATA**</span><span class="sxs-lookup"><span data-stu-id="6415e-696"><span id="ERROR_SXS_XML_E_BADCHARDATA"></span><span id="error_sxs_xml_e_badchardata"></span>**ERROR\_SXS\_XML\_E\_BADCHARDATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-697">14036 (0x36D4)</span><span class="sxs-lookup"><span data-stu-id="6415e-697">14036 (0x36D4)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-698">Errore di analisi del manifesto: è stato trovato un carattere non valido nel contenuto di testo.</span><span class="sxs-lookup"><span data-stu-id="6415e-698">Manifest Parse Error : An Invalid character was found in text content.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-699"><span id="ERROR_SXS_XML_E_MISSINGWHITESPACE"></span><span id="error_sxs_xml_e_missingwhitespace"></span>**ERRORE \_ SxS \_ XML \_ E \_ MISSINGWHITESPACE**</span><span class="sxs-lookup"><span data-stu-id="6415e-699"><span id="ERROR_SXS_XML_E_MISSINGWHITESPACE"></span><span id="error_sxs_xml_e_missingwhitespace"></span>**ERROR\_SXS\_XML\_E\_MISSINGWHITESPACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-700">14037 (0x36D5)</span><span class="sxs-lookup"><span data-stu-id="6415e-700">14037 (0x36D5)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-701">Errore di analisi del manifesto: manca lo spazio vuoto obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="6415e-701">Manifest Parse Error : Required white space was missing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-702"><span id="ERROR_SXS_XML_E_EXPECTINGTAGEND"></span><span id="error_sxs_xml_e_expectingtagend"></span>**ERRORE \_ SxS \_ XML \_ E \_ EXPECTINGTAGEND**</span><span class="sxs-lookup"><span data-stu-id="6415e-702"><span id="ERROR_SXS_XML_E_EXPECTINGTAGEND"></span><span id="error_sxs_xml_e_expectingtagend"></span>**ERROR\_SXS\_XML\_E\_EXPECTINGTAGEND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-703">14038 (0x36D6)</span><span class="sxs-lookup"><span data-stu-id="6415e-703">14038 (0x36D6)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-704">Errore di analisi del manifesto: previsto il carattere ' >'.</span><span class="sxs-lookup"><span data-stu-id="6415e-704">Manifest Parse Error : The character '>' was expected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-705"><span id="ERROR_SXS_XML_E_MISSINGSEMICOLON"></span><span id="error_sxs_xml_e_missingsemicolon"></span>**ERRORE \_ SxS \_ XML \_ E \_ MISSINGSEMICOLON**</span><span class="sxs-lookup"><span data-stu-id="6415e-705"><span id="ERROR_SXS_XML_E_MISSINGSEMICOLON"></span><span id="error_sxs_xml_e_missingsemicolon"></span>**ERROR\_SXS\_XML\_E\_MISSINGSEMICOLON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-706">14039 (0x36D7)</span><span class="sxs-lookup"><span data-stu-id="6415e-706">14039 (0x36D7)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-707">Errore di analisi del manifesto: previsto punto e virgola.</span><span class="sxs-lookup"><span data-stu-id="6415e-707">Manifest Parse Error : A semi colon character was expected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-708"><span id="ERROR_SXS_XML_E_UNBALANCEDPAREN"></span><span id="error_sxs_xml_e_unbalancedparen"></span>**ERRORE \_ SxS \_ XML \_ E \_ UNBALANCEDPAREN**</span><span class="sxs-lookup"><span data-stu-id="6415e-708"><span id="ERROR_SXS_XML_E_UNBALANCEDPAREN"></span><span id="error_sxs_xml_e_unbalancedparen"></span>**ERROR\_SXS\_XML\_E\_UNBALANCEDPAREN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-709">14040 (0x36D8)</span><span class="sxs-lookup"><span data-stu-id="6415e-709">14040 (0x36D8)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-710">Errore di analisi del manifesto: parentesi non bilanciate.</span><span class="sxs-lookup"><span data-stu-id="6415e-710">Manifest Parse Error : Unbalanced parentheses.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-711"><span id="ERROR_SXS_XML_E_INTERNALERROR"></span><span id="error_sxs_xml_e_internalerror"></span>**ERRORE \_ SxS \_ XML \_ E \_ INTERNALERROR**</span><span class="sxs-lookup"><span data-stu-id="6415e-711"><span id="ERROR_SXS_XML_E_INTERNALERROR"></span><span id="error_sxs_xml_e_internalerror"></span>**ERROR\_SXS\_XML\_E\_INTERNALERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-712">14041 (0x36D9)</span><span class="sxs-lookup"><span data-stu-id="6415e-712">14041 (0x36D9)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-713">Errore di analisi del manifesto: errore interno.</span><span class="sxs-lookup"><span data-stu-id="6415e-713">Manifest Parse Error : Internal error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-714"><span id="ERROR_SXS_XML_E_UNEXPECTED_WHITESPACE"></span><span id="error_sxs_xml_e_unexpected_whitespace"></span>**ERRORE \_ SxS \_ XML \_ E \_ \_ spazio vuoto imprevisto**</span><span class="sxs-lookup"><span data-stu-id="6415e-714"><span id="ERROR_SXS_XML_E_UNEXPECTED_WHITESPACE"></span><span id="error_sxs_xml_e_unexpected_whitespace"></span>**ERROR\_SXS\_XML\_E\_UNEXPECTED\_WHITESPACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-715">14042 (0x36DA)</span><span class="sxs-lookup"><span data-stu-id="6415e-715">14042 (0x36DA)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-716">Errore di analisi del manifesto: lo spazio vuoto non è consentito in questa posizione.</span><span class="sxs-lookup"><span data-stu-id="6415e-716">Manifest Parse Error : Whitespace is not allowed at this location.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-717"><span id="ERROR_SXS_XML_E_INCOMPLETE_ENCODING"></span><span id="error_sxs_xml_e_incomplete_encoding"></span>**ERRORE \_ SxS \_ XML \_ E \_ codifica incompleta \_**</span><span class="sxs-lookup"><span data-stu-id="6415e-717"><span id="ERROR_SXS_XML_E_INCOMPLETE_ENCODING"></span><span id="error_sxs_xml_e_incomplete_encoding"></span>**ERROR\_SXS\_XML\_E\_INCOMPLETE\_ENCODING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-718">14043 (0x36DB)</span><span class="sxs-lookup"><span data-stu-id="6415e-718">14043 (0x36DB)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-719">Errore di analisi del manifesto: la fine del file è stata raggiunta in stato non valido per la codifica corrente.</span><span class="sxs-lookup"><span data-stu-id="6415e-719">Manifest Parse Error : End of file reached in invalid state for current encoding.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-720"><span id="ERROR_SXS_XML_E_MISSING_PAREN"></span><span id="error_sxs_xml_e_missing_paren"></span>**ERRORE \_ SxS \_ XML \_ E \_ \_ parentesi mancante**</span><span class="sxs-lookup"><span data-stu-id="6415e-720"><span id="ERROR_SXS_XML_E_MISSING_PAREN"></span><span id="error_sxs_xml_e_missing_paren"></span>**ERROR\_SXS\_XML\_E\_MISSING\_PAREN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-721">14044 (0x36DC)</span><span class="sxs-lookup"><span data-stu-id="6415e-721">14044 (0x36DC)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-722">Errore di analisi del manifesto: parentesi mancante.</span><span class="sxs-lookup"><span data-stu-id="6415e-722">Manifest Parse Error : Missing parenthesis.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-723"><span id="ERROR_SXS_XML_E_EXPECTINGCLOSEQUOTE"></span><span id="error_sxs_xml_e_expectingclosequote"></span>**ERRORE \_ SxS \_ XML \_ E \_ EXPECTINGCLOSEQUOTE**</span><span class="sxs-lookup"><span data-stu-id="6415e-723"><span id="ERROR_SXS_XML_E_EXPECTINGCLOSEQUOTE"></span><span id="error_sxs_xml_e_expectingclosequote"></span>**ERROR\_SXS\_XML\_E\_EXPECTINGCLOSEQUOTE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-724">14045 (0x36DD)</span><span class="sxs-lookup"><span data-stu-id="6415e-724">14045 (0x36DD)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-725">Errore di analisi del manifesto: virgolette di chiusura singole o doppie ( \\ ' o \\ ") mancanti.</span><span class="sxs-lookup"><span data-stu-id="6415e-725">Manifest Parse Error : A single or double closing quote character (\\' or \\") is missing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-726"><span id="ERROR_SXS_XML_E_MULTIPLE_COLONS"></span><span id="error_sxs_xml_e_multiple_colons"></span>**ERROR \_ SxS \_ XML \_ E \_ più \_ due punti**</span><span class="sxs-lookup"><span data-stu-id="6415e-726"><span id="ERROR_SXS_XML_E_MULTIPLE_COLONS"></span><span id="error_sxs_xml_e_multiple_colons"></span>**ERROR\_SXS\_XML\_E\_MULTIPLE\_COLONS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-727">14046 (0x36DE)</span><span class="sxs-lookup"><span data-stu-id="6415e-727">14046 (0x36DE)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-728">Errore di analisi del manifesto: non sono consentiti più due punti in un nome.</span><span class="sxs-lookup"><span data-stu-id="6415e-728">Manifest Parse Error : Multiple colons are not allowed in a name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-729"><span id="ERROR_SXS_XML_E_INVALID_DECIMAL"></span><span id="error_sxs_xml_e_invalid_decimal"></span>**ERRORE \_ SxS \_ XML \_ E \_ \_ decimale non valido**</span><span class="sxs-lookup"><span data-stu-id="6415e-729"><span id="ERROR_SXS_XML_E_INVALID_DECIMAL"></span><span id="error_sxs_xml_e_invalid_decimal"></span>**ERROR\_SXS\_XML\_E\_INVALID\_DECIMAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-730">14047 (0x36DF)</span><span class="sxs-lookup"><span data-stu-id="6415e-730">14047 (0x36DF)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-731">Errore di analisi del manifesto: carattere non valido per la cifra decimale.</span><span class="sxs-lookup"><span data-stu-id="6415e-731">Manifest Parse Error : Invalid character for decimal digit.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-732"><span id="ERROR_SXS_XML_E_INVALID_HEXIDECIMAL"></span><span id="error_sxs_xml_e_invalid_hexidecimal"></span>**ERRORE \_ SxS \_ XML \_ E \_ esadecimali non valido \_**</span><span class="sxs-lookup"><span data-stu-id="6415e-732"><span id="ERROR_SXS_XML_E_INVALID_HEXIDECIMAL"></span><span id="error_sxs_xml_e_invalid_hexidecimal"></span>**ERROR\_SXS\_XML\_E\_INVALID\_HEXIDECIMAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-733">14048 (0x36E0)</span><span class="sxs-lookup"><span data-stu-id="6415e-733">14048 (0x36E0)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-734">Errore di analisi del manifesto: carattere non valido per la cifra esadecimale.</span><span class="sxs-lookup"><span data-stu-id="6415e-734">Manifest Parse Error : Invalid character for hexadecimal digit.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-735"><span id="ERROR_SXS_XML_E_INVALID_UNICODE"></span><span id="error_sxs_xml_e_invalid_unicode"></span>**ERROR \_ SxS \_ XML \_ E \_ Unicode non valido \_**</span><span class="sxs-lookup"><span data-stu-id="6415e-735"><span id="ERROR_SXS_XML_E_INVALID_UNICODE"></span><span id="error_sxs_xml_e_invalid_unicode"></span>**ERROR\_SXS\_XML\_E\_INVALID\_UNICODE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-736">14049 (0x36E1)</span><span class="sxs-lookup"><span data-stu-id="6415e-736">14049 (0x36E1)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-737">Errore di analisi del manifesto: valore del carattere Unicode non valido per questa piattaforma.</span><span class="sxs-lookup"><span data-stu-id="6415e-737">Manifest Parse Error : Invalid unicode character value for this platform.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-738"><span id="ERROR_SXS_XML_E_WHITESPACEORQUESTIONMARK"></span><span id="error_sxs_xml_e_whitespaceorquestionmark"></span>**ERRORE \_ SxS \_ XML \_ E \_ WHITESPACEORQUESTIONMARK**</span><span class="sxs-lookup"><span data-stu-id="6415e-738"><span id="ERROR_SXS_XML_E_WHITESPACEORQUESTIONMARK"></span><span id="error_sxs_xml_e_whitespaceorquestionmark"></span>**ERROR\_SXS\_XML\_E\_WHITESPACEORQUESTIONMARK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-739">14050 (0x36E2)</span><span class="sxs-lookup"><span data-stu-id="6415e-739">14050 (0x36E2)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-740">Errore di analisi del manifesto: è previsto uno spazio vuoto o '?'.</span><span class="sxs-lookup"><span data-stu-id="6415e-740">Manifest Parse Error : Expecting whitespace or '?'.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-741"><span id="ERROR_SXS_XML_E_UNEXPECTEDENDTAG"></span><span id="error_sxs_xml_e_unexpectedendtag"></span>**ERRORE \_ SxS \_ XML \_ E \_ UNEXPECTEDENDTAG**</span><span class="sxs-lookup"><span data-stu-id="6415e-741"><span id="ERROR_SXS_XML_E_UNEXPECTEDENDTAG"></span><span id="error_sxs_xml_e_unexpectedendtag"></span>**ERROR\_SXS\_XML\_E\_UNEXPECTEDENDTAG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-742">14051 (0x36E3)</span><span class="sxs-lookup"><span data-stu-id="6415e-742">14051 (0x36E3)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-743">Errore di analisi del manifesto: il tag di fine non era previsto in questa posizione.</span><span class="sxs-lookup"><span data-stu-id="6415e-743">Manifest Parse Error : End tag was not expected at this location.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-744"><span id="ERROR_SXS_XML_E_UNCLOSEDTAG"></span><span id="error_sxs_xml_e_unclosedtag"></span>**ERRORE \_ SxS \_ XML \_ E \_ UNCLOSEDTAG**</span><span class="sxs-lookup"><span data-stu-id="6415e-744"><span id="ERROR_SXS_XML_E_UNCLOSEDTAG"></span><span id="error_sxs_xml_e_unclosedtag"></span>**ERROR\_SXS\_XML\_E\_UNCLOSEDTAG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-745">14052 (0x36E4)</span><span class="sxs-lookup"><span data-stu-id="6415e-745">14052 (0x36E4)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-746">Errore di analisi del manifesto: i seguenti tag non sono stati chiusi: %1.</span><span class="sxs-lookup"><span data-stu-id="6415e-746">Manifest Parse Error : The following tags were not closed: %1.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-747"><span id="ERROR_SXS_XML_E_DUPLICATEATTRIBUTE"></span><span id="error_sxs_xml_e_duplicateattribute"></span>**ERRORE \_ SxS \_ XML \_ E \_ DUPLICATEATTRIBUTE**</span><span class="sxs-lookup"><span data-stu-id="6415e-747"><span id="ERROR_SXS_XML_E_DUPLICATEATTRIBUTE"></span><span id="error_sxs_xml_e_duplicateattribute"></span>**ERROR\_SXS\_XML\_E\_DUPLICATEATTRIBUTE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-748">14053 (0x36E5)</span><span class="sxs-lookup"><span data-stu-id="6415e-748">14053 (0x36E5)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-749">Errore di analisi del manifesto: attributo duplicato.</span><span class="sxs-lookup"><span data-stu-id="6415e-749">Manifest Parse Error : Duplicate attribute.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-750"><span id="ERROR_SXS_XML_E_MULTIPLEROOTS"></span><span id="error_sxs_xml_e_multipleroots"></span>**ERRORE \_ SxS \_ XML \_ E \_ MULTIPLEROOTS**</span><span class="sxs-lookup"><span data-stu-id="6415e-750"><span id="ERROR_SXS_XML_E_MULTIPLEROOTS"></span><span id="error_sxs_xml_e_multipleroots"></span>**ERROR\_SXS\_XML\_E\_MULTIPLEROOTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-751">14054 (0x36E6)</span><span class="sxs-lookup"><span data-stu-id="6415e-751">14054 (0x36E6)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-752">Errore di analisi del manifesto: in un documento XML è consentito un solo elemento di primo livello.</span><span class="sxs-lookup"><span data-stu-id="6415e-752">Manifest Parse Error : Only one top level element is allowed in an XML document.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-753"><span id="ERROR_SXS_XML_E_INVALIDATROOTLEVEL"></span><span id="error_sxs_xml_e_invalidatrootlevel"></span>**ERRORE \_ SxS \_ XML \_ E \_ INVALIDATROOTLEVEL**</span><span class="sxs-lookup"><span data-stu-id="6415e-753"><span id="ERROR_SXS_XML_E_INVALIDATROOTLEVEL"></span><span id="error_sxs_xml_e_invalidatrootlevel"></span>**ERROR\_SXS\_XML\_E\_INVALIDATROOTLEVEL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-754">14055 (0x36E7)</span><span class="sxs-lookup"><span data-stu-id="6415e-754">14055 (0x36E7)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-755">Errore di analisi del manifesto: non valido al livello principale del documento.</span><span class="sxs-lookup"><span data-stu-id="6415e-755">Manifest Parse Error : Invalid at the top level of the document.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-756"><span id="ERROR_SXS_XML_E_BADXMLDECL"></span><span id="error_sxs_xml_e_badxmldecl"></span>**ERRORE \_ SxS \_ XML \_ E \_ BADXMLDECL**</span><span class="sxs-lookup"><span data-stu-id="6415e-756"><span id="ERROR_SXS_XML_E_BADXMLDECL"></span><span id="error_sxs_xml_e_badxmldecl"></span>**ERROR\_SXS\_XML\_E\_BADXMLDECL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-757">14056 (0x36E8)</span><span class="sxs-lookup"><span data-stu-id="6415e-757">14056 (0x36E8)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-758">Errore di analisi del manifesto: dichiarazione XML non valida.</span><span class="sxs-lookup"><span data-stu-id="6415e-758">Manifest Parse Error : Invalid xml declaration.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-759"><span id="ERROR_SXS_XML_E_MISSINGROOT"></span><span id="error_sxs_xml_e_missingroot"></span>**ERRORE \_ SxS \_ XML \_ E \_ MISSINGROOT**</span><span class="sxs-lookup"><span data-stu-id="6415e-759"><span id="ERROR_SXS_XML_E_MISSINGROOT"></span><span id="error_sxs_xml_e_missingroot"></span>**ERROR\_SXS\_XML\_E\_MISSINGROOT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-760">14057 (0x36E9)</span><span class="sxs-lookup"><span data-stu-id="6415e-760">14057 (0x36E9)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-761">Errore di analisi del manifesto: il documento XML deve contenere un elemento di livello principale.</span><span class="sxs-lookup"><span data-stu-id="6415e-761">Manifest Parse Error : XML document must have a top level element.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-762"><span id="ERROR_SXS_XML_E_UNEXPECTEDEOF"></span><span id="error_sxs_xml_e_unexpectedeof"></span>**ERRORE \_ SxS \_ XML \_ E \_ UNEXPECTEDEOF**</span><span class="sxs-lookup"><span data-stu-id="6415e-762"><span id="ERROR_SXS_XML_E_UNEXPECTEDEOF"></span><span id="error_sxs_xml_e_unexpectedeof"></span>**ERROR\_SXS\_XML\_E\_UNEXPECTEDEOF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-763">14058 (0x36EA)</span><span class="sxs-lookup"><span data-stu-id="6415e-763">14058 (0x36EA)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-764">Errore di analisi del manifesto: fine del file imprevista.</span><span class="sxs-lookup"><span data-stu-id="6415e-764">Manifest Parse Error : Unexpected end of file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-765"><span id="ERROR_SXS_XML_E_BADPEREFINSUBSET"></span><span id="error_sxs_xml_e_badperefinsubset"></span>**ERRORE \_ SxS \_ XML \_ E \_ BADPEREFINSUBSET**</span><span class="sxs-lookup"><span data-stu-id="6415e-765"><span id="ERROR_SXS_XML_E_BADPEREFINSUBSET"></span><span id="error_sxs_xml_e_badperefinsubset"></span>**ERROR\_SXS\_XML\_E\_BADPEREFINSUBSET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-766">14059 (0x36EB)</span><span class="sxs-lookup"><span data-stu-id="6415e-766">14059 (0x36EB)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-767">Errore di analisi del manifesto: le entità parametro non possono essere usate nelle dichiarazioni di markup in un subset interno.</span><span class="sxs-lookup"><span data-stu-id="6415e-767">Manifest Parse Error : Parameter entities cannot be used inside markup declarations in an internal subset.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-768"><span id="ERROR_SXS_XML_E_UNCLOSEDSTARTTAG"></span><span id="error_sxs_xml_e_unclosedstarttag"></span>**ERRORE \_ SxS \_ XML \_ E \_ UNCLOSEDSTARTTAG**</span><span class="sxs-lookup"><span data-stu-id="6415e-768"><span id="ERROR_SXS_XML_E_UNCLOSEDSTARTTAG"></span><span id="error_sxs_xml_e_unclosedstarttag"></span>**ERROR\_SXS\_XML\_E\_UNCLOSEDSTARTTAG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-769">14060 (0x36EC)</span><span class="sxs-lookup"><span data-stu-id="6415e-769">14060 (0x36EC)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-770">Errore di analisi del manifesto: l'elemento non è stato chiuso.</span><span class="sxs-lookup"><span data-stu-id="6415e-770">Manifest Parse Error : Element was not closed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-771"><span id="ERROR_SXS_XML_E_UNCLOSEDENDTAG"></span><span id="error_sxs_xml_e_unclosedendtag"></span>**ERRORE \_ SxS \_ XML \_ E \_ UNCLOSEDENDTAG**</span><span class="sxs-lookup"><span data-stu-id="6415e-771"><span id="ERROR_SXS_XML_E_UNCLOSEDENDTAG"></span><span id="error_sxs_xml_e_unclosedendtag"></span>**ERROR\_SXS\_XML\_E\_UNCLOSEDENDTAG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-772">14061 (0x36ED)</span><span class="sxs-lookup"><span data-stu-id="6415e-772">14061 (0x36ED)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-773">Errore di analisi del manifesto: nell'elemento End manca il carattere ' >'.</span><span class="sxs-lookup"><span data-stu-id="6415e-773">Manifest Parse Error : End element was missing the character '>'.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-774"><span id="ERROR_SXS_XML_E_UNCLOSEDSTRING"></span><span id="error_sxs_xml_e_unclosedstring"></span>**ERRORE \_ SxS \_ XML \_ E \_ UNCLOSEDSTRING**</span><span class="sxs-lookup"><span data-stu-id="6415e-774"><span id="ERROR_SXS_XML_E_UNCLOSEDSTRING"></span><span id="error_sxs_xml_e_unclosedstring"></span>**ERROR\_SXS\_XML\_E\_UNCLOSEDSTRING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-775">14062 (0x36EE)</span><span class="sxs-lookup"><span data-stu-id="6415e-775">14062 (0x36EE)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-776">Errore di analisi del manifesto: un valore letterale stringa non è stato chiuso.</span><span class="sxs-lookup"><span data-stu-id="6415e-776">Manifest Parse Error : A string literal was not closed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-777"><span id="ERROR_SXS_XML_E_UNCLOSEDCOMMENT"></span><span id="error_sxs_xml_e_unclosedcomment"></span>**ERRORE \_ SxS \_ XML \_ E \_ UNCLOSEDCOMMENT**</span><span class="sxs-lookup"><span data-stu-id="6415e-777"><span id="ERROR_SXS_XML_E_UNCLOSEDCOMMENT"></span><span id="error_sxs_xml_e_unclosedcomment"></span>**ERROR\_SXS\_XML\_E\_UNCLOSEDCOMMENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-778">14063 (0x36EF)</span><span class="sxs-lookup"><span data-stu-id="6415e-778">14063 (0x36EF)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-779">Errore di analisi del manifesto: un commento non è stato chiuso.</span><span class="sxs-lookup"><span data-stu-id="6415e-779">Manifest Parse Error : A comment was not closed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-780"><span id="ERROR_SXS_XML_E_UNCLOSEDDECL"></span><span id="error_sxs_xml_e_uncloseddecl"></span>**ERRORE \_ SxS \_ XML \_ E \_ UNCLOSEDDECL**</span><span class="sxs-lookup"><span data-stu-id="6415e-780"><span id="ERROR_SXS_XML_E_UNCLOSEDDECL"></span><span id="error_sxs_xml_e_uncloseddecl"></span>**ERROR\_SXS\_XML\_E\_UNCLOSEDDECL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-781">14064 (0x36F0)</span><span class="sxs-lookup"><span data-stu-id="6415e-781">14064 (0x36F0)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-782">Errore di analisi del manifesto: una dichiarazione non è stata chiusa.</span><span class="sxs-lookup"><span data-stu-id="6415e-782">Manifest Parse Error : A declaration was not closed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-783"><span id="ERROR_SXS_XML_E_UNCLOSEDCDATA"></span><span id="error_sxs_xml_e_unclosedcdata"></span>**ERRORE \_ SxS \_ XML \_ E \_ UNCLOSEDCDATA**</span><span class="sxs-lookup"><span data-stu-id="6415e-783"><span id="ERROR_SXS_XML_E_UNCLOSEDCDATA"></span><span id="error_sxs_xml_e_unclosedcdata"></span>**ERROR\_SXS\_XML\_E\_UNCLOSEDCDATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-784">14065 (0x36F1)</span><span class="sxs-lookup"><span data-stu-id="6415e-784">14065 (0x36F1)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-785">Errore di analisi del manifesto: una sezione CDATA non è stata chiusa.</span><span class="sxs-lookup"><span data-stu-id="6415e-785">Manifest Parse Error : A CDATA section was not closed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-786"><span id="ERROR_SXS_XML_E_RESERVEDNAMESPACE"></span><span id="error_sxs_xml_e_reservednamespace"></span>**ERRORE \_ SxS \_ XML \_ E \_ RESERVEDNAMESPACE**</span><span class="sxs-lookup"><span data-stu-id="6415e-786"><span id="ERROR_SXS_XML_E_RESERVEDNAMESPACE"></span><span id="error_sxs_xml_e_reservednamespace"></span>**ERROR\_SXS\_XML\_E\_RESERVEDNAMESPACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-787">14066 (0x36F2)</span><span class="sxs-lookup"><span data-stu-id="6415e-787">14066 (0x36F2)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-788">Errore di analisi del manifesto: il prefisso dello spazio dei nomi non può iniziare con la stringa riservata "XML".</span><span class="sxs-lookup"><span data-stu-id="6415e-788">Manifest Parse Error : The namespace prefix is not allowed to start with the reserved string "xml".</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-789"><span id="ERROR_SXS_XML_E_INVALIDENCODING"></span><span id="error_sxs_xml_e_invalidencoding"></span>**ERRORE \_ SxS \_ XML \_ E \_ INVALIDENCODING**</span><span class="sxs-lookup"><span data-stu-id="6415e-789"><span id="ERROR_SXS_XML_E_INVALIDENCODING"></span><span id="error_sxs_xml_e_invalidencoding"></span>**ERROR\_SXS\_XML\_E\_INVALIDENCODING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-790">14067 (0x36F3)</span><span class="sxs-lookup"><span data-stu-id="6415e-790">14067 (0x36F3)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-791">Errore di analisi del manifesto: il sistema non supporta la codifica specificata.</span><span class="sxs-lookup"><span data-stu-id="6415e-791">Manifest Parse Error : System does not support the specified encoding.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-792"><span id="ERROR_SXS_XML_E_INVALIDSWITCH"></span><span id="error_sxs_xml_e_invalidswitch"></span>**ERRORE \_ SxS \_ XML \_ E \_ INVALIDSWITCH**</span><span class="sxs-lookup"><span data-stu-id="6415e-792"><span id="ERROR_SXS_XML_E_INVALIDSWITCH"></span><span id="error_sxs_xml_e_invalidswitch"></span>**ERROR\_SXS\_XML\_E\_INVALIDSWITCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-793">14068 (0x36F4)</span><span class="sxs-lookup"><span data-stu-id="6415e-793">14068 (0x36F4)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-794">Errore di analisi del manifesto: l'opzione dalla codifica corrente alla codifica specificata non è supportata.</span><span class="sxs-lookup"><span data-stu-id="6415e-794">Manifest Parse Error : Switch from current encoding to specified encoding not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-795"><span id="ERROR_SXS_XML_E_BADXMLCASE"></span><span id="error_sxs_xml_e_badxmlcase"></span>**ERRORE \_ SxS \_ XML \_ E \_ BADXMLCASE**</span><span class="sxs-lookup"><span data-stu-id="6415e-795"><span id="ERROR_SXS_XML_E_BADXMLCASE"></span><span id="error_sxs_xml_e_badxmlcase"></span>**ERROR\_SXS\_XML\_E\_BADXMLCASE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-796">14069 (0x36F5)</span><span class="sxs-lookup"><span data-stu-id="6415e-796">14069 (0x36F5)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-797">Errore di analisi del manifesto: il nome "XML" è riservato e deve essere in lettere minuscole.</span><span class="sxs-lookup"><span data-stu-id="6415e-797">Manifest Parse Error : The name 'xml' is reserved and must be lower case.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-798"><span id="ERROR_SXS_XML_E_INVALID_STANDALONE"></span><span id="error_sxs_xml_e_invalid_standalone"></span>**ERRORE \_ SxS \_ XML \_ E \_ \_ autonomo non valido**</span><span class="sxs-lookup"><span data-stu-id="6415e-798"><span id="ERROR_SXS_XML_E_INVALID_STANDALONE"></span><span id="error_sxs_xml_e_invalid_standalone"></span>**ERROR\_SXS\_XML\_E\_INVALID\_STANDALONE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-799">14070 (0x36F6)</span><span class="sxs-lookup"><span data-stu-id="6415e-799">14070 (0x36F6)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-800">Errore di analisi del manifesto: il valore dell'attributo standalone deve essere ' Yes ' o ' No '.</span><span class="sxs-lookup"><span data-stu-id="6415e-800">Manifest Parse Error : The standalone attribute must have the value 'yes' or 'no'.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-801"><span id="ERROR_SXS_XML_E_UNEXPECTED_STANDALONE"></span><span id="error_sxs_xml_e_unexpected_standalone"></span>**ERROR \_ SxS \_ XML \_ E \_ imprevisto \_ autonomo**</span><span class="sxs-lookup"><span data-stu-id="6415e-801"><span id="ERROR_SXS_XML_E_UNEXPECTED_STANDALONE"></span><span id="error_sxs_xml_e_unexpected_standalone"></span>**ERROR\_SXS\_XML\_E\_UNEXPECTED\_STANDALONE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-802">14071 (0x36F7)</span><span class="sxs-lookup"><span data-stu-id="6415e-802">14071 (0x36F7)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-803">Errore di analisi del manifesto: l'attributo standalone non può essere utilizzato in entità esterne.</span><span class="sxs-lookup"><span data-stu-id="6415e-803">Manifest Parse Error : The standalone attribute cannot be used in external entities.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-804"><span id="ERROR_SXS_XML_E_INVALID_VERSION"></span><span id="error_sxs_xml_e_invalid_version"></span>**ERRORE \_ SxS \_ XML \_ E \_ versione non valida \_**</span><span class="sxs-lookup"><span data-stu-id="6415e-804"><span id="ERROR_SXS_XML_E_INVALID_VERSION"></span><span id="error_sxs_xml_e_invalid_version"></span>**ERROR\_SXS\_XML\_E\_INVALID\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-805">14072 (0x36F8)</span><span class="sxs-lookup"><span data-stu-id="6415e-805">14072 (0x36F8)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-806">Errore di analisi del manifesto: numero di versione non valido.</span><span class="sxs-lookup"><span data-stu-id="6415e-806">Manifest Parse Error : Invalid version number.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-807"><span id="ERROR_SXS_XML_E_MISSINGEQUALS"></span><span id="error_sxs_xml_e_missingequals"></span>**ERRORE \_ SxS \_ XML \_ E \_ MISSINGEQUALS**</span><span class="sxs-lookup"><span data-stu-id="6415e-807"><span id="ERROR_SXS_XML_E_MISSINGEQUALS"></span><span id="error_sxs_xml_e_missingequals"></span>**ERROR\_SXS\_XML\_E\_MISSINGEQUALS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-808">14073 (0x36F9)</span><span class="sxs-lookup"><span data-stu-id="6415e-808">14073 (0x36F9)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-809">Errore di analisi del manifesto: manca il segno di uguale tra l'attributo e il valore dell'attributo.</span><span class="sxs-lookup"><span data-stu-id="6415e-809">Manifest Parse Error : Missing equals sign between attribute and attribute value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-810"><span id="ERROR_SXS_PROTECTION_RECOVERY_FAILED"></span><span id="error_sxs_protection_recovery_failed"></span>**errore durante il \_ \_ ripristino della protezione SxS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6415e-810"><span id="ERROR_SXS_PROTECTION_RECOVERY_FAILED"></span><span id="error_sxs_protection_recovery_failed"></span>**ERROR\_SXS\_PROTECTION\_RECOVERY\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-811">14074 (0x36FA)</span><span class="sxs-lookup"><span data-stu-id="6415e-811">14074 (0x36FA)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-812">Errore di protezione dell'assembly: Impossibile recuperare l'assembly specificato.</span><span class="sxs-lookup"><span data-stu-id="6415e-812">Assembly Protection Error : Unable to recover the specified assembly.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-813"><span id="ERROR_SXS_PROTECTION_PUBLIC_KEY_TOO_SHORT"></span><span id="error_sxs_protection_public_key_too_short"></span>**\_chiave pubblica di errore SxS \_ Protection \_ \_ \_ troppo \_ breve**</span><span class="sxs-lookup"><span data-stu-id="6415e-813"><span id="ERROR_SXS_PROTECTION_PUBLIC_KEY_TOO_SHORT"></span><span id="error_sxs_protection_public_key_too_short"></span>**ERROR\_SXS\_PROTECTION\_PUBLIC\_KEY\_TOO\_SHORT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-814">14075 (0x36FB)</span><span class="sxs-lookup"><span data-stu-id="6415e-814">14075 (0x36FB)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-815">Errore di protezione dell'assembly: la chiave pubblica per un assembly è troppo corta per essere consentita.</span><span class="sxs-lookup"><span data-stu-id="6415e-815">Assembly Protection Error : The public key for an assembly was too short to be allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-816"><span id="ERROR_SXS_PROTECTION_CATALOG_NOT_VALID"></span><span id="error_sxs_protection_catalog_not_valid"></span>**ERRORE \_ \_ Catalogo protezione \_ SxS \_ non \_ valido**</span><span class="sxs-lookup"><span data-stu-id="6415e-816"><span id="ERROR_SXS_PROTECTION_CATALOG_NOT_VALID"></span><span id="error_sxs_protection_catalog_not_valid"></span>**ERROR\_SXS\_PROTECTION\_CATALOG\_NOT\_VALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-817">14076 (0x36FC)</span><span class="sxs-lookup"><span data-stu-id="6415e-817">14076 (0x36FC)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-818">Errore di protezione dell'assembly: il catalogo di un assembly non è valido o non corrisponde al manifesto dell'assembly.</span><span class="sxs-lookup"><span data-stu-id="6415e-818">Assembly Protection Error : The catalog for an assembly is not valid, or does not match the assembly's manifest.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-819"><span id="ERROR_SXS_UNTRANSLATABLE_HRESULT"></span><span id="error_sxs_untranslatable_hresult"></span>**ERRORE \_ SxS non \_ convertibile \_ SxS**</span><span class="sxs-lookup"><span data-stu-id="6415e-819"><span id="ERROR_SXS_UNTRANSLATABLE_HRESULT"></span><span id="error_sxs_untranslatable_hresult"></span>**ERROR\_SXS\_UNTRANSLATABLE\_HRESULT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-820">14077 (0x36FD)</span><span class="sxs-lookup"><span data-stu-id="6415e-820">14077 (0x36FD)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-821">Non è stato possibile convertire un valore HRESULT in un codice di errore Win32 corrispondente.</span><span class="sxs-lookup"><span data-stu-id="6415e-821">An HRESULT could not be translated to a corresponding Win32 error code.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-822"><span id="ERROR_SXS_PROTECTION_CATALOG_FILE_MISSING"></span><span id="error_sxs_protection_catalog_file_missing"></span>**errore \_ nel \_ \_ file di catalogo della protezione \_ SxS errore \_**</span><span class="sxs-lookup"><span data-stu-id="6415e-822"><span id="ERROR_SXS_PROTECTION_CATALOG_FILE_MISSING"></span><span id="error_sxs_protection_catalog_file_missing"></span>**ERROR\_SXS\_PROTECTION\_CATALOG\_FILE\_MISSING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-823">14078 (0x36FE)</span><span class="sxs-lookup"><span data-stu-id="6415e-823">14078 (0x36FE)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-824">Errore di protezione dell'assembly: manca il catalogo di un assembly.</span><span class="sxs-lookup"><span data-stu-id="6415e-824">Assembly Protection Error : The catalog for an assembly is missing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-825"><span id="ERROR_SXS_MISSING_ASSEMBLY_IDENTITY_ATTRIBUTE"></span><span id="error_sxs_missing_assembly_identity_attribute"></span>**\_attributo di \_ \_ identità assembly \_ mancante \_ nell'errore SxS**</span><span class="sxs-lookup"><span data-stu-id="6415e-825"><span id="ERROR_SXS_MISSING_ASSEMBLY_IDENTITY_ATTRIBUTE"></span><span id="error_sxs_missing_assembly_identity_attribute"></span>**ERROR\_SXS\_MISSING\_ASSEMBLY\_IDENTITY\_ATTRIBUTE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-826">14079 (0x36FF)</span><span class="sxs-lookup"><span data-stu-id="6415e-826">14079 (0x36FF)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-827">Nell'identità dell'assembly specificata mancano uno o più attributi che devono essere presenti in questo contesto.</span><span class="sxs-lookup"><span data-stu-id="6415e-827">The supplied assembly identity is missing one or more attributes which must be present in this context.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-828"><span id="ERROR_SXS_INVALID_ASSEMBLY_IDENTITY_ATTRIBUTE_NAME"></span><span id="error_sxs_invalid_assembly_identity_attribute_name"></span>**ERRORE \_ SxS \_ \_ \_ \_ nome attributo identità assembly \_ non valido**</span><span class="sxs-lookup"><span data-stu-id="6415e-828"><span id="ERROR_SXS_INVALID_ASSEMBLY_IDENTITY_ATTRIBUTE_NAME"></span><span id="error_sxs_invalid_assembly_identity_attribute_name"></span>**ERROR\_SXS\_INVALID\_ASSEMBLY\_IDENTITY\_ATTRIBUTE\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-829">14080 (0x3700)</span><span class="sxs-lookup"><span data-stu-id="6415e-829">14080 (0x3700)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-830">L'identità dell'assembly fornita ha uno o più nomi di attributo che contengono caratteri non consentiti nei nomi XML.</span><span class="sxs-lookup"><span data-stu-id="6415e-830">The supplied assembly identity has one or more attribute names that contain characters not permitted in XML names.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-831"><span id="ERROR_SXS_ASSEMBLY_MISSING"></span><span id="error_sxs_assembly_missing"></span>**ERRORE \_ \_ assembly SxS \_ mancante**</span><span class="sxs-lookup"><span data-stu-id="6415e-831"><span id="ERROR_SXS_ASSEMBLY_MISSING"></span><span id="error_sxs_assembly_missing"></span>**ERROR\_SXS\_ASSEMBLY\_MISSING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-832">14081 (0x3701)</span><span class="sxs-lookup"><span data-stu-id="6415e-832">14081 (0x3701)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-833">Impossibile trovare l'assembly a cui si fa riferimento.</span><span class="sxs-lookup"><span data-stu-id="6415e-833">The referenced assembly could not be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-834"><span id="ERROR_SXS_CORRUPT_ACTIVATION_STACK"></span><span id="error_sxs_corrupt_activation_stack"></span>**\_stack di \_ \_ attivazione danneggiato SxS di \_ errore**</span><span class="sxs-lookup"><span data-stu-id="6415e-834"><span id="ERROR_SXS_CORRUPT_ACTIVATION_STACK"></span><span id="error_sxs_corrupt_activation_stack"></span>**ERROR\_SXS\_CORRUPT\_ACTIVATION\_STACK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-835">14082 (0x3702)</span><span class="sxs-lookup"><span data-stu-id="6415e-835">14082 (0x3702)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-836">Lo stack di attivazione del contesto di attivazione per il thread in esecuzione è danneggiato.</span><span class="sxs-lookup"><span data-stu-id="6415e-836">The activation context activation stack for the running thread of execution is corrupt.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-837"><span id="ERROR_SXS_CORRUPTION"></span><span id="error_sxs_corruption"></span>**\_ \_ danneggiamento SxS errore**</span><span class="sxs-lookup"><span data-stu-id="6415e-837"><span id="ERROR_SXS_CORRUPTION"></span><span id="error_sxs_corruption"></span>**ERROR\_SXS\_CORRUPTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-838">14083 (0x3703)</span><span class="sxs-lookup"><span data-stu-id="6415e-838">14083 (0x3703)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-839">I metadati di isolamento dell'applicazione per questo processo o thread sono diventati danneggiati.</span><span class="sxs-lookup"><span data-stu-id="6415e-839">The application isolation metadata for this process or thread has become corrupt.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-840"><span id="ERROR_SXS_EARLY_DEACTIVATION"></span><span id="error_sxs_early_deactivation"></span>**ERRORE \_ SxS \_ prima di \_ disattivazione**</span><span class="sxs-lookup"><span data-stu-id="6415e-840"><span id="ERROR_SXS_EARLY_DEACTIVATION"></span><span id="error_sxs_early_deactivation"></span>**ERROR\_SXS\_EARLY\_DEACTIVATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-841">14084 (0x3704)</span><span class="sxs-lookup"><span data-stu-id="6415e-841">14084 (0x3704)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-842">Il contesto di attivazione da disattivare non è quello attivato più di recente.</span><span class="sxs-lookup"><span data-stu-id="6415e-842">The activation context being deactivated is not the most recently activated one.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-843"><span id="ERROR_SXS_INVALID_DEACTIVATION"></span><span id="error_sxs_invalid_deactivation"></span>**ERRORE \_ SxS \_ non valido di \_ disattivazione**</span><span class="sxs-lookup"><span data-stu-id="6415e-843"><span id="ERROR_SXS_INVALID_DEACTIVATION"></span><span id="error_sxs_invalid_deactivation"></span>**ERROR\_SXS\_INVALID\_DEACTIVATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-844">14085 (0x3705)</span><span class="sxs-lookup"><span data-stu-id="6415e-844">14085 (0x3705)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-845">Il contesto di attivazione da disattivare non è attivo per il thread di esecuzione corrente.</span><span class="sxs-lookup"><span data-stu-id="6415e-845">The activation context being deactivated is not active for the current thread of execution.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-846"><span id="ERROR_SXS_MULTIPLE_DEACTIVATION"></span><span id="error_sxs_multiple_deactivation"></span>**ERRORE \_ SxS \_ più \_ disattivazione**</span><span class="sxs-lookup"><span data-stu-id="6415e-846"><span id="ERROR_SXS_MULTIPLE_DEACTIVATION"></span><span id="error_sxs_multiple_deactivation"></span>**ERROR\_SXS\_MULTIPLE\_DEACTIVATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-847">14086 (0x3706)</span><span class="sxs-lookup"><span data-stu-id="6415e-847">14086 (0x3706)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-848">Il contesto di attivazione disattivato è già stato disattivato.</span><span class="sxs-lookup"><span data-stu-id="6415e-848">The activation context being deactivated has already been deactivated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-849"><span id="ERROR_SXS_PROCESS_TERMINATION_REQUESTED"></span><span id="error_sxs_process_termination_requested"></span>**\_terminazione del processo SxS di errore \_ \_ \_ richiesta**</span><span class="sxs-lookup"><span data-stu-id="6415e-849"><span id="ERROR_SXS_PROCESS_TERMINATION_REQUESTED"></span><span id="error_sxs_process_termination_requested"></span>**ERROR\_SXS\_PROCESS\_TERMINATION\_REQUESTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-850">14087 (0x3707)</span><span class="sxs-lookup"><span data-stu-id="6415e-850">14087 (0x3707)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-851">Un componente utilizzato dalla funzionalità di isolamento ha richiesto l'interruzione del processo.</span><span class="sxs-lookup"><span data-stu-id="6415e-851">A component used by the isolation facility has requested to terminate the process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-852"><span id="ERROR_SXS_RELEASE_ACTIVATION_CONTEXT"></span><span id="error_sxs_release_activation_context"></span>**\_contesto di \_ attivazione della versione SxS \_ di errore \_**</span><span class="sxs-lookup"><span data-stu-id="6415e-852"><span id="ERROR_SXS_RELEASE_ACTIVATION_CONTEXT"></span><span id="error_sxs_release_activation_context"></span>**ERROR\_SXS\_RELEASE\_ACTIVATION\_CONTEXT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-853">14088 (0x3708)</span><span class="sxs-lookup"><span data-stu-id="6415e-853">14088 (0x3708)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-854">Un componente in modalità kernel sta rilasciando un riferimento in un contesto di attivazione.</span><span class="sxs-lookup"><span data-stu-id="6415e-854">A kernel mode component is releasing a reference on an activation context.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-855"><span id="ERROR_SXS_SYSTEM_DEFAULT_ACTIVATION_CONTEXT_EMPTY"></span><span id="error_sxs_system_default_activation_context_empty"></span>**ERRORE \_ nel \_ \_ contesto di attivazione predefinito del sistema SxS \_ \_ \_ vuoto**</span><span class="sxs-lookup"><span data-stu-id="6415e-855"><span id="ERROR_SXS_SYSTEM_DEFAULT_ACTIVATION_CONTEXT_EMPTY"></span><span id="error_sxs_system_default_activation_context_empty"></span>**ERROR\_SXS\_SYSTEM\_DEFAULT\_ACTIVATION\_CONTEXT\_EMPTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-856">14089 (0x3709)</span><span class="sxs-lookup"><span data-stu-id="6415e-856">14089 (0x3709)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-857">Impossibile generare il contesto di attivazione dell'assembly predefinito di sistema.</span><span class="sxs-lookup"><span data-stu-id="6415e-857">The activation context of system default assembly could not be generated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-858"><span id="ERROR_SXS_INVALID_IDENTITY_ATTRIBUTE_VALUE"></span><span id="error_sxs_invalid_identity_attribute_value"></span>**ERRORE \_ SxS \_ \_ valore dell' \_ attributo \_ Identity non valido**</span><span class="sxs-lookup"><span data-stu-id="6415e-858"><span id="ERROR_SXS_INVALID_IDENTITY_ATTRIBUTE_VALUE"></span><span id="error_sxs_invalid_identity_attribute_value"></span>**ERROR\_SXS\_INVALID\_IDENTITY\_ATTRIBUTE\_VALUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-859">14090 (0x370A)</span><span class="sxs-lookup"><span data-stu-id="6415e-859">14090 (0x370A)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-860">Il valore di un attributo in un'identità non è compreso nell'intervallo valido.</span><span class="sxs-lookup"><span data-stu-id="6415e-860">The value of an attribute in an identity is not within the legal range.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-861"><span id="ERROR_SXS_INVALID_IDENTITY_ATTRIBUTE_NAME"></span><span id="error_sxs_invalid_identity_attribute_name"></span>**ERRORE \_ SxS \_ \_ \_ nome attributo identità non valido \_**</span><span class="sxs-lookup"><span data-stu-id="6415e-861"><span id="ERROR_SXS_INVALID_IDENTITY_ATTRIBUTE_NAME"></span><span id="error_sxs_invalid_identity_attribute_name"></span>**ERROR\_SXS\_INVALID\_IDENTITY\_ATTRIBUTE\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-862">14091 (0x370B)</span><span class="sxs-lookup"><span data-stu-id="6415e-862">14091 (0x370B)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-863">Il nome di un attributo in un'identità non è compreso nell'intervallo valido.</span><span class="sxs-lookup"><span data-stu-id="6415e-863">The name of an attribute in an identity is not within the legal range.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-864"><span id="ERROR_SXS_IDENTITY_DUPLICATE_ATTRIBUTE"></span><span id="error_sxs_identity_duplicate_attribute"></span>**\_ \_ \_ attributo duplicato identità SxS errore \_**</span><span class="sxs-lookup"><span data-stu-id="6415e-864"><span id="ERROR_SXS_IDENTITY_DUPLICATE_ATTRIBUTE"></span><span id="error_sxs_identity_duplicate_attribute"></span>**ERROR\_SXS\_IDENTITY\_DUPLICATE\_ATTRIBUTE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-865">14092 (0x370C)</span><span class="sxs-lookup"><span data-stu-id="6415e-865">14092 (0x370C)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-866">Un'identità contiene due definizioni per lo stesso attributo.</span><span class="sxs-lookup"><span data-stu-id="6415e-866">An identity contains two definitions for the same attribute.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-867"><span id="ERROR_SXS_IDENTITY_PARSE_ERROR"></span><span id="error_sxs_identity_parse_error"></span>**errore \_ di \_ analisi identità SxS \_ errore \_**</span><span class="sxs-lookup"><span data-stu-id="6415e-867"><span id="ERROR_SXS_IDENTITY_PARSE_ERROR"></span><span id="error_sxs_identity_parse_error"></span>**ERROR\_SXS\_IDENTITY\_PARSE\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-868">14093 (0x370D)</span><span class="sxs-lookup"><span data-stu-id="6415e-868">14093 (0x370D)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-869">Il formato della stringa di identità non è valido.</span><span class="sxs-lookup"><span data-stu-id="6415e-869">The identity string is malformed.</span></span> <span data-ttu-id="6415e-870">Questo problema può essere dovuto a una virgola finale, a più di due attributi senza nome, a un nome di attributo mancante o a un valore di attributo mancante.</span><span class="sxs-lookup"><span data-stu-id="6415e-870">This may be due to a trailing comma, more than two unnamed attributes, missing attribute name or missing attribute value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-871"><span id="ERROR_MALFORMED_SUBSTITUTION_STRING"></span><span id="error_malformed_substitution_string"></span>**ERRORE \_ stringa di \_ sostituzione non valido \_**</span><span class="sxs-lookup"><span data-stu-id="6415e-871"><span id="ERROR_MALFORMED_SUBSTITUTION_STRING"></span><span id="error_malformed_substitution_string"></span>**ERROR\_MALFORMED\_SUBSTITUTION\_STRING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-872">14094 (0x370E)</span><span class="sxs-lookup"><span data-stu-id="6415e-872">14094 (0x370E)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-873">Formato non corretto di una stringa contenente contenuto sostituibile localizzato.</span><span class="sxs-lookup"><span data-stu-id="6415e-873">A string containing localized substitutable content was malformed.</span></span> <span data-ttu-id="6415e-874">Un segno di dollaro ($) è stato seguito da un elemento diverso da una parentesi aperta o da un altro segno di dollaro o dalla parentesi destra di una sostituzione non trovata.</span><span class="sxs-lookup"><span data-stu-id="6415e-874">Either a dollar sign ($) was followed by something other than a left parenthesis or another dollar sign or an substitution's right parenthesis was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-875"><span id="ERROR_SXS_INCORRECT_PUBLIC_KEY_TOKEN"></span><span id="error_sxs_incorrect_public_key_token"></span>**ERRORE \_ SxS \_ \_ chiave pubblica non corretta \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6415e-875"><span id="ERROR_SXS_INCORRECT_PUBLIC_KEY_TOKEN"></span><span id="error_sxs_incorrect_public_key_token"></span>**ERROR\_SXS\_INCORRECT\_PUBLIC\_KEY\_TOKEN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-876">14095 (0x370F)</span><span class="sxs-lookup"><span data-stu-id="6415e-876">14095 (0x370F)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-877">Il token di chiave pubblica non corrisponde alla chiave pubblica specificata.</span><span class="sxs-lookup"><span data-stu-id="6415e-877">The public key token does not correspond to the public key specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-878"><span id="ERROR_UNMAPPED_SUBSTITUTION_STRING"></span><span id="error_unmapped_substitution_string"></span>**errore durante il \_ mapping della \_ stringa di sostituzione \_**</span><span class="sxs-lookup"><span data-stu-id="6415e-878"><span id="ERROR_UNMAPPED_SUBSTITUTION_STRING"></span><span id="error_unmapped_substitution_string"></span>**ERROR\_UNMAPPED\_SUBSTITUTION\_STRING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-879">14096 (0x3710)</span><span class="sxs-lookup"><span data-stu-id="6415e-879">14096 (0x3710)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-880">Una stringa di sostituzione non ha alcun mapping.</span><span class="sxs-lookup"><span data-stu-id="6415e-880">A substitution string had no mapping.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-881"><span id="ERROR_SXS_ASSEMBLY_NOT_LOCKED"></span><span id="error_sxs_assembly_not_locked"></span>**ERRORE \_ \_ assembly SxS \_ non \_ bloccato**</span><span class="sxs-lookup"><span data-stu-id="6415e-881"><span id="ERROR_SXS_ASSEMBLY_NOT_LOCKED"></span><span id="error_sxs_assembly_not_locked"></span>**ERROR\_SXS\_ASSEMBLY\_NOT\_LOCKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-882">14097 (0x3711)</span><span class="sxs-lookup"><span data-stu-id="6415e-882">14097 (0x3711)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-883">Prima di eseguire la richiesta, è necessario bloccare il componente.</span><span class="sxs-lookup"><span data-stu-id="6415e-883">The component must be locked before making the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-884"><span id="ERROR_SXS_COMPONENT_STORE_CORRUPT"></span><span id="error_sxs_component_store_corrupt"></span>**ERRORE \_ \_ archivio componenti \_ SxS \_ danneggiato**</span><span class="sxs-lookup"><span data-stu-id="6415e-884"><span id="ERROR_SXS_COMPONENT_STORE_CORRUPT"></span><span id="error_sxs_component_store_corrupt"></span>**ERROR\_SXS\_COMPONENT\_STORE\_CORRUPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-885">14098 (0x3712)</span><span class="sxs-lookup"><span data-stu-id="6415e-885">14098 (0x3712)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-886">L'archivio componenti è danneggiato.</span><span class="sxs-lookup"><span data-stu-id="6415e-886">The component store has been corrupted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-887"><span id="ERROR_ADVANCED_INSTALLER_FAILED"></span><span id="error_advanced_installer_failed"></span>**ERRORE \_ del \_ programma di installazione avanzato \_ non riuscito**</span><span class="sxs-lookup"><span data-stu-id="6415e-887"><span id="ERROR_ADVANCED_INSTALLER_FAILED"></span><span id="error_advanced_installer_failed"></span>**ERROR\_ADVANCED\_INSTALLER\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-888">14099 (0x3713)</span><span class="sxs-lookup"><span data-stu-id="6415e-888">14099 (0x3713)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-889">Un programma di installazione avanzato non è riuscito durante l'installazione o la manutenzione.</span><span class="sxs-lookup"><span data-stu-id="6415e-889">An advanced installer failed during setup or servicing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-890"><span id="ERROR_XML_ENCODING_MISMATCH"></span><span id="error_xml_encoding_mismatch"></span>**ERRORE \_ di \_ codifica XML non \_ corrispondente**</span><span class="sxs-lookup"><span data-stu-id="6415e-890"><span id="ERROR_XML_ENCODING_MISMATCH"></span><span id="error_xml_encoding_mismatch"></span>**ERROR\_XML\_ENCODING\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-891">14100 (0x3714)</span><span class="sxs-lookup"><span data-stu-id="6415e-891">14100 (0x3714)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-892">La codifica dei caratteri nella dichiarazione XML non corrisponde alla codifica utilizzata nel documento.</span><span class="sxs-lookup"><span data-stu-id="6415e-892">The character encoding in the XML declaration did not match the encoding used in the document.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-893"><span id="ERROR_SXS_MANIFEST_IDENTITY_SAME_BUT_CONTENTS_DIFFERENT"></span><span id="error_sxs_manifest_identity_same_but_contents_different"></span>**errore di identità del manifesto SxS di errore, \_ \_ \_ \_ \_ ma \_ contenuto \_ diverso**</span><span class="sxs-lookup"><span data-stu-id="6415e-893"><span id="ERROR_SXS_MANIFEST_IDENTITY_SAME_BUT_CONTENTS_DIFFERENT"></span><span id="error_sxs_manifest_identity_same_but_contents_different"></span>**ERROR\_SXS\_MANIFEST\_IDENTITY\_SAME\_BUT\_CONTENTS\_DIFFERENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-894">14101 (0x3715)</span><span class="sxs-lookup"><span data-stu-id="6415e-894">14101 (0x3715)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-895">Le identità dei manifesti sono identiche, ma il relativo contenuto è diverso.</span><span class="sxs-lookup"><span data-stu-id="6415e-895">The identities of the manifests are identical but their contents are different.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-896"><span id="ERROR_SXS_IDENTITIES_DIFFERENT"></span><span id="error_sxs_identities_different"></span>**\_identità SxS di errore \_ \_ diverse**</span><span class="sxs-lookup"><span data-stu-id="6415e-896"><span id="ERROR_SXS_IDENTITIES_DIFFERENT"></span><span id="error_sxs_identities_different"></span>**ERROR\_SXS\_IDENTITIES\_DIFFERENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-897">14102 (0x3716)</span><span class="sxs-lookup"><span data-stu-id="6415e-897">14102 (0x3716)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-898">Le identità dei componenti sono diverse.</span><span class="sxs-lookup"><span data-stu-id="6415e-898">The component identities are different.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-899"><span id="ERROR_SXS_ASSEMBLY_IS_NOT_A_DEPLOYMENT"></span><span id="error_sxs_assembly_is_not_a_deployment"></span>**\_ \_ l'assembly SxS \_ \_ di errore non è \_ una \_ distribuzione**</span><span class="sxs-lookup"><span data-stu-id="6415e-899"><span id="ERROR_SXS_ASSEMBLY_IS_NOT_A_DEPLOYMENT"></span><span id="error_sxs_assembly_is_not_a_deployment"></span>**ERROR\_SXS\_ASSEMBLY\_IS\_NOT\_A\_DEPLOYMENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-900">14103 (0x3717)</span><span class="sxs-lookup"><span data-stu-id="6415e-900">14103 (0x3717)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-901">L'assembly non è una distribuzione.</span><span class="sxs-lookup"><span data-stu-id="6415e-901">The assembly is not a deployment.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-902"><span id="ERROR_SXS_FILE_NOT_PART_OF_ASSEMBLY"></span><span id="error_sxs_file_not_part_of_assembly"></span>**ERRORE \_ SxS \_ file \_ non \_ fa parte \_ dell' \_ assembly**</span><span class="sxs-lookup"><span data-stu-id="6415e-902"><span id="ERROR_SXS_FILE_NOT_PART_OF_ASSEMBLY"></span><span id="error_sxs_file_not_part_of_assembly"></span>**ERROR\_SXS\_FILE\_NOT\_PART\_OF\_ASSEMBLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-903">14104 (0x3718)</span><span class="sxs-lookup"><span data-stu-id="6415e-903">14104 (0x3718)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-904">Il file non fa parte dell'assembly.</span><span class="sxs-lookup"><span data-stu-id="6415e-904">The file is not a part of the assembly.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-905"><span id="ERROR_SXS_MANIFEST_TOO_BIG"></span><span id="error_sxs_manifest_too_big"></span>**\_manifesto SxS \_ errore \_ troppo \_ grande**</span><span class="sxs-lookup"><span data-stu-id="6415e-905"><span id="ERROR_SXS_MANIFEST_TOO_BIG"></span><span id="error_sxs_manifest_too_big"></span>**ERROR\_SXS\_MANIFEST\_TOO\_BIG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-906">14105 (0x3719)</span><span class="sxs-lookup"><span data-stu-id="6415e-906">14105 (0x3719)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-907">Le dimensioni del manifesto superano il valore massimo consentito.</span><span class="sxs-lookup"><span data-stu-id="6415e-907">The size of the manifest exceeds the maximum allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-908"><span id="ERROR_SXS_SETTING_NOT_REGISTERED"></span><span id="error_sxs_setting_not_registered"></span>**\_impostazione errore \_ SxS \_ non \_ registrata**</span><span class="sxs-lookup"><span data-stu-id="6415e-908"><span id="ERROR_SXS_SETTING_NOT_REGISTERED"></span><span id="error_sxs_setting_not_registered"></span>**ERROR\_SXS\_SETTING\_NOT\_REGISTERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-909">14106 (0x371A)</span><span class="sxs-lookup"><span data-stu-id="6415e-909">14106 (0x371A)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-910">L'impostazione non è registrata.</span><span class="sxs-lookup"><span data-stu-id="6415e-910">The setting is not registered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-911"><span id="ERROR_SXS_TRANSACTION_CLOSURE_INCOMPLETE"></span><span id="error_sxs_transaction_closure_incomplete"></span>**ERRORE \_ di \_ chiusura della transazione SxS \_ \_ incompleta**</span><span class="sxs-lookup"><span data-stu-id="6415e-911"><span id="ERROR_SXS_TRANSACTION_CLOSURE_INCOMPLETE"></span><span id="error_sxs_transaction_closure_incomplete"></span>**ERROR\_SXS\_TRANSACTION\_CLOSURE\_INCOMPLETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-912">14107 (0x371B)</span><span class="sxs-lookup"><span data-stu-id="6415e-912">14107 (0x371B)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-913">Uno o più membri obbligatori della transazione non sono presenti.</span><span class="sxs-lookup"><span data-stu-id="6415e-913">One or more required members of the transaction are not present.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-914"><span id="ERROR_SMI_PRIMITIVE_INSTALLER_FAILED"></span><span id="error_smi_primitive_installer_failed"></span>**ERRORE \_ del \_ programma di installazione primitive SMI \_ \_ non riuscito**</span><span class="sxs-lookup"><span data-stu-id="6415e-914"><span id="ERROR_SMI_PRIMITIVE_INSTALLER_FAILED"></span><span id="error_smi_primitive_installer_failed"></span>**ERROR\_SMI\_PRIMITIVE\_INSTALLER\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-915">14108 (0x371C)</span><span class="sxs-lookup"><span data-stu-id="6415e-915">14108 (0x371C)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-916">Il programma di installazione primitive SMI non è riuscito durante l'installazione o la manutenzione.</span><span class="sxs-lookup"><span data-stu-id="6415e-916">The SMI primitive installer failed during setup or servicing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-917"><span id="ERROR_GENERIC_COMMAND_FAILED"></span><span id="error_generic_command_failed"></span>**ERRORE \_ \_ comando generico \_ non riuscito**</span><span class="sxs-lookup"><span data-stu-id="6415e-917"><span id="ERROR_GENERIC_COMMAND_FAILED"></span><span id="error_generic_command_failed"></span>**ERROR\_GENERIC\_COMMAND\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-918">14109 (0x371D)</span><span class="sxs-lookup"><span data-stu-id="6415e-918">14109 (0x371D)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-919">Un eseguibile del comando generico ha restituito un risultato che indica un errore.</span><span class="sxs-lookup"><span data-stu-id="6415e-919">A generic command executable returned a result that indicates failure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-920"><span id="ERROR_SXS_FILE_HASH_MISSING"></span><span id="error_sxs_file_hash_missing"></span>**\_ \_ hash file SxS \_ errore \_ mancante**</span><span class="sxs-lookup"><span data-stu-id="6415e-920"><span id="ERROR_SXS_FILE_HASH_MISSING"></span><span id="error_sxs_file_hash_missing"></span>**ERROR\_SXS\_FILE\_HASH\_MISSING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-921">14110 (0x371E)</span><span class="sxs-lookup"><span data-stu-id="6415e-921">14110 (0x371E)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-922">Nel manifesto di un componente mancano le informazioni di verifica del file.</span><span class="sxs-lookup"><span data-stu-id="6415e-922">A component is missing file verification information in its manifest.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-923"><span id="ERROR_EVT_INVALID_CHANNEL_PATH"></span><span id="error_evt_invalid_channel_path"></span>**ERRORE \_ evt \_ \_ percorso del canale non valido \_**</span><span class="sxs-lookup"><span data-stu-id="6415e-923"><span id="ERROR_EVT_INVALID_CHANNEL_PATH"></span><span id="error_evt_invalid_channel_path"></span>**ERROR\_EVT\_INVALID\_CHANNEL\_PATH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-924">15000 (0x3A98)</span><span class="sxs-lookup"><span data-stu-id="6415e-924">15000 (0x3A98)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-925">Il percorso del canale specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="6415e-925">The specified channel path is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-926"><span id="ERROR_EVT_INVALID_QUERY"></span><span id="error_evt_invalid_query"></span>**ERRORE \_ evt \_ query non valida \_**</span><span class="sxs-lookup"><span data-stu-id="6415e-926"><span id="ERROR_EVT_INVALID_QUERY"></span><span id="error_evt_invalid_query"></span>**ERROR\_EVT\_INVALID\_QUERY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-927">15001 (0x3A99)</span><span class="sxs-lookup"><span data-stu-id="6415e-927">15001 (0x3A99)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-928">La query specificata non è valida.</span><span class="sxs-lookup"><span data-stu-id="6415e-928">The specified query is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-929"><span id="ERROR_EVT_PUBLISHER_METADATA_NOT_FOUND"></span><span id="error_evt_publisher_metadata_not_found"></span>**ERRORE \_ evt \_ pubblicazione \_ metadati \_ non \_ trovati**</span><span class="sxs-lookup"><span data-stu-id="6415e-929"><span id="ERROR_EVT_PUBLISHER_METADATA_NOT_FOUND"></span><span id="error_evt_publisher_metadata_not_found"></span>**ERROR\_EVT\_PUBLISHER\_METADATA\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-930">15002 (0x3A9A)</span><span class="sxs-lookup"><span data-stu-id="6415e-930">15002 (0x3A9A)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-931">Impossibile trovare i metadati del server di pubblicazione nella risorsa.</span><span class="sxs-lookup"><span data-stu-id="6415e-931">The publisher metadata cannot be found in the resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-932"><span id="ERROR_EVT_EVENT_TEMPLATE_NOT_FOUND"></span><span id="error_evt_event_template_not_found"></span>**ERRORE \_ evt \_ modello di evento \_ \_ non \_ trovato**</span><span class="sxs-lookup"><span data-stu-id="6415e-932"><span id="ERROR_EVT_EVENT_TEMPLATE_NOT_FOUND"></span><span id="error_evt_event_template_not_found"></span>**ERROR\_EVT\_EVENT\_TEMPLATE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-933">15003 (0x3A9B)</span><span class="sxs-lookup"><span data-stu-id="6415e-933">15003 (0x3A9B)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-934">Il modello per la definizione di un evento non è stato trovato nella risorsa (errore = %1).</span><span class="sxs-lookup"><span data-stu-id="6415e-934">The template for an event definition cannot be found in the resource (error = %1).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-935"><span id="ERROR_EVT_INVALID_PUBLISHER_NAME"></span><span id="error_evt_invalid_publisher_name"></span>**ERRORE \_ evt \_ \_ nome dell'autore non valido \_**</span><span class="sxs-lookup"><span data-stu-id="6415e-935"><span id="ERROR_EVT_INVALID_PUBLISHER_NAME"></span><span id="error_evt_invalid_publisher_name"></span>**ERROR\_EVT\_INVALID\_PUBLISHER\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-936">15004 (0x3A9C)</span><span class="sxs-lookup"><span data-stu-id="6415e-936">15004 (0x3A9C)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-937">Il nome del server di pubblicazione specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="6415e-937">The specified publisher name is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-938"><span id="ERROR_EVT_INVALID_EVENT_DATA"></span><span id="error_evt_invalid_event_data"></span>**ERRORE \_ evt \_ \_ dati evento non validi \_**</span><span class="sxs-lookup"><span data-stu-id="6415e-938"><span id="ERROR_EVT_INVALID_EVENT_DATA"></span><span id="error_evt_invalid_event_data"></span>**ERROR\_EVT\_INVALID\_EVENT\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-939">15005 (0x3A9D)</span><span class="sxs-lookup"><span data-stu-id="6415e-939">15005 (0x3A9D)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-940">I dati dell'evento generati dal server di pubblicazione non sono compatibili con la definizione del modello di evento nel manifesto del server di pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="6415e-940">The event data raised by the publisher is not compatible with the event template definition in the publisher's manifest.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-941"><span id="ERROR_EVT_CHANNEL_NOT_FOUND"></span><span id="error_evt_channel_not_found"></span>**ERRORE \_ \_ canale evt \_ non \_ trovato**</span><span class="sxs-lookup"><span data-stu-id="6415e-941"><span id="ERROR_EVT_CHANNEL_NOT_FOUND"></span><span id="error_evt_channel_not_found"></span>**ERROR\_EVT\_CHANNEL\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-942">15007 (0x3A9F)</span><span class="sxs-lookup"><span data-stu-id="6415e-942">15007 (0x3A9F)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-943">Il canale specificato non è stato trovato.</span><span class="sxs-lookup"><span data-stu-id="6415e-943">The specified channel could not be found.</span></span> <span data-ttu-id="6415e-944">Controllare la configurazione del canale.</span><span class="sxs-lookup"><span data-stu-id="6415e-944">Check channel configuration.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-945"><span id="ERROR_EVT_MALFORMED_XML_TEXT"></span><span id="error_evt_malformed_xml_text"></span>**ERRORE \_ evt \_ \_ testo XML non valido \_**</span><span class="sxs-lookup"><span data-stu-id="6415e-945"><span id="ERROR_EVT_MALFORMED_XML_TEXT"></span><span id="error_evt_malformed_xml_text"></span>**ERROR\_EVT\_MALFORMED\_XML\_TEXT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-946">15008 (0x3AA0)</span><span class="sxs-lookup"><span data-stu-id="6415e-946">15008 (0x3AA0)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-947">Il testo XML specificato non è ben formato.</span><span class="sxs-lookup"><span data-stu-id="6415e-947">The specified xml text was not well-formed.</span></span> <span data-ttu-id="6415e-948">Per ulteriori informazioni, vedere l'errore esteso.</span><span class="sxs-lookup"><span data-stu-id="6415e-948">See Extended Error for more details.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-949"><span id="ERROR_EVT_SUBSCRIPTION_TO_DIRECT_CHANNEL"></span><span id="error_evt_subscription_to_direct_channel"></span>**ERRORE \_ evt \_ sottoscrizione \_ al \_ \_ canale diretto**</span><span class="sxs-lookup"><span data-stu-id="6415e-949"><span id="ERROR_EVT_SUBSCRIPTION_TO_DIRECT_CHANNEL"></span><span id="error_evt_subscription_to_direct_channel"></span>**ERROR\_EVT\_SUBSCRIPTION\_TO\_DIRECT\_CHANNEL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-950">15009 (0x3AA1)</span><span class="sxs-lookup"><span data-stu-id="6415e-950">15009 (0x3AA1)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-951">Il chiamante sta provando a sottoscrivere un canale diretto che non è consentito.</span><span class="sxs-lookup"><span data-stu-id="6415e-951">The caller is trying to subscribe to a direct channel which is not allowed.</span></span> <span data-ttu-id="6415e-952">Gli eventi per un canale diretto passano direttamente a un file di log e non possono essere sottoscritti.</span><span class="sxs-lookup"><span data-stu-id="6415e-952">The events for a direct channel go directly to a logfile and cannot be subscribed to.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-953"><span id="ERROR_EVT_CONFIGURATION_ERROR"></span><span id="error_evt_configuration_error"></span>**errore \_ di \_ configurazione di evt \_**</span><span class="sxs-lookup"><span data-stu-id="6415e-953"><span id="ERROR_EVT_CONFIGURATION_ERROR"></span><span id="error_evt_configuration_error"></span>**ERROR\_EVT\_CONFIGURATION\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-954">15010 (0x3AA2)</span><span class="sxs-lookup"><span data-stu-id="6415e-954">15010 (0x3AA2)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-955">Errore di configurazione.</span><span class="sxs-lookup"><span data-stu-id="6415e-955">Configuration error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-956"><span id="ERROR_EVT_QUERY_RESULT_STALE"></span><span id="error_evt_query_result_stale"></span>**ERRORE il \_ risultato della query evt non è \_ \_ \_ aggiornato**</span><span class="sxs-lookup"><span data-stu-id="6415e-956"><span id="ERROR_EVT_QUERY_RESULT_STALE"></span><span id="error_evt_query_result_stale"></span>**ERROR\_EVT\_QUERY\_RESULT\_STALE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-957">15011 (0x3AA3)</span><span class="sxs-lookup"><span data-stu-id="6415e-957">15011 (0x3AA3)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-958">Il risultato della query non è aggiornato o non è valido.</span><span class="sxs-lookup"><span data-stu-id="6415e-958">The query result is stale / invalid.</span></span> <span data-ttu-id="6415e-959">Questo problema può essere dovuto al fatto che il log è stato cancellato o spostato dopo la creazione del risultato della query.</span><span class="sxs-lookup"><span data-stu-id="6415e-959">This may be due to the log being cleared or rolling over after the query result was created.</span></span> <span data-ttu-id="6415e-960">Gli utenti devono gestire questo codice rilasciando l'oggetto risultato della query ed eseguendo nuovamente la query.</span><span class="sxs-lookup"><span data-stu-id="6415e-960">Users should handle this code by releasing the query result object and reissuing the query.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-961"><span id="ERROR_EVT_QUERY_RESULT_INVALID_POSITION"></span><span id="error_evt_query_result_invalid_position"></span>**ERRORE \_ il \_ risultato della query evt \_ \_ posizione non valida \_**</span><span class="sxs-lookup"><span data-stu-id="6415e-961"><span id="ERROR_EVT_QUERY_RESULT_INVALID_POSITION"></span><span id="error_evt_query_result_invalid_position"></span>**ERROR\_EVT\_QUERY\_RESULT\_INVALID\_POSITION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-962">15012 (0x3AA4)</span><span class="sxs-lookup"><span data-stu-id="6415e-962">15012 (0x3AA4)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-963">Il risultato della query si trova attualmente in una posizione non valida.</span><span class="sxs-lookup"><span data-stu-id="6415e-963">Query result is currently at an invalid position.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-964"><span id="ERROR_EVT_NON_VALIDATING_MSXML"></span><span id="error_evt_non_validating_msxml"></span>**ERRORE \_ evt \_ non \_ convalida \_ MSXML**</span><span class="sxs-lookup"><span data-stu-id="6415e-964"><span id="ERROR_EVT_NON_VALIDATING_MSXML"></span><span id="error_evt_non_validating_msxml"></span>**ERROR\_EVT\_NON\_VALIDATING\_MSXML**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-965">15013 (0x3AA5)</span><span class="sxs-lookup"><span data-stu-id="6415e-965">15013 (0x3AA5)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-966">MSXML registrato non supporta la convalida.</span><span class="sxs-lookup"><span data-stu-id="6415e-966">Registered MSXML doesn't support validation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-967"><span id="ERROR_EVT_FILTER_ALREADYSCOPED"></span><span id="error_evt_filter_alreadyscoped"></span>**ERRORE \_ evt \_ filtro \_ ALREADYSCOPED**</span><span class="sxs-lookup"><span data-stu-id="6415e-967"><span id="ERROR_EVT_FILTER_ALREADYSCOPED"></span><span id="error_evt_filter_alreadyscoped"></span>**ERROR\_EVT\_FILTER\_ALREADYSCOPED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-968">15014 (0x3AA6)</span><span class="sxs-lookup"><span data-stu-id="6415e-968">15014 (0x3AA6)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-969">Un'espressione può essere seguita solo da una modifica dell'operazione di ambito se restituisce un set di nodi e non fa già parte di un'altra modifica dell'operazione dell'ambito.</span><span class="sxs-lookup"><span data-stu-id="6415e-969">An expression can only be followed by a change of scope operation if it itself evaluates to a node set and is not already part of some other change of scope operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-970"><span id="ERROR_EVT_FILTER_NOTELTSET"></span><span id="error_evt_filter_noteltset"></span>**ERRORE \_ evt \_ filtro \_ NOTELTSET**</span><span class="sxs-lookup"><span data-stu-id="6415e-970"><span id="ERROR_EVT_FILTER_NOTELTSET"></span><span id="error_evt_filter_noteltset"></span>**ERROR\_EVT\_FILTER\_NOTELTSET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-971">15015 (0x3AA7)</span><span class="sxs-lookup"><span data-stu-id="6415e-971">15015 (0x3AA7)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-972">Non è possibile eseguire un'operazione step da un termine che non rappresenta un set di elementi.</span><span class="sxs-lookup"><span data-stu-id="6415e-972">Can't perform a step operation from a term that does not represent an element set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-973"><span id="ERROR_EVT_FILTER_INVARG"></span><span id="error_evt_filter_invarg"></span>**ERRORE \_ evt \_ filtro \_ INVARG**</span><span class="sxs-lookup"><span data-stu-id="6415e-973"><span id="ERROR_EVT_FILTER_INVARG"></span><span id="error_evt_filter_invarg"></span>**ERROR\_EVT\_FILTER\_INVARG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-974">15016 (0x3AA8)</span><span class="sxs-lookup"><span data-stu-id="6415e-974">15016 (0x3AA8)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-975">Gli argomenti del lato sinistro per gli operatori binari devono essere attributi, nodi o variabili e gli argomenti lato destro devono essere costanti.</span><span class="sxs-lookup"><span data-stu-id="6415e-975">Left hand side arguments to binary operators must be either attributes, nodes or variables and right hand side arguments must be constants.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-976"><span id="ERROR_EVT_FILTER_INVTEST"></span><span id="error_evt_filter_invtest"></span>**ERRORE \_ evt \_ filtro \_ INVTEST**</span><span class="sxs-lookup"><span data-stu-id="6415e-976"><span id="ERROR_EVT_FILTER_INVTEST"></span><span id="error_evt_filter_invtest"></span>**ERROR\_EVT\_FILTER\_INVTEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-977">15017 (0x3AA9)</span><span class="sxs-lookup"><span data-stu-id="6415e-977">15017 (0x3AA9)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-978">Un'operazione Step deve coinvolgere un test di nodo o, nel caso di un predicato, un'espressione algebrica sulla quale testare ogni nodo nel set di nodi identificato dal set di nodi precedente.</span><span class="sxs-lookup"><span data-stu-id="6415e-978">A step operation must involve either a node test or, in the case of a predicate, an algebraic expression against which to test each node in the node set identified by the preceeding node set can be evaluated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-979"><span id="ERROR_EVT_FILTER_INVTYPE"></span><span id="error_evt_filter_invtype"></span>**ERRORE \_ evt \_ filtro \_ INVTYPE**</span><span class="sxs-lookup"><span data-stu-id="6415e-979"><span id="ERROR_EVT_FILTER_INVTYPE"></span><span id="error_evt_filter_invtype"></span>**ERROR\_EVT\_FILTER\_INVTYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-980">15018 (0x3AAA)</span><span class="sxs-lookup"><span data-stu-id="6415e-980">15018 (0x3AAA)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-981">Questo tipo di dati non è attualmente supportato.</span><span class="sxs-lookup"><span data-stu-id="6415e-981">This data type is currently unsupported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-982"><span id="ERROR_EVT_FILTER_PARSEERR"></span><span id="error_evt_filter_parseerr"></span>**ERRORE \_ evt \_ filtro \_ PARSEERR**</span><span class="sxs-lookup"><span data-stu-id="6415e-982"><span id="ERROR_EVT_FILTER_PARSEERR"></span><span id="error_evt_filter_parseerr"></span>**ERROR\_EVT\_FILTER\_PARSEERR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-983">15019 (0x3AAB)</span><span class="sxs-lookup"><span data-stu-id="6415e-983">15019 (0x3AAB)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-984">Si è verificato un errore di sintassi nella posizione %1! d!.</span><span class="sxs-lookup"><span data-stu-id="6415e-984">A syntax error occurred at position %1!d!.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-985"><span id="ERROR_EVT_FILTER_UNSUPPORTEDOP"></span><span id="error_evt_filter_unsupportedop"></span>**ERRORE \_ evt \_ filtro \_ UNSUPPORTEDOP**</span><span class="sxs-lookup"><span data-stu-id="6415e-985"><span id="ERROR_EVT_FILTER_UNSUPPORTEDOP"></span><span id="error_evt_filter_unsupportedop"></span>**ERROR\_EVT\_FILTER\_UNSUPPORTEDOP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-986">15020 (0x3AAC)</span><span class="sxs-lookup"><span data-stu-id="6415e-986">15020 (0x3AAC)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-987">Questo operatore non è supportato da questa implementazione del filtro.</span><span class="sxs-lookup"><span data-stu-id="6415e-987">This operator is unsupported by this implementation of the filter.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-988"><span id="ERROR_EVT_FILTER_UNEXPECTEDTOKEN"></span><span id="error_evt_filter_unexpectedtoken"></span>**ERRORE \_ evt \_ filtro \_ UNEXPECTEDTOKEN**</span><span class="sxs-lookup"><span data-stu-id="6415e-988"><span id="ERROR_EVT_FILTER_UNEXPECTEDTOKEN"></span><span id="error_evt_filter_unexpectedtoken"></span>**ERROR\_EVT\_FILTER\_UNEXPECTEDTOKEN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-989">15021 (0x3AAD)</span><span class="sxs-lookup"><span data-stu-id="6415e-989">15021 (0x3AAD)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-990">Il token rilevato è imprevisto.</span><span class="sxs-lookup"><span data-stu-id="6415e-990">The token encountered was unexpected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-991"><span id="ERROR_EVT_INVALID_OPERATION_OVER_ENABLED_DIRECT_CHANNEL"></span><span id="error_evt_invalid_operation_over_enabled_direct_channel"></span>**ERRORE \_ evt \_ \_ operazione non \_ valida \_ su \_ canale diretto abilitato \_**</span><span class="sxs-lookup"><span data-stu-id="6415e-991"><span id="ERROR_EVT_INVALID_OPERATION_OVER_ENABLED_DIRECT_CHANNEL"></span><span id="error_evt_invalid_operation_over_enabled_direct_channel"></span>**ERROR\_EVT\_INVALID\_OPERATION\_OVER\_ENABLED\_DIRECT\_CHANNEL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-992">15022 (0x3AAE)</span><span class="sxs-lookup"><span data-stu-id="6415e-992">15022 (0x3AAE)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-993">L'operazione richiesta non può essere eseguita su un canale diretto abilitato.</span><span class="sxs-lookup"><span data-stu-id="6415e-993">The requested operation cannot be performed over an enabled direct channel.</span></span> <span data-ttu-id="6415e-994">Il canale deve prima essere disabilitato prima di eseguire l'operazione richiesta.</span><span class="sxs-lookup"><span data-stu-id="6415e-994">The channel must first be disabled before performing the requested operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-995"><span id="ERROR_EVT_INVALID_CHANNEL_PROPERTY_VALUE"></span><span id="error_evt_invalid_channel_property_value"></span>**ERRORE \_ evt \_ \_ valore della \_ proprietà del canale non valido \_**</span><span class="sxs-lookup"><span data-stu-id="6415e-995"><span id="ERROR_EVT_INVALID_CHANNEL_PROPERTY_VALUE"></span><span id="error_evt_invalid_channel_property_value"></span>**ERROR\_EVT\_INVALID\_CHANNEL\_PROPERTY\_VALUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-996">15023 (0x3AAF)</span><span class="sxs-lookup"><span data-stu-id="6415e-996">15023 (0x3AAF)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-997">Proprietà canale %1! s!</span><span class="sxs-lookup"><span data-stu-id="6415e-997">Channel property %1!s!</span></span> <span data-ttu-id="6415e-998">contiene un valore non valido.</span><span class="sxs-lookup"><span data-stu-id="6415e-998">contains invalid value.</span></span> <span data-ttu-id="6415e-999">Il valore di tipo non valido, non è compreso nell'intervallo valido, non può essere aggiornato o non è supportato da questo tipo di canale.</span><span class="sxs-lookup"><span data-stu-id="6415e-999">The value has invalid type, is outside of valid range, can't be updated or is not supported by this type of channel.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-1000"><span id="ERROR_EVT_INVALID_PUBLISHER_PROPERTY_VALUE"></span><span id="error_evt_invalid_publisher_property_value"></span>**ERRORE \_ evt \_ valore della proprietà del server di pubblicazione non valido \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6415e-1000"><span id="ERROR_EVT_INVALID_PUBLISHER_PROPERTY_VALUE"></span><span id="error_evt_invalid_publisher_property_value"></span>**ERROR\_EVT\_INVALID\_PUBLISHER\_PROPERTY\_VALUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-1001">15024 (0x3AB0)</span><span class="sxs-lookup"><span data-stu-id="6415e-1001">15024 (0x3AB0)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-1002">Proprietà server di pubblicazione %1! s!</span><span class="sxs-lookup"><span data-stu-id="6415e-1002">Publisher property %1!s!</span></span> <span data-ttu-id="6415e-1003">contiene un valore non valido.</span><span class="sxs-lookup"><span data-stu-id="6415e-1003">contains invalid value.</span></span> <span data-ttu-id="6415e-1004">Il valore di tipo non valido, non è compreso nell'intervallo valido, non può essere aggiornato o non è supportato da questo tipo di server di pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="6415e-1004">The value has invalid type, is outside of valid range, can't be updated or is not supported by this type of publisher.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-1005"><span id="ERROR_EVT_CHANNEL_CANNOT_ACTIVATE"></span><span id="error_evt_channel_cannot_activate"></span>**ERRORE \_ \_ \_ non è possibile attivare il canale evt \_**</span><span class="sxs-lookup"><span data-stu-id="6415e-1005"><span id="ERROR_EVT_CHANNEL_CANNOT_ACTIVATE"></span><span id="error_evt_channel_cannot_activate"></span>**ERROR\_EVT\_CHANNEL\_CANNOT\_ACTIVATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-1006">15025 (0x3AB1)</span><span class="sxs-lookup"><span data-stu-id="6415e-1006">15025 (0x3AB1)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-1007">Non è possibile attivare il canale.</span><span class="sxs-lookup"><span data-stu-id="6415e-1007">The channel fails to activate.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-1008"><span id="ERROR_EVT_FILTER_TOO_COMPLEX"></span><span id="error_evt_filter_too_complex"></span>**ERRORE \_ \_ filtro evt \_ troppo \_ complesso**</span><span class="sxs-lookup"><span data-stu-id="6415e-1008"><span id="ERROR_EVT_FILTER_TOO_COMPLEX"></span><span id="error_evt_filter_too_complex"></span>**ERROR\_EVT\_FILTER\_TOO\_COMPLEX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-1009">15026 (0x3AB2)</span><span class="sxs-lookup"><span data-stu-id="6415e-1009">15026 (0x3AB2)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-1010">L'espressione XPath ha superato la complessità supportata.</span><span class="sxs-lookup"><span data-stu-id="6415e-1010">The xpath expression exceeded supported complexity.</span></span> <span data-ttu-id="6415e-1011">Symplify o suddividerlo in due o più espressioni semplici.</span><span class="sxs-lookup"><span data-stu-id="6415e-1011">Please symplify it or split it into two or more simple expressions.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-1012"><span id="ERROR_EVT_MESSAGE_NOT_FOUND"></span><span id="error_evt_message_not_found"></span>**ERRORE \_ evt \_ messaggio \_ non \_ trovato**</span><span class="sxs-lookup"><span data-stu-id="6415e-1012"><span id="ERROR_EVT_MESSAGE_NOT_FOUND"></span><span id="error_evt_message_not_found"></span>**ERROR\_EVT\_MESSAGE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-1013">15027 (0x3AB3)</span><span class="sxs-lookup"><span data-stu-id="6415e-1013">15027 (0x3AB3)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-1014">la risorsa messaggio è presente, ma il messaggio non viene trovato nella tabella stringa/messaggio.</span><span class="sxs-lookup"><span data-stu-id="6415e-1014">the message resource is present but the message is not found in the string/message table.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-1015"><span id="ERROR_EVT_MESSAGE_ID_NOT_FOUND"></span><span id="error_evt_message_id_not_found"></span>**ERRORE \_ evt \_ \_ ID messaggio \_ non \_ trovato**</span><span class="sxs-lookup"><span data-stu-id="6415e-1015"><span id="ERROR_EVT_MESSAGE_ID_NOT_FOUND"></span><span id="error_evt_message_id_not_found"></span>**ERROR\_EVT\_MESSAGE\_ID\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-1016">15028 (0x3AB4)</span><span class="sxs-lookup"><span data-stu-id="6415e-1016">15028 (0x3AB4)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-1017">Impossibile trovare l'ID di messaggio per il messaggio desiderato.</span><span class="sxs-lookup"><span data-stu-id="6415e-1017">The message id for the desired message could not be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-1018"><span id="ERROR_EVT_UNRESOLVED_VALUE_INSERT"></span><span id="error_evt_unresolved_value_insert"></span>**ERRORE \_ evt \_ \_ inserimento valore non risolto \_**</span><span class="sxs-lookup"><span data-stu-id="6415e-1018"><span id="ERROR_EVT_UNRESOLVED_VALUE_INSERT"></span><span id="error_evt_unresolved_value_insert"></span>**ERROR\_EVT\_UNRESOLVED\_VALUE\_INSERT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-1019">15029 (0x3AB5)</span><span class="sxs-lookup"><span data-stu-id="6415e-1019">15029 (0x3AB5)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-1020">Impossibile trovare la stringa di sostituzione per l'indice di inserimento (%1).</span><span class="sxs-lookup"><span data-stu-id="6415e-1020">The substitution string for insert index (%1) could not be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-1021"><span id="ERROR_EVT_UNRESOLVED_PARAMETER_INSERT"></span><span id="error_evt_unresolved_parameter_insert"></span>**ERRORE \_ evt \_ \_ inserimento parametro non risolto \_**</span><span class="sxs-lookup"><span data-stu-id="6415e-1021"><span id="ERROR_EVT_UNRESOLVED_PARAMETER_INSERT"></span><span id="error_evt_unresolved_parameter_insert"></span>**ERROR\_EVT\_UNRESOLVED\_PARAMETER\_INSERT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-1022">15030 (0x3AB6)</span><span class="sxs-lookup"><span data-stu-id="6415e-1022">15030 (0x3AB6)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-1023">Impossibile trovare la stringa di descrizione per il riferimento al parametro (%1).</span><span class="sxs-lookup"><span data-stu-id="6415e-1023">The description string for parameter reference (%1) could not be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-1024"><span id="ERROR_EVT_MAX_INSERTS_REACHED"></span><span id="error_evt_max_inserts_reached"></span>**ERRORE \_ evt \_ numero massimo di \_ inserimenti \_ raggiunti**</span><span class="sxs-lookup"><span data-stu-id="6415e-1024"><span id="ERROR_EVT_MAX_INSERTS_REACHED"></span><span id="error_evt_max_inserts_reached"></span>**ERROR\_EVT\_MAX\_INSERTS\_REACHED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-1025">15031 (0x3AB7)</span><span class="sxs-lookup"><span data-stu-id="6415e-1025">15031 (0x3AB7)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-1026">È stato raggiunto il numero massimo di sostituzioni.</span><span class="sxs-lookup"><span data-stu-id="6415e-1026">The maximum number of replacements has been reached.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-1027"><span id="ERROR_EVT_EVENT_DEFINITION_NOT_FOUND"></span><span id="error_evt_event_definition_not_found"></span>**ERRORE \_ evt \_ \_ \_ Impossibile trovare la definizione dell'evento \_**</span><span class="sxs-lookup"><span data-stu-id="6415e-1027"><span id="ERROR_EVT_EVENT_DEFINITION_NOT_FOUND"></span><span id="error_evt_event_definition_not_found"></span>**ERROR\_EVT\_EVENT\_DEFINITION\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-1028">15032 (0x3AB8)</span><span class="sxs-lookup"><span data-stu-id="6415e-1028">15032 (0x3AB8)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-1029">Impossibile trovare la definizione dell'evento per l'ID evento (%1).</span><span class="sxs-lookup"><span data-stu-id="6415e-1029">The event definition could not be found for event id (%1).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-1030"><span id="ERROR_EVT_MESSAGE_LOCALE_NOT_FOUND"></span><span id="error_evt_message_locale_not_found"></span>**ERRORE \_ nelle \_ \_ impostazioni locali del messaggio evt \_ non \_ trovato**</span><span class="sxs-lookup"><span data-stu-id="6415e-1030"><span id="ERROR_EVT_MESSAGE_LOCALE_NOT_FOUND"></span><span id="error_evt_message_locale_not_found"></span>**ERROR\_EVT\_MESSAGE\_LOCALE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-1031">15033 (0x3AB9)</span><span class="sxs-lookup"><span data-stu-id="6415e-1031">15033 (0x3AB9)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-1032">La risorsa specifica delle impostazioni locali per il messaggio desiderato non è presente.</span><span class="sxs-lookup"><span data-stu-id="6415e-1032">The locale specific resource for the desired message is not present.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-1033"><span id="ERROR_EVT_VERSION_TOO_OLD"></span><span id="error_evt_version_too_old"></span>**ERRORE \_ evt \_ versione \_ troppo \_ vecchia**</span><span class="sxs-lookup"><span data-stu-id="6415e-1033"><span id="ERROR_EVT_VERSION_TOO_OLD"></span><span id="error_evt_version_too_old"></span>**ERROR\_EVT\_VERSION\_TOO\_OLD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-1034">15034 (0x3ABA)</span><span class="sxs-lookup"><span data-stu-id="6415e-1034">15034 (0x3ABA)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-1035">La risorsa è troppo vecchia per essere compatibile.</span><span class="sxs-lookup"><span data-stu-id="6415e-1035">The resource is too old to be compatible.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-1036"><span id="ERROR_EVT_VERSION_TOO_NEW"></span><span id="error_evt_version_too_new"></span>**ERRORE \_ evt \_ versione \_ troppo \_ nuova**</span><span class="sxs-lookup"><span data-stu-id="6415e-1036"><span id="ERROR_EVT_VERSION_TOO_NEW"></span><span id="error_evt_version_too_new"></span>**ERROR\_EVT\_VERSION\_TOO\_NEW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-1037">15035 (0x3ABB)</span><span class="sxs-lookup"><span data-stu-id="6415e-1037">15035 (0x3ABB)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-1038">La risorsa è troppo nuova per essere compatibile.</span><span class="sxs-lookup"><span data-stu-id="6415e-1038">The resource is too new to be compatible.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-1039"><span id="ERROR_EVT_CANNOT_OPEN_CHANNEL_OF_QUERY"></span><span id="error_evt_cannot_open_channel_of_query"></span>**ERRORE \_ evt \_ Impossibile \_ aprire il \_ canale \_ della \_ query**</span><span class="sxs-lookup"><span data-stu-id="6415e-1039"><span id="ERROR_EVT_CANNOT_OPEN_CHANNEL_OF_QUERY"></span><span id="error_evt_cannot_open_channel_of_query"></span>**ERROR\_EVT\_CANNOT\_OPEN\_CHANNEL\_OF\_QUERY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-1040">15036 (0x3ABC)</span><span class="sxs-lookup"><span data-stu-id="6415e-1040">15036 (0x3ABC)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-1041">Il canale in corrispondenza dell'indice %1! d!</span><span class="sxs-lookup"><span data-stu-id="6415e-1041">The channel at index %1!d!</span></span> <span data-ttu-id="6415e-1042">non è possibile aprire la query.</span><span class="sxs-lookup"><span data-stu-id="6415e-1042">of the query can't be opened.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-1043"><span id="ERROR_EVT_PUBLISHER_DISABLED"></span><span id="error_evt_publisher_disabled"></span>**ERRORE \_ evt \_ Autore \_ disabilitato**</span><span class="sxs-lookup"><span data-stu-id="6415e-1043"><span id="ERROR_EVT_PUBLISHER_DISABLED"></span><span id="error_evt_publisher_disabled"></span>**ERROR\_EVT\_PUBLISHER\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-1044">15037 (0x3ABD)</span><span class="sxs-lookup"><span data-stu-id="6415e-1044">15037 (0x3ABD)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-1045">Il server di pubblicazione è stato disabilitato e la relativa risorsa non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="6415e-1045">The publisher has been disabled and its resource is not available.</span></span> <span data-ttu-id="6415e-1046">Questo problema si verifica in genere quando è in corso la disinstallazione o l'aggiornamento del server di pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="6415e-1046">This usually occurs when the publisher is in the process of being uninstalled or upgraded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-1047"><span id="ERROR_EVT_FILTER_OUT_OF_RANGE"></span><span id="error_evt_filter_out_of_range"></span>**ERRORE \_ evt \_ filtro \_ non \_ \_ compreso nell'intervallo**</span><span class="sxs-lookup"><span data-stu-id="6415e-1047"><span id="ERROR_EVT_FILTER_OUT_OF_RANGE"></span><span id="error_evt_filter_out_of_range"></span>**ERROR\_EVT\_FILTER\_OUT\_OF\_RANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-1048">15038 (0x3ABE)</span><span class="sxs-lookup"><span data-stu-id="6415e-1048">15038 (0x3ABE)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-1049">Tentativo di creare un tipo numerico non compreso nell'intervallo valido.</span><span class="sxs-lookup"><span data-stu-id="6415e-1049">Attempted to create a numeric type that is outside of its valid range.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-1050"><span id="ERROR_EC_SUBSCRIPTION_CANNOT_ACTIVATE"></span><span id="error_ec_subscription_cannot_activate"></span>**ERRORE \_ \_ \_ non è possibile attivare la sottoscrizione EC \_**</span><span class="sxs-lookup"><span data-stu-id="6415e-1050"><span id="ERROR_EC_SUBSCRIPTION_CANNOT_ACTIVATE"></span><span id="error_ec_subscription_cannot_activate"></span>**ERROR\_EC\_SUBSCRIPTION\_CANNOT\_ACTIVATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-1051">15080 (0x3AE8)</span><span class="sxs-lookup"><span data-stu-id="6415e-1051">15080 (0x3AE8)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-1052">Non è possibile attivare la sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="6415e-1052">The subscription fails to activate.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-1053"><span id="ERROR_EC_LOG_DISABLED"></span><span id="error_ec_log_disabled"></span>**ERRORE \_ \_ Registro EC \_ disabilitato**</span><span class="sxs-lookup"><span data-stu-id="6415e-1053"><span id="ERROR_EC_LOG_DISABLED"></span><span id="error_ec_log_disabled"></span>**ERROR\_EC\_LOG\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-1054">15081 (0x3AE9)</span><span class="sxs-lookup"><span data-stu-id="6415e-1054">15081 (0x3AE9)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-1055">Il log della sottoscrizione è in stato disabilitato e non può essere utilizzato per l'invio di eventi a.</span><span class="sxs-lookup"><span data-stu-id="6415e-1055">The log of the subscription is in disabled state, and can not be used to forward events to.</span></span> <span data-ttu-id="6415e-1056">Il log deve prima essere abilitato prima di poter attivare la sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="6415e-1056">The log must first be enabled before the subscription can be activated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-1057"><span id="ERROR_EC_CIRCULAR_FORWARDING"></span><span id="error_ec_circular_forwarding"></span>**ERRORE \_ di \_ inoltri circolari EC \_**</span><span class="sxs-lookup"><span data-stu-id="6415e-1057"><span id="ERROR_EC_CIRCULAR_FORWARDING"></span><span id="error_ec_circular_forwarding"></span>**ERROR\_EC\_CIRCULAR\_FORWARDING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-1058">15082 (0x3AEA)</span><span class="sxs-lookup"><span data-stu-id="6415e-1058">15082 (0x3AEA)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-1059">Quando si esegue l'invio di eventi dal computer locale a se stesso, la query della sottoscrizione non può contenere il log di destinazione della sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="6415e-1059">When forwarding events from local machine to itself, the query of the subscription can't contain target log of the subscription.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-1060"><span id="ERROR_EC_CREDSTORE_FULL"></span><span id="error_ec_credstore_full"></span>**ERRORE \_ EC \_ CREDSTORE \_ completo**</span><span class="sxs-lookup"><span data-stu-id="6415e-1060"><span id="ERROR_EC_CREDSTORE_FULL"></span><span id="error_ec_credstore_full"></span>**ERROR\_EC\_CREDSTORE\_FULL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-1061">15083 (0x3AEB)</span><span class="sxs-lookup"><span data-stu-id="6415e-1061">15083 (0x3AEB)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-1062">L'archivio delle credenziali utilizzato per salvare le credenziali è pieno.</span><span class="sxs-lookup"><span data-stu-id="6415e-1062">The credential store that is used to save credentials is full.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-1063"><span id="ERROR_EC_CRED_NOT_FOUND"></span><span id="error_ec_cred_not_found"></span>**ERRORE \_ EC \_ cred \_ non \_ trovato**</span><span class="sxs-lookup"><span data-stu-id="6415e-1063"><span id="ERROR_EC_CRED_NOT_FOUND"></span><span id="error_ec_cred_not_found"></span>**ERROR\_EC\_CRED\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-1064">15084 (0x3AEC)</span><span class="sxs-lookup"><span data-stu-id="6415e-1064">15084 (0x3AEC)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-1065">Le credenziali usate da questa sottoscrizione non sono state trovate nell'archivio credenziali.</span><span class="sxs-lookup"><span data-stu-id="6415e-1065">The credential used by this subscription can't be found in credential store.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-1066"><span id="ERROR_EC_NO_ACTIVE_CHANNEL"></span><span id="error_ec_no_active_channel"></span>**ERRORE \_ EC \_ nessun \_ \_ canale attivo**</span><span class="sxs-lookup"><span data-stu-id="6415e-1066"><span id="ERROR_EC_NO_ACTIVE_CHANNEL"></span><span id="error_ec_no_active_channel"></span>**ERROR\_EC\_NO\_ACTIVE\_CHANNEL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-1067">15085 (0x3AED)</span><span class="sxs-lookup"><span data-stu-id="6415e-1067">15085 (0x3AED)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-1068">Nessun canale attivo trovato per la query.</span><span class="sxs-lookup"><span data-stu-id="6415e-1068">No active channel is found for the query.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-1069"><span id="ERROR_MUI_FILE_NOT_FOUND"></span><span id="error_mui_file_not_found"></span>**ERRORE \_ \_ file MUI \_ non \_ trovato**</span><span class="sxs-lookup"><span data-stu-id="6415e-1069"><span id="ERROR_MUI_FILE_NOT_FOUND"></span><span id="error_mui_file_not_found"></span>**ERROR\_MUI\_FILE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-1070">15100 (0x3AFC)</span><span class="sxs-lookup"><span data-stu-id="6415e-1070">15100 (0x3AFC)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-1071">Il caricatore di risorse non è riuscito a trovare il file MUI.</span><span class="sxs-lookup"><span data-stu-id="6415e-1071">The resource loader failed to find MUI file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-1072"><span id="ERROR_MUI_INVALID_FILE"></span><span id="error_mui_invalid_file"></span>**ERRORE \_ MUI \_ file non valido \_**</span><span class="sxs-lookup"><span data-stu-id="6415e-1072"><span id="ERROR_MUI_INVALID_FILE"></span><span id="error_mui_invalid_file"></span>**ERROR\_MUI\_INVALID\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-1073">15101 (0x3AFD)</span><span class="sxs-lookup"><span data-stu-id="6415e-1073">15101 (0x3AFD)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-1074">Il caricatore di risorse non è riuscito a caricare il file MUI perché il file non supera la convalida.</span><span class="sxs-lookup"><span data-stu-id="6415e-1074">The resource loader failed to load MUI file because the file fail to pass validation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-1075"><span id="ERROR_MUI_INVALID_RC_CONFIG"></span><span id="error_mui_invalid_rc_config"></span>**ERRORE \_ MUI \_ non valido per la \_ \_ configurazione RC**</span><span class="sxs-lookup"><span data-stu-id="6415e-1075"><span id="ERROR_MUI_INVALID_RC_CONFIG"></span><span id="error_mui_invalid_rc_config"></span>**ERROR\_MUI\_INVALID\_RC\_CONFIG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-1076">15102 (0x3AFE)</span><span class="sxs-lookup"><span data-stu-id="6415e-1076">15102 (0x3AFE)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-1077">Il manifesto RC è danneggiato con dati di Garbage Collection o versioni non supportate o elementi necessari mancanti.</span><span class="sxs-lookup"><span data-stu-id="6415e-1077">The RC Manifest is corrupted with garbage data or unsupported version or missing required item.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-1078"><span id="ERROR_MUI_INVALID_LOCALE_NAME"></span><span id="error_mui_invalid_locale_name"></span>**ERRORE \_ MUI \_ \_ nome delle impostazioni locali non valido \_**</span><span class="sxs-lookup"><span data-stu-id="6415e-1078"><span id="ERROR_MUI_INVALID_LOCALE_NAME"></span><span id="error_mui_invalid_locale_name"></span>**ERROR\_MUI\_INVALID\_LOCALE\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-1079">15103 (0x3AFF)</span><span class="sxs-lookup"><span data-stu-id="6415e-1079">15103 (0x3AFF)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-1080">Il manifesto RC ha un nome di impostazioni cultura non valido.</span><span class="sxs-lookup"><span data-stu-id="6415e-1080">The RC Manifest has invalid culture name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-1081"><span id="ERROR_MUI_INVALID_ULTIMATEFALLBACK_NAME"></span><span id="error_mui_invalid_ultimatefallback_name"></span>**ERRORE \_ MUI \_ \_ nome ULTIMATEFALLBACK non valido \_**</span><span class="sxs-lookup"><span data-stu-id="6415e-1081"><span id="ERROR_MUI_INVALID_ULTIMATEFALLBACK_NAME"></span><span id="error_mui_invalid_ultimatefallback_name"></span>**ERROR\_MUI\_INVALID\_ULTIMATEFALLBACK\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-1082">15104 (0x3B00)</span><span class="sxs-lookup"><span data-stu-id="6415e-1082">15104 (0x3B00)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-1083">Il manifesto RC presenta un nome ultimatefallback non valido.</span><span class="sxs-lookup"><span data-stu-id="6415e-1083">The RC Manifest has invalid ultimatefallback name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-1084"><span id="ERROR_MUI_FILE_NOT_LOADED"></span><span id="error_mui_file_not_loaded"></span>**ERRORE \_ \_ file MUI \_ non \_ caricato**</span><span class="sxs-lookup"><span data-stu-id="6415e-1084"><span id="ERROR_MUI_FILE_NOT_LOADED"></span><span id="error_mui_file_not_loaded"></span>**ERROR\_MUI\_FILE\_NOT\_LOADED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-1085">15105 (0x3B01)</span><span class="sxs-lookup"><span data-stu-id="6415e-1085">15105 (0x3B01)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-1086">La cache del caricatore di risorse non ha caricato una voce MUI.</span><span class="sxs-lookup"><span data-stu-id="6415e-1086">The resource loader cache doesn't have loaded MUI entry.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-1087"><span id="ERROR_RESOURCE_ENUM_USER_STOP"></span><span id="error_resource_enum_user_stop"></span>**errore \_ \_ dell'enumerazione della risorsa di \_ errore \_**</span><span class="sxs-lookup"><span data-stu-id="6415e-1087"><span id="ERROR_RESOURCE_ENUM_USER_STOP"></span><span id="error_resource_enum_user_stop"></span>**ERROR\_RESOURCE\_ENUM\_USER\_STOP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-1088">15106 (0x3B02)</span><span class="sxs-lookup"><span data-stu-id="6415e-1088">15106 (0x3B02)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-1089">Enumerazione di risorse arrestata dall'utente.</span><span class="sxs-lookup"><span data-stu-id="6415e-1089">User stopped resource enumeration.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-1090"><span id="ERROR_MUI_INTLSETTINGS_UILANG_NOT_INSTALLED"></span><span id="error_mui_intlsettings_uilang_not_installed"></span>**ERRORE \_ MUI \_ INTLSETTINGS \_ UILANG \_ non \_ installato**</span><span class="sxs-lookup"><span data-stu-id="6415e-1090"><span id="ERROR_MUI_INTLSETTINGS_UILANG_NOT_INSTALLED"></span><span id="error_mui_intlsettings_uilang_not_installed"></span>**ERROR\_MUI\_INTLSETTINGS\_UILANG\_NOT\_INSTALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-1091">15107 (0x3B03)</span><span class="sxs-lookup"><span data-stu-id="6415e-1091">15107 (0x3B03)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-1092">Installazione della lingua dell'interfaccia utente non riuscita.</span><span class="sxs-lookup"><span data-stu-id="6415e-1092">UI language installation failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-1093"><span id="ERROR_MUI_INTLSETTINGS_INVALID_LOCALE_NAME"></span><span id="error_mui_intlsettings_invalid_locale_name"></span>**ERRORE \_ MUI \_ INTLSETTINGS \_ \_ nome impostazioni locali non valido \_**</span><span class="sxs-lookup"><span data-stu-id="6415e-1093"><span id="ERROR_MUI_INTLSETTINGS_INVALID_LOCALE_NAME"></span><span id="error_mui_intlsettings_invalid_locale_name"></span>**ERROR\_MUI\_INTLSETTINGS\_INVALID\_LOCALE\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-1094">15108 (0x3B04)</span><span class="sxs-lookup"><span data-stu-id="6415e-1094">15108 (0x3B04)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-1095">Installazione delle impostazioni locali non riuscita.</span><span class="sxs-lookup"><span data-stu-id="6415e-1095">Locale installation failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-1096"><span id="ERROR_MRM_RUNTIME_NO_DEFAULT_OR_NEUTRAL_RESOURCE"></span><span id="error_mrm_runtime_no_default_or_neutral_resource"></span>**ERRORE di runtime di gestione della \_ messaggistica \_ \_ senza \_ \_ risorsa predefinita o \_ neutra \_**</span><span class="sxs-lookup"><span data-stu-id="6415e-1096"><span id="ERROR_MRM_RUNTIME_NO_DEFAULT_OR_NEUTRAL_RESOURCE"></span><span id="error_mrm_runtime_no_default_or_neutral_resource"></span>**ERROR\_MRM\_RUNTIME\_NO\_DEFAULT\_OR\_NEUTRAL\_RESOURCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-1097">15110 (0x3B06)</span><span class="sxs-lookup"><span data-stu-id="6415e-1097">15110 (0x3B06)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-1098">Una risorsa non dispone di un valore predefinito o neutro.</span><span class="sxs-lookup"><span data-stu-id="6415e-1098">A resource does not have default or neutral value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-1099"><span id="ERROR_MRM_INVALID_PRICONFIG"></span><span id="error_mrm_invalid_priconfig"></span>**ERRORE di gestione della \_ messaggistica \_ file priconfig non valido \_**</span><span class="sxs-lookup"><span data-stu-id="6415e-1099"><span id="ERROR_MRM_INVALID_PRICONFIG"></span><span id="error_mrm_invalid_priconfig"></span>**ERROR\_MRM\_INVALID\_PRICONFIG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-1100">15111 (0x3B07)</span><span class="sxs-lookup"><span data-stu-id="6415e-1100">15111 (0x3B07)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-1101">File di configurazione PRI non valido.</span><span class="sxs-lookup"><span data-stu-id="6415e-1101">Invalid PRI config file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-1102"><span id="ERROR_MRM_INVALID_FILE_TYPE"></span><span id="error_mrm_invalid_file_type"></span>**\_tipo di \_ file non valido per \_ la gestione errori \_**</span><span class="sxs-lookup"><span data-stu-id="6415e-1102"><span id="ERROR_MRM_INVALID_FILE_TYPE"></span><span id="error_mrm_invalid_file_type"></span>**ERROR\_MRM\_INVALID\_FILE\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-1103">15112 (0x3B08)</span><span class="sxs-lookup"><span data-stu-id="6415e-1103">15112 (0x3B08)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-1104">Tipo di file non valido.</span><span class="sxs-lookup"><span data-stu-id="6415e-1104">Invalid file type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-1105"><span id="ERROR_MRM_UNKNOWN_QUALIFIER"></span><span id="error_mrm_unknown_qualifier"></span>**ERRORE di gestione del \_ \_ \_ qualificatore sconosciuto**</span><span class="sxs-lookup"><span data-stu-id="6415e-1105"><span id="ERROR_MRM_UNKNOWN_QUALIFIER"></span><span id="error_mrm_unknown_qualifier"></span>**ERROR\_MRM\_UNKNOWN\_QUALIFIER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-1106">15113 (0x3B09)</span><span class="sxs-lookup"><span data-stu-id="6415e-1106">15113 (0x3B09)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-1107">Qualificatore sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="6415e-1107">Unknown qualifier.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-1108"><span id="ERROR_MRM_INVALID_QUALIFIER_VALUE"></span><span id="error_mrm_invalid_qualifier_value"></span>**errore durante la gestione del \_ \_ qualificatore della messaggistica non valida \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6415e-1108"><span id="ERROR_MRM_INVALID_QUALIFIER_VALUE"></span><span id="error_mrm_invalid_qualifier_value"></span>**ERROR\_MRM\_INVALID\_QUALIFIER\_VALUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-1109">15114 (0x3B0A)</span><span class="sxs-lookup"><span data-stu-id="6415e-1109">15114 (0x3B0A)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-1110">Valore qualificatore non valido.</span><span class="sxs-lookup"><span data-stu-id="6415e-1110">Invalid qualifier value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-1111"><span id="ERROR_MRM_NO_CANDIDATE"></span><span id="error_mrm_no_candidate"></span>**ERRORE di gestione del \_ record \_ non \_ candidato**</span><span class="sxs-lookup"><span data-stu-id="6415e-1111"><span id="ERROR_MRM_NO_CANDIDATE"></span><span id="error_mrm_no_candidate"></span>**ERROR\_MRM\_NO\_CANDIDATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-1112">15115 (0x3B0B)</span><span class="sxs-lookup"><span data-stu-id="6415e-1112">15115 (0x3B0B)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-1113">Non è stato trovato alcun candidato.</span><span class="sxs-lookup"><span data-stu-id="6415e-1113">No Candidate found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-1114"><span id="ERROR_MRM_NO_MATCH_OR_DEFAULT_CANDIDATE"></span><span id="error_mrm_no_match_or_default_candidate"></span>**ERRORE di gestione della \_ messaggistica \_ non \_ corrispondente \_ o \_ \_ candidato predefinito**</span><span class="sxs-lookup"><span data-stu-id="6415e-1114"><span id="ERROR_MRM_NO_MATCH_OR_DEFAULT_CANDIDATE"></span><span id="error_mrm_no_match_or_default_candidate"></span>**ERROR\_MRM\_NO\_MATCH\_OR\_DEFAULT\_CANDIDATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-1115">15116 (0x3B0C)</span><span class="sxs-lookup"><span data-stu-id="6415e-1115">15116 (0x3B0C)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-1116">Per ResourceMap o NamedResource è presente un elemento che non ha una risorsa predefinita o neutra.</span><span class="sxs-lookup"><span data-stu-id="6415e-1116">The ResourceMap or NamedResource has an item that does not have default or neutral resource..</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-1117"><span id="ERROR_MRM_RESOURCE_TYPE_MISMATCH"></span><span id="error_mrm_resource_type_mismatch"></span>**tipo di risorsa gestione errori non \_ \_ \_ \_ corrispondente**</span><span class="sxs-lookup"><span data-stu-id="6415e-1117"><span id="ERROR_MRM_RESOURCE_TYPE_MISMATCH"></span><span id="error_mrm_resource_type_mismatch"></span>**ERROR\_MRM\_RESOURCE\_TYPE\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-1118">15117 (0x3B0D)</span><span class="sxs-lookup"><span data-stu-id="6415e-1118">15117 (0x3B0D)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-1119">Tipo ResourceCandidate non valido.</span><span class="sxs-lookup"><span data-stu-id="6415e-1119">Invalid ResourceCandidate type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-1120"><span id="ERROR_MRM_DUPLICATE_MAP_NAME"></span><span id="error_mrm_duplicate_map_name"></span>**\_ \_ nome mappa duplicato errore \_ Gestione errori \_**</span><span class="sxs-lookup"><span data-stu-id="6415e-1120"><span id="ERROR_MRM_DUPLICATE_MAP_NAME"></span><span id="error_mrm_duplicate_map_name"></span>**ERROR\_MRM\_DUPLICATE\_MAP\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-1121">15118 (0x3B0E)</span><span class="sxs-lookup"><span data-stu-id="6415e-1121">15118 (0x3B0E)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-1122">Mappa delle risorse duplicata.</span><span class="sxs-lookup"><span data-stu-id="6415e-1122">Duplicate Resource Map.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-1123"><span id="ERROR_MRM_DUPLICATE_ENTRY"></span><span id="error_mrm_duplicate_entry"></span>**\_ \_ voce duplicata di gestione errori \_**</span><span class="sxs-lookup"><span data-stu-id="6415e-1123"><span id="ERROR_MRM_DUPLICATE_ENTRY"></span><span id="error_mrm_duplicate_entry"></span>**ERROR\_MRM\_DUPLICATE\_ENTRY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-1124">15119 (0x3B0F)</span><span class="sxs-lookup"><span data-stu-id="6415e-1124">15119 (0x3B0F)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-1125">Voce duplicata.</span><span class="sxs-lookup"><span data-stu-id="6415e-1125">Duplicate Entry.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-1126"><span id="ERROR_MRM_INVALID_RESOURCE_IDENTIFIER"></span><span id="error_mrm_invalid_resource_identifier"></span>**errore durante la gestione dell' \_ \_ identificatore di risorsa non valido \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6415e-1126"><span id="ERROR_MRM_INVALID_RESOURCE_IDENTIFIER"></span><span id="error_mrm_invalid_resource_identifier"></span>**ERROR\_MRM\_INVALID\_RESOURCE\_IDENTIFIER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-1127">15120 (0x3B10)</span><span class="sxs-lookup"><span data-stu-id="6415e-1127">15120 (0x3B10)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-1128">Identificatore di risorsa non valido.</span><span class="sxs-lookup"><span data-stu-id="6415e-1128">Invalid Resource Identifier.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-1129"><span id="ERROR_MRM_FILEPATH_TOO_LONG"></span><span id="error_mrm_filepath_too_long"></span>**errore \_ filePath di gestione errori \_ \_ troppo \_ lungo**</span><span class="sxs-lookup"><span data-stu-id="6415e-1129"><span id="ERROR_MRM_FILEPATH_TOO_LONG"></span><span id="error_mrm_filepath_too_long"></span>**ERROR\_MRM\_FILEPATH\_TOO\_LONG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-1130">15121 (0x3B11)</span><span class="sxs-lookup"><span data-stu-id="6415e-1130">15121 (0x3B11)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-1131">FilePath troppo lungo.</span><span class="sxs-lookup"><span data-stu-id="6415e-1131">Filepath too long.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-1132"><span id="ERROR_MRM_UNSUPPORTED_DIRECTORY_TYPE"></span><span id="error_mrm_unsupported_directory_type"></span>**\_tipo di \_ Directory non supportato \_ dalla gestione errori di messaggistica \_**</span><span class="sxs-lookup"><span data-stu-id="6415e-1132"><span id="ERROR_MRM_UNSUPPORTED_DIRECTORY_TYPE"></span><span id="error_mrm_unsupported_directory_type"></span>**ERROR\_MRM\_UNSUPPORTED\_DIRECTORY\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-1133">15122 (0x3B12)</span><span class="sxs-lookup"><span data-stu-id="6415e-1133">15122 (0x3B12)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-1134">Tipo di directory non supportato.</span><span class="sxs-lookup"><span data-stu-id="6415e-1134">Unsupported directory type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-1135"><span id="ERROR_MRM_INVALID_PRI_FILE"></span><span id="error_mrm_invalid_pri_file"></span>**ERRORE di gestione del \_ \_ \_ file PRI non valido \_**</span><span class="sxs-lookup"><span data-stu-id="6415e-1135"><span id="ERROR_MRM_INVALID_PRI_FILE"></span><span id="error_mrm_invalid_pri_file"></span>**ERROR\_MRM\_INVALID\_PRI\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-1136">15126 (0x3B16)</span><span class="sxs-lookup"><span data-stu-id="6415e-1136">15126 (0x3B16)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-1137">File PRI non valido.</span><span class="sxs-lookup"><span data-stu-id="6415e-1137">Invalid PRI File.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-1138"><span id="ERROR_MRM_NAMED_RESOURCE_NOT_FOUND"></span><span id="error_mrm_named_resource_not_found"></span>**\_ \_ \_ \_ Impossibile trovare la risorsa \_ di gestione degli errori denominata**</span><span class="sxs-lookup"><span data-stu-id="6415e-1138"><span id="ERROR_MRM_NAMED_RESOURCE_NOT_FOUND"></span><span id="error_mrm_named_resource_not_found"></span>**ERROR\_MRM\_NAMED\_RESOURCE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-1139">15127 (0x3B17)</span><span class="sxs-lookup"><span data-stu-id="6415e-1139">15127 (0x3B17)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-1140">NamedResource non trovato.</span><span class="sxs-lookup"><span data-stu-id="6415e-1140">NamedResource Not Found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-1141"><span id="ERROR_MRM_MAP_NOT_FOUND"></span><span id="error_mrm_map_not_found"></span>**\_ \_ \_ Impossibile trovare la mappa di gestione della messaggistica degli errori \_**</span><span class="sxs-lookup"><span data-stu-id="6415e-1141"><span id="ERROR_MRM_MAP_NOT_FOUND"></span><span id="error_mrm_map_not_found"></span>**ERROR\_MRM\_MAP\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-1142">15135 (0x3B1F)</span><span class="sxs-lookup"><span data-stu-id="6415e-1142">15135 (0x3B1F)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-1143">ResourceMap non trovato.</span><span class="sxs-lookup"><span data-stu-id="6415e-1143">ResourceMap Not Found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-1144"><span id="ERROR_MRM_UNSUPPORTED_PROFILE_TYPE"></span><span id="error_mrm_unsupported_profile_type"></span>**\_tipo di \_ profilo non supportato \_ per la gestione errori di messaggistica \_**</span><span class="sxs-lookup"><span data-stu-id="6415e-1144"><span id="ERROR_MRM_UNSUPPORTED_PROFILE_TYPE"></span><span id="error_mrm_unsupported_profile_type"></span>**ERROR\_MRM\_UNSUPPORTED\_PROFILE\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-1145">15136 (0x3B20)</span><span class="sxs-lookup"><span data-stu-id="6415e-1145">15136 (0x3B20)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-1146">Tipo di profilo MRT non supportato.</span><span class="sxs-lookup"><span data-stu-id="6415e-1146">Unsupported MRT profile type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-1147"><span id="ERROR_MRM_INVALID_QUALIFIER_OPERATOR"></span><span id="error_mrm_invalid_qualifier_operator"></span>**ERRORE di gestione \_ \_ \_ qualificatore non valido \_**</span><span class="sxs-lookup"><span data-stu-id="6415e-1147"><span id="ERROR_MRM_INVALID_QUALIFIER_OPERATOR"></span><span id="error_mrm_invalid_qualifier_operator"></span>**ERROR\_MRM\_INVALID\_QUALIFIER\_OPERATOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-1148">15137 (0x3B21)</span><span class="sxs-lookup"><span data-stu-id="6415e-1148">15137 (0x3B21)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-1149">Operatore qualificatore non valido.</span><span class="sxs-lookup"><span data-stu-id="6415e-1149">Invalid qualifier operator.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-1150"><span id="ERROR_MRM_INDETERMINATE_QUALIFIER_VALUE"></span><span id="error_mrm_indeterminate_qualifier_value"></span>**\_ \_ \_ valore QUALIFICATOre indeterminato di gestione errori \_**</span><span class="sxs-lookup"><span data-stu-id="6415e-1150"><span id="ERROR_MRM_INDETERMINATE_QUALIFIER_VALUE"></span><span id="error_mrm_indeterminate_qualifier_value"></span>**ERROR\_MRM\_INDETERMINATE\_QUALIFIER\_VALUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-1151">15138 (0x3B22)</span><span class="sxs-lookup"><span data-stu-id="6415e-1151">15138 (0x3B22)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-1152">Impossibile determinare il valore del qualificatore o il valore del qualificatore non è stato impostato.</span><span class="sxs-lookup"><span data-stu-id="6415e-1152">Unable to determine qualifier value or qualifier value has not been set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-1153"><span id="ERROR_MRM_AUTOMERGE_ENABLED"></span><span id="error_mrm_automerge_enabled"></span>**errore di MERGE automatico della messaggistica di errore \_ \_ \_ abilitato**</span><span class="sxs-lookup"><span data-stu-id="6415e-1153"><span id="ERROR_MRM_AUTOMERGE_ENABLED"></span><span id="error_mrm_automerge_enabled"></span>**ERROR\_MRM\_AUTOMERGE\_ENABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-1154">15139 (0x3B23)</span><span class="sxs-lookup"><span data-stu-id="6415e-1154">15139 (0x3B23)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-1155">L'operazione di merge automatico è abilitata nel file PRI.</span><span class="sxs-lookup"><span data-stu-id="6415e-1155">Automerge is enabled in the PRI file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-1156"><span id="ERROR_MRM_TOO_MANY_RESOURCES"></span><span id="error_mrm_too_many_resources"></span>**errore durante la gestione di un \_ \_ numero eccessivo di \_ \_ risorse**</span><span class="sxs-lookup"><span data-stu-id="6415e-1156"><span id="ERROR_MRM_TOO_MANY_RESOURCES"></span><span id="error_mrm_too_many_resources"></span>**ERROR\_MRM\_TOO\_MANY\_RESOURCES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-1157">15140 (0x3B24)</span><span class="sxs-lookup"><span data-stu-id="6415e-1157">15140 (0x3B24)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-1158">Troppe risorse definite per il pacchetto.</span><span class="sxs-lookup"><span data-stu-id="6415e-1158">Too many resources defined for package.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-1159"><span id="ERROR_MCA_INVALID_CAPABILITIES_STRING"></span><span id="error_mca_invalid_capabilities_string"></span>**ERRORE \_ MCA \_ funzionalità non valide \_ \_ stringa**</span><span class="sxs-lookup"><span data-stu-id="6415e-1159"><span id="ERROR_MCA_INVALID_CAPABILITIES_STRING"></span><span id="error_mca_invalid_capabilities_string"></span>**ERROR\_MCA\_INVALID\_CAPABILITIES\_STRING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-1160">15200 (0x3B60)</span><span class="sxs-lookup"><span data-stu-id="6415e-1160">15200 (0x3B60)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-1161">Il monitoraggio ha restituito una stringa di funzionalità DDC/CI non conforme alla specifica ACCESS. bus 3,0, DDC/CI 1,1 o MCCS 2 Revision 1.</span><span class="sxs-lookup"><span data-stu-id="6415e-1161">The monitor returned a DDC/CI capabilities string that did not comply with the ACCESS.bus 3.0, DDC/CI 1.1 or MCCS 2 Revision 1 specification.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-1162"><span id="ERROR_MCA_INVALID_VCP_VERSION"></span><span id="error_mca_invalid_vcp_version"></span>**ERRORE \_ MCA \_ \_ versione VCP non valida \_**</span><span class="sxs-lookup"><span data-stu-id="6415e-1162"><span id="ERROR_MCA_INVALID_VCP_VERSION"></span><span id="error_mca_invalid_vcp_version"></span>**ERROR\_MCA\_INVALID\_VCP\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-1163">15201 (0x3B61)</span><span class="sxs-lookup"><span data-stu-id="6415e-1163">15201 (0x3B61)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-1164">Il codice VCP della versione VCP (0xDF) del monitoraggio ha restituito un valore di versione non valido.</span><span class="sxs-lookup"><span data-stu-id="6415e-1164">The monitor's VCP Version (0xDF) VCP code returned an invalid version value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-1165"><span id="ERROR_MCA_MONITOR_VIOLATES_MCCS_SPECIFICATION"></span><span id="error_mca_monitor_violates_mccs_specification"></span>**ERRORE \_ \_ Monitor MCA \_ viola la \_ \_ specifica MCCS**</span><span class="sxs-lookup"><span data-stu-id="6415e-1165"><span id="ERROR_MCA_MONITOR_VIOLATES_MCCS_SPECIFICATION"></span><span id="error_mca_monitor_violates_mccs_specification"></span>**ERROR\_MCA\_MONITOR\_VIOLATES\_MCCS\_SPECIFICATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-1166">15202 (0x3B62)</span><span class="sxs-lookup"><span data-stu-id="6415e-1166">15202 (0x3B62)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-1167">Il monitoraggio non è conforme alla specifica MCCS che attesta per il supporto.</span><span class="sxs-lookup"><span data-stu-id="6415e-1167">The monitor does not comply with the MCCS specification it claims to support.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-1168"><span id="ERROR_MCA_MCCS_VERSION_MISMATCH"></span><span id="error_mca_mccs_version_mismatch"></span>**ERRORE \_ di \_ versione di MCCS MCA non \_ \_ corrispondente**</span><span class="sxs-lookup"><span data-stu-id="6415e-1168"><span id="ERROR_MCA_MCCS_VERSION_MISMATCH"></span><span id="error_mca_mccs_version_mismatch"></span>**ERROR\_MCA\_MCCS\_VERSION\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-1169">15203 (0x3B63)</span><span class="sxs-lookup"><span data-stu-id="6415e-1169">15203 (0x3B63)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-1170">La versione di MCCS nella funzionalità MCCS ver di un monitoraggio \_ non corrisponde alla versione di MCCS che il monitoraggio segnala quando viene usato il codice VCP della versione VCP (0xDF).</span><span class="sxs-lookup"><span data-stu-id="6415e-1170">The MCCS version in a monitor's mccs\_ver capability does not match the MCCS version the monitor reports when the VCP Version (0xDF) VCP code is used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-1171"><span id="ERROR_MCA_UNSUPPORTED_MCCS_VERSION"></span><span id="error_mca_unsupported_mccs_version"></span>**ERRORE \_ MCA \_ \_ versione MCCS non supportata \_**</span><span class="sxs-lookup"><span data-stu-id="6415e-1171"><span id="ERROR_MCA_UNSUPPORTED_MCCS_VERSION"></span><span id="error_mca_unsupported_mccs_version"></span>**ERROR\_MCA\_UNSUPPORTED\_MCCS\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-1172">15204 (0x3B64)</span><span class="sxs-lookup"><span data-stu-id="6415e-1172">15204 (0x3B64)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-1173">L'API di configurazione del monitoraggio funziona solo con i monitoraggi che supportano la specifica MCCS 1,0, la specifica MCCS 2,0 o la specifica MCCS 2,0 Revisione 1.</span><span class="sxs-lookup"><span data-stu-id="6415e-1173">The Monitor Configuration API only works with monitors that support the MCCS 1.0 specification, MCCS 2.0 specification or the MCCS 2.0 Revision 1 specification.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-1174"><span id="ERROR_MCA_INTERNAL_ERROR"></span><span id="error_mca_internal_error"></span>**errore \_ interno MCA errore \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6415e-1174"><span id="ERROR_MCA_INTERNAL_ERROR"></span><span id="error_mca_internal_error"></span>**ERROR\_MCA\_INTERNAL\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-1175">15205 (0x3B65)</span><span class="sxs-lookup"><span data-stu-id="6415e-1175">15205 (0x3B65)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-1176">Si è verificato un errore interno dell'API di configurazione del monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="6415e-1176">An internal Monitor Configuration API error occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-1177"><span id="ERROR_MCA_INVALID_TECHNOLOGY_TYPE_RETURNED"></span><span id="error_mca_invalid_technology_type_returned"></span>**ERRORE \_ MCA \_ tipo di tecnologia non valido \_ \_ \_ restituito**</span><span class="sxs-lookup"><span data-stu-id="6415e-1177"><span id="ERROR_MCA_INVALID_TECHNOLOGY_TYPE_RETURNED"></span><span id="error_mca_invalid_technology_type_returned"></span>**ERROR\_MCA\_INVALID\_TECHNOLOGY\_TYPE\_RETURNED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-1178">15206 (0x3B66)</span><span class="sxs-lookup"><span data-stu-id="6415e-1178">15206 (0x3B66)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-1179">Il monitoraggio ha restituito un tipo di tecnologia di monitoraggio non valido.</span><span class="sxs-lookup"><span data-stu-id="6415e-1179">The monitor returned an invalid monitor technology type.</span></span> <span data-ttu-id="6415e-1180">CRT, plasma e LCD (TFT) sono esempi di tipi di tecnologia di monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="6415e-1180">CRT, Plasma and LCD (TFT) are examples of monitor technology types.</span></span> <span data-ttu-id="6415e-1181">Questo errore indica che il monitoraggio ha violato la specifica MCCS 2,0 o MCCS 2,0 Revisione 1.</span><span class="sxs-lookup"><span data-stu-id="6415e-1181">This error implies that the monitor violated the MCCS 2.0 or MCCS 2.0 Revision 1 specification.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-1182"><span id="ERROR_MCA_UNSUPPORTED_COLOR_TEMPERATURE"></span><span id="error_mca_unsupported_color_temperature"></span>**ERRORE per la temperatura di colore non supportata da \_ MCA \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6415e-1182"><span id="ERROR_MCA_UNSUPPORTED_COLOR_TEMPERATURE"></span><span id="error_mca_unsupported_color_temperature"></span>**ERROR\_MCA\_UNSUPPORTED\_COLOR\_TEMPERATURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-1183">15207 (0x3B67)</span><span class="sxs-lookup"><span data-stu-id="6415e-1183">15207 (0x3B67)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-1184">Il chiamante di [**SetMonitorColorTemperature**](/windows/win32/api/highlevelmonitorconfigurationapi/nf-highlevelmonitorconfigurationapi-setmonitorcolortemperature) ha specificato una temperatura di colore non supportata dal monitoraggio corrente.</span><span class="sxs-lookup"><span data-stu-id="6415e-1184">The caller of [**SetMonitorColorTemperature**](/windows/win32/api/highlevelmonitorconfigurationapi/nf-highlevelmonitorconfigurationapi-setmonitorcolortemperature) specified a color temperature that the current monitor did not support.</span></span> <span data-ttu-id="6415e-1185">Questo errore indica che il monitoraggio ha violato la specifica MCCS 2,0 o MCCS 2,0 Revisione 1.</span><span class="sxs-lookup"><span data-stu-id="6415e-1185">This error implies that the monitor violated the MCCS 2.0 or MCCS 2.0 Revision 1 specification.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-1186"><span id="ERROR_AMBIGUOUS_SYSTEM_DEVICE"></span><span id="error_ambiguous_system_device"></span>**ERRORE \_ ambiguo \_ dispositivo di sistema \_**</span><span class="sxs-lookup"><span data-stu-id="6415e-1186"><span id="ERROR_AMBIGUOUS_SYSTEM_DEVICE"></span><span id="error_ambiguous_system_device"></span>**ERROR\_AMBIGUOUS\_SYSTEM\_DEVICE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-1187">15250 (0x3B92)</span><span class="sxs-lookup"><span data-stu-id="6415e-1187">15250 (0x3B92)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-1188">Il dispositivo di sistema richiesto non può essere identificato a causa di più dispositivi indistinguibili che potenzialmente corrispondono ai criteri di identificazione.</span><span class="sxs-lookup"><span data-stu-id="6415e-1188">The requested system device cannot be identified due to multiple indistinguishable devices potentially matching the identification criteria.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-1189"><span id="ERROR_SYSTEM_DEVICE_NOT_FOUND"></span><span id="error_system_device_not_found"></span>**ERRORE \_ di \_ dispositivo di sistema \_ non \_ trovato**</span><span class="sxs-lookup"><span data-stu-id="6415e-1189"><span id="ERROR_SYSTEM_DEVICE_NOT_FOUND"></span><span id="error_system_device_not_found"></span>**ERROR\_SYSTEM\_DEVICE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-1190">15299 (0x3BC3)</span><span class="sxs-lookup"><span data-stu-id="6415e-1190">15299 (0x3BC3)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-1191">Il dispositivo di sistema richiesto non è stato trovato.</span><span class="sxs-lookup"><span data-stu-id="6415e-1191">The requested system device cannot be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-1192"><span id="ERROR_HASH_NOT_SUPPORTED"></span><span id="error_hash_not_supported"></span>**\_hash errore \_ non \_ supportato**</span><span class="sxs-lookup"><span data-stu-id="6415e-1192"><span id="ERROR_HASH_NOT_SUPPORTED"></span><span id="error_hash_not_supported"></span>**ERROR\_HASH\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-1193">15300 (0x3BC4)</span><span class="sxs-lookup"><span data-stu-id="6415e-1193">15300 (0x3BC4)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-1194">La generazione di hash per la versione hash e il tipo hash specificati non è abilitata nel server.</span><span class="sxs-lookup"><span data-stu-id="6415e-1194">Hash generation for the specified hash version and hash type is not enabled on the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-1195"><span id="ERROR_HASH_NOT_PRESENT"></span><span id="error_hash_not_present"></span>**\_hash errore \_ non \_ presente**</span><span class="sxs-lookup"><span data-stu-id="6415e-1195"><span id="ERROR_HASH_NOT_PRESENT"></span><span id="error_hash_not_present"></span>**ERROR\_HASH\_NOT\_PRESENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-1196">15301 (0x3BC5)</span><span class="sxs-lookup"><span data-stu-id="6415e-1196">15301 (0x3BC5)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-1197">L'hash richiesto dal server non è disponibile o non è più valido.</span><span class="sxs-lookup"><span data-stu-id="6415e-1197">The hash requested from the server is not available or no longer valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-1198"><span id="ERROR_SECONDARY_IC_PROVIDER_NOT_REGISTERED"></span><span id="error_secondary_ic_provider_not_registered"></span>**ERRORE \_ del \_ provider IC secondario \_ \_ non \_ registrato**</span><span class="sxs-lookup"><span data-stu-id="6415e-1198"><span id="ERROR_SECONDARY_IC_PROVIDER_NOT_REGISTERED"></span><span id="error_secondary_ic_provider_not_registered"></span>**ERROR\_SECONDARY\_IC\_PROVIDER\_NOT\_REGISTERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-1199">15321 (0x3BD9)</span><span class="sxs-lookup"><span data-stu-id="6415e-1199">15321 (0x3BD9)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-1200">L'istanza del controller di interrupt secondario che gestisce l'interrupt specificato non è registrata.</span><span class="sxs-lookup"><span data-stu-id="6415e-1200">The secondary interrupt controller instance that manages the specified interrupt is not registered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-1201"><span id="ERROR_GPIO_CLIENT_INFORMATION_INVALID"></span><span id="error_gpio_client_information_invalid"></span>**ERRORE \_ GPIO \_ \_ informazioni client \_ non valide**</span><span class="sxs-lookup"><span data-stu-id="6415e-1201"><span id="ERROR_GPIO_CLIENT_INFORMATION_INVALID"></span><span id="error_gpio_client_information_invalid"></span>**ERROR\_GPIO\_CLIENT\_INFORMATION\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-1202">15322 (0x3BDA)</span><span class="sxs-lookup"><span data-stu-id="6415e-1202">15322 (0x3BDA)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-1203">Le informazioni fornite dal driver client GPIO non sono valide.</span><span class="sxs-lookup"><span data-stu-id="6415e-1203">The information supplied by the GPIO client driver is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-1204"><span id="ERROR_GPIO_VERSION_NOT_SUPPORTED"></span><span id="error_gpio_version_not_supported"></span>**ERRORE \_ GPIO \_ versione \_ non \_ supportata**</span><span class="sxs-lookup"><span data-stu-id="6415e-1204"><span id="ERROR_GPIO_VERSION_NOT_SUPPORTED"></span><span id="error_gpio_version_not_supported"></span>**ERROR\_GPIO\_VERSION\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-1205">15323 (0x3BDB)</span><span class="sxs-lookup"><span data-stu-id="6415e-1205">15323 (0x3BDB)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-1206">La versione specificata dal driver client di GPIO non è supportata.</span><span class="sxs-lookup"><span data-stu-id="6415e-1206">The version specified by the GPIO client driver is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-1207"><span id="ERROR_GPIO_INVALID_REGISTRATION_PACKET"></span><span id="error_gpio_invalid_registration_packet"></span>**errore durante il \_ GPIO del pacchetto di \_ registrazione non valido \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6415e-1207"><span id="ERROR_GPIO_INVALID_REGISTRATION_PACKET"></span><span id="error_gpio_invalid_registration_packet"></span>**ERROR\_GPIO\_INVALID\_REGISTRATION\_PACKET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-1208">15324 (0x3BDC)</span><span class="sxs-lookup"><span data-stu-id="6415e-1208">15324 (0x3BDC)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-1209">Il pacchetto di registrazione fornito dal driver client di GPIO non è valido.</span><span class="sxs-lookup"><span data-stu-id="6415e-1209">The registration packet supplied by the GPIO client driver is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-1210"><span id="ERROR_GPIO_OPERATION_DENIED"></span><span id="error_gpio_operation_denied"></span>**ERRORE \_ GPIO \_ operazione \_ negata**</span><span class="sxs-lookup"><span data-stu-id="6415e-1210"><span id="ERROR_GPIO_OPERATION_DENIED"></span><span id="error_gpio_operation_denied"></span>**ERROR\_GPIO\_OPERATION\_DENIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-1211">15325 (0x3BDD)</span><span class="sxs-lookup"><span data-stu-id="6415e-1211">15325 (0x3BDD)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-1212">L'operazione richiesta non è supportata per l'handle specificato.</span><span class="sxs-lookup"><span data-stu-id="6415e-1212">The requested operation is not supported for the specified handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-1213"><span id="ERROR_GPIO_INCOMPATIBLE_CONNECT_MODE"></span><span id="error_gpio_incompatible_connect_mode"></span>**ERRORE \_ GPIO \_ modalità di \_ connessione incompatibile \_**</span><span class="sxs-lookup"><span data-stu-id="6415e-1213"><span id="ERROR_GPIO_INCOMPATIBLE_CONNECT_MODE"></span><span id="error_gpio_incompatible_connect_mode"></span>**ERROR\_GPIO\_INCOMPATIBLE\_CONNECT\_MODE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-1214">15326 (0x3BDE)</span><span class="sxs-lookup"><span data-stu-id="6415e-1214">15326 (0x3BDE)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-1215">La modalità di connessione richiesta è in conflitto con una modalità esistente in uno o più dei PIN specificati.</span><span class="sxs-lookup"><span data-stu-id="6415e-1215">The requested connect mode conflicts with an existing mode on one or more of the specified pins.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-1216"><span id="ERROR_GPIO_INTERRUPT_ALREADY_UNMASKED"></span><span id="error_gpio_interrupt_already_unmasked"></span>**ERRORE \_ GPIO \_ interrupt \_ già senza \_ maschera**</span><span class="sxs-lookup"><span data-stu-id="6415e-1216"><span id="ERROR_GPIO_INTERRUPT_ALREADY_UNMASKED"></span><span id="error_gpio_interrupt_already_unmasked"></span>**ERROR\_GPIO\_INTERRUPT\_ALREADY\_UNMASKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-1217">15327 (0x3BDF)</span><span class="sxs-lookup"><span data-stu-id="6415e-1217">15327 (0x3BDF)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-1218">L'interrupt richiesto per l'unmasking non è mascherato.</span><span class="sxs-lookup"><span data-stu-id="6415e-1218">The interrupt requested to be unmasked is not masked.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-1219"><span id="ERROR_CANNOT_SWITCH_RUNLEVEL"></span><span id="error_cannot_switch_runlevel"></span>**ERRORE \_ non può \_ passare a \_ runlevel**</span><span class="sxs-lookup"><span data-stu-id="6415e-1219"><span id="ERROR_CANNOT_SWITCH_RUNLEVEL"></span><span id="error_cannot_switch_runlevel"></span>**ERROR\_CANNOT\_SWITCH\_RUNLEVEL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-1220">15400 (0x3C28)</span><span class="sxs-lookup"><span data-stu-id="6415e-1220">15400 (0x3C28)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-1221">Non è possibile completare l'opzione del livello di esecuzione richiesto.</span><span class="sxs-lookup"><span data-stu-id="6415e-1221">The requested run level switch cannot be completed successfully.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-1222"><span id="ERROR_INVALID_RUNLEVEL_SETTING"></span><span id="error_invalid_runlevel_setting"></span>**ERRORE \_ \_ impostazione del runlevel non valida \_**</span><span class="sxs-lookup"><span data-stu-id="6415e-1222"><span id="ERROR_INVALID_RUNLEVEL_SETTING"></span><span id="error_invalid_runlevel_setting"></span>**ERROR\_INVALID\_RUNLEVEL\_SETTING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-1223">15401 (0x3C29)</span><span class="sxs-lookup"><span data-stu-id="6415e-1223">15401 (0x3C29)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-1224">L'impostazione del livello di esecuzione del servizio non è valida.</span><span class="sxs-lookup"><span data-stu-id="6415e-1224">The service has an invalid run level setting.</span></span> <span data-ttu-id="6415e-1225">Il livello di esecuzione per un servizio non deve essere maggiore del livello di esecuzione dei servizi dipendenti.</span><span class="sxs-lookup"><span data-stu-id="6415e-1225">The run level for a service must not be higher than the run level of its dependent services.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-1226"><span id="ERROR_RUNLEVEL_SWITCH_TIMEOUT"></span><span id="error_runlevel_switch_timeout"></span>**\_ \_ timeout switch runlevel \_ errore**</span><span class="sxs-lookup"><span data-stu-id="6415e-1226"><span id="ERROR_RUNLEVEL_SWITCH_TIMEOUT"></span><span id="error_runlevel_switch_timeout"></span>**ERROR\_RUNLEVEL\_SWITCH\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-1227">15402 (0x3C2A)</span><span class="sxs-lookup"><span data-stu-id="6415e-1227">15402 (0x3C2A)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-1228">Non è possibile completare l'opzione del livello di esecuzione richiesto perché uno o più servizi non verranno arrestati o riavviati entro il timeout specificato.</span><span class="sxs-lookup"><span data-stu-id="6415e-1228">The requested run level switch cannot be completed successfully since one or more services will not stop or restart within the specified timeout.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-1229"><span id="ERROR_RUNLEVEL_SWITCH_AGENT_TIMEOUT"></span><span id="error_runlevel_switch_agent_timeout"></span>**\_ \_ \_ timeout agente switch runlevel \_ errore**</span><span class="sxs-lookup"><span data-stu-id="6415e-1229"><span id="ERROR_RUNLEVEL_SWITCH_AGENT_TIMEOUT"></span><span id="error_runlevel_switch_agent_timeout"></span>**ERROR\_RUNLEVEL\_SWITCH\_AGENT\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-1230">15403 (0x3C2B)</span><span class="sxs-lookup"><span data-stu-id="6415e-1230">15403 (0x3C2B)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-1231">Un agente di commutazione del livello di esecuzione non ha risposto entro il timeout specificato.</span><span class="sxs-lookup"><span data-stu-id="6415e-1231">A run level switch agent did not respond within the specified timeout.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-1232"><span id="ERROR_RUNLEVEL_SWITCH_IN_PROGRESS"></span><span id="error_runlevel_switch_in_progress"></span>**l' \_ opzione di errore runlevel è \_ \_ in \_ corso**</span><span class="sxs-lookup"><span data-stu-id="6415e-1232"><span id="ERROR_RUNLEVEL_SWITCH_IN_PROGRESS"></span><span id="error_runlevel_switch_in_progress"></span>**ERROR\_RUNLEVEL\_SWITCH\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-1233">15404 (0x3C2C)</span><span class="sxs-lookup"><span data-stu-id="6415e-1233">15404 (0x3C2C)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-1234">È attualmente in corso un'opzione del livello di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="6415e-1234">A run level switch is currently in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-1235"><span id="ERROR_SERVICES_FAILED_AUTOSTART"></span><span id="error_services_failed_autostart"></span>**\_avvio automatico dei servizi di errore \_ non riuscito \_**</span><span class="sxs-lookup"><span data-stu-id="6415e-1235"><span id="ERROR_SERVICES_FAILED_AUTOSTART"></span><span id="error_services_failed_autostart"></span>**ERROR\_SERVICES\_FAILED\_AUTOSTART**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-1236">15405 (0x3C2D)</span><span class="sxs-lookup"><span data-stu-id="6415e-1236">15405 (0x3C2D)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-1237">Non è stato possibile avviare uno o più servizi durante la fase di avvio del servizio di un Commuter del livello di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="6415e-1237">One or more services failed to start during the service startup phase of a run level switch.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-1238"><span id="ERROR_COM_TASK_STOP_PENDING"></span><span id="error_com_task_stop_pending"></span>**ERRORE \_ \_ interruzione attività \_ com \_ in sospeso**</span><span class="sxs-lookup"><span data-stu-id="6415e-1238"><span id="ERROR_COM_TASK_STOP_PENDING"></span><span id="error_com_task_stop_pending"></span>**ERROR\_COM\_TASK\_STOP\_PENDING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-1239">15501 (0x3C8D)</span><span class="sxs-lookup"><span data-stu-id="6415e-1239">15501 (0x3C8D)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-1240">Non è possibile completare la richiesta di arresto dell'attività immediatamente perché è necessario più tempo per l'arresto dell'attività.</span><span class="sxs-lookup"><span data-stu-id="6415e-1240">The task stop request cannot be completed immediately since task needs more time to shutdown.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-1241"><span id="ERROR_INSTALL_OPEN_PACKAGE_FAILED"></span><span id="error_install_open_package_failed"></span>**ERRORE di \_ installazione del \_ \_ pacchetto aperto \_ non riuscito**</span><span class="sxs-lookup"><span data-stu-id="6415e-1241"><span id="ERROR_INSTALL_OPEN_PACKAGE_FAILED"></span><span id="error_install_open_package_failed"></span>**ERROR\_INSTALL\_OPEN\_PACKAGE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-1242">15600 (0x3CF0)</span><span class="sxs-lookup"><span data-stu-id="6415e-1242">15600 (0x3CF0)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-1243">Non è stato possibile aprire il pacchetto.</span><span class="sxs-lookup"><span data-stu-id="6415e-1243">Package could not be opened.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-1244"><span id="ERROR_INSTALL_PACKAGE_NOT_FOUND"></span><span id="error_install_package_not_found"></span>**ERRORE di \_ installazione \_ pacchetto \_ non \_ trovato**</span><span class="sxs-lookup"><span data-stu-id="6415e-1244"><span id="ERROR_INSTALL_PACKAGE_NOT_FOUND"></span><span id="error_install_package_not_found"></span>**ERROR\_INSTALL\_PACKAGE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-1245">15601 (0x3CF1)</span><span class="sxs-lookup"><span data-stu-id="6415e-1245">15601 (0x3CF1)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-1246">Il pacchetto non è stato trovato.</span><span class="sxs-lookup"><span data-stu-id="6415e-1246">Package was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-1247"><span id="ERROR_INSTALL_INVALID_PACKAGE"></span><span id="error_install_invalid_package"></span>**errore durante l' \_ installazione del \_ pacchetto non valido \_**</span><span class="sxs-lookup"><span data-stu-id="6415e-1247"><span id="ERROR_INSTALL_INVALID_PACKAGE"></span><span id="error_install_invalid_package"></span>**ERROR\_INSTALL\_INVALID\_PACKAGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-1248">15602 (0x3CF2)</span><span class="sxs-lookup"><span data-stu-id="6415e-1248">15602 (0x3CF2)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-1249">I dati del pacchetto non sono validi.</span><span class="sxs-lookup"><span data-stu-id="6415e-1249">Package data is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-1250"><span id="ERROR_INSTALL_RESOLVE_DEPENDENCY_FAILED"></span><span id="error_install_resolve_dependency_failed"></span>**ERRORE di \_ installazione della \_ dipendenza di risoluzione \_ \_ non riuscita**</span><span class="sxs-lookup"><span data-stu-id="6415e-1250"><span id="ERROR_INSTALL_RESOLVE_DEPENDENCY_FAILED"></span><span id="error_install_resolve_dependency_failed"></span>**ERROR\_INSTALL\_RESOLVE\_DEPENDENCY\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-1251">15603 (0x3CF3)</span><span class="sxs-lookup"><span data-stu-id="6415e-1251">15603 (0x3CF3)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-1252">Aggiornamenti del pacchetto non riusciti, dipendenza o convalida dei conflitti.</span><span class="sxs-lookup"><span data-stu-id="6415e-1252">Package failed updates, dependency or conflict validation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-1253"><span id="ERROR_INSTALL_OUT_OF_DISK_SPACE"></span><span id="error_install_out_of_disk_space"></span>**ERRORE \_ \_ di installazione \_ \_ dello spazio su disco \_ insufficiente**</span><span class="sxs-lookup"><span data-stu-id="6415e-1253"><span id="ERROR_INSTALL_OUT_OF_DISK_SPACE"></span><span id="error_install_out_of_disk_space"></span>**ERROR\_INSTALL\_OUT\_OF\_DISK\_SPACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-1254">15604 (0x3CF4)</span><span class="sxs-lookup"><span data-stu-id="6415e-1254">15604 (0x3CF4)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-1255">Spazio su disco insufficiente nel computer.</span><span class="sxs-lookup"><span data-stu-id="6415e-1255">There is not enough disk space on your computer.</span></span> <span data-ttu-id="6415e-1256">Liberare spazio e riprovare.</span><span class="sxs-lookup"><span data-stu-id="6415e-1256">Please free up some space and try again.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-1257"><span id="ERROR_INSTALL_NETWORK_FAILURE"></span><span id="error_install_network_failure"></span>**ERRORE di \_ installazione \_ rete non \_ riuscita**</span><span class="sxs-lookup"><span data-stu-id="6415e-1257"><span id="ERROR_INSTALL_NETWORK_FAILURE"></span><span id="error_install_network_failure"></span>**ERROR\_INSTALL\_NETWORK\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-1258">15605 (0x3CF5)</span><span class="sxs-lookup"><span data-stu-id="6415e-1258">15605 (0x3CF5)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-1259">Si è verificato un problema durante il download del prodotto.</span><span class="sxs-lookup"><span data-stu-id="6415e-1259">There was a problem downloading your product.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-1260"><span id="ERROR_INSTALL_REGISTRATION_FAILURE"></span><span id="error_install_registration_failure"></span>**ERRORE \_ di \_ registrazione dell'installazione \_**</span><span class="sxs-lookup"><span data-stu-id="6415e-1260"><span id="ERROR_INSTALL_REGISTRATION_FAILURE"></span><span id="error_install_registration_failure"></span>**ERROR\_INSTALL\_REGISTRATION\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-1261">15606 (0x3CF6)</span><span class="sxs-lookup"><span data-stu-id="6415e-1261">15606 (0x3CF6)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-1262">Non è stato possibile registrare il pacchetto.</span><span class="sxs-lookup"><span data-stu-id="6415e-1262">Package could not be registered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-1263"><span id="ERROR_INSTALL_DEREGISTRATION_FAILURE"></span><span id="error_install_deregistration_failure"></span>**ERRORE \_ di \_ annullamento della registrazione dell'installazione \_**</span><span class="sxs-lookup"><span data-stu-id="6415e-1263"><span id="ERROR_INSTALL_DEREGISTRATION_FAILURE"></span><span id="error_install_deregistration_failure"></span>**ERROR\_INSTALL\_DEREGISTRATION\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-1264">15607 (0x3CF7)</span><span class="sxs-lookup"><span data-stu-id="6415e-1264">15607 (0x3CF7)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-1265">Non è stato possibile annullare la registrazione del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="6415e-1265">Package could not be unregistered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-1266"><span id="ERROR_INSTALL_CANCEL"></span><span id="error_install_cancel"></span>**errore durante l' \_ installazione dell' \_ annullamento**</span><span class="sxs-lookup"><span data-stu-id="6415e-1266"><span id="ERROR_INSTALL_CANCEL"></span><span id="error_install_cancel"></span>**ERROR\_INSTALL\_CANCEL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-1267">15608 (0x3CF8)</span><span class="sxs-lookup"><span data-stu-id="6415e-1267">15608 (0x3CF8)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-1268">L'utente ha annullato la richiesta di installazione.</span><span class="sxs-lookup"><span data-stu-id="6415e-1268">User cancelled the install request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-1269"><span id="ERROR_INSTALL_FAILED"></span><span id="error_install_failed"></span>**ERRORE di \_ installazione \_**</span><span class="sxs-lookup"><span data-stu-id="6415e-1269"><span id="ERROR_INSTALL_FAILED"></span><span id="error_install_failed"></span>**ERROR\_INSTALL\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-1270">15609 (0x3CF9)</span><span class="sxs-lookup"><span data-stu-id="6415e-1270">15609 (0x3CF9)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-1271">Installazione non riuscita.</span><span class="sxs-lookup"><span data-stu-id="6415e-1271">Install failed.</span></span> <span data-ttu-id="6415e-1272">Contattare il fornitore del software.</span><span class="sxs-lookup"><span data-stu-id="6415e-1272">Please contact your software vendor.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-1273"><span id="ERROR_REMOVE_FAILED"></span><span id="error_remove_failed"></span>**\_rimozione errore \_ non riuscita**</span><span class="sxs-lookup"><span data-stu-id="6415e-1273"><span id="ERROR_REMOVE_FAILED"></span><span id="error_remove_failed"></span>**ERROR\_REMOVE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-1274">15610 (0x3CFA)</span><span class="sxs-lookup"><span data-stu-id="6415e-1274">15610 (0x3CFA)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-1275">Rimozione non riuscita.</span><span class="sxs-lookup"><span data-stu-id="6415e-1275">Removal failed.</span></span> <span data-ttu-id="6415e-1276">Contattare il fornitore del software.</span><span class="sxs-lookup"><span data-stu-id="6415e-1276">Please contact your software vendor.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-1277"><span id="ERROR_PACKAGE_ALREADY_EXISTS"></span><span id="error_package_already_exists"></span>**il \_ pacchetto degli errori \_ \_ esiste già**</span><span class="sxs-lookup"><span data-stu-id="6415e-1277"><span id="ERROR_PACKAGE_ALREADY_EXISTS"></span><span id="error_package_already_exists"></span>**ERROR\_PACKAGE\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-1278">15611 (0x3CFB)</span><span class="sxs-lookup"><span data-stu-id="6415e-1278">15611 (0x3CFB)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-1279">Il pacchetto specificato è già installato e la reinstallazione del pacchetto è stata bloccata.</span><span class="sxs-lookup"><span data-stu-id="6415e-1279">The provided package is already installed, and reinstallation of the package was blocked.</span></span> <span data-ttu-id="6415e-1280">Per informazioni dettagliate, vedere il registro eventi AppXDeployment-Server.</span><span class="sxs-lookup"><span data-stu-id="6415e-1280">Check the AppXDeployment-Server event log for details.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-1281"><span id="ERROR_NEEDS_REMEDIATION"></span><span id="error_needs_remediation"></span>**ERRORE \_ necessario \_ correzione**</span><span class="sxs-lookup"><span data-stu-id="6415e-1281"><span id="ERROR_NEEDS_REMEDIATION"></span><span id="error_needs_remediation"></span>**ERROR\_NEEDS\_REMEDIATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-1282">15612 (0x3CFC)</span><span class="sxs-lookup"><span data-stu-id="6415e-1282">15612 (0x3CFC)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-1283">Impossibile avviare l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="6415e-1283">The application cannot be started.</span></span> <span data-ttu-id="6415e-1284">Provare a reinstallare l'applicazione per risolvere il problema.</span><span class="sxs-lookup"><span data-stu-id="6415e-1284">Try reinstalling the application to fix the problem.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-1285"><span id="ERROR_INSTALL_PREREQUISITE_FAILED"></span><span id="error_install_prerequisite_failed"></span>**ERRORE di \_ installazione \_ prerequisiti \_ non riuscito**</span><span class="sxs-lookup"><span data-stu-id="6415e-1285"><span id="ERROR_INSTALL_PREREQUISITE_FAILED"></span><span id="error_install_prerequisite_failed"></span>**ERROR\_INSTALL\_PREREQUISITE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-1286">15613 (0x3CFD)</span><span class="sxs-lookup"><span data-stu-id="6415e-1286">15613 (0x3CFD)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-1287">Non è stato possibile soddisfare un prerequisito per un'installazione.</span><span class="sxs-lookup"><span data-stu-id="6415e-1287">A Prerequisite for an install could not be satisfied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-1288"><span id="ERROR_PACKAGE_REPOSITORY_CORRUPTED"></span><span id="error_package_repository_corrupted"></span>**REPOSITORY del pacchetto di errore \_ \_ \_ danneggiato**</span><span class="sxs-lookup"><span data-stu-id="6415e-1288"><span id="ERROR_PACKAGE_REPOSITORY_CORRUPTED"></span><span id="error_package_repository_corrupted"></span>**ERROR\_PACKAGE\_REPOSITORY\_CORRUPTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-1289">15614 (0x3CFE)</span><span class="sxs-lookup"><span data-stu-id="6415e-1289">15614 (0x3CFE)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-1290">Il repository del pacchetto è danneggiato.</span><span class="sxs-lookup"><span data-stu-id="6415e-1290">The package repository is corrupted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-1291"><span id="ERROR_INSTALL_POLICY_FAILURE"></span><span id="error_install_policy_failure"></span>**ERRORE di \_ installazione dei \_ criteri \_**</span><span class="sxs-lookup"><span data-stu-id="6415e-1291"><span id="ERROR_INSTALL_POLICY_FAILURE"></span><span id="error_install_policy_failure"></span>**ERROR\_INSTALL\_POLICY\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-1292">15615 (0x3CFF)</span><span class="sxs-lookup"><span data-stu-id="6415e-1292">15615 (0x3CFF)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-1293">Per installare questa applicazione, è necessario disporre di una licenza per sviluppatori Windows o di un sistema abilitato per sideload.</span><span class="sxs-lookup"><span data-stu-id="6415e-1293">To install this application you need either a Windows developer license or a sideloading-enabled system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-1294"><span id="ERROR_PACKAGE_UPDATING"></span><span id="error_package_updating"></span>**\_aggiornamento del pacchetto di errori \_**</span><span class="sxs-lookup"><span data-stu-id="6415e-1294"><span id="ERROR_PACKAGE_UPDATING"></span><span id="error_package_updating"></span>**ERROR\_PACKAGE\_UPDATING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-1295">15616 (0x3D00)</span><span class="sxs-lookup"><span data-stu-id="6415e-1295">15616 (0x3D00)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-1296">Non è possibile avviare l'applicazione perché è attualmente in fase di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="6415e-1296">The application cannot be started because it is currently updating.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-1297"><span id="ERROR_DEPLOYMENT_BLOCKED_BY_POLICY"></span><span id="error_deployment_blocked_by_policy"></span>**\_distribuzione \_ degli errori bloccata \_ dai \_ criteri**</span><span class="sxs-lookup"><span data-stu-id="6415e-1297"><span id="ERROR_DEPLOYMENT_BLOCKED_BY_POLICY"></span><span id="error_deployment_blocked_by_policy"></span>**ERROR\_DEPLOYMENT\_BLOCKED\_BY\_POLICY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-1298">15617 (0x3D01)</span><span class="sxs-lookup"><span data-stu-id="6415e-1298">15617 (0x3D01)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-1299">L'operazione di distribuzione del pacchetto è bloccata dai criteri.</span><span class="sxs-lookup"><span data-stu-id="6415e-1299">The package deployment operation is blocked by policy.</span></span> <span data-ttu-id="6415e-1300">Contattare l'amministratore di sistema.</span><span class="sxs-lookup"><span data-stu-id="6415e-1300">Please contact your system administrator.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-1301"><span id="ERROR_PACKAGES_IN_USE"></span><span id="error_packages_in_use"></span>**\_pacchetti \_ di errore in \_ uso**</span><span class="sxs-lookup"><span data-stu-id="6415e-1301"><span id="ERROR_PACKAGES_IN_USE"></span><span id="error_packages_in_use"></span>**ERROR\_PACKAGES\_IN\_USE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-1302">15618 (0x3D02)</span><span class="sxs-lookup"><span data-stu-id="6415e-1302">15618 (0x3D02)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-1303">Non è stato possibile installare il pacchetto perché le risorse modificate sono attualmente in uso.</span><span class="sxs-lookup"><span data-stu-id="6415e-1303">The package could not be installed because resources it modifies are currently in use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-1304"><span id="ERROR_RECOVERY_FILE_CORRUPT"></span><span id="error_recovery_file_corrupt"></span>**\_file di ripristino errori \_ \_ danneggiato**</span><span class="sxs-lookup"><span data-stu-id="6415e-1304"><span id="ERROR_RECOVERY_FILE_CORRUPT"></span><span id="error_recovery_file_corrupt"></span>**ERROR\_RECOVERY\_FILE\_CORRUPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-1305">15619 (0x3D03)</span><span class="sxs-lookup"><span data-stu-id="6415e-1305">15619 (0x3D03)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-1306">Non è stato possibile recuperare il pacchetto perché i dati necessari per il ripristino sono stati danneggiati.</span><span class="sxs-lookup"><span data-stu-id="6415e-1306">The package could not be recovered because necessary data for recovery have been corrupted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-1307"><span id="ERROR_INVALID_STAGED_SIGNATURE"></span><span id="error_invalid_staged_signature"></span>**ERRORE \_ di \_ firma temporanea non valida \_**</span><span class="sxs-lookup"><span data-stu-id="6415e-1307"><span id="ERROR_INVALID_STAGED_SIGNATURE"></span><span id="error_invalid_staged_signature"></span>**ERROR\_INVALID\_STAGED\_SIGNATURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-1308">15620 (0x3D04)</span><span class="sxs-lookup"><span data-stu-id="6415e-1308">15620 (0x3D04)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-1309">La firma non è valida.</span><span class="sxs-lookup"><span data-stu-id="6415e-1309">The signature is invalid.</span></span> <span data-ttu-id="6415e-1310">Per eseguire la registrazione in modalità sviluppatore, AppxSignature. p7x e AppxBlockMap.xml devono essere validi o non devono essere presenti.</span><span class="sxs-lookup"><span data-stu-id="6415e-1310">To register in developer mode, AppxSignature.p7x and AppxBlockMap.xml must be valid or should not be present.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-1311"><span id="ERROR_DELETING_EXISTING_APPLICATIONDATA_STORE_FAILED"></span><span id="error_deleting_existing_applicationdata_store_failed"></span>**errore durante l' \_ eliminazione dell' \_ \_ Archivio APPLICATIONDATA esistente \_ \_ non riuscito**</span><span class="sxs-lookup"><span data-stu-id="6415e-1311"><span id="ERROR_DELETING_EXISTING_APPLICATIONDATA_STORE_FAILED"></span><span id="error_deleting_existing_applicationdata_store_failed"></span>**ERROR\_DELETING\_EXISTING\_APPLICATIONDATA\_STORE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-1312">15621 (0x3D05)</span><span class="sxs-lookup"><span data-stu-id="6415e-1312">15621 (0x3D05)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-1313">Si è verificato un errore durante l'eliminazione dei dati dell'applicazione precedentemente esistenti del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="6415e-1313">An error occurred while deleting the package's previously existing application data.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-1314"><span id="ERROR_INSTALL_PACKAGE_DOWNGRADE"></span><span id="error_install_package_downgrade"></span>**ERRORE di \_ installazione del \_ downgrade del pacchetto \_**</span><span class="sxs-lookup"><span data-stu-id="6415e-1314"><span id="ERROR_INSTALL_PACKAGE_DOWNGRADE"></span><span id="error_install_package_downgrade"></span>**ERROR\_INSTALL\_PACKAGE\_DOWNGRADE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-1315">15622 (0x3D06)</span><span class="sxs-lookup"><span data-stu-id="6415e-1315">15622 (0x3D06)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-1316">Non è stato possibile installare il pacchetto perché è già installata una versione più recente del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="6415e-1316">The package could not be installed because a higher version of this package is already installed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-1317"><span id="ERROR_SYSTEM_NEEDS_REMEDIATION"></span><span id="error_system_needs_remediation"></span>**il \_ sistema di errori \_ richiede la \_ correzione**</span><span class="sxs-lookup"><span data-stu-id="6415e-1317"><span id="ERROR_SYSTEM_NEEDS_REMEDIATION"></span><span id="error_system_needs_remediation"></span>**ERROR\_SYSTEM\_NEEDS\_REMEDIATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-1318">15623 (0x3D07)</span><span class="sxs-lookup"><span data-stu-id="6415e-1318">15623 (0x3D07)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-1319">È stato rilevato un errore in un file binario di sistema.</span><span class="sxs-lookup"><span data-stu-id="6415e-1319">An error in a system binary was detected.</span></span> <span data-ttu-id="6415e-1320">Provare ad aggiornare il PC per risolvere il problema.</span><span class="sxs-lookup"><span data-stu-id="6415e-1320">Try refreshing the PC to fix the problem.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-1321"><span id="ERROR_APPX_INTEGRITY_FAILURE_CLR_NGEN"></span><span id="error_appx_integrity_failure_clr_ngen"></span>**errore errore di \_ \_ integrità appx \_ \_ CLR \_ NGen**</span><span class="sxs-lookup"><span data-stu-id="6415e-1321"><span id="ERROR_APPX_INTEGRITY_FAILURE_CLR_NGEN"></span><span id="error_appx_integrity_failure_clr_ngen"></span>**ERROR\_APPX\_INTEGRITY\_FAILURE\_CLR\_NGEN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-1322">15624 (0x3D08)</span><span class="sxs-lookup"><span data-stu-id="6415e-1322">15624 (0x3D08)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-1323">Rilevato un file binario NGEN CLR danneggiato nel sistema.</span><span class="sxs-lookup"><span data-stu-id="6415e-1323">A corrupted CLR NGEN binary was detected on the system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-1324"><span id="ERROR_RESILIENCY_FILE_CORRUPT"></span><span id="error_resiliency_file_corrupt"></span>**\_file di resilienza degli errori \_ \_ danneggiato**</span><span class="sxs-lookup"><span data-stu-id="6415e-1324"><span id="ERROR_RESILIENCY_FILE_CORRUPT"></span><span id="error_resiliency_file_corrupt"></span>**ERROR\_RESILIENCY\_FILE\_CORRUPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-1325">15625 (0x3D09)</span><span class="sxs-lookup"><span data-stu-id="6415e-1325">15625 (0x3D09)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-1326">Non è stato possibile riprendere l'operazione perché i dati necessari per il ripristino sono stati danneggiati.</span><span class="sxs-lookup"><span data-stu-id="6415e-1326">The operation could not be resumed because necessary data for recovery have been corrupted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-1327"><span id="ERROR_INSTALL_FIREWALL_SERVICE_NOT_RUNNING"></span><span id="error_install_firewall_service_not_running"></span>**errore durante l' \_ installazione del \_ \_ servizio firewall \_ non \_ in esecuzione**</span><span class="sxs-lookup"><span data-stu-id="6415e-1327"><span id="ERROR_INSTALL_FIREWALL_SERVICE_NOT_RUNNING"></span><span id="error_install_firewall_service_not_running"></span>**ERROR\_INSTALL\_FIREWALL\_SERVICE\_NOT\_RUNNING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-1328">15626 (0x3D0A)</span><span class="sxs-lookup"><span data-stu-id="6415e-1328">15626 (0x3D0A)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-1329">Non è stato possibile installare il pacchetto perché il servizio Windows Firewall non è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="6415e-1329">The package could not be installed because the Windows Firewall service is not running.</span></span> <span data-ttu-id="6415e-1330">Abilitare il servizio Windows Firewall e riprovare.</span><span class="sxs-lookup"><span data-stu-id="6415e-1330">Enable the Windows Firewall service and try again.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-1331"><span id="APPMODEL_ERROR_NO_PACKAGE"></span><span id="appmodel_error_no_package"></span>**\_errore APPMODEL \_ nessun \_ pacchetto**</span><span class="sxs-lookup"><span data-stu-id="6415e-1331"><span id="APPMODEL_ERROR_NO_PACKAGE"></span><span id="appmodel_error_no_package"></span>**APPMODEL\_ERROR\_NO\_PACKAGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-1332">15700 (0x3D54)</span><span class="sxs-lookup"><span data-stu-id="6415e-1332">15700 (0x3D54)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-1333">Il processo non ha un'identità del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="6415e-1333">The process has no package identity.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-1334"><span id="APPMODEL_ERROR_PACKAGE_RUNTIME_CORRUPT"></span><span id="appmodel_error_package_runtime_corrupt"></span>**\_runtime del \_ pacchetto errori APPMODEL \_ \_ danneggiato**</span><span class="sxs-lookup"><span data-stu-id="6415e-1334"><span id="APPMODEL_ERROR_PACKAGE_RUNTIME_CORRUPT"></span><span id="appmodel_error_package_runtime_corrupt"></span>**APPMODEL\_ERROR\_PACKAGE\_RUNTIME\_CORRUPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-1335">15701 (0x3D55)</span><span class="sxs-lookup"><span data-stu-id="6415e-1335">15701 (0x3D55)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-1336">Le informazioni di runtime del pacchetto sono danneggiate.</span><span class="sxs-lookup"><span data-stu-id="6415e-1336">The package runtime information is corrupted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-1337"><span id="APPMODEL_ERROR_PACKAGE_IDENTITY_CORRUPT"></span><span id="appmodel_error_package_identity_corrupt"></span>**\_identità del \_ pacchetto errori APPMODEL \_ \_ danneggiata**</span><span class="sxs-lookup"><span data-stu-id="6415e-1337"><span id="APPMODEL_ERROR_PACKAGE_IDENTITY_CORRUPT"></span><span id="appmodel_error_package_identity_corrupt"></span>**APPMODEL\_ERROR\_PACKAGE\_IDENTITY\_CORRUPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-1338">15702 (0x3D56)</span><span class="sxs-lookup"><span data-stu-id="6415e-1338">15702 (0x3D56)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-1339">L'identità del pacchetto è danneggiata.</span><span class="sxs-lookup"><span data-stu-id="6415e-1339">The package identity is corrupted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-1340"><span id="APPMODEL_ERROR_NO_APPLICATION"></span><span id="appmodel_error_no_application"></span>**\_errore APPMODEL \_ Nessuna \_ applicazione**</span><span class="sxs-lookup"><span data-stu-id="6415e-1340"><span id="APPMODEL_ERROR_NO_APPLICATION"></span><span id="appmodel_error_no_application"></span>**APPMODEL\_ERROR\_NO\_APPLICATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-1341">15703 (0x3D57)</span><span class="sxs-lookup"><span data-stu-id="6415e-1341">15703 (0x3D57)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-1342">Il processo non ha un'identità dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="6415e-1342">The process has no application identity.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-1343"><span id="ERROR_STATE_LOAD_STORE_FAILED"></span><span id="error_state_load_store_failed"></span>**\_Archivio di caricamento stato di errore \_ \_ \_ non riuscito**</span><span class="sxs-lookup"><span data-stu-id="6415e-1343"><span id="ERROR_STATE_LOAD_STORE_FAILED"></span><span id="error_state_load_store_failed"></span>**ERROR\_STATE\_LOAD\_STORE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-1344">15800 (0x3DB8)</span><span class="sxs-lookup"><span data-stu-id="6415e-1344">15800 (0x3DB8)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-1345">Il caricamento dell'archivio Stati non è riuscito.</span><span class="sxs-lookup"><span data-stu-id="6415e-1345">Loading the state store failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-1346"><span id="ERROR_STATE_GET_VERSION_FAILED"></span><span id="error_state_get_version_failed"></span>**\_ \_ Impossibile ottenere la \_ versione dello stato di \_ errore**</span><span class="sxs-lookup"><span data-stu-id="6415e-1346"><span id="ERROR_STATE_GET_VERSION_FAILED"></span><span id="error_state_get_version_failed"></span>**ERROR\_STATE\_GET\_VERSION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-1347">15801 (0x3DB9)</span><span class="sxs-lookup"><span data-stu-id="6415e-1347">15801 (0x3DB9)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-1348">Il recupero della versione dello stato per l'applicazione non è riuscito.</span><span class="sxs-lookup"><span data-stu-id="6415e-1348">Retrieving the state version for the application failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-1349"><span id="ERROR_STATE_SET_VERSION_FAILED"></span><span id="error_state_set_version_failed"></span>**versione del set di Stati di errore \_ \_ \_ \_ non riuscita**</span><span class="sxs-lookup"><span data-stu-id="6415e-1349"><span id="ERROR_STATE_SET_VERSION_FAILED"></span><span id="error_state_set_version_failed"></span>**ERROR\_STATE\_SET\_VERSION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-1350">15802 (0x3DBA)</span><span class="sxs-lookup"><span data-stu-id="6415e-1350">15802 (0x3DBA)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-1351">Impossibile impostare la versione dello stato per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="6415e-1351">Setting the state version for the application failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-1352"><span id="ERROR_STATE_STRUCTURED_RESET_FAILED"></span><span id="error_state_structured_reset_failed"></span>**\_ripristino strutturato dello stato di errore \_ \_ \_ non riuscito**</span><span class="sxs-lookup"><span data-stu-id="6415e-1352"><span id="ERROR_STATE_STRUCTURED_RESET_FAILED"></span><span id="error_state_structured_reset_failed"></span>**ERROR\_STATE\_STRUCTURED\_RESET\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-1353">15803 (0x3DBB)</span><span class="sxs-lookup"><span data-stu-id="6415e-1353">15803 (0x3DBB)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-1354">Reimpostazione dello stato strutturato dell'applicazione non riuscita.</span><span class="sxs-lookup"><span data-stu-id="6415e-1354">Resetting the structured state of the application failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-1355"><span id="ERROR_STATE_OPEN_CONTAINER_FAILED"></span><span id="error_state_open_container_failed"></span>**ERRORE \_ di \_ apertura del \_ contenitore di \_ stato di errore**</span><span class="sxs-lookup"><span data-stu-id="6415e-1355"><span id="ERROR_STATE_OPEN_CONTAINER_FAILED"></span><span id="error_state_open_container_failed"></span>**ERROR\_STATE\_OPEN\_CONTAINER\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-1356">15804 (0x3DBC)</span><span class="sxs-lookup"><span data-stu-id="6415e-1356">15804 (0x3DBC)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-1357">Il gestore degli Stati non è riuscito ad aprire il contenitore.</span><span class="sxs-lookup"><span data-stu-id="6415e-1357">State Manager failed to open the container.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-1358"><span id="ERROR_STATE_CREATE_CONTAINER_FAILED"></span><span id="error_state_create_container_failed"></span>**ERRORE \_ di \_ creazione del \_ contenitore di \_ stato di errore**</span><span class="sxs-lookup"><span data-stu-id="6415e-1358"><span id="ERROR_STATE_CREATE_CONTAINER_FAILED"></span><span id="error_state_create_container_failed"></span>**ERROR\_STATE\_CREATE\_CONTAINER\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-1359">15805 (0x3DBD)</span><span class="sxs-lookup"><span data-stu-id="6415e-1359">15805 (0x3DBD)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-1360">Gestione stato non è riuscito a creare il contenitore.</span><span class="sxs-lookup"><span data-stu-id="6415e-1360">State Manager failed to create the container.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-1361"><span id="ERROR_STATE_DELETE_CONTAINER_FAILED"></span><span id="error_state_delete_container_failed"></span>**eliminazione del contenitore di stato di errore \_ \_ \_ \_ non riuscita**</span><span class="sxs-lookup"><span data-stu-id="6415e-1361"><span id="ERROR_STATE_DELETE_CONTAINER_FAILED"></span><span id="error_state_delete_container_failed"></span>**ERROR\_STATE\_DELETE\_CONTAINER\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-1362">15806 (0x3DBE)</span><span class="sxs-lookup"><span data-stu-id="6415e-1362">15806 (0x3DBE)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-1363">Il gestore degli Stati non è riuscito a eliminare il contenitore.</span><span class="sxs-lookup"><span data-stu-id="6415e-1363">State Manager failed to delete the container.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-1364"><span id="ERROR_STATE_READ_SETTING_FAILED"></span><span id="error_state_read_setting_failed"></span>**\_impostazione di \_ lettura stato errore \_ \_ non riuscita**</span><span class="sxs-lookup"><span data-stu-id="6415e-1364"><span id="ERROR_STATE_READ_SETTING_FAILED"></span><span id="error_state_read_setting_failed"></span>**ERROR\_STATE\_READ\_SETTING\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-1365">15807 (0x3DBF)</span><span class="sxs-lookup"><span data-stu-id="6415e-1365">15807 (0x3DBF)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-1366">Il gestore degli Stati non è riuscito a leggere l'impostazione.</span><span class="sxs-lookup"><span data-stu-id="6415e-1366">State Manager failed to read the setting.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-1367"><span id="ERROR_STATE_WRITE_SETTING_FAILED"></span><span id="error_state_write_setting_failed"></span>**\_ \_ impostazione scrittura stato \_ errore \_ non riuscita**</span><span class="sxs-lookup"><span data-stu-id="6415e-1367"><span id="ERROR_STATE_WRITE_SETTING_FAILED"></span><span id="error_state_write_setting_failed"></span>**ERROR\_STATE\_WRITE\_SETTING\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-1368">15808 (0x3DC0)</span><span class="sxs-lookup"><span data-stu-id="6415e-1368">15808 (0x3DC0)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-1369">Il gestore degli Stati non è riuscito a scrivere l'impostazione.</span><span class="sxs-lookup"><span data-stu-id="6415e-1369">State Manager failed to write the setting.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-1370"><span id="ERROR_STATE_DELETE_SETTING_FAILED"></span><span id="error_state_delete_setting_failed"></span>**\_ \_ impostazione eliminazione stato \_ errore \_ non riuscita**</span><span class="sxs-lookup"><span data-stu-id="6415e-1370"><span id="ERROR_STATE_DELETE_SETTING_FAILED"></span><span id="error_state_delete_setting_failed"></span>**ERROR\_STATE\_DELETE\_SETTING\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-1371">15809 (0x3DC1)</span><span class="sxs-lookup"><span data-stu-id="6415e-1371">15809 (0x3DC1)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-1372">Il gestore degli Stati non è riuscito a eliminare l'impostazione.</span><span class="sxs-lookup"><span data-stu-id="6415e-1372">State Manager failed to delete the setting.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-1373"><span id="ERROR_STATE_QUERY_SETTING_FAILED"></span><span id="error_state_query_setting_failed"></span>**\_impostazione della query sullo stato di errore \_ \_ \_ non riuscita**</span><span class="sxs-lookup"><span data-stu-id="6415e-1373"><span id="ERROR_STATE_QUERY_SETTING_FAILED"></span><span id="error_state_query_setting_failed"></span>**ERROR\_STATE\_QUERY\_SETTING\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-1374">15810 (0x3DC2)</span><span class="sxs-lookup"><span data-stu-id="6415e-1374">15810 (0x3DC2)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-1375">Gestione stato non è riuscito a eseguire una query sull'impostazione.</span><span class="sxs-lookup"><span data-stu-id="6415e-1375">State Manager failed to query the setting.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-1376"><span id="ERROR_STATE_READ_COMPOSITE_SETTING_FAILED"></span><span id="error_state_read_composite_setting_failed"></span>**\_ \_ \_ Impossibile impostare l'impostazione composita di lettura stato \_ errore \_**</span><span class="sxs-lookup"><span data-stu-id="6415e-1376"><span id="ERROR_STATE_READ_COMPOSITE_SETTING_FAILED"></span><span id="error_state_read_composite_setting_failed"></span>**ERROR\_STATE\_READ\_COMPOSITE\_SETTING\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-1377">15811 (0x3DC3)</span><span class="sxs-lookup"><span data-stu-id="6415e-1377">15811 (0x3DC3)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-1378">Il gestore degli Stati non è riuscito a leggere l'impostazione composita.</span><span class="sxs-lookup"><span data-stu-id="6415e-1378">State Manager failed to read the composite setting.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-1379"><span id="ERROR_STATE_WRITE_COMPOSITE_SETTING_FAILED"></span><span id="error_state_write_composite_setting_failed"></span>**errore durante la \_ \_ scrittura dell' \_ impostazione composita \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6415e-1379"><span id="ERROR_STATE_WRITE_COMPOSITE_SETTING_FAILED"></span><span id="error_state_write_composite_setting_failed"></span>**ERROR\_STATE\_WRITE\_COMPOSITE\_SETTING\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-1380">15812 (0x3DC4)</span><span class="sxs-lookup"><span data-stu-id="6415e-1380">15812 (0x3DC4)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-1381">Il gestore degli Stati non è riuscito a scrivere l'impostazione composita.</span><span class="sxs-lookup"><span data-stu-id="6415e-1381">State Manager failed to write the composite setting.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-1382"><span id="ERROR_STATE_ENUMERATE_CONTAINER_FAILED"></span><span id="error_state_enumerate_container_failed"></span>**ERRORE \_ di \_ enumerazione del \_ contenitore di \_ stato di errore**</span><span class="sxs-lookup"><span data-stu-id="6415e-1382"><span id="ERROR_STATE_ENUMERATE_CONTAINER_FAILED"></span><span id="error_state_enumerate_container_failed"></span>**ERROR\_STATE\_ENUMERATE\_CONTAINER\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-1383">15813 (0x3DC5)</span><span class="sxs-lookup"><span data-stu-id="6415e-1383">15813 (0x3DC5)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-1384">Il gestore degli Stati non è riuscito a enumerare i contenitori.</span><span class="sxs-lookup"><span data-stu-id="6415e-1384">State Manager failed to enumerate the containers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-1385"><span id="ERROR_STATE_ENUMERATE_SETTINGS_FAILED"></span><span id="error_state_enumerate_settings_failed"></span>**\_ \_ Impossibile enumerare \_ le impostazioni di stato di errore \_**</span><span class="sxs-lookup"><span data-stu-id="6415e-1385"><span id="ERROR_STATE_ENUMERATE_SETTINGS_FAILED"></span><span id="error_state_enumerate_settings_failed"></span>**ERROR\_STATE\_ENUMERATE\_SETTINGS\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-1386">15814 (0x3DC6)</span><span class="sxs-lookup"><span data-stu-id="6415e-1386">15814 (0x3DC6)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-1387">Gestione stato non è riuscito a enumerare le impostazioni.</span><span class="sxs-lookup"><span data-stu-id="6415e-1387">State Manager failed to enumerate the settings.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-1388"><span id="ERROR_STATE_COMPOSITE_SETTING_VALUE_SIZE_LIMIT_EXCEEDED"></span><span id="error_state_composite_setting_value_size_limit_exceeded"></span>**\_ \_ limite dimensioni del valore dell'impostazione composita dello stato di errore \_ \_ \_ \_ \_ superato**</span><span class="sxs-lookup"><span data-stu-id="6415e-1388"><span id="ERROR_STATE_COMPOSITE_SETTING_VALUE_SIZE_LIMIT_EXCEEDED"></span><span id="error_state_composite_setting_value_size_limit_exceeded"></span>**ERROR\_STATE\_COMPOSITE\_SETTING\_VALUE\_SIZE\_LIMIT\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-1389">15815 (0x3DC7)</span><span class="sxs-lookup"><span data-stu-id="6415e-1389">15815 (0x3DC7)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-1390">La dimensione del valore dell'impostazione composita di gestione stati ha superato il limite.</span><span class="sxs-lookup"><span data-stu-id="6415e-1390">The size of the state manager composite setting value has exceeded the limit.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-1391"><span id="ERROR_STATE_SETTING_VALUE_SIZE_LIMIT_EXCEEDED"></span><span id="error_state_setting_value_size_limit_exceeded"></span>**\_ \_ \_ limite dimensioni valore impostazione stato errore \_ \_ \_ superato**</span><span class="sxs-lookup"><span data-stu-id="6415e-1391"><span id="ERROR_STATE_SETTING_VALUE_SIZE_LIMIT_EXCEEDED"></span><span id="error_state_setting_value_size_limit_exceeded"></span>**ERROR\_STATE\_SETTING\_VALUE\_SIZE\_LIMIT\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-1392">15816 (0x3DC8)</span><span class="sxs-lookup"><span data-stu-id="6415e-1392">15816 (0x3DC8)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-1393">La dimensione del valore dell'impostazione di gestione stati ha superato il limite.</span><span class="sxs-lookup"><span data-stu-id="6415e-1393">The size of the state manager setting value has exceeded the limit.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-1394"><span id="ERROR_STATE_SETTING_NAME_SIZE_LIMIT_EXCEEDED"></span><span id="error_state_setting_name_size_limit_exceeded"></span>**\_ \_ \_ limite dimensioni nome impostazione stato errore \_ \_ \_ superato**</span><span class="sxs-lookup"><span data-stu-id="6415e-1394"><span id="ERROR_STATE_SETTING_NAME_SIZE_LIMIT_EXCEEDED"></span><span id="error_state_setting_name_size_limit_exceeded"></span>**ERROR\_STATE\_SETTING\_NAME\_SIZE\_LIMIT\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-1395">15817 (0x3DC9)</span><span class="sxs-lookup"><span data-stu-id="6415e-1395">15817 (0x3DC9)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-1396">La lunghezza del nome dell'impostazione del gestore dello stato ha superato il limite.</span><span class="sxs-lookup"><span data-stu-id="6415e-1396">The length of the state manager setting name has exceeded the limit.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-1397"><span id="ERROR_STATE_CONTAINER_NAME_SIZE_LIMIT_EXCEEDED"></span><span id="error_state_container_name_size_limit_exceeded"></span>**\_ \_ \_ limite dimensioni nome contenitore stato errore \_ \_ \_ superato**</span><span class="sxs-lookup"><span data-stu-id="6415e-1397"><span id="ERROR_STATE_CONTAINER_NAME_SIZE_LIMIT_EXCEEDED"></span><span id="error_state_container_name_size_limit_exceeded"></span>**ERROR\_STATE\_CONTAINER\_NAME\_SIZE\_LIMIT\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-1398">15818 (0x3DCA)</span><span class="sxs-lookup"><span data-stu-id="6415e-1398">15818 (0x3DCA)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-1399">La lunghezza del nome del contenitore di gestione stati ha superato il limite.</span><span class="sxs-lookup"><span data-stu-id="6415e-1399">The length of the state manager container name has exceeded the limit.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6415e-1400"><span id="ERROR_API_UNAVAILABLE"></span><span id="error_api_unavailable"></span>**API di errore non \_ \_ disponibile**</span><span class="sxs-lookup"><span data-stu-id="6415e-1400"><span id="ERROR_API_UNAVAILABLE"></span><span id="error_api_unavailable"></span>**ERROR\_API\_UNAVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6415e-1401">15841 (0x3DE1)</span><span class="sxs-lookup"><span data-stu-id="6415e-1401">15841 (0x3DE1)</span></span>
</dt> <dt>



<span data-ttu-id="6415e-1402">Questa API non può essere usata nel contesto del tipo di applicazione del chiamante.</span><span class="sxs-lookup"><span data-stu-id="6415e-1402">This API cannot be used in the context of the caller's application type.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6415e-1403">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6415e-1403">Requirements</span></span>



| <span data-ttu-id="6415e-1404">Requisito</span><span class="sxs-lookup"><span data-stu-id="6415e-1404">Requirement</span></span> | <span data-ttu-id="6415e-1405">Valore</span><span class="sxs-lookup"><span data-stu-id="6415e-1405">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6415e-1406">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6415e-1406">Minimum supported client</span></span><br/> | <span data-ttu-id="6415e-1407">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="6415e-1407">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="6415e-1408">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6415e-1408">Minimum supported server</span></span><br/> | <span data-ttu-id="6415e-1409">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6415e-1409">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6415e-1410">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6415e-1410">Header</span></span><br/>                   | <dl> <span data-ttu-id="6415e-1411"><dt>WinError. h</dt></span><span class="sxs-lookup"><span data-stu-id="6415e-1411"><dt>WinError.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6415e-1412">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6415e-1412">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6415e-1413">Codici di errore di sistema</span><span class="sxs-lookup"><span data-stu-id="6415e-1413">System Error Codes</span></span>](system-error-codes.md)
</dt> </dl>

 

 
