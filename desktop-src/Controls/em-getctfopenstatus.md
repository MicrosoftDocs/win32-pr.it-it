---
title: Messaggio di EM_GETCTFOPENSTATUS (RichEdit. h)
description: Determina se la tastiera di Text Services Framework (TSF) è aperta o chiusa.
ms.assetid: a50fedf4-b4e5-4b99-be46-1bbbf08e85a8
keywords:
- Controlli di Windows Message EM_GETCTFOPENSTATUS
topic_type:
- apiref
api_name:
- EM_GETCTFOPENSTATUS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ce1bbf09af6c61a33c33c4172ff699fa5bd26f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964333"
---
# <a name="em_getctfopenstatus-message"></a>\_Messaggio GETCTFOPENSTATUS em

Determina se la tastiera di Text Services Framework (TSF) è aperta o chiusa.

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

Se la tastiera TSF è aperta, il valore restituito è **true**. In caso contrario, è **false**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP con SP1 \[\]<br/>                                  |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_SETCTFOPENSTATUS em**](em-setctfopenstatus.md)
</dt> </dl>

 

 





