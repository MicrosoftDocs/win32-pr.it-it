---
description: Destinazioni note che contengono i dati raccolti. Disponibile solo se l'agente di raccolta è in esecuzione con il log di stato abilitato.
ms.assetid: ab0d2949-9808-49c3-8a0c-f2ce9c300a2a
ms.tgt_platform: multiple
title: Classe TargetForwardingDestination
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TargetForwardingDestination
- TargetForwardingDestination.TargetEndpoint
- TargetForwardingDestination.TargetMac
- TargetForwardingDestination.TargetGuid
- TargetForwardingDestination.CollectorEndpoint
- TargetForwardingDestination.Computer
- TargetForwardingDestination.ForwarderType
- TargetForwardingDestination.Destination
- TargetForwardingDestination.DestinationPattern
- TargetForwardingDestination.Error
- TargetForwardingDestination.ConnectedSince
- TargetForwardingDestination.DisconnectedSince
- TargetForwardingDestination.WmiDateTime
api_type:
- DllExport
api_location:
- BEvtCol.exe
ms.openlocfilehash: 735b6179fe9d72b5faf0cad976410aeace427f63
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104482796"
---
# <a name="targetforwardingdestination-class"></a><span data-ttu-id="38d5c-104">Classe TargetForwardingDestination</span><span class="sxs-lookup"><span data-stu-id="38d5c-104">TargetForwardingDestination class</span></span>

<span data-ttu-id="38d5c-105">Destinazioni note che contengono i dati raccolti.</span><span class="sxs-lookup"><span data-stu-id="38d5c-105">The known destinations containing the collected data.</span></span> <span data-ttu-id="38d5c-106">Disponibile solo se l'agente di raccolta è in esecuzione con il log di stato abilitato.</span><span class="sxs-lookup"><span data-stu-id="38d5c-106">Available only if the collector is running with the status log enabled.</span></span>

<span data-ttu-id="38d5c-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="38d5c-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="38d5c-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="38d5c-108">Syntax</span></span>

