---
title: comando info
description: Il comando info recupera una descrizione hardware da un dispositivo. Tutti i dispositivi MCI riconoscono questo comando.
ms.assetid: cdd6628b-bff8-4a0d-9dad-a63321f584ea
keywords:
- comando informazioni Windows Multimedia
topic_type:
- apiref
api_name:
- info
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6d401efca6a59d1ed3cbf433d7c33311678705d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400865"
---
# <a name="info-command"></a>comando info

Il comando info recupera una descrizione hardware da un dispositivo. Tutti i dispositivi MCI riconoscono questo comando.

Per inviare questo comando, chiamare la funzione [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con il set di parametri *lpszCommand* come indicato di seguito.

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

Identificatore di un dispositivo MCI. Questo identificatore o alias viene assegnato quando il dispositivo viene aperto.

</dd> <dt>

<span id="lpszInfoType"></span><span id="lpszinfotype"></span><span id="LPSZINFOTYPE"></span>*lpszInfoType*
</dt> <dd>

Flag che identifica il tipo di informazioni richieste. Nella tabella seguente sono elencati i tipi di dispositivo che riconoscono il comando **info** e i flag utilizzati da ogni tipo.



| Valore        | Significato                                                             | Significato                                             |
|--------------|---------------------------------------------------------------------|-----------------------------------------------------|
| cdaudio      | info IdentityInfo UPC                                               | product                                             |
| digitalvideo | audio algorithmaudio qualityfileproductstill algorithmstill Quality | testo qualitywindow algorithmvideo usageversionvideo |
| overlay      | fileproduct                                                         | testo finestra                                         |
| sequencer    | copyrightfile                                                       | nameproduct                                         |
| VCR          | product                                                             | version                                             |
| videodisk    | product                                                             |                                                     |
| WaveAudio    | FileInput                                                           | outputproduct                                       |



 

Nella tabella seguente sono elencati i flag che è possibile specificare nel parametro **lpszInfoType** e i relativi significati.



| Valore           | Significato                                                                                                                                                                                            |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| algoritmo audio | Restituisce il nome dell'algoritmo di compressione audio corrente.                                                                                                                                       |
| qualità audio   | Restituisce il nome del descrittore di qualità audio corrente. Questo potrebbe restituire "Unknown" se l'applicazione dispone di parametri impostati su valori specifici che non corrispondono a qualità definite.       |
| copyright       | Recupera le informazioni sul copyright del file MIDI dall'evento meta del copyright.                                                                                                                            |
| file            | Recupera il nome del file usato dal dispositivo composto. Se il dispositivo viene aperto senza un file e non è stato usato il comando [Load](load.md) , viene restituita una stringa null.                  |
| identità informazioni   | Produce un identificatore univoco per il CD audio attualmente caricato nel lettore sottoposto a query.                                                                                                        |
| info UPC        | Genera il codice di prodotto universale (UPC) codificato in un CD audio. L'UPC è una stringa di cifre. Potrebbe non essere disponibile per tutti i CDs.                                                    |
| input           | Recupera la descrizione del dispositivo di input corrente. Restituisce "None" se non è impostato un dispositivo di input.                                                                                               |
| name            | Recupera il nome della sequenza dall'evento meta del nome di sequenza/track.                                                                                                                               |
| output          | Recupera la descrizione del dispositivo di output corrente. Restituisce "None" se non è impostato un dispositivo di output.                                                                                             |
| product         | Recupera una descrizione del dispositivo. Queste informazioni includono spesso il nome del prodotto e il modello. La lunghezza della stringa sarà pari a 31 caratteri o meno.                                               |
| algoritmo still | Restituisce il nome dell'algoritmo di compressione delle immagini ancora corrente.                                                                                                                                 |
| qualità ancora   | Restituisce il nome del descrittore di qualità dell'immagine ancora corrente. Questo potrebbe restituire "Unknown" se l'applicazione dispone di parametri impostati su valori specifici che non corrispondono a qualità definite. |
| utilizzo           | Restituisce una stringa che descrive le restrizioni di utilizzo che potrebbero essere imposte dal proprietario dei dati visivi o audio nell'area di lavoro.                                                                    |
| version         | Restituisce il livello di rilascio del driver e dell'hardware del dispositivo.                                                                                                                                       |
| algoritmo video | Restituisce il nome dell'algoritmo di compressione video corrente.                                                                                                                                       |
| qualità video   | Restituisce il nome del descrittore di qualità video corrente. Questo potrebbe restituire "Unknown" se l'applicazione dispone di parametri impostati su valori specifici che non corrispondono a qualità definite.       |
| testo finestra     | Recupera la didascalia della finestra usata dal dispositivo.                                                                                                                                            |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Può essere "Wait", "notify" o entrambi. Per i dispositivi digitali video e VCR è possibile specificare anche "test". Per ulteriori informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore.

## <a name="examples"></a>Esempio

Il comando che segue recupera una descrizione dell'hardware associato al dispositivo "audio".

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

[MCI](mci.md)
</dt> <dt>

[Stringhe di comando MCI](mci-command-strings.md)
</dt> <dt>

[carico](load.md)
</dt> </dl>

 

