---
title: Classe MDM_Policy_Config01_RemoteManagement02
description: Criteri MDM \_ \_ Config01 RemoteManagement02 criteri di \_ gestione remota.
ms.assetid: 2eabbf72-00a4-4c61-9ae1-ff49067cb502
keywords:
- Classe MDM_Policy_Config01_RemoteManagement02
- Classe MDM_Policy_Config01_RemoteManagement02, descritta
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_RemoteManagement02
- MDM_Policy_Config01_RemoteManagement02.InstanceID
- MDM_Policy_Config01_RemoteManagement02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a76aa1a04735897d0b1c8f0e16572dd124b601c2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873766"
---
# <a name="mdm_policy_config01_remotemanagement02-class"></a><span data-ttu-id="638ba-105">\_ \_ Classe Config01 RemoteManagement02 di criteri \_ MDM</span><span class="sxs-lookup"><span data-stu-id="638ba-105">MDM\_Policy\_Config01\_RemoteManagement02 class</span></span>

<span data-ttu-id="638ba-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="638ba-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="638ba-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="638ba-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="638ba-108">Criteri MDM \_ \_ Config01 RemoteManagement02 criteri di \_ gestione remota.</span><span class="sxs-lookup"><span data-stu-id="638ba-108">The MDM\_Policy\_Config01\_RemoteManagement02 remote management policies.</span></span>

<span data-ttu-id="638ba-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="638ba-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="638ba-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="638ba-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_RemoteManagement02
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

## <a name="members"></a><span data-ttu-id="638ba-111">Members</span><span class="sxs-lookup"><span data-stu-id="638ba-111">Members</span></span>

<span data-ttu-id="638ba-112">La **classe \_ \_ Config01 \_ RemoteManagement02 dei criteri MDM** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="638ba-112">The **MDM\_Policy\_Config01\_RemoteManagement02** class has these types of members:</span></span>

-   [<span data-ttu-id="638ba-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="638ba-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="638ba-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="638ba-114">Properties</span></span>

<span data-ttu-id="638ba-115">La **classe \_ \_ \_ RemoteManagement02 dei criteri MDM Config01** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="638ba-115">The **MDM\_Policy\_Config01\_RemoteManagement02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="638ba-116">\_Client AllowBasicAuthentication</span><span class="sxs-lookup"><span data-stu-id="638ba-116">AllowBasicAuthentication\_Client</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-allowbasicauthentication-client)
</dt> <dd> <dl> <dt>

<span data-ttu-id="638ba-117">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="638ba-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="638ba-118">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="638ba-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="638ba-119">\_Servizio AllowBasicAuthentication</span><span class="sxs-lookup"><span data-stu-id="638ba-119">AllowBasicAuthentication\_Service</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-allowbasicauthentication-service)
</dt> <dd> <dl> <dt>

<span data-ttu-id="638ba-120">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="638ba-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="638ba-121">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="638ba-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="638ba-122">AllowCredSSPAuthenticationClient</span><span class="sxs-lookup"><span data-stu-id="638ba-122">AllowCredSSPAuthenticationClient</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-allowcredsspauthenticationclient)
</dt> <dd> <dl> <dt>

<span data-ttu-id="638ba-123">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="638ba-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="638ba-124">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="638ba-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="638ba-125">AllowCredSSPAuthenticationService</span><span class="sxs-lookup"><span data-stu-id="638ba-125">AllowCredSSPAuthenticationService</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-allowcredsspauthenticationservice)
</dt> <dd> <dl> <dt>

<span data-ttu-id="638ba-126">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="638ba-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="638ba-127">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="638ba-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="638ba-128">AllowRemoteServerManagement</span><span class="sxs-lookup"><span data-stu-id="638ba-128">AllowRemoteServerManagement</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-allowremoteservermanagement)
</dt> <dd> <dl> <dt>

<span data-ttu-id="638ba-129">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="638ba-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="638ba-130">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="638ba-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="638ba-131">\_Client AllowUnencryptedTraffic</span><span class="sxs-lookup"><span data-stu-id="638ba-131">AllowUnencryptedTraffic\_Client</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-allowunencryptedtraffic-client)
</dt> <dd> <dl> <dt>

<span data-ttu-id="638ba-132">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="638ba-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="638ba-133">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="638ba-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="638ba-134">\_Servizio AllowUnencryptedTraffic</span><span class="sxs-lookup"><span data-stu-id="638ba-134">AllowUnencryptedTraffic\_Service</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-allowunencryptedtraffic-service)
</dt> <dd> <dl> <dt>

