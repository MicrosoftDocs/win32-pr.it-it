---
description: Il metodo statico della classe WMI SetTcpWindowSize viene utilizzato per impostare le dimensioni massime della finestra di ricezione TCP offerte dal sistema.
ms.assetid: c108fd9c-6de4-4f3e-9691-b0b5c1a3dc5f
ms.tgt_platform: multiple
title: Metodo SetTcpWindowSize della classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetTcpWindowSize
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: d4a77acdc81c06d1f78da8bbc0160bd0d21bcfd8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126854"
---
# <a name="settcpwindowsize-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="562d2-103">Metodo SetTcpWindowSize della \_ classe NetworkAdapterConfiguration Win32</span><span class="sxs-lookup"><span data-stu-id="562d2-103">SetTcpWindowSize method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="562d2-104">Il metodo statico della [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetTcpWindowSize** viene utilizzato per impostare le dimensioni massime della finestra di ricezione TCP offerte dal sistema.</span><span class="sxs-lookup"><span data-stu-id="562d2-104">The **SetTcpWindowSize** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to set the maximum TCP Receive Window size offered by the system.</span></span>

<span data-ttu-id="562d2-105">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="562d2-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="562d2-106">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="562d2-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="562d2-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="562d2-107">Syntax</span></span>


```mof
uint32 SetTcpWindowSize(
  [in] uint16 TcpWindowSize
);
```



## <a name="parameters"></a><span data-ttu-id="562d2-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="562d2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="562d2-109">*TcpWindowSize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="562d2-109">*TcpWindowSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="562d2-110">Dimensioni massime della finestra di ricezione TCP offerte dal sistema.</span><span class="sxs-lookup"><span data-stu-id="562d2-110">Maximum TCP receive window size offered by the system.</span></span> <span data-ttu-id="562d2-111">L'intervallo valido di valori in byte è 0-65535.</span><span class="sxs-lookup"><span data-stu-id="562d2-111">The valid range of values in bytes is 0 - 65535.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="562d2-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="562d2-112">Return value</span></span>

