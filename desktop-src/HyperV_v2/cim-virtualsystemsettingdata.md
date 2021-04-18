---
description: Vengono descritti gli aspetti virtuali di un sistema virtuale tramite un set di proprietà specifiche della virtualizzazione. CIM \_ VirtualSystemSettingData viene usato anche come classe di primo livello delle configurazioni di sistema virtuale.
ms.assetid: 501e659d-f190-41f9-aafa-447048a60e7c
title: Classe CIM_VirtualSystemSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemSettingData
- CIM_VirtualSystemSettingData.VirtualSystemIdentifier
- CIM_VirtualSystemSettingData.VirtualSystemType
- CIM_VirtualSystemSettingData.Notes
- CIM_VirtualSystemSettingData.CreationTime
- CIM_VirtualSystemSettingData.ConfigurationID
- CIM_VirtualSystemSettingData.ConfigurationDataRoot
- CIM_VirtualSystemSettingData.ConfigurationFile
- CIM_VirtualSystemSettingData.SnapshotDataRoot
- CIM_VirtualSystemSettingData.SuspendDataRoot
- CIM_VirtualSystemSettingData.SwapFileDataRoot
- CIM_VirtualSystemSettingData.LogDataRoot
- CIM_VirtualSystemSettingData.AutomaticStartupAction
- CIM_VirtualSystemSettingData.AutomaticStartupActionDelay
- CIM_VirtualSystemSettingData.AutomaticStartupActionSequenceNumber
- CIM_VirtualSystemSettingData.AutomaticShutdownAction
- CIM_VirtualSystemSettingData.AutomaticRecoveryAction
- CIM_VirtualSystemSettingData.RecoveryFile
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ff2c9725c8469b3e2c29d2e98a708d27e80378f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315521"
---
# <a name="cim_virtualsystemsettingdata-class"></a><span data-ttu-id="a46d2-104">CIM \_ VirtualSystemSettingData (classe)</span><span class="sxs-lookup"><span data-stu-id="a46d2-104">CIM\_VirtualSystemSettingData class</span></span>

<span data-ttu-id="a46d2-105">Vengono descritti gli aspetti virtuali di un sistema virtuale tramite un set di proprietà specifiche della virtualizzazione.</span><span class="sxs-lookup"><span data-stu-id="a46d2-105">Describes the virtual aspects of a virtual system through a set of virtualization specific properties.</span></span> <span data-ttu-id="a46d2-106">**CIM \_ VirtualSystemSettingData** viene utilizzato anche come classe di primo livello delle configurazioni di sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="a46d2-106">**CIM\_VirtualSystemSettingData** is also used as the top level class of virtual system configurations.</span></span>

## <a name="syntax"></a><span data-ttu-id="a46d2-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a46d2-107">Syntax</span></span>

``` syntax
[Abstract, Version("2.25.0"), UMLPackagePath("CIM::System::SystemElements"), AMENDMENT]
class CIM_VirtualSystemSettingData : CIM_SettingData
{
  string   VirtualSystemIdentifier;
  string   VirtualSystemType;
  string   Notes[];
  datetime CreationTime;
  string   ConfigurationID;
  string   ConfigurationDataRoot;
  string   ConfigurationFile;
  string   SnapshotDataRoot;
  string   SuspendDataRoot;
  string   SwapFileDataRoot;
  string   LogDataRoot;
  uint16   AutomaticStartupAction;
  datetime AutomaticStartupActionDelay;
  uint16   AutomaticStartupActionSequenceNumber;
  uint16   AutomaticShutdownAction;
  uint16   AutomaticRecoveryAction;
  string   RecoveryFile;
};
```

## <a name="members"></a><span data-ttu-id="a46d2-108">Members</span><span class="sxs-lookup"><span data-stu-id="a46d2-108">Members</span></span>

<span data-ttu-id="a46d2-109">La classe **CIM \_ VirtualSystemSettingData** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="a46d2-109">The **CIM\_VirtualSystemSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="a46d2-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a46d2-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a46d2-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a46d2-111">Properties</span></span>

