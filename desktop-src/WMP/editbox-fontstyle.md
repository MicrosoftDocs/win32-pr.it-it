---
title: EDITBOX.fontStyle
description: L'attributo fontStyle specifica o recupera lo stile del carattere per il controllo casella di modifica.
ms.assetid: bc71359d-2b75-4134-99e8-52b2ca48dcde
keywords:
- EditBOX.fontStyle Windows Media Player
topic_type:
- apiref
api_name:
- EDITBOX.fontStyle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65d9dc5ac5fe3750fb3a6af8658a5ddb30274764cc891438162434a44651322a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118578847"
---
# <a name="editboxfontstyle"></a>EDITBOX.fontStyle

**L'attributo fontStyle** specifica o recupera lo stile del carattere per il controllo casella di modifica.

``` syntax
        elementID.fontStyle
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è una stringa di **lettura/scrittura** contenente uno o più dei valori seguenti.



| Valore     | Descrizione           |
|-----------|-----------------------|
| Bold      | Stile carattere grassetto.      |
| Corsivo    | Stile del carattere corsivo.    |
| Sottolineato | Stile del carattere Di sottolineatura. |
| Barrato | Stile carattere barrato. |
| Normale    | Stile del carattere normale.    |



 

## <a name="remarks"></a>Commenti

È possibile usare qualsiasi combinazione di valori, separati da spazi. Lo stile Normale ha la priorità su tutti gli altri valori e tutti gli altri specificati insieme a Normale verranno ignorati.

Ai fini del rendering, Normal è lo stile del carattere predefinito. Il valore predefinito recuperato da questo attributo è "" (stringa vuota).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------|
| Versione<br/> | Windows Media Player per Windows XP o versioni successive<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento EDITBOX**](editbox-element.md)
</dt> <dt>

[**EDITBOX.fontFace**](editbox-fontface.md)
</dt> <dt>

[**EDITBOX.fontSize**](editbox-fontsize.md)
</dt> </dl>

 

 





