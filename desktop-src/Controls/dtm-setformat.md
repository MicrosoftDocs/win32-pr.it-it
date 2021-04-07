---
title: Messaggio DTM_SETFORMAT (COMmctrl. h)
description: Imposta la visualizzazione di un controllo di selezione data e ora (DTP) in base a una stringa di formato specificata. È possibile inviare questo messaggio in modo esplicito o utilizzare la \_ macro DateTime Seformatt.
ms.assetid: a89fa3ad-9894-4c52-ab56-fb62208e39b3
keywords:
- Controlli di Windows Message DTM_SETFORMAT
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
ms.openlocfilehash: 17669ed2e1ed23e3b090b77701bbe05d23a5ccb8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048565"
---
# <a name="dtm_setformat-message"></a>DTM- \_ Formatta messaggio

Imposta la visualizzazione di un controllo di selezione data e ora (DTP) in base a una stringa di formato specificata. È possibile inviare questo messaggio in modo esplicito o utilizzare la macro [**DateTime \_ seformatt**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setformat) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una [stringa di formato](date-and-time-picker-controls.md) con terminazione zero che definisce la visualizzazione desiderata. Se si imposta questo parametro su **null** , il controllo verrà reimpostato sulla stringa di formato predefinita per lo stile corrente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore diverso da zero se ha esito positivo oppure zero in caso contrario.

## <a name="remarks"></a>Commenti

È accettabile includere caratteri aggiuntivi nella stringa di formato per produrre una visualizzazione più dettagliata. Tutti i caratteri non formattati, tuttavia, devono essere racchiusi tra virgolette singole. Ad esempio, la stringa di formato "' oggi è:' HH ':'':' ddddMMMdd ',' yyy" produrrebbe output come "Today is: 04:22:31 Tuesday Mar 23, 1996".

> [!Note]  
> Un controllo DTP tiene traccia delle modifiche alle impostazioni locali quando usa la stringa di formato predefinita. Se si imposta una stringa di formato personalizzata, non verrà aggiornata in risposta alle modifiche delle impostazioni locali.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **DTM \_ SETFORMATW** (Unicode) e **MDT \_ formattera** (ANSI)<br/>               |



 

 





