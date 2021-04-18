---
title: EFFECTs. currentEffect
description: L'attributo currentEffect specifica o recupera la visualizzazione corrente.
ms.assetid: d6b0e77d-2872-420a-b5f5-36fd23243648
keywords:
- EFFECTs. currentEffect Windows Media Player
topic_type:
- apiref
api_name:
- EFFECTS.currentEffect
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b19398946906fb6c6ea43234c110383b27b16ede
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325854"
---
# <a name="effectscurrenteffect"></a>EFFECTs. currentEffect

L'attributo **currentEffect** specifica o recupera la visualizzazione corrente.

``` syntax
        elementID.currentEffect
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è un **oggetto** di lettura/scrittura. Il valore predefinito è la prima visualizzazione nell'ordine di creazione. Se non è stata creata alcuna visualizzazione nell'interfaccia, il valore predefinito è la prima visualizzazione nel registro di sistema.

## <a name="remarks"></a>Commenti

È possibile usare questo oggetto per accedere a visualizzazioni personalizzate create. Ad esempio, è possibile esporre una proprietà tramite l'interfaccia **IDispatch** nella visualizzazione. È quindi possibile modificare il valore della proprietà dall'interfaccia personalizzata rendendo la visualizzazione l'effetto corrente e quindi usando l'oggetto **currentEffect** per impostare un nuovo valore per la proprietà. Se, ad esempio, la visualizzazione espone una proprietà denominata backgroundColor, il codice JScript seguente specifica un nuovo valore:


```JScript
// The EFFECTS element ID is MyEffects.
MyEffects.currentEffect.backgroundColor = "blue";
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**EFFECTs-elemento**](effects-element.md)
</dt> <dt>

[**EFFECTs. currentEffectTitle**](effects-currenteffecttitle.md)
</dt> <dt>

[**EFFECTs. currentEffectType**](effects-currenteffecttype.md)
</dt> </dl>

 

 





