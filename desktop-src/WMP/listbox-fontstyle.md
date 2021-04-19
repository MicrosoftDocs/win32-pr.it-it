---
title: LISTBOX. fontStyle
description: L'attributo fontStyle specifica o recupera lo stile del carattere per il controllo casella di riepilogo.
ms.assetid: c42b80b6-0dea-4080-a06e-931fdc02fa55
keywords:
- Media Player di Windows LISTBOX. fontStyle
topic_type:
- apiref
api_name:
- LISTBOX.fontStyle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0903ac77f1fa4307dfcabad6311eb556617d8153
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327745"
---
# <a name="listboxfontstyle"></a>LISTBOX. fontStyle

L'attributo **FontStyle** specifica o recupera lo stile del carattere per il controllo casella di riepilogo.

``` syntax
        elementID.fontStyle
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

A scopo di rendering, Normal è lo stile del tipo di carattere predefinito. Il valore predefinito recuperato da questo attributo è "" (stringa vuota).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------|
| Versione<br/> | Windows Media Player per Windows XP o versione successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**LISTBOX (elemento)**](listbox-element.md)
</dt> <dt>

[**LISTBOX. fontSize**](listbox-fontsize.md)
</dt> </dl>

 

 





