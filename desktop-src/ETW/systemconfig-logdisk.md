---
description: Questa classe è la classe del tipo di evento per gli eventi di configurazione del disco logico.
ms.assetid: a11a8245-8ace-4061-b6c7-938002d8b9fc
title: Classe SystemConfig_LogDisk
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
ms.openlocfilehash: d3bff1cf526dfb7bf1ddd36fcb887e8a4b837be4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977586"
---
# <a name="systemconfig_logdisk-class"></a><span data-ttu-id="c47f6-103">\_Classe SystemConfig LogDisk</span><span class="sxs-lookup"><span data-stu-id="c47f6-103">SystemConfig\_LogDisk class</span></span>

<span data-ttu-id="c47f6-104">Questa classe è la classe del tipo di evento per gli eventi di configurazione del disco logico.</span><span class="sxs-lookup"><span data-stu-id="c47f6-104">This class is the event type class for logical disk configuration events.</span></span>

<span data-ttu-id="c47f6-105">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="c47f6-105">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="c47f6-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c47f6-106">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="c47f6-107">Members</span><span class="sxs-lookup"><span data-stu-id="c47f6-107">Members</span></span>

<span data-ttu-id="c47f6-108">La **classe \_ LogDisk di SystemConfig** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="c47f6-108">The **SystemConfig\_LogDisk** class has these types of members:</span></span>

