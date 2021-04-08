---
title: Impostazioni del registro di sistema della porta del firewall
description: Impostazioni del registro di sistema della porta del firewall
ms.assetid: 86995f2c-8794-45da-9dca-9cdd388b2a21
keywords:
- Windows Media Player, impostazioni del registro di sistema della porta firewall
- Windows Media Player, impostazioni del registro di sistema della porta
- Windows Media Player, registro di sistema
- Registro di sistema, impostazioni della porta del firewall
- Registro di sistema, impostazioni porta
- Registro di sistema, impostazioni per Windows Media Player
- impostazioni del registro di sistema della porta del firewall
- impostazioni del registro di sistema della porta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e231732e8d62efce575ae3fdee5edc63975f23c9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855565"
---
# <a name="firewall-port-registry-settings"></a><span data-ttu-id="e8ffd-111">Impostazioni del registro di sistema della porta del firewall</span><span class="sxs-lookup"><span data-stu-id="e8ffd-111">Firewall Port Registry Settings</span></span>

<span data-ttu-id="e8ffd-112">Windows Media Player inserisce le voci nel registro di sistema in modo che i firewall possano determinare se aprire o chiudere le porte utilizzate dalla condivisione del catalogo multimediale.</span><span class="sxs-lookup"><span data-stu-id="e8ffd-112">Windows Media Player places entries in the registry so that firewalls can determine whether to open or close the ports that are used by media library sharing.</span></span>

<span data-ttu-id="e8ffd-113">**Voce del registro di sistema AcceptedEULA**</span><span class="sxs-lookup"><span data-stu-id="e8ffd-113">**AcceptedEULA Registry Entry**</span></span>

<span data-ttu-id="e8ffd-114">Windows Media Player utilizza la seguente voce del registro di sistema per indicare se l'utente ha accettato il contratto di licenza con l'utente finale (EULA).</span><span class="sxs-lookup"><span data-stu-id="e8ffd-114">Windows Media Player uses the following registry entry to indicate whether the user has accepted the end user license agreement (EULA).</span></span>


```C++
[HKEY_LOCAL_MACHINE\Software\Microsoft\MediaPlayer\Preferences]
"AcceptedEULA" = dword:value
```



<span data-ttu-id="e8ffd-115">Il valore 1 indica che l'utente ha accettato il contratto di licenza.</span><span class="sxs-lookup"><span data-stu-id="e8ffd-115">A value of 1 indicates that the user has accepted the license agreement.</span></span> <span data-ttu-id="e8ffd-116">Il valore 0 indica che l'utente non ha accettato il contratto di licenza.</span><span class="sxs-lookup"><span data-stu-id="e8ffd-116">A value of 0 indicates that the user has not accepted the license agreement.</span></span>

<span data-ttu-id="e8ffd-117">**Voce del registro di sistema WMPNSSFirewallPortsOpen**</span><span class="sxs-lookup"><span data-stu-id="e8ffd-117">**WMPNSSFirewallPortsOpen Registry Entry**</span></span>

<span data-ttu-id="e8ffd-118">Windows Media Player utilizza la seguente voce del registro di sistema per indicare se l'utente ha scelto di condividere la propria libreria multimediale con altri computer in una rete domestica.</span><span class="sxs-lookup"><span data-stu-id="e8ffd-118">Windows Media Player uses the following registry entry to indicate whether the user has chosen to share his or her media library with other computers on a home network.</span></span>


```C++
[HKEY_LOCAL_MACHINE\Software\Microsoft\MediaPlayer\Preferences]
"WMPNSSFirewallPortsOpen" = dword:value
```



<span data-ttu-id="e8ffd-119">Il valore 1 indica che l'utente ha scelto di condividere la libreria.</span><span class="sxs-lookup"><span data-stu-id="e8ffd-119">A value of 1 indicates that the user has chosen to share the library.</span></span> <span data-ttu-id="e8ffd-120">Il valore 0 indica che l'utente ha scelto di non condividere la libreria.</span><span class="sxs-lookup"><span data-stu-id="e8ffd-120">A value of 0 indicates that the user has chosen not to share the library.</span></span>

