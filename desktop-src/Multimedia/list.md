---
title: comando list
description: Il comando list determina il numero e i tipi di input video e audio. I dispositivi video e videoregistratori digitali riconoscono questo comando.
ms.assetid: b3fe3819-0b8a-4de5-9c79-03e1e089436f
keywords:
- Comando list Windows Multimedia
topic_type:
- apiref
api_name:
- list
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8881c85d146ce869e41d234a72190901135d233f8e45d580d5f568c4ccc48da
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118139474"
---
# <a name="list-command"></a>comando list

Il comando list determina il numero e i tipi di input video e audio. I dispositivi video e videoregistratori digitali riconoscono questo comando.

Per inviare questo comando, chiamare la [**funzione mciSendString**](/previous-versions//dd757161(v=vs.85)) con il parametro *lpszCommand* impostato come indicato di seguito.

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

Identificatore di un dispositivo MCI. Questo identificatore o alias viene assegnato all'apertura del dispositivo.

</dd> <dt>

<span id="lpszList"></span><span id="lpszlist"></span><span id="LPSZLIST"></span>*lpszList*
</dt> <dd>

Flag che identifica il numero e i tipi di input video e audio. Nella tabella seguente sono elencati i tipi di dispositivo che riconoscono il **comando list** e i flag usati da ogni tipo.



| Valore        | Significato                                                                           | Significato                                                                                                                      |
|--------------|-----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| digitalvideo | algoritmo audioaudio quality *algorithm* audio streamcountnumber *index* | still algorithmstill quality *algorithm* video algorithmvideo quality *algorithm* video sourcevideo algorithm video sourcevideo |
| Vcr          | indice del numero di  origine audioaudio                                     | video source countvideo source number *index*                                                                                |



 

Nella tabella seguente sono elencati i flag che è possibile specificare nel **parametro lpszList** e i relativi significati.



| Valore                               | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| algoritmo audio                     | Specifica che il comando deve recuperare i nomi degli algoritmi audio.                                                                                                                                                                                                                                                                                                                                                                                                                           |
| Algoritmo di algoritmo di qualità *audio* | Specifica che il comando deve recuperare i livelli di qualità associati all'algoritmo *specificato.* Se *l'algoritmo* è "current", viene restituito il livello di qualità dell'algoritmo corrente.                                                                                                                                                                                                                                                                                                   |
| conteggio delle origini audio                  | Restituisce il numero totale di input audio.                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Indice del numero di origine *audio*         | Restituisce il tipo di input audio dell'indice *di origine.*                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| flusso audio                        | Specifica che il comando deve recuperare i nomi dei flussi audio associati all'area di lavoro. Queste stringhe,ad esempio "English" o "German" vengono incorporate nel file e identificano il flusso.                                                                                                                                                                                                                                                                                    |
| count                               | Restituisce il numero di opzioni del tipo specificato.                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| indice *dei numeri*                      | Restituisce una stringa che descrive un'opzione specifica (identificata *dall'indice*) del tipo di opzione specificato. *Index* deve essere un numero intero compreso tra 1 e il valore restituito da "count".                                                                                                                                                                                                                                                                                                         |
| algoritmo still                     | Specifica che il comando deve recuperare i nomi degli algoritmi.                                                                                                                                                                                                                                                                                                                                                                                                                           |
| Algoritmo di *algoritmo* still quality | Specifica che il comando deve recuperare i livelli di qualità associati all'algoritmo still *specificato.* Se *l'algoritmo* è "current", viene restituito il livello di qualità dell'algoritmo corrente.                                                                                                                                                                                                                                                                                             |
| algoritmo video                     | Specifica che il comando deve recuperare i nomi degli algoritmi video.                                                                                                                                                                                                                                                                                                                                                                                                                           |
| Algoritmo di algoritmo di qualità *video* | Specifica che il comando deve recuperare i livelli di qualità associati all'algoritmo video *specificato.* Se *l'algoritmo* è "current", viene restituito il livello di qualità dell'algoritmo corrente.                                                                                                                                                                                                                                                                                             |
| origine video                        | Specifica che il comando deve restituire informazioni sulle origini video. Se usato con il flag "count", restituisce il numero di origini video. Se usato con il flag "number", restituisce il tipo di un'origine video. MCI definisce le costanti seguenti per il tipo: "ntsc", "rgb", "pal", "secam", "svideo" e "generic". Potrebbe essere presente più di un'origine di ogni tipo restituito. Il tipo di origine "generico" viene usato quando per il connettore sono consentiti più segnali. |
| conteggio delle origini video                  | Restituisce il numero totale di input video.                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Indice del numero di origine *video*         | Restituisce il tipo di input video dell'indice *di origine.*                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| flusso video                        | Specifica che il comando deve recuperare i nomi dei flussi video associati all'area di lavoro. Queste stringhe, ad esempio "terminazione divertente" o "fine tristi", vengono incorporate nel file e identificano il flusso.                                                                                                                                                                                                                                                                               |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Può essere "wait", "notify" o "test". Per altre informazioni su questi flag, vedere [Flag di attesa, notifica e test](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore in caso contrario.

## <a name="remarks"></a>Commenti

Per i dispositivi VCR, è necessario specificare "origine video" o "origine audio" con i flag "count" o "number". Se si specifica "count", viene restituito il numero totale di input video o audio. Se viene specificato "number", il driver restituisce un tipo corrispondente all'input. Il tipo può essere uno dei seguenti: "tuner", "line", "svideo", "aux" o "generic". In genere, è necessario eseguire prima una query sul videoregistratore per il "conteggio" e quindi usare il conteggio come intervallo per il flag "number". I numeri di origine iniziano da 1.

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

 

