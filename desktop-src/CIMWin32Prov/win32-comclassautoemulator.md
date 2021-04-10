---
description: La \_ classe WMI dell'associazione ComClassAutoEmulator Win32 mette in correlazione una classe Component Object Model (com) e un'altra classe com che emula automaticamente.
ms.assetid: e060ba26-98e7-47cb-bf21-1ca80d0e8a07
ms.tgt_platform: multiple
title: Classe Win32_ComClassAutoEmulator
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ComClassAutoEmulator
- Win32_ComClassAutoEmulator.NewVersion
- Win32_ComClassAutoEmulator.OldVersion
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9442036d43859caa5fa277109c7e85553e7d42f0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127346"
---
# <a name="win32_comclassautoemulator-class"></a><span data-ttu-id="987db-103">Win32 \_ ComClassAutoEmulator (classe)</span><span class="sxs-lookup"><span data-stu-id="987db-103">Win32\_ComClassAutoEmulator class</span></span>

<span data-ttu-id="987db-104">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) dell'associazione **\_ ComClassAutoEmulator Win32** mette in correlazione una classe Component Object Model (com) e un'altra classe com che emula automaticamente.</span><span class="sxs-lookup"><span data-stu-id="987db-104">The **Win32\_ComClassAutoEmulator** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a Component Object Model (COM) class and another COM class that it automatically emulates.</span></span>

<span data-ttu-id="987db-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="987db-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="987db-106">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="987db-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="987db-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="987db-107">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("CIMWin32"), UUID("{0F73ED5D-8ED9-11d2-B340-00105A1F8569}"), AMENDMENT]
class Win32_ComClassAutoEmulator
{
  Win32_ClassicCOMClass REF NewVersion;
  Win32_ClassicCOMClass REF OldVersion;
};
```

## <a name="members"></a><span data-ttu-id="987db-108">Members</span><span class="sxs-lookup"><span data-stu-id="987db-108">Members</span></span>

<span data-ttu-id="987db-109">La classe **Win32 \_ ComClassAutoEmulator** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="987db-109">The **Win32\_ComClassAutoEmulator** class has these types of members:</span></span>

-   [<span data-ttu-id="987db-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="987db-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="987db-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="987db-111">Properties</span></span>

<span data-ttu-id="987db-112">La classe **Win32 \_ ComClassAutoEmulator** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="987db-112">The **Win32\_ComClassAutoEmulator** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="987db-113">**NewVersion**</span><span class="sxs-lookup"><span data-stu-id="987db-113">**NewVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="987db-114">Tipo di dati: **Win32 \_ ClassicCOMClass**</span><span class="sxs-lookup"><span data-stu-id="987db-114">Data type: **Win32\_ClassicCOMClass**</span></span>
</dt> <dt>

<span data-ttu-id="987db-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="987db-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="987db-116">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ ClassicCOMClass")</span><span class="sxs-lookup"><span data-stu-id="987db-116">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_ClassicCOMClass")</span></span>
</dt> </dl>

<span data-ttu-id="987db-117">Riferimento all'istanza che rappresenta il componente COM in grado di emulare automaticamente il componente COM associato.</span><span class="sxs-lookup"><span data-stu-id="987db-117">Reference to the instance representing the COM component that can automatically emulate the associated COM component.</span></span> <span data-ttu-id="987db-118">Queste informazioni vengono ottenute tramite la voce del registro di sistema autotreats.</span><span class="sxs-lookup"><span data-stu-id="987db-118">This information is obtained through the AutoTreatAs registry entry.</span></span>

</dd> <dt>

<span data-ttu-id="987db-119">**OldVersion**</span><span class="sxs-lookup"><span data-stu-id="987db-119">**OldVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="987db-120">Tipo di dati: **Win32 \_ ClassicCOMClass**</span><span class="sxs-lookup"><span data-stu-id="987db-120">Data type: **Win32\_ClassicCOMClass**</span></span>
</dt> <dt>

<span data-ttu-id="987db-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="987db-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="987db-122">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ ClassicCOMClass")</span><span class="sxs-lookup"><span data-stu-id="987db-122">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_ClassicCOMClass")</span></span>
</dt> </dl>

<span data-ttu-id="987db-123">Riferimento all'istanza che rappresenta il componente COM emulato automaticamente da un altro componente.</span><span class="sxs-lookup"><span data-stu-id="987db-123">Reference to the instance representing the COM component that is automatically emulated by another component.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="987db-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="987db-124">Requirements</span></span>



| <span data-ttu-id="987db-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="987db-125">Requirement</span></span> | <span data-ttu-id="987db-126">Valore</span><span class="sxs-lookup"><span data-stu-id="987db-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="987db-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="987db-127">Minimum supported client</span></span><br/> | <span data-ttu-id="987db-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="987db-128">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="987db-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="987db-129">Minimum supported server</span></span><br/> | <span data-ttu-id="987db-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="987db-130">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="987db-131">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="987db-131">Namespace</span></span><br/>                | <span data-ttu-id="987db-132">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="987db-132">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="987db-133">MOF</span><span class="sxs-lookup"><span data-stu-id="987db-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="987db-134"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="987db-134"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="987db-135">DLL</span><span class="sxs-lookup"><span data-stu-id="987db-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="987db-136"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="987db-136"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="987db-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="987db-137">See also</span></span>

<dl> <dt>

<span data-ttu-id="987db-138">[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="987db-138">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

