---
description: La \_ classe WMI COMApplicationClasses abstract Association di Win32 mette in correlazione un componente Component Object Model (com) e l'applicazione com in cui risiede.
ms.assetid: 7c188199-86fb-45ba-b318-9d9529b831b8
ms.tgt_platform: multiple
title: Classe Win32_COMApplicationClasses
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_COMApplicationClasses
- Win32_COMApplicationClasses.PartComponent
- Win32_COMApplicationClasses.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 01413128f7457049a4383c1148938e2136645337
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127347"
---
# <a name="win32_comapplicationclasses-class"></a><span data-ttu-id="dec3f-103">Win32 \_ COMApplicationClasses (classe)</span><span class="sxs-lookup"><span data-stu-id="dec3f-103">Win32\_COMApplicationClasses class</span></span>

<span data-ttu-id="dec3f-104">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ COMApplicationClasses** abstract Association di Win32 mette in correlazione un componente Component Object Model (COM) e l'applicazione com in cui risiede.</span><span class="sxs-lookup"><span data-stu-id="dec3f-104">The **Win32\_COMApplicationClasses** abstract association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a Component Object Model (COM) component and the COM application where it resides.</span></span>

<span data-ttu-id="dec3f-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="dec3f-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="dec3f-106">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="dec3f-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="dec3f-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dec3f-107">Syntax</span></span>

``` syntax
[abstract, UUID("{0F73ED51-8ED9-11d2-B340-00105A1F8569}"), AMENDMENT]
class Win32_COMApplicationClasses : CIM_Component
{
  Win32_COMClass       REF PartComponent;
  Win32_COMApplication REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="dec3f-108">Members</span><span class="sxs-lookup"><span data-stu-id="dec3f-108">Members</span></span>

<span data-ttu-id="dec3f-109">La classe **Win32 \_ COMApplicationClasses** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="dec3f-109">The **Win32\_COMApplicationClasses** class has these types of members:</span></span>

-   [<span data-ttu-id="dec3f-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="dec3f-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="dec3f-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="dec3f-111">Properties</span></span>

<span data-ttu-id="dec3f-112">La classe **Win32 \_ COMApplicationClasses** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="dec3f-112">The **Win32\_COMApplicationClasses** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="dec3f-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="dec3f-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dec3f-114">Tipo di dati **: \_ comApplicazione Win32**</span><span class="sxs-lookup"><span data-stu-id="dec3f-114">Data type: **Win32\_COMApplication**</span></span>
</dt> <dt>

<span data-ttu-id="dec3f-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dec3f-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dec3f-116">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ comapplication")</span><span class="sxs-lookup"><span data-stu-id="dec3f-116">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_COMApplication")</span></span>
</dt> </dl>

<span data-ttu-id="dec3f-117">[**ComApplicazione \_ Win32**](win32-comapplication.md) che rappresenta l'applicazione com contenente il componente com.</span><span class="sxs-lookup"><span data-stu-id="dec3f-117">A [**Win32\_COMApplication**](win32-comapplication.md) that represents the COM application containing the COM component.</span></span>

</dd> <dt>

<span data-ttu-id="dec3f-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="dec3f-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dec3f-119">Tipo di dati **: \_ Comclasse Win32**</span><span class="sxs-lookup"><span data-stu-id="dec3f-119">Data type: **Win32\_COMClass**</span></span>
</dt> <dt>

<span data-ttu-id="dec3f-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dec3f-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dec3f-121">Qualificatori: [**chiave**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| classe Win32 di WMI \_ ")</span><span class="sxs-lookup"><span data-stu-id="dec3f-121">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_COMClass")</span></span>
</dt> </dl>

<span data-ttu-id="dec3f-122">[**Comclasse \_ Win32**](win32-comclass.md) che rappresenta il componente com raggruppato nell'applicazione com.</span><span class="sxs-lookup"><span data-stu-id="dec3f-122">A [**Win32\_COMClass**](win32-comclass.md) that represents the COM component grouped under the COM application.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dec3f-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="dec3f-123">Remarks</span></span>

<span data-ttu-id="dec3f-124">La classe **Win32 \_ COMApplicationClasses** è derivata dal [**\_ componente CIM**](cim-component.md).</span><span class="sxs-lookup"><span data-stu-id="dec3f-124">The **Win32\_COMApplicationClasses** class is derived from [**CIM\_Component**](cim-component.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="dec3f-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dec3f-125">Requirements</span></span>



| <span data-ttu-id="dec3f-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="dec3f-126">Requirement</span></span> | <span data-ttu-id="dec3f-127">Valore</span><span class="sxs-lookup"><span data-stu-id="dec3f-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dec3f-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dec3f-128">Minimum supported client</span></span><br/> | <span data-ttu-id="dec3f-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="dec3f-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="dec3f-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dec3f-130">Minimum supported server</span></span><br/> | <span data-ttu-id="dec3f-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dec3f-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="dec3f-132">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="dec3f-132">Namespace</span></span><br/>                | <span data-ttu-id="dec3f-133">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="dec3f-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="dec3f-134">MOF</span><span class="sxs-lookup"><span data-stu-id="dec3f-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dec3f-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dec3f-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="dec3f-136">DLL</span><span class="sxs-lookup"><span data-stu-id="dec3f-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dec3f-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dec3f-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dec3f-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dec3f-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dec3f-139">**\_Componente CIM**</span><span class="sxs-lookup"><span data-stu-id="dec3f-139">**CIM\_Component**</span></span>](cim-component.md)
</dt> <dt>

<span data-ttu-id="dec3f-140">[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="dec3f-140">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

