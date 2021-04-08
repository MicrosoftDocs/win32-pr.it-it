---
description: Il metodo statico della classe WMI EnableIPFilterSec viene usato per abilitare Internet Protocol Security (IPsec) globalmente tra tutte le schede di rete con binding IP.
ms.assetid: 565acc18-61e7-473e-b2cc-41f0e8c29193
ms.tgt_platform: multiple
title: Metodo EnableIPFilterSec della classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.EnableIPFilterSec
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3429e2c2ba78e013da9195961b76ff84ffda9b68
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877602"
---
# <a name="enableipfiltersec-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="07a9d-103">Metodo EnableIPFilterSec della \_ classe NetworkAdapterConfiguration Win32</span><span class="sxs-lookup"><span data-stu-id="07a9d-103">EnableIPFilterSec method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="07a9d-104">Il metodo statico della [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **EnableIPFilterSec** viene usato per abilitare Internet Protocol Security (IPSec) globalmente tra tutte le schede di rete con binding IP.</span><span class="sxs-lookup"><span data-stu-id="07a9d-104">The **EnableIPFilterSec** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to enable Internet Protocol security (IPsec) globally across all IP-bound network adapters.</span></span>

<span data-ttu-id="07a9d-105">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="07a9d-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="07a9d-106">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="07a9d-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="07a9d-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="07a9d-107">Syntax</span></span>


