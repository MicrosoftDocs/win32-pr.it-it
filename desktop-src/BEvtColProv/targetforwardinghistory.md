---
description: Cronologia recente delle modifiche apportate ai dati di invio per un computer di destinazione.
ms.assetid: 621e2734-fc75-4e7a-9fae-de3d1b0272ae
ms.tgt_platform: multiple
title: Classe TargetForwardingHistory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TargetForwardingHistory
- TargetForwardingHistory.TargetEndpoint
- TargetForwardingHistory.TargetMac
- TargetForwardingHistory.TargetGuid
- TargetForwardingHistory.CollectorEndpoint
- TargetForwardingHistory.Computer
- TargetForwardingHistory.ForwarderType
- TargetForwardingHistory.Destination
- TargetForwardingHistory.DestinationPattern
- TargetForwardingHistory.Error
- TargetForwardingHistory.ConnectedSince
- TargetForwardingHistory.DisconnectedSince
- TargetForwardingHistory.WmiDateTime
api_type:
- DllExport
api_location:
- BEvtCol.exe
ms.openlocfilehash: 7fb713f98709f65de5fa32424f8a3484edaac758
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127771"
---
# <a name="targetforwardinghistory-class"></a><span data-ttu-id="7b186-103">Classe TargetForwardingHistory</span><span class="sxs-lookup"><span data-stu-id="7b186-103">TargetForwardingHistory class</span></span>

<span data-ttu-id="7b186-104">Cronologia recente delle modifiche apportate ai dati di invio per un computer di destinazione.</span><span class="sxs-lookup"><span data-stu-id="7b186-104">The recent history of changes to the forwarding data for a target computer.</span></span>

<span data-ttu-id="7b186-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="7b186-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b186-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7b186-106">Syntax</span></span>

``` syntax
[Provider("BootEventCollectorWmiProvider"), Dynamic, AMENDMENT]
class TargetForwardingHistory
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
  DATETIME DisconnectedSince;
  DATETIME WmiDateTime;
};
```

## <a name="members"></a><span data-ttu-id="7b186-107">Members</span><span class="sxs-lookup"><span data-stu-id="7b186-107">Members</span></span>

<span data-ttu-id="7b186-108">La classe **TargetForwardingHistory** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="7b186-108">The **TargetForwardingHistory** class has these types of members:</span></span>

