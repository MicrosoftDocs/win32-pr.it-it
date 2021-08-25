---
title: DTM_GETMCFONT messaggio (Commctrl.h)
description: Ottiene il tipo di carattere attualmente utilizzato dal controllo calendario mensile figlio del controllo selezione data e ora. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro DateTime GetMonthCalFont.
ms.assetid: 6687a1dc-6f6d-4684-80b2-f726b08d2f3a
keywords:
- DTM_GETMCFONT controlli Windows messaggio
topic_type:
- apiref
api_name:
- DTM_GETMCFONT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2bf60f226e7fe5d309324bc517a7fd215abe4591fd5141ff149b14e162ac9be
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119878131"
---
# <a name="dtm_getmcfont-message"></a>Messaggio DTM \_ GETMCFONT

Ottiene il tipo di carattere attualmente utilizzato dal controllo calendario mensile figlio del controllo selezione data e ora. È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ DateTime GetMonthCalFont.**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcalfont)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore HFONT che rappresenta l'handle per il tipo di carattere corrente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





