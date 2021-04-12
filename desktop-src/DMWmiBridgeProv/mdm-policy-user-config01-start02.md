---
title: Classe MDM_Policy_User_Config01_Start02
description: La \_ classe del criterio MDM \_ utente \_ Config01 \_ Start02 rappresenta i criteri di avvio disponibili impostati per ogni singolo utente.
ms.assetid: bbb64553-4d93-433d-96e4-bfd3f5588138
keywords:
- Classe MDM_Policy_User_Config01_Start02
- Classe MDM_Policy_User_Config01_Start02, descritta
topic_type:
- apiref
api_name:
- MDM_Policy_User_Config01_Start02
- MDM_Policy_User_Config01_Start02.InstanceID
- MDM_Policy_User_Config01_Start02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b98b25ee0c3118f741d3a52bc9001c6106d86f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400656"
---
# <a name="mdm_policy_user_config01_start02-class"></a><span data-ttu-id="2d3e0-105">\_Utente criteri \_ MDM \_ Config01 \_ classe Start02</span><span class="sxs-lookup"><span data-stu-id="2d3e0-105">MDM\_Policy\_User\_Config01\_Start02 class</span></span>

<span data-ttu-id="2d3e0-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="2d3e0-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="2d3e0-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="2d3e0-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="2d3e0-108">La classe del **\_ criterio MDM \_ utente \_ Config01 \_ Start02** rappresenta i criteri di avvio disponibili impostati per ogni singolo utente.</span><span class="sxs-lookup"><span data-stu-id="2d3e0-108">The **MDM\_Policy\_User\_Config01\_Start02** class represents the start policies available that are set on a per-user basis.</span></span>

<span data-ttu-id="2d3e0-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="2d3e0-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d3e0-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2d3e0-110">Syntax</span></span>

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Config01_Start02
{
  string InstanceID;
  string ParentID;
  sint32 HidePeopleBar;
  string StartLayout;
};
```

## <a name="members"></a><span data-ttu-id="2d3e0-111">Members</span><span class="sxs-lookup"><span data-stu-id="2d3e0-111">Members</span></span>

<span data-ttu-id="2d3e0-112">La **classe \_ \_ \_ Config01 \_ Start02 dell'utente dei criteri MDM** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="2d3e0-112">The **MDM\_Policy\_User\_Config01\_Start02** class has these types of members:</span></span>

-   [<span data-ttu-id="2d3e0-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2d3e0-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2d3e0-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2d3e0-114">Properties</span></span>

<span data-ttu-id="2d3e0-115">La **classe \_ \_ \_ Config01 \_ Start02 dell'utente dei criteri MDM** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="2d3e0-115">The **MDM\_Policy\_User\_Config01\_Start02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="2d3e0-116">HidePeopleBar</span><span class="sxs-lookup"><span data-stu-id="2d3e0-116">HidePeopleBar</span></span>](/windows/client-management/mdm/policy-csp-start#start-hidepeoplebar)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d3e0-117">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="2d3e0-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2d3e0-118">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="2d3e0-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2d3e0-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="2d3e0-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d3e0-120">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2d3e0-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2d3e0-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2d3e0-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2d3e0-122">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="2d3e0-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="2d3e0-123">Identifica il nome del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="2d3e0-123">Identifies the name of the parent node.</span></span> <span data-ttu-id="2d3e0-124">Per questa classe la stringa è "Start"</span><span class="sxs-lookup"><span data-stu-id="2d3e0-124">For this class, the string is "Start"</span></span>

</dd> <dt>

<span data-ttu-id="2d3e0-125">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="2d3e0-125">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d3e0-126">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2d3e0-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2d3e0-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2d3e0-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2d3e0-128">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="2d3e0-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="2d3e0-129">Descrive il percorso completo del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="2d3e0-129">Describes the full path to the parent node.</span></span> <span data-ttu-id="2d3e0-130">Per questa classe la stringa è "./User/Vendor/MSFT/Policy/Config"</span><span class="sxs-lookup"><span data-stu-id="2d3e0-130">For this class, the string is "./User/Vendor/MSFT/Policy/Config"</span></span>

</dd> <dt>

[<span data-ttu-id="2d3e0-131">StartLayout</span><span class="sxs-lookup"><span data-stu-id="2d3e0-131">StartLayout</span></span>](/windows/client-management/mdm/policy-csp-start#start-startlayout)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d3e0-132">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2d3e0-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2d3e0-133">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="2d3e0-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2d3e0-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2d3e0-134">Requirements</span></span>



| <span data-ttu-id="2d3e0-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="2d3e0-135">Requirement</span></span> | <span data-ttu-id="2d3e0-136">Valore</span><span class="sxs-lookup"><span data-stu-id="2d3e0-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d3e0-137">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2d3e0-137">Minimum supported client</span></span><br/> | <span data-ttu-id="2d3e0-138">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="2d3e0-138">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2d3e0-139">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2d3e0-139">Minimum supported server</span></span><br/> | <span data-ttu-id="2d3e0-140">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="2d3e0-140">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="2d3e0-141">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="2d3e0-141">Namespace</span></span><br/>                | <span data-ttu-id="2d3e0-142">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="2d3e0-142">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="2d3e0-143">MOF</span><span class="sxs-lookup"><span data-stu-id="2d3e0-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2d3e0-144"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2d3e0-144"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="2d3e0-145">DLL</span><span class="sxs-lookup"><span data-stu-id="2d3e0-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2d3e0-146"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2d3e0-146"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2d3e0-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2d3e0-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d3e0-148">Utilizzo di script di PowerShell con il provider del Bridge WMI</span><span class="sxs-lookup"><span data-stu-id="2d3e0-148">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

