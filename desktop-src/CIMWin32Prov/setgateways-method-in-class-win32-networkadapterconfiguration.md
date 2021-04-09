---
description: I gateway &\# 32; Il metodo della classe WMI specifica un elenco di gateway per il routing dei pacchetti a una subnet diversa dalla subnet a cui è connessa la scheda di rete.
ms.assetid: 240f7aff-7a07-4e0d-af30-7bcabb68c736
ms.tgt_platform: multiple
title: Metodo segateways della classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetGateways
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 215bfa736a0f9d67ae587ac1f0e1b4aa394b85d9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877961"
---
# <a name="setgateways-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="4f8a2-103">Metodo segateways della classe Win32 \_ NetworkAdapterConfiguration</span><span class="sxs-lookup"><span data-stu-id="4f8a2-103">SetGateways method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="4f8a2-104">Il metodo della [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) del **gateway** specifica un elenco di gateway per il routing dei pacchetti a una subnet diversa dalla subnet a cui è connessa la scheda di rete.</span><span class="sxs-lookup"><span data-stu-id="4f8a2-104">The **SetGateways** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method specifies a list of gateways for routing packets to a subnet that is different from the subnet that the network adapter is connected to.</span></span>

<span data-ttu-id="4f8a2-105">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="4f8a2-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="4f8a2-106">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="4f8a2-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="4f8a2-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4f8a2-107">Syntax</span></span>


```mof
uint32 SetGateways(
  [in]           string DefaultIPGateway[],
  [in, optional] uint16 GatewayCostMetric[]
);
```



## <a name="parameters"></a><span data-ttu-id="4f8a2-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="4f8a2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f8a2-109">*DefaultIPGateway* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4f8a2-109">*DefaultIPGateway* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4f8a2-110">Elenco di indirizzi IP ai gateway in cui vengono instradati i pacchetti di rete.</span><span class="sxs-lookup"><span data-stu-id="4f8a2-110">List of IP addresses to gateways where network packets are routed.</span></span>

</dd> <dt>

<span data-ttu-id="4f8a2-111">*GatewayCostMetric* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="4f8a2-111">*GatewayCostMetric* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4f8a2-112">Assegna un valore compreso tra 1 e 9999, utilizzato per calcolare le route più veloci e affidabili.</span><span class="sxs-lookup"><span data-stu-id="4f8a2-112">Assigns a value that ranges from 1 to 9999, which is used to calculate the fastest and most reliable routes.</span></span> <span data-ttu-id="4f8a2-113">I valori di questo parametro corrispondono ai valori nel parametro *DefaultIPGateway* .</span><span class="sxs-lookup"><span data-stu-id="4f8a2-113">The values of this parameter correspond with the values in the *DefaultIPGateway* parameter.</span></span> <span data-ttu-id="4f8a2-114">Il valore predefinito per un gateway è 1.</span><span class="sxs-lookup"><span data-stu-id="4f8a2-114">The default value for a gateway is 1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4f8a2-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4f8a2-115">Return value</span></span>

