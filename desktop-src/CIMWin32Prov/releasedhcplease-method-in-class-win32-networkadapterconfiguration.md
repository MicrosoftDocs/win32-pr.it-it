---
description: Il metodo della classe WMI ReleaseDHCPLease rilascia l'indirizzo IP associato a una specifica scheda di rete abilitata per DHCP.
ms.assetid: 0cf4b531-8626-4388-bffa-e16a4aa8c794
ms.tgt_platform: multiple
title: Metodo ReleaseDHCPLease della classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.ReleaseDHCPLease
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5520a6b2d0960c1d4258b19f8cd4d600c9b8fe34
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305103"
---
# <a name="releasedhcplease-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="76dce-103">Metodo ReleaseDHCPLease della \_ classe NetworkAdapterConfiguration Win32</span><span class="sxs-lookup"><span data-stu-id="76dce-103">ReleaseDHCPLease method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="76dce-104">Il metodo della [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **ReleaseDHCPLease** rilascia l'indirizzo IP associato a una specifica scheda di rete abilitata per DHCP.</span><span class="sxs-lookup"><span data-stu-id="76dce-104">The **ReleaseDHCPLease** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method releases the IP address bound to a specific DHCP-enabled network adapter.</span></span>

<span data-ttu-id="76dce-105">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="76dce-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="76dce-106">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="76dce-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="76dce-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="76dce-107">Syntax</span></span>


```mof
uint32 ReleaseDHCPLease();
```



## <a name="parameters"></a><span data-ttu-id="76dce-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="76dce-108">Parameters</span></span>

<span data-ttu-id="76dce-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="76dce-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="76dce-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="76dce-110">Return value</span></span>

