---
description: La \_ classe WMI AutochkSetting di Win32 rappresenta le impostazioni per l'operazione di verifica autocontrollo di un disco.
ms.assetid: 637f4d5d-f2f0-4fe0-bbde-7804156979b7
ms.tgt_platform: multiple
title: Classe Win32_AutochkSetting
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_AutochkSetting
- Win32_AutochkSetting.Caption
- Win32_AutochkSetting.Description
- Win32_AutochkSetting.SettingID
- Win32_AutochkSetting.UserInputDelay
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: ea3da60cd4075aa2e36285d30950d3a105d59354
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305174"
---
# <a name="win32_autochksetting-class"></a><span data-ttu-id="52c22-103">Win32 \_ AutochkSetting (classe)</span><span class="sxs-lookup"><span data-stu-id="52c22-103">Win32\_AutochkSetting class</span></span>

<span data-ttu-id="52c22-104">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ AutochkSetting di Win32** rappresenta le impostazioni per l'operazione di verifica autocontrollo di un disco.</span><span class="sxs-lookup"><span data-stu-id="52c22-104">The **Win32\_AutochkSetting** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the settings for the autocheck operation of a disk.</span></span>

<span data-ttu-id="52c22-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="52c22-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="52c22-106">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="52c22-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="52c22-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="52c22-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), SupportsUpdate, AMENDMENT]
class Win32_AutochkSetting : CIM_Setting
{
  string Caption;
  string Description;
  string SettingID;
  uint32 UserInputDelay;
};
```

## <a name="members"></a><span data-ttu-id="52c22-108">Members</span><span class="sxs-lookup"><span data-stu-id="52c22-108">Members</span></span>

<span data-ttu-id="52c22-109">La classe **Win32 \_ AutochkSetting** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="52c22-109">The **Win32\_AutochkSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="52c22-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="52c22-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="52c22-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="52c22-111">Properties</span></span>

<span data-ttu-id="52c22-112">La classe **Win32 \_ AutochkSetting** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="52c22-112">The **Win32\_AutochkSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="52c22-113">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="52c22-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52c22-114">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="52c22-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="52c22-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="52c22-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="52c22-116">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="52c22-116">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="52c22-117">Breve descrizione testuale dell'oggetto corrente.</span><span class="sxs-lookup"><span data-stu-id="52c22-117">Short textual description of the current object.</span></span>

<span data-ttu-id="52c22-118">Questa proprietà viene ereditata [**dall' \_ impostazione CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="52c22-118">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="52c22-119">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="52c22-119">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52c22-120">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="52c22-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="52c22-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="52c22-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="52c22-122">Descrizione testuale dell'oggetto corrente.</span><span class="sxs-lookup"><span data-stu-id="52c22-122">Textual description of the current object.</span></span>

<span data-ttu-id="52c22-123">Questa proprietà viene ereditata [**dall' \_ impostazione CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="52c22-123">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="52c22-124">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="52c22-124">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52c22-125">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="52c22-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="52c22-126">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="52c22-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="52c22-127">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("settingID"), [**chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="52c22-127">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("SettingId"), [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="52c22-128">ID utilizzato come parte di una chiave per l'oggetto corrente.</span><span class="sxs-lookup"><span data-stu-id="52c22-128">An ID that is used as part of a key for the current object.</span></span>

</dd> <dt>

<span data-ttu-id="52c22-129">**UserInputDelay**</span><span class="sxs-lookup"><span data-stu-id="52c22-129">**UserInputDelay**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52c22-130">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="52c22-130">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="52c22-131">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="52c22-131">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="52c22-132">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKLM \\ \\ CurrentControlSet \\ \\ Control \\ \\ Session Manager \| AutoChkTimeOut"), [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("secondi")</span><span class="sxs-lookup"><span data-stu-id="52c22-132">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKLM\\\\CurrentControlSet\\\\Control\\\\Session Manager \| AutoChkTimeOut"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("seconds")</span></span>
</dt> </dl>

<span data-ttu-id="52c22-133">Ritardo di input dell'utente per la verifica.</span><span class="sxs-lookup"><span data-stu-id="52c22-133">The user input delay for autocheck.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="52c22-134">Commenti</span><span class="sxs-lookup"><span data-stu-id="52c22-134">Remarks</span></span>

<span data-ttu-id="52c22-135">La classe **Win32 \_ AutochkSetting** deriva dall' [**\_ impostazione CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="52c22-135">The **Win32\_AutochkSetting** class is derived from [**CIM\_Setting**](cim-setting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="52c22-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="52c22-136">Requirements</span></span>



| <span data-ttu-id="52c22-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="52c22-137">Requirement</span></span> | <span data-ttu-id="52c22-138">Valore</span><span class="sxs-lookup"><span data-stu-id="52c22-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="52c22-139">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="52c22-139">Minimum supported client</span></span><br/> | <span data-ttu-id="52c22-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="52c22-140">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="52c22-141">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="52c22-141">Minimum supported server</span></span><br/> | <span data-ttu-id="52c22-142">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="52c22-142">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="52c22-143">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="52c22-143">Namespace</span></span><br/>                | <span data-ttu-id="52c22-144">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="52c22-144">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="52c22-145">MOF</span><span class="sxs-lookup"><span data-stu-id="52c22-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="52c22-146"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="52c22-146"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="52c22-147">DLL</span><span class="sxs-lookup"><span data-stu-id="52c22-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="52c22-148"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="52c22-148"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="52c22-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="52c22-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52c22-150">**\_Impostazione CIM**</span><span class="sxs-lookup"><span data-stu-id="52c22-150">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> <dt>

[<span data-ttu-id="52c22-151">Classi hardware del sistema del computer</span><span class="sxs-lookup"><span data-stu-id="52c22-151">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

