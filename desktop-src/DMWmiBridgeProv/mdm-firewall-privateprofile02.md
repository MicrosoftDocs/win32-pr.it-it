---
title: Classe MDM_Firewall_PrivateProfile02
description: La \_ classe PrivateProfile02 del firewall MDM \_ viene usata per configurare le impostazioni di Windows Defender Firewall.
ms.assetid: 9d25c181-e9a8-4f63-b276-b22676842667
keywords:
- Classe MDM_Firewall_PrivateProfile02
- Classe MDM_Firewall_PrivateProfile02, descritta
topic_type:
- apiref
api_name:
- MDM_Firewall_PrivateProfile02
- MDM_Firewall_PrivateProfile02.InstanceID
- MDM_Firewall_PrivateProfile02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57812ef7c8550937b009e4ff4855321983391585
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301391"
---
# <a name="mdm_firewall_privateprofile02-class"></a><span data-ttu-id="d3c5c-105">\_Classe PrivateProfile02 del firewall MDM \_</span><span class="sxs-lookup"><span data-stu-id="d3c5c-105">MDM\_Firewall\_PrivateProfile02 class</span></span>

<span data-ttu-id="d3c5c-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="d3c5c-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="d3c5c-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="d3c5c-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="d3c5c-108">La \_ classe PrivateProfile02 del firewall MDM \_ viene usata per configurare le impostazioni di Windows Defender Firewall.</span><span class="sxs-lookup"><span data-stu-id="d3c5c-108">The MDM\_Firewall\_PrivateProfile02 class is used to configure the Windows Defender Firewall settings.</span></span>

