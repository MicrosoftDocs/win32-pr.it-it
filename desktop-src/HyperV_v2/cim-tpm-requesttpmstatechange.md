---
description: Richiede che lo stato del TPM venga modificato in un valore specificato nel parametro RequestedTPMState.
ms.assetid: 7ad8bf4e-6263-45d5-8f33-fb842bbf1f1a
title: Metodo RequestTPMStateChange della classe CIM_TPM
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_TPM.RequestTPMStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 39bded1a43dd547780c3924f3af9c37cfc79aa1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967158"
---
# <a name="requesttpmstatechange-method-of-the-cim_tpm-class"></a><span data-ttu-id="bb8c3-103">Metodo RequestTPMStateChange della classe del \_ TPM CIM</span><span class="sxs-lookup"><span data-stu-id="bb8c3-103">RequestTPMStateChange method of the CIM\_TPM class</span></span>

<span data-ttu-id="bb8c3-104">Richiede che lo stato del TPM venga modificato in un valore specificato nel parametro *RequestedTPMState* .</span><span class="sxs-lookup"><span data-stu-id="bb8c3-104">Requests that the state of the TPM be changed to the value specified in the *RequestedTPMState* parameter.</span></span> <span data-ttu-id="bb8c3-105">Se la chiamata al metodo viene completata correttamente, la proprietà **TPMState** deve essere uguale al parametro **RequestedTPMState** .</span><span class="sxs-lookup"><span data-stu-id="bb8c3-105">If the method invocation completes successfully, the **TPMState** property shall be equal to the **RequestedTPMState** parameter.</span></span> <span data-ttu-id="bb8c3-106">Richiamando il metodo **RequestTPMStateChange** più volte, le richieste precedenti potrebbero essere sovrascritte o perse.</span><span class="sxs-lookup"><span data-stu-id="bb8c3-106">Invoking the **RequestTPMStateChange** method multiple times could result in earlier requests being overwritten or lost.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb8c3-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bb8c3-107">Syntax</span></span>


