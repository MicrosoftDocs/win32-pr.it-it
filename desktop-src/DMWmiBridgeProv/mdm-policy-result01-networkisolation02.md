---
title: Classe MDM_Policy_Result01_NetworkIsolation02
description: La \_ \_ classe Result01 NetworkIsolation02 dei criteri MDM \_ rappresenta i criteri del browser disponibili.
ms.assetid: f44f43fb-813b-4d40-a56c-0c497e004a8a
keywords:
- Classe MDM_Policy_Result01_NetworkIsolation02
- Classe MDM_Policy_Result01_NetworkIsolation02, descritta
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_NetworkIsolation02
- MDM_Policy_Result01_NetworkIsolation02.InstanceID
- MDM_Policy_Result01_NetworkIsolation02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5611d7e00ab0fa5210a657b55a3f2990fdf40880
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119559"
---
# <a name="mdm_policy_result01_networkisolation02-class"></a><span data-ttu-id="f881b-105">\_ \_ Classe Result01 NetworkIsolation02 di criteri \_ MDM</span><span class="sxs-lookup"><span data-stu-id="f881b-105">MDM\_Policy\_Result01\_NetworkIsolation02 class</span></span>

<span data-ttu-id="f881b-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="f881b-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="f881b-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="f881b-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="f881b-108">La **classe \_ \_ Result01 \_ NetworkIsolation02 dei criteri MDM** rappresenta i criteri del browser disponibili.</span><span class="sxs-lookup"><span data-stu-id="f881b-108">The **MDM\_Policy\_Result01\_NetworkIsolation02** class represents the browser policies available.</span></span>

<span data-ttu-id="f881b-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="f881b-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f881b-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f881b-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_NetworkIsolation02
{
  string InstanceID;
  string ParentID;
  string EnterpriseIPRange;
  sint32 EnterpriseIPRangesAreAuthoritative;
  string EnterpriseNetworkDomainNames;
  string EnterpriseProxyServers;
  sint32 EnterpriseProxyServersAreAuthoritative;
  string EnterpriseCloudResources;
  string EnterpriseInternalProxyServers;
  string NeutralResources;
};
```

## <a name="members"></a><span data-ttu-id="f881b-111">Members</span><span class="sxs-lookup"><span data-stu-id="f881b-111">Members</span></span>

<span data-ttu-id="f881b-112">La **classe \_ \_ Result01 \_ NetworkIsolation02 dei criteri MDM** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="f881b-112">The **MDM\_Policy\_Result01\_NetworkIsolation02** class has these types of members:</span></span>

-   [<span data-ttu-id="f881b-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f881b-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f881b-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f881b-114">Properties</span></span>

<span data-ttu-id="f881b-115">La **classe \_ \_ \_ NetworkIsolation02 dei criteri MDM Result01** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="f881b-115">The **MDM\_Policy\_Result01\_NetworkIsolation02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="f881b-116">EnterpriseCloudResources</span><span class="sxs-lookup"><span data-stu-id="f881b-116">EnterpriseCloudResources</span></span>](/windows/client-management/mdm/policy-csp-networkisolation#networkisolation-enterprisecloudresources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f881b-117">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f881b-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f881b-118">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="f881b-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f881b-119">EnterpriseInternalProxyServers</span><span class="sxs-lookup"><span data-stu-id="f881b-119">EnterpriseInternalProxyServers</span></span>](/windows/client-management/mdm/policy-csp-networkisolation#networkisolation-enterpriseinternalproxyservers)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f881b-120">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f881b-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f881b-121">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="f881b-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f881b-122">EnterpriseIPRange</span><span class="sxs-lookup"><span data-stu-id="f881b-122">EnterpriseIPRange</span></span>](/windows/client-management/mdm/policy-csp-networkisolation#networkisolation-enterpriseiprange)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f881b-123">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f881b-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f881b-124">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="f881b-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f881b-125">EnterpriseIPRangesAreAuthoritative</span><span class="sxs-lookup"><span data-stu-id="f881b-125">EnterpriseIPRangesAreAuthoritative</span></span>](/windows/client-management/mdm/policy-csp-networkisolation#networkisolation-enterpriseiprangesareauthoritative)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f881b-126">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="f881b-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f881b-127">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="f881b-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f881b-128">EnterpriseNetworkDomainNames</span><span class="sxs-lookup"><span data-stu-id="f881b-128">EnterpriseNetworkDomainNames</span></span>](/windows/client-management/mdm/policy-csp-networkisolation#networkisolation-enterprisenetworkdomainnames)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f881b-129">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f881b-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f881b-130">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="f881b-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f881b-131">EnterpriseProxyServers</span><span class="sxs-lookup"><span data-stu-id="f881b-131">EnterpriseProxyServers</span></span>](/windows/client-management/mdm/policy-csp-networkisolation#networkisolation-enterpriseproxyservers)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f881b-132">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f881b-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f881b-133">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="f881b-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f881b-134">EnterpriseProxyServersAreAuthoritative</span><span class="sxs-lookup"><span data-stu-id="f881b-134">EnterpriseProxyServersAreAuthoritative</span></span>](/windows/client-management/mdm/policy-csp-networkisolation#networkisolation-enterpriseproxyserversareauthoritative)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f881b-135">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="f881b-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f881b-136">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="f881b-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f881b-137">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="f881b-137">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f881b-138">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f881b-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f881b-139">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f881b-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f881b-140">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f881b-140">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="f881b-141">Identifica il nome del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="f881b-141">Identifies the name of the parent node.</span></span> <span data-ttu-id="f881b-142">Per questa classe la stringa è "NetworkIsolation".</span><span class="sxs-lookup"><span data-stu-id="f881b-142">For this class, the string is "NetworkIsolation".</span></span>

</dd> <dt>

[<span data-ttu-id="f881b-143">NeutralResources</span><span class="sxs-lookup"><span data-stu-id="f881b-143">NeutralResources</span></span>](/windows/client-management/mdm/policy-csp-networkisolation#networkisolation-neutralresources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f881b-144">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f881b-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f881b-145">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="f881b-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f881b-146">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="f881b-146">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f881b-147">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f881b-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f881b-148">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f881b-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f881b-149">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f881b-149">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="f881b-150">Descrive il percorso completo del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="f881b-150">Describes the full path to the parent node.</span></span> <span data-ttu-id="f881b-151">Per questa classe la stringa è "./Vendor/MSFT/Policy/Result"</span><span class="sxs-lookup"><span data-stu-id="f881b-151">For this class, the string is "./Vendor/MSFT/Policy/Result"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f881b-152">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f881b-152">Requirements</span></span>



| <span data-ttu-id="f881b-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="f881b-153">Requirement</span></span> | <span data-ttu-id="f881b-154">Valore</span><span class="sxs-lookup"><span data-stu-id="f881b-154">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f881b-155">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f881b-155">Minimum supported client</span></span><br/> | <span data-ttu-id="f881b-156">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="f881b-156">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f881b-157">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f881b-157">Minimum supported server</span></span><br/> | <span data-ttu-id="f881b-158">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="f881b-158">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="f881b-159">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f881b-159">Namespace</span></span><br/>                | <span data-ttu-id="f881b-160">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="f881b-160">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="f881b-161">MOF</span><span class="sxs-lookup"><span data-stu-id="f881b-161">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f881b-162"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f881b-162"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="f881b-163">DLL</span><span class="sxs-lookup"><span data-stu-id="f881b-163">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f881b-164"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f881b-164"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

