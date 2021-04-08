---
title: Funzioni API Servizi Desktop remoto
description: Con Servizi Desktop remoto vengono utilizzate le funzioni seguenti.
ms.assetid: e99a86ee-af0e-46db-8dad-69703ca84fa0
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e94a2168f5ad4501b9725b72923c98ea97cc707c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727978"
---
# <a name="remote-desktop-services-api-functions"></a><span data-ttu-id="83980-103">Funzioni API Servizi Desktop remoto</span><span class="sxs-lookup"><span data-stu-id="83980-103">Remote Desktop Services API Functions</span></span>

<span data-ttu-id="83980-104">Con Servizi Desktop remoto vengono utilizzate le funzioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="83980-104">The following functions are used with Remote Desktop Services.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="83980-105">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="83980-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="83980-106">**ProcessIdToSessionId**</span><span class="sxs-lookup"><span data-stu-id="83980-106">**ProcessIdToSessionId**</span></span>](/windows/win32/api/processthreadsapi/nf-processthreadsapi-processidtosessionid)
</dt> <dd>

<span data-ttu-id="83980-107">Recupera la sessione di Servizi Desktop remoto associata a un processo specificato.</span><span class="sxs-lookup"><span data-stu-id="83980-107">Retrieves the Remote Desktop Services session associated with a specified process.</span></span>

</dd> <dt>

[<span data-ttu-id="83980-108">**TLSConnectToLsServer**</span><span class="sxs-lookup"><span data-stu-id="83980-108">**TLSConnectToLsServer**</span></span>](tlsconnecttolsserver.md)
</dt> <dd>

<span data-ttu-id="83980-109">Apre un handle per il server licenze Desktop remoto specificato.</span><span class="sxs-lookup"><span data-stu-id="83980-109">Opens a handle to the specified Remote Desktop license server.</span></span>

</dd> <dt>

[<span data-ttu-id="83980-110">**TLSDisconnectFromServer**</span><span class="sxs-lookup"><span data-stu-id="83980-110">**TLSDisconnectFromServer**</span></span>](tlsdisconnectfromserver.md)
</dt> <dd>

<span data-ttu-id="83980-111">Chiude un handle aperto per un server licenze Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="83980-111">Closes an open handle to a Remote Desktop license server.</span></span>

</dd> <dt>

[<span data-ttu-id="83980-112">**TLSGetServerCertificate**</span><span class="sxs-lookup"><span data-stu-id="83980-112">**TLSGetServerCertificate**</span></span>](tlsgetservercertificate.md)
</dt> <dd>

<span data-ttu-id="83980-113">Restituisce il certificato del server licenze Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="83980-113">Returns the certificate of the Remote Desktop license server.</span></span>

</dd> <dt>

[<span data-ttu-id="83980-114">**TLSKeyPackEnumBegin**</span><span class="sxs-lookup"><span data-stu-id="83980-114">**TLSKeyPackEnumBegin**</span></span>](tlskeypackenumbegin.md)
</dt> <dd>

<span data-ttu-id="83980-115">Inizia l'enumerazione tramite tutti i Key Pack installati in un server licenze Desktop remoto in base ai criteri di ricerca.</span><span class="sxs-lookup"><span data-stu-id="83980-115">Begins enumeration through all key packs that are installed on a Remote Desktop license server based on search criteria.</span></span>

</dd> <dt>

[<span data-ttu-id="83980-116">**TLSKeyPackEnumEnd**</span><span class="sxs-lookup"><span data-stu-id="83980-116">**TLSKeyPackEnumEnd**</span></span>](tlskeypackenumend.md)
</dt> <dd>

<span data-ttu-id="83980-117">Continua da una precedente chiamata alla funzione [**TLSKeyPackEnumBegin**](tlskeypackenumbegin.md) e termina l'enumerazione.</span><span class="sxs-lookup"><span data-stu-id="83980-117">Continues from a previous call to the [**TLSKeyPackEnumBegin**](tlskeypackenumbegin.md) function and terminates the enumeration.</span></span>

</dd> <dt>

[<span data-ttu-id="83980-118">**TLSKeyPackEnumNext**</span><span class="sxs-lookup"><span data-stu-id="83980-118">**TLSKeyPackEnumNext**</span></span>](tlskeypackenumnext.md)
</dt> <dd>

