---
title: Classe MDM_HealthAttestation
description: La \_ classe MDM HealthAttestation consente ai responsabili IT aziendali di valutare l'integrità dei dispositivi gestiti e di intraprendere le azioni dei criteri aziendali.
ms.assetid: 64f40ccc-98f6-48d6-bcd4-793375e3dbfb
keywords:
- Classe MDM_HealthAttestation
- Classe MDM_HealthAttestation, descritta
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7f76af135e7eac09b3b104e924b26efbb359b256
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476042"
---
# <a name="mdm_healthattestation-class"></a><span data-ttu-id="33ad7-105">MDM \_ HealthAttestation (classe)</span><span class="sxs-lookup"><span data-stu-id="33ad7-105">MDM\_HealthAttestation class</span></span>

<span data-ttu-id="33ad7-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="33ad7-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="33ad7-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="33ad7-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="33ad7-108">La classe **MDM \_ HealthAttestation** consente ai responsabili IT aziendali di valutare l'integrità dei dispositivi gestiti e di intraprendere le azioni dei criteri aziendali.</span><span class="sxs-lookup"><span data-stu-id="33ad7-108">The **MDM\_HealthAttestation** class enables enterprise IT managers to assess the health of managed devices and take enterprise policy actions.</span></span>

<span data-ttu-id="33ad7-109">Di seguito è riportato un elenco di funzioni eseguite dal CSP HealthAttestation:</span><span class="sxs-lookup"><span data-stu-id="33ad7-109">The following is a list of functions performed by the HealthAttestation CSP:</span></span>

-   <span data-ttu-id="33ad7-110">Raccoglie i dati utilizzati per la verifica di uno stato di integrità dei dispositivi</span><span class="sxs-lookup"><span data-stu-id="33ad7-110">Collects data that is used in verifying a devices health states</span></span>
-   <span data-ttu-id="33ad7-111">Inoltro dei dati al servizio di attestazione dell'integrità</span><span class="sxs-lookup"><span data-stu-id="33ad7-111">Forwards the data to the Health Attestation Service (HAS)</span></span>
-   <span data-ttu-id="33ad7-112">Effettua il provisioning del certificato di attestazione dell'integrità ricevuto da</span><span class="sxs-lookup"><span data-stu-id="33ad7-112">Provisions the Health Attestation Certificate that it receives from HAS</span></span>
-   <span data-ttu-id="33ad7-113">In seguito alla richiesta, il certificato di attestazione dell'integrità (ricevuto da ha) e le informazioni di runtime correlate al server MDM per la verifica</span><span class="sxs-lookup"><span data-stu-id="33ad7-113">Upon request, forwards the Health Attestation Certificate (received from HAS) and related runtime information to the MDM Server for verification</span></span>

