---
description: Il metodo SetIPConnectionMetric viene utilizzato per impostare la metrica di routing associata a questo adapter associato a IP.
ms.assetid: d7f7c0df-51e3-4dc8-8a53-977ecde075df
ms.tgt_platform: multiple
title: Metodo SetIPConnectionMetric della classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetIPConnectionMetric
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 73d6dde0a8faea2aeaf0982459e3c377bb1ac51d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127066"
---
# <a name="setipconnectionmetric-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="f6b2d-103">Metodo SetIPConnectionMetric della \_ classe NetworkAdapterConfiguration Win32</span><span class="sxs-lookup"><span data-stu-id="f6b2d-103">SetIPConnectionMetric method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="f6b2d-104">Il metodo **SetIPConnectionMetric** viene utilizzato per impostare la metrica di routing associata a questo adapter associato a IP.</span><span class="sxs-lookup"><span data-stu-id="f6b2d-104">The **SetIPConnectionMetric** method is used to set the routing metric associated with this IP-bound adapter.</span></span>

<span data-ttu-id="f6b2d-105">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="f6b2d-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="f6b2d-106">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="f6b2d-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="f6b2d-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f6b2d-107">Syntax</span></span>


```mof
uint32 SetIPConnectionMetric(
  [in] uint32 IPConnectionMetric
);
```



## <a name="parameters"></a><span data-ttu-id="f6b2d-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="f6b2d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f6b2d-109">*IPConnectionMetric* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f6b2d-109">*IPConnectionMetric* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6b2d-110">Indica il costo di utilizzo delle route configurate per questa scheda associata a IP.</span><span class="sxs-lookup"><span data-stu-id="f6b2d-110">Indicates the cost of using the configured routes for this IP-bound adapter.</span></span> <span data-ttu-id="f6b2d-111">Il valore viene ponderato per le route nella tabella di routing IP.</span><span class="sxs-lookup"><span data-stu-id="f6b2d-111">The value is weighted for those routes in the IP routing table.</span></span> <span data-ttu-id="f6b2d-112">Se sono presenti più route per una destinazione nella tabella di routing, viene utilizzata la route con la metrica più bassa.</span><span class="sxs-lookup"><span data-stu-id="f6b2d-112">If there are multiple routes to a destination in the routing table, the route with the lowest metric is used.</span></span> <span data-ttu-id="f6b2d-113">L'intervallo di valori validi è compreso tra 1 e 9999.</span><span class="sxs-lookup"><span data-stu-id="f6b2d-113">The range of valid values is 1 through 9999.</span></span> <span data-ttu-id="f6b2d-114">Il valore predefinito è 1.</span><span class="sxs-lookup"><span data-stu-id="f6b2d-114">The default value is 1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f6b2d-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f6b2d-115">Return value</span></span>

