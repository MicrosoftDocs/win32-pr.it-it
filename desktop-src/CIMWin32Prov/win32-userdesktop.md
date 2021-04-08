---
description: La \_ classe WMI dell'associazione UserDesktop Win32 mette in correlazione un account utente e le impostazioni desktop specifiche.
ms.assetid: 5ea83ad6-bd0a-4c16-85b2-e3e61ef05903
ms.tgt_platform: multiple
title: Classe Win32_UserDesktop
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_UserDesktop
- Win32_UserDesktop.Element
- Win32_UserDesktop.Setting
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 39b45ee7859fea9f1068123041a87309cf40c2d2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877466"
---
# <a name="win32_userdesktop-class"></a><span data-ttu-id="873da-103">Win32 \_ UserDesktop (classe)</span><span class="sxs-lookup"><span data-stu-id="873da-103">Win32\_UserDesktop class</span></span>

<span data-ttu-id="873da-104">La [classe WMI](../wmisdk/retrieving-a-class.md) dell'associazione **\_ UserDesktop Win32** mette in correlazione un account utente e le impostazioni desktop specifiche.</span><span class="sxs-lookup"><span data-stu-id="873da-104">The **Win32\_UserDesktop** association [WMI class](../wmisdk/retrieving-a-class.md) relates a user account and desktop settings that are specific to it.</span></span>

<span data-ttu-id="873da-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="873da-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="873da-106">Le proprietà e i metodi sono in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="873da-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="873da-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="873da-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4FF-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_UserDesktop : CIM_ElementSetting
{
  Win32_UserAccount REF Element;
  Win32_Desktop     REF Setting;
};
```

## <a name="members"></a><span data-ttu-id="873da-108">Members</span><span class="sxs-lookup"><span data-stu-id="873da-108">Members</span></span>

<span data-ttu-id="873da-109">La classe **Win32 \_ UserDesktop** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="873da-109">The **Win32\_UserDesktop** class has these types of members:</span></span>

-   [<span data-ttu-id="873da-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="873da-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="873da-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="873da-111">Properties</span></span>

<span data-ttu-id="873da-112">La classe **Win32 \_ UserDesktop** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="873da-112">The **Win32\_UserDesktop** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="873da-113">**elemento**</span><span class="sxs-lookup"><span data-stu-id="873da-113">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="873da-114">Tipo di dati: **Win32 \_ AccountUtente**</span><span class="sxs-lookup"><span data-stu-id="873da-114">Data type: **Win32\_UserAccount**</span></span>
</dt> <dt>

<span data-ttu-id="873da-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="873da-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="873da-116">Qualificatori: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ AccountUtente")</span><span class="sxs-lookup"><span data-stu-id="873da-116">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_UserAccount")</span></span>
</dt> </dl>

<span data-ttu-id="873da-117">Riferimento all'istanza di che rappresenta l'account utente il cui desktop può essere personalizzato tramite la proprietà **Settings** di questa classe.</span><span class="sxs-lookup"><span data-stu-id="873da-117">Reference to the instance representing the user account whose desktop can be customized by the **Settings** property of this class.</span></span>

</dd> <dt>

<span data-ttu-id="873da-118">**Impostazione**</span><span class="sxs-lookup"><span data-stu-id="873da-118">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="873da-119">Tipo di dati **: \_ desktop Win32**</span><span class="sxs-lookup"><span data-stu-id="873da-119">Data type: **Win32\_Desktop**</span></span>
</dt> <dt>

<span data-ttu-id="873da-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="873da-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="873da-121">Qualificatori: [**chiave**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("impostazione"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| desktop Win32 WMI \_ ")</span><span class="sxs-lookup"><span data-stu-id="873da-121">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Setting"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_Desktop")</span></span>
</dt> </dl>

<span data-ttu-id="873da-122">Riferimento all'istanza di che rappresenta le impostazioni desktop che consentono di personalizzare un desktop dell'account utente specifico.</span><span class="sxs-lookup"><span data-stu-id="873da-122">Reference to the instance representing the desktop settings that serve to customize a specific user account desktop.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="873da-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="873da-123">Remarks</span></span>

<span data-ttu-id="873da-124">La classe **Win32 \_ UserDesktop** è derivata da [**CIM \_ ElementSetting**](cim-elementsetting.md).</span><span class="sxs-lookup"><span data-stu-id="873da-124">The **Win32\_UserDesktop** class is derived from [**CIM\_ElementSetting**](cim-elementsetting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="873da-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="873da-125">Requirements</span></span>



| <span data-ttu-id="873da-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="873da-126">Requirement</span></span> | <span data-ttu-id="873da-127">Valore</span><span class="sxs-lookup"><span data-stu-id="873da-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="873da-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="873da-128">Minimum supported client</span></span><br/> | <span data-ttu-id="873da-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="873da-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="873da-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="873da-130">Minimum supported server</span></span><br/> | <span data-ttu-id="873da-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="873da-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="873da-132">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="873da-132">Namespace</span></span><br/>                | <span data-ttu-id="873da-133">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="873da-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="873da-134">MOF</span><span class="sxs-lookup"><span data-stu-id="873da-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="873da-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="873da-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="873da-136">DLL</span><span class="sxs-lookup"><span data-stu-id="873da-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="873da-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="873da-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="873da-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="873da-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="873da-139">**\_ELEMENTSETTING CIM**</span><span class="sxs-lookup"><span data-stu-id="873da-139">**CIM\_ElementSetting**</span></span>](cim-elementsetting.md)
</dt> <dt>

[<span data-ttu-id="873da-140">Classi del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="873da-140">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
