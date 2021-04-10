---
description: Il metodo della classe WMI SetDNSDomain consente l'impostazione del dominio DNS.
ms.assetid: a531133e-1b7c-4d85-979d-63bf4f7c9bed
ms.tgt_platform: multiple
title: Metodo SetDNSDomain della classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetDNSDomain
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: c440d8cb5c720bf6922707f04bc75e2383755c1e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225744"
---
# <a name="setdnsdomain-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="1b4a7-103">Metodo SetDNSDomain della \_ classe NetworkAdapterConfiguration Win32</span><span class="sxs-lookup"><span data-stu-id="1b4a7-103">SetDNSDomain method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="1b4a7-104">Il metodo della [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetDNSDomain** consente l'impostazione del dominio DNS.</span><span class="sxs-lookup"><span data-stu-id="1b4a7-104">The **SetDNSDomain** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method allows for the setting of the DNS domain.</span></span>

<span data-ttu-id="1b4a7-105">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="1b4a7-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="1b4a7-106">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="1b4a7-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="1b4a7-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1b4a7-107">Syntax</span></span>


```mof
uint32 SetDNSDomain(
  [in] string DNSDomain
);
```



## <a name="parameters"></a><span data-ttu-id="1b4a7-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="1b4a7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b4a7-109">*Dnsdomain* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1b4a7-109">*DNSDomain* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b4a7-110">Dominio a cui è associato il DNS, rappresentato da un nome di organizzazione seguito da un punto e un'estensione che indica il tipo di organizzazione.</span><span class="sxs-lookup"><span data-stu-id="1b4a7-110">Domain with which the DNS is associated, represented by an organization name followed by a period and an extension that indicates the type of organization.</span></span>

<span data-ttu-id="1b4a7-111">Esempio: "microsoft.com"</span><span class="sxs-lookup"><span data-stu-id="1b4a7-111">Example: "microsoft.com"</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1b4a7-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1b4a7-112">Return value</span></span>

