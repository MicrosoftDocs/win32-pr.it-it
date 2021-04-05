---
title: comando di monitoraggio
description: Il comando di monitoraggio specifica l'origine della presentazione. L'origine della presentazione predefinita è l'area di lavoro. Il passaggio all'origine della presentazione commuta tutti i flussi audio e video nell'origine. I dispositivi digitali video riconoscono questo comando.
ms.assetid: 5cacbe88-b94e-4101-badf-2bb4796b19cf
keywords:
- monitoraggio del comando di Windows Multimedia
topic_type:
- apiref
api_name:
- monitor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ccbe1d8919c232ab88d04081dad242944868893
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741426"
---
# <a name="monitor-command"></a>comando di monitoraggio

Il comando di monitoraggio specifica l'origine della presentazione. L'origine della presentazione predefinita è l'area di lavoro. Il passaggio all'origine della presentazione commuta tutti i flussi audio e video nell'origine. I dispositivi digitali video riconoscono questo comando.

Per inviare questo comando, chiamare la funzione [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con il set di parametri *lpszCommand* come indicato di seguito.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("monitor %s %s %s"), 
  lpszDeviceID, 
  lpszMonitor, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificatore di un dispositivo MCI. Questo identificatore o alias viene assegnato quando il dispositivo viene aperto.

</dd> <dt>

<span id="lpszMonitor"></span><span id="lpszmonitor"></span><span id="LPSZMONITOR"></span>*lpszMonitor*
</dt> <dd>

Uno o più dei flag seguenti.



| Valore           | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| file            | Specifica che l'area di lavoro è l'origine della presentazione. Si tratta dell'origine predefinita.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| input           | Specifica che l'input esterno è l'origine della presentazione. Se è in corso un comando [Play](play.md) , viene prima sospesa. Se [sevideo](setvideo.md) è "on", questo flag Visualizza una finestra nascosta predefinita. I dispositivi potrebbero limitare le operazioni che possono essere eseguite da altre istanze del dispositivo durante il monitoraggio dell'input.                                                                                                                                                                                                                                                                                                                                                                    |
| metodo *Metodo* | Se usato con il **monitoraggio** "input", questo flag seleziona il metodo di monitoraggio. Il *Metodo* può essere "pre", "post" o "Direct". Il monitoraggio diretto richiede che il dispositivo sia configurato per una qualità di visualizzazione ottimale durante il monitoraggio. Il metodo di monitoraggio diretto potrebbe non essere compatibile con la registrazione video in movimento. Pre-e post-monitoraggio consentono la registrazione video in movimento. Il pre-monitoraggio Mostra l'input esterno prima della compressione, mentre il post-monitoraggio Mostra l'input esterno dopo la compressione. In genere, diversi metodi di monitoraggio hanno implicazioni hardware diverse. Il metodo di monitoraggio predefinito è selezionato dal dispositivo.<br/> |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Può essere "Wait", "notify", "test" o una combinazione di questi. Per ulteriori informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore.

## <a name="remarks"></a>Commenti

L'origine della presentazione passa automaticamente all'area di lavoro dopo un comando [Play](play.md), [Step](step.md), [pause](pause.md), [cue](cue.md) "output" o [Seek](seek.md) . Il comando [record](record.md) non cambia automaticamente le origini di presentazione, che consente all'applicazione di non visualizzare video mentre è in corso la registrazione.

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

[segnale](cue.md)
</dt> <dt>

[pause](pause.md)
</dt> <dt>

[Play](play.md)
</dt> <dt>

[record](record.md)
</dt> <dt>

[cercare](seek.md)
</dt> <dt>

[passo](step.md)
</dt> </dl>

 

