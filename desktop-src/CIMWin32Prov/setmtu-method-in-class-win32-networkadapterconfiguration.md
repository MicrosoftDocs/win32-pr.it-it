---
description: Il metodo statico della classe WMI SetMTU viene usato per impostare l'unità di trasmissione massima (MTU) predefinita per un'interfaccia di rete.
ms.assetid: 262c8bd7-1057-4204-80ab-725c60fc9c52
ms.tgt_platform: multiple
title: Metodo SetMTU della classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetMTU
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 466c344892f2c4bf4a1e979ac9c1f50cd709325a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748570"
---
# <a name="setmtu-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="2fa39-103">Metodo SetMTU della \_ classe NetworkAdapterConfiguration Win32</span><span class="sxs-lookup"><span data-stu-id="2fa39-103">SetMTU method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="2fa39-104">Il metodo statico della [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetMTU** viene usato per impostare l'unità di trasmissione massima (MTU) predefinita per un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="2fa39-104">The **SetMTU** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to set the default Maximum Transmission Unit (MTU) for a network interface.</span></span>

<span data-ttu-id="2fa39-105">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="2fa39-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="2fa39-106">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="2fa39-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="2fa39-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2fa39-107">Syntax</span></span>


```mof
uint32 SetMTU(
  [in] uint32 MTU
);
```



## <a name="parameters"></a><span data-ttu-id="2fa39-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="2fa39-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2fa39-109">*MTU* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2fa39-109">*MTU* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2fa39-110">Unità di trasmissione massima (MTU) predefinita per un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="2fa39-110">Default Maximum Transmission Unit (MTU) for a network interface.</span></span> <span data-ttu-id="2fa39-111">L'intervallo di questo valore si estende alla dimensione minima del pacchetto (68) al valore MTU supportato dalla rete sottostante.</span><span class="sxs-lookup"><span data-stu-id="2fa39-111">The range of this value spans the minimum packet size (68) to the MTU supported by the underlying network.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2fa39-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2fa39-112">Return value</span></span>

