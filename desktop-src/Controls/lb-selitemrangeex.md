---
title: Messaggio LB_SELITEMRANGEEX (winuser. h)
description: Seleziona uno o più elementi consecutivi in una casella di riepilogo a selezione multipla.
ms.assetid: aac85d72-43e2-4ab0-b9ee-c7a87e21d7a1
keywords:
- Controlli di Windows Message LB_SELITEMRANGEEX
topic_type:
- apiref
api_name:
- LB_SELITEMRANGEEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4aa3ca1335372b7a61c4dfcbc379c36e89ff933e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964751"
---
# <a name="lb_selitemrangeex-message"></a>\_Messaggio SELITEMRANGEEX lb

Seleziona uno o più elementi consecutivi in una casella di riepilogo a selezione multipla.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Specifica l'indice in base zero del primo elemento da selezionare.

Windows 95/Windows 98/Windows Millennium Edition (Windows Me): il parametro *wParam* è limitato ai valori a 16 bit. Ciò significa che le caselle di riepilogo non possono contenere più di 32.767 elementi. Sebbene il numero di elementi sia limitato, le dimensioni totali in byte degli elementi in una casella di riepilogo sono limitate solo dalla memoria disponibile.

</dd> <dt>

*lParam* 
</dt> <dd>

Specifica l'indice in base zero dell'ultimo elemento da selezionare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se si verifica un errore, il valore restituito è LB \_ Err.

## <a name="remarks"></a>Commenti

Se il parametro *wParam* è inferiore al parametro *lParam* , viene selezionato l'intervallo di elementi specificato. Se *wParam* è maggiore o uguale a *lParam*, l'intervallo viene rimosso dall'intervallo di elementi specificato. Per selezionare un solo elemento, selezionare due elementi, quindi deselezionare l'elemento indesiderato.

Utilizzare questo messaggio solo con caselle di riepilogo a selezione multipla.

Questo messaggio può selezionare un intervallo solo entro i primi 65.536 elementi.

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

[**\_SELITEMRANGE lb**](lb-selitemrange.md)
</dt> <dt>

[**\_SETSEL lb**](lb-setsel.md)
</dt> </dl>

 

 





