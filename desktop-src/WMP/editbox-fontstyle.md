---
title: CASELLA. fontStyle
description: L'attributo fontStyle specifica o recupera lo stile del carattere per il controllo casella di modifica.
ms.assetid: bc71359d-2b75-4134-99e8-52b2ca48dcde
keywords:
- Media Player Windows casella. fontStyle
topic_type:
- apiref
api_name:
- EDITBOX.fontStyle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4249f6224099c3d2a36a3b26244c9b804be519c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324745"
---
# <a name="editboxfontstyle"></a>CASELLA. fontStyle

L'attributo **FontStyle** specifica o recupera lo stile del carattere per il controllo casella di modifica.

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

[**Elemento casella**](editbox-element.md)
</dt> <dt>

[**CASELLA. fontFace**](editbox-fontface.md)
</dt> <dt>

[**CASELLA. fontSize**](editbox-fontsize.md)
</dt> </dl>

 

 





