---
description: Fornisce i dati di impostazione per un disco rigido virtuale.
ms.assetid: 492a0b81-86b2-4d7d-a118-6ec14e3971ed
title: Classe Msvm_VirtualHardDiskSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualHardDiskSettingData
- Msvm_VirtualHardDiskSettingData.InstanceID
- Msvm_VirtualHardDiskSettingData.Caption
- Msvm_VirtualHardDiskSettingData.Description
- Msvm_VirtualHardDiskSettingData.ElementName
- Msvm_VirtualHardDiskSettingData.Type
- Msvm_VirtualHardDiskSettingData.Format
- Msvm_VirtualHardDiskSettingData.Path
- Msvm_VirtualHardDiskSettingData.ParentPath
- Msvm_VirtualHardDiskSettingData.ParentTimestamp
- Msvm_VirtualHardDiskSettingData.ParentIdentifier
- Msvm_VirtualHardDiskSettingData.MaxInternalSize
- Msvm_VirtualHardDiskSettingData.BlockSize
- Msvm_VirtualHardDiskSettingData.LogicalSectorSize
- Msvm_VirtualHardDiskSettingData.PhysicalSectorSize
- Msvm_VirtualHardDiskSettingData.VirtualDiskId
- Msvm_VirtualHardDiskSettingData.DataAlignment
- Msvm_VirtualHardDiskSettingData.PmemAddressAbstractionType
- Msvm_VirtualHardDiskSettingData.IsPmemCompatible
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 6e13efbb068d15ca4051995e7d9f317eb2ccacab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128410"
---
# <a name="msvm_virtualharddisksettingdata-class"></a><span data-ttu-id="84cde-103">\_Classe MSVM VirtualHardDiskSettingData</span><span class="sxs-lookup"><span data-stu-id="84cde-103">Msvm\_VirtualHardDiskSettingData class</span></span>

<span data-ttu-id="84cde-104">Fornisce i dati di impostazione per un disco rigido virtuale.</span><span class="sxs-lookup"><span data-stu-id="84cde-104">Provides setting data for a virtual hard disk.</span></span>

<span data-ttu-id="84cde-105">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="84cde-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="84cde-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="84cde-106">Syntax</span></span>

``` syntax
[AMENDMENT]
class Msvm_VirtualHardDiskSettingData : CIM_SettingData
{
  string   InstanceID;
  string   Caption = "Virtual Hard Disk Setting Data";
  string   Description = "Setting Data for a Virtual Hard Disk";
  string   ElementName;
  uint16   Type;
  uint16   Format;
  string   Path;
  string   ParentPath;
  DATETIME ParentTimestamp;
  string   ParentIdentifier;
  uint64   MaxInternalSize;
  uint32   BlockSize;
  uint32   LogicalSectorSize;
  uint32   PhysicalSectorSize;
  string   VirtualDiskId;
  uint64   DataAlignment;
  uint16   PmemAddressAbstractionType;
  boolean  IsPmemCompatible;
};
```

## <a name="members"></a><span data-ttu-id="84cde-107">Members</span><span class="sxs-lookup"><span data-stu-id="84cde-107">Members</span></span>

<span data-ttu-id="84cde-108">La **classe \_ VirtualHardDiskSettingData di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="84cde-108">The **Msvm\_VirtualHardDiskSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="84cde-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="84cde-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="84cde-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="84cde-110">Properties</span></span>

<span data-ttu-id="84cde-111">La **classe \_ VirtualHardDiskSettingData di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="84cde-111">The **Msvm\_VirtualHardDiskSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="84cde-112">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="84cde-112">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84cde-113">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="84cde-113">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="84cde-114">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="84cde-114">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="84cde-115">Dimensioni in byte del blocco utilizzato dal disco rigido virtuale.</span><span class="sxs-lookup"><span data-stu-id="84cde-115">The block size used by the virtual hard disk, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="84cde-116">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="84cde-116">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84cde-117">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="84cde-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="84cde-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="84cde-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84cde-119">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="84cde-119">A short description of the object.</span></span> <span data-ttu-id="84cde-120">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "dati di impostazione del disco rigido virtuale".</span><span class="sxs-lookup"><span data-stu-id="84cde-120">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Virtual Hard Disk Setting Data".</span></span>

</dd> <dt>