<span data-ttu-id="83980-119">Continua da una precedente chiamata alla funzione [**TLSKeyPackEnumBegin**](tlskeypackenumbegin.md) e restituisce il key pack successivo installato in un server licenze Desktop remoto corrispondente ai criteri di ricerca.</span><span class="sxs-lookup"><span data-stu-id="83980-119">Continues from a previous call to the [**TLSKeyPackEnumBegin**](tlskeypackenumbegin.md) function and returns the next key pack that is installed on a Remote Desktop license server that matches the search criteria.</span></span>

</dd> <dt>

[<span data-ttu-id="83980-120">**TLSLicenseEnumBegin**</span><span class="sxs-lookup"><span data-stu-id="83980-120">**TLSLicenseEnumBegin**</span></span>](tlslicenseenumbegin.md)
</dt> <dd>

<span data-ttu-id="83980-121">Inizia l'enumerazione delle licenze rilasciate dal server licenze Desktop remoto in base ai criteri di ricerca.</span><span class="sxs-lookup"><span data-stu-id="83980-121">Begins enumeration of licenses that are issued by the Remote Desktop license server based on search criteria.</span></span>

</dd> <dt>

[<span data-ttu-id="83980-122">**TLSLicenseEnumEnd**</span><span class="sxs-lookup"><span data-stu-id="83980-122">**TLSLicenseEnumEnd**</span></span>](tlslicenseenumend.md)
</dt> <dd>

<span data-ttu-id="83980-123">Continua da una precedente chiamata alla funzione [**TLSLicenseEnumBegin**](tlslicenseenumbegin.md) e termina l'enumerazione.</span><span class="sxs-lookup"><span data-stu-id="83980-123">Continues from a previous call to the [**TLSLicenseEnumBegin**](tlslicenseenumbegin.md) function and terminates the enumeration.</span></span>

</dd> <dt>

[<span data-ttu-id="83980-124">**TLSLicenseEnumNext**</span><span class="sxs-lookup"><span data-stu-id="83980-124">**TLSLicenseEnumNext**</span></span>](tlslicenseenumnext.md)
</dt> <dd>

<span data-ttu-id="83980-125">Continua da una precedente chiamata alla funzione [**TLSLicenseEnumBegin**](tlslicenseenumbegin.md) e restituisce la licenza successiva installata in un server licenze Desktop remoto corrispondente ai criteri di ricerca.</span><span class="sxs-lookup"><span data-stu-id="83980-125">Continues from a previous call to the [**TLSLicenseEnumBegin**](tlslicenseenumbegin.md) function and returns the next license that is installed on a Remote Desktop license server that matches the search criteria.</span></span>

</dd> <dt>

[<span data-ttu-id="83980-126">**VirtualChannelClose**</span><span class="sxs-lookup"><span data-stu-id="83980-126">**VirtualChannelClose**</span></span>](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelclose)
</dt> <dd>

<span data-ttu-id="83980-127">Chiude l'estremità client di un canale virtuale.</span><span class="sxs-lookup"><span data-stu-id="83980-127">Closes the client end of a virtual channel.</span></span>

</dd> <dt>

[<span data-ttu-id="83980-128">**VirtualChannelEntry**</span><span class="sxs-lookup"><span data-stu-id="83980-128">**VirtualChannelEntry**</span></span>](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelentry)
</dt> <dd>

<span data-ttu-id="83980-129">Un punto di ingresso definito dall'applicazione per la DLL sul lato client di un'applicazione che usa Servizi Desktop remoto canali virtuali.</span><span class="sxs-lookup"><span data-stu-id="83980-129">An application-defined entry point for the client-side DLL of an application that uses Remote Desktop Services virtual channels.</span></span>

</dd> <dt>

[<span data-ttu-id="83980-130">**VirtualChannelInit**</span><span class="sxs-lookup"><span data-stu-id="83980-130">**VirtualChannelInit**</span></span>](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelinit)
</dt> <dd>

<span data-ttu-id="83980-131">Inizializza un accesso della DLL client ai canali virtuali Servizi Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="83980-131">Initializes a client DLL's access to Remote Desktop Services virtual channels.</span></span>

