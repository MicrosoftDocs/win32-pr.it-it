---
description: Questa classe è la classe del tipo di evento per gli eventi di configurazione della CPU.
ms.assetid: 9ca77676-ff0e-4c47-ae4e-f8192376d3ca
title: Classe SystemConfig_V0_CPU
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
ms.openlocfilehash: 6963201f76afa40e9b1741dc2936fa2ab4433a74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968328"
---
# <a name="systemconfig_v0_cpu-class"></a><span data-ttu-id="3ae98-103">\_Classe SystemConfig V0 \_ CPU</span><span class="sxs-lookup"><span data-stu-id="3ae98-103">SystemConfig\_V0\_CPU class</span></span>

<span data-ttu-id="3ae98-104">Questa classe è la classe del tipo di evento per gli eventi di configurazione della CPU.</span><span class="sxs-lookup"><span data-stu-id="3ae98-104">This class is the event type class for CPU configuration events.</span></span>

<span data-ttu-id="3ae98-105">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="3ae98-105">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ae98-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3ae98-106">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="3ae98-107">Members</span><span class="sxs-lookup"><span data-stu-id="3ae98-107">Members</span></span>

<span data-ttu-id="3ae98-108">La classe **SystemConfig \_ V0 \_ CPU** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="3ae98-108">The **SystemConfig\_V0\_CPU** class has these types of members:</span></span>

-   [<span data-ttu-id="3ae98-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="3ae98-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3ae98-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="3ae98-110">Properties</span></span>

<span data-ttu-id="3ae98-111">La classe **SystemConfig \_ V0 \_ CPU** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="3ae98-111">The **SystemConfig\_V0\_CPU** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3ae98-112">**AllocationGranularity**</span><span class="sxs-lookup"><span data-stu-id="3ae98-112">**AllocationGranularity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ae98-113">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3ae98-113">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3ae98-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3ae98-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ae98-115">Qualificatori: **WmiDataId** (5)</span><span class="sxs-lookup"><span data-stu-id="3ae98-115">Qualifiers: **WmiDataId** (5)</span></span>
</dt> </dl>

<span data-ttu-id="3ae98-116">Granularità con cui viene allocata la memoria virtuale.</span><span class="sxs-lookup"><span data-stu-id="3ae98-116">Granularity with which virtual memory is allocated.</span></span>

</dd> <dt>

<span data-ttu-id="3ae98-117">**NomeComputer**</span><span class="sxs-lookup"><span data-stu-id="3ae98-117">**ComputerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ae98-118">Tipo di dati: matrice **Char16**</span><span class="sxs-lookup"><span data-stu-id="3ae98-118">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="3ae98-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3ae98-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ae98-120">Qualificatori: **WmiDataId** (6), **Max** (256)</span><span class="sxs-lookup"><span data-stu-id="3ae98-120">Qualifiers: **WmiDataId** (6), **Max** (256)</span></span>
</dt> </dl>

<span data-ttu-id="3ae98-121">Nome del computer.</span><span class="sxs-lookup"><span data-stu-id="3ae98-121">Name of the computer.</span></span>

</dd> <dt>

<span data-ttu-id="3ae98-122">**NomeDominio**</span><span class="sxs-lookup"><span data-stu-id="3ae98-122">**DomainName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ae98-123">Tipo di dati: matrice **Char16**</span><span class="sxs-lookup"><span data-stu-id="3ae98-123">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="3ae98-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3ae98-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ae98-125">Qualificatori: **WmiDataId** (7), **Max** (132)</span><span class="sxs-lookup"><span data-stu-id="3ae98-125">Qualifiers: **WmiDataId** (7), **Max** (132)</span></span>
</dt> </dl>

<span data-ttu-id="3ae98-126">Nome del dominio in cui il computer è membro.</span><span class="sxs-lookup"><span data-stu-id="3ae98-126">Name of the domain in which the computer is a member.</span></span>

</dd> <dt>

<span data-ttu-id="3ae98-127">**MemSize**</span><span class="sxs-lookup"><span data-stu-id="3ae98-127">**MemSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ae98-128">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3ae98-128">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3ae98-129">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3ae98-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ae98-130">Qualificatori: **WmiDataId** (3)</span><span class="sxs-lookup"><span data-stu-id="3ae98-130">Qualifiers: **WmiDataId** (3)</span></span>
</dt> </dl>

<span data-ttu-id="3ae98-131">Quantità totale di memoria fisica disponibile per il sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="3ae98-131">Total amount of physical memory available to the operating system.</span></span>

</dd> <dt>

<span data-ttu-id="3ae98-132">**MHz**</span><span class="sxs-lookup"><span data-stu-id="3ae98-132">**MHz**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ae98-133">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3ae98-133">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3ae98-134">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3ae98-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ae98-135">Qualificatori: **WmiDataId** (1)</span><span class="sxs-lookup"><span data-stu-id="3ae98-135">Qualifiers: **WmiDataId** (1)</span></span>
</dt> </dl>

<span data-ttu-id="3ae98-136">Velocità massima del processore, in megahertz.</span><span class="sxs-lookup"><span data-stu-id="3ae98-136">Maximum speed of the processor, in megahertz.</span></span>

</dd> <dt>

<span data-ttu-id="3ae98-137">**NumberOfProcessors**</span><span class="sxs-lookup"><span data-stu-id="3ae98-137">**NumberOfProcessors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ae98-138">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3ae98-138">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3ae98-139">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3ae98-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ae98-140">Qualificatori: **WmiDataId** (2)</span><span class="sxs-lookup"><span data-stu-id="3ae98-140">Qualifiers: **WmiDataId** (2)</span></span>
</dt> </dl>

<span data-ttu-id="3ae98-141">Numero di processori nel computer.</span><span class="sxs-lookup"><span data-stu-id="3ae98-141">Number of processors on the computer.</span></span>

</dd> <dt>

<span data-ttu-id="3ae98-142">**PageSize**</span><span class="sxs-lookup"><span data-stu-id="3ae98-142">**PageSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ae98-143">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3ae98-143">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3ae98-144">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3ae98-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ae98-145">Qualificatori: **WmiDataId** (4)</span><span class="sxs-lookup"><span data-stu-id="3ae98-145">Qualifiers: **WmiDataId** (4)</span></span>
</dt> </dl>

<span data-ttu-id="3ae98-146">Dimensioni di una pagina di scambio, in byte.</span><span class="sxs-lookup"><span data-stu-id="3ae98-146">Size of a swap page, in bytes.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3ae98-147">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3ae98-147">Requirements</span></span>



| <span data-ttu-id="3ae98-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="3ae98-148">Requirement</span></span> | <span data-ttu-id="3ae98-149">Valore</span><span class="sxs-lookup"><span data-stu-id="3ae98-149">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="3ae98-150">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3ae98-150">Minimum supported client</span></span><br/> | <span data-ttu-id="3ae98-151">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="3ae98-151">None supported</span></span><br/>                            |
| <span data-ttu-id="3ae98-152">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3ae98-152">Minimum supported server</span></span><br/> | <span data-ttu-id="3ae98-153">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3ae98-153">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3ae98-154">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3ae98-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ae98-155">**SystemConfig \_ V0**</span><span class="sxs-lookup"><span data-stu-id="3ae98-155">**SystemConfig\_V0**</span></span>](systemconfig-v0.md)
</dt> </dl>

 

 




