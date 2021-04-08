---
description: Descrive i codici di errore 1700-3999 definiti nel file di intestazione WinError. h ed è destinato agli sviluppatori.
ms.assetid: 7e57c087-53e4-443d-9227-21d9eb3cc71f
title: Codici di errore di sistema (1700-3999) (WinError. h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: 23b90db71a6e2e84b28f4aafc94475e9e82e3e7a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877317"
---
# <a name="system-error-codes-1700-3999"></a><span data-ttu-id="e8037-103">Codici di errore di sistema (1700-3999)</span><span class="sxs-lookup"><span data-stu-id="e8037-103">System Error Codes (1700-3999)</span></span>

> [!NOTE]
> <span data-ttu-id="e8037-104">Queste informazioni sono destinate agli sviluppatori che effettuano il debug degli errori di sistema.</span><span class="sxs-lookup"><span data-stu-id="e8037-104">This information is intended for developers debugging system errors.</span></span> <span data-ttu-id="e8037-105">Per altri errori, ad esempio problemi con Windows Update, è disponibile un elenco di risorse nella pagina [codici di errore](system-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="e8037-105">For other errors, such as issues with Windows Update, there is a list of resources on the [Error codes](system-error-codes.md) page.</span></span>

<span data-ttu-id="e8037-106">Nell'elenco seguente vengono descritti i [codici di errore di sistema](system-error-codes.md) per gli errori da 1700 a 3999.</span><span class="sxs-lookup"><span data-stu-id="e8037-106">The following list describes [system error codes](system-error-codes.md) for errors 1700 to 3999.</span></span> <span data-ttu-id="e8037-107">Vengono restituiti dalla funzione [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) quando molte funzioni hanno esito negativo.</span><span class="sxs-lookup"><span data-stu-id="e8037-107">They are returned by the [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function when many functions fail.</span></span> <span data-ttu-id="e8037-108">Per recuperare il testo della descrizione dell'errore nell'applicazione, usare la funzione [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) con il **formato \_ Message from flag \_ di \_ sistema** .</span><span class="sxs-lookup"><span data-stu-id="e8037-108">To retrieve the description text for the error in your application, use the [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) function with the **FORMAT\_MESSAGE\_FROM\_SYSTEM** flag.</span></span>

<dl> <dt>

<span data-ttu-id="e8037-109"><span id="RPC_S_INVALID_STRING_BINDING"></span><span id="rpc_s_invalid_string_binding"></span>**\_ \_ \_ Binding stringa non valido \_ RPC**</span><span class="sxs-lookup"><span data-stu-id="e8037-109"><span id="RPC_S_INVALID_STRING_BINDING"></span><span id="rpc_s_invalid_string_binding"></span>**RPC\_S\_INVALID\_STRING\_BINDING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-110">1700 (0x6A4)</span><span class="sxs-lookup"><span data-stu-id="e8037-110">1700 (0x6A4)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-111">Binding stringa non valido.</span><span class="sxs-lookup"><span data-stu-id="e8037-111">The string binding is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-112"><span id="RPC_S_WRONG_KIND_OF_BINDING"></span><span id="rpc_s_wrong_kind_of_binding"></span>**\_ \_ \_ tipo \_ di \_ binding RPC S errato**</span><span class="sxs-lookup"><span data-stu-id="e8037-112"><span id="RPC_S_WRONG_KIND_OF_BINDING"></span><span id="rpc_s_wrong_kind_of_binding"></span>**RPC\_S\_WRONG\_KIND\_OF\_BINDING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-113">1701 (0x6A5)</span><span class="sxs-lookup"><span data-stu-id="e8037-113">1701 (0x6A5)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-114">Il tipo dell'handle di binding non è corretto.</span><span class="sxs-lookup"><span data-stu-id="e8037-114">The binding handle is not the correct type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-115"><span id="RPC_S_INVALID_BINDING"></span><span id="rpc_s_invalid_binding"></span>**\_binding RPC S \_ non valido \_**</span><span class="sxs-lookup"><span data-stu-id="e8037-115"><span id="RPC_S_INVALID_BINDING"></span><span id="rpc_s_invalid_binding"></span>**RPC\_S\_INVALID\_BINDING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-116">1702 (0x6A6)</span><span class="sxs-lookup"><span data-stu-id="e8037-116">1702 (0x6A6)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-117">Handle di binding non valido.</span><span class="sxs-lookup"><span data-stu-id="e8037-117">The binding handle is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-118"><span id="RPC_S_PROTSEQ_NOT_SUPPORTED"></span><span id="rpc_s_protseq_not_supported"></span>**RPC \_ S \_ PROTSEQ \_ non \_ supportato**</span><span class="sxs-lookup"><span data-stu-id="e8037-118"><span id="RPC_S_PROTSEQ_NOT_SUPPORTED"></span><span id="rpc_s_protseq_not_supported"></span>**RPC\_S\_PROTSEQ\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-119">1703 (0x6A7)</span><span class="sxs-lookup"><span data-stu-id="e8037-119">1703 (0x6A7)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-120">La sequenza del protocollo RPC non è supportata.</span><span class="sxs-lookup"><span data-stu-id="e8037-120">The RPC protocol sequence is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-121"><span id="RPC_S_INVALID_RPC_PROTSEQ"></span><span id="rpc_s_invalid_rpc_protseq"></span>**\_ \_ \_ PROTSEQ RPC non valido \_**</span><span class="sxs-lookup"><span data-stu-id="e8037-121"><span id="RPC_S_INVALID_RPC_PROTSEQ"></span><span id="rpc_s_invalid_rpc_protseq"></span>**RPC\_S\_INVALID\_RPC\_PROTSEQ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-122">1704 (0x6A8)</span><span class="sxs-lookup"><span data-stu-id="e8037-122">1704 (0x6A8)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-123">Sequenza del protocollo RPC non valida.</span><span class="sxs-lookup"><span data-stu-id="e8037-123">The RPC protocol sequence is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-124"><span id="RPC_S_INVALID_STRING_UUID"></span><span id="rpc_s_invalid_string_uuid"></span>**\_ \_ \_ UUID stringa non valido \_ RPC**</span><span class="sxs-lookup"><span data-stu-id="e8037-124"><span id="RPC_S_INVALID_STRING_UUID"></span><span id="rpc_s_invalid_string_uuid"></span>**RPC\_S\_INVALID\_STRING\_UUID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-125">1705 (0x6A9)</span><span class="sxs-lookup"><span data-stu-id="e8037-125">1705 (0x6A9)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-126">L'identificatore univoco universale (UUID) della stringa non è valido.</span><span class="sxs-lookup"><span data-stu-id="e8037-126">The string universal unique identifier (UUID) is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-127"><span id="RPC_S_INVALID_ENDPOINT_FORMAT"></span><span id="rpc_s_invalid_endpoint_format"></span>**\_ \_ \_ formato endpoint non valido \_ RPC**</span><span class="sxs-lookup"><span data-stu-id="e8037-127"><span id="RPC_S_INVALID_ENDPOINT_FORMAT"></span><span id="rpc_s_invalid_endpoint_format"></span>**RPC\_S\_INVALID\_ENDPOINT\_FORMAT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-128">1706 (0x6AA)</span><span class="sxs-lookup"><span data-stu-id="e8037-128">1706 (0x6AA)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-129">Il formato dell'endpoint non è valido.</span><span class="sxs-lookup"><span data-stu-id="e8037-129">The endpoint format is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-130"><span id="RPC_S_INVALID_NET_ADDR"></span><span id="rpc_s_invalid_net_addr"></span>**\_ \_ \_ \_ indirizzi NET addr non validi in RPC**</span><span class="sxs-lookup"><span data-stu-id="e8037-130"><span id="RPC_S_INVALID_NET_ADDR"></span><span id="rpc_s_invalid_net_addr"></span>**RPC\_S\_INVALID\_NET\_ADDR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-131">1707 (0x6AB)</span><span class="sxs-lookup"><span data-stu-id="e8037-131">1707 (0x6AB)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-132">L'indirizzo di rete non è valido.</span><span class="sxs-lookup"><span data-stu-id="e8037-132">The network address is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-133"><span id="RPC_S_NO_ENDPOINT_FOUND"></span><span id="rpc_s_no_endpoint_found"></span>**\_non è \_ stato \_ trovato alcun endpoint \_ RPC**</span><span class="sxs-lookup"><span data-stu-id="e8037-133"><span id="RPC_S_NO_ENDPOINT_FOUND"></span><span id="rpc_s_no_endpoint_found"></span>**RPC\_S\_NO\_ENDPOINT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-134">1708 (0x6AC)</span><span class="sxs-lookup"><span data-stu-id="e8037-134">1708 (0x6AC)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-135">Non è stato trovato alcun endpoint.</span><span class="sxs-lookup"><span data-stu-id="e8037-135">No endpoint was found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-136"><span id="RPC_S_INVALID_TIMEOUT"></span><span id="rpc_s_invalid_timeout"></span>**TIMEOUT di RPC \_ \_ non valido \_**</span><span class="sxs-lookup"><span data-stu-id="e8037-136"><span id="RPC_S_INVALID_TIMEOUT"></span><span id="rpc_s_invalid_timeout"></span>**RPC\_S\_INVALID\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-137">1709 (0x6AD)</span><span class="sxs-lookup"><span data-stu-id="e8037-137">1709 (0x6AD)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-138">Il valore di timeout non è valido.</span><span class="sxs-lookup"><span data-stu-id="e8037-138">The timeout value is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-139"><span id="RPC_S_OBJECT_NOT_FOUND"></span><span id="rpc_s_object_not_found"></span>**l' \_ oggetto RPC non è stato \_ \_ \_ trovato**</span><span class="sxs-lookup"><span data-stu-id="e8037-139"><span id="RPC_S_OBJECT_NOT_FOUND"></span><span id="rpc_s_object_not_found"></span>**RPC\_S\_OBJECT\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-140">1710 (0x6AE)</span><span class="sxs-lookup"><span data-stu-id="e8037-140">1710 (0x6AE)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-141">L'identificatore univoco universale (UUID) dell'oggetto non è stato trovato.</span><span class="sxs-lookup"><span data-stu-id="e8037-141">The object universal unique identifier (UUID) was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-142"><span id="RPC_S_ALREADY_REGISTERED"></span><span id="rpc_s_already_registered"></span>**la RPC \_ è \_ già \_ registrata**</span><span class="sxs-lookup"><span data-stu-id="e8037-142"><span id="RPC_S_ALREADY_REGISTERED"></span><span id="rpc_s_already_registered"></span>**RPC\_S\_ALREADY\_REGISTERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-143">1711 (0x6AF)</span><span class="sxs-lookup"><span data-stu-id="e8037-143">1711 (0x6AF)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-144">L'identificatore univoco universale (UUID) dell'oggetto è già stato registrato.</span><span class="sxs-lookup"><span data-stu-id="e8037-144">The object universal unique identifier (UUID) has already been registered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-145"><span id="RPC_S_TYPE_ALREADY_REGISTERED"></span><span id="rpc_s_type_already_registered"></span>**il \_ tipo RPC è \_ \_ già \_ registrato**</span><span class="sxs-lookup"><span data-stu-id="e8037-145"><span id="RPC_S_TYPE_ALREADY_REGISTERED"></span><span id="rpc_s_type_already_registered"></span>**RPC\_S\_TYPE\_ALREADY\_REGISTERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-146">1712 (0x6B0)</span><span class="sxs-lookup"><span data-stu-id="e8037-146">1712 (0x6B0)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-147">L'identificatore univoco universale (UUID) del tipo è già stato registrato.</span><span class="sxs-lookup"><span data-stu-id="e8037-147">The type universal unique identifier (UUID) has already been registered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-148"><span id="RPC_S_ALREADY_LISTENING"></span><span id="rpc_s_already_listening"></span>**RPC \_ \_ già in \_ ascolto**</span><span class="sxs-lookup"><span data-stu-id="e8037-148"><span id="RPC_S_ALREADY_LISTENING"></span><span id="rpc_s_already_listening"></span>**RPC\_S\_ALREADY\_LISTENING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-149">1713 (0x6B1)</span><span class="sxs-lookup"><span data-stu-id="e8037-149">1713 (0x6B1)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-150">Il server RPC è già in ascolto.</span><span class="sxs-lookup"><span data-stu-id="e8037-150">The RPC server is already listening.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-151"><span id="RPC_S_NO_PROTSEQS_REGISTERED"></span><span id="rpc_s_no_protseqs_registered"></span>**\_PROTSEQS RPC \_ non \_ \_ registrato**</span><span class="sxs-lookup"><span data-stu-id="e8037-151"><span id="RPC_S_NO_PROTSEQS_REGISTERED"></span><span id="rpc_s_no_protseqs_registered"></span>**RPC\_S\_NO\_PROTSEQS\_REGISTERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-152">1714 (0x6B2)</span><span class="sxs-lookup"><span data-stu-id="e8037-152">1714 (0x6B2)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-153">Nessuna sequenza di protocollo registrata.</span><span class="sxs-lookup"><span data-stu-id="e8037-153">No protocol sequences have been registered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-154"><span id="RPC_S_NOT_LISTENING"></span><span id="rpc_s_not_listening"></span>**RPC \_ \_ non in \_ ascolto**</span><span class="sxs-lookup"><span data-stu-id="e8037-154"><span id="RPC_S_NOT_LISTENING"></span><span id="rpc_s_not_listening"></span>**RPC\_S\_NOT\_LISTENING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-155">1715 (0x6B3)</span><span class="sxs-lookup"><span data-stu-id="e8037-155">1715 (0x6B3)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-156">Il server RPC non è in ascolto.</span><span class="sxs-lookup"><span data-stu-id="e8037-156">The RPC server is not listening.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-157"><span id="RPC_S_UNKNOWN_MGR_TYPE"></span><span id="rpc_s_unknown_mgr_type"></span>**tipo di gestione \_ \_ sconosciuto RPC \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e8037-157"><span id="RPC_S_UNKNOWN_MGR_TYPE"></span><span id="rpc_s_unknown_mgr_type"></span>**RPC\_S\_UNKNOWN\_MGR\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-158">1716 (0x6B4)</span><span class="sxs-lookup"><span data-stu-id="e8037-158">1716 (0x6B4)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-159">Il tipo di gestione è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="e8037-159">The manager type is unknown.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-160"><span id="RPC_S_UNKNOWN_IF"></span><span id="rpc_s_unknown_if"></span>**RPC \_ \_ sconosciuto \_ se**</span><span class="sxs-lookup"><span data-stu-id="e8037-160"><span id="RPC_S_UNKNOWN_IF"></span><span id="rpc_s_unknown_if"></span>**RPC\_S\_UNKNOWN\_IF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-161">1717 (0x6B5)</span><span class="sxs-lookup"><span data-stu-id="e8037-161">1717 (0x6B5)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-162">L'interfaccia è sconosciuta.</span><span class="sxs-lookup"><span data-stu-id="e8037-162">The interface is unknown.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-163"><span id="RPC_S_NO_BINDINGS"></span><span id="rpc_s_no_bindings"></span>**\_ \_ nessun binding RPC \_ S**</span><span class="sxs-lookup"><span data-stu-id="e8037-163"><span id="RPC_S_NO_BINDINGS"></span><span id="rpc_s_no_bindings"></span>**RPC\_S\_NO\_BINDINGS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-164">1718 (0x6B6)</span><span class="sxs-lookup"><span data-stu-id="e8037-164">1718 (0x6B6)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-165">Nessuna associazione.</span><span class="sxs-lookup"><span data-stu-id="e8037-165">There are no bindings.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-166"><span id="RPC_S_NO_PROTSEQS"></span><span id="rpc_s_no_protseqs"></span>**\_ \_ n \_ PROTSEQS di RPC**</span><span class="sxs-lookup"><span data-stu-id="e8037-166"><span id="RPC_S_NO_PROTSEQS"></span><span id="rpc_s_no_protseqs"></span>**RPC\_S\_NO\_PROTSEQS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-167">1719 (0x6B7)</span><span class="sxs-lookup"><span data-stu-id="e8037-167">1719 (0x6B7)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-168">Nessuna sequenza di protocolli.</span><span class="sxs-lookup"><span data-stu-id="e8037-168">There are no protocol sequences.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-169"><span id="RPC_S_CANT_CREATE_ENDPOINT"></span><span id="rpc_s_cant_create_endpoint"></span>**\_ \_ Impossibile creare l' \_ \_ endpoint di RPC S**</span><span class="sxs-lookup"><span data-stu-id="e8037-169"><span id="RPC_S_CANT_CREATE_ENDPOINT"></span><span id="rpc_s_cant_create_endpoint"></span>**RPC\_S\_CANT\_CREATE\_ENDPOINT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-170">1720 (0x6B8)</span><span class="sxs-lookup"><span data-stu-id="e8037-170">1720 (0x6B8)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-171">Impossibile creare l'endpoint.</span><span class="sxs-lookup"><span data-stu-id="e8037-171">The endpoint cannot be created.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-172"><span id="RPC_S_OUT_OF_RESOURCES"></span><span id="rpc_s_out_of_resources"></span>**\_ \_ risorse di RPC esaurite \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e8037-172"><span id="RPC_S_OUT_OF_RESOURCES"></span><span id="rpc_s_out_of_resources"></span>**RPC\_S\_OUT\_OF\_RESOURCES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-173">1721 (0x6B9)</span><span class="sxs-lookup"><span data-stu-id="e8037-173">1721 (0x6B9)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-174">Sono disponibili risorse insufficienti per completare questa operazione.</span><span class="sxs-lookup"><span data-stu-id="e8037-174">Not enough resources are available to complete this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-175"><span id="RPC_S_SERVER_UNAVAILABLE"></span><span id="rpc_s_server_unavailable"></span>**\_server RPC \_ non \_ disponibile**</span><span class="sxs-lookup"><span data-stu-id="e8037-175"><span id="RPC_S_SERVER_UNAVAILABLE"></span><span id="rpc_s_server_unavailable"></span>**RPC\_S\_SERVER\_UNAVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-176">1722 (0x6BA)</span><span class="sxs-lookup"><span data-stu-id="e8037-176">1722 (0x6BA)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-177">Server RPC non disponibile.</span><span class="sxs-lookup"><span data-stu-id="e8037-177">The RPC server is unavailable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-178"><span id="RPC_S_SERVER_TOO_BUSY"></span><span id="rpc_s_server_too_busy"></span>**\_server RPC \_ \_ troppo \_ occupato**</span><span class="sxs-lookup"><span data-stu-id="e8037-178"><span id="RPC_S_SERVER_TOO_BUSY"></span><span id="rpc_s_server_too_busy"></span>**RPC\_S\_SERVER\_TOO\_BUSY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-179">1723 (0x6BB)</span><span class="sxs-lookup"><span data-stu-id="e8037-179">1723 (0x6BB)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-180">Il server RPC è troppo occupato per completare questa operazione.</span><span class="sxs-lookup"><span data-stu-id="e8037-180">The RPC server is too busy to complete this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-181"><span id="RPC_S_INVALID_NETWORK_OPTIONS"></span><span id="rpc_s_invalid_network_options"></span>**\_Opzioni di \_ rete non valide per \_ RPC \_**</span><span class="sxs-lookup"><span data-stu-id="e8037-181"><span id="RPC_S_INVALID_NETWORK_OPTIONS"></span><span id="rpc_s_invalid_network_options"></span>**RPC\_S\_INVALID\_NETWORK\_OPTIONS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-182">1724 (0x6BC)</span><span class="sxs-lookup"><span data-stu-id="e8037-182">1724 (0x6BC)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-183">Le opzioni di rete non sono valide.</span><span class="sxs-lookup"><span data-stu-id="e8037-183">The network options are invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-184"><span id="RPC_S_NO_CALL_ACTIVE"></span><span id="rpc_s_no_call_active"></span>**RPC \_ \_ Nessuna \_ chiamata \_ attiva**</span><span class="sxs-lookup"><span data-stu-id="e8037-184"><span id="RPC_S_NO_CALL_ACTIVE"></span><span id="rpc_s_no_call_active"></span>**RPC\_S\_NO\_CALL\_ACTIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-185">1725 (0x6BD)</span><span class="sxs-lookup"><span data-stu-id="e8037-185">1725 (0x6BD)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-186">Non sono presenti chiamate a procedure remote attive in questo thread.</span><span class="sxs-lookup"><span data-stu-id="e8037-186">There are no remote procedure calls active on this thread.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-187"><span id="RPC_S_CALL_FAILED"></span><span id="rpc_s_call_failed"></span>**\_chiamata RPC \_ \_ non riuscita**</span><span class="sxs-lookup"><span data-stu-id="e8037-187"><span id="RPC_S_CALL_FAILED"></span><span id="rpc_s_call_failed"></span>**RPC\_S\_CALL\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-188">1726 (0x6BE)</span><span class="sxs-lookup"><span data-stu-id="e8037-188">1726 (0x6BE)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-189">La chiamata di procedura remota non è riuscita.</span><span class="sxs-lookup"><span data-stu-id="e8037-189">The remote procedure call failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-190"><span id="RPC_S_CALL_FAILED_DNE"></span><span id="rpc_s_call_failed_dne"></span>**\_chiamata RPC \_ \_ non riuscita \_ dne**</span><span class="sxs-lookup"><span data-stu-id="e8037-190"><span id="RPC_S_CALL_FAILED_DNE"></span><span id="rpc_s_call_failed_dne"></span>**RPC\_S\_CALL\_FAILED\_DNE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-191">1727 (0x6BF)</span><span class="sxs-lookup"><span data-stu-id="e8037-191">1727 (0x6BF)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-192">La chiamata di procedura remota non è riuscita e non è stata eseguita.</span><span class="sxs-lookup"><span data-stu-id="e8037-192">The remote procedure call failed and did not execute.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-193"><span id="RPC_S_PROTOCOL_ERROR"></span><span id="rpc_s_protocol_error"></span>**\_errore del \_ protocollo RPC S \_**</span><span class="sxs-lookup"><span data-stu-id="e8037-193"><span id="RPC_S_PROTOCOL_ERROR"></span><span id="rpc_s_protocol_error"></span>**RPC\_S\_PROTOCOL\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-194">1728 (0x6C0)</span><span class="sxs-lookup"><span data-stu-id="e8037-194">1728 (0x6C0)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-195">Si è verificato un errore del protocollo RPC (Remote Procedure Call).</span><span class="sxs-lookup"><span data-stu-id="e8037-195">A remote procedure call (RPC) protocol error occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-196"><span id="RPC_S_PROXY_ACCESS_DENIED"></span><span id="rpc_s_proxy_access_denied"></span>**\_ \_ accesso proxy RPC \_ \_ negato**</span><span class="sxs-lookup"><span data-stu-id="e8037-196"><span id="RPC_S_PROXY_ACCESS_DENIED"></span><span id="rpc_s_proxy_access_denied"></span>**RPC\_S\_PROXY\_ACCESS\_DENIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-197">1729 (0x6C1)</span><span class="sxs-lookup"><span data-stu-id="e8037-197">1729 (0x6C1)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-198">L'accesso al proxy HTTP è stato negato.</span><span class="sxs-lookup"><span data-stu-id="e8037-198">Access to the HTTP proxy is denied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-199"><span id="RPC_S_UNSUPPORTED_TRANS_SYN"></span><span id="rpc_s_unsupported_trans_syn"></span>**\_ \_ \_ SYN trans non supportato \_**</span><span class="sxs-lookup"><span data-stu-id="e8037-199"><span id="RPC_S_UNSUPPORTED_TRANS_SYN"></span><span id="rpc_s_unsupported_trans_syn"></span>**RPC\_S\_UNSUPPORTED\_TRANS\_SYN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-200">1730 (0x6C2)</span><span class="sxs-lookup"><span data-stu-id="e8037-200">1730 (0x6C2)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-201">La sintassi di trasferimento non è supportata dal server RPC.</span><span class="sxs-lookup"><span data-stu-id="e8037-201">The transfer syntax is not supported by the RPC server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-202"><span id="RPC_S_UNSUPPORTED_TYPE"></span><span id="rpc_s_unsupported_type"></span>**\_tipo non \_ supportato di RPC \_**</span><span class="sxs-lookup"><span data-stu-id="e8037-202"><span id="RPC_S_UNSUPPORTED_TYPE"></span><span id="rpc_s_unsupported_type"></span>**RPC\_S\_UNSUPPORTED\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-203">1732 (0x6C4)</span><span class="sxs-lookup"><span data-stu-id="e8037-203">1732 (0x6C4)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-204">Il tipo di identificatore univoco universale (UUID) non è supportato.</span><span class="sxs-lookup"><span data-stu-id="e8037-204">The universal unique identifier (UUID) type is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-205"><span id="RPC_S_INVALID_TAG"></span><span id="rpc_s_invalid_tag"></span>**il \_ \_ tag RPC non è valido \_**</span><span class="sxs-lookup"><span data-stu-id="e8037-205"><span id="RPC_S_INVALID_TAG"></span><span id="rpc_s_invalid_tag"></span>**RPC\_S\_INVALID\_TAG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-206">1733 (0x6C5)</span><span class="sxs-lookup"><span data-stu-id="e8037-206">1733 (0x6C5)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-207">Il tag non è valido.</span><span class="sxs-lookup"><span data-stu-id="e8037-207">The tag is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-208"><span id="RPC_S_INVALID_BOUND"></span><span id="rpc_s_invalid_bound"></span>**\_binding RPC \_ non valido \_**</span><span class="sxs-lookup"><span data-stu-id="e8037-208"><span id="RPC_S_INVALID_BOUND"></span><span id="rpc_s_invalid_bound"></span>**RPC\_S\_INVALID\_BOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-209">1734 (0x6C6)</span><span class="sxs-lookup"><span data-stu-id="e8037-209">1734 (0x6C6)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-210">I limiti della matrice non sono validi.</span><span class="sxs-lookup"><span data-stu-id="e8037-210">The array bounds are invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-211"><span id="RPC_S_NO_ENTRY_NAME"></span><span id="rpc_s_no_entry_name"></span>**\_ \_ nessun nome di \_ voce \_ della RPC**</span><span class="sxs-lookup"><span data-stu-id="e8037-211"><span id="RPC_S_NO_ENTRY_NAME"></span><span id="rpc_s_no_entry_name"></span>**RPC\_S\_NO\_ENTRY\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-212">1735 (0x6C7)</span><span class="sxs-lookup"><span data-stu-id="e8037-212">1735 (0x6C7)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-213">Il binding non contiene un nome di voce.</span><span class="sxs-lookup"><span data-stu-id="e8037-213">The binding does not contain an entry name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-214"><span id="RPC_S_INVALID_NAME_SYNTAX"></span><span id="rpc_s_invalid_name_syntax"></span>**la \_ sintassi del nome della RPC \_ non è valida \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e8037-214"><span id="RPC_S_INVALID_NAME_SYNTAX"></span><span id="rpc_s_invalid_name_syntax"></span>**RPC\_S\_INVALID\_NAME\_SYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-215">1736 (0x6C8)</span><span class="sxs-lookup"><span data-stu-id="e8037-215">1736 (0x6C8)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-216">La sintassi del nome non è valida.</span><span class="sxs-lookup"><span data-stu-id="e8037-216">The name syntax is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-217"><span id="RPC_S_UNSUPPORTED_NAME_SYNTAX"></span><span id="rpc_s_unsupported_name_syntax"></span>**la \_ sintassi del nome non è \_ supportata in \_ RPC \_**</span><span class="sxs-lookup"><span data-stu-id="e8037-217"><span id="RPC_S_UNSUPPORTED_NAME_SYNTAX"></span><span id="rpc_s_unsupported_name_syntax"></span>**RPC\_S\_UNSUPPORTED\_NAME\_SYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-218">1737 (0x6C9)</span><span class="sxs-lookup"><span data-stu-id="e8037-218">1737 (0x6C9)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-219">La sintassi del nome non è supportata.</span><span class="sxs-lookup"><span data-stu-id="e8037-219">The name syntax is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-220"><span id="RPC_S_UUID_NO_ADDRESS"></span><span id="rpc_s_uuid_no_address"></span>**\_UUID S \_ \_ nessun \_ Indirizzo**</span><span class="sxs-lookup"><span data-stu-id="e8037-220"><span id="RPC_S_UUID_NO_ADDRESS"></span><span id="rpc_s_uuid_no_address"></span>**RPC\_S\_UUID\_NO\_ADDRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-221">1739 (0x6CB)</span><span class="sxs-lookup"><span data-stu-id="e8037-221">1739 (0x6CB)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-222">Non è disponibile alcun indirizzo di rete da usare per costruire un identificatore univoco universale (UUID).</span><span class="sxs-lookup"><span data-stu-id="e8037-222">No network address is available to use to construct a universal unique identifier (UUID).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-223"><span id="RPC_S_DUPLICATE_ENDPOINT"></span><span id="rpc_s_duplicate_endpoint"></span>**\_ \_ endpoint DUPLICAto \_ RPC**</span><span class="sxs-lookup"><span data-stu-id="e8037-223"><span id="RPC_S_DUPLICATE_ENDPOINT"></span><span id="rpc_s_duplicate_endpoint"></span>**RPC\_S\_DUPLICATE\_ENDPOINT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-224">1740 (0x6CC)</span><span class="sxs-lookup"><span data-stu-id="e8037-224">1740 (0x6CC)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-225">L'endpoint è un duplicato.</span><span class="sxs-lookup"><span data-stu-id="e8037-225">The endpoint is a duplicate.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-226"><span id="RPC_S_UNKNOWN_AUTHN_TYPE"></span><span id="rpc_s_unknown_authn_type"></span>**\_tipo di \_ \_ autenticazione sconosciuto \_ RPC**</span><span class="sxs-lookup"><span data-stu-id="e8037-226"><span id="RPC_S_UNKNOWN_AUTHN_TYPE"></span><span id="rpc_s_unknown_authn_type"></span>**RPC\_S\_UNKNOWN\_AUTHN\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-227">1741 (0x6CD)</span><span class="sxs-lookup"><span data-stu-id="e8037-227">1741 (0x6CD)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-228">Il tipo di autenticazione è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="e8037-228">The authentication type is unknown.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-229"><span id="RPC_S_MAX_CALLS_TOO_SMALL"></span><span id="rpc_s_max_calls_too_small"></span>**il \_ \_ numero massimo di chiamate RPC è \_ \_ troppo \_ piccolo**</span><span class="sxs-lookup"><span data-stu-id="e8037-229"><span id="RPC_S_MAX_CALLS_TOO_SMALL"></span><span id="rpc_s_max_calls_too_small"></span>**RPC\_S\_MAX\_CALLS\_TOO\_SMALL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-230">1742 (0x6CE)</span><span class="sxs-lookup"><span data-stu-id="e8037-230">1742 (0x6CE)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-231">Il numero massimo di chiamate è troppo piccolo.</span><span class="sxs-lookup"><span data-stu-id="e8037-231">The maximum number of calls is too small.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-232"><span id="RPC_S_STRING_TOO_LONG"></span><span id="rpc_s_string_too_long"></span>**\_stringa RPC \_ \_ troppo \_ lungo**</span><span class="sxs-lookup"><span data-stu-id="e8037-232"><span id="RPC_S_STRING_TOO_LONG"></span><span id="rpc_s_string_too_long"></span>**RPC\_S\_STRING\_TOO\_LONG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-233">1743 (0x6CF)</span><span class="sxs-lookup"><span data-stu-id="e8037-233">1743 (0x6CF)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-234">Stringa troppo lunga.</span><span class="sxs-lookup"><span data-stu-id="e8037-234">The string is too long.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-235"><span id="RPC_S_PROTSEQ_NOT_FOUND"></span><span id="rpc_s_protseq_not_found"></span>**RPC \_ S \_ PROTSEQ \_ non \_ trovato**</span><span class="sxs-lookup"><span data-stu-id="e8037-235"><span id="RPC_S_PROTSEQ_NOT_FOUND"></span><span id="rpc_s_protseq_not_found"></span>**RPC\_S\_PROTSEQ\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-236">1744 (0x6D0)</span><span class="sxs-lookup"><span data-stu-id="e8037-236">1744 (0x6D0)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-237">La sequenza del protocollo RPC non è stata trovata.</span><span class="sxs-lookup"><span data-stu-id="e8037-237">The RPC protocol sequence was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-238"><span id="RPC_S_PROCNUM_OUT_OF_RANGE"></span><span id="rpc_s_procnum_out_of_range"></span>**PROCNUM RPC non \_ \_ compreso nell' \_ \_ \_ intervallo**</span><span class="sxs-lookup"><span data-stu-id="e8037-238"><span id="RPC_S_PROCNUM_OUT_OF_RANGE"></span><span id="rpc_s_procnum_out_of_range"></span>**RPC\_S\_PROCNUM\_OUT\_OF\_RANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-239">1745 (0x6D1)</span><span class="sxs-lookup"><span data-stu-id="e8037-239">1745 (0x6D1)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-240">Il numero di procedura non è compreso nell'intervallo.</span><span class="sxs-lookup"><span data-stu-id="e8037-240">The procedure number is out of range.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-241"><span id="RPC_S_BINDING_HAS_NO_AUTH"></span><span id="rpc_s_binding_has_no_auth"></span>**\_binding RPC \_ \_ \_ non privo di \_ autenticazione**</span><span class="sxs-lookup"><span data-stu-id="e8037-241"><span id="RPC_S_BINDING_HAS_NO_AUTH"></span><span id="rpc_s_binding_has_no_auth"></span>**RPC\_S\_BINDING\_HAS\_NO\_AUTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-242">1746 (0x6D2)</span><span class="sxs-lookup"><span data-stu-id="e8037-242">1746 (0x6D2)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-243">Il binding non contiene informazioni di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="e8037-243">The binding does not contain any authentication information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-244"><span id="RPC_S_UNKNOWN_AUTHN_SERVICE"></span><span id="rpc_s_unknown_authn_service"></span>**\_ \_ \_ servizio AuthN sconosciuto di \_ RPC**</span><span class="sxs-lookup"><span data-stu-id="e8037-244"><span id="RPC_S_UNKNOWN_AUTHN_SERVICE"></span><span id="rpc_s_unknown_authn_service"></span>**RPC\_S\_UNKNOWN\_AUTHN\_SERVICE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-245">1747 (0x6D3)</span><span class="sxs-lookup"><span data-stu-id="e8037-245">1747 (0x6D3)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-246">Il servizio di autenticazione è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="e8037-246">The authentication service is unknown.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-247"><span id="RPC_S_UNKNOWN_AUTHN_LEVEL"></span><span id="rpc_s_unknown_authn_level"></span>**\_ \_ \_ livello auth sconosciuto \_ di RPC**</span><span class="sxs-lookup"><span data-stu-id="e8037-247"><span id="RPC_S_UNKNOWN_AUTHN_LEVEL"></span><span id="rpc_s_unknown_authn_level"></span>**RPC\_S\_UNKNOWN\_AUTHN\_LEVEL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-248">1748 (0x6D4)</span><span class="sxs-lookup"><span data-stu-id="e8037-248">1748 (0x6D4)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-249">Il livello di autenticazione è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="e8037-249">The authentication level is unknown.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-250"><span id="RPC_S_INVALID_AUTH_IDENTITY"></span><span id="rpc_s_invalid_auth_identity"></span>**\_ \_ \_ identità autenticazione non valida \_ RPC**</span><span class="sxs-lookup"><span data-stu-id="e8037-250"><span id="RPC_S_INVALID_AUTH_IDENTITY"></span><span id="rpc_s_invalid_auth_identity"></span>**RPC\_S\_INVALID\_AUTH\_IDENTITY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-251">1749 (0x6D5)</span><span class="sxs-lookup"><span data-stu-id="e8037-251">1749 (0x6D5)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-252">Il contesto di sicurezza non è valido.</span><span class="sxs-lookup"><span data-stu-id="e8037-252">The security context is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-253"><span id="RPC_S_UNKNOWN_AUTHZ_SERVICE"></span><span id="rpc_s_unknown_authz_service"></span>**\_ \_ \_ servizio AUTHZ sconosciuto \_ RPC**</span><span class="sxs-lookup"><span data-stu-id="e8037-253"><span id="RPC_S_UNKNOWN_AUTHZ_SERVICE"></span><span id="rpc_s_unknown_authz_service"></span>**RPC\_S\_UNKNOWN\_AUTHZ\_SERVICE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-254">1750 (0x6D6)</span><span class="sxs-lookup"><span data-stu-id="e8037-254">1750 (0x6D6)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-255">Il servizio di autorizzazione è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="e8037-255">The authorization service is unknown.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-256"><span id="EPT_S_INVALID_ENTRY"></span><span id="ept_s_invalid_entry"></span>**\_ \_ voce non valida per EPT \_**</span><span class="sxs-lookup"><span data-stu-id="e8037-256"><span id="EPT_S_INVALID_ENTRY"></span><span id="ept_s_invalid_entry"></span>**EPT\_S\_INVALID\_ENTRY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-257">1751 (0x6D7)</span><span class="sxs-lookup"><span data-stu-id="e8037-257">1751 (0x6D7)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-258">La voce non è valida.</span><span class="sxs-lookup"><span data-stu-id="e8037-258">The entry is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-259"><span id="EPT_S_CANT_PERFORM_OP"></span><span id="ept_s_cant_perform_op"></span>**\_ \_ \_ operazioni eseguibili di EPT S \_**</span><span class="sxs-lookup"><span data-stu-id="e8037-259"><span id="EPT_S_CANT_PERFORM_OP"></span><span id="ept_s_cant_perform_op"></span>**EPT\_S\_CANT\_PERFORM\_OP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-260">1752 (0x6D8)</span><span class="sxs-lookup"><span data-stu-id="e8037-260">1752 (0x6D8)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-261">L'endpoint server non è in grado di eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="e8037-261">The server endpoint cannot perform the operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-262"><span id="EPT_S_NOT_REGISTERED"></span><span id="ept_s_not_registered"></span>**EPT \_ S \_ non \_ registrato**</span><span class="sxs-lookup"><span data-stu-id="e8037-262"><span id="EPT_S_NOT_REGISTERED"></span><span id="ept_s_not_registered"></span>**EPT\_S\_NOT\_REGISTERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-263">1753 (0x6D9)</span><span class="sxs-lookup"><span data-stu-id="e8037-263">1753 (0x6D9)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-264">Nessun endpoint disponibile nel mapper degli endpoint.</span><span class="sxs-lookup"><span data-stu-id="e8037-264">There are no more endpoints available from the endpoint mapper.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-265"><span id="RPC_S_NOTHING_TO_EXPORT"></span><span id="rpc_s_nothing_to_export"></span>**\_nessun elemento \_ RPC \_ da \_ esportare**</span><span class="sxs-lookup"><span data-stu-id="e8037-265"><span id="RPC_S_NOTHING_TO_EXPORT"></span><span id="rpc_s_nothing_to_export"></span>**RPC\_S\_NOTHING\_TO\_EXPORT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-266">1754 (0x6DA)</span><span class="sxs-lookup"><span data-stu-id="e8037-266">1754 (0x6DA)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-267">Non sono state esportate interfacce.</span><span class="sxs-lookup"><span data-stu-id="e8037-267">No interfaces have been exported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-268"><span id="RPC_S_INCOMPLETE_NAME"></span><span id="rpc_s_incomplete_name"></span>**\_nome non \_ completo \_ RPC**</span><span class="sxs-lookup"><span data-stu-id="e8037-268"><span id="RPC_S_INCOMPLETE_NAME"></span><span id="rpc_s_incomplete_name"></span>**RPC\_S\_INCOMPLETE\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-269">1755 (0x6DB)</span><span class="sxs-lookup"><span data-stu-id="e8037-269">1755 (0x6DB)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-270">Il nome della voce è incompleto.</span><span class="sxs-lookup"><span data-stu-id="e8037-270">The entry name is incomplete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-271"><span id="RPC_S_INVALID_VERS_OPTION"></span><span id="rpc_s_invalid_vers_option"></span>**RPC \_ S \_ \_ opzione vers non valida \_**</span><span class="sxs-lookup"><span data-stu-id="e8037-271"><span id="RPC_S_INVALID_VERS_OPTION"></span><span id="rpc_s_invalid_vers_option"></span>**RPC\_S\_INVALID\_VERS\_OPTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-272">1756 (0x6DC)</span><span class="sxs-lookup"><span data-stu-id="e8037-272">1756 (0x6DC)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-273">L'opzione version non è valida.</span><span class="sxs-lookup"><span data-stu-id="e8037-273">The version option is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-274"><span id="RPC_S_NO_MORE_MEMBERS"></span><span id="rpc_s_no_more_members"></span>**\_ \_ nessun \_ altro \_ membro della RPC**</span><span class="sxs-lookup"><span data-stu-id="e8037-274"><span id="RPC_S_NO_MORE_MEMBERS"></span><span id="rpc_s_no_more_members"></span>**RPC\_S\_NO\_MORE\_MEMBERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-275">1757 (0x6DD)</span><span class="sxs-lookup"><span data-stu-id="e8037-275">1757 (0x6DD)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-276">Non sono disponibili altri membri.</span><span class="sxs-lookup"><span data-stu-id="e8037-276">There are no more members.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-277"><span id="RPC_S_NOT_ALL_OBJS_UNEXPORTED"></span><span id="rpc_s_not_all_objs_unexported"></span>**RPC \_ \_ non \_ tutti i \_ obj non \_ esportati**</span><span class="sxs-lookup"><span data-stu-id="e8037-277"><span id="RPC_S_NOT_ALL_OBJS_UNEXPORTED"></span><span id="rpc_s_not_all_objs_unexported"></span>**RPC\_S\_NOT\_ALL\_OBJS\_UNEXPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-278">1758 (0x6DE)</span><span class="sxs-lookup"><span data-stu-id="e8037-278">1758 (0x6DE)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-279">Non è necessario annullarne l'esportazione.</span><span class="sxs-lookup"><span data-stu-id="e8037-279">There is nothing to unexport.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-280"><span id="RPC_S_INTERFACE_NOT_FOUND"></span><span id="rpc_s_interface_not_found"></span>**\_interfaccia RPC \_ \_ non \_ trovata**</span><span class="sxs-lookup"><span data-stu-id="e8037-280"><span id="RPC_S_INTERFACE_NOT_FOUND"></span><span id="rpc_s_interface_not_found"></span>**RPC\_S\_INTERFACE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-281">1759 (0x6DF)</span><span class="sxs-lookup"><span data-stu-id="e8037-281">1759 (0x6DF)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-282">L'interfaccia non è stata trovata.</span><span class="sxs-lookup"><span data-stu-id="e8037-282">The interface was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-283"><span id="RPC_S_ENTRY_ALREADY_EXISTS"></span><span id="rpc_s_entry_already_exists"></span>**la \_ \_ voce RPC \_ \_ esiste già**</span><span class="sxs-lookup"><span data-stu-id="e8037-283"><span id="RPC_S_ENTRY_ALREADY_EXISTS"></span><span id="rpc_s_entry_already_exists"></span>**RPC\_S\_ENTRY\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-284">1760 (0x6E0)</span><span class="sxs-lookup"><span data-stu-id="e8037-284">1760 (0x6E0)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-285">La voce esiste già.</span><span class="sxs-lookup"><span data-stu-id="e8037-285">The entry already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-286"><span id="RPC_S_ENTRY_NOT_FOUND"></span><span id="rpc_s_entry_not_found"></span>**la \_ \_ voce RPC \_ non è \_ stata trovata**</span><span class="sxs-lookup"><span data-stu-id="e8037-286"><span id="RPC_S_ENTRY_NOT_FOUND"></span><span id="rpc_s_entry_not_found"></span>**RPC\_S\_ENTRY\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-287">1761 (0x6E1)</span><span class="sxs-lookup"><span data-stu-id="e8037-287">1761 (0x6E1)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-288">La voce non è stata trovata.</span><span class="sxs-lookup"><span data-stu-id="e8037-288">The entry is not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-289"><span id="RPC_S_NAME_SERVICE_UNAVAILABLE"></span><span id="rpc_s_name_service_unavailable"></span>**\_ \_ servizio nome RPC \_ non \_ disponibile**</span><span class="sxs-lookup"><span data-stu-id="e8037-289"><span id="RPC_S_NAME_SERVICE_UNAVAILABLE"></span><span id="rpc_s_name_service_unavailable"></span>**RPC\_S\_NAME\_SERVICE\_UNAVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-290">1762 (0x6E2)</span><span class="sxs-lookup"><span data-stu-id="e8037-290">1762 (0x6E2)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-291">Il servizio nome non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="e8037-291">The name service is unavailable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-292"><span id="RPC_S_INVALID_NAF_ID"></span><span id="rpc_s_invalid_naf_id"></span>**\_ \_ \_ ID NAF non valido \_ in RPC**</span><span class="sxs-lookup"><span data-stu-id="e8037-292"><span id="RPC_S_INVALID_NAF_ID"></span><span id="rpc_s_invalid_naf_id"></span>**RPC\_S\_INVALID\_NAF\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-293">1763 (0x6E3)</span><span class="sxs-lookup"><span data-stu-id="e8037-293">1763 (0x6E3)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-294">La famiglia di indirizzi di rete non è valida.</span><span class="sxs-lookup"><span data-stu-id="e8037-294">The network address family is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-295"><span id="RPC_S_CANNOT_SUPPORT"></span><span id="rpc_s_cannot_support"></span>**RPC \_ \_ non può \_ supportare**</span><span class="sxs-lookup"><span data-stu-id="e8037-295"><span id="RPC_S_CANNOT_SUPPORT"></span><span id="rpc_s_cannot_support"></span>**RPC\_S\_CANNOT\_SUPPORT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-296">1764 (0x6E4)</span><span class="sxs-lookup"><span data-stu-id="e8037-296">1764 (0x6E4)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-297">L'operazione richiesta non è supportata.</span><span class="sxs-lookup"><span data-stu-id="e8037-297">The requested operation is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-298"><span id="RPC_S_NO_CONTEXT_AVAILABLE"></span><span id="rpc_s_no_context_available"></span>**\_non è \_ \_ disponibile alcun \_ contesto per la RPC**</span><span class="sxs-lookup"><span data-stu-id="e8037-298"><span id="RPC_S_NO_CONTEXT_AVAILABLE"></span><span id="rpc_s_no_context_available"></span>**RPC\_S\_NO\_CONTEXT\_AVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-299">1765 (0x6E5)</span><span class="sxs-lookup"><span data-stu-id="e8037-299">1765 (0x6E5)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-300">Non è disponibile alcun contesto di sicurezza per consentire la rappresentazione.</span><span class="sxs-lookup"><span data-stu-id="e8037-300">No security context is available to allow impersonation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-301"><span id="RPC_S_INTERNAL_ERROR"></span><span id="rpc_s_internal_error"></span>**\_ \_ errore interno di \_ RPC**</span><span class="sxs-lookup"><span data-stu-id="e8037-301"><span id="RPC_S_INTERNAL_ERROR"></span><span id="rpc_s_internal_error"></span>**RPC\_S\_INTERNAL\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-302">1766 (0x6E6)</span><span class="sxs-lookup"><span data-stu-id="e8037-302">1766 (0x6E6)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-303">Si è verificato un errore interno in una chiamata di procedura remota (RPC).</span><span class="sxs-lookup"><span data-stu-id="e8037-303">An internal error occurred in a remote procedure call (RPC).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-304"><span id="RPC_S_ZERO_DIVIDE"></span><span id="rpc_s_zero_divide"></span>**\_ \_ divisione zero di \_ RPC**</span><span class="sxs-lookup"><span data-stu-id="e8037-304"><span id="RPC_S_ZERO_DIVIDE"></span><span id="rpc_s_zero_divide"></span>**RPC\_S\_ZERO\_DIVIDE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-305">1767 (0x6E7)</span><span class="sxs-lookup"><span data-stu-id="e8037-305">1767 (0x6E7)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-306">Il server RPC ha tentato una divisione di interi per zero.</span><span class="sxs-lookup"><span data-stu-id="e8037-306">The RPC server attempted an integer division by zero.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-307"><span id="RPC_S_ADDRESS_ERROR"></span><span id="rpc_s_address_error"></span>**\_errore di \_ indirizzo \_ RPC**</span><span class="sxs-lookup"><span data-stu-id="e8037-307"><span id="RPC_S_ADDRESS_ERROR"></span><span id="rpc_s_address_error"></span>**RPC\_S\_ADDRESS\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-308">1768 (0x6E8)</span><span class="sxs-lookup"><span data-stu-id="e8037-308">1768 (0x6E8)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-309">Si è verificato un errore di indirizzamento nel server RPC.</span><span class="sxs-lookup"><span data-stu-id="e8037-309">An addressing error occurred in the RPC server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-310"><span id="RPC_S_FP_DIV_ZERO"></span><span id="rpc_s_fp_div_zero"></span>**\_ \_ \_ zero div FP \_ di RPC**</span><span class="sxs-lookup"><span data-stu-id="e8037-310"><span id="RPC_S_FP_DIV_ZERO"></span><span id="rpc_s_fp_div_zero"></span>**RPC\_S\_FP\_DIV\_ZERO**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-311">1769 (0x6E9)</span><span class="sxs-lookup"><span data-stu-id="e8037-311">1769 (0x6E9)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-312">Un'operazione a virgola mobile nel server RPC ha causato una divisione per zero.</span><span class="sxs-lookup"><span data-stu-id="e8037-312">A floating-point operation at the RPC server caused a division by zero.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-313"><span id="RPC_S_FP_UNDERFLOW"></span><span id="rpc_s_fp_underflow"></span>**\_ \_ underflow FP di \_ RPC**</span><span class="sxs-lookup"><span data-stu-id="e8037-313"><span id="RPC_S_FP_UNDERFLOW"></span><span id="rpc_s_fp_underflow"></span>**RPC\_S\_FP\_UNDERFLOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-314">1770 (0x6EA)</span><span class="sxs-lookup"><span data-stu-id="e8037-314">1770 (0x6EA)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-315">Si è verificato un underflow a virgola mobile nel server RPC.</span><span class="sxs-lookup"><span data-stu-id="e8037-315">A floating-point underflow occurred at the RPC server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-316"><span id="RPC_S_FP_OVERFLOW"></span><span id="rpc_s_fp_overflow"></span>**\_ \_ overflow FP di \_ RPC**</span><span class="sxs-lookup"><span data-stu-id="e8037-316"><span id="RPC_S_FP_OVERFLOW"></span><span id="rpc_s_fp_overflow"></span>**RPC\_S\_FP\_OVERFLOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-317">1771 (0x6EB)</span><span class="sxs-lookup"><span data-stu-id="e8037-317">1771 (0x6EB)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-318">Si è verificato un overflow a virgola mobile nel server RPC.</span><span class="sxs-lookup"><span data-stu-id="e8037-318">A floating-point overflow occurred at the RPC server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-319"><span id="RPC_X_NO_MORE_ENTRIES"></span><span id="rpc_x_no_more_entries"></span>**RPC \_ X \_ \_ altre \_ voci**</span><span class="sxs-lookup"><span data-stu-id="e8037-319"><span id="RPC_X_NO_MORE_ENTRIES"></span><span id="rpc_x_no_more_entries"></span>**RPC\_X\_NO\_MORE\_ENTRIES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-320">1772 (0x6EC)</span><span class="sxs-lookup"><span data-stu-id="e8037-320">1772 (0x6EC)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-321">L'elenco dei server RPC disponibili per l'associazione di handle automatici è stato esaurito.</span><span class="sxs-lookup"><span data-stu-id="e8037-321">The list of RPC servers available for the binding of auto handles has been exhausted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-322"><span id="RPC_X_SS_CHAR_TRANS_OPEN_FAIL"></span><span id="rpc_x_ss_char_trans_open_fail"></span>**\_errore di \_ trasporto char X SS RPC \_ \_ \_ \_ non riuscito**</span><span class="sxs-lookup"><span data-stu-id="e8037-322"><span id="RPC_X_SS_CHAR_TRANS_OPEN_FAIL"></span><span id="rpc_x_ss_char_trans_open_fail"></span>**RPC\_X\_SS\_CHAR\_TRANS\_OPEN\_FAIL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-323">1773 (0x6ED)</span><span class="sxs-lookup"><span data-stu-id="e8037-323">1773 (0x6ED)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-324">Impossibile aprire il file della tabella di conversione dei caratteri.</span><span class="sxs-lookup"><span data-stu-id="e8037-324">Unable to open the character translation table file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-325"><span id="RPC_X_SS_CHAR_TRANS_SHORT_FILE"></span><span id="rpc_x_ss_char_trans_short_file"></span>**\_ \_ \_ \_ \_ file Short trans del carattere RPC X SS \_**</span><span class="sxs-lookup"><span data-stu-id="e8037-325"><span id="RPC_X_SS_CHAR_TRANS_SHORT_FILE"></span><span id="rpc_x_ss_char_trans_short_file"></span>**RPC\_X\_SS\_CHAR\_TRANS\_SHORT\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-326">1774 (0x6EE)</span><span class="sxs-lookup"><span data-stu-id="e8037-326">1774 (0x6EE)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-327">Il file contenente la tabella di conversione dei caratteri ha meno di 512 byte.</span><span class="sxs-lookup"><span data-stu-id="e8037-327">The file containing the character translation table has fewer than 512 bytes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-328"><span id="RPC_X_SS_IN_NULL_CONTEXT"></span><span id="rpc_x_ss_in_null_context"></span>**RPC \_ X \_ SS \_ nel \_ \_ contesto null**</span><span class="sxs-lookup"><span data-stu-id="e8037-328"><span id="RPC_X_SS_IN_NULL_CONTEXT"></span><span id="rpc_x_ss_in_null_context"></span>**RPC\_X\_SS\_IN\_NULL\_CONTEXT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-329">1775 (0x6EF)</span><span class="sxs-lookup"><span data-stu-id="e8037-329">1775 (0x6EF)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-330">Un handle di contesto null è stato passato dal client all'host durante una chiamata di procedura remota.</span><span class="sxs-lookup"><span data-stu-id="e8037-330">A null context handle was passed from the client to the host during a remote procedure call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-331"><span id="RPC_X_SS_CONTEXT_DAMAGED"></span><span id="rpc_x_ss_context_damaged"></span>**\_contesto RPC \_ X \_ SS \_ danneggiato**</span><span class="sxs-lookup"><span data-stu-id="e8037-331"><span id="RPC_X_SS_CONTEXT_DAMAGED"></span><span id="rpc_x_ss_context_damaged"></span>**RPC\_X\_SS\_CONTEXT\_DAMAGED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-332">1777 (0x6F1)</span><span class="sxs-lookup"><span data-stu-id="e8037-332">1777 (0x6F1)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-333">Handle di contesto modificato durante una chiamata di procedura remota.</span><span class="sxs-lookup"><span data-stu-id="e8037-333">The context handle changed during a remote procedure call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-334"><span id="RPC_X_SS_HANDLES_MISMATCH"></span><span id="rpc_x_ss_handles_mismatch"></span>**\_handle RPC X \_ SS non \_ \_ corrispondenti**</span><span class="sxs-lookup"><span data-stu-id="e8037-334"><span id="RPC_X_SS_HANDLES_MISMATCH"></span><span id="rpc_x_ss_handles_mismatch"></span>**RPC\_X\_SS\_HANDLES\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-335">1778 (0x6F2)</span><span class="sxs-lookup"><span data-stu-id="e8037-335">1778 (0x6F2)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-336">Gli handle di binding passati a una chiamata di procedura remota non corrispondono.</span><span class="sxs-lookup"><span data-stu-id="e8037-336">The binding handles passed to a remote procedure call do not match.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-337"><span id="RPC_X_SS_CANNOT_GET_CALL_HANDLE"></span><span id="rpc_x_ss_cannot_get_call_handle"></span>**RPC \_ X \_ SS \_ non può \_ ottenere un \_ handle di chiamata \_**</span><span class="sxs-lookup"><span data-stu-id="e8037-337"><span id="RPC_X_SS_CANNOT_GET_CALL_HANDLE"></span><span id="rpc_x_ss_cannot_get_call_handle"></span>**RPC\_X\_SS\_CANNOT\_GET\_CALL\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-338">1779 (0x6F3)</span><span class="sxs-lookup"><span data-stu-id="e8037-338">1779 (0x6F3)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-339">Lo stub non è in grado di ottenere l'handle di chiamata di procedura remota.</span><span class="sxs-lookup"><span data-stu-id="e8037-339">The stub is unable to get the remote procedure call handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-340"><span id="RPC_X_NULL_REF_POINTER"></span><span id="rpc_x_null_ref_pointer"></span>**\_puntatore di \_ \_ riferimento null RPC X \_**</span><span class="sxs-lookup"><span data-stu-id="e8037-340"><span id="RPC_X_NULL_REF_POINTER"></span><span id="rpc_x_null_ref_pointer"></span>**RPC\_X\_NULL\_REF\_POINTER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-341">1780 (0x6F4)</span><span class="sxs-lookup"><span data-stu-id="e8037-341">1780 (0x6F4)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-342">Un puntatore di riferimento null è stato passato allo stub.</span><span class="sxs-lookup"><span data-stu-id="e8037-342">A null reference pointer was passed to the stub.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-343"><span id="RPC_X_ENUM_VALUE_OUT_OF_RANGE"></span><span id="rpc_x_enum_value_out_of_range"></span>**\_valore enum X RPC non \_ compreso nell' \_ \_ \_ \_ intervallo**</span><span class="sxs-lookup"><span data-stu-id="e8037-343"><span id="RPC_X_ENUM_VALUE_OUT_OF_RANGE"></span><span id="rpc_x_enum_value_out_of_range"></span>**RPC\_X\_ENUM\_VALUE\_OUT\_OF\_RANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-344">1781 (0x6F5)</span><span class="sxs-lookup"><span data-stu-id="e8037-344">1781 (0x6F5)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-345">Il valore di enumerazione è esterno all'intervallo.</span><span class="sxs-lookup"><span data-stu-id="e8037-345">The enumeration value is out of range.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-346"><span id="RPC_X_BYTE_COUNT_TOO_SMALL"></span><span id="rpc_x_byte_count_too_small"></span>**\_numero di byte RPC X \_ \_ \_ troppo \_ piccolo**</span><span class="sxs-lookup"><span data-stu-id="e8037-346"><span id="RPC_X_BYTE_COUNT_TOO_SMALL"></span><span id="rpc_x_byte_count_too_small"></span>**RPC\_X\_BYTE\_COUNT\_TOO\_SMALL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-347">1782 (0x6F6)</span><span class="sxs-lookup"><span data-stu-id="e8037-347">1782 (0x6F6)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-348">Il numero di byte è troppo piccolo.</span><span class="sxs-lookup"><span data-stu-id="e8037-348">The byte count is too small.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-349"><span id="RPC_X_BAD_STUB_DATA"></span><span id="rpc_x_bad_stub_data"></span>**\_ \_ dati stub non validi RPC X \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e8037-349"><span id="RPC_X_BAD_STUB_DATA"></span><span id="rpc_x_bad_stub_data"></span>**RPC\_X\_BAD\_STUB\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-350">1783 (0x6F7)</span><span class="sxs-lookup"><span data-stu-id="e8037-350">1783 (0x6F7)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-351">Lo stub ha ricevuto dati non validi.</span><span class="sxs-lookup"><span data-stu-id="e8037-351">The stub received bad data.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-352"><span id="ERROR_INVALID_USER_BUFFER"></span><span id="error_invalid_user_buffer"></span>**ERRORE \_ \_ buffer utente non valido \_**</span><span class="sxs-lookup"><span data-stu-id="e8037-352"><span id="ERROR_INVALID_USER_BUFFER"></span><span id="error_invalid_user_buffer"></span>**ERROR\_INVALID\_USER\_BUFFER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-353">1784 (0x6F8)</span><span class="sxs-lookup"><span data-stu-id="e8037-353">1784 (0x6F8)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-354">Il buffer utente specificato non è valido per l'operazione richiesta.</span><span class="sxs-lookup"><span data-stu-id="e8037-354">The supplied user buffer is not valid for the requested operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-355"><span id="ERROR_UNRECOGNIZED_MEDIA"></span><span id="error_unrecognized_media"></span>**ERRORE \_ supporto non riconosciuto \_**</span><span class="sxs-lookup"><span data-stu-id="e8037-355"><span id="ERROR_UNRECOGNIZED_MEDIA"></span><span id="error_unrecognized_media"></span>**ERROR\_UNRECOGNIZED\_MEDIA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-356">1785 (0x6F9)</span><span class="sxs-lookup"><span data-stu-id="e8037-356">1785 (0x6F9)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-357">Il supporto disco non è stato riconosciuto.</span><span class="sxs-lookup"><span data-stu-id="e8037-357">The disk media is not recognized.</span></span> <span data-ttu-id="e8037-358">Potrebbe non essere formattato.</span><span class="sxs-lookup"><span data-stu-id="e8037-358">It may not be formatted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-359"><span id="ERROR_NO_TRUST_LSA_SECRET"></span><span id="error_no_trust_lsa_secret"></span>**ERRORE \_ nessun \_ \_ segreto LSA attendibile \_**</span><span class="sxs-lookup"><span data-stu-id="e8037-359"><span id="ERROR_NO_TRUST_LSA_SECRET"></span><span id="error_no_trust_lsa_secret"></span>**ERROR\_NO\_TRUST\_LSA\_SECRET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-360">1786 (0x6FA)</span><span class="sxs-lookup"><span data-stu-id="e8037-360">1786 (0x6FA)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-361">La workstation non dispone di un segreto di attendibilità.</span><span class="sxs-lookup"><span data-stu-id="e8037-361">The workstation does not have a trust secret.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-362"><span id="ERROR_NO_TRUST_SAM_ACCOUNT"></span><span id="error_no_trust_sam_account"></span>**ERRORE \_ nessun \_ \_ account SAM attendibile \_**</span><span class="sxs-lookup"><span data-stu-id="e8037-362"><span id="ERROR_NO_TRUST_SAM_ACCOUNT"></span><span id="error_no_trust_sam_account"></span>**ERROR\_NO\_TRUST\_SAM\_ACCOUNT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-363">1787 (0x6FB)</span><span class="sxs-lookup"><span data-stu-id="e8037-363">1787 (0x6FB)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-364">Il database di sicurezza nel server non dispone di un account computer per la relazione di trust tra workstation.</span><span class="sxs-lookup"><span data-stu-id="e8037-364">The security database on the server does not have a computer account for this workstation trust relationship.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-365"><span id="ERROR_TRUSTED_DOMAIN_FAILURE"></span><span id="error_trusted_domain_failure"></span>**ERRORE \_ dominio attendibile errore \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e8037-365"><span id="ERROR_TRUSTED_DOMAIN_FAILURE"></span><span id="error_trusted_domain_failure"></span>**ERROR\_TRUSTED\_DOMAIN\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-366">1788 (0x6FC)</span><span class="sxs-lookup"><span data-stu-id="e8037-366">1788 (0x6FC)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-367">La relazione di trust tra il dominio primario e il dominio trusted non è riuscita.</span><span class="sxs-lookup"><span data-stu-id="e8037-367">The trust relationship between the primary domain and the trusted domain failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-368"><span id="ERROR_TRUSTED_RELATIONSHIP_FAILURE"></span><span id="error_trusted_relationship_failure"></span>**ERRORE \_ relazione attendibile errore \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e8037-368"><span id="ERROR_TRUSTED_RELATIONSHIP_FAILURE"></span><span id="error_trusted_relationship_failure"></span>**ERROR\_TRUSTED\_RELATIONSHIP\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-369">1789 (0x6FD)</span><span class="sxs-lookup"><span data-stu-id="e8037-369">1789 (0x6FD)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-370">La relazione di trust tra questa workstation e il dominio primario non è riuscita.</span><span class="sxs-lookup"><span data-stu-id="e8037-370">The trust relationship between this workstation and the primary domain failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-371"><span id="ERROR_TRUST_FAILURE"></span><span id="error_trust_failure"></span>**ERRORE di \_ attendibilità \_**</span><span class="sxs-lookup"><span data-stu-id="e8037-371"><span id="ERROR_TRUST_FAILURE"></span><span id="error_trust_failure"></span>**ERROR\_TRUST\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-372">1790 (0x6FE)</span><span class="sxs-lookup"><span data-stu-id="e8037-372">1790 (0x6FE)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-373">Accesso alla rete non riuscito.</span><span class="sxs-lookup"><span data-stu-id="e8037-373">The network logon failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-374"><span id="RPC_S_CALL_IN_PROGRESS"></span><span id="rpc_s_call_in_progress"></span>**\_chiamata RPC \_ \_ in \_ corso**</span><span class="sxs-lookup"><span data-stu-id="e8037-374"><span id="RPC_S_CALL_IN_PROGRESS"></span><span id="rpc_s_call_in_progress"></span>**RPC\_S\_CALL\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-375">1791 (0x6FF)</span><span class="sxs-lookup"><span data-stu-id="e8037-375">1791 (0x6FF)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-376">È già in corso una chiamata di procedura remota per questo thread.</span><span class="sxs-lookup"><span data-stu-id="e8037-376">A remote procedure call is already in progress for this thread.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-377"><span id="ERROR_NETLOGON_NOT_STARTED"></span><span id="error_netlogon_not_started"></span>**ERRORE \_ Netlogon \_ non \_ avviato**</span><span class="sxs-lookup"><span data-stu-id="e8037-377"><span id="ERROR_NETLOGON_NOT_STARTED"></span><span id="error_netlogon_not_started"></span>**ERROR\_NETLOGON\_NOT\_STARTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-378">1792 (0x700)</span><span class="sxs-lookup"><span data-stu-id="e8037-378">1792 (0x700)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-379">È stato effettuato un tentativo di accesso, ma il servizio di accesso alla rete non è stato avviato.</span><span class="sxs-lookup"><span data-stu-id="e8037-379">An attempt was made to logon, but the network logon service was not started.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-380"><span id="ERROR_ACCOUNT_EXPIRED"></span><span id="error_account_expired"></span>**l'account di errore è \_ \_ scaduto**</span><span class="sxs-lookup"><span data-stu-id="e8037-380"><span id="ERROR_ACCOUNT_EXPIRED"></span><span id="error_account_expired"></span>**ERROR\_ACCOUNT\_EXPIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-381">1793 (0x701)</span><span class="sxs-lookup"><span data-stu-id="e8037-381">1793 (0x701)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-382">L'account dell'utente è scaduto.</span><span class="sxs-lookup"><span data-stu-id="e8037-382">The user's account has expired.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-383"><span id="ERROR_REDIRECTOR_HAS_OPEN_HANDLES"></span><span id="error_redirector_has_open_handles"></span>**il \_ REdirector di \_ errore \_ ha \_ handle aperti**</span><span class="sxs-lookup"><span data-stu-id="e8037-383"><span id="ERROR_REDIRECTOR_HAS_OPEN_HANDLES"></span><span id="error_redirector_has_open_handles"></span>**ERROR\_REDIRECTOR\_HAS\_OPEN\_HANDLES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-384">1794 (0x702)</span><span class="sxs-lookup"><span data-stu-id="e8037-384">1794 (0x702)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-385">Il redirector è in uso e non può essere scaricato.</span><span class="sxs-lookup"><span data-stu-id="e8037-385">The redirector is in use and cannot be unloaded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-386"><span id="ERROR_PRINTER_DRIVER_ALREADY_INSTALLED"></span><span id="error_printer_driver_already_installed"></span>**\_driver della stampante di errore \_ \_ già \_ installato**</span><span class="sxs-lookup"><span data-stu-id="e8037-386"><span id="ERROR_PRINTER_DRIVER_ALREADY_INSTALLED"></span><span id="error_printer_driver_already_installed"></span>**ERROR\_PRINTER\_DRIVER\_ALREADY\_INSTALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-387">1795 (0x703)</span><span class="sxs-lookup"><span data-stu-id="e8037-387">1795 (0x703)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-388">Il driver della stampante specificato è già installato.</span><span class="sxs-lookup"><span data-stu-id="e8037-388">The specified printer driver is already installed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-389"><span id="ERROR_UNKNOWN_PORT"></span><span id="error_unknown_port"></span>**ERRORE \_ \_ porta sconosciuta**</span><span class="sxs-lookup"><span data-stu-id="e8037-389"><span id="ERROR_UNKNOWN_PORT"></span><span id="error_unknown_port"></span>**ERROR\_UNKNOWN\_PORT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-390">1796 (0x704)</span><span class="sxs-lookup"><span data-stu-id="e8037-390">1796 (0x704)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-391">La porta specificata è sconosciuta.</span><span class="sxs-lookup"><span data-stu-id="e8037-391">The specified port is unknown.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-392"><span id="ERROR_UNKNOWN_PRINTER_DRIVER"></span><span id="error_unknown_printer_driver"></span>**ERRORE \_ \_ driver della stampante sconosciuto \_**</span><span class="sxs-lookup"><span data-stu-id="e8037-392"><span id="ERROR_UNKNOWN_PRINTER_DRIVER"></span><span id="error_unknown_printer_driver"></span>**ERROR\_UNKNOWN\_PRINTER\_DRIVER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-393">1797 (0x705)</span><span class="sxs-lookup"><span data-stu-id="e8037-393">1797 (0x705)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-394">Il driver della stampante è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="e8037-394">The printer driver is unknown.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-395"><span id="ERROR_UNKNOWN_PRINTPROCESSOR"></span><span id="error_unknown_printprocessor"></span>**ERRORE \_ sconosciuto \_ PRINTPROCESSOR**</span><span class="sxs-lookup"><span data-stu-id="e8037-395"><span id="ERROR_UNKNOWN_PRINTPROCESSOR"></span><span id="error_unknown_printprocessor"></span>**ERROR\_UNKNOWN\_PRINTPROCESSOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-396">1798 (0x706)</span><span class="sxs-lookup"><span data-stu-id="e8037-396">1798 (0x706)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-397">Il processore di stampa è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="e8037-397">The print processor is unknown.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-398"><span id="ERROR_INVALID_SEPARATOR_FILE"></span><span id="error_invalid_separator_file"></span>**ERRORE \_ \_ file separatore non valido \_**</span><span class="sxs-lookup"><span data-stu-id="e8037-398"><span id="ERROR_INVALID_SEPARATOR_FILE"></span><span id="error_invalid_separator_file"></span>**ERROR\_INVALID\_SEPARATOR\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-399">1799 (0x707)</span><span class="sxs-lookup"><span data-stu-id="e8037-399">1799 (0x707)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-400">Il file separatore specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="e8037-400">The specified separator file is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-401"><span id="ERROR_INVALID_PRIORITY"></span><span id="error_invalid_priority"></span>**ERRORE \_ priorità non valida \_**</span><span class="sxs-lookup"><span data-stu-id="e8037-401"><span id="ERROR_INVALID_PRIORITY"></span><span id="error_invalid_priority"></span>**ERROR\_INVALID\_PRIORITY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-402">1800 (0x708)</span><span class="sxs-lookup"><span data-stu-id="e8037-402">1800 (0x708)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-403">La priorità specificata non è valida.</span><span class="sxs-lookup"><span data-stu-id="e8037-403">The specified priority is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-404"><span id="ERROR_INVALID_PRINTER_NAME"></span><span id="error_invalid_printer_name"></span>**ERRORE \_ \_ nome stampante non valido \_**</span><span class="sxs-lookup"><span data-stu-id="e8037-404"><span id="ERROR_INVALID_PRINTER_NAME"></span><span id="error_invalid_printer_name"></span>**ERROR\_INVALID\_PRINTER\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-405">1801 (0x709)</span><span class="sxs-lookup"><span data-stu-id="e8037-405">1801 (0x709)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-406">Il nome della stampante non è valido.</span><span class="sxs-lookup"><span data-stu-id="e8037-406">The printer name is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-407"><span id="ERROR_PRINTER_ALREADY_EXISTS"></span><span id="error_printer_already_exists"></span>**la \_ stampante degli errori \_ \_ esiste già**</span><span class="sxs-lookup"><span data-stu-id="e8037-407"><span id="ERROR_PRINTER_ALREADY_EXISTS"></span><span id="error_printer_already_exists"></span>**ERROR\_PRINTER\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-408">1802 (0x70A)</span><span class="sxs-lookup"><span data-stu-id="e8037-408">1802 (0x70A)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-409">La stampante esiste già.</span><span class="sxs-lookup"><span data-stu-id="e8037-409">The printer already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-410"><span id="ERROR_INVALID_PRINTER_COMMAND"></span><span id="error_invalid_printer_command"></span>**ERRORE \_ \_ comando stampante non valido \_**</span><span class="sxs-lookup"><span data-stu-id="e8037-410"><span id="ERROR_INVALID_PRINTER_COMMAND"></span><span id="error_invalid_printer_command"></span>**ERROR\_INVALID\_PRINTER\_COMMAND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-411">1803 (0x70B)</span><span class="sxs-lookup"><span data-stu-id="e8037-411">1803 (0x70B)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-412">Il comando della stampante non è valido.</span><span class="sxs-lookup"><span data-stu-id="e8037-412">The printer command is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-413"><span id="ERROR_INVALID_DATATYPE"></span><span id="error_invalid_datatype"></span>**ERRORE di tipo di dati \_ non valido \_**</span><span class="sxs-lookup"><span data-stu-id="e8037-413"><span id="ERROR_INVALID_DATATYPE"></span><span id="error_invalid_datatype"></span>**ERROR\_INVALID\_DATATYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-414">1804 (0x70C)</span><span class="sxs-lookup"><span data-stu-id="e8037-414">1804 (0x70C)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-415">Il tipo di dati specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="e8037-415">The specified datatype is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-416"><span id="ERROR_INVALID_ENVIRONMENT"></span><span id="error_invalid_environment"></span>**ERRORE \_ di \_ ambiente non valido**</span><span class="sxs-lookup"><span data-stu-id="e8037-416"><span id="ERROR_INVALID_ENVIRONMENT"></span><span id="error_invalid_environment"></span>**ERROR\_INVALID\_ENVIRONMENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-417">1805 (0x70D)</span><span class="sxs-lookup"><span data-stu-id="e8037-417">1805 (0x70D)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-418">L'ambiente specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="e8037-418">The environment specified is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-419"><span id="RPC_S_NO_MORE_BINDINGS"></span><span id="rpc_s_no_more_bindings"></span>**\_ \_ nessun \_ binding RPC S \_**</span><span class="sxs-lookup"><span data-stu-id="e8037-419"><span id="RPC_S_NO_MORE_BINDINGS"></span><span id="rpc_s_no_more_bindings"></span>**RPC\_S\_NO\_MORE\_BINDINGS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-420">1806 (0x70E)</span><span class="sxs-lookup"><span data-stu-id="e8037-420">1806 (0x70E)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-421">Non sono presenti altre associazioni.</span><span class="sxs-lookup"><span data-stu-id="e8037-421">There are no more bindings.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-422"><span id="ERROR_NOLOGON_INTERDOMAIN_TRUST_ACCOUNT"></span><span id="error_nologon_interdomain_trust_account"></span>**ERRORE \_ NOlogon- \_ \_ account trust \_ tra domini**</span><span class="sxs-lookup"><span data-stu-id="e8037-422"><span id="ERROR_NOLOGON_INTERDOMAIN_TRUST_ACCOUNT"></span><span id="error_nologon_interdomain_trust_account"></span>**ERROR\_NOLOGON\_INTERDOMAIN\_TRUST\_ACCOUNT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-423">1807 (0x70F)</span><span class="sxs-lookup"><span data-stu-id="e8037-423">1807 (0x70F)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-424">L'account utilizzato è un account trust tra domini.</span><span class="sxs-lookup"><span data-stu-id="e8037-424">The account used is an interdomain trust account.</span></span> <span data-ttu-id="e8037-425">Per accedere a questo server, utilizzare l'account utente globale o l'account utente locale.</span><span class="sxs-lookup"><span data-stu-id="e8037-425">Use your global user account or local user account to access this server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-426"><span id="ERROR_NOLOGON_WORKSTATION_TRUST_ACCOUNT"></span><span id="error_nologon_workstation_trust_account"></span>**ERRORE \_ NOlogon \_ workstation \_ trust \_ account**</span><span class="sxs-lookup"><span data-stu-id="e8037-426"><span id="ERROR_NOLOGON_WORKSTATION_TRUST_ACCOUNT"></span><span id="error_nologon_workstation_trust_account"></span>**ERROR\_NOLOGON\_WORKSTATION\_TRUST\_ACCOUNT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-427">1808 (0x710)</span><span class="sxs-lookup"><span data-stu-id="e8037-427">1808 (0x710)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-428">L'account utilizzato è un account computer.</span><span class="sxs-lookup"><span data-stu-id="e8037-428">The account used is a computer account.</span></span> <span data-ttu-id="e8037-429">Per accedere a questo server, utilizzare l'account utente globale o l'account utente locale.</span><span class="sxs-lookup"><span data-stu-id="e8037-429">Use your global user account or local user account to access this server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-430"><span id="ERROR_NOLOGON_SERVER_TRUST_ACCOUNT"></span><span id="error_nologon_server_trust_account"></span>**ERRORE \_ nologo \_ server \_ trust \_ account**</span><span class="sxs-lookup"><span data-stu-id="e8037-430"><span id="ERROR_NOLOGON_SERVER_TRUST_ACCOUNT"></span><span id="error_nologon_server_trust_account"></span>**ERROR\_NOLOGON\_SERVER\_TRUST\_ACCOUNT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-431">1809 (0x711)</span><span class="sxs-lookup"><span data-stu-id="e8037-431">1809 (0x711)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-432">L'account utilizzato è un account di attendibilità del server.</span><span class="sxs-lookup"><span data-stu-id="e8037-432">The account used is a server trust account.</span></span> <span data-ttu-id="e8037-433">Per accedere a questo server, utilizzare l'account utente globale o l'account utente locale.</span><span class="sxs-lookup"><span data-stu-id="e8037-433">Use your global user account or local user account to access this server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-434"><span id="ERROR_DOMAIN_TRUST_INCONSISTENT"></span><span id="error_domain_trust_inconsistent"></span>**Trust del dominio di errore non \_ \_ \_ coerente**</span><span class="sxs-lookup"><span data-stu-id="e8037-434"><span id="ERROR_DOMAIN_TRUST_INCONSISTENT"></span><span id="error_domain_trust_inconsistent"></span>**ERROR\_DOMAIN\_TRUST\_INCONSISTENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-435">1810 (0x712)</span><span class="sxs-lookup"><span data-stu-id="e8037-435">1810 (0x712)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-436">Il nome o l'ID di sicurezza (SID) del dominio specificato non è coerente con le informazioni sull'attendibilità per tale dominio.</span><span class="sxs-lookup"><span data-stu-id="e8037-436">The name or security ID (SID) of the domain specified is inconsistent with the trust information for that domain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-437"><span id="ERROR_SERVER_HAS_OPEN_HANDLES"></span><span id="error_server_has_open_handles"></span>**ERRORE \_ del \_ server \_ con \_ handle aperti**</span><span class="sxs-lookup"><span data-stu-id="e8037-437"><span id="ERROR_SERVER_HAS_OPEN_HANDLES"></span><span id="error_server_has_open_handles"></span>**ERROR\_SERVER\_HAS\_OPEN\_HANDLES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-438">1811 (0x713)</span><span class="sxs-lookup"><span data-stu-id="e8037-438">1811 (0x713)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-439">Il server è in uso e non può essere scaricato.</span><span class="sxs-lookup"><span data-stu-id="e8037-439">The server is in use and cannot be unloaded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-440"><span id="ERROR_RESOURCE_DATA_NOT_FOUND"></span><span id="error_resource_data_not_found"></span>**dati della risorsa di errore \_ \_ \_ non \_ trovati**</span><span class="sxs-lookup"><span data-stu-id="e8037-440"><span id="ERROR_RESOURCE_DATA_NOT_FOUND"></span><span id="error_resource_data_not_found"></span>**ERROR\_RESOURCE\_DATA\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-441">1812 (0x714)</span><span class="sxs-lookup"><span data-stu-id="e8037-441">1812 (0x714)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-442">Il file di immagine specificato non contiene una sezione delle risorse.</span><span class="sxs-lookup"><span data-stu-id="e8037-442">The specified image file did not contain a resource section.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-443"><span id="ERROR_RESOURCE_TYPE_NOT_FOUND"></span><span id="error_resource_type_not_found"></span>**\_ \_ \_ Impossibile trovare il tipo di risorsa errore \_**</span><span class="sxs-lookup"><span data-stu-id="e8037-443"><span id="ERROR_RESOURCE_TYPE_NOT_FOUND"></span><span id="error_resource_type_not_found"></span>**ERROR\_RESOURCE\_TYPE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-444">1813 (0x715)</span><span class="sxs-lookup"><span data-stu-id="e8037-444">1813 (0x715)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-445">Il tipo di risorsa specificato non è stato trovato nel file di immagine.</span><span class="sxs-lookup"><span data-stu-id="e8037-445">The specified resource type cannot be found in the image file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-446"><span id="ERROR_RESOURCE_NAME_NOT_FOUND"></span><span id="error_resource_name_not_found"></span>**\_ \_ \_ Impossibile trovare il nome della risorsa di errore \_**</span><span class="sxs-lookup"><span data-stu-id="e8037-446"><span id="ERROR_RESOURCE_NAME_NOT_FOUND"></span><span id="error_resource_name_not_found"></span>**ERROR\_RESOURCE\_NAME\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-447">1814 (0x716)</span><span class="sxs-lookup"><span data-stu-id="e8037-447">1814 (0x716)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-448">Il nome di risorsa specificato non è stato trovato nel file di immagine.</span><span class="sxs-lookup"><span data-stu-id="e8037-448">The specified resource name cannot be found in the image file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-449"><span id="ERROR_RESOURCE_LANG_NOT_FOUND"></span><span id="error_resource_lang_not_found"></span>**\_ \_ \_ Impossibile trovare la risorsa di errore lang \_**</span><span class="sxs-lookup"><span data-stu-id="e8037-449"><span id="ERROR_RESOURCE_LANG_NOT_FOUND"></span><span id="error_resource_lang_not_found"></span>**ERROR\_RESOURCE\_LANG\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-450">1815 (0x717)</span><span class="sxs-lookup"><span data-stu-id="e8037-450">1815 (0x717)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-451">Impossibile trovare l'ID lingua della risorsa specificato nel file di immagine.</span><span class="sxs-lookup"><span data-stu-id="e8037-451">The specified resource language ID cannot be found in the image file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-452"><span id="ERROR_NOT_ENOUGH_QUOTA"></span><span id="error_not_enough_quota"></span>**ERRORE \_ di \_ quota insufficiente \_**</span><span class="sxs-lookup"><span data-stu-id="e8037-452"><span id="ERROR_NOT_ENOUGH_QUOTA"></span><span id="error_not_enough_quota"></span>**ERROR\_NOT\_ENOUGH\_QUOTA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-453">1816 (0x718)</span><span class="sxs-lookup"><span data-stu-id="e8037-453">1816 (0x718)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-454">Non c'è abbastanza disponibilità di quota per elaborare il comando.</span><span class="sxs-lookup"><span data-stu-id="e8037-454">Not enough quota is available to process this command.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-455"><span id="RPC_S_NO_INTERFACES"></span><span id="rpc_s_no_interfaces"></span>**\_non ci \_ sono \_ interfacce di RPC**</span><span class="sxs-lookup"><span data-stu-id="e8037-455"><span id="RPC_S_NO_INTERFACES"></span><span id="rpc_s_no_interfaces"></span>**RPC\_S\_NO\_INTERFACES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-456">1817 (0x719)</span><span class="sxs-lookup"><span data-stu-id="e8037-456">1817 (0x719)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-457">Nessuna interfaccia registrata.</span><span class="sxs-lookup"><span data-stu-id="e8037-457">No interfaces have been registered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-458"><span id="RPC_S_CALL_CANCELLED"></span><span id="rpc_s_call_cancelled"></span>**\_chiamata RPC \_ \_ annullata**</span><span class="sxs-lookup"><span data-stu-id="e8037-458"><span id="RPC_S_CALL_CANCELLED"></span><span id="rpc_s_call_cancelled"></span>**RPC\_S\_CALL\_CANCELLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-459">1818 (0x71A)</span><span class="sxs-lookup"><span data-stu-id="e8037-459">1818 (0x71A)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-460">La chiamata di procedura remota è stata annullata.</span><span class="sxs-lookup"><span data-stu-id="e8037-460">The remote procedure call was cancelled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-461"><span id="RPC_S_BINDING_INCOMPLETE"></span><span id="rpc_s_binding_incomplete"></span>**\_binding RPC \_ \_ incompleto**</span><span class="sxs-lookup"><span data-stu-id="e8037-461"><span id="RPC_S_BINDING_INCOMPLETE"></span><span id="rpc_s_binding_incomplete"></span>**RPC\_S\_BINDING\_INCOMPLETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-462">1819 (0x71B)</span><span class="sxs-lookup"><span data-stu-id="e8037-462">1819 (0x71B)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-463">L'handle di associazione non contiene tutte le informazioni necessarie.</span><span class="sxs-lookup"><span data-stu-id="e8037-463">The binding handle does not contain all required information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-464"><span id="RPC_S_COMM_FAILURE"></span><span id="rpc_s_comm_failure"></span>**\_errore di \_ comunicazione RPC S \_**</span><span class="sxs-lookup"><span data-stu-id="e8037-464"><span id="RPC_S_COMM_FAILURE"></span><span id="rpc_s_comm_failure"></span>**RPC\_S\_COMM\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-465">1820 (0x71C)</span><span class="sxs-lookup"><span data-stu-id="e8037-465">1820 (0x71C)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-466">Si è verificato un errore di comunicazione durante una chiamata di procedura remota.</span><span class="sxs-lookup"><span data-stu-id="e8037-466">A communications failure occurred during a remote procedure call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-467"><span id="RPC_S_UNSUPPORTED_AUTHN_LEVEL"></span><span id="rpc_s_unsupported_authn_level"></span>**il \_ livello di autenticazione non è \_ supportato in \_ RPC \_**</span><span class="sxs-lookup"><span data-stu-id="e8037-467"><span id="RPC_S_UNSUPPORTED_AUTHN_LEVEL"></span><span id="rpc_s_unsupported_authn_level"></span>**RPC\_S\_UNSUPPORTED\_AUTHN\_LEVEL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-468">1821 (0x71D)</span><span class="sxs-lookup"><span data-stu-id="e8037-468">1821 (0x71D)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-469">Il livello di autenticazione richiesto non è supportato.</span><span class="sxs-lookup"><span data-stu-id="e8037-469">The requested authentication level is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-470"><span id="RPC_S_NO_PRINC_NAME"></span><span id="rpc_s_no_princ_name"></span>**\_ \_ \_ nome princ non presente \_ in RPC**</span><span class="sxs-lookup"><span data-stu-id="e8037-470"><span id="RPC_S_NO_PRINC_NAME"></span><span id="rpc_s_no_princ_name"></span>**RPC\_S\_NO\_PRINC\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-471">1822 (0x71E)</span><span class="sxs-lookup"><span data-stu-id="e8037-471">1822 (0x71E)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-472">Nessun nome entità registrato.</span><span class="sxs-lookup"><span data-stu-id="e8037-472">No principal name registered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-473"><span id="RPC_S_NOT_RPC_ERROR"></span><span id="rpc_s_not_rpc_error"></span>**\_errore RPC S \_ Not \_ RPC \_**</span><span class="sxs-lookup"><span data-stu-id="e8037-473"><span id="RPC_S_NOT_RPC_ERROR"></span><span id="rpc_s_not_rpc_error"></span>**RPC\_S\_NOT\_RPC\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-474">1823 (0x71F)</span><span class="sxs-lookup"><span data-stu-id="e8037-474">1823 (0x71F)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-475">L'errore specificato non è un codice di errore RPC di Windows valido.</span><span class="sxs-lookup"><span data-stu-id="e8037-475">The error specified is not a valid Windows RPC error code.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-476"><span id="RPC_S_UUID_LOCAL_ONLY"></span><span id="rpc_s_uuid_local_only"></span>**\_ \_ \_ solo locale UUID \_ di RPC**</span><span class="sxs-lookup"><span data-stu-id="e8037-476"><span id="RPC_S_UUID_LOCAL_ONLY"></span><span id="rpc_s_uuid_local_only"></span>**RPC\_S\_UUID\_LOCAL\_ONLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-477">1824 (0x720)</span><span class="sxs-lookup"><span data-stu-id="e8037-477">1824 (0x720)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-478">È stato allocato un UUID valido solo in questo computer.</span><span class="sxs-lookup"><span data-stu-id="e8037-478">A UUID that is valid only on this computer has been allocated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-479"><span id="RPC_S_SEC_PKG_ERROR"></span><span id="rpc_s_sec_pkg_error"></span>**errore pkg di RPC \_ s \_ sec \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e8037-479"><span id="RPC_S_SEC_PKG_ERROR"></span><span id="rpc_s_sec_pkg_error"></span>**RPC\_S\_SEC\_PKG\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-480">1825 (0x721)</span><span class="sxs-lookup"><span data-stu-id="e8037-480">1825 (0x721)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-481">Si è verificato un errore specifico del pacchetto di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="e8037-481">A security package specific error occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-482"><span id="RPC_S_NOT_CANCELLED"></span><span id="rpc_s_not_cancelled"></span>**RPC \_ \_ non \_ annullata**</span><span class="sxs-lookup"><span data-stu-id="e8037-482"><span id="RPC_S_NOT_CANCELLED"></span><span id="rpc_s_not_cancelled"></span>**RPC\_S\_NOT\_CANCELLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-483">1826 (0x722)</span><span class="sxs-lookup"><span data-stu-id="e8037-483">1826 (0x722)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-484">Il thread non è stato annullato.</span><span class="sxs-lookup"><span data-stu-id="e8037-484">Thread is not canceled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-485"><span id="RPC_X_INVALID_ES_ACTION"></span><span id="rpc_x_invalid_es_action"></span>**\_ \_ azione es non valida RPC X \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e8037-485"><span id="RPC_X_INVALID_ES_ACTION"></span><span id="rpc_x_invalid_es_action"></span>**RPC\_X\_INVALID\_ES\_ACTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-486">1827 (0x723)</span><span class="sxs-lookup"><span data-stu-id="e8037-486">1827 (0x723)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-487">Operazione non valida sull'handle di codifica/decodifica.</span><span class="sxs-lookup"><span data-stu-id="e8037-487">Invalid operation on the encoding/decoding handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-488"><span id="RPC_X_WRONG_ES_VERSION"></span><span id="rpc_x_wrong_es_version"></span>**RPC \_ X \_ errata \_ \_ versione es**</span><span class="sxs-lookup"><span data-stu-id="e8037-488"><span id="RPC_X_WRONG_ES_VERSION"></span><span id="rpc_x_wrong_es_version"></span>**RPC\_X\_WRONG\_ES\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-489">1828 (0x724)</span><span class="sxs-lookup"><span data-stu-id="e8037-489">1828 (0x724)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-490">Versione non compatibile del pacchetto di serializzazione.</span><span class="sxs-lookup"><span data-stu-id="e8037-490">Incompatible version of the serializing package.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-491"><span id="RPC_X_WRONG_STUB_VERSION"></span><span id="rpc_x_wrong_stub_version"></span>**RPC \_ X \_ \_ versione stub errata \_**</span><span class="sxs-lookup"><span data-stu-id="e8037-491"><span id="RPC_X_WRONG_STUB_VERSION"></span><span id="rpc_x_wrong_stub_version"></span>**RPC\_X\_WRONG\_STUB\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-492">1829 (0x725)</span><span class="sxs-lookup"><span data-stu-id="e8037-492">1829 (0x725)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-493">Versione non compatibile dello stub RPC.</span><span class="sxs-lookup"><span data-stu-id="e8037-493">Incompatible version of the RPC stub.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-494"><span id="RPC_X_INVALID_PIPE_OBJECT"></span><span id="rpc_x_invalid_pipe_object"></span>**RPC \_ X \_ \_ oggetto pipe non valido \_**</span><span class="sxs-lookup"><span data-stu-id="e8037-494"><span id="RPC_X_INVALID_PIPE_OBJECT"></span><span id="rpc_x_invalid_pipe_object"></span>**RPC\_X\_INVALID\_PIPE\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-495">1830 (0x726)</span><span class="sxs-lookup"><span data-stu-id="e8037-495">1830 (0x726)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-496">L'oggetto pipe RPC non è valido o è danneggiato.</span><span class="sxs-lookup"><span data-stu-id="e8037-496">The RPC pipe object is invalid or corrupted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-497"><span id="RPC_X_WRONG_PIPE_ORDER"></span><span id="rpc_x_wrong_pipe_order"></span>**\_ordine di \_ pipe non corretto RPC X \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e8037-497"><span id="RPC_X_WRONG_PIPE_ORDER"></span><span id="rpc_x_wrong_pipe_order"></span>**RPC\_X\_WRONG\_PIPE\_ORDER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-498">1831 (0x727)</span><span class="sxs-lookup"><span data-stu-id="e8037-498">1831 (0x727)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-499">Si è tentato di eseguire un'operazione non valida su un oggetto pipe RPC.</span><span class="sxs-lookup"><span data-stu-id="e8037-499">An invalid operation was attempted on an RPC pipe object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-500"><span id="RPC_X_WRONG_PIPE_VERSION"></span><span id="rpc_x_wrong_pipe_version"></span>**\_ \_ versione pipe non corretta RPC X \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e8037-500"><span id="RPC_X_WRONG_PIPE_VERSION"></span><span id="rpc_x_wrong_pipe_version"></span>**RPC\_X\_WRONG\_PIPE\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-501">1832 (0x728)</span><span class="sxs-lookup"><span data-stu-id="e8037-501">1832 (0x728)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-502">Versione pipe RPC non supportata.</span><span class="sxs-lookup"><span data-stu-id="e8037-502">Unsupported RPC pipe version.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-503"><span id="RPC_S_COOKIE_AUTH_FAILED"></span><span id="rpc_s_cookie_auth_failed"></span>**\_ \_ autenticazione cookie di \_ RPC \_ non riuscita**</span><span class="sxs-lookup"><span data-stu-id="e8037-503"><span id="RPC_S_COOKIE_AUTH_FAILED"></span><span id="rpc_s_cookie_auth_failed"></span>**RPC\_S\_COOKIE\_AUTH\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-504">1833 (0x729)</span><span class="sxs-lookup"><span data-stu-id="e8037-504">1833 (0x729)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-505">Il server proxy HTTP ha rifiutato la connessione perché l'autenticazione del cookie non è riuscita.</span><span class="sxs-lookup"><span data-stu-id="e8037-505">HTTP proxy server rejected the connection because the cookie authentication failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-506"><span id="RPC_S_GROUP_MEMBER_NOT_FOUND"></span><span id="rpc_s_group_member_not_found"></span>**il \_ \_ membro del gruppo RPC non è \_ stato \_ \_ trovato**</span><span class="sxs-lookup"><span data-stu-id="e8037-506"><span id="RPC_S_GROUP_MEMBER_NOT_FOUND"></span><span id="rpc_s_group_member_not_found"></span>**RPC\_S\_GROUP\_MEMBER\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-507">1898 (0x76A)</span><span class="sxs-lookup"><span data-stu-id="e8037-507">1898 (0x76A)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-508">Impossibile trovare il membro del gruppo.</span><span class="sxs-lookup"><span data-stu-id="e8037-508">The group member was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-509"><span id="EPT_S_CANT_CREATE"></span><span id="ept_s_cant_create"></span>**\_ \_ creazione cant di \_ EPT**</span><span class="sxs-lookup"><span data-stu-id="e8037-509"><span id="EPT_S_CANT_CREATE"></span><span id="ept_s_cant_create"></span>**EPT\_S\_CANT\_CREATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-510">1899 (0x76B)</span><span class="sxs-lookup"><span data-stu-id="e8037-510">1899 (0x76B)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-511">Non è stato possibile creare la voce del database di mapping degli endpoint.</span><span class="sxs-lookup"><span data-stu-id="e8037-511">The endpoint mapper database entry could not be created.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-512"><span id="RPC_S_INVALID_OBJECT"></span><span id="rpc_s_invalid_object"></span>**\_oggetto RPC \_ non valido \_**</span><span class="sxs-lookup"><span data-stu-id="e8037-512"><span id="RPC_S_INVALID_OBJECT"></span><span id="rpc_s_invalid_object"></span>**RPC\_S\_INVALID\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-513">1900 (0x76C)</span><span class="sxs-lookup"><span data-stu-id="e8037-513">1900 (0x76C)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-514">L'identificatore univoco universale (UUID) dell'oggetto è l'UUID Nil.</span><span class="sxs-lookup"><span data-stu-id="e8037-514">The object universal unique identifier (UUID) is the nil UUID.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-515"><span id="ERROR_INVALID_TIME"></span><span id="error_invalid_time"></span>**ERRORE \_ ora non valido \_**</span><span class="sxs-lookup"><span data-stu-id="e8037-515"><span id="ERROR_INVALID_TIME"></span><span id="error_invalid_time"></span>**ERROR\_INVALID\_TIME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-516">1901 (0x76D)</span><span class="sxs-lookup"><span data-stu-id="e8037-516">1901 (0x76D)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-517">L'ora specificata non è valida.</span><span class="sxs-lookup"><span data-stu-id="e8037-517">The specified time is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-518"><span id="ERROR_INVALID_FORM_NAME"></span><span id="error_invalid_form_name"></span>**ERRORE \_ \_ nome modulo non valido \_**</span><span class="sxs-lookup"><span data-stu-id="e8037-518"><span id="ERROR_INVALID_FORM_NAME"></span><span id="error_invalid_form_name"></span>**ERROR\_INVALID\_FORM\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-519">1902 (0x76E)</span><span class="sxs-lookup"><span data-stu-id="e8037-519">1902 (0x76E)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-520">Il nome del modulo specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="e8037-520">The specified form name is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-521"><span id="ERROR_INVALID_FORM_SIZE"></span><span id="error_invalid_form_size"></span>**ERRORE \_ dimensione formato non valido \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e8037-521"><span id="ERROR_INVALID_FORM_SIZE"></span><span id="error_invalid_form_size"></span>**ERROR\_INVALID\_FORM\_SIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-522">1903 (0x76F)</span><span class="sxs-lookup"><span data-stu-id="e8037-522">1903 (0x76F)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-523">Dimensioni del form specificate non valide.</span><span class="sxs-lookup"><span data-stu-id="e8037-523">The specified form size is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-524"><span id="ERROR_ALREADY_WAITING"></span><span id="error_already_waiting"></span>**ERRORE \_ già \_ in attesa**</span><span class="sxs-lookup"><span data-stu-id="e8037-524"><span id="ERROR_ALREADY_WAITING"></span><span id="error_already_waiting"></span>**ERROR\_ALREADY\_WAITING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-525">1904 (0x770)</span><span class="sxs-lookup"><span data-stu-id="e8037-525">1904 (0x770)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-526">L'handle della stampante specificato è già in attesa.</span><span class="sxs-lookup"><span data-stu-id="e8037-526">The specified printer handle is already being waited on.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-527"><span id="ERROR_PRINTER_DELETED"></span><span id="error_printer_deleted"></span>**stampante di errore \_ \_ eliminata**</span><span class="sxs-lookup"><span data-stu-id="e8037-527"><span id="ERROR_PRINTER_DELETED"></span><span id="error_printer_deleted"></span>**ERROR\_PRINTER\_DELETED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-528">1905 (0x771)</span><span class="sxs-lookup"><span data-stu-id="e8037-528">1905 (0x771)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-529">La stampante specificata è stata eliminata.</span><span class="sxs-lookup"><span data-stu-id="e8037-529">The specified printer has been deleted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-530"><span id="ERROR_INVALID_PRINTER_STATE"></span><span id="error_invalid_printer_state"></span>**ERRORE \_ di \_ stato della stampante non valido \_**</span><span class="sxs-lookup"><span data-stu-id="e8037-530"><span id="ERROR_INVALID_PRINTER_STATE"></span><span id="error_invalid_printer_state"></span>**ERROR\_INVALID\_PRINTER\_STATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-531">1906 (0x772)</span><span class="sxs-lookup"><span data-stu-id="e8037-531">1906 (0x772)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-532">Lo stato della stampante non è valido.</span><span class="sxs-lookup"><span data-stu-id="e8037-532">The state of the printer is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-533"><span id="ERROR_PASSWORD_MUST_CHANGE"></span><span id="error_password_must_change"></span>**è \_ \_ necessario \_ modificare la password di errore**</span><span class="sxs-lookup"><span data-stu-id="e8037-533"><span id="ERROR_PASSWORD_MUST_CHANGE"></span><span id="error_password_must_change"></span>**ERROR\_PASSWORD\_MUST\_CHANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-534">1907 (0x773)</span><span class="sxs-lookup"><span data-stu-id="e8037-534">1907 (0x773)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-535">È necessario modificare la password dell'utente prima dell'accesso.</span><span class="sxs-lookup"><span data-stu-id="e8037-535">The user's password must be changed before signing in.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-536"><span id="ERROR_DOMAIN_CONTROLLER_NOT_FOUND"></span><span id="error_domain_controller_not_found"></span>**\_ \_ \_ Impossibile trovare il controller di dominio di errore \_**</span><span class="sxs-lookup"><span data-stu-id="e8037-536"><span id="ERROR_DOMAIN_CONTROLLER_NOT_FOUND"></span><span id="error_domain_controller_not_found"></span>**ERROR\_DOMAIN\_CONTROLLER\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-537">1908 (0x774)</span><span class="sxs-lookup"><span data-stu-id="e8037-537">1908 (0x774)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-538">Non è stato possibile trovare il controller di dominio per questo dominio.</span><span class="sxs-lookup"><span data-stu-id="e8037-538">Could not find the domain controller for this domain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-539"><span id="ERROR_ACCOUNT_LOCKED_OUT"></span><span id="error_account_locked_out"></span>**\_account errore \_ bloccato \_**</span><span class="sxs-lookup"><span data-stu-id="e8037-539"><span id="ERROR_ACCOUNT_LOCKED_OUT"></span><span id="error_account_locked_out"></span>**ERROR\_ACCOUNT\_LOCKED\_OUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-540">1909 (0x775)</span><span class="sxs-lookup"><span data-stu-id="e8037-540">1909 (0x775)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-541">L'account a cui si fa riferimento è attualmente bloccato e potrebbe non essere connesso a.</span><span class="sxs-lookup"><span data-stu-id="e8037-541">The referenced account is currently locked out and may not be logged on to.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-542"><span id="OR_INVALID_OXID"></span><span id="or_invalid_oxid"></span>**o \_ Oxid non valido \_**</span><span class="sxs-lookup"><span data-stu-id="e8037-542"><span id="OR_INVALID_OXID"></span><span id="or_invalid_oxid"></span>**OR\_INVALID\_OXID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-543">1910 (0x776)</span><span class="sxs-lookup"><span data-stu-id="e8037-543">1910 (0x776)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-544">Impossibile trovare l'utilità di esportazione oggetti specificata.</span><span class="sxs-lookup"><span data-stu-id="e8037-544">The object exporter specified was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-545"><span id="OR_INVALID_OID"></span><span id="or_invalid_oid"></span>**o \_ OID non valido \_**</span><span class="sxs-lookup"><span data-stu-id="e8037-545"><span id="OR_INVALID_OID"></span><span id="or_invalid_oid"></span>**OR\_INVALID\_OID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-546">1911 (0x777)</span><span class="sxs-lookup"><span data-stu-id="e8037-546">1911 (0x777)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-547">Impossibile trovare l'oggetto specificato.</span><span class="sxs-lookup"><span data-stu-id="e8037-547">The object specified was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-548"><span id="OR_INVALID_SET"></span><span id="or_invalid_set"></span>**o \_ set non valido \_**</span><span class="sxs-lookup"><span data-stu-id="e8037-548"><span id="OR_INVALID_SET"></span><span id="or_invalid_set"></span>**OR\_INVALID\_SET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-549">1912 (0x778)</span><span class="sxs-lookup"><span data-stu-id="e8037-549">1912 (0x778)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-550">Il set di resolver di oggetti specificato non è stato trovato.</span><span class="sxs-lookup"><span data-stu-id="e8037-550">The object resolver set specified was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-551"><span id="RPC_S_SEND_INCOMPLETE"></span><span id="rpc_s_send_incomplete"></span>**\_invio di \_ RPC \_ incompleto**</span><span class="sxs-lookup"><span data-stu-id="e8037-551"><span id="RPC_S_SEND_INCOMPLETE"></span><span id="rpc_s_send_incomplete"></span>**RPC\_S\_SEND\_INCOMPLETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-552">1913 (0x779)</span><span class="sxs-lookup"><span data-stu-id="e8037-552">1913 (0x779)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-553">Alcuni dati restano da inviare nel buffer della richiesta.</span><span class="sxs-lookup"><span data-stu-id="e8037-553">Some data remains to be sent in the request buffer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-554"><span id="RPC_S_INVALID_ASYNC_HANDLE"></span><span id="rpc_s_invalid_async_handle"></span>**\_ \_ \_ handle asincrono non valido \_ RPC**</span><span class="sxs-lookup"><span data-stu-id="e8037-554"><span id="RPC_S_INVALID_ASYNC_HANDLE"></span><span id="rpc_s_invalid_async_handle"></span>**RPC\_S\_INVALID\_ASYNC\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-555">1914 (0x77A)</span><span class="sxs-lookup"><span data-stu-id="e8037-555">1914 (0x77A)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-556">Handle di chiamata di procedura remota asincrona non valido.</span><span class="sxs-lookup"><span data-stu-id="e8037-556">Invalid asynchronous remote procedure call handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-557"><span id="RPC_S_INVALID_ASYNC_CALL"></span><span id="rpc_s_invalid_async_call"></span>**\_ \_ \_ chiamata asincrona non valida \_ in RPC**</span><span class="sxs-lookup"><span data-stu-id="e8037-557"><span id="RPC_S_INVALID_ASYNC_CALL"></span><span id="rpc_s_invalid_async_call"></span>**RPC\_S\_INVALID\_ASYNC\_CALL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-558">1915 (0x77B)</span><span class="sxs-lookup"><span data-stu-id="e8037-558">1915 (0x77B)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-559">Handle di chiamata RPC asincrono non valido per questa operazione.</span><span class="sxs-lookup"><span data-stu-id="e8037-559">Invalid asynchronous RPC call handle for this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-560"><span id="RPC_X_PIPE_CLOSED"></span><span id="rpc_x_pipe_closed"></span>**\_pipe RPC \_ X \_ chiusa**</span><span class="sxs-lookup"><span data-stu-id="e8037-560"><span id="RPC_X_PIPE_CLOSED"></span><span id="rpc_x_pipe_closed"></span>**RPC\_X\_PIPE\_CLOSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-561">1916 (0x77C)</span><span class="sxs-lookup"><span data-stu-id="e8037-561">1916 (0x77C)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-562">L'oggetto pipe RPC è già stato chiuso.</span><span class="sxs-lookup"><span data-stu-id="e8037-562">The RPC pipe object has already been closed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-563"><span id="RPC_X_PIPE_DISCIPLINE_ERROR"></span><span id="rpc_x_pipe_discipline_error"></span>**\_errore di \_ disciplina della pipe RPC X \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e8037-563"><span id="RPC_X_PIPE_DISCIPLINE_ERROR"></span><span id="rpc_x_pipe_discipline_error"></span>**RPC\_X\_PIPE\_DISCIPLINE\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-564">1917 (0x77D)</span><span class="sxs-lookup"><span data-stu-id="e8037-564">1917 (0x77D)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-565">La chiamata RPC è stata completata prima dell'elaborazione di tutte le pipe.</span><span class="sxs-lookup"><span data-stu-id="e8037-565">The RPC call completed before all pipes were processed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-566"><span id="RPC_X_PIPE_EMPTY"></span><span id="rpc_x_pipe_empty"></span>**\_pipe RPC \_ X \_ vuota**</span><span class="sxs-lookup"><span data-stu-id="e8037-566"><span id="RPC_X_PIPE_EMPTY"></span><span id="rpc_x_pipe_empty"></span>**RPC\_X\_PIPE\_EMPTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-567">1918 (0x77E)</span><span class="sxs-lookup"><span data-stu-id="e8037-567">1918 (0x77E)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-568">Dalla pipe RPC non sono disponibili altri dati.</span><span class="sxs-lookup"><span data-stu-id="e8037-568">No more data is available from the RPC pipe.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-569"><span id="ERROR_NO_SITENAME"></span><span id="error_no_sitename"></span>**ERRORE \_ nessun \_ siteName**</span><span class="sxs-lookup"><span data-stu-id="e8037-569"><span id="ERROR_NO_SITENAME"></span><span id="error_no_sitename"></span>**ERROR\_NO\_SITENAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-570">1919 (0x77F)</span><span class="sxs-lookup"><span data-stu-id="e8037-570">1919 (0x77F)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-571">Nessun nome di sito disponibile per questo computer.</span><span class="sxs-lookup"><span data-stu-id="e8037-571">No site name is available for this machine.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-572"><span id="ERROR_CANT_ACCESS_FILE"></span><span id="error_cant_access_file"></span>**ERRORE \_ di \_ accesso al \_ file**</span><span class="sxs-lookup"><span data-stu-id="e8037-572"><span id="ERROR_CANT_ACCESS_FILE"></span><span id="error_cant_access_file"></span>**ERROR\_CANT\_ACCESS\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-573">1920 (0x780)</span><span class="sxs-lookup"><span data-stu-id="e8037-573">1920 (0x780)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-574">Non è possibile accedere al file dal sistema.</span><span class="sxs-lookup"><span data-stu-id="e8037-574">The file cannot be accessed by the system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-575"><span id="ERROR_CANT_RESOLVE_FILENAME"></span><span id="error_cant_resolve_filename"></span>**errore durante la \_ \_ risoluzione del \_ nome file**</span><span class="sxs-lookup"><span data-stu-id="e8037-575"><span id="ERROR_CANT_RESOLVE_FILENAME"></span><span id="error_cant_resolve_filename"></span>**ERROR\_CANT\_RESOLVE\_FILENAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-576">1921 (0x781)</span><span class="sxs-lookup"><span data-stu-id="e8037-576">1921 (0x781)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-577">Il nome del file non può essere risolto dal sistema.</span><span class="sxs-lookup"><span data-stu-id="e8037-577">The name of the file cannot be resolved by the system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-578"><span id="RPC_S_ENTRY_TYPE_MISMATCH"></span><span id="rpc_s_entry_type_mismatch"></span>**tipo di voce RPC non \_ \_ \_ \_ corrispondente**</span><span class="sxs-lookup"><span data-stu-id="e8037-578"><span id="RPC_S_ENTRY_TYPE_MISMATCH"></span><span id="rpc_s_entry_type_mismatch"></span>**RPC\_S\_ENTRY\_TYPE\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-579">1922 (0x782)</span><span class="sxs-lookup"><span data-stu-id="e8037-579">1922 (0x782)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-580">La voce non è del tipo previsto.</span><span class="sxs-lookup"><span data-stu-id="e8037-580">The entry is not of the expected type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-581"><span id="RPC_S_NOT_ALL_OBJS_EXPORTED"></span><span id="rpc_s_not_all_objs_exported"></span>**RPC \_ \_ non \_ tutti i \_ obj \_ esportati**</span><span class="sxs-lookup"><span data-stu-id="e8037-581"><span id="RPC_S_NOT_ALL_OBJS_EXPORTED"></span><span id="rpc_s_not_all_objs_exported"></span>**RPC\_S\_NOT\_ALL\_OBJS\_EXPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-582">1923 (0x783)</span><span class="sxs-lookup"><span data-stu-id="e8037-582">1923 (0x783)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-583">Non tutti gli UUID degli oggetti possono essere esportati nella voce specificata.</span><span class="sxs-lookup"><span data-stu-id="e8037-583">Not all object UUIDs could be exported to the specified entry.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-584"><span id="RPC_S_INTERFACE_NOT_EXPORTED"></span><span id="rpc_s_interface_not_exported"></span>**\_interfaccia RPC \_ \_ non \_ esportata**</span><span class="sxs-lookup"><span data-stu-id="e8037-584"><span id="RPC_S_INTERFACE_NOT_EXPORTED"></span><span id="rpc_s_interface_not_exported"></span>**RPC\_S\_INTERFACE\_NOT\_EXPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-585">1924 (0x784)</span><span class="sxs-lookup"><span data-stu-id="e8037-585">1924 (0x784)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-586">Impossibile esportare l'interfaccia nella voce specificata.</span><span class="sxs-lookup"><span data-stu-id="e8037-586">Interface could not be exported to the specified entry.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-587"><span id="RPC_S_PROFILE_NOT_ADDED"></span><span id="rpc_s_profile_not_added"></span>**\_ \_ il profilo RPC \_ non è stato \_ aggiunto**</span><span class="sxs-lookup"><span data-stu-id="e8037-587"><span id="RPC_S_PROFILE_NOT_ADDED"></span><span id="rpc_s_profile_not_added"></span>**RPC\_S\_PROFILE\_NOT\_ADDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-588">1925 (0x785)</span><span class="sxs-lookup"><span data-stu-id="e8037-588">1925 (0x785)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-589">Impossibile aggiungere la voce del profilo specificata.</span><span class="sxs-lookup"><span data-stu-id="e8037-589">The specified profile entry could not be added.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-590"><span id="RPC_S_PRF_ELT_NOT_ADDED"></span><span id="rpc_s_prf_elt_not_added"></span>**RPC \_ per \_ PRF \_ \_ non \_ aggiunti**</span><span class="sxs-lookup"><span data-stu-id="e8037-590"><span id="RPC_S_PRF_ELT_NOT_ADDED"></span><span id="rpc_s_prf_elt_not_added"></span>**RPC\_S\_PRF\_ELT\_NOT\_ADDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-591">1926 (0x786)</span><span class="sxs-lookup"><span data-stu-id="e8037-591">1926 (0x786)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-592">Non è stato possibile aggiungere l'elemento del profilo specificato.</span><span class="sxs-lookup"><span data-stu-id="e8037-592">The specified profile element could not be added.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-593"><span id="RPC_S_PRF_ELT_NOT_REMOVED"></span><span id="rpc_s_prf_elt_not_removed"></span>**RPC \_ \_ PRF \_ ELT \_ non \_ rimosso**</span><span class="sxs-lookup"><span data-stu-id="e8037-593"><span id="RPC_S_PRF_ELT_NOT_REMOVED"></span><span id="rpc_s_prf_elt_not_removed"></span>**RPC\_S\_PRF\_ELT\_NOT\_REMOVED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-594">1927 (0x787)</span><span class="sxs-lookup"><span data-stu-id="e8037-594">1927 (0x787)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-595">Non è stato possibile rimuovere l'elemento del profilo specificato.</span><span class="sxs-lookup"><span data-stu-id="e8037-595">The specified profile element could not be removed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-596"><span id="RPC_S_GRP_ELT_NOT_ADDED"></span><span id="rpc_s_grp_elt_not_added"></span>**RPC \_ \_ GRP \_ ELT \_ non \_ aggiunto**</span><span class="sxs-lookup"><span data-stu-id="e8037-596"><span id="RPC_S_GRP_ELT_NOT_ADDED"></span><span id="rpc_s_grp_elt_not_added"></span>**RPC\_S\_GRP\_ELT\_NOT\_ADDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-597">1928 (0x788)</span><span class="sxs-lookup"><span data-stu-id="e8037-597">1928 (0x788)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-598">Non è stato possibile aggiungere l'elemento di gruppo.</span><span class="sxs-lookup"><span data-stu-id="e8037-598">The group element could not be added.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-599"><span id="RPC_S_GRP_ELT_NOT_REMOVED"></span><span id="rpc_s_grp_elt_not_removed"></span>**RPC \_ \_ GRP \_ ELT \_ non \_ rimosso**</span><span class="sxs-lookup"><span data-stu-id="e8037-599"><span id="RPC_S_GRP_ELT_NOT_REMOVED"></span><span id="rpc_s_grp_elt_not_removed"></span>**RPC\_S\_GRP\_ELT\_NOT\_REMOVED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-600">1929 (0x789)</span><span class="sxs-lookup"><span data-stu-id="e8037-600">1929 (0x789)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-601">Non è stato possibile rimuovere l'elemento del gruppo.</span><span class="sxs-lookup"><span data-stu-id="e8037-601">The group element could not be removed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-602"><span id="ERROR_KM_DRIVER_BLOCKED"></span><span id="error_km_driver_blocked"></span>**ERRORE \_ km \_ driver \_ bloccato**</span><span class="sxs-lookup"><span data-stu-id="e8037-602"><span id="ERROR_KM_DRIVER_BLOCKED"></span><span id="error_km_driver_blocked"></span>**ERROR\_KM\_DRIVER\_BLOCKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-603">1930 (0x78A)</span><span class="sxs-lookup"><span data-stu-id="e8037-603">1930 (0x78A)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-604">Il driver della stampante non è compatibile con i criteri abilitati nel computer che blocca i driver NT 4,0.</span><span class="sxs-lookup"><span data-stu-id="e8037-604">The printer driver is not compatible with a policy enabled on your computer that blocks NT 4.0 drivers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-605"><span id="ERROR_CONTEXT_EXPIRED"></span><span id="error_context_expired"></span>**contesto di errore \_ \_ scaduto**</span><span class="sxs-lookup"><span data-stu-id="e8037-605"><span id="ERROR_CONTEXT_EXPIRED"></span><span id="error_context_expired"></span>**ERROR\_CONTEXT\_EXPIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-606">1931 (0x78B)</span><span class="sxs-lookup"><span data-stu-id="e8037-606">1931 (0x78B)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-607">Il contesto è scaduto e non può più essere utilizzato.</span><span class="sxs-lookup"><span data-stu-id="e8037-607">The context has expired and can no longer be used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-608"><span id="ERROR_PER_USER_TRUST_QUOTA_EXCEEDED"></span><span id="error_per_user_trust_quota_exceeded"></span>**ERRORE \_ per \_ \_ quota di attendibilità utente \_ \_ superata**</span><span class="sxs-lookup"><span data-stu-id="e8037-608"><span id="ERROR_PER_USER_TRUST_QUOTA_EXCEEDED"></span><span id="error_per_user_trust_quota_exceeded"></span>**ERROR\_PER\_USER\_TRUST\_QUOTA\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-609">1932 (0x78C)</span><span class="sxs-lookup"><span data-stu-id="e8037-609">1932 (0x78C)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-610">È stata superata la quota di creazione trust delegata dell'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="e8037-610">The current user's delegated trust creation quota has been exceeded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-611"><span id="ERROR_ALL_USER_TRUST_QUOTA_EXCEEDED"></span><span id="error_all_user_trust_quota_exceeded"></span>**ERRORE per \_ tutte le \_ quote di \_ attendibilità utente \_ \_ superate**</span><span class="sxs-lookup"><span data-stu-id="e8037-611"><span id="ERROR_ALL_USER_TRUST_QUOTA_EXCEEDED"></span><span id="error_all_user_trust_quota_exceeded"></span>**ERROR\_ALL\_USER\_TRUST\_QUOTA\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-612">1933 (0x78D)</span><span class="sxs-lookup"><span data-stu-id="e8037-612">1933 (0x78D)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-613">È stata superata la quota totale di creazione attendibile delegata.</span><span class="sxs-lookup"><span data-stu-id="e8037-613">The total delegated trust creation quota has been exceeded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-614"><span id="ERROR_USER_DELETE_TRUST_QUOTA_EXCEEDED"></span><span id="error_user_delete_trust_quota_exceeded"></span>**\_ \_ \_ superamento della quota di attendibilità Elimina utente \_ errore \_**</span><span class="sxs-lookup"><span data-stu-id="e8037-614"><span id="ERROR_USER_DELETE_TRUST_QUOTA_EXCEEDED"></span><span id="error_user_delete_trust_quota_exceeded"></span>**ERROR\_USER\_DELETE\_TRUST\_QUOTA\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-615">1934 (0x78E)</span><span class="sxs-lookup"><span data-stu-id="e8037-615">1934 (0x78E)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-616">È stata superata la quota di eliminazione Trust delegata dell'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="e8037-616">The current user's delegated trust deletion quota has been exceeded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-617"><span id="ERROR_AUTHENTICATION_FIREWALL_FAILED"></span><span id="error_authentication_firewall_failed"></span>**ERRORE \_ del \_ firewall di autenticazione \_**</span><span class="sxs-lookup"><span data-stu-id="e8037-617"><span id="ERROR_AUTHENTICATION_FIREWALL_FAILED"></span><span id="error_authentication_firewall_failed"></span>**ERROR\_AUTHENTICATION\_FIREWALL\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-618">1935 (0x78F)</span><span class="sxs-lookup"><span data-stu-id="e8037-618">1935 (0x78F)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-619">Il computer a cui si sta effettuando l'accesso è protetto da un firewall di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="e8037-619">The computer you are signing into is protected by an authentication firewall.</span></span> <span data-ttu-id="e8037-620">L'account specificato non è autorizzato a eseguire l'autenticazione nel computer.</span><span class="sxs-lookup"><span data-stu-id="e8037-620">The specified account is not allowed to authenticate to the computer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-621"><span id="ERROR_REMOTE_PRINT_CONNECTIONS_BLOCKED"></span><span id="error_remote_print_connections_blocked"></span>**ERRORE \_ \_ connessioni di stampa Remote \_ \_ bloccate**</span><span class="sxs-lookup"><span data-stu-id="e8037-621"><span id="ERROR_REMOTE_PRINT_CONNECTIONS_BLOCKED"></span><span id="error_remote_print_connections_blocked"></span>**ERROR\_REMOTE\_PRINT\_CONNECTIONS\_BLOCKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-622">1936 (0x790)</span><span class="sxs-lookup"><span data-stu-id="e8037-622">1936 (0x790)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-623">Le connessioni remote allo spooler di stampa sono bloccate da un set di criteri nel computer.</span><span class="sxs-lookup"><span data-stu-id="e8037-623">Remote connections to the Print Spooler are blocked by a policy set on your machine.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-624"><span id="ERROR_NTLM_BLOCKED"></span><span id="error_ntlm_blocked"></span>**ERRORE \_ NTLM \_ bloccato**</span><span class="sxs-lookup"><span data-stu-id="e8037-624"><span id="ERROR_NTLM_BLOCKED"></span><span id="error_ntlm_blocked"></span>**ERROR\_NTLM\_BLOCKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-625">1937 (0x791)</span><span class="sxs-lookup"><span data-stu-id="e8037-625">1937 (0x791)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-626">Autenticazione non riuscita perché l'autenticazione NTLM è stata disabilitata.</span><span class="sxs-lookup"><span data-stu-id="e8037-626">Authentication failed because NTLM authentication has been disabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-627"><span id="ERROR_PASSWORD_CHANGE_REQUIRED"></span><span id="error_password_change_required"></span>**modifica della password di errore \_ \_ \_ obbligatoria**</span><span class="sxs-lookup"><span data-stu-id="e8037-627"><span id="ERROR_PASSWORD_CHANGE_REQUIRED"></span><span id="error_password_change_required"></span>**ERROR\_PASSWORD\_CHANGE\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-628">1938 (0x792)</span><span class="sxs-lookup"><span data-stu-id="e8037-628">1938 (0x792)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-629">Errore di accesso: i criteri EAS richiedono che l'utente modifichi la password prima di poter eseguire questa operazione.</span><span class="sxs-lookup"><span data-stu-id="e8037-629">Logon Failure: EAS policy requires that the user change their password before this operation can be performed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-630"><span id="ERROR_INVALID_PIXEL_FORMAT"></span><span id="error_invalid_pixel_format"></span>**ERRORE \_ nel \_ formato pixel non valido \_**</span><span class="sxs-lookup"><span data-stu-id="e8037-630"><span id="ERROR_INVALID_PIXEL_FORMAT"></span><span id="error_invalid_pixel_format"></span>**ERROR\_INVALID\_PIXEL\_FORMAT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-631">2000 (0x7D0)</span><span class="sxs-lookup"><span data-stu-id="e8037-631">2000 (0x7D0)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-632">Il formato pixel non è valido.</span><span class="sxs-lookup"><span data-stu-id="e8037-632">The pixel format is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-633"><span id="ERROR_BAD_DRIVER"></span><span id="error_bad_driver"></span>**ERRORE \_ \_ driver errato**</span><span class="sxs-lookup"><span data-stu-id="e8037-633"><span id="ERROR_BAD_DRIVER"></span><span id="error_bad_driver"></span>**ERROR\_BAD\_DRIVER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-634">2001 (0x7D1)</span><span class="sxs-lookup"><span data-stu-id="e8037-634">2001 (0x7D1)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-635">Il driver specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="e8037-635">The specified driver is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-636"><span id="ERROR_INVALID_WINDOW_STYLE"></span><span id="error_invalid_window_style"></span>**ERRORE \_ \_ stile finestra non valido \_**</span><span class="sxs-lookup"><span data-stu-id="e8037-636"><span id="ERROR_INVALID_WINDOW_STYLE"></span><span id="error_invalid_window_style"></span>**ERROR\_INVALID\_WINDOW\_STYLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-637">2002 (0x7D2)</span><span class="sxs-lookup"><span data-stu-id="e8037-637">2002 (0x7D2)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-638">Lo stile della finestra o l'attributo della classe non è valido per questa operazione.</span><span class="sxs-lookup"><span data-stu-id="e8037-638">The window style or class attribute is invalid for this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-639"><span id="ERROR_METAFILE_NOT_SUPPORTED"></span><span id="error_metafile_not_supported"></span>**ERRORE \_ metafile \_ non \_ supportato**</span><span class="sxs-lookup"><span data-stu-id="e8037-639"><span id="ERROR_METAFILE_NOT_SUPPORTED"></span><span id="error_metafile_not_supported"></span>**ERROR\_METAFILE\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-640">2003 (0x7D3)</span><span class="sxs-lookup"><span data-stu-id="e8037-640">2003 (0x7D3)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-641">Operazione metafile richiesta non supportata.</span><span class="sxs-lookup"><span data-stu-id="e8037-641">The requested metafile operation is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-642"><span id="ERROR_TRANSFORM_NOT_SUPPORTED"></span><span id="error_transform_not_supported"></span>**\_trasformazione errore \_ non \_ supportata**</span><span class="sxs-lookup"><span data-stu-id="e8037-642"><span id="ERROR_TRANSFORM_NOT_SUPPORTED"></span><span id="error_transform_not_supported"></span>**ERROR\_TRANSFORM\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-643">2004 (0x7D4)</span><span class="sxs-lookup"><span data-stu-id="e8037-643">2004 (0x7D4)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-644">Operazione di trasformazione richiesta non supportata.</span><span class="sxs-lookup"><span data-stu-id="e8037-644">The requested transformation operation is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-645"><span id="ERROR_CLIPPING_NOT_SUPPORTED"></span><span id="error_clipping_not_supported"></span>**il \_ ritaglio degli errori \_ non è \_ supportato**</span><span class="sxs-lookup"><span data-stu-id="e8037-645"><span id="ERROR_CLIPPING_NOT_SUPPORTED"></span><span id="error_clipping_not_supported"></span>**ERROR\_CLIPPING\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-646">2005 (0x7D5)</span><span class="sxs-lookup"><span data-stu-id="e8037-646">2005 (0x7D5)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-647">Operazione di ritaglio richiesta non supportata.</span><span class="sxs-lookup"><span data-stu-id="e8037-647">The requested clipping operation is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-648"><span id="ERROR_INVALID_CMM"></span><span id="error_invalid_cmm"></span>**ERRORE \_ CMM non valido \_**</span><span class="sxs-lookup"><span data-stu-id="e8037-648"><span id="ERROR_INVALID_CMM"></span><span id="error_invalid_cmm"></span>**ERROR\_INVALID\_CMM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-649">2010 (0x7DA)</span><span class="sxs-lookup"><span data-stu-id="e8037-649">2010 (0x7DA)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-650">Il modulo di gestione colori specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="e8037-650">The specified color management module is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-651"><span id="ERROR_INVALID_PROFILE"></span><span id="error_invalid_profile"></span>**ERRORE \_ profilo non valido \_**</span><span class="sxs-lookup"><span data-stu-id="e8037-651"><span id="ERROR_INVALID_PROFILE"></span><span id="error_invalid_profile"></span>**ERROR\_INVALID\_PROFILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-652">2011 (0x7DB)</span><span class="sxs-lookup"><span data-stu-id="e8037-652">2011 (0x7DB)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-653">Il profilo colori specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="e8037-653">The specified color profile is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-654"><span id="ERROR_TAG_NOT_FOUND"></span><span id="error_tag_not_found"></span>**Tag di errore \_ \_ non \_ trovato**</span><span class="sxs-lookup"><span data-stu-id="e8037-654"><span id="ERROR_TAG_NOT_FOUND"></span><span id="error_tag_not_found"></span>**ERROR\_TAG\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-655">2012 (0x7DC)</span><span class="sxs-lookup"><span data-stu-id="e8037-655">2012 (0x7DC)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-656">Il tag specificato non è stato trovato.</span><span class="sxs-lookup"><span data-stu-id="e8037-656">The specified tag was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-657"><span id="ERROR_TAG_NOT_PRESENT"></span><span id="error_tag_not_present"></span>**Tag di errore \_ \_ non \_ presente**</span><span class="sxs-lookup"><span data-stu-id="e8037-657"><span id="ERROR_TAG_NOT_PRESENT"></span><span id="error_tag_not_present"></span>**ERROR\_TAG\_NOT\_PRESENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-658">2013 (0x7DD)</span><span class="sxs-lookup"><span data-stu-id="e8037-658">2013 (0x7DD)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-659">Un tag obbligatorio non è presente.</span><span class="sxs-lookup"><span data-stu-id="e8037-659">A required tag is not present.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-660"><span id="ERROR_DUPLICATE_TAG"></span><span id="error_duplicate_tag"></span>**ERRORE \_ tag duplicato \_**</span><span class="sxs-lookup"><span data-stu-id="e8037-660"><span id="ERROR_DUPLICATE_TAG"></span><span id="error_duplicate_tag"></span>**ERROR\_DUPLICATE\_TAG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-661">2014 (0x7DE)</span><span class="sxs-lookup"><span data-stu-id="e8037-661">2014 (0x7DE)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-662">Il tag specificato è già presente.</span><span class="sxs-lookup"><span data-stu-id="e8037-662">The specified tag is already present.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-663"><span id="ERROR_PROFILE_NOT_ASSOCIATED_WITH_DEVICE"></span><span id="error_profile_not_associated_with_device"></span>**\_profilo errore \_ non \_ associato \_ al \_ dispositivo**</span><span class="sxs-lookup"><span data-stu-id="e8037-663"><span id="ERROR_PROFILE_NOT_ASSOCIATED_WITH_DEVICE"></span><span id="error_profile_not_associated_with_device"></span>**ERROR\_PROFILE\_NOT\_ASSOCIATED\_WITH\_DEVICE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-664">2015 (0x7DF)</span><span class="sxs-lookup"><span data-stu-id="e8037-664">2015 (0x7DF)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-665">Il profilo colori specificato non è associato al dispositivo specificato.</span><span class="sxs-lookup"><span data-stu-id="e8037-665">The specified color profile is not associated with the specified device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-666"><span id="ERROR_PROFILE_NOT_FOUND"></span><span id="error_profile_not_found"></span>**\_profilo errore \_ non \_ trovato**</span><span class="sxs-lookup"><span data-stu-id="e8037-666"><span id="ERROR_PROFILE_NOT_FOUND"></span><span id="error_profile_not_found"></span>**ERROR\_PROFILE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-667">2016 (0x7E0)</span><span class="sxs-lookup"><span data-stu-id="e8037-667">2016 (0x7E0)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-668">Il profilo colori specificato non è stato trovato.</span><span class="sxs-lookup"><span data-stu-id="e8037-668">The specified color profile was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-669"><span id="ERROR_INVALID_COLORSPACE"></span><span id="error_invalid_colorspace"></span>**ERRORE \_ dello \_ spazio di colore non valido**</span><span class="sxs-lookup"><span data-stu-id="e8037-669"><span id="ERROR_INVALID_COLORSPACE"></span><span id="error_invalid_colorspace"></span>**ERROR\_INVALID\_COLORSPACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-670">2017 (0x7E1)</span><span class="sxs-lookup"><span data-stu-id="e8037-670">2017 (0x7E1)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-671">Lo spazio dei colori specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="e8037-671">The specified color space is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-672"><span id="ERROR_ICM_NOT_ENABLED"></span><span id="error_icm_not_enabled"></span>**ERRORE \_ ICM \_ non \_ abilitato**</span><span class="sxs-lookup"><span data-stu-id="e8037-672"><span id="ERROR_ICM_NOT_ENABLED"></span><span id="error_icm_not_enabled"></span>**ERROR\_ICM\_NOT\_ENABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-673">2018 (0x7E2)</span><span class="sxs-lookup"><span data-stu-id="e8037-673">2018 (0x7E2)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-674">La gestione dei colori dell'immagine non è abilitata.</span><span class="sxs-lookup"><span data-stu-id="e8037-674">Image Color Management is not enabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-675"><span id="ERROR_DELETING_ICM_XFORM"></span><span id="error_deleting_icm_xform"></span>**errore durante l' \_ eliminazione di \_ MCI. \_**</span><span class="sxs-lookup"><span data-stu-id="e8037-675"><span id="ERROR_DELETING_ICM_XFORM"></span><span id="error_deleting_icm_xform"></span>**ERROR\_DELETING\_ICM\_XFORM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-676">2019 (0x7E3)</span><span class="sxs-lookup"><span data-stu-id="e8037-676">2019 (0x7E3)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-677">Si è verificato un errore durante l'eliminazione della trasformazione colore.</span><span class="sxs-lookup"><span data-stu-id="e8037-677">There was an error while deleting the color transform.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-678"><span id="ERROR_INVALID_TRANSFORM"></span><span id="error_invalid_transform"></span>**\_trasformazione errore non valida \_**</span><span class="sxs-lookup"><span data-stu-id="e8037-678"><span id="ERROR_INVALID_TRANSFORM"></span><span id="error_invalid_transform"></span>**ERROR\_INVALID\_TRANSFORM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-679">2020 (0x7E4)</span><span class="sxs-lookup"><span data-stu-id="e8037-679">2020 (0x7E4)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-680">La trasformazione colore specificata non è valida.</span><span class="sxs-lookup"><span data-stu-id="e8037-680">The specified color transform is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-681"><span id="ERROR_COLORSPACE_MISMATCH"></span><span id="error_colorspace_mismatch"></span>**ERRORE di \_ corrispondenza dello spazio di colore \_**</span><span class="sxs-lookup"><span data-stu-id="e8037-681"><span id="ERROR_COLORSPACE_MISMATCH"></span><span id="error_colorspace_mismatch"></span>**ERROR\_COLORSPACE\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-682">2021 (0x7E5)</span><span class="sxs-lookup"><span data-stu-id="e8037-682">2021 (0x7E5)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-683">La trasformazione specificata non corrisponde allo spazio dei colori della bitmap.</span><span class="sxs-lookup"><span data-stu-id="e8037-683">The specified transform does not match the bitmap's color space.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-684"><span id="ERROR_INVALID_COLORINDEX"></span><span id="error_invalid_colorindex"></span>**ERRORE \_ ColorIndex non valido \_**</span><span class="sxs-lookup"><span data-stu-id="e8037-684"><span id="ERROR_INVALID_COLORINDEX"></span><span id="error_invalid_colorindex"></span>**ERROR\_INVALID\_COLORINDEX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-685">2022 (0x7E6)</span><span class="sxs-lookup"><span data-stu-id="e8037-685">2022 (0x7E6)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-686">L'indice dei colori denominato specificato non è presente nel profilo.</span><span class="sxs-lookup"><span data-stu-id="e8037-686">The specified named color index is not present in the profile.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-687"><span id="ERROR_PROFILE_DOES_NOT_MATCH_DEVICE"></span><span id="error_profile_does_not_match_device"></span>**\_il profilo errore non \_ corrisponde al \_ \_ \_ dispositivo**</span><span class="sxs-lookup"><span data-stu-id="e8037-687"><span id="ERROR_PROFILE_DOES_NOT_MATCH_DEVICE"></span><span id="error_profile_does_not_match_device"></span>**ERROR\_PROFILE\_DOES\_NOT\_MATCH\_DEVICE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-688">2023 (0x7E7)</span><span class="sxs-lookup"><span data-stu-id="e8037-688">2023 (0x7E7)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-689">Il profilo specificato è destinato a un dispositivo di un tipo diverso dal dispositivo specificato.</span><span class="sxs-lookup"><span data-stu-id="e8037-689">The specified profile is intended for a device of a different type than the specified device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-690"><span id="ERROR_CONNECTED_OTHER_PASSWORD"></span><span id="error_connected_other_password"></span>**ERRORE \_ connesso \_ altra \_ password**</span><span class="sxs-lookup"><span data-stu-id="e8037-690"><span id="ERROR_CONNECTED_OTHER_PASSWORD"></span><span id="error_connected_other_password"></span>**ERROR\_CONNECTED\_OTHER\_PASSWORD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-691">2108 (0x83C)</span><span class="sxs-lookup"><span data-stu-id="e8037-691">2108 (0x83C)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-692">La connessione di rete è stata eseguita correttamente, ma all'utente è stata richiesta una password diversa da quella specificata in origine.</span><span class="sxs-lookup"><span data-stu-id="e8037-692">The network connection was made successfully, but the user had to be prompted for a password other than the one originally specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-693"><span id="ERROR_CONNECTED_OTHER_PASSWORD_DEFAULT"></span><span id="error_connected_other_password_default"></span>**ERRORE \_ connesso \_ altra \_ password \_ predefinita**</span><span class="sxs-lookup"><span data-stu-id="e8037-693"><span id="ERROR_CONNECTED_OTHER_PASSWORD_DEFAULT"></span><span id="error_connected_other_password_default"></span>**ERROR\_CONNECTED\_OTHER\_PASSWORD\_DEFAULT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-694">2109 (0x83D)</span><span class="sxs-lookup"><span data-stu-id="e8037-694">2109 (0x83D)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-695">La connessione di rete è stata eseguita correttamente usando le credenziali predefinite.</span><span class="sxs-lookup"><span data-stu-id="e8037-695">The network connection was made successfully using default credentials.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-696"><span id="ERROR_BAD_USERNAME"></span><span id="error_bad_username"></span>**ERRORE \_ \_ nome utente errato**</span><span class="sxs-lookup"><span data-stu-id="e8037-696"><span id="ERROR_BAD_USERNAME"></span><span id="error_bad_username"></span>**ERROR\_BAD\_USERNAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-697">2202 (0x89A)</span><span class="sxs-lookup"><span data-stu-id="e8037-697">2202 (0x89A)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-698">Il nome utente specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="e8037-698">The specified username is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-699"><span id="ERROR_NOT_CONNECTED"></span><span id="error_not_connected"></span>**ERRORE \_ non \_ connesso**</span><span class="sxs-lookup"><span data-stu-id="e8037-699"><span id="ERROR_NOT_CONNECTED"></span><span id="error_not_connected"></span>**ERROR\_NOT\_CONNECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-700">2250 (0x8CA)</span><span class="sxs-lookup"><span data-stu-id="e8037-700">2250 (0x8CA)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-701">Questa connessione di rete non esiste.</span><span class="sxs-lookup"><span data-stu-id="e8037-701">This network connection does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-702"><span id="ERROR_OPEN_FILES"></span><span id="error_open_files"></span>**ERRORE di \_ apertura dei \_ file**</span><span class="sxs-lookup"><span data-stu-id="e8037-702"><span id="ERROR_OPEN_FILES"></span><span id="error_open_files"></span>**ERROR\_OPEN\_FILES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-703">2401 (0x961)</span><span class="sxs-lookup"><span data-stu-id="e8037-703">2401 (0x961)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-704">Questa connessione di rete contiene file aperti o richieste in sospeso.</span><span class="sxs-lookup"><span data-stu-id="e8037-704">This network connection has files open or requests pending.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-705"><span id="ERROR_ACTIVE_CONNECTIONS"></span><span id="error_active_connections"></span>**ERRORE \_ \_ connessioni attive**</span><span class="sxs-lookup"><span data-stu-id="e8037-705"><span id="ERROR_ACTIVE_CONNECTIONS"></span><span id="error_active_connections"></span>**ERROR\_ACTIVE\_CONNECTIONS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-706">2402 (0x962)</span><span class="sxs-lookup"><span data-stu-id="e8037-706">2402 (0x962)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-707">Sono ancora presenti connessioni attive.</span><span class="sxs-lookup"><span data-stu-id="e8037-707">Active connections still exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-708"><span id="ERROR_DEVICE_IN_USE"></span><span id="error_device_in_use"></span>**\_dispositivo \_ di errore in \_ uso**</span><span class="sxs-lookup"><span data-stu-id="e8037-708"><span id="ERROR_DEVICE_IN_USE"></span><span id="error_device_in_use"></span>**ERROR\_DEVICE\_IN\_USE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-709">2404 (0x964)</span><span class="sxs-lookup"><span data-stu-id="e8037-709">2404 (0x964)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-710">Il dispositivo è usato da un processo attivo e non può essere disconnesso.</span><span class="sxs-lookup"><span data-stu-id="e8037-710">The device is in use by an active process and cannot be disconnected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-711"><span id="ERROR_UNKNOWN_PRINT_MONITOR"></span><span id="error_unknown_print_monitor"></span>**ERRORE \_ di \_ monitoraggio stampa sconosciuto \_**</span><span class="sxs-lookup"><span data-stu-id="e8037-711"><span id="ERROR_UNKNOWN_PRINT_MONITOR"></span><span id="error_unknown_print_monitor"></span>**ERROR\_UNKNOWN\_PRINT\_MONITOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-712">3000 (0xBB8)</span><span class="sxs-lookup"><span data-stu-id="e8037-712">3000 (0xBB8)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-713">Il monitor di stampa specificato è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="e8037-713">The specified print monitor is unknown.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-714"><span id="ERROR_PRINTER_DRIVER_IN_USE"></span><span id="error_printer_driver_in_use"></span>**\_driver della \_ stampante \_ di errore in \_ uso**</span><span class="sxs-lookup"><span data-stu-id="e8037-714"><span id="ERROR_PRINTER_DRIVER_IN_USE"></span><span id="error_printer_driver_in_use"></span>**ERROR\_PRINTER\_DRIVER\_IN\_USE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-715">3001 (0xBB9)</span><span class="sxs-lookup"><span data-stu-id="e8037-715">3001 (0xBB9)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-716">Il driver della stampante specificato è attualmente in uso.</span><span class="sxs-lookup"><span data-stu-id="e8037-716">The specified printer driver is currently in use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-717"><span id="ERROR_SPOOL_FILE_NOT_FOUND"></span><span id="error_spool_file_not_found"></span>**\_ \_ \_ Impossibile trovare il file di SPOOLing degli errori \_**</span><span class="sxs-lookup"><span data-stu-id="e8037-717"><span id="ERROR_SPOOL_FILE_NOT_FOUND"></span><span id="error_spool_file_not_found"></span>**ERROR\_SPOOL\_FILE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-718">3002 (0xBBA)</span><span class="sxs-lookup"><span data-stu-id="e8037-718">3002 (0xBBA)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-719">Impossibile trovare il file di spooling.</span><span class="sxs-lookup"><span data-stu-id="e8037-719">The spool file was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-720"><span id="ERROR_SPL_NO_STARTDOC"></span><span id="error_spl_no_startdoc"></span>**ERRORE \_ SPL \_ nessun \_ StartDoc**</span><span class="sxs-lookup"><span data-stu-id="e8037-720"><span id="ERROR_SPL_NO_STARTDOC"></span><span id="error_spl_no_startdoc"></span>**ERROR\_SPL\_NO\_STARTDOC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-721">3003 (0xBBB)</span><span class="sxs-lookup"><span data-stu-id="e8037-721">3003 (0xBBB)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-722">Una chiamata StartDocPrinter non è stata rilasciata.</span><span class="sxs-lookup"><span data-stu-id="e8037-722">A StartDocPrinter call was not issued.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-723"><span id="ERROR_SPL_NO_ADDJOB"></span><span id="error_spl_no_addjob"></span>**ERRORE \_ SPL \_ nessun \_ ADDJOB**</span><span class="sxs-lookup"><span data-stu-id="e8037-723"><span id="ERROR_SPL_NO_ADDJOB"></span><span id="error_spl_no_addjob"></span>**ERROR\_SPL\_NO\_ADDJOB**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-724">3004 (0xBBC)</span><span class="sxs-lookup"><span data-stu-id="e8037-724">3004 (0xBBC)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-725">Una chiamata AddJob non è stata rilasciata.</span><span class="sxs-lookup"><span data-stu-id="e8037-725">An AddJob call was not issued.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-726"><span id="ERROR_PRINT_PROCESSOR_ALREADY_INSTALLED"></span><span id="error_print_processor_already_installed"></span>**processore di stampa degli errori \_ \_ \_ già \_ installato**</span><span class="sxs-lookup"><span data-stu-id="e8037-726"><span id="ERROR_PRINT_PROCESSOR_ALREADY_INSTALLED"></span><span id="error_print_processor_already_installed"></span>**ERROR\_PRINT\_PROCESSOR\_ALREADY\_INSTALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-727">3005 (0xBBD)</span><span class="sxs-lookup"><span data-stu-id="e8037-727">3005 (0xBBD)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-728">Il processore di stampa specificato è già stato installato.</span><span class="sxs-lookup"><span data-stu-id="e8037-728">The specified print processor has already been installed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-729"><span id="ERROR_PRINT_MONITOR_ALREADY_INSTALLED"></span><span id="error_print_monitor_already_installed"></span>**il monitoraggio della stampa degli errori è \_ \_ \_ già \_ installato**</span><span class="sxs-lookup"><span data-stu-id="e8037-729"><span id="ERROR_PRINT_MONITOR_ALREADY_INSTALLED"></span><span id="error_print_monitor_already_installed"></span>**ERROR\_PRINT\_MONITOR\_ALREADY\_INSTALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-730">3006 (0xBBE)</span><span class="sxs-lookup"><span data-stu-id="e8037-730">3006 (0xBBE)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-731">Il monitor di stampa specificato è già stato installato.</span><span class="sxs-lookup"><span data-stu-id="e8037-731">The specified print monitor has already been installed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-732"><span id="ERROR_INVALID_PRINT_MONITOR"></span><span id="error_invalid_print_monitor"></span>**ERRORE \_ di \_ monitoraggio stampa non valido \_**</span><span class="sxs-lookup"><span data-stu-id="e8037-732"><span id="ERROR_INVALID_PRINT_MONITOR"></span><span id="error_invalid_print_monitor"></span>**ERROR\_INVALID\_PRINT\_MONITOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-733">3007 (0xBBF)</span><span class="sxs-lookup"><span data-stu-id="e8037-733">3007 (0xBBF)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-734">Il monitor di stampa specificato non dispone delle funzioni obbligatorie.</span><span class="sxs-lookup"><span data-stu-id="e8037-734">The specified print monitor does not have the required functions.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-735"><span id="ERROR_PRINT_MONITOR_IN_USE"></span><span id="error_print_monitor_in_use"></span>**\_monitoraggio di stampa degli errori \_ \_ in \_ uso**</span><span class="sxs-lookup"><span data-stu-id="e8037-735"><span id="ERROR_PRINT_MONITOR_IN_USE"></span><span id="error_print_monitor_in_use"></span>**ERROR\_PRINT\_MONITOR\_IN\_USE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-736">3008 (0xBC0)</span><span class="sxs-lookup"><span data-stu-id="e8037-736">3008 (0xBC0)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-737">Il monitor di stampa specificato è attualmente in uso.</span><span class="sxs-lookup"><span data-stu-id="e8037-737">The specified print monitor is currently in use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-738"><span id="ERROR_PRINTER_HAS_JOBS_QUEUED"></span><span id="error_printer_has_jobs_queued"></span>**ERRORE \_ della stampante \_ con \_ processi in \_ coda**</span><span class="sxs-lookup"><span data-stu-id="e8037-738"><span id="ERROR_PRINTER_HAS_JOBS_QUEUED"></span><span id="error_printer_has_jobs_queued"></span>**ERROR\_PRINTER\_HAS\_JOBS\_QUEUED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-739">3009 (0xBC1)</span><span class="sxs-lookup"><span data-stu-id="e8037-739">3009 (0xBC1)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-740">L'operazione richiesta non è consentita quando sono presenti processi accodati alla stampante.</span><span class="sxs-lookup"><span data-stu-id="e8037-740">The requested operation is not allowed when there are jobs queued to the printer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-741"><span id="ERROR_SUCCESS_REBOOT_REQUIRED"></span><span id="error_success_reboot_required"></span>**ERRORE \_ di \_ riavvio \_ necessario**</span><span class="sxs-lookup"><span data-stu-id="e8037-741"><span id="ERROR_SUCCESS_REBOOT_REQUIRED"></span><span id="error_success_reboot_required"></span>**ERROR\_SUCCESS\_REBOOT\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-742">3010 (0xBC2)</span><span class="sxs-lookup"><span data-stu-id="e8037-742">3010 (0xBC2)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-743">Operazione richiesta completata.</span><span class="sxs-lookup"><span data-stu-id="e8037-743">The requested operation is successful.</span></span> <span data-ttu-id="e8037-744">Le modifiche non saranno effettive fino al riavvio del sistema.</span><span class="sxs-lookup"><span data-stu-id="e8037-744">Changes will not be effective until the system is rebooted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-745"><span id="ERROR_SUCCESS_RESTART_REQUIRED"></span><span id="error_success_restart_required"></span>**ERRORE \_ di \_ riavvio \_ necessario**</span><span class="sxs-lookup"><span data-stu-id="e8037-745"><span id="ERROR_SUCCESS_RESTART_REQUIRED"></span><span id="error_success_restart_required"></span>**ERROR\_SUCCESS\_RESTART\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-746">3011 (0xBC3)</span><span class="sxs-lookup"><span data-stu-id="e8037-746">3011 (0xBC3)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-747">Operazione richiesta completata.</span><span class="sxs-lookup"><span data-stu-id="e8037-747">The requested operation is successful.</span></span> <span data-ttu-id="e8037-748">Le modifiche non saranno effettive fino a quando il servizio non viene riavviato.</span><span class="sxs-lookup"><span data-stu-id="e8037-748">Changes will not be effective until the service is restarted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-749"><span id="ERROR_PRINTER_NOT_FOUND"></span><span id="error_printer_not_found"></span>**ERRORE di \_ stampante \_ non \_ trovato**</span><span class="sxs-lookup"><span data-stu-id="e8037-749"><span id="ERROR_PRINTER_NOT_FOUND"></span><span id="error_printer_not_found"></span>**ERROR\_PRINTER\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-750">3012 (0xBC4)</span><span class="sxs-lookup"><span data-stu-id="e8037-750">3012 (0xBC4)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-751">Non sono state trovate stampanti.</span><span class="sxs-lookup"><span data-stu-id="e8037-751">No printers were found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-752"><span id="ERROR_PRINTER_DRIVER_WARNED"></span><span id="error_printer_driver_warned"></span>**\_ \_ avviso driver stampante \_ errore**</span><span class="sxs-lookup"><span data-stu-id="e8037-752"><span id="ERROR_PRINTER_DRIVER_WARNED"></span><span id="error_printer_driver_warned"></span>**ERROR\_PRINTER\_DRIVER\_WARNED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-753">3013 (0xBC5)</span><span class="sxs-lookup"><span data-stu-id="e8037-753">3013 (0xBC5)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-754">Il driver della stampante è noto come inaffidabile.</span><span class="sxs-lookup"><span data-stu-id="e8037-754">The printer driver is known to be unreliable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-755"><span id="ERROR_PRINTER_DRIVER_BLOCKED"></span><span id="error_printer_driver_blocked"></span>**\_driver della stampante di errore \_ \_ bloccato**</span><span class="sxs-lookup"><span data-stu-id="e8037-755"><span id="ERROR_PRINTER_DRIVER_BLOCKED"></span><span id="error_printer_driver_blocked"></span>**ERROR\_PRINTER\_DRIVER\_BLOCKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-756">3014 (0xBC6)</span><span class="sxs-lookup"><span data-stu-id="e8037-756">3014 (0xBC6)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-757">Il driver della stampante è noto per danneggiare il sistema.</span><span class="sxs-lookup"><span data-stu-id="e8037-757">The printer driver is known to harm the system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-758"><span id="ERROR_PRINTER_DRIVER_PACKAGE_IN_USE"></span><span id="error_printer_driver_package_in_use"></span>**ERRORE \_ \_ del pacchetto driver della stampante \_ \_ in \_ uso**</span><span class="sxs-lookup"><span data-stu-id="e8037-758"><span id="ERROR_PRINTER_DRIVER_PACKAGE_IN_USE"></span><span id="error_printer_driver_package_in_use"></span>**ERROR\_PRINTER\_DRIVER\_PACKAGE\_IN\_USE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-759">3015 (0xBC7)</span><span class="sxs-lookup"><span data-stu-id="e8037-759">3015 (0xBC7)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-760">Il pacchetto di driver della stampante specificato è attualmente in uso.</span><span class="sxs-lookup"><span data-stu-id="e8037-760">The specified printer driver package is currently in use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-761"><span id="ERROR_CORE_DRIVER_PACKAGE_NOT_FOUND"></span><span id="error_core_driver_package_not_found"></span>**\_ \_ \_ \_ Impossibile trovare il pacchetto driver di base errore \_**</span><span class="sxs-lookup"><span data-stu-id="e8037-761"><span id="ERROR_CORE_DRIVER_PACKAGE_NOT_FOUND"></span><span id="error_core_driver_package_not_found"></span>**ERROR\_CORE\_DRIVER\_PACKAGE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-762">3016 (0xBC8)</span><span class="sxs-lookup"><span data-stu-id="e8037-762">3016 (0xBC8)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-763">Impossibile trovare un pacchetto driver di base richiesto dal pacchetto driver della stampante.</span><span class="sxs-lookup"><span data-stu-id="e8037-763">Unable to find a core driver package that is required by the printer driver package.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-764"><span id="ERROR_FAIL_REBOOT_REQUIRED"></span><span id="error_fail_reboot_required"></span>**ERRORE \_ di \_ riavvio \_ richiesto**</span><span class="sxs-lookup"><span data-stu-id="e8037-764"><span id="ERROR_FAIL_REBOOT_REQUIRED"></span><span id="error_fail_reboot_required"></span>**ERROR\_FAIL\_REBOOT\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-765">3017 (0xBC9)</span><span class="sxs-lookup"><span data-stu-id="e8037-765">3017 (0xBC9)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-766">L'operazione richiesta non è riuscita.</span><span class="sxs-lookup"><span data-stu-id="e8037-766">The requested operation failed.</span></span> <span data-ttu-id="e8037-767">Per eseguire il rollback delle modifiche apportate, è necessario riavviare il sistema.</span><span class="sxs-lookup"><span data-stu-id="e8037-767">A system reboot is required to roll back changes made.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-768"><span id="ERROR_FAIL_REBOOT_INITIATED"></span><span id="error_fail_reboot_initiated"></span>**ERRORE \_ di \_ riavvio \_ avviato**</span><span class="sxs-lookup"><span data-stu-id="e8037-768"><span id="ERROR_FAIL_REBOOT_INITIATED"></span><span id="error_fail_reboot_initiated"></span>**ERROR\_FAIL\_REBOOT\_INITIATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-769">3018 (0xBCA)</span><span class="sxs-lookup"><span data-stu-id="e8037-769">3018 (0xBCA)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-770">L'operazione richiesta non è riuscita.</span><span class="sxs-lookup"><span data-stu-id="e8037-770">The requested operation failed.</span></span> <span data-ttu-id="e8037-771">È stato avviato un riavvio del sistema per eseguire il rollback delle modifiche apportate.</span><span class="sxs-lookup"><span data-stu-id="e8037-771">A system reboot has been initiated to roll back changes made.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-772"><span id="ERROR_PRINTER_DRIVER_DOWNLOAD_NEEDED"></span><span id="error_printer_driver_download_needed"></span>**errore durante il \_ download del driver della stampante \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e8037-772"><span id="ERROR_PRINTER_DRIVER_DOWNLOAD_NEEDED"></span><span id="error_printer_driver_download_needed"></span>**ERROR\_PRINTER\_DRIVER\_DOWNLOAD\_NEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-773">3019 (0xBCB)</span><span class="sxs-lookup"><span data-stu-id="e8037-773">3019 (0xBCB)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-774">Il driver della stampante specificato non è stato trovato nel sistema ed è necessario scaricarlo.</span><span class="sxs-lookup"><span data-stu-id="e8037-774">The specified printer driver was not found on the system and needs to be downloaded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-775"><span id="ERROR_PRINT_JOB_RESTART_REQUIRED"></span><span id="error_print_job_restart_required"></span>**riavvio del processo di stampa degli errori \_ \_ \_ \_ obbligatorio**</span><span class="sxs-lookup"><span data-stu-id="e8037-775"><span id="ERROR_PRINT_JOB_RESTART_REQUIRED"></span><span id="error_print_job_restart_required"></span>**ERROR\_PRINT\_JOB\_RESTART\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-776">3020 (0xBCC)</span><span class="sxs-lookup"><span data-stu-id="e8037-776">3020 (0xBCC)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-777">Impossibile stampare il processo di stampa richiesto.</span><span class="sxs-lookup"><span data-stu-id="e8037-777">The requested print job has failed to print.</span></span> <span data-ttu-id="e8037-778">Per un aggiornamento del sistema di stampa è necessario inviare nuovamente il processo.</span><span class="sxs-lookup"><span data-stu-id="e8037-778">A print system update requires the job to be resubmitted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-779"><span id="ERROR_INVALID_PRINTER_DRIVER_MANIFEST"></span><span id="error_invalid_printer_driver_manifest"></span>**ERRORE \_ del \_ \_ manifesto del driver della stampante non valido \_**</span><span class="sxs-lookup"><span data-stu-id="e8037-779"><span id="ERROR_INVALID_PRINTER_DRIVER_MANIFEST"></span><span id="error_invalid_printer_driver_manifest"></span>**ERROR\_INVALID\_PRINTER\_DRIVER\_MANIFEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-780">3021 (0xBCD)</span><span class="sxs-lookup"><span data-stu-id="e8037-780">3021 (0xBCD)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-781">Il driver della stampante non contiene un manifesto valido o contiene troppi manifesti.</span><span class="sxs-lookup"><span data-stu-id="e8037-781">The printer driver does not contain a valid manifest, or contains too many manifests.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-782"><span id="ERROR_PRINTER_NOT_SHAREABLE"></span><span id="error_printer_not_shareable"></span>**stampante di errore \_ \_ non \_ condivisibile**</span><span class="sxs-lookup"><span data-stu-id="e8037-782"><span id="ERROR_PRINTER_NOT_SHAREABLE"></span><span id="error_printer_not_shareable"></span>**ERROR\_PRINTER\_NOT\_SHAREABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-783">3022 (0xBCE)</span><span class="sxs-lookup"><span data-stu-id="e8037-783">3022 (0xBCE)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-784">La stampante specificata non può essere condivisa.</span><span class="sxs-lookup"><span data-stu-id="e8037-784">The specified printer cannot be shared.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-785"><span id="ERROR_REQUEST_PAUSED"></span><span id="error_request_paused"></span>**richiesta di errore \_ \_ sospesa**</span><span class="sxs-lookup"><span data-stu-id="e8037-785"><span id="ERROR_REQUEST_PAUSED"></span><span id="error_request_paused"></span>**ERROR\_REQUEST\_PAUSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-786">3050 (0xBEA)</span><span class="sxs-lookup"><span data-stu-id="e8037-786">3050 (0xBEA)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-787">L'operazione è stata sospesa.</span><span class="sxs-lookup"><span data-stu-id="e8037-787">The operation was paused.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e8037-788"><span id="ERROR_IO_REISSUE_AS_CACHED"></span><span id="error_io_reissue_as_cached"></span>**ERRORI i/o \_ \_ ristampati \_ come \_ memorizzati nella cache**</span><span class="sxs-lookup"><span data-stu-id="e8037-788"><span id="ERROR_IO_REISSUE_AS_CACHED"></span><span id="error_io_reissue_as_cached"></span>**ERROR\_IO\_REISSUE\_AS\_CACHED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8037-789">3950 (0xF6E)</span><span class="sxs-lookup"><span data-stu-id="e8037-789">3950 (0xF6E)</span></span>
</dt> <dt>



<span data-ttu-id="e8037-790">Eseguire nuovamente l'operazione specificata come operazione di i/o memorizzato nella cache.</span><span class="sxs-lookup"><span data-stu-id="e8037-790">Reissue the given operation as a cached IO operation.</span></span>


</dt> </dl> </dd> </dl>


## <a name="requirements"></a><span data-ttu-id="e8037-791">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e8037-791">Requirements</span></span>



| <span data-ttu-id="e8037-792">Requisito</span><span class="sxs-lookup"><span data-stu-id="e8037-792">Requirement</span></span> | <span data-ttu-id="e8037-793">Valore</span><span class="sxs-lookup"><span data-stu-id="e8037-793">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e8037-794">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e8037-794">Minimum supported client</span></span><br/> | <span data-ttu-id="e8037-795">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="e8037-795">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="e8037-796">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e8037-796">Minimum supported server</span></span><br/> | <span data-ttu-id="e8037-797">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e8037-797">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e8037-798">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e8037-798">Header</span></span><br/>                   | <dl> <span data-ttu-id="e8037-799"><dt>WinError. h</dt></span><span class="sxs-lookup"><span data-stu-id="e8037-799"><dt>WinError.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e8037-800">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e8037-800">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8037-801">Codici di errore di sistema</span><span class="sxs-lookup"><span data-stu-id="e8037-801">System Error Codes</span></span>](system-error-codes.md)
</dt> </dl>

 

 




