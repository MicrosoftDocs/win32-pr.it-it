---
description: 'SystemConfig_V0_PhyDisk classe: questa classe è la classe del tipo di evento per gli eventi di configurazione del disco fisico.'
ms.assetid: 90ca3089-de5c-4e15-8abf-eaab9aafff06
title: SystemConfig_V0_PhyDisk classe
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
ms.openlocfilehash: fdb12fac8b2b902f21258fd4c7cfe9846d0456eb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105959"
---
# <a name="systemconfig_v0_phydisk-class"></a><span data-ttu-id="c0207-103">Classe SystemConfig \_ V0 \_ PhyDisk</span><span class="sxs-lookup"><span data-stu-id="c0207-103">SystemConfig\_V0\_PhyDisk class</span></span>

<span data-ttu-id="c0207-104">Questa classe è la classe del tipo di evento per gli eventi di configurazione del disco fisico.</span><span class="sxs-lookup"><span data-stu-id="c0207-104">This class is the event type class for physical disk configuration events.</span></span>

<span data-ttu-id="c0207-105">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="c0207-105">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0207-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c0207-106">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="c0207-107">Members</span><span class="sxs-lookup"><span data-stu-id="c0207-107">Members</span></span>

<span data-ttu-id="c0207-108">La **classe SystemConfig \_ V0 \_ PhyDisk** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="c0207-108">The **SystemConfig\_V0\_PhyDisk** class has these types of members:</span></span>

