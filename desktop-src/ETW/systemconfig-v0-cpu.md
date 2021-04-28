---
description: 'SystemConfig_V0_CPU: questa classe è la classe del tipo di evento per gli eventi di configurazione della CPU.'
ms.assetid: 9ca77676-ff0e-4c47-ae4e-f8192376d3ca
title: SystemConfig_V0_CPU classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_V0_CPU
- SystemConfig_V0_CPU.MHz
- SystemConfig_V0_CPU.NumberOfProcessors
- SystemConfig_V0_CPU.MemSize
- SystemConfig_V0_CPU.PageSize
- SystemConfig_V0_CPU.AllocationGranularity
- SystemConfig_V0_CPU.ComputerName
- SystemConfig_V0_CPU.DomainName
api_type:
- NA
api_location: ''
ms.openlocfilehash: de3b63def40cb6ead40f6f4c95625603cfc581ee
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105989"
---
# <a name="systemconfig_v0_cpu-class"></a><span data-ttu-id="5ea7f-103">Classe CPU SystemConfig \_ V0 \_</span><span class="sxs-lookup"><span data-stu-id="5ea7f-103">SystemConfig\_V0\_CPU class</span></span>

<span data-ttu-id="5ea7f-104">Questa classe è la classe del tipo di evento per gli eventi di configurazione della CPU.</span><span class="sxs-lookup"><span data-stu-id="5ea7f-104">This class is the event type class for CPU configuration events.</span></span>

<span data-ttu-id="5ea7f-105">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="5ea7f-105">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ea7f-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5ea7f-106">Syntax</span></span>

``` syntax
[EventType(10), EventTypeName("CPU")]
class SystemConfig_V0_CPU : SystemConfig_V0
{
  uint32 MHz;
  uint32 NumberOfProcessors;
  uint32 MemSize;
  uint32 PageSize;
  uint32 AllocationGranularity;
  char16 ComputerName[];
  char16 DomainName[];
};
```

## <a name="members"></a><span data-ttu-id="5ea7f-107">Members</span><span class="sxs-lookup"><span data-stu-id="5ea7f-107">Members</span></span>

<span data-ttu-id="5ea7f-108">La **classe CPU SystemConfig \_ V0 \_** include questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="5ea7f-108">The **SystemConfig\_V0\_CPU** class has these types of members:</span></span>

