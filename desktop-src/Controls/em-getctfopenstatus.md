---
title: EM_GETCTFOPENSTATUS messaggio (Richedit.h)
description: Determina se la Framework servizi di testo (TSF) è aperta o chiusa.
ms.assetid: a50fedf4-b4e5-4b99-be46-1bbbf08e85a8
keywords:
- EM_GETCTFOPENSTATUS dei controlli Windows messaggio
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
ms.openlocfilehash: ef55fe0944ad3632f8bfec11894c5613efde02dc1ec16f8c0d31105f6b19ea8e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019739"
---
# <a name="em_getctfopenstatus-message"></a>Messaggio \_ EM GETCTFOPENSTATUS

Determina se la Framework servizi di testo (TSF) è aperta o chiusa.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Non usato; deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Non usato; deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la tastiera TSF è aperta, il valore restituito è **TRUE.** In caso contrario, è **FALSE.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP solo con \[ app desktop SP1\]<br/>                                  |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**EM \_ SETCTFOPENSTATUS**](em-setctfopenstatus.md)
</dt> </dl>

 

 





