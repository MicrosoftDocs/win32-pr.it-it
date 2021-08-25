---
title: comando cue
description: Il comando cue si prepara per la riproduzione o la registrazione. I dispositivi digital-video, VCR e waveform-audio riconoscono questo comando.
ms.assetid: 94fa0d0c-d5c9-4ef1-bb7d-22dfb09a7689
keywords:
- Comando cue Windows Multimedia
topic_type:
- apiref
api_name:
- cue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d14b9445de1736f563a33e44f1e4524f9c0c280e7e274f6b010b9b45a61714ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119785441"
---
# <a name="cue-command"></a>comando cue

Il comando cue si prepara per la riproduzione o la registrazione. I dispositivi digital-video, VCR e waveform-audio riconoscono questo comando.

Per inviare questo comando, chiamare la [**funzione mciSendString**](/previous-versions//dd757161(v=vs.85)) con il parametro *lpszCommand* impostato come indicato di seguito.

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

Identificatore di un dispositivo MCI. Questo identificatore o alias viene assegnato all'apertura del dispositivo.

</dd> <dt>

<span id="lpszInOutTo"></span><span id="lpszinoutto"></span><span id="LPSZINOUTTO"></span>*lpszInOutTo*
</dt> <dd>

Flag che prepara un dispositivo per la riproduzione o la registrazione. Nella tabella seguente sono elencati i tipi di dispositivo che riconoscono il **comando cue** e i flag usati da ogni tipo.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Valore</th>
<th>segnale</th>
<th>segnale</th>
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
<li>alla <em>posizione</em></li>
</ul></td>
</tr>
<tr class="even">
<td>Vcr</td>
<td><ul>
<li>dalla <em>posizione</em></li>
<li>input</li>
<li>output</li>
</ul></td>
<td><ul>
<li>Preroll</li>
<li>reverse</li>
<li>alla <em>posizione</em></li>
</ul></td>
</tr>
<tr class="odd">
<td>Waveaudio</td>
<td>input</td>
<td>output</td>
</tr>
</tbody>
</table>



 

Nella tabella seguente sono elencati i flag che è possibile specificare nel parametro *lpszInOutTo* e i relativi significati.



| Valore           | Significato                                                                                                                                                                                                                                                                                                        |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| dalla *posizione* | Indica la posizione di inizio.                                                                                                                                                                                                                                                                                      |
| input           | Si prepara per la registrazione. Per i dispositivi digital-video, questo flag può essere omesso se l'origine di presentazione corrente è già l'input esterno.                                                                                                                                                                  |
| noshow          | Si prepara per la riproduzione di un frame senza visualizzarlo. Quando si specifica questo flag, la visualizzazione continua a visualizzare l'immagine nel buffer dei frame anche se il frame corrispondente non è la posizione corrente. Un comando cue successivo senza questo flag e senza il flag "to" visualizza il frame corrente. |
| output          | Si prepara per la riproduzione. Se non vengono specificati né "input" né "output", l'impostazione predefinita è "output".                                                                                                                                                                                                           |
| Preroll         | Sposta la distanza di preroll *dall'oggetto nel punto*. Il punto in è la posizione corrente o la posizione specificata dal flag "da".                                                                                                                                                                            |
| reverse         | Indica che la direzione di riproduzione è inversa (indietro).                                                                                                                                                                                                                                                             |
| alla *posizione*   | Sposta l'area di lavoro nella posizione specificata. Per i dispositivi vcr, questo flag indica dove arrestare.                                                                                                                                                                                                             |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Può essere "wait", "notify" o entrambi. Per i dispositivi digital-video e VCR, è anche possibile specificare "test". Per altre informazioni su questi flag, vedere [Flag di attesa, notifica e test](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore in caso contrario.

## <a name="remarks"></a>Commenti

Anche se non è necessario, l'emissione del comando cue prima della riproduzione o della registrazione in alcuni dispositivi potrebbe ridurre il ritardo prima che il dispositivo inizi l'azione.

Questo comando ha esito negativo se la riproduzione o la registrazione è in corso o se il dispositivo è sospeso.

Quando si segnala la riproduzione (usando il segnale "output"), l'emissione del comando di riproduzione con il flag "from", "to" o "reverse" annulla il comando cue. [](play.md)

Quando si segnala la registrazione (usando il segnale "input"), l'emissione del comando [di record](record.md) con il flag "from", "to" o "initialize" annulla il comando cue.

## <a name="examples"></a>Esempio

Il comando seguente prepara il dispositivo "mysound" per la registrazione.

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

[Mci](mci.md)
</dt> <dt>

[Stringhe di comando MCI](mci-command-strings.md)
</dt> <dt>

[Giocare](play.md)
</dt> <dt>

[Registrazione](record.md)
</dt> </dl>

 

