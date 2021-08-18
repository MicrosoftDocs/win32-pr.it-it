---
title: EFFECTS.currentEffect
description: L'attributo currentEffect specifica o recupera la visualizzazione corrente.
ms.assetid: d6b0e77d-2872-420a-b5f5-36fd23243648
keywords:
- Effects.currentEffect Windows Media Player
topic_type:
- apiref
api_name:
- EFFECTS.currentEffect
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d9ac47ef88d1a0bce4982f71ce2e20e33f48933c9916bbb1e62085b5a1e5178
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996871"
---
# <a name="effectscurrenteffect"></a>EFFECTS.currentEffect

**L'attributo currentEffect** specifica o recupera la visualizzazione corrente.

``` syntax
        elementID.currentEffect
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è un oggetto di **lettura/scrittura.** Il valore predefinito è la prima visualizzazione nell'ordine di creazione. Se nell'interfaccia non sono state scritte visualizzazioni, il valore predefinito è la prima visualizzazione nel registro.

## <a name="remarks"></a>Commenti

È possibile usare questo oggetto per accedere alle visualizzazioni personalizzate create. Ad esempio, è possibile esporre una proprietà tramite **l'interfaccia IDispatch** nella visualizzazione. È quindi possibile modificare il valore della proprietà dall'interfaccia impostando la visualizzazione come effetto corrente e quindi usando l'oggetto **currentEffect** per impostare un nuovo valore per la proprietà. Ad esempio, se la visualizzazione espone una proprietà denominata backgroundColor, il codice JScript seguente specifica un nuovo valore:


```JScript
// The EFFECTS element ID is MyEffects.
MyEffects.currentEffect.backgroundColor = "blue";
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7.0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento EFFECTS**](effects-element.md)
</dt> <dt>

[**EFFECTS.currentEffectTitle**](effects-currenteffecttitle.md)
</dt> <dt>

[**EFFECTS.currentEffectType**](effects-currenteffecttype.md)
</dt> </dl>

 

 





