---
title: EDITBOX.getSelectionStart
description: Il metodo getSelectionStart recupera la posizione iniziale del testo selezionato nel controllo casella di modifica.
ms.assetid: 2d7efe14-549c-4f73-96a7-b8ce88b881ad
keywords:
- EDITBOX.getSelectionStart Windows Media Player
topic_type:
- apiref
api_name:
- EDITBOX.getSelectionStart
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7c555cc7231440e15275dcd44a2508f1d8cc5ba53a8137db861cc71b61528ac3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118340032"
---
# <a name="editboxgetselectionstart"></a>EDITBOX.getSelectionStart

Il **metodo getSelectionStart** recupera la posizione iniziale del testo selezionato nel controllo casella di modifica.

``` syntax
        elementID.getSelectionStart()
```

## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce un **valore Number** (**long**).

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

[**Elemento EDITBOX**](editbox-element.md)
</dt> <dt>

[**EDITBOX.getSelectionEnd**](editbox-getselectionend.md)
</dt> <dt>

[**EDITBOX.replaceSelection**](editbox-replaceselection.md)
</dt> <dt>

[**EDITBOX.setSelection**](editbox-setselection.md)
</dt> </dl>

 

 





