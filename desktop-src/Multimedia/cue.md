---
title: CUE (comando)
description: Il comando CUE si prepara per la riproduzione o la registrazione. Digital-video, VCR e waveform-i dispositivi audio riconoscono questo comando.
ms.assetid: 94fa0d0c-d5c9-4ef1-bb7d-22dfb09a7689
keywords:
- Cue Command Windows Multimedia
topic_type:
- apiref
api_name:
- cue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1dd71f06a71c8aff4752fc31d750a3612564eb8a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874638"
---
# <a name="cue-command"></a>CUE (comando)

Il comando CUE si prepara per la riproduzione o la registrazione. Digital-video, VCR e waveform-i dispositivi audio riconoscono questo comando.

Per inviare questo comando, chiamare la funzione [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con il set di parametri *lpszCommand* come indicato di seguito.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("cue %s %s %s"), 
  lpszDeviceID, 
  lpszInOutTo, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificatore di un dispositivo MCI. Questo identificatore o alias viene assegnato quando il dispositivo viene aperto.

</dd> <dt>

<span id="lpszInOutTo"></span><span id="lpszinoutto"></span><span id="LPSZINOUTTO"></span>*lpszInOutTo*
</dt> <dd>

Flag che prepara un dispositivo per la riproduzione o la registrazione. Nella tabella seguente sono elencati i tipi di dispositivo che riconoscono il comando **cue** e i flag utilizzati da ogni tipo.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Valore</th>
<th>Segnale</th>
<th>Segnale</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>digitalvideo</td>
<td><ul>
<li>input</li>
<li>noshow</li>
</ul></td>
<td><ul>
<li>output</li>
<li><em>posizione</em></li>
</ul></td>
</tr>
<tr class="even">
<td>VCR</td>
<td><ul>
<li>dalla <em>posizione</em></li>
<li>input</li>
<li>output</li>
</ul></td>
<td><ul>
<li>preroll</li>
<li>reverse</li>
<li><em>posizione</em></li>
</ul></td>
</tr>
<tr class="odd">
<td>WaveAudio</td>
<td>input</td>
<td>output</td>
</tr>
</tbody>
</table>



 

Nella tabella seguente sono elencati i flag che è possibile specificare nel parametro *lpszInOutTo* e i relativi significati.



| Valore           | Significato                                                                                                                                                                                                                                                                                                        |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| dalla *posizione* | Indica dove iniziare.                                                                                                                                                                                                                                                                                      |
| input           | Prepara la registrazione. Per i dispositivi video digitali, questo flag può essere omesso se l'origine della presentazione corrente è già l'input esterno.                                                                                                                                                                  |
| noshow          | Prepara la riproduzione di un frame senza visualizzarlo. Quando questo flag viene specificato, la visualizzazione continua a mostrare l'immagine nel buffer del frame anche se il frame corrispondente non è la posizione corrente. Un comando cue successivo senza questo flag e senza il flag "to" Visualizza il frame corrente. |
| output          | Prepara per la riproduzione. Se non si specifica né "input" né "output", l'impostazione predefinita è "output".                                                                                                                                                                                                           |
| preroll         | Sposta la distanza di preroll dal *punto di partenza*. Il punto è la posizione corrente o la posizione specificata dal flag "from".                                                                                                                                                                            |
| reverse         | Indica che la direzione della riproduzione è in ordine inverso (indietro).                                                                                                                                                                                                                                                             |
| *posizione*   | Sposta l'area di lavoro nella posizione specificata. Per i dispositivi VCR, questo flag indica dove arrestare.                                                                                                                                                                                                             |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Può essere "Wait", "notify" o entrambi. Per i dispositivi digitali video e VCR è possibile specificare anche "test". Per ulteriori informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore.

## <a name="remarks"></a>Commenti

Sebbene non sia necessario, l'invio del comando cue prima della riproduzione o della registrazione su alcuni dispositivi potrebbe ridurre il ritardo prima che il dispositivo avvii l'azione.

Questo comando ha esito negativo se la riproduzione o la registrazione è in corso o se il dispositivo è sospeso.

Quando si avvia la riproduzione (usando la cue "output"), l'invio del comando [Play](play.md) con il flag "from", "to" o "Reverse" Annulla il comando cue.

Quando si esegue il ripasso per la registrazione (tramite cue "input"), l'invio del comando [record](record.md) con il flag "from", "to" o "Initialize" Annulla il comando cue.

## <a name="examples"></a>Esempio

Il comando seguente prepara il dispositivo "audio" per la registrazione.

``` syntax
cue mysound input
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

[Play](play.md)
</dt> <dt>

[record](record.md)
</dt> </dl>

 

