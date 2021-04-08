---
description: La \_ classe WMI dell'associazione ShareToDirectory Win32 mette in correlazione una risorsa condivisa nel computer e la directory a cui viene mappata.
ms.assetid: f8562539-2cb4-4661-8ef9-8b665e76a292
ms.tgt_platform: multiple
title: Classe Win32_ShareToDirectory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ShareToDirectory
- Win32_ShareToDirectory.Share
- Win32_ShareToDirectory.SharedElement
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: f02e5e1ce125a2c8495327a08c14c94ac9f48567
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103747823"
---
# <a name="win32_sharetodirectory-class"></a><span data-ttu-id="af6cf-103">Win32 \_ ShareToDirectory (classe)</span><span class="sxs-lookup"><span data-stu-id="af6cf-103">Win32\_ShareToDirectory class</span></span>

<span data-ttu-id="af6cf-104">La [classe WMI](../wmisdk/retrieving-a-class.md) dell'associazione **\_ ShareToDirectory Win32** mette in correlazione una risorsa condivisa nel computer e la directory a cui viene mappata.</span><span class="sxs-lookup"><span data-stu-id="af6cf-104">The **Win32\_ShareToDirectory** association [WMI class](../wmisdk/retrieving-a-class.md) relates a shared resource on the computer system and the directory to which it is mapped.</span></span>

<span data-ttu-id="af6cf-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="af6cf-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="af6cf-106">Le proprietà e i metodi sono in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="af6cf-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="af6cf-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="af6cf-107">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("CIMWin32"), UUID("{8502C511-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_ShareToDirectory
{
  Win32_Share   REF Share;
  CIM_Directory REF SharedElement;
};
```

## <a name="members"></a><span data-ttu-id="af6cf-108">Members</span><span class="sxs-lookup"><span data-stu-id="af6cf-108">Members</span></span>

<span data-ttu-id="af6cf-109">La classe **Win32 \_ ShareToDirectory** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="af6cf-109">The **Win32\_ShareToDirectory** class has these types of members:</span></span>

-   [<span data-ttu-id="af6cf-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="af6cf-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="af6cf-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="af6cf-111">Properties</span></span>

<span data-ttu-id="af6cf-112">La classe **Win32 \_ ShareToDirectory** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="af6cf-112">The **Win32\_ShareToDirectory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="af6cf-113">**Condividi**</span><span class="sxs-lookup"><span data-stu-id="af6cf-113">**Share**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af6cf-114">Tipo di dati **: \_ condivisione Win32**</span><span class="sxs-lookup"><span data-stu-id="af6cf-114">Data type: **Win32\_Share**</span></span>
</dt> <dt>

<span data-ttu-id="af6cf-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="af6cf-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af6cf-116">Qualificatori: [**Key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| condivisione Win32 WMI \_ ")</span><span class="sxs-lookup"><span data-stu-id="af6cf-116">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_Share")</span></span>
</dt> </dl>

<span data-ttu-id="af6cf-117">Riferimento all'istanza di che rappresenta le proprietà di una risorsa condivisa disponibile tramite la directory.</span><span class="sxs-lookup"><span data-stu-id="af6cf-117">Reference to the instance representing the properties of a shared resource available through the directory.</span></span>

</dd> <dt>

<span data-ttu-id="af6cf-118">**SharedElement**</span><span class="sxs-lookup"><span data-stu-id="af6cf-118">**SharedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af6cf-119">Tipo di dati **: \_ directory CIM**</span><span class="sxs-lookup"><span data-stu-id="af6cf-119">Data type: **CIM\_Directory**</span></span>
</dt> <dt>

<span data-ttu-id="af6cf-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="af6cf-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af6cf-121">Qualificatori: [**Key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM \| CIM \_ directory")</span><span class="sxs-lookup"><span data-stu-id="af6cf-121">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM\|CIM\_Directory")</span></span>
</dt> </dl>

<span data-ttu-id="af6cf-122">Riferimento all'istanza di che rappresenta le proprietà della directory di cui è stato eseguito il mapping a una risorsa condivisa.</span><span class="sxs-lookup"><span data-stu-id="af6cf-122">Reference to the instance representing the properties of the directory that has been mapped to a shared resource.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="af6cf-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="af6cf-123">Requirements</span></span>



| <span data-ttu-id="af6cf-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="af6cf-124">Requirement</span></span> | <span data-ttu-id="af6cf-125">Valore</span><span class="sxs-lookup"><span data-stu-id="af6cf-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="af6cf-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="af6cf-126">Minimum supported client</span></span><br/> | <span data-ttu-id="af6cf-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="af6cf-127">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="af6cf-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="af6cf-128">Minimum supported server</span></span><br/> | <span data-ttu-id="af6cf-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="af6cf-129">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="af6cf-130">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="af6cf-130">Namespace</span></span><br/>                | <span data-ttu-id="af6cf-131">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="af6cf-131">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="af6cf-132">MOF</span><span class="sxs-lookup"><span data-stu-id="af6cf-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="af6cf-133"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="af6cf-133"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="af6cf-134">DLL</span><span class="sxs-lookup"><span data-stu-id="af6cf-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="af6cf-135"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="af6cf-135"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="af6cf-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="af6cf-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af6cf-137">Classi del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="af6cf-137">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
