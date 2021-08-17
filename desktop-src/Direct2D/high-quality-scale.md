---
title: Effetto di scalabilità
description: Usare questo effetto per ridimensionare un'immagine verso l'alto o verso il basso. L'effetto ha sei modalità di ridimensionamento più vicino, lineare, cubico, lineare multi-campione, anisotropo e cubico di alta qualità.
ms.assetid: 99DFA8DB-384B-4F64-90A2-0D3D7E1ACF27
keywords:
- Effetto di ridimensionamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3a28e71dfb552a35bf138c245a82937bd600e61acd8b4a82b42cbc8d9d66a65
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118003663"
---
# <a name="scale-effect"></a>Effetto di scalabilità

Usare questo effetto per ridimensionare un'immagine verso l'alto o verso il basso. L'effetto ha sei modalità di ridimensionamento: vicino più vicino, lineare, cubico, lineare multi-campione, anisotropo e cubo di alta qualità.

Il CLSID per questo effetto è CLSID \_ D2D1Scale.

-   [Immagine di esempio](#example-image)
-   [Proprietà degli effetti](#effect-properties)
    -   [Modalità bordo](#border-modes)
-   [Modalità di interpolazione](#interpolation-modes)
-   [Bitmap di output](#output-bitmap)
-   [Requisiti](#requirements)
-   [Argomenti correlati](#related-topics)

## <a name="example-image"></a>Immagine di esempio

Questo esempio mostra l'effetto di ridimensionamento ingrandito di 2 volte l'input e il ritaglio alle dimensioni originali.



| Prima                                                     |
|------------------------------------------------------------|
| ![l'immagine prima dell'effetto.](images/default-before.jpg) |
| After                                                      |
| ![l'immagine dopo la trasformazione.](images/22-scale.png)     |



 


```C++
ComPtr<ID2D1Effect> scaleEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Scale, &scaleEffect);

scaleEffect->SetInput(0, bitmap);

scaleEffect->SetValue(D2D1_SCALE_PROP_CENTER_POINT, D2D1::Vector2F(256.0f, 192.0f));
scaleEffect->SetValue(D2D1_SCALE_PROP_SCALE, D2D1::Vector2F(2.0f, 2.0f));

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(scaleEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a>Proprietà degli effetti



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Nome visualizzato ed enumerazione dell'indice</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Scalabilità<br/> D2D1_SCALE_PROP_SCALE<br/></td>
<td>Quantità di scala nella direzione X e Y come rapporto tra le dimensioni dell'output e le dimensioni di input. Questa proprietà è D2D1_VECTOR_2Fdefined come: (scala X, scala Y). Gli importi della scala sono FLOAT, senza unità e devono essere positivi o 0.<br/> Il tipo è D2D1_VECTOR_2F.<br/> Il valore predefinito è {1.0f, 1.0f}.<br/></td>
</tr>
<tr class="even">
<td>CenterPoint<br/> D2D1_SCALE_PROP_CENTER_POINT<br/></td>
<td>Punto centrale di ridimensionamento dell'immagine. Questa proprietà è un D2D1_VECTOR_2F definito come: (punto X, punto Y). Le unità sono in DIP.<br/> Usare la proprietà del punto centrale per ridimensionare intorno a un punto diverso dall'angolo superiore sinistro.<br/> Il tipo è D2D1_VECTOR_2F.<br/> Il valore predefinito è {0.0f, 0.0f}.<br/></td>
</tr>
<tr class="odd">
<td>BorderMode<br/> D2D1_SCALE_PROP_BORDER_MODE<br/></td>
<td>Modalità usata per calcolare il bordo dell'immagine, soft o hard. Per <a href="#border-modes">altre informazioni, vedere</a> Modalità bordo. <br/> Il tipo è D2D1_BORDER_MODE.<br/> Il valore predefinito è D2D1_BORDER_MODE_SOFT.<br/></td>
</tr>
<tr class="even">
<td>Nitidezza<br/> D2D1_SCALE_PROP_SHARPNESS<br/></td>
<td>Nella modalità di interpolazione cubica di alta qualità, il livello di nitidezza del filtro di scala come float compreso tra 0 e 1. I valori sono senza unità. È possibile usare la nitidezza per regolare la qualità di un'immagine quando si ridimensiona l'immagine.<br/> Il fattore di nitidezza influisce sulla forma del kernel. Maggiore è il fattore di affilamento, più piccolo è il kernel.<br/>
<blockquote>
[!Note]<br />
Questa proprietà influisce solo sulla modalità di interpolazione cubica di alta qualità.
</blockquote>
<br/> Il tipo è FLOAT.<br/> Il valore predefinito è 0,0f.<br/></td>
</tr>
<tr class="odd">
<td>InterpolazioneMode<br/> D2D1_SCALE_PROP_INTERPOLATION_MODE<br/></td>
<td>Modalità di interpolazione utilizzata dall'effetto per ridimensionare l'immagine. Esistono 6 modalità di scalabilità che variano in qualità e velocità. Per <a href="#interpolation-modes">altre informazioni, vedere Modalità di interpolazione.</a> <br/> Il tipo è D2D1_SCALE_INTERPOLATION_MODE.<br/> Il valore predefinito è D2D1_SCALE_INTERPOLATION_MODE_LINEAR.<br/></td>
</tr>
</tbody>
</table>



 

### <a name="border-modes"></a>Modalità bordo



| Nome                     | Descrizione                                                                                                                                                                                                                                                              |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MODALITÀ BORDO D2D1 \_ \_ \_ SOFT | L'effetto applica il riempimento dell'immagine di input con pixel neri trasparenti per i campioni al di fuori dei limiti di input quando applica il kernel di convoluzione. In questo modo viene creato un bordo soft per l'immagine e nel processo la bitmap di output viene espansa in base alle dimensioni del kernel.<br/> |
| MODALITÀ BORDO D2D1 \_ \_ \_ HARD | L'effetto estende l'immagine di input con una trasformazione del bordo di tipo speculare per gli esempi al di fuori dei limiti di input. Le dimensioni della bitmap di output sono uguali alle dimensioni della bitmap di input.<br/>                                                                       |



 

\`

## <a name="interpolation-modes"></a>Modalità di interpolazione



| Enumerazione                                             | Descrizione                                                                                                                                                                                          |
|---------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ SCALE \_ INTERPOLATION \_ MODE \_ NEAREST \_ NEIGHBOR     | Campiota il singolo punto più vicino e lo usa. Questa modalità usa meno tempo di elaborazione, ma restituisce l'immagine di qualità più bassa.                                                                           |
| MODALITÀ DI INTERPOLAZIONE DELLA SCALA D2D1 \_ \_ \_ \_ LINEARE                | Usa un campione di quattro punti e un'interpolazione lineare. Questa modalità usa più tempo di elaborazione rispetto alla modalità vicina più vicina, ma restituisce un'immagine di qualità superiore.                                           |
| MODALITÀ DI INTERPOLAZIONE DELLA SCALA D2D1 \_ \_ \_ \_ CUBICA                 | Usa un kernel cubico di 16 campioni per l'interpolazione. Questa modalità usa la maggior parte del tempo di elaborazione, ma restituisce un'immagine di qualità superiore.                                                                        |
| D2D1 \_ SCALE \_ INTERPOLATION \_ MODE \_ MULTI \_ SAMPLE \_ LINEAR | Usa 4 campioni lineari all'interno di un singolo pixel per un anti-aliasing del bordo valido. Questa modalità è buona per ridurre di piccole quantità le immagini con pochi pixel.                                              |
| D2D1 \_ SCALE \_ INTERPOLATION \_ MODE \_ ANISOTROP           | Usa il filtro anisotropo per campionare un modello in base alla forma trasformata della bitmap.                                                                                                     |
| D2D1 \_ SCALE \_ INTERPOLATION \_ MODE \_ HIGH \_ QUALITY \_ CUBIC  | Usa un kernel cubico di qualità elevata di dimensioni variabili per eseguire una scalabilità preliminare dell'immagine se è coinvolta la scalabilità in basso nella matrice di trasformazione. Usa quindi la modalità di interpolazione cubica per l'output finale. |



 

> [!Note]  
> Se non si seleziona una modalità, per impostazione predefinita l'effetto è D2D1 \_ SCALE \_ INTERPOLATION \_ MODE \_ LINEAR.

 

> [!Note]  
> La modalità anisotrop genera mipmap durante il ridimensionamento, tuttavia, se si imposta la proprietà **Cached** su true sugli effetti immessi a questo effetto, le mipmap non verranno generate ogni volta per immagini sufficientemente piccole.

 

## <a name="output-bitmap"></a>Bitmap di output

La posizione e le dimensioni della bitmap di output dipendono dal fattore di scala e dal punto centrale specificati.

È possibile calcolare le dimensioni della bitmap di output usando questa equazione:<dl> BitmapSize? (Pixel)=Scala? \* Dimensioni bitmap originali? (DIP) \* (UserDPI/96)  
BitmapSize<sub>y</sub>(Pixel)=Scale<sub>y</sub>Original Bitmap \* Size<sub>y</sub> (DIP) \* (UserDPI/96)  
</dl>

L'effetto arrotonda le frazioni di pixel fino al pixel intero più vicino.

La posizione della bitmap è (0, 0) o il valore della proprietà del punto centrale.

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

 

