---
description: Il metodo della classe WMI EnableDHCP Abilita il Dynamic Host Configuration Protocol (DHCP) per il servizio con questa scheda di rete. DHCP consente l'allocazione dinamica degli indirizzi IP.
ms.assetid: 8c61d731-77a3-4ef4-bad9-26edaca60892
ms.tgt_platform: multiple
title: Metodo EnableDHCP della classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.EnableDHCP
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 002dedd3b0165053fea98dda035316676af638f4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966066"
---
# <a name="enabledhcp-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="f0226-104">Metodo EnableDHCP della \_ classe NetworkAdapterConfiguration Win32</span><span class="sxs-lookup"><span data-stu-id="f0226-104">EnableDHCP method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="f0226-105">Il metodo della [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **EnableDHCP** Abilita il Dynamic Host Configuration Protocol (DHCP) per il servizio con questa scheda di rete.</span><span class="sxs-lookup"><span data-stu-id="f0226-105">The **EnableDHCP** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method enables the Dynamic Host Configuration Protocol (DHCP) for service with this network adapter.</span></span> <span data-ttu-id="f0226-106">DHCP consente l'allocazione dinamica degli indirizzi IP.</span><span class="sxs-lookup"><span data-stu-id="f0226-106">DHCP allows IP addresses to be dynamically allocated.</span></span>

<span data-ttu-id="f0226-107">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="f0226-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="f0226-108">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="f0226-108">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="f0226-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f0226-109">Syntax</span></span>


```mof
uint32 EnableDHCP();
```



## <a name="parameters"></a><span data-ttu-id="f0226-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="f0226-110">Parameters</span></span>

<span data-ttu-id="f0226-111">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="f0226-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f0226-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f0226-112">Return value</span></span>

