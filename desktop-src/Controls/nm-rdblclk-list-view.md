---
title: NM_RDBLCLK di notifica (visualizzazione elenco) (Commctrl.h)
description: Inviato da un controllo di visualizzazione elenco quando l'utente fa doppio clic su un elemento con il pulsante destro del mouse. Questo codice di notifica viene inviato sotto forma di messaggio WM \_ NOTIFY.
ms.assetid: ebbb127f-07bd-48e0-bf38-7bbda5802f70
keywords:
- NM_RDBLCLK di notifica (visualizzazione elenco) Windows controlli
topic_type:
- apiref
api_name:
- NM_RDBLCLK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c0197659f89392d352e2500d37cbda9dadee5487c5ee180123f502d127925a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957990"
---
# <a name="nm_rdblclk-list-view-notification-code"></a>Codice \_ di notifica NM RDBLCLK (visualizzazione elenco)

Inviato da un controllo di visualizzazione elenco quando l'utente fa doppio clic su un elemento con il pulsante destro del mouse. Questo codice di notifica viene inviato sotto forma di [**messaggio WM \_ NOTIFY.**](wm-notify.md)


```C++
NM_RDBLCLK

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



 

 





