---
description: Rappresenta un'associazione tra un servizio e un punto di accesso al servizio (SAP) che fornisce al servizio funzionalità.
ms.assetid: 9b82fad2-9731-4e0d-bdb0-d1be13ea20fc
title: Classe CIM_ServiceSAPDependency (gestione Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ServiceSAPDependency
- CIM_ServiceSAPDependency.Antecedent
- CIM_ServiceSAPDependency.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d49b63dfb37dfddf009f01122f4aa49af316fa58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313863"
---
# <a name="cim_servicesapdependency-class-hyper-v-management"></a><span data-ttu-id="630a0-103">Classe CIM_ServiceSAPDependency (gestione Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="630a0-103">CIM_ServiceSAPDependency class (Hyper-V management)</span></span>

<span data-ttu-id="630a0-104">Rappresenta un'associazione tra un servizio e un punto di accesso al servizio (SAP) che fornisce al servizio funzionalità.</span><span class="sxs-lookup"><span data-stu-id="630a0-104">Represents an association between a service and a service access point (SAP) that provides the service with functionality.</span></span>

## <a name="syntax"></a><span data-ttu-id="630a0-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="630a0-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::Service")]
class CIM_ServiceSAPDependency : CIM_Dependency
{
  CIM_ServiceAccessPoint REF Antecedent;
  CIM_Service            REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="630a0-106">Members</span><span class="sxs-lookup"><span data-stu-id="630a0-106">Members</span></span>

<span data-ttu-id="630a0-107">La classe **CIM \_ ServiceSAPDependency** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="630a0-107">The **CIM\_ServiceSAPDependency** class has these types of members:</span></span>

-   [<span data-ttu-id="630a0-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="630a0-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="630a0-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="630a0-109">Properties</span></span>

<span data-ttu-id="630a0-110">La classe **CIM \_ ServiceSAPDependency** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="630a0-110">The **CIM\_ServiceSAPDependency** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="630a0-111">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="630a0-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="630a0-112">Tipo di dati: **CIM \_ serviceAccessPoint**</span><span class="sxs-lookup"><span data-stu-id="630a0-112">Data type: **CIM\_ServiceAccessPoint**</span></span>
</dt> <dt>

<span data-ttu-id="630a0-113">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="630a0-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="630a0-114">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="630a0-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="630a0-115">Il punto di accesso al servizio richiesto.</span><span class="sxs-lookup"><span data-stu-id="630a0-115">The required service access point.</span></span>

</dd> <dt>

<span data-ttu-id="630a0-116">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="630a0-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="630a0-117">Tipo di dati **: \_ servizio CIM**</span><span class="sxs-lookup"><span data-stu-id="630a0-117">Data type: **CIM\_Service**</span></span>
</dt> <dt>

<span data-ttu-id="630a0-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="630a0-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="630a0-119">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente")</span><span class="sxs-lookup"><span data-stu-id="630a0-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="630a0-120">Il servizio che dipende da SAP.</span><span class="sxs-lookup"><span data-stu-id="630a0-120">The service that is dependent on the SAP.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="630a0-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="630a0-121">Requirements</span></span>



| <span data-ttu-id="630a0-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="630a0-122">Requirement</span></span> | <span data-ttu-id="630a0-123">Valore</span><span class="sxs-lookup"><span data-stu-id="630a0-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="630a0-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="630a0-124">Minimum supported client</span></span><br/> | <span data-ttu-id="630a0-125">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="630a0-125">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="630a0-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="630a0-126">Minimum supported server</span></span><br/> | <span data-ttu-id="630a0-127">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="630a0-127">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="630a0-128">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="630a0-128">Namespace</span></span><br/>                | <span data-ttu-id="630a0-129">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="630a0-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="630a0-130">MOF</span><span class="sxs-lookup"><span data-stu-id="630a0-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="630a0-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="630a0-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="630a0-132">DLL</span><span class="sxs-lookup"><span data-stu-id="630a0-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="630a0-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="630a0-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="630a0-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="630a0-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="630a0-135">**\_Dipendenza CIM**</span><span class="sxs-lookup"><span data-stu-id="630a0-135">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

