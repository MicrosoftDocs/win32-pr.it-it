---
description: L'elemento Effect definisce un oggetto effetto audio o video. Un effetto viene applicato a un singolo flusso, ad esempio una composizione, una traccia o un'origine.
ms.assetid: aedb4491-f1f0-44b3-ad88-3fac8c90144d
title: Elemento Effect (Gdipluseffects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9dd31e85407b99c3dffd4417a051be168f7c6d3a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332050"
---
# <a name="effect-element"></a>Elemento Effect

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

L' `effect` elemento definisce un oggetto effetto audio o video. Un effetto viene applicato a un singolo flusso, ad esempio una composizione, una traccia o un'origine.

## <a name="attributes"></a>Attributi

[**CLSID**](clsid-attribute.md), [**Lock**](lock-attribute.md), [**mute**](mute-attribute.md), [**Start**](start-attribute.md), [**Stop**](stop-attribute.md), [**UserData**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md)

## <a name="parentchild-information"></a>Informazioni padre/figlio



|          |                                                                                                                                      |
|----------|--------------------------------------------------------------------------------------------------------------------------------------|
| Padre   | [**composito**](composite-element.md), [**gruppo**](group-element.md), [**clip**](clip-element.md), [**traccia**](track-element.md) |
| Children | [**param**](param-element.md)                                                                                                       |



 

## <a name="remarks"></a>Commenti

L'attributo **CLSID** specifica l'oggetto SubObject che crea l'effetto.

## <a name="examples"></a>Esempio


```XML
<effect clsid="{b05a941c-3ce1-11d2-952a-00c04fa34f05}" start="0" stop="32.0" />
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Gdipluseffects. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elementi XTL](xtl-elements.md)
</dt> </dl>

 

 




