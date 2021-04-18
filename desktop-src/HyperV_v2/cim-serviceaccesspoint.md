---
description: Rappresenta un punto di accesso al servizio (SAP), che è in grado di utilizzare o richiamare un servizio. SAP indica che un servizio è disponibile per l'utilizzo da altre entità.
ms.assetid: 09349c95-3f7e-46c5-bea1-c3d14ee16a2a
title: Classe CIM_ServiceAccessPoint (gestione Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ServiceAccessPoint
- CIM_ServiceAccessPoint.SystemCreationClassName
- CIM_ServiceAccessPoint.SystemName
- CIM_ServiceAccessPoint.CreationClassName
- CIM_ServiceAccessPoint.Name
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e3e27fc667c55cd101b06a34f9140cb9eed8923f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307765"
---
# <a name="cim_serviceaccesspoint-class-hyper-v-management"></a><span data-ttu-id="8e2a7-104">Classe CIM_ServiceAccessPoint (gestione Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="8e2a7-104">CIM_ServiceAccessPoint class (Hyper-V management)</span></span>

<span data-ttu-id="8e2a7-105">Rappresenta un punto di accesso al servizio (SAP), che è in grado di utilizzare o richiamare un servizio.</span><span class="sxs-lookup"><span data-stu-id="8e2a7-105">Represents a service access point (SAP), which is able to utilize or invoke a service.</span></span> <span data-ttu-id="8e2a7-106">SAP indica che un servizio è disponibile per l'utilizzo da altre entità.</span><span class="sxs-lookup"><span data-stu-id="8e2a7-106">SAPs indicate that a service is available for other entities to use.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e2a7-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8e2a7-107">Syntax</span></span>

``` syntax
[Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::Service"), AMENDMENT]
class CIM_ServiceAccessPoint : CIM_EnabledLogicalElement
{
  string SystemCreationClassName;
  string SystemName;
  string CreationClassName;
  string Name;
};
```

## <a name="members"></a><span data-ttu-id="8e2a7-108">Members</span><span class="sxs-lookup"><span data-stu-id="8e2a7-108">Members</span></span>

<span data-ttu-id="8e2a7-109">La classe **CIM \_ serviceAccessPoint** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="8e2a7-109">The **CIM\_ServiceAccessPoint** class has these types of members:</span></span>

-   [<span data-ttu-id="8e2a7-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="8e2a7-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8e2a7-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="8e2a7-111">Properties</span></span>

<span data-ttu-id="8e2a7-112">La classe **CIM \_ serviceAccessPoint** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="8e2a7-112">The **CIM\_ServiceAccessPoint** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8e2a7-113">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="8e2a7-113">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e2a7-114">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="8e2a7-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e2a7-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8e2a7-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e2a7-116">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="8e2a7-116">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="8e2a7-117">Nome della classe utilizzato per creare un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="8e2a7-117">The class name used to create an instance of this class.</span></span> <span data-ttu-id="8e2a7-118">**CreationClassName** è combinato con altre proprietà chiave di questa classe per identificare in modo univoco le istanze di questa classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="8e2a7-118">**CreationClassName** is combined with other key properties of this class to uniquely identify instances of this class and its subclasses.</span></span>

</dd> <dt>

<span data-ttu-id="8e2a7-119">**Nome**</span><span class="sxs-lookup"><span data-stu-id="8e2a7-119">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e2a7-120">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="8e2a7-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e2a7-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8e2a7-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e2a7-122">Qualificatori: [**chiave**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="8e2a7-122">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="8e2a7-123">Nome univoco del SAP che indica le funzionalità supportate da SAP.</span><span class="sxs-lookup"><span data-stu-id="8e2a7-123">The unique name of the SAP that indicates the features supported by the SAP.</span></span>

</dd> <dt>

<span data-ttu-id="8e2a7-124">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="8e2a7-124">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e2a7-125">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="8e2a7-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e2a7-126">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8e2a7-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e2a7-127">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**CreationClassName**")</span><span class="sxs-lookup"><span data-stu-id="8e2a7-127">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**")</span></span>
</dt> </dl>

<span data-ttu-id="8e2a7-128">Nome della classe utilizzato per creare un'istanza del sistema che contiene SAP.</span><span class="sxs-lookup"><span data-stu-id="8e2a7-128">The class name used to create an instance of the system that contains the SAP.</span></span> <span data-ttu-id="8e2a7-129">**SystemCreationClassName** è combinato con altre proprietà chiave di questa classe per identificare in modo univoco le istanze di questa classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="8e2a7-129">**SystemCreationClassName** is combined with other key properties of this class to uniquely identify instances of this class and its subclasses.</span></span>

</dd> <dt>

<span data-ttu-id="8e2a7-130">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="8e2a7-130">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e2a7-131">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="8e2a7-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e2a7-132">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8e2a7-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e2a7-133">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**Nome**")</span><span class="sxs-lookup"><span data-stu-id="8e2a7-133">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**")</span></span>
</dt> </dl>

<span data-ttu-id="8e2a7-134">Nome del sistema che contiene SAP.</span><span class="sxs-lookup"><span data-stu-id="8e2a7-134">The name of the system that contains the SAP.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8e2a7-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8e2a7-135">Requirements</span></span>



| <span data-ttu-id="8e2a7-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="8e2a7-136">Requirement</span></span> | <span data-ttu-id="8e2a7-137">Valore</span><span class="sxs-lookup"><span data-stu-id="8e2a7-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e2a7-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8e2a7-138">Minimum supported client</span></span><br/> | <span data-ttu-id="8e2a7-139">Windows 8</span><span class="sxs-lookup"><span data-stu-id="8e2a7-139">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="8e2a7-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8e2a7-140">Minimum supported server</span></span><br/> | <span data-ttu-id="8e2a7-141">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8e2a7-141">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="8e2a7-142">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="8e2a7-142">Namespace</span></span><br/>                | <span data-ttu-id="8e2a7-143">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="8e2a7-143">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="8e2a7-144">MOF</span><span class="sxs-lookup"><span data-stu-id="8e2a7-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8e2a7-145"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8e2a7-145"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="8e2a7-146">DLL</span><span class="sxs-lookup"><span data-stu-id="8e2a7-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8e2a7-147"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8e2a7-147"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="8e2a7-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8e2a7-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e2a7-149">**\_ENABLEDLOGICALELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="8e2a7-149">**CIM\_EnabledLogicalElement**</span></span>](cim-enabledlogicalelement.md)
</dt> </dl>

 

