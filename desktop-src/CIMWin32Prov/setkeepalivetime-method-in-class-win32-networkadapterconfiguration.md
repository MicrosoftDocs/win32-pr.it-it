---
description: Il metodo statico della classe WMI SetKeepAliveTime viene usato per impostare la frequenza con cui TCP tenta di verificare che una connessione inattiva sia ancora disponibile inviando un pacchetto keep-alive.
ms.assetid: 8640b109-928b-46fc-8dce-9ee5dcbd94e3
ms.tgt_platform: multiple
title: Metodo SetKeepAliveTime della classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetKeepAliveTime
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1dc2674f3c09626749b4c7ac6151349401670e27
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304960"
---
# <a name="setkeepalivetime-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="3aada-103">Metodo SetKeepAliveTime della \_ classe NetworkAdapterConfiguration Win32</span><span class="sxs-lookup"><span data-stu-id="3aada-103">SetKeepAliveTime method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="3aada-104">Il metodo statico della [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetKeepAliveTime** viene usato per impostare la frequenza con cui TCP tenta di verificare che una connessione inattiva sia ancora disponibile inviando un pacchetto keep-alive.</span><span class="sxs-lookup"><span data-stu-id="3aada-104">The **SetKeepAliveTime** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to set how often TCP attempts to verify that an idle connection is still available by sending a Keep Alive packet.</span></span>

<span data-ttu-id="3aada-105">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="3aada-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="3aada-106">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="3aada-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="3aada-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3aada-107">Syntax</span></span>


```mof
uint32 SetKeepAliveTime(
  [in] uint32 KeepAliveTime
);
```



## <a name="parameters"></a><span data-ttu-id="3aada-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="3aada-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3aada-109">*KeepAliveTime* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3aada-109">*KeepAliveTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3aada-110">Intervallo, in millisecondi, di attesa TCP per verificare che sia ancora disponibile una connessione inattiva.</span><span class="sxs-lookup"><span data-stu-id="3aada-110">Interval, in milliseconds, the TCP waits to check that an idle connection is still available.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3aada-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3aada-111">Return value</span></span>

