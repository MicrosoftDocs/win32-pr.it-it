---
title: CASELLA. getSelectionStart
description: Il metodo getSelectionStart recupera la posizione iniziale del testo selezionato nel controllo casella.
ms.assetid: 2d7efe14-549c-4f73-96a7-b8ce88b881ad
keywords:
- Media Player Windows casella. getSelectionStart
topic_type:
- apiref
api_name:
- EDITBOX.getSelectionStart
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2508119e5b1d46d09b3531582e86caad7e7facbd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333845"
---
# <a name="editboxgetselectionstart"></a>CASELLA. getSelectionStart

Il metodo **getSelectionStart** recupera la posizione iniziale del testo selezionato nel controllo casella.

``` syntax
        elementID.getSelectionStart()
```

## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce un **numero** (**Long**).

## <a name="remarks"></a>Commenti

Se non è selezionato alcun testo, questo metodo restituisce la posizione del punto di inserimento.

Se il controllo è su più righe, questo metodo restituisce l'indice dei caratteri nel controllo, non l'indice di riga.

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

[**CASELLA. replaceSelection**](editbox-replaceselection.md)
</dt> <dt>

[**CASELLA. seselection**](editbox-setselection.md)
</dt> </dl>

 

 





