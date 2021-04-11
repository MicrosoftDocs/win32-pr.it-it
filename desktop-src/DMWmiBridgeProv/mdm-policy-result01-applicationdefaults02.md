---
title: Classe MDM_Policy_Result01_ApplicationDefaults02
description: La \_ \_ classe Result01 ApplicationDefaults02 dei criteri MDM \_ rappresenta i criteri predefiniti dell'applicazione disponibili.
ms.assetid: bf7df9a1-7af1-49a6-9456-3e6ec48234e2
keywords:
- Classe MDM_Policy_Result01_ApplicationDefaults02
- Classe MDM_Policy_Result01_ApplicationDefaults02, descritta
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_ApplicationDefaults02
- MDM_Policy_Result01_ApplicationDefaults02.InstanceID
- MDM_Policy_Result01_ApplicationDefaults02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10592ceb4e4f401ce9f64c24ef207a4e2e033e9c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119907"
---
# <a name="mdm_policy_result01_applicationdefaults02-class"></a><span data-ttu-id="69086-105">\_ \_ Classe Result01 ApplicationDefaults02 di criteri \_ MDM</span><span class="sxs-lookup"><span data-stu-id="69086-105">MDM\_Policy\_Result01\_ApplicationDefaults02 class</span></span>

<span data-ttu-id="69086-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="69086-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="69086-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="69086-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="69086-108">La \_ \_ classe Result01 ApplicationDefaults02 dei criteri MDM \_ rappresenta i criteri predefiniti dell'applicazione disponibili.</span><span class="sxs-lookup"><span data-stu-id="69086-108">The MDM\_Policy\_Result01\_ApplicationDefaults02 class represents the available application defaults policies.</span></span>

<span data-ttu-id="69086-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="69086-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="69086-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="69086-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_ApplicationDefaults02
{
  string InstanceID;
  string ParentID;
  string DefaultAssociationsConfiguration;
};
```

## <a name="members"></a><span data-ttu-id="69086-111">Members</span><span class="sxs-lookup"><span data-stu-id="69086-111">Members</span></span>

<span data-ttu-id="69086-112">La **classe \_ \_ Result01 \_ ApplicationDefaults02 dei criteri MDM** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="69086-112">The **MDM\_Policy\_Result01\_ApplicationDefaults02** class has these types of members:</span></span>

-   [<span data-ttu-id="69086-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="69086-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="69086-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="69086-114">Properties</span></span>

<span data-ttu-id="69086-115">La **classe \_ \_ \_ ApplicationDefaults02 dei criteri MDM Result01** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="69086-115">The **MDM\_Policy\_Result01\_ApplicationDefaults02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="69086-116">DefaultAssociationsConfiguration</span><span class="sxs-lookup"><span data-stu-id="69086-116">DefaultAssociationsConfiguration</span></span>](/windows/client-management/mdm/policy-csp-applicationdefaults#applicationdefaults-defaultassociationsconfiguration)
</dt> <dd> <dl> <dt>

<span data-ttu-id="69086-117">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="69086-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="69086-118">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="69086-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="69086-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="69086-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69086-120">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="69086-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="69086-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="69086-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="69086-122">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="69086-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="69086-123">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="69086-123">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69086-124">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="69086-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="69086-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="69086-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="69086-126">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="69086-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="69086-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="69086-127">Requirements</span></span>



| <span data-ttu-id="69086-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="69086-128">Requirement</span></span> | <span data-ttu-id="69086-129">Valore</span><span class="sxs-lookup"><span data-stu-id="69086-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="69086-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="69086-130">Minimum supported client</span></span><br/> | <span data-ttu-id="69086-131">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="69086-131">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="69086-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="69086-132">Minimum supported server</span></span><br/> | <span data-ttu-id="69086-133">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="69086-133">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="69086-134">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="69086-134">Namespace</span></span><br/>                | <span data-ttu-id="69086-135">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="69086-135">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="69086-136">MOF</span><span class="sxs-lookup"><span data-stu-id="69086-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="69086-137"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="69086-137"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="69086-138">DLL</span><span class="sxs-lookup"><span data-stu-id="69086-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="69086-139"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="69086-139"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

