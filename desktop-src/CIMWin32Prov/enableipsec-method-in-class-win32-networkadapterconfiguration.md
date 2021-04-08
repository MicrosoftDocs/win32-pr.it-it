---
description: EnableIPSec&\# 8194; Il metodo della classe WMI Abilita Internet Protocol Security (IPsec) su una scheda di rete abilitata per TCP/IP.
ms.assetid: 0a45d864-606d-4adb-9b51-62d46a0d68b1
ms.tgt_platform: multiple
title: Metodo EnableIPSec della classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.EnableIPSec
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6988d68f9939752e3c8c2c9ace063b895a2d3720
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877601"
---
# <a name="enableipsec-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="f5917-103">Metodo EnableIPSec della \_ classe NetworkAdapterConfiguration Win32</span><span class="sxs-lookup"><span data-stu-id="f5917-103">EnableIPSec method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="f5917-104">Il metodo della [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **EnableIPSec** Abilita Internet Protocol Security (IPSec) su una scheda di rete abilitata per TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="f5917-104">The **EnableIPSec** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method enables Internet Protocol security (IPsec) on a TCP/IP-enabled network adapter.</span></span>

<span data-ttu-id="f5917-105">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="f5917-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="f5917-106">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="f5917-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="f5917-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f5917-107">Syntax</span></span>


```mof
uint32 EnableIPSec(
  [in] string IPSecPermitTCPPorts[],
  [in] string IPSecPermitUDPPorts[],
  [in] string IPSecPermitIPProtocols[]
);
```



## <a name="parameters"></a><span data-ttu-id="f5917-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="f5917-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5917-109">*IPSecPermitTCPPorts* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f5917-109">*IPSecPermitTCPPorts* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5917-110">Elenco di porte a cui concedere l'autorizzazione di accesso per TCP.</span><span class="sxs-lookup"><span data-stu-id="f5917-110">List of ports to be granted access permission for TCP.</span></span> <span data-ttu-id="f5917-111">Un valore numerico pari a 0 (zero) indica che è stata concessa l'autorizzazione di accesso per tutte le porte.</span><span class="sxs-lookup"><span data-stu-id="f5917-111">A numeric value of 0 (zero) indicates access permission is granted for all ports.</span></span> <span data-ttu-id="f5917-112">Una matrice vuota indica che a nessuna porta devono essere concesse le autorizzazioni di accesso.</span><span class="sxs-lookup"><span data-stu-id="f5917-112">An empty array indicates that no ports are to be granted access permission.</span></span>

</dd> <dt>

<span data-ttu-id="f5917-113">*IPSecPermitUDPPorts* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f5917-113">*IPSecPermitUDPPorts* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5917-114">Elenco di porte a cui concedere l'autorizzazione di accesso per UDP.</span><span class="sxs-lookup"><span data-stu-id="f5917-114">List of ports to be granted access permission for UDP.</span></span> <span data-ttu-id="f5917-115">Un valore numerico pari a 0 (zero) indica che è stata concessa l'autorizzazione di accesso per tutte le porte.</span><span class="sxs-lookup"><span data-stu-id="f5917-115">A numeric value of 0 (zero) indicates access permission is granted for all ports.</span></span> <span data-ttu-id="f5917-116">Una matrice vuota indica che a nessuna porta devono essere concesse le autorizzazioni di accesso.</span><span class="sxs-lookup"><span data-stu-id="f5917-116">An empty array indicates that no ports are to be granted access permission.</span></span>

</dd> <dt>

<span data-ttu-id="f5917-117">*IPSecPermitIPProtocols* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f5917-117">*IPSecPermitIPProtocols* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5917-118">Elenco di protocolli di cui è consentita l'esecuzione su IP.</span><span class="sxs-lookup"><span data-stu-id="f5917-118">List of protocols permitted to run over the IP.</span></span> <span data-ttu-id="f5917-119">Un valore numerico pari a 0 (zero) indica che è stata concessa l'autorizzazione di accesso per tutti i protocolli.</span><span class="sxs-lookup"><span data-stu-id="f5917-119">A numeric value of 0 (zero) indicates access permission is granted for all protocols.</span></span> <span data-ttu-id="f5917-120">Una matrice vuota indica che ai protocolli non è stata concessa l'autorizzazione di accesso.</span><span class="sxs-lookup"><span data-stu-id="f5917-120">An empty array indicates that no protocols are granted access permission.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5917-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f5917-121">Return value</span></span>

