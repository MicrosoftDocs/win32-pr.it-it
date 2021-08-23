---
title: Comando info
description: Il comando info recupera una descrizione dell'hardware da un dispositivo. Tutti i dispositivi MCI riconoscono questo comando.
ms.assetid: cdd6628b-bff8-4a0d-9dad-a63321f584ea
keywords:
- Comando info Windows Multimedia
topic_type:
- apiref
api_name:
- info
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f15675923f37a80ce694a400f18113f5178a54a3f75664008644919c6d9fc128
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119690471"
---
# <a name="info-command"></a>Comando info

Il comando info recupera una descrizione dell'hardware da un dispositivo. Tutti i dispositivi MCI riconoscono questo comando.

Per inviare questo comando, chiamare la [**funzione mciSendString**](/previous-versions//dd757161(v=vs.85)) con il parametro *lpszCommand* impostato come indicato di seguito.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("info %s %s %s"), 
  lpszDeviceID, 
  lpszInfoType, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificatore di un dispositivo MCI. Questo identificatore o alias viene assegnato all'apertura del dispositivo.

</dd> <dt>

<span id="lpszInfoType"></span><span id="lpszinfotype"></span><span id="LPSZINFOTYPE"></span>*lpszInfoType*
</dt> <dd>

Flag che identifica il tipo di informazioni necessarie. La tabella seguente elenca i tipi di dispositivo che **riconoscono il comando info** e i flag usati da ogni tipo.



| Valore        | Significato                                                             | Significato                                             |
|--------------|---------------------------------------------------------------------|-----------------------------------------------------|
| cdaudio      | info identityinfo upc                                               | product                                             |
| digitalvideo | algoritmo audioaudio qualityfileproduzione algoritmostill qualità | usageversione algorithmvideo qualitywindow text |
| overlay      | fileproduct                                                         | testo della finestra                                         |
| sequencer    | copyrightfile                                                       | nameproduct                                         |
| Vcr          | product                                                             | version                                             |
| videodisk    | product                                                             |                                                     |
| Waveaudio    | fileinput                                                           | outputproduct                                       |



 

La tabella seguente elenca i flag che possono essere specificati nel **parametro lpszInfoType** e i relativi significati.



| Valore           | Significato                                                                                                                                                                                            |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| algoritmo audio | Restituisce il nome dell'algoritmo di compressione audio corrente.                                                                                                                                       |
| qualità audio   | Restituisce il nome del descrittore di qualità audio corrente. Questa operazione potrebbe restituire "unknown" se l'applicazione ha impostato parametri su valori specifici che non corrispondono a qualità definite.       |
| copyright       | Recupera le informazioni sul copyright del file MIDI dall'evento meta copyright.                                                                                                                            |
| file            | Recupera il nome del file utilizzato dal dispositivo composto. Se il dispositivo viene aperto senza un file e il [comando load](load.md) non è stato usato, viene restituita una stringa Null.                  |
| info identity   | Produce un identificatore univoco per il CD audio attualmente caricato nel lettore sottoposto a query.                                                                                                        |
| info upc        | Produce il codice UPC (Universal Product Code) codificato in un CD audio. L'UPC è una stringa di cifre. Potrebbe non essere disponibile per tutti i CD.                                                    |
| input           | Recupera la descrizione del dispositivo di input corrente. Restituisce "none" se non è impostato un dispositivo di input.                                                                                               |
| name            | Recupera il nome della sequenza dall'evento meta nome sequenza/traccia.                                                                                                                               |
| output          | Recupera la descrizione del dispositivo di output corrente. Restituisce "none" se non è impostato un dispositivo di output.                                                                                             |
| product         | Recupera una descrizione del dispositivo. Queste informazioni includono spesso il nome del prodotto e il modello. La lunghezza della stringa sarà di 31 caratteri o meno.                                               |
| algoritmo still | Restituisce il nome dell'algoritmo di compressione dell'immagine ancorata corrente.                                                                                                                                 |
| qualità ancora   | Restituisce il nome del descrittore di qualità dell'immagine ancora corrente. Questa operazione potrebbe restituire "unknown" se l'applicazione ha impostato parametri su valori specifici che non corrispondono a qualità definite. |
| utilizzo           | Restituisce una stringa che descrive le restrizioni di utilizzo che potrebbero essere imposte dal proprietario dei dati audio o visivi nell'area di lavoro.                                                                    |
| version         | Restituisce il livello di rilascio del driver di dispositivo e dell'hardware.                                                                                                                                       |
| algoritmo video | Restituisce il nome dell'algoritmo di compressione video corrente.                                                                                                                                       |
| qualità video   | Restituisce il nome del descrittore di qualità video corrente. Questa operazione potrebbe restituire "unknown" se l'applicazione ha impostato parametri su valori specifici che non corrispondono a qualità definite.       |
| testo della finestra     | Recupera la didascalia della finestra utilizzata dal dispositivo.                                                                                                                                            |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Può essere "wait", "notify" o entrambi. Per i dispositivi video digitali e VCR, è anche possibile specificare "test". Per altre informazioni su questi flag, vedere [Wait, Notify e Test Flags.](the-wait-notify-and-test-flags.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore in caso contrario.

## <a name="examples"></a>Esempio

Il comando seguente recupera una descrizione dell'hardware associato al dispositivo "mysound".

``` syntax
info mysound product
```

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

[carico](load.md)
</dt> </dl>

 

