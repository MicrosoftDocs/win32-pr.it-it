---
title: LISTBOX.fontStyle
description: L'attributo fontStyle specifica o recupera lo stile del carattere per il controllo casella di riepilogo.
ms.assetid: c42b80b6-0dea-4080-a06e-931fdc02fa55
keywords:
- LISTBOX.fontStyle Windows Media Player
topic_type:
- apiref
api_name:
- LISTBOX.fontStyle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 258064ca4ee97fc33bb98bf64d8e3dcf305c5d7e045282a5218a060e904aff50
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118575038"
---
# <a name="listboxfontstyle"></a>LISTBOX.fontStyle

**L'attributo fontStyle** specifica o recupera lo stile del carattere per il controllo casella di riepilogo.

``` syntax
        elementID.fontStyle
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è una stringa di **lettura/scrittura** contenente uno o più dei valori seguenti.



| Valore     | Descrizione           |
|-----------|-----------------------|
| Bold      | Stile carattere grassetto.      |
| Corsivo    | Stile del carattere corsivo.    |
| Sottolineato | Stile del carattere di sottolineatura. |
| Barrato | Stile carattere barrato. |
| Normale    | Stile del carattere normale.    |



 

## <a name="remarks"></a>Commenti

È possibile usare qualsiasi combinazione di valori, separati da spazi. Lo stile Normale ha la priorità su tutti gli altri valori e tutti gli altri specificati insieme a Normal verranno ignorati.

Ai fini del rendering, Normal è lo stile del carattere predefinito. Il valore predefinito recuperato da questo attributo è "" (stringa vuota).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------|
| Versione<br/> | Windows Media Player per Windows XP o versioni successive<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento LISTBOX**](listbox-element.md)
</dt> <dt>

[**LISTBOX.fontSize**](listbox-fontsize.md)
</dt> </dl>

 

 





