---
title: DTM_SETSYSTEMTIME messaggio (Commctrl.h)
description: Imposta l'ora in un controllo di selezione data e ora (DTP). È possibile inviare questo messaggio in modo esplicito o usare la \_ macro DateTime SetSystemtime.
ms.assetid: aab023ac-22ef-485b-be2f-2aa76dfcf57f
keywords:
- DTM_SETSYSTEMTIME dei messaggi Windows controlli
topic_type:
- apiref
api_name:
- DTM_SETSYSTEMTIME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5acd0c6a09e3fc7bd9d068e27049329f3289a8ba1968ffae4592c7e07db9f2eb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088971"
---
# <a name="dtm_setsystemtime-message"></a>Messaggio DTM \_ SETSYSTEMTIME

Imposta l'ora in un controllo di selezione data e ora (DTP). È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ DateTime SetSystemtime.**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setsystemtime)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Valore che specifica l'azione da eseguire. Questo valore deve essere impostato su uno dei valori seguenti:



| Valore                                                                                                                                             | Significato                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GDT_VALID"></span><span id="gdt_valid"></span><dl> <dt>**GDT \_ VALIDO**</dt> </dl> | Impostare il controllo DTP in base ai dati all'interno della struttura a cui *punta lParam.* <br/>                                                                                                                                                                 |
| <span id="GDT_NONE"></span><span id="gdt_none"></span><dl> <dt>**GDT \_ NONE**</dt> </dl>    | Impostare il controllo DTP su "nessuna data" e deselezionarne la casella di controllo. Quando viene specificato questo flag, *lParam* viene ignorato. Questo flag si applica solo ai controlli DTP impostati sullo [**stile DTS \_ SHOWNONE.**](date-and-time-picker-control-styles.md) <br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una [**struttura SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) contenente l'ora di sistema utilizzata per impostare il controllo DTP.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore diverso da zero in caso di esito positivo oppure zero in caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

