---
title: AmbientAttributes.alphaBlendTo
description: Il metodo alphaBlendTo regola la proprietà alphaBlend in un determinato periodo di tempo.
ms.assetid: 5cb259bd-3010-4086-be9d-65022be297b7
keywords:
- AmbientAttributes.alphaBlendTo Windows Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.alphaBlendTo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a8e0e29df897d070cd4d337e27a7f5f7f7e3a86c7f44a784afadb5bc203674ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055229"
---
# <a name="ambientattributesalphablendto"></a>AmbientAttributes.alphaBlendTo

Il **metodo alphaBlendTo** regola la **proprietà alphaBlend** in un determinato periodo di tempo.

``` syntax
        elementID.alphaBlendTo(newVal, alphaTime)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="newVal"></span><span id="newval"></span><span id="NEWVAL"></span>*newVal*
</dt> <dd>

**Numero** (long) che specifica il nuovo valore di opacità. È compreso tra 0 (nessuna opacità) e 255 (opacità completa).

</dd> <dt>

<span id="alphaTime"></span><span id="alphatime"></span><span id="ALPHATIME"></span>*alphaTime*
</dt> <dd>

**Numero** (**long**) che specifica il tempo, in millisecondi, impiegato dall'elemento per modificare l'opacità.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questo metodo è utile per visualizzare o scomparire gradualmente gli elementi.

Quando si usa **alphaBlendTo** con un **elemento TEXT** per cui non è specificato **backgroundColor,** verrà usato un colore di sfondo nero. Se anche il colore di primo piano è nero, ovvero il valore predefinito per *TEXT.***foregroundColor**), il testo potrebbe diventare illeggibile. Per evitare questo problema, specificare sempre **l'attributo backgroundColor** o impostare **foregroundColor** su un colore diverso dal nero.

> [!Note]  
> Questo attributo non è supportato in Windows 98.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------|
| Versione<br/> | Windows Media Player serie 9 o successive<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Attributi di ambiente**](ambient-attributes.md)
</dt> <dt>

[**AmbientAttributes.alphaBlend**](ambientattributes-alphablend.md)
</dt> <dt>

[**Elemento TEXT**](text-element.md)
</dt> <dt>

[**TEXT.backgroundColor**](text-backgroundcolor.md)
</dt> <dt>

[**TEXT.foregroundColor**](text-foregroundcolor.md)
</dt> </dl>

 

 





