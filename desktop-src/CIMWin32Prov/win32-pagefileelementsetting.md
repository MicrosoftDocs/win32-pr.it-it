---
description: La \_ classe WMI dell'associazione PageFileElementSetting Win32 mette in relazione le impostazioni iniziali di un file di paging e lo stato di tali impostazioni durante il normale utilizzo.
ms.assetid: efc1f20d-166e-4e27-9767-f6ec0bbd6c14
ms.tgt_platform: multiple
title: Classe Win32_PageFileElementSetting
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PageFileElementSetting
- Win32_PageFileElementSetting.Element
- Win32_PageFileElementSetting.Setting
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: dfc1087225894cef2895cf41af5e5297769a4041
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966291"
---
# <a name="win32_pagefileelementsetting-class"></a><span data-ttu-id="5c78b-103">Win32 \_ PageFileElementSetting (classe)</span><span class="sxs-lookup"><span data-stu-id="5c78b-103">Win32\_PageFileElementSetting class</span></span>

<span data-ttu-id="5c78b-104">La [classe WMI](../wmisdk/retrieving-a-class.md) dell'associazione **\_ PageFileElementSetting Win32** mette in relazione le impostazioni iniziali di un file di paging e lo stato di tali impostazioni durante il normale utilizzo.</span><span class="sxs-lookup"><span data-stu-id="5c78b-104">The **Win32\_PageFileElementSetting** association [WMI class](../wmisdk/retrieving-a-class.md) relates the initial settings of a page file and the state of those settings during normal use.</span></span>

<span data-ttu-id="5c78b-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="5c78b-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="5c78b-106">Le proprietà e i metodi sono in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="5c78b-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c78b-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5c78b-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8E7F70E8-C856-11D2-B364-00105A1F77A1}"), AMENDMENT]
class Win32_PageFileElementSetting : CIM_ElementSetting
{
  Win32_PageFileUsage   REF Element;
  Win32_PageFileSetting REF Setting;
};
```

## <a name="members"></a><span data-ttu-id="5c78b-108">Members</span><span class="sxs-lookup"><span data-stu-id="5c78b-108">Members</span></span>

<span data-ttu-id="5c78b-109">La classe **Win32 \_ PageFileElementSetting** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="5c78b-109">The **Win32\_PageFileElementSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="5c78b-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5c78b-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5c78b-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5c78b-111">Properties</span></span>

<span data-ttu-id="5c78b-112">La classe **Win32 \_ PageFileElementSetting** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="5c78b-112">The **Win32\_PageFileElementSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5c78b-113">**elemento**</span><span class="sxs-lookup"><span data-stu-id="5c78b-113">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c78b-114">Tipo di dati: **Win32 \_ PageFileUsage**</span><span class="sxs-lookup"><span data-stu-id="5c78b-114">Data type: **Win32\_PageFileUsage**</span></span>
</dt> <dt>

<span data-ttu-id="5c78b-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5c78b-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5c78b-116">Qualificatori: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ PageFileUsage")</span><span class="sxs-lookup"><span data-stu-id="5c78b-116">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_PageFileUsage")</span></span>
</dt> </dl>

<span data-ttu-id="5c78b-117">Riferimento all'istanza di che rappresenta le proprietà di un file di paging mentre il sistema Win32 è in uso.</span><span class="sxs-lookup"><span data-stu-id="5c78b-117">Reference to the instance representing the properties of a page file while the Win32 system is in use.</span></span>

</dd> <dt>

<span data-ttu-id="5c78b-118">**Impostazione**</span><span class="sxs-lookup"><span data-stu-id="5c78b-118">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c78b-119">Tipo di dati: **Win32 \_ PageFileSetting**</span><span class="sxs-lookup"><span data-stu-id="5c78b-119">Data type: **Win32\_PageFileSetting**</span></span>
</dt> <dt>

<span data-ttu-id="5c78b-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5c78b-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5c78b-121">Qualificatori: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("setting"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ PageFileSetting")</span><span class="sxs-lookup"><span data-stu-id="5c78b-121">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Setting"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_PageFileSetting")</span></span>
</dt> </dl>

<span data-ttu-id="5c78b-122">Riferimento all'istanza di che rappresenta le impostazioni iniziali di un file di paging all'avvio del sistema Win32.</span><span class="sxs-lookup"><span data-stu-id="5c78b-122">Reference to the instance representing the initial settings of a page file when the Win32 system is starting up.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5c78b-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="5c78b-123">Remarks</span></span>

<span data-ttu-id="5c78b-124">La classe **Win32 \_ PageFileElementSetting** è derivata da [**CIM \_ ElementSetting**](cim-elementsetting.md).</span><span class="sxs-lookup"><span data-stu-id="5c78b-124">The **Win32\_PageFileElementSetting** class is derived from [**CIM\_ElementSetting**](cim-elementsetting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5c78b-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5c78b-125">Requirements</span></span>



| <span data-ttu-id="5c78b-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="5c78b-126">Requirement</span></span> | <span data-ttu-id="5c78b-127">Valore</span><span class="sxs-lookup"><span data-stu-id="5c78b-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5c78b-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5c78b-128">Minimum supported client</span></span><br/> | <span data-ttu-id="5c78b-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5c78b-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5c78b-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5c78b-130">Minimum supported server</span></span><br/> | <span data-ttu-id="5c78b-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5c78b-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5c78b-132">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="5c78b-132">Namespace</span></span><br/>                | <span data-ttu-id="5c78b-133">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="5c78b-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5c78b-134">MOF</span><span class="sxs-lookup"><span data-stu-id="5c78b-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5c78b-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5c78b-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5c78b-136">DLL</span><span class="sxs-lookup"><span data-stu-id="5c78b-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5c78b-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5c78b-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c78b-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5c78b-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c78b-139">**\_ELEMENTSETTING CIM**</span><span class="sxs-lookup"><span data-stu-id="5c78b-139">**CIM\_ElementSetting**</span></span>](cim-elementsetting.md)
</dt> <dt>

[<span data-ttu-id="5c78b-140">Classi del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="5c78b-140">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
