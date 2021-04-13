---
description: La \_ classe WMI astratta Comimpostazioni Win32 rappresenta le impostazioni associate a un componente Component Object Model (com) o a un'applicazione com.
ms.assetid: e8cdbee8-41ab-4aff-b17b-707667138411
ms.tgt_platform: multiple
title: Classe Win32_COMSetting
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_COMSetting
- Win32_COMSetting.Caption
- Win32_COMSetting.Description
- Win32_COMSetting.SettingID
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5ec7932117d1ff0bc058d2b9a131f77ff9e040bf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225570"
---
# <a name="win32_comsetting-class"></a><span data-ttu-id="1d1f9-103">\_Classe comsetting Win32</span><span class="sxs-lookup"><span data-stu-id="1d1f9-103">Win32\_COMSetting class</span></span>

<span data-ttu-id="1d1f9-104">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) astratta **\_ comimpostazioni Win32** rappresenta le impostazioni associate a un componente Component Object Model (com) o a un'applicazione com.</span><span class="sxs-lookup"><span data-stu-id="1d1f9-104">The **Win32\_COMSetting** abstract [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the settings associated with a Component Object Model (COM) component or COM application.</span></span>

<span data-ttu-id="1d1f9-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="1d1f9-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="1d1f9-106">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="1d1f9-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d1f9-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1d1f9-107">Syntax</span></span>

``` syntax
[abstract, UUID("{E5D8A560-F6C0-11d2-B35E-00105A1F8569}"), AMENDMENT]
class Win32_COMSetting : CIM_Setting
{
  string Caption;
  string Description;
  string SettingID;
};
```

## <a name="members"></a><span data-ttu-id="1d1f9-108">Members</span><span class="sxs-lookup"><span data-stu-id="1d1f9-108">Members</span></span>

<span data-ttu-id="1d1f9-109">La **classe \_ comsetting Win32** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="1d1f9-109">The **Win32\_COMSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="1d1f9-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="1d1f9-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1d1f9-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="1d1f9-111">Properties</span></span>

<span data-ttu-id="1d1f9-112">La **classe \_ comsetting Win32** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="1d1f9-112">The **Win32\_COMSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1d1f9-113">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="1d1f9-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d1f9-114">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1d1f9-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d1f9-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1d1f9-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d1f9-116">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="1d1f9-116">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="1d1f9-117">Breve descrizione testuale dell'oggetto corrente.</span><span class="sxs-lookup"><span data-stu-id="1d1f9-117">Short textual description of the current object.</span></span>

<span data-ttu-id="1d1f9-118">Questa proprietà viene ereditata [**dall' \_ impostazione CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="1d1f9-118">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="1d1f9-119">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="1d1f9-119">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d1f9-120">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1d1f9-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d1f9-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1d1f9-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d1f9-122">Descrizione testuale dell'oggetto corrente.</span><span class="sxs-lookup"><span data-stu-id="1d1f9-122">Textual description of the current object.</span></span>

<span data-ttu-id="1d1f9-123">Questa proprietà viene ereditata [**dall' \_ impostazione CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="1d1f9-123">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="1d1f9-124">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="1d1f9-124">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d1f9-125">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1d1f9-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d1f9-126">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1d1f9-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d1f9-127">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="1d1f9-127">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="1d1f9-128">Identificatore con cui è noto l'oggetto corrente.</span><span class="sxs-lookup"><span data-stu-id="1d1f9-128">Identifier by which the current object is known.</span></span>

<span data-ttu-id="1d1f9-129">Questa proprietà viene ereditata [**dall' \_ impostazione CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="1d1f9-129">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1d1f9-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="1d1f9-130">Remarks</span></span>

<span data-ttu-id="1d1f9-131">La **classe \_ comsetting Win32** deriva dall' [**\_ impostazione CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="1d1f9-131">The **Win32\_COMSetting** class is derived from [**CIM\_Setting**](cim-setting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1d1f9-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1d1f9-132">Requirements</span></span>



| <span data-ttu-id="1d1f9-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="1d1f9-133">Requirement</span></span> | <span data-ttu-id="1d1f9-134">Valore</span><span class="sxs-lookup"><span data-stu-id="1d1f9-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1d1f9-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1d1f9-135">Minimum supported client</span></span><br/> | <span data-ttu-id="1d1f9-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1d1f9-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1d1f9-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1d1f9-137">Minimum supported server</span></span><br/> | <span data-ttu-id="1d1f9-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1d1f9-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1d1f9-139">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="1d1f9-139">Namespace</span></span><br/>                | <span data-ttu-id="1d1f9-140">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="1d1f9-140">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1d1f9-141">MOF</span><span class="sxs-lookup"><span data-stu-id="1d1f9-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1d1f9-142"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1d1f9-142"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1d1f9-143">DLL</span><span class="sxs-lookup"><span data-stu-id="1d1f9-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1d1f9-144"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1d1f9-144"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d1f9-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1d1f9-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d1f9-146">**\_Impostazione CIM**</span><span class="sxs-lookup"><span data-stu-id="1d1f9-146">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> <dt>

<span data-ttu-id="1d1f9-147">[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1d1f9-147">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

