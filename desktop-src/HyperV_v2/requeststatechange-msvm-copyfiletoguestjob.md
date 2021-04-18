---
description: Modifica lo stato del processo.
ms.assetid: 3B11CE45-63E4-43D1-AAF6-02F83C9CBB85
title: 'Metodo Msvm_CopyFileToGuestJob:: RequestStateChange'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CopyFileToGuestJob.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: adf5d866989f3b3518cf53b52e073239e023e3c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314321"
---
# <a name="msvm_copyfiletoguestjobrequeststatechange-method"></a>\_Metodo MSVM CopyFileToGuestJob:: RequestStateChange

Modifica lo stato del processo.

## <a name="syntax"></a>Sintassi


```C++
uint32 RequestStateChange(
  [in] uint16   RequestedState,
  [in] datetime TimeoutPeriod
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*RequestedState* \[ in\]
</dt> <dd>

Nuovo stato. Questi sono i valori possibili:

<dt>

<span id="Start"></span><span id="start"></span><span id="START"></span>

<span id="Start"></span><span id="start"></span><span id="START"></span>**Avvio** (2)


</dt> <dd>

Imposta lo stato su "Running".

</dd> <dt>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Sospendi** (3)


</dt> <dd>

Arresta temporaneamente il processo. Il client può quindi riavviare il processo con ' Start '. Il client può eventualmente immettere lo stato ' servizio ' mentre è sospeso (specifico del processo).

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

Inserisce il processo in uno stato del servizio specifico del fornitore. Il client può eventualmente riavviare il processo.

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

Questo metodo restituisce uno dei valori seguenti.



| Codice/valore restituito                                                                                                                                                               | Descrizione                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <dt>**Completato senza errori**</dt> <dt>0</dt> </dl>                   | Esito positivo.<br/>                                                                |
| <dl> <dt>**Uso del parametro timeout non supportato**</dt> <dt>4098</dt> </dl> |                                                                                    |
| <dl> <dt>**Errore**</dt> <dt>32768</dt> </dl>                                |                                                                                    |
| <dl> <dt>**Accesso negato**</dt> <dt>32769</dt> </dl>                         | Accesso negato.<br/>                                                          |
| <dl> <dt>**Non supportato**</dt> <dt>32770</dt> </dl>                         |                                                                                    |
| <dl> <dt>**Stato sconosciuto**</dt> <dt>32771</dt> </dl>                     |                                                                                    |
| <dl> <dt>**Timeout**</dt> <dt>32772</dt> </dl>                               |                                                                                    |
| <dl> <dt>**Parametro non valido**</dt> <dt>32773</dt> </dl>                     |                                                                                    |
| <dl> Il <dt>**sistema è in uso**</dt> <dt>32774</dt> </dl>                      |                                                                                    |
| <dl> <dt>**Stato non valido per l'operazione**</dt> <dt>32775</dt> </dl>      | Il valore specificato nel parametro *RequestedState* non è supportato.<br/> |
| <dl> <dt>**Tipo di dati non corretto**</dt> <dt>32776</dt> </dl>                   |                                                                                    |
| <dl> Il <dt>**sistema non è disponibile**</dt> <dt>32777</dt> </dl>               |                                                                                    |
| <dl> <dt>**Memoria insufficiente**</dt> <dt>32778</dt> </dl>                         |                                                                                    |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8.1 \[ solo app desktop\]<br/>                                                            |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2012 R2 \[\]<br/>                                                 |
| Spazio dei nomi<br/>                | \\\\\\Virtualizzazione radice \\ v2<br/>                                                                 |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_CopyFileToGuestJob MSVM**](msvm-copyfiletoguestjob.md)
</dt> </dl>

 

 




