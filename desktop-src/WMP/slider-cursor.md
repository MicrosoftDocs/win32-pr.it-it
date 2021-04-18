---
title: SLIDER. Cursor
description: L'attributo Cursor specifica o recupera un valore che indica quale cursore viene visualizzato quando il mouse è posizionato sul controllo Slider.
ms.assetid: 5b96a20c-b3a6-4e08-95b2-32937bb15cc6
keywords:
- Media Player SLIDER. Cursor Windows
topic_type:
- apiref
api_name:
- SLIDER.cursor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2cbc8f581d7d087545e666565dd03f649112064d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325122"
---
# <a name="slidercursor"></a>SLIDER. Cursor

L'attributo **Cursor** specifica o recupera un valore che indica quale cursore viene visualizzato quando il mouse è posizionato sul controllo Slider.

``` syntax
        elementID.cursor
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è una **stringa** di lettura/scrittura.



| Valore            | Descrizione                                                                                 |
|------------------|---------------------------------------------------------------------------------------------|
| sistema           | Cursore dipendente dalla piattaforma (in genere una freccia).                                               |
| a sinistra             | Valore predefinito. A sinistra.                                                                              |
| help             | La freccia con il punto interrogativo che indica la guida è disponibile.                                      |
| sizeall          | Freccia a quattro punte che punta a nord, Sud, est e ovest.                                   |
| sizenesw         | Freccia a due punte che indica nordest e sud-ovest.                                      |
| sizens           | Freccia a due punte che punta verso nord e sud.                                              |
| sizenwse         | Freccia a due punte che indica nord-ovest e sud-est.                                      |
| sizewe           | Freccia a due punte che indica ovest e est.                                                |
| UpArrow          | Freccia verticale che punta verso l'alto.                                                             |
| \*. ani o \* . cur | Qualsiasi file. ani o. cur (deve trovarsi nella stessa directory del file con estensione WMS o nel file con estensione WMZ). |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento SLIDER**](slider-element.md)
</dt> </dl>

 

 





