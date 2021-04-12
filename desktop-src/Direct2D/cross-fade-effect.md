---
title: Effetto dissolvenza incrociata
description: Questo effetto combina due immagini aggiungendo pixel ponderati dalle immagini di input. Dispone di due input, denominato destinazione e origine.
ms.assetid: 5214b70a-d024-ba3e-771f-07d98d2278ba
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 904ac8e4e27efc646bb71b1766c8763bd64beb2d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517728"
---
# <a name="cross-fade-effect"></a>Effetto dissolvenza incrociata

Questo effetto combina due immagini aggiungendo pixel ponderati dalle immagini di input. Dispone di due input, denominato destinazione e origine.

La formula Cross Fade è **output = Weight \* Destination + (1-Weight) \* source**.

Il CLSID per questo effetto è CLSID \_ D2D1CrossFade.

## <a name="effect-properties"></a>Proprietà effetto

| Nome visualizzato e enumerazione dell'indice             | Tipo e valore predefinito | Descrizione                                                                                                                                                                                                                                                       |
|------------------------------------------------|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_Peso della \_ prop incrociata WeightD2D1 \_<br/> | FLOAT 0,5 f<br/>   | Quanto pesare i valori dei colori dell'immagine di origine rispetto all'immagine di destinazione. Il valore minimo è 0,0 f (usare esclusivamente l'immagine di destinazione per determinare l'output) e il valore massimo è 1,0 f (usare esclusivamente l'immagine di origine per determinare l'output). |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------------|---------------------------------------------------|
| Client minimo supportato | App \[ Windows 10 desktop app \| Windows Store\] |
| Server minimo supportato | App \[ Windows 10 desktop app \| Windows Store\] |
| Intestazione                   | d2d1effects \_ 2. h                                  |
| Libreria                  | d2d1. lib, dxguid. lib                              |

## <a name="related-topics"></a>Argomenti correlati

* [Interfaccia ID2D1Effect](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
