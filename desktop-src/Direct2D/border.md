---
title: Effetto bordo
description: Usare l'effetto bordo per estendere un'immagine dai bordi.
ms.assetid: D3D569F5-9496-4633-93E2-26665FFC3B37
keywords:
- effetto bordo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ce125a96730ee59f63b18cfd1a08abd2432af6f3fdc6b5f06cfc2e9272a7a3c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119928997"
---
# <a name="border-effect"></a>Effetto bordo

Usare l'effetto bordo per estendere un'immagine dai bordi. È possibile usare questo effetto per ripetere i pixel dai bordi dell'immagine, eseguire il wrapping dei pixel dall'estremità opposta dell'immagine o riflettere i pixel sul bordo della bitmap per estendere l'area bitmap.

Il CLSID per questo effetto è CLSID \_ D2D1Border.

## <a name="example-images"></a>Immagini di esempio

Gli esempi qui illustrano l'output dell'effetto bordo usando ogni modalità. Le dimensioni di output sono infinite, ma queste immagini di esempio vengono ritagliate fino al doppio delle dimensioni.

### <a name="mirror"></a>Mirror



| Prima                                                    |
|-----------------------------------------------------------|
| ![Screenshot che mostra l'immagine prima dell'effetto.](images/border-before.jpg) |
| After                                                     |
| ![Screenshot che mostra l'immagine dopo la trasformazione.](images/10-border.png)   |



 

### <a name="clamp"></a>Clamp



| Prima                                                        |
|---------------------------------------------------------------|
| ![Screenshot che mostra l'immagine prima dell'effetto per una morsa.](images/border-before.jpg)     |
| After                                                         |
| ![Screenshot che mostra l'immagine dopo la trasformazione per una morsa.](images/10-border-clamp.png) |



 

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



## <a name="effect-properties"></a>Proprietà degli effetti



| Nome visualizzato ed enumerazione dell'indice                                  | Descrizione                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Modalità Edge X<br/> D2D1 \_ BORDER \_ PROP \_ EDGE \_ MODE \_ X<br/> | Modalità bordo nella direzione X per l'effetto. È possibile impostare questa opzione su clamp, wrap o mirror. Per [altre informazioni, vedere Modalità](#edge-modes) edge.<br/> Il tipo è D2D1 \_ BORDER \_ EDGE \_ MODE.<br/> Il valore predefinito è D2D1 \_ BORDER \_ EDGE MODE \_ \_ CLAMP.<br/> |
| Modalità Edge Y<br/> D2D1 \_ BORDER \_ PROP \_ EDGE \_ MODE \_ Y<br/> | Modalità bordo nella direzione Y per l'effetto. È possibile impostare questa opzione su clamp, wrap o mirror. Per [altre informazioni, vedere Modalità](#edge-modes) edge.<br/> Il tipo è D2D1 \_ BORDER \_ EDGE \_ MODE.<br/> Il valore predefinito è D2D1 \_ BORDER \_ EDGE MODE \_ \_ CLAMP.<br/> |



 

## <a name="edge-modes"></a>Modalità perimetrali



| Nome visualizzato ed enumerazione dell'indice                            | Descrizione                                          |
|---------------------------------------------------------------|------------------------------------------------------|
| Clamp<br/> D2D1 \_ BORDER \_ EDGE \_ MODE \_ CLAMP<br/>   | Ripete i pixel dai bordi dell'immagine.      |
| Wrap<br/> RITORNO A CAPO DELLA MODALITÀ BORDO D2D1 \_ \_ \_ \_<br/>     | Usa i pixel dal bordo finale opposto dell'immagine. |
| Mirror<br/> D2D1 \_ BORDER \_ EDGE \_ MODE \_ MIRROR<br/> | Riflette i pixel sul bordo dell'immagine.         |



 

## <a name="output-bitmap"></a>Bitmap di output

Le dimensioni della bitmap di output sono infinite per tutti gli input, ad eccezione di un'immagine di input con dimensioni 0. Se l'altezza o la larghezza di un'immagine di input è 0, le dimensioni di output sono 0.

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

 

