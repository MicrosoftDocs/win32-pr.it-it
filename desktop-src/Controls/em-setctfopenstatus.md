---
title: Messaggio di EM_SETCTFOPENSTATUS (RichEdit. h)
description: Apre o chiude la tastiera di Text Services Framework (TSF).
ms.assetid: 9bdabf5a-93db-4b0e-9528-807d262de866
keywords:
- Controlli di Windows Message EM_SETCTFOPENSTATUS
topic_type:
- apiref
api_name:
- EM_SETCTFOPENSTATUS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf4163a415f129dfc5d3f98aa06578d13bb462e5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048655"
---
# <a name="em_setctfopenstatus-message"></a>\_Messaggio SETCTFOPENSTATUS em

Apre o chiude la tastiera di Text Services Framework (TSF).

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Per attivare la tastiera TSF, utilizzare **true**. Per disattivare la tastiera TSF, utilizzare **false**.

</dd> <dt>

*lParam* 
</dt> <dd>

Non utilizzato; deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

In caso di esito positivo, il messaggio restituisce **true**. Se ha esito negativo, il messaggio restituisce **false**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP con SP1 \[\]<br/>                                  |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_GETCTFOPENSTATUS em**](em-getctfopenstatus.md)
</dt> </dl>

 

 





