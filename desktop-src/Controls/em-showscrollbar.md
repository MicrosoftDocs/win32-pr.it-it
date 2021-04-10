---
title: Messaggio di EM_SHOWSCROLLBAR (RichEdit. h)
description: Consente di visualizzare o nascondere una delle barre di scorrimento nella finestra host di un controllo Rich Edit.
ms.assetid: 0a6ec010-4870-4faf-9dc2-1da961dc8194
keywords:
- Controlli di Windows Message EM_SHOWSCROLLBAR
topic_type:
- apiref
api_name:
- EM_SHOWSCROLLBAR
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb569b194be3d744db67f98b71a595ba18a2d3a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964117"
---
# <a name="em_showscrollbar-message"></a>\_Messaggio SHOWSCROLLBAR em

Consente di visualizzare o nascondere una delle barre di scorrimento nella finestra host di un controllo Rich Edit.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Identifica la barra di scorrimento da visualizzare: orizzontale o verticale. Questo parametro deve essere **SB \_ Vert** o **SB \_ orizzontalmente**.

</dd> <dt>

*lParam* 
</dt> <dd>

Consente di specificare se visualizzare o nascondere la barra di scorrimento. Specificare **true** per visualizzare la barra di scorrimento e **false** per nasconderlo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio non restituisce alcun valore.

## <a name="remarks"></a>Commenti

Questo metodo è valido solo quando il controllo è attivo sul posto. Le chiamate effettuate mentre il controllo è inattivo potrebbero non riuscire.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**\_GETSCROLLPOS em**](em-getscrollpos.md)
</dt> <dt>

[**\_SETSCROLLPOS em**](em-setscrollpos.md)
</dt> </dl>

 

 





