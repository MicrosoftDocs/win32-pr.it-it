---
description: Richiede una modifica dello stato.
ms.assetid: 2960bc44-f2af-49c6-9c33-5d9e1ad8056c
title: Metodo RequestStateChange della classe Msvm_StorageJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_StorageJob.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 1ce563fdae2e73ba2e6994afc3d70c8d4d6fe34a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883038"
---
# <a name="requeststatechange-method-of-the-msvm_storagejob-class"></a>Metodo RequestStateChange della classe MSVM \_ StorageJob

Richiede una modifica dello stato.

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

RequestStateChange modifica lo stato di un processo. I valori possibili sono i seguenti:

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

Questo metodo restituisce uno dei valori seguenti:

<dl> <dt>

  (0)
</dt> <dt>

 (32768)
</dt> <dt>

 (32769)
</dt> <dt>

 (32770)
</dt> <dt>

 (32771)
</dt> <dt>

 (32772)
</dt> <dt>

 (32773)
</dt> <dt>

 (32774)
</dt> <dt>

 (32775)
</dt> <dt>

 (32776)
</dt> <dt>

 (32777)
</dt> <dt>

 (32778)
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

[**\_StorageJob MSVM**](msvm-storagejob.md)
</dt> </dl>

 

 




