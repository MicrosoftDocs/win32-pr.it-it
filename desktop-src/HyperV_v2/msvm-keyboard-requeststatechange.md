---
description: Richiede che lo stato dell'elemento sia modificato.
ms.assetid: D1742588-D932-4FE1-8D2A-E410BEE371FF
title: Metodo RequestStateChange della Msvm_Keyboard classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Keyboard.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 457ed1e98714a2a20169fd1139b7f42475e5d893756591930b6a25147f756897
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119522241"
---
# <a name="requeststatechange-method-of-the-msvm_keyboard-class"></a>Metodo RequestStateChange della classe Msvm \_ Keyboard

Richiede che lo stato dell'elemento sia modificato.

## <a name="syntax"></a>Sintassi


```mof
uint32 RequestStateChange(
  [in]  uint16              RequestedState,
  [out] CIM_ConcreteJob REF Job,
  [in]  datetime            TimeoutPeriod
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*RequestedState* \[ Pollici\]
</dt> <dd>

Nuovo stato richiesto per l'elemento. Queste informazioni verranno inserite nella proprietà **RequestedState** dell'istanza se il codice restituito è 0 ('Completed with No Error'), 3 ('Timeout') o 4096 (0x1000) ('Job Started'). Per una spiegazione dettagliata dei valori *requestedState,* vedere la descrizione delle **proprietà EnabledState** **e RequestedState.**

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

**Abilitato** (2)


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**Disabilitato** (3)


</dt> <dd></dd> <dt>

<span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>

**Arresta** (4)


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

**Offline** (6)


</dt> <dd></dd> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>

**Test** (7)


</dt> <dd></dd> <dt>

<span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>

**Rinvia** (8)


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

**Inattiva** (9)


</dt> <dd></dd> <dt>

<span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>

**Riavvio** (10)


</dt> <dd></dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

**Reset** (11)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DmTF Reserved** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**Vendor Reserved** (32768..65535)


</dt> <dd></dd> </dl> </dd> <dt>

*Processo* \[ Cambio\]
</dt> <dd>

Riferimento al processo. Questo parametro può essere **Null se** l'attività è stata completata.

</dd> <dt>

*TimeoutPeriod* \[ Pollici\]
</dt> <dd>

Quantità massima di tempo prevista dal client per la transizione al nuovo stato. Il formato dell'intervallo deve essere usato per specificare questo periodo di timeout. Il valore 0 o **Null** indica che il client non ha requisiti di tempo per la transizione. Se questa proprietà non contiene 0 o **Null** e l'implementazione non supporta questo parametro, viene restituito un codice restituito 4098 ("Utilizzo del parametro di timeout non supportato").

</dd> </dl>

## <a name="return-value"></a>Valore restituito

<dl> <dt>

**Completata senza errori** (0)
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

**DmTF Reserved** (..)
</dt> <dt>

**Parametri del metodo verificati - Processo avviato** (4096)
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
| Client minimo supportato<br/> | \[Windows 8.1 solo app desktop\]<br/>                                                            |
| Server minimo supportato<br/> | Windows Server 2012 Solo \[ app desktop R2\]<br/>                                                 |
| Spazio dei nomi<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Tastiera \_ Msvm**](msvm-keyboard.md)
</dt> </dl>

 

 