<span data-ttu-id="e8ffd-121">**Porte correlate alla condivisione del catalogo multimediale**</span><span class="sxs-lookup"><span data-stu-id="e8ffd-121">**Ports Related to Media Library Sharing**</span></span>

<span data-ttu-id="e8ffd-122">In Windows Vista, se la voce del registro di sistema **WMPNSSFirewallPortsOpen** ha un valore pari a 1, è necessario aprire le porte seguenti.</span><span class="sxs-lookup"><span data-stu-id="e8ffd-122">On Windows Vista, if the **WMPNSSFirewallPortsOpen** registry entry has a value of 1, the following ports should be open.</span></span>



| <span data-ttu-id="e8ffd-123">Porta</span><span class="sxs-lookup"><span data-stu-id="e8ffd-123">Port</span></span>          | <span data-ttu-id="e8ffd-124">Protocollo</span><span class="sxs-lookup"><span data-stu-id="e8ffd-124">Protocol</span></span>                  | <span data-ttu-id="e8ffd-125">Processo</span><span class="sxs-lookup"><span data-stu-id="e8ffd-125">Process</span></span>                         | <span data-ttu-id="e8ffd-126">Direzione</span><span class="sxs-lookup"><span data-stu-id="e8ffd-126">Direction</span></span>            |
|---------------|---------------------------|---------------------------------|----------------------|
| <span data-ttu-id="e8ffd-127">554</span><span class="sxs-lookup"><span data-stu-id="e8ffd-127">554</span></span>           | <span data-ttu-id="e8ffd-128">RTSP TCP</span><span class="sxs-lookup"><span data-stu-id="e8ffd-128">TCP RTSP</span></span>                  | <span data-ttu-id="e8ffd-129">wmpnetwk.exe</span><span class="sxs-lookup"><span data-stu-id="e8ffd-129">wmpnetwk.exe</span></span>                    | <span data-ttu-id="e8ffd-130">in ingresso e in uscita</span><span class="sxs-lookup"><span data-stu-id="e8ffd-130">inbound and outbound</span></span> |
| <span data-ttu-id="e8ffd-131">8554-8558</span><span class="sxs-lookup"><span data-stu-id="e8ffd-131">8554 - 8558</span></span>   | <span data-ttu-id="e8ffd-132">RTSP TCP</span><span class="sxs-lookup"><span data-stu-id="e8ffd-132">TCP RTSP</span></span>                  | <span data-ttu-id="e8ffd-133">wmpnetwk.exe</span><span class="sxs-lookup"><span data-stu-id="e8ffd-133">wmpnetwk.exe</span></span>                    | <span data-ttu-id="e8ffd-134">in ingresso e in uscita</span><span class="sxs-lookup"><span data-stu-id="e8ffd-134">inbound and outbound</span></span> |
| <span data-ttu-id="e8ffd-135">5004, 5005</span><span class="sxs-lookup"><span data-stu-id="e8ffd-135">5004, 5005</span></span>    | <span data-ttu-id="e8ffd-136">RTCP/RTP UDP</span><span class="sxs-lookup"><span data-stu-id="e8ffd-136">UDP RTCP/RTP</span></span>              | <span data-ttu-id="e8ffd-137">wmpnetwk.exe</span><span class="sxs-lookup"><span data-stu-id="e8ffd-137">wmpnetwk.exe</span></span>                    | <span data-ttu-id="e8ffd-138">in ingresso e in uscita</span><span class="sxs-lookup"><span data-stu-id="e8ffd-138">inbound and outbound</span></span> |
| <span data-ttu-id="e8ffd-139">50004-50013</span><span class="sxs-lookup"><span data-stu-id="e8ffd-139">50004 - 50013</span></span> | <span data-ttu-id="e8ffd-140">RTCP/RTP UDP</span><span class="sxs-lookup"><span data-stu-id="e8ffd-140">UDP RTCP/RTP</span></span>              | <span data-ttu-id="e8ffd-141">wmpnetwk.exe</span><span class="sxs-lookup"><span data-stu-id="e8ffd-141">wmpnetwk.exe</span></span>                    | <span data-ttu-id="e8ffd-142">in ingresso e in uscita</span><span class="sxs-lookup"><span data-stu-id="e8ffd-142">inbound and outbound</span></span> |
| <span data-ttu-id="e8ffd-143">1900</span><span class="sxs-lookup"><span data-stu-id="e8ffd-143">1900</span></span>          | <span data-ttu-id="e8ffd-144">SSDP UDP</span><span class="sxs-lookup"><span data-stu-id="e8ffd-144">UDP SSDP</span></span>                  | <span data-ttu-id="e8ffd-145">SSDPsrv in svchost.exe</span><span class="sxs-lookup"><span data-stu-id="e8ffd-145">SSDPsrv in svchost.exe</span></span>          | <span data-ttu-id="e8ffd-146">in ingresso e in uscita</span><span class="sxs-lookup"><span data-stu-id="e8ffd-146">inbound and outbound</span></span> |
| <span data-ttu-id="e8ffd-147">2869</span><span class="sxs-lookup"><span data-stu-id="e8ffd-147">2869</span></span>          | <span data-ttu-id="e8ffd-148">TCP SSDP, UPnP</span><span class="sxs-lookup"><span data-stu-id="e8ffd-148">TCP SSDP, UPnP</span></span>            | <span data-ttu-id="e8ffd-149">SSDPsrv/UPnPHost in svchost.exe</span><span class="sxs-lookup"><span data-stu-id="e8ffd-149">SSDPsrv/UPnPHost in svchost.exe</span></span> | <span data-ttu-id="e8ffd-150">in entrata</span><span class="sxs-lookup"><span data-stu-id="e8ffd-150">inbound</span></span>              |
| <span data-ttu-id="e8ffd-151">10280-10284</span><span class="sxs-lookup"><span data-stu-id="e8ffd-151">10280 - 10284</span></span> | <span data-ttu-id="e8ffd-152">Registrazione UDP WMDRM-ND</span><span class="sxs-lookup"><span data-stu-id="e8ffd-152">UDP WMDRM-ND registration</span></span> | <span data-ttu-id="e8ffd-153">wmpnetwk.exe</span><span class="sxs-lookup"><span data-stu-id="e8ffd-153">wmpnetwk.exe</span></span>                    | <span data-ttu-id="e8ffd-154">in ingresso e in uscita</span><span class="sxs-lookup"><span data-stu-id="e8ffd-154">inbound and outbound</span></span> |
| <span data-ttu-id="e8ffd-155">10243</span><span class="sxs-lookup"><span data-stu-id="e8ffd-155">10243</span></span>         | <span data-ttu-id="e8ffd-156">TCP HTTP</span><span class="sxs-lookup"><span data-stu-id="e8ffd-156">TCP HTTP</span></span>                  | <span data-ttu-id="e8ffd-157">wmpnetwk.exe</span><span class="sxs-lookup"><span data-stu-id="e8ffd-157">wmpnetwk.exe</span></span>                    | <span data-ttu-id="e8ffd-158">in entrata</span><span class="sxs-lookup"><span data-stu-id="e8ffd-158">inbound</span></span>              |
| <span data-ttu-id="e8ffd-159">2177</span><span class="sxs-lookup"><span data-stu-id="e8ffd-159">2177</span></span>          | <span data-ttu-id="e8ffd-160">QWAVE UDP TCP</span><span class="sxs-lookup"><span data-stu-id="e8ffd-160">TCP UDP qWAVE</span></span>             | <span data-ttu-id="e8ffd-161">svchost.exe</span><span class="sxs-lookup"><span data-stu-id="e8ffd-161">svchost.exe</span></span>                     | <span data-ttu-id="e8ffd-162">in ingresso e in uscita</span><span class="sxs-lookup"><span data-stu-id="e8ffd-162">inbound and outbound</span></span> |



 

