---
description: La \_ classe Win32 ServerFeature rappresenta le funzionalità installate in un computer che esegue Windows Server.
ms.assetid: fe3bb95c-7f69-47b5-9c3d-771cdc3ed9ca
ms.tgt_platform: multiple
title: Classe Win32_ServerFeature
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ServerFeature
- Win32_ServerFeature.ID
- Win32_ServerFeature.ParentID
- Win32_ServerFeature.Name
api_type:
- DllExport
api_location:
- ServerCompProv.dll
ms.openlocfilehash: 1be8a2ea1d646e9d882febc7c8eba08b69bb69f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318171"
---
# <a name="win32_serverfeature-class"></a><span data-ttu-id="9827c-103">Win32 \_ ServerFeature (classe)</span><span class="sxs-lookup"><span data-stu-id="9827c-103">Win32\_ServerFeature class</span></span>

<span data-ttu-id="9827c-104">\[La classe **Win32 \_ ServerFeature** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="9827c-104">\[The **Win32\_ServerFeature** class is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="9827c-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="9827c-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="9827c-106">Usare invece le [classi del provider deploymentProvider di ServerManager](/previous-versions/windows/desktop/srvmgrdeployprov/server-manager-deployment).\]</span><span class="sxs-lookup"><span data-stu-id="9827c-106">Instead, use the [ServerManager Deploymentprovider Provider Classes](/previous-versions/windows/desktop/srvmgrdeployprov/server-manager-deployment).\]</span></span>

<span data-ttu-id="9827c-107">La classe **Win32 \_ ServerFeature** rappresenta le funzionalità installate in un computer che esegue Windows Server.</span><span class="sxs-lookup"><span data-stu-id="9827c-107">The **Win32\_ServerFeature** class represents the features installed on a computer running Windows Server.</span></span>

<span data-ttu-id="9827c-108">Questa classe può essere utilizzata da sviluppatori e amministratori che devono automatizzare il processo di determinazione delle funzionalità installate in un set di computer server.</span><span class="sxs-lookup"><span data-stu-id="9827c-108">This class can be used by developers and administrators who need to automate the process of determining the features installed on a set of server computers.</span></span> <span data-ttu-id="9827c-109">Le istanze di questa classe non sono disponibili nei computer client.</span><span class="sxs-lookup"><span data-stu-id="9827c-109">Instances of this class are not available on client computers.</span></span>

## <a name="syntax"></a><span data-ttu-id="9827c-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9827c-110">Syntax</span></span>

``` syntax
[Deprecated("No value"), Dynamic, Provider("ServerFeatureProvider"), AMENDMENT]
class Win32_ServerFeature
{
  uint32 ID;
  uint32 ParentID;
  string Name;
};
```

## <a name="members"></a><span data-ttu-id="9827c-111">Members</span><span class="sxs-lookup"><span data-stu-id="9827c-111">Members</span></span>

<span data-ttu-id="9827c-112">La classe **Win32 \_ ServerFeature** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="9827c-112">The **Win32\_ServerFeature** class has these types of members:</span></span>