<span data-ttu-id="a46d2-112">La classe **CIM \_ VirtualSystemSettingData** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="a46d2-112">The **CIM\_VirtualSystemSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a46d2-113">**AutomaticRecoveryAction**</span><span class="sxs-lookup"><span data-stu-id="a46d2-113">**AutomaticRecoveryAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a46d2-114">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a46d2-114">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a46d2-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a46d2-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a46d2-116">Azione da intraprendere per il sistema virtuale quando il software eseguito dal sistema virtuale ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="a46d2-116">The action to take for the virtual system when the software executed by the virtual system fails.</span></span> <span data-ttu-id="a46d2-117">Gli errori risolti da questa proprietà includono solo quelli che possono essere rilevati dalla piattaforma host, ad esempio una condizione di stato di attesa non interrompibili.</span><span class="sxs-lookup"><span data-stu-id="a46d2-117">The failures addressed by this property only include those that are detectable by the host platform, such as a non-interruptible wait state condition.</span></span>

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="a46d2-118">**Nessuno** (2)</span><span class="sxs-lookup"><span data-stu-id="a46d2-118">**None** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Restart"></span><span id="restart"></span><span id="RESTART"></span>

<span data-ttu-id="a46d2-119">**Riavvia** (3)</span><span class="sxs-lookup"><span data-stu-id="a46d2-119">**Restart** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Revert_to_snapshot"></span><span id="revert_to_snapshot"></span><span id="REVERT_TO_SNAPSHOT"></span>

<span data-ttu-id="a46d2-120">**Ripristina snapshot** (4)</span><span class="sxs-lookup"><span data-stu-id="a46d2-120">**Revert to snapshot** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="a46d2-121">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="a46d2-121">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a46d2-122">**AutomaticShutdownAction**</span><span class="sxs-lookup"><span data-stu-id="a46d2-122">**AutomaticShutdownAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a46d2-123">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a46d2-123">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a46d2-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a46d2-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a46d2-125">Azione da eseguire per il sistema virtuale quando l'host viene arrestato.</span><span class="sxs-lookup"><span data-stu-id="a46d2-125">The action to take for the virtual system when the host is shut down.</span></span>

<dt>

<span id="Turn_Off"></span><span id="turn_off"></span><span id="TURN_OFF"></span>

<span data-ttu-id="a46d2-126">**Disattiva** (2)</span><span class="sxs-lookup"><span data-stu-id="a46d2-126">**Turn Off** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Save_state"></span><span id="save_state"></span><span id="SAVE_STATE"></span>

<span data-ttu-id="a46d2-127">**Salva stato** (3)</span><span class="sxs-lookup"><span data-stu-id="a46d2-127">**Save state** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Shutdown"></span><span id="shutdown"></span><span id="SHUTDOWN"></span>

<span data-ttu-id="a46d2-128">**Arresto** (4)</span><span class="sxs-lookup"><span data-stu-id="a46d2-128">**Shutdown** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="a46d2-129">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="a46d2-129">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a46d2-130">**AutomaticStartupAction**</span><span class="sxs-lookup"><span data-stu-id="a46d2-130">**AutomaticStartupAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a46d2-131">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a46d2-131">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a46d2-132">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a46d2-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a46d2-133">Azione da intraprendere sul sistema virtuale quando l'host viene avviato.</span><span class="sxs-lookup"><span data-stu-id="a46d2-133">The action to take on the virtual system when the host is started.</span></span>

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="a46d2-134">**Nessuno** (2)</span><span class="sxs-lookup"><span data-stu-id="a46d2-134">**None** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Restart_if_previously_active"></span><span id="restart_if_previously_active"></span><span id="RESTART_IF_PREVIOUSLY_ACTIVE"></span>

<span data-ttu-id="a46d2-135">**Riavvia se in precedenza attivo** (3)</span><span class="sxs-lookup"><span data-stu-id="a46d2-135">**Restart if previously active** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Always_startup"></span><span id="always_startup"></span><span id="ALWAYS_STARTUP"></span>

<span data-ttu-id="a46d2-136">**Avvio sempre** (4)</span><span class="sxs-lookup"><span data-stu-id="a46d2-136">**Always startup** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="a46d2-137">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="a46d2-137">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a46d2-138">**AutomaticStartupActionDelay**</span><span class="sxs-lookup"><span data-stu-id="a46d2-138">**AutomaticStartupActionDelay**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a46d2-139">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="a46d2-139">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a46d2-140">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a46d2-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a46d2-141">Ritardo per l'azione di avvio.</span><span class="sxs-lookup"><span data-stu-id="a46d2-141">The delay for the startup action.</span></span> <span data-ttu-id="a46d2-142">Questo valore è una variante di intervallo del tipo di dati **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="a46d2-142">This value is an interval variant of the **datetime** data type.</span></span>

