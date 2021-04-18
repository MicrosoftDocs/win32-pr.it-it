---
description: Il metodo statico della classe WMI RenewDHCPLeaseAll rinnova gli indirizzi IP in tutte le schede di rete abilitate per DHCP.
ms.assetid: cbe0a607-cb3b-47c4-ad3a-c4fa03fe688c
ms.tgt_platform: multiple
title: Metodo RenewDHCPLeaseAll della classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.RenewDHCPLeaseAll
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a3ed94b44a629f619617186415ed3822387c6967
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305284"
---
# <a name="renewdhcpleaseall-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="bcd9c-103">Metodo RenewDHCPLeaseAll della \_ classe NetworkAdapterConfiguration Win32</span><span class="sxs-lookup"><span data-stu-id="bcd9c-103">RenewDHCPLeaseAll method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="bcd9c-104">Il metodo statico della [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **RenewDHCPLeaseAll** rinnova gli indirizzi IP in tutte le schede di rete abilitate per DHCP.</span><span class="sxs-lookup"><span data-stu-id="bcd9c-104">The **RenewDHCPLeaseAll** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method renews the IP addresses on all DHCP-enabled network adapters.</span></span>

<span data-ttu-id="bcd9c-105">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="bcd9c-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="bcd9c-106">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="bcd9c-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="bcd9c-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bcd9c-107">Syntax</span></span>


```mof
uint32 RenewDHCPLeaseAll();
```



## <a name="parameters"></a><span data-ttu-id="bcd9c-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="bcd9c-108">Parameters</span></span>

<span data-ttu-id="bcd9c-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="bcd9c-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="bcd9c-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bcd9c-110">Return value</span></span>

