---
title: NM_RCLICK di notifica (visualizzazione elenco) (Commctrl.h)
description: Inviato da un controllo di visualizzazione elenco quando l'utente fa clic su un elemento con il pulsante destro del mouse. Questo codice di notifica viene inviato sotto forma di messaggio WM \_ NOTIFY.
ms.assetid: dc7f97b3-4aec-4a8f-a87c-62cef5ba4c40
keywords:
- NM_RCLICK di notifica (visualizzazione elenco) Windows controlli
topic_type:
- apiref
api_name:
- NM_RCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f58ab6b2496c35bb4b95a3808afb7e58b961584b8b72d086933ad2c3281e6f29
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018809"
---
# <a name="nm_rclick-list-view-notification-code"></a>Codice di \_ notifica nm RCLICK (visualizzazione elenco)

Inviato da un controllo di visualizzazione elenco quando l'utente fa clic su un elemento con il pulsante destro del mouse. Questo codice di notifica viene inviato sotto forma di messaggio [**WM \_ NOTIFY.**](wm-notify.md)


```C++
NM_RCLICK

    lpnmitem = (LPNMITEMACTIVATE) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

[Versione 4.71.](common-control-versions.md) Puntatore a [**una struttura NMITEMACTIVATE**](/windows/win32/api/commctrl/ns-commctrl-nmitemactivate) che contiene informazioni aggiuntive su questa notifica. I **membri iItem**, **iSubItem** e **ptAction** di questa struttura contengono informazioni sull'elemento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore diverso da zero per non consentire l'elaborazione predefinita oppure zero per consentire l'elaborazione predefinita.

## <a name="remarks"></a>Commenti

Il **membro iItem** di *lParam* è valido solo se è stato fatto clic sull'icona o sull'etichetta della prima colonna. Per determinare quale elemento viene selezionato quando si fa clic altrove in una riga, inviare un [**messaggio LVM \_ SUBITEMHITTEST.**](lvm-subitemhittest.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





