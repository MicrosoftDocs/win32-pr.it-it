---
description: In questo argomento vengono presentate le origini bitmap, un componente di base di Windows Imaging Component (WIC) che rappresenta i pixel bitmap di un'immagine.
ms.assetid: cff0c088-ca22-4d55-9cf0-9cbe9803923e
title: Cenni preliminari sulle origini bitmap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 910bfc253798058639b98a1d1beaacec9bd4d1bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484780"
---
# <a name="bitmap-sources-overview"></a>Cenni preliminari sulle origini bitmap

In questo argomento vengono presentate le origini bitmap, un componente di base di Windows Imaging Component (WIC) che rappresenta i pixel bitmap di un'immagine.

In questo argomento sono contenute le sezioni seguenti.

-   [Origini bitmap](#bitmap-sources-overview)
-   [Frame bitmap](#bitmap-frames)
-   [Bitmap](#bitmap-sources-overview)
-   [Trasforma origini bitmap](#transform-bitmap-sources)
-   [Convertitori di contesto del colore e del formato pixel](#pixel-format-and-color-context-converters)
-   [Disegno di origini bitmap](#drawing-bitmap-sources)
-   [Argomenti correlati](#related-topics)

## <a name="bitmap-sources"></a>Origini bitmap

Il componente [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) è il blocco predefinito di base di WIC e rappresenta un singolo set di pixel. Un'origine bitmap può essere un singolo frame di un'immagine a più frame oppure il risultato di una trasformazione eseguita su un'origine bitmap. L'interfaccia **IWICBitmapSource** è la base di molte delle interfacce WIC principali, ad esempio il frame del decodificatore [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) e le origini bitmap di trasformazione, ad esempio [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator).

Nella tabella seguente vengono descritti i diversi componenti di origine della bitmap forniti da WIC.



| Origini bitmap                                                    | Descrizione                                                          |
|-------------------------------------------------------------------|----------------------------------------------------------------------|
| [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) | Rappresenta un frame di immagini del decodificatore.                                    |
| [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)                       | Fornisce la leggibilità e la rappresentazione in memoria alle origini bitmap. |
| [**IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper)         | Consente di eseguire il clip di un'origine bitmap a un rettangolo desiderato.                        |
| [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator) | Capovolge e/o ruota un'origine bitmap nell'orientamento desiderato.       |
| [**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler)           | Ridimensiona un'origine bitmap a una dimensione desiderata.                            |
| [**IWICColorTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolortransform)       | Trasforma il contesto del colore di un'origine bitmap.                     |
| [**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter)     | Converte il formato pixel di un'origine bitmap.                        |



 

## <a name="bitmap-frames"></a>Frame bitmap

Il [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) più comune è [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode). Questa interfaccia viene utilizzata per accedere ai dati bitmap effettivi di un formato di immagine. Molti formati di immagine supportano solo un singolo frame bitmap, mentre altri formati come GIF e TIFF supportano più frame per ogni immagine.

Per un esempio su come ottenere i frame bitmap da un'immagine, vedere l'argomento [How to retrieve the Frames of an image](https://www.bing.com/search?q=How+to+Retrieve+the+Frames+of+an+Image) .

## <a name="bitmaps"></a>Bitmap

Un [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) aggiunge i concetti di leggibilità e statica in memoria alle origini bitmap. Le bitmap WIC consentono agli utenti di accedere direttamente ai pixel di un'origine bitmap. Questo accesso diretto viene fornito dal metodo [**Lock**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmap-lock) e supporta qualsiasi combinazione di accesso in lettura e/o scrittura ai pixel bitmap. **Lock** Method blocca il rettangolo bitmap specificato e fornisce un oggetto [**IWICBitmapLock**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock) per accedere ai pixel.

Per un esempio di utilizzo degli oggetti [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) e [**IWICBitmapLock**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock) , vedere l'argomento [How to modify the pixels of a bitmap source](-wic-bitmapsources-howto-modifypixels.md) .

## <a name="transform-bitmap-sources"></a>Trasforma origini bitmap

WIC fornisce diverse interfacce [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) che trasformano i dati in pixel. In particolare, WIC fornisce le trasformazioni di origine bitmap per ridimensionare, ritagliare, ruotare e capovolgere i dati dei pixel. Queste trasformazioni di origine bitmap sono [**IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper), [**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler)e [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator). Ognuna di queste origini bitmap dispone di un metodo per inizializzare e creare una nuova origine bitmap trasformata. Ad esempio, **IWICBitmapClipper** include il metodo [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapclipper-initialize) . Questo metodo inizializza l'origine bitmap Clipper con i dati pixel ritagliati dell'origine della bitmap di input in corrispondenza del [**WICRect**](/windows/desktop/api/Wincodec/ns-wincodec-wicrect)specificato.

Nelle procedure seguenti vengono illustrati diversi utilizzi delle origini bitmap di trasformazione.

-   [Come ridimensionare un'origine bitmap](-wic-bitmapsources-howto-scale.md)
-   [Come ritagliare un'origine bitmap](-wic-bitmapsources-howto-clip.md)
-   [Come capovolgere e ruotare un'origine bitmap](-wic-bitmapsources-howto-flipandrotate.md)

## <a name="pixel-format-and-color-context-converters"></a>Convertitori di contesto del colore e del formato pixel

WIC fornisce anche origini bitmap che convertono il formato pixel e il contesto del colore di un'origine bitmap. WIC fornisce [**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter) e [**IWICColorTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolortransform) per queste operazioni.

[**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter) converte una determinata origine bitmap da un formato pixel a un altro.

Per un esempio di utilizzo di [**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter), vedere l'argomento [How to disegnato a bitmap source using Direct2D](-wic-bitmapsources-howto-drawusingd2d.md) .

## <a name="drawing-bitmap-sources"></a>Disegno di origini bitmap

WIC è una tecnologia di codec di immagini ancora utilizzata per gestire i dati e i metadati delle immagini e non fornisce in modo intrinseco un modo per eseguire il rendering delle immagini. Tuttavia, le origini bitmap possono essere disegnate con diverse tecnologie grafiche Windows come Direct2D, Windows Graphics Device Interface (GDI) e Windows GDI+. Ognuna di queste tecnologie ha un livello di interoperabilità diverso con WIC. Direct2D fornisce l'interoperabilità diretta tramite l'interfaccia [ID2D1Bitmap](../direct2d/render-targets-overview.md) e il metodo [ID2D1RenderTarget:: CreateBitmapFromWicBitmap](../direct2d/id2d1rendertarget-createbitmapfromwicbitmap.md) mentre GDI e GDI+ richiedono agli utenti di copiare i pixel di origine della bitmap in una [bitmap](../gdi/bitmaps.md).

Nell'esempio seguente viene illustrato come creare origini bitmap tramite Direct2D.

-   [Come creare un'origine bitmap usando Direct2D](-wic-bitmapsources-howto-drawusingd2d.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Panoramica del componente imaging Windows](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Panoramica della codifica](-wic-creating-encoder.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[Come scrivere un CODEC WIC-Enabled](-wic-howtowriteacodec.md)
</dt> </dl>

 

 
