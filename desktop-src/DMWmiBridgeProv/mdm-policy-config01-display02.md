---
title: Classe MDM_Policy_Config01_Display02
description: La \_ \_ classe Config01 Display02 dei criteri MDM \_ Configura i criteri di visualizzazione.
ms.assetid: 106eecc5-ede0-4d66-ba51-967a8f7bcb66
keywords:
- Classe MDM_Policy_Config01_Display02
- Classe MDM_Policy_Config01_Display02, descritta
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Display02
- MDM_Policy_Config01_Display02.InstanceID
- MDM_Policy_Config01_Display02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15e79861a911d03f1d9174053dc8ec7c62824fd9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119411"
---
# <a name="mdm_policy_config01_display02-class"></a><span data-ttu-id="1a546-105">\_ \_ Classe Config01 Display02 di criteri \_ MDM</span><span class="sxs-lookup"><span data-stu-id="1a546-105">MDM\_Policy\_Config01\_Display02 class</span></span>

<span data-ttu-id="1a546-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="1a546-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="1a546-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="1a546-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="1a546-108">La \_ \_ classe Config01 Display02 dei criteri MDM \_ Configura i criteri di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="1a546-108">The MDM\_Policy\_Config01\_Display02 class configures the display policies.</span></span>

<span data-ttu-id="1a546-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="1a546-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a546-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1a546-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Display02
{
  string InstanceID;
  string ParentID;
  string TurnOffGdiDPIScalingForApps;
  string TurnOnGdiDPIScalingForApps;
};
```

## <a name="members"></a><span data-ttu-id="1a546-111">Members</span><span class="sxs-lookup"><span data-stu-id="1a546-111">Members</span></span>

<span data-ttu-id="1a546-112">La **classe \_ \_ Config01 \_ Display02 dei criteri MDM** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="1a546-112">The **MDM\_Policy\_Config01\_Display02** class has these types of members:</span></span>

-   [<span data-ttu-id="1a546-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="1a546-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1a546-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="1a546-114">Properties</span></span>

<span data-ttu-id="1a546-115">La **classe \_ \_ \_ Display02 dei criteri MDM Config01** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="1a546-115">The **MDM\_Policy\_Config01\_Display02** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1a546-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="1a546-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a546-117">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1a546-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1a546-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1a546-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1a546-119">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="1a546-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1a546-120">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="1a546-120">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a546-121">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1a546-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1a546-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1a546-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1a546-123">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="1a546-123">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1a546-124">TurnOffGdiDPIScalingForApps</span><span class="sxs-lookup"><span data-stu-id="1a546-124">TurnOffGdiDPIScalingForApps</span></span>](/windows/client-management/mdm/policy-csp-display#display-turnoffgdidpiscalingforapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a546-125">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1a546-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1a546-126">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="1a546-126">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1a546-127">TurnOnGdiDPIScalingForApps</span><span class="sxs-lookup"><span data-stu-id="1a546-127">TurnOnGdiDPIScalingForApps</span></span>](/windows/client-management/mdm/policy-csp-display#display-turnongdidpiscalingforapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a546-128">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1a546-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1a546-129">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="1a546-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1a546-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1a546-130">Requirements</span></span>



| <span data-ttu-id="1a546-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="1a546-131">Requirement</span></span> | <span data-ttu-id="1a546-132">Valore</span><span class="sxs-lookup"><span data-stu-id="1a546-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a546-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1a546-133">Minimum supported client</span></span><br/> | <span data-ttu-id="1a546-134">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="1a546-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1a546-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1a546-135">Minimum supported server</span></span><br/> | <span data-ttu-id="1a546-136">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="1a546-136">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="1a546-137">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="1a546-137">Namespace</span></span><br/>                | <span data-ttu-id="1a546-138">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="1a546-138">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="1a546-139">MOF</span><span class="sxs-lookup"><span data-stu-id="1a546-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1a546-140"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1a546-140"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="1a546-141">DLL</span><span class="sxs-lookup"><span data-stu-id="1a546-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1a546-142"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1a546-142"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

