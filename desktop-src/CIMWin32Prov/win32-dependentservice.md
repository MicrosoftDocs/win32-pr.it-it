---
description: La \_ classe WMI dell'associazione DependentService Win32 mette in relazione due servizi di base interdipendenti.
ms.assetid: ba21fce3-f8f9-4886-b09d-a9e830376364
ms.tgt_platform: multiple
title: Classe Win32_DependentService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DependentService
- Win32_DependentService.TypeOfDependency
- Win32_DependentService.Antecedent
- Win32_DependentService.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 047ec3411186f09f3d0e76da27158aa8ee91d4cc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127723"
---
# <a name="win32_dependentservice-class"></a><span data-ttu-id="b8f41-103">Win32 \_ DependentService (classe)</span><span class="sxs-lookup"><span data-stu-id="b8f41-103">Win32\_DependentService class</span></span>

<span data-ttu-id="b8f41-104">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) dell'associazione **\_ DependentService Win32** mette in relazione due servizi di base interdipendenti.</span><span class="sxs-lookup"><span data-stu-id="b8f41-104">The **Win32\_DependentService** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates two interdependent base services.</span></span>

<span data-ttu-id="b8f41-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="b8f41-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="b8f41-106">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="b8f41-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8f41-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b8f41-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4FA-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_DependentService : CIM_ServiceServiceDependency
{
  uint16                TypeOfDependency;
  Win32_BaseService REF Antecedent;
  Win32_BaseService REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="b8f41-108">Members</span><span class="sxs-lookup"><span data-stu-id="b8f41-108">Members</span></span>

<span data-ttu-id="b8f41-109">La classe **Win32 \_ DependentService** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="b8f41-109">The **Win32\_DependentService** class has these types of members:</span></span>

-   [<span data-ttu-id="b8f41-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b8f41-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b8f41-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b8f41-111">Properties</span></span>

<span data-ttu-id="b8f41-112">La classe **Win32 \_ DependentService** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="b8f41-112">The **Win32\_DependentService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b8f41-113">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="b8f41-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8f41-114">Tipo di dati: **Win32 \_ BaseService**</span><span class="sxs-lookup"><span data-stu-id="b8f41-114">Data type: **Win32\_BaseService**</span></span>
</dt> <dt>

<span data-ttu-id="b8f41-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b8f41-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8f41-116">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| WMI \_ Win32 BaseService")</span><span class="sxs-lookup"><span data-stu-id="b8f41-116">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_BaseService")</span></span>
</dt> </dl>

<span data-ttu-id="b8f41-117">[**\_ BaseService Win32**](win32-baseservice.md) che rappresenta il servizio di base basato sulla proprietà **dipendente** della classe.</span><span class="sxs-lookup"><span data-stu-id="b8f41-117">A [**Win32\_BaseService**](win32-baseservice.md) representing the base service relied upon by the **Dependent** property of this class.</span></span>

</dd> <dt>

<span data-ttu-id="b8f41-118">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="b8f41-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8f41-119">Tipo di dati: **Win32 \_ BaseService**</span><span class="sxs-lookup"><span data-stu-id="b8f41-119">Data type: **Win32\_BaseService**</span></span>
</dt> <dt>

<span data-ttu-id="b8f41-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b8f41-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8f41-121">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ BaseService")</span><span class="sxs-lookup"><span data-stu-id="b8f41-121">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_BaseService")</span></span>
</dt> </dl>

<span data-ttu-id="b8f41-122">[**\_ BaseService Win32**](win32-baseservice.md) che rappresenta il servizio di base che dipende dalla proprietà **precedente** di questa classe.</span><span class="sxs-lookup"><span data-stu-id="b8f41-122">A [**Win32\_BaseService**](win32-baseservice.md) representing the base service that is dependent on the **Antecedent** property of this class.</span></span>

</dd> <dt>

<span data-ttu-id="b8f41-123">**TypeOfDependency**</span><span class="sxs-lookup"><span data-stu-id="b8f41-123">**TypeOfDependency**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8f41-124">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b8f41-124">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b8f41-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b8f41-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8f41-126">Natura della dipendenza da servizio a servizio.</span><span class="sxs-lookup"><span data-stu-id="b8f41-126">Nature of the service-to-service dependency.</span></span> <span data-ttu-id="b8f41-127">Questa proprietà indica che il servizio associato deve essere stato completato, deve essere avviato o non deve essere avviato per il funzionamento del servizio.</span><span class="sxs-lookup"><span data-stu-id="b8f41-127">This property indicates that the associated service must have completed, must be started, or must not be started for the service to function.</span></span>

