---
title: comando Reserve
description: Il comando Reserve alloca spazio su disco contiguo per l'area di lavoro dell'istanza del dispositivo. I dispositivi digitali video riconoscono questo comando.
ms.assetid: ac4fc75e-82d0-4817-a5cf-a77996bc69e2
keywords:
- comando riserva Windows Multimedia
topic_type:
- apiref
api_name:
- reserve
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f71889af552b9040777394047a0facfc6c81366
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963783"
---
# <a name="reserve-command"></a>comando Reserve

Il comando Reserve alloca spazio su disco contiguo per l'area di lavoro dell'istanza del dispositivo. I dispositivi digitali video riconoscono questo comando.

Per inviare questo comando, chiamare la funzione [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con il set di parametri *lpszCommand* come indicato di seguito.

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

Identificatore di un dispositivo MCI. Questo identificatore o alias viene assegnato quando il dispositivo viene aperto.

</dd> <dt>

<span id="lpszReserve"></span><span id="lpszreserve"></span><span id="LPSZRESERVE"></span>*lpszReserve*
</dt> <dd>

Uno o più dei flag seguenti.



| Valore           | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| in *percorso*       | Specifica l'unità e il percorso della directory, ma non il nome, di un file temporaneo usato per conservare i dati registrati. Il nome di questo file è specificato dal dispositivo. Il file temporaneo viene eliminato quando il dispositivo viene chiuso. Se questo flag viene omesso, il dispositivo specifica il percorso dello spazio su disco.                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| *durata* dimensioni | Specifica la quantità approssimativa di spazio su disco da riservare nell'area di lavoro. Il valore *Duration* viene specificato nel formato di ora corrente. Il dispositivo basa la stima dello spazio su disco richiesto nei parametri seguenti: il tempo richiesto, il formato del file, l'algoritmo di compressione video e audio e i valori di qualità di compressione in vigore. Se [sevideo](setvideo.md) "record" è disattivato, lo spazio è riservato solo per l'audio. Se il [file](setaudio.md) "record" è disattivato, lo spazio è riservato solo per i video. Se entrambi sono "off" o se *Duration* è zero, nessuno spazio viene riservato e lo spazio riservato esistente viene deallocato. Se questo flag viene omesso, il dispositivo userà un valore predefinito definito dal dispositivo. |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Può essere "Wait", "notify", "test" o una combinazione di questi. Per ulteriori informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore.

## <a name="remarks"></a>Commenti

Se necessario, i comandi [record](record.md) o [Save](save.md) successivi usano lo spazio riservato da questo comando. Se l'area di lavoro contiene dati non salvati, i dati andranno perduti. Alcuni dispositivi non richiedono la riserva e lo ignorano. Se lo spazio su disco non è riservato prima della registrazione, il comando record esegue una riserva implicita con i flag predefiniti specifici del dispositivo. Utilizzare un comando di riserva esplicito se si desidera un migliore controllo del momento in cui si verifica l'allocazione dei dischi, il controllo della quantità di spazio allocato e il controllo della posizione di allocazione dello spazio su disco. L'applicazione può modificare la quantità e la posizione dello spazio su disco precedentemente riservato con i comandi di riserva successivi. Qualsiasi spazio su disco allocato e ancora inutilizzato non viene deallocato fino al salvataggio dei dati registrati o fino alla chiusura dell'istanza del dispositivo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/> |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[Stringhe di comando MCI](mci-command-strings.md)
</dt> <dt>

[record](record.md)
</dt> <dt>

[salvataggio](save.md)
</dt> <dt>

[SetAudio](setaudio.md)
</dt> <dt>

[video](setvideo.md)
</dt> </dl>

 

