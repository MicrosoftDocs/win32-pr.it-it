---
description: Stride immagine
ms.assetid: 13cd1106-48b3-4522-ac09-8efbaab5c31d
title: Stride immagine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 813c0f3d99297758761bdfb5973fc2b16e3339f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104556888"
---
# <a name="image-stride"></a>Stride immagine

Quando un'immagine video è archiviata in memoria, il buffer di memoria potrebbe contenere byte di riempimento aggiuntivi dopo ogni riga di pixel. I byte di riempimento influiscono sulla modalità di archiviazione dell'immagine in memoria, ma non influiscono sulla modalità di visualizzazione dell'immagine.

Lo *stride* è il numero di byte da una riga di pixel in memoria alla riga successiva di pixel in memoria. Stride viene anche chiamato *pitch*. Se sono presenti byte di riempimento, lo stride è più ampio della larghezza dell'immagine, come illustrato nella figura seguente.

![diagramma che mostra un'immagine più la spaziatura interna.](images/c85c6a40-f0a8-48a3-b465-39ceada66339.gif)

Due buffer che contengono fotogrammi video con dimensioni uguali possono avere due diversi stride. Se si elabora un'immagine video, è necessario tenere conto dello stride.

Inoltre, è possibile disporre in memoria di un'immagine in due modi. In un'immagine dall' *alto verso il basso* , la prima riga di pixel nell'immagine viene visualizzata per prima in memoria. In un'immagine dal *basso in alto* , l'ultima riga di pixel viene visualizzata per prima nella memoria. Nella figura seguente viene illustrata la differenza tra un'immagine dall'alto verso il basso e un'immagine dal basso in alto.

![diagramma che mostra le immagini dall'alto verso il basso e dal basso verso l'alto.](images/f03bd9ff-0cf3-4a56-88c5-5b8c44637272.gif)

Un'immagine dal basso verso l'alto ha un stride negativo, perché lo stride viene definito come il numero di byte necessario per spostarsi verso il basso di una riga di pixel rispetto all'immagine visualizzata. Le immagini YUV devono sempre essere dall'alto verso il basso e qualsiasi immagine contenuta in una superficie Direct3D deve essere dall'alto verso il basso. Le immagini RGB nella memoria di sistema sono in genere dal basso verso l'alto.

Le trasformazioni video in particolare devono gestire i buffer con stride non corrispondenti, perché il buffer di input potrebbe non corrispondere al buffer di output. Si supponga, ad esempio, di voler convertire un'immagine di origine e scrivere il risultato in un'immagine di destinazione. Si supponga che entrambe le immagini abbiano la stessa larghezza e altezza, ma che potrebbero non avere lo stesso formato pixel o lo stesso stride di immagine.

Nell'esempio di codice riportato di seguito viene illustrato un approccio generalizzato per la scrittura di questo tipo di funzione. Non si tratta di un esempio di funzionamento completo, perché astrae molti dei dettagli specifici.


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

L'idea generale è elaborare una riga alla volta, scorrendo ogni pixel della riga. Si supponga che il tipo di pixel di origine \_ \_ e il \_ \_ tipo di pixel dest siano strutture che rappresentano rispettivamente il layout dei pixel per le immagini di origine e di destinazione. Ad esempio, RGB a 32 bit usa la struttura [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) . Non ogni formato pixel ha una struttura predefinita.) Il cast del puntatore di matrice al tipo di struttura consente di accedere ai componenti RGB o YUV di ogni pixel. All'inizio di ogni riga, la funzione Archivia un puntatore alla riga. Alla fine della riga, il puntatore viene incrementato in base alla larghezza dello stride dell'immagine, che sposta il puntatore alla riga successiva.

In questo esempio viene chiamata una funzione ipotetica denominata TransformPixelValue per ogni pixel. Potrebbe trattarsi di qualsiasi funzione che calcola un pixel di destinazione da un pixel di origine. Naturalmente, i dettagli esatti dipenderanno dall'attività specifica. Se, ad esempio, si dispone di un formato YUV planare, è necessario accedere ai piani Chroma indipendentemente dal piano Luma; con video interlacciato, potrebbe essere necessario elaborare i campi separatamente. e così via.

Per fornire un esempio più concreto, il codice seguente converte un'immagine RGB a 32 bit in un'immagine AYUV. È possibile accedere ai pixel RGB usando una struttura [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) e si accede ai pixel AYUV usando una struttura della struttura [**DXVA2 \_ AYUVSample8**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_ayuvsample8) .


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



Nell'esempio seguente viene convertita un'immagine RGB a 32 bit in un'immagine YV12. Questo esempio illustra come gestire un formato YUV planare. (YV12 è un formato Planar 4:2:0). In questo esempio, la funzione mantiene tre puntatori distinti per i tre piani nell'immagine di destinazione. Tuttavia, l'approccio di base è identico a quello dell'esempio precedente.


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



In tutti questi esempi, si presuppone che l'applicazione abbia già determinato lo stride dell'immagine. A volte è possibile ottenere queste informazioni dal buffer multimediale. In caso contrario, è necessario calcolarlo in base al formato video. Per altre informazioni sul calcolo dello stride dell'immagine e sull'uso di buffer multimediali per video, vedere [buffer video non compressi](uncompressed-video-buffers.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tipi di supporti video](video-media-types.md)
</dt> <dt>

[Tipi di supporto](media-types.md)
</dt> </dl>

 

 
