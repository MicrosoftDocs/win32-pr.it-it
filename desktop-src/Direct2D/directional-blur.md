---
title: Effetto sfocatura direzionale
description: L'effetto sfocatura direzionale è simile alla sfocatura gaussiana, ma è possibile inclinare la sfocatura in una particolare direzione.
ms.assetid: 59328FA4-5C27-4A81-AAB2-C5B25B3615C6
keywords:
- sfocatura direzionale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2a43dcaa60f8627473444572ec36a13c3949e9430c9befbb5c064b51d7813bc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119260436"
---
# <a name="directional-blur-effect"></a>Effetto sfocatura direzionale

L'effetto sfocatura direzionale è simile alla sfocatura [gaussiana,](gaussian-blur.md)ma è possibile inclinare la sfocatura in una particolare direzione. È possibile usare questo effetto per fare in modo che un'immagine sia in movimento o per evidenziare un'immagine animata.

Il CLSID per questo effetto è CLSID \_ D2D1DirectionalBlur.

-   [Immagine di esempio](#example-image)
-   [Proprietà degli effetti](#effect-properties)
-   [Modalità di ottimizzazione](#optimization-modes)
-   [Modalità bordo](#border-modes)
-   [Bitmap di output](#output-bitmap)
-   [Requisiti](#requirements)
-   [Argomenti correlati](#related-topics)

## <a name="example-image"></a>Immagine di esempio



| Prima                                                          |
|-----------------------------------------------------------------|
| ![l'immagine prima dell'effetto.](images/default-before.jpg)      |
| After                                                           |
| ![l'immagine dopo la trasformazione.](images/2-directionalblur.png) |



 


```C++
ComPtr<ID2D1Effect> directionalBlurEffect;
m_d2dContext->CreateEffect(CLSID_D2D1DirectionalBlur, &directionalBlurEffect);

directionalBlurEffect->SetInput(0, bitmap);
directionalBlurEffect->SetValue(D2D1_DIRECTIONALBLUR_PROP_STANDARD_DEVIATION, 7.0f);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(directionalBlurEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a>Proprietà degli effetti



| Nome visualizzato ed enumerazione dell'indice                                                       | Descrizione                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| StandardDeviation<br/> DEVIAZIONE STANDARD DELLA PROPRIETÀ \_ DIRECTIONALBLUR D2D1 \_ \_ \_<br/> | Quantità di sfocatura da applicare all'immagine. È possibile calcolare il raggio di sfocatura del kernel moltiplicando la deviazione standard per 3. Le unità della deviazione standard e del raggio di sfocatura sono DIP. Il valore 0 DIP disabilita questo effetto. Il tipo è FLOAT.<br/> Il valore predefinito è 3,0f.<br/>                                                                            |
| Angle<br/> D2D1 \_ DIRECTIONALBLUR \_ PROP \_ ANGLE<br/>                           | Angolo della sfocatura rispetto all'asse x, in senso antiorario. Le unità sono specificate in gradi.<br/> Il kernel di sfocatura viene prima generato usando lo stesso processo dell'effetto [sfocatura gaussiana.](gaussian-blur.md) I valori del kernel vengono quindi trasformati in base all'angolo di sfocatura.<br/> Il tipo è FLOAT.<br/> Il valore predefinito è 0,0f.<br/> |
| Optimization<br/> OTTIMIZZAZIONE DELLE PROPRIETÀ \_ DIRECTIONALBLUR D2D1 \_ \_<br/>             | Modalità di ottimizzazione. Per [altre informazioni, vedere](#optimization-modes) Modalità di ottimizzazione.<br/> Il tipo è D2D1 \_ DIRECTIONALBLUR \_ OPTIMIZATION.<br/> Il valore predefinito è D2D1 \_ DIRECTIONALBLUR \_ OPTIMIZATION \_ BALANCED. <br/>                                                                                                                                                         |
| BorderMode<br/> MODALITÀ BORDO DELLA PROPRIETÀ D2D1 \_ DIRECTIONALBLUR \_ \_ \_<br/>               | Modalità usata per calcolare il bordo dell'immagine, soft o hard. Per [altre informazioni, vedere](#border-modes) Modalità bordo.<br/> Il tipo è D2D1 \_ BORDER \_ MODE.<br/> Il valore predefinito è D2D1 \_ BORDER \_ MODE \_ SOFT.<br/>                                                                                                                                                                 |



 

## <a name="optimization-modes"></a>Modalità di ottimizzazione



| Nome                                          | Descrizione                                                                                                                           |
|-----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ DIRECTIONALBLUR \_ OPTIMIZATION \_ SPEED    | Applica ottimizzazioni interne, ad esempio il pre-ridimensionamento a raggi relativamente piccoli. Usa il filtro lineare.                                  |
| OTTIMIZZAZIONE D2D1 \_ DIRECTIONALBLUR \_ \_ BILANCIATA | Usa le stesse soglie di ottimizzazione della modalità velocità, ma usa il filtro trilineare.                                                    |
| QUALITÀ DI OTTIMIZZAZIONE D2D1 \_ DIRECTIONALBLUR \_ \_  | Usa solo ottimizzazioni interne con raggi di sfocatura di grandi dimensioni, in cui è meno probabile che le approssimazioni siano visibili. Usa il filtro trilineare. |



 

## <a name="border-modes"></a>Modalità bordo



| Nome                     | Descrizione                                                                                                                                                                                                              |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MODALITÀ BORDO D2D1 \_ \_ \_ SOFT | L'effetto consente di riempire l'immagine con pixel neri trasparenti quando applica il kernel sfocatura, determinando un bordo sfuocato. <br/>                                                                                             |
| MODALITÀ BORDO D2D1 \_ \_ \_ HARD | L'effetto stringe l'output alle dimensioni dell'immagine di input. Quando l'effetto applica il kernel di sfocatura, estende l'immagine di input con una trasformazione del bordo di tipo speculare per i campioni al di fuori dei limiti di input.<br/> |



 

## <a name="output-bitmap"></a>Bitmap di output

Le dimensioni della bitmap di output aumentano in base alla deviazione standard, all'angolo dell'effetto e alla modalità bordo. Se la modalità bordo è impostata su D2D1 BORDER MODE SOFT, le dimensioni della bitmap di output aumentano delle dimensioni del \_ kernel di sfocatura, \_ \_ rappresentate in pixel. Queste equazioni possono essere usate per calcolare le dimensioni della bitmap di output.



| Requisito | Valore |
|------------------------|-------------------------------------------------------------------|
| Aumento della bitmap di output X | StandardDeviation (DIP) \* 6 \* ((User DPI) /96) \* cos(Angle)) |
| Aumento della bitmap di output Y | StandardDeviation (DIP) \* 6 \* ((User DPI) /96) \* sin(Angle)) |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato | Windows 8 e aggiornamento della piattaforma per Windows 7 \[ app desktop \| Windows Store\] |
| Server minimo supportato | Windows 8 e aggiornamento della piattaforma per Windows 7 \[ app desktop \| Windows Store\] |
| Intestazione                   | d2d1effects.h                                                                      |
| Libreria                  | d2d1.lib, dxguid.lib                                                               |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

