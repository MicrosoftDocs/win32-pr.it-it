---
title: Comando freeze
description: Il comando freeze blocca l'input video o l'output video in un videoregistratore o disabilita l'acquisizione video nel buffer dei fotogrammi. Questo comando viene riconosciuto da dispositivi di video digitale, sovrimpressione video e videoregistratore.
ms.assetid: 49f3ab98-e893-402a-be78-6140af3b81df
keywords:
- Comando freeze Windows Multimedia
topic_type:
- apiref
api_name:
- freeze
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1261cc75575a5b59d200ff965a5325caef9fa966
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481557"
---
# <a name="freeze-command"></a>Comando freeze

Il comando freeze blocca l'input video o l'output video in un videoregistratore o disabilita l'acquisizione video nel buffer dei fotogrammi. Questo comando viene riconosciuto da dispositivi di video digitale, sovrimpressione video e videoregistratore.

Per inviare questo comando, chiamare la [**funzione mciSendString**](/previous-versions//dd757161(v=vs.85)) con il parametro *lpszCommand* impostato come indicato di seguito.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("freeze %s %s %s"), 
  lpszDeviceID, 
  lpszFreezeFlags, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificatore di un dispositivo MCI. Questo identificatore o alias viene assegnato all'apertura del dispositivo.

</dd> <dt>

<span id="lpszFreezeFlags"></span><span id="lpszfreezeflags"></span><span id="LPSZFREEZEFLAGS"></span>*lpszFreezeFlags*
</dt> <dd>

Flag che identifica gli elementi da bloccare. La tabella seguente elenca i tipi di dispositivo che riconoscono il **comando freeze** e i flag usati da ogni tipo.




| valore | Significato | Significato | 
|-------|---------|---------|
| digitalvideo | at <em>rectangle</em> | Fuori | 
| overlay | at <em>rectangle</em> | 
| Vcr | <ul><li>campo</li><li>frame</li></ul> | <ul><li>input</li><li>output</li></ul> | 




 

La tabella seguente elenca i flag che possono essere specificati nel *parametro lpszFreezeFlags* e i relativi significati.



| valore          | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| at *rectangle* | Specifica l'area che verrà bloccata. Per i dispositivi con sovrimpressione video, l'acquisizione video in quest'area sarà disabilitata. Per i dispositivi video digitali, i pixel all'interno del rettangolo avranno il bit della maschera di blocco attivato (a meno che non sia specificato il flag "esterno"). Il rettangolo è relativo all'origine del buffer video e viene specificato come *X1 Y1 X2 Y2*. Le coordinate *X1 Y1* specificano l'angolo superiore sinistro del rettangolo e le coordinate *X2 Y2* specificano la larghezza e l'altezza. |
| campo          | Blocca il primo campo. Il campo viene presupposto per impostazione predefinita (se non viene specificato né il frame né il campo).                                                                                                                                                                                                                                                                                                                                                                                               |
| frame          | Blocca l'intero frame, visualizzando entrambi i campi.                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| input          | Blocca il frame corrente dell'immagine di input, indipendentemente dal fatto che sia in pausa o in esecuzione.                                                                                                                                                                                                                                                                                                                                                                                                                |
| output         | Blocca il frame corrente dell'output dal vcr. Se il videoregistratore viene riprodotto quando viene generato il blocco, il frame corrente viene bloccato e il videoregistratore viene sospeso. Se il videoregistratore viene sospeso quando viene eseguito questo comando, il frame corrente viene bloccato. L'immagine bloccata rimane nel dispositivo di output fino a [quando non viene](unfreeze.md) eseguito un comando di sblocco. Se non viene specificato né "input" né "output", viene utilizzato "output".                                                                                    |
| Fuori        | Indica che l'area esterna all'area specificata usando il flag "at" è bloccata.                                                                                                                                                                                                                                                                                                                                                                                                           |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Può essere "wait", "notify" o entrambi. Per i dispositivi video digitali e VCR, è anche possibile specificare "test". Per altre informazioni su questi flag, vedere [Wait, Notify e Test Flags.](the-wait-notify-and-test-flags.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore in caso contrario.

## <a name="remarks"></a>Commenti

Se usato con dispositivi a videoregistrazione, questo comando è destinato alle schede di cattura dei fotogrammi.

Per specificare aree di acquisizione irregolari con il flag "at", usare una serie di comandi freeze e [unfreeze.](unfreeze.md) Alcuni dispositivi di sovrapposizione video limitano la complessità dell'area di acquisizione.

Questo comando è supportato solo se una chiamata al [comando capability](capability.md) con il flag "can freeze" restituisce **TRUE.**

## <a name="examples"></a>Esempio

Il comando seguente disabilita l'acquisizione video in un quadrato di 100 pixel nell'angolo superiore sinistro del buffer video.

``` syntax
freeze vboard at 0 0 100 100
```

## <a name="requirements"></a>Requisiti



| Requisito | valore |
|-------------------------------------|------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/> |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[Stringhe di comando MCI](mci-command-strings.md)
</dt> <dt>

[capability](capability.md)
</dt> <dt>

[Sbloccare](unfreeze.md)
</dt> </dl>

 

