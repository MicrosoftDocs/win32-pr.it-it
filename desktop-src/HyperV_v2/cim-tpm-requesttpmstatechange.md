---
description: Richiede che lo stato del TPM sia modificato nel valore specificato nel parametro RequestedTPMState.
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
ms.openlocfilehash: 94af1d619ffa686b2fb4546987c6b825e4c658a5ae045d84fe5c6181716e95e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118646449"
---
# <a name="requesttpmstatechange-method-of-the-cim_tpm-class"></a>Metodo RequestTPMStateChange della classe TPM CIM \_

Richiede che lo stato del TPM sia modificato nel valore specificato nel *parametro RequestedTPMState.* Se la chiamata al metodo viene completata correttamente, la proprietà **TPMState** deve essere uguale al **parametro RequestedTPMState.** La chiamata del **metodo RequestTPMStateChange** più volte può comportare la sovrascrittura o la perdita di richieste precedenti.

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

*RequestedTPMState* \[ Pollici\]
</dt> <dd>

Stati del TPM richiesto.

<dt>

<span id="S1_Enabled-Active-Owned"></span><span id="s1_enabled-active-owned"></span><span id="S1_ENABLED-ACTIVE-OWNED"></span>

**S1 Enabled-Active-Owned** (2)


</dt> <dd></dd> <dt>

<span id="S2_Disabled-Active-Owned"></span><span id="s2_disabled-active-owned"></span><span id="S2_DISABLED-ACTIVE-OWNED"></span>

**S2 Disabled-Active-Owned** (3)


</dt> <dd></dd> <dt>

<span id="S3_Enabled-Inactive-Owned"></span><span id="s3_enabled-inactive-owned"></span><span id="S3_ENABLED-INACTIVE-OWNED"></span>

**S3 Enabled-Inactive-Owned** (4)


</dt> <dd></dd> <dt>

<span id="S4_Disabled-Inactive-Owned"></span><span id="s4_disabled-inactive-owned"></span><span id="S4_DISABLED-INACTIVE-OWNED"></span>

**S4 Disabled-Inactive-Owned** (5)


</dt> <dd></dd> <dt>

<span id="S5_Enabled-Active-Unowned"></span><span id="s5_enabled-active-unowned"></span><span id="S5_ENABLED-ACTIVE-UNOWNED"></span>

**S5 Enabled-Active-Unwned** (6)


</dt> <dd></dd> <dt>

<span id="S6_Disabled-Active-Unowned"></span><span id="s6_disabled-active-unowned"></span><span id="S6_DISABLED-ACTIVE-UNOWNED"></span>

**S6 Disabled-Active-Unwned** (7)


</dt> <dd></dd> <dt>

<span id="S7_Enabled-Inactive-Unowned"></span><span id="s7_enabled-inactive-unowned"></span><span id="S7_ENABLED-INACTIVE-UNOWNED"></span>

**S7 Enabled-Inactive-Unwned** (8)


</dt> <dd></dd> <dt>

<span id="S8_Disabled-Inactive-Unowned"></span><span id="s8_disabled-inactive-unowned"></span><span id="S8_DISABLED-INACTIVE-UNOWNED"></span>

**S8 Disabled-Inactive-Unwned** (9)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF riservato** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**Fornitore riservato** (32768..65535)


</dt> <dd></dd> </dl> </dd> <dt>

*AuthorizationToken* \[ Pollici\]
</dt> <dd>

Token di autorizzazione che potrebbe essere necessario per l'applicazione dell'azione. Il *parametro AuthorizationToken* può essere necessario per stabilire la presenza fisica o per passare OwnerAuth, la password di autorizzazione del proprietario definita da TCG. Nel caso di OwnerAuth, potrebbe essere necessario CIM SharedCredential con valore non Null di \_ CIM \_ SharedCredential.Secret. È anche possibile specificare la proprietà \_ CIM SharedCredential.Algorithm in base alla proprietà CIM \_ TPMCapabilities.SupportedPasswordAlgorithms.

</dd> <dt>

*Processo* \[ Cambio\]
</dt> <dd>

Può contenere un riferimento al [**processo \_ concreto CIM**](cim-concretejob.md) creato per tenere traccia della transizione di stato avviata dalla chiamata al metodo.

</dd> <dt>

*TimeoutPeriod* \[ Pollici\]
</dt> <dd>

Periodo di timeout che specifica la quantità massima di tempo prevista dal client per la transizione al nuovo stato. Il formato dell'intervallo deve essere usato per specificare *TimeoutPeriod*. Il valore 0 o un parametro Null indica che il client non ha requisiti di tempo per la transizione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

In caso di esito positivo, restituisce un valore 0 o 4096. In caso contrario, restituisce un errore.

<dl> <dt>

**Completato senza errori** (0)
</dt> <dt>

**Non supportato** (1)
</dt> <dt>

**Errore sconosciuto o non specificato** (2)
</dt> <dt>

**Impossibile completare entro il periodo di timeout** (3)
</dt> <dt>

**Operazione non** riuscita (4)
</dt> <dt>

**Parametro non valido** (5)
</dt> <dt>

**In uso** (6)
</dt> <dt>

**DMTF riservato** (..)
</dt> <dt>

**Parametri del metodo controllati - Processo avviato** (4096)
</dt> <dt>

**Transizione di stato non** valida (4097)
</dt> <dt>

**Uso del parametro di timeout non supportato** (4098)
</dt> <dt>

**Occupato** (4099)
</dt> <dt>

**Metodo riservato** (4100..32767)
</dt> <dt>

**Specifico del** fornitore (32768..65535)
</dt> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 10 solo app desktop\]<br/>                                                             |
| Server minimo supportato<br/> | Windows Server 2016<br/>                                                                          |
| Spazio dei nomi<br/>                | Virtualizzazione \\ radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CIM \_ TPM**](cim-tpm.md)
</dt> </dl>

 

 




