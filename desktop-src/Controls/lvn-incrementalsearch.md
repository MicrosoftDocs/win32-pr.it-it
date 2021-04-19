---
title: Codice di notifica LVN_INCREMENTALSEARCH (COMmctrl. h)
description: Notifica alla finestra padre di un controllo di visualizzazione elenco che è stata avviata una ricerca incrementale. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 34517250-a6ba-490b-b87e-b09048543339
keywords:
- Controlli di Windows per il codice di notifica LVN_INCREMENTALSEARCH
topic_type:
- apiref
api_name:
- LVN_INCREMENTALSEARCH
- LVN_INCREMENTALSEARCHA
- LVN_INCREMENTALSEARCHW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4784ed8f2a9df664b203f776dc1102702d2861e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302801"
---
# <a name="lvn_incrementalsearch-notification-code"></a>\_Codice di notifica INCREMENTALSEARCH di LVN

Notifica alla finestra padre di un controllo di visualizzazione elenco che è stata avviata una ricerca incrementale. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
LVN_INCREMENTALSEARCH
          
    pnmv = (LPNMLVFINDITEM) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* \[ in\]
</dt> <dd>

Puntatore a una struttura [**NMLVFINDITEM**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema) che descrive il codice di notifica. Il chiamante è responsabile dell'allocazione di questa struttura, incluse le strutture [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) e [**LVFINDINFO**](/windows/win32/api/commctrl/ns-commctrl-lvfindinfoa) contenute. Impostare i membri della struttura **NMHDR** . Il membro del **codice** deve essere impostato su LVN \_ INCREMENTALSEARCH.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Il ricevitore di notifiche esegue il cast di *lParam* per recuperare la struttura [**NMLVFINDITEM**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema) . Il parametro *wParam* contiene l'ID del controllo che invia il codice di notifica.

Questo codice di notifica fornisce a un'applicazione (o al ricevitore di notifiche) la possibilità di personalizzare una ricerca incrementale. Se, ad esempio, gli elementi di ricerca sono numerici, l'applicazione può eseguire una ricerca numerica anziché una stringa.

L'applicazione imposta il membro **lParam** della struttura [**LVFINDINFO**](/windows/win32/api/commctrl/ns-commctrl-lvfindinfoa) contenuto nella struttura [**NMLVFINDITEM**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema) sul risultato della ricerca o su un altro valore definito dall'applicazione per interrompere la ricerca e indicare al controllo come continuare.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl>   |
| Nomi Unicode e ANSI<br/>   | **LVN \_ INCREMENTALSEARCHW** (Unicode) e **LVN \_ INCREMENTALSEARCHA** (ANSI)<br/> |



 

 





