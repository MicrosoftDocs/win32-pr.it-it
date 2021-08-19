---
title: BUTTON.cursor
description: L'attributo cursor specifica o recupera il cursore che viene visualizzato quando il puntatore del mouse viene posizionato su BUTTON.
ms.assetid: 19bdbb23-00e2-45cf-b67d-9ada036b9c3b
keywords:
- Controllo BUTTON.cursor Windows Media Player
topic_type:
- apiref
api_name:
- BUTTON.cursor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa98c91080bc6d108e8ab62f0de99758c4eb6ba4229a83f8ded8b22bb2ec9695
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120123791"
---
# <a name="buttoncursor"></a>BUTTON.cursor

**L'attributo cursor** specifica o recupera il cursore che viene visualizzato quando il puntatore del mouse viene posizionato su **BUTTON.**

``` syntax
        elementID.cursor
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è una stringa di **lettura/scrittura.**



| Valore            | Descrizione                                                                                |
|------------------|--------------------------------------------------------------------------------------------|
| sistema           | Valore predefinito. Cursore dipendente dalla piattaforma (in genere una freccia).                                     |
| Mano             | Mano.                                                                                      |
| help             | Freccia con punto interrogativo che indica che la Guida è disponibile.                                     |
| sizeall          | Freccia a quattro punte che punta a nord, sud, est e ovest.                                  |
| sizenesw         | Freccia a due punte che punta a nord-est e a sud-ovest.                                     |
| dimensioni           | Freccia a due punte che punta verso nord e sud.                                             |
| sizenwse         | Freccia a due punte che punta a nord-ovest e a sud-est.                                     |
| sizewe           | Freccia a due punte che punta a ovest e a est.                                               |
| uparrow          | Freccia verticale che punta verso l'alto.                                                            |
| \*.ani o \* .cur | Qualsiasi file con estensione ani o cur (deve essere nella stessa directory del file wms o nel file con estensione wmz) |



 

## <a name="remarks"></a>Commenti

Se il sistema non riconosce il valore del cursore specificato, il valore del cursore rimane in corrispondenza del valore impostato in precedenza.

I percorsi dei nomi file del cursore vengono ignorati, quindi il file del cursore deve risiedere nella directory predefinita.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7.0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento BUTTON**](button-element.md)
</dt> </dl>

 

 