</dd> <dt>

<span data-ttu-id="a46d2-143">**AutomaticStartupActionSequenceNumber**</span><span class="sxs-lookup"><span data-stu-id="a46d2-143">**AutomaticStartupActionSequenceNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a46d2-144">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a46d2-144">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a46d2-145">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a46d2-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a46d2-146">Numero di sequenza per l'attivazione del sistema virtuale quando viene avviato il sistema host.</span><span class="sxs-lookup"><span data-stu-id="a46d2-146">The sequence number for virtual system activation when the host system is started.</span></span> <span data-ttu-id="a46d2-147">Un numero inferiore indica l'attivazione precedente.</span><span class="sxs-lookup"><span data-stu-id="a46d2-147">A lower number indicates earlier activation.</span></span> <span data-ttu-id="a46d2-148">Se una o più configurazioni mostrano lo stesso valore, la sequenza è dipendente dall'implementazione.</span><span class="sxs-lookup"><span data-stu-id="a46d2-148">If one or more configurations show the same value, the sequence is implementation dependent.</span></span> <span data-ttu-id="a46d2-149">Il valore "0" indica che la sequenza è dipendente dall'implementazione.</span><span class="sxs-lookup"><span data-stu-id="a46d2-149">A value of "0" indicates that the sequence is implementation dependent.</span></span>

</dd> <dt>

<span data-ttu-id="a46d2-150">**ConfigurationDataRoot**</span><span class="sxs-lookup"><span data-stu-id="a46d2-150">**ConfigurationDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a46d2-151">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a46d2-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a46d2-152">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a46d2-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a46d2-153">Percorso del file della directory in cui sono archiviate le informazioni sulla configurazione del sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="a46d2-153">The file path of the directory where information about the virtual system configuration is stored.</span></span> <span data-ttu-id="a46d2-154">Il formato di questa proprietà è un URI basato su RFC 2079.</span><span class="sxs-lookup"><span data-stu-id="a46d2-154">The format of this property is a URI based on RFC 2079.</span></span>

</dd> <dt>

<span data-ttu-id="a46d2-155">**ConfigurationFile**</span><span class="sxs-lookup"><span data-stu-id="a46d2-155">**ConfigurationFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a46d2-156">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a46d2-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a46d2-157">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a46d2-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a46d2-158">Percorso relativo del file in cui sono archiviate le informazioni sulla configurazione del sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="a46d2-158">The relative path of the file where information about the virtual system configuration is stored.</span></span> <span data-ttu-id="a46d2-159">Il percorso relativo viene accodato al valore della proprietà **ConfigurationDataRoot** .</span><span class="sxs-lookup"><span data-stu-id="a46d2-159">The relative path appends to the value of the **ConfigurationDataRoot** property.</span></span> <span data-ttu-id="a46d2-160">Il formato di questa proprietà è un URI basato su RFC 2079.</span><span class="sxs-lookup"><span data-stu-id="a46d2-160">The format of this property is a URI based on RFC 2079.</span></span>

</dd> <dt>

<span data-ttu-id="a46d2-161">**ConfigurationID**</span><span class="sxs-lookup"><span data-stu-id="a46d2-161">**ConfigurationID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a46d2-162">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a46d2-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a46d2-163">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a46d2-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a46d2-164">ID univoco della configurazione del sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="a46d2-164">The unique id of the virtual system configuration.</span></span>

> [!Note]  
> <span data-ttu-id="a46d2-165">**ConfigurationID** è diverso da **InstanceID** e viene assegnato dall'implementazione a un sistema virtuale o a una configurazione di sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="a46d2-165">**ConfigurationID** is different from the **InstanceID**, and is assigned by the implementation to a virtual system or a virtual system configuration.</span></span> <span data-ttu-id="a46d2-166">**ConfigurationID** non è una chiave e lo stesso valore può verificarsi per più di un'istanza.</span><span class="sxs-lookup"><span data-stu-id="a46d2-166">**ConfigurationID** is not a key, and the same value may occur for more than one instance.</span></span>

 

</dd> <dt>

<span data-ttu-id="a46d2-167">**CreationTime**</span><span class="sxs-lookup"><span data-stu-id="a46d2-167">**CreationTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a46d2-168">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="a46d2-168">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a46d2-169">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a46d2-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a46d2-170">Data e ora di creazione della configurazione del sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="a46d2-170">The date and time when the virtual system configuration was created.</span></span>

