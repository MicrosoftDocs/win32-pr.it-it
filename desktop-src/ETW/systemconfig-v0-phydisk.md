---
description: Questa classe è la classe del tipo di evento per gli eventi di configurazione del disco fisico.
ms.assetid: 90ca3089-de5c-4e15-8abf-eaab9aafff06
title: Classe SystemConfig_V0_PhyDisk
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_V0_PhyDisk
- SystemConfig_V0_PhyDisk.DiskNumber
- SystemConfig_V0_PhyDisk.BytesPerSector
- SystemConfig_V0_PhyDisk.SectorsPerTrack
- SystemConfig_V0_PhyDisk.TracksPerCylinder
- SystemConfig_V0_PhyDisk.Cylinders
- SystemConfig_V0_PhyDisk.SCSIPort
- SystemConfig_V0_PhyDisk.SCSIPath
- SystemConfig_V0_PhyDisk.SCSITarget
- SystemConfig_V0_PhyDisk.SCSILun
- SystemConfig_V0_PhyDisk.Manufacturer
- SystemConfig_V0_PhyDisk.PartitionCount
- SystemConfig_V0_PhyDisk.WriteCacheEnabled
- SystemConfig_V0_PhyDisk.BootDriveLetter
api_type:
- NA
api_location: ''
ms.openlocfilehash: 2f7eab1cec90630e25ee5968e5740f787acb8662
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980543"
---
# <a name="systemconfig_v0_phydisk-class"></a><span data-ttu-id="01174-103">\_Classe SystemConfig V0 \_ PhyDisk</span><span class="sxs-lookup"><span data-stu-id="01174-103">SystemConfig\_V0\_PhyDisk class</span></span>

<span data-ttu-id="01174-104">Questa classe è la classe del tipo di evento per gli eventi di configurazione del disco fisico.</span><span class="sxs-lookup"><span data-stu-id="01174-104">This class is the event type class for physical disk configuration events.</span></span>

<span data-ttu-id="01174-105">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="01174-105">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="01174-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="01174-106">Syntax</span></span>

``` syntax
[EventType(11), EventTypeName("PhyDisk")]
class SystemConfig_V0_PhyDisk : SystemConfig_V0
{
  uint32  DiskNumber;
  uint32  BytesPerSector;
  uint32  SectorsPerTrack;
  uint32  TracksPerCylinder;
  uint64  Cylinders;
  uint32  SCSIPort;
  uint32  SCSIPath;
  uint32  SCSITarget;
  uint32  SCSILun;
  char16  Manufacturer[];
  uint32  PartitionCount;
  boolean WriteCacheEnabled;
  char16  BootDriveLetter[];
};
```

## <a name="members"></a><span data-ttu-id="01174-107">Members</span><span class="sxs-lookup"><span data-stu-id="01174-107">Members</span></span>

<span data-ttu-id="01174-108">La classe **SystemConfig \_ V0 \_ PhyDisk** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="01174-108">The **SystemConfig\_V0\_PhyDisk** class has these types of members:</span></span>

