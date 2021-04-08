---
title: Effetto trasferimento gamma
description: Usare l'effetto di trasferimento gamma per eseguire il mapping delle intensità dei colori di un'immagine usando una funzione gamma creata usando un'ampiezza, un esponente e un offset forniti per ogni canale.
ms.assetid: 0E0455CA-CFCA-4C4F-9DFA-1DB6A5205F6A
keywords:
- effetto trasferimento gamma
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b806ac8f59efe1b3fad3b61edc7f88f72b143f9c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874185"
---
# <a name="gamma-transfer-effect"></a>Effetto trasferimento gamma

Usare l'effetto di trasferimento gamma per eseguire il mapping delle intensità dei colori di un'immagine usando una funzione gamma creata usando un'ampiezza, un esponente e un offset forniti per ogni canale.

Il CLSID per questo effetto è CLSID \_ D2D1GammaTransfer. Per usare questo effetto, aggiungere dxguid. lib alle dipendenze del linker.

-   [Immagine di esempio](#example-image)
-   [Proprietà effetto](#effect-properties)
-   [Bitmap di output](#output-bitmap)
-   [Requisiti](#requirements)
-   [Argomenti correlati](#related-topics)

## <a name="example-image"></a>Immagine di esempio



| Prima                                                         |
|----------------------------------------------------------------|
| ![immagine prima dell'effetto.](images/default-before.jpg)     |
| After                                                          |
| ![immagine dopo la trasformazione.](images/14-gammatransfer.png) |



 


```C++
ComPtr<ID2D1Effect> gammaTransferEffect;
m_d2dContext->CreateEffect(CLSID_D2D1GammaTransfer, &gammaTransferEffect);

gammaTransferEffect->SetInput(0, bitmap);

gammaTransferEffect->SetValue(D2D1_GAMMATRANSFER_PROP_RED_EXPONENT, 0.25f);
gammaTransferEffect->SetValue(D2D1_GAMMATRANSFER_PROP_GREEN_EXPONENT, 0.25f);
gammaTransferEffect->SetValue(D2D1_GAMMATRANSFER_PROP_BLUE_EXPONENT, 0.25f);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(gammaTransferEffect.Get());
m_d2dContext->EndDraw();
```



Questo effetto applica una funzione di trasferimento gamma basata sull'equazione qui.

L'intensità dei pixel di input viene rappresentata come C e l'intensità del pixel di output come C. C'= \* <sup>esponente</sup> c di ampiezza + offset

Questo effetto funziona su immagini alfa diritte e premoltiplicate. L'effetto restituisce bitmap alfa premoltiplicate.

## <a name="effect-properties"></a>Proprietà effetto

> [!Note]  
> Per tutti i canali delle proprietà di trasferimento gamma:
>
> -   Il valore di ampiezza non è associato ed è senza unità.
> -   Il valore dell'esponente non è associato ed è senza unità.
> -   Il valore di offset non è associato ed è senza unità.

 



| Nome visualizzato e enumerazione dell'indice                                               | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| RedAmplitude<br/> D2D1 \_ GAMMATRANSFER \_ prop \_ Red \_ ampiezze<br/>     | Ampiezza della funzione di trasferimento gamma per il canale rosso. Il tipo è FLOAT.<br/> Il valore predefinito è 1.0 f.<br/>                                                                                                                                                                                                                                                                                                                                                                                             |
| RedExponent<br/> \_ \_ \_ Esponente Red d2d1 GAMMATRANSFER Prop \_<br/>       | Esponente della funzione di trasferimento gamma per il canale rosso. Il tipo è FLOAT.<br/> Il valore predefinito è 1.0 f.<br/>                                                                                                                                                                                                                                                                                                                                                                                              |
| RedOffset<br/> \_ \_ \_ Offset rosso d2d1 GAMMATRANSFER \_ prop<br/>           | Offset della funzione di trasferimento gamma per il canale rosso. Il tipo è FLOAT.<br/> Il valore predefinito è 0,0 f.<br/>                                                                                                                                                                                                                                                                                                                                                                                                |
| RedDisable<br/> D2D1 \_ GAMMATRANSFER \_ prop \_ Red \_ Disable<br/>         | Se si imposta su TRUE, la funzione di trasferimento non viene applicata al canale rosso. Viene utilizzata una funzione di trasferimento identità. Se si imposta questa opzione su FALSE, viene applicata la funzione di trasferimento gamma al canale rosso. Il tipo è BOOL.<br/> Il valore predefinito è FALSE.<br/>                                                                                                                                                                                                                                                |
| GreenAmplitude<br/> D2D1 \_ GAMMATRANSFER \_ - \_ \_ ampiezza verde<br/> | Ampiezza della funzione di trasferimento gamma per il canale verde. Il tipo è FLOAT.<br/> Il valore predefinito è 1.0 f.<br/>                                                                                                                                                                                                                                                                                                                                                                                           |
| GreenExponent<br/> \_ \_ \_ Esponente verde della prop d2d1 GAMMATRANSFER \_<br/>   | Esponente della funzione di trasferimento gamma per il canale verde. Il tipo è FLOAT.<br/> Il valore predefinito è 1.0 f.<br/>                                                                                                                                                                                                                                                                                                                                                                                            |
| GreenOffset<br/> \_ \_ \_ Offset verde prop d2d1 \_ GAMMATRANSFER<br/>       | Offset della funzione di trasferimento gamma per il canale verde. Il tipo è FLOAT.<br/> Il valore predefinito è 0,0 f.<br/>                                                                                                                                                                                                                                                                                                                                                                                              |
| GreenDisable<br/> D2D1 \_ GAMMATRANSFER \_ prop \_ Green \_ Disable<br/>     | Se si imposta su TRUE, la funzione di trasferimento non viene applicata al canale verde. Viene utilizzata una funzione di trasferimento identità. Se si imposta questa opzione su FALSE, viene applicata la funzione di trasferimento gamma al canale verde. Il tipo è BOOL.<br/> Il valore predefinito è FALSE.<br/>                                                                                                                                                                                                                                            |
| BlueAmplitude<br/> D2D1 \_ GAMMATRANSFER \_ - \_ \_ ampiezza blu<br/>   | Ampiezza della funzione di trasferimento gamma per il canale blu. Il tipo è FLOAT.<br/> Il valore predefinito è 1.0 f.<br/>                                                                                                                                                                                                                                                                                                                                                                                            |
| BlueExponent<br/> \_ \_ \_ Esponente blu \_ prop d2d1 GAMMATRANSFER<br/>     | Esponente della funzione di trasferimento gamma per il canale blu. Il tipo è FLOAT.<br/> Il valore predefinito è 1.0 f.<br/>                                                                                                                                                                                                                                                                                                                                                                                             |
| BlueOffset<br/> \_ \_ \_ Offset blu prop d2d1 \_ GAMMATRANSFER<br/>         | Offset della funzione di trasferimento gamma per il canale blu. Il tipo è FLOAT.<br/> Il valore predefinito è 0,0 f.<br/>                                                                                                                                                                                                                                                                                                                                                                                               |
| BlueDisable<br/> D2D1 \_ GAMMATRANSFER \_ prop \_ Blue \_ Disable<br/>       | Se si imposta su TRUE, la funzione di trasferimento non viene applicata al canale blu. Viene utilizzata una funzione di trasferimento identità. Se si imposta questa opzione su FALSE, viene applicata la funzione di trasferimento gamma al canale blu. Il tipo è BOOL.<br/> Il valore predefinito è FALSE.<br/>                                                                                                                                                                                                                                              |
| AlphaAmplitude<br/> D2D1 \_ GAMMATRANSFER \_ prop \_ Alpha \_ ampiezza<br/> | Ampiezza della funzione di trasferimento gamma per il canale alfa. Il tipo è FLOAT.<br/> Il valore predefinito è 1.0 f.<br/>                                                                                                                                                                                                                                                                                                                                                                                           |
| AlphaExponent<br/> \_ \_ \_ Esponente alfa d2d1 GAMMATRANSFER Prop \_<br/>   | Esponente della funzione di trasferimento gamma per il canale alfa. Il tipo è FLOAT.<br/> Il valore predefinito è 1.0 f.<br/>                                                                                                                                                                                                                                                                                                                                                                                            |
| AlphaOffset<br/> \_ \_ \_ Offset alfa d2d1 GAMMATRANSFER \_ prop<br/>       | Offset della funzione di trasferimento gamma per il canale alfa. Il tipo è FLOAT.<br/> Il valore predefinito è 0,0 f.<br/>                                                                                                                                                                                                                                                                                                                                                                                              |
| AlphaDisable<br/> D2D1 \_ GAMMATRANSFER \_ prop \_ Alpha \_ Disable<br/>     | Se si imposta su TRUE, la funzione di trasferimento non viene applicata al canale alfa. Viene utilizzata una funzione di trasferimento identità. Se si imposta questa opzione su FALSE, viene applicata la funzione di trasferimento gamma al canale alfa. Il tipo è BOOL.<br/> Il valore predefinito è FALSE.<br/>                                                                                                                                                                                                                                            |
| ClampOutput<br/> D2D1 \_ GAMMATRANSFER \_ prop \_ \_ output Clamp<br/>       | Indica se l'effetto fissa i valori dei colori a un valore compreso tra 0 e 1 prima che l'effetto passi i valori all'effetto successivo nel grafico. L'effetto blocca i valori prima di premoltiplicare l'alfa.<br/> Se si imposta questa impostazione su TRUE, i valori vengono bloccati dall'effetto. Se si imposta questa proprietà su FALSE, l'effetto non blocca i valori dei colori, mentre altri effetti e la superficie di output possono bloccare i valori se non hanno una precisione sufficientemente elevata.<br/> Il tipo è BOOL.<br/> Il valore predefinito è FALSE.<br/> |



 

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

 

