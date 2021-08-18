---
title: TEXT.cursor
description: L'attributo cursor specifica o recupera un valore che indica quale cursore viene visualizzato quando il mouse è posizionato sul controllo Text.
ms.assetid: 360d4ed1-9c4f-4210-8e77-2dfbe7573869
keywords:
- Text.cursor Windows Media Player
topic_type:
- apiref
api_name:
- TEXT.cursor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72dc904371333dcdf3b9c80e441fb1d8254285bcd6193150ecd3df4032afd22d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134654"
---
# <a name="textcursor"></a>TEXT.cursor

**L'attributo cursor** specifica o recupera un valore che indica quale cursore viene visualizzato quando il mouse è posizionato sul controllo Text.

``` syntax
        elementID.cursor
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è una stringa di **lettura/scrittura.**



| Valore            | Descrizione                                                                                 |
|------------------|---------------------------------------------------------------------------------------------|
| sistema           | Valore predefinito. Cursore dipendente dalla piattaforma (in genere una freccia).                                      |
| Mano             | Mano.                                                                                       |
| help             | Freccia con punto interrogativo che indica che la Guida è disponibile.                                      |
| sizeall          | Freccia a quattro punte che punta a nord, sud, est e ovest.                                   |
| sizenesw         | Freccia a due punte che punta verso nord-est e sud-ovest.                                      |
| sizens           | Freccia a due punte che punta a nord e a sud.                                              |
| dimensioninwse         | Freccia a due punte che punta a nord-ovest e a sud-est.                                      |
| sizewe           | Freccia a due punte che punta a ovest e a est.                                                |
| uparrow          | Freccia verticale che punta verso l'alto.                                                             |
| \*.ani o \* .cur | Qualsiasi file con estensione ani o cur (deve essere nella stessa directory del file con estensione wms o nel file wmz). |



 

Vedere [l'attributo value](text-value.md) per un esempio che illustra come vengono usati **gli** attributi dell'elemento TEXT.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7.0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento TEXT**](text-element.md)
</dt> </dl>

 

 





