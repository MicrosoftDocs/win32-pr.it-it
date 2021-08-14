---
title: BUTTONGROUP.showBackground
description: L'attributo showBackground specifica o recupera un valore che indica se BUTTONGROUP visualizza solo i pulsanti o visualizza la bitmap completa specificata nell'attributo image.
ms.assetid: 5c3fc873-937c-4dad-ac18-e7a37004ee1e
keywords:
- BUTTONGROUP.showBackground Windows Media Player
topic_type:
- apiref
api_name:
- BUTTONGROUP.showBackground
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb95b707fa7e14b00e86c5a65949ff9fba3ce3db32745116fa65ca4c53ac1998
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118342674"
---
# <a name="buttongroupshowbackground"></a>BUTTONGROUP.showBackground

**L'attributo showBackground** specifica o recupera un valore che indica se **BUTTONGROUP** visualizza solo i pulsanti oppure visualizza la bitmap completa specificata nell'attributo **image.**

``` syntax
        elementID.showBackground
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è un valore booleano di **lettura/scrittura.**



| Valore | Descrizione                                                                                |
|-------|--------------------------------------------------------------------------------------------|
| true  | I pulsanti vengono visualizzati e l'area non occupata dai pulsanti viene disegnata dalla bitmap Immagine. |
| false | Valore predefinito. Vengono visualizzati solo i pulsanti.                                                   |



 

## <a name="remarks"></a>Commenti

Quando **showBackground** è true, l'intera **immagine principale** sarà visibile.

Quando **showBackground** è false, verrà eseguito il rendering solo delle aree corrispondenti al **mapping** assegnatoI colori dell'immagine. In altre parole, saranno **visibili solo gli elementi BUTTONELEMEN Con** **mappingColor** assegnato.

Se viene specificato un valore non valido, viene mantenuto lo stato precedente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7.0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento BUTTONGROUP**](buttongroup-element.md)
</dt> <dt>

[**BUTTONELEMENT.mappingColor**](buttonelement-mappingcolor.md)
</dt> <dt>

[**BUTTONGROUP.image**](buttongroup-image.md)
</dt> <dt>

[**BUTTONGROUP.mappingImage**](buttongroup-mappingimage.md)
</dt> </dl>

 

 





