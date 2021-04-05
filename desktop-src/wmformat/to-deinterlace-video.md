---
title: Per deinterlacciare il video
description: Per deinterlacciare il video
ms.assetid: 60e6af09-fde1-4e4a-b54c-4923c0549b6b
keywords:
- Windows Media Format SDK, Video deinterlacciato
- Windows Media Format SDK, telecine inversa
- Windows Media Format SDK, telecine
- ASF (Advanced Systems Format), Video deinterlacciato
- ASF (Advanced Systems Format), Video deinterlacciato
- ASF (Advanced Systems Format), telecine inversa
- ASF (formato avanzato dei sistemi), telecine inversa
- Formato di sistemi avanzati (ASF), telecine
- ASF (formato avanzato dei sistemi), telecine
- Video deinterlacciato
- Telecine inversa, informazioni
- telecine, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 580b8425e5807fefdfa889fcd08deedb4143cf39
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104046322"
---
# <a name="to-deinterlace-video"></a>Per deinterlacciare il video

Alcune origini di video, ad esempio schede di acquisizione video, forniscono dati video per la visualizzazione interlacciata. Ogni frame di video interlacciato è costituito da due campi. Il campo superiore contiene la prima riga di video e ogni altra riga successiva. Il campo inferiore contiene la seconda riga di video e ogni altra riga successiva. Un campo contiene quindi tutte le righe numerate pari e l'altra contiene tutte le righe numerate dispari. I campi che costituiscono un frame rappresentano tempi di presentazione leggermente diversi, in modo che, in caso di interfoliazione, non formino un'immagine statica.

Quando si desidera visualizzare il video in un monitor del computer, ogni frame del video deve essere visualizzato come un'immagine (questo metodo di visualizzazione di un intero frame alla volta è denominato video *progressivo* ). Se si visualizza progressivamente il video interlacciato, i frame potrebbero non essere corretti, a causa della differenza di tempo tra i due campi. Il codec Windows Media Video e il codec del profilo avanzato Windows Media Video supportano entrambe una funzionalità di pre-elaborazione che converte il contenuto interlacciato in frame progressivi.

Per avere il video di input deinterlacciamento codec, chiamare il metodo [**IWMWriterAdvanced2:: SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting) . L'impostazione da usare è g \_ wszDeinterlaceMode. Impostare la modalità di deinterlacciamento su uno dei valori seguenti.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Valore</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WM_DM_NOTINTERLACED</td>
<td>L'input è progressivo. Usare questa impostazione per arrestare il deinterlacciamento se in precedenza è stata impostata la modalità di deinterlacciamento su un altro valore.</td>
</tr>
<tr class="even">
<td>WM_DM_DEINTERLACE_NORMAL</td>
<td>Selezionare questa modalità per combinare i campi pari e dispari di un frame interlacciato (usando un meccanismo di compensazione movimento). Vantaggi<br/>
<ul>
<li>Gli artefatti di interlacciamento della visualizzazione progressiva sono notevolmente ridotti.</li>
<li>Il codec Windows Media Video produce video compressi di qualità superiore.</li>
</ul></td>
</tr>
<tr class="odd">
<td>WM_DM_DEINTERLACE_HALFSIZE</td>
<td>Selezionare questa modalità quando la risoluzione dell'output è metà o minore della risoluzione di input. Usare, ad esempio, questa modalità quando la risoluzione del video di input è 640 x 480 pixel e la risoluzione del video di output è 320 x 240 pixel. Vantaggi<br/>
<ul>
<li>Gli artefatti di interlacciamento della visualizzazione progressiva sono notevolmente ridotti.</li>
</ul></td>
</tr>
<tr class="even">
<td>WM_DM_DEINTERLACE_HALFSIZEDOUBLERATE</td>
<td>Selezionare questa modalità quando la risoluzione dell'output è metà o minore della risoluzione di input e la frequenza dei <a href="wmformat-glossary.md"><em>fotogrammi</em></a> di output è due volte superiore. Usare, ad esempio, questa modalità quando la risoluzione del video di input è 640 x 480 pixel a 30 frame interlacciati/sec e la risoluzione del video di output è 320 x 240 pixel a 60 frame/sec. Vantaggi<br/>
<ul>
<li>Questo produce frame progressivi di elevata qualità, perché ogni campo viene convertito in un frame e pertanto non è necessario combinare alcuna informazione.</li>
<li>Viene acquisito il movimento completo dei campi interlacciati.</li>
</ul></td>
</tr>
<tr class="odd">
<td>WM_DM_DEINTERLACE_INVERSETELECINE</td>
<td>Selezionare questa modalità per convertire il video di 30 fotogrammi/sec telecine in 24 fotogrammi al secondo della pellicola originale. Vantaggi<br/>
<ul>
<li>La qualità della compressione migliora significativamente perché solo 24 frame al secondo anziché 30 fotogrammi/sec devono essere codificati.</li>
<li>Poiché il risultato è progressivo, vengono realizzati gli stessi vantaggi di compressione e visualizzazione della deinterlacciamento.</li>
</ul></td>
</tr>
<tr class="even">
<td>WM_DM_DEINTERLACE_VERTICALHALFSIZEDOUBLERATE</td>
<td>Selezionare questa modalità quando la risoluzione dell'output verticale è metà o minore della risoluzione verticale di input e la frequenza dei <a href="wmformat-glossary.md"><em>fotogrammi</em></a> di output è due volte superiore. Ad esempio, la risoluzione video verticale di input è 640 x 480 pixel a 30 fotogrammi interlacciati/sec e la risoluzione video verticale di output è 320 x 240 pixel a 60 frame/sec. Vantaggi<br/>
<ul>
<li>Questo produce frame progressivi di elevata qualità, perché ogni campo viene convertito in un frame e pertanto non è necessario combinare alcuna informazione.</li>
<li>Viene acquisito il movimento completo dei campi interlacciati.</li>
</ul></td>
</tr>
</tbody>
</table>



 

