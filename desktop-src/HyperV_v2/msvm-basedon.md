---
description: Associazione che descrive come possono essere assemblati gli extent di archiviazione dagli extent di livello inferiore.
ms.assetid: 8be9bb2c-ef46-454b-bfc3-0398c64d17b7
title: Classe Msvm_BasedOn
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_BasedOn
- Msvm_BasedOn.Antecedent
- Msvm_BasedOn.Dependent
- Msvm_BasedOn.StartingAddress
- Msvm_BasedOn.EndingAddress
- Msvm_BasedOn.OrderIndex
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8262ae5e510574bf02630410b584d9df10d64ecf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317208"
---
# <a name="msvm_basedon-class"></a><span data-ttu-id="52bc1-103">\_Classe MSVM BasedOn</span><span class="sxs-lookup"><span data-stu-id="52bc1-103">Msvm\_BasedOn class</span></span>

<span data-ttu-id="52bc1-104">Associazione che descrive come possono essere assemblati gli extent di archiviazione dagli extent di livello inferiore.</span><span class="sxs-lookup"><span data-stu-id="52bc1-104">An association that describes how storage extents can be assembled from lower level extents.</span></span> <span data-ttu-id="52bc1-105">Ad esempio, ProtectedSpaceExtents sono parti di PhysicalExtents, mentre VolumeSets vengono assemblati da uno o più fisici o ProtectedSpaceExtents.</span><span class="sxs-lookup"><span data-stu-id="52bc1-105">For example, ProtectedSpaceExtents are parts of PhysicalExtents, while VolumeSets are assembled from one or more Physical or ProtectedSpaceExtents.</span></span> <span data-ttu-id="52bc1-106">Come altro esempio, CacheMemory può essere definito in modo indipendente e realizzato in un oggetto PhysicalElement oppure può essere basato su volatile o NonVolatileStorageExtents.</span><span class="sxs-lookup"><span data-stu-id="52bc1-106">As another example, CacheMemory can be defined independently and realized in a PhysicalElement or can be based on Volatile or NonVolatileStorageExtents.</span></span>

