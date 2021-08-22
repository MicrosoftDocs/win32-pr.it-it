---
description: Impostare la nuova configurazione attiva dell'agente di raccolta.
ms.assetid: 1979e657-a8f3-4eab-991c-a884bde10724
ms.tgt_platform: multiple
title: Metodo SetConfiguration della classe Control
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.SetConfiguration
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: 41ff2c97eaa4b3e2080493c640b716ae4a822762b0f598c94e141a8cc4b4ac6b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119589071"
---
# <a name="setconfiguration-method-of-the-control-class"></a>Metodo SetConfiguration della classe Control

Impostare la nuova configurazione attiva dell'agente di raccolta.

## <a name="syntax"></a>Sintassi


```mof
Uint32 SetConfiguration(
  [in]  string Config,
  [in]  Uint32 OldTimestampLow,
  [in]  Uint32 OldTimestampHigh,
  [out] Uint32 NewTimestampLow,
  [out] Uint32 NewTimestampHigh,
  [out] string ErrorString,
  [out] string WarningString,
  [out] string InfoString,
  [out] uint32 ErrorType
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Configurazione* \[ Pollici\]
</dt> <dd>

Configurazione da attivare.

</dd> <dt>

*OldTimestampLow* \[ Pollici\]
</dt> <dd>

Bit di ordine basso di un timestamp che indica quando è stata impostata la configurazione attiva corrente. Il controllo dell'atomicità è abilitato se questa proprietà non è impostata su 0.

</dd> <dt>

*OldTimestampHigh* \[ Pollici\]
</dt> <dd>

Bit più elevati di un timestamp che indica quando è stata impostata la configurazione attiva corrente. Il controllo dell'atomicità è abilitato se questa proprietà non è impostata su 0.

</dd> <dt>

*NewTimestampLow* \[ Cambio\]
</dt> <dd>

Quando questo metodo viene restituito, questo parametro contiene i bit di ordine più basso di un timestamp che indica quando è stata impostata la nuova configurazione. Il controllo dell'atomicità è abilitato se questa proprietà non è impostata su 0.

</dd> <dt>

*NewTimestampHigh* \[ Cambio\]
</dt> <dd>

Quando questo metodo viene restituito, questo parametro contiene i bit più elevati del timestamp che indica quando è stata impostata la nuova configurazione. Il controllo dell'atomicità è abilitato se questa proprietà non è impostata su 0.

</dd> <dt>

*ErrorString* \[ Cambio\]
</dt> <dd>

Quando questo metodo viene restituito, se si è verificato un errore, questo parametro contiene la descrizione dell'errore.

</dd> <dt>

*WarningString* \[ Cambio\]
</dt> <dd>

Quando questo metodo viene restituito, questo parametro contiene tutti i messaggi di avviso per l'operazione.

</dd> <dt>

*InfoString* \[ Cambio\]
</dt> <dd>

Quando questo metodo viene restituito, questo parametro contiene informazioni per la nuova configurazione attiva.

</dd> <dt>

*ErrorType* \[ Cambio\]
</dt> <dd>

Quando questo metodo viene restituito, se si è verificato un errore, questo parametro indica il tipo di errore.

<dt>

0
</dt> <dd>

La nuova configurazione è mancante.

</dd> <dt>

1
</dt> <dd>

Il formato della nuova configurazione non è valido.

</dd> <dt>

2
</dt> <dd>

La nuova configurazione non è valida.

</dd> <dt>

3
</dt> <dd>

Si è verificato un errore causato da un socket aperto.

</dd> <dt>

4
</dt> <dd>

Si è verificato un errore di scrittura del file.

</dd> <dt>

5
</dt> <dd>

Si è verificato un errore di atomicità.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valore restituito

<dl> <dt>


</dt> <dd>

0

Errore

</dd> <dt>


</dt> <dd>

1

Operazione completata

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 10 solo app desktop\]<br/>                                                          |
| Server minimo supportato<br/> | Windows Server 2016<br/>                                                                       |
| Spazio dei nomi<br/>                | Root \\ Microsoft \\ Windows \\ BootEventCollector<br/>                                              |
| MOF<br/>                      | <dl> <dt>BootEventCollectorWMI.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>BEvtCol.exe</dt> </dl>               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Control**](control.md)
</dt> </dl>

 

 




