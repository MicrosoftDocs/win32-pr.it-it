---
title: Ritaglio (DirectComposition)
description: Questo argomento descrive il supporto di Microsoft DirectComposition per il ritaglio degli oggetti visivi.
ms.assetid: B6E0D8F5-B6B9-40CC-B079-850AC8F2D538
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4feb537dfb41053dd1099eca7f122b3284dce95
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104400192"
---
# <a name="clipping-directcomposition"></a>Ritaglio (DirectComposition)

> [!NOTE]
> Per le app in Windows 10, è consigliabile usare le API Windows. UI. Composition anziché DirectComposition. Per altre informazioni, vedere [modernizzare l'app desktop usando il livello visivo](/windows/uwp/composition/visual-layer-in-desktop-apps).

Il ritaglio consente di rivelare solo una parte di una struttura ad albero visuale o visuale limitando il rendering dell'oggetto visivo o dell'albero a una particolare area rettangolare. Questo argomento descrive il supporto di Microsoft DirectComposition per il ritaglio degli oggetti visivi. Include le sezioni seguenti:

-   [Rettangolo di ritaglio](#clip-rectangle)
-   [Clip (oggetto)](#clip-object)
-   [Rettangolo di ritaglio animato](#animated-clip-rectangle)
-   [Argomenti correlati](#related-topics)

## <a name="clip-rectangle"></a>Rettangolo di ritaglio

Un oggetto visivo ha una proprietà clip che definisce un'area rettangolare o un *rettangolo di ritaglio* nel contenuto bitmap dell'oggetto visivo. Quando viene eseguito il rendering dell'oggetto visivo sullo schermo, viene disegnata solo la parte del contenuto bitmap all'interno del rettangolo di ritaglio, mentre il contenuto che si estende all'esterno del rettangolo di ritaglio viene ritagliato (non disegnato). Per impostazione predefinita, la proprietà clip include tutto il contenuto della bitmap.

La proprietà di ritaglio di un oggetto visivo si applica a tutti gli oggetti visivi figlio e discendente. In altre parole, viene ritagliato anche eventuali contenuti figlio o discendenti che non rientrano nei limiti del rettangolo di ritaglio del padre.

DirectComposition applica la proprietà di ritaglio prima di applicare le proprietà della trasformazione OffsetX, OffsetY e 2D, ma dopo aver applicato le proprietà effetto e trasformazione 3D. Ciò significa che le trasformazioni 2D, OffsetX e OffsetY avranno effetto sia sul contenuto visivo che sul rettangolo di ritaglio. Mentre le trasformazioni 3D e gli effetti non si applicano al rettangolo di ritaglio.

Ad esempio, quando si applica un offset o una trasformazione 2D, il rettangolo di ritaglio è influenzato dalla matrice di trasformazione. In questo modo, l'aggiunta di un offset e di una rotazione 2D (45 gradi) insieme a un rettangolo di ritaglio di un angolo arrotondato comporterà la seguente

![diagramma che illustra l'effetto di una trasformazione 2D su un rettangolo di ritaglio.](images/clipping2dtransform.png)

Quando si applica una trasformazione 3D "all'interno di", il rettangolo di ritaglio non è influenzato dalla matrice di trasformazione. Anche quando si applica una rotazione intorno all'asse Z (in effetti lo stesso dell'esempio precedente), il diagramma seguente è il risultato:

![diagramma che mostra che una trasformazione 3D non influisce sulla clip rettangolare (l'oggetto visivo ruota all'interno della clip).](images/clipping3dtransform.png)

Si noti che l'oggetto visivo è stato ruotato all'interno del clip perché la matrice 3D non viene applicata alla clip stessa.

Se la proprietà clip è impostata su un rettangolo vuoto, l'oggetto visivo viene troncato completamente; ovvero, l'oggetto visivo è incluso nella struttura ad albero visuale, ma non esegue alcun rendering. Se non si desidera includere un oggetto visivo specifico in una composizione, rimuovere l'oggetto visivo dalla struttura ad albero visuale anziché impostare un rettangolo di ritaglio vuoto. La rimozione dell'oggetto visivo comporta un miglioramento delle prestazioni.

Per impostare la proprietà clip di un oggetto visivo, usare il metodo [**IDCompositionVisual:: seclip**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setclip(constd2d_rect_f_)) . Questo metodo include overload che consentono di impostare il valore della proprietà clip su un rettangolo statico o su un oggetto di ritaglio. Utilizzare un rettangolo statico se non è necessario modificare le dimensioni del rettangolo di ritaglio nel corso della durata dell'oggetto visivo. Se è necessario modificare le dimensioni o aggiungere un'animazione al rettangolo di ritaglio, utilizzare un oggetto di ritaglio.

## <a name="clip-object"></a>Clip (oggetto)

Un oggetto clip è un oggetto Component Object Model (COM) che rappresenta un rettangolo di ritaglio. Si crea un oggetto clip usando il metodo [**IDCompositionDevice:: CreateRectangleClip**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createrectangleclip) , quindi si usa l'interfaccia [**IDCompositionRectangleClip**](/windows/win32/api/dcomp/nn-dcomp-idcompositionrectangleclip) dell'oggetto per impostare le proprietà dell'oggetto. Un oggetto ClipArt appena creato presenta i valori minimi possibili per le proprietà Left e Top e i valori massimi possibili per le proprietà Right e Bottom, rendendolo effettivamente un oggetto clip senza op. In altre parole, l'oggetto rappresenta un rettangolo di ritaglio che include l'intero contenuto bitmap di un oggetto visivo.

Un oggetto clip include un set di proprietà che consentono di specificare gli angoli arrotondati per l'oggetto di ritaglio. Le proprietà consentono di impostare il raggio x e il raggio y di ogni angolo dell'oggetto di ritaglio.

## <a name="animated-clip-rectangle"></a>Rettangolo di ritaglio animato

È possibile aggiungere un'animazione a un rettangolo di ritaglio applicando oggetti di animazione alle proprietà Left, top, Right e Bottom di un oggetto clip. Usare il metodo di overload [**IDCompositionVisual:: seclip (IDCompositionClip)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setclip(idcompositionclip)) per applicare il rettangolo di ritaglio animato alla proprietà clip di un oggetto visivo.

Per ulteriori informazioni sugli oggetti di animazione, vedere [Animation](animation.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Concetti di DirectComposition](directcomposition-concepts.md)
</dt> <dt>

[Come eseguire il clip con un oggetto rettangolo clip](how-to--set-the-clip-rectangle-for-a-visual.md)
</dt> </dl>

 

 
