---
title: Codice di notifica NM_GETCUSTOMSPLITRECT (COMmctrl. h)
description: Inviato da un controllo pulsante al relativo elemento padre per ottenere le misurazioni per i due rettangoli del pulsante di suddivisione. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: ce72778d-3cca-46a4-9d05-40954a18681d
keywords:
- Controlli di Windows per il codice di notifica NM_GETCUSTOMSPLITRECT
topic_type:
- apiref
api_name:
- NM_GETCUSTOMSPLITRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97b839540da7e07069fdf56ed656ed8772d029eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104118986"
---
# <a name="nm_getcustomsplitrect-notification-code"></a>\_Codice di notifica GETCUSTOMSPLITRECT Nm

Inviato da un controllo pulsante al relativo elemento padre per ottenere le misurazioni per i due rettangoli del pulsante di suddivisione. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
NM_GETCUSTOMSPLITRECT
        
    nmCustomSplit = (NMCUSTOMSPLITRECTINFO *) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a un [**NMCUSTOMSPLITRECTINFO**](/windows/win32/api/commctrl/ns-commctrl-nmcustomsplitrectinfo) per ricevere informazioni sui rettangoli di delimitazione. La struttura **NMCUSTOMSPLITRECTINFO** viene inviata con il codice di notifica come richiesta all'elemento padre per fornire misure per i rettangoli del pulsante di suddivisione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce [**CDRF \_ SKIPDEFAULT**](cdrf-constants.md) per indicare al controllo Button di usare i valori restituiti nella struttura [**NMCUSTOMSPLITRECTINFO**](/windows/win32/api/commctrl/ns-commctrl-nmcustomsplitrectinfo) ; in caso contrario, restituisce [**CDRF \_ DODEFAULT**](cdrf-constants.md).

## <a name="remarks"></a>Commenti

Questo codice di notifica viene inviato da un controllo Button prima che venga disegnato. Il pulsante deve essere di tipo [**BS \_ SPLITBUTTON**](button-styles.md) o [**BS \_ DEFSPLITBUTTON**](button-styles.md). Se i rettangoli restituiti al controllo in *lParam* non sono validi, verranno ignorati.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





