---
description: Rappresenta un punto di riferimento per un sistema virtuale.
ms.assetid: b3ba4fa7-3b77-4a1d-ab8f-d38af12ab5dd
title: Classe Msvm_VirtualSystemReferencePoint
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePoint
- Msvm_VirtualSystemReferencePoint.InstanceID
- Msvm_VirtualSystemReferencePoint.ReferencePointType
- Msvm_VirtualSystemReferencePoint.ConsistencyLevel
- Msvm_VirtualSystemReferencePoint.VirtualSystemIdentifier
- Msvm_VirtualSystemReferencePoint.HasAssociatedData
- Msvm_VirtualSystemReferencePoint.VirtualDiskIdentifiers
- Msvm_VirtualSystemReferencePoint.ResilientChangeTrackingIdentifiers
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: add160cf44a592462634704ddf783cd8f4084068
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320727"
---
# <a name="msvm_virtualsystemreferencepoint-class"></a><span data-ttu-id="6f7e3-103">\_Classe MSVM VirtualSystemReferencePoint</span><span class="sxs-lookup"><span data-stu-id="6f7e3-103">Msvm\_VirtualSystemReferencePoint class</span></span>

<span data-ttu-id="6f7e3-104">Rappresenta un punto di riferimento per un sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="6f7e3-104">Represents a reference point for a virtual system.</span></span>

