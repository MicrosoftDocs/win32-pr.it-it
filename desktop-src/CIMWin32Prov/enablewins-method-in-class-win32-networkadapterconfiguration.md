---
description: EnableWINS &\# 32; Il metodo statico della classe WMI Abilita le impostazioni di Windows Internet Naming Service (WINS) specifiche per TCP/IP, ma indipendente dalla scheda di rete.
ms.assetid: ce0fb170-978f-4d70-bced-e530e43da719
ms.tgt_platform: multiple
title: Metodo EnableWINS della classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.EnableWINS
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 77f5ba32606ff228908e8b7a1559a73ae5139e9c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523386"
---
# <a name="enablewins-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="5ac4f-103">Metodo EnableWINS della \_ classe NetworkAdapterConfiguration Win32</span><span class="sxs-lookup"><span data-stu-id="5ac4f-103">EnableWINS method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="5ac4f-104">Il metodo statico della [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **EnableWINS** Abilita le impostazioni WINS (Windows Internet Naming Service) specifiche per TCP/IP, ma indipendente dalla scheda di rete.</span><span class="sxs-lookup"><span data-stu-id="5ac4f-104">The **EnableWINS** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method enables Windows Internet Naming Service (WINS) settings specific to TCP/IP, but independent of the network adapter.</span></span>

<span data-ttu-id="5ac4f-105">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="5ac4f-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="5ac4f-106">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="5ac4f-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="5ac4f-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5ac4f-107">Syntax</span></span>


```mof
uint32 EnableWINS(
  [in]           boolean DNSEnabledForWINSResolution,
  [in]           boolean WINSEnableLMHostsLookup,
  [in, optional] string  WINSHostLookupFile,
  [in, optional] string  WINSScopeID
);
```



## <a name="parameters"></a><span data-ttu-id="5ac4f-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="5ac4f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ac4f-109">*DNSEnabledForWINSResolution* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5ac4f-109">*DNSEnabledForWINSResolution* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ac4f-110">Se **true**, il Domain Name System (DNS) è abilitato per la risoluzione dei nomi rispetto alla risoluzione WINS.</span><span class="sxs-lookup"><span data-stu-id="5ac4f-110">If **true**, the Domain Name System (DNS) is enabled for name resolution over WINS resolution.</span></span>

</dd> <dt>

<span data-ttu-id="5ac4f-111">*WINSEnableLMHostsLookup* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5ac4f-111">*WINSEnableLMHostsLookup* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ac4f-112">Se **true**, vengono usati i file di ricerca locali.</span><span class="sxs-lookup"><span data-stu-id="5ac4f-112">If **true**, local lookup files are used.</span></span> <span data-ttu-id="5ac4f-113">I file di ricerca conterranno i mapping degli indirizzi IP ai nomi host.</span><span class="sxs-lookup"><span data-stu-id="5ac4f-113">Lookup files will contain mappings of IP addresses to host names.</span></span>

</dd> <dt>

<span data-ttu-id="5ac4f-114">*WINSHostLookupFile* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="5ac4f-114">*WINSHostLookupFile* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5ac4f-115">File di ricerca che contengono mapping degli indirizzi IP ai nomi host.</span><span class="sxs-lookup"><span data-stu-id="5ac4f-115">Lookup files that contain mappings of IP addresses to host names.</span></span> <span data-ttu-id="5ac4f-116">Se disponibile, i file verranno trovati nei driver% SystemRoot% \\ system32 \\ \\ .</span><span class="sxs-lookup"><span data-stu-id="5ac4f-116">If available, the files will be found in %SystemRoot%\\system32\\drivers\\ .</span></span>

</dd> <dt>

<span data-ttu-id="5ac4f-117">*WINSScopeID* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="5ac4f-117">*WINSScopeID* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5ac4f-118">Valore dell'identificatore dell'ambito che verrà aggiunto alla fine del nome NetBIOS del computer.</span><span class="sxs-lookup"><span data-stu-id="5ac4f-118">Scope identifier value that will be appended to the end of the computer's NetBIOS name.</span></span> <span data-ttu-id="5ac4f-119">I sistemi che utilizzano lo stesso identificatore di ambito possono comunicare con questo computer.</span><span class="sxs-lookup"><span data-stu-id="5ac4f-119">Systems that use the same scope identifier can communicate with this computer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ac4f-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5ac4f-120">Return value</span></span>

