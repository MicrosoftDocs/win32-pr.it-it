---
title: Classe MDM_VPNv2_NativeProfile02
description: La \_ classe MDM VPNv2 \_ NativeProfile2 definisce le informazioni sul profilo quando si usa un protocollo VPN della posta in arrivo di Windows (IKEV2, PPTP, L2TP).
ms.assetid: 50c4adc6-baef-437c-8223-9aeaaec813af
keywords:
- Classe MDM_VPNv2_NativeProfile02
- Classe MDM_VPNv2_NativeProfile02, descritta
topic_type:
- apiref
api_name:
- MDM_VPNv2_NativeProfile02
- MDM_VPNv2_NativeProfile02.InstanceID
- MDM_VPNv2_NativeProfile02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8573975c488df6e5c759e719d5c687f6a71c505
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874393"
---
# <a name="mdm_vpnv2_nativeprofile02-class"></a><span data-ttu-id="756a4-105">\_Classe MDM VPNv2 \_ NativeProfile02</span><span class="sxs-lookup"><span data-stu-id="756a4-105">MDM\_VPNv2\_NativeProfile02 class</span></span>

<span data-ttu-id="756a4-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="756a4-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="756a4-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="756a4-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="756a4-108">La classe **MDM \_ VPNv2 \_ NativeProfile2** definisce le informazioni sul profilo quando si usa un protocollo VPN della posta in arrivo di Windows (IKEV2, PPTP, L2TP).</span><span class="sxs-lookup"><span data-stu-id="756a4-108">The **MDM\_VPNv2\_NativeProfile2** class defines profile information when using a Windows Inbox VPN Protocol (IKEv2, PPTP, L2TP).</span></span>

<span data-ttu-id="756a4-109">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="756a4-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="756a4-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="756a4-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_NativeProfile02
{
  string InstanceID;
  string ParentID;
  string Servers;
  string RoutingPolicyType;
  string NativeProtocolType;
  string L2tpPsk;
};
```

## <a name="members"></a><span data-ttu-id="756a4-111">Members</span><span class="sxs-lookup"><span data-stu-id="756a4-111">Members</span></span>

<span data-ttu-id="756a4-112">La classe **MDM \_ VPNv2 \_ NativeProfile02** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="756a4-112">The **MDM\_VPNv2\_NativeProfile02** class has these types of members:</span></span>

-   [<span data-ttu-id="756a4-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="756a4-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="756a4-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="756a4-114">Properties</span></span>

<span data-ttu-id="756a4-115">La classe **MDM \_ VPNv2 \_ NativeProfile02** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="756a4-115">The **MDM\_VPNv2\_NativeProfile02** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="756a4-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="756a4-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="756a4-117">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="756a4-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="756a4-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="756a4-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="756a4-119">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="756a4-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="756a4-120">Identifica il nome del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="756a4-120">Identifies the name of the parent node.</span></span>

</dd> <dt>

[<span data-ttu-id="756a4-121">L2tpPsk</span><span class="sxs-lookup"><span data-stu-id="756a4-121">L2tpPsk</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-nativeprofile-l2tppsk)
</dt> <dd> <dl> <dt>

<span data-ttu-id="756a4-122">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="756a4-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="756a4-123">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="756a4-123">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="756a4-124">NativeProtocolType</span><span class="sxs-lookup"><span data-stu-id="756a4-124">NativeProtocolType</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-nativeprofile-nativeprotocoltype)
</dt> <dd> <dl> <dt>

<span data-ttu-id="756a4-125">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="756a4-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="756a4-126">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="756a4-126">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="756a4-127">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="756a4-127">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="756a4-128">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="756a4-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="756a4-129">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="756a4-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="756a4-130">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="756a4-130">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="756a4-131">Descrive il percorso completo del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="756a4-131">Describes the full path to the parent node.</span></span> <span data-ttu-id="756a4-132">Per questa classe la stringa è "./Vendor/MSFT/VPNv2/*ProfileName*"</span><span class="sxs-lookup"><span data-stu-id="756a4-132">For this class, the string is "./Vendor/MSFT/VPNv2/*ProfileName*"</span></span>

</dd> <dt>

[<span data-ttu-id="756a4-133">RoutingPolicyType</span><span class="sxs-lookup"><span data-stu-id="756a4-133">RoutingPolicyType</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-trafficfilterlist-trafficfilterid-routingpolicytype)
</dt> <dd> <dl> <dt>

<span data-ttu-id="756a4-134">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="756a4-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="756a4-135">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="756a4-135">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="756a4-136">Server</span><span class="sxs-lookup"><span data-stu-id="756a4-136">Servers</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-nativeprofile-servers)
</dt> <dd> <dl> <dt>

<span data-ttu-id="756a4-137">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="756a4-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="756a4-138">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="756a4-138">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="756a4-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="756a4-139">Requirements</span></span>



| <span data-ttu-id="756a4-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="756a4-140">Requirement</span></span> | <span data-ttu-id="756a4-141">Valore</span><span class="sxs-lookup"><span data-stu-id="756a4-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="756a4-142">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="756a4-142">Minimum supported client</span></span><br/> | <span data-ttu-id="756a4-143">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="756a4-143">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="756a4-144">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="756a4-144">Minimum supported server</span></span><br/> | <span data-ttu-id="756a4-145">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="756a4-145">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="756a4-146">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="756a4-146">Namespace</span></span><br/>                | <span data-ttu-id="756a4-147">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="756a4-147">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="756a4-148">MOF</span><span class="sxs-lookup"><span data-stu-id="756a4-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="756a4-149"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="756a4-149"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="756a4-150">DLL</span><span class="sxs-lookup"><span data-stu-id="756a4-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="756a4-151"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="756a4-151"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="756a4-152">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="756a4-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="756a4-153">Utilizzo di script di PowerShell con il provider del Bridge WMI</span><span class="sxs-lookup"><span data-stu-id="756a4-153">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

