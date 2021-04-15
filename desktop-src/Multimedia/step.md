---
title: comando Step
description: Il comando Step esegue la riproduzione di uno o più frame avanti o indietro. L'azione predefinita prevede l'esecuzione del passaggio avanti di un frame. I dispositivi videodisco Digital-video, VCR e CAV-Format riconoscono questo comando.
ms.assetid: 6017ace5-cde9-42a0-bb2f-f85d7847adc5
keywords:
- comando passaggio Windows Multimedia
topic_type:
- apiref
api_name:
- step
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6203d0b2d5dea401e8197e1261946955cd28618a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476583"
---
# <a name="step-command"></a>comando Step

Il comando Step esegue la riproduzione di uno o più frame avanti o indietro. L'azione predefinita prevede l'esecuzione del passaggio avanti di un frame. I dispositivi videodisco Digital-video, VCR e CAV-Format riconoscono questo comando.

Per inviare questo comando, chiamare la funzione [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con il set di parametri *lpszCommand* come indicato di seguito.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("step %s %s %s"), 
  lpszDeviceID, 
  lpszStepFlags, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificatore di un dispositivo MCI. Questo identificatore o alias viene assegnato quando il dispositivo viene aperto.

</dd> <dt>

<span id="lpszStepFlags"></span><span id="lpszstepflags"></span><span id="LPSZSTEPFLAGS"></span>*lpszStepFlags*
</dt> <dd>

Uno o entrambi i flag seguenti.



| Valore       | Significato                                                                                                                  |
|-------------|--------------------------------------------------------------------------------------------------------------------------|
| per *frame* | Indica il numero di frame da scorrere. Se si specifica un valore di *frame* negativi, non è possibile specificare il flag "Reverse". |
| reverse     | Eseguire il passaggio dei frame in senso inverso.                                                                                              |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Può essere "Wait", "notify" o entrambi. Per i dispositivi digitali video e VCR è possibile specificare anche "test". Per ulteriori informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).

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

 

