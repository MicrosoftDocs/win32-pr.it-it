---
title: TEXT.textWidth
description: L'attributo textWidth recupera la larghezza in pixel del testo contenuto nell'attributo value.
ms.assetid: 46c34659-f441-467c-8846-45785f7a2736
keywords:
- Text.textWidth Windows Media Player
topic_type:
- apiref
api_name:
- TEXT.textWidth
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb7ad69f332c746ead674e9cb0a2593379b01ac3dba388ebee90d710312eb65f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117932573"
---
# <a name="texttextwidth"></a>TEXT.textWidth

**L'attributo textWidth** recupera la larghezza in pixel del testo contenuto nell'attributo **value.**

``` syntax
        elementID.textWidth
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è un numero di sola **lettura** (**int**).

## <a name="remarks"></a>Commenti

Il valore restituito si basa sugli attributi **fontFace,** **fontSize** e **fontStyle,** nonché sui caratteri effettivi nella stringa **dell'attributo** value.

Vedere [l'attributo value](text-value.md) per un esempio che illustra come vengono usati gli attributi dell'elemento **TEXT.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7.0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento TEXT**](text-element.md)
</dt> <dt>

[**TEXT.fontFace**](text-fontface.md)
</dt> <dt>

[**TEXT.fontSize**](text-fontsize.md)
</dt> <dt>

[**TEXT.fontStyle**](text-fontstyle.md)
</dt> <dt>

[**TEXT.value**](text-value.md)
</dt> </dl>

 

 





