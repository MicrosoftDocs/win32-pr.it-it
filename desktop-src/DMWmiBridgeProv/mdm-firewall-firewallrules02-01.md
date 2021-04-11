---
title: Classe MDM_Firewall_FirewallRules02_01
description: La \_ classe MDM firewall \_ FirewallRules02 \_ 01 viene utilizzata per configurare le impostazioni di Windows Defender Firewall.
ms.assetid: b09cbd98-152e-486c-acb5-4e1d83e5f8e2
keywords:
- Classe MDM_Firewall_FirewallRules02_01
- Classe MDM_Firewall_FirewallRules02_01, descritta
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MDM_Firewall_FirewallRules02_01
- MDM_Firewall_FirewallRules02_01.InstanceID
- MDM_Firewall_FirewallRules02_01.ParentID
- MDM_Firewall_FirewallRules02_01.IcmpTypesAndCodes
- MDM_Firewall_FirewallRules02_01.FriendlyName
api_type:
- DllExport
api_location:
- DMWmiBridgeProv.dll
ms.openlocfilehash: 494be18ece91e7a1776780542f988b80cb822e42
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119439"
---
# <a name="mdm_firewall_firewallrules02_01-class"></a><span data-ttu-id="26d51-105">\_Classe MDM firewall \_ FirewallRules02 \_ 01</span><span class="sxs-lookup"><span data-stu-id="26d51-105">MDM\_Firewall\_FirewallRules02\_01 class</span></span>

<span data-ttu-id="26d51-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="26d51-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="26d51-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="26d51-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="26d51-108">La \_ classe MDM firewall \_ FirewallRules02 \_ 01 viene utilizzata per configurare le impostazioni di Windows Defender Firewall.</span><span class="sxs-lookup"><span data-stu-id="26d51-108">The MDM\_Firewall\_FirewallRules02\_01 class is used to configure the Windows Defender Firewall settings.</span></span>

