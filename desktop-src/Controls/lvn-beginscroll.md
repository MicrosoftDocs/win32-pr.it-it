---
title: Codice di notifica LVN_BEGINSCROLL (COMmctrl. h)
description: Notifica alla finestra padre di un controllo di visualizzazione elenco quando viene avviata un'operazione di scorrimento. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 67123db1-118c-43d7-8511-12a3c4413958
keywords:
- Controlli di Windows per il codice di notifica LVN_BEGINSCROLL
topic_type:
- apiref
api_name:
- LVN_BEGINSCROLL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae09a05525ac6e9f08d8cc7a0b7de6ef51329baa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475364"
---
# <a name="lvn_beginscroll-notification-code"></a>\_Codice di notifica BEGINSCROLL di LVN

Notifica alla finestra padre di un controllo di visualizzazione elenco quando viene avviata un'operazione di scorrimento. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
LVN_BEGINSCROLL

    pnmLVScroll = (LPNMLVSCROLL) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**NMLVSCROLL**](/windows/win32/api/commctrl/ns-commctrl-nmlvscroll) che contiene la posizione orizzontale o verticale della posizione in cui inizia l'operazione di scorrimento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Valore restituito non utilizzato.

## <a name="remarks"></a>Commenti

> [!Note]  
> Per usare questo codice di notifica, è necessario fornire un manifesto che specifichi Comclt32.dll versione 6,0. Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





