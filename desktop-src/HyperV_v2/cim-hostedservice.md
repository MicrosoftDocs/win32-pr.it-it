---
description: Rappresenta un'associazione tra un servizio e il sistema che ospita il servizio. Un sistema può ospitare molti servizi, tuttavia questa classe non rappresenta servizi ospitati in più sistemi.
ms.assetid: ede67a81-cf1b-41aa-b907-5b635cf80423
title: Classe CIM_HostedService (gestione Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_HostedService
- CIM_HostedService.Antecedent
- CIM_HostedService.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 841c0e26898ed3baa4b4947779a395ee9ce870d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484205"
---
# <a name="cim_hostedservice-class-hyper-v-management"></a><span data-ttu-id="29867-104">Classe CIM_HostedService (gestione Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="29867-104">CIM_HostedService class (Hyper-V management)</span></span>

<span data-ttu-id="29867-105">Rappresenta un'associazione tra un servizio e il sistema che ospita il servizio.</span><span class="sxs-lookup"><span data-stu-id="29867-105">Represents an association between a service and the system that hosts the service.</span></span> <span data-ttu-id="29867-106">Un sistema può ospitare molti servizi, tuttavia questa classe non rappresenta servizi ospitati in più sistemi.</span><span class="sxs-lookup"><span data-stu-id="29867-106">A System can host many services, however this class does not represent services hosted across multiple systems.</span></span>

## <a name="syntax"></a><span data-ttu-id="29867-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="29867-107">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::Service"), AMENDMENT]
class CIM_HostedService : CIM_HostedDependency
{
  CIM_System  REF Antecedent;
  CIM_Service REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="29867-108">Members</span><span class="sxs-lookup"><span data-stu-id="29867-108">Members</span></span>

<span data-ttu-id="29867-109">La classe **CIM \_ servizio ospitato** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="29867-109">The **CIM\_HostedService** class has these types of members:</span></span>

-   [<span data-ttu-id="29867-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="29867-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="29867-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="29867-111">Properties</span></span>

<span data-ttu-id="29867-112">La classe **CIM \_ servizio ospitato** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="29867-112">The **CIM\_HostedService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="29867-113">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="29867-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="29867-114">Tipo di dati **: \_ sistema CIM**</span><span class="sxs-lookup"><span data-stu-id="29867-114">Data type: **CIM\_System**</span></span>
</dt> <dt>

<span data-ttu-id="29867-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="29867-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="29867-116">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente"), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="29867-116">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="29867-117">Sistema di hosting.</span><span class="sxs-lookup"><span data-stu-id="29867-117">The hosting System.</span></span>

</dd> <dt>

<span data-ttu-id="29867-118">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="29867-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="29867-119">Tipo di dati **: \_ servizio CIM**</span><span class="sxs-lookup"><span data-stu-id="29867-119">Data type: **CIM\_Service**</span></span>
</dt> <dt>

<span data-ttu-id="29867-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="29867-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="29867-121">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente"), [**debole**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="29867-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="29867-122">Servizio ospitato nel sistema.</span><span class="sxs-lookup"><span data-stu-id="29867-122">The Service hosted on the System.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="29867-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="29867-123">Requirements</span></span>



| <span data-ttu-id="29867-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="29867-124">Requirement</span></span> | <span data-ttu-id="29867-125">Valore</span><span class="sxs-lookup"><span data-stu-id="29867-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="29867-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="29867-126">Minimum supported client</span></span><br/> | <span data-ttu-id="29867-127">Windows 8</span><span class="sxs-lookup"><span data-stu-id="29867-127">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="29867-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="29867-128">Minimum supported server</span></span><br/> | <span data-ttu-id="29867-129">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="29867-129">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="29867-130">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="29867-130">Namespace</span></span><br/>                | <span data-ttu-id="29867-131">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="29867-131">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="29867-132">MOF</span><span class="sxs-lookup"><span data-stu-id="29867-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="29867-133"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="29867-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="29867-134">DLL</span><span class="sxs-lookup"><span data-stu-id="29867-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="29867-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="29867-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="29867-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="29867-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29867-137">**\_HOSTEDDEPENDENCY CIM**</span><span class="sxs-lookup"><span data-stu-id="29867-137">**CIM\_HostedDependency**</span></span>](cim-hosteddependency.md)
</dt> </dl>

 