-   [<span data-ttu-id="01174-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="01174-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="01174-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="01174-110">Properties</span></span>

<span data-ttu-id="01174-111">La classe **SystemConfig \_ V0 \_ PhyDisk** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="01174-111">The **SystemConfig\_V0\_PhyDisk** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="01174-112">**BootDriveLetter**</span><span class="sxs-lookup"><span data-stu-id="01174-112">**BootDriveLetter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01174-113">Tipo di dati: matrice **Char16**</span><span class="sxs-lookup"><span data-stu-id="01174-113">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="01174-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="01174-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01174-115">Qualificatori: **WmiDataId** (13), **Max** (3)</span><span class="sxs-lookup"><span data-stu-id="01174-115">Qualifiers: **WmiDataId** (13), **Max** (3)</span></span>
</dt> </dl>

<span data-ttu-id="01174-116">Lettera di unità dell'unità di avvio nel formato " <letter> :".</span><span class="sxs-lookup"><span data-stu-id="01174-116">Drive letter of the boot drive in the form, "<letter>:".</span></span>

</dd> <dt>

<span data-ttu-id="01174-117">**BytesPerSector**</span><span class="sxs-lookup"><span data-stu-id="01174-117">**BytesPerSector**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01174-118">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="01174-118">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="01174-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="01174-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01174-120">Qualificatori: **WmiDataId** (2)</span><span class="sxs-lookup"><span data-stu-id="01174-120">Qualifiers: **WmiDataId** (2)</span></span>
</dt> </dl>

<span data-ttu-id="01174-121">Numero di byte in ogni settore per l'unità disco fisica.</span><span class="sxs-lookup"><span data-stu-id="01174-121">Number of bytes in each sector for the physical disk drive.</span></span>

</dd> <dt>

<span data-ttu-id="01174-122">**Cilindri**</span><span class="sxs-lookup"><span data-stu-id="01174-122">**Cylinders**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01174-123">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="01174-123">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="01174-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="01174-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01174-125">Qualificatori: **WmiDataId** (5)</span><span class="sxs-lookup"><span data-stu-id="01174-125">Qualifiers: **WmiDataId** (5)</span></span>
</dt> </dl>

<span data-ttu-id="01174-126">Numero totale di cilindri sull'unità disco fisica.</span><span class="sxs-lookup"><span data-stu-id="01174-126">Total number of cylinders on the physical disk drive.</span></span> <span data-ttu-id="01174-127">Nota: il valore di questa proprietà viene ottenuto tramite le funzioni estese dell'interrupt BIOS 13h.</span><span class="sxs-lookup"><span data-stu-id="01174-127">Note: the value for this property is obtained through extended functions of BIOS interrupt 13h.</span></span> <span data-ttu-id="01174-128">Il valore potrebbe non essere accurato se l'unità usa uno schema di conversione per supportare dimensioni del disco con capacità elevata.</span><span class="sxs-lookup"><span data-stu-id="01174-128">The value may be inaccurate if the drive uses a translation scheme to support high capacity disk sizes.</span></span> <span data-ttu-id="01174-129">Consultare il produttore per le specifiche di unità accurate.</span><span class="sxs-lookup"><span data-stu-id="01174-129">Consult the manufacturer for accurate drive specifications.</span></span>

</dd> <dt>

<span data-ttu-id="01174-130">**Numerodisco**</span><span class="sxs-lookup"><span data-stu-id="01174-130">**DiskNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01174-131">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="01174-131">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="01174-132">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="01174-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01174-133">Qualificatori: **WmiDataId** (1)</span><span class="sxs-lookup"><span data-stu-id="01174-133">Qualifiers: **WmiDataId** (1)</span></span>
</dt> </dl>

<span data-ttu-id="01174-134">Numero di indice del disco contenente questa partizione.</span><span class="sxs-lookup"><span data-stu-id="01174-134">Index number of the disk containing this partition.</span></span>

</dd> <dt>

<span data-ttu-id="01174-135">**Produttore**</span><span class="sxs-lookup"><span data-stu-id="01174-135">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01174-136">Tipo di dati: matrice **Char16**</span><span class="sxs-lookup"><span data-stu-id="01174-136">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="01174-137">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="01174-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01174-138">Qualificatori: **WmiDataId** (10), **Max** (256)</span><span class="sxs-lookup"><span data-stu-id="01174-138">Qualifiers: **WmiDataId** (10), **Max** (256)</span></span>
</dt> </dl>

<span data-ttu-id="01174-139">Nome del produttore dell'unità disco.</span><span class="sxs-lookup"><span data-stu-id="01174-139">Name of the disk drive manufacturer.</span></span>

</dd> <dt>

<span data-ttu-id="01174-140">**PartitionCount**</span><span class="sxs-lookup"><span data-stu-id="01174-140">**PartitionCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01174-141">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="01174-141">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="01174-142">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="01174-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01174-143">Qualificatori: **WmiDataId** (11)</span><span class="sxs-lookup"><span data-stu-id="01174-143">Qualifiers: **WmiDataId** (11)</span></span>
</dt> </dl>

<span data-ttu-id="01174-144">Numero di partizioni in questa unità disco fisica riconosciute dal sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="01174-144">Number of partitions on this physical disk drive that are recognized by the operating system.</span></span>

</dd> <dt>

<span data-ttu-id="01174-145">**SCSILun**</span><span class="sxs-lookup"><span data-stu-id="01174-145">**SCSILun**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01174-146">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="01174-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="01174-147">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="01174-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01174-148">Qualificatori: **WmiDataId** (9)</span><span class="sxs-lookup"><span data-stu-id="01174-148">Qualifiers: **WmiDataId** (9)</span></span>
</dt> </dl>

<span data-ttu-id="01174-149">Numero di unità logica (LUN) SCSI della scheda SCSI.</span><span class="sxs-lookup"><span data-stu-id="01174-149">SCSI logical unit number (LUN) of the SCSI adapter.</span></span>

</dd> <dt>

<span data-ttu-id="01174-150">**SCSIPath**</span><span class="sxs-lookup"><span data-stu-id="01174-150">**SCSIPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01174-151">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="01174-151">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="01174-152">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="01174-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01174-153">Qualificatori: **WmiDataId** (7)</span><span class="sxs-lookup"><span data-stu-id="01174-153">Qualifiers: **WmiDataId** (7)</span></span>
</dt> </dl>

<span data-ttu-id="01174-154">Numero del bus SCSI della scheda SCSI.</span><span class="sxs-lookup"><span data-stu-id="01174-154">SCSI bus number of the SCSI adapter.</span></span>

</dd> <dt>

<span data-ttu-id="01174-155">**SCSIPort**</span><span class="sxs-lookup"><span data-stu-id="01174-155">**SCSIPort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01174-156">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="01174-156">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="01174-157">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="01174-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01174-158">Qualificatori: **WmiDataId** (6)</span><span class="sxs-lookup"><span data-stu-id="01174-158">Qualifiers: **WmiDataId** (6)</span></span>
</dt> </dl>

<span data-ttu-id="01174-159">Numero SCSI della scheda SCSI.</span><span class="sxs-lookup"><span data-stu-id="01174-159">SCSI number of the SCSI adapter.</span></span>

</dd> <dt>

<span data-ttu-id="01174-160">**SCSITarget**</span><span class="sxs-lookup"><span data-stu-id="01174-160">**SCSITarget**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01174-161">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="01174-161">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="01174-162">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="01174-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01174-163">Qualificatori: **WmiDataId** (8)</span><span class="sxs-lookup"><span data-stu-id="01174-163">Qualifiers: **WmiDataId** (8)</span></span>
</dt> </dl>

<span data-ttu-id="01174-164">Contiene il numero del dispositivo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="01174-164">Contains the number of the target device.</span></span>

</dd> <dt>

<span data-ttu-id="01174-165">**SectorsPerTrack**</span><span class="sxs-lookup"><span data-stu-id="01174-165">**SectorsPerTrack**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01174-166">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="01174-166">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="01174-167">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="01174-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01174-168">Qualificatori: **WmiDataId** (3)</span><span class="sxs-lookup"><span data-stu-id="01174-168">Qualifiers: **WmiDataId** (3)</span></span>
</dt> </dl>

<span data-ttu-id="01174-169">Numero di settori in ogni traccia per questa unità disco fisica.</span><span class="sxs-lookup"><span data-stu-id="01174-169">Number of sectors in each track for this physical disk drive.</span></span>

</dd> <dt>

<span data-ttu-id="01174-170">**TracksPerCylinder**</span><span class="sxs-lookup"><span data-stu-id="01174-170">**TracksPerCylinder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01174-171">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="01174-171">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="01174-172">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="01174-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01174-173">Qualificatori: **WmiDataId** (4)</span><span class="sxs-lookup"><span data-stu-id="01174-173">Qualifiers: **WmiDataId** (4)</span></span>
</dt> </dl>

<span data-ttu-id="01174-174">Numero di tracce in ogni cilindro sull'unità disco fisica.</span><span class="sxs-lookup"><span data-stu-id="01174-174">Number of tracks in each cylinder on the physical disk drive.</span></span> <span data-ttu-id="01174-175">Nota: il valore di questa proprietà viene ottenuto tramite le funzioni estese dell'interrupt BIOS 13h.</span><span class="sxs-lookup"><span data-stu-id="01174-175">Note: the value for this property is obtained through extended functions of BIOS interrupt 13h.</span></span> <span data-ttu-id="01174-176">Il valore potrebbe non essere accurato se l'unità usa uno schema di conversione per supportare dimensioni del disco con capacità elevata.</span><span class="sxs-lookup"><span data-stu-id="01174-176">The value may be inaccurate if the drive uses a translation scheme to support high capacity disk sizes.</span></span> <span data-ttu-id="01174-177">Consultare il produttore per le specifiche di unità accurate.</span><span class="sxs-lookup"><span data-stu-id="01174-177">Consult the manufacturer for accurate drive specifications.</span></span>

</dd> <dt>

<span data-ttu-id="01174-178">**WriteCacheEnabled**</span><span class="sxs-lookup"><span data-stu-id="01174-178">**WriteCacheEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01174-179">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="01174-179">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="01174-180">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="01174-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01174-181">Qualificatori: **WmiDataId** (12)</span><span class="sxs-lookup"><span data-stu-id="01174-181">Qualifiers: **WmiDataId** (12)</span></span>
</dt> </dl>

<span data-ttu-id="01174-182">True se la cache di scrittura è abilitata.</span><span class="sxs-lookup"><span data-stu-id="01174-182">True if the write cache is enabled.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="01174-183">Requisiti</span><span class="sxs-lookup"><span data-stu-id="01174-183">Requirements</span></span>



| <span data-ttu-id="01174-184">Requisito</span><span class="sxs-lookup"><span data-stu-id="01174-184">Requirement</span></span> | <span data-ttu-id="01174-185">Valore</span><span class="sxs-lookup"><span data-stu-id="01174-185">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="01174-186">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="01174-186">Minimum supported client</span></span><br/> | <span data-ttu-id="01174-187">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="01174-187">None supported</span></span><br/>                            |
| <span data-ttu-id="01174-188">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="01174-188">Minimum supported server</span></span><br/> | <span data-ttu-id="01174-189">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="01174-189">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="01174-190">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="01174-190">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01174-191">**SystemConfig \_ V0**</span><span class="sxs-lookup"><span data-stu-id="01174-191">**SystemConfig\_V0**</span></span>](systemconfig-v0.md)
</dt> </dl>

 

 




