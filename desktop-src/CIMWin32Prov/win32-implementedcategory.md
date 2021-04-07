---
description: La \_ classe WMI dell'associazione ImplementedCategory Win32 mette in relazione una categoria di componenti e la classe Component Object Model (com) utilizzando le relative interfacce.
ms.assetid: 7cf32b50-9ae6-44e5-b364-bc74dea3dc17
ms.tgt_platform: multiple
title: Classe Win32_ImplementedCategory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ImplementedCategory
- Win32_ImplementedCategory.Category
- Win32_ImplementedCategory.Component
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1d885c8c8e92ea661e06b46f338924355438ff9a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749015"
---
# <a name="win32_implementedcategory-class"></a><span data-ttu-id="6ba38-103">Win32 \_ ImplementedCategory (classe)</span><span class="sxs-lookup"><span data-stu-id="6ba38-103">Win32\_ImplementedCategory class</span></span>

<span data-ttu-id="6ba38-104">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) dell'associazione **\_ ImplementedCategory Win32** mette in relazione una categoria di componenti e la classe Component Object Model (com) utilizzando le relative interfacce.</span><span class="sxs-lookup"><span data-stu-id="6ba38-104">The **Win32\_ImplementedCategory** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a component category and the Component Object Model (COM) class using its interfaces.</span></span>

<span data-ttu-id="6ba38-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="6ba38-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="6ba38-106">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="6ba38-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ba38-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6ba38-107">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("CIMWin32"), UUID("{0F73ED5B-8ED9-11d2-B340-00105A1F8569}"), AMENDMENT]
class Win32_ImplementedCategory
{
  Win32_ComponentCategory REF Category;
  Win32_ClassicCOMClass   REF Component;
};
```

## <a name="members"></a><span data-ttu-id="6ba38-108">Members</span><span class="sxs-lookup"><span data-stu-id="6ba38-108">Members</span></span>

<span data-ttu-id="6ba38-109">La classe **Win32 \_ ImplementedCategory** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="6ba38-109">The **Win32\_ImplementedCategory** class has these types of members:</span></span>

-   [<span data-ttu-id="6ba38-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="6ba38-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6ba38-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="6ba38-111">Properties</span></span>

<span data-ttu-id="6ba38-112">La classe **Win32 \_ ImplementedCategory** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="6ba38-112">The **Win32\_ImplementedCategory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6ba38-113">**Categoria**</span><span class="sxs-lookup"><span data-stu-id="6ba38-113">**Category**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ba38-114">Tipo di dati: **Win32 \_ ComponentCategory**</span><span class="sxs-lookup"><span data-stu-id="6ba38-114">Data type: **Win32\_ComponentCategory**</span></span>
</dt> <dt>

<span data-ttu-id="6ba38-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6ba38-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6ba38-116">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ ComponentCategory")</span><span class="sxs-lookup"><span data-stu-id="6ba38-116">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_ComponentCategory")</span></span>
</dt> </dl>

<span data-ttu-id="6ba38-117">Riferimento all'istanza di che rappresenta la categoria di componenti utilizzata dalla classe COM.</span><span class="sxs-lookup"><span data-stu-id="6ba38-117">Reference to the instance representing the component category being used by the COM class.</span></span>

</dd> <dt>

<span data-ttu-id="6ba38-118">**Componente**</span><span class="sxs-lookup"><span data-stu-id="6ba38-118">**Component**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ba38-119">Tipo di dati: **Win32 \_ ClassicCOMClass**</span><span class="sxs-lookup"><span data-stu-id="6ba38-119">Data type: **Win32\_ClassicCOMClass**</span></span>
</dt> <dt>

<span data-ttu-id="6ba38-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6ba38-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6ba38-121">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ ClassicCOMClass")</span><span class="sxs-lookup"><span data-stu-id="6ba38-121">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_ClassicCOMClass")</span></span>
</dt> </dl>

<span data-ttu-id="6ba38-122">Riferimento all'istanza di che rappresenta la classe COM utilizzando la categoria associata.</span><span class="sxs-lookup"><span data-stu-id="6ba38-122">Reference to the instance representing the COM class using the associated category.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6ba38-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6ba38-123">Requirements</span></span>



| <span data-ttu-id="6ba38-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="6ba38-124">Requirement</span></span> | <span data-ttu-id="6ba38-125">Valore</span><span class="sxs-lookup"><span data-stu-id="6ba38-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6ba38-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6ba38-126">Minimum supported client</span></span><br/> | <span data-ttu-id="6ba38-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6ba38-127">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6ba38-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6ba38-128">Minimum supported server</span></span><br/> | <span data-ttu-id="6ba38-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6ba38-129">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6ba38-130">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="6ba38-130">Namespace</span></span><br/>                | <span data-ttu-id="6ba38-131">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="6ba38-131">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6ba38-132">MOF</span><span class="sxs-lookup"><span data-stu-id="6ba38-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6ba38-133"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6ba38-133"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6ba38-134">DLL</span><span class="sxs-lookup"><span data-stu-id="6ba38-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6ba38-135"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6ba38-135"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ba38-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6ba38-136">See also</span></span>

<dl> <dt>

<span data-ttu-id="6ba38-137">[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6ba38-137">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

