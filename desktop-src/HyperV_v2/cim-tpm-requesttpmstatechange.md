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
# <a name="requesttpmstatechange-method-of-the-cim_tpm-class"></a>Metodo RequestTPMStateChange della classe del \_ TPM CIM

Richiede che lo stato del TPM venga modificato in un valore specificato nel parametro *RequestedTPMState* . Se la chiamata al metodo viene completata correttamente, la proprietà **TPMState** deve essere uguale al parametro **RequestedTPMState** . Richiamando il metodo **RequestTPMStateChange** più volte, le richieste precedenti potrebbero essere sovrascritte o perse.

## <a name="syntax"></a>Sintassi


```mof
uint32 RequestTPMStateChange(
  [in]  uint16              RequestedTPMState,
  [in]  string              AuthorizationToken,
  [out] CIM_ConcreteJob REF Job,
  [in]  datetime            TimeoutPeriod
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*RequestedTPMState* \[ in\]
</dt> <dd>

Stati del TPM richiesti.

<dt>

<span id="S1_Enabled-Active-Owned"></span><span id="s1_enabled-active-owned"></span><span id="S1_ENABLED-ACTIVE-OWNED"></span>

**S1 abilitato-di proprietà di Active** (2)


</dt> <dd></dd> <dt>

<span id="S2_Disabled-Active-Owned"></span><span id="s2_disabled-active-owned"></span><span id="S2_DISABLED-ACTIVE-OWNED"></span>

**S2 disabilitato-di proprietà di Active** (3)


</dt> <dd></dd> <dt>

<span id="S3_Enabled-Inactive-Owned"></span><span id="s3_enabled-inactive-owned"></span><span id="S3_ENABLED-INACTIVE-OWNED"></span>

**S3 abilitato-inattivo-di proprietà** (4)


</dt> <dd></dd> <dt>

<span id="S4_Disabled-Inactive-Owned"></span><span id="s4_disabled-inactive-owned"></span><span id="S4_DISABLED-INACTIVE-OWNED"></span>

**S4 disabilitato-proprietà inattiva** (5)


</dt> <dd></dd> <dt>

<span id="S5_Enabled-Active-Unowned"></span><span id="s5_enabled-active-unowned"></span><span id="S5_ENABLED-ACTIVE-UNOWNED"></span>

**S5 abilitato-attivo-senza proprietario** (6)


</dt> <dd></dd> <dt>

<span id="S6_Disabled-Active-Unowned"></span><span id="s6_disabled-active-unowned"></span><span id="S6_DISABLED-ACTIVE-UNOWNED"></span>

**S6 disabilitato-attivo-senza proprietario** (7)


</dt> <dd></dd> <dt>

<span id="S7_Enabled-Inactive-Unowned"></span><span id="s7_enabled-inactive-unowned"></span><span id="S7_ENABLED-INACTIVE-UNOWNED"></span>

**S7 abilitato-inattivo-senza proprietario** (8)


</dt> <dd></dd> <dt>

<span id="S8_Disabled-Inactive-Unowned"></span><span id="s8_disabled-inactive-unowned"></span><span id="S8_DISABLED-INACTIVE-UNOWNED"></span>

**S8 disabilitato-inattivo-non di proprietà** (9)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF riservato** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**Fornitore riservato** (32768.. 65535)


</dt> <dd></dd> </dl> </dd> <dt>

*AuthorizationToken* \[ in\]
</dt> <dd>

Token di autorizzazione che può essere necessario per rendere effettiva l'azione. Il parametro *AuthorizationToken* può essere necessario per stabilire la presenza fisica o per passare il OwnerAuth, la password di autorizzazione del proprietario definito dal TCG. Nel caso di OwnerAuth, \_ potrebbe essere necessario il SHAREDCREDENTIAL CIM con valore non null di CIM \_ SharedCredential. Secret. La \_ Proprietà CIM SharedCredential. Algorithm può essere specificata anche in base alla proprietà CIM \_ TPMCapabilities. SupportedPasswordAlgorithms.

</dd> <dt>

*Processo* \[ di out\]
</dt> <dd>

Può contenere un riferimento al [**\_ ConcreteJob CIM**](cim-concretejob.md) creato per tenere traccia della transizione di stato iniziata dalla chiamata al metodo.

</dd> <dt>

*TimeoutPeriod* \[ in\]
</dt> <dd>

Periodo di timeout che specifica la quantità massima di tempo per cui il client prevede che la transizione al nuovo stato venga eseguita. Per specificare *TimeoutPeriod*, è necessario utilizzare il formato intervallo. Il valore 0 o un parametro null indica che il client non dispone di requisiti temporali per la transizione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

In caso di esito positivo, restituisce 0 o 4096; in caso contrario, restituisce un errore.

<dl> <dt>

**Completato senza errori** (0)
</dt> <dt>

**Non supportato** (1)
</dt> <dt>

**Errore sconosciuto o non specificato** (2)
</dt> <dt>

**Non può essere completato entro il periodo di timeout** (3)
</dt> <dt>

**Non riuscito** (4)
</dt> <dt>

**Parametro non valido** (5)
</dt> <dt>

**In uso** (6)
</dt> <dt>

**DMTF riservato** (..)
</dt> <dt>

**Parametri del metodo controllati-processo avviato** (4096)
</dt> <dt>

**Transizione di stato non valida** (4097)
</dt> <dt>

**Utilizzo del parametro timeout non supportato** (4098)
</dt> <dt>

**Occupato** (4099)
</dt> <dt>

**Metodo riservato** (4100.. 32767)
</dt> <dt>

**Specifico del fornitore** (32768.. 65535)
</dt> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows 10\]<br/>                                                             |
| Server minimo supportato<br/> | Windows Server 2016<br/>                                                                          |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_TPM CIM**](cim-tpm.md)
</dt> </dl>

 

 