</dd> <dt>

<span data-ttu-id="a46d2-171">**LogDataRoot**</span><span class="sxs-lookup"><span data-stu-id="a46d2-171">**LogDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a46d2-172">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a46d2-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a46d2-173">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a46d2-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a46d2-174">Percorso relativo del file della directory in cui sono archiviate le informazioni sul log per il sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="a46d2-174">The relative file path of the directory where log information for the virtual system is stored.</span></span> <span data-ttu-id="a46d2-175">Il percorso relativo viene accodato al valore della proprietà **ConfigurationDataRoot** .</span><span class="sxs-lookup"><span data-stu-id="a46d2-175">The relative path appends to the value of the **ConfigurationDataRoot** property.</span></span> <span data-ttu-id="a46d2-176">Il formato di questa proprietà è un URI basato su RFC 2079.</span><span class="sxs-lookup"><span data-stu-id="a46d2-176">The format of this property is a URI based on RFC 2079.</span></span>

</dd> <dt>

<span data-ttu-id="a46d2-177">**Note**</span><span class="sxs-lookup"><span data-stu-id="a46d2-177">**Notes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a46d2-178">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="a46d2-178">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="a46d2-179">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a46d2-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a46d2-180">Matrice che contiene le note fornite dall'utente correlate al sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="a46d2-180">An array that contains user supplied notes that are related to the virtual system.</span></span>

</dd> <dt>

<span data-ttu-id="a46d2-181">**RecoveryFile**</span><span class="sxs-lookup"><span data-stu-id="a46d2-181">**RecoveryFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a46d2-182">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a46d2-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a46d2-183">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a46d2-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a46d2-184">Percorso del file in cui sono archiviate le informazioni relative al ripristino del sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="a46d2-184">The path of the file where recovery related information of the virtual system is stored.</span></span> <span data-ttu-id="a46d2-185">Il formato di questa proprietà è un URI basato su RFC 2079.</span><span class="sxs-lookup"><span data-stu-id="a46d2-185">The format of this property is a URI based on RFC 2079.</span></span>

</dd> <dt>

<span data-ttu-id="a46d2-186">**SnapshotDataRoot**</span><span class="sxs-lookup"><span data-stu-id="a46d2-186">**SnapshotDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a46d2-187">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a46d2-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a46d2-188">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a46d2-188">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a46d2-189">Percorso relativo della directory in cui vengono archiviate le informazioni sugli snapshot del sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="a46d2-189">The relative path of the directory where information about virtual system snapshots is stored.</span></span> <span data-ttu-id="a46d2-190">Il percorso relativo viene accodato al valore della proprietà **ConfigurationDataRoot** .</span><span class="sxs-lookup"><span data-stu-id="a46d2-190">The relative path appends to the value of the **ConfigurationDataRoot** property.</span></span> <span data-ttu-id="a46d2-191">Il formato di questa proprietà è un URI basato su RFC 2079.</span><span class="sxs-lookup"><span data-stu-id="a46d2-191">The format of this property is a URI based on RFC 2079.</span></span>

</dd> <dt>

<span data-ttu-id="a46d2-192">**SuspendDataRoot**</span><span class="sxs-lookup"><span data-stu-id="a46d2-192">**SuspendDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a46d2-193">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a46d2-193">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a46d2-194">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a46d2-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a46d2-195">Percorso relativo della directory in cui vengono archiviate le informazioni correlate di sospensione relative al sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="a46d2-195">The relative path of the directory where suspend related information about the virtual system is stored.</span></span> <span data-ttu-id="a46d2-196">Il percorso relativo viene accodato al valore della proprietà **ConfigurationDataRoot** .</span><span class="sxs-lookup"><span data-stu-id="a46d2-196">The relative path appends to the value of the **ConfigurationDataRoot** property.</span></span> <span data-ttu-id="a46d2-197">Il formato di questa proprietà è un URI basato su RFC 2079.</span><span class="sxs-lookup"><span data-stu-id="a46d2-197">The format of this property is a URI based on RFC 2079.</span></span>

</dd> <dt>

