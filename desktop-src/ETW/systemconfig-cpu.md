---
description: Questa classe è la classe del tipo di evento per gli eventi di configurazione della CPU.
ms.assetid: 5a24be04-9e5e-4ba9-baaf-b58b79ad947b
title: Classe SystemConfig_CPU
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_CPU
- SystemConfig_CPU.MHz
- SystemConfig_CPU.NumberOfProcessors
- SystemConfig_CPU.MemSize
- SystemConfig_CPU.PageSize
- SystemConfig_CPU.AllocationGranularity
- SystemConfig_CPU.ComputerName
- SystemConfig_CPU.DomainName
- SystemConfig_CPU.HyperThreadingFlag
api_type:
- NA
api_location: ''
ms.openlocfilehash: d08d0eeac9aa2287576bbb6dfe0e8ce41f116e8b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980071"
---
# <a name="systemconfig_cpu-class"></a><span data-ttu-id="5e86b-103">\_Classe CPU SystemConfig</span><span class="sxs-lookup"><span data-stu-id="5e86b-103">SystemConfig\_CPU class</span></span>

<span data-ttu-id="5e86b-104">Questa classe è la classe del tipo di evento per gli eventi di configurazione della CPU.</span><span class="sxs-lookup"><span data-stu-id="5e86b-104">This class is the event type class for CPU configuration events.</span></span>

<span data-ttu-id="5e86b-105">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="5e86b-105">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e86b-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5e86b-106">Syntax</span></span>

``` syntax
[EventType(10), EventTypeName("CPU")]
class SystemConfig_CPU : SystemConfig
{
  uint32 MHz;
  uint32 NumberOfProcessors;
  uint32 MemSize;
  uint32 PageSize;
  uint32 AllocationGranularity;
  char16 ComputerName[];
  char16 DomainName[];
  uint32 HyperThreadingFlag;
};
```

## <a name="members"></a><span data-ttu-id="5e86b-107">Members</span><span class="sxs-lookup"><span data-stu-id="5e86b-107">Members</span></span>

<span data-ttu-id="5e86b-108">La **classe \_ CPU SystemConfig** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="5e86b-108">The **SystemConfig\_CPU** class has these types of members:</span></span>

