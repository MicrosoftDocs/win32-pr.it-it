---
description: Rappresenta lo stato configurato di un dispositivo di partizione GPU.
ms.assetid: 33ec4ea2-4e79-4c84-8abe-da8308ad6702
title: Classe Msvm_GpuPartitionSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GpuPartitionSettingData
- Msvm_GpuPartitionSettingData.MinPartitionVRAM
- Msvm_GpuPartitionSettingData.MaxPartitionVRAM
- Msvm_GpuPartitionSettingData.OptimalPartitionVRAM
- Msvm_GpuPartitionSettingData.MinPartitionEncode
- Msvm_GpuPartitionSettingData.MaxPartitionEncode
- Msvm_GpuPartitionSettingData.OptimalPartitionEncode
- Msvm_GpuPartitionSettingData.MinPartitionDecode
- Msvm_GpuPartitionSettingData.MaxPartitionDecode
- Msvm_GpuPartitionSettingData.OptimalPartitionDecode
- Msvm_GpuPartitionSettingData.MinPartitionCompute
- Msvm_GpuPartitionSettingData.MaxPartitionCompute
- Msvm_GpuPartitionSettingData.OptimalPartitionCompute
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7d8c9809b3a062654eaf0fb7a73b75b0188f7284
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966792"
---
# <a name="msvm_gpupartitionsettingdata-class"></a><span data-ttu-id="13a25-103">\_Classe MSVM GpuPartitionSettingData</span><span class="sxs-lookup"><span data-stu-id="13a25-103">Msvm\_GpuPartitionSettingData class</span></span>

<span data-ttu-id="13a25-104">Rappresenta lo stato configurato di un dispositivo di partizione GPU.</span><span class="sxs-lookup"><span data-stu-id="13a25-104">Represents the configured state of a GPU partition device.</span></span>

