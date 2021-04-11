---
title: Effetto tinta
description: Questo effetto colora l'immagine di origine moltiplicando l'immagine di origine in base al colore specificato. Ha un singolo input.
ms.assetid: b0fd3598-26b6-faee-4f10-ebba96241bc8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f12e7593f9cb0695a6adb7b955fb66b13c8d00b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964149"
---
# <a name="tint-effect"></a>Effetto tinta

Questo effetto colora l'immagine di origine moltiplicando l'immagine di origine in base al colore specificato. Ha un singolo input.

Il CLSID per questo effetto è CLSID \_ D2D1Tint.

## <a name="effect-properties"></a>Proprietà effetto



| Nome visualizzato e enumerazione dell'indice                    | Tipo e valore predefinito                              | Descrizione                                                      |
|-------------------------------------------------------|-----------------------------------------------------|------------------------------------------------------------------|
| \_Colore della \_ prop tinta ColorD2D1 \_<br/>               | D2D1 \_ vector \_ 4F (1.0 f, 1.0 f, 1.0 f, 1.0 f)<br/> | I colori dell'immagine di origine vengono moltiplicati per questo valore.       |
| \_Output morsetto ClampOutputD2D1 tinta \_ prop \_ \_<br/> | BOOLFALSE<br/>                                | Indica se bloccare o meno i valori di output nell'intervallo compreso tra \[ 0 e 1 \] . |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------------|---------------------------------------------------|
| Client minimo supportato | App \[ Windows 10 desktop app \| Windows Store\] |
| Server minimo supportato | App \[ Windows 10 desktop app \| Windows Store\] |
| Intestazione                   | d2d1effects \_ 2. h                                  |
| Libreria                  | d2d1. lib, dxguid. lib                              |



 ## <a name="related-topics"></a>Argomenti correlati

* [Interfaccia ID2D1Effect](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
