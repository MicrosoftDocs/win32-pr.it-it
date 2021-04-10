---
title: Configurazione del registro di sistema per le allocazioni delle porte e l'associazione selettiva
description: A partire da Windows 2000, per impostare le associazioni è necessario usare un'utilità nel Resource Kit di Windows denominata Rpccfg.exe. Per ulteriori informazioni, consultare il Resource Kit di Windows per la versione appropriata del sistema operativo.
ms.assetid: a33b51e7-2ded-46bd-aadb-27cbd99e1029
keywords:
- RPC, attività, configurazione del registro di sistema per le allocazioni delle porte e associazione selettiva
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ef1749fab1beb8e637d208a7d7af64577066fe6
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/08/2020
ms.locfileid: "103963534"
---
# <a name="configuring-the-registry-for-port-allocations-and-selective-binding"></a><span data-ttu-id="89c10-105">Configurazione del registro di sistema per le allocazioni delle porte e l'associazione selettiva</span><span class="sxs-lookup"><span data-stu-id="89c10-105">Configuring the Registry for Port Allocations and Selective Binding</span></span>

<span data-ttu-id="89c10-106">A partire da Windows 2000, per impostare le associazioni è necessario usare un'utilità nel Resource Kit di Windows denominata Rpccfg.exe.</span><span class="sxs-lookup"><span data-stu-id="89c10-106">Starting with Windows 2000, a utility in the Windows Resource Kit called Rpccfg.exe should be used to set bindings.</span></span> <span data-ttu-id="89c10-107">Per ulteriori informazioni, consultare il Resource Kit di Windows per la versione appropriata del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="89c10-107">For more information, consult the Windows Resource Kit for the appropriate operating system version.</span></span>

<span data-ttu-id="89c10-108">Per le versioni di Windows precedenti a Windows 2000, le chiavi del registro di sistema nella tabella seguente specificano le impostazioni predefinite del sistema per l'allocazione delle porte dinamiche e per l'associazione alle schede di rete nei computer multihomed.</span><span class="sxs-lookup"><span data-stu-id="89c10-108">For versions of windows prior to Windows 2000, the registry keys in the following table specify the system defaults for dynamic port allocation and for binding to NICs on multihomed computers.</span></span> <span data-ttu-id="89c10-109">È necessario innanzitutto creare queste chiavi e quindi specificare le impostazioni appropriate.</span><span class="sxs-lookup"><span data-stu-id="89c10-109">You must first create these keys and then specify the appropriate settings.</span></span>

<span data-ttu-id="89c10-110">L'utilizzo della funzione [**RpcServerUseProtseqEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex) ha effetto su queste impostazioni.</span><span class="sxs-lookup"><span data-stu-id="89c10-110">Using the [**RpcServerUseProtseqEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex) function affects these settings.</span></span> <span data-ttu-id="89c10-111">Gli sviluppatori devono avere familiarità con le impostazioni del registro di sistema descritte in questa sezione e la funzione **RpcServerUseProtseqEx** quando si gestiscono le allocazioni delle porte.</span><span class="sxs-lookup"><span data-stu-id="89c10-111">Developers should be familiar with the registry settings explained in this section and the **RpcServerUseProtseqEx** function when managing port allocations.</span></span> <span data-ttu-id="89c10-112">Un esempio con tre applicazioni ipotetiche segue la tabella riportata di seguito e illustra il modo in cui queste impostazioni e la funzione **RpcServerUseProtseqEx** interagiscono.</span><span class="sxs-lookup"><span data-stu-id="89c10-112">An example with three hypothetical applications follows the table below, and illustrates how these settings and the **RpcServerUseProtseqEx** function interoperate.</span></span>

<span data-ttu-id="89c10-113">Se manca una chiave o se contiene un valore non valido, l'intera configurazione viene contrassegnata come non valida e tutte le chiamate **RpcServerUseProtseq \*** su [**ncacn \_ IP \_ TCP**](/windows/desktop/Midl/ncacn-ip-tcp) o [**ncadg \_ \_ UDP**](/windows/desktop/Midl/ncadg-ip-udp) avranno esito negativo.</span><span class="sxs-lookup"><span data-stu-id="89c10-113">If a key is missing or if it contains an invalid value, the entire configuration is marked as invalid, and all **RpcServerUseProtseq\*** calls over [**ncacn\_ip\_tcp**](/windows/desktop/Midl/ncacn-ip-tcp) or [**ncadg\_ip\_udp**](/windows/desktop/Midl/ncadg-ip-udp) will fail.</span></span>

