---
description: Il metodo statico della classe WMI SetArpUseEtherSNAP viene usato per abilitare i pacchetti Ethernet per l'uso della codifica SNAP 802,3.
ms.assetid: 437954c0-ea6b-4559-a4cb-1f66630e70fe
ms.tgt_platform: multiple
title: Metodo SetArpUseEtherSNAP della classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetArpUseEtherSNAP
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 52e3ce42948d5c40bbde3329b37ee3fa506c47ce
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878313"
---
# <a name="setarpuseethersnap-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="7b729-103">Metodo SetArpUseEtherSNAP della \_ classe NetworkAdapterConfiguration Win32</span><span class="sxs-lookup"><span data-stu-id="7b729-103">SetArpUseEtherSNAP method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="7b729-104">Il metodo statico della [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetArpUseEtherSNAP** viene usato per abilitare i pacchetti Ethernet per l'uso della codifica SNAP 802,3.</span><span class="sxs-lookup"><span data-stu-id="7b729-104">The **SetArpUseEtherSNAP** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to enable ethernet packets to use 802.3 SNAP encoding.</span></span>

<span data-ttu-id="7b729-105">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="7b729-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="7b729-106">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="7b729-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="7b729-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7b729-107">Syntax</span></span>


```mof
uint32 SetArpUseEtherSNAP(
  [in] boolean ArpUseEtherSNAP
);
```



## <a name="parameters"></a><span data-ttu-id="7b729-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="7b729-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7b729-109">*ArpUseEtherSNAP* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7b729-109">*ArpUseEtherSNAP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b729-110">Se **true** Abilita TCP/IP per la trasmissione di pacchetti Ethernet con la codifica di snap 802,3.</span><span class="sxs-lookup"><span data-stu-id="7b729-110">If **true** enables TCP/IP to transmit Ethernet packets using 802.3 SNAP encoding.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7b729-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7b729-111">Return value</span></span>