<span data-ttu-id="84cde-121">**Dataalignment**</span><span class="sxs-lookup"><span data-stu-id="84cde-121">**DataAlignment**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84cde-122">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="84cde-122">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="84cde-123">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="84cde-123">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="84cde-124">Specifica l'allineamento desiderato, in byte, per il payload dei dati del disco virtuale.</span><span class="sxs-lookup"><span data-stu-id="84cde-124">Specifies the desired alignment, in bytes, for the data payload of the virtual disk</span></span>

> [!Note]  
> <span data-ttu-id="84cde-125">Aggiunta in Windows 10, versione 1709.</span><span class="sxs-lookup"><span data-stu-id="84cde-125">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="84cde-126">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="84cde-126">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84cde-127">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="84cde-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="84cde-128">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="84cde-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84cde-129">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="84cde-129">A description of the object.</span></span> <span data-ttu-id="84cde-130">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "impostazione dei dati per un disco rigido virtuale".</span><span class="sxs-lookup"><span data-stu-id="84cde-130">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Setting Data for a Virtual Hard Disk".</span></span>

</dd> <dt>

<span data-ttu-id="84cde-131">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="84cde-131">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84cde-132">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="84cde-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="84cde-133">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="84cde-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84cde-134">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="84cde-134">A display name for the object.</span></span> <span data-ttu-id="84cde-135">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="84cde-135">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="84cde-136">**Formato**</span><span class="sxs-lookup"><span data-stu-id="84cde-136">**Format**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84cde-137">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="84cde-137">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="84cde-138">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="84cde-138">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="84cde-139">Formato del disco rigido virtuale.</span><span class="sxs-lookup"><span data-stu-id="84cde-139">The format for the virtual hard disk.</span></span> <span data-ttu-id="84cde-140">Si tratta di uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="84cde-140">This will be one of the following values.</span></span>

<dt>

<span id="VHD"></span><span id="vhd"></span>

<span data-ttu-id="84cde-141"><span id="VHD"></span><span id="vhd"></span>**Disco rigido virtuale** (2)</span><span class="sxs-lookup"><span data-stu-id="84cde-141"><span id="VHD"></span><span id="vhd"></span>**VHD** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="VHDX"></span><span id="vhdx"></span>

<span data-ttu-id="84cde-142"><span id="VHDX"></span><span id="vhdx"></span>**VHDX** (3)</span><span class="sxs-lookup"><span data-stu-id="84cde-142"><span id="VHDX"></span><span id="vhdx"></span>**VHDX** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="VHDSet"></span><span id="vhdset"></span><span id="VHDSET"></span>

<span data-ttu-id="84cde-143"><span id="VHDSet"></span><span id="vhdset"></span><span id="VHDSET"></span>**VHDSet** (4)</span><span class="sxs-lookup"><span data-stu-id="84cde-143"><span id="VHDSet"></span><span id="vhdset"></span><span id="VHDSET"></span>**VHDSet** (4)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="84cde-144">Aggiunta in Windows 10 e Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="84cde-144">Added in Windows 10 and Windows Server 2016.</span></span>

 

</dd> </dl>

</dd> <dt>

<span data-ttu-id="84cde-145">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="84cde-145">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84cde-146">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="84cde-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="84cde-147">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="84cde-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="84cde-148">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="84cde-148">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="84cde-149">Identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="84cde-149">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="84cde-150">Questa proprietà viene ereditata da [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="84cde-150">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="84cde-151">**IsPmemCompatible**</span><span class="sxs-lookup"><span data-stu-id="84cde-151">**IsPmemCompatible**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84cde-152">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="84cde-152">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="84cde-153">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="84cde-153">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="84cde-154">Specifica se il disco virtuale può essere utilizzato come archivio di backup per un dispositivo di memoria permanente.</span><span class="sxs-lookup"><span data-stu-id="84cde-154">Specifies whether the virtual disk can be used as the backing store for a persistent memory device.</span></span>

