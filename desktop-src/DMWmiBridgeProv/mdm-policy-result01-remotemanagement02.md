---
title: Classe MDM_Policy_Result01_RemoteManagement02
description: La \_ classe RemoteManagement02 dei criteri MDM \_ Result01 \_ rappresenta i criteri di gestione remota.
ms.assetid: f6eb96ff-a40e-4602-a812-786d1a89bf12
keywords:
- Classe MDM_Policy_Result01_RemoteManagement02
- Classe MDM_Policy_Result01_RemoteManagement02, descritta
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_RemoteManagement02
- MDM_Policy_Result01_RemoteManagement02.InstanceID
- MDM_Policy_Result01_RemoteManagement02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0a60228e39c8e1d6604534c8bd052ec7d40105e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475317"
---
# <a name="mdm_policy_result01_remotemanagement02-class"></a><span data-ttu-id="d370d-105">\_ \_ Classe Result01 RemoteManagement02 di criteri \_ MDM</span><span class="sxs-lookup"><span data-stu-id="d370d-105">MDM\_Policy\_Result01\_RemoteManagement02 class</span></span>

<span data-ttu-id="d370d-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="d370d-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="d370d-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="d370d-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="d370d-108">La \_ classe RemoteManagement02 dei criteri MDM \_ Result01 \_ rappresenta i criteri di gestione remota.</span><span class="sxs-lookup"><span data-stu-id="d370d-108">The MDM\_Policy\_Result01\_RemoteManagement02 class represents the remote management policies.</span></span>

