---
title: EDITBOX.editStyle
description: L'attributo editStyle specifica o recupera lo stile del controllo casella di modifica.
ms.assetid: 1b3052c4-3087-4d41-af03-d7758680cc3b
keywords:
- EditBOX.editStyle Windows Media Player
topic_type:
- apiref
api_name:
- EDITBOX.editStyle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4d40d1933c68c4e34707f01a4d425045c773297e8567ba8ea13a88c6fbc57c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117749462"
---
# <a name="editboxeditstyle"></a>EDITBOX.editStyle

**L'attributo editStyle** specifica o recupera lo stile del controllo casella di modifica.

``` syntax
        elementID.editStyle
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è una stringa di **lettura/scrittura** contenente uno dei valori seguenti.



| Valore     | Descrizione                                                                     |
|-----------|---------------------------------------------------------------------------------|
| normale    | Valore predefinito. Visualizza il testo normale su una singola riga.                                 |
| password  | Visualizza gli asterischi ( \* ) al posto del testo. Può essere specificato solo in fase di progettazione. |
| maiuscole | Visualizza il testo in maiuscolo.                                                 |
| lettere minuscole | Visualizza il testo in lettere minuscole.                                                 |
| d'acquisto    | Visualizza solo numeri.                                                          |
| Multilinea | Visualizza più righe di testo. Può essere specificato solo in fase di progettazione.          |



 

## <a name="remarks"></a>Commenti

Questo attributo può essere impostato solo su "password" o "multilinea" in fase di progettazione. Se è impostato su "multiline", il valore non può essere modificato in fase di esecuzione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------|
| Versione<br/> | Windows Media Player per Windows XP o versioni successive<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento EDITBOX**](editbox-element.md)
</dt> </dl>

 

 





