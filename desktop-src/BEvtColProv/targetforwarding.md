---
description: Recupera i dati di invio da un computer di destinazione.
ms.assetid: e9ed210d-09ad-4689-b6a0-f84c5cce86f5
ms.tgt_platform: multiple
title: Classe TargetForwarding
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TargetForwarding
- TargetForwarding.TargetEndpoint
- TargetForwarding.TargetMac
- TargetForwarding.TargetGuid
- TargetForwarding.CollectorEndpoint
- TargetForwarding.Computer
- TargetForwarding.ForwarderType
- TargetForwarding.Destination
- TargetForwarding.DestinationPattern
- TargetForwarding.Error
- TargetForwarding.ConnectedSince
api_type:
- DllExport
api_location:
- BEvtCol.exe
ms.openlocfilehash: aba0a40ccd5611cecfe7450e518620d4d41ec1e0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104522906"
---
# <a name="targetforwarding-class"></a><span data-ttu-id="82d55-103">Classe TargetForwarding</span><span class="sxs-lookup"><span data-stu-id="82d55-103">TargetForwarding class</span></span>

<span data-ttu-id="82d55-104">Recupera i dati di invio da un computer di destinazione.</span><span class="sxs-lookup"><span data-stu-id="82d55-104">Retrieves forwarding data from a target computer.</span></span>

> [!Note]  
> <span data-ttu-id="82d55-105">In un computer di destinazione potrebbero essere configurati più server d'inoltri.</span><span class="sxs-lookup"><span data-stu-id="82d55-105">A target computer may have multiple forwarders configured.</span></span>

 

<span data-ttu-id="82d55-106">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="82d55-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="82d55-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="82d55-107">Syntax</span></span>

``` syntax
[Provider("BootEventCollectorWmiProvider"), Dynamic, AMENDMENT]
class TargetForwarding
{
  string   TargetEndpoint;
  string   TargetMac;
  string   TargetGuid;
  string   CollectorEndpoint;
  string   Computer;
  string   ForwarderType;
  string   Destination;
  string   DestinationPattern;
  string   Error;
  DATETIME ConnectedSince;
};
```

## <a name="members"></a><span data-ttu-id="82d55-108">Members</span><span class="sxs-lookup"><span data-stu-id="82d55-108">Members</span></span>

<span data-ttu-id="82d55-109">La classe **TargetForwarding** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="82d55-109">The **TargetForwarding** class has these types of members:</span></span>

