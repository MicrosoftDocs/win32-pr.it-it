---
description: Il metodo statico della classe WMI SetTcpNumConnections viene usato per impostare il numero massimo di connessioni che TCP può aprire contemporaneamente.
ms.assetid: 50458161-1f28-47f9-b395-09586e859d5d
ms.tgt_platform: multiple
title: Metodo SetTcpNumConnections della classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetTcpNumConnections
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5708c7ce80930c0924b560cc7b84e5af45ad7962
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126858"
---
# <a name="settcpnumconnections-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="2e794-103">Metodo SetTcpNumConnections della \_ classe NetworkAdapterConfiguration Win32</span><span class="sxs-lookup"><span data-stu-id="2e794-103">SetTcpNumConnections method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="2e794-104">Il metodo statico della [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetTcpNumConnections** viene usato per impostare il numero massimo di connessioni che TCP può aprire contemporaneamente.</span><span class="sxs-lookup"><span data-stu-id="2e794-104">The **SetTcpNumConnections** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to set the maximum number of connections that TCP may have open simultaneously.</span></span>

<span data-ttu-id="2e794-105">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="2e794-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="2e794-106">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="2e794-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="2e794-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2e794-107">Syntax</span></span>


```mof
uint32 SetTcpNumConnections(
  [in] uint32 TcpNumConnections
);
```



## <a name="parameters"></a><span data-ttu-id="2e794-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="2e794-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e794-109">*TcpNumConnections* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2e794-109">*TcpNumConnections* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e794-110">Numero massimo di connessioni che TCP potrebbe avere aperto simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="2e794-110">Maximum number of connections that TCP may have open simultaneously.</span></span> <span data-ttu-id="2e794-111">L'intervallo valido di valori è 0-0xFFFFFE.</span><span class="sxs-lookup"><span data-stu-id="2e794-111">The valid range of values is 0 - 0xFFFFFE.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e794-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2e794-112">Return value</span></span>

