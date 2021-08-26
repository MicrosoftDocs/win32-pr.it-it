---
description: Illustra come usare l'elaborazione video DXVA.
ms.assetid: 1465bd41-94f9-4e19-8236-00e7a2d6f54a
title: DXVA2_VideoProc esempio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8fc4be1bad6a3955af255cb083a4595ecedfd30
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473927"
---
# <a name="dxva2_videoproc-sample"></a>Esempio \_ videoproc DXVA2

Illustra come usare [l'elaborazione video DXVA.](dxva-video-processing.md)

Questo esempio genera video a livello di codice con un flusso primario e un flusso secondario. Il flusso principale visualizza le barre dei colori SMPTE e il flusso secondario è un rettangolo semitrasparente. Il video viene quindi elaborato e visualizzato usando un processore video DXVA. L'utente può modificare i valori alfa planari, i rettangoli di origine e di destinazione, le regolazioni dei colori e lo spazio colore.

![screenshot dell'esempio videoproc dxva2 \-](images/dxva2-videoproc.png)

## <a name="apis-demonstrated"></a>DIMOSTRAZIONE DELLE API

In questo esempio vengono illustrate le interfacce DXVA seguenti:

-   [**IDirectXVideoProcessorService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessorservice)
-   [**IDirectXVideoProcessor**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessor)

## <a name="usage"></a>Utilizzo

L'esempio VideoProc DXVA2 \_ compila un'Windows applicazione.

Opzioni della riga di comando:



| Opzione | Descrizione                                                                          |
|--------|--------------------------------------------------------------------------------------|
| -hh    | Forza l'applicazione a usare un dispositivo Direct3D hardware e un dispositivo DXVA hardware. |
| -hs    | Forza l'applicazione a usare un dispositivo Direct3D hardware e un dispositivo DXVA software. |
| -ss    | Forza l'applicazione a usare un dispositivo Direct3D software e un dispositivo DXVA software. |



 

Comandi da tastiera:



| Chiave       | Descrizione                                             |
|-----------|---------------------------------------------------------|
| ALT+INVIO | Passare dalla modalità finestra alla modalità schermo intero e dalla modalità a schermo intero.      |
| F1-F8     | Immettere una delle modalità illustrate nella tabella seguente.    |
| FINE       | Abilitare o disabilitare la registrazione di debug per i frame eliminati. |
| HOME      | Reimpostare un parametro sul valore iniziale.                 |



 

Ognuno dei tasti funzione da F1 a F8 passa a una modalità in cui i tasti di direzione possono essere usati per modificare un determinato parametro di rendering. Inoltre, il colore del flusso secondario cambia.




| Chiave | Descrizione | 
|-----|-------------|
| F1 | Modificare i valori alfa.<br /><ul><li>UP: aumenta il valore alfa planare di entrambi i flussi.</li><li>DOWN: riduce il valore alfa planare di entrambi i flussi.</li><li>RIGHT: aumenta il pixel alfa del flusso secondario.</li><li>LEFT: riduce il pixel alfa del flusso secondario.</li></ul>Colore del flusso secondario: bianco<br /> | 
| F2 | Regolare l'area di origine del flusso primario (zoom).<br /><ul><li>SU: aumenta verticalmente (zoom avanti).</li><li>DOWN: consente di ridurre verticalmente (zoom indietro).</li><li>RIGHT: aumenta orizzontalmente (zoom avanti).</li><li>LEFT: consente di ridurre orizzontalmente (zoom indietro).</li></ul>Colore del flusso secondario: rosso<br /> | 
| F3 | Spostare l'area di origine del flusso primario.<br /><ul><li>UP: sposta verso l'alto.</li><li>DOWN: consente di spostarsi verso il basso.</li><li>RIGHT: sposta a destra.</li><li>LEFT: sposta a sinistra.</li></ul>Colore del flusso secondario: giallo<br /> | 
| F4 | Modificare l'area di destinazione del flusso primario.<br /><ul><li>UP: aumenta verticalmente.</li><li>DOWN: consente di ridurre verticalmente.</li><li>RIGHT: aumenta orizzontalmente.</li><li>LEFT: consente di ridurre orizzontalmente.</li></ul>Colore del flusso secondario: verde<br /> | 
| F5 | Spostare l'area di destinazione del flusso primario.<br /><ul><li>UP: sposta verso l'alto.</li><li>DOWN: consente di spostarsi verso il basso.</li><li>RIGHT: sposta a destra.</li><li>LEFT: sposta a sinistra.</li></ul>Colore del flusso secondario: ciano<br /> | 
| F6 | Modificare il colore di sfondo o lo spazio colore.<br /><ul><li>SU, GIÙ: consente di scorrere gli spazi colori.</li><li>RIGHT, LEFT: consente di scorrere i colori di sfondo.</li></ul>Colore del flusso secondario: blu<br /> | 
| F7 | Regolare luminosità e contrasto.<br /><ul><li>UP: aumentare la luminosità.</li><li>DOWN: diminuisce la luminosità.</li><li>RIGHT: aumenta il contrasto.</li><li>LEFT: consente di ridurre il contrasto.</li></ul>Colore del flusso secondario: Magenta<br /> | 
| F8 | Regolare la tonalità e la saturazione.<br /><ul><li>UP: aumenta la tonalità.</li><li>DOWN: consente di ridurre la tonalità.</li><li>RIGHT: aumentare la saturazione.</li><li>LEFT: riduce la saturazione.</li></ul>Colore del flusso secondario: Nero<br /> | 




 

In ogni modalità, premendo HOME i parametri per tale modalità vengono reimpostati sui valori iniziali.

## <a name="requirements"></a>Requisiti



| Prodotto                                                        | Versione   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |



 

## <a name="downloading-the-sample"></a>Download dell'esempio

Questo esempio è disponibile nel repository [github Windows esempi classici](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/evrpresenter).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Accelerazione video DirectX 2.0](directx-video-acceleration-2-0.md)
</dt> <dt>

[Elaborazione video DXVA](dxva-video-processing.md)
</dt> <dt>

[Esempi di Media Foundation SDK](media-foundation-sdk-samples.md)
</dt> </dl>

 

 




