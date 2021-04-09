---
description: Il metodo della classe WMI RenewDHCPLease rinnova l'indirizzo IP in specifiche schede di rete abilitate per DHCP.
ms.assetid: b6e5d1fb-db3f-4491-bbac-46b1f2e7206e
ms.tgt_platform: multiple
title: Metodo RenewDHCPLease della classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.RenewDHCPLease
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4603f013c6b4c2c80edd555608b5f59325b6a6d9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049288"
---
# <a name="renewdhcplease-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="caef2-103">Metodo RenewDHCPLease della \_ classe NetworkAdapterConfiguration Win32</span><span class="sxs-lookup"><span data-stu-id="caef2-103">RenewDHCPLease method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="caef2-104">Il metodo della [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **RenewDHCPLease** rinnova l'indirizzo IP in specifiche schede di rete abilitate per DHCP.</span><span class="sxs-lookup"><span data-stu-id="caef2-104">The **RenewDHCPLease** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method renews the IP address on specific DHCP-enabled network adapters.</span></span>

<span data-ttu-id="caef2-105">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="caef2-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="caef2-106">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="caef2-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="caef2-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="caef2-107">Syntax</span></span>


```mof
uint32 RenewDHCPLease();
```



## <a name="parameters"></a><span data-ttu-id="caef2-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="caef2-108">Parameters</span></span>

<span data-ttu-id="caef2-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="caef2-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="caef2-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="caef2-110">Return value</span></span>

