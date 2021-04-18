---
title: CASELLA. replaceSelection
description: Il metodo replaceSelection sostituisce la selezione corrente con il testo specificato.
ms.assetid: 600650fb-f0c8-489a-9bf2-04f31705c6b0
keywords:
- Media Player Windows casella. replaceSelection
topic_type:
- apiref
api_name:
- EDITBOX.replaceSelection
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6546f24c864d0b466acd17d9a42616c3f8ab01b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325866"
---
# <a name="editboxreplaceselection"></a>CASELLA. replaceSelection

Il metodo **replaceSelection** sostituisce la selezione corrente con il testo specificato.

``` syntax
        elementID.replaceSelection(newValue)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="newValue"></span><span id="newvalue"></span><span id="NEWVALUE"></span>*newValue*
</dt> <dd>

**Stringa** contenente il testo in cui sostituire il testo selezionato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Se non è selezionato alcun testo, il testo di sostituzione viene inserito nella posizione corrente del punto di inserimento.

Questo metodo può essere chiamato solo dopo che il controllo diventa visibile.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------|
| Versione<br/> | Windows Media Player per Windows XP o versione successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento casella**](editbox-element.md)
</dt> <dt>

[**CASELLA. getSelectionEnd**](editbox-getselectionend.md)
</dt> <dt>

[**CASELLA. getSelectionStart**](editbox-getselectionstart.md)
</dt> <dt>

[**CASELLA. seselection**](editbox-setselection.md)
</dt> </dl>

 

 





