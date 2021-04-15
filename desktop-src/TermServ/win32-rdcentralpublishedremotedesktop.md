---
title: Classe Win32_RDCentralPublishedRemoteDesktop
description: Desktop pubblicato in un altro computer, per l'utilizzo remoto tramite Servizi terminal.
ms.assetid: 2b28a2d3-048f-446f-9ce0-eb684b393eaa
ms.tgt_platform: multiple
keywords:
- Classe Win32_RDCentralPublishedRemoteDesktop Servizi Desktop remoto
- Classe Win32_RDCentralPublishedRemoteDesktop Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- Win32_RDCentralPublishedRemoteDesktop
- Win32_RDCentralPublishedRemoteDesktop.Caption
- Win32_RDCentralPublishedRemoteDesktop.Description
- Win32_RDCentralPublishedRemoteDesktop.InstallDate
- Win32_RDCentralPublishedRemoteDesktop.Name
- Win32_RDCentralPublishedRemoteDesktop.Status
- Win32_RDCentralPublishedRemoteDesktop.PublishingFarm
- Win32_RDCentralPublishedRemoteDesktop.Alias
- Win32_RDCentralPublishedRemoteDesktop.IconContents
- Win32_RDCentralPublishedRemoteDesktop.ShowInPortal
- Win32_RDCentralPublishedRemoteDesktop.RDPFileContents
- Win32_RDCentralPublishedRemoteDesktop.Folders
api_location:
- TscPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04696331b7027b7cc65d2202c29e6ce95bb3f4b8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476210"
---
# <a name="win32_rdcentralpublishedremotedesktop-class"></a><span data-ttu-id="558ee-105">Win32 \_ RDCentralPublishedRemoteDesktop (classe)</span><span class="sxs-lookup"><span data-stu-id="558ee-105">Win32\_RDCentralPublishedRemoteDesktop class</span></span>

<span data-ttu-id="558ee-106">Desktop pubblicato in un altro computer, per l'utilizzo remoto tramite Servizi terminal</span><span class="sxs-lookup"><span data-stu-id="558ee-106">Desktop published on another computer, for remote use through Terminal Services</span></span>

