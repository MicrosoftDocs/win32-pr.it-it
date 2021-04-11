---
description: Imposta le coppie di frame/numero di rete IPX (Internetworking Packet Exchange) per questa scheda di rete.
ms.assetid: 8190564f-7d9f-4b05-9949-2e732ce36dba
ms.tgt_platform: multiple
title: Metodo SetIPXFrameTypeNetworkPairs della classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetIPXFrameTypeNetworkPairs
api_type:
- COM
api_location:
- cimwin32.dll
ms.openlocfilehash: e4d53ec7b5600a767505e517a02fbf87b5a43d13
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127471"
---
# <a name="setipxframetypenetworkpairs-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="1e6f7-103">Metodo SetIPXFrameTypeNetworkPairs della \_ classe NetworkAdapterConfiguration Win32</span><span class="sxs-lookup"><span data-stu-id="1e6f7-103">SetIPXFrameTypeNetworkPairs method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="1e6f7-104">Imposta le coppie di frame/numero di rete IPX (Internetworking Packet Exchange) per questa scheda di rete.</span><span class="sxs-lookup"><span data-stu-id="1e6f7-104">Sets the Internetworking Packet Exchange (IPX) network number/frame pairs for this network adapter.</span></span>

<span data-ttu-id="1e6f7-105">Windows 2000 e Windows NT 3,51 e versioni successive utilizzano un numero di rete IPX a scopo di routing.</span><span class="sxs-lookup"><span data-stu-id="1e6f7-105">Windows 2000 and Windows NT 3.51 and higher use an IPX network number for routing purposes.</span></span> <span data-ttu-id="1e6f7-106">Viene assegnato a ogni combinazione di tipo di frame/scheda di rete configurata nel sistema del computer.</span><span class="sxs-lookup"><span data-stu-id="1e6f7-106">It is assigned to each configured frame type/network adapter combination on your computer system.</span></span> <span data-ttu-id="1e6f7-107">Questo numero viene talvolta definito "numero di rete esterna".</span><span class="sxs-lookup"><span data-stu-id="1e6f7-107">This number is sometimes referred to as the "external network number."</span></span> <span data-ttu-id="1e6f7-108">Deve essere univoco per ogni segmento di rete.</span><span class="sxs-lookup"><span data-stu-id="1e6f7-108">It must be unique for each network segment.</span></span> <span data-ttu-id="1e6f7-109">Se il tipo di frame è impostato su automatico, il numero di rete deve essere pari a zero.</span><span class="sxs-lookup"><span data-stu-id="1e6f7-109">If the frame type is set to AUTO, the network number should to zero.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e6f7-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1e6f7-110">Syntax</span></span>


```mof
uint32 SetIPXFrameTypeNetworkPairs(
  [in] string IPXNetworkNumber[],
  [in] uint32 IPXFrameType[]
);
```



## <a name="parameters"></a><span data-ttu-id="1e6f7-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="1e6f7-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e6f7-112">*IPXNetworkNumber* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1e6f7-112">*IPXNetworkNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e6f7-113">Matrice di caratteri che identifica in modo univoco un adapter nel computer.</span><span class="sxs-lookup"><span data-stu-id="1e6f7-113">An array of characters that uniquely identify an adapter on the computer system.</span></span> <span data-ttu-id="1e6f7-114">Il trasporto con connessione NetWare (NWLink) compatibile con IPX/SPX in Windows 2000 e Windows NT 3,51 o versione successiva usa due tipi diversi di numeri di rete.</span><span class="sxs-lookup"><span data-stu-id="1e6f7-114">The NetWare Link (NWLink) IPX/SPX-compatible transport in Windows 2000 and Windows NT 3.51 or higher, uses two different types of network numbers.</span></span> <span data-ttu-id="1e6f7-115">Questo numero viene talvolta definito numero di rete esterna.</span><span class="sxs-lookup"><span data-stu-id="1e6f7-115">This number is sometimes referred to as the External Network Number.</span></span> <span data-ttu-id="1e6f7-116">Deve essere univoco per ogni segmento di rete.</span><span class="sxs-lookup"><span data-stu-id="1e6f7-116">It must be unique for each network segment.</span></span> <span data-ttu-id="1e6f7-117">I valori in questo elenco di stringhe devono avere un valore corrispondente nel parametro IPXFrameType che identifica il tipo di frame del pacchetto usato per la rete.</span><span class="sxs-lookup"><span data-stu-id="1e6f7-117">The values in this string list must have a corresponding value in the IPXFrameType parameter identifying the packet frame type used for this network.</span></span>

