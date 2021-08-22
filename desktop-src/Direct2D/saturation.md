---
title: Effetto saturazione
description: Usare questo effetto per modificare la saturazione di un'immagine.
ms.assetid: 03A374D9-BED4-49ED-B90E-21193909C8AB
keywords:
- effetto di saturazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf5f9a4bff56ed47a0ca182dab855899d98022252c6f20c250aef693451df4c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118665040"
---
# <a name="saturation-effect"></a>Effetto saturazione

Usare questo effetto per modificare la saturazione di un'immagine. L'effetto di saturazione è una specializzazione [dell'effetto matrice di](color-matrix.md) colori.

Il CLSID per questo effetto è CLSID \_ D2D1Saturation.

-   [Immagine di esempio](#example-image)
-   [Proprietà degli effetti](#effect-properties)
-   [Requisiti](#requirements)
-   [Argomenti correlati](#related-topics)

## <a name="example-image"></a>Immagine di esempio

L'esempio seguente mostra le immagini di input e output dell'effetto di saturazione con saturazione pari a 0%.



| Prima                                                      |
|-------------------------------------------------------------|
| ![l'immagine prima dell'effetto.](images/default-before.jpg)  |
| After                                                       |
| ![l'immagine dopo la trasformazione.](images/16-saturation.png) |



 


```C++
ComPtr<ID2D1Effect> saturationEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Saturation, &saturationEffect);

saturationEffect->SetInput(0, bitmap);

saturationEffect->SetValue(D2D1_SATURATION_PROP_SATURATION, 0.0f);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(saturationEffect.Get());
m_d2dContext->EndDraw();
```



L'effetto calcola una matrice di colori in base al valore di saturazione (*s* nell'equazione qui) specificato con la proprietà D2D1 \_ SATURATION \_ PROP \_ SATURATION. L'equazione matrice è illustrata qui.

![formula per il calcolo di una matrice di saturazione.](images/saturation-formula.png)

La matrice creata dipende solo dal valore di saturazione. È possibile usare [l'effetto matrice di](color-matrix.md) colori se è necessaria una matrice specifica.

Questo effetto usa e restituisce immagini alfa premoltilied. L'effetto non funzionerà sulle immagini alfa rette a meno che non siano completamente opache.

## <a name="effect-properties"></a>Proprietà degli effetti



| Nome visualizzato ed enumerazione dell'indice                                  | Tipo e valore predefinito           | Descrizione                                                                                                                                                                                                                      |
|---------------------------------------------------------------------|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Saturazione<br/> SATURAZIONE DELLA PROPRIETÀ \_ \_ DI SATURAZIONE D2D1 \_<br/> | FLOAT<br/> 0,5f<br/> | Saturazione dell'immagine. È possibile impostare la saturazione su un valore compreso tra 0 e 1. Se si imposta su 1, l'immagine di output è completamente satura. Se si imposta su 0, l'immagine di output è monocromatica. Il valore di saturazione è senza unità. |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato | Windows 8 e Platform Update per Windows 7 \[ app desktop \| Windows Store\] |
| Server minimo supportato | Windows 8 e Platform Update per Windows 7 \[ app desktop \| Windows Store\] |
| Intestazione                   | d2d1effects.h                                                                      |
| Libreria                  | d2d1.lib, dxguid.lib                                                               |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

