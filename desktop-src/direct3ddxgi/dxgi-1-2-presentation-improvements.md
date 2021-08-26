---
title: Capovolgi modello, rettangoli dirty, aree con scorrimento
description: DXGI 1.2 supporta una nuova catena di scambio del modello flip, rettangoli dirty e aree scorreggiate. Vengono illustrati i vantaggi dell'uso della nuova catena di scambio del modello flip e dell'ottimizzazione della presentazione specificando rettangoli dirty e aree di scorrimento.
ms.assetid: 22236FBD-E881-49B5-8AE9-96FB526DFEF8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12f191af4a94b1379e2539b8d544163467fe4dc49141f244e8dcc1f13a3e36af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119984226"
---
# <a name="flip-model-dirty-rectangles-scrolled-areas"></a>Capovolgi modello, rettangoli dirty, aree con scorrimento

DXGI 1.2 supporta una nuova catena di scambio del modello flip, rettangoli dirty e aree scorreggiate. Vengono illustrati i vantaggi dell'uso della nuova catena di scambio del modello flip e dell'ottimizzazione della presentazione specificando rettangoli dirty e aree di scorrimento.

## <a name="dxgi-flip-model-presentation"></a>Presentazione del modello flip DXGI

DXGI 1.2 aggiunge il supporto per il modello di presentazione flip per le API Direct3D 10 e successive. In Windows 7 Direct3D 9EX ha [](../direct3darticles/direct3d-9ex-improvements.md) adottato per la prima volta la presentazione del modello flip per evitare di copiare inutilmente il buffer della catena di scambio. Usando il modello flip, i buffer back vengono capovolti tra il runtime e Gestione finestre desktop (DWM), quindi DWM compone sempre direttamente dal buffer nascosto anziché copiare il contenuto del buffer nascosto.

Le API DXGI 1.2 includono un'interfaccia della catena di scambio DXGI modificata, [**IDXGISwapChain1.**](/windows/desktop/api/DXGI1_2/nn-dxgi1_2-idxgiswapchain1) È possibile usare più metodi di interfaccia [**IDXGIFactory2**](/windows/desktop/api/DXGI1_2/nn-dxgi1_2-idxgifactory2) per creare l'oggetto **IDXGISwapChain1** appropriato da usare con un handle [**HWND,**](../winprog/windows-data-types.md) un [oggetto CoreWindow,](/uwp/api/Windows.UI.Core.CoreWindow?view=winrt-19041) [DirectComposition](../directcomp/directcomposition-portal.md)o il [**Windows. Ui. Framework Xaml.**](/uwp/api/Windows.UI.Xaml?view=winrt-19041)

È possibile selezionare il modello di presentazione flip specificando il valore di enumerazione [**DXGI \_ SWAP EFFECT FLIP \_ \_ \_ SEQUENTIAL**](/windows/desktop/api/DXGI/ne-dxgi-dxgi_swap_effect) nel membro **SwapEffect** della struttura [**DXGI \_ SWAP CHAIN \_ \_ DESC1**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_swap_chain_desc1) e impostando il membro **BufferCount** di **DXGI \_ SWAP CHAIN \_ \_ DESC1** su un valore minimo di 2. Per altre informazioni su come usare il modello flip DXGI, vedere [Modello di inversione DXGI.](dxgi-flip-model.md) A causa della presentazione più uniforme del modello di presentazione flip e di altre nuove funzionalità, è consigliabile usare il modello di presentazione capovolgimento per tutte le nuove app che si scrivono con le API Direct3D 10 e successive.

## <a name="using-dirty-rectangles-and-the-scroll-rectangle-in-swap-chain-presentation"></a>Uso di rettangoli dirty e del rettangolo di scorrimento nella presentazione della catena di scambio

