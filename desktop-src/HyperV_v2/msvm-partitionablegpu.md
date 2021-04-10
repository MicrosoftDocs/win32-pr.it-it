---
description: Rappresenta una GPU partizionabile. Ogni GPU può essere sezionata in una serie di partizioni GPU, che possono essere assegnate a una macchina virtuale come vGPU.
ms.assetid: a32dfc03-6967-4fa3-ae32-bf074137740b
title: Classe Msvm_PartitionableGpu
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_PartitionableGpu
- Msvm_PartitionableGpu.ValidPartitionCounts
- Msvm_PartitionableGpu.PartitionCount
- Msvm_PartitionableGpu.TotalVRAM
- Msvm_PartitionableGpu.AvailableVRAM
- Msvm_PartitionableGpu.MinPartitionVRAM
- Msvm_PartitionableGpu.MaxPartitionVRAM
- Msvm_PartitionableGpu.OptimalPartitionVRAM
- Msvm_PartitionableGpu.TotalEncode
- Msvm_PartitionableGpu.AvailableEncode
- Msvm_PartitionableGpu.MinPartitionEncode
- Msvm_PartitionableGpu.MaxPartitionEncode
- Msvm_PartitionableGpu.OptimalPartitionEncode
- Msvm_PartitionableGpu.TotalDecode
- Msvm_PartitionableGpu.AvailableDecode
- Msvm_PartitionableGpu.MinPartitionDecode
- Msvm_PartitionableGpu.MaxPartitionDecode
- Msvm_PartitionableGpu.OptimalPartitionDecode
- Msvm_PartitionableGpu.TotalCompute
- Msvm_PartitionableGpu.AvailableCompute
- Msvm_PartitionableGpu.MinPartitionCompute
- Msvm_PartitionableGpu.MaxPartitionCompute
- Msvm_PartitionableGpu.OptimalPartitionCompute
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7f82904608a8e2ee4dfa13942066d57d35d511f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885138"
---
# <a name="msvm_partitionablegpu-class"></a><span data-ttu-id="e7148-104">\_Classe MSVM PartitionableGpu</span><span class="sxs-lookup"><span data-stu-id="e7148-104">Msvm\_PartitionableGpu class</span></span>

<span data-ttu-id="e7148-105">Rappresenta una GPU partizionabile.</span><span class="sxs-lookup"><span data-stu-id="e7148-105">Represents a partitionable GPU.</span></span> <span data-ttu-id="e7148-106">Ogni GPU può essere sezionata in una serie di partizioni GPU, che possono essere assegnate a una macchina virtuale come vGPU.</span><span class="sxs-lookup"><span data-stu-id="e7148-106">Each GPU can be sliced into a number of GPU partitions, which can be assigned to a virtual machine as a vGPU.</span></span>

