---
description: Il metodo statico della classe WMI SetTcpMaxDataRetransmissions viene usato per impostare il numero di volte in cui TCP ritrasmette un singolo segmento di dati prima di interrompere la connessione.
ms.assetid: 1b5407ee-8e2b-4aed-a17a-58d960f976f2
ms.tgt_platform: multiple
title: Metodo SetTcpMaxDataRetransmissions della classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetTcpMaxDataRetransmissions
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 59998888eb2aed170b626fb4cb61780cbe0cb6e4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127730"
---
# <a name="settcpmaxdataretransmissions-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="89cf9-103">Metodo SetTcpMaxDataRetransmissions della \_ classe NetworkAdapterConfiguration Win32</span><span class="sxs-lookup"><span data-stu-id="89cf9-103">SetTcpMaxDataRetransmissions method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="89cf9-104">Il metodo statico della [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetTcpMaxDataRetransmissions** viene usato per impostare il numero di volte in cui TCP ritrasmette un singolo segmento di dati prima di interrompere la connessione.</span><span class="sxs-lookup"><span data-stu-id="89cf9-104">The **SetTcpMaxDataRetransmissions** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to set the number of times TCP retransmits an individual data segment before aborting the connection.</span></span>

<span data-ttu-id="89cf9-105">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="89cf9-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="89cf9-106">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="89cf9-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="89cf9-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="89cf9-107">Syntax</span></span>


```mof
uint32 SetTcpMaxDataRetransmissions(
  [in] uint32 TcpMaxDataRetransmissions
);
```



## <a name="parameters"></a><span data-ttu-id="89cf9-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="89cf9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89cf9-109">*TcpMaxDataRetransmissions* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="89cf9-109">*TcpMaxDataRetransmissions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89cf9-110">Numero di volte in cui TCP ritrasmette un singolo segmento di dati prima di interrompere la connessione.</span><span class="sxs-lookup"><span data-stu-id="89cf9-110">Number of times TCP retransmits an individual data segment before aborting the connection.</span></span> <span data-ttu-id="89cf9-111">Intervallo valido: 0-0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="89cf9-111">Valid range: 0 - 0xFFFFFFFF.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="89cf9-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="89cf9-112">Return value</span></span>