</dd> <dt>

[<span data-ttu-id="83980-132">*VirtualChannelInitEvent*</span><span class="sxs-lookup"><span data-stu-id="83980-132">*VirtualChannelInitEvent*</span></span>](/windows/desktop/api/Cchannel/nc-cchannel-channel_init_event_fn)
</dt> <dd>

<span data-ttu-id="83980-133">Funzione di callback definita dall'applicazione che Servizi Desktop remoto chiama per notificare la DLL client degli eventi del canale virtuale.</span><span class="sxs-lookup"><span data-stu-id="83980-133">An application-defined callback function that Remote Desktop Services calls to notify the client DLL of virtual channel events.</span></span>

</dd> <dt>

[<span data-ttu-id="83980-134">**VirtualChannelOpen**</span><span class="sxs-lookup"><span data-stu-id="83980-134">**VirtualChannelOpen**</span></span>](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelopen)
</dt> <dd>

<span data-ttu-id="83980-135">Apre l'estremità client di un canale virtuale.</span><span class="sxs-lookup"><span data-stu-id="83980-135">Opens the client end of a virtual channel.</span></span>

</dd> <dt>

[<span data-ttu-id="83980-136">*VirtualChannelOpenEvent*</span><span class="sxs-lookup"><span data-stu-id="83980-136">*VirtualChannelOpenEvent*</span></span>](/windows/desktop/api/Cchannel/nc-cchannel-channel_open_event_fn)
</dt> <dd>

<span data-ttu-id="83980-137">Funzione di callback definita dall'applicazione che Servizi Desktop remoto chiama per notificare alla DLL del client gli eventi per un canale virtuale specifico.</span><span class="sxs-lookup"><span data-stu-id="83980-137">An application-defined callback function that Remote Desktop Services calls to notify the client DLL of events for a specific virtual channel.</span></span>

</dd> <dt>

[<span data-ttu-id="83980-138">**VirtualChannelWrite**</span><span class="sxs-lookup"><span data-stu-id="83980-138">**VirtualChannelWrite**</span></span>](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelwrite)
</dt> <dd>

<span data-ttu-id="83980-139">Invia i dati dall'estremità client di un canale virtuale a un'applicazione partner sul lato server.</span><span class="sxs-lookup"><span data-stu-id="83980-139">Sends data from the client end of a virtual channel to a partner application on the server end.</span></span>

</dd> <dt>

[<span data-ttu-id="83980-140">**WTSCloseServer**</span><span class="sxs-lookup"><span data-stu-id="83980-140">**WTSCloseServer**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtscloseserver)
</dt> <dd>

<span data-ttu-id="83980-141">Chiude un handle aperto per un server di host sessione Desktop remoto (host sessione Desktop remoto).</span><span class="sxs-lookup"><span data-stu-id="83980-141">Closes an open handle to a Remote Desktop Session Host (RD Session Host) server.</span></span>

</dd> <dt>

[<span data-ttu-id="83980-142">**WTSConnectSession**</span><span class="sxs-lookup"><span data-stu-id="83980-142">**WTSConnectSession**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsconnectsessiona)
</dt> <dd>

<span data-ttu-id="83980-143">Connette una sessione di Servizi Desktop remoto a una sessione esistente nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="83980-143">Connects a Remote Desktop Services session to an existing session on the local computer.</span></span>

</dd> <dt>

[<span data-ttu-id="83980-144">**WTSCreateListener**</span><span class="sxs-lookup"><span data-stu-id="83980-144">**WTSCreateListener**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtscreatelistenera)
</dt> <dd>

<span data-ttu-id="83980-145">Crea un nuovo listener di Servizi Desktop remoto o configura un listener esistente.</span><span class="sxs-lookup"><span data-stu-id="83980-145">Creates a new Remote Desktop Services listener or configures an existing listener.</span></span>

</dd> <dt>

[<span data-ttu-id="83980-146">**WTSDisconnectSession**</span><span class="sxs-lookup"><span data-stu-id="83980-146">**WTSDisconnectSession**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsdisconnectsession)
</dt> <dd>

