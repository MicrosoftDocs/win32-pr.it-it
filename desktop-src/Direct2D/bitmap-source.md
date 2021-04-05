---
title: Effetto origine bitmap
description: Usare l'effetto origine bitmap per generare un ID2D1Image da un IWICBitmapSource da usare come input in un grafico effetto.
ms.assetid: 86646111-208A-4E6D-A28C-7B23A1742D24
keywords:
- effetto origine bitmap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a439c94f0f520b318b3cb3511775dbec58b6e139
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874469"
---
# <a name="bitmap-source-effect"></a>Effetto origine bitmap

Usare l'effetto origine bitmap per generare un [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) da un [**IWICBitmapSource**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource) da usare come input in un grafico effetto. Questo effetto esegue la scalabilità e la rotazione sulla CPU. Può anche generare facoltativamente una memoria di sistema mipmap, che può essere un'ottimizzazione delle prestazioni per scalare attivamente immagini di grandi dimensioni con diverse soluzioni ridotte.

> [!Note]  
> L'effetto origine bitmap accetta il proprio input come proprietà, non come input di immagine. È necessario [**usare il metodo SetValue,**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32)) non il metodo [**seinput**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1effect-setinput) . La proprietà *WicBitmapSource* è la posizione in cui si specificano i dati di input dell'immagine.

 

Il CLSID per questo effetto è CLSID \_ D2D1BitmapSource.

