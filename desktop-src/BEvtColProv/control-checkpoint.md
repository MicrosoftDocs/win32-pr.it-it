---
description: Se la configurazione corrente è il risultato di Undo/Redo/Restore, la contrassegna come se fosse stata impostata in modo esplicito, in modo che la cronologia conservi l'ora in cui è stata impostata e verrà creato un file di backup alla successiva modifica della configurazione.
ms.assetid: 1b3d398a-c7f9-4e21-9e43-1245a13fe564
ms.tgt_platform: multiple
title: Metodo Checkpoint della classe Control (Srrestoreptapi.h)
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
ms.openlocfilehash: ff71086703e409331e420fd064f73ff2406ec4e5167ea97da78b2afc498bf244
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119579851"
---
# <a name="checkpoint-method-of-the-control-class"></a>Metodo Checkpoint della classe Control

Se la configurazione corrente è il risultato di Undo/Redo/Restore, la contrassegna come se fosse stata impostata in modo esplicito, in modo che la cronologia conservi l'ora in cui è stata impostata e verrà creato un file di backup alla successiva modifica della configurazione. Se la configurazione corrente è già stata impostata in modo esplicito, non ha alcun effetto.

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

*OldTimestampLow* \[ Pollici\]
</dt> <dd>

Timestamp di quando è stata impostata la configurazione corrente. Se non è 0, abilita il controllo dell'atomicità: l'azione verrà applicata solo se il timestamp della configurazione precedente corrisponde (ad esempio, la configurazione non è stata modificata tra). Si tratta della parte bassa di [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).

</dd> <dt>

*OldTimestampHigh* \[ Pollici\]
</dt> <dd>

Timestamp di quando è stata impostata la configurazione corrente. Se non è 0, abilita il controllo dell'atomicità: l'azione verrà applicata solo se il timestamp della configurazione precedente corrisponde (ad esempio, la configurazione non è stata modificata tra). Questa è la parte più elevata di [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).

</dd> <dt>

*ErrorString* \[ Cambio\]
</dt> <dd>

Stringa di testo con la spiegazione dell'errore.

</dd> <dt>

*WarningString* \[ Cambio\]
</dt> <dd>

Stringa di testo con avvisi.

</dd> <dt>

*InfoString* \[ Cambio\]
</dt> <dd>

Stringa di testo con informazioni sulla configurazione.

</dd> <dt>

*ErrorType* \[ Cambio\]
</dt> <dd>

Il tipo di errore, Si noti che 0 o absent indica l'esito positivo.

<dt>

0
</dt> <dd>

Esito positivo.

</dd> <dt>

1
</dt> <dd>

formato dell'argomento non valido

</dd> <dt>

2
</dt> <dd>

valore dell'argomento non valido

</dd> <dt>

3
</dt> <dd>

Errore di apertura della risorsa (socket)

</dd> <dt>

4
</dt> <dd>

Errore di persistenza (scrittura file)

</dd> <dt>

5
</dt> <dd>

Errore di atomicità (il timestamp precedente non corrisponde)

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
| Intestazione<br/>                   | <dl> <dt>Srrestoreptapi.h</dt> </dl>          |
| MOF<br/>                      | <dl> <dt>BootEventCollectorWMI.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>BEvtCol.exe</dt> </dl>               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Control**](control.md)
</dt> </dl>

 