<span data-ttu-id="2e794-113">Restituisce un valore pari a 0 (zero) per un completamento corretto quando non è richiesto il riavvio, 1 (uno) per un completamento corretto quando è necessario un riavvio e un numero diverso se si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="2e794-113">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="2e794-114">Per ulteriori informazioni sui codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="2e794-114">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="2e794-115">Per i valori **HRESULT** generali, vedere [codici di errore di sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="2e794-115">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="2e794-116">**Operazione completata, non è necessario riavviare il computer**</span><span class="sxs-lookup"><span data-stu-id="2e794-116">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="2e794-117">0</span><span class="sxs-lookup"><span data-stu-id="2e794-117">0</span></span>

<span data-ttu-id="2e794-118">Operazione completata, non è necessario riavviare il computer.</span><span class="sxs-lookup"><span data-stu-id="2e794-118">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="2e794-119">**Operazione completata, riavvio richiesto**</span><span class="sxs-lookup"><span data-stu-id="2e794-119">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="2e794-120">1</span><span class="sxs-lookup"><span data-stu-id="2e794-120">1</span></span>

<span data-ttu-id="2e794-121">Operazione completata, è necessario riavviare il computer.</span><span class="sxs-lookup"><span data-stu-id="2e794-121">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="2e794-122">**Metodo non supportato in questa piattaforma**</span><span class="sxs-lookup"><span data-stu-id="2e794-122">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="2e794-123">64</span><span class="sxs-lookup"><span data-stu-id="2e794-123">64</span></span>

<span data-ttu-id="2e794-124">Metodo non supportato in questa piattaforma.</span><span class="sxs-lookup"><span data-stu-id="2e794-124">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="2e794-125">**Errore sconosciuto**</span><span class="sxs-lookup"><span data-stu-id="2e794-125">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="2e794-126">65</span><span class="sxs-lookup"><span data-stu-id="2e794-126">65</span></span>

<span data-ttu-id="2e794-127">Errore sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="2e794-127">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="2e794-128">**subnet mask non valido**</span><span class="sxs-lookup"><span data-stu-id="2e794-128">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="2e794-129">66</span><span class="sxs-lookup"><span data-stu-id="2e794-129">66</span></span>

<span data-ttu-id="2e794-130">Subnet mask non valido.</span><span class="sxs-lookup"><span data-stu-id="2e794-130">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="2e794-131">**Si è verificato un errore durante l'elaborazione di un'istanza restituita**</span><span class="sxs-lookup"><span data-stu-id="2e794-131">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="2e794-132">67</span><span class="sxs-lookup"><span data-stu-id="2e794-132">67</span></span>

<span data-ttu-id="2e794-133">Si è verificato un errore durante l'elaborazione di un'istanza di restituita.</span><span class="sxs-lookup"><span data-stu-id="2e794-133">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="2e794-134">**Parametro di input non valido**</span><span class="sxs-lookup"><span data-stu-id="2e794-134">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="2e794-135">68</span><span class="sxs-lookup"><span data-stu-id="2e794-135">68</span></span>

<span data-ttu-id="2e794-136">Parametro di input non valido.</span><span class="sxs-lookup"><span data-stu-id="2e794-136">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="2e794-137">**Sono stati specificati più di 5 gateway**</span><span class="sxs-lookup"><span data-stu-id="2e794-137">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="2e794-138">69</span><span class="sxs-lookup"><span data-stu-id="2e794-138">69</span></span>

<span data-ttu-id="2e794-139">Sono stati specificati più di cinque gateway.</span><span class="sxs-lookup"><span data-stu-id="2e794-139">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="2e794-140">**Indirizzo IP non valido**</span><span class="sxs-lookup"><span data-stu-id="2e794-140">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="2e794-141">70</span><span class="sxs-lookup"><span data-stu-id="2e794-141">70</span></span>

<span data-ttu-id="2e794-142">Indirizzo IP non valido.</span><span class="sxs-lookup"><span data-stu-id="2e794-142">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="2e794-143">**Indirizzo IP gateway non valido**</span><span class="sxs-lookup"><span data-stu-id="2e794-143">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="2e794-144">71</span><span class="sxs-lookup"><span data-stu-id="2e794-144">71</span></span>

<span data-ttu-id="2e794-145">Indirizzo IP del gateway non valido.</span><span class="sxs-lookup"><span data-stu-id="2e794-145">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="2e794-146">**Si è verificato un errore durante l'accesso al registro di sistema per le informazioni richieste**</span><span class="sxs-lookup"><span data-stu-id="2e794-146">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="2e794-147">72</span><span class="sxs-lookup"><span data-stu-id="2e794-147">72</span></span>

<span data-ttu-id="2e794-148">Si è verificato un errore durante l'accesso al registro di sistema per le informazioni richieste.</span><span class="sxs-lookup"><span data-stu-id="2e794-148">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="2e794-149">**Nome di dominio non valido**</span><span class="sxs-lookup"><span data-stu-id="2e794-149">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="2e794-150">73</span><span class="sxs-lookup"><span data-stu-id="2e794-150">73</span></span>

<span data-ttu-id="2e794-151">Nome di dominio non valido.</span><span class="sxs-lookup"><span data-stu-id="2e794-151">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="2e794-152">**Nome host non valido**</span><span class="sxs-lookup"><span data-stu-id="2e794-152">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="2e794-153">74</span><span class="sxs-lookup"><span data-stu-id="2e794-153">74</span></span>

<span data-ttu-id="2e794-154">Nome host non valido.</span><span class="sxs-lookup"><span data-stu-id="2e794-154">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="2e794-155">**Nessun server WINS primario/secondario definito**</span><span class="sxs-lookup"><span data-stu-id="2e794-155">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="2e794-156">75</span><span class="sxs-lookup"><span data-stu-id="2e794-156">75</span></span>

<span data-ttu-id="2e794-157">Nessun server WINS primario o secondario definito.</span><span class="sxs-lookup"><span data-stu-id="2e794-157">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="2e794-158">**File non valido**</span><span class="sxs-lookup"><span data-stu-id="2e794-158">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="2e794-159">76</span><span class="sxs-lookup"><span data-stu-id="2e794-159">76</span></span>

<span data-ttu-id="2e794-160">File non valido.</span><span class="sxs-lookup"><span data-stu-id="2e794-160">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="2e794-161">**Percorso di sistema non valido**</span><span class="sxs-lookup"><span data-stu-id="2e794-161">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="2e794-162">77</span><span class="sxs-lookup"><span data-stu-id="2e794-162">77</span></span>

<span data-ttu-id="2e794-163">Percorso di sistema non valido.</span><span class="sxs-lookup"><span data-stu-id="2e794-163">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="2e794-164">**Copia del file non riuscita**</span><span class="sxs-lookup"><span data-stu-id="2e794-164">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="2e794-165">78</span><span class="sxs-lookup"><span data-stu-id="2e794-165">78</span></span>

<span data-ttu-id="2e794-166">Copia del file non riuscita.</span><span class="sxs-lookup"><span data-stu-id="2e794-166">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="2e794-167">**Parametro di sicurezza non valido**</span><span class="sxs-lookup"><span data-stu-id="2e794-167">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="2e794-168">79</span><span class="sxs-lookup"><span data-stu-id="2e794-168">79</span></span>

<span data-ttu-id="2e794-169">Parametro di sicurezza non valido.</span><span class="sxs-lookup"><span data-stu-id="2e794-169">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="2e794-170">**Impossibile configurare il servizio TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="2e794-170">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="2e794-171">80</span><span class="sxs-lookup"><span data-stu-id="2e794-171">80</span></span>

<span data-ttu-id="2e794-172">Impossibile configurare il servizio TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="2e794-172">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="2e794-173">**Non è possibile configurare il servizio DHCP**</span><span class="sxs-lookup"><span data-stu-id="2e794-173">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="2e794-174">81</span><span class="sxs-lookup"><span data-stu-id="2e794-174">81</span></span>

<span data-ttu-id="2e794-175">Impossibile configurare il servizio DHCP.</span><span class="sxs-lookup"><span data-stu-id="2e794-175">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="2e794-176">**Non è possibile rinnovare il lease DHCP**</span><span class="sxs-lookup"><span data-stu-id="2e794-176">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="2e794-177">82</span><span class="sxs-lookup"><span data-stu-id="2e794-177">82</span></span>

<span data-ttu-id="2e794-178">Non è possibile rinnovare il lease DHCP.</span><span class="sxs-lookup"><span data-stu-id="2e794-178">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="2e794-179">**Non è possibile rilasciare il lease DHCP**</span><span class="sxs-lookup"><span data-stu-id="2e794-179">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="2e794-180">83</span><span class="sxs-lookup"><span data-stu-id="2e794-180">83</span></span>

<span data-ttu-id="2e794-181">Impossibile rilasciare il lease DHCP.</span><span class="sxs-lookup"><span data-stu-id="2e794-181">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="2e794-182">**IP non abilitato sulla scheda**</span><span class="sxs-lookup"><span data-stu-id="2e794-182">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="2e794-183">84</span><span class="sxs-lookup"><span data-stu-id="2e794-183">84</span></span>

<span data-ttu-id="2e794-184">IP non abilitato sulla scheda.</span><span class="sxs-lookup"><span data-stu-id="2e794-184">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="2e794-185">**IPX non abilitato sull'adapter**</span><span class="sxs-lookup"><span data-stu-id="2e794-185">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="2e794-186">85</span><span class="sxs-lookup"><span data-stu-id="2e794-186">85</span></span>

<span data-ttu-id="2e794-187">IPX non abilitato sulla scheda.</span><span class="sxs-lookup"><span data-stu-id="2e794-187">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="2e794-188">**Errore limite numero frame/rete**</span><span class="sxs-lookup"><span data-stu-id="2e794-188">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="2e794-189">86</span><span class="sxs-lookup"><span data-stu-id="2e794-189">86</span></span>

<span data-ttu-id="2e794-190">Errore dei limiti del numero di rete o del frame.</span><span class="sxs-lookup"><span data-stu-id="2e794-190">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="2e794-191">**Tipo di frame non valido**</span><span class="sxs-lookup"><span data-stu-id="2e794-191">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="2e794-192">87</span><span class="sxs-lookup"><span data-stu-id="2e794-192">87</span></span>

<span data-ttu-id="2e794-193">Tipo di frame non valido.</span><span class="sxs-lookup"><span data-stu-id="2e794-193">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="2e794-194">**Numero di rete non valido**</span><span class="sxs-lookup"><span data-stu-id="2e794-194">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="2e794-195">88</span><span class="sxs-lookup"><span data-stu-id="2e794-195">88</span></span>

<span data-ttu-id="2e794-196">Numero di rete non valido.</span><span class="sxs-lookup"><span data-stu-id="2e794-196">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="2e794-197">**Numero di rete duplicato**</span><span class="sxs-lookup"><span data-stu-id="2e794-197">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="2e794-198">89</span><span class="sxs-lookup"><span data-stu-id="2e794-198">89</span></span>

<span data-ttu-id="2e794-199">Numero di rete duplicato.</span><span class="sxs-lookup"><span data-stu-id="2e794-199">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="2e794-200">**Parametro fuori limite**</span><span class="sxs-lookup"><span data-stu-id="2e794-200">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="2e794-201">90</span><span class="sxs-lookup"><span data-stu-id="2e794-201">90</span></span>

<span data-ttu-id="2e794-202">Parametro fuori limite.</span><span class="sxs-lookup"><span data-stu-id="2e794-202">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="2e794-203">**Accesso negato**</span><span class="sxs-lookup"><span data-stu-id="2e794-203">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="2e794-204">91</span><span class="sxs-lookup"><span data-stu-id="2e794-204">91</span></span>

<span data-ttu-id="2e794-205">Accesso negato.</span><span class="sxs-lookup"><span data-stu-id="2e794-205">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="2e794-206">**Memoria insufficiente**</span><span class="sxs-lookup"><span data-stu-id="2e794-206">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="2e794-207">92</span><span class="sxs-lookup"><span data-stu-id="2e794-207">92</span></span>

<span data-ttu-id="2e794-208">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="2e794-208">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="2e794-209">**Esiste già**</span><span class="sxs-lookup"><span data-stu-id="2e794-209">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="2e794-210">93</span><span class="sxs-lookup"><span data-stu-id="2e794-210">93</span></span>

<span data-ttu-id="2e794-211">Esiste già.</span><span class="sxs-lookup"><span data-stu-id="2e794-211">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="2e794-212">**Percorso, file o oggetto non trovato**</span><span class="sxs-lookup"><span data-stu-id="2e794-212">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="2e794-213">94</span><span class="sxs-lookup"><span data-stu-id="2e794-213">94</span></span>

<span data-ttu-id="2e794-214">Il percorso, il file o l'oggetto non è stato trovato.</span><span class="sxs-lookup"><span data-stu-id="2e794-214">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="2e794-215">**Non è possibile inviare una notifica al servizio**</span><span class="sxs-lookup"><span data-stu-id="2e794-215">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="2e794-216">95</span><span class="sxs-lookup"><span data-stu-id="2e794-216">95</span></span>

<span data-ttu-id="2e794-217">Impossibile notificare il servizio.</span><span class="sxs-lookup"><span data-stu-id="2e794-217">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="2e794-218">**Non è possibile inviare una notifica al servizio DNS**</span><span class="sxs-lookup"><span data-stu-id="2e794-218">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="2e794-219">96</span><span class="sxs-lookup"><span data-stu-id="2e794-219">96</span></span>

<span data-ttu-id="2e794-220">Impossibile inviare una notifica al servizio DNS.</span><span class="sxs-lookup"><span data-stu-id="2e794-220">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="2e794-221">**Interfaccia non configurabile**</span><span class="sxs-lookup"><span data-stu-id="2e794-221">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="2e794-222">97</span><span class="sxs-lookup"><span data-stu-id="2e794-222">97</span></span>

<span data-ttu-id="2e794-223">Interfaccia non configurabile.</span><span class="sxs-lookup"><span data-stu-id="2e794-223">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="2e794-224">**Non tutti i lease DHCP possono essere rilasciati/rinnovati**</span><span class="sxs-lookup"><span data-stu-id="2e794-224">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="2e794-225">98</span><span class="sxs-lookup"><span data-stu-id="2e794-225">98</span></span>

<span data-ttu-id="2e794-226">Non tutti i lease DHCP possono essere rilasciati o rinnovati.</span><span class="sxs-lookup"><span data-stu-id="2e794-226">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="2e794-227">**DHCP non abilitato sull'adapter**</span><span class="sxs-lookup"><span data-stu-id="2e794-227">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="2e794-228">100</span><span class="sxs-lookup"><span data-stu-id="2e794-228">100</span></span>

<span data-ttu-id="2e794-229">DHCP non abilitato sulla scheda.</span><span class="sxs-lookup"><span data-stu-id="2e794-229">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="2e794-230">**Altri**</span><span class="sxs-lookup"><span data-stu-id="2e794-230">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="2e794-231">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="2e794-231">101 4294967295</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="2e794-232">Esempio</span><span class="sxs-lookup"><span data-stu-id="2e794-232">Examples</span></span>

<span data-ttu-id="2e794-233">L'esempio relativo alla [modifica del numero consentito di connessioni TCP](https://Gallery.TechNet.Microsoft.Com/016d09f3-28aa-47eb-b439-100b89999bab) consente di impostare il numero massimo consentito di connessioni TCP aperte contemporaneamente in un computer su 10.</span><span class="sxs-lookup"><span data-stu-id="2e794-233">The [Modify the Allowed Number of TCP Connections](https://Gallery.TechNet.Microsoft.Com/016d09f3-28aa-47eb-b439-100b89999bab) VBScript sample sets the maximum allowed number of simultaneously-opened TCP connections on a computer to 10.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e794-234">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2e794-234">Requirements</span></span>



| <span data-ttu-id="2e794-235">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e794-235">Requirement</span></span> | <span data-ttu-id="2e794-236">Valore</span><span class="sxs-lookup"><span data-stu-id="2e794-236">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2e794-237">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2e794-237">Minimum supported client</span></span><br/> | <span data-ttu-id="2e794-238">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2e794-238">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2e794-239">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2e794-239">Minimum supported server</span></span><br/> | <span data-ttu-id="2e794-240">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2e794-240">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2e794-241">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="2e794-241">Namespace</span></span><br/>                | <span data-ttu-id="2e794-242">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="2e794-242">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2e794-243">MOF</span><span class="sxs-lookup"><span data-stu-id="2e794-243">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2e794-244"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2e794-244"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2e794-245">DLL</span><span class="sxs-lookup"><span data-stu-id="2e794-245">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2e794-246"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2e794-246"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e794-247">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2e794-247">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e794-248">Classi hardware del sistema del computer</span><span class="sxs-lookup"><span data-stu-id="2e794-248">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="2e794-249">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="2e794-249">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="2e794-250">Attività WMI: rete</span><span class="sxs-lookup"><span data-stu-id="2e794-250">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="2e794-251">Attività WMI: account e domini</span><span class="sxs-lookup"><span data-stu-id="2e794-251">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="2e794-252">Supporto di IPv6 e IPv4 in WMI</span><span class="sxs-lookup"><span data-stu-id="2e794-252">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

