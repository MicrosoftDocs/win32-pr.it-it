---
description: Rappresenta un'associazione tra un oggetto StorageExtent CIM di livello superiore \_ e un oggetto STORAGEEXTENT CIM di livello inferiore \_ . Un \_ oggetto CIM ProtectedSpaceExtent, ad esempio, fa parte di un \_ oggetto CIM PhysicalExtent.
ms.assetid: 40a88927-981b-4fc4-af5f-be91d9933284
title: Classe CIM_BasedOn (gestione Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BasedOn
- CIM_BasedOn.Antecedent
- CIM_BasedOn.Dependent
- CIM_BasedOn.StartingAddress
- CIM_BasedOn.EndingAddress
- CIM_BasedOn.OrderIndex
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 47d2e44d1106eba57f4c46c0957662c348c9ca1e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879109"
---
# <a name="cim_basedon-class-hyper-v-management"></a><span data-ttu-id="f1a69-104">Classe CIM_BasedOn (gestione Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="f1a69-104">CIM_BasedOn class (Hyper-V management)</span></span>

<span data-ttu-id="f1a69-105">Rappresenta un'associazione tra un oggetto **\_ StorageExtent CIM** di livello superiore e un oggetto **\_ StorageExtent CIM** di livello inferiore.</span><span class="sxs-lookup"><span data-stu-id="f1a69-105">Represents an association between a higher level **CIM\_StorageExtent** object and a lower level **CIM\_StorageExtent** object.</span></span> <span data-ttu-id="f1a69-106">Un oggetto [**CIM \_ ProtectedSpaceExtent**](/windows/desktop/CIMWin32Prov/cim-protectedspaceextent) , ad esempio, fa parte di un oggetto [**CIM \_ PhysicalExtent**](/windows/desktop/CIMWin32Prov/cim-physicalextent) .</span><span class="sxs-lookup"><span data-stu-id="f1a69-106">For example a [**CIM\_ProtectedSpaceExtent**](/windows/desktop/CIMWin32Prov/cim-protectedspaceextent) object is a part of a [**CIM\_PhysicalExtent**](/windows/desktop/CIMWin32Prov/cim-physicalextent) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1a69-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f1a69-107">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.6.0"), UMLPackagePath("CIM::Core::StorageExtent"), AMENDMENT]
class CIM_BasedOn : CIM_Dependency
{
  CIM_StorageExtent REF Antecedent;
  CIM_StorageExtent REF Dependent;
  uint64                StartingAddress;
  uint64                EndingAddress;
  uint16                OrderIndex;
};
```

## <a name="members"></a><span data-ttu-id="f1a69-108">Members</span><span class="sxs-lookup"><span data-stu-id="f1a69-108">Members</span></span>

<span data-ttu-id="f1a69-109">La classe **CIM \_ BasedOn** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="f1a69-109">The **CIM\_BasedOn** class has these types of members:</span></span>

-   [<span data-ttu-id="f1a69-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f1a69-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f1a69-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f1a69-111">Properties</span></span>

<span data-ttu-id="f1a69-112">La classe **CIM \_ BasedOn** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="f1a69-112">The **CIM\_BasedOn** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f1a69-113">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="f1a69-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1a69-114">Tipo di dati: **CIM \_ StorageExtent**</span><span class="sxs-lookup"><span data-stu-id="f1a69-114">Data type: **CIM\_StorageExtent**</span></span>
</dt> <dt>

<span data-ttu-id="f1a69-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f1a69-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1a69-116">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="f1a69-116">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="f1a69-117">Oggetto **\_ StorageExtent CIM** di livello inferiore.</span><span class="sxs-lookup"><span data-stu-id="f1a69-117">The lower level **CIM\_StorageExtent** object.</span></span>

</dd> <dt>

<span data-ttu-id="f1a69-118">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="f1a69-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1a69-119">Tipo di dati: **CIM \_ StorageExtent**</span><span class="sxs-lookup"><span data-stu-id="f1a69-119">Data type: **CIM\_StorageExtent**</span></span>
</dt> <dt>

<span data-ttu-id="f1a69-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f1a69-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1a69-121">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente")</span><span class="sxs-lookup"><span data-stu-id="f1a69-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="f1a69-122">Oggetto **\_ StorageExtent CIM** di livello superiore.</span><span class="sxs-lookup"><span data-stu-id="f1a69-122">The higher level **CIM\_StorageExtent** object.</span></span>

</dd> <dt>

<span data-ttu-id="f1a69-123">**EndingAddress**</span><span class="sxs-lookup"><span data-stu-id="f1a69-123">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1a69-124">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f1a69-124">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f1a69-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f1a69-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1a69-126">Indirizzo che indica il punto in cui si conclude l'oggetto di archiviazione di livello inferiore, l'oggetto **\_ StorageExtent** di livello superiore.</span><span class="sxs-lookup"><span data-stu-id="f1a69-126">The address that indicates where in lower level storage, the higher level **CIM\_StorageExtent** object ends.</span></span> <span data-ttu-id="f1a69-127">Questa proprietà è utile quando si esegue il mapping di oggetti **CIM \_ StorageExtent** non contigui in un raggruppamento di livello superiore.</span><span class="sxs-lookup"><span data-stu-id="f1a69-127">This property is useful when mapping non-contiguous **CIM\_StorageExtent** objects into a higher level grouping.</span></span>

</dd> <dt>

<span data-ttu-id="f1a69-128">**OrderIndex**</span><span class="sxs-lookup"><span data-stu-id="f1a69-128">**OrderIndex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1a69-129">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f1a69-129">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f1a69-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f1a69-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1a69-131">Indice utilizzato per specificare l'ordine delle associazioni **CIM \_ BasedOn** in una raccolta; in caso contrario, "0" indica nessun ordine.</span><span class="sxs-lookup"><span data-stu-id="f1a69-131">An index that is used to specify the order of **CIM\_BasedOn** associations in a collection; otherwise "0" indicates no order.</span></span> <span data-ttu-id="f1a69-132">**CIM \_** Le istanze di BasedOn con lo stesso valore dipendente devono inserire valori univoci nella proprietà **OrderIndex** .</span><span class="sxs-lookup"><span data-stu-id="f1a69-132">**CIM\_BasedOn** instances with the same dependent value should place unique values in the **OrderIndex** property.</span></span> <span data-ttu-id="f1a69-133">Il valore **OrderIndex** più basso specifica il primo membro della raccolta.</span><span class="sxs-lookup"><span data-stu-id="f1a69-133">The lowest **OrderIndex** value specifies the first member of the collection.</span></span>

<span data-ttu-id="f1a69-134">Un esempio di utilizzo di questa proprietà è la definizione di una matrice con striping RAID 0 di 3 dischi.</span><span class="sxs-lookup"><span data-stu-id="f1a69-134">An example of the use of this property is to define a RAID-0 striped array of 3 disks.</span></span> <span data-ttu-id="f1a69-135">La matrice RAID risultante è un extent di archiviazione che dipende dagli extent di archiviazione che descrivono ognuno dei 3 dischi.</span><span class="sxs-lookup"><span data-stu-id="f1a69-135">The resultant RAID array is a storage extent that is dependent on the storage extents that describe each of the 3 disks.</span></span> <span data-ttu-id="f1a69-136">Il valore **OrderIndex** di ogni associazione **CIM \_ BasedOn** da extent del disco all'array RAID può essere specificato come 1, 2 e 3 per indicare l'ordine in cui gli extent del disco vengono usati per accedere ai dati RAID.</span><span class="sxs-lookup"><span data-stu-id="f1a69-136">The **OrderIndex** value of each **CIM\_BasedOn** association from the disk extents to the RAID array could be specified as 1, 2, and 3 to indicate the order in which the disk extents are used to access the RAID data.</span></span>

</dd> <dt>

<span data-ttu-id="f1a69-137">**IndirizzoIniziale**</span><span class="sxs-lookup"><span data-stu-id="f1a69-137">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1a69-138">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f1a69-138">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f1a69-139">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f1a69-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1a69-140">Indirizzo che indica il punto in cui viene avviata l'oggetto **\_ StorageExtent** di livello più alto.</span><span class="sxs-lookup"><span data-stu-id="f1a69-140">The address that indicates where in lower level storage, the higher level **CIM\_StorageExtent** object begins.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f1a69-141">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f1a69-141">Requirements</span></span>



| <span data-ttu-id="f1a69-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="f1a69-142">Requirement</span></span> | <span data-ttu-id="f1a69-143">Valore</span><span class="sxs-lookup"><span data-stu-id="f1a69-143">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1a69-144">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f1a69-144">Minimum supported client</span></span><br/> | <span data-ttu-id="f1a69-145">Windows 8</span><span class="sxs-lookup"><span data-stu-id="f1a69-145">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="f1a69-146">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f1a69-146">Minimum supported server</span></span><br/> | <span data-ttu-id="f1a69-147">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f1a69-147">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="f1a69-148">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f1a69-148">Namespace</span></span><br/>                | <span data-ttu-id="f1a69-149">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="f1a69-149">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="f1a69-150">MOF</span><span class="sxs-lookup"><span data-stu-id="f1a69-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f1a69-151"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f1a69-151"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f1a69-152">DLL</span><span class="sxs-lookup"><span data-stu-id="f1a69-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f1a69-153"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f1a69-153"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f1a69-154">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f1a69-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1a69-155">**\_Dipendenza CIM**</span><span class="sxs-lookup"><span data-stu-id="f1a69-155">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