<span data-ttu-id="33ad7-114">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="33ad7-114">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="33ad7-115">Sintassi</span><span class="sxs-lookup"><span data-stu-id="33ad7-115">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_HealthAttestation
{
  string  InstanceID;
  string  ParentID;
  sint32  Status;
  boolean ForceRetrieve;
  string  Certificate;
  string  Nonce;
  string  CorrelationID;
  sint32  TpmReadyStatus;
  sint32  MaxSupportedProtocolVersion;
  sint32  PreferredMaxProtocolVersion;
  sint32  CurrentProtocolVersion;
  string  HASEndpoint;
};
```

## <a name="members"></a><span data-ttu-id="33ad7-116">Members</span><span class="sxs-lookup"><span data-stu-id="33ad7-116">Members</span></span>

<span data-ttu-id="33ad7-117">La classe **MDM \_ HealthAttestation** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="33ad7-117">The **MDM\_HealthAttestation** class has these types of members:</span></span>

-   [<span data-ttu-id="33ad7-118">Metodi</span><span class="sxs-lookup"><span data-stu-id="33ad7-118">Methods</span></span>](#methods)
-   [<span data-ttu-id="33ad7-119">Proprietà</span><span class="sxs-lookup"><span data-stu-id="33ad7-119">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="33ad7-120">Metodi</span><span class="sxs-lookup"><span data-stu-id="33ad7-120">Methods</span></span>

<span data-ttu-id="33ad7-121">La classe **MDM \_ HealthAttestation** ha questi metodi.</span><span class="sxs-lookup"><span data-stu-id="33ad7-121">The **MDM\_HealthAttestation** class has these methods.</span></span>



| <span data-ttu-id="33ad7-122">Metodo</span><span class="sxs-lookup"><span data-stu-id="33ad7-122">Method</span></span>                                                                 | <span data-ttu-id="33ad7-123">Descrizione</span><span class="sxs-lookup"><span data-stu-id="33ad7-123">Description</span></span>                                                                                  |
|:-----------------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="33ad7-124">**VerifyHealthMethod**</span><span class="sxs-lookup"><span data-stu-id="33ad7-124">**VerifyHealthMethod**</span></span>](mdm-healthattestation-verifyhealthmethod.md) | <span data-ttu-id="33ad7-125">Metodo per notificare al dispositivo di preparare una richiesta di verifica del certificato di integrità.</span><span class="sxs-lookup"><span data-stu-id="33ad7-125">Method to notify the device to prepare a health certificate verification request.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="33ad7-126">Proprietà</span><span class="sxs-lookup"><span data-stu-id="33ad7-126">Properties</span></span>

<span data-ttu-id="33ad7-127">La classe **MDM \_ HealthAttestation** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="33ad7-127">The **MDM\_HealthAttestation** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="33ad7-128">Certificate</span><span class="sxs-lookup"><span data-stu-id="33ad7-128">Certificate</span></span>](/windows/client-management/mdm/healthattestation-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33ad7-129">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="33ad7-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33ad7-130">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="33ad7-130">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="33ad7-131">Qualificatori: **OctetString**</span><span class="sxs-lookup"><span data-stu-id="33ad7-131">Qualifiers: **Octetstring**</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33ad7-132">CorrelationID</span><span class="sxs-lookup"><span data-stu-id="33ad7-132">CorrelationID</span></span>](/windows/client-management/mdm/healthattestation-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33ad7-133">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="33ad7-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33ad7-134">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="33ad7-134">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="33ad7-135">**CurrentProtocolVersion**</span><span class="sxs-lookup"><span data-stu-id="33ad7-135">**CurrentProtocolVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33ad7-136">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="33ad7-136">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="33ad7-137">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="33ad7-137">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="33ad7-138">TBD</span><span class="sxs-lookup"><span data-stu-id="33ad7-138">TBD</span></span>

</dd> <dt>

[<span data-ttu-id="33ad7-139">ForceRetrieve</span><span class="sxs-lookup"><span data-stu-id="33ad7-139">ForceRetrieve</span></span>](/windows/client-management/mdm/healthattestation-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33ad7-140">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="33ad7-140">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="33ad7-141">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="33ad7-141">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33ad7-142">HASEndpoint</span><span class="sxs-lookup"><span data-stu-id="33ad7-142">HASEndpoint</span></span>](/windows/client-management/mdm/healthattestation-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33ad7-143">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="33ad7-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33ad7-144">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="33ad7-144">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="33ad7-145">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="33ad7-145">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33ad7-146">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="33ad7-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33ad7-147">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="33ad7-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="33ad7-148">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="33ad7-148">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="33ad7-149">Identifica il nome del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="33ad7-149">Identifies the name of the parent node.</span></span> <span data-ttu-id="33ad7-150">Per questa classe la stringa è "HealthAttestation".</span><span class="sxs-lookup"><span data-stu-id="33ad7-150">For this class, the string is "HealthAttestation".</span></span>

</dd> <dt>

<span data-ttu-id="33ad7-151">**MaxSupportedProtocolVersion**</span><span class="sxs-lookup"><span data-stu-id="33ad7-151">**MaxSupportedProtocolVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33ad7-152">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="33ad7-152">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="33ad7-153">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="33ad7-153">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="33ad7-154">TBD</span><span class="sxs-lookup"><span data-stu-id="33ad7-154">TBD</span></span>

</dd> <dt>

[<span data-ttu-id="33ad7-155">Nonce</span><span class="sxs-lookup"><span data-stu-id="33ad7-155">Nonce</span></span>](/windows/client-management/mdm/healthattestation-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33ad7-156">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="33ad7-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33ad7-157">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="33ad7-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="33ad7-158">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="33ad7-158">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33ad7-159">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="33ad7-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33ad7-160">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="33ad7-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="33ad7-161">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="33ad7-161">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="33ad7-162">Descrive il percorso completo del nodo padre.</span><span class="sxs-lookup"><span data-stu-id="33ad7-162">Describes the full path to the parent node.</span></span> <span data-ttu-id="33ad7-163">Per questa classe la stringa è "./Vendor/MSFT/"</span><span class="sxs-lookup"><span data-stu-id="33ad7-163">For this class, the string is "./Vendor/MSFT/"</span></span>

</dd> <dt>

<span data-ttu-id="33ad7-164">**PreferredMaxProtocolVersion**</span><span class="sxs-lookup"><span data-stu-id="33ad7-164">**PreferredMaxProtocolVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33ad7-165">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="33ad7-165">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="33ad7-166">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="33ad7-166">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="33ad7-167">TBD</span><span class="sxs-lookup"><span data-stu-id="33ad7-167">TBD</span></span>

</dd> <dt>

[<span data-ttu-id="33ad7-168">Status</span><span class="sxs-lookup"><span data-stu-id="33ad7-168">Status</span></span>](/windows/client-management/mdm/healthattestation-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33ad7-169">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="33ad7-169">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="33ad7-170">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="33ad7-170">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33ad7-171">TpmReadyStatus</span><span class="sxs-lookup"><span data-stu-id="33ad7-171">TpmReadyStatus</span></span>](/windows/client-management/mdm/healthattestation-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33ad7-172">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="33ad7-172">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="33ad7-173">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="33ad7-173">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="33ad7-174">Requisiti</span><span class="sxs-lookup"><span data-stu-id="33ad7-174">Requirements</span></span>



| <span data-ttu-id="33ad7-175">Requisito</span><span class="sxs-lookup"><span data-stu-id="33ad7-175">Requirement</span></span> | <span data-ttu-id="33ad7-176">Valore</span><span class="sxs-lookup"><span data-stu-id="33ad7-176">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33ad7-177">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="33ad7-177">Minimum supported client</span></span><br/> | <span data-ttu-id="33ad7-178">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="33ad7-178">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="33ad7-179">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="33ad7-179">Minimum supported server</span></span><br/> | <span data-ttu-id="33ad7-180">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="33ad7-180">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="33ad7-181">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="33ad7-181">Namespace</span></span><br/>                | <span data-ttu-id="33ad7-182">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="33ad7-182">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="33ad7-183">MOF</span><span class="sxs-lookup"><span data-stu-id="33ad7-183">MOF</span></span><br/>                      | <dl> <span data-ttu-id="33ad7-184"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="33ad7-184"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="33ad7-185">DLL</span><span class="sxs-lookup"><span data-stu-id="33ad7-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="33ad7-186"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="33ad7-186"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33ad7-187">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="33ad7-187">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33ad7-188">Utilizzo di script di PowerShell con il provider del Bridge WMI</span><span class="sxs-lookup"><span data-stu-id="33ad7-188">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

