---
title: Classe MDM_VPNv2_TrafficFilterList02_App04
description: La \_ classe MDM TrafficFilterList02 \_ App04 fornisce la configurazione delle app consentite sull'interfaccia VPN.
ms.assetid: a56d004b-8fe3-4187-8aad-962f1cab8f7f
keywords:
- Classe MDM_VPNv2_TrafficFilterList02_App04
- Classe MDM_VPNv2_TrafficFilterList02_App04, descritta
topic_type:
- apiref
api_name:
- MDM_VPNv2_TrafficFilterList02_App04
- MDM_VPNv2_TrafficFilterList02_App04.InstanceID
- MDM_VPNv2_TrafficFilterList02_App04.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8b1cd3edbfec5fa270f8404983af57dba4fad31
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120619"
---
# <a name="mdm_vpnv2_trafficfilterlist02_app04-class"></a><span data-ttu-id="89104-105">MDM \_ VPNv2 \_ TrafficFilterList02 \_ classe App04</span><span class="sxs-lookup"><span data-stu-id="89104-105">MDM\_VPNv2\_TrafficFilterList02\_App04 class</span></span>

<span data-ttu-id="89104-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="89104-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="89104-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="89104-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="89104-108">La classe **MDM \_ TrafficFilterList02 \_ App04** fornisce la configurazione delle app consentite sull'interfaccia VPN.</span><span class="sxs-lookup"><span data-stu-id="89104-108">The **MDM\_TrafficFilterList02\_App04** class provides configuration of the apps that are allowed over the VPN interface.</span></span>

<span data-ttu-id="89104-109">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="89104-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="89104-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="89104-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_TrafficFilterList02_App04
{
  string InstanceID;
  string ParentID;
  string Id;
  string Type;
};
```

## <a name="members"></a><span data-ttu-id="89104-111">Members</span><span class="sxs-lookup"><span data-stu-id="89104-111">Members</span></span>

<span data-ttu-id="89104-112">La classe **MDM \_ VPNv2 \_ TrafficFilterList02 \_ App04** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="89104-112">The **MDM\_VPNv2\_TrafficFilterList02\_App04** class has these types of members:</span></span>

-   [<span data-ttu-id="89104-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="89104-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="89104-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="89104-114">Properties</span></span>

<span data-ttu-id="89104-115">La classe **MDM \_ VPNv2 \_ TrafficFilterList02 \_ App04** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="89104-115">The **MDM\_VPNv2\_TrafficFilterList02\_App04** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="89104-116">Id</span><span class="sxs-lookup"><span data-stu-id="89104-116">Id</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-trafficfilterlist-trafficfilterid-app-id)
</dt> <dd> <dl> <dt>

<span data-ttu-id="89104-117">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="89104-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89104-118">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="89104-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="89104-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="89104-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89104-120">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="89104-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89104-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="89104-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89104-122">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="89104-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="89104-123">Regola VPN per app.</span><span class="sxs-lookup"><span data-stu-id="89104-123">Per app VPN rule.</span></span> <span data-ttu-id="89104-124">In questo modo, solo le app specificate possono essere consentite sull'interfaccia VPN.</span><span class="sxs-lookup"><span data-stu-id="89104-124">This will allow only the apps specified to be allowed over the VPN interface.</span></span> <span data-ttu-id="89104-125">Per questa classe la stringa è "app"</span><span class="sxs-lookup"><span data-stu-id="89104-125">For this class, the string is "App"</span></span>

</dd> <dt>

<span data-ttu-id="89104-126">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="89104-126">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89104-127">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="89104-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89104-128">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="89104-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89104-129">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="89104-129">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="89104-130">Descrive il percorso completo del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="89104-130">Describes the full path to the parent node.</span></span> <span data-ttu-id="89104-131">Per questa classe la stringa è "./Vendor/MSFT/VPNv2/*ProfileName*/TrafficFilterList/*trafficFilterListId*"</span><span class="sxs-lookup"><span data-stu-id="89104-131">For this class, the string is "./Vendor/MSFT/VPNv2/*ProfileName*/TrafficFilterList/*trafficFilterListId*"</span></span>

</dd> <dt>

[<span data-ttu-id="89104-132">Tipo</span><span class="sxs-lookup"><span data-stu-id="89104-132">Type</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-apptriggerlist-apptriggerrowid-app-type)
</dt> <dd> <dl> <dt>

<span data-ttu-id="89104-133">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="89104-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89104-134">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="89104-134">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="89104-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="89104-135">Requirements</span></span>



| <span data-ttu-id="89104-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="89104-136">Requirement</span></span> | <span data-ttu-id="89104-137">Valore</span><span class="sxs-lookup"><span data-stu-id="89104-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89104-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="89104-138">Minimum supported client</span></span><br/> | <span data-ttu-id="89104-139">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="89104-139">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="89104-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="89104-140">Minimum supported server</span></span><br/> | <span data-ttu-id="89104-141">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="89104-141">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="89104-142">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="89104-142">Namespace</span></span><br/>                | <span data-ttu-id="89104-143">\\ \\ DMMap MDM CIMv2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="89104-143">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="89104-144">MOF</span><span class="sxs-lookup"><span data-stu-id="89104-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="89104-145"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="89104-145"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="89104-146">DLL</span><span class="sxs-lookup"><span data-stu-id="89104-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="89104-147"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="89104-147"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="89104-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="89104-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89104-149">Utilizzo di script di PowerShell con il provider del Bridge WMI</span><span class="sxs-lookup"><span data-stu-id="89104-149">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

