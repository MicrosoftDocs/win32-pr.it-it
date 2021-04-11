---
description: Il metodo statico della classe WMI SetTcpUseRFC1122UrgentPointer viene utilizzato per specificare se TCP utilizza la specifica RFC 1122 per i dati urgenti o la modalità utilizzata dai sistemi derivati di Berkeley Software Design (BSD).
ms.assetid: f8d07690-2723-4bc3-b15f-a24d575456a7
ms.tgt_platform: multiple
title: Metodo SetTcpUseRFC1122UrgentPointer della classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetTcpUseRFC1122UrgentPointer
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 928a809211288eb7f024c735ce033b819e5d49f7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126855"
---
# <a name="settcpuserfc1122urgentpointer-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="f66e8-103">Metodo SetTcpUseRFC1122UrgentPointer della \_ classe NetworkAdapterConfiguration Win32</span><span class="sxs-lookup"><span data-stu-id="f66e8-103">SetTcpUseRFC1122UrgentPointer method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="f66e8-104">Il metodo statico della [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetTcpUseRFC1122UrgentPointer** viene utilizzato per specificare se TCP utilizza la specifica RFC 1122 per i dati urgenti o la modalità utilizzata dai sistemi derivati di Berkeley Software Design (BSD).</span><span class="sxs-lookup"><span data-stu-id="f66e8-104">The **SetTcpUseRFC1122UrgentPointer** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to specify whether TCP uses the RFC 1122 specification for urgent data, or the mode used by Berkeley Software Design (BSD) derived systems.</span></span>

<span data-ttu-id="f66e8-105">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="f66e8-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="f66e8-106">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="f66e8-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="f66e8-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f66e8-107">Syntax</span></span>


```mof
uint32 SetTcpUseRFC1122UrgentPointer(
  [in] boolean TcpUseRFC1122UrgentPointer
);
```



## <a name="parameters"></a><span data-ttu-id="f66e8-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="f66e8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f66e8-109">*TcpUseRFC1122UrgentPointer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f66e8-109">*TcpUseRFC1122UrgentPointer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f66e8-110">Se **true**, TCP utilizza la specifica RFC 1122.</span><span class="sxs-lookup"><span data-stu-id="f66e8-110">If **true**, TCP uses the RFC 1122 specification.</span></span> <span data-ttu-id="f66e8-111">Se **false**, i dati urgenti vengono inviati in modalità utilizzata dai sistemi derivati da BSD.</span><span class="sxs-lookup"><span data-stu-id="f66e8-111">If **false**, urgent data is sent in the mode used by BSD-derived systems.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f66e8-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f66e8-112">Return value</span></span>

