---
description: Il metodo statico della classe WMI ReleaseDHCPLeaseAll rilascia gli indirizzi IP associati a tutte le schede di rete abilitate per DHCP.
ms.assetid: d9f83953-f3da-419d-8c84-649c39b4945e
ms.tgt_platform: multiple
title: Metodo ReleaseDHCPLeaseAll della classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.ReleaseDHCPLeaseAll
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3e7b1f7cf2f09fa20f7bf19b15e82f536ca0aa50
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305102"
---
# <a name="releasedhcpleaseall-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="02974-103">Metodo ReleaseDHCPLeaseAll della \_ classe NetworkAdapterConfiguration Win32</span><span class="sxs-lookup"><span data-stu-id="02974-103">ReleaseDHCPLeaseAll method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="02974-104">Il metodo statico della [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **ReleaseDHCPLeaseAll** rilascia gli indirizzi IP associati a tutte le schede di rete abilitate per DHCP.</span><span class="sxs-lookup"><span data-stu-id="02974-104">The **ReleaseDHCPLeaseAll** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method releases the IP addresses bound to all DHCP-enabled network adapters.</span></span>

> [!Note]  
> <span data-ttu-id="02974-105">Avviso se DHCP è abilitato nel computer locale, l'opzione consente di terminare tutte le connessioni TCP/IP DHCP.</span><span class="sxs-lookup"><span data-stu-id="02974-105">Warning If DHCP is enabled on the local computer system, the option will terminate all DHCP TCP/IP connections.</span></span>

 

<span data-ttu-id="02974-106">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="02974-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="02974-107">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="02974-107">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="02974-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="02974-108">Syntax</span></span>


```mof
uint32 ReleaseDHCPLeaseAll();
```



## <a name="parameters"></a><span data-ttu-id="02974-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="02974-109">Parameters</span></span>

<span data-ttu-id="02974-110">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="02974-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="02974-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="02974-111">Return value</span></span>