</dd> <dt>

<span data-ttu-id="1e6f7-118">*IPXFrameType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1e6f7-118">*IPXFrameType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e6f7-119">Matrice di Integer di identificatori del tipo di frame.</span><span class="sxs-lookup"><span data-stu-id="1e6f7-119">An integer array of frame type identifiers.</span></span> <span data-ttu-id="1e6f7-120">I valori in questa matrice corrispondono agli elementi nel parametro *IPXNetworkNumber* .</span><span class="sxs-lookup"><span data-stu-id="1e6f7-120">The values in this array correspond to the elements in the *IPXNetworkNumber* parameter.</span></span>

<dt>

<span id="Ethernet_II"></span><span id="ethernet_ii"></span><span id="ETHERNET_II"></span>

<span data-ttu-id="1e6f7-121">**Ethernet II** (0)</span><span class="sxs-lookup"><span data-stu-id="1e6f7-121">**Ethernet II** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_802.3"></span><span id="ethernet_802.3"></span><span id="ETHERNET_802.3"></span>

<span data-ttu-id="1e6f7-122">**Ethernet 802,3** (1)</span><span class="sxs-lookup"><span data-stu-id="1e6f7-122">**Ethernet 802.3** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_802.2"></span><span id="ethernet_802.2"></span><span id="ETHERNET_802.2"></span>

<span data-ttu-id="1e6f7-123">**Ethernet 802,2** (2)</span><span class="sxs-lookup"><span data-stu-id="1e6f7-123">**Ethernet 802.2** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_SNAP"></span><span id="ethernet_snap"></span><span id="ETHERNET_SNAP"></span>

<span data-ttu-id="1e6f7-124">**Snap** -in Ethernet (3)</span><span class="sxs-lookup"><span data-stu-id="1e6f7-124">**Ethernet SNAP** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="AUTO"></span><span id="auto"></span>

<span data-ttu-id="1e6f7-125">**Automatico** (255)</span><span class="sxs-lookup"><span data-stu-id="1e6f7-125">**AUTO** (255)</span></span>


<span data-ttu-id="1e6f7-126"></dt> <dd></dd> </dl> </dd> </dl></span><span class="sxs-lookup"><span data-stu-id="1e6f7-126"></dt> <dd></dd> </dl> </dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="1e6f7-127">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1e6f7-127">Return value</span></span>

<dl> <dt>

<span data-ttu-id="1e6f7-128">**Operazione completata, non è necessario riavviare** il computer (0)</span><span class="sxs-lookup"><span data-stu-id="1e6f7-128">**Successful completion, no reboot required** (0)</span></span>
</dt> <dt>

<span data-ttu-id="1e6f7-129">**Operazione completata, riavvio richiesto** (1)</span><span class="sxs-lookup"><span data-stu-id="1e6f7-129">**Successful completion, reboot required** (1)</span></span>
</dt> <dt>

<span data-ttu-id="1e6f7-130">**Metodo non supportato in questa piattaforma** (64)</span><span class="sxs-lookup"><span data-stu-id="1e6f7-130">**Method not supported on this platform** (64)</span></span>
</dt> <dt>

<span data-ttu-id="1e6f7-131">**Errore sconosciuto** (65)</span><span class="sxs-lookup"><span data-stu-id="1e6f7-131">**Unknown failure** (65)</span></span>
</dt> <dt>

<span data-ttu-id="1e6f7-132">**Subnet mask non valido** (66)</span><span class="sxs-lookup"><span data-stu-id="1e6f7-132">**Invalid subnet mask** (66)</span></span>
</dt> <dt>

<span data-ttu-id="1e6f7-133">**Si è verificato un errore durante l'elaborazione di un'istanza restituita** (67)</span><span class="sxs-lookup"><span data-stu-id="1e6f7-133">**An error occurred while processing an Instance that was returned** (67)</span></span>
</dt> <dt>

<span data-ttu-id="1e6f7-134">**Parametro di input non valido** (68)</span><span class="sxs-lookup"><span data-stu-id="1e6f7-134">**Invalid input parameter** (68)</span></span>
</dt> <dt>

<span data-ttu-id="1e6f7-135">Sono stati **specificati più di 5 gateway** (69)</span><span class="sxs-lookup"><span data-stu-id="1e6f7-135">**More than 5 gateways specified** (69)</span></span>
</dt> <dt>

