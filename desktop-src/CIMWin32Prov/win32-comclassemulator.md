---
description: La \_ classe WMI dell'associazione ComClassEmulator Win32 mette in relazione due versioni di una classe Component Object Model (com).
ms.assetid: 33899c1e-911d-49ad-be25-355dcdb8f0c7
ms.tgt_platform: multiple
title: Classe Win32_ComClassEmulator
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ComClassEmulator
- Win32_ComClassEmulator.NewVersion
- Win32_ComClassEmulator.OldVersion
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9966ed85b0e0b4eeb25073e13ad679759f1d460b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126108"
---
# <a name="win32_comclassemulator-class"></a><span data-ttu-id="2fa40-103">Win32 \_ ComClassEmulator (classe)</span><span class="sxs-lookup"><span data-stu-id="2fa40-103">Win32\_ComClassEmulator class</span></span>

<span data-ttu-id="2fa40-104">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) dell'associazione **\_ ComClassEmulator Win32** mette in relazione due versioni di una classe Component Object Model (com).</span><span class="sxs-lookup"><span data-stu-id="2fa40-104">The **Win32\_ComClassEmulator** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates two versions of a Component Object Model (COM) class.</span></span>

<span data-ttu-id="2fa40-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="2fa40-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="2fa40-106">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="2fa40-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="2fa40-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2fa40-107">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("CIMWin32"), UUID("{0F73ED5C-8ED9-11d2-B340-00105A1F8569}"), AMENDMENT]
class Win32_ComClassEmulator
{
  Win32_ClassicCOMClass REF NewVersion;
  Win32_ClassicCOMClass REF OldVersion;
};
```

## <a name="members"></a><span data-ttu-id="2fa40-108">Members</span><span class="sxs-lookup"><span data-stu-id="2fa40-108">Members</span></span>

<span data-ttu-id="2fa40-109">La classe **Win32 \_ ComClassEmulator** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="2fa40-109">The **Win32\_ComClassEmulator** class has these types of members:</span></span>

-   [<span data-ttu-id="2fa40-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2fa40-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2fa40-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2fa40-111">Properties</span></span>

<span data-ttu-id="2fa40-112">La classe **Win32 \_ ComClassEmulator** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="2fa40-112">The **Win32\_ComClassEmulator** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2fa40-113">**NewVersion**</span><span class="sxs-lookup"><span data-stu-id="2fa40-113">**NewVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2fa40-114">Tipo di dati: **Win32 \_ ClassicCOMClass**</span><span class="sxs-lookup"><span data-stu-id="2fa40-114">Data type: **Win32\_ClassicCOMClass**</span></span>
</dt> <dt>

<span data-ttu-id="2fa40-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2fa40-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2fa40-116">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ ClassicCOMClass")</span><span class="sxs-lookup"><span data-stu-id="2fa40-116">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_ClassicCOMClass")</span></span>
</dt> </dl>

<span data-ttu-id="2fa40-117">Riferimento all'istanza che rappresenta il componente COM che contiene le interfacce che emulano la versione precedente del componente.</span><span class="sxs-lookup"><span data-stu-id="2fa40-117">Reference to the instance representing the COM component that contains interfaces emulating the older version of the component.</span></span>

</dd> <dt>

<span data-ttu-id="2fa40-118">**OldVersion**</span><span class="sxs-lookup"><span data-stu-id="2fa40-118">**OldVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2fa40-119">Tipo di dati: **Win32 \_ ClassicCOMClass**</span><span class="sxs-lookup"><span data-stu-id="2fa40-119">Data type: **Win32\_ClassicCOMClass**</span></span>
</dt> <dt>

<span data-ttu-id="2fa40-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2fa40-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2fa40-121">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ ClassicCOMClass")</span><span class="sxs-lookup"><span data-stu-id="2fa40-121">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_ClassicCOMClass")</span></span>
</dt> </dl>

<span data-ttu-id="2fa40-122">Riferimento all'istanza che rappresenta il componente COM con interfacce che possono essere emulate dalla nuova versione del componente.</span><span class="sxs-lookup"><span data-stu-id="2fa40-122">Reference to the instance representing the COM component with interfaces that can be emulated by the new version of the component.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2fa40-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2fa40-123">Requirements</span></span>



| <span data-ttu-id="2fa40-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="2fa40-124">Requirement</span></span> | <span data-ttu-id="2fa40-125">Valore</span><span class="sxs-lookup"><span data-stu-id="2fa40-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2fa40-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2fa40-126">Minimum supported client</span></span><br/> | <span data-ttu-id="2fa40-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2fa40-127">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2fa40-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2fa40-128">Minimum supported server</span></span><br/> | <span data-ttu-id="2fa40-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2fa40-129">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2fa40-130">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="2fa40-130">Namespace</span></span><br/>                | <span data-ttu-id="2fa40-131">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="2fa40-131">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2fa40-132">MOF</span><span class="sxs-lookup"><span data-stu-id="2fa40-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2fa40-133"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2fa40-133"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2fa40-134">DLL</span><span class="sxs-lookup"><span data-stu-id="2fa40-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2fa40-135"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2fa40-135"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2fa40-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2fa40-136">See also</span></span>

<dl> <dt>

<span data-ttu-id="2fa40-137">[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2fa40-137">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