> [!Note]  
> <span data-ttu-id="89c10-114">Le porte allocate a un processo restano allocate fino al termine del processo.</span><span class="sxs-lookup"><span data-stu-id="89c10-114">Ports allocated to a process remain allocated until that process dies.</span></span> <span data-ttu-id="89c10-115">Se tutte le porte disponibili sono in uso, la funzione restituisce \_ le \_ risorse RPC esaurite \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="89c10-115">If all available ports are in use, the function returns RPC\_S\_OUT\_OF\_RESOURCES.</span></span>

 



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="89c10-116">Chiave porta</span><span class="sxs-lookup"><span data-stu-id="89c10-116">Port key</span></span></th>
<th><span data-ttu-id="89c10-117">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="89c10-117">Data type</span></span></th>
<th><span data-ttu-id="89c10-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="89c10-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre data-space="preserve"><code>HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Rpc
            Internet
               Ports</code></pre></td>
<td><span data-ttu-id="89c10-119"><strong>REG_MULTI_SZ</strong></span><span class="sxs-lookup"><span data-stu-id="89c10-119"><strong>REG_MULTI_SZ</strong></span></span></td>
<td><span data-ttu-id="89c10-120">Specifica un set di intervalli di porte IP costituito da tutte le porte disponibili da Internet o da tutte le porte non disponibili in Internet.</span><span class="sxs-lookup"><span data-stu-id="89c10-120">Specifies a set of IP port ranges consisting of either all the ports available from the Internet or all the ports not available from the Internet.</span></span> <span data-ttu-id="89c10-121">Ogni stringa rappresenta una singola porta o un set di porte inclusivo (ad esempio, 1000-1050, 1984).</span><span class="sxs-lookup"><span data-stu-id="89c10-121">Each string represents a single port or an inclusive set of ports (for example,1000-1050, 1984).</span></span> <span data-ttu-id="89c10-122">Se le voci non rientrano nell'intervallo compreso tra 0 e 65535 o se non è possibile interpretare una stringa, il tempo di esecuzione RPC considererà l'intera configurazione come non valida.</span><span class="sxs-lookup"><span data-stu-id="89c10-122">If any entries are outside the range 0 to 65535, or if any string cannot be interpreted, the RPC run time will treat the entire configuration as invalid.</span></span></td>
</tr>
<tr class="even">
<td><pre data-space="preserve"><code>HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Rpc
            Internet
               PortsInternetAvailable</code></pre></td>
<td><span data-ttu-id="89c10-123"><strong>REG_SZ</strong></span><span class="sxs-lookup"><span data-stu-id="89c10-123"><strong>REG_SZ</strong></span></span></td>
<td><span data-ttu-id="89c10-124">Y o N (senza distinzione tra maiuscole e minuscole).</span><span class="sxs-lookup"><span data-stu-id="89c10-124">Y or N (not case-sensitive).</span></span> <span data-ttu-id="89c10-125">Se Y, le porte elencate nella chiave porte sono tutte le porte disponibili su Internet nel computer.</span><span class="sxs-lookup"><span data-stu-id="89c10-125">If Y, the ports listed in the Ports key are all the Internet-available ports on that computer.</span></span> <span data-ttu-id="89c10-126">Se N, le porte elencate nella chiave porte sono tutte le porte che non sono disponibili su Internet.</span><span class="sxs-lookup"><span data-stu-id="89c10-126">If N, the ports listed in the Ports key are all those ports that are not Internet-available.</span></span></td>
</tr>
<tr class="odd">
<td><pre data-space="preserve"><code>HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Rpc
            Internet
               UseInternetPorts</code></pre></td>
