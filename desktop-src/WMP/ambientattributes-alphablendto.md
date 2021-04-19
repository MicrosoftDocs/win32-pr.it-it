---
title: AmbientAttributes.alphaBlendTo
description: Il metodo alphaBlendTo regola la proprietà alphaBlend in un determinato periodo di tempo.
ms.assetid: 5cb259bd-3010-4086-be9d-65022be297b7
keywords:
- Media Player Windows AmbientAttributes. alphaBlendTo
topic_type:
- apiref
api_name:
- AmbientAttributes.alphaBlendTo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 16b21e78de3510e2e4a58c7214995f7888f778c1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326736"
---
# <a name="ambientattributesalphablendto"></a>AmbientAttributes.alphaBlendTo

Il metodo **alphaBlendTo** regola la proprietà **alphaBlend** in un determinato periodo di tempo.

``` syntax
        elementID.alphaBlendTo(newVal, alphaTime)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="newVal"></span><span id="newval"></span><span id="NEWVAL"></span>*newVal*
</dt> <dd>

**Numero** (Long) che specifica il nuovo valore di opacità. L'intervallo è compreso tra 0 (nessuna opacità) e 255 (opacità completa).

</dd> <dt>

<span id="alphaTime"></span><span id="alphatime"></span><span id="ALPHATIME"></span>*alphaTime*
</dt> <dd>

**Numero** (**Long**) che specifica l'intervallo di tempo, in millisecondi, impiegato dall'elemento per modificare l'opacità.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questo metodo è utile per far apparire o scomparire elementi gradualmente.

Quando si usa **alphaBlendTo** con un elemento di **testo** che non ha il valore **BackgroundColor** specificato, verrà usato un colore di sfondo nero. Se il colore di primo piano è anche nero (ovvero il valore predefinito per il *testo*.**foregroundColor**), il testo potrebbe diventare illeggibile. Per evitare questo problema, specificare sempre l'attributo **BackgroundColor** o impostare **ForegroundColor** su un colore diverso dal nero.

> [!Note]  
> Questo attributo non è supportato in Windows 98.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------|
| Versione<br/> | Windows Media Player 9 serie o versione successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Attributi di ambiente**](ambient-attributes.md)
</dt> <dt>

[**AmbientAttributes. alphaBlend**](ambientattributes-alphablend.md)
</dt> <dt>

[**Elemento TEXT**](text-element.md)
</dt> <dt>

[**TESTO. backgroundColor**](text-backgroundcolor.md)
</dt> <dt>

[**TESTO. foregroundColor**](text-foregroundcolor.md)
</dt> </dl>

 

 





