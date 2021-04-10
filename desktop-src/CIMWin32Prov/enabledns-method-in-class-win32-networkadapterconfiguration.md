---
description: Il metodo statico della classe WMI EnableDNS abilita il Domain Name System (DNS) per il servizio.
ms.assetid: 083dccb1-eb38-4ae5-a252-0001759c0f50
ms.tgt_platform: multiple
title: Metodo EnableDNS della classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.EnableDNS
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: fc217211455d8804de47b2b3ffc761d4328fa49a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126519"
---
# <a name="enabledns-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="db677-103">Metodo EnableDNS della \_ classe NetworkAdapterConfiguration Win32</span><span class="sxs-lookup"><span data-stu-id="db677-103">EnableDNS method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="db677-104">Il metodo statico della [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **EnableDNS** Abilita il Domain Name System (DNS) per il servizio.</span><span class="sxs-lookup"><span data-stu-id="db677-104">The **EnableDNS** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method enables the Domain Name System (DNS) for service.</span></span>

<span data-ttu-id="db677-105">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="db677-105">This topic uses the Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="db677-106">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="db677-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="db677-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="db677-107">Syntax</span></span>


```mof
uint32 EnableDNS(
  [in, optional] string DNSHostName,
  [in, optional] string DNSDomain,
  [in, optional] string DNSServerSearchOrder[],
  [in, optional] string DNSDomainSuffixSearchOrder[]
);
```



## <a name="parameters"></a><span data-ttu-id="db677-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="db677-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db677-109">*DNSHostName* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="db677-109">*DNSHostName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="db677-110">Nome dell'host DNS abilitato da questo metodo.</span><span class="sxs-lookup"><span data-stu-id="db677-110">Name of the DNS host that this method enables.</span></span>

<span data-ttu-id="db677-111">Esempio: "corpdns"</span><span class="sxs-lookup"><span data-stu-id="db677-111">Example: "corpdns"</span></span>

</dd> <dt>

<span data-ttu-id="db677-112">*Dnsdomain* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="db677-112">*DNSDomain* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="db677-113">Rappresenta il nome di un'organizzazione seguito da un punto e un'estensione che indica il tipo di organizzazione.</span><span class="sxs-lookup"><span data-stu-id="db677-113">Represents an organization name followed by a period and an extension that indicates the type of organization.</span></span>

<span data-ttu-id="db677-114">Esempio: "microsoft.com"</span><span class="sxs-lookup"><span data-stu-id="db677-114">Example: "microsoft.com"</span></span>

</dd> <dt>

<span data-ttu-id="db677-115">*DNSServerSearchOrder* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="db677-115">*DNSServerSearchOrder* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="db677-116">Elenco di indirizzi IP del server su cui eseguire una query per i server DNS.</span><span class="sxs-lookup"><span data-stu-id="db677-116">List of server IP addresses to query for DNS servers.</span></span>

</dd> <dt>

<span data-ttu-id="db677-117">*DNSDomainSuffixSearchOrder* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="db677-117">*DNSDomainSuffixSearchOrder* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="db677-118">Suffisso di dominio DNS aggiunto a un nome host durante la risoluzione dei nomi.</span><span class="sxs-lookup"><span data-stu-id="db677-118">DNS domain suffix that is appended to a host name during name resolution.</span></span> <span data-ttu-id="db677-119">Quando si risolve un nome di dominio completo (FQDN) da un nome di solo host, il sistema aggiunge il nome di dominio locale.</span><span class="sxs-lookup"><span data-stu-id="db677-119">When resolving a fully qualified domain name (FQDN) from a host-only name, the system appends the local domain name.</span></span> <span data-ttu-id="db677-120">Se la risoluzione dei nomi ha esito negativo, il sistema utilizza l'elenco dei suffissi di dominio per creare altri FQDN nell'ordine elencato, quindi esegue una query sui server DNS per ciascuno di essi.</span><span class="sxs-lookup"><span data-stu-id="db677-120">If the name resolution is not successful, the system uses the domain suffix list to create additional FQDNs in the order listed, and then queries DNS servers for each one.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db677-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="db677-121">Return value</span></span>