-   [<span data-ttu-id="7b186-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="7b186-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7b186-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="7b186-110">Properties</span></span>

<span data-ttu-id="7b186-111">La classe **TargetForwardingHistory** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="7b186-111">The **TargetForwardingHistory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7b186-112">**CollectorEndpoint**</span><span class="sxs-lookup"><span data-stu-id="7b186-112">**CollectorEndpoint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b186-113">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7b186-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7b186-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7b186-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b186-115">Qualificatori: [ **corretti**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="7b186-115">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="7b186-116">Informazioni sull'endpoint del server dell'agente di raccolta.</span><span class="sxs-lookup"><span data-stu-id="7b186-116">The endpoint information of the collector server.</span></span> <span data-ttu-id="7b186-117">Questa proprietà è formattata come stringa *host*:*porta* .</span><span class="sxs-lookup"><span data-stu-id="7b186-117">This property is formatted as a *host*:*port* string.</span></span>

</dd> <dt>

<span data-ttu-id="7b186-118">**Computer**</span><span class="sxs-lookup"><span data-stu-id="7b186-118">**Computer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b186-119">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7b186-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7b186-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7b186-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b186-121">Qualificatori: [ **corretti**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="7b186-121">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="7b186-122">Nome del computer di destinazione.</span><span class="sxs-lookup"><span data-stu-id="7b186-122">The computer name of the target computer.</span></span>

</dd> <dt>

<span data-ttu-id="7b186-123">**ConnectedSince**</span><span class="sxs-lookup"><span data-stu-id="7b186-123">**ConnectedSince**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b186-124">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="7b186-124">Data type: **DATETIME**</span></span>
</dt> <dt>

<span data-ttu-id="7b186-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7b186-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b186-126">Qualificatori: [ **corretti**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="7b186-126">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="7b186-127">Timestamp che indica quando è stata stabilita la connessione per i dati di invio.</span><span class="sxs-lookup"><span data-stu-id="7b186-127">The timestamp that indicates when the connection was established for the forwarding data.</span></span>

</dd> <dt>

<span data-ttu-id="7b186-128">**Destinazione**</span><span class="sxs-lookup"><span data-stu-id="7b186-128">**Destination**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b186-129">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7b186-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7b186-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7b186-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b186-131">Qualificatori: [ **corretti**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="7b186-131">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="7b186-132">Destinazione dei dati di invio, ad esempio un nome di file.</span><span class="sxs-lookup"><span data-stu-id="7b186-132">The destination of the forwarding data, such as a file name.</span></span>

</dd> <dt>

<span data-ttu-id="7b186-133">**DestinationPattern**</span><span class="sxs-lookup"><span data-stu-id="7b186-133">**DestinationPattern**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b186-134">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7b186-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7b186-135">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7b186-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b186-136">Qualificatori: [ **corretti**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="7b186-136">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="7b186-137">Formato utilizzato per generare la destinazione dei dati di invio.</span><span class="sxs-lookup"><span data-stu-id="7b186-137">The format used to generate the destination of the forwarding data.</span></span>

</dd> <dt>

<span data-ttu-id="7b186-138">**DisconnectedSince**</span><span class="sxs-lookup"><span data-stu-id="7b186-138">**DisconnectedSince**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b186-139">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="7b186-139">Data type: **DATETIME**</span></span>
</dt> <dt>

<span data-ttu-id="7b186-140">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7b186-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b186-141">Qualificatori: [ **corretti**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="7b186-141">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="7b186-142">Timestamp che indica quando la connessione è stata disconnessa.</span><span class="sxs-lookup"><span data-stu-id="7b186-142">The timestamp that indicates when the connection was disconnected.</span></span>

</dd> <dt>

<span data-ttu-id="7b186-143">**Error (Errore) (Error (Errore)e)**</span><span class="sxs-lookup"><span data-stu-id="7b186-143">**Error**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b186-144">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7b186-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7b186-145">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7b186-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b186-146">Qualificatori: [ **corretti**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="7b186-146">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="7b186-147">Messaggio di errore che descrive un errore rilevato.</span><span class="sxs-lookup"><span data-stu-id="7b186-147">An error message that describes an encountered error.</span></span> <span data-ttu-id="7b186-148">Questa proprietà è vuota se non si è verificato alcun errore.</span><span class="sxs-lookup"><span data-stu-id="7b186-148">This property is empty if no error was encountered.</span></span>

</dd> <dt>

<span data-ttu-id="7b186-149">**ForwarderType**</span><span class="sxs-lookup"><span data-stu-id="7b186-149">**ForwarderType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b186-150">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7b186-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7b186-151">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7b186-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b186-152">Qualificatori: [ **corretti**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="7b186-152">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="7b186-153">Tipo di file che contiene i dati di invio, ad esempio ETL.</span><span class="sxs-lookup"><span data-stu-id="7b186-153">The file type that contains the forwarding data, such as ETL.</span></span>

</dd> <dt>

<span data-ttu-id="7b186-154">**TargetEndpoint**</span><span class="sxs-lookup"><span data-stu-id="7b186-154">**TargetEndpoint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b186-155">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7b186-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7b186-156">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7b186-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b186-157">Qualificatori: [**chiave**](/windows/desktop/WmiSdk/key-qualifier), [**correzione**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="7b186-157">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="7b186-158">Informazioni sull'endpoint del computer di destinazione, in formato leggibile.</span><span class="sxs-lookup"><span data-stu-id="7b186-158">The endpoint information of the target computer, in human-readable format.</span></span> <span data-ttu-id="7b186-159">Questa proprietà è formattata come stringa *host*:*porta* .</span><span class="sxs-lookup"><span data-stu-id="7b186-159">This property is formatted as a *host*:*port* string.</span></span> <span data-ttu-id="7b186-160">Ad esempio, "127.0.0.1:50000".</span><span class="sxs-lookup"><span data-stu-id="7b186-160">For example, "127.0.0.1:50000".</span></span>

</dd> <dt>

<span data-ttu-id="7b186-161">**TargetGuid**</span><span class="sxs-lookup"><span data-stu-id="7b186-161">**TargetGuid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b186-162">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7b186-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7b186-163">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7b186-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b186-164">Qualificatori: [**chiave**](/windows/desktop/WmiSdk/key-qualifier), [**correzione**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="7b186-164">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="7b186-165">**GUID** SMBIOS del computer di destinazione.</span><span class="sxs-lookup"><span data-stu-id="7b186-165">The SMBIOS **GUID** of the target computer.</span></span>

</dd> <dt>

<span data-ttu-id="7b186-166">**TargetMac**</span><span class="sxs-lookup"><span data-stu-id="7b186-166">**TargetMac**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b186-167">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7b186-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7b186-168">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7b186-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b186-169">Qualificatori: [**chiave**](/windows/desktop/WmiSdk/key-qualifier), [**correzione**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="7b186-169">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="7b186-170">Indirizzo MAC del computer di destinazione.</span><span class="sxs-lookup"><span data-stu-id="7b186-170">The MAC address of the target computer.</span></span>

</dd> <dt>

<span data-ttu-id="7b186-171">**WmiDateTime**</span><span class="sxs-lookup"><span data-stu-id="7b186-171">**WmiDateTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b186-172">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="7b186-172">Data type: **DATETIME**</span></span>
</dt> <dt>

<span data-ttu-id="7b186-173">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7b186-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b186-174">Qualificatori: [ **corretti**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="7b186-174">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="7b186-175">Timestamp di quando è stata registrata questa modifica dello stato.</span><span class="sxs-lookup"><span data-stu-id="7b186-175">Timestamp of when this state change was recorded.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7b186-176">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7b186-176">Requirements</span></span>



| <span data-ttu-id="7b186-177">Requisito</span><span class="sxs-lookup"><span data-stu-id="7b186-177">Requirement</span></span> | <span data-ttu-id="7b186-178">Valore</span><span class="sxs-lookup"><span data-stu-id="7b186-178">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b186-179">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7b186-179">Minimum supported client</span></span><br/> | <span data-ttu-id="7b186-180">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="7b186-180">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="7b186-181">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7b186-181">Minimum supported server</span></span><br/> | <span data-ttu-id="7b186-182">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="7b186-182">Windows Server 2016</span></span><br/>                                                                       |
| <span data-ttu-id="7b186-183">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="7b186-183">Namespace</span></span><br/>                | <span data-ttu-id="7b186-184">Radice \\ Microsoft \\ Windows \\ BootEventCollector</span><span class="sxs-lookup"><span data-stu-id="7b186-184">Root\\Microsoft\\Windows\\BootEventCollector</span></span><br/>                                              |
| <span data-ttu-id="7b186-185">MOF</span><span class="sxs-lookup"><span data-stu-id="7b186-185">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7b186-186"><dt>BootEventCollectorWMI. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7b186-186"><dt>BootEventCollectorWMI.mof</dt></span></span> </dl> |
| <span data-ttu-id="7b186-187">DLL</span><span class="sxs-lookup"><span data-stu-id="7b186-187">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7b186-188"><dt>BEvtCol.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7b186-188"><dt>BEvtCol.exe</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="7b186-189">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7b186-189">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b186-190">Provider WMI raccolta eventi di avvio</span><span class="sxs-lookup"><span data-stu-id="7b186-190">Boot Event Collector WMI Provider</span></span>](boot-event-collector-wmi-provider-portal.md)
</dt> </dl>

 

