---
description: Ripristinare la configurazione attiva dell'agente di raccolta da un file di backup.
ms.assetid: b59b04a5-d2b3-4299-8347-5026b982dc02
ms.tgt_platform: multiple
title: Metodo RestoreFile della classe Control
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.RestoreFile
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: 148b35199822c98ca03041561f402dc5acaadddf067b9eeecd80e9b32e325db2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119589111"
---
# <a name="restorefile-method-of-the-control-class"></a>Metodo RestoreFile della classe Control

Ripristinare la configurazione attiva dell'agente di raccolta da un file di backup.

## <a name="syntax"></a>Sintassi


```mof
Uint32 RestoreFile(
  [in]  string File,
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

*File* \[ Pollici\]
</dt> <dd>

Nome del file di backup da ripristinare, dall'elenco restituito da ListBackups().

</dd> <dt>

*OldTimestampLow* \[ Pollici\]
</dt> <dd>

Timestamp di quando è stata impostata la configurazione precedente. Se non è 0, abilita il controllo dell'atomicità: la nuova configurazione verrà applicata solo se il timestamp della configurazione precedente corrisponde (ad esempio, la configurazione non è stata modificata tra). Si tratta della parte bassa di [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).

</dd> <dt>

*OldTimestampHigh* \[ Pollici\]
</dt> <dd>

Timestamp di quando è stata impostata la configurazione precedente. Se non è 0, abilita il controllo dell'atomicità: la nuova configurazione verrà applicata solo se il timestamp della configurazione precedente corrisponde (ad esempio, la configurazione non è stata modificata tra). Questa è la parte più elevata di [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).

</dd> <dt>

*NewTimestampLow* \[ Cambio\]
</dt> <dd>

Timestamp di quando è stata impostata la nuova configurazione, se la chiamata ha esito positivo. Si tratta della parte bassa di [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).

</dd> <dt>

*NewTimestampHigh* \[ Cambio\]
</dt> <dd>

Timestamp di quando è stata impostata la nuova configurazione, se la chiamata ha esito positivo. Questa è la parte più elevata di [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).

</dd> <dt>

*OriginalTimestampLow* \[ Cambio\]
</dt> <dd>

Timestamp originale di quando la configurazione ripristinata è stata impostata per la prima volta. Si tratta della parte bassa di [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).

</dd> <dt>

*OriginalTimestampHigh* \[ Cambio\]
</dt> <dd>

Timestamp originale di quando la configurazione ripristinata è stata impostata per la prima volta. Questa è la parte più elevata di [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).

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

Tipo di errore: si noti che 0 o absent indica l'esito positivo.

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
| MOF<br/>                      | <dl> <dt>BootEventCollectorWMI.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>BEvtCol.exe</dt> </dl>               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Control**](control.md)
</dt> </dl>

 

