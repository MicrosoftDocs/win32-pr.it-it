---
title: Codice di notifica TBN_DROPDOWN (COMmctrl. h)
description: Inviato da un controllo Toolbar quando l'utente fa clic su un pulsante a discesa. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 85360f74-4b43-4d0a-8c89-22b0741fe96a
keywords:
- Controlli di Windows per il codice di notifica TBN_DROPDOWN
topic_type:
- apiref
api_name:
- TBN_DROPDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad7adbb9e0e2ed3d77f8ca8bfb6b09dedd2265be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964035"
---
# <a name="tbn_dropdown-notification-code"></a>\_Codice di notifica a discesa TBN

Inviato da un controllo Toolbar quando l'utente fa clic su un pulsante a discesa. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
TBN_DROPDOWN

    lpnmtb = (LPNMTOOLBAR) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) che contiene informazioni su questo codice di notifica. Per questo codice di notifica, sono validi solo i membri **HDR** e **iItem** di questa struttura.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori seguenti:



| Codice restituito                                                                                          | Descrizione                                                                       |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <dl> <dt>**\_impostazione predefinita TBDDRET**</dt> </dl>      | L'elenco a discesa è stato gestito.<br/>                                             |
| <dl> <dt>**TBDDRET \_ NOdefault**</dt> </dl>    | L'elenco a discesa non è stato gestito.<br/>                                         |
| <dl> <dt>**\_TREATPRESSED TBDDRET**</dt> </dl> | L'elenco a discesa è stato gestito, ma viene considerato come un pulsante normale.<br/> |



 

## <a name="remarks"></a>Commenti

> [!Note]  
> I pulsanti a discesa possono essere semplici (stile [**\_ elenco a discesa BTNS**](toolbar-control-and-button-styles.md) ), visualizzare una freccia accanto all'immagine del pulsante (stile [**\_ WHOLEDROPDOWN BTNS**](toolbar-control-and-button-styles.md) ) o visualizzare una freccia separata dall'immagine (stile [**TBSTYLE \_ ex \_ DRAWDDARROWS**](toolbar-extended-styles.md) ). Se viene utilizzata una freccia separata, \_ l'elenco a discesa TBN viene inviato solo se l'utente fa clic sulla parte della freccia del pulsante. Se l'utente fa clic sulla parte principale del pulsante, viene inviato un messaggio di [**\_ comando WM**](/windows/desktop/menurc/wm-command) con ID del pulsante, come per un pulsante standard. Per gli altri due stili del pulsante a discesa, \_ l'elenco a discesa TBN viene inviato quando l'utente fa clic su una parte del pulsante.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

