---
title: comando Quality
description: Il comando qualità definisce un livello di qualità personalizzato per la compressione di dati audio, video o di immagine continua. I dispositivi digitali video riconoscono questo comando.
ms.assetid: cc920ec9-362c-43db-808e-b9fb59d1df6d
keywords:
- controllo qualità Windows Multimedia
topic_type:
- apiref
api_name:
- quality
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2de9cc61d72db541b5f06d8903d7c9dcf153ce07
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302352"
---
# <a name="quality-command"></a>comando Quality

Il comando qualità definisce un livello di qualità personalizzato per la compressione di dati audio, video o di immagine continua. I dispositivi digitali video riconoscono questo comando.

Per inviare questo comando, chiamare la funzione [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con il set di parametri *lpszCommand* come indicato di seguito.

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

Identificatore di un dispositivo MCI. Questo identificatore o alias viene assegnato quando il dispositivo viene aperto.

</dd> <dt>

<span id="lpszQuality"></span><span id="lpszquality"></span><span id="LPSZQUALITY"></span>*lpszQuality*
</dt> <dd>

Uno o più dei flag seguenti. (Uno dei tre flag "audio", "ancora" e "video" deve essere presente).



| Valore                 | Significato                                                                                                                                                                                                                             |
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| algoritmo *algoritmo* | Associa il livello di qualità all' *algoritmo* specificato. Questo *algoritmo* deve essere supportato dal dispositivo ed essere compatibile con il flag "audio", "ancora" o "video" usato. Se omesso, viene utilizzato l'algoritmo corrente. |
| *nome* audio          | Indica che questo comando specifica un livello di qualità "audio" identificato con il *nome*.                                                                                                                                                   |
| dialogo                | Richiede che il dispositivo visualizzi una finestra di dialogo. Questa finestra di dialogo contiene campi specifici dell'algoritmo che vengono usati internamente dal dispositivo per creare la struttura che descrive un livello di qualità specifico.                                    |
| handle *handle*       | Specifica un *handle* per una struttura che contiene dati specifici dell'algoritmo che descrivono un livello di qualità specifico. Le strutture per i dati a cui fa riferimento questo handle sono specifiche del dispositivo.                                         |
| *nome* ancora          | Indica che il comando specifica un livello di qualità "ancora" identificato con il *nome.*                                                                                                                                                     |
| *nome* del video          | Indica che il comando specifica un livello di qualità "video" identificato con il *nome*.                                                                                                                                                     |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Può essere "Wait", "notify", "test" o una combinazione di questi. Per ulteriori informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore.

## <a name="remarks"></a>Commenti

Questo comando definisce un nome di stringa per il livello di qualità, che può quindi essere utilizzato in un comando [sevideo](setvideo.md) "Quality", sevideo "still Quality [" o "Quality",](setaudio.md) per stabilirlo come il video corrente, ancora o il livello di qualità della compressione audio.

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

[SetAudio](setaudio.md)
</dt> <dt>

[video](setvideo.md)
</dt> </dl>

 

