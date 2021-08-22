---
description: Implementazione di IWICBitmapSourceTransform
ms.assetid: 6a3e682c-55c6-4728-9d14-5eb0290f3dcc
title: Implementazione di IWICBitmapSourceTransform
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79caa17fdb874b9cbee73a9a371c4ba454e72c6eb249a6ca7d626fdd9c86aea0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118711076"
---
# <a name="implementing-iwicbitmapsourcetransform"></a>Implementazione di IWICBitmapSourceTransform

## <a name="iwicbitmapsourcetransform"></a>IWICBitmapSourceTransform

Anche se facoltativo, è consigliabile che ogni decodificatore implementi questa interfaccia nella classe di decodifica a livello di fotogramma, perché può offrire vantaggi significativi in termini di prestazioni. Quando un'applicazione richiede un'area specifica di interesse, dimensioni, orientamento o formato pixel, anziché semplicemente decodificare l'intera immagine alla risoluzione completa e quindi applicare le trasformazioni richieste, Windows Imaging Component (WIC) chiama [IUnknown::QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) per questa interfaccia sull'oggetto [**IWICBitmapFrameDecode.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) Se il decodificatore di frame lo supporta, WIC chiama il metodo o i metodi appropriati per determinare se il decodificatore può eseguire la trasformazione richiesta o determinare la dimensione o il formato pixel più vicino che il decodificatore può fornire a quello richiesto. Se il decodificatore può eseguire la trasformazione o le trasformazioni richieste, WIC richiama [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) con i parametri appropriati. Se il decodificatore può eseguire alcune, ma non tutte le trasformazioni richieste, WIC chiede al decodificatore di eseguirle e usa gli oggetti di trasformazione WIC ([**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler), [**IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper), [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator)e [**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter)) per eseguire le trasformazioni rimanenti che non possono essere eseguite dal decodificatore di frame sul risultato della chiamata **a CopyPixels.** Se il decodificatore non supporta [**IWICBitmapSourceTransform,**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform)WIC deve usare gli oggetti transform per eseguire tutte le trasformazioni. È in genere molto più efficiente per il decodificatore eseguire trasformazioni durante il processo di decodifica rispetto a decodificare l'intera immagine e quindi eseguire le trasformazioni. Ciò vale soprattutto per operazioni quali il ridimensionamento a dimensioni molto più piccole o conversioni in formato pixel.


```C++
interface IWICBitmapSourceTransform : IUnknown
{
   // Required methods
   HRESULT DoesSupportTransform ( WICTransformOptions dstTransform,
              BOOL *pfIsSupported);
   HRESULT CopyPixels ( WICRect *prcSrc, 
      UINT uiWidth, 
      UINT uiHeight,
      WICPixelFormatGUID * pguidDstFormat,
      WICBitmapTransformOptions dstTransform, 
      UINT nStride, 
      UINT cbBufferSize, 
      BYTE *pbBuffer );

   // Optional methods
   HRESULT GetClosestSize ( UINT *puiWidth,
              UINT *puiHeight);
   HRESULT GetClosestPixelFormat ( WICPixelFormatGUID *pguidDstFormat);
}
```



