---
description: Stride dell'immagine
ms.assetid: 13cd1106-48b3-4522-ac09-8efbaab5c31d
title: Stride dell'immagine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 360afb6fdeca4c543957326b041654d75ff17b66db8918e42d781d414e8b7586
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119958152"
---
# <a name="image-stride"></a>Stride dell'immagine

Quando un'immagine video viene archiviata in memoria, il buffer di memoria potrebbe contenere byte di spaziatura interna aggiuntivi dopo ogni riga di pixel. I byte di spaziatura interna influiscono sulla modalità di archiviazione dell'immagine in memoria, ma non sulla modalità di visualizzazione dell'immagine.

Lo *stride* è il numero di byte da una riga di pixel in memoria alla riga successiva di pixel in memoria. Stride è anche detto *passo.* Se sono presenti byte di spaziatura interna, lo stride è più ampio della larghezza dell'immagine, come illustrato nella figura seguente.

![diagramma che mostra un'immagine più la spaziatura interna.](images/c85c6a40-f0a8-48a3-b465-39ceada66339.gif)

Due buffer che contengono fotogrammi video con dimensioni uguali possono avere due diversi passi. Se si elabora un'immagine video, è necessario prendere in considerazione lo stride.

Esistono anche due modi in cui un'immagine può essere disposta in memoria. In *un'immagine dall'alto* verso il basso la prima riga di pixel nell'immagine viene visualizzata per prima in memoria. In *un'immagine dal basso verso* l'alto, l'ultima riga di pixel viene visualizzata per prima in memoria. La figura seguente mostra la differenza tra un'immagine dall'alto verso il basso e un'immagine dal basso verso l'alto.

![diagramma che mostra immagini dall'alto verso il basso e dall'alto.](images/f03bd9ff-0cf3-4a56-88c5-5b8c44637272.gif)

Un'immagine dal basso verso l'alto ha uno stride negativo, perché stride è definito come il numero di byte necessari per spostarsi verso il basso di una riga di pixel, rispetto all'immagine visualizzata. Le immagini YUV devono essere sempre dall'alto verso il basso e qualsiasi immagine contenuta in una superficie Direct3D deve essere dall'alto verso il basso. Le immagini RGB nella memoria di sistema sono in genere dal basso verso l'alto.

Le trasformazioni video, in particolare, devono gestire i buffer con passi non corrispondenti, perché il buffer di input potrebbe non corrispondere al buffer di output. Si supponga, ad esempio, di voler convertire un'immagine di origine e scrivere il risultato in un'immagine di destinazione. Si supponga che entrambe le immagini hanno la stessa larghezza e altezza, ma potrebbero non avere lo stesso formato pixel o lo stesso stride dell'immagine.

Il codice di esempio seguente illustra un approccio generalizzato per la scrittura di questo tipo di funzione. Questo non è un esempio funzionante completo, perché astrae molti dettagli specifici.


```C++
void ProcessVideoImage(
    BYTE*       pDestScanLine0,     
    LONG        lDestStride,        
    const BYTE* pSrcScanLine0,      
    LONG        lSrcStride,         
    DWORD       dwWidthInPixels,     
    DWORD       dwHeightInPixels
    )
{
    for (DWORD y = 0; y < dwHeightInPixels; y++)
    {
        SOURCE_PIXEL_TYPE *pSrcPixel = (SOURCE_PIXEL_TYPE*)pDestScanLine0;
        DEST_PIXEL_TYPE *pDestPixel = (DEST_PIXEL_TYPE*)pSrcScanLine0;

        for (DWORD x = 0; x < dwWidthInPixels; x +=2)
        {
            pDestPixel[x] = TransformPixelValue(pSrcPixel[x]);
        }
        pDestScanLine0 += lDestStride;
        pSrcScanLine0 += lSrcStride;
    }
}
```



Questa funzione accetta sei parametri:

-   Puntatore all'inizio della riga di analisi 0 nell'immagine di destinazione.
-   Stride dell'immagine di destinazione.
-   Puntatore all'inizio della riga di analisi 0 nell'immagine di origine.
-   Stride dell'immagine di origine.
-   Larghezza dell'immagine in pixel.
-   Altezza dell'immagine in pixel.

L'idea generale è elaborare una riga alla volta, iterando ogni pixel nella riga. Si supponga che SOURCE PIXEL TYPE e DEST PIXEL TYPE siano strutture che rappresentano rispettivamente il layout pixel per le immagini di origine \_ \_ e di \_ \_ destinazione. (Ad esempio, RGB a 32 bit usa la [**struttura RGBQUAD.**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) Non tutti i formati pixel hanno una struttura predefinita. Il cast del puntatore di matrice al tipo di struttura consente di accedere ai componenti RGB o YUV di ogni pixel. All'inizio di ogni riga, la funzione archivia un puntatore alla riga. Alla fine della riga, incrementa il puntatore della larghezza dello stride dell'immagine, spostando il puntatore alla riga successiva.

Questo esempio chiama una funzione ipotetica denominata TransformPixelValue per ogni pixel. Può trattarsi di qualsiasi funzione che calcola un pixel di destinazione da un pixel di origine. Naturalmente, i dettagli esatti dipenderanno dall'attività specifica. Ad esempio, se si ha un formato YUV planare, è necessario accedere ai piani chroma in modo indipendente dal piano luma. con il video interlacciato, potrebbe essere necessario elaborare i campi separatamente. e così via.

Per fornire un esempio più concreto, il codice seguente converte un'immagine RGB a 32 bit in un'immagine AYUV. I pixel RGB sono accessibili usando una [**struttura RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) e i pixel AYUV sono accessibili usando una struttura [**DXVA2 \_ AYUVSample8.**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_ayuvsample8)


```C++
//-------------------------------------------------------------------
// Name: RGB32_To_AYUV
// Description: Converts an image from RGB32 to AYUV
//-------------------------------------------------------------------
void RGB32_To_AYUV(
    BYTE*       pDest,
    LONG        lDestStride,
    const BYTE* pSrc,
    LONG        lSrcStride,
    DWORD       dwWidthInPixels,
    DWORD       dwHeightInPixels
    )
{
    for (DWORD y = 0; y < dwHeightInPixels; y++)
    {
        RGBQUAD             *pSrcPixel = (RGBQUAD*)pSrc;
        DXVA2_AYUVSample8   *pDestPixel = (DXVA2_AYUVSample8*)pDest;
        
        for (DWORD x = 0; x < dwWidthInPixels; x++)
        {
            pDestPixel[x].Alpha = 0x80;
            pDestPixel[x].Y = RGBtoY(pSrcPixel[x]);   
            pDestPixel[x].Cb = RGBtoU(pSrcPixel[x]);   
            pDestPixel[x].Cr = RGBtoV(pSrcPixel[x]);   
        }
        pDest += lDestStride;
        pSrc += lSrcStride;
    }
}
```



L'esempio seguente converte un'immagine RGB a 32 bit in un'immagine YV12. Questo esempio illustra come gestire un formato YUV planare. YV12 è un formato planare 4:2:0. In questo esempio la funzione mantiene tre puntatori separati per i tre piani nell'immagine di destinazione. Tuttavia, l'approccio di base è lo stesso dell'esempio precedente.


```C++
void RGB32_To_YV12(
    BYTE*       pDest,
    LONG        lDestStride,
    const BYTE* pSrc,
    LONG        lSrcStride,
    DWORD       dwWidthInPixels,
    DWORD       dwHeightInPixels
    )
{
    assert(dwWidthInPixels % 2 == 0);
    assert(dwHeightInPixels % 2 == 0);

    const BYTE *pSrcRow = pSrc;
    
    BYTE *pDestY = pDest;

    // Calculate the offsets for the V and U planes.

    // In YV12, each chroma plane has half the stride and half the height  
    // as the Y plane.
    BYTE *pDestV = pDest + (lDestStride * dwHeightInPixels);
    BYTE *pDestU = pDest + 
                   (lDestStride * dwHeightInPixels) + 
                   ((lDestStride * dwHeightInPixels) / 4);

    // Convert the Y plane.
    for (DWORD y = 0; y < dwHeightInPixels; y++)
    {
        RGBQUAD *pSrcPixel = (RGBQUAD*)pSrcRow;
        
        for (DWORD x = 0; x < dwWidthInPixels; x++)
        {
            pDestY[x] = RGBtoY(pSrcPixel[x]);    // Y0
        }
        pDestY += lDestStride;
        pSrcRow += lSrcStride;
    }

    // Convert the V and U planes.

    // YV12 is a 4:2:0 format, so each chroma sample is derived from four 
    // RGB pixels.
    pSrcRow = pSrc;
    for (DWORD y = 0; y < dwHeightInPixels; y += 2)
    {
        RGBQUAD *pSrcPixel = (RGBQUAD*)pSrcRow;
        RGBQUAD *pNextSrcRow = (RGBQUAD*)(pSrcRow + lSrcStride);

        BYTE *pbV = pDestV;
        BYTE *pbU = pDestU;

        for (DWORD x = 0; x < dwWidthInPixels; x += 2)
        {
            // Use a simple average to downsample the chroma.

            *pbV++ = ( RGBtoV(pSrcPixel[x]) +
                       RGBtoV(pSrcPixel[x + 1]) +       
                       RGBtoV(pNextSrcRow[x]) +         
                       RGBtoV(pNextSrcRow[x + 1]) ) / 4;        

            *pbU++ = ( RGBtoU(pSrcPixel[x]) +
                       RGBtoU(pSrcPixel[x + 1]) +       
                       RGBtoU(pNextSrcRow[x]) +         
                       RGBtoU(pNextSrcRow[x + 1]) ) / 4;    
        }
        pDestV += lDestStride / 2;
        pDestU += lDestStride / 2;
        
        // Skip two lines on the source image.
        pSrcRow += (lSrcStride * 2);
    }
}
```



In tutti questi esempi si presuppone che l'applicazione abbia già determinato lo stride dell'immagine. A volte è possibile ottenere queste informazioni dal buffer multimediale. In caso contrario, è necessario calcolarlo in base al formato video. Per altre informazioni sul calcolo dello stride dell'immagine e sull'uso dei buffer multimediali per i video, vedere [Buffer video non compressi](uncompressed-video-buffers.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tipi di supporti video](video-media-types.md)
</dt> <dt>

[Tipi di supporti](media-types.md)
</dt> </dl>

 

 
