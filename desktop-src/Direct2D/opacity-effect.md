---
title: Effetto di opacità
description: Questo effetto regola l'opacità di un'immagine moltiplicando il canale alfa dell'input per il valore di opacità specificato. Ha un singolo input.
ms.assetid: a4995228-e08f-b543-0af1-e0eedfe8ecb2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58073e3b692b45f86f57c61571d81f5add47427c8a1a801ac43121b37aa43a67
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119636231"
---
# <a name="opacity-effect"></a>Effetto di opacità

Questo effetto regola l'opacità di un'immagine moltiplicando il canale alfa dell'input per il valore di opacità specificato. Ha un singolo input.

Il CLSID per questo effetto è CLSID \_ D2D1Opacity.

## <a name="effect-properties"></a>Proprietà degli effetti



| Enumerazione del nome visualizzato e dell'indice              | Tipo e valore predefinito | Descrizione                                                                                                 |
|-------------------------------------------------|------------------------|-------------------------------------------------------------------------------------------------------------|
| Opacità D2D1 \_ OPACITY \_ PROP \_ OPACITY<br/> | FLOAT1.0f<br/>   | Moltiplicatore per il canale alfa dell'immagine di input. Il valore minimo è 0,0f e il valore massimo è 1,0f. |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------------|---------------------------------------------------|
| Client minimo supportato | \[Windows 10 app desktop \| Windows Store\] |
| Server minimo supportato | \[Windows 10 app desktop \| Windows Store\] |
| Intestazione                   | d2d1effects \_ 2.h                                  |
| Libreria                  | d2d1.lib, dxguid.lib                              |


## <a name="related-topics"></a>Argomenti correlati

* [Interfaccia ID2D1Effect](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