-   [<span data-ttu-id="c0207-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c0207-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c0207-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c0207-110">Properties</span></span>

<span data-ttu-id="c0207-111">La **classe SystemConfig \_ V0 \_ PhyDisk** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="c0207-111">The **SystemConfig\_V0\_PhyDisk** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c0207-112">**BootDriveLetter**</span><span class="sxs-lookup"><span data-stu-id="c0207-112">**BootDriveLetter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0207-113">Tipo di dati: **matrice char16**</span><span class="sxs-lookup"><span data-stu-id="c0207-113">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="c0207-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c0207-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0207-115">Qualificatori: **WmiDataId** (13), **Max** (3)</span><span class="sxs-lookup"><span data-stu-id="c0207-115">Qualifiers: **WmiDataId** (13), **Max** (3)</span></span>
</dt> </dl>

<span data-ttu-id="c0207-116">Lettera di unità dell'unità di avvio nel formato " <letter> :".</span><span class="sxs-lookup"><span data-stu-id="c0207-116">Drive letter of the boot drive in the form, "<letter>:".</span></span>

</dd> <dt>

<span data-ttu-id="c0207-117">**BytesPerSector**</span><span class="sxs-lookup"><span data-stu-id="c0207-117">**BytesPerSector**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0207-118">Tipo di dati: **uint32**</span><span class="sxs-lookup"><span data-stu-id="c0207-118">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c0207-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c0207-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0207-120">Qualificatori: **WmiDataId** (2)</span><span class="sxs-lookup"><span data-stu-id="c0207-120">Qualifiers: **WmiDataId** (2)</span></span>
</dt> </dl>

<span data-ttu-id="c0207-121">Numero di byte in ogni settore per l'unità disco fisico.</span><span class="sxs-lookup"><span data-stu-id="c0207-121">Number of bytes in each sector for the physical disk drive.</span></span>

</dd> <dt>

<span data-ttu-id="c0207-122">**Cilindri**</span><span class="sxs-lookup"><span data-stu-id="c0207-122">**Cylinders**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0207-123">Tipo di dati: **uint64**</span><span class="sxs-lookup"><span data-stu-id="c0207-123">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c0207-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c0207-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0207-125">Qualificatori: **WmiDataId** (5)</span><span class="sxs-lookup"><span data-stu-id="c0207-125">Qualifiers: **WmiDataId** (5)</span></span>
</dt> </dl>

<span data-ttu-id="c0207-126">Numero totale di cilindri nell'unità disco fisico.</span><span class="sxs-lookup"><span data-stu-id="c0207-126">Total number of cylinders on the physical disk drive.</span></span> <span data-ttu-id="c0207-127">Nota: il valore di questa proprietà viene ottenuto tramite funzioni estese dell'interrupt BIOS 13 ore.</span><span class="sxs-lookup"><span data-stu-id="c0207-127">Note: the value for this property is obtained through extended functions of BIOS interrupt 13h.</span></span> <span data-ttu-id="c0207-128">Il valore potrebbe non essere accurato se l'unità usa uno schema di conversione per supportare dimensioni del disco con capacità elevata.</span><span class="sxs-lookup"><span data-stu-id="c0207-128">The value may be inaccurate if the drive uses a translation scheme to support high capacity disk sizes.</span></span> <span data-ttu-id="c0207-129">Per specifiche di unità accurate, rivolgersi al produttore.</span><span class="sxs-lookup"><span data-stu-id="c0207-129">Consult the manufacturer for accurate drive specifications.</span></span>

</dd> <dt>

<span data-ttu-id="c0207-130">**DiskNumber**</span><span class="sxs-lookup"><span data-stu-id="c0207-130">**DiskNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0207-131">Tipo di dati: **uint32**</span><span class="sxs-lookup"><span data-stu-id="c0207-131">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c0207-132">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c0207-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0207-133">Qualificatori: **WmiDataId** (1)</span><span class="sxs-lookup"><span data-stu-id="c0207-133">Qualifiers: **WmiDataId** (1)</span></span>
</dt> </dl>

<span data-ttu-id="c0207-134">Numero di indice del disco contenente la partizione.</span><span class="sxs-lookup"><span data-stu-id="c0207-134">Index number of the disk containing this partition.</span></span>

</dd> <dt>

<span data-ttu-id="c0207-135">**Produttore**</span><span class="sxs-lookup"><span data-stu-id="c0207-135">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0207-136">Tipo di dati: **matrice char16**</span><span class="sxs-lookup"><span data-stu-id="c0207-136">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="c0207-137">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c0207-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0207-138">Qualificatori: **WmiDataId** (10), **Max** (256)</span><span class="sxs-lookup"><span data-stu-id="c0207-138">Qualifiers: **WmiDataId** (10), **Max** (256)</span></span>
</dt> </dl>

<span data-ttu-id="c0207-139">Nome del produttore dell'unità disco.</span><span class="sxs-lookup"><span data-stu-id="c0207-139">Name of the disk drive manufacturer.</span></span>

</dd> <dt>

<span data-ttu-id="c0207-140">**PartitionCount**</span><span class="sxs-lookup"><span data-stu-id="c0207-140">**PartitionCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0207-141">Tipo di dati: **uint32**</span><span class="sxs-lookup"><span data-stu-id="c0207-141">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c0207-142">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c0207-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0207-143">Qualificatori: **WmiDataId** (11)</span><span class="sxs-lookup"><span data-stu-id="c0207-143">Qualifiers: **WmiDataId** (11)</span></span>
</dt> </dl>

<span data-ttu-id="c0207-144">Numero di partizioni in questa unità disco fisica riconosciute dal sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="c0207-144">Number of partitions on this physical disk drive that are recognized by the operating system.</span></span>

</dd> <dt>

<span data-ttu-id="c0207-145">**SCSILun**</span><span class="sxs-lookup"><span data-stu-id="c0207-145">**SCSILun**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0207-146">Tipo di dati: **uint32**</span><span class="sxs-lookup"><span data-stu-id="c0207-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c0207-147">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c0207-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0207-148">Qualificatori: **WmiDataId** (9)</span><span class="sxs-lookup"><span data-stu-id="c0207-148">Qualifiers: **WmiDataId** (9)</span></span>
</dt> </dl>

<span data-ttu-id="c0207-149">Numero di unità logica SCSI (LUN) della scheda SCSI.</span><span class="sxs-lookup"><span data-stu-id="c0207-149">SCSI logical unit number (LUN) of the SCSI adapter.</span></span>

</dd> <dt>

<span data-ttu-id="c0207-150">**SCSIPath**</span><span class="sxs-lookup"><span data-stu-id="c0207-150">**SCSIPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0207-151">Tipo di dati: **uint32**</span><span class="sxs-lookup"><span data-stu-id="c0207-151">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c0207-152">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c0207-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0207-153">Qualificatori: **WmiDataId** (7)</span><span class="sxs-lookup"><span data-stu-id="c0207-153">Qualifiers: **WmiDataId** (7)</span></span>
</dt> </dl>

<span data-ttu-id="c0207-154">Numero di bus SCSI della scheda SCSI.</span><span class="sxs-lookup"><span data-stu-id="c0207-154">SCSI bus number of the SCSI adapter.</span></span>

</dd> <dt>

<span data-ttu-id="c0207-155">**SCSIPort**</span><span class="sxs-lookup"><span data-stu-id="c0207-155">**SCSIPort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0207-156">Tipo di dati: **uint32**</span><span class="sxs-lookup"><span data-stu-id="c0207-156">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c0207-157">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c0207-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0207-158">Qualificatori: **WmiDataId** (6)</span><span class="sxs-lookup"><span data-stu-id="c0207-158">Qualifiers: **WmiDataId** (6)</span></span>
</dt> </dl>

<span data-ttu-id="c0207-159">Numero SCSI della scheda SCSI.</span><span class="sxs-lookup"><span data-stu-id="c0207-159">SCSI number of the SCSI adapter.</span></span>

</dd> <dt>

<span data-ttu-id="c0207-160">**SCSITarget**</span><span class="sxs-lookup"><span data-stu-id="c0207-160">**SCSITarget**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0207-161">Tipo di dati: **uint32**</span><span class="sxs-lookup"><span data-stu-id="c0207-161">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c0207-162">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c0207-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0207-163">Qualificatori: **WmiDataId** (8)</span><span class="sxs-lookup"><span data-stu-id="c0207-163">Qualifiers: **WmiDataId** (8)</span></span>
</dt> </dl>

<span data-ttu-id="c0207-164">Contiene il numero del dispositivo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="c0207-164">Contains the number of the target device.</span></span>

</dd> <dt>

<span data-ttu-id="c0207-165">**SectorsPerTrack**</span><span class="sxs-lookup"><span data-stu-id="c0207-165">**SectorsPerTrack**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0207-166">Tipo di dati: **uint32**</span><span class="sxs-lookup"><span data-stu-id="c0207-166">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c0207-167">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c0207-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0207-168">Qualificatori: **WmiDataId** (3)</span><span class="sxs-lookup"><span data-stu-id="c0207-168">Qualifiers: **WmiDataId** (3)</span></span>
</dt> </dl>

<span data-ttu-id="c0207-169">Numero di settori in ogni traccia per questa unità disco fisico.</span><span class="sxs-lookup"><span data-stu-id="c0207-169">Number of sectors in each track for this physical disk drive.</span></span>

</dd> <dt>

<span data-ttu-id="c0207-170">**TracksPerCylinder**</span><span class="sxs-lookup"><span data-stu-id="c0207-170">**TracksPerCylinder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0207-171">Tipo di dati: **uint32**</span><span class="sxs-lookup"><span data-stu-id="c0207-171">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c0207-172">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c0207-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0207-173">Qualificatori: **WmiDataId** (4)</span><span class="sxs-lookup"><span data-stu-id="c0207-173">Qualifiers: **WmiDataId** (4)</span></span>
</dt> </dl>

<span data-ttu-id="c0207-174">Numero di tracce in ogni cilindro nell'unità disco fisico.</span><span class="sxs-lookup"><span data-stu-id="c0207-174">Number of tracks in each cylinder on the physical disk drive.</span></span> <span data-ttu-id="c0207-175">Nota: il valore di questa proprietà viene ottenuto tramite funzioni estese dell'interrupt BIOS 13 ore.</span><span class="sxs-lookup"><span data-stu-id="c0207-175">Note: the value for this property is obtained through extended functions of BIOS interrupt 13h.</span></span> <span data-ttu-id="c0207-176">Il valore potrebbe non essere accurato se l'unità usa uno schema di conversione per supportare dimensioni del disco con capacità elevata.</span><span class="sxs-lookup"><span data-stu-id="c0207-176">The value may be inaccurate if the drive uses a translation scheme to support high capacity disk sizes.</span></span> <span data-ttu-id="c0207-177">Per specifiche di unità accurate, rivolgersi al produttore.</span><span class="sxs-lookup"><span data-stu-id="c0207-177">Consult the manufacturer for accurate drive specifications.</span></span>

</dd> <dt>

<span data-ttu-id="c0207-178">**WriteCacheEnabled**</span><span class="sxs-lookup"><span data-stu-id="c0207-178">**WriteCacheEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0207-179">Tipo di dati: **booleano**</span><span class="sxs-lookup"><span data-stu-id="c0207-179">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c0207-180">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c0207-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0207-181">Qualificatori: **WmiDataId** (12)</span><span class="sxs-lookup"><span data-stu-id="c0207-181">Qualifiers: **WmiDataId** (12)</span></span>
</dt> </dl>

<span data-ttu-id="c0207-182">True se la cache di scrittura è abilitata.</span><span class="sxs-lookup"><span data-stu-id="c0207-182">True if the write cache is enabled.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c0207-183">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c0207-183">Requirements</span></span>



| <span data-ttu-id="c0207-184">Requisito</span><span class="sxs-lookup"><span data-stu-id="c0207-184">Requirement</span></span> | <span data-ttu-id="c0207-185">Valore</span><span class="sxs-lookup"><span data-stu-id="c0207-185">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c0207-186">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c0207-186">Minimum supported client</span></span><br/> | <span data-ttu-id="c0207-187">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="c0207-187">None supported</span></span><br/>                            |
| <span data-ttu-id="c0207-188">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c0207-188">Minimum supported server</span></span><br/> | <span data-ttu-id="c0207-189">Solo app desktop di Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="c0207-189">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c0207-190">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c0207-190">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0207-191">**SystemConfig \_ V0**</span><span class="sxs-lookup"><span data-stu-id="c0207-191">**SystemConfig\_V0**</span></span>](systemconfig-v0.md)
</dt> </dl>

 

 




