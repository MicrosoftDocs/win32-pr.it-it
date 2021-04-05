---
title: Classe MDM_Policy_Result01_ActiveXControls02
description: La \_ classe ActiveXControls02 dei criteri MDM \_ Result01 \_ rappresenta i criteri di controllo ActiveX disponibili.
ms.assetid: 46778743-59d7-4d37-836c-3f263bb8a083
keywords:
- Classe MDM_Policy_Result01_ActiveXControls02
- Classe MDM_Policy_Result01_ActiveXControls02, descritta
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_ActiveXControls02
- MDM_Policy_Result01_ActiveXControls02.InstanceID
- MDM_Policy_Result01_ActiveXControls02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36ee572cfbbd823ce9e819688d9399b22f5d564c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048414"
---
# <a name="mdm_policy_result01_activexcontrols02-class"></a><span data-ttu-id="6bd61-105">\_ \_ Classe Result01 ActiveXControls02 di criteri \_ MDM</span><span class="sxs-lookup"><span data-stu-id="6bd61-105">MDM\_Policy\_Result01\_ActiveXControls02 class</span></span>

<span data-ttu-id="6bd61-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="6bd61-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="6bd61-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="6bd61-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="6bd61-108">La \_ classe ActiveXControls02 dei criteri MDM \_ Result01 \_ rappresenta i criteri di controllo ActiveX disponibili.</span><span class="sxs-lookup"><span data-stu-id="6bd61-108">The MDM\_Policy\_Result01\_ActiveXControls02 class represents the available ActiveX Controls policies.</span></span>

<span data-ttu-id="6bd61-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="6bd61-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="6bd61-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6bd61-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_ActiveXControls02
{
  string InstanceID;
  string ParentID;
  string ApprovedInstallationSites;
};
```

## <a name="members"></a><span data-ttu-id="6bd61-111">Members</span><span class="sxs-lookup"><span data-stu-id="6bd61-111">Members</span></span>

<span data-ttu-id="6bd61-112">La **classe \_ \_ Result01 \_ ActiveXControls02 dei criteri MDM** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="6bd61-112">The **MDM\_Policy\_Result01\_ActiveXControls02** class has these types of members:</span></span>

-   [<span data-ttu-id="6bd61-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="6bd61-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6bd61-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="6bd61-114">Properties</span></span>

<span data-ttu-id="6bd61-115">La **classe \_ \_ \_ ActiveXControls02 dei criteri MDM Result01** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="6bd61-115">The **MDM\_Policy\_Result01\_ActiveXControls02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="6bd61-116">ApprovedInstallationSites</span><span class="sxs-lookup"><span data-stu-id="6bd61-116">ApprovedInstallationSites</span></span>](/windows/client-management/mdm/policy-csp-activexcontrols#activexcontrols-approvedinstallationsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bd61-117">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6bd61-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6bd61-118">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="6bd61-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="6bd61-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="6bd61-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bd61-120">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6bd61-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6bd61-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6bd61-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6bd61-122">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="6bd61-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="6bd61-123">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="6bd61-123">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6bd61-124">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6bd61-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6bd61-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6bd61-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6bd61-126">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="6bd61-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6bd61-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6bd61-127">Requirements</span></span>



| <span data-ttu-id="6bd61-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="6bd61-128">Requirement</span></span> | <span data-ttu-id="6bd61-129">Valore</span><span class="sxs-lookup"><span data-stu-id="6bd61-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6bd61-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6bd61-130">Minimum supported client</span></span><br/> | <span data-ttu-id="6bd61-131">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="6bd61-131">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6bd61-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6bd61-132">Minimum supported server</span></span><br/> | <span data-ttu-id="6bd61-133">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="6bd61-133">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="6bd61-134">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="6bd61-134">Namespace</span></span><br/>                | <span data-ttu-id="6bd61-135">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="6bd61-135">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="6bd61-136">MOF</span><span class="sxs-lookup"><span data-stu-id="6bd61-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6bd61-137"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6bd61-137"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="6bd61-138">DLL</span><span class="sxs-lookup"><span data-stu-id="6bd61-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6bd61-139"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6bd61-139"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

