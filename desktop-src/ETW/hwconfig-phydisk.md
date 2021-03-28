---
description: La \_ classe HWConfig PhyDisk è la classe del tipo di evento per gli eventi di configurazione del disco fisico. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: b134ab45-b161-452f-be84-ccbdfa3fe4af
title: Classe HWConfig_PhyDisk
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HWConfig_PhyDisk
- HWConfig_PhyDisk.DiskNumber
- HWConfig_PhyDisk.BytesPerSector
- HWConfig_PhyDisk.SectorsPerTrack
- HWConfig_PhyDisk.TracksPerCylinder
- HWConfig_PhyDisk.Cylinders
- HWConfig_PhyDisk.SCSIPort
- HWConfig_PhyDisk.SCSIPath
- HWConfig_PhyDisk.SCSITarget
- HWConfig_PhyDisk.SCSILun
- HWConfig_PhyDisk.Manufacturer
api_type:
- NA
api_location: ''
ms.openlocfilehash: 453f06ae11bb8b1e11c9efddd6f63bffd38540e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977655"
---
# <a name="hwconfig_phydisk-class"></a><span data-ttu-id="9d59c-104">\_Classe HWConfig PhyDisk</span><span class="sxs-lookup"><span data-stu-id="9d59c-104">HWConfig\_PhyDisk class</span></span>

<span data-ttu-id="9d59c-105">La classe **HWConfig \_ PhyDisk** è la classe del tipo di evento per gli eventi di configurazione del disco fisico.</span><span class="sxs-lookup"><span data-stu-id="9d59c-105">The **HWConfig\_PhyDisk** class is the event type class for physical disk configuration events.</span></span>

<span data-ttu-id="9d59c-106">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="9d59c-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d59c-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9d59c-107">Syntax</span></span>

``` syntax
[EventType(11), EventTypeName("PhyDisk")]
class HWConfig_PhyDisk : HWConfig
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
  string Manufacturer;
};
```

## <a name="members"></a><span data-ttu-id="9d59c-108">Members</span><span class="sxs-lookup"><span data-stu-id="9d59c-108">Members</span></span>

<span data-ttu-id="9d59c-109">La **classe \_ PhyDisk di HWConfig** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="9d59c-109">The **HWConfig\_PhyDisk** class has these types of members:</span></span>

