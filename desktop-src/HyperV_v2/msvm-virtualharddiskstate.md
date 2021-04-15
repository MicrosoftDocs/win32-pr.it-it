---
description: Fornisce informazioni sullo stato per un'immagine del disco rigido virtuale esistente.
ms.assetid: b0177906-71dc-4be8-b351-97d7ef427acd
title: Classe Msvm_VirtualHardDiskState
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualHardDiskState
- Msvm_VirtualHardDiskState.FileSize
- Msvm_VirtualHardDiskState.InUse
- Msvm_VirtualHardDiskState.MinInternalSize
- Msvm_VirtualHardDiskState.PhysicalSectorSize
- Msvm_VirtualHardDiskState.Alignment
- Msvm_VirtualHardDiskState.FragmentationPercentage
- Msvm_VirtualHardDiskState.Timestamp
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 15d0a8b150e83c17946a6d1b66c7086383f08466
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484356"
---
# <a name="msvm_virtualharddiskstate-class"></a><span data-ttu-id="3be20-103">\_Classe MSVM VirtualHardDiskState</span><span class="sxs-lookup"><span data-stu-id="3be20-103">Msvm\_VirtualHardDiskState class</span></span>

<span data-ttu-id="3be20-104">Fornisce informazioni sullo stato per un'immagine del disco rigido virtuale esistente.</span><span class="sxs-lookup"><span data-stu-id="3be20-104">Provides state information for an existing virtual hard disk image.</span></span>

<span data-ttu-id="3be20-105">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="3be20-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3be20-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3be20-106">Syntax</span></span>

``` syntax
[AMENDMENT]
class Msvm_VirtualHardDiskState
{
  uint64   FileSize;
  boolean  InUse;
  uint64   MinInternalSize;
  uint32   PhysicalSectorSize;
  uint32   Alignment;
  uint32   FragmentationPercentage;
  DATETIME Timestamp;
};
```

## <a name="members"></a><span data-ttu-id="3be20-107">Members</span><span class="sxs-lookup"><span data-stu-id="3be20-107">Members</span></span>

<span data-ttu-id="3be20-108">La **classe \_ VirtualHardDiskState di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="3be20-108">The **Msvm\_VirtualHardDiskState** class has these types of members:</span></span>