<span data-ttu-id="d370d-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="d370d-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d370d-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d370d-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_RemoteManagement02
{
  string InstanceID;
  string ParentID;
  string AllowBasicAuthentication_Client;
  string AllowBasicAuthentication_Service;
  string AllowCredSSPAuthenticationClient;
  string AllowCredSSPAuthenticationService;
  string AllowRemoteServerManagement;
  string AllowUnencryptedTraffic_Client;
  string AllowUnencryptedTraffic_Service;
  string DisallowDigestAuthentication;
  string DisallowNegotiateAuthenticationClient;
  string DisallowNegotiateAuthenticationService;
  string DisallowStoringOfRunAsCredentials;
  string SpecifyChannelBindingTokenHardeningLevel;
  string TrustedHosts;
  string TurnOnCompatibilityHTTPListener;
  string TurnOnCompatibilityHTTPSListener;
};
```

## <a name="members"></a><span data-ttu-id="d370d-111">Members</span><span class="sxs-lookup"><span data-stu-id="d370d-111">Members</span></span>

<span data-ttu-id="d370d-112">La **classe \_ \_ Result01 \_ RemoteManagement02 dei criteri MDM** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="d370d-112">The **MDM\_Policy\_Result01\_RemoteManagement02** class has these types of members:</span></span>

-   [<span data-ttu-id="d370d-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d370d-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d370d-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d370d-114">Properties</span></span>

<span data-ttu-id="d370d-115">La **classe \_ \_ \_ RemoteManagement02 dei criteri MDM Result01** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="d370d-115">The **MDM\_Policy\_Result01\_RemoteManagement02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="d370d-116">\_Client AllowBasicAuthentication</span><span class="sxs-lookup"><span data-stu-id="d370d-116">AllowBasicAuthentication\_Client</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-allowbasicauthentication-client)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d370d-117">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d370d-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d370d-118">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="d370d-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d370d-119">\_Servizio AllowBasicAuthentication</span><span class="sxs-lookup"><span data-stu-id="d370d-119">AllowBasicAuthentication\_Service</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-allowbasicauthentication-service)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d370d-120">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d370d-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d370d-121">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="d370d-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d370d-122">AllowCredSSPAuthenticationClient</span><span class="sxs-lookup"><span data-stu-id="d370d-122">AllowCredSSPAuthenticationClient</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-allowcredsspauthenticationclient)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d370d-123">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d370d-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d370d-124">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="d370d-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d370d-125">AllowCredSSPAuthenticationService</span><span class="sxs-lookup"><span data-stu-id="d370d-125">AllowCredSSPAuthenticationService</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-allowcredsspauthenticationservice)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d370d-126">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d370d-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d370d-127">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="d370d-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d370d-128">AllowRemoteServerManagement</span><span class="sxs-lookup"><span data-stu-id="d370d-128">AllowRemoteServerManagement</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-allowremoteservermanagement)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d370d-129">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d370d-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d370d-130">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="d370d-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d370d-131">\_Client AllowUnencryptedTraffic</span><span class="sxs-lookup"><span data-stu-id="d370d-131">AllowUnencryptedTraffic\_Client</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-allowunencryptedtraffic-client)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d370d-132">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d370d-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d370d-133">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="d370d-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d370d-134">\_Servizio AllowUnencryptedTraffic</span><span class="sxs-lookup"><span data-stu-id="d370d-134">AllowUnencryptedTraffic\_Service</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-allowunencryptedtraffic-service)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d370d-135">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d370d-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d370d-136">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="d370d-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d370d-137">DisallowDigestAuthentication</span><span class="sxs-lookup"><span data-stu-id="d370d-137">DisallowDigestAuthentication</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-disallowdigestauthentication)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d370d-138">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d370d-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d370d-139">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="d370d-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d370d-140">DisallowNegotiateAuthenticationClient</span><span class="sxs-lookup"><span data-stu-id="d370d-140">DisallowNegotiateAuthenticationClient</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-disallownegotiateauthenticationclient)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d370d-141">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d370d-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d370d-142">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="d370d-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d370d-143">DisallowNegotiateAuthenticationService</span><span class="sxs-lookup"><span data-stu-id="d370d-143">DisallowNegotiateAuthenticationService</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-disallownegotiateauthenticationservice)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d370d-144">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d370d-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d370d-145">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="d370d-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d370d-146">DisallowStoringOfRunAsCredentials</span><span class="sxs-lookup"><span data-stu-id="d370d-146">DisallowStoringOfRunAsCredentials</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-disallowstoringofrunascredentials)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d370d-147">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d370d-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d370d-148">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="d370d-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d370d-149">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="d370d-149">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d370d-150">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d370d-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d370d-151">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d370d-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d370d-152">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d370d-152">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d370d-153">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="d370d-153">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d370d-154">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d370d-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d370d-155">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d370d-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d370d-156">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d370d-156">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d370d-157">SpecifyChannelBindingTokenHardeningLevel</span><span class="sxs-lookup"><span data-stu-id="d370d-157">SpecifyChannelBindingTokenHardeningLevel</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-specifychannelbindingtokenhardeninglevel)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d370d-158">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d370d-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d370d-159">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="d370d-159">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d370d-160">TrustedHosts</span><span class="sxs-lookup"><span data-stu-id="d370d-160">TrustedHosts</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-trustedhosts)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d370d-161">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d370d-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d370d-162">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="d370d-162">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d370d-163">TurnOnCompatibilityHTTPListener</span><span class="sxs-lookup"><span data-stu-id="d370d-163">TurnOnCompatibilityHTTPListener</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-turnoncompatibilityhttplistener)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d370d-164">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d370d-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d370d-165">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="d370d-165">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d370d-166">TurnOnCompatibilityHTTPSListener</span><span class="sxs-lookup"><span data-stu-id="d370d-166">TurnOnCompatibilityHTTPSListener</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-turnoncompatibilityhttpslistener)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d370d-167">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d370d-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d370d-168">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="d370d-168">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d370d-169">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d370d-169">Requirements</span></span>



| <span data-ttu-id="d370d-170">Requisito</span><span class="sxs-lookup"><span data-stu-id="d370d-170">Requirement</span></span> | <span data-ttu-id="d370d-171">Valore</span><span class="sxs-lookup"><span data-stu-id="d370d-171">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d370d-172">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d370d-172">Minimum supported client</span></span><br/> | <span data-ttu-id="d370d-173">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="d370d-173">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d370d-174">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d370d-174">Minimum supported server</span></span><br/> | <span data-ttu-id="d370d-175">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="d370d-175">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="d370d-176">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="d370d-176">Namespace</span></span><br/>                | <span data-ttu-id="d370d-177">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="d370d-177">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="d370d-178">MOF</span><span class="sxs-lookup"><span data-stu-id="d370d-178">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d370d-179"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d370d-179"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="d370d-180">DLL</span><span class="sxs-lookup"><span data-stu-id="d370d-180">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d370d-181"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d370d-181"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

