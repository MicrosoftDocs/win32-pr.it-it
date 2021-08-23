---
title: Effetto origine bitmap
description: Usare l'effetto origine bitmap per generare un id2D1Image da un oggetto IWICBitmapSource da usare come input in un grafico degli effetti.
ms.assetid: 86646111-208A-4E6D-A28C-7B23A1742D24
keywords:
- Effetto origine bitmap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19889372c7ebd4268f1b6fd8b77c360f290cc416631e9fb5e1cd3a0b0320844c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119833322"
---
# <a name="bitmap-source-effect"></a>Effetto origine bitmap

Usare l'effetto origine bitmap per generare un [**id2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) da [**un oggetto IWICBitmapSource**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource) da usare come input in un grafico degli effetti. Questo effetto esegue il ridimensionamento e la rotazione sulla CPU. Può anche generare facoltativamente un mipmap di memoria di sistema, che può essere un'ottimizzazione delle prestazioni per ridimensionare attivamente immagini molto grandi a varie risoluzioni ridotte.

> [!Note]  
> L'effetto di origine bitmap accetta l'input come proprietà, non come input di immagine. È necessario usare il [**metodo SetValue,**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32)) non il [**metodo SetInput.**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1effect-setinput) La *proprietà WicBitmapSource* consente di specificare i dati di input dell'immagine.

 

Il CLSID per questo effetto è CLSID \_ D2D1BitmapSource.

