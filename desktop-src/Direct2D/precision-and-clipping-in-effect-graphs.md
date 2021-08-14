---
title: Precisione e ritaglio numerico nei grafici degli effetti
description: Le applicazioni che eseguono il rendering degli effetti con Direct2D devono fare attenzione a ottenere il livello desiderato di qualità e prevedibilità rispetto alla precisione numerica.
ms.assetid: 6fd1d77f-e613-534f-3205-bad11fa24c30
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24f2af6fdee4561caa60ea22a0c700593f2333727e6c5a63c5346fdc78bbdb40
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118160505"
---
# <a name="precision-and-numerical-clipping-in-effect-graphs"></a>Precisione e ritaglio numerico nei grafici degli effetti

Le applicazioni che eseguono il rendering degli effetti con Direct2D devono fare attenzione a ottenere il livello desiderato di qualità e prevedibilità rispetto alla precisione numerica. Questo argomento descrive le procedure consigliate e le impostazioni pertinenti in Direct2D che sono utili nei seguenti modi:

-   Il grafico degli effetti si basa su una precisione numerica elevata o su colori esterni all'intervallo 0, 1 e si vuole assicurarsi che \[ \] siano sempre disponibili
-   In caso contrario, il grafico degli effetti si basa sull'implementazione del rendering per impostare i colori intermedi in base all'intervallo 0, 1 e si vuole assicurarsi che questa chiusura si verifichi \[ \] sempre

Direct2D spesso divide un grafico degli effetti in sezioni ed esegue il rendering di ogni sezione in un passaggio separato. L'output di alcuni passaggi può essere archiviato in trame Direct3D intermedie che per impostazione predefinita hanno un intervallo numerico e una precisione limitati. Direct2D non garantisce se o dove vengono usate queste trame intermedie. Questo comportamento può variare in base alle funzionalità della GPU e tra Windows versioni.

In Windows 10 Direct2D usa meno trame intermedie a causa dell'uso del collegamento dello shader. Direct2D può quindi produrre risultati diversi con le impostazioni predefinite rispetto alle versioni Windows precedenti. Questo influisce principalmente sugli scenari in cui il collegamento dello shader è possibile in un grafico degli effetti e tale grafico contiene anche effetti che producono colori di output a intervalli estesi.

## <a name="overview-of-effect-rendering-and-intermediates"></a>Panoramica del rendering degli effetti e degli elementi intermedi

Per eseguire il rendering di un grafico degli effetti, Direct2D trova innanzitutto il grafico sottostante delle "trasformazioni", in cui una trasformazione è un nodo del grafo usato all'interno di un effetto. Esistono diversi tipi di trasformazioni, inclusi quelli che forniscono shader Direct3D che Direct2D può usare.

Ad esempio, Direct2D può eseguire il rendering di un grafico degli effetti come segue:

![grafico degli effetti con trame intermedie](images/precision-and-clipping-1.png)

Direct2D cerca opportunità per ridurre il numero di trame intermedie usate per eseguire il rendering del grafico degli effetti; Questa logica è opaca per le applicazioni. Ad esempio, il rendering del grafico seguente può essere eseguito da Direct2D usando una chiamata di disegno Direct3D e nessuna trama intermedia:

![Grafico degli effetti senza trame intermedie](images/precision-and-clipping-2.png)

Prima di Windows 10, Direct2D usava sempre trame intermedie se venivano usati più shader pixel all'interno dello stesso grafico degli effetti. La maggior parte degli effetti predefiniti che regolano semplicemente i valori dei colori (ad esempio Luminosità o Saturazione) usa pixel shader.

In Windows 10, Direct2D può ora evitare l'uso di trame intermedie in questi casi. A tale scopo, collega internamente pixel shader adiacenti. Esempio:

![Grafico degli effetti di Windows 10 con più pixel shader e nessuna trama intermedia](images/precision-and-clipping-3.png)

Si noti che non tutti i pixel shader adiacenti in un grafo possono essere collegati tra loro e pertanto solo determinati grafici produrranno output diversi in Windows 10. Per informazioni dettagliate, vedere [Effect Shader Linking (Collegamento degli effetti shader).](effect-shader-linking.md) Le restrizioni principali sono:

-   Un effetto non verrà collegato agli effetti che utilizzano l'output, se il primo effetto è connesso come input a più effetti.
-   Un effetto non verrà collegato con un set di effetti come input, se il primo effetto campione l'input in una posizione logica diversa rispetto all'output. Ad esempio, un effetto Matrice di colori potrebbe essere collegato al relativo input, ma un effetto Convoluzione non lo sarà.

