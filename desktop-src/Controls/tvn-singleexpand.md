---
title: Codice di notifica TVN_SINGLEEXPAND (COMmctrl. h)
description: Inviato da un controllo di visualizzazione albero con lo \_ stile SINGLEEXPAND TVS quando l'utente apre o chiude un elemento della struttura ad albero usando un solo clic del mouse. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: ae738237-172a-400b-b9fe-33832224e299
keywords:
- Controlli di Windows per il codice di notifica TVN_SINGLEEXPAND
topic_type:
- apiref
api_name:
- TVN_SINGLEEXPAND
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 976c0e8acfee1f024e4ee7f88d9f745e4029ec82
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475743"
---
# <a name="tvn_singleexpand-notification-code"></a>\_Codice di notifica SINGLEEXPAND di TVN

Inviato da un controllo di visualizzazione albero con lo [**stile \_ SINGLEEXPAND TVS**](tree-view-control-window-styles.md) quando l'utente apre o chiude un elemento della struttura ad albero usando un solo clic del mouse. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
TVN_SINGLEEXPAND

    lpnmtv = (LPNMTREEVIEW)lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) che contiene informazioni su questo codice di notifica.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce TVNRET \_ default per consentire il comportamento predefinito. Per modificare il comportamento predefinito, restituire:



| Codice restituito                                                                                    | Descrizione                                                      |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <dt>**\_SKIPOLD TVNRET**</dt> </dl> | Ignora l'elaborazione predefinita dell'elemento da deselezionare.<br/> |
| <dl> <dt>**\_SKIPNEW TVNRET**</dt> </dl> | Ignora l'elaborazione predefinita dell'elemento selezionato.<br/>   |



 

## <a name="remarks"></a>Commenti

Per ignorare l'elaborazione predefinita di elementi selezionati e deselezionati, restituire sia TVNRET \_ SKIPOLD che TVNRET \_ SKIPNEW combinando questi elementi con un OR logico.

Questo codice di notifica viene inviato solo da controlli di visualizzazione albero con lo [**stile \_ SINGLEEXPAND TV**](tree-view-control-window-styles.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





