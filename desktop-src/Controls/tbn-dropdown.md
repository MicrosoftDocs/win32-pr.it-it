---
title: TBN_DROPDOWN di notifica (Commctrl.h)
description: Inviato da un controllo barra degli strumenti quando l'utente fa clic su un pulsante a discesa. Questo codice di notifica viene inviato sotto forma di messaggio WM \_ NOTIFY.
ms.assetid: 85360f74-4b43-4d0a-8c89-22b0741fe96a
keywords:
- TBN_DROPDOWN codice di notifica Windows controlli
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
ms.openlocfilehash: 1e2cdee38176b2ed72d42aaa29ca685a5e73dd30ceb7e315b5cbe0971161dc13
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119077925"
---
# <a name="tbn_dropdown-notification-code"></a>Codice di notifica TBN \_ DROPDOWN

Inviato da un controllo barra degli strumenti quando l'utente fa clic su un pulsante a discesa. Questo codice di notifica viene inviato sotto forma di [**messaggio WM \_ NOTIFY.**](wm-notify.md)


```C++
TBN_DROPDOWN

    lpnmtb = (LPNMTOOLBAR) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a [**una struttura NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) che contiene informazioni su questo codice di notifica. Per questo codice di notifica, sono validi solo i **membri hdr** e **iItem** di questa struttura.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori seguenti:



| Codice restituito                                                                                          | Descrizione                                                                       |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <dl> <dt>**TBDDRET \_ DEFAULT**</dt> </dl>      | L'elenco a discesa è stato gestito.<br/>                                             |
| <dl> <dt>**TBDDRET \_ NODEFAULT**</dt> </dl>    | L'elenco a discesa non è stato gestito.<br/>                                         |
| <dl> <dt>**TBDDRET \_ TREATPRESSED**</dt> </dl> | L'elenco a discesa è stato gestito, ma il pulsante viene trattato come un normale pulsante.<br/> |



 

## <a name="remarks"></a>Commenti

> [!Note]  
> I pulsanti a discesa possono essere semplici (stile [**BTNS \_ DROPDOWN),**](toolbar-control-and-button-styles.md) visualizzare una freccia accanto all'immagine del pulsante (stile [**BTNS \_ WHOLEDROPDOWN)**](toolbar-control-and-button-styles.md) o una freccia separata dall'immagine (stile [**TBSTYLE \_ EX \_ DRAWDDARROWS).**](toolbar-extended-styles.md) Se si usa una freccia separata, TBN DROPDOWN viene inviato solo se l'utente fa clic sulla parte \_ freccia del pulsante. Se l'utente fa clic sulla parte principale del pulsante, viene inviato un messaggio [**WM \_ COMMAND**](/windows/desktop/menurc/wm-command) con l'ID del pulsante, proprio come con un pulsante standard. Per gli altri due stili del pulsante a discesa, TBN DROPDOWN viene inviato quando l'utente fa clic su qualsiasi \_ parte del pulsante.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