<td><span data-ttu-id="89c10-127"><strong>REG_SZ</strong></span><span class="sxs-lookup"><span data-stu-id="89c10-127"><strong>REG_SZ</strong></span></span></td>
<td><span data-ttu-id="89c10-128">Y o N (senza distinzione tra maiuscole e minuscole).</span><span class="sxs-lookup"><span data-stu-id="89c10-128">Y or N (not case-sensitive).</span></span> <span data-ttu-id="89c10-129">Specifica i criteri predefiniti di sistema.</span><span class="sxs-lookup"><span data-stu-id="89c10-129">Specifies the system default policy.</span></span> <span data-ttu-id="89c10-130">Se Y, ai processi che usano l'impostazione predefinita verranno assegnate le porte dal set di porte disponibili per Internet, come definito in precedenza.</span><span class="sxs-lookup"><span data-stu-id="89c10-130">If Y, the processes using the default will be assigned ports from the set of Internet-available ports, as defined above.</span></span> <span data-ttu-id="89c10-131">Se N, i processi che utilizzano il valore predefinito verranno assegnati alle porte dal set di porte solo Intranet.</span><span class="sxs-lookup"><span data-stu-id="89c10-131">If N, processes using the default will be assigned ports from the set of intranet-only ports.</span></span></td>
</tr>
<tr class="even">
<td><pre data-space="preserve"><code>HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Services
            Rpc
               Linkage
                  Bind</code></pre></td>
<td><span data-ttu-id="89c10-132"><strong>REG_MULTI_SZ</strong></span><span class="sxs-lookup"><span data-stu-id="89c10-132"><strong>REG_MULTI_SZ</strong></span></span></td>
<td><span data-ttu-id="89c10-133">Elenca i nomi dei dispositivi di tutte le schede di rete su cui eseguire il binding per impostazione predefinita (ad esempio, \Device\AMDPCN1).</span><span class="sxs-lookup"><span data-stu-id="89c10-133">Lists the device names of all the NICs on which to bind by default (for example, \Device\AMDPCN1).</span></span> <span data-ttu-id="89c10-134">Se la chiave non esiste, il server eseguirà l'associazione a tutte le schede di rete.</span><span class="sxs-lookup"><span data-stu-id="89c10-134">If the key does not exist, the server will bind to all NICs.</span></span> <span data-ttu-id="89c10-135">Se la chiave esiste, il server verrà associato alle schede di rete specificate nella chiave, a meno che il campo NICFlags non sia impostato su RPC_C_BIND_TO_ALL_NICS.</span><span class="sxs-lookup"><span data-stu-id="89c10-135">If the key does exist, the server will bind to the NICs specified in the key, unless the NICFlags field is set to RPC_C_BIND_TO_ALL_NICS.</span></span> <span data-ttu-id="89c10-136">Se la chiave ha un valore null ( &quot; &quot; ), la configurazione verrà contrassegnata come non valida e tutte le chiamate a <strong>RpcServerUseProtseq \*</strong> over <a href="/windows/desktop/Midl/ncacn-ip-tcp"><strong>ncacn_ip_tcp</strong></a> o <a href="/windows/desktop/Midl/ncadg-ip-udp"><strong>ncadg_ip_udp</strong></a> avranno esito negativo.</span><span class="sxs-lookup"><span data-stu-id="89c10-136">If the key has a null (&quot;&quot;) value, the configuration will be marked as invalid and all calls to <strong>RpcServerUseProtseq\*</strong> over <a href="/windows/desktop/Midl/ncacn-ip-tcp"><strong>ncacn_ip_tcp</strong></a> or <a href="/windows/desktop/Midl/ncadg-ip-udp"><strong>ncadg_ip_udp</strong></a> will fail.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="89c10-137">La tabella seguente illustra il modo in cui le impostazioni definite nella tabella precedente hanno effetto su tre applicazioni di esempio e sulle modalità di utilizzo delle impostazioni applicate mediante la funzione [**RpcServerUseProtseqEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex) .</span><span class="sxs-lookup"><span data-stu-id="89c10-137">The following table illustrates how three sample applications are affected by the settings defined in the previous table, and how settings applied using the [**RpcServerUseProtseqEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex) function are also affected.</span></span>

<span data-ttu-id="89c10-138">In questo esempio vengono considerate tre applicazioni ipotetiche:</span><span class="sxs-lookup"><span data-stu-id="89c10-138">In this example, three hypothetical applications are considered:</span></span>

