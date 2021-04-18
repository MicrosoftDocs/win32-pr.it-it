---
title: Codice di notifica TTN_LINKCLICK (COMmctrl. h)
description: Inviato quando si fa clic su un collegamento di testo all'interno di una descrizione comandi a fumetto. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: d3e76431-5b5f-4d67-8528-db21fd939917
keywords:
- Controlli di Windows per il codice di notifica TTN_LINKCLICK
topic_type:
- apiref
api_name:
- TTN_LINKCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c90be24910c2739b4495b651abf97156342d955b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301934"
---
# <a name="ttn_linkclick-notification-code"></a>\_Codice di notifica LINKCLICK di TTN

Inviato quando si fa clic su un collegamento di testo all'interno di una descrizione comandi a fumetto. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
TTN_LINKCLICK
```



## <a name="parameters"></a>Parametri

Questo codice di notifica non contiene parametri.

## <a name="return-value"></a>Valore restituito

Valore restituito non utilizzato.

## <a name="remarks"></a>Commenti

Di seguito è riportato un esempio di quando viene inviata la notifica. Si supponga che la descrizione comando del fumetto includa il testo seguente: "questo è un <A>collegamento</A>". Quando si fa clic su "link", il controllo tooltip Invia un \_ codice di notifica LINKCLICK TTN.

> [!Note]  
> Per usare questo codice di notifica, è necessario fornire un manifesto che specifichi Comclt32.dll versione 6,0. Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