<span data-ttu-id="4f8a2-116">Restituisce un valore pari a 0 (zero) per un completamento corretto quando non è richiesto un riavvio, 1 (uno) per un completamento corretto quando è necessario un riavvio e qualsiasi altro valore se si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="4f8a2-116">Returns a value of 0 (zero) for a successful completion when a reboot is not required, 1 (one) for a successful completion when a reboot is required, and any other value if there is an error.</span></span> <span data-ttu-id="4f8a2-117">Per ulteriori informazioni sui codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="4f8a2-117">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="4f8a2-118">Per i valori **HRESULT** generali, vedere [codici di errore di sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="4f8a2-118">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="4f8a2-119">**Operazione completata, non è necessario riavviare il computer**</span><span class="sxs-lookup"><span data-stu-id="4f8a2-119">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="4f8a2-120">0</span><span class="sxs-lookup"><span data-stu-id="4f8a2-120">0</span></span>

</dd> <dt>

<span data-ttu-id="4f8a2-121">**Operazione completata, riavvio richiesto**</span><span class="sxs-lookup"><span data-stu-id="4f8a2-121">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="4f8a2-122">1</span><span class="sxs-lookup"><span data-stu-id="4f8a2-122">1</span></span>

</dd> <dt>

<span data-ttu-id="4f8a2-123">**Metodo non supportato in questa piattaforma**</span><span class="sxs-lookup"><span data-stu-id="4f8a2-123">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="4f8a2-124">64</span><span class="sxs-lookup"><span data-stu-id="4f8a2-124">64</span></span>

<span data-ttu-id="4f8a2-125">Metodo non supportato quando la scheda di interfaccia di rete è in modalità DHCP.</span><span class="sxs-lookup"><span data-stu-id="4f8a2-125">Method not supported when the NIC is in DHCP mode.</span></span>

</dd> <dt>

<span data-ttu-id="4f8a2-126">**Errore sconosciuto**</span><span class="sxs-lookup"><span data-stu-id="4f8a2-126">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="4f8a2-127">65</span><span class="sxs-lookup"><span data-stu-id="4f8a2-127">65</span></span>

</dd> <dt>

<span data-ttu-id="4f8a2-128">**subnet mask non valido**</span><span class="sxs-lookup"><span data-stu-id="4f8a2-128">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="4f8a2-129">66</span><span class="sxs-lookup"><span data-stu-id="4f8a2-129">66</span></span>

</dd> <dt>

<span data-ttu-id="4f8a2-130">**Si è verificato un errore durante l'elaborazione di un'istanza restituita**</span><span class="sxs-lookup"><span data-stu-id="4f8a2-130">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="4f8a2-131">67</span><span class="sxs-lookup"><span data-stu-id="4f8a2-131">67</span></span>

</dd> <dt>

<span data-ttu-id="4f8a2-132">**Parametro di input non valido**</span><span class="sxs-lookup"><span data-stu-id="4f8a2-132">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="4f8a2-133">68</span><span class="sxs-lookup"><span data-stu-id="4f8a2-133">68</span></span>

</dd> <dt>

<span data-ttu-id="4f8a2-134">**Sono stati specificati più di 5 gateway**</span><span class="sxs-lookup"><span data-stu-id="4f8a2-134">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="4f8a2-135">69</span><span class="sxs-lookup"><span data-stu-id="4f8a2-135">69</span></span>

</dd> <dt>

<span data-ttu-id="4f8a2-136">**Indirizzo IP non valido**</span><span class="sxs-lookup"><span data-stu-id="4f8a2-136">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="4f8a2-137">70</span><span class="sxs-lookup"><span data-stu-id="4f8a2-137">70</span></span>

</dd> <dt>

<span data-ttu-id="4f8a2-138">**Indirizzo IP gateway non valido**</span><span class="sxs-lookup"><span data-stu-id="4f8a2-138">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="4f8a2-139">71</span><span class="sxs-lookup"><span data-stu-id="4f8a2-139">71</span></span>

</dd> <dt>

<span data-ttu-id="4f8a2-140">**Si è verificato un errore durante l'accesso al registro di sistema per le informazioni richieste**</span><span class="sxs-lookup"><span data-stu-id="4f8a2-140">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="4f8a2-141">72</span><span class="sxs-lookup"><span data-stu-id="4f8a2-141">72</span></span>

</dd> <dt>

<span data-ttu-id="4f8a2-142">**Nome di dominio non valido**</span><span class="sxs-lookup"><span data-stu-id="4f8a2-142">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="4f8a2-143">73</span><span class="sxs-lookup"><span data-stu-id="4f8a2-143">73</span></span>

</dd> <dt>

<span data-ttu-id="4f8a2-144">**Nome host non valido**</span><span class="sxs-lookup"><span data-stu-id="4f8a2-144">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="4f8a2-145">74</span><span class="sxs-lookup"><span data-stu-id="4f8a2-145">74</span></span>

</dd> <dt>

<span data-ttu-id="4f8a2-146">**Nessun server WINS primario/secondario definito**</span><span class="sxs-lookup"><span data-stu-id="4f8a2-146">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="4f8a2-147">75</span><span class="sxs-lookup"><span data-stu-id="4f8a2-147">75</span></span>

</dd> <dt>

<span data-ttu-id="4f8a2-148">**File non valido**</span><span class="sxs-lookup"><span data-stu-id="4f8a2-148">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="4f8a2-149">76</span><span class="sxs-lookup"><span data-stu-id="4f8a2-149">76</span></span>

</dd> <dt>

<span data-ttu-id="4f8a2-150">**Percorso di sistema non valido**</span><span class="sxs-lookup"><span data-stu-id="4f8a2-150">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="4f8a2-151">77</span><span class="sxs-lookup"><span data-stu-id="4f8a2-151">77</span></span>

</dd> <dt>

<span data-ttu-id="4f8a2-152">**Copia del file non riuscita**</span><span class="sxs-lookup"><span data-stu-id="4f8a2-152">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="4f8a2-153">78</span><span class="sxs-lookup"><span data-stu-id="4f8a2-153">78</span></span>

</dd> <dt>

<span data-ttu-id="4f8a2-154">**Parametro di sicurezza non valido**</span><span class="sxs-lookup"><span data-stu-id="4f8a2-154">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="4f8a2-155">79</span><span class="sxs-lookup"><span data-stu-id="4f8a2-155">79</span></span>

</dd> <dt>

<span data-ttu-id="4f8a2-156">**Impossibile configurare il servizio TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="4f8a2-156">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="4f8a2-157">80</span><span class="sxs-lookup"><span data-stu-id="4f8a2-157">80</span></span>

</dd> <dt>

<span data-ttu-id="4f8a2-158">**Non è possibile configurare il servizio DHCP**</span><span class="sxs-lookup"><span data-stu-id="4f8a2-158">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="4f8a2-159">81</span><span class="sxs-lookup"><span data-stu-id="4f8a2-159">81</span></span>

</dd> <dt>

<span data-ttu-id="4f8a2-160">**Non è possibile rinnovare il lease DHCP**</span><span class="sxs-lookup"><span data-stu-id="4f8a2-160">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="4f8a2-161">82</span><span class="sxs-lookup"><span data-stu-id="4f8a2-161">82</span></span>

</dd> <dt>

<span data-ttu-id="4f8a2-162">**Non è possibile rilasciare il lease DHCP**</span><span class="sxs-lookup"><span data-stu-id="4f8a2-162">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="4f8a2-163">83</span><span class="sxs-lookup"><span data-stu-id="4f8a2-163">83</span></span>

</dd> <dt>

<span data-ttu-id="4f8a2-164">**IP non abilitato sulla scheda**</span><span class="sxs-lookup"><span data-stu-id="4f8a2-164">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="4f8a2-165">84</span><span class="sxs-lookup"><span data-stu-id="4f8a2-165">84</span></span>

</dd> <dt>

<span data-ttu-id="4f8a2-166">**IPX non abilitato sull'adapter**</span><span class="sxs-lookup"><span data-stu-id="4f8a2-166">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="4f8a2-167">85</span><span class="sxs-lookup"><span data-stu-id="4f8a2-167">85</span></span>

</dd> <dt>

<span data-ttu-id="4f8a2-168">**Errore limite numero frame/rete**</span><span class="sxs-lookup"><span data-stu-id="4f8a2-168">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="4f8a2-169">86</span><span class="sxs-lookup"><span data-stu-id="4f8a2-169">86</span></span>

</dd> <dt>

<span data-ttu-id="4f8a2-170">**Tipo di frame non valido**</span><span class="sxs-lookup"><span data-stu-id="4f8a2-170">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="4f8a2-171">87</span><span class="sxs-lookup"><span data-stu-id="4f8a2-171">87</span></span>

</dd> <dt>

<span data-ttu-id="4f8a2-172">**Numero di rete non valido**</span><span class="sxs-lookup"><span data-stu-id="4f8a2-172">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="4f8a2-173">88</span><span class="sxs-lookup"><span data-stu-id="4f8a2-173">88</span></span>

</dd> <dt>

<span data-ttu-id="4f8a2-174">**Numero di rete duplicato**</span><span class="sxs-lookup"><span data-stu-id="4f8a2-174">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="4f8a2-175">89</span><span class="sxs-lookup"><span data-stu-id="4f8a2-175">89</span></span>

</dd> <dt>

<span data-ttu-id="4f8a2-176">**Parametro fuori limite**</span><span class="sxs-lookup"><span data-stu-id="4f8a2-176">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="4f8a2-177">90</span><span class="sxs-lookup"><span data-stu-id="4f8a2-177">90</span></span>

</dd> <dt>

<span data-ttu-id="4f8a2-178">**Accesso negato**</span><span class="sxs-lookup"><span data-stu-id="4f8a2-178">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="4f8a2-179">91</span><span class="sxs-lookup"><span data-stu-id="4f8a2-179">91</span></span>

</dd> <dt>

<span data-ttu-id="4f8a2-180">**Memoria insufficiente**</span><span class="sxs-lookup"><span data-stu-id="4f8a2-180">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="4f8a2-181">92</span><span class="sxs-lookup"><span data-stu-id="4f8a2-181">92</span></span>

</dd> <dt>

<span data-ttu-id="4f8a2-182">**Esiste già**</span><span class="sxs-lookup"><span data-stu-id="4f8a2-182">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="4f8a2-183">93</span><span class="sxs-lookup"><span data-stu-id="4f8a2-183">93</span></span>

</dd> <dt>

<span data-ttu-id="4f8a2-184">**Percorso, file o oggetto non trovato**</span><span class="sxs-lookup"><span data-stu-id="4f8a2-184">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="4f8a2-185">94</span><span class="sxs-lookup"><span data-stu-id="4f8a2-185">94</span></span>

</dd> <dt>

<span data-ttu-id="4f8a2-186">**Non è possibile inviare una notifica al servizio**</span><span class="sxs-lookup"><span data-stu-id="4f8a2-186">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="4f8a2-187">95</span><span class="sxs-lookup"><span data-stu-id="4f8a2-187">95</span></span>

</dd> <dt>

<span data-ttu-id="4f8a2-188">**Non è possibile inviare una notifica al servizio DNS**</span><span class="sxs-lookup"><span data-stu-id="4f8a2-188">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="4f8a2-189">96</span><span class="sxs-lookup"><span data-stu-id="4f8a2-189">96</span></span>

</dd> <dt>

<span data-ttu-id="4f8a2-190">**Interfaccia non configurabile**</span><span class="sxs-lookup"><span data-stu-id="4f8a2-190">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="4f8a2-191">97</span><span class="sxs-lookup"><span data-stu-id="4f8a2-191">97</span></span>

</dd> <dt>

<span data-ttu-id="4f8a2-192">**Non tutti i lease DHCP possono essere rilasciati/rinnovati**</span><span class="sxs-lookup"><span data-stu-id="4f8a2-192">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="4f8a2-193">98</span><span class="sxs-lookup"><span data-stu-id="4f8a2-193">98</span></span>

</dd> <dt>

<span data-ttu-id="4f8a2-194">**DHCP non abilitato sull'adapter**</span><span class="sxs-lookup"><span data-stu-id="4f8a2-194">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="4f8a2-195">100</span><span class="sxs-lookup"><span data-stu-id="4f8a2-195">100</span></span>

</dd> <dt>

<span data-ttu-id="4f8a2-196">**Altri**</span><span class="sxs-lookup"><span data-stu-id="4f8a2-196">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="4f8a2-197">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="4f8a2-197">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4f8a2-198">Commenti</span><span class="sxs-lookup"><span data-stu-id="4f8a2-198">Remarks</span></span>

<span data-ttu-id="4f8a2-199">Questo metodo funziona solo quando la scheda di interfaccia di rete (NIC) è in modalità IP statico.</span><span class="sxs-lookup"><span data-stu-id="4f8a2-199">This method only works when the Network Interface Card (NIC) is in the static IP mode.</span></span>

<span data-ttu-id="4f8a2-200">Per cancellare il gateway, impostare il gateway sullo stesso IP usato in [**EnableStatic**](enablestatic-method-in-class-win32-networkadapterconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="4f8a2-200">To clear the gateway, set your gateway to the same IP you use on [**EnableStatic**](enablestatic-method-in-class-win32-networkadapterconfiguration.md).</span></span>

## <a name="examples"></a><span data-ttu-id="4f8a2-201">Esempio</span><span class="sxs-lookup"><span data-stu-id="4f8a2-201">Examples</span></span>

<span data-ttu-id="4f8a2-202">L'esempio [modificare i gateway per una scheda di rete](https://Gallery.TechNet.Microsoft.Com/9ea7670b-f68f-4efb-9cd2-7c299a8f657f) VBScript configura due gateway per una scheda di rete.</span><span class="sxs-lookup"><span data-stu-id="4f8a2-202">The [Modify the Gateways for a Network Adapter](https://Gallery.TechNet.Microsoft.Com/9ea7670b-f68f-4efb-9cd2-7c299a8f657f) VBScript sample configures two gateways for a network adapter.</span></span>

<span data-ttu-id="4f8a2-203">L'esempio [assegnare un indirizzo IP statico](https://Gallery.TechNet.Microsoft.Com/8979c752-8288-4a18-b5ed-f3b79f013f4a) VBScript consente di impostare l'indirizzo IP e il gateway di un computer.</span><span class="sxs-lookup"><span data-stu-id="4f8a2-203">The [Assign a Static IP Address](https://Gallery.TechNet.Microsoft.Com/8979c752-8288-4a18-b5ed-f3b79f013f4a) VBScript sample sets the IP address and gateway of a computer.</span></span>

<span data-ttu-id="4f8a2-204">L' [indirizzo IP statico e quindi un join a un esempio di](https://Gallery.TechNet.Microsoft.Com/Static-IP-and-then-join-to-130d4b8a) PowerShell di dominio assiste nella ricompilazione dei computer.</span><span class="sxs-lookup"><span data-stu-id="4f8a2-204">The [Static IP and then join to a domain](https://Gallery.TechNet.Microsoft.Com/Static-IP-and-then-join-to-130d4b8a) PowerShell sample assists in rebuilding machines.</span></span>

## <a name="requirements"></a><span data-ttu-id="4f8a2-205">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4f8a2-205">Requirements</span></span>



| <span data-ttu-id="4f8a2-206">Requisito</span><span class="sxs-lookup"><span data-stu-id="4f8a2-206">Requirement</span></span> | <span data-ttu-id="4f8a2-207">Valore</span><span class="sxs-lookup"><span data-stu-id="4f8a2-207">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4f8a2-208">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4f8a2-208">Minimum supported client</span></span><br/> | <span data-ttu-id="4f8a2-209">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4f8a2-209">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4f8a2-210">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4f8a2-210">Minimum supported server</span></span><br/> | <span data-ttu-id="4f8a2-211">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4f8a2-211">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4f8a2-212">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="4f8a2-212">Namespace</span></span><br/>                | <span data-ttu-id="4f8a2-213">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="4f8a2-213">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="4f8a2-214">MOF</span><span class="sxs-lookup"><span data-stu-id="4f8a2-214">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4f8a2-215"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4f8a2-215"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="4f8a2-216">DLL</span><span class="sxs-lookup"><span data-stu-id="4f8a2-216">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4f8a2-217"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4f8a2-217"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f8a2-218">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4f8a2-218">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f8a2-219">Classi hardware del sistema del computer</span><span class="sxs-lookup"><span data-stu-id="4f8a2-219">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="4f8a2-220">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="4f8a2-220">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="4f8a2-221">Attività WMI: rete</span><span class="sxs-lookup"><span data-stu-id="4f8a2-221">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="4f8a2-222">Attività WMI: account e domini</span><span class="sxs-lookup"><span data-stu-id="4f8a2-222">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="4f8a2-223">Supporto di IPv6 e IPv4 in WMI</span><span class="sxs-lookup"><span data-stu-id="4f8a2-223">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