<span data-ttu-id="1b4a7-113">Restituisce un valore pari a 0 (zero) per un completamento corretto quando non è richiesto il riavvio, 1 (uno) per un completamento corretto quando è necessario un riavvio e un numero diverso se si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="1b4a7-113">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required and a different number if there is an error.</span></span> <span data-ttu-id="1b4a7-114">Per ulteriori informazioni sui codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="1b4a7-114">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="1b4a7-115">Per i valori **HRESULT** generali, vedere [codici di errore di sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="1b4a7-115">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="1b4a7-116">**Operazione completata, non è necessario riavviare il computer**</span><span class="sxs-lookup"><span data-stu-id="1b4a7-116">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="1b4a7-117">0</span><span class="sxs-lookup"><span data-stu-id="1b4a7-117">0</span></span>

<span data-ttu-id="1b4a7-118">Operazione completata, non è necessario riavviare il computer.</span><span class="sxs-lookup"><span data-stu-id="1b4a7-118">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="1b4a7-119">**Operazione completata, riavvio richiesto**</span><span class="sxs-lookup"><span data-stu-id="1b4a7-119">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="1b4a7-120">1</span><span class="sxs-lookup"><span data-stu-id="1b4a7-120">1</span></span>

<span data-ttu-id="1b4a7-121">Operazione completata, è necessario riavviare il computer.</span><span class="sxs-lookup"><span data-stu-id="1b4a7-121">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="1b4a7-122">**Metodo non supportato in questa piattaforma**</span><span class="sxs-lookup"><span data-stu-id="1b4a7-122">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="1b4a7-123">64</span><span class="sxs-lookup"><span data-stu-id="1b4a7-123">64</span></span>

<span data-ttu-id="1b4a7-124">Metodo non supportato in questa piattaforma.</span><span class="sxs-lookup"><span data-stu-id="1b4a7-124">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="1b4a7-125">**Errore sconosciuto**</span><span class="sxs-lookup"><span data-stu-id="1b4a7-125">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="1b4a7-126">65</span><span class="sxs-lookup"><span data-stu-id="1b4a7-126">65</span></span>

<span data-ttu-id="1b4a7-127">Errore sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="1b4a7-127">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="1b4a7-128">**subnet mask non valido**</span><span class="sxs-lookup"><span data-stu-id="1b4a7-128">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="1b4a7-129">66</span><span class="sxs-lookup"><span data-stu-id="1b4a7-129">66</span></span>

<span data-ttu-id="1b4a7-130">Subnet mask non valido.</span><span class="sxs-lookup"><span data-stu-id="1b4a7-130">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="1b4a7-131">**Si è verificato un errore durante l'elaborazione di un'istanza restituita**</span><span class="sxs-lookup"><span data-stu-id="1b4a7-131">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="1b4a7-132">67</span><span class="sxs-lookup"><span data-stu-id="1b4a7-132">67</span></span>

<span data-ttu-id="1b4a7-133">Si è verificato un errore durante l'elaborazione di un'istanza di restituita.</span><span class="sxs-lookup"><span data-stu-id="1b4a7-133">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="1b4a7-134">**Parametro di input non valido**</span><span class="sxs-lookup"><span data-stu-id="1b4a7-134">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="1b4a7-135">68</span><span class="sxs-lookup"><span data-stu-id="1b4a7-135">68</span></span>

<span data-ttu-id="1b4a7-136">Parametro di input non valido.</span><span class="sxs-lookup"><span data-stu-id="1b4a7-136">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="1b4a7-137">**Sono stati specificati più di 5 gateway**</span><span class="sxs-lookup"><span data-stu-id="1b4a7-137">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="1b4a7-138">69</span><span class="sxs-lookup"><span data-stu-id="1b4a7-138">69</span></span>

<span data-ttu-id="1b4a7-139">Sono stati specificati più di cinque gateway.</span><span class="sxs-lookup"><span data-stu-id="1b4a7-139">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="1b4a7-140">**Indirizzo IP non valido**</span><span class="sxs-lookup"><span data-stu-id="1b4a7-140">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="1b4a7-141">70</span><span class="sxs-lookup"><span data-stu-id="1b4a7-141">70</span></span>

<span data-ttu-id="1b4a7-142">Indirizzo IP non valido.</span><span class="sxs-lookup"><span data-stu-id="1b4a7-142">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="1b4a7-143">**Indirizzo IP gateway non valido**</span><span class="sxs-lookup"><span data-stu-id="1b4a7-143">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="1b4a7-144">71</span><span class="sxs-lookup"><span data-stu-id="1b4a7-144">71</span></span>

<span data-ttu-id="1b4a7-145">Indirizzo IP del gateway non valido.</span><span class="sxs-lookup"><span data-stu-id="1b4a7-145">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="1b4a7-146">**Si è verificato un errore durante l'accesso al registro di sistema per le informazioni richieste**</span><span class="sxs-lookup"><span data-stu-id="1b4a7-146">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="1b4a7-147">72</span><span class="sxs-lookup"><span data-stu-id="1b4a7-147">72</span></span>

<span data-ttu-id="1b4a7-148">Si è verificato un errore durante l'accesso al registro di sistema per le informazioni richieste.</span><span class="sxs-lookup"><span data-stu-id="1b4a7-148">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="1b4a7-149">**Nome di dominio non valido**</span><span class="sxs-lookup"><span data-stu-id="1b4a7-149">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="1b4a7-150">73</span><span class="sxs-lookup"><span data-stu-id="1b4a7-150">73</span></span>

<span data-ttu-id="1b4a7-151">Nome di dominio non valido.</span><span class="sxs-lookup"><span data-stu-id="1b4a7-151">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="1b4a7-152">**Nome host non valido**</span><span class="sxs-lookup"><span data-stu-id="1b4a7-152">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="1b4a7-153">74</span><span class="sxs-lookup"><span data-stu-id="1b4a7-153">74</span></span>

<span data-ttu-id="1b4a7-154">Nome host non valido.</span><span class="sxs-lookup"><span data-stu-id="1b4a7-154">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="1b4a7-155">**Nessun server WINS primario/secondario definito**</span><span class="sxs-lookup"><span data-stu-id="1b4a7-155">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="1b4a7-156">75</span><span class="sxs-lookup"><span data-stu-id="1b4a7-156">75</span></span>

<span data-ttu-id="1b4a7-157">Nessun server WINS primario o secondario definito.</span><span class="sxs-lookup"><span data-stu-id="1b4a7-157">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="1b4a7-158">**File non valido**</span><span class="sxs-lookup"><span data-stu-id="1b4a7-158">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="1b4a7-159">76</span><span class="sxs-lookup"><span data-stu-id="1b4a7-159">76</span></span>

<span data-ttu-id="1b4a7-160">File non valido.</span><span class="sxs-lookup"><span data-stu-id="1b4a7-160">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="1b4a7-161">**Percorso di sistema non valido**</span><span class="sxs-lookup"><span data-stu-id="1b4a7-161">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="1b4a7-162">77</span><span class="sxs-lookup"><span data-stu-id="1b4a7-162">77</span></span>

<span data-ttu-id="1b4a7-163">Percorso di sistema non valido.</span><span class="sxs-lookup"><span data-stu-id="1b4a7-163">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="1b4a7-164">**Copia del file non riuscita**</span><span class="sxs-lookup"><span data-stu-id="1b4a7-164">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="1b4a7-165">78</span><span class="sxs-lookup"><span data-stu-id="1b4a7-165">78</span></span>

<span data-ttu-id="1b4a7-166">Copia del file non riuscita.</span><span class="sxs-lookup"><span data-stu-id="1b4a7-166">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="1b4a7-167">**Parametro di sicurezza non valido**</span><span class="sxs-lookup"><span data-stu-id="1b4a7-167">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="1b4a7-168">79</span><span class="sxs-lookup"><span data-stu-id="1b4a7-168">79</span></span>

<span data-ttu-id="1b4a7-169">Parametro di sicurezza non valido.</span><span class="sxs-lookup"><span data-stu-id="1b4a7-169">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="1b4a7-170">**Impossibile configurare il servizio TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="1b4a7-170">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="1b4a7-171">80</span><span class="sxs-lookup"><span data-stu-id="1b4a7-171">80</span></span>

<span data-ttu-id="1b4a7-172">Impossibile configurare il servizio TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="1b4a7-172">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="1b4a7-173">**Non è possibile configurare il servizio DHCP**</span><span class="sxs-lookup"><span data-stu-id="1b4a7-173">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="1b4a7-174">81</span><span class="sxs-lookup"><span data-stu-id="1b4a7-174">81</span></span>

<span data-ttu-id="1b4a7-175">Impossibile configurare il servizio DHCP.</span><span class="sxs-lookup"><span data-stu-id="1b4a7-175">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="1b4a7-176">**Non è possibile rinnovare il lease DHCP**</span><span class="sxs-lookup"><span data-stu-id="1b4a7-176">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="1b4a7-177">82</span><span class="sxs-lookup"><span data-stu-id="1b4a7-177">82</span></span>

<span data-ttu-id="1b4a7-178">Non è possibile rinnovare il lease DHCP.</span><span class="sxs-lookup"><span data-stu-id="1b4a7-178">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="1b4a7-179">**Non è possibile rilasciare il lease DHCP**</span><span class="sxs-lookup"><span data-stu-id="1b4a7-179">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="1b4a7-180">83</span><span class="sxs-lookup"><span data-stu-id="1b4a7-180">83</span></span>

<span data-ttu-id="1b4a7-181">Impossibile rilasciare il lease DHCP.</span><span class="sxs-lookup"><span data-stu-id="1b4a7-181">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="1b4a7-182">**IP non abilitato sulla scheda**</span><span class="sxs-lookup"><span data-stu-id="1b4a7-182">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="1b4a7-183">84</span><span class="sxs-lookup"><span data-stu-id="1b4a7-183">84</span></span>

<span data-ttu-id="1b4a7-184">IP non abilitato sulla scheda.</span><span class="sxs-lookup"><span data-stu-id="1b4a7-184">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="1b4a7-185">**IPX non abilitato sull'adapter**</span><span class="sxs-lookup"><span data-stu-id="1b4a7-185">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="1b4a7-186">85</span><span class="sxs-lookup"><span data-stu-id="1b4a7-186">85</span></span>

<span data-ttu-id="1b4a7-187">IPX non abilitato sulla scheda.</span><span class="sxs-lookup"><span data-stu-id="1b4a7-187">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="1b4a7-188">**Errore limite numero frame/rete**</span><span class="sxs-lookup"><span data-stu-id="1b4a7-188">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="1b4a7-189">86</span><span class="sxs-lookup"><span data-stu-id="1b4a7-189">86</span></span>

<span data-ttu-id="1b4a7-190">Errore dei limiti del numero di rete o del frame.</span><span class="sxs-lookup"><span data-stu-id="1b4a7-190">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="1b4a7-191">**Tipo di frame non valido**</span><span class="sxs-lookup"><span data-stu-id="1b4a7-191">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="1b4a7-192">87</span><span class="sxs-lookup"><span data-stu-id="1b4a7-192">87</span></span>

<span data-ttu-id="1b4a7-193">Tipo di frame non valido.</span><span class="sxs-lookup"><span data-stu-id="1b4a7-193">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="1b4a7-194">**Numero di rete non valido**</span><span class="sxs-lookup"><span data-stu-id="1b4a7-194">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="1b4a7-195">88</span><span class="sxs-lookup"><span data-stu-id="1b4a7-195">88</span></span>

<span data-ttu-id="1b4a7-196">Numero di rete non valido.</span><span class="sxs-lookup"><span data-stu-id="1b4a7-196">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="1b4a7-197">**Numero di rete duplicato**</span><span class="sxs-lookup"><span data-stu-id="1b4a7-197">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="1b4a7-198">89</span><span class="sxs-lookup"><span data-stu-id="1b4a7-198">89</span></span>

<span data-ttu-id="1b4a7-199">Numero di rete duplicato.</span><span class="sxs-lookup"><span data-stu-id="1b4a7-199">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="1b4a7-200">**Parametro fuori limite**</span><span class="sxs-lookup"><span data-stu-id="1b4a7-200">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="1b4a7-201">90</span><span class="sxs-lookup"><span data-stu-id="1b4a7-201">90</span></span>

<span data-ttu-id="1b4a7-202">Parametro fuori limite.</span><span class="sxs-lookup"><span data-stu-id="1b4a7-202">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="1b4a7-203">**Accesso negato**</span><span class="sxs-lookup"><span data-stu-id="1b4a7-203">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="1b4a7-204">91</span><span class="sxs-lookup"><span data-stu-id="1b4a7-204">91</span></span>

<span data-ttu-id="1b4a7-205">Accesso negato.</span><span class="sxs-lookup"><span data-stu-id="1b4a7-205">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="1b4a7-206">**Memoria insufficiente**</span><span class="sxs-lookup"><span data-stu-id="1b4a7-206">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="1b4a7-207">92</span><span class="sxs-lookup"><span data-stu-id="1b4a7-207">92</span></span>

<span data-ttu-id="1b4a7-208">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="1b4a7-208">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="1b4a7-209">**Esiste già**</span><span class="sxs-lookup"><span data-stu-id="1b4a7-209">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="1b4a7-210">93</span><span class="sxs-lookup"><span data-stu-id="1b4a7-210">93</span></span>

<span data-ttu-id="1b4a7-211">Esiste già.</span><span class="sxs-lookup"><span data-stu-id="1b4a7-211">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="1b4a7-212">**Percorso, file o oggetto non trovato**</span><span class="sxs-lookup"><span data-stu-id="1b4a7-212">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="1b4a7-213">94</span><span class="sxs-lookup"><span data-stu-id="1b4a7-213">94</span></span>

<span data-ttu-id="1b4a7-214">Il percorso, il file o l'oggetto non è stato trovato.</span><span class="sxs-lookup"><span data-stu-id="1b4a7-214">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="1b4a7-215">**Non è possibile inviare una notifica al servizio**</span><span class="sxs-lookup"><span data-stu-id="1b4a7-215">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="1b4a7-216">95</span><span class="sxs-lookup"><span data-stu-id="1b4a7-216">95</span></span>

<span data-ttu-id="1b4a7-217">Impossibile notificare il servizio.</span><span class="sxs-lookup"><span data-stu-id="1b4a7-217">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="1b4a7-218">**Non è possibile inviare una notifica al servizio DNS**</span><span class="sxs-lookup"><span data-stu-id="1b4a7-218">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="1b4a7-219">96</span><span class="sxs-lookup"><span data-stu-id="1b4a7-219">96</span></span>

<span data-ttu-id="1b4a7-220">Impossibile inviare una notifica al servizio DNS.</span><span class="sxs-lookup"><span data-stu-id="1b4a7-220">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="1b4a7-221">**Interfaccia non configurabile**</span><span class="sxs-lookup"><span data-stu-id="1b4a7-221">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="1b4a7-222">97</span><span class="sxs-lookup"><span data-stu-id="1b4a7-222">97</span></span>

<span data-ttu-id="1b4a7-223">Interfaccia non configurabile.</span><span class="sxs-lookup"><span data-stu-id="1b4a7-223">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="1b4a7-224">**Non tutti i lease DHCP possono essere rilasciati/rinnovati**</span><span class="sxs-lookup"><span data-stu-id="1b4a7-224">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="1b4a7-225">98</span><span class="sxs-lookup"><span data-stu-id="1b4a7-225">98</span></span>

<span data-ttu-id="1b4a7-226">Non tutti i lease DHCP possono essere rilasciati o rinnovati.</span><span class="sxs-lookup"><span data-stu-id="1b4a7-226">Not all DHCP leases can be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="1b4a7-227">**DHCP non abilitato sull'adapter**</span><span class="sxs-lookup"><span data-stu-id="1b4a7-227">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="1b4a7-228">100</span><span class="sxs-lookup"><span data-stu-id="1b4a7-228">100</span></span>

<span data-ttu-id="1b4a7-229">DHCP non abilitato sulla scheda.</span><span class="sxs-lookup"><span data-stu-id="1b4a7-229">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="1b4a7-230">**Altri**</span><span class="sxs-lookup"><span data-stu-id="1b4a7-230">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="1b4a7-231">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="1b4a7-231">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1b4a7-232">Commenti</span><span class="sxs-lookup"><span data-stu-id="1b4a7-232">Remarks</span></span>

<span data-ttu-id="1b4a7-233">Si tratta di una chiamata al metodo dipendente dall'istanza che viene applicata a ogni adapter.</span><span class="sxs-lookup"><span data-stu-id="1b4a7-233">This is an instance-dependent method call that applies on a per-adapter basis.</span></span> <span data-ttu-id="1b4a7-234">L'impostazione si applica all'adapter di destinazione.</span><span class="sxs-lookup"><span data-stu-id="1b4a7-234">The setting applies to the targeted adapter.</span></span>

## <a name="examples"></a><span data-ttu-id="1b4a7-235">Esempio</span><span class="sxs-lookup"><span data-stu-id="1b4a7-235">Examples</span></span>

<span data-ttu-id="1b4a7-236">L'esempio di codice di [assegnazione del dominio DNS per una scheda di rete](https://Gallery.TechNet.Microsoft.Com/6044a0a4-d320-4c18-a94b-c125796d219b) in TechNet Gallery USA **SetDNSDomain** per impostare il dominio DNS per una scheda di rete associata a TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="1b4a7-236">The [Assign the DNS Domain for a Network Adapter](https://Gallery.TechNet.Microsoft.Com/6044a0a4-d320-4c18-a94b-c125796d219b) VBScript code sample on TechNet gallery uses **SetDNSDomain** to set the DNS domain for a TCP/IP-bound network adapter.</span></span>

<span data-ttu-id="1b4a7-237">L'esempio di codice per la [modifica della configurazione TCP/IP per un computer](https://Gallery.TechNet.Microsoft.Com/3d5ae334-1d75-4cea-8079-78c6bd836faf) VBScript nella raccolta TechNet utilizza **SetDNSDomain** per modificare le impostazioni TCP/IP per una scheda di rete.</span><span class="sxs-lookup"><span data-stu-id="1b4a7-237">The [Modify the TCP/IP Configuration for a Computer](https://Gallery.TechNet.Microsoft.Com/3d5ae334-1d75-4cea-8079-78c6bd836faf) VBScript code sample on TechNet Gallery uses **SetDNSDomain** to modify TCP/IP settings for a network adapter.</span></span>

<span data-ttu-id="1b4a7-238">L'esempio [Enable DHCP settings on a computer](https://Gallery.TechNet.Microsoft.Com/41e6ab51-78c0-4413-b086-03fde33ea125) VBScript nella raccolta TechNet USA **SetDNSDomain** per configurare tutte le impostazioni in genere necessarie per abilitare DHCP in un computer.</span><span class="sxs-lookup"><span data-stu-id="1b4a7-238">The [Enable DHCP Settings on a Computer](https://Gallery.TechNet.Microsoft.Com/41e6ab51-78c0-4413-b086-03fde33ea125) VBScript sample on TechNet Gallery uses **SetDNSDomain** to configure all the settings typically required to enable DHCP on a computer.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b4a7-239">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1b4a7-239">Requirements</span></span>



| <span data-ttu-id="1b4a7-240">Requisito</span><span class="sxs-lookup"><span data-stu-id="1b4a7-240">Requirement</span></span> | <span data-ttu-id="1b4a7-241">Valore</span><span class="sxs-lookup"><span data-stu-id="1b4a7-241">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1b4a7-242">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1b4a7-242">Minimum supported client</span></span><br/> | <span data-ttu-id="1b4a7-243">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1b4a7-243">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1b4a7-244">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1b4a7-244">Minimum supported server</span></span><br/> | <span data-ttu-id="1b4a7-245">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1b4a7-245">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1b4a7-246">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="1b4a7-246">Namespace</span></span><br/>                | <span data-ttu-id="1b4a7-247">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="1b4a7-247">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1b4a7-248">MOF</span><span class="sxs-lookup"><span data-stu-id="1b4a7-248">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1b4a7-249"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1b4a7-249"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1b4a7-250">DLL</span><span class="sxs-lookup"><span data-stu-id="1b4a7-250">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1b4a7-251"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1b4a7-251"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1b4a7-252">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1b4a7-252">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b4a7-253">Classi hardware del sistema del computer</span><span class="sxs-lookup"><span data-stu-id="1b4a7-253">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="1b4a7-254">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="1b4a7-254">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="1b4a7-255">Attività WMI: rete</span><span class="sxs-lookup"><span data-stu-id="1b4a7-255">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="1b4a7-256">Attività WMI: account e domini</span><span class="sxs-lookup"><span data-stu-id="1b4a7-256">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="1b4a7-257">Supporto di IPv6 e IPv4 in WMI</span><span class="sxs-lookup"><span data-stu-id="1b4a7-257">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

