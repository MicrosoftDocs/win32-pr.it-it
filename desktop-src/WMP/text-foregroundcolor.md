---
title: TESTO. foregroundColor
description: L'attributo foregroundColor specifica o Recupera il colore del testo per il controllo di testo.
ms.assetid: 1ddbad93-fbff-4be6-9797-6594b5f09a1e
keywords:
- Media Player di Windows TEXT. foregroundColor
topic_type:
- apiref
api_name:
- TEXT.foregroundColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e452a18a085337e8cbf0ec88567d6a57a0a498a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325826"
---
# <a name="textforegroundcolor"></a>TESTO. foregroundColor

L'attributo **ForegroundColor** specifica o Recupera il colore del testo per il controllo di testo.

``` syntax
        elementID.foregroundColor
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è una **stringa** di lettura/scrittura contenente qualsiasi valore di colore di Microsoft Internet Explorer. Il valore predefinito è "Black".

Vedere l'attributo [value](text-value.md) per un esempio che illustra la modalità di utilizzo degli attributi dell'elemento di **testo** .

Quando si usa **alphaBlend** o **alphaBlendTo** con un elemento di **testo** che non ha il valore **BackgroundColor** specificato, verrà usato un colore di sfondo nero. Se anche il colore di primo piano è nero (ovvero il valore predefinito per l'attributo **ForegroundColor** ), il testo potrebbe diventare illeggibile. Per evitare questo problema, specificare sempre l'attributo **BackgroundColor** o impostare **ForegroundColor** su un colore diverso dal nero.

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

[**TESTO. backgroundColor**](text-backgroundcolor.md)
</dt> </dl>

 

 