-   [<span data-ttu-id="9d59c-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="9d59c-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9d59c-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="9d59c-111">Properties</span></span>

<span data-ttu-id="9d59c-112">La **classe \_ PhyDisk di HWConfig** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="9d59c-112">The **HWConfig\_PhyDisk** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9d59c-113">BytesPerSector</span><span class="sxs-lookup"><span data-stu-id="9d59c-113">BytesPerSector</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d59c-114">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9d59c-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9d59c-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9d59c-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9d59c-116">Qualificatori: WmiDataId (2)</span><span class="sxs-lookup"><span data-stu-id="9d59c-116">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="9d59c-117">Numero di byte in ogni settore per l'unità disco fisica.</span><span class="sxs-lookup"><span data-stu-id="9d59c-117">Number of bytes in each sector for the physical disk drive.</span></span>

</dd> <dt>

<span data-ttu-id="9d59c-118">Cilindri</span><span class="sxs-lookup"><span data-stu-id="9d59c-118">Cylinders</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d59c-119">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9d59c-119">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9d59c-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9d59c-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9d59c-121">Qualificatori: WmiDataId (5)</span><span class="sxs-lookup"><span data-stu-id="9d59c-121">Qualifiers: WmiDataId(5)</span></span>
</dt> </dl>

<span data-ttu-id="9d59c-122">Numero totale di cilindri sull'unità disco fisica.</span><span class="sxs-lookup"><span data-stu-id="9d59c-122">Total number of cylinders on the physical disk drive.</span></span> <span data-ttu-id="9d59c-123">Nota: il valore di questa proprietà viene ottenuto tramite le funzioni estese dell'interrupt BIOS 13h.</span><span class="sxs-lookup"><span data-stu-id="9d59c-123">Note: the value for this property is obtained through extended functions of BIOS interrupt 13h.</span></span> <span data-ttu-id="9d59c-124">Il valore potrebbe non essere accurato se l'unità usa uno schema di conversione per supportare dimensioni del disco con capacità elevata.</span><span class="sxs-lookup"><span data-stu-id="9d59c-124">The value may be inaccurate if the drive uses a translation scheme to support high capacity disk sizes.</span></span> <span data-ttu-id="9d59c-125">Consultare il produttore per le specifiche di unità accurate.</span><span class="sxs-lookup"><span data-stu-id="9d59c-125">Consult the manufacturer for accurate drive specifications.</span></span>

</dd> <dt>

<span data-ttu-id="9d59c-126">Numerodisco</span><span class="sxs-lookup"><span data-stu-id="9d59c-126">DiskNumber</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d59c-127">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9d59c-127">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9d59c-128">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9d59c-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9d59c-129">Qualificatori: WmiDataId (1)</span><span class="sxs-lookup"><span data-stu-id="9d59c-129">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="9d59c-130">Numero di indice del disco contenente questa partizione.</span><span class="sxs-lookup"><span data-stu-id="9d59c-130">Index number of the disk containing this partition.</span></span>

</dd> <dt>

<span data-ttu-id="9d59c-131">Produttore</span><span class="sxs-lookup"><span data-stu-id="9d59c-131">Manufacturer</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d59c-132">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9d59c-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9d59c-133">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9d59c-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9d59c-134">Qualificatori: WmiDataId (10), StringTermination ("NullTerminated"), Format ("w")</span><span class="sxs-lookup"><span data-stu-id="9d59c-134">Qualifiers: WmiDataId(10), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="9d59c-135">Nome del produttore dell'unità disco.</span><span class="sxs-lookup"><span data-stu-id="9d59c-135">Name of the disk drive manufacturer.</span></span>

</dd> <dt>

<span data-ttu-id="9d59c-136">SCSILun</span><span class="sxs-lookup"><span data-stu-id="9d59c-136">SCSILun</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d59c-137">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9d59c-137">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9d59c-138">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9d59c-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9d59c-139">Qualificatori: WmiDataId (9)</span><span class="sxs-lookup"><span data-stu-id="9d59c-139">Qualifiers: WmiDataId(9)</span></span>
</dt> </dl>

<span data-ttu-id="9d59c-140">Numero di unità logica (LUN) SCSI della scheda SCSI.</span><span class="sxs-lookup"><span data-stu-id="9d59c-140">SCSI logical unit number (LUN) of the SCSI adapter.</span></span>

</dd> <dt>

<span data-ttu-id="9d59c-141">SCSIPath</span><span class="sxs-lookup"><span data-stu-id="9d59c-141">SCSIPath</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d59c-142">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9d59c-142">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9d59c-143">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9d59c-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9d59c-144">Qualificatori: WmiDataId (7)</span><span class="sxs-lookup"><span data-stu-id="9d59c-144">Qualifiers: WmiDataId(7)</span></span>
</dt> </dl>

<span data-ttu-id="9d59c-145">Numero del bus SCSI della scheda SCSI.</span><span class="sxs-lookup"><span data-stu-id="9d59c-145">SCSI bus number of the SCSI adapter.</span></span>

</dd> <dt>

<span data-ttu-id="9d59c-146">SCSIPort</span><span class="sxs-lookup"><span data-stu-id="9d59c-146">SCSIPort</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d59c-147">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9d59c-147">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9d59c-148">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9d59c-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9d59c-149">Qualificatori: WmiDataId (6)</span><span class="sxs-lookup"><span data-stu-id="9d59c-149">Qualifiers: WmiDataId(6)</span></span>
</dt> </dl>

<span data-ttu-id="9d59c-150">Numero SCSI della scheda SCSI.</span><span class="sxs-lookup"><span data-stu-id="9d59c-150">SCSI number of the SCSI adapter.</span></span>

</dd> <dt>

<span data-ttu-id="9d59c-151">SCSITarget</span><span class="sxs-lookup"><span data-stu-id="9d59c-151">SCSITarget</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d59c-152">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9d59c-152">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9d59c-153">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9d59c-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9d59c-154">Qualificatori: WmiDataId (8)</span><span class="sxs-lookup"><span data-stu-id="9d59c-154">Qualifiers: WmiDataId(8)</span></span>
</dt> </dl>

<span data-ttu-id="9d59c-155">Contiene il numero del dispositivo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="9d59c-155">Contains the number of the target device.</span></span>

</dd> <dt>

<span data-ttu-id="9d59c-156">SectorsPerTrack</span><span class="sxs-lookup"><span data-stu-id="9d59c-156">SectorsPerTrack</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d59c-157">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9d59c-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9d59c-158">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9d59c-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9d59c-159">Qualificatori: WmiDataId (3)</span><span class="sxs-lookup"><span data-stu-id="9d59c-159">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="9d59c-160">Numero di settori in ogni traccia per questa unità disco fisica.</span><span class="sxs-lookup"><span data-stu-id="9d59c-160">Number of sectors in each track for this physical disk drive.</span></span>

</dd> <dt>

<span data-ttu-id="9d59c-161">TracksPerCylinder</span><span class="sxs-lookup"><span data-stu-id="9d59c-161">TracksPerCylinder</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d59c-162">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9d59c-162">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9d59c-163">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9d59c-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9d59c-164">Qualificatori: WmiDataId (4)</span><span class="sxs-lookup"><span data-stu-id="9d59c-164">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="9d59c-165">Numero di tracce in ogni cilindro sull'unità disco fisica.</span><span class="sxs-lookup"><span data-stu-id="9d59c-165">Number of tracks in each cylinder on the physical disk drive.</span></span> <span data-ttu-id="9d59c-166">Nota: il valore di questa proprietà viene ottenuto tramite le funzioni estese dell'interrupt BIOS 13h.</span><span class="sxs-lookup"><span data-stu-id="9d59c-166">Note: the value for this property is obtained through extended functions of BIOS interrupt 13h.</span></span> <span data-ttu-id="9d59c-167">Il valore potrebbe non essere accurato se l'unità usa uno schema di conversione per supportare dimensioni del disco con capacità elevata.</span><span class="sxs-lookup"><span data-stu-id="9d59c-167">The value may be inaccurate if the drive uses a translation scheme to support high capacity disk sizes.</span></span> <span data-ttu-id="9d59c-168">Consultare il produttore per le specifiche di unità accurate.</span><span class="sxs-lookup"><span data-stu-id="9d59c-168">Consult the manufacturer for accurate drive specifications.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9d59c-169">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9d59c-169">Requirements</span></span>



| <span data-ttu-id="9d59c-170">Requisito</span><span class="sxs-lookup"><span data-stu-id="9d59c-170">Requirement</span></span> | <span data-ttu-id="9d59c-171">Valore</span><span class="sxs-lookup"><span data-stu-id="9d59c-171">Value</span></span> |
|-------------------------------------|---------------------------------------------|
| <span data-ttu-id="9d59c-172">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9d59c-172">Minimum supported client</span></span><br/> | <span data-ttu-id="9d59c-173">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="9d59c-173">Windows XP \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="9d59c-174">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9d59c-174">Minimum supported server</span></span><br/> | <span data-ttu-id="9d59c-175">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="9d59c-175">None supported</span></span><br/>                   |



## <a name="see-also"></a><span data-ttu-id="9d59c-176">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9d59c-176">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d59c-177">**HWConfig**</span><span class="sxs-lookup"><span data-stu-id="9d59c-177">**HWConfig**</span></span>](hwconfig.md)
</dt> </dl>

 

 




