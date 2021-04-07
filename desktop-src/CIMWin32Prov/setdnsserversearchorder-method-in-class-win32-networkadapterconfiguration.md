---
description: SetDNSServerSearchOrder &\# 32; Il metodo della classe WMI utilizza una matrice di elementi stringa per impostare l'ordine di ricerca del server.
ms.assetid: fce688fa-7264-4965-8e1c-138160e03a7e
ms.tgt_platform: multiple
title: Metodo SetDNSServerSearchOrder della classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetDNSServerSearchOrder
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2bfe731ea1d89e8e0ad702bfa229a61fba30dfc7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049228"
---
# <a name="setdnsserversearchorder-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="90756-103">Metodo SetDNSServerSearchOrder della \_ classe NetworkAdapterConfiguration Win32</span><span class="sxs-lookup"><span data-stu-id="90756-103">SetDNSServerSearchOrder method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="90756-104">Il metodo della [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetDNSServerSearchOrder** utilizza una matrice di elementi stringa per impostare l'ordine di ricerca del server.</span><span class="sxs-lookup"><span data-stu-id="90756-104">The **SetDNSServerSearchOrder** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method uses an array of string elements to set the server search order.</span></span>

<span data-ttu-id="90756-105">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="90756-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="90756-106">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="90756-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="90756-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="90756-107">Syntax</span></span>


```mof
uint32 SetDNSServerSearchOrder(
  [in] string DNSServerSearchOrder[]
);
```



## <a name="parameters"></a><span data-ttu-id="90756-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="90756-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90756-109">*DNSServerSearchOrder* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="90756-109">*DNSServerSearchOrder* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90756-110">Elenco di indirizzi IP del server su cui eseguire una query per i server DNS.</span><span class="sxs-lookup"><span data-stu-id="90756-110">List of server IP addresses to query for DNS servers.</span></span>

<span data-ttu-id="90756-111">Esempio: 130.215.24.1 o 157.54.164.1</span><span class="sxs-lookup"><span data-stu-id="90756-111">Example: 130.215.24.1 or 157.54.164.1</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="90756-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="90756-112">Return value</span></span>

