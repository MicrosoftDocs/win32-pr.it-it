---
title: Codice di notifica HDN_BEGINDRAG (COMmctrl. h)
description: Inviato da un controllo intestazione quando un'operazione di trascinamento è iniziata su uno degli elementi. Questo codice di notifica viene inviato solo da controlli intestazione impostati sullo \_ stile DragDrop di HDS. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 3dfb7a7c-d783-48e0-ba92-8144104f163a
keywords:
- Controlli di Windows per il codice di notifica HDN_BEGINDRAG
topic_type:
- apiref
api_name:
- HDN_BEGINDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed6b4af8e662a8a9891e9a81535de987337567f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048296"
---
# <a name="hdn_begindrag-notification-code"></a>\_Codice di notifica BEGINDRAG di HDN

Inviato da un controllo intestazione quando un'operazione di trascinamento è iniziata su uno degli elementi. Questo codice di notifica viene inviato solo da controlli intestazione impostati sullo stile [**\_ DragDrop di HDS**](header-control-styles.md) . Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
HDN_BEGINDRAG

   pNMHeader = (LPNMHEADER) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) contenente informazioni sull'elemento dell'intestazione trascinato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per consentire al controllo intestazione di gestire automaticamente le operazioni di trascinamento della selezione, restituire **false**. Se il proprietario del controllo esegue manualmente il riordinamento con trascinamento della selezione, restituisce **true**.

## <a name="remarks"></a>Commenti

Per impostazione predefinita, il controllo dell'intestazione gestisce automaticamente il riordinamento con trascinamento della selezione. Restituisce **true** per indicare che la gestione esterna (manuale) del trascinamento della selezione consente al proprietario del controllo di fornire servizi personalizzati come parte del processo di trascinamento della selezione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