<span data-ttu-id="b8f41-128">Questa proprietà viene ereditata da [**CIM \_ ServiceServiceDependency**](cim-serviceservicedependency.md).</span><span class="sxs-lookup"><span data-stu-id="b8f41-128">This property is inherited from [**CIM\_ServiceServiceDependency**](cim-serviceservicedependency.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b8f41-129"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="b8f41-129"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="b8f41-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="b8f41-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_Must_Have_Completed"></span><span id="service_must_have_completed"></span><span id="SERVICE_MUST_HAVE_COMPLETED"></span>

<span data-ttu-id="b8f41-131"><span id="Service_Must_Have_Completed"></span><span id="service_must_have_completed"></span><span id="SERVICE_MUST_HAVE_COMPLETED"></span>Il **servizio deve essere stato completato** (2)</span><span class="sxs-lookup"><span data-stu-id="b8f41-131"><span id="Service_Must_Have_Completed"></span><span id="service_must_have_completed"></span><span id="SERVICE_MUST_HAVE_COMPLETED"></span>**Service Must Have Completed** (2)</span></span>


</dt> <dd>

<span data-ttu-id="b8f41-132">Il servizio deve essere stato completato.</span><span class="sxs-lookup"><span data-stu-id="b8f41-132">Service must have completed.</span></span>

</dd> <dt>

<span id="Service_Must_Be_Started"></span><span id="service_must_be_started"></span><span id="SERVICE_MUST_BE_STARTED"></span>

<span data-ttu-id="b8f41-133"><span id="Service_Must_Be_Started"></span><span id="service_must_be_started"></span><span id="SERVICE_MUST_BE_STARTED"></span>Il **servizio deve essere avviato** (3)</span><span class="sxs-lookup"><span data-stu-id="b8f41-133"><span id="Service_Must_Be_Started"></span><span id="service_must_be_started"></span><span id="SERVICE_MUST_BE_STARTED"></span>**Service Must Be Started** (3)</span></span>


</dt> <dd>

<span data-ttu-id="b8f41-134">Il servizio deve essere avviato.</span><span class="sxs-lookup"><span data-stu-id="b8f41-134">Service must be started.</span></span>

</dd> <dt>

<span id="Service_Must_Not_Be_Started"></span><span id="service_must_not_be_started"></span><span id="SERVICE_MUST_NOT_BE_STARTED"></span>

<span data-ttu-id="b8f41-135"><span id="Service_Must_Not_Be_Started"></span><span id="service_must_not_be_started"></span><span id="SERVICE_MUST_NOT_BE_STARTED"></span>Il **servizio non deve essere avviato** (4)</span><span class="sxs-lookup"><span data-stu-id="b8f41-135"><span id="Service_Must_Not_Be_Started"></span><span id="service_must_not_be_started"></span><span id="SERVICE_MUST_NOT_BE_STARTED"></span>**Service Must Not Be Started** (4)</span></span>


</dt> <dd>

<span data-ttu-id="b8f41-136">Il servizio non deve essere avviato.</span><span class="sxs-lookup"><span data-stu-id="b8f41-136">Service must not be started.</span></span>

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b8f41-137">Commenti</span><span class="sxs-lookup"><span data-stu-id="b8f41-137">Remarks</span></span>

<span data-ttu-id="b8f41-138">La classe **Win32 \_ DependentService** è derivata da [**CIM \_ ServiceServiceDependency**](cim-serviceservicedependency.md).</span><span class="sxs-lookup"><span data-stu-id="b8f41-138">The **Win32\_DependentService** class is derived from [**CIM\_ServiceServiceDependency**](cim-serviceservicedependency.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b8f41-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b8f41-139">Requirements</span></span>



| <span data-ttu-id="b8f41-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="b8f41-140">Requirement</span></span> | <span data-ttu-id="b8f41-141">Valore</span><span class="sxs-lookup"><span data-stu-id="b8f41-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b8f41-142">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b8f41-142">Minimum supported client</span></span><br/> | <span data-ttu-id="b8f41-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b8f41-143">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b8f41-144">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b8f41-144">Minimum supported server</span></span><br/> | <span data-ttu-id="b8f41-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b8f41-145">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b8f41-146">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b8f41-146">Namespace</span></span><br/>                | <span data-ttu-id="b8f41-147">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="b8f41-147">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b8f41-148">MOF</span><span class="sxs-lookup"><span data-stu-id="b8f41-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b8f41-149"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b8f41-149"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b8f41-150">DLL</span><span class="sxs-lookup"><span data-stu-id="b8f41-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b8f41-151"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b8f41-151"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8f41-152">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b8f41-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8f41-153">**\_SERVICESERVICEDEPENDENCY CIM**</span><span class="sxs-lookup"><span data-stu-id="b8f41-153">**CIM\_ServiceServiceDependency**</span></span>](cim-serviceservicedependency.md)
</dt> <dt>

<span data-ttu-id="b8f41-154">[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b8f41-154">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

