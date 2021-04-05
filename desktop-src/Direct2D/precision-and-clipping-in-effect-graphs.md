---
title: Precisione e ritaglio numerico nei grafici effettivi
description: Le applicazioni che eseguono il rendering degli effetti utilizzando Direct2D devono prestare attenzione a raggiungere il livello di qualità e prevedibilità desiderato rispetto alla precisione numerica.
ms.assetid: 6fd1d77f-e613-534f-3205-bad11fa24c30
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90628661ec8cd3f16ff6a6149aecbb7e8be3e5a9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047200"
---
# <a name="precision-and-numerical-clipping-in-effect-graphs"></a>Precisione e ritaglio numerico nei grafici effettivi

Le applicazioni che eseguono il rendering degli effetti utilizzando Direct2D devono prestare attenzione a raggiungere il livello di qualità e prevedibilità desiderato rispetto alla precisione numerica. In questo argomento vengono descritte le procedure consigliate e le impostazioni rilevanti in Direct2D utili se:

-   Il grafico degli effetti si basa su colori o precisione numerica elevata al di fuori dell' \[ intervallo 0, 1 \] e si desidera assicurarsi che siano sempre disponibili
-   In alternativa, il grafico degli effetti si basa sull'implementazione del rendering per bloccare i colori intermedi all' \[ intervallo 0, 1 \] e si vuole garantire che questo blocco avvenga sempre

Direct2D spesso divide un grafico effetto in sezioni ed esegue il rendering di ogni sezione in un passaggio separato. L'output di alcuni passaggi può essere archiviato in trame Direct3D intermedie, che per impostazione predefinita hanno un intervallo numerico e una precisione limitati. Direct2D non fornisce alcuna garanzia su se o dove vengono utilizzate queste trame intermedie. Questo comportamento può variare in base alle funzionalità GPU, oltre che tra le versioni di Windows.

In Windows 10, Direct2D utilizza un minor numero di trame intermedie a causa dell'utilizzo del collegamento dello shader. Direct2D può pertanto produrre risultati diversi con le impostazioni predefinite rispetto alle versioni precedenti di Windows. Ciò influisce principalmente sugli scenari in cui è possibile il collegamento dello shader in un grafico effetto e tale grafico contiene anche gli effetti che producono colori di output con intervallo esteso.

## <a name="overview-of-effect-rendering-and-intermediates"></a>Panoramica del rendering degli effetti e dei intermedi

Per eseguire il rendering di un grafico effetto, Direct2D trova innanzitutto il grafico sottostante di "trasformazioni", dove una trasformazione è un nodo grafico utilizzato in un effetto. Sono disponibili tipi diversi di trasformazioni, inclusi quelli che forniscono Direct3D shader per Direct2D da usare.

Ad esempio, Direct2D può eseguire il rendering di un grafico effetto come segue:

![grafico effetto con trame intermedie](images/precision-and-clipping-1.png)

Direct2D Cerca le opportunità per ridurre il numero di trame intermedie usate per eseguire il rendering del grafico di effetto; Questa logica è opaca per le applicazioni. Il grafico seguente, ad esempio, può essere sottoposto a rendering tramite Direct2D usando una chiamata di disegno Direct3D e nessuna trama intermedia:

![grafico effetto senza trame intermedie](images/precision-and-clipping-2.png)

Prima di Windows 10, Direct2D usava sempre le trame intermedie se venivano usati più pixel shader nello stesso grafico effetto. La maggior parte degli effetti predefiniti che regolano semplicemente i valori dei colori, ad esempio luminosità o saturazione, usano pixel shader.

In Windows 10, Direct2D può ora evitare l'uso di trame intermedie in tali casi. A tale scopo, collega internamente i pixel shader adiacenti. Ad esempio:

![grafico effetto Windows 10 con più pixel shader e nessuna trama intermedia](images/precision-and-clipping-3.png)

Si noti che non tutti i pixel shader adiacenti in un grafico possono essere collegati tra loro e, di conseguenza, solo determinati grafici produrranno output diversi in Windows 10. Per i dettagli completi, vedere [Effect shader linking](effect-shader-linking.md). Le restrizioni principali sono:

