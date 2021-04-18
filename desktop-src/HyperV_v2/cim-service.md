---
description: Rappresenta un elemento logico che contiene informazioni per rappresentare e gestire la funzionalità fornita da una funzionalità del dispositivo o software.
ms.assetid: 0b2312da-433b-43d8-8d21-babab12a5b2c
title: Classe CIM_Service (gestione Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Service
- CIM_Service.SystemCreationClassName
- CIM_Service.SystemName
- CIM_Service.CreationClassName
- CIM_Service.Name
- CIM_Service.PrimaryOwnerName
- CIM_Service.PrimaryOwnerContact
- CIM_Service.StartMode
- CIM_Service.Started
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b6ee3c51b6af50d77e94bb0a29bd1c8148cda8f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307766"
---
# <a name="cim_service-class-hyper-v-management"></a><span data-ttu-id="4412b-103">Classe CIM_Service (gestione Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="4412b-103">CIM_Service class (Hyper-V management)</span></span>

<span data-ttu-id="4412b-104">Rappresenta un elemento logico che contiene informazioni per rappresentare e gestire la funzionalità fornita da una funzionalità del dispositivo o software.</span><span class="sxs-lookup"><span data-stu-id="4412b-104">Represents a logical element that contains information to represent and manage the functionality provided by a device or software feature.</span></span> <span data-ttu-id="4412b-105">Un servizio è un oggetto generico per la configurazione e la gestione dell'implementazione di funzionalità. non si tratta della funzionalità stessa.</span><span class="sxs-lookup"><span data-stu-id="4412b-105">A service is a general-purpose object to configure and manage the implementation of functionality; it is not the functionality itself.</span></span>

## <a name="syntax"></a><span data-ttu-id="4412b-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4412b-106">Syntax</span></span>

``` syntax
[Abstract, Version("2.14.0"), UMLPackagePath("CIM::Core::Service"), AMENDMENT]
class CIM_Service : CIM_EnabledLogicalElement
{
  string  SystemCreationClassName;
  string  SystemName;
  string  CreationClassName;
  string  Name;
  string  PrimaryOwnerName;
  string  PrimaryOwnerContact;
  string  StartMode;
  boolean Started;
};
```

## <a name="members"></a><span data-ttu-id="4412b-107">Members</span><span class="sxs-lookup"><span data-stu-id="4412b-107">Members</span></span>

<span data-ttu-id="4412b-108">La classe del **\_ servizio CIM** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="4412b-108">The **CIM\_Service** class has these types of members:</span></span>

-   [<span data-ttu-id="4412b-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="4412b-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="4412b-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="4412b-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="4412b-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="4412b-111">Methods</span></span>

<span data-ttu-id="4412b-112">La classe del **\_ servizio CIM** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="4412b-112">The **CIM\_Service** class has these methods.</span></span>



| <span data-ttu-id="4412b-113">Metodo</span><span class="sxs-lookup"><span data-stu-id="4412b-113">Method</span></span>                                           | <span data-ttu-id="4412b-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4412b-114">Description</span></span>                    |
|:-------------------------------------------------|:-------------------------------|
| [<span data-ttu-id="4412b-115">**StartService**</span><span class="sxs-lookup"><span data-stu-id="4412b-115">**StartService**</span></span>](cim-service-startservice.md) | <span data-ttu-id="4412b-116">avvia il servizio.</span><span class="sxs-lookup"><span data-stu-id="4412b-116">Starts the service.</span></span><br/> |
| [<span data-ttu-id="4412b-117">**StopService**</span><span class="sxs-lookup"><span data-stu-id="4412b-117">**StopService**</span></span>](cim-service-stopservice.md)   | <span data-ttu-id="4412b-118">arresta il servizio.</span><span class="sxs-lookup"><span data-stu-id="4412b-118">Stops the service.</span></span><br/>  |



 

### <a name="properties"></a><span data-ttu-id="4412b-119">Proprietà</span><span class="sxs-lookup"><span data-stu-id="4412b-119">Properties</span></span>

<span data-ttu-id="4412b-120">La classe del **\_ servizio CIM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="4412b-120">The **CIM\_Service** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4412b-121">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="4412b-121">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4412b-122">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="4412b-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4412b-123">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4412b-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4412b-124">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="4412b-124">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="4412b-125">Nome della classe utilizzato per creare un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="4412b-125">The class name used to create an instance of this class.</span></span> <span data-ttu-id="4412b-126">**CreationClassName** è combinato con altre proprietà chiave di questa classe per identificare in modo univoco le istanze di questa classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="4412b-126">**CreationClassName** is combined with other key properties of this class to uniquely identify instances of this class and its subclasses.</span></span>

</dd> <dt>

<span data-ttu-id="4412b-127">**Nome**</span><span class="sxs-lookup"><span data-stu-id="4412b-127">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4412b-128">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="4412b-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4412b-129">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4412b-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4412b-130">Qualificatori: [**chiave**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="4412b-130">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="4412b-131">Identificatore univoco del servizio che indica la funzionalità del servizio.</span><span class="sxs-lookup"><span data-stu-id="4412b-131">A unique identifier of the service that indicates the functionality of the service.</span></span>

</dd> <dt>

<span data-ttu-id="4412b-132">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="4412b-132">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4412b-133">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="4412b-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4412b-134">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="4412b-134">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="4412b-135">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| informazioni generali \| 001,4 ")</span><span class="sxs-lookup"><span data-stu-id="4412b-135">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|General Information\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="4412b-136">Informazioni di contatto per il proprietario principale del servizio.</span><span class="sxs-lookup"><span data-stu-id="4412b-136">Contact information for the primary owner of the service.</span></span>

</dd> <dt>

<span data-ttu-id="4412b-137">**PrimaryOwnerName**</span><span class="sxs-lookup"><span data-stu-id="4412b-137">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4412b-138">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="4412b-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4412b-139">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="4412b-139">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="4412b-140">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| informazioni generali \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="4412b-140">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|General Information\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="4412b-141">Nome del proprietario primario del servizio.</span><span class="sxs-lookup"><span data-stu-id="4412b-141">The name of the primary owner of the service.</span></span>

</dd> <dt>

<span data-ttu-id="4412b-142">**Avviato**</span><span class="sxs-lookup"><span data-stu-id="4412b-142">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4412b-143">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="4412b-143">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4412b-144">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4412b-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4412b-145">**true** se il servizio è stato avviato. in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="4412b-145">**true** if the service has been started; otherwise, **false**.</span></span>

</dd> <dt>

<span data-ttu-id="4412b-146">**Modalità avvio**</span><span class="sxs-lookup"><span data-stu-id="4412b-146">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4412b-147">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="4412b-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4412b-148">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4412b-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4412b-149">Qualificatori: [**deprecato**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("**\_ servizio CIM**.**EnabledDefault**"), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="4412b-149">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("**CIM\_Service**.**EnabledDefault**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="4412b-150">Questa proprietà è deprecata.</span><span class="sxs-lookup"><span data-stu-id="4412b-150">This property is deprecated.</span></span> <span data-ttu-id="4412b-151">Usare invece la proprietà **EnabledDefault** ereditata da [**CIM \_ EnabledLogicalElement**](cim-enabledlogicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="4412b-151">Instead, use the **EnabledDefault** property that is inherited from [**CIM\_EnabledLogicalElement**](cim-enabledlogicalelement.md).</span></span>

> [!Note]  
> <span data-ttu-id="4412b-152">Deprecated Description: indica se il servizio viene avviato automaticamente, ad esempio da un sistema operativo, oppure è stato avviato solo su richiesta.</span><span class="sxs-lookup"><span data-stu-id="4412b-152">Deprecated description: Indicates whether the service is automatically started (for example, by an operating system) or only started upon request.</span></span>

 

<dt>



 <span data-ttu-id="4412b-153">("Automatico")</span><span class="sxs-lookup"><span data-stu-id="4412b-153">("Automatic")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="4412b-154">("Manuale")</span><span class="sxs-lookup"><span data-stu-id="4412b-154">("Manual")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4412b-155">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="4412b-155">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4412b-156">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="4412b-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4412b-157">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4412b-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4412b-158">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**CreationClassName**")</span><span class="sxs-lookup"><span data-stu-id="4412b-158">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**")</span></span>
</dt> </dl>

<span data-ttu-id="4412b-159">Nome della classe utilizzato per creare un'istanza del sistema che contiene il servizio.</span><span class="sxs-lookup"><span data-stu-id="4412b-159">The class name used to create an instance of the system that contains the service.</span></span> <span data-ttu-id="4412b-160">**SystemCreationClassName** è combinato con altre proprietà chiave di questa classe per identificare in modo univoco le istanze di questa classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="4412b-160">**SystemCreationClassName** is combined with other key properties of this class to uniquely identify instances of this class and its subclasses.</span></span>

</dd> <dt>

<span data-ttu-id="4412b-161">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="4412b-161">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4412b-162">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="4412b-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4412b-163">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4412b-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4412b-164">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**Nome**")</span><span class="sxs-lookup"><span data-stu-id="4412b-164">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**")</span></span>
</dt> </dl>

<span data-ttu-id="4412b-165">Nome del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="4412b-165">The name of the scoping system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4412b-166">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4412b-166">Requirements</span></span>



| <span data-ttu-id="4412b-167">Requisito</span><span class="sxs-lookup"><span data-stu-id="4412b-167">Requirement</span></span> | <span data-ttu-id="4412b-168">Valore</span><span class="sxs-lookup"><span data-stu-id="4412b-168">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4412b-169">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4412b-169">Minimum supported client</span></span><br/> | <span data-ttu-id="4412b-170">Windows 8</span><span class="sxs-lookup"><span data-stu-id="4412b-170">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="4412b-171">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4412b-171">Minimum supported server</span></span><br/> | <span data-ttu-id="4412b-172">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4412b-172">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="4412b-173">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="4412b-173">Namespace</span></span><br/>                | <span data-ttu-id="4412b-174">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="4412b-174">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="4412b-175">MOF</span><span class="sxs-lookup"><span data-stu-id="4412b-175">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4412b-176"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4412b-176"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4412b-177">DLL</span><span class="sxs-lookup"><span data-stu-id="4412b-177">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4412b-178"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4412b-178"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="4412b-179">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4412b-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4412b-180">**\_ENABLEDLOGICALELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="4412b-180">**CIM\_EnabledLogicalElement**</span></span>](cim-enabledlogicalelement.md)
</dt> </dl>

 

