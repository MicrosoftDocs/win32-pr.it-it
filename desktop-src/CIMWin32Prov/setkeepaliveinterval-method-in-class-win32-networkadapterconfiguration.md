---
description: Il metodo statico della classe WMI SetKeepAliveInterval viene usato per impostare l'intervallo che separa le ritrasmissioni keep-alive fino a quando non viene ricevuta una risposta.
ms.assetid: 83415000-124a-44a7-93cc-92ce9df143aa
ms.tgt_platform: multiple
title: Metodo SetKeepAliveInterval della classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetKeepAliveInterval
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2ce6a1491fd9e414f503d0165216794c67db0e97
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127059"
---
# <a name="setkeepaliveinterval-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="b1531-103">Metodo SetKeepAliveInterval della \_ classe NetworkAdapterConfiguration Win32</span><span class="sxs-lookup"><span data-stu-id="b1531-103">SetKeepAliveInterval method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="b1531-104">Il metodo statico della [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetKeepAliveInterval** viene usato per impostare l'intervallo che separa le ritrasmissioni keep-alive fino a quando non viene ricevuta una risposta.</span><span class="sxs-lookup"><span data-stu-id="b1531-104">The **SetKeepAliveInterval** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to set the interval separating Keep Alive Retransmissions until a response is received.</span></span>

<span data-ttu-id="b1531-105">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="b1531-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="b1531-106">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="b1531-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="b1531-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b1531-107">Syntax</span></span>


```mof
uint32 SetKeepAliveInterval(
  [in] uint32 KeepAliveInterval
);
```



## <a name="parameters"></a><span data-ttu-id="b1531-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="b1531-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1531-109">*KeepAliveInterval* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b1531-109">*KeepAliveInterval* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1531-110">Valore, in millisecondi, per l'intervallo che separa le ritrasmissioni keep-alive fino a quando non viene ricevuta una risposta.</span><span class="sxs-lookup"><span data-stu-id="b1531-110">Value, in milliseconds, for the interval separating Keep Alive Retransmissions until a response is received.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b1531-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b1531-111">Return value</span></span>

