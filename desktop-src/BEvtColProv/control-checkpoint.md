---
description: Se la configurazione corrente è il risultato dell'operazione di annullamento/ripetizione/ripristino, lo contrassegna come se fosse stato impostato in modo esplicito, in modo che la cronologia manterrà l'ora in cui è stata impostata e verrà creato un file di backup alla successiva modifica della configurazione.
ms.assetid: 1b3d398a-c7f9-4e21-9e43-1245a13fe564
ms.tgt_platform: multiple
title: Metodo Checkpoint della classe Control (Srrestoreptapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.Checkpoint
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: 44453f647d55f29a9a6cfc5622e29dcc88ad2446
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104125844"
---
# <a name="checkpoint-method-of-the-control-class"></a>Metodo Checkpoint della classe Control

Se la configurazione corrente è il risultato dell'operazione di annullamento/ripetizione/ripristino, lo contrassegna come se fosse stato impostato in modo esplicito, in modo che la cronologia manterrà l'ora in cui è stata impostata e verrà creato un file di backup alla successiva modifica della configurazione. Se la configurazione corrente è già stata impostata in modo esplicito, non ha alcun effetto.

## <a name="syntax"></a>Sintassi


```mof
Uint32 Checkpoint(
  [in]  Uint32 OldTimestampLow,
  [in]  Uint32 OldTimestampHigh,
  [out] string ErrorString,
  [out] string WarningString,
  [out] string InfoString,
  [out] uint32 ErrorType
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*OldTimestampLow* \[ in\]
</dt> <dd>

Timestamp di quando è stata impostata la configurazione corrente. Se non è 0, Abilita il controllo di atomicità: l'azione verrà applicata solo se il timestamp della configurazione precedente corrisponde a (ovvero la configurazione non è stata modificata in un intervallo compreso tra). Questa è la parte bassa di [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).

</dd> <dt>

*OldTimestampHigh* \[ in\]
</dt> <dd>

Timestamp di quando è stata impostata la configurazione corrente. Se non è 0, Abilita il controllo di atomicità: l'azione verrà applicata solo se il timestamp della configurazione precedente corrisponde a (ovvero la configurazione non è stata modificata in un intervallo compreso tra). Si tratta della parte superiore di [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).

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

Il tipo di errore, Si noti che 0 o assente indica l'esito positivo.

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
| Intestazione<br/>                   | <dl> <dt>Srrestoreptapi. h</dt> </dl>          |
| MOF<br/>                      | <dl> <dt>BootEventCollectorWMI. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>BEvtCol.exe</dt> </dl>               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Control**](control.md)
</dt> </dl>

 

