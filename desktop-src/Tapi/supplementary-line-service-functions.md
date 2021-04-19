---
description: Le funzioni di servizio linea supplementare sono elencate per categoria negli argomenti seguenti.
ms.assetid: d4338b3c-cd84-4abb-b74e-9df895c8355b
title: Funzioni di servizio linea supplementare
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21a29831369fd6b886d57cfae075b5b8bf7a83b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311869"
---
# <a name="supplementary-line-service-functions"></a><span data-ttu-id="74aca-103">Funzioni di servizio linea supplementare</span><span class="sxs-lookup"><span data-stu-id="74aca-103">Supplementary Line Service Functions</span></span>

<span data-ttu-id="74aca-104">Le funzioni di servizio linea supplementare sono elencate per categoria negli argomenti seguenti.</span><span class="sxs-lookup"><span data-stu-id="74aca-104">The supplementary line service functions are listed by category in the following topics.</span></span> <span data-ttu-id="74aca-105">Una funzione viene identificata come [*asincrona*](a-tapgloss.md) se indicherà il completamento di un messaggio di risposta all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="74aca-105">A function is identified as [*asynchronous*](a-tapgloss.md) if it will indicate completion in a REPLY message to the application.</span></span> <span data-ttu-id="74aca-106">Se la funzione restituisce sempre il risultato all'applicazione immediatamente, la funzione viene considerata [*sincrona*](s-tapgloss.md).</span><span class="sxs-lookup"><span data-stu-id="74aca-106">If the function always returns its result to the application immediately, the function is considered [*synchronous*](s-tapgloss.md).</span></span>

<span data-ttu-id="74aca-107">Di seguito è riportato un raggruppamento funzionale delle funzioni di servizio di linea supplementare:</span><span class="sxs-lookup"><span data-stu-id="74aca-107">Following is a functional grouping of the supplementary line service functions:</span></span>