<span data-ttu-id="83980-147">Disconnette l'utente connesso dalla sessione di Servizi Desktop remoto specificata senza chiudere la sessione.</span><span class="sxs-lookup"><span data-stu-id="83980-147">Disconnects the logged-on user from the specified Remote Desktop Services session without closing the session.</span></span>

</dd> <dt>

[<span data-ttu-id="83980-148">**WTSEnableChildSessions**</span><span class="sxs-lookup"><span data-stu-id="83980-148">**WTSEnableChildSessions**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenablechildsessions)
</dt> <dd>

<span data-ttu-id="83980-149">Abilita o Disabilita le [sessioni figlio](child-sessions.md).</span><span class="sxs-lookup"><span data-stu-id="83980-149">Enables or disables [Child Sessions](child-sessions.md).</span></span>

</dd> <dt>

[<span data-ttu-id="83980-150">**WTSEnumerateListeners**</span><span class="sxs-lookup"><span data-stu-id="83980-150">**WTSEnumerateListeners**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenumeratelistenersa)
</dt> <dd>

<span data-ttu-id="83980-151">Enumera tutti i listener di Servizi Desktop remoto in un server Host sessione Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="83980-151">Enumerates all the Remote Desktop Services listeners on a RD Session Host server.</span></span>

</dd> <dt>

[<span data-ttu-id="83980-152">**WTSEnumerateProcesses**</span><span class="sxs-lookup"><span data-stu-id="83980-152">**WTSEnumerateProcesses**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenumerateprocessesa)
</dt> <dd>

<span data-ttu-id="83980-153">Recupera le informazioni sui processi attivi in un server Host sessione Desktop remoto specificato.</span><span class="sxs-lookup"><span data-stu-id="83980-153">Retrieves information about the active processes on a specified RD Session Host server.</span></span>

</dd> <dt>

[<span data-ttu-id="83980-154">**WTSEnumerateProcessesEx**</span><span class="sxs-lookup"><span data-stu-id="83980-154">**WTSEnumerateProcessesEx**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenumerateprocessesexa)
</dt> <dd>

<span data-ttu-id="83980-155">Recupera le informazioni sui processi attivi nel server Host sessione Desktop remoto specificato o nel server Host di virtualizzazione Desktop remoto (host di virtualizzazione Desktop remoto).</span><span class="sxs-lookup"><span data-stu-id="83980-155">Retrieves information about the active processes on the specified RD Session Host server or Remote Desktop Virtualization Host (RD Virtualization Host) server.</span></span>

</dd> <dt>

[<span data-ttu-id="83980-156">**WTSEnumerateServers**</span><span class="sxs-lookup"><span data-stu-id="83980-156">**WTSEnumerateServers**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenumerateserversa)
</dt> <dd>

<span data-ttu-id="83980-157">Restituisce un elenco di tutti i server Host sessione Desktop remoto all'interno del dominio specificato.</span><span class="sxs-lookup"><span data-stu-id="83980-157">Returns a list of all RD Session Host servers within the specified domain.</span></span>

</dd> <dt>

[<span data-ttu-id="83980-158">**WTSEnumerateSessions**</span><span class="sxs-lookup"><span data-stu-id="83980-158">**WTSEnumerateSessions**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenumeratesessionsa)
</dt> <dd>

<span data-ttu-id="83980-159">Recupera un elenco di sessioni in un server Host sessione Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="83980-159">Retrieves a list of sessions on a RD Session Host server.</span></span>

</dd> <dt>

[<span data-ttu-id="83980-160">**WTSEnumerateSessionsEx**</span><span class="sxs-lookup"><span data-stu-id="83980-160">**WTSEnumerateSessionsEx**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenumeratesessionsexa)
</dt> <dd>

<span data-ttu-id="83980-161">Recupera un elenco di sessioni in un server Host sessione Desktop remoto o in un server host di virtualizzazione Desktop remoto specificato.</span><span class="sxs-lookup"><span data-stu-id="83980-161">Retrieves a list of sessions on a specified RD Session Host server or RD Virtualization Host server.</span></span>

</dd> <dt>

[<span data-ttu-id="83980-162">**WTSFreeMemory**</span><span class="sxs-lookup"><span data-stu-id="83980-162">**WTSFreeMemory**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsfreememory)
</dt> <dd>

