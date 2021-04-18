---
description: Il metodo della classe WMI SetWINSServer imposta i server WINS (Windows Internet Naming Service) primari e secondari in questa scheda di rete associata a TCP/IP. Questo metodo viene applicato indipendentemente dalla scheda di rete.
ms.assetid: fa8ce436-b67e-4975-a5c5-1a7d6aab4c8e
ms.tgt_platform: multiple
title: Metodo SetWINSServer della classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetWINSServer
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 49bfb0103a7d9cbbd6ea3faa0e1a868bac7b0196
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304482"
---
# <a name="setwinsserver-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="fbe0e-104">Metodo SetWINSServer della \_ classe NetworkAdapterConfiguration Win32</span><span class="sxs-lookup"><span data-stu-id="fbe0e-104">SetWINSServer method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="fbe0e-105">Il metodo della [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetWINSServer** imposta i server WINS (Windows Internet Naming Service) primari e secondari in questa scheda di rete associata a TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="fbe0e-105">The **SetWINSServer** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method sets the primary and secondary Windows Internet Naming Service (WINS) servers on this TCP/IP-bound network adapter.</span></span> <span data-ttu-id="fbe0e-106">Questo metodo viene applicato indipendentemente dalla scheda di rete.</span><span class="sxs-lookup"><span data-stu-id="fbe0e-106">This method is applied independently of the network adapter.</span></span>

<span data-ttu-id="fbe0e-107">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="fbe0e-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="fbe0e-108">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="fbe0e-108">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="fbe0e-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fbe0e-109">Syntax</span></span>


```mof
uint32 SetWINSServer(
  [in] string WINSPrimaryServer,
  [in] string WINSSecondaryServer
);
```



## <a name="parameters"></a><span data-ttu-id="fbe0e-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="fbe0e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fbe0e-111">*WINSPrimaryServer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fbe0e-111">*WINSPrimaryServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fbe0e-112">Indirizzo IP del server WINS primario.</span><span class="sxs-lookup"><span data-stu-id="fbe0e-112">IP address of the primary WINS server.</span></span>

> [!Note]  
> <span data-ttu-id="fbe0e-113">Verificare sempre la validità di questo indirizzo IP da un'origine sconosciuta o da un'origine non attendibile.</span><span class="sxs-lookup"><span data-stu-id="fbe0e-113">Always verify the validity of this IP address when it is from an unknown source, or a source that you do not trust.</span></span>

 

</dd> <dt>

<span data-ttu-id="fbe0e-114">*WINSSecondaryServer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fbe0e-114">*WINSSecondaryServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fbe0e-115">Indirizzo IP del server WINS secondario.</span><span class="sxs-lookup"><span data-stu-id="fbe0e-115">IP address of the secondary WINS server.</span></span>

> [!Note]  
> <span data-ttu-id="fbe0e-116">Verificare sempre la validità di questo indirizzo IP da un'origine sconosciuta o da un'origine non attendibile.</span><span class="sxs-lookup"><span data-stu-id="fbe0e-116">Always verify the validity of this IP address when it is from an unknown source, or a source that you do not trust.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fbe0e-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fbe0e-117">Return value</span></span>