<span data-ttu-id="e7148-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="e7148-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7148-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e7148-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_PartitionableGpu : CIM_ComputerSystem
{
  uint16 ValidPartitionCounts[];
  uint16 PartitionCount;
  uint64 TotalVRAM;
  uint64 AvailableVRAM;
  uint64 MinPartitionVRAM;
  uint64 MaxPartitionVRAM;
  uint64 OptimalPartitionVRAM;
  uint64 TotalEncode;
  uint64 AvailableEncode;
  uint64 MinPartitionEncode;
  uint64 MaxPartitionEncode;
  uint64 OptimalPartitionEncode;
  uint64 TotalDecode;
  uint64 AvailableDecode;
  uint64 MinPartitionDecode;
  uint64 MaxPartitionDecode;
  uint64 OptimalPartitionDecode;
  uint64 TotalCompute;
  uint64 AvailableCompute;
  uint64 MinPartitionCompute;
  uint64 MaxPartitionCompute;
  uint64 OptimalPartitionCompute;
};
```

## <a name="members"></a><span data-ttu-id="e7148-109">Members</span><span class="sxs-lookup"><span data-stu-id="e7148-109">Members</span></span>

<span data-ttu-id="e7148-110">La **classe \_ PartitionableGpu di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="e7148-110">The **Msvm\_PartitionableGpu** class has these types of members:</span></span>

-   [<span data-ttu-id="e7148-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e7148-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e7148-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e7148-112">Properties</span></span>

<span data-ttu-id="e7148-113">La **classe \_ PartitionableGpu di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="e7148-113">The **Msvm\_PartitionableGpu** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e7148-114">**AvailableCompute**</span><span class="sxs-lookup"><span data-stu-id="e7148-114">**AvailableCompute**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7148-115">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e7148-115">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e7148-116">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e7148-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e7148-117">Quantità disponibile di motori di calcolo che verranno visualizzati nella partizione GPU.</span><span class="sxs-lookup"><span data-stu-id="e7148-117">The available amount of compute engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="e7148-118">**AvailableDecode**</span><span class="sxs-lookup"><span data-stu-id="e7148-118">**AvailableDecode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7148-119">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e7148-119">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e7148-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e7148-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e7148-121">Quantità di motori di decodifica disponibili che verranno visualizzati nella partizione GPU.</span><span class="sxs-lookup"><span data-stu-id="e7148-121">The available amount of decode engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="e7148-122">**AvailableEncode**</span><span class="sxs-lookup"><span data-stu-id="e7148-122">**AvailableEncode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7148-123">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e7148-123">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e7148-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e7148-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e7148-125">Quantità disponibile di motori di codifica che verranno visualizzati nella partizione GPU.</span><span class="sxs-lookup"><span data-stu-id="e7148-125">The available amount of encode engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="e7148-126">**AvailableVRAM**</span><span class="sxs-lookup"><span data-stu-id="e7148-126">**AvailableVRAM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7148-127">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e7148-127">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e7148-128">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e7148-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e7148-129">Quantità di VRAM disponibile che verrà visualizzata nella partizione GPU.</span><span class="sxs-lookup"><span data-stu-id="e7148-129">The available amount of VRAM which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="e7148-130">**MaxPartitionCompute**</span><span class="sxs-lookup"><span data-stu-id="e7148-130">**MaxPartitionCompute**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7148-131">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e7148-131">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e7148-132">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e7148-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e7148-133">Quantità massima di motori di calcolo che verranno visualizzati nella partizione GPU.</span><span class="sxs-lookup"><span data-stu-id="e7148-133">The maximum amount of compute engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="e7148-134">**MaxPartitionDecode**</span><span class="sxs-lookup"><span data-stu-id="e7148-134">**MaxPartitionDecode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7148-135">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e7148-135">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e7148-136">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e7148-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e7148-137">Quantità massima di motori di decodifica che verranno visualizzati nella partizione GPU.</span><span class="sxs-lookup"><span data-stu-id="e7148-137">The maximum amount of decode engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="e7148-138">**MaxPartitionEncode**</span><span class="sxs-lookup"><span data-stu-id="e7148-138">**MaxPartitionEncode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7148-139">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e7148-139">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e7148-140">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e7148-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e7148-141">Quantità massima di motori di codifica che verranno visualizzati nella partizione GPU.</span><span class="sxs-lookup"><span data-stu-id="e7148-141">The maximum amount of encode engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="e7148-142">**MaxPartitionVRAM**</span><span class="sxs-lookup"><span data-stu-id="e7148-142">**MaxPartitionVRAM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7148-143">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e7148-143">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e7148-144">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e7148-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e7148-145">Quantità massima di VRAM che verrà visualizzata nella partizione GPU.</span><span class="sxs-lookup"><span data-stu-id="e7148-145">The maximum amount of VRAM which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="e7148-146">**MinPartitionCompute**</span><span class="sxs-lookup"><span data-stu-id="e7148-146">**MinPartitionCompute**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7148-147">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e7148-147">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e7148-148">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e7148-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e7148-149">Quantità minima di motori di calcolo che verranno visualizzati nella partizione GPU.</span><span class="sxs-lookup"><span data-stu-id="e7148-149">The minumum amount of compute engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="e7148-150">**MinPartitionDecode**</span><span class="sxs-lookup"><span data-stu-id="e7148-150">**MinPartitionDecode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7148-151">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e7148-151">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e7148-152">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e7148-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e7148-153">Quantità minima di motori di decodifica che verranno visualizzati nella partizione GPU.</span><span class="sxs-lookup"><span data-stu-id="e7148-153">The minimum amount of decode engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="e7148-154">**MinPartitionEncode**</span><span class="sxs-lookup"><span data-stu-id="e7148-154">**MinPartitionEncode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7148-155">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e7148-155">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e7148-156">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e7148-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e7148-157">Quantità minima di motori di codifica che verranno visualizzati nella partizione GPU.</span><span class="sxs-lookup"><span data-stu-id="e7148-157">The minumum amount of encode engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="e7148-158">**MinPartitionVRAM**</span><span class="sxs-lookup"><span data-stu-id="e7148-158">**MinPartitionVRAM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7148-159">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e7148-159">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e7148-160">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e7148-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e7148-161">Quantità minima di VRAM che verrà visualizzata nella partizione GPU.</span><span class="sxs-lookup"><span data-stu-id="e7148-161">The minimum amount of VRAM which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="e7148-162">**OptimalPartitionCompute**</span><span class="sxs-lookup"><span data-stu-id="e7148-162">**OptimalPartitionCompute**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7148-163">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e7148-163">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e7148-164">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e7148-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e7148-165">Quantità ottimale di motori di calcolo che verranno visualizzati nella partizione GPU.</span><span class="sxs-lookup"><span data-stu-id="e7148-165">The optimal amount of compute engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="e7148-166">**OptimalPartitionDecode**</span><span class="sxs-lookup"><span data-stu-id="e7148-166">**OptimalPartitionDecode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7148-167">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e7148-167">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e7148-168">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e7148-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e7148-169">Quantità ottimale di motori di decodifica che verranno visualizzati nella partizione GPU.</span><span class="sxs-lookup"><span data-stu-id="e7148-169">The optimal amount of decode engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="e7148-170">**OptimalPartitionEncode**</span><span class="sxs-lookup"><span data-stu-id="e7148-170">**OptimalPartitionEncode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7148-171">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e7148-171">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e7148-172">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e7148-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e7148-173">La quantità ottimale di motori di codifica che verranno visualizzati nella partizione GPU.</span><span class="sxs-lookup"><span data-stu-id="e7148-173">The optimal amount of encode engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="e7148-174">**OptimalPartitionVRAM**</span><span class="sxs-lookup"><span data-stu-id="e7148-174">**OptimalPartitionVRAM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7148-175">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e7148-175">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e7148-176">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e7148-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e7148-177">Quantità ottimale di VRAM che verrà visualizzata nella partizione GPU.</span><span class="sxs-lookup"><span data-stu-id="e7148-177">The optimal amount of VRAM which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="e7148-178">**PartitionCount**</span><span class="sxs-lookup"><span data-stu-id="e7148-178">**PartitionCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7148-179">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e7148-179">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e7148-180">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="e7148-180">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e7148-181">Quantità di partizioni GPU in cui viene sezionata la GPU fisica.</span><span class="sxs-lookup"><span data-stu-id="e7148-181">The amount of GPU partitions the physical GPU is sliced into.</span></span>

</dd> <dt>

<span data-ttu-id="e7148-182">**TotalCompute**</span><span class="sxs-lookup"><span data-stu-id="e7148-182">**TotalCompute**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7148-183">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e7148-183">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e7148-184">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e7148-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e7148-185">Quantità totale di motori di calcolo che verranno visualizzati nella partizione GPU.</span><span class="sxs-lookup"><span data-stu-id="e7148-185">The total amount of compute engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="e7148-186">**TotalDecode**</span><span class="sxs-lookup"><span data-stu-id="e7148-186">**TotalDecode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7148-187">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e7148-187">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e7148-188">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e7148-188">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e7148-189">Quantità totale di motori di decodifica che verranno visualizzati nella partizione GPU.</span><span class="sxs-lookup"><span data-stu-id="e7148-189">The total amount of decode engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="e7148-190">**TotalEncode**</span><span class="sxs-lookup"><span data-stu-id="e7148-190">**TotalEncode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7148-191">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e7148-191">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e7148-192">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e7148-192">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e7148-193">Quantità totale di motori di codifica che verranno visualizzati nella partizione GPU.</span><span class="sxs-lookup"><span data-stu-id="e7148-193">The total amount of encode engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="e7148-194">**TotalVRAM**</span><span class="sxs-lookup"><span data-stu-id="e7148-194">**TotalVRAM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7148-195">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e7148-195">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e7148-196">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e7148-196">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e7148-197">Quantità totale di VRAM che verrà visualizzata nella partizione GPU.</span><span class="sxs-lookup"><span data-stu-id="e7148-197">The total amount of VRAM which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="e7148-198">**ValidPartitionCounts**</span><span class="sxs-lookup"><span data-stu-id="e7148-198">**ValidPartitionCounts**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7148-199">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e7148-199">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="e7148-200">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="e7148-200">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e7148-201">Matrice di opzioni di partizione GPU valide in cui è possibile suddividere la GPU fisica.</span><span class="sxs-lookup"><span data-stu-id="e7148-201">An array of valid GPU partition options the physical GPU can be sliced into.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e7148-202">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e7148-202">Requirements</span></span>



| <span data-ttu-id="e7148-203">Requisito</span><span class="sxs-lookup"><span data-stu-id="e7148-203">Requirement</span></span> | <span data-ttu-id="e7148-204">Valore</span><span class="sxs-lookup"><span data-stu-id="e7148-204">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7148-205">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e7148-205">Minimum supported client</span></span><br/> | <span data-ttu-id="e7148-206">Solo app desktop Windows 10 versione 1703 \[\]</span><span class="sxs-lookup"><span data-stu-id="e7148-206">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="e7148-207">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e7148-207">Minimum supported server</span></span><br/> | <span data-ttu-id="e7148-208">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="e7148-208">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="e7148-209">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="e7148-209">Namespace</span></span><br/>                | <span data-ttu-id="e7148-210">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="e7148-210">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="e7148-211">MOF</span><span class="sxs-lookup"><span data-stu-id="e7148-211">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e7148-212"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e7148-212"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e7148-213">DLL</span><span class="sxs-lookup"><span data-stu-id="e7148-213">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e7148-214"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e7148-214"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e7148-215">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e7148-215">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7148-216">**\_ComputerSystem CIM**</span><span class="sxs-lookup"><span data-stu-id="e7148-216">**CIM\_ComputerSystem**</span></span>](cim-computersystem.md)
</dt> </dl>

 

 




