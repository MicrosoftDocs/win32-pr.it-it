---
title: CASELLA. editStyle
description: L'attributo editStyle specifica o recupera lo stile del controllo casella di modifica.
ms.assetid: 1b3052c4-3087-4d41-af03-d7758680cc3b
keywords:
- Media Player Windows casella. editStyle
topic_type:
- apiref
api_name:
- EDITBOX.editStyle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 229f225dfca0ec00dd4f45a4eb63f6b2503d5df1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329936"
---
# <a name="editboxeditstyle"></a>CASELLA. editStyle

L'attributo **editStyle** specifica o recupera lo stile del controllo casella di modifica.

``` syntax
        elementID.editStyle
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è una **stringa** di lettura/scrittura contenente uno dei valori seguenti.



| Valore     | Descrizione                                                                     |
|-----------|---------------------------------------------------------------------------------|
| normale    | Valore predefinito. Visualizza il testo normale su una sola riga.                                 |
| password  | Visualizza gli asterischi ( \* ) al posto del testo. Può essere specificato solo in fase di progettazione. |
| maiuscole | Visualizza il testo come tutti i caratteri maiuscoli.                                                 |
| lettere minuscole | Visualizza il testo in caratteri minuscoli.                                                 |
| d'acquisto    | Visualizza solo numeri.                                                          |
| Multiline | Visualizza più righe di testo. Può essere specificato solo in fase di progettazione.          |



 

## <a name="remarks"></a>Commenti

Questo attributo può essere impostato solo su "password" o "Multiline" in fase di progettazione. Se è impostato su "Multiline", il valore non può essere modificato in fase di esecuzione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------|
| Versione<br/> | Windows Media Player per Windows XP o versione successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento casella**](editbox-element.md)
</dt> </dl>

 

 





