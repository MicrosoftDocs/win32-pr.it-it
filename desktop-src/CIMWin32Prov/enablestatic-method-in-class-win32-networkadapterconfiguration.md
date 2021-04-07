---
description: Il metodo della classe WMI EnableStatic consente l'indirizzamento TCP/IP statico per la scheda di rete di destinazione. Di conseguenza, DHCP per questa scheda di rete è disabilitato.
ms.assetid: d0076424-58c0-4cfe-b55b-44c0f2620388
ms.tgt_platform: multiple
title: Metodo EnableStatic della classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.EnableStatic
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 74a7b9ca8c8016cca5a78f2e7fe753f00398193e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748143"
---
# <a name="enablestatic-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="ef1b1-104">Metodo EnableStatic della \_ classe NetworkAdapterConfiguration Win32</span><span class="sxs-lookup"><span data-stu-id="ef1b1-104">EnableStatic method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="ef1b1-105">Il metodo della [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **EnableStatic** consente l'indirizzamento TCP/IP statico per la scheda di rete di destinazione.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-105">The **EnableStatic** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method enables static TCP/IP addressing for the target network adapter.</span></span> <span data-ttu-id="ef1b1-106">Di conseguenza, DHCP per questa scheda di rete è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-106">As a result, DHCP for this network adapter is disabled.</span></span>

<span data-ttu-id="ef1b1-107">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="ef1b1-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="ef1b1-108">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="ef1b1-108">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="ef1b1-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ef1b1-109">Syntax</span></span>


```mof
uint32 EnableStatic(
  [in] string IPAddress[],
  [in] string SubnetMask[]
);
```



## <a name="parameters"></a><span data-ttu-id="ef1b1-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="ef1b1-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef1b1-111">*Indirizzo IP* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ef1b1-111">*IPAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef1b1-112">Elenca tutti gli indirizzi IP statici per la scheda di rete corrente.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-112">Lists all of the static IP addresses for the current network adapter.</span></span>

<span data-ttu-id="ef1b1-113">Esempio: 155.34.22.0.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-113">Example: 155.34.22.0.</span></span>

</dd> <dt>

<span data-ttu-id="ef1b1-114">*Subnet mask* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ef1b1-114">*SubnetMask* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef1b1-115">Subnet mask che integrano i valori nel parametro *IPAddress* .</span><span class="sxs-lookup"><span data-stu-id="ef1b1-115">Subnet masks that complement the values in the *IPAddress* parameter.</span></span>

<span data-ttu-id="ef1b1-116">Esempio: 255.255.0.0.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-116">Example: 255.255.0.0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef1b1-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ef1b1-117">Return value</span></span>

<span data-ttu-id="ef1b1-118">Restituisce un valore pari a 0 (zero) per un completamento corretto quando non è richiesto un riavvio, 1 (uno) per un completamento corretto quando è necessario un riavvio e qualsiasi altro numero se si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-118">Returns a value of 0 (zero) for a successful completion when a reboot is not required, 1 (one) for a successful completion when a reboot is required, and any other number if there is an error.</span></span> <span data-ttu-id="ef1b1-119">Per ulteriori informazioni sui codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="ef1b1-119">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="ef1b1-120">Per i valori **HRESULT** generali, vedere [codici di errore di sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="ef1b1-120">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="ef1b1-121">**Operazione completata, non è necessario riavviare il computer**</span><span class="sxs-lookup"><span data-stu-id="ef1b1-121">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="ef1b1-122">0</span><span class="sxs-lookup"><span data-stu-id="ef1b1-122">0</span></span>

<span data-ttu-id="ef1b1-123">Operazione completata, non è necessario riavviare il computer.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-123">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="ef1b1-124">**Operazione completata, riavvio richiesto**</span><span class="sxs-lookup"><span data-stu-id="ef1b1-124">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="ef1b1-125">1</span><span class="sxs-lookup"><span data-stu-id="ef1b1-125">1</span></span>

<span data-ttu-id="ef1b1-126">Operazione completata, è necessario riavviare il computer.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-126">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="ef1b1-127">**Metodo non supportato in questa piattaforma**</span><span class="sxs-lookup"><span data-stu-id="ef1b1-127">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="ef1b1-128">64</span><span class="sxs-lookup"><span data-stu-id="ef1b1-128">64</span></span>

