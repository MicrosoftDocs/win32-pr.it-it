---
title: Classe MDM_Update
description: La \_ classe di aggiornamento MDM viene utilizzata per gestire e controllare l'implementazione di nuovi aggiornamenti.
ms.assetid: 503884fd-190c-482d-b600-1a15363891f3
keywords:
- Classe MDM_Update
- Classe MDM_Update, descritta
topic_type:
- apiref
api_name:
- MDM_Update
- MDM_Update.InstanceID
- MDM_Update.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2735b5eaaef4abc468586cb7608be7969a1eab3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873641"
---
# <a name="mdm_update-class"></a><span data-ttu-id="dfcb1-105">\_Classe di aggiornamento MDM</span><span class="sxs-lookup"><span data-stu-id="dfcb1-105">MDM\_Update class</span></span>

<span data-ttu-id="dfcb1-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="dfcb1-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="dfcb1-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="dfcb1-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="dfcb1-108">La classe di **\_ aggiornamento MDM** viene utilizzata per gestire e controllare l'implementazione di nuovi aggiornamenti.</span><span class="sxs-lookup"><span data-stu-id="dfcb1-108">The **MDM\_Update** class is used to manage and control the rollout of new updates.</span></span>

<span data-ttu-id="dfcb1-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="dfcb1-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="dfcb1-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dfcb1-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Update
{
  string   InstanceID;
  string   ParentID;
  datetime LastSuccessfulScanTime;
  sint32   DeferUpgrade;
};
```

## <a name="members"></a><span data-ttu-id="dfcb1-111">Members</span><span class="sxs-lookup"><span data-stu-id="dfcb1-111">Members</span></span>

<span data-ttu-id="dfcb1-112">La classe di **\_ aggiornamento MDM** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="dfcb1-112">The **MDM\_Update** class has these types of members:</span></span>

-   [<span data-ttu-id="dfcb1-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="dfcb1-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="dfcb1-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="dfcb1-114">Properties</span></span>

<span data-ttu-id="dfcb1-115">La classe di **\_ aggiornamento MDM** presenta queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="dfcb1-115">The **MDM\_Update** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="dfcb1-116">DeferUpgrade</span><span class="sxs-lookup"><span data-stu-id="dfcb1-116">DeferUpgrade</span></span>](/windows/client-management/mdm/update-csp#deferupgrade)
</dt> <dd> <dl> <dt>

<span data-ttu-id="dfcb1-117">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="dfcb1-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="dfcb1-118">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="dfcb1-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="dfcb1-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="dfcb1-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dfcb1-120">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="dfcb1-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dfcb1-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dfcb1-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dfcb1-122">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="dfcb1-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="dfcb1-123">Identifica il nome del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="dfcb1-123">Identifies the name of the parent node.</span></span> <span data-ttu-id="dfcb1-124">Per questa classe la stringa è "Update".</span><span class="sxs-lookup"><span data-stu-id="dfcb1-124">For this class, the string is "Update".</span></span>

</dd> <dt>

[<span data-ttu-id="dfcb1-125">LastSuccessfulScanTime</span><span class="sxs-lookup"><span data-stu-id="dfcb1-125">LastSuccessfulScanTime</span></span>](/windows/client-management/mdm/update-csp#lastsuccessfulscantime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="dfcb1-126">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="dfcb1-126">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="dfcb1-127">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="dfcb1-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="dfcb1-128">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="dfcb1-128">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dfcb1-129">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="dfcb1-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dfcb1-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dfcb1-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dfcb1-131">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="dfcb1-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="dfcb1-132">Descrive il percorso completo del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="dfcb1-132">Describes the full path to the parent node.</span></span> <span data-ttu-id="dfcb1-133">Per questa classe la stringa è "./Vendor/MSFT/"</span><span class="sxs-lookup"><span data-stu-id="dfcb1-133">For this class, the string is "./Vendor/MSFT/"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="dfcb1-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dfcb1-134">Requirements</span></span>



| <span data-ttu-id="dfcb1-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="dfcb1-135">Requirement</span></span> | <span data-ttu-id="dfcb1-136">Valore</span><span class="sxs-lookup"><span data-stu-id="dfcb1-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dfcb1-137">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dfcb1-137">Minimum supported client</span></span><br/> | <span data-ttu-id="dfcb1-138">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="dfcb1-138">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="dfcb1-139">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dfcb1-139">Minimum supported server</span></span><br/> | <span data-ttu-id="dfcb1-140">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="dfcb1-140">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="dfcb1-141">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="dfcb1-141">Namespace</span></span><br/>                | <span data-ttu-id="dfcb1-142">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="dfcb1-142">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="dfcb1-143">MOF</span><span class="sxs-lookup"><span data-stu-id="dfcb1-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dfcb1-144"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dfcb1-144"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl>      |
| <span data-ttu-id="dfcb1-145">DLL</span><span class="sxs-lookup"><span data-stu-id="dfcb1-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dfcb1-146"><dt>\\DMWmiBridgeProv.dllfile MOF</dt></span><span class="sxs-lookup"><span data-stu-id="dfcb1-146"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

