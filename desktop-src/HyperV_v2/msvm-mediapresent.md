---
description: Associa un'unità di archiviazione al supporto inserito nell'unità.
ms.assetid: C0B2D604-0B55-4EA0-A46E-2450D89A5B22
title: Classe Msvm_MediaPresent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MediaPresent
- Msvm_MediaPresent.Antecedent
- Msvm_MediaPresent.Dependent
- Msvm_MediaPresent.FixedMedia
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 57d46fb711ab8d4abcf27966e6ec92ed2287bc3e
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "103886024"
---
# <a name="msvm_mediapresent-class"></a><span data-ttu-id="9f929-103">\_Classe MSVM MediaPresent</span><span class="sxs-lookup"><span data-stu-id="9f929-103">Msvm\_MediaPresent class</span></span>

<span data-ttu-id="9f929-104">Associa un'unità di archiviazione al supporto inserito nell'unità.</span><span class="sxs-lookup"><span data-stu-id="9f929-104">Associates a storage drive with the media inserted into the drive.</span></span> <span data-ttu-id="9f929-105">Questa associazione viene utilizzata per tutti gli oggetti unità di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="9f929-105">This association is used for all storage drive objects.</span></span>

<span data-ttu-id="9f929-106">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="9f929-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f929-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9f929-107">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_MediaPresent : CIM_MediaPresent
{
  CIM_MediaAccessDevice REF Antecedent;
  CIM_StorageExtent     REF Dependent;
  boolean                   FixedMedia;
};
```

## <a name="members"></a><span data-ttu-id="9f929-108">Members</span><span class="sxs-lookup"><span data-stu-id="9f929-108">Members</span></span>

<span data-ttu-id="9f929-109">La **classe \_ MediaPresent di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="9f929-109">The **Msvm\_MediaPresent** class has these types of members:</span></span>

-   [<span data-ttu-id="9f929-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="9f929-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9f929-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="9f929-111">Properties</span></span>

<span data-ttu-id="9f929-112">La **classe \_ MediaPresent di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="9f929-112">The **Msvm\_MediaPresent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9f929-113">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="9f929-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f929-114">Tipo di dati: **[ **CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)**</span><span class="sxs-lookup"><span data-stu-id="9f929-114">Data type: **[**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)**</span></span>
</dt> <dt>

<span data-ttu-id="9f929-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9f929-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9f929-116">Riferimento al dispositivo di accesso multimediale.</span><span class="sxs-lookup"><span data-stu-id="9f929-116">The reference to the media access device.</span></span> <span data-ttu-id="9f929-117">Questa proprietà viene ereditata da [**CIM \_ MediaPresent**](/windows/desktop/CIMWin32Prov/cim-mediapresent).</span><span class="sxs-lookup"><span data-stu-id="9f929-117">This property is inherited from [**CIM\_MediaPresent**](/windows/desktop/CIMWin32Prov/cim-mediapresent).</span></span>

</dd> <dt>

<span data-ttu-id="9f929-118">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="9f929-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f929-119">Tipo di dati: **[ **CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)**</span><span class="sxs-lookup"><span data-stu-id="9f929-119">Data type: **[**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)**</span></span>
</dt> <dt>

<span data-ttu-id="9f929-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9f929-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9f929-121">Riferimento all'extent di archiviazione a cui si accede con il dispositivo di accesso multimediale.</span><span class="sxs-lookup"><span data-stu-id="9f929-121">The reference to the storage extent accessed with the media access device.</span></span> <span data-ttu-id="9f929-122">Questa proprietà viene ereditata da [**CIM \_ MediaPresent**](/windows/desktop/CIMWin32Prov/cim-mediapresent).</span><span class="sxs-lookup"><span data-stu-id="9f929-122">This property is inherited from [**CIM\_MediaPresent**](/windows/desktop/CIMWin32Prov/cim-mediapresent).</span></span>

</dd> <dt>

<span data-ttu-id="9f929-123">**FixedMedia**</span><span class="sxs-lookup"><span data-stu-id="9f929-123">**FixedMedia**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f929-124">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="9f929-124">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9f929-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9f929-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9f929-126">Indica se l'extent di archiviazione a cui si accede è fisso e non può essere rimosso.</span><span class="sxs-lookup"><span data-stu-id="9f929-126">Indicates whether the accessed storage extent is fixed and cannot be ejected.</span></span> <span data-ttu-id="9f929-127">Il valore è **true** per i dischi rigidi e **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="9f929-127">The value is **True** for hard disks and **False** otherwise.</span></span> <span data-ttu-id="9f929-128">Questa proprietà viene ereditata da [**CIM \_ MediaPresent**](/windows/desktop/CIMWin32Prov/cim-mediapresent).</span><span class="sxs-lookup"><span data-stu-id="9f929-128">This property is inherited from [**CIM\_MediaPresent**](/windows/desktop/CIMWin32Prov/cim-mediapresent).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9f929-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="9f929-129">Remarks</span></span>

<span data-ttu-id="9f929-130">L'accesso alla **classe \_ MediaPresent di MSVM** potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="9f929-130">Access to the **Msvm\_MediaPresent** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="9f929-131">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="9f929-131">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="9f929-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9f929-132">Requirements</span></span>



| <span data-ttu-id="9f929-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="9f929-133">Requirement</span></span> | <span data-ttu-id="9f929-134">Valore</span><span class="sxs-lookup"><span data-stu-id="9f929-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f929-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9f929-135">Minimum supported client</span></span><br/> | <span data-ttu-id="9f929-136">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="9f929-136">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="9f929-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9f929-137">Minimum supported server</span></span><br/> | <span data-ttu-id="9f929-138">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="9f929-138">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9f929-139">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="9f929-139">Namespace</span></span><br/>                | <span data-ttu-id="9f929-140">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="9f929-140">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="9f929-141">MOF</span><span class="sxs-lookup"><span data-stu-id="9f929-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9f929-142"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9f929-142"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9f929-143">DLL</span><span class="sxs-lookup"><span data-stu-id="9f929-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9f929-144"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9f929-144"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="9f929-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9f929-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f929-146">**\_MEDIAPRESENT CIM**</span><span class="sxs-lookup"><span data-stu-id="9f929-146">**CIM\_MediaPresent**</span></span>](cim-mediapresent.md)
</dt> <dt>

[<span data-ttu-id="9f929-147">**\_MEDIAPRESENT CIM**</span><span class="sxs-lookup"><span data-stu-id="9f929-147">**CIM\_MediaPresent**</span></span>](/windows/desktop/CIMWin32Prov/cim-mediapresent)
</dt> <dt>

[<span data-ttu-id="9f929-148">Classi di archiviazione</span><span class="sxs-lookup"><span data-stu-id="9f929-148">Storage Classes</span></span>](storage-classes.md)
</dt> </dl>

 

