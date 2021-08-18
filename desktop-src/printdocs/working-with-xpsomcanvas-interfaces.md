---
title: Interfacce canvas e visive XPS OM
description: Questo argomento descrive come usare le interfacce correlate all'area di disegno dell'API documento XPS in un OM XPS.
ms.assetid: 368b8c47-9803-42ee-a3a8-681bf55315ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97f7214a06779d997331f57a22ae29217e5cabdd635d0c3feac85bd8a3070065
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118469270"
---
# <a name="working-with-xps-om-canvas-and-visual-interfaces"></a>Uso delle interfacce canvas e visive di XPS OM

Questo argomento descrive come usare le interfacce correlate all'area di disegno dell'API documento XPS in un OM XPS.

| Nome dell'interfaccia                                  | Interfacce figlio logiche                                                                                                                    | Descrizione                                                                                                                                                                                                             |
|-------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IXpsOMVisual**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual)<br/> | [**IXpsOMCanvas**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas)<br/> [**IXpsOMGlyphs**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs)<br/> [**IXpsOMPath**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath)<br/> | Classe di base delle interfacce che definiscono oggetti visivi, ad esempio testo e grafica.<br/> Gli oggetti visivi possono essere raccolti in [**un'interfaccia IXpsOMVisualCollection.**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualcollection)<br/> |
| [**IXpsOMCanvas**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas)<br/> | [**IXpsOMCanvas**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas)<br/> [**IXpsOMGlyphs**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs)<br/> [**IXpsOMPath**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath)<br/> | Raccolta di oggetti visivi che possono essere considerati come un singolo oggetto visivo.<br/>                                                                                                                                |

[**IXpsOMVisual è**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual) l'interfaccia di base. Gli oggetti visibili di una pagina ereditano da essa. [**IXpsOMCanvas**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas) eredita da [**IXpsOMVisual**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual) e consente di raggruppare e agire su molti altri elementi visivi come un singolo elemento visivo. Ad esempio, è possibile usare [**un'interfaccia IXpsOMCanvas**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas) per creare un banner di pagina che contiene una raccolta di testo ed elementi grafici. Un banner di questo tipo potrebbe contenere un logo, la società e l'indirizzo della società. È possibile inserire tutti questi elementi nell'oggetto [**IXpsOMVisualCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualcollection) di [**un'interfaccia IXpsOMCanvas**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas) e quindi applicare una singola trasformazione all'oggetto [**IXpsOMCanvas**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas) per ridimensionarlo in una pagina specifica. Questa operazione è molto più semplice rispetto al calcolo e all'applicazione di una trasformazione a ogni singolo componente visivo nel banner.

È anche possibile usare un'area di disegno per ridimensionare il contenuto della pagina in base alle dimensioni della pagina corrente. A tale scopo, inserire tutto il contenuto della pagina in un'unica area di disegno, quindi applicare la trasformazione appropriata per adattare l'area di disegno alle dimensioni della pagina corrente. Questa operazione è molto più semplice rispetto al tentativo di ridimensionare ogni elemento visivo nella raccolta di oggetti visivi nella pagina.

## <a name="move-page-contents-to-a-canvas"></a>Spostare il contenuto della pagina in un'area di disegno

Nell'esempio di codice seguente il contenuto di una pagina viene spostato in un'area di disegno.

```C++
    HRESULT                   hr = S_OK;

    IXpsOMVisualCollection    *pageVisuals;
    IXpsOMVisualCollection    *canvasVisuals;
    IXpsOMVisual              *oneVisual;
    IXpsOMCanvas              *newPageCanvas;

    UINT32 numVisuals = 0;
    UINT32 thisVisual;

    // get the page's visual collection
    // and how many objects it contains
    hr = page->GetVisuals( &pageVisuals );
    hr = pageVisuals->GetCount ( &numVisuals );

    // create the new canvas object and
    // its (empty) visual collection
    hr = xpsFactory->CreateCanvas ( &newPageCanvas );
    hr = newPageCanvas->GetVisuals ( &canvasVisuals );

    // go through the page's list of visual objects,
    //  move each one from the page's list to the canvas' list
    //  release the local pointer
    //  remove it from the page's collection
    thisVisual = 0;
    while (thisVisual < numVisuals) {
        hr = pageVisuals->GetAt (0, &oneVisual);
        hr = canvasVisuals->Append (oneVisual);
        hr = pageVisuals->RemoveAt (0);
        thisVisual++;
    }
    // the page's visual collection should be empty
    hr = pageVisuals->GetCount (&numVisuals);
    _ASSERT (0 == numVisuals);

    // add the new canvas to the page's visual collection
    pageVisuals->Append ( newPageCanvas );

```

## <a name="related-topics"></a>Argomenti correlati

<dl> 
  <dt>[**Interfaccia IXpsOMCanvas**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas)</dt>
  <dt>[**IXpsOMVisual Interface**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual)</dt>
  <dt>[**IXpsOMVisualCollection Interface**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualcollection)</dt>
</dl>