<span data-ttu-id="ef1b1-129">Metodo non supportato in questa piattaforma.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-129">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="ef1b1-130">**Errore sconosciuto**</span><span class="sxs-lookup"><span data-stu-id="ef1b1-130">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="ef1b1-131">65</span><span class="sxs-lookup"><span data-stu-id="ef1b1-131">65</span></span>

<span data-ttu-id="ef1b1-132">Errore sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-132">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="ef1b1-133">**subnet mask non valido**</span><span class="sxs-lookup"><span data-stu-id="ef1b1-133">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="ef1b1-134">66</span><span class="sxs-lookup"><span data-stu-id="ef1b1-134">66</span></span>

<span data-ttu-id="ef1b1-135">Subnet mask non valido.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-135">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="ef1b1-136">**Si è verificato un errore durante l'elaborazione di un'istanza restituita**</span><span class="sxs-lookup"><span data-stu-id="ef1b1-136">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="ef1b1-137">67</span><span class="sxs-lookup"><span data-stu-id="ef1b1-137">67</span></span>

<span data-ttu-id="ef1b1-138">Si è verificato un errore durante l'elaborazione di un'istanza di restituita.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-138">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="ef1b1-139">**Parametro di input non valido**</span><span class="sxs-lookup"><span data-stu-id="ef1b1-139">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="ef1b1-140">68</span><span class="sxs-lookup"><span data-stu-id="ef1b1-140">68</span></span>

<span data-ttu-id="ef1b1-141">Parametro di input non valido.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-141">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="ef1b1-142">**Sono stati specificati più di 5 gateway**</span><span class="sxs-lookup"><span data-stu-id="ef1b1-142">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="ef1b1-143">69</span><span class="sxs-lookup"><span data-stu-id="ef1b1-143">69</span></span>

<span data-ttu-id="ef1b1-144">Sono stati specificati più di cinque gateway.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-144">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="ef1b1-145">**Indirizzo IP non valido**</span><span class="sxs-lookup"><span data-stu-id="ef1b1-145">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="ef1b1-146">70</span><span class="sxs-lookup"><span data-stu-id="ef1b1-146">70</span></span>

<span data-ttu-id="ef1b1-147">Indirizzo IP non valido.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-147">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="ef1b1-148">**Indirizzo IP gateway non valido**</span><span class="sxs-lookup"><span data-stu-id="ef1b1-148">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="ef1b1-149">71</span><span class="sxs-lookup"><span data-stu-id="ef1b1-149">71</span></span>

<span data-ttu-id="ef1b1-150">Indirizzo IP del gateway non valido.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-150">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="ef1b1-151">**Si è verificato un errore durante l'accesso al registro di sistema per le informazioni richieste**</span><span class="sxs-lookup"><span data-stu-id="ef1b1-151">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="ef1b1-152">72</span><span class="sxs-lookup"><span data-stu-id="ef1b1-152">72</span></span>

<span data-ttu-id="ef1b1-153">Si è verificato un errore durante l'accesso al registro di sistema per le informazioni richieste.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-153">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="ef1b1-154">**Nome di dominio non valido**</span><span class="sxs-lookup"><span data-stu-id="ef1b1-154">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="ef1b1-155">73</span><span class="sxs-lookup"><span data-stu-id="ef1b1-155">73</span></span>

<span data-ttu-id="ef1b1-156">Nome di dominio non valido.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-156">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="ef1b1-157">**Nome host non valido**</span><span class="sxs-lookup"><span data-stu-id="ef1b1-157">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="ef1b1-158">74</span><span class="sxs-lookup"><span data-stu-id="ef1b1-158">74</span></span>

<span data-ttu-id="ef1b1-159">Nome host non valido.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-159">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="ef1b1-160">**Nessun server WINS primario/secondario definito**</span><span class="sxs-lookup"><span data-stu-id="ef1b1-160">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="ef1b1-161">75</span><span class="sxs-lookup"><span data-stu-id="ef1b1-161">75</span></span>

<span data-ttu-id="ef1b1-162">Nessun server WINS primario o secondario definito.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-162">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="ef1b1-163">**File non valido**</span><span class="sxs-lookup"><span data-stu-id="ef1b1-163">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="ef1b1-164">76</span><span class="sxs-lookup"><span data-stu-id="ef1b1-164">76</span></span>

