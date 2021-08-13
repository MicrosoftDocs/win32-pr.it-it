---
title: TEXT.foregroundColor
description: L'attributo foregroundColor specifica o recupera il colore del testo per il controllo Text.
ms.assetid: 1ddbad93-fbff-4be6-9797-6594b5f09a1e
keywords:
- Text.foregroundColor Windows Media Player
topic_type:
- apiref
api_name:
- TEXT.foregroundColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b134058fdc39b653982f752f2623c6cd69b192e24e417ac012a02813a38334a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119467071"
---
# <a name="textforegroundcolor"></a>TEXT.foregroundColor

**L'attributo foregroundColor** specifica o recupera il colore del testo per il controllo Text.

``` syntax
        elementID.foregroundColor
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è una  stringa di lettura/scrittura contenente qualsiasi valore di colore Internet Explorer Microsoft. Il valore predefinito è "black".

Vedere [l'attributo value](text-value.md) per un esempio che illustra come vengono usati gli attributi dell'elemento **TEXT.**

Quando si usa **alphaBlend** o **alphaBlendTo** con un elemento **TEXT** per cui non è specificato **backgroundColor,** verrà usato un colore di sfondo nero. Se anche il colore di primo piano è nero (che è il valore predefinito per l'attributo **foregroundColor),** il testo potrebbe diventare illeggibile. Per evitare questo problema, specificare sempre **l'attributo backgroundColor** o impostare **foregroundColor** su un colore diverso dal nero.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7.0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**AmbientAttributes.alphaBlend**](ambientattributes-alphablend.md)
</dt> <dt>

[**AmbientAttributes.alphaBlendTo**](ambientattributes-alphablendto.md)
</dt> <dt>

[**Informazioni di riferimento sul colore**](color-reference.md)
</dt> <dt>

[**Elemento TEXT**](text-element.md)
</dt> <dt>

[**TEXT.backgroundColor**](text-backgroundcolor.md)
</dt> </dl>

 

 