Usando rettangoli dirty e il rettangolo di scorrimento nella presentazione della catena di scambio, si risparmia sull'utilizzo della larghezza di banda della memoria e sull'utilizzo correlato dell'alimentazione del sistema, perché la quantità di dati pixel che il sistema operativo deve disegnare il frame presentato successivo viene ridotta se il sistema operativo non deve disegnare l'intero frame. Per le app spesso visualizzate tramite Connessione Desktop remoto e altre tecnologie di accesso remoto, i risparmi sono particolarmente evidenti nella qualità dello schermo perché queste tecnologie usano rettangoli dirty e metadati di scorrimento.

È possibile usare lo scorrimento solo con catene di scambio DXGI eseguite nel modello di presentazione flip. È possibile usare rettangoli dirty con catene di scambio DXGI eseguite sia nel modello flip che nel modello bitblt (impostato con [**DXGI \_ SWAP \_ EFFECT \_ SEQUENTIAL).**](/windows/desktop/api/DXGI/ne-dxgi-dxgi_swap_effect)

In questo scenario e illustrazione viene illustrata la funzionalità dell'uso di rettangoli dirty e dello scorrimento. In questo caso, un'app scorrevole contiene testo e video di animazione. L'app usa rettangoli dirty per aggiornare solo il video di animazione e la nuova riga per la finestra, invece di aggiornare l'intera finestra. Il rettangolo di scorrimento consente al sistema operativo di copiare e tradurre il contenuto di cui è stato eseguito il rendering in precedenza nel nuovo frame ed eseguire il rendering solo della nuova riga nel nuovo frame.

L'app esegue la presentazione chiamando il [**metodo IDXGISwapChain1::P resent1.**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) In questa chiamata, l'app passa un puntatore a una struttura [**DXGI \_ PRESENT \_ PARAMETERS**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_present_parameters) che include rettangoli dirty e il numero di rettangoli dirty, il rettangolo di scorrimento e l'offset di scorrimento associato o entrambi i rettangoli dirty e il rettangolo di scorrimento. L'app passa 2 rettangoli dirty e il rettangolo di scorrimento. Il rettangolo di scorrimento è l'area del frame precedente che il sistema operativo deve copiare nel frame corrente prima di eseguire il rendering del frame corrente. L'app specifica il video di animazione e la nuova riga come rettangoli dirty e il sistema operativo li esegue il rendering nel frame corrente.

![Illustrazione della sovrapposizione di rettangoli di scorrimento e dirty](images/dxgipresentparam.png)

``` syntax
DirtyRectsCount = 2
pDirtyRects[ 0 ] = { 10, 30, 40, 50 } // Video
pDirtyRects[ 1 ] = { 0, 70, 50, 80 } // New line
*pScrollRect = { 0, 0, 50, 70 }
*pScrollOffset = { 0, -10 }
```

Il rettangolo tratteggiato mostra il rettangolo di scorrimento nel frame corrente. Il rettangolo di scorrimento viene specificato dal **membro pScrollRect** di [**DXGI \_ PRESENT \_ PARAMETERS**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_present_parameters). La freccia mostra l'offset di scorrimento. L'offset di scorrimento viene specificato dal **membro pScrollOffset** **di DXGI \_ PRESENT \_ PARAMETERS**. I rettangoli riempiti mostrano rettangoli dirty aggiornati dall'app con nuovo contenuto. I rettangoli riempiti vengono specificati dai membri **DirtyRectsCount** e **pDirtyRects** **di DXGI \_ PRESENT \_ PARAMETERS**.

### <a name="sample-2-buffer-flip-model-swap-chain-with-dirty-rectangles-and-scroll-rectangle"></a>Esempio di catena di scambio a 2 buffer flip-model con rettangoli dirty e rettangolo di scorrimento

La figura e la sequenza seguenti illustrano un esempio di un'operazione di presentazione del modello flip DXGI che usa rettangoli dirty e un rettangolo di scorrimento. In questo esempio viene utilizzato il numero minimo di buffer per la presentazione del modello flip, ovvero un numero di buffer di due, un front buffer che contiene il contenuto visualizzato dell'app e un buffer nascosto che contiene il frame corrente di cui l'app vuole eseguire il rendering.