-   [<span data-ttu-id="74aca-108">Agenti</span><span class="sxs-lookup"><span data-stu-id="74aca-108">Agents</span></span>](#agents)
-   [<span data-ttu-id="74aca-109">Priorità applicazione</span><span class="sxs-lookup"><span data-stu-id="74aca-109">Application priority</span></span>](#application-priority)
-   [<span data-ttu-id="74aca-110">Modalità di Bearer e frequenza</span><span class="sxs-lookup"><span data-stu-id="74aca-110">Bearer mode and rate</span></span>](#bearer-mode-and-rate)
-   [<span data-ttu-id="74aca-111">Chiama Accept e reindirizza</span><span class="sxs-lookup"><span data-stu-id="74aca-111">Call accept and redirect</span></span>](#call-accept-and-redirect)
-   [<span data-ttu-id="74aca-112">Completamento chiamata</span><span class="sxs-lookup"><span data-stu-id="74aca-112">Call completion</span></span>](#call-completion)
-   [<span data-ttu-id="74aca-113">Conference Call</span><span class="sxs-lookup"><span data-stu-id="74aca-113">Call conference</span></span>](#call-conference)
-   [<span data-ttu-id="74aca-114">Invio di chiamate</span><span class="sxs-lookup"><span data-stu-id="74aca-114">Call forwarding</span></span>](#call-forwarding)
-   [<span data-ttu-id="74aca-115">Attesa chiamata</span><span class="sxs-lookup"><span data-stu-id="74aca-115">Call hold</span></span>](#call-hold)
-   [<span data-ttu-id="74aca-116">Call Park</span><span class="sxs-lookup"><span data-stu-id="74aca-116">Call park</span></span>](#call-park)
-   [<span data-ttu-id="74aca-117">Pickup chiamata</span><span class="sxs-lookup"><span data-stu-id="74aca-117">Call pickup</span></span>](#call-pickup)
-   [<span data-ttu-id="74aca-118">Rifiuto chiamata</span><span class="sxs-lookup"><span data-stu-id="74aca-118">Call reject</span></span>](#call-reject)
-   [<span data-ttu-id="74aca-119">Trasferimento chiamate</span><span class="sxs-lookup"><span data-stu-id="74aca-119">Call transfer</span></span>](#call-transfer)
-   [<span data-ttu-id="74aca-120">Monitoraggio e raccolta dei numeri</span><span class="sxs-lookup"><span data-stu-id="74aca-120">Digit monitoring and gathering</span></span>](#digit-monitoring-and-gathering)
-   [<span data-ttu-id="74aca-121">Generazione di cifre e toni inband</span><span class="sxs-lookup"><span data-stu-id="74aca-121">Generating inband digits and tones</span></span>](#generating-inband-digits-and-tones)
-   [<span data-ttu-id="74aca-122">Esecuzione di chiamate</span><span class="sxs-lookup"><span data-stu-id="74aca-122">Making calls</span></span>](basic-telephony-services-reference.md)
-   [<span data-ttu-id="74aca-123">Controllo multimediale</span><span class="sxs-lookup"><span data-stu-id="74aca-123">Media control</span></span>](#media-control)
-   [<span data-ttu-id="74aca-124">Monitoraggio dei supporti</span><span class="sxs-lookup"><span data-stu-id="74aca-124">Media monitoring</span></span>](#media-monitoring)
-   [<span data-ttu-id="74aca-125">Proxy</span><span class="sxs-lookup"><span data-stu-id="74aca-125">Proxies</span></span>](#proxies)
-   [<span data-ttu-id="74aca-126">QoS (Quality of Service)</span><span class="sxs-lookup"><span data-stu-id="74aca-126">Quality of Service</span></span>](#quality-of-service)
-   [<span data-ttu-id="74aca-127">Invio di informazioni a un'entità remota</span><span class="sxs-lookup"><span data-stu-id="74aca-127">Sending information to remote party</span></span>](#sending-information-to-remote-party)
-   [<span data-ttu-id="74aca-128">Gestione provider di servizi</span><span class="sxs-lookup"><span data-stu-id="74aca-128">Service provider management</span></span>](#service-provider-management)
-   [<span data-ttu-id="74aca-129">Impostazione di un terminale per le conversazioni telefoniche</span><span class="sxs-lookup"><span data-stu-id="74aca-129">Setting a terminal for phone conversations</span></span>](#setting-a-terminal-for-phone-conversations)
-   [<span data-ttu-id="74aca-130">Monitoraggio del tono</span><span class="sxs-lookup"><span data-stu-id="74aca-130">Tone monitoring</span></span>](#tone-monitoring)

<span data-ttu-id="74aca-131">Sono disponibili anche [varie](#miscellaneous) funzioni di servizio di linea supplementari.</span><span class="sxs-lookup"><span data-stu-id="74aca-131">There are also [miscellaneous](#miscellaneous) supplementary line service functions.</span></span>

## <a name="bearer-mode-and-rate"></a><span data-ttu-id="74aca-132">Modalità di Bearer e frequenza</span><span class="sxs-lookup"><span data-stu-id="74aca-132">Bearer Mode and Rate</span></span>



| <span data-ttu-id="74aca-133">Funzione</span><span class="sxs-lookup"><span data-stu-id="74aca-133">Function</span></span>                                       | <span data-ttu-id="74aca-134">Descrizione</span><span class="sxs-lookup"><span data-stu-id="74aca-134">Description</span></span>                                                                |
|------------------------------------------------|----------------------------------------------------------------------------|
| [<span data-ttu-id="74aca-135">**lineSetCallParams**</span><span class="sxs-lookup"><span data-stu-id="74aca-135">**lineSetCallParams**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetcallparams) | <span data-ttu-id="74aca-136">Richiede una modifica nei parametri di chiamata di una chiamata esistente.</span><span class="sxs-lookup"><span data-stu-id="74aca-136">Requests a change in the call parameters of an existing call.</span></span> <span data-ttu-id="74aca-137">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="74aca-137">Synchronous.</span></span> |



 

## <a name="media-monitoring"></a><span data-ttu-id="74aca-138">Monitoraggio dei supporti</span><span class="sxs-lookup"><span data-stu-id="74aca-138">Media Monitoring</span></span>



| <span data-ttu-id="74aca-139">Funzione</span><span class="sxs-lookup"><span data-stu-id="74aca-139">Function</span></span>                                     | <span data-ttu-id="74aca-140">Descrizione</span><span class="sxs-lookup"><span data-stu-id="74aca-140">Description</span></span>                                                                   |
|----------------------------------------------|-------------------------------------------------------------------------------|
| [<span data-ttu-id="74aca-141">**lineMonitorMedia**</span><span class="sxs-lookup"><span data-stu-id="74aca-141">**lineMonitorMedia**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linemonitormedia) | <span data-ttu-id="74aca-142">Abilita o Disabilita la notifica in modalità supporto per una chiamata specificata.</span><span class="sxs-lookup"><span data-stu-id="74aca-142">Enables or disables media mode notification on a specified call.</span></span> <span data-ttu-id="74aca-143">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="74aca-143">Synchronous.</span></span> |



 

## <a name="digit-monitoring-and-gathering"></a><span data-ttu-id="74aca-144">Monitoraggio e raccolta dei numeri</span><span class="sxs-lookup"><span data-stu-id="74aca-144">Digit Monitoring and Gathering</span></span>



| <span data-ttu-id="74aca-145">Funzione</span><span class="sxs-lookup"><span data-stu-id="74aca-145">Function</span></span>                                       | <span data-ttu-id="74aca-146">Descrizione</span><span class="sxs-lookup"><span data-stu-id="74aca-146">Description</span></span>                                                                        |
|------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="74aca-147">**lineMonitorDigits**</span><span class="sxs-lookup"><span data-stu-id="74aca-147">**lineMonitorDigits**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linemonitordigits) | <span data-ttu-id="74aca-148">Abilita o Disabilita la notifica di rilevamento digit per una chiamata specificata.</span><span class="sxs-lookup"><span data-stu-id="74aca-148">Enables or disables digit detection notification on a specified call.</span></span> <span data-ttu-id="74aca-149">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="74aca-149">Synchronous.</span></span> |
| [<span data-ttu-id="74aca-150">**lineGatherDigits**</span><span class="sxs-lookup"><span data-stu-id="74aca-150">**lineGatherDigits**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegatherdigits)   | <span data-ttu-id="74aca-151">Esegue la raccolta memorizzata nel buffer di cifre in una chiamata.</span><span class="sxs-lookup"><span data-stu-id="74aca-151">Performs the buffered gathering of digits on a call.</span></span> <span data-ttu-id="74aca-152">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="74aca-152">Synchronous.</span></span>                  |



 

## <a name="tone-monitoring"></a><span data-ttu-id="74aca-153">Monitoraggio del tono</span><span class="sxs-lookup"><span data-stu-id="74aca-153">Tone Monitoring</span></span>



| <span data-ttu-id="74aca-154">Funzione</span><span class="sxs-lookup"><span data-stu-id="74aca-154">Function</span></span>                                     | <span data-ttu-id="74aca-155">Descrizione</span><span class="sxs-lookup"><span data-stu-id="74aca-155">Description</span></span>                                                       |
|----------------------------------------------|-------------------------------------------------------------------|
| [<span data-ttu-id="74aca-156">**lineMonitorTones**</span><span class="sxs-lookup"><span data-stu-id="74aca-156">**lineMonitorTones**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linemonitortones) | <span data-ttu-id="74aca-157">Specifica i toni da rilevare in una chiamata specificata.</span><span class="sxs-lookup"><span data-stu-id="74aca-157">Specifies which tones to detect on a specified call.</span></span> <span data-ttu-id="74aca-158">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="74aca-158">Synchronous.</span></span> |



 

## <a name="media-control"></a><span data-ttu-id="74aca-159">Controllo multimediale</span><span class="sxs-lookup"><span data-stu-id="74aca-159">Media Control</span></span>



| <span data-ttu-id="74aca-160">Funzione</span><span class="sxs-lookup"><span data-stu-id="74aca-160">Function</span></span>                                           | <span data-ttu-id="74aca-161">Descrizione</span><span class="sxs-lookup"><span data-stu-id="74aca-161">Description</span></span>                                                                                                          |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="74aca-162">**lineSetMediaControl**</span><span class="sxs-lookup"><span data-stu-id="74aca-162">**lineSetMediaControl**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetmediacontrol) | <span data-ttu-id="74aca-163">Imposta un flusso multimediale della chiamata per il controllo multimediale.</span><span class="sxs-lookup"><span data-stu-id="74aca-163">Sets up a call's media stream for media control.</span></span> <span data-ttu-id="74aca-164">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="74aca-164">Synchronous.</span></span>                                                        |
| [<span data-ttu-id="74aca-165">**lineSetMediaMode**</span><span class="sxs-lookup"><span data-stu-id="74aca-165">**lineSetMediaMode**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetmediamode)       | <span data-ttu-id="74aca-166">Imposta la modalità multimediale della chiamata specificata nella relativa struttura [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) .</span><span class="sxs-lookup"><span data-stu-id="74aca-166">Sets the media mode(s) of the specified call in its [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) structure.</span></span> <span data-ttu-id="74aca-167">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="74aca-167">Synchronous.</span></span> |



 

## <a name="generating-inband-digits-and-tones"></a><span data-ttu-id="74aca-168">Generazione di cifre e toni inband</span><span class="sxs-lookup"><span data-stu-id="74aca-168">Generating Inband Digits and Tones</span></span>



| <span data-ttu-id="74aca-169">Funzione</span><span class="sxs-lookup"><span data-stu-id="74aca-169">Function</span></span>                                         | <span data-ttu-id="74aca-170">Descrizione</span><span class="sxs-lookup"><span data-stu-id="74aca-170">Description</span></span>                                                   |
|--------------------------------------------------|---------------------------------------------------------------|
| [<span data-ttu-id="74aca-171">**lineGenerateDigits**</span><span class="sxs-lookup"><span data-stu-id="74aca-171">**lineGenerateDigits**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegeneratedigits) | <span data-ttu-id="74aca-172">Genera cifre inband in una chiamata.</span><span class="sxs-lookup"><span data-stu-id="74aca-172">Generates inband digits on a call.</span></span> <span data-ttu-id="74aca-173">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="74aca-173">Synchronous.</span></span>               |
| [<span data-ttu-id="74aca-174">**lineGenerateTone**</span><span class="sxs-lookup"><span data-stu-id="74aca-174">**lineGenerateTone**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegeneratetone)     | <span data-ttu-id="74aca-175">Genera un set di toni specificato in una chiamata.</span><span class="sxs-lookup"><span data-stu-id="74aca-175">Generates a given set of tones inband on a call.</span></span> <span data-ttu-id="74aca-176">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="74aca-176">Synchronous.</span></span> |



 

## <a name="call-accept-and-redirect"></a><span data-ttu-id="74aca-177">Chiama Accept e reindirizza</span><span class="sxs-lookup"><span data-stu-id="74aca-177">Call Accept and Redirect</span></span>



| <span data-ttu-id="74aca-178">Funzione</span><span class="sxs-lookup"><span data-stu-id="74aca-178">Function</span></span>                             | <span data-ttu-id="74aca-179">Descrizione</span><span class="sxs-lookup"><span data-stu-id="74aca-179">Description</span></span>                                                                                               |
|--------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="74aca-180">**lineAccept**</span><span class="sxs-lookup"><span data-stu-id="74aca-180">**lineAccept**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineaccept)     | <span data-ttu-id="74aca-181">Accetta una chiamata offerta e avvia avvisi sia del chiamante (richiamabile) che del chiamante (anello).</span><span class="sxs-lookup"><span data-stu-id="74aca-181">Accepts an offered call and starts alerting both caller (ringback) and called party (ring).</span></span> <span data-ttu-id="74aca-182">Asincrona.</span><span class="sxs-lookup"><span data-stu-id="74aca-182">Asynchronous.</span></span> |
| [<span data-ttu-id="74aca-183">**lineRedirect**</span><span class="sxs-lookup"><span data-stu-id="74aca-183">**lineRedirect**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineredirect) | <span data-ttu-id="74aca-184">Reindirizza una chiamata di offerta a un altro indirizzo.</span><span class="sxs-lookup"><span data-stu-id="74aca-184">Redirects an offering call to another address.</span></span> <span data-ttu-id="74aca-185">Asincrona.</span><span class="sxs-lookup"><span data-stu-id="74aca-185">Asynchronous.</span></span>                                              |



 

## <a name="call-reject"></a><span data-ttu-id="74aca-186">Rifiuto chiamata</span><span class="sxs-lookup"><span data-stu-id="74aca-186">Call Reject</span></span>



| <span data-ttu-id="74aca-187">Funzione</span><span class="sxs-lookup"><span data-stu-id="74aca-187">Function</span></span>                     | <span data-ttu-id="74aca-188">Descrizione</span><span class="sxs-lookup"><span data-stu-id="74aca-188">Description</span></span>                                                               |
|------------------------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="74aca-189">**lineDrop**</span><span class="sxs-lookup"><span data-stu-id="74aca-189">**lineDrop**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linedrop) | <span data-ttu-id="74aca-190">Disconnette una chiamata o abbandona un tentativo di chiamata in corso.</span><span class="sxs-lookup"><span data-stu-id="74aca-190">Disconnects a call, or abandons a call attempt in progress.</span></span> <span data-ttu-id="74aca-191">Asincrona.</span><span class="sxs-lookup"><span data-stu-id="74aca-191">Asynchronous.</span></span> |



 

## <a name="call-hold"></a><span data-ttu-id="74aca-192">Attesa chiamata</span><span class="sxs-lookup"><span data-stu-id="74aca-192">Call Hold</span></span>



| <span data-ttu-id="74aca-193">Funzione</span><span class="sxs-lookup"><span data-stu-id="74aca-193">Function</span></span>                         | <span data-ttu-id="74aca-194">Descrizione</span><span class="sxs-lookup"><span data-stu-id="74aca-194">Description</span></span>                                           |
|----------------------------------|-------------------------------------------------------|
| [<span data-ttu-id="74aca-195">**lineHold**</span><span class="sxs-lookup"><span data-stu-id="74aca-195">**lineHold**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linehold)     | <span data-ttu-id="74aca-196">Inserisce la chiamata specificata sul disco rigido.</span><span class="sxs-lookup"><span data-stu-id="74aca-196">Places the specified call on hard hold.</span></span> <span data-ttu-id="74aca-197">Asincrona.</span><span class="sxs-lookup"><span data-stu-id="74aca-197">Asynchronous.</span></span> |
| [<span data-ttu-id="74aca-198">**lineUnhold**</span><span class="sxs-lookup"><span data-stu-id="74aca-198">**lineUnhold**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineunhold) | <span data-ttu-id="74aca-199">Recupera una chiamata mantenuta.</span><span class="sxs-lookup"><span data-stu-id="74aca-199">Retrieves a held call.</span></span> <span data-ttu-id="74aca-200">Asincrona.</span><span class="sxs-lookup"><span data-stu-id="74aca-200">Asynchronous.</span></span>                  |



 

## <a name="securing-calls"></a><span data-ttu-id="74aca-201">Protezione delle chiamate</span><span class="sxs-lookup"><span data-stu-id="74aca-201">Securing Calls</span></span>



| <span data-ttu-id="74aca-202">Funzione</span><span class="sxs-lookup"><span data-stu-id="74aca-202">Function</span></span>                                 | <span data-ttu-id="74aca-203">Descrizione</span><span class="sxs-lookup"><span data-stu-id="74aca-203">Description</span></span>                                                                                                              |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="74aca-204">**lineSecureCall**</span><span class="sxs-lookup"><span data-stu-id="74aca-204">**lineSecureCall**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesecurecall) | <span data-ttu-id="74aca-205">Protegge una chiamata esistente da interferenze da altri eventi, ad esempio segnali acustici in attesa di chiamate sulle connessioni dati.</span><span class="sxs-lookup"><span data-stu-id="74aca-205">Secures an existing call from interference by other events such as call-waiting beeps on data connections.</span></span> <span data-ttu-id="74aca-206">Asincrona.</span><span class="sxs-lookup"><span data-stu-id="74aca-206">Asynchronous.</span></span> |



 

## <a name="call-transfer"></a><span data-ttu-id="74aca-207">Trasferimento chiamate</span><span class="sxs-lookup"><span data-stu-id="74aca-207">Call Transfer</span></span>



| <span data-ttu-id="74aca-208">Funzione</span><span class="sxs-lookup"><span data-stu-id="74aca-208">Function</span></span>                                             | <span data-ttu-id="74aca-209">Descrizione</span><span class="sxs-lookup"><span data-stu-id="74aca-209">Description</span></span>                                                                                                    |
|------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="74aca-210">**lineSetupTransfer**</span><span class="sxs-lookup"><span data-stu-id="74aca-210">**lineSetupTransfer**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetuptransfer)       | <span data-ttu-id="74aca-211">Prepara una chiamata specificata per il trasferimento a un altro indirizzo.</span><span class="sxs-lookup"><span data-stu-id="74aca-211">Prepares a specified call for transfer to another address.</span></span> <span data-ttu-id="74aca-212">Asincrona.</span><span class="sxs-lookup"><span data-stu-id="74aca-212">Asynchronous.</span></span>                                       |
| [<span data-ttu-id="74aca-213">**lineCompleteTransfer**</span><span class="sxs-lookup"><span data-stu-id="74aca-213">**lineCompleteTransfer**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer) | <span data-ttu-id="74aca-214">Trasferisce una chiamata impostata per il trasferimento a un'altra chiamata o entra in una conferenza a tre vie.</span><span class="sxs-lookup"><span data-stu-id="74aca-214">Transfers a call that was set up for transfer to another call, or enters a three-way conference.</span></span> <span data-ttu-id="74aca-215">Asincrona.</span><span class="sxs-lookup"><span data-stu-id="74aca-215">Asynchronous.</span></span> |
| [<span data-ttu-id="74aca-216">**lineBlindTransfer**</span><span class="sxs-lookup"><span data-stu-id="74aca-216">**lineBlindTransfer**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineblindtransfer)       | <span data-ttu-id="74aca-217">Trasferisce una chiamata a un'altra entità.</span><span class="sxs-lookup"><span data-stu-id="74aca-217">Transfers a call to another party.</span></span> <span data-ttu-id="74aca-218">Asincrona.</span><span class="sxs-lookup"><span data-stu-id="74aca-218">Asynchronous.</span></span>                                                               |
| [<span data-ttu-id="74aca-219">**lineSwapHold**</span><span class="sxs-lookup"><span data-stu-id="74aca-219">**lineSwapHold**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineswaphold)                 | <span data-ttu-id="74aca-220">Scambia la chiamata attiva con la chiamata attualmente in attesa di consultazione.</span><span class="sxs-lookup"><span data-stu-id="74aca-220">Swaps the active call with the call currently on consultation hold.</span></span> <span data-ttu-id="74aca-221">Asincrona.</span><span class="sxs-lookup"><span data-stu-id="74aca-221">Asynchronous.</span></span>                              |



 

## <a name="call-conference"></a><span data-ttu-id="74aca-222">Conference Call</span><span class="sxs-lookup"><span data-stu-id="74aca-222">Call Conference</span></span>



| <span data-ttu-id="74aca-223">Funzione</span><span class="sxs-lookup"><span data-stu-id="74aca-223">Function</span></span>                                                         | <span data-ttu-id="74aca-224">Descrizione</span><span class="sxs-lookup"><span data-stu-id="74aca-224">Description</span></span>                                                                                                                                                                                          |
|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="74aca-225">**lineSetupConference**</span><span class="sxs-lookup"><span data-stu-id="74aca-225">**lineSetupConference**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetupconference)               | <span data-ttu-id="74aca-226">Prepara una determinata chiamata per l'aggiunta di un'altra parte.</span><span class="sxs-lookup"><span data-stu-id="74aca-226">Prepares a given call for the addition of another party.</span></span> <span data-ttu-id="74aca-227">Asincrona.</span><span class="sxs-lookup"><span data-stu-id="74aca-227">Asynchronous.</span></span>                                                                                                                               |
| [<span data-ttu-id="74aca-228">**linePrepareAddToConference**</span><span class="sxs-lookup"><span data-stu-id="74aca-228">**linePrepareAddToConference**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineprepareaddtoconference) | <span data-ttu-id="74aca-229">Prepara l'aggiunta di un'entità a una chiamata di conferenza esistente posizionando la chiamata di conferenza in uno stato di attesa e creando una chiamata di consultazione che può essere aggiunta successivamente alla chiamata di conferenza.</span><span class="sxs-lookup"><span data-stu-id="74aca-229">Prepares to add a party to an existing conference call by placing the conference call in a hold state and creating a consultation call that can be added later to the conference call.</span></span> <span data-ttu-id="74aca-230">Asincrona.</span><span class="sxs-lookup"><span data-stu-id="74aca-230">Asynchronous.</span></span> |
| [<span data-ttu-id="74aca-231">**lineAddToConference**</span><span class="sxs-lookup"><span data-stu-id="74aca-231">**lineAddToConference**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineaddtoconference)               | <span data-ttu-id="74aca-232">Aggiunge una chiamata di consultazione a una chiamata di conferenza esistente.</span><span class="sxs-lookup"><span data-stu-id="74aca-232">Adds a consultation call to an existing conference call.</span></span> <span data-ttu-id="74aca-233">Asincrona.</span><span class="sxs-lookup"><span data-stu-id="74aca-233">Asynchronous.</span></span>                                                                                                                               |
| [<span data-ttu-id="74aca-234">**lineRemoveFromConference**</span><span class="sxs-lookup"><span data-stu-id="74aca-234">**lineRemoveFromConference**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineremovefromconference)     | <span data-ttu-id="74aca-235">Rimuove un'entità da una chiamata di conferenza.</span><span class="sxs-lookup"><span data-stu-id="74aca-235">Removes a party from a conference call.</span></span> <span data-ttu-id="74aca-236">Asincrona.</span><span class="sxs-lookup"><span data-stu-id="74aca-236">Asynchronous.</span></span>                                                                                                                                                |



 

## <a name="call-park"></a><span data-ttu-id="74aca-237">Call Park</span><span class="sxs-lookup"><span data-stu-id="74aca-237">Call Park</span></span>



| <span data-ttu-id="74aca-238">Funzione</span><span class="sxs-lookup"><span data-stu-id="74aca-238">Function</span></span>                         | <span data-ttu-id="74aca-239">Descrizione</span><span class="sxs-lookup"><span data-stu-id="74aca-239">Description</span></span>                                          |
|----------------------------------|------------------------------------------------------|
| [<span data-ttu-id="74aca-240">**linePark**</span><span class="sxs-lookup"><span data-stu-id="74aca-240">**linePark**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linepark)     | <span data-ttu-id="74aca-241">Parcheggia una determinata chiamata a un altro indirizzo.</span><span class="sxs-lookup"><span data-stu-id="74aca-241">Parks a given call at another address.</span></span> <span data-ttu-id="74aca-242">Asincrona.</span><span class="sxs-lookup"><span data-stu-id="74aca-242">Asynchronous.</span></span> |
| [<span data-ttu-id="74aca-243">**lineUnpark**</span><span class="sxs-lookup"><span data-stu-id="74aca-243">**lineUnpark**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineunpark) | <span data-ttu-id="74aca-244">Recupera una chiamata parcheggiata.</span><span class="sxs-lookup"><span data-stu-id="74aca-244">Retrieves a parked call.</span></span> <span data-ttu-id="74aca-245">Asincrona.</span><span class="sxs-lookup"><span data-stu-id="74aca-245">Asynchronous.</span></span>               |



 

## <a name="call-forwarding"></a><span data-ttu-id="74aca-246">Invio di chiamate</span><span class="sxs-lookup"><span data-stu-id="74aca-246">Call Forwarding</span></span>



| <span data-ttu-id="74aca-247">Funzione</span><span class="sxs-lookup"><span data-stu-id="74aca-247">Function</span></span>                           | <span data-ttu-id="74aca-248">Descrizione</span><span class="sxs-lookup"><span data-stu-id="74aca-248">Description</span></span>                                             |
|------------------------------------|---------------------------------------------------------|
| [<span data-ttu-id="74aca-249">**lineForward**</span><span class="sxs-lookup"><span data-stu-id="74aca-249">**lineForward**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineforward) | <span data-ttu-id="74aca-250">Imposta o Annulla le richieste di invio della chiamata.</span><span class="sxs-lookup"><span data-stu-id="74aca-250">Sets or cancels call forwarding requests.</span></span> <span data-ttu-id="74aca-251">Asincrona.</span><span class="sxs-lookup"><span data-stu-id="74aca-251">Asynchronous.</span></span> |



 

## <a name="call-pickup"></a><span data-ttu-id="74aca-252">Pickup chiamata</span><span class="sxs-lookup"><span data-stu-id="74aca-252">Call Pickup</span></span>



| <span data-ttu-id="74aca-253">Funzione</span><span class="sxs-lookup"><span data-stu-id="74aca-253">Function</span></span>                         | <span data-ttu-id="74aca-254">Descrizione</span><span class="sxs-lookup"><span data-stu-id="74aca-254">Description</span></span>                                                                                                                                                                                      |
|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="74aca-255">**linePickup**</span><span class="sxs-lookup"><span data-stu-id="74aca-255">**linePickup**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linepickup) | <span data-ttu-id="74aca-256">Preleva un avviso di chiamata a un indirizzo di destinazione specificato e restituisce un handle di chiamata per la chiamata selezionata ([**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup) può essere usato anche per la chiamata in attesa).</span><span class="sxs-lookup"><span data-stu-id="74aca-256">Picks up a call alerting at a specified destination address and returns a call handle for the picked-up call ([**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup) can also be used for call waiting).</span></span> <span data-ttu-id="74aca-257">Asincrona.</span><span class="sxs-lookup"><span data-stu-id="74aca-257">Asynchronous.</span></span> |



 

## <a name="sending-information-to-remote-party"></a><span data-ttu-id="74aca-258">Invio di informazioni a un'entità remota</span><span class="sxs-lookup"><span data-stu-id="74aca-258">Sending Information to Remote Party</span></span>



| <span data-ttu-id="74aca-259">Funzione</span><span class="sxs-lookup"><span data-stu-id="74aca-259">Function</span></span>                                                   | <span data-ttu-id="74aca-260">Descrizione</span><span class="sxs-lookup"><span data-stu-id="74aca-260">Description</span></span>                                                                                                         |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="74aca-261">**lineReleaseUserUserInfo**</span><span class="sxs-lookup"><span data-stu-id="74aca-261">**lineReleaseUserUserInfo**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linereleaseuseruserinfo) | <span data-ttu-id="74aca-262">Rilascia informazioni utente utente, consentendo al sistema di sovrascrivere questa risorsa di archiviazione con nuove informazioni.</span><span class="sxs-lookup"><span data-stu-id="74aca-262">Releases user-user information, permitting the system to overwrite this storage with new information.</span></span> <span data-ttu-id="74aca-263">Asincrona.</span><span class="sxs-lookup"><span data-stu-id="74aca-263">Asynchronous.</span></span> |
| [<span data-ttu-id="74aca-264">**lineSendUserUserInfo**</span><span class="sxs-lookup"><span data-stu-id="74aca-264">**lineSendUserUserInfo**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesenduseruserinfo)       | <span data-ttu-id="74aca-265">Invia le informazioni utente utente alla parte remota sulla chiamata specificata.</span><span class="sxs-lookup"><span data-stu-id="74aca-265">Sends user-user information to the remote party on the specified call.</span></span> <span data-ttu-id="74aca-266">Asincrona.</span><span class="sxs-lookup"><span data-stu-id="74aca-266">Asynchronous.</span></span>                                |



 

## <a name="call-completion"></a><span data-ttu-id="74aca-267">Completamento chiamata</span><span class="sxs-lookup"><span data-stu-id="74aca-267">Call Completion</span></span>



| <span data-ttu-id="74aca-268">Funzione</span><span class="sxs-lookup"><span data-stu-id="74aca-268">Function</span></span>                                         | <span data-ttu-id="74aca-269">Descrizione</span><span class="sxs-lookup"><span data-stu-id="74aca-269">Description</span></span>                                      |
|--------------------------------------------------|--------------------------------------------------|
| [<span data-ttu-id="74aca-270">**lineCompleteCall**</span><span class="sxs-lookup"><span data-stu-id="74aca-270">**lineCompleteCall**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linecompletecall)     | <span data-ttu-id="74aca-271">Inserisce una richiesta di completamento della chiamata.</span><span class="sxs-lookup"><span data-stu-id="74aca-271">Places a call completion request.</span></span> <span data-ttu-id="74aca-272">Asincrona.</span><span class="sxs-lookup"><span data-stu-id="74aca-272">Asynchronous.</span></span>  |
| [<span data-ttu-id="74aca-273">**lineUncompleteCall**</span><span class="sxs-lookup"><span data-stu-id="74aca-273">**lineUncompleteCall**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineuncompletecall) | <span data-ttu-id="74aca-274">Annulla una richiesta di completamento della chiamata.</span><span class="sxs-lookup"><span data-stu-id="74aca-274">Cancels a call completion request.</span></span> <span data-ttu-id="74aca-275">Asincrona.</span><span class="sxs-lookup"><span data-stu-id="74aca-275">Asynchronous.</span></span> |



 

## <a name="setting-a-terminal-for-phone-conversations"></a><span data-ttu-id="74aca-276">Impostazione di un terminale per le conversazioni telefoniche</span><span class="sxs-lookup"><span data-stu-id="74aca-276">Setting a Terminal for Phone Conversations</span></span>



| <span data-ttu-id="74aca-277">Funzione</span><span class="sxs-lookup"><span data-stu-id="74aca-277">Function</span></span>                                   | <span data-ttu-id="74aca-278">Descrizione</span><span class="sxs-lookup"><span data-stu-id="74aca-278">Description</span></span>                                                                                                                      |
|--------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="74aca-279">**lineSetTerminal**</span><span class="sxs-lookup"><span data-stu-id="74aca-279">**lineSetTerminal**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetterminal) | <span data-ttu-id="74aca-280">Specifica il dispositivo terminal a cui vengono indirizzati gli eventi di riga, di indirizzo o di chiamata del flusso multimediale specificati.</span><span class="sxs-lookup"><span data-stu-id="74aca-280">Specifies the terminal device to which the specified line, address events, or call media stream events are routed.</span></span> <span data-ttu-id="74aca-281">Asincrona.</span><span class="sxs-lookup"><span data-stu-id="74aca-281">Asynchronous.</span></span> |



 

## <a name="application-priority"></a><span data-ttu-id="74aca-282">Priorità applicazione</span><span class="sxs-lookup"><span data-stu-id="74aca-282">Application Priority</span></span>



| <span data-ttu-id="74aca-283">Funzione</span><span class="sxs-lookup"><span data-stu-id="74aca-283">Function</span></span>                                         | <span data-ttu-id="74aca-284">Descrizione</span><span class="sxs-lookup"><span data-stu-id="74aca-284">Description</span></span>                                                                                       |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="74aca-285">**lineGetAppPriority**</span><span class="sxs-lookup"><span data-stu-id="74aca-285">**lineGetAppPriority**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetapppriority) | <span data-ttu-id="74aca-286">Recupera le informazioni sulla priorità di telefonia uniforme e/o assistita per un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="74aca-286">Retrieves handoff and/or Assisted Telephony priority information for an application.</span></span> <span data-ttu-id="74aca-287">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="74aca-287">Synchronous.</span></span> |
| [<span data-ttu-id="74aca-288">**lineSetAppPriority**</span><span class="sxs-lookup"><span data-stu-id="74aca-288">**lineSetAppPriority**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetapppriority) | <span data-ttu-id="74aca-289">Imposta la priorità di consegna e/o di telefonia assistita per un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="74aca-289">Sets the handoff and/or Assisted Telephony priority for an application.</span></span> <span data-ttu-id="74aca-290">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="74aca-290">Synchronous.</span></span>              |



 

## <a name="service-provider-management"></a><span data-ttu-id="74aca-291">Gestione provider di servizi</span><span class="sxs-lookup"><span data-stu-id="74aca-291">Service Provider Management</span></span>



| <span data-ttu-id="74aca-292">Funzione</span><span class="sxs-lookup"><span data-stu-id="74aca-292">Function</span></span>                                           | <span data-ttu-id="74aca-293">Descrizione</span><span class="sxs-lookup"><span data-stu-id="74aca-293">Description</span></span>                                                           |
|----------------------------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="74aca-294">**lineAddProvider**</span><span class="sxs-lookup"><span data-stu-id="74aca-294">**lineAddProvider**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineaddprovider)         | <span data-ttu-id="74aca-295">Installa un provider di servizi di telefonia.</span><span class="sxs-lookup"><span data-stu-id="74aca-295">Installs a telephony service provider.</span></span> <span data-ttu-id="74aca-296">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="74aca-296">Synchronous.</span></span>                   |
| [<span data-ttu-id="74aca-297">**lineConfigProvider**</span><span class="sxs-lookup"><span data-stu-id="74aca-297">**lineConfigProvider**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineconfigprovider)   | <span data-ttu-id="74aca-298">Visualizza la finestra di dialogo di configurazione di un provider di servizi.</span><span class="sxs-lookup"><span data-stu-id="74aca-298">Displays configuration dialog box of a service provider.</span></span> <span data-ttu-id="74aca-299">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="74aca-299">Synchronous.</span></span> |
| [<span data-ttu-id="74aca-300">**lineRemoveProvider**</span><span class="sxs-lookup"><span data-stu-id="74aca-300">**lineRemoveProvider**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineremoveprovider)   | <span data-ttu-id="74aca-301">Rimuove un provider di servizi di telefonia esistente.</span><span class="sxs-lookup"><span data-stu-id="74aca-301">Removes an existing telephony service provider.</span></span> <span data-ttu-id="74aca-302">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="74aca-302">Synchronous.</span></span>          |
| [<span data-ttu-id="74aca-303">**lineGetProviderList**</span><span class="sxs-lookup"><span data-stu-id="74aca-303">**lineGetProviderList**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetproviderlist) | <span data-ttu-id="74aca-304">Recupera un elenco di provider di servizi installati.</span><span class="sxs-lookup"><span data-stu-id="74aca-304">Retrieves a list of installed service providers.</span></span> <span data-ttu-id="74aca-305">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="74aca-305">Synchronous.</span></span>         |



 

## <a name="agents"></a><span data-ttu-id="74aca-306">Agenti</span><span class="sxs-lookup"><span data-stu-id="74aca-306">Agents</span></span>



| <span data-ttu-id="74aca-307">Funzione</span><span class="sxs-lookup"><span data-stu-id="74aca-307">Function</span></span>                                                     | <span data-ttu-id="74aca-308">Descrizione</span><span class="sxs-lookup"><span data-stu-id="74aca-308">Description</span></span>                                                                                                                             |
|--------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="74aca-309">**lineAgentSpecific**</span><span class="sxs-lookup"><span data-stu-id="74aca-309">**lineAgentSpecific**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineagentspecific)               | <span data-ttu-id="74aca-310">Consente all'applicazione di accedere alle funzioni proprietarie specifiche del gestore dell'agente associato all'indirizzo.</span><span class="sxs-lookup"><span data-stu-id="74aca-310">Allows the application to access proprietary handler-specific functions of the agent handler associated with the address.</span></span> <span data-ttu-id="74aca-311">Asincrona.</span><span class="sxs-lookup"><span data-stu-id="74aca-311">Asynchronous.</span></span> |
| [<span data-ttu-id="74aca-312">**lineGetAgentActivityList**</span><span class="sxs-lookup"><span data-stu-id="74aca-312">**lineGetAgentActivityList**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetagentactivitylista) | <span data-ttu-id="74aca-313">Ottiene l'elenco delle attività da cui un'applicazione seleziona le funzioni eseguite da un agente.</span><span class="sxs-lookup"><span data-stu-id="74aca-313">Obtains the list of activities from which an application selects the functions an agent is performing.</span></span> <span data-ttu-id="74aca-314">Asincrona.</span><span class="sxs-lookup"><span data-stu-id="74aca-314">Asynchronous.</span></span>                    |
| [<span data-ttu-id="74aca-315">**lineGetAgentCaps**</span><span class="sxs-lookup"><span data-stu-id="74aca-315">**lineGetAgentCaps**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetagentcapsa)                 | <span data-ttu-id="74aca-316">Ottiene le funzionalità correlate all'agente supportate nel dispositivo a linee specificato.</span><span class="sxs-lookup"><span data-stu-id="74aca-316">Obtains the agent-related capabilities supported on the specified line device.</span></span> <span data-ttu-id="74aca-317">Asincrona.</span><span class="sxs-lookup"><span data-stu-id="74aca-317">Asynchronous.</span></span>                                            |
| [<span data-ttu-id="74aca-318">**lineGetAgentGroupList**</span><span class="sxs-lookup"><span data-stu-id="74aca-318">**lineGetAgentGroupList**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetagentgrouplista)       | <span data-ttu-id="74aca-319">Ottiene l'elenco dei gruppi di agenti in cui un agente può accedere al server di distribuzione chiamate automatico.</span><span class="sxs-lookup"><span data-stu-id="74aca-319">Obtains the list of agent groups into which an agent can log into on the automatic call distributor.</span></span> <span data-ttu-id="74aca-320">Asincrona.</span><span class="sxs-lookup"><span data-stu-id="74aca-320">Asynchronous.</span></span>                      |
| [<span data-ttu-id="74aca-321">**lineGetAgentStatus**</span><span class="sxs-lookup"><span data-stu-id="74aca-321">**lineGetAgentStatus**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetagentstatusa)             | <span data-ttu-id="74aca-322">Ottiene lo stato relativo all'agente nell'indirizzo specificato.</span><span class="sxs-lookup"><span data-stu-id="74aca-322">Obtains the agent-related status on the specified address.</span></span> <span data-ttu-id="74aca-323">Asincrona.</span><span class="sxs-lookup"><span data-stu-id="74aca-323">Asynchronous.</span></span>                                                                |
| [<span data-ttu-id="74aca-324">**lineSetAgentActivity**</span><span class="sxs-lookup"><span data-stu-id="74aca-324">**lineSetAgentActivity**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetagentactivity)         | <span data-ttu-id="74aca-325">Imposta il codice dell'attività dell'agente associato a un indirizzo specifico.</span><span class="sxs-lookup"><span data-stu-id="74aca-325">Sets the agent activity code associated with a particular address.</span></span> <span data-ttu-id="74aca-326">Asincrona.</span><span class="sxs-lookup"><span data-stu-id="74aca-326">Asynchronous.</span></span>                                                        |
| [<span data-ttu-id="74aca-327">**lineSetAgentGroup**</span><span class="sxs-lookup"><span data-stu-id="74aca-327">**lineSetAgentGroup**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetagentgroup)               | <span data-ttu-id="74aca-328">Imposta i gruppi di agenti a cui l'agente è connesso in un determinato indirizzo.</span><span class="sxs-lookup"><span data-stu-id="74aca-328">Sets the agent groups that the agent is logged into on a particular address.</span></span> <span data-ttu-id="74aca-329">Asincrona.</span><span class="sxs-lookup"><span data-stu-id="74aca-329">Asynchronous.</span></span>                                              |
| [<span data-ttu-id="74aca-330">**lineSetAgentState**</span><span class="sxs-lookup"><span data-stu-id="74aca-330">**lineSetAgentState**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetagentstate)               | <span data-ttu-id="74aca-331">Imposta lo stato dell'agente associato a un determinato indirizzo.</span><span class="sxs-lookup"><span data-stu-id="74aca-331">Sets the agent state associated with a particular address.</span></span> <span data-ttu-id="74aca-332">Asincrona.</span><span class="sxs-lookup"><span data-stu-id="74aca-332">Asynchronous.</span></span>                                                                |



 

## <a name="proxies"></a><span data-ttu-id="74aca-333">Proxy</span><span class="sxs-lookup"><span data-stu-id="74aca-333">Proxies</span></span>



| <span data-ttu-id="74aca-334">Funzione</span><span class="sxs-lookup"><span data-stu-id="74aca-334">Function</span></span>                                       | <span data-ttu-id="74aca-335">Descrizione</span><span class="sxs-lookup"><span data-stu-id="74aca-335">Description</span></span>                                                                         |
|------------------------------------------------|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="74aca-336">**lineProxyMessage**</span><span class="sxs-lookup"><span data-stu-id="74aca-336">**lineProxyMessage**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage)   | <span data-ttu-id="74aca-337">Utilizzato da un gestore di richieste proxy registrato per generare messaggi TAPI.</span><span class="sxs-lookup"><span data-stu-id="74aca-337">Used by a registered proxy request handler to generate TAPI messages.</span></span> <span data-ttu-id="74aca-338">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="74aca-338">Synchronous.</span></span>  |
| [<span data-ttu-id="74aca-339">**lineProxyResponse**</span><span class="sxs-lookup"><span data-stu-id="74aca-339">**lineProxyResponse**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse) | <span data-ttu-id="74aca-340">Indica il completamento di una richiesta proxy da un gestore proxy registrato.</span><span class="sxs-lookup"><span data-stu-id="74aca-340">Indicates completion of a proxy request by a registered proxy handler.</span></span> <span data-ttu-id="74aca-341">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="74aca-341">Synchronous.</span></span> |



 

## <a name="quality-of-service"></a><span data-ttu-id="74aca-342">QoS (Quality of Service)</span><span class="sxs-lookup"><span data-stu-id="74aca-342">Quality of Service</span></span>



| <span data-ttu-id="74aca-343">Funzione</span><span class="sxs-lookup"><span data-stu-id="74aca-343">Function</span></span>                                                           | <span data-ttu-id="74aca-344">Descrizione</span><span class="sxs-lookup"><span data-stu-id="74aca-344">Description</span></span>                                                                                |
|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="74aca-345">**lineSetCallQualityOfService**</span><span class="sxs-lookup"><span data-stu-id="74aca-345">**lineSetCallQualityOfService**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetcallqualityofservice) | <span data-ttu-id="74aca-346">Richiede una modifica dei parametri di qualità del servizio per una chiamata esistente.</span><span class="sxs-lookup"><span data-stu-id="74aca-346">Requests a change of the quality of service parameters for an existing call.</span></span> <span data-ttu-id="74aca-347">Asincrona.</span><span class="sxs-lookup"><span data-stu-id="74aca-347">Asynchronous.</span></span> |



 

## <a name="miscellaneous"></a><span data-ttu-id="74aca-348">Varie</span><span class="sxs-lookup"><span data-stu-id="74aca-348">Miscellaneous</span></span>



| <span data-ttu-id="74aca-349">Funzione</span><span class="sxs-lookup"><span data-stu-id="74aca-349">Function</span></span>                                             | <span data-ttu-id="74aca-350">Descrizione</span><span class="sxs-lookup"><span data-stu-id="74aca-350">Description</span></span>                                                                                           |
|------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="74aca-351">**lineSetCallData**</span><span class="sxs-lookup"><span data-stu-id="74aca-351">**lineSetCallData**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetcalldata)           | <span data-ttu-id="74aca-352">Imposta il membro **CallData** della struttura [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) .</span><span class="sxs-lookup"><span data-stu-id="74aca-352">Sets the **CallData** member of the [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) structure.</span></span> <span data-ttu-id="74aca-353">Asincrona.</span><span class="sxs-lookup"><span data-stu-id="74aca-353">Asynchronous.</span></span> |
| [<span data-ttu-id="74aca-354">**lineSetCallTreatment**</span><span class="sxs-lookup"><span data-stu-id="74aca-354">**lineSetCallTreatment**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetcalltreatment) | <span data-ttu-id="74aca-355">Imposta i suoni che l'utente avverte quando una chiamata non risponde o è in attesa.</span><span class="sxs-lookup"><span data-stu-id="74aca-355">Sets the sounds that the user hears when a call is unanswered or on hold.</span></span> <span data-ttu-id="74aca-356">Asincrona.</span><span class="sxs-lookup"><span data-stu-id="74aca-356">Asynchronous.</span></span>               |
| [<span data-ttu-id="74aca-357">**lineSetLineDevStatus**</span><span class="sxs-lookup"><span data-stu-id="74aca-357">**lineSetLineDevStatus**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetlinedevstatus) | <span data-ttu-id="74aca-358">Imposta lo stato del dispositivo di linea.</span><span class="sxs-lookup"><span data-stu-id="74aca-358">Sets the line device status.</span></span> <span data-ttu-id="74aca-359">Asincrona.</span><span class="sxs-lookup"><span data-stu-id="74aca-359">Asynchronous.</span></span>                                                            |



 

 

 



