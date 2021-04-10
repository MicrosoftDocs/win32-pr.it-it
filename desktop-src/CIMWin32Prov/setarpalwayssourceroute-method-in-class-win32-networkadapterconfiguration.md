---
description: Il metodo statico della classe WMI SetArpAlwaysSourceRoute viene usato per impostare la trasmissione di query ARP tramite TCP/IP.
ms.assetid: bbff4e2e-aea6-400e-8bd8-f62aaa9fa601
ms.tgt_platform: multiple
title: Metodo SetArpAlwaysSourceRoute della classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetArpAlwaysSourceRoute
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7151fbbd13d3ac6fdf4ac3b129cdcb438abe73a9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126285"
---
# <a name="setarpalwayssourceroute-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="9a976-103">Metodo SetArpAlwaysSourceRoute della \_ classe NetworkAdapterConfiguration Win32</span><span class="sxs-lookup"><span data-stu-id="9a976-103">SetArpAlwaysSourceRoute method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="9a976-104">Il metodo statico della [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetArpAlwaysSourceRoute** viene usato per impostare la trasmissione di query ARP tramite TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="9a976-104">The **SetArpAlwaysSourceRoute** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to set the transmission of ARP queries by TCP/IP.</span></span>

<span data-ttu-id="9a976-105">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="9a976-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="9a976-106">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="9a976-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="9a976-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9a976-107">Syntax</span></span>


```mof
uint32 SetArpAlwaysSourceRoute(
  [in] boolean ArpAlwaysSourceRoute
);
```



## <a name="parameters"></a><span data-ttu-id="9a976-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="9a976-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a976-109">*ArpAlwaysSourceRoute* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9a976-109">*ArpAlwaysSourceRoute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a976-110">Se **true**, TCP/IP è forzato a trasmettere query ARP con il routing di origine abilitato nelle reti token ring.</span><span class="sxs-lookup"><span data-stu-id="9a976-110">If **true**, TCP/IP is forced to transmit ARP queries with source routing enabled on Token Ring networks.</span></span> <span data-ttu-id="9a976-111">Per impostazione predefinita, lo stack trasmette le query ARP senza prima il routing del codice sorgente, quindi i tentativi con il routing del codice sorgente abilitato se non viene ricevuta alcuna risposta.</span><span class="sxs-lookup"><span data-stu-id="9a976-111">By default, the stack transmits ARP queries without source routing first, then retries with source routing enabled if no reply is received.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a976-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9a976-112">Return value</span></span>