<span data-ttu-id="638ba-135">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="638ba-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="638ba-136">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="638ba-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="638ba-137">DisallowDigestAuthentication</span><span class="sxs-lookup"><span data-stu-id="638ba-137">DisallowDigestAuthentication</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-disallowdigestauthentication)
</dt> <dd> <dl> <dt>

<span data-ttu-id="638ba-138">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="638ba-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="638ba-139">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="638ba-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="638ba-140">DisallowNegotiateAuthenticationClient</span><span class="sxs-lookup"><span data-stu-id="638ba-140">DisallowNegotiateAuthenticationClient</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-disallownegotiateauthenticationclient)
</dt> <dd> <dl> <dt>

<span data-ttu-id="638ba-141">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="638ba-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="638ba-142">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="638ba-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="638ba-143">DisallowNegotiateAuthenticationService</span><span class="sxs-lookup"><span data-stu-id="638ba-143">DisallowNegotiateAuthenticationService</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-disallownegotiateauthenticationservice)
</dt> <dd> <dl> <dt>

<span data-ttu-id="638ba-144">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="638ba-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="638ba-145">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="638ba-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="638ba-146">DisallowStoringOfRunAsCredentials</span><span class="sxs-lookup"><span data-stu-id="638ba-146">DisallowStoringOfRunAsCredentials</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-disallowstoringofrunascredentials)
</dt> <dd> <dl> <dt>

<span data-ttu-id="638ba-147">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="638ba-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="638ba-148">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="638ba-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="638ba-149">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="638ba-149">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="638ba-150">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="638ba-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="638ba-151">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="638ba-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="638ba-152">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="638ba-152">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="638ba-153">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="638ba-153">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="638ba-154">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="638ba-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="638ba-155">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="638ba-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="638ba-156">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="638ba-156">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="638ba-157">SpecifyChannelBindingTokenHardeningLevel</span><span class="sxs-lookup"><span data-stu-id="638ba-157">SpecifyChannelBindingTokenHardeningLevel</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-specifychannelbindingtokenhardeninglevel)
</dt> <dd> <dl> <dt>

<span data-ttu-id="638ba-158">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="638ba-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="638ba-159">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="638ba-159">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="638ba-160">TrustedHosts</span><span class="sxs-lookup"><span data-stu-id="638ba-160">TrustedHosts</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-trustedhosts)
</dt> <dd> <dl> <dt>

<span data-ttu-id="638ba-161">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="638ba-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="638ba-162">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="638ba-162">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="638ba-163">TurnOnCompatibilityHTTPListener</span><span class="sxs-lookup"><span data-stu-id="638ba-163">TurnOnCompatibilityHTTPListener</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-turnoncompatibilityhttplistener)
</dt> <dd> <dl> <dt>

<span data-ttu-id="638ba-164">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="638ba-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="638ba-165">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="638ba-165">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="638ba-166">TurnOnCompatibilityHTTPSListener</span><span class="sxs-lookup"><span data-stu-id="638ba-166">TurnOnCompatibilityHTTPSListener</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-turnoncompatibilityhttpslistener)
</dt> <dd> <dl> <dt>

<span data-ttu-id="638ba-167">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="638ba-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="638ba-168">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="638ba-168">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="638ba-169">Requisiti</span><span class="sxs-lookup"><span data-stu-id="638ba-169">Requirements</span></span>



| <span data-ttu-id="638ba-170">Requisito</span><span class="sxs-lookup"><span data-stu-id="638ba-170">Requirement</span></span> | <span data-ttu-id="638ba-171">Valore</span><span class="sxs-lookup"><span data-stu-id="638ba-171">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="638ba-172">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="638ba-172">Minimum supported client</span></span><br/> | <span data-ttu-id="638ba-173">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="638ba-173">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="638ba-174">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="638ba-174">Minimum supported server</span></span><br/> | <span data-ttu-id="638ba-175">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="638ba-175">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="638ba-176">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="638ba-176">Namespace</span></span><br/>                | <span data-ttu-id="638ba-177">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="638ba-177">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="638ba-178">MOF</span><span class="sxs-lookup"><span data-stu-id="638ba-178">MOF</span></span><br/>                      | <dl> <span data-ttu-id="638ba-179"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="638ba-179"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="638ba-180">DLL</span><span class="sxs-lookup"><span data-stu-id="638ba-180">DLL</span></span><br/>                      | <dl> <span data-ttu-id="638ba-181"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="638ba-181"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

