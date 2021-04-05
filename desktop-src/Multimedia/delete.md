---
title: comando Delete
description: Il comando Delete Elimina un segmento di dati da un file. Digital-video e waveform-i dispositivi audio riconoscono questo comando.
ms.assetid: 9cf084f6-d64e-4487-9407-b68502b7cec9
keywords:
- Elimina il comando Windows Multimedia
topic_type:
- apiref
api_name:
- delete
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e356d4972384e676f2e521bd2ca102bb21d7ef2c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874458"
---
# <a name="delete-command"></a>comando Delete

Il comando Delete Elimina un segmento di dati da un file. Digital-video e waveform-i dispositivi audio riconoscono questo comando.

Per inviare questo comando, chiamare la funzione [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con il set di parametri *lpszCommand* come indicato di seguito.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("delete %s %s %s"), 
  lpszDeviceID, 
  lpszPosition, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificatore di un dispositivo MCI. Questo identificatore o alias viene assegnato quando il dispositivo viene aperto.

</dd> <dt>

<span id="lpszPosition"></span><span id="lpszposition"></span><span id="LPSZPOSITION"></span>*lpszPosition*
</dt> <dd>

Flag che identifica un segmento di dati da eliminare. Nella tabella seguente sono elencati i tipi di dispositivo che riconoscono il comando **Delete** e i flag utilizzati da ogni tipo.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Valore</th>
<th>Significato</th>
<th>Significato</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>digitalvideo</td>
<td><ul>
<li>al <em>rettangolo</em></li>
<li><em>flusso</em> del flusso audio</li>
<li>dalla <em>posizione</em></li>
</ul></td>
<td><ul>
<li><em>posizione</em></li>
<li><em>flusso</em> del flusso video</li>
</ul></td>
</tr>
<tr class="even">
<td>WaveAudio</td>
<td>dalla <em>posizione</em></td>
<td><em>posizione</em></td>
</tr>
</tbody>
</table>



 

Nella tabella seguente sono elencati i flag che è possibile specificare nel parametro *lpszPosition* e i relativi significati.



| Valore                 | Significato                                                                                                                                                                                                                                      |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| al *rettangolo*        | Specifica la parte di ogni frame eliminata. Se omesso, il valore predefinito è l'intero frame. Quando si specifica questo elemento, i frame non vengono eliminati. L'area all'interno del rettangolo diventa invece nero.                                          |
| *flusso* del flusso audio | Specifica il flusso audio nell'area di lavoro interessata dal comando. Se si usa questo flag e si vuole anche eliminare il video, è necessario usare anche il flag "flusso video". Se non viene specificato alcun flag, vengono eliminati tutti i flussi audio e video. |
| dalla *posizione*       | Specifica la posizione di inizio dell'eliminazione. Se questo flag viene omesso, l'eliminazione inizia in corrispondenza della posizione corrente.                                                                                                                       |
| *posizione*         | Specifica la posizione in cui termina l'eliminazione. Se questo flag viene omesso, l'eliminazione continua fino alla fine del contenuto o dell'area di lavoro.                                                                                                       |
| *flusso* del flusso video | Specifica il flusso video nell'area di lavoro interessata dal comando. Se si utilizza questo flag e si desidera eliminare anche audio, è necessario utilizzare anche il flag "flusso audio". Se non viene specificato alcun flag, vengono eliminati tutti i flussi audio e video.     |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Può essere "Wait", "notify" o entrambi. Per i dispositivi digitali video e VCR è possibile specificare anche "test". Per ulteriori informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore.

## <a name="remarks"></a>Commenti

Prima di emettere i comandi che usano i valori di posizione, è necessario impostare il formato di ora desiderato usando il comando [set](set.md) .

## <a name="examples"></a>Esempio

Il comando seguente elimina i dati audio della forma d'onda da 1 millisecondo a 900 millisecondi (presupponendo che il formato dell'ora sia impostato su millisecondi).

``` syntax
delete mysound from 1 to 900
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

[set](set.md)
</dt> </dl>

 

