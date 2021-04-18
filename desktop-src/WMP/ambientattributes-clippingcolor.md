---
title: AmbientAttributes.clippingColor
description: L'attributo clippingColor specifica o Recupera il colore da ritagliare dalla bitmap clippingImage.
ms.assetid: d6ea43d3-c118-43d3-bfdc-29ddd6ea4978
keywords:
- Media Player Windows AmbientAttributes. clippingColor
topic_type:
- apiref
api_name:
- AmbientAttributes.clippingColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ad526eb0f705d1fce95f3813a666420b29db9de
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331408"
---
# <a name="ambientattributesclippingcolor"></a>AmbientAttributes.clippingColor

L'attributo **clippingColor** specifica o Recupera il colore da ritagliare dalla bitmap **clippingImage** .

``` syntax
        elementID.clippingColor
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è una **stringa** di lettura/scrittura.



| Valore                                       | Descrizione                                       |
|---------------------------------------------|---------------------------------------------------|
| Auto                                        | Valore predefinito. Viene utilizzato il colore nella posizione del pixel 0, 0. |
| qualsiasi valore di colore di Microsoft Internet Explorer | Viene utilizzato il colore di Internet Explorer specificato.    |



 

## <a name="remarks"></a>Commenti

Il colore di ritaglio indica le aree di **clippingImage** (o **BackgroundImage** per la **visualizzazione** o la **visualizzazione**) che corrispondono a parti trasparenti e non selezionabili del controllo. Il colore di ritaglio può indicare più aree da ritagliare. Viene emesso un avviso se **clippingImage** è un jpg per avvertire la perdita di colore in jpg.

L'attributo **clippingColor** non è supportato dall'elemento **playlist** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Attributi di ambiente**](ambient-attributes.md)
</dt> <dt>

[**AmbientAttributes.clippingImage**](ambientattributes-clippingimage.md)
</dt> <dt>

[**Riferimento ai colori**](color-reference.md)
</dt> </dl>

 

 





