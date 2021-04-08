---
title: Classe MDM_RemoteFind
description: La \_ classe MDM RemoteFind recupera le informazioni sulla posizione per un dispositivo specifico.
ms.assetid: 8dfbe951-b4ca-4709-bec9-0821571f9b0e
keywords:
- Classe MDM_RemoteFind
- Classe MDM_RemoteFind, descritta
topic_type:
- apiref
api_name:
- MDM_RemoteFind
- MDM_RemoteFind.InstanceID
- MDM_RemoteFind.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8930d80ede9daad5c721cd3b226c85e3d9918a19
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740074"
---
# <a name="mdm_remotefind-class"></a><span data-ttu-id="e7941-105">MDM \_ RemoteFind (classe)</span><span class="sxs-lookup"><span data-stu-id="e7941-105">MDM\_RemoteFind class</span></span>

<span data-ttu-id="e7941-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="e7941-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="e7941-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="e7941-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="e7941-108">La classe **MDM \_ RemoteFind** recupera le informazioni sulla posizione per un dispositivo specifico.</span><span class="sxs-lookup"><span data-stu-id="e7941-108">The **MDM\_RemoteFind** class retrieves the location information for a particular device.</span></span>

<span data-ttu-id="e7941-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="e7941-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7941-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e7941-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_RemoteFind
{
  string InstanceID;
  string ParentID;
  sint32 DesiredAccuracy;
  sint32 MaximumAge;
  sint32 Timeout;
};
```

## <a name="members"></a><span data-ttu-id="e7941-111">Members</span><span class="sxs-lookup"><span data-stu-id="e7941-111">Members</span></span>

<span data-ttu-id="e7941-112">La classe **MDM \_ RemoteFind** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="e7941-112">The **MDM\_RemoteFind** class has these types of members:</span></span>

-   [<span data-ttu-id="e7941-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e7941-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e7941-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e7941-114">Properties</span></span>

<span data-ttu-id="e7941-115">La classe **MDM \_ RemoteFind** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="e7941-115">The **MDM\_RemoteFind** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="e7941-116">DesiredAccuracy</span><span class="sxs-lookup"><span data-stu-id="e7941-116">DesiredAccuracy</span></span>](/windows/client-management/mdm/remotefind-csp#desiredaccuracy)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7941-117">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="e7941-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e7941-118">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="e7941-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e7941-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="e7941-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7941-120">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e7941-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e7941-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e7941-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e7941-122">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e7941-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="e7941-123">Identifica il nome del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="e7941-123">Identifies the name of the parent node.</span></span> <span data-ttu-id="e7941-124">Per questa classe la stringa è "RemoteFind".</span><span class="sxs-lookup"><span data-stu-id="e7941-124">For this class, the string is "RemoteFind".</span></span>

</dd> <dt>

[<span data-ttu-id="e7941-125">Numero massimo</span><span class="sxs-lookup"><span data-stu-id="e7941-125">MaximumAge</span></span>](/windows/client-management/mdm/remotefind-csp#maximumage)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7941-126">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="e7941-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e7941-127">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="e7941-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e7941-128">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="e7941-128">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7941-129">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e7941-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e7941-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e7941-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e7941-131">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e7941-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="e7941-132">Descrive il percorso completo del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="e7941-132">Describes the full path to the parent node.</span></span> <span data-ttu-id="e7941-133">Per questa classe la stringa è "./Vendor/MSFT/"</span><span class="sxs-lookup"><span data-stu-id="e7941-133">For this class, the string is "./Vendor/MSFT/"</span></span>

</dd> <dt>

[<span data-ttu-id="e7941-134">Timeout</span><span class="sxs-lookup"><span data-stu-id="e7941-134">Timeout</span></span>](/windows/client-management/mdm/remotefind-csp#timeout)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7941-135">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="e7941-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e7941-136">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="e7941-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e7941-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e7941-137">Requirements</span></span>



| <span data-ttu-id="e7941-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="e7941-138">Requirement</span></span> | <span data-ttu-id="e7941-139">Valore</span><span class="sxs-lookup"><span data-stu-id="e7941-139">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7941-140">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e7941-140">Minimum supported client</span></span><br/> | <span data-ttu-id="e7941-141">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="e7941-141">Windows 10 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e7941-142">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e7941-142">Minimum supported server</span></span><br/> | <span data-ttu-id="e7941-143">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="e7941-143">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="e7941-144">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="e7941-144">Namespace</span></span><br/>                | <span data-ttu-id="e7941-145">\\ \\ DMMap MDM CIMv2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="e7941-145">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                              |
| <span data-ttu-id="e7941-146">MOF</span><span class="sxs-lookup"><span data-stu-id="e7941-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e7941-147"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e7941-147"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl> |
| <span data-ttu-id="e7941-148">DLL</span><span class="sxs-lookup"><span data-stu-id="e7941-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e7941-149"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e7941-149"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="e7941-150">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e7941-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7941-151">Utilizzo di script di PowerShell con il provider del Bridge WMI</span><span class="sxs-lookup"><span data-stu-id="e7941-151">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

