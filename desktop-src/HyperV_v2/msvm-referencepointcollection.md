---
description: Rappresenta una raccolta di punti di riferimento del sistema virtuale.
ms.assetid: dc293f94-a683-468f-af05-ba99824d773e
title: Classe Msvm_ReferencePointCollection
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReferencePointCollection
- Msvm_ReferencePointCollection.CollectionID
- Msvm_ReferencePointCollection.ElementName
- Msvm_ReferencePointCollection.ReferencePointType
- Msvm_ReferencePointCollection.ConsistencyLevel
- Msvm_ReferencePointCollection.VirtualSystemCollectionId
- Msvm_ReferencePointCollection.HasAssociatedLog
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 570590221ee8568d78e150fec3c359365c8434cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882169"
---
# <a name="msvm_referencepointcollection-class"></a><span data-ttu-id="0f0da-103">\_Classe MSVM ReferencePointCollection</span><span class="sxs-lookup"><span data-stu-id="0f0da-103">Msvm\_ReferencePointCollection class</span></span>

<span data-ttu-id="0f0da-104">Rappresenta una raccolta di punti di riferimento del sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="0f0da-104">Represents a collection of virtual system reference points.</span></span>

<span data-ttu-id="0f0da-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="0f0da-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f0da-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0f0da-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ReferencePointCollection : CIM_Collection
{
  string  CollectionID;
  string  ElementName;
  uint16  ReferencePointType;
  uint16  ConsistencyLevel;
  string  VirtualSystemCollectionId;
  boolean HasAssociatedLog;
};
```

## <a name="members"></a><span data-ttu-id="0f0da-107">Members</span><span class="sxs-lookup"><span data-stu-id="0f0da-107">Members</span></span>

<span data-ttu-id="0f0da-108">La **classe \_ ReferencePointCollection di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="0f0da-108">The **Msvm\_ReferencePointCollection** class has these types of members:</span></span>

-   [<span data-ttu-id="0f0da-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="0f0da-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0f0da-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="0f0da-110">Properties</span></span>

<span data-ttu-id="0f0da-111">La **classe \_ ReferencePointCollection di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="0f0da-111">The **Msvm\_ReferencePointCollection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0f0da-112">**CollectionID**</span><span class="sxs-lookup"><span data-stu-id="0f0da-112">**CollectionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f0da-113">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0f0da-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f0da-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0f0da-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f0da-115">Qualificatori: [**chiave**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CollectionId"), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="0f0da-115">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CollectionID"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="0f0da-116">Identificazione univoca dell'oggetto raccolta.</span><span class="sxs-lookup"><span data-stu-id="0f0da-116">The unique identification of the collection object.</span></span>

</dd> <dt>

<span data-ttu-id="0f0da-117">**ConsistencyLevel**</span><span class="sxs-lookup"><span data-stu-id="0f0da-117">**ConsistencyLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f0da-118">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0f0da-118">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0f0da-119">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="0f0da-119">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0f0da-120">Livello di coerenza del punto di riferimento.</span><span class="sxs-lookup"><span data-stu-id="0f0da-120">Consistency level of the reference point.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0f0da-121"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="0f0da-121"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Crash_Consistent"></span><span id="crash_consistent"></span><span id="CRASH_CONSISTENT"></span>

<span data-ttu-id="0f0da-122"><span id="Crash_Consistent"></span><span id="crash_consistent"></span><span id="CRASH_CONSISTENT"></span>**Coerente con l'arresto anomalo** (1)</span><span class="sxs-lookup"><span data-stu-id="0f0da-122"><span id="Crash_Consistent"></span><span id="crash_consistent"></span><span id="CRASH_CONSISTENT"></span>**Crash Consistent** (1)</span></span>


</dt> <dd>

<span data-ttu-id="0f0da-123">Il punto di riferimento indica un punto nel tempo in cui il sistema virtuale si trova in uno stato di arresto anomalo.</span><span class="sxs-lookup"><span data-stu-id="0f0da-123">The reference point indicates a point in time when the virtual system was in crash consistent state.</span></span>

</dd> <dt>

<span id="Application_Consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>

<span data-ttu-id="0f0da-124"><span id="Application_Consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>**Coerente** con l'applicazione (2)</span><span class="sxs-lookup"><span data-stu-id="0f0da-124"><span id="Application_Consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>**Application Consistent** (2)</span></span>


</dt> <dd>

<span data-ttu-id="0f0da-125">Il punto di riferimento indica un punto nel tempo in cui il sistema virtuale era in uno stato coerente con l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="0f0da-125">The reference point indicates a point in time when the virtual system was in application consistent state.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0f0da-126">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="0f0da-126">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f0da-127">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0f0da-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f0da-128">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0f0da-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f0da-129">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ElementName")</span><span class="sxs-lookup"><span data-stu-id="0f0da-129">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ElementName")</span></span>
</dt> </dl>

<span data-ttu-id="0f0da-130">Nome definito dall'utente per la raccolta.</span><span class="sxs-lookup"><span data-stu-id="0f0da-130">An user-defined name for the collection.</span></span> <span data-ttu-id="0f0da-131">Si noti che non è garantito che sia univoco.</span><span class="sxs-lookup"><span data-stu-id="0f0da-131">Note this is not guaranteed to be unique.</span></span>

</dd> <dt>

<span data-ttu-id="0f0da-132">**HasAssociatedLog**</span><span class="sxs-lookup"><span data-stu-id="0f0da-132">**HasAssociatedLog**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f0da-133">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="0f0da-133">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0f0da-134">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="0f0da-134">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0f0da-135">**true** se a tutti i punti di riferimento del membro sono associati log.</span><span class="sxs-lookup"><span data-stu-id="0f0da-135">**true** if all the member reference points have associated logs.</span></span> <span data-ttu-id="0f0da-136">Questa operazione è valida solo per i punti di riferimento basati su log.</span><span class="sxs-lookup"><span data-stu-id="0f0da-136">This is valid only for log based reference points.</span></span> <span data-ttu-id="0f0da-137">Per i punti di riferimento basati su RCT, **HasAssociatedLog** è impostato su **false**.</span><span class="sxs-lookup"><span data-stu-id="0f0da-137">For RCT based reference points, **HasAssociatedLog** is set to **false**.</span></span> <span data-ttu-id="0f0da-138">Per i punti di riferimento basati su log, dopo l'eliminazione del log **HasAssociatedLog** diventa **false**.</span><span class="sxs-lookup"><span data-stu-id="0f0da-138">For log based reference points, once the log is discarded **HasAssociatedLog** becomes **false**.</span></span>

</dd> <dt>

<span data-ttu-id="0f0da-139">**ReferencePointType**</span><span class="sxs-lookup"><span data-stu-id="0f0da-139">**ReferencePointType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f0da-140">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0f0da-140">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0f0da-141">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0f0da-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f0da-142">Qualificatori: [ **in**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="0f0da-142">Qualifiers: [**In**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="0f0da-143">Indica il tipo del punto di riferimento.</span><span class="sxs-lookup"><span data-stu-id="0f0da-143">Indicates the type of the reference point.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0f0da-144"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="0f0da-144"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Log_based"></span><span id="log_based"></span><span id="LOG_BASED"></span>

<span data-ttu-id="0f0da-145"><span id="Log_based"></span><span id="log_based"></span><span id="LOG_BASED"></span>**Basato su log** (1)</span><span class="sxs-lookup"><span data-stu-id="0f0da-145"><span id="Log_based"></span><span id="log_based"></span><span id="LOG_BASED"></span>**Log based** (1)</span></span>


</dt> <dd>

<span data-ttu-id="0f0da-146">Rilevamento del log della replica Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="0f0da-146">Hyper-V replica log tracking.</span></span>

</dd> <dt>

<span id="RCT_based"></span><span id="rct_based"></span><span id="RCT_BASED"></span>

<span data-ttu-id="0f0da-147"><span id="RCT_based"></span><span id="rct_based"></span><span id="RCT_BASED"></span>**Basato su RCT** (2)</span><span class="sxs-lookup"><span data-stu-id="0f0da-147"><span id="RCT_based"></span><span id="rct_based"></span><span id="RCT_BASED"></span>**RCT based** (2)</span></span>


</dt> <dd>

<span data-ttu-id="0f0da-148">Basato su Rilevamento modifiche resiliente di dischi virtuali.</span><span class="sxs-lookup"><span data-stu-id="0f0da-148">Based on Resilient Change Tracking of virtual disks.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="0f0da-149"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="0f0da-149"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

<span data-ttu-id="0f0da-150"><span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>**Specifico del fornitore** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="0f0da-150"><span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>**Vendor Specific** (32768..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0f0da-151">**VirtualSystemCollectionId**</span><span class="sxs-lookup"><span data-stu-id="0f0da-151">**VirtualSystemCollectionId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f0da-152">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0f0da-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f0da-153">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0f0da-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f0da-154">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**MSVM \_ VirtualSystemCollection**](msvm-virtualsystemcollection.md).**CollectionID**")</span><span class="sxs-lookup"><span data-stu-id="0f0da-154">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**Msvm\_VirtualSystemCollection**](msvm-virtualsystemcollection.md).**CollectionID**")</span></span>
</dt> </dl>

<span data-ttu-id="0f0da-155">Identificatore del [**\_ VirtualSystemCollection MSVM**](msvm-virtualsystemcollection.md) a cui appartiene il punto di riferimento.</span><span class="sxs-lookup"><span data-stu-id="0f0da-155">The identifier of the [**Msvm\_VirtualSystemCollection**](msvm-virtualsystemcollection.md) to which this reference point belongs.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0f0da-156">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0f0da-156">Requirements</span></span>



| <span data-ttu-id="0f0da-157">Requisito</span><span class="sxs-lookup"><span data-stu-id="0f0da-157">Requirement</span></span> | <span data-ttu-id="0f0da-158">Valore</span><span class="sxs-lookup"><span data-stu-id="0f0da-158">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f0da-159">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0f0da-159">Minimum supported client</span></span><br/> | <span data-ttu-id="0f0da-160">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="0f0da-160">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="0f0da-161">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0f0da-161">Minimum supported server</span></span><br/> | <span data-ttu-id="0f0da-162">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="0f0da-162">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="0f0da-163">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="0f0da-163">Namespace</span></span><br/>                | <span data-ttu-id="0f0da-164">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="0f0da-164">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="0f0da-165">MOF</span><span class="sxs-lookup"><span data-stu-id="0f0da-165">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0f0da-166"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0f0da-166"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0f0da-167">DLL</span><span class="sxs-lookup"><span data-stu-id="0f0da-167">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0f0da-168"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0f0da-168"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="0f0da-169">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0f0da-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f0da-170">**\_Raccolta CIM**</span><span class="sxs-lookup"><span data-stu-id="0f0da-170">**CIM\_Collection**</span></span>](cim-collection.md)
</dt> </dl>

 

