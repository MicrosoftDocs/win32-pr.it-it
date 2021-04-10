---
description: Il metodo statico della classe WMI SetPMTUBHDetect viene usato per abilitare il rilevamento di router black hole durante l'individuazione del percorso MTU.
ms.assetid: a1e45ed9-85a9-4fdd-890a-d578c3f94b72
ms.tgt_platform: multiple
title: Metodo SetPMTUBHDetect della classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetPMTUBHDetect
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 098652c6ea0a53f9d3b1f616def3dd8b5e7228af
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127058"
---
# <a name="setpmtubhdetect-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="f564b-103">Metodo SetPMTUBHDetect della \_ classe NetworkAdapterConfiguration Win32</span><span class="sxs-lookup"><span data-stu-id="f564b-103">SetPMTUBHDetect method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="f564b-104">Il metodo statico della [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetPMTUBHDetect** viene usato per abilitare il rilevamento di router black hole durante l'individuazione del percorso MTU.</span><span class="sxs-lookup"><span data-stu-id="f564b-104">The **SetPMTUBHDetect** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to enable the detection of Black Hole routers while doing Path MTU Discovery.</span></span>

<span data-ttu-id="f564b-105">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="f564b-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="f564b-106">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="f564b-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="f564b-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f564b-107">Syntax</span></span>


