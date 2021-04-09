---
description: La \_ classe WMI dell'associazione ClientApplicationSetting Win32 mette in correlazione un file eseguibile e un'applicazione Component Object Model (com) che contiene le opzioni di configurazione com per il file eseguibile.
ms.assetid: c43d80ee-0f29-4452-b51f-f18543bc1d35
ms.tgt_platform: multiple
title: Classe Win32_ClientApplicationSetting
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ClientApplicationSetting
- Win32_ClientApplicationSetting.Application
- Win32_ClientApplicationSetting.Client
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: fda1f1305904fa919bb2080fe5de02f0e5850a8a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966271"
---
# <a name="win32_clientapplicationsetting-class"></a><span data-ttu-id="ade75-103">Win32 \_ ClientApplicationSetting (classe)</span><span class="sxs-lookup"><span data-stu-id="ade75-103">Win32\_ClientApplicationSetting class</span></span>

<span data-ttu-id="ade75-104">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) dell'associazione **\_ ClientApplicationSetting Win32** mette in correlazione un file eseguibile e un'applicazione Component Object Model (com) che contiene le opzioni di configurazione com per il file eseguibile.</span><span class="sxs-lookup"><span data-stu-id="ade75-104">The **Win32\_ClientApplicationSetting** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates an executable file and a Component Object Model (COM) application that contains the COM configuration options for the executable file.</span></span>

<span data-ttu-id="ade75-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="ade75-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="ade75-106">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="ade75-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="ade75-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ade75-107">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("CIMWin32"), UUID("{0F73ED5E-8ED9-11d2-B340-00105A1F8569}"), AMENDMENT]
class Win32_ClientApplicationSetting
{
  Win32_DCOMApplication REF Application;
  CIM_DataFile          REF Client;
};
```

## <a name="members"></a><span data-ttu-id="ade75-108">Members</span><span class="sxs-lookup"><span data-stu-id="ade75-108">Members</span></span>

<span data-ttu-id="ade75-109">La classe **Win32 \_ ClientApplicationSetting** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="ade75-109">The **Win32\_ClientApplicationSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="ade75-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ade75-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ade75-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ade75-111">Properties</span></span>

<span data-ttu-id="ade75-112">La classe **Win32 \_ ClientApplicationSetting** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="ade75-112">The **Win32\_ClientApplicationSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ade75-113">**Applicazione**</span><span class="sxs-lookup"><span data-stu-id="ade75-113">**Application**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ade75-114">Tipo di dati: **Win32 \_ DCOMApplication**</span><span class="sxs-lookup"><span data-stu-id="ade75-114">Data type: **Win32\_DCOMApplication**</span></span>
</dt> <dt>

<span data-ttu-id="ade75-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ade75-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ade75-116">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ DCOMApplication")</span><span class="sxs-lookup"><span data-stu-id="ade75-116">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_DCOMApplication")</span></span>
</dt> </dl>

<span data-ttu-id="ade75-117">Riferimento all'istanza di che rappresenta l'applicazione COM che contiene le opzioni di configurazione del file eseguibile.</span><span class="sxs-lookup"><span data-stu-id="ade75-117">Reference to the instance that represents the COM application that contains configuration options of the executable file.</span></span>

</dd> <dt>

<span data-ttu-id="ade75-118">**Client**</span><span class="sxs-lookup"><span data-stu-id="ade75-118">**Client**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ade75-119">Tipo di dati **: \_ DataFile CIM**</span><span class="sxs-lookup"><span data-stu-id="ade75-119">Data type: **CIM\_DataFile**</span></span>
</dt> <dt>

<span data-ttu-id="ade75-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ade75-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ade75-121">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| DataFile CIM CIM \_ ")</span><span class="sxs-lookup"><span data-stu-id="ade75-121">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\|CIM\_DataFile")</span></span>
</dt> </dl>

<span data-ttu-id="ade75-122">Riferimento all'istanza di che rappresenta il file eseguibile che utilizza le impostazioni COM.</span><span class="sxs-lookup"><span data-stu-id="ade75-122">Reference to the instance that represents the executable file that uses COM settings.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ade75-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="ade75-123">Remarks</span></span>

<span data-ttu-id="ade75-124">**Win32 \_ ClientApplicationSetting** non supporta l'enumerazione.</span><span class="sxs-lookup"><span data-stu-id="ade75-124">**Win32\_ClientApplicationSetting** does not support enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="ade75-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ade75-125">Requirements</span></span>



| <span data-ttu-id="ade75-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="ade75-126">Requirement</span></span> | <span data-ttu-id="ade75-127">Valore</span><span class="sxs-lookup"><span data-stu-id="ade75-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ade75-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ade75-128">Minimum supported client</span></span><br/> | <span data-ttu-id="ade75-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ade75-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ade75-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ade75-130">Minimum supported server</span></span><br/> | <span data-ttu-id="ade75-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ade75-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ade75-132">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ade75-132">Namespace</span></span><br/>                | <span data-ttu-id="ade75-133">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="ade75-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ade75-134">MOF</span><span class="sxs-lookup"><span data-stu-id="ade75-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ade75-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ade75-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ade75-136">DLL</span><span class="sxs-lookup"><span data-stu-id="ade75-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ade75-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ade75-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ade75-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ade75-138">See also</span></span>

<dl> <dt>

<span data-ttu-id="ade75-139">[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ade75-139">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

