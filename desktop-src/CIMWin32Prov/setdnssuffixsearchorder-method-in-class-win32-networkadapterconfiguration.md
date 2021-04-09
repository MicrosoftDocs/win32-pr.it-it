---
description: Il metodo statico della classe WMI SetDNSSuffixSearchOrder utilizza una matrice di elementi stringa per impostare l'ordine di ricerca dei suffissi.
ms.assetid: 1ad9fc99-8c57-43d4-92d2-b12f2c1451cb
ms.tgt_platform: multiple
title: Metodo SetDNSSuffixSearchOrder della classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetDNSSuffixSearchOrder
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 10088b1d0722f968e5d3742984baa91ec3e423aa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878026"
---
# <a name="setdnssuffixsearchorder-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="a3e62-103">Metodo SetDNSSuffixSearchOrder della \_ classe NetworkAdapterConfiguration Win32</span><span class="sxs-lookup"><span data-stu-id="a3e62-103">SetDNSSuffixSearchOrder method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="a3e62-104">Il metodo statico della [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetDNSSuffixSearchOrder** utilizza una matrice di elementi stringa per impostare l'ordine di ricerca dei suffissi.</span><span class="sxs-lookup"><span data-stu-id="a3e62-104">The **SetDNSSuffixSearchOrder** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method uses an array of string elements to set the suffix search order.</span></span>

<span data-ttu-id="a3e62-105">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="a3e62-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="a3e62-106">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="a3e62-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="a3e62-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a3e62-107">Syntax</span></span>


```mof
uint32 SetDNSSuffixSearchOrder(
  [in] string DNSDomainSuffixSearchOrder[]
);
```



## <a name="parameters"></a><span data-ttu-id="a3e62-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="a3e62-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3e62-109">*DNSDomainSuffixSearchOrder* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a3e62-109">*DNSDomainSuffixSearchOrder* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3e62-110">Elenco di suffissi del server per eseguire una query per i server DNS.</span><span class="sxs-lookup"><span data-stu-id="a3e62-110">List of server suffixes to query for DNS servers.</span></span> <span data-ttu-id="a3e62-111">Il percorso del registro di sistema del suffisso DNS è **HKEY \_ Local \_ Machine** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **TCPIP \| nameserver**</span><span class="sxs-lookup"><span data-stu-id="a3e62-111">The registry location of the DNS suffix is **HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Services**\\**Tcpip\|NameServer**</span></span>

<span data-ttu-id="a3e62-112">Esempio: "suffix1.company.com", "suffix2.company.com"</span><span class="sxs-lookup"><span data-stu-id="a3e62-112">Example: "suffix1.company.com", "suffix2.company.com"</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3e62-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a3e62-113">Return value</span></span>