```mof
uint32 RequestTPMStateChange(
  [in]  uint16              RequestedTPMState,
  [in]  string              AuthorizationToken,
  [out] CIM_ConcreteJob REF Job,
  [in]  datetime            TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="bb8c3-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="bb8c3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb8c3-109">*RequestedTPMState* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bb8c3-109">*RequestedTPMState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb8c3-110">Stati del TPM richiesti.</span><span class="sxs-lookup"><span data-stu-id="bb8c3-110">The requested TPM states.</span></span>

<dt>

<span id="S1_Enabled-Active-Owned"></span><span id="s1_enabled-active-owned"></span><span id="S1_ENABLED-ACTIVE-OWNED"></span>

<span data-ttu-id="bb8c3-111">**S1 abilitato-di proprietà di Active** (2)</span><span class="sxs-lookup"><span data-stu-id="bb8c3-111">**S1 Enabled-Active-Owned** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="S2_Disabled-Active-Owned"></span><span id="s2_disabled-active-owned"></span><span id="S2_DISABLED-ACTIVE-OWNED"></span>

<span data-ttu-id="bb8c3-112">**S2 disabilitato-di proprietà di Active** (3)</span><span class="sxs-lookup"><span data-stu-id="bb8c3-112">**S2 Disabled-Active-Owned** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="S3_Enabled-Inactive-Owned"></span><span id="s3_enabled-inactive-owned"></span><span id="S3_ENABLED-INACTIVE-OWNED"></span>

<span data-ttu-id="bb8c3-113">**S3 abilitato-inattivo-di proprietà** (4)</span><span class="sxs-lookup"><span data-stu-id="bb8c3-113">**S3 Enabled-Inactive-Owned** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="S4_Disabled-Inactive-Owned"></span><span id="s4_disabled-inactive-owned"></span><span id="S4_DISABLED-INACTIVE-OWNED"></span>

<span data-ttu-id="bb8c3-114">**S4 disabilitato-proprietà inattiva** (5)</span><span class="sxs-lookup"><span data-stu-id="bb8c3-114">**S4 Disabled-Inactive-Owned** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="S5_Enabled-Active-Unowned"></span><span id="s5_enabled-active-unowned"></span><span id="S5_ENABLED-ACTIVE-UNOWNED"></span>

<span data-ttu-id="bb8c3-115">**S5 abilitato-attivo-senza proprietario** (6)</span><span class="sxs-lookup"><span data-stu-id="bb8c3-115">**S5 Enabled-Active-Unowned** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="S6_Disabled-Active-Unowned"></span><span id="s6_disabled-active-unowned"></span><span id="S6_DISABLED-ACTIVE-UNOWNED"></span>

<span data-ttu-id="bb8c3-116">**S6 disabilitato-attivo-senza proprietario** (7)</span><span class="sxs-lookup"><span data-stu-id="bb8c3-116">**S6 Disabled-Active-Unowned** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="S7_Enabled-Inactive-Unowned"></span><span id="s7_enabled-inactive-unowned"></span><span id="S7_ENABLED-INACTIVE-UNOWNED"></span>

<span data-ttu-id="bb8c3-117">**S7 abilitato-inattivo-senza proprietario** (8)</span><span class="sxs-lookup"><span data-stu-id="bb8c3-117">**S7 Enabled-Inactive-Unowned** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="S8_Disabled-Inactive-Unowned"></span><span id="s8_disabled-inactive-unowned"></span><span id="S8_DISABLED-INACTIVE-UNOWNED"></span>

<span data-ttu-id="bb8c3-118">**S8 disabilitato-inattivo-non di proprietà** (9)</span><span class="sxs-lookup"><span data-stu-id="bb8c3-118">**S8 Disabled-Inactive-Unowned** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="bb8c3-119">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="bb8c3-119">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="bb8c3-120">**Fornitore riservato** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="bb8c3-120">**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="bb8c3-121">*AuthorizationToken* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bb8c3-121">*AuthorizationToken* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb8c3-122">Token di autorizzazione che può essere necessario per rendere effettiva l'azione.</span><span class="sxs-lookup"><span data-stu-id="bb8c3-122">Authorization token that may be required for the action to take effect.</span></span> <span data-ttu-id="bb8c3-123">Il parametro *AuthorizationToken* può essere necessario per stabilire la presenza fisica o per passare il OwnerAuth, la password di autorizzazione del proprietario definito dal TCG.</span><span class="sxs-lookup"><span data-stu-id="bb8c3-123">The *AuthorizationToken* parameter may be required to establish Physical Presence, or to pass the OwnerAuth, the TCG defined owner authorization password.</span></span> <span data-ttu-id="bb8c3-124">Nel caso di OwnerAuth, \_ potrebbe essere necessario il SHAREDCREDENTIAL CIM con valore non null di CIM \_ SharedCredential. Secret.</span><span class="sxs-lookup"><span data-stu-id="bb8c3-124">In the case of OwnerAuth, the CIM\_SharedCredential with non-null value of the CIM\_SharedCredential.Secret may be required.</span></span> <span data-ttu-id="bb8c3-125">La \_ Proprietà CIM SharedCredential. Algorithm può essere specificata anche in base alla proprietà CIM \_ TPMCapabilities. SupportedPasswordAlgorithms.</span><span class="sxs-lookup"><span data-stu-id="bb8c3-125">The CIM\_SharedCredential.Algorithm property may also be specified based on the property CIM\_TPMCapabilities.SupportedPasswordAlgorithms.</span></span>

</dd> <dt>

<span data-ttu-id="bb8c3-126">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="bb8c3-126">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bb8c3-127">Può contenere un riferimento al [**\_ ConcreteJob CIM**](cim-concretejob.md) creato per tenere traccia della transizione di stato iniziata dalla chiamata al metodo.</span><span class="sxs-lookup"><span data-stu-id="bb8c3-127">May contain a reference to the [**CIM\_ConcreteJob**](cim-concretejob.md) created to track the state transition initiated by the method invocation.</span></span>

</dd> <dt>

<span data-ttu-id="bb8c3-128">*TimeoutPeriod* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bb8c3-128">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb8c3-129">Periodo di timeout che specifica la quantità massima di tempo per cui il client prevede che la transizione al nuovo stato venga eseguita.</span><span class="sxs-lookup"><span data-stu-id="bb8c3-129">A timeout period that specifies the maximum amount of time that the client expects the transition to the new state to take.</span></span> <span data-ttu-id="bb8c3-130">Per specificare *TimeoutPeriod*, è necessario utilizzare il formato intervallo.</span><span class="sxs-lookup"><span data-stu-id="bb8c3-130">The interval format must be used to specify the *TimeoutPeriod*.</span></span> <span data-ttu-id="bb8c3-131">Il valore 0 o un parametro null indica che il client non dispone di requisiti temporali per la transizione.</span><span class="sxs-lookup"><span data-stu-id="bb8c3-131">A value of 0 or a null parameter indicates that the client has no time requirements for the transition.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb8c3-132">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bb8c3-132">Return value</span></span>

<span data-ttu-id="bb8c3-133">In caso di esito positivo, restituisce 0 o 4096; in caso contrario, restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="bb8c3-133">On success, returns a 0 or 4096; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="bb8c3-134">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="bb8c3-134">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="bb8c3-135">**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="bb8c3-135">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="bb8c3-136">**Errore sconosciuto o non specificato** (2)</span><span class="sxs-lookup"><span data-stu-id="bb8c3-136">**Unknown or Unspecified Error** (2)</span></span>
</dt> <dt>

<span data-ttu-id="bb8c3-137">**Non può essere completato entro il periodo di timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="bb8c3-137">**Cannot complete within Timeout Period** (3)</span></span>
</dt> <dt>

<span data-ttu-id="bb8c3-138">**Non riuscito** (4)</span><span class="sxs-lookup"><span data-stu-id="bb8c3-138">**Failed** (4)</span></span>
</dt> <dt>

<span data-ttu-id="bb8c3-139">**Parametro non valido** (5)</span><span class="sxs-lookup"><span data-stu-id="bb8c3-139">**Invalid Parameter** (5)</span></span>
</dt> <dt>

<span data-ttu-id="bb8c3-140">**In uso** (6)</span><span class="sxs-lookup"><span data-stu-id="bb8c3-140">**In Use** (6)</span></span>
</dt> <dt>

<span data-ttu-id="bb8c3-141">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="bb8c3-141">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="bb8c3-142">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="bb8c3-142">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="bb8c3-143">**Transizione di stato non valida** (4097)</span><span class="sxs-lookup"><span data-stu-id="bb8c3-143">**Invalid State Transition** (4097)</span></span>
</dt> <dt>

<span data-ttu-id="bb8c3-144">**Utilizzo del parametro timeout non supportato** (4098)</span><span class="sxs-lookup"><span data-stu-id="bb8c3-144">**Use of Timeout Parameter Not Supported** (4098)</span></span>
</dt> <dt>

<span data-ttu-id="bb8c3-145">**Occupato** (4099)</span><span class="sxs-lookup"><span data-stu-id="bb8c3-145">**Busy** (4099)</span></span>
</dt> <dt>

<span data-ttu-id="bb8c3-146">**Metodo riservato** (4100.. 32767)</span><span class="sxs-lookup"><span data-stu-id="bb8c3-146">**Method Reserved** (4100..32767)</span></span>
</dt> <dt>

<span data-ttu-id="bb8c3-147">**Specifico del fornitore** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="bb8c3-147">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="bb8c3-148">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bb8c3-148">Requirements</span></span>



| <span data-ttu-id="bb8c3-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="bb8c3-149">Requirement</span></span> | <span data-ttu-id="bb8c3-150">Valore</span><span class="sxs-lookup"><span data-stu-id="bb8c3-150">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb8c3-151">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bb8c3-151">Minimum supported client</span></span><br/> | <span data-ttu-id="bb8c3-152">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="bb8c3-152">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="bb8c3-153">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bb8c3-153">Minimum supported server</span></span><br/> | <span data-ttu-id="bb8c3-154">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="bb8c3-154">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="bb8c3-155">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="bb8c3-155">Namespace</span></span><br/>                | <span data-ttu-id="bb8c3-156">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="bb8c3-156">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="bb8c3-157">MOF</span><span class="sxs-lookup"><span data-stu-id="bb8c3-157">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bb8c3-158"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bb8c3-158"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="bb8c3-159">DLL</span><span class="sxs-lookup"><span data-stu-id="bb8c3-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bb8c3-160"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="bb8c3-160"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="bb8c3-161">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bb8c3-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb8c3-162">**\_TPM CIM**</span><span class="sxs-lookup"><span data-stu-id="bb8c3-162">**CIM\_TPM**</span></span>](cim-tpm.md)
</dt> </dl>

 

 




