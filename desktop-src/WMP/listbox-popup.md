---
title: LISTBOX. popUp
description: L'attributo popUp specifica un valore che indica se l'elemento rappresenta un controllo popup o una casella di riepilogo.
ms.assetid: b0ade23a-6164-4dd4-b599-43ea1fcd44e4
keywords:
- Media Player finestre LISTBOX. popUp
topic_type:
- apiref
api_name:
- LISTBOX.popUp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43d197adbdf2ec27ea6ef7bf04c5c71d15ae923d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327730"
---
# <a name="listboxpopup"></a>LISTBOX. popUp

L'attributo **popup** specifica un valore che indica se l'elemento rappresenta un controllo popup o una casella di riepilogo.

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

L'elemento **popup** rappresenta un controllo casella di riepilogo visualizzato solo quando necessario. È identico all'elemento **ListBox** , ad eccezione del valore predefinito di questo attributo, che modifica il comportamento di visualizzazione. Per gli elementi **ListBox** , il valore predefinito è false. Per gli elementi **popup** , il valore predefinito è true. Anziché specificare questo attributo, l'elemento **ListBox** o **popup** deve essere usato in base al comportamento desiderato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------|
| Versione<br/> | Windows Media Player per Windows XP o versione successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**LISTBOX (elemento)**](listbox-element.md)
</dt> <dt>

[**Elemento POPUP**](popup-element.md)
</dt> </dl>

 

 