<span data-ttu-id="ef1b1-165">File non valido.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-165">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="ef1b1-166">**Percorso di sistema non valido**</span><span class="sxs-lookup"><span data-stu-id="ef1b1-166">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="ef1b1-167">77</span><span class="sxs-lookup"><span data-stu-id="ef1b1-167">77</span></span>

<span data-ttu-id="ef1b1-168">Percorso di sistema non valido.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-168">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="ef1b1-169">**Copia del file non riuscita**</span><span class="sxs-lookup"><span data-stu-id="ef1b1-169">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="ef1b1-170">78</span><span class="sxs-lookup"><span data-stu-id="ef1b1-170">78</span></span>

<span data-ttu-id="ef1b1-171">Copia del file non riuscita.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-171">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="ef1b1-172">**Parametro di sicurezza non valido**</span><span class="sxs-lookup"><span data-stu-id="ef1b1-172">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="ef1b1-173">79</span><span class="sxs-lookup"><span data-stu-id="ef1b1-173">79</span></span>

<span data-ttu-id="ef1b1-174">Parametro di sicurezza non valido.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-174">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="ef1b1-175">**Impossibile configurare il servizio TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="ef1b1-175">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="ef1b1-176">80</span><span class="sxs-lookup"><span data-stu-id="ef1b1-176">80</span></span>

<span data-ttu-id="ef1b1-177">Impossibile configurare il servizio TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-177">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="ef1b1-178">**Non è possibile configurare il servizio DHCP**</span><span class="sxs-lookup"><span data-stu-id="ef1b1-178">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="ef1b1-179">81</span><span class="sxs-lookup"><span data-stu-id="ef1b1-179">81</span></span>

<span data-ttu-id="ef1b1-180">Impossibile configurare il servizio DHCP.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-180">Unable to configure DHCP service.</span></span> <span data-ttu-id="ef1b1-181">Per altre informazioni, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-181">For more information, see the Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="ef1b1-182">**Non è possibile rinnovare il lease DHCP**</span><span class="sxs-lookup"><span data-stu-id="ef1b1-182">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="ef1b1-183">82</span><span class="sxs-lookup"><span data-stu-id="ef1b1-183">82</span></span>

<span data-ttu-id="ef1b1-184">Non è possibile rinnovare il lease DHCP.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-184">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="ef1b1-185">**Non è possibile rilasciare il lease DHCP**</span><span class="sxs-lookup"><span data-stu-id="ef1b1-185">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="ef1b1-186">83</span><span class="sxs-lookup"><span data-stu-id="ef1b1-186">83</span></span>

<span data-ttu-id="ef1b1-187">Impossibile rilasciare il lease DHCP.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-187">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="ef1b1-188">**IP non abilitato sulla scheda**</span><span class="sxs-lookup"><span data-stu-id="ef1b1-188">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="ef1b1-189">84</span><span class="sxs-lookup"><span data-stu-id="ef1b1-189">84</span></span>

<span data-ttu-id="ef1b1-190">IP non abilitato sulla scheda.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-190">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="ef1b1-191">**IPX non abilitato sull'adapter**</span><span class="sxs-lookup"><span data-stu-id="ef1b1-191">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="ef1b1-192">85</span><span class="sxs-lookup"><span data-stu-id="ef1b1-192">85</span></span>

<span data-ttu-id="ef1b1-193">IPX non abilitato sulla scheda.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-193">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="ef1b1-194">**Errore limite numero frame/rete**</span><span class="sxs-lookup"><span data-stu-id="ef1b1-194">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="ef1b1-195">86</span><span class="sxs-lookup"><span data-stu-id="ef1b1-195">86</span></span>

<span data-ttu-id="ef1b1-196">Errore dei limiti del numero di rete o del frame.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-196">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="ef1b1-197">**Tipo di frame non valido**</span><span class="sxs-lookup"><span data-stu-id="ef1b1-197">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="ef1b1-198">87</span><span class="sxs-lookup"><span data-stu-id="ef1b1-198">87</span></span>

<span data-ttu-id="ef1b1-199">Tipo di frame non valido.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-199">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="ef1b1-200">**Numero di rete non valido**</span><span class="sxs-lookup"><span data-stu-id="ef1b1-200">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="ef1b1-201">88</span><span class="sxs-lookup"><span data-stu-id="ef1b1-201">88</span></span>

<span data-ttu-id="ef1b1-202">Numero di rete non valido.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-202">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="ef1b1-203">**Numero di rete duplicato**</span><span class="sxs-lookup"><span data-stu-id="ef1b1-203">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="ef1b1-204">89</span><span class="sxs-lookup"><span data-stu-id="ef1b1-204">89</span></span>

