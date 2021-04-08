---
description: Rappresenta un evento generato ogni volta che viene modificata la proprietà OperationalStatus della \_ classe MSVM ResourcePool o MSVM \_ disco logico.
ms.assetid: 20E7C22A-A151-4EDC-90D8-4BCD53C42355
title: Classe Msvm_StorageAlert
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_StorageAlert
- Msvm_StorageAlert.AlertingManagedElement
- Msvm_StorageAlert.AlertingElementFormat
- Msvm_StorageAlert.OtherAlertingElementFormat
- Msvm_StorageAlert.AlertType
- Msvm_StorageAlert.PerceivedSeverity
- Msvm_StorageAlert.ProbableCause
- Msvm_StorageAlert.ProbableCauseDescription
- Msvm_StorageAlert.EventTime
- Msvm_StorageAlert.OwningEntity
- Msvm_StorageAlert.MessageArguments
- Msvm_StorageAlert.MessageID
- Msvm_StorageAlert.Message
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: fa7f0430631082a9690cf2083f6b075ca62ee26b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104057820"
---
# <a name="msvm_storagealert-class"></a><span data-ttu-id="4b18f-103">\_Classe MSVM StorageAlert</span><span class="sxs-lookup"><span data-stu-id="4b18f-103">Msvm\_StorageAlert class</span></span>

<span data-ttu-id="4b18f-104">Rappresenta un evento generato ogni volta che viene modificata la proprietà **OperationalStatus** della classe [**MSVM \_ ResourcePool**](msvm-resourcepool.md) o [**MSVM \_ disco logico**](msvm-logicaldisk.md) .</span><span class="sxs-lookup"><span data-stu-id="4b18f-104">Represents an event that is raised each time the **OperationalStatus** property of the [**Msvm\_ResourcePool**](msvm-resourcepool.md) or [**Msvm\_LogicalDisk**](msvm-logicaldisk.md) class changes.</span></span>

<span data-ttu-id="4b18f-105">La sintassi seguente è semplificata dal codice MOF e include queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="4b18f-105">The following syntax is simplified from MOF code and includes these properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b18f-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4b18f-106">Syntax</span></span>

``` syntax
[Indication, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_StorageAlert : CIM_AlertIndication
{
  string   AlertingManagedElement[];
  uint16   AlertingElementFormat;
  uint16   OtherAlertingElementFormat;
  uint16   AlertType;
  uint16   PerceivedSeverity;
  uint16   ProbableCause;
  string   ProbableCauseDescription;
  datetime EventTime;
  string   OwningEntity;
  string   MessageArguments[];
  string   MessageID;
  string   Message;
};
```

## <a name="members"></a><span data-ttu-id="4b18f-107">Members</span><span class="sxs-lookup"><span data-stu-id="4b18f-107">Members</span></span>

<span data-ttu-id="4b18f-108">La **classe \_ StorageAlert di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="4b18f-108">The **Msvm\_StorageAlert** class has these types of members:</span></span>