<span data-ttu-id="e8ffd-163">In Windows Vista, se la voce del registro di sistema **AcceptedEULA** ha un valore pari a 1, è necessario aprire le porte seguenti.</span><span class="sxs-lookup"><span data-stu-id="e8ffd-163">On Windows Vista, if the **AcceptedEULA** registry entry has a value of 1, the following ports should be open.</span></span>



| <span data-ttu-id="e8ffd-164">Porta</span><span class="sxs-lookup"><span data-stu-id="e8ffd-164">Port</span></span>          | <span data-ttu-id="e8ffd-165">Protocollo</span><span class="sxs-lookup"><span data-stu-id="e8ffd-165">Protocol</span></span>       | <span data-ttu-id="e8ffd-166">Processo</span><span class="sxs-lookup"><span data-stu-id="e8ffd-166">Process</span></span>                         | <span data-ttu-id="e8ffd-167">Direzione</span><span class="sxs-lookup"><span data-stu-id="e8ffd-167">Direction</span></span>            |
|---------------|----------------|---------------------------------|----------------------|
| <span data-ttu-id="e8ffd-168">Tutte le porte UDP</span><span class="sxs-lookup"><span data-stu-id="e8ffd-168">All UDP ports</span></span> | <span data-ttu-id="e8ffd-169">RTP UDP, MSB</span><span class="sxs-lookup"><span data-stu-id="e8ffd-169">UDP RTP, MSB</span></span>   | <span data-ttu-id="e8ffd-170">wmplayer.exe, qualsiasi subnet</span><span class="sxs-lookup"><span data-stu-id="e8ffd-170">wmplayer.exe, any subnet</span></span>        | <span data-ttu-id="e8ffd-171">in entrata</span><span class="sxs-lookup"><span data-stu-id="e8ffd-171">inbound</span></span>              |
| <span data-ttu-id="e8ffd-172">1900</span><span class="sxs-lookup"><span data-stu-id="e8ffd-172">1900</span></span>          | <span data-ttu-id="e8ffd-173">SSDP UDP</span><span class="sxs-lookup"><span data-stu-id="e8ffd-173">UDP SSDP</span></span>       | <span data-ttu-id="e8ffd-174">SSDPsrv/UPnPHost in svchost.exe</span><span class="sxs-lookup"><span data-stu-id="e8ffd-174">SSDPsrv/UPnPHost in svchost.exe</span></span> | <span data-ttu-id="e8ffd-175">in ingresso e in uscita</span><span class="sxs-lookup"><span data-stu-id="e8ffd-175">inbound and outbound</span></span> |
| <span data-ttu-id="e8ffd-176">2869</span><span class="sxs-lookup"><span data-stu-id="e8ffd-176">2869</span></span>          | <span data-ttu-id="e8ffd-177">TCP SSDP, UPnP</span><span class="sxs-lookup"><span data-stu-id="e8ffd-177">TCP SSDP, UPnP</span></span> | <span data-ttu-id="e8ffd-178">SSDPsrv, UPnPHost</span><span class="sxs-lookup"><span data-stu-id="e8ffd-178">SSDPsrv, UPnPHost</span></span>               | <span data-ttu-id="e8ffd-179">in entrata</span><span class="sxs-lookup"><span data-stu-id="e8ffd-179">inbound</span></span>              |



 

