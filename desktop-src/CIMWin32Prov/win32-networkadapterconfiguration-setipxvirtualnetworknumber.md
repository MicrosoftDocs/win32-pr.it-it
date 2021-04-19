---
description: Imposta il numero di rete virtuale IPX (Internetworking Packet Exchange) nel computer di destinazione.
ms.assetid: 52064250-b94f-4dc0-bf1a-8601cd135a90
ms.tgt_platform: multiple
title: Metodo SetIPXVirtualNetworkNumber della classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetIPXVirtualNetworkNumber
api_type:
- COM
api_location:
- cimwin32.dll
ms.openlocfilehash: ed6e6802a17ef6ec4393d2ae0c5ec43f0e21d247
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305166"
---
# <a name="setipxvirtualnetworknumber-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="df474-103">Metodo SetIPXVirtualNetworkNumber della \_ classe NetworkAdapterConfiguration Win32</span><span class="sxs-lookup"><span data-stu-id="df474-103">SetIPXVirtualNetworkNumber method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="df474-104">Imposta il numero di rete virtuale IPX (Internetworking Packet Exchange) nel computer di destinazione.</span><span class="sxs-lookup"><span data-stu-id="df474-104">Sets the Internetworking Packet Exchange (IPX) virtual network number on the target computer system.</span></span> <span data-ttu-id="df474-105">Windows 2000 e Windows NT 3,51 o versione successiva utilizzano un numero di rete interno per il routing interno.</span><span class="sxs-lookup"><span data-stu-id="df474-105">Windows 2000 and Windows NT 3.51 or greater uses an internal network number for internal routing.</span></span> <span data-ttu-id="df474-106">Il numero di rete interno è noto anche come numero di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="df474-106">The internal network number is also known as a virtual network number.</span></span> <span data-ttu-id="df474-107">Identifica in modo univoco il sistema computer della rete.</span><span class="sxs-lookup"><span data-stu-id="df474-107">It uniquely identifies the computer system on the network.</span></span> <span data-ttu-id="df474-108">Il metodo restituisce un valore intero che può essere interpretted come segue:</span><span class="sxs-lookup"><span data-stu-id="df474-108">The method returns an integer value that can be interpretted as follows:</span></span>

## <a name="syntax"></a><span data-ttu-id="df474-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="df474-109">Syntax</span></span>


```mof
uint32 SetIPXVirtualNetworkNumber(
  [in] string IPXVirtualNetNumber
);
```



## <a name="parameters"></a><span data-ttu-id="df474-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="df474-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df474-111">*IPXVirtualNetNumber* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="df474-111">*IPXVirtualNetNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df474-112">Numero di rete virtuale per il sistema.</span><span class="sxs-lookup"><span data-stu-id="df474-112">The virtual network number for this system.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df474-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="df474-113">Return value</span></span>

<dl> <dt>

<span data-ttu-id="df474-114">**Operazione completata, non è necessario riavviare** il computer (0)</span><span class="sxs-lookup"><span data-stu-id="df474-114">**Successful completion, no reboot required** (0)</span></span>
</dt> <dt>

<span data-ttu-id="df474-115">**Operazione completata, riavvio richiesto** (1)</span><span class="sxs-lookup"><span data-stu-id="df474-115">**Successful completion, reboot required** (1)</span></span>
</dt> <dt>

<span data-ttu-id="df474-116">**Metodo non supportato in questa piattaforma** (64)</span><span class="sxs-lookup"><span data-stu-id="df474-116">**Method not supported on this platform** (64)</span></span>
</dt> <dt>

<span data-ttu-id="df474-117">**Errore sconosciuto** (65)</span><span class="sxs-lookup"><span data-stu-id="df474-117">**Unknown failure** (65)</span></span>
</dt> <dt>

<span data-ttu-id="df474-118">**Subnet mask non valido** (66)</span><span class="sxs-lookup"><span data-stu-id="df474-118">**Invalid subnet mask** (66)</span></span>
</dt> <dt>

<span data-ttu-id="df474-119">**Si è verificato un errore durante l'elaborazione di un'istanza restituita** (67)</span><span class="sxs-lookup"><span data-stu-id="df474-119">**An error occurred while processing an Instance that was returned** (67)</span></span>
</dt> <dt>