<span data-ttu-id="db677-122">Restituisce un valore pari a 0 (zero) per un completamento corretto quando non è richiesto un riavvio, 1 (uno) per un completamento corretto quando è necessario un riavvio e qualsiasi altro numero se si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="db677-122">Returns a value of 0 (zero) for a successful completion when a reboot is not required, 1 (one) for a successful completion when a reboot is required, and any other number if there is an error.</span></span> <span data-ttu-id="db677-123">Per ulteriori informazioni sui codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="db677-123">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="db677-124">Per i valori **HRESULT** generali, vedere [codici di errore di sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="db677-124">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="db677-125">**Operazione completata, non è necessario riavviare il computer**</span><span class="sxs-lookup"><span data-stu-id="db677-125">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="db677-126">0</span><span class="sxs-lookup"><span data-stu-id="db677-126">0</span></span>

<span data-ttu-id="db677-127">Operazione completata, non è necessario riavviare il computer.</span><span class="sxs-lookup"><span data-stu-id="db677-127">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="db677-128">**Operazione completata, riavvio richiesto**</span><span class="sxs-lookup"><span data-stu-id="db677-128">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="db677-129">1</span><span class="sxs-lookup"><span data-stu-id="db677-129">1</span></span>

<span data-ttu-id="db677-130">Operazione completata, è necessario riavviare il computer.</span><span class="sxs-lookup"><span data-stu-id="db677-130">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="db677-131">**Metodo non supportato in questa piattaforma**</span><span class="sxs-lookup"><span data-stu-id="db677-131">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="db677-132">64</span><span class="sxs-lookup"><span data-stu-id="db677-132">64</span></span>

<span data-ttu-id="db677-133">Metodo non supportato in questa piattaforma.</span><span class="sxs-lookup"><span data-stu-id="db677-133">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="db677-134">**Errore sconosciuto**</span><span class="sxs-lookup"><span data-stu-id="db677-134">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="db677-135">65</span><span class="sxs-lookup"><span data-stu-id="db677-135">65</span></span>

<span data-ttu-id="db677-136">Errore sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="db677-136">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="db677-137">**subnet mask non valido**</span><span class="sxs-lookup"><span data-stu-id="db677-137">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="db677-138">66</span><span class="sxs-lookup"><span data-stu-id="db677-138">66</span></span>

<span data-ttu-id="db677-139">Subnet mask non valido.</span><span class="sxs-lookup"><span data-stu-id="db677-139">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="db677-140">**Si è verificato un errore durante l'elaborazione di un'istanza restituita**</span><span class="sxs-lookup"><span data-stu-id="db677-140">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="db677-141">67</span><span class="sxs-lookup"><span data-stu-id="db677-141">67</span></span>

<span data-ttu-id="db677-142">Si è verificato un errore durante l'elaborazione di un'istanza di restituita.</span><span class="sxs-lookup"><span data-stu-id="db677-142">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="db677-143">**Parametro di input non valido**</span><span class="sxs-lookup"><span data-stu-id="db677-143">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="db677-144">68</span><span class="sxs-lookup"><span data-stu-id="db677-144">68</span></span>

<span data-ttu-id="db677-145">Parametro di input non valido.</span><span class="sxs-lookup"><span data-stu-id="db677-145">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="db677-146">**Sono stati specificati più di 5 gateway**</span><span class="sxs-lookup"><span data-stu-id="db677-146">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="db677-147">69</span><span class="sxs-lookup"><span data-stu-id="db677-147">69</span></span>

<span data-ttu-id="db677-148">Sono stati specificati più di cinque gateway.</span><span class="sxs-lookup"><span data-stu-id="db677-148">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="db677-149">**Indirizzo IP non valido**</span><span class="sxs-lookup"><span data-stu-id="db677-149">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="db677-150">70</span><span class="sxs-lookup"><span data-stu-id="db677-150">70</span></span>

<span data-ttu-id="db677-151">Indirizzo IP non valido.</span><span class="sxs-lookup"><span data-stu-id="db677-151">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="db677-152">**Indirizzo IP gateway non valido**</span><span class="sxs-lookup"><span data-stu-id="db677-152">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="db677-153">71</span><span class="sxs-lookup"><span data-stu-id="db677-153">71</span></span>

<span data-ttu-id="db677-154">Indirizzo IP del gateway non valido.</span><span class="sxs-lookup"><span data-stu-id="db677-154">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="db677-155">**Si è verificato un errore durante l'accesso al registro di sistema per le informazioni richieste**</span><span class="sxs-lookup"><span data-stu-id="db677-155">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="db677-156">72</span><span class="sxs-lookup"><span data-stu-id="db677-156">72</span></span>

<span data-ttu-id="db677-157">Si è verificato un errore durante l'accesso al registro di sistema per le informazioni richieste.</span><span class="sxs-lookup"><span data-stu-id="db677-157">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="db677-158">**Nome di dominio non valido**</span><span class="sxs-lookup"><span data-stu-id="db677-158">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="db677-159">73</span><span class="sxs-lookup"><span data-stu-id="db677-159">73</span></span>

<span data-ttu-id="db677-160">Nome di dominio non valido.</span><span class="sxs-lookup"><span data-stu-id="db677-160">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="db677-161">**Nome host non valido**</span><span class="sxs-lookup"><span data-stu-id="db677-161">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="db677-162">74</span><span class="sxs-lookup"><span data-stu-id="db677-162">74</span></span>

<span data-ttu-id="db677-163">Nome host non valido.</span><span class="sxs-lookup"><span data-stu-id="db677-163">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="db677-164">**Nessun server WINS primario/secondario definito**</span><span class="sxs-lookup"><span data-stu-id="db677-164">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="db677-165">75</span><span class="sxs-lookup"><span data-stu-id="db677-165">75</span></span>

<span data-ttu-id="db677-166">Nessun server WINS primario o secondario definito.</span><span class="sxs-lookup"><span data-stu-id="db677-166">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="db677-167">**File non valido**</span><span class="sxs-lookup"><span data-stu-id="db677-167">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="db677-168">76</span><span class="sxs-lookup"><span data-stu-id="db677-168">76</span></span>

<span data-ttu-id="db677-169">File non valido.</span><span class="sxs-lookup"><span data-stu-id="db677-169">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="db677-170">**Percorso di sistema non valido**</span><span class="sxs-lookup"><span data-stu-id="db677-170">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="db677-171">77</span><span class="sxs-lookup"><span data-stu-id="db677-171">77</span></span>

<span data-ttu-id="db677-172">Percorso di sistema non valido.</span><span class="sxs-lookup"><span data-stu-id="db677-172">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="db677-173">**Copia del file non riuscita**</span><span class="sxs-lookup"><span data-stu-id="db677-173">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="db677-174">78</span><span class="sxs-lookup"><span data-stu-id="db677-174">78</span></span>

<span data-ttu-id="db677-175">Copia del file non riuscita.</span><span class="sxs-lookup"><span data-stu-id="db677-175">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="db677-176">**Parametro di sicurezza non valido**</span><span class="sxs-lookup"><span data-stu-id="db677-176">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="db677-177">79</span><span class="sxs-lookup"><span data-stu-id="db677-177">79</span></span>

<span data-ttu-id="db677-178">Parametro di sicurezza non valido.</span><span class="sxs-lookup"><span data-stu-id="db677-178">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="db677-179">**Impossibile configurare il servizio TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="db677-179">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="db677-180">80</span><span class="sxs-lookup"><span data-stu-id="db677-180">80</span></span>

<span data-ttu-id="db677-181">Impossibile configurare il servizio TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="db677-181">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="db677-182">**Non è possibile configurare il servizio DHCP**</span><span class="sxs-lookup"><span data-stu-id="db677-182">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="db677-183">81</span><span class="sxs-lookup"><span data-stu-id="db677-183">81</span></span>

<span data-ttu-id="db677-184">Impossibile configurare il servizio DHCP.</span><span class="sxs-lookup"><span data-stu-id="db677-184">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="db677-185">**Non è possibile rinnovare il lease DHCP**</span><span class="sxs-lookup"><span data-stu-id="db677-185">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="db677-186">82</span><span class="sxs-lookup"><span data-stu-id="db677-186">82</span></span>

<span data-ttu-id="db677-187">Non è possibile rinnovare il lease DHCP.</span><span class="sxs-lookup"><span data-stu-id="db677-187">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="db677-188">**Non è possibile rilasciare il lease DHCP**</span><span class="sxs-lookup"><span data-stu-id="db677-188">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="db677-189">83</span><span class="sxs-lookup"><span data-stu-id="db677-189">83</span></span>

<span data-ttu-id="db677-190">Impossibile rilasciare il lease DHCP.</span><span class="sxs-lookup"><span data-stu-id="db677-190">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="db677-191">**IP non abilitato sulla scheda**</span><span class="sxs-lookup"><span data-stu-id="db677-191">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="db677-192">84</span><span class="sxs-lookup"><span data-stu-id="db677-192">84</span></span>

<span data-ttu-id="db677-193">IP non abilitato sulla scheda.</span><span class="sxs-lookup"><span data-stu-id="db677-193">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="db677-194">**IPX non abilitato sull'adapter**</span><span class="sxs-lookup"><span data-stu-id="db677-194">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="db677-195">85</span><span class="sxs-lookup"><span data-stu-id="db677-195">85</span></span>

<span data-ttu-id="db677-196">IPX non abilitato sulla scheda.</span><span class="sxs-lookup"><span data-stu-id="db677-196">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="db677-197">**Errore limite numero frame/rete**</span><span class="sxs-lookup"><span data-stu-id="db677-197">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="db677-198">86</span><span class="sxs-lookup"><span data-stu-id="db677-198">86</span></span>

<span data-ttu-id="db677-199">Errore dei limiti del numero di rete o del frame.</span><span class="sxs-lookup"><span data-stu-id="db677-199">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="db677-200">**Tipo di frame non valido**</span><span class="sxs-lookup"><span data-stu-id="db677-200">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="db677-201">87</span><span class="sxs-lookup"><span data-stu-id="db677-201">87</span></span>

<span data-ttu-id="db677-202">Tipo di frame non valido.</span><span class="sxs-lookup"><span data-stu-id="db677-202">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="db677-203">**Numero di rete non valido**</span><span class="sxs-lookup"><span data-stu-id="db677-203">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="db677-204">88</span><span class="sxs-lookup"><span data-stu-id="db677-204">88</span></span>

<span data-ttu-id="db677-205">Numero di rete non valido.</span><span class="sxs-lookup"><span data-stu-id="db677-205">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="db677-206">**Numero di rete duplicato**</span><span class="sxs-lookup"><span data-stu-id="db677-206">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="db677-207">89</span><span class="sxs-lookup"><span data-stu-id="db677-207">89</span></span>

<span data-ttu-id="db677-208">Numero di rete duplicato.</span><span class="sxs-lookup"><span data-stu-id="db677-208">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="db677-209">**Parametro fuori limite**</span><span class="sxs-lookup"><span data-stu-id="db677-209">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="db677-210">90</span><span class="sxs-lookup"><span data-stu-id="db677-210">90</span></span>

<span data-ttu-id="db677-211">Parametro fuori limite.</span><span class="sxs-lookup"><span data-stu-id="db677-211">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="db677-212">**Accesso negato**</span><span class="sxs-lookup"><span data-stu-id="db677-212">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="db677-213">91</span><span class="sxs-lookup"><span data-stu-id="db677-213">91</span></span>

<span data-ttu-id="db677-214">Accesso negato.</span><span class="sxs-lookup"><span data-stu-id="db677-214">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="db677-215">**Memoria insufficiente**</span><span class="sxs-lookup"><span data-stu-id="db677-215">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="db677-216">92</span><span class="sxs-lookup"><span data-stu-id="db677-216">92</span></span>

<span data-ttu-id="db677-217">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="db677-217">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="db677-218">**Esiste già**</span><span class="sxs-lookup"><span data-stu-id="db677-218">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="db677-219">93</span><span class="sxs-lookup"><span data-stu-id="db677-219">93</span></span>

<span data-ttu-id="db677-220">Esiste già.</span><span class="sxs-lookup"><span data-stu-id="db677-220">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="db677-221">**Percorso, file o oggetto non trovato**</span><span class="sxs-lookup"><span data-stu-id="db677-221">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="db677-222">94</span><span class="sxs-lookup"><span data-stu-id="db677-222">94</span></span>

<span data-ttu-id="db677-223">Il percorso, il file o l'oggetto non è stato trovato.</span><span class="sxs-lookup"><span data-stu-id="db677-223">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="db677-224">**Non è possibile inviare una notifica al servizio**</span><span class="sxs-lookup"><span data-stu-id="db677-224">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="db677-225">95</span><span class="sxs-lookup"><span data-stu-id="db677-225">95</span></span>

<span data-ttu-id="db677-226">Impossibile notificare il servizio.</span><span class="sxs-lookup"><span data-stu-id="db677-226">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="db677-227">**Non è possibile inviare una notifica al servizio DNS**</span><span class="sxs-lookup"><span data-stu-id="db677-227">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="db677-228">96</span><span class="sxs-lookup"><span data-stu-id="db677-228">96</span></span>

<span data-ttu-id="db677-229">Impossibile inviare una notifica al servizio DNS.</span><span class="sxs-lookup"><span data-stu-id="db677-229">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="db677-230">**Interfaccia non configurabile**</span><span class="sxs-lookup"><span data-stu-id="db677-230">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="db677-231">97</span><span class="sxs-lookup"><span data-stu-id="db677-231">97</span></span>

<span data-ttu-id="db677-232">Interfaccia non configurabile.</span><span class="sxs-lookup"><span data-stu-id="db677-232">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="db677-233">**Non tutti i lease DHCP possono essere rilasciati/rinnovati**</span><span class="sxs-lookup"><span data-stu-id="db677-233">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="db677-234">98</span><span class="sxs-lookup"><span data-stu-id="db677-234">98</span></span>

<span data-ttu-id="db677-235">Non tutti i lease DHCP possono essere rilasciati o rinnovati.</span><span class="sxs-lookup"><span data-stu-id="db677-235">Not all DHCP leases can be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="db677-236">**DHCP non abilitato sull'adapter**</span><span class="sxs-lookup"><span data-stu-id="db677-236">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="db677-237">100</span><span class="sxs-lookup"><span data-stu-id="db677-237">100</span></span>

<span data-ttu-id="db677-238">DHCP non abilitato sulla scheda.</span><span class="sxs-lookup"><span data-stu-id="db677-238">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="db677-239">**Altri**</span><span class="sxs-lookup"><span data-stu-id="db677-239">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="db677-240">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="db677-240">101 4294967295</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="db677-241">Esempio</span><span class="sxs-lookup"><span data-stu-id="db677-241">Examples</span></span>

<span data-ttu-id="db677-242">Nell'esempio di codice seguente, tratto dall'esempio di codice VBScript [Abilita DNS su tutte le schede di rete](https://Gallery.TechNet.Microsoft.Com/c5736a48-71cc-4483-9605-d71d222740ac) nella raccolta TechNet, Abilita il DNS per tutte le schede di rete in un computer.</span><span class="sxs-lookup"><span data-stu-id="db677-242">The following code sample, taken from the [Enable DNS on All Network Adapters](https://Gallery.TechNet.Microsoft.Com/c5736a48-71cc-4483-9605-d71d222740ac) VBScript code sample on TechNet Gallery, enables DNS for all network adapters on a computer.</span></span>


```VB
On Error Resume Next 
 
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set objNetworkSettings = objWMIService.Get("Win32_NetworkAdapterConfiguration") 
strHostName = "fabrikam1" 
arrDNSSuffixes = Array("hr.fabrikam.com", "research.fabrikam.com") 
objNetworkSettings.EnableDNS strHostName, , , arrDNSSuffixes 
```



## <a name="requirements"></a><span data-ttu-id="db677-243">Requisiti</span><span class="sxs-lookup"><span data-stu-id="db677-243">Requirements</span></span>



| <span data-ttu-id="db677-244">Requisito</span><span class="sxs-lookup"><span data-stu-id="db677-244">Requirement</span></span> | <span data-ttu-id="db677-245">Valore</span><span class="sxs-lookup"><span data-stu-id="db677-245">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="db677-246">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="db677-246">Minimum supported client</span></span><br/> | <span data-ttu-id="db677-247">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="db677-247">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="db677-248">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="db677-248">Minimum supported server</span></span><br/> | <span data-ttu-id="db677-249">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="db677-249">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="db677-250">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="db677-250">Namespace</span></span><br/>                | <span data-ttu-id="db677-251">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="db677-251">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="db677-252">MOF</span><span class="sxs-lookup"><span data-stu-id="db677-252">MOF</span></span><br/>                      | <dl> <span data-ttu-id="db677-253"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="db677-253"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="db677-254">DLL</span><span class="sxs-lookup"><span data-stu-id="db677-254">DLL</span></span><br/>                      | <dl> <span data-ttu-id="db677-255"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="db677-255"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db677-256">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="db677-256">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db677-257">Classi hardware del sistema del computer</span><span class="sxs-lookup"><span data-stu-id="db677-257">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="db677-258">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="db677-258">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="db677-259">Attività WMI: rete</span><span class="sxs-lookup"><span data-stu-id="db677-259">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="db677-260">Attività WMI: account e domini</span><span class="sxs-lookup"><span data-stu-id="db677-260">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="db677-261">Supporto di IPv6 e IPv4 in WMI</span><span class="sxs-lookup"><span data-stu-id="db677-261">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

