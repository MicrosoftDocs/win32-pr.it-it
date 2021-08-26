---
title: Comando save
description: Il comando save salva un file MCI. I dispositivi con sovrimpressione video e audio waveform riconoscono questo comando. Anche se i dispositivi video digitali e i sequencer MIDI riconoscono anche questo comando, i driver MCIAVI e MCISEQ non lo supportano.
ms.assetid: cae199b3-4ac4-49e0-9213-12d816b2f865
keywords:
- Comando save Windows Multimedia
topic_type:
- apiref
api_name:
- save
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0c7b4fb75f78f8468a204217f5a4fa1593a1c50d5db541a83070a7faed41cc5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037481"
---
# <a name="save-command"></a>Comando save

Il comando save salva un file MCI. I dispositivi con sovrimpressione video e audio waveform riconoscono questo comando. Anche se i dispositivi video digitali e i sequencer MIDI riconoscono anche questo comando, i driver MCIAVI e MCISEQ non lo supportano.

Per inviare questo comando, chiamare la [**funzione mciSendString**](/previous-versions//dd757161(v=vs.85)) con il parametro *lpszCommand* impostato come segue.

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

Identificatore di un dispositivo MCI. Questo identificatore o alias viene assegnato all'apertura del dispositivo.

</dd> <dt>

<span id="lpszFilename"></span><span id="lpszfilename"></span><span id="LPSZFILENAME"></span>*lpszFilename*
</dt> <dd>

Flag che specifica il nome del file da salvare e, facoltativamente, flag aggiuntivi che modificano l'operazione di salvataggio. La tabella seguente elenca i tipi di dispositivo che **riconoscono il comando di** salvataggio e i flag usati da ogni tipo.



| Valore        | Significato              | Significato               |
|--------------|----------------------|-----------------------|
| digitalvideo | interruzione in corrispondenza del *rettangolo* | *nome file* keepreserve |
| overlay      | at *rectangle*       | *Filename*            |
| sequencer    | *Filename*           |                       |
| Waveaudio    | *Filename*           |                       |



 

La tabella seguente elenca i flag che possono essere specificati nel **parametro lpszFilename** e i relativi significati.



| Valore          | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abort          | Arresta **un'operazione** di salvataggio in corso. Se usato, deve essere l'unico elemento presente.                                                                                                                                                                                                                                                                                                                                                                                                                 |
| at *rectangle* | Specifica un rettangolo relativo all'origine del buffer dei frame. Il *rettangolo* viene specificato *come X1 Y1 X2 Y2*. Le coordinate *X1 Y1* specificano l'angolo superiore sinistro e le coordinate *X2 Y2* specificano la larghezza e l'altezza. Per i dispositivi video digitali, il [comando di](capture.md) acquisizione viene usato per acquisire il contenuto del buffer dei fotogrammi.<br/>                                                                                                                                               |
| *Filename*     | Specifica il nome file da assegnare al file di dati. Se non viene specificato un percorso, il file verrà inserito sul disco e nella directory specificata in precedenza nel comando di riserva esplicito [o](reserve.md) implicito. Se **la prenotazione** non è stata rilasciata, l'unità e la directory predefinite sono quelle associate all'attività dell'applicazione. Se viene specificato un percorso, il dispositivo potrebbe richiederlo nell'unità disco specificata dall'oggetto di riserva esplicita o **implicita.** Questo flag è obbligatorio. |
| keepreserve    | Specifica che lo spazio su disco inutilizzato rimanente dal comando **di** riserva originale non viene deallocato.                                                                                                                                                                                                                                                                                                                                                                                                 |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Può essere "wait", "notify" o entrambi. Per i dispositivi video digitali e VCR, è anche possibile specificare "test". Per altre informazioni su questi flag, vedere [Wait, Notify e Test Flags.](the-wait-notify-and-test-flags.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore in caso contrario.

## <a name="remarks"></a>Commenti

La *variabile filename* è obbligatoria se il dispositivo è stato aperto usando l'identificatore di dispositivo "nuovo".

## <a name="examples"></a>Esempio

Il comando seguente salva l'intero buffer video in un file denominato VCAPFILE. Tga.

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

[Mci](mci.md)
</dt> <dt>

[Stringhe di comando MCI](mci-command-strings.md)
</dt> <dt>

[Catturare](capture.md)
</dt> <dt>

[Riserva](reserve.md)
</dt> </dl>

 