-   [Proprietà degli effetti](#effect-properties)
-   [Modalità di interpolazione](#interpolation-modes)
-   [Orientamento](#orientation)
-   [Modalità alfa](#alpha-modes)
-   [Osservazioni:](#remarks)
-   [Requisiti](#requirements)
-   [Argomenti correlati](#related-topics)

## <a name="effect-properties"></a>Proprietà degli effetti



| Nome visualizzato ed enumerazione dell'indice                                                          | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WicBitmapSource<br/> ORIGINE BITMAP D2D1 \_ BITMAPSOURCE \_ PROP \_ WIC \_ \_<br/>         | Oggetto [IWICBitmapSource](/windows/desktop/wic/-wic-imp-iwicbitmapsource) contenente i dati dell'immagine da caricare.<br/> Il tipo è [IWICBitmapSource.](/windows/desktop/wic/-wic-imp-iwicbitmapsource)<br/> Il valore predefinito è NULL.<br/>                                                                                                                                                                                                                   |
| Scalabilità<br/> SCALA DELLE PROPRIETÀ \_ BITMAPSOURCE D2D1 \_ \_<br/>                                 | Quantità di scala nella direzione X e Y. L'effetto moltiplica la larghezza per il valore X e l'altezza per il valore Y. Questa proprietà è un vettore D2D1 \_ \_ 2F definito come: (scala X, scala Y). Gli importi della scala sono FLOAT, senza unità e devono essere positivi o 0.<br/> Il tipo è D2D1 \_ VECTOR \_ 2F.<br/> Il valore predefinito è {1.0f, 1.0f}.<br/>                                                                           |
| InterpolazioneMode.<br/> MODALITÀ DI \_ \_ INTERPOLAZIONE DELLA PROPRIETÀ BITMAPSOURCE D2D1 \_ \_<br/>      | Modalità di interpolazione usata per ridimensionare l'immagine. Per [altre informazioni, vedere Modalità di interpolazione.](#interpolation-modes)<br/> Se la modalità disabilita il mipmap, BitmapSouce memorizza nella cache l'immagine alla risoluzione determinata dalle proprietà Scale e EnableDPICorrection.<br/> Il tipo è D2D1 \_ BITMAPSOURCE \_ INTERPOLATION \_ MODE.<br/> Il valore predefinito è D2D1 \_ BITMAPSOURCE \_ INTERPOLATION \_ MODE \_ LINEAR.<br/> |
| EnableDPICorrection<br/> D2D1 \_ BITMAPSOURCE \_ PROP \_ ENABLE \_ DPI \_ CORRECTION<br/> | Se si imposta questa proprietà su TRUE, l'effetto ridimensiona l'immagine di input per convertire il valore DPI segnalato da [**IWICBitmapSource**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource) nel valore DPI del contesto di dispositivo. L'effetto usa la modalità di interpolazione impostata con la proprietà InterpolationMode. Se si imposta questa opzione su FALSE, l'effetto usa un valore DPI di 96.0 per l'immagine di output.<br/> Il tipo è BOOL.<br/> Il valore predefinito è FALSE.<br/>   |
| AlphaMode<br/> MODALITÀ ALFA DELLA \_ \_ PROPRIETÀ BITMAPSOURCE \_ \_ D2D1<br/>                       | Modalità alfa dell'output. Può essere premoltimulliato o diritto. Per [altre informazioni, vedere](#alpha-modes) Modalità alfa.<br/> Il tipo è D2D1 \_ BITMAPSOURCE \_ ALPHA \_ MODE.<br/> Il valore predefinito è D2D1 \_ BITMAPSOURCE \_ ALPHA MODE \_ \_ PREMULTIPLIED.<br/>                                                                                                                                                              |
| Orientamento<br/> ORIENTAMENTO DELLA PROPRIETÀ \_ BITMAPSOURCE D2D1 \_ \_<br/>                     | Operazione di capovolgimento e/o rotazione da eseguire sull'immagine. Per [altre informazioni,](#orientation) vedere Orientamento.<br/> Il tipo è D2D1 \_ BITMAPSOURCE \_ ORIENTATION.<br/> Il valore predefinito è D2D1 \_ BITMAPSOURCE \_ ORIENTATION \_ DEFAULT.<br/>                                                                                                                                                                                 |



 

## <a name="interpolation-modes"></a>Modalità di interpolazione

L'effetto interpola usando questa modalità quando ridimensiona un'immagine o quando corregge il valore DPI. Le modalità di interpolazione utilizzate da questo effetto vengono calcolate dalla CPU, non dalla GPU.



| Nome                                                       | Descrizione                                                                                                                                                                                                                          |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ BITMAPSOURCE \_ INTERPOLATION \_ MODE \_ NEAREST \_ NEIGHBOR | Campiota il singolo punto più vicino e lo usa. Non genera un mipmap.                                                                                                                                                           |
| MODALITÀ DI INTERPOLAZIONE D2D1 \_ BITMAPSOURCE \_ \_ \_ LINEARE            | Usa un campione di quattro punti e un'interpolazione lineare. Non genera un mipmap.                                                                                                                                                        |
| MODALITÀ DI INTERPOLAZIONE D2D1 \_ BITMAPSOURCE \_ \_ \_ CUBIC             | Usa un kernel cubo di 16 campioni per l'interpolazione. Non genera un mipmap.                                                                                                                                                          |
| MODALITÀ DI \_ \_ INTERPOLAZIONE \_ D2D1 BITMAPSOURCE \_              | Usa l'interpolazione fant wic, la stessa [**dell'interfaccia IWICBitmapScaler.**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapscaler) Non genera un mipmap.                                                                                       |
| D2D1 \_ BITMAPSOURCE \_ INTERPOLATION \_ MODE \_ MIPMAP \_ LINEAR    | Genera la catena mipmap nella memoria di sistema usando l'interpolazione bilineare. Per ogni mipmap l'effetto viene ridimensionato al multiplo più vicino di 0,5 usando l'interpolazione bilineare e quindi ridimensiona la quantità rimanente usando l'interpolazione lineare. |



 

## <a name="orientation"></a>Orientamento

La proprietà Orientation può essere usata per applicare un flag di orientamento EXIF incorporato all'interno di un'immagine.



| Nome                                                                    | Descrizione                                                        |
|-------------------------------------------------------------------------|--------------------------------------------------------------------|
| D2D1 \_ BITMAPSOURCE \_ ORIENTATION \_ DEFAULT                                | Valore predefinito. L'effetto non modifica l'orientamento dell'input.   |
| D2D1 \_ BITMAPSOURCE \_ ORIENTATION \_ FLIP \_ HORIZONTAL                       | Capovolge orizzontalmente l'immagine.                                      |
| D2D1 \_ BITMAPSOURCE \_ ORIENTATION \_ ROTATE \_ CLOCKWISE180                   | Ruota l'immagine di 180 gradi in senso orario.                           |
| D2D1 \_ BITMAPSOURCE \_ ORIENTATION \_ ROTATE \_ CLOCKWISE180 \_ FLIP \_ HORIZONTAL | Ruota l'immagine di 180 gradi in senso orario e la capovolge orizzontalmente. |
| D2D1 \_ BITMAPSOURCE \_ ORIENTATION \_ ROTATE \_ CLOCKWISE270 \_ FLIP \_ HORIZONTAL | Ruota l'immagine di 270 gradi in senso orario e la capovolge orizzontalmente. |
| D2D1 \_ BITMAPSOURCE \_ ORIENTATION \_ ROTATE \_ CLOCKWISE90                    | Ruota l'immagine di 90 gradi in senso orario.                            |
| D2D1 \_ BITMAPSOURCE \_ ORIENTATION \_ ROTATE \_ CLOCKWISE90 \_ FLIP \_ HORIZONTAL  | Ruota l'immagine di 90 gradi in senso orario e la capovolge orizzontalmente.  |
| D2D1 \_ BITMAP ORIENTATION ROTATE \_ \_ \_ CLOCKWISE270                   | Ruota l'immagine di 270 gradi in senso orario.                           |



 

Questo frammento di codice illustra come eseguire la conversione da valori di orientamento EXIF (definiti in propkey.h) a valori \_ DI ORIENTAMENTO BITMAPSOURCE D2D1. \_


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



## <a name="alpha-modes"></a>Modalità alfa



| Nome                                           | Descrizione                                            |
|------------------------------------------------|--------------------------------------------------------|
| D2D1 \_ BITMAPSOURCE \_ ALPHA \_ MODE \_ PREMULTIPLIED | L'output dell'effetto usa valori alfa premoltiliati.<br/> |
| D2D1 \_ BITMAPSOURCE \_ ALPHA \_ MODE \_ STRAIGHT      | L'output dell'effetto usa alfa rette.<br/>      |



 

## <a name="remarks"></a>Commenti

Per ottimizzare le prestazioni quando si usano insieme WIC e [Direct2D,](./direct2d-portal.md) è necessario usare [**IWICFormatConverter**](/windows/desktop/api/wincodec/nn-wincodec-iwicformatconverter) per eseguire la conversione in un formato pixel appropriato in base allo scenario dell'app e alla precisione nativa dell'immagine.

Nella maggior parte dei casi, la pipeline [Direct2D](./direct2d-portal.md) dell'app richiede solo 8 bit per canale (bpc) di precisione oppure l'immagine fornisce solo 8 bpc di precisione ed è quindi consigliabile eseguire la conversione al GUID \_ WICPixelFormat32bppPBGRA. Tuttavia, se si vuole sfruttare la precisione aggiuntiva fornita da un'immagine (ad esempio, un JPEG-XR o TIFF archiviato con una precisione maggiore di 8 bpc), è consigliabile usare un formato pixel basato su RGBA. La tabella seguente fornisce altri dettagli.



| Precisione desiderata   | Precisione nativa dell'immagine | Formato pixel consigliato                |
|---------------------|-------------------------------|-----------------------------------------|
| 8 bit per canale  | <= 8 bit per canale      | GUID \_ WICPixelFormat32bppPBGRA          |
| Il più alto possibile | <= 8 bit per canale      | GUID \_ WICPixelFormat32bppPBGRA          |
| Il più alto possibile | > 8 bit per canale       | RGBA channel order, premultiplied alpha |



 

Poiché molti formati di immagine supportano più livelli di precisione, è consigliabile usare [**IWICBitmapSource::GetPixelFormat**](/windows/desktop/wic/-wic-codec-iwicbitmapsource-getpixelformat-proxy) per ottenere il formato pixel nativo dell'immagine e quindi usare [**IWICPixelFormatInfo**](/windows/desktop/api/wincodec/nn-wincodec-iwicpixelformatinfo) per determinare quanti bit per canale di precisione sono disponibili per tale formato. Si noti inoltre che non tutti i componenti hardware supportano formati pixel ad alta precisione. In questi casi l'app potrebbe dover eseguire il fall back al dispositivo WARP per supportare la precisione elevata.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato | Windows 8 e l'aggiornamento della piattaforma per Windows 7 \[ app desktop \| Windows Store\] |
| Server minimo supportato | Windows 8 e l'aggiornamento della piattaforma per Windows 7 \[ app desktop \| Windows Store\] |
| Intestazione                   | d2d1effects.h                                                                      |
| Libreria                  | d2d1.lib, dxguid.lib                                                               |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

