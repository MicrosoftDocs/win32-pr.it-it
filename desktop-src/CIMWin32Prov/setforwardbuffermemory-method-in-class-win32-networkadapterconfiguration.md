---
description: Il metodo statico della classe WMI SetForwardBufferMemory viene utilizzato per specificare la quantità di memoria allocata dall'IP per archiviare i dati dei pacchetti nella coda dei pacchetti del router.
ms.assetid: e76452e8-2ee8-4d39-9405-33b0aeeac74d
ms.tgt_platform: multiple
title: Metodo SetForwardBufferMemory della classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetForwardBufferMemory
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 30179610e6eee121a86119fa347067b40ef04c2f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877962"
---
# <a name="setforwardbuffermemory-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="b8a2e-103">Metodo SetForwardBufferMemory della \_ classe NetworkAdapterConfiguration Win32</span><span class="sxs-lookup"><span data-stu-id="b8a2e-103">SetForwardBufferMemory method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="b8a2e-104">Il metodo statico della [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetForwardBufferMemory** viene utilizzato per specificare la quantità di memoria allocata dall'IP per archiviare i dati dei pacchetti nella coda dei pacchetti del router.</span><span class="sxs-lookup"><span data-stu-id="b8a2e-104">The **SetForwardBufferMemory** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to specify how much memory IP allocates to store packet data in the router packet queue.</span></span>

<span data-ttu-id="b8a2e-105">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="b8a2e-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="b8a2e-106">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="b8a2e-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="b8a2e-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b8a2e-107">Syntax</span></span>


```mof
uint32 SetForwardBufferMemory(
  [in] uint32 ForwardBufferMemory
);
```



## <a name="parameters"></a><span data-ttu-id="b8a2e-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="b8a2e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8a2e-109">*ForwardBufferMemory* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b8a2e-109">*ForwardBufferMemory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8a2e-110">Dimensione, in byte, della coda di pacchetti del router utilizzata per archiviare i dati dei pacchetti.</span><span class="sxs-lookup"><span data-stu-id="b8a2e-110">Size, in bytes, of the router packet queue used to store packet data.</span></span> <span data-ttu-id="b8a2e-111">Il valore predefinito è 74240 (pacchetti da 50 1480 byte, arrotondati a un multiplo di 256).</span><span class="sxs-lookup"><span data-stu-id="b8a2e-111">The default value is 74240 (fifty 1480-byte packets, rounded to a multiple of 256).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8a2e-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b8a2e-112">Return value</span></span>