-   [<span data-ttu-id="4b18f-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="4b18f-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4b18f-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="4b18f-110">Properties</span></span>

<span data-ttu-id="4b18f-111">La **classe \_ StorageAlert di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="4b18f-111">The **Msvm\_StorageAlert** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4b18f-112">**AlertingElementFormat**</span><span class="sxs-lookup"><span data-stu-id="4b18f-112">**AlertingElementFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4b18f-113">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4b18f-113">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4b18f-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4b18f-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4b18f-115">Qualificatori: **ModelCorrespondence** ("CIM \_ AlertIndication. AlertingManagedElement", "CIM \_ AlertIndication. OtherAlertingElementFormat")</span><span class="sxs-lookup"><span data-stu-id="4b18f-115">Qualifiers: **ModelCorrespondence** ("CIM\_AlertIndication.AlertingManagedElement", "CIM\_AlertIndication.OtherAlertingElementFormat")</span></span>
</dt> </dl>

<span data-ttu-id="4b18f-116">Specifica il formato della proprietà **AlertingManagedElement** .</span><span class="sxs-lookup"><span data-stu-id="4b18f-116">Specifies the format of the **AlertingManagedElement** property.</span></span> <span data-ttu-id="4b18f-117">Il formato è CIMObjectPath, con formato *<NamespacePath> : <ClassName> . <Prop1> = \\ " <Value1> \\ ", " <Prop2> = \\ " <Value2> \\ "*, che specifica un'istanza nello schema CIM.</span><span class="sxs-lookup"><span data-stu-id="4b18f-117">The format is a CIMObjectPath, with the format *<NamespacePath>:<ClassName>.<Prop1>=\\"<Value1>\\", "<Prop2>=\\"<Value2>\\"*, which specifies an instance in the CIM Schema.</span></span>

<span data-ttu-id="4b18f-118">Questa proprietà viene ereditata dalla classe **CIM \_ AlertIndication** .</span><span class="sxs-lookup"><span data-stu-id="4b18f-118">This property is inherited from the **CIM\_AlertIndication** class.</span></span>

<span data-ttu-id="4b18f-119">I valori possibili sono:</span><span class="sxs-lookup"><span data-stu-id="4b18f-119">The possible values are:</span></span>

<dl> <dt>

<span data-ttu-id="4b18f-120"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="4b18f-120"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="4b18f-121"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="4b18f-121"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="4b18f-122"><span id="CIMObjectPath"></span><span id="cimobjectpath"></span><span id="CIMOBJECTPATH"></span>**CIMObjectPath** (2)</span><span class="sxs-lookup"><span data-stu-id="4b18f-122"><span id="CIMObjectPath"></span><span id="cimobjectpath"></span><span id="CIMOBJECTPATH"></span>**CIMObjectPath** (2)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="4b18f-123">**AlertingManagedElement**</span><span class="sxs-lookup"><span data-stu-id="4b18f-123">**AlertingManagedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4b18f-124">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="4b18f-124">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="4b18f-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4b18f-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4b18f-126">Percorsi WMI dell'istanza per la quale viene generato l'avviso.</span><span class="sxs-lookup"><span data-stu-id="4b18f-126">The WMI paths of the instance for which the alert is generated.</span></span>

</dd> <dt>

<span data-ttu-id="4b18f-127">**AlertType**</span><span class="sxs-lookup"><span data-stu-id="4b18f-127">**AlertType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4b18f-128">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4b18f-128">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4b18f-129">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4b18f-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4b18f-130">Specifica la classificazione primaria dell'avviso.</span><span class="sxs-lookup"><span data-stu-id="4b18f-130">Specifies the primary classification of the alert.</span></span> <span data-ttu-id="4b18f-131">I valori possibili per questa proprietà sono:</span><span class="sxs-lookup"><span data-stu-id="4b18f-131">The possible values for this property are:</span></span>

<dl> <dt>

<span data-ttu-id="4b18f-132"><span id="Quality_of_Service_Alert"></span><span id="quality_of_service_alert"></span><span id="QUALITY_OF_SERVICE_ALERT"></span>**Avviso di qualità del servizio** (3)</span><span class="sxs-lookup"><span data-stu-id="4b18f-132"><span id="Quality_of_Service_Alert"></span><span id="quality_of_service_alert"></span><span id="QUALITY_OF_SERVICE_ALERT"></span>**Quality of Service Alert** (3)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="4b18f-133">**EventTime**</span><span class="sxs-lookup"><span data-stu-id="4b18f-133">**EventTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4b18f-134">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="4b18f-134">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="4b18f-135">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4b18f-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4b18f-136">Data e ora in cui è stato rilevato l'evento sottostante.</span><span class="sxs-lookup"><span data-stu-id="4b18f-136">The date and time at which the underlying event was detected.</span></span>

</dd> <dt>

<span data-ttu-id="4b18f-137">**Messaggio**</span><span class="sxs-lookup"><span data-stu-id="4b18f-137">**Message**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4b18f-138">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="4b18f-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4b18f-139">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4b18f-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4b18f-140">Messaggio formattato costruito combinando alcuni o tutti gli elementi dinamici specificati nella proprietà **MessageArguments** con gli elementi statici identificati in modo univoco dalla proprietà **MessageID** in un registro messaggi o in un altro catalogo associato alla proprietà **OwningEntity** .</span><span class="sxs-lookup"><span data-stu-id="4b18f-140">A formatted message that is constructed by combining some or all of the dynamic elements that are specified in the **MessageArguments** property with the static elements uniquely identified by the **MessageID** property in a message registry or other catalog associated with the **OwningEntity** property.</span></span>

</dd> <dt>

<span data-ttu-id="4b18f-141">**MessageArguments**</span><span class="sxs-lookup"><span data-stu-id="4b18f-141">**MessageArguments**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4b18f-142">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="4b18f-142">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="4b18f-143">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4b18f-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4b18f-144">Matrice che contiene il contenuto dinamico del messaggio.</span><span class="sxs-lookup"><span data-stu-id="4b18f-144">An array that contains the dynamic content of the message.</span></span> <span data-ttu-id="4b18f-145">Se il valore di **MessageID** è 32930, l'argomento nella posizione 0 è il **PoolID** dell'istanza di [**MSVM \_ ResourcePool**](msvm-resourcepoolcomponent.md) per la quale viene generato l'avviso.</span><span class="sxs-lookup"><span data-stu-id="4b18f-145">If the value of **MessageID** is 32930, the argument at position 0 is the **PoolID** of the [**Msvm\_ResourcePool**](msvm-resourcepoolcomponent.md) instance for which the alert is generated.</span></span>

</dd> <dt>

<span data-ttu-id="4b18f-146">**MessageID**</span><span class="sxs-lookup"><span data-stu-id="4b18f-146">**MessageID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4b18f-147">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="4b18f-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4b18f-148">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4b18f-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4b18f-149">Identifica in modo univoco, all'interno dell'ambito della proprietà **OwningEntity** , il formato della proprietà del **messaggio** .</span><span class="sxs-lookup"><span data-stu-id="4b18f-149">Uniquely identifies, within the scope of the **OwningEntity** property, the format of the **Message** property.</span></span> <span data-ttu-id="4b18f-150">I valori possibili per questa proprietà sono:</span><span class="sxs-lookup"><span data-stu-id="4b18f-150">The possible values for this property are:</span></span>

<span data-ttu-id="4b18f-151">32930 ("messaggio di velocità effettiva di QoS insufficiente nel pool di archiviazione")</span><span class="sxs-lookup"><span data-stu-id="4b18f-151">32930 ("Storage Pool QoS Insufficient Throughput Message")</span></span>

</dd> <dt>

<span data-ttu-id="4b18f-152">**OtherAlertingElementFormat**</span><span class="sxs-lookup"><span data-stu-id="4b18f-152">**OtherAlertingElementFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4b18f-153">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4b18f-153">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4b18f-154">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4b18f-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4b18f-155">Stringa che definisce i valori "other" per **AlertingManagedElement**.</span><span class="sxs-lookup"><span data-stu-id="4b18f-155">A string that defines "Other" values for **AlertingManagedElement**.</span></span> <span data-ttu-id="4b18f-156">Questo valore deve essere impostato su un valore non NULL quando **AlertingManagedElement** è impostato su un valore pari a 1 ("altro").</span><span class="sxs-lookup"><span data-stu-id="4b18f-156">This value MUST be set to a non NULL value when **AlertingManagedElement** is set to a value of 1 ("Other").</span></span> <span data-ttu-id="4b18f-157">Per tutti gli altri valori di **AlertingManagedElement**, il valore di questa stringa deve essere impostato su null.</span><span class="sxs-lookup"><span data-stu-id="4b18f-157">For all other values of **AlertingManagedElement**, the value of this string must be set to NULL.</span></span>

<span data-ttu-id="4b18f-158">Questa proprietà viene ereditata dalla classe **CIM \_ AlertIndication** .</span><span class="sxs-lookup"><span data-stu-id="4b18f-158">This property is inherited from the **CIM\_AlertIndication** class.</span></span>

</dd> <dt>

<span data-ttu-id="4b18f-159">**OwningEntity**</span><span class="sxs-lookup"><span data-stu-id="4b18f-159">**OwningEntity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4b18f-160">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="4b18f-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4b18f-161">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4b18f-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4b18f-162">Identifica in modo univoco l'entità a cui appartiene la definizione del formato del **messaggio** descritto in questa istanza.</span><span class="sxs-lookup"><span data-stu-id="4b18f-162">Uniquely identifies the entity that owns the definition of the format of the **Message** described in this instance.</span></span> <span data-ttu-id="4b18f-163">Il valore di questa proprietà è sempre "Microsoft-Windows-Hyper-V".</span><span class="sxs-lookup"><span data-stu-id="4b18f-163">The value of this property is always "Microsoft-Windows- Hyper-V."</span></span>

<span data-ttu-id="4b18f-164">"Microsoft-Windows-Hyper-V"</span><span class="sxs-lookup"><span data-stu-id="4b18f-164">"Microsoft-Windows- Hyper-V"</span></span>

</dd> <dt>

<span data-ttu-id="4b18f-165">**PerceivedSeverity**</span><span class="sxs-lookup"><span data-stu-id="4b18f-165">**PerceivedSeverity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4b18f-166">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4b18f-166">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4b18f-167">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4b18f-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4b18f-168">Descrive il livello di gravità dell'indicazione di avviso.</span><span class="sxs-lookup"><span data-stu-id="4b18f-168">Describes the severity of the alert indication.</span></span> <span data-ttu-id="4b18f-169">I valori possibili per questa proprietà sono:</span><span class="sxs-lookup"><span data-stu-id="4b18f-169">The possible values for this property are:</span></span>

<dl> <dt>

<span data-ttu-id="4b18f-170"><span id="Information"></span><span id="information"></span><span id="INFORMATION"></span>**Informazioni** (2)</span><span class="sxs-lookup"><span data-stu-id="4b18f-170"><span id="Information"></span><span id="information"></span><span id="INFORMATION"></span>**Information** (2)</span></span>
</dt> <dt>

<span data-ttu-id="4b18f-171"><span id="Degraded_Warning"></span><span id="degraded_warning"></span><span id="DEGRADED_WARNING"></span>**Danneggiato/avviso** (3)</span><span class="sxs-lookup"><span data-stu-id="4b18f-171"><span id="Degraded_Warning"></span><span id="degraded_warning"></span><span id="DEGRADED_WARNING"></span>**Degraded/Warning** (3)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="4b18f-172">**ProbableCause**</span><span class="sxs-lookup"><span data-stu-id="4b18f-172">**ProbableCause**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4b18f-173">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4b18f-173">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4b18f-174">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4b18f-174">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4b18f-175">Descrive la causa probabile della situazione che ha generato l'indicazione di avviso.</span><span class="sxs-lookup"><span data-stu-id="4b18f-175">Describes the probable cause of the situation that resulted in the alert indication.</span></span>

<dl> <dt>

<span data-ttu-id="4b18f-176"><span id="Storage_Capacity_Problem"></span><span id="storage_capacity_problem"></span><span id="STORAGE_CAPACITY_PROBLEM"></span>**Problema di capacità di archiviazione** (50)</span><span class="sxs-lookup"><span data-stu-id="4b18f-176"><span id="Storage_Capacity_Problem"></span><span id="storage_capacity_problem"></span><span id="STORAGE_CAPACITY_PROBLEM"></span>**Storage Capacity Problem** (50)</span></span>
</dt> <dt>

<span data-ttu-id="4b18f-177"><span id="Previous_Alert_Cleared"></span><span id="previous_alert_cleared"></span><span id="PREVIOUS_ALERT_CLEARED"></span>**Avviso precedente cancellato** (59)</span><span class="sxs-lookup"><span data-stu-id="4b18f-177"><span id="Previous_Alert_Cleared"></span><span id="previous_alert_cleared"></span><span id="PREVIOUS_ALERT_CLEARED"></span>**Previous Alert Cleared** (59)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="4b18f-178">**ProbableCauseDescription**</span><span class="sxs-lookup"><span data-stu-id="4b18f-178">**ProbableCauseDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4b18f-179">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="4b18f-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4b18f-180">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4b18f-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4b18f-181">Descrizione testuale che corrisponde al valore della proprietà **ProbableCause** .</span><span class="sxs-lookup"><span data-stu-id="4b18f-181">A textual description that corresponds to the value of the **ProbableCause** property.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4b18f-182">Commenti</span><span class="sxs-lookup"><span data-stu-id="4b18f-182">Remarks</span></span>

<span data-ttu-id="4b18f-183">Il provider WMI Hyper-V non genera eventi per i singoli dischi virtuali, in modo da evitare che i client vengano sovraccaricati con eventi in caso di malfunzionamenti su larga scala dei sistemi di archiviazione sottostanti.</span><span class="sxs-lookup"><span data-stu-id="4b18f-183">The Hyper-V WMI provider won't raise events for individual virtual disks to avoid flooding clients with events in case of large scale malfunctions of the underlying storage systems.</span></span>

<span data-ttu-id="4b18f-184">Quando un client riceve un evento **MSVM \_ StorageAlert** , se il valore della proprietà **ProbableCause** è 50 (problema di capacità di archiviazione), il client può individuare i dischi virtuali che operano al di fuori dei criteri QoS usando una di queste procedure:</span><span class="sxs-lookup"><span data-stu-id="4b18f-184">When a client receives an **Msvm\_StorageAlert** event, if the value of the **ProbableCause** property is 50 ( Storage Capacity Problem ), the client can discover which virtual disks are operating outside their QoS policy by using one of these procedures:</span></span>

-   <span data-ttu-id="4b18f-185">Eseguire una query su tutte le istanze di [**\_ disco logico MSVM**](msvm-logicaldisk.md) allocate dal pool di risorse per il quale è stato generato l'evento.</span><span class="sxs-lookup"><span data-stu-id="4b18f-185">Query all the [**Msvm\_LogicalDisk**](msvm-logicaldisk.md) instances that were allocated from the resource pool for which the event was generated.</span></span> <span data-ttu-id="4b18f-186">Queste **istanze \_ disco logico di MSVM** sono associate al pool di risorse tramite l'associazione [**MSVM \_ ElementAllocatedFromPool**](msvm-elementallocatedfrompool.md) .</span><span class="sxs-lookup"><span data-stu-id="4b18f-186">These **Msvm\_LogicalDisk** instances are associated to the resource pool via the [**Msvm\_ElementAllocatedFromPool**](msvm-elementallocatedfrompool.md) association.</span></span>
-   <span data-ttu-id="4b18f-187">Filtrare l'elenco dei risultati selezionando le istanze il cui OperationalStatus contiene una velocità effettiva insufficiente.</span><span class="sxs-lookup"><span data-stu-id="4b18f-187">Filter the result list by selecting instances whose OperationalStatus contains  Insufficient Throughput .</span></span>

## <a name="requirements"></a><span data-ttu-id="4b18f-188">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4b18f-188">Requirements</span></span>



| <span data-ttu-id="4b18f-189">Requisito</span><span class="sxs-lookup"><span data-stu-id="4b18f-189">Requirement</span></span> | <span data-ttu-id="4b18f-190">Valore</span><span class="sxs-lookup"><span data-stu-id="4b18f-190">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b18f-191">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4b18f-191">Minimum supported client</span></span><br/> | <span data-ttu-id="4b18f-192">Windows 8.1 \[ solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="4b18f-192">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="4b18f-193">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4b18f-193">Minimum supported server</span></span><br/> | <span data-ttu-id="4b18f-194">Solo app desktop Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="4b18f-194">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="4b18f-195">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="4b18f-195">Namespace</span></span><br/>                | <span data-ttu-id="4b18f-196">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="4b18f-196">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="4b18f-197">MOF</span><span class="sxs-lookup"><span data-stu-id="4b18f-197">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4b18f-198"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4b18f-198"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4b18f-199">DLL</span><span class="sxs-lookup"><span data-stu-id="4b18f-199">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4b18f-200"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4b18f-200"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="4b18f-201">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4b18f-201">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b18f-202">**\_ALERTINDICATION CIM**</span><span class="sxs-lookup"><span data-stu-id="4b18f-202">**CIM\_AlertIndication**</span></span>](cim-alertindication.md)
</dt> <dt>

[<span data-ttu-id="4b18f-203">**\_Disco logico MSVM**</span><span class="sxs-lookup"><span data-stu-id="4b18f-203">**Msvm\_LogicalDisk**</span></span>](msvm-logicaldisk.md)
</dt> <dt>

[<span data-ttu-id="4b18f-204">**\_ResourcePool MSVM**</span><span class="sxs-lookup"><span data-stu-id="4b18f-204">**Msvm\_ResourcePool**</span></span>](msvm-resourcepoolcomponent.md)
</dt> </dl>

 

 




