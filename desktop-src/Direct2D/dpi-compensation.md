---
title: Effetto di compensazione DPI
description: Usare l'effetto di compensazione DPI per regolare automaticamente una bitmap di input in modo che corrisponda al valore DPI del contesto. Ciò è utile per le situazioni in cui una bitmap viene creata o caricata in un valore DPI diverso rispetto allo schermo.
ms.assetid: EA8AD89B-A710-468F-A6F3-474DA29586F1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38f1390825087cabb9ee1bec65f2708990757ff25f08e71140be5be0fc6ae11e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119967117"
---
# <a name="dpi-compensation-effect"></a>Effetto di compensazione DPI

Usare l'effetto di compensazione DPI per regolare automaticamente una bitmap di input in modo che corrisponda al valore DPI del contesto. Ciò è utile per le situazioni in cui una bitmap viene creata o caricata in un valore DPI diverso rispetto allo schermo.

Il CLSID per questo effetto è CLSID \_ D2D1DpiCompensation.

## <a name="effect-properties"></a>Proprietà degli effetti



| Nome visualizzato ed enumerazione dell'indice                                                       | Descrizione                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| InterpolazioneMode<br/> MODALITÀ DI \_ \_ \_ INTERPOLAZIONE D2D1 DPICOMPENSATION PROP \_<br/> | Modalità di interpolazione utilizzata dall'effetto per ridimensionare l'immagine.<br/> Il tipo è D2D1 \_ DPICOMPENSATION \_ INTERPOLATION \_ MODE.<br/> Il valore predefinito è D2D1 \_ DPICOMPENSATION \_ INTERPOLATION \_ MODE LINEAR \_ .<br/>                  |
| BorderMode<br/> MODALITÀ BORDO DELLA PROPRIETÀ D2D1 \_ DPICOMPENSATION \_ \_ \_<br/>               | Modalità usata per calcolare il bordo dell'immagine, soft o hard. Per [altre informazioni, vedere](https://www.bing.com/search?q=Border+modes) Modalità bordo. <br/> Il tipo è D2D1 \_ BORDER \_ MODE.<br/> Il valore predefinito è D2D1 \_ BORDER \_ MODE \_ SOFT.<br/> |
| InputDpi<br/> D2D1 \_ DPICOMPENSATION \_ PROP \_ INPUT \_ DPI<br/>                   | Valore DPI dell'immagine di input.<br/> Il tipo è FLOAT.<br/> Il valore predefinito è 96.0f.<br/>                                                                                                                                    |



 

## <a name="interpolation-modes"></a>Modalità di interpolazione



| Enumerazione                                                       | Descrizione                                                                                                                                                                                          |
|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ DPICOMPENSATION \_ INTERPOLATION \_ MODE \_ NEAREST \_ NEIGHBOR     | Campiota il singolo punto più vicino e lo usa. Questa modalità usa meno tempo di elaborazione, ma restituisce l'immagine di qualità più bassa.                                                                           |
| MODALITÀ DI \_ INTERPOLAZIONE D2D1 DPICOMPENSATION \_ \_ \_ LINEARE                | Usa un campione di quattro punti e un'interpolazione lineare. Questa modalità usa più tempo di elaborazione rispetto alla modalità vicina più vicina, ma restituisce un'immagine di qualità superiore.                                           |
| D2D1 \_ DPICOMPENSATION \_ INTERPOLATION \_ MODE \_ CUBIC                 | Usa un kernel cubo di 16 campioni per l'interpolazione. Questa modalità usa il maggior tempo di elaborazione, ma restituisce un'immagine di qualità superiore.                                                                        |
| D2D1 \_ DPICOMPENSATION \_ INTERPOLATION \_ MODE \_ MULTI \_ SAMPLE \_ LINEAR | Usa 4 campioni lineari all'interno di un singolo pixel per un anti-aliasing dei bordi valido. Questa modalità è buona per ridurre di piccole quantità le immagini con pochi pixel.                                              |
| D2D1 \_ DPICOMPENSATION \_ INTERPOLATION \_ MODE \_ ANISOTROP           | Usa il filtro anisotropo per campionare un modello in base alla forma trasformata della bitmap.                                                                                                     |
| D2D1 \_ DPICOMPENSATION \_ INTERPOLATION \_ MODE \_ HIGH \_ QUALITY \_ CUBIC  | Usa un kernel cubico di qualità elevata di dimensioni variabili per eseguire una scalabilità preliminare dell'immagine se è coinvolta la scalabilità in basso nella matrice di trasformazione. Usa quindi la modalità di interpolazione cubica per l'output finale. |



 

> [!Note]  
> Se non si seleziona una modalità, per impostazione predefinita l'effetto è D2D1 \_ DPICOMPENSTION \_ INTERPOLATION \_ MODE \_ LINEAR.

 

## <a name="border-modes"></a>Modalità bordo



| Nome                     | Descrizione                                                                                                 |
|--------------------------|-------------------------------------------------------------------------------------------------------------|
| MODALITÀ BORDO D2D1 \_ \_ \_ SOFT | I pixel all'esterno dei limiti di input vengono generati [dall'effetto del bordo speculare.](border.md) <br/> |
| MODALITÀ BORDO D2D1 \_ \_ \_ HARD | I pixel all'esterno dei limiti di input sono di colore nero trasparente.<br/>                                    |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato | Windows 8 e l'aggiornamento della piattaforma Windows 7 \[ app desktop \| Windows Store\] |
| Server minimo supportato | Windows 8 e l'aggiornamento della piattaforma Windows 7 \[ app desktop \| Windows Store\] |
| Intestazione                   | d2d1effects.h                                                                      |
| Libreria                  | d2d1.lib, dxguid.lib                                                               |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