<span data-ttu-id="13a25-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="13a25-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="13a25-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="13a25-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_GpuPartitionSettingData : CIM_ResourceAllocationSettingData
{
  uint64 MinPartitionVRAM;
  uint64 MaxPartitionVRAM;
  uint64 OptimalPartitionVRAM;
  uint64 MinPartitionEncode;
  uint64 MaxPartitionEncode;
  uint64 OptimalPartitionEncode;
  uint64 MinPartitionDecode;
  uint64 MaxPartitionDecode;
  uint64 OptimalPartitionDecode;
  uint64 MinPartitionCompute;
  uint64 MaxPartitionCompute;
  uint64 OptimalPartitionCompute;
};
```

## <a name="members"></a><span data-ttu-id="13a25-107">Members</span><span class="sxs-lookup"><span data-stu-id="13a25-107">Members</span></span>

<span data-ttu-id="13a25-108">La **classe \_ GpuPartitionSettingData di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="13a25-108">The **Msvm\_GpuPartitionSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="13a25-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="13a25-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="13a25-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="13a25-110">Properties</span></span>

<span data-ttu-id="13a25-111">La **classe \_ GpuPartitionSettingData di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="13a25-111">The **Msvm\_GpuPartitionSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="13a25-112">**MaxPartitionCompute**</span><span class="sxs-lookup"><span data-stu-id="13a25-112">**MaxPartitionCompute**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13a25-113">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="13a25-113">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="13a25-114">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="13a25-114">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="13a25-115">Quantità massima di motori di calcolo che verranno visualizzati nella partizione GPU.</span><span class="sxs-lookup"><span data-stu-id="13a25-115">The maximum amount of compute engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="13a25-116">**MaxPartitionDecode**</span><span class="sxs-lookup"><span data-stu-id="13a25-116">**MaxPartitionDecode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13a25-117">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="13a25-117">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="13a25-118">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="13a25-118">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="13a25-119">Quantità massima di motori di decodifica che verranno visualizzati nella partizione GPU.</span><span class="sxs-lookup"><span data-stu-id="13a25-119">The maximum amount of decode engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="13a25-120">**MaxPartitionEncode**</span><span class="sxs-lookup"><span data-stu-id="13a25-120">**MaxPartitionEncode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13a25-121">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="13a25-121">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="13a25-122">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="13a25-122">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="13a25-123">Quantità massima di motori di codifica che verranno visualizzati nella partizione GPU.</span><span class="sxs-lookup"><span data-stu-id="13a25-123">The maximum amount of encode engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="13a25-124">**MaxPartitionVRAM**</span><span class="sxs-lookup"><span data-stu-id="13a25-124">**MaxPartitionVRAM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13a25-125">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="13a25-125">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="13a25-126">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="13a25-126">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="13a25-127">Quantità massima di VRAM che verrà visualizzata nella partizione GPU.</span><span class="sxs-lookup"><span data-stu-id="13a25-127">The maximum amount of VRAM which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="13a25-128">**MinPartitionCompute**</span><span class="sxs-lookup"><span data-stu-id="13a25-128">**MinPartitionCompute**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13a25-129">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="13a25-129">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="13a25-130">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="13a25-130">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="13a25-131">Quantità minima di motori di calcolo che verranno visualizzati nella partizione GPU.</span><span class="sxs-lookup"><span data-stu-id="13a25-131">The minumum amount of compute engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="13a25-132">**MinPartitionDecode**</span><span class="sxs-lookup"><span data-stu-id="13a25-132">**MinPartitionDecode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13a25-133">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="13a25-133">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="13a25-134">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="13a25-134">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="13a25-135">Quantità minima di motori di decodifica che verranno visualizzati nella partizione GPU.</span><span class="sxs-lookup"><span data-stu-id="13a25-135">The minimum amount of decode engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="13a25-136">**MinPartitionEncode**</span><span class="sxs-lookup"><span data-stu-id="13a25-136">**MinPartitionEncode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13a25-137">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="13a25-137">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="13a25-138">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="13a25-138">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="13a25-139">Quantità minima di motori di codifica che verranno visualizzati nella partizione GPU.</span><span class="sxs-lookup"><span data-stu-id="13a25-139">The minimum amount of encode engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="13a25-140">**MinPartitionVRAM**</span><span class="sxs-lookup"><span data-stu-id="13a25-140">**MinPartitionVRAM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13a25-141">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="13a25-141">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="13a25-142">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="13a25-142">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="13a25-143">Quantità minima di VRAM che verrà visualizzata nella partizione GPU.</span><span class="sxs-lookup"><span data-stu-id="13a25-143">The minimum amount of VRAM which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="13a25-144">**OptimalPartitionCompute**</span><span class="sxs-lookup"><span data-stu-id="13a25-144">**OptimalPartitionCompute**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13a25-145">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="13a25-145">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="13a25-146">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="13a25-146">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="13a25-147">Quantità ottimale di motori di calcolo che verranno visualizzati nella partizione GPU.</span><span class="sxs-lookup"><span data-stu-id="13a25-147">The optimal amount of compute engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="13a25-148">**OptimalPartitionDecode**</span><span class="sxs-lookup"><span data-stu-id="13a25-148">**OptimalPartitionDecode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13a25-149">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="13a25-149">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="13a25-150">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="13a25-150">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="13a25-151">Quantità ottimale di motori di decodifica che verranno visualizzati nella partizione GPU.</span><span class="sxs-lookup"><span data-stu-id="13a25-151">The optimal amount of decode engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="13a25-152">**OptimalPartitionEncode**</span><span class="sxs-lookup"><span data-stu-id="13a25-152">**OptimalPartitionEncode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13a25-153">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="13a25-153">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="13a25-154">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="13a25-154">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="13a25-155">La quantità ottimale di motori di codifica che verranno visualizzati nella partizione GPU.</span><span class="sxs-lookup"><span data-stu-id="13a25-155">The optimal amount of encode engines which will appear in the GPU partition.</span></span>

</dd> <dt>

<span data-ttu-id="13a25-156">**OptimalPartitionVRAM**</span><span class="sxs-lookup"><span data-stu-id="13a25-156">**OptimalPartitionVRAM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13a25-157">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="13a25-157">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="13a25-158">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="13a25-158">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="13a25-159">Quantità ottimale di VRAM che verrà visualizzata nella partizione GPU.</span><span class="sxs-lookup"><span data-stu-id="13a25-159">The optimal amount of VRAM which will appear in the GPU partition.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="13a25-160">Requisiti</span><span class="sxs-lookup"><span data-stu-id="13a25-160">Requirements</span></span>



| <span data-ttu-id="13a25-161">Requisito</span><span class="sxs-lookup"><span data-stu-id="13a25-161">Requirement</span></span> | <span data-ttu-id="13a25-162">Valore</span><span class="sxs-lookup"><span data-stu-id="13a25-162">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13a25-163">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="13a25-163">Minimum supported client</span></span><br/> | <span data-ttu-id="13a25-164">Solo app desktop Windows 10 versione 1703 \[\]</span><span class="sxs-lookup"><span data-stu-id="13a25-164">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="13a25-165">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="13a25-165">Minimum supported server</span></span><br/> | <span data-ttu-id="13a25-166">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="13a25-166">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="13a25-167">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="13a25-167">Namespace</span></span><br/>                | <span data-ttu-id="13a25-168">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="13a25-168">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="13a25-169">MOF</span><span class="sxs-lookup"><span data-stu-id="13a25-169">MOF</span></span><br/>                      | <dl> <span data-ttu-id="13a25-170"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="13a25-170"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="13a25-171">DLL</span><span class="sxs-lookup"><span data-stu-id="13a25-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="13a25-172"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="13a25-172"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="13a25-173">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="13a25-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13a25-174">**\_RESOURCEALLOCATIONSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="13a25-174">**CIM\_ResourceAllocationSettingData**</span></span>](cim-resourceallocationsettingdata.md)
</dt> </dl>

 

 




