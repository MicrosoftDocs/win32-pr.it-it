---
title: Messaggio PSM_SETCURSELID (Prsht. h)
description: Attiva la pagina specificata in una finestra delle proprietà in base all'identificatore di risorsa della pagina. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro PropSheet SetCurSelByID.
ms.assetid: 6db5f6ab-77ce-4a80-a84d-cb66eb1cdeaa
keywords:
- Controlli di Windows Message PSM_SETCURSELID
topic_type:
- apiref
api_name:
- PSM_SETCURSELID
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9da6ec827bbf3b9bade0af649f124d25c420d299
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120707"
---
# <a name="psm_setcurselid-message"></a>\_Messaggio SETCURSELID di PSM

Attiva la pagina specificata in una finestra delle proprietà in base all'identificatore di risorsa della pagina. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**PropSheet \_ SetCurSelByID**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setcurselbyid) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Identificatore di risorsa della pagina da attivare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.

## <a name="remarks"></a>Commenti

La finestra che sta per perdere l'attivazione riceve il codice di notifica [ \_ KILLACTIVE PSN](psn-killactive.md) e la finestra che sta ottenendo l'attivazione riceve il codice di notifica [ \_ seattivo PSN](psn-setactive.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                     |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

 





