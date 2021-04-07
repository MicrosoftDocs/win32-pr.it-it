---
title: Classe MDM_Policy_Result01_Messaging02
description: La \_ classe Messaging02 dei criteri MDM \_ Result01 \_ rappresenta il backup e il ripristino dei messaggi di testo e la messaggistica ovunque.
ms.assetid: cdc92999-3a2b-4653-b64f-79e19abe5559
keywords:
- Classe MDM_Policy_Result01_Messaging02
- Classe MDM_Policy_Result01_Messaging02, descritta
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Messaging02
- MDM_Policy_Result01_Messaging02.InstanceID
- MDM_Policy_Result01_Messaging02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: afd0eda84b9e2492243b2af85457450b0e443a93
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964105"
---
# <a name="mdm_policy_result01_messaging02-class"></a><span data-ttu-id="fb733-105">\_ \_ Classe Result01 Messaging02 di criteri \_ MDM</span><span class="sxs-lookup"><span data-stu-id="fb733-105">MDM\_Policy\_Result01\_Messaging02 class</span></span>

<span data-ttu-id="fb733-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="fb733-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="fb733-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="fb733-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="fb733-108">La \_ classe Messaging02 dei criteri MDM \_ Result01 \_ rappresenta il backup e il ripristino dei messaggi di testo e la messaggistica ovunque.</span><span class="sxs-lookup"><span data-stu-id="fb733-108">The MDM\_Policy\_Result01\_Messaging02 class represents the text message back up and restore and Messaging Everywhere.</span></span>

<span data-ttu-id="fb733-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="fb733-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb733-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fb733-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Messaging02
{
  string InstanceID;
  string ParentID;
  sint32 AllowMessageSync;
};
```

## <a name="members"></a><span data-ttu-id="fb733-111">Members</span><span class="sxs-lookup"><span data-stu-id="fb733-111">Members</span></span>

<span data-ttu-id="fb733-112">La **classe \_ \_ Result01 \_ Messaging02 dei criteri MDM** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="fb733-112">The **MDM\_Policy\_Result01\_Messaging02** class has these types of members:</span></span>

-   [<span data-ttu-id="fb733-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="fb733-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fb733-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="fb733-114">Properties</span></span>

<span data-ttu-id="fb733-115">La **classe \_ \_ \_ Messaging02 dei criteri MDM Result01** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="fb733-115">The **MDM\_Policy\_Result01\_Messaging02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="fb733-116">AllowMessageSync</span><span class="sxs-lookup"><span data-stu-id="fb733-116">AllowMessageSync</span></span>](/windows/client-management/mdm/policy-csp-messaging#messaging-allowmessagesync)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb733-117">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="fb733-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="fb733-118">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="fb733-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="fb733-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="fb733-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb733-120">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="fb733-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fb733-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fb733-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fb733-122">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="fb733-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="fb733-123">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="fb733-123">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb733-124">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="fb733-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fb733-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fb733-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fb733-126">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="fb733-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fb733-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fb733-127">Requirements</span></span>



| <span data-ttu-id="fb733-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="fb733-128">Requirement</span></span> | <span data-ttu-id="fb733-129">Valore</span><span class="sxs-lookup"><span data-stu-id="fb733-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb733-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fb733-130">Minimum supported client</span></span><br/> | <span data-ttu-id="fb733-131">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="fb733-131">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="fb733-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fb733-132">Minimum supported server</span></span><br/> | <span data-ttu-id="fb733-133">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="fb733-133">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="fb733-134">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="fb733-134">Namespace</span></span><br/>                | <span data-ttu-id="fb733-135">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="fb733-135">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="fb733-136">MOF</span><span class="sxs-lookup"><span data-stu-id="fb733-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fb733-137"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fb733-137"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="fb733-138">DLL</span><span class="sxs-lookup"><span data-stu-id="fb733-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fb733-139"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fb733-139"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

