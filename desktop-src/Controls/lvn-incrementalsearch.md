---
title: LVN_INCREMENTALSEARCH di notifica (Commctrl.h)
description: Notifica alla finestra padre di un controllo visualizzazione elenco che è stata avviata una ricerca incrementale. Questo codice di notifica viene inviato sotto forma di messaggio WM \_ NOTIFY.
ms.assetid: 34517250-a6ba-490b-b87e-b09048543339
keywords:
- LVN_INCREMENTALSEARCH del codice di notifica Windows controlli
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
ms.openlocfilehash: 0ec3207fbb16bca23bf44ac61fee58bb6e4fad1ff74c38d7b56910ed52997f39
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119826121"
---
# <a name="lvn_incrementalsearch-notification-code"></a>Codice di notifica LVN \_ INCREMENTALSEARCH

Notifica alla finestra padre di un controllo visualizzazione elenco che è stata avviata una ricerca incrementale. Questo codice di notifica viene inviato sotto forma di messaggio [**WM \_ NOTIFY.**](wm-notify.md)


```C++
LVN_INCREMENTALSEARCH
          
    pnmv = (LPNMLVFINDITEM) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* \[ Pollici\]
</dt> <dd>

Puntatore a [**una struttura NMLVFINDITEM**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema) che descrive il codice di notifica. Il chiamante è responsabile dell'allocazione di questa struttura, incluse le strutture [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) e [**LVFINDINFO**](/windows/win32/api/commctrl/ns-commctrl-lvfindinfoa) contenute. Impostare i membri della **struttura NMHDR.** Il **membro** di codice deve essere impostato su LVN \_ INCREMENTALSEARCH.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Il ricevitore della notifica esegue il cast *di lParam* per recuperare [**la struttura NMLVFINDITEM.**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema) Il *parametro wParam* contiene l'ID del controllo che invia questo codice di notifica.

Questo codice di notifica offre a un'applicazione (o al destinatario della notifica) la possibilità di personalizzare una ricerca incrementale. Ad esempio, se gli elementi di ricerca sono numerici, l'applicazione può eseguire una ricerca numerica anziché una ricerca di stringhe.

L'applicazione imposta il membro **lParam** della struttura [**LVFINDINFO**](/windows/win32/api/commctrl/ns-commctrl-lvfindinfoa) contenuta nella struttura [**NMLVFINDITEM**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema) sul risultato della ricerca o su un altro valore definito dall'applicazione per non eseguire la ricerca e indicare al controllo come procedere.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                          |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl>   |
| Nomi Unicode e ANSI<br/>   | **LVN \_ INCREMENTALSEARCHW** (Unicode) e **LVN \_ INCREMENTALSEARCHA** (ANSI)<br/> |



 

 





