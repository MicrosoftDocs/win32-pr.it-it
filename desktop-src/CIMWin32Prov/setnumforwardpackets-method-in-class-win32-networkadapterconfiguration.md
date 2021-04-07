---
description: Il metodo statico della classe WMI SetNumForwardPackets viene utilizzato per impostare il numero di intestazioni di pacchetti IP allocate per la coda dei pacchetti router. Quando tutte le intestazioni sono in uso, il router inizierà a eliminare i pacchetti dalla coda in modo casuale.
ms.assetid: cadc7565-4cad-4e0f-a1eb-bf99d333bb28
ms.tgt_platform: multiple
title: Metodo SetNumForwardPackets della classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetNumForwardPackets
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: f46ecd62766b5df642dff1e52614171a513a8fca
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748567"
---
# <a name="setnumforwardpackets-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="4b49e-104">Metodo SetNumForwardPackets della \_ classe NetworkAdapterConfiguration Win32</span><span class="sxs-lookup"><span data-stu-id="4b49e-104">SetNumForwardPackets method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="4b49e-105">Il metodo statico della [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetNumForwardPackets** viene utilizzato per impostare il numero di intestazioni di pacchetti IP allocate per la coda dei pacchetti router.</span><span class="sxs-lookup"><span data-stu-id="4b49e-105">The **SetNumForwardPackets** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to set the number of IP packet headers allocated for the router packet queue.</span></span> <span data-ttu-id="4b49e-106">Quando tutte le intestazioni sono in uso, il router inizierà a eliminare i pacchetti dalla coda in modo casuale.</span><span class="sxs-lookup"><span data-stu-id="4b49e-106">When all headers are in use, the router will begin to discard packets from the queue at random.</span></span>

<span data-ttu-id="4b49e-107">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="4b49e-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="4b49e-108">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="4b49e-108">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="4b49e-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4b49e-109">Syntax</span></span>


```mof
uint32 SetNumForwardPackets(
  [in] uint32 NumForwardPackets
);
```



## <a name="parameters"></a><span data-ttu-id="4b49e-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="4b49e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4b49e-111">*NumForwardPackets* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4b49e-111">*NumForwardPackets* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b49e-112">Numero di intestazioni di pacchetti IP allocate per la coda dei pacchetti router.</span><span class="sxs-lookup"><span data-stu-id="4b49e-112">Number of IP packet headers allocated for the router packet queue.</span></span> <span data-ttu-id="4b49e-113">Deve essere almeno uguale al valore della proprietà [**ForwardBufferMemory**](win32-networkadapterconfiguration.md) divisa per la dimensione massima dei dati IP delle reti connesse al router.</span><span class="sxs-lookup"><span data-stu-id="4b49e-113">This should be at least as large as the value of the [**ForwardBufferMemory**](win32-networkadapterconfiguration.md) property divided by the maximum IP data size of the networks connected to the router.</span></span> <span data-ttu-id="4b49e-114">Il valore non deve essere maggiore del valore di **ForwardBufferMemory** diviso per 256, perché ogni pacchetto richiede almeno 256 byte di memoria del buffer di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="4b49e-114">It should be no larger than the **ForwardBufferMemory** value divided by 256, since at least 256 bytes of forward buffer memory are required by each packet.</span></span> <span data-ttu-id="4b49e-115">Il numero ottimale di pacchetti di avanzamento per una determinata dimensione di **ForwardBufferMemory** dipende dal tipo di traffico che viene eseguito sulla rete e da un punto tra questi due valori.</span><span class="sxs-lookup"><span data-stu-id="4b49e-115">The optimal number of forward packets for a given **ForwardBufferMemory** size depends on the type of traffic carried on the network, and will be somewhere between these two values.</span></span> <span data-ttu-id="4b49e-116">Se il router è disabilitato, questo parametro viene ignorato e non vengono allocate intestazioni.</span><span class="sxs-lookup"><span data-stu-id="4b49e-116">If the router is disabled, this parameter is ignored and no headers are allocated.</span></span> <span data-ttu-id="4b49e-117">Intervallo valido: 1 0xFFFFFFFE.</span><span class="sxs-lookup"><span data-stu-id="4b49e-117">Valid range: 1 - 0xFFFFFFFE.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4b49e-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4b49e-118">Return value</span></span>

