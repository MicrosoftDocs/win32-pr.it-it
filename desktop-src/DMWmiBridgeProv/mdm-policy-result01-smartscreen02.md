---
title: Classe MDM_Policy_Result01_SmartScreen02
description: La \_ classe SmartScreen02 dei criteri MDM \_ Result01 \_ rappresenta i criteri della Smart Screen.
ms.assetid: 9a775712-ce42-48c2-b286-eaf7ca8fed20
keywords:
- Classe MDM_Policy_Result01_SmartScreen02
- Classe MDM_Policy_Result01_SmartScreen02, descritta
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_SmartScreen02
- MDM_Policy_Result01_SmartScreen02.InstanceID
- MDM_Policy_Result01_SmartScreen02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03a49aad764492c54b43327cfb71c0c93fa36870
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121470"
---
# <a name="mdm_policy_result01_smartscreen02-class"></a><span data-ttu-id="e13ee-105">\_ \_ Classe Result01 SmartScreen02 di criteri \_ MDM</span><span class="sxs-lookup"><span data-stu-id="e13ee-105">MDM\_Policy\_Result01\_SmartScreen02 class</span></span>

<span data-ttu-id="e13ee-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="e13ee-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="e13ee-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="e13ee-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="e13ee-108">la \_ classe SmartScreen02 dei criteri MDM \_ Result01 \_ rappresenta i criteri della Smart Screen.</span><span class="sxs-lookup"><span data-stu-id="e13ee-108">the MDM\_Policy\_Result01\_SmartScreen02 class represents the smart screen policies.</span></span>

<span data-ttu-id="e13ee-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="e13ee-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e13ee-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e13ee-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_SmartScreen02
{
  string InstanceID;
  string ParentID;
  sint32 EnableAppInstallControl;
  sint32 EnableSmartScreenInShell;
  sint32 PreventOverrideForFilesInShell;
};
```

## <a name="members"></a><span data-ttu-id="e13ee-111">Members</span><span class="sxs-lookup"><span data-stu-id="e13ee-111">Members</span></span>

<span data-ttu-id="e13ee-112">La **classe \_ \_ Result01 \_ SmartScreen02 dei criteri MDM** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="e13ee-112">The **MDM\_Policy\_Result01\_SmartScreen02** class has these types of members:</span></span>

-   [<span data-ttu-id="e13ee-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e13ee-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e13ee-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e13ee-114">Properties</span></span>

<span data-ttu-id="e13ee-115">La **classe \_ \_ \_ SmartScreen02 dei criteri MDM Result01** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="e13ee-115">The **MDM\_Policy\_Result01\_SmartScreen02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="e13ee-116">EnableAppInstallControl</span><span class="sxs-lookup"><span data-stu-id="e13ee-116">EnableAppInstallControl</span></span>](/windows/client-management/mdm/policy-csp-smartscreen#smartscreen-enableappinstallcontrol)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e13ee-117">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="e13ee-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e13ee-118">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="e13ee-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e13ee-119">EnableSmartScreenInShell</span><span class="sxs-lookup"><span data-stu-id="e13ee-119">EnableSmartScreenInShell</span></span>](/windows/client-management/mdm/policy-csp-smartscreen#smartscreen-enablesmartscreeninshell)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e13ee-120">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="e13ee-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e13ee-121">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="e13ee-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e13ee-122">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="e13ee-122">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e13ee-123">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e13ee-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e13ee-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e13ee-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e13ee-125">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e13ee-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e13ee-126">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="e13ee-126">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e13ee-127">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e13ee-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e13ee-128">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e13ee-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e13ee-129">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e13ee-129">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e13ee-130">PreventOverrideForFilesInShell</span><span class="sxs-lookup"><span data-stu-id="e13ee-130">PreventOverrideForFilesInShell</span></span>](/windows/client-management/mdm/policy-csp-smartscreen#smartscreen-preventoverrideforfilesinshell)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e13ee-131">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="e13ee-131">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e13ee-132">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="e13ee-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e13ee-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e13ee-133">Requirements</span></span>



| <span data-ttu-id="e13ee-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="e13ee-134">Requirement</span></span> | <span data-ttu-id="e13ee-135">Valore</span><span class="sxs-lookup"><span data-stu-id="e13ee-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e13ee-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e13ee-136">Minimum supported client</span></span><br/> | <span data-ttu-id="e13ee-137">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="e13ee-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e13ee-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e13ee-138">Minimum supported server</span></span><br/> | <span data-ttu-id="e13ee-139">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="e13ee-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="e13ee-140">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="e13ee-140">Namespace</span></span><br/>                | <span data-ttu-id="e13ee-141">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="e13ee-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="e13ee-142">MOF</span><span class="sxs-lookup"><span data-stu-id="e13ee-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e13ee-143"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e13ee-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="e13ee-144">DLL</span><span class="sxs-lookup"><span data-stu-id="e13ee-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e13ee-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e13ee-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

