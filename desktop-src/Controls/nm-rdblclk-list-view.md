---
title: Codice di notifica NM_RDBLCLK (visualizzazione elenco) (COMmctrl. h)
description: Inviato da un controllo di visualizzazione elenco quando l'utente fa doppio clic su un elemento con il pulsante destro del mouse. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: ebbb127f-07bd-48e0-bf38-7bbda5802f70
keywords:
- Codice di notifica NM_RDBLCLK (visualizzazione elenco) controlli Windows
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
ms.openlocfilehash: 41832b228fe40b212c0aba809b15022c6f7b39ce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103965008"
---
# <a name="nm_rdblclk-list-view-notification-code"></a>\_Codice di notifica di RDBLCLK Nm (visualizzazione elenco)

Inviato da un controllo di visualizzazione elenco quando l'utente fa doppio clic su un elemento con il pulsante destro del mouse. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
NM_RDBLCLK

    lpnmitem = (LPNMITEMACTIVATE) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

[Versione 4,71](common-control-versions.md). Puntatore a una struttura [**NMITEMACTIVATE**](/windows/win32/api/commctrl/ns-commctrl-nmitemactivate) che contiene informazioni aggiuntive su questa notifica. I membri **iItem**, **iSubItem** e **ptAction** di questa struttura contengono informazioni sull'elemento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito per questa notifica non viene utilizzato.

## <a name="remarks"></a>Commenti

Il membro **iItem** di *lParam* è valido solo se è stato fatto clic sull'etichetta dell'icona o della prima colonna. Per determinare quale elemento è selezionato quando si fa clic su un punto qualsiasi in una riga, inviare un messaggio [**LVM \_ SUBITEMHITTEST**](lvm-subitemhittest.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