<span data-ttu-id="fbe0e-118">Restituisce un valore intero pari a 0 (zero) al completamento corretto e qualsiasi altro numero per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="fbe0e-118">Returns an integer value of 0 (zero) on successful completion, and any other number to indicate an error.</span></span> <span data-ttu-id="fbe0e-119">Per ulteriori informazioni sui codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="fbe0e-119">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="fbe0e-120">Per i valori **HRESULT** generali, vedere [codici di errore di sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="fbe0e-120">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="fbe0e-121">**Operazione completata, non è necessario riavviare il computer**</span><span class="sxs-lookup"><span data-stu-id="fbe0e-121">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="fbe0e-122">0</span><span class="sxs-lookup"><span data-stu-id="fbe0e-122">0</span></span>

<span data-ttu-id="fbe0e-123">Operazione completata, non è necessario riavviare il computer.</span><span class="sxs-lookup"><span data-stu-id="fbe0e-123">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="fbe0e-124">**Operazione completata, riavvio richiesto**</span><span class="sxs-lookup"><span data-stu-id="fbe0e-124">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="fbe0e-125">1</span><span class="sxs-lookup"><span data-stu-id="fbe0e-125">1</span></span>

<span data-ttu-id="fbe0e-126">Operazione completata, è necessario riavviare il computer.</span><span class="sxs-lookup"><span data-stu-id="fbe0e-126">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="fbe0e-127">**Metodo non supportato in questa piattaforma**</span><span class="sxs-lookup"><span data-stu-id="fbe0e-127">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="fbe0e-128">64</span><span class="sxs-lookup"><span data-stu-id="fbe0e-128">64</span></span>

<span data-ttu-id="fbe0e-129">Metodo non supportato in questa piattaforma.</span><span class="sxs-lookup"><span data-stu-id="fbe0e-129">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="fbe0e-130">**Errore sconosciuto**</span><span class="sxs-lookup"><span data-stu-id="fbe0e-130">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="fbe0e-131">65</span><span class="sxs-lookup"><span data-stu-id="fbe0e-131">65</span></span>

<span data-ttu-id="fbe0e-132">Errore sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="fbe0e-132">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="fbe0e-133">**subnet mask non valido**</span><span class="sxs-lookup"><span data-stu-id="fbe0e-133">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="fbe0e-134">66</span><span class="sxs-lookup"><span data-stu-id="fbe0e-134">66</span></span>

<span data-ttu-id="fbe0e-135">Subnet mask non valido.</span><span class="sxs-lookup"><span data-stu-id="fbe0e-135">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="fbe0e-136">**Si è verificato un errore durante l'elaborazione di un'istanza restituita**</span><span class="sxs-lookup"><span data-stu-id="fbe0e-136">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="fbe0e-137">67</span><span class="sxs-lookup"><span data-stu-id="fbe0e-137">67</span></span>

<span data-ttu-id="fbe0e-138">Si è verificato un errore durante l'elaborazione di un'istanza di restituita.</span><span class="sxs-lookup"><span data-stu-id="fbe0e-138">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="fbe0e-139">**Parametro di input non valido**</span><span class="sxs-lookup"><span data-stu-id="fbe0e-139">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="fbe0e-140">68</span><span class="sxs-lookup"><span data-stu-id="fbe0e-140">68</span></span>

<span data-ttu-id="fbe0e-141">Parametro di input non valido.</span><span class="sxs-lookup"><span data-stu-id="fbe0e-141">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="fbe0e-142">**Sono stati specificati più di 5 gateway**</span><span class="sxs-lookup"><span data-stu-id="fbe0e-142">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="fbe0e-143">69</span><span class="sxs-lookup"><span data-stu-id="fbe0e-143">69</span></span>

<span data-ttu-id="fbe0e-144">Sono stati specificati più di cinque gateway.</span><span class="sxs-lookup"><span data-stu-id="fbe0e-144">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="fbe0e-145">**Indirizzo IP non valido**</span><span class="sxs-lookup"><span data-stu-id="fbe0e-145">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="fbe0e-146">70</span><span class="sxs-lookup"><span data-stu-id="fbe0e-146">70</span></span>

<span data-ttu-id="fbe0e-147">Indirizzo IP non valido.</span><span class="sxs-lookup"><span data-stu-id="fbe0e-147">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="fbe0e-148">**Indirizzo IP gateway non valido**</span><span class="sxs-lookup"><span data-stu-id="fbe0e-148">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="fbe0e-149">71</span><span class="sxs-lookup"><span data-stu-id="fbe0e-149">71</span></span>

<span data-ttu-id="fbe0e-150">Indirizzo IP del gateway non valido.</span><span class="sxs-lookup"><span data-stu-id="fbe0e-150">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="fbe0e-151">**Si è verificato un errore durante l'accesso al registro di sistema per le informazioni richieste**</span><span class="sxs-lookup"><span data-stu-id="fbe0e-151">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="fbe0e-152">72</span><span class="sxs-lookup"><span data-stu-id="fbe0e-152">72</span></span>

<span data-ttu-id="fbe0e-153">Si è verificato un errore durante l'accesso al registro di sistema per le informazioni richieste.</span><span class="sxs-lookup"><span data-stu-id="fbe0e-153">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="fbe0e-154">**Nome di dominio non valido**</span><span class="sxs-lookup"><span data-stu-id="fbe0e-154">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="fbe0e-155">73</span><span class="sxs-lookup"><span data-stu-id="fbe0e-155">73</span></span>

<span data-ttu-id="fbe0e-156">Nome di dominio non valido.</span><span class="sxs-lookup"><span data-stu-id="fbe0e-156">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="fbe0e-157">**Nome host non valido**</span><span class="sxs-lookup"><span data-stu-id="fbe0e-157">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="fbe0e-158">74</span><span class="sxs-lookup"><span data-stu-id="fbe0e-158">74</span></span>

<span data-ttu-id="fbe0e-159">Nome host non valido.</span><span class="sxs-lookup"><span data-stu-id="fbe0e-159">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="fbe0e-160">**Nessun server WINS primario/secondario definito**</span><span class="sxs-lookup"><span data-stu-id="fbe0e-160">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="fbe0e-161">75</span><span class="sxs-lookup"><span data-stu-id="fbe0e-161">75</span></span>

<span data-ttu-id="fbe0e-162">Nessun server WINS primario o secondario definito.</span><span class="sxs-lookup"><span data-stu-id="fbe0e-162">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="fbe0e-163">**File non valido**</span><span class="sxs-lookup"><span data-stu-id="fbe0e-163">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="fbe0e-164">76</span><span class="sxs-lookup"><span data-stu-id="fbe0e-164">76</span></span>

<span data-ttu-id="fbe0e-165">File non valido.</span><span class="sxs-lookup"><span data-stu-id="fbe0e-165">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="fbe0e-166">**Percorso di sistema non valido**</span><span class="sxs-lookup"><span data-stu-id="fbe0e-166">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="fbe0e-167">77</span><span class="sxs-lookup"><span data-stu-id="fbe0e-167">77</span></span>

<span data-ttu-id="fbe0e-168">Percorso di sistema non valido.</span><span class="sxs-lookup"><span data-stu-id="fbe0e-168">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="fbe0e-169">**Copia del file non riuscita**</span><span class="sxs-lookup"><span data-stu-id="fbe0e-169">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="fbe0e-170">78</span><span class="sxs-lookup"><span data-stu-id="fbe0e-170">78</span></span>

<span data-ttu-id="fbe0e-171">Copia del file non riuscita.</span><span class="sxs-lookup"><span data-stu-id="fbe0e-171">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="fbe0e-172">**Parametro di sicurezza non valido**</span><span class="sxs-lookup"><span data-stu-id="fbe0e-172">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="fbe0e-173">79</span><span class="sxs-lookup"><span data-stu-id="fbe0e-173">79</span></span>

<span data-ttu-id="fbe0e-174">Parametro di sicurezza non valido.</span><span class="sxs-lookup"><span data-stu-id="fbe0e-174">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="fbe0e-175">**Impossibile configurare il servizio TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="fbe0e-175">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="fbe0e-176">80</span><span class="sxs-lookup"><span data-stu-id="fbe0e-176">80</span></span>

<span data-ttu-id="fbe0e-177">Impossibile configurare il servizio TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="fbe0e-177">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="fbe0e-178">**Non è possibile configurare il servizio DHCP**</span><span class="sxs-lookup"><span data-stu-id="fbe0e-178">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="fbe0e-179">81</span><span class="sxs-lookup"><span data-stu-id="fbe0e-179">81</span></span>

<span data-ttu-id="fbe0e-180">Impossibile configurare il servizio DHCP.</span><span class="sxs-lookup"><span data-stu-id="fbe0e-180">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="fbe0e-181">**Non è possibile rinnovare il lease DHCP**</span><span class="sxs-lookup"><span data-stu-id="fbe0e-181">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="fbe0e-182">82</span><span class="sxs-lookup"><span data-stu-id="fbe0e-182">82</span></span>

<span data-ttu-id="fbe0e-183">Non è possibile rinnovare il lease DHCP.</span><span class="sxs-lookup"><span data-stu-id="fbe0e-183">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="fbe0e-184">**Non è possibile rilasciare il lease DHCP**</span><span class="sxs-lookup"><span data-stu-id="fbe0e-184">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="fbe0e-185">83</span><span class="sxs-lookup"><span data-stu-id="fbe0e-185">83</span></span>

<span data-ttu-id="fbe0e-186">Impossibile rilasciare il lease DHCP.</span><span class="sxs-lookup"><span data-stu-id="fbe0e-186">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="fbe0e-187">**IP non abilitato sulla scheda**</span><span class="sxs-lookup"><span data-stu-id="fbe0e-187">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="fbe0e-188">84</span><span class="sxs-lookup"><span data-stu-id="fbe0e-188">84</span></span>

<span data-ttu-id="fbe0e-189">IP non abilitato sulla scheda.</span><span class="sxs-lookup"><span data-stu-id="fbe0e-189">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="fbe0e-190">**IPX non abilitato sull'adapter**</span><span class="sxs-lookup"><span data-stu-id="fbe0e-190">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="fbe0e-191">85</span><span class="sxs-lookup"><span data-stu-id="fbe0e-191">85</span></span>

<span data-ttu-id="fbe0e-192">IPX non abilitato sulla scheda.</span><span class="sxs-lookup"><span data-stu-id="fbe0e-192">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="fbe0e-193">**Errore limite numero frame/rete**</span><span class="sxs-lookup"><span data-stu-id="fbe0e-193">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="fbe0e-194">86</span><span class="sxs-lookup"><span data-stu-id="fbe0e-194">86</span></span>

<span data-ttu-id="fbe0e-195">Errore dei limiti del numero di rete o del frame.</span><span class="sxs-lookup"><span data-stu-id="fbe0e-195">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="fbe0e-196">**Tipo di frame non valido**</span><span class="sxs-lookup"><span data-stu-id="fbe0e-196">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="fbe0e-197">87</span><span class="sxs-lookup"><span data-stu-id="fbe0e-197">87</span></span>

<span data-ttu-id="fbe0e-198">Tipo di frame non valido.</span><span class="sxs-lookup"><span data-stu-id="fbe0e-198">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="fbe0e-199">**Numero di rete non valido**</span><span class="sxs-lookup"><span data-stu-id="fbe0e-199">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="fbe0e-200">88</span><span class="sxs-lookup"><span data-stu-id="fbe0e-200">88</span></span>

<span data-ttu-id="fbe0e-201">Numero di rete non valido.</span><span class="sxs-lookup"><span data-stu-id="fbe0e-201">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="fbe0e-202">**Numero di rete duplicato**</span><span class="sxs-lookup"><span data-stu-id="fbe0e-202">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="fbe0e-203">89</span><span class="sxs-lookup"><span data-stu-id="fbe0e-203">89</span></span>

<span data-ttu-id="fbe0e-204">Numero di rete duplicato.</span><span class="sxs-lookup"><span data-stu-id="fbe0e-204">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="fbe0e-205">**Parametro fuori limite**</span><span class="sxs-lookup"><span data-stu-id="fbe0e-205">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="fbe0e-206">90</span><span class="sxs-lookup"><span data-stu-id="fbe0e-206">90</span></span>

<span data-ttu-id="fbe0e-207">Parametro fuori limite.</span><span class="sxs-lookup"><span data-stu-id="fbe0e-207">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="fbe0e-208">**Accesso negato**</span><span class="sxs-lookup"><span data-stu-id="fbe0e-208">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="fbe0e-209">91</span><span class="sxs-lookup"><span data-stu-id="fbe0e-209">91</span></span>

<span data-ttu-id="fbe0e-210">Accesso negato.</span><span class="sxs-lookup"><span data-stu-id="fbe0e-210">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="fbe0e-211">**Memoria insufficiente**</span><span class="sxs-lookup"><span data-stu-id="fbe0e-211">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="fbe0e-212">92</span><span class="sxs-lookup"><span data-stu-id="fbe0e-212">92</span></span>

<span data-ttu-id="fbe0e-213">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="fbe0e-213">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="fbe0e-214">**Esiste già**</span><span class="sxs-lookup"><span data-stu-id="fbe0e-214">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="fbe0e-215">93</span><span class="sxs-lookup"><span data-stu-id="fbe0e-215">93</span></span>

<span data-ttu-id="fbe0e-216">Esiste già.</span><span class="sxs-lookup"><span data-stu-id="fbe0e-216">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="fbe0e-217">**Percorso, file o oggetto non trovato**</span><span class="sxs-lookup"><span data-stu-id="fbe0e-217">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="fbe0e-218">94</span><span class="sxs-lookup"><span data-stu-id="fbe0e-218">94</span></span>

<span data-ttu-id="fbe0e-219">Il percorso, il file o l'oggetto non è stato trovato.</span><span class="sxs-lookup"><span data-stu-id="fbe0e-219">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="fbe0e-220">**Non è possibile inviare una notifica al servizio**</span><span class="sxs-lookup"><span data-stu-id="fbe0e-220">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="fbe0e-221">95</span><span class="sxs-lookup"><span data-stu-id="fbe0e-221">95</span></span>

<span data-ttu-id="fbe0e-222">Impossibile notificare il servizio.</span><span class="sxs-lookup"><span data-stu-id="fbe0e-222">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="fbe0e-223">**Non è possibile inviare una notifica al servizio DNS**</span><span class="sxs-lookup"><span data-stu-id="fbe0e-223">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="fbe0e-224">96</span><span class="sxs-lookup"><span data-stu-id="fbe0e-224">96</span></span>

<span data-ttu-id="fbe0e-225">Impossibile inviare una notifica al servizio DNS.</span><span class="sxs-lookup"><span data-stu-id="fbe0e-225">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="fbe0e-226">**Interfaccia non configurabile**</span><span class="sxs-lookup"><span data-stu-id="fbe0e-226">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="fbe0e-227">97</span><span class="sxs-lookup"><span data-stu-id="fbe0e-227">97</span></span>

<span data-ttu-id="fbe0e-228">Interfaccia non configurabile.</span><span class="sxs-lookup"><span data-stu-id="fbe0e-228">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="fbe0e-229">**Non tutti i lease DHCP possono essere rilasciati/rinnovati**</span><span class="sxs-lookup"><span data-stu-id="fbe0e-229">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="fbe0e-230">98</span><span class="sxs-lookup"><span data-stu-id="fbe0e-230">98</span></span>

<span data-ttu-id="fbe0e-231">Non tutti i lease DHCP possono essere rilasciati o rinnovati.</span><span class="sxs-lookup"><span data-stu-id="fbe0e-231">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="fbe0e-232">**DHCP non abilitato sull'adapter**</span><span class="sxs-lookup"><span data-stu-id="fbe0e-232">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="fbe0e-233">100</span><span class="sxs-lookup"><span data-stu-id="fbe0e-233">100</span></span>

<span data-ttu-id="fbe0e-234">DHCP non abilitato sulla scheda.</span><span class="sxs-lookup"><span data-stu-id="fbe0e-234">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="fbe0e-235">**Altri**</span><span class="sxs-lookup"><span data-stu-id="fbe0e-235">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="fbe0e-236">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="fbe0e-236">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fbe0e-237">Commenti</span><span class="sxs-lookup"><span data-stu-id="fbe0e-237">Remarks</span></span>

<span data-ttu-id="fbe0e-238">Se *WINSPrimaryServer* e *WINSSecondaryServer* sono entrambi impostati su "" (una stringa vuota), i server WINS espliciti torneranno a DHCP.</span><span class="sxs-lookup"><span data-stu-id="fbe0e-238">If both *WINSPrimaryServer* and *WINSSecondaryServer* are set to "" (an empty string), then explicit WINS servers revert back to DHCP.</span></span>

## <a name="examples"></a><span data-ttu-id="fbe0e-239">Esempio</span><span class="sxs-lookup"><span data-stu-id="fbe0e-239">Examples</span></span>

<span data-ttu-id="fbe0e-240">[Assegnazione di un indirizzo IP recuperato da un database](https://Gallery.TechNet.Microsoft.Com/d4526355-e682-4116-a79a-8bba569b084d) L'esempio di codice VBScript Cerca un computer in un database e assegna tale computer all'indirizzo IP specificato.</span><span class="sxs-lookup"><span data-stu-id="fbe0e-240">[The Assign an IP Address Retrieved from a Database](https://Gallery.TechNet.Microsoft.Com/d4526355-e682-4116-a79a-8bba569b084d) VBScript code sample looks up a computer in a database and assigns that computer the specified IP address.</span></span>

<span data-ttu-id="fbe0e-241">Nell'esempio di codice VBScript seguente viene impostato il server WINS primario e secondario per una scheda di rete associata a TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="fbe0e-241">The following VBScript code sample sets the primary and secondary WINS server for a TCP/IP-bound network adapter.</span></span>


```VB
On Error Resume Next 
 
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colNetCards = objWMIService.ExecQuery _ 
    ("Select * From Win32_NetworkAdapterConfiguration Where IPEnabled = True") 
 
For Each objNetCard in colNetCards 
    strPrimaryServer = "192.168.1.100" 
    strSecondaryServer = "192.168.1.200" 
    objNetCard.SetWINSServer strPrimaryServer, strSecondaryServer 
Next 
```



## <a name="requirements"></a><span data-ttu-id="fbe0e-242">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fbe0e-242">Requirements</span></span>



| <span data-ttu-id="fbe0e-243">Requisito</span><span class="sxs-lookup"><span data-stu-id="fbe0e-243">Requirement</span></span> | <span data-ttu-id="fbe0e-244">Valore</span><span class="sxs-lookup"><span data-stu-id="fbe0e-244">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fbe0e-245">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fbe0e-245">Minimum supported client</span></span><br/> | <span data-ttu-id="fbe0e-246">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fbe0e-246">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="fbe0e-247">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fbe0e-247">Minimum supported server</span></span><br/> | <span data-ttu-id="fbe0e-248">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fbe0e-248">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="fbe0e-249">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="fbe0e-249">Namespace</span></span><br/>                | <span data-ttu-id="fbe0e-250">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="fbe0e-250">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="fbe0e-251">MOF</span><span class="sxs-lookup"><span data-stu-id="fbe0e-251">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fbe0e-252"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fbe0e-252"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="fbe0e-253">DLL</span><span class="sxs-lookup"><span data-stu-id="fbe0e-253">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fbe0e-254"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fbe0e-254"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fbe0e-255">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fbe0e-255">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fbe0e-256">Classi hardware del sistema del computer</span><span class="sxs-lookup"><span data-stu-id="fbe0e-256">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="fbe0e-257">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="fbe0e-257">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="fbe0e-258">Attività WMI: rete</span><span class="sxs-lookup"><span data-stu-id="fbe0e-258">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="fbe0e-259">Attività WMI: account e domini</span><span class="sxs-lookup"><span data-stu-id="fbe0e-259">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="fbe0e-260">Supporto di IPv6 e IPv4 in WMI</span><span class="sxs-lookup"><span data-stu-id="fbe0e-260">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