<span data-ttu-id="2fa39-113">Restituisce un valore pari a 0 (zero) per un completamento corretto quando non è richiesto il riavvio, 1 (uno) per un completamento corretto quando è necessario un riavvio e un numero diverso se si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="2fa39-113">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="2fa39-114">Per ulteriori informazioni sui codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="2fa39-114">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="2fa39-115">Per i valori **HRESULT** generali, vedere [codici di errore di sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="2fa39-115">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="2fa39-116">**Operazione completata, non è necessario riavviare il computer**</span><span class="sxs-lookup"><span data-stu-id="2fa39-116">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="2fa39-117">0</span><span class="sxs-lookup"><span data-stu-id="2fa39-117">0</span></span>

<span data-ttu-id="2fa39-118">Operazione completata.</span><span class="sxs-lookup"><span data-stu-id="2fa39-118">Successful completion.</span></span> <span data-ttu-id="2fa39-119">Non è necessario riavviare il computer.</span><span class="sxs-lookup"><span data-stu-id="2fa39-119">No reboot is required.</span></span>

</dd> <dt>

<span data-ttu-id="2fa39-120">**Operazione completata, riavvio richiesto**</span><span class="sxs-lookup"><span data-stu-id="2fa39-120">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="2fa39-121">1</span><span class="sxs-lookup"><span data-stu-id="2fa39-121">1</span></span>

<span data-ttu-id="2fa39-122">Operazione completata.</span><span class="sxs-lookup"><span data-stu-id="2fa39-122">Successful completion.</span></span> <span data-ttu-id="2fa39-123">È necessario un riavvio.</span><span class="sxs-lookup"><span data-stu-id="2fa39-123">Reboot is required.</span></span>

</dd> <dt>

<span data-ttu-id="2fa39-124">**Metodo non supportato in questa piattaforma**</span><span class="sxs-lookup"><span data-stu-id="2fa39-124">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="2fa39-125">64</span><span class="sxs-lookup"><span data-stu-id="2fa39-125">64</span></span>

<span data-ttu-id="2fa39-126">Metodo non supportato in questa piattaforma.</span><span class="sxs-lookup"><span data-stu-id="2fa39-126">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="2fa39-127">**Errore sconosciuto**</span><span class="sxs-lookup"><span data-stu-id="2fa39-127">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="2fa39-128">65</span><span class="sxs-lookup"><span data-stu-id="2fa39-128">65</span></span>

<span data-ttu-id="2fa39-129">Errore sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="2fa39-129">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="2fa39-130">**subnet mask non valido**</span><span class="sxs-lookup"><span data-stu-id="2fa39-130">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="2fa39-131">66</span><span class="sxs-lookup"><span data-stu-id="2fa39-131">66</span></span>

<span data-ttu-id="2fa39-132">Subnet mask non valido.</span><span class="sxs-lookup"><span data-stu-id="2fa39-132">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="2fa39-133">**Si è verificato un errore durante l'elaborazione di un'istanza restituita**</span><span class="sxs-lookup"><span data-stu-id="2fa39-133">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="2fa39-134">67</span><span class="sxs-lookup"><span data-stu-id="2fa39-134">67</span></span>

<span data-ttu-id="2fa39-135">Si è verificato un errore durante l'elaborazione di un'istanza di restituita.</span><span class="sxs-lookup"><span data-stu-id="2fa39-135">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="2fa39-136">**Parametro di input non valido**</span><span class="sxs-lookup"><span data-stu-id="2fa39-136">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="2fa39-137">68</span><span class="sxs-lookup"><span data-stu-id="2fa39-137">68</span></span>

<span data-ttu-id="2fa39-138">Parametro di input non valido.</span><span class="sxs-lookup"><span data-stu-id="2fa39-138">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="2fa39-139">**Sono stati specificati più di 5 gateway**</span><span class="sxs-lookup"><span data-stu-id="2fa39-139">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="2fa39-140">69</span><span class="sxs-lookup"><span data-stu-id="2fa39-140">69</span></span>

<span data-ttu-id="2fa39-141">Sono stati specificati più di cinque gateway.</span><span class="sxs-lookup"><span data-stu-id="2fa39-141">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="2fa39-142">**Indirizzo IP non valido**</span><span class="sxs-lookup"><span data-stu-id="2fa39-142">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="2fa39-143">70</span><span class="sxs-lookup"><span data-stu-id="2fa39-143">70</span></span>

<span data-ttu-id="2fa39-144">Indirizzo IP non valido.</span><span class="sxs-lookup"><span data-stu-id="2fa39-144">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="2fa39-145">**Indirizzo IP gateway non valido**</span><span class="sxs-lookup"><span data-stu-id="2fa39-145">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="2fa39-146">71</span><span class="sxs-lookup"><span data-stu-id="2fa39-146">71</span></span>

<span data-ttu-id="2fa39-147">Indirizzo IP del gateway non valido.</span><span class="sxs-lookup"><span data-stu-id="2fa39-147">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="2fa39-148">**Si è verificato un errore durante l'accesso al registro di sistema per le informazioni richieste**</span><span class="sxs-lookup"><span data-stu-id="2fa39-148">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="2fa39-149">72</span><span class="sxs-lookup"><span data-stu-id="2fa39-149">72</span></span>

<span data-ttu-id="2fa39-150">Si è verificato un errore durante l'accesso al registro di sistema per le informazioni richieste.</span><span class="sxs-lookup"><span data-stu-id="2fa39-150">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="2fa39-151">**Nome di dominio non valido**</span><span class="sxs-lookup"><span data-stu-id="2fa39-151">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="2fa39-152">73</span><span class="sxs-lookup"><span data-stu-id="2fa39-152">73</span></span>

<span data-ttu-id="2fa39-153">Nome di dominio non valido.</span><span class="sxs-lookup"><span data-stu-id="2fa39-153">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="2fa39-154">**Nome host non valido**</span><span class="sxs-lookup"><span data-stu-id="2fa39-154">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="2fa39-155">74</span><span class="sxs-lookup"><span data-stu-id="2fa39-155">74</span></span>

<span data-ttu-id="2fa39-156">Nome host non valido.</span><span class="sxs-lookup"><span data-stu-id="2fa39-156">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="2fa39-157">**Nessun server WINS primario/secondario definito**</span><span class="sxs-lookup"><span data-stu-id="2fa39-157">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="2fa39-158">75</span><span class="sxs-lookup"><span data-stu-id="2fa39-158">75</span></span>

<span data-ttu-id="2fa39-159">Nessun server WINS primario o secondario definito.</span><span class="sxs-lookup"><span data-stu-id="2fa39-159">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="2fa39-160">**File non valido**</span><span class="sxs-lookup"><span data-stu-id="2fa39-160">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="2fa39-161">76</span><span class="sxs-lookup"><span data-stu-id="2fa39-161">76</span></span>

<span data-ttu-id="2fa39-162">File non valido.</span><span class="sxs-lookup"><span data-stu-id="2fa39-162">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="2fa39-163">**Percorso di sistema non valido**</span><span class="sxs-lookup"><span data-stu-id="2fa39-163">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="2fa39-164">77</span><span class="sxs-lookup"><span data-stu-id="2fa39-164">77</span></span>

<span data-ttu-id="2fa39-165">Percorso di sistema non valido.</span><span class="sxs-lookup"><span data-stu-id="2fa39-165">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="2fa39-166">**Copia del file non riuscita**</span><span class="sxs-lookup"><span data-stu-id="2fa39-166">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="2fa39-167">78</span><span class="sxs-lookup"><span data-stu-id="2fa39-167">78</span></span>

<span data-ttu-id="2fa39-168">Copia del file non riuscita.</span><span class="sxs-lookup"><span data-stu-id="2fa39-168">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="2fa39-169">**Parametro di sicurezza non valido**</span><span class="sxs-lookup"><span data-stu-id="2fa39-169">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="2fa39-170">79</span><span class="sxs-lookup"><span data-stu-id="2fa39-170">79</span></span>

<span data-ttu-id="2fa39-171">Parametro di sicurezza non valido.</span><span class="sxs-lookup"><span data-stu-id="2fa39-171">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="2fa39-172">**Impossibile configurare il servizio TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="2fa39-172">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="2fa39-173">80</span><span class="sxs-lookup"><span data-stu-id="2fa39-173">80</span></span>

<span data-ttu-id="2fa39-174">Impossibile configurare il servizio TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="2fa39-174">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="2fa39-175">**Non è possibile configurare il servizio DHCP**</span><span class="sxs-lookup"><span data-stu-id="2fa39-175">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="2fa39-176">81</span><span class="sxs-lookup"><span data-stu-id="2fa39-176">81</span></span>

<span data-ttu-id="2fa39-177">Impossibile configurare il servizio DHCP.</span><span class="sxs-lookup"><span data-stu-id="2fa39-177">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="2fa39-178">**Non è possibile rinnovare il lease DHCP**</span><span class="sxs-lookup"><span data-stu-id="2fa39-178">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="2fa39-179">82</span><span class="sxs-lookup"><span data-stu-id="2fa39-179">82</span></span>

<span data-ttu-id="2fa39-180">Non è possibile rinnovare il lease DHCP.</span><span class="sxs-lookup"><span data-stu-id="2fa39-180">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="2fa39-181">**Non è possibile rilasciare il lease DHCP**</span><span class="sxs-lookup"><span data-stu-id="2fa39-181">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="2fa39-182">83</span><span class="sxs-lookup"><span data-stu-id="2fa39-182">83</span></span>

<span data-ttu-id="2fa39-183">Impossibile rilasciare il lease DHCP.</span><span class="sxs-lookup"><span data-stu-id="2fa39-183">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="2fa39-184">**IP non abilitato sulla scheda**</span><span class="sxs-lookup"><span data-stu-id="2fa39-184">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="2fa39-185">84</span><span class="sxs-lookup"><span data-stu-id="2fa39-185">84</span></span>

<span data-ttu-id="2fa39-186">IP non abilitato sulla scheda.</span><span class="sxs-lookup"><span data-stu-id="2fa39-186">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="2fa39-187">**IPX non abilitato sull'adapter**</span><span class="sxs-lookup"><span data-stu-id="2fa39-187">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="2fa39-188">85</span><span class="sxs-lookup"><span data-stu-id="2fa39-188">85</span></span>

<span data-ttu-id="2fa39-189">IPX non abilitato sulla scheda.</span><span class="sxs-lookup"><span data-stu-id="2fa39-189">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="2fa39-190">**Errore limite numero frame/rete**</span><span class="sxs-lookup"><span data-stu-id="2fa39-190">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="2fa39-191">86</span><span class="sxs-lookup"><span data-stu-id="2fa39-191">86</span></span>

<span data-ttu-id="2fa39-192">Errore dei limiti del numero di rete o del frame.</span><span class="sxs-lookup"><span data-stu-id="2fa39-192">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="2fa39-193">**Tipo di frame non valido**</span><span class="sxs-lookup"><span data-stu-id="2fa39-193">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="2fa39-194">87</span><span class="sxs-lookup"><span data-stu-id="2fa39-194">87</span></span>

<span data-ttu-id="2fa39-195">Tipo di frame non valido.</span><span class="sxs-lookup"><span data-stu-id="2fa39-195">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="2fa39-196">**Numero di rete non valido**</span><span class="sxs-lookup"><span data-stu-id="2fa39-196">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="2fa39-197">88</span><span class="sxs-lookup"><span data-stu-id="2fa39-197">88</span></span>

<span data-ttu-id="2fa39-198">Numero di rete non valido.</span><span class="sxs-lookup"><span data-stu-id="2fa39-198">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="2fa39-199">**Numero di rete duplicato**</span><span class="sxs-lookup"><span data-stu-id="2fa39-199">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="2fa39-200">89</span><span class="sxs-lookup"><span data-stu-id="2fa39-200">89</span></span>

<span data-ttu-id="2fa39-201">Numero di rete duplicato.</span><span class="sxs-lookup"><span data-stu-id="2fa39-201">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="2fa39-202">**Parametro fuori limite**</span><span class="sxs-lookup"><span data-stu-id="2fa39-202">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="2fa39-203">90</span><span class="sxs-lookup"><span data-stu-id="2fa39-203">90</span></span>

<span data-ttu-id="2fa39-204">Parametro fuori limite.</span><span class="sxs-lookup"><span data-stu-id="2fa39-204">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="2fa39-205">**Accesso negato**</span><span class="sxs-lookup"><span data-stu-id="2fa39-205">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="2fa39-206">91</span><span class="sxs-lookup"><span data-stu-id="2fa39-206">91</span></span>

<span data-ttu-id="2fa39-207">Accesso negato.</span><span class="sxs-lookup"><span data-stu-id="2fa39-207">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="2fa39-208">**Memoria insufficiente**</span><span class="sxs-lookup"><span data-stu-id="2fa39-208">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="2fa39-209">92</span><span class="sxs-lookup"><span data-stu-id="2fa39-209">92</span></span>

<span data-ttu-id="2fa39-210">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="2fa39-210">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="2fa39-211">**Esiste già**</span><span class="sxs-lookup"><span data-stu-id="2fa39-211">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="2fa39-212">93</span><span class="sxs-lookup"><span data-stu-id="2fa39-212">93</span></span>

<span data-ttu-id="2fa39-213">Esiste già.</span><span class="sxs-lookup"><span data-stu-id="2fa39-213">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="2fa39-214">**Percorso, file o oggetto non trovato**</span><span class="sxs-lookup"><span data-stu-id="2fa39-214">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="2fa39-215">94</span><span class="sxs-lookup"><span data-stu-id="2fa39-215">94</span></span>

<span data-ttu-id="2fa39-216">Il percorso, il file o l'oggetto non è stato trovato.</span><span class="sxs-lookup"><span data-stu-id="2fa39-216">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="2fa39-217">**Non è possibile inviare una notifica al servizio**</span><span class="sxs-lookup"><span data-stu-id="2fa39-217">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="2fa39-218">95</span><span class="sxs-lookup"><span data-stu-id="2fa39-218">95</span></span>

<span data-ttu-id="2fa39-219">Impossibile notificare il servizio.</span><span class="sxs-lookup"><span data-stu-id="2fa39-219">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="2fa39-220">**Non è possibile inviare una notifica al servizio DNS**</span><span class="sxs-lookup"><span data-stu-id="2fa39-220">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="2fa39-221">96</span><span class="sxs-lookup"><span data-stu-id="2fa39-221">96</span></span>

<span data-ttu-id="2fa39-222">Impossibile inviare una notifica al servizio DNS.</span><span class="sxs-lookup"><span data-stu-id="2fa39-222">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="2fa39-223">**Interfaccia non configurabile**</span><span class="sxs-lookup"><span data-stu-id="2fa39-223">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="2fa39-224">97</span><span class="sxs-lookup"><span data-stu-id="2fa39-224">97</span></span>

<span data-ttu-id="2fa39-225">Interfaccia non configurabile.</span><span class="sxs-lookup"><span data-stu-id="2fa39-225">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="2fa39-226">**Non tutti i lease DHCP possono essere rilasciati/rinnovati**</span><span class="sxs-lookup"><span data-stu-id="2fa39-226">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="2fa39-227">98</span><span class="sxs-lookup"><span data-stu-id="2fa39-227">98</span></span>

<span data-ttu-id="2fa39-228">Non tutti i lease DHCP possono essere rilasciati o rinnovati.</span><span class="sxs-lookup"><span data-stu-id="2fa39-228">Not all DHCP leases can be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="2fa39-229">**DHCP non abilitato sull'adapter**</span><span class="sxs-lookup"><span data-stu-id="2fa39-229">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="2fa39-230">100</span><span class="sxs-lookup"><span data-stu-id="2fa39-230">100</span></span>

<span data-ttu-id="2fa39-231">DHCP non è abilitato sulla scheda.</span><span class="sxs-lookup"><span data-stu-id="2fa39-231">DHCP is not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="2fa39-232">**Altri**</span><span class="sxs-lookup"><span data-stu-id="2fa39-232">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="2fa39-233">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="2fa39-233">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2fa39-234">Commenti</span><span class="sxs-lookup"><span data-stu-id="2fa39-234">Remarks</span></span>

<span data-ttu-id="2fa39-235">L'MTU corrisponde alla dimensione massima del pacchetto (in byte) che un trasporto trasmetterà sulla rete sottostante.</span><span class="sxs-lookup"><span data-stu-id="2fa39-235">The MTU is the maximum packet size (in bytes) that a transport will transmit over the underlying network.</span></span> <span data-ttu-id="2fa39-236">Le dimensioni includono l'intestazione del trasporto.</span><span class="sxs-lookup"><span data-stu-id="2fa39-236">The size includes the transport header.</span></span>

<span data-ttu-id="2fa39-237">Si noti che un datagramma IP può estendersi su più pacchetti.</span><span class="sxs-lookup"><span data-stu-id="2fa39-237">Note that an IP datagram can span multiple packets.</span></span> <span data-ttu-id="2fa39-238">I valori maggiori di quelli predefiniti per la rete sottostante comportano il trasporto usando la MTU predefinita di rete.</span><span class="sxs-lookup"><span data-stu-id="2fa39-238">Values larger than the default for the underlying network result in the transport using the network default MTU.</span></span> <span data-ttu-id="2fa39-239">I valori minori di 68 generano il trasporto usando un valore MTU pari a 68.</span><span class="sxs-lookup"><span data-stu-id="2fa39-239">Values smaller than 68 result in the transport using an MTU of 68.</span></span>

## <a name="examples"></a><span data-ttu-id="2fa39-240">Esempio</span><span class="sxs-lookup"><span data-stu-id="2fa39-240">Examples</span></span>

<span data-ttu-id="2fa39-241">L'esempio [Modify the MTU for all Network Adapters](https://Gallery.TechNet.Microsoft.Com/49c26363-d46c-4288-9c8d-feb0a1982998) VBScript configura l'unità di trasmissione massima per tutte le schede di rete installate in un computer.</span><span class="sxs-lookup"><span data-stu-id="2fa39-241">The [Modify the MTU for all Network Adapters](https://Gallery.TechNet.Microsoft.Com/49c26363-d46c-4288-9c8d-feb0a1982998) VBScript sample configures the maximum transmission unit for all network adapters installed in a computer.</span></span>

## <a name="requirements"></a><span data-ttu-id="2fa39-242">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2fa39-242">Requirements</span></span>



| <span data-ttu-id="2fa39-243">Requisito</span><span class="sxs-lookup"><span data-stu-id="2fa39-243">Requirement</span></span> | <span data-ttu-id="2fa39-244">Valore</span><span class="sxs-lookup"><span data-stu-id="2fa39-244">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2fa39-245">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2fa39-245">Minimum supported client</span></span><br/> | <span data-ttu-id="2fa39-246">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2fa39-246">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2fa39-247">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2fa39-247">Minimum supported server</span></span><br/> | <span data-ttu-id="2fa39-248">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2fa39-248">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2fa39-249">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="2fa39-249">Namespace</span></span><br/>                | <span data-ttu-id="2fa39-250">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="2fa39-250">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2fa39-251">MOF</span><span class="sxs-lookup"><span data-stu-id="2fa39-251">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2fa39-252"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2fa39-252"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2fa39-253">DLL</span><span class="sxs-lookup"><span data-stu-id="2fa39-253">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2fa39-254"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2fa39-254"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2fa39-255">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2fa39-255">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2fa39-256">Classi hardware del sistema del computer</span><span class="sxs-lookup"><span data-stu-id="2fa39-256">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="2fa39-257">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="2fa39-257">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="2fa39-258">Attività WMI: rete</span><span class="sxs-lookup"><span data-stu-id="2fa39-258">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="2fa39-259">Attività WMI: account e domini</span><span class="sxs-lookup"><span data-stu-id="2fa39-259">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="2fa39-260">Supporto di IPv6 e IPv4 in WMI</span><span class="sxs-lookup"><span data-stu-id="2fa39-260">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

