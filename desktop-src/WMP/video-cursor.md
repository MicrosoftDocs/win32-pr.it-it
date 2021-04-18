---
title: VIDEO. Cursor
description: L'attributo Cursor specifica o Recupera il valore del cursore utilizzato quando il mouse è posizionato su un'area selezionabile del video.
ms.assetid: 2faaf9cd-47be-47d5-ad4e-8f3bb322d812
keywords:
- Media Player di Windows VIDEO. Cursor
topic_type:
- apiref
api_name:
- VIDEO.cursor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c23ab90b974ad5a7f9cfaf9fcc598371cd0697f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330453"
---
# <a name="videocursor"></a>VIDEO. Cursor

L'attributo **Cursor** specifica o Recupera il valore del cursore utilizzato quando il mouse è posizionato su un'area selezionabile del video.

``` syntax
        elementID.cursor
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è una **stringa** di lettura/scrittura.



| Valore            | Descrizione                                                                                 |
|------------------|---------------------------------------------------------------------------------------------|
| sistema           | Cursore dipendente dalla piattaforma (in genere una freccia).                                               |
| a sinistra             | A sinistra.                                                                                       |
| help             | La freccia con il punto interrogativo che indica la guida è disponibile.                                      |
| sizeall          | Freccia a quattro punte che punta a nord, Sud, est e ovest.                                   |
| sizenesw         | Freccia a due punte che indica nordest e sud-ovest.                                      |
| sizens           | Freccia a due punte che punta verso nord e sud.                                              |
| sizenwse         | Freccia a due punte che indica nord-ovest e sud-est.                                      |
| sizewe           | Freccia a due punte che indica ovest e est.                                                |
| UpArrow          | Freccia verticale che punta verso l'alto.                                                             |
| \*. ani o \* . cur | Qualsiasi file. ani o. cur (deve trovarsi nella stessa directory del file con estensione WMS o nel file con estensione WMZ). |



 

## <a name="remarks"></a>Commenti

A scopo di rendering, System è il cursore predefinito. Il valore predefinito recuperato da questo attributo è "" (stringa vuota).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento VIDEO**](video-element.md)
</dt> </dl>

 

 





