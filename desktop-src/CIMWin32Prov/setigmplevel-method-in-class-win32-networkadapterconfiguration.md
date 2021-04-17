---
description: Il metodo statico della classe WMI SetIGMPLevel viene usato per impostare la misura in cui il sistema supporta il multicast IP e fa parte del protocollo di gestione dei gruppi Internet.
ms.assetid: 38877576-aa23-4841-b3ae-1a02bfdd70d8
ms.tgt_platform: multiple
title: Metodo SetIGMPLevel della classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetIGMPLevel
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 97ead4df1d45b110c3d0a91976dc8eca6ffd72c7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523786"
---
# <a name="setigmplevel-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="ebb8b-103">Metodo SetIGMPLevel della \_ classe NetworkAdapterConfiguration Win32</span><span class="sxs-lookup"><span data-stu-id="ebb8b-103">SetIGMPLevel method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="ebb8b-104">Il metodo statico della [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetIGMPLevel** viene usato per impostare la misura in cui il sistema supporta il multicast IP e fa parte del protocollo di gestione dei gruppi Internet.</span><span class="sxs-lookup"><span data-stu-id="ebb8b-104">The **SetIGMPLevel** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to set the extent to which the system supports IP multicasting and participates in the Internet Group Management Protocol.</span></span>

<span data-ttu-id="ebb8b-105">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="ebb8b-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="ebb8b-106">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="ebb8b-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="ebb8b-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ebb8b-107">Syntax</span></span>


```mof
uint32 SetIGMPLevel(
  [in] uint8 IGMPLevel
);
```



## <a name="parameters"></a><span data-ttu-id="ebb8b-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="ebb8b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ebb8b-109">*IGMPLevel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ebb8b-109">*IGMPLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ebb8b-110">Tipo di dati: **Integer**</span><span class="sxs-lookup"><span data-stu-id="ebb8b-110">Data type: **Integer**</span></span>

<span data-ttu-id="ebb8b-111">Imposta il livello in cui il sistema supporta il multicast IP e partecipa al protocollo di gestione dei gruppi Internet.</span><span class="sxs-lookup"><span data-stu-id="ebb8b-111">Sets the level at which the system supports IP multicast and participates in the Internet Group Management Protocol.</span></span> <span data-ttu-id="ebb8b-112">Al livello 0, il sistema non fornisce alcun supporto per il multicast.</span><span class="sxs-lookup"><span data-stu-id="ebb8b-112">At level 0, the system provides no multicast support.</span></span> <span data-ttu-id="ebb8b-113">Al livello 1, il sistema può inviare solo pacchetti multicast IP.</span><span class="sxs-lookup"><span data-stu-id="ebb8b-113">At level 1, the system may only send IP multicast packets.</span></span> <span data-ttu-id="ebb8b-114">Al livello 2, il sistema può inviare pacchetti multicast IP e partecipare completamente a IGMP per ricevere pacchetti multicast.</span><span class="sxs-lookup"><span data-stu-id="ebb8b-114">At level 2, the system may send IP multicast packets and fully participate in IGMP to receive multicast packets.</span></span>

<dt>

<span id="No_Multicast"></span><span id="no_multicast"></span><span id="NO_MULTICAST"></span>

<span data-ttu-id="ebb8b-115">**Nessun multicast** (0)</span><span class="sxs-lookup"><span data-stu-id="ebb8b-115">**No Multicast** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="IP_Multicast"></span><span id="ip_multicast"></span><span id="IP_MULTICAST"></span>

<span data-ttu-id="ebb8b-116">**Multicast IP** (1)</span><span class="sxs-lookup"><span data-stu-id="ebb8b-116">**IP Multicast** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="IP___IGMP_multicast"></span><span id="ip___igmp_multicast"></span><span id="IP___IGMP_MULTICAST"></span>

