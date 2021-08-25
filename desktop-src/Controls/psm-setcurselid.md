---
title: PSM_SETCURSELID messaggio (Prsht.h)
description: Attiva la pagina specificata in una finestra delle proprietà in base all'identificatore di risorsa della pagina. È possibile inviare questo messaggio in modo esplicito o tramite la \_ macro PropSheet SetCurSelByID.
ms.assetid: 6db5f6ab-77ce-4a80-a84d-cb66eb1cdeaa
keywords:
- PSM_SETCURSELID di controllo Windows messaggio
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
ms.openlocfilehash: 7be1d21b5153d480e409c6e9e7f4204746b5509b058bc292509e24ad9e03b538
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119877021"
---
# <a name="psm_setcurselid-message"></a>Messaggio \_ SETCURSELID PSM

Attiva la pagina specificata in una finestra delle proprietà in base all'identificatore di risorsa della pagina. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**\_ PropSheet SetCurSelByID.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setcurselbyid)

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

Restituisce **TRUE in** caso di esito positivo oppure FALSE **in** caso contrario.

## <a name="remarks"></a>Commenti

La finestra che perde l'attivazione riceve il codice di notifica [PSN \_ KILLACTIVE](psn-killactive.md) e la finestra che sta ricevendo l'attivazione riceve il codice di notifica [PSN \_ SETACTIVE.](psn-setactive.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                     |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |



 

 