<span data-ttu-id="9a976-113">Restituisce un valore pari a 0 (zero) per un completamento corretto quando non è richiesto il riavvio, 1 (uno) per un completamento corretto quando è necessario un riavvio e un numero diverso se si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="9a976-113">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="9a976-114">Per ulteriori informazioni sui codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="9a976-114">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="9a976-115">Per i valori **HRESULT** generali, vedere [codici di errore di sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="9a976-115">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="9a976-116">**Operazione completata, non è necessario riavviare il computer**</span><span class="sxs-lookup"><span data-stu-id="9a976-116">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="9a976-117">0</span><span class="sxs-lookup"><span data-stu-id="9a976-117">0</span></span>

<span data-ttu-id="9a976-118">Operazione completata, non è necessario riavviare il computer.</span><span class="sxs-lookup"><span data-stu-id="9a976-118">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="9a976-119">**Operazione completata, riavvio richiesto**</span><span class="sxs-lookup"><span data-stu-id="9a976-119">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="9a976-120">1</span><span class="sxs-lookup"><span data-stu-id="9a976-120">1</span></span>

<span data-ttu-id="9a976-121">Operazione completata, è necessario riavviare il computer.</span><span class="sxs-lookup"><span data-stu-id="9a976-121">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="9a976-122">**Metodo non supportato in questa piattaforma**</span><span class="sxs-lookup"><span data-stu-id="9a976-122">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="9a976-123">64</span><span class="sxs-lookup"><span data-stu-id="9a976-123">64</span></span>

<span data-ttu-id="9a976-124">Metodo non supportato in questa piattaforma.</span><span class="sxs-lookup"><span data-stu-id="9a976-124">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="9a976-125">**Errore sconosciuto**</span><span class="sxs-lookup"><span data-stu-id="9a976-125">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="9a976-126">65</span><span class="sxs-lookup"><span data-stu-id="9a976-126">65</span></span>

<span data-ttu-id="9a976-127">Errore sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="9a976-127">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="9a976-128">**subnet mask non valido**</span><span class="sxs-lookup"><span data-stu-id="9a976-128">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="9a976-129">66</span><span class="sxs-lookup"><span data-stu-id="9a976-129">66</span></span>

<span data-ttu-id="9a976-130">Subnet mask non valido.</span><span class="sxs-lookup"><span data-stu-id="9a976-130">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="9a976-131">**Si è verificato un errore durante l'elaborazione di un'istanza restituita**</span><span class="sxs-lookup"><span data-stu-id="9a976-131">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="9a976-132">67</span><span class="sxs-lookup"><span data-stu-id="9a976-132">67</span></span>

<span data-ttu-id="9a976-133">Si è verificato un errore durante l'elaborazione di un'istanza di restituita.</span><span class="sxs-lookup"><span data-stu-id="9a976-133">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="9a976-134">**Parametro di input non valido**</span><span class="sxs-lookup"><span data-stu-id="9a976-134">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="9a976-135">68</span><span class="sxs-lookup"><span data-stu-id="9a976-135">68</span></span>

<span data-ttu-id="9a976-136">Parametro di input non valido.</span><span class="sxs-lookup"><span data-stu-id="9a976-136">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="9a976-137">**Sono stati specificati più di 5 gateway**</span><span class="sxs-lookup"><span data-stu-id="9a976-137">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="9a976-138">69</span><span class="sxs-lookup"><span data-stu-id="9a976-138">69</span></span>

<span data-ttu-id="9a976-139">Sono stati specificati più di cinque gateway.</span><span class="sxs-lookup"><span data-stu-id="9a976-139">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="9a976-140">**Indirizzo IP non valido**</span><span class="sxs-lookup"><span data-stu-id="9a976-140">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="9a976-141">70</span><span class="sxs-lookup"><span data-stu-id="9a976-141">70</span></span>

<span data-ttu-id="9a976-142">Indirizzo IP non valido.</span><span class="sxs-lookup"><span data-stu-id="9a976-142">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="9a976-143">**Indirizzo IP gateway non valido**</span><span class="sxs-lookup"><span data-stu-id="9a976-143">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="9a976-144">71</span><span class="sxs-lookup"><span data-stu-id="9a976-144">71</span></span>

<span data-ttu-id="9a976-145">Indirizzo IP del gateway non valido.</span><span class="sxs-lookup"><span data-stu-id="9a976-145">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="9a976-146">**Si è verificato un errore durante l'accesso al registro di sistema per le informazioni richieste**</span><span class="sxs-lookup"><span data-stu-id="9a976-146">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="9a976-147">72</span><span class="sxs-lookup"><span data-stu-id="9a976-147">72</span></span>

<span data-ttu-id="9a976-148">Si è verificato un errore durante l'accesso al registro di sistema per le informazioni richieste.</span><span class="sxs-lookup"><span data-stu-id="9a976-148">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="9a976-149">**Nome di dominio non valido**</span><span class="sxs-lookup"><span data-stu-id="9a976-149">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="9a976-150">73</span><span class="sxs-lookup"><span data-stu-id="9a976-150">73</span></span>

<span data-ttu-id="9a976-151">Nome di dominio non valido.</span><span class="sxs-lookup"><span data-stu-id="9a976-151">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="9a976-152">**Nome host non valido**</span><span class="sxs-lookup"><span data-stu-id="9a976-152">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="9a976-153">74</span><span class="sxs-lookup"><span data-stu-id="9a976-153">74</span></span>

<span data-ttu-id="9a976-154">Nome host non valido.</span><span class="sxs-lookup"><span data-stu-id="9a976-154">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="9a976-155">**Nessun server WINS primario/secondario definito**</span><span class="sxs-lookup"><span data-stu-id="9a976-155">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="9a976-156">75</span><span class="sxs-lookup"><span data-stu-id="9a976-156">75</span></span>

<span data-ttu-id="9a976-157">Nessun server WINS primario o secondario definito.</span><span class="sxs-lookup"><span data-stu-id="9a976-157">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="9a976-158">**File non valido**</span><span class="sxs-lookup"><span data-stu-id="9a976-158">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="9a976-159">76</span><span class="sxs-lookup"><span data-stu-id="9a976-159">76</span></span>

<span data-ttu-id="9a976-160">File non valido.</span><span class="sxs-lookup"><span data-stu-id="9a976-160">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="9a976-161">**Percorso di sistema non valido**</span><span class="sxs-lookup"><span data-stu-id="9a976-161">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="9a976-162">77</span><span class="sxs-lookup"><span data-stu-id="9a976-162">77</span></span>

<span data-ttu-id="9a976-163">Percorso di sistema non valido.</span><span class="sxs-lookup"><span data-stu-id="9a976-163">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="9a976-164">**Copia del file non riuscita**</span><span class="sxs-lookup"><span data-stu-id="9a976-164">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="9a976-165">78</span><span class="sxs-lookup"><span data-stu-id="9a976-165">78</span></span>

<span data-ttu-id="9a976-166">Copia del file non riuscita.</span><span class="sxs-lookup"><span data-stu-id="9a976-166">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="9a976-167">**Parametro di sicurezza non valido**</span><span class="sxs-lookup"><span data-stu-id="9a976-167">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="9a976-168">79</span><span class="sxs-lookup"><span data-stu-id="9a976-168">79</span></span>

<span data-ttu-id="9a976-169">Parametro di sicurezza non valido.</span><span class="sxs-lookup"><span data-stu-id="9a976-169">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="9a976-170">**Impossibile configurare il servizio TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="9a976-170">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="9a976-171">80</span><span class="sxs-lookup"><span data-stu-id="9a976-171">80</span></span>

<span data-ttu-id="9a976-172">Impossibile configurare il servizio TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="9a976-172">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="9a976-173">**Non è possibile configurare il servizio DHCP**</span><span class="sxs-lookup"><span data-stu-id="9a976-173">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="9a976-174">81</span><span class="sxs-lookup"><span data-stu-id="9a976-174">81</span></span>

<span data-ttu-id="9a976-175">Impossibile configurare il servizio DHCP.</span><span class="sxs-lookup"><span data-stu-id="9a976-175">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="9a976-176">**Non è possibile rinnovare il lease DHCP**</span><span class="sxs-lookup"><span data-stu-id="9a976-176">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="9a976-177">82</span><span class="sxs-lookup"><span data-stu-id="9a976-177">82</span></span>

<span data-ttu-id="9a976-178">Non è possibile rinnovare il lease DHCP.</span><span class="sxs-lookup"><span data-stu-id="9a976-178">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="9a976-179">**Non è possibile rilasciare il lease DHCP**</span><span class="sxs-lookup"><span data-stu-id="9a976-179">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="9a976-180">83</span><span class="sxs-lookup"><span data-stu-id="9a976-180">83</span></span>

<span data-ttu-id="9a976-181">Impossibile rilasciare il lease DHCP.</span><span class="sxs-lookup"><span data-stu-id="9a976-181">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="9a976-182">**IP non abilitato sulla scheda**</span><span class="sxs-lookup"><span data-stu-id="9a976-182">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="9a976-183">84</span><span class="sxs-lookup"><span data-stu-id="9a976-183">84</span></span>

<span data-ttu-id="9a976-184">IP non abilitato sulla scheda.</span><span class="sxs-lookup"><span data-stu-id="9a976-184">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="9a976-185">**IPX non abilitato sull'adapter**</span><span class="sxs-lookup"><span data-stu-id="9a976-185">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="9a976-186">85</span><span class="sxs-lookup"><span data-stu-id="9a976-186">85</span></span>

<span data-ttu-id="9a976-187">IPX non abilitato sulla scheda.</span><span class="sxs-lookup"><span data-stu-id="9a976-187">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="9a976-188">**Errore limite numero frame/rete**</span><span class="sxs-lookup"><span data-stu-id="9a976-188">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="9a976-189">86</span><span class="sxs-lookup"><span data-stu-id="9a976-189">86</span></span>

<span data-ttu-id="9a976-190">Errore dei limiti del numero di rete o del frame.</span><span class="sxs-lookup"><span data-stu-id="9a976-190">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="9a976-191">**Tipo di frame non valido**</span><span class="sxs-lookup"><span data-stu-id="9a976-191">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="9a976-192">87</span><span class="sxs-lookup"><span data-stu-id="9a976-192">87</span></span>

<span data-ttu-id="9a976-193">Tipo di frame non valido.</span><span class="sxs-lookup"><span data-stu-id="9a976-193">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="9a976-194">**Numero di rete non valido**</span><span class="sxs-lookup"><span data-stu-id="9a976-194">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="9a976-195">88</span><span class="sxs-lookup"><span data-stu-id="9a976-195">88</span></span>

<span data-ttu-id="9a976-196">Numero di rete non valido.</span><span class="sxs-lookup"><span data-stu-id="9a976-196">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="9a976-197">**Numero di rete duplicato**</span><span class="sxs-lookup"><span data-stu-id="9a976-197">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="9a976-198">89</span><span class="sxs-lookup"><span data-stu-id="9a976-198">89</span></span>

<span data-ttu-id="9a976-199">Numero di rete duplicato.</span><span class="sxs-lookup"><span data-stu-id="9a976-199">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="9a976-200">**Parametro fuori limite**</span><span class="sxs-lookup"><span data-stu-id="9a976-200">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="9a976-201">90</span><span class="sxs-lookup"><span data-stu-id="9a976-201">90</span></span>

<span data-ttu-id="9a976-202">Parametro fuori limite.</span><span class="sxs-lookup"><span data-stu-id="9a976-202">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="9a976-203">**Accesso negato**</span><span class="sxs-lookup"><span data-stu-id="9a976-203">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="9a976-204">91</span><span class="sxs-lookup"><span data-stu-id="9a976-204">91</span></span>

<span data-ttu-id="9a976-205">Accesso negato.</span><span class="sxs-lookup"><span data-stu-id="9a976-205">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="9a976-206">**Memoria insufficiente**</span><span class="sxs-lookup"><span data-stu-id="9a976-206">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="9a976-207">92</span><span class="sxs-lookup"><span data-stu-id="9a976-207">92</span></span>

<span data-ttu-id="9a976-208">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="9a976-208">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="9a976-209">**Esiste già**</span><span class="sxs-lookup"><span data-stu-id="9a976-209">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="9a976-210">93</span><span class="sxs-lookup"><span data-stu-id="9a976-210">93</span></span>

<span data-ttu-id="9a976-211">Esiste già.</span><span class="sxs-lookup"><span data-stu-id="9a976-211">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="9a976-212">**Percorso, file o oggetto non trovato**</span><span class="sxs-lookup"><span data-stu-id="9a976-212">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="9a976-213">94</span><span class="sxs-lookup"><span data-stu-id="9a976-213">94</span></span>

<span data-ttu-id="9a976-214">Il percorso, il file o l'oggetto non è stato trovato.</span><span class="sxs-lookup"><span data-stu-id="9a976-214">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="9a976-215">**Non è possibile inviare una notifica al servizio**</span><span class="sxs-lookup"><span data-stu-id="9a976-215">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="9a976-216">95</span><span class="sxs-lookup"><span data-stu-id="9a976-216">95</span></span>

<span data-ttu-id="9a976-217">Impossibile notificare il servizio.</span><span class="sxs-lookup"><span data-stu-id="9a976-217">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="9a976-218">**Non è possibile inviare una notifica al servizio DNS**</span><span class="sxs-lookup"><span data-stu-id="9a976-218">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="9a976-219">96</span><span class="sxs-lookup"><span data-stu-id="9a976-219">96</span></span>

<span data-ttu-id="9a976-220">Impossibile inviare una notifica al servizio DNS.</span><span class="sxs-lookup"><span data-stu-id="9a976-220">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="9a976-221">**Interfaccia non configurabile**</span><span class="sxs-lookup"><span data-stu-id="9a976-221">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="9a976-222">97</span><span class="sxs-lookup"><span data-stu-id="9a976-222">97</span></span>

<span data-ttu-id="9a976-223">Interfaccia non configurabile.</span><span class="sxs-lookup"><span data-stu-id="9a976-223">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="9a976-224">**Non tutti i lease DHCP possono essere rilasciati/rinnovati**</span><span class="sxs-lookup"><span data-stu-id="9a976-224">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="9a976-225">98</span><span class="sxs-lookup"><span data-stu-id="9a976-225">98</span></span>

<span data-ttu-id="9a976-226">Non tutti i lease DHCP possono essere rilasciati o rinnovati.</span><span class="sxs-lookup"><span data-stu-id="9a976-226">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="9a976-227">**DHCP non abilitato sull'adapter**</span><span class="sxs-lookup"><span data-stu-id="9a976-227">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="9a976-228">100</span><span class="sxs-lookup"><span data-stu-id="9a976-228">100</span></span>

<span data-ttu-id="9a976-229">DHCP non abilitato sulla scheda.</span><span class="sxs-lookup"><span data-stu-id="9a976-229">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="9a976-230">**Altri**</span><span class="sxs-lookup"><span data-stu-id="9a976-230">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="9a976-231">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="9a976-231">101 4294967295</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="9a976-232">Esempio</span><span class="sxs-lookup"><span data-stu-id="9a976-232">Examples</span></span>

<span data-ttu-id="9a976-233">L'esempio [Modify ARP queries to use source routing](https://Gallery.TechNet.Microsoft.Com/e0298c96-acc2-4809-9365-fce3000db00e) VBScript nella raccolta TechNet USA **SETARPALWAYSSOURCEROUTE** per configurare TCP/IP in modo da usare sempre il routing del codice sorgente in tutte le reti token ring.</span><span class="sxs-lookup"><span data-stu-id="9a976-233">The [Modify ARP Queries to Use Source Routing](https://Gallery.TechNet.Microsoft.Com/e0298c96-acc2-4809-9365-fce3000db00e) VBScript sample on TechNet Gallery uses **SetArpAlwaysSourceRoute** to configure TCP/IP to always use source routing on all Token Ring networks.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a976-234">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9a976-234">Requirements</span></span>



| <span data-ttu-id="9a976-235">Requisito</span><span class="sxs-lookup"><span data-stu-id="9a976-235">Requirement</span></span> | <span data-ttu-id="9a976-236">Valore</span><span class="sxs-lookup"><span data-stu-id="9a976-236">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9a976-237">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9a976-237">Minimum supported client</span></span><br/> | <span data-ttu-id="9a976-238">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9a976-238">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9a976-239">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9a976-239">Minimum supported server</span></span><br/> | <span data-ttu-id="9a976-240">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9a976-240">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9a976-241">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="9a976-241">Namespace</span></span><br/>                | <span data-ttu-id="9a976-242">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="9a976-242">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9a976-243">MOF</span><span class="sxs-lookup"><span data-stu-id="9a976-243">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9a976-244"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9a976-244"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9a976-245">DLL</span><span class="sxs-lookup"><span data-stu-id="9a976-245">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9a976-246"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9a976-246"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a976-247">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9a976-247">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a976-248">Classi hardware del sistema del computer</span><span class="sxs-lookup"><span data-stu-id="9a976-248">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="9a976-249">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="9a976-249">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="9a976-250">Attività WMI: rete</span><span class="sxs-lookup"><span data-stu-id="9a976-250">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="9a976-251">Attività WMI: account e domini</span><span class="sxs-lookup"><span data-stu-id="9a976-251">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="9a976-252">Supporto di IPv6 e IPv4 in WMI</span><span class="sxs-lookup"><span data-stu-id="9a976-252">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