-   Un effetto non verrà collegato agli effetti che utilizzano l'output, se il primo effetto è connesso come input a più effetti.
-   Un effetto non verrà collegato con un set di effetti come input, se il primo effetto esegue il campionamento dell'input in una posizione logica diversa rispetto all'output. Ad esempio, un effetto della matrice di colori potrebbe essere collegato al relativo input, ma un effetto di convoluzione non sarà.

## <a name="built-in-effect-behavior"></a>Comportamento degli effetti predefiniti

Molti effetti predefiniti possono produrre colori al di fuori dell' \[ intervallo compreso tra 0 e 1 \] nello spazio colore unpremultiplied, anche quando i relativi colori di input sono compresi in tale intervallo. Quando si verifica questo problema, questi colori possono essere soggetti a ritaglio numerico. Si noti che è importante considerare l'intervallo di colori nello spazio unpremultiplied, anche se gli effetti predefiniti producono in genere colori nello spazio premoltiplicato. Ciò garantisce che i colori rientrino nell'intervallo, anche se altri effetti li unpremultiply successivamente.

Alcuni degli effetti che possono generare questi colori fuori intervallo offrono una proprietà "ClampOutput". Tra queste sono incluse:

-   [Matrice colori](color-matrix.md)
-   [Composizione aritmetica](arithmetic-composite.md)
-   [Condensa](convolve-matrix.md)
-   [Effetti di trasferimento](built-in-effects.md)

L'impostazione della proprietà ClampOutput su TRUE per questi effetti garantisce che venga ottenuto un risultato coerente indipendentemente da fattori quali il collegamento dello shader. Si noti che la pressione si verifica nello spazio unpremultiplied.

Altri effetti predefiniti possono anche produrre colori di output oltre l' \[ intervallo compreso tra 0 e 1 \] nello spazio unpremultiplied, anche quando i colori pixel (e le eventuali proprietà "color") sono compresi in tale intervallo. Tra queste sono incluse:

