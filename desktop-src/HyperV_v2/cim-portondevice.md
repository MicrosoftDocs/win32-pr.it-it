---
description: Rappresenta un'associazione tra una porta o un punto di connessione e un dispositivo.
ms.assetid: b35e741a-7110-4e48-a132-d436f4fbf038
title: Classe CIM_PortOnDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PortOnDevice
- CIM_PortOnDevice.Antecedent
- CIM_PortOnDevice.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 76d8500daaa5db1746efa347e5dd10eb70a82234
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106320038"
---
# <a name="cim_portondevice-class"></a><span data-ttu-id="3fa38-103">CIM \_ PortOnDevice (classe)</span><span class="sxs-lookup"><span data-stu-id="3fa38-103">CIM\_PortOnDevice class</span></span>

<span data-ttu-id="3fa38-104">Rappresenta un'associazione tra una porta o un punto di connessione e un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3fa38-104">Represents an association between a port or connection point and a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="3fa38-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3fa38-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.8.0"), UMLPackagePath("CIM::Device::Ports"), AMENDMENT]
class CIM_PortOnDevice : CIM_HostedDependency
{
  CIM_LogicalDevice REF Antecedent;
  CIM_LogicalPort   REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="3fa38-106">Members</span><span class="sxs-lookup"><span data-stu-id="3fa38-106">Members</span></span>

<span data-ttu-id="3fa38-107">La classe **CIM \_ PortOnDevice** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="3fa38-107">The **CIM\_PortOnDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="3fa38-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="3fa38-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3fa38-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="3fa38-109">Properties</span></span>

<span data-ttu-id="3fa38-110">La classe **CIM \_ PortOnDevice** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="3fa38-110">The **CIM\_PortOnDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3fa38-111">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="3fa38-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3fa38-112">Tipo di dati: **CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="3fa38-112">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="3fa38-113">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3fa38-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3fa38-114">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="3fa38-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="3fa38-115">Il dispositivo che include la porta.</span><span class="sxs-lookup"><span data-stu-id="3fa38-115">The device that includes the port.</span></span>

</dd> <dt>

<span data-ttu-id="3fa38-116">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="3fa38-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3fa38-117">Tipo di dati: **CIM \_ LogicalPort**</span><span class="sxs-lookup"><span data-stu-id="3fa38-117">Data type: **CIM\_LogicalPort**</span></span>
</dt> <dt>

<span data-ttu-id="3fa38-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3fa38-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3fa38-119">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente")</span><span class="sxs-lookup"><span data-stu-id="3fa38-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="3fa38-120">Porta sul dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3fa38-120">The port on the device.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3fa38-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3fa38-121">Requirements</span></span>



| <span data-ttu-id="3fa38-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="3fa38-122">Requirement</span></span> | <span data-ttu-id="3fa38-123">Valore</span><span class="sxs-lookup"><span data-stu-id="3fa38-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3fa38-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3fa38-124">Minimum supported client</span></span><br/> | <span data-ttu-id="3fa38-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="3fa38-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="3fa38-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3fa38-126">Minimum supported server</span></span><br/> | <span data-ttu-id="3fa38-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3fa38-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="3fa38-128">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="3fa38-128">Namespace</span></span><br/>                | <span data-ttu-id="3fa38-129">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="3fa38-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="3fa38-130">MOF</span><span class="sxs-lookup"><span data-stu-id="3fa38-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3fa38-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3fa38-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3fa38-132">DLL</span><span class="sxs-lookup"><span data-stu-id="3fa38-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3fa38-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3fa38-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="3fa38-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3fa38-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3fa38-135">**\_HOSTEDDEPENDENCY CIM**</span><span class="sxs-lookup"><span data-stu-id="3fa38-135">**CIM\_HostedDependency**</span></span>](cim-hosteddependency.md)
</dt> </dl>

 