<span data-ttu-id="7b729-112">Restituisce un valore pari a 0 (zero) per un completamento corretto quando non è richiesto il riavvio, 1 (uno) per un completamento corretto quando è necessario un riavvio e un numero diverso se si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="7b729-112">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="7b729-113">Per ulteriori informazioni sui codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="7b729-113">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="7b729-114">Per i valori **HRESULT** generali, vedere [codici di errore di sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="7b729-114">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="7b729-115">**Operazione completata, non è necessario riavviare il computer**</span><span class="sxs-lookup"><span data-stu-id="7b729-115">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="7b729-116">0</span><span class="sxs-lookup"><span data-stu-id="7b729-116">0</span></span>

<span data-ttu-id="7b729-117">Operazione completata, non è necessario riavviare il computer.</span><span class="sxs-lookup"><span data-stu-id="7b729-117">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="7b729-118">**Operazione completata, riavvio richiesto**</span><span class="sxs-lookup"><span data-stu-id="7b729-118">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="7b729-119">1</span><span class="sxs-lookup"><span data-stu-id="7b729-119">1</span></span>

<span data-ttu-id="7b729-120">Operazione completata, è necessario riavviare il computer.</span><span class="sxs-lookup"><span data-stu-id="7b729-120">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="7b729-121">**Metodo non supportato in questa piattaforma**</span><span class="sxs-lookup"><span data-stu-id="7b729-121">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="7b729-122">64</span><span class="sxs-lookup"><span data-stu-id="7b729-122">64</span></span>

<span data-ttu-id="7b729-123">Metodo non supportato in questa piattaforma.</span><span class="sxs-lookup"><span data-stu-id="7b729-123">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="7b729-124">**Errore sconosciuto**</span><span class="sxs-lookup"><span data-stu-id="7b729-124">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="7b729-125">65</span><span class="sxs-lookup"><span data-stu-id="7b729-125">65</span></span>

<span data-ttu-id="7b729-126">Errore sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="7b729-126">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="7b729-127">**subnet mask non valido**</span><span class="sxs-lookup"><span data-stu-id="7b729-127">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="7b729-128">66</span><span class="sxs-lookup"><span data-stu-id="7b729-128">66</span></span>

<span data-ttu-id="7b729-129">Subnet mask non valido.</span><span class="sxs-lookup"><span data-stu-id="7b729-129">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="7b729-130">**Si è verificato un errore durante l'elaborazione di un'istanza restituita**</span><span class="sxs-lookup"><span data-stu-id="7b729-130">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="7b729-131">67</span><span class="sxs-lookup"><span data-stu-id="7b729-131">67</span></span>

<span data-ttu-id="7b729-132">Si è verificato un errore durante l'elaborazione di un'istanza di restituita.</span><span class="sxs-lookup"><span data-stu-id="7b729-132">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="7b729-133">**Parametro di input non valido**</span><span class="sxs-lookup"><span data-stu-id="7b729-133">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="7b729-134">68</span><span class="sxs-lookup"><span data-stu-id="7b729-134">68</span></span>

<span data-ttu-id="7b729-135">Parametro di input non valido.</span><span class="sxs-lookup"><span data-stu-id="7b729-135">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="7b729-136">**Sono stati specificati più di 5 gateway**</span><span class="sxs-lookup"><span data-stu-id="7b729-136">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="7b729-137">69</span><span class="sxs-lookup"><span data-stu-id="7b729-137">69</span></span>

<span data-ttu-id="7b729-138">Sono stati specificati più di cinque gateway.</span><span class="sxs-lookup"><span data-stu-id="7b729-138">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="7b729-139">**Indirizzo IP non valido**</span><span class="sxs-lookup"><span data-stu-id="7b729-139">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="7b729-140">70</span><span class="sxs-lookup"><span data-stu-id="7b729-140">70</span></span>

<span data-ttu-id="7b729-141">Indirizzo IP non valido.</span><span class="sxs-lookup"><span data-stu-id="7b729-141">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="7b729-142">**Indirizzo IP gateway non valido**</span><span class="sxs-lookup"><span data-stu-id="7b729-142">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="7b729-143">71</span><span class="sxs-lookup"><span data-stu-id="7b729-143">71</span></span>

<span data-ttu-id="7b729-144">Indirizzo IP del gateway non valido.</span><span class="sxs-lookup"><span data-stu-id="7b729-144">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="7b729-145">**Si è verificato un errore durante l'accesso al registro di sistema per le informazioni richieste**</span><span class="sxs-lookup"><span data-stu-id="7b729-145">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="7b729-146">72</span><span class="sxs-lookup"><span data-stu-id="7b729-146">72</span></span>

<span data-ttu-id="7b729-147">Si è verificato un errore durante l'accesso al registro di sistema per le informazioni richieste.</span><span class="sxs-lookup"><span data-stu-id="7b729-147">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="7b729-148">**Nome di dominio non valido**</span><span class="sxs-lookup"><span data-stu-id="7b729-148">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="7b729-149">73</span><span class="sxs-lookup"><span data-stu-id="7b729-149">73</span></span>

<span data-ttu-id="7b729-150">Nome di dominio non valido.</span><span class="sxs-lookup"><span data-stu-id="7b729-150">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="7b729-151">**Nome host non valido**</span><span class="sxs-lookup"><span data-stu-id="7b729-151">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="7b729-152">74</span><span class="sxs-lookup"><span data-stu-id="7b729-152">74</span></span>

<span data-ttu-id="7b729-153">Nome host non valido.</span><span class="sxs-lookup"><span data-stu-id="7b729-153">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="7b729-154">**Nessun server WINS primario/secondario definito**</span><span class="sxs-lookup"><span data-stu-id="7b729-154">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="7b729-155">75</span><span class="sxs-lookup"><span data-stu-id="7b729-155">75</span></span>

<span data-ttu-id="7b729-156">Nessun server WINS primario o secondario definito.</span><span class="sxs-lookup"><span data-stu-id="7b729-156">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="7b729-157">**File non valido**</span><span class="sxs-lookup"><span data-stu-id="7b729-157">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="7b729-158">76</span><span class="sxs-lookup"><span data-stu-id="7b729-158">76</span></span>

<span data-ttu-id="7b729-159">File non valido.</span><span class="sxs-lookup"><span data-stu-id="7b729-159">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="7b729-160">**Percorso di sistema non valido**</span><span class="sxs-lookup"><span data-stu-id="7b729-160">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="7b729-161">77</span><span class="sxs-lookup"><span data-stu-id="7b729-161">77</span></span>

<span data-ttu-id="7b729-162">Percorso di sistema non valido.</span><span class="sxs-lookup"><span data-stu-id="7b729-162">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="7b729-163">**Copia del file non riuscita**</span><span class="sxs-lookup"><span data-stu-id="7b729-163">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="7b729-164">78</span><span class="sxs-lookup"><span data-stu-id="7b729-164">78</span></span>

<span data-ttu-id="7b729-165">Copia del file non riuscita.</span><span class="sxs-lookup"><span data-stu-id="7b729-165">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="7b729-166">**Parametro di sicurezza non valido**</span><span class="sxs-lookup"><span data-stu-id="7b729-166">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="7b729-167">79</span><span class="sxs-lookup"><span data-stu-id="7b729-167">79</span></span>

<span data-ttu-id="7b729-168">Parametro di sicurezza non valido.</span><span class="sxs-lookup"><span data-stu-id="7b729-168">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="7b729-169">**Impossibile configurare il servizio TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="7b729-169">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="7b729-170">80</span><span class="sxs-lookup"><span data-stu-id="7b729-170">80</span></span>

<span data-ttu-id="7b729-171">Impossibile configurare il servizio TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="7b729-171">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="7b729-172">**Non è possibile configurare il servizio DHCP**</span><span class="sxs-lookup"><span data-stu-id="7b729-172">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="7b729-173">81</span><span class="sxs-lookup"><span data-stu-id="7b729-173">81</span></span>

<span data-ttu-id="7b729-174">Impossibile configurare il servizio DHCP.</span><span class="sxs-lookup"><span data-stu-id="7b729-174">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="7b729-175">**Non è possibile rinnovare il lease DHCP**</span><span class="sxs-lookup"><span data-stu-id="7b729-175">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="7b729-176">82</span><span class="sxs-lookup"><span data-stu-id="7b729-176">82</span></span>

<span data-ttu-id="7b729-177">Non è possibile rinnovare il lease DHCP.</span><span class="sxs-lookup"><span data-stu-id="7b729-177">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="7b729-178">**Non è possibile rilasciare il lease DHCP**</span><span class="sxs-lookup"><span data-stu-id="7b729-178">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="7b729-179">83</span><span class="sxs-lookup"><span data-stu-id="7b729-179">83</span></span>

<span data-ttu-id="7b729-180">Impossibile rilasciare il lease DHCP.</span><span class="sxs-lookup"><span data-stu-id="7b729-180">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="7b729-181">**IP non abilitato sulla scheda**</span><span class="sxs-lookup"><span data-stu-id="7b729-181">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="7b729-182">84</span><span class="sxs-lookup"><span data-stu-id="7b729-182">84</span></span>

<span data-ttu-id="7b729-183">IP non abilitato sulla scheda.</span><span class="sxs-lookup"><span data-stu-id="7b729-183">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="7b729-184">**IPX non abilitato sull'adapter**</span><span class="sxs-lookup"><span data-stu-id="7b729-184">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="7b729-185">85</span><span class="sxs-lookup"><span data-stu-id="7b729-185">85</span></span>

<span data-ttu-id="7b729-186">IPX non abilitato sulla scheda.</span><span class="sxs-lookup"><span data-stu-id="7b729-186">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="7b729-187">**Errore limite numero frame/rete**</span><span class="sxs-lookup"><span data-stu-id="7b729-187">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="7b729-188">86</span><span class="sxs-lookup"><span data-stu-id="7b729-188">86</span></span>

<span data-ttu-id="7b729-189">Errore dei limiti del numero di rete o del frame.</span><span class="sxs-lookup"><span data-stu-id="7b729-189">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="7b729-190">**Tipo di frame non valido**</span><span class="sxs-lookup"><span data-stu-id="7b729-190">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="7b729-191">87</span><span class="sxs-lookup"><span data-stu-id="7b729-191">87</span></span>

<span data-ttu-id="7b729-192">Tipo di frame non valido.</span><span class="sxs-lookup"><span data-stu-id="7b729-192">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="7b729-193">**Numero di rete non valido**</span><span class="sxs-lookup"><span data-stu-id="7b729-193">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="7b729-194">88</span><span class="sxs-lookup"><span data-stu-id="7b729-194">88</span></span>

<span data-ttu-id="7b729-195">Numero di rete non valido.</span><span class="sxs-lookup"><span data-stu-id="7b729-195">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="7b729-196">**Numero di rete duplicato**</span><span class="sxs-lookup"><span data-stu-id="7b729-196">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="7b729-197">89</span><span class="sxs-lookup"><span data-stu-id="7b729-197">89</span></span>

<span data-ttu-id="7b729-198">Numero di rete duplicato.</span><span class="sxs-lookup"><span data-stu-id="7b729-198">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="7b729-199">**Parametro fuori limite**</span><span class="sxs-lookup"><span data-stu-id="7b729-199">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="7b729-200">90</span><span class="sxs-lookup"><span data-stu-id="7b729-200">90</span></span>

<span data-ttu-id="7b729-201">Parametro fuori limite.</span><span class="sxs-lookup"><span data-stu-id="7b729-201">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="7b729-202">**Accesso negato**</span><span class="sxs-lookup"><span data-stu-id="7b729-202">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="7b729-203">91</span><span class="sxs-lookup"><span data-stu-id="7b729-203">91</span></span>

<span data-ttu-id="7b729-204">Accesso negato.</span><span class="sxs-lookup"><span data-stu-id="7b729-204">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="7b729-205">**Memoria insufficiente**</span><span class="sxs-lookup"><span data-stu-id="7b729-205">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="7b729-206">92</span><span class="sxs-lookup"><span data-stu-id="7b729-206">92</span></span>

<span data-ttu-id="7b729-207">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="7b729-207">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="7b729-208">**Esiste già**</span><span class="sxs-lookup"><span data-stu-id="7b729-208">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="7b729-209">93</span><span class="sxs-lookup"><span data-stu-id="7b729-209">93</span></span>

<span data-ttu-id="7b729-210">Esiste già.</span><span class="sxs-lookup"><span data-stu-id="7b729-210">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="7b729-211">**Percorso, file o oggetto non trovato**</span><span class="sxs-lookup"><span data-stu-id="7b729-211">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="7b729-212">94</span><span class="sxs-lookup"><span data-stu-id="7b729-212">94</span></span>

<span data-ttu-id="7b729-213">Il percorso, il file o l'oggetto non è stato trovato.</span><span class="sxs-lookup"><span data-stu-id="7b729-213">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="7b729-214">**Non è possibile inviare una notifica al servizio**</span><span class="sxs-lookup"><span data-stu-id="7b729-214">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="7b729-215">95</span><span class="sxs-lookup"><span data-stu-id="7b729-215">95</span></span>

<span data-ttu-id="7b729-216">Impossibile notificare il servizio.</span><span class="sxs-lookup"><span data-stu-id="7b729-216">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="7b729-217">**Non è possibile inviare una notifica al servizio DNS**</span><span class="sxs-lookup"><span data-stu-id="7b729-217">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="7b729-218">96</span><span class="sxs-lookup"><span data-stu-id="7b729-218">96</span></span>

<span data-ttu-id="7b729-219">Impossibile inviare una notifica al servizio DNS.</span><span class="sxs-lookup"><span data-stu-id="7b729-219">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="7b729-220">**Interfaccia non configurabile**</span><span class="sxs-lookup"><span data-stu-id="7b729-220">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="7b729-221">97</span><span class="sxs-lookup"><span data-stu-id="7b729-221">97</span></span>

<span data-ttu-id="7b729-222">Interfaccia non configurabile.</span><span class="sxs-lookup"><span data-stu-id="7b729-222">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="7b729-223">**Non tutti i lease DHCP possono essere rilasciati/rinnovati**</span><span class="sxs-lookup"><span data-stu-id="7b729-223">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="7b729-224">98</span><span class="sxs-lookup"><span data-stu-id="7b729-224">98</span></span>

<span data-ttu-id="7b729-225">Non tutti i lease DHCP possono essere rilasciati o rinnovati.</span><span class="sxs-lookup"><span data-stu-id="7b729-225">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="7b729-226">**DHCP non abilitato sull'adapter**</span><span class="sxs-lookup"><span data-stu-id="7b729-226">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="7b729-227">100</span><span class="sxs-lookup"><span data-stu-id="7b729-227">100</span></span>

<span data-ttu-id="7b729-228">DHCP non abilitato sulla scheda.</span><span class="sxs-lookup"><span data-stu-id="7b729-228">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="7b729-229">**Altri**</span><span class="sxs-lookup"><span data-stu-id="7b729-229">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="7b729-230">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="7b729-230">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7b729-231">Commenti</span><span class="sxs-lookup"><span data-stu-id="7b729-231">Remarks</span></span>

<span data-ttu-id="7b729-232">Per impostazione predefinita, lo stack trasmette i pacchetti in formato digitale, Intel, Xerox (DIX) Ethernet.</span><span class="sxs-lookup"><span data-stu-id="7b729-232">By default, the stack transmits packets in Digital, Intel, Xerox (DIX) Ethernet format.</span></span> <span data-ttu-id="7b729-233">Riceve sempre entrambi i formati.</span><span class="sxs-lookup"><span data-stu-id="7b729-233">It always receives both formats.</span></span>

## <a name="examples"></a><span data-ttu-id="7b729-234">Esempio</span><span class="sxs-lookup"><span data-stu-id="7b729-234">Examples</span></span>

<span data-ttu-id="7b729-235">Per configurare le schede di rete di un computer in modo da usare la codifica di SNAP 802,3 per i pacchetti Ethernet, l'esempio di codice per la [modifica delle query ARP per l'uso di EtherSNAP](https://Gallery.TechNet.Microsoft.Com/2fe24075-fdb1-486d-8c0b-d25075fd8f21) VBScript nella raccolta TechNet USA **SetArpUseEtherSNAP** .</span><span class="sxs-lookup"><span data-stu-id="7b729-235">The [Modify ARP Queries to Use EtherSNAP](https://Gallery.TechNet.Microsoft.Com/2fe24075-fdb1-486d-8c0b-d25075fd8f21) VBScript code sample on TechNet Gallery uses **SetArpUseEtherSNAP** to configure the network adapters on a computer to use 802.3 SNAP encoding for Ethernet packets.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b729-236">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7b729-236">Requirements</span></span>



| <span data-ttu-id="7b729-237">Requisito</span><span class="sxs-lookup"><span data-stu-id="7b729-237">Requirement</span></span> | <span data-ttu-id="7b729-238">Valore</span><span class="sxs-lookup"><span data-stu-id="7b729-238">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7b729-239">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7b729-239">Minimum supported client</span></span><br/> | <span data-ttu-id="7b729-240">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7b729-240">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7b729-241">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7b729-241">Minimum supported server</span></span><br/> | <span data-ttu-id="7b729-242">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7b729-242">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7b729-243">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="7b729-243">Namespace</span></span><br/>                | <span data-ttu-id="7b729-244">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="7b729-244">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="7b729-245">MOF</span><span class="sxs-lookup"><span data-stu-id="7b729-245">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7b729-246"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7b729-246"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="7b729-247">DLL</span><span class="sxs-lookup"><span data-stu-id="7b729-247">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7b729-248"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7b729-248"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b729-249">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7b729-249">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b729-250">Classi hardware del sistema del computer</span><span class="sxs-lookup"><span data-stu-id="7b729-250">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="7b729-251">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="7b729-251">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="7b729-252">Attività WMI: rete</span><span class="sxs-lookup"><span data-stu-id="7b729-252">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="7b729-253">Attività WMI: account e domini</span><span class="sxs-lookup"><span data-stu-id="7b729-253">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="7b729-254">Supporto di IPv6 e IPv4 in WMI</span><span class="sxs-lookup"><span data-stu-id="7b729-254">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

