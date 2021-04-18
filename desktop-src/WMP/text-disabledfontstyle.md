---
title: TESTO. disabledFontStyle
description: L'attributo disabledFontStyle specifica o recupera lo stile del carattere utilizzato per il controllo di testo quando è disabilitato.
ms.assetid: d0593fe0-f80d-44a3-b989-e85887465d8a
keywords:
- Media Player di Windows TEXT. disabledFontStyle
topic_type:
- apiref
api_name:
- TEXT.disabledFontStyle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 563ab039a5eae00324f3a810c7d32f08729629b3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329596"
---
# <a name="textdisabledfontstyle"></a>TESTO. disabledFontStyle

L'attributo **disabledFontStyle** specifica o recupera lo stile del carattere utilizzato per il controllo di testo quando è disabilitato.

``` syntax
        elementID.disabledFontStyle
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

Se **disabledFontStyle** non è specificato, viene utilizzato **FontStyle** .

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

 

 





