---
title: Effetto bordo
description: Utilizzare l'effetto bordo per estendere un'immagine dai bordi.
ms.assetid: D3D569F5-9496-4633-93E2-26665FFC3B37
keywords:
- effetto bordo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49fb43ae8b3e9c4eb449a8231f8b4ffcacf7658b
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/28/2021
ms.locfileid: "104530414"
---
# <a name="border-effect"></a>Effetto bordo

Utilizzare l'effetto bordo per estendere un'immagine dai bordi. È possibile utilizzare questo effetto per ripetere i pixel dai bordi dell'immagine, eseguire il wrapping dei pixel dall'estremità opposta dell'immagine o eseguire il mirroring dei pixel sul bordo della bitmap per estendere l'area bitmap.

Il CLSID per questo effetto è CLSID \_ D2D1Border.

## <a name="example-images"></a>Immagini di esempio

Negli esempi riportati di seguito viene illustrato l'output dell'effetto del bordo utilizzando ogni modalità. Le dimensioni di output sono infinite, ma queste immagini di esempio vengono ritagliate fino al doppio delle dimensioni.

### <a name="mirror"></a>Mirror



| Prima                                                    |
|-----------------------------------------------------------|
| ![Screenshot che mostra l'immagine prima dell'effetto.](images/border-before.jpg) |
| After                                                     |
| ![Screenshot che mostra l'immagine dopo la trasformazione.](images/10-border.png)   |



 

### <a name="clamp"></a>Clamp



| Prima                                                        |
|---------------------------------------------------------------|
| ![Screenshot che mostra l'immagine prima dell'effetto per un morsetto.](images/border-before.jpg)     |
| After                                                         |
| ![Screenshot che mostra l'immagine dopo la trasformazione per un morsetto.](images/10-border-clamp.png) |



 

### <a name="wrap"></a>Wrap



| Prima                                                       |
|--------------------------------------------------------------|
| ![Screenshot che mostra l'immagine prima dell'effetto per un ritorno a capo.](images/border-before.jpg)    |
| After                                                        |
| ![Screenshot che mostra l'immagine dopo la trasformazione per un ritorno a capo.](images/10-border-wrap.png) |



 


```C++
ComPtr<ID2D1Effect> borderEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Border, &borderEffect);

borderEffect->SetInput(0, bitmap);
borderEffect->SetValue(D2D1_BORDER_PROP_EDGE_MODE_X, D2D1_BORDER_EDGE_MODE_MIRROR);
borderEffect->SetValue(D2D1_BORDER_PROP_EDGE_MODE_Y, D2D1_BORDER_EDGE_MODE_MIRROR);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(borderEffect.Get());
m_d2dContext->EndDraw(); 
```



## <a name="effect-properties"></a>Proprietà effetto



| Nome visualizzato e enumerazione dell'indice                                  | Descrizione                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Modalità bordo X<br/> \_ \_ \_ Modalità bordo prop bordo \_ d2d1 \_ X<br/> | Modalità bordo nella direzione X dell'effetto. È possibile impostare questa impostazione su Clamp, wrap o mirror. Per altre informazioni, vedere [modalità Edge](#edge-modes) .<br/> Il tipo è D2D1 \_ Border \_ Edge \_ mode.<br/> Il valore predefinito è D2D1 \_ Border \_ Edge \_ mode \_ Clamp.<br/> |
| Modalità bordo Y<br/> D2D1 \_ bordo della \_ prop in \_ \_ modalità bordo \_ Y<br/> | Modalità bordo nella direzione Y dell'effetto. È possibile impostare questa impostazione su Clamp, wrap o mirror. Per altre informazioni, vedere [modalità Edge](#edge-modes) .<br/> Il tipo è D2D1 \_ Border \_ Edge \_ mode.<br/> Il valore predefinito è D2D1 \_ Border \_ Edge \_ mode \_ Clamp.<br/> |



 

## <a name="edge-modes"></a>Modalità Edge



| Nome visualizzato e enumerazione dell'indice                            | Descrizione                                          |
|---------------------------------------------------------------|------------------------------------------------------|
| Clamp<br/> \_Clamp in \_ \_ modalità bordo d2d1 bordo \_<br/>   | Ripete i pixel dai bordi dell'immagine.      |
| Wrap<br/> \_Wrapping in \_ \_ modalità bordo \_ bordo d2d1<br/>     | USA i pixel dall'estremità opposta dell'immagine. |
| Mirror<br/> \_ \_ \_ Mirroring della modalità \_ bordo bordo d2d1<br/> | Riflette i pixel relativi al bordo dell'immagine.         |



 

## <a name="output-bitmap"></a>Bitmap di output

Le dimensioni della bitmap di output sono infinite per tutti gli input, ad eccezione di un'immagine di input di dimensioni 0. Se l'altezza o la larghezza di un'immagine di input è 0, le dimensioni di output sono pari a 0.

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

 

