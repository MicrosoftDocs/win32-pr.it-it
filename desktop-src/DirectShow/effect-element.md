---
description: L'elemento effect definisce un oggetto effetto audio o video. Un effetto viene applicato a un singolo flusso, ad esempio una composizione, una traccia o un'origine.
ms.assetid: aedb4491-f1f0-44b3-ad88-3fac8c90144d
title: Elemento effect (Gdipluseffects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4c925e61578857415bb22248a9ad2b1df27cdac
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908659"
---
# <a name="effect-element"></a>Elemento effect

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future di Windows.\]

 

`effect`L'elemento definisce un oggetto effetto audio o video. Un effetto viene applicato a un singolo flusso, ad esempio una composizione, una traccia o un'origine.

## <a name="attributes"></a>Attributi

[**clsid**](clsid-attribute.md), [**lock**](lock-attribute.md), [**mute**](mute-attribute.md), [**start**](start-attribute.md), [**stop**](stop-attribute.md), [**userdata**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md)

## <a name="parentchild-information"></a>Informazioni padre/figlio



| Label | Valore |
|----------|--------------------------------------------------------------------------------------------------------------------------------------|
| Padre   | [**composite,**](composite-element.md) [**group,**](group-element.md) [**clip,**](clip-element.md) [**track**](track-element.md) |
| Children | [**Param**](param-element.md)                                                                                                       |



 

## <a name="remarks"></a>Commenti

**L'attributo clsid** specifica il sottooggetto che crea l'effetto.

## <a name="examples"></a>Esempio


```XML
<effect clsid="{b05a941c-3ce1-11d2-952a-00c04fa34f05}" start="0" stop="32.0" />
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Gdipluseffects.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elementi XTL](xtl-elements.md)
</dt> </dl>

 

 