> [!Note]  
> <span data-ttu-id="84cde-155">Aggiunta in Windows 10, versione 1709.</span><span class="sxs-lookup"><span data-stu-id="84cde-155">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="84cde-156">**LogicalSectorSize**</span><span class="sxs-lookup"><span data-stu-id="84cde-156">**LogicalSectorSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84cde-157">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="84cde-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="84cde-158">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="84cde-158">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="84cde-159">Dimensioni del settore logico utilizzate dal disco rigido virtuale, in byte.</span><span class="sxs-lookup"><span data-stu-id="84cde-159">The logical sector size used by the virtual hard disk, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="84cde-160">**MaxInternalSize**</span><span class="sxs-lookup"><span data-stu-id="84cde-160">**MaxInternalSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84cde-161">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="84cde-161">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="84cde-162">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="84cde-162">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="84cde-163">Dimensione massima del disco rigido virtuale, in byte, visualizzabile dalla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="84cde-163">The maximum size of the virtual hard disk as viewable by the virtual machine, in bytes.</span></span> <span data-ttu-id="84cde-164">Questa dimensione verrà arrotondata al multiplo più grande successivo delle dimensioni del settore.</span><span class="sxs-lookup"><span data-stu-id="84cde-164">This size will be rounded up to the next largest multiple of the sector size.</span></span>

</dd> <dt>

<span data-ttu-id="84cde-165">**ParentIdentifier**</span><span class="sxs-lookup"><span data-stu-id="84cde-165">**ParentIdentifier**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84cde-166">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="84cde-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="84cde-167">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="84cde-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84cde-168">GUID utilizzato per identificare in modo univoco l'elemento padre del disco rigido virtuale.</span><span class="sxs-lookup"><span data-stu-id="84cde-168">The GUID used to uniquely identify the parent of the virtual hard disk.</span></span> <span data-ttu-id="84cde-169">Se il disco rigido virtuale non dispone di un elemento padre, questo campo è vuoto.</span><span class="sxs-lookup"><span data-stu-id="84cde-169">If the virtual hard disk does not have a parent, then this field is empty.</span></span>

> [!Note]  
> <span data-ttu-id="84cde-170">Aggiunta in Windows 10 e Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="84cde-170">Added in Windows 10 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="84cde-171">**ParentPath**</span><span class="sxs-lookup"><span data-stu-id="84cde-171">**ParentPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84cde-172">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="84cde-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="84cde-173">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="84cde-173">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="84cde-174">Elemento padre del disco rigido virtuale.</span><span class="sxs-lookup"><span data-stu-id="84cde-174">The parent of the virtual hard disk.</span></span> <span data-ttu-id="84cde-175">Se il disco rigido virtuale non dispone di un elemento padre, questa proprietà è vuota.</span><span class="sxs-lookup"><span data-stu-id="84cde-175">If the virtual hard disk does not have a parent, then this property is empty.</span></span>

</dd> <dt>

<span data-ttu-id="84cde-176">**ParentTimestamp**</span><span class="sxs-lookup"><span data-stu-id="84cde-176">**ParentTimestamp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84cde-177">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="84cde-177">Data type: **DATETIME**</span></span>
</dt> <dt>

<span data-ttu-id="84cde-178">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="84cde-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="84cde-179">Timestamp dell'elemento padre del disco rigido virtuale.</span><span class="sxs-lookup"><span data-stu-id="84cde-179">The timestamp of the parent of the virtual hard disk.</span></span> <span data-ttu-id="84cde-180">Se il disco rigido virtuale non dispone di un elemento padre, questo campo è vuoto.</span><span class="sxs-lookup"><span data-stu-id="84cde-180">If the virtual hard disk does not have a parent, then this field is empty.</span></span>

> [!Note]  
> <span data-ttu-id="84cde-181">Aggiunta in Windows 10 e Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="84cde-181">Added in Windows 10 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="84cde-182">**Percorso**</span><span class="sxs-lookup"><span data-stu-id="84cde-182">**Path**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84cde-183">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="84cde-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="84cde-184">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="84cde-184">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="84cde-185">Percorso completo del disco rigido virtuale.</span><span class="sxs-lookup"><span data-stu-id="84cde-185">The fully qualified path of the virtual hard disk.</span></span>

</dd> <dt>