-   [DoesSupportTransform](#doessupporttransform)
-   [CopyPixels](#copypixels)
-   [GetClosestSize](#getclosestsize)
-   [GetClosestPixelFormat](#getclosestpixelformat)

### <a name="doessupporttransform"></a>DoesSupportTransform

[**DoesSupportTransform**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-doessupporttransform) chiede se il decodificatore supporta l'operazione di rotazione o capovolgimento richiesta. Le [**wicBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) che possono essere richieste sono:


```C++
enum WICBitmapTransformOptions
{   
   WICBitmapTransformRotate0,
   WICBitmapTransformRotate90,
   WICBitmapTransformRotate180,
   WICBitmapTransformRotate270,
   WICBitmapTransformFlipHorizontal,
   WICBitmapTransformFlipVertical
}
```



### <a name="copypixels"></a>CopyPixels

[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) esegue il lavoro effettivo di decodifica dei bit dell'immagine, ad esempio il metodo [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) [**nell'interfaccia IWICBitmapSource,**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) ma il metodo [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) in [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) è molto più potente e può migliorare notevolmente le prestazioni di elaborazione delle immagini.

Quando vengono richieste più operazioni di trasformazione, il risultato dipende dall'ordine in cui vengono eseguite le operazioni. Per garantire prevedibilità e coerenza tra i codec, è importante che tutti i codec esercitino queste operazioni nello stesso ordine. Questo è l'ordine canonico per l'esecuzione di queste operazioni.

1.  Scalabilità
2.  Ritaglia
3.  Ruota

La conversione del formato pixel può essere eseguita in qualsiasi momento, perché non ha alcun effetto sulle altre trasformazioni.

Il primo parametro, *prcSrc,* viene usato per specificare l'area di interesse per il ritaglio dell'immagine. Poiché il ridimensionamento viene eseguito prima del ritaglio per convenzione, se l'immagine deve essere ridimensionata e ritagliata, l'area di interesse deve essere determinata dopo che l'immagine è stata ridimensionata.

Il secondo e il terzo parametro indicano le dimensioni in base alle quali ridimensionare l'immagine.

Il *parametro pguidDstFormat* indica il formato pixel richiesto per l'immagine decodificata. Poiché WIC ha già chiamato [**GetClosestPixelFormat,**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-getclosestpixelformat)deve essere un formato pixel che il decodificatore ha indicato di supportare.

Il *parametro dstTransform* indica l'angolo di rotazione richiesto e indica se capovolgere l'immagine verticalmente, orizzontalmente o entrambi. Anche in questo caso, poiché WIC avrà già chiamato [**DoesSupportTransform,**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-doessupporttransform)la trasformazione richiesta deve essere una trasformazione che il decodificatore ha già indicato di supportare. Tenere presente che la rotazione deve essere sempre eseguita dopo il ridimensionamento e il ritaglio.

### <a name="getclosestsize"></a>GetClosestSize

[**GetClosestSize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-getclosestsize) accetta due parametri in/out. Il chiamante usa *i parametri puiWidth* e *puiHeight* per specificare le dimensioni in base alle quali il chiamante preferisce la decodifica dell'immagine. Tuttavia, un decodificatore può decodificare un'immagine solo in dimensioni che sono un multiplo delle dimensioni DCT e formati di immagine diversi possono avere dimensioni DCT diverse. Il decodificatore deve determinare, in base alle proprie dimensioni DCT, quanto più vicino può arrivare alla dimensione richiesta e impostare *puiWidth* e *puiHeight* su tali dimensioni al ritorno. Se vengono richieste dimensioni maggiori, ma il codec non supporta l'upscaling, deve essere restituito l'originale.

### <a name="getclosestpixelformat"></a>GetClosestPixelFormat

[**GetClosestPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-getclosestpixelformat) viene usato per determinare il formato pixel più vicino al formato pixel richiesto che il decodificatore può fornire senza perdita di dati. È sempre preferibile eseguire la conversione in un formato pixel più ampio rispetto a un formato più ristretto, anche se aumenta le dimensioni dell'immagine, perché può sempre essere riconvertito in un formato più restrittivo, se necessario. Tuttavia, dopo che i dati sono stati persi, non possono essere recuperati.

## <a name="continued-reading"></a>Lettura continua

Per altre informazioni su come creare un codec abilitato per WIC, vedere [Implementazione di IWICDevelopRaw.](-wic-imp-iwicdevelopraw.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Riferimento**
</dt> <dt>

[**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform)
</dt> <dt>

[**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Implementazione di IWICMetadataBlockReader](-wic-imp-iwicmetadatablockreader.md)
</dt> <dt>

[Implementazione di IWICDevelopRaw](-wic-imp-iwicdevelopraw.md)
</dt> <dt>

[Come scrivere un codec WIC-Enabled](-wic-howtowriteacodec.md)
</dt> <dt>

[Windows Cenni preliminari sul componente di creazione dell'immagine](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 
