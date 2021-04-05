---
title: Effetto saturazione
description: Utilizzare questo effetto per modificare la saturazione di un'immagine.
ms.assetid: 03A374D9-BED4-49ED-B90E-21193909C8AB
keywords:
- effetto saturazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d6912e64c9297a3554b4785128e1282a3974d36
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048238"
---
# <a name="saturation-effect"></a>Effetto saturazione

Utilizzare questo effetto per modificare la saturazione di un'immagine. L'effetto di saturazione è una specializzazione dell'effetto della [matrice di colori](color-matrix.md) .

Il CLSID per questo effetto è CLSID \_ D2D1Saturation.

-   [Immagine di esempio](#example-image)
-   [Proprietà effetto](#effect-properties)
-   [Requisiti](#requirements)
-   [Argomenti correlati](#related-topics)

## <a name="example-image"></a>Immagine di esempio

Nell'esempio riportato di seguito vengono illustrate le immagini di input e di output dell'effetto di saturazione con una saturazione pari allo 0%.



| Prima                                                      |
|-------------------------------------------------------------|
| ![immagine prima dell'effetto.](images/default-before.jpg)  |
| After                                                       |
| ![immagine dopo la trasformazione.](images/16-saturation.png) |



 


```C++
ComPtr<ID2D1Effect> saturationEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Saturation, &saturationEffect);

saturationEffect->SetInput(0, bitmap);

saturationEffect->SetValue(D2D1_SATURATION_PROP_SATURATION, 0.0f);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(saturationEffect.Get());
m_d2dContext->EndDraw();
```



L'effetto calcola una matrice di colori in base al valore di saturazione (*s* nell'equazione qui) specificata con la \_ \_ \_ Proprietà saturazione d2d1 saturazione. L'equazione della matrice è illustrata di seguito.

![formula per il calcolo di una matrice di saturazione.](images/saturation-formula.png)

La matrice creata dipende solo dal valore di saturazione. Se è necessaria una matrice specifica, è possibile usare l'effetto della [matrice di colori](color-matrix.md) .

Questo effetto utilizza e restituisce immagini alfa premoltiplicate. L'effetto non funzionerà su immagini Alpha dritte a meno che non siano completamente opache.

## <a name="effect-properties"></a>Proprietà effetto



| Nome visualizzato e enumerazione dell'indice                                  | Tipo e valore predefinito           | Descrizione                                                                                                                                                                                                                      |
|---------------------------------------------------------------------|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Saturazione<br/> \_Saturazione d2d1 saturazione \_ \_<br/> | FLOAT<br/> 0,5 f<br/> | Saturazione dell'immagine. È possibile impostare la saturazione su un valore compreso tra 0 e 1. Se lo si imposta su 1, l'immagine di output è completamente satura. Se lo si imposta su 0, l'immagine di output è monocromatica. Il valore di saturazione è di unità. |



 

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

 