<span data-ttu-id="df474-120">**Parametro di input non valido** (68)</span><span class="sxs-lookup"><span data-stu-id="df474-120">**Invalid input parameter** (68)</span></span>
</dt> <dt>

<span data-ttu-id="df474-121">Sono stati **specificati più di 5 gateway** (69)</span><span class="sxs-lookup"><span data-stu-id="df474-121">**More than 5 gateways specified** (69)</span></span>
</dt> <dt>

<span data-ttu-id="df474-122">**Indirizzo IP non valido** (70)</span><span class="sxs-lookup"><span data-stu-id="df474-122">**Invalid IP address** (70)</span></span>
</dt> <dt>

<span data-ttu-id="df474-123">**Indirizzo IP gateway non valido** (71)</span><span class="sxs-lookup"><span data-stu-id="df474-123">**Invalid gateway IP address** (71)</span></span>
</dt> <dt>

<span data-ttu-id="df474-124">**Si è verificato un errore durante l'accesso al registro di sistema per le informazioni richieste** (72)</span><span class="sxs-lookup"><span data-stu-id="df474-124">**An error occurred while accessing the Registry for the requested information** (72)</span></span>
</dt> <dt>

<span data-ttu-id="df474-125">**Nome di dominio non valido** (73)</span><span class="sxs-lookup"><span data-stu-id="df474-125">**Invalid domain name** (73)</span></span>
</dt> <dt>

<span data-ttu-id="df474-126">**Nome host non valido** (74)</span><span class="sxs-lookup"><span data-stu-id="df474-126">**Invalid host name** (74)</span></span>
</dt> <dt>

<span data-ttu-id="df474-127">**Nessun server WINS primario/secondario definito** (75)</span><span class="sxs-lookup"><span data-stu-id="df474-127">**No primary/secondary WINS server defined** (75)</span></span>
</dt> <dt>

<span data-ttu-id="df474-128">**File non valido** (76)</span><span class="sxs-lookup"><span data-stu-id="df474-128">**Invalid file** (76)</span></span>
</dt> <dt>

<span data-ttu-id="df474-129">**Percorso di sistema non valido** (77)</span><span class="sxs-lookup"><span data-stu-id="df474-129">**Invalid system path** (77)</span></span>
</dt> <dt>

<span data-ttu-id="df474-130">**Copia del file non riuscita** (78)</span><span class="sxs-lookup"><span data-stu-id="df474-130">**File copy failed** (78)</span></span>
</dt> <dt>

<span data-ttu-id="df474-131">**Parametro di sicurezza non valido** (79)</span><span class="sxs-lookup"><span data-stu-id="df474-131">**Invalid security parameter** (79)</span></span>
</dt> <dt>

<span data-ttu-id="df474-132">**Impossibile configurare il servizio TCP/IP** (80)</span><span class="sxs-lookup"><span data-stu-id="df474-132">**Unable to configure TCP/IP service** (80)</span></span>
</dt> <dt>

<span data-ttu-id="df474-133">**Impossibile configurare il servizio DHCP** (81)</span><span class="sxs-lookup"><span data-stu-id="df474-133">**Unable to configure DHCP service** (81)</span></span>
</dt> <dt>

<span data-ttu-id="df474-134">**Non è possibile rinnovare il lease DHCP** (82)</span><span class="sxs-lookup"><span data-stu-id="df474-134">**Unable to renew DHCP lease** (82)</span></span>
</dt> <dt>

<span data-ttu-id="df474-135">**Impossibile rilasciare il lease DHCP** (83)</span><span class="sxs-lookup"><span data-stu-id="df474-135">**Unable to release DHCP lease** (83)</span></span>
</dt> <dt>

<span data-ttu-id="df474-136">**IP non abilitato sulla scheda** (84)</span><span class="sxs-lookup"><span data-stu-id="df474-136">**IP not enabled on adapter** (84)</span></span>
</dt> <dt>

<span data-ttu-id="df474-137">**IPX non abilitato sulla scheda** (85)</span><span class="sxs-lookup"><span data-stu-id="df474-137">**IPX not enabled on adapter** (85)</span></span>
</dt> <dt>

<span data-ttu-id="df474-138">**Errore limite numero frame/rete** (86)</span><span class="sxs-lookup"><span data-stu-id="df474-138">**Frame/network number bounds error** (86)</span></span>
</dt> <dt>

