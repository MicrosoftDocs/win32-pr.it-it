---
title: TTN_LINKCLICK di notifica (Commctrl.h)
description: Inviato quando si fa clic su un collegamento di testo all'interno di una descrizione comando a fumetto. Questo codice di notifica viene inviato sotto forma di messaggio WM \_ NOTIFY.
ms.assetid: d3e76431-5b5f-4d67-8528-db21fd939917
keywords:
- TTN_LINKCLICK del codice di notifica Windows controlli
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
ms.openlocfilehash: a2a31b1f942627ee22fb050bbddd0b74ac10dd09a7a8f14018189620f6c8155f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118166097"
---
# <a name="ttn_linkclick-notification-code"></a>Codice di notifica TTN \_ LINKCLICK

Inviato quando si fa clic su un collegamento di testo all'interno di una descrizione comando a fumetto. Questo codice di notifica viene inviato sotto forma di messaggio [**WM \_ NOTIFY.**](wm-notify.md)


```C++
TTN_LINKCLICK
```



## <a name="parameters"></a>Parametri

Questo codice di notifica non ha parametri.

## <a name="return-value"></a>Valore restituito

Valore restituito non utilizzato.

## <a name="remarks"></a>Commenti

Di seguito è riportato un esempio di quando viene inviata questa notifica. Si supponga che la descrizione comando del fumetto contenga il testo seguente, "This is a <A>link".</A> Quando si fa clic su "link", il controllo descrizione comando invia un codice di notifica TTN \_ LINKCLICK.

> [!Note]  
> Per usare questo codice di notifica, è necessario specificare un manifesto Comclt32.dll versione 6.0. Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione.](cookbook-overview.md)

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