<span data-ttu-id="83980-163">Libera la memoria allocata da una funzione Servizi Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="83980-163">Frees memory allocated by a Remote Desktop Services function.</span></span>

</dd> <dt>

[<span data-ttu-id="83980-164">**WTSFreeMemoryEx**</span><span class="sxs-lookup"><span data-stu-id="83980-164">**WTSFreeMemoryEx**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsfreememoryexa)
</dt> <dd>

<span data-ttu-id="83980-165">Libera la memoria che contiene le strutture delle informazioni di [**sessione WTS o WTS \_ \_ \_ 1**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_session_info_1a) allocate da una funzione Servizi Desktop remoto. [**\_ \_ \_**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_process_info_exa)</span><span class="sxs-lookup"><span data-stu-id="83980-165">Frees memory that contains [**WTS\_PROCESS\_INFO\_EX**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_process_info_exa) or [**WTS\_SESSION\_INFO\_1**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_session_info_1a) structures allocated by a Remote Desktop Services function.</span></span>

</dd> <dt>

[<span data-ttu-id="83980-166">**WTSGetActiveConsoleSessionId**</span><span class="sxs-lookup"><span data-stu-id="83980-166">**WTSGetActiveConsoleSessionId**</span></span>](/windows/desktop/api/Winbase/nf-winbase-wtsgetactiveconsolesessionid)
</dt> <dd>

<span data-ttu-id="83980-167">Recupera l'identificatore di sessione della sessione della console.</span><span class="sxs-lookup"><span data-stu-id="83980-167">Retrieves the session identifier of the console session.</span></span>

</dd> <dt>

[<span data-ttu-id="83980-168">**WTSGetChildSessionId**</span><span class="sxs-lookup"><span data-stu-id="83980-168">**WTSGetChildSessionId**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsgetchildsessionid)
</dt> <dd>

<span data-ttu-id="83980-169">Recupera l'identificatore della sessione figlio, se presente.</span><span class="sxs-lookup"><span data-stu-id="83980-169">Retrieves the child session identifier, if present.</span></span>

</dd> <dt>

[<span data-ttu-id="83980-170">**WTSGetListenerSecurity**</span><span class="sxs-lookup"><span data-stu-id="83980-170">**WTSGetListenerSecurity**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsgetlistenersecuritya)
</dt> <dd>

<span data-ttu-id="83980-171">Recupera il descrittore di sicurezza di un listener di Servizi Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="83980-171">Retrieves the security descriptor of a Remote Desktop Services listener.</span></span>

</dd> <dt>

[<span data-ttu-id="83980-172">**WTSIsChildSessionsEnabled**</span><span class="sxs-lookup"><span data-stu-id="83980-172">**WTSIsChildSessionsEnabled**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsischildsessionsenabled)
</dt> <dd>

<span data-ttu-id="83980-173">Determina se le sessioni figlio sono abilitate.</span><span class="sxs-lookup"><span data-stu-id="83980-173">Determines whether child sessions are enabled.</span></span>

</dd> <dt>

[<span data-ttu-id="83980-174">**WTSLogoffSession**</span><span class="sxs-lookup"><span data-stu-id="83980-174">**WTSLogoffSession**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtslogoffsession)
</dt> <dd>

<span data-ttu-id="83980-175">Disconnette una sessione di Servizi Desktop remoto specificata.</span><span class="sxs-lookup"><span data-stu-id="83980-175">Logs off a specified Remote Desktop Services session.</span></span>

</dd> <dt>

[<span data-ttu-id="83980-176">**WTSOpenServer**</span><span class="sxs-lookup"><span data-stu-id="83980-176">**WTSOpenServer**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsopenservera)
</dt> <dd>

<span data-ttu-id="83980-177">Apre un handle per il server Host sessione Desktop remoto specificato.</span><span class="sxs-lookup"><span data-stu-id="83980-177">Opens a handle to the specified RD Session Host server.</span></span>

</dd> <dt>

[<span data-ttu-id="83980-178">**WTSOpenServerEx**</span><span class="sxs-lookup"><span data-stu-id="83980-178">**WTSOpenServerEx**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsopenserverexa)
</dt> <dd>