<span data-ttu-id="f5917-122">Restituisce un valore pari a 0 (zero) per un completamento corretto quando non è richiesto un riavvio, 1 (uno) per un completamento corretto quando è necessario un riavvio e qualsiasi altro numero se si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="f5917-122">Returns a value of 0 (zero) for a successful completion when a reboot is not required, 1 (one) for a successful completion when a reboot is required, and any other number if there is an error.</span></span> <span data-ttu-id="f5917-123">Per ulteriori informazioni sui codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="f5917-123">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="f5917-124">Per i valori **HRESULT** generali, vedere [codici di errore di sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="f5917-124">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="f5917-125">**Operazione completata, non è necessario riavviare il computer**</span><span class="sxs-lookup"><span data-stu-id="f5917-125">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="f5917-126">0</span><span class="sxs-lookup"><span data-stu-id="f5917-126">0</span></span>

<span data-ttu-id="f5917-127">Operazione completata, non è necessario riavviare il computer.</span><span class="sxs-lookup"><span data-stu-id="f5917-127">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="f5917-128">**Operazione completata, riavvio richiesto**</span><span class="sxs-lookup"><span data-stu-id="f5917-128">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="f5917-129">1</span><span class="sxs-lookup"><span data-stu-id="f5917-129">1</span></span>

<span data-ttu-id="f5917-130">Operazione completata, è necessario riavviare il computer.</span><span class="sxs-lookup"><span data-stu-id="f5917-130">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="f5917-131">**Metodo non supportato in questa piattaforma**</span><span class="sxs-lookup"><span data-stu-id="f5917-131">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="f5917-132">64</span><span class="sxs-lookup"><span data-stu-id="f5917-132">64</span></span>

<span data-ttu-id="f5917-133">Metodo non supportato in questa piattaforma.</span><span class="sxs-lookup"><span data-stu-id="f5917-133">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="f5917-134">**Errore sconosciuto**</span><span class="sxs-lookup"><span data-stu-id="f5917-134">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="f5917-135">65</span><span class="sxs-lookup"><span data-stu-id="f5917-135">65</span></span>

<span data-ttu-id="f5917-136">Errore sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="f5917-136">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="f5917-137">**subnet mask non valido**</span><span class="sxs-lookup"><span data-stu-id="f5917-137">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="f5917-138">66</span><span class="sxs-lookup"><span data-stu-id="f5917-138">66</span></span>

<span data-ttu-id="f5917-139">Subnet mask non valido.</span><span class="sxs-lookup"><span data-stu-id="f5917-139">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="f5917-140">**Si è verificato un errore durante l'elaborazione di un'istanza restituita**</span><span class="sxs-lookup"><span data-stu-id="f5917-140">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="f5917-141">67</span><span class="sxs-lookup"><span data-stu-id="f5917-141">67</span></span>

<span data-ttu-id="f5917-142">Si è verificato un errore durante l'elaborazione di un'istanza di restituita.</span><span class="sxs-lookup"><span data-stu-id="f5917-142">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="f5917-143">**Parametro di input non valido**</span><span class="sxs-lookup"><span data-stu-id="f5917-143">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="f5917-144">68</span><span class="sxs-lookup"><span data-stu-id="f5917-144">68</span></span>

<span data-ttu-id="f5917-145">Parametro di input non valido.</span><span class="sxs-lookup"><span data-stu-id="f5917-145">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="f5917-146">**Sono stati specificati più di 5 gateway**</span><span class="sxs-lookup"><span data-stu-id="f5917-146">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="f5917-147">69</span><span class="sxs-lookup"><span data-stu-id="f5917-147">69</span></span>

<span data-ttu-id="f5917-148">Sono stati specificati più di cinque gateway.</span><span class="sxs-lookup"><span data-stu-id="f5917-148">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="f5917-149">**Indirizzo IP non valido**</span><span class="sxs-lookup"><span data-stu-id="f5917-149">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="f5917-150">70</span><span class="sxs-lookup"><span data-stu-id="f5917-150">70</span></span>

<span data-ttu-id="f5917-151">Indirizzo IP non valido.</span><span class="sxs-lookup"><span data-stu-id="f5917-151">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="f5917-152">**Indirizzo IP gateway non valido**</span><span class="sxs-lookup"><span data-stu-id="f5917-152">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="f5917-153">71</span><span class="sxs-lookup"><span data-stu-id="f5917-153">71</span></span>

<span data-ttu-id="f5917-154">Indirizzo IP del gateway non valido.</span><span class="sxs-lookup"><span data-stu-id="f5917-154">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="f5917-155">**Si è verificato un errore durante l'accesso al registro di sistema per le informazioni richieste**</span><span class="sxs-lookup"><span data-stu-id="f5917-155">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="f5917-156">72</span><span class="sxs-lookup"><span data-stu-id="f5917-156">72</span></span>

<span data-ttu-id="f5917-157">Si è verificato un errore durante l'accesso al registro di sistema per le informazioni richieste.</span><span class="sxs-lookup"><span data-stu-id="f5917-157">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="f5917-158">**Nome di dominio non valido**</span><span class="sxs-lookup"><span data-stu-id="f5917-158">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="f5917-159">73</span><span class="sxs-lookup"><span data-stu-id="f5917-159">73</span></span>

<span data-ttu-id="f5917-160">Nome di dominio non valido.</span><span class="sxs-lookup"><span data-stu-id="f5917-160">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="f5917-161">**Nome host non valido**</span><span class="sxs-lookup"><span data-stu-id="f5917-161">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="f5917-162">74</span><span class="sxs-lookup"><span data-stu-id="f5917-162">74</span></span>

<span data-ttu-id="f5917-163">Nome host non valido.</span><span class="sxs-lookup"><span data-stu-id="f5917-163">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="f5917-164">**Nessun server WINS primario/secondario definito**</span><span class="sxs-lookup"><span data-stu-id="f5917-164">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="f5917-165">75</span><span class="sxs-lookup"><span data-stu-id="f5917-165">75</span></span>

<span data-ttu-id="f5917-166">Nessun server WINS primario o secondario definito.</span><span class="sxs-lookup"><span data-stu-id="f5917-166">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="f5917-167">**File non valido**</span><span class="sxs-lookup"><span data-stu-id="f5917-167">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="f5917-168">76</span><span class="sxs-lookup"><span data-stu-id="f5917-168">76</span></span>

<span data-ttu-id="f5917-169">File non valido.</span><span class="sxs-lookup"><span data-stu-id="f5917-169">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="f5917-170">**Percorso di sistema non valido**</span><span class="sxs-lookup"><span data-stu-id="f5917-170">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="f5917-171">77</span><span class="sxs-lookup"><span data-stu-id="f5917-171">77</span></span>

<span data-ttu-id="f5917-172">Percorso di sistema non valido.</span><span class="sxs-lookup"><span data-stu-id="f5917-172">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="f5917-173">**Copia del file non riuscita**</span><span class="sxs-lookup"><span data-stu-id="f5917-173">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="f5917-174">78</span><span class="sxs-lookup"><span data-stu-id="f5917-174">78</span></span>

<span data-ttu-id="f5917-175">Copia del file non riuscita.</span><span class="sxs-lookup"><span data-stu-id="f5917-175">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="f5917-176">**Parametro di sicurezza non valido**</span><span class="sxs-lookup"><span data-stu-id="f5917-176">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="f5917-177">79</span><span class="sxs-lookup"><span data-stu-id="f5917-177">79</span></span>

<span data-ttu-id="f5917-178">Parametro di sicurezza non valido.</span><span class="sxs-lookup"><span data-stu-id="f5917-178">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="f5917-179">**Impossibile configurare il servizio TCP/IP**</span><span class="sxs-lookup"><span data-stu-id="f5917-179">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="f5917-180">80</span><span class="sxs-lookup"><span data-stu-id="f5917-180">80</span></span>

<span data-ttu-id="f5917-181">Impossibile configurare il servizio TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="f5917-181">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="f5917-182">**Non è possibile configurare il servizio DHCP**</span><span class="sxs-lookup"><span data-stu-id="f5917-182">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="f5917-183">81</span><span class="sxs-lookup"><span data-stu-id="f5917-183">81</span></span>

<span data-ttu-id="f5917-184">Impossibile configurare il servizio DHCP.</span><span class="sxs-lookup"><span data-stu-id="f5917-184">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="f5917-185">**Non è possibile rinnovare il lease DHCP**</span><span class="sxs-lookup"><span data-stu-id="f5917-185">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="f5917-186">82</span><span class="sxs-lookup"><span data-stu-id="f5917-186">82</span></span>

<span data-ttu-id="f5917-187">Non è possibile rinnovare il lease DHCP.</span><span class="sxs-lookup"><span data-stu-id="f5917-187">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="f5917-188">**Non è possibile rilasciare il lease DHCP**</span><span class="sxs-lookup"><span data-stu-id="f5917-188">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="f5917-189">83</span><span class="sxs-lookup"><span data-stu-id="f5917-189">83</span></span>

<span data-ttu-id="f5917-190">Impossibile rilasciare il lease DHCP.</span><span class="sxs-lookup"><span data-stu-id="f5917-190">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="f5917-191">**IP non abilitato sulla scheda**</span><span class="sxs-lookup"><span data-stu-id="f5917-191">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="f5917-192">84</span><span class="sxs-lookup"><span data-stu-id="f5917-192">84</span></span>

<span data-ttu-id="f5917-193">IP non abilitato sulla scheda.</span><span class="sxs-lookup"><span data-stu-id="f5917-193">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="f5917-194">**IPX non abilitato sull'adapter**</span><span class="sxs-lookup"><span data-stu-id="f5917-194">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="f5917-195">85</span><span class="sxs-lookup"><span data-stu-id="f5917-195">85</span></span>

<span data-ttu-id="f5917-196">IPX non abilitato sulla scheda.</span><span class="sxs-lookup"><span data-stu-id="f5917-196">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="f5917-197">**Errore limite numero frame/rete**</span><span class="sxs-lookup"><span data-stu-id="f5917-197">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="f5917-198">86</span><span class="sxs-lookup"><span data-stu-id="f5917-198">86</span></span>

<span data-ttu-id="f5917-199">Errore dei limiti del numero di rete o del frame.</span><span class="sxs-lookup"><span data-stu-id="f5917-199">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="f5917-200">**Tipo di frame non valido**</span><span class="sxs-lookup"><span data-stu-id="f5917-200">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="f5917-201">87</span><span class="sxs-lookup"><span data-stu-id="f5917-201">87</span></span>

<span data-ttu-id="f5917-202">Tipo di frame non valido.</span><span class="sxs-lookup"><span data-stu-id="f5917-202">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="f5917-203">**Numero di rete non valido**</span><span class="sxs-lookup"><span data-stu-id="f5917-203">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="f5917-204">88</span><span class="sxs-lookup"><span data-stu-id="f5917-204">88</span></span>

<span data-ttu-id="f5917-205">Numero di rete non valido.</span><span class="sxs-lookup"><span data-stu-id="f5917-205">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="f5917-206">**Numero di rete duplicato**</span><span class="sxs-lookup"><span data-stu-id="f5917-206">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="f5917-207">89</span><span class="sxs-lookup"><span data-stu-id="f5917-207">89</span></span>

<span data-ttu-id="f5917-208">Numero di rete duplicato.</span><span class="sxs-lookup"><span data-stu-id="f5917-208">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="f5917-209">**Parametro fuori limite**</span><span class="sxs-lookup"><span data-stu-id="f5917-209">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="f5917-210">90</span><span class="sxs-lookup"><span data-stu-id="f5917-210">90</span></span>

<span data-ttu-id="f5917-211">Parametro fuori limite.</span><span class="sxs-lookup"><span data-stu-id="f5917-211">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="f5917-212">**Accesso negato**</span><span class="sxs-lookup"><span data-stu-id="f5917-212">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="f5917-213">91</span><span class="sxs-lookup"><span data-stu-id="f5917-213">91</span></span>

<span data-ttu-id="f5917-214">Accesso negato.</span><span class="sxs-lookup"><span data-stu-id="f5917-214">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="f5917-215">**Memoria insufficiente**</span><span class="sxs-lookup"><span data-stu-id="f5917-215">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="f5917-216">92</span><span class="sxs-lookup"><span data-stu-id="f5917-216">92</span></span>

<span data-ttu-id="f5917-217">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="f5917-217">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="f5917-218">**Esiste già**</span><span class="sxs-lookup"><span data-stu-id="f5917-218">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="f5917-219">93</span><span class="sxs-lookup"><span data-stu-id="f5917-219">93</span></span>

<span data-ttu-id="f5917-220">Esiste già.</span><span class="sxs-lookup"><span data-stu-id="f5917-220">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="f5917-221">**Percorso, file o oggetto non trovato**</span><span class="sxs-lookup"><span data-stu-id="f5917-221">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="f5917-222">94</span><span class="sxs-lookup"><span data-stu-id="f5917-222">94</span></span>

<span data-ttu-id="f5917-223">Il percorso, il file o l'oggetto non è stato trovato.</span><span class="sxs-lookup"><span data-stu-id="f5917-223">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="f5917-224">**Non è possibile inviare una notifica al servizio**</span><span class="sxs-lookup"><span data-stu-id="f5917-224">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="f5917-225">95</span><span class="sxs-lookup"><span data-stu-id="f5917-225">95</span></span>

<span data-ttu-id="f5917-226">Impossibile notificare il servizio.</span><span class="sxs-lookup"><span data-stu-id="f5917-226">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="f5917-227">**Non è possibile inviare una notifica al servizio DNS**</span><span class="sxs-lookup"><span data-stu-id="f5917-227">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="f5917-228">96</span><span class="sxs-lookup"><span data-stu-id="f5917-228">96</span></span>

<span data-ttu-id="f5917-229">Impossibile inviare una notifica al servizio DNS.</span><span class="sxs-lookup"><span data-stu-id="f5917-229">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="f5917-230">**Interfaccia non configurabile**</span><span class="sxs-lookup"><span data-stu-id="f5917-230">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="f5917-231">97</span><span class="sxs-lookup"><span data-stu-id="f5917-231">97</span></span>

<span data-ttu-id="f5917-232">Interfaccia non configurabile.</span><span class="sxs-lookup"><span data-stu-id="f5917-232">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="f5917-233">**Non tutti i lease DHCP possono essere rilasciati/rinnovati**</span><span class="sxs-lookup"><span data-stu-id="f5917-233">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="f5917-234">98</span><span class="sxs-lookup"><span data-stu-id="f5917-234">98</span></span>

<span data-ttu-id="f5917-235">Non tutti i lease DHCP possono essere rilasciati o rinnovati.</span><span class="sxs-lookup"><span data-stu-id="f5917-235">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="f5917-236">**DHCP non abilitato sull'adapter**</span><span class="sxs-lookup"><span data-stu-id="f5917-236">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="f5917-237">100</span><span class="sxs-lookup"><span data-stu-id="f5917-237">100</span></span>

<span data-ttu-id="f5917-238">DHCP non abilitato nell'adapter.</span><span class="sxs-lookup"><span data-stu-id="f5917-238">DHCP not enabled on the adapter.</span></span>

</dd> <dt>

<span data-ttu-id="f5917-239">**Altri**</span><span class="sxs-lookup"><span data-stu-id="f5917-239">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="f5917-240">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="f5917-240">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f5917-241">Commenti</span><span class="sxs-lookup"><span data-stu-id="f5917-241">Remarks</span></span>

<span data-ttu-id="f5917-242">Le porte sono protette solo quando la proprietà **IPFilterSecurityEnabled** in [**Win32 \_ NetworkAdapterConfiguration**](win32-networkadapterconfiguration.md) è **true**.</span><span class="sxs-lookup"><span data-stu-id="f5917-242">Ports are secured only when the **IPFilterSecurityEnabled** property in [**Win32\_NetworkAdapterConfiguration**](win32-networkadapterconfiguration.md) is **true**.</span></span>

## <a name="examples"></a><span data-ttu-id="f5917-243">Esempio</span><span class="sxs-lookup"><span data-stu-id="f5917-243">Examples</span></span>

<span data-ttu-id="f5917-244">L'esempio [Enable IPSec on a Network Adapter](https://Gallery.TechNet.Microsoft.Com/ff821218-c392-42fb-a77c-c3eab899587c) VBScript, sulla raccolta TechNet, USA **EnableIPSec** per abilitare la sicurezza IP per una scheda di rete.</span><span class="sxs-lookup"><span data-stu-id="f5917-244">The [Enable IPSec on a Network Adapter](https://Gallery.TechNet.Microsoft.Com/ff821218-c392-42fb-a77c-c3eab899587c) VBScript sample, on TechNet Gallery, uses **EnableIPSec** to enable IP security for a network adapter.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5917-245">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f5917-245">Requirements</span></span>



| <span data-ttu-id="f5917-246">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5917-246">Requirement</span></span> | <span data-ttu-id="f5917-247">Valore</span><span class="sxs-lookup"><span data-stu-id="f5917-247">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f5917-248">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f5917-248">Minimum supported client</span></span><br/> | <span data-ttu-id="f5917-249">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f5917-249">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f5917-250">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f5917-250">Minimum supported server</span></span><br/> | <span data-ttu-id="f5917-251">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f5917-251">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f5917-252">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f5917-252">Namespace</span></span><br/>                | <span data-ttu-id="f5917-253">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="f5917-253">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f5917-254">MOF</span><span class="sxs-lookup"><span data-stu-id="f5917-254">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f5917-255"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f5917-255"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f5917-256">DLL</span><span class="sxs-lookup"><span data-stu-id="f5917-256">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f5917-257"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f5917-257"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5917-258">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f5917-258">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5917-259">Classi hardware del sistema del computer</span><span class="sxs-lookup"><span data-stu-id="f5917-259">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="f5917-260">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="f5917-260">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="f5917-261">Attività WMI: rete</span><span class="sxs-lookup"><span data-stu-id="f5917-261">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="f5917-262">Attività WMI: account e domini</span><span class="sxs-lookup"><span data-stu-id="f5917-262">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="f5917-263">Supporto di IPv6 e IPv4 in WMI</span><span class="sxs-lookup"><span data-stu-id="f5917-263">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