<span data-ttu-id="26d51-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="26d51-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="26d51-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="26d51-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Firewall_FirewallRules02_01
{
  string  InstanceID;
  string  ParentID;
  sint32  Protocol;
  string  LocalPortRanges;
  string  RemotePortRanges;
  string  LocalAddressRanges;
  string  RemoteAddressRanges;
  string  Description;
  boolean Enabled;
  sint32  Profiles;
  string  Direction;
  string  InterfaceTypes;
  string  IcmpTypesAndCodes;
  boolean EdgeTraversal;
  string  LocalUserAuthorizedList;
  string  Status;
  string  FriendlyName;
  string  Name;
};
```

## <a name="members"></a><span data-ttu-id="26d51-111">Members</span><span class="sxs-lookup"><span data-stu-id="26d51-111">Members</span></span>

<span data-ttu-id="26d51-112">La classe **MDM \_ firewall \_ FirewallRules02 \_ 01** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="26d51-112">The **MDM\_Firewall\_FirewallRules02\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="26d51-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="26d51-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="26d51-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="26d51-114">Properties</span></span>

<span data-ttu-id="26d51-115">La classe **MDM \_ firewall \_ FirewallRules02 \_ 01** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="26d51-115">The **MDM\_Firewall\_FirewallRules02\_01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="26d51-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="26d51-116">Description</span></span>](/windows/client-management/mdm/firewall-csp#description)
</dt> <dd> <dl> <dt>

<span data-ttu-id="26d51-117">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="26d51-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="26d51-118">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="26d51-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="26d51-119">Direzione</span><span class="sxs-lookup"><span data-stu-id="26d51-119">Direction</span></span>](/windows/client-management/mdm/firewall-csp#direction)
</dt> <dd> <dl> <dt>

<span data-ttu-id="26d51-120">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="26d51-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="26d51-121">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="26d51-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="26d51-122">EdgeTraversal</span><span class="sxs-lookup"><span data-stu-id="26d51-122">EdgeTraversal</span></span>](/windows/client-management/mdm/firewall-csp#edgetraversal)
</dt> <dd> <dl> <dt>

<span data-ttu-id="26d51-123">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="26d51-123">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="26d51-124">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="26d51-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="26d51-125">Enabled</span><span class="sxs-lookup"><span data-stu-id="26d51-125">Enabled</span></span>](/windows/client-management/mdm/firewall-csp#enabled)
</dt> <dd> <dl> <dt>

<span data-ttu-id="26d51-126">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="26d51-126">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="26d51-127">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="26d51-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="26d51-128">**FriendlyName**</span><span class="sxs-lookup"><span data-stu-id="26d51-128">**FriendlyName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26d51-129">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="26d51-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="26d51-130">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="26d51-130">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="26d51-131">TBD</span><span class="sxs-lookup"><span data-stu-id="26d51-131">TBD</span></span>

</dd> <dt>

<span data-ttu-id="26d51-132">**IcmpTypesAndCodes**</span><span class="sxs-lookup"><span data-stu-id="26d51-132">**IcmpTypesAndCodes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26d51-133">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="26d51-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="26d51-134">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="26d51-134">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="26d51-135">TBD</span><span class="sxs-lookup"><span data-stu-id="26d51-135">TBD</span></span>

</dd> <dt>

<span data-ttu-id="26d51-136">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="26d51-136">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26d51-137">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="26d51-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="26d51-138">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="26d51-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26d51-139">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="26d51-139">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="26d51-140">InterfaceTypes</span><span class="sxs-lookup"><span data-stu-id="26d51-140">InterfaceTypes</span></span>](/windows/client-management/mdm/firewall-csp#interfacetypes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="26d51-141">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="26d51-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="26d51-142">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="26d51-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="26d51-143">LocalAddressRanges</span><span class="sxs-lookup"><span data-stu-id="26d51-143">LocalAddressRanges</span></span>](/windows/client-management/mdm/firewall-csp#localaddressranges)
</dt> <dd> <dl> <dt>

<span data-ttu-id="26d51-144">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="26d51-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="26d51-145">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="26d51-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="26d51-146">LocalPortRanges</span><span class="sxs-lookup"><span data-stu-id="26d51-146">LocalPortRanges</span></span>](/windows/client-management/mdm/firewall-csp#localportranges)
</dt> <dd> <dl> <dt>

<span data-ttu-id="26d51-147">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="26d51-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="26d51-148">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="26d51-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="26d51-149">LocalUserAuthorizedList</span><span class="sxs-lookup"><span data-stu-id="26d51-149">LocalUserAuthorizedList</span></span>](/windows/client-management/mdm/firewall-csp#localuserauthorizedlist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="26d51-150">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="26d51-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="26d51-151">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="26d51-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="26d51-152">Nome</span><span class="sxs-lookup"><span data-stu-id="26d51-152">Name</span></span>](/windows/client-management/mdm/firewall-csp#name)
</dt> <dd> <dl> <dt>

<span data-ttu-id="26d51-153">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="26d51-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="26d51-154">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="26d51-154">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="26d51-155">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="26d51-155">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26d51-156">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="26d51-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="26d51-157">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="26d51-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26d51-158">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="26d51-158">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="26d51-159">Profili</span><span class="sxs-lookup"><span data-stu-id="26d51-159">Profiles</span></span>](/windows/client-management/mdm/firewall-csp#profiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="26d51-160">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="26d51-160">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="26d51-161">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="26d51-161">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="26d51-162">Protocollo</span><span class="sxs-lookup"><span data-stu-id="26d51-162">Protocol</span></span>](/windows/client-management/mdm/firewall-csp#protocol)
</dt> <dd> <dl> <dt>

<span data-ttu-id="26d51-163">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="26d51-163">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="26d51-164">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="26d51-164">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="26d51-165">RemoteAddressRanges</span><span class="sxs-lookup"><span data-stu-id="26d51-165">RemoteAddressRanges</span></span>](/windows/client-management/mdm/firewall-csp#remoteaddressranges)
</dt> <dd> <dl> <dt>

<span data-ttu-id="26d51-166">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="26d51-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="26d51-167">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="26d51-167">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="26d51-168">RemotePortRanges</span><span class="sxs-lookup"><span data-stu-id="26d51-168">RemotePortRanges</span></span>](/windows/client-management/mdm/firewall-csp#remoteportranges)
</dt> <dd> <dl> <dt>

<span data-ttu-id="26d51-169">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="26d51-169">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="26d51-170">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="26d51-170">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="26d51-171">Status</span><span class="sxs-lookup"><span data-stu-id="26d51-171">Status</span></span>](/windows/client-management/mdm/firewall-csp#status)
</dt> <dd> <dl> <dt>

<span data-ttu-id="26d51-172">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="26d51-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="26d51-173">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="26d51-173">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="26d51-174">Requisiti</span><span class="sxs-lookup"><span data-stu-id="26d51-174">Requirements</span></span>



| <span data-ttu-id="26d51-175">Requisito</span><span class="sxs-lookup"><span data-stu-id="26d51-175">Requirement</span></span> | <span data-ttu-id="26d51-176">Valore</span><span class="sxs-lookup"><span data-stu-id="26d51-176">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="26d51-177">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="26d51-177">Minimum supported client</span></span><br/> | <span data-ttu-id="26d51-178">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="26d51-178">Windows 10 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="26d51-179">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="26d51-179">Minimum supported server</span></span><br/> | <span data-ttu-id="26d51-180">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="26d51-180">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="26d51-181">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="26d51-181">Namespace</span></span><br/>                | <span data-ttu-id="26d51-182">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="26d51-182">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                              |
| <span data-ttu-id="26d51-183">MOF</span><span class="sxs-lookup"><span data-stu-id="26d51-183">MOF</span></span><br/>                      | <dl> <span data-ttu-id="26d51-184"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="26d51-184"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl> |
| <span data-ttu-id="26d51-185">DLL</span><span class="sxs-lookup"><span data-stu-id="26d51-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="26d51-186"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="26d51-186"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl>  |



 