<span data-ttu-id="83980-179">Apre un handle per il server Host sessione Desktop remoto o il server host di virtualizzazione Desktop remoto specificato.</span><span class="sxs-lookup"><span data-stu-id="83980-179">Opens a handle to the specified RD Session Host server or RD Virtualization Host server.</span></span>

</dd> <dt>

[<span data-ttu-id="83980-180">**WTSQueryListenerConfig**</span><span class="sxs-lookup"><span data-stu-id="83980-180">**WTSQueryListenerConfig**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsquerylistenerconfiga)
</dt> <dd>

<span data-ttu-id="83980-181">Recupera le informazioni di configurazione per un listener di Servizi Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="83980-181">Retrieves configuration information for a Remote Desktop Services listener.</span></span>

</dd> <dt>

[<span data-ttu-id="83980-182">**WTSQuerySessionInformation**</span><span class="sxs-lookup"><span data-stu-id="83980-182">**WTSQuerySessionInformation**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsquerysessioninformationa)
</dt> <dd>

<span data-ttu-id="83980-183">Recupera le informazioni sulla sessione per la sessione specificata nel server Host sessione Desktop remoto specificato.</span><span class="sxs-lookup"><span data-stu-id="83980-183">Retrieves session information for the specified session on the specified RD Session Host server.</span></span>

</dd> <dt>

[<span data-ttu-id="83980-184">**WTSQueryUserConfig**</span><span class="sxs-lookup"><span data-stu-id="83980-184">**WTSQueryUserConfig**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsqueryuserconfiga)
</dt> <dd>

<span data-ttu-id="83980-185">Recupera le informazioni di configurazione per l'utente specificato nel controller di dominio o nel server Host sessione Desktop remoto specificati.</span><span class="sxs-lookup"><span data-stu-id="83980-185">Retrieves configuration information for the specified user on the specified domain controller or RD Session Host server.</span></span>

</dd> <dt>

[<span data-ttu-id="83980-186">**WTSQueryUserToken**</span><span class="sxs-lookup"><span data-stu-id="83980-186">**WTSQueryUserToken**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsqueryusertoken)
</dt> <dd>

<span data-ttu-id="83980-187">Ottiene il token di accesso primario dell'utente connesso specificato dall'ID sessione.</span><span class="sxs-lookup"><span data-stu-id="83980-187">Obtains the primary access token of the logged-on user specified by the session ID.</span></span>

</dd> <dt>

[<span data-ttu-id="83980-188">**WTSRegisterSessionNotification**</span><span class="sxs-lookup"><span data-stu-id="83980-188">**WTSRegisterSessionNotification**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsregistersessionnotification)
</dt> <dd>

<span data-ttu-id="83980-189">Registra la finestra specificata per ricevere le notifiche di modifica della sessione.</span><span class="sxs-lookup"><span data-stu-id="83980-189">Registers the specified window to receive session change notifications.</span></span>

</dd> <dt>

[<span data-ttu-id="83980-190">**WTSRegisterSessionNotificationEx**</span><span class="sxs-lookup"><span data-stu-id="83980-190">**WTSRegisterSessionNotificationEx**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsregistersessionnotificationex)
</dt> <dd>

<span data-ttu-id="83980-191">Registra la finestra specificata per ricevere le notifiche di modifica della sessione.</span><span class="sxs-lookup"><span data-stu-id="83980-191">Registers the specified window to receive session change notifications.</span></span>

</dd> <dt>

[<span data-ttu-id="83980-192">**WTSSendMessage**</span><span class="sxs-lookup"><span data-stu-id="83980-192">**WTSSendMessage**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtssendmessagea)
</dt> <dd>

<span data-ttu-id="83980-193">Visualizza una finestra di messaggio sul desktop client di una sessione di Servizi Desktop remoto specificata.</span><span class="sxs-lookup"><span data-stu-id="83980-193">Displays a message box on the client desktop of a specified Remote Desktop Services session.</span></span>

</dd> <dt>

[<span data-ttu-id="83980-194">**WTSSetListenerSecurity**</span><span class="sxs-lookup"><span data-stu-id="83980-194">**WTSSetListenerSecurity**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtssetlistenersecuritya)
</dt> <dd>

<span data-ttu-id="83980-195">Configura il descrittore di sicurezza di un listener di Servizi Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="83980-195">Configures the security descriptor of a Remote Desktop Services listener.</span></span>