<span data-ttu-id="1e6f7-136">**Indirizzo IP non valido** (70)</span><span class="sxs-lookup"><span data-stu-id="1e6f7-136">**Invalid IP address** (70)</span></span>
</dt> <dt>

<span data-ttu-id="1e6f7-137">**Indirizzo IP gateway non valido** (71)</span><span class="sxs-lookup"><span data-stu-id="1e6f7-137">**Invalid gateway IP address** (71)</span></span>
</dt> <dt>

<span data-ttu-id="1e6f7-138">**Si è verificato un errore durante l'accesso al registro di sistema per le informazioni richieste** (72)</span><span class="sxs-lookup"><span data-stu-id="1e6f7-138">**An error occurred while accessing the Registry for the requested information** (72)</span></span>
</dt> <dt>

<span data-ttu-id="1e6f7-139">**Nome di dominio non valido** (73)</span><span class="sxs-lookup"><span data-stu-id="1e6f7-139">**Invalid domain name** (73)</span></span>
</dt> <dt>

<span data-ttu-id="1e6f7-140">**Nome host non valido** (74)</span><span class="sxs-lookup"><span data-stu-id="1e6f7-140">**Invalid host name** (74)</span></span>
</dt> <dt>

<span data-ttu-id="1e6f7-141">**Nessun server WINS primario/secondario definito** (75)</span><span class="sxs-lookup"><span data-stu-id="1e6f7-141">**No primary/secondary WINS server defined** (75)</span></span>
</dt> <dt>

<span data-ttu-id="1e6f7-142">**File non valido** (76)</span><span class="sxs-lookup"><span data-stu-id="1e6f7-142">**Invalid file** (76)</span></span>
</dt> <dt>

<span data-ttu-id="1e6f7-143">**Percorso di sistema non valido** (77)</span><span class="sxs-lookup"><span data-stu-id="1e6f7-143">**Invalid system path** (77)</span></span>
</dt> <dt>

<span data-ttu-id="1e6f7-144">**Copia del file non riuscita** (78)</span><span class="sxs-lookup"><span data-stu-id="1e6f7-144">**File copy failed** (78)</span></span>
</dt> <dt>

<span data-ttu-id="1e6f7-145">**Parametro di sicurezza non valido** (79)</span><span class="sxs-lookup"><span data-stu-id="1e6f7-145">**Invalid security parameter** (79)</span></span>
</dt> <dt>

<span data-ttu-id="1e6f7-146">**Impossibile configurare il servizio TCP/IP** (80)</span><span class="sxs-lookup"><span data-stu-id="1e6f7-146">**Unable to configure TCP/IP service** (80)</span></span>
</dt> <dt>

<span data-ttu-id="1e6f7-147">**Impossibile configurare il servizio DHCP** (81)</span><span class="sxs-lookup"><span data-stu-id="1e6f7-147">**Unable to configure DHCP service** (81)</span></span>
</dt> <dt>

<span data-ttu-id="1e6f7-148">**Non è possibile rinnovare il lease DHCP** (82)</span><span class="sxs-lookup"><span data-stu-id="1e6f7-148">**Unable to renew DHCP lease** (82)</span></span>
</dt> <dt>

<span data-ttu-id="1e6f7-149">**Impossibile rilasciare il lease DHCP** (83)</span><span class="sxs-lookup"><span data-stu-id="1e6f7-149">**Unable to release DHCP lease** (83)</span></span>
</dt> <dt>

<span data-ttu-id="1e6f7-150">**IP non abilitato sulla scheda** (84)</span><span class="sxs-lookup"><span data-stu-id="1e6f7-150">**IP not enabled on adapter** (84)</span></span>
</dt> <dt>

<span data-ttu-id="1e6f7-151">**IPX non abilitato sulla scheda** (85)</span><span class="sxs-lookup"><span data-stu-id="1e6f7-151">**IPX not enabled on adapter** (85)</span></span>
</dt> <dt>

<span data-ttu-id="1e6f7-152">**Errore limite numero frame/rete** (86)</span><span class="sxs-lookup"><span data-stu-id="1e6f7-152">**Frame/network number bounds error** (86)</span></span>
</dt> <dt>

<span data-ttu-id="1e6f7-153">**Tipo di frame non valido** (87)</span><span class="sxs-lookup"><span data-stu-id="1e6f7-153">**Invalid frame type** (87)</span></span>
</dt> <dt>

