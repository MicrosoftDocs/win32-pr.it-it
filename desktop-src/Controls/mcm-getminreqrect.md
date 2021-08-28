---
title: MCM_GETMINREQRECT messaggio (Commctrl.h)
description: Recupera le dimensioni minime necessarie per visualizzare un mese completo in un controllo calendario mensile. È possibile inviare questo messaggio in modo esplicito o tramite la \_ macro MonthCal GetMinReqRect.
ms.assetid: f0378338-4809-48e9-9387-ed8b79356f95
keywords:
- MCM_GETMINREQRECT dei messaggi Windows controlli
topic_type:
- apiref
api_name:
- MCM_GETMINREQRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 575636837b1485de62dd5e603a0dea38455c4c99926c13f3bd05101fe2a27eca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062051"
---
# <a name="mcm_getminreqrect-message"></a>Messaggio \_ MCM GETMINREQRECT

Recupera le dimensioni minime necessarie per visualizzare un mese completo in un controllo calendario mensile. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**\_ MonthCal GetMinReqRect.**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getminreqrect)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una [**struttura RECT**](/previous-versions//dd162897(v=vs.85)) che riceverà informazioni sul rettangolo di delimitazione. Questo parametro deve essere un indirizzo valido e non può essere **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore diverso da zero e *lParam riceve* le informazioni di delimitazione applicabili in caso di esito positivo. In caso contrario, il messaggio restituisce zero.

## <a name="remarks"></a>Commenti

Le dimensioni minime della finestra necessarie per un controllo calendario mensile dipendono dal tipo di carattere, dagli stili di controllo, dalle metriche di sistema e dalle impostazioni internazionali attualmente selezionate. Quando un'applicazione modifica qualsiasi elemento che influisce sulle dimensioni minime della finestra o elabora un messaggio [**WM \_ SETTINGCHANGE,**](/windows/desktop/winmsg/wm-settingchange) deve inviare **MCM \_ GETMINREQRECT** per determinare le nuove dimensioni minime.

> [!Note]  
> Il rettangolo restituito **da MCM \_ GETMINREQRECT** non include la larghezza della stringa "Today", se presente. Se lo [**stile MCS \_ NOTODAY**](month-calendar-control-styles.md) non è impostato, l'applicazione deve recuperare anche il rettangolo che definisce la larghezza della stringa "Today" inviando un messaggio [**MCM \_ GETMAXTODAYWIDTH.**](mcm-getmaxtodaywidth.md) Usare il più grande dei due rettangoli per assicurarsi che la stringa "Oggi" non sia ritagliata.

 

I **membri superiore** **e** sinistro della struttura a cui punta *lParam* saranno sempre zero. I **membri** destro **e inferiore** rappresentano il valore minimo *cx* *e cy* richiesto per il controllo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

