---
title: BUTTONGROUP. showBackground
description: L'attributo showBackground specifica o recupera un valore che indica se BUTTONGROUP Visualizza solo i pulsanti oppure Visualizza la bitmap completa specificata nell'attributo Image.
ms.assetid: 5c3fc873-937c-4dad-ac18-e7a37004ee1e
keywords:
- Media Player Windows BUTTONGROUP. showBackground
topic_type:
- apiref
api_name:
- BUTTONGROUP.showBackground
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31cc87260d4b0fca74d6063c757e6c3dae0db850
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326481"
---
# <a name="buttongroupshowbackground"></a>BUTTONGROUP. showBackground

L'attributo **showBackground** specifica o recupera un valore che indica se **ButtonGroup** Visualizza solo i pulsanti oppure Visualizza la bitmap completa specificata nell'attributo **Image** .

``` syntax
        elementID.showBackground
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è un **valore booleano** di lettura/scrittura.



| Valore | Descrizione                                                                                |
|-------|--------------------------------------------------------------------------------------------|
| true  | Vengono visualizzati i pulsanti e l'area non occupata dai pulsanti viene disegnata dalla bitmap dell'immagine. |
| false | Valore predefinito. Vengono visualizzati solo i pulsanti.                                                   |



 

## <a name="remarks"></a>Commenti

Quando **showBackground** è true, l'intera **immagine** principale sarà visibile.

Quando **showBackground** è false, verrà eseguito il rendering solo delle aree corrispondenti ai colori **mappingImage** assegnati. In altre parole, sarà visibile solo **BUTTONELEMENTs** con la loro **mappingColor** assegnata.

Se viene specificato un valore non valido, viene mantenuto lo stato precedente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento BUTTONGROUP**](buttongroup-element.md)
</dt> <dt>

[**BUTTONelement. mappingColor**](buttonelement-mappingcolor.md)
</dt> <dt>

[**BUTTONGROUP. image**](buttongroup-image.md)
</dt> <dt>

[**BUTTONGROUP. mappingImage**](buttongroup-mappingimage.md)
</dt> </dl>

 

 





