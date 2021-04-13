---
description: Rappresenta un'associazione tra due punti di accesso al servizio (SAP), in cui un SAP è dipendente dall'altro per utilizzare o connettersi a un servizio.
ms.assetid: fba4144b-833f-469f-93df-e8a79aa37811
title: Classe CIM_SAPSAPDependency (gestione Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SAPSAPDependency
- CIM_SAPSAPDependency.Antecedent
- CIM_SAPSAPDependency.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 6888cbb74ea03b85bc9abfcea24e65660fd65953
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526779"
---
# <a name="cim_sapsapdependency-class-hyper-v-management"></a><span data-ttu-id="dcb2e-103">Classe CIM_SAPSAPDependency (gestione Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="dcb2e-103">CIM_SAPSAPDependency class (Hyper-V management)</span></span>

<span data-ttu-id="dcb2e-104">Rappresenta un'associazione tra due punti di accesso al servizio (SAP), in cui un SAP è dipendente dall'altro per utilizzare o connettersi a un servizio.</span><span class="sxs-lookup"><span data-stu-id="dcb2e-104">Represents an association between two service access points (SAP), in which one SAP is dependant on the other to utilize or connect with a service.</span></span> <span data-ttu-id="dcb2e-105">Per stampare, ad esempio, in una stampante di rete, i punti di accesso di stampa locali devono usare gli SAP correlati alla rete sottostanti per inviare la richiesta di stampa.</span><span class="sxs-lookup"><span data-stu-id="dcb2e-105">For example, to print on a network printer, local print access points must utilize underlying network-related SAPs to send the print request.</span></span>

## <a name="syntax"></a><span data-ttu-id="dcb2e-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dcb2e-106">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::Service"), AMENDMENT]
class CIM_SAPSAPDependency : CIM_Dependency
{
  CIM_ServiceAccessPoint REF Antecedent;
  CIM_ServiceAccessPoint REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="dcb2e-107">Members</span><span class="sxs-lookup"><span data-stu-id="dcb2e-107">Members</span></span>

<span data-ttu-id="dcb2e-108">La classe **CIM \_ SAPSAPDependency** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="dcb2e-108">The **CIM\_SAPSAPDependency** class has these types of members:</span></span>

-   [<span data-ttu-id="dcb2e-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="dcb2e-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="dcb2e-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="dcb2e-110">Properties</span></span>

<span data-ttu-id="dcb2e-111">La classe **CIM \_ SAPSAPDependency** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="dcb2e-111">The **CIM\_SAPSAPDependency** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="dcb2e-112">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="dcb2e-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dcb2e-113">Tipo di dati: **CIM \_ serviceAccessPoint**</span><span class="sxs-lookup"><span data-stu-id="dcb2e-113">Data type: **CIM\_ServiceAccessPoint**</span></span>
</dt> <dt>

<span data-ttu-id="dcb2e-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dcb2e-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dcb2e-115">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="dcb2e-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="dcb2e-116">Riferimento al SAP richiesto.</span><span class="sxs-lookup"><span data-stu-id="dcb2e-116">A reference to the required SAP.</span></span>

</dd> <dt>

<span data-ttu-id="dcb2e-117">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="dcb2e-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dcb2e-118">Tipo di dati: **CIM \_ serviceAccessPoint**</span><span class="sxs-lookup"><span data-stu-id="dcb2e-118">Data type: **CIM\_ServiceAccessPoint**</span></span>
</dt> <dt>

<span data-ttu-id="dcb2e-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dcb2e-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dcb2e-120">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente")</span><span class="sxs-lookup"><span data-stu-id="dcb2e-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="dcb2e-121">Riferimento al SAP dipendente.</span><span class="sxs-lookup"><span data-stu-id="dcb2e-121">A reference to the dependant SAP.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="dcb2e-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dcb2e-122">Requirements</span></span>



| <span data-ttu-id="dcb2e-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="dcb2e-123">Requirement</span></span> | <span data-ttu-id="dcb2e-124">Valore</span><span class="sxs-lookup"><span data-stu-id="dcb2e-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dcb2e-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dcb2e-125">Minimum supported client</span></span><br/> | <span data-ttu-id="dcb2e-126">Windows 8</span><span class="sxs-lookup"><span data-stu-id="dcb2e-126">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="dcb2e-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dcb2e-127">Minimum supported server</span></span><br/> | <span data-ttu-id="dcb2e-128">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="dcb2e-128">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="dcb2e-129">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="dcb2e-129">Namespace</span></span><br/>                | <span data-ttu-id="dcb2e-130">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="dcb2e-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="dcb2e-131">MOF</span><span class="sxs-lookup"><span data-stu-id="dcb2e-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dcb2e-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dcb2e-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="dcb2e-133">DLL</span><span class="sxs-lookup"><span data-stu-id="dcb2e-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dcb2e-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="dcb2e-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="dcb2e-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dcb2e-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dcb2e-136">**\_Dipendenza CIM**</span><span class="sxs-lookup"><span data-stu-id="dcb2e-136">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