1.  Come illustrato nel front buffer all'inizio del frame, l'app scorrevole mostra inizialmente un frame con testo e video di animazione.
2.  Per eseguire il rendering del fotogramma successivo, l'app esegue il rendering nel buffer nascosto dei rettangoli dirty che aggiornano il video animato e la nuova riga per la finestra.
3.  Quando l'app chiama [**IDXGISwapChain1::P resent1,**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1)specifica i rettangoli dirty e il rettangolo di scorrimento e l'offset. Il runtime copia quindi il rettangolo di scorrimento dal frame precedente meno i rettangoli dirty aggiornati nel buffer nascosto corrente.
4.  Il runtime scambia infine i buffer front-back e back.

![Esempio di catena di scambio di modelli flip con rettangoli di scorrimento e dirty](images/2-buffer-flip-model-swap-chain.png)

### <a name="tracking-dirty-rectangles-and-scroll-rectangles-across-multiple-frames"></a>Rilevamento di rettangoli dirty e rettangoli di scorrimento tra più fotogrammi

Quando si usano rettangoli dirty nell'app, è necessario tenere traccia dei rettangoli dirty per supportare il rendering incrementale. Quando l'app chiama [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) con rettangoli dirty, è necessario assicurarsi che ogni pixel all'interno dei rettangoli dirty sia aggiornato. Se non si esegue completamente il rendering dell'intera area del rettangolo dirty o se non è possibile conoscere determinate aree di cui si esegue il rendering, è necessario copiare alcuni dati dal buffer nascosto completamente coerente precedente al buffer nascosto corrente e non obsoleto prima di avviare il rendering.

Il runtime copia solo le differenze tra le aree aggiornate del frame precedente e le aree aggiornate del frame corrente nel buffer nascosto corrente. Se queste aree si intersecano, il runtime copia solo la differenza tra di esse. Come si può vedere nel diagramma e nella sequenza seguenti, è necessario copiare l'intersezione tra il rettangolo dirty dal frame 1 e il rettangolo dirty dal frame 2 al rettangolo dirty del frame 2.

1.  Presentare il rettangolo dirty nel frame 1.
2.  Copiare l'intersezione tra il rettangolo dirty dal frame 1 e il rettangolo dirty dal frame 2 al rettangolo dirty del frame 2.
3.  Presentare il rettangolo dirty nel frame 2.

![rilevamento di rettangoli di scorrimento e dirty in più fotogrammi](images/track-dirty-rects-scroll-rects.png)

Per generalizzare, per una catena di scambio con N buffer, l'area copiata dal runtime dall'ultimo frame al frame corrente nel frame corrente è:

