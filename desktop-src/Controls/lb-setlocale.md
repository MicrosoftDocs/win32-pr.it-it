---
title: Messaggio LB_SETLOCALE (winuser. h)
description: Imposta le impostazioni locali correnti della casella di riepilogo. È possibile utilizzare le impostazioni locali per determinare l'ordinamento corretto del testo visualizzato (per le caselle di riepilogo con lo \_ stile di ordinamento lbs) e del testo aggiunto dal \_ messaggio ADDSTRING lb.
ms.assetid: e9503124-de9f-4b92-a59e-ec9320864ae7
keywords:
- Controlli di Windows Message LB_SETLOCALE
topic_type:
- apiref
api_name:
- LB_SETLOCALE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd8ea7bb7b6d19144a84ab166f56cd2c0ad49e05
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048648"
---
# <a name="lb_setlocale-message"></a>\_Messaggio setlocale di lb

Imposta le impostazioni locali correnti della casella di riepilogo. È possibile utilizzare le impostazioni locali per determinare l'ordinamento corretto del testo visualizzato (per le caselle di riepilogo con lo stile di [**\_ ordinamento lbs**](list-box-styles.md) ) e del testo aggiunto dal [**messaggio \_ ADDSTRING lb**](lb-addstring.md) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Specifica l'identificatore delle impostazioni locali che la casella di riepilogo utilizzerà per l'ordinamento quando si aggiunge il testo.

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è l'identificatore delle impostazioni locali precedente. Se il parametro *wParam* specifica impostazioni locali non installate nel sistema, il valore restituito è lb \_ Err e le impostazioni locali correnti della casella di riepilogo non vengono modificate.

## <a name="remarks"></a>Commenti

Usare la macro [**MAKELCID**](/windows/desktop/api/winnt/nf-winnt-makelcid) per costruire un identificatore delle impostazioni locali.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**\_ADDSTRING lb**](lb-addstring.md)
</dt> <dt>

[**LB \_ GETlocale**](lb-getlocale.md)
</dt> </dl>

 

