---
description: 'SystemConfig_LogDisk classe: questa classe è la classe del tipo di evento per gli eventi di configurazione del disco logico.'
ms.assetid: a11a8245-8ace-4061-b6c7-938002d8b9fc
title: SystemConfig_LogDisk classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_LogDisk
- SystemConfig_LogDisk.StartOffset
- SystemConfig_LogDisk.PartitionSize
- SystemConfig_LogDisk.DiskNumber
- SystemConfig_LogDisk.Size
- SystemConfig_LogDisk.DriveType
- SystemConfig_LogDisk.DriveLetterString
- SystemConfig_LogDisk.Pad1
- SystemConfig_LogDisk.PartitionNumber
- SystemConfig_LogDisk.SectorsPerCluster
- SystemConfig_LogDisk.BytesPerSector
- SystemConfig_LogDisk.Pad2
- SystemConfig_LogDisk.NumberOfFreeClusters
- SystemConfig_LogDisk.TotalNumberOfClusters
- SystemConfig_LogDisk.FileSystem
- SystemConfig_LogDisk.VolumeExt
- SystemConfig_LogDisk.Pad3
api_type:
- NA
api_location: ''
ms.openlocfilehash: 1d7ca8dc3f632e88c250715292a27e18ff36e3af
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106109"
---
# <a name="systemconfig_logdisk-class"></a><span data-ttu-id="4dbab-103">Classe SystemConfig \_ LogDisk</span><span class="sxs-lookup"><span data-stu-id="4dbab-103">SystemConfig\_LogDisk class</span></span>

<span data-ttu-id="4dbab-104">Questa classe è la classe del tipo di evento per gli eventi di configurazione del disco logico.</span><span class="sxs-lookup"><span data-stu-id="4dbab-104">This class is the event type class for logical disk configuration events.</span></span>

<span data-ttu-id="4dbab-105">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="4dbab-105">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="4dbab-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4dbab-106">Syntax</span></span>

``` syntax
[EventType(12), EventTypeName("LogDisk")]
class SystemConfig_LogDisk : SystemConfig
{
  uint64 StartOffset;
  uint64 PartitionSize;
  uint32 DiskNumber;
  uint32 Size;
  uint32 DriveType;
  char16 DriveLetterString[];
  uint32 Pad1;
  uint32 PartitionNumber;
  uint32 SectorsPerCluster;
  uint32 BytesPerSector;
  uint32 Pad2;
  sint64 NumberOfFreeClusters;
  sint64 TotalNumberOfClusters;
  char16 FileSystem;
  uint32 VolumeExt;
  uint32 Pad3;
};
```

## <a name="members"></a><span data-ttu-id="4dbab-107">Members</span><span class="sxs-lookup"><span data-stu-id="4dbab-107">Members</span></span>

<span data-ttu-id="4dbab-108">La **classe SystemConfig \_ LogDisk** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="4dbab-108">The **SystemConfig\_LogDisk** class has these types of members:</span></span>

