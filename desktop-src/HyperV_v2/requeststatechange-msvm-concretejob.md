---
description: Richiede che lo stato del processo sia stato modificato nello stato specificato.
ms.assetid: 5D7D7D20-4BB9-4375-BBBF-7AA64FEE6D13
title: Metodo RequestStateChange della classe Msvm_ConcreteJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ConcreteJob.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 579ad52bd83bd43dc3071f704914eb7b5f9cae4f0be89f018e56b9608b1c12be
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119501131"
---
# <a name="requeststatechange-method-of-the-msvm_concretejob-class"></a>Metodo RequestStateChange della classe Msvm \_ ConcreteJob

Richiede che lo stato del processo sia stato modificato nello stato specificato. La chiamata del **metodo RequestStateChange** più volte può comportare la sovrascrittura o la perdita di richieste precedenti. Se viene restituito 0, l'attività è stata completata correttamente. Qualsiasi altro codice restituito indica una condizione di errore.

## <a name="syntax"></a>Sintassi


```mof
uint32 RequestStateChange(
  [in] uint16   RequestedState,
  [in] datetime TimeoutPeriod
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*RequestedState* \[ Pollici\]
</dt> <dd>

Tipo: **uint16**

Nuovo stato di un processo.

<dt>

<span id="Start"></span><span id="start"></span><span id="START"></span>

<span id="Start"></span><span id="start"></span><span id="START"></span>**Inizio** (2)


</dt> <dd>

Modifica lo stato in "In esecuzione".

</dd> <dt>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Sospendi** (3)


</dt> <dd>

Arresta temporaneamente il processo. L'intenzione è riavviare successivamente il processo con "Start". Potrebbe essere possibile immettere lo stato "Servizio" durante la sospensione. Si tratta di un processo specifico.

</dd> <dt>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Termina** (4)


</dt> <dd>

Arresta il processo in modo pulito, salvando i dati, mantenendo lo stato e arrestando tutti i processi sottostanti in modo ordinato.

</dd> <dt>

<span id="Kill"></span><span id="kill"></span><span id="KILL"></span>

<span id="Kill"></span><span id="kill"></span><span id="KILL"></span>**Kill** (5)


</dt> <dd>

Termina immediatamente il processo senza alcun requisito per salvare i dati o mantenere lo stato.

</dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Servizio** (6)


</dt> <dd>

Inserisce il processo in uno stato del servizio specifico del fornitore. Potrebbe essere possibile riavviare il processo.

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DmTF riservato**


</dt> <dd>

Riservato.

</dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fornitore riservato**


</dt> <dd>

Riservato.

</dd> </dl> </dd> <dt>

*TimeoutPeriod* \[ Pollici\]
</dt> <dd>

Tipo: **datetime**

Periodo di timeout che specifica la quantità massima di tempo prevista dal client per la transizione al nuovo stato. Il formato dell'intervallo deve essere usato per specificare il periodo di timeout. Il valore 0 o **Null** indica che il client non ha requisiti di tempo per la transizione. Se questa proprietà non contiene 0 o **Null** e l'implementazione non supporta questo parametro, deve essere restituito un codice restituito 4098 (utilizzo del parametro di timeout non supportato).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **uint32**

Questo metodo restituisce uno dei valori seguenti.

<dl> <dt>

**Completato senza errori** (0)
</dt> <dt>

**Non supportato** (1)
</dt> <dt>

**Errore sconosciuto/non specificato** (2)
</dt> <dt>

**Impossibile completare entro il periodo di timeout** (3)
</dt> <dt>

**Operazione non** riuscita (4)
</dt> <dt>

**Parametro non** valido (5)
</dt> <dt>

**In uso** (6)
</dt> <dt>

**DMTF riservato** (7 4095)
</dt> <dt>

**Parametri del metodo controllati - Transizione avviata** (4096)
</dt> <dt>

**Transizione di stato non** valida (4097)
</dt> <dt>

**Uso del parametro di timeout non supportato** (4098)
</dt> <dt>

**Occupato** (4099)
</dt> <dt>

**Metodo riservato** (4100 32767)
</dt> <dt>

**Specifico del** fornitore (32768 65535)
</dt> </dl>

## <a name="remarks"></a>Commenti

L'accesso alla [**classe Msvm \_ ConcreteJob**](msvm-concretejob.md) potrebbe essere limitato dal filtro del controllo dell'account utente. Per altre informazioni, vedere [Controllo dell'account utente e WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                                              |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                                    |
| Spazio dei nomi<br/>                | Virtualizzazione \\ radice \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Processo \_ concreto msvm**](msvm-concretejob.md)
</dt> </dl>

 

