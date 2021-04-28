---
description: 'SystemConfig_PhyDisk: questa classe è la classe del tipo di evento per gli eventi di configurazione del disco fisico.'
ms.assetid: 850a6b2c-69e6-47ae-95ff-585fcc70c1c8
title: SystemConfig_PhyDisk classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_PhyDisk
- SystemConfig_PhyDisk.DiskNumber
- SystemConfig_PhyDisk.BytesPerSector
- SystemConfig_PhyDisk.SectorsPerTrack
- SystemConfig_PhyDisk.TracksPerCylinder
- SystemConfig_PhyDisk.Cylinders
- SystemConfig_PhyDisk.SCSIPort
- SystemConfig_PhyDisk.SCSIPath
- SystemConfig_PhyDisk.SCSITarget
- SystemConfig_PhyDisk.SCSILun
- SystemConfig_PhyDisk.Manufacturer
- SystemConfig_PhyDisk.PartitionCount
- SystemConfig_PhyDisk.WriteCacheEnabled
- SystemConfig_PhyDisk.Pad
- SystemConfig_PhyDisk.BootDriveLetter
- SystemConfig_PhyDisk.Spare
api_type:
- NA
api_location: ''
ms.openlocfilehash: 52ab249ab5087a1528317687d90f6d8fa665bc1a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106099"
---
# <a name="systemconfig_phydisk-class"></a><span data-ttu-id="ba738-103">Classe SystemConfig \_ PhyDisk</span><span class="sxs-lookup"><span data-stu-id="ba738-103">SystemConfig\_PhyDisk class</span></span>

<span data-ttu-id="ba738-104">Questa classe è la classe del tipo di evento per gli eventi di configurazione del disco fisico.</span><span class="sxs-lookup"><span data-stu-id="ba738-104">This class is the event type class for physical disk configuration events.</span></span>

<span data-ttu-id="ba738-105">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="ba738-105">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba738-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ba738-106">Syntax</span></span>

``` syntax
[EventType(11), EventTypeName("PhyDisk")]
class SystemConfig_PhyDisk : SystemConfig
{
  uint32 DiskNumber;
  uint32 BytesPerSector;
  uint32 SectorsPerTrack;
  uint32 TracksPerCylinder;
  uint64 Cylinders;
  uint32 SCSIPort;
  uint32 SCSIPath;
  uint32 SCSITarget;
  uint32 SCSILun;
  char16 Manufacturer[];
  uint32 PartitionCount;
  uint8  WriteCacheEnabled;
  uint8  Pad;
  char16 BootDriveLetter[];
  char16 Spare[];
};
```

## <a name="members"></a><span data-ttu-id="ba738-107">Members</span><span class="sxs-lookup"><span data-stu-id="ba738-107">Members</span></span>

<span data-ttu-id="ba738-108">La **classe \_ SystemConfig PhyDisk** include questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="ba738-108">The **SystemConfig\_PhyDisk** class has these types of members:</span></span>

