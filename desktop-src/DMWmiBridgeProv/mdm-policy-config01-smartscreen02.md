---
title: Classe MDM_Policy_Config01_SmartScreen02
description: La \_ \_ classe Config01 SmartScreen02 dei criteri MDM \_ Configura i criteri della Smart Screen.
ms.assetid: e5ad04a1-afa9-4887-a4c1-c92c574a5398
keywords:
- Classe MDM_Policy_Config01_SmartScreen02
- Classe MDM_Policy_Config01_SmartScreen02, descritta
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_SmartScreen02
- MDM_Policy_Config01_SmartScreen02.InstanceID
- MDM_Policy_Config01_SmartScreen02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09e0b8ca0c1e53005ab2a2ab80cce3f18dec40b0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048416"
---
# <a name="mdm_policy_config01_smartscreen02-class"></a><span data-ttu-id="b8dcc-105">\_ \_ Classe Config01 SmartScreen02 di criteri \_ MDM</span><span class="sxs-lookup"><span data-stu-id="b8dcc-105">MDM\_Policy\_Config01\_SmartScreen02 class</span></span>

<span data-ttu-id="b8dcc-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="b8dcc-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="b8dcc-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="b8dcc-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="b8dcc-108">La \_ \_ classe Config01 SmartScreen02 dei criteri MDM \_ Configura i criteri della Smart Screen.</span><span class="sxs-lookup"><span data-stu-id="b8dcc-108">The MDM\_Policy\_Config01\_SmartScreen02 class configures the smart screen policies.</span></span>

<span data-ttu-id="b8dcc-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="b8dcc-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8dcc-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b8dcc-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_SmartScreen02
{
  string InstanceID;
  string ParentID;
  sint32 EnableAppInstallControl;
  sint32 EnableSmartScreenInShell;
  sint32 PreventOverrideForFilesInShell;
};
```

## <a name="members"></a><span data-ttu-id="b8dcc-111">Members</span><span class="sxs-lookup"><span data-stu-id="b8dcc-111">Members</span></span>

<span data-ttu-id="b8dcc-112">La **classe \_ \_ Config01 \_ SmartScreen02 dei criteri MDM** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="b8dcc-112">The **MDM\_Policy\_Config01\_SmartScreen02** class has these types of members:</span></span>

-   [<span data-ttu-id="b8dcc-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b8dcc-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b8dcc-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b8dcc-114">Properties</span></span>

<span data-ttu-id="b8dcc-115">La **classe \_ \_ \_ SmartScreen02 dei criteri MDM Config01** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="b8dcc-115">The **MDM\_Policy\_Config01\_SmartScreen02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="b8dcc-116">EnableAppInstallControl</span><span class="sxs-lookup"><span data-stu-id="b8dcc-116">EnableAppInstallControl</span></span>](/windows/client-management/mdm/policy-csp-smartscreen#smartscreen-enableappinstallcontrol)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8dcc-117">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b8dcc-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b8dcc-118">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b8dcc-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b8dcc-119">EnableSmartScreenInShell</span><span class="sxs-lookup"><span data-stu-id="b8dcc-119">EnableSmartScreenInShell</span></span>](/windows/client-management/mdm/policy-csp-smartscreen#smartscreen-enablesmartscreeninshell)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8dcc-120">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b8dcc-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b8dcc-121">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b8dcc-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b8dcc-122">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="b8dcc-122">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8dcc-123">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b8dcc-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8dcc-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b8dcc-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8dcc-125">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b8dcc-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b8dcc-126">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="b8dcc-126">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8dcc-127">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b8dcc-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8dcc-128">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b8dcc-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8dcc-129">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b8dcc-129">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b8dcc-130">PreventOverrideForFilesInShell</span><span class="sxs-lookup"><span data-stu-id="b8dcc-130">PreventOverrideForFilesInShell</span></span>](/windows/client-management/mdm/policy-csp-smartscreen#smartscreen-preventoverrideforfilesinshell)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8dcc-131">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b8dcc-131">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b8dcc-132">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b8dcc-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b8dcc-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b8dcc-133">Requirements</span></span>



| <span data-ttu-id="b8dcc-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="b8dcc-134">Requirement</span></span> | <span data-ttu-id="b8dcc-135">Valore</span><span class="sxs-lookup"><span data-stu-id="b8dcc-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8dcc-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b8dcc-136">Minimum supported client</span></span><br/> | <span data-ttu-id="b8dcc-137">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="b8dcc-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b8dcc-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b8dcc-138">Minimum supported server</span></span><br/> | <span data-ttu-id="b8dcc-139">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="b8dcc-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="b8dcc-140">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b8dcc-140">Namespace</span></span><br/>                | <span data-ttu-id="b8dcc-141">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="b8dcc-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="b8dcc-142">MOF</span><span class="sxs-lookup"><span data-stu-id="b8dcc-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b8dcc-143"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b8dcc-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="b8dcc-144">DLL</span><span class="sxs-lookup"><span data-stu-id="b8dcc-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b8dcc-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b8dcc-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

