---
title: Messaggio CB_SETEXTENDEDUI (winuser. h)
description: Un'applicazione invia un \_ messaggio CB SETEXTENDEDUI per selezionare l'interfaccia utente predefinita o l'interfaccia utente estesa per una casella combinata con l' \_ elenco a discesa CBS o \_ lo stile DropDownList CBS.
ms.assetid: c489e484-777e-4afa-996b-1ec3eb6552ab
keywords:
- Controlli di Windows Message CB_SETEXTENDEDUI
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
ms.openlocfilehash: f94c31c8bc5457799d0038ecd8340c03c55aed91
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476636"
---
# <a name="cb_setextendedui-message"></a>\_Messaggio SETEXTENDEDUI CB

Un'applicazione invia un messaggio **CB \_ SETEXTENDEDUI** per selezionare l'interfaccia utente predefinita o l'interfaccia utente estesa per una casella combinata con l' [**elenco a \_ discesa CBS**](combo-box-styles.md) o lo stile [**\_ DropDownList CBS**](combo-box-styles.md) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

**Bool** che specifica se la casella combinata utilizza l'interfaccia utente estesa (**true**) o l'interfaccia utente predefinita (**false**).

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se l'operazione ha esito positivo, il valore restituito è CB \_ OK. Se si verifica un errore, è CB \_ Err.

## <a name="remarks"></a>Commenti

Per impostazione predefinita, il tasto F4 apre o chiude l'elenco e la freccia in giù modifica la selezione corrente. Nell'interfaccia utente estesa il tasto F4 è disabilitato e il tasto freccia giù apre l'elenco a discesa. La rotellina del mouse, che in genere scorre gli elementi nell'elenco, non ha alcun effetto quando viene impostata l'interfaccia utente estesa.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



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

 

 





