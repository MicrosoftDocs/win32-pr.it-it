---
description: L' \_ associazione CIM PackageAlarm rappresenta la relazione in cui viene installato un dispositivo di allarme come parte di un pacchetto. L'installazione indica i problemi con l'ambiente del pacchetto&\# 8212, il suo stato di sicurezza o l'integrità generale.
ms.assetid: 4911502a-de9c-46b4-91f6-a042c69fd052
ms.tgt_platform: multiple
title: Classe CIM_PackageAlarm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PackageAlarm
- CIM_PackageAlarm.Dependent
- CIM_PackageAlarm.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 29aae3a2c1093e026356ea7a096f8b673673f67d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126144"
---
# <a name="cim_packagealarm-class"></a><span data-ttu-id="3ed79-104">CIM \_ PackageAlarm (classe)</span><span class="sxs-lookup"><span data-stu-id="3ed79-104">CIM\_PackageAlarm class</span></span>

<span data-ttu-id="3ed79-105">L'associazione [**CIM \_ PackageAlarm**](/windows/desktop/SecCrypto/extendedproperties-newenum) rappresenta la relazione in cui viene installato un dispositivo di allarme come parte di un pacchetto.</span><span class="sxs-lookup"><span data-stu-id="3ed79-105">The [**CIM\_PackageAlarm**](/windows/desktop/SecCrypto/extendedproperties-newenum) association represents the relationship in which an alarm device is installed as part of a package.</span></span> <span data-ttu-id="3ed79-106">L'installazione indica i problemi con l'ambiente del pacchetto, lo stato di sicurezza o l'integrità generale.</span><span class="sxs-lookup"><span data-stu-id="3ed79-106">The installation indicates issues with the package's environment its security state or its overall health.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3ed79-107">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="3ed79-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="3ed79-108">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="3ed79-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="3ed79-109">La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="3ed79-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="3ed79-110">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="3ed79-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ed79-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3ed79-111">Syntax</span></span>

``` syntax
[Abstract, Aggregation, UUID("{FAF76B90-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PackageAlarm : CIM_Dependency
{
  CIM_PhysicalPackage REF Dependent;
  CIM_AlarmDevice     REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="3ed79-112">Members</span><span class="sxs-lookup"><span data-stu-id="3ed79-112">Members</span></span>

<span data-ttu-id="3ed79-113">La classe **CIM \_ PackageAlarm** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="3ed79-113">The **CIM\_PackageAlarm** class has these types of members:</span></span>

-   [<span data-ttu-id="3ed79-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="3ed79-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3ed79-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="3ed79-115">Properties</span></span>

<span data-ttu-id="3ed79-116">La classe **CIM \_ PackageAlarm** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="3ed79-116">The **CIM\_PackageAlarm** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3ed79-117">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="3ed79-117">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ed79-118">Tipo di dati: **CIM \_ AlarmDevice**</span><span class="sxs-lookup"><span data-stu-id="3ed79-118">Data type: **CIM\_AlarmDevice**</span></span>
</dt> <dt>

<span data-ttu-id="3ed79-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3ed79-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ed79-120">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="3ed79-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="3ed79-121">Un [**\_ AlarmDevice CIM**](cim-alarmdevice.md) che descrive il dispositivo di allarme per il pacchetto.</span><span class="sxs-lookup"><span data-stu-id="3ed79-121">A [**CIM\_AlarmDevice**](cim-alarmdevice.md) that describes the alarm device for the package.</span></span>

</dd> <dt>

<span data-ttu-id="3ed79-122">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="3ed79-122">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ed79-123">Tipo di dati: **CIM \_ PhysicalPackage**</span><span class="sxs-lookup"><span data-stu-id="3ed79-123">Data type: **CIM\_PhysicalPackage**</span></span>
</dt> <dt>

<span data-ttu-id="3ed79-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3ed79-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ed79-125">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente")</span><span class="sxs-lookup"><span data-stu-id="3ed79-125">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="3ed79-126">Un [**\_ PhysicalPackage CIM**](cim-physicalpackage.md) che descrive il pacchetto fisico il cui integrità, sicurezza, ambiente e così via sono allarmanti.</span><span class="sxs-lookup"><span data-stu-id="3ed79-126">A [**CIM\_PhysicalPackage**](cim-physicalpackage.md) describing the physical package whose health, security, environment, etc. is alarmed.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3ed79-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="3ed79-127">Remarks</span></span>

<span data-ttu-id="3ed79-128">**CIM \_ PackageAlarm** è derivato dalla [**\_ dipendenza CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="3ed79-128">**CIM\_PackageAlarm** is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="3ed79-129">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="3ed79-129">WMI does not implement this class.</span></span>

<span data-ttu-id="3ed79-130">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="3ed79-130">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="3ed79-131">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="3ed79-131">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="3ed79-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3ed79-132">Requirements</span></span>



| <span data-ttu-id="3ed79-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="3ed79-133">Requirement</span></span> | <span data-ttu-id="3ed79-134">Valore</span><span class="sxs-lookup"><span data-stu-id="3ed79-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3ed79-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3ed79-135">Minimum supported client</span></span><br/> | <span data-ttu-id="3ed79-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3ed79-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3ed79-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3ed79-137">Minimum supported server</span></span><br/> | <span data-ttu-id="3ed79-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3ed79-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3ed79-139">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="3ed79-139">Namespace</span></span><br/>                | <span data-ttu-id="3ed79-140">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="3ed79-140">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3ed79-141">MOF</span><span class="sxs-lookup"><span data-stu-id="3ed79-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3ed79-142"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3ed79-142"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3ed79-143">DLL</span><span class="sxs-lookup"><span data-stu-id="3ed79-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3ed79-144"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3ed79-144"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3ed79-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3ed79-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ed79-146">**\_Dipendenza CIM**</span><span class="sxs-lookup"><span data-stu-id="3ed79-146">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