<span data-ttu-id="a46d2-198">**SwapFileDataRoot**</span><span class="sxs-lookup"><span data-stu-id="a46d2-198">**SwapFileDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a46d2-199">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a46d2-199">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a46d2-200">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a46d2-200">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a46d2-201">Percorso relativo del file della directory in cui sono archiviati i file di scambio del sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="a46d2-201">The relative file path of the directory where swap files of the virtual system are stored.</span></span> <span data-ttu-id="a46d2-202">Il percorso relativo viene accodato al valore della proprietà **ConfigurationDataRoot** .</span><span class="sxs-lookup"><span data-stu-id="a46d2-202">The relative path appends to the value of the **ConfigurationDataRoot** property.</span></span> <span data-ttu-id="a46d2-203">Il formato di questa proprietà è un URI basato su RFC 2079.</span><span class="sxs-lookup"><span data-stu-id="a46d2-203">The format of this property is a URI based on RFC 2079.</span></span>

</dd> <dt>

<span data-ttu-id="a46d2-204">**VirtualSystemIdentifier**</span><span class="sxs-lookup"><span data-stu-id="a46d2-204">**VirtualSystemIdentifier**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a46d2-205">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a46d2-205">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a46d2-206">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a46d2-206">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a46d2-207">Nome univoco del sistema all'interno della piattaforma di virtualizzazione.</span><span class="sxs-lookup"><span data-stu-id="a46d2-207">The unique name for the system within the virtualization platform.</span></span> <span data-ttu-id="a46d2-208">**VirtualSystemIdentifier** non è il nome host assegnato all'istanza del sistema operativo in esecuzione nel sistema virtuale, né un indirizzo IP o un indirizzo MAC assegnato a una delle porte di rete.</span><span class="sxs-lookup"><span data-stu-id="a46d2-208">**VirtualSystemIdentifier** is not the hostname assigned to the operating system instance running within the virtual system, nor is it an IP address or MAC address assigned to any of its network ports.</span></span>

<span data-ttu-id="a46d2-209">**VirtualSystemIdentifier** può contenere regole specifiche di implementazione, ad esempio semplici modelli o un'espressione regolare che può essere interpretata dall'implementazione durante l'impostazione di **VirtualSystemIdentifier**.</span><span class="sxs-lookup"><span data-stu-id="a46d2-209">The **VirtualSystemIdentifier** may contain implementation specific rules, like simple patterns or a regular expression that may be interpreted by the implementation when setting **VirtualSystemIdentifier**.</span></span>

</dd> <dt>

<span data-ttu-id="a46d2-210">**VirtualSystemType**</span><span class="sxs-lookup"><span data-stu-id="a46d2-210">**VirtualSystemType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a46d2-211">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a46d2-211">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a46d2-212">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a46d2-212">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a46d2-213">Tipo di sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="a46d2-213">The type of the virtual system.</span></span>

> [!Note]  
> <span data-ttu-id="a46d2-214">Se il tipo di sistema virtuale è sconosciuto, questo valore deve essere impostato su "DMTF: Unknown".</span><span class="sxs-lookup"><span data-stu-id="a46d2-214">If the virtual system type is unknown, this value must be set to "DMTF:unknown".</span></span>

 

<span data-ttu-id="a46d2-215">Questa proprietà viene formattata usando il formato ABNF (Augmented Naur Form) seguente:</span><span class="sxs-lookup"><span data-stu-id="a46d2-215">This property is formatted using the following Augmented Backus Naur Form (ABNF) format:</span></span>

<span data-ttu-id="a46d2-216">vs-Type = DMTF-value/other-org-value/legacy-value; DMTF-value = "DMTF:" define-org ":" org-vs-Type; Other-org-value = defineing-org ":" org-vs-Type;</span><span class="sxs-lookup"><span data-stu-id="a46d2-216">vs-type = dmtf-value / other-org-value / legacy-value; dmtf-value = "DMTF:" defining-org ":" org-vs-type; other-org-value = defining-org ":" org-vs-type;</span></span>

<span data-ttu-id="a46d2-217">Il valore del formato ABNF precedente è:</span><span class="sxs-lookup"><span data-stu-id="a46d2-217">The value of the above ABNF format are:</span></span>

