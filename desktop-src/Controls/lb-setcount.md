---
title: Messaggio LB_SETCOUNT (winuser. h)
description: Imposta il numero di elementi in una casella di riepilogo creata con lo \_ stile NODATA lbs e non viene creato con lo \_ stile HASSTRINGS lbs.
ms.assetid: 3ebc4237-24d3-443f-86d5-bdcd66a31baf
keywords:
- Controlli di Windows Message LB_SETCOUNT
topic_type:
- apiref
api_name:
- LB_SETCOUNT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2042bcf0e0cbe7f5daacfcf7f493a070860ac9a5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048649"
---
# <a name="lb_setcount-message"></a>\_Messaggi di conteggio lb

Imposta il numero di elementi in una casella di riepilogo creata con lo stile [**\_ NoData lbs**](list-box-styles.md) e non viene creato con lo stile [**\_ HASSTRINGS lbs**](list-box-styles.md) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Specifica il nuovo conteggio degli elementi nella casella di riepilogo.

Windows 95/Windows 98/Windows Millennium Edition (Windows Me): il parametro *wParam* è limitato ai valori a 16 bit. Ciò significa che le caselle di riepilogo non possono contenere più di 32.767 elementi. Sebbene il numero di elementi sia limitato, le dimensioni totali in byte degli elementi in una casella di riepilogo sono limitate solo dalla memoria disponibile.

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se si verifica un errore, il valore restituito è LB \_ Err. Se la memoria disponibile non è sufficiente per archiviare gli elementi, il valore restituito è LB \_ ERRSPACE.

## <a name="remarks"></a>Commenti

Il messaggio **lb \_ secount** è supportato solo dalle caselle di riepilogo create con lo stile [**\_ NoData di lbs**](list-box-styles.md) e non create con lo stile [**\_ HASSTRINGS lbs**](list-box-styles.md) . Tutte le altre caselle di riepilogo restituiscono LB \_ Err.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CONTEGGIO di LB \_**](lb-getcount.md)
</dt> </dl>

 

 





