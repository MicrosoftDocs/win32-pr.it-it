---
title: Salva comando
description: Il comando Save Salva un file MCI. Video-overlay e waveform-i dispositivi audio riconoscono questo comando. Sebbene i dispositivi Digital-video e i sequencer MIDI riconoscano anche questo comando, i driver MCIAVI e MCISEQ non lo supportano.
ms.assetid: cae199b3-4ac4-49e0-9213-12d816b2f865
keywords:
- Salva comando di Windows
topic_type:
- apiref
api_name:
- save
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0029ad03c1b7fe855e8485b2719b11628fac1103
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301012"
---
# <a name="save-command"></a>Salva comando

Il comando Save Salva un file MCI. Video-overlay e waveform-i dispositivi audio riconoscono questo comando. Sebbene i dispositivi Digital-video e i sequencer MIDI riconoscano anche questo comando, i driver MCIAVI e MCISEQ non lo supportano.

Per inviare questo comando, chiamare la funzione [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con il set di parametri *lpszCommand* come indicato di seguito.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("save %s %s %s"), 
  lpszDeviceID, 
  lpszFilename, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificatore di un dispositivo MCI. Questo identificatore o alias viene assegnato quando il dispositivo viene aperto.

</dd> <dt>

<span id="lpszFilename"></span><span id="lpszfilename"></span><span id="LPSZFILENAME"></span>*lpszFilename*
</dt> <dd>

Flag che specifica il nome del file salvato e, facoltativamente, flag aggiuntivi che modificano l'operazione di salvataggio. Nella tabella seguente sono elencati i tipi di dispositivo che riconoscono il comando **Salva** e i flag utilizzati da ogni tipo.



| Valore        | Significato              | Significato               |
|--------------|----------------------|-----------------------|
| digitalvideo | Interrompi al *rettangolo* | *nome file* keepreserve |
| overlay      | al *rettangolo*       | *filename*            |
| sequencer    | *filename*           |                       |
| WaveAudio    | *filename*           |                       |



 

Nella tabella seguente sono elencati i flag che è possibile specificare nel parametro **lpszFileName** e i relativi significati.



| Valore          | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abort          | Arresta un'operazione di **salvataggio** in corso. Se utilizzato, deve essere l'unico elemento presente.                                                                                                                                                                                                                                                                                                                                                                                                                 |
| al *rettangolo* | Specifica un rettangolo relativo all'origine del buffer del frame. Il *rettangolo* viene specificato come *X1 Y1 Y1 2*. Le coordinate *X1 Y1* specificano l'angolo superiore sinistro e le coordinate *X2 Y2* specificano la larghezza e l'altezza. Per i dispositivi digitali video, il comando [Acquisisci](capture.md) viene usato per acquisire il contenuto del buffer del frame.<br/>                                                                                                                                               |
| *filename*     | Specifica il nome file da assegnare al file di dati. Se non si specifica un percorso, il file verrà inserito sul disco e nella directory specificata in precedenza nel comando di [riserva](reserve.md) esplicito o implicito. Se **Reserve** non è stato emesso, l'unità e la directory predefinite sono quelle associate all'attività dell'applicazione. Se viene specificato un percorso, è possibile che il dispositivo lo richieda nell'unità disco specificata dalla **riserva** esplicita o implicita. Questo flag è obbligatorio. |
| keepreserve    | Specifica che lo spazio su disco inutilizzato rimanente dal comando di **riserva** originale non viene deallocato.                                                                                                                                                                                                                                                                                                                                                                                                 |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Può essere "Wait", "notify" o entrambi. Per i dispositivi digitali video e VCR è possibile specificare anche "test". Per ulteriori informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore.

## <a name="remarks"></a>Commenti

La variabile *filename* è obbligatoria se il dispositivo è stato aperto con l'identificatore del dispositivo "nuovo".

## <a name="examples"></a>Esempio

Il seguente comando Salva l'intero buffer video in un file denominato VCAPFILE. TGA.

``` syntax
save vboard c:\vcap\vcapfile.tga
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

[catturare](capture.md)
</dt> <dt>

[riserva](reserve.md)
</dt> </dl>

 

