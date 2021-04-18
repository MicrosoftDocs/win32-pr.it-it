---
description: Rappresenta lo stato della partizione GPU.
ms.assetid: 319b37d5-b5f0-4251-9482-316347a9015b
title: Classe Msvm_GpuPartition
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GpuPartition
- Msvm_GpuPartition.DeviceInstancePath
- Msvm_GpuPartition.PartitionId
- Msvm_GpuPartition.PartitionVfLuid
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: cc0975644609832c692f5522cc756240f7a5bff6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307913"
---
# <a name="msvm_gpupartition-class"></a><span data-ttu-id="d0065-103">\_Classe MSVM GpuPartition</span><span class="sxs-lookup"><span data-stu-id="d0065-103">Msvm\_GpuPartition class</span></span>

<span data-ttu-id="d0065-104">Rappresenta lo stato della partizione GPU.</span><span class="sxs-lookup"><span data-stu-id="d0065-104">Represents the state of the GPU partition.</span></span>

<span data-ttu-id="d0065-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="d0065-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0065-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d0065-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_GpuPartition : CIM_LogicalDevice
{
  string DeviceInstancePath;
  uint16 PartitionId;
  string PartitionVfLuid;
};
```

## <a name="members"></a><span data-ttu-id="d0065-107">Members</span><span class="sxs-lookup"><span data-stu-id="d0065-107">Members</span></span>

<span data-ttu-id="d0065-108">La **classe \_ GpuPartition di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="d0065-108">The **Msvm\_GpuPartition** class has these types of members:</span></span>

-   [<span data-ttu-id="d0065-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d0065-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d0065-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d0065-110">Properties</span></span>

<span data-ttu-id="d0065-111">La **classe \_ GpuPartition di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="d0065-111">The **Msvm\_GpuPartition** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d0065-112">**DeviceInstancePath**</span><span class="sxs-lookup"><span data-stu-id="d0065-112">**DeviceInstancePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0065-113">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d0065-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d0065-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d0065-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d0065-115">Stringa che contiene il percorso dell'istanza del dispositivo che identifica il dispositivo di partizione GPU.</span><span class="sxs-lookup"><span data-stu-id="d0065-115">A string containing the device instance path that identifies the GPU partition device.</span></span>

</dd> <dt>

<span data-ttu-id="d0065-116">**PartitionId**</span><span class="sxs-lookup"><span data-stu-id="d0065-116">**PartitionId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0065-117">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d0065-117">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d0065-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d0065-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d0065-119">ID partizione del dispositivo di partizione GPU.</span><span class="sxs-lookup"><span data-stu-id="d0065-119">The partition ID of the GPU partition device.</span></span>

</dd> <dt>

<span data-ttu-id="d0065-120">**PartitionVfLuid**</span><span class="sxs-lookup"><span data-stu-id="d0065-120">**PartitionVfLuid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0065-121">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d0065-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d0065-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d0065-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d0065-123">Funzione virtuale LUID, che rappresenta una partizione GPU.</span><span class="sxs-lookup"><span data-stu-id="d0065-123">The virtual function LUID, which represents a GPU partition.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d0065-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d0065-124">Requirements</span></span>



| <span data-ttu-id="d0065-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="d0065-125">Requirement</span></span> | <span data-ttu-id="d0065-126">Valore</span><span class="sxs-lookup"><span data-stu-id="d0065-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d0065-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d0065-127">Minimum supported client</span></span><br/> | <span data-ttu-id="d0065-128">Solo app desktop Windows 10 versione 1703 \[\]</span><span class="sxs-lookup"><span data-stu-id="d0065-128">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="d0065-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d0065-129">Minimum supported server</span></span><br/> | <span data-ttu-id="d0065-130">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="d0065-130">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="d0065-131">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="d0065-131">Namespace</span></span><br/>                | <span data-ttu-id="d0065-132">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="d0065-132">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="d0065-133">MOF</span><span class="sxs-lookup"><span data-stu-id="d0065-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d0065-134"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d0065-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d0065-135">DLL</span><span class="sxs-lookup"><span data-stu-id="d0065-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d0065-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d0065-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d0065-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d0065-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0065-138">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="d0065-138">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

 




