---
title: Glossario DirectComposition
description: Questo argomento definisce le condizioni di DirectComposition Microsoft.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 3B9932EA-3182-41D0-B64A-7699EC98A714
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c72186f65f64e1187069963f0aae36de2835fd9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338047"
---
# <a name="directcomposition-glossary"></a>Glossario DirectComposition

> [!NOTE]
> Per le app in Windows 10, è consigliabile usare le API Windows. UI. Composition anziché DirectComposition. Per altre informazioni, vedere [modernizzare l'app desktop usando il livello visivo](/windows/uwp/composition/visual-layer-in-desktop-apps).

Questo argomento definisce le condizioni di DirectComposition Microsoft.

<dl> <dt>

<span id="directcomp_glossary_animation_function"></span><span id="DIRECTCOMP_GLOSSARY_ANIMATION_FUNCTION"></span>**animazione (funzione)**
</dt> <dd>

Costrutto che specifica la modalità di modifica del valore di una singola proprietà dell'oggetto in un determinato periodo di tempo.

</dd> <dt>

<span id="directcomp_glossary_animation_object"></span><span id="DIRECTCOMP_GLOSSARY_ANIMATION_OBJECT"></span>**oggetto Animation**
</dt> <dd>

Oggetto che rappresenta una funzione per l'animazione delle proprietà di un altro oggetto.

</dd> <dt>

<span id="directcomp_glossary_animation_primitive"></span><span id="DIRECTCOMP_GLOSSARY_ANIMATION_PRIMITIVE"></span>**segmento di animazione**
</dt> <dd>

Definizioni di intervallo fondamentali di una funzione di animazione; sono le primitive da cui vengono compilate funzioni di animazione più complesse e di livello superiore.

</dd> <dt>

<span id="directcomp_glossary_back_buffer"></span><span id="DIRECTCOMP_GLOSSARY_BACK_BUFFER"></span>**buffer nascosto**
</dt> <dd>

Un rettangolo di memoria in cui un'applicazione può scrivere direttamente. Il buffer nascosto non viene mai visualizzato direttamente sul monitor.

</dd> <dt>

<span id="directcomp_glossary_batch"></span><span id="DIRECTCOMP_GLOSSARY_BATCH"></span>**batch**
</dt> <dd>

Gruppo di chiamate al metodo DirectComposition elaborate atomicamente.

</dd> <dt>

<span id="directcomp_glossary_bitmap"></span><span id="DIRECTCOMP_GLOSSARY_BITMAP"></span>**bitmap**
</dt> <dd>

Un buffer di colore, con o senza un canale alfa, che risiede nella memoria di sistema o video.

</dd> <dt>

<span id="directcomp_glossary_border_mode"></span><span id="DIRECTCOMP_GLOSSARY_BORDER_MODE"></span>**modalità bordo**
</dt> <dd>

Proprietà di un oggetto visivo Microsoft DirectComposition che influiscono sulla composizione dei bordi di una bitmap quando la bitmap viene trasformata in modo tale che i bordi non siano allineati all'asse con le coordinate di tipo Integer. Influiscono inoltre sul modo in cui il contenuto viene ritagliato negli angoli di una clip con angoli arrotondati e al bordo di una clip trasformata in modo tale che i bordi non siano allineati all'asse con le coordinate di tipo Integer.

</dd> <dt>

<span id="directcomp_glossary_clip_object"></span><span id="DIRECTCOMP_GLOSSARY_CLIP_OBJECT"></span>**clip (oggetto)**
</dt> <dd>

Oggetto che rappresenta un rettangolo di ritaglio.

</dd> <dt>

<span id="directcomp_glossary_clip_rectangle"></span><span id="DIRECTCOMP_GLOSSARY_CLIP_RECTANGLE"></span>**rettangolo di ritaglio**
</dt> <dd>

Set di coordinate che definiscono l'area del contenuto bitmap dell'oggetto visivo disegnato sullo schermo quando viene eseguito il rendering della bitmap.

</dd> <dt>

<span id="directcomp_glossary_cloak"></span><span id="DIRECTCOMP_GLOSSARY_CLOAK"></span>**mantello**
</dt> <dd>

Per impedire temporaneamente a Gestione finestre desktop (DWM) di disegnare una finestra sullo schermo. Le applicazioni in genere mascherano una finestra mentre DirectComposition usa la bitmap della finestra in una composizione.

</dd> <dt>

<span id="directcomp_glossary_commit"></span><span id="DIRECTCOMP_GLOSSARY_COMMIT"></span>**commit**
</dt> <dd>

Per inviare un batch di comandi a DirectCompositionDirectComposition per l'elaborazione.

</dd> <dt>

<span id="directcomp_glossary_composite_mode"></span><span id="DIRECTCOMP_GLOSSARY_COMPOSITE_MODE"></span>**modalità composita**
</dt> <dd>

Uno dei diversi modi per combinare due bitmap, un'origine e una destinazione, per ottenere un effetto particolare.

</dd> <dt>

<span id="directcomp_glossary_composition"></span><span id="DIRECTCOMP_GLOSSARY_COMPOSITION"></span>**Composizione**
</dt> <dd>

Raccolta di bitmap combinate e modificate applicando varie trasformazioni, effetti e animazioni per produrre un risultato visivo previsto in un'interfaccia utente dell'applicazione.

</dd> <dt>

<span id="directcomp_glossary_composition_target_window"></span><span id="DIRECTCOMP_GLOSSARY_COMPOSITION_TARGET_WINDOW"></span>**finestra di destinazione composizione**
</dt> <dd>

La finestra a cui è associata una struttura ad albero visuale e in cui viene disegnata la composizione risultante.

</dd> <dt>

<span id="directcomp_glossary_effect"></span><span id="DIRECTCOMP_GLOSSARY_EFFECT"></span>**effetto**
</dt> <dd>

Operazione che modifica il modo in cui le bitmap di una struttura ad albero visuale vengono rasterizzate, in genere applicando un pixel shader.

</dd> <dt>

<span id="directcomp_glossary_effect_group"></span><span id="DIRECTCOMP_GLOSSARY_EFFECT_GROUP"></span>**gruppo effetti**
</dt> <dd>

Gruppo di effetti bitmap che vengono applicati insieme per modificare la rasterizzazione del sottoalbero di un oggetto visivo.

</dd> <dt>

<span id="directcomp_glossary_frame"></span><span id="DIRECTCOMP_GLOSSARY_FRAME"></span>**frame**
</dt> <dd>

Iterazione del motore di composizione che produce una rasterizzazione della struttura ad albero visuale.

</dd> <dt>

<span id="directcomp_glossary_front_buffer"></span><span id="DIRECTCOMP_GLOSSARY_FRONT_BUFFER"></span>**buffer anteriore**
</dt> <dd>

Un rettangolo di memoria convertito dalla scheda grafica e visualizzato sul monitor.

</dd> <dt>

<span id="directcomp_glossary_interpolation_mode"></span><span id="DIRECTCOMP_GLOSSARY_INTERPOLATION_MODE"></span>**modalità di interpolazione**
</dt> <dd>

Proprietà che determina la modalità di composizione di una bitmap quando viene trasformata in modo tale che non esista una corrispondenza uno-a-uno tra i pixel nella bitmap e i pixel sullo schermo.

</dd> <dt>

<span id="directcomp_glossary_root_visual"></span><span id="DIRECTCOMP_GLOSSARY_ROOT_VISUAL"></span>**elemento visivo radice**
</dt> <dd>

Oggetto visivo da cui discendono tutti gli altri oggetti visivi in una struttura ad albero visuale.

</dd> <dt>

<span id="directcomp_glossary_swap_chain"></span><span id="DIRECTCOMP_GLOSSARY_SWAP_CHAIN"></span>**Scambia catena**
</dt> <dd>

Raccolta di uno o più buffer back che possono essere presentati in modo seriale al buffer anteriore

</dd> <dt>

<span id="directcomp_glossary_surface"></span><span id="DIRECTCOMP_GLOSSARY_SURFACE"></span>**area**
</dt> <dd>

Rappresentazione di un'area lineare della memoria di visualizzazione che in genere risiede nella memoria di visualizzazione della scheda video, sebbene le superfici possano essere presenti nella memoria di sistema.

</dd> <dt>

<span id="directcomp_glossary_transform"></span><span id="DIRECTCOMP_GLOSSARY_TRANSFORM"></span>**trasformazione**
</dt> <dd>

Matrice che rappresenta una trasformazione delle coordinate in uno spazio bidimensionale o tridimensionale.

</dd> <dt>

<span id="directcomp_glossary_transform_group"></span><span id="DIRECTCOMP_GLOSSARY_TRANSFORM_GROUP"></span>**gruppo di trasformazione**
</dt> <dd>

Raccolta di trasformazioni le cui matrici vengono moltiplicate insieme nell'ordine in cui sono specificate nella raccolta prima che vengano applicate a un oggetto visivo.

</dd> <dt>

<span id="directcomp_glossary_visual"></span><span id="DIRECTCOMP_GLOSSARY_VISUAL"></span>**Visual**
</dt> <dd>

Oggetto che contiene un riferimento facoltativo a un oggetto bitmap e un set di proprietà che determinano la posizione e il modo in cui viene eseguito il rendering della bitmap sullo schermo.

</dd> <dt>

<span id="directcomp_glossary_visual_object"></span><span id="DIRECTCOMP_GLOSSARY_VISUAL_OBJECT"></span>**oggetto visivo**
</dt> <dd>

Vedere [*Visual*](/windows).

</dd> <dt>

<span id="directcomp_glossary_visual_subtree"></span><span id="DIRECTCOMP_GLOSSARY_VISUAL_SUBTREE"></span>**sottoalbero visuale**
</dt> <dd>

Parte di una struttura ad albero visuale costituita da un oggetto visivo particolare e da tutti i relativi oggetti visivi figlio e discendente.

</dd> <dt>

<span id="directcomp_glossary_visual_tree"></span><span id="DIRECTCOMP_GLOSSARY_VISUAL_TREE"></span>**struttura ad albero visuale**
</dt> <dd>

Raccolta gerarchica di oggetti visivi utilizzati per creare una composizione.

</dd> <dt>

<span id="directcomp_glossary_windowless_swap_chain"></span><span id="DIRECTCOMP_GLOSSARY_WINDOWLESS_SWAP_CHAIN"></span>**catena di scambio senza finestra**
</dt> <dd>

Catena di scambio associata a un oggetto visivo DirectComposition anziché a una finestra.

</dd> </dl>

 

 