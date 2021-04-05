---
title: Messaggio DTM_GETSYSTEMTIME (COMmctrl. h)
description: Ottiene l'ora attualmente selezionata da un controllo di selezione data e ora (DTP) e la inserisce in una struttura SYSTEMTIME specificata. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro DateTime GetSystemtime.
ms.assetid: 81c95187-109c-4b36-98ea-a2e77ce42d9a
keywords:
- Controlli di Windows Message DTM_GETSYSTEMTIME
topic_type:
- apiref
api_name:
- DTM_GETSYSTEMTIME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e14d8c998720cc987a03877e1918e97304bf769
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120546"
---
# <a name="dtm_getsystemtime-message"></a>\_Messaggio GETSYSTEMTIME DTM

Ottiene l'ora attualmente selezionata da un controllo di selezione data e ora (DTP) e la inserisce in una struttura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) specificata. È possibile inviare questo messaggio in modo esplicito o usare la macro [**DateTime \_ GetSystemtime**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getsystemtime) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) . Se **DTM \_ GETSYSTEMTIME** restituisce GDT \_ valido, questa struttura conterrà l'ora attualmente selezionata. In caso contrario, non conterrà informazioni valide. Questo parametro deve essere un puntatore valido; non può essere **null**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce GDT \_ valido se le informazioni sull'ora sono state inserite correttamente in *lParam*. Restituisce GDT \_ None se il controllo è stato impostato sullo stile [**DTS \_ SHOWNONE**](date-and-time-picker-control-styles.md) e non è stata selezionata la casella di controllo Control. Restituisce \_ un errore GDT se si verifica un errore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

