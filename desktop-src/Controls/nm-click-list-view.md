---
title: NM_CLICK (visualizzazione elenco) codice di notifica (Commctrl.h)
description: Inviato da un controllo di visualizzazione elenco quando l'utente fa clic su un elemento con il pulsante sinistro del mouse. Questo codice di notifica viene inviato sotto forma di messaggio WM \_ NOTIFY.
ms.assetid: 7921bc27-54ca-4bb2-ac88-8267776661ab
keywords:
- NM_CLICK di notifica (visualizzazione elenco) Windows controlli
topic_type:
- apiref
api_name:
- NM_CLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e9189861db0ec956b549145584202e3b88978478a9dd8de4386785d46e0d160
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120061761"
---
# <a name="nm_click-list-view-notification-code"></a>Codice \_ di notifica NM CLICK (visualizzazione elenco)

Inviato da un controllo di visualizzazione elenco quando l'utente fa clic su un elemento con il pulsante sinistro del mouse. Questo codice di notifica viene inviato sotto forma di [**messaggio WM \_ NOTIFY.**](wm-notify.md)


```C++
NM_CLICK

    lpnmitem = (LPNMITEMACTIVATE) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

[Versione 4.71](common-control-versions.md). Puntatore a [**una struttura NMITEMACTIVATE**](/windows/win32/api/commctrl/ns-commctrl-nmitemactivate) che contiene informazioni aggiuntive su questa notifica. I **membri iItem**, **iSubItem** e **ptAction** di questa struttura contengono informazioni sull'elemento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito per questa notifica non viene usato.

## <a name="remarks"></a>Commenti

Il **membro iItem** di *lParam* è valido solo se è stato fatto clic sull'icona o sull'etichetta della prima colonna. Per determinare quale elemento viene selezionato quando un clic viene fatto altrove in una riga, inviare un [**messaggio LVM \_ SUBITEMHITTEST.**](lvm-subitemhittest.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





