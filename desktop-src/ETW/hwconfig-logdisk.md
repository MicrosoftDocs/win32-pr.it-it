---
description: La \_ classe HWConfig LogDisk è la classe del tipo di evento per gli eventi di configurazione del disco logico. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: 2b7038fa-2f20-4bb5-bac1-76b272b3421c
title: Classe HWConfig_LogDisk
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HWConfig_LogDisk
- HWConfig_LogDisk.DiskNumber
- HWConfig_LogDisk.Pad
- HWConfig_LogDisk.StartOffset
- HWConfig_LogDisk.PartitionSize
api_type:
- NA
api_location: ''
ms.openlocfilehash: dce4faed913d01f76ff23177b2dad42ea74e5c08
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529886"
---
# <a name="hwconfig_logdisk-class"></a><span data-ttu-id="e1b6e-104">\_Classe HWConfig LogDisk</span><span class="sxs-lookup"><span data-stu-id="e1b6e-104">HWConfig\_LogDisk class</span></span>

<span data-ttu-id="e1b6e-105">La classe **HWConfig \_ LogDisk** è la classe del tipo di evento per gli eventi di configurazione del disco logico.</span><span class="sxs-lookup"><span data-stu-id="e1b6e-105">The **HWConfig\_LogDisk** class is the event type class for logical disk configuration events.</span></span>

<span data-ttu-id="e1b6e-106">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="e1b6e-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1b6e-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e1b6e-107">Syntax</span></span>

``` syntax
[EventType(12), EventTypeName("LogDisk")]
class HWConfig_LogDisk : HWConfig
{
  uint32 DiskNumber;
  uint32 Pad;
  uint64 StartOffset;
  uint64 PartitionSize;
};
```

## <a name="members"></a><span data-ttu-id="e1b6e-108">Members</span><span class="sxs-lookup"><span data-stu-id="e1b6e-108">Members</span></span>

<span data-ttu-id="e1b6e-109">La **classe \_ LogDisk di HWConfig** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="e1b6e-109">The **HWConfig\_LogDisk** class has these types of members:</span></span>

-   [<span data-ttu-id="e1b6e-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e1b6e-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e1b6e-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e1b6e-111">Properties</span></span>

<span data-ttu-id="e1b6e-112">La **classe \_ LogDisk di HWConfig** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="e1b6e-112">The **HWConfig\_LogDisk** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e1b6e-113">Numerodisco</span><span class="sxs-lookup"><span data-stu-id="e1b6e-113">DiskNumber</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1b6e-114">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e1b6e-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e1b6e-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e1b6e-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e1b6e-116">Qualificatori: WmiDataId (1)</span><span class="sxs-lookup"><span data-stu-id="e1b6e-116">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="e1b6e-117">Numero di indice del disco contenente questa partizione.</span><span class="sxs-lookup"><span data-stu-id="e1b6e-117">Index number of the disk containing this partition.</span></span>

</dd> <dt>

<span data-ttu-id="e1b6e-118">Pad</span><span class="sxs-lookup"><span data-stu-id="e1b6e-118">Pad</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1b6e-119">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e1b6e-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e1b6e-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e1b6e-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e1b6e-121">Qualificatori: WmiDataId (2)</span><span class="sxs-lookup"><span data-stu-id="e1b6e-121">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="e1b6e-122">Riservato.</span><span class="sxs-lookup"><span data-stu-id="e1b6e-122">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="e1b6e-123">PartitionSize</span><span class="sxs-lookup"><span data-stu-id="e1b6e-123">PartitionSize</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1b6e-124">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e1b6e-124">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e1b6e-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e1b6e-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e1b6e-126">Qualificatori: WmiDataId (4)</span><span class="sxs-lookup"><span data-stu-id="e1b6e-126">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="e1b6e-127">Dimensioni totali, in byte, della partizione.</span><span class="sxs-lookup"><span data-stu-id="e1b6e-127">Total size of the partition, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="e1b6e-128">StartOffset</span><span class="sxs-lookup"><span data-stu-id="e1b6e-128">StartOffset</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1b6e-129">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e1b6e-129">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e1b6e-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e1b6e-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e1b6e-131">Qualificatori: WmiDataId (3)</span><span class="sxs-lookup"><span data-stu-id="e1b6e-131">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="e1b6e-132">Offset iniziale (in byte) della partizione dall'inizio del disco.</span><span class="sxs-lookup"><span data-stu-id="e1b6e-132">Starting offset (in bytes) of the partition from the beginning of the disk.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e1b6e-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e1b6e-133">Requirements</span></span>



| <span data-ttu-id="e1b6e-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="e1b6e-134">Requirement</span></span> | <span data-ttu-id="e1b6e-135">Valore</span><span class="sxs-lookup"><span data-stu-id="e1b6e-135">Value</span></span> |
|-------------------------------------|---------------------------------------------|
| <span data-ttu-id="e1b6e-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e1b6e-136">Minimum supported client</span></span><br/> | <span data-ttu-id="e1b6e-137">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="e1b6e-137">Windows XP \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="e1b6e-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e1b6e-138">Minimum supported server</span></span><br/> | <span data-ttu-id="e1b6e-139">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="e1b6e-139">None supported</span></span><br/>                   |



## <a name="see-also"></a><span data-ttu-id="e1b6e-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e1b6e-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1b6e-141">**HWConfig**</span><span class="sxs-lookup"><span data-stu-id="e1b6e-141">**HWConfig**</span></span>](hwconfig.md)
</dt> </dl>

 

 