-   [<span data-ttu-id="5e86b-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5e86b-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5e86b-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5e86b-110">Properties</span></span>

<span data-ttu-id="5e86b-111">La **classe \_ CPU SystemConfig** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="5e86b-111">The **SystemConfig\_CPU** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5e86b-112">**AllocationGranularity**</span><span class="sxs-lookup"><span data-stu-id="5e86b-112">**AllocationGranularity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e86b-113">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5e86b-113">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5e86b-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5e86b-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5e86b-115">Qualificatori: **WmiDataId** (5)</span><span class="sxs-lookup"><span data-stu-id="5e86b-115">Qualifiers: **WmiDataId** (5)</span></span>
</dt> </dl>

<span data-ttu-id="5e86b-116">Granularità con cui viene allocata la memoria virtuale.</span><span class="sxs-lookup"><span data-stu-id="5e86b-116">Granularity with which virtual memory is allocated.</span></span>

</dd> <dt>

<span data-ttu-id="5e86b-117">**NomeComputer**</span><span class="sxs-lookup"><span data-stu-id="5e86b-117">**ComputerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e86b-118">Tipo di dati: matrice **Char16**</span><span class="sxs-lookup"><span data-stu-id="5e86b-118">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="5e86b-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5e86b-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5e86b-120">Qualificatori: **WmiDataId** (6), **Max** (256), **Format ("s")**</span><span class="sxs-lookup"><span data-stu-id="5e86b-120">Qualifiers: **WmiDataId** (6), **Max** (256), **Format("s")**</span></span>
</dt> </dl>

<span data-ttu-id="5e86b-121">Nome del computer.</span><span class="sxs-lookup"><span data-stu-id="5e86b-121">Name of the computer.</span></span>

</dd> <dt>

<span data-ttu-id="5e86b-122">**NomeDominio**</span><span class="sxs-lookup"><span data-stu-id="5e86b-122">**DomainName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e86b-123">Tipo di dati: matrice **Char16**</span><span class="sxs-lookup"><span data-stu-id="5e86b-123">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="5e86b-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5e86b-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5e86b-125">Qualificatori: **WmiDataId** (7), **Max** (132), **Format ("s")**</span><span class="sxs-lookup"><span data-stu-id="5e86b-125">Qualifiers: **WmiDataId** (7), **Max** (132), **Format("s")**</span></span>
</dt> </dl>

<span data-ttu-id="5e86b-126">Nome del dominio in cui il computer è membro.</span><span class="sxs-lookup"><span data-stu-id="5e86b-126">Name of the domain in which the computer is a member.</span></span>

</dd> <dt>

<span data-ttu-id="5e86b-127">**HyperThreadingFlag**</span><span class="sxs-lookup"><span data-stu-id="5e86b-127">**HyperThreadingFlag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e86b-128">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5e86b-128">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5e86b-129">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5e86b-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5e86b-130">Qualificatori: **WmiDataId** (8), puntatore</span><span class="sxs-lookup"><span data-stu-id="5e86b-130">Qualifiers: **WmiDataId** (8), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="5e86b-131">Indica se l'opzione Hyper-Threading è attiva o disattiva per un processore.</span><span class="sxs-lookup"><span data-stu-id="5e86b-131">Indicates if the hyper-threading option is on or off for a processor.</span></span> <span data-ttu-id="5e86b-132">Ogni bit riflette lo stato di Hyper-Threading di una CPU nel computer.</span><span class="sxs-lookup"><span data-stu-id="5e86b-132">Each bit reflects the hyper-threading state of a CPU on the computer.</span></span>

</dd> <dt>

<span data-ttu-id="5e86b-133">**MemSize**</span><span class="sxs-lookup"><span data-stu-id="5e86b-133">**MemSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e86b-134">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5e86b-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5e86b-135">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5e86b-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5e86b-136">Qualificatori: **WmiDataId** (3)</span><span class="sxs-lookup"><span data-stu-id="5e86b-136">Qualifiers: **WmiDataId** (3)</span></span>
</dt> </dl>

<span data-ttu-id="5e86b-137">Quantità totale di memoria fisica disponibile per il sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="5e86b-137">Total amount of physical memory available to the operating system.</span></span>

</dd> <dt>

<span data-ttu-id="5e86b-138">**MHz**</span><span class="sxs-lookup"><span data-stu-id="5e86b-138">**MHz**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e86b-139">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5e86b-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5e86b-140">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5e86b-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5e86b-141">Qualificatori: **WmiDataId** (1)</span><span class="sxs-lookup"><span data-stu-id="5e86b-141">Qualifiers: **WmiDataId** (1)</span></span>
</dt> </dl>

<span data-ttu-id="5e86b-142">Velocità massima del processore, in megahertz.</span><span class="sxs-lookup"><span data-stu-id="5e86b-142">Maximum speed of the processor, in megahertz.</span></span>

</dd> <dt>

<span data-ttu-id="5e86b-143">**NumberOfProcessors**</span><span class="sxs-lookup"><span data-stu-id="5e86b-143">**NumberOfProcessors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e86b-144">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5e86b-144">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5e86b-145">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5e86b-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5e86b-146">Qualificatori: **WmiDataId** (2)</span><span class="sxs-lookup"><span data-stu-id="5e86b-146">Qualifiers: **WmiDataId** (2)</span></span>
</dt> </dl>

<span data-ttu-id="5e86b-147">Numero di processori nel computer.</span><span class="sxs-lookup"><span data-stu-id="5e86b-147">Number of processors on the computer.</span></span>

</dd> <dt>

<span data-ttu-id="5e86b-148">**PageSize**</span><span class="sxs-lookup"><span data-stu-id="5e86b-148">**PageSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5e86b-149">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5e86b-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5e86b-150">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5e86b-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5e86b-151">Qualificatori: **WmiDataId** (4)</span><span class="sxs-lookup"><span data-stu-id="5e86b-151">Qualifiers: **WmiDataId** (4)</span></span>
</dt> </dl>

<span data-ttu-id="5e86b-152">Dimensioni di una pagina di scambio, in byte.</span><span class="sxs-lookup"><span data-stu-id="5e86b-152">Size of a swap page, in bytes.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5e86b-153">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5e86b-153">Requirements</span></span>



| <span data-ttu-id="5e86b-154">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e86b-154">Requirement</span></span> | <span data-ttu-id="5e86b-155">Valore</span><span class="sxs-lookup"><span data-stu-id="5e86b-155">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5e86b-156">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5e86b-156">Minimum supported client</span></span><br/> | <span data-ttu-id="5e86b-157">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5e86b-157">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="5e86b-158">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5e86b-158">Minimum supported server</span></span><br/> | <span data-ttu-id="5e86b-159">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5e86b-159">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5e86b-160">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5e86b-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e86b-161">**SystemConfig**</span><span class="sxs-lookup"><span data-stu-id="5e86b-161">**SystemConfig**</span></span>](systemconfig.md)
</dt> </dl>

 

 




