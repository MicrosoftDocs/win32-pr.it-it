---
description: 'SystemConfig_V0_LogDisk: questa classe è la classe del tipo di evento per gli eventi di configurazione del disco logico.'
ms.assetid: 3fa5f2e4-f6fa-4c10-9634-04908783cd28
title: SystemConfig_V0_LogDisk classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_V0_LogDisk
- SystemConfig_V0_LogDisk.StartOffset
- SystemConfig_V0_LogDisk.PartitionSize
- SystemConfig_V0_LogDisk.DiskNumber
- SystemConfig_V0_LogDisk.Size
- SystemConfig_V0_LogDisk.DriveType
- SystemConfig_V0_LogDisk.DriveLetterString
- SystemConfig_V0_LogDisk.Pad
- SystemConfig_V0_LogDisk.PartitionNumber
- SystemConfig_V0_LogDisk.SectorsPerCluster
- SystemConfig_V0_LogDisk.BytesPerSector
- SystemConfig_V0_LogDisk.NumberOfFreeClusters
- SystemConfig_V0_LogDisk.TotalNumberOfClusters
- SystemConfig_V0_LogDisk.FileSystem
- SystemConfig_V0_LogDisk.VolumeExt
api_type:
- NA
api_location: ''
ms.openlocfilehash: eb0ad959d637a38a03b77bd8d7a812ff608ddc04
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105979"
---
# <a name="systemconfig_v0_logdisk-class"></a><span data-ttu-id="ab40b-103">Classe SystemConfig \_ V0 \_ LogDisk</span><span class="sxs-lookup"><span data-stu-id="ab40b-103">SystemConfig\_V0\_LogDisk class</span></span>

<span data-ttu-id="ab40b-104">Questa classe è la classe del tipo di evento per gli eventi di configurazione del disco logico.</span><span class="sxs-lookup"><span data-stu-id="ab40b-104">This class is the event type class for logical disk configuration events.</span></span>

<span data-ttu-id="ab40b-105">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="ab40b-105">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab40b-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ab40b-106">Syntax</span></span>

``` syntax
[EventType(12), EventTypeName("LogDisk")]
class SystemConfig_V0_LogDisk : SystemConfig_V0
{
  uint64 StartOffset;
  uint64 PartitionSize;
  uint32 DiskNumber;
  uint32 Size;
  uint32 DriveType;
  char16 DriveLetterString[];
  uint32 Pad;
  uint32 PartitionNumber;
  uint32 SectorsPerCluster;
  uint32 BytesPerSector;
  sint64 NumberOfFreeClusters;
  sint64 TotalNumberOfClusters;
  char16 FileSystem;
  uint32 VolumeExt;
};
```

## <a name="members"></a><span data-ttu-id="ab40b-107">Members</span><span class="sxs-lookup"><span data-stu-id="ab40b-107">Members</span></span>

<span data-ttu-id="ab40b-108">La **classe SystemConfig \_ V0 \_ LogDisk** include questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="ab40b-108">The **SystemConfig\_V0\_LogDisk** class has these types of members:</span></span>

