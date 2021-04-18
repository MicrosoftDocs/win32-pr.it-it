---
description: Ripristinare la configurazione attiva dell'agente di raccolta da un file di backup, selezionato da un timestamp.
ms.assetid: 3ee4156b-c68f-4c44-b9be-dd86e8f4b340
ms.tgt_platform: multiple
title: Metodo RestoreFromTime della classe Control
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.RestoreFromTime
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: 79b89c0c89e4954d8a641d037e08757f83cad618
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305303"
---
# <a name="restorefromtime-method-of-the-control-class"></a>Metodo RestoreFromTime della classe Control

Ripristinare la configurazione attiva dell'agente di raccolta da un file di backup, selezionato da un timestamp.

## <a name="syntax"></a>Sintassi


```mof
Uint32 RestoreFromTime(
  [in]  Uint32 TargetTimestampLow,
  [in]  Uint32 TargetTimestampHigh,
  [in]  Uint32 OldTimestampLow,
  [in]  Uint32 OldTimestampHigh,
  [out] Uint32 NewTimestampLow,
  [out] Uint32 NewTimestampHigh,
  [out] Uint32 OriginalTimestampLow,
  [out] Uint32 OriginalTimestampHigh,
  [out] string ErrorString,
  [out] string WarningString,
  [out] string InfoString,
  [out] uint32 ErrorType
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*TargetTimestampLow* \[ in\]
</dt> <dd>

Ripristinare il file di backup in questo timestamp. Questa è la parte bassa di [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).

</dd> <dt>

*TargetTimestampHigh* \[ in\]
</dt> <dd>

Ripristinare il file di backup in questo timestamp. Si tratta della parte superiore di [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).

</dd> <dt>

*OldTimestampLow* \[ in\]
</dt> <dd>

Timestamp del momento in cui è stata impostata la configurazione precedente. Se non è 0, Abilita il controllo di atomicità: la nuova configurazione verrà applicata solo se il timestamp della configurazione precedente corrisponde a (ovvero la configurazione non è stata modificata in un intervallo compreso tra). Questa è la parte bassa di [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).

</dd> <dt>

*OldTimestampHigh* \[ in\]
</dt> <dd>

Timestamp del momento in cui è stata impostata la configurazione precedente. Se non è 0, Abilita il controllo di atomicità: la nuova configurazione verrà applicata solo se il timestamp della configurazione precedente corrisponde a (ovvero la configurazione non è stata modificata in un intervallo compreso tra). Si tratta della parte superiore di [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).

</dd> <dt>

*NewTimestampLow* \[ out\]
</dt> <dd>

Timestamp di quando è stata impostata la nuova configurazione, se la chiamata ha esito positivo. Questa è la parte bassa di [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).

</dd> <dt>

*NewTimestampHigh* \[ out\]
</dt> <dd>

Timestamp di quando è stata impostata la nuova configurazione, se la chiamata ha esito positivo. Si tratta della parte superiore di [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).

</dd> <dt>

*OriginalTimestampLow* \[ out\]
</dt> <dd>

Timestamp originale del momento in cui la configurazione ripristinata è stata impostata per la prima volta. Questa è la parte bassa di [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).

</dd> <dt>

*OriginalTimestampHigh* \[ out\]
</dt> <dd>

Timestamp originale del momento in cui la configurazione ripristinata è stata impostata per la prima volta. Si tratta della parte superiore di [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).

</dd> <dt>

*ErrorString* \[ out\]
</dt> <dd>

Stringa di testo con la spiegazione dell'errore.

</dd> <dt>

*WarningString* \[ out\]
</dt> <dd>

Stringa di testo con avvisi.

</dd> <dt>

*InfoString* \[ out\]
</dt> <dd>

Stringa di testo con le informazioni sulla configurazione.

</dd> <dt>

*ErrorType* \[ out\]
</dt> <dd>

Tipo di errore: si noti che 0 o assente indica l'esito positivo.

<dt>

0
</dt> <dd>

Esito positivo.

</dd> <dt>

1
</dt> <dd>

formato di argomento non valido

</dd> <dt>

2
</dt> <dd>

valore argomento non valido

</dd> <dt>

3
</dt> <dd>

errore di apertura della risorsa (socket)

</dd> <dt>

4
</dt> <dd>

errore di persistenza (scrittura file)

</dd> <dt>

5
</dt> <dd>

errore di atomicità (il timestamp precedente non corrisponde)

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

 

