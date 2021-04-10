---
title: Impostazioni di rete predefinite
description: Impostazioni di rete predefinite
ms.assetid: 07464107-9cf7-4ed0-a76b-17ea153399a1
keywords:
- Windows Media Format SDK, impostazioni di rete predefinite
- ASF (Advanced Systems Format), impostazioni di rete predefinite
- ASF (formato avanzato dei sistemi), impostazioni di rete predefinite
- Windows Media Format SDK, impostazioni di rete
- ASF (Advanced Systems Format), impostazioni di rete
- ASF (formato avanzato dei sistemi), impostazioni di rete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f4f219a60d9211b63eb124500c014452a0143d1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856925"
---
# <a name="default-networking-settings"></a><span data-ttu-id="e62cb-109">Impostazioni di rete predefinite</span><span class="sxs-lookup"><span data-stu-id="e62cb-109">Default Networking Settings</span></span>

<span data-ttu-id="e62cb-110">Le tabelle seguenti descrivono le impostazioni predefinite dei parametri di rete in Windows Media Format SDK, raggruppate per interfaccia.</span><span class="sxs-lookup"><span data-stu-id="e62cb-110">The following tables describe the default settings of the networking parameters in the Windows Media Format SDK, grouped by interface.</span></span>



| <span data-ttu-id="e62cb-111">IWMReaderNetworkConfig</span><span class="sxs-lookup"><span data-stu-id="e62cb-111">IWMReaderNetworkConfig</span></span>                | <span data-ttu-id="e62cb-112">Impostazione predefinita</span><span class="sxs-lookup"><span data-stu-id="e62cb-112">Default setting</span></span>              |
|---------------------------------------|------------------------------|
| <span data-ttu-id="e62cb-113">Tempo di memorizzazione nel buffer</span><span class="sxs-lookup"><span data-stu-id="e62cb-113">Buffering time</span></span>                        | <span data-ttu-id="e62cb-114">5 secondi</span><span class="sxs-lookup"><span data-stu-id="e62cb-114">5 seconds</span></span>                    |
| <span data-ttu-id="e62cb-115">UseFixedUDPPort</span><span class="sxs-lookup"><span data-stu-id="e62cb-115">UseFixedUDPPort</span></span>                       | <span data-ttu-id="e62cb-116">FALSE</span><span class="sxs-lookup"><span data-stu-id="e62cb-116">FALSE</span></span>                        |
| <span data-ttu-id="e62cb-117">FixedUDPPort</span><span class="sxs-lookup"><span data-stu-id="e62cb-117">FixedUDPPort</span></span>                          | <span data-ttu-id="e62cb-118">0 (non valido)</span><span class="sxs-lookup"><span data-stu-id="e62cb-118">0 (not valid)</span></span>                |
| <span data-ttu-id="e62cb-119">ProxySetting: HTTP</span><span class="sxs-lookup"><span data-stu-id="e62cb-119">ProxySetting: HTTP</span></span>                    | <span data-ttu-id="e62cb-120">\_ \_ browser impostazioni proxy \_ WMT</span><span class="sxs-lookup"><span data-stu-id="e62cb-120">WMT\_PROXY\_SETTING\_BROWSER</span></span> |
| <span data-ttu-id="e62cb-121">ProxySetting: MMS</span><span class="sxs-lookup"><span data-stu-id="e62cb-121">ProxySetting: MMS</span></span>                     | <span data-ttu-id="e62cb-122">\_impostazione del proxy WMT \_ \_ None</span><span class="sxs-lookup"><span data-stu-id="e62cb-122">WMT\_PROXY\_SETTING\_NONE</span></span>    |
| <span data-ttu-id="e62cb-123">ProxySetting: RTSP</span><span class="sxs-lookup"><span data-stu-id="e62cb-123">ProxySetting: RTSP</span></span>                    | <span data-ttu-id="e62cb-124">\_impostazione del proxy WMT \_ \_ None</span><span class="sxs-lookup"><span data-stu-id="e62cb-124">WMT\_PROXY\_SETTING\_NONE</span></span>    |
| <span data-ttu-id="e62cb-125">ProxyHostName (HTTP, MMS, RTSP)</span><span class="sxs-lookup"><span data-stu-id="e62cb-125">ProxyHostName (HTTP, MMS, RTSP)</span></span>       | <span data-ttu-id="e62cb-126">""</span><span class="sxs-lookup"><span data-stu-id="e62cb-126">""</span></span>                           |
| <span data-ttu-id="e62cb-127">ProxyPort: HTTP</span><span class="sxs-lookup"><span data-stu-id="e62cb-127">ProxyPort: HTTP</span></span>                       | <span data-ttu-id="e62cb-128">80</span><span class="sxs-lookup"><span data-stu-id="e62cb-128">80</span></span>                           |
| <span data-ttu-id="e62cb-129">ProxyPort: MMS</span><span class="sxs-lookup"><span data-stu-id="e62cb-129">ProxyPort: MMS</span></span>                        | <span data-ttu-id="e62cb-130">1755</span><span class="sxs-lookup"><span data-stu-id="e62cb-130">1755</span></span>                         |
| <span data-ttu-id="e62cb-131">ProxtPort: RTSP</span><span class="sxs-lookup"><span data-stu-id="e62cb-131">ProxtPort: RTSP</span></span>                       | <span data-ttu-id="e62cb-132">554</span><span class="sxs-lookup"><span data-stu-id="e62cb-132">554</span></span>                          |
| <span data-ttu-id="e62cb-133">ProxyExceptionList (HTTP, MMS, RTSP)</span><span class="sxs-lookup"><span data-stu-id="e62cb-133">ProxyExceptionList (HTTP, MMS, RTSP)</span></span>  | <span data-ttu-id="e62cb-134">""</span><span class="sxs-lookup"><span data-stu-id="e62cb-134">""</span></span>                           |
| <span data-ttu-id="e62cb-135">ProxyBypassForLocal (HTTP, MMS, RTSP)</span><span class="sxs-lookup"><span data-stu-id="e62cb-135">ProxyBypassForLocal (HTTP, MMS, RTSP)</span></span> | <span data-ttu-id="e62cb-136">FALSE</span><span class="sxs-lookup"><span data-stu-id="e62cb-136">FALSE</span></span>                        |
| <span data-ttu-id="e62cb-137">ForceRerunAutoDetection</span><span class="sxs-lookup"><span data-stu-id="e62cb-137">ForceRerunAutoDetection</span></span>               | <span data-ttu-id="e62cb-138">FALSE</span><span class="sxs-lookup"><span data-stu-id="e62cb-138">FALSE</span></span>                        |
| <span data-ttu-id="e62cb-139">EnableMulticast</span><span class="sxs-lookup"><span data-stu-id="e62cb-139">EnableMulticast</span></span>                       | <span data-ttu-id="e62cb-140">true</span><span class="sxs-lookup"><span data-stu-id="e62cb-140">TRUE</span></span>                         |
| <span data-ttu-id="e62cb-141">EnableHTTP</span><span class="sxs-lookup"><span data-stu-id="e62cb-141">EnableHTTP</span></span>                            | <span data-ttu-id="e62cb-142">true</span><span class="sxs-lookup"><span data-stu-id="e62cb-142">TRUE</span></span>                         |
| <span data-ttu-id="e62cb-143">EnableTCP</span><span class="sxs-lookup"><span data-stu-id="e62cb-143">EnableTCP</span></span>                             | <span data-ttu-id="e62cb-144">true</span><span class="sxs-lookup"><span data-stu-id="e62cb-144">TRUE</span></span>                         |
| <span data-ttu-id="e62cb-145">EnableUDP</span><span class="sxs-lookup"><span data-stu-id="e62cb-145">EnableUDP</span></span>                             | <span data-ttu-id="e62cb-146">true</span><span class="sxs-lookup"><span data-stu-id="e62cb-146">TRUE</span></span>                         |
| <span data-ttu-id="e62cb-147">Larghezza di banda di connessione</span><span class="sxs-lookup"><span data-stu-id="e62cb-147">Connection Bandwidth</span></span>                  | <span data-ttu-id="e62cb-148">0 (rilevamento automatico)</span><span class="sxs-lookup"><span data-stu-id="e62cb-148">0 (auto-detect)</span></span>              |



 



