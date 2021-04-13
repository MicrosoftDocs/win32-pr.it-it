---
description: Richiede che lo stato del processo venga modificato in un valore specificato nel parametro RequestedState. Richiamando il metodo RequestStateChange più volte, le richieste precedenti potrebbero essere sovrascritte o perse.
ms.assetid: 64a9d63e-8af4-4ab1-8343-9a0418b951e2
title: Metodo RequestStateChange della classe CIM_ConcreteJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ConcreteJob.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 6e3efcea0f7ed7d6ecbfef7b543a0e82d90a15b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344131"
---
# <a name="requeststatechange-method-of-the-cim_concretejob-class"></a>Metodo RequestStateChange della classe CIM \_ ConcreteJob

Richiede che lo stato del processo venga modificato in un valore specificato nel parametro RequestedState. Richiamando il metodo RequestStateChange più volte, le richieste precedenti potrebbero essere sovrascritte o perse.

Se viene restituito 0, l'attività è stata completata correttamente. Qualsiasi altro codice restituito indica una condizione di errore.

## <a name="syntax"></a>Sintassi


```mof
uint32 RequestStateChange(
  [in] uint16   RequestedState,
  [in] datetime TimeoutPeriod
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*RequestedState* \[ in\]
</dt> <dd>

Stato da richiedere per un processo. I valori possibili sono i seguenti:

<dt>

<span id="Start"></span><span id="start"></span><span id="START"></span>

<span id="Start"></span><span id="start"></span><span id="START"></span>**Avvio** (2)


</dt> <dd>

Imposta lo stato su "Running".

</dd> <dt>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Sospendi** (3)


</dt> <dd>

Arresta temporaneamente il processo. L'intenzione è di riavviare successivamente il processo con "Start". Potrebbe essere possibile immettere lo stato del servizio mentre è sospeso. (Si tratta di un processo specifico).

</dd> <dt>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Termina** (4)


</dt> <dd>

Arresta il processo in modo pulito, Salva i dati, conserva lo stato e arresta tutti i processi sottostanti in modo ordinato.

</dd> <dt>

<span id="Kill"></span><span id="kill"></span><span id="KILL"></span>

<span id="Kill"></span><span id="kill"></span><span id="KILL"></span>**Kill** (5)


</dt> <dd>

Termina immediatamente il processo senza alcuna necessità di salvare i dati o mantenere lo stato.

</dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Servizio** (6)


</dt> <dd>

Inserisce il processo in uno stato del servizio specifico del fornitore. Potrebbe essere possibile riavviare il processo.

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (7.. 32767)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fornitore riservato** (32768.. 65535)


</dt> <dd></dd> </dl> </dd> <dt>

*TimeoutPeriod* \[ in\]
</dt> <dd>

Periodo di timeout che specifica la quantità massima di tempo per cui il client prevede che la transizione al nuovo stato venga eseguita. Per specificare il periodo di timeout, è necessario utilizzare il formato intervallo. Il valore 0 o **null** indica che il client non dispone di requisiti temporali per la transizione. Se questa proprietà non contiene 0 o **null** e l'implementazione non supporta questo parametro, deve essere restituito un codice restituito 4098 (**utilizzo del parametro timeout non supportato**).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce 0 in caso di esito positivo; in caso contrario, restituisce un errore.

<dl> <dt>

**Completato senza errori** (0)
</dt> <dt>

**Non supportato** (1)
</dt> <dt>

**Errore sconosciuto/non specificato** (2)
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

**Parametri del metodo controllati-transizione avviata** (4096)
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
| Client minimo supportato<br/> | Windows 8.1<br/>                                                                                  |
| Server minimo supportato<br/> | Windows Server 2012 R2<br/>                                                                       |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_CONCRETEJOB CIM**](cim-concretejob.md)
</dt> </dl>

 

 




