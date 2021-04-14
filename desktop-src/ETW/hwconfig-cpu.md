---
description: La \_ classe CPU HWConfig è la classe del tipo di evento per gli eventi di configurazione della CPU. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: a94714c6-009c-4300-a0a0-b7b3ce94f91e
title: Classe HWConfig_CPU
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HWConfig_CPU
- HWConfig_CPU.MHz
- HWConfig_CPU.NumberOfProcessors
- HWConfig_CPU.MemSize
- HWConfig_CPU.PageSize
- HWConfig_CPU.AllocationGranularity
- HWConfig_CPU.ComputerName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 493952e25080d4a64e018477ca1b45033c8747af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978274"
---
# <a name="hwconfig_cpu-class"></a><span data-ttu-id="b059f-104">\_Classe CPU HWConfig</span><span class="sxs-lookup"><span data-stu-id="b059f-104">HWConfig\_CPU class</span></span>

<span data-ttu-id="b059f-105">La **classe \_ CPU HWConfig** è la classe del tipo di evento per gli eventi di configurazione della CPU.</span><span class="sxs-lookup"><span data-stu-id="b059f-105">The **HWConfig\_CPU** class is the event type class for CPU configuration events.</span></span>

<span data-ttu-id="b059f-106">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="b059f-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="b059f-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b059f-107">Syntax</span></span>

``` syntax
[EventType(10), EventTypeName("CPU")]
class HWConfig_CPU : HWConfig
{
  uint32 MHz;
  uint32 NumberOfProcessors;
  uint32 MemSize;
  uint32 PageSize;
  uint32 AllocationGranularity;
  string ComputerName;
};
```

## <a name="members"></a><span data-ttu-id="b059f-108">Members</span><span class="sxs-lookup"><span data-stu-id="b059f-108">Members</span></span>

<span data-ttu-id="b059f-109">La **classe \_ CPU HWConfig** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="b059f-109">The **HWConfig\_CPU** class has these types of members:</span></span>

-   [<span data-ttu-id="b059f-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b059f-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b059f-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b059f-111">Properties</span></span>

<span data-ttu-id="b059f-112">La **classe \_ CPU HWConfig** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="b059f-112">The **HWConfig\_CPU** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b059f-113">AllocationGranularity</span><span class="sxs-lookup"><span data-stu-id="b059f-113">AllocationGranularity</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b059f-114">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b059f-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b059f-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b059f-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b059f-116">Qualificatori: WmiDataId (5)</span><span class="sxs-lookup"><span data-stu-id="b059f-116">Qualifiers: WmiDataId(5)</span></span>
</dt> </dl>

<span data-ttu-id="b059f-117">Granularità con cui viene allocata la memoria virtuale.</span><span class="sxs-lookup"><span data-stu-id="b059f-117">Granularity with which virtual memory is allocated.</span></span>

</dd> <dt>

<span data-ttu-id="b059f-118">NomeComputer</span><span class="sxs-lookup"><span data-stu-id="b059f-118">ComputerName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b059f-119">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b059f-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b059f-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b059f-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b059f-121">Qualificatori: WmiDataId (6), StringTermination ("NullTerminated"), Format ("w")</span><span class="sxs-lookup"><span data-stu-id="b059f-121">Qualifiers: WmiDataId(6), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="b059f-122">Nome del computer.</span><span class="sxs-lookup"><span data-stu-id="b059f-122">Name of the computer.</span></span>

</dd> <dt>

<span data-ttu-id="b059f-123">MemSize</span><span class="sxs-lookup"><span data-stu-id="b059f-123">MemSize</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b059f-124">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b059f-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b059f-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b059f-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b059f-126">Qualificatori: WmiDataId (3)</span><span class="sxs-lookup"><span data-stu-id="b059f-126">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="b059f-127">Quantità totale di memoria fisica disponibile per il sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="b059f-127">Total amount of physical memory available to the operating system.</span></span>

</dd> <dt>

<span data-ttu-id="b059f-128">MHz</span><span class="sxs-lookup"><span data-stu-id="b059f-128">MHz</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b059f-129">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b059f-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b059f-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b059f-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b059f-131">Qualificatori: WmiDataId (1)</span><span class="sxs-lookup"><span data-stu-id="b059f-131">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="b059f-132">Velocità massima del processore, in megahertz.</span><span class="sxs-lookup"><span data-stu-id="b059f-132">Maximum speed of the processor, in megahertz.</span></span>

</dd> <dt>

<span data-ttu-id="b059f-133">NumberOfProcessors</span><span class="sxs-lookup"><span data-stu-id="b059f-133">NumberOfProcessors</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b059f-134">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b059f-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b059f-135">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b059f-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b059f-136">Qualificatori: WmiDataId (2)</span><span class="sxs-lookup"><span data-stu-id="b059f-136">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="b059f-137">Numero di processori nel computer.</span><span class="sxs-lookup"><span data-stu-id="b059f-137">Number of processors on the computer.</span></span>

</dd> <dt>

<span data-ttu-id="b059f-138">PageSize</span><span class="sxs-lookup"><span data-stu-id="b059f-138">PageSize</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b059f-139">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b059f-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b059f-140">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b059f-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b059f-141">Qualificatori: WmiDataId (4)</span><span class="sxs-lookup"><span data-stu-id="b059f-141">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="b059f-142">Dimensioni di una pagina di scambio, in byte.</span><span class="sxs-lookup"><span data-stu-id="b059f-142">Size of a swap page, in bytes.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b059f-143">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b059f-143">Requirements</span></span>



| <span data-ttu-id="b059f-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="b059f-144">Requirement</span></span> | <span data-ttu-id="b059f-145">Valore</span><span class="sxs-lookup"><span data-stu-id="b059f-145">Value</span></span> |
|-------------------------------------|---------------------------------------------|
| <span data-ttu-id="b059f-146">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b059f-146">Minimum supported client</span></span><br/> | <span data-ttu-id="b059f-147">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="b059f-147">Windows XP \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="b059f-148">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b059f-148">Minimum supported server</span></span><br/> | <span data-ttu-id="b059f-149">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="b059f-149">None supported</span></span><br/>                   |



## <a name="see-also"></a><span data-ttu-id="b059f-150">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b059f-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b059f-151">**HWConfig**</span><span class="sxs-lookup"><span data-stu-id="b059f-151">**HWConfig**</span></span>](hwconfig.md)
</dt> </dl>

 

 




