---
title: Effetto Gradazioni di grigio
description: Converte un'immagine in grigio monocromatico.
ms.assetid: 4e0b26ed-ba71-5f8f-db1e-f1b4e28fbd11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03b74e553074b3ee0c9ad4e0d5121b9b084884ddb030c75308eb9964531fc6b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119075336"
---
# <a name="grayscale-effect"></a>Effetto Gradazioni di grigio

Converte un'immagine in grigio monocromatico.

La scala di grigi usa l'effetto matrice di colori per la conversione in scala di grigi, usando la matrice seguente:

![matrice di conversione](images/grayscale-effect-matrix.png)

Il CLSID per questo effetto è CLSID \_ D2D1Grayscale.

-   [Immagine di esempio](#example-image)
-   [Proprietà degli effetti](#effect-properties)
-   [Requisiti](#requirements)
-   [Argomenti correlati](#related-topics)

## <a name="example-image"></a>Immagine di esempio

![esempio di output dell'effetto](images/grayscale-effect.png)

## <a name="effect-properties"></a>Proprietà degli effetti

Questo effetto non ha proprietà.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------------|---------------------------------------------------|
| Client minimo supportato | \[Windows 10 app desktop \| Windows Store\] |
| Server minimo supportato | \[Windows 10 app desktop \| Windows Store\] |
| Intestazione                   | d2d1effects \_ 2.h                                  |
| Libreria                  | d2d1.lib, dxguid.lib                              |


## <a name="related-topics"></a>Argomenti correlati

* [Interfaccia ID2D1Effect](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
