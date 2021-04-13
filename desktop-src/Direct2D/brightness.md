---
title: Effetto luminosità
description: Usare l'effetto di luminosità per controllare la luminosità dell'immagine.
ms.assetid: 5088D4D4-DFC8-45D3-B1C3-D576742D931C
keywords:
- effetto luminosità
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88dd9797aa125e7099ba4a706bac730a30715f6c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104552095"
---
# <a name="brightness-effect"></a>Effetto luminosità

Usare l'effetto di luminosità per controllare la luminosità dell'immagine.

Il CLSID per questo effetto è CLSID \_ D2D1Brightness.

-   [Immagine di esempio](#example-image)
-   [Proprietà effetto](#effect-properties)
-   [Bitmap di output](#output-bitmap)
-   [Requisiti](#requirements)
-   [Argomenti correlati](#related-topics)

## <a name="example-image"></a>Immagine di esempio



| Prima                                                      |
|-------------------------------------------------------------|
| ![immagine prima dell'effetto.](images/default-before.jpg)  |
| After                                                       |
| ![immagine dopo la trasformazione.](images/34-brightness.png) |



 


```C++
ComPtr<ID2D1Effect> brightnessEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Brightness, &brightnessEffect);

brightnessEffect->SetValue(D2D1_BRIGHTNESS_PROP_BLACK_POINT, D2D1::Vector2F(0.0f, 0.2f));

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(brightnessEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a>Proprietà effetto



| Nome visualizzato proprietà                                                 | Tipo e valore predefinito                              | Descrizione                                                                                                                                                                                                                                                                 |
|-----------------------------------------------------------------------|-----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WhitePoint<br/> \_ \_ \_ Punto bianco prop luminosità \_ d2d1<br/> | D2D1 \_ vector \_ 2F<br/> {1.0 f, 1.0 f}<br/> | Parte superiore della curva di trasferimento della luminosità. Il punto bianco regola l'aspetto delle parti più luminose dell'immagine. Questa proprietà è per il valore x e il valore y, in questo ordine. Ognuno dei valori di questa proprietà è compreso tra 0 e 1 inclusi. |
| BlackPoint<br/> \_ \_ Punto nero della prop d2d1 brightness \_ \_<br/> | D2D1 \_ vector \_ 2F<br/> {0,0 f, 0,0 f}<br/> | Parte inferiore della curva di trasferimento della luminosità. Il punto nero regola l'aspetto delle parti più scure dell'immagine. Questa proprietà è per il valore x e il valore y, in questo ordine. Ognuno dei valori di questa proprietà è compreso tra 0 e 1 inclusi.   |



 

Questo effetto utilizza i punti bianco e nero specificati per generare una funzione di trasferimento utilizzata per modificare la bitmap. L'equazione successiva descrive la funzione di trasferimento. Le intensità di input sono definite tra 0 e 1.

![algoritmo di luminosità](images/brightness-formula1.png)

L'algoritmo Effect implementa un'equazione che crea la funzione di trasferimento. Questa funzione viene usata per modificare i pixel dell'immagine. I valori x e y del punto nero e del punto bianco sono le coordinate in due dimensioni connesse alla trasformazione. Ogni parte dell'equazione di output finale:

1.  Converte i dati dell'immagine dallo spazio lineare allo spazio non lineare utilizzando questa equazione:![funzione helper 1](images/brightness-formula2.png)

2.  Regola l'immagine in base a questi valori:
    -   *input* è il valore di intensità pixel dell'immagine di input compreso tra 0 e 1.

    -   *PT bianco. (x, y)* posizione della curva di trasformazione per le intensità dei pixel più brillanti.

    -   *Black pt. (x, y)* è la posizione della curva di trasformazione per le intensità dei pixel dimmer.

3.  Converte nuovamente i dati dell'immagine nello spazio lineare usando questa equazione: ![funzione helper 2](images/brightness-formula3.png)

L'equazione di output finale e le parti del componente sono illustrate di seguito.

![calcoli completi per la regolazione della luminosità](images/brightness-formula4.png)

## <a name="output-bitmap"></a>Bitmap di output

La dimensione bitmap di output corrisponde alla dimensione bitmap di input.

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

 