-   [<span data-ttu-id="5ea7f-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5ea7f-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5ea7f-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5ea7f-110">Properties</span></span>

<span data-ttu-id="5ea7f-111">La **classe CPU SystemConfig \_ V0 \_** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="5ea7f-111">The **SystemConfig\_V0\_CPU** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5ea7f-112">**AllocationGranularity**</span><span class="sxs-lookup"><span data-stu-id="5ea7f-112">**AllocationGranularity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ea7f-113">Tipo di dati: **uint32**</span><span class="sxs-lookup"><span data-stu-id="5ea7f-113">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5ea7f-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5ea7f-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ea7f-115">Qualificatori: **WmiDataId** (5)</span><span class="sxs-lookup"><span data-stu-id="5ea7f-115">Qualifiers: **WmiDataId** (5)</span></span>
</dt> </dl>

<span data-ttu-id="5ea7f-116">Granularità con cui viene allocata la memoria virtuale.</span><span class="sxs-lookup"><span data-stu-id="5ea7f-116">Granularity with which virtual memory is allocated.</span></span>

</dd> <dt>

<span data-ttu-id="5ea7f-117">**NomeComputer**</span><span class="sxs-lookup"><span data-stu-id="5ea7f-117">**ComputerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ea7f-118">Tipo di dati: **matrice char16**</span><span class="sxs-lookup"><span data-stu-id="5ea7f-118">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="5ea7f-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5ea7f-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ea7f-120">Qualificatori: **WmiDataId** (6), **Max** (256)</span><span class="sxs-lookup"><span data-stu-id="5ea7f-120">Qualifiers: **WmiDataId** (6), **Max** (256)</span></span>
</dt> </dl>

<span data-ttu-id="5ea7f-121">Nome del computer.</span><span class="sxs-lookup"><span data-stu-id="5ea7f-121">Name of the computer.</span></span>

</dd> <dt>

<span data-ttu-id="5ea7f-122">**Domainname**</span><span class="sxs-lookup"><span data-stu-id="5ea7f-122">**DomainName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ea7f-123">Tipo di dati: **matrice char16**</span><span class="sxs-lookup"><span data-stu-id="5ea7f-123">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="5ea7f-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5ea7f-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ea7f-125">Qualificatori: **WmiDataId** (7), **Max** (132)</span><span class="sxs-lookup"><span data-stu-id="5ea7f-125">Qualifiers: **WmiDataId** (7), **Max** (132)</span></span>
</dt> </dl>

<span data-ttu-id="5ea7f-126">Nome del dominio di cui il computer è membro.</span><span class="sxs-lookup"><span data-stu-id="5ea7f-126">Name of the domain in which the computer is a member.</span></span>

</dd> <dt>

<span data-ttu-id="5ea7f-127">**MemSize**</span><span class="sxs-lookup"><span data-stu-id="5ea7f-127">**MemSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ea7f-128">Tipo di dati: **uint32**</span><span class="sxs-lookup"><span data-stu-id="5ea7f-128">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5ea7f-129">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5ea7f-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ea7f-130">Qualificatori: **WmiDataId** (3)</span><span class="sxs-lookup"><span data-stu-id="5ea7f-130">Qualifiers: **WmiDataId** (3)</span></span>
</dt> </dl>

<span data-ttu-id="5ea7f-131">Quantità totale di memoria fisica disponibile per il sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="5ea7f-131">Total amount of physical memory available to the operating system.</span></span>

</dd> <dt>

<span data-ttu-id="5ea7f-132">**Mhz**</span><span class="sxs-lookup"><span data-stu-id="5ea7f-132">**MHz**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ea7f-133">Tipo di dati: **uint32**</span><span class="sxs-lookup"><span data-stu-id="5ea7f-133">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5ea7f-134">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5ea7f-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ea7f-135">Qualificatori: **WmiDataId** (1)</span><span class="sxs-lookup"><span data-stu-id="5ea7f-135">Qualifiers: **WmiDataId** (1)</span></span>
</dt> </dl>

<span data-ttu-id="5ea7f-136">Velocità massima del processore, in megahertz.</span><span class="sxs-lookup"><span data-stu-id="5ea7f-136">Maximum speed of the processor, in megahertz.</span></span>

</dd> <dt>

<span data-ttu-id="5ea7f-137">**NumberOfProcessors**</span><span class="sxs-lookup"><span data-stu-id="5ea7f-137">**NumberOfProcessors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ea7f-138">Tipo di dati: **uint32**</span><span class="sxs-lookup"><span data-stu-id="5ea7f-138">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5ea7f-139">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5ea7f-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ea7f-140">Qualificatori: **WmiDataId** (2)</span><span class="sxs-lookup"><span data-stu-id="5ea7f-140">Qualifiers: **WmiDataId** (2)</span></span>
</dt> </dl>

<span data-ttu-id="5ea7f-141">Numero di processori nel computer.</span><span class="sxs-lookup"><span data-stu-id="5ea7f-141">Number of processors on the computer.</span></span>

</dd> <dt>

<span data-ttu-id="5ea7f-142">**PageSize**</span><span class="sxs-lookup"><span data-stu-id="5ea7f-142">**PageSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ea7f-143">Tipo di dati: **uint32**</span><span class="sxs-lookup"><span data-stu-id="5ea7f-143">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5ea7f-144">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5ea7f-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ea7f-145">Qualificatori: **WmiDataId** (4)</span><span class="sxs-lookup"><span data-stu-id="5ea7f-145">Qualifiers: **WmiDataId** (4)</span></span>
</dt> </dl>

<span data-ttu-id="5ea7f-146">Dimensioni di una pagina di scambio, in byte.</span><span class="sxs-lookup"><span data-stu-id="5ea7f-146">Size of a swap page, in bytes.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5ea7f-147">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5ea7f-147">Requirements</span></span>



| <span data-ttu-id="5ea7f-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="5ea7f-148">Requirement</span></span> | <span data-ttu-id="5ea7f-149">Valore</span><span class="sxs-lookup"><span data-stu-id="5ea7f-149">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5ea7f-150">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5ea7f-150">Minimum supported client</span></span><br/> | <span data-ttu-id="5ea7f-151">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="5ea7f-151">None supported</span></span><br/>                            |
| <span data-ttu-id="5ea7f-152">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5ea7f-152">Minimum supported server</span></span><br/> | <span data-ttu-id="5ea7f-153">Solo app desktop di Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="5ea7f-153">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5ea7f-154">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5ea7f-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ea7f-155">**SystemConfig \_ V0**</span><span class="sxs-lookup"><span data-stu-id="5ea7f-155">**SystemConfig\_V0**</span></span>](systemconfig-v0.md)
</dt> </dl>

 

 




