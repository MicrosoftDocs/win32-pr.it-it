---
title: Classe MDM_ActiveSync_User_ContentTypes04_01
description: La \_ classe MDM ActiveSync \_ User \_ ContentTypes04 \_ 01 definisce il tipo di contenuto da abilitare/disabilitare singolarmente per la sincronizzazione.
ms.assetid: 82759cf9-ea2a-4d75-bb07-6832c3005074
keywords:
- Classe MDM_ActiveSync_User_ContentTypes04_01
- Classe MDM_ActiveSync_User_ContentTypes04_01, descritta
topic_type:
- apiref
api_name:
- MDM_ActiveSync_User_ContentTypes04_01
- MDM_ActiveSync_User_ContentTypes04_01.InstanceID
- MDM_ActiveSync_User_ContentTypes04_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ef158daf25c6dc1c084966673f71c5907c4df1a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301473"
---
# <a name="mdm_activesync_user_contenttypes04_01-class"></a><span data-ttu-id="2cd68-105">\_Classe MDM ActiveSync \_ User \_ ContentTypes04 \_ 01</span><span class="sxs-lookup"><span data-stu-id="2cd68-105">MDM\_ActiveSync\_User\_ContentTypes04\_01 class</span></span>

<span data-ttu-id="2cd68-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="2cd68-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="2cd68-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="2cd68-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="2cd68-108">La classe **MDM \_ ActiveSync \_ User \_ ContentTypes04 \_ 01** definisce il tipo di contenuto da abilitare/disabilitare singolarmente per la sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="2cd68-108">The **MDM\_ActiveSync\_User\_ContentTypes04\_01** class defines the type of content to be individually enabled/disabled for sync.</span></span>

<span data-ttu-id="2cd68-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="2cd68-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="2cd68-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2cd68-110">Syntax</span></span>

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_ActiveSync_User_ContentTypes04_01
{
  string InstanceID;
  string ParentID;
  string Enabled;
  string Name;
};
```

## <a name="members"></a><span data-ttu-id="2cd68-111">Members</span><span class="sxs-lookup"><span data-stu-id="2cd68-111">Members</span></span>

<span data-ttu-id="2cd68-112">La classe **MDM \_ ActiveSync \_ User \_ ContentTypes04 \_ 01** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="2cd68-112">The **MDM\_ActiveSync\_User\_ContentTypes04\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="2cd68-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2cd68-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2cd68-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2cd68-114">Properties</span></span>

<span data-ttu-id="2cd68-115">La classe **MDM \_ ActiveSync \_ User \_ ContentTypes04 \_ 01** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="2cd68-115">The **MDM\_ActiveSync\_User\_ContentTypes04\_01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="2cd68-116">Enabled</span><span class="sxs-lookup"><span data-stu-id="2cd68-116">Enabled</span></span>](/windows/client-management/mdm/activesync-csp#options-contenttypes-content-type-guid-enabled)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cd68-117">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2cd68-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2cd68-118">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="2cd68-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2cd68-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="2cd68-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cd68-120">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2cd68-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2cd68-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2cd68-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2cd68-122">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="2cd68-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="2cd68-123">Identifica il nome del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="2cd68-123">Identifies the name of the parent node.</span></span>

</dd> <dt>

[<span data-ttu-id="2cd68-124">Nome</span><span class="sxs-lookup"><span data-stu-id="2cd68-124">Name</span></span>](/windows/client-management/mdm/activesync-csp#options-contenttypes-content-type-guid-name)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cd68-125">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2cd68-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2cd68-126">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="2cd68-126">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2cd68-127">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="2cd68-127">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cd68-128">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2cd68-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2cd68-129">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2cd68-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2cd68-130">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="2cd68-130">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="2cd68-131">Descrive il percorso completo del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="2cd68-131">Describes the full path to the parent node.</span></span> <span data-ttu-id="2cd68-132">Per questa classe la stringa è "./Vendor/MSFT/ActiveSync/Accounts/*GUID*/Options"</span><span class="sxs-lookup"><span data-stu-id="2cd68-132">For this class, the string is "./Vendor/MSFT/ActiveSync/Accounts/*GUID*/Options"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2cd68-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2cd68-133">Requirements</span></span>



| <span data-ttu-id="2cd68-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="2cd68-134">Requirement</span></span> | <span data-ttu-id="2cd68-135">Valore</span><span class="sxs-lookup"><span data-stu-id="2cd68-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2cd68-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2cd68-136">Minimum supported client</span></span><br/> | <span data-ttu-id="2cd68-137">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="2cd68-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2cd68-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2cd68-138">Minimum supported server</span></span><br/> | <span data-ttu-id="2cd68-139">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="2cd68-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="2cd68-140">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="2cd68-140">Namespace</span></span><br/>                | <span data-ttu-id="2cd68-141">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="2cd68-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="2cd68-142">MOF</span><span class="sxs-lookup"><span data-stu-id="2cd68-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2cd68-143"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2cd68-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="2cd68-144">DLL</span><span class="sxs-lookup"><span data-stu-id="2cd68-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2cd68-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2cd68-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2cd68-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2cd68-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2cd68-147">Utilizzo di script di PowerShell con il provider del Bridge WMI</span><span class="sxs-lookup"><span data-stu-id="2cd68-147">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