<span data-ttu-id="f66e8-113">Restituisce un valore pari a 0 (zero) per un completamento corretto quando non è richiesto il riavvio, 1 (uno) per un completamento corretto quando è necessario un riavvio e un numero diverso se si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="f66e8-113">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="f66e8-114">Per ulteriori informazioni sui codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="f66e8-114">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="f66e8-115">Per i valori **HRESULT** generali, vedere [codici di errore di sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="f66e8-115">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="f66e8-116">**Operazione completata, non è necessario riavviare il computer**</span><span class="sxs-lookup"><span data-stu-id="f66e8-116">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="f66e8-117">0</span><span class="sxs-lookup"><span data-stu-id="f66e8-117">0</span></span>

<span data-ttu-id="f66e8-118">Operazione completata, non è necessario riavviare il computer.</span><span class="sxs-lookup"><span data-stu-id="f66e8-118">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="f66e8-119">**Operazione completata, riavvio richiesto**</span><span class="sxs-lookup"><span data-stu-id="f66e8-119">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="f66e8-120">1</span><span class="sxs-lookup"><span data-stu-id="f66e8-120">1</span></span>

<span data-ttu-id="f66e8-121">Operazione completata, è necessario riavviare il computer.</span><span class="sxs-lookup"><span data-stu-id="f66e8-121">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="f66e8-122">**Metodo non supportato in questa piattaforma**</span><span class="sxs-lookup"><span data-stu-id="f66e8-122">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="f66e8-123">64</span><span class="sxs-lookup"><span data-stu-id="f66e8-123">64</span></span>

<span data-ttu-id="f66e8-124">Metodo non supportato in questa piattaforma.</span><span class="sxs-lookup"><span data-stu-id="f66e8-124">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="f66e8-125">**Errore sconosciuto**</span><span class="sxs-lookup"><span data-stu-id="f66e8-125">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="f66e8-126">65</span><span class="sxs-lookup"><span data-stu-id="f66e8-126">65</span></span>

<span data-ttu-id="f66e8-127">Errore sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="f66e8-127">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="f66e8-128">**subnet mask non valido**</span><span class="sxs-lookup"><span data-stu-id="f66e8-128">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="f66e8-129">66</span><span class="sxs-lookup"><span data-stu-id="f66e8-129">66</span></span>

<span data-ttu-id="f66e8-130">Subnet mask non valido.</span><span class="sxs-lookup"><span data-stu-id="f66e8-130">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="f66e8-131">**Si è verificato un errore durante l'elaborazione di un'istanza restituita**</span><span class="sxs-lookup"><span data-stu-id="f66e8-131">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="f66e8-132">67</span><span class="sxs-lookup"><span data-stu-id="f66e8-132">67</span></span>

<span data-ttu-id="f66e8-133">Si è verificato un errore durante l'elaborazione di un'istanza di restituita.</span><span class="sxs-lookup"><span data-stu-id="f66e8-133">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="f66e8-134">**Parametro di input non valido**</span><span class="sxs-lookup"><span data-stu-id="f66e8-134">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="f66e8-135">68</span><span class="sxs-lookup"><span data-stu-id="f66e8-135">68</span></span>

<span data-ttu-id="f66e8-136">Parametro di input non valido.</span><span class="sxs-lookup"><span data-stu-id="f66e8-136">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="f66e8-137">**Sono stati specificati più di 5 gateway**</span><span class="sxs-lookup"><span data-stu-id="f66e8-137">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="f66e8-138">69</span><span class="sxs-lookup"><span data-stu-id="f66e8-138">69</span></span>

<span data-ttu-id="f66e8-139">Sono stati specificati più di cinque gateway.</span><span class="sxs-lookup"><span data-stu-id="f66e8-139">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="f66e8-140">**Indirizzo IP non valido**</span><span class="sxs-lookup"><span data-stu-id="f66e8-140">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="f66e8-141">70</span><span class="sxs-lookup"><span data-stu-id="f66e8-141">70</span></span>

<span data-ttu-id="f66e8-142">Indirizzo IP non valido.</span><span class="sxs-lookup"><span data-stu-id="f66e8-142">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="f66e8-143">**Indirizzo IP gateway non valido**</span><span class="sxs-lookup"><span data-stu-id="f66e8-143">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="f66e8-144">71</span><span class="sxs-lookup"><span data-stu-id="f66e8-144">71</span></span>

<span data-ttu-id="f66e8-145">Indirizzo IP del gateway non valido.</span><span class="sxs-lookup"><span data-stu-id="f66e8-145">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="f66e8-146">**Si è verificato un errore durante l'accesso al registro di sistema per le informazioni richieste**</span><span class="sxs-lookup"><span data-stu-id="f66e8-146">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="f66e8-147">72</span><span class="sxs-lookup"><span data-stu-id="f66e8-147">72</span></span>

<span data-ttu-id="f66e8-148">Si è verificato un errore durante l'accesso al registro di sistema per le informazioni richieste.</span><span class="sxs-lookup"><span data-stu-id="f66e8-148">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="f66e8-149">**Nome di dominio non valido**</span><span class="sxs-lookup"><span data-stu-id="f66e8-149">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="f66e8-150">73</span><span class="sxs-lookup"><span data-stu-id="f66e8-150">73</span></span>

<span data-ttu-id="f66e8-151">Nome di dominio non valido.</span><span class="sxs-lookup"><span data-stu-id="f66e8-151">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="f66e8-152">**Nome host non valido**</span><span class="sxs-lookup"><span data-stu-id="f66e8-152">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="f66e8-153">74</span><span class="sxs-lookup"><span data-stu-id="f66e8-153">74</span></span>

<span data-ttu-id="f66e8-154">Nome host non valido.</span><span class="sxs-lookup"><span data-stu-id="f66e8-154">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="f66e8-155">**Nessun server WINS primario/secondario definito**</span><span class="sxs-lookup"><span data-stu-id="f66e8-155">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="f66e8-156">75</span><span class="sxs-lookup"><span data-stu-id="f66e8-156">75</span></span>

<span data-ttu-id="f66e8-157">Nessun server WINS primario o secondario definito.</span><span class="sxs-lookup"><span data-stu-id="f66e8-157">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="f66e8-158">**File non valido**</span><span class="sxs-lookup"><span data-stu-id="f66e8-158">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="f66e8-159">76</span><span class="sxs-lookup"><span data-stu-id="f66e8-159">76</span></span>

<span data-ttu-id="f66e8-160">File non valido.</span><span class="sxs-lookup"><span data-stu-id="f66e8-160">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="f66e8-161">**Percorso di sistema non valido**</span><span class="sxs-lookup"><span data-stu-id="f66e8-161">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="f66e8-162">77</span><span class="sxs-lookup"><span data-stu-id="f66e8-162">77</span></span>

<span data-ttu-id="f66e8-163">Percorso di sistema non valido.</span><span class="sxs-lookup"><span data-stu-id="f66e8-163">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="f66e8-164">**Copia del file non riuscita**</span><span class="sxs-lookup"><span data-stu-id="f66e8-164">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="f66e8-165">78</span><span class="sxs-lookup"><span data-stu-id="f66e8-165">78</span></span>

<span data-ttu-id="f66e8-166">Copia del file non riuscita.</span><span class="sxs-lookup"><span data-stu-id="f66e8-166">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="f66e8-167">**Parametro di sicurezza non valido**</span><span class="sxs-lookup"><span data-stu-id="f66e8-167">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="f66e8-168">79</span><span class="sxs-lookup"><span data-stu-id="f66e8-168">79</span></span>

<span data-ttu-id="f66e8-169">Parametro di sicurezza non valido.</span><span class="sxs-lookup"><span data-stu-id="f66e8-169">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="f66e8-170">**Impossibile configurare il servizio TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="f66e8-170">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="f66e8-171">80</span><span class="sxs-lookup"><span data-stu-id="f66e8-171">80</span></span>

<span data-ttu-id="f66e8-172">Impossibile configurare il servizio TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="f66e8-172">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="f66e8-173">**Non è possibile configurare il servizio DHCP**</span><span class="sxs-lookup"><span data-stu-id="f66e8-173">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="f66e8-174">81</span><span class="sxs-lookup"><span data-stu-id="f66e8-174">81</span></span>

<span data-ttu-id="f66e8-175">Impossibile configurare il servizio DHCP.</span><span class="sxs-lookup"><span data-stu-id="f66e8-175">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="f66e8-176">**Non è possibile rinnovare il lease DHCP**</span><span class="sxs-lookup"><span data-stu-id="f66e8-176">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="f66e8-177">82</span><span class="sxs-lookup"><span data-stu-id="f66e8-177">82</span></span>

<span data-ttu-id="f66e8-178">Non è possibile rinnovare il lease DHCP.</span><span class="sxs-lookup"><span data-stu-id="f66e8-178">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="f66e8-179">**Non è possibile rilasciare il lease DHCP**</span><span class="sxs-lookup"><span data-stu-id="f66e8-179">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="f66e8-180">83</span><span class="sxs-lookup"><span data-stu-id="f66e8-180">83</span></span>

<span data-ttu-id="f66e8-181">Impossibile rilasciare il lease DHCP.</span><span class="sxs-lookup"><span data-stu-id="f66e8-181">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="f66e8-182">**IP non abilitato sulla scheda**</span><span class="sxs-lookup"><span data-stu-id="f66e8-182">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="f66e8-183">84</span><span class="sxs-lookup"><span data-stu-id="f66e8-183">84</span></span>

<span data-ttu-id="f66e8-184">IP non abilitato sulla scheda.</span><span class="sxs-lookup"><span data-stu-id="f66e8-184">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="f66e8-185">**IPX non abilitato sull'adapter**</span><span class="sxs-lookup"><span data-stu-id="f66e8-185">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="f66e8-186">85</span><span class="sxs-lookup"><span data-stu-id="f66e8-186">85</span></span>

<span data-ttu-id="f66e8-187">IPX non abilitato sulla scheda.</span><span class="sxs-lookup"><span data-stu-id="f66e8-187">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="f66e8-188">**Errore limite numero frame/rete**</span><span class="sxs-lookup"><span data-stu-id="f66e8-188">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="f66e8-189">86</span><span class="sxs-lookup"><span data-stu-id="f66e8-189">86</span></span>

<span data-ttu-id="f66e8-190">Errore dei limiti del numero di rete o del frame.</span><span class="sxs-lookup"><span data-stu-id="f66e8-190">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="f66e8-191">**Tipo di frame non valido**</span><span class="sxs-lookup"><span data-stu-id="f66e8-191">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="f66e8-192">87</span><span class="sxs-lookup"><span data-stu-id="f66e8-192">87</span></span>

<span data-ttu-id="f66e8-193">Tipo di frame non valido.</span><span class="sxs-lookup"><span data-stu-id="f66e8-193">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="f66e8-194">**Numero di rete non valido**</span><span class="sxs-lookup"><span data-stu-id="f66e8-194">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="f66e8-195">88</span><span class="sxs-lookup"><span data-stu-id="f66e8-195">88</span></span>

<span data-ttu-id="f66e8-196">Numero di rete non valido.</span><span class="sxs-lookup"><span data-stu-id="f66e8-196">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="f66e8-197">**Numero di rete duplicato**</span><span class="sxs-lookup"><span data-stu-id="f66e8-197">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="f66e8-198">89</span><span class="sxs-lookup"><span data-stu-id="f66e8-198">89</span></span>

<span data-ttu-id="f66e8-199">Numero di rete duplicato.</span><span class="sxs-lookup"><span data-stu-id="f66e8-199">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="f66e8-200">**Parametro fuori limite**</span><span class="sxs-lookup"><span data-stu-id="f66e8-200">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="f66e8-201">90</span><span class="sxs-lookup"><span data-stu-id="f66e8-201">90</span></span>

<span data-ttu-id="f66e8-202">Parametro fuori limite.</span><span class="sxs-lookup"><span data-stu-id="f66e8-202">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="f66e8-203">**Accesso negato**</span><span class="sxs-lookup"><span data-stu-id="f66e8-203">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="f66e8-204">91</span><span class="sxs-lookup"><span data-stu-id="f66e8-204">91</span></span>

<span data-ttu-id="f66e8-205">Accesso negato.</span><span class="sxs-lookup"><span data-stu-id="f66e8-205">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="f66e8-206">**Memoria insufficiente**</span><span class="sxs-lookup"><span data-stu-id="f66e8-206">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="f66e8-207">92</span><span class="sxs-lookup"><span data-stu-id="f66e8-207">92</span></span>

<span data-ttu-id="f66e8-208">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="f66e8-208">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="f66e8-209">**Esiste già**</span><span class="sxs-lookup"><span data-stu-id="f66e8-209">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="f66e8-210">93</span><span class="sxs-lookup"><span data-stu-id="f66e8-210">93</span></span>

<span data-ttu-id="f66e8-211">Esiste già.</span><span class="sxs-lookup"><span data-stu-id="f66e8-211">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="f66e8-212">**Percorso, file o oggetto non trovato**</span><span class="sxs-lookup"><span data-stu-id="f66e8-212">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="f66e8-213">94</span><span class="sxs-lookup"><span data-stu-id="f66e8-213">94</span></span>

<span data-ttu-id="f66e8-214">Il percorso, il file o l'oggetto non è stato trovato.</span><span class="sxs-lookup"><span data-stu-id="f66e8-214">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="f66e8-215">**Non è possibile inviare una notifica al servizio**</span><span class="sxs-lookup"><span data-stu-id="f66e8-215">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="f66e8-216">95</span><span class="sxs-lookup"><span data-stu-id="f66e8-216">95</span></span>

<span data-ttu-id="f66e8-217">Impossibile notificare il servizio.</span><span class="sxs-lookup"><span data-stu-id="f66e8-217">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="f66e8-218">**Non è possibile inviare una notifica al servizio DNS**</span><span class="sxs-lookup"><span data-stu-id="f66e8-218">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="f66e8-219">96</span><span class="sxs-lookup"><span data-stu-id="f66e8-219">96</span></span>

<span data-ttu-id="f66e8-220">Impossibile inviare una notifica al servizio DNS.</span><span class="sxs-lookup"><span data-stu-id="f66e8-220">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="f66e8-221">**Interfaccia non configurabile**</span><span class="sxs-lookup"><span data-stu-id="f66e8-221">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="f66e8-222">97</span><span class="sxs-lookup"><span data-stu-id="f66e8-222">97</span></span>

<span data-ttu-id="f66e8-223">Interfaccia non configurabile.</span><span class="sxs-lookup"><span data-stu-id="f66e8-223">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="f66e8-224">**Non tutti i lease DHCP possono essere rilasciati/rinnovati**</span><span class="sxs-lookup"><span data-stu-id="f66e8-224">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="f66e8-225">98</span><span class="sxs-lookup"><span data-stu-id="f66e8-225">98</span></span>

<span data-ttu-id="f66e8-226">Non tutti i lease DHCP possono essere rilasciati o rinnovati.</span><span class="sxs-lookup"><span data-stu-id="f66e8-226">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="f66e8-227">**DHCP non abilitato sull'adapter**</span><span class="sxs-lookup"><span data-stu-id="f66e8-227">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="f66e8-228">100</span><span class="sxs-lookup"><span data-stu-id="f66e8-228">100</span></span>

<span data-ttu-id="f66e8-229">DHCP non abilitato sulla scheda.</span><span class="sxs-lookup"><span data-stu-id="f66e8-229">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="f66e8-230">**Altri**</span><span class="sxs-lookup"><span data-stu-id="f66e8-230">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="f66e8-231">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="f66e8-231">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f66e8-232">Commenti</span><span class="sxs-lookup"><span data-stu-id="f66e8-232">Remarks</span></span>

<span data-ttu-id="f66e8-233">RFC 1122 e BSD interpretano il puntatore urgente nell'intestazione TCP e la lunghezza dei dati urgenti in modo diverso.</span><span class="sxs-lookup"><span data-stu-id="f66e8-233">RFC 1122 and BSD interpret the urgent pointer in the TCP header and the length of the urgent data differently.</span></span> <span data-ttu-id="f66e8-234">Non sono interoperativi.</span><span class="sxs-lookup"><span data-stu-id="f66e8-234">They are not interoperable.</span></span> <span data-ttu-id="f66e8-235">Il valore predefinito è la modalità BSD.</span><span class="sxs-lookup"><span data-stu-id="f66e8-235">The default is BSD mode.</span></span>

## <a name="examples"></a><span data-ttu-id="f66e8-236">Esempio</span><span class="sxs-lookup"><span data-stu-id="f66e8-236">Examples</span></span>

<span data-ttu-id="f66e8-237">L'esempio [modifica utilizzo puntatore urgente per tutte le schede di rete](https://Gallery.TechNet.Microsoft.Com/0ff22a90-0be6-4914-8db7-aaf72cbea9cb) di VBScript configura un computer per l'utilizzo della specifica RFC 1122 per i dati urgenti.</span><span class="sxs-lookup"><span data-stu-id="f66e8-237">The [Modify Urgent Pointer Use for All Network Adapters](https://Gallery.TechNet.Microsoft.Com/0ff22a90-0be6-4914-8db7-aaf72cbea9cb) VBScript sample configures a computer to use the RFC 1122 specification for urgent data.</span></span>

## <a name="requirements"></a><span data-ttu-id="f66e8-238">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f66e8-238">Requirements</span></span>



| <span data-ttu-id="f66e8-239">Requisito</span><span class="sxs-lookup"><span data-stu-id="f66e8-239">Requirement</span></span> | <span data-ttu-id="f66e8-240">Valore</span><span class="sxs-lookup"><span data-stu-id="f66e8-240">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f66e8-241">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f66e8-241">Minimum supported client</span></span><br/> | <span data-ttu-id="f66e8-242">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f66e8-242">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f66e8-243">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f66e8-243">Minimum supported server</span></span><br/> | <span data-ttu-id="f66e8-244">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f66e8-244">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f66e8-245">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f66e8-245">Namespace</span></span><br/>                | <span data-ttu-id="f66e8-246">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="f66e8-246">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f66e8-247">MOF</span><span class="sxs-lookup"><span data-stu-id="f66e8-247">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f66e8-248"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f66e8-248"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f66e8-249">DLL</span><span class="sxs-lookup"><span data-stu-id="f66e8-249">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f66e8-250"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f66e8-250"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f66e8-251">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f66e8-251">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f66e8-252">Classi hardware del sistema del computer</span><span class="sxs-lookup"><span data-stu-id="f66e8-252">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="f66e8-253">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="f66e8-253">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="f66e8-254">Attività WMI: rete</span><span class="sxs-lookup"><span data-stu-id="f66e8-254">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="f66e8-255">Attività WMI: account e domini</span><span class="sxs-lookup"><span data-stu-id="f66e8-255">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="f66e8-256">Supporto di IPv6 e IPv4 in WMI</span><span class="sxs-lookup"><span data-stu-id="f66e8-256">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

