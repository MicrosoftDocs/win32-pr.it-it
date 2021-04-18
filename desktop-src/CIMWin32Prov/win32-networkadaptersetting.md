---
description: La \_ classe WMI dell'associazione NetworkAdapterSetting Win32 mette in correlazione una scheda di rete e le relative impostazioni di configurazione.
ms.assetid: 6fc646c3-05f9-4c92-8598-07ea20fffaca
ms.tgt_platform: multiple
title: Classe Win32_NetworkAdapterSetting
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterSetting
- Win32_NetworkAdapterSetting.Setting
- Win32_NetworkAdapterSetting.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: c51ef9ed790c902a6a662dc3ebc45df97fa29721
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305165"
---
# <a name="win32_networkadaptersetting-class"></a><span data-ttu-id="79e76-103">Win32 \_ NetworkAdapterSetting (classe)</span><span class="sxs-lookup"><span data-stu-id="79e76-103">Win32\_NetworkAdapterSetting class</span></span>

<span data-ttu-id="79e76-104">La [classe WMI](../wmisdk/retrieving-a-class.md) dell'associazione **\_ NetworkAdapterSetting Win32** mette in correlazione una scheda di rete e le relative impostazioni di configurazione.</span><span class="sxs-lookup"><span data-stu-id="79e76-104">The **Win32\_NetworkAdapterSetting** association [WMI class](../wmisdk/retrieving-a-class.md) relates a network adapter and its configuration settings.</span></span>

<span data-ttu-id="79e76-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="79e76-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="79e76-106">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="79e76-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="79e76-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="79e76-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C50A-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_NetworkAdapterSetting : Win32_DeviceSettings
{
  Win32_NetworkAdapterConfiguration REF Setting;
  Win32_NetworkAdapter              REF Element;
};
```

## <a name="members"></a><span data-ttu-id="79e76-108">Members</span><span class="sxs-lookup"><span data-stu-id="79e76-108">Members</span></span>

<span data-ttu-id="79e76-109">La classe **Win32 \_ NetworkAdapterSetting** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="79e76-109">The **Win32\_NetworkAdapterSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="79e76-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="79e76-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="79e76-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="79e76-111">Properties</span></span>

<span data-ttu-id="79e76-112">La classe **Win32 \_ NetworkAdapterSetting** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="79e76-112">The **Win32\_NetworkAdapterSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="79e76-113">**elemento**</span><span class="sxs-lookup"><span data-stu-id="79e76-113">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79e76-114">Tipo di dati: **Win32 \_ NetworkAdapter**</span><span class="sxs-lookup"><span data-stu-id="79e76-114">Data type: **Win32\_NetworkAdapter**</span></span>
</dt> <dt>

<span data-ttu-id="79e76-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="79e76-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79e76-116">Qualificatori: [**override**](../wmisdk/standard-qualifiers.md) ("element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ NetworkAdapter")</span><span class="sxs-lookup"><span data-stu-id="79e76-116">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_NetworkAdapter")</span></span>
</dt> </dl>

<span data-ttu-id="79e76-117">[**\_ NetworkAdapter Win32**](win32-networkadapter.md) che descrive le proprietà della scheda di rete che utilizza una particolare impostazione della scheda di rete.</span><span class="sxs-lookup"><span data-stu-id="79e76-117">A [**Win32\_NetworkAdapter**](win32-networkadapter.md) that describes the properties of the network adapter that is using a particular network adapter setting.</span></span>

</dd> <dt>

<span data-ttu-id="79e76-118">**Impostazione**</span><span class="sxs-lookup"><span data-stu-id="79e76-118">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79e76-119">Tipo di dati: **Win32 \_ NetworkAdapterConfiguration**</span><span class="sxs-lookup"><span data-stu-id="79e76-119">Data type: **Win32\_NetworkAdapterConfiguration**</span></span>
</dt> <dt>

<span data-ttu-id="79e76-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="79e76-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79e76-121">Qualificatori: [**override**](../wmisdk/standard-qualifiers.md) ("setting"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ NetworkAdapterConfiguration")</span><span class="sxs-lookup"><span data-stu-id="79e76-121">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Setting"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_NetworkAdapterConfiguration")</span></span>
</dt> </dl>

<span data-ttu-id="79e76-122">[**\_ NetworkAdapterConfiguration Win32**](win32-networkadapterconfiguration.md) che descrive le impostazioni di configurazione utilizzate nella scheda di rete.</span><span class="sxs-lookup"><span data-stu-id="79e76-122">A [**Win32\_NetworkAdapterConfiguration**](win32-networkadapterconfiguration.md) that describes the configuration settings used on the network adapter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="79e76-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="79e76-123">Remarks</span></span>

<span data-ttu-id="79e76-124">La classe **Win32 \_ NetworkAdapterSetting** è derivata da [**Win32 \_ DeviceSettings**](win32-devicesettings.md).</span><span class="sxs-lookup"><span data-stu-id="79e76-124">The **Win32\_NetworkAdapterSetting** class is derived from [**Win32\_DeviceSettings**](win32-devicesettings.md).</span></span>

<span data-ttu-id="79e76-125">Per informazioni sull'utilizzo delle classi di associazione, vedere [ASSOCIATORS of Statement](../wmisdk/associators-of-statement.md).</span><span class="sxs-lookup"><span data-stu-id="79e76-125">For information on how to use association classes, see [ASSOCIATORS OF Statement](../wmisdk/associators-of-statement.md).</span></span>

## <a name="examples"></a><span data-ttu-id="79e76-126">Esempio</span><span class="sxs-lookup"><span data-stu-id="79e76-126">Examples</span></span>

<span data-ttu-id="79e76-127">Nell'esempio VBScript seguente viene usato **Win32 \_ NetworkAdapterSetting** per identificare l'indirizzo IP nella connessione alla rete locale.</span><span class="sxs-lookup"><span data-stu-id="79e76-127">The following VBScript sample uses **Win32\_NetworkAdapterSetting** to identify the IP Address on the Local Area Connection.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject( _
    "winmgmts:\\" & strComputer & "\root\cimv2")
Set colNics = objWMIService.ExecQuery _
    ("Select * From Win32_NetworkAdapter " _
        & "Where NetConnectionID = " & _
        "'Local Area Connection'")
 
For Each objNic in colNics
    Set colNicConfigs = objWMIService.ExecQuery _
      ("ASSOCIATORS OF " _
          & "{Win32_NetworkAdapter.DeviceID='" & _
      objNic.DeviceID & "'}" & _
      " WHERE AssocClass=Win32_NetworkAdapterSetting")
    For Each objNicConfig In colNicConfigs
        For Each strIPAddress in objNicConfig.IPAddress
            Wscript.Echo "IP Address: " &  strIPAddress
        Next
    Next
Next
```