<span data-ttu-id="bcd9c-111">Restituisce un valore pari a 0 (zero) per un completamento corretto quando non è richiesto il riavvio, 1 (uno) per un completamento corretto quando è necessario un riavvio e un numero diverso se si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="bcd9c-111">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="bcd9c-112">Per ulteriori informazioni sui codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="bcd9c-112">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="bcd9c-113">Per i valori **HRESULT** generali, vedere [codici di errore di sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="bcd9c-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="bcd9c-114">**Operazione completata, non è necessario riavviare il computer**</span><span class="sxs-lookup"><span data-stu-id="bcd9c-114">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="bcd9c-115">0</span><span class="sxs-lookup"><span data-stu-id="bcd9c-115">0</span></span>

<span data-ttu-id="bcd9c-116">Operazione completata, non è necessario riavviare il computer.</span><span class="sxs-lookup"><span data-stu-id="bcd9c-116">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="bcd9c-117">**Operazione completata, riavvio richiesto**</span><span class="sxs-lookup"><span data-stu-id="bcd9c-117">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="bcd9c-118">1</span><span class="sxs-lookup"><span data-stu-id="bcd9c-118">1</span></span>

<span data-ttu-id="bcd9c-119">Operazione completata, è necessario riavviare il computer.</span><span class="sxs-lookup"><span data-stu-id="bcd9c-119">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="bcd9c-120">**Metodo non supportato in questa piattaforma**</span><span class="sxs-lookup"><span data-stu-id="bcd9c-120">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="bcd9c-121">64</span><span class="sxs-lookup"><span data-stu-id="bcd9c-121">64</span></span>

<span data-ttu-id="bcd9c-122">Metodo non supportato in questa piattaforma.</span><span class="sxs-lookup"><span data-stu-id="bcd9c-122">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="bcd9c-123">**Errore sconosciuto**</span><span class="sxs-lookup"><span data-stu-id="bcd9c-123">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="bcd9c-124">65</span><span class="sxs-lookup"><span data-stu-id="bcd9c-124">65</span></span>

<span data-ttu-id="bcd9c-125">Errore sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="bcd9c-125">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="bcd9c-126">**subnet mask non valido**</span><span class="sxs-lookup"><span data-stu-id="bcd9c-126">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="bcd9c-127">66</span><span class="sxs-lookup"><span data-stu-id="bcd9c-127">66</span></span>

<span data-ttu-id="bcd9c-128">Subnet mask non valido.</span><span class="sxs-lookup"><span data-stu-id="bcd9c-128">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="bcd9c-129">**Si è verificato un errore durante l'elaborazione di un'istanza restituita**</span><span class="sxs-lookup"><span data-stu-id="bcd9c-129">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="bcd9c-130">67</span><span class="sxs-lookup"><span data-stu-id="bcd9c-130">67</span></span>

<span data-ttu-id="bcd9c-131">Si è verificato un errore durante l'elaborazione di un'istanza di restituita.</span><span class="sxs-lookup"><span data-stu-id="bcd9c-131">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="bcd9c-132">**Parametro di input non valido**</span><span class="sxs-lookup"><span data-stu-id="bcd9c-132">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="bcd9c-133">68</span><span class="sxs-lookup"><span data-stu-id="bcd9c-133">68</span></span>

<span data-ttu-id="bcd9c-134">Parametro di input non valido.</span><span class="sxs-lookup"><span data-stu-id="bcd9c-134">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="bcd9c-135">**Sono stati specificati più di 5 gateway**</span><span class="sxs-lookup"><span data-stu-id="bcd9c-135">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="bcd9c-136">69</span><span class="sxs-lookup"><span data-stu-id="bcd9c-136">69</span></span>

<span data-ttu-id="bcd9c-137">Sono stati specificati più di cinque gateway.</span><span class="sxs-lookup"><span data-stu-id="bcd9c-137">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="bcd9c-138">**Indirizzo IP non valido**</span><span class="sxs-lookup"><span data-stu-id="bcd9c-138">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="bcd9c-139">70</span><span class="sxs-lookup"><span data-stu-id="bcd9c-139">70</span></span>

<span data-ttu-id="bcd9c-140">Indirizzo IP non valido.</span><span class="sxs-lookup"><span data-stu-id="bcd9c-140">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="bcd9c-141">**Indirizzo IP gateway non valido**</span><span class="sxs-lookup"><span data-stu-id="bcd9c-141">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="bcd9c-142">71</span><span class="sxs-lookup"><span data-stu-id="bcd9c-142">71</span></span>

<span data-ttu-id="bcd9c-143">Indirizzo IP del gateway non valido.</span><span class="sxs-lookup"><span data-stu-id="bcd9c-143">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="bcd9c-144">**Si è verificato un errore durante l'accesso al registro di sistema per le informazioni richieste**</span><span class="sxs-lookup"><span data-stu-id="bcd9c-144">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="bcd9c-145">72</span><span class="sxs-lookup"><span data-stu-id="bcd9c-145">72</span></span>

<span data-ttu-id="bcd9c-146">Si è verificato un errore durante l'accesso al registro di sistema per le informazioni richieste.</span><span class="sxs-lookup"><span data-stu-id="bcd9c-146">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="bcd9c-147">**Nome di dominio non valido**</span><span class="sxs-lookup"><span data-stu-id="bcd9c-147">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="bcd9c-148">73</span><span class="sxs-lookup"><span data-stu-id="bcd9c-148">73</span></span>

<span data-ttu-id="bcd9c-149">Nome di dominio non valido.</span><span class="sxs-lookup"><span data-stu-id="bcd9c-149">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="bcd9c-150">**Nome host non valido**</span><span class="sxs-lookup"><span data-stu-id="bcd9c-150">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="bcd9c-151">74</span><span class="sxs-lookup"><span data-stu-id="bcd9c-151">74</span></span>

<span data-ttu-id="bcd9c-152">Nome host non valido.</span><span class="sxs-lookup"><span data-stu-id="bcd9c-152">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="bcd9c-153">**Nessun server WINS primario/secondario definito**</span><span class="sxs-lookup"><span data-stu-id="bcd9c-153">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="bcd9c-154">75</span><span class="sxs-lookup"><span data-stu-id="bcd9c-154">75</span></span>

<span data-ttu-id="bcd9c-155">Nessun server WINS primario o secondario definito.</span><span class="sxs-lookup"><span data-stu-id="bcd9c-155">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="bcd9c-156">**File non valido**</span><span class="sxs-lookup"><span data-stu-id="bcd9c-156">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="bcd9c-157">76</span><span class="sxs-lookup"><span data-stu-id="bcd9c-157">76</span></span>

<span data-ttu-id="bcd9c-158">File non valido.</span><span class="sxs-lookup"><span data-stu-id="bcd9c-158">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="bcd9c-159">**Percorso di sistema non valido**</span><span class="sxs-lookup"><span data-stu-id="bcd9c-159">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="bcd9c-160">77</span><span class="sxs-lookup"><span data-stu-id="bcd9c-160">77</span></span>

<span data-ttu-id="bcd9c-161">Percorso di sistema non valido.</span><span class="sxs-lookup"><span data-stu-id="bcd9c-161">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="bcd9c-162">**Copia del file non riuscita**</span><span class="sxs-lookup"><span data-stu-id="bcd9c-162">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="bcd9c-163">78</span><span class="sxs-lookup"><span data-stu-id="bcd9c-163">78</span></span>

<span data-ttu-id="bcd9c-164">Copia del file non riuscita.</span><span class="sxs-lookup"><span data-stu-id="bcd9c-164">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="bcd9c-165">**Parametro di sicurezza non valido**</span><span class="sxs-lookup"><span data-stu-id="bcd9c-165">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="bcd9c-166">79</span><span class="sxs-lookup"><span data-stu-id="bcd9c-166">79</span></span>

<span data-ttu-id="bcd9c-167">Parametro di sicurezza non valido.</span><span class="sxs-lookup"><span data-stu-id="bcd9c-167">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="bcd9c-168">**Impossibile configurare il servizio TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="bcd9c-168">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="bcd9c-169">80</span><span class="sxs-lookup"><span data-stu-id="bcd9c-169">80</span></span>

<span data-ttu-id="bcd9c-170">Impossibile configurare il servizio TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="bcd9c-170">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="bcd9c-171">**Non è possibile configurare il servizio DHCP**</span><span class="sxs-lookup"><span data-stu-id="bcd9c-171">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="bcd9c-172">81</span><span class="sxs-lookup"><span data-stu-id="bcd9c-172">81</span></span>

<span data-ttu-id="bcd9c-173">Impossibile configurare il servizio DHCP.</span><span class="sxs-lookup"><span data-stu-id="bcd9c-173">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="bcd9c-174">**Non è possibile rinnovare il lease DHCP**</span><span class="sxs-lookup"><span data-stu-id="bcd9c-174">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="bcd9c-175">82</span><span class="sxs-lookup"><span data-stu-id="bcd9c-175">82</span></span>

<span data-ttu-id="bcd9c-176">Non è possibile rinnovare il lease DHCP.</span><span class="sxs-lookup"><span data-stu-id="bcd9c-176">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="bcd9c-177">**Non è possibile rilasciare il lease DHCP**</span><span class="sxs-lookup"><span data-stu-id="bcd9c-177">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="bcd9c-178">83</span><span class="sxs-lookup"><span data-stu-id="bcd9c-178">83</span></span>

<span data-ttu-id="bcd9c-179">Impossibile rilasciare il lease DHCP.</span><span class="sxs-lookup"><span data-stu-id="bcd9c-179">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="bcd9c-180">**IP non abilitato sulla scheda**</span><span class="sxs-lookup"><span data-stu-id="bcd9c-180">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="bcd9c-181">84</span><span class="sxs-lookup"><span data-stu-id="bcd9c-181">84</span></span>

<span data-ttu-id="bcd9c-182">IP non abilitato sulla scheda.</span><span class="sxs-lookup"><span data-stu-id="bcd9c-182">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="bcd9c-183">**IPX non abilitato sull'adapter**</span><span class="sxs-lookup"><span data-stu-id="bcd9c-183">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="bcd9c-184">85</span><span class="sxs-lookup"><span data-stu-id="bcd9c-184">85</span></span>

<span data-ttu-id="bcd9c-185">IPX non abilitato sulla scheda.</span><span class="sxs-lookup"><span data-stu-id="bcd9c-185">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="bcd9c-186">**Errore limite numero frame/rete**</span><span class="sxs-lookup"><span data-stu-id="bcd9c-186">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="bcd9c-187">86</span><span class="sxs-lookup"><span data-stu-id="bcd9c-187">86</span></span>

<span data-ttu-id="bcd9c-188">Errore dei limiti del numero di rete o del frame.</span><span class="sxs-lookup"><span data-stu-id="bcd9c-188">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="bcd9c-189">**Tipo di frame non valido**</span><span class="sxs-lookup"><span data-stu-id="bcd9c-189">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="bcd9c-190">87</span><span class="sxs-lookup"><span data-stu-id="bcd9c-190">87</span></span>

<span data-ttu-id="bcd9c-191">Tipo di frame non valido.</span><span class="sxs-lookup"><span data-stu-id="bcd9c-191">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="bcd9c-192">**Numero di rete non valido**</span><span class="sxs-lookup"><span data-stu-id="bcd9c-192">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="bcd9c-193">88</span><span class="sxs-lookup"><span data-stu-id="bcd9c-193">88</span></span>

<span data-ttu-id="bcd9c-194">Numero di rete non valido.</span><span class="sxs-lookup"><span data-stu-id="bcd9c-194">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="bcd9c-195">**Numero di rete duplicato**</span><span class="sxs-lookup"><span data-stu-id="bcd9c-195">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="bcd9c-196">89</span><span class="sxs-lookup"><span data-stu-id="bcd9c-196">89</span></span>

<span data-ttu-id="bcd9c-197">Numero di rete duplicato.</span><span class="sxs-lookup"><span data-stu-id="bcd9c-197">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="bcd9c-198">**Parametro fuori limite**</span><span class="sxs-lookup"><span data-stu-id="bcd9c-198">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="bcd9c-199">90</span><span class="sxs-lookup"><span data-stu-id="bcd9c-199">90</span></span>

<span data-ttu-id="bcd9c-200">Parametro fuori limite.</span><span class="sxs-lookup"><span data-stu-id="bcd9c-200">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="bcd9c-201">**Accesso negato**</span><span class="sxs-lookup"><span data-stu-id="bcd9c-201">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="bcd9c-202">91</span><span class="sxs-lookup"><span data-stu-id="bcd9c-202">91</span></span>

<span data-ttu-id="bcd9c-203">Accesso negato.</span><span class="sxs-lookup"><span data-stu-id="bcd9c-203">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="bcd9c-204">**Memoria insufficiente**</span><span class="sxs-lookup"><span data-stu-id="bcd9c-204">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="bcd9c-205">92</span><span class="sxs-lookup"><span data-stu-id="bcd9c-205">92</span></span>

<span data-ttu-id="bcd9c-206">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="bcd9c-206">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="bcd9c-207">**Esiste già**</span><span class="sxs-lookup"><span data-stu-id="bcd9c-207">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="bcd9c-208">93</span><span class="sxs-lookup"><span data-stu-id="bcd9c-208">93</span></span>

<span data-ttu-id="bcd9c-209">Esiste già.</span><span class="sxs-lookup"><span data-stu-id="bcd9c-209">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="bcd9c-210">**Percorso, file o oggetto non trovato**</span><span class="sxs-lookup"><span data-stu-id="bcd9c-210">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="bcd9c-211">94</span><span class="sxs-lookup"><span data-stu-id="bcd9c-211">94</span></span>

<span data-ttu-id="bcd9c-212">Il percorso, il file o l'oggetto non è stato trovato.</span><span class="sxs-lookup"><span data-stu-id="bcd9c-212">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="bcd9c-213">**Non è possibile inviare una notifica al servizio**</span><span class="sxs-lookup"><span data-stu-id="bcd9c-213">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="bcd9c-214">95</span><span class="sxs-lookup"><span data-stu-id="bcd9c-214">95</span></span>

<span data-ttu-id="bcd9c-215">Impossibile notificare il servizio.</span><span class="sxs-lookup"><span data-stu-id="bcd9c-215">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="bcd9c-216">**Non è possibile inviare una notifica al servizio DNS**</span><span class="sxs-lookup"><span data-stu-id="bcd9c-216">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="bcd9c-217">96</span><span class="sxs-lookup"><span data-stu-id="bcd9c-217">96</span></span>

<span data-ttu-id="bcd9c-218">Impossibile inviare una notifica al servizio DNS.</span><span class="sxs-lookup"><span data-stu-id="bcd9c-218">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="bcd9c-219">**Interfaccia non configurabile**</span><span class="sxs-lookup"><span data-stu-id="bcd9c-219">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="bcd9c-220">97</span><span class="sxs-lookup"><span data-stu-id="bcd9c-220">97</span></span>

<span data-ttu-id="bcd9c-221">Interfaccia non configurabile.</span><span class="sxs-lookup"><span data-stu-id="bcd9c-221">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="bcd9c-222">**Non tutti i lease DHCP possono essere rilasciati/rinnovati**</span><span class="sxs-lookup"><span data-stu-id="bcd9c-222">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="bcd9c-223">98</span><span class="sxs-lookup"><span data-stu-id="bcd9c-223">98</span></span>

<span data-ttu-id="bcd9c-224">Non tutti i lease DHCP possono essere rilasciati o rinnovati.</span><span class="sxs-lookup"><span data-stu-id="bcd9c-224">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="bcd9c-225">**DHCP non abilitato sull'adapter**</span><span class="sxs-lookup"><span data-stu-id="bcd9c-225">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="bcd9c-226">100</span><span class="sxs-lookup"><span data-stu-id="bcd9c-226">100</span></span>

<span data-ttu-id="bcd9c-227">DHCP non abilitato sulla scheda.</span><span class="sxs-lookup"><span data-stu-id="bcd9c-227">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="bcd9c-228">**Altri**</span><span class="sxs-lookup"><span data-stu-id="bcd9c-228">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="bcd9c-229">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="bcd9c-229">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bcd9c-230">Commenti</span><span class="sxs-lookup"><span data-stu-id="bcd9c-230">Remarks</span></span>

<span data-ttu-id="bcd9c-231">Il lease per l'indirizzo IP assegnato da un server DHCP ha una data di scadenza che il client deve rinnovare se intende continuare a usare l'indirizzo IP assegnato.</span><span class="sxs-lookup"><span data-stu-id="bcd9c-231">The lease for the IP address assigned by a DHCP server has an expiration date that the client must renew if it intends to continue use of the assigned IP address.</span></span>

## <a name="examples"></a><span data-ttu-id="bcd9c-232">Esempio</span><span class="sxs-lookup"><span data-stu-id="bcd9c-232">Examples</span></span>

<span data-ttu-id="bcd9c-233">Nell'esempio relativo al [rinnovo di tutti i lease DHCP](https://Gallery.TechNet.Microsoft.Com/b29171b8-21b0-492a-b0fe-67e650adca99) in TechNet Gallery vengono rinnovati tutti i lease DHCP attualmente in uso in un computer.</span><span class="sxs-lookup"><span data-stu-id="bcd9c-233">The [Renew All DHCP Leases](https://Gallery.TechNet.Microsoft.Com/b29171b8-21b0-492a-b0fe-67e650adca99) VBScript example on TechNet Gallery renews all the DHCP leases currently in use on a computer.</span></span>

## <a name="requirements"></a><span data-ttu-id="bcd9c-234">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bcd9c-234">Requirements</span></span>



| <span data-ttu-id="bcd9c-235">Requisito</span><span class="sxs-lookup"><span data-stu-id="bcd9c-235">Requirement</span></span> | <span data-ttu-id="bcd9c-236">Valore</span><span class="sxs-lookup"><span data-stu-id="bcd9c-236">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bcd9c-237">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bcd9c-237">Minimum supported client</span></span><br/> | <span data-ttu-id="bcd9c-238">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bcd9c-238">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="bcd9c-239">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bcd9c-239">Minimum supported server</span></span><br/> | <span data-ttu-id="bcd9c-240">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bcd9c-240">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="bcd9c-241">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="bcd9c-241">Namespace</span></span><br/>                | <span data-ttu-id="bcd9c-242">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="bcd9c-242">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="bcd9c-243">MOF</span><span class="sxs-lookup"><span data-stu-id="bcd9c-243">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bcd9c-244"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bcd9c-244"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="bcd9c-245">DLL</span><span class="sxs-lookup"><span data-stu-id="bcd9c-245">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bcd9c-246"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bcd9c-246"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bcd9c-247">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bcd9c-247">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bcd9c-248">Classi hardware del sistema del computer</span><span class="sxs-lookup"><span data-stu-id="bcd9c-248">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="bcd9c-249">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="bcd9c-249">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="bcd9c-250">Attività WMI: rete</span><span class="sxs-lookup"><span data-stu-id="bcd9c-250">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="bcd9c-251">Attività WMI: account e domini</span><span class="sxs-lookup"><span data-stu-id="bcd9c-251">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="bcd9c-252">Supporto di IPv6 e IPv4 in WMI</span><span class="sxs-lookup"><span data-stu-id="bcd9c-252">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