<span data-ttu-id="89cf9-113">Restituisce un valore pari a 0 (zero) per un completamento corretto quando non è richiesto il riavvio, 1 (uno) per un completamento corretto quando è necessario un riavvio e un numero diverso se si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="89cf9-113">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="89cf9-114">Per ulteriori informazioni sui codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="89cf9-114">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="89cf9-115">Per i valori **HRESULT** generali, vedere [codici di errore di sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="89cf9-115">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="89cf9-116">**Operazione completata, non è necessario riavviare il computer**</span><span class="sxs-lookup"><span data-stu-id="89cf9-116">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="89cf9-117">0</span><span class="sxs-lookup"><span data-stu-id="89cf9-117">0</span></span>

<span data-ttu-id="89cf9-118">Operazione completata, non è necessario riavviare il computer.</span><span class="sxs-lookup"><span data-stu-id="89cf9-118">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="89cf9-119">**Operazione completata, riavvio richiesto**</span><span class="sxs-lookup"><span data-stu-id="89cf9-119">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="89cf9-120">1</span><span class="sxs-lookup"><span data-stu-id="89cf9-120">1</span></span>

<span data-ttu-id="89cf9-121">Operazione completata, è necessario riavviare il computer.</span><span class="sxs-lookup"><span data-stu-id="89cf9-121">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="89cf9-122">**Metodo non supportato in questa piattaforma**</span><span class="sxs-lookup"><span data-stu-id="89cf9-122">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="89cf9-123">64</span><span class="sxs-lookup"><span data-stu-id="89cf9-123">64</span></span>

<span data-ttu-id="89cf9-124">Metodo non supportato in questa piattaforma.</span><span class="sxs-lookup"><span data-stu-id="89cf9-124">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="89cf9-125">**Errore sconosciuto**</span><span class="sxs-lookup"><span data-stu-id="89cf9-125">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="89cf9-126">65</span><span class="sxs-lookup"><span data-stu-id="89cf9-126">65</span></span>

<span data-ttu-id="89cf9-127">Errore sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="89cf9-127">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="89cf9-128">**subnet mask non valido**</span><span class="sxs-lookup"><span data-stu-id="89cf9-128">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="89cf9-129">66</span><span class="sxs-lookup"><span data-stu-id="89cf9-129">66</span></span>

<span data-ttu-id="89cf9-130">Subnet mask non valido.</span><span class="sxs-lookup"><span data-stu-id="89cf9-130">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="89cf9-131">**Si è verificato un errore durante l'elaborazione di un'istanza restituita**</span><span class="sxs-lookup"><span data-stu-id="89cf9-131">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="89cf9-132">67</span><span class="sxs-lookup"><span data-stu-id="89cf9-132">67</span></span>

<span data-ttu-id="89cf9-133">Si è verificato un errore durante l'elaborazione di un'istanza di restituita.</span><span class="sxs-lookup"><span data-stu-id="89cf9-133">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="89cf9-134">**Parametro di input non valido**</span><span class="sxs-lookup"><span data-stu-id="89cf9-134">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="89cf9-135">68</span><span class="sxs-lookup"><span data-stu-id="89cf9-135">68</span></span>

<span data-ttu-id="89cf9-136">Parametro di input non valido.</span><span class="sxs-lookup"><span data-stu-id="89cf9-136">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="89cf9-137">**Sono stati specificati più di 5 gateway**</span><span class="sxs-lookup"><span data-stu-id="89cf9-137">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="89cf9-138">69</span><span class="sxs-lookup"><span data-stu-id="89cf9-138">69</span></span>

<span data-ttu-id="89cf9-139">Sono stati specificati più di cinque gateway.</span><span class="sxs-lookup"><span data-stu-id="89cf9-139">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="89cf9-140">**Indirizzo IP non valido**</span><span class="sxs-lookup"><span data-stu-id="89cf9-140">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="89cf9-141">70</span><span class="sxs-lookup"><span data-stu-id="89cf9-141">70</span></span>

<span data-ttu-id="89cf9-142">Indirizzo IP non valido.</span><span class="sxs-lookup"><span data-stu-id="89cf9-142">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="89cf9-143">**Indirizzo IP gateway non valido**</span><span class="sxs-lookup"><span data-stu-id="89cf9-143">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="89cf9-144">71</span><span class="sxs-lookup"><span data-stu-id="89cf9-144">71</span></span>

<span data-ttu-id="89cf9-145">Indirizzo IP del gateway non valido.</span><span class="sxs-lookup"><span data-stu-id="89cf9-145">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="89cf9-146">**Si è verificato un errore durante l'accesso al registro di sistema per le informazioni richieste**</span><span class="sxs-lookup"><span data-stu-id="89cf9-146">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="89cf9-147">72</span><span class="sxs-lookup"><span data-stu-id="89cf9-147">72</span></span>

<span data-ttu-id="89cf9-148">Si è verificato un errore durante l'accesso al registro di sistema per le informazioni richieste.</span><span class="sxs-lookup"><span data-stu-id="89cf9-148">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="89cf9-149">**Nome di dominio non valido**</span><span class="sxs-lookup"><span data-stu-id="89cf9-149">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="89cf9-150">73</span><span class="sxs-lookup"><span data-stu-id="89cf9-150">73</span></span>

<span data-ttu-id="89cf9-151">Nome di dominio non valido.</span><span class="sxs-lookup"><span data-stu-id="89cf9-151">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="89cf9-152">**Nome host non valido**</span><span class="sxs-lookup"><span data-stu-id="89cf9-152">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="89cf9-153">74</span><span class="sxs-lookup"><span data-stu-id="89cf9-153">74</span></span>

<span data-ttu-id="89cf9-154">Nome host non valido.</span><span class="sxs-lookup"><span data-stu-id="89cf9-154">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="89cf9-155">**Nessun server WINS primario/secondario definito**</span><span class="sxs-lookup"><span data-stu-id="89cf9-155">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="89cf9-156">75</span><span class="sxs-lookup"><span data-stu-id="89cf9-156">75</span></span>

<span data-ttu-id="89cf9-157">Nessun server WINS primario o secondario definito.</span><span class="sxs-lookup"><span data-stu-id="89cf9-157">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="89cf9-158">**File non valido**</span><span class="sxs-lookup"><span data-stu-id="89cf9-158">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="89cf9-159">76</span><span class="sxs-lookup"><span data-stu-id="89cf9-159">76</span></span>

<span data-ttu-id="89cf9-160">File non valido.</span><span class="sxs-lookup"><span data-stu-id="89cf9-160">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="89cf9-161">**Percorso di sistema non valido**</span><span class="sxs-lookup"><span data-stu-id="89cf9-161">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="89cf9-162">77</span><span class="sxs-lookup"><span data-stu-id="89cf9-162">77</span></span>

<span data-ttu-id="89cf9-163">Percorso di sistema non valido.</span><span class="sxs-lookup"><span data-stu-id="89cf9-163">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="89cf9-164">**Copia del file non riuscita**</span><span class="sxs-lookup"><span data-stu-id="89cf9-164">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="89cf9-165">78</span><span class="sxs-lookup"><span data-stu-id="89cf9-165">78</span></span>

<span data-ttu-id="89cf9-166">Copia del file non riuscita.</span><span class="sxs-lookup"><span data-stu-id="89cf9-166">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="89cf9-167">**Parametro di sicurezza non valido**</span><span class="sxs-lookup"><span data-stu-id="89cf9-167">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="89cf9-168">79</span><span class="sxs-lookup"><span data-stu-id="89cf9-168">79</span></span>

<span data-ttu-id="89cf9-169">Parametro di sicurezza non valido.</span><span class="sxs-lookup"><span data-stu-id="89cf9-169">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="89cf9-170">**Impossibile configurare il servizio TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="89cf9-170">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="89cf9-171">80</span><span class="sxs-lookup"><span data-stu-id="89cf9-171">80</span></span>

<span data-ttu-id="89cf9-172">Impossibile configurare il servizio TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="89cf9-172">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="89cf9-173">**Non è possibile configurare il servizio DHCP**</span><span class="sxs-lookup"><span data-stu-id="89cf9-173">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="89cf9-174">81</span><span class="sxs-lookup"><span data-stu-id="89cf9-174">81</span></span>

<span data-ttu-id="89cf9-175">Impossibile configurare il servizio DHCP.</span><span class="sxs-lookup"><span data-stu-id="89cf9-175">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="89cf9-176">**Non è possibile rinnovare il lease DHCP**</span><span class="sxs-lookup"><span data-stu-id="89cf9-176">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="89cf9-177">82</span><span class="sxs-lookup"><span data-stu-id="89cf9-177">82</span></span>

<span data-ttu-id="89cf9-178">Non è possibile rinnovare il lease DHCP.</span><span class="sxs-lookup"><span data-stu-id="89cf9-178">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="89cf9-179">**Non è possibile rilasciare il lease DHCP**</span><span class="sxs-lookup"><span data-stu-id="89cf9-179">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="89cf9-180">83</span><span class="sxs-lookup"><span data-stu-id="89cf9-180">83</span></span>

<span data-ttu-id="89cf9-181">Impossibile rilasciare il lease DHCP.</span><span class="sxs-lookup"><span data-stu-id="89cf9-181">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="89cf9-182">**IP non abilitato sulla scheda**</span><span class="sxs-lookup"><span data-stu-id="89cf9-182">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="89cf9-183">84</span><span class="sxs-lookup"><span data-stu-id="89cf9-183">84</span></span>

<span data-ttu-id="89cf9-184">IP non abilitato sulla scheda.</span><span class="sxs-lookup"><span data-stu-id="89cf9-184">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="89cf9-185">**IPX non abilitato sull'adapter**</span><span class="sxs-lookup"><span data-stu-id="89cf9-185">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="89cf9-186">85</span><span class="sxs-lookup"><span data-stu-id="89cf9-186">85</span></span>

<span data-ttu-id="89cf9-187">IPX non abilitato sulla scheda.</span><span class="sxs-lookup"><span data-stu-id="89cf9-187">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="89cf9-188">**Errore limite numero frame/rete**</span><span class="sxs-lookup"><span data-stu-id="89cf9-188">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="89cf9-189">86</span><span class="sxs-lookup"><span data-stu-id="89cf9-189">86</span></span>

<span data-ttu-id="89cf9-190">Errore dei limiti del numero di rete o del frame.</span><span class="sxs-lookup"><span data-stu-id="89cf9-190">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="89cf9-191">**Tipo di frame non valido**</span><span class="sxs-lookup"><span data-stu-id="89cf9-191">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="89cf9-192">87</span><span class="sxs-lookup"><span data-stu-id="89cf9-192">87</span></span>

<span data-ttu-id="89cf9-193">Tipo di frame non valido.</span><span class="sxs-lookup"><span data-stu-id="89cf9-193">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="89cf9-194">**Numero di rete non valido**</span><span class="sxs-lookup"><span data-stu-id="89cf9-194">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="89cf9-195">88</span><span class="sxs-lookup"><span data-stu-id="89cf9-195">88</span></span>

<span data-ttu-id="89cf9-196">Numero di rete non valido.</span><span class="sxs-lookup"><span data-stu-id="89cf9-196">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="89cf9-197">**Numero di rete duplicato**</span><span class="sxs-lookup"><span data-stu-id="89cf9-197">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="89cf9-198">89</span><span class="sxs-lookup"><span data-stu-id="89cf9-198">89</span></span>

<span data-ttu-id="89cf9-199">Numero di rete duplicato.</span><span class="sxs-lookup"><span data-stu-id="89cf9-199">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="89cf9-200">**Parametro fuori limite**</span><span class="sxs-lookup"><span data-stu-id="89cf9-200">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="89cf9-201">90</span><span class="sxs-lookup"><span data-stu-id="89cf9-201">90</span></span>

<span data-ttu-id="89cf9-202">Parametro fuori limite.</span><span class="sxs-lookup"><span data-stu-id="89cf9-202">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="89cf9-203">**Accesso negato**</span><span class="sxs-lookup"><span data-stu-id="89cf9-203">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="89cf9-204">91</span><span class="sxs-lookup"><span data-stu-id="89cf9-204">91</span></span>

<span data-ttu-id="89cf9-205">Accesso negato.</span><span class="sxs-lookup"><span data-stu-id="89cf9-205">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="89cf9-206">**Memoria insufficiente**</span><span class="sxs-lookup"><span data-stu-id="89cf9-206">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="89cf9-207">92</span><span class="sxs-lookup"><span data-stu-id="89cf9-207">92</span></span>

<span data-ttu-id="89cf9-208">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="89cf9-208">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="89cf9-209">**Esiste già**</span><span class="sxs-lookup"><span data-stu-id="89cf9-209">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="89cf9-210">93</span><span class="sxs-lookup"><span data-stu-id="89cf9-210">93</span></span>

<span data-ttu-id="89cf9-211">Esiste già.</span><span class="sxs-lookup"><span data-stu-id="89cf9-211">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="89cf9-212">**Percorso, file o oggetto non trovato**</span><span class="sxs-lookup"><span data-stu-id="89cf9-212">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="89cf9-213">94</span><span class="sxs-lookup"><span data-stu-id="89cf9-213">94</span></span>

<span data-ttu-id="89cf9-214">Il percorso, il file o l'oggetto non è stato trovato.</span><span class="sxs-lookup"><span data-stu-id="89cf9-214">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="89cf9-215">**Non è possibile inviare una notifica al servizio**</span><span class="sxs-lookup"><span data-stu-id="89cf9-215">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="89cf9-216">95</span><span class="sxs-lookup"><span data-stu-id="89cf9-216">95</span></span>

<span data-ttu-id="89cf9-217">Impossibile notificare il servizio.</span><span class="sxs-lookup"><span data-stu-id="89cf9-217">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="89cf9-218">**Non è possibile inviare una notifica al servizio DNS**</span><span class="sxs-lookup"><span data-stu-id="89cf9-218">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="89cf9-219">96</span><span class="sxs-lookup"><span data-stu-id="89cf9-219">96</span></span>

<span data-ttu-id="89cf9-220">Impossibile inviare una notifica al servizio DNS.</span><span class="sxs-lookup"><span data-stu-id="89cf9-220">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="89cf9-221">**Interfaccia non configurabile**</span><span class="sxs-lookup"><span data-stu-id="89cf9-221">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="89cf9-222">97</span><span class="sxs-lookup"><span data-stu-id="89cf9-222">97</span></span>

<span data-ttu-id="89cf9-223">Interfaccia non configurabile.</span><span class="sxs-lookup"><span data-stu-id="89cf9-223">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="89cf9-224">**Non tutti i lease DHCP possono essere rilasciati/rinnovati**</span><span class="sxs-lookup"><span data-stu-id="89cf9-224">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="89cf9-225">98</span><span class="sxs-lookup"><span data-stu-id="89cf9-225">98</span></span>

<span data-ttu-id="89cf9-226">Non tutti i lease DHCP possono essere rilasciati o rinnovati.</span><span class="sxs-lookup"><span data-stu-id="89cf9-226">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="89cf9-227">**DHCP non abilitato sull'adapter**</span><span class="sxs-lookup"><span data-stu-id="89cf9-227">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="89cf9-228">100</span><span class="sxs-lookup"><span data-stu-id="89cf9-228">100</span></span>

<span data-ttu-id="89cf9-229">DHCP non abilitato sulla scheda.</span><span class="sxs-lookup"><span data-stu-id="89cf9-229">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="89cf9-230">**Altri**</span><span class="sxs-lookup"><span data-stu-id="89cf9-230">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="89cf9-231">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="89cf9-231">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="89cf9-232">Commenti</span><span class="sxs-lookup"><span data-stu-id="89cf9-232">Remarks</span></span>

<span data-ttu-id="89cf9-233">Il timeout di ritrasmissione raddoppia con ogni ritrasmissione successiva in una connessione.</span><span class="sxs-lookup"><span data-stu-id="89cf9-233">The retransmission timeout doubles with each successive retransmission on a connection.</span></span>

## <a name="examples"></a><span data-ttu-id="89cf9-234">Esempio</span><span class="sxs-lookup"><span data-stu-id="89cf9-234">Examples</span></span>

<span data-ttu-id="89cf9-235">L'esempio relativo alla [modifica del numero massimo consentito di ritrasmissioni dati TCP](https://Gallery.TechNet.Microsoft.Com/8a581692-7950-412e-bd28-74f223b27827) consente di configurare il numero di tentativi di ritrasmissione di un singolo segmento di dati da parte di TCP prima di abbandonare il lavoro richiesto.</span><span class="sxs-lookup"><span data-stu-id="89cf9-235">The [Modify the Maximum Allowed TCP Data Retransmissions](https://Gallery.TechNet.Microsoft.Com/8a581692-7950-412e-bd28-74f223b27827) VBScript sample configures the number of times TCP will attempt to retransmit an individual data segment before abandoning the effort.</span></span>

## <a name="requirements"></a><span data-ttu-id="89cf9-236">Requisiti</span><span class="sxs-lookup"><span data-stu-id="89cf9-236">Requirements</span></span>



| <span data-ttu-id="89cf9-237">Requisito</span><span class="sxs-lookup"><span data-stu-id="89cf9-237">Requirement</span></span> | <span data-ttu-id="89cf9-238">Valore</span><span class="sxs-lookup"><span data-stu-id="89cf9-238">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="89cf9-239">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="89cf9-239">Minimum supported client</span></span><br/> | <span data-ttu-id="89cf9-240">Windows Vista, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="89cf9-240">Windows Vista, Windows Vista</span></span><br/>                                                 |
| <span data-ttu-id="89cf9-241">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="89cf9-241">Minimum supported server</span></span><br/> | <span data-ttu-id="89cf9-242">Windows Server 2008, Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="89cf9-242">Windows Server 2008, Windows Server 2008</span></span><br/>                                     |
| <span data-ttu-id="89cf9-243">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="89cf9-243">Namespace</span></span><br/>                | <span data-ttu-id="89cf9-244">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="89cf9-244">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="89cf9-245">MOF</span><span class="sxs-lookup"><span data-stu-id="89cf9-245">MOF</span></span><br/>                      | <dl> <span data-ttu-id="89cf9-246"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="89cf9-246"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="89cf9-247">DLL</span><span class="sxs-lookup"><span data-stu-id="89cf9-247">DLL</span></span><br/>                      | <dl> <span data-ttu-id="89cf9-248"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="89cf9-248"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="89cf9-249">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="89cf9-249">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89cf9-250">Classi hardware del sistema del computer</span><span class="sxs-lookup"><span data-stu-id="89cf9-250">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="89cf9-251">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="89cf9-251">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="89cf9-252">Attività WMI: rete</span><span class="sxs-lookup"><span data-stu-id="89cf9-252">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="89cf9-253">Attività WMI: account e domini</span><span class="sxs-lookup"><span data-stu-id="89cf9-253">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="89cf9-254">Supporto di IPv6 e IPv4 in WMI</span><span class="sxs-lookup"><span data-stu-id="89cf9-254">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

