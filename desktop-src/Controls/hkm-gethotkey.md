---
title: Messaggio HKM_GETHOTKEY (COMmctrl. h)
description: Ottiene il codice della chiave virtuale e i flag di modifica di un tasto di scelta da un controllo tasto di scelta.
ms.assetid: 8b061411-604d-46ea-a082-3eca2d47d992
keywords:
- Controlli di Windows Message HKM_GETHOTKEY
topic_type:
- apiref
api_name:
- HKM_GETHOTKEY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16e23e02f32a4dd6f82f61fd735688353f48ec19
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476319"
---
# <a name="hkm_gethotkey-message"></a>\_Messaggio GETHOTKEY HKM

Ottiene il codice della chiave virtuale e i flag di modifica di un tasto di scelta da un controllo tasto di scelta.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il codice della chiave virtuale e i flag di modifica. Il [**LOBYTE**](/previous-versions/windows/desktop/legacy/ms632658(v=vs.85)) del [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) è il codice della chiave virtuale del tasto di scelta. [**HIBYTE**](/previous-versions/windows/desktop/legacy/ms632656(v=vs.85)) di **LOWORD** è il modificatore di chiave che specifica le chiavi che definiscono una combinazione di tasti di scelta rapida. I flag di modifica possono essere una combinazione dei valori seguenti.



| Valore            | Significato      |
|------------------|--------------|
| HOTKEYF \_ ALT     | ALT (tasto)      |
| \_controllo HOTKEYF | Chiave di controllo  |
| HOTKEYF \_ ext     | Chiave estesa |
| HOTKEYF \_ Shift   | Tasto MAIUSC    |



 

## <a name="remarks"></a>Commenti

Il valore a 16 bit restituito da questo messaggio può essere utilizzato come parametro *wParam* nel messaggio del [**\_ sehotkey WM**](/windows/desktop/inputdev/wm-sethotkey) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

