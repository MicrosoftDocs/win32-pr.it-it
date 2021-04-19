---
description: Richiede che lo stato del processo venga modificato nello stato specificato.
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
ms.openlocfilehash: 0e7abf5f4bf78ac469e528ab72bb5786130e9cf8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314322"
---
# <a name="requeststatechange-method-of-the-msvm_concretejob-class"></a>Metodo RequestStateChange della classe MSVM \_ ConcreteJob

Richiede che lo stato del processo venga modificato nello stato specificato. Richiamando il metodo **RequestStateChange** più volte è possibile che le richieste precedenti vengano sovrascritte o perse. Se viene restituito 0, l'attività è stata completata correttamente. Qualsiasi altro codice restituito indica una condizione di errore.

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

Tipo: **UInt16**

Nuovo stato di un processo.

<dt>

<span id="Start"></span><span id="start"></span><span id="START"></span>

<span id="Start"></span><span id="start"></span><span id="START"></span>**Avvio** (2)


</dt> <dd>

Imposta lo stato su "Running".

</dd> <dt>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Sospendi** (3)


</dt> <dd>

Arresta temporaneamente il processo. Lo scopo è quello di riavviare successivamente il processo con "Start". Potrebbe essere possibile immettere lo stato "servizio" mentre è sospeso. (Si tratta di un processo specifico).

</dd> <dt>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Termina** (4)


</dt> <dd>

Arresta il processo in modo corretto, salvando i dati, mantenendo lo stato e chiudendo tutti i processi sottostanti in modo ordinato.

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

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato**


</dt> <dd>

Riservato.

</dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fornitore riservato**


</dt> <dd>

Riservato.

</dd> </dl> </dd> <dt>

*TimeoutPeriod* \[ in\]
</dt> <dd>

Tipo: **DateTime**

Periodo di timeout che specifica la quantità massima di tempo per cui il client prevede che la transizione al nuovo stato venga eseguita. Per specificare il periodo di timeout, è necessario utilizzare il formato intervallo. Il valore 0 o **null** indica che il client non dispone di requisiti temporali per la transizione. Se questa proprietà non contiene 0 o **null** e l'implementazione non supporta questo parametro, deve essere restituito un codice restituito 4098 (utilizzo del parametro timeout non supportato).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **UInt32**

Questo metodo restituisce uno dei valori seguenti.

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

**DMTF riservato** (7 4095)
</dt> <dt>

**Parametri del metodo controllati-transizione avviata** (4096)
</dt> <dt>

**Transizione di stato non valida** (4097)
</dt> <dt>

**Utilizzo del parametro timeout non supportato** (4098)
</dt> <dt>

**Occupato** (4099)
</dt> <dt>

**Metodo riservato** (4100 32767)
</dt> <dt>

**Specifico del fornitore** (32768 65535)
</dt> </dl>

## <a name="remarks"></a>Commenti

L'accesso alla [**classe \_ ConcreteJob di MSVM**](msvm-concretejob.md) potrebbe essere limitato dal filtraggio del controllo dell'account utente. Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                                              |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                                    |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_ConcreteJob MSVM**](msvm-concretejob.md)
</dt> </dl>

 