<span data-ttu-id="d3c5c-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="d3c5c-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3c5c-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d3c5c-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Firewall_PrivateProfile02
{
  string InstanceID;
  string ParentID;
  sint32 EnableFirewall;
  sint32 DisableStealthMode;
  sint32 Shielded;
  sint32 DisableUnicastResponsesToMulticastBroadcast;
  sint32 DisableInboundNotifications;
  sint32 AuthAppsAllowUserPrefMerge;
  sint32 GlobalPortsAllowUserPrefMerge;
  sint32 AllowLocalPolicyMerge;
  sint32 AllowLocalIpsecPolicyMerge;
  sint32 DefaultOutboundAction;
  sint32 DefaultInboundAction;
  sint32 DisableStealthModeIpsecSecuredPacketExemption;
};
```

## <a name="members"></a><span data-ttu-id="d3c5c-111">Members</span><span class="sxs-lookup"><span data-stu-id="d3c5c-111">Members</span></span>

<span data-ttu-id="d3c5c-112">La **classe \_ \_ PrivateProfile02 del firewall MDM** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="d3c5c-112">The **MDM\_Firewall\_PrivateProfile02** class has these types of members:</span></span>

-   [<span data-ttu-id="d3c5c-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d3c5c-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d3c5c-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d3c5c-114">Properties</span></span>

<span data-ttu-id="d3c5c-115">La **classe \_ \_ PrivateProfile02 del firewall MDM** presenta queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="d3c5c-115">The **MDM\_Firewall\_PrivateProfile02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="d3c5c-116">AllowLocalIpsecPolicyMerge</span><span class="sxs-lookup"><span data-stu-id="d3c5c-116">AllowLocalIpsecPolicyMerge</span></span>](/windows/client-management/mdm/firewall-csp#allowlocalipsecpolicymerge)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3c5c-117">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d3c5c-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d3c5c-118">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="d3c5c-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d3c5c-119">AllowLocalPolicyMerge</span><span class="sxs-lookup"><span data-stu-id="d3c5c-119">AllowLocalPolicyMerge</span></span>](/windows/client-management/mdm/firewall-csp#allowlocalpolicymerge)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3c5c-120">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d3c5c-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d3c5c-121">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="d3c5c-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d3c5c-122">AuthAppsAllowUserPrefMerge</span><span class="sxs-lookup"><span data-stu-id="d3c5c-122">AuthAppsAllowUserPrefMerge</span></span>](/windows/client-management/mdm/firewall-csp#authappsallowuserprefmerge)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3c5c-123">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d3c5c-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d3c5c-124">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="d3c5c-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d3c5c-125">DefaultInboundAction</span><span class="sxs-lookup"><span data-stu-id="d3c5c-125">DefaultInboundAction</span></span>](/windows/client-management/mdm/firewall-csp#defaultinboundaction)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3c5c-126">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d3c5c-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d3c5c-127">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="d3c5c-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d3c5c-128">DefaultOutboundAction</span><span class="sxs-lookup"><span data-stu-id="d3c5c-128">DefaultOutboundAction</span></span>](/windows/client-management/mdm/firewall-csp#defaultoutboundaction)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3c5c-129">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d3c5c-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d3c5c-130">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="d3c5c-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d3c5c-131">DisableInboundNotifications</span><span class="sxs-lookup"><span data-stu-id="d3c5c-131">DisableInboundNotifications</span></span>](/windows/client-management/mdm/firewall-csp#disableinboundnotifications)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3c5c-132">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d3c5c-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d3c5c-133">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="d3c5c-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d3c5c-134">DisableStealthMode</span><span class="sxs-lookup"><span data-stu-id="d3c5c-134">DisableStealthMode</span></span>](/windows/client-management/mdm/firewall-csp#disablestealthmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3c5c-135">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d3c5c-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d3c5c-136">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="d3c5c-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d3c5c-137">DisableStealthModeIpsecSecuredPacketExemption</span><span class="sxs-lookup"><span data-stu-id="d3c5c-137">DisableStealthModeIpsecSecuredPacketExemption</span></span>](/windows/client-management/mdm/firewall-csp#disablestealthmodeipsecsecuredpacketexemption)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3c5c-138">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d3c5c-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d3c5c-139">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="d3c5c-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d3c5c-140">DisableUnicastResponsesToMulticastBroadcast</span><span class="sxs-lookup"><span data-stu-id="d3c5c-140">DisableUnicastResponsesToMulticastBroadcast</span></span>](/windows/client-management/mdm/firewall-csp#disableunicastresponsestomulticastbroadcast)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3c5c-141">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d3c5c-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d3c5c-142">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="d3c5c-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d3c5c-143">EnableFirewall</span><span class="sxs-lookup"><span data-stu-id="d3c5c-143">EnableFirewall</span></span>](/windows/client-management/mdm/firewall-csp#enablefirewall)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3c5c-144">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d3c5c-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d3c5c-145">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="d3c5c-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d3c5c-146">GlobalPortsAllowUserPrefMerge</span><span class="sxs-lookup"><span data-stu-id="d3c5c-146">GlobalPortsAllowUserPrefMerge</span></span>](/windows/client-management/mdm/firewall-csp#globalportsallowuserprefmerge)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3c5c-147">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d3c5c-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d3c5c-148">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="d3c5c-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d3c5c-149">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="d3c5c-149">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3c5c-150">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d3c5c-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d3c5c-151">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d3c5c-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d3c5c-152">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d3c5c-152">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d3c5c-153">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="d3c5c-153">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3c5c-154">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d3c5c-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d3c5c-155">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d3c5c-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d3c5c-156">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d3c5c-156">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d3c5c-157">Schermato</span><span class="sxs-lookup"><span data-stu-id="d3c5c-157">Shielded</span></span>](/windows/client-management/mdm/firewall-csp#shielded)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3c5c-158">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d3c5c-158">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d3c5c-159">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="d3c5c-159">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d3c5c-160">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d3c5c-160">Requirements</span></span>



| <span data-ttu-id="d3c5c-161">Requisito</span><span class="sxs-lookup"><span data-stu-id="d3c5c-161">Requirement</span></span> | <span data-ttu-id="d3c5c-162">Valore</span><span class="sxs-lookup"><span data-stu-id="d3c5c-162">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3c5c-163">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d3c5c-163">Minimum supported client</span></span><br/> | <span data-ttu-id="d3c5c-164">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="d3c5c-164">Windows 10 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d3c5c-165">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d3c5c-165">Minimum supported server</span></span><br/> | <span data-ttu-id="d3c5c-166">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="d3c5c-166">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="d3c5c-167">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="d3c5c-167">Namespace</span></span><br/>                | <span data-ttu-id="d3c5c-168">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="d3c5c-168">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                              |
| <span data-ttu-id="d3c5c-169">MOF</span><span class="sxs-lookup"><span data-stu-id="d3c5c-169">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d3c5c-170"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d3c5c-170"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl> |
| <span data-ttu-id="d3c5c-171">DLL</span><span class="sxs-lookup"><span data-stu-id="d3c5c-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d3c5c-172"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d3c5c-172"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl>  |



 

