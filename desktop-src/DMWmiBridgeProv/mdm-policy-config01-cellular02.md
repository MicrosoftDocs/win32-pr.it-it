---
title: Classe MDM_Policy_Config01_Cellular02
description: La \_ \_ classe Config01 Cellular02 dei criteri MDM \_ Configura i criteri cellulari.
ms.assetid: e5926a21-a375-4d1c-8b37-7fe7f7532c50
keywords:
- Classe MDM_Policy_Config01_Cellular02
- Classe MDM_Policy_Config01_Cellular02, descritta
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Cellular02
- MDM_Policy_Config01_Cellular02.InstanceID
- MDM_Policy_Config01_Cellular02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b1b6d9163723299b144368d9d2b73a12ccc7a91
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119422"
---
# <a name="mdm_policy_config01_cellular02-class"></a><span data-ttu-id="c30bb-105">\_ \_ Classe Config01 Cellular02 di criteri \_ MDM</span><span class="sxs-lookup"><span data-stu-id="c30bb-105">MDM\_Policy\_Config01\_Cellular02 class</span></span>

<span data-ttu-id="c30bb-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="c30bb-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="c30bb-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="c30bb-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="c30bb-108">La \_ \_ classe Config01 Cellular02 dei criteri MDM \_ Configura i criteri cellulari.</span><span class="sxs-lookup"><span data-stu-id="c30bb-108">The MDM\_Policy\_Config01\_Cellular02 class configures the cellular policies.</span></span>

<span data-ttu-id="c30bb-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="c30bb-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c30bb-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c30bb-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Cellular02
{
  string InstanceID;
  string ParentID;
  string LetAppsAccessCellularData_UserInControlOfTheseApps;
  string LetAppsAccessCellularData_ForceDenyTheseApps;
  string LetAppsAccessCellularData_ForceAllowTheseApps;
  sint32 LetAppsAccessCellularData;
  string ShowAppCellularAccessUI;
};
```

## <a name="members"></a><span data-ttu-id="c30bb-111">Members</span><span class="sxs-lookup"><span data-stu-id="c30bb-111">Members</span></span>

<span data-ttu-id="c30bb-112">La **classe \_ \_ Config01 \_ Cellular02 dei criteri MDM** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="c30bb-112">The **MDM\_Policy\_Config01\_Cellular02** class has these types of members:</span></span>

-   [<span data-ttu-id="c30bb-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c30bb-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c30bb-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c30bb-114">Properties</span></span>

<span data-ttu-id="c30bb-115">La **classe \_ \_ \_ Cellular02 dei criteri MDM Config01** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="c30bb-115">The **MDM\_Policy\_Config01\_Cellular02** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c30bb-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="c30bb-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c30bb-117">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c30bb-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c30bb-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c30bb-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c30bb-119">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c30bb-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c30bb-120">LetAppsAccessCellularData</span><span class="sxs-lookup"><span data-stu-id="c30bb-120">LetAppsAccessCellularData</span></span>](/windows/client-management/mdm/policy-csp-cellular#cellular-letappsaccesscellulardata)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c30bb-121">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c30bb-121">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c30bb-122">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="c30bb-122">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c30bb-123">\_ForceAllowTheseApps LetAppsAccessCellularData</span><span class="sxs-lookup"><span data-stu-id="c30bb-123">LetAppsAccessCellularData\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-cellular#cellular-letappsaccesscellulardata-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c30bb-124">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c30bb-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c30bb-125">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="c30bb-125">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c30bb-126">\_ForceDenyTheseApps LetAppsAccessCellularData</span><span class="sxs-lookup"><span data-stu-id="c30bb-126">LetAppsAccessCellularData\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-cellular#cellular-letappsaccesscellulardata-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c30bb-127">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c30bb-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c30bb-128">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="c30bb-128">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c30bb-129">\_UserInControlOfTheseApps LetAppsAccessCellularData</span><span class="sxs-lookup"><span data-stu-id="c30bb-129">LetAppsAccessCellularData\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-cellular#cellular-letappsaccesscellulardata-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c30bb-130">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c30bb-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c30bb-131">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="c30bb-131">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c30bb-132">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="c30bb-132">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c30bb-133">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c30bb-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c30bb-134">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c30bb-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c30bb-135">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c30bb-135">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c30bb-136">ShowAppCellularAccessUI</span><span class="sxs-lookup"><span data-stu-id="c30bb-136">ShowAppCellularAccessUI</span></span>](/windows/client-management/mdm/policy-csp-cellular#cellular-showappcellularaccessui)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c30bb-137">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c30bb-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c30bb-138">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="c30bb-138">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c30bb-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c30bb-139">Requirements</span></span>



| <span data-ttu-id="c30bb-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="c30bb-140">Requirement</span></span> | <span data-ttu-id="c30bb-141">Valore</span><span class="sxs-lookup"><span data-stu-id="c30bb-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c30bb-142">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c30bb-142">Minimum supported client</span></span><br/> | <span data-ttu-id="c30bb-143">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="c30bb-143">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c30bb-144">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c30bb-144">Minimum supported server</span></span><br/> | <span data-ttu-id="c30bb-145">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="c30bb-145">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="c30bb-146">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="c30bb-146">Namespace</span></span><br/>                | <span data-ttu-id="c30bb-147">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="c30bb-147">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="c30bb-148">MOF</span><span class="sxs-lookup"><span data-stu-id="c30bb-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c30bb-149"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c30bb-149"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="c30bb-150">DLL</span><span class="sxs-lookup"><span data-stu-id="c30bb-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c30bb-151"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c30bb-151"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

