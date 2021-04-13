---
description: Mostra come usare l'elaborazione video di DXVA.
ms.assetid: 1465bd41-94f9-4e19-8236-00e7a2d6f54a
title: Esempio DXVA2_VideoProc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8497a241baf07b76148a5bc2e7ddb4dd5e878e86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342496"
---
# <a name="dxva2_videoproc-sample"></a>\_Esempio DXVA2 VideoProc

Mostra come usare l' [elaborazione video di DXVA](dxva-video-processing.md).

Questo esempio genera video a livello di codice con un flusso primario e un sottoflusso. Il flusso primario Visualizza le barre dei colori SMPTE e il sottoflusso è un rettangolo semitrasparente. Il video viene quindi elaborato e visualizzato usando un processore video DXVA. L'utente può modificare i valori alfa planari, i rettangoli di origine e di destinazione, le regolazioni dei colori e lo spazio colore.

![screenshot dell'esempio dxva2 \- videoproc](images/dxva2-videoproc.png)

## <a name="apis-demonstrated"></a>API illustrate

In questo esempio vengono illustrate le interfacce DXVA seguenti:

-   [**IDirectXVideoProcessorService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessorservice)
-   [**IDirectXVideoProcessor**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessor)

## <a name="usage"></a>Utilizzo

L' \_ esempio DXVA2 VideoProc compila un'applicazione Windows.

Opzioni della riga di comando:



| Opzione | Descrizione                                                                          |
|--------|--------------------------------------------------------------------------------------|
| -HH    | Impone all'applicazione di usare un dispositivo Direct3D hardware e un dispositivo DXVA hardware. |
| -HS    | Impone all'applicazione di usare un dispositivo Direct3D hardware e un dispositivo DXVA software. |
| -ss    | Impone all'applicazione di usare un dispositivo Direct3D software e un dispositivo DXVA software. |



 

Comandi da tastiera:



| Chiave       | Descrizione                                             |
|-----------|---------------------------------------------------------|
| ALT+INVIO | Passa tra la modalità finestra e la modalità schermo intero.      |
| F1 – F8     | Immettere una delle modalità illustrate nella tabella seguente.    |
| FINE       | Abilita o Disabilita la registrazione del debug per i frame eliminati. |
| HOME      | Reimposta un parametro sul valore iniziale.                 |



 

Ogni tasto funzione da F1 a F8 passa a una modalità in cui è possibile usare i tasti di direzione per modificare un determinato parametro di rendering. Inoltre, il colore del sottoflusso cambia.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Chiave</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>F1</td>
<td>Modificare i valori alfa.<br/>
<ul>
<li>UP: aumenta l'alfa planare di entrambi i flussi.</li>
<li>DOWN: riduce l'alfa planare di entrambi i flussi.</li>
<li>RIGHT: aumentare il pixel alfa del sottoflusso.</li>
<li>LEFT: riduce il pixel alfa del sottoflusso.</li>
</ul>
Colore flusso substream: bianco<br/></td>
</tr>
<tr class="even">
<td>F2</td>
<td>Modificare l'area di origine del flusso primario (zoom).<br/>
<ul>
<li>UP: aumenta verticalmente (zoom avanti).</li>
<li>DOWN: riduzione verticale (zoom indietro).</li>
<li>RIGHT: aumenta orizzontalmente (zoom avanti).</li>
<li>LEFT: decrementa orizzontalmente (zoom indietro).</li>
</ul>
Colore flusso substream: rosso<br/></td>
</tr>
<tr class="odd">
<td>F3</td>
<td>Spostare l'area di origine del flusso primario.<br/>
<ul>
<li>SU: sposta su.</li>
<li>GIÙ: Sposta giù.</li>
<li>A destra: sposta a destra.</li>
<li>LEFT: sposta a sinistra.</li>
</ul>
Colore flusso substream: giallo<br/></td>
</tr>
<tr class="even">
<td>F4</td>
<td>Modificare l'area di destinazione del flusso primario.<br/>
<ul>
<li>UP: aumento verticale.</li>
<li>DOWN: riduzione verticale.</li>
<li>RIGHT: aumenta orizzontalmente.</li>
<li>LEFT: diminuisce orizzontalmente.</li>
</ul>
Colore flusso substream: verde<br/></td>
</tr>
<tr class="odd">
<td>F5</td>
<td>Spostare l'area di destinazione del flusso primario.<br/>
<ul>
<li>SU: sposta su.</li>
<li>GIÙ: Sposta giù.</li>
<li>A destra: sposta a destra.</li>
<li>LEFT: sposta a sinistra.</li>
</ul>
Colore flusso substream: ciano<br/></td>
</tr>
<tr class="even">
<td>F6</td>
<td>Modificare il colore di sfondo o lo spazio colore.<br/>
<ul>
<li>Verso l'alto, verso il basso: scorrere gli spazi dei colori.</li>
<li>RIGHT, LEFT: scorre i colori di sfondo.</li>
</ul>
Colore flusso substream: blu<br/></td>
</tr>
<tr class="odd">
<td>F7</td>
<td>Regolazione della luminosità e del contrasto.<br/>
<ul>
<li>UP: aumento della luminosità.</li>
<li>GIÙ: Diminuisci luminosità.</li>
<li>RIGHT: aumenta il contrasto.</li>
<li>LEFT: Riduci contrasto.</li>
</ul>
Colore flusso substream: Magenta<br/></td>
</tr>
<tr class="even">
<td>F8</td>
<td>Regolare la tonalità e la saturazione.<br/>
<ul>
<li>SU: aumenta tonalità.</li>
<li>GIÙ: Diminuisci tonalità.</li>
<li>RIGHT: aumenta la saturazione.</li>
<li>LEFT: riduzione della saturazione.</li>
</ul>
Colore sottoflusso: nero<br/></td>
</tr>
</tbody>
</table>



 

In ogni modalità la pressione del tasto HOME consente di reimpostare i parametri per tale modalità sui valori iniziali.

## <a name="requirements"></a>Requisiti



| Prodotto                                                        | Versione   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |



 

## <a name="downloading-the-sample"></a>Download dell'esempio

Questo esempio è disponibile nel [repository GitHub degli esempi classici di Windows](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/evrpresenter).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Accelerazione video DirectX 2,0](directx-video-acceleration-2-0.md)
</dt> <dt>

[Elaborazione video DXVA](dxva-video-processing.md)
</dt> <dt>

[Esempi di Media Foundation SDK](media-foundation-sdk-samples.md)
</dt> </dl>

 

 




