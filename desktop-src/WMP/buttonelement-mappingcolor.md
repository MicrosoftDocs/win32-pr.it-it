---
title: BUTTONelement. mappingColor
description: L'attributo mappingColor specifica o recupera la chiave di colore che identifica questo BUTTONelement in BUTTONGROUP.
ms.assetid: e7b1663c-3263-41d5-9a69-4cf1dcf0fc1f
keywords:
- BUTTONelement. mappingColor Windows Media Player
topic_type:
- apiref
api_name:
- BUTTONELEMENT.mappingColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7318f01246578fe8ff34118427c95afb7b3bb098
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325002"
---
# <a name="buttonelementmappingcolor"></a>BUTTONelement. mappingColor

L'attributo **mappingColor** specifica o recupera la chiave di colore che identifica questo **ButtonElement** in **ButtonGroup**.

``` syntax
        elementID.mappingColor
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è una **stringa** di lettura/scrittura contenente qualsiasi valore di colore di Microsoft Internet Explorer. e non prevede alcun valore predefinito.

## <a name="remarks"></a>Commenti

Questo attributo specifica il colore dell'area nel gruppo di pulsanti **mappingImage** che corrisponde a questo elemento Button. Tutti i clic su questa area vengono gestiti da questo elemento Button.

Se viene specificato un colore non valido, il **pulsante** non viene attivato.

## <a name="examples"></a>Esempio

L'esempio seguente è un file di definizione dell'interfaccia completa che illustra come vengono usati alcuni degli attributi **ButtonElement** . Si trova nella directory degli esempi installata con l'SDK.


```
<THEME>
  <VIEW
    backgroundImage = "background.bmp"
    titleBar = "False"
  >
    <PLAYER
      URL = "https://proseware.com/mellow.wma"
    />
    <EFFECTS
      id = "myeffects"
      top = "25"
      left = "88"
      width = "180"
      height = "150"
    />
    <BUTTONGROUP
      mappingImage = "map.bmp"
      hoverImage = "hover.bmp"
    >
      <BUTTONELEMENT
        mappingColor = "#00FF00"
        upToolTip = "Next"
        onClick = "JScript:myeffects.next();"
      />
      <BUTTONELEMENT
        mappingColor = "#FF0000"
        upToolTip = "Previous"
        onClick = "JScript:myeffects.previous();"
      />
    </BUTTONGROUP>
  </VIEW>
</THEME>

```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Riferimento ai colori**](color-reference.md)
</dt> <dt>

[**BUTTONelement (elemento)**](buttonelement-element.md)
</dt> <dt>

[**BUTTONGROUP. mappingImage**](buttongroup-mappingimage.md)
</dt> </dl>

 

 





