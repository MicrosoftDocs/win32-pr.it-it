---
description: Il metodo SetDynamicDNSRegistration indica la registrazione DNS dinamica degli indirizzi IP per questa scheda con binding IP.
ms.assetid: 8e6ca408-3283-40b8-b621-9befdc39b730
ms.tgt_platform: multiple
title: Metodo SetDynamicDNSRegistration della classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetDynamicDNSRegistration
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 36818205e356f873b391159293e9204a9ced44a7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878025"
---
# <a name="setdynamicdnsregistration-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="e9489-103">Metodo SetDynamicDNSRegistration della \_ classe NetworkAdapterConfiguration Win32</span><span class="sxs-lookup"><span data-stu-id="e9489-103">SetDynamicDNSRegistration method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="e9489-104">Il metodo **SetDynamicDNSRegistration** indica la registrazione DNS dinamica degli indirizzi IP per questa scheda con binding IP.</span><span class="sxs-lookup"><span data-stu-id="e9489-104">The **SetDynamicDNSRegistration** method indicates the dynamic DNS registration of IP addresses for this IP-bound adapter.</span></span>

<span data-ttu-id="e9489-105">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="e9489-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="e9489-106">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="e9489-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="e9489-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e9489-107">Syntax</span></span>


```mof
uint32 SetDynamicDNSRegistration(
  [in]           boolean FullDNSRegistrationEnabled,
  [in, optional] boolean DomainDNSRegistrationEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="e9489-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="e9489-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9489-109">*FullDNSRegistrationEnabled* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e9489-109">*FullDNSRegistrationEnabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9489-110">Se **true**, gli indirizzi IP per questa connessione sono registrati in DNS con il nome DNS completo del computer.</span><span class="sxs-lookup"><span data-stu-id="e9489-110">If **true**, the IP addresses for this connection is registered in DNS under the computer's full DNS name.</span></span> <span data-ttu-id="e9489-111">Il nome DNS completo del computer viene visualizzato nella scheda **Identificazione rete** del pannello di controllo del sistema.</span><span class="sxs-lookup"><span data-stu-id="e9489-111">The full DNS name of the computer is displayed on the **Network Identification** tab of the system Control Panel.</span></span>

</dd> <dt>

<span data-ttu-id="e9489-112">*DomainDNSRegistrationEnabled* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="e9489-112">*DomainDNSRegistrationEnabled* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e9489-113">Se **true**, gli indirizzi IP per questa connessione vengono registrati con il nome di dominio della connessione, oltre a essere registrati con il nome DNS completo del computer.</span><span class="sxs-lookup"><span data-stu-id="e9489-113">If **true**, the IP addresses for this connection are registered under the domain name of this connection, in addition to being registered under the computer's full DNS name.</span></span> <span data-ttu-id="e9489-114">Il nome di dominio della connessione viene impostato utilizzando il metodo [**SetDNSDomain**](setdnsdomain-method-in-class-win32-networkadapterconfiguration.md) o assegnato da DHCP.</span><span class="sxs-lookup"><span data-stu-id="e9489-114">The domain name of this connection is either set using the method [**SetDNSDomain**](setdnsdomain-method-in-class-win32-networkadapterconfiguration.md) or assigned by DHCP.</span></span> <span data-ttu-id="e9489-115">Il nome registrato è il nome host del computer a cui è stato aggiunto il nome di dominio.</span><span class="sxs-lookup"><span data-stu-id="e9489-115">The registered name is the host name of the computer with the domain name appended.</span></span> <span data-ttu-id="e9489-116">Questo parametro ha un significato solo quando *FullDNSRegistrationEnabled* è abilitato.</span><span class="sxs-lookup"><span data-stu-id="e9489-116">This parameter has meaning only when *FullDNSRegistrationEnabled* is enabled.</span></span> <span data-ttu-id="e9489-117">Il valore predefinito è **false**.</span><span class="sxs-lookup"><span data-stu-id="e9489-117">The default value is **false**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9489-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e9489-118">Return value</span></span>

<span data-ttu-id="e9489-119">Restituisce un valore pari a 0 (zero) per un completamento corretto quando non è richiesto il riavvio, 1 (uno) per un completamento corretto quando è necessario un riavvio e un numero diverso se si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="e9489-119">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="e9489-120">Per ulteriori informazioni sui codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="e9489-120">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="e9489-121">Per i valori **HRESULT** generali, vedere [codici di errore di sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="e9489-121">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="e9489-122">**Operazione completata, non è necessario riavviare il computer**</span><span class="sxs-lookup"><span data-stu-id="e9489-122">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="e9489-123">0</span><span class="sxs-lookup"><span data-stu-id="e9489-123">0</span></span>

<span data-ttu-id="e9489-124">Operazione completata, non è necessario riavviare il computer.</span><span class="sxs-lookup"><span data-stu-id="e9489-124">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="e9489-125">**Operazione completata, riavvio richiesto**</span><span class="sxs-lookup"><span data-stu-id="e9489-125">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="e9489-126">1</span><span class="sxs-lookup"><span data-stu-id="e9489-126">1</span></span>

<span data-ttu-id="e9489-127">Operazione completata, è necessario riavviare il computer.</span><span class="sxs-lookup"><span data-stu-id="e9489-127">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="e9489-128">**Metodo non supportato in questa piattaforma**</span><span class="sxs-lookup"><span data-stu-id="e9489-128">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="e9489-129">64</span><span class="sxs-lookup"><span data-stu-id="e9489-129">64</span></span>

<span data-ttu-id="e9489-130">Metodo non supportato in questa piattaforma.</span><span class="sxs-lookup"><span data-stu-id="e9489-130">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="e9489-131">**Errore sconosciuto**</span><span class="sxs-lookup"><span data-stu-id="e9489-131">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="e9489-132">65</span><span class="sxs-lookup"><span data-stu-id="e9489-132">65</span></span>

<span data-ttu-id="e9489-133">Errore sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="e9489-133">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="e9489-134">**subnet mask non valido**</span><span class="sxs-lookup"><span data-stu-id="e9489-134">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="e9489-135">66</span><span class="sxs-lookup"><span data-stu-id="e9489-135">66</span></span>

<span data-ttu-id="e9489-136">Subnet mask non valido.</span><span class="sxs-lookup"><span data-stu-id="e9489-136">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="e9489-137">**Si è verificato un errore durante l'elaborazione di un'istanza restituita**</span><span class="sxs-lookup"><span data-stu-id="e9489-137">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="e9489-138">67</span><span class="sxs-lookup"><span data-stu-id="e9489-138">67</span></span>

<span data-ttu-id="e9489-139">Si è verificato un errore durante l'elaborazione di un'istanza di restituita.</span><span class="sxs-lookup"><span data-stu-id="e9489-139">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="e9489-140">**Parametro di input non valido**</span><span class="sxs-lookup"><span data-stu-id="e9489-140">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="e9489-141">68</span><span class="sxs-lookup"><span data-stu-id="e9489-141">68</span></span>

<span data-ttu-id="e9489-142">Parametro di input non valido.</span><span class="sxs-lookup"><span data-stu-id="e9489-142">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="e9489-143">**Sono stati specificati più di 5 gateway**</span><span class="sxs-lookup"><span data-stu-id="e9489-143">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="e9489-144">69</span><span class="sxs-lookup"><span data-stu-id="e9489-144">69</span></span>

<span data-ttu-id="e9489-145">Sono stati specificati più di cinque gateway.</span><span class="sxs-lookup"><span data-stu-id="e9489-145">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="e9489-146">**Indirizzo IP non valido**</span><span class="sxs-lookup"><span data-stu-id="e9489-146">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="e9489-147">70</span><span class="sxs-lookup"><span data-stu-id="e9489-147">70</span></span>

<span data-ttu-id="e9489-148">Indirizzo IP non valido.</span><span class="sxs-lookup"><span data-stu-id="e9489-148">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="e9489-149">**Indirizzo IP gateway non valido**</span><span class="sxs-lookup"><span data-stu-id="e9489-149">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="e9489-150">71</span><span class="sxs-lookup"><span data-stu-id="e9489-150">71</span></span>

<span data-ttu-id="e9489-151">Indirizzo IP del gateway non valido.</span><span class="sxs-lookup"><span data-stu-id="e9489-151">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="e9489-152">**Si è verificato un errore durante l'accesso al registro di sistema per le informazioni richieste**</span><span class="sxs-lookup"><span data-stu-id="e9489-152">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="e9489-153">72</span><span class="sxs-lookup"><span data-stu-id="e9489-153">72</span></span>

<span data-ttu-id="e9489-154">Si è verificato un errore durante l'accesso al registro di sistema per le informazioni richieste.</span><span class="sxs-lookup"><span data-stu-id="e9489-154">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="e9489-155">**Nome di dominio non valido**</span><span class="sxs-lookup"><span data-stu-id="e9489-155">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="e9489-156">73</span><span class="sxs-lookup"><span data-stu-id="e9489-156">73</span></span>

<span data-ttu-id="e9489-157">Nome di dominio non valido.</span><span class="sxs-lookup"><span data-stu-id="e9489-157">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="e9489-158">**Nome host non valido**</span><span class="sxs-lookup"><span data-stu-id="e9489-158">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="e9489-159">74</span><span class="sxs-lookup"><span data-stu-id="e9489-159">74</span></span>

<span data-ttu-id="e9489-160">Nome host non valido.</span><span class="sxs-lookup"><span data-stu-id="e9489-160">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="e9489-161">**Nessun server WINS primario/secondario definito**</span><span class="sxs-lookup"><span data-stu-id="e9489-161">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="e9489-162">75</span><span class="sxs-lookup"><span data-stu-id="e9489-162">75</span></span>

<span data-ttu-id="e9489-163">Nessun server WINS primario o secondario definito.</span><span class="sxs-lookup"><span data-stu-id="e9489-163">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="e9489-164">**File non valido**</span><span class="sxs-lookup"><span data-stu-id="e9489-164">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="e9489-165">76</span><span class="sxs-lookup"><span data-stu-id="e9489-165">76</span></span>

<span data-ttu-id="e9489-166">File non valido.</span><span class="sxs-lookup"><span data-stu-id="e9489-166">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="e9489-167">**Percorso di sistema non valido**</span><span class="sxs-lookup"><span data-stu-id="e9489-167">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="e9489-168">77</span><span class="sxs-lookup"><span data-stu-id="e9489-168">77</span></span>

<span data-ttu-id="e9489-169">Percorso di sistema non valido.</span><span class="sxs-lookup"><span data-stu-id="e9489-169">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="e9489-170">**Copia del file non riuscita**</span><span class="sxs-lookup"><span data-stu-id="e9489-170">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="e9489-171">78</span><span class="sxs-lookup"><span data-stu-id="e9489-171">78</span></span>

<span data-ttu-id="e9489-172">Copia del file non riuscita.</span><span class="sxs-lookup"><span data-stu-id="e9489-172">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="e9489-173">**Parametro di sicurezza non valido**</span><span class="sxs-lookup"><span data-stu-id="e9489-173">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="e9489-174">79</span><span class="sxs-lookup"><span data-stu-id="e9489-174">79</span></span>

<span data-ttu-id="e9489-175">Parametro di sicurezza non valido.</span><span class="sxs-lookup"><span data-stu-id="e9489-175">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="e9489-176">**Impossibile configurare il servizio TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="e9489-176">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="e9489-177">80</span><span class="sxs-lookup"><span data-stu-id="e9489-177">80</span></span>

<span data-ttu-id="e9489-178">Impossibile configurare il servizio TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="e9489-178">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="e9489-179">**Non è possibile configurare il servizio DHCP**</span><span class="sxs-lookup"><span data-stu-id="e9489-179">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="e9489-180">81</span><span class="sxs-lookup"><span data-stu-id="e9489-180">81</span></span>

<span data-ttu-id="e9489-181">Impossibile configurare il servizio DHCP.</span><span class="sxs-lookup"><span data-stu-id="e9489-181">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="e9489-182">**Non è possibile rinnovare il lease DHCP**</span><span class="sxs-lookup"><span data-stu-id="e9489-182">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="e9489-183">82</span><span class="sxs-lookup"><span data-stu-id="e9489-183">82</span></span>

<span data-ttu-id="e9489-184">Non è possibile rinnovare il lease DHCP.</span><span class="sxs-lookup"><span data-stu-id="e9489-184">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="e9489-185">**Non è possibile rilasciare il lease DHCP**</span><span class="sxs-lookup"><span data-stu-id="e9489-185">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="e9489-186">83</span><span class="sxs-lookup"><span data-stu-id="e9489-186">83</span></span>

<span data-ttu-id="e9489-187">Impossibile rilasciare il lease DHCP.</span><span class="sxs-lookup"><span data-stu-id="e9489-187">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="e9489-188">**IP non abilitato sulla scheda**</span><span class="sxs-lookup"><span data-stu-id="e9489-188">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="e9489-189">84</span><span class="sxs-lookup"><span data-stu-id="e9489-189">84</span></span>

<span data-ttu-id="e9489-190">IP non abilitato sulla scheda.</span><span class="sxs-lookup"><span data-stu-id="e9489-190">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="e9489-191">**IPX non abilitato sull'adapter**</span><span class="sxs-lookup"><span data-stu-id="e9489-191">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="e9489-192">85</span><span class="sxs-lookup"><span data-stu-id="e9489-192">85</span></span>

<span data-ttu-id="e9489-193">IPX non abilitato sulla scheda.</span><span class="sxs-lookup"><span data-stu-id="e9489-193">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="e9489-194">**Errore limite numero frame/rete**</span><span class="sxs-lookup"><span data-stu-id="e9489-194">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="e9489-195">86</span><span class="sxs-lookup"><span data-stu-id="e9489-195">86</span></span>

<span data-ttu-id="e9489-196">Errore dei limiti del numero di rete o del frame.</span><span class="sxs-lookup"><span data-stu-id="e9489-196">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="e9489-197">**Tipo di frame non valido**</span><span class="sxs-lookup"><span data-stu-id="e9489-197">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="e9489-198">87</span><span class="sxs-lookup"><span data-stu-id="e9489-198">87</span></span>

<span data-ttu-id="e9489-199">Tipo di frame non valido.</span><span class="sxs-lookup"><span data-stu-id="e9489-199">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="e9489-200">**Numero di rete non valido**</span><span class="sxs-lookup"><span data-stu-id="e9489-200">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="e9489-201">88</span><span class="sxs-lookup"><span data-stu-id="e9489-201">88</span></span>

<span data-ttu-id="e9489-202">Numero di rete non valido.</span><span class="sxs-lookup"><span data-stu-id="e9489-202">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="e9489-203">**Numero di rete duplicato**</span><span class="sxs-lookup"><span data-stu-id="e9489-203">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="e9489-204">89</span><span class="sxs-lookup"><span data-stu-id="e9489-204">89</span></span>

<span data-ttu-id="e9489-205">Numero di rete duplicato.</span><span class="sxs-lookup"><span data-stu-id="e9489-205">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="e9489-206">**Parametro fuori limite**</span><span class="sxs-lookup"><span data-stu-id="e9489-206">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="e9489-207">90</span><span class="sxs-lookup"><span data-stu-id="e9489-207">90</span></span>

<span data-ttu-id="e9489-208">Parametro fuori limite.</span><span class="sxs-lookup"><span data-stu-id="e9489-208">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="e9489-209">**Accesso negato**</span><span class="sxs-lookup"><span data-stu-id="e9489-209">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="e9489-210">91</span><span class="sxs-lookup"><span data-stu-id="e9489-210">91</span></span>

<span data-ttu-id="e9489-211">Accesso negato.</span><span class="sxs-lookup"><span data-stu-id="e9489-211">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="e9489-212">**Memoria insufficiente**</span><span class="sxs-lookup"><span data-stu-id="e9489-212">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="e9489-213">92</span><span class="sxs-lookup"><span data-stu-id="e9489-213">92</span></span>

<span data-ttu-id="e9489-214">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="e9489-214">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="e9489-215">**Esiste già**</span><span class="sxs-lookup"><span data-stu-id="e9489-215">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="e9489-216">93</span><span class="sxs-lookup"><span data-stu-id="e9489-216">93</span></span>

<span data-ttu-id="e9489-217">Esiste già.</span><span class="sxs-lookup"><span data-stu-id="e9489-217">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="e9489-218">**Percorso, file o oggetto non trovato**</span><span class="sxs-lookup"><span data-stu-id="e9489-218">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="e9489-219">94</span><span class="sxs-lookup"><span data-stu-id="e9489-219">94</span></span>

<span data-ttu-id="e9489-220">Il percorso, il file o l'oggetto non è stato trovato.</span><span class="sxs-lookup"><span data-stu-id="e9489-220">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="e9489-221">**Non è possibile inviare una notifica al servizio**</span><span class="sxs-lookup"><span data-stu-id="e9489-221">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="e9489-222">95</span><span class="sxs-lookup"><span data-stu-id="e9489-222">95</span></span>

<span data-ttu-id="e9489-223">Impossibile notificare il servizio.</span><span class="sxs-lookup"><span data-stu-id="e9489-223">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="e9489-224">**Non è possibile inviare una notifica al servizio DNS**</span><span class="sxs-lookup"><span data-stu-id="e9489-224">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="e9489-225">96</span><span class="sxs-lookup"><span data-stu-id="e9489-225">96</span></span>

<span data-ttu-id="e9489-226">Impossibile inviare una notifica al servizio DNS.</span><span class="sxs-lookup"><span data-stu-id="e9489-226">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="e9489-227">**Interfaccia non configurabile**</span><span class="sxs-lookup"><span data-stu-id="e9489-227">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="e9489-228">97</span><span class="sxs-lookup"><span data-stu-id="e9489-228">97</span></span>

<span data-ttu-id="e9489-229">Interfaccia non configurabile.</span><span class="sxs-lookup"><span data-stu-id="e9489-229">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="e9489-230">**Non tutti i lease DHCP possono essere rilasciati/rinnovati**</span><span class="sxs-lookup"><span data-stu-id="e9489-230">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="e9489-231">98</span><span class="sxs-lookup"><span data-stu-id="e9489-231">98</span></span>

<span data-ttu-id="e9489-232">Non tutti i lease DHCP possono essere rilasciati o rinnovati.</span><span class="sxs-lookup"><span data-stu-id="e9489-232">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="e9489-233">**DHCP non abilitato sull'adapter**</span><span class="sxs-lookup"><span data-stu-id="e9489-233">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="e9489-234">100</span><span class="sxs-lookup"><span data-stu-id="e9489-234">100</span></span>

<span data-ttu-id="e9489-235">DHCP non abilitato sulla scheda.</span><span class="sxs-lookup"><span data-stu-id="e9489-235">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="e9489-236">**Altri**</span><span class="sxs-lookup"><span data-stu-id="e9489-236">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="e9489-237">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="e9489-237">101 4294967295</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="e9489-238">Esempio</span><span class="sxs-lookup"><span data-stu-id="e9489-238">Examples</span></span>

<span data-ttu-id="e9489-239">L'esempio [Modify Dynamic DNS Registration for a Network Adapter](https://Gallery.TechNet.Microsoft.Com/6c72969c-16c8-4bb6-92e9-b9020001759f) VBScript configura la registrazione DNS dinamica per una scheda di rete.</span><span class="sxs-lookup"><span data-stu-id="e9489-239">The [Modify Dynamic DNS Registration for a Network Adapter](https://Gallery.TechNet.Microsoft.Com/6c72969c-16c8-4bb6-92e9-b9020001759f) VBScript sample configures dynamic DNS registration for a network adapter.</span></span>

<span data-ttu-id="e9489-240">L'esempio di configurazione delle [schede di rete iSCSI come per le procedure consigliate di Microsoft](https://Gallery.TechNet.Microsoft.Com/Configure-iSCSI-Network-81232a5e) consente di automatizzare le impostazioni di configurazione per una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e9489-240">The [Configure iSCSI Network Cards as per Microsoft Best Practices PowerShell](https://Gallery.TechNet.Microsoft.Com/Configure-iSCSI-Network-81232a5e) sample automates the configuration settings for a Virtual Machine.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9489-241">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e9489-241">Requirements</span></span>



| <span data-ttu-id="e9489-242">Requisito</span><span class="sxs-lookup"><span data-stu-id="e9489-242">Requirement</span></span> | <span data-ttu-id="e9489-243">Valore</span><span class="sxs-lookup"><span data-stu-id="e9489-243">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e9489-244">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e9489-244">Minimum supported client</span></span><br/> | <span data-ttu-id="e9489-245">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e9489-245">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e9489-246">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e9489-246">Minimum supported server</span></span><br/> | <span data-ttu-id="e9489-247">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e9489-247">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e9489-248">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="e9489-248">Namespace</span></span><br/>                | <span data-ttu-id="e9489-249">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="e9489-249">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e9489-250">MOF</span><span class="sxs-lookup"><span data-stu-id="e9489-250">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e9489-251"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e9489-251"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e9489-252">DLL</span><span class="sxs-lookup"><span data-stu-id="e9489-252">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e9489-253"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e9489-253"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9489-254">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e9489-254">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9489-255">Classi hardware del sistema del computer</span><span class="sxs-lookup"><span data-stu-id="e9489-255">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="e9489-256">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="e9489-256">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="e9489-257">Attività WMI: rete</span><span class="sxs-lookup"><span data-stu-id="e9489-257">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="e9489-258">Attività WMI: account e domini</span><span class="sxs-lookup"><span data-stu-id="e9489-258">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="e9489-259">Supporto di IPv6 e IPv4 in WMI</span><span class="sxs-lookup"><span data-stu-id="e9489-259">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

