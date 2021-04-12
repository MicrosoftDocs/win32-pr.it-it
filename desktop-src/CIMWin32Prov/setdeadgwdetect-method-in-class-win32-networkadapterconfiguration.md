---
description: Il metodo statico della classe WMI SetDeadGWDetect viene usato per abilitare il rilevamento del gateway non attivo.
ms.assetid: c813aaef-7215-4759-b68f-7808fd203d9c
ms.tgt_platform: multiple
title: Metodo SetDeadGWDetect della classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetDeadGWDetect
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 83f62d84af193be99850f1a82b720a2983ca77c3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104482988"
---
# <a name="setdeadgwdetect-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="4d8af-103">Metodo SetDeadGWDetect della \_ classe NetworkAdapterConfiguration Win32</span><span class="sxs-lookup"><span data-stu-id="4d8af-103">SetDeadGWDetect method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="4d8af-104">Il metodo statico della [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetDeadGWDetect** viene usato per abilitare il rilevamento del gateway non attivo.</span><span class="sxs-lookup"><span data-stu-id="4d8af-104">The **SetDeadGWDetect** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to enable dead gateway detection.</span></span>

<span data-ttu-id="4d8af-105">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="4d8af-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="4d8af-106">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="4d8af-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="4d8af-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4d8af-107">Syntax</span></span>


