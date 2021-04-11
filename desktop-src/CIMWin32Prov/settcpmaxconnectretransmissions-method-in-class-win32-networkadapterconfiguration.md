---
description: Il metodo statico della classe WMI SetTcpMaxConnectRetransmissions viene usato per impostare il numero di tentativi che TCP ritrasmetterà una richiesta di connessione prima di interrompersi.
ms.assetid: cb0dfba3-4ef5-4052-94f3-f688a1c55d90
ms.tgt_platform: multiple
title: Metodo SetTcpMaxConnectRetransmissions della classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetTcpMaxConnectRetransmissions
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 160d84c2a466bff34070a6dec4a34804d5a3a7fc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127731"
---
# <a name="settcpmaxconnectretransmissions-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="0f5ba-103">Metodo SetTcpMaxConnectRetransmissions della \_ classe NetworkAdapterConfiguration Win32</span><span class="sxs-lookup"><span data-stu-id="0f5ba-103">SetTcpMaxConnectRetransmissions method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="0f5ba-104">Il metodo statico della [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetTcpMaxConnectRetransmissions** viene usato per impostare il numero di tentativi che TCP ritrasmetterà una richiesta di connessione prima di interrompersi.</span><span class="sxs-lookup"><span data-stu-id="0f5ba-104">The **SetTcpMaxConnectRetransmissions** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to set the number of attempts TCP will retransmit a connect request before aborting.</span></span>

<span data-ttu-id="0f5ba-105">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="0f5ba-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="0f5ba-106">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="0f5ba-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="0f5ba-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0f5ba-107">Syntax</span></span>


```mof
uint32 SetTcpMaxConnectRetransmissions(
  [in] uint32 TcpMaxConnectRetransmissions
);
```



## <a name="parameters"></a><span data-ttu-id="0f5ba-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="0f5ba-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f5ba-109">*TcpMaxConnectRetransmissions* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0f5ba-109">*TcpMaxConnectRetransmissions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0f5ba-110">Il numero di tentativi TCP ritrasmette una richiesta di connessione prima dell'interruzione.</span><span class="sxs-lookup"><span data-stu-id="0f5ba-110">Number of attempts TCP will retransmit a connect request before aborting.</span></span> <span data-ttu-id="0f5ba-111">L'intervallo valido per i valori è 0-0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="0f5ba-111">The valid range for values is 0 - 0xFFFFFFFF.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f5ba-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0f5ba-112">Return value</span></span>

