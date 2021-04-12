---
title: Classe MDM_Update_FailedUpdates01_01
description: La \_ classe MDM Update \_ FailedUpdates01 \_ 01 viene usata per gestire gli aggiornamenti non riusciti.
ms.assetid: 3bb7993b-b44b-44d1-84ee-dbdda0093ca0
keywords:
- Classe MDM_Update_FailedUpdates01_01
- Classe MDM_Update_FailedUpdates01_01, descritta
topic_type:
- apiref
api_name:
- MDM_Update_FailedUpdates01_01
- MDM_Update_FailedUpdates01_01.InstanceID
- MDM_Update_FailedUpdates01_01.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e0ba8d42d97b15cd195e87f536abad9610492e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475274"
---
# <a name="mdm_update_failedupdates01_01-class"></a><span data-ttu-id="ab949-105">\_Classe MDM Update \_ FailedUpdates01 \_ 01</span><span class="sxs-lookup"><span data-stu-id="ab949-105">MDM\_Update\_FailedUpdates01\_01 class</span></span>

<span data-ttu-id="ab949-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="ab949-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="ab949-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="ab949-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="ab949-108">La classe **MDM \_ Update \_ FailedUpdates01 \_ 01** viene usata per gestire gli aggiornamenti non riusciti.</span><span class="sxs-lookup"><span data-stu-id="ab949-108">The **MDM\_Update\_FailedUpdates01\_01** class is used to manage failed updates.</span></span>

<span data-ttu-id="ab949-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="ab949-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab949-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ab949-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Update_FailedUpdates01_01
{
  string InstanceID;
  string ParentID;
  sint32 HResult;
  sint32 State;
};
```

## <a name="members"></a><span data-ttu-id="ab949-111">Members</span><span class="sxs-lookup"><span data-stu-id="ab949-111">Members</span></span>

<span data-ttu-id="ab949-112">La classe **MDM \_ Update \_ FailedUpdates01 \_ 01** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="ab949-112">The **MDM\_Update\_FailedUpdates01\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="ab949-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ab949-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ab949-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ab949-114">Properties</span></span>

<span data-ttu-id="ab949-115">La classe **MDM \_ Update \_ FailedUpdates01 \_ 01** presenta queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="ab949-115">The **MDM\_Update\_FailedUpdates01\_01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="ab949-116">HResult</span><span class="sxs-lookup"><span data-stu-id="ab949-116">HResult</span></span>](/windows/client-management/mdm/update-csp#failedupdates-failed-update-guid-hresult)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab949-117">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ab949-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ab949-118">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ab949-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ab949-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="ab949-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab949-120">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ab949-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ab949-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ab949-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ab949-122">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ab949-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="ab949-123">Identifica il nome del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="ab949-123">Identifies the name of the parent node.</span></span> <span data-ttu-id="ab949-124">Per questa classe, la stringa è il GUID dell'aggiornamento non riuscito.</span><span class="sxs-lookup"><span data-stu-id="ab949-124">For this class, the string is the GUID of the failed update.</span></span>

</dd> <dt>

<span data-ttu-id="ab949-125">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="ab949-125">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab949-126">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ab949-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ab949-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ab949-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ab949-128">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ab949-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="ab949-129">Descrive il percorso completo del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="ab949-129">Describes the full path to the parent node.</span></span> <span data-ttu-id="ab949-130">Per questa classe la stringa è "./Vendor/MSFT/Update/FailedUpdates"</span><span class="sxs-lookup"><span data-stu-id="ab949-130">For this class, the string is "./Vendor/MSFT/Update/FailedUpdates"</span></span>

</dd> <dt>

[<span data-ttu-id="ab949-131">**State**</span><span class="sxs-lookup"><span data-stu-id="ab949-131">**State**</span></span>](/windows/client-management/mdm/update-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab949-132">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ab949-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ab949-133">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ab949-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ab949-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ab949-134">Requirements</span></span>



| <span data-ttu-id="ab949-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="ab949-135">Requirement</span></span> | <span data-ttu-id="ab949-136">Valore</span><span class="sxs-lookup"><span data-stu-id="ab949-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab949-137">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ab949-137">Minimum supported client</span></span><br/> | <span data-ttu-id="ab949-138">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="ab949-138">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="ab949-139">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ab949-139">Minimum supported server</span></span><br/> | <span data-ttu-id="ab949-140">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="ab949-140">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="ab949-141">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ab949-141">Namespace</span></span><br/>                | <span data-ttu-id="ab949-142">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="ab949-142">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="ab949-143">MOF</span><span class="sxs-lookup"><span data-stu-id="ab949-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ab949-144"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ab949-144"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl>      |
| <span data-ttu-id="ab949-145">DLL</span><span class="sxs-lookup"><span data-stu-id="ab949-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ab949-146"><dt>\\DMWmiBridgeProv.dllfile MOF</dt></span><span class="sxs-lookup"><span data-stu-id="ab949-146"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