<span data-ttu-id="84cde-186">**PhysicalSectorSize**</span><span class="sxs-lookup"><span data-stu-id="84cde-186">**PhysicalSectorSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84cde-187">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="84cde-187">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="84cde-188">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="84cde-188">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="84cde-189">Dimensioni del settore fisico utilizzate dal disco rigido virtuale, in byte.</span><span class="sxs-lookup"><span data-stu-id="84cde-189">The physical sector size used by the virtual hard disk, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="84cde-190">**PmemAddressAbstractionType**</span><span class="sxs-lookup"><span data-stu-id="84cde-190">**PmemAddressAbstractionType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84cde-191">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="84cde-191">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="84cde-192">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="84cde-192">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="84cde-193">Metodo di astrazione dell'indirizzo di memoria permanente da usare con questo disco virtuale.</span><span class="sxs-lookup"><span data-stu-id="84cde-193">The persistent memory address abstraction method to be used with this virtual disk.</span></span>

> [!Note]  
> <span data-ttu-id="84cde-194">Aggiunta in Windows 10, versione 1709.</span><span class="sxs-lookup"><span data-stu-id="84cde-194">Added in Windows 10, version 1709.</span></span>

 

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="84cde-195">**Nessuno** (0)</span><span class="sxs-lookup"><span data-stu-id="84cde-195">**None** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="BTT"></span><span id="btt"></span>