<span data-ttu-id="ef1b1-205">Numero di rete duplicato.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-205">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="ef1b1-206">**Parametro fuori limite**</span><span class="sxs-lookup"><span data-stu-id="ef1b1-206">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="ef1b1-207">90</span><span class="sxs-lookup"><span data-stu-id="ef1b1-207">90</span></span>

<span data-ttu-id="ef1b1-208">Parametro fuori limite.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-208">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="ef1b1-209">**Accesso negato**</span><span class="sxs-lookup"><span data-stu-id="ef1b1-209">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="ef1b1-210">91</span><span class="sxs-lookup"><span data-stu-id="ef1b1-210">91</span></span>

<span data-ttu-id="ef1b1-211">Accesso negato.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-211">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="ef1b1-212">**Memoria insufficiente**</span><span class="sxs-lookup"><span data-stu-id="ef1b1-212">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="ef1b1-213">92</span><span class="sxs-lookup"><span data-stu-id="ef1b1-213">92</span></span>

<span data-ttu-id="ef1b1-214">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-214">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="ef1b1-215">**Esiste già**</span><span class="sxs-lookup"><span data-stu-id="ef1b1-215">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="ef1b1-216">93</span><span class="sxs-lookup"><span data-stu-id="ef1b1-216">93</span></span>

<span data-ttu-id="ef1b1-217">Esiste già.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-217">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="ef1b1-218">**Percorso, file o oggetto non trovato**</span><span class="sxs-lookup"><span data-stu-id="ef1b1-218">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="ef1b1-219">94</span><span class="sxs-lookup"><span data-stu-id="ef1b1-219">94</span></span>

<span data-ttu-id="ef1b1-220">Il percorso, il file o l'oggetto non è stato trovato.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-220">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="ef1b1-221">**Non è possibile inviare una notifica al servizio**</span><span class="sxs-lookup"><span data-stu-id="ef1b1-221">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="ef1b1-222">95</span><span class="sxs-lookup"><span data-stu-id="ef1b1-222">95</span></span>

<span data-ttu-id="ef1b1-223">Impossibile notificare il servizio.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-223">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="ef1b1-224">**Non è possibile inviare una notifica al servizio DNS**</span><span class="sxs-lookup"><span data-stu-id="ef1b1-224">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="ef1b1-225">96</span><span class="sxs-lookup"><span data-stu-id="ef1b1-225">96</span></span>

<span data-ttu-id="ef1b1-226">Impossibile inviare una notifica al servizio DNS.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-226">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="ef1b1-227">**Interfaccia non configurabile**</span><span class="sxs-lookup"><span data-stu-id="ef1b1-227">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="ef1b1-228">97</span><span class="sxs-lookup"><span data-stu-id="ef1b1-228">97</span></span>

<span data-ttu-id="ef1b1-229">Interfaccia non configurabile.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-229">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="ef1b1-230">**Non tutti i lease DHCP possono essere rilasciati/rinnovati**</span><span class="sxs-lookup"><span data-stu-id="ef1b1-230">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="ef1b1-231">98</span><span class="sxs-lookup"><span data-stu-id="ef1b1-231">98</span></span>

<span data-ttu-id="ef1b1-232">Non tutti i lease DHCP possono essere rilasciati o rinnovati.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-232">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="ef1b1-233">**DHCP non abilitato sull'adapter**</span><span class="sxs-lookup"><span data-stu-id="ef1b1-233">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="ef1b1-234">100</span><span class="sxs-lookup"><span data-stu-id="ef1b1-234">100</span></span>

<span data-ttu-id="ef1b1-235">DHCP non abilitato sulla scheda.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-235">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="ef1b1-236">**2147786788**</span><span class="sxs-lookup"><span data-stu-id="ef1b1-236">**2147786788**</span></span>
</dt> <dd>