<span data-ttu-id="b1531-112">Restituisce un valore pari a 0 (zero) per un completamento corretto quando non è richiesto il riavvio, 1 (uno) per un completamento corretto quando è necessario un riavvio e un numero diverso se si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="b1531-112">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="b1531-113">Per ulteriori informazioni sui codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="b1531-113">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="b1531-114">Per i valori **HRESULT** generali, vedere [codici di errore di sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="b1531-114">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="b1531-115">**Operazione completata, non è necessario riavviare il computer**</span><span class="sxs-lookup"><span data-stu-id="b1531-115">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="b1531-116">0</span><span class="sxs-lookup"><span data-stu-id="b1531-116">0</span></span>

<span data-ttu-id="b1531-117">Operazione completata, non è necessario riavviare il computer.</span><span class="sxs-lookup"><span data-stu-id="b1531-117">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="b1531-118">**Operazione completata, riavvio richiesto**</span><span class="sxs-lookup"><span data-stu-id="b1531-118">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="b1531-119">1</span><span class="sxs-lookup"><span data-stu-id="b1531-119">1</span></span>

<span data-ttu-id="b1531-120">Operazione completata, è necessario riavviare il computer.</span><span class="sxs-lookup"><span data-stu-id="b1531-120">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="b1531-121">**Metodo non supportato in questa piattaforma**</span><span class="sxs-lookup"><span data-stu-id="b1531-121">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="b1531-122">64</span><span class="sxs-lookup"><span data-stu-id="b1531-122">64</span></span>

<span data-ttu-id="b1531-123">Metodo non supportato in questa piattaforma.</span><span class="sxs-lookup"><span data-stu-id="b1531-123">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="b1531-124">**Errore sconosciuto**</span><span class="sxs-lookup"><span data-stu-id="b1531-124">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="b1531-125">65</span><span class="sxs-lookup"><span data-stu-id="b1531-125">65</span></span>

<span data-ttu-id="b1531-126">Errore sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="b1531-126">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="b1531-127">**subnet mask non valido**</span><span class="sxs-lookup"><span data-stu-id="b1531-127">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="b1531-128">66</span><span class="sxs-lookup"><span data-stu-id="b1531-128">66</span></span>

<span data-ttu-id="b1531-129">Subnet mask non valido.</span><span class="sxs-lookup"><span data-stu-id="b1531-129">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="b1531-130">**Si è verificato un errore durante l'elaborazione di un'istanza restituita**</span><span class="sxs-lookup"><span data-stu-id="b1531-130">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="b1531-131">67</span><span class="sxs-lookup"><span data-stu-id="b1531-131">67</span></span>

<span data-ttu-id="b1531-132">Si è verificato un errore durante l'elaborazione di un'istanza di restituita.</span><span class="sxs-lookup"><span data-stu-id="b1531-132">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="b1531-133">**Parametro di input non valido**</span><span class="sxs-lookup"><span data-stu-id="b1531-133">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="b1531-134">68</span><span class="sxs-lookup"><span data-stu-id="b1531-134">68</span></span>

<span data-ttu-id="b1531-135">Parametro di input non valido.</span><span class="sxs-lookup"><span data-stu-id="b1531-135">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="b1531-136">**Sono stati specificati più di 5 gateway**</span><span class="sxs-lookup"><span data-stu-id="b1531-136">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="b1531-137">69</span><span class="sxs-lookup"><span data-stu-id="b1531-137">69</span></span>

<span data-ttu-id="b1531-138">Sono stati specificati più di cinque gateway.</span><span class="sxs-lookup"><span data-stu-id="b1531-138">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="b1531-139">**Indirizzo IP non valido**</span><span class="sxs-lookup"><span data-stu-id="b1531-139">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="b1531-140">70</span><span class="sxs-lookup"><span data-stu-id="b1531-140">70</span></span>

<span data-ttu-id="b1531-141">Indirizzo IP non valido.</span><span class="sxs-lookup"><span data-stu-id="b1531-141">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="b1531-142">**Indirizzo IP gateway non valido**</span><span class="sxs-lookup"><span data-stu-id="b1531-142">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="b1531-143">71</span><span class="sxs-lookup"><span data-stu-id="b1531-143">71</span></span>

<span data-ttu-id="b1531-144">Indirizzo IP del gateway non valido.</span><span class="sxs-lookup"><span data-stu-id="b1531-144">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="b1531-145">**Si è verificato un errore durante l'accesso al registro di sistema per le informazioni richieste**</span><span class="sxs-lookup"><span data-stu-id="b1531-145">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="b1531-146">72</span><span class="sxs-lookup"><span data-stu-id="b1531-146">72</span></span>

<span data-ttu-id="b1531-147">Si è verificato un errore durante l'accesso al registro di sistema per le informazioni richieste.</span><span class="sxs-lookup"><span data-stu-id="b1531-147">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="b1531-148">**Nome di dominio non valido**</span><span class="sxs-lookup"><span data-stu-id="b1531-148">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="b1531-149">73</span><span class="sxs-lookup"><span data-stu-id="b1531-149">73</span></span>

<span data-ttu-id="b1531-150">Nome di dominio non valido.</span><span class="sxs-lookup"><span data-stu-id="b1531-150">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="b1531-151">**Nome host non valido**</span><span class="sxs-lookup"><span data-stu-id="b1531-151">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="b1531-152">74</span><span class="sxs-lookup"><span data-stu-id="b1531-152">74</span></span>

<span data-ttu-id="b1531-153">Nome host non valido.</span><span class="sxs-lookup"><span data-stu-id="b1531-153">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="b1531-154">**Nessun server WINS primario/secondario definito**</span><span class="sxs-lookup"><span data-stu-id="b1531-154">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="b1531-155">75</span><span class="sxs-lookup"><span data-stu-id="b1531-155">75</span></span>

<span data-ttu-id="b1531-156">Nessun server WINS primario o secondario definito.</span><span class="sxs-lookup"><span data-stu-id="b1531-156">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="b1531-157">**File non valido**</span><span class="sxs-lookup"><span data-stu-id="b1531-157">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="b1531-158">76</span><span class="sxs-lookup"><span data-stu-id="b1531-158">76</span></span>

<span data-ttu-id="b1531-159">File non valido.</span><span class="sxs-lookup"><span data-stu-id="b1531-159">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="b1531-160">**Percorso di sistema non valido**</span><span class="sxs-lookup"><span data-stu-id="b1531-160">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="b1531-161">77</span><span class="sxs-lookup"><span data-stu-id="b1531-161">77</span></span>

<span data-ttu-id="b1531-162">Percorso di sistema non valido.</span><span class="sxs-lookup"><span data-stu-id="b1531-162">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="b1531-163">**Copia del file non riuscita**</span><span class="sxs-lookup"><span data-stu-id="b1531-163">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="b1531-164">78</span><span class="sxs-lookup"><span data-stu-id="b1531-164">78</span></span>

<span data-ttu-id="b1531-165">Copia del file non riuscita.</span><span class="sxs-lookup"><span data-stu-id="b1531-165">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="b1531-166">**Parametro di sicurezza non valido**</span><span class="sxs-lookup"><span data-stu-id="b1531-166">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="b1531-167">79</span><span class="sxs-lookup"><span data-stu-id="b1531-167">79</span></span>

<span data-ttu-id="b1531-168">Parametro di sicurezza non valido.</span><span class="sxs-lookup"><span data-stu-id="b1531-168">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="b1531-169">**Impossibile configurare il servizio TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="b1531-169">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="b1531-170">80</span><span class="sxs-lookup"><span data-stu-id="b1531-170">80</span></span>

<span data-ttu-id="b1531-171">Impossibile configurare il servizio TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="b1531-171">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="b1531-172">**Non è possibile configurare il servizio DHCP**</span><span class="sxs-lookup"><span data-stu-id="b1531-172">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="b1531-173">81</span><span class="sxs-lookup"><span data-stu-id="b1531-173">81</span></span>

<span data-ttu-id="b1531-174">Impossibile configurare il servizio DHCP.</span><span class="sxs-lookup"><span data-stu-id="b1531-174">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="b1531-175">**Non è possibile rinnovare il lease DHCP**</span><span class="sxs-lookup"><span data-stu-id="b1531-175">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="b1531-176">82</span><span class="sxs-lookup"><span data-stu-id="b1531-176">82</span></span>

<span data-ttu-id="b1531-177">Non è possibile rinnovare il lease DHCP.</span><span class="sxs-lookup"><span data-stu-id="b1531-177">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="b1531-178">**Non è possibile rilasciare il lease DHCP**</span><span class="sxs-lookup"><span data-stu-id="b1531-178">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="b1531-179">83</span><span class="sxs-lookup"><span data-stu-id="b1531-179">83</span></span>

<span data-ttu-id="b1531-180">Impossibile rilasciare il lease DHCP.</span><span class="sxs-lookup"><span data-stu-id="b1531-180">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="b1531-181">**IP non abilitato sulla scheda**</span><span class="sxs-lookup"><span data-stu-id="b1531-181">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="b1531-182">84</span><span class="sxs-lookup"><span data-stu-id="b1531-182">84</span></span>

<span data-ttu-id="b1531-183">IP non abilitato sulla scheda.</span><span class="sxs-lookup"><span data-stu-id="b1531-183">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="b1531-184">**IPX non abilitato sull'adapter**</span><span class="sxs-lookup"><span data-stu-id="b1531-184">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="b1531-185">85</span><span class="sxs-lookup"><span data-stu-id="b1531-185">85</span></span>

<span data-ttu-id="b1531-186">IPX non abilitato sulla scheda.</span><span class="sxs-lookup"><span data-stu-id="b1531-186">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="b1531-187">**Errore limite numero frame/rete**</span><span class="sxs-lookup"><span data-stu-id="b1531-187">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="b1531-188">86</span><span class="sxs-lookup"><span data-stu-id="b1531-188">86</span></span>

<span data-ttu-id="b1531-189">Errore dei limiti del numero di rete o del frame.</span><span class="sxs-lookup"><span data-stu-id="b1531-189">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="b1531-190">**Tipo di frame non valido**</span><span class="sxs-lookup"><span data-stu-id="b1531-190">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="b1531-191">87</span><span class="sxs-lookup"><span data-stu-id="b1531-191">87</span></span>

<span data-ttu-id="b1531-192">Tipo di frame non valido.</span><span class="sxs-lookup"><span data-stu-id="b1531-192">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="b1531-193">**Numero di rete non valido**</span><span class="sxs-lookup"><span data-stu-id="b1531-193">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="b1531-194">88</span><span class="sxs-lookup"><span data-stu-id="b1531-194">88</span></span>

<span data-ttu-id="b1531-195">Numero di rete non valido.</span><span class="sxs-lookup"><span data-stu-id="b1531-195">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="b1531-196">**Numero di rete duplicato**</span><span class="sxs-lookup"><span data-stu-id="b1531-196">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="b1531-197">89</span><span class="sxs-lookup"><span data-stu-id="b1531-197">89</span></span>

<span data-ttu-id="b1531-198">Numero di rete duplicato.</span><span class="sxs-lookup"><span data-stu-id="b1531-198">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="b1531-199">**Parametro fuori limite**</span><span class="sxs-lookup"><span data-stu-id="b1531-199">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="b1531-200">90</span><span class="sxs-lookup"><span data-stu-id="b1531-200">90</span></span>

<span data-ttu-id="b1531-201">Parametro fuori limite.</span><span class="sxs-lookup"><span data-stu-id="b1531-201">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="b1531-202">**Accesso negato**</span><span class="sxs-lookup"><span data-stu-id="b1531-202">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="b1531-203">91</span><span class="sxs-lookup"><span data-stu-id="b1531-203">91</span></span>

<span data-ttu-id="b1531-204">Accesso negato.</span><span class="sxs-lookup"><span data-stu-id="b1531-204">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="b1531-205">**Memoria insufficiente**</span><span class="sxs-lookup"><span data-stu-id="b1531-205">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="b1531-206">92</span><span class="sxs-lookup"><span data-stu-id="b1531-206">92</span></span>

<span data-ttu-id="b1531-207">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="b1531-207">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="b1531-208">**Esiste già**</span><span class="sxs-lookup"><span data-stu-id="b1531-208">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="b1531-209">93</span><span class="sxs-lookup"><span data-stu-id="b1531-209">93</span></span>

<span data-ttu-id="b1531-210">Esiste già.</span><span class="sxs-lookup"><span data-stu-id="b1531-210">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="b1531-211">**Percorso, file o oggetto non trovato**</span><span class="sxs-lookup"><span data-stu-id="b1531-211">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="b1531-212">94</span><span class="sxs-lookup"><span data-stu-id="b1531-212">94</span></span>

<span data-ttu-id="b1531-213">Il percorso, il file o l'oggetto non è stato trovato.</span><span class="sxs-lookup"><span data-stu-id="b1531-213">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="b1531-214">**Non è possibile inviare una notifica al servizio**</span><span class="sxs-lookup"><span data-stu-id="b1531-214">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="b1531-215">95</span><span class="sxs-lookup"><span data-stu-id="b1531-215">95</span></span>

<span data-ttu-id="b1531-216">Impossibile notificare il servizio.</span><span class="sxs-lookup"><span data-stu-id="b1531-216">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="b1531-217">**Non è possibile inviare una notifica al servizio DNS**</span><span class="sxs-lookup"><span data-stu-id="b1531-217">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="b1531-218">96</span><span class="sxs-lookup"><span data-stu-id="b1531-218">96</span></span>

<span data-ttu-id="b1531-219">Impossibile inviare una notifica al servizio DNS.</span><span class="sxs-lookup"><span data-stu-id="b1531-219">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="b1531-220">**Interfaccia non configurabile**</span><span class="sxs-lookup"><span data-stu-id="b1531-220">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="b1531-221">97</span><span class="sxs-lookup"><span data-stu-id="b1531-221">97</span></span>

<span data-ttu-id="b1531-222">Interfaccia non configurabile.</span><span class="sxs-lookup"><span data-stu-id="b1531-222">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="b1531-223">**Non tutti i lease DHCP possono essere rilasciati/rinnovati**</span><span class="sxs-lookup"><span data-stu-id="b1531-223">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="b1531-224">98</span><span class="sxs-lookup"><span data-stu-id="b1531-224">98</span></span>

<span data-ttu-id="b1531-225">Non tutti i lease DHCP possono essere rilasciati o rinnovati.</span><span class="sxs-lookup"><span data-stu-id="b1531-225">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="b1531-226">**DHCP non abilitato sull'adapter**</span><span class="sxs-lookup"><span data-stu-id="b1531-226">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="b1531-227">100</span><span class="sxs-lookup"><span data-stu-id="b1531-227">100</span></span>

<span data-ttu-id="b1531-228">DHCP non abilitato sulla scheda.</span><span class="sxs-lookup"><span data-stu-id="b1531-228">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="b1531-229">**Altri**</span><span class="sxs-lookup"><span data-stu-id="b1531-229">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="b1531-230">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="b1531-230">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b1531-231">Commenti</span><span class="sxs-lookup"><span data-stu-id="b1531-231">Remarks</span></span>

<span data-ttu-id="b1531-232">Dopo la ricezione di una risposta, il ritardo fino alla successiva trasmissione Keep-Alive viene nuovamente controllato dal valore della proprietà [**KeepAliveTime**](win32-networkadapterconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="b1531-232">After a response is received, the delay until the next Keep Alive Transmission is again controlled by the value of the [**KeepAliveTime**](win32-networkadapterconfiguration.md) property.</span></span> <span data-ttu-id="b1531-233">La connessione viene terminata dopo che il numero di ritrasmissioni specificato dalla proprietà **TcpMaxDataRetransmissions** è andato senza risposta</span><span class="sxs-lookup"><span data-stu-id="b1531-233">The connection is terminated after the number of retransmissions specified by the **TcpMaxDataRetransmissions** property have gone unanswered</span></span>

## <a name="examples"></a><span data-ttu-id="b1531-234">Esempio</span><span class="sxs-lookup"><span data-stu-id="b1531-234">Examples</span></span>

<span data-ttu-id="b1531-235">L'esempio di [modifica dell'intervallo keep-alive per tutte le schede di rete](https://Gallery.TechNet.Microsoft.Com/f6d4a0e7-5b59-42e3-888d-82a028e2bf35) VBScript configura l'intervallo keep-alive per tutte le schede di rete in un computer a 300, 00 millisecondi (5 minuti).</span><span class="sxs-lookup"><span data-stu-id="b1531-235">The [Modify the Keep Alive Interval for all Network Adapters](https://Gallery.TechNet.Microsoft.Com/f6d4a0e7-5b59-42e3-888d-82a028e2bf35) VBScript sample configures the keep alive interval for all network adapters on a computer to 300,00 milliseconds (5 minutes).</span></span>

## <a name="requirements"></a><span data-ttu-id="b1531-236">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b1531-236">Requirements</span></span>



| <span data-ttu-id="b1531-237">Requisito</span><span class="sxs-lookup"><span data-stu-id="b1531-237">Requirement</span></span> | <span data-ttu-id="b1531-238">Valore</span><span class="sxs-lookup"><span data-stu-id="b1531-238">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b1531-239">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b1531-239">Minimum supported client</span></span><br/> | <span data-ttu-id="b1531-240">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b1531-240">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b1531-241">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b1531-241">Minimum supported server</span></span><br/> | <span data-ttu-id="b1531-242">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b1531-242">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b1531-243">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b1531-243">Namespace</span></span><br/>                | <span data-ttu-id="b1531-244">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="b1531-244">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b1531-245">MOF</span><span class="sxs-lookup"><span data-stu-id="b1531-245">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b1531-246"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b1531-246"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b1531-247">DLL</span><span class="sxs-lookup"><span data-stu-id="b1531-247">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b1531-248"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b1531-248"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b1531-249">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b1531-249">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1531-250">Classi hardware del sistema del computer</span><span class="sxs-lookup"><span data-stu-id="b1531-250">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="b1531-251">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="b1531-251">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="b1531-252">Attività WMI: rete</span><span class="sxs-lookup"><span data-stu-id="b1531-252">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="b1531-253">Attività WMI: account e domini</span><span class="sxs-lookup"><span data-stu-id="b1531-253">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="b1531-254">Supporto di IPv6 e IPv4 in WMI</span><span class="sxs-lookup"><span data-stu-id="b1531-254">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