-   [<span data-ttu-id="4dbab-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="4dbab-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4dbab-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="4dbab-110">Properties</span></span>

<span data-ttu-id="4dbab-111">La **classe SystemConfig \_ LogDisk** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="4dbab-111">The **SystemConfig\_LogDisk** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4dbab-112">**BytesPerSector**</span><span class="sxs-lookup"><span data-stu-id="4dbab-112">**BytesPerSector**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4dbab-113">Tipo di dati: **uint32**</span><span class="sxs-lookup"><span data-stu-id="4dbab-113">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4dbab-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4dbab-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4dbab-115">Qualificatori: **WmiDataId** (10)</span><span class="sxs-lookup"><span data-stu-id="4dbab-115">Qualifiers: **WmiDataId** (10)</span></span>
</dt> </dl>

<span data-ttu-id="4dbab-116">Numero di byte in ogni settore per l'unità disco fisico.</span><span class="sxs-lookup"><span data-stu-id="4dbab-116">Number of bytes in each sector for the physical disk drive.</span></span>

</dd> <dt>

<span data-ttu-id="4dbab-117">**DiskNumber**</span><span class="sxs-lookup"><span data-stu-id="4dbab-117">**DiskNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4dbab-118">Tipo di dati: **uint32**</span><span class="sxs-lookup"><span data-stu-id="4dbab-118">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4dbab-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4dbab-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4dbab-120">Qualificatori: **WmiDataId** (3)</span><span class="sxs-lookup"><span data-stu-id="4dbab-120">Qualifiers: **WmiDataId** (3)</span></span>
</dt> </dl>

<span data-ttu-id="4dbab-121">Numero di indice del disco contenente questa partizione.</span><span class="sxs-lookup"><span data-stu-id="4dbab-121">Index number of the disk containing this partition.</span></span>

</dd> <dt>

<span data-ttu-id="4dbab-122">**DriveLetterString**</span><span class="sxs-lookup"><span data-stu-id="4dbab-122">**DriveLetterString**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4dbab-123">Tipo di dati: **matrice char16**</span><span class="sxs-lookup"><span data-stu-id="4dbab-123">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="4dbab-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4dbab-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4dbab-125">Qualificatori: **WmiDataId** (6), **Max** (4), **Format("s")**</span><span class="sxs-lookup"><span data-stu-id="4dbab-125">Qualifiers: **WmiDataId** (6), **Max** (4), **Format("s")**</span></span>
</dt> </dl>

<span data-ttu-id="4dbab-126">Lettera di unità del disco nel formato " <letter> :".</span><span class="sxs-lookup"><span data-stu-id="4dbab-126">Drive letter of the disk in the form, "<letter>:".</span></span>

</dd> <dt>

<span data-ttu-id="4dbab-127">**DriveType**</span><span class="sxs-lookup"><span data-stu-id="4dbab-127">**DriveType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4dbab-128">Tipo di dati: **uint32**</span><span class="sxs-lookup"><span data-stu-id="4dbab-128">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4dbab-129">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4dbab-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4dbab-130">Qualificatori: **WmiDataId** (5)</span><span class="sxs-lookup"><span data-stu-id="4dbab-130">Qualifiers: **WmiDataId** (5)</span></span>
</dt> </dl>

<span data-ttu-id="4dbab-131">Tipo di unità disco.</span><span class="sxs-lookup"><span data-stu-id="4dbab-131">Type of disk drive.</span></span> <span data-ttu-id="4dbab-132">I valori possibili sono:</span><span class="sxs-lookup"><span data-stu-id="4dbab-132">Possible values are:</span></span>



| <span data-ttu-id="4dbab-133">Valore</span><span class="sxs-lookup"><span data-stu-id="4dbab-133">Value</span></span>                                                                        | <span data-ttu-id="4dbab-134">Significato</span><span class="sxs-lookup"><span data-stu-id="4dbab-134">Meaning</span></span>                                         |
|------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="4dbab-135"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="4dbab-135"><dt>1</dt></span></span> </dl> | <span data-ttu-id="4dbab-136">Partition</span><span class="sxs-lookup"><span data-stu-id="4dbab-136">Partition</span></span><br/>                            |
| <dl> <span data-ttu-id="4dbab-137"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="4dbab-137"><dt>2</dt></span></span> </dl> | <span data-ttu-id="4dbab-138">Volume</span><span class="sxs-lookup"><span data-stu-id="4dbab-138">Volume</span></span><br/>                               |
| <dl> <span data-ttu-id="4dbab-139"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="4dbab-139"><dt>3</dt></span></span> </dl> | <span data-ttu-id="4dbab-140">Partizione estesa su più dischi</span><span class="sxs-lookup"><span data-stu-id="4dbab-140">Extended partition on multiple disks</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="4dbab-141">**Filesystem**</span><span class="sxs-lookup"><span data-stu-id="4dbab-141">**FileSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4dbab-142">Tipo di dati: **char16**</span><span class="sxs-lookup"><span data-stu-id="4dbab-142">Data type: **char16**</span></span>
</dt> <dt>

<span data-ttu-id="4dbab-143">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4dbab-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4dbab-144">Qualificatori: **WmiDataId** (14), **Max** (16), **Format("s")**</span><span class="sxs-lookup"><span data-stu-id="4dbab-144">Qualifiers: **WmiDataId** (14), **Max** (16), **Format("s")**</span></span>
</dt> </dl>

<span data-ttu-id="4dbab-145">File system sul disco logico, ad esempio NTFS.</span><span class="sxs-lookup"><span data-stu-id="4dbab-145">File system on the logical disk, for example, NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="4dbab-146">**NumberOfFreeClusters**</span><span class="sxs-lookup"><span data-stu-id="4dbab-146">**NumberOfFreeClusters**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4dbab-147">Tipo di dati: **sint64**</span><span class="sxs-lookup"><span data-stu-id="4dbab-147">Data type: **sint64**</span></span>
</dt> <dt>

<span data-ttu-id="4dbab-148">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4dbab-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4dbab-149">Qualificatori: **WmiDataId** (12)</span><span class="sxs-lookup"><span data-stu-id="4dbab-149">Qualifiers: **WmiDataId** (12)</span></span>
</dt> </dl>

<span data-ttu-id="4dbab-150">Numero di cluster liberi nel volume specificato.</span><span class="sxs-lookup"><span data-stu-id="4dbab-150">Number of free clusters in the specified volume.</span></span>

</dd> <dt>

<span data-ttu-id="4dbab-151">**Pad1**</span><span class="sxs-lookup"><span data-stu-id="4dbab-151">**Pad1**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4dbab-152">Tipo di dati: **uint32**</span><span class="sxs-lookup"><span data-stu-id="4dbab-152">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4dbab-153">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4dbab-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4dbab-154">Qualificatori: **WmiDataId** (7)</span><span class="sxs-lookup"><span data-stu-id="4dbab-154">Qualifiers: **WmiDataId** (7)</span></span>
</dt> </dl>

<span data-ttu-id="4dbab-155">Non usato.</span><span class="sxs-lookup"><span data-stu-id="4dbab-155">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="4dbab-156">**Pad2**</span><span class="sxs-lookup"><span data-stu-id="4dbab-156">**Pad2**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4dbab-157">Tipo di dati: **uint32**</span><span class="sxs-lookup"><span data-stu-id="4dbab-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4dbab-158">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4dbab-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4dbab-159">Qualificatori: **WmiDataId** (11)</span><span class="sxs-lookup"><span data-stu-id="4dbab-159">Qualifiers: **WmiDataId** (11)</span></span>
</dt> </dl>

<span data-ttu-id="4dbab-160">Non usato.</span><span class="sxs-lookup"><span data-stu-id="4dbab-160">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="4dbab-161">**Pad3**</span><span class="sxs-lookup"><span data-stu-id="4dbab-161">**Pad3**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4dbab-162">Tipo di dati: **uint32**</span><span class="sxs-lookup"><span data-stu-id="4dbab-162">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4dbab-163">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4dbab-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4dbab-164">Qualificatori: **WmiDataId** (16)</span><span class="sxs-lookup"><span data-stu-id="4dbab-164">Qualifiers: **WmiDataId** (16)</span></span>
</dt> </dl>

<span data-ttu-id="4dbab-165">Non usato.</span><span class="sxs-lookup"><span data-stu-id="4dbab-165">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="4dbab-166">**PartitionNumber**</span><span class="sxs-lookup"><span data-stu-id="4dbab-166">**PartitionNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4dbab-167">Tipo di dati: **uint32**</span><span class="sxs-lookup"><span data-stu-id="4dbab-167">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4dbab-168">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4dbab-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4dbab-169">Qualificatori: **WmiDataId** (8)</span><span class="sxs-lookup"><span data-stu-id="4dbab-169">Qualifiers: **WmiDataId** (8)</span></span>
</dt> </dl>

<span data-ttu-id="4dbab-170">Numero di indice della partizione.</span><span class="sxs-lookup"><span data-stu-id="4dbab-170">Index number of the partition.</span></span>

</dd> <dt>

<span data-ttu-id="4dbab-171">**PartitionSize**</span><span class="sxs-lookup"><span data-stu-id="4dbab-171">**PartitionSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4dbab-172">Tipo di dati: **uint64**</span><span class="sxs-lookup"><span data-stu-id="4dbab-172">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4dbab-173">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4dbab-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4dbab-174">Qualificatori: **WmiDataId** (2)</span><span class="sxs-lookup"><span data-stu-id="4dbab-174">Qualifiers: **WmiDataId** (2)</span></span>
</dt> </dl>

<span data-ttu-id="4dbab-175">Dimensioni totali della partizione, in byte.</span><span class="sxs-lookup"><span data-stu-id="4dbab-175">Total size of the partition, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="4dbab-176">**SettoriPerCluster**</span><span class="sxs-lookup"><span data-stu-id="4dbab-176">**SectorsPerCluster**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4dbab-177">Tipo di dati: **uint32**</span><span class="sxs-lookup"><span data-stu-id="4dbab-177">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4dbab-178">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4dbab-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4dbab-179">Qualificatori: **WmiDataId** (9)</span><span class="sxs-lookup"><span data-stu-id="4dbab-179">Qualifiers: **WmiDataId** (9)</span></span>
</dt> </dl>

<span data-ttu-id="4dbab-180">Numero di settori nel volume.</span><span class="sxs-lookup"><span data-stu-id="4dbab-180">Number of sectors in the volume.</span></span>

</dd> <dt>

<span data-ttu-id="4dbab-181">**Size**</span><span class="sxs-lookup"><span data-stu-id="4dbab-181">**Size**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4dbab-182">Tipo di dati: **uint32**</span><span class="sxs-lookup"><span data-stu-id="4dbab-182">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4dbab-183">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4dbab-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4dbab-184">Qualificatori: **WmiDataId** (4)</span><span class="sxs-lookup"><span data-stu-id="4dbab-184">Qualifiers: **WmiDataId** (4)</span></span>
</dt> </dl>

<span data-ttu-id="4dbab-185">Dimensioni dell'unità disco, in byte.</span><span class="sxs-lookup"><span data-stu-id="4dbab-185">Size of the disk drive, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="4dbab-186">**StartOffset**</span><span class="sxs-lookup"><span data-stu-id="4dbab-186">**StartOffset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4dbab-187">Tipo di dati: **uint64**</span><span class="sxs-lookup"><span data-stu-id="4dbab-187">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4dbab-188">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4dbab-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4dbab-189">Qualificatori: **WmiDataId** (1)</span><span class="sxs-lookup"><span data-stu-id="4dbab-189">Qualifiers: **WmiDataId** (1)</span></span>
</dt> </dl>

<span data-ttu-id="4dbab-190">Offset iniziale (in byte) della partizione dall'inizio del disco.</span><span class="sxs-lookup"><span data-stu-id="4dbab-190">Starting offset (in bytes) of the partition from the beginning of the disk.</span></span>

</dd> <dt>

<span data-ttu-id="4dbab-191">**TotalNumberOfClusters**</span><span class="sxs-lookup"><span data-stu-id="4dbab-191">**TotalNumberOfClusters**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4dbab-192">Tipo di dati: **sint64**</span><span class="sxs-lookup"><span data-stu-id="4dbab-192">Data type: **sint64**</span></span>
</dt> <dt>

<span data-ttu-id="4dbab-193">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4dbab-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4dbab-194">Qualificatori: **WmiDataId** (13)</span><span class="sxs-lookup"><span data-stu-id="4dbab-194">Qualifiers: **WmiDataId** (13)</span></span>
</dt> </dl>

<span data-ttu-id="4dbab-195">Numero di cluster usati e gratuiti nel volume.</span><span class="sxs-lookup"><span data-stu-id="4dbab-195">Number of used and free clusters in the volume.</span></span>

</dd> <dt>

<span data-ttu-id="4dbab-196">**VolumeExt**</span><span class="sxs-lookup"><span data-stu-id="4dbab-196">**VolumeExt**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4dbab-197">Tipo di dati: **uint32**</span><span class="sxs-lookup"><span data-stu-id="4dbab-197">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4dbab-198">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4dbab-198">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4dbab-199">Qualificatori: **WmiDataId** (15)</span><span class="sxs-lookup"><span data-stu-id="4dbab-199">Qualifiers: **WmiDataId** (15)</span></span>
</dt> </dl>

<span data-ttu-id="4dbab-200">Riservato.</span><span class="sxs-lookup"><span data-stu-id="4dbab-200">Reserved.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4dbab-201">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4dbab-201">Requirements</span></span>



| <span data-ttu-id="4dbab-202">Requisito</span><span class="sxs-lookup"><span data-stu-id="4dbab-202">Requirement</span></span> | <span data-ttu-id="4dbab-203">Valore</span><span class="sxs-lookup"><span data-stu-id="4dbab-203">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="4dbab-204">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4dbab-204">Minimum supported client</span></span><br/> | <span data-ttu-id="4dbab-205">Solo app desktop di Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="4dbab-205">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="4dbab-206">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4dbab-206">Minimum supported server</span></span><br/> | <span data-ttu-id="4dbab-207">Solo app desktop di Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="4dbab-207">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4dbab-208">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4dbab-208">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4dbab-209">**SystemConfig**</span><span class="sxs-lookup"><span data-stu-id="4dbab-209">**SystemConfig**</span></span>](systemconfig.md)
</dt> </dl>

 

 




