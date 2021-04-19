---
title: TESTO. hoverFontStyle
description: L'attributo hoverFontStyle specifica o recupera lo stile del carattere utilizzato per il controllo di testo quando il cursore del mouse viene posizionato su di esso.
ms.assetid: 77ca8512-6150-4a75-8220-19de3fe9e719
keywords:
- Media Player di Windows TEXT. hoverFontStyle
topic_type:
- apiref
api_name:
- TEXT.hoverFontStyle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebaeed6d9701b6e81ac91bc5292dc5b431aa70d7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326223"
---
# <a name="texthoverfontstyle"></a>TESTO. hoverFontStyle

L'attributo **hoverFontStyle** specifica o recupera lo stile del carattere utilizzato per il controllo di testo quando il cursore del mouse viene posizionato su di esso.

``` syntax
        elementID.hoverFontStyle
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è una **stringa** di lettura/scrittura contenente uno o più dei valori seguenti.



| Valore     | Descrizione           |
|-----------|-----------------------|
| Grassetto      | Stile del carattere in grassetto.      |
| Corsivo    | Stile del carattere corsivo.    |
| Sottolineato | Stile del carattere sottolineato. |
| Barrato | Stile del carattere di attacco. |
| Normale    | Stile del carattere normale.    |



 

## <a name="remarks"></a>Commenti

È possibile utilizzare qualsiasi combinazione di valori, separati da spazi. Lo stile normale ha la priorità su tutti gli altri valori, mentre quelli specificati insieme al normale verranno ignorati.

Se **hoverFontStyle** non è specificato, viene utilizzato **FontStyle** .

Vedere l'attributo [value](text-value.md) per un esempio che illustra la modalità di utilizzo degli attributi dell'elemento di **testo** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento TEXT**](text-element.md)
</dt> <dt>

[**TEXT. fontStyle**](text-fontstyle.md)
</dt> </dl>

 

 