```mof
uint32 SetPMTUBHDetect(
  [in] boolean PMTUBHDetectEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="f564b-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="f564b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f564b-109">*PMTUBHDetectEnabled* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f564b-109">*PMTUBHDetectEnabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f564b-110">Se **true**, il protocollo TCP tenta di individuare il Black Hole e di indirizzare i pacchetti in percorsi di rete diversi.</span><span class="sxs-lookup"><span data-stu-id="f564b-110">If **true**, TCP attempts to discover Black Hole and route packets in different network paths.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f564b-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f564b-111">Return value</span></span>

<span data-ttu-id="f564b-112">Restituisce un valore pari a 0 (zero) per un completamento corretto quando non è richiesto il riavvio, 1 (uno) per un completamento corretto quando è necessario un riavvio e un numero diverso se si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="f564b-112">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="f564b-113">Per ulteriori informazioni sui codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="f564b-113">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="f564b-114">Per i valori **HRESULT** generali, vedere [codici di errore di sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="f564b-114">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="f564b-115">**Operazione completata, non è necessario riavviare il computer**</span><span class="sxs-lookup"><span data-stu-id="f564b-115">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="f564b-116">0</span><span class="sxs-lookup"><span data-stu-id="f564b-116">0</span></span>

<span data-ttu-id="f564b-117">Operazione completata, non è necessario riavviare il computer.</span><span class="sxs-lookup"><span data-stu-id="f564b-117">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="f564b-118">**Operazione completata, riavvio richiesto**</span><span class="sxs-lookup"><span data-stu-id="f564b-118">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="f564b-119">1</span><span class="sxs-lookup"><span data-stu-id="f564b-119">1</span></span>

<span data-ttu-id="f564b-120">Operazione completata, è necessario riavviare il computer.</span><span class="sxs-lookup"><span data-stu-id="f564b-120">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="f564b-121">**Metodo non supportato in questa piattaforma**</span><span class="sxs-lookup"><span data-stu-id="f564b-121">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="f564b-122">64</span><span class="sxs-lookup"><span data-stu-id="f564b-122">64</span></span>

<span data-ttu-id="f564b-123">Metodo non supportato in questa piattaforma.</span><span class="sxs-lookup"><span data-stu-id="f564b-123">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="f564b-124">**Errore sconosciuto**</span><span class="sxs-lookup"><span data-stu-id="f564b-124">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="f564b-125">65</span><span class="sxs-lookup"><span data-stu-id="f564b-125">65</span></span>

<span data-ttu-id="f564b-126">Errore sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="f564b-126">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="f564b-127">**subnet mask non valido**</span><span class="sxs-lookup"><span data-stu-id="f564b-127">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="f564b-128">66</span><span class="sxs-lookup"><span data-stu-id="f564b-128">66</span></span>

<span data-ttu-id="f564b-129">Subnet mask non valido.</span><span class="sxs-lookup"><span data-stu-id="f564b-129">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="f564b-130">**Si è verificato un errore durante l'elaborazione di un'istanza restituita**</span><span class="sxs-lookup"><span data-stu-id="f564b-130">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="f564b-131">67</span><span class="sxs-lookup"><span data-stu-id="f564b-131">67</span></span>

<span data-ttu-id="f564b-132">Si è verificato un errore durante l'elaborazione di un'istanza di restituita.</span><span class="sxs-lookup"><span data-stu-id="f564b-132">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="f564b-133">**Parametro di input non valido**</span><span class="sxs-lookup"><span data-stu-id="f564b-133">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="f564b-134">68</span><span class="sxs-lookup"><span data-stu-id="f564b-134">68</span></span>

<span data-ttu-id="f564b-135">Parametro di input non valido.</span><span class="sxs-lookup"><span data-stu-id="f564b-135">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="f564b-136">**Sono stati specificati più di 5 gateway**</span><span class="sxs-lookup"><span data-stu-id="f564b-136">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="f564b-137">69</span><span class="sxs-lookup"><span data-stu-id="f564b-137">69</span></span>

<span data-ttu-id="f564b-138">Sono stati specificati più di cinque gateway.</span><span class="sxs-lookup"><span data-stu-id="f564b-138">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="f564b-139">**Indirizzo IP non valido**</span><span class="sxs-lookup"><span data-stu-id="f564b-139">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="f564b-140">70</span><span class="sxs-lookup"><span data-stu-id="f564b-140">70</span></span>

<span data-ttu-id="f564b-141">Indirizzo IP non valido.</span><span class="sxs-lookup"><span data-stu-id="f564b-141">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="f564b-142">**Indirizzo IP gateway non valido**</span><span class="sxs-lookup"><span data-stu-id="f564b-142">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="f564b-143">71</span><span class="sxs-lookup"><span data-stu-id="f564b-143">71</span></span>

<span data-ttu-id="f564b-144">Indirizzo IP del gateway non valido.</span><span class="sxs-lookup"><span data-stu-id="f564b-144">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="f564b-145">**Si è verificato un errore durante l'accesso al registro di sistema per le informazioni richieste**</span><span class="sxs-lookup"><span data-stu-id="f564b-145">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="f564b-146">72</span><span class="sxs-lookup"><span data-stu-id="f564b-146">72</span></span>

<span data-ttu-id="f564b-147">Si è verificato un errore durante l'accesso al registro di sistema per le informazioni richieste.</span><span class="sxs-lookup"><span data-stu-id="f564b-147">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="f564b-148">**Nome di dominio non valido**</span><span class="sxs-lookup"><span data-stu-id="f564b-148">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="f564b-149">73</span><span class="sxs-lookup"><span data-stu-id="f564b-149">73</span></span>

<span data-ttu-id="f564b-150">Nome di dominio non valido.</span><span class="sxs-lookup"><span data-stu-id="f564b-150">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="f564b-151">**Nome host non valido**</span><span class="sxs-lookup"><span data-stu-id="f564b-151">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="f564b-152">74</span><span class="sxs-lookup"><span data-stu-id="f564b-152">74</span></span>

<span data-ttu-id="f564b-153">Nome host non valido.</span><span class="sxs-lookup"><span data-stu-id="f564b-153">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="f564b-154">**Nessun server WINS primario/secondario definito**</span><span class="sxs-lookup"><span data-stu-id="f564b-154">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="f564b-155">75</span><span class="sxs-lookup"><span data-stu-id="f564b-155">75</span></span>

<span data-ttu-id="f564b-156">Nessun server WINS primario o secondario definito.</span><span class="sxs-lookup"><span data-stu-id="f564b-156">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="f564b-157">**File non valido**</span><span class="sxs-lookup"><span data-stu-id="f564b-157">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="f564b-158">76</span><span class="sxs-lookup"><span data-stu-id="f564b-158">76</span></span>

<span data-ttu-id="f564b-159">File non valido.</span><span class="sxs-lookup"><span data-stu-id="f564b-159">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="f564b-160">**Percorso di sistema non valido**</span><span class="sxs-lookup"><span data-stu-id="f564b-160">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="f564b-161">77</span><span class="sxs-lookup"><span data-stu-id="f564b-161">77</span></span>

<span data-ttu-id="f564b-162">Percorso di sistema non valido.</span><span class="sxs-lookup"><span data-stu-id="f564b-162">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="f564b-163">**Copia del file non riuscita**</span><span class="sxs-lookup"><span data-stu-id="f564b-163">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="f564b-164">78</span><span class="sxs-lookup"><span data-stu-id="f564b-164">78</span></span>

<span data-ttu-id="f564b-165">Copia del file non riuscita.</span><span class="sxs-lookup"><span data-stu-id="f564b-165">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="f564b-166">**Parametro di sicurezza non valido**</span><span class="sxs-lookup"><span data-stu-id="f564b-166">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="f564b-167">79</span><span class="sxs-lookup"><span data-stu-id="f564b-167">79</span></span>

<span data-ttu-id="f564b-168">Parametro di sicurezza non valido.</span><span class="sxs-lookup"><span data-stu-id="f564b-168">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="f564b-169">**Impossibile configurare il servizio TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="f564b-169">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="f564b-170">80</span><span class="sxs-lookup"><span data-stu-id="f564b-170">80</span></span>

<span data-ttu-id="f564b-171">Impossibile configurare il servizio TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="f564b-171">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="f564b-172">**Non è possibile configurare il servizio DHCP**</span><span class="sxs-lookup"><span data-stu-id="f564b-172">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="f564b-173">81</span><span class="sxs-lookup"><span data-stu-id="f564b-173">81</span></span>

<span data-ttu-id="f564b-174">Impossibile configurare il servizio DHCP.</span><span class="sxs-lookup"><span data-stu-id="f564b-174">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="f564b-175">**Non è possibile rinnovare il lease DHCP**</span><span class="sxs-lookup"><span data-stu-id="f564b-175">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="f564b-176">82</span><span class="sxs-lookup"><span data-stu-id="f564b-176">82</span></span>

<span data-ttu-id="f564b-177">Non è possibile rinnovare il lease DHCP.</span><span class="sxs-lookup"><span data-stu-id="f564b-177">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="f564b-178">**Non è possibile rilasciare il lease DHCP**</span><span class="sxs-lookup"><span data-stu-id="f564b-178">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="f564b-179">83</span><span class="sxs-lookup"><span data-stu-id="f564b-179">83</span></span>

<span data-ttu-id="f564b-180">Impossibile rilasciare il lease DHCP.</span><span class="sxs-lookup"><span data-stu-id="f564b-180">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="f564b-181">**IP non abilitato sulla scheda**</span><span class="sxs-lookup"><span data-stu-id="f564b-181">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="f564b-182">84</span><span class="sxs-lookup"><span data-stu-id="f564b-182">84</span></span>

<span data-ttu-id="f564b-183">IP non abilitato sulla scheda.</span><span class="sxs-lookup"><span data-stu-id="f564b-183">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="f564b-184">**IPX non abilitato sull'adapter**</span><span class="sxs-lookup"><span data-stu-id="f564b-184">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="f564b-185">85</span><span class="sxs-lookup"><span data-stu-id="f564b-185">85</span></span>

<span data-ttu-id="f564b-186">IPX non abilitato sulla scheda.</span><span class="sxs-lookup"><span data-stu-id="f564b-186">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="f564b-187">**Errore limite numero frame/rete**</span><span class="sxs-lookup"><span data-stu-id="f564b-187">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="f564b-188">86</span><span class="sxs-lookup"><span data-stu-id="f564b-188">86</span></span>

<span data-ttu-id="f564b-189">Errore dei limiti del numero di rete o del frame.</span><span class="sxs-lookup"><span data-stu-id="f564b-189">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="f564b-190">**Tipo di frame non valido**</span><span class="sxs-lookup"><span data-stu-id="f564b-190">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="f564b-191">87</span><span class="sxs-lookup"><span data-stu-id="f564b-191">87</span></span>

<span data-ttu-id="f564b-192">Tipo di frame non valido.</span><span class="sxs-lookup"><span data-stu-id="f564b-192">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="f564b-193">**Numero di rete non valido**</span><span class="sxs-lookup"><span data-stu-id="f564b-193">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="f564b-194">88</span><span class="sxs-lookup"><span data-stu-id="f564b-194">88</span></span>

<span data-ttu-id="f564b-195">Numero di rete non valido.</span><span class="sxs-lookup"><span data-stu-id="f564b-195">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="f564b-196">**Numero di rete duplicato**</span><span class="sxs-lookup"><span data-stu-id="f564b-196">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="f564b-197">89</span><span class="sxs-lookup"><span data-stu-id="f564b-197">89</span></span>

<span data-ttu-id="f564b-198">Numero di rete duplicato.</span><span class="sxs-lookup"><span data-stu-id="f564b-198">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="f564b-199">**Parametro fuori limite**</span><span class="sxs-lookup"><span data-stu-id="f564b-199">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="f564b-200">90</span><span class="sxs-lookup"><span data-stu-id="f564b-200">90</span></span>

<span data-ttu-id="f564b-201">Parametro fuori limite.</span><span class="sxs-lookup"><span data-stu-id="f564b-201">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="f564b-202">**Accesso negato**</span><span class="sxs-lookup"><span data-stu-id="f564b-202">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="f564b-203">91</span><span class="sxs-lookup"><span data-stu-id="f564b-203">91</span></span>

<span data-ttu-id="f564b-204">Accesso negato.</span><span class="sxs-lookup"><span data-stu-id="f564b-204">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="f564b-205">**Memoria insufficiente**</span><span class="sxs-lookup"><span data-stu-id="f564b-205">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="f564b-206">92</span><span class="sxs-lookup"><span data-stu-id="f564b-206">92</span></span>

<span data-ttu-id="f564b-207">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="f564b-207">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="f564b-208">**Esiste già**</span><span class="sxs-lookup"><span data-stu-id="f564b-208">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="f564b-209">93</span><span class="sxs-lookup"><span data-stu-id="f564b-209">93</span></span>

<span data-ttu-id="f564b-210">Esiste già.</span><span class="sxs-lookup"><span data-stu-id="f564b-210">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="f564b-211">**Percorso, file o oggetto non trovato**</span><span class="sxs-lookup"><span data-stu-id="f564b-211">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="f564b-212">94</span><span class="sxs-lookup"><span data-stu-id="f564b-212">94</span></span>

<span data-ttu-id="f564b-213">Il percorso, il file o l'oggetto non è stato trovato.</span><span class="sxs-lookup"><span data-stu-id="f564b-213">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="f564b-214">**Non è possibile inviare una notifica al servizio**</span><span class="sxs-lookup"><span data-stu-id="f564b-214">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="f564b-215">95</span><span class="sxs-lookup"><span data-stu-id="f564b-215">95</span></span>

<span data-ttu-id="f564b-216">Impossibile notificare il servizio.</span><span class="sxs-lookup"><span data-stu-id="f564b-216">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="f564b-217">**Non è possibile inviare una notifica al servizio DNS**</span><span class="sxs-lookup"><span data-stu-id="f564b-217">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="f564b-218">96</span><span class="sxs-lookup"><span data-stu-id="f564b-218">96</span></span>

<span data-ttu-id="f564b-219">Impossibile inviare una notifica al servizio DNS.</span><span class="sxs-lookup"><span data-stu-id="f564b-219">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="f564b-220">**Interfaccia non configurabile**</span><span class="sxs-lookup"><span data-stu-id="f564b-220">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="f564b-221">97</span><span class="sxs-lookup"><span data-stu-id="f564b-221">97</span></span>

<span data-ttu-id="f564b-222">Interfaccia non configurabile.</span><span class="sxs-lookup"><span data-stu-id="f564b-222">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="f564b-223">**Non tutti i lease DHCP possono essere rilasciati/rinnovati**</span><span class="sxs-lookup"><span data-stu-id="f564b-223">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="f564b-224">98</span><span class="sxs-lookup"><span data-stu-id="f564b-224">98</span></span>

<span data-ttu-id="f564b-225">Non tutti i lease DHCP possono essere rilasciati o rinnovati.</span><span class="sxs-lookup"><span data-stu-id="f564b-225">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="f564b-226">**DHCP non abilitato sull'adapter**</span><span class="sxs-lookup"><span data-stu-id="f564b-226">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="f564b-227">100</span><span class="sxs-lookup"><span data-stu-id="f564b-227">100</span></span>

<span data-ttu-id="f564b-228">DHCP non abilitato sulla scheda.</span><span class="sxs-lookup"><span data-stu-id="f564b-228">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="f564b-229">**Altri**</span><span class="sxs-lookup"><span data-stu-id="f564b-229">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="f564b-230">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="f564b-230">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f564b-231">Commenti</span><span class="sxs-lookup"><span data-stu-id="f564b-231">Remarks</span></span>

<span data-ttu-id="f564b-232">Un router black hole non restituisce i messaggi non raggiungibili della destinazione di Internet Control Message Protocol (ICMP) quando è necessario frammentare un datagramma IP con il bit not Fragment impostato.</span><span class="sxs-lookup"><span data-stu-id="f564b-232">A Black Hole router does not return the Internet Control Message Protocol (ICMP) Destination Unreachable messages when it needs to fragment an IP datagram with the Don't Fragment bit set.</span></span> <span data-ttu-id="f564b-233">TCP dipende dalla ricezione di questi messaggi per l'esecuzione dell'individuazione MTU del percorso.</span><span class="sxs-lookup"><span data-stu-id="f564b-233">TCP depends on receiving these messages to perform Path MTU Discovery.</span></span>

<span data-ttu-id="f564b-234">Se questa funzionalità è abilitata, TCP tenterà di inviare segmenti senza il bit non frammento impostato se diverse ritrasmissioni di un segmento non vengono riconosciute.</span><span class="sxs-lookup"><span data-stu-id="f564b-234">With this feature enabled, TCP will try to send segments without the Don't Fragment bit set if several retransmissions of a segment go unacknowledged.</span></span> <span data-ttu-id="f564b-235">Se il segmento viene riconosciuto come risultato, la dimensione massima del segmento (MSS) verrà ridotta e il bit not Fragment verrà impostato in pacchetti futuri sulla connessione.</span><span class="sxs-lookup"><span data-stu-id="f564b-235">If the segment is acknowledged as a result, the maximum segment size (MSS) will be decreased and the Don't Fragment bit will be set in future packets on the connection.</span></span> <span data-ttu-id="f564b-236">L'abilitazione del rilevamento di buchi neri aumenta il numero massimo di ritrasmissioni eseguite per un determinato segmento.</span><span class="sxs-lookup"><span data-stu-id="f564b-236">Enabling black hole detection increases the maximum number of retransmissions performed for a given segment.</span></span>

## <a name="examples"></a><span data-ttu-id="f564b-237">Esempio</span><span class="sxs-lookup"><span data-stu-id="f564b-237">Examples</span></span>

<span data-ttu-id="f564b-238">Il [rilevamento delle modifiche APrilevamento pmtubhte su tutte le schede di rete](https://Gallery.TechNet.Microsoft.Com/a576d97b-38fe-437e-a632-d2f7e122301c) consente l'individuazione automatica dei router black hole quando si determina l'unità di trasmissione massima in una rete.</span><span class="sxs-lookup"><span data-stu-id="f564b-238">The [Modify PMTUBH Detection on All Network Adapters](https://Gallery.TechNet.Microsoft.Com/a576d97b-38fe-437e-a632-d2f7e122301c) enables the auto-discovery of black hole routers when determining the maximum transmission unit on a network.</span></span>

## <a name="requirements"></a><span data-ttu-id="f564b-239">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f564b-239">Requirements</span></span>



| <span data-ttu-id="f564b-240">Requisito</span><span class="sxs-lookup"><span data-stu-id="f564b-240">Requirement</span></span> | <span data-ttu-id="f564b-241">Valore</span><span class="sxs-lookup"><span data-stu-id="f564b-241">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f564b-242">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f564b-242">Minimum supported client</span></span><br/> | <span data-ttu-id="f564b-243">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f564b-243">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f564b-244">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f564b-244">Minimum supported server</span></span><br/> | <span data-ttu-id="f564b-245">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f564b-245">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f564b-246">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f564b-246">Namespace</span></span><br/>                | <span data-ttu-id="f564b-247">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="f564b-247">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f564b-248">MOF</span><span class="sxs-lookup"><span data-stu-id="f564b-248">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f564b-249"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f564b-249"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f564b-250">DLL</span><span class="sxs-lookup"><span data-stu-id="f564b-250">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f564b-251"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f564b-251"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f564b-252">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f564b-252">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f564b-253">Classi hardware del sistema del computer</span><span class="sxs-lookup"><span data-stu-id="f564b-253">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="f564b-254">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="f564b-254">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="f564b-255">Attività WMI: rete</span><span class="sxs-lookup"><span data-stu-id="f564b-255">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="f564b-256">Attività WMI: account e domini</span><span class="sxs-lookup"><span data-stu-id="f564b-256">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="f564b-257">Supporto di IPv6 e IPv4 in WMI</span><span class="sxs-lookup"><span data-stu-id="f564b-257">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