![equazione per calcolare l'area copiata dal runtime](images/runtime-copy-equation.png)

dove buffer indica l'indice del buffer in una catena di scambio, a partire dall'indice del buffer corrente su zero.

È possibile tenere traccia di eventuali intersezioni tra il frame precedente e i rettangoli dirty del frame corrente mantenendo una copia dei rettangoli dirty del frame precedente o ri-rendering dei rettangoli dirty del nuovo frame con il contenuto appropriato dal frame precedente.

Analogamente, nei casi in cui la catena di scambio ha più di 2 buffer indietro, è necessario assicurarsi che le aree sovrapposte tra i rettangoli dirty del buffer corrente e i rettangoli dirty di tutti i frame precedenti siano copiate o sottoposte a nuovo rendering.

### <a name="tracking-a-single-intersection-between-2-dirty-rectangles"></a>Rilevamento di una singola intersezione tra 2 rettangoli dirty

Nel caso più semplice, quando si aggiorna un singolo rettangolo dirty per frame, i rettangoli dirty tra due fotogrammi potrebbero intersecarsi. Per determinare se il rettangolo dirty del frame precedente e il rettangolo dirty del frame corrente si sovrappongono, è necessario verificare se il rettangolo dirty del frame precedente si interseca con il rettangolo dirty del frame corrente. È possibile chiamare la funzione [**GDI IntersectRect**](/windows/win32/api/winuser/nf-winuser-intersectrect) per determinare se due [**strutture RECT**](/previous-versions//dd162897(v=vs.85)) che rappresentano i due rettangoli dirty si intersecano.

In questo frammento di codice una chiamata a [**IntersectRect**](/windows/win32/api/winuser/nf-winuser-intersectrect) restituisce l'intersezione di due rettangoli dirty in un altro [**RECT**](/previous-versions//dd162897(v=vs.85)) denominato dirtyRectCopy. Dopo che il frammento di codice ha determinato l'intersezione dei due rettangoli dirty, chiama il metodo [**ID3D11DeviceContext1::CopySubresourceRegion1**](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11devicecontext1-copysubresourceregion1) per copiare l'area di intersezione nel frame corrente.

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

Se si usa questo frammento di codice nell'applicazione, l'app sarà quindi pronta a chiamare [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) per aggiornare il frame corrente con il rettangolo dirty corrente.

### <a name="tracking-intersections-between-n-dirty-rectangles"></a>Rilevamento delle intersezioni tra N rettangoli dirty

Se si specificano più rettangoli dirty, che possono includere un rettangolo dirty per la nuova linea di scorrimento rivelata, per frame, è necessario verificare e tenere traccia di eventuali sovrapposizioni che potrebbero verificarsi tra tutti i rettangoli dirty del frame precedente e tutti i rettangoli dirty del frame corrente. Per calcolare le intersezioni tra i rettangoli dirty del frame precedente e i rettangoli dirty del frame corrente, è possibile raggruppare i rettangoli dirty in aree.

In questo frammento di codice viene chiamata la funzione [**GDI SetRectRgn**](/windows/win32/api/wingdi/nf-wingdi-setrectrgn) per convertire ogni rettangolo dirty in un'area rettangolare e quindi viene chiamata la funzione GDI [**CombineRgn**](/windows/win32/api/wingdi/nf-wingdi-combinergn) per combinare tutte le aree rettangolari dirty in un gruppo.

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

È ora possibile usare la funzione [**GDI CombineRgn**](/windows/win32/api/wingdi/nf-wingdi-combinergn) per determinare l'intersezione tra l'area dirty del frame precedente e l'area dirty del frame corrente. Dopo aver ottenuto l'area di intersezione, chiamare la funzione [**GDI GetRegionData**](/windows/win32/api/wingdi/nf-wingdi-getregiondata) per ottenere ogni singolo rettangolo dall'area intersecata e quindi chiamare il [**metodo ID3D11DeviceContext1::CopySubresourceRegion1**](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11devicecontext1-copysubresourceregion1) per copiare ogni rettangolo intersecante nel buffer nascosto corrente. Il frammento di codice successivo illustra come usare queste funzioni GDI e Direct3D.

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

### <a name="bitblt-model-swap-chain-with-dirty-rectangles"></a>Catena di scambio del modello Bitblt con rettangoli dirty

È possibile usare rettangoli dirty con catene di scambio DXGI eseguite nel modello bitblt (impostato con [**DXGI \_ SWAP \_ EFFECT \_ SEQUENTIAL).**](/windows/desktop/api/DXGI/ne-dxgi-dxgi_swap_effect) Le catene di scambio del modello Bitblt che usano più di un buffer devono anche tenere traccia dei rettangoli dirty sovrapposti tra frame nello stesso modo descritto in [Rilevamento](#tracking-dirty-rectangles-and-scroll-rectangles-across-multiple-frames) di rettangoli dirty e rettangoli di scorrimento tra più frame per le catene di scambio del modello di inversione. Le catene di scambio del modello Bitblt con un solo buffer non devono tenere traccia dei rettangoli dirty sovrapposti perché l'intero buffer viene ridisegnato ogni frame.

## <a name="related-topics"></a>Argomenti correlati

[Miglioramenti di DXGI 1.2](dxgi-1-2-improvements.md)
