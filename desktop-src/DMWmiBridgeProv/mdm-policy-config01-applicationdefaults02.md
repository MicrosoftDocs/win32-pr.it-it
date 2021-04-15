---
title: Classe MDM_Policy_Config01_ApplicationDefaults02
description: La \_ \_ \_ classe Config01 APPLICATIONDEFAULTS02 di criteri MDM consente a un amministratore di impostare il tipo di file e le associazioni di protocollo predefiniti. Se impostato, le associazioni predefinite verranno applicate all'accesso al PC.
ms.assetid: 01a45151-bce3-47a7-bffe-1a3f5a1348ff
keywords:
- Classe MDM_Policy_Config01_ApplicationDefaults02
- Classe MDM_Policy_Config01_ApplicationDefaults02, descritta
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_ApplicationDefaults02
- MDM_Policy_Config01_ApplicationDefaults02.InstanceID
- MDM_Policy_Config01_ApplicationDefaults02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 246278b1e4185337ebb63d9d23f74e2ff8753615
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476036"
---
# <a name="mdm_policy_config01_applicationdefaults02-class"></a><span data-ttu-id="14885-106">\_ \_ Classe Config01 ApplicationDefaults02 di criteri \_ MDM</span><span class="sxs-lookup"><span data-stu-id="14885-106">MDM\_Policy\_Config01\_ApplicationDefaults02 class</span></span>

<span data-ttu-id="14885-107">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="14885-107">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="14885-108">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="14885-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="14885-109">La \_ \_ \_ classe Config01 APPLICATIONDEFAULTS02 di criteri MDM consente a un amministratore di impostare il tipo di file e le associazioni di protocollo predefiniti.</span><span class="sxs-lookup"><span data-stu-id="14885-109">The MDM\_Policy\_Config01\_ApplicationDefaults02 class allows an administrator to set default file type and protocol associations.</span></span> <span data-ttu-id="14885-110">Se impostato, le associazioni predefinite verranno applicate all'accesso al PC.</span><span class="sxs-lookup"><span data-stu-id="14885-110">When set, default associations will be applied on sign-in to the PC.</span></span>

<span data-ttu-id="14885-111">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="14885-111">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="14885-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="14885-112">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_ApplicationDefaults02
{
  string InstanceID;
  string ParentID;
  string DefaultAssociationsConfiguration;
};
```

## <a name="members"></a><span data-ttu-id="14885-113">Members</span><span class="sxs-lookup"><span data-stu-id="14885-113">Members</span></span>

<span data-ttu-id="14885-114">La **classe \_ \_ Config01 \_ ApplicationDefaults02 dei criteri MDM** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="14885-114">The **MDM\_Policy\_Config01\_ApplicationDefaults02** class has these types of members:</span></span>

-   [<span data-ttu-id="14885-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="14885-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="14885-116">Proprietà</span><span class="sxs-lookup"><span data-stu-id="14885-116">Properties</span></span>

<span data-ttu-id="14885-117">La **classe \_ \_ \_ ApplicationDefaults02 dei criteri MDM Config01** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="14885-117">The **MDM\_Policy\_Config01\_ApplicationDefaults02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="14885-118">DefaultAssociationsConfiguration</span><span class="sxs-lookup"><span data-stu-id="14885-118">DefaultAssociationsConfiguration</span></span>](/windows/client-management/mdm/policy-csp-applicationdefaults#applicationdefaults-defaultassociationsconfiguration)
</dt> <dd> <dl> <dt>

<span data-ttu-id="14885-119">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="14885-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="14885-120">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="14885-120">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="14885-121">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="14885-121">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14885-122">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="14885-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="14885-123">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="14885-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14885-124">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="14885-124">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="14885-125">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="14885-125">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14885-126">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="14885-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="14885-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="14885-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14885-128">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="14885-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="14885-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="14885-129">Requirements</span></span>



| <span data-ttu-id="14885-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="14885-130">Requirement</span></span> | <span data-ttu-id="14885-131">Valore</span><span class="sxs-lookup"><span data-stu-id="14885-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="14885-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="14885-132">Minimum supported client</span></span><br/> | <span data-ttu-id="14885-133">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="14885-133">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="14885-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="14885-134">Minimum supported server</span></span><br/> | <span data-ttu-id="14885-135">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="14885-135">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="14885-136">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="14885-136">Namespace</span></span><br/>                | <span data-ttu-id="14885-137">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="14885-137">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="14885-138">MOF</span><span class="sxs-lookup"><span data-stu-id="14885-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="14885-139"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="14885-139"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="14885-140">DLL</span><span class="sxs-lookup"><span data-stu-id="14885-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="14885-141"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="14885-141"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

