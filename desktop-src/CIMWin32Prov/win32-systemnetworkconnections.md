---
description: La \_ classe WMI dell'associazione SystemNetworkConnections Win32 mette in correlazione una connessione di rete e il computer in cui risiede.
ms.assetid: 7c47f653-74a9-4729-a72c-94930181f8c9
ms.tgt_platform: multiple
title: Classe Win32_SystemNetworkConnections
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemNetworkConnections
- Win32_SystemNetworkConnections.GroupComponent
- Win32_SystemNetworkConnections.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e90562dd4f98a00cf848fb83a9e3051b387241e4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127611"
---
# <a name="win32_systemnetworkconnections-class"></a><span data-ttu-id="03a5e-103">Win32 \_ SystemNetworkConnections (classe)</span><span class="sxs-lookup"><span data-stu-id="03a5e-103">Win32\_SystemNetworkConnections class</span></span>

<span data-ttu-id="03a5e-104">La [classe WMI](../wmisdk/retrieving-a-class.md) dell'associazione **\_ SystemNetworkConnections Win32** mette in correlazione una connessione di rete e il computer in cui risiede.</span><span class="sxs-lookup"><span data-stu-id="03a5e-104">The **Win32\_SystemNetworkConnections** association [WMI class](../wmisdk/retrieving-a-class.md) relates a network connection and the computer system on which it resides.</span></span>

<span data-ttu-id="03a5e-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="03a5e-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="03a5e-106">Le proprietà e i metodi sono in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="03a5e-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="03a5e-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="03a5e-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4F7-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemNetworkConnections : CIM_SystemComponent
{
  Win32_ComputerSystem    REF GroupComponent;
  Win32_NetworkConnection REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="03a5e-108">Members</span><span class="sxs-lookup"><span data-stu-id="03a5e-108">Members</span></span>

<span data-ttu-id="03a5e-109">La classe **Win32 \_ SystemNetworkConnections** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="03a5e-109">The **Win32\_SystemNetworkConnections** class has these types of members:</span></span>

-   [<span data-ttu-id="03a5e-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="03a5e-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="03a5e-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="03a5e-111">Properties</span></span>

<span data-ttu-id="03a5e-112">La classe **Win32 \_ SystemNetworkConnections** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="03a5e-112">The **Win32\_SystemNetworkConnections** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="03a5e-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="03a5e-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03a5e-114">Tipo di dati: **Win32 \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="03a5e-114">Data type: **Win32\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="03a5e-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="03a5e-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03a5e-116">Qualificatori: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ ComputerSystem")</span><span class="sxs-lookup"><span data-stu-id="03a5e-116">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_ComputerSystem")</span></span>
</dt> </dl>

<span data-ttu-id="03a5e-117">Riferimento all'istanza di che rappresenta il sistema di computer connesso alla rete.</span><span class="sxs-lookup"><span data-stu-id="03a5e-117">Reference to the instance representing the computer system connected to the network.</span></span>

</dd> <dt>

<span data-ttu-id="03a5e-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="03a5e-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03a5e-119">Tipo di dati: **Win32 \_ NetworkConnection**</span><span class="sxs-lookup"><span data-stu-id="03a5e-119">Data type: **Win32\_NetworkConnection**</span></span>
</dt> <dt>

<span data-ttu-id="03a5e-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="03a5e-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03a5e-121">Qualificatori: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ NetworkConnection")</span><span class="sxs-lookup"><span data-stu-id="03a5e-121">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_NetworkConnection")</span></span>
</dt> </dl>

<span data-ttu-id="03a5e-122">Riferimento all'istanza di che rappresenta la connessione di rete a questo sistema del computer.</span><span class="sxs-lookup"><span data-stu-id="03a5e-122">Reference to the instance representing the network connection to this computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="03a5e-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="03a5e-123">Remarks</span></span>

<span data-ttu-id="03a5e-124">La classe **Win32 \_ SystemNetworkConnections** è derivata da [**CIM \_ SystemComponent**](cim-systemcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="03a5e-124">The **Win32\_SystemNetworkConnections** class is derived from [**CIM\_SystemComponent**](cim-systemcomponent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="03a5e-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="03a5e-125">Requirements</span></span>



| <span data-ttu-id="03a5e-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="03a5e-126">Requirement</span></span> | <span data-ttu-id="03a5e-127">Valore</span><span class="sxs-lookup"><span data-stu-id="03a5e-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="03a5e-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="03a5e-128">Minimum supported client</span></span><br/> | <span data-ttu-id="03a5e-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="03a5e-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="03a5e-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="03a5e-130">Minimum supported server</span></span><br/> | <span data-ttu-id="03a5e-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="03a5e-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="03a5e-132">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="03a5e-132">Namespace</span></span><br/>                | <span data-ttu-id="03a5e-133">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="03a5e-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="03a5e-134">MOF</span><span class="sxs-lookup"><span data-stu-id="03a5e-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="03a5e-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="03a5e-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="03a5e-136">DLL</span><span class="sxs-lookup"><span data-stu-id="03a5e-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="03a5e-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="03a5e-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03a5e-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="03a5e-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03a5e-139">**\_SYSTEMCOMPONENT CIM**</span><span class="sxs-lookup"><span data-stu-id="03a5e-139">**CIM\_SystemComponent**</span></span>](cim-systemcomponent.md)
</dt> <dt>

[<span data-ttu-id="03a5e-140">Classi del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="03a5e-140">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