-   [<span data-ttu-id="3be20-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="3be20-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3be20-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="3be20-110">Properties</span></span>

<span data-ttu-id="3be20-111">La **classe \_ VirtualHardDiskState di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="3be20-111">The **Msvm\_VirtualHardDiskState** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3be20-112">**Allineamento**</span><span class="sxs-lookup"><span data-stu-id="3be20-112">**Alignment**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3be20-113">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3be20-113">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3be20-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3be20-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3be20-115">Specifica il tipo di allineamento del disco rigido virtuale.</span><span class="sxs-lookup"><span data-stu-id="3be20-115">Specifies the type of alignment of the virtual hard disk.</span></span> <span data-ttu-id="3be20-116">Si tratta di uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="3be20-116">This will be one of the following values.</span></span>



| <span data-ttu-id="3be20-117">Valore</span><span class="sxs-lookup"><span data-stu-id="3be20-117">Value</span></span>                                                                        | <span data-ttu-id="3be20-118">Significato</span><span class="sxs-lookup"><span data-stu-id="3be20-118">Meaning</span></span>                        |
|------------------------------------------------------------------------------|--------------------------------|
| <dl> <span data-ttu-id="3be20-119"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="3be20-119"><dt>0</dt></span></span> </dl> | <span data-ttu-id="3be20-120">allineamento a 512 byte.</span><span class="sxs-lookup"><span data-stu-id="3be20-120">512 byte alignment.</span></span><br/> |
| <dl> <span data-ttu-id="3be20-121"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="3be20-121"><dt>1</dt></span></span> </dl> | <span data-ttu-id="3be20-122">allineamento a 4 KB.</span><span class="sxs-lookup"><span data-stu-id="3be20-122">4 KB alignment.</span></span><br/>     |



 

</dd> <dt>

<span data-ttu-id="3be20-123">**FileSize**</span><span class="sxs-lookup"><span data-stu-id="3be20-123">**FileSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3be20-124">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3be20-124">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3be20-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3be20-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3be20-126">Dimensioni del file del disco rigido virtuale, ovvero la quantità effettiva di spazio di archiviazione utilizzata dal file, in byte.</span><span class="sxs-lookup"><span data-stu-id="3be20-126">The size of the virtual hard disk file (the actual amount of storage being consumed by the file), in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="3be20-127">**FragmentationPercentage**</span><span class="sxs-lookup"><span data-stu-id="3be20-127">**FragmentationPercentage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3be20-128">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3be20-128">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3be20-129">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3be20-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3be20-130">Approssimazione della percentuale di blocchi di dischi virtuali frammentati nel file del disco rigido virtuale.</span><span class="sxs-lookup"><span data-stu-id="3be20-130">An approximation of the percentage of virtual disk blocks that are fragmented in the virtual hard disk file.</span></span>

</dd> <dt>

<span data-ttu-id="3be20-131">**InUse**</span><span class="sxs-lookup"><span data-stu-id="3be20-131">**InUse**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3be20-132">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="3be20-132">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3be20-133">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3be20-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3be20-134">La proprietà viene riservata per un utilizzo futuro.</span><span class="sxs-lookup"><span data-stu-id="3be20-134">This property is reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="3be20-135">**MinInternalSize**</span><span class="sxs-lookup"><span data-stu-id="3be20-135">**MinInternalSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3be20-136">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3be20-136">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3be20-137">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3be20-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3be20-138">Dimensioni minime in byte in cui è possibile compattare il disco rigido virtuale.</span><span class="sxs-lookup"><span data-stu-id="3be20-138">The minimum size that the virtual hard disk can be shrunk to, in bytes.</span></span> <span data-ttu-id="3be20-139">Questa dimensione viene arrotondata per eccesso al successivo multiplo più grande delle dimensioni del settore.</span><span class="sxs-lookup"><span data-stu-id="3be20-139">This size is rounded up to the next largest multiple of the sector size.</span></span>

</dd> <dt>

<span data-ttu-id="3be20-140">**PhysicalSectorSize**</span><span class="sxs-lookup"><span data-stu-id="3be20-140">**PhysicalSectorSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3be20-141">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3be20-141">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3be20-142">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3be20-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3be20-143">Dimensioni del settore fisico utilizzate dal disco fisico sottostante, in byte.</span><span class="sxs-lookup"><span data-stu-id="3be20-143">The physical sector size used by the underlying physical disk, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="3be20-144">**Timestamp**</span><span class="sxs-lookup"><span data-stu-id="3be20-144">**Timestamp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3be20-145">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="3be20-145">Data type: **DATETIME**</span></span>
</dt> <dt>

<span data-ttu-id="3be20-146">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3be20-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3be20-147">Timestamp del disco rigido virtuale</span><span class="sxs-lookup"><span data-stu-id="3be20-147">The timestamp of the virtual hard disk</span></span>

> [!Note]  
> <span data-ttu-id="3be20-148">Aggiunta in Windows 10 e Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="3be20-148">Added in Windows 10 and Windows Server 2016.</span></span>

 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3be20-149">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3be20-149">Requirements</span></span>



| <span data-ttu-id="3be20-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="3be20-150">Requirement</span></span> | <span data-ttu-id="3be20-151">Valore</span><span class="sxs-lookup"><span data-stu-id="3be20-151">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3be20-152">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3be20-152">Minimum supported client</span></span><br/> | <span data-ttu-id="3be20-153">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="3be20-153">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="3be20-154">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3be20-154">Minimum supported server</span></span><br/> | <span data-ttu-id="3be20-155">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="3be20-155">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3be20-156">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="3be20-156">Namespace</span></span><br/>                | <span data-ttu-id="3be20-157">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="3be20-157">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="3be20-158">MOF</span><span class="sxs-lookup"><span data-stu-id="3be20-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3be20-159"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3be20-159"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3be20-160">DLL</span><span class="sxs-lookup"><span data-stu-id="3be20-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3be20-161"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3be20-161"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="3be20-162">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3be20-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3be20-163">**GetVirtualHardDiskState**</span><span class="sxs-lookup"><span data-stu-id="3be20-163">**GetVirtualHardDiskState**</span></span>](getvirtualharddiskstate-msvm-imagemanagementservice.md)
</dt> </dl>

 

 




