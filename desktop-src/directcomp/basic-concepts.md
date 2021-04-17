---
title: Concetti di base (DirectComposition)
description: Questo argomento fornisce una panoramica dei concetti di base di Microsoft DirectComposition.
ms.assetid: F442BDCA-C913-4438-BFFA-D3F28B68EE85
keywords:
- Concetti di DirectComposition
- Concetti di base di DirectComposition
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0550dc12cb0dcc5262701658d8e3883ee1ce8d82
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/20/2020
ms.locfileid: "104559680"
---
# <a name="basic-concepts"></a>Concetti fondamentali

> [!NOTE]
> Per le app in Windows 10, è consigliabile usare le API Windows. UI. Composition anziché DirectComposition. Per altre informazioni, vedere [modernizzare l'app desktop usando il livello visivo](/windows/uwp/composition/visual-layer-in-desktop-apps).

Questo argomento fornisce una panoramica dei concetti di base di Microsoft DirectComposition. Contiene le sezioni seguenti:

-   [Composizione](#composition-target-window)
-   [Oggetti visivi](#visuals)
    -   [Struttura ad albero visuale](#visual-tree)
    -   [Proprietà di un oggetto visivo](#properties-of-a-visual-object)
-   [Oggetto dispositivo](#device-object)
-   [Finestra di destinazione composizione](#composition-target-window)
-   [Composizione transazionale](#transactional-composition)
    -   [Batch](#batching)
    -   [Sincronizzazione](#synchronization)
    -   [Alberi visivi tra dispositivi](#cross-device-visual-trees)
-   [Argomenti correlati](#related-topics)

## <a name="composition"></a>Composizione

DirectComposition definisce una *composizione* come raccolta di bitmap combinate e modificate applicando varie trasformazioni, effetti e animazioni per produrre un risultato visivo in un'interfaccia utente dell'applicazione. DirectComposition funziona solo con contenuto bitmap. non supporta vettori o testo. DirectComposition non fornisce contenuto bitmap. Fornisce invece interfacce in cui gli utenti possono creare con D2D, DXGI o caricare il proprio contenuto di trama.

Un'applicazione DirectComposition crea due set di oggetti per comporre una scena: bitmap composte insieme e oggetti visivi che definiscono le relazioni spaziali tra le bitmap. Per ulteriori informazioni sugli oggetti bitmap supportati da DirectComposition, vedere [oggetti bitmap](bitmap-surfaces.md).

## <a name="visuals"></a>Oggetti visivi

Gli oggetti *visivi* (o *oggetti visivi*) sono gli elementi fondamentali di DirectComposition. Si tratta dei blocchi predefiniti di base usati per creare composizioni e animazioni nell'interfaccia utente dell'applicazione.

In termini di programmazione, un oggetto visivo è un oggetto che dispone di un set di proprietà ed espone un'interfaccia utilizzata per impostare il valore delle proprietà. La proprietà Content di un oggetto visivo associa una particolare bitmap all'oggetto visivo, mentre altre proprietà controllano il modo in cui DirectComposition posiziona e modifica l'oggetto visivo mentre viene sottoposto a rendering sullo schermo.

Per ulteriori informazioni, vedere [proprietà di un oggetto visivo](#properties-of-a-visual-object).

### <a name="visual-tree"></a>Struttura ad albero visuale

DirectComposition crea una composizione da una raccolta gerarchica di oggetti visivi denominata *struttura ad albero visuale*. L'oggetto visivo alla radice di un albero è denominato oggetto *visivo radice* e può essere associato a uno o più oggetti *visivi figlio* . Un oggetto visivo figlio può avere uno o più oggetti visivi figlio. Tutti gli oggetti visivi associati agli oggetti visivi figlio vengono chiamati oggetti *visivi padre* e tutti gli oggetti visivi figlio che condividono lo stesso elemento padre vengono chiamati oggetti *visivi di pari livello*. Un oggetto visivo particolare insieme a tutti gli oggetti visivi figlio e discendente viene definito *sottoalbero visuale*.

La posizione di un oggetto visivo nell'albero consente di determinare la posizione dello schermo e l'ordine z rispetto agli altri oggetti visivi nella composizione. L'oggetto visivo radice è posizionato in relazione all'angolo superiore sinistro dell'area client della finestra di destinazione in cui viene eseguito il rendering della composizione. Tutti gli oggetti visivi figlio sono posizionati in relazione all'angolo superiore sinistro dell'oggetto visivo padre (o all'oggetto visivo specificato dalla proprietà TransformParent) e vengono sempre visualizzati davanti all'elemento padre nell'ordine z.

Nella figura seguente viene illustrata una composizione di oggetti visivi e la struttura della struttura ad albero visuale utilizzata per produrre la composizione. Visual 1 è l'oggetto visivo radice ed è anche il padre degli oggetti visivi figlio 2 e 3, che sono oggetti visivi di pari livello. Visual 3 presenta due oggetti visivi figlio, gli oggetti visivi 4 e 5. Insieme, gli oggetti visivi da 3 a 5 costituiscono un sottoalbero visuale.

![composizione di oggetti visivi e della struttura ad albero visuale corrispondente](images/visuals-and-corresponding-tree.png)

Un oggetto visivo padre gestisce un elenco ordinato di oggetti visivi figlio. Quando gli oggetti visivi di pari livello vengono posizionati in modo che si sovrappongano tra loro, DirectComposition imposta l'ordine z degli elementi di pari livello in base all'ordine in cui vengono visualizzati nell'elenco elementi figlio dell'oggetto visivo padre. Un elemento di pari livello visualizzato più avanti nell'elenco viene inserito davanti a tutti gli elementi di pari livello indicati in precedenza nell'elenco. Nella figura seguente viene illustrato l'ordine z degli oggetti visivi figlio sovrapposti.

![ordine z degli oggetti visivi figlio sovrapposti](images/overlapping-child-visuals.png)

### <a name="properties-of-a-visual-object"></a>Proprietà di un oggetto visivo

Un oggetto visivo espone un set di proprietà che consentono di impostare il contenuto della bitmap per l'oggetto visivo e di controllare il modo in cui DirectComposition posiziona e manipola il contenuto visivo. Nelle sezioni seguenti vengono descritte in dettaglio le singole proprietà.

-   [Proprietà di contenuto](#content-property)
-   [Clip (proprietà)](#clip-property)
-   [Proprietà BorderMode](#bordermode-property)
-   [Proprietà BitmapInterpolationMode](#bitmapinterpolationmode-property)
-   [Proprietà CompositeMode](#compositemode-property)
-   [Proprietà OffsetX e OffsetY](#offsetx-and-offsety-properties)
-   [Proprietà Effect](#effect-property)
-   [Transform (proprietà)](#transform-property)
-   [Proprietà TransformParent](#transformparent-property)

### <a name="content-property"></a>Proprietà di contenuto

La proprietà Content di un oggetto visivo specifica il contenuto della bitmap associato all'oggetto visivo. Si tratta della bitmap utilizzata da DirectComposition quando si include l'oggetto visivo in una composizione.

Per impostare la proprietà Content di un oggetto visivo, chiamare il metodo [**IDCompositionVisual::**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setcontent) SetValue.

Per ulteriori informazioni sui tipi di contenuto bitmap supportati da DirectComposition, vedere [oggetti bitmap](bitmap-surfaces.md).

### <a name="clip-property"></a>Clip (proprietà)

La proprietà clip di un oggetto visivo specifica un'area rettangolare denominata area di *ridimensionamento* (o *rettangolo* di ritaglio). Quando viene eseguito il rendering di un oggetto visivo, viene visualizzata solo la parte dell'oggetto visivo che si trova all'interno dell'area di visualizzazione, mentre qualsiasi contenuto che si estende al di fuori dell'area di visualizzazione viene ritagliato, ovvero non viene visualizzato. DirectComposition supporta le aree di ritaglio con angoli arrotondati o quadrati.

Per impostare la proprietà clip di un oggetto visivo, chiamare il metodo [**IDCompositionVisual:: seclip**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setclip(constd2d_rect_f_)) .

Per ulteriori informazioni, vedere [ritaglio](clipping.md).

### <a name="bordermode-property"></a>Proprietà BorderMode

La proprietà BorderMode specifica come comporre i bordi delle bitmap e delle clip associate a questo oggetto visivo o con gli oggetti visivi nel sottoalbero radice in questo oggetto visivo.

La modalità bordo influiscono sul modo in cui vengono composti i bordi di una bitmap quando la bitmap viene trasformata in modo tale che i bordi non siano allineati all'asse con le coordinate di tipo Integer. Influiscono inoltre sul modo in cui il contenuto viene ritagliato negli angoli di una clip con angoli arrotondati e al bordo di una clip trasformata in modo tale che i bordi non siano allineati all'asse con le coordinate di tipo Integer.

Per ulteriori informazioni, vedere [**IDCompositionVisual:: SetBorderMode**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setbordermode).

### <a name="bitmapinterpolationmode-property"></a>Proprietà BitmapInterpolationMode

La proprietà BitmapInterpolationMode indica a DirectComposition come comporre una bitmap quando viene trasformata in modo che non esista una corrispondenza uno-a-uno tra i pixel nella bitmap e i pixel sullo schermo.

Per impostare la proprietà BitmapInterpolationMode di un oggetto visivo, chiamare il metodo [**IDCompositionVisual:: SetBitmapInterpolationMode**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setbitmapinterpolationmode) .

### <a name="compositemode-property"></a>Proprietà CompositeMode

La proprietà CompositeMode indica a DirectComposition come unire il contenuto bitmap di un oggetto visivo con la destinazione di rendering. Per una descrizione delle modalità composite supportate, vedere [**\_ \_ modalità composita DCOMPOSITION**](/windows/desktop/api/DcompTypes/ne-dcomptypes-dcomposition_composite_mode).

Per impostare la proprietà CompositeMode di un oggetto visivo, chiamare il metodo [**IDCompositionVisual:: SetCompositeMode**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setcompositemode) .

### <a name="offsetx-and-offsety-properties"></a>Proprietà OffsetX e OffsetY

Le proprietà OffsetX e OffsetY indicano a DirectComposition dove posizionare un oggetto visivo orizzontalmente e verticalmente. Definiscono la posizione fissa bidimensionale dalla quale vengono calcolate tutte le trasformazioni e gli effetti per l'oggetto visivo.

Per un oggetto visivo radice, le proprietà OffsetX e OffsetY definiscono la coordinata x e la coordinata y di un punto rispetto all'angolo superiore sinistro della finestra che ospita l'oggetto visivo. Per un oggetto visivo figlio, le coordinate sono relative all'angolo superiore sinistro dell'elemento padre o, se viene specificata la [Proprietà TransformParent](#transformparent-property) , l'angolo superiore sinistro dell'oggetto visivo specificato. Quando viene eseguito il rendering di un oggetto visivo, questo viene posizionato in modo tale che l'angolo superiore sinistro dell'oggetto visivo coincida con le coordinate specificate.

Per impostare le proprietà OffsetX e OffsetY di un oggetto visivo, chiamare i metodi [**IDCompositionVisual:: SetOffsetX**](/previous-versions/windows/desktop/legacy/hh449126(v=vs.85)) e [**seoffsety**](/previous-versions/windows/desktop/legacy/hh449131(v=vs.85)) .

### <a name="effect-property"></a>Proprietà Effect

La proprietà Effect consente di specificare un effetto o un gruppo di effetti che modifica il modo in cui viene composto un oggetto visivo e il relativo sottoalbero. Ad esempio, è possibile specificare gli effetti che controllano l'opacità di un oggetto visivo, combinano l'oggetto visivo con un'altra bitmap in diversi modi e applicano le trasformazioni della prospettiva all'oggetto visivo.

Per impostare la proprietà Effect di un oggetto visivo, chiamare il metodo [**IDCompositionVisual:: seeffect**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-seteffect) .

Per altre informazioni, vedere [Effects](effects.md) (Effetti).

### <a name="transform-property"></a>Transform (proprietà)

La proprietà Transform specifica una trasformazione bidimensionale (2D), o un gruppo di trasformazioni 2D, per l'esecuzione di DirectComposition sull'oggetto visivo. Una trasformazione (o trasformazione) è un'operazione che modifica il sistema di coordinate di un oggetto visivo rispetto al relativo padre o relativo all'oggetto visivo specificato dalla [Proprietà TransformParent](#transformparent-property). È possibile utilizzare le trasformazioni per modificare la posizione, le dimensioni o la natura di un oggetto visivo spostando l'oggetto in un altro percorso (conversione), rendendolo più grande o più piccolo (ridimensionamento), trasformandolo (rotazione), distorsione della forma (inclinazione) e così via.

Per impostare la proprietà Transform di un oggetto visivo, chiamare il metodo [**IDCompositionVisual:: setransform**](/previous-versions/windows/desktop/legacy/hh449178(v=vs.85)) .

Per altre informazioni, vedere [Trasformazioni](transforms.md).

### <a name="transformparent-property"></a>Proprietà TransformParent

Il sistema di coordinate di un oggetto visivo viene modificato dalle proprietà OffsetX, OffsetY e Transform. In genere, queste proprietà definiscono il sistema di coordinate di un oggetto visivo rispetto al relativo elemento padre diretto. Per utilizzare alcuni oggetti visivi diversi dall'elemento padre come base per il sistema di coordinate di un oggetto visivo figlio, utilizzare la proprietà TransformParent per specificare un oggetto visivo diverso come "padre" per finalità di trasformazione.

Per impostare la proprietà TransformParent di un oggetto visivo, chiamare il metodo [**IDCompositionVisual:: SetTransformParent**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-settransformparent) .

## <a name="device-object"></a>Oggetto dispositivo

Per utilizzare DirectComposition, è necessario creare e modificare un'ampia gamma di oggetti Component Object Model (COM). Il primo oggetto che è necessario creare è l' *oggetto dispositivo* DirectComposition, perché funge da Factory per la creazione di tutti gli altri oggetti utilizzati in una composizione.

Per creare un oggetto dispositivo, chiamare la funzione [**DCompositionCreateDevice**](/windows/desktop/api/Dcomp/nf-dcomp-dcompositioncreatedevice) , che restituisce un puntatore a interfaccia [**IDCompositionDevice**](/windows/win32/api/dcomp/nn-dcomp-idcompositiondevice) . Questa interfaccia espone un set di metodi usati per creare oggetti visivi, ritagliare oggetti, oggetti animazione, oggetti Transform, oggetti Effect e così via.

L'oggetto dispositivo serve un altro scopo oltre a essere una factory per la creazione di altri oggetti. Espone un metodo denominato [**commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit) che passa una struttura ad albero visuale a DirectComposition per l'elaborazione. Per ulteriori informazioni, vedere [composizione transazionale](#transactional-composition).

Tenere presente che, sebbene sia possibile creare più istanze dell'oggetto dispositivo nell'applicazione, tutti gli oggetti utilizzati in una determinata composizione devono essere creati dallo stesso oggetto dispositivo, con una sola eccezione: è possibile combinare oggetti visivi da oggetti dispositivo diversi nella stessa struttura ad albero visuale. Quando si esegue questa operazione, DirectComposition considera la struttura ad albero visuale come in genere, ad eccezione del fatto che le modifiche apportate a un determinato oggetto visivo nell'albero diventano effettive solo quando il metodo [**commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit) viene chiamato sull'oggetto dispositivo che ha creato l'oggetto visivo.

La possibilità di usare oggetti visivi di dispositivi diversi nella stessa struttura ad albero visuale consente a più thread di creare e modificare una singola struttura ad albero visuale mantenendo due dispositivi indipendenti che possono essere usati per eseguire il commit delle modifiche in modo asincrono. Per altre informazioni, vedere [alberi visivi tra dispositivi](#cross-device-visual-trees).

## <a name="composition-target-window"></a>Finestra di destinazione composizione

Una struttura ad albero visuale deve essere associata a una finestra prima che uno degli oggetti visivi dell'albero possa essere visualizzato sullo schermo. La finestra, denominata *finestra di destinazione della composizione*, può essere una finestra di primo livello o una finestra figlio. Inoltre, la finestra di destinazione della composizione può essere una finestra sovrapposta. ovvero, può avere lo stile della finestra [**WS ex a più \_ \_ livelli**](/windows/desktop/winmsg/extended-window-styles) .

DirectComposition consente a un'applicazione di associare un massimo di due alberi visivi a ogni finestra. Gli alberi visivi includono uno che viene composto nella parte superiore della finestra stessa, ma dietro tutte le finestre figlio della finestra e un altro composto nella parte superiore della finestra e nella parte superiore delle finestre figlio. In altre parole, ogni finestra dispone di quattro livelli concettuali e tutti i livelli vengono ritagliati nell'area visibile della finestra di destinazione. Nella figura seguente sono illustrati i quattro livelli concettuali di una finestra.

![livelli concettuali di una finestra](images/directcomposition-layers.png)

## <a name="transactional-composition"></a>Composizione transazionale

DirectComposition usa un modello transazionale in cui si crea un set di modifiche in batch in un oggetto visivo e quindi si esegue il commit del set in DirectComposition per l'elaborazione in una sola volta. È possibile modificare lo stesso oggetto visivo DirectComposition ed eseguire il commit delle modifiche per un numero qualsiasi di volte. Quando il Gestione finestre desktop (DWM) preleva batch, preleva tutti i batch in sospeso e li applica al frame successivo nell'ordine in cui sono stati sottoposte a commit.

Tutte le modifiche all'interno di un singolo commit sono sicuramente applicabili a un singolo frame. Poiché DWM raccoglie batch una volta per ogni fotogramma, è possibile modificare qualsiasi oggetto specifico solo una volta per fotogramma. I commit successivi che modificano oggetti diversi possono anche essere applicati al frame corrente, ma DirectComposition non garantisce che le modifiche vengano eseguite nello stesso frame.

I metodi [**IDCompositionSurface:: BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw) e [**IDCompositionSurface:: EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw) consentono di sincronizzare gli aggiornamenti del rendering con gli aggiornamenti visivi. Ad esempio, è possibile chiamare **IDCompositionSurface:: BeginDraw**, aggiornare le proprietà OffsetX e clip di un oggetto visivo, chiamare [**IDCompositionDevice:: commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit), creare contenuto con Microsoft DirectX, quindi chiamare **IDCompositionSurface:: EndDraw**. In questo caso, Microsoft DirectComposition garantisce che il contenuto bitmap e le proprietà visive vengano aggiornate contemporaneamente.

### <a name="batching"></a>Creazione di batch

È possibile eseguire il commit di più modifiche nello stesso oggetto visivo o più modifiche a oggetti visivi diversi, all'interno dello stesso frame. Quando si apportano più modifiche allo stesso oggetto visivo nello stesso frame, tenere presenti le considerazioni seguenti:

-   Se si apportano più modifiche alla stessa proprietà di un oggetto visivo, viene applicata solo l'ultima modifica. Se, ad esempio, si imposta l'opacità su 0, quindi su 0,5 e infine su 1,0, all'oggetto visivo viene applicata solo un'opacità 1,0.
-   Se si modificano più proprietà dello stesso oggetto visivo, DirectComposition applica prima le modifiche all'oggetto visivo e quindi agli oggetti visivi figlio. Le proprietà vengono applicate nell'ordine seguente indipendentemente dall'ordine in cui vengono specificate:

    1.  Offset
    2.  Trasformare
    3.  Ritaglia
    4.  Effetto

    Nella figura seguente viene illustrato il risultato dell'applicazione di tutte e quattro le proprietà a un oggetto visivo.

    ![risultato dell'applicazione di tutte e quattro le proprietà a un oggetto visivo](images/order-of-properties.png)

    Tenere presente che tutte le modifiche vengono applicate all'oggetto visivo in una sola volta all'interno del contesto dello stesso frame. Ciò significa che, dal punto di vista dell'utente, le modifiche apportate all'oggetto visivo vengono eseguite immediatamente.

-   Per la proprietà Transform, è possibile usare [**IDCompositionDevice:: CreateTransformGroup**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtransformgroup) per creare un gruppo di trasformazioni da applicare a un oggetto visivo in una sola volta. DirectComposition applica le trasformazioni nell'ordine specificato.
-   Per la proprietà Effect, è possibile usare [**IDCompositionEffectGroup**](/windows/win32/api/dcomp/nn-dcomp-idcompositioneffectgroup) per applicare un gruppo di effetti. DirectComposition applica gli effetti nell'ordine specificato. Inoltre, le trasformazioni della prospettiva 3D comportano l'appiattimento della struttura ad albero visuale dopo l'applicazione di tutte le trasformazioni 3D nell'oggetto visivo corrente. Ciò consente di garantire che l'oggetto visivo risultante risulti più vicino possibile al 3D.

### <a name="synchronization"></a>Sincronizzazione

L'applicazione può chiamare DirectComposition da più thread contemporaneamente. L'ordine di esecuzione è garantito per le chiamate sequenziali, ma non per le chiamate simultanee. Se, ad esempio, il thread A modifica un oggetto visivo e il thread B esegue il commit del batch nello stesso momento, non viene definito se la modifica visiva viene inclusa nel batch di cui è stato eseguito il commit o se viene avviato un nuovo batch. D'altra parte, se l'applicazione usa altri meccanismi di sincronizzazione per assicurarsi che un metodo venga chiamato prima dell'altro, DirectComposition rispetta l'ordine di chiamata e li elabora come se entrambe le chiamate fossero state emesse nell'ordine da un singolo thread.

### <a name="cross-device-visual-trees"></a>Alberi visivi tra dispositivi

Gli oggetti DirectComposition non sono associati al thread; è possibile usare più thread per modificare lo stesso set di oggetti. Tuttavia, tenere presente i seguenti problemi durante la condivisione dello stesso oggetto dispositivo.

-   Entrambi i thread devono essere in grado di chiamare [**IDCompositionDevice:: commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit). Se solo uno dei thread chiama **IDCompositionDevice:: commit**, l'altro thread non può eseguire il commit delle modifiche apportate a DirectComposition.
-   Il comportamento transazionale potrebbe andare perduto se un thread chiama [**IDCompositionDevice:: commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit) mentre l'altro thread continua a apportare modifiche che devono far parte della stessa transazione.

Se è necessario eseguire il commit di più transazioni simultanee in DirectComposition, è necessario usare più oggetti dispositivo, possibilmente da più thread. In questo scenario, la stessa struttura ad albero visuale è condivisa da entrambi gli oggetti dispositivo e ogni oggetto dispositivo effettua il commit delle proprie transazioni.

Nella figura seguente è illustrata una struttura ad albero visuale condivisa da due oggetti dispositivo. Gli oggetti visivi 1, 2, 4 e 5 sono di proprietà di un dispositivo o l'altro, ma Visual 3 è condiviso da entrambi i dispositivi e pertanto può essere usato per connettere due sottoalberi a una singola struttura ad albero visuale più ampia. La condivisione della struttura ad albero visuale consente la manipolazione dei due dispositivi da due thread diversi in modo asincrono.

![una struttura ad albero visuale condivisa da due dispositivi](images/shared-visual-tree-1.png)

Per illustrare l'utilità di condivisione di una struttura ad albero visuale tra due dispositivi, si consideri un'architettura che consente l'input tocco a bassa latenza. L'architettura può usare due thread, uno che gestisce la maggior parte delle attività dell'interfaccia utente e un secondo thread dedicato all'elaborazione degli eventi di input tocco. Il thread tocco aggiorna la trasformazione di un determinato oggetto visivo in base al movimento di input dell'utente. Aggiornando la trasformazione, il thread di tocco può fare in modo che l'intero sottoalbero sotto tale oggetto visivo segua il dito dell'utente, venga scalato verso l'alto o verso il basso quando l'utente esegue un movimento multitocco e così via. Il thread dell'interfaccia utente mantiene la proprietà della maggior parte dell'albero di composizione, con il thread di tocco che possiede solo i pochi oggetti visivi contrassegnati per la risposta asincrona al tocco. Nella figura seguente è illustrata una versione semplificata di tale albero di composizione:

![una struttura ad albero visuale condivisa tra un thread dell'interfaccia utente e un thread di tocco](images/shared-visual-tree-2.png)

In genere, il thread dell'interfaccia utente modifica solo gli oggetti visivi che possiede esclusivamente e il thread tocco modifica solo l'oggetto visivo condiviso. L'unica eccezione si verifica quando si crea o si elimina un sottoalbero abilitato per il tocco.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IDCompositionSurface:: BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw)
</dt> <dt>

[**IDCompositionSurface:: EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw)
</dt> <dt>

[**IDCompositonDevice:: commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit)
</dt> <dt>

[Concetti di DirectComposition](directcomposition-concepts.md)
</dt> </dl>

 

 