-   [<span data-ttu-id="9827c-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="9827c-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9827c-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="9827c-114">Properties</span></span>

<span data-ttu-id="9827c-115">La classe **Win32 \_ ServerFeature** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="9827c-115">The **Win32\_ServerFeature** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9827c-116">**ID**</span><span class="sxs-lookup"><span data-stu-id="9827c-116">**ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9827c-117">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9827c-117">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9827c-118">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="9827c-118">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="9827c-119">Qualificatori: [**chiave**](key-qualifier.md), [**Not \_ null**](optional-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="9827c-119">Qualifiers: [**Key**](key-qualifier.md), [**Not\_Null**](optional-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="9827c-120">ID funzionalità server.</span><span class="sxs-lookup"><span data-stu-id="9827c-120">Server feature ID.</span></span> <span data-ttu-id="9827c-121">Nell'elenco seguente vengono illustrati i valori possibili della proprietà ID:</span><span class="sxs-lookup"><span data-stu-id="9827c-121">The following list shows the possible values of the ID property:</span></span>



<span data-ttu-id="9827c-122">Valore</span><span class="sxs-lookup"><span data-stu-id="9827c-122">Value</span></span>

<span data-ttu-id="9827c-123">Nome</span><span class="sxs-lookup"><span data-stu-id="9827c-123">Name</span></span>

<span data-ttu-id="9827c-124">1</span><span class="sxs-lookup"><span data-stu-id="9827c-124">1</span></span>

[<span data-ttu-id="9827c-125">Server applicazioni</span><span class="sxs-lookup"><span data-stu-id="9827c-125">Application Server</span></span>](/windows)

<span data-ttu-id="9827c-126">2</span><span class="sxs-lookup"><span data-stu-id="9827c-126">2</span></span>

<span data-ttu-id="9827c-127">Server Web (IIS)</span><span class="sxs-lookup"><span data-stu-id="9827c-127">Web Server (IIS)</span></span>

<span data-ttu-id="9827c-128">3</span><span class="sxs-lookup"><span data-stu-id="9827c-128">3</span></span>

[<span data-ttu-id="9827c-129">Servizi flussi multimediali</span><span class="sxs-lookup"><span data-stu-id="9827c-129">Streaming Media Services</span></span>](/windows)

<span data-ttu-id="9827c-130">5</span><span class="sxs-lookup"><span data-stu-id="9827c-130">5</span></span>

<span data-ttu-id="9827c-131">Server fax</span><span class="sxs-lookup"><span data-stu-id="9827c-131">Fax Server</span></span>

<span data-ttu-id="9827c-132">6</span><span class="sxs-lookup"><span data-stu-id="9827c-132">6</span></span>

<span data-ttu-id="9827c-133">Servizi file e iSCSI</span><span class="sxs-lookup"><span data-stu-id="9827c-133">File and iSCSI Services</span></span><br/> [<span data-ttu-id="9827c-134">modifica nome</span><span class="sxs-lookup"><span data-stu-id="9827c-134">name change</span></span>](/windows)<br/>

<span data-ttu-id="9827c-135">7</span><span class="sxs-lookup"><span data-stu-id="9827c-135">7</span></span>

<span data-ttu-id="9827c-136">Servizi di stampa e digitalizzazione</span><span class="sxs-lookup"><span data-stu-id="9827c-136">Print and Document Services</span></span><br/> [<span data-ttu-id="9827c-137">modifica nome</span><span class="sxs-lookup"><span data-stu-id="9827c-137">name change</span></span>](/windows)<br/>

<span data-ttu-id="9827c-138">8</span><span class="sxs-lookup"><span data-stu-id="9827c-138">8</span></span>

[<span data-ttu-id="9827c-139">Active Directory Federation Services</span><span class="sxs-lookup"><span data-stu-id="9827c-139">Active Directory Federation Services</span></span>](/windows)

<span data-ttu-id="9827c-140">9</span><span class="sxs-lookup"><span data-stu-id="9827c-140">9</span></span>

<span data-ttu-id="9827c-141">Active Directory Lightweight Directory Services</span><span class="sxs-lookup"><span data-stu-id="9827c-141">Active Directory Lightweight Directory Services</span></span>

<span data-ttu-id="9827c-142">10</span><span class="sxs-lookup"><span data-stu-id="9827c-142">10</span></span>

<span data-ttu-id="9827c-143">Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="9827c-143">Active Directory Domain Services</span></span>

<span data-ttu-id="9827c-144">11</span><span class="sxs-lookup"><span data-stu-id="9827c-144">11</span></span>

[<span data-ttu-id="9827c-145">Servizi UDDI</span><span class="sxs-lookup"><span data-stu-id="9827c-145">UDDI Services</span></span>](/windows)<br/>

<span data-ttu-id="9827c-146">12</span><span class="sxs-lookup"><span data-stu-id="9827c-146">12</span></span>

[<span data-ttu-id="9827c-147">Server DHCP</span><span class="sxs-lookup"><span data-stu-id="9827c-147">DHCP Server</span></span>](/windows)

<span data-ttu-id="9827c-148">13</span><span class="sxs-lookup"><span data-stu-id="9827c-148">13</span></span>

[<span data-ttu-id="9827c-149">Server DNS</span><span class="sxs-lookup"><span data-stu-id="9827c-149">DNS Server</span></span>](/windows)

<span data-ttu-id="9827c-150">14</span><span class="sxs-lookup"><span data-stu-id="9827c-150">14</span></span>

<span data-ttu-id="9827c-151">Servizi di accesso e criteri di rete</span><span class="sxs-lookup"><span data-stu-id="9827c-151">Network Policy and Access Services</span></span>

<span data-ttu-id="9827c-152">16</span><span class="sxs-lookup"><span data-stu-id="9827c-152">16</span></span>

<span data-ttu-id="9827c-153">Servizi certificati Active Directory</span><span class="sxs-lookup"><span data-stu-id="9827c-153">Active Directory Certificate Services</span></span>

<span data-ttu-id="9827c-154">17</span><span class="sxs-lookup"><span data-stu-id="9827c-154">17</span></span>

<span data-ttu-id="9827c-155">Active Directory Rights Management Services</span><span class="sxs-lookup"><span data-stu-id="9827c-155">Active Directory Rights Management Services</span></span>

<span data-ttu-id="9827c-156">18</span><span class="sxs-lookup"><span data-stu-id="9827c-156">18</span></span>

[<span data-ttu-id="9827c-157">Servizi Desktop remoto</span><span class="sxs-lookup"><span data-stu-id="9827c-157">Remote Desktop Services</span></span>](/windows)<br/> [<span data-ttu-id="9827c-158">modifica nome</span><span class="sxs-lookup"><span data-stu-id="9827c-158">name change</span></span>](/windows)<br/>

<span data-ttu-id="9827c-159">19</span><span class="sxs-lookup"><span data-stu-id="9827c-159">19</span></span>

<span data-ttu-id="9827c-160">Servizi di distribuzione Windows</span><span class="sxs-lookup"><span data-stu-id="9827c-160">Windows Deployment Services</span></span>

<span data-ttu-id="9827c-161">20</span><span class="sxs-lookup"><span data-stu-id="9827c-161">20</span></span>

<span data-ttu-id="9827c-162">Hyper-V</span><span class="sxs-lookup"><span data-stu-id="9827c-162">Hyper-V</span></span>

<span data-ttu-id="9827c-163">21</span><span class="sxs-lookup"><span data-stu-id="9827c-163">21</span></span>

[<span data-ttu-id="9827c-164">Windows Server Update Services</span><span class="sxs-lookup"><span data-stu-id="9827c-164">Windows Server Update Services</span></span>](/windows)

<span data-ttu-id="9827c-165">33</span><span class="sxs-lookup"><span data-stu-id="9827c-165">33</span></span>

[<span data-ttu-id="9827c-166">Clustering di failover</span><span class="sxs-lookup"><span data-stu-id="9827c-166">Failover Clustering</span></span>](/windows)

<span data-ttu-id="9827c-167">34</span><span class="sxs-lookup"><span data-stu-id="9827c-167">34</span></span>

[<span data-ttu-id="9827c-168">Bilanciamento del carico di rete</span><span class="sxs-lookup"><span data-stu-id="9827c-168">Network Load Balancing</span></span>](/windows)

<span data-ttu-id="9827c-169">36</span><span class="sxs-lookup"><span data-stu-id="9827c-169">36</span></span>

[<span data-ttu-id="9827c-170">Funzionalità di .NET Framework 3.5.1</span><span class="sxs-lookup"><span data-stu-id="9827c-170">.NET Framework 3.5.1 Features</span></span>](/windows)<br/> [<span data-ttu-id="9827c-171">modifica nome</span><span class="sxs-lookup"><span data-stu-id="9827c-171">name change</span></span>](/windows)<br/>

<span data-ttu-id="9827c-172">37</span><span class="sxs-lookup"><span data-stu-id="9827c-172">37</span></span>

[<span data-ttu-id="9827c-173">Gestione risorse di sistema Windows</span><span class="sxs-lookup"><span data-stu-id="9827c-173">Windows System Resource Manager</span></span>](/windows)

<span data-ttu-id="9827c-174">38</span><span class="sxs-lookup"><span data-stu-id="9827c-174">38</span></span>

<span data-ttu-id="9827c-175">Servizio LAN Wireless</span><span class="sxs-lookup"><span data-stu-id="9827c-175">Wireless LAN Service</span></span>

<span data-ttu-id="9827c-176">39</span><span class="sxs-lookup"><span data-stu-id="9827c-176">39</span></span>

[<span data-ttu-id="9827c-177">Funzionalità di Windows Server Backup</span><span class="sxs-lookup"><span data-stu-id="9827c-177">Windows Server Backup Features</span></span>](/windows)

<span data-ttu-id="9827c-178">40</span><span class="sxs-lookup"><span data-stu-id="9827c-178">40</span></span>

<span data-ttu-id="9827c-179">Server WINS</span><span class="sxs-lookup"><span data-stu-id="9827c-179">WINS Server</span></span>

<span data-ttu-id="9827c-180">41</span><span class="sxs-lookup"><span data-stu-id="9827c-180">41</span></span>

<span data-ttu-id="9827c-181">Servizio Attivazione dei processi Windows</span><span class="sxs-lookup"><span data-stu-id="9827c-181">Windows Process Activation Service</span></span>

<span data-ttu-id="9827c-182">42</span><span class="sxs-lookup"><span data-stu-id="9827c-182">42</span></span>

[<span data-ttu-id="9827c-183">Assistenza remota</span><span class="sxs-lookup"><span data-stu-id="9827c-183">Remote Assistance</span></span>](/windows)

<span data-ttu-id="9827c-184">43</span><span class="sxs-lookup"><span data-stu-id="9827c-184">43</span></span>

<span data-ttu-id="9827c-185">Servizi TCP/IP semplificati</span><span class="sxs-lookup"><span data-stu-id="9827c-185">Simple TCP/IP Services</span></span>

<span data-ttu-id="9827c-186">44</span><span class="sxs-lookup"><span data-stu-id="9827c-186">44</span></span>

[<span data-ttu-id="9827c-187">Client Telnet</span><span class="sxs-lookup"><span data-stu-id="9827c-187">Telnet Client</span></span>](/windows)

<span data-ttu-id="9827c-188">45</span><span class="sxs-lookup"><span data-stu-id="9827c-188">45</span></span>

[<span data-ttu-id="9827c-189">Server Telnet</span><span class="sxs-lookup"><span data-stu-id="9827c-189">Telnet Server</span></span>](/windows)

<span data-ttu-id="9827c-190">46</span><span class="sxs-lookup"><span data-stu-id="9827c-190">46</span></span>

[<span data-ttu-id="9827c-191">Sottosistema per applicazioni basate su UNIX</span><span class="sxs-lookup"><span data-stu-id="9827c-191">Subsystem For Unix-based Applications</span></span>](/windows)

<span data-ttu-id="9827c-192">47</span><span class="sxs-lookup"><span data-stu-id="9827c-192">47</span></span>

<span data-ttu-id="9827c-193">Proxy RPC su HTTP</span><span class="sxs-lookup"><span data-stu-id="9827c-193">RPC Over HTTP Proxy</span></span>

<span data-ttu-id="9827c-194">48</span><span class="sxs-lookup"><span data-stu-id="9827c-194">48</span></span>

<span data-ttu-id="9827c-195">Server SMTP</span><span class="sxs-lookup"><span data-stu-id="9827c-195">SMTP Server</span></span>

<span data-ttu-id="9827c-196">49</span><span class="sxs-lookup"><span data-stu-id="9827c-196">49</span></span>

<span data-ttu-id="9827c-197">accodamento messaggi</span><span class="sxs-lookup"><span data-stu-id="9827c-197">Message Queuing</span></span>

<span data-ttu-id="9827c-198">51</span><span class="sxs-lookup"><span data-stu-id="9827c-198">51</span></span>

[<span data-ttu-id="9827c-199">Database interno di Windows</span><span class="sxs-lookup"><span data-stu-id="9827c-199">Windows Internal Database</span></span>](/windows)

<span data-ttu-id="9827c-200">52</span><span class="sxs-lookup"><span data-stu-id="9827c-200">52</span></span>

[<span data-ttu-id="9827c-201">Gestione archivi San</span><span class="sxs-lookup"><span data-stu-id="9827c-201">Storage Manager For SANs</span></span>](/windows)

<span data-ttu-id="9827c-202">53</span><span class="sxs-lookup"><span data-stu-id="9827c-202">53</span></span>

<span data-ttu-id="9827c-203">Monitoraggio porta LPR</span><span class="sxs-lookup"><span data-stu-id="9827c-203">LPR Port Monitor</span></span>

<span data-ttu-id="9827c-204">55</span><span class="sxs-lookup"><span data-stu-id="9827c-204">55</span></span>

[<span data-ttu-id="9827c-205">Internet Storage Name Server</span><span class="sxs-lookup"><span data-stu-id="9827c-205">Internet Storage Name Server</span></span>](/windows)

<span data-ttu-id="9827c-206">57</span><span class="sxs-lookup"><span data-stu-id="9827c-206">57</span></span>

[<span data-ttu-id="9827c-207">Multipath I/O</span><span class="sxs-lookup"><span data-stu-id="9827c-207">Multipath I/O</span></span>](/windows)

<span data-ttu-id="9827c-208">58</span><span class="sxs-lookup"><span data-stu-id="9827c-208">58</span></span>

<span data-ttu-id="9827c-209">Client TFTP</span><span class="sxs-lookup"><span data-stu-id="9827c-209">TFTP Client</span></span>

<span data-ttu-id="9827c-210">59</span><span class="sxs-lookup"><span data-stu-id="9827c-210">59</span></span>

[<span data-ttu-id="9827c-211">Servizi SNMP</span><span class="sxs-lookup"><span data-stu-id="9827c-211">SNMP Services</span></span>](/windows)

<span data-ttu-id="9827c-212">60</span><span class="sxs-lookup"><span data-stu-id="9827c-212">60</span></span>

[<span data-ttu-id="9827c-213">Gestione archivi rimovibili</span><span class="sxs-lookup"><span data-stu-id="9827c-213">Removable Storage Manager</span></span>](/windows)

<span data-ttu-id="9827c-214">61</span><span class="sxs-lookup"><span data-stu-id="9827c-214">61</span></span>

<span data-ttu-id="9827c-215">Crittografia unità BitLocker</span><span class="sxs-lookup"><span data-stu-id="9827c-215">BitLocker Drive Encryption</span></span>

<span data-ttu-id="9827c-216">62</span><span class="sxs-lookup"><span data-stu-id="9827c-216">62</span></span>

[<span data-ttu-id="9827c-217">Servizi per il file System di rete</span><span class="sxs-lookup"><span data-stu-id="9827c-217">Services For Network File System</span></span>](/windows)

<span data-ttu-id="9827c-218">63</span><span class="sxs-lookup"><span data-stu-id="9827c-218">63</span></span>

<span data-ttu-id="9827c-219">Client di stampa Internet</span><span class="sxs-lookup"><span data-stu-id="9827c-219">Internet Printing Client</span></span>

<span data-ttu-id="9827c-220">64</span><span class="sxs-lookup"><span data-stu-id="9827c-220">64</span></span>

[<span data-ttu-id="9827c-221">Protocollo PNRP (Peer Name Resolution Protocol)</span><span class="sxs-lookup"><span data-stu-id="9827c-221">Peer Name Resolution Protocol</span></span>](/windows)

<span data-ttu-id="9827c-222">65</span><span class="sxs-lookup"><span data-stu-id="9827c-222">65</span></span>

<span data-ttu-id="9827c-223">Connection Manager Administration Kit</span><span class="sxs-lookup"><span data-stu-id="9827c-223">Connection Manager Administration Kit</span></span>

<span data-ttu-id="9827c-224">66</span><span class="sxs-lookup"><span data-stu-id="9827c-224">66</span></span>

[<span data-ttu-id="9827c-225">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="9827c-225">Windows PowerShell</span></span>](/windows)<br/>

<span data-ttu-id="9827c-226">67</span><span class="sxs-lookup"><span data-stu-id="9827c-226">67</span></span>

[<span data-ttu-id="9827c-227">Strumenti di amministrazione remota del server</span><span class="sxs-lookup"><span data-stu-id="9827c-227">Remote Server Administration Tools</span></span>](/windows)

<span data-ttu-id="9827c-228">68</span><span class="sxs-lookup"><span data-stu-id="9827c-228">68</span></span>

[<span data-ttu-id="9827c-229">Servizio audio/video Windows di qualità</span><span class="sxs-lookup"><span data-stu-id="9827c-229">Quality Windows Audio Video Experience</span></span>](/windows)

<span data-ttu-id="9827c-230">69</span><span class="sxs-lookup"><span data-stu-id="9827c-230">69</span></span>

[<span data-ttu-id="9827c-231">Gestione Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="9827c-231">Group Policy Management</span></span>](/windows)

<span data-ttu-id="9827c-232">71</span><span class="sxs-lookup"><span data-stu-id="9827c-232">71</span></span>

[<span data-ttu-id="9827c-233">Servizio di indicizzazione</span><span class="sxs-lookup"><span data-stu-id="9827c-233">Indexing Service</span></span>](/windows)

<span data-ttu-id="9827c-234">72</span><span class="sxs-lookup"><span data-stu-id="9827c-234">72</span></span>

[<span data-ttu-id="9827c-235">Gestione risorse file server</span><span class="sxs-lookup"><span data-stu-id="9827c-235">File Server Resource Manager (FSRM)</span></span>](/windows)

<span data-ttu-id="9827c-236">73</span><span class="sxs-lookup"><span data-stu-id="9827c-236">73</span></span>

<span data-ttu-id="9827c-237">Compressione differenziale remota</span><span class="sxs-lookup"><span data-stu-id="9827c-237">Remote Differential Compression</span></span>

<span data-ttu-id="9827c-238">310</span><span class="sxs-lookup"><span data-stu-id="9827c-238">310</span></span>

<span data-ttu-id="9827c-239">Servizi di riconoscimento della grafia</span><span class="sxs-lookup"><span data-stu-id="9827c-239">Ink and Handwriting Services</span></span><br/>

<span data-ttu-id="9827c-240">320</span><span class="sxs-lookup"><span data-stu-id="9827c-240">320</span></span>

[<span data-ttu-id="9827c-241">Strumenti di migrazione per Windows Server</span><span class="sxs-lookup"><span data-stu-id="9827c-241">Windows Server Migration Tools</span></span>](/windows)<br/>

<span data-ttu-id="9827c-242">321</span><span class="sxs-lookup"><span data-stu-id="9827c-242">321</span></span>

[<span data-ttu-id="9827c-243">Estensione IIS di Gestione remota Windows</span><span class="sxs-lookup"><span data-stu-id="9827c-243">WinRM IIS Extension</span></span>](/windows)<br/>

<span data-ttu-id="9827c-244">324</span><span class="sxs-lookup"><span data-stu-id="9827c-244">324</span></span>

[<span data-ttu-id="9827c-245">BranchCache</span><span class="sxs-lookup"><span data-stu-id="9827c-245">BranchCache</span></span>](#branchcache)<br/>

<span data-ttu-id="9827c-246">334</span><span class="sxs-lookup"><span data-stu-id="9827c-246">334</span></span>

[<span data-ttu-id="9827c-247">Console Gestione DirectAccess</span><span class="sxs-lookup"><span data-stu-id="9827c-247">DirectAccess Management Console</span></span>](/windows)<br/>

<span data-ttu-id="9827c-248">335</span><span class="sxs-lookup"><span data-stu-id="9827c-248">335</span></span>

[<span data-ttu-id="9827c-249">Servizio trasferimento intelligente in background (BITS)</span><span class="sxs-lookup"><span data-stu-id="9827c-249">Background Intelligent Transfer Service (BITS)</span></span>](/windows)<br/>

<span data-ttu-id="9827c-250">338</span><span class="sxs-lookup"><span data-stu-id="9827c-250">338</span></span>

[<span data-ttu-id="9827c-251">XPS Viewer</span><span class="sxs-lookup"><span data-stu-id="9827c-251">XPS Viewer</span></span>](/windows)<br/>

<span data-ttu-id="9827c-252">339</span><span class="sxs-lookup"><span data-stu-id="9827c-252">339</span></span>

[<span data-ttu-id="9827c-253">Windows Biometric Framework</span><span class="sxs-lookup"><span data-stu-id="9827c-253">Windows Biometric Framework</span></span>](/windows)<br/>

<span data-ttu-id="9827c-254">340</span><span class="sxs-lookup"><span data-stu-id="9827c-254">340</span></span>

<span data-ttu-id="9827c-255">Supporto WoW64</span><span class="sxs-lookup"><span data-stu-id="9827c-255">WoW64 Support</span></span><br/>

<span data-ttu-id="9827c-256">351</span><span class="sxs-lookup"><span data-stu-id="9827c-256">351</span></span>

[<span data-ttu-id="9827c-257">Windows PowerShell Integrated Scripting Environment (ISE)</span><span class="sxs-lookup"><span data-stu-id="9827c-257">Windows PowerShell Integrated Scripting Environment (ISE)</span></span>](/windows)<br/>

<span data-ttu-id="9827c-258">352</span><span class="sxs-lookup"><span data-stu-id="9827c-258">352</span></span>

<span data-ttu-id="9827c-259">Windows TIFF IFilter</span><span class="sxs-lookup"><span data-stu-id="9827c-259">Windows TIFF IFilter</span></span><br/>

<span data-ttu-id="9827c-260">404</span><span class="sxs-lookup"><span data-stu-id="9827c-260">404</span></span>

[<span data-ttu-id="9827c-261">Windows Server Update Services</span><span class="sxs-lookup"><span data-stu-id="9827c-261">Window Server Update Services</span></span>](/windows)

<span data-ttu-id="9827c-262">409</span><span class="sxs-lookup"><span data-stu-id="9827c-262">409</span></span>

[<span data-ttu-id="9827c-263">Server di Gestione indirizzi IP</span><span class="sxs-lookup"><span data-stu-id="9827c-263">IP Address Management (IPAM) Server</span></span>](/windows)

<span data-ttu-id="9827c-264">417</span><span class="sxs-lookup"><span data-stu-id="9827c-264">417</span></span>

[<span data-ttu-id="9827c-265">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="9827c-265">Windows PowerShell</span></span>](/windows)

<span data-ttu-id="9827c-266">418</span><span class="sxs-lookup"><span data-stu-id="9827c-266">418</span></span>

[<span data-ttu-id="9827c-267">.NET Framework 4.5</span><span class="sxs-lookup"><span data-stu-id="9827c-267">.NET Framework 4.5</span></span>](/windows)

<span data-ttu-id="9827c-268">432</span><span class="sxs-lookup"><span data-stu-id="9827c-268">432</span></span>

[<span data-ttu-id="9827c-269">Servizio Windows Search</span><span class="sxs-lookup"><span data-stu-id="9827c-269">Windows Search Service</span></span>](/windows)

<span data-ttu-id="9827c-270">438</span><span class="sxs-lookup"><span data-stu-id="9827c-270">438</span></span>

[<span data-ttu-id="9827c-271">Client per NFS</span><span class="sxs-lookup"><span data-stu-id="9827c-271">Client for NFS</span></span>](/windows)

<span data-ttu-id="9827c-272">441</span><span class="sxs-lookup"><span data-stu-id="9827c-272">441</span></span>

[<span data-ttu-id="9827c-273">Sblocco di rete via BitLocker</span><span class="sxs-lookup"><span data-stu-id="9827c-273">BitLocker Network Unlock</span></span>](/windows)

<span data-ttu-id="9827c-274">442</span><span class="sxs-lookup"><span data-stu-id="9827c-274">442</span></span>

[<span data-ttu-id="9827c-275">Estensione IIS OData gestione</span><span class="sxs-lookup"><span data-stu-id="9827c-275">Management OData IIS Extension</span></span>](/windows)

<span data-ttu-id="9827c-276">450</span><span class="sxs-lookup"><span data-stu-id="9827c-276">450</span></span>

[<span data-ttu-id="9827c-277">.NET Framework 4.5 Advanced Services</span><span class="sxs-lookup"><span data-stu-id="9827c-277">.NET Framework 4.5 Advanced Services</span></span>](/windows)

<span data-ttu-id="9827c-278">466</span><span class="sxs-lookup"><span data-stu-id="9827c-278">466</span></span>

[<span data-ttu-id="9827c-279">Funzionalità di .NET Framework 4.5</span><span class="sxs-lookup"><span data-stu-id="9827c-279">.NET Framework 4.5 Features</span></span>](/windows)

<span data-ttu-id="9827c-280">468</span><span class="sxs-lookup"><span data-stu-id="9827c-280">468</span></span>

[<span data-ttu-id="9827c-281">Accesso remoto</span><span class="sxs-lookup"><span data-stu-id="9827c-281">Remote Access</span></span>](/windows)<br/>

<span data-ttu-id="9827c-282">477</span><span class="sxs-lookup"><span data-stu-id="9827c-282">477</span></span>

[<span data-ttu-id="9827c-283">Interfacce utente e infrastruttura</span><span class="sxs-lookup"><span data-stu-id="9827c-283">User Interfaces and Infrastructure</span></span>](/windows)

<span data-ttu-id="9827c-284">478</span><span class="sxs-lookup"><span data-stu-id="9827c-284">478</span></span>

[<span data-ttu-id="9827c-285">Strumenti di gestione e infrastruttura grafica</span><span class="sxs-lookup"><span data-stu-id="9827c-285">Graphical Management Tools and Infrastructure</span></span>](/windows)

<span data-ttu-id="9827c-286">481</span><span class="sxs-lookup"><span data-stu-id="9827c-286">481</span></span>

[<span data-ttu-id="9827c-287">Servizi file e archiviazione</span><span class="sxs-lookup"><span data-stu-id="9827c-287">File and Storage Services</span></span>](/windows)

<span data-ttu-id="9827c-288">485</span><span class="sxs-lookup"><span data-stu-id="9827c-288">485</span></span>

[<span data-ttu-id="9827c-289">Esperienza Windows Server Essentials</span><span class="sxs-lookup"><span data-stu-id="9827c-289">Windows Server Essentials Experience</span></span>](/windows)

<span data-ttu-id="9827c-290">488</span><span class="sxs-lookup"><span data-stu-id="9827c-290">488</span></span>

[<span data-ttu-id="9827c-291">Esecuzione diretta</span><span class="sxs-lookup"><span data-stu-id="9827c-291">Direct Play</span></span>](/windows)

<span data-ttu-id="9827c-292">Servizi file-servizi ruolo (6)</span><span class="sxs-lookup"><span data-stu-id="9827c-292">File Services - Role Services (6)</span></span>

<span data-ttu-id="9827c-293">Valore</span><span class="sxs-lookup"><span data-stu-id="9827c-293">Value</span></span>

<span data-ttu-id="9827c-294">Nome</span><span class="sxs-lookup"><span data-stu-id="9827c-294">Name</span></span>

<span data-ttu-id="9827c-295">100</span><span class="sxs-lookup"><span data-stu-id="9827c-295">100</span></span>

[<span data-ttu-id="9827c-296">file system distribuito</span><span class="sxs-lookup"><span data-stu-id="9827c-296">Distributed File System</span></span>](/windows)

<span data-ttu-id="9827c-297">101</span><span class="sxs-lookup"><span data-stu-id="9827c-297">101</span></span>

<span data-ttu-id="9827c-298">Spazio dei nomi DFS</span><span class="sxs-lookup"><span data-stu-id="9827c-298">DFS Namespace</span></span>

<span data-ttu-id="9827c-299">102</span><span class="sxs-lookup"><span data-stu-id="9827c-299">102</span></span>

<span data-ttu-id="9827c-300">Replica DFS</span><span class="sxs-lookup"><span data-stu-id="9827c-300">DFS Replication</span></span>

<span data-ttu-id="9827c-301">103</span><span class="sxs-lookup"><span data-stu-id="9827c-301">103</span></span>

[<span data-ttu-id="9827c-302">Servizio Replica file</span><span class="sxs-lookup"><span data-stu-id="9827c-302">File Replication Service</span></span>](/windows)

<span data-ttu-id="9827c-303">104</span><span class="sxs-lookup"><span data-stu-id="9827c-303">104</span></span>

[<span data-ttu-id="9827c-304">Gestione risorse file server</span><span class="sxs-lookup"><span data-stu-id="9827c-304">File Server Resource Manager (FSRM)</span></span>](/windows)

<span data-ttu-id="9827c-305">105</span><span class="sxs-lookup"><span data-stu-id="9827c-305">105</span></span>

[<span data-ttu-id="9827c-306">Servizi per il file System di rete</span><span class="sxs-lookup"><span data-stu-id="9827c-306">Services For Network File System</span></span>](/windows)

<span data-ttu-id="9827c-307">106</span><span class="sxs-lookup"><span data-stu-id="9827c-307">106</span></span>

[<span data-ttu-id="9827c-308">Single Instance Storage (SIS)</span><span class="sxs-lookup"><span data-stu-id="9827c-308">Single Instance Storage</span></span>](/windows)

<span data-ttu-id="9827c-309">107</span><span class="sxs-lookup"><span data-stu-id="9827c-309">107</span></span>

[<span data-ttu-id="9827c-310">Servizio Windows Search</span><span class="sxs-lookup"><span data-stu-id="9827c-310">Windows Search Service</span></span>](/windows)

<span data-ttu-id="9827c-311">108</span><span class="sxs-lookup"><span data-stu-id="9827c-311">108</span></span>

[<span data-ttu-id="9827c-312">Servizio di indicizzazione</span><span class="sxs-lookup"><span data-stu-id="9827c-312">Indexing Service</span></span>](/windows)

<span data-ttu-id="9827c-313">255</span><span class="sxs-lookup"><span data-stu-id="9827c-313">255</span></span>

<span data-ttu-id="9827c-314">File Server</span><span class="sxs-lookup"><span data-stu-id="9827c-314">File Server</span></span>

<span data-ttu-id="9827c-315">350</span><span class="sxs-lookup"><span data-stu-id="9827c-315">350</span></span>

<span data-ttu-id="9827c-316">BranchCache per file di rete</span><span class="sxs-lookup"><span data-stu-id="9827c-316">BranchCache for Network Files</span></span>

<span data-ttu-id="9827c-317">431</span><span class="sxs-lookup"><span data-stu-id="9827c-317">431</span></span>

[<span data-ttu-id="9827c-318">Server per NFS</span><span class="sxs-lookup"><span data-stu-id="9827c-318">Server for NFS</span></span>](/windows)<br/>

<span data-ttu-id="9827c-319">434</span><span class="sxs-lookup"><span data-stu-id="9827c-319">434</span></span>

[<span data-ttu-id="9827c-320">Servizio agente File Server VSS</span><span class="sxs-lookup"><span data-stu-id="9827c-320">File Server VSS Agent Service</span></span>](/windows)<br/>

<span data-ttu-id="9827c-321">435</span><span class="sxs-lookup"><span data-stu-id="9827c-321">435</span></span>

[<span data-ttu-id="9827c-322">Server di destinazione iSCSI</span><span class="sxs-lookup"><span data-stu-id="9827c-322">iSCSI Target Server</span></span>](/windows)<br/>

<span data-ttu-id="9827c-323">436</span><span class="sxs-lookup"><span data-stu-id="9827c-323">436</span></span>

[<span data-ttu-id="9827c-324">Deduplicazione dati</span><span class="sxs-lookup"><span data-stu-id="9827c-324">Data Deduplication</span></span>](/windows)<br/>

<span data-ttu-id="9827c-325">437</span><span class="sxs-lookup"><span data-stu-id="9827c-325">437</span></span>

[<span data-ttu-id="9827c-326">Provider di archiviazione di destinazione iSCSI (provider hardware VDS e VSS)</span><span class="sxs-lookup"><span data-stu-id="9827c-326">iSCSI Target Storage Provider (VDS and VSS hardware providers)</span></span>](/windows)

<span data-ttu-id="9827c-327">486</span><span class="sxs-lookup"><span data-stu-id="9827c-327">486</span></span>

[<span data-ttu-id="9827c-328">Cartelle di lavoro</span><span class="sxs-lookup"><span data-stu-id="9827c-328">Work Folders</span></span>](/windows)

<span data-ttu-id="9827c-329">Servizi di dominio Active Directory-servizi ruolo (10)</span><span class="sxs-lookup"><span data-stu-id="9827c-329">AD DS - Role Services (10)</span></span>

<span data-ttu-id="9827c-330">Valore</span><span class="sxs-lookup"><span data-stu-id="9827c-330">Value</span></span>

<span data-ttu-id="9827c-331">Nome</span><span class="sxs-lookup"><span data-stu-id="9827c-331">Name</span></span>

<span data-ttu-id="9827c-332">110</span><span class="sxs-lookup"><span data-stu-id="9827c-332">110</span></span>

[<span data-ttu-id="9827c-333">Controller di dominio di Active Directory</span><span class="sxs-lookup"><span data-stu-id="9827c-333">Active Directory Domain Controller</span></span>](/windows)

<span data-ttu-id="9827c-334">111</span><span class="sxs-lookup"><span data-stu-id="9827c-334">111</span></span>

[<span data-ttu-id="9827c-335">Gestione delle identità per UNIX</span><span class="sxs-lookup"><span data-stu-id="9827c-335">Identity Management For Unix</span></span>](/windows)

<span data-ttu-id="9827c-336">112</span><span class="sxs-lookup"><span data-stu-id="9827c-336">112</span></span>

[<span data-ttu-id="9827c-337">Server per Network Information Services</span><span class="sxs-lookup"><span data-stu-id="9827c-337">Server For Network Information Services</span></span>](/windows)

<span data-ttu-id="9827c-338">113</span><span class="sxs-lookup"><span data-stu-id="9827c-338">113</span></span>

[<span data-ttu-id="9827c-339">Sincronizzazione delle password</span><span class="sxs-lookup"><span data-stu-id="9827c-339">Password Synchronization</span></span>](/windows)

<span data-ttu-id="9827c-340">294</span><span class="sxs-lookup"><span data-stu-id="9827c-340">294</span></span>

[<span data-ttu-id="9827c-341">Strumenti di amministrazione remota del server</span><span class="sxs-lookup"><span data-stu-id="9827c-341">Remote Server Administration Tools</span></span>](/windows)

<span data-ttu-id="9827c-342">Flussi multimediali-servizi ruolo (3)</span><span class="sxs-lookup"><span data-stu-id="9827c-342">Streaming Media - Role Services (3)</span></span>

<span data-ttu-id="9827c-343">Valore</span><span class="sxs-lookup"><span data-stu-id="9827c-343">Value</span></span>

<span data-ttu-id="9827c-344">Nome</span><span class="sxs-lookup"><span data-stu-id="9827c-344">Name</span></span>

<span data-ttu-id="9827c-345">120</span><span class="sxs-lookup"><span data-stu-id="9827c-345">120</span></span>

[<span data-ttu-id="9827c-346">Windows Media Server</span><span class="sxs-lookup"><span data-stu-id="9827c-346">Windows Media Server</span></span>](/windows)

<span data-ttu-id="9827c-347">121</span><span class="sxs-lookup"><span data-stu-id="9827c-347">121</span></span>

[<span data-ttu-id="9827c-348">Amministrazione basata sul Web</span><span class="sxs-lookup"><span data-stu-id="9827c-348">Web-based Administration</span></span>](/windows)

<span data-ttu-id="9827c-349">122</span><span class="sxs-lookup"><span data-stu-id="9827c-349">122</span></span>

[<span data-ttu-id="9827c-350">Agente di registrazione</span><span class="sxs-lookup"><span data-stu-id="9827c-350">Logging Agent</span></span>](/windows)

<span data-ttu-id="9827c-351">ADFS-servizi ruolo (8)</span><span class="sxs-lookup"><span data-stu-id="9827c-351">ADFS - Role Services (8)</span></span>

<span data-ttu-id="9827c-352">Valore</span><span class="sxs-lookup"><span data-stu-id="9827c-352">Value</span></span>

<span data-ttu-id="9827c-353">Nome</span><span class="sxs-lookup"><span data-stu-id="9827c-353">Name</span></span>

<span data-ttu-id="9827c-354">125</span><span class="sxs-lookup"><span data-stu-id="9827c-354">125</span></span>

[<span data-ttu-id="9827c-355">Active Directory Federation Services</span><span class="sxs-lookup"><span data-stu-id="9827c-355">Active Directory Federation Services</span></span>](/windows)

<span data-ttu-id="9827c-356">126</span><span class="sxs-lookup"><span data-stu-id="9827c-356">126</span></span>

[<span data-ttu-id="9827c-357">Criteri di Servizio federativo</span><span class="sxs-lookup"><span data-stu-id="9827c-357">Federation Service Policy</span></span>](/windows)

<span data-ttu-id="9827c-358">127</span><span class="sxs-lookup"><span data-stu-id="9827c-358">127</span></span>

[<span data-ttu-id="9827c-359">Agenti Web ADFS</span><span class="sxs-lookup"><span data-stu-id="9827c-359">AD FS Web Agents</span></span>](/windows)

<span data-ttu-id="9827c-360">128</span><span class="sxs-lookup"><span data-stu-id="9827c-360">128</span></span>

[<span data-ttu-id="9827c-361">Agente in grado di riconoscere attestazioni</span><span class="sxs-lookup"><span data-stu-id="9827c-361">Claims-aware Agent</span></span>](/windows)

<span data-ttu-id="9827c-362">129</span><span class="sxs-lookup"><span data-stu-id="9827c-362">129</span></span>

[<span data-ttu-id="9827c-363">Agente basato su token Windows</span><span class="sxs-lookup"><span data-stu-id="9827c-363">Windows Token-based Agent</span></span>](/windows)

<span data-ttu-id="9827c-364">Servizi ruolo Servizi Desktop remoto (18)</span><span class="sxs-lookup"><span data-stu-id="9827c-364">Remote Desktop Services - Role Services (18)</span></span>

<span data-ttu-id="9827c-365">Valore</span><span class="sxs-lookup"><span data-stu-id="9827c-365">Value</span></span>

<span data-ttu-id="9827c-366">Nome</span><span class="sxs-lookup"><span data-stu-id="9827c-366">Name</span></span>

<span data-ttu-id="9827c-367">130</span><span class="sxs-lookup"><span data-stu-id="9827c-367">130</span></span>

<span data-ttu-id="9827c-368">Host sessione Desktop remoto</span><span class="sxs-lookup"><span data-stu-id="9827c-368">Remote Desktop Session Host</span></span><br/> [<span data-ttu-id="9827c-369">modifica nome</span><span class="sxs-lookup"><span data-stu-id="9827c-369">name change</span></span>](/windows)<br/>

<span data-ttu-id="9827c-370">131</span><span class="sxs-lookup"><span data-stu-id="9827c-370">131</span></span>

[<span data-ttu-id="9827c-371">Servizio licenze Desktop remoto</span><span class="sxs-lookup"><span data-stu-id="9827c-371">Remote Desktop Licensing</span></span>](/windows)<br/> [<span data-ttu-id="9827c-372">modifica nome</span><span class="sxs-lookup"><span data-stu-id="9827c-372">name change</span></span>](/windows)<br/>

<span data-ttu-id="9827c-373">132</span><span class="sxs-lookup"><span data-stu-id="9827c-373">132</span></span>

<span data-ttu-id="9827c-374">Gateway Desktop remoto</span><span class="sxs-lookup"><span data-stu-id="9827c-374">Remote Desktop Gateway</span></span><br/> [<span data-ttu-id="9827c-375">modifica nome</span><span class="sxs-lookup"><span data-stu-id="9827c-375">name change</span></span>](/windows)<br/>

<span data-ttu-id="9827c-376">133</span><span class="sxs-lookup"><span data-stu-id="9827c-376">133</span></span>

<span data-ttu-id="9827c-377">Gestore connessione Desktop remoto</span><span class="sxs-lookup"><span data-stu-id="9827c-377">Remote Desktop Connection Broker</span></span><br/> [<span data-ttu-id="9827c-378">modifica nome</span><span class="sxs-lookup"><span data-stu-id="9827c-378">name change</span></span>](/windows)<br/>

<span data-ttu-id="9827c-379">134</span><span class="sxs-lookup"><span data-stu-id="9827c-379">134</span></span>

<span data-ttu-id="9827c-380">Accesso Web Desktop remoto</span><span class="sxs-lookup"><span data-stu-id="9827c-380">Remote Desktop Web Access</span></span><br/> [<span data-ttu-id="9827c-381">modifica nome</span><span class="sxs-lookup"><span data-stu-id="9827c-381">name change</span></span>](/windows)<br/>

<span data-ttu-id="9827c-382">322</span><span class="sxs-lookup"><span data-stu-id="9827c-382">322</span></span>

<span data-ttu-id="9827c-383">Host di virtualizzazione Desktop remoto</span><span class="sxs-lookup"><span data-stu-id="9827c-383">Remote Desktop Virtualization Host</span></span><br/>

<span data-ttu-id="9827c-384">Servizi ruolo Host di virtualizzazione Desktop remoto (322)</span><span class="sxs-lookup"><span data-stu-id="9827c-384">Remote Desktop Virtualization Host - Role Services (322)</span></span>

<span data-ttu-id="9827c-385">Valore</span><span class="sxs-lookup"><span data-stu-id="9827c-385">Value</span></span>

<span data-ttu-id="9827c-386">Nome</span><span class="sxs-lookup"><span data-stu-id="9827c-386">Name</span></span>

<span data-ttu-id="9827c-387">325</span><span class="sxs-lookup"><span data-stu-id="9827c-387">325</span></span>

[<span data-ttu-id="9827c-388">Servizi di base</span><span class="sxs-lookup"><span data-stu-id="9827c-388">Core Services</span></span>](/windows)<br/>

<span data-ttu-id="9827c-389">327</span><span class="sxs-lookup"><span data-stu-id="9827c-389">327</span></span>

[<span data-ttu-id="9827c-390">Desktop remoto grafica virtuale</span><span class="sxs-lookup"><span data-stu-id="9827c-390">Remote Desktop Virtual Graphics</span></span>](/windows)<br/>

<span data-ttu-id="9827c-391">Servizi ruolo Servizi di stampa e digitalizzazione (7)</span><span class="sxs-lookup"><span data-stu-id="9827c-391">Print and Document Services - Role Services (7)</span></span>

<span data-ttu-id="9827c-392">Valore</span><span class="sxs-lookup"><span data-stu-id="9827c-392">Value</span></span>

<span data-ttu-id="9827c-393">Nome</span><span class="sxs-lookup"><span data-stu-id="9827c-393">Name</span></span>

<span data-ttu-id="9827c-394">135</span><span class="sxs-lookup"><span data-stu-id="9827c-394">135</span></span>

<span data-ttu-id="9827c-395">Server di stampa</span><span class="sxs-lookup"><span data-stu-id="9827c-395">Print Server</span></span>

<span data-ttu-id="9827c-396">136</span><span class="sxs-lookup"><span data-stu-id="9827c-396">136</span></span>

<span data-ttu-id="9827c-397">Stampa Internet</span><span class="sxs-lookup"><span data-stu-id="9827c-397">Internet Printing</span></span>

<span data-ttu-id="9827c-398">137</span><span class="sxs-lookup"><span data-stu-id="9827c-398">137</span></span>

<span data-ttu-id="9827c-399">Servizio di stampa LPD</span><span class="sxs-lookup"><span data-stu-id="9827c-399">LPD Print Service</span></span>

<span data-ttu-id="9827c-400">328</span><span class="sxs-lookup"><span data-stu-id="9827c-400">328</span></span>

[<span data-ttu-id="9827c-401">Server Digitalizzazione distribuita</span><span class="sxs-lookup"><span data-stu-id="9827c-401">Distributed Scan Server</span></span>](/windows)<br/>

<span data-ttu-id="9827c-402">Server Web (IIS)-servizi ruolo (2)</span><span class="sxs-lookup"><span data-stu-id="9827c-402">Web Server (IIS) - Role Services (2)</span></span>

<span data-ttu-id="9827c-403">Valore</span><span class="sxs-lookup"><span data-stu-id="9827c-403">Value</span></span>

<span data-ttu-id="9827c-404">Nome</span><span class="sxs-lookup"><span data-stu-id="9827c-404">Name</span></span>

<span data-ttu-id="9827c-405">140</span><span class="sxs-lookup"><span data-stu-id="9827c-405">140</span></span>

<span data-ttu-id="9827c-406">Server web</span><span class="sxs-lookup"><span data-stu-id="9827c-406">Web Server</span></span>

<span data-ttu-id="9827c-407">141</span><span class="sxs-lookup"><span data-stu-id="9827c-407">141</span></span>

<span data-ttu-id="9827c-408">Funzionalità HTTP comuni</span><span class="sxs-lookup"><span data-stu-id="9827c-408">Common HTTP Features</span></span>

<span data-ttu-id="9827c-409">142</span><span class="sxs-lookup"><span data-stu-id="9827c-409">142</span></span>

<span data-ttu-id="9827c-410">Contenuto statico</span><span class="sxs-lookup"><span data-stu-id="9827c-410">Static Content</span></span>

<span data-ttu-id="9827c-411">143</span><span class="sxs-lookup"><span data-stu-id="9827c-411">143</span></span>

<span data-ttu-id="9827c-412">Documento predefinito</span><span class="sxs-lookup"><span data-stu-id="9827c-412">Default Document</span></span>

<span data-ttu-id="9827c-413">144</span><span class="sxs-lookup"><span data-stu-id="9827c-413">144</span></span>

<span data-ttu-id="9827c-414">Esplorazione directory</span><span class="sxs-lookup"><span data-stu-id="9827c-414">Directory Browse</span></span>

<span data-ttu-id="9827c-415">145</span><span class="sxs-lookup"><span data-stu-id="9827c-415">145</span></span>

<span data-ttu-id="9827c-416">Errori HTTP</span><span class="sxs-lookup"><span data-stu-id="9827c-416">HTTP Errors</span></span>

<span data-ttu-id="9827c-417">146</span><span class="sxs-lookup"><span data-stu-id="9827c-417">146</span></span>

<span data-ttu-id="9827c-418">Reindirizzamento HTTP</span><span class="sxs-lookup"><span data-stu-id="9827c-418">HTTP Redirection</span></span>

<span data-ttu-id="9827c-419">147</span><span class="sxs-lookup"><span data-stu-id="9827c-419">147</span></span>

<span data-ttu-id="9827c-420">Sviluppo applicazioni</span><span class="sxs-lookup"><span data-stu-id="9827c-420">Application Development</span></span>

<span data-ttu-id="9827c-421">148</span><span class="sxs-lookup"><span data-stu-id="9827c-421">148</span></span>

<span data-ttu-id="9827c-422">ASP.NET</span><span class="sxs-lookup"><span data-stu-id="9827c-422">ASP.NET</span></span>

<span data-ttu-id="9827c-423">149</span><span class="sxs-lookup"><span data-stu-id="9827c-423">149</span></span>

<span data-ttu-id="9827c-424">Estendibilità .NET</span><span class="sxs-lookup"><span data-stu-id="9827c-424">.NET Extensibility</span></span>

<span data-ttu-id="9827c-425">150</span><span class="sxs-lookup"><span data-stu-id="9827c-425">150</span></span>

<span data-ttu-id="9827c-426">ASP</span><span class="sxs-lookup"><span data-stu-id="9827c-426">ASP</span></span>

<span data-ttu-id="9827c-427">151</span><span class="sxs-lookup"><span data-stu-id="9827c-427">151</span></span>

<span data-ttu-id="9827c-428">CGI</span><span class="sxs-lookup"><span data-stu-id="9827c-428">CGI</span></span>

<span data-ttu-id="9827c-429">152</span><span class="sxs-lookup"><span data-stu-id="9827c-429">152</span></span>

<span data-ttu-id="9827c-430">Estensioni ISAPI</span><span class="sxs-lookup"><span data-stu-id="9827c-430">ISAPI Extensions</span></span>

<span data-ttu-id="9827c-431">153</span><span class="sxs-lookup"><span data-stu-id="9827c-431">153</span></span>

<span data-ttu-id="9827c-432">Filtri ISAPI</span><span class="sxs-lookup"><span data-stu-id="9827c-432">ISAPI Filters</span></span>

<span data-ttu-id="9827c-433">154</span><span class="sxs-lookup"><span data-stu-id="9827c-433">154</span></span>

<span data-ttu-id="9827c-434">Server Side Includes</span><span class="sxs-lookup"><span data-stu-id="9827c-434">Server Side Includes</span></span>

<span data-ttu-id="9827c-435">155</span><span class="sxs-lookup"><span data-stu-id="9827c-435">155</span></span>

<span data-ttu-id="9827c-436">Integrità e diagnostica</span><span class="sxs-lookup"><span data-stu-id="9827c-436">Health And Diagnostics</span></span>

<span data-ttu-id="9827c-437">156</span><span class="sxs-lookup"><span data-stu-id="9827c-437">156</span></span>

<span data-ttu-id="9827c-438">Registrazione HTTP</span><span class="sxs-lookup"><span data-stu-id="9827c-438">HTTP Logging</span></span>

<span data-ttu-id="9827c-439">157</span><span class="sxs-lookup"><span data-stu-id="9827c-439">157</span></span>

<span data-ttu-id="9827c-440">Strumenti di registrazione</span><span class="sxs-lookup"><span data-stu-id="9827c-440">Logging Tools</span></span>

<span data-ttu-id="9827c-441">158</span><span class="sxs-lookup"><span data-stu-id="9827c-441">158</span></span>

<span data-ttu-id="9827c-442">Monitoraggio richieste</span><span class="sxs-lookup"><span data-stu-id="9827c-442">Request Monitor</span></span>

<span data-ttu-id="9827c-443">159</span><span class="sxs-lookup"><span data-stu-id="9827c-443">159</span></span>

<span data-ttu-id="9827c-444">Traccia</span><span class="sxs-lookup"><span data-stu-id="9827c-444">Tracing</span></span>

<span data-ttu-id="9827c-445">160</span><span class="sxs-lookup"><span data-stu-id="9827c-445">160</span></span>

<span data-ttu-id="9827c-446">Registrazione personalizzata</span><span class="sxs-lookup"><span data-stu-id="9827c-446">Custom Logging</span></span>

<span data-ttu-id="9827c-447">161</span><span class="sxs-lookup"><span data-stu-id="9827c-447">161</span></span>

<span data-ttu-id="9827c-448">Registrazione ODBC</span><span class="sxs-lookup"><span data-stu-id="9827c-448">ODBC Logging</span></span>

<span data-ttu-id="9827c-449">162</span><span class="sxs-lookup"><span data-stu-id="9827c-449">162</span></span>

<span data-ttu-id="9827c-450">Sicurezza</span><span class="sxs-lookup"><span data-stu-id="9827c-450">Security</span></span>

<span data-ttu-id="9827c-451">163</span><span class="sxs-lookup"><span data-stu-id="9827c-451">163</span></span>

<span data-ttu-id="9827c-452">Autenticazione di base</span><span class="sxs-lookup"><span data-stu-id="9827c-452">Basic Authentication</span></span>

<span data-ttu-id="9827c-453">164</span><span class="sxs-lookup"><span data-stu-id="9827c-453">164</span></span>

<span data-ttu-id="9827c-454">Autenticazione di Windows</span><span class="sxs-lookup"><span data-stu-id="9827c-454">Windows Authentication</span></span>

<span data-ttu-id="9827c-455">165</span><span class="sxs-lookup"><span data-stu-id="9827c-455">165</span></span>

<span data-ttu-id="9827c-456">Autenticazione del digest</span><span class="sxs-lookup"><span data-stu-id="9827c-456">Digest Authentication</span></span>

<span data-ttu-id="9827c-457">166</span><span class="sxs-lookup"><span data-stu-id="9827c-457">166</span></span>

<span data-ttu-id="9827c-458">Autenticazione mapping certificati client</span><span class="sxs-lookup"><span data-stu-id="9827c-458">Client Certificate Mapping Authentication</span></span>

<span data-ttu-id="9827c-459">167</span><span class="sxs-lookup"><span data-stu-id="9827c-459">167</span></span>

<span data-ttu-id="9827c-460">Autenticazione mapping certificati client IIS</span><span class="sxs-lookup"><span data-stu-id="9827c-460">IIS Client Certificate Mapping Authentication</span></span>

<span data-ttu-id="9827c-461">168</span><span class="sxs-lookup"><span data-stu-id="9827c-461">168</span></span>

<span data-ttu-id="9827c-462">Autorizzazione URL</span><span class="sxs-lookup"><span data-stu-id="9827c-462">URL Authorization</span></span>

<span data-ttu-id="9827c-463">169</span><span class="sxs-lookup"><span data-stu-id="9827c-463">169</span></span>

<span data-ttu-id="9827c-464">Filtro richieste</span><span class="sxs-lookup"><span data-stu-id="9827c-464">Request Filtering</span></span>

<span data-ttu-id="9827c-465">170</span><span class="sxs-lookup"><span data-stu-id="9827c-465">170</span></span>

<span data-ttu-id="9827c-466">Restrizioni per IP e domini</span><span class="sxs-lookup"><span data-stu-id="9827c-466">IP And Domain Restrictions</span></span>

<span data-ttu-id="9827c-467">171</span><span class="sxs-lookup"><span data-stu-id="9827c-467">171</span></span>

<span data-ttu-id="9827c-468">Prestazioni</span><span class="sxs-lookup"><span data-stu-id="9827c-468">Performance</span></span>

<span data-ttu-id="9827c-469">172</span><span class="sxs-lookup"><span data-stu-id="9827c-469">172</span></span>

<span data-ttu-id="9827c-470">Compressione contenuto statico</span><span class="sxs-lookup"><span data-stu-id="9827c-470">Static Content Compression</span></span>

<span data-ttu-id="9827c-471">173</span><span class="sxs-lookup"><span data-stu-id="9827c-471">173</span></span>

<span data-ttu-id="9827c-472">Compressione contenuto dinamico</span><span class="sxs-lookup"><span data-stu-id="9827c-472">Dynamic Content Compression</span></span>

<span data-ttu-id="9827c-473">174</span><span class="sxs-lookup"><span data-stu-id="9827c-473">174</span></span>

<span data-ttu-id="9827c-474">Strumenti di gestione</span><span class="sxs-lookup"><span data-stu-id="9827c-474">Management Tools</span></span>

<span data-ttu-id="9827c-475">175</span><span class="sxs-lookup"><span data-stu-id="9827c-475">175</span></span>

<span data-ttu-id="9827c-476">Console di gestione IIS</span><span class="sxs-lookup"><span data-stu-id="9827c-476">IIS Management Console</span></span>

<span data-ttu-id="9827c-477">176</span><span class="sxs-lookup"><span data-stu-id="9827c-477">176</span></span>

<span data-ttu-id="9827c-478">Strumenti e script di gestione IIS</span><span class="sxs-lookup"><span data-stu-id="9827c-478">IIS Management Scripts And Tools</span></span>

<span data-ttu-id="9827c-479">177</span><span class="sxs-lookup"><span data-stu-id="9827c-479">177</span></span>

<span data-ttu-id="9827c-480">Servizio di gestione</span><span class="sxs-lookup"><span data-stu-id="9827c-480">Management Service</span></span>

<span data-ttu-id="9827c-481">178</span><span class="sxs-lookup"><span data-stu-id="9827c-481">178</span></span>

<span data-ttu-id="9827c-482">Compatibilità Gestione IIS 6</span><span class="sxs-lookup"><span data-stu-id="9827c-482">IIS 6 Management Compatibility</span></span>

<span data-ttu-id="9827c-483">179</span><span class="sxs-lookup"><span data-stu-id="9827c-483">179</span></span>

<span data-ttu-id="9827c-484">Compatibilità Metabase IIS 6</span><span class="sxs-lookup"><span data-stu-id="9827c-484">IIS 6 Metabase Compatibility</span></span>

<span data-ttu-id="9827c-485">180</span><span class="sxs-lookup"><span data-stu-id="9827c-485">180</span></span>

<span data-ttu-id="9827c-486">Compatibilità WMI IIS 6</span><span class="sxs-lookup"><span data-stu-id="9827c-486">IIS 6 WMI Compatibility</span></span>

<span data-ttu-id="9827c-487">181</span><span class="sxs-lookup"><span data-stu-id="9827c-487">181</span></span>

<span data-ttu-id="9827c-488">Strumenti di scripting di IIS 6</span><span class="sxs-lookup"><span data-stu-id="9827c-488">IIS 6 Scripting Tools</span></span>

<span data-ttu-id="9827c-489">182</span><span class="sxs-lookup"><span data-stu-id="9827c-489">182</span></span>

<span data-ttu-id="9827c-490">Console di gestione IIS 6</span><span class="sxs-lookup"><span data-stu-id="9827c-490">IIS 6 Management Console</span></span>

<span data-ttu-id="9827c-491">183</span><span class="sxs-lookup"><span data-stu-id="9827c-491">183</span></span>

<span data-ttu-id="9827c-492">Servizio di pubblicazione FTP</span><span class="sxs-lookup"><span data-stu-id="9827c-492">FTP Publishing Service</span></span><br/>

<span data-ttu-id="9827c-493">184</span><span class="sxs-lookup"><span data-stu-id="9827c-493">184</span></span>

<span data-ttu-id="9827c-494">Server FTP</span><span class="sxs-lookup"><span data-stu-id="9827c-494">FTP Server</span></span>

<span data-ttu-id="9827c-495">185</span><span class="sxs-lookup"><span data-stu-id="9827c-495">185</span></span>

<span data-ttu-id="9827c-496">Console di gestione FTP</span><span class="sxs-lookup"><span data-stu-id="9827c-496">FTP Management Console</span></span><br/>

<span data-ttu-id="9827c-497">314</span><span class="sxs-lookup"><span data-stu-id="9827c-497">314</span></span>

<span data-ttu-id="9827c-498">Pubblicazione WebDAV</span><span class="sxs-lookup"><span data-stu-id="9827c-498">WebDAV Publishing</span></span>

<span data-ttu-id="9827c-499">316</span><span class="sxs-lookup"><span data-stu-id="9827c-499">316</span></span>

<span data-ttu-id="9827c-500">Servizio FTP</span><span class="sxs-lookup"><span data-stu-id="9827c-500">FTP Service</span></span><br/>

<span data-ttu-id="9827c-501">317</span><span class="sxs-lookup"><span data-stu-id="9827c-501">317</span></span>

<span data-ttu-id="9827c-502">Estendibilità FTP</span><span class="sxs-lookup"><span data-stu-id="9827c-502">FTP Extensibility</span></span><br/>

<span data-ttu-id="9827c-503">336</span><span class="sxs-lookup"><span data-stu-id="9827c-503">336</span></span>

<span data-ttu-id="9827c-504">HWC (Hostable Web Core) di IIS</span><span class="sxs-lookup"><span data-stu-id="9827c-504">IIS Hostable Web Core</span></span><br/>

<span data-ttu-id="9827c-505">413</span><span class="sxs-lookup"><span data-stu-id="9827c-505">413</span></span>

[<span data-ttu-id="9827c-506">ASP.NET 4.5</span><span class="sxs-lookup"><span data-stu-id="9827c-506">ASP.NET 4.5</span></span>](/windows)

<span data-ttu-id="9827c-507">414</span><span class="sxs-lookup"><span data-stu-id="9827c-507">414</span></span>

[<span data-ttu-id="9827c-508">Estendibilità .NET 4.5</span><span class="sxs-lookup"><span data-stu-id="9827c-508">.NET Extensibility 4.5</span></span>](/windows)

<span data-ttu-id="9827c-509">445</span><span class="sxs-lookup"><span data-stu-id="9827c-509">445</span></span>

[<span data-ttu-id="9827c-510">appialization</span><span class="sxs-lookup"><span data-stu-id="9827c-510">appialization</span></span>](/windows)

<span data-ttu-id="9827c-511">446</span><span class="sxs-lookup"><span data-stu-id="9827c-511">446</span></span>

[<span data-ttu-id="9827c-512">Supporto certificato SSL centralizzato</span><span class="sxs-lookup"><span data-stu-id="9827c-512">Centralized SSL Certificate Support</span></span>](/windows)

<span data-ttu-id="9827c-513">447</span><span class="sxs-lookup"><span data-stu-id="9827c-513">447</span></span>

[<span data-ttu-id="9827c-514">Protocollo WebSocket</span><span class="sxs-lookup"><span data-stu-id="9827c-514">WebSocket Protocol</span></span>](/windows)

<span data-ttu-id="9827c-515">Accodamento messaggi-funzionalità (49)</span><span class="sxs-lookup"><span data-stu-id="9827c-515">Message Queuing - Features (49)</span></span>

<span data-ttu-id="9827c-516">Valore</span><span class="sxs-lookup"><span data-stu-id="9827c-516">Value</span></span>

<span data-ttu-id="9827c-517">Nome</span><span class="sxs-lookup"><span data-stu-id="9827c-517">Name</span></span>

<span data-ttu-id="9827c-518">190</span><span class="sxs-lookup"><span data-stu-id="9827c-518">190</span></span>

<span data-ttu-id="9827c-519">Servizi di Accodamento messaggi</span><span class="sxs-lookup"><span data-stu-id="9827c-519">Message Queuing Services</span></span>

<span data-ttu-id="9827c-520">191</span><span class="sxs-lookup"><span data-stu-id="9827c-520">191</span></span>

<span data-ttu-id="9827c-521">Message Queuing Server</span><span class="sxs-lookup"><span data-stu-id="9827c-521">Message Queuing Server</span></span>

<span data-ttu-id="9827c-522">192</span><span class="sxs-lookup"><span data-stu-id="9827c-522">192</span></span>

<span data-ttu-id="9827c-523">Integrazione servizio directory</span><span class="sxs-lookup"><span data-stu-id="9827c-523">Directory Service Integration</span></span>

<span data-ttu-id="9827c-524">193</span><span class="sxs-lookup"><span data-stu-id="9827c-524">193</span></span>

<span data-ttu-id="9827c-525">Trigger di Accodamento messaggi</span><span class="sxs-lookup"><span data-stu-id="9827c-525">Message Queuing Triggers</span></span>

<span data-ttu-id="9827c-526">194</span><span class="sxs-lookup"><span data-stu-id="9827c-526">194</span></span>

<span data-ttu-id="9827c-527">Supporto HTTP</span><span class="sxs-lookup"><span data-stu-id="9827c-527">HTTP Support</span></span>

<span data-ttu-id="9827c-528">195</span><span class="sxs-lookup"><span data-stu-id="9827c-528">195</span></span>

<span data-ttu-id="9827c-529">Servizio di routing</span><span class="sxs-lookup"><span data-stu-id="9827c-529">Routing Service</span></span>

<span data-ttu-id="9827c-530">196</span><span class="sxs-lookup"><span data-stu-id="9827c-530">196</span></span>

[<span data-ttu-id="9827c-531">Supporto client Windows 2000</span><span class="sxs-lookup"><span data-stu-id="9827c-531">Windows 2000 Client Support</span></span>](/windows)<br/>

<span data-ttu-id="9827c-532">197</span><span class="sxs-lookup"><span data-stu-id="9827c-532">197</span></span>

<span data-ttu-id="9827c-533">Proxy DCOM di Accodamento messaggi</span><span class="sxs-lookup"><span data-stu-id="9827c-533">Message Queuing DCOM Proxy</span></span>

<span data-ttu-id="9827c-534">228</span><span class="sxs-lookup"><span data-stu-id="9827c-534">228</span></span>

<span data-ttu-id="9827c-535">Supporto multicast</span><span class="sxs-lookup"><span data-stu-id="9827c-535">Multicasting Support</span></span>

<span data-ttu-id="9827c-536">Servizi certificati Active Directory-servizi ruolo (16)</span><span class="sxs-lookup"><span data-stu-id="9827c-536">Active Directory Certificate Services - Role Services (16)</span></span>

<span data-ttu-id="9827c-537">Valore</span><span class="sxs-lookup"><span data-stu-id="9827c-537">Value</span></span>

<span data-ttu-id="9827c-538">Nome</span><span class="sxs-lookup"><span data-stu-id="9827c-538">Name</span></span>

<span data-ttu-id="9827c-539">200</span><span class="sxs-lookup"><span data-stu-id="9827c-539">200</span></span>

<span data-ttu-id="9827c-540">Autorità di certificazione</span><span class="sxs-lookup"><span data-stu-id="9827c-540">Certification Authority</span></span>

<span data-ttu-id="9827c-541">201</span><span class="sxs-lookup"><span data-stu-id="9827c-541">201</span></span>

<span data-ttu-id="9827c-542">Registrazione Web Autorità di certificazione</span><span class="sxs-lookup"><span data-stu-id="9827c-542">Certification Authority Web Enrollment</span></span>

<span data-ttu-id="9827c-543">202</span><span class="sxs-lookup"><span data-stu-id="9827c-543">202</span></span>

<span data-ttu-id="9827c-544">Risponditore online</span><span class="sxs-lookup"><span data-stu-id="9827c-544">Online Responder</span></span>

<span data-ttu-id="9827c-545">204</span><span class="sxs-lookup"><span data-stu-id="9827c-545">204</span></span>

<span data-ttu-id="9827c-546">Servizio Registrazione dispositivi di rete</span><span class="sxs-lookup"><span data-stu-id="9827c-546">Network Device Enrollment Service</span></span>

<span data-ttu-id="9827c-547">318</span><span class="sxs-lookup"><span data-stu-id="9827c-547">318</span></span>

[<span data-ttu-id="9827c-548">Servizio Web di registrazione certificati</span><span class="sxs-lookup"><span data-stu-id="9827c-548">Certificate Enrollment Web Service</span></span>](/windows)<br/>

<span data-ttu-id="9827c-549">319</span><span class="sxs-lookup"><span data-stu-id="9827c-549">319</span></span>

[<span data-ttu-id="9827c-550">Servizio Web di informazioni sulle registrazioni di certificati</span><span class="sxs-lookup"><span data-stu-id="9827c-550">Certificate Enrollment Policy Web Service</span></span>](/windows)<br/>

<span data-ttu-id="9827c-551">Servizi di accesso e criteri di rete-servizi ruolo (14)</span><span class="sxs-lookup"><span data-stu-id="9827c-551">Network Policy and Access Services - Role Services (14)</span></span>

<span data-ttu-id="9827c-552">Valore</span><span class="sxs-lookup"><span data-stu-id="9827c-552">Value</span></span>

<span data-ttu-id="9827c-553">Nome</span><span class="sxs-lookup"><span data-stu-id="9827c-553">Name</span></span>

<span data-ttu-id="9827c-554">205</span><span class="sxs-lookup"><span data-stu-id="9827c-554">205</span></span>

[<span data-ttu-id="9827c-555">Server dei criteri di rete</span><span class="sxs-lookup"><span data-stu-id="9827c-555">Network Policy Server</span></span>](/windows)

<span data-ttu-id="9827c-556">206</span><span class="sxs-lookup"><span data-stu-id="9827c-556">206</span></span>

[<span data-ttu-id="9827c-557">VPN</span><span class="sxs-lookup"><span data-stu-id="9827c-557">VPN</span></span>](#vpn)

<span data-ttu-id="9827c-558">207</span><span class="sxs-lookup"><span data-stu-id="9827c-558">207</span></span>

[<span data-ttu-id="9827c-559">Servizi di accesso remoto</span><span class="sxs-lookup"><span data-stu-id="9827c-559">Remote Access Services</span></span>](/windows)

<span data-ttu-id="9827c-560">208</span><span class="sxs-lookup"><span data-stu-id="9827c-560">208</span></span>

[<span data-ttu-id="9827c-561">Routing</span><span class="sxs-lookup"><span data-stu-id="9827c-561">Routing</span></span>](#routing)

<span data-ttu-id="9827c-562">210</span><span class="sxs-lookup"><span data-stu-id="9827c-562">210</span></span>

[<span data-ttu-id="9827c-563">Autorità registrazione integrità</span><span class="sxs-lookup"><span data-stu-id="9827c-563">Health Registration Authority</span></span>](/windows)

<span data-ttu-id="9827c-564">250</span><span class="sxs-lookup"><span data-stu-id="9827c-564">250</span></span>

[<span data-ttu-id="9827c-565">Protocollo di autorizzazione Host Credential</span><span class="sxs-lookup"><span data-stu-id="9827c-565">Host Credential Authorization Protocol</span></span>](/windows)

<span data-ttu-id="9827c-566">Servizi UDDI-servizi ruolo (11)</span><span class="sxs-lookup"><span data-stu-id="9827c-566">UDDI Services - Role Services (11)</span></span>

<span data-ttu-id="9827c-567">Valore</span><span class="sxs-lookup"><span data-stu-id="9827c-567">Value</span></span>

<span data-ttu-id="9827c-568">Nome</span><span class="sxs-lookup"><span data-stu-id="9827c-568">Name</span></span>

<span data-ttu-id="9827c-569">215</span><span class="sxs-lookup"><span data-stu-id="9827c-569">215</span></span>

[<span data-ttu-id="9827c-570">Applicazione Web Servizi UDDI</span><span class="sxs-lookup"><span data-stu-id="9827c-570">UDDI Services Web Application</span></span>](/windows)<br/>

<span data-ttu-id="9827c-571">216</span><span class="sxs-lookup"><span data-stu-id="9827c-571">216</span></span>

[<span data-ttu-id="9827c-572">Database dei servizi UDDI</span><span class="sxs-lookup"><span data-stu-id="9827c-572">UDDI Services Database</span></span>](/windows)<br/>

<span data-ttu-id="9827c-573">Servizio Attivazione processo Windows-servizi ruolo (41)</span><span class="sxs-lookup"><span data-stu-id="9827c-573">Windows Process Activation Service - Role Services (41)</span></span>

<span data-ttu-id="9827c-574">Valore</span><span class="sxs-lookup"><span data-stu-id="9827c-574">Value</span></span>

<span data-ttu-id="9827c-575">Nome</span><span class="sxs-lookup"><span data-stu-id="9827c-575">Name</span></span>

<span data-ttu-id="9827c-576">217</span><span class="sxs-lookup"><span data-stu-id="9827c-576">217</span></span>

<span data-ttu-id="9827c-577">API di configurazione</span><span class="sxs-lookup"><span data-stu-id="9827c-577">Configuration API</span></span>

<span data-ttu-id="9827c-578">218</span><span class="sxs-lookup"><span data-stu-id="9827c-578">218</span></span>

<span data-ttu-id="9827c-579">Ambiente .NET</span><span class="sxs-lookup"><span data-stu-id="9827c-579">.NET Environment</span></span>

<span data-ttu-id="9827c-580">219</span><span class="sxs-lookup"><span data-stu-id="9827c-580">219</span></span>

<span data-ttu-id="9827c-581">Modello di processo</span><span class="sxs-lookup"><span data-stu-id="9827c-581">Process Model</span></span>

<span data-ttu-id="9827c-582">.NET Framework 3.5.1-funzionalità (36)</span><span class="sxs-lookup"><span data-stu-id="9827c-582">.NET Framework 3.5.1 - Features (36)</span></span>

<span data-ttu-id="9827c-583">Valore</span><span class="sxs-lookup"><span data-stu-id="9827c-583">Value</span></span>

<span data-ttu-id="9827c-584">Nome</span><span class="sxs-lookup"><span data-stu-id="9827c-584">Name</span></span>

<span data-ttu-id="9827c-585">220</span><span class="sxs-lookup"><span data-stu-id="9827c-585">220</span></span>

<span data-ttu-id="9827c-586">.NET Framework 3.5.1</span><span class="sxs-lookup"><span data-stu-id="9827c-586">.NET Framework 3.5.1</span></span><br/> [<span data-ttu-id="9827c-587">modifica nome</span><span class="sxs-lookup"><span data-stu-id="9827c-587">name change</span></span>](/windows)<br/>

<span data-ttu-id="9827c-588">221</span><span class="sxs-lookup"><span data-stu-id="9827c-588">221</span></span>

<span data-ttu-id="9827c-589">Attivazione di WCF</span><span class="sxs-lookup"><span data-stu-id="9827c-589">WCF Activation</span></span>

<span data-ttu-id="9827c-590">222</span><span class="sxs-lookup"><span data-stu-id="9827c-590">222</span></span>

<span data-ttu-id="9827c-591">Attivazione HTTP</span><span class="sxs-lookup"><span data-stu-id="9827c-591">HTTP Activation</span></span>

<span data-ttu-id="9827c-592">223</span><span class="sxs-lookup"><span data-stu-id="9827c-592">223</span></span>

<span data-ttu-id="9827c-593">Attivazione non HTTP</span><span class="sxs-lookup"><span data-stu-id="9827c-593">Non-HTTP Activation</span></span>

<span data-ttu-id="9827c-594">227</span><span class="sxs-lookup"><span data-stu-id="9827c-594">227</span></span>

<span data-ttu-id="9827c-595">XPS Viewer</span><span class="sxs-lookup"><span data-stu-id="9827c-595">XPS Viewer</span></span><br/>

<span data-ttu-id="9827c-596">Servizi SNMP-funzionalità (59)</span><span class="sxs-lookup"><span data-stu-id="9827c-596">SNMP Services - Features (59)</span></span>

<span data-ttu-id="9827c-597">Valore</span><span class="sxs-lookup"><span data-stu-id="9827c-597">Value</span></span>

<span data-ttu-id="9827c-598">Nome</span><span class="sxs-lookup"><span data-stu-id="9827c-598">Name</span></span>

<span data-ttu-id="9827c-599">224</span><span class="sxs-lookup"><span data-stu-id="9827c-599">224</span></span>

[<span data-ttu-id="9827c-600">Servizio SNMP</span><span class="sxs-lookup"><span data-stu-id="9827c-600">SNMP Service</span></span>](/windows)

<span data-ttu-id="9827c-601">225</span><span class="sxs-lookup"><span data-stu-id="9827c-601">225</span></span>

[<span data-ttu-id="9827c-602">Provider WMI SNMP</span><span class="sxs-lookup"><span data-stu-id="9827c-602">SNMP WMI Provider</span></span>](/windows)

<span data-ttu-id="9827c-603">Servizi ruolo Servizi per le applicazioni</span><span class="sxs-lookup"><span data-stu-id="9827c-603">Application Services - Role Services</span></span>

<span data-ttu-id="9827c-604">Valore</span><span class="sxs-lookup"><span data-stu-id="9827c-604">Value</span></span>

<span data-ttu-id="9827c-605">Nome</span><span class="sxs-lookup"><span data-stu-id="9827c-605">Name</span></span>

<span data-ttu-id="9827c-606">230</span><span class="sxs-lookup"><span data-stu-id="9827c-606">230</span></span>

[<span data-ttu-id="9827c-607">.NET Framework 3.5.1</span><span class="sxs-lookup"><span data-stu-id="9827c-607">.NET Framework 3.5.1</span></span>](/windows)<br/> [<span data-ttu-id="9827c-608">modifica nome</span><span class="sxs-lookup"><span data-stu-id="9827c-608">name change</span></span>](/windows)<br/>

<span data-ttu-id="9827c-609">231</span><span class="sxs-lookup"><span data-stu-id="9827c-609">231</span></span>

[<span data-ttu-id="9827c-610">Supporto server Web (IIS)</span><span class="sxs-lookup"><span data-stu-id="9827c-610">Web Server (IIS) Support</span></span>](/windows)

<span data-ttu-id="9827c-611">232</span><span class="sxs-lookup"><span data-stu-id="9827c-611">232</span></span>

[<span data-ttu-id="9827c-612">Accesso alla rete COM+</span><span class="sxs-lookup"><span data-stu-id="9827c-612">COM+ Network Access</span></span>](/windows)

<span data-ttu-id="9827c-613">233</span><span class="sxs-lookup"><span data-stu-id="9827c-613">233</span></span>

[<span data-ttu-id="9827c-614">Condivisione delle porte TCP</span><span class="sxs-lookup"><span data-stu-id="9827c-614">TCP Port Sharing</span></span>](/windows)

<span data-ttu-id="9827c-615">234</span><span class="sxs-lookup"><span data-stu-id="9827c-615">234</span></span>

[<span data-ttu-id="9827c-616">Supporto del servizio Attivazione processo Windows</span><span class="sxs-lookup"><span data-stu-id="9827c-616">Windows Process Activation Service Support</span></span>](/windows)

<span data-ttu-id="9827c-617">235</span><span class="sxs-lookup"><span data-stu-id="9827c-617">235</span></span>

[<span data-ttu-id="9827c-618">Attivazione HTTP</span><span class="sxs-lookup"><span data-stu-id="9827c-618">HTTP Activation</span></span>](/windows)

<span data-ttu-id="9827c-619">236</span><span class="sxs-lookup"><span data-stu-id="9827c-619">236</span></span>

[<span data-ttu-id="9827c-620">Attivazione di Accodamento messaggi</span><span class="sxs-lookup"><span data-stu-id="9827c-620">Message Queuing Activation</span></span>](/windows)

<span data-ttu-id="9827c-621">237</span><span class="sxs-lookup"><span data-stu-id="9827c-621">237</span></span>

[<span data-ttu-id="9827c-622">Attivazione TCP</span><span class="sxs-lookup"><span data-stu-id="9827c-622">TCP Activation</span></span>](/windows)

<span data-ttu-id="9827c-623">238</span><span class="sxs-lookup"><span data-stu-id="9827c-623">238</span></span>

[<span data-ttu-id="9827c-624">Attivazione named pipe</span><span class="sxs-lookup"><span data-stu-id="9827c-624">Named Pipes Activation</span></span>](/windows)

<span data-ttu-id="9827c-625">239</span><span class="sxs-lookup"><span data-stu-id="9827c-625">239</span></span>

[<span data-ttu-id="9827c-626">Transazioni distribuite</span><span class="sxs-lookup"><span data-stu-id="9827c-626">Distributed Transactions</span></span>](/windows)

<span data-ttu-id="9827c-627">240</span><span class="sxs-lookup"><span data-stu-id="9827c-627">240</span></span>

[<span data-ttu-id="9827c-628">Transazioni remote in ingresso</span><span class="sxs-lookup"><span data-stu-id="9827c-628">Incoming Remote Transactions</span></span>](/windows)

<span data-ttu-id="9827c-629">241</span><span class="sxs-lookup"><span data-stu-id="9827c-629">241</span></span>

[<span data-ttu-id="9827c-630">Transazioni remote in uscita</span><span class="sxs-lookup"><span data-stu-id="9827c-630">Outgoing Remote Transactions</span></span>](/windows)

<span data-ttu-id="9827c-631">242</span><span class="sxs-lookup"><span data-stu-id="9827c-631">242</span></span>

[<span data-ttu-id="9827c-632">Transazioni WS-automatiche</span><span class="sxs-lookup"><span data-stu-id="9827c-632">WS-Automatic Transactions</span></span>](/windows)

<span data-ttu-id="9827c-633">353</span><span class="sxs-lookup"><span data-stu-id="9827c-633">353</span></span>

[<span data-ttu-id="9827c-634">Estensioni del server applicazioni per .NET 4,0</span><span class="sxs-lookup"><span data-stu-id="9827c-634">Application Server Extensions for .NET 4.0</span></span>](/windows)<br/>

<span data-ttu-id="9827c-635">Servizi di distribuzione Windows-ruolo (19)</span><span class="sxs-lookup"><span data-stu-id="9827c-635">Windows Deployment Services - Role (19)</span></span>

<span data-ttu-id="9827c-636">Valore</span><span class="sxs-lookup"><span data-stu-id="9827c-636">Value</span></span>

<span data-ttu-id="9827c-637">Nome</span><span class="sxs-lookup"><span data-stu-id="9827c-637">Name</span></span>

<span data-ttu-id="9827c-638">251</span><span class="sxs-lookup"><span data-stu-id="9827c-638">251</span></span>

<span data-ttu-id="9827c-639">Server di distribuzione</span><span class="sxs-lookup"><span data-stu-id="9827c-639">Deployment Server</span></span>

<span data-ttu-id="9827c-640">252</span><span class="sxs-lookup"><span data-stu-id="9827c-640">252</span></span>

<span data-ttu-id="9827c-641">Server di trasporto</span><span class="sxs-lookup"><span data-stu-id="9827c-641">Transport Server</span></span>

<span data-ttu-id="9827c-642">Servizi ruolo Active Directory Rights Management Services (17)</span><span class="sxs-lookup"><span data-stu-id="9827c-642">Active Directory Rights Management Services - Role Services (17)</span></span>

<span data-ttu-id="9827c-643">Valore</span><span class="sxs-lookup"><span data-stu-id="9827c-643">Value</span></span>

<span data-ttu-id="9827c-644">Nome</span><span class="sxs-lookup"><span data-stu-id="9827c-644">Name</span></span>

<span data-ttu-id="9827c-645">253</span><span class="sxs-lookup"><span data-stu-id="9827c-645">253</span></span>

<span data-ttu-id="9827c-646">Server AD RMS (Active Directory Rights Management Services)</span><span class="sxs-lookup"><span data-stu-id="9827c-646">Active Directory Rights Management Server</span></span>

<span data-ttu-id="9827c-647">254</span><span class="sxs-lookup"><span data-stu-id="9827c-647">254</span></span>

<span data-ttu-id="9827c-648">Supporto federazione identità</span><span class="sxs-lookup"><span data-stu-id="9827c-648">Identity Federation Support</span></span>

<span data-ttu-id="9827c-649">Strumenti di amministrazione remota del server (67)</span><span class="sxs-lookup"><span data-stu-id="9827c-649">Remote Server Administration Tools (67)</span></span>

<span data-ttu-id="9827c-650">Valore</span><span class="sxs-lookup"><span data-stu-id="9827c-650">Value</span></span>

<span data-ttu-id="9827c-651">Nome</span><span class="sxs-lookup"><span data-stu-id="9827c-651">Name</span></span>

<span data-ttu-id="9827c-652">256</span><span class="sxs-lookup"><span data-stu-id="9827c-652">256</span></span>

[<span data-ttu-id="9827c-653">Strumenti di amministrazione ruoli</span><span class="sxs-lookup"><span data-stu-id="9827c-653">Role Administration Tools</span></span>](/windows)

<span data-ttu-id="9827c-654">257</span><span class="sxs-lookup"><span data-stu-id="9827c-654">257</span></span>

[<span data-ttu-id="9827c-655">Strumenti di Servizi di dominio Active Directory</span><span class="sxs-lookup"><span data-stu-id="9827c-655">AD DS Tools</span></span>](/windows)<br/> [<span data-ttu-id="9827c-656">modifica nome</span><span class="sxs-lookup"><span data-stu-id="9827c-656">name change</span></span>](/windows)<br/>

<span data-ttu-id="9827c-657">258</span><span class="sxs-lookup"><span data-stu-id="9827c-657">258</span></span>

[<span data-ttu-id="9827c-658">Strumenti di AD LDS Snap-Ins e Command-Line</span><span class="sxs-lookup"><span data-stu-id="9827c-658">AD LDS Snap-Ins and Command-Line Tools</span></span>](/windows)<br/> [<span data-ttu-id="9827c-659">modifica nome</span><span class="sxs-lookup"><span data-stu-id="9827c-659">name change</span></span>](/windows)<br/>

<span data-ttu-id="9827c-660">259</span><span class="sxs-lookup"><span data-stu-id="9827c-660">259</span></span>

<span data-ttu-id="9827c-661">Strumenti per Servizi certificati Active Directory</span><span class="sxs-lookup"><span data-stu-id="9827c-661">Active Directory Certificate Services Tools</span></span>

<span data-ttu-id="9827c-662">260</span><span class="sxs-lookup"><span data-stu-id="9827c-662">260</span></span>

[<span data-ttu-id="9827c-663">Servizi di accesso e criteri di rete</span><span class="sxs-lookup"><span data-stu-id="9827c-663">Network Policy and Access Services</span></span>](/windows)

<span data-ttu-id="9827c-664">261</span><span class="sxs-lookup"><span data-stu-id="9827c-664">261</span></span>

<span data-ttu-id="9827c-665">Strumenti di Servizi di stampa e digitalizzazione</span><span class="sxs-lookup"><span data-stu-id="9827c-665">Print and Document Services Tools</span></span><br/> [<span data-ttu-id="9827c-666">modifica nome</span><span class="sxs-lookup"><span data-stu-id="9827c-666">name change</span></span>](/windows)<br/>

<span data-ttu-id="9827c-667">262</span><span class="sxs-lookup"><span data-stu-id="9827c-667">262</span></span>

[<span data-ttu-id="9827c-668">Active Directory Rights Management Services</span><span class="sxs-lookup"><span data-stu-id="9827c-668">Active Directory Rights Management Services</span></span>](/windows)

<span data-ttu-id="9827c-669">263</span><span class="sxs-lookup"><span data-stu-id="9827c-669">263</span></span>

[<span data-ttu-id="9827c-670">Strumenti di Servizi Desktop remoto</span><span class="sxs-lookup"><span data-stu-id="9827c-670">Remote Desktop Services Tools</span></span>](/windows)<br/> [<span data-ttu-id="9827c-671">modifica nome</span><span class="sxs-lookup"><span data-stu-id="9827c-671">name change</span></span>](/windows)<br/>

<span data-ttu-id="9827c-672">264</span><span class="sxs-lookup"><span data-stu-id="9827c-672">264</span></span>

<span data-ttu-id="9827c-673">Strumenti di servizi di distribuzione Windows</span><span class="sxs-lookup"><span data-stu-id="9827c-673">Windows Deployment Services Tools</span></span>

<span data-ttu-id="9827c-674">265</span><span class="sxs-lookup"><span data-stu-id="9827c-674">265</span></span>

[<span data-ttu-id="9827c-675">Strumenti di amministrazione funzionalità</span><span class="sxs-lookup"><span data-stu-id="9827c-675">Feature Administration Tools</span></span>](/windows)

<span data-ttu-id="9827c-676">266</span><span class="sxs-lookup"><span data-stu-id="9827c-676">266</span></span>

<span data-ttu-id="9827c-677">BitLocker Drive Encryption Tools</span><span class="sxs-lookup"><span data-stu-id="9827c-677">BitLocker Drive Encryption Tools</span></span>

<span data-ttu-id="9827c-678">267</span><span class="sxs-lookup"><span data-stu-id="9827c-678">267</span></span>

<span data-ttu-id="9827c-679">Strumenti per Estensioni server BITS</span><span class="sxs-lookup"><span data-stu-id="9827c-679">BITS Server Extensions Tools</span></span>

<span data-ttu-id="9827c-680">268</span><span class="sxs-lookup"><span data-stu-id="9827c-680">268</span></span>

[<span data-ttu-id="9827c-681">Strumenti per Clustering di failover</span><span class="sxs-lookup"><span data-stu-id="9827c-681">Failover Clustering Tools</span></span>](/windows)

<span data-ttu-id="9827c-682">269</span><span class="sxs-lookup"><span data-stu-id="9827c-682">269</span></span>

<span data-ttu-id="9827c-683">Strumenti di bilanciamento carico di rete</span><span class="sxs-lookup"><span data-stu-id="9827c-683">Network Load Balancing Tools</span></span>

<span data-ttu-id="9827c-684">270</span><span class="sxs-lookup"><span data-stu-id="9827c-684">270</span></span>

<span data-ttu-id="9827c-685">Strumenti server SMTP</span><span class="sxs-lookup"><span data-stu-id="9827c-685">SMTP Server Tools</span></span>

<span data-ttu-id="9827c-686">273</span><span class="sxs-lookup"><span data-stu-id="9827c-686">273</span></span>

[<span data-ttu-id="9827c-687">Strumenti server DNS</span><span class="sxs-lookup"><span data-stu-id="9827c-687">DNS Server Tools</span></span>](/windows)

<span data-ttu-id="9827c-688">277</span><span class="sxs-lookup"><span data-stu-id="9827c-688">277</span></span>

<span data-ttu-id="9827c-689">Strumenti per servizi file</span><span class="sxs-lookup"><span data-stu-id="9827c-689">File Services Tools</span></span>

<span data-ttu-id="9827c-690">278</span><span class="sxs-lookup"><span data-stu-id="9827c-690">278</span></span>

<span data-ttu-id="9827c-691">Strumenti di file system distribuito</span><span class="sxs-lookup"><span data-stu-id="9827c-691">Distributed File System Tools</span></span>

<span data-ttu-id="9827c-692">279</span><span class="sxs-lookup"><span data-stu-id="9827c-692">279</span></span>

<span data-ttu-id="9827c-693">Strumenti per Gestione risorse file server</span><span class="sxs-lookup"><span data-stu-id="9827c-693">File Server Resource Manager Tools</span></span>

<span data-ttu-id="9827c-694">280</span><span class="sxs-lookup"><span data-stu-id="9827c-694">280</span></span>

[<span data-ttu-id="9827c-695">Servizi per gli strumenti del file System di rete</span><span class="sxs-lookup"><span data-stu-id="9827c-695">Services For Network File System Tools</span></span>](/windows)

<span data-ttu-id="9827c-696">281</span><span class="sxs-lookup"><span data-stu-id="9827c-696">281</span></span>

<span data-ttu-id="9827c-697">Strumenti per server Web (IIS)</span><span class="sxs-lookup"><span data-stu-id="9827c-697">Web Server (IIS) Tools</span></span>

<span data-ttu-id="9827c-698">284</span><span class="sxs-lookup"><span data-stu-id="9827c-698">284</span></span>

[<span data-ttu-id="9827c-699">Strumenti di host sessione Desktop remoto</span><span class="sxs-lookup"><span data-stu-id="9827c-699">Remote Desktop Session Host Tools</span></span>](/windows)<br/> [<span data-ttu-id="9827c-700">modifica nome</span><span class="sxs-lookup"><span data-stu-id="9827c-700">name change</span></span>](/windows)<br/>

<span data-ttu-id="9827c-701">285</span><span class="sxs-lookup"><span data-stu-id="9827c-701">285</span></span>

<span data-ttu-id="9827c-702">Strumenti di Desktop remoto Gateway</span><span class="sxs-lookup"><span data-stu-id="9827c-702">Remote Desktop Gateway Tools</span></span><br/> [<span data-ttu-id="9827c-703">modifica nome</span><span class="sxs-lookup"><span data-stu-id="9827c-703">name change</span></span>](/windows)<br/>

<span data-ttu-id="9827c-704">286</span><span class="sxs-lookup"><span data-stu-id="9827c-704">286</span></span>

<span data-ttu-id="9827c-705">Strumenti di gestione licenze Desktop remoto</span><span class="sxs-lookup"><span data-stu-id="9827c-705">Remote Desktop Licensing Tools</span></span><br/> [<span data-ttu-id="9827c-706">modifica nome</span><span class="sxs-lookup"><span data-stu-id="9827c-706">name change</span></span>](/windows)<br/>

<span data-ttu-id="9827c-707">288</span><span class="sxs-lookup"><span data-stu-id="9827c-707">288</span></span>

<span data-ttu-id="9827c-708">Strumenti server fax</span><span class="sxs-lookup"><span data-stu-id="9827c-708">Fax Server Tools</span></span>

<span data-ttu-id="9827c-709">290</span><span class="sxs-lookup"><span data-stu-id="9827c-709">290</span></span>

<span data-ttu-id="9827c-710">Strumenti server WINS</span><span class="sxs-lookup"><span data-stu-id="9827c-710">WINS Server Tools</span></span>

<span data-ttu-id="9827c-711">291</span><span class="sxs-lookup"><span data-stu-id="9827c-711">291</span></span>

[<span data-ttu-id="9827c-712">Strumenti per Servizi UDDI</span><span class="sxs-lookup"><span data-stu-id="9827c-712">UDDI Services Tools</span></span>](/windows)<br/>

<span data-ttu-id="9827c-713">292</span><span class="sxs-lookup"><span data-stu-id="9827c-713">292</span></span>

<span data-ttu-id="9827c-714">Strumenti autorità di certificazione</span><span class="sxs-lookup"><span data-stu-id="9827c-714">Certification Authority Tools</span></span>

<span data-ttu-id="9827c-715">293</span><span class="sxs-lookup"><span data-stu-id="9827c-715">293</span></span>

<span data-ttu-id="9827c-716">Strumenti risponditore online</span><span class="sxs-lookup"><span data-stu-id="9827c-716">Online Responder Tools</span></span>

<span data-ttu-id="9827c-717">297</span><span class="sxs-lookup"><span data-stu-id="9827c-717">297</span></span>

[<span data-ttu-id="9827c-718">Strumenti di server per NIS</span><span class="sxs-lookup"><span data-stu-id="9827c-718">Server for NIS Tools</span></span>](/windows)

<span data-ttu-id="9827c-719">299</span><span class="sxs-lookup"><span data-stu-id="9827c-719">299</span></span>

[<span data-ttu-id="9827c-720">Snap-in e strumenti da riga di comando di Servizi di dominio Active Directory</span><span class="sxs-lookup"><span data-stu-id="9827c-720">AD DS Snap-Ins and Command-Line Tools</span></span>](/windows)<br/> [<span data-ttu-id="9827c-721">modifica nome</span><span class="sxs-lookup"><span data-stu-id="9827c-721">name change</span></span>](/windows)<br/>

<span data-ttu-id="9827c-722">300</span><span class="sxs-lookup"><span data-stu-id="9827c-722">300</span></span>

[<span data-ttu-id="9827c-723">Centro di amministrazione di Active Directory</span><span class="sxs-lookup"><span data-stu-id="9827c-723">Active Directory Administrative Center</span></span>](/windows)

<span data-ttu-id="9827c-724">301</span><span class="sxs-lookup"><span data-stu-id="9827c-724">301</span></span>

<span data-ttu-id="9827c-725">Strumenti di Hyper-V</span><span class="sxs-lookup"><span data-stu-id="9827c-725">Hyper-V Tools</span></span>

<span data-ttu-id="9827c-726">323</span><span class="sxs-lookup"><span data-stu-id="9827c-726">323</span></span>

[<span data-ttu-id="9827c-727">Visualizzatore password di ripristino BitLocker</span><span class="sxs-lookup"><span data-stu-id="9827c-727">BitLocker Recovery Password Viewer</span></span>](/windows)<br/>

<span data-ttu-id="9827c-728">326</span><span class="sxs-lookup"><span data-stu-id="9827c-728">326</span></span>

[<span data-ttu-id="9827c-729">Utilità di amministrazione di Crittografia unità BitLocker</span><span class="sxs-lookup"><span data-stu-id="9827c-729">BitLocker Drive Encryption Administration Utilities</span></span>](/windows)<br/>

<span data-ttu-id="9827c-730">329</span><span class="sxs-lookup"><span data-stu-id="9827c-730">329</span></span>

[<span data-ttu-id="9827c-731">Strumenti per Servizi di dominio Active Directory e AD LDS</span><span class="sxs-lookup"><span data-stu-id="9827c-731">AD DS and AD LDS Tools</span></span>](/windows)<br/>

<span data-ttu-id="9827c-732">330</span><span class="sxs-lookup"><span data-stu-id="9827c-732">330</span></span>

<span data-ttu-id="9827c-733">Centro di amministrazione di Active Directory</span><span class="sxs-lookup"><span data-stu-id="9827c-733">Active Directory Administrative Center</span></span><br/>

<span data-ttu-id="9827c-734">331</span><span class="sxs-lookup"><span data-stu-id="9827c-734">331</span></span>

[<span data-ttu-id="9827c-735">Modulo di Active Directory per Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="9827c-735">Active Directory module for Windows PowerShell</span></span>](/windows)<br/>

<span data-ttu-id="9827c-736">337</span><span class="sxs-lookup"><span data-stu-id="9827c-736">337</span></span>

[<span data-ttu-id="9827c-737">Strumenti di Connessione Desktop remoto broker</span><span class="sxs-lookup"><span data-stu-id="9827c-737">Remote Desktop Connection Broker Tools</span></span>](/windows)<br/>

<span data-ttu-id="9827c-738">410</span><span class="sxs-lookup"><span data-stu-id="9827c-738">410</span></span>

[<span data-ttu-id="9827c-739">Client di gestione indirizzi IP</span><span class="sxs-lookup"><span data-stu-id="9827c-739">IP Address Management (IPAM) Client</span></span>](/windows)

<span data-ttu-id="9827c-740">450</span><span class="sxs-lookup"><span data-stu-id="9827c-740">450</span></span>

[<span data-ttu-id="9827c-741">Modulo Hyper-V per Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="9827c-741">Hyper-V Module for Windows PowerShell</span></span>](/windows)

<span data-ttu-id="9827c-742">462</span><span class="sxs-lookup"><span data-stu-id="9827c-742">462</span></span>

[<span data-ttu-id="9827c-743">Strumenti di Active Directory Rights Management Services</span><span class="sxs-lookup"><span data-stu-id="9827c-743">Active Directory Rights Management Services Tools</span></span>](/windows)

<span data-ttu-id="9827c-744">465</span><span class="sxs-lookup"><span data-stu-id="9827c-744">465</span></span>

[<span data-ttu-id="9827c-745">Strumento di Gestione condivisione e archiviazione</span><span class="sxs-lookup"><span data-stu-id="9827c-745">Share and Storage Management Tool</span></span>](/windows)

<span data-ttu-id="9827c-746">471</span><span class="sxs-lookup"><span data-stu-id="9827c-746">471</span></span>

[<span data-ttu-id="9827c-747">Strumenti di gestione di accesso remoto</span><span class="sxs-lookup"><span data-stu-id="9827c-747">Remote Access Management Tools</span></span>](/windows)

<span data-ttu-id="9827c-748">472</span><span class="sxs-lookup"><span data-stu-id="9827c-748">472</span></span>

[<span data-ttu-id="9827c-749">Modulo Accesso remoto per Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="9827c-749">Remote Access module for Windows PowerShell</span></span>](/windows)

<span data-ttu-id="9827c-750">473</span><span class="sxs-lookup"><span data-stu-id="9827c-750">473</span></span>

[<span data-ttu-id="9827c-751">GUI di accesso remoto e strumenti di Command-Line</span><span class="sxs-lookup"><span data-stu-id="9827c-751">Remote Access GUI and Command-Line Tools</span></span>](/windows)

<span data-ttu-id="9827c-752">474</span><span class="sxs-lookup"><span data-stu-id="9827c-752">474</span></span>

[<span data-ttu-id="9827c-753">Strumenti di Windows Server Update Services</span><span class="sxs-lookup"><span data-stu-id="9827c-753">Windows Server Update Services Tools</span></span>](/windows)

<span data-ttu-id="9827c-754">476</span><span class="sxs-lookup"><span data-stu-id="9827c-754">476</span></span>

[<span data-ttu-id="9827c-755">Strumenti di diagnostica delle licenze Desktop remoto</span><span class="sxs-lookup"><span data-stu-id="9827c-755">Remote Desktop Licensing Diagnoser Tools</span></span>](/windows)

<span data-ttu-id="9827c-756">479</span><span class="sxs-lookup"><span data-stu-id="9827c-756">479</span></span>

[<span data-ttu-id="9827c-757">Strumenti SNMP</span><span class="sxs-lookup"><span data-stu-id="9827c-757">SNMP Tools</span></span>](/windows)

<span data-ttu-id="9827c-758">480</span><span class="sxs-lookup"><span data-stu-id="9827c-758">480</span></span>

[<span data-ttu-id="9827c-759">Strumenti di attivazione contratti multilicenza</span><span class="sxs-lookup"><span data-stu-id="9827c-759">Volume Activation Tools</span></span>](/windows)

<span data-ttu-id="9827c-760">Funzionalità di Windows Server Backup (39)</span><span class="sxs-lookup"><span data-stu-id="9827c-760">Windows Server Backup - Features (39)</span></span>

<span data-ttu-id="9827c-761">Valore</span><span class="sxs-lookup"><span data-stu-id="9827c-761">Value</span></span>

<span data-ttu-id="9827c-762">Nome</span><span class="sxs-lookup"><span data-stu-id="9827c-762">Name</span></span>

<span data-ttu-id="9827c-763">296</span><span class="sxs-lookup"><span data-stu-id="9827c-763">296</span></span>

[<span data-ttu-id="9827c-764">Windows Server Backup</span><span class="sxs-lookup"><span data-stu-id="9827c-764">Windows Server Backup</span></span>](/windows)

<span data-ttu-id="9827c-765">297</span><span class="sxs-lookup"><span data-stu-id="9827c-765">297</span></span>

[<span data-ttu-id="9827c-766">Strumenti da riga di comando</span><span class="sxs-lookup"><span data-stu-id="9827c-766">Command Line Tools</span></span>](/windows)

<span data-ttu-id="9827c-767">Funzionalità di Servizi di riconoscimento della grafia (310)</span><span class="sxs-lookup"><span data-stu-id="9827c-767">Ink and Handwriting Services - Features (310)</span></span>

<span data-ttu-id="9827c-768">Valore</span><span class="sxs-lookup"><span data-stu-id="9827c-768">Value</span></span>

<span data-ttu-id="9827c-769">Nome</span><span class="sxs-lookup"><span data-stu-id="9827c-769">Name</span></span>

<span data-ttu-id="9827c-770">311</span><span class="sxs-lookup"><span data-stu-id="9827c-770">311</span></span>

[<span data-ttu-id="9827c-771">Supporto per input penna</span><span class="sxs-lookup"><span data-stu-id="9827c-771">Ink Support</span></span>](/windows)<br/>

<span data-ttu-id="9827c-772">312</span><span class="sxs-lookup"><span data-stu-id="9827c-772">312</span></span>

[<span data-ttu-id="9827c-773">Riconoscimento della grafia</span><span class="sxs-lookup"><span data-stu-id="9827c-773">Handwriting Recognition</span></span>](/windows)<br/>

<span data-ttu-id="9827c-774">Servizio trasferimento intelligente in background (BITS)-features (335)</span><span class="sxs-lookup"><span data-stu-id="9827c-774">Background Intelligent Transfer Service (BITS) - Features (335)</span></span>

<span data-ttu-id="9827c-775">Valore</span><span class="sxs-lookup"><span data-stu-id="9827c-775">Value</span></span>

<span data-ttu-id="9827c-776">Nome</span><span class="sxs-lookup"><span data-stu-id="9827c-776">Name</span></span>

<span data-ttu-id="9827c-777">54</span><span class="sxs-lookup"><span data-stu-id="9827c-777">54</span></span>

<span data-ttu-id="9827c-778">Estensione del server IIS</span><span class="sxs-lookup"><span data-stu-id="9827c-778">IIS Server Extension</span></span>

<span data-ttu-id="9827c-779">332</span><span class="sxs-lookup"><span data-stu-id="9827c-779">332</span></span>

[<span data-ttu-id="9827c-780">Compact Server</span><span class="sxs-lookup"><span data-stu-id="9827c-780">Compact Server</span></span>](/windows)<br/>

<span data-ttu-id="9827c-781">Supporto di WOW64-funzionalità (340)</span><span class="sxs-lookup"><span data-stu-id="9827c-781">Wow64 Support - Features (340)</span></span>

<span data-ttu-id="9827c-782">Valore</span><span class="sxs-lookup"><span data-stu-id="9827c-782">Value</span></span>

<span data-ttu-id="9827c-783">Nome</span><span class="sxs-lookup"><span data-stu-id="9827c-783">Name</span></span>

<span data-ttu-id="9827c-784">341</span><span class="sxs-lookup"><span data-stu-id="9827c-784">341</span></span>

[<span data-ttu-id="9827c-785">WoW64</span><span class="sxs-lookup"><span data-stu-id="9827c-785">WoW64</span></span>](#wow64)<br/>

<span data-ttu-id="9827c-786">342</span><span class="sxs-lookup"><span data-stu-id="9827c-786">342</span></span>

[<span data-ttu-id="9827c-787">WoW64 per .NET Framework 2,0 e Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="9827c-787">WoW64 for .NET Framework 2.0 and Windows PowerShell</span></span>](/windows)<br/>

<span data-ttu-id="9827c-788">343</span><span class="sxs-lookup"><span data-stu-id="9827c-788">343</span></span>

[<span data-ttu-id="9827c-789">WoW64 per .NET Framework 2,0</span><span class="sxs-lookup"><span data-stu-id="9827c-789">WoW64 for .NET Framework 2.0</span></span>](/windows)<br/>

<span data-ttu-id="9827c-790">344</span><span class="sxs-lookup"><span data-stu-id="9827c-790">344</span></span>

[<span data-ttu-id="9827c-791">WoW64 per PowerShell</span><span class="sxs-lookup"><span data-stu-id="9827c-791">WoW64 for PowerShell</span></span>](/windows)<br/>

<span data-ttu-id="9827c-792">345</span><span class="sxs-lookup"><span data-stu-id="9827c-792">345</span></span>

[<span data-ttu-id="9827c-793">WoW64 per .NET Framework 3,0 e 3,5</span><span class="sxs-lookup"><span data-stu-id="9827c-793">WoW64 for .NET Framework 3.0 and 3.5</span></span>](/windows)<br/>

<span data-ttu-id="9827c-794">346</span><span class="sxs-lookup"><span data-stu-id="9827c-794">346</span></span>

[<span data-ttu-id="9827c-795">WoW64 per servizi di stampa</span><span class="sxs-lookup"><span data-stu-id="9827c-795">WoW64 for Print Services</span></span>](/windows)<br/>

<span data-ttu-id="9827c-796">347</span><span class="sxs-lookup"><span data-stu-id="9827c-796">347</span></span>

[<span data-ttu-id="9827c-797">WoW64 per il clustering di failover</span><span class="sxs-lookup"><span data-stu-id="9827c-797">WoW64 for Failover Clustering</span></span>](/windows)<br/>

<span data-ttu-id="9827c-798">348</span><span class="sxs-lookup"><span data-stu-id="9827c-798">348</span></span>

[<span data-ttu-id="9827c-799">WoW64 per input Method Editor</span><span class="sxs-lookup"><span data-stu-id="9827c-799">WoW64 for Input Method Editor</span></span>](/windows)<br/>

<span data-ttu-id="9827c-800">349</span><span class="sxs-lookup"><span data-stu-id="9827c-800">349</span></span>

[<span data-ttu-id="9827c-801">WoW64 per sottosistema per applicazioni basate su UNIX</span><span class="sxs-lookup"><span data-stu-id="9827c-801">WoW64 for Subsystem for UNIX-based Applications</span></span>](/windows)<br/>

<span data-ttu-id="9827c-802">Interfacce utente e servizi ruolo infrastruttura (447)</span><span class="sxs-lookup"><span data-stu-id="9827c-802">User Interfaces and Infrastructure - Role Services (447)</span></span>

<span data-ttu-id="9827c-803">Valore</span><span class="sxs-lookup"><span data-stu-id="9827c-803">Value</span></span>

<span data-ttu-id="9827c-804">Nome</span><span class="sxs-lookup"><span data-stu-id="9827c-804">Name</span></span>

<span data-ttu-id="9827c-805">35</span><span class="sxs-lookup"><span data-stu-id="9827c-805">35</span></span>

[<span data-ttu-id="9827c-806">Esperienza desktop</span><span class="sxs-lookup"><span data-stu-id="9827c-806">Desktop Experience</span></span>](/windows)

<span data-ttu-id="9827c-807">99</span><span class="sxs-lookup"><span data-stu-id="9827c-807">99</span></span>

[<span data-ttu-id="9827c-808">Shell grafica server</span><span class="sxs-lookup"><span data-stu-id="9827c-808">Server Graphical Shell</span></span>](/windows)

<span data-ttu-id="9827c-809">Windows Server Update Services-funzionalità (404)</span><span class="sxs-lookup"><span data-stu-id="9827c-809">Window Server Update Services - Features (404)</span></span>

<span data-ttu-id="9827c-810">Valore</span><span class="sxs-lookup"><span data-stu-id="9827c-810">Value</span></span>

<span data-ttu-id="9827c-811">Nome</span><span class="sxs-lookup"><span data-stu-id="9827c-811">Name</span></span>

<span data-ttu-id="9827c-812">405</span><span class="sxs-lookup"><span data-stu-id="9827c-812">405</span></span>

[<span data-ttu-id="9827c-813">API e cmdlet di PowerShell</span><span class="sxs-lookup"><span data-stu-id="9827c-813">API and PowerShell cmdlets</span></span>](/windows)

<span data-ttu-id="9827c-814">406</span><span class="sxs-lookup"><span data-stu-id="9827c-814">406</span></span>

[<span data-ttu-id="9827c-815">Connettività SQL Server</span><span class="sxs-lookup"><span data-stu-id="9827c-815">SQL Server Connectivity</span></span>](/windows)

<span data-ttu-id="9827c-816">407</span><span class="sxs-lookup"><span data-stu-id="9827c-816">407</span></span>

[<span data-ttu-id="9827c-817">Servizi WSUS</span><span class="sxs-lookup"><span data-stu-id="9827c-817">WSUS Services</span></span>](/windows)

<span data-ttu-id="9827c-818">408</span><span class="sxs-lookup"><span data-stu-id="9827c-818">408</span></span>

[<span data-ttu-id="9827c-819">Console di gestione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="9827c-819">User Interface Management Console</span></span>](/windows)

<span data-ttu-id="9827c-820">449</span><span class="sxs-lookup"><span data-stu-id="9827c-820">449</span></span>

[<span data-ttu-id="9827c-821">Connettività WID</span><span class="sxs-lookup"><span data-stu-id="9827c-821">WID Connectivity</span></span>](/windows)

<span data-ttu-id="9827c-822">Funzionalità di Windows PowerShell (417)</span><span class="sxs-lookup"><span data-stu-id="9827c-822">Windows PowerShell - Features (417)</span></span>

<span data-ttu-id="9827c-823">Valore</span><span class="sxs-lookup"><span data-stu-id="9827c-823">Value</span></span>

<span data-ttu-id="9827c-824">Nome</span><span class="sxs-lookup"><span data-stu-id="9827c-824">Name</span></span>

<span data-ttu-id="9827c-825">411</span><span class="sxs-lookup"><span data-stu-id="9827c-825">411</span></span>

[<span data-ttu-id="9827c-826">Motore di Windows PowerShell 2,0</span><span class="sxs-lookup"><span data-stu-id="9827c-826">Windows PowerShell 2.0 Engine</span></span>](/windows)

<span data-ttu-id="9827c-827">412</span><span class="sxs-lookup"><span data-stu-id="9827c-827">412</span></span>

[<span data-ttu-id="9827c-828">Windows PowerShell 3.0</span><span class="sxs-lookup"><span data-stu-id="9827c-828">Windows PowerShell 3.0</span></span>](/windows)

<span data-ttu-id="9827c-829">448</span><span class="sxs-lookup"><span data-stu-id="9827c-829">448</span></span>

[<span data-ttu-id="9827c-830">Accesso Web di Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="9827c-830">Windows PowerShell Web Access</span></span>](/windows)

<span data-ttu-id="9827c-831">1000</span><span class="sxs-lookup"><span data-stu-id="9827c-831">1000</span></span>

[<span data-ttu-id="9827c-832">Servizio di configurazione dello stato desiderato di Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="9827c-832">Windows PowerShell Desired State Configuration Service</span></span>](/windows)

<span data-ttu-id="9827c-833">.NET Framework 4,5-funzionalità (418)</span><span class="sxs-lookup"><span data-stu-id="9827c-833">.NET Framework 4.5 - Features (418)</span></span>

<span data-ttu-id="9827c-834">Valore</span><span class="sxs-lookup"><span data-stu-id="9827c-834">Value</span></span>

<span data-ttu-id="9827c-835">Nome</span><span class="sxs-lookup"><span data-stu-id="9827c-835">Name</span></span>

<span data-ttu-id="9827c-836">419</span><span class="sxs-lookup"><span data-stu-id="9827c-836">419</span></span>

[<span data-ttu-id="9827c-837">.NET Framework 4,5 esteso</span><span class="sxs-lookup"><span data-stu-id="9827c-837">.NET Framework 4.5 Extended</span></span>](/windows)

<span data-ttu-id="9827c-838">420</span><span class="sxs-lookup"><span data-stu-id="9827c-838">420</span></span>

[<span data-ttu-id="9827c-839">Servizi WCF</span><span class="sxs-lookup"><span data-stu-id="9827c-839">WCF Services</span></span>](/windows)

<span data-ttu-id="9827c-840">421</span><span class="sxs-lookup"><span data-stu-id="9827c-840">421</span></span>

[<span data-ttu-id="9827c-841">Attivazione HTTP</span><span class="sxs-lookup"><span data-stu-id="9827c-841">HTTP Activation</span></span>](/windows)

<span data-ttu-id="9827c-842">422</span><span class="sxs-lookup"><span data-stu-id="9827c-842">422</span></span>

[<span data-ttu-id="9827c-843">Attivazione di Accodamento messaggi (MSMQ)</span><span class="sxs-lookup"><span data-stu-id="9827c-843">Message Queuing (MSMQ) Activation</span></span>](/windows)

<span data-ttu-id="9827c-844">423</span><span class="sxs-lookup"><span data-stu-id="9827c-844">423</span></span>

[<span data-ttu-id="9827c-845">Attivazione named pipe</span><span class="sxs-lookup"><span data-stu-id="9827c-845">Named Pipe Activation</span></span>](/windows)

<span data-ttu-id="9827c-846">424</span><span class="sxs-lookup"><span data-stu-id="9827c-846">424</span></span>

[<span data-ttu-id="9827c-847">Attivazione TCP</span><span class="sxs-lookup"><span data-stu-id="9827c-847">TCP Activation</span></span>](/windows)

<span data-ttu-id="9827c-848">425</span><span class="sxs-lookup"><span data-stu-id="9827c-848">425</span></span>

[<span data-ttu-id="9827c-849">Condivisione delle porte TCP</span><span class="sxs-lookup"><span data-stu-id="9827c-849">TCP Port Sharing</span></span>](/windows)

<span data-ttu-id="9827c-850">429</span><span class="sxs-lookup"><span data-stu-id="9827c-850">429</span></span>

[<span data-ttu-id="9827c-851">ASP.NET 4.5</span><span class="sxs-lookup"><span data-stu-id="9827c-851">ASP.NET 4.5</span></span>](/windows)

<span data-ttu-id="9827c-852">Accesso remoto-ruolo (468)</span><span class="sxs-lookup"><span data-stu-id="9827c-852">Remote Access - Role (468)</span></span>

<span data-ttu-id="9827c-853">Valore</span><span class="sxs-lookup"><span data-stu-id="9827c-853">Value</span></span>

<span data-ttu-id="9827c-854">Nome</span><span class="sxs-lookup"><span data-stu-id="9827c-854">Name</span></span>

<span data-ttu-id="9827c-855">469</span><span class="sxs-lookup"><span data-stu-id="9827c-855">469</span></span>

[<span data-ttu-id="9827c-856">DirectAccess e VPN (RAS)</span><span class="sxs-lookup"><span data-stu-id="9827c-856">DirectAccess and VPN (RAS)</span></span>](/windows)

<span data-ttu-id="9827c-857">470</span><span class="sxs-lookup"><span data-stu-id="9827c-857">470</span></span>

[<span data-ttu-id="9827c-858">Routing</span><span class="sxs-lookup"><span data-stu-id="9827c-858">Routing</span></span>](#routing)

<span data-ttu-id="9827c-859">Servizi file e archiviazione-ruolo (481)</span><span class="sxs-lookup"><span data-stu-id="9827c-859">File and Storage Services - Role (481)</span></span>

<span data-ttu-id="9827c-860">Valore</span><span class="sxs-lookup"><span data-stu-id="9827c-860">Value</span></span>

<span data-ttu-id="9827c-861">Nome</span><span class="sxs-lookup"><span data-stu-id="9827c-861">Name</span></span>

<span data-ttu-id="9827c-862">482</span><span class="sxs-lookup"><span data-stu-id="9827c-862">482</span></span>

[<span data-ttu-id="9827c-863">Servizi di archiviazione</span><span class="sxs-lookup"><span data-stu-id="9827c-863">Storage Services</span></span>](/windows)

<span data-ttu-id="9827c-864">484</span><span class="sxs-lookup"><span data-stu-id="9827c-864">484</span></span>

[<span data-ttu-id="9827c-865">Strumenti di gestione del cluster di failover</span><span class="sxs-lookup"><span data-stu-id="9827c-865">Failover Cluster Management Tools</span></span>](/windows)



 

</dd> <dt>

<span data-ttu-id="9827c-866">**Nome**</span><span class="sxs-lookup"><span data-stu-id="9827c-866">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9827c-867">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9827c-867">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9827c-868">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="9827c-868">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="9827c-869">Nome visualizzato della funzionalità server, ad esempio "file server", "server di stampa" o "esperienza desktop".</span><span class="sxs-lookup"><span data-stu-id="9827c-869">Display name of the server feature, such as "File Server", "Print Server", or "Desktop Experience".</span></span>

</dd> <dt>

<span data-ttu-id="9827c-870">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="9827c-870">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9827c-871">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9827c-871">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9827c-872">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="9827c-872">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="9827c-873">Numero ID della funzionalità server padre.</span><span class="sxs-lookup"><span data-stu-id="9827c-873">ID number of the parent server feature.</span></span> <span data-ttu-id="9827c-874">Questa proprietà è 0 se la funzionalità rappresentata dall'istanza corrente della classe non dispone di una funzionalità padre.</span><span class="sxs-lookup"><span data-stu-id="9827c-874">This property is 0 if the feature represented by the current instance of the class does not have a parent feature.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9827c-875">Commenti</span><span class="sxs-lookup"><span data-stu-id="9827c-875">Remarks</span></span>

<span data-ttu-id="9827c-876">Per informazioni sulle funzionalità server, leggere la [Panoramica tecnica su Windows server 2008 Server Manager](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc753319(v=ws.10)) .</span><span class="sxs-lookup"><span data-stu-id="9827c-876">Read the [Windows Server 2008 Server Manager Technical Overview](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc753319(v=ws.10)) to learn about server features.</span></span>

<span data-ttu-id="9827c-877">Le aziende che non utilizzano software di gestione che segnala le funzionalità server, ad esempio System Center Operations Manager con i Management Pack installati, possono ottenere tali informazioni eseguendo una query sulla classe **Win32 \_ ServerFeature** .</span><span class="sxs-lookup"><span data-stu-id="9827c-877">Enterprises that do not use management software that reports server features, such as System Center Operations Manager with management packs installed, can get that information by querying the **Win32\_ServerFeature** class.</span></span>

<span data-ttu-id="9827c-878">È possibile utilizzare le funzionalità remote di WMI o WinRM per ottenere informazioni sulle funzionalità server da server remoti.</span><span class="sxs-lookup"><span data-stu-id="9827c-878">You can use the remoting features of WMI or WinRM to get server feature information from remote servers.</span></span> <span data-ttu-id="9827c-879">Per ulteriori informazioni sulle connessioni DCOM remote WMI, vedere [la pagina relativa alla connessione a WMI in un computer remoto](connecting-to-wmi-on-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="9827c-879">For more information about remote WMI DCOM connections, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span> <span data-ttu-id="9827c-880">Per altre informazioni su WinRM, vedere Windows Remote Management (Gestione remota Windows).</span><span class="sxs-lookup"><span data-stu-id="9827c-880">For more information about WinRM, see Windows Remote Management.</span></span>

<span data-ttu-id="9827c-881">Windows Server 2012: **Win32 \_ ServerFeature** è stato deprecato.</span><span class="sxs-lookup"><span data-stu-id="9827c-881">Windows Server 2012: **Win32\_ServerFeature** has been deprecated.</span></span> <span data-ttu-id="9827c-882">Per accedere alle informazioni sulle funzionalità di Windows Server a livello di codice, è possibile utilizzare i [cmdlet di Server Manager](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/ee662311(v=technet.10)).</span><span class="sxs-lookup"><span data-stu-id="9827c-882">To access windows server feature information programmatically, you can use the [Server Manager Cmdlets](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/ee662311(v=technet.10)).</span></span>

### <a name="windows-server-2012-r2"></a><span data-ttu-id="9827c-883">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="9827c-883">Windows Server 2012 R2</span></span>

<dl> <dt>

<span data-ttu-id="9827c-884"><span id="Application_Server"></span><span id="application_server"></span><span id="APPLICATION_SERVER"></span>Server applicazioni</span><span class="sxs-lookup"><span data-stu-id="9827c-884"><span id="Application_Server"></span><span id="application_server"></span><span id="APPLICATION_SERVER"></span>Application Server</span></span>
</dt> <dd>

<span data-ttu-id="9827c-885">Non più supportato</span><span class="sxs-lookup"><span data-stu-id="9827c-885">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9827c-886"><span id="Streaming_Media_Services"></span><span id="streaming_media_services"></span><span id="STREAMING_MEDIA_SERVICES"></span>Servizi flussi multimediali</span><span class="sxs-lookup"><span data-stu-id="9827c-886"><span id="Streaming_Media_Services"></span><span id="streaming_media_services"></span><span id="STREAMING_MEDIA_SERVICES"></span>Streaming Media Services</span></span>
</dt> <dd>

<span data-ttu-id="9827c-887">Non più supportato</span><span class="sxs-lookup"><span data-stu-id="9827c-887">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9827c-888"><span id="Active_Directory_Federation_Services"></span><span id="active_directory_federation_services"></span><span id="ACTIVE_DIRECTORY_FEDERATION_SERVICES"></span>Active Directory Federation Services</span><span class="sxs-lookup"><span data-stu-id="9827c-888"><span id="Active_Directory_Federation_Services"></span><span id="active_directory_federation_services"></span><span id="ACTIVE_DIRECTORY_FEDERATION_SERVICES"></span>Active Directory Federation Services</span></span>
</dt> <dd>

<span data-ttu-id="9827c-889">Non più supportato</span><span class="sxs-lookup"><span data-stu-id="9827c-889">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9827c-890"><span id="DHCP_Server"></span><span id="dhcp_server"></span><span id="DHCP_SERVER"></span>Server DHCP</span><span class="sxs-lookup"><span data-stu-id="9827c-890"><span id="DHCP_Server"></span><span id="dhcp_server"></span><span id="DHCP_SERVER"></span>DHCP Server</span></span>
</dt> <dd>

<span data-ttu-id="9827c-891">Non più supportato</span><span class="sxs-lookup"><span data-stu-id="9827c-891">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9827c-892"><span id="DNS_Server"></span><span id="dns_server"></span><span id="DNS_SERVER"></span>Server DNS</span><span class="sxs-lookup"><span data-stu-id="9827c-892"><span id="DNS_Server"></span><span id="dns_server"></span><span id="DNS_SERVER"></span>DNS Server</span></span>
</dt> <dd>

<span data-ttu-id="9827c-893">Non più supportato</span><span class="sxs-lookup"><span data-stu-id="9827c-893">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9827c-894"><span id="Remote_Desktop_Services"></span><span id="remote_desktop_services"></span><span id="REMOTE_DESKTOP_SERVICES"></span>Servizi Desktop remoto</span><span class="sxs-lookup"><span data-stu-id="9827c-894"><span id="Remote_Desktop_Services"></span><span id="remote_desktop_services"></span><span id="REMOTE_DESKTOP_SERVICES"></span>Remote Desktop Services</span></span>
</dt> <dd>

<span data-ttu-id="9827c-895">Non più supportato</span><span class="sxs-lookup"><span data-stu-id="9827c-895">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9827c-896"><span id="Windows_Server_Update_Services"></span><span id="windows_server_update_services"></span><span id="WINDOWS_SERVER_UPDATE_SERVICES"></span>Windows Server Update Services</span><span class="sxs-lookup"><span data-stu-id="9827c-896"><span id="Windows_Server_Update_Services"></span><span id="windows_server_update_services"></span><span id="WINDOWS_SERVER_UPDATE_SERVICES"></span>Windows Server Update Services</span></span>
</dt> <dd>

<span data-ttu-id="9827c-897">Non più supportato</span><span class="sxs-lookup"><span data-stu-id="9827c-897">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9827c-898"><span id="Failover_Clustering"></span><span id="failover_clustering"></span><span id="FAILOVER_CLUSTERING"></span>Clustering di failover</span><span class="sxs-lookup"><span data-stu-id="9827c-898"><span id="Failover_Clustering"></span><span id="failover_clustering"></span><span id="FAILOVER_CLUSTERING"></span>Failover Clustering</span></span>
</dt> <dd>

<span data-ttu-id="9827c-899">Non più supportato</span><span class="sxs-lookup"><span data-stu-id="9827c-899">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9827c-900"><span id="Network_Load_Balancing"></span><span id="network_load_balancing"></span><span id="NETWORK_LOAD_BALANCING"></span>Bilanciamento carico di rete</span><span class="sxs-lookup"><span data-stu-id="9827c-900"><span id="Network_Load_Balancing"></span><span id="network_load_balancing"></span><span id="NETWORK_LOAD_BALANCING"></span>Network Load Balancing</span></span>
</dt> <dd>

<span data-ttu-id="9827c-901">Non più supportato</span><span class="sxs-lookup"><span data-stu-id="9827c-901">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9827c-902"><span id=".NET_Framework_3.5.1_Features"></span><span id=".net_framework_3.5.1_features"></span><span id=".NET_FRAMEWORK_3.5.1_FEATURES"></span>Funzionalità di .NET Framework 3.5.1</span><span class="sxs-lookup"><span data-stu-id="9827c-902"><span id=".NET_Framework_3.5.1_Features"></span><span id=".net_framework_3.5.1_features"></span><span id=".NET_FRAMEWORK_3.5.1_FEATURES"></span>.NET Framework 3.5.1 Features</span></span>
</dt> <dd>

<span data-ttu-id="9827c-903">Non più supportato</span><span class="sxs-lookup"><span data-stu-id="9827c-903">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9827c-904"><span id="Windows_System_Resource_Manager"></span><span id="windows_system_resource_manager"></span><span id="WINDOWS_SYSTEM_RESOURCE_MANAGER"></span>Gestione risorse di sistema Windows</span><span class="sxs-lookup"><span data-stu-id="9827c-904"><span id="Windows_System_Resource_Manager"></span><span id="windows_system_resource_manager"></span><span id="WINDOWS_SYSTEM_RESOURCE_MANAGER"></span>Windows System Resource Manager</span></span>
</dt> <dd>

<span data-ttu-id="9827c-905">Non più supportato</span><span class="sxs-lookup"><span data-stu-id="9827c-905">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9827c-906"><span id="Windows_Server_Backup_Features"></span><span id="windows_server_backup_features"></span><span id="WINDOWS_SERVER_BACKUP_FEATURES"></span>Funzionalità di Windows Server Backup</span><span class="sxs-lookup"><span data-stu-id="9827c-906"><span id="Windows_Server_Backup_Features"></span><span id="windows_server_backup_features"></span><span id="WINDOWS_SERVER_BACKUP_FEATURES"></span>Windows Server Backup Features</span></span>
</dt> <dd>

<span data-ttu-id="9827c-907">Non più supportato</span><span class="sxs-lookup"><span data-stu-id="9827c-907">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9827c-908"><span id="Remote_Assistance"></span><span id="remote_assistance"></span><span id="REMOTE_ASSISTANCE"></span>Assistenza remota</span><span class="sxs-lookup"><span data-stu-id="9827c-908"><span id="Remote_Assistance"></span><span id="remote_assistance"></span><span id="REMOTE_ASSISTANCE"></span>Remote Assistance</span></span>
</dt> <dd>

<span data-ttu-id="9827c-909">Non più supportato</span><span class="sxs-lookup"><span data-stu-id="9827c-909">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9827c-910"><span id="Telnet_Client"></span><span id="telnet_client"></span><span id="TELNET_CLIENT"></span>Client Telnet</span><span class="sxs-lookup"><span data-stu-id="9827c-910"><span id="Telnet_Client"></span><span id="telnet_client"></span><span id="TELNET_CLIENT"></span>Telnet Client</span></span>
</dt> <dd>

<span data-ttu-id="9827c-911">Non più supportato</span><span class="sxs-lookup"><span data-stu-id="9827c-911">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9827c-912"><span id="Telnet_Server"></span><span id="telnet_server"></span><span id="TELNET_SERVER"></span>Server Telnet</span><span class="sxs-lookup"><span data-stu-id="9827c-912"><span id="Telnet_Server"></span><span id="telnet_server"></span><span id="TELNET_SERVER"></span>Telnet Server</span></span>
</dt> <dd>

<span data-ttu-id="9827c-913">Non più supportato</span><span class="sxs-lookup"><span data-stu-id="9827c-913">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9827c-914"><span id="Subsystem_For_Unix-based_Applications"></span><span id="subsystem_for_unix-based_applications"></span><span id="SUBSYSTEM_FOR_UNIX-BASED_APPLICATIONS"></span>Sottosistema per applicazioni basate su UNIX</span><span class="sxs-lookup"><span data-stu-id="9827c-914"><span id="Subsystem_For_Unix-based_Applications"></span><span id="subsystem_for_unix-based_applications"></span><span id="SUBSYSTEM_FOR_UNIX-BASED_APPLICATIONS"></span>Subsystem For Unix-based Applications</span></span>
</dt> <dd>

<span data-ttu-id="9827c-915">Non più supportato</span><span class="sxs-lookup"><span data-stu-id="9827c-915">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9827c-916"><span id="Windows_Internal_Database"></span><span id="windows_internal_database"></span><span id="WINDOWS_INTERNAL_DATABASE"></span>Database interno di Windows</span><span class="sxs-lookup"><span data-stu-id="9827c-916"><span id="Windows_Internal_Database"></span><span id="windows_internal_database"></span><span id="WINDOWS_INTERNAL_DATABASE"></span>Windows Internal Database</span></span>
</dt> <dd>

<span data-ttu-id="9827c-917">Non più supportato</span><span class="sxs-lookup"><span data-stu-id="9827c-917">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9827c-918"><span id="Storage_Manager_For_SANs"></span><span id="storage_manager_for_sans"></span><span id="STORAGE_MANAGER_FOR_SANS"></span>Gestione archivi San</span><span class="sxs-lookup"><span data-stu-id="9827c-918"><span id="Storage_Manager_For_SANs"></span><span id="storage_manager_for_sans"></span><span id="STORAGE_MANAGER_FOR_SANS"></span>Storage Manager For SANs</span></span>
</dt> <dd>

<span data-ttu-id="9827c-919">Non più supportato</span><span class="sxs-lookup"><span data-stu-id="9827c-919">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9827c-920"><span id="Internet_Storage_Name_Server"></span><span id="internet_storage_name_server"></span><span id="INTERNET_STORAGE_NAME_SERVER"></span>Internet Storage Name Server</span><span class="sxs-lookup"><span data-stu-id="9827c-920"><span id="Internet_Storage_Name_Server"></span><span id="internet_storage_name_server"></span><span id="INTERNET_STORAGE_NAME_SERVER"></span>Internet Storage Name Server</span></span>
</dt> <dd>

<span data-ttu-id="9827c-921">Non più supportato</span><span class="sxs-lookup"><span data-stu-id="9827c-921">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9827c-922"><span id="Multipath_I_O"></span><span id="multipath_i_o"></span><span id="MULTIPATH_I_O"></span>Multipath I/O</span><span class="sxs-lookup"><span data-stu-id="9827c-922"><span id="Multipath_I_O"></span><span id="multipath_i_o"></span><span id="MULTIPATH_I_O"></span>Multipath I/O</span></span>
</dt> <dd>

<span data-ttu-id="9827c-923">Non più supportato</span><span class="sxs-lookup"><span data-stu-id="9827c-923">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9827c-924"><span id="SNMP_Services"></span><span id="snmp_services"></span><span id="SNMP_SERVICES"></span>Servizi SNMP</span><span class="sxs-lookup"><span data-stu-id="9827c-924"><span id="SNMP_Services"></span><span id="snmp_services"></span><span id="SNMP_SERVICES"></span>SNMP Services</span></span>
</dt> <dd>

<span data-ttu-id="9827c-925">Non più supportato</span><span class="sxs-lookup"><span data-stu-id="9827c-925">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9827c-926"><span id="Services_For_Network_File_System"></span><span id="services_for_network_file_system"></span><span id="SERVICES_FOR_NETWORK_FILE_SYSTEM"></span>Servizi per il file System di rete</span><span class="sxs-lookup"><span data-stu-id="9827c-926"><span id="Services_For_Network_File_System"></span><span id="services_for_network_file_system"></span><span id="SERVICES_FOR_NETWORK_FILE_SYSTEM"></span>Services For Network File System</span></span>
</dt> <dd>

<span data-ttu-id="9827c-927">Non più supportato</span><span class="sxs-lookup"><span data-stu-id="9827c-927">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9827c-928"><span id="Peer_Name_Resolution_Protocol"></span><span id="peer_name_resolution_protocol"></span><span id="PEER_NAME_RESOLUTION_PROTOCOL"></span>Protocollo di risoluzione del nome peer</span><span class="sxs-lookup"><span data-stu-id="9827c-928"><span id="Peer_Name_Resolution_Protocol"></span><span id="peer_name_resolution_protocol"></span><span id="PEER_NAME_RESOLUTION_PROTOCOL"></span>Peer Name Resolution Protocol</span></span>
</dt> <dd>

<span data-ttu-id="9827c-929">Non più supportato</span><span class="sxs-lookup"><span data-stu-id="9827c-929">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9827c-930"><span id="Remote_Server_Administration_Tools"></span><span id="remote_server_administration_tools"></span><span id="REMOTE_SERVER_ADMINISTRATION_TOOLS"></span>Strumenti di amministrazione remota del server</span><span class="sxs-lookup"><span data-stu-id="9827c-930"><span id="Remote_Server_Administration_Tools"></span><span id="remote_server_administration_tools"></span><span id="REMOTE_SERVER_ADMINISTRATION_TOOLS"></span>Remote Server Administration Tools</span></span>
</dt> <dd>

<span data-ttu-id="9827c-931">Non più supportato</span><span class="sxs-lookup"><span data-stu-id="9827c-931">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9827c-932"><span id="Quality_Windows_Audio_Video_Experience"></span><span id="quality_windows_audio_video_experience"></span><span id="QUALITY_WINDOWS_AUDIO_VIDEO_EXPERIENCE"></span>Esperienza audio video Windows di qualità</span><span class="sxs-lookup"><span data-stu-id="9827c-932"><span id="Quality_Windows_Audio_Video_Experience"></span><span id="quality_windows_audio_video_experience"></span><span id="QUALITY_WINDOWS_AUDIO_VIDEO_EXPERIENCE"></span>Quality Windows Audio Video Experience</span></span>
</dt> <dd>

<span data-ttu-id="9827c-933">Non più supportato</span><span class="sxs-lookup"><span data-stu-id="9827c-933">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9827c-934"><span id="Group_Policy_Management"></span><span id="group_policy_management"></span><span id="GROUP_POLICY_MANAGEMENT"></span>Gestione Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="9827c-934"><span id="Group_Policy_Management"></span><span id="group_policy_management"></span><span id="GROUP_POLICY_MANAGEMENT"></span>Group Policy Management</span></span>
</dt> <dd>

<span data-ttu-id="9827c-935">Non più supportato</span><span class="sxs-lookup"><span data-stu-id="9827c-935">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9827c-936"><span id="Indexing_Service"></span><span id="indexing_service"></span><span id="INDEXING_SERVICE"></span>Servizio di indicizzazione</span><span class="sxs-lookup"><span data-stu-id="9827c-936"><span id="Indexing_Service"></span><span id="indexing_service"></span><span id="INDEXING_SERVICE"></span>Indexing Service</span></span>
</dt> <dd>

<span data-ttu-id="9827c-937">Non più supportato</span><span class="sxs-lookup"><span data-stu-id="9827c-937">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9827c-938"><span id="File_Server_Resource_Manager__FSRM_"></span><span id="file_server_resource_manager__fsrm_"></span><span id="FILE_SERVER_RESOURCE_MANAGER__FSRM_"></span>Gestione risorse file server (FSRM)</span><span class="sxs-lookup"><span data-stu-id="9827c-938"><span id="File_Server_Resource_Manager__FSRM_"></span><span id="file_server_resource_manager__fsrm_"></span><span id="FILE_SERVER_RESOURCE_MANAGER__FSRM_"></span>File Server Resource Manager (FSRM)</span></span>
</dt> <dd>

<span data-ttu-id="9827c-939">Non più supportato</span><span class="sxs-lookup"><span data-stu-id="9827c-939">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9827c-940"><span id="Windows_Server_Migration_Tools"></span><span id="windows_server_migration_tools"></span><span id="WINDOWS_SERVER_MIGRATION_TOOLS"></span>Strumenti di migrazione per Windows Server</span><span class="sxs-lookup"><span data-stu-id="9827c-940"><span id="Windows_Server_Migration_Tools"></span><span id="windows_server_migration_tools"></span><span id="WINDOWS_SERVER_MIGRATION_TOOLS"></span>Windows Server Migration Tools</span></span>
</dt> <dd>

<span data-ttu-id="9827c-941">Non più supportato</span><span class="sxs-lookup"><span data-stu-id="9827c-941">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9827c-942"><span id="BranchCache"></span><span id="branchcache"></span><span id="BRANCHCACHE"></span>BranchCache</span><span class="sxs-lookup"><span data-stu-id="9827c-942"><span id="BranchCache"></span><span id="branchcache"></span><span id="BRANCHCACHE"></span>BranchCache</span></span>
</dt> <dd>

<span data-ttu-id="9827c-943">Non più supportato</span><span class="sxs-lookup"><span data-stu-id="9827c-943">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9827c-944"><span id="DirectAccess_Management_Console"></span><span id="directaccess_management_console"></span><span id="DIRECTACCESS_MANAGEMENT_CONSOLE"></span>Console di Gestione DirectAccess</span><span class="sxs-lookup"><span data-stu-id="9827c-944"><span id="DirectAccess_Management_Console"></span><span id="directaccess_management_console"></span><span id="DIRECTACCESS_MANAGEMENT_CONSOLE"></span>DirectAccess Management Console</span></span>
</dt> <dd>

<span data-ttu-id="9827c-945">Non più supportato</span><span class="sxs-lookup"><span data-stu-id="9827c-945">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9827c-946"><span id="Background_Intelligent_Transfer_Service__BITS_"></span><span id="background_intelligent_transfer_service__bits_"></span><span id="BACKGROUND_INTELLIGENT_TRANSFER_SERVICE__BITS_"></span>Servizio trasferimento intelligente in background (BITS)</span><span class="sxs-lookup"><span data-stu-id="9827c-946"><span id="Background_Intelligent_Transfer_Service__BITS_"></span><span id="background_intelligent_transfer_service__bits_"></span><span id="BACKGROUND_INTELLIGENT_TRANSFER_SERVICE__BITS_"></span>Background Intelligent Transfer Service (BITS)</span></span>
</dt> <dd>

<span data-ttu-id="9827c-947">Non più supportato</span><span class="sxs-lookup"><span data-stu-id="9827c-947">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9827c-948"><span id="WoW64_Support"></span><span id="wow64_support"></span><span id="WOW64_SUPPORT"></span>Supporto di WoW64</span><span class="sxs-lookup"><span data-stu-id="9827c-948"><span id="WoW64_Support"></span><span id="wow64_support"></span><span id="WOW64_SUPPORT"></span>WoW64 Support</span></span>
</dt> <dd>

<span data-ttu-id="9827c-949">Non più supportato</span><span class="sxs-lookup"><span data-stu-id="9827c-949">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9827c-950"><span id="Window_Server_Update_Services"></span><span id="window_server_update_services"></span><span id="WINDOW_SERVER_UPDATE_SERVICES"></span>Windows Server Update Services</span><span class="sxs-lookup"><span data-stu-id="9827c-950"><span id="Window_Server_Update_Services"></span><span id="window_server_update_services"></span><span id="WINDOW_SERVER_UPDATE_SERVICES"></span>Window Server Update Services</span></span>
</dt> <dd>

<span data-ttu-id="9827c-951">Aggiunta</span><span class="sxs-lookup"><span data-stu-id="9827c-951">Added</span></span>

</dd> <dt>

<span data-ttu-id="9827c-952"><span id="IP_Address_Management__IPAM__Server"></span><span id="ip_address_management__ipam__server"></span><span id="IP_ADDRESS_MANAGEMENT__IPAM__SERVER"></span>Server gestione indirizzi IP</span><span class="sxs-lookup"><span data-stu-id="9827c-952"><span id="IP_Address_Management__IPAM__Server"></span><span id="ip_address_management__ipam__server"></span><span id="IP_ADDRESS_MANAGEMENT__IPAM__SERVER"></span>IP Address Management (IPAM) Server</span></span>
</dt> <dd>

<span data-ttu-id="9827c-953">Aggiunta</span><span class="sxs-lookup"><span data-stu-id="9827c-953">Added</span></span>

</dd> <dt>

<span data-ttu-id="9827c-954"><span id="Windows_PowerShell"></span><span id="windows_powershell"></span><span id="WINDOWS_POWERSHELL"></span>Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="9827c-954"><span id="Windows_PowerShell"></span><span id="windows_powershell"></span><span id="WINDOWS_POWERSHELL"></span>Windows PowerShell</span></span>
</dt> <dd>

<span data-ttu-id="9827c-955">Aggiunta</span><span class="sxs-lookup"><span data-stu-id="9827c-955">Added</span></span>

</dd> <dt>

<span data-ttu-id="9827c-956"><span id=".NET_Framework_4.5"></span><span id=".net_framework_4.5"></span><span id=".NET_FRAMEWORK_4.5"></span>.NET Framework 4,5</span><span class="sxs-lookup"><span data-stu-id="9827c-956"><span id=".NET_Framework_4.5"></span><span id=".net_framework_4.5"></span><span id=".NET_FRAMEWORK_4.5"></span>.NET Framework 4.5</span></span>
</dt> <dd>

<span data-ttu-id="9827c-957">Aggiunta</span><span class="sxs-lookup"><span data-stu-id="9827c-957">Added</span></span>

</dd> <dt>

<span data-ttu-id="9827c-958"><span id="Windows_Search_Service"></span><span id="windows_search_service"></span><span id="WINDOWS_SEARCH_SERVICE"></span>servizio di ricerca di Windows</span><span class="sxs-lookup"><span data-stu-id="9827c-958"><span id="Windows_Search_Service"></span><span id="windows_search_service"></span><span id="WINDOWS_SEARCH_SERVICE"></span>Windows Search Service</span></span>
</dt> <dd>

<span data-ttu-id="9827c-959">Aggiunta</span><span class="sxs-lookup"><span data-stu-id="9827c-959">Added</span></span>

</dd> <dt>

<span data-ttu-id="9827c-960"><span id="Client_for_NFS"></span><span id="client_for_nfs"></span><span id="CLIENT_FOR_NFS"></span>Client per NFS</span><span class="sxs-lookup"><span data-stu-id="9827c-960"><span id="Client_for_NFS"></span><span id="client_for_nfs"></span><span id="CLIENT_FOR_NFS"></span>Client for NFS</span></span>
</dt> <dd>

<span data-ttu-id="9827c-961">Aggiunta</span><span class="sxs-lookup"><span data-stu-id="9827c-961">Added</span></span>

</dd> <dt>

<span data-ttu-id="9827c-962"><span id="BitLocker_Network_Unlock"></span><span id="bitlocker_network_unlock"></span><span id="BITLOCKER_NETWORK_UNLOCK"></span>Sblocco di rete BitLocker</span><span class="sxs-lookup"><span data-stu-id="9827c-962"><span id="BitLocker_Network_Unlock"></span><span id="bitlocker_network_unlock"></span><span id="BITLOCKER_NETWORK_UNLOCK"></span>BitLocker Network Unlock</span></span>
</dt> <dd>

<span data-ttu-id="9827c-963">Aggiunta</span><span class="sxs-lookup"><span data-stu-id="9827c-963">Added</span></span>

</dd> <dt>

<span data-ttu-id="9827c-964"><span id="Management_OData_IIS_Extension"></span><span id="management_odata_iis_extension"></span><span id="MANAGEMENT_ODATA_IIS_EXTENSION"></span>Estensione IIS OData gestione</span><span class="sxs-lookup"><span data-stu-id="9827c-964"><span id="Management_OData_IIS_Extension"></span><span id="management_odata_iis_extension"></span><span id="MANAGEMENT_ODATA_IIS_EXTENSION"></span>Management OData IIS Extension</span></span>
</dt> <dd>

<span data-ttu-id="9827c-965">Aggiunta</span><span class="sxs-lookup"><span data-stu-id="9827c-965">Added</span></span>

</dd> <dt>

<span data-ttu-id="9827c-966"><span id=".NET_Framework_4.5_Advanced_Services"></span><span id=".net_framework_4.5_advanced_services"></span><span id=".NET_FRAMEWORK_4.5_ADVANCED_SERVICES"></span>.NET Framework 4,5 servizi avanzati</span><span class="sxs-lookup"><span data-stu-id="9827c-966"><span id=".NET_Framework_4.5_Advanced_Services"></span><span id=".net_framework_4.5_advanced_services"></span><span id=".NET_FRAMEWORK_4.5_ADVANCED_SERVICES"></span>.NET Framework 4.5 Advanced Services</span></span>
</dt> <dd>

<span data-ttu-id="9827c-967">Aggiunta</span><span class="sxs-lookup"><span data-stu-id="9827c-967">Added</span></span>

</dd> <dt>

<span data-ttu-id="9827c-968"><span id=".NET_Framework_4.5_Features"></span><span id=".net_framework_4.5_features"></span><span id=".NET_FRAMEWORK_4.5_FEATURES"></span>Funzionalità di .NET Framework 4,5</span><span class="sxs-lookup"><span data-stu-id="9827c-968"><span id=".NET_Framework_4.5_Features"></span><span id=".net_framework_4.5_features"></span><span id=".NET_FRAMEWORK_4.5_FEATURES"></span>.NET Framework 4.5 Features</span></span>
</dt> <dd>

<span data-ttu-id="9827c-969">Aggiunta</span><span class="sxs-lookup"><span data-stu-id="9827c-969">Added</span></span>

</dd> <dt>

<span data-ttu-id="9827c-970"><span id="User_Interfaces_and_Infrastructure"></span><span id="user_interfaces_and_infrastructure"></span><span id="USER_INTERFACES_AND_INFRASTRUCTURE"></span>Interfacce utente e infrastruttura</span><span class="sxs-lookup"><span data-stu-id="9827c-970"><span id="User_Interfaces_and_Infrastructure"></span><span id="user_interfaces_and_infrastructure"></span><span id="USER_INTERFACES_AND_INFRASTRUCTURE"></span>User Interfaces and Infrastructure</span></span>
</dt> <dd>

<span data-ttu-id="9827c-971">Aggiunta</span><span class="sxs-lookup"><span data-stu-id="9827c-971">Added</span></span>

</dd> <dt>

<span data-ttu-id="9827c-972"><span id="Graphical_Management_Tools_and_Infrastructure"></span><span id="graphical_management_tools_and_infrastructure"></span><span id="GRAPHICAL_MANAGEMENT_TOOLS_AND_INFRASTRUCTURE"></span>Strumenti di gestione e infrastruttura grafica</span><span class="sxs-lookup"><span data-stu-id="9827c-972"><span id="Graphical_Management_Tools_and_Infrastructure"></span><span id="graphical_management_tools_and_infrastructure"></span><span id="GRAPHICAL_MANAGEMENT_TOOLS_AND_INFRASTRUCTURE"></span>Graphical Management Tools and Infrastructure</span></span>
</dt> <dd>

<span data-ttu-id="9827c-973">Aggiunta</span><span class="sxs-lookup"><span data-stu-id="9827c-973">Added</span></span>

</dd> <dt>

<span data-ttu-id="9827c-974"><span id="File_and_Storage_Services"></span><span id="file_and_storage_services"></span><span id="FILE_AND_STORAGE_SERVICES"></span>Servizi file e archiviazione</span><span class="sxs-lookup"><span data-stu-id="9827c-974"><span id="File_and_Storage_Services"></span><span id="file_and_storage_services"></span><span id="FILE_AND_STORAGE_SERVICES"></span>File and Storage Services</span></span>
</dt> <dd>

<span data-ttu-id="9827c-975">Aggiunta</span><span class="sxs-lookup"><span data-stu-id="9827c-975">Added</span></span>

</dd> <dt>

<span data-ttu-id="9827c-976"><span id="Windows_Server_Essentials_Experience"></span><span id="windows_server_essentials_experience"></span><span id="WINDOWS_SERVER_ESSENTIALS_EXPERIENCE"></span>Esperienza Windows Server Essentials</span><span class="sxs-lookup"><span data-stu-id="9827c-976"><span id="Windows_Server_Essentials_Experience"></span><span id="windows_server_essentials_experience"></span><span id="WINDOWS_SERVER_ESSENTIALS_EXPERIENCE"></span>Windows Server Essentials Experience</span></span>
</dt> <dd>

<span data-ttu-id="9827c-977">Aggiunta</span><span class="sxs-lookup"><span data-stu-id="9827c-977">Added</span></span>

</dd> <dt>

<span data-ttu-id="9827c-978"><span id="Direct_Play"></span><span id="direct_play"></span><span id="DIRECT_PLAY"></span>Riproduzione diretta</span><span class="sxs-lookup"><span data-stu-id="9827c-978"><span id="Direct_Play"></span><span id="direct_play"></span><span id="DIRECT_PLAY"></span>Direct Play</span></span>
</dt> <dd>

<span data-ttu-id="9827c-979">Aggiunta</span><span class="sxs-lookup"><span data-stu-id="9827c-979">Added</span></span>

</dd> <dt>

<span data-ttu-id="9827c-980"><span id="Distributed_File_System"></span><span id="distributed_file_system"></span><span id="DISTRIBUTED_FILE_SYSTEM"></span>file system distribuito</span><span class="sxs-lookup"><span data-stu-id="9827c-980"><span id="Distributed_File_System"></span><span id="distributed_file_system"></span><span id="DISTRIBUTED_FILE_SYSTEM"></span>Distributed File System</span></span>
</dt> <dd>

<span data-ttu-id="9827c-981">Non più supportato</span><span class="sxs-lookup"><span data-stu-id="9827c-981">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9827c-982"><span id="File_Server_Resource_Manager"></span><span id="file_server_resource_manager"></span><span id="FILE_SERVER_RESOURCE_MANAGER"></span>Gestione risorse file server</span><span class="sxs-lookup"><span data-stu-id="9827c-982"><span id="File_Server_Resource_Manager"></span><span id="file_server_resource_manager"></span><span id="FILE_SERVER_RESOURCE_MANAGER"></span>File Server Resource Manager</span></span>
</dt> <dd>

<span data-ttu-id="9827c-983">Non più supportato</span><span class="sxs-lookup"><span data-stu-id="9827c-983">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9827c-984"><span id="Services_For_Network_File_System"></span><span id="services_for_network_file_system"></span><span id="SERVICES_FOR_NETWORK_FILE_SYSTEM"></span>Servizi per il file System di rete</span><span class="sxs-lookup"><span data-stu-id="9827c-984"><span id="Services_For_Network_File_System"></span><span id="services_for_network_file_system"></span><span id="SERVICES_FOR_NETWORK_FILE_SYSTEM"></span>Services For Network File System</span></span>
</dt> <dd>

<span data-ttu-id="9827c-985">Non più supportato</span><span class="sxs-lookup"><span data-stu-id="9827c-985">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9827c-986"><span id="Single_Instance_Storage"></span><span id="single_instance_storage"></span><span id="SINGLE_INSTANCE_STORAGE"></span>Archiviazione a istanza singola</span><span class="sxs-lookup"><span data-stu-id="9827c-986"><span id="Single_Instance_Storage"></span><span id="single_instance_storage"></span><span id="SINGLE_INSTANCE_STORAGE"></span>Single Instance Storage</span></span>
</dt> <dd>

<span data-ttu-id="9827c-987">Non più supportato</span><span class="sxs-lookup"><span data-stu-id="9827c-987">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9827c-988"><span id="Windows_Search_Service"></span><span id="windows_search_service"></span><span id="WINDOWS_SEARCH_SERVICE"></span>servizio di ricerca di Windows</span><span class="sxs-lookup"><span data-stu-id="9827c-988"><span id="Windows_Search_Service"></span><span id="windows_search_service"></span><span id="WINDOWS_SEARCH_SERVICE"></span>Windows Search Service</span></span>
</dt> <dd>

<span data-ttu-id="9827c-989">Non più supportato</span><span class="sxs-lookup"><span data-stu-id="9827c-989">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9827c-990"><span id="Indexing_Service"></span><span id="indexing_service"></span><span id="INDEXING_SERVICE"></span>Servizio di indicizzazione</span><span class="sxs-lookup"><span data-stu-id="9827c-990"><span id="Indexing_Service"></span><span id="indexing_service"></span><span id="INDEXING_SERVICE"></span>Indexing Service</span></span>
</dt> <dd>

<span data-ttu-id="9827c-991">Non più supportato</span><span class="sxs-lookup"><span data-stu-id="9827c-991">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9827c-992"><span id="iSCSI_Target_Storage_Provider__VDS_and_VSS_hardware_providers_"></span><span id="iscsi_target_storage_provider__vds_and_vss_hardware_providers_"></span><span id="ISCSI_TARGET_STORAGE_PROVIDER__VDS_AND_VSS_HARDWARE_PROVIDERS_"></span>Provider di archiviazione di destinazione iSCSI (provider hardware VDS e VSS)</span><span class="sxs-lookup"><span data-stu-id="9827c-992"><span id="iSCSI_Target_Storage_Provider__VDS_and_VSS_hardware_providers_"></span><span id="iscsi_target_storage_provider__vds_and_vss_hardware_providers_"></span><span id="ISCSI_TARGET_STORAGE_PROVIDER__VDS_AND_VSS_HARDWARE_PROVIDERS_"></span>iSCSI Target Storage Provider (VDS and VSS hardware providers)</span></span>
</dt> <dd>

<span data-ttu-id="9827c-993">Aggiunta</span><span class="sxs-lookup"><span data-stu-id="9827c-993">Added</span></span>

</dd> <dt>

<span data-ttu-id="9827c-994"><span id="Work_Folders"></span><span id="work_folders"></span><span id="WORK_FOLDERS"></span>Cartelle di lavoro</span><span class="sxs-lookup"><span data-stu-id="9827c-994"><span id="Work_Folders"></span><span id="work_folders"></span><span id="WORK_FOLDERS"></span>Work Folders</span></span>
</dt> <dd>

<span data-ttu-id="9827c-995">Aggiunta</span><span class="sxs-lookup"><span data-stu-id="9827c-995">Added</span></span>

</dd> <dt>

<span data-ttu-id="9827c-996"><span id="Active_Directory_Domain_Controller"></span><span id="active_directory_domain_controller"></span><span id="ACTIVE_DIRECTORY_DOMAIN_CONTROLLER"></span>Controller Dominio di Active Directory</span><span class="sxs-lookup"><span data-stu-id="9827c-996"><span id="Active_Directory_Domain_Controller"></span><span id="active_directory_domain_controller"></span><span id="ACTIVE_DIRECTORY_DOMAIN_CONTROLLER"></span>Active Directory Domain Controller</span></span>
</dt> <dd>

<span data-ttu-id="9827c-997">Non più supportato</span><span class="sxs-lookup"><span data-stu-id="9827c-997">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9827c-998"><span id="Identity_Management_For_Unix"></span><span id="identity_management_for_unix"></span><span id="IDENTITY_MANAGEMENT_FOR_UNIX"></span>Gestione delle identità per UNIX</span><span class="sxs-lookup"><span data-stu-id="9827c-998"><span id="Identity_Management_For_Unix"></span><span id="identity_management_for_unix"></span><span id="IDENTITY_MANAGEMENT_FOR_UNIX"></span>Identity Management For Unix</span></span>
</dt> <dd>

<span data-ttu-id="9827c-999">Non più supportato</span><span class="sxs-lookup"><span data-stu-id="9827c-999">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1000"><span id="Server_For_Network_Information_Services"></span><span id="server_for_network_information_services"></span><span id="SERVER_FOR_NETWORK_INFORMATION_SERVICES"></span>Server per Network Information Services</span><span class="sxs-lookup"><span data-stu-id="9827c-1000"><span id="Server_For_Network_Information_Services"></span><span id="server_for_network_information_services"></span><span id="SERVER_FOR_NETWORK_INFORMATION_SERVICES"></span>Server For Network Information Services</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1001">Non più supportato</span><span class="sxs-lookup"><span data-stu-id="9827c-1001">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1002"><span id="Password_Synchronization"></span><span id="password_synchronization"></span><span id="PASSWORD_SYNCHRONIZATION"></span>Sincronizzazione password</span><span class="sxs-lookup"><span data-stu-id="9827c-1002"><span id="Password_Synchronization"></span><span id="password_synchronization"></span><span id="PASSWORD_SYNCHRONIZATION"></span>Password Synchronization</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1003">Non più supportato</span><span class="sxs-lookup"><span data-stu-id="9827c-1003">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1004"><span id="Administration_Tools"></span><span id="administration_tools"></span><span id="ADMINISTRATION_TOOLS"></span>Strumenti di amministrazione</span><span class="sxs-lookup"><span data-stu-id="9827c-1004"><span id="Administration_Tools"></span><span id="administration_tools"></span><span id="ADMINISTRATION_TOOLS"></span>Administration Tools</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1005">Non più supportato</span><span class="sxs-lookup"><span data-stu-id="9827c-1005">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1006"><span id="Windows_Media_Server"></span><span id="windows_media_server"></span><span id="WINDOWS_MEDIA_SERVER"></span>Windows Media Server</span><span class="sxs-lookup"><span data-stu-id="9827c-1006"><span id="Windows_Media_Server"></span><span id="windows_media_server"></span><span id="WINDOWS_MEDIA_SERVER"></span>Windows Media Server</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1007">Non più supportata.</span><span class="sxs-lookup"><span data-stu-id="9827c-1007">No longer supported.</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1008"><span id="Web-based_Administration"></span><span id="web-based_administration"></span><span id="WEB-BASED_ADMINISTRATION"></span>Amministrazione basata sul Web</span><span class="sxs-lookup"><span data-stu-id="9827c-1008"><span id="Web-based_Administration"></span><span id="web-based_administration"></span><span id="WEB-BASED_ADMINISTRATION"></span>Web-based Administration</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1009">Non più supportato</span><span class="sxs-lookup"><span data-stu-id="9827c-1009">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1010"><span id="Logging_Agent"></span><span id="logging_agent"></span><span id="LOGGING_AGENT"></span>Agente di registrazione</span><span class="sxs-lookup"><span data-stu-id="9827c-1010"><span id="Logging_Agent"></span><span id="logging_agent"></span><span id="LOGGING_AGENT"></span>Logging Agent</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1011">Non più supportato</span><span class="sxs-lookup"><span data-stu-id="9827c-1011">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1012"><span id="Federation_Service"></span><span id="federation_service"></span><span id="FEDERATION_SERVICE"></span>Servizio federativo</span><span class="sxs-lookup"><span data-stu-id="9827c-1012"><span id="Federation_Service"></span><span id="federation_service"></span><span id="FEDERATION_SERVICE"></span>Federation Service</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1013">Non più supportato</span><span class="sxs-lookup"><span data-stu-id="9827c-1013">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1014"><span id="Federation_Service_Policy"></span><span id="federation_service_policy"></span><span id="FEDERATION_SERVICE_POLICY"></span>Criteri di Servizio federativo</span><span class="sxs-lookup"><span data-stu-id="9827c-1014"><span id="Federation_Service_Policy"></span><span id="federation_service_policy"></span><span id="FEDERATION_SERVICE_POLICY"></span>Federation Service Policy</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1015">Non più supportato</span><span class="sxs-lookup"><span data-stu-id="9827c-1015">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1016"><span id="AD_FS_Web_Agents"></span><span id="ad_fs_web_agents"></span><span id="AD_FS_WEB_AGENTS"></span>Agenti Web di AD FS</span><span class="sxs-lookup"><span data-stu-id="9827c-1016"><span id="AD_FS_Web_Agents"></span><span id="ad_fs_web_agents"></span><span id="AD_FS_WEB_AGENTS"></span>AD FS Web Agents</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1017">Non più supportato</span><span class="sxs-lookup"><span data-stu-id="9827c-1017">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1018"><span id="Windows_Token-based_Agent"></span><span id="windows_token-based_agent"></span><span id="WINDOWS_TOKEN-BASED_AGENT"></span>Agente basato su token Windows</span><span class="sxs-lookup"><span data-stu-id="9827c-1018"><span id="Windows_Token-based_Agent"></span><span id="windows_token-based_agent"></span><span id="WINDOWS_TOKEN-BASED_AGENT"></span>Windows Token-based Agent</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1019">Non più supportato</span><span class="sxs-lookup"><span data-stu-id="9827c-1019">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1020"><span id="Remote_Desktop_Licensing"></span><span id="remote_desktop_licensing"></span><span id="REMOTE_DESKTOP_LICENSING"></span>Gestione licenze Desktop remoto</span><span class="sxs-lookup"><span data-stu-id="9827c-1020"><span id="Remote_Desktop_Licensing"></span><span id="remote_desktop_licensing"></span><span id="REMOTE_DESKTOP_LICENSING"></span>Remote Desktop Licensing</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1021">Non più supportato</span><span class="sxs-lookup"><span data-stu-id="9827c-1021">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1022"><span id="Network_Policy_Server"></span><span id="network_policy_server"></span><span id="NETWORK_POLICY_SERVER"></span>Server dei criteri di rete</span><span class="sxs-lookup"><span data-stu-id="9827c-1022"><span id="Network_Policy_Server"></span><span id="network_policy_server"></span><span id="NETWORK_POLICY_SERVER"></span>Network Policy Server</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1023">Non più supportato</span><span class="sxs-lookup"><span data-stu-id="9827c-1023">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1024"><span id="VPN"></span><span id="vpn"></span>VPN</span><span class="sxs-lookup"><span data-stu-id="9827c-1024"><span id="VPN"></span><span id="vpn"></span>VPN</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1025">Non più supportato</span><span class="sxs-lookup"><span data-stu-id="9827c-1025">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1026"><span id="Remote_Access_Services"></span><span id="remote_access_services"></span><span id="REMOTE_ACCESS_SERVICES"></span>Servizi di accesso remoto</span><span class="sxs-lookup"><span data-stu-id="9827c-1026"><span id="Remote_Access_Services"></span><span id="remote_access_services"></span><span id="REMOTE_ACCESS_SERVICES"></span>Remote Access Services</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1027">Non più supportato</span><span class="sxs-lookup"><span data-stu-id="9827c-1027">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1028"><span id="Routing"></span><span id="routing"></span><span id="ROUTING"></span>Routing</span><span class="sxs-lookup"><span data-stu-id="9827c-1028"><span id="Routing"></span><span id="routing"></span><span id="ROUTING"></span>Routing</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1029">Non più supportato</span><span class="sxs-lookup"><span data-stu-id="9827c-1029">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1030"><span id="Health_Registration_Authority"></span><span id="health_registration_authority"></span><span id="HEALTH_REGISTRATION_AUTHORITY"></span>Autorità registrazione integrità</span><span class="sxs-lookup"><span data-stu-id="9827c-1030"><span id="Health_Registration_Authority"></span><span id="health_registration_authority"></span><span id="HEALTH_REGISTRATION_AUTHORITY"></span>Health Registration Authority</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1031">Non più supportato</span><span class="sxs-lookup"><span data-stu-id="9827c-1031">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1032"><span id="Host_Credential_Authorization_Protocol"></span><span id="host_credential_authorization_protocol"></span><span id="HOST_CREDENTIAL_AUTHORIZATION_PROTOCOL"></span>Protocollo di autorizzazione Host Credential</span><span class="sxs-lookup"><span data-stu-id="9827c-1032"><span id="Host_Credential_Authorization_Protocol"></span><span id="host_credential_authorization_protocol"></span><span id="HOST_CREDENTIAL_AUTHORIZATION_PROTOCOL"></span>Host Credential Authorization Protocol</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1033">Non più supportato</span><span class="sxs-lookup"><span data-stu-id="9827c-1033">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1034"><span id=".NET_Framework_3.5.1"></span><span id=".net_framework_3.5.1"></span><span id=".NET_FRAMEWORK_3.5.1"></span>.NET Framework 3.5.1</span><span class="sxs-lookup"><span data-stu-id="9827c-1034"><span id=".NET_Framework_3.5.1"></span><span id=".net_framework_3.5.1"></span><span id=".NET_FRAMEWORK_3.5.1"></span>.NET Framework 3.5.1</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1035">Non più supportato</span><span class="sxs-lookup"><span data-stu-id="9827c-1035">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1036"><span id="XPS_Viewer"></span><span id="xps_viewer"></span><span id="XPS_VIEWER"></span>Visualizzatore XPS</span><span class="sxs-lookup"><span data-stu-id="9827c-1036"><span id="XPS_Viewer"></span><span id="xps_viewer"></span><span id="XPS_VIEWER"></span>XPS Viewer</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1037">Non più supportato</span><span class="sxs-lookup"><span data-stu-id="9827c-1037">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1038"><span id="SNMP_Service"></span><span id="snmp_service"></span><span id="SNMP_SERVICE"></span>Servizio SNMP</span><span class="sxs-lookup"><span data-stu-id="9827c-1038"><span id="SNMP_Service"></span><span id="snmp_service"></span><span id="SNMP_SERVICE"></span>SNMP Service</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1039">Non più supportato</span><span class="sxs-lookup"><span data-stu-id="9827c-1039">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1040"><span id="SNMP_WMI_Provider"></span><span id="snmp_wmi_provider"></span><span id="SNMP_WMI_PROVIDER"></span>Provider WMI SNMP</span><span class="sxs-lookup"><span data-stu-id="9827c-1040"><span id="SNMP_WMI_Provider"></span><span id="snmp_wmi_provider"></span><span id="SNMP_WMI_PROVIDER"></span>SNMP WMI Provider</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1041">Non più supportato</span><span class="sxs-lookup"><span data-stu-id="9827c-1041">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1042"><span id=".NET_Framework_3.5.1"></span><span id=".net_framework_3.5.1"></span><span id=".NET_FRAMEWORK_3.5.1"></span>.NET Framework 3.5.1</span><span class="sxs-lookup"><span data-stu-id="9827c-1042"><span id=".NET_Framework_3.5.1"></span><span id=".net_framework_3.5.1"></span><span id=".NET_FRAMEWORK_3.5.1"></span>.NET Framework 3.5.1</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1043">Non più supportato</span><span class="sxs-lookup"><span data-stu-id="9827c-1043">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1044"><span id="Web_Server__IIS__Support"></span><span id="web_server__iis__support"></span><span id="WEB_SERVER__IIS__SUPPORT"></span>Supporto per server Web (IIS)</span><span class="sxs-lookup"><span data-stu-id="9827c-1044"><span id="Web_Server__IIS__Support"></span><span id="web_server__iis__support"></span><span id="WEB_SERVER__IIS__SUPPORT"></span>Web Server (IIS) Support</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1045">Non più supportato</span><span class="sxs-lookup"><span data-stu-id="9827c-1045">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1046"><span id="COM__Network_Access"></span><span id="com__network_access"></span><span id="COM__NETWORK_ACCESS"></span>Accesso alla rete COM+</span><span class="sxs-lookup"><span data-stu-id="9827c-1046"><span id="COM__Network_Access"></span><span id="com__network_access"></span><span id="COM__NETWORK_ACCESS"></span>COM+ Network Access</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1047">Non più supportato</span><span class="sxs-lookup"><span data-stu-id="9827c-1047">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1048"><span id="TCP_Port_Sharing"></span><span id="tcp_port_sharing"></span><span id="TCP_PORT_SHARING"></span>Condivisione delle porte TCP</span><span class="sxs-lookup"><span data-stu-id="9827c-1048"><span id="TCP_Port_Sharing"></span><span id="tcp_port_sharing"></span><span id="TCP_PORT_SHARING"></span>TCP Port Sharing</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1049">Non più supportato</span><span class="sxs-lookup"><span data-stu-id="9827c-1049">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1050"><span id="Windows_Process_Activation_Service_Support"></span><span id="windows_process_activation_service_support"></span><span id="WINDOWS_PROCESS_ACTIVATION_SERVICE_SUPPORT"></span>Supporto del servizio Attivazione processo Windows</span><span class="sxs-lookup"><span data-stu-id="9827c-1050"><span id="Windows_Process_Activation_Service_Support"></span><span id="windows_process_activation_service_support"></span><span id="WINDOWS_PROCESS_ACTIVATION_SERVICE_SUPPORT"></span>Windows Process Activation Service Support</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1051">Non più supportato</span><span class="sxs-lookup"><span data-stu-id="9827c-1051">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1052"><span id="HTTP_Activation"></span><span id="http_activation"></span><span id="HTTP_ACTIVATION"></span>Attivazione HTTP</span><span class="sxs-lookup"><span data-stu-id="9827c-1052"><span id="HTTP_Activation"></span><span id="http_activation"></span><span id="HTTP_ACTIVATION"></span>HTTP Activation</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1053">Non più supportato</span><span class="sxs-lookup"><span data-stu-id="9827c-1053">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1054"><span id="Message_Queuing_Activation"></span><span id="message_queuing_activation"></span><span id="MESSAGE_QUEUING_ACTIVATION"></span>Attivazione di Accodamento messaggi</span><span class="sxs-lookup"><span data-stu-id="9827c-1054"><span id="Message_Queuing_Activation"></span><span id="message_queuing_activation"></span><span id="MESSAGE_QUEUING_ACTIVATION"></span>Message Queuing Activation</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1055">Non più supportato</span><span class="sxs-lookup"><span data-stu-id="9827c-1055">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1056"><span id="TCP_Activation"></span><span id="tcp_activation"></span><span id="TCP_ACTIVATION"></span>Attivazione TCP</span><span class="sxs-lookup"><span data-stu-id="9827c-1056"><span id="TCP_Activation"></span><span id="tcp_activation"></span><span id="TCP_ACTIVATION"></span>TCP Activation</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1057">Non più supportato</span><span class="sxs-lookup"><span data-stu-id="9827c-1057">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1058"><span id="Named_Pipes_Activation"></span><span id="named_pipes_activation"></span><span id="NAMED_PIPES_ACTIVATION"></span>Attivazione named pipe</span><span class="sxs-lookup"><span data-stu-id="9827c-1058"><span id="Named_Pipes_Activation"></span><span id="named_pipes_activation"></span><span id="NAMED_PIPES_ACTIVATION"></span>Named Pipes Activation</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1059">Non più supportato</span><span class="sxs-lookup"><span data-stu-id="9827c-1059">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1060"><span id="Distributed_Transactions"></span><span id="distributed_transactions"></span><span id="DISTRIBUTED_TRANSACTIONS"></span>Transazioni distribuite</span><span class="sxs-lookup"><span data-stu-id="9827c-1060"><span id="Distributed_Transactions"></span><span id="distributed_transactions"></span><span id="DISTRIBUTED_TRANSACTIONS"></span>Distributed Transactions</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1061">Non più supportato</span><span class="sxs-lookup"><span data-stu-id="9827c-1061">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1062"><span id="Incoming_Remote_Transactions"></span><span id="incoming_remote_transactions"></span><span id="INCOMING_REMOTE_TRANSACTIONS"></span>Transazioni remote in ingresso</span><span class="sxs-lookup"><span data-stu-id="9827c-1062"><span id="Incoming_Remote_Transactions"></span><span id="incoming_remote_transactions"></span><span id="INCOMING_REMOTE_TRANSACTIONS"></span>Incoming Remote Transactions</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1063">Non più supportato</span><span class="sxs-lookup"><span data-stu-id="9827c-1063">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1064"><span id="Outgoing_Remote_Transactions"></span><span id="outgoing_remote_transactions"></span><span id="OUTGOING_REMOTE_TRANSACTIONS"></span>Transazioni remote in uscita</span><span class="sxs-lookup"><span data-stu-id="9827c-1064"><span id="Outgoing_Remote_Transactions"></span><span id="outgoing_remote_transactions"></span><span id="OUTGOING_REMOTE_TRANSACTIONS"></span>Outgoing Remote Transactions</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1065">Non più supportato</span><span class="sxs-lookup"><span data-stu-id="9827c-1065">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1066"><span id="WS-Automatic_Transactions"></span><span id="ws-automatic_transactions"></span><span id="WS-AUTOMATIC_TRANSACTIONS"></span>Transazioni WS-automatiche</span><span class="sxs-lookup"><span data-stu-id="9827c-1066"><span id="WS-Automatic_Transactions"></span><span id="ws-automatic_transactions"></span><span id="WS-AUTOMATIC_TRANSACTIONS"></span>WS-Automatic Transactions</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1067">Non più supportato</span><span class="sxs-lookup"><span data-stu-id="9827c-1067">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1068"><span id="Application_Server_Extensions_for_.NET_4.0"></span><span id="application_server_extensions_for_.net_4.0"></span><span id="APPLICATION_SERVER_EXTENSIONS_FOR_.NET_4.0"></span>Estensioni del server applicazioni per .NET 4,0</span><span class="sxs-lookup"><span data-stu-id="9827c-1068"><span id="Application_Server_Extensions_for_.NET_4.0"></span><span id="application_server_extensions_for_.net_4.0"></span><span id="APPLICATION_SERVER_EXTENSIONS_FOR_.NET_4.0"></span>Application Server Extensions for .NET 4.0</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1069">Non più supportato</span><span class="sxs-lookup"><span data-stu-id="9827c-1069">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1070"><span id="Role_Administration_Tools"></span><span id="role_administration_tools"></span><span id="ROLE_ADMINISTRATION_TOOLS"></span>Strumenti di amministrazione ruoli</span><span class="sxs-lookup"><span data-stu-id="9827c-1070"><span id="Role_Administration_Tools"></span><span id="role_administration_tools"></span><span id="ROLE_ADMINISTRATION_TOOLS"></span>Role Administration Tools</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1071">Non più supportato</span><span class="sxs-lookup"><span data-stu-id="9827c-1071">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1072"><span id="AD_DS_Tools"></span><span id="ad_ds_tools"></span><span id="AD_DS_TOOLS"></span>Strumenti di servizi di dominio Active Directory</span><span class="sxs-lookup"><span data-stu-id="9827c-1072"><span id="AD_DS_Tools"></span><span id="ad_ds_tools"></span><span id="AD_DS_TOOLS"></span>AD DS Tools</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1073">Non più supportato</span><span class="sxs-lookup"><span data-stu-id="9827c-1073">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1074"><span id="AD_LDS_Snap-Ins_and_Command-Line_Tools"></span><span id="ad_lds_snap-ins_and_command-line_tools"></span><span id="AD_LDS_SNAP-INS_AND_COMMAND-LINE_TOOLS"></span>Strumenti di AD LDS Snap-Ins e Command-Line</span><span class="sxs-lookup"><span data-stu-id="9827c-1074"><span id="AD_LDS_Snap-Ins_and_Command-Line_Tools"></span><span id="ad_lds_snap-ins_and_command-line_tools"></span><span id="AD_LDS_SNAP-INS_AND_COMMAND-LINE_TOOLS"></span>AD LDS Snap-Ins and Command-Line Tools</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1075">Non più supportato</span><span class="sxs-lookup"><span data-stu-id="9827c-1075">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1076"><span id="Network_Policy_and_Access_Services"></span><span id="network_policy_and_access_services"></span><span id="NETWORK_POLICY_AND_ACCESS_SERVICES"></span>Servizi di accesso e criteri di rete</span><span class="sxs-lookup"><span data-stu-id="9827c-1076"><span id="Network_Policy_and_Access_Services"></span><span id="network_policy_and_access_services"></span><span id="NETWORK_POLICY_AND_ACCESS_SERVICES"></span>Network Policy and Access Services</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1077">Non più supportato</span><span class="sxs-lookup"><span data-stu-id="9827c-1077">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1078"><span id="Active_Directory_Rights_Management_Services"></span><span id="active_directory_rights_management_services"></span><span id="ACTIVE_DIRECTORY_RIGHTS_MANAGEMENT_SERVICES"></span>Active Directory Rights Management Services</span><span class="sxs-lookup"><span data-stu-id="9827c-1078"><span id="Active_Directory_Rights_Management_Services"></span><span id="active_directory_rights_management_services"></span><span id="ACTIVE_DIRECTORY_RIGHTS_MANAGEMENT_SERVICES"></span>Active Directory Rights Management Services</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1079">Non più supportato</span><span class="sxs-lookup"><span data-stu-id="9827c-1079">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1080"><span id="Remote_Desktop_Services_Tools"></span><span id="remote_desktop_services_tools"></span><span id="REMOTE_DESKTOP_SERVICES_TOOLS"></span>Strumenti di Servizi Desktop remoto</span><span class="sxs-lookup"><span data-stu-id="9827c-1080"><span id="Remote_Desktop_Services_Tools"></span><span id="remote_desktop_services_tools"></span><span id="REMOTE_DESKTOP_SERVICES_TOOLS"></span>Remote Desktop Services Tools</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1081">Non più supportato</span><span class="sxs-lookup"><span data-stu-id="9827c-1081">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1082"><span id="Feature_Administration_Tools"></span><span id="feature_administration_tools"></span><span id="FEATURE_ADMINISTRATION_TOOLS"></span>Strumenti di amministrazione funzionalità</span><span class="sxs-lookup"><span data-stu-id="9827c-1082"><span id="Feature_Administration_Tools"></span><span id="feature_administration_tools"></span><span id="FEATURE_ADMINISTRATION_TOOLS"></span>Feature Administration Tools</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1083">Non più supportato</span><span class="sxs-lookup"><span data-stu-id="9827c-1083">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1084"><span id="Failover_Clustering_Tools"></span><span id="failover_clustering_tools"></span><span id="FAILOVER_CLUSTERING_TOOLS"></span>Strumenti per clustering di failover</span><span class="sxs-lookup"><span data-stu-id="9827c-1084"><span id="Failover_Clustering_Tools"></span><span id="failover_clustering_tools"></span><span id="FAILOVER_CLUSTERING_TOOLS"></span>Failover Clustering Tools</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1085">Non più supportato</span><span class="sxs-lookup"><span data-stu-id="9827c-1085">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1086"><span id="DNS_Server_Tools"></span><span id="dns_server_tools"></span><span id="DNS_SERVER_TOOLS"></span>Strumenti server DNS</span><span class="sxs-lookup"><span data-stu-id="9827c-1086"><span id="DNS_Server_Tools"></span><span id="dns_server_tools"></span><span id="DNS_SERVER_TOOLS"></span>DNS Server Tools</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1087">Non più supportato</span><span class="sxs-lookup"><span data-stu-id="9827c-1087">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1088"><span id="Services_For_Network_File_System_Tools"></span><span id="services_for_network_file_system_tools"></span><span id="SERVICES_FOR_NETWORK_FILE_SYSTEM_TOOLS"></span>Servizi per gli strumenti del file System di rete</span><span class="sxs-lookup"><span data-stu-id="9827c-1088"><span id="Services_For_Network_File_System_Tools"></span><span id="services_for_network_file_system_tools"></span><span id="SERVICES_FOR_NETWORK_FILE_SYSTEM_TOOLS"></span>Services For Network File System Tools</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1089">Non più supportato</span><span class="sxs-lookup"><span data-stu-id="9827c-1089">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1090"><span id="Web_Server__IIS__Tools"></span><span id="web_server__iis__tools"></span><span id="WEB_SERVER__IIS__TOOLS"></span>Strumenti per server Web (IIS)</span><span class="sxs-lookup"><span data-stu-id="9827c-1090"><span id="Web_Server__IIS__Tools"></span><span id="web_server__iis__tools"></span><span id="WEB_SERVER__IIS__TOOLS"></span>Web Server (IIS) Tools</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1091">Non più supportato</span><span class="sxs-lookup"><span data-stu-id="9827c-1091">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1092"><span id="Server_for_NIS_Tools"></span><span id="server_for_nis_tools"></span><span id="SERVER_FOR_NIS_TOOLS"></span>Strumenti di server per NIS</span><span class="sxs-lookup"><span data-stu-id="9827c-1092"><span id="Server_for_NIS_Tools"></span><span id="server_for_nis_tools"></span><span id="SERVER_FOR_NIS_TOOLS"></span>Server for NIS Tools</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1093">Non più supportato</span><span class="sxs-lookup"><span data-stu-id="9827c-1093">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1094"><span id="AD_DS_Snap-Ins_and_Command-Line_Tools"></span><span id="ad_ds_snap-ins_and_command-line_tools"></span><span id="AD_DS_SNAP-INS_AND_COMMAND-LINE_TOOLS"></span>Strumenti di Snap-Ins e Command-Line di servizi di dominio Active Directory</span><span class="sxs-lookup"><span data-stu-id="9827c-1094"><span id="AD_DS_Snap-Ins_and_Command-Line_Tools"></span><span id="ad_ds_snap-ins_and_command-line_tools"></span><span id="AD_DS_SNAP-INS_AND_COMMAND-LINE_TOOLS"></span>AD DS Snap-Ins and Command-Line Tools</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1095">Non più supportato</span><span class="sxs-lookup"><span data-stu-id="9827c-1095">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1096"><span id="AD_DS_and_AD_LDS_Tools"></span><span id="ad_ds_and_ad_lds_tools"></span><span id="AD_DS_AND_AD_LDS_TOOLS"></span>Strumenti per servizi di dominio Active Directory e AD LDS</span><span class="sxs-lookup"><span data-stu-id="9827c-1096"><span id="AD_DS_and_AD_LDS_Tools"></span><span id="ad_ds_and_ad_lds_tools"></span><span id="AD_DS_AND_AD_LDS_TOOLS"></span>AD DS and AD LDS Tools</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1097">Non più supportato</span><span class="sxs-lookup"><span data-stu-id="9827c-1097">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1098"><span id="Remote_Desktop_Connection_Broker_Tools"></span><span id="remote_desktop_connection_broker_tools"></span><span id="REMOTE_DESKTOP_CONNECTION_BROKER_TOOLS"></span>Strumenti di Connessione Desktop remoto broker</span><span class="sxs-lookup"><span data-stu-id="9827c-1098"><span id="Remote_Desktop_Connection_Broker_Tools"></span><span id="remote_desktop_connection_broker_tools"></span><span id="REMOTE_DESKTOP_CONNECTION_BROKER_TOOLS"></span>Remote Desktop Connection Broker Tools</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1099">Non più supportato</span><span class="sxs-lookup"><span data-stu-id="9827c-1099">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1100"><span id="IP_Address_Management__IPAM__Client"></span><span id="ip_address_management__ipam__client"></span><span id="IP_ADDRESS_MANAGEMENT__IPAM__CLIENT"></span>Client di gestione indirizzi IP</span><span class="sxs-lookup"><span data-stu-id="9827c-1100"><span id="IP_Address_Management__IPAM__Client"></span><span id="ip_address_management__ipam__client"></span><span id="IP_ADDRESS_MANAGEMENT__IPAM__CLIENT"></span>IP Address Management (IPAM) Client</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1101">Aggiunta</span><span class="sxs-lookup"><span data-stu-id="9827c-1101">Added</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1102"><span id="Hyper-V_Module_for_Windows_PowerShell"></span><span id="hyper-v_module_for_windows_powershell"></span><span id="HYPER-V_MODULE_FOR_WINDOWS_POWERSHELL"></span>Modulo Hyper-V per Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="9827c-1102"><span id="Hyper-V_Module_for_Windows_PowerShell"></span><span id="hyper-v_module_for_windows_powershell"></span><span id="HYPER-V_MODULE_FOR_WINDOWS_POWERSHELL"></span>Hyper-V Module for Windows PowerShell</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="9827c-1103"><span id="Active_Directory_Rights_Management_Services_Tool"></span><span id="active_directory_rights_management_services_tool"></span><span id="ACTIVE_DIRECTORY_RIGHTS_MANAGEMENT_SERVICES_TOOL"></span>Strumento Active Directory Rights Management Services</span><span class="sxs-lookup"><span data-stu-id="9827c-1103"><span id="Active_Directory_Rights_Management_Services_Tool"></span><span id="active_directory_rights_management_services_tool"></span><span id="ACTIVE_DIRECTORY_RIGHTS_MANAGEMENT_SERVICES_TOOL"></span>Active Directory Rights Management Services Tool</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1104">Aggiunta</span><span class="sxs-lookup"><span data-stu-id="9827c-1104">Added</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1105"><span id="Share_and_Storage_Management_Tool"></span><span id="share_and_storage_management_tool"></span><span id="SHARE_AND_STORAGE_MANAGEMENT_TOOL"></span>Strumento di Gestione condivisione e archiviazione</span><span class="sxs-lookup"><span data-stu-id="9827c-1105"><span id="Share_and_Storage_Management_Tool"></span><span id="share_and_storage_management_tool"></span><span id="SHARE_AND_STORAGE_MANAGEMENT_TOOL"></span>Share and Storage Management Tool</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1106">Aggiunta</span><span class="sxs-lookup"><span data-stu-id="9827c-1106">Added</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1107"><span id="Remote_Access_Management_Tools"></span><span id="remote_access_management_tools"></span><span id="REMOTE_ACCESS_MANAGEMENT_TOOLS"></span>Strumenti di gestione di accesso remoto</span><span class="sxs-lookup"><span data-stu-id="9827c-1107"><span id="Remote_Access_Management_Tools"></span><span id="remote_access_management_tools"></span><span id="REMOTE_ACCESS_MANAGEMENT_TOOLS"></span>Remote Access Management Tools</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1108">Aggiunta</span><span class="sxs-lookup"><span data-stu-id="9827c-1108">Added</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1109"><span id="Remote_Access_module_for_Windows_PowerShell"></span><span id="remote_access_module_for_windows_powershell"></span><span id="REMOTE_ACCESS_MODULE_FOR_WINDOWS_POWERSHELL"></span>Modulo di accesso remoto per Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="9827c-1109"><span id="Remote_Access_module_for_Windows_PowerShell"></span><span id="remote_access_module_for_windows_powershell"></span><span id="REMOTE_ACCESS_MODULE_FOR_WINDOWS_POWERSHELL"></span>Remote Access module for Windows PowerShell</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1110">Aggiunta</span><span class="sxs-lookup"><span data-stu-id="9827c-1110">Added</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1111"><span id="Remote_Access_GUI_and_Command-Line_Tools"></span><span id="remote_access_gui_and_command-line_tools"></span><span id="REMOTE_ACCESS_GUI_AND_COMMAND-LINE_TOOLS"></span>GUI di accesso remoto e strumenti di Command-Line</span><span class="sxs-lookup"><span data-stu-id="9827c-1111"><span id="Remote_Access_GUI_and_Command-Line_Tools"></span><span id="remote_access_gui_and_command-line_tools"></span><span id="REMOTE_ACCESS_GUI_AND_COMMAND-LINE_TOOLS"></span>Remote Access GUI and Command-Line Tools</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1112">Aggiunta</span><span class="sxs-lookup"><span data-stu-id="9827c-1112">Added</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1113"><span id="Windows_Server_Update_Services_Tools"></span><span id="windows_server_update_services_tools"></span><span id="WINDOWS_SERVER_UPDATE_SERVICES_TOOLS"></span>Strumenti di Windows Server Update Services</span><span class="sxs-lookup"><span data-stu-id="9827c-1113"><span id="Windows_Server_Update_Services_Tools"></span><span id="windows_server_update_services_tools"></span><span id="WINDOWS_SERVER_UPDATE_SERVICES_TOOLS"></span>Windows Server Update Services Tools</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1114">Aggiunta</span><span class="sxs-lookup"><span data-stu-id="9827c-1114">Added</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1115"><span id="Remote_Desktop_Licensing_Diagnoser_Tools"></span><span id="remote_desktop_licensing_diagnoser_tools"></span><span id="REMOTE_DESKTOP_LICENSING_DIAGNOSER_TOOLS"></span>Strumenti di diagnostica delle licenze Desktop remoto</span><span class="sxs-lookup"><span data-stu-id="9827c-1115"><span id="Remote_Desktop_Licensing_Diagnoser_Tools"></span><span id="remote_desktop_licensing_diagnoser_tools"></span><span id="REMOTE_DESKTOP_LICENSING_DIAGNOSER_TOOLS"></span>Remote Desktop Licensing Diagnoser Tools</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1116">Aggiunta</span><span class="sxs-lookup"><span data-stu-id="9827c-1116">Added</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1117"><span id="SNMP_Tools"></span><span id="snmp_tools"></span><span id="SNMP_TOOLS"></span>Strumenti SNMP</span><span class="sxs-lookup"><span data-stu-id="9827c-1117"><span id="SNMP_Tools"></span><span id="snmp_tools"></span><span id="SNMP_TOOLS"></span>SNMP Tools</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1118">Aggiunta</span><span class="sxs-lookup"><span data-stu-id="9827c-1118">Added</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1119"><span id="Volume_Activation_Tools"></span><span id="volume_activation_tools"></span><span id="VOLUME_ACTIVATION_TOOLS"></span>Strumenti di attivazione contratti multilicenza</span><span class="sxs-lookup"><span data-stu-id="9827c-1119"><span id="Volume_Activation_Tools"></span><span id="volume_activation_tools"></span><span id="VOLUME_ACTIVATION_TOOLS"></span>Volume Activation Tools</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1120">Aggiunta</span><span class="sxs-lookup"><span data-stu-id="9827c-1120">Added</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1121"><span id="Windows_Server_Backup"></span><span id="windows_server_backup"></span><span id="WINDOWS_SERVER_BACKUP"></span>Windows Server Backup</span><span class="sxs-lookup"><span data-stu-id="9827c-1121"><span id="Windows_Server_Backup"></span><span id="windows_server_backup"></span><span id="WINDOWS_SERVER_BACKUP"></span>Windows Server Backup</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1122">Non più supportato</span><span class="sxs-lookup"><span data-stu-id="9827c-1122">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1123"><span id="Command_Line_Tools"></span><span id="command_line_tools"></span><span id="COMMAND_LINE_TOOLS"></span>Strumenti da riga di comando</span><span class="sxs-lookup"><span data-stu-id="9827c-1123"><span id="Command_Line_Tools"></span><span id="command_line_tools"></span><span id="COMMAND_LINE_TOOLS"></span>Command Line Tools</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1124">Non più supportato</span><span class="sxs-lookup"><span data-stu-id="9827c-1124">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1125"><span id="Ink_Support"></span><span id="ink_support"></span><span id="INK_SUPPORT"></span>Supporto per input penna</span><span class="sxs-lookup"><span data-stu-id="9827c-1125"><span id="Ink_Support"></span><span id="ink_support"></span><span id="INK_SUPPORT"></span>Ink Support</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1126">Non più supportato</span><span class="sxs-lookup"><span data-stu-id="9827c-1126">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1127"><span id="Handwriting_Recognition"></span><span id="handwriting_recognition"></span><span id="HANDWRITING_RECOGNITION"></span>Riconoscimento della grafia</span><span class="sxs-lookup"><span data-stu-id="9827c-1127"><span id="Handwriting_Recognition"></span><span id="handwriting_recognition"></span><span id="HANDWRITING_RECOGNITION"></span>Handwriting Recognition</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1128">Non più supportato</span><span class="sxs-lookup"><span data-stu-id="9827c-1128">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1129"><span id="Compact_Server"></span><span id="compact_server"></span><span id="COMPACT_SERVER"></span>Server Compact</span><span class="sxs-lookup"><span data-stu-id="9827c-1129"><span id="Compact_Server"></span><span id="compact_server"></span><span id="COMPACT_SERVER"></span>Compact Server</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1130">Non più supportato</span><span class="sxs-lookup"><span data-stu-id="9827c-1130">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1131"><span id="WoW64"></span><span id="wow64"></span><span id="WOW64"></span>WoW64</span><span class="sxs-lookup"><span data-stu-id="9827c-1131"><span id="WoW64"></span><span id="wow64"></span><span id="WOW64"></span>WoW64</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1132">Non più supportato</span><span class="sxs-lookup"><span data-stu-id="9827c-1132">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1133"><span id="WoW64_for_.NET_Framework_2.0_and___________"></span><span id="wow64_for_.net_framework_2.0_and___________"></span><span id="WOW64_FOR_.NET_FRAMEWORK_2.0_AND___________"></span>WoW64 per .NET Framework 2,0 e PowerShell</span><span class="sxs-lookup"><span data-stu-id="9827c-1133"><span id="WoW64_for_.NET_Framework_2.0_and___________"></span><span id="wow64_for_.net_framework_2.0_and___________"></span><span id="WOW64_FOR_.NET_FRAMEWORK_2.0_AND___________"></span>WoW64 for .NET Framework 2.0 and PowerShell</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1134">Non più supportato</span><span class="sxs-lookup"><span data-stu-id="9827c-1134">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1135"><span id="WoW64_for_.NET_Framework_2.0"></span><span id="wow64_for_.net_framework_2.0"></span><span id="WOW64_FOR_.NET_FRAMEWORK_2.0"></span>WoW64 per .NET Framework 2,0</span><span class="sxs-lookup"><span data-stu-id="9827c-1135"><span id="WoW64_for_.NET_Framework_2.0"></span><span id="wow64_for_.net_framework_2.0"></span><span id="WOW64_FOR_.NET_FRAMEWORK_2.0"></span>WoW64 for .NET Framework 2.0</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1136">Non più supportato</span><span class="sxs-lookup"><span data-stu-id="9827c-1136">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1137"><span id="WoW64_for___________"></span><span id="wow64_for___________"></span><span id="WOW64_FOR___________"></span>WoW64 per PowerShell</span><span class="sxs-lookup"><span data-stu-id="9827c-1137"><span id="WoW64_for___________"></span><span id="wow64_for___________"></span><span id="WOW64_FOR___________"></span>WoW64 for PowerShell</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1138">Non più supportato</span><span class="sxs-lookup"><span data-stu-id="9827c-1138">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1139"><span id="WoW64_for_.NET_Framework_3.0_and_3.5"></span><span id="wow64_for_.net_framework_3.0_and_3.5"></span><span id="WOW64_FOR_.NET_FRAMEWORK_3.0_AND_3.5"></span>WoW64 per .NET Framework 3,0 e 3,5</span><span class="sxs-lookup"><span data-stu-id="9827c-1139"><span id="WoW64_for_.NET_Framework_3.0_and_3.5"></span><span id="wow64_for_.net_framework_3.0_and_3.5"></span><span id="WOW64_FOR_.NET_FRAMEWORK_3.0_AND_3.5"></span>WoW64 for .NET Framework 3.0 and 3.5</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1140">Non più supportato</span><span class="sxs-lookup"><span data-stu-id="9827c-1140">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1141"><span id="WoW64_for_Print_Services"></span><span id="wow64_for_print_services"></span><span id="WOW64_FOR_PRINT_SERVICES"></span>WoW64 per servizi di stampa</span><span class="sxs-lookup"><span data-stu-id="9827c-1141"><span id="WoW64_for_Print_Services"></span><span id="wow64_for_print_services"></span><span id="WOW64_FOR_PRINT_SERVICES"></span>WoW64 for Print Services</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1142">Non più supportato</span><span class="sxs-lookup"><span data-stu-id="9827c-1142">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1143"><span id="WoW64_for_Failover_Clustering"></span><span id="wow64_for_failover_clustering"></span><span id="WOW64_FOR_FAILOVER_CLUSTERING"></span>WoW64 per il clustering di failover</span><span class="sxs-lookup"><span data-stu-id="9827c-1143"><span id="WoW64_for_Failover_Clustering"></span><span id="wow64_for_failover_clustering"></span><span id="WOW64_FOR_FAILOVER_CLUSTERING"></span>WoW64 for Failover Clustering</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1144">Non più supportato</span><span class="sxs-lookup"><span data-stu-id="9827c-1144">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1145"><span id="WoW64_for_Input_Method_Editor"></span><span id="wow64_for_input_method_editor"></span><span id="WOW64_FOR_INPUT_METHOD_EDITOR"></span>WoW64 per input Method Editor</span><span class="sxs-lookup"><span data-stu-id="9827c-1145"><span id="WoW64_for_Input_Method_Editor"></span><span id="wow64_for_input_method_editor"></span><span id="WOW64_FOR_INPUT_METHOD_EDITOR"></span>WoW64 for Input Method Editor</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1146">Non più supportato</span><span class="sxs-lookup"><span data-stu-id="9827c-1146">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1147"><span id="WoW64_for_Subsystem_for_UNIX-based_Applications"></span><span id="wow64_for_subsystem_for_unix-based_applications"></span><span id="WOW64_FOR_SUBSYSTEM_FOR_UNIX-BASED_APPLICATIONS"></span>WoW64 per sottosistema per applicazioni basate su UNIX</span><span class="sxs-lookup"><span data-stu-id="9827c-1147"><span id="WoW64_for_Subsystem_for_UNIX-based_Applications"></span><span id="wow64_for_subsystem_for_unix-based_applications"></span><span id="WOW64_FOR_SUBSYSTEM_FOR_UNIX-BASED_APPLICATIONS"></span>WoW64 for Subsystem for UNIX-based Applications</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1148">Non più supportato</span><span class="sxs-lookup"><span data-stu-id="9827c-1148">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1149"><span id="Desktop_Experience"></span><span id="desktop_experience"></span><span id="DESKTOP_EXPERIENCE"></span>Esperienza desktop</span><span class="sxs-lookup"><span data-stu-id="9827c-1149"><span id="Desktop_Experience"></span><span id="desktop_experience"></span><span id="DESKTOP_EXPERIENCE"></span>Desktop Experience</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1150">Aggiunta</span><span class="sxs-lookup"><span data-stu-id="9827c-1150">Added</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1151"><span id="Server_Graphical_Shell"></span><span id="server_graphical_shell"></span><span id="SERVER_GRAPHICAL_SHELL"></span>Shell grafica server</span><span class="sxs-lookup"><span data-stu-id="9827c-1151"><span id="Server_Graphical_Shell"></span><span id="server_graphical_shell"></span><span id="SERVER_GRAPHICAL_SHELL"></span>Server Graphical Shell</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1152">Aggiunta</span><span class="sxs-lookup"><span data-stu-id="9827c-1152">Added</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1153"><span id="API_and_PowerShell_cmdlets"></span><span id="api_and_powershell_cmdlets"></span><span id="API_AND_POWERSHELL_CMDLETS"></span>API e cmdlet di PowerShell</span><span class="sxs-lookup"><span data-stu-id="9827c-1153"><span id="API_and_PowerShell_cmdlets"></span><span id="api_and_powershell_cmdlets"></span><span id="API_AND_POWERSHELL_CMDLETS"></span>API and PowerShell cmdlets</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1154">Aggiunta</span><span class="sxs-lookup"><span data-stu-id="9827c-1154">Added</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1155"><span id="SQL_Server_Connectivity"></span><span id="sql_server_connectivity"></span><span id="SQL_SERVER_CONNECTIVITY"></span>Connettività SQL Server</span><span class="sxs-lookup"><span data-stu-id="9827c-1155"><span id="SQL_Server_Connectivity"></span><span id="sql_server_connectivity"></span><span id="SQL_SERVER_CONNECTIVITY"></span>SQL Server Connectivity</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1156">Aggiunta</span><span class="sxs-lookup"><span data-stu-id="9827c-1156">Added</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1157"><span id="WSUS_Services"></span><span id="wsus_services"></span><span id="WSUS_SERVICES"></span>Servizi WSUS</span><span class="sxs-lookup"><span data-stu-id="9827c-1157"><span id="WSUS_Services"></span><span id="wsus_services"></span><span id="WSUS_SERVICES"></span>WSUS Services</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1158">Aggiunta</span><span class="sxs-lookup"><span data-stu-id="9827c-1158">Added</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1159"><span id="User_Interface_Management_Console"></span><span id="user_interface_management_console"></span><span id="USER_INTERFACE_MANAGEMENT_CONSOLE"></span>Console di gestione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="9827c-1159"><span id="User_Interface_Management_Console"></span><span id="user_interface_management_console"></span><span id="USER_INTERFACE_MANAGEMENT_CONSOLE"></span>User Interface Management Console</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1160">Aggiunta</span><span class="sxs-lookup"><span data-stu-id="9827c-1160">Added</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1161"><span id="WID_Connectivity"></span><span id="wid_connectivity"></span><span id="WID_CONNECTIVITY"></span>Connettività WID</span><span class="sxs-lookup"><span data-stu-id="9827c-1161"><span id="WID_Connectivity"></span><span id="wid_connectivity"></span><span id="WID_CONNECTIVITY"></span>WID Connectivity</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1162">Aggiunta</span><span class="sxs-lookup"><span data-stu-id="9827c-1162">Added</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1163"><span id="Windows_PowerShell_2.0_Engine"></span><span id="windows_powershell_2.0_engine"></span><span id="WINDOWS_POWERSHELL_2.0_ENGINE"></span>Motore di Windows PowerShell 2,0</span><span class="sxs-lookup"><span data-stu-id="9827c-1163"><span id="Windows_PowerShell_2.0_Engine"></span><span id="windows_powershell_2.0_engine"></span><span id="WINDOWS_POWERSHELL_2.0_ENGINE"></span>Windows PowerShell 2.0 Engine</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1164">Aggiunta</span><span class="sxs-lookup"><span data-stu-id="9827c-1164">Added</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1165"><span id="Windows_PowerShell_3.0"></span><span id="windows_powershell_3.0"></span><span id="WINDOWS_POWERSHELL_3.0"></span>Windows PowerShell 3,0</span><span class="sxs-lookup"><span data-stu-id="9827c-1165"><span id="Windows_PowerShell_3.0"></span><span id="windows_powershell_3.0"></span><span id="WINDOWS_POWERSHELL_3.0"></span>Windows PowerShell 3.0</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1166">Aggiunta</span><span class="sxs-lookup"><span data-stu-id="9827c-1166">Added</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1167"><span id="Windows_PowerShell_Web_Access"></span><span id="windows_powershell_web_access"></span><span id="WINDOWS_POWERSHELL_WEB_ACCESS"></span>Accesso Web di Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="9827c-1167"><span id="Windows_PowerShell_Web_Access"></span><span id="windows_powershell_web_access"></span><span id="WINDOWS_POWERSHELL_WEB_ACCESS"></span>Windows PowerShell Web Access</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1168">Aggiunta</span><span class="sxs-lookup"><span data-stu-id="9827c-1168">Added</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1169"><span id="Windows_PowerShell_Desired_State_Configuration_Service"></span><span id="windows_powershell_desired_state_configuration_service"></span><span id="WINDOWS_POWERSHELL_DESIRED_STATE_CONFIGURATION_SERVICE"></span>Servizio di configurazione dello stato desiderato di Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="9827c-1169"><span id="Windows_PowerShell_Desired_State_Configuration_Service"></span><span id="windows_powershell_desired_state_configuration_service"></span><span id="WINDOWS_POWERSHELL_DESIRED_STATE_CONFIGURATION_SERVICE"></span>Windows PowerShell Desired State Configuration Service</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1170">Aggiunta</span><span class="sxs-lookup"><span data-stu-id="9827c-1170">Added</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1171"><span id=".NET_Framework_4.5_Extended"></span><span id=".net_framework_4.5_extended"></span><span id=".NET_FRAMEWORK_4.5_EXTENDED"></span>.NET Framework 4,5 esteso</span><span class="sxs-lookup"><span data-stu-id="9827c-1171"><span id=".NET_Framework_4.5_Extended"></span><span id=".net_framework_4.5_extended"></span><span id=".NET_FRAMEWORK_4.5_EXTENDED"></span>.NET Framework 4.5 Extended</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1172">Aggiunta</span><span class="sxs-lookup"><span data-stu-id="9827c-1172">Added</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1173"><span id="WCF_Services"></span><span id="wcf_services"></span><span id="WCF_SERVICES"></span>Servizi WCF</span><span class="sxs-lookup"><span data-stu-id="9827c-1173"><span id="WCF_Services"></span><span id="wcf_services"></span><span id="WCF_SERVICES"></span>WCF Services</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1174">Aggiunta</span><span class="sxs-lookup"><span data-stu-id="9827c-1174">Added</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1175"><span id="HTTP_Activation"></span><span id="http_activation"></span><span id="HTTP_ACTIVATION"></span>Attivazione HTTP</span><span class="sxs-lookup"><span data-stu-id="9827c-1175"><span id="HTTP_Activation"></span><span id="http_activation"></span><span id="HTTP_ACTIVATION"></span>HTTP Activation</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1176">Aggiunta</span><span class="sxs-lookup"><span data-stu-id="9827c-1176">Added</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1177"><span id="Message_Queuing__MSMQ__Activation"></span><span id="message_queuing__msmq__activation"></span><span id="MESSAGE_QUEUING__MSMQ__ACTIVATION"></span>Attivazione di Accodamento messaggi (MSMQ)</span><span class="sxs-lookup"><span data-stu-id="9827c-1177"><span id="Message_Queuing__MSMQ__Activation"></span><span id="message_queuing__msmq__activation"></span><span id="MESSAGE_QUEUING__MSMQ__ACTIVATION"></span>Message Queuing (MSMQ) Activation</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="9827c-1178"><span id="Named_Pipe_Activation"></span><span id="named_pipe_activation"></span><span id="NAMED_PIPE_ACTIVATION"></span>Attivazione named pipe</span><span class="sxs-lookup"><span data-stu-id="9827c-1178"><span id="Named_Pipe_Activation"></span><span id="named_pipe_activation"></span><span id="NAMED_PIPE_ACTIVATION"></span>Named Pipe Activation</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1179">Aggiunta</span><span class="sxs-lookup"><span data-stu-id="9827c-1179">Added</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1180"><span id="TCP_Activation"></span><span id="tcp_activation"></span><span id="TCP_ACTIVATION"></span>Attivazione TCP</span><span class="sxs-lookup"><span data-stu-id="9827c-1180"><span id="TCP_Activation"></span><span id="tcp_activation"></span><span id="TCP_ACTIVATION"></span>TCP Activation</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1181">Aggiunta</span><span class="sxs-lookup"><span data-stu-id="9827c-1181">Added</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1182"><span id="TCP_Port_Sharing"></span><span id="tcp_port_sharing"></span><span id="TCP_PORT_SHARING"></span>Condivisione delle porte TCP</span><span class="sxs-lookup"><span data-stu-id="9827c-1182"><span id="TCP_Port_Sharing"></span><span id="tcp_port_sharing"></span><span id="TCP_PORT_SHARING"></span>TCP Port Sharing</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1183">Aggiunta</span><span class="sxs-lookup"><span data-stu-id="9827c-1183">Added</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1184"><span id="ASP.NET_4.5"></span><span id="asp.net_4.5"></span>ASP.NET 4,5</span><span class="sxs-lookup"><span data-stu-id="9827c-1184"><span id="ASP.NET_4.5"></span><span id="asp.net_4.5"></span>ASP.NET 4.5</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1185">Aggiunta</span><span class="sxs-lookup"><span data-stu-id="9827c-1185">Added</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1186"><span id=".NET_Extensibility_4.5"></span><span id=".net_extensibility_4.5"></span><span id=".NET_EXTENSIBILITY_4.5"></span>Estendibilità .NET 4,5</span><span class="sxs-lookup"><span data-stu-id="9827c-1186"><span id=".NET_Extensibility_4.5"></span><span id=".net_extensibility_4.5"></span><span id=".NET_EXTENSIBILITY_4.5"></span>.NET Extensibility 4.5</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1187">Aggiunta</span><span class="sxs-lookup"><span data-stu-id="9827c-1187">Added</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1188"><span id="DirectAccess_and_VPN__RAS_"></span><span id="directaccess_and_vpn__ras_"></span><span id="DIRECTACCESS_AND_VPN__RAS_"></span>DirectAccess e VPN (RAS)</span><span class="sxs-lookup"><span data-stu-id="9827c-1188"><span id="DirectAccess_and_VPN__RAS_"></span><span id="directaccess_and_vpn__ras_"></span><span id="DIRECTACCESS_AND_VPN__RAS_"></span>DirectAccess and VPN (RAS)</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1189">Aggiunta</span><span class="sxs-lookup"><span data-stu-id="9827c-1189">Added</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1190"><span id="Routing"></span><span id="routing"></span><span id="ROUTING"></span>Routing</span><span class="sxs-lookup"><span data-stu-id="9827c-1190"><span id="Routing"></span><span id="routing"></span><span id="ROUTING"></span>Routing</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1191">Aggiunta</span><span class="sxs-lookup"><span data-stu-id="9827c-1191">Added</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1192"><span id="Storage_Services"></span><span id="storage_services"></span><span id="STORAGE_SERVICES"></span>Servizi di archiviazione</span><span class="sxs-lookup"><span data-stu-id="9827c-1192"><span id="Storage_Services"></span><span id="storage_services"></span><span id="STORAGE_SERVICES"></span>Storage Services</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1193">Aggiunta</span><span class="sxs-lookup"><span data-stu-id="9827c-1193">Added</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1194"><span id="Failover_Cluster_Management_Tools"></span><span id="failover_cluster_management_tools"></span><span id="FAILOVER_CLUSTER_MANAGEMENT_TOOLS"></span>Strumenti di gestione del cluster di failover</span><span class="sxs-lookup"><span data-stu-id="9827c-1194"><span id="Failover_Cluster_Management_Tools"></span><span id="failover_cluster_management_tools"></span><span id="FAILOVER_CLUSTER_MANAGEMENT_TOOLS"></span>Failover Cluster Management Tools</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1195">Aggiunta</span><span class="sxs-lookup"><span data-stu-id="9827c-1195">Added</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1196"><span id="Active_Directory_Rights_Management_Services_Tools"></span><span id="active_directory_rights_management_services_tools"></span><span id="ACTIVE_DIRECTORY_RIGHTS_MANAGEMENT_SERVICES_TOOLS"></span>Strumenti di Active Directory Rights Management Services</span><span class="sxs-lookup"><span data-stu-id="9827c-1196"><span id="Active_Directory_Rights_Management_Services_Tools"></span><span id="active_directory_rights_management_services_tools"></span><span id="ACTIVE_DIRECTORY_RIGHTS_MANAGEMENT_SERVICES_TOOLS"></span>Active Directory Rights Management Services Tools</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1197">Aggiunta</span><span class="sxs-lookup"><span data-stu-id="9827c-1197">Added</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1198"><span id="Application_Initialization"></span><span id="application_initialization"></span><span id="APPLICATION_INITIALIZATION"></span>Inizializzazione dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="9827c-1198"><span id="Application_Initialization"></span><span id="application_initialization"></span><span id="APPLICATION_INITIALIZATION"></span>Application Initialization</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1199">Aggiunta</span><span class="sxs-lookup"><span data-stu-id="9827c-1199">Added</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1200"><span id="Centralized_SSL_Certificate_Support"></span><span id="centralized_ssl_certificate_support"></span><span id="CENTRALIZED_SSL_CERTIFICATE_SUPPORT"></span>Supporto certificato SSL centralizzato</span><span class="sxs-lookup"><span data-stu-id="9827c-1200"><span id="Centralized_SSL_Certificate_Support"></span><span id="centralized_ssl_certificate_support"></span><span id="CENTRALIZED_SSL_CERTIFICATE_SUPPORT"></span>Centralized SSL Certificate Support</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1201">Aggiunta</span><span class="sxs-lookup"><span data-stu-id="9827c-1201">Added</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1202"><span id="Claims-aware_Agent"></span><span id="claims-aware_agent"></span><span id="CLAIMS-AWARE_AGENT"></span>Agente in grado di riconoscere attestazioni</span><span class="sxs-lookup"><span data-stu-id="9827c-1202"><span id="Claims-aware_Agent"></span><span id="claims-aware_agent"></span><span id="CLAIMS-AWARE_AGENT"></span>Claims-aware Agent</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1203">Non più supportato</span><span class="sxs-lookup"><span data-stu-id="9827c-1203">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1204"><span id="Remote_Desktop_Session_Host_Tools"></span><span id="remote_desktop_session_host_tools"></span><span id="REMOTE_DESKTOP_SESSION_HOST_TOOLS"></span>Strumenti di host sessione Desktop remoto</span><span class="sxs-lookup"><span data-stu-id="9827c-1204"><span id="Remote_Desktop_Session_Host_Tools"></span><span id="remote_desktop_session_host_tools"></span><span id="REMOTE_DESKTOP_SESSION_HOST_TOOLS"></span>Remote Desktop Session Host Tools</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1205">Non più supportato</span><span class="sxs-lookup"><span data-stu-id="9827c-1205">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1206"><span id="WebSocket_Protocol"></span><span id="websocket_protocol"></span><span id="WEBSOCKET_PROTOCOL"></span>Protocollo WebSocket</span><span class="sxs-lookup"><span data-stu-id="9827c-1206"><span id="WebSocket_Protocol"></span><span id="websocket_protocol"></span><span id="WEBSOCKET_PROTOCOL"></span>WebSocket Protocol</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1207">non più supportato</span><span class="sxs-lookup"><span data-stu-id="9827c-1207">no longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1208"><span id="COM__Network_Access"></span><span id="com__network_access"></span><span id="COM__NETWORK_ACCESS"></span>Accesso alla rete COM+</span><span class="sxs-lookup"><span data-stu-id="9827c-1208"><span id="COM__Network_Access"></span><span id="com__network_access"></span><span id="COM__NETWORK_ACCESS"></span>COM+ Network Access</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1209">Non più supportato</span><span class="sxs-lookup"><span data-stu-id="9827c-1209">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1210"><span id="File_and_iSCSI_Services_name_change"></span><span id="file_and_iscsi_services_name_change"></span><span id="FILE_AND_ISCSI_SERVICES_NAME_CHANGE"></span>Modifica del nome dei servizi file e iSCSI</span><span class="sxs-lookup"><span data-stu-id="9827c-1210"><span id="File_and_iSCSI_Services_name_change"></span><span id="file_and_iscsi_services_name_change"></span><span id="FILE_AND_ISCSI_SERVICES_NAME_CHANGE"></span>File and iSCSI Services name change</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1211">Modificato in Servizi file</span><span class="sxs-lookup"><span data-stu-id="9827c-1211">Changed to File Services</span></span>

</dd> </dl>

### <a name="windows-server-2012"></a><span data-ttu-id="9827c-1212">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9827c-1212">Windows Server 2012</span></span>

<dl> <dt>

<span data-ttu-id="9827c-1213"><span id="User_Interfaces_and_Infrastructure"></span><span id="user_interfaces_and_infrastructure"></span><span id="USER_INTERFACES_AND_INFRASTRUCTURE"></span>Interfacce utente e infrastruttura</span><span class="sxs-lookup"><span data-stu-id="9827c-1213"><span id="User_Interfaces_and_Infrastructure"></span><span id="user_interfaces_and_infrastructure"></span><span id="USER_INTERFACES_AND_INFRASTRUCTURE"></span>User Interfaces and Infrastructure</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1214">Aggiunta</span><span class="sxs-lookup"><span data-stu-id="9827c-1214">Added</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1215"><span id="Server_for_NFS"></span><span id="server_for_nfs"></span><span id="SERVER_FOR_NFS"></span>Server per NFS</span><span class="sxs-lookup"><span data-stu-id="9827c-1215"><span id="Server_for_NFS"></span><span id="server_for_nfs"></span><span id="SERVER_FOR_NFS"></span>Server for NFS</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1216">Aggiunta</span><span class="sxs-lookup"><span data-stu-id="9827c-1216">Added</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1217"><span id="File_Server_VSS_Agent_Service"></span><span id="file_server_vss_agent_service"></span><span id="FILE_SERVER_VSS_AGENT_SERVICE"></span>Servizio file Server VSS Agent</span><span class="sxs-lookup"><span data-stu-id="9827c-1217"><span id="File_Server_VSS_Agent_Service"></span><span id="file_server_vss_agent_service"></span><span id="FILE_SERVER_VSS_AGENT_SERVICE"></span>File Server VSS Agent Service</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1218">Aggiunta</span><span class="sxs-lookup"><span data-stu-id="9827c-1218">Added</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1219"><span id="iSCSI_Target_Server"></span><span id="iscsi_target_server"></span><span id="ISCSI_TARGET_SERVER"></span>Server di destinazione iSCSI</span><span class="sxs-lookup"><span data-stu-id="9827c-1219"><span id="iSCSI_Target_Server"></span><span id="iscsi_target_server"></span><span id="ISCSI_TARGET_SERVER"></span>iSCSI Target Server</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1220">Aggiunta</span><span class="sxs-lookup"><span data-stu-id="9827c-1220">Added</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1221"><span id="Data_Deduplication"></span><span id="data_deduplication"></span><span id="DATA_DEDUPLICATION"></span>Deduplicazione dati</span><span class="sxs-lookup"><span data-stu-id="9827c-1221"><span id="Data_Deduplication"></span><span id="data_deduplication"></span><span id="DATA_DEDUPLICATION"></span>Data Deduplication</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1222">Aggiunta</span><span class="sxs-lookup"><span data-stu-id="9827c-1222">Added</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1223"><span id="Work_Folders"></span><span id="work_folders"></span><span id="WORK_FOLDERS"></span>Cartelle di lavoro</span><span class="sxs-lookup"><span data-stu-id="9827c-1223"><span id="Work_Folders"></span><span id="work_folders"></span><span id="WORK_FOLDERS"></span>Work Folders</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1224">Rimosso</span><span class="sxs-lookup"><span data-stu-id="9827c-1224">Removed</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1225"><span id="Core_Services"></span><span id="core_services"></span><span id="CORE_SERVICES"></span>Servizi di base</span><span class="sxs-lookup"><span data-stu-id="9827c-1225"><span id="Core_Services"></span><span id="core_services"></span><span id="CORE_SERVICES"></span>Core Services</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1226">Aggiunto solo per questa versione.</span><span class="sxs-lookup"><span data-stu-id="9827c-1226">Added for this version only.</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1227"><span id="Remote_Desktop_Virtual_Graphics"></span><span id="remote_desktop_virtual_graphics"></span><span id="REMOTE_DESKTOP_VIRTUAL_GRAPHICS"></span>Desktop remoto grafica virtuale</span><span class="sxs-lookup"><span data-stu-id="9827c-1227"><span id="Remote_Desktop_Virtual_Graphics"></span><span id="remote_desktop_virtual_graphics"></span><span id="REMOTE_DESKTOP_VIRTUAL_GRAPHICS"></span>Remote Desktop Virtual Graphics</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1228">Aggiunto solo per questa versione</span><span class="sxs-lookup"><span data-stu-id="9827c-1228">Added for this version only</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1229"><span id="Remote_Access"></span><span id="remote_access"></span><span id="REMOTE_ACCESS"></span>Accesso remoto</span><span class="sxs-lookup"><span data-stu-id="9827c-1229"><span id="Remote_Access"></span><span id="remote_access"></span><span id="REMOTE_ACCESS"></span>Remote Access</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1230">Aggiunta</span><span class="sxs-lookup"><span data-stu-id="9827c-1230">Added</span></span>

</dd> </dl>

### <a name="windows-server-2008-r2"></a><span data-ttu-id="9827c-1231">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9827c-1231">Windows Server 2008 R2</span></span>

<dl> <dt>

<span data-ttu-id="9827c-1232"><span id="UDDI_Services"></span><span id="uddi_services"></span><span id="UDDI_SERVICES"></span>Servizi UDDI</span><span class="sxs-lookup"><span data-stu-id="9827c-1232"><span id="UDDI_Services"></span><span id="uddi_services"></span><span id="UDDI_SERVICES"></span>UDDI Services</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1233">Non più supportato</span><span class="sxs-lookup"><span data-stu-id="9827c-1233">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1234"><span id="Windows_System_Resource_Manager"></span><span id="windows_system_resource_manager"></span><span id="WINDOWS_SYSTEM_RESOURCE_MANAGER"></span>Gestione risorse di sistema Windows</span><span class="sxs-lookup"><span data-stu-id="9827c-1234"><span id="Windows_System_Resource_Manager"></span><span id="windows_system_resource_manager"></span><span id="WINDOWS_SYSTEM_RESOURCE_MANAGER"></span>Windows System Resource Manager</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1235">Non più supportato</span><span class="sxs-lookup"><span data-stu-id="9827c-1235">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1236"><span id="Removable_Storage_Manager"></span><span id="removable_storage_manager"></span><span id="REMOVABLE_STORAGE_MANAGER"></span>Gestione archivi rimovibili</span><span class="sxs-lookup"><span data-stu-id="9827c-1236"><span id="Removable_Storage_Manager"></span><span id="removable_storage_manager"></span><span id="REMOVABLE_STORAGE_MANAGER"></span>Removable Storage Manager</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1237">Non più supportato</span><span class="sxs-lookup"><span data-stu-id="9827c-1237">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1238"><span id="Windows_PowerShell"></span><span id="windows_powershell"></span><span id="WINDOWS_POWERSHELL"></span>Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="9827c-1238"><span id="Windows_PowerShell"></span><span id="windows_powershell"></span><span id="WINDOWS_POWERSHELL"></span>Windows PowerShell</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1239">Non più supportato</span><span class="sxs-lookup"><span data-stu-id="9827c-1239">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1240"><span id="Ink_and_Handwriting_Services"></span><span id="ink_and_handwriting_services"></span><span id="INK_AND_HANDWRITING_SERVICES"></span>Servizi di riconoscimento della grafia</span><span class="sxs-lookup"><span data-stu-id="9827c-1240"><span id="Ink_and_Handwriting_Services"></span><span id="ink_and_handwriting_services"></span><span id="INK_AND_HANDWRITING_SERVICES"></span>Ink and Handwriting Services</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1241">Aggiunta</span><span class="sxs-lookup"><span data-stu-id="9827c-1241">Added</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1242"><span id="WinRM_IIS_Extension"></span><span id="winrm_iis_extension"></span><span id="WINRM_IIS_EXTENSION"></span>Estensione IIS WinRM</span><span class="sxs-lookup"><span data-stu-id="9827c-1242"><span id="WinRM_IIS_Extension"></span><span id="winrm_iis_extension"></span><span id="WINRM_IIS_EXTENSION"></span>WinRM IIS Extension</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1243">Aggiunta</span><span class="sxs-lookup"><span data-stu-id="9827c-1243">Added</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1244"><span id="DirectAccess_Management_Console"></span><span id="directaccess_management_console"></span><span id="DIRECTACCESS_MANAGEMENT_CONSOLE"></span>Console di Gestione DirectAccess</span><span class="sxs-lookup"><span data-stu-id="9827c-1244"><span id="DirectAccess_Management_Console"></span><span id="directaccess_management_console"></span><span id="DIRECTACCESS_MANAGEMENT_CONSOLE"></span>DirectAccess Management Console</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1245">Aggiunta</span><span class="sxs-lookup"><span data-stu-id="9827c-1245">Added</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1246"><span id="Background_Intelligent_Transfer_Service__BITS_"></span><span id="background_intelligent_transfer_service__bits_"></span><span id="BACKGROUND_INTELLIGENT_TRANSFER_SERVICE__BITS_"></span>Servizio trasferimento intelligente in background (BITS)</span><span class="sxs-lookup"><span data-stu-id="9827c-1246"><span id="Background_Intelligent_Transfer_Service__BITS_"></span><span id="background_intelligent_transfer_service__bits_"></span><span id="BACKGROUND_INTELLIGENT_TRANSFER_SERVICE__BITS_"></span>Background Intelligent Transfer Service (BITS)</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1247">Aggiunta</span><span class="sxs-lookup"><span data-stu-id="9827c-1247">Added</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1248"><span id="XPS_Viewer"></span><span id="xps_viewer"></span><span id="XPS_VIEWER"></span>Visualizzatore XPS</span><span class="sxs-lookup"><span data-stu-id="9827c-1248"><span id="XPS_Viewer"></span><span id="xps_viewer"></span><span id="XPS_VIEWER"></span>XPS Viewer</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1249">Aggiunta</span><span class="sxs-lookup"><span data-stu-id="9827c-1249">Added</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1250"><span id="Windows_Biometric_Framework"></span><span id="windows_biometric_framework"></span><span id="WINDOWS_BIOMETRIC_FRAMEWORK"></span>Windows Biometric Framework</span><span class="sxs-lookup"><span data-stu-id="9827c-1250"><span id="Windows_Biometric_Framework"></span><span id="windows_biometric_framework"></span><span id="WINDOWS_BIOMETRIC_FRAMEWORK"></span>Windows Biometric Framework</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1251">Aggiunta</span><span class="sxs-lookup"><span data-stu-id="9827c-1251">Added</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1252"><span id="WoW64_Support"></span><span id="wow64_support"></span><span id="WOW64_SUPPORT"></span>Supporto di WoW64</span><span class="sxs-lookup"><span data-stu-id="9827c-1252"><span id="WoW64_Support"></span><span id="wow64_support"></span><span id="WOW64_SUPPORT"></span>WoW64 Support</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1253">Aggiunta</span><span class="sxs-lookup"><span data-stu-id="9827c-1253">Added</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1254"><span id="Windows_PowerShell_Integrated_Scripting_Environment__ISE_"></span><span id="windows_powershell_integrated_scripting_environment__ise_"></span><span id="WINDOWS_POWERSHELL_INTEGRATED_SCRIPTING_ENVIRONMENT__ISE_"></span>Windows PowerShell Integrated Scripting Environment (ISE)</span><span class="sxs-lookup"><span data-stu-id="9827c-1254"><span id="Windows_PowerShell_Integrated_Scripting_Environment__ISE_"></span><span id="windows_powershell_integrated_scripting_environment__ise_"></span><span id="WINDOWS_POWERSHELL_INTEGRATED_SCRIPTING_ENVIRONMENT__ISE_"></span>Windows PowerShell Integrated Scripting Environment (ISE)</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1255">Aggiunta</span><span class="sxs-lookup"><span data-stu-id="9827c-1255">Added</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1256"><span id="File_Replication_Service"></span><span id="file_replication_service"></span><span id="FILE_REPLICATION_SERVICE"></span>Servizio Replica file</span><span class="sxs-lookup"><span data-stu-id="9827c-1256"><span id="File_Replication_Service"></span><span id="file_replication_service"></span><span id="FILE_REPLICATION_SERVICE"></span>File Replication Service</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1257">Non più supportato</span><span class="sxs-lookup"><span data-stu-id="9827c-1257">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1258"><span id="BranchCache_for_Network_Files"></span><span id="branchcache_for_network_files"></span><span id="BRANCHCACHE_FOR_NETWORK_FILES"></span>BranchCache per file di rete</span><span class="sxs-lookup"><span data-stu-id="9827c-1258"><span id="BranchCache_for_Network_Files"></span><span id="branchcache_for_network_files"></span><span id="BRANCHCACHE_FOR_NETWORK_FILES"></span>BranchCache for Network Files</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1259">Aggiunta</span><span class="sxs-lookup"><span data-stu-id="9827c-1259">Added</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1260"><span id="Work_Folders"></span><span id="work_folders"></span><span id="WORK_FOLDERS"></span>Cartelle di lavoro</span><span class="sxs-lookup"><span data-stu-id="9827c-1260"><span id="Work_Folders"></span><span id="work_folders"></span><span id="WORK_FOLDERS"></span>Work Folders</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1261">Aggiunta</span><span class="sxs-lookup"><span data-stu-id="9827c-1261">Added</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1262"><span id="Distributed_Scan_Server"></span><span id="distributed_scan_server"></span><span id="DISTRIBUTED_SCAN_SERVER"></span>Server Digitalizzazione distribuita</span><span class="sxs-lookup"><span data-stu-id="9827c-1262"><span id="Distributed_Scan_Server"></span><span id="distributed_scan_server"></span><span id="DISTRIBUTED_SCAN_SERVER"></span>Distributed Scan Server</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1263">Aggiunta</span><span class="sxs-lookup"><span data-stu-id="9827c-1263">Added</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1264"><span id="FTP_Publishing_Service"></span><span id="ftp_publishing_service"></span><span id="FTP_PUBLISHING_SERVICE"></span>Servizio di pubblicazione FTP</span><span class="sxs-lookup"><span data-stu-id="9827c-1264"><span id="FTP_Publishing_Service"></span><span id="ftp_publishing_service"></span><span id="FTP_PUBLISHING_SERVICE"></span>FTP Publishing Service</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1265">Non più supportato</span><span class="sxs-lookup"><span data-stu-id="9827c-1265">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1266"><span id="FTP_Management_Console"></span><span id="ftp_management_console"></span><span id="FTP_MANAGEMENT_CONSOLE"></span>Console di gestione FTP</span><span class="sxs-lookup"><span data-stu-id="9827c-1266"><span id="FTP_Management_Console"></span><span id="ftp_management_console"></span><span id="FTP_MANAGEMENT_CONSOLE"></span>FTP Management Console</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1267">Non più supportato</span><span class="sxs-lookup"><span data-stu-id="9827c-1267">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1268"><span id="FTP_Service"></span><span id="ftp_service"></span><span id="FTP_SERVICE"></span>Servizio FTP</span><span class="sxs-lookup"><span data-stu-id="9827c-1268"><span id="FTP_Service"></span><span id="ftp_service"></span><span id="FTP_SERVICE"></span>FTP Service</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1269">Aggiunta</span><span class="sxs-lookup"><span data-stu-id="9827c-1269">Added</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1270"><span id="FTP_Extensibility"></span><span id="ftp_extensibility"></span><span id="FTP_EXTENSIBILITY"></span>Estendibilità FTP</span><span class="sxs-lookup"><span data-stu-id="9827c-1270"><span id="FTP_Extensibility"></span><span id="ftp_extensibility"></span><span id="FTP_EXTENSIBILITY"></span>FTP Extensibility</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1271">Aggiunta</span><span class="sxs-lookup"><span data-stu-id="9827c-1271">Added</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1272"><span id="IIS_Hostable_Web_Core"></span><span id="iis_hostable_web_core"></span><span id="IIS_HOSTABLE_WEB_CORE"></span>Web Core ospitabile in IIS</span><span class="sxs-lookup"><span data-stu-id="9827c-1272"><span id="IIS_Hostable_Web_Core"></span><span id="iis_hostable_web_core"></span><span id="IIS_HOSTABLE_WEB_CORE"></span>IIS Hostable Web Core</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="9827c-1273"><span id="Windows_2000_Client_Support"></span><span id="windows_2000_client_support"></span><span id="WINDOWS_2000_CLIENT_SUPPORT"></span>Supporto client Windows 2000</span><span class="sxs-lookup"><span data-stu-id="9827c-1273"><span id="Windows_2000_Client_Support"></span><span id="windows_2000_client_support"></span><span id="WINDOWS_2000_CLIENT_SUPPORT"></span>Windows 2000 Client Support</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1274">Non più supportato</span><span class="sxs-lookup"><span data-stu-id="9827c-1274">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1275"><span id="Certificate_Enrollment_Web_Service"></span><span id="certificate_enrollment_web_service"></span><span id="CERTIFICATE_ENROLLMENT_WEB_SERVICE"></span>Servizio Web di registrazione certificati</span><span class="sxs-lookup"><span data-stu-id="9827c-1275"><span id="Certificate_Enrollment_Web_Service"></span><span id="certificate_enrollment_web_service"></span><span id="CERTIFICATE_ENROLLMENT_WEB_SERVICE"></span>Certificate Enrollment Web Service</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1276">Aggiunta</span><span class="sxs-lookup"><span data-stu-id="9827c-1276">Added</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1277"><span id="Certificate_Enrollment_Policy_Web_Service"></span><span id="certificate_enrollment_policy_web_service"></span><span id="CERTIFICATE_ENROLLMENT_POLICY_WEB_SERVICE"></span>Servizio Web di informazioni sulle registrazioni di certificati</span><span class="sxs-lookup"><span data-stu-id="9827c-1277"><span id="Certificate_Enrollment_Policy_Web_Service"></span><span id="certificate_enrollment_policy_web_service"></span><span id="CERTIFICATE_ENROLLMENT_POLICY_WEB_SERVICE"></span>Certificate Enrollment Policy Web Service</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1278">Aggiunta</span><span class="sxs-lookup"><span data-stu-id="9827c-1278">Added</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1279"><span id="UDDI_Services_Web_Application"></span><span id="uddi_services_web_application"></span><span id="UDDI_SERVICES_WEB_APPLICATION"></span>Applicazione Web Servizi UDDI</span><span class="sxs-lookup"><span data-stu-id="9827c-1279"><span id="UDDI_Services_Web_Application"></span><span id="uddi_services_web_application"></span><span id="UDDI_SERVICES_WEB_APPLICATION"></span>UDDI Services Web Application</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1280">Non più supportato</span><span class="sxs-lookup"><span data-stu-id="9827c-1280">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1281"><span id="UDDI_Services_Database"></span><span id="uddi_services_database"></span><span id="UDDI_SERVICES_DATABASE"></span>Database dei servizi UDDI</span><span class="sxs-lookup"><span data-stu-id="9827c-1281"><span id="UDDI_Services_Database"></span><span id="uddi_services_database"></span><span id="UDDI_SERVICES_DATABASE"></span>UDDI Services Database</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1282">Non più supportato</span><span class="sxs-lookup"><span data-stu-id="9827c-1282">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1283"><span id="Application_Server_Extensions_for_.NET_4.0"></span><span id="application_server_extensions_for_.net_4.0"></span><span id="APPLICATION_SERVER_EXTENSIONS_FOR_.NET_4.0"></span>Estensioni del server applicazioni per .NET 4,0</span><span class="sxs-lookup"><span data-stu-id="9827c-1283"><span id="Application_Server_Extensions_for_.NET_4.0"></span><span id="application_server_extensions_for_.net_4.0"></span><span id="APPLICATION_SERVER_EXTENSIONS_FOR_.NET_4.0"></span>Application Server Extensions for .NET 4.0</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1284">Aggiunta</span><span class="sxs-lookup"><span data-stu-id="9827c-1284">Added</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1285"><span id="UDDI_Services_Tools"></span><span id="uddi_services_tools"></span><span id="UDDI_SERVICES_TOOLS"></span>Strumenti per Servizi UDDI</span><span class="sxs-lookup"><span data-stu-id="9827c-1285"><span id="UDDI_Services_Tools"></span><span id="uddi_services_tools"></span><span id="UDDI_SERVICES_TOOLS"></span>UDDI Services Tools</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1286">Non più supportato</span><span class="sxs-lookup"><span data-stu-id="9827c-1286">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1287"><span id="BitLocker_Drive_Encryption_Administration_Utilities"></span><span id="bitlocker_drive_encryption_administration_utilities"></span><span id="BITLOCKER_DRIVE_ENCRYPTION_ADMINISTRATION_UTILITIES"></span>Utilità di amministrazione di Crittografia unità BitLocker</span><span class="sxs-lookup"><span data-stu-id="9827c-1287"><span id="BitLocker_Drive_Encryption_Administration_Utilities"></span><span id="bitlocker_drive_encryption_administration_utilities"></span><span id="BITLOCKER_DRIVE_ENCRYPTION_ADMINISTRATION_UTILITIES"></span>BitLocker Drive Encryption Administration Utilities</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1288">Aggiunta</span><span class="sxs-lookup"><span data-stu-id="9827c-1288">Added</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1289"><span id="AD_DS_and_AD_LDS_Tools"></span><span id="ad_ds_and_ad_lds_tools"></span><span id="AD_DS_AND_AD_LDS_TOOLS"></span>Strumenti per servizi di dominio Active Directory e AD LDS</span><span class="sxs-lookup"><span data-stu-id="9827c-1289"><span id="AD_DS_and_AD_LDS_Tools"></span><span id="ad_ds_and_ad_lds_tools"></span><span id="AD_DS_AND_AD_LDS_TOOLS"></span>AD DS and AD LDS Tools</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1290">Non più supportato</span><span class="sxs-lookup"><span data-stu-id="9827c-1290">No longer supported</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1291"><span id="AD_DS_and_AD_LDS_Tools"></span><span id="ad_ds_and_ad_lds_tools"></span><span id="AD_DS_AND_AD_LDS_TOOLS"></span>Strumenti per servizi di dominio Active Directory e AD LDS</span><span class="sxs-lookup"><span data-stu-id="9827c-1291"><span id="AD_DS_and_AD_LDS_Tools"></span><span id="ad_ds_and_ad_lds_tools"></span><span id="AD_DS_AND_AD_LDS_TOOLS"></span>AD DS and AD LDS Tools</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1292">Aggiunta</span><span class="sxs-lookup"><span data-stu-id="9827c-1292">Added</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1293"><span id="Active_Directory_Administrative_Center"></span><span id="active_directory_administrative_center"></span><span id="ACTIVE_DIRECTORY_ADMINISTRATIVE_CENTER"></span>Centro di amministrazione di Active Directory</span><span class="sxs-lookup"><span data-stu-id="9827c-1293"><span id="Active_Directory_Administrative_Center"></span><span id="active_directory_administrative_center"></span><span id="ACTIVE_DIRECTORY_ADMINISTRATIVE_CENTER"></span>Active Directory Administrative Center</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1294">Aggiunta</span><span class="sxs-lookup"><span data-stu-id="9827c-1294">Added</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1295"><span id="Active_Directory_module_for___________Windows_PowerShell"></span><span id="active_directory_module_for___________windows_powershell"></span><span id="ACTIVE_DIRECTORY_MODULE_FOR___________WINDOWS_POWERSHELL"></span>Modulo Active Directory per Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="9827c-1295"><span id="Active_Directory_module_for___________Windows_PowerShell"></span><span id="active_directory_module_for___________windows_powershell"></span><span id="ACTIVE_DIRECTORY_MODULE_FOR___________WINDOWS_POWERSHELL"></span>Active Directory module for Windows PowerShell</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1296">Aggiunta</span><span class="sxs-lookup"><span data-stu-id="9827c-1296">Added</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1297"><span id="Remote_Desktop_Connection_Broker_Tools"></span><span id="remote_desktop_connection_broker_tools"></span><span id="REMOTE_DESKTOP_CONNECTION_BROKER_TOOLS"></span>Strumenti di Connessione Desktop remoto broker</span><span class="sxs-lookup"><span data-stu-id="9827c-1297"><span id="Remote_Desktop_Connection_Broker_Tools"></span><span id="remote_desktop_connection_broker_tools"></span><span id="REMOTE_DESKTOP_CONNECTION_BROKER_TOOLS"></span>Remote Desktop Connection Broker Tools</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1298">Aggiunta</span><span class="sxs-lookup"><span data-stu-id="9827c-1298">Added</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1299"><span id="WoW64"></span><span id="wow64"></span><span id="WOW64"></span>WoW64</span><span class="sxs-lookup"><span data-stu-id="9827c-1299"><span id="WoW64"></span><span id="wow64"></span><span id="WOW64"></span>WoW64</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1300">Aggiunta</span><span class="sxs-lookup"><span data-stu-id="9827c-1300">Added</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1301"><span id="WoW64_for_.NET_Framework_2.0_and_Windows_PowerShell"></span><span id="wow64_for_.net_framework_2.0_and_windows_powershell"></span><span id="WOW64_FOR_.NET_FRAMEWORK_2.0_AND_WINDOWS_POWERSHELL"></span>WoW64 per .NET Framework 2,0 e Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="9827c-1301"><span id="WoW64_for_.NET_Framework_2.0_and_Windows_PowerShell"></span><span id="wow64_for_.net_framework_2.0_and_windows_powershell"></span><span id="WOW64_FOR_.NET_FRAMEWORK_2.0_AND_WINDOWS_POWERSHELL"></span>WoW64 for .NET Framework 2.0 and Windows PowerShell</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1302">Aggiunta</span><span class="sxs-lookup"><span data-stu-id="9827c-1302">Added</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1303"><span id="WoW64_for_.NET_Framework_2.0"></span><span id="wow64_for_.net_framework_2.0"></span><span id="WOW64_FOR_.NET_FRAMEWORK_2.0"></span>WoW64 per .NET Framework 2,0</span><span class="sxs-lookup"><span data-stu-id="9827c-1303"><span id="WoW64_for_.NET_Framework_2.0"></span><span id="wow64_for_.net_framework_2.0"></span><span id="WOW64_FOR_.NET_FRAMEWORK_2.0"></span>WoW64 for .NET Framework 2.0</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1304">Aggiunta</span><span class="sxs-lookup"><span data-stu-id="9827c-1304">Added</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1305"><span id="WoW64_for___________"></span><span id="wow64_for___________"></span><span id="WOW64_FOR___________"></span>WoW64 per PowerShell</span><span class="sxs-lookup"><span data-stu-id="9827c-1305"><span id="WoW64_for___________"></span><span id="wow64_for___________"></span><span id="WOW64_FOR___________"></span>WoW64 for PowerShell</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1306">Aggiunta</span><span class="sxs-lookup"><span data-stu-id="9827c-1306">Added</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1307"><span id="WoW64_for_.NET_Framework_3.0_and_3.5"></span><span id="wow64_for_.net_framework_3.0_and_3.5"></span><span id="WOW64_FOR_.NET_FRAMEWORK_3.0_AND_3.5"></span>WoW64 per .NET Framework 3,0 e 3,5</span><span class="sxs-lookup"><span data-stu-id="9827c-1307"><span id="WoW64_for_.NET_Framework_3.0_and_3.5"></span><span id="wow64_for_.net_framework_3.0_and_3.5"></span><span id="WOW64_FOR_.NET_FRAMEWORK_3.0_AND_3.5"></span>WoW64 for .NET Framework 3.0 and 3.5</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1308">Aggiunta</span><span class="sxs-lookup"><span data-stu-id="9827c-1308">Added</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1309"><span id="WoW64_for_Print_Services"></span><span id="wow64_for_print_services"></span><span id="WOW64_FOR_PRINT_SERVICES"></span>WoW64 per servizi di stampa</span><span class="sxs-lookup"><span data-stu-id="9827c-1309"><span id="WoW64_for_Print_Services"></span><span id="wow64_for_print_services"></span><span id="WOW64_FOR_PRINT_SERVICES"></span>WoW64 for Print Services</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1310">Aggiunta</span><span class="sxs-lookup"><span data-stu-id="9827c-1310">Added</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1311"><span id="WoW64_for_Failover_Clustering"></span><span id="wow64_for_failover_clustering"></span><span id="WOW64_FOR_FAILOVER_CLUSTERING"></span>WoW64 per il clustering di failover</span><span class="sxs-lookup"><span data-stu-id="9827c-1311"><span id="WoW64_for_Failover_Clustering"></span><span id="wow64_for_failover_clustering"></span><span id="WOW64_FOR_FAILOVER_CLUSTERING"></span>WoW64 for Failover Clustering</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1312">Aggiunta</span><span class="sxs-lookup"><span data-stu-id="9827c-1312">Added</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1313"><span id="WoW64_for_Input_Method_Editor"></span><span id="wow64_for_input_method_editor"></span><span id="WOW64_FOR_INPUT_METHOD_EDITOR"></span>WoW64 per input Method Editor</span><span class="sxs-lookup"><span data-stu-id="9827c-1313"><span id="WoW64_for_Input_Method_Editor"></span><span id="wow64_for_input_method_editor"></span><span id="WOW64_FOR_INPUT_METHOD_EDITOR"></span>WoW64 for Input Method Editor</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1314">Aggiunta</span><span class="sxs-lookup"><span data-stu-id="9827c-1314">Added</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1315"><span id="WoW64_for_Subsystem_for_UNIX-based_Applications"></span><span id="wow64_for_subsystem_for_unix-based_applications"></span><span id="WOW64_FOR_SUBSYSTEM_FOR_UNIX-BASED_APPLICATIONS"></span>WoW64 per sottosistema per applicazioni basate su UNIX</span><span class="sxs-lookup"><span data-stu-id="9827c-1315"><span id="WoW64_for_Subsystem_for_UNIX-based_Applications"></span><span id="wow64_for_subsystem_for_unix-based_applications"></span><span id="WOW64_FOR_SUBSYSTEM_FOR_UNIX-BASED_APPLICATIONS"></span>WoW64 for Subsystem for UNIX-based Applications</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1316">Aggiunta</span><span class="sxs-lookup"><span data-stu-id="9827c-1316">Added</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1317"><span id="BitLocker_Recovery_Password_Viewer"></span><span id="bitlocker_recovery_password_viewer"></span><span id="BITLOCKER_RECOVERY_PASSWORD_VIEWER"></span>Visualizzatore password di ripristino BitLocker</span><span class="sxs-lookup"><span data-stu-id="9827c-1317"><span id="BitLocker_Recovery_Password_Viewer"></span><span id="bitlocker_recovery_password_viewer"></span><span id="BITLOCKER_RECOVERY_PASSWORD_VIEWER"></span>BitLocker Recovery Password Viewer</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1318">Aggiunta</span><span class="sxs-lookup"><span data-stu-id="9827c-1318">Added</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1319"><span id="Print_and_Document_Services_name_change"></span><span id="print_and_document_services_name_change"></span><span id="PRINT_AND_DOCUMENT_SERVICES_NAME_CHANGE"></span>Modifica nome Servizi di stampa e digitalizzazione</span><span class="sxs-lookup"><span data-stu-id="9827c-1319"><span id="Print_and_Document_Services_name_change"></span><span id="print_and_document_services_name_change"></span><span id="PRINT_AND_DOCUMENT_SERVICES_NAME_CHANGE"></span>Print and Document Services name change</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1320">Servizi di stampa denominati per questa versione</span><span class="sxs-lookup"><span data-stu-id="9827c-1320">named Print Services for this release</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1321"><span id="Remote_Desktop_Services_name_change"></span><span id="remote_desktop_services_name_change"></span><span id="REMOTE_DESKTOP_SERVICES_NAME_CHANGE"></span>Modifica nome Servizi Desktop remoto</span><span class="sxs-lookup"><span data-stu-id="9827c-1321"><span id="Remote_Desktop_Services_name_change"></span><span id="remote_desktop_services_name_change"></span><span id="REMOTE_DESKTOP_SERVICES_NAME_CHANGE"></span>Remote Desktop Services name change</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1322">Servizi terminal denominati in questa versione</span><span class="sxs-lookup"><span data-stu-id="9827c-1322">named Terminal Services in this release</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1323"><span id=".NET_Framework_3.5.1_Features_name_change"></span><span id=".net_framework_3.5.1_features_name_change"></span><span id=".NET_FRAMEWORK_3.5.1_FEATURES_NAME_CHANGE"></span>Modifica del nome delle funzionalità di .NET Framework 3.5.1</span><span class="sxs-lookup"><span data-stu-id="9827c-1323"><span id=".NET_Framework_3.5.1_Features_name_change"></span><span id=".net_framework_3.5.1_features_name_change"></span><span id=".NET_FRAMEWORK_3.5.1_FEATURES_NAME_CHANGE"></span>.NET Framework 3.5.1 Features name change</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1324">Funzionalità denominate .NET Framework 3,0 in questa versione</span><span class="sxs-lookup"><span data-stu-id="9827c-1324">Named .NET Framework 3.0 Features in this release</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1325"><span id="Remote_Desktop_Session_Host_name_change"></span><span id="remote_desktop_session_host_name_change"></span><span id="REMOTE_DESKTOP_SESSION_HOST_NAME_CHANGE"></span>Modifica nome host sessione Desktop remoto</span><span class="sxs-lookup"><span data-stu-id="9827c-1325"><span id="Remote_Desktop_Session_Host_name_change"></span><span id="remote_desktop_session_host_name_change"></span><span id="REMOTE_DESKTOP_SESSION_HOST_NAME_CHANGE"></span>Remote Desktop Session Host name change</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1326">Terminal Server denominati in questa versione</span><span class="sxs-lookup"><span data-stu-id="9827c-1326">Named Terminal Server in this release</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1327"><span id="Remote_Desktop_Licensing_name_change"></span><span id="remote_desktop_licensing_name_change"></span><span id="REMOTE_DESKTOP_LICENSING_NAME_CHANGE"></span>Modifica nome licenza Desktop remoto</span><span class="sxs-lookup"><span data-stu-id="9827c-1327"><span id="Remote_Desktop_Licensing_name_change"></span><span id="remote_desktop_licensing_name_change"></span><span id="REMOTE_DESKTOP_LICENSING_NAME_CHANGE"></span>Remote Desktop Licensing name change</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1328">Licenze TS denominate in questa versione</span><span class="sxs-lookup"><span data-stu-id="9827c-1328">Named TS Licensing in this release</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1329"><span id="Remote_Desktop_Gateway_name_change"></span><span id="remote_desktop_gateway_name_change"></span><span id="REMOTE_DESKTOP_GATEWAY_NAME_CHANGE"></span>Modifica del nome del Gateway Desktop remoto</span><span class="sxs-lookup"><span data-stu-id="9827c-1329"><span id="Remote_Desktop_Gateway_name_change"></span><span id="remote_desktop_gateway_name_change"></span><span id="REMOTE_DESKTOP_GATEWAY_NAME_CHANGE"></span>Remote Desktop Gateway name change</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1330">Gateway di Servizi terminal denominato in questa versione</span><span class="sxs-lookup"><span data-stu-id="9827c-1330">Named TS Gateway in this release</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1331"><span id="Remote_Desktop_Connection_Broker_name_change"></span><span id="remote_desktop_connection_broker_name_change"></span><span id="REMOTE_DESKTOP_CONNECTION_BROKER_NAME_CHANGE"></span>Modifica del nome del broker Connessione Desktop remoto</span><span class="sxs-lookup"><span data-stu-id="9827c-1331"><span id="Remote_Desktop_Connection_Broker_name_change"></span><span id="remote_desktop_connection_broker_name_change"></span><span id="REMOTE_DESKTOP_CONNECTION_BROKER_NAME_CHANGE"></span>Remote Desktop Connection Broker name change</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1332">Gestore sessioni Servizi terminal denominato in questa versione</span><span class="sxs-lookup"><span data-stu-id="9827c-1332">Named TS Session Broker in this release</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1333"><span id="Remote_Desktop_Web_Access_name_change"></span><span id="remote_desktop_web_access_name_change"></span><span id="REMOTE_DESKTOP_WEB_ACCESS_NAME_CHANGE"></span>Desktop remoto Accesso Web modificare il nome</span><span class="sxs-lookup"><span data-stu-id="9827c-1333"><span id="Remote_Desktop_Web_Access_name_change"></span><span id="remote_desktop_web_access_name_change"></span><span id="REMOTE_DESKTOP_WEB_ACCESS_NAME_CHANGE"></span>Remote Desktop Web Access name change</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1334">Accesso Web TS denominato in questa versione</span><span class="sxs-lookup"><span data-stu-id="9827c-1334">Named TS Web Access in this release</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1335"><span id=".NET_Framework_3.5.1_name_change"></span><span id=".net_framework_3.5.1_name_change"></span><span id=".NET_FRAMEWORK_3.5.1_NAME_CHANGE"></span>Modifica nome .NET Framework 3.5.1</span><span class="sxs-lookup"><span data-stu-id="9827c-1335"><span id=".NET_Framework_3.5.1_name_change"></span><span id=".net_framework_3.5.1_name_change"></span><span id=".NET_FRAMEWORK_3.5.1_NAME_CHANGE"></span>.NET Framework 3.5.1 name change</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1336">(220) funzionalità denominate NET FX 3,0 in questa versione</span><span class="sxs-lookup"><span data-stu-id="9827c-1336">(220) Named Net FX 3.0 Features in this release</span></span>

<span data-ttu-id="9827c-1337">(230) denominato server applicazioni di base in questa versione</span><span class="sxs-lookup"><span data-stu-id="9827c-1337">(230) Named Application Server Core in this release</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1338"><span id="AD_DS_Tools_name_change"></span><span id="ad_ds_tools_name_change"></span><span id="AD_DS_TOOLS_NAME_CHANGE"></span>Modifica nome strumenti di servizi di dominio Active Directory</span><span class="sxs-lookup"><span data-stu-id="9827c-1338"><span id="AD_DS_Tools_name_change"></span><span id="ad_ds_tools_name_change"></span><span id="AD_DS_TOOLS_NAME_CHANGE"></span>AD DS Tools name change</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1339">Strumenti di Active Directory Domain Services denominati in questa versione</span><span class="sxs-lookup"><span data-stu-id="9827c-1339">Named Active Directory Domain Services Tools in this release</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1340"><span id="AD_LDS_Snap-Ins_and_Command-Line_Tools_name_change"></span><span id="ad_lds_snap-ins_and_command-line_tools_name_change"></span><span id="AD_LDS_SNAP-INS_AND_COMMAND-LINE_TOOLS_NAME_CHANGE"></span>AD LDS Snap-Ins e la modifica del nome degli strumenti Command-Line</span><span class="sxs-lookup"><span data-stu-id="9827c-1340"><span id="AD_LDS_Snap-Ins_and_Command-Line_Tools_name_change"></span><span id="ad_lds_snap-ins_and_command-line_tools_name_change"></span><span id="AD_LDS_SNAP-INS_AND_COMMAND-LINE_TOOLS_NAME_CHANGE"></span>AD LDS Snap-Ins and Command-Line Tools name change</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1341">Strumenti di Active Directory Lightweight Directory Services denominati in questa versione</span><span class="sxs-lookup"><span data-stu-id="9827c-1341">Named Active Directory Lightweight Directory Services Tools in this release</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1342"><span id="Print_and_Document_Services_Tools_name_change"></span><span id="print_and_document_services_tools_name_change"></span><span id="PRINT_AND_DOCUMENT_SERVICES_TOOLS_NAME_CHANGE"></span>Modifica del nome di strumenti di Servizi di stampa e digitalizzazione</span><span class="sxs-lookup"><span data-stu-id="9827c-1342"><span id="Print_and_Document_Services_Tools_name_change"></span><span id="print_and_document_services_tools_name_change"></span><span id="PRINT_AND_DOCUMENT_SERVICES_TOOLS_NAME_CHANGE"></span>Print and Document Services Tools name change</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1343">Strumenti per servizi di stampa denominati in questa versione</span><span class="sxs-lookup"><span data-stu-id="9827c-1343">Named Print Services Tools in this release</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1344"><span id="Remote_Desktop_Services_Tools_name_change"></span><span id="remote_desktop_services_tools_name_change"></span><span id="REMOTE_DESKTOP_SERVICES_TOOLS_NAME_CHANGE"></span>Modifica del nome di strumenti di Servizi Desktop remoto</span><span class="sxs-lookup"><span data-stu-id="9827c-1344"><span id="Remote_Desktop_Services_Tools_name_change"></span><span id="remote_desktop_services_tools_name_change"></span><span id="REMOTE_DESKTOP_SERVICES_TOOLS_NAME_CHANGE"></span>Remote Desktop Services Tools name change</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1345">Strumenti di Servizi terminal denominati in questa versione</span><span class="sxs-lookup"><span data-stu-id="9827c-1345">Named Terminal Services Tools in this release</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1346"><span id="Remote_Desktop_Session_Host_Tools_name_change"></span><span id="remote_desktop_session_host_tools_name_change"></span><span id="REMOTE_DESKTOP_SESSION_HOST_TOOLS_NAME_CHANGE"></span>Modifica del nome di strumenti di host sessione Desktop remoto</span><span class="sxs-lookup"><span data-stu-id="9827c-1346"><span id="Remote_Desktop_Session_Host_Tools_name_change"></span><span id="remote_desktop_session_host_tools_name_change"></span><span id="REMOTE_DESKTOP_SESSION_HOST_TOOLS_NAME_CHANGE"></span>Remote Desktop Session Host Tools name change</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1347">Strumenti di Terminal Server denominati in questa versione</span><span class="sxs-lookup"><span data-stu-id="9827c-1347">Named Terminal Server Tools in this release</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1348"><span id="Remote_Desktop_Gateway_Tools_name_change"></span><span id="remote_desktop_gateway_tools_name_change"></span><span id="REMOTE_DESKTOP_GATEWAY_TOOLS_NAME_CHANGE"></span>Modifica del nome degli strumenti del Gateway Desktop remoto</span><span class="sxs-lookup"><span data-stu-id="9827c-1348"><span id="Remote_Desktop_Gateway_Tools_name_change"></span><span id="remote_desktop_gateway_tools_name_change"></span><span id="REMOTE_DESKTOP_GATEWAY_TOOLS_NAME_CHANGE"></span>Remote Desktop Gateway Tools name change</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1349">Strumenti di gateway di Servizi terminal denominati in questa versione</span><span class="sxs-lookup"><span data-stu-id="9827c-1349">Named TS Gateway Tools in this release</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1350"><span id="Remote_Desktop_Licensing_Tools_name_change"></span><span id="remote_desktop_licensing_tools_name_change"></span><span id="REMOTE_DESKTOP_LICENSING_TOOLS_NAME_CHANGE"></span>Modifica del nome degli strumenti di gestione licenze Desktop remoto</span><span class="sxs-lookup"><span data-stu-id="9827c-1350"><span id="Remote_Desktop_Licensing_Tools_name_change"></span><span id="remote_desktop_licensing_tools_name_change"></span><span id="REMOTE_DESKTOP_LICENSING_TOOLS_NAME_CHANGE"></span>Remote Desktop Licensing Tools name change</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1351">Strumenti di licenze Servizi terminal denominati in questa versione</span><span class="sxs-lookup"><span data-stu-id="9827c-1351">Named TS Licensing Tools in this release</span></span>

</dd> <dt>

<span data-ttu-id="9827c-1352"><span id="AD_DS_Snap-Ins_and_Command-Line_Tools_name_change"></span><span id="ad_ds_snap-ins_and_command-line_tools_name_change"></span><span id="AD_DS_SNAP-INS_AND_COMMAND-LINE_TOOLS_NAME_CHANGE"></span>Snap-Ins di servizi di dominio Active Directory e modifica del nome degli strumenti Command-Line</span><span class="sxs-lookup"><span data-stu-id="9827c-1352"><span id="AD_DS_Snap-Ins_and_Command-Line_Tools_name_change"></span><span id="ad_ds_snap-ins_and_command-line_tools_name_change"></span><span id="AD_DS_SNAP-INS_AND_COMMAND-LINE_TOOLS_NAME_CHANGE"></span>AD DS Snap-Ins and Command-Line Tools name change</span></span>
</dt> <dd>

<span data-ttu-id="9827c-1353">Strumenti del Controller di dominio Active Directory</span><span class="sxs-lookup"><span data-stu-id="9827c-1353">Active Directory Domain Controller Tools</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="9827c-1354">Esempio</span><span class="sxs-lookup"><span data-stu-id="9827c-1354">Examples</span></span>

<span data-ttu-id="9827c-1355">Nello script seguente vengono visualizzati i nomi di tutte le funzionalità server nel computer denominato "FABRIKAM".</span><span class="sxs-lookup"><span data-stu-id="9827c-1355">The following script displays the names of all the server features on the computer named "FABRIKAM".</span></span> <span data-ttu-id="9827c-1356">Si noti che nel computer di destinazione deve essere in esecuzione Windows Server 2008 o un sistema operativo server successivo.</span><span class="sxs-lookup"><span data-stu-id="9827c-1356">Note that the target computer must be running Windows Server 2008 or a later server operating system.</span></span>


```VB
strComputer = "FABRIKAM"

Set objWMIService = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")

Set colFeatureList = objWMIService.ExecQuery("SELECT Name FROM Win32_ServerFeature")

For Each objFeature In colFeatureList
   WScript.Echo objFeature.Name

Next
```



## <a name="requirements"></a><span data-ttu-id="9827c-1357">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9827c-1357">Requirements</span></span>



| <span data-ttu-id="9827c-1358">Requisito</span><span class="sxs-lookup"><span data-stu-id="9827c-1358">Requirement</span></span> | <span data-ttu-id="9827c-1359">Valore</span><span class="sxs-lookup"><span data-stu-id="9827c-1359">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="9827c-1360">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9827c-1360">Minimum supported client</span></span><br/> | <span data-ttu-id="9827c-1361">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="9827c-1361">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="9827c-1362">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9827c-1362">Minimum supported server</span></span><br/> | <span data-ttu-id="9827c-1363">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9827c-1363">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="9827c-1364">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="9827c-1364">Namespace</span></span><br/>                | <span data-ttu-id="9827c-1365">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="9827c-1365">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="9827c-1366">MOF</span><span class="sxs-lookup"><span data-stu-id="9827c-1366">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9827c-1367"><dt>ServerCompProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9827c-1367"><dt>ServerCompProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="9827c-1368">DLL</span><span class="sxs-lookup"><span data-stu-id="9827c-1368">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9827c-1369"><dt>ServerCompProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9827c-1369"><dt>ServerCompProv.dll</dt></span></span> </dl> |



 