<span data-ttu-id="4b49e-119">Restituisce un valore pari a 0 (zero) per un completamento corretto quando non è richiesto il riavvio, 1 (uno) per un completamento corretto quando è necessario un riavvio e un numero diverso se si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="4b49e-119">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="4b49e-120">Per ulteriori informazioni sui codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="4b49e-120">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="4b49e-121">Per i valori **HRESULT** generali, vedere [codici di errore di sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="4b49e-121">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="4b49e-122">**Operazione completata, non è necessario riavviare il computer**</span><span class="sxs-lookup"><span data-stu-id="4b49e-122">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="4b49e-123">0</span><span class="sxs-lookup"><span data-stu-id="4b49e-123">0</span></span>

<span data-ttu-id="4b49e-124">Operazione completata, non è necessario riavviare il computer.</span><span class="sxs-lookup"><span data-stu-id="4b49e-124">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="4b49e-125">**Operazione completata, riavvio richiesto**</span><span class="sxs-lookup"><span data-stu-id="4b49e-125">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="4b49e-126">1</span><span class="sxs-lookup"><span data-stu-id="4b49e-126">1</span></span>

<span data-ttu-id="4b49e-127">Operazione completata, è necessario riavviare il computer.</span><span class="sxs-lookup"><span data-stu-id="4b49e-127">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="4b49e-128">**Metodo non supportato in questa piattaforma**</span><span class="sxs-lookup"><span data-stu-id="4b49e-128">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="4b49e-129">64</span><span class="sxs-lookup"><span data-stu-id="4b49e-129">64</span></span>

<span data-ttu-id="4b49e-130">Metodo non supportato in questa piattaforma.</span><span class="sxs-lookup"><span data-stu-id="4b49e-130">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="4b49e-131">**Errore sconosciuto**</span><span class="sxs-lookup"><span data-stu-id="4b49e-131">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="4b49e-132">65</span><span class="sxs-lookup"><span data-stu-id="4b49e-132">65</span></span>

<span data-ttu-id="4b49e-133">Errore sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="4b49e-133">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="4b49e-134">**subnet mask non valido**</span><span class="sxs-lookup"><span data-stu-id="4b49e-134">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="4b49e-135">66</span><span class="sxs-lookup"><span data-stu-id="4b49e-135">66</span></span>

<span data-ttu-id="4b49e-136">Subnet mask non valido.</span><span class="sxs-lookup"><span data-stu-id="4b49e-136">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="4b49e-137">**Si è verificato un errore durante l'elaborazione di un'istanza restituita**</span><span class="sxs-lookup"><span data-stu-id="4b49e-137">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="4b49e-138">67</span><span class="sxs-lookup"><span data-stu-id="4b49e-138">67</span></span>

<span data-ttu-id="4b49e-139">Si è verificato un errore durante l'elaborazione di un'istanza di restituita.</span><span class="sxs-lookup"><span data-stu-id="4b49e-139">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="4b49e-140">**Parametro di input non valido**</span><span class="sxs-lookup"><span data-stu-id="4b49e-140">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="4b49e-141">68</span><span class="sxs-lookup"><span data-stu-id="4b49e-141">68</span></span>

<span data-ttu-id="4b49e-142">Parametro di input non valido.</span><span class="sxs-lookup"><span data-stu-id="4b49e-142">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="4b49e-143">**Sono stati specificati più di 5 gateway**</span><span class="sxs-lookup"><span data-stu-id="4b49e-143">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="4b49e-144">69</span><span class="sxs-lookup"><span data-stu-id="4b49e-144">69</span></span>

<span data-ttu-id="4b49e-145">Sono stati specificati più di cinque gateway.</span><span class="sxs-lookup"><span data-stu-id="4b49e-145">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="4b49e-146">**Indirizzo IP non valido**</span><span class="sxs-lookup"><span data-stu-id="4b49e-146">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="4b49e-147">70</span><span class="sxs-lookup"><span data-stu-id="4b49e-147">70</span></span>

<span data-ttu-id="4b49e-148">Indirizzo IP non valido.</span><span class="sxs-lookup"><span data-stu-id="4b49e-148">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="4b49e-149">**Indirizzo IP gateway non valido**</span><span class="sxs-lookup"><span data-stu-id="4b49e-149">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="4b49e-150">71</span><span class="sxs-lookup"><span data-stu-id="4b49e-150">71</span></span>

<span data-ttu-id="4b49e-151">Indirizzo IP del gateway non valido.</span><span class="sxs-lookup"><span data-stu-id="4b49e-151">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="4b49e-152">**Si è verificato un errore durante l'accesso al registro di sistema per le informazioni richieste**</span><span class="sxs-lookup"><span data-stu-id="4b49e-152">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="4b49e-153">72</span><span class="sxs-lookup"><span data-stu-id="4b49e-153">72</span></span>

<span data-ttu-id="4b49e-154">Si è verificato un errore durante l'accesso al registro di sistema per le informazioni richieste.</span><span class="sxs-lookup"><span data-stu-id="4b49e-154">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="4b49e-155">**Nome di dominio non valido**</span><span class="sxs-lookup"><span data-stu-id="4b49e-155">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="4b49e-156">73</span><span class="sxs-lookup"><span data-stu-id="4b49e-156">73</span></span>

<span data-ttu-id="4b49e-157">Nome di dominio non valido.</span><span class="sxs-lookup"><span data-stu-id="4b49e-157">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="4b49e-158">**Nome host non valido**</span><span class="sxs-lookup"><span data-stu-id="4b49e-158">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="4b49e-159">74</span><span class="sxs-lookup"><span data-stu-id="4b49e-159">74</span></span>

<span data-ttu-id="4b49e-160">Nome host non valido.</span><span class="sxs-lookup"><span data-stu-id="4b49e-160">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="4b49e-161">**Nessun server WINS primario/secondario definito**</span><span class="sxs-lookup"><span data-stu-id="4b49e-161">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="4b49e-162">75</span><span class="sxs-lookup"><span data-stu-id="4b49e-162">75</span></span>

<span data-ttu-id="4b49e-163">Nessun server WINS primario o secondario definito.</span><span class="sxs-lookup"><span data-stu-id="4b49e-163">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="4b49e-164">**File non valido**</span><span class="sxs-lookup"><span data-stu-id="4b49e-164">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="4b49e-165">76</span><span class="sxs-lookup"><span data-stu-id="4b49e-165">76</span></span>

<span data-ttu-id="4b49e-166">File non valido.</span><span class="sxs-lookup"><span data-stu-id="4b49e-166">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="4b49e-167">**Percorso di sistema non valido**</span><span class="sxs-lookup"><span data-stu-id="4b49e-167">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="4b49e-168">77</span><span class="sxs-lookup"><span data-stu-id="4b49e-168">77</span></span>

<span data-ttu-id="4b49e-169">Percorso di sistema non valido.</span><span class="sxs-lookup"><span data-stu-id="4b49e-169">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="4b49e-170">**Copia del file non riuscita**</span><span class="sxs-lookup"><span data-stu-id="4b49e-170">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="4b49e-171">78</span><span class="sxs-lookup"><span data-stu-id="4b49e-171">78</span></span>

<span data-ttu-id="4b49e-172">Copia del file non riuscita.</span><span class="sxs-lookup"><span data-stu-id="4b49e-172">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="4b49e-173">**Parametro di sicurezza non valido**</span><span class="sxs-lookup"><span data-stu-id="4b49e-173">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="4b49e-174">79</span><span class="sxs-lookup"><span data-stu-id="4b49e-174">79</span></span>

<span data-ttu-id="4b49e-175">Parametro di sicurezza non valido.</span><span class="sxs-lookup"><span data-stu-id="4b49e-175">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="4b49e-176">**Impossibile configurare il servizio TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="4b49e-176">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="4b49e-177">80</span><span class="sxs-lookup"><span data-stu-id="4b49e-177">80</span></span>

<span data-ttu-id="4b49e-178">Impossibile configurare il servizio TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="4b49e-178">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="4b49e-179">**Non è possibile configurare il servizio DHCP**</span><span class="sxs-lookup"><span data-stu-id="4b49e-179">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="4b49e-180">81</span><span class="sxs-lookup"><span data-stu-id="4b49e-180">81</span></span>

<span data-ttu-id="4b49e-181">Impossibile configurare il servizio DHCP.</span><span class="sxs-lookup"><span data-stu-id="4b49e-181">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="4b49e-182">**Non è possibile rinnovare il lease DHCP**</span><span class="sxs-lookup"><span data-stu-id="4b49e-182">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="4b49e-183">82</span><span class="sxs-lookup"><span data-stu-id="4b49e-183">82</span></span>

<span data-ttu-id="4b49e-184">Non è possibile rinnovare il lease DHCP.</span><span class="sxs-lookup"><span data-stu-id="4b49e-184">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="4b49e-185">**Non è possibile rilasciare il lease DHCP**</span><span class="sxs-lookup"><span data-stu-id="4b49e-185">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="4b49e-186">83</span><span class="sxs-lookup"><span data-stu-id="4b49e-186">83</span></span>

<span data-ttu-id="4b49e-187">Impossibile rilasciare il lease DHCP.</span><span class="sxs-lookup"><span data-stu-id="4b49e-187">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="4b49e-188">**IP non abilitato sulla scheda**</span><span class="sxs-lookup"><span data-stu-id="4b49e-188">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="4b49e-189">84</span><span class="sxs-lookup"><span data-stu-id="4b49e-189">84</span></span>

<span data-ttu-id="4b49e-190">IP non abilitato sulla scheda.</span><span class="sxs-lookup"><span data-stu-id="4b49e-190">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="4b49e-191">**IPX non abilitato sull'adapter**</span><span class="sxs-lookup"><span data-stu-id="4b49e-191">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="4b49e-192">85</span><span class="sxs-lookup"><span data-stu-id="4b49e-192">85</span></span>

<span data-ttu-id="4b49e-193">IPX non abilitato sulla scheda.</span><span class="sxs-lookup"><span data-stu-id="4b49e-193">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="4b49e-194">**Errore limite numero frame/rete**</span><span class="sxs-lookup"><span data-stu-id="4b49e-194">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="4b49e-195">86</span><span class="sxs-lookup"><span data-stu-id="4b49e-195">86</span></span>

<span data-ttu-id="4b49e-196">Errore dei limiti del numero di rete o del frame.</span><span class="sxs-lookup"><span data-stu-id="4b49e-196">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="4b49e-197">**Tipo di frame non valido**</span><span class="sxs-lookup"><span data-stu-id="4b49e-197">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="4b49e-198">87</span><span class="sxs-lookup"><span data-stu-id="4b49e-198">87</span></span>

<span data-ttu-id="4b49e-199">Tipo di frame non valido.</span><span class="sxs-lookup"><span data-stu-id="4b49e-199">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="4b49e-200">**Numero di rete non valido**</span><span class="sxs-lookup"><span data-stu-id="4b49e-200">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="4b49e-201">88</span><span class="sxs-lookup"><span data-stu-id="4b49e-201">88</span></span>

<span data-ttu-id="4b49e-202">Numero di rete non valido.</span><span class="sxs-lookup"><span data-stu-id="4b49e-202">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="4b49e-203">**Numero di rete duplicato**</span><span class="sxs-lookup"><span data-stu-id="4b49e-203">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="4b49e-204">89</span><span class="sxs-lookup"><span data-stu-id="4b49e-204">89</span></span>

<span data-ttu-id="4b49e-205">Numero di rete duplicato.</span><span class="sxs-lookup"><span data-stu-id="4b49e-205">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="4b49e-206">**Parametro fuori limite**</span><span class="sxs-lookup"><span data-stu-id="4b49e-206">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="4b49e-207">90</span><span class="sxs-lookup"><span data-stu-id="4b49e-207">90</span></span>

<span data-ttu-id="4b49e-208">Parametro fuori limite.</span><span class="sxs-lookup"><span data-stu-id="4b49e-208">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="4b49e-209">**Accesso negato**</span><span class="sxs-lookup"><span data-stu-id="4b49e-209">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="4b49e-210">91</span><span class="sxs-lookup"><span data-stu-id="4b49e-210">91</span></span>

<span data-ttu-id="4b49e-211">Accesso negato.</span><span class="sxs-lookup"><span data-stu-id="4b49e-211">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="4b49e-212">**Memoria insufficiente**</span><span class="sxs-lookup"><span data-stu-id="4b49e-212">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="4b49e-213">92</span><span class="sxs-lookup"><span data-stu-id="4b49e-213">92</span></span>

<span data-ttu-id="4b49e-214">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="4b49e-214">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="4b49e-215">**Esiste già**</span><span class="sxs-lookup"><span data-stu-id="4b49e-215">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="4b49e-216">93</span><span class="sxs-lookup"><span data-stu-id="4b49e-216">93</span></span>

<span data-ttu-id="4b49e-217">Esiste già.</span><span class="sxs-lookup"><span data-stu-id="4b49e-217">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="4b49e-218">**Percorso, file o oggetto non trovato**</span><span class="sxs-lookup"><span data-stu-id="4b49e-218">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="4b49e-219">94</span><span class="sxs-lookup"><span data-stu-id="4b49e-219">94</span></span>

<span data-ttu-id="4b49e-220">Il percorso, il file o l'oggetto non è stato trovato.</span><span class="sxs-lookup"><span data-stu-id="4b49e-220">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="4b49e-221">**Non è possibile inviare una notifica al servizio**</span><span class="sxs-lookup"><span data-stu-id="4b49e-221">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="4b49e-222">95</span><span class="sxs-lookup"><span data-stu-id="4b49e-222">95</span></span>

<span data-ttu-id="4b49e-223">Impossibile notificare il servizio.</span><span class="sxs-lookup"><span data-stu-id="4b49e-223">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="4b49e-224">**Non è possibile inviare una notifica al servizio DNS**</span><span class="sxs-lookup"><span data-stu-id="4b49e-224">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="4b49e-225">96</span><span class="sxs-lookup"><span data-stu-id="4b49e-225">96</span></span>

<span data-ttu-id="4b49e-226">Impossibile inviare una notifica al servizio DNS.</span><span class="sxs-lookup"><span data-stu-id="4b49e-226">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="4b49e-227">**Interfaccia non configurabile**</span><span class="sxs-lookup"><span data-stu-id="4b49e-227">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="4b49e-228">97</span><span class="sxs-lookup"><span data-stu-id="4b49e-228">97</span></span>

<span data-ttu-id="4b49e-229">Interfaccia non configurabile.</span><span class="sxs-lookup"><span data-stu-id="4b49e-229">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="4b49e-230">**Non tutti i lease DHCP possono essere rilasciati/rinnovati**</span><span class="sxs-lookup"><span data-stu-id="4b49e-230">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="4b49e-231">98</span><span class="sxs-lookup"><span data-stu-id="4b49e-231">98</span></span>

<span data-ttu-id="4b49e-232">Non tutti i lease DHCP possono essere rilasciati o rinnovati.</span><span class="sxs-lookup"><span data-stu-id="4b49e-232">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="4b49e-233">**DHCP non abilitato sull'adapter**</span><span class="sxs-lookup"><span data-stu-id="4b49e-233">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="4b49e-234">100</span><span class="sxs-lookup"><span data-stu-id="4b49e-234">100</span></span>

<span data-ttu-id="4b49e-235">DHCP non abilitato sulla scheda.</span><span class="sxs-lookup"><span data-stu-id="4b49e-235">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="4b49e-236">**Altri**</span><span class="sxs-lookup"><span data-stu-id="4b49e-236">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="4b49e-237">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="4b49e-237">101 4294967295</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="4b49e-238">Esempio</span><span class="sxs-lookup"><span data-stu-id="4b49e-238">Examples</span></span>

<span data-ttu-id="4b49e-239">Il [modificare il numero di pacchetti di esempio VBScript consentiti](https://Gallery.TechNet.Microsoft.Com/4123c28e-25c4-444e-818b-67bdbcc0cd4c) consente di configurare il numero di pacchetti di avanzamento allocati nella coda dei pacchetti del router.</span><span class="sxs-lookup"><span data-stu-id="4b49e-239">The [Modify the Number of Allowed Forward Packets](https://Gallery.TechNet.Microsoft.Com/4123c28e-25c4-444e-818b-67bdbcc0cd4c) VBScript sample configures the number of forward packets allocated to the router packet queue.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b49e-240">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4b49e-240">Requirements</span></span>



| <span data-ttu-id="4b49e-241">Requisito</span><span class="sxs-lookup"><span data-stu-id="4b49e-241">Requirement</span></span> | <span data-ttu-id="4b49e-242">Valore</span><span class="sxs-lookup"><span data-stu-id="4b49e-242">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4b49e-243">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4b49e-243">Minimum supported client</span></span><br/> | <span data-ttu-id="4b49e-244">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4b49e-244">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4b49e-245">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4b49e-245">Minimum supported server</span></span><br/> | <span data-ttu-id="4b49e-246">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4b49e-246">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4b49e-247">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="4b49e-247">Namespace</span></span><br/>                | <span data-ttu-id="4b49e-248">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="4b49e-248">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="4b49e-249">MOF</span><span class="sxs-lookup"><span data-stu-id="4b49e-249">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4b49e-250"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4b49e-250"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="4b49e-251">DLL</span><span class="sxs-lookup"><span data-stu-id="4b49e-251">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4b49e-252"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4b49e-252"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4b49e-253">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4b49e-253">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b49e-254">Classi hardware del sistema del computer</span><span class="sxs-lookup"><span data-stu-id="4b49e-254">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="4b49e-255">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="4b49e-255">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="4b49e-256">Attività WMI: rete</span><span class="sxs-lookup"><span data-stu-id="4b49e-256">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="4b49e-257">Attività WMI: account e domini</span><span class="sxs-lookup"><span data-stu-id="4b49e-257">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="4b49e-258">Supporto di IPv6 e IPv4 in WMI</span><span class="sxs-lookup"><span data-stu-id="4b49e-258">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

