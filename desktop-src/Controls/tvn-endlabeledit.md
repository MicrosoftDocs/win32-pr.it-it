---
title: Codice di notifica TVN_ENDLABELEDIT (COMmctrl. h)
description: Notifica alla finestra padre di un controllo di visualizzazione albero la fine della modifica dell'etichetta per un elemento. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 82eb9fcd-de10-4efb-8501-78c5af5e089e
keywords:
- Controlli di Windows per il codice di notifica TVN_ENDLABELEDIT
topic_type:
- apiref
api_name:
- TVN_ENDLABELEDIT
- TVN_ENDLABELEDITA
- TVN_ENDLABELEDITW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c30d494ad90b3d55f85b1ad154aed0f814a1eec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119918"
---
# <a name="tvn_endlabeledit-notification-code"></a>\_Codice di notifica ENDLABELEDIT di TVN

Notifica alla finestra padre di un controllo di visualizzazione albero la fine della modifica dell'etichetta per un elemento. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
TVN_ENDLABELEDIT 

    ptvdi = (LPNMTVDISPINFO) lParam 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**struttura NMTVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmtvdispinfoa) . Il membro dell' **elemento** di questa struttura è una struttura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) i cui membri **Hite**, **lParam** e **pszText** contengono informazioni valide sull'elemento che è stato modificato. Se la modifica dell'etichetta è stata annullata, il membro **pszText** della struttura **TVITEM** è **null**. in caso contrario, **pszText** è l'indirizzo del testo modificato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il membro **pszText** è diverso da **null**, restituire **true** per impostare l'etichetta dell'elemento sul testo modificato. Restituisce **false** per rifiutare il testo modificato e ripristinare l'etichetta originale.

## <a name="remarks"></a>Commenti

Se il membro **pszText** è **null**, il valore restituito viene ignorato.

Se è stato specificato il \_ valore TEXTCALLBACK di LPSTR per questo elemento e il membro **pszText** è diverso da **null**, il \_ gestore ENDLABELEDIT di TVN deve copiare il testo da **pszText** nella risorsa di archiviazione locale.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **TVN \_ ENDLABELEDITW** (Unicode) e **TVN \_ ENDLABELEDITA** (ANSI)<br/>         |



 

 





