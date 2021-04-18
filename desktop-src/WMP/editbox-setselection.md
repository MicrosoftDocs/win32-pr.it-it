---
title: CASELLA. seselection
description: Il metodo di selezione Seleziona il testo nel controllo casella di modifica dall'indice iniziale specificato all'indice finale specificato.
ms.assetid: 97b20a17-4b9c-4144-b448-8d7611c0e994
keywords:
- Media Player di Windows casella. seselectation
topic_type:
- apiref
api_name:
- EDITBOX.setSelection
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9d7077de0ea59940c4afa551d22188d5583d0e4c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325865"
---
# <a name="editboxsetselection"></a>CASELLA. seselection

Il metodo di **selezione** seleziona il testo nel controllo casella di modifica dall'indice iniziale specificato all'indice finale specificato.

``` syntax
        elementID.setSelection(start, end)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="start"></span><span id="START"></span>*iniziare*
</dt> <dd>

**Numero** (**Long**) che contiene l'indice dei caratteri della posizione iniziale del testo selezionato.

</dd> <dt>

<span id="end"></span><span id="END"></span>*fine*
</dt> <dd>

**Numero** (**Long**) che contiene l'indice dei caratteri della posizione finale del testo selezionato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Se l'inizio è 0 e la fine è 1, tutto il testo nel controllo casella di modifica viene selezionato. Se l'inizio è 1, viene deselezionata la selezione corrente.

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

[**CASELLA. replaceSelection**](editbox-replaceselection.md)
</dt> </dl>

 

 