-   <span data-ttu-id="89c10-139">Internetapp: questa applicazione è destinata all'esposizione a Internet e ha specificato il linguaggio RPC C per l' \_ \_ utilizzo della \_ \_ porta Internet nel membro **EndpointFlags** della struttura dei [**\_ criteri RPC**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_policy) passata alla funzione [**RpcServerUseProtseqEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex) .</span><span class="sxs-lookup"><span data-stu-id="89c10-139">InternetApp: This application is intended for exposure to the Internet, and has specified RPC\_C\_USE\_INTERNET\_PORT in the **EndpointFlags** member of the [**RPC\_POLICY**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_policy) structure passed to the [**RpcServerUseProtseqEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex) function.</span></span>
-   <span data-ttu-id="89c10-140">LocalApp: questa applicazione non è progettata per l'esposizione a Internet e ha specificato che RPC \_ C \_ Usa \_ la \_ porta Intranet nel membro **EndpointFlags** della struttura [**dei \_ criteri RPC**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_policy) passata alla funzione [**RpcServerUseProtseqEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex) .</span><span class="sxs-lookup"><span data-stu-id="89c10-140">LocalApp: This application is not intended for exposure to the Internet, and has specified RPC\_C\_USE\_INTRANET\_PORT in the **EndpointFlags** member of the [**RPC\_POLICY**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_policy) structure passed to the [**RpcServerUseProtseqEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex) function.</span></span>
-   <span data-ttu-id="89c10-141">File DefaultApp: questa applicazione specifica zero nel membro **EndpointFlags** della struttura dei [**\_ criteri RPC**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_policy) passata alla funzione [**RpcServerUseProtseqEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex) .</span><span class="sxs-lookup"><span data-stu-id="89c10-141">DefaultApp: This application specifies zero in the **EndpointFlags** member of the [**RPC\_POLICY**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_policy) structure passed to the [**RpcServerUseProtseqEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex) function.</span></span>

<span data-ttu-id="89c10-142">La tabella seguente illustra l'effetto di queste impostazioni in base ai valori specificati nelle voci del registro di sistema descritte nella tabella precedente.</span><span class="sxs-lookup"><span data-stu-id="89c10-142">The following table explains the impact these settings have based on values specified in the registry entries explained in the previous table.</span></span> <span data-ttu-id="89c10-143">Per considerazioni sulla formattazione, vengono assegnati i codici seguenti:</span><span class="sxs-lookup"><span data-stu-id="89c10-143">For formatting considerations, the following codes are assigned:</span></span>

<span data-ttu-id="89c10-144">PIA = valore chiave PortsInternetAvailable</span><span class="sxs-lookup"><span data-stu-id="89c10-144">PIA = PortsInternetAvailable Key value</span></span>

<span data-ttu-id="89c10-145">UIP = valore chiave UseInternetPorts</span><span class="sxs-lookup"><span data-stu-id="89c10-145">UIP = UseInternetPorts Key value</span></span>

<span data-ttu-id="89c10-146">Il valore della chiave Ports, a scopo di questo esempio, è 5000-5100 per ogni voce.</span><span class="sxs-lookup"><span data-stu-id="89c10-146">The value of the Ports key, for sake of this example, is 5000-5100 for each entry.</span></span>