<span data-ttu-id="f6b2d-116">Restituisce un valore pari a 0 (zero) per un completamento corretto quando non è richiesto il riavvio, 1 (uno) per un completamento corretto quando è necessario un riavvio e un numero diverso se si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="f6b2d-116">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="f6b2d-117">Per ulteriori informazioni sui codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="f6b2d-117">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="f6b2d-118">Per i valori **HRESULT** generali, vedere [codici di errore di sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="f6b2d-118">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="f6b2d-119">**Operazione completata, non è necessario riavviare il computer**</span><span class="sxs-lookup"><span data-stu-id="f6b2d-119">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="f6b2d-120">0</span><span class="sxs-lookup"><span data-stu-id="f6b2d-120">0</span></span>

<span data-ttu-id="f6b2d-121">Operazione completata, non è necessario riavviare il computer.</span><span class="sxs-lookup"><span data-stu-id="f6b2d-121">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="f6b2d-122">**Operazione completata, riavvio richiesto**</span><span class="sxs-lookup"><span data-stu-id="f6b2d-122">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="f6b2d-123">1</span><span class="sxs-lookup"><span data-stu-id="f6b2d-123">1</span></span>

<span data-ttu-id="f6b2d-124">Operazione completata, è necessario riavviare il computer.</span><span class="sxs-lookup"><span data-stu-id="f6b2d-124">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="f6b2d-125">**Metodo non supportato in questa piattaforma**</span><span class="sxs-lookup"><span data-stu-id="f6b2d-125">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="f6b2d-126">64</span><span class="sxs-lookup"><span data-stu-id="f6b2d-126">64</span></span>

<span data-ttu-id="f6b2d-127">Metodo non supportato in questa piattaforma.</span><span class="sxs-lookup"><span data-stu-id="f6b2d-127">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="f6b2d-128">**Errore sconosciuto**</span><span class="sxs-lookup"><span data-stu-id="f6b2d-128">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="f6b2d-129">65</span><span class="sxs-lookup"><span data-stu-id="f6b2d-129">65</span></span>

<span data-ttu-id="f6b2d-130">Errore sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="f6b2d-130">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="f6b2d-131">**subnet mask non valido**</span><span class="sxs-lookup"><span data-stu-id="f6b2d-131">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="f6b2d-132">66</span><span class="sxs-lookup"><span data-stu-id="f6b2d-132">66</span></span>

<span data-ttu-id="f6b2d-133">Subnet mask non valido.</span><span class="sxs-lookup"><span data-stu-id="f6b2d-133">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="f6b2d-134">**Si è verificato un errore durante l'elaborazione di un'istanza restituita**</span><span class="sxs-lookup"><span data-stu-id="f6b2d-134">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="f6b2d-135">67</span><span class="sxs-lookup"><span data-stu-id="f6b2d-135">67</span></span>

<span data-ttu-id="f6b2d-136">Si è verificato un errore durante l'elaborazione di un'istanza di restituita.</span><span class="sxs-lookup"><span data-stu-id="f6b2d-136">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="f6b2d-137">**Parametro di input non valido**</span><span class="sxs-lookup"><span data-stu-id="f6b2d-137">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="f6b2d-138">68</span><span class="sxs-lookup"><span data-stu-id="f6b2d-138">68</span></span>

<span data-ttu-id="f6b2d-139">Parametro di input non valido.</span><span class="sxs-lookup"><span data-stu-id="f6b2d-139">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="f6b2d-140">**Sono stati specificati più di 5 gateway**</span><span class="sxs-lookup"><span data-stu-id="f6b2d-140">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="f6b2d-141">69</span><span class="sxs-lookup"><span data-stu-id="f6b2d-141">69</span></span>

<span data-ttu-id="f6b2d-142">Sono stati specificati più di cinque gateway.</span><span class="sxs-lookup"><span data-stu-id="f6b2d-142">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="f6b2d-143">**Indirizzo IP non valido**</span><span class="sxs-lookup"><span data-stu-id="f6b2d-143">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="f6b2d-144">70</span><span class="sxs-lookup"><span data-stu-id="f6b2d-144">70</span></span>

<span data-ttu-id="f6b2d-145">Indirizzo IP non valido.</span><span class="sxs-lookup"><span data-stu-id="f6b2d-145">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="f6b2d-146">**Indirizzo IP gateway non valido**</span><span class="sxs-lookup"><span data-stu-id="f6b2d-146">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="f6b2d-147">71</span><span class="sxs-lookup"><span data-stu-id="f6b2d-147">71</span></span>

<span data-ttu-id="f6b2d-148">Indirizzo IP del gateway non valido.</span><span class="sxs-lookup"><span data-stu-id="f6b2d-148">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="f6b2d-149">**Si è verificato un errore durante l'accesso al registro di sistema per le informazioni richieste**</span><span class="sxs-lookup"><span data-stu-id="f6b2d-149">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="f6b2d-150">72</span><span class="sxs-lookup"><span data-stu-id="f6b2d-150">72</span></span>

<span data-ttu-id="f6b2d-151">Si è verificato un errore durante l'accesso al registro di sistema per le informazioni richieste.</span><span class="sxs-lookup"><span data-stu-id="f6b2d-151">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="f6b2d-152">**Nome di dominio non valido**</span><span class="sxs-lookup"><span data-stu-id="f6b2d-152">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="f6b2d-153">73</span><span class="sxs-lookup"><span data-stu-id="f6b2d-153">73</span></span>

<span data-ttu-id="f6b2d-154">Nome di dominio non valido.</span><span class="sxs-lookup"><span data-stu-id="f6b2d-154">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="f6b2d-155">**Nome host non valido**</span><span class="sxs-lookup"><span data-stu-id="f6b2d-155">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="f6b2d-156">74</span><span class="sxs-lookup"><span data-stu-id="f6b2d-156">74</span></span>

<span data-ttu-id="f6b2d-157">Nome host non valido.</span><span class="sxs-lookup"><span data-stu-id="f6b2d-157">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="f6b2d-158">**Nessun server WINS primario/secondario definito**</span><span class="sxs-lookup"><span data-stu-id="f6b2d-158">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="f6b2d-159">75</span><span class="sxs-lookup"><span data-stu-id="f6b2d-159">75</span></span>

<span data-ttu-id="f6b2d-160">Nessun server WINS primario o secondario definito.</span><span class="sxs-lookup"><span data-stu-id="f6b2d-160">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="f6b2d-161">**File non valido**</span><span class="sxs-lookup"><span data-stu-id="f6b2d-161">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="f6b2d-162">76</span><span class="sxs-lookup"><span data-stu-id="f6b2d-162">76</span></span>

<span data-ttu-id="f6b2d-163">File non valido.</span><span class="sxs-lookup"><span data-stu-id="f6b2d-163">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="f6b2d-164">**Percorso di sistema non valido**</span><span class="sxs-lookup"><span data-stu-id="f6b2d-164">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="f6b2d-165">77</span><span class="sxs-lookup"><span data-stu-id="f6b2d-165">77</span></span>

<span data-ttu-id="f6b2d-166">Percorso di sistema non valido.</span><span class="sxs-lookup"><span data-stu-id="f6b2d-166">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="f6b2d-167">**Copia del file non riuscita**</span><span class="sxs-lookup"><span data-stu-id="f6b2d-167">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="f6b2d-168">78</span><span class="sxs-lookup"><span data-stu-id="f6b2d-168">78</span></span>

<span data-ttu-id="f6b2d-169">Copia del file non riuscita.</span><span class="sxs-lookup"><span data-stu-id="f6b2d-169">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="f6b2d-170">**Parametro di sicurezza non valido**</span><span class="sxs-lookup"><span data-stu-id="f6b2d-170">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="f6b2d-171">79</span><span class="sxs-lookup"><span data-stu-id="f6b2d-171">79</span></span>

<span data-ttu-id="f6b2d-172">Parametro di sicurezza non valido.</span><span class="sxs-lookup"><span data-stu-id="f6b2d-172">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="f6b2d-173">**Impossibile configurare il servizio TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="f6b2d-173">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="f6b2d-174">80</span><span class="sxs-lookup"><span data-stu-id="f6b2d-174">80</span></span>

<span data-ttu-id="f6b2d-175">Impossibile configurare il servizio TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="f6b2d-175">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="f6b2d-176">**Non è possibile configurare il servizio DHCP**</span><span class="sxs-lookup"><span data-stu-id="f6b2d-176">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="f6b2d-177">81</span><span class="sxs-lookup"><span data-stu-id="f6b2d-177">81</span></span>

<span data-ttu-id="f6b2d-178">Impossibile configurare il servizio DHCP.</span><span class="sxs-lookup"><span data-stu-id="f6b2d-178">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="f6b2d-179">**Non è possibile rinnovare il lease DHCP**</span><span class="sxs-lookup"><span data-stu-id="f6b2d-179">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="f6b2d-180">82</span><span class="sxs-lookup"><span data-stu-id="f6b2d-180">82</span></span>

<span data-ttu-id="f6b2d-181">Non è possibile rinnovare il lease DHCP.</span><span class="sxs-lookup"><span data-stu-id="f6b2d-181">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="f6b2d-182">**Non è possibile rilasciare il lease DHCP**</span><span class="sxs-lookup"><span data-stu-id="f6b2d-182">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="f6b2d-183">83</span><span class="sxs-lookup"><span data-stu-id="f6b2d-183">83</span></span>

<span data-ttu-id="f6b2d-184">Impossibile rilasciare il lease DHCP.</span><span class="sxs-lookup"><span data-stu-id="f6b2d-184">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="f6b2d-185">**IP non abilitato sulla scheda**</span><span class="sxs-lookup"><span data-stu-id="f6b2d-185">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="f6b2d-186">84</span><span class="sxs-lookup"><span data-stu-id="f6b2d-186">84</span></span>

<span data-ttu-id="f6b2d-187">IP non abilitato sulla scheda.</span><span class="sxs-lookup"><span data-stu-id="f6b2d-187">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="f6b2d-188">**IPX non abilitato sull'adapter**</span><span class="sxs-lookup"><span data-stu-id="f6b2d-188">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="f6b2d-189">85</span><span class="sxs-lookup"><span data-stu-id="f6b2d-189">85</span></span>

<span data-ttu-id="f6b2d-190">IPX non abilitato sulla scheda.</span><span class="sxs-lookup"><span data-stu-id="f6b2d-190">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="f6b2d-191">**Errore limite numero frame/rete**</span><span class="sxs-lookup"><span data-stu-id="f6b2d-191">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="f6b2d-192">86</span><span class="sxs-lookup"><span data-stu-id="f6b2d-192">86</span></span>

<span data-ttu-id="f6b2d-193">Errore dei limiti del numero di rete o del frame.</span><span class="sxs-lookup"><span data-stu-id="f6b2d-193">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="f6b2d-194">**Tipo di frame non valido**</span><span class="sxs-lookup"><span data-stu-id="f6b2d-194">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="f6b2d-195">87</span><span class="sxs-lookup"><span data-stu-id="f6b2d-195">87</span></span>

<span data-ttu-id="f6b2d-196">Tipo di frame non valido.</span><span class="sxs-lookup"><span data-stu-id="f6b2d-196">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="f6b2d-197">**Numero di rete non valido**</span><span class="sxs-lookup"><span data-stu-id="f6b2d-197">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="f6b2d-198">88</span><span class="sxs-lookup"><span data-stu-id="f6b2d-198">88</span></span>

<span data-ttu-id="f6b2d-199">Numero di rete non valido.</span><span class="sxs-lookup"><span data-stu-id="f6b2d-199">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="f6b2d-200">**Numero di rete duplicato**</span><span class="sxs-lookup"><span data-stu-id="f6b2d-200">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="f6b2d-201">89</span><span class="sxs-lookup"><span data-stu-id="f6b2d-201">89</span></span>

<span data-ttu-id="f6b2d-202">Numero di rete duplicato.</span><span class="sxs-lookup"><span data-stu-id="f6b2d-202">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="f6b2d-203">**Parametro fuori limite**</span><span class="sxs-lookup"><span data-stu-id="f6b2d-203">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="f6b2d-204">90</span><span class="sxs-lookup"><span data-stu-id="f6b2d-204">90</span></span>

<span data-ttu-id="f6b2d-205">Parametro fuori limite.</span><span class="sxs-lookup"><span data-stu-id="f6b2d-205">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="f6b2d-206">**Accesso negato**</span><span class="sxs-lookup"><span data-stu-id="f6b2d-206">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="f6b2d-207">91</span><span class="sxs-lookup"><span data-stu-id="f6b2d-207">91</span></span>

<span data-ttu-id="f6b2d-208">Accesso negato.</span><span class="sxs-lookup"><span data-stu-id="f6b2d-208">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="f6b2d-209">**Memoria insufficiente**</span><span class="sxs-lookup"><span data-stu-id="f6b2d-209">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="f6b2d-210">92</span><span class="sxs-lookup"><span data-stu-id="f6b2d-210">92</span></span>

<span data-ttu-id="f6b2d-211">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="f6b2d-211">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="f6b2d-212">**Esiste già**</span><span class="sxs-lookup"><span data-stu-id="f6b2d-212">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="f6b2d-213">93</span><span class="sxs-lookup"><span data-stu-id="f6b2d-213">93</span></span>

<span data-ttu-id="f6b2d-214">Esiste già.</span><span class="sxs-lookup"><span data-stu-id="f6b2d-214">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="f6b2d-215">**Percorso, file o oggetto non trovato**</span><span class="sxs-lookup"><span data-stu-id="f6b2d-215">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="f6b2d-216">94</span><span class="sxs-lookup"><span data-stu-id="f6b2d-216">94</span></span>

<span data-ttu-id="f6b2d-217">Il percorso, il file o l'oggetto non è stato trovato.</span><span class="sxs-lookup"><span data-stu-id="f6b2d-217">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="f6b2d-218">**Non è possibile inviare una notifica al servizio**</span><span class="sxs-lookup"><span data-stu-id="f6b2d-218">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="f6b2d-219">95</span><span class="sxs-lookup"><span data-stu-id="f6b2d-219">95</span></span>

<span data-ttu-id="f6b2d-220">Impossibile notificare il servizio.</span><span class="sxs-lookup"><span data-stu-id="f6b2d-220">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="f6b2d-221">**Non è possibile inviare una notifica al servizio DNS**</span><span class="sxs-lookup"><span data-stu-id="f6b2d-221">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="f6b2d-222">96</span><span class="sxs-lookup"><span data-stu-id="f6b2d-222">96</span></span>

<span data-ttu-id="f6b2d-223">Impossibile inviare una notifica al servizio DNS.</span><span class="sxs-lookup"><span data-stu-id="f6b2d-223">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="f6b2d-224">**Interfaccia non configurabile**</span><span class="sxs-lookup"><span data-stu-id="f6b2d-224">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="f6b2d-225">97</span><span class="sxs-lookup"><span data-stu-id="f6b2d-225">97</span></span>

<span data-ttu-id="f6b2d-226">Interfaccia non configurabile.</span><span class="sxs-lookup"><span data-stu-id="f6b2d-226">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="f6b2d-227">**Non tutti i lease DHCP possono essere rilasciati/rinnovati**</span><span class="sxs-lookup"><span data-stu-id="f6b2d-227">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="f6b2d-228">98</span><span class="sxs-lookup"><span data-stu-id="f6b2d-228">98</span></span>

<span data-ttu-id="f6b2d-229">Non tutti i lease DHCP possono essere rilasciati o rinnovati.</span><span class="sxs-lookup"><span data-stu-id="f6b2d-229">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="f6b2d-230">**DHCP non abilitato sull'adapter**</span><span class="sxs-lookup"><span data-stu-id="f6b2d-230">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="f6b2d-231">100</span><span class="sxs-lookup"><span data-stu-id="f6b2d-231">100</span></span>

<span data-ttu-id="f6b2d-232">DHCP non abilitato sulla scheda.</span><span class="sxs-lookup"><span data-stu-id="f6b2d-232">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="f6b2d-233">**Altri**</span><span class="sxs-lookup"><span data-stu-id="f6b2d-233">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="f6b2d-234">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="f6b2d-234">101 4294967295</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="f6b2d-235">Esempio</span><span class="sxs-lookup"><span data-stu-id="f6b2d-235">Examples</span></span>

<span data-ttu-id="f6b2d-236">L'esempio [modificare la metrica della connessione IP per una scheda di rete](https://Gallery.TechNet.Microsoft.Com/73367c75-7a39-44dc-a8d7-eb2359030969) VBScript imposta la metrica di connessione IP per una scheda di rete su 100.</span><span class="sxs-lookup"><span data-stu-id="f6b2d-236">The [Modify the IP Connection Metric for a Network Adapter](https://Gallery.TechNet.Microsoft.Com/73367c75-7a39-44dc-a8d7-eb2359030969) VBScript sample sets the IP connection metric for a network adapter to 100.</span></span>

## <a name="requirements"></a><span data-ttu-id="f6b2d-237">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f6b2d-237">Requirements</span></span>



| <span data-ttu-id="f6b2d-238">Requisito</span><span class="sxs-lookup"><span data-stu-id="f6b2d-238">Requirement</span></span> | <span data-ttu-id="f6b2d-239">Valore</span><span class="sxs-lookup"><span data-stu-id="f6b2d-239">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f6b2d-240">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f6b2d-240">Minimum supported client</span></span><br/> | <span data-ttu-id="f6b2d-241">Windows Vista, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f6b2d-241">Windows Vista, Windows Vista</span></span><br/>                                                 |
| <span data-ttu-id="f6b2d-242">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f6b2d-242">Minimum supported server</span></span><br/> | <span data-ttu-id="f6b2d-243">Windows Server 2008, Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f6b2d-243">Windows Server 2008, Windows Server 2008</span></span><br/>                                     |
| <span data-ttu-id="f6b2d-244">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f6b2d-244">Namespace</span></span><br/>                | <span data-ttu-id="f6b2d-245">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="f6b2d-245">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f6b2d-246">MOF</span><span class="sxs-lookup"><span data-stu-id="f6b2d-246">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f6b2d-247"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f6b2d-247"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f6b2d-248">DLL</span><span class="sxs-lookup"><span data-stu-id="f6b2d-248">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f6b2d-249"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f6b2d-249"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f6b2d-250">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f6b2d-250">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6b2d-251">Classi hardware del sistema del computer</span><span class="sxs-lookup"><span data-stu-id="f6b2d-251">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="f6b2d-252">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="f6b2d-252">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="f6b2d-253">Attività WMI: rete</span><span class="sxs-lookup"><span data-stu-id="f6b2d-253">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="f6b2d-254">Attività WMI: account e domini</span><span class="sxs-lookup"><span data-stu-id="f6b2d-254">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="f6b2d-255">Supporto di IPv6 e IPv4 in WMI</span><span class="sxs-lookup"><span data-stu-id="f6b2d-255">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

