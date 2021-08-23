---
title: LB_SETLOCALE messaggio (Winuser.h)
description: Imposta le impostazioni locali correnti della casella di riepilogo. È possibile usare le impostazioni locali per determinare l'ordinamento corretto del testo visualizzato (per le caselle di riepilogo con lo stile SORT di LBS) e del testo aggiunto dal messaggio \_ \_ LB ADDSTRING.
ms.assetid: e9503124-de9f-4b92-a59e-ec9320864ae7
keywords:
- LB_SETLOCALE del messaggio Windows controlli
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
ms.openlocfilehash: 623b8550b3d5f382ddc8ccc1e1cfcf861a2f8c0a7877ba60c57e393abc1401d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118958540"
---
# <a name="lb_setlocale-message"></a>Messaggio \_ LB SETLOCALE

Imposta le impostazioni locali correnti della casella di riepilogo. È possibile usare le impostazioni locali per determinare l'ordinamento corretto del testo visualizzato (per le caselle di riepilogo con lo stile SORT di [**LBS) \_**](list-box-styles.md) e del testo aggiunto dal messaggio [**\_ LB ADDSTRING.**](lb-addstring.md)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Specifica l'identificatore delle impostazioni locali che verrà utilizzato dalla casella di riepilogo per l'ordinamento durante l'aggiunta di testo.

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è l'identificatore delle impostazioni locali precedente. Se il *parametro wParam* specifica impostazioni locali non installate nel sistema, il valore restituito è LB ERR e le impostazioni locali correnti della casella di riepilogo \_ non vengono modificate.

## <a name="remarks"></a>Commenti

Utilizzare la macro [**MAKELCID**](/windows/desktop/api/winnt/nf-winnt-makelcid) per costruire un identificatore delle impostazioni locali.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                                           |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**LB \_ ADDSTRING**](lb-addstring.md)
</dt> <dt>

[**LB \_ GETLOCALE**](lb-getlocale.md)
</dt> </dl>

 