| <span data-ttu-id="89c10-147">Applicazione</span><span class="sxs-lookup"><span data-stu-id="89c10-147">Application</span></span> | <span data-ttu-id="89c10-148">PIA</span><span class="sxs-lookup"><span data-stu-id="89c10-148">PIA</span></span> | <span data-ttu-id="89c10-149">UIP</span><span class="sxs-lookup"><span data-stu-id="89c10-149">UIP</span></span> | <span data-ttu-id="89c10-150">Risultato</span><span class="sxs-lookup"><span data-stu-id="89c10-150">Result</span></span>                                  |
|-------------|-----|-----|-----------------------------------------|
| <span data-ttu-id="89c10-151">Internetapp</span><span class="sxs-lookup"><span data-stu-id="89c10-151">InternetApp</span></span> | <span data-ttu-id="89c10-152">S</span><span class="sxs-lookup"><span data-stu-id="89c10-152">Y</span></span>   | <span data-ttu-id="89c10-153">S</span><span class="sxs-lookup"><span data-stu-id="89c10-153">Y</span></span>   | <span data-ttu-id="89c10-154">Usa le porte comprese tra 5000 e 5100</span><span class="sxs-lookup"><span data-stu-id="89c10-154">Uses ports between 5000 and 5100</span></span>        |
| <span data-ttu-id="89c10-155">LocalApp</span><span class="sxs-lookup"><span data-stu-id="89c10-155">LocalApp</span></span>    | <span data-ttu-id="89c10-156">S</span><span class="sxs-lookup"><span data-stu-id="89c10-156">Y</span></span>   | <span data-ttu-id="89c10-157">S</span><span class="sxs-lookup"><span data-stu-id="89c10-157">Y</span></span>   | <span data-ttu-id="89c10-158">Usa una porta al di fuori dell'intervallo 5000-5100</span><span class="sxs-lookup"><span data-stu-id="89c10-158">Uses a port outside the 5000-5100 range</span></span> |
| <span data-ttu-id="89c10-159">File DefaultApp</span><span class="sxs-lookup"><span data-stu-id="89c10-159">DefaultApp</span></span>  | <span data-ttu-id="89c10-160">S</span><span class="sxs-lookup"><span data-stu-id="89c10-160">Y</span></span>   | <span data-ttu-id="89c10-161">S</span><span class="sxs-lookup"><span data-stu-id="89c10-161">Y</span></span>   | <span data-ttu-id="89c10-162">Usa le porte comprese tra 5000 e 5100</span><span class="sxs-lookup"><span data-stu-id="89c10-162">Uses ports between 5000 and 5100</span></span>        |
| <span data-ttu-id="89c10-163">Internetapp</span><span class="sxs-lookup"><span data-stu-id="89c10-163">InternetApp</span></span> | <span data-ttu-id="89c10-164">S</span><span class="sxs-lookup"><span data-stu-id="89c10-164">Y</span></span>   | <span data-ttu-id="89c10-165">N</span><span class="sxs-lookup"><span data-stu-id="89c10-165">N</span></span>   | <span data-ttu-id="89c10-166">Usa le porte comprese tra 5000 e 5100</span><span class="sxs-lookup"><span data-stu-id="89c10-166">Uses ports between 5000 and 5100</span></span>        |
| <span data-ttu-id="89c10-167">LocalApp</span><span class="sxs-lookup"><span data-stu-id="89c10-167">LocalApp</span></span>    | <span data-ttu-id="89c10-168">S</span><span class="sxs-lookup"><span data-stu-id="89c10-168">Y</span></span>   | <span data-ttu-id="89c10-169">N</span><span class="sxs-lookup"><span data-stu-id="89c10-169">N</span></span>   | <span data-ttu-id="89c10-170">Usa una porta al di fuori dell'intervallo 5000-5100</span><span class="sxs-lookup"><span data-stu-id="89c10-170">Uses a port outside the 5000-5100 range</span></span> |
| <span data-ttu-id="89c10-171">File DefaultApp</span><span class="sxs-lookup"><span data-stu-id="89c10-171">DefaultApp</span></span>  | <span data-ttu-id="89c10-172">S</span><span class="sxs-lookup"><span data-stu-id="89c10-172">Y</span></span>   | <span data-ttu-id="89c10-173">N</span><span class="sxs-lookup"><span data-stu-id="89c10-173">N</span></span>   | <span data-ttu-id="89c10-174">Usa una porta al di fuori dell'intervallo 5000-5100</span><span class="sxs-lookup"><span data-stu-id="89c10-174">Uses a port outside the 5000-5100 range</span></span> |
| <span data-ttu-id="89c10-175">Internetapp</span><span class="sxs-lookup"><span data-stu-id="89c10-175">InternetApp</span></span> | <span data-ttu-id="89c10-176">N</span><span class="sxs-lookup"><span data-stu-id="89c10-176">N</span></span>   | <span data-ttu-id="89c10-177">S</span><span class="sxs-lookup"><span data-stu-id="89c10-177">Y</span></span>   | <span data-ttu-id="89c10-178">Usa una porta al di fuori dell'intervallo 5000-5100</span><span class="sxs-lookup"><span data-stu-id="89c10-178">Uses a port outside the 5000-5100 range</span></span> |
| <span data-ttu-id="89c10-179">LocalApp</span><span class="sxs-lookup"><span data-stu-id="89c10-179">LocalApp</span></span>    | <span data-ttu-id="89c10-180">N</span><span class="sxs-lookup"><span data-stu-id="89c10-180">N</span></span>   | <span data-ttu-id="89c10-181">S</span><span class="sxs-lookup"><span data-stu-id="89c10-181">Y</span></span>   | <span data-ttu-id="89c10-182">Usa le porte comprese tra 5000 e 5100</span><span class="sxs-lookup"><span data-stu-id="89c10-182">Uses ports between 5000 and 5100</span></span>        |
| <span data-ttu-id="89c10-183">File DefaultApp</span><span class="sxs-lookup"><span data-stu-id="89c10-183">DefaultApp</span></span>  | <span data-ttu-id="89c10-184">N</span><span class="sxs-lookup"><span data-stu-id="89c10-184">N</span></span>   | <span data-ttu-id="89c10-185">S</span><span class="sxs-lookup"><span data-stu-id="89c10-185">Y</span></span>   | <span data-ttu-id="89c10-186">Usa una porta al di fuori dell'intervallo 5000-5100</span><span class="sxs-lookup"><span data-stu-id="89c10-186">Uses a port outside the 5000-5100 range</span></span> |
| <span data-ttu-id="89c10-187">Internetapp</span><span class="sxs-lookup"><span data-stu-id="89c10-187">InternetApp</span></span> | <span data-ttu-id="89c10-188">N</span><span class="sxs-lookup"><span data-stu-id="89c10-188">N</span></span>   | <span data-ttu-id="89c10-189">N</span><span class="sxs-lookup"><span data-stu-id="89c10-189">N</span></span>   | <span data-ttu-id="89c10-190">Usa una porta al di fuori dell'intervallo 5000-5100</span><span class="sxs-lookup"><span data-stu-id="89c10-190">Uses a port outside the 5000-5100 range</span></span> |
| <span data-ttu-id="89c10-191">LocalApp</span><span class="sxs-lookup"><span data-stu-id="89c10-191">LocalApp</span></span>    | <span data-ttu-id="89c10-192">N</span><span class="sxs-lookup"><span data-stu-id="89c10-192">N</span></span>   | <span data-ttu-id="89c10-193">N</span><span class="sxs-lookup"><span data-stu-id="89c10-193">N</span></span>   | <span data-ttu-id="89c10-194">Usa le porte comprese tra 5000 e 5100</span><span class="sxs-lookup"><span data-stu-id="89c10-194">Uses ports between 5000 and 5100</span></span>        |
| <span data-ttu-id="89c10-195">File DefaultApp</span><span class="sxs-lookup"><span data-stu-id="89c10-195">DefaultApp</span></span>  | <span data-ttu-id="89c10-196">N</span><span class="sxs-lookup"><span data-stu-id="89c10-196">N</span></span>   | <span data-ttu-id="89c10-197">N</span><span class="sxs-lookup"><span data-stu-id="89c10-197">N</span></span>   | <span data-ttu-id="89c10-198">Usa le porte comprese tra 5000 e 5100</span><span class="sxs-lookup"><span data-stu-id="89c10-198">Uses ports between 5000 and 5100</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="89c10-199">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="89c10-199">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="89c10-200">**\_criterio RPC**</span><span class="sxs-lookup"><span data-stu-id="89c10-200">**RPC\_POLICY**</span></span>](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_policy)
</dt> <dt>

