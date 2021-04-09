---
title: Classe MDM_Firewall_App04
description: La \_ classe App04 del firewall MDM \_ viene usata per configurare le impostazioni di Windows Defender Firewall.
ms.assetid: d7844d89-97d3-43b4-85af-c9464d475167
keywords:
- Classe MDM_Firewall_App04
- Classe MDM_Firewall_App04, descritta
topic_type:
- apiref
api_name:
- MDM_Firewall_App04
- MDM_Firewall_App04.InstanceID
- MDM_Firewall_App04.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00a8558fb2834ba9b0143d644cf4922aa9a710d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119442"
---
# <a name="mdm_firewall_app04-class"></a><span data-ttu-id="3ae14-105">\_Classe App04 del firewall MDM \_</span><span class="sxs-lookup"><span data-stu-id="3ae14-105">MDM\_Firewall\_App04 class</span></span>

<span data-ttu-id="3ae14-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="3ae14-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="3ae14-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="3ae14-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="3ae14-108">La \_ classe App04 del firewall MDM \_ viene usata per configurare le impostazioni di Windows Defender Firewall.</span><span class="sxs-lookup"><span data-stu-id="3ae14-108">The MDM\_Firewall\_App04 class is used to configure the Windows Defender Firewall settings.</span></span>

<span data-ttu-id="3ae14-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="3ae14-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ae14-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3ae14-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Firewall_App04
{
  string InstanceID;
  string ParentID;
  string PackageFamilyName;
  string FilePath;
  string Fqbn;
  string ServiceName;
};
```

## <a name="members"></a><span data-ttu-id="3ae14-111">Members</span><span class="sxs-lookup"><span data-stu-id="3ae14-111">Members</span></span>

<span data-ttu-id="3ae14-112">La **classe \_ \_ App04 del firewall MDM** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="3ae14-112">The **MDM\_Firewall\_App04** class has these types of members:</span></span>

-   [<span data-ttu-id="3ae14-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="3ae14-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3ae14-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="3ae14-114">Properties</span></span>

<span data-ttu-id="3ae14-115">La **classe \_ \_ App04 del firewall MDM** presenta queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="3ae14-115">The **MDM\_Firewall\_App04** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="3ae14-116">FilePath</span><span class="sxs-lookup"><span data-stu-id="3ae14-116">FilePath</span></span>](/windows/client-management/mdm/firewall-csp#filepath)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ae14-117">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3ae14-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3ae14-118">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="3ae14-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3ae14-119">Fqbn</span><span class="sxs-lookup"><span data-stu-id="3ae14-119">Fqbn</span></span>](/windows/client-management/mdm/firewall-csp#fqbn)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ae14-120">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3ae14-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3ae14-121">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="3ae14-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3ae14-122">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="3ae14-122">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ae14-123">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3ae14-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3ae14-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3ae14-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ae14-125">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="3ae14-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3ae14-126">PackageFamilyName</span><span class="sxs-lookup"><span data-stu-id="3ae14-126">PackageFamilyName</span></span>](/windows/client-management/mdm/firewall-csp#packagefamilyname)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ae14-127">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3ae14-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3ae14-128">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="3ae14-128">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3ae14-129">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="3ae14-129">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ae14-130">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3ae14-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3ae14-131">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3ae14-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ae14-132">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="3ae14-132">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3ae14-133">ServiceName</span><span class="sxs-lookup"><span data-stu-id="3ae14-133">ServiceName</span></span>](/windows/client-management/mdm/firewall-csp#servicename)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ae14-134">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3ae14-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3ae14-135">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="3ae14-135">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3ae14-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3ae14-136">Requirements</span></span>



| <span data-ttu-id="3ae14-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="3ae14-137">Requirement</span></span> | <span data-ttu-id="3ae14-138">Valore</span><span class="sxs-lookup"><span data-stu-id="3ae14-138">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ae14-139">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3ae14-139">Minimum supported client</span></span><br/> | <span data-ttu-id="3ae14-140">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="3ae14-140">Windows 10 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="3ae14-141">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3ae14-141">Minimum supported server</span></span><br/> | <span data-ttu-id="3ae14-142">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="3ae14-142">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="3ae14-143">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="3ae14-143">Namespace</span></span><br/>                | <span data-ttu-id="3ae14-144">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="3ae14-144">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                              |
| <span data-ttu-id="3ae14-145">MOF</span><span class="sxs-lookup"><span data-stu-id="3ae14-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3ae14-146"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3ae14-146"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl> |
| <span data-ttu-id="3ae14-147">DLL</span><span class="sxs-lookup"><span data-stu-id="3ae14-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3ae14-148"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3ae14-148"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl>  |



 

