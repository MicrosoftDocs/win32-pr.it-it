---
title: Comando quality
description: Il comando quality definisce un livello di qualità personalizzato per la compressione dei dati audio, video o immagine. I dispositivi video digitali riconoscono questo comando.
ms.assetid: cc920ec9-362c-43db-808e-b9fb59d1df6d
keywords:
- Comando quality Windows Multimedia
topic_type:
- apiref
api_name:
- quality
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f50f019b0e89f21d792f75c13e6c8e755486009d38d242878fec3121333fb9af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118372326"
---
# <a name="quality-command"></a>Comando quality

Il comando quality definisce un livello di qualità personalizzato per la compressione dei dati audio, video o immagine. I dispositivi video digitali riconoscono questo comando.

Per inviare questo comando, chiamare la [**funzione mciSendString**](/previous-versions//dd757161(v=vs.85)) con il parametro *lpszCommand* impostato come indicato di seguito.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("quality %s %s %s"), 
  lpszDeviceID, 
  lpszQuality, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificatore di un dispositivo MCI. Questo identificatore o alias viene assegnato all'apertura del dispositivo.

</dd> <dt>

<span id="lpszQuality"></span><span id="lpszquality"></span><span id="LPSZQUALITY"></span>*lpszQuality*
</dt> <dd>

Uno o più dei flag seguenti. Uno dei tre flag "audio", "still" e "video" deve essere presente.



| Valore                 | Significato                                                                                                                                                                                                                             |
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *algoritmo* algorithm | Associa il livello di qualità all'algoritmo *specificato.* Questo *algoritmo* deve essere supportato dal dispositivo ed essere compatibile con il flag "audio", "still" o "video" usato. Se omesso, viene utilizzato l'algoritmo corrente. |
| nome  audio          | Indica che questo comando specifica un livello di qualità "audio" identificato con *il nome*.                                                                                                                                                   |
| dialogo                | Richiede che nel dispositivo sia visualizzata una finestra di dialogo. Questa finestra di dialogo contiene campi specifici dell'algoritmo usati internamente dal dispositivo per creare la struttura che descrive un livello di qualità specifico.                                    |
| handle *handle*       | Specifica un *handle per una* struttura che contiene dati specifici dell'algoritmo che descrivono un livello di qualità specifico. Le strutture per i dati a cui fa riferimento questo handle sono specifiche del dispositivo.                                         |
| still *name*          | Indica che il comando specifica un livello di qualità "still" identificato con *il nome.*                                                                                                                                                     |
| nome *video*          | Indica che il comando specifica un livello di qualità "video" identificato con *il nome*.                                                                                                                                                     |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Può essere "wait", "notify", "test" o una combinazione di questi elementi. Per altre informazioni su questi flag, vedere [Wait, Notify e Test Flags.](the-wait-notify-and-test-flags.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore in caso contrario.

## <a name="remarks"></a>Commenti

Questo comando definisce un nome di stringa per il livello di qualità, che può quindi essere usato in un [setvideo](setvideo.md) "quality", setvideo "still quality" o [setaudio](setaudio.md) "quality" per impostarlo come livello di qualità video corrente o di compressione audio.

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

[setaudio](setaudio.md)
</dt> <dt>

[setvideo](setvideo.md)
</dt> </dl>

 