<span data-ttu-id="6f7e3-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="6f7e3-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f7e3-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6f7e3-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemReferencePoint : CIM_ManagedElement
{
  string  InstanceID;
  uint16  ReferencePointType;
  uint16  ConsistencyLevel;
  string  VirtualSystemIdentifier;
  boolean HasAssociatedData;
  string  VirtualDiskIdentifiers[];
  string  ResilientChangeTrackingIdentifiers[];
};
```

## <a name="members"></a><span data-ttu-id="6f7e3-107">Members</span><span class="sxs-lookup"><span data-stu-id="6f7e3-107">Members</span></span>

<span data-ttu-id="6f7e3-108">La **classe \_ VirtualSystemReferencePoint di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="6f7e3-108">The **Msvm\_VirtualSystemReferencePoint** class has these types of members:</span></span>

-   [<span data-ttu-id="6f7e3-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="6f7e3-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6f7e3-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="6f7e3-110">Properties</span></span>

<span data-ttu-id="6f7e3-111">La **classe \_ VirtualSystemReferencePoint di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="6f7e3-111">The **Msvm\_VirtualSystemReferencePoint** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6f7e3-112">**ConsistencyLevel**</span><span class="sxs-lookup"><span data-stu-id="6f7e3-112">**ConsistencyLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f7e3-113">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6f7e3-113">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6f7e3-114">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="6f7e3-114">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="6f7e3-115">Livello di coerenza del punto di riferimento.</span><span class="sxs-lookup"><span data-stu-id="6f7e3-115">The consistency level of the reference point.</span></span>

<dt>

<span id="Application_Consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>

<span data-ttu-id="6f7e3-116"><span id="Application_Consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>**Coerente** con l'applicazione (1)</span><span class="sxs-lookup"><span data-stu-id="6f7e3-116"><span id="Application_Consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>**Application Consistent** (1)</span></span>


</dt> <dd>

<span data-ttu-id="6f7e3-117">Il punto di riferimento indica un punto nel tempo in cui il sistema virtuale era in uno stato coerente con l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="6f7e3-117">The reference point indicates a point in time when the virtual system was in application consistent state.</span></span>

</dd> <dt>

<span id="Crash_Consistent"></span><span id="crash_consistent"></span><span id="CRASH_CONSISTENT"></span>

<span data-ttu-id="6f7e3-118"><span id="Crash_Consistent"></span><span id="crash_consistent"></span><span id="CRASH_CONSISTENT"></span>**Coerente con l'arresto anomalo** (2)</span><span class="sxs-lookup"><span data-stu-id="6f7e3-118"><span id="Crash_Consistent"></span><span id="crash_consistent"></span><span id="CRASH_CONSISTENT"></span>**Crash Consistent** (2)</span></span>


</dt> <dd>

<span data-ttu-id="6f7e3-119">Il punto di riferimento indica un punto nel tempo in cui il sistema virtuale si trova in uno stato di arresto anomalo.</span><span class="sxs-lookup"><span data-stu-id="6f7e3-119">The reference point indicates a point in time when the virtual system was in crash consistent state.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="6f7e3-120">**HasAssociatedData**</span><span class="sxs-lookup"><span data-stu-id="6f7e3-120">**HasAssociatedData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f7e3-121">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="6f7e3-121">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6f7e3-122">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="6f7e3-122">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="6f7e3-123">Impostare su **true** se il punto di riferimento dispone di dati associati.</span><span class="sxs-lookup"><span data-stu-id="6f7e3-123">Set to **true** if the reference point has associated data.</span></span> <span data-ttu-id="6f7e3-124">Questa operazione è valida solo per i punti di riferimento basati su log.</span><span class="sxs-lookup"><span data-stu-id="6f7e3-124">This is valid only for log based reference points.</span></span> <span data-ttu-id="6f7e3-125">Per i punti di riferimento basati su RCT, **HasAssociatedData** è impostato su **false**.</span><span class="sxs-lookup"><span data-stu-id="6f7e3-125">For RCT-based reference points, **HasAssociatedData** is set to **false**.</span></span> <span data-ttu-id="6f7e3-126">Per i punti di riferimento basati su log, dopo l'eliminazione del log **HasAssociatedData** diventa **false**.</span><span class="sxs-lookup"><span data-stu-id="6f7e3-126">For log based reference points, once the log is discarded **HasAssociatedData** becomes **false**.</span></span>

</dd> <dt>

<span data-ttu-id="6f7e3-127">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="6f7e3-127">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f7e3-128">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6f7e3-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6f7e3-129">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6f7e3-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f7e3-130">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("InstanceId"), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="6f7e3-130">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("InstanceID"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="6f7e3-131">Identificazione univoca di un oggetto punto di riferimento.</span><span class="sxs-lookup"><span data-stu-id="6f7e3-131">Unique identification of a reference point object.</span></span>

</dd> <dt>

<span data-ttu-id="6f7e3-132">**ReferencePointType**</span><span class="sxs-lookup"><span data-stu-id="6f7e3-132">**ReferencePointType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f7e3-133">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6f7e3-133">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6f7e3-134">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="6f7e3-134">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="6f7e3-135">Indica il tipo del punto di riferimento.</span><span class="sxs-lookup"><span data-stu-id="6f7e3-135">Indicates the type of the reference point.</span></span>

<dt>

<span id="Log_based"></span><span id="log_based"></span><span id="LOG_BASED"></span>

<span data-ttu-id="6f7e3-136"><span id="Log_based"></span><span id="log_based"></span><span id="LOG_BASED"></span>**Basato su log** (1)</span><span class="sxs-lookup"><span data-stu-id="6f7e3-136"><span id="Log_based"></span><span id="log_based"></span><span id="LOG_BASED"></span>**Log based** (1)</span></span>


</dt> <dd>

<span data-ttu-id="6f7e3-137">Rilevamento del log della replica Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="6f7e3-137">Hyper-V replica log tracking.</span></span>

</dd> <dt>

<span id="RCT_based"></span><span id="rct_based"></span><span id="RCT_BASED"></span>

<span data-ttu-id="6f7e3-138"><span id="RCT_based"></span><span id="rct_based"></span><span id="RCT_BASED"></span>**Basato su RCT** (2)</span><span class="sxs-lookup"><span data-stu-id="6f7e3-138"><span id="RCT_based"></span><span id="rct_based"></span><span id="RCT_BASED"></span>**RCT based** (2)</span></span>


</dt> <dd>

<span data-ttu-id="6f7e3-139">Basato su Rilevamento modifiche resiliente di dischi virtuali.</span><span class="sxs-lookup"><span data-stu-id="6f7e3-139">Based on Resilient Change Tracking of virtual disks.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="6f7e3-140">**ResilientChangeTrackingIdentifiers**</span><span class="sxs-lookup"><span data-stu-id="6f7e3-140">**ResilientChangeTrackingIdentifiers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f7e3-141">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="6f7e3-141">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="6f7e3-142">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6f7e3-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f7e3-143">Matrice di ID RCT corrispondente ai dischi virtuali della macchina virtuale al momento della creazione del punto di riferimento.</span><span class="sxs-lookup"><span data-stu-id="6f7e3-143">An array of RCT IDs corresponding to the virtual disks of the VM at the time this reference point was created.</span></span> <span data-ttu-id="6f7e3-144">Questo campo è valido solo per i punti di riferimento basati su RCT.</span><span class="sxs-lookup"><span data-stu-id="6f7e3-144">This field is valid only for RCT-based reference points.</span></span>

</dd> <dt>

<span data-ttu-id="6f7e3-145">**VirtualDiskIdentifiers**</span><span class="sxs-lookup"><span data-stu-id="6f7e3-145">**VirtualDiskIdentifiers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f7e3-146">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="6f7e3-146">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="6f7e3-147">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6f7e3-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f7e3-148">Matrice di ID di istanza WMI corrispondente ai dischi virtuali della macchina virtuale al momento della creazione del punto di riferimento.</span><span class="sxs-lookup"><span data-stu-id="6f7e3-148">An array of WMI instance IDs corresponding to the virtual disks of the VM at the time this reference point was created.</span></span> <span data-ttu-id="6f7e3-149">A questi dischi virtuali sono associati ID RCT.</span><span class="sxs-lookup"><span data-stu-id="6f7e3-149">These virtual disks have RCT IDs associated with them.</span></span>

</dd> <dt>

<span data-ttu-id="6f7e3-150">**VirtualSystemIdentifier**</span><span class="sxs-lookup"><span data-stu-id="6f7e3-150">**VirtualSystemIdentifier**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f7e3-151">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6f7e3-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6f7e3-152">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6f7e3-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f7e3-153">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**Nome**")</span><span class="sxs-lookup"><span data-stu-id="6f7e3-153">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**Name**")</span></span>
</dt> </dl>

<span data-ttu-id="6f7e3-154">Nome del [**\_ ComputerSystem CIM**](cim-computersystem.md) a cui appartiene il punto di riferimento</span><span class="sxs-lookup"><span data-stu-id="6f7e3-154">The name of the [**CIM\_ComputerSystem**](cim-computersystem.md) to which this reference point belongs</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6f7e3-155">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6f7e3-155">Requirements</span></span>



| <span data-ttu-id="6f7e3-156">Requisito</span><span class="sxs-lookup"><span data-stu-id="6f7e3-156">Requirement</span></span> | <span data-ttu-id="6f7e3-157">Valore</span><span class="sxs-lookup"><span data-stu-id="6f7e3-157">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f7e3-158">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6f7e3-158">Minimum supported client</span></span><br/> | <span data-ttu-id="6f7e3-159">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="6f7e3-159">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="6f7e3-160">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6f7e3-160">Minimum supported server</span></span><br/> | <span data-ttu-id="6f7e3-161">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="6f7e3-161">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="6f7e3-162">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="6f7e3-162">Namespace</span></span><br/>                | <span data-ttu-id="6f7e3-163">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="6f7e3-163">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="6f7e3-164">MOF</span><span class="sxs-lookup"><span data-stu-id="6f7e3-164">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6f7e3-165"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6f7e3-165"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6f7e3-166">DLL</span><span class="sxs-lookup"><span data-stu-id="6f7e3-166">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6f7e3-167"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6f7e3-167"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="6f7e3-168">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6f7e3-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f7e3-169">**\_ManagementName CIM**</span><span class="sxs-lookup"><span data-stu-id="6f7e3-169">**CIM\_ManagedElement**</span></span>](cim-managedelement.md)
</dt> </dl>

 

