---
description: La \_ classe WMI dell'associazione ClassicCOMApplicationClasses Win32 mette in correlazione un'applicazione com e un componente com raggruppati sotto di esso.
ms.assetid: 77f24461-9ca0-4fc3-8728-4a4b9a1edbc3
ms.tgt_platform: multiple
title: Classe Win32_ClassicCOMApplicationClasses
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ClassicCOMApplicationClasses
- Win32_ClassicCOMApplicationClasses.PartComponent
- Win32_ClassicCOMApplicationClasses.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: dfd451c1c5d4819f1ec1d21f890b207a06d6fb82
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878162"
---
# <a name="win32_classiccomapplicationclasses-class"></a><span data-ttu-id="1e5ce-103">Win32 \_ ClassicCOMApplicationClasses (classe)</span><span class="sxs-lookup"><span data-stu-id="1e5ce-103">Win32\_ClassicCOMApplicationClasses class</span></span>

<span data-ttu-id="1e5ce-104">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) dell'associazione **\_ ClassicCOMApplicationClasses Win32** mette in correlazione un'applicazione com e un componente com raggruppati sotto di esso.</span><span class="sxs-lookup"><span data-stu-id="1e5ce-104">The **Win32\_ClassicCOMApplicationClasses** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a COM application and a COM component grouped under it.</span></span>

<span data-ttu-id="1e5ce-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="1e5ce-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="1e5ce-106">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="1e5ce-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e5ce-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1e5ce-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{0F73ED54-8ED9-11d2-B340-00105A1F8569}"), AMENDMENT]
class Win32_ClassicCOMApplicationClasses : Win32_COMApplicationClasses
{
  Win32_ClassicCOMClass REF PartComponent;
  Win32_DCOMApplication REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="1e5ce-108">Members</span><span class="sxs-lookup"><span data-stu-id="1e5ce-108">Members</span></span>

<span data-ttu-id="1e5ce-109">La classe **Win32 \_ ClassicCOMApplicationClasses** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="1e5ce-109">The **Win32\_ClassicCOMApplicationClasses** class has these types of members:</span></span>

-   [<span data-ttu-id="1e5ce-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="1e5ce-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1e5ce-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="1e5ce-111">Properties</span></span>

<span data-ttu-id="1e5ce-112">La classe **Win32 \_ ClassicCOMApplicationClasses** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="1e5ce-112">The **Win32\_ClassicCOMApplicationClasses** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1e5ce-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="1e5ce-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e5ce-114">Tipo di dati: **Win32 \_ DCOMApplication**</span><span class="sxs-lookup"><span data-stu-id="1e5ce-114">Data type: **Win32\_DCOMApplication**</span></span>
</dt> <dt>

<span data-ttu-id="1e5ce-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1e5ce-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1e5ce-116">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ DCOMApplication")</span><span class="sxs-lookup"><span data-stu-id="1e5ce-116">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_DCOMApplication")</span></span>
</dt> </dl>

<span data-ttu-id="1e5ce-117">[**\_ DCOMApplication Win32**](win32-dcomapplication.md) che rappresenta un'applicazione DCOM che contiene o usa il componente com.</span><span class="sxs-lookup"><span data-stu-id="1e5ce-117">A [**Win32\_DCOMApplication**](win32-dcomapplication.md) that represents a DCOM application containing or using the COM component.</span></span>

</dd> <dt>

<span data-ttu-id="1e5ce-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="1e5ce-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e5ce-119">Tipo di dati: **Win32 \_ ClassicCOMClass**</span><span class="sxs-lookup"><span data-stu-id="1e5ce-119">Data type: **Win32\_ClassicCOMClass**</span></span>
</dt> <dt>

<span data-ttu-id="1e5ce-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1e5ce-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1e5ce-121">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ ClassicCOMClass")</span><span class="sxs-lookup"><span data-stu-id="1e5ce-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_ClassicCOMClass")</span></span>
</dt> </dl>

<span data-ttu-id="1e5ce-122">[**\_ ClassicCOMClass Win32**](win32-classiccomclass.md) che rappresenta il componente COM esistente o utilizzato dall'applicazione DCOM.</span><span class="sxs-lookup"><span data-stu-id="1e5ce-122">A [**Win32\_ClassicCOMClass**](win32-classiccomclass.md) that represents the COM component existing in or used by the DCOM application.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1e5ce-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="1e5ce-123">Remarks</span></span>

<span data-ttu-id="1e5ce-124">La classe **Win32 \_ ClassicCOMApplicationClasses** è derivata da [**Win32 \_ COMApplicationClasses**](win32-comapplicationclasses.md).</span><span class="sxs-lookup"><span data-stu-id="1e5ce-124">The **Win32\_ClassicCOMApplicationClasses** class is derived from [**Win32\_COMApplicationClasses**](win32-comapplicationclasses.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1e5ce-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1e5ce-125">Requirements</span></span>



| <span data-ttu-id="1e5ce-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="1e5ce-126">Requirement</span></span> | <span data-ttu-id="1e5ce-127">Valore</span><span class="sxs-lookup"><span data-stu-id="1e5ce-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1e5ce-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1e5ce-128">Minimum supported client</span></span><br/> | <span data-ttu-id="1e5ce-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1e5ce-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1e5ce-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1e5ce-130">Minimum supported server</span></span><br/> | <span data-ttu-id="1e5ce-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1e5ce-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1e5ce-132">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="1e5ce-132">Namespace</span></span><br/>                | <span data-ttu-id="1e5ce-133">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="1e5ce-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1e5ce-134">MOF</span><span class="sxs-lookup"><span data-stu-id="1e5ce-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1e5ce-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1e5ce-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1e5ce-136">DLL</span><span class="sxs-lookup"><span data-stu-id="1e5ce-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1e5ce-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1e5ce-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e5ce-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1e5ce-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e5ce-139">**\_COMApplicationClasses Win32**</span><span class="sxs-lookup"><span data-stu-id="1e5ce-139">**Win32\_COMApplicationClasses**</span></span>](win32-comapplicationclasses.md)
</dt> <dt>

<span data-ttu-id="1e5ce-140">[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1e5ce-140">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