<span data-ttu-id="5ac4f-121">Restituisce un valore pari a 0 (zero) per un completamento corretto quando non è necessario riavviare il computer; 1 (uno) per un completamento corretto quando è necessario un riavvio; un numero diverso se si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="5ac4f-121">Returns a value of 0 (zero) for a successful completion when no reboot is required; 1 (one) for a successful completion when a reboot is required; a different number if there is an error.</span></span> <span data-ttu-id="5ac4f-122">Per ulteriori informazioni sui codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="5ac4f-122">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="5ac4f-123">Per i valori **HRESULT** generali, vedere [codici di errore di sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="5ac4f-123">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="5ac4f-124">**Operazione completata, non è necessario riavviare** il computer (0)</span><span class="sxs-lookup"><span data-stu-id="5ac4f-124">**Successful completion, no reboot required** (0)</span></span>
</dt> <dt>

<span data-ttu-id="5ac4f-125">**Operazione completata, riavvio richiesto** (1)</span><span class="sxs-lookup"><span data-stu-id="5ac4f-125">**Successful completion, reboot required** (1)</span></span>
</dt> <dt>

<span data-ttu-id="5ac4f-126">**Metodo non supportato in questa piattaforma** (64)</span><span class="sxs-lookup"><span data-stu-id="5ac4f-126">**Method not supported on this platform** (64)</span></span>
</dt> <dt>

<span data-ttu-id="5ac4f-127">**Errore sconosciuto** (65)</span><span class="sxs-lookup"><span data-stu-id="5ac4f-127">**Unknown failure** (65)</span></span>
</dt> <dt>

<span data-ttu-id="5ac4f-128">**Subnet mask non valido** (66)</span><span class="sxs-lookup"><span data-stu-id="5ac4f-128">**Invalid subnet mask** (66)</span></span>
</dt> <dt>

<span data-ttu-id="5ac4f-129">**Si è verificato un errore durante l'elaborazione di un'istanza restituita** (67)</span><span class="sxs-lookup"><span data-stu-id="5ac4f-129">**An error occurred while processing an Instance that was returned** (67)</span></span>
</dt> <dt>

<span data-ttu-id="5ac4f-130">**Parametro di input non valido** (68)</span><span class="sxs-lookup"><span data-stu-id="5ac4f-130">**Invalid input parameter** (68)</span></span>
</dt> <dt>

<span data-ttu-id="5ac4f-131">Sono stati **specificati più di 5 gateway** (69)</span><span class="sxs-lookup"><span data-stu-id="5ac4f-131">**More than 5 gateways specified** (69)</span></span>
</dt> <dt>

<span data-ttu-id="5ac4f-132">**Indirizzo IP non valido** (70)</span><span class="sxs-lookup"><span data-stu-id="5ac4f-132">**Invalid IP address** (70)</span></span>
</dt> <dt>

<span data-ttu-id="5ac4f-133">**Indirizzo IP gateway non valido** (71)</span><span class="sxs-lookup"><span data-stu-id="5ac4f-133">**Invalid gateway IP address** (71)</span></span>
</dt> <dt>

<span data-ttu-id="5ac4f-134">**Si è verificato un errore durante l'accesso al registro di sistema per le informazioni richieste** (72)</span><span class="sxs-lookup"><span data-stu-id="5ac4f-134">**An error occurred while accessing the Registry for the requested information** (72)</span></span>
</dt> <dt>

<span data-ttu-id="5ac4f-135">**Nome di dominio non valido** (73)</span><span class="sxs-lookup"><span data-stu-id="5ac4f-135">**Invalid domain name** (73)</span></span>
</dt> <dt>

<span data-ttu-id="5ac4f-136">**Nome host non valido** (74)</span><span class="sxs-lookup"><span data-stu-id="5ac4f-136">**Invalid host name** (74)</span></span>
</dt> <dt>

<span data-ttu-id="5ac4f-137">**Nessun server WINS primario/secondario definito** (75)</span><span class="sxs-lookup"><span data-stu-id="5ac4f-137">**No primary/secondary WINS server defined** (75)</span></span>
</dt> <dt>

<span data-ttu-id="5ac4f-138">**File non valido** (76)</span><span class="sxs-lookup"><span data-stu-id="5ac4f-138">**Invalid file** (76)</span></span>
</dt> <dt>

<span data-ttu-id="5ac4f-139">**Percorso di sistema non valido** (77)</span><span class="sxs-lookup"><span data-stu-id="5ac4f-139">**Invalid system path** (77)</span></span>
</dt> <dt>

<span data-ttu-id="5ac4f-140">**Copia del file non riuscita** (78)</span><span class="sxs-lookup"><span data-stu-id="5ac4f-140">**File copy failed** (78)</span></span>
</dt> <dt>

<span data-ttu-id="5ac4f-141">**Parametro di sicurezza non valido** (79)</span><span class="sxs-lookup"><span data-stu-id="5ac4f-141">**Invalid security parameter** (79)</span></span>
</dt> <dt>

<span data-ttu-id="5ac4f-142">**Impossibile configurare il servizio TCP/IP** (80)</span><span class="sxs-lookup"><span data-stu-id="5ac4f-142">**Unable to configure TCP/IP service** (80)</span></span>
</dt> <dt>

<span data-ttu-id="5ac4f-143">**Impossibile configurare il servizio DHCP** (81)</span><span class="sxs-lookup"><span data-stu-id="5ac4f-143">**Unable to configure DHCP service** (81)</span></span>
</dt> <dt>

<span data-ttu-id="5ac4f-144">**Non è possibile rinnovare il lease DHCP** (82)</span><span class="sxs-lookup"><span data-stu-id="5ac4f-144">**Unable to renew DHCP lease** (82)</span></span>
</dt> <dt>

<span data-ttu-id="5ac4f-145">**Impossibile rilasciare il lease DHCP** (83)</span><span class="sxs-lookup"><span data-stu-id="5ac4f-145">**Unable to release DHCP lease** (83)</span></span>
</dt> <dt>

<span data-ttu-id="5ac4f-146">**IP non abilitato sulla scheda** (84)</span><span class="sxs-lookup"><span data-stu-id="5ac4f-146">**IP not enabled on adapter** (84)</span></span>
</dt> <dt>

<span data-ttu-id="5ac4f-147">**IPX non abilitato sulla scheda** (85)</span><span class="sxs-lookup"><span data-stu-id="5ac4f-147">**IPX not enabled on adapter** (85)</span></span>
</dt> <dt>

<span data-ttu-id="5ac4f-148">**Errore limite numero frame/rete** (86)</span><span class="sxs-lookup"><span data-stu-id="5ac4f-148">**Frame/network number bounds error** (86)</span></span>
</dt> <dt>

<span data-ttu-id="5ac4f-149">**Tipo di frame non valido** (87)</span><span class="sxs-lookup"><span data-stu-id="5ac4f-149">**Invalid frame type** (87)</span></span>
</dt> <dt>

<span data-ttu-id="5ac4f-150">**Numero di rete non valido** (88)</span><span class="sxs-lookup"><span data-stu-id="5ac4f-150">**Invalid network number** (88)</span></span>
</dt> <dt>

<span data-ttu-id="5ac4f-151">**Numero di rete duplicato** (89)</span><span class="sxs-lookup"><span data-stu-id="5ac4f-151">**Duplicate network number** (89)</span></span>
</dt> <dt>

<span data-ttu-id="5ac4f-152">**Parametro fuori limite** (90)</span><span class="sxs-lookup"><span data-stu-id="5ac4f-152">**Parameter out of bounds** (90)</span></span>
</dt> <dt>

<span data-ttu-id="5ac4f-153">**Accesso negato** (91)</span><span class="sxs-lookup"><span data-stu-id="5ac4f-153">**Access denied** (91)</span></span>
</dt> <dt>

<span data-ttu-id="5ac4f-154">**Memoria insufficiente** (92)</span><span class="sxs-lookup"><span data-stu-id="5ac4f-154">**Out of memory** (92)</span></span>
</dt> <dt>

<span data-ttu-id="5ac4f-155">**Già esistente** (93)</span><span class="sxs-lookup"><span data-stu-id="5ac4f-155">**Already exists** (93)</span></span>
</dt> <dt>

<span data-ttu-id="5ac4f-156">**Percorso, file o oggetto non trovato** (94)</span><span class="sxs-lookup"><span data-stu-id="5ac4f-156">**Path, file or object not found** (94)</span></span>
</dt> <dt>

<span data-ttu-id="5ac4f-157">**Non è possibile inviare una notifica al servizio** (95)</span><span class="sxs-lookup"><span data-stu-id="5ac4f-157">**Unable to notify service** (95)</span></span>
</dt> <dt>

<span data-ttu-id="5ac4f-158">**Impossibile inviare una notifica al servizio DNS** (96)</span><span class="sxs-lookup"><span data-stu-id="5ac4f-158">**Unable to notify DNS service** (96)</span></span>
</dt> <dt>

<span data-ttu-id="5ac4f-159">**Interfaccia non configurabile** (97)</span><span class="sxs-lookup"><span data-stu-id="5ac4f-159">**Interface not configurable** (97)</span></span>
</dt> <dt>

<span data-ttu-id="5ac4f-160">**Non tutti i lease DHCP possono essere rilasciati/rinnovati** (98)</span><span class="sxs-lookup"><span data-stu-id="5ac4f-160">**Not all DHCP leases could be released/renewed** (98)</span></span>
</dt> <dt>

<span data-ttu-id="5ac4f-161">**DHCP non abilitato sulla scheda** (100)</span><span class="sxs-lookup"><span data-stu-id="5ac4f-161">**DHCP not enabled on adapter** (100)</span></span>
</dt> <dt>

<span data-ttu-id="5ac4f-162">**Altro** (101 4294967295)</span><span class="sxs-lookup"><span data-stu-id="5ac4f-162">**Other** (101 4294967295)</span></span>
</dt> </dl>

## <a name="examples"></a><span data-ttu-id="5ac4f-163">Esempio</span><span class="sxs-lookup"><span data-stu-id="5ac4f-163">Examples</span></span>

<span data-ttu-id="5ac4f-164">L'esempio di codice per [abilitare WINS per tutte le schede di rete](https://Gallery.TechNet.Microsoft.Com/64cae6dd-4155-4825-ab25-5727503edf5a) VBScript, nella raccolta TechNet, USA **ENABLEWINS** per abilitare WINS in tutte le schede di rete installate in un computer.</span><span class="sxs-lookup"><span data-stu-id="5ac4f-164">The [Enable WINS for All Network Adapters](https://Gallery.TechNet.Microsoft.Com/64cae6dd-4155-4825-ab25-5727503edf5a) VBScript code sample, on TechNet Gallery, uses **EnableWINS** to Enables WINS on all the network adapters installed in a computer.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ac4f-165">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5ac4f-165">Requirements</span></span>



| <span data-ttu-id="5ac4f-166">Requisito</span><span class="sxs-lookup"><span data-stu-id="5ac4f-166">Requirement</span></span> | <span data-ttu-id="5ac4f-167">Valore</span><span class="sxs-lookup"><span data-stu-id="5ac4f-167">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5ac4f-168">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5ac4f-168">Minimum supported client</span></span><br/> | <span data-ttu-id="5ac4f-169">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5ac4f-169">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5ac4f-170">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5ac4f-170">Minimum supported server</span></span><br/> | <span data-ttu-id="5ac4f-171">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5ac4f-171">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5ac4f-172">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="5ac4f-172">Namespace</span></span><br/>                | <span data-ttu-id="5ac4f-173">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="5ac4f-173">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5ac4f-174">MOF</span><span class="sxs-lookup"><span data-stu-id="5ac4f-174">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5ac4f-175"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5ac4f-175"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5ac4f-176">DLL</span><span class="sxs-lookup"><span data-stu-id="5ac4f-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5ac4f-177"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5ac4f-177"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ac4f-178">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5ac4f-178">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ac4f-179">Classi hardware del sistema del computer</span><span class="sxs-lookup"><span data-stu-id="5ac4f-179">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="5ac4f-180">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="5ac4f-180">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="5ac4f-181">Attività WMI: rete</span><span class="sxs-lookup"><span data-stu-id="5ac4f-181">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="5ac4f-182">Attività WMI: account e domini</span><span class="sxs-lookup"><span data-stu-id="5ac4f-182">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="5ac4f-183">Supporto di IPv6 e IPv4 in WMI</span><span class="sxs-lookup"><span data-stu-id="5ac4f-183">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

