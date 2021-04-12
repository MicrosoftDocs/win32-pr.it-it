---
title: Classe MDM_Firewall_Global02
description: La \_ classe Global02 del firewall MDM \_ viene usata per configurare le impostazioni di Windows Defender Firewall.
ms.assetid: 387a60c6-6dc9-4710-a1e3-0468ac004395
keywords:
- Classe MDM_Firewall_Global02
- Classe MDM_Firewall_Global02, descritta
topic_type:
- apiref
api_name:
- MDM_Firewall_Global02
- MDM_Firewall_Global02.InstanceID
- MDM_Firewall_Global02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1cef2a8b11585848ac10035528db176b78d2e66b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104225205"
---
# <a name="mdm_firewall_global02-class"></a><span data-ttu-id="ac949-105">\_Classe Global02 del firewall MDM \_</span><span class="sxs-lookup"><span data-stu-id="ac949-105">MDM\_Firewall\_Global02 class</span></span>

<span data-ttu-id="ac949-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="ac949-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="ac949-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="ac949-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="ac949-108">La \_ classe Global02 del firewall MDM \_ viene usata per configurare le impostazioni di Windows Defender Firewall.</span><span class="sxs-lookup"><span data-stu-id="ac949-108">The MDM\_Firewall\_Global02 class is used to configure the Windows Defender Firewall settings.</span></span>

<span data-ttu-id="ac949-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="ac949-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac949-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ac949-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Firewall_Global02
{
  string  InstanceID;
  string  ParentID;
  sint32  PolicyVersionSupported;
  sint32  CurrentProfiles;
  boolean DisableStatefulFtp;
  sint32  SaIdleTime;
  sint32  PresharedKeyEncoding;
  sint32  IPsecExempt;
  sint32  CRLcheck;
  string  PolicyVersion;
  string  BinaryVersionSupported;
  boolean OpportunisticallyMatchAuthSetPerKM;
  sint32  EnablePacketQueue;
};
```

## <a name="members"></a><span data-ttu-id="ac949-111">Members</span><span class="sxs-lookup"><span data-stu-id="ac949-111">Members</span></span>

<span data-ttu-id="ac949-112">La **classe \_ \_ Global02 del firewall MDM** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="ac949-112">The **MDM\_Firewall\_Global02** class has these types of members:</span></span>

-   [<span data-ttu-id="ac949-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ac949-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ac949-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ac949-114">Properties</span></span>

<span data-ttu-id="ac949-115">La **classe \_ \_ Global02 del firewall MDM** presenta queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="ac949-115">The **MDM\_Firewall\_Global02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="ac949-116">BinaryVersionSupported</span><span class="sxs-lookup"><span data-stu-id="ac949-116">BinaryVersionSupported</span></span>](/windows/client-management/mdm/firewall-csp#binaryversionsupported)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac949-117">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ac949-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac949-118">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ac949-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac949-119">CRLcheck</span><span class="sxs-lookup"><span data-stu-id="ac949-119">CRLcheck</span></span>](/windows/client-management/mdm/firewall-csp#crlcheck)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac949-120">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ac949-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ac949-121">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ac949-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac949-122">CurrentProfiles</span><span class="sxs-lookup"><span data-stu-id="ac949-122">CurrentProfiles</span></span>](/windows/client-management/mdm/firewall-csp#currentprofiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac949-123">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ac949-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ac949-124">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ac949-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac949-125">DisableStatefulFtp</span><span class="sxs-lookup"><span data-stu-id="ac949-125">DisableStatefulFtp</span></span>](/windows/client-management/mdm/firewall-csp#disablestatefulftp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac949-126">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="ac949-126">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ac949-127">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ac949-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac949-128">EnablePacketQueue</span><span class="sxs-lookup"><span data-stu-id="ac949-128">EnablePacketQueue</span></span>](/windows/client-management/mdm/firewall-csp#enablepacketqueue)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac949-129">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ac949-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ac949-130">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ac949-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ac949-131">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="ac949-131">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac949-132">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ac949-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac949-133">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ac949-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ac949-134">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ac949-134">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac949-135">IPsecExempt</span><span class="sxs-lookup"><span data-stu-id="ac949-135">IPsecExempt</span></span>](/windows/client-management/mdm/firewall-csp#ipsecexempt)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac949-136">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ac949-136">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ac949-137">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ac949-137">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac949-138">OpportunisticallyMatchAuthSetPerKM</span><span class="sxs-lookup"><span data-stu-id="ac949-138">OpportunisticallyMatchAuthSetPerKM</span></span>](/windows/client-management/mdm/firewall-csp#opportunisticallymatchauthsetperkm)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac949-139">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="ac949-139">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ac949-140">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ac949-140">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ac949-141">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="ac949-141">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac949-142">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ac949-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac949-143">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ac949-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ac949-144">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ac949-144">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac949-145">PolicyVersion</span><span class="sxs-lookup"><span data-stu-id="ac949-145">PolicyVersion</span></span>](/windows/client-management/mdm/firewall-csp#policyversion)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac949-146">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ac949-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac949-147">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ac949-147">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac949-148">PolicyVersionSupported</span><span class="sxs-lookup"><span data-stu-id="ac949-148">PolicyVersionSupported</span></span>](/windows/client-management/mdm/firewall-csp#policyversionsupported)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac949-149">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ac949-149">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ac949-150">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ac949-150">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac949-151">PresharedKeyEncoding</span><span class="sxs-lookup"><span data-stu-id="ac949-151">PresharedKeyEncoding</span></span>](/windows/client-management/mdm/firewall-csp#presharedkeyencoding)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac949-152">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ac949-152">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ac949-153">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ac949-153">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac949-154">SaIdleTime</span><span class="sxs-lookup"><span data-stu-id="ac949-154">SaIdleTime</span></span>](/windows/client-management/mdm/firewall-csp#saidletime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac949-155">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ac949-155">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ac949-156">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ac949-156">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ac949-157">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ac949-157">Requirements</span></span>



| <span data-ttu-id="ac949-158">Requisito</span><span class="sxs-lookup"><span data-stu-id="ac949-158">Requirement</span></span> | <span data-ttu-id="ac949-159">Valore</span><span class="sxs-lookup"><span data-stu-id="ac949-159">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac949-160">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ac949-160">Minimum supported client</span></span><br/> | <span data-ttu-id="ac949-161">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="ac949-161">Windows 10 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ac949-162">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ac949-162">Minimum supported server</span></span><br/> | <span data-ttu-id="ac949-163">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="ac949-163">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="ac949-164">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ac949-164">Namespace</span></span><br/>                | <span data-ttu-id="ac949-165">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="ac949-165">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                              |
| <span data-ttu-id="ac949-166">MOF</span><span class="sxs-lookup"><span data-stu-id="ac949-166">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ac949-167"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ac949-167"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl> |
| <span data-ttu-id="ac949-168">DLL</span><span class="sxs-lookup"><span data-stu-id="ac949-168">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ac949-169"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ac949-169"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl>  |



 

