---
description: Questo metodo è obsoleto. Le applicazioni devono usare l'API di qualità del servizio (QoS) per modificare i bit dei servizi (TOS).
ms.assetid: 18860c13-7324-4a37-b83c-f3d15c425acb
ms.tgt_platform: multiple
title: Metodo SetDefaultTOS della classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetDefaultTOS
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5df55ff88c87047a48a84a122c8e58c8148a7cff
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305179"
---
# <a name="setdefaulttos-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="db94a-104">Metodo SetDefaultTOS della \_ classe NetworkAdapterConfiguration Win32</span><span class="sxs-lookup"><span data-stu-id="db94a-104">SetDefaultTOS method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="db94a-105">Questo metodo è obsoleto.</span><span class="sxs-lookup"><span data-stu-id="db94a-105">This method is obsolete.</span></span> <span data-ttu-id="db94a-106">Le applicazioni devono usare l'API di qualità del servizio (QoS) per modificare i bit dei servizi (TOS).</span><span class="sxs-lookup"><span data-stu-id="db94a-106">Applications should use the Quality of Service (QoS) API to manipulate Type of Service (TOS) bits.</span></span> <span data-ttu-id="db94a-107">Per ulteriori informazioni, vedere la pagina relativa alla [qualità del servizio](/previous-versions/windows/desktop/qos/qos-start-page).</span><span class="sxs-lookup"><span data-stu-id="db94a-107">For more information, see [Quality of Service](/previous-versions/windows/desktop/qos/qos-start-page).</span></span>

<span data-ttu-id="db94a-108">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="db94a-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="db94a-109">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="db94a-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="db94a-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="db94a-110">Syntax</span></span>


```mof
uint32 SetDefaultTOS(
  [in] uint8 DefaultTOS
);
```



## <a name="parameters"></a><span data-ttu-id="db94a-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="db94a-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db94a-112">*DefaultTOS* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="db94a-112">*DefaultTOS* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db94a-113">Valore del tipo di servizio (TOS) inserito nell'intestazione dei pacchetti IP in uscita.</span><span class="sxs-lookup"><span data-stu-id="db94a-113">Type of Service (TOS) value put in the header of outgoing IP packets.</span></span> <span data-ttu-id="db94a-114">Per una definizione dei valori, vedere RFC 791.</span><span class="sxs-lookup"><span data-stu-id="db94a-114">For a definition of the values, see RFC 791.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db94a-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="db94a-115">Return value</span></span>

