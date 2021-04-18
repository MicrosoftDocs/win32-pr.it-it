---
title: Effetto opacità
description: Questo effetto regola l'opacità di un'immagine moltiplicando il canale alfa dell'input in base al valore di opacità specificato. Ha un singolo input.
ms.assetid: a4995228-e08f-b543-0af1-e0eedfe8ecb2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfdc12aa8545f2742561490a3ddce799d6a1aa62
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302034"
---
# <a name="opacity-effect"></a>Effetto opacità

Questo effetto regola l'opacità di un'immagine moltiplicando il canale alfa dell'input in base al valore di opacità specificato. Ha un singolo input.

Il CLSID per questo effetto è CLSID \_ D2D1Opacity.

## <a name="effect-properties"></a>Proprietà effetto



| Nome visualizzato e enumerazione dell'indice              | Tipo e valore predefinito | Descrizione                                                                                                 |
|-------------------------------------------------|------------------------|-------------------------------------------------------------------------------------------------------------|
| Opacità \_ della \_ prop \_ Opacity d2d1 Opacity<br/> | FLOAT 1.0 f<br/>   | Moltiplicatore per il canale alfa dell'immagine di input. Il valore minimo è 0,0 f e il valore massimo è 1,0 f. |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------------|---------------------------------------------------|
| Client minimo supportato | App \[ Windows 10 desktop app \| Windows Store\] |
| Server minimo supportato | App \[ Windows 10 desktop app \| Windows Store\] |
| Intestazione                   | d2d1effects \_ 2. h                                  |
| Libreria                  | d2d1. lib, dxguid. lib                              |


## <a name="related-topics"></a>Argomenti correlati

* [Interfaccia ID2D1Effect](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
