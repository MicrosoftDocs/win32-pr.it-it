---
title: Oggetti bitmap
description: Questo argomento descrive i tipi di contenuto bitmap supportati da DirectComposition.
ms.assetid: BC32CF76-D5E4-4B25-AFD5-42E8DABFA0D0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc36253511c060b264039f27975c694272c1c916ad0067c1955fd02f00553d6d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118089051"
---
# <a name="bitmap-objects"></a>Oggetti bitmap

> [!NOTE]
> Per le app Windows 10, è consigliabile usare le API Windows.UI.Composition anziché DirectComposition. Per altre informazioni, vedi [Modernizzare l'app desktop usando il livello visivo](/windows/uwp/composition/visual-layer-in-desktop-apps).

Microsoft DirectComposition è un motore di composizione bitmap. Consente agli sviluppatori di applicazioni di combinare più bitmap e modificarle in vari modi per ottenere effetti visivi e animazioni interessanti nell'interfaccia utente di un'applicazione. Questo argomento descrive i tipi di contenuto bitmap supportati da DirectComposition.

-   [Contenuto bitmap](#bitmap-content)
    -   [Bitmap della memoria video](#video-memory-bitmaps)
    -   [Bitmap della finestra](#window-bitmaps)
    -   [Associazione del contenuto bitmap a un oggetto visivo](#associating-bitmap-content-with-a-visual)
    -   [Canale alfa](#alpha-channel)
-   [Argomenti correlati](#related-topics)

## <a name="bitmap-content"></a>Contenuto bitmap

Le applicazioni forniscono a DirectComposition il contenuto bitmap da comporre e animare creando oggetti visivi e quindi impostando la [proprietà Content](basic-concepts.md) di tali oggetti. DirectComposition non offre servizi di rasterizzazione. Un'applicazione deve usare un'altra libreria di rasterizzazione basata su software o con accelerazione hardware, ad esempio [Direct2D](../direct2d/direct2d-portal.md) o [Direct3D,](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) per popolare le bitmap che devono essere composte. Dopo la composizione, DirectComposition passa il contenuto bitmap composto [a Gestione finestre desktop (DWM) per](/windows/desktop/dwm/dwm-overview) il rendering sullo schermo.

**Tipi supportati di contenuto bitmap** Microsoft DirectComposition supporta i tipi di bitmap seguenti:

-   [Bitmap della memoria video](#video-memory-bitmaps)
-   [Bitmap della finestra](#window-bitmaps)

### <a name="video-memory-bitmaps"></a>Bitmap della memoria video

Una bitmap della memoria video viene rasterizzata nell'hardware usando i metodi Microsoft DirectX (incluso il modello di interoperabilità da DX a GDI). È supportata da superfici condivise tra processi visibili all'applicazione chiamante e a DirectComposition. Una bitmap della memoria video non è soggetta alla rimozione perché l'applicazione può leggere solo dalle superfici da cui DirectComposition è in grado di eseguire le trame.

### <a name="video-content"></a>Contenuto video

Le applicazioni possono usare DirectComposition per comporre fotogrammi video che usano catene di scambio senza finestra DirectX associate a una superficie DirectComposition. Concettualmente, DirectComposition considera il contenuto video come una sequenza di bitmap. DirectComposition non fornisce un modo per presentare fotogrammi video.

DirectComposition supporta catene di scambio senza finestra DirectX, ovvero catene di scambio non associate a una determinata finestra, e consente a due applicazioni diverse di condividere catene di scambio senza finestra tra i limiti del processo. La condivisione di catene di scambio senza finestra consente scenari video in cui la catena di scambio viene creata in un processo e viene usata con DirectComposition in un secondo processo. Le catene di scambio senza finestra vengono create usando il [**metodo IDXGIFactory2::CreateSwapChainForCompositionSurface.**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcomposition)

Per altre informazioni sulle catene di scambio DirectX, vedere [Panoramica di DXGI.](/windows/desktop/direct3ddxgi/d3d10-graphics-programming-guide-dxgi)

### <a name="stereo-content"></a>Contenuto stereo

Concettualmente, una catena di scambio stereo è costituita da superfici Microsoft DirectX Graphic Infrastructure (DXGI) che rappresentano i canali sinistro e destro per il contenuto 3D stereo. Quando una catena di scambio stereo viene usata come risorsa bitmap per un oggetto visivo, DirectComposition esegue la composizione in stereo. Tutti i contenuti non stereo (contenuto mono) sono considerati con lo stesso contenuto dei canali sinistro e destro; in altri casi, lo stesso contenuto bitmap viene usato per entrambi i canali. DirectComposition compone tutto il contenuto sinistro e tutto il contenuto a destra separatamente. Se il dispositivo di visualizzazione non supporta lo stereo, DirectComposition considera il canale stereo sinistro o destro (a seconda dell'applicazione) come contenuto mono e compone usando solo i dati per la risorsa bitmap.

DirectComposition non supporta la creazione o la modifica di contenuto stereo e non può alzare di livello una catena di scambio mono a una coppia stereo. Un'applicazione deve eseguire queste attività prima di presentare contenuto stereo DirectX a DirectComposition. Inoltre, un'applicazione deve fornire gli offset dei canali sinistro e destro per la percezione della profondità; DirectComposition non può modificare gli offset dei canali sinistro e destro per modificare la profondità percepita del contenuto stereo DirectX.

Il contenuto stereo DirectX viene composto e salvato in modo permanente in DWM quando è disponibile hardware con supporto per stereo.

### <a name="window-bitmaps"></a>Bitmap della finestra

Una "bitmap della finestra" non è una bitmap reale, ma è un segnaposto che DirectComposition sostituisce in tempo reale con rasterizzazioni di finestre di primo livello o figlio su più livelli. Una bitmap della finestra è simile a un'anteprima DWM, ad eccezione del fatto che un'anteprima può contenere contributi da molte finestre, ad esempio finestre non figlio di proprietà, mentre una bitmap della finestra DirectComposition è sempre una rappresentazione di una sola finestra e dei relativi elementi figlio.

Poiché DirectComposition ha accesso alle superfici di reindirizzamento di tutte le finestre e di tutte le strutture ad albero visuali, può riutilizzare il contenuto da una finestra in più alberi visivi. La finestra deve essere su più livelli perché una finestra non su più livelli non ha una superficie di reindirizzamento dedicata e, pertanto, la rasterizzazione non è sempre disponibile per DirectComposition.

Per usare una bitmap della finestra, un'applicazione associa un oggetto visivo a un handle di finestra (HWND). In seguito, DirectComposition ricomposi l'oggetto visivo ogni volta che il contenuto della finestra cambia, incluso quando il contenuto cambia in seguito alle modifiche apportate alle strutture ad albero visuali associate alla finestra. In altre parole, come le anteprime DWM, le bitmap della finestra DirectComposition sono "live".

### <a name="associating-bitmap-content-with-a-visual"></a>Associazione del contenuto bitmap a un oggetto visivo

Per tutti e tre i tipi di bitmap, un'applicazione può associare la stessa bitmap a più oggetti visivi, il che significa che è possibile usare una singola allocazione di memoria per visualizzare più volte lo stesso contenuto.

### <a name="alpha-channel"></a>Canale alfa

Tutte le bitmap hanno un formato BPP (32 bit per pixel), che include otto bit per la trasparenza per pixel. Tuttavia, un'applicazione può specificare come DirectComposition deve utilizzare il canale alfa. In particolare, DirectComposition può rispettare il canale alfa o ignorare completamente il valore alfa, nel qual caso la bitmap viene considerata completamente opaca.

Una modalità alfa aggiuntiva ignora il canale alfa, ma considera i valori rosso, verde e blu come valori alfa per canale anziché la normale interpretazione di tali canali come intensità di colore. Questa modalità è utile per il rendering ClearType, che richiede informazioni sulla copertura dei pixel secondari. Per usare la modalità alfa per canale, un'applicazione deve prima di tutto usare [Direct2D](../direct2d/direct2d-portal.md) e DirectWrite per [scrivere](/windows/desktop/DirectWrite/direct-write-portal) dati di code coverage sub-pixel in una bitmap. Successivamente, l'applicazione deve impostare la modalità alfa corretta e specificare un colore del testo quando associa la bitmap a un oggetto visivo. DirectComposition combina il colore del testo con i dati di code coverage, che generano la fusione ClearType sullo sfondo.

Nelle situazioni in cui l'algoritmo ClearType non è applicabile, ad esempio se la bitmap non è allineata a pixel e allineata all'asse o se deve essere disegnata su una superficie intermedia, DirectComposition può usare i dati di code coverage subpixel nella bitmap per produrre invece una rasterizzazione in scala di grigi, automaticamente e senza costi aggiuntivi.

Per altre informazioni, vedere la descrizione del parametro *alphaMode* della funzione [**IDCompositionDevice::CreateSurface**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createsurface) [**o IDCompositionDevice::CreateVirtualSurface.**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createvirtualsurface)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Concetti relativi a DirectComposition](directcomposition-concepts.md)
</dt> </dl>

 

 