-   [<span data-ttu-id="c47f6-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c47f6-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c47f6-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c47f6-110">Properties</span></span>

<span data-ttu-id="c47f6-111">La **classe \_ LogDisk di SystemConfig** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="c47f6-111">The **SystemConfig\_LogDisk** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c47f6-112">**BytesPerSector**</span><span class="sxs-lookup"><span data-stu-id="c47f6-112">**BytesPerSector**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c47f6-113">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c47f6-113">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c47f6-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c47f6-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c47f6-115">Qualificatori: **WmiDataId** (10)</span><span class="sxs-lookup"><span data-stu-id="c47f6-115">Qualifiers: **WmiDataId** (10)</span></span>
</dt> </dl>

<span data-ttu-id="c47f6-116">Numero di byte in ogni settore per l'unità disco fisica.</span><span class="sxs-lookup"><span data-stu-id="c47f6-116">Number of bytes in each sector for the physical disk drive.</span></span>

</dd> <dt>

<span data-ttu-id="c47f6-117">**Numerodisco**</span><span class="sxs-lookup"><span data-stu-id="c47f6-117">**DiskNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c47f6-118">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c47f6-118">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c47f6-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c47f6-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c47f6-120">Qualificatori: **WmiDataId** (3)</span><span class="sxs-lookup"><span data-stu-id="c47f6-120">Qualifiers: **WmiDataId** (3)</span></span>
</dt> </dl>

<span data-ttu-id="c47f6-121">Numero di indice del disco contenente questa partizione.</span><span class="sxs-lookup"><span data-stu-id="c47f6-121">Index number of the disk containing this partition.</span></span>

</dd> <dt>

<span data-ttu-id="c47f6-122">**DriveLetterString**</span><span class="sxs-lookup"><span data-stu-id="c47f6-122">**DriveLetterString**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c47f6-123">Tipo di dati: matrice **Char16**</span><span class="sxs-lookup"><span data-stu-id="c47f6-123">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="c47f6-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c47f6-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c47f6-125">Qualificatori: **WmiDataId** (6), **Max** (4), **Format ("s")**</span><span class="sxs-lookup"><span data-stu-id="c47f6-125">Qualifiers: **WmiDataId** (6), **Max** (4), **Format("s")**</span></span>
</dt> </dl>

<span data-ttu-id="c47f6-126">Lettera di unità del disco nel formato " <letter> :".</span><span class="sxs-lookup"><span data-stu-id="c47f6-126">Drive letter of the disk in the form, "<letter>:".</span></span>

</dd> <dt>

<span data-ttu-id="c47f6-127">**DriveType**</span><span class="sxs-lookup"><span data-stu-id="c47f6-127">**DriveType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c47f6-128">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c47f6-128">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c47f6-129">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c47f6-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c47f6-130">Qualificatori: **WmiDataId** (5)</span><span class="sxs-lookup"><span data-stu-id="c47f6-130">Qualifiers: **WmiDataId** (5)</span></span>
</dt> </dl>

<span data-ttu-id="c47f6-131">Tipo di unità disco.</span><span class="sxs-lookup"><span data-stu-id="c47f6-131">Type of disk drive.</span></span> <span data-ttu-id="c47f6-132">I valori possibili sono:</span><span class="sxs-lookup"><span data-stu-id="c47f6-132">Possible values are:</span></span>



| <span data-ttu-id="c47f6-133">Valore</span><span class="sxs-lookup"><span data-stu-id="c47f6-133">Value</span></span>                                                                        | <span data-ttu-id="c47f6-134">Significato</span><span class="sxs-lookup"><span data-stu-id="c47f6-134">Meaning</span></span>                                         |
|------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="c47f6-135"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="c47f6-135"><dt>1</dt></span></span> </dl> | <span data-ttu-id="c47f6-136">Partition</span><span class="sxs-lookup"><span data-stu-id="c47f6-136">Partition</span></span><br/>                            |
| <dl> <span data-ttu-id="c47f6-137"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="c47f6-137"><dt>2</dt></span></span> </dl> | <span data-ttu-id="c47f6-138">Volume</span><span class="sxs-lookup"><span data-stu-id="c47f6-138">Volume</span></span><br/>                               |
| <dl> <span data-ttu-id="c47f6-139"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="c47f6-139"><dt>3</dt></span></span> </dl> | <span data-ttu-id="c47f6-140">Partizione estesa su più dischi</span><span class="sxs-lookup"><span data-stu-id="c47f6-140">Extended partition on multiple disks</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="c47f6-141">**FileSystem**</span><span class="sxs-lookup"><span data-stu-id="c47f6-141">**FileSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c47f6-142">Tipo di dati: **Char16**</span><span class="sxs-lookup"><span data-stu-id="c47f6-142">Data type: **char16**</span></span>
</dt> <dt>

<span data-ttu-id="c47f6-143">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c47f6-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c47f6-144">Qualificatori: **WmiDataId** (14), **Max** (16), **Format ("s")**</span><span class="sxs-lookup"><span data-stu-id="c47f6-144">Qualifiers: **WmiDataId** (14), **Max** (16), **Format("s")**</span></span>
</dt> </dl>

<span data-ttu-id="c47f6-145">File System sul disco logico, ad esempio NTFS.</span><span class="sxs-lookup"><span data-stu-id="c47f6-145">File system on the logical disk, for example, NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="c47f6-146">**NumberOfFreeClusters**</span><span class="sxs-lookup"><span data-stu-id="c47f6-146">**NumberOfFreeClusters**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c47f6-147">Tipo di dati: **sint64**</span><span class="sxs-lookup"><span data-stu-id="c47f6-147">Data type: **sint64**</span></span>
</dt> <dt>

<span data-ttu-id="c47f6-148">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c47f6-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c47f6-149">Qualificatori: **WmiDataId** (12)</span><span class="sxs-lookup"><span data-stu-id="c47f6-149">Qualifiers: **WmiDataId** (12)</span></span>
</dt> </dl>

<span data-ttu-id="c47f6-150">Numero di cluster liberi nel volume specificato.</span><span class="sxs-lookup"><span data-stu-id="c47f6-150">Number of free clusters in the specified volume.</span></span>

</dd> <dt>

<span data-ttu-id="c47f6-151">**Pad1**</span><span class="sxs-lookup"><span data-stu-id="c47f6-151">**Pad1**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c47f6-152">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c47f6-152">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c47f6-153">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c47f6-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c47f6-154">Qualificatori: **WmiDataId** (7)</span><span class="sxs-lookup"><span data-stu-id="c47f6-154">Qualifiers: **WmiDataId** (7)</span></span>
</dt> </dl>

<span data-ttu-id="c47f6-155">Non usato.</span><span class="sxs-lookup"><span data-stu-id="c47f6-155">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="c47f6-156">**Pad2**</span><span class="sxs-lookup"><span data-stu-id="c47f6-156">**Pad2**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c47f6-157">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c47f6-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c47f6-158">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c47f6-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c47f6-159">Qualificatori: **WmiDataId** (11)</span><span class="sxs-lookup"><span data-stu-id="c47f6-159">Qualifiers: **WmiDataId** (11)</span></span>
</dt> </dl>

<span data-ttu-id="c47f6-160">Non usato.</span><span class="sxs-lookup"><span data-stu-id="c47f6-160">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="c47f6-161">**Pad3**</span><span class="sxs-lookup"><span data-stu-id="c47f6-161">**Pad3**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c47f6-162">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c47f6-162">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c47f6-163">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c47f6-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c47f6-164">Qualificatori: **WmiDataId** (16)</span><span class="sxs-lookup"><span data-stu-id="c47f6-164">Qualifiers: **WmiDataId** (16)</span></span>
</dt> </dl>

<span data-ttu-id="c47f6-165">Non usato.</span><span class="sxs-lookup"><span data-stu-id="c47f6-165">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="c47f6-166">**PartitionNumber**</span><span class="sxs-lookup"><span data-stu-id="c47f6-166">**PartitionNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c47f6-167">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c47f6-167">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c47f6-168">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c47f6-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c47f6-169">Qualificatori: **WmiDataId** (8)</span><span class="sxs-lookup"><span data-stu-id="c47f6-169">Qualifiers: **WmiDataId** (8)</span></span>
</dt> </dl>

<span data-ttu-id="c47f6-170">Numero di indice della partizione.</span><span class="sxs-lookup"><span data-stu-id="c47f6-170">Index number of the partition.</span></span>

</dd> <dt>

<span data-ttu-id="c47f6-171">**PartitionSize**</span><span class="sxs-lookup"><span data-stu-id="c47f6-171">**PartitionSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c47f6-172">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c47f6-172">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c47f6-173">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c47f6-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c47f6-174">Qualificatori: **WmiDataId** (2)</span><span class="sxs-lookup"><span data-stu-id="c47f6-174">Qualifiers: **WmiDataId** (2)</span></span>
</dt> </dl>

<span data-ttu-id="c47f6-175">Dimensioni totali, in byte, della partizione.</span><span class="sxs-lookup"><span data-stu-id="c47f6-175">Total size of the partition, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="c47f6-176">**SectorsPerCluster**</span><span class="sxs-lookup"><span data-stu-id="c47f6-176">**SectorsPerCluster**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c47f6-177">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c47f6-177">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c47f6-178">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c47f6-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c47f6-179">Qualificatori: **WmiDataId** (9)</span><span class="sxs-lookup"><span data-stu-id="c47f6-179">Qualifiers: **WmiDataId** (9)</span></span>
</dt> </dl>

<span data-ttu-id="c47f6-180">Numero di settori nel volume.</span><span class="sxs-lookup"><span data-stu-id="c47f6-180">Number of sectors in the volume.</span></span>

</dd> <dt>

<span data-ttu-id="c47f6-181">**Dimensioni**</span><span class="sxs-lookup"><span data-stu-id="c47f6-181">**Size**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c47f6-182">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c47f6-182">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c47f6-183">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c47f6-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c47f6-184">Qualificatori: **WmiDataId** (4)</span><span class="sxs-lookup"><span data-stu-id="c47f6-184">Qualifiers: **WmiDataId** (4)</span></span>
</dt> </dl>

<span data-ttu-id="c47f6-185">Dimensioni, in byte, dell'unità disco.</span><span class="sxs-lookup"><span data-stu-id="c47f6-185">Size of the disk drive, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="c47f6-186">**StartOffset**</span><span class="sxs-lookup"><span data-stu-id="c47f6-186">**StartOffset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c47f6-187">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c47f6-187">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c47f6-188">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c47f6-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c47f6-189">Qualificatori: **WmiDataId** (1)</span><span class="sxs-lookup"><span data-stu-id="c47f6-189">Qualifiers: **WmiDataId** (1)</span></span>
</dt> </dl>

<span data-ttu-id="c47f6-190">Offset iniziale (in byte) della partizione dall'inizio del disco.</span><span class="sxs-lookup"><span data-stu-id="c47f6-190">Starting offset (in bytes) of the partition from the beginning of the disk.</span></span>

</dd> <dt>

<span data-ttu-id="c47f6-191">**TotalNumberOfClusters**</span><span class="sxs-lookup"><span data-stu-id="c47f6-191">**TotalNumberOfClusters**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c47f6-192">Tipo di dati: **sint64**</span><span class="sxs-lookup"><span data-stu-id="c47f6-192">Data type: **sint64**</span></span>
</dt> <dt>

<span data-ttu-id="c47f6-193">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c47f6-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c47f6-194">Qualificatori: **WmiDataId** (13)</span><span class="sxs-lookup"><span data-stu-id="c47f6-194">Qualifiers: **WmiDataId** (13)</span></span>
</dt> </dl>

<span data-ttu-id="c47f6-195">Numero di cluster usati e disponibili nel volume.</span><span class="sxs-lookup"><span data-stu-id="c47f6-195">Number of used and free clusters in the volume.</span></span>

</dd> <dt>

<span data-ttu-id="c47f6-196">**VolumeExt**</span><span class="sxs-lookup"><span data-stu-id="c47f6-196">**VolumeExt**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c47f6-197">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c47f6-197">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c47f6-198">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c47f6-198">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c47f6-199">Qualificatori: **WmiDataId** (15)</span><span class="sxs-lookup"><span data-stu-id="c47f6-199">Qualifiers: **WmiDataId** (15)</span></span>
</dt> </dl>

<span data-ttu-id="c47f6-200">Riservato.</span><span class="sxs-lookup"><span data-stu-id="c47f6-200">Reserved.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c47f6-201">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c47f6-201">Requirements</span></span>



| <span data-ttu-id="c47f6-202">Requisito</span><span class="sxs-lookup"><span data-stu-id="c47f6-202">Requirement</span></span> | <span data-ttu-id="c47f6-203">Valore</span><span class="sxs-lookup"><span data-stu-id="c47f6-203">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c47f6-204">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c47f6-204">Minimum supported client</span></span><br/> | <span data-ttu-id="c47f6-205">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c47f6-205">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="c47f6-206">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c47f6-206">Minimum supported server</span></span><br/> | <span data-ttu-id="c47f6-207">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c47f6-207">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c47f6-208">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c47f6-208">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c47f6-209">**SystemConfig**</span><span class="sxs-lookup"><span data-stu-id="c47f6-209">**SystemConfig**</span></span>](systemconfig.md)
</dt> </dl>

 

 