</dd> <dt>

[<span data-ttu-id="83980-196">**WTSSetUserConfig**</span><span class="sxs-lookup"><span data-stu-id="83980-196">**WTSSetUserConfig**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtssetuserconfiga)
</dt> <dd>

<span data-ttu-id="83980-197">Modifica le informazioni di configurazione per l'utente specificato nel server Host sessione Desktop remoto o nel controller di dominio specificato.</span><span class="sxs-lookup"><span data-stu-id="83980-197">Modifies configuration information for the specified user on the specified domain controller or RD Session Host server.</span></span>

</dd> <dt>

[<span data-ttu-id="83980-198">**WTSShutdownSystem**</span><span class="sxs-lookup"><span data-stu-id="83980-198">**WTSShutdownSystem**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsshutdownsystem)
</dt> <dd>

<span data-ttu-id="83980-199">Arresta (e, facoltativamente, riavvia) il server Host sessione Desktop remoto specificato.</span><span class="sxs-lookup"><span data-stu-id="83980-199">Shuts down (and optionally restarts) the specified RD Session Host server.</span></span>

</dd> <dt>

[<span data-ttu-id="83980-200">**WTSStartRemoteControlSession**</span><span class="sxs-lookup"><span data-stu-id="83980-200">**WTSStartRemoteControlSession**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsstartremotecontrolsessiona)
</dt> <dd>

<span data-ttu-id="83980-201">Avvia il controllo remoto di un'altra sessione di Servizi Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="83980-201">Starts the remote control of another Remote Desktop Services session.</span></span> <span data-ttu-id="83980-202">È necessario chiamare questa funzione da una sessione remota.</span><span class="sxs-lookup"><span data-stu-id="83980-202">You must call this function from a remote session.</span></span>

</dd> <dt>

[<span data-ttu-id="83980-203">**WTSStopRemoteControlSession**</span><span class="sxs-lookup"><span data-stu-id="83980-203">**WTSStopRemoteControlSession**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsstopremotecontrolsession)
</dt> <dd>

<span data-ttu-id="83980-204">Arresta una sessione di controllo remoto.</span><span class="sxs-lookup"><span data-stu-id="83980-204">Stops a remote control session.</span></span>

</dd> <dt>

[<span data-ttu-id="83980-205">**WTSTerminateProcess**</span><span class="sxs-lookup"><span data-stu-id="83980-205">**WTSTerminateProcess**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsterminateprocess)
</dt> <dd>

<span data-ttu-id="83980-206">Termina il processo specificato nel server Host sessione Desktop remoto specificato.</span><span class="sxs-lookup"><span data-stu-id="83980-206">Terminates the specified process on the specified RD Session Host server.</span></span>

</dd> <dt>

[<span data-ttu-id="83980-207">**WTSUnRegisterSessionNotification**</span><span class="sxs-lookup"><span data-stu-id="83980-207">**WTSUnRegisterSessionNotification**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsunregistersessionnotification)
</dt> <dd>

<span data-ttu-id="83980-208">Annulla la registrazione della finestra specificata in modo che non riceva ulteriori notifiche di modifica della sessione.</span><span class="sxs-lookup"><span data-stu-id="83980-208">Unregisters the specified window so that it receives no further session change notifications.</span></span>

</dd> <dt>

[<span data-ttu-id="83980-209">**WTSUnRegisterSessionNotificationEx**</span><span class="sxs-lookup"><span data-stu-id="83980-209">**WTSUnRegisterSessionNotificationEx**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsunregistersessionnotificationex)
</dt> <dd>

<span data-ttu-id="83980-210">Annulla la registrazione della finestra specificata in modo che non riceva ulteriori notifiche di modifica della sessione.</span><span class="sxs-lookup"><span data-stu-id="83980-210">Unregisters the specified window so that it receives no further session change notifications.</span></span>

</dd> <dt>

[<span data-ttu-id="83980-211">**WTSVirtualChannelClose**</span><span class="sxs-lookup"><span data-stu-id="83980-211">**WTSVirtualChannelClose**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelclose)
</dt> <dd>

