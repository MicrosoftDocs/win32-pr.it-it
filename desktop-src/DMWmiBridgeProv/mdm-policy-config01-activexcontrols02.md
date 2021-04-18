---
title: Classe MDM_Policy_Config01_ActiveXControls02
description: Questa impostazione dei criteri determina quali siti di installazione ActiveX gli utenti standard dell'organizzazione possono utilizzare per installare i controlli ActiveX nei computer.
ms.assetid: 242888ae-f07a-40b7-9539-29fcca9cfc40
keywords:
- Classe MDM_Policy_Config01_ActiveXControls02
- Classe MDM_Policy_Config01_ActiveXControls02, descritta
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_ActiveXControls02
- MDM_Policy_Config01_ActiveXControls02.InstanceID
- MDM_Policy_Config01_ActiveXControls02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 213edcea47bc0fd3379f753613c5b884963ca781
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301384"
---
# <a name="mdm_policy_config01_activexcontrols02-class"></a><span data-ttu-id="3d5be-105">\_ \_ Classe Config01 ActiveXControls02 di criteri \_ MDM</span><span class="sxs-lookup"><span data-stu-id="3d5be-105">MDM\_Policy\_Config01\_ActiveXControls02 class</span></span>

<span data-ttu-id="3d5be-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="3d5be-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="3d5be-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="3d5be-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="3d5be-108">Questa impostazione dei criteri determina quali siti di installazione ActiveX gli utenti standard dell'organizzazione possono utilizzare per installare i controlli ActiveX nei computer.</span><span class="sxs-lookup"><span data-stu-id="3d5be-108">This policy setting determines which ActiveX installation sites standard users in your organization can use to install ActiveX controls on their computers.</span></span> <span data-ttu-id="3d5be-109">Quando questa impostazione è abilitata, l'amministratore può creare un elenco dei siti di installazione ActiveX approvati specificati dall'URL host.</span><span class="sxs-lookup"><span data-stu-id="3d5be-109">When this setting is enabled, the administrator can create a list of approved Activex Install sites specified by host URL.</span></span>

<span data-ttu-id="3d5be-110">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="3d5be-110">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d5be-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3d5be-111">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_ActiveXControls02
{
  string InstanceID;
  string ParentID;
  string ApprovedInstallationSites;
};
```

## <a name="members"></a><span data-ttu-id="3d5be-112">Members</span><span class="sxs-lookup"><span data-stu-id="3d5be-112">Members</span></span>

<span data-ttu-id="3d5be-113">La **classe \_ \_ Config01 \_ ActiveXControls02 dei criteri MDM** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="3d5be-113">The **MDM\_Policy\_Config01\_ActiveXControls02** class has these types of members:</span></span>

-   [<span data-ttu-id="3d5be-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="3d5be-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3d5be-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="3d5be-115">Properties</span></span>

<span data-ttu-id="3d5be-116">La **classe \_ \_ \_ ActiveXControls02 dei criteri MDM Config01** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="3d5be-116">The **MDM\_Policy\_Config01\_ActiveXControls02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="3d5be-117">ApprovedInstallationSites</span><span class="sxs-lookup"><span data-stu-id="3d5be-117">ApprovedInstallationSites</span></span>](/windows/client-management/mdm/policy-csp-activexcontrols#activexcontrols-approvedinstallationsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d5be-118">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3d5be-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3d5be-119">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="3d5be-119">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3d5be-120">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="3d5be-120">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d5be-121">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3d5be-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3d5be-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3d5be-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3d5be-123">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="3d5be-123">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3d5be-124">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="3d5be-124">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d5be-125">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3d5be-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3d5be-126">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3d5be-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3d5be-127">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="3d5be-127">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3d5be-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3d5be-128">Requirements</span></span>



| <span data-ttu-id="3d5be-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="3d5be-129">Requirement</span></span> | <span data-ttu-id="3d5be-130">Valore</span><span class="sxs-lookup"><span data-stu-id="3d5be-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d5be-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3d5be-131">Minimum supported client</span></span><br/> | <span data-ttu-id="3d5be-132">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="3d5be-132">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3d5be-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3d5be-133">Minimum supported server</span></span><br/> | <span data-ttu-id="3d5be-134">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="3d5be-134">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="3d5be-135">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="3d5be-135">Namespace</span></span><br/>                | <span data-ttu-id="3d5be-136">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="3d5be-136">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="3d5be-137">MOF</span><span class="sxs-lookup"><span data-stu-id="3d5be-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3d5be-138"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3d5be-138"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="3d5be-139">DLL</span><span class="sxs-lookup"><span data-stu-id="3d5be-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3d5be-140"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3d5be-140"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