<span data-ttu-id="562d2-113">Restituisce un valore pari a 0 (zero) per un completamento corretto quando non è richiesto il riavvio, 1 (uno) per un completamento corretto quando è necessario un riavvio e un numero diverso se si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="562d2-113">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="562d2-114">Per ulteriori informazioni sui codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="562d2-114">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="562d2-115">Per i valori **HRESULT** generali, vedere [codici di errore di sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="562d2-115">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="562d2-116">**Operazione completata, non è necessario riavviare il computer**</span><span class="sxs-lookup"><span data-stu-id="562d2-116">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="562d2-117">0</span><span class="sxs-lookup"><span data-stu-id="562d2-117">0</span></span>

<span data-ttu-id="562d2-118">Operazione completata, non è necessario riavviare il computer.</span><span class="sxs-lookup"><span data-stu-id="562d2-118">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="562d2-119">**Operazione completata, riavvio richiesto**</span><span class="sxs-lookup"><span data-stu-id="562d2-119">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="562d2-120">1</span><span class="sxs-lookup"><span data-stu-id="562d2-120">1</span></span>

<span data-ttu-id="562d2-121">Operazione completata, è necessario riavviare il computer.</span><span class="sxs-lookup"><span data-stu-id="562d2-121">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="562d2-122">**Metodo non supportato in questa piattaforma**</span><span class="sxs-lookup"><span data-stu-id="562d2-122">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="562d2-123">64</span><span class="sxs-lookup"><span data-stu-id="562d2-123">64</span></span>

<span data-ttu-id="562d2-124">Metodo non supportato in questa piattaforma.</span><span class="sxs-lookup"><span data-stu-id="562d2-124">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="562d2-125">**Errore sconosciuto**</span><span class="sxs-lookup"><span data-stu-id="562d2-125">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="562d2-126">65</span><span class="sxs-lookup"><span data-stu-id="562d2-126">65</span></span>

<span data-ttu-id="562d2-127">Errore sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="562d2-127">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="562d2-128">**subnet mask non valido**</span><span class="sxs-lookup"><span data-stu-id="562d2-128">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="562d2-129">66</span><span class="sxs-lookup"><span data-stu-id="562d2-129">66</span></span>

<span data-ttu-id="562d2-130">Subnet mask non valido.</span><span class="sxs-lookup"><span data-stu-id="562d2-130">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="562d2-131">**Si è verificato un errore durante l'elaborazione di un'istanza restituita**</span><span class="sxs-lookup"><span data-stu-id="562d2-131">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="562d2-132">67</span><span class="sxs-lookup"><span data-stu-id="562d2-132">67</span></span>

<span data-ttu-id="562d2-133">Si è verificato un errore durante l'elaborazione di un'istanza di restituita.</span><span class="sxs-lookup"><span data-stu-id="562d2-133">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="562d2-134">**Parametro di input non valido**</span><span class="sxs-lookup"><span data-stu-id="562d2-134">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="562d2-135">68</span><span class="sxs-lookup"><span data-stu-id="562d2-135">68</span></span>

<span data-ttu-id="562d2-136">Parametro di input non valido.</span><span class="sxs-lookup"><span data-stu-id="562d2-136">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="562d2-137">**Sono stati specificati più di 5 gateway**</span><span class="sxs-lookup"><span data-stu-id="562d2-137">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="562d2-138">69</span><span class="sxs-lookup"><span data-stu-id="562d2-138">69</span></span>

<span data-ttu-id="562d2-139">Sono stati specificati più di cinque gateway.</span><span class="sxs-lookup"><span data-stu-id="562d2-139">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="562d2-140">**Indirizzo IP non valido**</span><span class="sxs-lookup"><span data-stu-id="562d2-140">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="562d2-141">70</span><span class="sxs-lookup"><span data-stu-id="562d2-141">70</span></span>

<span data-ttu-id="562d2-142">Indirizzo IP non valido.</span><span class="sxs-lookup"><span data-stu-id="562d2-142">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="562d2-143">**Indirizzo IP gateway non valido**</span><span class="sxs-lookup"><span data-stu-id="562d2-143">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="562d2-144">71</span><span class="sxs-lookup"><span data-stu-id="562d2-144">71</span></span>

<span data-ttu-id="562d2-145">Indirizzo IP del gateway non valido.</span><span class="sxs-lookup"><span data-stu-id="562d2-145">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="562d2-146">**Si è verificato un errore durante l'accesso al registro di sistema per le informazioni richieste**</span><span class="sxs-lookup"><span data-stu-id="562d2-146">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="562d2-147">72</span><span class="sxs-lookup"><span data-stu-id="562d2-147">72</span></span>

<span data-ttu-id="562d2-148">Si è verificato un errore durante l'accesso al registro di sistema per le informazioni richieste.</span><span class="sxs-lookup"><span data-stu-id="562d2-148">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="562d2-149">**Nome di dominio non valido**</span><span class="sxs-lookup"><span data-stu-id="562d2-149">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="562d2-150">73</span><span class="sxs-lookup"><span data-stu-id="562d2-150">73</span></span>

<span data-ttu-id="562d2-151">Nome di dominio non valido.</span><span class="sxs-lookup"><span data-stu-id="562d2-151">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="562d2-152">**Nome host non valido**</span><span class="sxs-lookup"><span data-stu-id="562d2-152">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="562d2-153">74</span><span class="sxs-lookup"><span data-stu-id="562d2-153">74</span></span>

<span data-ttu-id="562d2-154">Nome host non valido.</span><span class="sxs-lookup"><span data-stu-id="562d2-154">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="562d2-155">**Nessun server WINS primario/secondario definito**</span><span class="sxs-lookup"><span data-stu-id="562d2-155">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="562d2-156">75</span><span class="sxs-lookup"><span data-stu-id="562d2-156">75</span></span>

<span data-ttu-id="562d2-157">Nessun server WINS primario o secondario definito.</span><span class="sxs-lookup"><span data-stu-id="562d2-157">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="562d2-158">**File non valido**</span><span class="sxs-lookup"><span data-stu-id="562d2-158">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="562d2-159">76</span><span class="sxs-lookup"><span data-stu-id="562d2-159">76</span></span>

<span data-ttu-id="562d2-160">File non valido.</span><span class="sxs-lookup"><span data-stu-id="562d2-160">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="562d2-161">**Percorso di sistema non valido**</span><span class="sxs-lookup"><span data-stu-id="562d2-161">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="562d2-162">77</span><span class="sxs-lookup"><span data-stu-id="562d2-162">77</span></span>

<span data-ttu-id="562d2-163">Percorso di sistema non valido.</span><span class="sxs-lookup"><span data-stu-id="562d2-163">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="562d2-164">**Copia del file non riuscita**</span><span class="sxs-lookup"><span data-stu-id="562d2-164">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="562d2-165">78</span><span class="sxs-lookup"><span data-stu-id="562d2-165">78</span></span>

<span data-ttu-id="562d2-166">Copia del file non riuscita.</span><span class="sxs-lookup"><span data-stu-id="562d2-166">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="562d2-167">**Parametro di sicurezza non valido**</span><span class="sxs-lookup"><span data-stu-id="562d2-167">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="562d2-168">79</span><span class="sxs-lookup"><span data-stu-id="562d2-168">79</span></span>

<span data-ttu-id="562d2-169">Parametro di sicurezza non valido.</span><span class="sxs-lookup"><span data-stu-id="562d2-169">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="562d2-170">**Impossibile configurare il servizio TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="562d2-170">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="562d2-171">80</span><span class="sxs-lookup"><span data-stu-id="562d2-171">80</span></span>

<span data-ttu-id="562d2-172">Impossibile configurare il servizio TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="562d2-172">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="562d2-173">**Non è possibile configurare il servizio DHCP**</span><span class="sxs-lookup"><span data-stu-id="562d2-173">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="562d2-174">81</span><span class="sxs-lookup"><span data-stu-id="562d2-174">81</span></span>

<span data-ttu-id="562d2-175">Impossibile configurare il servizio DHCP.</span><span class="sxs-lookup"><span data-stu-id="562d2-175">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="562d2-176">**Non è possibile rinnovare il lease DHCP**</span><span class="sxs-lookup"><span data-stu-id="562d2-176">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="562d2-177">82</span><span class="sxs-lookup"><span data-stu-id="562d2-177">82</span></span>

<span data-ttu-id="562d2-178">Non è possibile rinnovare il lease DHCP.</span><span class="sxs-lookup"><span data-stu-id="562d2-178">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="562d2-179">**Non è possibile rilasciare il lease DHCP**</span><span class="sxs-lookup"><span data-stu-id="562d2-179">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="562d2-180">83</span><span class="sxs-lookup"><span data-stu-id="562d2-180">83</span></span>

<span data-ttu-id="562d2-181">Impossibile rilasciare il lease DHCP.</span><span class="sxs-lookup"><span data-stu-id="562d2-181">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="562d2-182">**IP non abilitato sulla scheda**</span><span class="sxs-lookup"><span data-stu-id="562d2-182">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="562d2-183">84</span><span class="sxs-lookup"><span data-stu-id="562d2-183">84</span></span>

<span data-ttu-id="562d2-184">IP non abilitato sulla scheda.</span><span class="sxs-lookup"><span data-stu-id="562d2-184">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="562d2-185">**IPX non abilitato sull'adapter**</span><span class="sxs-lookup"><span data-stu-id="562d2-185">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="562d2-186">85</span><span class="sxs-lookup"><span data-stu-id="562d2-186">85</span></span>

<span data-ttu-id="562d2-187">IPX non abilitato sulla scheda.</span><span class="sxs-lookup"><span data-stu-id="562d2-187">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="562d2-188">**Errore limite numero frame/rete**</span><span class="sxs-lookup"><span data-stu-id="562d2-188">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="562d2-189">86</span><span class="sxs-lookup"><span data-stu-id="562d2-189">86</span></span>

<span data-ttu-id="562d2-190">Errore dei limiti del numero di rete o del frame.</span><span class="sxs-lookup"><span data-stu-id="562d2-190">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="562d2-191">**Tipo di frame non valido**</span><span class="sxs-lookup"><span data-stu-id="562d2-191">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="562d2-192">87</span><span class="sxs-lookup"><span data-stu-id="562d2-192">87</span></span>

<span data-ttu-id="562d2-193">Tipo di frame non valido.</span><span class="sxs-lookup"><span data-stu-id="562d2-193">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="562d2-194">**Numero di rete non valido**</span><span class="sxs-lookup"><span data-stu-id="562d2-194">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="562d2-195">88</span><span class="sxs-lookup"><span data-stu-id="562d2-195">88</span></span>

<span data-ttu-id="562d2-196">Numero di rete non valido.</span><span class="sxs-lookup"><span data-stu-id="562d2-196">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="562d2-197">**Numero di rete duplicato**</span><span class="sxs-lookup"><span data-stu-id="562d2-197">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="562d2-198">89</span><span class="sxs-lookup"><span data-stu-id="562d2-198">89</span></span>

<span data-ttu-id="562d2-199">Numero di rete duplicato.</span><span class="sxs-lookup"><span data-stu-id="562d2-199">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="562d2-200">**Parametro fuori limite**</span><span class="sxs-lookup"><span data-stu-id="562d2-200">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="562d2-201">90</span><span class="sxs-lookup"><span data-stu-id="562d2-201">90</span></span>

<span data-ttu-id="562d2-202">Parametro fuori limite.</span><span class="sxs-lookup"><span data-stu-id="562d2-202">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="562d2-203">**Accesso negato**</span><span class="sxs-lookup"><span data-stu-id="562d2-203">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="562d2-204">91</span><span class="sxs-lookup"><span data-stu-id="562d2-204">91</span></span>

<span data-ttu-id="562d2-205">Accesso negato.</span><span class="sxs-lookup"><span data-stu-id="562d2-205">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="562d2-206">**Memoria insufficiente**</span><span class="sxs-lookup"><span data-stu-id="562d2-206">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="562d2-207">92</span><span class="sxs-lookup"><span data-stu-id="562d2-207">92</span></span>

<span data-ttu-id="562d2-208">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="562d2-208">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="562d2-209">**Esiste già**</span><span class="sxs-lookup"><span data-stu-id="562d2-209">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="562d2-210">93</span><span class="sxs-lookup"><span data-stu-id="562d2-210">93</span></span>

<span data-ttu-id="562d2-211">Esiste già.</span><span class="sxs-lookup"><span data-stu-id="562d2-211">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="562d2-212">**Percorso, file o oggetto non trovato**</span><span class="sxs-lookup"><span data-stu-id="562d2-212">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="562d2-213">94</span><span class="sxs-lookup"><span data-stu-id="562d2-213">94</span></span>

<span data-ttu-id="562d2-214">Il percorso, il file o l'oggetto non è stato trovato.</span><span class="sxs-lookup"><span data-stu-id="562d2-214">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="562d2-215">**Non è possibile inviare una notifica al servizio**</span><span class="sxs-lookup"><span data-stu-id="562d2-215">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="562d2-216">95</span><span class="sxs-lookup"><span data-stu-id="562d2-216">95</span></span>

<span data-ttu-id="562d2-217">Impossibile notificare il servizio.</span><span class="sxs-lookup"><span data-stu-id="562d2-217">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="562d2-218">**Non è possibile inviare una notifica al servizio DNS**</span><span class="sxs-lookup"><span data-stu-id="562d2-218">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="562d2-219">96</span><span class="sxs-lookup"><span data-stu-id="562d2-219">96</span></span>

<span data-ttu-id="562d2-220">Impossibile inviare una notifica al servizio DNS.</span><span class="sxs-lookup"><span data-stu-id="562d2-220">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="562d2-221">**Interfaccia non configurabile**</span><span class="sxs-lookup"><span data-stu-id="562d2-221">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="562d2-222">97</span><span class="sxs-lookup"><span data-stu-id="562d2-222">97</span></span>

<span data-ttu-id="562d2-223">Interfaccia non configurabile.</span><span class="sxs-lookup"><span data-stu-id="562d2-223">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="562d2-224">**Non tutti i lease DHCP possono essere rilasciati/rinnovati**</span><span class="sxs-lookup"><span data-stu-id="562d2-224">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="562d2-225">98</span><span class="sxs-lookup"><span data-stu-id="562d2-225">98</span></span>

<span data-ttu-id="562d2-226">Non tutti i lease DHCP possono essere rilasciati o rinnovati.</span><span class="sxs-lookup"><span data-stu-id="562d2-226">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="562d2-227">**DHCP non abilitato sull'adapter**</span><span class="sxs-lookup"><span data-stu-id="562d2-227">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="562d2-228">100</span><span class="sxs-lookup"><span data-stu-id="562d2-228">100</span></span>

<span data-ttu-id="562d2-229">DHCP non abilitato sulla scheda.</span><span class="sxs-lookup"><span data-stu-id="562d2-229">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="562d2-230">**Altri**</span><span class="sxs-lookup"><span data-stu-id="562d2-230">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="562d2-231">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="562d2-231">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="562d2-232">Commenti</span><span class="sxs-lookup"><span data-stu-id="562d2-232">Remarks</span></span>

<span data-ttu-id="562d2-233">La finestra di ricezione specifica il numero di byte che un mittente può trasmettere senza ricevere un riconoscimento.</span><span class="sxs-lookup"><span data-stu-id="562d2-233">The receive window specifies the number of bytes a sender can transmit without receiving an acknowledgment.</span></span> <span data-ttu-id="562d2-234">In generale, le finestre di ricezione più grandi migliorano le prestazioni rispetto alle reti a larghezza di banda elevata e a ritardo elevato.</span><span class="sxs-lookup"><span data-stu-id="562d2-234">In general, larger receive windows improve performance over high-delay and high-bandwidth networks.</span></span> <span data-ttu-id="562d2-235">Per migliorare l'efficienza, la finestra di ricezione deve essere un multiplo pari delle dimensioni del segmento massimo TCP (MSS).</span><span class="sxs-lookup"><span data-stu-id="562d2-235">For efficiency, the receive window should be an even multiple of the TCP Maximum Segment Size (MSS).</span></span>

> [!Note]  
> <span data-ttu-id="562d2-236">Windows Vista: questo metodo accede alla `"CurrentControlSet\\Services\\Tcpip\\Parameters|TcpWindowSize"` voce del registro di sistema, che non viene usata nell'implementazione corrente del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="562d2-236">Windows Vista: This method accesses the `"CurrentControlSet\\Services\\Tcpip\\Parameters|TcpWindowSize"` registry entry, which is not used in the current implementation of the operating system.</span></span>

 

## <a name="examples"></a><span data-ttu-id="562d2-237">Esempio</span><span class="sxs-lookup"><span data-stu-id="562d2-237">Examples</span></span>

<span data-ttu-id="562d2-238">L'esempio [modificare le dimensioni della finestra TCP per tutte le schede di rete](https://Gallery.TechNet.Microsoft.Com/74cf7be0-0044-4a88-85a3-9bc98490897b) VBScript imposta la dimensione della finestra TCP per tutte le schede di rete in un computer.</span><span class="sxs-lookup"><span data-stu-id="562d2-238">The [Modify the TCP Window Size for All Network Adapters](https://Gallery.TechNet.Microsoft.Com/74cf7be0-0044-4a88-85a3-9bc98490897b) VBScript sample sets the TCP window size for all network adapters on a computer.</span></span>

## <a name="requirements"></a><span data-ttu-id="562d2-239">Requisiti</span><span class="sxs-lookup"><span data-stu-id="562d2-239">Requirements</span></span>



| <span data-ttu-id="562d2-240">Requisito</span><span class="sxs-lookup"><span data-stu-id="562d2-240">Requirement</span></span> | <span data-ttu-id="562d2-241">Valore</span><span class="sxs-lookup"><span data-stu-id="562d2-241">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="562d2-242">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="562d2-242">Minimum supported client</span></span><br/> | <span data-ttu-id="562d2-243">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="562d2-243">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="562d2-244">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="562d2-244">Minimum supported server</span></span><br/> | <span data-ttu-id="562d2-245">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="562d2-245">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="562d2-246">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="562d2-246">End of client support</span></span><br/>    | <span data-ttu-id="562d2-247">Windows 7</span><span class="sxs-lookup"><span data-stu-id="562d2-247">Windows 7</span></span><br/>                                                                    |
| <span data-ttu-id="562d2-248">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="562d2-248">End of server support</span></span><br/>    | <span data-ttu-id="562d2-249">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="562d2-249">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="562d2-250">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="562d2-250">Namespace</span></span><br/>                | <span data-ttu-id="562d2-251">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="562d2-251">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="562d2-252">MOF</span><span class="sxs-lookup"><span data-stu-id="562d2-252">MOF</span></span><br/>                      | <dl> <span data-ttu-id="562d2-253"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="562d2-253"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="562d2-254">DLL</span><span class="sxs-lookup"><span data-stu-id="562d2-254">DLL</span></span><br/>                      | <dl> <span data-ttu-id="562d2-255"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="562d2-255"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="562d2-256">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="562d2-256">See also</span></span>

<dl> <dt>

[<span data-ttu-id="562d2-257">Classi hardware del sistema del computer</span><span class="sxs-lookup"><span data-stu-id="562d2-257">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="562d2-258">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="562d2-258">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="562d2-259">Attività WMI: rete</span><span class="sxs-lookup"><span data-stu-id="562d2-259">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="562d2-260">Attività WMI: account e domini</span><span class="sxs-lookup"><span data-stu-id="562d2-260">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="562d2-261">Supporto di IPv6 e IPv4 in WMI</span><span class="sxs-lookup"><span data-stu-id="562d2-261">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

