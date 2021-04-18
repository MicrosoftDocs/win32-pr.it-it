---
description: Rappresenta un'associazione in cui un \_ oggetto CIM serviceAccessPoint richiede servizi di protocollo da un \_ oggetto CIM ProtocolEndpoint.
ms.assetid: d1ef774d-f0e0-43e7-8a9d-63c2fad5ca4a
title: Classe CIM_BindsTo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BindsTo
- CIM_BindsTo.Antecedent
- CIM_BindsTo.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ae32bd10d1e7d1944519fe8fb039453989c165fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313868"
---
# <a name="cim_bindsto-class"></a><span data-ttu-id="48a55-103">CIM \_ BindsTo (classe)</span><span class="sxs-lookup"><span data-stu-id="48a55-103">CIM\_BindsTo class</span></span>

<span data-ttu-id="48a55-104">Rappresenta un'associazione in cui un oggetto [**CIM \_ serviceAccessPoint**](cim-serviceaccesspoint.md) richiede servizi di protocollo da un oggetto [**CIM \_ ProtocolEndpoint**](cim-protocolendpoint.md) .</span><span class="sxs-lookup"><span data-stu-id="48a55-104">Represents an association where a [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md) object requests protocol services from a [**CIM\_ProtocolEndpoint**](cim-protocolendpoint.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="48a55-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="48a55-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::Service"), AMENDMENT]
class CIM_BindsTo : CIM_SAPSAPDependency
{
  CIM_ProtocolEndpoint   REF Antecedent;
  CIM_ServiceAccessPoint REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="48a55-106">Members</span><span class="sxs-lookup"><span data-stu-id="48a55-106">Members</span></span>

<span data-ttu-id="48a55-107">La classe **CIM \_ BindsTo** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="48a55-107">The **CIM\_BindsTo** class has these types of members:</span></span>

-   [<span data-ttu-id="48a55-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="48a55-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="48a55-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="48a55-109">Properties</span></span>

<span data-ttu-id="48a55-110">La classe **CIM \_ BindsTo** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="48a55-110">The **CIM\_BindsTo** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="48a55-111">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="48a55-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48a55-112">Tipo di dati: **CIM \_ ProtocolEndpoint**</span><span class="sxs-lookup"><span data-stu-id="48a55-112">Data type: **CIM\_ProtocolEndpoint**</span></span>
</dt> <dt>

<span data-ttu-id="48a55-113">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="48a55-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48a55-114">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="48a55-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="48a55-115">Endpoint di livello inferiore a cui si accede dal punto di accesso al servizio.</span><span class="sxs-lookup"><span data-stu-id="48a55-115">The lower level endpoint that is accessed by the service access point.</span></span>

</dd> <dt>

<span data-ttu-id="48a55-116">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="48a55-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48a55-117">Tipo di dati: **CIM \_ serviceAccessPoint**</span><span class="sxs-lookup"><span data-stu-id="48a55-117">Data type: **CIM\_ServiceAccessPoint**</span></span>
</dt> <dt>

<span data-ttu-id="48a55-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="48a55-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48a55-119">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente")</span><span class="sxs-lookup"><span data-stu-id="48a55-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="48a55-120">Endpoint del protocollo o del punto di accesso dipendente dall'endpoint di livello inferiore.</span><span class="sxs-lookup"><span data-stu-id="48a55-120">The access point or protocol endpoint that is dependent on the lower level endpoint.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="48a55-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="48a55-121">Requirements</span></span>



| <span data-ttu-id="48a55-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="48a55-122">Requirement</span></span> | <span data-ttu-id="48a55-123">Valore</span><span class="sxs-lookup"><span data-stu-id="48a55-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="48a55-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="48a55-124">Minimum supported client</span></span><br/> | <span data-ttu-id="48a55-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="48a55-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="48a55-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="48a55-126">Minimum supported server</span></span><br/> | <span data-ttu-id="48a55-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="48a55-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="48a55-128">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="48a55-128">Namespace</span></span><br/>                | <span data-ttu-id="48a55-129">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="48a55-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="48a55-130">MOF</span><span class="sxs-lookup"><span data-stu-id="48a55-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="48a55-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="48a55-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="48a55-132">DLL</span><span class="sxs-lookup"><span data-stu-id="48a55-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="48a55-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="48a55-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="48a55-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="48a55-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48a55-135">**\_SAPSAPDEPENDENCY CIM**</span><span class="sxs-lookup"><span data-stu-id="48a55-135">**CIM\_SAPSAPDependency**</span></span>](cim-sapsapdependency.md)
</dt> </dl>

 

