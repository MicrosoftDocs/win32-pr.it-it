---
description: Il metodo statico della classe WMI SetDefaultTTL viene usato per impostare il valore TTL (time to Live) predefinito nell'intestazione dei pacchetti IP in uscita.
ms.assetid: 74b060de-512c-407e-9f93-c3b496f8d09d
ms.tgt_platform: multiple
title: Metodo SetDefaultTTL della classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetDefaultTTL
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 253048b44a836f92646124fb972fe32c135e3b9a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877197"
---
# <a name="setdefaultttl-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="7a5fb-103">Metodo SetDefaultTTL della \_ classe NetworkAdapterConfiguration Win32</span><span class="sxs-lookup"><span data-stu-id="7a5fb-103">SetDefaultTTL method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="7a5fb-104">Il metodo statico della [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetDefaultTTL** viene usato per impostare il valore TTL (time to Live) predefinito nell'intestazione dei pacchetti IP in uscita.</span><span class="sxs-lookup"><span data-stu-id="7a5fb-104">The **SetDefaultTTL** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to set the default Time to Live (TTL) value in the header of outgoing IP packets.</span></span>

<span data-ttu-id="7a5fb-105">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="7a5fb-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="7a5fb-106">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="7a5fb-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="7a5fb-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7a5fb-107">Syntax</span></span>


```mof
uint32 SetDefaultTTL(
  [in] uint8 DefaultTTL
);
```



## <a name="parameters"></a><span data-ttu-id="7a5fb-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="7a5fb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a5fb-109">*DefaultTTL* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7a5fb-109">*DefaultTTL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a5fb-110">Valore di durata (TTL) impostato nell'intestazione dei pacchetti IP in uscita.</span><span class="sxs-lookup"><span data-stu-id="7a5fb-110">Time to Live value set in the header of outgoing IP packets.</span></span> <span data-ttu-id="7a5fb-111">Il valore predefinito è 32; Intervallo valido: 1-255</span><span class="sxs-lookup"><span data-stu-id="7a5fb-111">The default value is 32; Valid range: 1 - 255</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7a5fb-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7a5fb-112">Return value</span></span>

