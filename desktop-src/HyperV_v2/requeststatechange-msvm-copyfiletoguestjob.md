---
description: Modifica lo stato del processo.
ms.assetid: 3B11CE45-63E4-43D1-AAF6-02F83C9CBB85
title: Msvm_CopyFileToGuestJob::RequestStateChange
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
ms.openlocfilehash: 09fdc3a1ee7d0f8942e1e02c5d18f20c42f74db2e65ae065132f164b199ee861
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014339"
---
# <a name="msvm_copyfiletoguestjobrequeststatechange-method"></a>Metodo \_ Msvm CopyFileToGuestJob::RequestStateChange

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

*RequestedState* \[ Pollici\]
</dt> <dd>

Nuovo stato. Questi sono i valori possibili:

<dt>

<span id="Start"></span><span id="start"></span><span id="START"></span>

<span id="Start"></span><span id="start"></span><span id="START"></span>**Start** (2)


</dt> <dd>

Modifica lo stato in "In esecuzione".

</dd> <dt>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Suspend** (3)


</dt> <dd>

Arresta temporaneamente il processo. Il client può quindi riavviare il processo con 'Start'. Il client può entrare nello stato "Servizio" durante la sospensione (è specifico del processo).

</dd> <dt>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Terminate** (4)


</dt> <dd>

Arresta il processo in modo pulito, salvando i dati, mantenendo lo stato e arrestando tutti i processi sottostanti in modo ordinato.

</dd> <dt>

<span id="Kill"></span><span id="kill"></span><span id="KILL"></span>

<span id="Kill"></span><span id="kill"></span><span id="KILL"></span>**Kill** (5)


</dt> <dd>

Termina immediatamente il processo senza che sia necessario salvare i dati o mantenere lo stato.

</dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Servizio** (6)


</dt> <dd>

Inserisce il processo in uno stato del servizio specifico del fornitore. Il client può eventualmente riavviare il processo.

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DmTF Reserved** (7..32767)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768..65535)


</dt> <dd></dd> </dl> </dd> <dt>

*TimeoutPeriod* \[ Pollici\]
</dt> <dd>

Periodo di timeout che specifica la quantità massima di tempo prevista dal client per la transizione al nuovo stato. Il formato dell'intervallo deve essere usato per specificare il periodo di timeout. Il valore 0 o **Null** indica che il client non ha requisiti di tempo per la transizione. Se questa proprietà non contiene 0 o **Null** e l'implementazione non supporta questo parametro, deve essere restituito un codice restituito 4098 (Utilizzo del parametro di **timeout** non supportato).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce uno dei valori seguenti.



| Codice/valore restituito                                                                                                                                                               | Descrizione                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <dt>**Completata senza errori**</dt> <dt>0</dt> </dl>                   | Operazione completata.<br/>                                                                |
| <dl> <dt>**Uso del parametro di timeout non supportato**</dt> <dt>4098</dt> </dl> |                                                                                    |
| <dl> <dt>**Errore**</dt> <dt>32768</dt> </dl>                                |                                                                                    |
| <dl> <dt>**Accesso negato**</dt> <dt>32769</dt> </dl>                         | Accesso negato.<br/>                                                          |
| <dl> <dt>**Non supportato**</dt> <dt>32770</dt> </dl>                         |                                                                                    |
| <dl> <dt>**Lo stato è sconosciuto**</dt> <dt>32771</dt> </dl>                     |                                                                                    |
| <dl> <dt>**Timeout**</dt> <dt>32772</dt> </dl>                               |                                                                                    |
| <dl> <dt>**Parametro**</dt> <dt>32773 non valido</dt> </dl>                     |                                                                                    |
| <dl> <dt>**Il sistema è in uso**</dt> <dt>32774</dt> </dl>                      |                                                                                    |
| <dl> <dt>**Stato non valido per questa operazione**</dt> <dt>32775</dt> </dl>      | Il valore specificato nel *parametro RequestedState* non è supportato.<br/> |
| <dl> <dt>**Tipo di dati**</dt> <dt>32776 non corretto</dt> </dl>                   |                                                                                    |
| <dl> <dt>**Il sistema non è disponibile**</dt> <dt>32777</dt> </dl>               |                                                                                    |
| <dl> <dt>**Memoria insufficiente**</dt> <dt>32778</dt> </dl>                         |                                                                                    |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8.1 solo app desktop\]<br/>                                                            |
| Server minimo supportato<br/> | Windows Server 2012 Solo \[ app desktop R2\]<br/>                                                 |
| Spazio dei nomi<br/>                | \\\\Root \\ Virtualization \\ V2<br/>                                                                 |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Msvm \_ CopyFileToGuestJob**](msvm-copyfiletoguestjob.md)
</dt> </dl>

 

 




