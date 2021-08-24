---
title: comando signal
description: Il comando signal identifica una posizione specificata nell'area di lavoro inviando all'applicazione un messaggio \_ MM MCISIGNAL. I dispositivi video digitali riconoscono questo comando. MCIAVI supporta un solo segnale attivo alla volta.
ms.assetid: 3d10eac0-fd1a-41ee-98fa-2518642c7339
keywords:
- Comando signal Windows Multimedia
topic_type:
- apiref
api_name:
- signal
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0db007a03738f13bb9acc0733b67bcd38de4b97f2b194bb16cdfcd85f798cfdc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037181"
---
# <a name="signal-command"></a>comando signal

Il comando signal identifica una posizione specificata nell'area di lavoro inviando all'applicazione un [messaggio \_ MM MCISIGNAL.](mm-mcisignal.md) I dispositivi video digitali riconoscono questo comando. MCIAVI supporta un solo segnale attivo alla volta.

Per inviare questo comando, chiamare la [**funzione mciSendString**](/previous-versions//dd757161(v=vs.85)) con il parametro *lpszCommand* impostato come segue.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("signal %s %s %s"), 
  lpszDeviceID, 
  lpszSignalFlags, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificatore di un dispositivo MCI. Questo identificatore o alias viene assegnato all'apertura del dispositivo.

</dd> <dt>

<span id="lpszSignalFlags"></span><span id="lpszsignalflags"></span><span id="LPSZSIGNALFLAGS"></span>*lpszSignalFlags*
</dt> <dd>

Uno dei flag seguenti.



| Valore            | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| in corrispondenza della posizione      | Specifica il frame per richiamare un segnale.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| cancel           | Rimuove i segnali dall'area di lavoro. Un singolo segnale viene specificato usando il flag "uservalue". Se il flag "uservalue" non viene specificato usando "cancel", il dispositivo annulla tutti i segnali. Il flag "cancel" non è compatibile con i flag "at", "every" e "return position".                                                                                                                                                                                                                                                                                          |
| ogni *intervallo* | Specifica il periodo dei segnali. Il *valore* dell'intervallo viene specificato nel formato di ora corrente. Se usato con la posizione *"at",* i segnali vengono posizionati in tutta l'area di lavoro con un contrassegno di segnale posizionato nella *posizione*.<br/> Senza il flag "at", i segnali vengono inseriti in tutta l'area di lavoro con un segnale nella posizione corrente.<br/> Se questo flag viene omesso, viene contrassegnata solo la posizione indicata dal flag "at".<br/> Se il *valore* dell'intervallo è minore della frequenza minima supportata da un dispositivo, verrà utilizzato il valore minimo.<br/> |
| return position  | Indica che il dispositivo deve inviare il valore della posizione anziché l'identificatore "uservalue" nel messaggio di segnalazione. L'identificatore "uservalue" può comunque essere usato per annullare o ridefinire i contrassegni di segnale.                                                                                                                                                                                                                                                                                                                                                                      |
| uservalue *id*   | Specifica un identificatore segnalato con il messaggio di segnalazione. Questo identificatore funge da identificatore che può essere usato con altri comandi di **segnale** per fare riferimento a questa **impostazione del** segnale. Se omesso, il valore predefinito è zero.                                                                                                                                                                                                                                                                                                                                     |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Può essere "wait", "notify", "test" o una combinazione di questi elementi. Per altre informazioni su questi flag, vedere [Wait, Notify e Test Flags.](the-wait-notify-and-test-flags.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore in caso contrario.

## <a name="remarks"></a>Commenti

L'handle di finestra usato per la notifica dei messaggi di completamento dei comandi viene usato anche per la segnalazione.

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

[MM \_ MCISIGNAL](mm-mcisignal.md)
</dt> </dl>

 