## <a name="built-in-effect-behavior"></a>Comportamento degli effetti predefiniti

Molti effetti predefiniti possono produrre colori al di fuori dell'intervallo 0, 1 nello spazio colori nonpremoltilied, anche quando i colori di input sono all'interno di \[ \] tale intervallo. In questo caso, tali colori possono essere soggetti a ritaglio numerico. Si noti che è importante considerare l'intervallo di colori nello spazio nonpremoltilied, anche se gli effetti predefiniti producono in genere colori nello spazio premoltimullied. In questo modo si garantisce che i colori rimangano entro l'intervallo, anche se altri effetti successivamente non li eserciterà in modo imprevedibile.

Alcuni degli effetti che possono generare questi colori fuori intervallo offrono una proprietà "ClampOutput". Queste includono:

-   [Matrice colori](color-matrix.md)
-   [Composito aritmetico](arithmetic-composite.md)
-   [Convolvo](convolve-matrix.md)
-   [Effetti di trasferimento](built-in-effects.md)

L'impostazione della proprietà ClampOutput su TRUE per questi effetti garantisce un risultato coerente indipendentemente da fattori come il collegamento dello shader. Si noti che la chiusura avviene in uno spazio nonpremoltilied.

Altri effetti predefiniti possono anche produrre colori di output oltre l'intervallo 0, 1 nello spazio nonpremoltilied, anche quando i relativi pixel dei colori (e le proprietà "Color" se presenti) sono all'interno di tale \[ \] intervallo. Queste includono:

-   [Effetti di trasformazione e ridimensionamento](built-in-effects.md) (quando la proprietà Modalità di interpolazione è Cubic o Cubic di alta qualità)
-   [Effetti di illuminazione](built-in-effects.md)
-   [Rilevamento dei bordi](edge-detection-effect.md) (quando la proprietà Bordi sovrimpressione è TRUE)
-   [Esposizione](exposure-effect.md)
-   [Composito](composite.md) (quando la proprietà Mode è Plus)
-   [Temperatura e tinta](temperature-and-tint-effect.md)
-   [Seppia](sepia-effect.md)
-   [Saturazione](saturation.md)

## <a name="forcing-numerical-clipping-within-an-effect-graph"></a>Forzatura del ritaglio numerico all'interno di un grafico degli effetti

Anche se si usano gli effetti elencati in precedenza che non hanno una proprietà ClampOutput, le applicazioni devono prendere in considerazione la forzatura del blocco numerico. Questa operazione può essere eseguita inserendo un effetto aggiuntivo nel grafico che ne stringe i pixel. È possibile usare un effetto Matrice colori, con la proprietà 'ClampOutput' impostata su TRUE e lasciando la proprietà 'ColorMatrix' come valore predefinito (pass-through).

Una seconda opzione per ottenere risultati coerenti consiste nel richiedere che Direct2D usi trame intermedie con maggiore precisione. Questa operazione è descritta di seguito.

## <a name="controlling-precision-of-intermediate-textures"></a>Controllo della precisione delle trame intermedie

Direct2D offre diversi modi per controllare la precisione di un grafo. Prima di usare formati ad alta precisione in Direct2D, le applicazioni devono assicurarsi che siano sufficientemente supportate dalla GPU. Per verificare questo problema, [**usare ID2D1DeviceContext::IsBufferPrecisionSupported.**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-isbufferprecisionsupported)

Le applicazioni possono creare un dispositivo Direct3D usando WARP (emulazione software) per garantire che tutte le precisione del buffer siano supportate indipendentemente dall'hardware GPU effettivo nel dispositivo. Questa operazione è consigliata in scenari come l'applicazione di effetti a una foto durante il salvataggio su disco. Anche se Direct2D supporta formati di buffer ad alta precisione nella GPU, in questo scenario è consigliabile usare WARP nelle GPU a livello di funzionalità 9.X, a causa della precisione limitata dell'aritmetica dello shader e del campionamento in alcune GPU per dispositivi mobili a bassa potenza.

In ogni caso riportato di seguito, la precisione richiesta è effettivamente la precisione minima che verrà utilizzata da Direct2D. Se non sono necessari intermedi, è possibile usare una precisione più elevata. Direct2D può anche condividere trame intermedie per parti diverse dello stesso grafo o per grafici diversi. In questo caso Direct2D usa la precisione massima richiesta per tutte le operazioni coinvolte.