<span data-ttu-id="83980-212">Chiude un handle di canale virtuale aperto.</span><span class="sxs-lookup"><span data-stu-id="83980-212">Closes an open virtual channel handle.</span></span>

</dd> <dt>

[<span data-ttu-id="83980-213">**WTSVirtualChannelOpen**</span><span class="sxs-lookup"><span data-stu-id="83980-213">**WTSVirtualChannelOpen**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelopen)
</dt> <dd>

<span data-ttu-id="83980-214">Apre un handle per la fine del server di un canale virtuale specificato.</span><span class="sxs-lookup"><span data-stu-id="83980-214">Opens a handle to the server end of a specified virtual channel.</span></span>

</dd> <dt>

[<span data-ttu-id="83980-215">**WTSVirtualChannelOpenEx**</span><span class="sxs-lookup"><span data-stu-id="83980-215">**WTSVirtualChannelOpenEx**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelopenex)
</dt> <dd>

<span data-ttu-id="83980-216">Crea un canale virtuale in modo analogo a [**WTSVirtualChannelOpen**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelopen).</span><span class="sxs-lookup"><span data-stu-id="83980-216">Creates a virtual channel in a manner similar to [**WTSVirtualChannelOpen**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelopen).</span></span>

</dd> <dt>

[<span data-ttu-id="83980-217">**WTSVirtualChannelPurgeInput**</span><span class="sxs-lookup"><span data-stu-id="83980-217">**WTSVirtualChannelPurgeInput**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelpurgeinput)
</dt> <dd>

<span data-ttu-id="83980-218">Elimina tutti i dati di input in coda inviati dal client al server su un canale virtuale specificato.</span><span class="sxs-lookup"><span data-stu-id="83980-218">Deletes all queued input data sent from the client to the server on a specified virtual channel.</span></span>

</dd> <dt>

[<span data-ttu-id="83980-219">**WTSVirtualChannelPurgeOutput**</span><span class="sxs-lookup"><span data-stu-id="83980-219">**WTSVirtualChannelPurgeOutput**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelpurgeoutput)
</dt> <dd>

<span data-ttu-id="83980-220">Elimina tutti i dati di output in coda inviati dal server al client su un canale virtuale specificato.</span><span class="sxs-lookup"><span data-stu-id="83980-220">Deletes all queued output data sent from the server to the client on a specified virtual channel.</span></span>

</dd> <dt>

[<span data-ttu-id="83980-221">**WTSVirtualChannelQuery**</span><span class="sxs-lookup"><span data-stu-id="83980-221">**WTSVirtualChannelQuery**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelquery)
</dt> <dd>

<span data-ttu-id="83980-222">Restituisce informazioni su un canale virtuale specificato.</span><span class="sxs-lookup"><span data-stu-id="83980-222">Returns information about a specified virtual channel.</span></span>

</dd> <dt>

[<span data-ttu-id="83980-223">**WTSVirtualChannelRead**</span><span class="sxs-lookup"><span data-stu-id="83980-223">**WTSVirtualChannelRead**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelread)
</dt> <dd>

<span data-ttu-id="83980-224">Legge i dati dall'estremità server di un canale virtuale.</span><span class="sxs-lookup"><span data-stu-id="83980-224">Reads data from the server end of a virtual channel.</span></span>

</dd> <dt>

[<span data-ttu-id="83980-225">**WTSVirtualChannelWrite**</span><span class="sxs-lookup"><span data-stu-id="83980-225">**WTSVirtualChannelWrite**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelwrite)
</dt> <dd>

<span data-ttu-id="83980-226">Scrive i dati nell'entità finale del server di un canale virtuale.</span><span class="sxs-lookup"><span data-stu-id="83980-226">Writes data to the server end of a virtual channel.</span></span>

</dd> <dt>

[<span data-ttu-id="83980-227">**WTSWaitSystemEvent**</span><span class="sxs-lookup"><span data-stu-id="83980-227">**WTSWaitSystemEvent**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtswaitsystemevent)
</dt> <dd>

<span data-ttu-id="83980-228">Attende un evento Servizi Desktop remoto prima di tornare al chiamante.</span><span class="sxs-lookup"><span data-stu-id="83980-228">Waits for a Remote Desktop Services event before returning to the caller.</span></span>

</dd> </dl>

 

 