| <span data-ttu-id="e62cb-149">IWMReaderNetworkConfig2</span><span class="sxs-lookup"><span data-stu-id="e62cb-149">IWMReaderNetworkConfig2</span></span>        | <span data-ttu-id="e62cb-150">Impostazione predefinita</span><span class="sxs-lookup"><span data-stu-id="e62cb-150">Default setting</span></span>        |
|--------------------------------|------------------------|
| <span data-ttu-id="e62cb-151">Durata flusso accelerato</span><span class="sxs-lookup"><span data-stu-id="e62cb-151">Accelerated streaming duration</span></span> | <span data-ttu-id="e62cb-152">100 milioni (10 secondi)</span><span class="sxs-lookup"><span data-stu-id="e62cb-152">100000000 (10 seconds)</span></span> |
| <span data-ttu-id="e62cb-153">Abilita Caching contenuto</span><span class="sxs-lookup"><span data-stu-id="e62cb-153">Enable content caching</span></span>         | <span data-ttu-id="e62cb-154">true</span><span class="sxs-lookup"><span data-stu-id="e62cb-154">TRUE</span></span>                   |
| <span data-ttu-id="e62cb-155">Abilita cache veloce</span><span class="sxs-lookup"><span data-stu-id="e62cb-155">Enable fast cache</span></span>              | <span data-ttu-id="e62cb-156">true</span><span class="sxs-lookup"><span data-stu-id="e62cb-156">TRUE</span></span>                   |
| <span data-ttu-id="e62cb-157">Abilita reinvii</span><span class="sxs-lookup"><span data-stu-id="e62cb-157">Enable resends</span></span>                 | <span data-ttu-id="e62cb-158">true</span><span class="sxs-lookup"><span data-stu-id="e62cb-158">TRUE</span></span>                   |
| <span data-ttu-id="e62cb-159">Abilita l'assottigliamento del contenuto</span><span class="sxs-lookup"><span data-stu-id="e62cb-159">Enable content thinning</span></span>        | <span data-ttu-id="e62cb-160">true</span><span class="sxs-lookup"><span data-stu-id="e62cb-160">TRUE</span></span>                   |
| <span data-ttu-id="e62cb-161">Limite riconnessione</span><span class="sxs-lookup"><span data-stu-id="e62cb-161">Reconnect limit</span></span>                | <span data-ttu-id="e62cb-162">25</span><span class="sxs-lookup"><span data-stu-id="e62cb-162">25</span></span>                     |



 



