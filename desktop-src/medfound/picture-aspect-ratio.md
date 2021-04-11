---
description: In questo argomento vengono descritti due concetti correlati, proporzioni dell'immagine e proporzioni in pixel.
ms.assetid: 384bdeaa-5360-42af-9f95-b791af2dcafc
title: Proporzioni immagine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74e81f1b8e26af753a5c8c1bc7ecb09d8a658582
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226514"
---
# <a name="picture-aspect-ratio"></a>Proporzioni immagine

In questo argomento vengono descritti due concetti correlati, proporzioni dell'immagine e proporzioni in pixel. Viene quindi descritto come questi concetti vengono espressi in Microsoft Media Foundation utilizzando i tipi di supporto.

-   [Proporzioni immagine](#picture-aspect-ratio)
    -   [Letterboxing](#letterboxing)
    -   [Pan-and-Scan](#pan-and-scan)
-   [Proporzioni pixel](#pixel-aspect-ratio)
-   [Utilizzo delle proporzioni](#working-with-aspect-ratios)
-   [Esempi di codice](#code-examples)
    -   [Ricerca dell'area di visualizzazione](#finding-the-display-area)
    -   [Conversione tra proporzioni in pixel](#converting-between-pixel-aspect-ratios)
    -   [Calcolo dell'area letterbox](#calculating-the-letterbox-area)
-   [Argomenti correlati](#related-topics)

## <a name="picture-aspect-ratio"></a>Proporzioni immagine

Proporzioni *immagine* definisce la forma dell'immagine video visualizzata. L'aspetto dell'immagine è X:Y, dove X:Y è il rapporto tra la larghezza dell'immagine e l'altezza dell'immagine. La maggior parte degli standard video usa proporzioni dell'immagine 4:3 o 16:9. Le proporzioni 16:9 sono comunemente denominate *widescreen*. Cinema film usa spesso una proporzione 1:85:1 o 1:66:1. Le proporzioni dell'immagine sono denominate anche proporzioni di *visualizzazione* (Dar).

![diagramma che mostra le proporzioni 4:3 e 16:9](images/aspect-ratio01.png)

In alcuni casi l'immagine video non ha la stessa forma dell'area di visualizzazione. Ad esempio, un video 4:3 potrebbe essere visualizzato su un televisore widescreen (16 × 9). Nel video del computer il video potrebbe essere visualizzato all'interno di una finestra con dimensioni arbitrarie. In tal caso, è possibile creare l'immagine in tre modi per adattarla all'area di visualizzazione:

-   Estendere l'immagine lungo un asse per adattarla all'area di visualizzazione.
-   Ridimensionare l'immagine per adattarla all'area di visualizzazione, mantenendo le proporzioni originali dell'immagine.
-   Ritagliare l'immagine.

L'adattamento dell'immagine per adattarla all'area di visualizzazione è quasi sempre errato, perché non mantiene le proporzioni dell'immagine corrette.

### <a name="letterboxing"></a>Letterboxing

Il processo di ridimensionamento di un'immagine widescreen per adattarsi a una visualizzazione 4:3 è denominato *letterbox*, illustrato nel diagramma seguente. Le aree rectanglular risultanti nella parte superiore e inferiore dell'immagine vengono in genere compilate con il nero, sebbene sia possibile utilizzare altri colori.

![diagramma che mostra la modalità corretta per la letterbox](images/aspect-ratio02.png)

In caso contrario, il ridimensionamento di un'immagine 4:3 per adattarsi a una visualizzazione widescreen viene talvolta denominato *pillarbox*. Tuttavia, il termine *letterbox* viene anche usato in senso generale, per indicare la scalabilità di un'immagine video per adattarsi a qualsiasi area di visualizzazione specificata.

![diagramma che mostra pillarbox](images/aspect-ratio03.png)

### <a name="pan-and-scan"></a>Pan-and-Scan

Pan-and-Scan è una tecnica per cui un'immagine in formato widescreen viene ritagliata in un'area rettangolare da 4 × 3, per la visualizzazione in un dispositivo di visualizzazione 4:3. L'immagine risultante riempie l'intero schermo, senza richiedere le aree della cassetta nera, ma le parti dell'immagine originale vengono ritagliate dall'immagine. L'area ritagliata può spostarsi dal fotogramma al frame, in quanto l'area di interesse viene spostata. Il termine "Pan" in *Pan-and-Scan* si riferisce all'effetto di panning causato dallo spostamento dell'area di Pan-and-Scan.

![diagramma che illustra la Panoramica di Pan-and-Scan](images/aspect-ratio04.png)

## <a name="pixel-aspect-ratio"></a>Proporzioni pixel

Proporzioni *pixel* (par) misura la forma di un pixel.

Quando viene acquisita un'immagine digitale, l'immagine viene campionata verticalmente e orizzontalmente, ottenendo una matrice rettangolare di campioni quantizzati, denominati *pixel* o *Pels*. La forma della griglia di campionamento determina la forma dei pixel nell'immagine digitalizzata.

Di seguito è riportato un esempio che usa piccoli numeri per semplificare la matematica. Si supponga che l'immagine originale sia quadrata (ovvero, le proporzioni dell'immagine sono 1:1); e si supponga che la griglia di campionamento includa 12 elementi, disposti in una griglia di 4 × 3. La forma di ogni pixel risultante sarà più alta rispetto a quella estesa. In particolare, la forma di ogni pixel sarà 3 × 4. I pixel che non sono quadrati sono detti *pixel non quadrati*.

![diagramma che mostra una griglia di campionamento non quadrato](images/aspect-ratio05.png)

Le proporzioni dei pixel si applicano anche al dispositivo di visualizzazione. La forma fisica del dispositivo di visualizzazione e la risoluzione dei pixel fisici (in orizzontale e in basso) determinano la PAR del dispositivo di visualizzazione. I monitoraggi computer utilizzano in genere pixel quadrati. Se la par dell'immagine e la PAR della visualizzazione non corrispondono, l'immagine deve essere ridimensionata in una dimensione, verticalmente o orizzontalmente, per poter essere visualizzata correttamente. La formula seguente mette in relazione PAR, Display aspect ratio (DAR) e dimensioni dell'immagine in pixel:

*Dar* = (*Larghezza immagine* in pixel  /  *altezza in pixel*) × *par*

Si noti che la larghezza dell'immagine e l'altezza dell'immagine in questa formula fanno riferimento all'immagine in memoria, non all'immagine visualizzata.

Ecco un esempio reale: il video analogico NTSC-M contiene 480 righe di analisi nell'area immagine attiva. ITU-R REC. BT. 601 specifica una frequenza di campionamento orizzontale di 704 pixel visibili per riga, restituendo un'immagine digitale con 704 x 480 pixel. Le proporzioni dell'immagine desiderate sono pari a 4:3, ottenendo un valore pari a 10:11.

-   DAR: 4:3
-   Larghezza in pixel: 704
-   Altezza in pixel: 480
-   PAR: 10/11

4/3 = (704/420) x (10/11)

Per visualizzare correttamente questa immagine in un dispositivo di visualizzazione con pixel quadrati, è necessario ridimensionare la larghezza di 10/11 o l'altezza di 11/10.

## <a name="working-with-aspect-ratios"></a>Utilizzo delle proporzioni

La forma corretta di un frame video è definita dalle proporzioni in *pixel* (par) e dall' *area di visualizzazione*.

-   Il PAR definisce la forma dei pixel in un'immagine. I pixel quadrati hanno proporzioni pari a 1:1. Tutte le altre proporzioni descrivono un pixel non quadrato. Ad esempio, la televisione NTSC USA un 10:11 PAR. Supponendo che si stia visualizzando il video in un monitor del computer, la visualizzazione avrà i pixel quadrati (1:1 PAR). La PAR del contenuto di origine viene specificata nell'attributo [**delle \_ \_ \_ proporzioni \_ del pixel MF mt**](mf-mt-pixel-aspect-ratio-attribute.md) sul tipo di supporto.
-   L'area di visualizzazione è l'area dell'immagine video che deve essere visualizzata. Esistono due aree di visualizzazione rilevanti che possono essere specificate nel tipo di supporto:
    -   Apertura Pan-and-Scan. L'apertura Pan-and-Scan è un'area di video da 4 × 3 che dovrebbe essere visualizzata in modalità Pan/Scan. Viene usato per mostrare contenuto a schermo intero in una visualizzazione 4 × 3 senza letterbox. L'apertura di Pan-and-Scan è specificata nell'attributo dell'apertura di Pan [**\_ \_ \_ \_ Scan MF mt**](mf-mt-pan-scan-aperture-attribute.md) e deve essere usata solo quando l'attributo [**MF \_ mt \_ Pan \_ Scan \_ Enabled**](mf-mt-pan-scan-enabled-attribute.md) è **true**.
    -   Visualizza apertura. Questa apertura è definita in alcuni standard video. Qualsiasi elemento all'esterno dell'apertura di visualizzazione è l'area di overscan e non deve essere visualizzato. Ad esempio, la televisione NTSC è 720 × 480 pixel con un diaframma di visualizzazione di 704 × 480. L'apertura di visualizzazione viene specificata nell'attributo di [**\_ \_ \_ \_ apertura della visualizzazione minima MF mt**](mf-mt-minimum-display-aperture-attribute.md) . Se presente, deve essere usato quando la modalità Pan-and-Scan è **false**.

Se la modalità Pan-and-can è **false** e non è definita alcuna apertura di visualizzazione, verrà visualizzato l'intero frame video. In realtà, questo è il caso per la maggior parte dei contenuti video diversi dalla televisione e dal video DVD. Le proporzioni dell'intera immagine vengono calcolate come (  /  *Altezza area di visualizzazione* Larghezza area di visualizzazione) × *par*.

## <a name="code-examples"></a>Esempi di codice

### <a name="finding-the-display-area"></a>Ricerca dell'area di visualizzazione

Nel codice seguente viene illustrato come ottenere l'area di visualizzazione dal tipo di supporto.


```C++
MFVideoArea MakeArea(float x, float y, DWORD width, DWORD height);

HRESULT GetVideoDisplayArea(IMFMediaType *pType, MFVideoArea *pArea)
{
    HRESULT hr = S_OK;
    BOOL bPanScan = FALSE;
    UINT32 width = 0, height = 0;

    bPanScan = MFGetAttributeUINT32(pType, MF_MT_PAN_SCAN_ENABLED, FALSE);

    // In pan-and-scan mode, try to get the pan-and-scan region.
    if (bPanScan)
    {
        hr = pType->GetBlob(MF_MT_PAN_SCAN_APERTURE, (UINT8*)pArea, 
            sizeof(MFVideoArea), NULL);
    }

    // If not in pan-and-scan mode, or the pan-and-scan region is not set, 
    // get the minimimum display aperture.

    if (!bPanScan || hr == MF_E_ATTRIBUTENOTFOUND)
    {
        hr = pType->GetBlob(MF_MT_MINIMUM_DISPLAY_APERTURE, (UINT8*)pArea, 
            sizeof(MFVideoArea), NULL);

        if (hr == MF_E_ATTRIBUTENOTFOUND)
        {
            // Minimum display aperture is not set.

            // For backward compatibility with some components, 
            // check for a geometric aperture. 

            hr = pType->GetBlob(MF_MT_GEOMETRIC_APERTURE, (UINT8*)pArea, 
                sizeof(MFVideoArea), NULL);
        }

        // Default: Use the entire video area.

        if (hr == MF_E_ATTRIBUTENOTFOUND)
        {
            hr = MFGetAttributeSize(pType, MF_MT_FRAME_SIZE, &width, &height);

            if (SUCCEEDED(hr))
            {
                *pArea = MakeArea(0.0, 0.0, width, height);
            }
        }
    }
    return hr;
}
```




```C++
MFOffset MakeOffset(float v)
{
    MFOffset offset;
    offset.value = short(v);
    offset.fract = WORD(65536 * (v-offset.value));
    return offset;
}
```




```C++
MFVideoArea MakeArea(float x, float y, DWORD width, DWORD height)
{
    MFVideoArea area;
    area.OffsetX = MakeOffset(x);
    area.OffsetY = MakeOffset(y);
    area.Area.cx = width;
    area.Area.cy = height;
    return area;
}
```



### <a name="converting-between-pixel-aspect-ratios"></a>Conversione tra proporzioni in pixel

Nel codice riportato di seguito viene illustrato come convertire un rettangolo da una proporzioni in pixel (PAR) a un altro, mantenendo le proporzioni dell'immagine.


```C++
//-----------------------------------------------------------------------------
// Converts a rectangle from one pixel aspect ratio (PAR) to another PAR.
// Returns the corrected rectangle.
//
// For example, a 720 x 486 rect with a PAR of 9:10, when converted to 1x1 PAR,
// must be stretched to 720 x 540.
//-----------------------------------------------------------------------------

RECT CorrectAspectRatio(const RECT& src, const MFRatio& srcPAR, const MFRatio& destPAR)
{
    // Start with a rectangle the same size as src, but offset to (0,0).
    RECT rc = {0, 0, src.right - src.left, src.bottom - src.top};

    // If the source and destination have the same PAR, there is nothing to do.
    // Otherwise, adjust the image size, in two steps:
    //  1. Transform from source PAR to 1:1
    //  2. Transform from 1:1 to destination PAR.

    if ((srcPAR.Numerator != destPAR.Numerator) || 
        (srcPAR.Denominator != destPAR.Denominator))
    {
        // Correct for the source's PAR.

        if (srcPAR.Numerator > srcPAR.Denominator)
        {
            // The source has "wide" pixels, so stretch the width.
            rc.right = MulDiv(rc.right, srcPAR.Numerator, srcPAR.Denominator);
        }
        else if (srcPAR.Numerator < srcPAR.Denominator)
        {
            // The source has "tall" pixels, so stretch the height.
            rc.bottom = MulDiv(rc.bottom, srcPAR.Denominator, srcPAR.Numerator);
        }
        // else: PAR is 1:1, which is a no-op.

        // Next, correct for the target's PAR. This is the inverse operation of 
        // the previous.

        if (destPAR.Numerator > destPAR.Denominator)
        {
            // The destination has "wide" pixels, so stretch the height.
            rc.bottom = MulDiv(rc.bottom, destPAR.Numerator, destPAR.Denominator);
        }
        else if (destPAR.Numerator < destPAR.Denominator)
        {
            // The destination has "tall" pixels, so stretch the width.
            rc.right = MulDiv(rc.right, destPAR.Denominator, destPAR.Numerator);
        }
        // else: PAR is 1:1, which is a no-op.
    }
    return rc;
}
```



### <a name="calculating-the-letterbox-area"></a>Calcolo dell'area letterbox

Il codice seguente calcola l'area Letterbox, dato un rettangolo di origine e di destinazione. Si presuppone che entrambi i rettangoli abbiano lo stesso PAR.


```C++
RECT LetterBoxRect(const RECT& rcSrc, const RECT& rcDst)
{
    // Compute source/destination ratios.
    int iSrcWidth  = rcSrc.right - rcSrc.left;
    int iSrcHeight = rcSrc.bottom - rcSrc.top;

    int iDstWidth  = rcDst.right - rcDst.left;
    int iDstHeight = rcDst.bottom - rcDst.top;

    int iDstLBWidth;
    int iDstLBHeight;

    if (MulDiv(iSrcWidth, iDstHeight, iSrcHeight) <= iDstWidth) 
    {
        // Column letterboxing ("pillar box")
        iDstLBWidth  = MulDiv(iDstHeight, iSrcWidth, iSrcHeight);
        iDstLBHeight = iDstHeight;
    }
    else 
    {
        // Row letterboxing.
        iDstLBWidth  = iDstWidth;
        iDstLBHeight = MulDiv(iDstWidth, iSrcHeight, iSrcWidth);
    }

    // Create a centered rectangle within the current destination rect

    LONG left = rcDst.left + ((iDstWidth - iDstLBWidth) / 2);
    LONG top = rcDst.top + ((iDstHeight - iDstLBHeight) / 2);

    RECT rc;
    SetRect(&rc, left, top, left + iDstLBWidth, top + iDstLBHeight);
    return rc;
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tipi di supporto](media-types.md)
</dt> <dt>

[Tipi di supporti video](video-media-types.md)
</dt> <dt>

[**\_ \_ \_ apertura minima schermo \_ MF mt**](mf-mt-minimum-display-aperture-attribute.md)
</dt> <dt>

[**\_apertura dell' \_ analisi della panoramica MF mt \_ \_**](mf-mt-pan-scan-aperture-attribute.md)
</dt> <dt>

[**\_ \_ Analisi panoramica MF \_ mt \_ abilitata**](mf-mt-pan-scan-enabled-attribute.md)
</dt> <dt>

[**proporzioni MF \_ mt \_ pixel \_ \_**](mf-mt-pixel-aspect-ratio-attribute.md)
</dt> </dl>

 

 