-   <span data-ttu-id="a46d2-218">*DMTF-value*   un valore della proprietà definito da DMTF ed è definito nella descrizione di questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="a46d2-218">*dmtf-value*   a property value defined by DMTF and is defined in the description of this property.</span></span>
-   <span data-ttu-id="a46d2-219">*other-org-value*   è un valore di proprietà definito da un'entità di business diversa da DMTF e non è definito nella descrizione di questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="a46d2-219">*other-org-value*   is a property value defined by a business entity other than DMTF and is not defined in the description of this property.</span></span>
-   <span data-ttu-id="a46d2-220">*valore Legacy:*   valore della proprietà definito da un'entità di business diversa da DMTF e non è definito nella descrizione di questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="a46d2-220">*legacy-value*   a property value defined by a business entity other than DMTF and is not defined in the description of this property.</span></span> <span data-ttu-id="a46d2-221">Questi valori sono consentiti, ma è consigliabile deprecarli nel tempo.</span><span class="sxs-lookup"><span data-stu-id="a46d2-221">These values are permitted but recommended to be deprecated over time.</span></span>
-   <span data-ttu-id="a46d2-222">*definizione di-org*   un identificatore per l'entità business che definisce il tipo di sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="a46d2-222">*defining-org*   an identifier for the business entity that defines the virtual system type.</span></span> <span data-ttu-id="a46d2-223">Deve includere un nome con copyright, un marchio o un nome univoco di proprietà dell'entità di business.</span><span class="sxs-lookup"><span data-stu-id="a46d2-223">It should include a copyrighted, trademarked, or a unique name that is owned by the business entity.</span></span> <span data-ttu-id="a46d2-224">Non deve essere "DMTF" e non deve contenere i due punti.</span><span class="sxs-lookup"><span data-stu-id="a46d2-224">It should not be "DMTF" and shall not contain a colon.</span></span>
-   <span data-ttu-id="a46d2-225">*org-vs-digitare*   un identificatore per il tipo di sistema virtuale all'interno dell'entità di business che definisce.</span><span class="sxs-lookup"><span data-stu-id="a46d2-225">*org-vs-type*   an identifier for the virtual system type within the defining business entity.</span></span> <span data-ttu-id="a46d2-226">Deve essere univoco all'interno di define-org. org-vs-Type può usare qualsiasi carattere consentito per le stringhe CIM, ad eccezione dei seguenti: u0000-U001F (controlli Unicode C0), U0020 (spazio), U007F (controlli C0 Unicode) o U0080-U009F (controlli Unicode C1).</span><span class="sxs-lookup"><span data-stu-id="a46d2-226">It should be unique within defining-org. org-vs-type may use any character allowed for CIM strings, except the following: U0000-U001F (Unicode C0 controls), U0020 (space), U007F (Unicode C0 controls), or U0080-U009F (Unicode C1 controls).</span></span>
-   <span data-ttu-id="a46d2-227">Se è necessario strutturare il valore in segmenti, è necessario che i segmenti siano separati da un solo segno di due punti.</span><span class="sxs-lookup"><span data-stu-id="a46d2-227">If there is a need to structure the value into segments, the segments should be separated with a single colon.</span></span>
-   <span data-ttu-id="a46d2-228">I valori di questa proprietà devono essere elaborati con distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="a46d2-228">The values of this property should be processed case sensitively.</span></span> <span data-ttu-id="a46d2-229">Sono progettati per essere elaborati a livello di codice, anziché essere un nome visualizzato e dovrebbero essere brevi.</span><span class="sxs-lookup"><span data-stu-id="a46d2-229">They are intended to be processed programmatically, instead of being a display name, and should be short.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a46d2-230">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a46d2-230">Requirements</span></span>



| <span data-ttu-id="a46d2-231">Requisito</span><span class="sxs-lookup"><span data-stu-id="a46d2-231">Requirement</span></span> | <span data-ttu-id="a46d2-232">Valore</span><span class="sxs-lookup"><span data-stu-id="a46d2-232">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a46d2-233">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a46d2-233">Minimum supported client</span></span><br/> | <span data-ttu-id="a46d2-234">Windows 8</span><span class="sxs-lookup"><span data-stu-id="a46d2-234">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="a46d2-235">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a46d2-235">Minimum supported server</span></span><br/> | <span data-ttu-id="a46d2-236">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a46d2-236">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="a46d2-237">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="a46d2-237">Namespace</span></span><br/>                | <span data-ttu-id="a46d2-238">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="a46d2-238">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="a46d2-239">MOF</span><span class="sxs-lookup"><span data-stu-id="a46d2-239">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a46d2-240"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a46d2-240"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a46d2-241">DLL</span><span class="sxs-lookup"><span data-stu-id="a46d2-241">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a46d2-242"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a46d2-242"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="a46d2-243">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a46d2-243">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a46d2-244">**\_SETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="a46d2-244">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> </dl>

 

 