-   [Trasformazione e scalabilità degli effetti](built-in-effects.md) (quando la proprietà modalità di interpolazione è cubica o di alta qualità)
-   [Effetti sull'illuminazione](built-in-effects.md)
-   [Rilevamento Edge](edge-detection-effect.md) (quando la proprietà bordi sovrapposti è true)
-   [Esposizione](exposure-effect.md)
-   [Composite](composite.md) (quando la proprietà Mode è più)
-   [Temperatura e tinta](temperature-and-tint-effect.md)
-   [Seppia](sepia-effect.md)
-   [Saturazione](saturation.md)

## <a name="forcing-numerical-clipping-within-an-effect-graph"></a>Forzare il ritaglio numerico in un grafico effetto

Quando si usano gli effetti elencati sopra che non dispongono di una proprietà ClampOutput, le applicazioni devono prendere in considerazione la forzatura della pressione numerica. Questa operazione può essere eseguita inserendo un effetto aggiuntivo nel grafico che blocca i pixel. È possibile utilizzare un effetto matrice di colori, con la proprietà' ClampOutput ' impostata su TRUE e lasciando la proprietà' ColorMatrix ' come valore predefinito (pass-through).

Una seconda opzione per ottenere risultati coerenti consiste nel richiedere che Direct2D usi trame intermedie con maggiore precisione. Questa procedura è descritta di seguito.

## <a name="controlling-precision-of-intermediate-textures"></a>Controllo della precisione delle trame intermedie

Direct2D fornisce alcuni modi per controllare la precisione di un grafico. Prima di usare formati a precisione elevata in Direct2D, le applicazioni devono assicurarsi che siano supportate in modo sufficiente dalla GPU. Per verificarlo, usare [**ID2D1DeviceContext:: IsBufferPrecisionSupported**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-isbufferprecisionsupported).

Le applicazioni possono creare un dispositivo Direct3D usando WARP (emulazione software) per garantire che tutte le precisioni del buffer siano supportate indipendentemente dall'hardware GPU effettivo sul dispositivo. Questa operazione è consigliata in scenari come l'applicazione di effetti a una foto durante il salvataggio su disco. Anche se Direct2D supporta formati di buffer a precisione elevata sulla GPU, l'uso di WARP è consigliato in questo scenario sulle GPU a livello di funzionalità 9. X, a causa della precisione limitata dell'aritmetica e del campionamento di shader in alcune GPU mobili a basso consumo.

In ogni caso di seguito, la precisione richiesta è in realtà la precisione minima che verrà usata da Direct2D. Se non sono necessari intermediari, è possibile utilizzare una precisione più elevata. Direct2D può inoltre condividere trame intermedie per diverse parti dello stesso grafico o grafici diversi. In questo caso Direct2D usa la precisione massima richiesta per tutte le operazioni necessarie.

### <a name="precision-selection-from-id2d1devicecontextsetrenderingcontrols"></a>Selezione precisione da ID2D1DeviceContext:: SetRenderingControls

Il modo più semplice per controllare la precisione delle trame intermedie le convenzioni consiste nell'usare [**ID2D1DeviceContext:: SetRenderingControls**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-setrenderingcontrols(constd2d1_rendering_controls)). Consente di controllare la precisione di tutte le trame intermedie, purché una precisione non venga impostata manualmente su effetti o trasformazioni direttamente.


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

Le applicazioni possono anche basarsi sulla precisione degli input in un grafico effetto per controllare la precisione delle trame intermedie. Questa condizione è vera purché una precisione del buffer non venga specificata con [**ID2D1DeviceContext:: SetRenderingControls**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-setrenderingcontrols(constd2d1_rendering_controls))e non sia impostata manualmente su effetti e trasforma direttamente.

Le precisioni degli input agli effetti vengono propagate tramite il grafo per selezionare la precisione dei intermediari downstream. Quando vengono soddisfatti rami diversi nel grafico degli effetti, viene usata la massima precisione di qualsiasi input.

La precisione selezionata in base a una bitmap Direct2D è determinata dal formato pixel. La precisione selezionata per un [**ID2D1ImageSource**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1imagesource) è determinata dal formato pixel WIC del IWICBitmapSource sottostante utilizzato per creare **ID2D1ImageSource**. Si noti che Direct2D non consente la creazione di origini di immagini con origini WIC usando le precisioni non supportate da Direct2D e dalla GPU.

È possibile che Direct2D non possa assegnare un effetto a una precisione in base ai relativi input. Ciò si verifica quando un effetto non ha input o quando viene usato un [**ID2D1CommandList**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1commandlist) , che non ha precisione specifica. In questo caso, la precisione delle trame intermedie viene determinata dalla bitmap impostata come destinazione di rendering corrente del contesto.

### <a name="precision-selection-directly-on-the-effect-and-transforms"></a>Selezione di precisione direttamente sull'effetto e le trasformazioni

La precisione minima per le trame intermedie può essere impostata anche in posizioni esplicite all'interno di un grafico effetto. Questa opzione è consigliata solo per scenari avanzati.

La precisione minima può essere impostata utilizzando una proprietà in un effetto come indicato di seguito:


```cpp
if (Device->IsBufferPrecisionSupported(D2D1_BUFFER_PRECISION_32BPC_FLOAT))
{
  hr = Effect->SetValue(D2D1_PROPERTY_PRECISION, D2D1_BUFFER_PRECISION_32BPC_FLOAT);
}
              
```



All'interno di un'implementazione di effetto, la precisione minima può essere impostata usando ID2D1RenderInfo:: SetOutputPrecision come indicato di seguito:


```cpp
if (EffectContext->IsBufferPrecisionSupported(D2D1_BUFFER_PRECISION_32BPC_FLOAT))
{
  hr = RenderInfo->SetOutputBuffer(
  D2D1_BUFFER_PRECISION_32BPC_FLOAT,
  D2D1_CHANNEL_DEPTH_4);
}
              
```



Si noti che la precisione impostata su un effetto verrà propagata agli effetti downstream nello stesso grafico effetto, a meno che non venga impostata una precisione diversa per tali effetti downstream. Il set di precisione in una trasformazione all'interno di un effetto non influisce sulla precisione per i nodi di trasformazione downstream.

Di seguito è riportata la logica ricorsiva completa utilizzata per determinare la precisione minima per un buffer intermedio che archivia l'output di un nodo di trasformazione specificato:

![Logica minima di precisione del buffer intermedio](images/precision-and-clipping-4.png)

 

 