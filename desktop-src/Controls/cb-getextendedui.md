---
title: Messaggio CB_GETEXTENDEDUI (winuser. h)
description: Determina se una casella combinata dispone dell'interfaccia utente predefinita o dell'interfaccia utente estesa.
ms.assetid: 4f5580e0-68b1-4584-bf79-561fb8222fe0
keywords:
- Controlli di Windows Message CB_GETEXTENDEDUI
topic_type:
- apiref
api_name:
- CB_GETEXTENDEDUI
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94d90550bf341fc8586174c7ec57eb77fad08c59
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476655"
---
# <a name="cb_getextendedui-message"></a>\_Messaggio GETEXTENDEDUI CB

Determina se una casella combinata dispone dell'interfaccia utente predefinita o dell'interfaccia utente estesa.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Non utilizzato; deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Non utilizzato; deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la casella combinata dispone dell'interfaccia utente estesa, il valore restituito è **true**; in caso contrario, è **false**.

## <a name="remarks"></a>Commenti

Per impostazione predefinita, il tasto F4 apre o chiude l'elenco e la freccia in giù modifica la selezione corrente. In una casella combinata con l'interfaccia utente estesa, il tasto F4 è disabilitato e premendo il tasto freccia giù si apre l'elenco a discesa.

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

[**CB \_ SETEXTENDEDUI**](cb-setextendedui.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Funzionalità della casella combinata](combo-box-features.md)
</dt> </dl>

 

 





