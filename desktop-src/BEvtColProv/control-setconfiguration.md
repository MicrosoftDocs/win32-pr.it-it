---
description: Imposta la nuova configurazione attiva dell'agente di raccolta.
ms.assetid: 1979e657-a8f3-4eab-991c-a884bde10724
ms.tgt_platform: multiple
title: Metodo di configurazione della classe Control
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
ms.openlocfilehash: 4f482de9c4cd8f410371da51e605762a1f92e104
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103747783"
---
# <a name="setconfiguration-method-of-the-control-class"></a>Metodo di configurazione della classe Control

Imposta la nuova configurazione attiva dell'agente di raccolta.

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

*Configurazione* \[ di in\]
</dt> <dd>

Configurazione da attivare.

</dd> <dt>

*OldTimestampLow* \[ in\]
</dt> <dd>

Bit di ordine inferiore di un timestamp che indica quando è stata impostata la configurazione attiva corrente. Il controllo di atomicità è abilitato se questa proprietà non è impostata su 0.

</dd> <dt>

*OldTimestampHigh* \[ in\]
</dt> <dd>

Bit di ordine superiore di un timestamp che indica quando è stata impostata la configurazione attiva corrente. Il controllo di atomicità è abilitato se questa proprietà non è impostata su 0.

</dd> <dt>

*NewTimestampLow* \[ out\]
</dt> <dd>

Quando questo metodo restituisce un risultato, questo parametro contiene i bit di ordine inferiore di un timestamp che indica quando è stata impostata la nuova configurazione. Il controllo di atomicità è abilitato se questa proprietà non è impostata su 0.

</dd> <dt>

*NewTimestampHigh* \[ out\]
</dt> <dd>

Quando questo metodo viene restituito, questo parametro contiene i bit più significativi del timestamp che indica quando è stata impostata la nuova configurazione. Il controllo di atomicità è abilitato se questa proprietà non è impostata su 0.

</dd> <dt>

*ErrorString* \[ out\]
</dt> <dd>

Quando questo metodo restituisce, se si è verificato un errore, questo parametro contiene la descrizione dell'errore.

</dd> <dt>

*WarningString* \[ out\]
</dt> <dd>

Quando questo metodo termina, questo parametro contiene tutti i messaggi di avviso per l'operazione.

</dd> <dt>

*InfoString* \[ out\]
</dt> <dd>

Quando questo metodo restituisce un risultato, questo parametro contiene informazioni per la nuova configurazione attiva.

</dd> <dt>

*ErrorType* \[ out\]
</dt> <dd>

Quando questo metodo restituisce, se si è verificato un errore, questo parametro indica il tipo di errore.

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
| Client minimo supportato<br/> | \[Solo app desktop Windows 10\]<br/>                                                          |
| Server minimo supportato<br/> | Windows Server 2016<br/>                                                                       |
| Spazio dei nomi<br/>                | Radice \\ Microsoft \\ Windows \\ BootEventCollector<br/>                                              |
| MOF<br/>                      | <dl> <dt>BootEventCollectorWMI. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>BEvtCol.exe</dt> </dl>               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Control**](control.md)
</dt> </dl>

 

 




