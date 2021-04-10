---
description: La \_ classe WMI dell'associazione COMApplicationSettings Win32 mette in correlazione un'applicazione DCOM e le relative impostazioni di configurazione.
ms.assetid: b08eaff1-b42a-42f3-abf7-3664b6195acd
ms.tgt_platform: multiple
title: Classe Win32_COMApplicationSettings
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_COMApplicationSettings
- Win32_COMApplicationSettings.Setting
- Win32_COMApplicationSettings.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8f2fd5953d770d541e704b7dc7fe8580e98b3066
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225547"
---
# <a name="win32_comapplicationsettings-class"></a><span data-ttu-id="9293c-103">Win32 \_ COMApplicationSettings (classe)</span><span class="sxs-lookup"><span data-stu-id="9293c-103">Win32\_COMApplicationSettings class</span></span>

<span data-ttu-id="9293c-104">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) dell'associazione **\_ COMApplicationSettings Win32** mette in correlazione un'applicazione DCOM e le relative impostazioni di configurazione.</span><span class="sxs-lookup"><span data-stu-id="9293c-104">The **Win32\_COMApplicationSettings** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a DCOM application and its configuration settings.</span></span>

<span data-ttu-id="9293c-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="9293c-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="9293c-106">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="9293c-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="9293c-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9293c-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{E5D8A563-F6C0-11d2-B35E-00105A1F8569}"), AMENDMENT]
class Win32_COMApplicationSettings : CIM_ElementSetting
{
  Win32_DCOMApplicationSetting REF Setting;
  Win32_DCOMApplication        REF Element;
};
```

## <a name="members"></a><span data-ttu-id="9293c-108">Members</span><span class="sxs-lookup"><span data-stu-id="9293c-108">Members</span></span>

<span data-ttu-id="9293c-109">La classe **Win32 \_ COMApplicationSettings** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="9293c-109">The **Win32\_COMApplicationSettings** class has these types of members:</span></span>

-   [<span data-ttu-id="9293c-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="9293c-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9293c-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="9293c-111">Properties</span></span>

<span data-ttu-id="9293c-112">La classe **Win32 \_ COMApplicationSettings** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="9293c-112">The **Win32\_COMApplicationSettings** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9293c-113">**elemento**</span><span class="sxs-lookup"><span data-stu-id="9293c-113">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9293c-114">Tipo di dati: **Win32 \_ DCOMApplication**</span><span class="sxs-lookup"><span data-stu-id="9293c-114">Data type: **Win32\_DCOMApplication**</span></span>
</dt> <dt>

<span data-ttu-id="9293c-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9293c-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9293c-116">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("element"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ DCOMApplication")</span><span class="sxs-lookup"><span data-stu-id="9293c-116">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Element"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_DCOMApplication")</span></span>
</dt> </dl>

<span data-ttu-id="9293c-117">[**\_ DCOMApplication Win32**](win32-dcomapplication.md) che rappresenta l'applicazione DCOM A cui vengono applicate le impostazioni.</span><span class="sxs-lookup"><span data-stu-id="9293c-117">A [**Win32\_DCOMApplication**](win32-dcomapplication.md) that represents the DCOM application where the settings are applied.</span></span>

</dd> <dt>

<span data-ttu-id="9293c-118">**Impostazione**</span><span class="sxs-lookup"><span data-stu-id="9293c-118">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9293c-119">Tipo di dati: **Win32 \_ DCOMApplicationSetting**</span><span class="sxs-lookup"><span data-stu-id="9293c-119">Data type: **Win32\_DCOMApplicationSetting**</span></span>
</dt> <dt>

<span data-ttu-id="9293c-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9293c-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9293c-121">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("setting"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ DCOMApplicationSetting")</span><span class="sxs-lookup"><span data-stu-id="9293c-121">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Setting"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_DCOMApplicationSetting")</span></span>
</dt> </dl>

<span data-ttu-id="9293c-122">[**\_ DCOMApplicationSetting Win32**](win32-dcomapplicationsetting.md) che rappresenta le impostazioni di configurazione associate all'applicazione DCOM.</span><span class="sxs-lookup"><span data-stu-id="9293c-122">A [**Win32\_DCOMApplicationSetting**](win32-dcomapplicationsetting.md) that represents the configuration settings associated with the DCOM application.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9293c-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="9293c-123">Remarks</span></span>

<span data-ttu-id="9293c-124">La classe **Win32 \_ COMApplicationSettings** è derivata da [**CIM \_ ElementSetting**](cim-elementsetting.md).</span><span class="sxs-lookup"><span data-stu-id="9293c-124">The **Win32\_COMApplicationSettings** class is derived from [**CIM\_ElementSetting**](cim-elementsetting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9293c-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9293c-125">Requirements</span></span>



| <span data-ttu-id="9293c-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="9293c-126">Requirement</span></span> | <span data-ttu-id="9293c-127">Valore</span><span class="sxs-lookup"><span data-stu-id="9293c-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9293c-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9293c-128">Minimum supported client</span></span><br/> | <span data-ttu-id="9293c-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9293c-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9293c-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9293c-130">Minimum supported server</span></span><br/> | <span data-ttu-id="9293c-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9293c-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9293c-132">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="9293c-132">Namespace</span></span><br/>                | <span data-ttu-id="9293c-133">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="9293c-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9293c-134">MOF</span><span class="sxs-lookup"><span data-stu-id="9293c-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9293c-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9293c-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9293c-136">DLL</span><span class="sxs-lookup"><span data-stu-id="9293c-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9293c-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9293c-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9293c-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9293c-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9293c-139">**\_ELEMENTSETTING CIM**</span><span class="sxs-lookup"><span data-stu-id="9293c-139">**CIM\_ElementSetting**</span></span>](cim-elementsetting.md)
</dt> <dt>

<span data-ttu-id="9293c-140">[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9293c-140">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

