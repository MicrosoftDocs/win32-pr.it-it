---
title: comando monitor
description: Il comando monitor specifica l'origine della presentazione. L'origine di presentazione predefinita è l'area di lavoro. Il passaggio all'origine della presentazione cambia tutti i flussi audio e video nell'origine. I dispositivi video digitali riconoscono questo comando.
ms.assetid: 5cacbe88-b94e-4101-badf-2bb4796b19cf
keywords:
- Comando monitor Windows Multimedia
topic_type:
- apiref
api_name:
- monitor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bef9a47db68856196dc84aefb3c5f110941189dec80f62b369eae13c60932d71
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120038811"
---
# <a name="monitor-command"></a>comando monitor

Il comando monitor specifica l'origine della presentazione. L'origine di presentazione predefinita è l'area di lavoro. Il passaggio all'origine della presentazione cambia tutti i flussi audio e video nell'origine. I dispositivi video digitali riconoscono questo comando.

Per inviare questo comando, chiamare la [**funzione mciSendString**](/previous-versions//dd757161(v=vs.85)) con il parametro *lpszCommand* impostato come segue.

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

Identificatore di un dispositivo MCI. Questo identificatore o alias viene assegnato all'apertura del dispositivo.

</dd> <dt>

<span id="lpszMonitor"></span><span id="lpszmonitor"></span><span id="LPSZMONITOR"></span>*lpszMonitor*
</dt> <dd>

Uno o più dei flag seguenti.



| Valore           | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| file            | Specifica che l'area di lavoro è l'origine della presentazione. Si tratta dell'origine predefinita.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| input           | Specifica che l'input esterno è l'origine della presentazione. Se è [in](play.md) corso un comando di riproduzione, questo viene prima sospeso. Se [setvideo](setvideo.md) è "on", questo flag visualizza una finestra nascosta predefinita. I dispositivi potrebbero limitare le attività che altre istanze del dispositivo possono eseguire durante il monitoraggio dell'input.                                                                                                                                                                                                                                                                                                                                                                    |
| metodo *method* | Se usato con **il monitoraggio** "input", questo flag seleziona il metodo di monitoraggio. Il *metodo* è "pre", "post" o "direct". Il monitoraggio diretto richiede che il dispositivo sia configurato per una qualità di visualizzazione ottimale durante il monitoraggio. Il metodo di monitoraggio diretto potrebbe non essere compatibile con la registrazione video in movimento. Le funzionalità di pre-monitoraggio e post-monitoraggio consentono la registrazione di video in movimento. Il pre-monitoraggio mostra l'input esterno prima della compressione, mentre il post-monitoraggio mostra l'input esterno dopo la compressione. In genere, metodi di monitoraggio diversi hanno implicazioni hardware diverse. Il metodo di monitoraggio predefinito viene selezionato dal dispositivo.<br/> |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Può essere "wait", "notify", "test" o una combinazione di questi elementi. Per altre informazioni su questi flag, vedere [Wait, Notify e Test Flags.](the-wait-notify-and-test-flags.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore in caso contrario.

## <a name="remarks"></a>Commenti

L'origine della presentazione passa automaticamente all'area di lavoro dopo un comando [play,](play.md) [step](step.md), [pause,](pause.md) [cue](cue.md) "output" [o seek.](seek.md) Il [comando di](record.md) registrazione non cambia automaticamente le origini di presentazione, il che offre all'applicazione la possibilità di non visualizzare il video durante la registrazione.

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

[segnale](cue.md)
</dt> <dt>

[pause](pause.md)
</dt> <dt>

[Giocare](play.md)
</dt> <dt>

[Registrazione](record.md)
</dt> <dt>

[Cercare](seek.md)
</dt> <dt>

[Passo](step.md)
</dt> </dl>

 

