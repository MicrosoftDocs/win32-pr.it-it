---
title: BUTTONGROUP. Cursor
description: L'attributo Cursor specifica o Recupera il tipo di cursore visualizzato quando il mouse è posizionato su un pulsante in BUTTONGROUP.
ms.assetid: c1b7e3e1-862b-48c1-bd2d-d9abd9ada14c
keywords:
- Media Player di Windows BUTTONGROUP. Cursor
topic_type:
- apiref
api_name:
- BUTTONGROUP.cursor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7b3de12950aed383f48dcde5d8978724037f86e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329203"
---
# <a name="buttongroupcursor"></a>BUTTONGROUP. Cursor

L'attributo **Cursor** specifica o Recupera il tipo di cursore visualizzato quando il mouse è posizionato su un pulsante in **ButtonGroup**.

``` syntax
        elementID.cursor
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è una **stringa** di lettura/scrittura contenente uno dei valori seguenti.



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



 

## <a name="remarks"></a>Commenti

Il cursore specificato si applica a tutti i pulsanti presenti in **ButtonGroup**.

Se si specifica un valore di cursore non valido, rimane in corrispondenza del valore impostato in precedenza.

I percorsi dei nomi di file di cursore vengono ignorati, pertanto il file di cursore deve trovarsi nella directory predefinita.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento BUTTONGROUP**](buttongroup-element.md)
</dt> </dl>

 

 





