---
description: Il metodo statico della classe WMI SetPMTUDiscovery viene usato per abilitare l'individuazione dell'unità di trasmissione massima (MTU) nel percorso di un host remoto.
ms.assetid: 43c640bb-c4e7-4b4b-9c18-6cc426229954
ms.tgt_platform: multiple
title: Metodo SetPMTUDiscovery della classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetPMTUDiscovery
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: ef3bc9ad5d6203077275f3665c4b0efc98265fbe
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748562"
---
# <a name="setpmtudiscovery-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="72d6e-103">Metodo SetPMTUDiscovery della \_ classe NetworkAdapterConfiguration Win32</span><span class="sxs-lookup"><span data-stu-id="72d6e-103">SetPMTUDiscovery method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="72d6e-104">Il metodo statico della [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetPMTUDiscovery** viene usato per abilitare l'individuazione dell'unità di trasmissione massima (MTU) nel percorso di un host remoto.</span><span class="sxs-lookup"><span data-stu-id="72d6e-104">The **SetPMTUDiscovery** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to enable Maximum Transmission Unit (MTU) discovery over the path to a remote host.</span></span>

<span data-ttu-id="72d6e-105">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="72d6e-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="72d6e-106">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="72d6e-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="72d6e-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="72d6e-107">Syntax</span></span>


