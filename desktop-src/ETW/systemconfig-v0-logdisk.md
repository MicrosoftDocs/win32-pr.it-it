---
description: Questa classe è la classe del tipo di evento per gli eventi di configurazione del disco logico.
ms.assetid: 3fa5f2e4-f6fa-4c10-9634-04908783cd28
title: Classe SystemConfig_V0_LogDisk
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
ms.openlocfilehash: dbc1ee189bae1fe71f42267f38bd40763764dea2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980546"
---
# <a name="systemconfig_v0_logdisk-class"></a><span data-ttu-id="a81f5-103">\_Classe SystemConfig V0 \_ LogDisk</span><span class="sxs-lookup"><span data-stu-id="a81f5-103">SystemConfig\_V0\_LogDisk class</span></span>

<span data-ttu-id="a81f5-104">Questa classe è la classe del tipo di evento per gli eventi di configurazione del disco logico.</span><span class="sxs-lookup"><span data-stu-id="a81f5-104">This class is the event type class for logical disk configuration events.</span></span>

<span data-ttu-id="a81f5-105">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="a81f5-105">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="a81f5-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a81f5-106">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="a81f5-107">Members</span><span class="sxs-lookup"><span data-stu-id="a81f5-107">Members</span></span>

<span data-ttu-id="a81f5-108">La classe **SystemConfig \_ V0 \_ LogDisk** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="a81f5-108">The **SystemConfig\_V0\_LogDisk** class has these types of members:</span></span>