<span data-ttu-id="558ee-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="558ee-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="558ee-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="558ee-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_TSCentralPublisher_Prov")]
class Win32_RDCentralPublishedRemoteDesktop : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   PublishingFarm;
  string   Alias;
  uint8    IconContents[];
  boolean  ShowInPortal;
  string   RDPFileContents;
  string   Folders[];
};
```

## <a name="members"></a><span data-ttu-id="558ee-109">Members</span><span class="sxs-lookup"><span data-stu-id="558ee-109">Members</span></span>

<span data-ttu-id="558ee-110">La classe **Win32 \_ RDCentralPublishedRemoteDesktop** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="558ee-110">The **Win32\_RDCentralPublishedRemoteDesktop** class has these types of members:</span></span>

-   [<span data-ttu-id="558ee-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="558ee-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="558ee-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="558ee-112">Properties</span></span>

<span data-ttu-id="558ee-113">La classe **Win32 \_ RDCentralPublishedRemoteDesktop** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="558ee-113">The **Win32\_RDCentralPublishedRemoteDesktop** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="558ee-114">**Alias**</span><span class="sxs-lookup"><span data-stu-id="558ee-114">**Alias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="558ee-115">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="558ee-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="558ee-116">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="558ee-116">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="558ee-117">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="558ee-117">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="558ee-118">Alias del desktop.</span><span class="sxs-lookup"><span data-stu-id="558ee-118">Alias of the desktop.</span></span>

</dd> <dt>

<span data-ttu-id="558ee-119">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="558ee-119">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="558ee-120">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="558ee-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="558ee-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="558ee-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="558ee-122">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="558ee-122">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="558ee-123">Breve descrizione (stringa a una riga) dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="558ee-123">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="558ee-124">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="558ee-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="558ee-125">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="558ee-125">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="558ee-126">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="558ee-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="558ee-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="558ee-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="558ee-128">Descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="558ee-128">Description of the object.</span></span>

<span data-ttu-id="558ee-129">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="558ee-129">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="558ee-130">**Cartelle**</span><span class="sxs-lookup"><span data-stu-id="558ee-130">**Folders**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="558ee-131">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="558ee-131">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="558ee-132">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="558ee-132">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="558ee-133">Elenco delle cartelle in cui deve essere visualizzata la risorsa.</span><span class="sxs-lookup"><span data-stu-id="558ee-133">List of the folders where this resource should be displayed.</span></span>

</dd> <dt>

<span data-ttu-id="558ee-134">**IconContents**</span><span class="sxs-lookup"><span data-stu-id="558ee-134">**IconContents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="558ee-135">Tipo di dati: matrice **Uint8**</span><span class="sxs-lookup"><span data-stu-id="558ee-135">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="558ee-136">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="558ee-136">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="558ee-137">Qualificatori: [ **facoltativo**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="558ee-137">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="558ee-138">Contenuto dell'icona corrispondente all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="558ee-138">Contents of the icon corresponding to the application.</span></span>

</dd> <dt>

<span data-ttu-id="558ee-139">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="558ee-139">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="558ee-140">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="558ee-140">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="558ee-141">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="558ee-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="558ee-142">Qualificatori: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="558ee-142">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="558ee-143">Data di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="558ee-143">The date the object was installed.</span></span> <span data-ttu-id="558ee-144">La mancanza di un valore non indica che l'oggetto non è installato.</span><span class="sxs-lookup"><span data-stu-id="558ee-144">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="558ee-145">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="558ee-145">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="558ee-146">**Nome**</span><span class="sxs-lookup"><span data-stu-id="558ee-146">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="558ee-147">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="558ee-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="558ee-148">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="558ee-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="558ee-149">Nome dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="558ee-149">The name of the object.</span></span>

<span data-ttu-id="558ee-150">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="558ee-150">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="558ee-151">**PublishingFarm**</span><span class="sxs-lookup"><span data-stu-id="558ee-151">**PublishingFarm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="558ee-152">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="558ee-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="558ee-153">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="558ee-153">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="558ee-154">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="558ee-154">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="558ee-155">Alias della farm che ha pubblicato il desktop.</span><span class="sxs-lookup"><span data-stu-id="558ee-155">Alias of the farm that published the desktop.</span></span>

</dd> <dt>

<span data-ttu-id="558ee-156">**RDPFileContents**</span><span class="sxs-lookup"><span data-stu-id="558ee-156">**RDPFileContents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="558ee-157">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="558ee-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="558ee-158">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="558ee-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="558ee-159">Contenuto del file RDP corrispondente al desktop.</span><span class="sxs-lookup"><span data-stu-id="558ee-159">Contents of the RDP file corresponding to the desktop.</span></span>

</dd> <dt>

<span data-ttu-id="558ee-160">**ShowInPortal**</span><span class="sxs-lookup"><span data-stu-id="558ee-160">**ShowInPortal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="558ee-161">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="558ee-161">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="558ee-162">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="558ee-162">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="558ee-163">**true** se l'applicazione deve essere visualizzata nel accesso Web di Servizi terminal; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="558ee-163">**true** if this application should be shown in the TS Web Access; otherwise, **false**.</span></span>

</dd> <dt>

<span data-ttu-id="558ee-164">**Status**</span><span class="sxs-lookup"><span data-stu-id="558ee-164">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="558ee-165">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="558ee-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="558ee-166">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="558ee-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="558ee-167">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="558ee-167">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="558ee-168">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="558ee-168">Current status of the object.</span></span> <span data-ttu-id="558ee-169">È possibile definire diversi stati operativi e non operativi.</span><span class="sxs-lookup"><span data-stu-id="558ee-169">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="558ee-170">Gli stati operativi includono: "OK", "degradato" e "errore Predator" (un elemento, ad esempio un'unità disco rigido abilitata per SMART, potrebbe funzionare correttamente, ma prevedere un errore nel prossimo futuro).</span><span class="sxs-lookup"><span data-stu-id="558ee-170">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="558ee-171">Gli Stati non operativi includono: "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="558ee-171">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="558ee-172">Il secondo "servizio" può essere applicato durante il mirroring di un disco, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="558ee-172">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="558ee-173">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="558ee-173">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="558ee-174">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="558ee-174">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="558ee-175">("OK")</span><span class="sxs-lookup"><span data-stu-id="558ee-175">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="558ee-176">("Errore")</span><span class="sxs-lookup"><span data-stu-id="558ee-176">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="558ee-177">("Danneggiato")</span><span class="sxs-lookup"><span data-stu-id="558ee-177">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="558ee-178">("Sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="558ee-178">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="558ee-179">("Errore di predazione")</span><span class="sxs-lookup"><span data-stu-id="558ee-179">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="558ee-180">("Avvio")</span><span class="sxs-lookup"><span data-stu-id="558ee-180">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="558ee-181">("Arresto")</span><span class="sxs-lookup"><span data-stu-id="558ee-181">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="558ee-182">("Servizio")</span><span class="sxs-lookup"><span data-stu-id="558ee-182">("Service")</span></span>


<span data-ttu-id="558ee-183"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="558ee-183"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="558ee-184">Requisiti</span><span class="sxs-lookup"><span data-stu-id="558ee-184">Requirements</span></span>



| <span data-ttu-id="558ee-185">Requisito</span><span class="sxs-lookup"><span data-stu-id="558ee-185">Requirement</span></span> | <span data-ttu-id="558ee-186">Valore</span><span class="sxs-lookup"><span data-stu-id="558ee-186">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="558ee-187">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="558ee-187">Minimum supported client</span></span><br/> | <span data-ttu-id="558ee-188">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="558ee-188">None supported</span></span><br/>                                                                |
| <span data-ttu-id="558ee-189">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="558ee-189">Minimum supported server</span></span><br/> | <span data-ttu-id="558ee-190">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="558ee-190">Windows Server 2012</span></span><br/>                                                           |
| <span data-ttu-id="558ee-191">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="558ee-191">Namespace</span></span><br/>                | <span data-ttu-id="558ee-192">Radice \\ CIMV2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="558ee-192">Root\\cimv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="558ee-193">MOF</span><span class="sxs-lookup"><span data-stu-id="558ee-193">MOF</span></span><br/>                      | <dl> <span data-ttu-id="558ee-194"><dt>Tscpub. mof</dt></span><span class="sxs-lookup"><span data-stu-id="558ee-194"><dt>Tscpub.mof</dt></span></span> </dl>    |
| <span data-ttu-id="558ee-195">DLL</span><span class="sxs-lookup"><span data-stu-id="558ee-195">DLL</span></span><br/>                      | <dl> <span data-ttu-id="558ee-196"><dt>TscPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="558ee-196"><dt>TscPubWmi.dll</dt></span></span> </dl> |



 

