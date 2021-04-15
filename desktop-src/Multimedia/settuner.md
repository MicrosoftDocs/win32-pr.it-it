---
title: comando setuner
description: Il comando setuner modifica il sintonizzatore corrente o l'impostazione del canale del sintonizzatore corrente. I dispositivi VCR riconoscono questo comando.
ms.assetid: 76d05210-3c2a-4d00-b3eb-c912c1deabf7
keywords:
- comando di setuner Windows Multimedia
topic_type:
- apiref
api_name:
- settuner
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51150043a68f3cd34525eb74a64237fc4dc150e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479367"
---
# <a name="settuner-command"></a>comando setuner

Il comando setuner modifica il sintonizzatore corrente o l'impostazione del canale del sintonizzatore corrente. I dispositivi VCR riconoscono questo comando.

Per inviare questo comando, chiamare la funzione [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con il set di parametri *lpszCommand* come indicato di seguito.

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

Identificatore di un dispositivo MCI. Questo identificatore o alias viene assegnato quando il dispositivo viene aperto.

</dd> <dt>

<span id="lpszTuner"></span><span id="lpsztuner"></span><span id="LPSZTUNER"></span>*lpszTuner*
</dt> <dd>

Uno dei flag seguenti.



| Valore                            | Significato                                                                                                                                                                                                                                                                                                     |
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *canale* canale                | Imposta il sintonizzatore sul *canale*. Potrebbe non essere possibile modificare il canale durante la registrazione, a seconda del videoregistratore. Un canale di dimensioni maggiori rispetto al valore massimo imposta il sintonizzatore sul canale massimo.                                                                                                                    |
| ricerca canale verso il basso | Cerca il canale successivo con un segnale valido. "Seek Up" incrementa il numero di canale nella ricerca. "Seek Down" decrementa il numero di canale nella ricerca. Il sintonizzatore esegue il wrapping sul canale 1 quando viene superato il numero massimo di canali. Analogamente, durante la ricerca, il sintonizzatore esegue il wrapping sul canale massimo. |
| canale verso il basso           | Incrementa o decrementa il canale del sintonizzatore. Potrebbe non essere possibile modificare il canale durante la registrazione, a seconda del videoregistratore. Il sintonizzatore esegue il wrapping sul canale 1 quando viene superato il numero massimo di canali. Analogamente, durante la ricerca, il sintonizzatore esegue il wrapping sul canale massimo.                              |
| numero                   | Specifica il sintonizzatore interessato dal comando setuner. Se il *numero* non viene specificato, viene utilizzato il valore predefinito 1.                                                                                                                                                                                    |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Può essere "Wait", "notify", "test" o una combinazione di questi. Per ulteriori informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore.

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
</dt> </dl>

 

