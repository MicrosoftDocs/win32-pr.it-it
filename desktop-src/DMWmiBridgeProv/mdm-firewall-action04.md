---
title: Classe MDM_Firewall_Action04
description: La \_ classe Action04 del firewall MDM \_ viene usata per configurare le impostazioni di Windows Defender Firewall.
ms.assetid: d0704662-ac2b-4ff5-a2c1-8f2bc7835488
keywords:
- Classe MDM_Firewall_Action04
- Classe MDM_Firewall_Action04, descritta
topic_type:
- apiref
api_name:
- MDM_Firewall_Action04
- MDM_Firewall_Action04.InstanceID
- MDM_Firewall_Action04.ParentID
- MDM_Firewall_Action04.Type
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1eede757f6a3e129300e6d81a28d34248dda1f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476054"
---
# <a name="mdm_firewall_action04-class"></a><span data-ttu-id="b3778-105">\_Classe Action04 del firewall MDM \_</span><span class="sxs-lookup"><span data-stu-id="b3778-105">MDM\_Firewall\_Action04 class</span></span>

<span data-ttu-id="b3778-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="b3778-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="b3778-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="b3778-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="b3778-108">La \_ classe Action04 del firewall MDM \_ viene usata per configurare le impostazioni di Windows Defender Firewall.</span><span class="sxs-lookup"><span data-stu-id="b3778-108">The MDM\_Firewall\_Action04 class is used to configure the Windows Defender Firewall settings.</span></span>

<span data-ttu-id="b3778-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="b3778-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3778-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b3778-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Firewall_Action04
{
  string InstanceID;
  string ParentID;
  sint32 Type;
};
```

## <a name="members"></a><span data-ttu-id="b3778-111">Members</span><span class="sxs-lookup"><span data-stu-id="b3778-111">Members</span></span>

<span data-ttu-id="b3778-112">La **classe \_ \_ Action04 del firewall MDM** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="b3778-112">The **MDM\_Firewall\_Action04** class has these types of members:</span></span>

-   [<span data-ttu-id="b3778-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b3778-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b3778-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b3778-114">Properties</span></span>

<span data-ttu-id="b3778-115">La **classe \_ \_ Action04 del firewall MDM** presenta queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="b3778-115">The **MDM\_Firewall\_Action04** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b3778-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="b3778-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3778-117">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b3778-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3778-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b3778-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b3778-119">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b3778-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b3778-120">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="b3778-120">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3778-121">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b3778-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3778-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b3778-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b3778-123">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b3778-123">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b3778-124">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="b3778-124">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3778-125">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b3778-125">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b3778-126">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b3778-126">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b3778-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b3778-127">Requirements</span></span>



| <span data-ttu-id="b3778-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="b3778-128">Requirement</span></span> | <span data-ttu-id="b3778-129">Valore</span><span class="sxs-lookup"><span data-stu-id="b3778-129">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3778-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b3778-130">Minimum supported client</span></span><br/> | <span data-ttu-id="b3778-131">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="b3778-131">Windows 10 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b3778-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b3778-132">Minimum supported server</span></span><br/> | <span data-ttu-id="b3778-133">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="b3778-133">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="b3778-134">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b3778-134">Namespace</span></span><br/>                | <span data-ttu-id="b3778-135">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="b3778-135">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                              |
| <span data-ttu-id="b3778-136">MOF</span><span class="sxs-lookup"><span data-stu-id="b3778-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b3778-137"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b3778-137"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl> |
| <span data-ttu-id="b3778-138">DLL</span><span class="sxs-lookup"><span data-stu-id="b3778-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b3778-139"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b3778-139"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl>  |



 

