---
title: LISTBOX.popUp
description: L'attributo popUp specifica un valore che indica se l'elemento rappresenta un controllo popup o casella di riepilogo.
ms.assetid: b0ade23a-6164-4dd4-b599-43ea1fcd44e4
keywords:
- LISTBOX.popUp Windows Media Player
topic_type:
- apiref
api_name:
- LISTBOX.popUp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a755a4fc8f5e1451ee118f718a9b6618e75875789faef7318164f7f2add2069
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996441"
---
# <a name="listboxpopup"></a>LISTBOX.popUp

**L'attributo popUp** specifica un valore che indica se l'elemento rappresenta un controllo popup o casella di riepilogo.

``` syntax
<ELEMENT popUp="value">
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è un **valore booleano** specificato solo in fase di progettazione.



| Valore | Descrizione                                |
|-------|--------------------------------------------|
| true  | L'elemento rappresenta un controllo popup.    |
| false | L'elemento rappresenta un controllo casella di riepilogo. |



 

## <a name="remarks"></a>Commenti

**L'elemento POPUP** rappresenta un controllo casella di riepilogo che viene visualizzato solo quando necessario. È identico **all'elemento LISTBOX,** ad eccezione del valore predefinito di questo attributo, che modifica il comportamento di visualizzazione. Per **gli elementi LISTBOX,** il valore predefinito è false. Per **gli elementi POPUP,** il valore predefinito è true. Anziché specificare questo attributo, **l'elemento LISTBOX** o **POPUP** deve essere usato in base al comportamento desiderato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------|
| Versione<br/> | Windows Media Player per Windows XP o versione successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento LISTBOX**](listbox-element.md)
</dt> <dt>

[**Elemento POPUP**](popup-element.md)
</dt> </dl>

 

 





