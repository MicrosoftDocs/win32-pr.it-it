---
title: TESTO. textWidth
description: L'attributo textWidth recupera la larghezza in pixel del testo contenuto nell'attributo value.
ms.assetid: 46c34659-f441-467c-8846-45785f7a2736
keywords:
- Media Player di Windows TEXT. textWidth
topic_type:
- apiref
api_name:
- TEXT.textWidth
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17ce93517837aecf737336137df3cf5d8bf292dd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328550"
---
# <a name="texttextwidth"></a>TESTO. textWidth

L'attributo **TextWidth** recupera la larghezza in pixel del testo contenuto nell'attributo **value** .

``` syntax
        elementID.textWidth
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è un **numero** di sola lettura (**int**).

## <a name="remarks"></a>Commenti

Il valore restituito è basato sugli attributi **fontFace**, **FontSize** e **FontStyle** , nonché sui caratteri effettivi nella stringa dell'attributo **value** .

Vedere l'attributo [value](text-value.md) per un esempio che illustra la modalità di utilizzo degli attributi dell'elemento di **testo** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento TEXT**](text-element.md)
</dt> <dt>

[**TESTO. fontFace**](text-fontface.md)
</dt> <dt>

[**TESTO. fontSize**](text-fontsize.md)
</dt> <dt>

[**TEXT. fontStyle**](text-fontstyle.md)
</dt> <dt>

[**TEXT. Value**](text-value.md)
</dt> </dl>

 

 





