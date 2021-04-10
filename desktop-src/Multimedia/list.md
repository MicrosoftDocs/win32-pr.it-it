---
title: comando list
description: Il comando list determina il numero e i tipi di input video e audio. I dispositivi Digital-video e VCR riconoscono questo comando.
ms.assetid: b3fe3819-0b8a-4de5-9c79-03e1e089436f
keywords:
- elenco dei comandi multimediali di Windows
topic_type:
- apiref
api_name:
- list
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5d0a171c6768caf1b947a0d07cb46e5cccd28c6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121459"
---
# <a name="list-command"></a>comando list

Il comando list determina il numero e i tipi di input video e audio. I dispositivi Digital-video e VCR riconoscono questo comando.

Per inviare questo comando, chiamare la funzione [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con il set di parametri *lpszCommand* come indicato di seguito.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("list %s %s %s"), 
  lpszDeviceID, 
  lpszList, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificatore di un dispositivo MCI. Questo identificatore o alias viene assegnato quando il dispositivo viene aperto.

</dd> <dt>

<span id="lpszList"></span><span id="lpszlist"></span><span id="LPSZLIST"></span>*lpszList*
</dt> <dd>

Flag che identifica il numero e i tipi di input audio e video. Nella tabella seguente sono elencati i tipi di dispositivo che riconoscono il comando **List** e i flag utilizzati da ogni tipo.



| Valore        | Significato                                                                           | Significato                                                                                                                      |
|--------------|-----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| digitalvideo | *Indice* streamcountnumber audio *algoritmo* algoritmo algorithmaudio di qualità audio | Still algorithmstill *Quality Algorithm Algorithm video algorithmvideo* Stream algorithm *algoritmo video SourceVideo* |
| VCR          | *Indice* numero di origine countaudio origine audio                                     | *Indice* numero di origine countvideo origine video                                                                                |



 

Nella tabella seguente sono elencati i flag che è possibile specificare nel parametro **lpszList** e i relativi significati.



| Valore                               | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| algoritmo audio                     | Specifica che il comando deve recuperare i nomi degli algoritmi audio.                                                                                                                                                                                                                                                                                                                                                                                                                           |
| *algoritmo* algoritmo di qualità audio | Specifica che il comando deve recuperare i livelli di qualità associati all' *algoritmo* specificato. Se *Algorithm* è "Current", viene restituito il livello di qualità dell'algoritmo corrente.                                                                                                                                                                                                                                                                                                   |
| conteggio origine audio                  | Restituisce il numero totale di input audio.                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| *Indice* numero di origine audio         | Restituisce il tipo di input audio dell' *Indice* di origine.                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| flusso audio                        | Specifica che il comando deve recuperare i nomi dei flussi audio associati all'area di lavoro. Queste stringhe (ad esempio "inglese" o "tedesco") sono incorporate nel file e identificano il flusso.                                                                                                                                                                                                                                                                                    |
| count                               | Restituisce il numero di opzioni del tipo specificato.                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| *Indice* numero                      | Restituisce una stringa che descrive un'opzione specifica (identificata dall' *Indice*) del tipo di opzione specificato. *Index* deve essere un numero intero compreso tra 1 e il valore restituito da "count".                                                                                                                                                                                                                                                                                                         |
| algoritmo still                     | Specifica che il comando deve recuperare i nomi degli algoritmi ancora.                                                                                                                                                                                                                                                                                                                                                                                                                           |
| *algoritmo* di algoritmo di qualità ancora | Specifica che il comando deve recuperare i livelli di qualità associati all' *algoritmo* ancora specificato. Se *Algorithm* è "Current", viene restituito il livello di qualità dell'algoritmo corrente.                                                                                                                                                                                                                                                                                             |
| algoritmo video                     | Specifica che il comando deve recuperare i nomi degli algoritmi video.                                                                                                                                                                                                                                                                                                                                                                                                                           |
| *algoritmo* algoritmo di qualità video | Specifica che il comando deve recuperare i livelli di qualità associati all' *algoritmo* video specificato. Se *Algorithm* è "Current", viene restituito il livello di qualità dell'algoritmo corrente.                                                                                                                                                                                                                                                                                             |
| origine video                        | Specifica che il comando deve restituire informazioni sulle origini video. Quando viene usato con il flag "count", restituisce il numero di origini video. Quando viene usato con il flag "Number", restituisce il tipo di un'origine video. MCI definisce le costanti seguenti per il tipo: "NTSC", "RGB", "PAL", "SECAM", "SVIDEO" e "generico". Potrebbe essere restituita più di un'origine di ogni tipo. Il tipo di origine "generico" viene usato quando è consentito più di un segnale per quel connettore. |
| conteggio origine video                  | Restituisce il numero totale di input video.                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| *Indice* numero origine video         | Restituisce il tipo di input video dell' *Indice* di origine.                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| flusso video                        | Specifica che il comando deve recuperare i nomi dei flussi video associati all'area di lavoro. Queste stringhe (ad esempio "fine divertente" o "fine triste") sono incorporate nel file e identificano il flusso.                                                                                                                                                                                                                                                                               |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Può essere "Wait", "notify" o "test". Per ulteriori informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore.

## <a name="remarks"></a>Commenti

Per i dispositivi VCR, è necessario specificare "origine video" o "origine audio" con i flag "conteggio" o "numero". Se si specifica "count", viene restituito il numero totale di input di video o audio. Se si specifica "Number", il driver restituisce un tipo corrispondente all'input. Il tipo può essere uno dei seguenti: "Tuner", "line", "SVIDEO", "aux" o "Generic". In genere, è necessario prima eseguire una query sul VCR per il "conteggio" e quindi usare il conteggio come intervallo per il flag "Number". I numeri "Source" iniziano da 1.

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

 

