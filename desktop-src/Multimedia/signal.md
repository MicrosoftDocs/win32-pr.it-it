---
title: Signal (comando)
description: Il comando Signal identifica una posizione specificata nell'area di lavoro inviando all'applicazione un \_ messaggio MCISIGNAL mm. I dispositivi digitali video riconoscono questo comando. MCIAVI supporta un solo segnale attivo alla volta.
ms.assetid: 3d10eac0-fd1a-41ee-98fa-2518642c7339
keywords:
- comando segnale Windows Multimedia
topic_type:
- apiref
api_name:
- signal
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4fd96b8970ebbb6502306c6d2d5fd8c49f172cad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301824"
---
# <a name="signal-command"></a>Signal (comando)

Il comando Signal identifica una posizione specificata nell'area di lavoro inviando all'applicazione un messaggio [ \_ MCISIGNAL mm](mm-mcisignal.md) . I dispositivi digitali video riconoscono questo comando. MCIAVI supporta un solo segnale attivo alla volta.

Per inviare questo comando, chiamare la funzione [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con il set di parametri *lpszCommand* come indicato di seguito.

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

Identificatore di un dispositivo MCI. Questo identificatore o alias viene assegnato quando il dispositivo viene aperto.

</dd> <dt>

<span id="lpszSignalFlags"></span><span id="lpszsignalflags"></span><span id="LPSZSIGNALFLAGS"></span>*lpszSignalFlags*
</dt> <dd>

Uno dei flag seguenti.



| Valore            | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| alla posizione      | Specifica il frame per richiamare un segnale.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| cancel           | Rimuove i segnali dall'area di lavoro. Un singolo segnale viene specificato tramite il flag "userValue". Se il flag "userValue" non viene specificato con "Annulla", il dispositivo annulla tutti i segnali. Il flag "Cancel" non è compatibile con i flag "at", "Ever" e "Return position".                                                                                                                                                                                                                                                                                          |
| ogni *intervallo* | Specifica il periodo dei segnali. Il valore dell' *intervallo* è specificato nel formato dell'ora corrente. Se usato con la *posizione*"at", i segnali vengono posizionati in tutta l'area di lavoro con un segno di segnale posizionato alla *posizione*.<br/> Senza il flag "at", i segnali vengono posizionati nell'area di lavoro con un segnale nella posizione corrente.<br/> Se questo flag viene omesso, viene contrassegnata solo la posizione indicata dal flag "at".<br/> Se il valore dell' *intervallo* è inferiore alla frequenza minima supportata da un dispositivo, utilizzerà il relativo valore minimo.<br/> |
| posizione di ritorno  | Indica che il dispositivo deve inviare il valore di posizione anziché l'identificatore "userValue" nel messaggio di segnalazione. L'identificatore "userValue" può comunque essere usato per annullare o ridefinire i contrassegni di segnale.                                                                                                                                                                                                                                                                                                                                                                      |
| *ID* userValue   | Specifica un identificatore restituito con il messaggio di segnalazione. Questo identificatore funge da identificatore che può essere usato con altri comandi del **segnale** per fare riferimento a questa impostazione del **segnale** . Se omesso, il valore predefinito è zero.                                                                                                                                                                                                                                                                                                                                     |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Può essere "Wait", "notify", "test" o una combinazione di questi. Per ulteriori informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore.

## <a name="remarks"></a>Commenti

L'handle della finestra utilizzato per la notifica dei messaggi di completamento del comando viene utilizzato anche per la segnalazione.

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

[\_MCISIGNAL mm](mm-mcisignal.md)
</dt> </dl>

 