<span data-ttu-id="3aada-112">Restituisce un valore pari a 0 (zero) per un completamento corretto quando non è richiesto il riavvio, 1 (uno) per un completamento corretto quando è necessario un riavvio e un numero diverso se si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="3aada-112">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="3aada-113">Per ulteriori informazioni sui codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="3aada-113">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="3aada-114">Per i valori **HRESULT** generali, vedere [codici di errore di sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="3aada-114">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="3aada-115">**Operazione completata, non è necessario riavviare il computer**</span><span class="sxs-lookup"><span data-stu-id="3aada-115">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="3aada-116">0</span><span class="sxs-lookup"><span data-stu-id="3aada-116">0</span></span>

<span data-ttu-id="3aada-117">Operazione completata, non è necessario riavviare il computer.</span><span class="sxs-lookup"><span data-stu-id="3aada-117">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="3aada-118">**Operazione completata, riavvio richiesto**</span><span class="sxs-lookup"><span data-stu-id="3aada-118">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="3aada-119">1</span><span class="sxs-lookup"><span data-stu-id="3aada-119">1</span></span>

<span data-ttu-id="3aada-120">Operazione completata, è necessario riavviare il computer.</span><span class="sxs-lookup"><span data-stu-id="3aada-120">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="3aada-121">**Metodo non supportato in questa piattaforma**</span><span class="sxs-lookup"><span data-stu-id="3aada-121">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="3aada-122">64</span><span class="sxs-lookup"><span data-stu-id="3aada-122">64</span></span>

<span data-ttu-id="3aada-123">Metodo non supportato in questa piattaforma.</span><span class="sxs-lookup"><span data-stu-id="3aada-123">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="3aada-124">**Errore sconosciuto**</span><span class="sxs-lookup"><span data-stu-id="3aada-124">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="3aada-125">65</span><span class="sxs-lookup"><span data-stu-id="3aada-125">65</span></span>

<span data-ttu-id="3aada-126">Errore sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="3aada-126">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="3aada-127">**subnet mask non valido**</span><span class="sxs-lookup"><span data-stu-id="3aada-127">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="3aada-128">66</span><span class="sxs-lookup"><span data-stu-id="3aada-128">66</span></span>

<span data-ttu-id="3aada-129">Subnet mask non valido.</span><span class="sxs-lookup"><span data-stu-id="3aada-129">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="3aada-130">**Si è verificato un errore durante l'elaborazione di un'istanza restituita**</span><span class="sxs-lookup"><span data-stu-id="3aada-130">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="3aada-131">67</span><span class="sxs-lookup"><span data-stu-id="3aada-131">67</span></span>

<span data-ttu-id="3aada-132">Si è verificato un errore durante l'elaborazione di un'istanza di restituita.</span><span class="sxs-lookup"><span data-stu-id="3aada-132">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="3aada-133">**Parametro di input non valido**</span><span class="sxs-lookup"><span data-stu-id="3aada-133">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="3aada-134">68</span><span class="sxs-lookup"><span data-stu-id="3aada-134">68</span></span>

<span data-ttu-id="3aada-135">Parametro di input non valido.</span><span class="sxs-lookup"><span data-stu-id="3aada-135">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="3aada-136">**Sono stati specificati più di 5 gateway**</span><span class="sxs-lookup"><span data-stu-id="3aada-136">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="3aada-137">69</span><span class="sxs-lookup"><span data-stu-id="3aada-137">69</span></span>

<span data-ttu-id="3aada-138">Sono stati specificati più di cinque gateway.</span><span class="sxs-lookup"><span data-stu-id="3aada-138">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="3aada-139">**Indirizzo IP non valido**</span><span class="sxs-lookup"><span data-stu-id="3aada-139">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="3aada-140">70</span><span class="sxs-lookup"><span data-stu-id="3aada-140">70</span></span>

<span data-ttu-id="3aada-141">Indirizzo IP non valido.</span><span class="sxs-lookup"><span data-stu-id="3aada-141">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="3aada-142">**Indirizzo IP gateway non valido**</span><span class="sxs-lookup"><span data-stu-id="3aada-142">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="3aada-143">71</span><span class="sxs-lookup"><span data-stu-id="3aada-143">71</span></span>

<span data-ttu-id="3aada-144">Indirizzo IP del gateway non valido.</span><span class="sxs-lookup"><span data-stu-id="3aada-144">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="3aada-145">**Si è verificato un errore durante l'accesso al registro di sistema per le informazioni richieste**</span><span class="sxs-lookup"><span data-stu-id="3aada-145">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="3aada-146">72</span><span class="sxs-lookup"><span data-stu-id="3aada-146">72</span></span>

<span data-ttu-id="3aada-147">Si è verificato un errore durante l'accesso al registro di sistema per le informazioni richieste.</span><span class="sxs-lookup"><span data-stu-id="3aada-147">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="3aada-148">**Nome di dominio non valido**</span><span class="sxs-lookup"><span data-stu-id="3aada-148">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="3aada-149">73</span><span class="sxs-lookup"><span data-stu-id="3aada-149">73</span></span>

<span data-ttu-id="3aada-150">Nome di dominio non valido.</span><span class="sxs-lookup"><span data-stu-id="3aada-150">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="3aada-151">**Nome host non valido**</span><span class="sxs-lookup"><span data-stu-id="3aada-151">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="3aada-152">74</span><span class="sxs-lookup"><span data-stu-id="3aada-152">74</span></span>

<span data-ttu-id="3aada-153">Nome host non valido.</span><span class="sxs-lookup"><span data-stu-id="3aada-153">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="3aada-154">**Nessun server WINS primario/secondario definito**</span><span class="sxs-lookup"><span data-stu-id="3aada-154">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="3aada-155">75</span><span class="sxs-lookup"><span data-stu-id="3aada-155">75</span></span>

<span data-ttu-id="3aada-156">Nessun server WINS primario o secondario definito.</span><span class="sxs-lookup"><span data-stu-id="3aada-156">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="3aada-157">**File non valido**</span><span class="sxs-lookup"><span data-stu-id="3aada-157">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="3aada-158">76</span><span class="sxs-lookup"><span data-stu-id="3aada-158">76</span></span>

<span data-ttu-id="3aada-159">File non valido.</span><span class="sxs-lookup"><span data-stu-id="3aada-159">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="3aada-160">**Percorso di sistema non valido**</span><span class="sxs-lookup"><span data-stu-id="3aada-160">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="3aada-161">77</span><span class="sxs-lookup"><span data-stu-id="3aada-161">77</span></span>

<span data-ttu-id="3aada-162">Percorso di sistema non valido.</span><span class="sxs-lookup"><span data-stu-id="3aada-162">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="3aada-163">**Copia del file non riuscita**</span><span class="sxs-lookup"><span data-stu-id="3aada-163">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="3aada-164">78</span><span class="sxs-lookup"><span data-stu-id="3aada-164">78</span></span>

<span data-ttu-id="3aada-165">Copia del file non riuscita.</span><span class="sxs-lookup"><span data-stu-id="3aada-165">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="3aada-166">**Parametro di sicurezza non valido**</span><span class="sxs-lookup"><span data-stu-id="3aada-166">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="3aada-167">79</span><span class="sxs-lookup"><span data-stu-id="3aada-167">79</span></span>

<span data-ttu-id="3aada-168">Parametro di sicurezza non valido.</span><span class="sxs-lookup"><span data-stu-id="3aada-168">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="3aada-169">**Impossibile configurare il servizio TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="3aada-169">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="3aada-170">80</span><span class="sxs-lookup"><span data-stu-id="3aada-170">80</span></span>

<span data-ttu-id="3aada-171">Impossibile configurare il servizio TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="3aada-171">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="3aada-172">**Non è possibile configurare il servizio DHCP**</span><span class="sxs-lookup"><span data-stu-id="3aada-172">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="3aada-173">81</span><span class="sxs-lookup"><span data-stu-id="3aada-173">81</span></span>

<span data-ttu-id="3aada-174">Impossibile configurare il servizio DHCP.</span><span class="sxs-lookup"><span data-stu-id="3aada-174">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="3aada-175">**Non è possibile rinnovare il lease DHCP**</span><span class="sxs-lookup"><span data-stu-id="3aada-175">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="3aada-176">82</span><span class="sxs-lookup"><span data-stu-id="3aada-176">82</span></span>

<span data-ttu-id="3aada-177">Non è possibile rinnovare il lease DHCP.</span><span class="sxs-lookup"><span data-stu-id="3aada-177">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="3aada-178">**Non è possibile rilasciare il lease DHCP**</span><span class="sxs-lookup"><span data-stu-id="3aada-178">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="3aada-179">83</span><span class="sxs-lookup"><span data-stu-id="3aada-179">83</span></span>

<span data-ttu-id="3aada-180">Impossibile rilasciare il lease DHCP.</span><span class="sxs-lookup"><span data-stu-id="3aada-180">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="3aada-181">**IP non abilitato sulla scheda**</span><span class="sxs-lookup"><span data-stu-id="3aada-181">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="3aada-182">84</span><span class="sxs-lookup"><span data-stu-id="3aada-182">84</span></span>

<span data-ttu-id="3aada-183">IP non abilitato sulla scheda.</span><span class="sxs-lookup"><span data-stu-id="3aada-183">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="3aada-184">**IPX non abilitato sull'adapter**</span><span class="sxs-lookup"><span data-stu-id="3aada-184">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="3aada-185">85</span><span class="sxs-lookup"><span data-stu-id="3aada-185">85</span></span>

<span data-ttu-id="3aada-186">IPX non abilitato sulla scheda.</span><span class="sxs-lookup"><span data-stu-id="3aada-186">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="3aada-187">**Errore limite numero frame/rete**</span><span class="sxs-lookup"><span data-stu-id="3aada-187">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="3aada-188">86</span><span class="sxs-lookup"><span data-stu-id="3aada-188">86</span></span>

<span data-ttu-id="3aada-189">Errore dei limiti del numero di rete o del frame.</span><span class="sxs-lookup"><span data-stu-id="3aada-189">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="3aada-190">**Tipo di frame non valido**</span><span class="sxs-lookup"><span data-stu-id="3aada-190">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="3aada-191">87</span><span class="sxs-lookup"><span data-stu-id="3aada-191">87</span></span>

<span data-ttu-id="3aada-192">Tipo di frame non valido.</span><span class="sxs-lookup"><span data-stu-id="3aada-192">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="3aada-193">**Numero di rete non valido**</span><span class="sxs-lookup"><span data-stu-id="3aada-193">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="3aada-194">88</span><span class="sxs-lookup"><span data-stu-id="3aada-194">88</span></span>

<span data-ttu-id="3aada-195">Numero di rete non valido.</span><span class="sxs-lookup"><span data-stu-id="3aada-195">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="3aada-196">**Numero di rete duplicato**</span><span class="sxs-lookup"><span data-stu-id="3aada-196">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="3aada-197">89</span><span class="sxs-lookup"><span data-stu-id="3aada-197">89</span></span>

<span data-ttu-id="3aada-198">Numero di rete duplicato.</span><span class="sxs-lookup"><span data-stu-id="3aada-198">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="3aada-199">**Parametro fuori limite**</span><span class="sxs-lookup"><span data-stu-id="3aada-199">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="3aada-200">90</span><span class="sxs-lookup"><span data-stu-id="3aada-200">90</span></span>

<span data-ttu-id="3aada-201">Parametro fuori limite.</span><span class="sxs-lookup"><span data-stu-id="3aada-201">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="3aada-202">**Accesso negato**</span><span class="sxs-lookup"><span data-stu-id="3aada-202">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="3aada-203">91</span><span class="sxs-lookup"><span data-stu-id="3aada-203">91</span></span>

<span data-ttu-id="3aada-204">Accesso negato.</span><span class="sxs-lookup"><span data-stu-id="3aada-204">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="3aada-205">**Memoria insufficiente**</span><span class="sxs-lookup"><span data-stu-id="3aada-205">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="3aada-206">92</span><span class="sxs-lookup"><span data-stu-id="3aada-206">92</span></span>

<span data-ttu-id="3aada-207">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="3aada-207">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="3aada-208">**Esiste già**</span><span class="sxs-lookup"><span data-stu-id="3aada-208">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="3aada-209">93</span><span class="sxs-lookup"><span data-stu-id="3aada-209">93</span></span>

<span data-ttu-id="3aada-210">Esiste già.</span><span class="sxs-lookup"><span data-stu-id="3aada-210">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="3aada-211">**Percorso, file o oggetto non trovato**</span><span class="sxs-lookup"><span data-stu-id="3aada-211">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="3aada-212">94</span><span class="sxs-lookup"><span data-stu-id="3aada-212">94</span></span>

<span data-ttu-id="3aada-213">Il percorso, il file o l'oggetto non è stato trovato.</span><span class="sxs-lookup"><span data-stu-id="3aada-213">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="3aada-214">**Non è possibile inviare una notifica al servizio**</span><span class="sxs-lookup"><span data-stu-id="3aada-214">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="3aada-215">95</span><span class="sxs-lookup"><span data-stu-id="3aada-215">95</span></span>

<span data-ttu-id="3aada-216">Impossibile notificare il servizio.</span><span class="sxs-lookup"><span data-stu-id="3aada-216">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="3aada-217">**Non è possibile inviare una notifica al servizio DNS**</span><span class="sxs-lookup"><span data-stu-id="3aada-217">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="3aada-218">96</span><span class="sxs-lookup"><span data-stu-id="3aada-218">96</span></span>

<span data-ttu-id="3aada-219">Impossibile inviare una notifica al servizio DNS.</span><span class="sxs-lookup"><span data-stu-id="3aada-219">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="3aada-220">**Interfaccia non configurabile**</span><span class="sxs-lookup"><span data-stu-id="3aada-220">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="3aada-221">97</span><span class="sxs-lookup"><span data-stu-id="3aada-221">97</span></span>

<span data-ttu-id="3aada-222">Interfaccia non configurabile.</span><span class="sxs-lookup"><span data-stu-id="3aada-222">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="3aada-223">**Non tutti i lease DHCP possono essere rilasciati/rinnovati**</span><span class="sxs-lookup"><span data-stu-id="3aada-223">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="3aada-224">98</span><span class="sxs-lookup"><span data-stu-id="3aada-224">98</span></span>

<span data-ttu-id="3aada-225">Non tutti i lease DHCP possono essere rilasciati o rinnovati.</span><span class="sxs-lookup"><span data-stu-id="3aada-225">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="3aada-226">**DHCP non abilitato sull'adapter**</span><span class="sxs-lookup"><span data-stu-id="3aada-226">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="3aada-227">100</span><span class="sxs-lookup"><span data-stu-id="3aada-227">100</span></span>

<span data-ttu-id="3aada-228">DHCP non abilitato sulla scheda.</span><span class="sxs-lookup"><span data-stu-id="3aada-228">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="3aada-229">**Altri**</span><span class="sxs-lookup"><span data-stu-id="3aada-229">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="3aada-230">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="3aada-230">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3aada-231">Commenti</span><span class="sxs-lookup"><span data-stu-id="3aada-231">Remarks</span></span>

<span data-ttu-id="3aada-232">Se il sistema remoto è ancora raggiungibile e funzionante, verrà riconosciuta la trasmissione keep-alive.</span><span class="sxs-lookup"><span data-stu-id="3aada-232">If the remote system is still reachable and functioning, it will acknowledge the Keep Alive transmission.</span></span> <span data-ttu-id="3aada-233">I pacchetti Keep-Alive non vengono inviati per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="3aada-233">Keep Alive packets are not sent by default.</span></span> <span data-ttu-id="3aada-234">Questa funzionalità può essere abilitata in una connessione da un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="3aada-234">This feature may be enabled in a connection by an application.</span></span>

## <a name="examples"></a><span data-ttu-id="3aada-235">Esempio</span><span class="sxs-lookup"><span data-stu-id="3aada-235">Examples</span></span>

<span data-ttu-id="3aada-236">L'esempio di [modifica del tempo di conservazione per tutte le schede di rete](https://Gallery.TechNet.Microsoft.Com/35c1b0ac-285d-4baa-be6e-d3fb0b461676) VBScript configura il tempo Keep-Alive per tutte le schede di rete in un computer a 300.000 millisecondi (5 minuti).</span><span class="sxs-lookup"><span data-stu-id="3aada-236">The [Modify Keep Alive Time for All Network Adapters](https://Gallery.TechNet.Microsoft.Com/35c1b0ac-285d-4baa-be6e-d3fb0b461676) VBScript sample configures the keep alive time for all network adapters on a computer to 300,000 milliseconds (5 minutes).</span></span>

## <a name="requirements"></a><span data-ttu-id="3aada-237">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3aada-237">Requirements</span></span>



| <span data-ttu-id="3aada-238">Requisito</span><span class="sxs-lookup"><span data-stu-id="3aada-238">Requirement</span></span> | <span data-ttu-id="3aada-239">Valore</span><span class="sxs-lookup"><span data-stu-id="3aada-239">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3aada-240">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3aada-240">Minimum supported client</span></span><br/> | <span data-ttu-id="3aada-241">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3aada-241">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3aada-242">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3aada-242">Minimum supported server</span></span><br/> | <span data-ttu-id="3aada-243">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3aada-243">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3aada-244">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="3aada-244">Namespace</span></span><br/>                | <span data-ttu-id="3aada-245">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="3aada-245">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3aada-246">MOF</span><span class="sxs-lookup"><span data-stu-id="3aada-246">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3aada-247"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3aada-247"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3aada-248">DLL</span><span class="sxs-lookup"><span data-stu-id="3aada-248">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3aada-249"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3aada-249"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3aada-250">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3aada-250">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3aada-251">Classi hardware del sistema del computer</span><span class="sxs-lookup"><span data-stu-id="3aada-251">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="3aada-252">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="3aada-252">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="3aada-253">Attività WMI: rete</span><span class="sxs-lookup"><span data-stu-id="3aada-253">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="3aada-254">Attività WMI: account e domini</span><span class="sxs-lookup"><span data-stu-id="3aada-254">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="3aada-255">Supporto di IPv6 e IPv4 in WMI</span><span class="sxs-lookup"><span data-stu-id="3aada-255">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

