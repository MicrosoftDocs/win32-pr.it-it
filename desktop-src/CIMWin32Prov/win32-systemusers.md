---
description: La \_ classe WMI dell'associazione SystemUsers Win32 mette in correlazione un computer e un account utente nel sistema.
ms.assetid: 0f6cba69-86f7-4795-a47d-6fb8ed0a00b8
ms.tgt_platform: multiple
title: Classe Win32_SystemUsers
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemUsers
- Win32_SystemUsers.GroupComponent
- Win32_SystemUsers.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a2239983d5b9c080c60d301a557b5487f8cf7fcf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966322"
---
# <a name="win32_systemusers-class"></a><span data-ttu-id="6abb9-103">Win32 \_ SystemUsers (classe)</span><span class="sxs-lookup"><span data-stu-id="6abb9-103">Win32\_SystemUsers class</span></span>

<span data-ttu-id="6abb9-104">La [classe WMI](../wmisdk/retrieving-a-class.md) dell'associazione **\_ SystemUsers Win32** mette in correlazione un computer e un account utente nel sistema.</span><span class="sxs-lookup"><span data-stu-id="6abb9-104">The **Win32\_SystemUsers** association [WMI class](../wmisdk/retrieving-a-class.md) relates a computer system and a user account on that system.</span></span>

<span data-ttu-id="6abb9-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="6abb9-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="6abb9-106">Le proprietà e i metodi sono in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="6abb9-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="6abb9-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6abb9-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4F2-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemUsers : CIM_SystemComponent
{
  Win32_ComputerSystem REF GroupComponent;
  Win32_UserAccount    REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="6abb9-108">Members</span><span class="sxs-lookup"><span data-stu-id="6abb9-108">Members</span></span>

<span data-ttu-id="6abb9-109">La classe **Win32 \_ SystemUsers** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="6abb9-109">The **Win32\_SystemUsers** class has these types of members:</span></span>

-   [<span data-ttu-id="6abb9-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="6abb9-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6abb9-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="6abb9-111">Properties</span></span>

<span data-ttu-id="6abb9-112">La classe **Win32 \_ SystemUsers** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="6abb9-112">The **Win32\_SystemUsers** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6abb9-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="6abb9-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6abb9-114">Tipo di dati: **Win32 \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="6abb9-114">Data type: **Win32\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="6abb9-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6abb9-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6abb9-116">Qualificatori: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ ComputerSystem")</span><span class="sxs-lookup"><span data-stu-id="6abb9-116">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_ComputerSystem")</span></span>
</dt> </dl>

<span data-ttu-id="6abb9-117">Riferimento all'istanza di che rappresenta il computer che contiene l'account utente.</span><span class="sxs-lookup"><span data-stu-id="6abb9-117">Reference to the instance representing the computer system containing the user account.</span></span>

</dd> <dt>

<span data-ttu-id="6abb9-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="6abb9-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6abb9-119">Tipo di dati: **Win32 \_ AccountUtente**</span><span class="sxs-lookup"><span data-stu-id="6abb9-119">Data type: **Win32\_UserAccount**</span></span>
</dt> <dt>

<span data-ttu-id="6abb9-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6abb9-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6abb9-121">Qualificatori: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ AccountUtente")</span><span class="sxs-lookup"><span data-stu-id="6abb9-121">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_UserAccount")</span></span>
</dt> </dl>

<span data-ttu-id="6abb9-122">Riferimento all'istanza di che rappresenta l'account utente nel computer.</span><span class="sxs-lookup"><span data-stu-id="6abb9-122">Reference to the instance representing the user account on the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6abb9-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="6abb9-123">Remarks</span></span>

<span data-ttu-id="6abb9-124">La classe **Win32 \_ SystemUsers** è derivata da [**CIM \_ SystemComponent**](cim-systemcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="6abb9-124">The **Win32\_SystemUsers** class is derived from [**CIM\_SystemComponent**](cim-systemcomponent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6abb9-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6abb9-125">Requirements</span></span>



| <span data-ttu-id="6abb9-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="6abb9-126">Requirement</span></span> | <span data-ttu-id="6abb9-127">Valore</span><span class="sxs-lookup"><span data-stu-id="6abb9-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6abb9-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6abb9-128">Minimum supported client</span></span><br/> | <span data-ttu-id="6abb9-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6abb9-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6abb9-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6abb9-130">Minimum supported server</span></span><br/> | <span data-ttu-id="6abb9-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6abb9-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6abb9-132">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="6abb9-132">Namespace</span></span><br/>                | <span data-ttu-id="6abb9-133">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="6abb9-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6abb9-134">MOF</span><span class="sxs-lookup"><span data-stu-id="6abb9-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6abb9-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6abb9-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6abb9-136">DLL</span><span class="sxs-lookup"><span data-stu-id="6abb9-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6abb9-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6abb9-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6abb9-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6abb9-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6abb9-139">**\_SYSTEMCOMPONENT CIM**</span><span class="sxs-lookup"><span data-stu-id="6abb9-139">**CIM\_SystemComponent**</span></span>](cim-systemcomponent.md)
</dt> <dt>

[<span data-ttu-id="6abb9-140">Classi del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="6abb9-140">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
