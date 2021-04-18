---
title: TESTO. backgroundColor
description: L'attributo backgroundColor specifica o Recupera il colore di sfondo per il controllo di testo.
ms.assetid: 0c16318f-bf57-4c5f-85c1-46641124d431
keywords:
- Media Player di Windows TEXT. backgroundColor
topic_type:
- apiref
api_name:
- TEXT.backgroundColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bff833fad0b5ad60b49479c57dc51cbe82f48dbd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325572"
---
# <a name="textbackgroundcolor"></a>TESTO. backgroundColor

L'attributo **BackgroundColor** specifica o Recupera il colore di sfondo per il controllo di testo.

``` syntax
        elementID.backgroundColor
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è una **stringa** di lettura/scrittura contenente qualsiasi valore di colore di Microsoft Internet Explorer oppure il valore "None". Il valore predefinito è "None", che indica che lo sfondo è trasparente.

## <a name="remarks"></a>Commenti

Il colore di sfondo è impostato per l'altezza e la larghezza del controllo. Se l'altezza e la larghezza non sono impostate, il colore di sfondo viene impostato sull'altezza e sulla larghezza del testo.

Quando si usa **alphaBlend** o **alphaBlendTo** con un elemento di **testo** che non ha il valore **BackgroundColor** specificato, verrà usato un colore di sfondo nero. Se anche il colore di primo piano è nero (ovvero il valore predefinito per l'attributo **ForegroundColor** ), il testo potrebbe diventare illeggibile. Per evitare questo problema, specificare sempre l'attributo **BackgroundColor** o impostare **ForegroundColor** su un colore diverso dal nero.

Vedere l'attributo [value](text-value.md) per un esempio che illustra la modalità di utilizzo degli attributi dell'elemento di **testo** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**AmbientAttributes. alphaBlend**](ambientattributes-alphablend.md)
</dt> <dt>

[**AmbientAttributes.alphaBlendTo**](ambientattributes-alphablendto.md)
</dt> <dt>

[**Riferimento ai colori**](color-reference.md)
</dt> <dt>

[**Elemento TEXT**](text-element.md)
</dt> <dt>

[**TESTO. foregroundColor**](text-foregroundcolor.md)
</dt> </dl>

 

 





