---
description: Rappresenta un intervallo contiguo di blocchi logici identificabili da un file system tramite il campo disks DeviceID (Key).
ms.assetid: a70b4bee-7f5d-43b1-a7cc-7f0593bc8a11
title: Classe CIM_LogicalDisk (gestione Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDisk
- CIM_LogicalDisk.NameFormat
- CIM_LogicalDisk.NameNamespace
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b7305d0fa6ef45b5a97eb0fb6ab9ea740c98a392
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968029"
---
# <a name="cim_logicaldisk-class-hyper-v-management"></a><span data-ttu-id="db828-103">Classe CIM_LogicalDisk (gestione Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="db828-103">CIM_LogicalDisk class (Hyper-V management)</span></span>

<span data-ttu-id="db828-104">Rappresenta un intervallo contiguo di blocchi logici identificabili da un file system tramite il campo **DeviceID** (Key) del disco.</span><span class="sxs-lookup"><span data-stu-id="db828-104">Represents a contiguous range of logical blocks that is identifiable by a file system through the disk's **DeviceID** (key) field.</span></span> <span data-ttu-id="db828-105">Ad esempio, in un ambiente Windows, il campo **DeviceID** contiene una lettera di unità; in un ambiente UNIX, contiene il percorso di accesso; e in un ambiente NetWare contiene il nome del volume.</span><span class="sxs-lookup"><span data-stu-id="db828-105">For example, in a Windows environment, the **DeviceID** field contains a drive letter; in a UNIX environment, it contains the access path; and in a NetWare environment, it contains the volume name.</span></span>

## <a name="syntax"></a><span data-ttu-id="db828-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="db828-106">Syntax</span></span>

``` syntax
[Abstract, Version("2.15.0"), UMLPackagePath("CIM::Device::StorageExtents"), AMENDMENT]
class CIM_LogicalDisk : CIM_StorageExtent
{
  uint16 NameFormat = 12;
  uint16 NameNamespace = 8;
};
```

## <a name="members"></a><span data-ttu-id="db828-107">Members</span><span class="sxs-lookup"><span data-stu-id="db828-107">Members</span></span>

<span data-ttu-id="db828-108">La classe **CIM \_ disco logico** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="db828-108">The **CIM\_LogicalDisk** class has these types of members:</span></span>

-   [<span data-ttu-id="db828-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="db828-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="db828-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="db828-110">Properties</span></span>

<span data-ttu-id="db828-111">La classe **CIM \_ disco logico** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="db828-111">The **CIM\_LogicalDisk** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="db828-112">**NameFormat**</span><span class="sxs-lookup"><span data-stu-id="db828-112">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db828-113">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="db828-113">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="db828-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="db828-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="db828-115">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NameFormat")</span><span class="sxs-lookup"><span data-stu-id="db828-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NameFormat")</span></span>
</dt> </dl>

<span data-ttu-id="db828-116">Indica se il dispositivo logico utilizza il formato del nome del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="db828-116">Indicates whether the logical device uses the name format of the OS.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="db828-117">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="db828-117">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_Device_Name"></span><span id="os_device_name"></span><span id="OS_DEVICE_NAME"></span>

<span data-ttu-id="db828-118">**Nome dispositivo del sistema operativo** (12)</span><span class="sxs-lookup"><span data-stu-id="db828-118">**OS Device Name** (12)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="db828-119">**NameNamespace**</span><span class="sxs-lookup"><span data-stu-id="db828-119">**NameNamespace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db828-120">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="db828-120">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="db828-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="db828-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="db828-122">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NameNamespace")</span><span class="sxs-lookup"><span data-stu-id="db828-122">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NameNamespace")</span></span>
</dt> </dl>

<span data-ttu-id="db828-123">Indica se il dispositivo logico ha lo stesso spazio dei nomi del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="db828-123">Indicates whether the logical device has the same namespace as the OS.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="db828-124">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="db828-124">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_Device_Namespace"></span><span id="os_device_namespace"></span><span id="OS_DEVICE_NAMESPACE"></span>

<span data-ttu-id="db828-125">**Spazio dei nomi del dispositivo del sistema operativo** (8)</span><span class="sxs-lookup"><span data-stu-id="db828-125">**OS Device Namespace** (8)</span></span>


<span data-ttu-id="db828-126"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="db828-126"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="db828-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="db828-127">Requirements</span></span>



| <span data-ttu-id="db828-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="db828-128">Requirement</span></span> | <span data-ttu-id="db828-129">Valore</span><span class="sxs-lookup"><span data-stu-id="db828-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="db828-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="db828-130">Minimum supported client</span></span><br/> | <span data-ttu-id="db828-131">Windows 8</span><span class="sxs-lookup"><span data-stu-id="db828-131">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="db828-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="db828-132">Minimum supported server</span></span><br/> | <span data-ttu-id="db828-133">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="db828-133">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="db828-134">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="db828-134">Namespace</span></span><br/>                | <span data-ttu-id="db828-135">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="db828-135">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="db828-136">MOF</span><span class="sxs-lookup"><span data-stu-id="db828-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="db828-137"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="db828-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="db828-138">DLL</span><span class="sxs-lookup"><span data-stu-id="db828-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="db828-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="db828-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="db828-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="db828-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db828-141">**\_STORAGEEXTENT CIM**</span><span class="sxs-lookup"><span data-stu-id="db828-141">**CIM\_StorageExtent**</span></span>](cim-storageextent.md)
</dt> </dl>

 

