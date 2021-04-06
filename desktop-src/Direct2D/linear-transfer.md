---
title: Effetto trasferimento lineare
description: Usare l'effetto di trasferimento lineare per eseguire il mapping delle intensità dei colori di un'immagine usando una funzione lineare creata da un elenco di valori forniti per ogni canale.
ms.assetid: 22DC496E-2958-4726-A74D-B3DE934F507C
keywords:
- effetto trasferimento lineare
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfedbb79f057ee871ce23cc086034afc3e6cdda0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743946"
---
# <a name="linear-transfer-effect"></a>Effetto trasferimento lineare

Usare l'effetto di trasferimento lineare per eseguire il mapping delle intensità dei colori di un'immagine usando una funzione lineare creata da un elenco di valori forniti per ogni canale.

Il CLSID per questo effetto è CLSID \_ D2D1LinearTransfer.

-   [Immagine di esempio](#example-image)
-   [Proprietà effetto](#effect-properties)
-   [Requisiti](#requirements)
-   [Argomenti correlati](#related-topics)

## <a name="example-image"></a>Immagine di esempio



| Prima                                                          |
|-----------------------------------------------------------------|
| ![immagine prima dell'effetto.](images/default-before.jpg)      |
| After                                                           |
| ![immagine dopo la trasformazione.](images/13-lineartransfer.png) |



 


```C++
ComPtr<ID2D1Effect> linearTransferEffect;
m_d2dContext->CreateEffect(CLSID_D2D1LinearTransfer, &linearTransferEffect);

linearTransferEffect->SetInput(0, bitmap);

linearTransferEffect->SetValue(D2D1_LINEARTRANSFER_PROP_RED_Y_INTERCEPT, -1.0f);
linearTransferEffect->SetValue(D2D1_LINEARTRANSFER_PROP_RED_SLOPE, 2.5f);
linearTransferEffect->SetValue(D2D1_LINEARTRANSFER_PROP_GREEN_Y_INTERCEPT, -1.0f);
linearTransferEffect->SetValue(D2D1_LINEARTRANSFER_PROP_GREEN_SLOPE, 5.0f);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(linearTransferEffect.Get());
m_d2dContext->EndDraw();
```



La funzione di trasferimento lineare viene creata in base alla inclinazione e all'intercettazione y per ogni canale specificato. L'intensità del pixel di output C viene calcolata con l'equazione: C'= mC + B, dove m è la pendenza della funzione lineare e B è l'intercetta Y della funzione lineare.

Questo effetto funziona su immagini alfa diritte e premoltiplicate. L'effetto restituisce bitmap alfa premoltiplicate.

## <a name="effect-properties"></a>Proprietà effetto

> [!Note]  
> Per tutti i canali delle proprietà di trasferimento lineare:
>
> -   L'intercetta Y non è vincolata e non è unita.
> -   La pendenza non è vincolata ed è senza unità.

 



| Nome visualizzato e enumerazione dell'indice                                                    | Tipo e valore predefinito           | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------|----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| RedYIntercept<br/> D2D1 \_ LINEARTRANSFER \_ prop \_ Red \_ Y \_ Interceptor<br/>     | FLOAT<br/> 0,0 f<br/> | L'intersezione Y della funzione lineare per il canale rosso.                                                                                                                                                                                                                                                                                                                                                                                                   |
| RedSlope<br/> D2D1 \_ LINEARTRANSFER \_ prop \_ Red \_ Slope<br/>                 | FLOAT<br/> 1,0 f<br/> | Pendenza della funzione lineare per il canale rosso.                                                                                                                                                                                                                                                                                                                                                                                                         |
| RedDisable<br/> D2D1 \_ LINEARTRANSFER \_ prop \_ Red \_ Disable<br/>             | BOOL<br/> FALSE<br/> | Se si imposta questo valore su TRUE, l'effetto non applica la funzione di trasferimento al canale rosso. Se si imposta questa opzione su FALSE, l'effetto applica la funzione RedLinearTransfer al canale rosso.                                                                                                                                                                                                                                                                    |
| GreenYIntercept<br/> D2D1 \_ LINEARTRANSFER \_ - \_ \_ intersezione Y \_ verde<br/> | FLOAT<br/> 0,0 f<br/> | L'intersezione Y della funzione lineare per il canale verde.                                                                                                                                                                                                                                                                                                                                                                                                 |
| GreenSlope<br/> \_ \_ Inclinazione verde della prop d2d1 LINEARTRANSFER \_ \_<br/>             | FLOAT<br/> 1,0 f<br/> | Pendenza della funzione lineare per il canale verde.                                                                                                                                                                                                                                                                                                                                                                                                       |
| GreenDisable<br/> D2D1 \_ LINEARTRANSFER \_ prop \_ Green \_ Disable<br/>         | BOOL<br/> FALSE<br/> | Se si imposta questo valore su TRUE, l'effetto non applica la funzione di trasferimento al canale verde. Se si imposta questa opzione su FALSE, viene applicata la funzione GreenLinearTransfer al canale verde.                                                                                                                                                                                                                                                                      |
| BlueYIntercept<br/> D2D1 \_ LINEARTRANSFER \_ ( \_ \_ intercetta Y \_ blu)<br/>   | FLOAT<br/> 0,0 f<br/> | L'intersezione Y della funzione lineare per il canale blu.                                                                                                                                                                                                                                                                                                                                                                                                  |
| BlueSlope<br/> D2D1 \_ LINEARTRANSFER \_ della \_ \_ pendenza blu<br/>               | FLOAT<br/> 1,0 f<br/> | Pendenza della funzione lineare per il canale blu.                                                                                                                                                                                                                                                                                                                                                                                                        |
| BlueDisable<br/> D2D1 \_ LINEARTRANSFER \_ prop \_ Blue \_ Disable<br/>           | BOOL<br/> FALSE<br/> | Se si imposta questo valore su TRUE, l'effetto non applica la funzione di trasferimento al canale blu. Se si imposta questa opzione su FALSE, viene applicata la funzione BlueLinearTransfer al canale blu.                                                                                                                                                                                                                                                                         |
| AlphaYIntercept<br/> D2D1 \_ LINEARTRANSFER \_ prop \_ Alpha \_ Y \_ intercetta<br/> | FLOAT<br/> 0,0 f<br/> | L'intersezione Y della funzione lineare per il canale alfa.                                                                                                                                                                                                                                                                                                                                                                                                 |
| AlphaSlope<br/> D2D1 \_ LINEARTRANSFER \_ prop \_ Alpha \_ Slope<br/>             | FLOAT<br/> 0,0 f<br/> | Pendenza della funzione lineare per il canale alfa.                                                                                                                                                                                                                                                                                                                                                                                                       |
| AlphaDisable<br/> D2D1 \_ LINEARTRANSFER \_ prop \_ Alpha \_ Disable<br/>         | BOOL<br/> FALSE<br/> | Se si imposta questo valore su TRUE, l'effetto non applica la funzione di trasferimento al canale alfa. Se si imposta questa opzione su FALSE, viene applicata la funzione AlphaLinearTransfer al canale alfa.                                                                                                                                                                                                                                                                      |
| ClampOutput<br/> D2D1 \_ LINEARTRANSFER \_ prop \_ \_ output Clamp<br/>           | BOOL<br/> FALSE<br/> | Indica se l'effetto fissa i valori dei colori a un valore compreso tra 0 e 1 prima che l'effetto passi i valori all'effetto successivo nel grafico. L'effetto blocca i valori prima di premoltiplicare l'alfa.<br/> Se si imposta questa impostazione su TRUE, i valori vengono bloccati dall'effetto. Se si imposta questa proprietà su FALSE, l'effetto non blocca i valori dei colori, mentre altri effetti e la superficie di output possono bloccare i valori se non hanno una precisione sufficientemente elevata.<br/> |



 

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

 