-   [<span data-ttu-id="ba738-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ba738-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ba738-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ba738-110">Properties</span></span>

<span data-ttu-id="ba738-111">La **classe SystemConfig \_ PhyDisk** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="ba738-111">The **SystemConfig\_PhyDisk** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ba738-112">**BootDriveLetter**</span><span class="sxs-lookup"><span data-stu-id="ba738-112">**BootDriveLetter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba738-113">Tipo di dati: **matrice char16**</span><span class="sxs-lookup"><span data-stu-id="ba738-113">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="ba738-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ba738-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ba738-115">Qualificatori: **WmiDataId** (14), **Max** (3), **Format("s")**</span><span class="sxs-lookup"><span data-stu-id="ba738-115">Qualifiers: **WmiDataId** (14), **Max** (3), **Format("s")**</span></span>
</dt> </dl>

<span data-ttu-id="ba738-116">Lettera di unità dell'unità di avvio nel formato " <letter> :".</span><span class="sxs-lookup"><span data-stu-id="ba738-116">Drive letter of the boot drive in the form, "<letter>:".</span></span>

</dd> <dt>

<span data-ttu-id="ba738-117">**BytesPerSector**</span><span class="sxs-lookup"><span data-stu-id="ba738-117">**BytesPerSector**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba738-118">Tipo di dati: **uint32**</span><span class="sxs-lookup"><span data-stu-id="ba738-118">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ba738-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ba738-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ba738-120">Qualificatori: **WmiDataId** (2)</span><span class="sxs-lookup"><span data-stu-id="ba738-120">Qualifiers: **WmiDataId** (2)</span></span>
</dt> </dl>

<span data-ttu-id="ba738-121">Numero di byte in ogni settore per l'unità disco fisica.</span><span class="sxs-lookup"><span data-stu-id="ba738-121">Number of bytes in each sector for the physical disk drive.</span></span>

</dd> <dt>

<span data-ttu-id="ba738-122">**Cilindri**</span><span class="sxs-lookup"><span data-stu-id="ba738-122">**Cylinders**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba738-123">Tipo di dati: **uint64**</span><span class="sxs-lookup"><span data-stu-id="ba738-123">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ba738-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ba738-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ba738-125">Qualificatori: **WmiDataId** (5)</span><span class="sxs-lookup"><span data-stu-id="ba738-125">Qualifiers: **WmiDataId** (5)</span></span>
</dt> </dl>

<span data-ttu-id="ba738-126">Numero totale di cilindri nell'unità disco fisica.</span><span class="sxs-lookup"><span data-stu-id="ba738-126">Total number of cylinders on the physical disk drive.</span></span> <span data-ttu-id="ba738-127">Nota: il valore di questa proprietà viene ottenuto tramite funzioni estese dell'interrupt BIOS 13h.</span><span class="sxs-lookup"><span data-stu-id="ba738-127">Note: the value for this property is obtained through extended functions of BIOS interrupt 13h.</span></span> <span data-ttu-id="ba738-128">Il valore potrebbe non essere accurato se l'unità usa uno schema di conversione per supportare dimensioni del disco con capacità elevata.</span><span class="sxs-lookup"><span data-stu-id="ba738-128">The value may be inaccurate if the drive uses a translation scheme to support high capacity disk sizes.</span></span> <span data-ttu-id="ba738-129">Per specifiche di unità accurate, consultare il produttore.</span><span class="sxs-lookup"><span data-stu-id="ba738-129">Consult the manufacturer for accurate drive specifications.</span></span>

</dd> <dt>

<span data-ttu-id="ba738-130">**DiskNumber**</span><span class="sxs-lookup"><span data-stu-id="ba738-130">**DiskNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba738-131">Tipo di dati: **uint32**</span><span class="sxs-lookup"><span data-stu-id="ba738-131">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ba738-132">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ba738-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ba738-133">Qualificatori: **WmiDataId** (1)</span><span class="sxs-lookup"><span data-stu-id="ba738-133">Qualifiers: **WmiDataId** (1)</span></span>
</dt> </dl>

<span data-ttu-id="ba738-134">Numero di indice del disco contenente questa partizione.</span><span class="sxs-lookup"><span data-stu-id="ba738-134">Index number of the disk containing this partition.</span></span>

</dd> <dt>

<span data-ttu-id="ba738-135">**Produttore**</span><span class="sxs-lookup"><span data-stu-id="ba738-135">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba738-136">Tipo di dati: **matrice char16**</span><span class="sxs-lookup"><span data-stu-id="ba738-136">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="ba738-137">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ba738-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ba738-138">Qualificatori: **WmiDataId** (10), **Max** (256), **Format("s")**</span><span class="sxs-lookup"><span data-stu-id="ba738-138">Qualifiers: **WmiDataId** (10), **Max** (256), **Format("s")**</span></span>
</dt> </dl>

<span data-ttu-id="ba738-139">Nome del produttore dell'unità disco.</span><span class="sxs-lookup"><span data-stu-id="ba738-139">Name of the disk drive manufacturer.</span></span>

</dd> <dt>

<span data-ttu-id="ba738-140">**Riempimento**</span><span class="sxs-lookup"><span data-stu-id="ba738-140">**Pad**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba738-141">Tipo di dati: **uint8**</span><span class="sxs-lookup"><span data-stu-id="ba738-141">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="ba738-142">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ba738-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ba738-143">Qualificatori: **WmiDataId** (13)</span><span class="sxs-lookup"><span data-stu-id="ba738-143">Qualifiers: **WmiDataId** (13)</span></span>
</dt> </dl>

<span data-ttu-id="ba738-144">Non usato.</span><span class="sxs-lookup"><span data-stu-id="ba738-144">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="ba738-145">**PartitionCount**</span><span class="sxs-lookup"><span data-stu-id="ba738-145">**PartitionCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba738-146">Tipo di dati: **uint32**</span><span class="sxs-lookup"><span data-stu-id="ba738-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ba738-147">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ba738-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ba738-148">Qualificatori: **WmiDataId** (11)</span><span class="sxs-lookup"><span data-stu-id="ba738-148">Qualifiers: **WmiDataId** (11)</span></span>
</dt> </dl>

<span data-ttu-id="ba738-149">Numero di partizioni in questa unità disco fisico riconosciute dal sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="ba738-149">Number of partitions on this physical disk drive that are recognized by the operating system.</span></span>

</dd> <dt>

<span data-ttu-id="ba738-150">**SCSILun**</span><span class="sxs-lookup"><span data-stu-id="ba738-150">**SCSILun**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba738-151">Tipo di dati: **uint32**</span><span class="sxs-lookup"><span data-stu-id="ba738-151">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ba738-152">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ba738-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ba738-153">Qualificatori: **WmiDataId** (9)</span><span class="sxs-lookup"><span data-stu-id="ba738-153">Qualifiers: **WmiDataId** (9)</span></span>
</dt> </dl>

<span data-ttu-id="ba738-154">Numero di unità logica SCSI (LUN) della scheda SCSI.</span><span class="sxs-lookup"><span data-stu-id="ba738-154">SCSI logical unit number (LUN) of the SCSI adapter.</span></span>

</dd> <dt>

<span data-ttu-id="ba738-155">**SCSIPath**</span><span class="sxs-lookup"><span data-stu-id="ba738-155">**SCSIPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba738-156">Tipo di dati: **uint32**</span><span class="sxs-lookup"><span data-stu-id="ba738-156">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ba738-157">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ba738-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ba738-158">Qualificatori: **WmiDataId** (7)</span><span class="sxs-lookup"><span data-stu-id="ba738-158">Qualifiers: **WmiDataId** (7)</span></span>
</dt> </dl>

<span data-ttu-id="ba738-159">Numero di bus SCSI della scheda SCSI.</span><span class="sxs-lookup"><span data-stu-id="ba738-159">SCSI bus number of the SCSI adapter.</span></span>

</dd> <dt>

<span data-ttu-id="ba738-160">**SCSIPort**</span><span class="sxs-lookup"><span data-stu-id="ba738-160">**SCSIPort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba738-161">Tipo di dati: **uint32**</span><span class="sxs-lookup"><span data-stu-id="ba738-161">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ba738-162">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ba738-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ba738-163">Qualificatori: **WmiDataId** (6)</span><span class="sxs-lookup"><span data-stu-id="ba738-163">Qualifiers: **WmiDataId** (6)</span></span>
</dt> </dl>

<span data-ttu-id="ba738-164">Numero SCSI della scheda SCSI.</span><span class="sxs-lookup"><span data-stu-id="ba738-164">SCSI number of the SCSI adapter.</span></span>

</dd> <dt>

<span data-ttu-id="ba738-165">**SCSITarget**</span><span class="sxs-lookup"><span data-stu-id="ba738-165">**SCSITarget**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba738-166">Tipo di dati: **uint32**</span><span class="sxs-lookup"><span data-stu-id="ba738-166">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ba738-167">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ba738-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ba738-168">Qualificatori: **WmiDataId** (8)</span><span class="sxs-lookup"><span data-stu-id="ba738-168">Qualifiers: **WmiDataId** (8)</span></span>
</dt> </dl>

<span data-ttu-id="ba738-169">Contiene il numero del dispositivo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="ba738-169">Contains the number of the target device.</span></span>

</dd> <dt>

<span data-ttu-id="ba738-170">**SettoriPerTraccia**</span><span class="sxs-lookup"><span data-stu-id="ba738-170">**SectorsPerTrack**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba738-171">Tipo di dati: **uint32**</span><span class="sxs-lookup"><span data-stu-id="ba738-171">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ba738-172">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ba738-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ba738-173">Qualificatori: **WmiDataId** (3)</span><span class="sxs-lookup"><span data-stu-id="ba738-173">Qualifiers: **WmiDataId** (3)</span></span>
</dt> </dl>

<span data-ttu-id="ba738-174">Numero di settori in ogni traccia per questa unità disco fisica.</span><span class="sxs-lookup"><span data-stu-id="ba738-174">Number of sectors in each track for this physical disk drive.</span></span>

</dd> <dt>

<span data-ttu-id="ba738-175">**Ricambio**</span><span class="sxs-lookup"><span data-stu-id="ba738-175">**Spare**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba738-176">Tipo di dati: **matrice char16**</span><span class="sxs-lookup"><span data-stu-id="ba738-176">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="ba738-177">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ba738-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ba738-178">Qualificatori: **WmiDataId** (15), **Max** (2), **Format("s")**</span><span class="sxs-lookup"><span data-stu-id="ba738-178">Qualifiers: **WmiDataId** (15), **Max** (2), **Format("s")**</span></span>
</dt> </dl>

<span data-ttu-id="ba738-179">Non usato.</span><span class="sxs-lookup"><span data-stu-id="ba738-179">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="ba738-180">**TracksPerCylinder**</span><span class="sxs-lookup"><span data-stu-id="ba738-180">**TracksPerCylinder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba738-181">Tipo di dati: **uint32**</span><span class="sxs-lookup"><span data-stu-id="ba738-181">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ba738-182">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ba738-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ba738-183">Qualificatori: **WmiDataId** (4)</span><span class="sxs-lookup"><span data-stu-id="ba738-183">Qualifiers: **WmiDataId** (4)</span></span>
</dt> </dl>

<span data-ttu-id="ba738-184">Numero di tracce in ogni cilindro nell'unità disco fisico.</span><span class="sxs-lookup"><span data-stu-id="ba738-184">Number of tracks in each cylinder on the physical disk drive.</span></span> <span data-ttu-id="ba738-185">Nota: il valore di questa proprietà viene ottenuto tramite funzioni estese dell'interrupt BIOS 13 ore.</span><span class="sxs-lookup"><span data-stu-id="ba738-185">Note: the value for this property is obtained through extended functions of BIOS interrupt 13h.</span></span> <span data-ttu-id="ba738-186">Il valore potrebbe non essere accurato se l'unità usa uno schema di conversione per supportare dimensioni del disco con capacità elevata.</span><span class="sxs-lookup"><span data-stu-id="ba738-186">The value may be inaccurate if the drive uses a translation scheme to support high capacity disk sizes.</span></span> <span data-ttu-id="ba738-187">Per specifiche di unità accurate, rivolgersi al produttore.</span><span class="sxs-lookup"><span data-stu-id="ba738-187">Consult the manufacturer for accurate drive specifications.</span></span>

</dd> <dt>

<span data-ttu-id="ba738-188">**WriteCacheEnabled**</span><span class="sxs-lookup"><span data-stu-id="ba738-188">**WriteCacheEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba738-189">Tipo di dati: **uint8**</span><span class="sxs-lookup"><span data-stu-id="ba738-189">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="ba738-190">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ba738-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ba738-191">Qualificatori: **WmiDataId** (12)</span><span class="sxs-lookup"><span data-stu-id="ba738-191">Qualifiers: **WmiDataId** (12)</span></span>
</dt> </dl>

<span data-ttu-id="ba738-192">True se la cache di scrittura è abilitata.</span><span class="sxs-lookup"><span data-stu-id="ba738-192">True if the write cache is enabled.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ba738-193">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ba738-193">Requirements</span></span>



| <span data-ttu-id="ba738-194">Requisito</span><span class="sxs-lookup"><span data-stu-id="ba738-194">Requirement</span></span> | <span data-ttu-id="ba738-195">Valore</span><span class="sxs-lookup"><span data-stu-id="ba738-195">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ba738-196">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ba738-196">Minimum supported client</span></span><br/> | <span data-ttu-id="ba738-197">Solo app desktop di Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="ba738-197">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ba738-198">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ba738-198">Minimum supported server</span></span><br/> | <span data-ttu-id="ba738-199">Solo app desktop di Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="ba738-199">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ba738-200">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ba738-200">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba738-201">**SystemConfig**</span><span class="sxs-lookup"><span data-stu-id="ba738-201">**SystemConfig**</span></span>](systemconfig.md)
</dt> </dl>

 

 