<span data-ttu-id="84cde-196">**BTT** (1)</span><span class="sxs-lookup"><span data-stu-id="84cde-196">**BTT** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="84cde-197">**Sconosciuto** (65535)</span><span class="sxs-lookup"><span data-stu-id="84cde-197">**Unknown** (65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="84cde-198">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="84cde-198">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84cde-199">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="84cde-199">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="84cde-200">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="84cde-200">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="84cde-201">Tipo di disco rigido virtuale.</span><span class="sxs-lookup"><span data-stu-id="84cde-201">The type of virtual hard disk.</span></span> <span data-ttu-id="84cde-202">Si tratta di uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="84cde-202">This will be one of the following values.</span></span>

<dt>

<span id="Fixed"></span><span id="fixed"></span><span id="FIXED"></span>

<span data-ttu-id="84cde-203">**Corretto** (2)</span><span class="sxs-lookup"><span data-stu-id="84cde-203">**Fixed** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Dynamic"></span><span id="dynamic"></span><span id="DYNAMIC"></span>

<span data-ttu-id="84cde-204">**Dinamica** (3)</span><span class="sxs-lookup"><span data-stu-id="84cde-204">**Dynamic** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Differencing"></span><span id="differencing"></span><span id="DIFFERENCING"></span>

<span data-ttu-id="84cde-205">**Differenze** (4)</span><span class="sxs-lookup"><span data-stu-id="84cde-205">**Differencing** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="84cde-206">**VirtualDiskId**</span><span class="sxs-lookup"><span data-stu-id="84cde-206">**VirtualDiskId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84cde-207">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="84cde-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="84cde-208">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="84cde-208">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="84cde-209">GUID utilizzato per identificare in modo univoco il disco virtuale.</span><span class="sxs-lookup"><span data-stu-id="84cde-209">The GUID that is used to uniquely identify the virtual disk.</span></span>

<span data-ttu-id="84cde-210">Quando il metodo [**MSVM \_ servizio. GetVirtualHardDiskSettingData**](getvirtualharddisksettingdata-msvm-imagemanagementservice.md) restituisce un'istanza di **MSVM \_ VirtualHardDiskSettingData**, il client può usare questa proprietà per ottenere l'ID disco univoco del disco rigido virtuale.</span><span class="sxs-lookup"><span data-stu-id="84cde-210">When the [**Msvm\_ImageManagementService.GetVirtualHardDiskSettingData**](getvirtualharddisksettingdata-msvm-imagemanagementservice.md) method returns an instance of **Msvm\_VirtualHardDiskSettingData**, the client can use this property to get the unique disk ID of the VHD.</span></span>

<span data-ttu-id="84cde-211">Nel rilevamento dei conflitti o in caso contrario, un client può impostare il valore **VirtualDiskId** su un nuovo GUID e passare questa istanza **MSVM \_ VirtualHardDiskSettingData** al metodo [**MSVM \_ servizio. SetVirtualHardDiskSettingData**](setvirtualharddisksettingdata-msvm-imagemanagementservice.md) per modificare l'ID disco del disco rigido virtuale.</span><span class="sxs-lookup"><span data-stu-id="84cde-211">On conflict detection or otherwise, a client can set the **VirtualDiskId** value to a new GUID and pass this **Msvm\_VirtualHardDiskSettingData** instance to the [**Msvm\_ImageManagementService.SetVirtualHardDiskSettingData**](setvirtualharddisksettingdata-msvm-imagemanagementservice.md) method to change the disk ID of the VHD.</span></span> <span data-ttu-id="84cde-212">Se il disco rigido virtuale non è un VHD VHDX o se il disco rigido virtuale è collegato, l'operazione ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="84cde-212">If the VHD is not a VHDX VHD, or if the VHD is attached, the operation fails.</span></span> <span data-ttu-id="84cde-213">L'operazione ha esito negativo anche se il valore passato non è valido, ovvero non è un GUID o ha tutti i 0.</span><span class="sxs-lookup"><span data-stu-id="84cde-213">The operation also fails if the passed value is malformed, that is, not a GUID or has all 0s.</span></span> <span data-ttu-id="84cde-214">L'operazione ha esito positivo automaticamente se il valore passato è uguale all'ID del disco corrente.</span><span class="sxs-lookup"><span data-stu-id="84cde-214">The operation silently succeeds if the passed value is the same as the current disk ID.</span></span>

<span data-ttu-id="84cde-215">Gli errori generati dalla funzione [**SetVirtualDiskInformation**](/windows/win32/api/virtdisk/nf-virtdisk-setvirtualdiskinformation) vengono propagati tramite questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="84cde-215">Errors generated by the [**SetVirtualDiskInformation**](/windows/win32/api/virtdisk/nf-virtdisk-setvirtualdiskinformation) function are bubbled up through this property.</span></span> <span data-ttu-id="84cde-216">Un client può anche usare lo stesso meccanismo per fornire il valore **VirtualDiskId** in fase di creazione del disco rigido virtuale tramite il metodo [**MSVM \_ servizio. CreateVirtualHardDisk**](createvirtualharddisk-msvm-imagemanagementservice.md) nello stesso spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="84cde-216">A client can also use the same mechanism to provide the **VirtualDiskId** value at VHD creation via the [**Msvm\_ImageManagementService.CreateVirtualHardDisk**](createvirtualharddisk-msvm-imagemanagementservice.md) method in the same namespace.</span></span> <span data-ttu-id="84cde-217">Questa operazione può essere usata per creare dischi rigidi virtuali VHD1 o VHD2.</span><span class="sxs-lookup"><span data-stu-id="84cde-217">This can be used to create VHD1 or VHD2 VHDs.</span></span>

<span data-ttu-id="84cde-218">**Windows 8.1:** Questo valore non è supportato fino a Windows 8.1 e Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="84cde-218">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="84cde-219">Requisiti</span><span class="sxs-lookup"><span data-stu-id="84cde-219">Requirements</span></span>



| <span data-ttu-id="84cde-220">Requisito</span><span class="sxs-lookup"><span data-stu-id="84cde-220">Requirement</span></span> | <span data-ttu-id="84cde-221">Valore</span><span class="sxs-lookup"><span data-stu-id="84cde-221">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="84cde-222">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="84cde-222">Minimum supported client</span></span><br/> | <span data-ttu-id="84cde-223">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="84cde-223">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="84cde-224">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="84cde-224">Minimum supported server</span></span><br/> | <span data-ttu-id="84cde-225">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="84cde-225">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="84cde-226">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="84cde-226">Namespace</span></span><br/>                | <span data-ttu-id="84cde-227">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="84cde-227">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="84cde-228">MOF</span><span class="sxs-lookup"><span data-stu-id="84cde-228">MOF</span></span><br/>                      | <dl> <span data-ttu-id="84cde-229"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="84cde-229"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="84cde-230">DLL</span><span class="sxs-lookup"><span data-stu-id="84cde-230">DLL</span></span><br/>                      | <dl> <span data-ttu-id="84cde-231"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="84cde-231"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="84cde-232">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="84cde-232">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84cde-233">**\_SETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="84cde-233">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> <dt>

[<span data-ttu-id="84cde-234">**GetVirtualHardDiskSettingData**</span><span class="sxs-lookup"><span data-stu-id="84cde-234">**GetVirtualHardDiskSettingData**</span></span>](getvirtualharddisksettingdata-msvm-imagemanagementservice.md)
</dt> </dl>

 

