---
title: CB_SETEXTENDEDUI messaggio (Winuser.h)
description: Un'applicazione invia un messaggio CB SETEXTENDEDUI per selezionare l'interfaccia utente predefinita o l'interfaccia utente estesa per una casella combinata con lo stile CBS DROPDOWN o \_ \_ CBS \_ DROPDOWNLIST.
ms.assetid: c489e484-777e-4afa-996b-1ec3eb6552ab
keywords:
- CB_SETEXTENDEDUI di controllo Windows messaggio
topic_type:
- apiref
api_name:
- CB_SETEXTENDEDUI
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36b77e67e555628475b9e40e78b7b0391d0b631fd77e6ff7f549700a553fa507
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118414223"
---
# <a name="cb_setextendedui-message"></a>Messaggio CB \_ SETEXTENDEDUI

Un'applicazione invia un **messaggio CB \_ SETEXTENDEDUI** per selezionare l'interfaccia utente predefinita o l'interfaccia utente estesa per una casella combinata con lo stile [**CBS \_ DROPDOWN**](combo-box-styles.md) o [**CBS \_ DROPDOWNLIST.**](combo-box-styles.md)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

VALORE **BOOL che** specifica se la casella combinata usa l'interfaccia utente estesa (**TRUE**) o l'interfaccia utente predefinita (**FALSE**).

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se l'operazione ha esito positivo, il valore restituito è CB \_ OK. Se si verifica un errore, si tratta di CB \_ ERR.

## <a name="remarks"></a>Commenti

Per impostazione predefinita, il tasto F4 apre o chiude l'elenco e la freccia GIÙ modifica la selezione corrente. Nell'interfaccia utente estesa il tasto F4 è disabilitato e il tasto FRECCIA GIÙ apre l'elenco a discesa. La rotellina del mouse, che in genere scorre gli elementi nell'elenco, non ha alcun effetto quando viene impostata l'interfaccia utente estesa.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                                           |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**CB \_ GETEXTENDEDUI**](cb-getextendedui.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Funzionalità della casella combinata](combo-box-features.md)
</dt> </dl>

 

 





