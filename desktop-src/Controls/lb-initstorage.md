---
title: Messaggio LB_INITSTORAGE (winuser. h)
description: Alloca memoria per archiviare gli elementi della casella di riepilogo. Questo messaggio viene usato prima che un'applicazione aggiunga un numero elevato di elementi a una casella di riepilogo.
ms.assetid: abc49049-3424-46c6-981a-b858afe88883
keywords:
- Controlli di Windows Message LB_INITSTORAGE
topic_type:
- apiref
api_name:
- LB_INITSTORAGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28216705dd0446aeb11adad9d45f9e604171e62c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476816"
---
# <a name="lb_initstorage-message"></a>\_Messaggio INITSTORAGE lb

Alloca memoria per archiviare gli elementi della casella di riepilogo. Questo messaggio viene usato prima che un'applicazione aggiunga un numero elevato di elementi a una casella di riepilogo.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Numero di elementi da aggiungere.

Windows 95/Windows 98/Windows Millennium Edition (Windows Me): il parametro *wParam* è limitato ai valori a 16 bit. Ciò significa che le caselle di riepilogo non possono contenere più di 32.767 elementi. Sebbene il numero di elementi sia limitato, le dimensioni totali in byte degli elementi in una casella di riepilogo sono limitate solo dalla memoria disponibile.

</dd> <dt>

*lParam* 
</dt> <dd>

Quantità di memoria, in byte, da allocare per le stringhe di elemento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il messaggio ha esito positivo, il valore restituito è il numero totale di elementi per cui la memoria è stata pre-allocata, ovvero il numero totale di elementi aggiunti da tutti i messaggi **lb \_ INITSTORAGE** riusciti.

Se il messaggio ha esito negativo, il valore restituito è LB \_ ERRSPACE.

Microsoft Windows NT 4,0: questo messaggio non alloca la quantità di memoria specificata. Tuttavia, restituisce sempre il valore specificato nel parametro *wParam* .

## <a name="remarks"></a>Commenti

Il messaggio **lb \_ INITSTORAGE** consente di velocizzare l'inizializzazione di caselle di riepilogo con un numero elevato di elementi (più di 100). Si riserva la quantità di memoria specificata in modo che i messaggi [**lb \_ ADDSTRING**](lb-addstring.md), [**lb \_ INSERTSTRING**](lb-insertstring.md), [**lb \_ dir**](lb-dir.md)e [**lb \_ AddFile**](lb-addfile.md) prendano il minor tempo possibile. È possibile utilizzare le stime per i parametri *wParam* e *lParam* . Se si esegue la sovrastima, viene allocata la memoria aggiuntiva. Se si sottovaluta, l'allocazione normale viene utilizzata per gli elementi che superano la quantità richiesta.

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

[**\_AddFile lb**](lb-addfile.md)
</dt> <dt>

[**\_ADDSTRING lb**](lb-addstring.md)
</dt> <dt>

[**\_dir lb**](lb-dir.md)
</dt> <dt>

[**\_INSERTSTRING lb**](lb-insertstring.md)
</dt> </dl>

 

 





