---
description: Implementazione di IWICBitmapSourceTransform
ms.assetid: 6a3e682c-55c6-4728-9d14-5eb0290f3dcc
title: Implementazione di IWICBitmapSourceTransform
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0809e1e56fe3c05c8803bb70106c4a24a466eafe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347186"
---
# <a name="implementing-iwicbitmapsourcetransform"></a>Implementazione di IWICBitmapSourceTransform

## <a name="iwicbitmapsourcetransform"></a>IWICBitmapSourceTransform

Sebbene sia facoltativo, è consigliabile che ogni decodificatore implementi questa interfaccia sulla classe di decodifica a livello di frame, in quanto può offrire notevoli vantaggi a livello di prestazioni. Quando un'applicazione richiede un'area specifica di interesse, dimensioni, orientamento o formato pixel, anziché semplicemente decodificare l'intera immagine alla risoluzione completa e quindi applicare le trasformazioni richieste, Windows Imaging Component (WIC) chiama [IUnknown:: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) per questa interfaccia nell'oggetto [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) . Se il decodificatore di frame lo supporta, WIC chiama il metodo o i metodi appropriati per determinare se il decodificatore di frame può eseguire la trasformazione richiesta o determinare il formato pixel o dimensioni più vicino che il decodificatore può fornire a quello richiesto. Se il decodificatore è in grado di eseguire la trasformazione o le trasformazioni richieste, WIC richiama [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) con i parametri appropriati. Se il decodificatore è in grado di eseguire alcune, ma non tutte le trasformazioni richieste, WIC chiede al decodificatore di eseguire quelle che possono e utilizza gli oggetti di trasformazione WIC ([**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler), [**IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper), [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator)e [**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter)) per eseguire le trasformazioni rimanenti che non possono essere eseguite dal decodificatore del frame sul risultato della chiamata **CopyPixels** . Se il decodificatore non supporta [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform), è necessario che WIC usi gli oggetti Transform per eseguire tutte le trasformazioni. È in genere molto più efficiente per il decodificatore eseguire trasformazioni durante il processo di decodifica rispetto a decodificare l'intera immagine e quindi eseguire le trasformazioni. Ciò vale soprattutto per le operazioni, ad esempio il ridimensionamento a una dimensione molto più piccola o le conversioni di formato pixel.


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

[**DoesSupportTransform**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-doessupporttransform) chiede se il decodificatore supporta la rotazione o l'operazione di capovolgimento richiesta. I [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) che possono essere richiesti sono:


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

[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) esegue il lavoro effettivo di decodifica dei bit dell'immagine, ad esempio il metodo [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) sull'interfaccia [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) , ma il metodo [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) su [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) è molto più potente e può migliorare significativamente le prestazioni di elaborazione delle immagini.

Quando vengono richieste più operazioni di trasformazione, il risultato dipende dall'ordine in cui vengono eseguite le operazioni. Per garantire la prevedibilità e la coerenza tra i codec, è importante che tutti i codec eseguano queste operazioni nello stesso ordine. Questo è l'ordine canonico per l'esecuzione di queste operazioni.

1.  Scalabilità
2.  Ritaglia
3.  Ruota

La conversione del formato pixel può essere eseguita in qualsiasi momento, perché non ha alcun effetto sulle altre trasformazioni.

Il primo parametro, *prcSrc*, viene usato per specificare l'area di interesse per il ritaglio dell'immagine. Poiché il ridimensionamento viene eseguito prima del ritaglio per convenzione, se l'immagine deve essere ridimensionata e ritagliata, è necessario determinare l'area di interesse dopo che l'immagine è stata ridimensionata.

Il secondo e il terzo parametro indicano le dimensioni a cui ridimensionare l'immagine.

Il parametro *pguidDstFormat* indica il formato pixel richiesto per l'immagine decodificata. Poiché WIC ha già chiamato [**GetClosestPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-getclosestpixelformat), deve essere un formato pixel che il decodificatore ha indicato che supporta.

Il parametro *dstTransform* indica l'angolo di rotazione richiesto e se capovolgere l'immagine verticalmente, orizzontalmente o entrambi. Anche in questo caso, poiché WIC avrà già chiamato [**DoesSupportTransform**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-doessupporttransform), la trasformazione richiesta dovrebbe essere una delle quali il decodificatore ha già indicato che supporta. Tenere presente che la rotazione deve sempre essere eseguita dopo il ridimensionamento e il ritaglio.

### <a name="getclosestsize"></a>GetClosestSize

[**GetClosestSize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-getclosestsize) accetta due parametri in/out. Il chiamante utilizza i parametri *puiWidth* e *puiHeight* per specificare le dimensioni in base alle quali il chiamante preferisce l'immagine da decodificare. Tuttavia, un decodificatore può decodificare un'immagine solo in una dimensione che è un multiplo delle dimensioni DCT e formati di immagine diversi possono avere dimensioni DCT diverse. Il decodificatore deve determinare, in base alle proprie dimensioni DCT, il più vicino possibile alla dimensione richiesta e impostare *puiWidth* e *puiHeight* su tali dimensioni alla restituzione. Se è richiesta una dimensione maggiore, ma il codec non supporta il ridimensionamento, verrà restituito il valore originale.

### <a name="getclosestpixelformat"></a>GetClosestPixelFormat

[**GetClosestPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-getclosestpixelformat) viene usato per determinare il formato pixel più vicino al formato pixel richiesto che può essere fornito dal decodificatore senza perdita di dati. È sempre preferibile eseguire la conversione in un formato pixel più ampio rispetto a uno più piccolo, anche se aumenterà le dimensioni dell'immagine, perché può sempre essere riconvertito in un formato più restrittivo, se necessario. Tuttavia, una volta persi, i dati non possono essere recuperati.

## <a name="continued-reading"></a>Continua lettura

Per ulteriori informazioni su come creare un codec abilitato per WIC, vedere [implementazione di IWICDevelopRaw](-wic-imp-iwicdevelopraw.md).

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

[Come scrivere un CODEC WIC-Enabled](-wic-howtowriteacodec.md)
</dt> <dt>

[Panoramica del componente imaging Windows](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 
