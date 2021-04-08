---
title: Classe MDM_Policy_Config01_DeviceGuard02
description: Il \_ criterio MDM \_ Config01 \_ DeviceGuard02 configura i criteri di Device Guard.
ms.assetid: b8edf906-2486-4d8d-9410-d216bacf1728
keywords:
- Classe MDM_Policy_Config01_DeviceGuard02
- Classe MDM_Policy_Config01_DeviceGuard02, descritta
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_DeviceGuard02
- MDM_Policy_Config01_DeviceGuard02.InstanceID
- MDM_Policy_Config01_DeviceGuard02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ebcc8f3d929708cdff3ada8fe440f49a1aeb1ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047911"
---
# <a name="mdm_policy_config01_deviceguard02-class"></a><span data-ttu-id="2751a-105">\_ \_ Classe Config01 DeviceGuard02 di criteri \_ MDM</span><span class="sxs-lookup"><span data-stu-id="2751a-105">MDM\_Policy\_Config01\_DeviceGuard02 class</span></span>

<span data-ttu-id="2751a-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="2751a-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="2751a-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="2751a-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="2751a-108">Il \_ criterio MDM \_ Config01 \_ DeviceGuard02 configura i criteri di Device Guard.</span><span class="sxs-lookup"><span data-stu-id="2751a-108">The MDM\_Policy\_Config01\_DeviceGuard02 configures the Device Guard policies.</span></span>

<span data-ttu-id="2751a-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="2751a-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="2751a-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2751a-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_DeviceGuard02
{
  string InstanceID;
  string ParentID;
  sint32 EnableVirtualizationBasedSecurity;
  sint32 LsaCfgFlags;
  sint32 RequirePlatformSecurityFeatures;
};
```

## <a name="members"></a><span data-ttu-id="2751a-111">Members</span><span class="sxs-lookup"><span data-stu-id="2751a-111">Members</span></span>

<span data-ttu-id="2751a-112">La **classe \_ \_ Config01 \_ DeviceGuard02 dei criteri MDM** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="2751a-112">The **MDM\_Policy\_Config01\_DeviceGuard02** class has these types of members:</span></span>

-   [<span data-ttu-id="2751a-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2751a-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2751a-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2751a-114">Properties</span></span>

<span data-ttu-id="2751a-115">La **classe \_ \_ \_ DeviceGuard02 dei criteri MDM Config01** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="2751a-115">The **MDM\_Policy\_Config01\_DeviceGuard02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="2751a-116">EnableVirtualizationBasedSecurity</span><span class="sxs-lookup"><span data-stu-id="2751a-116">EnableVirtualizationBasedSecurity</span></span>](/windows/client-management/mdm/policy-csp-deviceguard#deviceguard-enablevirtualizationbasedsecurity)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2751a-117">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="2751a-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2751a-118">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="2751a-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2751a-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="2751a-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2751a-120">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2751a-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2751a-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2751a-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2751a-122">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="2751a-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2751a-123">LsaCfgFlags</span><span class="sxs-lookup"><span data-stu-id="2751a-123">LsaCfgFlags</span></span>](/windows/client-management/mdm/policy-csp-deviceguard#deviceguard-lsacfgflags)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2751a-124">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="2751a-124">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2751a-125">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="2751a-125">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2751a-126">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="2751a-126">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2751a-127">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2751a-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2751a-128">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2751a-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2751a-129">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="2751a-129">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2751a-130">RequirePlatformSecurityFeatures</span><span class="sxs-lookup"><span data-stu-id="2751a-130">RequirePlatformSecurityFeatures</span></span>](/windows/client-management/mdm/policy-csp-deviceguard#deviceguard-requireplatformsecurityfeatures)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2751a-131">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="2751a-131">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2751a-132">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="2751a-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2751a-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2751a-133">Requirements</span></span>



| <span data-ttu-id="2751a-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="2751a-134">Requirement</span></span> | <span data-ttu-id="2751a-135">Valore</span><span class="sxs-lookup"><span data-stu-id="2751a-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2751a-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2751a-136">Minimum supported client</span></span><br/> | <span data-ttu-id="2751a-137">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="2751a-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2751a-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2751a-138">Minimum supported server</span></span><br/> | <span data-ttu-id="2751a-139">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="2751a-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="2751a-140">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="2751a-140">Namespace</span></span><br/>                | <span data-ttu-id="2751a-141">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="2751a-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="2751a-142">MOF</span><span class="sxs-lookup"><span data-stu-id="2751a-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2751a-143"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2751a-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="2751a-144">DLL</span><span class="sxs-lookup"><span data-stu-id="2751a-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2751a-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2751a-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