<span data-ttu-id="b8a2e-113">Restituisce un valore pari a 0 (zero) per un completamento corretto quando non è richiesto il riavvio, 1 (uno) per un completamento corretto quando è necessario un riavvio e un numero diverso se si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="b8a2e-113">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="b8a2e-114">Per ulteriori informazioni sui codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="b8a2e-114">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="b8a2e-115">Per i valori **HRESULT** generali, vedere [codici di errore di sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="b8a2e-115">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="b8a2e-116">**Operazione completata, non è necessario riavviare il computer**</span><span class="sxs-lookup"><span data-stu-id="b8a2e-116">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="b8a2e-117">0</span><span class="sxs-lookup"><span data-stu-id="b8a2e-117">0</span></span>

<span data-ttu-id="b8a2e-118">Operazione completata, non è necessario riavviare il computer.</span><span class="sxs-lookup"><span data-stu-id="b8a2e-118">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="b8a2e-119">**Operazione completata, riavvio richiesto**</span><span class="sxs-lookup"><span data-stu-id="b8a2e-119">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="b8a2e-120">1</span><span class="sxs-lookup"><span data-stu-id="b8a2e-120">1</span></span>

<span data-ttu-id="b8a2e-121">Operazione completata, è necessario riavviare il computer.</span><span class="sxs-lookup"><span data-stu-id="b8a2e-121">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="b8a2e-122">**Metodo non supportato in questa piattaforma**</span><span class="sxs-lookup"><span data-stu-id="b8a2e-122">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="b8a2e-123">64</span><span class="sxs-lookup"><span data-stu-id="b8a2e-123">64</span></span>

<span data-ttu-id="b8a2e-124">Metodo non supportato in questa piattaforma.</span><span class="sxs-lookup"><span data-stu-id="b8a2e-124">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="b8a2e-125">**Errore sconosciuto**</span><span class="sxs-lookup"><span data-stu-id="b8a2e-125">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="b8a2e-126">65</span><span class="sxs-lookup"><span data-stu-id="b8a2e-126">65</span></span>

<span data-ttu-id="b8a2e-127">Errore sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="b8a2e-127">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="b8a2e-128">**subnet mask non valido**</span><span class="sxs-lookup"><span data-stu-id="b8a2e-128">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="b8a2e-129">66</span><span class="sxs-lookup"><span data-stu-id="b8a2e-129">66</span></span>

<span data-ttu-id="b8a2e-130">Subnet mask non valido.</span><span class="sxs-lookup"><span data-stu-id="b8a2e-130">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="b8a2e-131">**Si è verificato un errore durante l'elaborazione di un'istanza restituita**</span><span class="sxs-lookup"><span data-stu-id="b8a2e-131">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="b8a2e-132">67</span><span class="sxs-lookup"><span data-stu-id="b8a2e-132">67</span></span>

<span data-ttu-id="b8a2e-133">Si è verificato un errore durante l'elaborazione di un'istanza di restituita.</span><span class="sxs-lookup"><span data-stu-id="b8a2e-133">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="b8a2e-134">**Parametro di input non valido**</span><span class="sxs-lookup"><span data-stu-id="b8a2e-134">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="b8a2e-135">68</span><span class="sxs-lookup"><span data-stu-id="b8a2e-135">68</span></span>

<span data-ttu-id="b8a2e-136">Parametro di input non valido.</span><span class="sxs-lookup"><span data-stu-id="b8a2e-136">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="b8a2e-137">**Sono stati specificati più di 5 gateway**</span><span class="sxs-lookup"><span data-stu-id="b8a2e-137">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="b8a2e-138">69</span><span class="sxs-lookup"><span data-stu-id="b8a2e-138">69</span></span>

<span data-ttu-id="b8a2e-139">Sono stati specificati più di cinque gateway.</span><span class="sxs-lookup"><span data-stu-id="b8a2e-139">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="b8a2e-140">**Indirizzo IP non valido**</span><span class="sxs-lookup"><span data-stu-id="b8a2e-140">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="b8a2e-141">70</span><span class="sxs-lookup"><span data-stu-id="b8a2e-141">70</span></span>

<span data-ttu-id="b8a2e-142">Indirizzo IP non valido.</span><span class="sxs-lookup"><span data-stu-id="b8a2e-142">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="b8a2e-143">**Indirizzo IP gateway non valido**</span><span class="sxs-lookup"><span data-stu-id="b8a2e-143">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="b8a2e-144">71</span><span class="sxs-lookup"><span data-stu-id="b8a2e-144">71</span></span>

<span data-ttu-id="b8a2e-145">Indirizzo IP del gateway non valido.</span><span class="sxs-lookup"><span data-stu-id="b8a2e-145">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="b8a2e-146">**Si è verificato un errore durante l'accesso al registro di sistema per le informazioni richieste**</span><span class="sxs-lookup"><span data-stu-id="b8a2e-146">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="b8a2e-147">72</span><span class="sxs-lookup"><span data-stu-id="b8a2e-147">72</span></span>

<span data-ttu-id="b8a2e-148">Si è verificato un errore durante l'accesso al registro di sistema per le informazioni richieste.</span><span class="sxs-lookup"><span data-stu-id="b8a2e-148">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="b8a2e-149">**Nome di dominio non valido**</span><span class="sxs-lookup"><span data-stu-id="b8a2e-149">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="b8a2e-150">73</span><span class="sxs-lookup"><span data-stu-id="b8a2e-150">73</span></span>

<span data-ttu-id="b8a2e-151">Nome di dominio non valido.</span><span class="sxs-lookup"><span data-stu-id="b8a2e-151">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="b8a2e-152">**Nome host non valido**</span><span class="sxs-lookup"><span data-stu-id="b8a2e-152">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="b8a2e-153">74</span><span class="sxs-lookup"><span data-stu-id="b8a2e-153">74</span></span>

<span data-ttu-id="b8a2e-154">Nome host non valido.</span><span class="sxs-lookup"><span data-stu-id="b8a2e-154">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="b8a2e-155">**Nessun server WINS primario/secondario definito**</span><span class="sxs-lookup"><span data-stu-id="b8a2e-155">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="b8a2e-156">75</span><span class="sxs-lookup"><span data-stu-id="b8a2e-156">75</span></span>

<span data-ttu-id="b8a2e-157">Nessun server WINS primario o secondario definito.</span><span class="sxs-lookup"><span data-stu-id="b8a2e-157">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="b8a2e-158">**File non valido**</span><span class="sxs-lookup"><span data-stu-id="b8a2e-158">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="b8a2e-159">76</span><span class="sxs-lookup"><span data-stu-id="b8a2e-159">76</span></span>

<span data-ttu-id="b8a2e-160">File non valido.</span><span class="sxs-lookup"><span data-stu-id="b8a2e-160">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="b8a2e-161">**Percorso di sistema non valido**</span><span class="sxs-lookup"><span data-stu-id="b8a2e-161">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="b8a2e-162">77</span><span class="sxs-lookup"><span data-stu-id="b8a2e-162">77</span></span>

<span data-ttu-id="b8a2e-163">Percorso di sistema non valido.</span><span class="sxs-lookup"><span data-stu-id="b8a2e-163">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="b8a2e-164">**Copia del file non riuscita**</span><span class="sxs-lookup"><span data-stu-id="b8a2e-164">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="b8a2e-165">78</span><span class="sxs-lookup"><span data-stu-id="b8a2e-165">78</span></span>

<span data-ttu-id="b8a2e-166">Copia del file non riuscita.</span><span class="sxs-lookup"><span data-stu-id="b8a2e-166">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="b8a2e-167">**Parametro di sicurezza non valido**</span><span class="sxs-lookup"><span data-stu-id="b8a2e-167">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="b8a2e-168">79</span><span class="sxs-lookup"><span data-stu-id="b8a2e-168">79</span></span>

<span data-ttu-id="b8a2e-169">Parametro di sicurezza non valido.</span><span class="sxs-lookup"><span data-stu-id="b8a2e-169">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="b8a2e-170">**Impossibile configurare il servizio TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="b8a2e-170">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="b8a2e-171">80</span><span class="sxs-lookup"><span data-stu-id="b8a2e-171">80</span></span>

<span data-ttu-id="b8a2e-172">Impossibile configurare il servizio TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="b8a2e-172">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="b8a2e-173">**Non è possibile configurare il servizio DHCP**</span><span class="sxs-lookup"><span data-stu-id="b8a2e-173">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="b8a2e-174">81</span><span class="sxs-lookup"><span data-stu-id="b8a2e-174">81</span></span>

<span data-ttu-id="b8a2e-175">Impossibile configurare il servizio DHCP.</span><span class="sxs-lookup"><span data-stu-id="b8a2e-175">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="b8a2e-176">**Non è possibile rinnovare il lease DHCP**</span><span class="sxs-lookup"><span data-stu-id="b8a2e-176">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="b8a2e-177">82</span><span class="sxs-lookup"><span data-stu-id="b8a2e-177">82</span></span>

<span data-ttu-id="b8a2e-178">Non è possibile rinnovare il lease DHCP.</span><span class="sxs-lookup"><span data-stu-id="b8a2e-178">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="b8a2e-179">**Non è possibile rilasciare il lease DHCP**</span><span class="sxs-lookup"><span data-stu-id="b8a2e-179">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="b8a2e-180">83</span><span class="sxs-lookup"><span data-stu-id="b8a2e-180">83</span></span>

<span data-ttu-id="b8a2e-181">Impossibile rilasciare il lease DHCP.</span><span class="sxs-lookup"><span data-stu-id="b8a2e-181">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="b8a2e-182">**IP non abilitato sulla scheda**</span><span class="sxs-lookup"><span data-stu-id="b8a2e-182">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="b8a2e-183">84</span><span class="sxs-lookup"><span data-stu-id="b8a2e-183">84</span></span>

<span data-ttu-id="b8a2e-184">IP non abilitato sulla scheda.</span><span class="sxs-lookup"><span data-stu-id="b8a2e-184">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="b8a2e-185">**IPX non abilitato sull'adapter**</span><span class="sxs-lookup"><span data-stu-id="b8a2e-185">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="b8a2e-186">85</span><span class="sxs-lookup"><span data-stu-id="b8a2e-186">85</span></span>

<span data-ttu-id="b8a2e-187">IPX non abilitato sulla scheda.</span><span class="sxs-lookup"><span data-stu-id="b8a2e-187">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="b8a2e-188">**Errore limite numero frame/rete**</span><span class="sxs-lookup"><span data-stu-id="b8a2e-188">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="b8a2e-189">86</span><span class="sxs-lookup"><span data-stu-id="b8a2e-189">86</span></span>

<span data-ttu-id="b8a2e-190">Errore dei limiti del numero di rete o del frame.</span><span class="sxs-lookup"><span data-stu-id="b8a2e-190">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="b8a2e-191">**Tipo di frame non valido**</span><span class="sxs-lookup"><span data-stu-id="b8a2e-191">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="b8a2e-192">87</span><span class="sxs-lookup"><span data-stu-id="b8a2e-192">87</span></span>

<span data-ttu-id="b8a2e-193">Tipo di frame non valido.</span><span class="sxs-lookup"><span data-stu-id="b8a2e-193">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="b8a2e-194">**Numero di rete non valido**</span><span class="sxs-lookup"><span data-stu-id="b8a2e-194">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="b8a2e-195">88</span><span class="sxs-lookup"><span data-stu-id="b8a2e-195">88</span></span>

<span data-ttu-id="b8a2e-196">Numero di rete non valido.</span><span class="sxs-lookup"><span data-stu-id="b8a2e-196">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="b8a2e-197">**Numero di rete duplicato**</span><span class="sxs-lookup"><span data-stu-id="b8a2e-197">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="b8a2e-198">89</span><span class="sxs-lookup"><span data-stu-id="b8a2e-198">89</span></span>

<span data-ttu-id="b8a2e-199">Numero di rete duplicato.</span><span class="sxs-lookup"><span data-stu-id="b8a2e-199">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="b8a2e-200">**Parametro fuori limite**</span><span class="sxs-lookup"><span data-stu-id="b8a2e-200">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="b8a2e-201">90</span><span class="sxs-lookup"><span data-stu-id="b8a2e-201">90</span></span>

<span data-ttu-id="b8a2e-202">Parametro fuori limite.</span><span class="sxs-lookup"><span data-stu-id="b8a2e-202">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="b8a2e-203">**Accesso negato**</span><span class="sxs-lookup"><span data-stu-id="b8a2e-203">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="b8a2e-204">91</span><span class="sxs-lookup"><span data-stu-id="b8a2e-204">91</span></span>

<span data-ttu-id="b8a2e-205">Accesso negato.</span><span class="sxs-lookup"><span data-stu-id="b8a2e-205">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="b8a2e-206">**Memoria insufficiente**</span><span class="sxs-lookup"><span data-stu-id="b8a2e-206">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="b8a2e-207">92</span><span class="sxs-lookup"><span data-stu-id="b8a2e-207">92</span></span>

<span data-ttu-id="b8a2e-208">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="b8a2e-208">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="b8a2e-209">**Esiste già**</span><span class="sxs-lookup"><span data-stu-id="b8a2e-209">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="b8a2e-210">93</span><span class="sxs-lookup"><span data-stu-id="b8a2e-210">93</span></span>

<span data-ttu-id="b8a2e-211">Esiste già.</span><span class="sxs-lookup"><span data-stu-id="b8a2e-211">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="b8a2e-212">**Percorso, file o oggetto non trovato**</span><span class="sxs-lookup"><span data-stu-id="b8a2e-212">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="b8a2e-213">94</span><span class="sxs-lookup"><span data-stu-id="b8a2e-213">94</span></span>

<span data-ttu-id="b8a2e-214">Il percorso, il file o l'oggetto non è stato trovato.</span><span class="sxs-lookup"><span data-stu-id="b8a2e-214">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="b8a2e-215">**Non è possibile inviare una notifica al servizio**</span><span class="sxs-lookup"><span data-stu-id="b8a2e-215">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="b8a2e-216">95</span><span class="sxs-lookup"><span data-stu-id="b8a2e-216">95</span></span>

<span data-ttu-id="b8a2e-217">Impossibile notificare il servizio.</span><span class="sxs-lookup"><span data-stu-id="b8a2e-217">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="b8a2e-218">**Non è possibile inviare una notifica al servizio DNS**</span><span class="sxs-lookup"><span data-stu-id="b8a2e-218">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="b8a2e-219">96</span><span class="sxs-lookup"><span data-stu-id="b8a2e-219">96</span></span>

<span data-ttu-id="b8a2e-220">Impossibile inviare una notifica al servizio DNS.</span><span class="sxs-lookup"><span data-stu-id="b8a2e-220">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="b8a2e-221">**Interfaccia non configurabile**</span><span class="sxs-lookup"><span data-stu-id="b8a2e-221">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="b8a2e-222">97</span><span class="sxs-lookup"><span data-stu-id="b8a2e-222">97</span></span>

<span data-ttu-id="b8a2e-223">Interfaccia non configurabile.</span><span class="sxs-lookup"><span data-stu-id="b8a2e-223">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="b8a2e-224">**Non tutti i lease DHCP possono essere rilasciati/rinnovati**</span><span class="sxs-lookup"><span data-stu-id="b8a2e-224">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="b8a2e-225">98</span><span class="sxs-lookup"><span data-stu-id="b8a2e-225">98</span></span>

<span data-ttu-id="b8a2e-226">Non tutti i lease DHCP possono essere rilasciati o rinnovati.</span><span class="sxs-lookup"><span data-stu-id="b8a2e-226">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="b8a2e-227">**DHCP non abilitato sull'adapter**</span><span class="sxs-lookup"><span data-stu-id="b8a2e-227">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="b8a2e-228">100</span><span class="sxs-lookup"><span data-stu-id="b8a2e-228">100</span></span>

<span data-ttu-id="b8a2e-229">DHCP non abilitato sulla scheda.</span><span class="sxs-lookup"><span data-stu-id="b8a2e-229">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="b8a2e-230">**Altri**</span><span class="sxs-lookup"><span data-stu-id="b8a2e-230">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="b8a2e-231">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="b8a2e-231">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b8a2e-232">Commenti</span><span class="sxs-lookup"><span data-stu-id="b8a2e-232">Remarks</span></span>

<span data-ttu-id="b8a2e-233">Quando lo spazio del buffer viene riempito, il router inizia a scartare i pacchetti in modo casuale dalla propria coda.</span><span class="sxs-lookup"><span data-stu-id="b8a2e-233">When this buffer space is filled, the router begins discarding packets at random from its queue.</span></span>

<span data-ttu-id="b8a2e-234">I buffer di dati della coda di pacchetti hanno una lunghezza di 256 byte, quindi il valore del parametro *ForwardBufferMemory* deve essere un multiplo di 256.</span><span class="sxs-lookup"><span data-stu-id="b8a2e-234">Packet queue data buffers are 256 bytes in length, so the value of the *ForwardBufferMemory* parameter should be a multiple of 256.</span></span> <span data-ttu-id="b8a2e-235">Più buffer vengono concatenati per i pacchetti più grandi.</span><span class="sxs-lookup"><span data-stu-id="b8a2e-235">Multiple buffers are chained together for larger packets.</span></span> <span data-ttu-id="b8a2e-236">L'intestazione IP per un pacchetto viene archiviata separatamente.</span><span class="sxs-lookup"><span data-stu-id="b8a2e-236">The IP header for a packet is stored separately.</span></span> <span data-ttu-id="b8a2e-237">Questo parametro viene ignorato e non vengono allocati buffer se il router IP non è abilitato.</span><span class="sxs-lookup"><span data-stu-id="b8a2e-237">This parameter is ignored and no buffers are allocated if the IP router is not enabled.</span></span> <span data-ttu-id="b8a2e-238">La dimensione del buffer può variare dall'unità di trasmissione massima (MTU) di rete a un valore inferiore a 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="b8a2e-238">The buffer size can range from the network Maximum Transmission Unit (MTU) to a value smaller than 0xFFFFFFFF.</span></span>

## <a name="examples"></a><span data-ttu-id="b8a2e-239">Esempio</span><span class="sxs-lookup"><span data-stu-id="b8a2e-239">Examples</span></span>

<span data-ttu-id="b8a2e-240">L'esempio di [modifica della memoria del buffer di avanzamento per tutte le schede di rete](https://Gallery.TechNet.Microsoft.Com/da5712dc-f854-4099-98a9-59c0ff20a524) consente di configurare la memoria del buffer di avanzamento per tutte le schede di rete in un computer.</span><span class="sxs-lookup"><span data-stu-id="b8a2e-240">The [Modify the Forward Buffer Memory for All Network Adapters](https://Gallery.TechNet.Microsoft.Com/da5712dc-f854-4099-98a9-59c0ff20a524) VBScript sample configures the forward buffer memory for all network adapters on a computer.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8a2e-241">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b8a2e-241">Requirements</span></span>



| <span data-ttu-id="b8a2e-242">Requisito</span><span class="sxs-lookup"><span data-stu-id="b8a2e-242">Requirement</span></span> | <span data-ttu-id="b8a2e-243">Valore</span><span class="sxs-lookup"><span data-stu-id="b8a2e-243">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b8a2e-244">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b8a2e-244">Minimum supported client</span></span><br/> | <span data-ttu-id="b8a2e-245">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b8a2e-245">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b8a2e-246">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b8a2e-246">Minimum supported server</span></span><br/> | <span data-ttu-id="b8a2e-247">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b8a2e-247">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b8a2e-248">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b8a2e-248">Namespace</span></span><br/>                | <span data-ttu-id="b8a2e-249">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="b8a2e-249">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b8a2e-250">MOF</span><span class="sxs-lookup"><span data-stu-id="b8a2e-250">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b8a2e-251"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b8a2e-251"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b8a2e-252">DLL</span><span class="sxs-lookup"><span data-stu-id="b8a2e-252">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b8a2e-253"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b8a2e-253"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8a2e-254">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b8a2e-254">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8a2e-255">Classi hardware del sistema del computer</span><span class="sxs-lookup"><span data-stu-id="b8a2e-255">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="b8a2e-256">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="b8a2e-256">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="b8a2e-257">Attività WMI: rete</span><span class="sxs-lookup"><span data-stu-id="b8a2e-257">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="b8a2e-258">Attività WMI: account e domini</span><span class="sxs-lookup"><span data-stu-id="b8a2e-258">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="b8a2e-259">Supporto di IPv6 e IPv4 in WMI</span><span class="sxs-lookup"><span data-stu-id="b8a2e-259">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