<span data-ttu-id="90756-113">Restituisce un valore pari a 0 (zero) per un completamento corretto quando non è richiesto il riavvio, 1 (uno) per un completamento corretto quando è necessario un riavvio e un numero diverso se si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="90756-113">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="90756-114">Per ulteriori informazioni sui codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="90756-114">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="90756-115">Per i valori **HRESULT** generali, vedere [codici di errore di sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="90756-115">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="90756-116">**Operazione completata, non è necessario riavviare** il computer (0)</span><span class="sxs-lookup"><span data-stu-id="90756-116">**Successful completion, no reboot required** (0)</span></span>
</dt> <dt>

<span data-ttu-id="90756-117">**Operazione completata, riavvio richiesto** (1)</span><span class="sxs-lookup"><span data-stu-id="90756-117">**Successful completion, reboot required** (1)</span></span>
</dt> <dt>

<span data-ttu-id="90756-118">**Metodo non supportato in questa piattaforma** (64)</span><span class="sxs-lookup"><span data-stu-id="90756-118">**Method not supported on this platform** (64)</span></span>
</dt> <dt>

<span data-ttu-id="90756-119">**Errore sconosciuto** (65)</span><span class="sxs-lookup"><span data-stu-id="90756-119">**Unknown failure** (65)</span></span>
</dt> <dt>

<span data-ttu-id="90756-120">**Subnet mask non valido** (66)</span><span class="sxs-lookup"><span data-stu-id="90756-120">**Invalid subnet mask** (66)</span></span>
</dt> <dt>

<span data-ttu-id="90756-121">**Si è verificato un errore durante l'elaborazione di un'istanza restituita** (67)</span><span class="sxs-lookup"><span data-stu-id="90756-121">**An error occurred while processing an Instance that was returned** (67)</span></span>
</dt> <dt>

<span data-ttu-id="90756-122">**Parametro di input non valido** (68)</span><span class="sxs-lookup"><span data-stu-id="90756-122">**Invalid input parameter** (68)</span></span>
</dt> <dt>

<span data-ttu-id="90756-123">Sono stati **specificati più di 5 gateway** (69)</span><span class="sxs-lookup"><span data-stu-id="90756-123">**More than 5 gateways specified** (69)</span></span>
</dt> <dt>

<span data-ttu-id="90756-124">**Indirizzo IP non valido** (70)</span><span class="sxs-lookup"><span data-stu-id="90756-124">**Invalid IP address** (70)</span></span>
</dt> <dt>

<span data-ttu-id="90756-125">**Indirizzo IP gateway non valido** (71)</span><span class="sxs-lookup"><span data-stu-id="90756-125">**Invalid gateway IP address** (71)</span></span>
</dt> <dt>

<span data-ttu-id="90756-126">**Si è verificato un errore durante l'accesso al registro di sistema per le informazioni richieste** (72)</span><span class="sxs-lookup"><span data-stu-id="90756-126">**An error occurred while accessing the Registry for the requested information** (72)</span></span>
</dt> <dt>

<span data-ttu-id="90756-127">**Nome di dominio non valido** (73)</span><span class="sxs-lookup"><span data-stu-id="90756-127">**Invalid domain name** (73)</span></span>
</dt> <dt>

<span data-ttu-id="90756-128">**Nome host non valido** (74)</span><span class="sxs-lookup"><span data-stu-id="90756-128">**Invalid host name** (74)</span></span>
</dt> <dt>

<span data-ttu-id="90756-129">**Nessun server WINS primario/secondario definito** (75)</span><span class="sxs-lookup"><span data-stu-id="90756-129">**No primary/secondary WINS server defined** (75)</span></span>
</dt> <dt>

<span data-ttu-id="90756-130">**File non valido** (76)</span><span class="sxs-lookup"><span data-stu-id="90756-130">**Invalid file** (76)</span></span>
</dt> <dt>

<span data-ttu-id="90756-131">**Percorso di sistema non valido** (77)</span><span class="sxs-lookup"><span data-stu-id="90756-131">**Invalid system path** (77)</span></span>
</dt> <dt>

<span data-ttu-id="90756-132">**Copia del file non riuscita** (78)</span><span class="sxs-lookup"><span data-stu-id="90756-132">**File copy failed** (78)</span></span>
</dt> <dt>

<span data-ttu-id="90756-133">**Parametro di sicurezza non valido** (79)</span><span class="sxs-lookup"><span data-stu-id="90756-133">**Invalid security parameter** (79)</span></span>
</dt> <dt>

<span data-ttu-id="90756-134">**Impossibile configurare il servizio TCP/IP** (80)</span><span class="sxs-lookup"><span data-stu-id="90756-134">**Unable to configure TCP/IP service** (80)</span></span>
</dt> <dt>

<span data-ttu-id="90756-135">**Impossibile configurare il servizio DHCP** (81)</span><span class="sxs-lookup"><span data-stu-id="90756-135">**Unable to configure DHCP service** (81)</span></span>
</dt> <dt>

<span data-ttu-id="90756-136">**Non è possibile rinnovare il lease DHCP** (82)</span><span class="sxs-lookup"><span data-stu-id="90756-136">**Unable to renew DHCP lease** (82)</span></span>
</dt> <dt>

<span data-ttu-id="90756-137">**Impossibile rilasciare il lease DHCP** (83)</span><span class="sxs-lookup"><span data-stu-id="90756-137">**Unable to release DHCP lease** (83)</span></span>
</dt> <dt>

<span data-ttu-id="90756-138">**IP non abilitato sulla scheda** (84)</span><span class="sxs-lookup"><span data-stu-id="90756-138">**IP not enabled on adapter** (84)</span></span>
</dt> <dt>

<span data-ttu-id="90756-139">**IPX non abilitato sulla scheda** (85)</span><span class="sxs-lookup"><span data-stu-id="90756-139">**IPX not enabled on adapter** (85)</span></span>
</dt> <dt>

<span data-ttu-id="90756-140">**Errore limite numero frame/rete** (86)</span><span class="sxs-lookup"><span data-stu-id="90756-140">**Frame/network number bounds error** (86)</span></span>
</dt> <dt>

<span data-ttu-id="90756-141">**Tipo di frame non valido** (87)</span><span class="sxs-lookup"><span data-stu-id="90756-141">**Invalid frame type** (87)</span></span>
</dt> <dt>

<span data-ttu-id="90756-142">**Numero di rete non valido** (88)</span><span class="sxs-lookup"><span data-stu-id="90756-142">**Invalid network number** (88)</span></span>
</dt> <dt>

<span data-ttu-id="90756-143">**Numero di rete duplicato** (89)</span><span class="sxs-lookup"><span data-stu-id="90756-143">**Duplicate network number** (89)</span></span>
</dt> <dt>

<span data-ttu-id="90756-144">**Parametro fuori limite** (90)</span><span class="sxs-lookup"><span data-stu-id="90756-144">**Parameter out of bounds** (90)</span></span>
</dt> <dt>

<span data-ttu-id="90756-145">**Accesso negato** (91)</span><span class="sxs-lookup"><span data-stu-id="90756-145">**Access denied** (91)</span></span>
</dt> <dt>

<span data-ttu-id="90756-146">**Memoria insufficiente** (92)</span><span class="sxs-lookup"><span data-stu-id="90756-146">**Out of memory** (92)</span></span>
</dt> <dt>

<span data-ttu-id="90756-147">**Già esistente** (93)</span><span class="sxs-lookup"><span data-stu-id="90756-147">**Already exists** (93)</span></span>
</dt> <dt>

<span data-ttu-id="90756-148">**Percorso, file o oggetto non trovato** (94)</span><span class="sxs-lookup"><span data-stu-id="90756-148">**Path, file or object not found** (94)</span></span>
</dt> <dt>

<span data-ttu-id="90756-149">**Non è possibile inviare una notifica al servizio** (95)</span><span class="sxs-lookup"><span data-stu-id="90756-149">**Unable to notify service** (95)</span></span>
</dt> <dt>

<span data-ttu-id="90756-150">**Impossibile inviare una notifica al servizio DNS** (96)</span><span class="sxs-lookup"><span data-stu-id="90756-150">**Unable to notify DNS service** (96)</span></span>
</dt> <dt>

<span data-ttu-id="90756-151">**Interfaccia non configurabile** (97)</span><span class="sxs-lookup"><span data-stu-id="90756-151">**Interface not configurable** (97)</span></span>
</dt> <dt>

<span data-ttu-id="90756-152">**Non tutti i lease DHCP possono essere rilasciati/rinnovati** (98)</span><span class="sxs-lookup"><span data-stu-id="90756-152">**Not all DHCP leases could be released/renewed** (98)</span></span>
</dt> <dt>

<span data-ttu-id="90756-153">**DHCP non abilitato sulla scheda** (100)</span><span class="sxs-lookup"><span data-stu-id="90756-153">**DHCP not enabled on adapter** (100)</span></span>
</dt> <dt>

<span data-ttu-id="90756-154">**Altro** (101 4294967295)</span><span class="sxs-lookup"><span data-stu-id="90756-154">**Other** (101 4294967295)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="90756-155">Commenti</span><span class="sxs-lookup"><span data-stu-id="90756-155">Remarks</span></span>

<span data-ttu-id="90756-156">Si tratta di una chiamata al metodo dipendente dall'istanza che viene applicata a ogni adapter.</span><span class="sxs-lookup"><span data-stu-id="90756-156">This is an instance-dependent method call that applies on a per-adapter basis.</span></span> <span data-ttu-id="90756-157">Dopo aver specificato i server DNS statici per iniziare a usare Dynamic Host Configuration Protocol (DHCP) invece dei server DNS statici, è possibile chiamare il metodo senza specificare i parametri "in".</span><span class="sxs-lookup"><span data-stu-id="90756-157">After static DNS servers are specified to start using Dynamic Host Configuration Protocol (DHCP) instead of static DNS servers, you can call the method without supplying "in" parameters.</span></span>

## <a name="examples"></a><span data-ttu-id="90756-158">Esempio</span><span class="sxs-lookup"><span data-stu-id="90756-158">Examples</span></span>

<span data-ttu-id="90756-159">L' [impostazione dell'ordine di ricerca del server DNS per più computer in un esempio di unità organizzativa](https://Gallery.TechNet.Microsoft.Com/Set-DNS-Server-Search-6a3e3ede) VBScript nella raccolta TechNet Recupera o imposta l'ordine di ricerca dei server DNS per più computer che appartengono a un'unità organizzativa.</span><span class="sxs-lookup"><span data-stu-id="90756-159">The [Set DNS Server Search Order for Multiple Computers in an Organizational Unit](https://Gallery.TechNet.Microsoft.Com/Set-DNS-Server-Search-6a3e3ede) VBScript sample on TechNet Gallery retrieves or sets DNS Server search order for multiple computers that belongs to one organizational unit.</span></span>

<span data-ttu-id="90756-160">L'esempio [modificare l'ordine di ricerca del server DNS per una scheda di rete](https://Gallery.TechNet.Microsoft.Com/7824348c-5a92-42cb-b4e9-ef2187702e02) consente di configurare una scheda di rete associata a TCP/IP per l'utilizzo di due server DNS.</span><span class="sxs-lookup"><span data-stu-id="90756-160">The [Modify the DNS Server Search Order for a Network Adapter](https://Gallery.TechNet.Microsoft.Com/7824348c-5a92-42cb-b4e9-ef2187702e02) VBScript sample configures a TCP/IP-bound network adapter to use two DNS servers.</span></span>

## <a name="requirements"></a><span data-ttu-id="90756-161">Requisiti</span><span class="sxs-lookup"><span data-stu-id="90756-161">Requirements</span></span>



| <span data-ttu-id="90756-162">Requisito</span><span class="sxs-lookup"><span data-stu-id="90756-162">Requirement</span></span> | <span data-ttu-id="90756-163">Valore</span><span class="sxs-lookup"><span data-stu-id="90756-163">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="90756-164">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="90756-164">Minimum supported client</span></span><br/> | <span data-ttu-id="90756-165">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="90756-165">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="90756-166">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="90756-166">Minimum supported server</span></span><br/> | <span data-ttu-id="90756-167">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="90756-167">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="90756-168">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="90756-168">Namespace</span></span><br/>                | <span data-ttu-id="90756-169">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="90756-169">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="90756-170">MOF</span><span class="sxs-lookup"><span data-stu-id="90756-170">MOF</span></span><br/>                      | <dl> <span data-ttu-id="90756-171"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="90756-171"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="90756-172">DLL</span><span class="sxs-lookup"><span data-stu-id="90756-172">DLL</span></span><br/>                      | <dl> <span data-ttu-id="90756-173"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="90756-173"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="90756-174">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="90756-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90756-175">Classi hardware del sistema del computer</span><span class="sxs-lookup"><span data-stu-id="90756-175">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="90756-176">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="90756-176">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="90756-177">Attività WMI: rete</span><span class="sxs-lookup"><span data-stu-id="90756-177">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="90756-178">Attività WMI: account e domini</span><span class="sxs-lookup"><span data-stu-id="90756-178">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="90756-179">Supporto di IPv6 e IPv4 in WMI</span><span class="sxs-lookup"><span data-stu-id="90756-179">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