-   [<span data-ttu-id="82d55-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="82d55-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="82d55-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="82d55-111">Properties</span></span>

<span data-ttu-id="82d55-112">La classe **TargetForwarding** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="82d55-112">The **TargetForwarding** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="82d55-113">**CollectorEndpoint**</span><span class="sxs-lookup"><span data-stu-id="82d55-113">**CollectorEndpoint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82d55-114">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82d55-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82d55-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="82d55-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="82d55-116">Qualificatori: [ **corretti**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="82d55-116">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="82d55-117">Informazioni sull'endpoint del server dell'agente di raccolta.</span><span class="sxs-lookup"><span data-stu-id="82d55-117">The endpoint information of the collector server.</span></span> <span data-ttu-id="82d55-118">Questa proprietà è formattata come stringa *host*:*porta* .</span><span class="sxs-lookup"><span data-stu-id="82d55-118">This property is formatted as a *host*:*port* string.</span></span>

</dd> <dt>

<span data-ttu-id="82d55-119">**Computer**</span><span class="sxs-lookup"><span data-stu-id="82d55-119">**Computer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82d55-120">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82d55-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82d55-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="82d55-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="82d55-122">Qualificatori: [ **corretti**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="82d55-122">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="82d55-123">Nome del computer di destinazione.</span><span class="sxs-lookup"><span data-stu-id="82d55-123">The computer name of the target computer.</span></span>

</dd> <dt>

<span data-ttu-id="82d55-124">**ConnectedSince**</span><span class="sxs-lookup"><span data-stu-id="82d55-124">**ConnectedSince**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82d55-125">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="82d55-125">Data type: **DATETIME**</span></span>
</dt> <dt>

<span data-ttu-id="82d55-126">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="82d55-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="82d55-127">Qualificatori: [ **corretti**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="82d55-127">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="82d55-128">Timestamp che indica quando è stata stabilita la connessione per i dati di invio.</span><span class="sxs-lookup"><span data-stu-id="82d55-128">The timestamp that indicates when the connection was established for the forwarding data.</span></span>

</dd> <dt>

<span data-ttu-id="82d55-129">**Destinazione**</span><span class="sxs-lookup"><span data-stu-id="82d55-129">**Destination**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82d55-130">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82d55-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82d55-131">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="82d55-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="82d55-132">Qualificatori: [ **corretti**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="82d55-132">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="82d55-133">Destinazione dei dati di invio, ad esempio un nome di file.</span><span class="sxs-lookup"><span data-stu-id="82d55-133">The destination of the forwarding data, such as a file name.</span></span>

</dd> <dt>

<span data-ttu-id="82d55-134">**DestinationPattern**</span><span class="sxs-lookup"><span data-stu-id="82d55-134">**DestinationPattern**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82d55-135">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82d55-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82d55-136">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="82d55-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="82d55-137">Qualificatori: [ **corretti**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="82d55-137">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="82d55-138">Formato utilizzato per generare la destinazione dei dati di invio.</span><span class="sxs-lookup"><span data-stu-id="82d55-138">The format used to generate the destination of the forwarding data.</span></span>

</dd> <dt>

<span data-ttu-id="82d55-139">**Error (Errore) (Error (Errore)e)**</span><span class="sxs-lookup"><span data-stu-id="82d55-139">**Error**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82d55-140">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82d55-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82d55-141">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="82d55-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="82d55-142">Qualificatori: [ **corretti**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="82d55-142">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="82d55-143">Messaggio di errore che descrive un errore rilevato.</span><span class="sxs-lookup"><span data-stu-id="82d55-143">An error message that describes an encountered error.</span></span> <span data-ttu-id="82d55-144">Questa proprietà è vuota se non si è verificato alcun errore.</span><span class="sxs-lookup"><span data-stu-id="82d55-144">This property is empty if no error was encountered.</span></span>

</dd> <dt>

<span data-ttu-id="82d55-145">**ForwarderType**</span><span class="sxs-lookup"><span data-stu-id="82d55-145">**ForwarderType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82d55-146">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82d55-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82d55-147">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="82d55-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="82d55-148">Qualificatori: [ **corretti**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="82d55-148">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="82d55-149">Tipo di file che contiene i dati di invio, ad esempio ETL.</span><span class="sxs-lookup"><span data-stu-id="82d55-149">The file type that contains the forwarding data, such as ETL.</span></span>

</dd> <dt>

<span data-ttu-id="82d55-150">**TargetEndpoint**</span><span class="sxs-lookup"><span data-stu-id="82d55-150">**TargetEndpoint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82d55-151">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82d55-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82d55-152">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="82d55-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="82d55-153">Qualificatori: [**chiave**](/windows/desktop/WmiSdk/key-qualifier), [**correzione**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="82d55-153">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="82d55-154">Informazioni sull'endpoint del computer di destinazione, in formato leggibile.</span><span class="sxs-lookup"><span data-stu-id="82d55-154">The endpoint information of the target computer, in human-readable format.</span></span> <span data-ttu-id="82d55-155">Questa proprietà è formattata come stringa *host*:*porta* .</span><span class="sxs-lookup"><span data-stu-id="82d55-155">This property is formatted as a *host*:*port* string.</span></span> <span data-ttu-id="82d55-156">Ad esempio, "127.0.0.1:50000".</span><span class="sxs-lookup"><span data-stu-id="82d55-156">For example, "127.0.0.1:50000".</span></span>

</dd> <dt>

<span data-ttu-id="82d55-157">**TargetGuid**</span><span class="sxs-lookup"><span data-stu-id="82d55-157">**TargetGuid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82d55-158">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82d55-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82d55-159">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="82d55-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="82d55-160">Qualificatori: [**chiave**](/windows/desktop/WmiSdk/key-qualifier), [**correzione**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="82d55-160">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="82d55-161">**GUID** SMBIOS del computer di destinazione.</span><span class="sxs-lookup"><span data-stu-id="82d55-161">The SMBIOS **GUID** of the target computer.</span></span>

</dd> <dt>

<span data-ttu-id="82d55-162">**TargetMac**</span><span class="sxs-lookup"><span data-stu-id="82d55-162">**TargetMac**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82d55-163">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="82d55-163">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82d55-164">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="82d55-164">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="82d55-165">Qualificatori: [**chiave**](/windows/desktop/WmiSdk/key-qualifier), [**correzione**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="82d55-165">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="82d55-166">Indirizzo MAC del computer di destinazione.</span><span class="sxs-lookup"><span data-stu-id="82d55-166">The MAC address of the target computer.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="82d55-167">Requisiti</span><span class="sxs-lookup"><span data-stu-id="82d55-167">Requirements</span></span>



| <span data-ttu-id="82d55-168">Requisito</span><span class="sxs-lookup"><span data-stu-id="82d55-168">Requirement</span></span> | <span data-ttu-id="82d55-169">Valore</span><span class="sxs-lookup"><span data-stu-id="82d55-169">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="82d55-170">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="82d55-170">Minimum supported client</span></span><br/> | <span data-ttu-id="82d55-171">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="82d55-171">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="82d55-172">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="82d55-172">Minimum supported server</span></span><br/> | <span data-ttu-id="82d55-173">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="82d55-173">Windows Server 2016</span></span><br/>                                                                       |
| <span data-ttu-id="82d55-174">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="82d55-174">Namespace</span></span><br/>                | <span data-ttu-id="82d55-175">Radice \\ Microsoft \\ Windows \\ BootEventCollector</span><span class="sxs-lookup"><span data-stu-id="82d55-175">Root\\Microsoft\\Windows\\BootEventCollector</span></span><br/>                                              |
| <span data-ttu-id="82d55-176">MOF</span><span class="sxs-lookup"><span data-stu-id="82d55-176">MOF</span></span><br/>                      | <dl> <span data-ttu-id="82d55-177"><dt>BootEventCollectorWMI. mof</dt></span><span class="sxs-lookup"><span data-stu-id="82d55-177"><dt>BootEventCollectorWMI.mof</dt></span></span> </dl> |
| <span data-ttu-id="82d55-178">DLL</span><span class="sxs-lookup"><span data-stu-id="82d55-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="82d55-179"><dt>BEvtCol.exe</dt></span><span class="sxs-lookup"><span data-stu-id="82d55-179"><dt>BEvtCol.exe</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="82d55-180">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="82d55-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82d55-181">Provider WMI raccolta eventi di avvio</span><span class="sxs-lookup"><span data-stu-id="82d55-181">Boot Event Collector WMI Provider</span></span>](boot-event-collector-wmi-provider-portal.md)
</dt> </dl>

 