<span data-ttu-id="76dce-111">Restituisce un valore pari a 0 (zero) per un completamento corretto quando non è richiesto il riavvio, 1 (uno) per un completamento corretto quando è necessario un riavvio e un numero diverso se si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="76dce-111">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="76dce-112">Per ulteriori informazioni sui codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="76dce-112">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="76dce-113">Per i valori **HRESULT** generali, vedere [codici di errore di sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="76dce-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="76dce-114">**Operazione completata, non è necessario riavviare il computer**</span><span class="sxs-lookup"><span data-stu-id="76dce-114">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="76dce-115">0</span><span class="sxs-lookup"><span data-stu-id="76dce-115">0</span></span>

<span data-ttu-id="76dce-116">Operazione completata, non è necessario riavviare il computer.</span><span class="sxs-lookup"><span data-stu-id="76dce-116">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="76dce-117">**Operazione completata, riavvio richiesto**</span><span class="sxs-lookup"><span data-stu-id="76dce-117">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="76dce-118">1</span><span class="sxs-lookup"><span data-stu-id="76dce-118">1</span></span>

<span data-ttu-id="76dce-119">Operazione completata, è necessario riavviare il computer.</span><span class="sxs-lookup"><span data-stu-id="76dce-119">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="76dce-120">**Metodo non supportato in questa piattaforma**</span><span class="sxs-lookup"><span data-stu-id="76dce-120">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="76dce-121">64</span><span class="sxs-lookup"><span data-stu-id="76dce-121">64</span></span>

<span data-ttu-id="76dce-122">Metodo non supportato in questa piattaforma.</span><span class="sxs-lookup"><span data-stu-id="76dce-122">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="76dce-123">**Errore sconosciuto**</span><span class="sxs-lookup"><span data-stu-id="76dce-123">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="76dce-124">65</span><span class="sxs-lookup"><span data-stu-id="76dce-124">65</span></span>

<span data-ttu-id="76dce-125">Errore sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="76dce-125">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="76dce-126">**subnet mask non valido**</span><span class="sxs-lookup"><span data-stu-id="76dce-126">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="76dce-127">66</span><span class="sxs-lookup"><span data-stu-id="76dce-127">66</span></span>

<span data-ttu-id="76dce-128">Subnet mask non valido.</span><span class="sxs-lookup"><span data-stu-id="76dce-128">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="76dce-129">**Si è verificato un errore durante l'elaborazione di un'istanza restituita**</span><span class="sxs-lookup"><span data-stu-id="76dce-129">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="76dce-130">67</span><span class="sxs-lookup"><span data-stu-id="76dce-130">67</span></span>

<span data-ttu-id="76dce-131">Si è verificato un errore durante l'elaborazione di un'istanza di restituita.</span><span class="sxs-lookup"><span data-stu-id="76dce-131">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="76dce-132">**Parametro di input non valido**</span><span class="sxs-lookup"><span data-stu-id="76dce-132">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="76dce-133">68</span><span class="sxs-lookup"><span data-stu-id="76dce-133">68</span></span>

<span data-ttu-id="76dce-134">Parametro di input non valido.</span><span class="sxs-lookup"><span data-stu-id="76dce-134">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="76dce-135">**Sono stati specificati più di 5 gateway**</span><span class="sxs-lookup"><span data-stu-id="76dce-135">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="76dce-136">69</span><span class="sxs-lookup"><span data-stu-id="76dce-136">69</span></span>

<span data-ttu-id="76dce-137">Sono stati specificati più di cinque gateway.</span><span class="sxs-lookup"><span data-stu-id="76dce-137">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="76dce-138">**Indirizzo IP non valido**</span><span class="sxs-lookup"><span data-stu-id="76dce-138">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="76dce-139">70</span><span class="sxs-lookup"><span data-stu-id="76dce-139">70</span></span>

<span data-ttu-id="76dce-140">Indirizzo IP non valido.</span><span class="sxs-lookup"><span data-stu-id="76dce-140">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="76dce-141">**Indirizzo IP gateway non valido**</span><span class="sxs-lookup"><span data-stu-id="76dce-141">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="76dce-142">71</span><span class="sxs-lookup"><span data-stu-id="76dce-142">71</span></span>

<span data-ttu-id="76dce-143">Indirizzo IP del gateway non valido.</span><span class="sxs-lookup"><span data-stu-id="76dce-143">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="76dce-144">**Si è verificato un errore durante l'accesso al registro di sistema per le informazioni richieste**</span><span class="sxs-lookup"><span data-stu-id="76dce-144">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="76dce-145">72</span><span class="sxs-lookup"><span data-stu-id="76dce-145">72</span></span>

<span data-ttu-id="76dce-146">Si è verificato un errore durante l'accesso al registro di sistema per le informazioni richieste.</span><span class="sxs-lookup"><span data-stu-id="76dce-146">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="76dce-147">**Nome di dominio non valido**</span><span class="sxs-lookup"><span data-stu-id="76dce-147">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="76dce-148">73</span><span class="sxs-lookup"><span data-stu-id="76dce-148">73</span></span>

<span data-ttu-id="76dce-149">Nome di dominio non valido.</span><span class="sxs-lookup"><span data-stu-id="76dce-149">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="76dce-150">**Nome host non valido**</span><span class="sxs-lookup"><span data-stu-id="76dce-150">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="76dce-151">74</span><span class="sxs-lookup"><span data-stu-id="76dce-151">74</span></span>

<span data-ttu-id="76dce-152">Nome host non valido.</span><span class="sxs-lookup"><span data-stu-id="76dce-152">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="76dce-153">**Nessun server WINS primario/secondario definito**</span><span class="sxs-lookup"><span data-stu-id="76dce-153">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="76dce-154">75</span><span class="sxs-lookup"><span data-stu-id="76dce-154">75</span></span>

<span data-ttu-id="76dce-155">Nessun server WINS primario o secondario definito.</span><span class="sxs-lookup"><span data-stu-id="76dce-155">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="76dce-156">**File non valido**</span><span class="sxs-lookup"><span data-stu-id="76dce-156">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="76dce-157">76</span><span class="sxs-lookup"><span data-stu-id="76dce-157">76</span></span>

<span data-ttu-id="76dce-158">File non valido.</span><span class="sxs-lookup"><span data-stu-id="76dce-158">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="76dce-159">**Percorso di sistema non valido**</span><span class="sxs-lookup"><span data-stu-id="76dce-159">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="76dce-160">77</span><span class="sxs-lookup"><span data-stu-id="76dce-160">77</span></span>

<span data-ttu-id="76dce-161">Percorso di sistema non valido.</span><span class="sxs-lookup"><span data-stu-id="76dce-161">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="76dce-162">**Copia del file non riuscita**</span><span class="sxs-lookup"><span data-stu-id="76dce-162">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="76dce-163">78</span><span class="sxs-lookup"><span data-stu-id="76dce-163">78</span></span>

<span data-ttu-id="76dce-164">Copia del file non riuscita.</span><span class="sxs-lookup"><span data-stu-id="76dce-164">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="76dce-165">**Parametro di sicurezza non valido**</span><span class="sxs-lookup"><span data-stu-id="76dce-165">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="76dce-166">79</span><span class="sxs-lookup"><span data-stu-id="76dce-166">79</span></span>

<span data-ttu-id="76dce-167">Parametro di sicurezza non valido.</span><span class="sxs-lookup"><span data-stu-id="76dce-167">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="76dce-168">**Impossibile configurare il servizio TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="76dce-168">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="76dce-169">80</span><span class="sxs-lookup"><span data-stu-id="76dce-169">80</span></span>

<span data-ttu-id="76dce-170">Impossibile configurare il servizio TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="76dce-170">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="76dce-171">**Non è possibile configurare il servizio DHCP**</span><span class="sxs-lookup"><span data-stu-id="76dce-171">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="76dce-172">81</span><span class="sxs-lookup"><span data-stu-id="76dce-172">81</span></span>

<span data-ttu-id="76dce-173">Impossibile configurare il servizio DHCP.</span><span class="sxs-lookup"><span data-stu-id="76dce-173">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="76dce-174">**Non è possibile rinnovare il lease DHCP**</span><span class="sxs-lookup"><span data-stu-id="76dce-174">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="76dce-175">82</span><span class="sxs-lookup"><span data-stu-id="76dce-175">82</span></span>

<span data-ttu-id="76dce-176">Non è possibile rinnovare il lease DHCP.</span><span class="sxs-lookup"><span data-stu-id="76dce-176">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="76dce-177">**Non è possibile rilasciare il lease DHCP**</span><span class="sxs-lookup"><span data-stu-id="76dce-177">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="76dce-178">83</span><span class="sxs-lookup"><span data-stu-id="76dce-178">83</span></span>

<span data-ttu-id="76dce-179">Impossibile rilasciare il lease DHCP.</span><span class="sxs-lookup"><span data-stu-id="76dce-179">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="76dce-180">**IP non abilitato sulla scheda**</span><span class="sxs-lookup"><span data-stu-id="76dce-180">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="76dce-181">84</span><span class="sxs-lookup"><span data-stu-id="76dce-181">84</span></span>

<span data-ttu-id="76dce-182">IP non abilitato sulla scheda.</span><span class="sxs-lookup"><span data-stu-id="76dce-182">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="76dce-183">**IPX non abilitato sull'adapter**</span><span class="sxs-lookup"><span data-stu-id="76dce-183">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="76dce-184">85</span><span class="sxs-lookup"><span data-stu-id="76dce-184">85</span></span>

<span data-ttu-id="76dce-185">IPX non abilitato sulla scheda.</span><span class="sxs-lookup"><span data-stu-id="76dce-185">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="76dce-186">**Errore limite numero frame/rete**</span><span class="sxs-lookup"><span data-stu-id="76dce-186">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="76dce-187">86</span><span class="sxs-lookup"><span data-stu-id="76dce-187">86</span></span>

<span data-ttu-id="76dce-188">Errore dei limiti del numero di rete o del frame.</span><span class="sxs-lookup"><span data-stu-id="76dce-188">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="76dce-189">**Tipo di frame non valido**</span><span class="sxs-lookup"><span data-stu-id="76dce-189">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="76dce-190">87</span><span class="sxs-lookup"><span data-stu-id="76dce-190">87</span></span>

<span data-ttu-id="76dce-191">Tipo di frame non valido.</span><span class="sxs-lookup"><span data-stu-id="76dce-191">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="76dce-192">**Numero di rete non valido**</span><span class="sxs-lookup"><span data-stu-id="76dce-192">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="76dce-193">88</span><span class="sxs-lookup"><span data-stu-id="76dce-193">88</span></span>

<span data-ttu-id="76dce-194">Numero di rete non valido.</span><span class="sxs-lookup"><span data-stu-id="76dce-194">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="76dce-195">**Numero di rete duplicato**</span><span class="sxs-lookup"><span data-stu-id="76dce-195">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="76dce-196">89</span><span class="sxs-lookup"><span data-stu-id="76dce-196">89</span></span>

<span data-ttu-id="76dce-197">Numero di rete duplicato.</span><span class="sxs-lookup"><span data-stu-id="76dce-197">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="76dce-198">**Parametro fuori limite**</span><span class="sxs-lookup"><span data-stu-id="76dce-198">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="76dce-199">90</span><span class="sxs-lookup"><span data-stu-id="76dce-199">90</span></span>

<span data-ttu-id="76dce-200">Parametro fuori limite.</span><span class="sxs-lookup"><span data-stu-id="76dce-200">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="76dce-201">**Accesso negato**</span><span class="sxs-lookup"><span data-stu-id="76dce-201">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="76dce-202">91</span><span class="sxs-lookup"><span data-stu-id="76dce-202">91</span></span>

<span data-ttu-id="76dce-203">Accesso negato.</span><span class="sxs-lookup"><span data-stu-id="76dce-203">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="76dce-204">**Memoria insufficiente**</span><span class="sxs-lookup"><span data-stu-id="76dce-204">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="76dce-205">92</span><span class="sxs-lookup"><span data-stu-id="76dce-205">92</span></span>

<span data-ttu-id="76dce-206">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="76dce-206">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="76dce-207">**Esiste già**</span><span class="sxs-lookup"><span data-stu-id="76dce-207">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="76dce-208">93</span><span class="sxs-lookup"><span data-stu-id="76dce-208">93</span></span>

<span data-ttu-id="76dce-209">Esiste già.</span><span class="sxs-lookup"><span data-stu-id="76dce-209">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="76dce-210">**Percorso, file o oggetto non trovato**</span><span class="sxs-lookup"><span data-stu-id="76dce-210">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="76dce-211">94</span><span class="sxs-lookup"><span data-stu-id="76dce-211">94</span></span>

<span data-ttu-id="76dce-212">Il percorso, il file o l'oggetto non è stato trovato.</span><span class="sxs-lookup"><span data-stu-id="76dce-212">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="76dce-213">**Non è possibile inviare una notifica al servizio**</span><span class="sxs-lookup"><span data-stu-id="76dce-213">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="76dce-214">95</span><span class="sxs-lookup"><span data-stu-id="76dce-214">95</span></span>

<span data-ttu-id="76dce-215">Impossibile notificare il servizio.</span><span class="sxs-lookup"><span data-stu-id="76dce-215">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="76dce-216">**Non è possibile inviare una notifica al servizio DNS**</span><span class="sxs-lookup"><span data-stu-id="76dce-216">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="76dce-217">96</span><span class="sxs-lookup"><span data-stu-id="76dce-217">96</span></span>

<span data-ttu-id="76dce-218">Impossibile inviare una notifica al servizio DNS.</span><span class="sxs-lookup"><span data-stu-id="76dce-218">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="76dce-219">**Interfaccia non configurabile**</span><span class="sxs-lookup"><span data-stu-id="76dce-219">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="76dce-220">97</span><span class="sxs-lookup"><span data-stu-id="76dce-220">97</span></span>

<span data-ttu-id="76dce-221">Interfaccia non configurabile.</span><span class="sxs-lookup"><span data-stu-id="76dce-221">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="76dce-222">**Non tutti i lease DHCP possono essere rilasciati/rinnovati**</span><span class="sxs-lookup"><span data-stu-id="76dce-222">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="76dce-223">98</span><span class="sxs-lookup"><span data-stu-id="76dce-223">98</span></span>

<span data-ttu-id="76dce-224">Non tutti i lease DHCP possono essere rilasciati o rinnovati.</span><span class="sxs-lookup"><span data-stu-id="76dce-224">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="76dce-225">**DHCP non abilitato sull'adapter**</span><span class="sxs-lookup"><span data-stu-id="76dce-225">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="76dce-226">100</span><span class="sxs-lookup"><span data-stu-id="76dce-226">100</span></span>

<span data-ttu-id="76dce-227">DHCP non abilitato sulla scheda.</span><span class="sxs-lookup"><span data-stu-id="76dce-227">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="76dce-228">**Altri**</span><span class="sxs-lookup"><span data-stu-id="76dce-228">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="76dce-229">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="76dce-229">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="76dce-230">Commenti</span><span class="sxs-lookup"><span data-stu-id="76dce-230">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="76dce-231">Se DHCP è abilitato nel computer locale, l'opzione Disabilita TCP/IP in questa scheda di rete specifica.</span><span class="sxs-lookup"><span data-stu-id="76dce-231">If DHCP is enabled on the local computer system, the option disables TCP/IP on this specific network adapter.</span></span> <span data-ttu-id="76dce-232">A meno che non esista un percorso alternativo al sistema di destinazione, ovvero un'altra scheda di rete associata TCP/IP, tutte le comunicazioni TCP/IP andranno perse.</span><span class="sxs-lookup"><span data-stu-id="76dce-232">Unless you have an alternate path to the target system, that is, another TCP/IP bound network adapter, all TCP/IP communications will be lost.</span></span>

 

## <a name="examples"></a><span data-ttu-id="76dce-233">Esempio</span><span class="sxs-lookup"><span data-stu-id="76dce-233">Examples</span></span>

<span data-ttu-id="76dce-234">L'esempio di rinnovo di indirizzi IP per la [versione con](https://Gallery.TechNet.Microsoft.Com/Renew-IP-Adresses-Using-365f6bfa) PowerShell PowerShell nella raccolta TechNet USA **ReleaseDHCPLease** per rilasciare e rinnovare un indirizzo IP.</span><span class="sxs-lookup"><span data-stu-id="76dce-234">The [Release Renew IP Adresses Using PowerShell](https://Gallery.TechNet.Microsoft.Com/Renew-IP-Adresses-Using-365f6bfa) PowerShell example on TechNet Gallery uses **ReleaseDHCPLease** to release and renew an IP address.</span></span>

<span data-ttu-id="76dce-235">Il codice VBScript seguente rilascia i lease DHCP per tutte le schede di rete con binding TCP/IP in un computer.</span><span class="sxs-lookup"><span data-stu-id="76dce-235">The following VBScript code releases the DHCP leases for all TCP/IP-bound network adapters on a computer.</span></span>


```VB
On Error Resume Next 
 
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colNetCards = objWMIService.ExecQuery _ 
    ("Select * From Win32_NetworkAdapterConfiguration Where IPEnabled = True") 
 
For Each objNetCard in colNetCards 
    objNetCard.ReleaseDHCPLease() 
Next 
```



## <a name="requirements"></a><span data-ttu-id="76dce-236">Requisiti</span><span class="sxs-lookup"><span data-stu-id="76dce-236">Requirements</span></span>



| <span data-ttu-id="76dce-237">Requisito</span><span class="sxs-lookup"><span data-stu-id="76dce-237">Requirement</span></span> | <span data-ttu-id="76dce-238">Valore</span><span class="sxs-lookup"><span data-stu-id="76dce-238">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="76dce-239">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="76dce-239">Minimum supported client</span></span><br/> | <span data-ttu-id="76dce-240">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="76dce-240">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="76dce-241">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="76dce-241">Minimum supported server</span></span><br/> | <span data-ttu-id="76dce-242">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="76dce-242">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="76dce-243">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="76dce-243">Namespace</span></span><br/>                | <span data-ttu-id="76dce-244">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="76dce-244">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="76dce-245">MOF</span><span class="sxs-lookup"><span data-stu-id="76dce-245">MOF</span></span><br/>                      | <dl> <span data-ttu-id="76dce-246"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="76dce-246"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="76dce-247">DLL</span><span class="sxs-lookup"><span data-stu-id="76dce-247">DLL</span></span><br/>                      | <dl> <span data-ttu-id="76dce-248"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="76dce-248"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="76dce-249">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="76dce-249">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76dce-250">Classi hardware del sistema del computer</span><span class="sxs-lookup"><span data-stu-id="76dce-250">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="76dce-251">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="76dce-251">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="76dce-252">Attività WMI: rete</span><span class="sxs-lookup"><span data-stu-id="76dce-252">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="76dce-253">Attività WMI: account e domini</span><span class="sxs-lookup"><span data-stu-id="76dce-253">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="76dce-254">Supporto di IPv6 e IPv4 in WMI</span><span class="sxs-lookup"><span data-stu-id="76dce-254">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