<span data-ttu-id="a3e62-114">Restituisce un valore pari a 0 (zero) per un completamento corretto quando non è richiesto il riavvio, 1 (uno) per un completamento corretto quando è necessario un riavvio e un numero diverso se si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="a3e62-114">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="a3e62-115">Per ulteriori informazioni sui codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="a3e62-115">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="a3e62-116">Per i valori **HRESULT** generali, vedere [codici di errore di sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="a3e62-116">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="a3e62-117">**Operazione completata, non è necessario riavviare il computer**</span><span class="sxs-lookup"><span data-stu-id="a3e62-117">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="a3e62-118">0</span><span class="sxs-lookup"><span data-stu-id="a3e62-118">0</span></span>

<span data-ttu-id="a3e62-119">Operazione completata, non è necessario riavviare il computer.</span><span class="sxs-lookup"><span data-stu-id="a3e62-119">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="a3e62-120">**Operazione completata, riavvio richiesto**</span><span class="sxs-lookup"><span data-stu-id="a3e62-120">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="a3e62-121">1</span><span class="sxs-lookup"><span data-stu-id="a3e62-121">1</span></span>

<span data-ttu-id="a3e62-122">Operazione completata, è necessario riavviare il computer.</span><span class="sxs-lookup"><span data-stu-id="a3e62-122">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="a3e62-123">**Metodo non supportato in questa piattaforma**</span><span class="sxs-lookup"><span data-stu-id="a3e62-123">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="a3e62-124">64</span><span class="sxs-lookup"><span data-stu-id="a3e62-124">64</span></span>

<span data-ttu-id="a3e62-125">Metodo non supportato in questa piattaforma.</span><span class="sxs-lookup"><span data-stu-id="a3e62-125">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="a3e62-126">**Errore sconosciuto**</span><span class="sxs-lookup"><span data-stu-id="a3e62-126">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="a3e62-127">65</span><span class="sxs-lookup"><span data-stu-id="a3e62-127">65</span></span>

<span data-ttu-id="a3e62-128">Errore sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="a3e62-128">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="a3e62-129">**subnet mask non valido**</span><span class="sxs-lookup"><span data-stu-id="a3e62-129">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="a3e62-130">66</span><span class="sxs-lookup"><span data-stu-id="a3e62-130">66</span></span>

<span data-ttu-id="a3e62-131">Subnet mask non valido.</span><span class="sxs-lookup"><span data-stu-id="a3e62-131">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="a3e62-132">**Si è verificato un errore durante l'elaborazione di un'istanza restituita**</span><span class="sxs-lookup"><span data-stu-id="a3e62-132">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="a3e62-133">67</span><span class="sxs-lookup"><span data-stu-id="a3e62-133">67</span></span>

<span data-ttu-id="a3e62-134">Si è verificato un errore durante l'elaborazione di un'istanza di restituita.</span><span class="sxs-lookup"><span data-stu-id="a3e62-134">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="a3e62-135">**Parametro di input non valido**</span><span class="sxs-lookup"><span data-stu-id="a3e62-135">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="a3e62-136">68</span><span class="sxs-lookup"><span data-stu-id="a3e62-136">68</span></span>

<span data-ttu-id="a3e62-137">Parametro di input non valido.</span><span class="sxs-lookup"><span data-stu-id="a3e62-137">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="a3e62-138">**Sono stati specificati più di 5 gateway**</span><span class="sxs-lookup"><span data-stu-id="a3e62-138">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="a3e62-139">69</span><span class="sxs-lookup"><span data-stu-id="a3e62-139">69</span></span>

<span data-ttu-id="a3e62-140">Sono stati specificati più di cinque gateway.</span><span class="sxs-lookup"><span data-stu-id="a3e62-140">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="a3e62-141">**Indirizzo IP non valido**</span><span class="sxs-lookup"><span data-stu-id="a3e62-141">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="a3e62-142">70</span><span class="sxs-lookup"><span data-stu-id="a3e62-142">70</span></span>

<span data-ttu-id="a3e62-143">Indirizzo IP non valido.</span><span class="sxs-lookup"><span data-stu-id="a3e62-143">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="a3e62-144">**Indirizzo IP gateway non valido**</span><span class="sxs-lookup"><span data-stu-id="a3e62-144">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="a3e62-145">71</span><span class="sxs-lookup"><span data-stu-id="a3e62-145">71</span></span>

<span data-ttu-id="a3e62-146">Indirizzo IP del gateway non valido.</span><span class="sxs-lookup"><span data-stu-id="a3e62-146">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="a3e62-147">**Si è verificato un errore durante l'accesso al registro di sistema per le informazioni richieste**</span><span class="sxs-lookup"><span data-stu-id="a3e62-147">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="a3e62-148">72</span><span class="sxs-lookup"><span data-stu-id="a3e62-148">72</span></span>

<span data-ttu-id="a3e62-149">Si è verificato un errore durante l'accesso al registro di sistema per le informazioni richieste.</span><span class="sxs-lookup"><span data-stu-id="a3e62-149">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="a3e62-150">**Nome di dominio non valido**</span><span class="sxs-lookup"><span data-stu-id="a3e62-150">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="a3e62-151">73</span><span class="sxs-lookup"><span data-stu-id="a3e62-151">73</span></span>

<span data-ttu-id="a3e62-152">Nome di dominio non valido.</span><span class="sxs-lookup"><span data-stu-id="a3e62-152">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="a3e62-153">**Nome host non valido**</span><span class="sxs-lookup"><span data-stu-id="a3e62-153">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="a3e62-154">74</span><span class="sxs-lookup"><span data-stu-id="a3e62-154">74</span></span>

<span data-ttu-id="a3e62-155">Nome host non valido.</span><span class="sxs-lookup"><span data-stu-id="a3e62-155">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="a3e62-156">**Nessun server WINS primario/secondario definito**</span><span class="sxs-lookup"><span data-stu-id="a3e62-156">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="a3e62-157">75</span><span class="sxs-lookup"><span data-stu-id="a3e62-157">75</span></span>

<span data-ttu-id="a3e62-158">Nessun server WINS primario o secondario definito.</span><span class="sxs-lookup"><span data-stu-id="a3e62-158">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="a3e62-159">**File non valido**</span><span class="sxs-lookup"><span data-stu-id="a3e62-159">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="a3e62-160">76</span><span class="sxs-lookup"><span data-stu-id="a3e62-160">76</span></span>

<span data-ttu-id="a3e62-161">File non valido.</span><span class="sxs-lookup"><span data-stu-id="a3e62-161">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="a3e62-162">**Percorso di sistema non valido**</span><span class="sxs-lookup"><span data-stu-id="a3e62-162">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="a3e62-163">77</span><span class="sxs-lookup"><span data-stu-id="a3e62-163">77</span></span>

<span data-ttu-id="a3e62-164">Percorso di sistema non valido.</span><span class="sxs-lookup"><span data-stu-id="a3e62-164">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="a3e62-165">**Copia del file non riuscita**</span><span class="sxs-lookup"><span data-stu-id="a3e62-165">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="a3e62-166">78</span><span class="sxs-lookup"><span data-stu-id="a3e62-166">78</span></span>

<span data-ttu-id="a3e62-167">Copia del file non riuscita.</span><span class="sxs-lookup"><span data-stu-id="a3e62-167">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="a3e62-168">**Parametro di sicurezza non valido**</span><span class="sxs-lookup"><span data-stu-id="a3e62-168">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="a3e62-169">79</span><span class="sxs-lookup"><span data-stu-id="a3e62-169">79</span></span>

<span data-ttu-id="a3e62-170">Parametro di sicurezza non valido.</span><span class="sxs-lookup"><span data-stu-id="a3e62-170">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="a3e62-171">**Impossibile configurare il servizio TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="a3e62-171">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="a3e62-172">80</span><span class="sxs-lookup"><span data-stu-id="a3e62-172">80</span></span>

<span data-ttu-id="a3e62-173">Impossibile configurare il servizio TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="a3e62-173">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="a3e62-174">**Non è possibile configurare il servizio DHCP**</span><span class="sxs-lookup"><span data-stu-id="a3e62-174">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="a3e62-175">81</span><span class="sxs-lookup"><span data-stu-id="a3e62-175">81</span></span>

<span data-ttu-id="a3e62-176">Impossibile configurare il servizio DHCP.</span><span class="sxs-lookup"><span data-stu-id="a3e62-176">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="a3e62-177">**Non è possibile rinnovare il lease DHCP**</span><span class="sxs-lookup"><span data-stu-id="a3e62-177">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="a3e62-178">82</span><span class="sxs-lookup"><span data-stu-id="a3e62-178">82</span></span>

<span data-ttu-id="a3e62-179">Non è possibile rinnovare il lease DHCP.</span><span class="sxs-lookup"><span data-stu-id="a3e62-179">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="a3e62-180">**Non è possibile rilasciare il lease DHCP**</span><span class="sxs-lookup"><span data-stu-id="a3e62-180">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="a3e62-181">83</span><span class="sxs-lookup"><span data-stu-id="a3e62-181">83</span></span>

<span data-ttu-id="a3e62-182">Impossibile rilasciare il lease DHCP.</span><span class="sxs-lookup"><span data-stu-id="a3e62-182">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="a3e62-183">**IP non abilitato sulla scheda**</span><span class="sxs-lookup"><span data-stu-id="a3e62-183">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="a3e62-184">84</span><span class="sxs-lookup"><span data-stu-id="a3e62-184">84</span></span>

<span data-ttu-id="a3e62-185">IP non abilitato sulla scheda.</span><span class="sxs-lookup"><span data-stu-id="a3e62-185">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="a3e62-186">**IPX non abilitato sull'adapter**</span><span class="sxs-lookup"><span data-stu-id="a3e62-186">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="a3e62-187">85</span><span class="sxs-lookup"><span data-stu-id="a3e62-187">85</span></span>

<span data-ttu-id="a3e62-188">IPX non abilitato sulla scheda.</span><span class="sxs-lookup"><span data-stu-id="a3e62-188">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="a3e62-189">**Errore limite numero frame/rete**</span><span class="sxs-lookup"><span data-stu-id="a3e62-189">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="a3e62-190">86</span><span class="sxs-lookup"><span data-stu-id="a3e62-190">86</span></span>

<span data-ttu-id="a3e62-191">Errore dei limiti del numero di rete o del frame.</span><span class="sxs-lookup"><span data-stu-id="a3e62-191">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="a3e62-192">**Tipo di frame non valido**</span><span class="sxs-lookup"><span data-stu-id="a3e62-192">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="a3e62-193">87</span><span class="sxs-lookup"><span data-stu-id="a3e62-193">87</span></span>

<span data-ttu-id="a3e62-194">Tipo di frame non valido.</span><span class="sxs-lookup"><span data-stu-id="a3e62-194">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="a3e62-195">**Numero di rete non valido**</span><span class="sxs-lookup"><span data-stu-id="a3e62-195">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="a3e62-196">88</span><span class="sxs-lookup"><span data-stu-id="a3e62-196">88</span></span>

<span data-ttu-id="a3e62-197">Numero di rete non valido.</span><span class="sxs-lookup"><span data-stu-id="a3e62-197">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="a3e62-198">**Numero di rete duplicato**</span><span class="sxs-lookup"><span data-stu-id="a3e62-198">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="a3e62-199">89</span><span class="sxs-lookup"><span data-stu-id="a3e62-199">89</span></span>

<span data-ttu-id="a3e62-200">Numero di rete duplicato.</span><span class="sxs-lookup"><span data-stu-id="a3e62-200">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="a3e62-201">**Parametro fuori limite**</span><span class="sxs-lookup"><span data-stu-id="a3e62-201">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="a3e62-202">90</span><span class="sxs-lookup"><span data-stu-id="a3e62-202">90</span></span>

<span data-ttu-id="a3e62-203">Parametro fuori limite.</span><span class="sxs-lookup"><span data-stu-id="a3e62-203">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="a3e62-204">**Accesso negato**</span><span class="sxs-lookup"><span data-stu-id="a3e62-204">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="a3e62-205">91</span><span class="sxs-lookup"><span data-stu-id="a3e62-205">91</span></span>

<span data-ttu-id="a3e62-206">Accesso negato.</span><span class="sxs-lookup"><span data-stu-id="a3e62-206">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="a3e62-207">**Memoria insufficiente**</span><span class="sxs-lookup"><span data-stu-id="a3e62-207">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="a3e62-208">92</span><span class="sxs-lookup"><span data-stu-id="a3e62-208">92</span></span>

<span data-ttu-id="a3e62-209">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="a3e62-209">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="a3e62-210">**Esiste già**</span><span class="sxs-lookup"><span data-stu-id="a3e62-210">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="a3e62-211">93</span><span class="sxs-lookup"><span data-stu-id="a3e62-211">93</span></span>

<span data-ttu-id="a3e62-212">Esiste già.</span><span class="sxs-lookup"><span data-stu-id="a3e62-212">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="a3e62-213">**Percorso, file o oggetto non trovato**</span><span class="sxs-lookup"><span data-stu-id="a3e62-213">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="a3e62-214">94</span><span class="sxs-lookup"><span data-stu-id="a3e62-214">94</span></span>

<span data-ttu-id="a3e62-215">Il percorso, il file o l'oggetto non è stato trovato.</span><span class="sxs-lookup"><span data-stu-id="a3e62-215">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="a3e62-216">**Non è possibile inviare una notifica al servizio**</span><span class="sxs-lookup"><span data-stu-id="a3e62-216">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="a3e62-217">95</span><span class="sxs-lookup"><span data-stu-id="a3e62-217">95</span></span>

<span data-ttu-id="a3e62-218">Impossibile notificare il servizio.</span><span class="sxs-lookup"><span data-stu-id="a3e62-218">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="a3e62-219">**Non è possibile inviare una notifica al servizio DNS**</span><span class="sxs-lookup"><span data-stu-id="a3e62-219">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="a3e62-220">96</span><span class="sxs-lookup"><span data-stu-id="a3e62-220">96</span></span>

<span data-ttu-id="a3e62-221">Impossibile inviare una notifica al servizio DNS.</span><span class="sxs-lookup"><span data-stu-id="a3e62-221">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="a3e62-222">**Interfaccia non configurabile**</span><span class="sxs-lookup"><span data-stu-id="a3e62-222">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="a3e62-223">97</span><span class="sxs-lookup"><span data-stu-id="a3e62-223">97</span></span>

<span data-ttu-id="a3e62-224">Interfaccia non configurabile.</span><span class="sxs-lookup"><span data-stu-id="a3e62-224">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="a3e62-225">**Non tutti i lease DHCP possono essere rilasciati/rinnovati**</span><span class="sxs-lookup"><span data-stu-id="a3e62-225">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="a3e62-226">98</span><span class="sxs-lookup"><span data-stu-id="a3e62-226">98</span></span>

<span data-ttu-id="a3e62-227">Non tutti i lease DHCP vengono rilasciati o rinnovati.</span><span class="sxs-lookup"><span data-stu-id="a3e62-227">Not all DHCP leases are released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="a3e62-228">**DHCP non abilitato sull'adapter**</span><span class="sxs-lookup"><span data-stu-id="a3e62-228">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="a3e62-229">100</span><span class="sxs-lookup"><span data-stu-id="a3e62-229">100</span></span>

<span data-ttu-id="a3e62-230">DHCP non abilitato sulla scheda.</span><span class="sxs-lookup"><span data-stu-id="a3e62-230">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="a3e62-231">**Altri**</span><span class="sxs-lookup"><span data-stu-id="a3e62-231">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="a3e62-232">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="a3e62-232">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a3e62-233">Commenti</span><span class="sxs-lookup"><span data-stu-id="a3e62-233">Remarks</span></span>

<span data-ttu-id="a3e62-234">Si tratta di una chiamata indipendente dall'istanza che si applica a tutte le schede, ma solo per Windows.</span><span class="sxs-lookup"><span data-stu-id="a3e62-234">This is an instance-independent call that applies to all adapters but only for Windows.</span></span>

## <a name="examples"></a><span data-ttu-id="a3e62-235">Esempio</span><span class="sxs-lookup"><span data-stu-id="a3e62-235">Examples</span></span>

<span data-ttu-id="a3e62-236">L'esempio [modificare l'ordine di ricerca del suffisso DNS per tutte le schede di rete](https://Gallery.TechNet.Microsoft.Com/2857b7b0-1327-4ce2-9f2b-b662cce387c6) codice VBScript configura un computer per l'utilizzo di due suffissi DNS quando si eseguono ricerche DNS.</span><span class="sxs-lookup"><span data-stu-id="a3e62-236">The [Modify the DNS Suffix Search Order for All Network Adapters](https://Gallery.TechNet.Microsoft.Com/2857b7b0-1327-4ce2-9f2b-b662cce387c6) VBScript code sample configures a computer to use two DNS suffixes when performing DNS searches.</span></span>

<span data-ttu-id="a3e62-237">L'esempio [Enable DHCP settings on a computer](https://Gallery.TechNet.Microsoft.Com/41e6ab51-78c0-4413-b086-03fde33ea125) VBScript configura tutte le impostazioni in genere necessarie per abilitare DHCP in un computer.</span><span class="sxs-lookup"><span data-stu-id="a3e62-237">The [Enable DHCP Settings on a Computer](https://Gallery.TechNet.Microsoft.Com/41e6ab51-78c0-4413-b086-03fde33ea125) VBScript sample configures all the settings typically required to enable DHCP on a computer.</span></span>

<span data-ttu-id="a3e62-238">Il codice di PowerShell seguente imposta l'ordine di ricerca dei suffissi DNS.</span><span class="sxs-lookup"><span data-stu-id="a3e62-238">The following PowerShell code sets the DNS suffix search order.</span></span>


```PowerShell
#First store the suffixes to set in a variable
$suffixes = 'microsoft.com', 'google.com', 'yahoo.com'

#Since this is a static method, get a class object and then call the method. 
$class = [wmiclass]'Win32_NetworkAdapterConfiguration'
$class.SetDNSSuffixSearchOrder($suffixes)
```



## <a name="requirements"></a><span data-ttu-id="a3e62-239">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a3e62-239">Requirements</span></span>



| <span data-ttu-id="a3e62-240">Requisito</span><span class="sxs-lookup"><span data-stu-id="a3e62-240">Requirement</span></span> | <span data-ttu-id="a3e62-241">Valore</span><span class="sxs-lookup"><span data-stu-id="a3e62-241">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a3e62-242">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a3e62-242">Minimum supported client</span></span><br/> | <span data-ttu-id="a3e62-243">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a3e62-243">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a3e62-244">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a3e62-244">Minimum supported server</span></span><br/> | <span data-ttu-id="a3e62-245">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a3e62-245">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a3e62-246">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="a3e62-246">Namespace</span></span><br/>                | <span data-ttu-id="a3e62-247">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="a3e62-247">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a3e62-248">MOF</span><span class="sxs-lookup"><span data-stu-id="a3e62-248">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a3e62-249"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a3e62-249"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a3e62-250">DLL</span><span class="sxs-lookup"><span data-stu-id="a3e62-250">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a3e62-251"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a3e62-251"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a3e62-252">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a3e62-252">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3e62-253">Classi hardware del sistema del computer</span><span class="sxs-lookup"><span data-stu-id="a3e62-253">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="a3e62-254">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="a3e62-254">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="a3e62-255">Attività WMI: rete</span><span class="sxs-lookup"><span data-stu-id="a3e62-255">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="a3e62-256">Attività WMI: account e domini</span><span class="sxs-lookup"><span data-stu-id="a3e62-256">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="a3e62-257">Supporto di IPv6 e IPv4 in WMI</span><span class="sxs-lookup"><span data-stu-id="a3e62-257">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

