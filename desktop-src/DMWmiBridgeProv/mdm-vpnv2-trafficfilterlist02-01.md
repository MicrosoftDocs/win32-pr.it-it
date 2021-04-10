---
title: Classe MDM_VPNv2_TrafficFilterList02_01
description: La \_ classe MDM VPNv2 \_ TrafficFilterList02 \_ 01 contiene un elenco facoltativo di regole. Solo il traffico che corrisponde a queste regole può essere inviato tramite l'interfaccia VPN.
ms.assetid: 3cffe96d-7454-43a1-aa5b-33e820369e7e
keywords:
- Classe MDM_VPNv2_TrafficFilterList02_01
- Classe MDM_VPNv2_TrafficFilterList02_01, descritta
topic_type:
- apiref
api_name:
- MDM_VPNv2_TrafficFilterList02_01
- MDM_VPNv2_TrafficFilterList02_01.InstanceID
- MDM_VPNv2_TrafficFilterList02_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3005026a85aa118a4122e073579fcb06389a9fd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120622"
---
# <a name="mdm_vpnv2_trafficfilterlist02_01-class"></a><span data-ttu-id="76e84-106">\_Classe MDM VPNv2 \_ TrafficFilterList02 \_ 01</span><span class="sxs-lookup"><span data-stu-id="76e84-106">MDM\_VPNv2\_TrafficFilterList02\_01 class</span></span>

<span data-ttu-id="76e84-107">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="76e84-107">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="76e84-108">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="76e84-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="76e84-109">La classe **MDM \_ VPNv2 \_ TrafficFilterList02 \_ 01** contiene un elenco facoltativo di regole.</span><span class="sxs-lookup"><span data-stu-id="76e84-109">The **MDM\_VPNv2\_TrafficFilterList02\_01** class contains an optional list of rules.</span></span> <span data-ttu-id="76e84-110">Solo il traffico che corrisponde a queste regole può essere inviato tramite l'interfaccia VPN.</span><span class="sxs-lookup"><span data-stu-id="76e84-110">Only traffic that matches these rules can be sent via the VPN Interface.</span></span>

<span data-ttu-id="76e84-111">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="76e84-111">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="76e84-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="76e84-112">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_TrafficFilterList02_01
{
  string InstanceID;
  string ParentID;
  string Claims;
  sint32 Protocol;
  string LocalPortRanges;
  string RemotePortRanges;
  string LocalAddressRanges;
  string RemoteAddressRanges;
  string RoutingPolicyType;
};
```

## <a name="members"></a><span data-ttu-id="76e84-113">Members</span><span class="sxs-lookup"><span data-stu-id="76e84-113">Members</span></span>

<span data-ttu-id="76e84-114">La classe **MDM \_ VPNv2 \_ TrafficFilterList02 \_ 01** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="76e84-114">The **MDM\_VPNv2\_TrafficFilterList02\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="76e84-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="76e84-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="76e84-116">Proprietà</span><span class="sxs-lookup"><span data-stu-id="76e84-116">Properties</span></span>

<span data-ttu-id="76e84-117">La classe **MDM \_ VPNv2 \_ TrafficFilterList02 \_ 01** presenta queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="76e84-117">The **MDM\_VPNv2\_TrafficFilterList02\_01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="76e84-118">Richieste</span><span class="sxs-lookup"><span data-stu-id="76e84-118">Claims</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-trafficfilterlist-trafficfilterid-claims)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e84-119">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="76e84-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e84-120">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="76e84-120">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="76e84-121">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="76e84-121">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e84-122">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="76e84-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e84-123">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="76e84-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="76e84-124">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="76e84-124">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="76e84-125">Identifica il nome del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="76e84-125">Identifies the name of the parent node.</span></span>

</dd> <dt>

[<span data-ttu-id="76e84-126">LocalAddressRanges</span><span class="sxs-lookup"><span data-stu-id="76e84-126">LocalAddressRanges</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-trafficfilterlist-trafficfilterid-localaddressranges)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e84-127">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="76e84-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e84-128">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="76e84-128">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e84-129">LocalPortRanges</span><span class="sxs-lookup"><span data-stu-id="76e84-129">LocalPortRanges</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-trafficfilterlist-trafficfilterid-localportranges)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e84-130">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="76e84-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e84-131">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="76e84-131">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="76e84-132">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="76e84-132">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e84-133">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="76e84-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e84-134">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="76e84-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="76e84-135">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="76e84-135">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="76e84-136">Descrive il percorso completo del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="76e84-136">Describes the full path to the parent node.</span></span> <span data-ttu-id="76e84-137">Per questa classe la stringa è "./Vendor/MSFT/VPNv2/*ProfileName*/TrafficFilterList"</span><span class="sxs-lookup"><span data-stu-id="76e84-137">For this class, the string is "./Vendor/MSFT/VPNv2/*ProfileName*/TrafficFilterList"</span></span>

</dd> <dt>

[<span data-ttu-id="76e84-138">Protocollo</span><span class="sxs-lookup"><span data-stu-id="76e84-138">Protocol</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-trafficfilterlist-trafficfilterid-protocol)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e84-139">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="76e84-139">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="76e84-140">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="76e84-140">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e84-141">RemoteAddressRanges</span><span class="sxs-lookup"><span data-stu-id="76e84-141">RemoteAddressRanges</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-trafficfilterlist-trafficfilterid-remoteaddressranges)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e84-142">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="76e84-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e84-143">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="76e84-143">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e84-144">RemotePortRanges</span><span class="sxs-lookup"><span data-stu-id="76e84-144">RemotePortRanges</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-trafficfilterlist-trafficfilterid-remoteportranges)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e84-145">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="76e84-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e84-146">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="76e84-146">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="76e84-147">RoutingPolicyType</span><span class="sxs-lookup"><span data-stu-id="76e84-147">RoutingPolicyType</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-trafficfilterlist-trafficfilterid-routingpolicytype)
</dt> <dd> <dl> <dt>

<span data-ttu-id="76e84-148">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="76e84-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76e84-149">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="76e84-149">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="76e84-150">Requisiti</span><span class="sxs-lookup"><span data-stu-id="76e84-150">Requirements</span></span>



| <span data-ttu-id="76e84-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="76e84-151">Requirement</span></span> | <span data-ttu-id="76e84-152">Valore</span><span class="sxs-lookup"><span data-stu-id="76e84-152">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="76e84-153">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="76e84-153">Minimum supported client</span></span><br/> | <span data-ttu-id="76e84-154">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="76e84-154">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="76e84-155">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="76e84-155">Minimum supported server</span></span><br/> | <span data-ttu-id="76e84-156">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="76e84-156">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="76e84-157">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="76e84-157">Namespace</span></span><br/>                | <span data-ttu-id="76e84-158">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="76e84-158">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="76e84-159">MOF</span><span class="sxs-lookup"><span data-stu-id="76e84-159">MOF</span></span><br/>                      | <dl> <span data-ttu-id="76e84-160"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="76e84-160"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="76e84-161">DLL</span><span class="sxs-lookup"><span data-stu-id="76e84-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="76e84-162"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="76e84-162"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="76e84-163">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="76e84-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76e84-164">Utilizzo di script di PowerShell con il provider del Bridge WMI</span><span class="sxs-lookup"><span data-stu-id="76e84-164">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

