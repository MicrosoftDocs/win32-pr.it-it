---
title: TEXT.disabledFontStyle
description: L'attributo disabledFontStyle specifica o recupera lo stile del carattere usato per il controllo Text quando è disabilitato.
ms.assetid: d0593fe0-f80d-44a3-b989-e85887465d8a
keywords:
- Text.disabledFontStyle Windows Media Player
topic_type:
- apiref
api_name:
- TEXT.disabledFontStyle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0119139e481eee6673c61f95425eac0a3918d738c3d18278442ba7713718b7bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119507591"
---
# <a name="textdisabledfontstyle"></a>TEXT.disabledFontStyle

**L'attributo disabledFontStyle** specifica o recupera lo stile del carattere usato per il controllo Text quando è disabilitato.

``` syntax
        elementID.disabledFontStyle
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è una stringa di **lettura/scrittura** contenente uno o più dei valori seguenti.



| Valore     | Descrizione           |
|-----------|-----------------------|
| Bold      | Stile carattere grassetto.      |
| Corsivo    | Stile del carattere corsivo.    |
| Sottolineato | Stile del carattere di sottolineatura. |
| Barrato | Stile del carattere barrato. |
| Normale    | Stile del carattere normale.    |



 

## <a name="remarks"></a>Commenti

È possibile usare qualsiasi combinazione di valori, separati da spazi. Lo stile Normale ha la priorità su tutti gli altri valori e tutti gli altri specificati insieme a Normal verranno ignorati.

Se **disabledFontStyle non** viene specificato, **viene usato fontStyle.**

Vedere [l'attributo value](text-value.md) per un esempio che illustra come vengono usati gli attributi dell'elemento **TEXT.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7.0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento TEXT**](text-element.md)
</dt> <dt>

[**TEXT.fontStyle**](text-fontstyle.md)
</dt> </dl>

 

 





