---
title: Capovolgi modello, rettangoli Dirty, aree a scorrimento
description: DXGI 1,2 supporta una nuova catena di scambio Flip-Model, rettangoli Dirty e aree a scorrimento. Vengono illustrati i vantaggi derivanti dall'utilizzo della nuova catena di scambio flip-model e dall'ottimizzazione della presentazione specificando rettangoli Dirty e aree a scorrimento.
ms.assetid: 22236FBD-E881-49B5-8AE9-96FB526DFEF8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a3abbb784de82f5bf647a4b66503497edcd4f89
ms.sourcegitcommit: 5724b38883e518ac565e1b266defa85ad0941bb2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/14/2021
ms.locfileid: "104568728"
---
# <a name="flip-model-dirty-rectangles-scrolled-areas"></a>Capovolgi modello, rettangoli Dirty, aree a scorrimento

DXGI 1,2 supporta una nuova catena di scambio Flip-Model, rettangoli Dirty e aree a scorrimento. Vengono illustrati i vantaggi derivanti dall'utilizzo della nuova catena di scambio flip-model e dall'ottimizzazione della presentazione specificando rettangoli Dirty e aree a scorrimento.

## <a name="dxgi-flip-model-presentation"></a>Presentazione del modello DXGI Flip

DXGI 1,2 aggiunge il supporto per il modello Flip Presentation per le API Direct3D 10 e versioni successive. In Windows 7, Direct3D 9EX ha adottato per la prima volta la [presentazione del modello Flip](../direct3darticles/direct3d-9ex-improvements.md) per evitare la copia inutilmente del buffer della catena di scambio. Utilizzando Capovolgi modello, i buffer indietro vengono capovolti tra il runtime e Gestione finestre desktop (DWM), quindi DWM si compone sempre direttamente dal buffer nascosto anziché copiare il contenuto del buffer nascosto.

Le API DXGI 1,2 includono un'interfaccia a catena di scambio DXGI modificata, [**IDXGISwapChain1**](/windows/desktop/api/DXGI1_2/nn-dxgi1_2-idxgiswapchain1). È possibile usare più metodi di interfaccia [**IDXGIFactory2**](/windows/desktop/api/DXGI1_2/nn-dxgi1_2-idxgifactory2) per creare l'oggetto **IDXGISwapChain1** appropriato da usare con un handle [**HWND**](../winprog/windows-data-types.md) , un oggetto [CoreWindow](/uwp/api/Windows.UI.Core.CoreWindow?view=winrt-19041) , [DirectComposition](../directcomp/directcomposition-portal.md)o il Framework [**Windows. UI. XAML**](/uwp/api/Windows.UI.Xaml?view=winrt-19041) .

È possibile selezionare il modello Flip Presentation specificando il valore di enumerazione [**\_ \_ \_ \_ sequenziale DXGI swap effect Flip**](/windows/desktop/api/DXGI/ne-dxgi-dxgi_swap_effect) nel membro **SwapEffect** della struttura [**DXGI \_ \_ Chain swap \_ DESC1**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_swap_chain_desc1) e impostando il membro **BufferCount** di **DXGI \_ swap \_ Chain \_ DESC1** su un minimo di 2. Per ulteriori informazioni sull'utilizzo del modello DXGI Flip, vedere [DXGI flip model](dxgi-flip-model.md). Grazie alla presentazione più semplice del modello di presentazione e ad altre nuove funzionalità, è consigliabile usare il modello Flip Presentation per tutte le nuove app scritte con le API Direct3D 10 e versioni successive.

## <a name="using-dirty-rectangles-and-the-scroll-rectangle-in-swap-chain-presentation"></a>Uso di rettangoli Dirty e del rettangolo di scorrimento nella presentazione della catena di scambio