<span data-ttu-id="1e6f7-154">**Numero di rete non valido** (88)</span><span class="sxs-lookup"><span data-stu-id="1e6f7-154">**Invalid network number** (88)</span></span>
</dt> <dt>

<span data-ttu-id="1e6f7-155">**Numero di rete duplicato** (89)</span><span class="sxs-lookup"><span data-stu-id="1e6f7-155">**Duplicate network number** (89)</span></span>
</dt> <dt>

<span data-ttu-id="1e6f7-156">**Parametro fuori limite** (90)</span><span class="sxs-lookup"><span data-stu-id="1e6f7-156">**Parameter out of bounds** (90)</span></span>
</dt> <dt>

<span data-ttu-id="1e6f7-157">**Accesso negato** (91)</span><span class="sxs-lookup"><span data-stu-id="1e6f7-157">**Access denied** (91)</span></span>
</dt> <dt>

<span data-ttu-id="1e6f7-158">**Memoria insufficiente** (92)</span><span class="sxs-lookup"><span data-stu-id="1e6f7-158">**Out of memory** (92)</span></span>
</dt> <dt>

<span data-ttu-id="1e6f7-159">**Già esistente** (93)</span><span class="sxs-lookup"><span data-stu-id="1e6f7-159">**Already exists** (93)</span></span>
</dt> <dt>

<span data-ttu-id="1e6f7-160">**Percorso, file o oggetto non trovato** (94)</span><span class="sxs-lookup"><span data-stu-id="1e6f7-160">**Path, file or object not found** (94)</span></span>
</dt> <dt>

<span data-ttu-id="1e6f7-161">**Non è possibile inviare una notifica al servizio** (95)</span><span class="sxs-lookup"><span data-stu-id="1e6f7-161">**Unable to notify service** (95)</span></span>
</dt> <dt>

<span data-ttu-id="1e6f7-162">**Impossibile inviare una notifica al servizio DNS** (96)</span><span class="sxs-lookup"><span data-stu-id="1e6f7-162">**Unable to notify DNS service** (96)</span></span>
</dt> <dt>

<span data-ttu-id="1e6f7-163">**Interfaccia non configurabile** (97)</span><span class="sxs-lookup"><span data-stu-id="1e6f7-163">**Interface not configurable** (97)</span></span>
</dt> <dt>

<span data-ttu-id="1e6f7-164">**Non tutti i lease DHCP possono essere rilasciati/rinnovati** (98)</span><span class="sxs-lookup"><span data-stu-id="1e6f7-164">**Not all DHCP leases could be released/renewed** (98)</span></span>
</dt> <dt>

<span data-ttu-id="1e6f7-165">**DHCP non abilitato sulla scheda** (100)</span><span class="sxs-lookup"><span data-stu-id="1e6f7-165">**DHCP not enabled on adapter** (100)</span></span>
</dt> <dt>

<span data-ttu-id="1e6f7-166">**Altro** (101-4294967295)</span><span class="sxs-lookup"><span data-stu-id="1e6f7-166">**Other** (101–4294967295)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="1e6f7-167">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1e6f7-167">Requirements</span></span>



| <span data-ttu-id="1e6f7-168">Requisito</span><span class="sxs-lookup"><span data-stu-id="1e6f7-168">Requirement</span></span> | <span data-ttu-id="1e6f7-169">Valore</span><span class="sxs-lookup"><span data-stu-id="1e6f7-169">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1e6f7-170">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1e6f7-170">Minimum supported client</span></span><br/> | <span data-ttu-id="1e6f7-171">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1e6f7-171">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1e6f7-172">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1e6f7-172">Minimum supported server</span></span><br/> | <span data-ttu-id="1e6f7-173">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1e6f7-173">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1e6f7-174">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="1e6f7-174">Namespace</span></span><br/>                | <span data-ttu-id="1e6f7-175">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="1e6f7-175">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1e6f7-176">MOF</span><span class="sxs-lookup"><span data-stu-id="1e6f7-176">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1e6f7-177"><dt>CimWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1e6f7-177"><dt>CimWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1e6f7-178">DLL</span><span class="sxs-lookup"><span data-stu-id="1e6f7-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1e6f7-179"><dt>Cimwin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1e6f7-179"><dt>Cimwin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e6f7-180">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1e6f7-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e6f7-181">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="1e6f7-181">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> </dl>

 

 