| <span data-ttu-id="e62cb-163">IWMWriterNetworkSink</span><span class="sxs-lookup"><span data-stu-id="e62cb-163">IWMWriterNetworkSink</span></span> | <span data-ttu-id="e62cb-164">Impostazione predefinita</span><span class="sxs-lookup"><span data-stu-id="e62cb-164">Default setting</span></span>         |
|----------------------|-------------------------|
| <span data-ttu-id="e62cb-165">Numero massimo di client</span><span class="sxs-lookup"><span data-stu-id="e62cb-165">Maximum clients</span></span>      | <span data-ttu-id="e62cb-166">5</span><span class="sxs-lookup"><span data-stu-id="e62cb-166">5</span></span>                       |
| <span data-ttu-id="e62cb-167">Protocollo di rete</span><span class="sxs-lookup"><span data-stu-id="e62cb-167">Network protocol</span></span>     | <span data-ttu-id="e62cb-168">0 ( \_ protocollo \_ http WMT)</span><span class="sxs-lookup"><span data-stu-id="e62cb-168">0 (WMT\_PROTOCOL\_HTTP)</span></span> |
| <span data-ttu-id="e62cb-169">URL host</span><span class="sxs-lookup"><span data-stu-id="e62cb-169">Host URL</span></span>             | <span data-ttu-id="e62cb-170">0 (non valido)</span><span class="sxs-lookup"><span data-stu-id="e62cb-170">0 (not valid)</span></span>           |



 



| <span data-ttu-id="e62cb-171">IWMWriterAdvanced2</span><span class="sxs-lookup"><span data-stu-id="e62cb-171">IWMWriterAdvanced2</span></span>  | <span data-ttu-id="e62cb-172">Impostazione predefinita</span><span class="sxs-lookup"><span data-stu-id="e62cb-172">Default setting</span></span>             |
|---------------------|-----------------------------|
| <span data-ttu-id="e62cb-173">Dimensioni massime pacchetto</span><span class="sxs-lookup"><span data-stu-id="e62cb-173">Maximum packet size</span></span> | <span data-ttu-id="e62cb-174">1400</span><span class="sxs-lookup"><span data-stu-id="e62cb-174">1400</span></span>                        |
| <span data-ttu-id="e62cb-175">ID client di log</span><span class="sxs-lookup"><span data-stu-id="e62cb-175">Log client ID</span></span>       | <span data-ttu-id="e62cb-176">FALSE</span><span class="sxs-lookup"><span data-stu-id="e62cb-176">FALSE</span></span>                       |
| <span data-ttu-id="e62cb-177">Modalità di riproduzione</span><span class="sxs-lookup"><span data-stu-id="e62cb-177">Play mode</span></span>           | <span data-ttu-id="e62cb-178">\_ \_ \_ selezione autoselezione modalità di riproduzione WMT</span><span class="sxs-lookup"><span data-stu-id="e62cb-178">WMT\_PLAY\_MODE\_AUTOSELECT</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="e62cb-179">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e62cb-179">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e62cb-180">**Implementazione della funzionalità di rete**</span><span class="sxs-lookup"><span data-stu-id="e62cb-180">**Implementing Network Functionality**</span></span>](implementing-network-functionality.md)
</dt> </dl>

 

 




