---
description: Questa classe è la classe del tipo di evento per gli eventi di configurazione del disco fisico.
ms.assetid: 850a6b2c-69e6-47ae-95ff-585fcc70c1c8
title: Classe SystemConfig_PhyDisk
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
ms.openlocfilehash: d868e3943f22a71b4513f4f77841ddea9204ffea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977479"
---
# <a name="systemconfig_phydisk-class"></a><span data-ttu-id="b5e3e-103">\_Classe SystemConfig PhyDisk</span><span class="sxs-lookup"><span data-stu-id="b5e3e-103">SystemConfig\_PhyDisk class</span></span>

<span data-ttu-id="b5e3e-104">Questa classe è la classe del tipo di evento per gli eventi di configurazione del disco fisico.</span><span class="sxs-lookup"><span data-stu-id="b5e3e-104">This class is the event type class for physical disk configuration events.</span></span>

<span data-ttu-id="b5e3e-105">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="b5e3e-105">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5e3e-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b5e3e-106">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="b5e3e-107">Members</span><span class="sxs-lookup"><span data-stu-id="b5e3e-107">Members</span></span>

<span data-ttu-id="b5e3e-108">La **classe \_ PhyDisk di SystemConfig** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="b5e3e-108">The **SystemConfig\_PhyDisk** class has these types of members:</span></span>

