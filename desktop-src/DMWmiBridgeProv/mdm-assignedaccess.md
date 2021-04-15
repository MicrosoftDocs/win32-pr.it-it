---
title: Classe MDM_AssignedAccess
description: La \_ classe MDM AssignedAccess viene usata per impostare il dispositivo per l'esecuzione in modalità tutto schermo.
ms.assetid: b9837f91-3c13-4a80-bf6d-66d8b53dfa70
keywords:
- Classe MDM_AssignedAccess
- Classe MDM_AssignedAccess, descritta
topic_type:
- apiref
api_name:
- MDM_AssignedAccess
- MDM_AssignedAccess.InstanceID
- MDM_AssignedAccess.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b5f03f99183400d4e7672323072415918e8e58e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479073"
---
# <a name="mdm_assignedaccess-class"></a><span data-ttu-id="e3496-105">MDM \_ AssignedAccess (classe)</span><span class="sxs-lookup"><span data-stu-id="e3496-105">MDM\_AssignedAccess class</span></span>

<span data-ttu-id="e3496-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="e3496-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="e3496-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="e3496-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="e3496-108">La classe **MDM \_ AssignedAccess** viene usata per impostare il dispositivo per l'esecuzione in modalità tutto schermo.</span><span class="sxs-lookup"><span data-stu-id="e3496-108">The **MDM\_AssignedAccess** class is used to set the device to run in kiosk mode.</span></span> <span data-ttu-id="e3496-109">Dopo che la classe è stata eseguita, il successivo accesso utente associato alla modalità tutto schermo consente di inserire il dispositivo in modalità tutto schermo che esegue l'applicazione specificata nel pacchetto di provisioning.</span><span class="sxs-lookup"><span data-stu-id="e3496-109">Once the class has been executed, then the next user login that is associated with the kiosk mode puts the device in the kiosk mode running the application specified in the provisioning package.</span></span>

<span data-ttu-id="e3496-110">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="e3496-110">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3496-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e3496-111">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_AssignedAccess
{
  string InstanceID;
  string ParentID;
  string KioskModeApp;
  string Configuration;
};
```

## <a name="members"></a><span data-ttu-id="e3496-112">Members</span><span class="sxs-lookup"><span data-stu-id="e3496-112">Members</span></span>

<span data-ttu-id="e3496-113">La classe **MDM \_ AssignedAccess** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="e3496-113">The **MDM\_AssignedAccess** class has these types of members:</span></span>

-   [<span data-ttu-id="e3496-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e3496-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e3496-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e3496-115">Properties</span></span>

<span data-ttu-id="e3496-116">La classe **MDM \_ AssignedAccess** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="e3496-116">The **MDM\_AssignedAccess** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="e3496-117">Configuration</span><span class="sxs-lookup"><span data-stu-id="e3496-117">Configuration</span></span>](/windows/client-management/mdm/assignedaccess-csp#assignedaccess-configuration)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e3496-118">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e3496-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e3496-119">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="e3496-119">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e3496-120">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="e3496-120">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e3496-121">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e3496-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e3496-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e3496-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e3496-123">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e3496-123">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="e3496-124">Identifica il nome del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="e3496-124">Identifies the name of the parent node.</span></span> <span data-ttu-id="e3496-125">Per questa classe la stringa è "AssignedAccess".</span><span class="sxs-lookup"><span data-stu-id="e3496-125">For this class, the string is "AssignedAccess".</span></span>

</dd> <dt>

[<span data-ttu-id="e3496-126">KioskModeApp</span><span class="sxs-lookup"><span data-stu-id="e3496-126">KioskModeApp</span></span>](/windows/client-management/mdm/assignedaccess-csp#assignedaccess-kioskmodeapp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e3496-127">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e3496-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e3496-128">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="e3496-128">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e3496-129">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="e3496-129">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e3496-130">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e3496-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e3496-131">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e3496-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e3496-132">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e3496-132">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="e3496-133">Descrive il percorso completo del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="e3496-133">Describes the full path to the parent node.</span></span> <span data-ttu-id="e3496-134">Per questa classe la stringa è "./Vendor/MSFT/"</span><span class="sxs-lookup"><span data-stu-id="e3496-134">For this class, the string is "./Vendor/MSFT/"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e3496-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e3496-135">Requirements</span></span>



| <span data-ttu-id="e3496-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="e3496-136">Requirement</span></span> | <span data-ttu-id="e3496-137">Valore</span><span class="sxs-lookup"><span data-stu-id="e3496-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3496-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e3496-138">Minimum supported client</span></span><br/> | <span data-ttu-id="e3496-139">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="e3496-139">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e3496-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e3496-140">Minimum supported server</span></span><br/> | <span data-ttu-id="e3496-141">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="e3496-141">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="e3496-142">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="e3496-142">Namespace</span></span><br/>                | <span data-ttu-id="e3496-143">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="e3496-143">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="e3496-144">MOF</span><span class="sxs-lookup"><span data-stu-id="e3496-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e3496-145"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e3496-145"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="e3496-146">DLL</span><span class="sxs-lookup"><span data-stu-id="e3496-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e3496-147"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e3496-147"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3496-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e3496-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3496-149">Utilizzo di script di PowerShell con il provider del Bridge WMI</span><span class="sxs-lookup"><span data-stu-id="e3496-149">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

