---
title: comando Capability
description: Il comando Capability richiede informazioni su una particolare funzionalità di un dispositivo. Tutti i dispositivi MCI riconoscono questo comando.
ms.assetid: 1b470473-0de6-41ba-9f6e-41f0b13ceaeb
keywords:
- funzionalità di Windows Multimedia Command
topic_type:
- apiref
api_name:
- capability
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a6ac87b98fb8d748a5baf2665cc5a63230b6a98
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475707"
---
# <a name="capability-command"></a>comando Capability

Il comando Capability richiede informazioni su una particolare funzionalità di un dispositivo. Tutti i dispositivi MCI riconoscono questo comando.

Per inviare questo comando, chiamare la funzione [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con il set di parametri *lpszCommand* come indicato di seguito.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("capability %s %s %s"), 
  lpszDeviceID, 
  lpszRequest, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificatore di un dispositivo MCI. Questo identificatore o alias viene assegnato quando il dispositivo viene aperto.

</dd> <dt>

<span id="lpszRequest"></span><span id="lpszrequest"></span><span id="LPSZREQUEST"></span>*lpszRequest*
</dt> <dd>

Flag che identifica una funzionalità del dispositivo. Nella tabella seguente sono elencati i tipi di dispositivo che riconoscono il comando **Capability** e i flag utilizzati da ogni tipo:



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Valore</th>
<th>Tipo</th>
<th>Tipo</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>cdaudio</td>
<td><ul>
<li>può espulsione</li>
<li>può riprodurre</li>
<li>può registrare</li>
<li>consente di salvare</li>
<li>dispositivo composto</li>
</ul></td>
<td><ul>
<li>tipo di dispositivo</li>
<li>con audio</li>
<li>con video</li>
<li>Usa file</li>
</ul></td>
</tr>
<tr class="even">
<td>digitalvideo</td>
<td><ul>
<li>può espulsione</li>
<li>può bloccare</li>
<li>può bloccare</li>
<li>può riprodurre</li>
<li>può registrare</li>
<li>può invertire</li>
<li>consente di salvare</li>
<li>può estendersi</li>
<li>è possibile estendere l'input</li>
<li>è possibile eseguire il test</li>
</ul></td>
<td><ul>
<li>dispositivo composto</li>
<li>tipo di dispositivo</li>
<li>con audio</li>
<li>ha ancora</li>
<li>con video</li>
<li>velocità di riproduzione massima</li>
<li>velocità di riproduzione minima</li>
<li>Usa file</li>
<li>USA tavolozze</li>
<li>windows</li>
</ul></td>
</tr>
<tr class="odd">
<td>overlay</td>
<td><ul>
<li>può espulsione</li>
<li>può bloccare</li>
<li>può riprodurre</li>
<li>può registrare</li>
<li>consente di salvare</li>
<li>può estendersi</li>
</ul></td>
<td><ul>
<li>dispositivo composto</li>
<li>tipo di dispositivo</li>
<li>con audio</li>
<li>con video</li>
<li>Usa file</li>
<li>windows</li>
</ul></td>
</tr>
<tr class="even">
<td>sequencer</td>
<td><ul>
<li>può espulsione</li>
<li>può riprodurre</li>
<li>può registrare</li>
<li>consente di salvare</li>
<li>dispositivo composto</li>
</ul></td>
<td><ul>
<li>tipo di dispositivo</li>
<li>con audio</li>
<li>con video</li>
<li>Usa file</li>
</ul></td>
</tr>
<tr class="odd">
<td>VCR</td>
<td><ul>
<li>può rilevare la lunghezza</li>
<li>può espulsione</li>
<li>può bloccare</li>
<li>consente di monitorare le origini</li>
<li>può riprodurre</li>
<li>è possibile preroll</li>
<li>anteprima</li>
<li>può registrare</li>
<li>può invertire</li>
<li>consente di salvare</li>
<li>è possibile eseguire il test</li>
</ul></td>
<td><ul>
<li>frequenza di incremento Clock</li>
<li>dispositivo composto</li>
<li>tipo di dispositivo</li>
<li>con audio</li>
<li>con clock</li>
<li>con timecode</li>
<li>con video</li>
<li>numero di contrassegni</li>
<li>accuratezza ricerca</li>
<li>Usa file</li>
</ul></td>
</tr>
<tr class="even">
<td>videodisco</td>
<td><ul>
<li>può espulsione</li>
<li>può riprodurre</li>
<li>può registrare</li>
<li>può invertire</li>
<li>consente di salvare</li>
<li>CAV</li>
<li>CLV</li>
<li>dispositivo composto</li>
</ul></td>
<td><ul>
<li>tipo di dispositivo</li>
<li>velocità di riproduzione veloce</li>
<li>con audio</li>
<li>con video</li>
<li>frequenza di riproduzione normale</li>
<li>velocità di riproduzione lenta</li>
<li>Usa file</li>
</ul></td>
</tr>
<tr class="odd">
<td>WaveAudio</td>
<td><ul>
<li>può espulsione</li>
<li>può riprodurre</li>
<li>può registrare</li>
<li>consente di salvare</li>
<li>dispositivo composto</li>
<li>tipo di dispositivo</li>
</ul></td>
<td><ul>
<li>con audio</li>
<li>con video</li>
<li>input</li>
<li>outputs</li>
<li>Usa file</li>
</ul></td>
</tr>
</tbody>
</table>



 

Nella tabella seguente sono elencati i flag che è possibile specificare nel parametro *lpszRequest* e i relativi significati:



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Flags</th>
<th>Significato</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>può rilevare la lunghezza</td>
<td>Restituisce <strong>true</strong> se il dispositivo è in grado di rilevare la lunghezza del supporto.</td>
</tr>
<tr class="even">
<td>può espulsione</td>
<td>Restituisce <strong>true</strong> se il dispositivo può espellere il supporto.</td>
</tr>
<tr class="odd">
<td>può bloccare</td>
<td>Restituisce <strong>true</strong> se il dispositivo può bloccare i dati nel buffer del frame.</td>
</tr>
<tr class="even">
<td>può bloccare</td>
<td>Restituisce <strong>true</strong> se il dispositivo può bloccare i dati.</td>
</tr>
<tr class="odd">
<td>consente di monitorare le origini</td>
<td>Restituisce <strong>true</strong> se il dispositivo può passare un input (origine) all'output monitorato, indipendentemente dalla selezione di input corrente.</td>
</tr>
<tr class="even">
<td>può riprodurre</td>
<td>Restituisce <strong>true</strong> se il dispositivo è in grado di riprodurre.</td>
</tr>
<tr class="odd">
<td>è possibile preroll</td>
<td>Restituisce <strong>true</strong> se il dispositivo supporta il &quot; flag preroll &quot; con il comando <a href="cue.md">cue</a> .</td>
</tr>
<tr class="even">
<td>anteprima</td>
<td>Restituisce <strong>true</strong> se il dispositivo supporta le anteprime.</td>
</tr>
<tr class="odd">
<td>può registrare</td>
<td>Restituisce <strong>true</strong> se il dispositivo supporta la registrazione.</td>
</tr>
<tr class="even">
<td>può invertire</td>
<td>Restituisce <strong>true</strong> se il dispositivo può essere riprodotto in senso inverso.</td>
</tr>
<tr class="odd">
<td>consente di salvare</td>
<td>Restituisce <strong>true</strong> se il dispositivo è in grado di salvare i dati.</td>
</tr>
<tr class="even">
<td>può estendersi</td>
<td>Restituisce <strong>true</strong> se il dispositivo può estendere i frame per riempire un rettangolo di visualizzazione specificato.</td>
</tr>
<tr class="odd">
<td>è possibile estendere l'input</td>
<td>Restituisce <strong>true</strong> se il dispositivo può ridimensionare un'immagine nel processo di digitalizzazione nel buffer del frame.</td>
</tr>
<tr class="even">
<td>è possibile eseguire il test</td>
<td>Restituisce <strong>true</strong> se il dispositivo riconosce la parola chiave di test.</td>
</tr>
<tr class="odd">
<td>CAV</td>
<td>In combinazione con altri elementi, questo flag specifica che le informazioni restituite si applicano al formato CAV videodischi. Si tratta dell'impostazione predefinita se non viene inserito alcun videodisco.</td>
</tr>
<tr class="even">
<td>frequenza di incremento Clock</td>
<td>Restituisce il numero di suddivisioni supportate dal clock esterno al secondo. Se il clock esterno è un clock in millisecondi, il valore restituito è 1000. Se il valore restituito è 0, non è supportato alcun clock.</td>
</tr>
<tr class="odd">
<td>clv</td>
<td>In combinazione con altri elementi, questo flag specifica che le informazioni restituite si applicano al formato CLV videodischi.</td>
</tr>
<tr class="even">
<td>dispositivo composto</td>
<td>Restituisce <strong>true</strong> se il dispositivo supporta il nome di un elemento (filename).</td>
</tr>
<tr class="odd">
<td>tipo di dispositivo</td>
<td>Restituisce un nome di tipo di dispositivo, che può essere uno dei seguenti:
<ul>
<li>cdaudio</li>
<li>dat</li>
<li>digitalvideo</li>
<li>altro</li>
<li>overlay</li>
<li>scanner</li>
<li>sequencer</li>
<li>VCR</li>
<li>videodisco</li>
<li>WaveAudio</li>
</ul></td>
</tr>
<tr class="even">
<td>velocità di riproduzione veloce</td>
<td>Restituisce la velocità di riproduzione rapida in frame al secondo oppure zero se il dispositivo non può essere riprodotto velocemente.</td>
</tr>
<tr class="odd">
<td>con audio</td>
<td>Restituisce <strong>true</strong> se il dispositivo supporta la riproduzione audio.</td>
</tr>
<tr class="even">
<td>con clock</td>
<td>Restituisce <strong>true</strong> se il dispositivo ha un clock.</td>
</tr>
<tr class="odd">
<td>ha ancora</td>
<td>Restituisce <strong>true</strong> se il dispositivo considera i file con una singola immagine in modo più efficiente rispetto ai file video di movimento.</td>
</tr>
<tr class="even">
<td>con timecode</td>
<td>Restituisce <strong>true</strong> se il dispositivo è in grado di supportare il codice temporale o se è sconosciuto.</td>
</tr>
<tr class="odd">
<td>con video</td>
<td>Restituisce <strong>true</strong> se il dispositivo supporta il video.</td>
</tr>
<tr class="even">
<td>input</td>
<td>Restituisce il numero totale di dispositivi di input.</td>
</tr>
<tr class="odd">
<td>velocità di riproduzione massima</td>
<td>Restituisce la velocità di riproduzione massima, in frame al secondo, per il dispositivo.</td>
</tr>
<tr class="even">
<td>velocità di riproduzione minima</td>
<td>Restituisce la velocità di riproduzione minima, in frame al secondo, per il dispositivo.</td>
</tr>
<tr class="odd">
<td>frequenza di riproduzione normale</td>
<td>Restituisce la frequenza di riproduzione normale, in frame al secondo, per il dispositivo.</td>
</tr>
<tr class="even">
<td>numero di contrassegni</td>
<td>Restituisce il numero massimo di contrassegni che è possibile utilizzare. zero indica che i contrassegni non sono supportati.</td>
</tr>
<tr class="odd">
<td>outputs</td>
<td>Restituisce il numero totale di dispositivi di output.</td>
</tr>
<tr class="even">
<td>accuratezza ricerca</td>
<td>Restituisce l'accuratezza prevista di una ricerca nei frame; 0 indica che il dispositivo è accurato per il frame, 1 indica che il dispositivo è previsto che si trovi all'interno di un frame della posizione di ricerca indicata e così via.</td>
</tr>
<tr class="odd">
<td>velocità di riproduzione lenta</td>
<td>Restituisce la velocità di riproduzione lenta in frame al secondo oppure zero se il dispositivo non può essere riprodotto lentamente.</td>
</tr>
<tr class="even">
<td>Usa file</td>
<td>Restituisce <strong>true</strong> se l'archivio dati utilizzato da un dispositivo composto è un file.</td>
</tr>
<tr class="odd">
<td>USA tavolozze</td>
<td>Restituisce <strong>true</strong> se il dispositivo utilizza tavolozze.</td>
</tr>
<tr class="even">
<td>windows</td>
<td>Restituisce il numero di finestre di visualizzazione simultanee che il dispositivo può supportare.</td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Può essere "Wait", "notify" o entrambi. Per i dispositivi digitali video e VCR è possibile specificare anche "test". Per ulteriori informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce le informazioni nel parametro *lpszReturnString* della funzione [**mciSendString**](/previous-versions//dd757161(v=vs.85)) . Le informazioni dipendono dal tipo di richiesta.

## <a name="examples"></a>Esempio

Il comando seguente restituisce il tipo di dispositivo del dispositivo "audio".

``` syntax
capability mysound device type
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

[segnale](cue.md)
</dt> </dl>

 

