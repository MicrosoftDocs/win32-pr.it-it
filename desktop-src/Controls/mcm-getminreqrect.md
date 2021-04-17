---
title: Messaggio MCM_GETMINREQRECT (COMmctrl. h)
description: Recupera le dimensioni minime necessarie per visualizzare un mese intero in un controllo di calendario mensile. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro MonthCal GetMinReqRect.
ms.assetid: f0378338-4809-48e9-9387-ed8b79356f95
keywords:
- Controlli di Windows Message MCM_GETMINREQRECT
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
ms.openlocfilehash: ac6b2e2b16a70841836a277ffe55e030a6d6a241
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476072"
---
# <a name="mcm_getminreqrect-message"></a>\_Messaggio GETMINREQRECT MCM

Recupera le dimensioni minime necessarie per visualizzare un mese intero in un controllo di calendario mensile. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**MonthCal \_ GetMinReqRect**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getminreqrect) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**Rect**](/previous-versions//dd162897(v=vs.85)) che riceverà informazioni sul rettangolo di delimitazione. Questo parametro deve essere un indirizzo valido e non può essere **null**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore diverso da zero e *lParam* riceve le informazioni di delimitazione applicabili in caso di esito positivo. In caso contrario, il messaggio restituisce zero.

## <a name="remarks"></a>Commenti

Le dimensioni minime della finestra richiesta per un controllo di calendario mensile dipendono dal tipo di carattere correntemente selezionato, dagli stili dei controlli, dalle metriche di sistema e dalle impostazioni internazionali. Quando un'applicazione modifica qualsiasi elemento che influisca sulle dimensioni minime della finestra o elabora un messaggio [**WM \_ SETTINGCHANGE**](/windows/desktop/winmsg/wm-settingchange) , deve inviare **MCM \_ GETMINREQRECT** per determinare le nuove dimensioni minime.

> [!Note]  
> Il rettangolo restituito da **MCM \_ GETMINREQRECT** non include la larghezza della stringa "Today", se presente. Se lo [**stile \_ notoday MCS**](month-calendar-control-styles.md) non è impostato, l'applicazione deve recuperare anche il rettangolo che definisce la larghezza della stringa "Today" inviando un messaggio [**MCM \_ GETMAXTODAYWIDTH**](mcm-getmaxtodaywidth.md) . Usare il più grande dei due rettangoli per assicurarsi che la stringa "Today" non venga troncata.

 

I membri **superiore** e **sinistro** della struttura a cui punta *lParam* saranno sempre zero. I membri **destro** e **inferiore** rappresentano il valore minimo *CX* e *CY* necessari per il controllo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

