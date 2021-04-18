---
description: Il metodo della classe WMI DisableIPSec viene utilizzato per disabilitare Internet Protocol Security (IPsec) in questa scheda di rete abilitata per TCP/IP.
ms.assetid: 6fff2721-1ee2-42b4-bbf9-fd36b97318e3
ms.tgt_platform: multiple
title: Metodo DisableIPSec della classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.DisableIPSec
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9b2a17bbfa0f10c08edb581b4a4bf51173facfea
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304697"
---
# <a name="disableipsec-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="9d254-103">Metodo DisableIPSec della \_ classe NetworkAdapterConfiguration Win32</span><span class="sxs-lookup"><span data-stu-id="9d254-103">DisableIPSec method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="9d254-104">Il metodo della [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **DisableIPSec** viene utilizzato per disabilitare Internet Protocol Security (IPSec) in questa scheda di rete abilitata per TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="9d254-104">The **DisableIPSec** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method is used to disable Internet Protocol security (IPsec) on this TCP/IP-enabled network adapter.</span></span>

<span data-ttu-id="9d254-105">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="9d254-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="9d254-106">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="9d254-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="9d254-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9d254-107">Syntax</span></span>


```mof
uint32 DisableIPSec();
```



## <a name="parameters"></a><span data-ttu-id="9d254-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="9d254-108">Parameters</span></span>

<span data-ttu-id="9d254-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="9d254-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9d254-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9d254-110">Return value</span></span>