<span data-ttu-id="02974-112">Restituisce un valore pari a 0 (zero) per un completamento corretto quando non è richiesto il riavvio, 1 (uno) per un completamento corretto quando è necessario un riavvio e un numero diverso se si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="02974-112">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="02974-113">Per ulteriori informazioni sui codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="02974-113">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="02974-114">Per i valori **HRESULT** generali, vedere [codici di errore di sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="02974-114">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="02974-115">**Operazione completata, non è necessario riavviare il computer**</span><span class="sxs-lookup"><span data-stu-id="02974-115">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="02974-116">0</span><span class="sxs-lookup"><span data-stu-id="02974-116">0</span></span>

<span data-ttu-id="02974-117">Operazione completata, non è necessario riavviare il computer.</span><span class="sxs-lookup"><span data-stu-id="02974-117">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="02974-118">**Operazione completata, riavvio richiesto**</span><span class="sxs-lookup"><span data-stu-id="02974-118">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="02974-119">1</span><span class="sxs-lookup"><span data-stu-id="02974-119">1</span></span>

<span data-ttu-id="02974-120">Operazione completata, è necessario riavviare il computer.</span><span class="sxs-lookup"><span data-stu-id="02974-120">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="02974-121">**Metodo non supportato in questa piattaforma**</span><span class="sxs-lookup"><span data-stu-id="02974-121">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="02974-122">64</span><span class="sxs-lookup"><span data-stu-id="02974-122">64</span></span>

<span data-ttu-id="02974-123">Metodo non supportato in questa piattaforma.</span><span class="sxs-lookup"><span data-stu-id="02974-123">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="02974-124">**Errore sconosciuto**</span><span class="sxs-lookup"><span data-stu-id="02974-124">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="02974-125">65</span><span class="sxs-lookup"><span data-stu-id="02974-125">65</span></span>

<span data-ttu-id="02974-126">Errore sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="02974-126">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="02974-127">**subnet mask non valido**</span><span class="sxs-lookup"><span data-stu-id="02974-127">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="02974-128">66</span><span class="sxs-lookup"><span data-stu-id="02974-128">66</span></span>

<span data-ttu-id="02974-129">Subnet mask non valido.</span><span class="sxs-lookup"><span data-stu-id="02974-129">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="02974-130">**Si è verificato un errore durante l'elaborazione di un'istanza restituita**</span><span class="sxs-lookup"><span data-stu-id="02974-130">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="02974-131">67</span><span class="sxs-lookup"><span data-stu-id="02974-131">67</span></span>

<span data-ttu-id="02974-132">Si è verificato un errore durante l'elaborazione di un'istanza di restituita.</span><span class="sxs-lookup"><span data-stu-id="02974-132">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="02974-133">**Parametro di input non valido**</span><span class="sxs-lookup"><span data-stu-id="02974-133">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="02974-134">68</span><span class="sxs-lookup"><span data-stu-id="02974-134">68</span></span>

<span data-ttu-id="02974-135">Parametro di input non valido.</span><span class="sxs-lookup"><span data-stu-id="02974-135">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="02974-136">**Sono stati specificati più di 5 gateway**</span><span class="sxs-lookup"><span data-stu-id="02974-136">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="02974-137">69</span><span class="sxs-lookup"><span data-stu-id="02974-137">69</span></span>

<span data-ttu-id="02974-138">Sono stati specificati più di cinque gateway.</span><span class="sxs-lookup"><span data-stu-id="02974-138">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="02974-139">**Indirizzo IP non valido**</span><span class="sxs-lookup"><span data-stu-id="02974-139">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="02974-140">70</span><span class="sxs-lookup"><span data-stu-id="02974-140">70</span></span>

<span data-ttu-id="02974-141">Indirizzo IP non valido.</span><span class="sxs-lookup"><span data-stu-id="02974-141">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="02974-142">**Indirizzo IP gateway non valido**</span><span class="sxs-lookup"><span data-stu-id="02974-142">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="02974-143">71</span><span class="sxs-lookup"><span data-stu-id="02974-143">71</span></span>

<span data-ttu-id="02974-144">Indirizzo IP del gateway non valido.</span><span class="sxs-lookup"><span data-stu-id="02974-144">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="02974-145">**Si è verificato un errore durante l'accesso al registro di sistema per le informazioni richieste**</span><span class="sxs-lookup"><span data-stu-id="02974-145">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="02974-146">72</span><span class="sxs-lookup"><span data-stu-id="02974-146">72</span></span>

<span data-ttu-id="02974-147">Si è verificato un errore durante l'accesso al registro di sistema per le informazioni richieste.</span><span class="sxs-lookup"><span data-stu-id="02974-147">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="02974-148">**Nome di dominio non valido**</span><span class="sxs-lookup"><span data-stu-id="02974-148">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="02974-149">73</span><span class="sxs-lookup"><span data-stu-id="02974-149">73</span></span>

<span data-ttu-id="02974-150">Nome di dominio non valido.</span><span class="sxs-lookup"><span data-stu-id="02974-150">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="02974-151">**Nome host non valido**</span><span class="sxs-lookup"><span data-stu-id="02974-151">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="02974-152">74</span><span class="sxs-lookup"><span data-stu-id="02974-152">74</span></span>

<span data-ttu-id="02974-153">Nome host non valido.</span><span class="sxs-lookup"><span data-stu-id="02974-153">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="02974-154">**Nessun server WINS primario/secondario definito**</span><span class="sxs-lookup"><span data-stu-id="02974-154">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="02974-155">75</span><span class="sxs-lookup"><span data-stu-id="02974-155">75</span></span>

<span data-ttu-id="02974-156">Nessun server WINS primario o secondario definito.</span><span class="sxs-lookup"><span data-stu-id="02974-156">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="02974-157">**File non valido**</span><span class="sxs-lookup"><span data-stu-id="02974-157">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="02974-158">76</span><span class="sxs-lookup"><span data-stu-id="02974-158">76</span></span>

<span data-ttu-id="02974-159">File non valido.</span><span class="sxs-lookup"><span data-stu-id="02974-159">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="02974-160">**Percorso di sistema non valido**</span><span class="sxs-lookup"><span data-stu-id="02974-160">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="02974-161">77</span><span class="sxs-lookup"><span data-stu-id="02974-161">77</span></span>

<span data-ttu-id="02974-162">Percorso di sistema non valido.</span><span class="sxs-lookup"><span data-stu-id="02974-162">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="02974-163">**Copia del file non riuscita**</span><span class="sxs-lookup"><span data-stu-id="02974-163">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="02974-164">78</span><span class="sxs-lookup"><span data-stu-id="02974-164">78</span></span>

<span data-ttu-id="02974-165">Copia del file non riuscita.</span><span class="sxs-lookup"><span data-stu-id="02974-165">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="02974-166">**Parametro di sicurezza non valido**</span><span class="sxs-lookup"><span data-stu-id="02974-166">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="02974-167">79</span><span class="sxs-lookup"><span data-stu-id="02974-167">79</span></span>

<span data-ttu-id="02974-168">Parametro di sicurezza non valido.</span><span class="sxs-lookup"><span data-stu-id="02974-168">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="02974-169">**Impossibile configurare il servizio TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="02974-169">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="02974-170">80</span><span class="sxs-lookup"><span data-stu-id="02974-170">80</span></span>

<span data-ttu-id="02974-171">Impossibile configurare il servizio TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="02974-171">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="02974-172">**Non è possibile configurare il servizio DHCP**</span><span class="sxs-lookup"><span data-stu-id="02974-172">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="02974-173">81</span><span class="sxs-lookup"><span data-stu-id="02974-173">81</span></span>

<span data-ttu-id="02974-174">Impossibile configurare il servizio DHCP.</span><span class="sxs-lookup"><span data-stu-id="02974-174">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="02974-175">**Non è possibile rinnovare il lease DHCP**</span><span class="sxs-lookup"><span data-stu-id="02974-175">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="02974-176">82</span><span class="sxs-lookup"><span data-stu-id="02974-176">82</span></span>

<span data-ttu-id="02974-177">Non è possibile rinnovare il lease DHCP.</span><span class="sxs-lookup"><span data-stu-id="02974-177">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="02974-178">**Non è possibile rilasciare il lease DHCP**</span><span class="sxs-lookup"><span data-stu-id="02974-178">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="02974-179">83</span><span class="sxs-lookup"><span data-stu-id="02974-179">83</span></span>

<span data-ttu-id="02974-180">Impossibile rilasciare il lease DHCP.</span><span class="sxs-lookup"><span data-stu-id="02974-180">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="02974-181">**IP non abilitato sulla scheda**</span><span class="sxs-lookup"><span data-stu-id="02974-181">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="02974-182">84</span><span class="sxs-lookup"><span data-stu-id="02974-182">84</span></span>

<span data-ttu-id="02974-183">IP non abilitato sulla scheda.</span><span class="sxs-lookup"><span data-stu-id="02974-183">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="02974-184">**IPX non abilitato sull'adapter**</span><span class="sxs-lookup"><span data-stu-id="02974-184">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="02974-185">85</span><span class="sxs-lookup"><span data-stu-id="02974-185">85</span></span>

<span data-ttu-id="02974-186">IPX non abilitato sulla scheda.</span><span class="sxs-lookup"><span data-stu-id="02974-186">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="02974-187">**Errore limite numero frame/rete**</span><span class="sxs-lookup"><span data-stu-id="02974-187">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="02974-188">86</span><span class="sxs-lookup"><span data-stu-id="02974-188">86</span></span>

<span data-ttu-id="02974-189">Errore dei limiti del numero di rete o del frame.</span><span class="sxs-lookup"><span data-stu-id="02974-189">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="02974-190">**Tipo di frame non valido**</span><span class="sxs-lookup"><span data-stu-id="02974-190">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="02974-191">87</span><span class="sxs-lookup"><span data-stu-id="02974-191">87</span></span>

<span data-ttu-id="02974-192">Tipo di frame non valido.</span><span class="sxs-lookup"><span data-stu-id="02974-192">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="02974-193">**Numero di rete non valido**</span><span class="sxs-lookup"><span data-stu-id="02974-193">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="02974-194">88</span><span class="sxs-lookup"><span data-stu-id="02974-194">88</span></span>

<span data-ttu-id="02974-195">Numero di rete non valido.</span><span class="sxs-lookup"><span data-stu-id="02974-195">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="02974-196">**Numero di rete duplicato**</span><span class="sxs-lookup"><span data-stu-id="02974-196">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="02974-197">89</span><span class="sxs-lookup"><span data-stu-id="02974-197">89</span></span>

<span data-ttu-id="02974-198">Numero di rete duplicato.</span><span class="sxs-lookup"><span data-stu-id="02974-198">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="02974-199">**Parametro fuori limite**</span><span class="sxs-lookup"><span data-stu-id="02974-199">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="02974-200">90</span><span class="sxs-lookup"><span data-stu-id="02974-200">90</span></span>

<span data-ttu-id="02974-201">Parametro fuori limite.</span><span class="sxs-lookup"><span data-stu-id="02974-201">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="02974-202">**Accesso negato**</span><span class="sxs-lookup"><span data-stu-id="02974-202">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="02974-203">91</span><span class="sxs-lookup"><span data-stu-id="02974-203">91</span></span>

<span data-ttu-id="02974-204">Accesso negato.</span><span class="sxs-lookup"><span data-stu-id="02974-204">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="02974-205">**Memoria insufficiente**</span><span class="sxs-lookup"><span data-stu-id="02974-205">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="02974-206">92</span><span class="sxs-lookup"><span data-stu-id="02974-206">92</span></span>

<span data-ttu-id="02974-207">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="02974-207">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="02974-208">**Esiste già**</span><span class="sxs-lookup"><span data-stu-id="02974-208">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="02974-209">93</span><span class="sxs-lookup"><span data-stu-id="02974-209">93</span></span>

<span data-ttu-id="02974-210">Esiste già.</span><span class="sxs-lookup"><span data-stu-id="02974-210">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="02974-211">**Percorso, file o oggetto non trovato**</span><span class="sxs-lookup"><span data-stu-id="02974-211">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="02974-212">94</span><span class="sxs-lookup"><span data-stu-id="02974-212">94</span></span>

<span data-ttu-id="02974-213">Il percorso, il file o l'oggetto non è stato trovato.</span><span class="sxs-lookup"><span data-stu-id="02974-213">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="02974-214">**Non è possibile inviare una notifica al servizio**</span><span class="sxs-lookup"><span data-stu-id="02974-214">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="02974-215">95</span><span class="sxs-lookup"><span data-stu-id="02974-215">95</span></span>

<span data-ttu-id="02974-216">Impossibile notificare il servizio.</span><span class="sxs-lookup"><span data-stu-id="02974-216">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="02974-217">**Non è possibile inviare una notifica al servizio DNS**</span><span class="sxs-lookup"><span data-stu-id="02974-217">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="02974-218">96</span><span class="sxs-lookup"><span data-stu-id="02974-218">96</span></span>

<span data-ttu-id="02974-219">Impossibile inviare una notifica al servizio DNS.</span><span class="sxs-lookup"><span data-stu-id="02974-219">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="02974-220">**Interfaccia non configurabile**</span><span class="sxs-lookup"><span data-stu-id="02974-220">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="02974-221">97</span><span class="sxs-lookup"><span data-stu-id="02974-221">97</span></span>

<span data-ttu-id="02974-222">Interfaccia non configurabile.</span><span class="sxs-lookup"><span data-stu-id="02974-222">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="02974-223">**Non tutti i lease DHCP possono essere rilasciati/rinnovati**</span><span class="sxs-lookup"><span data-stu-id="02974-223">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="02974-224">98</span><span class="sxs-lookup"><span data-stu-id="02974-224">98</span></span>

<span data-ttu-id="02974-225">Non tutti i lease DHCP possono essere rilasciati o rinnovati.</span><span class="sxs-lookup"><span data-stu-id="02974-225">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="02974-226">**DHCP non abilitato sull'adapter**</span><span class="sxs-lookup"><span data-stu-id="02974-226">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="02974-227">100</span><span class="sxs-lookup"><span data-stu-id="02974-227">100</span></span>

<span data-ttu-id="02974-228">DHCP non abilitato sulla scheda.</span><span class="sxs-lookup"><span data-stu-id="02974-228">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="02974-229">**Altri**</span><span class="sxs-lookup"><span data-stu-id="02974-229">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="02974-230">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="02974-230">101 4294967295</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="02974-231">Esempio</span><span class="sxs-lookup"><span data-stu-id="02974-231">Examples</span></span>

<span data-ttu-id="02974-232">L'esempio di codice VBScript seguente rilascia tutti i lease DHCP attualmente in uso in un computer.</span><span class="sxs-lookup"><span data-stu-id="02974-232">The following VBScript code sample releases all the DHCP leases currently in use on a computer.</span></span>


```VB
On Error Resume Next 
 
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set objNetworkSettings = objWMIService.Get("Win32_NetworkAdapterConfiguration") 
objNetworkSettings.ReleaseDHCPLeaseAll() 
```



## <a name="requirements"></a><span data-ttu-id="02974-233">Requisiti</span><span class="sxs-lookup"><span data-stu-id="02974-233">Requirements</span></span>



| <span data-ttu-id="02974-234">Requisito</span><span class="sxs-lookup"><span data-stu-id="02974-234">Requirement</span></span> | <span data-ttu-id="02974-235">Valore</span><span class="sxs-lookup"><span data-stu-id="02974-235">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="02974-236">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="02974-236">Minimum supported client</span></span><br/> | <span data-ttu-id="02974-237">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="02974-237">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="02974-238">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="02974-238">Minimum supported server</span></span><br/> | <span data-ttu-id="02974-239">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="02974-239">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="02974-240">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="02974-240">Namespace</span></span><br/>                | <span data-ttu-id="02974-241">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="02974-241">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="02974-242">MOF</span><span class="sxs-lookup"><span data-stu-id="02974-242">MOF</span></span><br/>                      | <dl> <span data-ttu-id="02974-243"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="02974-243"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="02974-244">DLL</span><span class="sxs-lookup"><span data-stu-id="02974-244">DLL</span></span><br/>                      | <dl> <span data-ttu-id="02974-245"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="02974-245"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02974-246">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="02974-246">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02974-247">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="02974-247">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="02974-248">Classi hardware del sistema del computer</span><span class="sxs-lookup"><span data-stu-id="02974-248">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="02974-249">Attività WMI: rete</span><span class="sxs-lookup"><span data-stu-id="02974-249">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="02974-250">Attività WMI: account e domini</span><span class="sxs-lookup"><span data-stu-id="02974-250">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="02974-251">Supporto di IPv6 e IPv4 in WMI</span><span class="sxs-lookup"><span data-stu-id="02974-251">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

