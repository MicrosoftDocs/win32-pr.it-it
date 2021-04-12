---
title: Classe MDM_VPNv2_AppTriggerList02_App04
description: La \_ classe MDM VPNv2AppTriggerList02 \_ App04 descrive un elenco di applicazioni impostate per attivare la VPN.
ms.assetid: d17ec7b9-8a66-47da-8373-81b56168b495
keywords:
- Classe MDM_VPNv2_AppTriggerList02_App04
- Classe MDM_VPNv2_AppTriggerList02_App04, descritta
topic_type:
- apiref
api_name:
- MDM_VPNv2_AppTriggerList02_App04
- MDM_VPNv2_AppTriggerList02_App04.InstanceID
- MDM_VPNv2_AppTriggerList02_App04.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62685ea94b99e843625e87e7c653a2ff19ab737d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120095"
---
# <a name="mdm_vpnv2_apptriggerlist02_app04-class"></a><span data-ttu-id="159a7-105">MDM \_ VPNv2 \_ AppTriggerList02 \_ classe App04</span><span class="sxs-lookup"><span data-stu-id="159a7-105">MDM\_VPNv2\_AppTriggerList02\_App04 class</span></span>

<span data-ttu-id="159a7-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="159a7-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="159a7-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="159a7-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="159a7-108">La classe **MDM \_ VPNv2AppTriggerList02 \_ App04** descrive un elenco di applicazioni impostate per attivare la VPN.</span><span class="sxs-lookup"><span data-stu-id="159a7-108">The **MDM\_VPNv2AppTriggerList02\_App04** class describes a list of applications set to trigger the VPN.</span></span>

<span data-ttu-id="159a7-109">Se una di queste app viene avviata e il profilo VPN è attualmente il profilo attivo, questo profilo VPN verrà attivato per la connessione.</span><span class="sxs-lookup"><span data-stu-id="159a7-109">If any of these apps are launched and the VPN profile is currently the active profile, this VPN profile will be triggered to connect.</span></span>

<span data-ttu-id="159a7-110">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="159a7-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="159a7-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="159a7-111">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_AppTriggerList02_App04
{
  string InstanceID;
  string ParentID;
  string Id;
  string Type;
};
```

## <a name="members"></a><span data-ttu-id="159a7-112">Members</span><span class="sxs-lookup"><span data-stu-id="159a7-112">Members</span></span>

<span data-ttu-id="159a7-113">La classe **MDM \_ VPNv2 \_ AppTriggerList02 \_ App04** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="159a7-113">The **MDM\_VPNv2\_AppTriggerList02\_App04** class has these types of members:</span></span>

-   [<span data-ttu-id="159a7-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="159a7-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="159a7-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="159a7-115">Properties</span></span>

<span data-ttu-id="159a7-116">La classe **MDM \_ VPNv2 \_ AppTriggerList02 \_ App04** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="159a7-116">The **MDM\_VPNv2\_AppTriggerList02\_App04** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="159a7-117">Id</span><span class="sxs-lookup"><span data-stu-id="159a7-117">Id</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-trafficfilterlist-trafficfilterid-app-id)
</dt> <dd> <dl> <dt>

<span data-ttu-id="159a7-118">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="159a7-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="159a7-119">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="159a7-119">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="159a7-120">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="159a7-120">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="159a7-121">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="159a7-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="159a7-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="159a7-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="159a7-123">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="159a7-123">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="159a7-124">Nodo dell'app sotto l'ID di riga.</span><span class="sxs-lookup"><span data-stu-id="159a7-124">App Node under the Row Id.</span></span>

</dd> <dt>

<span data-ttu-id="159a7-125">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="159a7-125">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="159a7-126">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="159a7-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="159a7-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="159a7-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="159a7-128">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="159a7-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="159a7-129">Descrive il percorso completo del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="159a7-129">Describes the full path to the parent node.</span></span> <span data-ttu-id="159a7-130">Per questa classe la stringa è "./Vendor/MSFT/VPNv2/*ProfileName*/AppTriggerList/*appTriggerRowId*"</span><span class="sxs-lookup"><span data-stu-id="159a7-130">For this class, the string is "./Vendor/MSFT/VPNv2/*ProfileName*/AppTriggerList/*appTriggerRowId*"</span></span>

</dd> <dt>

[<span data-ttu-id="159a7-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="159a7-131">Type</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-apptriggerlist-apptriggerrowid-app-type)
</dt> <dd> <dl> <dt>

<span data-ttu-id="159a7-132">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="159a7-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="159a7-133">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="159a7-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="159a7-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="159a7-134">Requirements</span></span>



| <span data-ttu-id="159a7-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="159a7-135">Requirement</span></span> | <span data-ttu-id="159a7-136">Valore</span><span class="sxs-lookup"><span data-stu-id="159a7-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="159a7-137">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="159a7-137">Minimum supported client</span></span><br/> | <span data-ttu-id="159a7-138">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="159a7-138">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="159a7-139">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="159a7-139">Minimum supported server</span></span><br/> | <span data-ttu-id="159a7-140">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="159a7-140">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="159a7-141">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="159a7-141">Namespace</span></span><br/>                | <span data-ttu-id="159a7-142">\\ \\ DMMap MDM CIMv2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="159a7-142">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="159a7-143">MOF</span><span class="sxs-lookup"><span data-stu-id="159a7-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="159a7-144"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="159a7-144"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="159a7-145">DLL</span><span class="sxs-lookup"><span data-stu-id="159a7-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="159a7-146"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="159a7-146"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="159a7-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="159a7-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="159a7-148">Utilizzo di script di PowerShell con il provider del Bridge WMI</span><span class="sxs-lookup"><span data-stu-id="159a7-148">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

