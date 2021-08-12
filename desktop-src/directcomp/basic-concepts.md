---
title: Concetti di base (DirectComposition)
description: Questo argomento offre una panoramica dei concetti di base di Microsoft DirectComposition.
ms.assetid: F442BDCA-C913-4438-BFFA-D3F28B68EE85
keywords:
- Concetti relativi a DirectComposition
- Concetti di base di DirectComposition
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c2dadcea55ec18089380d7dbe17d99e5dba92b06dd15774c43cd604f28f991c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118282029"
---
# <a name="basic-concepts"></a>Concetti fondamentali

> [!NOTE]
> Per le app Windows 10, è consigliabile usare le API Windows.UI.Composition anziché DirectComposition. Per altre informazioni, vedere [Modernizzare l'app desktop usando il livello Visivo.](/windows/uwp/composition/visual-layer-in-desktop-apps)

Questo argomento offre una panoramica dei concetti di base di Microsoft DirectComposition. Contiene le sezioni seguenti:

-   [Composizione](#composition-target-window)
-   [Oggetti visivi](#visuals)
    -   [Albero visuale](#visual-tree)
    -   [Proprietà di un oggetto visivo](#properties-of-a-visual-object)
-   [Oggetto dispositivo](#device-object)
-   [Finestra di destinazione della composizione](#composition-target-window)
-   [Composizione transazionale](#transactional-composition)
    -   [Batch](#batching)
    -   [Sincronizzazione](#synchronization)
    -   [Alberi visivi tra dispositivi](#cross-device-visual-trees)
-   [Argomenti correlati](#related-topics)

## <a name="composition"></a>Composizione

DirectComposition definisce  una composizione come raccolta di bitmap combinate e manipolate applicando varie trasformazioni, effetti e animazioni per produrre un risultato visivo in un'interfaccia utente dell'applicazione. DirectComposition funziona solo con il contenuto bitmap; non supporta vettori o testo. DirectComposition non fornisce contenuto bitmap. Fornisce invece interfacce in cui gli utenti possono disegnare con D2D, DXGI o caricare il proprio contenuto di trama.

Un'applicazione DirectComposition crea due set di oggetti per comporre una scena: bitmap composte insieme e oggetti visivi che definiscono le relazioni spaziali tra le bitmap. Per altre informazioni sugli oggetti bitmap supportati da DirectComposition, vedere [Oggetti bitmap](bitmap-surfaces.md).

## <a name="visuals"></a>Oggetti visivi

*Gli oggetti* visivi *(o oggetti visivi)* sono gli elementi fondamentali di DirectComposition. Sono i blocchi predefiniti di base che si usano per creare composizioni e animazioni nell'interfaccia utente dell'applicazione.

In termini di programmazione, un oggetto visivo è un oggetto con un set di proprietà ed espone un'interfaccia utilizzata per impostare il valore delle proprietà. La proprietà Content di un oggetto visivo associa una particolare bitmap all'oggetto visivo, mentre altre proprietà controllano il modo in cui DirectComposition posiziona e modifica l'oggetto visivo durante il rendering sullo schermo.

Per altre informazioni, vedere [Proprietà di un oggetto visivo](#properties-of-a-visual-object).

### <a name="visual-tree"></a>Albero visuale

DirectComposition crea una composizione da una raccolta gerarchica di oggetti visivi denominata struttura *ad albero visuale.* L'oggetto visivo alla radice di  un albero è detto oggetto visivo radice e può avere uno o più *oggetti visivi* figlio associati. Un oggetto visivo figlio può avere uno o più oggetti visivi figlio propri. Qualsiasi oggetto visivo a cui sono associati oggetti visivi figlio viene chiamato oggetto visivo padre e tutti gli oggetti visivi figlio che condividono lo stesso oggetto visivo padre sono denominati *oggetti visivi di pari livello.* Un oggetto visivo specifico insieme a tutti gli oggetti visivi figlio e discendenti è detto *sottoalbero visivo*.

La posizione di un oggetto visivo nell'albero consente di determinare la posizione dello schermo e l'ordine z rispetto agli altri oggetti visivi nella composizione. L'oggetto visivo radice viene posizionato rispetto all'angolo superiore sinistro dell'area client della finestra di destinazione in cui viene eseguito il rendering della composizione. Tutti gli oggetti visivi figlio vengono posizionati in relazione all'angolo superiore sinistro dell'oggetto visivo padre (o all'oggetto visivo specificato dalla proprietà TransformParent) e vengono sempre visualizzati davanti all'oggetto padre nell'ordine z.

La figura seguente illustra una composizione di oggetti visivi e la struttura della struttura ad albero visuale usata per produrre la composizione. L'oggetto visivo 1 è l'oggetto visivo radice ed è anche l'elemento padre degli oggetti visivi figlio 2 e 3, che sono oggetti visivi di pari livello. L'oggetto visivo 3 ha due oggetti visivi figlio propri, Gli oggetti visivi 4 e 5. Insieme, gli oggetti visivi da 3 a 5 costituiscono un sottoalbero visivo.

![una composizione di oggetti visivi e la struttura ad albero visuale corrispondente](images/visuals-and-corresponding-tree.png)

Un oggetto visivo padre gestisce un elenco ordinato degli oggetti visivi figlio. Quando gli oggetti visivi di pari livello sono posizionati in modo che si sovrappongano tra loro, DirectComposition imposta l'ordine z degli oggetti visivi di pari livello in base all'ordine in cui vengono visualizzati nell'elenco degli elementi figlio dell'oggetto visivo padre. Un elemento di pari livello visualizzato più avanti nell'elenco viene posizionato davanti a tutti gli elementi di pari livello visualizzati in precedenza nell'elenco. La figura seguente mostra l'ordine z degli oggetti visivi figlio sovrapposti.

![ordine z degli oggetti visivi figlio sovrapposti](images/overlapping-child-visuals.png)

### <a name="properties-of-a-visual-object"></a>Proprietà di un oggetto visivo

Un oggetto visivo espone un set di proprietà che consentono di impostare il contenuto bitmap per l'oggetto visivo e di controllare il modo in cui DirectComposition posiziona e modifica il contenuto visivo. Le sezioni seguenti descrivono ogni proprietà in dettaglio.

-   [Proprietà di contenuto](#content-property)
-   [Clip - proprietà](#clip-property)
-   [BorderMode - proprietà](#bordermode-property)
-   [BitmapInterpolationMode - proprietà](#bitmapinterpolationmode-property)
-   [Proprietà CompositeMode](#compositemode-property)
-   [Proprietà OffsetX e OffsetY](#offsetx-and-offsety-properties)
-   [Proprietà Effect](#effect-property)
-   [Transform (proprietà)](#transform-property)
-   [Proprietà TransformParent](#transformparent-property)

### <a name="content-property"></a>Proprietà di contenuto

La proprietà Content di un oggetto visivo specifica il contenuto bitmap associato all'oggetto visivo. Si tratta della bitmap utilizzata da DirectComposition quando si include l'oggetto visivo in una composizione.

Impostare la proprietà Content di un oggetto visivo chiamando il [**metodo IDCompositionVisual::SetContent.**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setcontent)

Per altre informazioni sui tipi di contenuto bitmap supportati da DirectComposition, vedere [Oggetti bitmap](bitmap-surfaces.md).

### <a name="clip-property"></a>Clip - proprietà

La proprietà Clip di un oggetto visivo specifica un'area rettangolare denominata area *di ritaglio* (o rettangolo *di ritaglio).* Quando viene eseguito il rendering di un oggetto visivo, viene visualizzata solo la parte dell'oggetto visivo che si trova all'interno dell'area di ritaglio, mentre qualsiasi contenuto che si estende all'esterno dell'area di ritaglio viene ritagliato, ovvero non visualizzato. DirectComposition supporta aree di ritaglio con angoli arrotondati o quadrati.

Per impostare la proprietà Clip di un oggetto visivo, chiamare il [**metodo IDCompositionVisual::SetClip.**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setclip(constd2d_rect_f_))

Per altre informazioni, vedere [Ritaglio.](clipping.md)

### <a name="bordermode-property"></a>BorderMode - proprietà

La proprietà BorderMode specifica come comporre i bordi delle bitmap e delle clip associate a questo oggetto visivo o con oggetti visivi nel sottoalbero con radice in questo oggetto visivo.

La modalità bordo influisce sulla composizione dei bordi di una bitmap quando la bitmap viene trasformata in modo che i bordi non siano allineati all'asse con le coordinate intere. Influisce anche sul modo in cui il contenuto viene ritagliato agli angoli di una clip con angoli arrotondati e sul bordo di una clip trasformata in modo che i bordi non siano allineati all'asse con le coordinate intere.

Per altre informazioni, vedere [**IDCompositionVisual::SetBorderMode**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setbordermode).

### <a name="bitmapinterpolationmode-property"></a>BitmapInterpolationMode - proprietà

La proprietà BitmapInterpolationMode indica a DirectComposition come comporre una bitmap quando viene trasformata in modo che non vi sia corrispondenza uno-a-uno tra i pixel nella bitmap e i pixel sullo schermo.

Impostare la proprietà BitmapInterpolationMode di un oggetto visivo chiamando il [**metodo IDCompositionVisual::SetBitmapInterpolationMode.**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setbitmapinterpolationmode)

### <a name="compositemode-property"></a>Proprietà CompositeMode

La proprietà CompositeMode indica a DirectComposition come unire il contenuto bitmap di un oggetto visivo con la destinazione di rendering. Per una descrizione delle modalità composite supportate, vedere [**DCOMPOSITION \_ COMPOSITE \_ MODE**](/windows/desktop/api/DcompTypes/ne-dcomptypes-dcomposition_composite_mode).

Impostare la proprietà CompositeMode di un oggetto visivo chiamando il [**metodo IDCompositionVisual::SetCompositeMode.**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setcompositemode)

### <a name="offsetx-and-offsety-properties"></a>Proprietà OffsetX e OffsetY

Le proprietà OffsetX e OffsetY indicano a DirectComposition dove posizionare un oggetto visivo orizzontalmente e verticalmente. Definiscono la posizione fissa bidimensionale da cui vengono calcolati tutti gli effetti e le trasformazioni per l'oggetto visivo.

Per un oggetto visivo radice, le proprietà OffsetX e OffsetY definiscono la coordinata x e y di un punto rispetto all'angolo superiore sinistro della finestra che ospita l'oggetto visivo. Per un oggetto visivo figlio, le coordinate sono relative all'angolo superiore sinistro dell'oggetto visivo padre o, se viene specificata la proprietà [TransformParent,](#transformparent-property) all'angolo superiore sinistro dell'oggetto visivo specificato. Quando viene eseguito il rendering di un oggetto visivo, viene posizionato in modo che l'angolo superiore sinistro dell'oggetto visivo coincida con le coordinate specificate.

Impostare le proprietà OffsetX e OffsetY di un oggetto visivo chiamando i metodi [**IDCompositionVisual::SetOffsetX**](/previous-versions/windows/desktop/legacy/hh449126(v=vs.85)) [**e SetOffsetY.**](/previous-versions/windows/desktop/legacy/hh449131(v=vs.85))

### <a name="effect-property"></a>Proprietà Effect

La proprietà Effect consente di specificare un effetto, o gruppo di effetti, che modificherà la composizione di un oggetto visivo e del relativo sottoalbero. Ad esempio, è possibile specificare gli effetti che controllano l'opacità di un oggetto visivo, unire l'oggetto visivo a un'altra bitmap in vari modi e applicare trasformazioni prospettica all'oggetto visivo.

Impostare la proprietà Effect di un oggetto visivo chiamando il [**metodo IDCompositionVisual::SetEffect.**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-seteffect)

Per altre informazioni, vedere [Effects](effects.md) (Effetti).

### <a name="transform-property"></a>Transform (proprietà)

La proprietà Transform specifica una trasformazione bidimensionale (2D), o gruppo di trasformazioni 2D, che DirectComposition deve eseguire sull'oggetto visivo. Una trasformazione (o trasformazione) è un'operazione che modifica il sistema di coordinate di un oggetto visivo rispetto all'oggetto padre o rispetto all'oggetto visivo specificato dalla [proprietà TransformParent](#transformparent-property). È possibile usare le trasformazioni per modificare la posizione, le dimensioni o la natura di un oggetto visivo spostarlo in un'altra posizione (traslazione), renderlo più grande o più piccolo (ridimensionamento), ruotarlo (rotazione), distorcerne la forma (inclinazione) e così via.

Impostare la proprietà Transform di un oggetto visivo chiamando il [**metodo IDCompositionVisual::SetTransform.**](/previous-versions/windows/desktop/legacy/hh449178(v=vs.85))

Per altre informazioni, vedere [Trasformazioni](transforms.md).

### <a name="transformparent-property"></a>Proprietà TransformParent

Il sistema di coordinate di un oggetto visivo viene modificato dalle proprietà OffsetX, OffsetY e Transform. In genere, queste proprietà definiscono il sistema di coordinate di un oggetto visivo rispetto all'elemento padre immediato. Per usare un oggetto visivo diverso dall'oggetto padre come base per il sistema di coordinate di un oggetto visivo figlio, usare la proprietà TransformParent per specificare un oggetto visivo diverso come "padre" ai fini della trasformazione.

Impostare la proprietà TransformParent di un oggetto visivo chiamando il [**metodo IDCompositionVisual::SetTransformParent.**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-settransformparent)

## <a name="device-object"></a>Oggetto dispositivo

Per usare DirectComposition, è necessario creare e modificare un'ampia gamma di Component Object Model (COM). Il primo oggetto che è necessario creare  è l'oggetto dispositivo DirectComposition perché funge da factory per la creazione di tutti gli altri oggetti usati in una composizione.

Per creare un oggetto dispositivo, chiamare la [**funzione DCompositionCreateDevice,**](/windows/desktop/api/Dcomp/nf-dcomp-dcompositioncreatedevice) che restituisce un puntatore a [**interfaccia IDCompositionDevice.**](/windows/win32/api/dcomp/nn-dcomp-idcompositiondevice) Questa interfaccia espone un set di metodi che consentono di creare oggetti visivi, oggetti clip, oggetti di animazione, oggetti di trasformazione, oggetti effetto e così via.

L'oggetto dispositivo serve a un altro scopo oltre a essere una factory per la creazione di altri oggetti. Espone un metodo denominato [**Commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit) che passa una struttura ad albero visuale a DirectComposition per l'elaborazione. Per altre informazioni, vedere [Composizione transazionale.](#transactional-composition)

Tenere presente che, anche se è possibile creare più istanze dell'oggetto dispositivo nell'applicazione, tutti gli oggetti utilizzati in una particolare composizione devono essere creati dallo stesso oggetto dispositivo, con una sola eccezione: è possibile combinare oggetti visivi da oggetti dispositivo diversi nella stessa struttura ad albero visuale. In questo caso, DirectComposition considera la struttura ad albero visuale come farebbe normalmente, ad eccezione del fatto che le modifiche apportate a un particolare oggetto visivo nella struttura ad albero hanno effetto solo quando viene chiamato il metodo [**Commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit) sull'oggetto dispositivo che ha creato l'oggetto visivo.

La possibilità di usare oggetti visivi di dispositivi diversi nella stessa struttura ad albero visuale consente a più thread di creare e modificare una singola struttura ad albero visuale mantenendo due dispositivi indipendenti che possono essere usati per eseguire il commit delle modifiche in modo asincrono. Per altre informazioni, vedere Alberi degli oggetti [visivi tra dispositivi](#cross-device-visual-trees).

## <a name="composition-target-window"></a>Finestra di destinazione della composizione

Una struttura ad albero visuale deve essere associata a una finestra prima che uno degli oggetti visivi dell'albero possa essere visualizzato sullo schermo. La finestra, denominata finestra *di destinazione della composizione,* può essere una finestra di primo livello o una finestra figlio. Inoltre, la finestra di destinazione della composizione può essere una finestra a più livelli. ciò significa che può avere lo stile di finestra [**WS \_ EX a \_ livelli.**](/windows/desktop/winmsg/extended-window-styles)

DirectComposition consente a un'applicazione di associare un massimo di due alberi visivi a ogni finestra. Gli alberi visivi includono una che è composta sopra la finestra stessa, ma dietro tutte le finestre figlio della finestra e un'altra che è composta sopra la finestra e sopra le finestre figlio. In altre parole, ogni finestra ha quattro livelli concettuali e tutti i livelli vengono ritagliati nell'area visibile della finestra di destinazione. La figura seguente illustra i quattro livelli concettuali di una finestra.

![livelli concettuali di una finestra](images/directcomposition-layers.png)

## <a name="transactional-composition"></a>Composizione transazionale

DirectComposition usa un modello transazionale in cui si crea un set in batch di modifiche a un oggetto visivo e quindi si esegue il commit del set su DirectComposition per l'elaborazione in una sola volta. È possibile modificare lo stesso oggetto visivo DirectComposition ed eseguire il commit delle modifiche per un numero qualsiasi di volte. Quando il Gestione finestre desktop (DWM) raccoglie i batch, raccoglie tutti i batch in sospeso e li applica al frame successivo nell'ordine in cui sono stati emessi.

Tutte le modifiche all'interno di un singolo commit vengono applicate a un singolo frame. Poiché DWM raccoglie batch una sola volta per ogni frame, è possibile modificare qualsiasi oggetto specifico una sola volta per ogni frame. Anche i commit successivi che modificano oggetti diversi possono essere applicati al frame corrente, ma DirectComposition non garantisce che le modifiche si verificheranno nello stesso frame.

I [**metodi IDCompositionSurface::BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw) e [**IDCompositionSurface::EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw) consentono di sincronizzare gli aggiornamenti del rendering con gli aggiornamenti visivi. Ad esempio, è possibile chiamare **IDCompositionSurface::BeginDraw,** aggiornare le proprietà OffsetX e Clip di un oggetto visivo, chiamare [**IDCompositionDevice::Commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit), disegnare contenuto con Microsoft DirectX e quindi **chiamare IDCompositionSurface::EndDraw**. In questo caso, Microsoft DirectComposition garantisce che il contenuto bitmap e le proprietà visive siano aggiornati contemporaneamente.

### <a name="batching"></a>Creazione di batch

È possibile eseguire il commit di più modifiche nello stesso oggetto visivo o di più modifiche a oggetti visivi diversi, all'interno dello stesso frame. Quando si apportano più modifiche allo stesso oggetto visivo all'interno dello stesso frame, tenere presenti i punti seguenti:

-   Se si apportano più modifiche alla stessa proprietà di un oggetto visivo, viene applicata solo l'ultima modifica. Ad esempio, se si imposta l'opacità su 0, quindi su 0,5 e infine su 1,0, all'oggetto visivo viene applicata solo un'opacità di 1,0.
-   Se si modificano più proprietà dello stesso oggetto visivo, DirectComposition applica prima le modifiche all'oggetto visivo e quindi a tutti gli oggetti visivi figlio. Le proprietà vengono applicate nell'ordine seguente indipendentemente dall'ordine in cui vengono specificate:

    1.  Offset
    2.  Trasformazione
    3.  Ritaglia
    4.  Effetto

    La figura seguente mostra il risultato dell'applicazione di tutte e quattro le proprietà a un oggetto visivo.

    ![risultato dell'applicazione di tutte e quattro le proprietà a un oggetto visivo](images/order-of-properties.png)

    Tenere presente che tutte le modifiche vengono applicate contemporaneamente all'oggetto visivo all'interno del contesto dello stesso frame. Ciò significa che, dal punto di vista dell'utente, le modifiche all'oggetto visivo si verificano immediatamente.

-   Per la proprietà Transform è possibile usare [**IDCompositionDevice::CreateTransformGroup**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtransformgroup) per creare un gruppo di trasformazioni da applicare a un oggetto visivo contemporaneamente. DirectComposition applica le trasformazioni nell'ordine specificato.
-   Per la proprietà Effect è possibile usare [**IDCompositionEffectGroup**](/windows/win32/api/dcomp/nn-dcomp-idcompositioneffectgroup) per applicare un gruppo di effetti. DirectComposition applica gli effetti nell'ordine specificato. Inoltre, le trasformazioni della prospettiva 3D comportano l'appiattimento della struttura ad albero visuale dopo l'applicazione di tutte le trasformazioni 3D nell'oggetto visivo corrente. In questo modo si garantisce che l'oggetto visivo risultante sia il più vicino possibile al 3D.

### <a name="synchronization"></a>Sincronizzazione

L'applicazione può chiamare DirectComposition da più thread contemporaneamente. L'ordine di esecuzione è garantito per le chiamate sequenziali, ma non per le chiamate simultanee. Ad esempio, se il thread A modifica un oggetto visivo e il thread B esegue il commit del batch contemporaneamente, non è definito se tale modifica visiva è inclusa nel batch di cui è stato eseguito il commit o se avvia un nuovo batch. D'altra parte, se l'applicazione usa altri meccanismi di sincronizzazione per garantire che un metodo venga chiamato prima dell'altro, DirectComposition rispetta l'ordine di chiamata e li elabora come se entrambe le chiamate fossero state emesse in tale ordine da un singolo thread.

### <a name="cross-device-visual-trees"></a>Alberi visivi tra dispositivi

Gli oggetti DirectComposition non sono associati a thread. è possibile usare più thread per modificare lo stesso set di oggetti. Tenere tuttavia presenti i problemi seguenti quando si condivide lo stesso oggetto dispositivo.

-   Entrambi i thread devono essere in grado di chiamare [**IDCompositionDevice::Commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit). Se solo uno dei thread chiama **IDCompositionDevice::Commit,** l'altro thread non può eseguire il commit delle modifiche apportate a DirectComposition.
-   Il comportamento transazionale potrebbe andare perso se un thread chiama [**IDCompositionDevice::Commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit) mentre l'altro thread sta ancora apportando modifiche che devono far parte della stessa transazione.

Se è necessario eseguire il commit di più transazioni simultanee in DirectComposition, è necessario usare più oggetti dispositivo, possibilmente da più thread. In questo scenario, la stessa struttura ad albero visuale è condivisa da entrambi gli oggetti dispositivo e ogni oggetto dispositivo esegue il commit delle proprie transazioni.

La figura seguente mostra una struttura ad albero visuale condivisa da due oggetti dispositivo. Gli oggetti visivi 1, 2, 4 e 5 sono di proprietà di un dispositivo o dell'altro, ma l'oggetto visivo 3 è condiviso da entrambi i dispositivi e può quindi essere usato per connettere due sottoalto in un singolo albero visivo più grande. La condivisione dell'albero visuale consente ai due dispositivi di essere manipolati da due thread diversi in modo asincrono.

![una struttura ad albero visuale condivisa da due dispositivi](images/shared-visual-tree-1.png)

Per illustrare l'utilità della condivisione di una struttura ad albero visuale tra due dispositivi, prendere in considerazione un'architettura che consente l'input tocco a bassa latenza. L'architettura può usare due thread, uno che gestisce la maggior parte delle attività dell'interfaccia utente e un secondo thread dedicato all'elaborazione degli eventi di input tocco. Il thread di tocco aggiorna la trasformazione di un oggetto visivo specifico in base al movimento di input dell'utente. Aggiornando la trasformazione, il thread di tocco può fare in modo che l'intero sottoalbero sotto l'oggetto visivo segua il dito dell'utente, la scalabilità verso l'alto o verso il basso quando l'utente esegue un movimento multitocchetto e così via. Il thread dell'interfaccia utente mantiene la proprietà della maggior parte dell'albero della composizione, con il thread di tocco proprietario solo dei pochi oggetti visivi contrassegnati per la risposta tocco asincrona. La figura seguente mostra una versione semplificata di un albero di composizione di questo tipo:

![una struttura ad albero visuale condivisa tra un thread dell'interfaccia utente e un thread di tocco](images/shared-visual-tree-2.png)

In genere, il thread dell'interfaccia utente modifica solo gli oggetti visivi di cui è proprietario esclusivamente e il thread di tocco modifica solo l'oggetto visivo condiviso. L'unica eccezione si verifica quando si crea o si elimina un sottoalbero abilitato per il tocco.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IDCompositionSurface::BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw)
</dt> <dt>

[**IDCompositionSurface::EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw)
</dt> <dt>

[**IDCompositonDevice::Commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit)
</dt> <dt>

[Concetti relativi a DirectComposition](directcomposition-concepts.md)
</dt> </dl>

 

 