<span data-ttu-id="7a5fb-113">Restituisce un valore pari a 0 (zero) per un completamento corretto quando non è richiesto il riavvio, 1 (uno) per un completamento corretto quando è necessario un riavvio e un numero diverso se si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="7a5fb-113">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="7a5fb-114">Per ulteriori informazioni sui codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="7a5fb-114">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="7a5fb-115">Per i valori **HRESULT** generali, vedere [codici di errore di sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="7a5fb-115">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="7a5fb-116">**Operazione completata, non è necessario riavviare il computer**</span><span class="sxs-lookup"><span data-stu-id="7a5fb-116">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="7a5fb-117">0</span><span class="sxs-lookup"><span data-stu-id="7a5fb-117">0</span></span>

<span data-ttu-id="7a5fb-118">Operazione completata, non è necessario riavviare il computer.</span><span class="sxs-lookup"><span data-stu-id="7a5fb-118">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="7a5fb-119">**Operazione completata, riavvio richiesto**</span><span class="sxs-lookup"><span data-stu-id="7a5fb-119">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="7a5fb-120">1</span><span class="sxs-lookup"><span data-stu-id="7a5fb-120">1</span></span>

<span data-ttu-id="7a5fb-121">Operazione completata, è necessario riavviare il computer.</span><span class="sxs-lookup"><span data-stu-id="7a5fb-121">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="7a5fb-122">**Metodo non supportato in questa piattaforma**</span><span class="sxs-lookup"><span data-stu-id="7a5fb-122">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="7a5fb-123">64</span><span class="sxs-lookup"><span data-stu-id="7a5fb-123">64</span></span>

<span data-ttu-id="7a5fb-124">Metodo non supportato in questa piattaforma.</span><span class="sxs-lookup"><span data-stu-id="7a5fb-124">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="7a5fb-125">**Errore sconosciuto**</span><span class="sxs-lookup"><span data-stu-id="7a5fb-125">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="7a5fb-126">65</span><span class="sxs-lookup"><span data-stu-id="7a5fb-126">65</span></span>

<span data-ttu-id="7a5fb-127">Errore sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="7a5fb-127">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="7a5fb-128">**subnet mask non valido**</span><span class="sxs-lookup"><span data-stu-id="7a5fb-128">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="7a5fb-129">66</span><span class="sxs-lookup"><span data-stu-id="7a5fb-129">66</span></span>

<span data-ttu-id="7a5fb-130">Subnet mask non valido.</span><span class="sxs-lookup"><span data-stu-id="7a5fb-130">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="7a5fb-131">**Si è verificato un errore durante l'elaborazione di un'istanza restituita**</span><span class="sxs-lookup"><span data-stu-id="7a5fb-131">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="7a5fb-132">67</span><span class="sxs-lookup"><span data-stu-id="7a5fb-132">67</span></span>

<span data-ttu-id="7a5fb-133">Si è verificato un errore durante l'elaborazione di un'istanza di restituita.</span><span class="sxs-lookup"><span data-stu-id="7a5fb-133">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="7a5fb-134">**Parametro di input non valido**</span><span class="sxs-lookup"><span data-stu-id="7a5fb-134">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="7a5fb-135">68</span><span class="sxs-lookup"><span data-stu-id="7a5fb-135">68</span></span>

<span data-ttu-id="7a5fb-136">Parametro di input non valido.</span><span class="sxs-lookup"><span data-stu-id="7a5fb-136">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="7a5fb-137">**Sono stati specificati più di 5 gateway**</span><span class="sxs-lookup"><span data-stu-id="7a5fb-137">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="7a5fb-138">69</span><span class="sxs-lookup"><span data-stu-id="7a5fb-138">69</span></span>

<span data-ttu-id="7a5fb-139">Sono stati specificati più di cinque gateway.</span><span class="sxs-lookup"><span data-stu-id="7a5fb-139">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="7a5fb-140">**Indirizzo IP non valido**</span><span class="sxs-lookup"><span data-stu-id="7a5fb-140">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="7a5fb-141">70</span><span class="sxs-lookup"><span data-stu-id="7a5fb-141">70</span></span>

<span data-ttu-id="7a5fb-142">Indirizzo IP non valido.</span><span class="sxs-lookup"><span data-stu-id="7a5fb-142">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="7a5fb-143">**Indirizzo IP gateway non valido**</span><span class="sxs-lookup"><span data-stu-id="7a5fb-143">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="7a5fb-144">71</span><span class="sxs-lookup"><span data-stu-id="7a5fb-144">71</span></span>

<span data-ttu-id="7a5fb-145">Indirizzo IP del gateway non valido.</span><span class="sxs-lookup"><span data-stu-id="7a5fb-145">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="7a5fb-146">**Si è verificato un errore durante l'accesso al registro di sistema per le informazioni richieste**</span><span class="sxs-lookup"><span data-stu-id="7a5fb-146">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="7a5fb-147">72</span><span class="sxs-lookup"><span data-stu-id="7a5fb-147">72</span></span>

<span data-ttu-id="7a5fb-148">Si è verificato un errore durante l'accesso al registro di sistema per le informazioni richieste.</span><span class="sxs-lookup"><span data-stu-id="7a5fb-148">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="7a5fb-149">**Nome di dominio non valido**</span><span class="sxs-lookup"><span data-stu-id="7a5fb-149">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="7a5fb-150">73</span><span class="sxs-lookup"><span data-stu-id="7a5fb-150">73</span></span>

<span data-ttu-id="7a5fb-151">Nome di dominio non valido.</span><span class="sxs-lookup"><span data-stu-id="7a5fb-151">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="7a5fb-152">**Nome host non valido**</span><span class="sxs-lookup"><span data-stu-id="7a5fb-152">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="7a5fb-153">74</span><span class="sxs-lookup"><span data-stu-id="7a5fb-153">74</span></span>

<span data-ttu-id="7a5fb-154">Nome host non valido.</span><span class="sxs-lookup"><span data-stu-id="7a5fb-154">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="7a5fb-155">**Nessun server WINS primario/secondario definito**</span><span class="sxs-lookup"><span data-stu-id="7a5fb-155">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="7a5fb-156">75</span><span class="sxs-lookup"><span data-stu-id="7a5fb-156">75</span></span>

<span data-ttu-id="7a5fb-157">Nessun server WINS primario o secondario definito.</span><span class="sxs-lookup"><span data-stu-id="7a5fb-157">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="7a5fb-158">**File non valido**</span><span class="sxs-lookup"><span data-stu-id="7a5fb-158">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="7a5fb-159">76</span><span class="sxs-lookup"><span data-stu-id="7a5fb-159">76</span></span>

<span data-ttu-id="7a5fb-160">File non valido.</span><span class="sxs-lookup"><span data-stu-id="7a5fb-160">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="7a5fb-161">**Percorso di sistema non valido**</span><span class="sxs-lookup"><span data-stu-id="7a5fb-161">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="7a5fb-162">77</span><span class="sxs-lookup"><span data-stu-id="7a5fb-162">77</span></span>

<span data-ttu-id="7a5fb-163">Percorso di sistema non valido.</span><span class="sxs-lookup"><span data-stu-id="7a5fb-163">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="7a5fb-164">**Copia del file non riuscita**</span><span class="sxs-lookup"><span data-stu-id="7a5fb-164">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="7a5fb-165">78</span><span class="sxs-lookup"><span data-stu-id="7a5fb-165">78</span></span>

<span data-ttu-id="7a5fb-166">Copia del file non riuscita.</span><span class="sxs-lookup"><span data-stu-id="7a5fb-166">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="7a5fb-167">**Parametro di sicurezza non valido**</span><span class="sxs-lookup"><span data-stu-id="7a5fb-167">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="7a5fb-168">79</span><span class="sxs-lookup"><span data-stu-id="7a5fb-168">79</span></span>

<span data-ttu-id="7a5fb-169">Parametro di sicurezza non valido.</span><span class="sxs-lookup"><span data-stu-id="7a5fb-169">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="7a5fb-170">**Impossibile configurare il servizio TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="7a5fb-170">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="7a5fb-171">80</span><span class="sxs-lookup"><span data-stu-id="7a5fb-171">80</span></span>

<span data-ttu-id="7a5fb-172">Impossibile configurare il servizio TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="7a5fb-172">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="7a5fb-173">**Non è possibile configurare il servizio DHCP**</span><span class="sxs-lookup"><span data-stu-id="7a5fb-173">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="7a5fb-174">81</span><span class="sxs-lookup"><span data-stu-id="7a5fb-174">81</span></span>

<span data-ttu-id="7a5fb-175">Impossibile configurare il servizio DHCP.</span><span class="sxs-lookup"><span data-stu-id="7a5fb-175">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="7a5fb-176">**Non è possibile rinnovare il lease DHCP**</span><span class="sxs-lookup"><span data-stu-id="7a5fb-176">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="7a5fb-177">82</span><span class="sxs-lookup"><span data-stu-id="7a5fb-177">82</span></span>

<span data-ttu-id="7a5fb-178">Non è possibile rinnovare il lease DHCP.</span><span class="sxs-lookup"><span data-stu-id="7a5fb-178">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="7a5fb-179">**Non è possibile rilasciare il lease DHCP**</span><span class="sxs-lookup"><span data-stu-id="7a5fb-179">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="7a5fb-180">83</span><span class="sxs-lookup"><span data-stu-id="7a5fb-180">83</span></span>

<span data-ttu-id="7a5fb-181">Impossibile rilasciare il lease DHCP.</span><span class="sxs-lookup"><span data-stu-id="7a5fb-181">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="7a5fb-182">**IP non abilitato sulla scheda**</span><span class="sxs-lookup"><span data-stu-id="7a5fb-182">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="7a5fb-183">84</span><span class="sxs-lookup"><span data-stu-id="7a5fb-183">84</span></span>

<span data-ttu-id="7a5fb-184">IP non abilitato sulla scheda.</span><span class="sxs-lookup"><span data-stu-id="7a5fb-184">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="7a5fb-185">**IPX non abilitato sull'adapter**</span><span class="sxs-lookup"><span data-stu-id="7a5fb-185">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="7a5fb-186">85</span><span class="sxs-lookup"><span data-stu-id="7a5fb-186">85</span></span>

<span data-ttu-id="7a5fb-187">IPX non abilitato sulla scheda.</span><span class="sxs-lookup"><span data-stu-id="7a5fb-187">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="7a5fb-188">**Errore limite numero frame/rete**</span><span class="sxs-lookup"><span data-stu-id="7a5fb-188">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="7a5fb-189">86</span><span class="sxs-lookup"><span data-stu-id="7a5fb-189">86</span></span>

<span data-ttu-id="7a5fb-190">Errore dei limiti del numero di rete o del frame.</span><span class="sxs-lookup"><span data-stu-id="7a5fb-190">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="7a5fb-191">**Tipo di frame non valido**</span><span class="sxs-lookup"><span data-stu-id="7a5fb-191">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="7a5fb-192">87</span><span class="sxs-lookup"><span data-stu-id="7a5fb-192">87</span></span>

<span data-ttu-id="7a5fb-193">Tipo di frame non valido.</span><span class="sxs-lookup"><span data-stu-id="7a5fb-193">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="7a5fb-194">**Numero di rete non valido**</span><span class="sxs-lookup"><span data-stu-id="7a5fb-194">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="7a5fb-195">88</span><span class="sxs-lookup"><span data-stu-id="7a5fb-195">88</span></span>

<span data-ttu-id="7a5fb-196">Numero di rete non valido.</span><span class="sxs-lookup"><span data-stu-id="7a5fb-196">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="7a5fb-197">**Numero di rete duplicato**</span><span class="sxs-lookup"><span data-stu-id="7a5fb-197">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="7a5fb-198">89</span><span class="sxs-lookup"><span data-stu-id="7a5fb-198">89</span></span>

<span data-ttu-id="7a5fb-199">Numero di rete duplicato.</span><span class="sxs-lookup"><span data-stu-id="7a5fb-199">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="7a5fb-200">**Parametro fuori limite**</span><span class="sxs-lookup"><span data-stu-id="7a5fb-200">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="7a5fb-201">90</span><span class="sxs-lookup"><span data-stu-id="7a5fb-201">90</span></span>

<span data-ttu-id="7a5fb-202">Parametro fuori limite.</span><span class="sxs-lookup"><span data-stu-id="7a5fb-202">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="7a5fb-203">**Accesso negato**</span><span class="sxs-lookup"><span data-stu-id="7a5fb-203">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="7a5fb-204">91</span><span class="sxs-lookup"><span data-stu-id="7a5fb-204">91</span></span>

<span data-ttu-id="7a5fb-205">Accesso negato.</span><span class="sxs-lookup"><span data-stu-id="7a5fb-205">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="7a5fb-206">**Memoria insufficiente**</span><span class="sxs-lookup"><span data-stu-id="7a5fb-206">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="7a5fb-207">92</span><span class="sxs-lookup"><span data-stu-id="7a5fb-207">92</span></span>

<span data-ttu-id="7a5fb-208">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="7a5fb-208">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="7a5fb-209">**Esiste già**</span><span class="sxs-lookup"><span data-stu-id="7a5fb-209">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="7a5fb-210">93</span><span class="sxs-lookup"><span data-stu-id="7a5fb-210">93</span></span>

<span data-ttu-id="7a5fb-211">Esiste già.</span><span class="sxs-lookup"><span data-stu-id="7a5fb-211">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="7a5fb-212">**Percorso, file o oggetto non trovato**</span><span class="sxs-lookup"><span data-stu-id="7a5fb-212">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="7a5fb-213">94</span><span class="sxs-lookup"><span data-stu-id="7a5fb-213">94</span></span>

<span data-ttu-id="7a5fb-214">Il percorso, il file o l'oggetto non è stato trovato.</span><span class="sxs-lookup"><span data-stu-id="7a5fb-214">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="7a5fb-215">**Non è possibile inviare una notifica al servizio**</span><span class="sxs-lookup"><span data-stu-id="7a5fb-215">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="7a5fb-216">95</span><span class="sxs-lookup"><span data-stu-id="7a5fb-216">95</span></span>

<span data-ttu-id="7a5fb-217">Impossibile notificare il servizio.</span><span class="sxs-lookup"><span data-stu-id="7a5fb-217">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="7a5fb-218">**Non è possibile inviare una notifica al servizio DNS**</span><span class="sxs-lookup"><span data-stu-id="7a5fb-218">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="7a5fb-219">96</span><span class="sxs-lookup"><span data-stu-id="7a5fb-219">96</span></span>

<span data-ttu-id="7a5fb-220">Impossibile inviare una notifica al servizio DNS.</span><span class="sxs-lookup"><span data-stu-id="7a5fb-220">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="7a5fb-221">**Interfaccia non configurabile**</span><span class="sxs-lookup"><span data-stu-id="7a5fb-221">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="7a5fb-222">97</span><span class="sxs-lookup"><span data-stu-id="7a5fb-222">97</span></span>

<span data-ttu-id="7a5fb-223">Interfaccia non configurabile.</span><span class="sxs-lookup"><span data-stu-id="7a5fb-223">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="7a5fb-224">**Non tutti i lease DHCP possono essere rilasciati/rinnovati**</span><span class="sxs-lookup"><span data-stu-id="7a5fb-224">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="7a5fb-225">98</span><span class="sxs-lookup"><span data-stu-id="7a5fb-225">98</span></span>

<span data-ttu-id="7a5fb-226">Non tutti i lease DHCP possono essere rilasciati o rinnovati.</span><span class="sxs-lookup"><span data-stu-id="7a5fb-226">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="7a5fb-227">**DHCP non abilitato sull'adapter**</span><span class="sxs-lookup"><span data-stu-id="7a5fb-227">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="7a5fb-228">100</span><span class="sxs-lookup"><span data-stu-id="7a5fb-228">100</span></span>

<span data-ttu-id="7a5fb-229">DHCP non abilitato sulla scheda.</span><span class="sxs-lookup"><span data-stu-id="7a5fb-229">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="7a5fb-230">**Altri**</span><span class="sxs-lookup"><span data-stu-id="7a5fb-230">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="7a5fb-231">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="7a5fb-231">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7a5fb-232">Commenti</span><span class="sxs-lookup"><span data-stu-id="7a5fb-232">Remarks</span></span>

<span data-ttu-id="7a5fb-233">La durata (TTL) specifica il numero di router che possono essere passati da un pacchetto IP per raggiungere la destinazione prima di essere eliminati.</span><span class="sxs-lookup"><span data-stu-id="7a5fb-233">The TTL specifies the number of routers an IP packet may pass through to reach its destination before being discarded.</span></span> <span data-ttu-id="7a5fb-234">Ogni router decrementa di uno il numero di TTL di un pacchetto e rimuove i pacchetti con un valore TTL pari a 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="7a5fb-234">Each router decrements the TTL count of a packet by one and discards the packets with a TTL of 0 (zero).</span></span>

## <a name="examples"></a><span data-ttu-id="7a5fb-235">Esempio</span><span class="sxs-lookup"><span data-stu-id="7a5fb-235">Examples</span></span>

<span data-ttu-id="7a5fb-236">L'esempio di [modifica della durata (TTL) predefinita per tutte le schede di rete](https://Gallery.TechNet.Microsoft.Com/scriptcenter/3a228fb8-5517-4e23-800e-2a15f427d05d) VBScript USA **SetDefaultTTL** per impostare il valore predefinito di durata (TTL) nell'intestazione dei pacchetti IP in uscita su 64</span><span class="sxs-lookup"><span data-stu-id="7a5fb-236">The [Modify the Default Time-to-Live for All Network Adapters](https://Gallery.TechNet.Microsoft.Com/scriptcenter/3a228fb8-5517-4e23-800e-2a15f427d05d) VBScript sample uses **SetDefaultTTL** to set the default time-to-live value in the header of outgoing IP packets to 64</span></span>

## <a name="requirements"></a><span data-ttu-id="7a5fb-237">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7a5fb-237">Requirements</span></span>



| <span data-ttu-id="7a5fb-238">Requisito</span><span class="sxs-lookup"><span data-stu-id="7a5fb-238">Requirement</span></span> | <span data-ttu-id="7a5fb-239">Valore</span><span class="sxs-lookup"><span data-stu-id="7a5fb-239">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7a5fb-240">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7a5fb-240">Minimum supported client</span></span><br/> | <span data-ttu-id="7a5fb-241">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7a5fb-241">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7a5fb-242">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7a5fb-242">Minimum supported server</span></span><br/> | <span data-ttu-id="7a5fb-243">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7a5fb-243">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7a5fb-244">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="7a5fb-244">Namespace</span></span><br/>                | <span data-ttu-id="7a5fb-245">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="7a5fb-245">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="7a5fb-246">MOF</span><span class="sxs-lookup"><span data-stu-id="7a5fb-246">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7a5fb-247"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7a5fb-247"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="7a5fb-248">DLL</span><span class="sxs-lookup"><span data-stu-id="7a5fb-248">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7a5fb-249"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7a5fb-249"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7a5fb-250">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7a5fb-250">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a5fb-251">Classi hardware del sistema del computer</span><span class="sxs-lookup"><span data-stu-id="7a5fb-251">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="7a5fb-252">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="7a5fb-252">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="7a5fb-253">Attività WMI: rete</span><span class="sxs-lookup"><span data-stu-id="7a5fb-253">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="7a5fb-254">Attività WMI: account e domini</span><span class="sxs-lookup"><span data-stu-id="7a5fb-254">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="7a5fb-255">Supporto di IPv6 e IPv4 in WMI</span><span class="sxs-lookup"><span data-stu-id="7a5fb-255">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

