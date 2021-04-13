---
description: La \_ classe WMI SystemSetting abstract Association di Win32 mette in correlazione un computer e un'impostazione generale del sistema.
ms.assetid: 796ee263-2526-43f8-bd3d-23442b6bd4ca
ms.tgt_platform: multiple
title: Classe Win32_SystemSetting
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemSetting
- Win32_SystemSetting.Element
- Win32_SystemSetting.Setting
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e29b752d769cd347ce1cfdb729bf8c0c3959a4f5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483893"
---
# <a name="win32_systemsetting-class"></a><span data-ttu-id="8d013-103">Win32 \_ SystemSetting (classe)</span><span class="sxs-lookup"><span data-stu-id="8d013-103">Win32\_SystemSetting class</span></span>

<span data-ttu-id="8d013-104">La [classe WMI](../wmisdk/retrieving-a-class.md) **\_ SystemSetting** abstract Association di Win32 mette in correlazione un computer e un'impostazione generale del sistema.</span><span class="sxs-lookup"><span data-stu-id="8d013-104">The **Win32\_SystemSetting** abstract association [WMI class](../wmisdk/retrieving-a-class.md) relates a computer system and a general setting on that system.</span></span>

<span data-ttu-id="8d013-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="8d013-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="8d013-106">Le proprietà e i metodi sono in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="8d013-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d013-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8d013-107">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C501-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemSetting : CIM_ElementSetting
{
  Win32_ComputerSystem REF Element;
  CIM_Setting          REF Setting;
};
```

## <a name="members"></a><span data-ttu-id="8d013-108">Members</span><span class="sxs-lookup"><span data-stu-id="8d013-108">Members</span></span>

<span data-ttu-id="8d013-109">La classe **Win32 \_ SystemSetting** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="8d013-109">The **Win32\_SystemSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="8d013-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="8d013-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8d013-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="8d013-111">Properties</span></span>

<span data-ttu-id="8d013-112">La classe **Win32 \_ SystemSetting** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="8d013-112">The **Win32\_SystemSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8d013-113">**elemento**</span><span class="sxs-lookup"><span data-stu-id="8d013-113">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d013-114">Tipo di dati: **Win32 \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="8d013-114">Data type: **Win32\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="8d013-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8d013-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8d013-116">Qualificatori: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ ComputerSystem")</span><span class="sxs-lookup"><span data-stu-id="8d013-116">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_ComputerSystem")</span></span>
</dt> </dl>

<span data-ttu-id="8d013-117">Riferimento all'istanza di che rappresenta le proprietà di un sistema di computer in cui è possibile applicare questa impostazione.</span><span class="sxs-lookup"><span data-stu-id="8d013-117">Reference to the instance representing the properties of a computer system where this setting can be applied.</span></span>

</dd> <dt>

<span data-ttu-id="8d013-118">**Impostazione**</span><span class="sxs-lookup"><span data-stu-id="8d013-118">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d013-119">Tipo di dati **: \_ impostazione CIM**</span><span class="sxs-lookup"><span data-stu-id="8d013-119">Data type: **CIM\_Setting**</span></span>
</dt> <dt>

<span data-ttu-id="8d013-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8d013-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8d013-121">Qualificatori: [**chiave**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("impostazione"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("impostazione CIM CIM \| \_ ")</span><span class="sxs-lookup"><span data-stu-id="8d013-121">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Setting"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM\|CIM\_Setting")</span></span>
</dt> </dl>

<span data-ttu-id="8d013-122">Riferimento all'istanza di che rappresenta le proprietà dell'impostazione che può essere applicata al sistema del computer.</span><span class="sxs-lookup"><span data-stu-id="8d013-122">Reference to the instance representing the properties of the setting that can be applied to the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8d013-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="8d013-123">Remarks</span></span>

<span data-ttu-id="8d013-124">La classe **Win32 \_ SystemSetting** è derivata da [**CIM \_ ElementSetting**](cim-elementsetting.md).</span><span class="sxs-lookup"><span data-stu-id="8d013-124">The **Win32\_SystemSetting** class is derived from [**CIM\_ElementSetting**](cim-elementsetting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8d013-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8d013-125">Requirements</span></span>



| <span data-ttu-id="8d013-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="8d013-126">Requirement</span></span> | <span data-ttu-id="8d013-127">Valore</span><span class="sxs-lookup"><span data-stu-id="8d013-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8d013-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8d013-128">Minimum supported client</span></span><br/> | <span data-ttu-id="8d013-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8d013-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8d013-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8d013-130">Minimum supported server</span></span><br/> | <span data-ttu-id="8d013-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8d013-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8d013-132">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="8d013-132">Namespace</span></span><br/>                | <span data-ttu-id="8d013-133">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="8d013-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8d013-134">MOF</span><span class="sxs-lookup"><span data-stu-id="8d013-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8d013-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8d013-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8d013-136">DLL</span><span class="sxs-lookup"><span data-stu-id="8d013-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8d013-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8d013-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8d013-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8d013-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d013-139">**\_ELEMENTSETTING CIM**</span><span class="sxs-lookup"><span data-stu-id="8d013-139">**CIM\_ElementSetting**</span></span>](cim-elementsetting.md)
</dt> <dt>

[<span data-ttu-id="8d013-140">Classi del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="8d013-140">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