[<span data-ttu-id="89c10-201">**RpcServerUseAllProtseqsEx**</span><span class="sxs-lookup"><span data-stu-id="89c10-201">**RpcServerUseAllProtseqsEx**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqsex)
</dt> <dt>

[<span data-ttu-id="89c10-202">**RpcServerUseAllProtseqsIfEx**</span><span class="sxs-lookup"><span data-stu-id="89c10-202">**RpcServerUseAllProtseqsIfEx**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqsifex)
</dt> <dt>

[<span data-ttu-id="89c10-203">**RpcServerUseProtseqEx**</span><span class="sxs-lookup"><span data-stu-id="89c10-203">**RpcServerUseProtseqEx**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex)
</dt> <dt>

[<span data-ttu-id="89c10-204">**RpcServerUseProtseqEpEx**</span><span class="sxs-lookup"><span data-stu-id="89c10-204">**RpcServerUseProtseqEpEx**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqepex)
</dt> <dt>

[<span data-ttu-id="89c10-205">**RpcServerUseProtseqIfEx**</span><span class="sxs-lookup"><span data-stu-id="89c10-205">**RpcServerUseProtseqIfEx**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqifex)
</dt> <dt>

[<span data-ttu-id="89c10-206">**\_TCP IP \_ ncacn**</span><span class="sxs-lookup"><span data-stu-id="89c10-206">**ncacn\_ip\_tcp**</span></span>](/windows/desktop/Midl/ncacn-ip-tcp)
</dt> <dt>

[<span data-ttu-id="89c10-207">**\_UDP IP \_ ncadg**</span><span class="sxs-lookup"><span data-stu-id="89c10-207">**ncadg\_ip\_udp**</span></span>](/windows/desktop/Midl/ncadg-ip-udp)
</dt> </dl>

 

 