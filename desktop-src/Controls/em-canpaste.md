---
title: Messaggio di EM_CANPASTE (RichEdit. h)
description: Determina se un controllo Rich Edit può incollare un formato degli Appunti specificato.
ms.assetid: 1b858ad8-1312-407b-b12a-c63668ba9f72
keywords:
- Controlli di Windows Message EM_CANPASTE
topic_type:
- apiref
api_name:
- EM_CANPASTE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aad400b610a033b6f67177da99876a892d294ec8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048525"
---
# <a name="em_canpaste-message"></a>\_Messaggio CANPASTE em

Determina se un controllo Rich Edit può incollare un formato degli Appunti specificato.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Specifica i [formati degli Appunti](/windows/desktop/dataxchg/clipboard-formats) da provare. Per provare qualsiasi formato attualmente negli Appunti, impostare questo parametro su zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene utilizzato. deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il formato degli Appunti può essere incollato, il valore restituito è un valore diverso da zero.

Se il formato degli Appunti non può essere incollato, il valore restituito è zero.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> </dl>

 