<span data-ttu-id="ebb8b-117">**Multicast IP & IGMP** (2)</span><span class="sxs-lookup"><span data-stu-id="ebb8b-117">**IP & IGMP multicast** (2)</span></span>


<span data-ttu-id="ebb8b-118"></dt> <dd></dd> </dl> </dd> </dl></span><span class="sxs-lookup"><span data-stu-id="ebb8b-118"></dt> <dd></dd> </dl> </dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="ebb8b-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ebb8b-119">Return value</span></span>

<span data-ttu-id="ebb8b-120">Restituisce un valore pari a 0 (zero) per un completamento corretto quando non è richiesto il riavvio, 1 (uno) per un completamento corretto quando è necessario un riavvio e un numero diverso se si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="ebb8b-120">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="ebb8b-121">Per ulteriori informazioni sui codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="ebb8b-121">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="ebb8b-122">Per i valori **HRESULT** generali, vedere [codici di errore di sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="ebb8b-122">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="ebb8b-123">**Operazione completata, non è necessario riavviare il computer**</span><span class="sxs-lookup"><span data-stu-id="ebb8b-123">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="ebb8b-124">0</span><span class="sxs-lookup"><span data-stu-id="ebb8b-124">0</span></span>

<span data-ttu-id="ebb8b-125">Operazione completata, non è necessario riavviare il computer.</span><span class="sxs-lookup"><span data-stu-id="ebb8b-125">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="ebb8b-126">**Operazione completata, riavvio richiesto**</span><span class="sxs-lookup"><span data-stu-id="ebb8b-126">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="ebb8b-127">1</span><span class="sxs-lookup"><span data-stu-id="ebb8b-127">1</span></span>

<span data-ttu-id="ebb8b-128">Operazione completata, è necessario riavviare il computer.</span><span class="sxs-lookup"><span data-stu-id="ebb8b-128">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="ebb8b-129">**Metodo non supportato in questa piattaforma**</span><span class="sxs-lookup"><span data-stu-id="ebb8b-129">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="ebb8b-130">64</span><span class="sxs-lookup"><span data-stu-id="ebb8b-130">64</span></span>

<span data-ttu-id="ebb8b-131">Metodo non supportato in questa piattaforma.</span><span class="sxs-lookup"><span data-stu-id="ebb8b-131">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="ebb8b-132">**Errore sconosciuto**</span><span class="sxs-lookup"><span data-stu-id="ebb8b-132">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="ebb8b-133">65</span><span class="sxs-lookup"><span data-stu-id="ebb8b-133">65</span></span>

<span data-ttu-id="ebb8b-134">Errore sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="ebb8b-134">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="ebb8b-135">**subnet mask non valido**</span><span class="sxs-lookup"><span data-stu-id="ebb8b-135">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="ebb8b-136">66</span><span class="sxs-lookup"><span data-stu-id="ebb8b-136">66</span></span>

<span data-ttu-id="ebb8b-137">Subnet mask non valido.</span><span class="sxs-lookup"><span data-stu-id="ebb8b-137">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="ebb8b-138">**Si è verificato un errore durante l'elaborazione di un'istanza restituita**</span><span class="sxs-lookup"><span data-stu-id="ebb8b-138">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="ebb8b-139">67</span><span class="sxs-lookup"><span data-stu-id="ebb8b-139">67</span></span>

<span data-ttu-id="ebb8b-140">Si è verificato un errore durante l'elaborazione di un'istanza di restituita.</span><span class="sxs-lookup"><span data-stu-id="ebb8b-140">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="ebb8b-141">**Parametro di input non valido**</span><span class="sxs-lookup"><span data-stu-id="ebb8b-141">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="ebb8b-142">68</span><span class="sxs-lookup"><span data-stu-id="ebb8b-142">68</span></span>

<span data-ttu-id="ebb8b-143">Parametro di input non valido.</span><span class="sxs-lookup"><span data-stu-id="ebb8b-143">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="ebb8b-144">**Sono stati specificati più di 5 gateway**</span><span class="sxs-lookup"><span data-stu-id="ebb8b-144">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="ebb8b-145">69</span><span class="sxs-lookup"><span data-stu-id="ebb8b-145">69</span></span>

<span data-ttu-id="ebb8b-146">Sono stati specificati più di cinque gateway.</span><span class="sxs-lookup"><span data-stu-id="ebb8b-146">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="ebb8b-147">**Indirizzo IP non valido**</span><span class="sxs-lookup"><span data-stu-id="ebb8b-147">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="ebb8b-148">70</span><span class="sxs-lookup"><span data-stu-id="ebb8b-148">70</span></span>

<span data-ttu-id="ebb8b-149">Indirizzo IP non valido.</span><span class="sxs-lookup"><span data-stu-id="ebb8b-149">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="ebb8b-150">**Indirizzo IP gateway non valido**</span><span class="sxs-lookup"><span data-stu-id="ebb8b-150">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="ebb8b-151">71</span><span class="sxs-lookup"><span data-stu-id="ebb8b-151">71</span></span>

<span data-ttu-id="ebb8b-152">Indirizzo IP del gateway non valido.</span><span class="sxs-lookup"><span data-stu-id="ebb8b-152">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="ebb8b-153">**Si è verificato un errore durante l'accesso al registro di sistema per le informazioni richieste**</span><span class="sxs-lookup"><span data-stu-id="ebb8b-153">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="ebb8b-154">72</span><span class="sxs-lookup"><span data-stu-id="ebb8b-154">72</span></span>

<span data-ttu-id="ebb8b-155">Si è verificato un errore durante l'accesso al registro di sistema per le informazioni richieste.</span><span class="sxs-lookup"><span data-stu-id="ebb8b-155">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="ebb8b-156">**Nome di dominio non valido**</span><span class="sxs-lookup"><span data-stu-id="ebb8b-156">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="ebb8b-157">73</span><span class="sxs-lookup"><span data-stu-id="ebb8b-157">73</span></span>

<span data-ttu-id="ebb8b-158">Nome di dominio non valido.</span><span class="sxs-lookup"><span data-stu-id="ebb8b-158">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="ebb8b-159">**Nome host non valido**</span><span class="sxs-lookup"><span data-stu-id="ebb8b-159">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="ebb8b-160">74</span><span class="sxs-lookup"><span data-stu-id="ebb8b-160">74</span></span>

<span data-ttu-id="ebb8b-161">Nome host non valido.</span><span class="sxs-lookup"><span data-stu-id="ebb8b-161">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="ebb8b-162">**Nessun server WINS primario/secondario definito**</span><span class="sxs-lookup"><span data-stu-id="ebb8b-162">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="ebb8b-163">75</span><span class="sxs-lookup"><span data-stu-id="ebb8b-163">75</span></span>

<span data-ttu-id="ebb8b-164">Nessun server WINS primario o secondario definito.</span><span class="sxs-lookup"><span data-stu-id="ebb8b-164">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="ebb8b-165">**File non valido**</span><span class="sxs-lookup"><span data-stu-id="ebb8b-165">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="ebb8b-166">76</span><span class="sxs-lookup"><span data-stu-id="ebb8b-166">76</span></span>

<span data-ttu-id="ebb8b-167">File non valido.</span><span class="sxs-lookup"><span data-stu-id="ebb8b-167">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="ebb8b-168">**Percorso di sistema non valido**</span><span class="sxs-lookup"><span data-stu-id="ebb8b-168">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="ebb8b-169">77</span><span class="sxs-lookup"><span data-stu-id="ebb8b-169">77</span></span>

<span data-ttu-id="ebb8b-170">Percorso di sistema non valido.</span><span class="sxs-lookup"><span data-stu-id="ebb8b-170">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="ebb8b-171">**Copia del file non riuscita**</span><span class="sxs-lookup"><span data-stu-id="ebb8b-171">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="ebb8b-172">78</span><span class="sxs-lookup"><span data-stu-id="ebb8b-172">78</span></span>

<span data-ttu-id="ebb8b-173">Copia del file non riuscita.</span><span class="sxs-lookup"><span data-stu-id="ebb8b-173">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="ebb8b-174">**Parametro di sicurezza non valido**</span><span class="sxs-lookup"><span data-stu-id="ebb8b-174">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="ebb8b-175">79</span><span class="sxs-lookup"><span data-stu-id="ebb8b-175">79</span></span>

<span data-ttu-id="ebb8b-176">Parametro di sicurezza non valido.</span><span class="sxs-lookup"><span data-stu-id="ebb8b-176">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="ebb8b-177">**Impossibile configurare il servizio TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="ebb8b-177">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="ebb8b-178">80</span><span class="sxs-lookup"><span data-stu-id="ebb8b-178">80</span></span>

<span data-ttu-id="ebb8b-179">Impossibile configurare il servizio TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="ebb8b-179">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="ebb8b-180">**Non è possibile configurare il servizio DHCP**</span><span class="sxs-lookup"><span data-stu-id="ebb8b-180">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="ebb8b-181">81</span><span class="sxs-lookup"><span data-stu-id="ebb8b-181">81</span></span>

<span data-ttu-id="ebb8b-182">Impossibile configurare il servizio DHCP.</span><span class="sxs-lookup"><span data-stu-id="ebb8b-182">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="ebb8b-183">**Non è possibile rinnovare il lease DHCP**</span><span class="sxs-lookup"><span data-stu-id="ebb8b-183">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="ebb8b-184">82</span><span class="sxs-lookup"><span data-stu-id="ebb8b-184">82</span></span>

<span data-ttu-id="ebb8b-185">Non è possibile rinnovare il lease DHCP.</span><span class="sxs-lookup"><span data-stu-id="ebb8b-185">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="ebb8b-186">**Non è possibile rilasciare il lease DHCP**</span><span class="sxs-lookup"><span data-stu-id="ebb8b-186">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="ebb8b-187">83</span><span class="sxs-lookup"><span data-stu-id="ebb8b-187">83</span></span>

<span data-ttu-id="ebb8b-188">Impossibile rilasciare il lease DHCP.</span><span class="sxs-lookup"><span data-stu-id="ebb8b-188">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="ebb8b-189">**IP non abilitato sulla scheda**</span><span class="sxs-lookup"><span data-stu-id="ebb8b-189">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="ebb8b-190">84</span><span class="sxs-lookup"><span data-stu-id="ebb8b-190">84</span></span>

<span data-ttu-id="ebb8b-191">IP non abilitato sulla scheda.</span><span class="sxs-lookup"><span data-stu-id="ebb8b-191">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="ebb8b-192">**IPX non abilitato sull'adapter**</span><span class="sxs-lookup"><span data-stu-id="ebb8b-192">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="ebb8b-193">85</span><span class="sxs-lookup"><span data-stu-id="ebb8b-193">85</span></span>

<span data-ttu-id="ebb8b-194">IPX non abilitato sulla scheda.</span><span class="sxs-lookup"><span data-stu-id="ebb8b-194">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="ebb8b-195">**Errore limite numero frame/rete**</span><span class="sxs-lookup"><span data-stu-id="ebb8b-195">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="ebb8b-196">86</span><span class="sxs-lookup"><span data-stu-id="ebb8b-196">86</span></span>

<span data-ttu-id="ebb8b-197">Errore dei limiti del numero di rete o del frame.</span><span class="sxs-lookup"><span data-stu-id="ebb8b-197">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="ebb8b-198">**Tipo di frame non valido**</span><span class="sxs-lookup"><span data-stu-id="ebb8b-198">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="ebb8b-199">87</span><span class="sxs-lookup"><span data-stu-id="ebb8b-199">87</span></span>

<span data-ttu-id="ebb8b-200">Tipo di frame non valido.</span><span class="sxs-lookup"><span data-stu-id="ebb8b-200">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="ebb8b-201">**Numero di rete non valido**</span><span class="sxs-lookup"><span data-stu-id="ebb8b-201">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="ebb8b-202">88</span><span class="sxs-lookup"><span data-stu-id="ebb8b-202">88</span></span>

<span data-ttu-id="ebb8b-203">Numero di rete non valido.</span><span class="sxs-lookup"><span data-stu-id="ebb8b-203">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="ebb8b-204">**Numero di rete duplicato**</span><span class="sxs-lookup"><span data-stu-id="ebb8b-204">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="ebb8b-205">89</span><span class="sxs-lookup"><span data-stu-id="ebb8b-205">89</span></span>

<span data-ttu-id="ebb8b-206">Numero di rete duplicato.</span><span class="sxs-lookup"><span data-stu-id="ebb8b-206">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="ebb8b-207">**Parametro fuori limite**</span><span class="sxs-lookup"><span data-stu-id="ebb8b-207">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="ebb8b-208">90</span><span class="sxs-lookup"><span data-stu-id="ebb8b-208">90</span></span>

<span data-ttu-id="ebb8b-209">Parametro fuori limite.</span><span class="sxs-lookup"><span data-stu-id="ebb8b-209">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="ebb8b-210">**Accesso negato**</span><span class="sxs-lookup"><span data-stu-id="ebb8b-210">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="ebb8b-211">91</span><span class="sxs-lookup"><span data-stu-id="ebb8b-211">91</span></span>

<span data-ttu-id="ebb8b-212">Accesso negato.</span><span class="sxs-lookup"><span data-stu-id="ebb8b-212">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="ebb8b-213">**Memoria insufficiente**</span><span class="sxs-lookup"><span data-stu-id="ebb8b-213">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="ebb8b-214">92</span><span class="sxs-lookup"><span data-stu-id="ebb8b-214">92</span></span>

<span data-ttu-id="ebb8b-215">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="ebb8b-215">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="ebb8b-216">**Esiste già**</span><span class="sxs-lookup"><span data-stu-id="ebb8b-216">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="ebb8b-217">93</span><span class="sxs-lookup"><span data-stu-id="ebb8b-217">93</span></span>

<span data-ttu-id="ebb8b-218">Esiste già.</span><span class="sxs-lookup"><span data-stu-id="ebb8b-218">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="ebb8b-219">**Percorso, file o oggetto non trovato**</span><span class="sxs-lookup"><span data-stu-id="ebb8b-219">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="ebb8b-220">94</span><span class="sxs-lookup"><span data-stu-id="ebb8b-220">94</span></span>

<span data-ttu-id="ebb8b-221">Il percorso, il file o l'oggetto non è stato trovato.</span><span class="sxs-lookup"><span data-stu-id="ebb8b-221">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="ebb8b-222">**Non è possibile inviare una notifica al servizio**</span><span class="sxs-lookup"><span data-stu-id="ebb8b-222">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="ebb8b-223">95</span><span class="sxs-lookup"><span data-stu-id="ebb8b-223">95</span></span>

<span data-ttu-id="ebb8b-224">Impossibile notificare il servizio.</span><span class="sxs-lookup"><span data-stu-id="ebb8b-224">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="ebb8b-225">**Non è possibile inviare una notifica al servizio DNS**</span><span class="sxs-lookup"><span data-stu-id="ebb8b-225">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="ebb8b-226">96</span><span class="sxs-lookup"><span data-stu-id="ebb8b-226">96</span></span>

<span data-ttu-id="ebb8b-227">Impossibile inviare una notifica al servizio DNS.</span><span class="sxs-lookup"><span data-stu-id="ebb8b-227">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="ebb8b-228">**Interfaccia non configurabile**</span><span class="sxs-lookup"><span data-stu-id="ebb8b-228">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="ebb8b-229">97</span><span class="sxs-lookup"><span data-stu-id="ebb8b-229">97</span></span>

<span data-ttu-id="ebb8b-230">Interfaccia non configurabile.</span><span class="sxs-lookup"><span data-stu-id="ebb8b-230">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="ebb8b-231">**Non tutti i lease DHCP possono essere rilasciati/rinnovati**</span><span class="sxs-lookup"><span data-stu-id="ebb8b-231">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="ebb8b-232">98</span><span class="sxs-lookup"><span data-stu-id="ebb8b-232">98</span></span>

<span data-ttu-id="ebb8b-233">Non tutti i lease DHCP possono essere rilasciati o rinnovati.</span><span class="sxs-lookup"><span data-stu-id="ebb8b-233">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="ebb8b-234">**DHCP non abilitato sull'adapter**</span><span class="sxs-lookup"><span data-stu-id="ebb8b-234">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="ebb8b-235">100</span><span class="sxs-lookup"><span data-stu-id="ebb8b-235">100</span></span>

<span data-ttu-id="ebb8b-236">DHCP non abilitato sulla scheda.</span><span class="sxs-lookup"><span data-stu-id="ebb8b-236">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="ebb8b-237">**Altri**</span><span class="sxs-lookup"><span data-stu-id="ebb8b-237">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="ebb8b-238">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="ebb8b-238">101 4294967295</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="ebb8b-239">Esempio</span><span class="sxs-lookup"><span data-stu-id="ebb8b-239">Examples</span></span>

<span data-ttu-id="ebb8b-240">L'esempio [Modify the IGMP level for all Network Adapters](https://Gallery.TechNet.Microsoft.Com/b92f894c-5cf8-4484-b5f0-d54761bacd5c) VBScript Disabilita il multicast IGMP in un computer.</span><span class="sxs-lookup"><span data-stu-id="ebb8b-240">The [Modify the IGMP Level for All Network Adapters](https://Gallery.TechNet.Microsoft.Com/b92f894c-5cf8-4484-b5f0-d54761bacd5c) VBScript sample disables IGMP multicasting on a computer.</span></span>

## <a name="requirements"></a><span data-ttu-id="ebb8b-241">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ebb8b-241">Requirements</span></span>



| <span data-ttu-id="ebb8b-242">Requisito</span><span class="sxs-lookup"><span data-stu-id="ebb8b-242">Requirement</span></span> | <span data-ttu-id="ebb8b-243">Valore</span><span class="sxs-lookup"><span data-stu-id="ebb8b-243">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ebb8b-244">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ebb8b-244">Minimum supported client</span></span><br/> | <span data-ttu-id="ebb8b-245">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ebb8b-245">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ebb8b-246">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ebb8b-246">Minimum supported server</span></span><br/> | <span data-ttu-id="ebb8b-247">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ebb8b-247">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ebb8b-248">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ebb8b-248">Namespace</span></span><br/>                | <span data-ttu-id="ebb8b-249">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="ebb8b-249">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ebb8b-250">MOF</span><span class="sxs-lookup"><span data-stu-id="ebb8b-250">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ebb8b-251"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ebb8b-251"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ebb8b-252">DLL</span><span class="sxs-lookup"><span data-stu-id="ebb8b-252">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ebb8b-253"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ebb8b-253"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ebb8b-254">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ebb8b-254">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebb8b-255">Classi hardware del sistema del computer</span><span class="sxs-lookup"><span data-stu-id="ebb8b-255">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="ebb8b-256">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="ebb8b-256">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="ebb8b-257">Attività WMI: rete</span><span class="sxs-lookup"><span data-stu-id="ebb8b-257">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="ebb8b-258">Attività WMI: account e domini</span><span class="sxs-lookup"><span data-stu-id="ebb8b-258">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="ebb8b-259">Supporto di IPv6 e IPv4 in WMI</span><span class="sxs-lookup"><span data-stu-id="ebb8b-259">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

