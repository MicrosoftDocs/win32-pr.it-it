---
description: Il metodo SetTcpipNetbios consente viene utilizzato per impostare l'operazione predefinita di NetBIOS su TCP/IP.
ms.assetid: 2c639595-da13-400d-b4d0-432b39460554
ms.tgt_platform: multiple
title: Metodo SetTcpipNetbios consente della classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetTcpipNetbios
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 20ecab5918d00dc5f189464becc0252f2a8c0569
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878370"
---
# <a name="settcpipnetbios-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="df6fc-103">Metodo SetTcpipNetbios consente della \_ classe NetworkAdapterConfiguration Win32</span><span class="sxs-lookup"><span data-stu-id="df6fc-103">SetTcpipNetbios method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="df6fc-104">Il metodo **SetTcpipNetbios consente** viene utilizzato per impostare l'operazione predefinita di NetBIOS su TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="df6fc-104">The **SetTcpipNetbios** method is used to set the default operation of NetBIOS over TCP/IP.</span></span>

<span data-ttu-id="df6fc-105">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="df6fc-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="df6fc-106">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="df6fc-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="df6fc-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="df6fc-107">Syntax</span></span>


```mof
uint32 SetTcpipNetbios(
  [in] uint32 TcpipNetbiosOptions
);
```



## <a name="parameters"></a><span data-ttu-id="df6fc-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="df6fc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df6fc-109">*TcpipNetbiosOptions* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="df6fc-109">*TcpipNetbiosOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df6fc-110">Valore che specifica le possibili impostazioni correlate a NetBIOS su TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="df6fc-110">Value that specifies the possible settings related to NetBIOS over TCP/IP.</span></span>

<dt>

<span id="EnableNetbiosViaDhcp"></span><span id="enablenetbiosviadhcp"></span><span id="ENABLENETBIOSVIADHCP"></span>

<span data-ttu-id="df6fc-111"><span id="EnableNetbiosViaDhcp"></span><span id="enablenetbiosviadhcp"></span><span id="ENABLENETBIOSVIADHCP"></span>**EnableNetbiosViaDhcp** (0)</span><span class="sxs-lookup"><span data-stu-id="df6fc-111"><span id="EnableNetbiosViaDhcp"></span><span id="enablenetbiosviadhcp"></span><span id="ENABLENETBIOSVIADHCP"></span>**EnableNetbiosViaDhcp** (0)</span></span>


</dt> <dd>

<span data-ttu-id="df6fc-112">Abilitare NetBIOS tramite DHCP</span><span class="sxs-lookup"><span data-stu-id="df6fc-112">Enable Netbios via DHCP</span></span>

</dd> <dt>

<span id="EnableNetbios"></span><span id="enablenetbios"></span><span id="ENABLENETBIOS"></span>

<span data-ttu-id="df6fc-113"><span id="EnableNetbios"></span><span id="enablenetbios"></span><span id="ENABLENETBIOS"></span>**EnableNetbios** (1)</span><span class="sxs-lookup"><span data-stu-id="df6fc-113"><span id="EnableNetbios"></span><span id="enablenetbios"></span><span id="ENABLENETBIOS"></span>**EnableNetbios** (1)</span></span>


</dt> <dd>

<span data-ttu-id="df6fc-114">Abilita NetBIOS</span><span class="sxs-lookup"><span data-stu-id="df6fc-114">Enable Netbios</span></span>

</dd> <dt>

<span id="DisableNetbios"></span><span id="disablenetbios"></span><span id="DISABLENETBIOS"></span>

<span data-ttu-id="df6fc-115"><span id="DisableNetbios"></span><span id="disablenetbios"></span><span id="DISABLENETBIOS"></span>**DisableNetbios** (2)</span><span class="sxs-lookup"><span data-stu-id="df6fc-115"><span id="DisableNetbios"></span><span id="disablenetbios"></span><span id="DISABLENETBIOS"></span>**DisableNetbios** (2)</span></span>


</dt> <dd>

