---
title: TEXT.hoverFontStyle
description: L'attributo hoverFontStyle specifica o recupera lo stile del carattere usato per il controllo Text quando il cursore del mouse viene posizionato su di esso.
ms.assetid: 77ca8512-6150-4a75-8220-19de3fe9e719
keywords:
- Text.hoverFontStyle Windows Media Player
topic_type:
- apiref
api_name:
- TEXT.hoverFontStyle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d04f2ae8e4231ca89f37a65e591271f2536679da649d1efd22ffc1063c89d17d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134624"
---
# <a name="texthoverfontstyle"></a>TEXT.hoverFontStyle

**L'attributo hoverFontStyle** specifica o recupera lo stile del carattere usato per il controllo Text quando il cursore del mouse viene posizionato su di esso.

``` syntax
        elementID.hoverFontStyle
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

Se **hoverFontStyle non** viene specificato, **viene usato fontStyle.**

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

 

 





