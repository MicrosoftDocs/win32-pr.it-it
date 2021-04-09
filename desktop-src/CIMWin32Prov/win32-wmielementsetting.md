---
description: La \_ classe WMI dell'associazione WMIElementSetting Win32 mette in relazione un servizio in esecuzione nel sistema Windows e le impostazioni WMI che può utilizzare.
ms.assetid: 00e9f882-5f54-4042-a916-2f90ed9a37c0
ms.tgt_platform: multiple
title: Classe Win32_WMIElementSetting
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_WMIElementSetting
- Win32_WMIElementSetting.Element
- Win32_WMIElementSetting.Setting
api_type:
- DllExport
api_location:
- Wbemcore.dll
ms.openlocfilehash: 41f79614fd0931759d502bbd61c7f4143e9e7dc9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877330"
---
# <a name="win32_wmielementsetting-class"></a><span data-ttu-id="d247c-103">Win32 \_ WMIElementSetting (classe)</span><span class="sxs-lookup"><span data-stu-id="d247c-103">Win32\_WMIElementSetting class</span></span>

<span data-ttu-id="d247c-104">La [classe WMI](../wmisdk/retrieving-a-class.md) dell'associazione **\_ WMIElementSetting Win32** mette in relazione un servizio in esecuzione nel sistema Windows e le impostazioni WMI che può utilizzare.</span><span class="sxs-lookup"><span data-stu-id="d247c-104">The **Win32\_WMIElementSetting** association [WMI class](../wmisdk/retrieving-a-class.md) relates a service running in the Windows system and the WMI settings it can use.</span></span>

<span data-ttu-id="d247c-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="d247c-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="d247c-106">Le proprietà e i metodi sono in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="d247c-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="d247c-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d247c-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("WBEMCORE"), UUID("{A83EF167-CA8D-11d2-B33D-00104BCC4B4A}"), AMENDMENT]
class Win32_WMIElementSetting : CIM_ElementSetting
{
  Win32_Service    REF Element;
  Win32_WMISetting REF Setting;
};
```

## <a name="members"></a><span data-ttu-id="d247c-108">Members</span><span class="sxs-lookup"><span data-stu-id="d247c-108">Members</span></span>

<span data-ttu-id="d247c-109">La classe **Win32 \_ WMIElementSetting** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="d247c-109">The **Win32\_WMIElementSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="d247c-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d247c-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d247c-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d247c-111">Properties</span></span>

<span data-ttu-id="d247c-112">La classe **Win32 \_ WMIElementSetting** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="d247c-112">The **Win32\_WMIElementSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d247c-113">**elemento**</span><span class="sxs-lookup"><span data-stu-id="d247c-113">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d247c-114">Tipo di dati **: \_ servizio Win32**</span><span class="sxs-lookup"><span data-stu-id="d247c-114">Data type: **Win32\_Service**</span></span>
</dt> <dt>

<span data-ttu-id="d247c-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d247c-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d247c-116">Qualificatori: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ Service")</span><span class="sxs-lookup"><span data-stu-id="d247c-116">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_Service")</span></span>
</dt> </dl>

<span data-ttu-id="d247c-117">Riferimento all'istanza di che rappresenta il servizio Windows utilizzando o le proprietà WMI di emersione.</span><span class="sxs-lookup"><span data-stu-id="d247c-117">Reference to the instance representing the Windows service using or surfacing WMI properties.</span></span>

</dd> <dt>

<span data-ttu-id="d247c-118">**Impostazione**</span><span class="sxs-lookup"><span data-stu-id="d247c-118">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d247c-119">Tipo di dati: **Win32 \_ WMISetting**</span><span class="sxs-lookup"><span data-stu-id="d247c-119">Data type: **Win32\_WMISetting**</span></span>
</dt> <dt>

<span data-ttu-id="d247c-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d247c-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d247c-121">Qualificatori: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("setting"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ WMISetting")</span><span class="sxs-lookup"><span data-stu-id="d247c-121">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Setting"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_WMISetting")</span></span>
</dt> </dl>

<span data-ttu-id="d247c-122">Riferimento all'istanza di che rappresenta le impostazioni WMI disponibili per il servizio Windows.</span><span class="sxs-lookup"><span data-stu-id="d247c-122">Reference to the instance representing the WMI settings available to the Windows service.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d247c-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="d247c-123">Remarks</span></span>

<span data-ttu-id="d247c-124">La classe **Win32 \_ WMIElementSetting** è derivata da [**CIM \_ ElementSetting**](cim-elementsetting.md).</span><span class="sxs-lookup"><span data-stu-id="d247c-124">The **Win32\_WMIElementSetting** class is derived from [**CIM\_ElementSetting**](cim-elementsetting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d247c-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d247c-125">Requirements</span></span>



| <span data-ttu-id="d247c-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="d247c-126">Requirement</span></span> | <span data-ttu-id="d247c-127">Valore</span><span class="sxs-lookup"><span data-stu-id="d247c-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d247c-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d247c-128">Minimum supported client</span></span><br/> | <span data-ttu-id="d247c-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d247c-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d247c-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d247c-130">Minimum supported server</span></span><br/> | <span data-ttu-id="d247c-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d247c-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d247c-132">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="d247c-132">Namespace</span></span><br/>                | <span data-ttu-id="d247c-133">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="d247c-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d247c-134">MOF</span><span class="sxs-lookup"><span data-stu-id="d247c-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d247c-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d247c-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d247c-136">DLL</span><span class="sxs-lookup"><span data-stu-id="d247c-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d247c-137"><dt>Wbemcore.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d247c-137"><dt>Wbemcore.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d247c-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d247c-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d247c-139">**\_ELEMENTSETTING CIM**</span><span class="sxs-lookup"><span data-stu-id="d247c-139">**CIM\_ElementSetting**</span></span>](cim-elementsetting.md)
</dt> <dt>

[<span data-ttu-id="d247c-140">Classi di gestione del servizio WMI</span><span class="sxs-lookup"><span data-stu-id="d247c-140">WMI Service Management Classes</span></span>](./wmi-service-management-classes.md)
</dt> </dl>

 

 