## <a name="requirements"></a><span data-ttu-id="79e76-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="79e76-128">Requirements</span></span>



| <span data-ttu-id="79e76-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="79e76-129">Requirement</span></span> | <span data-ttu-id="79e76-130">Valore</span><span class="sxs-lookup"><span data-stu-id="79e76-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="79e76-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="79e76-131">Minimum supported client</span></span><br/> | <span data-ttu-id="79e76-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="79e76-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="79e76-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="79e76-133">Minimum supported server</span></span><br/> | <span data-ttu-id="79e76-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="79e76-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="79e76-135">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="79e76-135">Namespace</span></span><br/>                | <span data-ttu-id="79e76-136">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="79e76-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="79e76-137">MOF</span><span class="sxs-lookup"><span data-stu-id="79e76-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="79e76-138"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="79e76-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="79e76-139">DLL</span><span class="sxs-lookup"><span data-stu-id="79e76-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="79e76-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="79e76-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79e76-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="79e76-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79e76-142">**\_DeviceSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="79e76-142">**Win32\_DeviceSettings**</span></span>](win32-devicesettings.md)
</dt> <dt>

[<span data-ttu-id="79e76-143">Classi hardware del sistema del computer</span><span class="sxs-lookup"><span data-stu-id="79e76-143">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="79e76-144">Attività WMI: rete</span><span class="sxs-lookup"><span data-stu-id="79e76-144">WMI Tasks: Networking</span></span>](../wmisdk/wmi-tasks--networking.md)
</dt> </dl>

 

 
