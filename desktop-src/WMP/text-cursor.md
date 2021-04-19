---
title: TEXT. Cursor
description: L'attributo Cursor specifica o recupera un valore che indica quale cursore viene visualizzato quando il mouse si trova sul controllo di testo.
ms.assetid: 360d4ed1-9c4f-4210-8e77-2dfbe7573869
keywords:
- Media Player di Windows TEXT. Cursor
topic_type:
- apiref
api_name:
- TEXT.cursor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8cf7b135ed0a99b5c65f760a08e4e7083234674
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325227"
---
# <a name="textcursor"></a>TEXT. Cursor

L'attributo **Cursor** specifica o recupera un valore che indica quale cursore viene visualizzato quando il mouse si trova sul controllo di testo.

``` syntax
        elementID.cursor
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è una **stringa** di lettura/scrittura.



| Valore            | Descrizione                                                                                 |
|------------------|---------------------------------------------------------------------------------------------|
| sistema           | Valore predefinito. Cursore dipendente dalla piattaforma (in genere una freccia).                                      |
| a sinistra             | A sinistra.                                                                                       |
| help             | La freccia con il punto interrogativo che indica la guida è disponibile.                                      |
| sizeall          | Freccia a quattro punte che punta a nord, Sud, est e ovest.                                   |
| sizenesw         | Freccia a due punte che indica nordest e sud-ovest.                                      |
| sizens           | Freccia a due punte che punta verso nord e sud.                                              |
| sizenwse         | Freccia a due punte che indica nord-ovest e sud-est.                                      |
| sizewe           | Freccia a due punte che indica ovest e est.                                                |
| UpArrow          | Freccia verticale che punta verso l'alto.                                                             |
| \*. ani o \* . cur | Qualsiasi file. ani o. cur (deve trovarsi nella stessa directory del file con estensione WMS o nel file con estensione WMZ). |



 

Vedere l'attributo [value](text-value.md) per un esempio che illustra la modalità di utilizzo degli attributi dell'elemento di **testo** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento TEXT**](text-element.md)
</dt> </dl>

 

 





