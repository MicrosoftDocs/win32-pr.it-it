---
title: SLIDER. affiancato
description: L'attributo affiancato specifica o recupera un valore che indica se l'immagine del dispositivo di scorrimento verrà affiancata.
ms.assetid: 159a2972-a0eb-4e43-a083-e124e56782f5
keywords:
- Media Player Windows SLIDER. tiled
topic_type:
- apiref
api_name:
- SLIDER.tiled
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b1448f496ee45d6c8b01356499b9628c745d69f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328198"
---
# <a name="slidertiled"></a>SLIDER. affiancato

L'attributo **affiancato** specifica o recupera un valore che indica se l'immagine del dispositivo di scorrimento verrà affiancata.

``` syntax
        elementID.tiled
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è un **valore booleano** di lettura/scrittura.



| Valore | Descrizione                                                                                 |
|-------|---------------------------------------------------------------------------------------------|
| true  | Valore predefinito. La bitmap dell'immagine verrà ripetuta fino a riempire l'intera area del controllo. |
| false | L'immagine non verrà affiancata.                                                                |



 

## <a name="remarks"></a>Commenti

Questo attributo si applica solo se si usano immagini di primo piano e di sfondo per definire un controllo dispositivo di scorrimento. Se le immagini sono più piccole dell'area definita del dispositivo di scorrimento e l'attributo **affiancato** è impostato su true, le immagini verranno ripetute fino a riempire l'intera lunghezza del controllo.

È possibile utilizzare questo attributo in combinazione con l'attributo **borderSize** . L'attributo **borderSize** consente di definire un bordo che non viene ripetuto durante l'affiancamento.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento SLIDER**](slider-element.md)
</dt> <dt>

[**SLIDER. backgroundImage**](slider-backgroundimage.md)
</dt> <dt>

[**SLIDER. borderSize**](slider-bordersize.md)
</dt> <dt>

[**SLIDER. foregroundImage**](slider-foregroundimage.md)
</dt> </dl>

 

 





