---
title: Effetto compensazione DPI
description: Usare l'effetto di compensazione DPI per modificare automaticamente una bitmap di input in modo che corrisponda al valore DPI del contesto. Questa operazione è utile per le situazioni in cui viene creata o caricata una bitmap con un valore DPI diverso da quello dello schermo.
ms.assetid: EA8AD89B-A710-468F-A6F3-474DA29586F1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69a0477d2a57f39738fa9b1ce16c97995c60cf96
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874650"
---
# <a name="dpi-compensation-effect"></a>Effetto compensazione DPI

Usare l'effetto di compensazione DPI per modificare automaticamente una bitmap di input in modo che corrisponda al valore DPI del contesto. Questa operazione è utile per le situazioni in cui viene creata o caricata una bitmap con un valore DPI diverso da quello dello schermo.

Il CLSID per questo effetto è CLSID \_ D2D1DpiCompensation.

## <a name="effect-properties"></a>Proprietà effetto



| Nome visualizzato e enumerazione dell'indice                                                       | Descrizione                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| InterpolationMode<br/> \_Modalità di \_ \_ interpolazione della prop DPICOMPENSATION d2d1 \_<br/> | Modalità di interpolazione utilizzata dall'effetto per ridimensionare l'immagine.<br/> Il tipo è D2D1 \_ DPICOMPENSATION \_ Interpolation \_ mode.<br/> Il valore predefinito è D2D1 \_ DPICOMPENSATION \_ modalità di interpolazione \_ \_ lineare.<br/>                  |
| BorderMode<br/> \_ \_ \_ Modalità bordo prop DPICOMPENSATION \_ d2d1<br/>               | Modalità utilizzata per calcolare il bordo dell'immagine, soft o hard. Per altre informazioni, vedere [Border modes](https://www.bing.com/search?q=Border+modes) . <br/> Il tipo è D2D1 \_ Border \_ mode.<br/> Il valore predefinito è D2D1 \_ Border \_ mode \_ .<br/> |
| InputDpi<br/> \_Dpi di \_ input della prop DPICOMPENSATION \_ d2d1 \_<br/>                   | Valore DPI dell'immagine di input.<br/> Il tipo è FLOAT.<br/> Il valore predefinito è 96.0 f.<br/>                                                                                                                                    |



 

## <a name="interpolation-modes"></a>Modalità di interpolazione



| Enumerazione                                                       | Descrizione                                                                                                                                                                                          |
|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ DPICOMPENSATION- \_ modalità di interpolazione \_ \_ più vicina \_     | Campiona il punto singolo più vicino e lo utilizza. In questa modalità viene utilizzato un minor tempo di elaborazione, ma viene restituita l'immagine di qualità più bassa.                                                                           |
| D2D1 \_ DPICOMPENSATION- \_ modalità di interpolazione \_ \_ lineare                | Usa un esempio a quattro punti e un'interpolazione lineare. Questa modalità utilizza un tempo di elaborazione maggiore rispetto alla modalità adiacente più vicina, ma restituisce un'immagine di qualità superiore.                                           |
| D2D1 \_ DPICOMPENSATION- \_ modalità di interpolazione \_ \_ cubica                 | Usa un kernel cubico di esempio 16 per l'interpolazione. Questa modalità usa la maggior parte del tempo di elaborazione, ma restituisce un'immagine di qualità superiore.                                                                        |
| D2D1 \_ DPICOMPENSATION- \_ modalità di interpolazione più \_ \_ \_ lineare di esempio \_ | USA 4 campioni lineari all'interno di un singolo pixel per l'anti-aliasing dei bordi validi. Questa modalità è ideale per ridurre le dimensioni delle immagini con pochi pixel.                                              |
| D2D1 \_ DPICOMPENSATION \_ modalità di interpolazione \_ \_ anisotropico           | Usa il filtro anisotropico per campionare un modello in base alla forma trasformata della bitmap.                                                                                                     |
| D2D1 \_ DPICOMPENSATION- \_ modalità di interpolazione \_ \_ alta \_ qualità \_ cubica  | Usa un kernel cubico a dimensione variabile di alta qualità per eseguire un'downscaling dell'immagine se downscaling è associato alla matrice di trasformazione. USA quindi la modalità di interpolazione cubica per l'output finale. |



 

> [!Note]  
> Se non si seleziona una modalità, l'effetto predefinito è D2D1 \_ DPICOMPENSTION \_ modalità di interpolazione \_ \_ lineare.

 

## <a name="border-modes"></a>Modalità bordo



| Nome                     | Descrizione                                                                                                 |
|--------------------------|-------------------------------------------------------------------------------------------------------------|
| \_Modalità bordo \_ d2d1 \_ Soft | I pixel all'esterno dei limiti di input vengono generati dall' [effetto del bordo mirror](border.md). <br/> |
| \_Modalità bordo \_ d2d1 \_ | I pixel all'esterno dei limiti di input sono neri trasparenti.<br/>                                    |



 

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

 

