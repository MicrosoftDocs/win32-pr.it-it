---
description: Rappresenta un'associazione tra un punto di accesso al servizio (SAP) e il sistema che lo ospita.
ms.assetid: 82db71d6-6d14-408e-87e0-fe869e454d4d
title: Classe CIM_HostedAccessPoint (gestione Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_HostedAccessPoint
- CIM_HostedAccessPoint.Antecedent
- CIM_HostedAccessPoint.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0684c2855e7966a0c01d1d9f9bfa0cbd71c2397a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484212"
---
# <a name="cim_hostedaccesspoint-class-hyper-v-management"></a><span data-ttu-id="2404a-103">Classe CIM_HostedAccessPoint (gestione Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="2404a-103">CIM_HostedAccessPoint class (Hyper-V management)</span></span>

<span data-ttu-id="2404a-104">Rappresenta un'associazione tra un punto di accesso al servizio (SAP) e il sistema che lo ospita.</span><span class="sxs-lookup"><span data-stu-id="2404a-104">Represents an association between a service access point (SAP) and the system that hosts it.</span></span> <span data-ttu-id="2404a-105">Un sistema può ospitare più punti di accesso.</span><span class="sxs-lookup"><span data-stu-id="2404a-105">A system can host multiple access points.</span></span> <span data-ttu-id="2404a-106">Se l'implementazione di SAP è modellata, deve essere implementata da un dispositivo o una funzionalità software che fa parte del sistema che ospita SAP.</span><span class="sxs-lookup"><span data-stu-id="2404a-106">If the implementation of the SAP is modeled, it must be implemented by a device or software feature that is part of the system that hosts the SAP.</span></span>

## <a name="syntax"></a><span data-ttu-id="2404a-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2404a-107">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::Service")]
class CIM_HostedAccessPoint : CIM_HostedDependency
{
  CIM_System             REF Antecedent;
  CIM_ServiceAccessPoint REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="2404a-108">Members</span><span class="sxs-lookup"><span data-stu-id="2404a-108">Members</span></span>

<span data-ttu-id="2404a-109">La classe **CIM \_ HostedAccessPoint** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="2404a-109">The **CIM\_HostedAccessPoint** class has these types of members:</span></span>

-   [<span data-ttu-id="2404a-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2404a-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2404a-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2404a-111">Properties</span></span>

<span data-ttu-id="2404a-112">La classe **CIM \_ HostedAccessPoint** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="2404a-112">The **CIM\_HostedAccessPoint** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2404a-113">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="2404a-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2404a-114">Tipo di dati **: \_ sistema CIM**</span><span class="sxs-lookup"><span data-stu-id="2404a-114">Data type: **CIM\_System**</span></span>
</dt> <dt>

<span data-ttu-id="2404a-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2404a-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2404a-116">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente"), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="2404a-116">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="2404a-117">Sistema di hosting.</span><span class="sxs-lookup"><span data-stu-id="2404a-117">The hosting System.</span></span>

</dd> <dt>

<span data-ttu-id="2404a-118">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="2404a-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2404a-119">Tipo di dati: **CIM \_ serviceAccessPoint**</span><span class="sxs-lookup"><span data-stu-id="2404a-119">Data type: **CIM\_ServiceAccessPoint**</span></span>
</dt> <dt>

<span data-ttu-id="2404a-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2404a-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2404a-121">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente"), [**debole**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="2404a-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="2404a-122">Gli SAP ospitati nel sistema.</span><span class="sxs-lookup"><span data-stu-id="2404a-122">The SAPs that are hosted on the system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2404a-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2404a-123">Requirements</span></span>



| <span data-ttu-id="2404a-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="2404a-124">Requirement</span></span> | <span data-ttu-id="2404a-125">Valore</span><span class="sxs-lookup"><span data-stu-id="2404a-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2404a-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2404a-126">Minimum supported client</span></span><br/> | <span data-ttu-id="2404a-127">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="2404a-127">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="2404a-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2404a-128">Minimum supported server</span></span><br/> | <span data-ttu-id="2404a-129">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="2404a-129">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="2404a-130">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="2404a-130">Namespace</span></span><br/>                | <span data-ttu-id="2404a-131">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="2404a-131">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="2404a-132">MOF</span><span class="sxs-lookup"><span data-stu-id="2404a-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2404a-133"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2404a-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2404a-134">DLL</span><span class="sxs-lookup"><span data-stu-id="2404a-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2404a-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2404a-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="2404a-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2404a-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2404a-137">**\_HOSTEDDEPENDENCY CIM**</span><span class="sxs-lookup"><span data-stu-id="2404a-137">**CIM\_HostedDependency**</span></span>](cim-hosteddependency.md)
</dt> </dl>

 