Per il contenuto misto, impostare la modalità di deinterlacciamento in base alle esigenze prima di passare campioni di un nuovo tipo. Ad esempio, per avviare la codifica con input progressivo, non è necessario impostare alcuna modalità di deinterlacciamento. Se alcuni esempi richiedono il normale deinterlacciamento, è necessario impostare la modalità di deinterlacciamento su WM \_ DM \_ Deinterlaccia \_ Normal. Per elaborare gli esempi progressivi aggiuntivi è necessario impostare la modalità di deinterlacciamento su WM \_ DM \_ NOTINTERLACED.

## <a name="inverse-telecine-settings"></a>Impostazioni di telecine inverse

Per una descrizione della telecine, vedere [per usare la telecine inversa](to-use-inverse-telecine.md).

Se si imposta la modalità di deinterlacciamento su WM \_ DM \_ Deinterlaccia \_ INVERSETELECINE, è possibile specificare il modello di telecine del primo frame di input chiamando [**IWMWriterAdvanced2:: SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting). L'impostazione da usare è g \_ wszInitialPatternForInverseTelecine. Impostare il criterio iniziale su uno dei valori seguenti.



| Valore                                              | Descrizione                                                                                                                                                                                                                                                                                                   |
|----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WM \_ DM \_ \_ Disabilita la \_ \_ modalità coerente                | Specifica che i supporti di input sono passati attraverso il processo di telecine, ma che i frame non sono più in uno schema stimabile. Questo in genere indica che il supporto è stato modificato dopo l'elaborazione del telecine. Quando si usa questa impostazione, il codec tenta di ricostruire i frame originali in modo autonomo. |
| WM \_ DM \_ it \_ First \_ frame \_ in \_ clip \_ è \_ AA \_ Top    | Specifica che il campo superiore del frame AA è il primo campione.                                                                                                                                                                                                                                             |
| il \_ \_ \_ primo frame di WM DM it \_ \_ nel \_ clip \_ è \_ BB \_ Top    | Specifica che il campo superiore del fotogramma BB è il primo campione.                                                                                                                                                                                                                                             |
| WM \_ DM \_ it \_ First \_ frame \_ in \_ clip \_ è \_ BC \_ Top    | Specifica che il campo superiore del frame BC è il primo campione.                                                                                                                                                                                                                                             |
| WM \_ DM \_ it \_ First \_ frame \_ in \_ clip \_ è un \_ CD- \_ Top    | Specifica che il campo superiore del fotogramma CD è il primo esempio.                                                                                                                                                                                                                                             |
| il \_ \_ \_ primo frame di WM DM it \_ \_ nel \_ clip \_ è \_ DD \_ Top    | Specifica che il campo superiore del frame DD è il primo campione.                                                                                                                                                                                                                                             |
| WM \_ DM \_ il \_ primo \_ frame \_ nel \_ clip \_ è \_ AA \_ inferiore | Specifica che il campo inferiore del frame AA è il primo campione.                                                                                                                                                                                                                                          |
| il \_ \_ \_ primo frame di WM DM it \_ \_ nel \_ clip \_ è BB in \_ \_ basso | Specifica che il campo inferiore del frame BB è il primo campione.                                                                                                                                                                                                                                          |
| il \_ \_ \_ primo frame di WM DM it \_ \_ nel \_ clip \_ è \_ BC \_ Bottom | Specifica che il campo inferiore del frame BC è il primo campione.                                                                                                                                                                                                                                          |
| WM \_ DM \_ it \_ First \_ frame \_ in \_ clip \_ è un \_ CD \_ inferiore | Specifica che il campo inferiore del fotogramma CD è il primo esempio.                                                                                                                                                                                                                                          |
| il \_ \_ \_ primo frame di WM DM it \_ \_ nel \_ clip \_ è \_ DD \_ inferiore | Specifica che il campo inferiore del frame DD è il primo campione.                                                                                                                                                                                                                                          |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Argomenti avanzati**](advanced-topics.md)
</dt> </dl>

 

 





