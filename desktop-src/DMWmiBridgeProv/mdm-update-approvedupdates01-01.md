---
title: Classe MDM_Update_ApprovedUpdates01_01
description: La \_ classe MDM Update \_ ApprovedUpdates01 \_ 01 viene usata per gestire e controllare l'implementazione degli aggiornamenti approvati.
ms.assetid: 3903dbc1-c745-4e9a-a7f7-455338b77563
keywords:
- Classe MDM_Update_ApprovedUpdates01_01
- Classe MDM_Update_ApprovedUpdates01_01, descritta
topic_type:
- apiref
api_name:
- MDM_Update_ApprovedUpdates01_01
- MDM_Update_ApprovedUpdates01_01.InstanceID
- MDM_Update_ApprovedUpdates01_01.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e6e12700b04f6e48fdf746cb27953da5849169d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963788"
---
# <a name="mdm_update_approvedupdates01_01-class"></a><span data-ttu-id="ce77c-105">\_Classe MDM Update \_ ApprovedUpdates01 \_ 01</span><span class="sxs-lookup"><span data-stu-id="ce77c-105">MDM\_Update\_ApprovedUpdates01\_01 class</span></span>

<span data-ttu-id="ce77c-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="ce77c-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="ce77c-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="ce77c-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="ce77c-108">La classe **MDM \_ Update \_ ApprovedUpdates01 \_ 01** viene usata per gestire e controllare l'implementazione degli aggiornamenti approvati.</span><span class="sxs-lookup"><span data-stu-id="ce77c-108">The **MDM\_Update\_ApprovedUpdates01\_01** class is used to manage and control the rollout of approved updates.</span></span>

<span data-ttu-id="ce77c-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="ce77c-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce77c-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ce77c-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Update_ApprovedUpdates01_01
{
  string   InstanceID;
  string   ParentID;
  datetime ApprovedTime;
};
```

## <a name="members"></a><span data-ttu-id="ce77c-111">Members</span><span class="sxs-lookup"><span data-stu-id="ce77c-111">Members</span></span>

<span data-ttu-id="ce77c-112">La classe **MDM \_ Update \_ ApprovedUpdates01 \_ 01** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="ce77c-112">The **MDM\_Update\_ApprovedUpdates01\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="ce77c-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ce77c-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ce77c-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ce77c-114">Properties</span></span>

<span data-ttu-id="ce77c-115">La classe **MDM \_ Update \_ ApprovedUpdates01 \_ 01** presenta queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="ce77c-115">The **MDM\_Update\_ApprovedUpdates01\_01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="ce77c-116">ApprovedTime</span><span class="sxs-lookup"><span data-stu-id="ce77c-116">ApprovedTime</span></span>](/windows/client-management/mdm/update-csp#approvedupdates-approved-update-guid-approvedtime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce77c-117">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="ce77c-117">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ce77c-118">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ce77c-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ce77c-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="ce77c-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce77c-120">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ce77c-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ce77c-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ce77c-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ce77c-122">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ce77c-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="ce77c-123">Identifica il nome del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="ce77c-123">Identifies the name of the parent node.</span></span> <span data-ttu-id="ce77c-124">Per questa classe, la stringa è il GUID dell'aggiornamento approvato.</span><span class="sxs-lookup"><span data-stu-id="ce77c-124">For this class, the string is the GUID of the approved update.</span></span>

</dd> <dt>

<span data-ttu-id="ce77c-125">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="ce77c-125">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce77c-126">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ce77c-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ce77c-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ce77c-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ce77c-128">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ce77c-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="ce77c-129">Descrive il percorso completo del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="ce77c-129">Describes the full path to the parent node.</span></span> <span data-ttu-id="ce77c-130">Per questa classe la stringa è "./Vendor/MSFT/Update/ApprovedUpdates"</span><span class="sxs-lookup"><span data-stu-id="ce77c-130">For this class, the string is "./Vendor/MSFT/Update/ApprovedUpdates"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ce77c-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ce77c-131">Requirements</span></span>



| <span data-ttu-id="ce77c-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="ce77c-132">Requirement</span></span> | <span data-ttu-id="ce77c-133">Valore</span><span class="sxs-lookup"><span data-stu-id="ce77c-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce77c-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ce77c-134">Minimum supported client</span></span><br/> | <span data-ttu-id="ce77c-135">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="ce77c-135">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="ce77c-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ce77c-136">Minimum supported server</span></span><br/> | <span data-ttu-id="ce77c-137">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="ce77c-137">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="ce77c-138">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ce77c-138">Namespace</span></span><br/>                | <span data-ttu-id="ce77c-139">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="ce77c-139">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="ce77c-140">MOF</span><span class="sxs-lookup"><span data-stu-id="ce77c-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ce77c-141"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ce77c-141"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl>      |
| <span data-ttu-id="ce77c-142">DLL</span><span class="sxs-lookup"><span data-stu-id="ce77c-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ce77c-143"><dt>\\DMWmiBridgeProv.dllfile MOF</dt></span><span class="sxs-lookup"><span data-stu-id="ce77c-143"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