<span data-ttu-id="caef2-111">Restituisce un valore pari a 0 (zero) per un completamento corretto quando non è richiesto il riavvio, 1 (uno) per un completamento corretto quando è necessario un riavvio e un numero diverso se si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="caef2-111">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="caef2-112">Per ulteriori informazioni sui codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="caef2-112">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="caef2-113">Per i valori **HRESULT** generali, vedere [codici di errore di sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="caef2-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="caef2-114">**Operazione completata, non è necessario riavviare il computer**</span><span class="sxs-lookup"><span data-stu-id="caef2-114">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="caef2-115">0</span><span class="sxs-lookup"><span data-stu-id="caef2-115">0</span></span>

<span data-ttu-id="caef2-116">Operazione completata, non è necessario riavviare il computer.</span><span class="sxs-lookup"><span data-stu-id="caef2-116">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="caef2-117">**Operazione completata, riavvio richiesto**</span><span class="sxs-lookup"><span data-stu-id="caef2-117">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="caef2-118">1</span><span class="sxs-lookup"><span data-stu-id="caef2-118">1</span></span>

<span data-ttu-id="caef2-119">Operazione completata, è necessario riavviare il computer.</span><span class="sxs-lookup"><span data-stu-id="caef2-119">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="caef2-120">**Metodo non supportato in questa piattaforma**</span><span class="sxs-lookup"><span data-stu-id="caef2-120">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="caef2-121">64</span><span class="sxs-lookup"><span data-stu-id="caef2-121">64</span></span>

<span data-ttu-id="caef2-122">Metodo non supportato in questa piattaforma.</span><span class="sxs-lookup"><span data-stu-id="caef2-122">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="caef2-123">**Errore sconosciuto**</span><span class="sxs-lookup"><span data-stu-id="caef2-123">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="caef2-124">65</span><span class="sxs-lookup"><span data-stu-id="caef2-124">65</span></span>

<span data-ttu-id="caef2-125">Errore sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="caef2-125">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="caef2-126">**subnet mask non valido**</span><span class="sxs-lookup"><span data-stu-id="caef2-126">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="caef2-127">66</span><span class="sxs-lookup"><span data-stu-id="caef2-127">66</span></span>

<span data-ttu-id="caef2-128">Subnet mask non valido.</span><span class="sxs-lookup"><span data-stu-id="caef2-128">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="caef2-129">**Si è verificato un errore durante l'elaborazione di un'istanza restituita**</span><span class="sxs-lookup"><span data-stu-id="caef2-129">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="caef2-130">67</span><span class="sxs-lookup"><span data-stu-id="caef2-130">67</span></span>

<span data-ttu-id="caef2-131">Si è verificato un errore durante l'elaborazione di un'istanza di restituita.</span><span class="sxs-lookup"><span data-stu-id="caef2-131">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="caef2-132">**Parametro di input non valido**</span><span class="sxs-lookup"><span data-stu-id="caef2-132">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="caef2-133">68</span><span class="sxs-lookup"><span data-stu-id="caef2-133">68</span></span>

<span data-ttu-id="caef2-134">Parametro di input non valido.</span><span class="sxs-lookup"><span data-stu-id="caef2-134">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="caef2-135">**Sono stati specificati più di 5 gateway**</span><span class="sxs-lookup"><span data-stu-id="caef2-135">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="caef2-136">69</span><span class="sxs-lookup"><span data-stu-id="caef2-136">69</span></span>

<span data-ttu-id="caef2-137">Sono stati specificati più di cinque gateway.</span><span class="sxs-lookup"><span data-stu-id="caef2-137">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="caef2-138">**Indirizzo IP non valido**</span><span class="sxs-lookup"><span data-stu-id="caef2-138">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="caef2-139">70</span><span class="sxs-lookup"><span data-stu-id="caef2-139">70</span></span>

<span data-ttu-id="caef2-140">Indirizzo IP non valido.</span><span class="sxs-lookup"><span data-stu-id="caef2-140">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="caef2-141">**Indirizzo IP gateway non valido**</span><span class="sxs-lookup"><span data-stu-id="caef2-141">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="caef2-142">71</span><span class="sxs-lookup"><span data-stu-id="caef2-142">71</span></span>

<span data-ttu-id="caef2-143">Indirizzo IP del gateway non valido.</span><span class="sxs-lookup"><span data-stu-id="caef2-143">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="caef2-144">**Si è verificato un errore durante l'accesso al registro di sistema per le informazioni richieste**</span><span class="sxs-lookup"><span data-stu-id="caef2-144">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="caef2-145">72</span><span class="sxs-lookup"><span data-stu-id="caef2-145">72</span></span>

<span data-ttu-id="caef2-146">Si è verificato un errore durante l'accesso al registro di sistema per le informazioni richieste.</span><span class="sxs-lookup"><span data-stu-id="caef2-146">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="caef2-147">**Nome di dominio non valido**</span><span class="sxs-lookup"><span data-stu-id="caef2-147">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="caef2-148">73</span><span class="sxs-lookup"><span data-stu-id="caef2-148">73</span></span>

<span data-ttu-id="caef2-149">Nome di dominio non valido.</span><span class="sxs-lookup"><span data-stu-id="caef2-149">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="caef2-150">**Nome host non valido**</span><span class="sxs-lookup"><span data-stu-id="caef2-150">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="caef2-151">74</span><span class="sxs-lookup"><span data-stu-id="caef2-151">74</span></span>

<span data-ttu-id="caef2-152">Nome host non valido.</span><span class="sxs-lookup"><span data-stu-id="caef2-152">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="caef2-153">**Nessun server WINS primario/secondario definito**</span><span class="sxs-lookup"><span data-stu-id="caef2-153">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="caef2-154">75</span><span class="sxs-lookup"><span data-stu-id="caef2-154">75</span></span>

<span data-ttu-id="caef2-155">Nessun server WINS primario o secondario definito.</span><span class="sxs-lookup"><span data-stu-id="caef2-155">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="caef2-156">**File non valido**</span><span class="sxs-lookup"><span data-stu-id="caef2-156">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="caef2-157">76</span><span class="sxs-lookup"><span data-stu-id="caef2-157">76</span></span>

<span data-ttu-id="caef2-158">File non valido.</span><span class="sxs-lookup"><span data-stu-id="caef2-158">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="caef2-159">**Percorso di sistema non valido**</span><span class="sxs-lookup"><span data-stu-id="caef2-159">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="caef2-160">77</span><span class="sxs-lookup"><span data-stu-id="caef2-160">77</span></span>

<span data-ttu-id="caef2-161">Percorso di sistema non valido.</span><span class="sxs-lookup"><span data-stu-id="caef2-161">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="caef2-162">**Copia del file non riuscita**</span><span class="sxs-lookup"><span data-stu-id="caef2-162">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="caef2-163">78</span><span class="sxs-lookup"><span data-stu-id="caef2-163">78</span></span>

<span data-ttu-id="caef2-164">Copia del file non riuscita.</span><span class="sxs-lookup"><span data-stu-id="caef2-164">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="caef2-165">**Parametro di sicurezza non valido**</span><span class="sxs-lookup"><span data-stu-id="caef2-165">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="caef2-166">79</span><span class="sxs-lookup"><span data-stu-id="caef2-166">79</span></span>

<span data-ttu-id="caef2-167">Parametro di sicurezza non valido.</span><span class="sxs-lookup"><span data-stu-id="caef2-167">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="caef2-168">**Impossibile configurare il servizio TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="caef2-168">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="caef2-169">80</span><span class="sxs-lookup"><span data-stu-id="caef2-169">80</span></span>

<span data-ttu-id="caef2-170">Impossibile configurare il servizio TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="caef2-170">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="caef2-171">**Non è possibile configurare il servizio DHCP**</span><span class="sxs-lookup"><span data-stu-id="caef2-171">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="caef2-172">81</span><span class="sxs-lookup"><span data-stu-id="caef2-172">81</span></span>

<span data-ttu-id="caef2-173">Impossibile configurare il servizio DHCP.</span><span class="sxs-lookup"><span data-stu-id="caef2-173">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="caef2-174">**Non è possibile rinnovare il lease DHCP**</span><span class="sxs-lookup"><span data-stu-id="caef2-174">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="caef2-175">82</span><span class="sxs-lookup"><span data-stu-id="caef2-175">82</span></span>

<span data-ttu-id="caef2-176">Non è possibile rinnovare il lease DHCP.</span><span class="sxs-lookup"><span data-stu-id="caef2-176">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="caef2-177">**Non è possibile rilasciare il lease DHCP**</span><span class="sxs-lookup"><span data-stu-id="caef2-177">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="caef2-178">83</span><span class="sxs-lookup"><span data-stu-id="caef2-178">83</span></span>

<span data-ttu-id="caef2-179">Impossibile rilasciare il lease DHCP.</span><span class="sxs-lookup"><span data-stu-id="caef2-179">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="caef2-180">**IP non abilitato sulla scheda**</span><span class="sxs-lookup"><span data-stu-id="caef2-180">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="caef2-181">84</span><span class="sxs-lookup"><span data-stu-id="caef2-181">84</span></span>

<span data-ttu-id="caef2-182">IP non abilitato sulla scheda.</span><span class="sxs-lookup"><span data-stu-id="caef2-182">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="caef2-183">**IPX non abilitato sull'adapter**</span><span class="sxs-lookup"><span data-stu-id="caef2-183">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="caef2-184">85</span><span class="sxs-lookup"><span data-stu-id="caef2-184">85</span></span>

<span data-ttu-id="caef2-185">IPX non abilitato sulla scheda.</span><span class="sxs-lookup"><span data-stu-id="caef2-185">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="caef2-186">**Errore limite numero frame/rete**</span><span class="sxs-lookup"><span data-stu-id="caef2-186">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="caef2-187">86</span><span class="sxs-lookup"><span data-stu-id="caef2-187">86</span></span>

<span data-ttu-id="caef2-188">Errore dei limiti del numero di rete o del frame.</span><span class="sxs-lookup"><span data-stu-id="caef2-188">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="caef2-189">**Tipo di frame non valido**</span><span class="sxs-lookup"><span data-stu-id="caef2-189">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="caef2-190">87</span><span class="sxs-lookup"><span data-stu-id="caef2-190">87</span></span>

<span data-ttu-id="caef2-191">Tipo di frame non valido.</span><span class="sxs-lookup"><span data-stu-id="caef2-191">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="caef2-192">**Numero di rete non valido**</span><span class="sxs-lookup"><span data-stu-id="caef2-192">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="caef2-193">88</span><span class="sxs-lookup"><span data-stu-id="caef2-193">88</span></span>

<span data-ttu-id="caef2-194">Numero di rete non valido.</span><span class="sxs-lookup"><span data-stu-id="caef2-194">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="caef2-195">**Numero di rete duplicato**</span><span class="sxs-lookup"><span data-stu-id="caef2-195">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="caef2-196">89</span><span class="sxs-lookup"><span data-stu-id="caef2-196">89</span></span>

<span data-ttu-id="caef2-197">Numero di rete duplicato.</span><span class="sxs-lookup"><span data-stu-id="caef2-197">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="caef2-198">**Parametro fuori limite**</span><span class="sxs-lookup"><span data-stu-id="caef2-198">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="caef2-199">90</span><span class="sxs-lookup"><span data-stu-id="caef2-199">90</span></span>

<span data-ttu-id="caef2-200">Parametro fuori limite.</span><span class="sxs-lookup"><span data-stu-id="caef2-200">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="caef2-201">**Accesso negato**</span><span class="sxs-lookup"><span data-stu-id="caef2-201">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="caef2-202">91</span><span class="sxs-lookup"><span data-stu-id="caef2-202">91</span></span>

<span data-ttu-id="caef2-203">Accesso negato.</span><span class="sxs-lookup"><span data-stu-id="caef2-203">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="caef2-204">**Memoria insufficiente**</span><span class="sxs-lookup"><span data-stu-id="caef2-204">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="caef2-205">92</span><span class="sxs-lookup"><span data-stu-id="caef2-205">92</span></span>

<span data-ttu-id="caef2-206">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="caef2-206">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="caef2-207">**Esiste già**</span><span class="sxs-lookup"><span data-stu-id="caef2-207">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="caef2-208">93</span><span class="sxs-lookup"><span data-stu-id="caef2-208">93</span></span>

<span data-ttu-id="caef2-209">Esiste già.</span><span class="sxs-lookup"><span data-stu-id="caef2-209">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="caef2-210">**Percorso, file o oggetto non trovato**</span><span class="sxs-lookup"><span data-stu-id="caef2-210">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="caef2-211">94</span><span class="sxs-lookup"><span data-stu-id="caef2-211">94</span></span>

<span data-ttu-id="caef2-212">Il percorso, il file o l'oggetto non è stato trovato.</span><span class="sxs-lookup"><span data-stu-id="caef2-212">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="caef2-213">**Non è possibile inviare una notifica al servizio**</span><span class="sxs-lookup"><span data-stu-id="caef2-213">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="caef2-214">95</span><span class="sxs-lookup"><span data-stu-id="caef2-214">95</span></span>

<span data-ttu-id="caef2-215">Impossibile notificare il servizio.</span><span class="sxs-lookup"><span data-stu-id="caef2-215">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="caef2-216">**Non è possibile inviare una notifica al servizio DNS**</span><span class="sxs-lookup"><span data-stu-id="caef2-216">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="caef2-217">96</span><span class="sxs-lookup"><span data-stu-id="caef2-217">96</span></span>

<span data-ttu-id="caef2-218">Impossibile inviare una notifica al servizio DNS.</span><span class="sxs-lookup"><span data-stu-id="caef2-218">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="caef2-219">**Interfaccia non configurabile**</span><span class="sxs-lookup"><span data-stu-id="caef2-219">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="caef2-220">97</span><span class="sxs-lookup"><span data-stu-id="caef2-220">97</span></span>

<span data-ttu-id="caef2-221">Interfaccia non configurabile.</span><span class="sxs-lookup"><span data-stu-id="caef2-221">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="caef2-222">**Non tutti i lease DHCP possono essere rilasciati/rinnovati**</span><span class="sxs-lookup"><span data-stu-id="caef2-222">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="caef2-223">98</span><span class="sxs-lookup"><span data-stu-id="caef2-223">98</span></span>

<span data-ttu-id="caef2-224">Non tutti i lease DHCP possono essere rilasciati o rinnovati.</span><span class="sxs-lookup"><span data-stu-id="caef2-224">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="caef2-225">**DHCP non abilitato sull'adapter**</span><span class="sxs-lookup"><span data-stu-id="caef2-225">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="caef2-226">100</span><span class="sxs-lookup"><span data-stu-id="caef2-226">100</span></span>

<span data-ttu-id="caef2-227">DHCP non abilitato sulla scheda.</span><span class="sxs-lookup"><span data-stu-id="caef2-227">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="caef2-228">**Altri**</span><span class="sxs-lookup"><span data-stu-id="caef2-228">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="caef2-229">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="caef2-229">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="caef2-230">Commenti</span><span class="sxs-lookup"><span data-stu-id="caef2-230">Remarks</span></span>

<span data-ttu-id="caef2-231">Il lease per l'indirizzo IP assegnato da un server DHCP ha una data di scadenza che il client deve rinnovare se intende continuare a usare l'indirizzo IP assegnato.</span><span class="sxs-lookup"><span data-stu-id="caef2-231">The lease for the IP address assigned by a DHCP server has an expiration date that the client must renew if it intends to continue use of the assigned IP address.</span></span>

## <a name="examples"></a><span data-ttu-id="caef2-232">Esempio</span><span class="sxs-lookup"><span data-stu-id="caef2-232">Examples</span></span>

<span data-ttu-id="caef2-233">L'esempio di rinnovo di indirizzi IP per la [versione con](https://Gallery.TechNet.Microsoft.Com/Renew-IP-Adresses-Using-365f6bfa) PowerShell PowerShell nella raccolta TechNet USA **RenewDHCPLease** per rilasciare e rinnovare un indirizzo IP.</span><span class="sxs-lookup"><span data-stu-id="caef2-233">The [Release Renew IP Adresses Using PowerShell](https://Gallery.TechNet.Microsoft.Com/Renew-IP-Adresses-Using-365f6bfa) PowerShell example on TechNet Gallery uses **RenewDHCPLease** to release and renew an IP address.</span></span>

<span data-ttu-id="caef2-234">Il [rinnovo del lease DHCP per un](https://Gallery.TechNet.Microsoft.Com/39443fd7-0152-4c0a-89e9-e2753049b203) esempio VBScript della scheda di rete nella raccolta TechNet utilizza **RenewDHCPLease** per rinnovare il lease DHCP per ogni scheda di rete associata a TCP/IP in un computer.</span><span class="sxs-lookup"><span data-stu-id="caef2-234">The [Renew the DHCP Lease for a Network Adapter](https://Gallery.TechNet.Microsoft.Com/39443fd7-0152-4c0a-89e9-e2753049b203) VBScript sample on TechNet Gallery uses **RenewDHCPLease** to renew the DHCP lease for each TCP/IP-bound network adapter in a computer.</span></span>

## <a name="requirements"></a><span data-ttu-id="caef2-235">Requisiti</span><span class="sxs-lookup"><span data-stu-id="caef2-235">Requirements</span></span>



| <span data-ttu-id="caef2-236">Requisito</span><span class="sxs-lookup"><span data-stu-id="caef2-236">Requirement</span></span> | <span data-ttu-id="caef2-237">Valore</span><span class="sxs-lookup"><span data-stu-id="caef2-237">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="caef2-238">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="caef2-238">Minimum supported client</span></span><br/> | <span data-ttu-id="caef2-239">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="caef2-239">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="caef2-240">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="caef2-240">Minimum supported server</span></span><br/> | <span data-ttu-id="caef2-241">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="caef2-241">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="caef2-242">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="caef2-242">Namespace</span></span><br/>                | <span data-ttu-id="caef2-243">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="caef2-243">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="caef2-244">MOF</span><span class="sxs-lookup"><span data-stu-id="caef2-244">MOF</span></span><br/>                      | <dl> <span data-ttu-id="caef2-245"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="caef2-245"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="caef2-246">DLL</span><span class="sxs-lookup"><span data-stu-id="caef2-246">DLL</span></span><br/>                      | <dl> <span data-ttu-id="caef2-247"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="caef2-247"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="caef2-248">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="caef2-248">See also</span></span>

<dl> <dt>

[<span data-ttu-id="caef2-249">Classi hardware del sistema del computer</span><span class="sxs-lookup"><span data-stu-id="caef2-249">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="caef2-250">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="caef2-250">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="caef2-251">Attività WMI: rete</span><span class="sxs-lookup"><span data-stu-id="caef2-251">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="caef2-252">Attività WMI: account e domini</span><span class="sxs-lookup"><span data-stu-id="caef2-252">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="caef2-253">Supporto di IPv6 e IPv4 in WMI</span><span class="sxs-lookup"><span data-stu-id="caef2-253">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

