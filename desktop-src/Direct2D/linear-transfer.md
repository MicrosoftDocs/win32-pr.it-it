---
title: Effetto di trasferimento lineare
description: Usare l'effetto di trasferimento lineare per eseguire il mapping delle intensità dei colori di un'immagine usando una funzione lineare creata da un elenco di valori specificati per ogni canale.
ms.assetid: 22DC496E-2958-4726-A74D-B3DE934F507C
keywords:
- effetto di trasferimento lineare
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dcb2bb688d1e8ebf4b1b1ebfdd531d900755b46840bada2bade49d957ed0f6c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119385296"
---
# <a name="linear-transfer-effect"></a>Effetto di trasferimento lineare

Usare l'effetto di trasferimento lineare per eseguire il mapping delle intensità dei colori di un'immagine usando una funzione lineare creata da un elenco di valori specificati per ogni canale.

Il CLSID per questo effetto è CLSID \_ D2D1LinearTransfer.

-   [Immagine di esempio](#example-image)
-   [Proprietà degli effetti](#effect-properties)
-   [Requisiti](#requirements)
-   [Argomenti correlati](#related-topics)

## <a name="example-image"></a>Immagine di esempio



| Prima                                                          |
|-----------------------------------------------------------------|
| ![l'immagine prima dell'effetto.](images/default-before.jpg)      |
| After                                                           |
| ![l'immagine dopo la trasformazione.](images/13-lineartransfer.png) |



 


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



La funzione di trasferimento lineare viene creata in base al inclinazione e all'intercetta y per ogni canale specificato. L'intensità in pixel di output C viene calcolata con l'equazione: C' = mC + B, dove m è il inclinazione della funzione lineare e B è l'intercetta Y della funzione lineare.

Questo effetto funziona su immagini alfa rette e premoltiliate. L'effetto restituisce bitmap alfa premoltiliate.

## <a name="effect-properties"></a>Proprietà degli effetti

> [!Note]  
> Per tutti i canali delle proprietà di trasferimento lineare:
>
> -   L'intercetta Y non è delimitata ed è senza unità.
> -   Il inclinazione non è delimitato ed è senza unità.

 



| Enumerazione del nome visualizzato e dell'indice                                                    | Tipo e valore predefinito           | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------|----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| RedYIntercept<br/> D2D1 \_ LINEARTRANSFER \_ PROP \_ RED \_ Y \_ INTERCEPT<br/>     | FLOAT<br/> 0,0f<br/> | Intercetta Y della funzione lineare per il canale Rosso.                                                                                                                                                                                                                                                                                                                                                                                                   |
| RedSlope<br/> D2D1 \_ LINEARTRANSFER \_ PROP \_ RED \_ SLOPE<br/>                 | FLOAT<br/> 1.0f<br/> | Inclinazione della funzione lineare per il canale Rosso.                                                                                                                                                                                                                                                                                                                                                                                                         |
| RedDisable<br/> D2D1 \_ LINEARTRANSFER \_ PROP \_ RED \_ DISABLE<br/>             | BOOL<br/> FALSE<br/> | Se si imposta questa proprietà su TRUE, l'effetto non applica la funzione di trasferimento al canale Rosso. Se si imposta questa proprietà su FALSE, l'effetto applica la funzione RedLinearTransfer al canale Red.                                                                                                                                                                                                                                                                    |
| GreenYIntercept<br/> D2D1 \_ LINEARTRANSFER \_ PROP \_ GREEN \_ Y \_ INTERCEPT<br/> | FLOAT<br/> 0,0f<br/> | Intercetta Y della funzione lineare per il canale verde.                                                                                                                                                                                                                                                                                                                                                                                                 |
| GreenSlope<br/> D2D1 \_ LINEARTRANSFER \_ PROP \_ GREEN \_ SLOPE<br/>             | FLOAT<br/> 1.0f<br/> | Inclinazione della funzione lineare per il canale verde.                                                                                                                                                                                                                                                                                                                                                                                                       |
| GreenDisable<br/> D2D1 \_ LINEARTRANSFER \_ PROP \_ GREEN \_ DISABLE<br/>         | BOOL<br/> FALSE<br/> | Se si imposta questa proprietà su TRUE, l'effetto non applica la funzione di trasferimento al canale verde. Se si imposta questa proprietà su FALSE, la funzione GreenLinearTransfer viene applicata al canale Verde.                                                                                                                                                                                                                                                                      |
| BlueYIntercept<br/> D2D1 \_ LINEARTRANSFER \_ PROP \_ BLUE \_ Y \_ INTERCEPT<br/>   | FLOAT<br/> 0,0f<br/> | Intercetta Y della funzione lineare per il canale Blu.                                                                                                                                                                                                                                                                                                                                                                                                  |
| BlueSlope<br/> D2D1 \_ LINEARTRANSFER \_ PROP \_ BLUE \_ SLOPE<br/>               | FLOAT<br/> 1.0f<br/> | Inclinazione della funzione lineare per il canale Blu.                                                                                                                                                                                                                                                                                                                                                                                                        |
| BlueDisable<br/> D2D1 \_ LINEARTRANSFER \_ PROP \_ BLUE \_ DISABLE<br/>           | BOOL<br/> FALSE<br/> | Se si imposta questa proprietà su TRUE, l'effetto non applica la funzione di trasferimento al canale Blu. Se si imposta questa proprietà su FALSE, la funzione BlueLinearTransfer viene applicata al canale Blue.                                                                                                                                                                                                                                                                         |
| AlphaYIntercept<br/> D2D1 \_ LINEARTRANSFER \_ PROP \_ ALPHA \_ Y \_ INTERCEPT<br/> | FLOAT<br/> 0,0f<br/> | Intercetta Y della funzione lineare per il canale Alfa.                                                                                                                                                                                                                                                                                                                                                                                                 |
| AlphaSlope<br/> D2D1 \_ LINEARTRANSFER \_ PROP \_ ALPHA \_ SLOPE<br/>             | FLOAT<br/> 0,0f<br/> | Inclinazione della funzione lineare per il canale Alfa.                                                                                                                                                                                                                                                                                                                                                                                                       |
| AlphaDisable<br/> D2D1 \_ LINEARTRANSFER \_ PROP \_ ALPHA \_ DISABLE<br/>         | BOOL<br/> FALSE<br/> | Se si imposta questa proprietà su TRUE, l'effetto non applica la funzione di trasferimento al canale Alfa. Se si imposta questa opzione su FALSE, la funzione AlphaLinearTransfer viene applicata al canale Alfa.                                                                                                                                                                                                                                                                      |
| ClampOutput<br/> OUTPUT DI D2D1 \_ LINEARTRANSFER \_ PROP \_ CLAMP \_<br/>           | BOOL<br/> FALSE<br/> | Indica se l'effetto stringe i valori di colore tra 0 e 1 prima che l'effetto passi i valori all'effetto successivo nel grafico. L'effetto stringe i valori prima di premultiplare il valore alfa .<br/> Se si imposta questa opzione su TRUE, l'effetto stringerà i valori. Se si imposta questa proprietà su FALSE, l'effetto non stringerà i valori di colore, ma altri effetti e la superficie di output potrebbero stringere i valori se non hanno una precisione sufficientemente elevata.<br/> |



 

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

 

