---
description: Questo argomento descrive due concetti correlati, le proporzioni delle immagini e le proporzioni pixel.
ms.assetid: 384bdeaa-5360-42af-9f95-b791af2dcafc
title: Proporzioni immagine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71ae59cf213a9d44c9075f33be4bd422b81ced6dea270cf4fc9408990442529e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972983"
---
# <a name="picture-aspect-ratio"></a>Proporzioni immagine

Questo argomento descrive due concetti correlati, le proporzioni delle immagini e le proporzioni pixel. Descrive quindi in che modo questi concetti vengono espressi in Microsoft Media Foundation usando i tipi di supporti.

-   [Proporzioni immagine](#picture-aspect-ratio)
    -   [Creazione di lettere](#letterboxing)
    -   [Panoramica e analisi](#pan-and-scan)
-   [Proporzioni pixel](#pixel-aspect-ratio)
-   [Uso delle proporzioni](#working-with-aspect-ratios)
-   [Esempi di codice](#code-examples)
    -   [Ricerca dell'area di visualizzazione](#finding-the-display-area)
    -   [Conversione tra proporzioni pixel](#converting-between-pixel-aspect-ratios)
    -   [Calcolo dell'area Letterbox](#calculating-the-letterbox-area)
-   [Argomenti correlati](#related-topics)

## <a name="picture-aspect-ratio"></a>Proporzioni immagine

*Le proporzioni dell'immagine* definiscono la forma dell'immagine video visualizzata. Le proporzioni dell'immagine vengono notate X:Y, dove X:Y è il rapporto tra larghezza e altezza dell'immagine. La maggior parte degli standard video usa le proporzioni delle immagini 4:3 o 16:9. Le proporzioni 16:9 sono comunemente chiamate *widescreen.* Il film cinematografico usa spesso proporzioni 1:85:1 o 1:66:1. Le proporzioni dell'immagine sono *chiamate anche proporzioni di visualizzazione* (DAR).

![Diagramma che mostra le proporzioni 4:3 e 16:9](images/aspect-ratio01.png)

A volte l'immagine video non ha la stessa forma dell'area di visualizzazione. Ad esempio, un video 4:3 potrebbe essere visualizzato su un tv widescreen (16×9). Nel video del computer, il video potrebbe essere visualizzato all'interno di una finestra con dimensioni arbitrarie. In tal caso, l'immagine può essere adattata all'interno dell'area di visualizzazione in tre modi:

-   Estendere l'immagine lungo un asse per adattarla all'area di visualizzazione.
-   Ridimensionare l'immagine per adattarla all'area di visualizzazione, mantenendo le proporzioni dell'immagine originale.
-   Ritagliare l'immagine.

L'estensione dell'immagine per adattarla all'area di visualizzazione è quasi sempre errata, perché non mantiene le proporzioni corrette dell'immagine.

### <a name="letterboxing"></a>Creazione di lettere

Il processo di ridimensionamento di un'immagine widescreen per adattarla a uno schermo 4:3 è denominato *letterboxing*, illustrato nel diagramma successivo. Le aree rettangolari risultanti nella parte superiore e inferiore dell'immagine sono in genere riempite di nero, anche se è possibile usare altri colori.

![diagramma che mostra il modo corretto di letterbox](images/aspect-ratio02.png)

Il caso inverso, il ridimensionamento di un'immagine 4:3 per adattarla a uno schermo widescreen, viene talvolta chiamato *pillarboxing.* Tuttavia, il termine *letterbox* viene usato anche in senso generale, per indicare il ridimensionamento di un'immagine video per adattarla a una determinata area di visualizzazione.

![Diagramma che illustra pillarboxing](images/aspect-ratio03.png)

### <a name="pan-and-scan"></a>Panoramica e analisi

La panoramica e la scansione è una tecnica in base alla quale un'immagine widescreen viene ritagliata in un'area rettangolare 4×3, per la visualizzazione in un dispositivo di visualizzazione 4:3. L'immagine risultante riempie l'intero schermo, senza richiedere aree in formato letterbox nero, ma parti dell'immagine originale vengono ritagliate dall'immagine. L'area ritagliata può spostarsi da un frame all'altro, mentre l'area di interesse viene spostata. Il termine "panoramica" nella *panoramica* e nell'analisi si riferisce all'effetto di panoramica causato dallo spostamento dell'area di panoramica e analisi.

![Diagramma che illustra la panoramica e l'analisi](images/aspect-ratio04.png)

## <a name="pixel-aspect-ratio"></a>Proporzioni pixel

*Le proporzioni pixel* misurano la forma di un pixel.

Quando un'immagine digitale viene acquisita, l'immagine viene campionata sia verticalmente che orizzontalmente, con conseguente matrice rettangolare di campioni quantizzati, denominati *pixel* *o pels.* La forma della griglia di campionamento determina la forma dei pixel nell'immagine digitalizzata.

Di seguito è riportato un esempio che usa numeri piccoli per mantenere la matematica semplice. Si supponga che l'immagine originale sia quadrata, ovvero le proporzioni dell'immagine sono 1:1. e si supponga che la griglia di campionamento contenga 12 elementi disposti in una griglia 4×3. La forma di ogni pixel risultante sarà più alta rispetto alla larghezza. In particolare, la forma di ogni pixel sarà 3×4. I pixel che non sono quadrati sono detti *pixel non quadrati.*

![Diagramma che mostra una griglia di campionamento non quadrata](images/aspect-ratio05.png)

Le proporzioni pixel si applicano anche al dispositivo di visualizzazione. La forma fisica del dispositivo di visualizzazione e la risoluzione dei pixel fisici (su e giù) determinano il PAR del dispositivo di visualizzazione. I monitoraggi computer usano in genere pixel quadrati. Se l'immagine PAR e la visualizzazione PAR non corrispondono, è necessario ridimensionare l'immagine in una dimensione, verticalmente o orizzontalmente, per poter essere visualizzata correttamente. La formula seguente mette in relazione PAR, le proporzioni di visualizzazione (DAR) e le dimensioni dell'immagine in pixel:

*DAR* = ( larghezza *dell'immagine in pixel*  /  *altezza immagine in pixel*) × *PAR*

Si noti che la larghezza e l'altezza dell'immagine in questa formula fanno riferimento all'immagine in memoria, non all'immagine visualizzata.

Ecco un esempio reale: il video analogico NTSC-M contiene 480 linee di analisi nell'area dell'immagine attiva. ITU-R Rec. BT.601 specifica una frequenza di campionamento orizzontale di 704 pixel visibili per riga, producendo un'immagine digitale con 704 x 480 pixel. Le proporzioni dell'immagine prevista sono 4:3, producendo un PAR di 10:11.

-   DAR: 4:3
-   Larghezza in pixel: 704
-   Altezza in pixel: 480
-   PAR: 10/11

4/3 = (704/420) x (10/11)

Per visualizzare correttamente questa immagine in un dispositivo di visualizzazione con pixel quadrati, è necessario ridimensionare la larghezza di 10/11 o l'altezza di 11/10.

## <a name="working-with-aspect-ratios"></a>Uso delle proporzioni

La forma corretta di un fotogramma video è definita dalle proporzioni *pixel* (PAR) e dall'area *di visualizzazione.*

-   Par definisce la forma dei pixel in un'immagine. I pixel quadrati hanno proporzioni di 1:1. Qualsiasi altra proporzione descrive un pixel non quadrato. Ad esempio, NTSC tv usa un PAR 10:11. Supponendo che il video sia presentato su un monitor del computer, lo schermo avrà pixel quadrati (PAR 1:1). Il par del contenuto di origine è specificato nell'attributo [**\_ MF MT \_ PIXEL ASPECT \_ \_ RATIO**](mf-mt-pixel-aspect-ratio-attribute.md) sul tipo di supporto.
-   L'area di visualizzazione è l'area dell'immagine video che deve essere visualizzata. Nel tipo di supporto possono essere specificate due aree di visualizzazione pertinenti:
    -   Apertura di panoramica e analisi. L'apertura di panoramica e scansione è un'area video di 4×3 che deve essere visualizzata in modalità panoramica/scansione. Viene usato per visualizzare il contenuto a schermo wide su uno schermo a 4×3 senza letterboxing. L'apertura di panoramica e analisi viene specificata nell'attributo [**\_ MF MT \_ PAN SCAN \_ \_ APERTURE**](mf-mt-pan-scan-aperture-attribute.md) e deve essere usata solo quando l'attributo [**\_ MF MT PAN SCAN \_ \_ \_ ENABLED**](mf-mt-pan-scan-enabled-attribute.md) è **TRUE.**
    -   Apertura della visualizzazione. Questa apertura è definita in alcuni standard video. Qualsiasi elemento esterno all'apertura dello schermo è l'area overscan e non deve essere visualizzato. Ad esempio, la tv NTSC è di 720×480 pixel con un'apertura di visualizzazione di 704×480. L'apertura di visualizzazione è specificata [**nell'attributo \_ MF MT \_ MINIMUM \_ DISPLAY \_ APERTURE.**](mf-mt-minimum-display-aperture-attribute.md) Se presente, deve essere usato quando la modalità di panoramica e analisi è **FALSE.**

Se la modalità pan-and-can **è IMPOSTATA SU FALSE** e non è stata definita alcuna apertura di visualizzazione, verrà visualizzato l'intero fotogramma video. In realtà, questo è il caso della maggior parte dei contenuti video diversi da quelli per la tv e i DVD. Le proporzioni dell'intera immagine vengono calcolate come ( altezza *area* di visualizzazione larghezza area di visualizzazione  /  ) × *PAR*.

## <a name="code-examples"></a>Esempi di codice

### <a name="finding-the-display-area"></a>Ricerca dell'area di visualizzazione

Il codice seguente illustra come ottenere l'area di visualizzazione dal tipo di supporto.


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



### <a name="converting-between-pixel-aspect-ratios"></a>Conversione tra proporzioni pixel

Il codice seguente illustra come convertire un rettangolo da un pixel proporzioni (PAR) a un altro, mantenendo le proporzioni dell'immagine.


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



### <a name="calculating-the-letterbox-area"></a>Calcolo dell'area Letterbox

Il codice seguente calcola l'area letterbox, dati un rettangolo di origine e di destinazione. Si presuppone che entrambi i rettangoli hanno lo stesso PAR.


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

[Tipi di supporti](media-types.md)
</dt> <dt>

[Tipi di supporti video](video-media-types.md)
</dt> <dt>

[**MF \_ MT \_ MINIMUM \_ DISPLAY \_ APERTURE**](mf-mt-minimum-display-aperture-attribute.md)
</dt> <dt>

[**MF \_ MT \_ PAN \_ SCAN \_ APERTURE**](mf-mt-pan-scan-aperture-attribute.md)
</dt> <dt>

[**MF MT PAN SCAN ENABLED (ANALISI \_ PANORAMICA MT \_ MF \_ \_ ABILITATA)**](mf-mt-pan-scan-enabled-attribute.md)
</dt> <dt>

[**PROPORZIONI \_ DEI PIXEL MF MT \_ \_ \_**](mf-mt-pixel-aspect-ratio-attribute.md)
</dt> </dl>

 

 