<span data-ttu-id="db94a-116">Restituisce un valore pari a 0 (zero) per un completamento corretto quando non è richiesto il riavvio, 1 (uno) per un completamento corretto quando è necessario un riavvio e un numero diverso se si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="db94a-116">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="db94a-117">Per ulteriori informazioni sui codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="db94a-117">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="db94a-118">Per i valori **HRESULT** generali, vedere [codici di errore di sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="db94a-118">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="db94a-119">**Operazione completata, non è necessario riavviare il computer**</span><span class="sxs-lookup"><span data-stu-id="db94a-119">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="db94a-120">0</span><span class="sxs-lookup"><span data-stu-id="db94a-120">0</span></span>

<span data-ttu-id="db94a-121">Operazione completata, non è necessario riavviare il computer.</span><span class="sxs-lookup"><span data-stu-id="db94a-121">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="db94a-122">**Operazione completata, riavvio richiesto**</span><span class="sxs-lookup"><span data-stu-id="db94a-122">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="db94a-123">1</span><span class="sxs-lookup"><span data-stu-id="db94a-123">1</span></span>

<span data-ttu-id="db94a-124">Operazione completata, è necessario riavviare il computer.</span><span class="sxs-lookup"><span data-stu-id="db94a-124">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="db94a-125">**Metodo non supportato in questa piattaforma**</span><span class="sxs-lookup"><span data-stu-id="db94a-125">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="db94a-126">64</span><span class="sxs-lookup"><span data-stu-id="db94a-126">64</span></span>

<span data-ttu-id="db94a-127">Metodo non supportato in questa piattaforma.</span><span class="sxs-lookup"><span data-stu-id="db94a-127">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="db94a-128">**Errore sconosciuto**</span><span class="sxs-lookup"><span data-stu-id="db94a-128">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="db94a-129">65</span><span class="sxs-lookup"><span data-stu-id="db94a-129">65</span></span>

<span data-ttu-id="db94a-130">Errore sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="db94a-130">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="db94a-131">**subnet mask non valido**</span><span class="sxs-lookup"><span data-stu-id="db94a-131">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="db94a-132">66</span><span class="sxs-lookup"><span data-stu-id="db94a-132">66</span></span>

<span data-ttu-id="db94a-133">Subnet mask non valido.</span><span class="sxs-lookup"><span data-stu-id="db94a-133">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="db94a-134">**Si è verificato un errore durante l'elaborazione di un'istanza restituita**</span><span class="sxs-lookup"><span data-stu-id="db94a-134">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="db94a-135">67</span><span class="sxs-lookup"><span data-stu-id="db94a-135">67</span></span>

<span data-ttu-id="db94a-136">Si è verificato un errore durante l'elaborazione di un'istanza di restituita.</span><span class="sxs-lookup"><span data-stu-id="db94a-136">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="db94a-137">**Parametro di input non valido**</span><span class="sxs-lookup"><span data-stu-id="db94a-137">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="db94a-138">68</span><span class="sxs-lookup"><span data-stu-id="db94a-138">68</span></span>

<span data-ttu-id="db94a-139">Parametro di input non valido.</span><span class="sxs-lookup"><span data-stu-id="db94a-139">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="db94a-140">**Sono stati specificati più di 5 gateway**</span><span class="sxs-lookup"><span data-stu-id="db94a-140">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="db94a-141">69</span><span class="sxs-lookup"><span data-stu-id="db94a-141">69</span></span>

<span data-ttu-id="db94a-142">Sono stati specificati più di cinque gateway.</span><span class="sxs-lookup"><span data-stu-id="db94a-142">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="db94a-143">**Indirizzo IP non valido**</span><span class="sxs-lookup"><span data-stu-id="db94a-143">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="db94a-144">70</span><span class="sxs-lookup"><span data-stu-id="db94a-144">70</span></span>

<span data-ttu-id="db94a-145">Indirizzo IP non valido.</span><span class="sxs-lookup"><span data-stu-id="db94a-145">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="db94a-146">**Indirizzo IP gateway non valido**</span><span class="sxs-lookup"><span data-stu-id="db94a-146">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="db94a-147">71</span><span class="sxs-lookup"><span data-stu-id="db94a-147">71</span></span>

<span data-ttu-id="db94a-148">Indirizzo IP del gateway non valido.</span><span class="sxs-lookup"><span data-stu-id="db94a-148">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="db94a-149">**Si è verificato un errore durante l'accesso al registro di sistema per le informazioni richieste**</span><span class="sxs-lookup"><span data-stu-id="db94a-149">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="db94a-150">72</span><span class="sxs-lookup"><span data-stu-id="db94a-150">72</span></span>

<span data-ttu-id="db94a-151">Si è verificato un errore durante l'accesso al registro di sistema per le informazioni richieste.</span><span class="sxs-lookup"><span data-stu-id="db94a-151">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="db94a-152">**Nome di dominio non valido**</span><span class="sxs-lookup"><span data-stu-id="db94a-152">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="db94a-153">73</span><span class="sxs-lookup"><span data-stu-id="db94a-153">73</span></span>

<span data-ttu-id="db94a-154">Nome di dominio non valido.</span><span class="sxs-lookup"><span data-stu-id="db94a-154">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="db94a-155">**Nome host non valido**</span><span class="sxs-lookup"><span data-stu-id="db94a-155">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="db94a-156">74</span><span class="sxs-lookup"><span data-stu-id="db94a-156">74</span></span>

<span data-ttu-id="db94a-157">Nome host non valido.</span><span class="sxs-lookup"><span data-stu-id="db94a-157">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="db94a-158">**Nessun server WINS primario/secondario definito**</span><span class="sxs-lookup"><span data-stu-id="db94a-158">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="db94a-159">75</span><span class="sxs-lookup"><span data-stu-id="db94a-159">75</span></span>

<span data-ttu-id="db94a-160">Nessun server WINS primario o secondario definito.</span><span class="sxs-lookup"><span data-stu-id="db94a-160">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="db94a-161">**File non valido**</span><span class="sxs-lookup"><span data-stu-id="db94a-161">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="db94a-162">76</span><span class="sxs-lookup"><span data-stu-id="db94a-162">76</span></span>

<span data-ttu-id="db94a-163">File non valido.</span><span class="sxs-lookup"><span data-stu-id="db94a-163">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="db94a-164">**Percorso di sistema non valido**</span><span class="sxs-lookup"><span data-stu-id="db94a-164">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="db94a-165">77</span><span class="sxs-lookup"><span data-stu-id="db94a-165">77</span></span>

<span data-ttu-id="db94a-166">Percorso di sistema non valido.</span><span class="sxs-lookup"><span data-stu-id="db94a-166">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="db94a-167">**Copia del file non riuscita**</span><span class="sxs-lookup"><span data-stu-id="db94a-167">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="db94a-168">78</span><span class="sxs-lookup"><span data-stu-id="db94a-168">78</span></span>

<span data-ttu-id="db94a-169">Copia del file non riuscita.</span><span class="sxs-lookup"><span data-stu-id="db94a-169">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="db94a-170">**Parametro di sicurezza non valido**</span><span class="sxs-lookup"><span data-stu-id="db94a-170">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="db94a-171">79</span><span class="sxs-lookup"><span data-stu-id="db94a-171">79</span></span>

<span data-ttu-id="db94a-172">Parametro di sicurezza non valido.</span><span class="sxs-lookup"><span data-stu-id="db94a-172">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="db94a-173">**Impossibile configurare il servizio TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="db94a-173">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="db94a-174">80</span><span class="sxs-lookup"><span data-stu-id="db94a-174">80</span></span>

<span data-ttu-id="db94a-175">Impossibile configurare il servizio TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="db94a-175">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="db94a-176">**Non è possibile configurare il servizio DHCP**</span><span class="sxs-lookup"><span data-stu-id="db94a-176">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="db94a-177">81</span><span class="sxs-lookup"><span data-stu-id="db94a-177">81</span></span>

<span data-ttu-id="db94a-178">Impossibile configurare il servizio DHCP.</span><span class="sxs-lookup"><span data-stu-id="db94a-178">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="db94a-179">**Non è possibile rinnovare il lease DHCP**</span><span class="sxs-lookup"><span data-stu-id="db94a-179">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="db94a-180">82</span><span class="sxs-lookup"><span data-stu-id="db94a-180">82</span></span>

<span data-ttu-id="db94a-181">Non è possibile rinnovare il lease DHCP.</span><span class="sxs-lookup"><span data-stu-id="db94a-181">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="db94a-182">**Non è possibile rilasciare il lease DHCP**</span><span class="sxs-lookup"><span data-stu-id="db94a-182">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="db94a-183">83</span><span class="sxs-lookup"><span data-stu-id="db94a-183">83</span></span>

<span data-ttu-id="db94a-184">Impossibile rilasciare il lease DHCP.</span><span class="sxs-lookup"><span data-stu-id="db94a-184">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="db94a-185">**IP non abilitato sulla scheda**</span><span class="sxs-lookup"><span data-stu-id="db94a-185">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="db94a-186">84</span><span class="sxs-lookup"><span data-stu-id="db94a-186">84</span></span>

<span data-ttu-id="db94a-187">IP non abilitato sulla scheda.</span><span class="sxs-lookup"><span data-stu-id="db94a-187">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="db94a-188">**IPX non abilitato sull'adapter**</span><span class="sxs-lookup"><span data-stu-id="db94a-188">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="db94a-189">85</span><span class="sxs-lookup"><span data-stu-id="db94a-189">85</span></span>

<span data-ttu-id="db94a-190">IPX non abilitato sulla scheda.</span><span class="sxs-lookup"><span data-stu-id="db94a-190">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="db94a-191">**Errore limite numero frame/rete**</span><span class="sxs-lookup"><span data-stu-id="db94a-191">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="db94a-192">86</span><span class="sxs-lookup"><span data-stu-id="db94a-192">86</span></span>

<span data-ttu-id="db94a-193">Errore dei limiti del numero di rete o del frame.</span><span class="sxs-lookup"><span data-stu-id="db94a-193">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="db94a-194">**Tipo di frame non valido**</span><span class="sxs-lookup"><span data-stu-id="db94a-194">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="db94a-195">87</span><span class="sxs-lookup"><span data-stu-id="db94a-195">87</span></span>

<span data-ttu-id="db94a-196">Tipo di frame non valido.</span><span class="sxs-lookup"><span data-stu-id="db94a-196">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="db94a-197">**Numero di rete non valido**</span><span class="sxs-lookup"><span data-stu-id="db94a-197">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="db94a-198">88</span><span class="sxs-lookup"><span data-stu-id="db94a-198">88</span></span>

<span data-ttu-id="db94a-199">Numero di rete non valido.</span><span class="sxs-lookup"><span data-stu-id="db94a-199">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="db94a-200">**Numero di rete duplicato**</span><span class="sxs-lookup"><span data-stu-id="db94a-200">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="db94a-201">89</span><span class="sxs-lookup"><span data-stu-id="db94a-201">89</span></span>

<span data-ttu-id="db94a-202">Numero di rete duplicato.</span><span class="sxs-lookup"><span data-stu-id="db94a-202">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="db94a-203">**Parametro fuori limite**</span><span class="sxs-lookup"><span data-stu-id="db94a-203">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="db94a-204">90</span><span class="sxs-lookup"><span data-stu-id="db94a-204">90</span></span>

<span data-ttu-id="db94a-205">Parametro fuori limite.</span><span class="sxs-lookup"><span data-stu-id="db94a-205">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="db94a-206">**Accesso negato**</span><span class="sxs-lookup"><span data-stu-id="db94a-206">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="db94a-207">91</span><span class="sxs-lookup"><span data-stu-id="db94a-207">91</span></span>

<span data-ttu-id="db94a-208">Accesso negato.</span><span class="sxs-lookup"><span data-stu-id="db94a-208">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="db94a-209">**Memoria insufficiente**</span><span class="sxs-lookup"><span data-stu-id="db94a-209">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="db94a-210">92</span><span class="sxs-lookup"><span data-stu-id="db94a-210">92</span></span>

<span data-ttu-id="db94a-211">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="db94a-211">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="db94a-212">**Esiste già**</span><span class="sxs-lookup"><span data-stu-id="db94a-212">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="db94a-213">93</span><span class="sxs-lookup"><span data-stu-id="db94a-213">93</span></span>

<span data-ttu-id="db94a-214">Esiste già.</span><span class="sxs-lookup"><span data-stu-id="db94a-214">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="db94a-215">**Percorso, file o oggetto non trovato**</span><span class="sxs-lookup"><span data-stu-id="db94a-215">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="db94a-216">94</span><span class="sxs-lookup"><span data-stu-id="db94a-216">94</span></span>

<span data-ttu-id="db94a-217">Il percorso, il file o l'oggetto non è stato trovato.</span><span class="sxs-lookup"><span data-stu-id="db94a-217">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="db94a-218">**Non è possibile inviare una notifica al servizio**</span><span class="sxs-lookup"><span data-stu-id="db94a-218">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="db94a-219">95</span><span class="sxs-lookup"><span data-stu-id="db94a-219">95</span></span>

<span data-ttu-id="db94a-220">Impossibile notificare il servizio.</span><span class="sxs-lookup"><span data-stu-id="db94a-220">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="db94a-221">**Non è possibile inviare una notifica al servizio DNS**</span><span class="sxs-lookup"><span data-stu-id="db94a-221">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="db94a-222">96</span><span class="sxs-lookup"><span data-stu-id="db94a-222">96</span></span>

<span data-ttu-id="db94a-223">Impossibile inviare una notifica al servizio DNS.</span><span class="sxs-lookup"><span data-stu-id="db94a-223">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="db94a-224">**Interfaccia non configurabile**</span><span class="sxs-lookup"><span data-stu-id="db94a-224">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="db94a-225">97</span><span class="sxs-lookup"><span data-stu-id="db94a-225">97</span></span>

<span data-ttu-id="db94a-226">Interfaccia non configurabile.</span><span class="sxs-lookup"><span data-stu-id="db94a-226">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="db94a-227">**Non tutti i lease DHCP possono essere rilasciati/rinnovati**</span><span class="sxs-lookup"><span data-stu-id="db94a-227">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="db94a-228">98</span><span class="sxs-lookup"><span data-stu-id="db94a-228">98</span></span>

<span data-ttu-id="db94a-229">Non tutti i lease DHCP possono essere rilasciati o rinnovati.</span><span class="sxs-lookup"><span data-stu-id="db94a-229">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="db94a-230">**DHCP non abilitato sull'adapter**</span><span class="sxs-lookup"><span data-stu-id="db94a-230">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="db94a-231">100</span><span class="sxs-lookup"><span data-stu-id="db94a-231">100</span></span>

<span data-ttu-id="db94a-232">DHCP non abilitato sulla scheda.</span><span class="sxs-lookup"><span data-stu-id="db94a-232">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="db94a-233">**Altri**</span><span class="sxs-lookup"><span data-stu-id="db94a-233">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="db94a-234">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="db94a-234">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="db94a-235">Commenti</span><span class="sxs-lookup"><span data-stu-id="db94a-235">Remarks</span></span>

<span data-ttu-id="db94a-236">Il metodo statico della [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetDefaultTOS** viene usato per impostare il valore predefinito di TOS nell'intestazione dei pacchetti IP in uscita.</span><span class="sxs-lookup"><span data-stu-id="db94a-236">The **SetDefaultTOS** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to set the default TOS value in the header of outgoing IP packets.</span></span>

## <a name="requirements"></a><span data-ttu-id="db94a-237">Requisiti</span><span class="sxs-lookup"><span data-stu-id="db94a-237">Requirements</span></span>



| <span data-ttu-id="db94a-238">Requisito</span><span class="sxs-lookup"><span data-stu-id="db94a-238">Requirement</span></span> | <span data-ttu-id="db94a-239">Valore</span><span class="sxs-lookup"><span data-stu-id="db94a-239">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="db94a-240">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="db94a-240">Minimum supported client</span></span><br/> | <span data-ttu-id="db94a-241">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="db94a-241">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="db94a-242">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="db94a-242">Minimum supported server</span></span><br/> | <span data-ttu-id="db94a-243">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="db94a-243">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="db94a-244">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="db94a-244">Namespace</span></span><br/>                | <span data-ttu-id="db94a-245">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="db94a-245">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="db94a-246">MOF</span><span class="sxs-lookup"><span data-stu-id="db94a-246">MOF</span></span><br/>                      | <dl> <span data-ttu-id="db94a-247"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="db94a-247"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="db94a-248">DLL</span><span class="sxs-lookup"><span data-stu-id="db94a-248">DLL</span></span><br/>                      | <dl> <span data-ttu-id="db94a-249"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="db94a-249"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db94a-250">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="db94a-250">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db94a-251">Classi hardware del sistema del computer</span><span class="sxs-lookup"><span data-stu-id="db94a-251">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="db94a-252">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="db94a-252">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="db94a-253">Attività WMI: rete</span><span class="sxs-lookup"><span data-stu-id="db94a-253">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="db94a-254">Attività WMI: account e domini</span><span class="sxs-lookup"><span data-stu-id="db94a-254">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="db94a-255">Supporto di IPv6 e IPv4 in WMI</span><span class="sxs-lookup"><span data-stu-id="db94a-255">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