Utilizzando rettangoli Dirty e il rettangolo di scorrimento nella presentazione della catena di scambio, è possibile risparmiare sull'utilizzo della larghezza di banda della memoria e sull'utilizzo correlato della potenza del sistema, perché la quantità di dati pixel che il sistema operativo deve creare il successivo frame presentato è ridotta se non è necessario che il sistema operativo disegni l'intero frame. Per le app che vengono spesso visualizzate tramite Connessione Desktop remoto e altre tecnologie di accesso remoto, i risparmi sono particolarmente evidenti nella qualità di visualizzazione, in quanto tali tecnologie utilizzano rettangoli Dirty e metadati di scorrimento.

È possibile usare Scroll solo con le catene di scambio DXGI eseguite nel modello Flip Presentation. È possibile usare rettangoli Dirty con le catene di scambio DXGI che vengono eseguite sia nel modello flip che nel modello BitBlt (impostato con l' [**\_ effetto di scambio DXGI \_ \_ sequenziale**](/windows/desktop/api/DXGI/ne-dxgi-dxgi_swap_effect)).

In questo scenario viene illustrata la funzionalità di utilizzo di rettangoli e scorrimenti Dirty. Qui, un'app scorrevole contiene testo e animazione di video. L'app usa rettangoli Dirty per aggiornare semplicemente il video di animazione e la nuova riga per la finestra, anziché aggiornare l'intera finestra. Il rettangolo di scorrimento consente al sistema operativo di copiare e tradurre il contenuto precedentemente sottoposto a rendering sul nuovo frame e di eseguire il rendering solo della nuova riga sul nuovo frame.

L'app esegue la presentazione chiamando il metodo [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) . In questa chiamata, l'app passa un puntatore a una struttura di [**\_ \_ parametri presente DXGI**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_present_parameters) che include rettangoli Dirty e il numero di rettangoli Dirty, oppure il rettangolo di scorrimento e l'offset di scorrimento associato oppure i rettangoli Dirty e il rettangolo di scorrimento. L'app passa 2 rettangoli Dirty e il rettangolo di scorrimento. Il rettangolo di scorrimento è l'area del fotogramma precedente che il sistema operativo deve copiare nel frame corrente prima di eseguire il rendering del frame corrente. L'app specifica il video di animazione e la nuova riga come rettangoli Dirty e il sistema operativo li esegue il rendering nel frame corrente.

![illustrazione dei rettangoli scroll e Dirty sovrapposti](images/dxgipresentparam.png)

``` syntax
DirtyRectsCount = 2
pDirtyRects[ 0 ] = { 10, 30, 40, 50 } // Video
pDirtyRects[ 1 ] = { 0, 70, 50, 80 } // New line
*pScrollRect = { 0, 0, 50, 70 }
*pScrollOffset = { 0, -10 }
```

Il rettangolo tratteggiato Mostra il rettangolo di scorrimento nel frame corrente. Il rettangolo di scorrimento viene specificato dal membro **pScrollRect** di [**DXGI \_ \_ parametri presenti**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_present_parameters). La freccia Mostra l'offset di scorrimento. L'offset di scorrimento viene specificato dal membro **pScrollOffset** di **DXGI \_ \_ parametri presenti**. I rettangoli riempiti mostrano i rettangoli Dirty che l'app ha aggiornato con nuovo contenuto. I rettangoli riempiti sono specificati dai membri **DirtyRectsCount** e **pDirtyRects** di **DXGI \_ present \_ Parameters**.

### <a name="sample-2-buffer-flip-model-swap-chain-with-dirty-rectangles-and-scroll-rectangle"></a>Esempio 2: catena di scambio Flip del buffer con rettangoli Dirty e rettangolo di scorrimento

L'illustrazione e la sequenza successive mostrano un esempio di un'operazione di presentazione del modello DXGI flip che usa rettangoli Dirty e un rettangolo di scorrimento. In questo esempio viene usato il numero minimo di buffer per la presentazione del modello Flip, ovvero un numero di buffer di due, un buffer anteriore che contiene il contenuto di visualizzazione dell'app e un buffer nascosto che contiene il frame corrente di cui l'app vuole eseguire il rendering.

1.  Come illustrato nel buffer anteriore all'inizio del frame, l'app scorrevole Mostra inizialmente un frame con testo e animazione di video.
2.  Per eseguire il rendering del frame successivo, l'app esegue il rendering sul buffer nascosto dei rettangoli Dirty che aggiornano il video di animazione e la nuova riga per la finestra.
3.  Quando l'app chiama [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1), specifica i rettangoli Dirty e il rettangolo di scorrimento e l'offset. Il runtime copia successivamente il rettangolo di scorrimento dal fotogramma precedente meno i rettangoli Dirty aggiornati sul buffer nascosto corrente.
4.  Il runtime scambia infine i buffer anteriore e posteriore.

![esempio di catena di scambio flip-model con rettangoli scroll e Dirty](images/2-buffer-flip-model-swap-chain.png)

### <a name="tracking-dirty-rectangles-and-scroll-rectangles-across-multiple-frames"></a>Rilevamento di rettangoli Dirty e rettangoli di scorrimento tra più frame

Quando si usano rettangoli Dirty nell'app, è necessario tenere traccia dei rettangoli Dirty per supportare il rendering incrementale. Quando l'app chiama [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) con rettangoli Dirty, è necessario assicurarsi che ogni pixel all'interno dei rettangoli Dirty sia aggiornato. Se non si esegue completamente il rendering dell'intera area del rettangolo modificato o se non si è in grado di individuare determinate aree sporche, è necessario copiare alcuni dati dal buffer nascosto precedente completamente coerente al buffer nascosto corrente, prima di iniziare il rendering.

Il runtime copia solo le differenze tra le aree aggiornate del frame precedente e le aree aggiornate del frame corrente nel buffer nascosto corrente. Se queste aree si intersecano, il runtime copia solo la differenza tra di esse. Come si può notare nel diagramma e nella sequenza seguenti, è necessario copiare l'intersezione tra il rettangolo Dirty dal frame 1 e il rettangolo Dirty dal frame 2 al rettangolo modificato del frame 2.

1.  Presentare un rettangolo modificato nel frame 1.
2.  Copia intersezione tra il rettangolo Dirty dal frame 1 e il rettangolo Dirty dal frame 2 al rettangolo modificato del frame 2.
3.  Presentare un rettangolo modificato nel frame 2.

![rilevamento dei rettangoli scroll e Dirty tra più frame](images/track-dirty-rects-scroll-rects.png)

Per generalizzare, per una catena di scambio con N buffer, l'area che il runtime copia dall'ultimo frame al frame corrente sul presente frame corrente è:

![equazione per calcolare l'area copiata dal runtime](images/runtime-copy-equation.png)

dove buffer indica l'indice del buffer in una catena di scambio, a partire dall'indice del buffer corrente a zero.

È possibile tenere traccia di tutte le intersezioni tra il frame precedente e i rettangoli Dirty del frame corrente mantenendo una copia dei rettangoli Dirty del fotogramma precedente oppure eseguendo nuovamente il rendering dei rettangoli Dirty del nuovo frame con il contenuto appropriato del frame precedente.

Analogamente, nei casi in cui la catena di scambio dispone di più di 2 buffer indietro, è necessario assicurarsi che le aree sovrapposte tra i rettangoli Dirty del buffer corrente e i rettangoli Dirty di tutti i frame precedenti vengano copiati o nuovamente sottoposti a rendering.

### <a name="tracking-a-single-intersection-between-2-dirty-rectangles"></a>Rilevamento di una singola intersezione tra due rettangoli Dirty

Nel caso più semplice, quando si aggiorna un singolo rettangolo modificato per fotogramma, è possibile che i rettangoli Dirty tra due frame si intersecano. Per determinare se il rettangolo modificato del frame precedente e il rettangolo modificato del frame corrente si sovrappongono, è necessario verificare se il rettangolo modificato del fotogramma precedente si interseca con il rettangolo modificato del frame corrente. È possibile chiamare la funzione GDI [**IntersectRect**](/windows/win32/api/winuser/nf-winuser-intersectrect) per determinare se due strutture [**Rect**](/previous-versions//dd162897(v=vs.85)) che rappresentano i due rettangoli Dirty si intersecano.

In questo frammento di codice, una chiamata a [**IntersectRect**](/windows/win32/api/winuser/nf-winuser-intersectrect) restituisce l'intersezione di due rettangoli Dirty in un altro oggetto [**Rect**](/previous-versions//dd162897(v=vs.85)) denominato dirtyRectCopy. Dopo che il frammento di codice ha determinato che i due rettangoli Dirty si intersecano, chiama il metodo [**ID3D11DeviceContext1:: CopySubresourceRegion1**](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11devicecontext1-copysubresourceregion1) per copiare l'area di intersezione nel frame corrente.

```
RECT dirtyRectPrev, dirtyRectCurrent, dirtyRectCopy;
 
if (IntersectRect( &dirtyRectCopy, &dirtyRectPrev, &dirtyRectCurrent ))
{
       D3D11_BOX intersectBox;
       intersectBox.left    = dirtyRectCopy.left;
       intersectBox.top     = dirtyRectCopy.top;
       intersectBox.front   = 0;
       intersectBox.right   = dirtyRectCopy.right;
       intersectBox.bottom  = dirtyRectCopy.bottom;
       intersectBox.back    = 1;
 
       d3dContext->CopySubresourceRegion1(pBackbuffer,
                                    0,
                                    0,
                                    0,
                                    0,
                                    pPrevBackbuffer,
                                    0,
                                    &intersectBox,
                                    0
                                    );
}

// Render additional content to the current pBackbuffer and call Present1.
```

Se si usa questo frammento di codice nell'applicazione, l'app sarà pronta per chiamare [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) per aggiornare il frame corrente con il rettangolo modificato corrente.

### <a name="tracking-intersections-between-n-dirty-rectangles"></a>Rilevamento di intersezioni tra N rettangoli Dirty

Se si specificano più rettangoli Dirty, che possono includere un rettangolo modificato per la riga di scorrimento appena rivelata, per fotogramma, è necessario verificare e tenere traccia di eventuali sovrapposizioni che potrebbero verificarsi tra tutti i rettangoli Dirty del frame precedente e tutti i rettangoli modificati del frame corrente. Per calcolare le intersezioni tra i rettangoli Dirty del fotogramma precedente e i rettangoli Dirty del frame corrente, è possibile raggruppare i rettangoli Dirty in aree.

In questo frammento di codice viene chiamata la funzione GDI [**SetRectRgn**](/windows/win32/api/wingdi/nf-wingdi-setrectrgn) per convertire ogni rettangolo modificato in un'area rettangolare, quindi viene chiamata la funzione GDI [**CombineRgn**](/windows/win32/api/wingdi/nf-wingdi-combinergn) per combinare tutte le aree rettangolari Dirty in un gruppo.

```
HRGN hDirtyRgnPrev, hDirtyRgnCurrent, hRectRgn; // Handles to regions 
// Save all the dirty rectangles from the previous frame.
 
RECT dirtyRect[N]; // N is the number of dirty rectangles in current frame, which includes newly scrolled area.
 
int iReturn;
SetRectRgn(hDirtyRgnCurrent, 
       dirtyRect[0].left, 
       dirtyRect[0].top, 
       dirtyRect[0].right, 
       dirtyRect[0].bottom 
       );

for (int i = 1; i<N; i++)
{
   SetRectRgn(hRectRgn, 
          dirtyRect[0].left, 
          dirtyRect[0].top, 
          dirtyRect[0].right, 
          dirtyRect[0].bottom 
          );

   iReturn = CombineRgn(hDirtyRgnCurrent,
                        hDirtyRgnCurrent,
                        hRectRgn,
                        RGN_OR
                        );
   // Handle the error that CombineRgn returns for iReturn.
}
```

È ora possibile usare la funzione GDI [**CombineRgn**](/windows/win32/api/wingdi/nf-wingdi-combinergn) per determinare l'intersezione tra l'area dirty del frame precedente e l'area dirty del frame corrente. Una volta ottenuta l'area di intersezione, chiamare la funzione GDI [**GetRegionData**](/windows/win32/api/wingdi/nf-wingdi-getregiondata) per ottenere ogni singolo rettangolo dall'area intersecante, quindi chiamare il metodo [**ID3D11DeviceContext1:: CopySubresourceRegion1**](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11devicecontext1-copysubresourceregion1) per copiare ogni rettangolo intersecante nel buffer nascosto corrente. Il frammento di codice successivo Mostra come usare queste funzioni GDI e Direct3D.

```
HRGN hIntersectRgn;
bool bRegionsIntersect;
iReturn = CombineRgn(hIntersectRgn, hDirtyRgnCurrent, hDirtyRgnPrev, RGN_AND);
if (iReturn == ERROR)
{
       // Handle error.
}
else if(iReturn == NULLREGION)
{
       bRegionsIntersect = false;
}
else
{
       bRegionsIntersect = true;
}
 
if (bRegionsIntersect)
{
       int rgnDataSize = GetRegionData(hIntersectRgn, 0, NULL);
       if (rgnDataSize)
       {
              char pMem[] = new char[size];
              RGNDATA* pRgnData = reinterpret_cast<RGNDATA*>(pMem);
              iReturn = GetRegionData(hIntersectRgn, rgnDataSize, pRgnData);
              // Handle iReturn failure.
 
              for (int rectcount = 0; rectcount < pRgnData->rdh.nCount; ++r)
              {
                     const RECT* pIntersectRect = reinterpret_cast<RECT*>(pRgnData->Buffer) +                                            
                                                  rectcount;                
                     D3D11_BOX intersectBox;
                     intersectBox.left    = pIntersectRect->left;
                     intersectBox.top     = pIntersectRect->top;
                     intersectBox.front   = 0;
                     intersectBox.right   = pIntersectRect->right;
                     intersectBox.bottom  = pIntersectRect->bottom;
                     intersectBox.back    = 1;
 
                     d3dContext->CopySubresourceRegion1(pBackbuffer,
                                                      0,
                                                      0,
                                                      0,
                                                      0,
                                                      pPrevBackbuffer,
                                                      0,
                                                      &intersectBox,
                                                      0
                                                      );
              }

              delete [] pMem;
       }
}
```

### <a name="bitblt-model-swap-chain-with-dirty-rectangles"></a>Catena di scambio del modello BitBlt con rettangoli Dirty

È possibile usare rettangoli Dirty con le catene di scambio DXGI eseguite nel modello BitBlt (impostate con l' [**\_ effetto di scambio DXGI \_ \_ sequenziale**](/windows/desktop/api/DXGI/ne-dxgi-dxgi_swap_effect)). Le catene di scambio del modello BitBlt che usano più di un buffer devono anche tenere traccia dei rettangoli sporchi sovrapposti tra i frame nello stesso modo descritto in [rilevamento di rettangoli Dirty e rettangoli di scorrimento tra più frame per le](#tracking-dirty-rectangles-and-scroll-rectangles-across-multiple-frames) catene di scambio del modello flip. Le catene di scambio del modello BitBlt con un solo buffer non devono rilevare rettangoli sporchi sovrapposti perché l'intero buffer viene ridisegnato ogni frame.

## <a name="related-topics"></a>Argomenti correlati

[Miglioramenti di DXGI 1,2](dxgi-1-2-improvements.md)