```mof
uint32 EnableIPFilterSec(
  [in] boolean IPFilterSecurityEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="07a9d-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="07a9d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07a9d-109">*IPFilterSecurityEnabled* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="07a9d-109">*IPFilterSecurityEnabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07a9d-110">Se **true**, IPSec viene abilitato globalmente in tutte le schede di rete con binding IP.</span><span class="sxs-lookup"><span data-stu-id="07a9d-110">If **true**, IPsec is enabled globally across all IP-bound network adapters.</span></span> <span data-ttu-id="07a9d-111">Se **false**, è consentito il flusso non filtrato di tutto il traffico di porta e protocollo.</span><span class="sxs-lookup"><span data-stu-id="07a9d-111">If **false**, all port and protocol traffic is allowed to flow unfiltered.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="07a9d-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="07a9d-112">Return value</span></span>

<span data-ttu-id="07a9d-113">Restituisce un valore pari a 0 (zero) per un completamento corretto quando non è richiesto un riavvio, 1 (uno) per un completamento corretto quando è necessario un riavvio e qualsiasi altro numero se si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="07a9d-113">Returns a value of 0 (zero) for a successful completion when a reboot is not required, 1 (one) for a successful completion when a reboot is required, and any other number if there is an error.</span></span> <span data-ttu-id="07a9d-114">Per ulteriori informazioni sui codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="07a9d-114">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="07a9d-115">Per i valori **HRESULT** generali, vedere [codici di errore di sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="07a9d-115">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="07a9d-116">**Operazione completata, non è necessario riavviare il computer**</span><span class="sxs-lookup"><span data-stu-id="07a9d-116">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="07a9d-117">0</span><span class="sxs-lookup"><span data-stu-id="07a9d-117">0</span></span>

<span data-ttu-id="07a9d-118">Operazione completata, non è necessario riavviare il computer.</span><span class="sxs-lookup"><span data-stu-id="07a9d-118">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="07a9d-119">**Operazione completata, riavvio richiesto**</span><span class="sxs-lookup"><span data-stu-id="07a9d-119">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="07a9d-120">1</span><span class="sxs-lookup"><span data-stu-id="07a9d-120">1</span></span>

<span data-ttu-id="07a9d-121">Operazione completata, è necessario riavviare il computer.</span><span class="sxs-lookup"><span data-stu-id="07a9d-121">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="07a9d-122">**Metodo non supportato in questa piattaforma**</span><span class="sxs-lookup"><span data-stu-id="07a9d-122">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="07a9d-123">64</span><span class="sxs-lookup"><span data-stu-id="07a9d-123">64</span></span>

<span data-ttu-id="07a9d-124">Metodo non supportato in questa piattaforma.</span><span class="sxs-lookup"><span data-stu-id="07a9d-124">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="07a9d-125">**Errore sconosciuto**</span><span class="sxs-lookup"><span data-stu-id="07a9d-125">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="07a9d-126">65</span><span class="sxs-lookup"><span data-stu-id="07a9d-126">65</span></span>

<span data-ttu-id="07a9d-127">Errore sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="07a9d-127">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="07a9d-128">**subnet mask non valido**</span><span class="sxs-lookup"><span data-stu-id="07a9d-128">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="07a9d-129">66</span><span class="sxs-lookup"><span data-stu-id="07a9d-129">66</span></span>

<span data-ttu-id="07a9d-130">Subnet mask non valido.</span><span class="sxs-lookup"><span data-stu-id="07a9d-130">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="07a9d-131">**Si è verificato un errore durante l'elaborazione di un'istanza restituita**</span><span class="sxs-lookup"><span data-stu-id="07a9d-131">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="07a9d-132">67</span><span class="sxs-lookup"><span data-stu-id="07a9d-132">67</span></span>

<span data-ttu-id="07a9d-133">Si è verificato un errore durante l'elaborazione di un'istanza di restituita.</span><span class="sxs-lookup"><span data-stu-id="07a9d-133">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="07a9d-134">**Parametro di input non valido**</span><span class="sxs-lookup"><span data-stu-id="07a9d-134">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="07a9d-135">68</span><span class="sxs-lookup"><span data-stu-id="07a9d-135">68</span></span>

<span data-ttu-id="07a9d-136">Parametro di input non valido.</span><span class="sxs-lookup"><span data-stu-id="07a9d-136">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="07a9d-137">**Sono stati specificati più di 5 gateway**</span><span class="sxs-lookup"><span data-stu-id="07a9d-137">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="07a9d-138">69</span><span class="sxs-lookup"><span data-stu-id="07a9d-138">69</span></span>

<span data-ttu-id="07a9d-139">Sono stati specificati più di cinque gateway.</span><span class="sxs-lookup"><span data-stu-id="07a9d-139">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="07a9d-140">**Indirizzo IP non valido**</span><span class="sxs-lookup"><span data-stu-id="07a9d-140">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="07a9d-141">70</span><span class="sxs-lookup"><span data-stu-id="07a9d-141">70</span></span>

<span data-ttu-id="07a9d-142">Indirizzo IP non valido.</span><span class="sxs-lookup"><span data-stu-id="07a9d-142">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="07a9d-143">**Indirizzo IP gateway non valido**</span><span class="sxs-lookup"><span data-stu-id="07a9d-143">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="07a9d-144">71</span><span class="sxs-lookup"><span data-stu-id="07a9d-144">71</span></span>

<span data-ttu-id="07a9d-145">Indirizzo IP del gateway non valido.</span><span class="sxs-lookup"><span data-stu-id="07a9d-145">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="07a9d-146">**Si è verificato un errore durante l'accesso al registro di sistema per le informazioni richieste**</span><span class="sxs-lookup"><span data-stu-id="07a9d-146">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="07a9d-147">72</span><span class="sxs-lookup"><span data-stu-id="07a9d-147">72</span></span>

<span data-ttu-id="07a9d-148">Si è verificato un errore durante l'accesso al registro di sistema per le informazioni richieste.</span><span class="sxs-lookup"><span data-stu-id="07a9d-148">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="07a9d-149">**Nome di dominio non valido**</span><span class="sxs-lookup"><span data-stu-id="07a9d-149">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="07a9d-150">73</span><span class="sxs-lookup"><span data-stu-id="07a9d-150">73</span></span>

<span data-ttu-id="07a9d-151">Nome di dominio non valido.</span><span class="sxs-lookup"><span data-stu-id="07a9d-151">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="07a9d-152">**Nome host non valido**</span><span class="sxs-lookup"><span data-stu-id="07a9d-152">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="07a9d-153">74</span><span class="sxs-lookup"><span data-stu-id="07a9d-153">74</span></span>

<span data-ttu-id="07a9d-154">Nome host non valido.</span><span class="sxs-lookup"><span data-stu-id="07a9d-154">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="07a9d-155">**Nessun server WINS primario/secondario definito**</span><span class="sxs-lookup"><span data-stu-id="07a9d-155">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="07a9d-156">75</span><span class="sxs-lookup"><span data-stu-id="07a9d-156">75</span></span>

<span data-ttu-id="07a9d-157">Nessun server WINS primario o secondario definito.</span><span class="sxs-lookup"><span data-stu-id="07a9d-157">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="07a9d-158">**File non valido**</span><span class="sxs-lookup"><span data-stu-id="07a9d-158">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="07a9d-159">76</span><span class="sxs-lookup"><span data-stu-id="07a9d-159">76</span></span>

<span data-ttu-id="07a9d-160">File non valido.</span><span class="sxs-lookup"><span data-stu-id="07a9d-160">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="07a9d-161">**Percorso di sistema non valido**</span><span class="sxs-lookup"><span data-stu-id="07a9d-161">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="07a9d-162">77</span><span class="sxs-lookup"><span data-stu-id="07a9d-162">77</span></span>

<span data-ttu-id="07a9d-163">Percorso di sistema non valido.</span><span class="sxs-lookup"><span data-stu-id="07a9d-163">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="07a9d-164">**Copia del file non riuscita**</span><span class="sxs-lookup"><span data-stu-id="07a9d-164">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="07a9d-165">78</span><span class="sxs-lookup"><span data-stu-id="07a9d-165">78</span></span>

<span data-ttu-id="07a9d-166">Copia del file non riuscita.</span><span class="sxs-lookup"><span data-stu-id="07a9d-166">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="07a9d-167">**Parametro di sicurezza non valido**</span><span class="sxs-lookup"><span data-stu-id="07a9d-167">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="07a9d-168">79</span><span class="sxs-lookup"><span data-stu-id="07a9d-168">79</span></span>

<span data-ttu-id="07a9d-169">Parametro di sicurezza non valido.</span><span class="sxs-lookup"><span data-stu-id="07a9d-169">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="07a9d-170">**Impossibile configurare il servizio TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="07a9d-170">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="07a9d-171">80</span><span class="sxs-lookup"><span data-stu-id="07a9d-171">80</span></span>

<span data-ttu-id="07a9d-172">Impossibile configurare il servizio TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="07a9d-172">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="07a9d-173">**Non è possibile configurare il servizio DHCP**</span><span class="sxs-lookup"><span data-stu-id="07a9d-173">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="07a9d-174">81</span><span class="sxs-lookup"><span data-stu-id="07a9d-174">81</span></span>

<span data-ttu-id="07a9d-175">Impossibile configurare il servizio DHCP.</span><span class="sxs-lookup"><span data-stu-id="07a9d-175">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="07a9d-176">**Non è possibile rinnovare il lease DHCP**</span><span class="sxs-lookup"><span data-stu-id="07a9d-176">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="07a9d-177">82</span><span class="sxs-lookup"><span data-stu-id="07a9d-177">82</span></span>

<span data-ttu-id="07a9d-178">Non è possibile rinnovare il lease DHCP.</span><span class="sxs-lookup"><span data-stu-id="07a9d-178">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="07a9d-179">**Non è possibile rilasciare il lease DHCP**</span><span class="sxs-lookup"><span data-stu-id="07a9d-179">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="07a9d-180">83</span><span class="sxs-lookup"><span data-stu-id="07a9d-180">83</span></span>

<span data-ttu-id="07a9d-181">Impossibile rilasciare il lease DHCP.</span><span class="sxs-lookup"><span data-stu-id="07a9d-181">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="07a9d-182">**IP non abilitato sulla scheda**</span><span class="sxs-lookup"><span data-stu-id="07a9d-182">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="07a9d-183">84</span><span class="sxs-lookup"><span data-stu-id="07a9d-183">84</span></span>

<span data-ttu-id="07a9d-184">IP non abilitato sulla scheda.</span><span class="sxs-lookup"><span data-stu-id="07a9d-184">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="07a9d-185">**IPX non abilitato sull'adapter**</span><span class="sxs-lookup"><span data-stu-id="07a9d-185">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="07a9d-186">85</span><span class="sxs-lookup"><span data-stu-id="07a9d-186">85</span></span>

<span data-ttu-id="07a9d-187">IPX non abilitato sulla scheda.</span><span class="sxs-lookup"><span data-stu-id="07a9d-187">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="07a9d-188">**Errore limite numero frame/rete**</span><span class="sxs-lookup"><span data-stu-id="07a9d-188">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="07a9d-189">86</span><span class="sxs-lookup"><span data-stu-id="07a9d-189">86</span></span>

<span data-ttu-id="07a9d-190">Errore dei limiti del numero di rete o del frame.</span><span class="sxs-lookup"><span data-stu-id="07a9d-190">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="07a9d-191">**Tipo di frame non valido**</span><span class="sxs-lookup"><span data-stu-id="07a9d-191">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="07a9d-192">87</span><span class="sxs-lookup"><span data-stu-id="07a9d-192">87</span></span>

<span data-ttu-id="07a9d-193">Tipo di frame non valido.</span><span class="sxs-lookup"><span data-stu-id="07a9d-193">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="07a9d-194">**Numero di rete non valido**</span><span class="sxs-lookup"><span data-stu-id="07a9d-194">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="07a9d-195">88</span><span class="sxs-lookup"><span data-stu-id="07a9d-195">88</span></span>

<span data-ttu-id="07a9d-196">Numero di rete non valido.</span><span class="sxs-lookup"><span data-stu-id="07a9d-196">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="07a9d-197">**Numero di rete duplicato**</span><span class="sxs-lookup"><span data-stu-id="07a9d-197">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="07a9d-198">89</span><span class="sxs-lookup"><span data-stu-id="07a9d-198">89</span></span>

<span data-ttu-id="07a9d-199">Numero di rete duplicato.</span><span class="sxs-lookup"><span data-stu-id="07a9d-199">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="07a9d-200">**Parametro fuori limite**</span><span class="sxs-lookup"><span data-stu-id="07a9d-200">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="07a9d-201">90</span><span class="sxs-lookup"><span data-stu-id="07a9d-201">90</span></span>

<span data-ttu-id="07a9d-202">Parametro fuori limite.</span><span class="sxs-lookup"><span data-stu-id="07a9d-202">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="07a9d-203">**Accesso negato**</span><span class="sxs-lookup"><span data-stu-id="07a9d-203">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="07a9d-204">91</span><span class="sxs-lookup"><span data-stu-id="07a9d-204">91</span></span>

<span data-ttu-id="07a9d-205">Accesso negato.</span><span class="sxs-lookup"><span data-stu-id="07a9d-205">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="07a9d-206">**Memoria insufficiente**</span><span class="sxs-lookup"><span data-stu-id="07a9d-206">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="07a9d-207">92</span><span class="sxs-lookup"><span data-stu-id="07a9d-207">92</span></span>

<span data-ttu-id="07a9d-208">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="07a9d-208">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="07a9d-209">**Esiste già**</span><span class="sxs-lookup"><span data-stu-id="07a9d-209">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="07a9d-210">93</span><span class="sxs-lookup"><span data-stu-id="07a9d-210">93</span></span>

<span data-ttu-id="07a9d-211">Esiste già.</span><span class="sxs-lookup"><span data-stu-id="07a9d-211">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="07a9d-212">**Percorso, file o oggetto non trovato**</span><span class="sxs-lookup"><span data-stu-id="07a9d-212">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="07a9d-213">94</span><span class="sxs-lookup"><span data-stu-id="07a9d-213">94</span></span>

<span data-ttu-id="07a9d-214">Il percorso, il file o l'oggetto non è stato trovato.</span><span class="sxs-lookup"><span data-stu-id="07a9d-214">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="07a9d-215">**Non è possibile inviare una notifica al servizio**</span><span class="sxs-lookup"><span data-stu-id="07a9d-215">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="07a9d-216">95</span><span class="sxs-lookup"><span data-stu-id="07a9d-216">95</span></span>

<span data-ttu-id="07a9d-217">Impossibile notificare il servizio.</span><span class="sxs-lookup"><span data-stu-id="07a9d-217">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="07a9d-218">**Non è possibile inviare una notifica al servizio DNS**</span><span class="sxs-lookup"><span data-stu-id="07a9d-218">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="07a9d-219">96</span><span class="sxs-lookup"><span data-stu-id="07a9d-219">96</span></span>

<span data-ttu-id="07a9d-220">Impossibile inviare una notifica al servizio DNS.</span><span class="sxs-lookup"><span data-stu-id="07a9d-220">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="07a9d-221">**Interfaccia non configurabile**</span><span class="sxs-lookup"><span data-stu-id="07a9d-221">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="07a9d-222">97</span><span class="sxs-lookup"><span data-stu-id="07a9d-222">97</span></span>

<span data-ttu-id="07a9d-223">Interfaccia non configurabile.</span><span class="sxs-lookup"><span data-stu-id="07a9d-223">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="07a9d-224">**Non tutti i lease DHCP possono essere rilasciati/rinnovati**</span><span class="sxs-lookup"><span data-stu-id="07a9d-224">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="07a9d-225">98</span><span class="sxs-lookup"><span data-stu-id="07a9d-225">98</span></span>

<span data-ttu-id="07a9d-226">Non tutti i lease DHCP possono essere rilasciati o rinnovati.</span><span class="sxs-lookup"><span data-stu-id="07a9d-226">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="07a9d-227">**DHCP non abilitato sull'adapter**</span><span class="sxs-lookup"><span data-stu-id="07a9d-227">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="07a9d-228">100</span><span class="sxs-lookup"><span data-stu-id="07a9d-228">100</span></span>

<span data-ttu-id="07a9d-229">DHCP non abilitato nell'adapter.</span><span class="sxs-lookup"><span data-stu-id="07a9d-229">DHCP not enabled on the adapter.</span></span>

</dd> <dt>

<span data-ttu-id="07a9d-230">**Altri**</span><span class="sxs-lookup"><span data-stu-id="07a9d-230">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="07a9d-231">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="07a9d-231">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="07a9d-232">Commenti</span><span class="sxs-lookup"><span data-stu-id="07a9d-232">Remarks</span></span>

<span data-ttu-id="07a9d-233">Con la sicurezza abilitata, è possibile controllare le caratteristiche di sicurezza operativa per una scheda di rete usando il metodo [**EnableIPSec**](enableipsec-method-in-class-win32-networkadapterconfiguration.md) specifico della scheda di rete.</span><span class="sxs-lookup"><span data-stu-id="07a9d-233">With security enabled, the operational security characteristics for any one network adapter can be controlled by using the network adapter-specific [**EnableIPSec**](enableipsec-method-in-class-win32-networkadapterconfiguration.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="07a9d-234">Esempio</span><span class="sxs-lookup"><span data-stu-id="07a9d-234">Examples</span></span>

<span data-ttu-id="07a9d-235">Il codice seguente, tratto dall'esempio [Enable IPFilter Security on all network adattations](https://Gallery.TechNet.Microsoft.Com/f8e56021-5a54-4554-b7b6-d76cc40d8d1d) on TechNet Gallery, Abilita la sicurezza del filtro IP per tutte le schede di rete installate in un computer.</span><span class="sxs-lookup"><span data-stu-id="07a9d-235">The following code, taken from the [Enable IPFilter Security on All Network Adapters](https://Gallery.TechNet.Microsoft.Com/f8e56021-5a54-4554-b7b6-d76cc40d8d1d) sample on TechNet Gallery, enables IP filter security for all the network adapters installed in a computer.</span></span>


```VB
On Error Resume Next 
 
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set objNetworkSettings = objWMIService.Get("Win32_NetworkAdapterConfiguration") 
objNetworkSettings.EnableIPFilterSec(True)
```



## <a name="requirements"></a><span data-ttu-id="07a9d-236">Requisiti</span><span class="sxs-lookup"><span data-stu-id="07a9d-236">Requirements</span></span>



| <span data-ttu-id="07a9d-237">Requisito</span><span class="sxs-lookup"><span data-stu-id="07a9d-237">Requirement</span></span> | <span data-ttu-id="07a9d-238">Valore</span><span class="sxs-lookup"><span data-stu-id="07a9d-238">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="07a9d-239">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="07a9d-239">Minimum supported client</span></span><br/> | <span data-ttu-id="07a9d-240">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="07a9d-240">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="07a9d-241">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="07a9d-241">Minimum supported server</span></span><br/> | <span data-ttu-id="07a9d-242">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="07a9d-242">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="07a9d-243">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="07a9d-243">Namespace</span></span><br/>                | <span data-ttu-id="07a9d-244">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="07a9d-244">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="07a9d-245">MOF</span><span class="sxs-lookup"><span data-stu-id="07a9d-245">MOF</span></span><br/>                      | <dl> <span data-ttu-id="07a9d-246"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="07a9d-246"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="07a9d-247">DLL</span><span class="sxs-lookup"><span data-stu-id="07a9d-247">DLL</span></span><br/>                      | <dl> <span data-ttu-id="07a9d-248"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="07a9d-248"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07a9d-249">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="07a9d-249">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07a9d-250">Classi hardware del sistema del computer</span><span class="sxs-lookup"><span data-stu-id="07a9d-250">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="07a9d-251">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="07a9d-251">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="07a9d-252">Attività WMI: rete</span><span class="sxs-lookup"><span data-stu-id="07a9d-252">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="07a9d-253">Attività WMI: account e domini</span><span class="sxs-lookup"><span data-stu-id="07a9d-253">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="07a9d-254">Supporto di IPv6 e IPv4 in WMI</span><span class="sxs-lookup"><span data-stu-id="07a9d-254">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