-   [<span data-ttu-id="a81f5-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a81f5-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a81f5-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a81f5-110">Properties</span></span>

<span data-ttu-id="a81f5-111">La classe **SystemConfig \_ V0 \_ LogDisk** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="a81f5-111">The **SystemConfig\_V0\_LogDisk** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a81f5-112">**BytesPerSector**</span><span class="sxs-lookup"><span data-stu-id="a81f5-112">**BytesPerSector**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a81f5-113">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a81f5-113">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a81f5-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a81f5-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a81f5-115">Qualificatori: **WmiDataId** (10)</span><span class="sxs-lookup"><span data-stu-id="a81f5-115">Qualifiers: **WmiDataId** (10)</span></span>
</dt> </dl>

<span data-ttu-id="a81f5-116">Numero di byte in ogni settore per l'unità disco fisica.</span><span class="sxs-lookup"><span data-stu-id="a81f5-116">Number of bytes in each sector for the physical disk drive.</span></span>

</dd> <dt>

<span data-ttu-id="a81f5-117">**Numerodisco**</span><span class="sxs-lookup"><span data-stu-id="a81f5-117">**DiskNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a81f5-118">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a81f5-118">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a81f5-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a81f5-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a81f5-120">Qualificatori: **WmiDataId** (3)</span><span class="sxs-lookup"><span data-stu-id="a81f5-120">Qualifiers: **WmiDataId** (3)</span></span>
</dt> </dl>

<span data-ttu-id="a81f5-121">Numero di indice del disco contenente questa partizione.</span><span class="sxs-lookup"><span data-stu-id="a81f5-121">Index number of the disk containing this partition.</span></span>

</dd> <dt>

<span data-ttu-id="a81f5-122">**DriveLetterString**</span><span class="sxs-lookup"><span data-stu-id="a81f5-122">**DriveLetterString**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a81f5-123">Tipo di dati: matrice **Char16**</span><span class="sxs-lookup"><span data-stu-id="a81f5-123">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="a81f5-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a81f5-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a81f5-125">Qualificatori: **WmiDataId** (6), **Max** (4)</span><span class="sxs-lookup"><span data-stu-id="a81f5-125">Qualifiers: **WmiDataId** (6), **Max** (4)</span></span>
</dt> </dl>

<span data-ttu-id="a81f5-126">Lettera di unità del disco nel formato " <letter> :".</span><span class="sxs-lookup"><span data-stu-id="a81f5-126">Drive letter of the disk in the form, "<letter>:".</span></span>

</dd> <dt>

<span data-ttu-id="a81f5-127">**DriveType**</span><span class="sxs-lookup"><span data-stu-id="a81f5-127">**DriveType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a81f5-128">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a81f5-128">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a81f5-129">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a81f5-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a81f5-130">Qualificatori: **WmiDataId** (5)</span><span class="sxs-lookup"><span data-stu-id="a81f5-130">Qualifiers: **WmiDataId** (5)</span></span>
</dt> </dl>

<span data-ttu-id="a81f5-131">Tipo di unità disco.</span><span class="sxs-lookup"><span data-stu-id="a81f5-131">Type of disk drive.</span></span> <span data-ttu-id="a81f5-132">I valori possibili sono:</span><span class="sxs-lookup"><span data-stu-id="a81f5-132">Possible values are:</span></span>



| <span data-ttu-id="a81f5-133">Valore</span><span class="sxs-lookup"><span data-stu-id="a81f5-133">Value</span></span>                                                                        | <span data-ttu-id="a81f5-134">Significato</span><span class="sxs-lookup"><span data-stu-id="a81f5-134">Meaning</span></span>                                         |
|------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="a81f5-135"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="a81f5-135"><dt>1</dt></span></span> </dl> | <span data-ttu-id="a81f5-136">Partition</span><span class="sxs-lookup"><span data-stu-id="a81f5-136">Partition</span></span><br/>                            |
| <dl> <span data-ttu-id="a81f5-137"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="a81f5-137"><dt>2</dt></span></span> </dl> | <span data-ttu-id="a81f5-138">Volume</span><span class="sxs-lookup"><span data-stu-id="a81f5-138">Volume</span></span><br/>                               |
| <dl> <span data-ttu-id="a81f5-139"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="a81f5-139"><dt>3</dt></span></span> </dl> | <span data-ttu-id="a81f5-140">Partizione estesa su più dischi</span><span class="sxs-lookup"><span data-stu-id="a81f5-140">Extended partition on multiple disks</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="a81f5-141">**FileSystem**</span><span class="sxs-lookup"><span data-stu-id="a81f5-141">**FileSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a81f5-142">Tipo di dati: **Char16**</span><span class="sxs-lookup"><span data-stu-id="a81f5-142">Data type: **char16**</span></span>
</dt> <dt>

<span data-ttu-id="a81f5-143">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a81f5-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a81f5-144">Qualificatori: **WmiDataId** (13), **Max** (16)</span><span class="sxs-lookup"><span data-stu-id="a81f5-144">Qualifiers: **WmiDataId** (13), **Max** (16)</span></span>
</dt> </dl>

<span data-ttu-id="a81f5-145">File System sul disco logico, ad esempio NTFS.</span><span class="sxs-lookup"><span data-stu-id="a81f5-145">File system on the logical disk, for example, NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="a81f5-146">**NumberOfFreeClusters**</span><span class="sxs-lookup"><span data-stu-id="a81f5-146">**NumberOfFreeClusters**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a81f5-147">Tipo di dati: **sint64**</span><span class="sxs-lookup"><span data-stu-id="a81f5-147">Data type: **sint64**</span></span>
</dt> <dt>

<span data-ttu-id="a81f5-148">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a81f5-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a81f5-149">Qualificatori: **WmiDataId** (11)</span><span class="sxs-lookup"><span data-stu-id="a81f5-149">Qualifiers: **WmiDataId** (11)</span></span>
</dt> </dl>

<span data-ttu-id="a81f5-150">Numero di cluster liberi nel volume specificato.</span><span class="sxs-lookup"><span data-stu-id="a81f5-150">Number of free clusters in the specified volume.</span></span>

</dd> <dt>

<span data-ttu-id="a81f5-151">**Pad**</span><span class="sxs-lookup"><span data-stu-id="a81f5-151">**Pad**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a81f5-152">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a81f5-152">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a81f5-153">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a81f5-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a81f5-154">Qualificatori: **WmiDataId** (7)</span><span class="sxs-lookup"><span data-stu-id="a81f5-154">Qualifiers: **WmiDataId** (7)</span></span>
</dt> </dl>

<span data-ttu-id="a81f5-155">Riservato.</span><span class="sxs-lookup"><span data-stu-id="a81f5-155">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="a81f5-156">**PartitionNumber**</span><span class="sxs-lookup"><span data-stu-id="a81f5-156">**PartitionNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a81f5-157">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a81f5-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a81f5-158">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a81f5-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a81f5-159">Qualificatori: **WmiDataId** (8)</span><span class="sxs-lookup"><span data-stu-id="a81f5-159">Qualifiers: **WmiDataId** (8)</span></span>
</dt> </dl>

<span data-ttu-id="a81f5-160">Numero di indice della partizione.</span><span class="sxs-lookup"><span data-stu-id="a81f5-160">Index number of the partition.</span></span>

</dd> <dt>

<span data-ttu-id="a81f5-161">**PartitionSize**</span><span class="sxs-lookup"><span data-stu-id="a81f5-161">**PartitionSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a81f5-162">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a81f5-162">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a81f5-163">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a81f5-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a81f5-164">Qualificatori: **WmiDataId** (2)</span><span class="sxs-lookup"><span data-stu-id="a81f5-164">Qualifiers: **WmiDataId** (2)</span></span>
</dt> </dl>

<span data-ttu-id="a81f5-165">Dimensioni totali, in byte, della partizione.</span><span class="sxs-lookup"><span data-stu-id="a81f5-165">Total size of the partition, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="a81f5-166">**SectorsPerCluster**</span><span class="sxs-lookup"><span data-stu-id="a81f5-166">**SectorsPerCluster**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a81f5-167">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a81f5-167">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a81f5-168">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a81f5-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a81f5-169">Qualificatori: **WmiDataId** (9)</span><span class="sxs-lookup"><span data-stu-id="a81f5-169">Qualifiers: **WmiDataId** (9)</span></span>
</dt> </dl>

<span data-ttu-id="a81f5-170">Numero di settori nel volume.</span><span class="sxs-lookup"><span data-stu-id="a81f5-170">Number of sectors in the volume.</span></span>

</dd> <dt>

<span data-ttu-id="a81f5-171">**Dimensioni**</span><span class="sxs-lookup"><span data-stu-id="a81f5-171">**Size**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a81f5-172">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a81f5-172">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a81f5-173">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a81f5-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a81f5-174">Qualificatori: **WmiDataId** (4)</span><span class="sxs-lookup"><span data-stu-id="a81f5-174">Qualifiers: **WmiDataId** (4)</span></span>
</dt> </dl>

<span data-ttu-id="a81f5-175">Dimensioni, in byte, dell'unità disco.</span><span class="sxs-lookup"><span data-stu-id="a81f5-175">Size of the disk drive, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="a81f5-176">**StartOffset**</span><span class="sxs-lookup"><span data-stu-id="a81f5-176">**StartOffset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a81f5-177">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a81f5-177">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a81f5-178">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a81f5-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a81f5-179">Qualificatori: **WmiDataId** (1)</span><span class="sxs-lookup"><span data-stu-id="a81f5-179">Qualifiers: **WmiDataId** (1)</span></span>
</dt> </dl>

<span data-ttu-id="a81f5-180">Offset iniziale (in byte) della partizione dall'inizio del disco.</span><span class="sxs-lookup"><span data-stu-id="a81f5-180">Starting offset (in bytes) of the partition from the beginning of the disk.</span></span>

</dd> <dt>

<span data-ttu-id="a81f5-181">**TotalNumberOfClusters**</span><span class="sxs-lookup"><span data-stu-id="a81f5-181">**TotalNumberOfClusters**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a81f5-182">Tipo di dati: **sint64**</span><span class="sxs-lookup"><span data-stu-id="a81f5-182">Data type: **sint64**</span></span>
</dt> <dt>

<span data-ttu-id="a81f5-183">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a81f5-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a81f5-184">Qualificatori: **WmiDataId** (12)</span><span class="sxs-lookup"><span data-stu-id="a81f5-184">Qualifiers: **WmiDataId** (12)</span></span>
</dt> </dl>

<span data-ttu-id="a81f5-185">Numero di cluster usati e disponibili nel volume.</span><span class="sxs-lookup"><span data-stu-id="a81f5-185">Number of used and free clusters in the volume.</span></span>

</dd> <dt>

<span data-ttu-id="a81f5-186">**VolumeExt**</span><span class="sxs-lookup"><span data-stu-id="a81f5-186">**VolumeExt**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a81f5-187">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a81f5-187">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a81f5-188">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a81f5-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a81f5-189">Qualificatori: **WmiDataId** (14)</span><span class="sxs-lookup"><span data-stu-id="a81f5-189">Qualifiers: **WmiDataId** (14)</span></span>
</dt> </dl>

<span data-ttu-id="a81f5-190">Riservato.</span><span class="sxs-lookup"><span data-stu-id="a81f5-190">Reserved.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a81f5-191">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a81f5-191">Requirements</span></span>



| <span data-ttu-id="a81f5-192">Requisito</span><span class="sxs-lookup"><span data-stu-id="a81f5-192">Requirement</span></span> | <span data-ttu-id="a81f5-193">Valore</span><span class="sxs-lookup"><span data-stu-id="a81f5-193">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a81f5-194">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a81f5-194">Minimum supported client</span></span><br/> | <span data-ttu-id="a81f5-195">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="a81f5-195">None supported</span></span><br/>                            |
| <span data-ttu-id="a81f5-196">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a81f5-196">Minimum supported server</span></span><br/> | <span data-ttu-id="a81f5-197">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a81f5-197">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a81f5-198">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a81f5-198">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a81f5-199">**SystemConfig \_ V0**</span><span class="sxs-lookup"><span data-stu-id="a81f5-199">**SystemConfig\_V0**</span></span>](systemconfig-v0.md)
</dt> </dl>

 

 




