---
title: Comando settuner
description: Il comando settuner modifica il siner corrente o l'impostazione del canale del siner corrente. I dispositivi vcr riconoscono questo comando.
ms.assetid: 76d05210-3c2a-4d00-b3eb-c912c1deabf7
keywords:
- Comando settuner Windows Multimedia
topic_type:
- apiref
api_name:
- settuner
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7075de6ed50c49773a502ba77e093d84e85b079a6b17c462ea8ee65ad1330aa6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119688800"
---
# <a name="settuner-command"></a>Comando settuner

Il comando settuner modifica il siner corrente o l'impostazione del canale del siner corrente. I dispositivi vcr riconoscono questo comando.

Per inviare questo comando, chiamare la [**funzione mciSendString**](/previous-versions//dd757161(v=vs.85)) con il parametro *lpszCommand* impostato come indicato di seguito.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("settuner %s %s %s"), 
  lpszDeviceID, 
  lpszTuner, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificatore di un dispositivo MCI. Questo identificatore o alias viene assegnato all'apertura del dispositivo.

</dd> <dt>

<span id="lpszTuner"></span><span id="lpsztuner"></span><span id="LPSZTUNER"></span>*lpszTuner*
</dt> <dd>

Uno dei flag seguenti.



| Valore                            | Significato                                                                                                                                                                                                                                                                                                     |
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| canale *canale*                | Imposta il siner sul *canale*. Potrebbe non essere possibile modificare il canale durante la registrazione, a seconda del videoregistratore. Un canale maggiore del valore massimo imposta il siner sul canale massimo.                                                                                                                    |
| channel seek upchannel seek down | Cerca il canale successivo con un segnale valido. "Seek up" incrementa il numero di canale nella ricerca. "Cerca in basso" decrementa il numero di canale nella ricerca. Il tuner esegue il wrapping al canale 1 quando viene superato il numero massimo di canali. Analogamente, quando si cerca verso il basso, il tuner esegue il wrapping al canale massimo. |
| channel upchannel down           | Incrementa o decrementa il canale del tuner. Potrebbe non essere possibile modificare il canale durante la registrazione, a seconda del videoregistratore. Il tuner esegue il wrapping al canale 1 quando viene superato il numero massimo di canali. Analogamente, quando si cerca verso il basso, il tuner esegue il wrapping al canale massimo.                              |
| number *number*                  | Specifica il siner interessato dal comando settuner. Se *number* non viene specificato, viene utilizzato il valore predefinito 1.                                                                                                                                                                                    |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Può essere "wait", "notify", "test" o una combinazione di questi elementi. Per altre informazioni su questi flag, vedere [Wait, Notify e Test Flags.](the-wait-notify-and-test-flags.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore in caso contrario.

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
</dt> </dl>

 

