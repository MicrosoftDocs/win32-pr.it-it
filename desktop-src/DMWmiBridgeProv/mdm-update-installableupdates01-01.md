---
title: Classe MDM_Update_InstallableUpdates01_01
description: La \_ classe MDM Update \_ InstallableUpdates01 \_ 01 viene usata per gestire e controllare l'implementazione degli aggiornamenti approvati.
ms.assetid: 53ca2291-a92a-46ed-948d-6d2a2dddd296
keywords:
- Classe MDM_Update_InstallableUpdates01_01
- Classe MDM_Update_InstallableUpdates01_01, descritta
topic_type:
- apiref
api_name:
- MDM_Update_InstallableUpdates01_01
- MDM_Update_InstallableUpdates01_01.InstanceID
- MDM_Update_InstallableUpdates01_01.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2bcb9dd3ec026e6894d4ba7155cc41f12bc01e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873353"
---
# <a name="mdm_update_installableupdates01_01-class"></a><span data-ttu-id="4e687-105">\_Classe MDM Update \_ InstallableUpdates01 \_ 01</span><span class="sxs-lookup"><span data-stu-id="4e687-105">MDM\_Update\_InstallableUpdates01\_01 class</span></span>

<span data-ttu-id="4e687-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="4e687-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="4e687-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="4e687-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="4e687-108">La classe **MDM \_ Update \_ InstallableUpdates01 \_ 01** viene usata per gestire e controllare l'implementazione degli aggiornamenti approvati.</span><span class="sxs-lookup"><span data-stu-id="4e687-108">The **MDM\_Update\_InstallableUpdates01\_01** class is used to manage and control the rollout of approved updates.</span></span>

<span data-ttu-id="4e687-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="4e687-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e687-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4e687-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Update_InstallableUpdates01_01
{
  string InstanceID;
  string ParentID;
  sint32 Type;
  sint32 RevisionNumber;
};
```

## <a name="members"></a><span data-ttu-id="4e687-111">Members</span><span class="sxs-lookup"><span data-stu-id="4e687-111">Members</span></span>

<span data-ttu-id="4e687-112">La classe **MDM \_ Update \_ InstallableUpdates01 \_ 01** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="4e687-112">The **MDM\_Update\_InstallableUpdates01\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="4e687-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="4e687-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4e687-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="4e687-114">Properties</span></span>

<span data-ttu-id="4e687-115">La classe **MDM \_ Update \_ InstallableUpdates01 \_ 01** presenta queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="4e687-115">The **MDM\_Update\_InstallableUpdates01\_01** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4e687-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="4e687-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e687-117">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="4e687-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4e687-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4e687-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e687-119">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="4e687-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="4e687-120">Identifica il nome del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="4e687-120">Identifies the name of the parent node.</span></span> <span data-ttu-id="4e687-121">Per questa classe, la stringa è il GUID dell'aggiornamento approvato.</span><span class="sxs-lookup"><span data-stu-id="4e687-121">For this class, the string is the GUID of the approved update.</span></span>

</dd> <dt>

<span data-ttu-id="4e687-122">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="4e687-122">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e687-123">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="4e687-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4e687-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4e687-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e687-125">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="4e687-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="4e687-126">Descrive il percorso completo del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="4e687-126">Describes the full path to the parent node.</span></span> <span data-ttu-id="4e687-127">Per questa classe la stringa è "./Vendor/MSFT/Update/InstallableUpdates"</span><span class="sxs-lookup"><span data-stu-id="4e687-127">For this class, the string is "./Vendor/MSFT/Update/InstallableUpdates"</span></span>

</dd> <dt>

[<span data-ttu-id="4e687-128">RevisionNumber</span><span class="sxs-lookup"><span data-stu-id="4e687-128">RevisionNumber</span></span>](/windows/client-management/mdm/update-csp#failedupdates-failed-update-guid-revisionnumber)
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e687-129">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="4e687-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="4e687-130">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="4e687-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="4e687-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="4e687-131">Type</span></span>](/windows/client-management/mdm/update-csp#installableupdates-installable-update-guid-type)
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e687-132">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="4e687-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="4e687-133">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="4e687-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4e687-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4e687-134">Requirements</span></span>



| <span data-ttu-id="4e687-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="4e687-135">Requirement</span></span> | <span data-ttu-id="4e687-136">Valore</span><span class="sxs-lookup"><span data-stu-id="4e687-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e687-137">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4e687-137">Minimum supported client</span></span><br/> | <span data-ttu-id="4e687-138">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="4e687-138">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="4e687-139">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4e687-139">Minimum supported server</span></span><br/> | <span data-ttu-id="4e687-140">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="4e687-140">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="4e687-141">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="4e687-141">Namespace</span></span><br/>                | <span data-ttu-id="4e687-142">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="4e687-142">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="4e687-143">MOF</span><span class="sxs-lookup"><span data-stu-id="4e687-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4e687-144"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4e687-144"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl>      |
| <span data-ttu-id="4e687-145">DLL</span><span class="sxs-lookup"><span data-stu-id="4e687-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4e687-146"><dt>\\DMWmiBridgeProv.dllfile MOF</dt></span><span class="sxs-lookup"><span data-stu-id="4e687-146"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

