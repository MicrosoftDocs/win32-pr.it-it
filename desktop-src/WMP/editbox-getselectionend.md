---
title: CASELLA. getSelectionEnd
description: Il metodo getSelectionEnd recupera la posizione finale del testo selezionato nel controllo casella.
ms.assetid: 82a445da-3c50-41b7-8ac8-da6c860056ba
keywords:
- Media Player Windows casella. getSelectionEnd
topic_type:
- apiref
api_name:
- EDITBOX.getSelectionEnd
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f27c2974360e7e77becfa67a27b4e96b529ad1e5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333849"
---
# <a name="editboxgetselectionend"></a>CASELLA. getSelectionEnd

Il metodo **getSelectionEnd** recupera la posizione finale del testo selezionato nel controllo casella.

``` syntax
        elementID.getSelectionEnd()
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

[**CASELLA. getSelectionStart**](editbox-getselectionstart.md)
</dt> <dt>

[**CASELLA. replaceSelection**](editbox-replaceselection.md)
</dt> <dt>

[**CASELLA. seselection**](editbox-setselection.md)
</dt> </dl>

 

 