``` syntax
[Provider("BootEventCollectorWmiProvider"), Dynamic, AMENDMENT]
class TargetForwardingDestination
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

## <a name="members"></a><span data-ttu-id="38d5c-109">Members</span><span class="sxs-lookup"><span data-stu-id="38d5c-109">Members</span></span>

<span data-ttu-id="38d5c-110">La classe **TargetForwardingDestination** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="38d5c-110">The **TargetForwardingDestination** class has these types of members:</span></span>

-   [<span data-ttu-id="38d5c-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="38d5c-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="38d5c-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="38d5c-112">Properties</span></span>

<span data-ttu-id="38d5c-113">La classe **TargetForwardingDestination** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="38d5c-113">The **TargetForwardingDestination** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="38d5c-114">**CollectorEndpoint**</span><span class="sxs-lookup"><span data-stu-id="38d5c-114">**CollectorEndpoint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38d5c-115">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="38d5c-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="38d5c-116">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="38d5c-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="38d5c-117">Qualificatori: [ **corretti**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="38d5c-117">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="38d5c-118">Host: informazioni sulla porta dell'endpoint sul lato agente di raccolta.</span><span class="sxs-lookup"><span data-stu-id="38d5c-118">The host:port information of the endpoint on the collector side.</span></span>

</dd> <dt>

<span data-ttu-id="38d5c-119">**Computer**</span><span class="sxs-lookup"><span data-stu-id="38d5c-119">**Computer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38d5c-120">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="38d5c-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="38d5c-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="38d5c-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="38d5c-122">Qualificatori: [ **corretti**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="38d5c-122">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="38d5c-123">Nome del computer di destinazione, come determinato dall'agente di raccolta in base alla relativa configurazione.</span><span class="sxs-lookup"><span data-stu-id="38d5c-123">Target computer name, as determined by the collector according to its configuration.</span></span>

</dd> <dt>

<span data-ttu-id="38d5c-124">**ConnectedSince**</span><span class="sxs-lookup"><span data-stu-id="38d5c-124">**ConnectedSince**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38d5c-125">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="38d5c-125">Data type: **DATETIME**</span></span>
</dt> <dt>

<span data-ttu-id="38d5c-126">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="38d5c-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="38d5c-127">Qualificatori: [ **corretti**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="38d5c-127">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="38d5c-128">Timestamp del momento in cui è stata stabilita la connessione.</span><span class="sxs-lookup"><span data-stu-id="38d5c-128">Timestamp of when the connection was established.</span></span>

</dd> <dt>

<span data-ttu-id="38d5c-129">**Destinazione**</span><span class="sxs-lookup"><span data-stu-id="38d5c-129">**Destination**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38d5c-130">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="38d5c-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="38d5c-131">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="38d5c-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="38d5c-132">Qualificatori: [**chiave**](/windows/desktop/WmiSdk/key-qualifier), [**correzione**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="38d5c-132">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="38d5c-133">Destinazione dei dati.</span><span class="sxs-lookup"><span data-stu-id="38d5c-133">Destination of the data.</span></span> <span data-ttu-id="38d5c-134">Il significato dipende dal tipo di server d'avanzamento.</span><span class="sxs-lookup"><span data-stu-id="38d5c-134">The meaning depends on the forwarder type.</span></span> <span data-ttu-id="38d5c-135">Può essere un nome di file o un'altra identificazione.</span><span class="sxs-lookup"><span data-stu-id="38d5c-135">May be a file name or some other identification.</span></span>

</dd> <dt>

<span data-ttu-id="38d5c-136">**DestinationPattern**</span><span class="sxs-lookup"><span data-stu-id="38d5c-136">**DestinationPattern**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38d5c-137">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="38d5c-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="38d5c-138">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="38d5c-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="38d5c-139">Qualificatori: [ **corretti**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="38d5c-139">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="38d5c-140">Modello utilizzato per generare la destinazione dei dati.</span><span class="sxs-lookup"><span data-stu-id="38d5c-140">Pattern used to generate the destination of the data.</span></span> <span data-ttu-id="38d5c-141">Il significato dipende dal tipo e dalla configurazione del server d'avanzamento.</span><span class="sxs-lookup"><span data-stu-id="38d5c-141">The meaning depends on the forwarder type and configuration.</span></span> <span data-ttu-id="38d5c-142">Per una destinazione fissa, sarà uguale alla destinazione stessa.</span><span class="sxs-lookup"><span data-stu-id="38d5c-142">For a fixed destination, would be the same as the destination itself.</span></span> <span data-ttu-id="38d5c-143">Per la destinazione con rotazione dei file sono inclusi i caratteri di pattern che verranno sostituiti con l'indice effettivo nella destinazione.</span><span class="sxs-lookup"><span data-stu-id="38d5c-143">For the destination with rotation of the files would contain the pattern characters that will be replaced with the actual index in the destination.</span></span>

</dd> <dt>

<span data-ttu-id="38d5c-144">**DisconnectedSince**</span><span class="sxs-lookup"><span data-stu-id="38d5c-144">**DisconnectedSince**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38d5c-145">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="38d5c-145">Data type: **DATETIME**</span></span>
</dt> <dt>

<span data-ttu-id="38d5c-146">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="38d5c-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="38d5c-147">Qualificatori: [ **corretti**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="38d5c-147">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="38d5c-148">Timestamp del momento in cui la connessione è stata eliminata.</span><span class="sxs-lookup"><span data-stu-id="38d5c-148">Timestamp of when the connection was dropped.</span></span>

</dd> <dt>

<span data-ttu-id="38d5c-149">**Error (Errore) (Error (Errore)e)**</span><span class="sxs-lookup"><span data-stu-id="38d5c-149">**Error**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38d5c-150">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="38d5c-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="38d5c-151">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="38d5c-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="38d5c-152">Qualificatori: [ **corretti**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="38d5c-152">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="38d5c-153">Messaggio di errore se si è verificato un errore.</span><span class="sxs-lookup"><span data-stu-id="38d5c-153">Error message if an error was encountered.</span></span> <span data-ttu-id="38d5c-154">In caso contrario, sarà vuoto.</span><span class="sxs-lookup"><span data-stu-id="38d5c-154">Otherwise will be empty.</span></span>

</dd> <dt>

<span data-ttu-id="38d5c-155">**ForwarderType**</span><span class="sxs-lookup"><span data-stu-id="38d5c-155">**ForwarderType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38d5c-156">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="38d5c-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="38d5c-157">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="38d5c-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="38d5c-158">Qualificatori: [**chiave**](/windows/desktop/WmiSdk/key-qualifier), [**correzione**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="38d5c-158">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="38d5c-159">Tipo del server d'inoltre (ad esempio "ETL").</span><span class="sxs-lookup"><span data-stu-id="38d5c-159">Type of the forwarder (such as 'etl').</span></span>

</dd> <dt>

<span data-ttu-id="38d5c-160">**TargetEndpoint**</span><span class="sxs-lookup"><span data-stu-id="38d5c-160">**TargetEndpoint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38d5c-161">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="38d5c-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="38d5c-162">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="38d5c-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="38d5c-163">Qualificatori: [ **corretti**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="38d5c-163">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="38d5c-164">Informazioni sull'endpoint del computer di destinazione, in formato leggibile.</span><span class="sxs-lookup"><span data-stu-id="38d5c-164">The endpoint information of the target computer, in human-readable format.</span></span> <span data-ttu-id="38d5c-165">Questa proprietà è formattata come stringa *host*:*porta* .</span><span class="sxs-lookup"><span data-stu-id="38d5c-165">This property is formatted as a *host*:*port* string.</span></span> <span data-ttu-id="38d5c-166">Ad esempio, "127.0.0.1:50000".</span><span class="sxs-lookup"><span data-stu-id="38d5c-166">For example, "127.0.0.1:50000".</span></span>

</dd> <dt>

<span data-ttu-id="38d5c-167">**TargetGuid**</span><span class="sxs-lookup"><span data-stu-id="38d5c-167">**TargetGuid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38d5c-168">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="38d5c-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="38d5c-169">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="38d5c-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="38d5c-170">Qualificatori: [ **corretti**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="38d5c-170">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="38d5c-171">Il GUID SMBIOS del computer di destinazione (se noto).</span><span class="sxs-lookup"><span data-stu-id="38d5c-171">The target computer's SMBIOS GUID (if known).</span></span>

</dd> <dt>

<span data-ttu-id="38d5c-172">**TargetMac**</span><span class="sxs-lookup"><span data-stu-id="38d5c-172">**TargetMac**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38d5c-173">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="38d5c-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="38d5c-174">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="38d5c-174">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="38d5c-175">Qualificatori: [ **corretti**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="38d5c-175">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="38d5c-176">Indirizzo MAC del computer di destinazione (se noto).</span><span class="sxs-lookup"><span data-stu-id="38d5c-176">The target computer's MAC address (if known).</span></span>

</dd> <dt>

<span data-ttu-id="38d5c-177">**WmiDateTime**</span><span class="sxs-lookup"><span data-stu-id="38d5c-177">**WmiDateTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38d5c-178">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="38d5c-178">Data type: **DATETIME**</span></span>
</dt> <dt>

<span data-ttu-id="38d5c-179">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="38d5c-179">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="38d5c-180">Qualificatori: [ **corretti**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="38d5c-180">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="38d5c-181">Timestamp di quando è stata registrata questa modifica dello stato.</span><span class="sxs-lookup"><span data-stu-id="38d5c-181">Timestamp of when this state change was recorded.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="38d5c-182">Requisiti</span><span class="sxs-lookup"><span data-stu-id="38d5c-182">Requirements</span></span>



| <span data-ttu-id="38d5c-183">Requisito</span><span class="sxs-lookup"><span data-stu-id="38d5c-183">Requirement</span></span> | <span data-ttu-id="38d5c-184">Valore</span><span class="sxs-lookup"><span data-stu-id="38d5c-184">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="38d5c-185">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="38d5c-185">Minimum supported client</span></span><br/> | <span data-ttu-id="38d5c-186">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="38d5c-186">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="38d5c-187">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="38d5c-187">Minimum supported server</span></span><br/> | <span data-ttu-id="38d5c-188">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="38d5c-188">Windows Server 2016</span></span><br/>                                                                       |
| <span data-ttu-id="38d5c-189">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="38d5c-189">Namespace</span></span><br/>                | <span data-ttu-id="38d5c-190">Radice \\ Microsoft \\ Windows \\ BootEventCollector</span><span class="sxs-lookup"><span data-stu-id="38d5c-190">Root\\Microsoft\\Windows\\BootEventCollector</span></span><br/>                                              |
| <span data-ttu-id="38d5c-191">MOF</span><span class="sxs-lookup"><span data-stu-id="38d5c-191">MOF</span></span><br/>                      | <dl> <span data-ttu-id="38d5c-192"><dt>BootEventCollectorWMI. mof</dt></span><span class="sxs-lookup"><span data-stu-id="38d5c-192"><dt>BootEventCollectorWMI.mof</dt></span></span> </dl> |
| <span data-ttu-id="38d5c-193">DLL</span><span class="sxs-lookup"><span data-stu-id="38d5c-193">DLL</span></span><br/>                      | <dl> <span data-ttu-id="38d5c-194"><dt>BEvtCol.exe</dt></span><span class="sxs-lookup"><span data-stu-id="38d5c-194"><dt>BEvtCol.exe</dt></span></span> </dl>               |



 