-   [<span data-ttu-id="ab40b-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ab40b-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ab40b-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ab40b-110">Properties</span></span>

<span data-ttu-id="ab40b-111">La **classe SystemConfig \_ V0 \_ LogDisk** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="ab40b-111">The **SystemConfig\_V0\_LogDisk** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ab40b-112">**BytesPerSector**</span><span class="sxs-lookup"><span data-stu-id="ab40b-112">**BytesPerSector**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab40b-113">Tipo di dati: **uint32**</span><span class="sxs-lookup"><span data-stu-id="ab40b-113">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ab40b-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ab40b-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ab40b-115">Qualificatori: **WmiDataId** (10)</span><span class="sxs-lookup"><span data-stu-id="ab40b-115">Qualifiers: **WmiDataId** (10)</span></span>
</dt> </dl>

<span data-ttu-id="ab40b-116">Numero di byte in ogni settore per l'unità disco fisica.</span><span class="sxs-lookup"><span data-stu-id="ab40b-116">Number of bytes in each sector for the physical disk drive.</span></span>

</dd> <dt>

<span data-ttu-id="ab40b-117">**DiskNumber**</span><span class="sxs-lookup"><span data-stu-id="ab40b-117">**DiskNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab40b-118">Tipo di dati: **uint32**</span><span class="sxs-lookup"><span data-stu-id="ab40b-118">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ab40b-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ab40b-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ab40b-120">Qualificatori: **WmiDataId** (3)</span><span class="sxs-lookup"><span data-stu-id="ab40b-120">Qualifiers: **WmiDataId** (3)</span></span>
</dt> </dl>

<span data-ttu-id="ab40b-121">Numero di indice del disco contenente la partizione.</span><span class="sxs-lookup"><span data-stu-id="ab40b-121">Index number of the disk containing this partition.</span></span>

</dd> <dt>

<span data-ttu-id="ab40b-122">**DriveLetterString**</span><span class="sxs-lookup"><span data-stu-id="ab40b-122">**DriveLetterString**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab40b-123">Tipo di dati: **matrice char16**</span><span class="sxs-lookup"><span data-stu-id="ab40b-123">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="ab40b-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ab40b-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ab40b-125">Qualificatori: **WmiDataId** (6), **Max** (4)</span><span class="sxs-lookup"><span data-stu-id="ab40b-125">Qualifiers: **WmiDataId** (6), **Max** (4)</span></span>
</dt> </dl>

<span data-ttu-id="ab40b-126">Lettera di unità del disco nel formato " <letter> :".</span><span class="sxs-lookup"><span data-stu-id="ab40b-126">Drive letter of the disk in the form, "<letter>:".</span></span>

</dd> <dt>

<span data-ttu-id="ab40b-127">**DriveType**</span><span class="sxs-lookup"><span data-stu-id="ab40b-127">**DriveType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab40b-128">Tipo di dati: **uint32**</span><span class="sxs-lookup"><span data-stu-id="ab40b-128">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ab40b-129">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ab40b-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ab40b-130">Qualificatori: **WmiDataId** (5)</span><span class="sxs-lookup"><span data-stu-id="ab40b-130">Qualifiers: **WmiDataId** (5)</span></span>
</dt> </dl>

<span data-ttu-id="ab40b-131">Tipo di unità disco.</span><span class="sxs-lookup"><span data-stu-id="ab40b-131">Type of disk drive.</span></span> <span data-ttu-id="ab40b-132">I valori possibili sono:</span><span class="sxs-lookup"><span data-stu-id="ab40b-132">Possible values are:</span></span>



| <span data-ttu-id="ab40b-133">Valore</span><span class="sxs-lookup"><span data-stu-id="ab40b-133">Value</span></span>                                                                        | <span data-ttu-id="ab40b-134">Significato</span><span class="sxs-lookup"><span data-stu-id="ab40b-134">Meaning</span></span>                                         |
|------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="ab40b-135"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="ab40b-135"><dt>1</dt></span></span> </dl> | <span data-ttu-id="ab40b-136">Partition</span><span class="sxs-lookup"><span data-stu-id="ab40b-136">Partition</span></span><br/>                            |
| <dl> <span data-ttu-id="ab40b-137"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="ab40b-137"><dt>2</dt></span></span> </dl> | <span data-ttu-id="ab40b-138">Volume</span><span class="sxs-lookup"><span data-stu-id="ab40b-138">Volume</span></span><br/>                               |
| <dl> <span data-ttu-id="ab40b-139"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="ab40b-139"><dt>3</dt></span></span> </dl> | <span data-ttu-id="ab40b-140">Partizione estesa su più dischi</span><span class="sxs-lookup"><span data-stu-id="ab40b-140">Extended partition on multiple disks</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="ab40b-141">**Filesystem**</span><span class="sxs-lookup"><span data-stu-id="ab40b-141">**FileSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab40b-142">Tipo di dati: **char16**</span><span class="sxs-lookup"><span data-stu-id="ab40b-142">Data type: **char16**</span></span>
</dt> <dt>

<span data-ttu-id="ab40b-143">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ab40b-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ab40b-144">Qualificatori: **WmiDataId** (13), **Max** (16)</span><span class="sxs-lookup"><span data-stu-id="ab40b-144">Qualifiers: **WmiDataId** (13), **Max** (16)</span></span>
</dt> </dl>

<span data-ttu-id="ab40b-145">File system sul disco logico, ad esempio NTFS.</span><span class="sxs-lookup"><span data-stu-id="ab40b-145">File system on the logical disk, for example, NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="ab40b-146">**NumberOfFreeClusters**</span><span class="sxs-lookup"><span data-stu-id="ab40b-146">**NumberOfFreeClusters**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab40b-147">Tipo di dati: **sint64**</span><span class="sxs-lookup"><span data-stu-id="ab40b-147">Data type: **sint64**</span></span>
</dt> <dt>

<span data-ttu-id="ab40b-148">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ab40b-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ab40b-149">Qualificatori: **WmiDataId** (11)</span><span class="sxs-lookup"><span data-stu-id="ab40b-149">Qualifiers: **WmiDataId** (11)</span></span>
</dt> </dl>

<span data-ttu-id="ab40b-150">Numero di cluster liberi nel volume specificato.</span><span class="sxs-lookup"><span data-stu-id="ab40b-150">Number of free clusters in the specified volume.</span></span>

</dd> <dt>

<span data-ttu-id="ab40b-151">**Riempimento**</span><span class="sxs-lookup"><span data-stu-id="ab40b-151">**Pad**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab40b-152">Tipo di dati: **uint32**</span><span class="sxs-lookup"><span data-stu-id="ab40b-152">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ab40b-153">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ab40b-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ab40b-154">Qualificatori: **WmiDataId** (7)</span><span class="sxs-lookup"><span data-stu-id="ab40b-154">Qualifiers: **WmiDataId** (7)</span></span>
</dt> </dl>

<span data-ttu-id="ab40b-155">Riservato.</span><span class="sxs-lookup"><span data-stu-id="ab40b-155">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="ab40b-156">**PartitionNumber**</span><span class="sxs-lookup"><span data-stu-id="ab40b-156">**PartitionNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab40b-157">Tipo di dati: **uint32**</span><span class="sxs-lookup"><span data-stu-id="ab40b-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ab40b-158">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ab40b-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ab40b-159">Qualificatori: **WmiDataId** (8)</span><span class="sxs-lookup"><span data-stu-id="ab40b-159">Qualifiers: **WmiDataId** (8)</span></span>
</dt> </dl>

<span data-ttu-id="ab40b-160">Numero di indice della partizione.</span><span class="sxs-lookup"><span data-stu-id="ab40b-160">Index number of the partition.</span></span>

</dd> <dt>

<span data-ttu-id="ab40b-161">**PartitionSize**</span><span class="sxs-lookup"><span data-stu-id="ab40b-161">**PartitionSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab40b-162">Tipo di dati: **uint64**</span><span class="sxs-lookup"><span data-stu-id="ab40b-162">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ab40b-163">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ab40b-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ab40b-164">Qualificatori: **WmiDataId** (2)</span><span class="sxs-lookup"><span data-stu-id="ab40b-164">Qualifiers: **WmiDataId** (2)</span></span>
</dt> </dl>

<span data-ttu-id="ab40b-165">Dimensioni totali della partizione, in byte.</span><span class="sxs-lookup"><span data-stu-id="ab40b-165">Total size of the partition, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="ab40b-166">**SettoriPerCluster**</span><span class="sxs-lookup"><span data-stu-id="ab40b-166">**SectorsPerCluster**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab40b-167">Tipo di dati: **uint32**</span><span class="sxs-lookup"><span data-stu-id="ab40b-167">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ab40b-168">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ab40b-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ab40b-169">Qualificatori: **WmiDataId** (9)</span><span class="sxs-lookup"><span data-stu-id="ab40b-169">Qualifiers: **WmiDataId** (9)</span></span>
</dt> </dl>

<span data-ttu-id="ab40b-170">Numero di settori nel volume.</span><span class="sxs-lookup"><span data-stu-id="ab40b-170">Number of sectors in the volume.</span></span>

</dd> <dt>

<span data-ttu-id="ab40b-171">**Size**</span><span class="sxs-lookup"><span data-stu-id="ab40b-171">**Size**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab40b-172">Tipo di dati: **uint32**</span><span class="sxs-lookup"><span data-stu-id="ab40b-172">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ab40b-173">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ab40b-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ab40b-174">Qualificatori: **WmiDataId** (4)</span><span class="sxs-lookup"><span data-stu-id="ab40b-174">Qualifiers: **WmiDataId** (4)</span></span>
</dt> </dl>

<span data-ttu-id="ab40b-175">Dimensioni dell'unità disco, in byte.</span><span class="sxs-lookup"><span data-stu-id="ab40b-175">Size of the disk drive, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="ab40b-176">**StartOffset**</span><span class="sxs-lookup"><span data-stu-id="ab40b-176">**StartOffset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab40b-177">Tipo di dati: **uint64**</span><span class="sxs-lookup"><span data-stu-id="ab40b-177">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ab40b-178">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ab40b-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ab40b-179">Qualificatori: **WmiDataId** (1)</span><span class="sxs-lookup"><span data-stu-id="ab40b-179">Qualifiers: **WmiDataId** (1)</span></span>
</dt> </dl>

<span data-ttu-id="ab40b-180">Offset iniziale (in byte) della partizione dall'inizio del disco.</span><span class="sxs-lookup"><span data-stu-id="ab40b-180">Starting offset (in bytes) of the partition from the beginning of the disk.</span></span>

</dd> <dt>

<span data-ttu-id="ab40b-181">**TotalNumberOfClusters**</span><span class="sxs-lookup"><span data-stu-id="ab40b-181">**TotalNumberOfClusters**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab40b-182">Tipo di dati: **sint64**</span><span class="sxs-lookup"><span data-stu-id="ab40b-182">Data type: **sint64**</span></span>
</dt> <dt>

<span data-ttu-id="ab40b-183">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ab40b-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ab40b-184">Qualificatori: **WmiDataId** (12)</span><span class="sxs-lookup"><span data-stu-id="ab40b-184">Qualifiers: **WmiDataId** (12)</span></span>
</dt> </dl>

<span data-ttu-id="ab40b-185">Numero di cluster usati e gratuiti nel volume.</span><span class="sxs-lookup"><span data-stu-id="ab40b-185">Number of used and free clusters in the volume.</span></span>

</dd> <dt>

<span data-ttu-id="ab40b-186">**VolumeExt**</span><span class="sxs-lookup"><span data-stu-id="ab40b-186">**VolumeExt**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab40b-187">Tipo di dati: **uint32**</span><span class="sxs-lookup"><span data-stu-id="ab40b-187">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ab40b-188">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ab40b-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ab40b-189">Qualificatori: **WmiDataId** (14)</span><span class="sxs-lookup"><span data-stu-id="ab40b-189">Qualifiers: **WmiDataId** (14)</span></span>
</dt> </dl>

<span data-ttu-id="ab40b-190">Riservato.</span><span class="sxs-lookup"><span data-stu-id="ab40b-190">Reserved.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ab40b-191">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ab40b-191">Requirements</span></span>



| <span data-ttu-id="ab40b-192">Requisito</span><span class="sxs-lookup"><span data-stu-id="ab40b-192">Requirement</span></span> | <span data-ttu-id="ab40b-193">Valore</span><span class="sxs-lookup"><span data-stu-id="ab40b-193">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ab40b-194">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ab40b-194">Minimum supported client</span></span><br/> | <span data-ttu-id="ab40b-195">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="ab40b-195">None supported</span></span><br/>                            |
| <span data-ttu-id="ab40b-196">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ab40b-196">Minimum supported server</span></span><br/> | <span data-ttu-id="ab40b-197">Solo app desktop di Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="ab40b-197">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ab40b-198">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ab40b-198">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab40b-199">**SystemConfig \_ V0**</span><span class="sxs-lookup"><span data-stu-id="ab40b-199">**SystemConfig\_V0**</span></span>](systemconfig-v0.md)
</dt> </dl>

 

 




