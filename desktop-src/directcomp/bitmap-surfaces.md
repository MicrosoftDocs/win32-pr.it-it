---
title: Oggetti bitmap
description: Questo argomento descrive i tipi di contenuto bitmap supportati da DirectComposition.
ms.assetid: BC32CF76-D5E4-4B25-AFD5-42E8DABFA0D0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c390778fef1ee7ad96c90a8b7706fa635f3615ff
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399654"
---
# <a name="bitmap-objects"></a>Oggetti bitmap

> [!NOTE]
> Per le app in Windows 10, è consigliabile usare le API Windows. UI. Composition anziché DirectComposition. Per altre informazioni, vedere [modernizzare l'app desktop usando il livello visivo](/windows/uwp/composition/visual-layer-in-desktop-apps).

Microsoft DirectComposition è un motore di composizione bitmap. Consente agli sviluppatori di applicazioni di combinare più bitmap e di modificarle in diversi modi per ottenere effetti visivi e animazioni interessanti in un'interfaccia utente dell'applicazione. Questo argomento descrive i tipi di contenuto bitmap supportati da DirectComposition.

-   [Contenuto bitmap](#bitmap-content)
    -   [Bitmap memoria video](#video-memory-bitmaps)
    -   [Bitmap finestra](#window-bitmaps)
    -   [Associazione di contenuto bitmap a un oggetto visivo](#associating-bitmap-content-with-a-visual)
    -   [Canale alfa](#alpha-channel)
-   [Argomenti correlati](#related-topics)

## <a name="bitmap-content"></a>Contenuto bitmap

Le applicazioni forniscono DirectComposition con il contenuto della bitmap per comporre e animare creando oggetti visivi e quindi impostando la [proprietà Content](basic-concepts.md) di tali oggetti. DirectComposition non offre alcun servizio di rasterizzazione. Per popolare le bitmap da comporre, un'applicazione deve usare altre librerie di rasterizzazione basate su software o con accelerazione hardware, ad esempio [Direct2D](../direct2d/direct2d-portal.md) o [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) . Dopo la composizione, DirectComposition passa il contenuto della bitmap composto a [Gestione finestre desktop (DWM)](/windows/desktop/dwm/dwm-overview) per il rendering sullo schermo.

**Tipi supportati di contenuto bitmap**   Microsoft DirectComposition supporta i tipi di bitmap seguenti:

-   [Bitmap memoria video](#video-memory-bitmaps)
-   [Bitmap finestra](#window-bitmaps)

### <a name="video-memory-bitmaps"></a>Bitmap memoria video

Una bitmap di memoria video viene rasterizzata nell'hardware usando i metodi Microsoft DirectX (incluso il modello di interoperabilità DX-to-GDI). È supportato da superfici condivise tra processi visibili all'applicazione chiamante e a DirectComposition. Una bitmap di memoria video non è soggetta a strappi perché l'applicazione può solo leggere dalle superfici da cui DirectComposition le trame.

### <a name="video-content"></a>Contenuto video

Le applicazioni possono usare DirectComposition per comporre fotogrammi video che usano catene di scambio senza finestra DirectX associate a una superficie DirectComposition. Concettualmente, DirectComposition considera il contenuto video come una sequenza di bitmap. DirectComposition non fornisce un mezzo per la presentazione di fotogrammi video.

DirectComposition supporta le catene di scambio senza finestra DirectX, ovvero le catene di scambio non associate a una particolare finestra, e consente a due diverse applicazioni di condividere le catene di scambio senza finestra tra i limiti dei processi. La condivisione di catene di scambio senza finestra consente scenari di video in cui la catena di scambio viene creata in un processo e viene utilizzata con DirectComposition in un secondo processo. Le catene di scambio senza finestra vengono create usando il metodo [**IDXGIFactory2:: CreateSwapChainForCompositionSurface**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcomposition) .

Per altre informazioni sulle catene di scambio DirectX, vedere [Panoramica di DXGI](/windows/desktop/direct3ddxgi/d3d10-graphics-programming-guide-dxgi).

### <a name="stereo-content"></a>Contenuto stereo

A livello concettuale, una catena di swap stereo è costituita da superfici di Microsoft DirectX Graphics Infrastructure (DXGI) che rappresentano i canali sinistro e destro per il contenuto 3D stereo. Quando viene usata una catena di scambio stereo come risorsa bitmap per un oggetto visivo, DirectComposition è in formato stereo. Tutto il contenuto non stereo (contenuto mono) viene considerato con il contenuto del canale sinistro e destro identico; ovvero, viene usato lo stesso contenuto bitmap per entrambi i canali. DirectComposition compone separatamente tutto il contenuto a sinistra e tutto il contenuto corretto. Se il dispositivo di visualizzazione non è compatibile con lo stereo, DirectComposition considera il canale stereo sinistro o destro (a seconda dell'applicazione) come contenuto mono e compone solo i dati per la risorsa bitmap.

DirectComposition non supporta la creazione o la manipolazione di contenuto stereo e non può alzare di livello una catena di scambio mono a una coppia stereo. Un'applicazione deve eseguire queste attività prima di presentare contenuto stereo DirectX a DirectComposition. Inoltre, un'applicazione deve fornire gli offset del canale sinistro e destro per la percezione della profondità; DirectComposition non è in grado di modificare gli offset del canale sinistro e destro per modificare la profondità percepita del contenuto stereo DirectX.

Il contenuto stereo DirectX viene composto e reso permanente in DWM quando è disponibile hardware idoneo per la funzionalità stereo.

### <a name="window-bitmaps"></a>Bitmap finestra

Una "bitmap della finestra" non è una bitmap reale, ma è un segnaposto che DirectComposition sostituisce in tempo reale con le rasterizzazioni delle finestre figlio o di primo livello a più livelli. Una bitmap della finestra è simile a un'anteprima di DWM, ad eccezione del fatto che un'anteprima può contenere contributi da molte finestre, ad esempio finestre non figlio di proprietà, mentre una bitmap della finestra DirectComposition è sempre una rappresentazione di una sola finestra e dei relativi elementi figlio.

Poiché DirectComposition ha accesso alle aree di reindirizzamento di tutte le finestre e di tutte le strutture ad albero visive, può riutilizzare il contenuto da una finestra in più alberi visivi. La finestra deve essere sovrapposta perché una finestra non sovrapposta non dispone di una superficie di reindirizzamento dedicata e, pertanto, la rasterizzazione non è sempre disponibile per DirectComposition.

Per utilizzare una bitmap della finestra, un'applicazione associa un oggetto visivo a un handle di finestra (HWND). Successivamente, DirectComposition ricompone l'oggetto visivo ogni volta che viene modificato il contenuto della finestra, anche quando il contenuto cambia in seguito a modifiche apportate alle strutture ad albero visuali associate alla finestra. In altre parole, come le anteprime di DWM, le bitmap della finestra DirectComposition sono "attive".

### <a name="associating-bitmap-content-with-a-visual"></a>Associazione di contenuto bitmap a un oggetto visivo

Per tutti e tre i tipi di bitmap, un'applicazione può associare la stessa bitmap a più oggetti visivi, il che significa che una singola allocazione di memoria può essere usata per visualizzare lo stesso contenuto più volte.

### <a name="alpha-channel"></a>Canale alfa

Tutte le bitmap hanno un formato di 32 bit per pixel (BPP), che include otto bit per la trasparenza per pixel. Tuttavia, un'applicazione può specificare la modalità di utilizzo del canale alfa da parte di DirectComposition. In particolare, DirectComposition è in grado di rispettare il canale alfa, oppure può ignorare completamente Alpha, nel qual caso la bitmap viene considerata completamente opaca.

Una modalità Alpha aggiuntiva ignora il canale alfa, ma considera i valori rosso, verde e blu come valori alfa per canale anziché l'interpretazione normale di tali canali come intensità dei colori. Questa modalità è utile per il rendering ClearType, che richiede informazioni sul code coverage dei pixel. Per usare la modalità Alpha per canale, un'applicazione deve prima di tutto usare [Direct2D](../direct2d/direct2d-portal.md) e [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) per scrivere i dati di code coverage di pixel in una bitmap. Successivamente, l'applicazione deve impostare la modalità Alpha corretta e specificare un colore del testo quando associa la bitmap a un oggetto visivo. DirectComposition combina il colore del testo con i dati di code coverage, che producono la fusione ClearType rispetto allo sfondo.

Nelle situazioni in cui l'algoritmo ClearType non è applicabile, ad esempio se la bitmap non è allineata al pixel e allineata all'asse o se è necessario disegnarla in una superficie intermedia, DirectComposition può usare i dati di code coverage dei sottopixel nella bitmap per produrre una rasterizzazione in scala di grigi, automaticamente e senza costi aggiuntivi.

Per ulteriori informazioni, vedere la descrizione del parametro *alphaMode* della funzione [**IDCompositionDevice:: CreateSurface**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createsurface) o [**IDCompositionDevice:: CreateVirtualSurface**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createvirtualsurface) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Concetti di DirectComposition](directcomposition-concepts.md)
</dt> </dl>

 

 