<span data-ttu-id="df6fc-116">Disabilitare NetBIOS</span><span class="sxs-lookup"><span data-stu-id="df6fc-116">Disable Netbios</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df6fc-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="df6fc-117">Return value</span></span>

<span data-ttu-id="df6fc-118">Restituisce un valore pari a 0 (zero) per un completamento corretto quando non è richiesto il riavvio, 1 (uno) per un completamento corretto quando è necessario un riavvio e un numero diverso se si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="df6fc-118">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="df6fc-119">Per ulteriori informazioni sui codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="df6fc-119">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="df6fc-120">Per i valori **HRESULT** generali, vedere [codici di errore di sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="df6fc-120">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="df6fc-121">**Operazione completata, non è necessario riavviare il computer**</span><span class="sxs-lookup"><span data-stu-id="df6fc-121">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="df6fc-122">0</span><span class="sxs-lookup"><span data-stu-id="df6fc-122">0</span></span>

<span data-ttu-id="df6fc-123">Operazione completata.</span><span class="sxs-lookup"><span data-stu-id="df6fc-123">Successful completion.</span></span> <span data-ttu-id="df6fc-124">Non è necessario riavviare il computer.</span><span class="sxs-lookup"><span data-stu-id="df6fc-124">No reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="df6fc-125">**Operazione completata, riavvio richiesto**</span><span class="sxs-lookup"><span data-stu-id="df6fc-125">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="df6fc-126">1</span><span class="sxs-lookup"><span data-stu-id="df6fc-126">1</span></span>

<span data-ttu-id="df6fc-127">Operazione completata.</span><span class="sxs-lookup"><span data-stu-id="df6fc-127">Successful completion.</span></span> <span data-ttu-id="df6fc-128">Riavvio richiesto.</span><span class="sxs-lookup"><span data-stu-id="df6fc-128">Reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="df6fc-129">**Metodo non supportato in questa piattaforma**</span><span class="sxs-lookup"><span data-stu-id="df6fc-129">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="df6fc-130">64</span><span class="sxs-lookup"><span data-stu-id="df6fc-130">64</span></span>

<span data-ttu-id="df6fc-131">Metodo non supportato in questa piattaforma.</span><span class="sxs-lookup"><span data-stu-id="df6fc-131">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="df6fc-132">**Errore sconosciuto**</span><span class="sxs-lookup"><span data-stu-id="df6fc-132">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="df6fc-133">65</span><span class="sxs-lookup"><span data-stu-id="df6fc-133">65</span></span>

<span data-ttu-id="df6fc-134">Errore sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="df6fc-134">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="df6fc-135">**subnet mask non valido**</span><span class="sxs-lookup"><span data-stu-id="df6fc-135">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="df6fc-136">66</span><span class="sxs-lookup"><span data-stu-id="df6fc-136">66</span></span>

<span data-ttu-id="df6fc-137">Subnet mask non valido.</span><span class="sxs-lookup"><span data-stu-id="df6fc-137">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="df6fc-138">**Si è verificato un errore durante l'elaborazione di un'istanza restituita**</span><span class="sxs-lookup"><span data-stu-id="df6fc-138">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="df6fc-139">67</span><span class="sxs-lookup"><span data-stu-id="df6fc-139">67</span></span>

<span data-ttu-id="df6fc-140">Si è verificato un errore durante l'elaborazione di un'istanza di restituita.</span><span class="sxs-lookup"><span data-stu-id="df6fc-140">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="df6fc-141">**Parametro di input non valido**</span><span class="sxs-lookup"><span data-stu-id="df6fc-141">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="df6fc-142">68</span><span class="sxs-lookup"><span data-stu-id="df6fc-142">68</span></span>

<span data-ttu-id="df6fc-143">Parametro di input non valido.</span><span class="sxs-lookup"><span data-stu-id="df6fc-143">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="df6fc-144">**Sono stati specificati più di 5 gateway**</span><span class="sxs-lookup"><span data-stu-id="df6fc-144">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="df6fc-145">69</span><span class="sxs-lookup"><span data-stu-id="df6fc-145">69</span></span>

<span data-ttu-id="df6fc-146">Sono stati specificati più di cinque gateway.</span><span class="sxs-lookup"><span data-stu-id="df6fc-146">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="df6fc-147">**Indirizzo IP non valido**</span><span class="sxs-lookup"><span data-stu-id="df6fc-147">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="df6fc-148">70</span><span class="sxs-lookup"><span data-stu-id="df6fc-148">70</span></span>

<span data-ttu-id="df6fc-149">Indirizzo IP non valido.</span><span class="sxs-lookup"><span data-stu-id="df6fc-149">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="df6fc-150">**Indirizzo IP gateway non valido**</span><span class="sxs-lookup"><span data-stu-id="df6fc-150">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="df6fc-151">71</span><span class="sxs-lookup"><span data-stu-id="df6fc-151">71</span></span>

<span data-ttu-id="df6fc-152">Indirizzo IP del gateway non valido.</span><span class="sxs-lookup"><span data-stu-id="df6fc-152">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="df6fc-153">**Si è verificato un errore durante l'accesso al registro di sistema per le informazioni richieste**</span><span class="sxs-lookup"><span data-stu-id="df6fc-153">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="df6fc-154">72</span><span class="sxs-lookup"><span data-stu-id="df6fc-154">72</span></span>

<span data-ttu-id="df6fc-155">Si è verificato un errore durante l'accesso al registro di sistema per le informazioni richieste.</span><span class="sxs-lookup"><span data-stu-id="df6fc-155">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="df6fc-156">**Nome di dominio non valido**</span><span class="sxs-lookup"><span data-stu-id="df6fc-156">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="df6fc-157">73</span><span class="sxs-lookup"><span data-stu-id="df6fc-157">73</span></span>

<span data-ttu-id="df6fc-158">Nome di dominio non valido.</span><span class="sxs-lookup"><span data-stu-id="df6fc-158">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="df6fc-159">**Nome host non valido**</span><span class="sxs-lookup"><span data-stu-id="df6fc-159">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="df6fc-160">74</span><span class="sxs-lookup"><span data-stu-id="df6fc-160">74</span></span>

<span data-ttu-id="df6fc-161">Nome host non valido.</span><span class="sxs-lookup"><span data-stu-id="df6fc-161">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="df6fc-162">**Nessun server WINS primario/secondario definito**</span><span class="sxs-lookup"><span data-stu-id="df6fc-162">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="df6fc-163">75</span><span class="sxs-lookup"><span data-stu-id="df6fc-163">75</span></span>

<span data-ttu-id="df6fc-164">Nessun server WINS primario o secondario definito.</span><span class="sxs-lookup"><span data-stu-id="df6fc-164">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="df6fc-165">**File non valido**</span><span class="sxs-lookup"><span data-stu-id="df6fc-165">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="df6fc-166">76</span><span class="sxs-lookup"><span data-stu-id="df6fc-166">76</span></span>

<span data-ttu-id="df6fc-167">File non valido.</span><span class="sxs-lookup"><span data-stu-id="df6fc-167">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="df6fc-168">**Percorso di sistema non valido**</span><span class="sxs-lookup"><span data-stu-id="df6fc-168">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="df6fc-169">77</span><span class="sxs-lookup"><span data-stu-id="df6fc-169">77</span></span>

<span data-ttu-id="df6fc-170">Percorso di sistema non valido.</span><span class="sxs-lookup"><span data-stu-id="df6fc-170">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="df6fc-171">**Copia del file non riuscita**</span><span class="sxs-lookup"><span data-stu-id="df6fc-171">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="df6fc-172">78</span><span class="sxs-lookup"><span data-stu-id="df6fc-172">78</span></span>

<span data-ttu-id="df6fc-173">Copia del file non riuscita.</span><span class="sxs-lookup"><span data-stu-id="df6fc-173">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="df6fc-174">**Parametro di sicurezza non valido**</span><span class="sxs-lookup"><span data-stu-id="df6fc-174">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="df6fc-175">79</span><span class="sxs-lookup"><span data-stu-id="df6fc-175">79</span></span>

<span data-ttu-id="df6fc-176">Parametro di sicurezza non valido.</span><span class="sxs-lookup"><span data-stu-id="df6fc-176">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="df6fc-177">**Impossibile configurare il servizio TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="df6fc-177">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="df6fc-178">80</span><span class="sxs-lookup"><span data-stu-id="df6fc-178">80</span></span>

<span data-ttu-id="df6fc-179">Impossibile configurare il servizio TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="df6fc-179">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="df6fc-180">**Non è possibile configurare il servizio DHCP**</span><span class="sxs-lookup"><span data-stu-id="df6fc-180">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="df6fc-181">81</span><span class="sxs-lookup"><span data-stu-id="df6fc-181">81</span></span>

<span data-ttu-id="df6fc-182">Impossibile configurare il servizio DHCP.</span><span class="sxs-lookup"><span data-stu-id="df6fc-182">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="df6fc-183">**Non è possibile rinnovare il lease DHCP**</span><span class="sxs-lookup"><span data-stu-id="df6fc-183">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="df6fc-184">82</span><span class="sxs-lookup"><span data-stu-id="df6fc-184">82</span></span>

<span data-ttu-id="df6fc-185">Non è possibile rinnovare il lease DHCP.</span><span class="sxs-lookup"><span data-stu-id="df6fc-185">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="df6fc-186">**Non è possibile rilasciare il lease DHCP**</span><span class="sxs-lookup"><span data-stu-id="df6fc-186">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="df6fc-187">83</span><span class="sxs-lookup"><span data-stu-id="df6fc-187">83</span></span>

<span data-ttu-id="df6fc-188">Impossibile rilasciare il lease DHCP.</span><span class="sxs-lookup"><span data-stu-id="df6fc-188">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="df6fc-189">**IP non abilitato sulla scheda**</span><span class="sxs-lookup"><span data-stu-id="df6fc-189">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="df6fc-190">84</span><span class="sxs-lookup"><span data-stu-id="df6fc-190">84</span></span>

<span data-ttu-id="df6fc-191">IP non abilitato sulla scheda.</span><span class="sxs-lookup"><span data-stu-id="df6fc-191">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="df6fc-192">**IPX non abilitato sull'adapter**</span><span class="sxs-lookup"><span data-stu-id="df6fc-192">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="df6fc-193">85</span><span class="sxs-lookup"><span data-stu-id="df6fc-193">85</span></span>

<span data-ttu-id="df6fc-194">IPX non abilitato sulla scheda.</span><span class="sxs-lookup"><span data-stu-id="df6fc-194">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="df6fc-195">**Errore limite numero frame/rete**</span><span class="sxs-lookup"><span data-stu-id="df6fc-195">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="df6fc-196">86</span><span class="sxs-lookup"><span data-stu-id="df6fc-196">86</span></span>

<span data-ttu-id="df6fc-197">Errore dei limiti del numero di rete o del frame.</span><span class="sxs-lookup"><span data-stu-id="df6fc-197">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="df6fc-198">**Tipo di frame non valido**</span><span class="sxs-lookup"><span data-stu-id="df6fc-198">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="df6fc-199">87</span><span class="sxs-lookup"><span data-stu-id="df6fc-199">87</span></span>

<span data-ttu-id="df6fc-200">Tipo di frame non valido.</span><span class="sxs-lookup"><span data-stu-id="df6fc-200">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="df6fc-201">**Numero di rete non valido**</span><span class="sxs-lookup"><span data-stu-id="df6fc-201">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="df6fc-202">88</span><span class="sxs-lookup"><span data-stu-id="df6fc-202">88</span></span>

<span data-ttu-id="df6fc-203">Numero di rete non valido.</span><span class="sxs-lookup"><span data-stu-id="df6fc-203">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="df6fc-204">**Numero di rete duplicato**</span><span class="sxs-lookup"><span data-stu-id="df6fc-204">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="df6fc-205">89</span><span class="sxs-lookup"><span data-stu-id="df6fc-205">89</span></span>

<span data-ttu-id="df6fc-206">Numero di rete duplicato.</span><span class="sxs-lookup"><span data-stu-id="df6fc-206">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="df6fc-207">**Parametro fuori limite**</span><span class="sxs-lookup"><span data-stu-id="df6fc-207">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="df6fc-208">90</span><span class="sxs-lookup"><span data-stu-id="df6fc-208">90</span></span>

<span data-ttu-id="df6fc-209">Parametro fuori limite.</span><span class="sxs-lookup"><span data-stu-id="df6fc-209">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="df6fc-210">**Accesso negato**</span><span class="sxs-lookup"><span data-stu-id="df6fc-210">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="df6fc-211">91</span><span class="sxs-lookup"><span data-stu-id="df6fc-211">91</span></span>

<span data-ttu-id="df6fc-212">Accesso negato.</span><span class="sxs-lookup"><span data-stu-id="df6fc-212">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="df6fc-213">**Memoria insufficiente**</span><span class="sxs-lookup"><span data-stu-id="df6fc-213">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="df6fc-214">92</span><span class="sxs-lookup"><span data-stu-id="df6fc-214">92</span></span>

<span data-ttu-id="df6fc-215">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="df6fc-215">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="df6fc-216">**Esiste già**</span><span class="sxs-lookup"><span data-stu-id="df6fc-216">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="df6fc-217">93</span><span class="sxs-lookup"><span data-stu-id="df6fc-217">93</span></span>

<span data-ttu-id="df6fc-218">Esiste già.</span><span class="sxs-lookup"><span data-stu-id="df6fc-218">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="df6fc-219">**Percorso, file o oggetto non trovato**</span><span class="sxs-lookup"><span data-stu-id="df6fc-219">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="df6fc-220">94</span><span class="sxs-lookup"><span data-stu-id="df6fc-220">94</span></span>

<span data-ttu-id="df6fc-221">Il percorso, il file o l'oggetto non è stato trovato.</span><span class="sxs-lookup"><span data-stu-id="df6fc-221">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="df6fc-222">**Non è possibile inviare una notifica al servizio**</span><span class="sxs-lookup"><span data-stu-id="df6fc-222">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="df6fc-223">95</span><span class="sxs-lookup"><span data-stu-id="df6fc-223">95</span></span>

<span data-ttu-id="df6fc-224">Impossibile notificare il servizio.</span><span class="sxs-lookup"><span data-stu-id="df6fc-224">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="df6fc-225">**Non è possibile inviare una notifica al servizio DNS**</span><span class="sxs-lookup"><span data-stu-id="df6fc-225">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="df6fc-226">96</span><span class="sxs-lookup"><span data-stu-id="df6fc-226">96</span></span>

<span data-ttu-id="df6fc-227">Impossibile inviare una notifica al servizio DNS.</span><span class="sxs-lookup"><span data-stu-id="df6fc-227">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="df6fc-228">**Interfaccia non configurabile**</span><span class="sxs-lookup"><span data-stu-id="df6fc-228">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="df6fc-229">97</span><span class="sxs-lookup"><span data-stu-id="df6fc-229">97</span></span>

<span data-ttu-id="df6fc-230">Interfaccia non configurabile.</span><span class="sxs-lookup"><span data-stu-id="df6fc-230">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="df6fc-231">**Non tutti i lease DHCP possono essere rilasciati/rinnovati**</span><span class="sxs-lookup"><span data-stu-id="df6fc-231">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="df6fc-232">98</span><span class="sxs-lookup"><span data-stu-id="df6fc-232">98</span></span>

<span data-ttu-id="df6fc-233">Non tutti i lease DHCP possono essere rilasciati o rinnovati.</span><span class="sxs-lookup"><span data-stu-id="df6fc-233">Not all DHCP leases can be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="df6fc-234">**DHCP non abilitato sull'adapter**</span><span class="sxs-lookup"><span data-stu-id="df6fc-234">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="df6fc-235">100</span><span class="sxs-lookup"><span data-stu-id="df6fc-235">100</span></span>

<span data-ttu-id="df6fc-236">DHCP non abilitato sulla scheda.</span><span class="sxs-lookup"><span data-stu-id="df6fc-236">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="df6fc-237">**Altri**</span><span class="sxs-lookup"><span data-stu-id="df6fc-237">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="df6fc-238">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="df6fc-238">101 4294967295</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="df6fc-239">Esempio</span><span class="sxs-lookup"><span data-stu-id="df6fc-239">Examples</span></span>

<span data-ttu-id="df6fc-240">L'esempio [Modify NetBIOS use on a Network Adapter](https://Gallery.TechNet.Microsoft.Com/01d541f7-5c0d-46d3-8619-28aaab154dc0) VBScript Abilita NetBIOS per una scheda di rete.</span><span class="sxs-lookup"><span data-stu-id="df6fc-240">The [Modify NetBIOS Use on a Network Adapter](https://Gallery.TechNet.Microsoft.Com/01d541f7-5c0d-46d3-8619-28aaab154dc0) VBScript sample enables NetBIOS for a network adapter.</span></span>

<span data-ttu-id="df6fc-241">L'esempio di configurazione delle [schede di rete iSCSI come per le procedure consigliate di Microsoft](https://Gallery.TechNet.Microsoft.Com/Configure-iSCSI-Network-81232a5e) consente di automatizzare le impostazioni di configurazione per una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="df6fc-241">The [Configure iSCSI Network Cards as per Microsoft Best Practices PowerShell](https://Gallery.TechNet.Microsoft.Com/Configure-iSCSI-Network-81232a5e) sample automates the configuration settings for a Virtual Machine.</span></span>

## <a name="requirements"></a><span data-ttu-id="df6fc-242">Requisiti</span><span class="sxs-lookup"><span data-stu-id="df6fc-242">Requirements</span></span>



| <span data-ttu-id="df6fc-243">Requisito</span><span class="sxs-lookup"><span data-stu-id="df6fc-243">Requirement</span></span> | <span data-ttu-id="df6fc-244">Valore</span><span class="sxs-lookup"><span data-stu-id="df6fc-244">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="df6fc-245">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="df6fc-245">Minimum supported client</span></span><br/> | <span data-ttu-id="df6fc-246">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="df6fc-246">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="df6fc-247">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="df6fc-247">Minimum supported server</span></span><br/> | <span data-ttu-id="df6fc-248">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="df6fc-248">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="df6fc-249">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="df6fc-249">Namespace</span></span><br/>                | <span data-ttu-id="df6fc-250">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="df6fc-250">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="df6fc-251">MOF</span><span class="sxs-lookup"><span data-stu-id="df6fc-251">MOF</span></span><br/>                      | <dl> <span data-ttu-id="df6fc-252"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="df6fc-252"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="df6fc-253">DLL</span><span class="sxs-lookup"><span data-stu-id="df6fc-253">DLL</span></span><br/>                      | <dl> <span data-ttu-id="df6fc-254"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="df6fc-254"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df6fc-255">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="df6fc-255">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df6fc-256">Classi hardware del sistema del computer</span><span class="sxs-lookup"><span data-stu-id="df6fc-256">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="df6fc-257">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="df6fc-257">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="df6fc-258">Attività WMI: rete</span><span class="sxs-lookup"><span data-stu-id="df6fc-258">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="df6fc-259">Attività WMI: account e domini</span><span class="sxs-lookup"><span data-stu-id="df6fc-259">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="df6fc-260">Supporto di IPv6 e IPv4 in WMI</span><span class="sxs-lookup"><span data-stu-id="df6fc-260">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