-   [Proprietà effetto](#effect-properties)
-   [Modalità di interpolazione](#interpolation-modes)
-   [Orientamento](#orientation)
-   [Modalità Alpha](#alpha-modes)
-   [Osservazioni:](#remarks)
-   [Requisiti](#requirements)
-   [Argomenti correlati](#related-topics)

## <a name="effect-properties"></a>Proprietà effetto



| Nome visualizzato e enumerazione dell'indice                                                          | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WicBitmapSource<br/> D2D1 \_ BITMAPSOURCE \_ prop \_ WIC \_ bitmap \_ source<br/>         | [IWICBitmapSource](/windows/desktop/wic/-wic-imp-iwicbitmapsource) contenente i dati dell'immagine da caricare.<br/> Il tipo è [IWICBitmapSource](/windows/desktop/wic/-wic-imp-iwicbitmapsource).<br/> Il valore predefinito è NULL.<br/>                                                                                                                                                                                                                   |
| Scalabilità<br/> \_Scala della \_ prop d2d1 BITMAPSOURCE \_<br/>                                 | Importo della scala nella direzione X e Y. L'effetto moltiplica la larghezza per il valore X e l'altezza in base al valore Y. Questa proprietà è un D2D1 \_ vector \_ 2F definito come: (scala X, scala Y). Gli importi di scala sono FLOAT, unità e devono essere positivi o 0.<br/> Il tipo è D2D1 \_ vector \_ 2F.<br/> Il valore predefinito è {1.0 f, 1.0 f}.<br/>                                                                           |
| InterpolationMode.<br/> \_Modalità di \_ \_ interpolazione della Prop \_ d2d1 di BITMAPSOURCE<br/>      | Modalità di interpolazione utilizzata per ridimensionare l'immagine. Per altre informazioni, vedere [modalità di interpolazione](#interpolation-modes) .<br/> Se la modalità disabilita la mipmap, BitmapSouce memorizza nella cache l'immagine in base alla risoluzione determinata dalle proprietà scale e EnableDPICorrection.<br/> Il tipo è D2D1 \_ \_ modalità di interpolazione BITMAPSOURCE \_ .<br/> Il valore predefinito è la \_ \_ modalità di interpolazione d2d1 di BITMAPSOURCE \_ \_ lineare.<br/> |
| EnableDPICorrection<br/> D2D1 \_ BITMAPSOURCE \_ prop \_ Abilita \_ \_ correzione dpi<br/> | Se si imposta questa impostazione su TRUE, l'effetto scalarà l'immagine di input per convertire il valore DPI segnalato da [**IWICBitmapSource**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource) in dpi del contesto di dispositivo. L'effetto utilizza la modalità di interpolazione impostata con la proprietà InterpolationMode. Se si imposta su FALSE, l'effetto utilizzerà un valore DPI di 96,0 per l'immagine di output.<br/> Il tipo è BOOL.<br/> Il valore predefinito è FALSE.<br/>   |
| AlphaMode<br/> \_ \_ \_ Modalità Alpha della Prop \_ d2d1 di BITMAPSOURCE<br/>                       | Modalità Alpha dell'output. Può essere premoltiplicato o lineare. Per altre informazioni, vedere [modalità Alpha](#alpha-modes) .<br/> Il tipo è D2D1 \_ BITMAPSOURCE \_ Alpha \_ mode.<br/> Il valore predefinito è D2D1 \_ BITMAPSOURCE \_ Alpha \_ mode \_ premoltiplicato.<br/>                                                                                                                                                              |
| Orientamento<br/> \_Orientamento della \_ prop d2d1 BITMAPSOURCE \_<br/>                     | Operazione di capovolgimento e/o rotazione da eseguire sull'immagine. Per altre informazioni, vedere [orientamento](#orientation) .<br/> Il tipo è D2D1 \_ BITMAPSOURCE \_ Orientation.<br/> Il valore predefinito è D2D1 \_ BITMAPSOURCE \_ Orientation \_ default.<br/>                                                                                                                                                                                 |



 

## <a name="interpolation-modes"></a>Modalità di interpolazione

L'effetto esegue l'interpolazione usando questa modalità quando ridimensiona un'immagine o quando corregge il valore DPI. Le modalità di interpolazione utilizzate da questo effetto vengono calcolate dalla CPU, non dalla GPU.



| Nome                                                       | Descrizione                                                                                                                                                                                                                          |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_Modalità di \_ interpolazione BITMAPSOURCE d2d1 \_ \_ più \_ vicina | Campiona il punto singolo più vicino e lo utilizza. Non genera un mipmap.                                                                                                                                                           |
| D2D1 \_ \_ modalità di interpolazione BITMAPSOURCE \_ \_ lineare            | Usa un esempio a quattro punti e un'interpolazione lineare. Non genera un mipmap.                                                                                                                                                        |
| D2D1 \_ \_ modalità di interpolazione BITMAPSOURCE \_ \_ cubica             | Usa un kernel cubico di esempio 16 per l'interpolazione. Non genera un mipmap.                                                                                                                                                          |
| D2D1 \_ \_ modalità di interpolazione BITMAPSOURCE \_ \_ fant              | Utilizza l'interpolazione Fant di WIC, uguale all'interfaccia [**IWICBitmapScaler**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapscaler) . Non genera un mipmap.                                                                                       |
| D2D1 \_ \_ modalità di interpolazione BITMAPSOURCE \_ \_ MIPMAP \_ lineare    | Genera la catena mipmap nella memoria di sistema usando l'interpolazione bilineare. Per ogni mipmap, l'effetto si ridimensiona al multiplo più vicino di 0,5 usando l'interpolazione bilineare e quindi ridimensiona la quantità rimanente usando l'interpolazione lineare. |



 

## <a name="orientation"></a>Orientamento

La proprietà Orientation può essere usata per applicare un flag di orientamento EXIF incorporato in un'immagine.



| Nome                                                                    | Descrizione                                                        |
|-------------------------------------------------------------------------|--------------------------------------------------------------------|
| \_ \_ Impostazione predefinita orientamento d2d1 BITMAPSOURCE \_                                | Valore predefinito. L'effetto non modifica l'orientamento dell'input.   |
| D2D1 \_ \_ \_ Capovolgi orientamento \_ orizzontale                       | Capovolge l'immagine orizzontalmente.                                      |
| Orientamento di D2D1 \_ BITMAPSOURCE \_ \_ ruotare \_ CLOCKWISE180                   | Ruota l'immagine in senso orario di 180 gradi.                           |
| D2D1 \_ BITMAPSOURCE \_ Orientation \_ ruotare \_ CLOCKWISE180 \_ Flip \_ Horizontal | Ruota l'immagine in senso orario di 180 gradi e la capovolge orizzontalmente. |
| D2D1 \_ BITMAPSOURCE \_ Orientation \_ ruotare \_ CLOCKWISE270 \_ Flip \_ Horizontal | Ruota l'immagine in senso orario di 270 gradi e la capovolge orizzontalmente. |
| Orientamento di D2D1 \_ BITMAPSOURCE \_ \_ ruotare \_ CLOCKWISE90                    | Ruota l'immagine in senso orario di 90 gradi.                            |
| D2D1 \_ BITMAPSOURCE \_ Orientation \_ ruotare \_ CLOCKWISE90 \_ Flip \_ Horizontal  | Ruota l'immagine in senso orario di 90 gradi e la capovolge orizzontalmente.  |
| Orientamento di D2D1 \_ BITMAPSOURCE \_ \_ ruotare \_ CLOCKWISE270                   | Ruota l'immagine in senso orario di 270 gradi.                           |



 

Questo frammento di codice illustra come eseguire la conversione dai valori di orientamento EXIF (definiti in propkey. h) ai valori di orientamento di D2D1 \_ BITMAPSOURCE \_ .


```C++
#include <propkey.h>
#include <d2d1effects.h>

D2D1_BITMAPSOURCE_ORIENTATION GetBitmapSourceOrientation(unsigned short PhotoOrientation)
{
       switch (PhotoOrientation)
       {
       case PHOTO_ORIENTATION_NORMAL:
              return D2D1_BITMAPSOURCE_ORIENTATION_DEFAULT;
       case PHOTO_ORIENTATION_FLIPHORIZONTAL:
              return D2D1_BITMAPSOURCE_ORIENTATION_FLIP_HORIZONTAL;
       case PHOTO_ORIENTATION_ROTATE180:
              return D2D1_BITMAPSOURCE_ORIENTATION_ROTATE_CLOCKWISE180;
       case PHOTO_ORIENTATION_FLIPVERTICAL:
              return D2D1_BITMAPSOURCE_ORIENTATION_ROTATE_CLOCKWISE180_FLIP_HORIZONTAL;
       case PHOTO_ORIENTATION_TRANSPOSE: 
              return D2D1_BITMAPSOURCE_ORIENTATION_ROTATE_CLOCKWISE90_FLIP_HORIZONTAL;
       case PHOTO_ORIENTATION_ROTATE270:
              return D2D1_BITMAPSOURCE_ORIENTATION_ROTATE_CLOCKWISE90;
       case PHOTO_ORIENTATION_TRANSVERSE:
              return D2D1_BITMAPSOURCE_ORIENTATION_ROTATE_CLOCKWISE270_FLIP_HORIZONTAL;
       case PHOTO_ORIENTATION_ROTATE90:
              return D2D1_BITMAPSOURCE_ORIENTATION_ROTATE_CLOCKWISE270;
       default:
              return D2D1_BITMAPSOURCE_ORIENTATION_DEFAULT;
       }
}
```



## <a name="alpha-modes"></a>Modalità Alpha



| Nome                                           | Descrizione                                            |
|------------------------------------------------|--------------------------------------------------------|
| \_Modalità alfa di d2d1 BITMAPSOURCE \_ \_ \_ premoltiplicata | L'output dell'effetto usa l'alfa premoltiplicato.<br/> |
| D2D1 \_ \_ modalità Alpha di BITMAPSOURCE \_ \_ diretta      | L'output dell'effetto usa l'Alpha lineare.<br/>      |



 

## <a name="remarks"></a>Commenti

Per ottimizzare le prestazioni quando si utilizzano WIC e [Direct2D](./direct2d-portal.md) insieme, è necessario utilizzare [**IWICFormatConverter**](/windows/desktop/api/wincodec/nn-wincodec-iwicformatconverter) per eseguire la conversione in un formato pixel appropriato basato sullo scenario dell'app e la precisione nativa dell'immagine.

Nella maggior parte dei casi, la pipeline [Direct2D](./direct2d-portal.md) dell'app s richiede solo 8 bit per canale (bpc) di precisione oppure l'immagine fornisce solo una precisione di 8 bpc ed è quindi necessario convertirla in GUID \_ WICPixelFormat32bppPBGRA. Tuttavia, se si desidera sfruttare la precisione aggiuntiva fornita da un'immagine, ad esempio JPEG-XR o TIFF archiviato con una precisione maggiore di 8 bpc, è necessario utilizzare un formato pixel basato su RGBA. La tabella seguente fornisce altri dettagli.



| Precisione desiderata   | Precisione nativa dell'immagine | Formato pixel consigliato                |
|---------------------|-------------------------------|-----------------------------------------|
| 8 bit per canale  | <= 8 bit per canale      | GUID \_ WICPixelFormat32bppPBGRA          |
| Quanto più alto possibile | <= 8 bit per canale      | GUID \_ WICPixelFormat32bppPBGRA          |
| Quanto più alto possibile | > 8 bit per canale       | Ordine del canale RGBA, alfa premoltiplicato |



 

Poiché molti formati di immagine supportano più livelli di precisione, è necessario utilizzare [**IWICBitmapSource:: GetPixelFormat**](/windows/desktop/wic/-wic-codec-iwicbitmapsource-getpixelformat-proxy) per ottenere il formato pixel nativo dell'immagine, quindi utilizzare [**IWICPixelFormatInfo**](/windows/desktop/api/wincodec/nn-wincodec-iwicpixelformatinfo) per determinare il numero di bit per canale di precisione disponibili per tale formato. Si noti inoltre che non tutti i componenti hardware supportano formati pixel a precisione elevata. In questi casi è possibile che l'app debba eseguire il fallback al dispositivo WARP per supportare la precisione elevata.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato | Windows 8 e aggiornamento della piattaforma per app desktop Windows 7 app \[ \| Windows Store\] |
| Server minimo supportato | Windows 8 e aggiornamento della piattaforma per app desktop Windows 7 app \[ \| Windows Store\] |
| Intestazione                   | d2d1effects. h                                                                      |
| Libreria                  | d2d1. lib, dxguid. lib                                                               |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