```mof
uint32 SetPMTUDiscovery(
  [in] boolean PMTUDiscoveryEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="72d6e-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="72d6e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="72d6e-109">*PMTUDiscoveryEnabled consente* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="72d6e-109">*PMTUDiscoveryEnabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72d6e-110">Se **true**, il protocollo TCP è abilitato per tentare di individuare l'unità di trasmissione massima (MTU) o le dimensioni del pacchetto più grande rispetto al percorso di un host remoto.</span><span class="sxs-lookup"><span data-stu-id="72d6e-110">If **true**, TCP is enabled to attempt to discover the Maximum Transmission Unit (MTU) or largest packet size over the path to a remote host.</span></span> <span data-ttu-id="72d6e-111">Il valore predefinito è **True**.</span><span class="sxs-lookup"><span data-stu-id="72d6e-111">The default is **true**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="72d6e-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="72d6e-112">Return value</span></span>

<span data-ttu-id="72d6e-113">Restituisce un valore pari a 0 (zero) per un completamento corretto quando non è richiesto il riavvio, 1 (uno) per un completamento corretto quando è necessario un riavvio e un numero diverso se si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="72d6e-113">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="72d6e-114">Per ulteriori informazioni sui codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="72d6e-114">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="72d6e-115">Per i valori **HRESULT** generali, vedere [codici di errore di sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="72d6e-115">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="72d6e-116">**Operazione completata, non è necessario riavviare il computer**</span><span class="sxs-lookup"><span data-stu-id="72d6e-116">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="72d6e-117">0</span><span class="sxs-lookup"><span data-stu-id="72d6e-117">0</span></span>

<span data-ttu-id="72d6e-118">Operazione completata, non è necessario riavviare il computer.</span><span class="sxs-lookup"><span data-stu-id="72d6e-118">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="72d6e-119">**Operazione completata, riavvio richiesto**</span><span class="sxs-lookup"><span data-stu-id="72d6e-119">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="72d6e-120">1</span><span class="sxs-lookup"><span data-stu-id="72d6e-120">1</span></span>

<span data-ttu-id="72d6e-121">Operazione completata, è necessario riavviare il computer.</span><span class="sxs-lookup"><span data-stu-id="72d6e-121">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="72d6e-122">**Metodo non supportato in questa piattaforma**</span><span class="sxs-lookup"><span data-stu-id="72d6e-122">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="72d6e-123">64</span><span class="sxs-lookup"><span data-stu-id="72d6e-123">64</span></span>

<span data-ttu-id="72d6e-124">Metodo non supportato in questa piattaforma.</span><span class="sxs-lookup"><span data-stu-id="72d6e-124">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="72d6e-125">**Errore sconosciuto**</span><span class="sxs-lookup"><span data-stu-id="72d6e-125">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="72d6e-126">65</span><span class="sxs-lookup"><span data-stu-id="72d6e-126">65</span></span>

<span data-ttu-id="72d6e-127">Errore sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="72d6e-127">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="72d6e-128">**subnet mask non valido**</span><span class="sxs-lookup"><span data-stu-id="72d6e-128">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="72d6e-129">66</span><span class="sxs-lookup"><span data-stu-id="72d6e-129">66</span></span>

<span data-ttu-id="72d6e-130">Subnet mask non valido.</span><span class="sxs-lookup"><span data-stu-id="72d6e-130">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="72d6e-131">**Si è verificato un errore durante l'elaborazione di un'istanza restituita**</span><span class="sxs-lookup"><span data-stu-id="72d6e-131">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="72d6e-132">67</span><span class="sxs-lookup"><span data-stu-id="72d6e-132">67</span></span>

<span data-ttu-id="72d6e-133">Si è verificato un errore durante l'elaborazione di un'istanza di restituita.</span><span class="sxs-lookup"><span data-stu-id="72d6e-133">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="72d6e-134">**Parametro di input non valido**</span><span class="sxs-lookup"><span data-stu-id="72d6e-134">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="72d6e-135">68</span><span class="sxs-lookup"><span data-stu-id="72d6e-135">68</span></span>

<span data-ttu-id="72d6e-136">Parametro di input non valido.</span><span class="sxs-lookup"><span data-stu-id="72d6e-136">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="72d6e-137">**Sono stati specificati più di 5 gateway**</span><span class="sxs-lookup"><span data-stu-id="72d6e-137">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="72d6e-138">69</span><span class="sxs-lookup"><span data-stu-id="72d6e-138">69</span></span>

<span data-ttu-id="72d6e-139">Sono stati specificati più di cinque gateway.</span><span class="sxs-lookup"><span data-stu-id="72d6e-139">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="72d6e-140">**Indirizzo IP non valido**</span><span class="sxs-lookup"><span data-stu-id="72d6e-140">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="72d6e-141">70</span><span class="sxs-lookup"><span data-stu-id="72d6e-141">70</span></span>

<span data-ttu-id="72d6e-142">Indirizzo IP non valido.</span><span class="sxs-lookup"><span data-stu-id="72d6e-142">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="72d6e-143">**Indirizzo IP gateway non valido**</span><span class="sxs-lookup"><span data-stu-id="72d6e-143">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="72d6e-144">71</span><span class="sxs-lookup"><span data-stu-id="72d6e-144">71</span></span>

<span data-ttu-id="72d6e-145">Indirizzo IP del gateway non valido.</span><span class="sxs-lookup"><span data-stu-id="72d6e-145">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="72d6e-146">**Si è verificato un errore durante l'accesso al registro di sistema per le informazioni richieste**</span><span class="sxs-lookup"><span data-stu-id="72d6e-146">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="72d6e-147">72</span><span class="sxs-lookup"><span data-stu-id="72d6e-147">72</span></span>

<span data-ttu-id="72d6e-148">Si è verificato un errore durante l'accesso al registro di sistema per le informazioni richieste.</span><span class="sxs-lookup"><span data-stu-id="72d6e-148">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="72d6e-149">**Nome di dominio non valido**</span><span class="sxs-lookup"><span data-stu-id="72d6e-149">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="72d6e-150">73</span><span class="sxs-lookup"><span data-stu-id="72d6e-150">73</span></span>

<span data-ttu-id="72d6e-151">Nome di dominio non valido.</span><span class="sxs-lookup"><span data-stu-id="72d6e-151">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="72d6e-152">**Nome host non valido**</span><span class="sxs-lookup"><span data-stu-id="72d6e-152">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="72d6e-153">74</span><span class="sxs-lookup"><span data-stu-id="72d6e-153">74</span></span>

<span data-ttu-id="72d6e-154">Nome host non valido.</span><span class="sxs-lookup"><span data-stu-id="72d6e-154">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="72d6e-155">**Nessun server WINS primario/secondario definito**</span><span class="sxs-lookup"><span data-stu-id="72d6e-155">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="72d6e-156">75</span><span class="sxs-lookup"><span data-stu-id="72d6e-156">75</span></span>

<span data-ttu-id="72d6e-157">Nessun server WINS primario o secondario definito.</span><span class="sxs-lookup"><span data-stu-id="72d6e-157">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="72d6e-158">**File non valido**</span><span class="sxs-lookup"><span data-stu-id="72d6e-158">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="72d6e-159">76</span><span class="sxs-lookup"><span data-stu-id="72d6e-159">76</span></span>

<span data-ttu-id="72d6e-160">File non valido.</span><span class="sxs-lookup"><span data-stu-id="72d6e-160">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="72d6e-161">**Percorso di sistema non valido**</span><span class="sxs-lookup"><span data-stu-id="72d6e-161">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="72d6e-162">77</span><span class="sxs-lookup"><span data-stu-id="72d6e-162">77</span></span>

<span data-ttu-id="72d6e-163">Percorso di sistema non valido.</span><span class="sxs-lookup"><span data-stu-id="72d6e-163">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="72d6e-164">**Copia del file non riuscita**</span><span class="sxs-lookup"><span data-stu-id="72d6e-164">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="72d6e-165">78</span><span class="sxs-lookup"><span data-stu-id="72d6e-165">78</span></span>

<span data-ttu-id="72d6e-166">Copia del file non riuscita.</span><span class="sxs-lookup"><span data-stu-id="72d6e-166">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="72d6e-167">**Parametro di sicurezza non valido**</span><span class="sxs-lookup"><span data-stu-id="72d6e-167">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="72d6e-168">79</span><span class="sxs-lookup"><span data-stu-id="72d6e-168">79</span></span>

<span data-ttu-id="72d6e-169">Parametro di sicurezza non valido.</span><span class="sxs-lookup"><span data-stu-id="72d6e-169">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="72d6e-170">**Impossibile configurare il servizio TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="72d6e-170">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="72d6e-171">80</span><span class="sxs-lookup"><span data-stu-id="72d6e-171">80</span></span>

<span data-ttu-id="72d6e-172">Impossibile configurare il servizio TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="72d6e-172">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="72d6e-173">**Non è possibile configurare il servizio DHCP**</span><span class="sxs-lookup"><span data-stu-id="72d6e-173">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="72d6e-174">81</span><span class="sxs-lookup"><span data-stu-id="72d6e-174">81</span></span>

<span data-ttu-id="72d6e-175">Impossibile configurare il servizio DHCP.</span><span class="sxs-lookup"><span data-stu-id="72d6e-175">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="72d6e-176">**Non è possibile rinnovare il lease DHCP**</span><span class="sxs-lookup"><span data-stu-id="72d6e-176">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="72d6e-177">82</span><span class="sxs-lookup"><span data-stu-id="72d6e-177">82</span></span>

<span data-ttu-id="72d6e-178">Non è possibile rinnovare il lease DHCP.</span><span class="sxs-lookup"><span data-stu-id="72d6e-178">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="72d6e-179">**Non è possibile rilasciare il lease DHCP**</span><span class="sxs-lookup"><span data-stu-id="72d6e-179">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="72d6e-180">83</span><span class="sxs-lookup"><span data-stu-id="72d6e-180">83</span></span>

<span data-ttu-id="72d6e-181">Impossibile rilasciare il lease DHCP.</span><span class="sxs-lookup"><span data-stu-id="72d6e-181">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="72d6e-182">**IP non abilitato sulla scheda**</span><span class="sxs-lookup"><span data-stu-id="72d6e-182">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="72d6e-183">84</span><span class="sxs-lookup"><span data-stu-id="72d6e-183">84</span></span>

<span data-ttu-id="72d6e-184">IP non abilitato sulla scheda.</span><span class="sxs-lookup"><span data-stu-id="72d6e-184">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="72d6e-185">**IPX non abilitato sull'adapter**</span><span class="sxs-lookup"><span data-stu-id="72d6e-185">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="72d6e-186">85</span><span class="sxs-lookup"><span data-stu-id="72d6e-186">85</span></span>

<span data-ttu-id="72d6e-187">IPX non abilitato sulla scheda.</span><span class="sxs-lookup"><span data-stu-id="72d6e-187">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="72d6e-188">**Errore limite numero frame/rete**</span><span class="sxs-lookup"><span data-stu-id="72d6e-188">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="72d6e-189">86</span><span class="sxs-lookup"><span data-stu-id="72d6e-189">86</span></span>

<span data-ttu-id="72d6e-190">Errore dei limiti del numero di rete o del frame.</span><span class="sxs-lookup"><span data-stu-id="72d6e-190">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="72d6e-191">**Tipo di frame non valido**</span><span class="sxs-lookup"><span data-stu-id="72d6e-191">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="72d6e-192">87</span><span class="sxs-lookup"><span data-stu-id="72d6e-192">87</span></span>

<span data-ttu-id="72d6e-193">Tipo di frame non valido.</span><span class="sxs-lookup"><span data-stu-id="72d6e-193">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="72d6e-194">**Numero di rete non valido**</span><span class="sxs-lookup"><span data-stu-id="72d6e-194">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="72d6e-195">88</span><span class="sxs-lookup"><span data-stu-id="72d6e-195">88</span></span>

<span data-ttu-id="72d6e-196">Numero di rete non valido.</span><span class="sxs-lookup"><span data-stu-id="72d6e-196">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="72d6e-197">**Numero di rete duplicato**</span><span class="sxs-lookup"><span data-stu-id="72d6e-197">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="72d6e-198">89</span><span class="sxs-lookup"><span data-stu-id="72d6e-198">89</span></span>

<span data-ttu-id="72d6e-199">Numero di rete duplicato.</span><span class="sxs-lookup"><span data-stu-id="72d6e-199">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="72d6e-200">**Parametro fuori limite**</span><span class="sxs-lookup"><span data-stu-id="72d6e-200">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="72d6e-201">90</span><span class="sxs-lookup"><span data-stu-id="72d6e-201">90</span></span>

<span data-ttu-id="72d6e-202">Parametro fuori limite.</span><span class="sxs-lookup"><span data-stu-id="72d6e-202">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="72d6e-203">**Accesso negato**</span><span class="sxs-lookup"><span data-stu-id="72d6e-203">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="72d6e-204">91</span><span class="sxs-lookup"><span data-stu-id="72d6e-204">91</span></span>

<span data-ttu-id="72d6e-205">Accesso negato.</span><span class="sxs-lookup"><span data-stu-id="72d6e-205">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="72d6e-206">**Memoria insufficiente**</span><span class="sxs-lookup"><span data-stu-id="72d6e-206">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="72d6e-207">92</span><span class="sxs-lookup"><span data-stu-id="72d6e-207">92</span></span>

<span data-ttu-id="72d6e-208">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="72d6e-208">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="72d6e-209">**Esiste già**</span><span class="sxs-lookup"><span data-stu-id="72d6e-209">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="72d6e-210">93</span><span class="sxs-lookup"><span data-stu-id="72d6e-210">93</span></span>

<span data-ttu-id="72d6e-211">Esiste già.</span><span class="sxs-lookup"><span data-stu-id="72d6e-211">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="72d6e-212">**Percorso, file o oggetto non trovato**</span><span class="sxs-lookup"><span data-stu-id="72d6e-212">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="72d6e-213">94</span><span class="sxs-lookup"><span data-stu-id="72d6e-213">94</span></span>

<span data-ttu-id="72d6e-214">Il percorso, il file o l'oggetto non è stato trovato.</span><span class="sxs-lookup"><span data-stu-id="72d6e-214">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="72d6e-215">**Non è possibile inviare una notifica al servizio**</span><span class="sxs-lookup"><span data-stu-id="72d6e-215">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="72d6e-216">95</span><span class="sxs-lookup"><span data-stu-id="72d6e-216">95</span></span>

<span data-ttu-id="72d6e-217">Impossibile notificare il servizio.</span><span class="sxs-lookup"><span data-stu-id="72d6e-217">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="72d6e-218">**Non è possibile inviare una notifica al servizio DNS**</span><span class="sxs-lookup"><span data-stu-id="72d6e-218">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="72d6e-219">96</span><span class="sxs-lookup"><span data-stu-id="72d6e-219">96</span></span>

<span data-ttu-id="72d6e-220">Impossibile inviare una notifica al servizio DNS.</span><span class="sxs-lookup"><span data-stu-id="72d6e-220">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="72d6e-221">**Interfaccia non configurabile**</span><span class="sxs-lookup"><span data-stu-id="72d6e-221">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="72d6e-222">97</span><span class="sxs-lookup"><span data-stu-id="72d6e-222">97</span></span>

<span data-ttu-id="72d6e-223">Interfaccia non configurabile.</span><span class="sxs-lookup"><span data-stu-id="72d6e-223">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="72d6e-224">**Non tutti i lease DHCP possono essere rilasciati/rinnovati**</span><span class="sxs-lookup"><span data-stu-id="72d6e-224">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="72d6e-225">98</span><span class="sxs-lookup"><span data-stu-id="72d6e-225">98</span></span>

<span data-ttu-id="72d6e-226">Non tutti i lease DHCP possono essere rilasciati o rinnovati.</span><span class="sxs-lookup"><span data-stu-id="72d6e-226">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="72d6e-227">**DHCP non abilitato sull'adapter**</span><span class="sxs-lookup"><span data-stu-id="72d6e-227">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="72d6e-228">100</span><span class="sxs-lookup"><span data-stu-id="72d6e-228">100</span></span>

<span data-ttu-id="72d6e-229">DHCP non abilitato sulla scheda.</span><span class="sxs-lookup"><span data-stu-id="72d6e-229">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="72d6e-230">**Altri**</span><span class="sxs-lookup"><span data-stu-id="72d6e-230">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="72d6e-231">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="72d6e-231">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="72d6e-232">Commenti</span><span class="sxs-lookup"><span data-stu-id="72d6e-232">Remarks</span></span>

<span data-ttu-id="72d6e-233">Se si individua il percorso MTU e si limitano i segmenti TCP a questa dimensione, TCP può eliminare la frammentazione nei router lungo il percorso che connette le reti con MTU diversi.</span><span class="sxs-lookup"><span data-stu-id="72d6e-233">By discovering the Path MTU and limiting TCP segments to this size, TCP can eliminate fragmentation at routers along the path that connect networks with different MTUs.</span></span> <span data-ttu-id="72d6e-234">La frammentazione influisce negativamente sulla velocità effettiva TCP e sulla congestione della rete.</span><span class="sxs-lookup"><span data-stu-id="72d6e-234">Fragmentation adversely affects TCP throughput and network congestion.</span></span> <span data-ttu-id="72d6e-235">Impostando questo parametro su **false** , viene usato un MTU di 576 byte per tutte le connessioni che non sono computer nella subnet locale</span><span class="sxs-lookup"><span data-stu-id="72d6e-235">Setting this parameter to **FALSE** causes an MTU of 576 bytes to be used for all connections that are not to machines on the local subnet</span></span>

## <a name="examples"></a><span data-ttu-id="72d6e-236">Esempio</span><span class="sxs-lookup"><span data-stu-id="72d6e-236">Examples</span></span>

<span data-ttu-id="72d6e-237">L'esempio [Enable PMTU Discovery on all Network Adapters](https://Gallery.TechNet.Microsoft.Com/dd68dc8d-d452-484c-add7-2da5c87c3568) VBScript consente a un computer di individuare automaticamente l'unità di trasmissione massima in una rete.</span><span class="sxs-lookup"><span data-stu-id="72d6e-237">The [Enable PMTU Discovery on all Network Adapters](https://Gallery.TechNet.Microsoft.Com/dd68dc8d-d452-484c-add7-2da5c87c3568) VBScript sample enables a computer to automatically discover the maximum transmission unit on a network.</span></span>

## <a name="requirements"></a><span data-ttu-id="72d6e-238">Requisiti</span><span class="sxs-lookup"><span data-stu-id="72d6e-238">Requirements</span></span>



| <span data-ttu-id="72d6e-239">Requisito</span><span class="sxs-lookup"><span data-stu-id="72d6e-239">Requirement</span></span> | <span data-ttu-id="72d6e-240">Valore</span><span class="sxs-lookup"><span data-stu-id="72d6e-240">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="72d6e-241">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="72d6e-241">Minimum supported client</span></span><br/> | <span data-ttu-id="72d6e-242">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="72d6e-242">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="72d6e-243">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="72d6e-243">Minimum supported server</span></span><br/> | <span data-ttu-id="72d6e-244">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="72d6e-244">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="72d6e-245">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="72d6e-245">Namespace</span></span><br/>                | <span data-ttu-id="72d6e-246">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="72d6e-246">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="72d6e-247">MOF</span><span class="sxs-lookup"><span data-stu-id="72d6e-247">MOF</span></span><br/>                      | <dl> <span data-ttu-id="72d6e-248"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="72d6e-248"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="72d6e-249">DLL</span><span class="sxs-lookup"><span data-stu-id="72d6e-249">DLL</span></span><br/>                      | <dl> <span data-ttu-id="72d6e-250"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="72d6e-250"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72d6e-251">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="72d6e-251">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72d6e-252">Classi hardware del sistema del computer</span><span class="sxs-lookup"><span data-stu-id="72d6e-252">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="72d6e-253">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="72d6e-253">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="72d6e-254">Attività WMI: rete</span><span class="sxs-lookup"><span data-stu-id="72d6e-254">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="72d6e-255">Attività WMI: account e domini</span><span class="sxs-lookup"><span data-stu-id="72d6e-255">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="72d6e-256">Supporto di IPv6 e IPv4 in WMI</span><span class="sxs-lookup"><span data-stu-id="72d6e-256">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