### <a name="precision-selection-from-id2d1devicecontextsetrenderingcontrols"></a>Selezione della precisione da ID2D1DeviceContext::SetRenderingControls

Il modo più semplice per controllare la precisione delle trame intermedie di Direct2D consiste nell'usare [**ID2D1DeviceContext::SetRenderingControls.**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-setrenderingcontrols(constd2d1_rendering_controls)) Controlla la precisione di tutte le trame intermedie, purché non sia impostata manualmente anche su effetti o trasformazioni direttamente.


```cpp
if (Device->IsBufferPrecisionSupported(D2D1_BUFFER_PRECISION_32BPC_FLOAT))
{
  // Get the current rendering controls
  D2D1_RENDERING_CONTROLS renderingControls = {};
  Context->GetRenderingControls(&renderingControls);

  // Switch the precision within the rendering controls and set it
  renderingControls.bufferPrecision = D2D1_BUFFER_PRECISION_32BPC_FLOAT;
  Context->SetRenderingControls(&renderingControls);
}
              
```



### <a name="precision-selection-from-inputs-and-render-targets"></a>Selezione della precisione dagli input e dalle destinazioni di rendering

Le applicazioni possono anche basarsi sulla precisione degli input in un grafico degli effetti per controllare la precisione delle trame intermedie. Questo vale purché la precisione del buffer non sia specificata usando [**ID2D1DeviceContext::SetRenderingControls**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-setrenderingcontrols(constd2d1_rendering_controls))e non sia impostata manualmente sugli effetti e la trasformazione direttamente.

Le precisione degli input per gli effetti vengono propagate tramite il grafico per selezionare la precisione degli intermedi downstream. Quando si incontrano rami diversi nel grafico degli effetti, viene usata la massima precisione di qualsiasi input.

La precisione selezionata in base a una bitmap Direct2D è determinata dal formato pixel. La precisione selezionata per [**id2D1ImageSource**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1imagesource) è determinata dal formato in pixel WIC dell'oggetto IWICBitmapSource sottostante usato per creare **l'oggetto ID2D1ImageSource.** Si noti che Direct2D non consente la creazione di origini di immagini con origini WIC usando precisione non supportate da Direct2D e dalla GPU.

È possibile che Direct2D non possa assegnare a un effetto una precisione in base ai relativi input. Ciò si verifica quando un effetto non ha input o quando viene usato [**id2D1CommandList,**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1commandlist) che non ha una precisione specifica. In questo caso, la precisione delle trame intermedie è determinata dal set di bitmap come destinazione di rendering corrente del contesto.

### <a name="precision-selection-directly-on-the-effect-and-transforms"></a>Selezione della precisione direttamente sull'effetto e sulle trasformazioni

La precisione minima per le trame intermedie può anche essere impostata in posizioni esplicite all'interno di un grafico degli effetti. Questa opzione è consigliata solo per scenari avanzati.

La precisione minima può essere impostata usando una proprietà su un effetto come indicato di seguito:


```cpp
if (Device->IsBufferPrecisionSupported(D2D1_BUFFER_PRECISION_32BPC_FLOAT))
{
  hr = Effect->SetValue(D2D1_PROPERTY_PRECISION, D2D1_BUFFER_PRECISION_32BPC_FLOAT);
}
              
```



All'interno di un'implementazione dell'effetto, la precisione minima può essere impostata usando ID2D1RenderInfo::SetOutputPrecision come indicato di seguito:


```cpp
if (EffectContext->IsBufferPrecisionSupported(D2D1_BUFFER_PRECISION_32BPC_FLOAT))
{
  hr = RenderInfo->SetOutputBuffer(
  D2D1_BUFFER_PRECISION_32BPC_FLOAT,
  D2D1_CHANNEL_DEPTH_4);
}
              
```



Si noti che la precisione impostata su un effetto verrà propagata agli effetti downstream nello stesso grafico degli effetti, a meno che non venga impostata una precisione diversa su tali effetti downstream. La precisione impostata su una trasformazione all'interno di un effetto non influisce sulla precisione per i nodi di trasformazione a valle.

Di seguito è riportata la logica ricorsiva completa usata per determinare la precisione minima per un buffer intermedio che archivia l'output di un nodo di trasformazione specificato:

![Logica di precisione minima del buffer intermedia](images/precision-and-clipping-4.png)

 

 