-   [<span data-ttu-id="b5e3e-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b5e3e-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b5e3e-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b5e3e-110">Properties</span></span>

<span data-ttu-id="b5e3e-111">La **classe \_ PhyDisk di SystemConfig** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="b5e3e-111">The **SystemConfig\_PhyDisk** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b5e3e-112">**BootDriveLetter**</span><span class="sxs-lookup"><span data-stu-id="b5e3e-112">**BootDriveLetter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5e3e-113">Tipo di dati: matrice **Char16**</span><span class="sxs-lookup"><span data-stu-id="b5e3e-113">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="b5e3e-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b5e3e-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5e3e-115">Qualificatori: **WmiDataId** (14), **Max** (3), **Format ("s")**</span><span class="sxs-lookup"><span data-stu-id="b5e3e-115">Qualifiers: **WmiDataId** (14), **Max** (3), **Format("s")**</span></span>
</dt> </dl>

<span data-ttu-id="b5e3e-116">Lettera di unità dell'unità di avvio nel formato " <letter> :".</span><span class="sxs-lookup"><span data-stu-id="b5e3e-116">Drive letter of the boot drive in the form, "<letter>:".</span></span>

</dd> <dt>

<span data-ttu-id="b5e3e-117">**BytesPerSector**</span><span class="sxs-lookup"><span data-stu-id="b5e3e-117">**BytesPerSector**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5e3e-118">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b5e3e-118">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b5e3e-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b5e3e-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5e3e-120">Qualificatori: **WmiDataId** (2)</span><span class="sxs-lookup"><span data-stu-id="b5e3e-120">Qualifiers: **WmiDataId** (2)</span></span>
</dt> </dl>

<span data-ttu-id="b5e3e-121">Numero di byte in ogni settore per l'unità disco fisica.</span><span class="sxs-lookup"><span data-stu-id="b5e3e-121">Number of bytes in each sector for the physical disk drive.</span></span>

</dd> <dt>

<span data-ttu-id="b5e3e-122">**Cilindri**</span><span class="sxs-lookup"><span data-stu-id="b5e3e-122">**Cylinders**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5e3e-123">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b5e3e-123">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b5e3e-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b5e3e-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5e3e-125">Qualificatori: **WmiDataId** (5)</span><span class="sxs-lookup"><span data-stu-id="b5e3e-125">Qualifiers: **WmiDataId** (5)</span></span>
</dt> </dl>

<span data-ttu-id="b5e3e-126">Numero totale di cilindri sull'unità disco fisica.</span><span class="sxs-lookup"><span data-stu-id="b5e3e-126">Total number of cylinders on the physical disk drive.</span></span> <span data-ttu-id="b5e3e-127">Nota: il valore di questa proprietà viene ottenuto tramite le funzioni estese dell'interrupt BIOS 13h.</span><span class="sxs-lookup"><span data-stu-id="b5e3e-127">Note: the value for this property is obtained through extended functions of BIOS interrupt 13h.</span></span> <span data-ttu-id="b5e3e-128">Il valore potrebbe non essere accurato se l'unità usa uno schema di conversione per supportare dimensioni del disco con capacità elevata.</span><span class="sxs-lookup"><span data-stu-id="b5e3e-128">The value may be inaccurate if the drive uses a translation scheme to support high capacity disk sizes.</span></span> <span data-ttu-id="b5e3e-129">Consultare il produttore per le specifiche di unità accurate.</span><span class="sxs-lookup"><span data-stu-id="b5e3e-129">Consult the manufacturer for accurate drive specifications.</span></span>

</dd> <dt>

<span data-ttu-id="b5e3e-130">**Numerodisco**</span><span class="sxs-lookup"><span data-stu-id="b5e3e-130">**DiskNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5e3e-131">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b5e3e-131">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b5e3e-132">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b5e3e-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5e3e-133">Qualificatori: **WmiDataId** (1)</span><span class="sxs-lookup"><span data-stu-id="b5e3e-133">Qualifiers: **WmiDataId** (1)</span></span>
</dt> </dl>

<span data-ttu-id="b5e3e-134">Numero di indice del disco contenente questa partizione.</span><span class="sxs-lookup"><span data-stu-id="b5e3e-134">Index number of the disk containing this partition.</span></span>

</dd> <dt>

<span data-ttu-id="b5e3e-135">**Produttore**</span><span class="sxs-lookup"><span data-stu-id="b5e3e-135">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5e3e-136">Tipo di dati: matrice **Char16**</span><span class="sxs-lookup"><span data-stu-id="b5e3e-136">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="b5e3e-137">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b5e3e-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5e3e-138">Qualificatori: **WmiDataId** (10), **Max** (256), **Format ("s")**</span><span class="sxs-lookup"><span data-stu-id="b5e3e-138">Qualifiers: **WmiDataId** (10), **Max** (256), **Format("s")**</span></span>
</dt> </dl>

<span data-ttu-id="b5e3e-139">Nome del produttore dell'unità disco.</span><span class="sxs-lookup"><span data-stu-id="b5e3e-139">Name of the disk drive manufacturer.</span></span>

</dd> <dt>

<span data-ttu-id="b5e3e-140">**Pad**</span><span class="sxs-lookup"><span data-stu-id="b5e3e-140">**Pad**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5e3e-141">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="b5e3e-141">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="b5e3e-142">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b5e3e-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5e3e-143">Qualificatori: **WmiDataId** (13)</span><span class="sxs-lookup"><span data-stu-id="b5e3e-143">Qualifiers: **WmiDataId** (13)</span></span>
</dt> </dl>

<span data-ttu-id="b5e3e-144">Non usato.</span><span class="sxs-lookup"><span data-stu-id="b5e3e-144">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="b5e3e-145">**PartitionCount**</span><span class="sxs-lookup"><span data-stu-id="b5e3e-145">**PartitionCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5e3e-146">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b5e3e-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b5e3e-147">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b5e3e-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5e3e-148">Qualificatori: **WmiDataId** (11)</span><span class="sxs-lookup"><span data-stu-id="b5e3e-148">Qualifiers: **WmiDataId** (11)</span></span>
</dt> </dl>

<span data-ttu-id="b5e3e-149">Numero di partizioni in questa unità disco fisica riconosciute dal sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="b5e3e-149">Number of partitions on this physical disk drive that are recognized by the operating system.</span></span>

</dd> <dt>

<span data-ttu-id="b5e3e-150">**SCSILun**</span><span class="sxs-lookup"><span data-stu-id="b5e3e-150">**SCSILun**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5e3e-151">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b5e3e-151">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b5e3e-152">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b5e3e-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5e3e-153">Qualificatori: **WmiDataId** (9)</span><span class="sxs-lookup"><span data-stu-id="b5e3e-153">Qualifiers: **WmiDataId** (9)</span></span>
</dt> </dl>

<span data-ttu-id="b5e3e-154">Numero di unità logica (LUN) SCSI della scheda SCSI.</span><span class="sxs-lookup"><span data-stu-id="b5e3e-154">SCSI logical unit number (LUN) of the SCSI adapter.</span></span>

</dd> <dt>

<span data-ttu-id="b5e3e-155">**SCSIPath**</span><span class="sxs-lookup"><span data-stu-id="b5e3e-155">**SCSIPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5e3e-156">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b5e3e-156">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b5e3e-157">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b5e3e-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5e3e-158">Qualificatori: **WmiDataId** (7)</span><span class="sxs-lookup"><span data-stu-id="b5e3e-158">Qualifiers: **WmiDataId** (7)</span></span>
</dt> </dl>

<span data-ttu-id="b5e3e-159">Numero del bus SCSI della scheda SCSI.</span><span class="sxs-lookup"><span data-stu-id="b5e3e-159">SCSI bus number of the SCSI adapter.</span></span>

</dd> <dt>

<span data-ttu-id="b5e3e-160">**SCSIPort**</span><span class="sxs-lookup"><span data-stu-id="b5e3e-160">**SCSIPort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5e3e-161">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b5e3e-161">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b5e3e-162">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b5e3e-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5e3e-163">Qualificatori: **WmiDataId** (6)</span><span class="sxs-lookup"><span data-stu-id="b5e3e-163">Qualifiers: **WmiDataId** (6)</span></span>
</dt> </dl>

<span data-ttu-id="b5e3e-164">Numero SCSI della scheda SCSI.</span><span class="sxs-lookup"><span data-stu-id="b5e3e-164">SCSI number of the SCSI adapter.</span></span>

</dd> <dt>

<span data-ttu-id="b5e3e-165">**SCSITarget**</span><span class="sxs-lookup"><span data-stu-id="b5e3e-165">**SCSITarget**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5e3e-166">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b5e3e-166">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b5e3e-167">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b5e3e-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5e3e-168">Qualificatori: **WmiDataId** (8)</span><span class="sxs-lookup"><span data-stu-id="b5e3e-168">Qualifiers: **WmiDataId** (8)</span></span>
</dt> </dl>

<span data-ttu-id="b5e3e-169">Contiene il numero del dispositivo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="b5e3e-169">Contains the number of the target device.</span></span>

</dd> <dt>

<span data-ttu-id="b5e3e-170">**SectorsPerTrack**</span><span class="sxs-lookup"><span data-stu-id="b5e3e-170">**SectorsPerTrack**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5e3e-171">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b5e3e-171">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b5e3e-172">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b5e3e-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5e3e-173">Qualificatori: **WmiDataId** (3)</span><span class="sxs-lookup"><span data-stu-id="b5e3e-173">Qualifiers: **WmiDataId** (3)</span></span>
</dt> </dl>

<span data-ttu-id="b5e3e-174">Numero di settori in ogni traccia per questa unità disco fisica.</span><span class="sxs-lookup"><span data-stu-id="b5e3e-174">Number of sectors in each track for this physical disk drive.</span></span>

</dd> <dt>

<span data-ttu-id="b5e3e-175">**Ricambio**</span><span class="sxs-lookup"><span data-stu-id="b5e3e-175">**Spare**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5e3e-176">Tipo di dati: matrice **Char16**</span><span class="sxs-lookup"><span data-stu-id="b5e3e-176">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="b5e3e-177">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b5e3e-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5e3e-178">Qualificatori: **WmiDataId** (15), **Max** (2), **Format ("s")**</span><span class="sxs-lookup"><span data-stu-id="b5e3e-178">Qualifiers: **WmiDataId** (15), **Max** (2), **Format("s")**</span></span>
</dt> </dl>

<span data-ttu-id="b5e3e-179">Non usato.</span><span class="sxs-lookup"><span data-stu-id="b5e3e-179">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="b5e3e-180">**TracksPerCylinder**</span><span class="sxs-lookup"><span data-stu-id="b5e3e-180">**TracksPerCylinder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5e3e-181">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b5e3e-181">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b5e3e-182">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b5e3e-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5e3e-183">Qualificatori: **WmiDataId** (4)</span><span class="sxs-lookup"><span data-stu-id="b5e3e-183">Qualifiers: **WmiDataId** (4)</span></span>
</dt> </dl>

<span data-ttu-id="b5e3e-184">Numero di tracce in ogni cilindro sull'unità disco fisica.</span><span class="sxs-lookup"><span data-stu-id="b5e3e-184">Number of tracks in each cylinder on the physical disk drive.</span></span> <span data-ttu-id="b5e3e-185">Nota: il valore di questa proprietà viene ottenuto tramite le funzioni estese dell'interrupt BIOS 13h.</span><span class="sxs-lookup"><span data-stu-id="b5e3e-185">Note: the value for this property is obtained through extended functions of BIOS interrupt 13h.</span></span> <span data-ttu-id="b5e3e-186">Il valore potrebbe non essere accurato se l'unità usa uno schema di conversione per supportare dimensioni del disco con capacità elevata.</span><span class="sxs-lookup"><span data-stu-id="b5e3e-186">The value may be inaccurate if the drive uses a translation scheme to support high capacity disk sizes.</span></span> <span data-ttu-id="b5e3e-187">Consultare il produttore per le specifiche di unità accurate.</span><span class="sxs-lookup"><span data-stu-id="b5e3e-187">Consult the manufacturer for accurate drive specifications.</span></span>

</dd> <dt>

<span data-ttu-id="b5e3e-188">**WriteCacheEnabled**</span><span class="sxs-lookup"><span data-stu-id="b5e3e-188">**WriteCacheEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5e3e-189">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="b5e3e-189">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="b5e3e-190">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b5e3e-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5e3e-191">Qualificatori: **WmiDataId** (12)</span><span class="sxs-lookup"><span data-stu-id="b5e3e-191">Qualifiers: **WmiDataId** (12)</span></span>
</dt> </dl>

<span data-ttu-id="b5e3e-192">True se la cache di scrittura è abilitata.</span><span class="sxs-lookup"><span data-stu-id="b5e3e-192">True if the write cache is enabled.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b5e3e-193">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b5e3e-193">Requirements</span></span>



| <span data-ttu-id="b5e3e-194">Requisito</span><span class="sxs-lookup"><span data-stu-id="b5e3e-194">Requirement</span></span> | <span data-ttu-id="b5e3e-195">Valore</span><span class="sxs-lookup"><span data-stu-id="b5e3e-195">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b5e3e-196">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b5e3e-196">Minimum supported client</span></span><br/> | <span data-ttu-id="b5e3e-197">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b5e3e-197">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="b5e3e-198">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b5e3e-198">Minimum supported server</span></span><br/> | <span data-ttu-id="b5e3e-199">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b5e3e-199">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b5e3e-200">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b5e3e-200">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5e3e-201">**SystemConfig**</span><span class="sxs-lookup"><span data-stu-id="b5e3e-201">**SystemConfig**</span></span>](systemconfig.md)
</dt> </dl>

 

 