<span data-ttu-id="ef1b1-237">Il blocco di scrittura non è abilitato.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-237">Write lock not enabled.</span></span> <span data-ttu-id="ef1b1-238">Per ulteriori informazioni, vedere [**INetCfgLock:: AcquireWriteLock**](/previous-versions/windows/hardware/network/ff547914(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ef1b1-238">For more information, see [**INetCfgLock::AcquireWriteLock**](/previous-versions/windows/hardware/network/ff547914(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="ef1b1-239">**Altri**</span><span class="sxs-lookup"><span data-stu-id="ef1b1-239">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="ef1b1-240">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="ef1b1-240">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ef1b1-241">Commenti</span><span class="sxs-lookup"><span data-stu-id="ef1b1-241">Remarks</span></span>

<span data-ttu-id="ef1b1-242">Quando si utilizza **EnableStatic** per modificare l'indirizzo IP del computer remoto, mentre si è connessi tramite tale adapter, è probabile che si elimini la connessione al computer remoto e si riceva un messaggio di errore RPC non disponibile.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-242">When using **EnableStatic** to change the IP address of the remote computer, while being connected through that adapter, you will likely loose connection to the remote computer, and receive an RPC not available error-message.</span></span> <span data-ttu-id="ef1b1-243">(le impostazioni vengono tuttavia modificate).</span><span class="sxs-lookup"><span data-stu-id="ef1b1-243">(the settings are changed however).</span></span> <span data-ttu-id="ef1b1-244">Per evitare questo scenario, è consigliabile modificare il gateway e/o le impostazioni DNS prima di impostare l'indirizzo IP della scheda.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-244">To avoid this scenario, consider changing the Gateway and/or DNS-settings prior to setting the adapter's IP-address.</span></span>

<span data-ttu-id="ef1b1-245">Quando si usa **EnableStatic** per assegnare a un adapter una configurazione IP statica, la funzione restituisce un "81-Impossibile configurare il servizio DHCP" se l'adapter è già configurato con un indirizzo statico.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-245">When using **EnableStatic** to give an adapter a static IP configuration, the function returns an "81 - Unable to configure DHCP service" if the adapter is already configured with a static address.</span></span> <span data-ttu-id="ef1b1-246">Tuttavia, la funzione riesce comunque a impostare con la nuova operazione.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-246">However, the function still succeeds in setting with the new operation.</span></span>

## <a name="examples"></a><span data-ttu-id="ef1b1-247">Esempio</span><span class="sxs-lookup"><span data-stu-id="ef1b1-247">Examples</span></span>

<span data-ttu-id="ef1b1-248">L' [indirizzo IP statico e quindi un join a un](https://Gallery.TechNet.Microsoft.Com/Static-IP-and-then-join-to-130d4b8a) esempio di codice PowerShell di dominio, nella raccolta TechNet, USA **EnableStatic** per aggiungere un indirizzo IP statico a un computer locale.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-248">The [Static IP and then join to a domain](https://Gallery.TechNet.Microsoft.Com/Static-IP-and-then-join-to-130d4b8a) PowerShell code sample, on TechNet Gallery, uses **EnableStatic** to add a static IP to a local machine.</span></span>

<span data-ttu-id="ef1b1-249">Nell'esempio relativo all' [assegnazione di un indirizzo IP statico](https://Gallery.TechNet.Microsoft.Com/8979c752-8288-4a18-b5ed-f3b79f013f4a) di codice VBScript, nella raccolta TechNet, viene utilizzato **EnableStatic** per impostare l'indirizzo IP di un computer.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-249">The [Assign a Static IP Address](https://Gallery.TechNet.Microsoft.Com/8979c752-8288-4a18-b5ed-f3b79f013f4a) VBScript code example, on TechNet Gallery, uses **EnableStatic** to set the IP address of a computer.</span></span>

<span data-ttu-id="ef1b1-250">Nell'esempio VBScript seguente viene illustrato come disabilitare l'utilizzo DHCP in un'istanza di [**Win32 \_ NetworkAdapterConfiguration**](win32-networkadapterconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="ef1b1-250">The following VBScript sample demonstrates how to disable DHCP use on an instance of [**Win32\_NetworkAdapterConfiguration**](win32-networkadapterconfiguration.md).</span></span> <span data-ttu-id="ef1b1-251">In questo caso viene specificato l'adapter con un indice pari a 0.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-251">In this case we specify the adapter with an Index of 0.</span></span> <span data-ttu-id="ef1b1-252">È necessario selezionare l'indice corretto dalle \_ istanze di NetworkAdapter Win32 per altre interfacce.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-252">The correct index should be selected from Win32\_NetworkAdapter instances for other interfaces.</span></span>

> [!Note]  
> <span data-ttu-id="ef1b1-253">Questo script si applica solo ai sistemi basati su NT modificare le variabili di IPADDR e subnet seguenti con i valori che si desidera applicare alla scheda.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-253">This script only applies to NT-based systems Change the ipaddr and subnet variables below to the values you wish to apply to the adapter.</span></span>

 


```VB
Set Adapter = GetObject("winmgmts:Win32_NetworkAdapterConfiguration=1")

ipaddr = Array("1.1.1.1")
subnet = Array("255.255.255.0")


RetVal = Adapter.EnableStatic(ipaddr,subnet)

if RetVal = 0 then 
 WScript.Echo "DHCP disabled, using static IP address"
else 
 WScript.Echo "DHCP disable failed"
end if
```



<span data-ttu-id="ef1b1-254">Nell'esempio Perl seguente viene illustrato come disabilitare l'utilizzo DHCP in un'istanza di [**Win32 \_ NetworkAdapterConfiguration**](win32-networkadapterconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="ef1b1-254">The following Perl sample demonstrates how to disable DHCP use on an instance of [**Win32\_NetworkAdapterConfiguration**](win32-networkadapterconfiguration.md).</span></span> <span data-ttu-id="ef1b1-255">In questo caso viene specificato l'adapter con un indice pari a 0.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-255">In this case we specify the adapter with an Index of 0.</span></span> <span data-ttu-id="ef1b1-256">È necessario selezionare l'indice corretto dalle \_ istanze di NetworkAdapter Win32 per altre interfacce.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-256">The correct index should be selected from Win32\_NetworkAdapter instances for other interfaces.</span></span>

> [!Note]  
> <span data-ttu-id="ef1b1-257">Questo script si applica solo ai sistemi basati su NT modificare le variabili di IPADDR e subnet seguenti con i valori che si desidera applicare alla scheda.</span><span class="sxs-lookup"><span data-stu-id="ef1b1-257">This script only applies to NT-based systems Change the ipaddr and subnet variables below to the values you wish to apply to the adapter.</span></span>

 


```
use strict;
use Win32::OLE;

my ($Adapter, @ipaddr, @subnet, $RetVal);  
eval { $Adapter = 
 Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\cimv2:Win32_NetworkAdapterConfiguration.Index=\"0\""); };

unless ($@) 
{
 push @ipaddr, "192.168.144.107";
 push @subnet, "255.255.255.0";

 $RetVal = $Adapter->EnableStatic(\@ipaddr, \@subnet);

 if ($RetVal == 0) 
 {
  print "\nDHCP disabled, using static IP address\n";
 }
 else 
 {
  print "\nDHCP disable failed\n";
 }
}
else
{
 print STDERR "\n", Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a><span data-ttu-id="ef1b1-258">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ef1b1-258">Requirements</span></span>



| <span data-ttu-id="ef1b1-259">Requisito</span><span class="sxs-lookup"><span data-stu-id="ef1b1-259">Requirement</span></span> | <span data-ttu-id="ef1b1-260">Valore</span><span class="sxs-lookup"><span data-stu-id="ef1b1-260">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ef1b1-261">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ef1b1-261">Minimum supported client</span></span><br/> | <span data-ttu-id="ef1b1-262">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ef1b1-262">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ef1b1-263">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ef1b1-263">Minimum supported server</span></span><br/> | <span data-ttu-id="ef1b1-264">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ef1b1-264">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ef1b1-265">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ef1b1-265">Namespace</span></span><br/>                | <span data-ttu-id="ef1b1-266">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="ef1b1-266">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ef1b1-267">MOF</span><span class="sxs-lookup"><span data-stu-id="ef1b1-267">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ef1b1-268"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ef1b1-268"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ef1b1-269">DLL</span><span class="sxs-lookup"><span data-stu-id="ef1b1-269">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ef1b1-270"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ef1b1-270"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef1b1-271">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ef1b1-271">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef1b1-272">Classi hardware del sistema del computer</span><span class="sxs-lookup"><span data-stu-id="ef1b1-272">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="ef1b1-273">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="ef1b1-273">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="ef1b1-274">Attività WMI: rete</span><span class="sxs-lookup"><span data-stu-id="ef1b1-274">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="ef1b1-275">Attività WMI: account e domini</span><span class="sxs-lookup"><span data-stu-id="ef1b1-275">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="ef1b1-276">Supporto di IPv6 e IPv4 in WMI</span><span class="sxs-lookup"><span data-stu-id="ef1b1-276">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