<span data-ttu-id="9d254-111">Restituisce un valore pari a 0 (zero) per un completamento corretto quando non è richiesto un riavvio, 1 (uno) per un completamento corretto quando è necessario un riavvio e qualsiasi altro numero se si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="9d254-111">Returns a value of 0 (zero) for a successful completion when a reboot is not required, 1 (one) for a successful completion when a reboot is required, and any other number if there is an error.</span></span> <span data-ttu-id="9d254-112">Per ulteriori informazioni sui codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="9d254-112">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="9d254-113">Per i valori **HRESULT** generali, vedere [codici di errore di sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="9d254-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="9d254-114">**Operazione completata, non è necessario riavviare il computer**</span><span class="sxs-lookup"><span data-stu-id="9d254-114">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="9d254-115">0</span><span class="sxs-lookup"><span data-stu-id="9d254-115">0</span></span>

<span data-ttu-id="9d254-116">Operazione completata, non è necessario riavviare il computer.</span><span class="sxs-lookup"><span data-stu-id="9d254-116">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="9d254-117">**Operazione completata, riavvio richiesto**</span><span class="sxs-lookup"><span data-stu-id="9d254-117">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="9d254-118">1</span><span class="sxs-lookup"><span data-stu-id="9d254-118">1</span></span>

<span data-ttu-id="9d254-119">Operazione completata, è necessario riavviare il computer.</span><span class="sxs-lookup"><span data-stu-id="9d254-119">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="9d254-120">**Metodo non supportato in questa piattaforma**</span><span class="sxs-lookup"><span data-stu-id="9d254-120">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="9d254-121">64</span><span class="sxs-lookup"><span data-stu-id="9d254-121">64</span></span>

<span data-ttu-id="9d254-122">Metodo non supportato in questa piattaforma.</span><span class="sxs-lookup"><span data-stu-id="9d254-122">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="9d254-123">**Errore sconosciuto**</span><span class="sxs-lookup"><span data-stu-id="9d254-123">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="9d254-124">65</span><span class="sxs-lookup"><span data-stu-id="9d254-124">65</span></span>

<span data-ttu-id="9d254-125">Errore sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="9d254-125">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="9d254-126">**subnet mask non valido**</span><span class="sxs-lookup"><span data-stu-id="9d254-126">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="9d254-127">66</span><span class="sxs-lookup"><span data-stu-id="9d254-127">66</span></span>

<span data-ttu-id="9d254-128">Subnet mask non valido.</span><span class="sxs-lookup"><span data-stu-id="9d254-128">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="9d254-129">**Si è verificato un errore durante l'elaborazione di un'istanza restituita**</span><span class="sxs-lookup"><span data-stu-id="9d254-129">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="9d254-130">67</span><span class="sxs-lookup"><span data-stu-id="9d254-130">67</span></span>

<span data-ttu-id="9d254-131">Si è verificato un errore durante l'elaborazione di un'istanza di restituita.</span><span class="sxs-lookup"><span data-stu-id="9d254-131">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="9d254-132">**Parametro di input non valido**</span><span class="sxs-lookup"><span data-stu-id="9d254-132">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="9d254-133">68</span><span class="sxs-lookup"><span data-stu-id="9d254-133">68</span></span>

<span data-ttu-id="9d254-134">Parametro di input non valido.</span><span class="sxs-lookup"><span data-stu-id="9d254-134">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="9d254-135">**Sono stati specificati più di 5 gateway**</span><span class="sxs-lookup"><span data-stu-id="9d254-135">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="9d254-136">69</span><span class="sxs-lookup"><span data-stu-id="9d254-136">69</span></span>

<span data-ttu-id="9d254-137">Sono stati specificati più di cinque gateway.</span><span class="sxs-lookup"><span data-stu-id="9d254-137">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="9d254-138">**Indirizzo IP non valido**</span><span class="sxs-lookup"><span data-stu-id="9d254-138">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="9d254-139">70</span><span class="sxs-lookup"><span data-stu-id="9d254-139">70</span></span>

<span data-ttu-id="9d254-140">Indirizzo IP non valido.</span><span class="sxs-lookup"><span data-stu-id="9d254-140">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="9d254-141">**Indirizzo IP gateway non valido**</span><span class="sxs-lookup"><span data-stu-id="9d254-141">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="9d254-142">71</span><span class="sxs-lookup"><span data-stu-id="9d254-142">71</span></span>

<span data-ttu-id="9d254-143">Indirizzo IP del gateway non valido.</span><span class="sxs-lookup"><span data-stu-id="9d254-143">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="9d254-144">**Si è verificato un errore durante l'accesso al registro di sistema per le informazioni richieste**</span><span class="sxs-lookup"><span data-stu-id="9d254-144">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="9d254-145">72</span><span class="sxs-lookup"><span data-stu-id="9d254-145">72</span></span>

<span data-ttu-id="9d254-146">Si è verificato un errore durante l'accesso al registro di sistema per le informazioni richieste.</span><span class="sxs-lookup"><span data-stu-id="9d254-146">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="9d254-147">**Nome di dominio non valido**</span><span class="sxs-lookup"><span data-stu-id="9d254-147">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="9d254-148">73</span><span class="sxs-lookup"><span data-stu-id="9d254-148">73</span></span>

<span data-ttu-id="9d254-149">Nome di dominio non valido.</span><span class="sxs-lookup"><span data-stu-id="9d254-149">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="9d254-150">**Nome host non valido**</span><span class="sxs-lookup"><span data-stu-id="9d254-150">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="9d254-151">74</span><span class="sxs-lookup"><span data-stu-id="9d254-151">74</span></span>

<span data-ttu-id="9d254-152">Nome host non valido.</span><span class="sxs-lookup"><span data-stu-id="9d254-152">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="9d254-153">**Nessun server WINS primario/secondario definito**</span><span class="sxs-lookup"><span data-stu-id="9d254-153">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="9d254-154">75</span><span class="sxs-lookup"><span data-stu-id="9d254-154">75</span></span>

<span data-ttu-id="9d254-155">Nessun server WINS primario o secondario definito.</span><span class="sxs-lookup"><span data-stu-id="9d254-155">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="9d254-156">**File non valido**</span><span class="sxs-lookup"><span data-stu-id="9d254-156">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="9d254-157">76</span><span class="sxs-lookup"><span data-stu-id="9d254-157">76</span></span>

<span data-ttu-id="9d254-158">File non valido.</span><span class="sxs-lookup"><span data-stu-id="9d254-158">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="9d254-159">**Percorso di sistema non valido**</span><span class="sxs-lookup"><span data-stu-id="9d254-159">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="9d254-160">77</span><span class="sxs-lookup"><span data-stu-id="9d254-160">77</span></span>

<span data-ttu-id="9d254-161">Percorso di sistema non valido.</span><span class="sxs-lookup"><span data-stu-id="9d254-161">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="9d254-162">**Copia del file non riuscita**</span><span class="sxs-lookup"><span data-stu-id="9d254-162">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="9d254-163">78</span><span class="sxs-lookup"><span data-stu-id="9d254-163">78</span></span>

<span data-ttu-id="9d254-164">Copia del file non riuscita.</span><span class="sxs-lookup"><span data-stu-id="9d254-164">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="9d254-165">**Parametro di sicurezza non valido**</span><span class="sxs-lookup"><span data-stu-id="9d254-165">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="9d254-166">79</span><span class="sxs-lookup"><span data-stu-id="9d254-166">79</span></span>

<span data-ttu-id="9d254-167">Parametro di sicurezza non valido.</span><span class="sxs-lookup"><span data-stu-id="9d254-167">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="9d254-168">**Impossibile configurare il servizio TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="9d254-168">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="9d254-169">80</span><span class="sxs-lookup"><span data-stu-id="9d254-169">80</span></span>

<span data-ttu-id="9d254-170">Impossibile configurare il servizio TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="9d254-170">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="9d254-171">**Non è possibile configurare il servizio DHCP**</span><span class="sxs-lookup"><span data-stu-id="9d254-171">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="9d254-172">81</span><span class="sxs-lookup"><span data-stu-id="9d254-172">81</span></span>

<span data-ttu-id="9d254-173">Impossibile configurare il servizio DHCP.</span><span class="sxs-lookup"><span data-stu-id="9d254-173">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="9d254-174">**Non è possibile rinnovare il lease DHCP**</span><span class="sxs-lookup"><span data-stu-id="9d254-174">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="9d254-175">82</span><span class="sxs-lookup"><span data-stu-id="9d254-175">82</span></span>

<span data-ttu-id="9d254-176">Non è possibile rinnovare il lease DHCP.</span><span class="sxs-lookup"><span data-stu-id="9d254-176">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="9d254-177">**Non è possibile rilasciare il lease DHCP**</span><span class="sxs-lookup"><span data-stu-id="9d254-177">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="9d254-178">83</span><span class="sxs-lookup"><span data-stu-id="9d254-178">83</span></span>

<span data-ttu-id="9d254-179">Impossibile rilasciare il lease DHCP.</span><span class="sxs-lookup"><span data-stu-id="9d254-179">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="9d254-180">**IP non abilitato sulla scheda**</span><span class="sxs-lookup"><span data-stu-id="9d254-180">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="9d254-181">84</span><span class="sxs-lookup"><span data-stu-id="9d254-181">84</span></span>

<span data-ttu-id="9d254-182">IP non abilitato sulla scheda.</span><span class="sxs-lookup"><span data-stu-id="9d254-182">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="9d254-183">**IPX non abilitato sull'adapter**</span><span class="sxs-lookup"><span data-stu-id="9d254-183">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="9d254-184">85</span><span class="sxs-lookup"><span data-stu-id="9d254-184">85</span></span>

<span data-ttu-id="9d254-185">IPX non abilitato sulla scheda.</span><span class="sxs-lookup"><span data-stu-id="9d254-185">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="9d254-186">**Errore limite numero frame/rete**</span><span class="sxs-lookup"><span data-stu-id="9d254-186">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="9d254-187">86</span><span class="sxs-lookup"><span data-stu-id="9d254-187">86</span></span>

<span data-ttu-id="9d254-188">Errore dei limiti del numero di rete o del frame.</span><span class="sxs-lookup"><span data-stu-id="9d254-188">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="9d254-189">**Tipo di frame non valido**</span><span class="sxs-lookup"><span data-stu-id="9d254-189">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="9d254-190">87</span><span class="sxs-lookup"><span data-stu-id="9d254-190">87</span></span>

<span data-ttu-id="9d254-191">Tipo di frame non valido.</span><span class="sxs-lookup"><span data-stu-id="9d254-191">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="9d254-192">**Numero di rete non valido**</span><span class="sxs-lookup"><span data-stu-id="9d254-192">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="9d254-193">88</span><span class="sxs-lookup"><span data-stu-id="9d254-193">88</span></span>

<span data-ttu-id="9d254-194">Numero di rete non valido.</span><span class="sxs-lookup"><span data-stu-id="9d254-194">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="9d254-195">**Numero di rete duplicato**</span><span class="sxs-lookup"><span data-stu-id="9d254-195">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="9d254-196">89</span><span class="sxs-lookup"><span data-stu-id="9d254-196">89</span></span>

<span data-ttu-id="9d254-197">Numero di rete duplicato.</span><span class="sxs-lookup"><span data-stu-id="9d254-197">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="9d254-198">**Parametro fuori limite**</span><span class="sxs-lookup"><span data-stu-id="9d254-198">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="9d254-199">90</span><span class="sxs-lookup"><span data-stu-id="9d254-199">90</span></span>

<span data-ttu-id="9d254-200">Parametro fuori limite.</span><span class="sxs-lookup"><span data-stu-id="9d254-200">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="9d254-201">**Accesso negato**</span><span class="sxs-lookup"><span data-stu-id="9d254-201">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="9d254-202">91</span><span class="sxs-lookup"><span data-stu-id="9d254-202">91</span></span>

<span data-ttu-id="9d254-203">Accesso negato.</span><span class="sxs-lookup"><span data-stu-id="9d254-203">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="9d254-204">**Memoria insufficiente**</span><span class="sxs-lookup"><span data-stu-id="9d254-204">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="9d254-205">92</span><span class="sxs-lookup"><span data-stu-id="9d254-205">92</span></span>

<span data-ttu-id="9d254-206">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="9d254-206">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="9d254-207">**Esiste già**</span><span class="sxs-lookup"><span data-stu-id="9d254-207">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="9d254-208">93</span><span class="sxs-lookup"><span data-stu-id="9d254-208">93</span></span>

<span data-ttu-id="9d254-209">Esiste già.</span><span class="sxs-lookup"><span data-stu-id="9d254-209">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="9d254-210">**Percorso, file o oggetto non trovato**</span><span class="sxs-lookup"><span data-stu-id="9d254-210">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="9d254-211">94</span><span class="sxs-lookup"><span data-stu-id="9d254-211">94</span></span>

<span data-ttu-id="9d254-212">Il percorso, il file o l'oggetto non è stato trovato.</span><span class="sxs-lookup"><span data-stu-id="9d254-212">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="9d254-213">**Non è possibile inviare una notifica al servizio**</span><span class="sxs-lookup"><span data-stu-id="9d254-213">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="9d254-214">95</span><span class="sxs-lookup"><span data-stu-id="9d254-214">95</span></span>

<span data-ttu-id="9d254-215">Impossibile notificare il servizio.</span><span class="sxs-lookup"><span data-stu-id="9d254-215">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="9d254-216">**Non è possibile inviare una notifica al servizio DNS**</span><span class="sxs-lookup"><span data-stu-id="9d254-216">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="9d254-217">96</span><span class="sxs-lookup"><span data-stu-id="9d254-217">96</span></span>

<span data-ttu-id="9d254-218">Impossibile inviare una notifica al servizio DNS.</span><span class="sxs-lookup"><span data-stu-id="9d254-218">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="9d254-219">**Interfaccia non configurabile**</span><span class="sxs-lookup"><span data-stu-id="9d254-219">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="9d254-220">97</span><span class="sxs-lookup"><span data-stu-id="9d254-220">97</span></span>

<span data-ttu-id="9d254-221">Interfaccia non configurabile.</span><span class="sxs-lookup"><span data-stu-id="9d254-221">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="9d254-222">**Non tutti i lease DHCP possono essere rilasciati/rinnovati**</span><span class="sxs-lookup"><span data-stu-id="9d254-222">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="9d254-223">98</span><span class="sxs-lookup"><span data-stu-id="9d254-223">98</span></span>

<span data-ttu-id="9d254-224">Non tutti i lease DHCP possono essere rilasciati o rinnovati.</span><span class="sxs-lookup"><span data-stu-id="9d254-224">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="9d254-225">**DHCP non abilitato sull'adapter**</span><span class="sxs-lookup"><span data-stu-id="9d254-225">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="9d254-226">100</span><span class="sxs-lookup"><span data-stu-id="9d254-226">100</span></span>

<span data-ttu-id="9d254-227">DHCP non abilitato nell'adapter.</span><span class="sxs-lookup"><span data-stu-id="9d254-227">DHCP not enabled on the adapter.</span></span>

</dd> <dt>

<span data-ttu-id="9d254-228">**Altri**</span><span class="sxs-lookup"><span data-stu-id="9d254-228">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="9d254-229">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="9d254-229">101 4294967295</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="9d254-230">Esempio</span><span class="sxs-lookup"><span data-stu-id="9d254-230">Examples</span></span>

<span data-ttu-id="9d254-231">Nell'esempio VBScript seguente viene disabilitata la protezione IP in un computer.</span><span class="sxs-lookup"><span data-stu-id="9d254-231">The following VBScript sample disables the IP Security on a computer.</span></span> <span data-ttu-id="9d254-232">Si noti che la chiamata effettiva a DisableIPSec è impostata come commento, per motivi di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="9d254-232">Note that the actual call to DisableIPSec is commented out, for safety purposes.</span></span>


```VB
strServer = "."

Set objWMI = GetObject("winmgmts:\\" & strServer & "\root\cimv2")

strWQL = "select * from Win32_NetworkAdapterConfiguration"
Set objInstances = objWMI.ExecQuery(strWQL,,48)

For Each objInstance in objInstances

 ' Uncomment next line to disable security
 ' intResult = objInstance.DisableIPSec

Next
```



## <a name="requirements"></a><span data-ttu-id="9d254-233">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9d254-233">Requirements</span></span>



| <span data-ttu-id="9d254-234">Requisito</span><span class="sxs-lookup"><span data-stu-id="9d254-234">Requirement</span></span> | <span data-ttu-id="9d254-235">Valore</span><span class="sxs-lookup"><span data-stu-id="9d254-235">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9d254-236">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9d254-236">Minimum supported client</span></span><br/> | <span data-ttu-id="9d254-237">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9d254-237">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9d254-238">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9d254-238">Minimum supported server</span></span><br/> | <span data-ttu-id="9d254-239">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9d254-239">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9d254-240">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="9d254-240">Namespace</span></span><br/>                | <span data-ttu-id="9d254-241">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="9d254-241">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9d254-242">MOF</span><span class="sxs-lookup"><span data-stu-id="9d254-242">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9d254-243"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9d254-243"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9d254-244">DLL</span><span class="sxs-lookup"><span data-stu-id="9d254-244">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9d254-245"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9d254-245"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9d254-246">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9d254-246">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d254-247">Classi hardware del sistema del computer</span><span class="sxs-lookup"><span data-stu-id="9d254-247">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="9d254-248">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="9d254-248">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="9d254-249">Attività WMI: rete</span><span class="sxs-lookup"><span data-stu-id="9d254-249">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="9d254-250">Attività WMI: account e domini</span><span class="sxs-lookup"><span data-stu-id="9d254-250">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="9d254-251">Supporto di IPv6 e IPv4 in WMI</span><span class="sxs-lookup"><span data-stu-id="9d254-251">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