<span data-ttu-id="52bc1-107">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="52bc1-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="52bc1-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="52bc1-108">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_BasedOn : CIM_BasedOn
{
  CIM_StorageExtent REF Antecedent;
  CIM_StorageExtent REF Dependent;
  uint64                StartingAddress;
  uint64                EndingAddress;
  uint16                OrderIndex;
};
```

## <a name="members"></a><span data-ttu-id="52bc1-109">Members</span><span class="sxs-lookup"><span data-stu-id="52bc1-109">Members</span></span>

<span data-ttu-id="52bc1-110">La **classe \_ BasedOn di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="52bc1-110">The **Msvm\_BasedOn** class has these types of members:</span></span>

-   [<span data-ttu-id="52bc1-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="52bc1-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="52bc1-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="52bc1-112">Properties</span></span>

<span data-ttu-id="52bc1-113">La **classe \_ BasedOn di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="52bc1-113">The **Msvm\_BasedOn** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="52bc1-114">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="52bc1-114">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52bc1-115">Tipo di dati: **[ **CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)**</span><span class="sxs-lookup"><span data-stu-id="52bc1-115">Data type: **[**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)**</span></span>
</dt> <dt>

<span data-ttu-id="52bc1-116">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="52bc1-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="52bc1-117">Extent di archiviazione di livello inferiore.</span><span class="sxs-lookup"><span data-stu-id="52bc1-117">The lower level storage extent.</span></span> <span data-ttu-id="52bc1-118">Questa proprietà viene ereditata da [**CIM \_ BasedOn**](/windows/desktop/CIMWin32Prov/cim-basedon).</span><span class="sxs-lookup"><span data-stu-id="52bc1-118">This property is inherited from [**CIM\_BasedOn**](/windows/desktop/CIMWin32Prov/cim-basedon).</span></span>

</dd> <dt>

<span data-ttu-id="52bc1-119">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="52bc1-119">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52bc1-120">Tipo di dati: **[ **CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)**</span><span class="sxs-lookup"><span data-stu-id="52bc1-120">Data type: **[**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)**</span></span>
</dt> <dt>

<span data-ttu-id="52bc1-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="52bc1-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="52bc1-122">Extent di archiviazione di livello superiore.</span><span class="sxs-lookup"><span data-stu-id="52bc1-122">The higher level storage extent.</span></span> <span data-ttu-id="52bc1-123">Questa proprietà viene ereditata da [**CIM \_ BasedOn**](/windows/desktop/CIMWin32Prov/cim-basedon).</span><span class="sxs-lookup"><span data-stu-id="52bc1-123">This property is inherited from [**CIM\_BasedOn**](/windows/desktop/CIMWin32Prov/cim-basedon).</span></span>

</dd> <dt>

<span data-ttu-id="52bc1-124">**EndingAddress**</span><span class="sxs-lookup"><span data-stu-id="52bc1-124">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52bc1-125">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="52bc1-125">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="52bc1-126">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="52bc1-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="52bc1-127">Indirizzo finale in cui termina, nell'archiviazione di livello inferiore, l'extent di livello superiore.</span><span class="sxs-lookup"><span data-stu-id="52bc1-127">The ending address where, in lower level storage, the higher level extent ends.</span></span> <span data-ttu-id="52bc1-128">Questa proprietà è utile quando si esegue il mapping di extent non contigui in un raggruppamento di livello superiore.</span><span class="sxs-lookup"><span data-stu-id="52bc1-128">This property is useful when mapping non-contiguous extents into a higher level grouping.</span></span> <span data-ttu-id="52bc1-129">Questa proprietà viene ereditata da [**CIM \_ BasedOn**](/windows/desktop/CIMWin32Prov/cim-basedon).</span><span class="sxs-lookup"><span data-stu-id="52bc1-129">This property is inherited from [**CIM\_BasedOn**](/windows/desktop/CIMWin32Prov/cim-basedon).</span></span>

</dd> <dt>

<span data-ttu-id="52bc1-130">**OrderIndex**</span><span class="sxs-lookup"><span data-stu-id="52bc1-130">**OrderIndex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52bc1-131">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="52bc1-131">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="52bc1-132">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="52bc1-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="52bc1-133">Se è presente un ordine per l'oggetto in base alle associazioni che descrivono come viene assemblato un extent di archiviazione di livello superiore, la proprietà **OrderIndex** indica questa.</span><span class="sxs-lookup"><span data-stu-id="52bc1-133">If there is an order to the based on associations that describe how a higher level storage extent is assembled, the **OrderIndex** property indicates this.</span></span> <span data-ttu-id="52bc1-134">Quando esiste un ordine, le istanze con lo stesso valore **dipendente** (lo stesso extent di livello superiore) devono inserire valori univoci nella proprietà **OrderIndex** .</span><span class="sxs-lookup"><span data-stu-id="52bc1-134">When an order exists, the instances with the same **Dependent** value (the same higher level extent) should place unique values in the **OrderIndex** property.</span></span> <span data-ttu-id="52bc1-135">Il valore più basso implica il primo membro della raccolta di extent di livello inferiore e i valori crescenti implicano i membri successivi della raccolta.</span><span class="sxs-lookup"><span data-stu-id="52bc1-135">The lowest value implies the first member of the collection of lower level extents, and increasing values imply successive members of the collection.</span></span> <span data-ttu-id="52bc1-136">Se non è presente alcuna relazione ordinata, è necessario specificare un valore pari a zero.</span><span class="sxs-lookup"><span data-stu-id="52bc1-136">If there is no ordered relationship, a value of zero should be specified.</span></span> <span data-ttu-id="52bc1-137">Un esempio di utilizzo di questa proprietà è la definizione di una matrice con striping RAID 0 di tre dischi.</span><span class="sxs-lookup"><span data-stu-id="52bc1-137">An example of the use of this property is to define a RAID-0 striped array of three disks.</span></span> <span data-ttu-id="52bc1-138">La matrice RAID risultante è un extent di archiviazione che dipende dagli extent di archiviazione che descrivono ognuno dei tre dischi.</span><span class="sxs-lookup"><span data-stu-id="52bc1-138">The resultant RAID array is a storage extent that is dependent on the storage extents that describe each of the three disks.</span></span> <span data-ttu-id="52bc1-139">Per indicare l'ordine in cui vengono usati gli extent del disco per accedere ai dati RAID, è possibile specificare il **OrderIndex** di ogni associazione tra gli extent del disco e la matrice RAID come 1, 2 e 3.</span><span class="sxs-lookup"><span data-stu-id="52bc1-139">The **OrderIndex** of each association from the disk extents to the RAID array could be specified as 1, 2, and 3 to indicate the order in which the disk extents are used to access the RAID data.</span></span> <span data-ttu-id="52bc1-140">Questa proprietà viene ereditata da [**CIM \_ BasedOn**](/windows/desktop/CIMWin32Prov/cim-basedon).</span><span class="sxs-lookup"><span data-stu-id="52bc1-140">This property is inherited from [**CIM\_BasedOn**](/windows/desktop/CIMWin32Prov/cim-basedon).</span></span>

</dd> <dt>

<span data-ttu-id="52bc1-141">**IndirizzoIniziale**</span><span class="sxs-lookup"><span data-stu-id="52bc1-141">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52bc1-142">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="52bc1-142">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="52bc1-143">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="52bc1-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="52bc1-144">Indirizzo iniziale in cui inizia l'extent di livello superiore nell'archiviazione di livello più basso.</span><span class="sxs-lookup"><span data-stu-id="52bc1-144">The starting address where, in lower level storage, the higher level extent begins.</span></span> <span data-ttu-id="52bc1-145">Questa proprietà viene ereditata da [**CIM \_ BasedOn**](/windows/desktop/CIMWin32Prov/cim-basedon).</span><span class="sxs-lookup"><span data-stu-id="52bc1-145">This property is inherited from [**CIM\_BasedOn**](/windows/desktop/CIMWin32Prov/cim-basedon).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="52bc1-146">Requisiti</span><span class="sxs-lookup"><span data-stu-id="52bc1-146">Requirements</span></span>



| <span data-ttu-id="52bc1-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="52bc1-147">Requirement</span></span> | <span data-ttu-id="52bc1-148">Valore</span><span class="sxs-lookup"><span data-stu-id="52bc1-148">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="52bc1-149">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="52bc1-149">Minimum supported client</span></span><br/> | <span data-ttu-id="52bc1-150">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="52bc1-150">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="52bc1-151">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="52bc1-151">Minimum supported server</span></span><br/> | <span data-ttu-id="52bc1-152">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="52bc1-152">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="52bc1-153">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="52bc1-153">Namespace</span></span><br/>                | <span data-ttu-id="52bc1-154">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="52bc1-154">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="52bc1-155">MOF</span><span class="sxs-lookup"><span data-stu-id="52bc1-155">MOF</span></span><br/>                      | <dl> <span data-ttu-id="52bc1-156"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="52bc1-156"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="52bc1-157">DLL</span><span class="sxs-lookup"><span data-stu-id="52bc1-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="52bc1-158"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="52bc1-158"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

