---
title: Effetto sfocatura direzionale
description: L'effetto di sfocatura direzionale è simile alla sfocatura gaussiana, ad eccezione del fatto che è possibile inclinare la sfocatura in una direzione specifica.
ms.assetid: 59328FA4-5C27-4A81-AAB2-C5B25B3615C6
keywords:
- sfocatura direzionale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0e1c098d17929563cf69f4e61416fa0d93a88dd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739855"
---
# <a name="directional-blur-effect"></a>Effetto sfocatura direzionale

L'effetto di sfocatura direzionale è simile alla [sfocatura gaussiana](gaussian-blur.md), ad eccezione del fatto che è possibile inclinare la sfocatura in una direzione specifica. È possibile usare questo effetto per creare un'immagine come se fosse in movimento o per enfatizzare un'immagine animata.

Il CLSID per questo effetto è CLSID \_ D2D1DirectionalBlur.

-   [Immagine di esempio](#example-image)
-   [Proprietà effetto](#effect-properties)
-   [Modalità di ottimizzazione](#optimization-modes)
-   [Modalità bordo](#border-modes)
-   [Bitmap di output](#output-bitmap)
-   [Requisiti](#requirements)
-   [Argomenti correlati](#related-topics)

## <a name="example-image"></a>Immagine di esempio



| Prima                                                          |
|-----------------------------------------------------------------|
| ![immagine prima dell'effetto.](images/default-before.jpg)      |
| After                                                           |
| ![immagine dopo la trasformazione.](images/2-directionalblur.png) |



 


```C++
ComPtr<ID2D1Effect> directionalBlurEffect;
m_d2dContext->CreateEffect(CLSID_D2D1DirectionalBlur, &directionalBlurEffect);

directionalBlurEffect->SetInput(0, bitmap);
directionalBlurEffect->SetValue(D2D1_DIRECTIONALBLUR_PROP_STANDARD_DEVIATION, 7.0f);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(directionalBlurEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a>Proprietà effetto



| Nome visualizzato e enumerazione dell'indice                                                       | Descrizione                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| StandardDeviation<br/> D2D1 \_ DIRECTIONALBLUR \_ prop \_ \_ deviazione standard<br/> | Quantità di sfocatura da applicare all'immagine. È possibile calcolare il raggio di sfocatura del kernel moltiplicando la deviazione standard di 3. Le unità della deviazione standard e del raggio di sfocatura sono dip. Il valore 0 DIP Disabilita questo effetto. Il tipo è FLOAT.<br/> Il valore predefinito è 3.0 f.<br/>                                                                            |
| Angle<br/> \_Angolo della \_ prop \_ DIRECTIONALBLUR d2d1<br/>                           | Angolo della sfocatura rispetto all'asse x, in senso antiorario. Le unità vengono specificate in gradi.<br/> Il kernel di sfocatura viene innanzitutto generato utilizzando lo stesso processo dell'effetto [sfocatura gaussiana](gaussian-blur.md) . I valori del kernel vengono quindi trasformati in base all'angolo di sfocatura.<br/> Il tipo è FLOAT.<br/> Il valore predefinito è 0,0 f.<br/> |
| Optimization<br/> \_Ottimizzazione della \_ prop \_ DIRECTIONALBLUR d2d1<br/>             | Modalità di ottimizzazione. Per altre informazioni, vedere [modalità di ottimizzazione](#optimization-modes) .<br/> Il tipo è D2D1 \_ DIRECTIONALBLUR \_ Optimization.<br/> Il valore predefinito è D2D1 \_ DIRECTIONALBLUR \_ Optimization \_ Balanced. <br/>                                                                                                                                                         |
| BorderMode<br/> \_ \_ \_ Modalità bordo prop DIRECTIONALBLUR \_ d2d1<br/>               | Modalità utilizzata per calcolare il bordo dell'immagine, soft o hard. Per altre informazioni, vedere [Border modes](#border-modes) .<br/> Il tipo è D2D1 \_ Border \_ mode.<br/> Il valore predefinito è D2D1 \_ Border \_ mode \_ .<br/>                                                                                                                                                                 |



 

## <a name="optimization-modes"></a>Modalità di ottimizzazione



| Nome                                          | Descrizione                                                                                                                           |
|-----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| \_Velocità di \_ ottimizzazione \_ DIRECTIONALBLUR di d2d1    | Applica le ottimizzazioni interne, ad esempio la pre-scalabilità a raggi relativamente piccoli. Usa il filtro lineare.                                  |
| \_Ottimizzazione d2d1 \_ DIRECTIONALBLUR \_ | Usa le stesse soglie di ottimizzazione della modalità velocità, ma usa il filtro trilineare.                                                    |
| \_ \_ Qualità ottimizzazione DIRECTIONALBLUR \_ d2d1  | USA solo le ottimizzazioni interne con raggi di sfocatura grandi, in cui è meno probabile che le approssimazioni siano visibili. Usa il filtro trilineare. |



 

## <a name="border-modes"></a>Modalità bordo



| Nome                     | Descrizione                                                                                                                                                                                                              |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_Modalità bordo \_ d2d1 \_ Soft | L'effetto Ritaglia l'immagine con i pixel neri trasparenti quando applica il kernel di sfocatura, ottenendo un bordo flessibile. <br/>                                                                                             |
| \_Modalità bordo \_ d2d1 \_ | L'effetto fissa l'output alla dimensione dell'immagine di input. Quando l'effetto applica il kernel di sfocatura, estende l'immagine di input con una trasformazione del bordo di tipo mirror per i campioni all'esterno dei limiti di input.<br/> |



 

## <a name="output-bitmap"></a>Bitmap di output

La dimensione della bitmap di output aumenta in base alla deviazione standard, all'angolo dell'effetto e alla modalità del bordo. Se la modalità bordo è impostata su D2D1 \_ Border \_ mode \_ , le dimensioni della bitmap di output aumentano in base alle dimensioni del kernel di sfocatura, rappresentate in pixel. Queste equazioni possono essere usate per calcolare le dimensioni della bitmap di output.



| Requisito | Valore |
|------------------------|-------------------------------------------------------------------|
| Aumento dimensioni bitmap di output X | StandardDeviation (DIP) \* 6 \* (((dpi utente)/96) \* cos (angolo)) |
| Crescita bitmap di output Y | StandardDeviation (DIP) \* 6 \* (((dpi utente)/96) \* sin (angolo)) |



 

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

 