```mof
uint32 SetDeadGWDetect(
  [in] boolean DeadGWDetectEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="4d8af-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="4d8af-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d8af-109">*DeadGWDetectEnabled* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4d8af-109">*DeadGWDetectEnabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d8af-110">Se **true**, è necessario abilitare il rilevamento del gateway inattivo.</span><span class="sxs-lookup"><span data-stu-id="4d8af-110">If **true**, dead gateway detection should be enabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4d8af-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4d8af-111">Return value</span></span>

<span data-ttu-id="4d8af-112">Restituisce un valore pari a 0 (zero) per un completamento corretto quando non è richiesto il riavvio, 1 (uno) per un completamento corretto quando è necessario un riavvio e un numero diverso se si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="4d8af-112">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="4d8af-113">Per ulteriori informazioni sui codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="4d8af-113">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="4d8af-114">Per i valori **HRESULT** generali, vedere [codici di errore di sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="4d8af-114">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="4d8af-115">**Operazione completata, non è necessario riavviare il computer**</span><span class="sxs-lookup"><span data-stu-id="4d8af-115">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="4d8af-116">0</span><span class="sxs-lookup"><span data-stu-id="4d8af-116">0</span></span>

<span data-ttu-id="4d8af-117">Operazione completata, non è necessario riavviare il computer.</span><span class="sxs-lookup"><span data-stu-id="4d8af-117">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="4d8af-118">**Operazione completata, riavvio richiesto**</span><span class="sxs-lookup"><span data-stu-id="4d8af-118">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="4d8af-119">1</span><span class="sxs-lookup"><span data-stu-id="4d8af-119">1</span></span>

<span data-ttu-id="4d8af-120">Operazione completata, è necessario riavviare il computer.</span><span class="sxs-lookup"><span data-stu-id="4d8af-120">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="4d8af-121">**Metodo non supportato in questa piattaforma**</span><span class="sxs-lookup"><span data-stu-id="4d8af-121">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="4d8af-122">64</span><span class="sxs-lookup"><span data-stu-id="4d8af-122">64</span></span>

<span data-ttu-id="4d8af-123">Metodo non supportato in questa piattaforma.</span><span class="sxs-lookup"><span data-stu-id="4d8af-123">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="4d8af-124">**Errore sconosciuto**</span><span class="sxs-lookup"><span data-stu-id="4d8af-124">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="4d8af-125">65</span><span class="sxs-lookup"><span data-stu-id="4d8af-125">65</span></span>

<span data-ttu-id="4d8af-126">Errore sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="4d8af-126">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="4d8af-127">**subnet mask non valido**</span><span class="sxs-lookup"><span data-stu-id="4d8af-127">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="4d8af-128">66</span><span class="sxs-lookup"><span data-stu-id="4d8af-128">66</span></span>

<span data-ttu-id="4d8af-129">Subnet mask non valido.</span><span class="sxs-lookup"><span data-stu-id="4d8af-129">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="4d8af-130">**Si è verificato un errore durante l'elaborazione di un'istanza restituita**</span><span class="sxs-lookup"><span data-stu-id="4d8af-130">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="4d8af-131">67</span><span class="sxs-lookup"><span data-stu-id="4d8af-131">67</span></span>

<span data-ttu-id="4d8af-132">Si è verificato un errore durante l'elaborazione di un'istanza di restituita.</span><span class="sxs-lookup"><span data-stu-id="4d8af-132">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="4d8af-133">**Parametro di input non valido**</span><span class="sxs-lookup"><span data-stu-id="4d8af-133">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="4d8af-134">68</span><span class="sxs-lookup"><span data-stu-id="4d8af-134">68</span></span>

<span data-ttu-id="4d8af-135">Parametro di input non valido.</span><span class="sxs-lookup"><span data-stu-id="4d8af-135">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="4d8af-136">**Sono stati specificati più di 5 gateway**</span><span class="sxs-lookup"><span data-stu-id="4d8af-136">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="4d8af-137">69</span><span class="sxs-lookup"><span data-stu-id="4d8af-137">69</span></span>

<span data-ttu-id="4d8af-138">Sono stati specificati più di cinque gateway.</span><span class="sxs-lookup"><span data-stu-id="4d8af-138">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="4d8af-139">**Indirizzo IP non valido**</span><span class="sxs-lookup"><span data-stu-id="4d8af-139">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="4d8af-140">70</span><span class="sxs-lookup"><span data-stu-id="4d8af-140">70</span></span>

<span data-ttu-id="4d8af-141">Indirizzo IP non valido.</span><span class="sxs-lookup"><span data-stu-id="4d8af-141">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="4d8af-142">**Indirizzo IP gateway non valido**</span><span class="sxs-lookup"><span data-stu-id="4d8af-142">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="4d8af-143">71</span><span class="sxs-lookup"><span data-stu-id="4d8af-143">71</span></span>

<span data-ttu-id="4d8af-144">Indirizzo IP del gateway non valido.</span><span class="sxs-lookup"><span data-stu-id="4d8af-144">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="4d8af-145">**Si è verificato un errore durante l'accesso al registro di sistema per le informazioni richieste**</span><span class="sxs-lookup"><span data-stu-id="4d8af-145">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="4d8af-146">72</span><span class="sxs-lookup"><span data-stu-id="4d8af-146">72</span></span>

<span data-ttu-id="4d8af-147">Si è verificato un errore durante l'accesso al registro di sistema per le informazioni richieste.</span><span class="sxs-lookup"><span data-stu-id="4d8af-147">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="4d8af-148">**Nome di dominio non valido**</span><span class="sxs-lookup"><span data-stu-id="4d8af-148">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="4d8af-149">73</span><span class="sxs-lookup"><span data-stu-id="4d8af-149">73</span></span>

<span data-ttu-id="4d8af-150">Nome di dominio non valido.</span><span class="sxs-lookup"><span data-stu-id="4d8af-150">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="4d8af-151">**Nome host non valido**</span><span class="sxs-lookup"><span data-stu-id="4d8af-151">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="4d8af-152">74</span><span class="sxs-lookup"><span data-stu-id="4d8af-152">74</span></span>

<span data-ttu-id="4d8af-153">Nome host non valido.</span><span class="sxs-lookup"><span data-stu-id="4d8af-153">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="4d8af-154">**Nessun server WINS primario/secondario definito**</span><span class="sxs-lookup"><span data-stu-id="4d8af-154">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="4d8af-155">75</span><span class="sxs-lookup"><span data-stu-id="4d8af-155">75</span></span>

<span data-ttu-id="4d8af-156">Nessun server WINS primario o secondario definito.</span><span class="sxs-lookup"><span data-stu-id="4d8af-156">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="4d8af-157">**File non valido**</span><span class="sxs-lookup"><span data-stu-id="4d8af-157">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="4d8af-158">76</span><span class="sxs-lookup"><span data-stu-id="4d8af-158">76</span></span>

<span data-ttu-id="4d8af-159">File non valido.</span><span class="sxs-lookup"><span data-stu-id="4d8af-159">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="4d8af-160">**Percorso di sistema non valido**</span><span class="sxs-lookup"><span data-stu-id="4d8af-160">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="4d8af-161">77</span><span class="sxs-lookup"><span data-stu-id="4d8af-161">77</span></span>

<span data-ttu-id="4d8af-162">Percorso di sistema non valido.</span><span class="sxs-lookup"><span data-stu-id="4d8af-162">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="4d8af-163">**Copia del file non riuscita**</span><span class="sxs-lookup"><span data-stu-id="4d8af-163">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="4d8af-164">78</span><span class="sxs-lookup"><span data-stu-id="4d8af-164">78</span></span>

<span data-ttu-id="4d8af-165">Copia del file non riuscita.</span><span class="sxs-lookup"><span data-stu-id="4d8af-165">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="4d8af-166">**Parametro di sicurezza non valido**</span><span class="sxs-lookup"><span data-stu-id="4d8af-166">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="4d8af-167">79</span><span class="sxs-lookup"><span data-stu-id="4d8af-167">79</span></span>

<span data-ttu-id="4d8af-168">Parametro di sicurezza non valido.</span><span class="sxs-lookup"><span data-stu-id="4d8af-168">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="4d8af-169">**Impossibile configurare il servizio TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="4d8af-169">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="4d8af-170">80</span><span class="sxs-lookup"><span data-stu-id="4d8af-170">80</span></span>

<span data-ttu-id="4d8af-171">Impossibile configurare il servizio TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="4d8af-171">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="4d8af-172">**Non è possibile configurare il servizio DHCP**</span><span class="sxs-lookup"><span data-stu-id="4d8af-172">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="4d8af-173">81</span><span class="sxs-lookup"><span data-stu-id="4d8af-173">81</span></span>

<span data-ttu-id="4d8af-174">Impossibile configurare il servizio DHCP.</span><span class="sxs-lookup"><span data-stu-id="4d8af-174">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="4d8af-175">**Non è possibile rinnovare il lease DHCP**</span><span class="sxs-lookup"><span data-stu-id="4d8af-175">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="4d8af-176">82</span><span class="sxs-lookup"><span data-stu-id="4d8af-176">82</span></span>

<span data-ttu-id="4d8af-177">Non è possibile rinnovare il lease DHCP.</span><span class="sxs-lookup"><span data-stu-id="4d8af-177">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="4d8af-178">**Non è possibile rilasciare il lease DHCP**</span><span class="sxs-lookup"><span data-stu-id="4d8af-178">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="4d8af-179">83</span><span class="sxs-lookup"><span data-stu-id="4d8af-179">83</span></span>

<span data-ttu-id="4d8af-180">Impossibile rilasciare il lease DHCP.</span><span class="sxs-lookup"><span data-stu-id="4d8af-180">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="4d8af-181">**IP non abilitato sulla scheda**</span><span class="sxs-lookup"><span data-stu-id="4d8af-181">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="4d8af-182">84</span><span class="sxs-lookup"><span data-stu-id="4d8af-182">84</span></span>

<span data-ttu-id="4d8af-183">IP non abilitato sulla scheda.</span><span class="sxs-lookup"><span data-stu-id="4d8af-183">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="4d8af-184">**IPX non abilitato sull'adapter**</span><span class="sxs-lookup"><span data-stu-id="4d8af-184">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="4d8af-185">85</span><span class="sxs-lookup"><span data-stu-id="4d8af-185">85</span></span>

<span data-ttu-id="4d8af-186">IPX non abilitato sulla scheda.</span><span class="sxs-lookup"><span data-stu-id="4d8af-186">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="4d8af-187">**Errore limite numero frame/rete**</span><span class="sxs-lookup"><span data-stu-id="4d8af-187">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="4d8af-188">86</span><span class="sxs-lookup"><span data-stu-id="4d8af-188">86</span></span>

<span data-ttu-id="4d8af-189">Errore dei limiti del numero di rete o del frame.</span><span class="sxs-lookup"><span data-stu-id="4d8af-189">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="4d8af-190">**Tipo di frame non valido**</span><span class="sxs-lookup"><span data-stu-id="4d8af-190">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="4d8af-191">87</span><span class="sxs-lookup"><span data-stu-id="4d8af-191">87</span></span>

<span data-ttu-id="4d8af-192">Tipo di frame non valido.</span><span class="sxs-lookup"><span data-stu-id="4d8af-192">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="4d8af-193">**Numero di rete non valido**</span><span class="sxs-lookup"><span data-stu-id="4d8af-193">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="4d8af-194">88</span><span class="sxs-lookup"><span data-stu-id="4d8af-194">88</span></span>

<span data-ttu-id="4d8af-195">Numero di rete non valido.</span><span class="sxs-lookup"><span data-stu-id="4d8af-195">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="4d8af-196">**Numero di rete duplicato**</span><span class="sxs-lookup"><span data-stu-id="4d8af-196">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="4d8af-197">89</span><span class="sxs-lookup"><span data-stu-id="4d8af-197">89</span></span>

<span data-ttu-id="4d8af-198">Numero di rete duplicato.</span><span class="sxs-lookup"><span data-stu-id="4d8af-198">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="4d8af-199">**Parametro fuori limite**</span><span class="sxs-lookup"><span data-stu-id="4d8af-199">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="4d8af-200">90</span><span class="sxs-lookup"><span data-stu-id="4d8af-200">90</span></span>

<span data-ttu-id="4d8af-201">Parametro fuori limite.</span><span class="sxs-lookup"><span data-stu-id="4d8af-201">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="4d8af-202">**Accesso negato**</span><span class="sxs-lookup"><span data-stu-id="4d8af-202">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="4d8af-203">91</span><span class="sxs-lookup"><span data-stu-id="4d8af-203">91</span></span>

<span data-ttu-id="4d8af-204">Accesso negato.</span><span class="sxs-lookup"><span data-stu-id="4d8af-204">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="4d8af-205">**Memoria insufficiente**</span><span class="sxs-lookup"><span data-stu-id="4d8af-205">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="4d8af-206">92</span><span class="sxs-lookup"><span data-stu-id="4d8af-206">92</span></span>

<span data-ttu-id="4d8af-207">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="4d8af-207">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="4d8af-208">**Esiste già**</span><span class="sxs-lookup"><span data-stu-id="4d8af-208">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="4d8af-209">93</span><span class="sxs-lookup"><span data-stu-id="4d8af-209">93</span></span>

<span data-ttu-id="4d8af-210">Esiste già.</span><span class="sxs-lookup"><span data-stu-id="4d8af-210">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="4d8af-211">**Percorso, file o oggetto non trovato**</span><span class="sxs-lookup"><span data-stu-id="4d8af-211">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="4d8af-212">94</span><span class="sxs-lookup"><span data-stu-id="4d8af-212">94</span></span>

<span data-ttu-id="4d8af-213">Il percorso, il file o l'oggetto non è stato trovato.</span><span class="sxs-lookup"><span data-stu-id="4d8af-213">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="4d8af-214">**Non è possibile inviare una notifica al servizio**</span><span class="sxs-lookup"><span data-stu-id="4d8af-214">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="4d8af-215">95</span><span class="sxs-lookup"><span data-stu-id="4d8af-215">95</span></span>

<span data-ttu-id="4d8af-216">Impossibile notificare il servizio.</span><span class="sxs-lookup"><span data-stu-id="4d8af-216">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="4d8af-217">**Non è possibile inviare una notifica al servizio DNS**</span><span class="sxs-lookup"><span data-stu-id="4d8af-217">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="4d8af-218">96</span><span class="sxs-lookup"><span data-stu-id="4d8af-218">96</span></span>

<span data-ttu-id="4d8af-219">Impossibile inviare una notifica al servizio DNS.</span><span class="sxs-lookup"><span data-stu-id="4d8af-219">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="4d8af-220">**Interfaccia non configurabile**</span><span class="sxs-lookup"><span data-stu-id="4d8af-220">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="4d8af-221">97</span><span class="sxs-lookup"><span data-stu-id="4d8af-221">97</span></span>

<span data-ttu-id="4d8af-222">Interfaccia non configurabile.</span><span class="sxs-lookup"><span data-stu-id="4d8af-222">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="4d8af-223">**Non tutti i lease DHCP possono essere rilasciati/rinnovati**</span><span class="sxs-lookup"><span data-stu-id="4d8af-223">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="4d8af-224">98</span><span class="sxs-lookup"><span data-stu-id="4d8af-224">98</span></span>

<span data-ttu-id="4d8af-225">Non tutti i lease DHCP possono essere rilasciati o rinnovati.</span><span class="sxs-lookup"><span data-stu-id="4d8af-225">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="4d8af-226">**DHCP non abilitato sull'adapter**</span><span class="sxs-lookup"><span data-stu-id="4d8af-226">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="4d8af-227">100</span><span class="sxs-lookup"><span data-stu-id="4d8af-227">100</span></span>

<span data-ttu-id="4d8af-228">DHCP non abilitato sulla scheda.</span><span class="sxs-lookup"><span data-stu-id="4d8af-228">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="4d8af-229">**Altri**</span><span class="sxs-lookup"><span data-stu-id="4d8af-229">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="4d8af-230">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="4d8af-230">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4d8af-231">Commenti</span><span class="sxs-lookup"><span data-stu-id="4d8af-231">Remarks</span></span>

<span data-ttu-id="4d8af-232">Se questa funzionalità è abilitata, TCP chiede all'IP di passare a un gateway di backup se ritrasmette un segmento più volte senza ricevere una risposta.</span><span class="sxs-lookup"><span data-stu-id="4d8af-232">With this feature enabled, TCP asks IP to change to a backup gateway if it retransmits a segment several times without receiving a response.</span></span>

## <a name="examples"></a><span data-ttu-id="4d8af-233">Esempio</span><span class="sxs-lookup"><span data-stu-id="4d8af-233">Examples</span></span>

<span data-ttu-id="4d8af-234">L'esempio per l' [Abilitazione del rilevamento di gateway non recapitabili per tutte le schede di rete](https://Gallery.TechNet.Microsoft.Com/4a24b080-1a8b-4085-9419-58d096ef8437) in TechNet Gallery USA **SetDeadGWDetect** per configurare tutte le schede di rete in un computer per rilevare automaticamente i gateway inattivi.</span><span class="sxs-lookup"><span data-stu-id="4d8af-234">The [Enable Dead Gateway Detection for All Network Adapters](https://Gallery.TechNet.Microsoft.Com/4a24b080-1a8b-4085-9419-58d096ef8437) VBScript sample on TechNet Gallery uses **SetDeadGWDetect** to configure all network adapters on a computer to automatically detect dead gateways.</span></span>

## <a name="requirements"></a><span data-ttu-id="4d8af-235">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4d8af-235">Requirements</span></span>



| <span data-ttu-id="4d8af-236">Requisito</span><span class="sxs-lookup"><span data-stu-id="4d8af-236">Requirement</span></span> | <span data-ttu-id="4d8af-237">Valore</span><span class="sxs-lookup"><span data-stu-id="4d8af-237">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4d8af-238">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4d8af-238">Minimum supported client</span></span><br/> | <span data-ttu-id="4d8af-239">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4d8af-239">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4d8af-240">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4d8af-240">Minimum supported server</span></span><br/> | <span data-ttu-id="4d8af-241">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4d8af-241">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4d8af-242">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="4d8af-242">Namespace</span></span><br/>                | <span data-ttu-id="4d8af-243">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="4d8af-243">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="4d8af-244">MOF</span><span class="sxs-lookup"><span data-stu-id="4d8af-244">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4d8af-245"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4d8af-245"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="4d8af-246">DLL</span><span class="sxs-lookup"><span data-stu-id="4d8af-246">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4d8af-247"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4d8af-247"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4d8af-248">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4d8af-248">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d8af-249">Classi hardware del sistema del computer</span><span class="sxs-lookup"><span data-stu-id="4d8af-249">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="4d8af-250">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="4d8af-250">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="4d8af-251">Attività WMI: rete</span><span class="sxs-lookup"><span data-stu-id="4d8af-251">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="4d8af-252">Attività WMI: account e domini</span><span class="sxs-lookup"><span data-stu-id="4d8af-252">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="4d8af-253">Supporto di IPv6 e IPv4 in WMI</span><span class="sxs-lookup"><span data-stu-id="4d8af-253">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

