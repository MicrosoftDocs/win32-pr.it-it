---
title: Classe MDM_WindowsAdvancedThreatProtection_DeviceTagging01
description: La \_ classe MDM WindowsAdvancedThreatProtection \_ DeviceTagging01 viene usata per eseguire l'onboarding, determinare lo stato di integrità e configurazione ed endpoint offboard per Windows Defender Advanced Threat Protection.
ms.assetid: b56d5d46-e994-404a-865a-c59bb948f2b3
keywords:
- Classe MDM_WindowsAdvancedThreatProtection_DeviceTagging01
- Classe MDM_WindowsAdvancedThreatProtection_DeviceTagging01, descritta
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MDM_WindowsAdvancedThreatProtection_DeviceTagging01
- MDM_WindowsAdvancedThreatProtection_DeviceTagging01.InstanceID
- MDM_WindowsAdvancedThreatProtection_DeviceTagging01.ParentID
- MDM_WindowsAdvancedThreatProtection_DeviceTagging01.IdMethod
api_type:
- DllExport
api_location:
- DMWmiBridgeProv.dll
ms.openlocfilehash: 12cf3863ba67f422b42572a6934807d86abbc0e0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120614"
---
# <a name="mdm_windowsadvancedthreatprotection_devicetagging01-class"></a><span data-ttu-id="06946-105">\_Classe MDM WindowsAdvancedThreatProtection \_ DeviceTagging01</span><span class="sxs-lookup"><span data-stu-id="06946-105">MDM\_WindowsAdvancedThreatProtection\_DeviceTagging01 class</span></span>

<span data-ttu-id="06946-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="06946-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="06946-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="06946-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="06946-108">La \_ classe MDM WindowsAdvancedThreatProtection \_ DeviceTagging01 viene usata per eseguire l'onboarding, determinare lo stato di integrità e configurazione ed endpoint offboard per Windows Defender Advanced Threat Protection.</span><span class="sxs-lookup"><span data-stu-id="06946-108">The MDM\_WindowsAdvancedThreatProtection\_DeviceTagging01 class is used to onboard, determine configuration and health status, and offboard endpoints for Windows Defender Advanced Threat Protection.</span></span>

<span data-ttu-id="06946-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="06946-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="06946-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="06946-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_WindowsAdvancedThreatProtection_DeviceTagging01
{
  string InstanceID;
  string ParentID;
  string Group;
  sint32 Criticality;
  sint32 IdMethod;
};
```

## <a name="members"></a><span data-ttu-id="06946-111">Members</span><span class="sxs-lookup"><span data-stu-id="06946-111">Members</span></span>

<span data-ttu-id="06946-112">La classe **MDM \_ WindowsAdvancedThreatProtection \_ DeviceTagging01** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="06946-112">The **MDM\_WindowsAdvancedThreatProtection\_DeviceTagging01** class has these types of members:</span></span>

-   [<span data-ttu-id="06946-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="06946-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="06946-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="06946-114">Properties</span></span>

<span data-ttu-id="06946-115">La classe **MDM \_ WindowsAdvancedThreatProtection \_ DeviceTagging01** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="06946-115">The **MDM\_WindowsAdvancedThreatProtection\_DeviceTagging01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="06946-116">Criticità</span><span class="sxs-lookup"><span data-stu-id="06946-116">Criticality</span></span>](/windows/client-management/mdm/windowsadvancedthreatprotection-csp#criticality)
</dt> <dd> <dl> <dt>

<span data-ttu-id="06946-117">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="06946-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="06946-118">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="06946-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="06946-119">Gruppo</span><span class="sxs-lookup"><span data-stu-id="06946-119">Group</span></span>](/windows/client-management/mdm/windowsadvancedthreatprotection-csp#group)
</dt> <dd> <dl> <dt>

<span data-ttu-id="06946-120">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="06946-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06946-121">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="06946-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="06946-122">**IdMethod**</span><span class="sxs-lookup"><span data-stu-id="06946-122">**IdMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06946-123">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="06946-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="06946-124">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="06946-124">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="06946-125">TBD</span><span class="sxs-lookup"><span data-stu-id="06946-125">TBD</span></span>

</dd> <dt>

<span data-ttu-id="06946-126">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="06946-126">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06946-127">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="06946-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06946-128">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="06946-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06946-129">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="06946-129">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="06946-130">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="06946-130">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06946-131">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="06946-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06946-132">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="06946-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06946-133">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="06946-133">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="06946-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="06946-134">Requirements</span></span>



| <span data-ttu-id="06946-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="06946-135">Requirement</span></span> | <span data-ttu-id="06946-136">Valore</span><span class="sxs-lookup"><span data-stu-id="06946-136">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06946-137">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="06946-137">Minimum supported client</span></span><br/> | <span data-ttu-id="06946-138">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="06946-138">Windows 10 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="06946-139">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="06946-139">Minimum supported server</span></span><br/> | <span data-ttu-id="06946-140">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="06946-140">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="06946-141">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="06946-141">Namespace</span></span><br/>                | <span data-ttu-id="06946-142">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="06946-142">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                              |
| <span data-ttu-id="06946-143">MOF</span><span class="sxs-lookup"><span data-stu-id="06946-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="06946-144"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="06946-144"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl> |
| <span data-ttu-id="06946-145">DLL</span><span class="sxs-lookup"><span data-stu-id="06946-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="06946-146"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="06946-146"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl>  |



 

