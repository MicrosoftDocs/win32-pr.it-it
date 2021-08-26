---
title: DTM_SETFORMAT messaggio (Commctrl.h)
description: Imposta la visualizzazione di un controllo di selezione data e ora (DTP) in base a una determinata stringa di formato. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro DateTime SetFormat.
ms.assetid: a89fa3ad-9894-4c52-ab56-fb62208e39b3
keywords:
- DTM_SETFORMAT di controllo Windows messaggio
topic_type:
- apiref
api_name:
- DTM_SETFORMAT
- DTM_SETFORMATA
- DTM_SETFORMATW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17d4bb08694b63c21f1790d0a1366dd34d1083592bdeb62d532a32a96be3857a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119877861"
---
# <a name="dtm_setformat-message"></a>Messaggio \_ DTM SETFORMAT

Imposta la visualizzazione di un controllo di selezione data e ora (DTP) in base a una determinata stringa di formato. È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ DateTime SetFormat.**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setformat)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una stringa di formato con [terminazione](date-and-time-picker-controls.md) zero che definisce la visualizzazione desiderata. Se si imposta questo **parametro su NULL,** il controllo verrà reimpostato sulla stringa di formato predefinita per lo stile corrente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore diverso da zero in caso di esito positivo oppure zero in caso contrario.

## <a name="remarks"></a>Commenti

È accettabile includere caratteri aggiuntivi all'interno della stringa di formato per produrre una visualizzazione più ricca. Tuttavia, tutti i caratteri non di formato devono essere racchiusi tra virgolette singole. Ad esempio, la stringa di formato "'Today is: 'hh':'m':'s ddddMMMdd', 'yyy" produce un output simile a "Today is: 04:22:31 Tuesday Mar 23, 1996".

> [!Note]  
> Un controllo DTP tiene traccia delle modifiche alle impostazioni locali quando usa la stringa di formato predefinita. Se si imposta una stringa di formato personalizzata, non verrà aggiornata in risposta alle modifiche delle impostazioni locali.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **DTM \_ SETFORMATW** (Unicode) e **DTM \_ SETFORMATA** (ANSI)<br/>               |



 

 





