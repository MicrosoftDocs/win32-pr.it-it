---
title: comando reserve
description: Il comando reserve alloca spazio su disco contiguo per l'area di lavoro dell'istanza del dispositivo. I dispositivi video digitali riconoscono questo comando.
ms.assetid: ac4fc75e-82d0-4817-a5cf-a77996bc69e2
keywords:
- Comando reserve Windows Multimedia
topic_type:
- apiref
api_name:
- reserve
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83f4573f5a630bbf1243b7126867c2d6c6beef61810210624fe87958e12b02ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119892921"
---
# <a name="reserve-command"></a>comando reserve

Il comando reserve alloca spazio su disco contiguo per l'area di lavoro dell'istanza del dispositivo. I dispositivi video digitali riconoscono questo comando.

Per inviare questo comando, chiamare la [**funzione mciSendString**](/previous-versions//dd757161(v=vs.85)) con il parametro *lpszCommand* impostato come indicato di seguito.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("reserve %s %s %s"), 
  lpszDeviceID, 
  lpszReserve, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificatore di un dispositivo MCI. Questo identificatore o alias viene assegnato all'apertura del dispositivo.

</dd> <dt>

<span id="lpszReserve"></span><span id="lpszreserve"></span><span id="LPSZRESERVE"></span>*lpszReserve*
</dt> <dd>

Uno o più dei flag seguenti.



| Valore           | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| in *path*       | Specifica l'unità e il percorso della directory (ma non il nome) di un file temporaneo utilizzato per contenere i dati registrati. Il nome di questo file viene specificato dal dispositivo. Il file temporaneo viene eliminato alla chiusura del dispositivo. Se questo flag viene omesso, il dispositivo specifica la posizione dello spazio su disco.                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| durata *delle dimensioni* | Specifica la quantità approssimativa di spazio su disco da riservare nell'area di lavoro. Il *valore* della durata viene specificato nel formato di ora corrente. Il dispositivo basa la stima dello spazio su disco richiesto sui parametri seguenti: l'ora richiesta, il formato di file, l'algoritmo di compressione audio e video e i valori di qualità della compressione in vigore. Se [setvideo](setvideo.md) "record" è "off", lo spazio è riservato solo per l'audio. Se [setaudio](setaudio.md) "record" è "off", lo spazio è riservato solo per i video. Se entrambi sono "disattivati" o se *duration* è zero, non viene riservato alcuno spazio e viene deallocato qualsiasi spazio riservato esistente. Se questo flag viene omesso, il dispositivo userà un valore predefinito definito dal dispositivo. |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Può essere "wait", "notify", "test" o una combinazione di questi elementi. Per altre informazioni su questi flag, vedere [Wait, Notify e Test Flags.](the-wait-notify-and-test-flags.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore in caso contrario.

## <a name="remarks"></a>Commenti

Se necessario, i comandi [successivi di registrazione](record.md) [o](save.md) salvataggio usano lo spazio riservato da questo comando. Se l'area di lavoro contiene dati non salvati, i dati vengono persi. Alcuni dispositivi non richiedono la prenotazione e la ignorano. Se lo spazio su disco non è riservato prima della registrazione, il comando di registrazione esegue una riserva implicita con flag predefiniti specifici del dispositivo. Usare un comando di riserva esplicito per controllare meglio quando si verifica il ritardo per l'allocazione del disco, controllare la quantità di spazio allocato e il punto in cui viene allocato lo spazio su disco. L'applicazione può modificare la quantità e la posizione dello spazio su disco precedentemente riservato con i comandi di riserva successivi. Lo spazio su disco allocato e ancora inutilizzato non viene deallocato fino a quando non vengono salvati i dati registrati o fino alla chiusura dell'istanza del dispositivo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/> |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Mci](mci.md)
</dt> <dt>

[Stringhe di comando MCI](mci-command-strings.md)
</dt> <dt>

[Registrazione](record.md)
</dt> <dt>

[salvataggio](save.md)
</dt> <dt>

[setaudio](setaudio.md)
</dt> <dt>

[setvideo](setvideo.md)
</dt> </dl>

 