<span data-ttu-id="f0226-113">Restituisce un valore pari a 0 (zero) per un completamento corretto quando non è richiesto un riavvio, 1 (uno) per un completamento corretto quando è necessario un riavvio e qualsiasi altro numero se si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="f0226-113">Returns a value of 0 (zero) for a successful completion when a reboot is not required, 1 (one) for a successful completion when a reboot is required, and any other number if there is an error.</span></span> <span data-ttu-id="f0226-114">Per ulteriori informazioni sui codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="f0226-114">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="f0226-115">Per i valori **HRESULT** generali, vedere [codici di errore di sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="f0226-115">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="f0226-116">**Operazione completata, non è necessario riavviare il computer**</span><span class="sxs-lookup"><span data-stu-id="f0226-116">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="f0226-117">0</span><span class="sxs-lookup"><span data-stu-id="f0226-117">0</span></span>

<span data-ttu-id="f0226-118">Operazione completata, non è necessario riavviare il computer.</span><span class="sxs-lookup"><span data-stu-id="f0226-118">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="f0226-119">**Operazione completata, riavvio richiesto**</span><span class="sxs-lookup"><span data-stu-id="f0226-119">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="f0226-120">1</span><span class="sxs-lookup"><span data-stu-id="f0226-120">1</span></span>

<span data-ttu-id="f0226-121">Operazione completata, è necessario riavviare il computer.</span><span class="sxs-lookup"><span data-stu-id="f0226-121">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="f0226-122">**Metodo non supportato in questa piattaforma**</span><span class="sxs-lookup"><span data-stu-id="f0226-122">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="f0226-123">64</span><span class="sxs-lookup"><span data-stu-id="f0226-123">64</span></span>

<span data-ttu-id="f0226-124">Metodo non supportato in questa piattaforma.</span><span class="sxs-lookup"><span data-stu-id="f0226-124">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="f0226-125">**Errore sconosciuto**</span><span class="sxs-lookup"><span data-stu-id="f0226-125">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="f0226-126">65</span><span class="sxs-lookup"><span data-stu-id="f0226-126">65</span></span>

<span data-ttu-id="f0226-127">Errore sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="f0226-127">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="f0226-128">**subnet mask non valido**</span><span class="sxs-lookup"><span data-stu-id="f0226-128">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="f0226-129">66</span><span class="sxs-lookup"><span data-stu-id="f0226-129">66</span></span>

<span data-ttu-id="f0226-130">Subnet mask non valido.</span><span class="sxs-lookup"><span data-stu-id="f0226-130">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="f0226-131">**Si è verificato un errore durante l'elaborazione di un'istanza restituita**</span><span class="sxs-lookup"><span data-stu-id="f0226-131">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="f0226-132">67</span><span class="sxs-lookup"><span data-stu-id="f0226-132">67</span></span>

<span data-ttu-id="f0226-133">Si è verificato un errore durante l'elaborazione di un'istanza di restituita.</span><span class="sxs-lookup"><span data-stu-id="f0226-133">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="f0226-134">**Parametro di input non valido**</span><span class="sxs-lookup"><span data-stu-id="f0226-134">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="f0226-135">68</span><span class="sxs-lookup"><span data-stu-id="f0226-135">68</span></span>

<span data-ttu-id="f0226-136">Parametro di input non valido.</span><span class="sxs-lookup"><span data-stu-id="f0226-136">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="f0226-137">**Sono stati specificati più di 5 gateway**</span><span class="sxs-lookup"><span data-stu-id="f0226-137">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="f0226-138">69</span><span class="sxs-lookup"><span data-stu-id="f0226-138">69</span></span>

<span data-ttu-id="f0226-139">Sono stati specificati più di cinque gateway.</span><span class="sxs-lookup"><span data-stu-id="f0226-139">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="f0226-140">**Indirizzo IP non valido**</span><span class="sxs-lookup"><span data-stu-id="f0226-140">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="f0226-141">70</span><span class="sxs-lookup"><span data-stu-id="f0226-141">70</span></span>

<span data-ttu-id="f0226-142">Indirizzo IP non valido.</span><span class="sxs-lookup"><span data-stu-id="f0226-142">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="f0226-143">**Indirizzo IP gateway non valido**</span><span class="sxs-lookup"><span data-stu-id="f0226-143">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="f0226-144">71</span><span class="sxs-lookup"><span data-stu-id="f0226-144">71</span></span>

<span data-ttu-id="f0226-145">Indirizzo IP del gateway non valido.</span><span class="sxs-lookup"><span data-stu-id="f0226-145">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="f0226-146">**Si è verificato un errore durante l'accesso al registro di sistema per le informazioni richieste**</span><span class="sxs-lookup"><span data-stu-id="f0226-146">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="f0226-147">72</span><span class="sxs-lookup"><span data-stu-id="f0226-147">72</span></span>

<span data-ttu-id="f0226-148">Si è verificato un errore durante l'accesso al registro di sistema per le informazioni richieste.</span><span class="sxs-lookup"><span data-stu-id="f0226-148">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="f0226-149">**Nome di dominio non valido**</span><span class="sxs-lookup"><span data-stu-id="f0226-149">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="f0226-150">73</span><span class="sxs-lookup"><span data-stu-id="f0226-150">73</span></span>

<span data-ttu-id="f0226-151">Nome di dominio non valido.</span><span class="sxs-lookup"><span data-stu-id="f0226-151">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="f0226-152">**Nome host non valido**</span><span class="sxs-lookup"><span data-stu-id="f0226-152">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="f0226-153">74</span><span class="sxs-lookup"><span data-stu-id="f0226-153">74</span></span>

<span data-ttu-id="f0226-154">Nome host non valido.</span><span class="sxs-lookup"><span data-stu-id="f0226-154">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="f0226-155">**Nessun server WINS primario/secondario definito**</span><span class="sxs-lookup"><span data-stu-id="f0226-155">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="f0226-156">75</span><span class="sxs-lookup"><span data-stu-id="f0226-156">75</span></span>

<span data-ttu-id="f0226-157">Nessun server WINS primario o secondario definito.</span><span class="sxs-lookup"><span data-stu-id="f0226-157">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="f0226-158">**File non valido**</span><span class="sxs-lookup"><span data-stu-id="f0226-158">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="f0226-159">76</span><span class="sxs-lookup"><span data-stu-id="f0226-159">76</span></span>

<span data-ttu-id="f0226-160">File non valido.</span><span class="sxs-lookup"><span data-stu-id="f0226-160">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="f0226-161">**Percorso di sistema non valido**</span><span class="sxs-lookup"><span data-stu-id="f0226-161">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="f0226-162">77</span><span class="sxs-lookup"><span data-stu-id="f0226-162">77</span></span>

<span data-ttu-id="f0226-163">Percorso di sistema non valido.</span><span class="sxs-lookup"><span data-stu-id="f0226-163">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="f0226-164">**Copia del file non riuscita**</span><span class="sxs-lookup"><span data-stu-id="f0226-164">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="f0226-165">78</span><span class="sxs-lookup"><span data-stu-id="f0226-165">78</span></span>

<span data-ttu-id="f0226-166">Copia del file non riuscita.</span><span class="sxs-lookup"><span data-stu-id="f0226-166">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="f0226-167">**Parametro di sicurezza non valido**</span><span class="sxs-lookup"><span data-stu-id="f0226-167">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="f0226-168">79</span><span class="sxs-lookup"><span data-stu-id="f0226-168">79</span></span>

<span data-ttu-id="f0226-169">Parametro di sicurezza non valido.</span><span class="sxs-lookup"><span data-stu-id="f0226-169">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="f0226-170">**Impossibile configurare il servizio TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="f0226-170">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="f0226-171">80</span><span class="sxs-lookup"><span data-stu-id="f0226-171">80</span></span>

<span data-ttu-id="f0226-172">Impossibile configurare il servizio TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="f0226-172">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="f0226-173">**Non è possibile configurare il servizio DHCP**</span><span class="sxs-lookup"><span data-stu-id="f0226-173">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="f0226-174">81</span><span class="sxs-lookup"><span data-stu-id="f0226-174">81</span></span>

<span data-ttu-id="f0226-175">Impossibile configurare il servizio DHCP.</span><span class="sxs-lookup"><span data-stu-id="f0226-175">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="f0226-176">**Non è possibile rinnovare il lease DHCP**</span><span class="sxs-lookup"><span data-stu-id="f0226-176">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="f0226-177">82</span><span class="sxs-lookup"><span data-stu-id="f0226-177">82</span></span>

<span data-ttu-id="f0226-178">Non è possibile rinnovare il lease DHCP.</span><span class="sxs-lookup"><span data-stu-id="f0226-178">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="f0226-179">**Non è possibile rilasciare il lease DHCP**</span><span class="sxs-lookup"><span data-stu-id="f0226-179">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="f0226-180">83</span><span class="sxs-lookup"><span data-stu-id="f0226-180">83</span></span>

<span data-ttu-id="f0226-181">Impossibile rilasciare il lease DHCP.</span><span class="sxs-lookup"><span data-stu-id="f0226-181">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="f0226-182">**IP non abilitato sulla scheda**</span><span class="sxs-lookup"><span data-stu-id="f0226-182">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="f0226-183">84</span><span class="sxs-lookup"><span data-stu-id="f0226-183">84</span></span>

<span data-ttu-id="f0226-184">IP non abilitato sulla scheda.</span><span class="sxs-lookup"><span data-stu-id="f0226-184">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="f0226-185">**IPX non abilitato sull'adapter**</span><span class="sxs-lookup"><span data-stu-id="f0226-185">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="f0226-186">85</span><span class="sxs-lookup"><span data-stu-id="f0226-186">85</span></span>

<span data-ttu-id="f0226-187">IPX non abilitato sulla scheda.</span><span class="sxs-lookup"><span data-stu-id="f0226-187">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="f0226-188">**Errore limite numero frame/rete**</span><span class="sxs-lookup"><span data-stu-id="f0226-188">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="f0226-189">86</span><span class="sxs-lookup"><span data-stu-id="f0226-189">86</span></span>

<span data-ttu-id="f0226-190">Errore dei limiti del numero di rete o del frame.</span><span class="sxs-lookup"><span data-stu-id="f0226-190">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="f0226-191">**Tipo di frame non valido**</span><span class="sxs-lookup"><span data-stu-id="f0226-191">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="f0226-192">87</span><span class="sxs-lookup"><span data-stu-id="f0226-192">87</span></span>

<span data-ttu-id="f0226-193">Tipo di frame non valido.</span><span class="sxs-lookup"><span data-stu-id="f0226-193">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="f0226-194">**Numero di rete non valido**</span><span class="sxs-lookup"><span data-stu-id="f0226-194">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="f0226-195">88</span><span class="sxs-lookup"><span data-stu-id="f0226-195">88</span></span>

<span data-ttu-id="f0226-196">Numero di rete non valido.</span><span class="sxs-lookup"><span data-stu-id="f0226-196">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="f0226-197">**Numero di rete duplicato**</span><span class="sxs-lookup"><span data-stu-id="f0226-197">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="f0226-198">89</span><span class="sxs-lookup"><span data-stu-id="f0226-198">89</span></span>

<span data-ttu-id="f0226-199">Numero di rete duplicato.</span><span class="sxs-lookup"><span data-stu-id="f0226-199">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="f0226-200">**Parametro fuori limite**</span><span class="sxs-lookup"><span data-stu-id="f0226-200">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="f0226-201">90</span><span class="sxs-lookup"><span data-stu-id="f0226-201">90</span></span>

<span data-ttu-id="f0226-202">Parametro fuori limite.</span><span class="sxs-lookup"><span data-stu-id="f0226-202">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="f0226-203">**Accesso negato**</span><span class="sxs-lookup"><span data-stu-id="f0226-203">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="f0226-204">91</span><span class="sxs-lookup"><span data-stu-id="f0226-204">91</span></span>

<span data-ttu-id="f0226-205">Accesso negato.</span><span class="sxs-lookup"><span data-stu-id="f0226-205">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="f0226-206">**Memoria insufficiente**</span><span class="sxs-lookup"><span data-stu-id="f0226-206">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="f0226-207">92</span><span class="sxs-lookup"><span data-stu-id="f0226-207">92</span></span>

<span data-ttu-id="f0226-208">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="f0226-208">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="f0226-209">**Esiste già**</span><span class="sxs-lookup"><span data-stu-id="f0226-209">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="f0226-210">93</span><span class="sxs-lookup"><span data-stu-id="f0226-210">93</span></span>

<span data-ttu-id="f0226-211">Esiste già.</span><span class="sxs-lookup"><span data-stu-id="f0226-211">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="f0226-212">**Percorso, file o oggetto non trovato**</span><span class="sxs-lookup"><span data-stu-id="f0226-212">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="f0226-213">94</span><span class="sxs-lookup"><span data-stu-id="f0226-213">94</span></span>

<span data-ttu-id="f0226-214">Il percorso, il file o l'oggetto non è stato trovato.</span><span class="sxs-lookup"><span data-stu-id="f0226-214">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="f0226-215">**Non è possibile inviare una notifica al servizio**</span><span class="sxs-lookup"><span data-stu-id="f0226-215">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="f0226-216">95</span><span class="sxs-lookup"><span data-stu-id="f0226-216">95</span></span>

<span data-ttu-id="f0226-217">Impossibile notificare il servizio.</span><span class="sxs-lookup"><span data-stu-id="f0226-217">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="f0226-218">**Non è possibile inviare una notifica al servizio DNS**</span><span class="sxs-lookup"><span data-stu-id="f0226-218">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="f0226-219">96</span><span class="sxs-lookup"><span data-stu-id="f0226-219">96</span></span>

<span data-ttu-id="f0226-220">Impossibile inviare una notifica al servizio DNS.</span><span class="sxs-lookup"><span data-stu-id="f0226-220">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="f0226-221">**Interfaccia non configurabile**</span><span class="sxs-lookup"><span data-stu-id="f0226-221">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="f0226-222">97</span><span class="sxs-lookup"><span data-stu-id="f0226-222">97</span></span>

<span data-ttu-id="f0226-223">Interfaccia non configurabile.</span><span class="sxs-lookup"><span data-stu-id="f0226-223">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="f0226-224">**Non tutti i lease DHCP possono essere rilasciati/rinnovati**</span><span class="sxs-lookup"><span data-stu-id="f0226-224">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="f0226-225">98</span><span class="sxs-lookup"><span data-stu-id="f0226-225">98</span></span>

<span data-ttu-id="f0226-226">Non tutti i lease DHCP possono essere rilasciati o rinnovati.</span><span class="sxs-lookup"><span data-stu-id="f0226-226">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="f0226-227">**DHCP non abilitato sull'adapter**</span><span class="sxs-lookup"><span data-stu-id="f0226-227">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="f0226-228">100</span><span class="sxs-lookup"><span data-stu-id="f0226-228">100</span></span>

<span data-ttu-id="f0226-229">DHCP non abilitato nell'adapter.</span><span class="sxs-lookup"><span data-stu-id="f0226-229">DHCP not enabled on the adapter.</span></span>

</dd> <dt>

<span data-ttu-id="f0226-230">**Altri**</span><span class="sxs-lookup"><span data-stu-id="f0226-230">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="f0226-231">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="f0226-231">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f0226-232">Commenti</span><span class="sxs-lookup"><span data-stu-id="f0226-232">Remarks</span></span>

<span data-ttu-id="f0226-233">Questo metodo non cancella tutti i gateway statici predefiniti presenti nel computer.</span><span class="sxs-lookup"><span data-stu-id="f0226-233">This method does not clears any static default gateways present on the machine.</span></span>

## <a name="examples"></a><span data-ttu-id="f0226-234">Esempio</span><span class="sxs-lookup"><span data-stu-id="f0226-234">Examples</span></span>

<span data-ttu-id="f0226-235">L'esempio di codice [Enable DHCP and assign DNS Servers](https://Gallery.TechNet.Microsoft.Com/7b1cec46-bdb8-4afc-b240-9789eefce6de) VBScript sulla raccolta TechNet USA EnableDHCP per abilitare DHCP e assegnare i server DNS a un computer.</span><span class="sxs-lookup"><span data-stu-id="f0226-235">The [Enable DHCP and Assign DNS Servers](https://Gallery.TechNet.Microsoft.Com/7b1cec46-bdb8-4afc-b240-9789eefce6de) VBScript code sample on TechNet Gallery uses EnableDHCP to enable DHCP and assign DNS servers to a computer.</span></span>

<span data-ttu-id="f0226-236">Nell'esempio di codice VBScript seguente viene illustrato come abilitare l'utilizzo di DHCP in un'istanza di [**Win32 \_ NetworkAdapterConfiguration**](win32-networkadapterconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="f0226-236">The following VBScript code sample demonstrates how to enable DHCP use on an instance of [**Win32\_NetworkAdapterConfiguration**](win32-networkadapterconfiguration.md) .</span></span> <span data-ttu-id="f0226-237">In questo caso viene specificato l'adapter con un indice pari a 0.</span><span class="sxs-lookup"><span data-stu-id="f0226-237">In this case we specify the adapter with an Index of 0.</span></span> <span data-ttu-id="f0226-238">È necessario selezionare l'indice corretto dalle \_ istanze di NetworkAdapter Win32 per altre interfacce.</span><span class="sxs-lookup"><span data-stu-id="f0226-238">The correct index should be selected from Win32\_NetworkAdapter instances for other interfaces.</span></span>

> [!Note]  
> <span data-ttu-id="f0226-239">Supportato solo nelle piattaforme NT.</span><span class="sxs-lookup"><span data-stu-id="f0226-239">Supported on NT platforms only.</span></span>

 


```VB
Set Adapter = GetObject("winmgmts:Win32_NetworkAdapterConfiguration=0")

RetVal = Adapter.EnableDHCP()

if RetVal = 0 then 
 WScript.Echo "DHCP Enabled"
else 
 WScript.Echo "DHCP enable failed"
end if
```



<span data-ttu-id="f0226-240">Nell'esempio di codice Perl seguente viene illustrato come abilitare l'utilizzo di DHCP in un'istanza di [**Win32 \_ NetworkAdapterConfiguration**](win32-networkadapterconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="f0226-240">The following Perl code sample demonstrates how to enable DHCP use on an instance of [**Win32\_NetworkAdapterConfiguration**](win32-networkadapterconfiguration.md) .</span></span> <span data-ttu-id="f0226-241">In questo caso viene specificato l'adapter con un indice pari a 0.</span><span class="sxs-lookup"><span data-stu-id="f0226-241">In this case we specify the adapter with an Index of 0.</span></span> <span data-ttu-id="f0226-242">È necessario selezionare l'indice corretto dalle \_ istanze di NetworkAdapter Win32 per altre interfacce.</span><span class="sxs-lookup"><span data-stu-id="f0226-242">The correct index should be selected from Win32\_NetworkAdapter instances for other interfaces.</span></span>

> [!Note]  
> <span data-ttu-id="f0226-243">Supportato solo nelle piattaforme NT.</span><span class="sxs-lookup"><span data-stu-id="f0226-243">Supported on NT platforms only.</span></span>

 


```
use strict;
use Win32::OLE;

my ( $Adapter, $RetVal );

eval { $Adapter = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\cimv2")->
       Get("Win32_NetworkAdapterConfiguration=0"); };
unless ($@)
{
 print "\n";
 $RetVal = $Adapter->EnableDHCP();
 if ( $RetVal == 0)
 {
  print "DHCP Enabled\n";
 }
 else
 {
  print "DHCP enable failed\n";
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a><span data-ttu-id="f0226-244">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f0226-244">Requirements</span></span>



| <span data-ttu-id="f0226-245">Requisito</span><span class="sxs-lookup"><span data-stu-id="f0226-245">Requirement</span></span> | <span data-ttu-id="f0226-246">Valore</span><span class="sxs-lookup"><span data-stu-id="f0226-246">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f0226-247">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f0226-247">Minimum supported client</span></span><br/> | <span data-ttu-id="f0226-248">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f0226-248">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f0226-249">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f0226-249">Minimum supported server</span></span><br/> | <span data-ttu-id="f0226-250">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f0226-250">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f0226-251">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f0226-251">Namespace</span></span><br/>                | <span data-ttu-id="f0226-252">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="f0226-252">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f0226-253">MOF</span><span class="sxs-lookup"><span data-stu-id="f0226-253">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f0226-254"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f0226-254"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f0226-255">DLL</span><span class="sxs-lookup"><span data-stu-id="f0226-255">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f0226-256"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f0226-256"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0226-257">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f0226-257">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0226-258">Classi hardware del sistema del computer</span><span class="sxs-lookup"><span data-stu-id="f0226-258">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="f0226-259">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="f0226-259">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="f0226-260">Attività WMI: rete</span><span class="sxs-lookup"><span data-stu-id="f0226-260">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="f0226-261">Attività WMI: account e domini</span><span class="sxs-lookup"><span data-stu-id="f0226-261">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="f0226-262">Supporto di IPv6 e IPv4 in WMI</span><span class="sxs-lookup"><span data-stu-id="f0226-262">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