<span data-ttu-id="df474-139">**Tipo di frame non valido** (87)</span><span class="sxs-lookup"><span data-stu-id="df474-139">**Invalid frame type** (87)</span></span>
</dt> <dt>

<span data-ttu-id="df474-140">**Numero di rete non valido** (88)</span><span class="sxs-lookup"><span data-stu-id="df474-140">**Invalid network number** (88)</span></span>
</dt> <dt>

<span data-ttu-id="df474-141">**Numero di rete duplicato** (89)</span><span class="sxs-lookup"><span data-stu-id="df474-141">**Duplicate network number** (89)</span></span>
</dt> <dt>

<span data-ttu-id="df474-142">**Parametro fuori limite** (90)</span><span class="sxs-lookup"><span data-stu-id="df474-142">**Parameter out of bounds** (90)</span></span>
</dt> <dt>

<span data-ttu-id="df474-143">**Accesso negato** (91)</span><span class="sxs-lookup"><span data-stu-id="df474-143">**Access denied** (91)</span></span>
</dt> <dt>

<span data-ttu-id="df474-144">**Memoria insufficiente** (92)</span><span class="sxs-lookup"><span data-stu-id="df474-144">**Out of memory** (92)</span></span>
</dt> <dt>

<span data-ttu-id="df474-145">**Già esistente** (93)</span><span class="sxs-lookup"><span data-stu-id="df474-145">**Already exists** (93)</span></span>
</dt> <dt>

<span data-ttu-id="df474-146">**Percorso, file o oggetto non trovato** (94)</span><span class="sxs-lookup"><span data-stu-id="df474-146">**Path, file or object not found** (94)</span></span>
</dt> <dt>

<span data-ttu-id="df474-147">**Non è possibile inviare una notifica al servizio** (95)</span><span class="sxs-lookup"><span data-stu-id="df474-147">**Unable to notify service** (95)</span></span>
</dt> <dt>

<span data-ttu-id="df474-148">**Impossibile inviare una notifica al servizio DNS** (96)</span><span class="sxs-lookup"><span data-stu-id="df474-148">**Unable to notify DNS service** (96)</span></span>
</dt> <dt>

<span data-ttu-id="df474-149">**Interfaccia non configurabile** (97)</span><span class="sxs-lookup"><span data-stu-id="df474-149">**Interface not configurable** (97)</span></span>
</dt> <dt>

<span data-ttu-id="df474-150">**Non tutti i lease DHCP possono essere rilasciati/rinnovati** (98)</span><span class="sxs-lookup"><span data-stu-id="df474-150">**Not all DHCP leases could be released/renewed** (98)</span></span>
</dt> <dt>

<span data-ttu-id="df474-151">**DHCP non abilitato sulla scheda** (100)</span><span class="sxs-lookup"><span data-stu-id="df474-151">**DHCP not enabled on adapter** (100)</span></span>
</dt> <dt>

<span data-ttu-id="df474-152">**Altro** (101-4294967295)</span><span class="sxs-lookup"><span data-stu-id="df474-152">**Other** (101–4294967295)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="df474-153">Requisiti</span><span class="sxs-lookup"><span data-stu-id="df474-153">Requirements</span></span>



| <span data-ttu-id="df474-154">Requisito</span><span class="sxs-lookup"><span data-stu-id="df474-154">Requirement</span></span> | <span data-ttu-id="df474-155">Valore</span><span class="sxs-lookup"><span data-stu-id="df474-155">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="df474-156">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="df474-156">Minimum supported client</span></span><br/> | <span data-ttu-id="df474-157">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="df474-157">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="df474-158">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="df474-158">Minimum supported server</span></span><br/> | <span data-ttu-id="df474-159">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="df474-159">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="df474-160">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="df474-160">Namespace</span></span><br/>                | <span data-ttu-id="df474-161">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="df474-161">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="df474-162">MOF</span><span class="sxs-lookup"><span data-stu-id="df474-162">MOF</span></span><br/>                      | <dl> <span data-ttu-id="df474-163"><dt>CimWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="df474-163"><dt>CimWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="df474-164">DLL</span><span class="sxs-lookup"><span data-stu-id="df474-164">DLL</span></span><br/>                      | <dl> <span data-ttu-id="df474-165"><dt>Cimwin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="df474-165"><dt>Cimwin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df474-166">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="df474-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df474-167">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="df474-167">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> </dl>

 

 