<span data-ttu-id="0f5ba-113">Restituisce un valore pari a 0 (zero) per un completamento corretto quando non è richiesto il riavvio, 1 (uno) per un completamento corretto quando è necessario un riavvio e un numero diverso se si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="0f5ba-113">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="0f5ba-114">Per ulteriori informazioni sui codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="0f5ba-114">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="0f5ba-115">Per i valori **HRESULT** generali, vedere [codici di errore di sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="0f5ba-115">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="0f5ba-116">**Operazione completata, non è necessario riavviare il computer**</span><span class="sxs-lookup"><span data-stu-id="0f5ba-116">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="0f5ba-117">0</span><span class="sxs-lookup"><span data-stu-id="0f5ba-117">0</span></span>

<span data-ttu-id="0f5ba-118">Operazione completata, non è necessario riavviare il computer.</span><span class="sxs-lookup"><span data-stu-id="0f5ba-118">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="0f5ba-119">**Operazione completata, riavvio richiesto**</span><span class="sxs-lookup"><span data-stu-id="0f5ba-119">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="0f5ba-120">1</span><span class="sxs-lookup"><span data-stu-id="0f5ba-120">1</span></span>

<span data-ttu-id="0f5ba-121">Operazione completata, è necessario riavviare il computer.</span><span class="sxs-lookup"><span data-stu-id="0f5ba-121">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="0f5ba-122">**Metodo non supportato in questa piattaforma**</span><span class="sxs-lookup"><span data-stu-id="0f5ba-122">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="0f5ba-123">64</span><span class="sxs-lookup"><span data-stu-id="0f5ba-123">64</span></span>

<span data-ttu-id="0f5ba-124">Metodo non supportato in questa piattaforma.</span><span class="sxs-lookup"><span data-stu-id="0f5ba-124">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="0f5ba-125">**Errore sconosciuto**</span><span class="sxs-lookup"><span data-stu-id="0f5ba-125">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="0f5ba-126">65</span><span class="sxs-lookup"><span data-stu-id="0f5ba-126">65</span></span>

<span data-ttu-id="0f5ba-127">Errore sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="0f5ba-127">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="0f5ba-128">**subnet mask non valido**</span><span class="sxs-lookup"><span data-stu-id="0f5ba-128">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="0f5ba-129">66</span><span class="sxs-lookup"><span data-stu-id="0f5ba-129">66</span></span>

<span data-ttu-id="0f5ba-130">Subnet mask non valido.</span><span class="sxs-lookup"><span data-stu-id="0f5ba-130">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="0f5ba-131">**Si è verificato un errore durante l'elaborazione di un'istanza restituita**</span><span class="sxs-lookup"><span data-stu-id="0f5ba-131">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="0f5ba-132">67</span><span class="sxs-lookup"><span data-stu-id="0f5ba-132">67</span></span>

<span data-ttu-id="0f5ba-133">Si è verificato un errore durante l'elaborazione di un'istanza di restituita.</span><span class="sxs-lookup"><span data-stu-id="0f5ba-133">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="0f5ba-134">**Parametro di input non valido**</span><span class="sxs-lookup"><span data-stu-id="0f5ba-134">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="0f5ba-135">68</span><span class="sxs-lookup"><span data-stu-id="0f5ba-135">68</span></span>

<span data-ttu-id="0f5ba-136">Parametro di input non valido.</span><span class="sxs-lookup"><span data-stu-id="0f5ba-136">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="0f5ba-137">**Sono stati specificati più di 5 gateway**</span><span class="sxs-lookup"><span data-stu-id="0f5ba-137">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="0f5ba-138">69</span><span class="sxs-lookup"><span data-stu-id="0f5ba-138">69</span></span>

<span data-ttu-id="0f5ba-139">Sono stati specificati più di cinque gateway.</span><span class="sxs-lookup"><span data-stu-id="0f5ba-139">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="0f5ba-140">**Indirizzo IP non valido**</span><span class="sxs-lookup"><span data-stu-id="0f5ba-140">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="0f5ba-141">70</span><span class="sxs-lookup"><span data-stu-id="0f5ba-141">70</span></span>

<span data-ttu-id="0f5ba-142">Indirizzo IP non valido.</span><span class="sxs-lookup"><span data-stu-id="0f5ba-142">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="0f5ba-143">**Indirizzo IP gateway non valido**</span><span class="sxs-lookup"><span data-stu-id="0f5ba-143">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="0f5ba-144">71</span><span class="sxs-lookup"><span data-stu-id="0f5ba-144">71</span></span>

<span data-ttu-id="0f5ba-145">Indirizzo IP del gateway non valido.</span><span class="sxs-lookup"><span data-stu-id="0f5ba-145">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="0f5ba-146">**Si è verificato un errore durante l'accesso al registro di sistema per le informazioni richieste**</span><span class="sxs-lookup"><span data-stu-id="0f5ba-146">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="0f5ba-147">72</span><span class="sxs-lookup"><span data-stu-id="0f5ba-147">72</span></span>

<span data-ttu-id="0f5ba-148">Si è verificato un errore durante l'accesso al registro di sistema per le informazioni richieste.</span><span class="sxs-lookup"><span data-stu-id="0f5ba-148">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="0f5ba-149">**Nome di dominio non valido**</span><span class="sxs-lookup"><span data-stu-id="0f5ba-149">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="0f5ba-150">73</span><span class="sxs-lookup"><span data-stu-id="0f5ba-150">73</span></span>

<span data-ttu-id="0f5ba-151">Nome di dominio non valido.</span><span class="sxs-lookup"><span data-stu-id="0f5ba-151">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="0f5ba-152">**Nome host non valido**</span><span class="sxs-lookup"><span data-stu-id="0f5ba-152">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="0f5ba-153">74</span><span class="sxs-lookup"><span data-stu-id="0f5ba-153">74</span></span>

<span data-ttu-id="0f5ba-154">Nome host non valido.</span><span class="sxs-lookup"><span data-stu-id="0f5ba-154">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="0f5ba-155">**Nessun server WINS primario/secondario definito**</span><span class="sxs-lookup"><span data-stu-id="0f5ba-155">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="0f5ba-156">75</span><span class="sxs-lookup"><span data-stu-id="0f5ba-156">75</span></span>

<span data-ttu-id="0f5ba-157">Nessun server WINS primario o secondario definito.</span><span class="sxs-lookup"><span data-stu-id="0f5ba-157">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="0f5ba-158">**File non valido**</span><span class="sxs-lookup"><span data-stu-id="0f5ba-158">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="0f5ba-159">76</span><span class="sxs-lookup"><span data-stu-id="0f5ba-159">76</span></span>

<span data-ttu-id="0f5ba-160">File non valido.</span><span class="sxs-lookup"><span data-stu-id="0f5ba-160">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="0f5ba-161">**Percorso di sistema non valido**</span><span class="sxs-lookup"><span data-stu-id="0f5ba-161">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="0f5ba-162">77</span><span class="sxs-lookup"><span data-stu-id="0f5ba-162">77</span></span>

<span data-ttu-id="0f5ba-163">Percorso di sistema non valido.</span><span class="sxs-lookup"><span data-stu-id="0f5ba-163">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="0f5ba-164">**Copia del file non riuscita**</span><span class="sxs-lookup"><span data-stu-id="0f5ba-164">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="0f5ba-165">78</span><span class="sxs-lookup"><span data-stu-id="0f5ba-165">78</span></span>

<span data-ttu-id="0f5ba-166">Copia del file non riuscita.</span><span class="sxs-lookup"><span data-stu-id="0f5ba-166">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="0f5ba-167">**Parametro di sicurezza non valido**</span><span class="sxs-lookup"><span data-stu-id="0f5ba-167">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="0f5ba-168">79</span><span class="sxs-lookup"><span data-stu-id="0f5ba-168">79</span></span>

<span data-ttu-id="0f5ba-169">Parametro di sicurezza non valido.</span><span class="sxs-lookup"><span data-stu-id="0f5ba-169">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="0f5ba-170">**Impossibile configurare il servizio TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="0f5ba-170">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="0f5ba-171">80</span><span class="sxs-lookup"><span data-stu-id="0f5ba-171">80</span></span>

<span data-ttu-id="0f5ba-172">Impossibile configurare il servizio TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="0f5ba-172">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="0f5ba-173">**Non è possibile configurare il servizio DHCP**</span><span class="sxs-lookup"><span data-stu-id="0f5ba-173">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="0f5ba-174">81</span><span class="sxs-lookup"><span data-stu-id="0f5ba-174">81</span></span>

<span data-ttu-id="0f5ba-175">Impossibile configurare il servizio DHCP.</span><span class="sxs-lookup"><span data-stu-id="0f5ba-175">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="0f5ba-176">**Non è possibile rinnovare il lease DHCP**</span><span class="sxs-lookup"><span data-stu-id="0f5ba-176">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="0f5ba-177">82</span><span class="sxs-lookup"><span data-stu-id="0f5ba-177">82</span></span>

<span data-ttu-id="0f5ba-178">Non è possibile rinnovare il lease DHCP.</span><span class="sxs-lookup"><span data-stu-id="0f5ba-178">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="0f5ba-179">**Non è possibile rilasciare il lease DHCP**</span><span class="sxs-lookup"><span data-stu-id="0f5ba-179">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="0f5ba-180">83</span><span class="sxs-lookup"><span data-stu-id="0f5ba-180">83</span></span>

<span data-ttu-id="0f5ba-181">Impossibile rilasciare il lease DHCP.</span><span class="sxs-lookup"><span data-stu-id="0f5ba-181">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="0f5ba-182">**IP non abilitato sulla scheda**</span><span class="sxs-lookup"><span data-stu-id="0f5ba-182">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="0f5ba-183">84</span><span class="sxs-lookup"><span data-stu-id="0f5ba-183">84</span></span>

<span data-ttu-id="0f5ba-184">IP non abilitato sulla scheda.</span><span class="sxs-lookup"><span data-stu-id="0f5ba-184">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="0f5ba-185">**IPX non abilitato sull'adapter**</span><span class="sxs-lookup"><span data-stu-id="0f5ba-185">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="0f5ba-186">85</span><span class="sxs-lookup"><span data-stu-id="0f5ba-186">85</span></span>

<span data-ttu-id="0f5ba-187">IPX non abilitato sulla scheda.</span><span class="sxs-lookup"><span data-stu-id="0f5ba-187">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="0f5ba-188">**Errore limite numero frame/rete**</span><span class="sxs-lookup"><span data-stu-id="0f5ba-188">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="0f5ba-189">86</span><span class="sxs-lookup"><span data-stu-id="0f5ba-189">86</span></span>

<span data-ttu-id="0f5ba-190">Errore dei limiti del numero di rete o del frame.</span><span class="sxs-lookup"><span data-stu-id="0f5ba-190">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="0f5ba-191">**Tipo di frame non valido**</span><span class="sxs-lookup"><span data-stu-id="0f5ba-191">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="0f5ba-192">87</span><span class="sxs-lookup"><span data-stu-id="0f5ba-192">87</span></span>

<span data-ttu-id="0f5ba-193">Tipo di frame non valido.</span><span class="sxs-lookup"><span data-stu-id="0f5ba-193">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="0f5ba-194">**Numero di rete non valido**</span><span class="sxs-lookup"><span data-stu-id="0f5ba-194">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="0f5ba-195">88</span><span class="sxs-lookup"><span data-stu-id="0f5ba-195">88</span></span>

<span data-ttu-id="0f5ba-196">Numero di rete non valido.</span><span class="sxs-lookup"><span data-stu-id="0f5ba-196">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="0f5ba-197">**Numero di rete duplicato**</span><span class="sxs-lookup"><span data-stu-id="0f5ba-197">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="0f5ba-198">89</span><span class="sxs-lookup"><span data-stu-id="0f5ba-198">89</span></span>

<span data-ttu-id="0f5ba-199">Numero di rete duplicato.</span><span class="sxs-lookup"><span data-stu-id="0f5ba-199">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="0f5ba-200">**Parametro fuori limite**</span><span class="sxs-lookup"><span data-stu-id="0f5ba-200">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="0f5ba-201">90</span><span class="sxs-lookup"><span data-stu-id="0f5ba-201">90</span></span>

<span data-ttu-id="0f5ba-202">Parametro fuori limite.</span><span class="sxs-lookup"><span data-stu-id="0f5ba-202">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="0f5ba-203">**Accesso negato**</span><span class="sxs-lookup"><span data-stu-id="0f5ba-203">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="0f5ba-204">91</span><span class="sxs-lookup"><span data-stu-id="0f5ba-204">91</span></span>

<span data-ttu-id="0f5ba-205">Accesso negato.</span><span class="sxs-lookup"><span data-stu-id="0f5ba-205">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="0f5ba-206">**Memoria insufficiente**</span><span class="sxs-lookup"><span data-stu-id="0f5ba-206">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="0f5ba-207">92</span><span class="sxs-lookup"><span data-stu-id="0f5ba-207">92</span></span>

<span data-ttu-id="0f5ba-208">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="0f5ba-208">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="0f5ba-209">**Esiste già**</span><span class="sxs-lookup"><span data-stu-id="0f5ba-209">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="0f5ba-210">93</span><span class="sxs-lookup"><span data-stu-id="0f5ba-210">93</span></span>

<span data-ttu-id="0f5ba-211">Esiste già.</span><span class="sxs-lookup"><span data-stu-id="0f5ba-211">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="0f5ba-212">**Percorso, file o oggetto non trovato**</span><span class="sxs-lookup"><span data-stu-id="0f5ba-212">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="0f5ba-213">94</span><span class="sxs-lookup"><span data-stu-id="0f5ba-213">94</span></span>

<span data-ttu-id="0f5ba-214">Il percorso, il file o l'oggetto non è stato trovato.</span><span class="sxs-lookup"><span data-stu-id="0f5ba-214">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="0f5ba-215">**Non è possibile inviare una notifica al servizio**</span><span class="sxs-lookup"><span data-stu-id="0f5ba-215">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="0f5ba-216">95</span><span class="sxs-lookup"><span data-stu-id="0f5ba-216">95</span></span>

<span data-ttu-id="0f5ba-217">Impossibile notificare il servizio.</span><span class="sxs-lookup"><span data-stu-id="0f5ba-217">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="0f5ba-218">**Non è possibile inviare una notifica al servizio DNS**</span><span class="sxs-lookup"><span data-stu-id="0f5ba-218">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="0f5ba-219">96</span><span class="sxs-lookup"><span data-stu-id="0f5ba-219">96</span></span>

<span data-ttu-id="0f5ba-220">Impossibile inviare una notifica al servizio DNS.</span><span class="sxs-lookup"><span data-stu-id="0f5ba-220">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="0f5ba-221">**Interfaccia non configurabile**</span><span class="sxs-lookup"><span data-stu-id="0f5ba-221">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="0f5ba-222">97</span><span class="sxs-lookup"><span data-stu-id="0f5ba-222">97</span></span>

<span data-ttu-id="0f5ba-223">Interfaccia non configurabile.</span><span class="sxs-lookup"><span data-stu-id="0f5ba-223">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="0f5ba-224">**Non tutti i lease DHCP possono essere rilasciati/rinnovati**</span><span class="sxs-lookup"><span data-stu-id="0f5ba-224">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="0f5ba-225">98</span><span class="sxs-lookup"><span data-stu-id="0f5ba-225">98</span></span>

<span data-ttu-id="0f5ba-226">Non tutti i lease DHCP possono essere rilasciati o rinnovati.</span><span class="sxs-lookup"><span data-stu-id="0f5ba-226">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="0f5ba-227">**DHCP non abilitato sull'adapter**</span><span class="sxs-lookup"><span data-stu-id="0f5ba-227">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="0f5ba-228">100</span><span class="sxs-lookup"><span data-stu-id="0f5ba-228">100</span></span>

<span data-ttu-id="0f5ba-229">DHCP non abilitato sulla scheda.</span><span class="sxs-lookup"><span data-stu-id="0f5ba-229">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="0f5ba-230">**Altri**</span><span class="sxs-lookup"><span data-stu-id="0f5ba-230">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="0f5ba-231">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="0f5ba-231">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0f5ba-232">Commenti</span><span class="sxs-lookup"><span data-stu-id="0f5ba-232">Remarks</span></span>

<span data-ttu-id="0f5ba-233">Il timeout di ritrasmissione iniziale è di tre secondi e raddoppia per ogni tentativo successivo.</span><span class="sxs-lookup"><span data-stu-id="0f5ba-233">The initial retransmission timeout is three seconds, and doubles for each successive attempt.</span></span>

## <a name="examples"></a><span data-ttu-id="0f5ba-234">Esempio</span><span class="sxs-lookup"><span data-stu-id="0f5ba-234">Examples</span></span>

<span data-ttu-id="0f5ba-235">L'esempio che consente di [modificare il numero massimo consentito di ritrasmissioni di connessioni TCP](https://Gallery.TechNet.Microsoft.Com/e599c6bc-fa37-457d-b7e3-3c003517ed46) consente di configurare il numero di volte in cui TCP ritrasmette un tentativo di connessione prima di abbandonare il lavoro richiesto.</span><span class="sxs-lookup"><span data-stu-id="0f5ba-235">The [Modify the Maximum Allowed TCP Connection Retransmissions](https://Gallery.TechNet.Microsoft.Com/e599c6bc-fa37-457d-b7e3-3c003517ed46) VBScript sample configures the number of times TCP will retransmit a connection attempt before abandoning the effort.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f5ba-236">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0f5ba-236">Requirements</span></span>



| <span data-ttu-id="0f5ba-237">Requisito</span><span class="sxs-lookup"><span data-stu-id="0f5ba-237">Requirement</span></span> | <span data-ttu-id="0f5ba-238">Valore</span><span class="sxs-lookup"><span data-stu-id="0f5ba-238">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0f5ba-239">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0f5ba-239">Minimum supported client</span></span><br/> | <span data-ttu-id="0f5ba-240">Windows Vista, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0f5ba-240">Windows Vista, Windows Vista</span></span><br/>                                                 |
| <span data-ttu-id="0f5ba-241">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0f5ba-241">Minimum supported server</span></span><br/> | <span data-ttu-id="0f5ba-242">Windows Server 2008, Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0f5ba-242">Windows Server 2008, Windows Server 2008</span></span><br/>                                     |
| <span data-ttu-id="0f5ba-243">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="0f5ba-243">Namespace</span></span><br/>                | <span data-ttu-id="0f5ba-244">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="0f5ba-244">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0f5ba-245">MOF</span><span class="sxs-lookup"><span data-stu-id="0f5ba-245">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0f5ba-246"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0f5ba-246"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0f5ba-247">DLL</span><span class="sxs-lookup"><span data-stu-id="0f5ba-247">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0f5ba-248"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0f5ba-248"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f5ba-249">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0f5ba-249">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f5ba-250">Classi hardware del sistema del computer</span><span class="sxs-lookup"><span data-stu-id="0f5ba-250">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="0f5ba-251">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="0f5ba-251">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="0f5ba-252">Attività WMI: rete</span><span class="sxs-lookup"><span data-stu-id="0f5ba-252">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="0f5ba-253">Attività WMI: account e domini</span><span class="sxs-lookup"><span data-stu-id="0f5ba-253">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="0f5ba-254">Supporto di IPv6 e IPv4 in WMI</span><span class="sxs-lookup"><span data-stu-id="0f5ba-254">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

