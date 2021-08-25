---
title: AmbientAttributes.clippingColor
description: L'attributo clippingColor specifica o recupera il colore da ritagliare dalla bitmap clippingImage.
ms.assetid: d6ea43d3-c118-43d3-bfdc-29ddd6ea4978
keywords:
- AmbientAttributes.clippingColor Windows Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.clippingColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 299ee63b93abfdea337bb25e8b399e6011fb42d7fa4e1e0c09b3feb259d4f1d6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119902811"
---
# <a name="ambientattributesclippingcolor"></a>AmbientAttributes.clippingColor

**L'attributo clippingColor** specifica o recupera il colore da ritagliare dalla bitmap **clippingImage.**

``` syntax
        elementID.clippingColor
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è una stringa di **lettura/scrittura.**



| Valore                                       | Descrizione                                       |
|---------------------------------------------|---------------------------------------------------|
| Auto                                        | Valore predefinito. Viene usato il colore in corrispondenza della posizione in pixel 0,0. |
| qualsiasi valore di colore Internet Explorer Microsoft | Il colore Internet Explorer specificato.    |



 

## <a name="remarks"></a>Commenti

Il colore di ritaglio indica le aree dell'oggetto **clippingImage** (o **backgroundImage** per **VIEW** o **SUBVIEW)** che corrispondono a parti trasparenti e non selezionabili del controllo. Il colore di ritaglio può indicare più aree da ritagliare. Viene generato un avviso se **clippingImage è** un file JPG per avvisare della perdita di colore nei file JPG.

**L'attributo clippingColor** non è supportato dall'elemento **PLAYLIST.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7.0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Attributi di ambiente**](ambient-attributes.md)
</dt> <dt>

[**AmbientAttributes.clippingImage**](ambientattributes-clippingimage.md)
</dt> <dt>

[**Informazioni di riferimento sul colore**](color-reference.md)
</dt> </dl>

 

 





