---
title: Messaggio PGM_GETBUTTONSIZE (COMmctrl. h)
description: Recupera le dimensioni correnti del pulsante per il controllo pager. È possibile inviare questo messaggio in modo esplicito o utilizzare la \_ macro GetButtonSize del cercapersone.
ms.assetid: fa8b4814-4587-4149-83a7-84faad2a4641
keywords:
- Controlli di Windows Message PGM_GETBUTTONSIZE
topic_type:
- apiref
api_name:
- PGM_GETBUTTONSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae5cb36d203aaeae748db9adb1b13cacf2e40f5e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048553"
---
# <a name="pgm_getbuttonsize-message"></a>\_Messaggio GETBUTTONSIZE PGM

Recupera le dimensioni correnti del pulsante per il controllo pager. È possibile inviare questo messaggio in modo esplicito o utilizzare la macro [**\_ GetButtonSize del cercapersone**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getbuttonsize) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore INT che contiene la dimensione corrente del pulsante, in pixel.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_SETBUTTONSIZE PGM**](pgm-setbuttonsize.md)
</dt> </dl>

 

 





