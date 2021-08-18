---
title: TVN_SELCHANGING codice di notifica (Commctrl.h)
description: Notifica alla finestra padre di un controllo visualizzazione albero che la selezione sta per passare da un elemento a un altro. Questo codice di notifica viene inviato sotto forma di messaggio WM \_ NOTIFY.
ms.assetid: 53f24ee0-433c-4680-9075-5e2b21117ed9
keywords:
- TVN_SELCHANGING codice di notifica Windows controlli
topic_type:
- apiref
api_name:
- TVN_SELCHANGING
- TVN_SELCHANGINGA
- TVN_SELCHANGINGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b09933e1e4c7393521f298c60435efde76fbea23ef703f536fb241cc9f78610
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119433481"
---
# <a name="tvn_selchanging-notification-code"></a>Codice di notifica \_ TVN SELCHANGING

Notifica alla finestra padre di un controllo visualizzazione albero che la selezione sta per passare da un elemento a un altro. Questo codice di notifica viene inviato sotto forma di [**messaggio WM \_ NOTIFY.**](wm-notify.md)


```C++
TVN_SELCHANGING 

    pnmtv = (LPNMTREEVIEW) lParam 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a [**una struttura NMTREEVIEW.**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) **ItemOld** e **itemNew** members contengono informazioni valide sull'elemento attualmente selezionato e sull'elemento appena selezionato. Il **membro** dell'azione indica se un'azione del mouse o della tastiera sta causando la modifica della selezione. Per un elenco dei valori possibili, vedere la descrizione del codice di notifica [ \_ TVN SELCHANGED.](tvn-selchanged.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE** per impedire la modifica della selezione.

## <a name="remarks"></a>Commenti

Quando si risponde a questo codice di notifica, le applicazioni non devono eliminare gli elementi che stanno guadagnando o perdendo la selezione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **TVN \_ SELCHANGINGW** (Unicode) e **TVN \_ SELCHANGINGA** (ANSI)<br/>           |



 

 





