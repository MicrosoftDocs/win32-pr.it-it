---
title: BUTTONELEMENT.cursor
description: L'attributo cursor specifica o recupera il valore del cursore BUTTONELEMENT visualizzato quando il puntatore del mouse viene posizionato su BUTTONELEMENT.
ms.assetid: 29e7fadb-30d8-40e4-9a64-6b6f45eac80a
keywords:
- BUTTONELEMENT.cursor Windows Media Player
topic_type:
- apiref
api_name:
- BUTTONELEMENT.cursor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82f08d8e6b26ac2227d9040249b2daca55dcbe0ec068e120f1aba962bea0f089
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119764481"
---
# <a name="buttonelementcursor"></a>BUTTONELEMENT.cursor

**L'attributo cursor** specifica o recupera il valore del **cursore BUTTONELEMENT** che viene visualizzato quando il mouse si trova su **BUTTONELEMENT.**

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
| sizenesw         | Freccia a due punte che punta a nord-est e a sud-ovest.                                      |
| dimensioni           | Freccia a due punte che punta verso nord e sud.                                              |
| sizenwse         | Freccia a due punte che punta a nord-ovest e a sud-est.                                      |
| sizewe           | Freccia a due punte che punta a ovest e a est.                                                |
| uparrow          | Freccia verticale che punta verso l'alto.                                                             |
| \*.ani o \* .cur | Qualsiasi file con estensione ani o cur (deve essere nella stessa directory del file wms o nel file con estensione wmz). |



 

## <a name="remarks"></a>Commenti

Se viene specificato un valore non valido, viene mantenuto il valore precedente.

I percorsi dei nomi file del cursore vengono ignorati, quindi il file del cursore deve risiedere nella directory predefinita.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7.0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento BUTTONELEMENT**](buttonelement-element.md)
</dt> </dl>

 

 