<span data-ttu-id="e8ffd-180">In Microsoft Windows XP, se la voce del registro di sistema **WMPNSSFirewallPortsOpen** ha un valore pari a 1, è necessario aprire le porte seguenti.</span><span class="sxs-lookup"><span data-stu-id="e8ffd-180">On Microsoft Windows XP, if the **WMPNSSFirewallPortsOpen** registry entry has a value of 1, the following ports should be open.</span></span>



| <span data-ttu-id="e8ffd-181">Porta</span><span class="sxs-lookup"><span data-stu-id="e8ffd-181">Port</span></span>          | <span data-ttu-id="e8ffd-182">Protocollo</span><span class="sxs-lookup"><span data-stu-id="e8ffd-182">Protocol</span></span>                  | <span data-ttu-id="e8ffd-183">Processo</span><span class="sxs-lookup"><span data-stu-id="e8ffd-183">Process</span></span>                         | <span data-ttu-id="e8ffd-184">Direzione</span><span class="sxs-lookup"><span data-stu-id="e8ffd-184">Direction</span></span>            |
|---------------|---------------------------|---------------------------------|----------------------|
| <span data-ttu-id="e8ffd-185">1900</span><span class="sxs-lookup"><span data-stu-id="e8ffd-185">1900</span></span>          | <span data-ttu-id="e8ffd-186">SSDP UDP</span><span class="sxs-lookup"><span data-stu-id="e8ffd-186">UDP SSDP</span></span>                  | <span data-ttu-id="e8ffd-187">SSDPsrv in svchost.exe</span><span class="sxs-lookup"><span data-stu-id="e8ffd-187">SSDPsrv in svchost.exe</span></span>          | <span data-ttu-id="e8ffd-188">in ingresso e in uscita</span><span class="sxs-lookup"><span data-stu-id="e8ffd-188">inbound and outbound</span></span> |
| <span data-ttu-id="e8ffd-189">2869</span><span class="sxs-lookup"><span data-stu-id="e8ffd-189">2869</span></span>          | <span data-ttu-id="e8ffd-190">TCP SSDP, UPnP</span><span class="sxs-lookup"><span data-stu-id="e8ffd-190">TCP SSDP, UPnP</span></span>            | <span data-ttu-id="e8ffd-191">SSDPsrv/UPnPHost in svchost.exe</span><span class="sxs-lookup"><span data-stu-id="e8ffd-191">SSDPsrv/UPnPHost in svchost.exe</span></span> | <span data-ttu-id="e8ffd-192">in entrata</span><span class="sxs-lookup"><span data-stu-id="e8ffd-192">inbound</span></span>              |
| <span data-ttu-id="e8ffd-193">10280-10284</span><span class="sxs-lookup"><span data-stu-id="e8ffd-193">10280 - 10284</span></span> | <span data-ttu-id="e8ffd-194">Registrazione UDP WMDRM-ND</span><span class="sxs-lookup"><span data-stu-id="e8ffd-194">UDP WMDRM-ND registration</span></span> | <span data-ttu-id="e8ffd-195">wmpnetwk.exe</span><span class="sxs-lookup"><span data-stu-id="e8ffd-195">wmpnetwk.exe</span></span>                    | <span data-ttu-id="e8ffd-196">in ingresso e in uscita</span><span class="sxs-lookup"><span data-stu-id="e8ffd-196">inbound and outbound</span></span> |
| <span data-ttu-id="e8ffd-197">10243</span><span class="sxs-lookup"><span data-stu-id="e8ffd-197">10243</span></span>         | <span data-ttu-id="e8ffd-198">TCP HTTP</span><span class="sxs-lookup"><span data-stu-id="e8ffd-198">TCP HTTP</span></span>                  | <span data-ttu-id="e8ffd-199">wmpnetwk.exe</span><span class="sxs-lookup"><span data-stu-id="e8ffd-199">wmpnetwk.exe</span></span>                    | <span data-ttu-id="e8ffd-200">in entrata</span><span class="sxs-lookup"><span data-stu-id="e8ffd-200">inbound</span></span>              |



 

## <a name="related-topics"></a><span data-ttu-id="e8ffd-201">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e8ffd-201">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e8ffd-202">**Impostazioni del registro di sistema**</span><span class="sxs-lookup"><span data-stu-id="e8ffd-202">**Registry Settings**</span></span>](registry-settings.md)
</dt> </dl>

 

 




