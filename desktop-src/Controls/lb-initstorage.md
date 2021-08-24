---
title: LB_INITSTORAGE messaggio (Winuser.h)
description: Alloca memoria per l'archiviazione degli elementi della casella di riepilogo. Questo messaggio viene usato prima che un'applicazione abiliti un numero elevato di elementi a una casella di riepilogo.
ms.assetid: abc49049-3424-46c6-981a-b858afe88883
keywords:
- LB_INITSTORAGE dei controlli Windows messaggio
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
ms.openlocfilehash: fe873244358bf171c3fcedc994facd36e194edf38e0ee0442f12556cc4342514
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119544271"
---
# <a name="lb_initstorage-message"></a>Messaggio \_ LB INITSTORAGE

Alloca memoria per l'archiviazione degli elementi della casella di riepilogo. Questo messaggio viene usato prima che un'applicazione abiliti un numero elevato di elementi a una casella di riepilogo.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Numero di elementi da aggiungere.

Windows 95/Windows 98/Windows Millennium Edition (Windows Me): il *parametro wParam* è limitato a valori a 16 bit. Ciò significa che le caselle di riepilogo non possono contenere più di 32.767 elementi. Anche se il numero di elementi è limitato, la dimensione totale in byte degli elementi in una casella di riepilogo è limitata solo dalla memoria disponibile.

</dd> <dt>

*lParam* 
</dt> <dd>

Quantità di memoria, in byte, da allocare per le stringhe degli elementi.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il messaggio ha esito positivo, il valore restituito è il numero totale di elementi per cui è stata preallocazione memoria, ovvero il numero totale di elementi aggiunti da tutti i messaggi **\_ LB INITSTORAGE** riusciti.

Se il messaggio ha esito negativo, il valore restituito è LB \_ ERRSPACE.

Microsoft Windows NT 4.0: questo messaggio non alloca la quantità di memoria specificata. tuttavia, restituisce sempre il valore specificato nel *parametro wParam.*

## <a name="remarks"></a>Commenti

Il **messaggio \_ LB INITSTORAGE** consente di velocizzare l'inizializzazione delle caselle di riepilogo con un numero elevato di elementi (più di 100). Riserva la quantità di memoria specificata in modo che i messaggi [**LB \_ ADDSTRING,**](lb-addstring.md) [**LB \_ INSERTSTRING,**](lb-insertstring.md) [**LB \_ DIR**](lb-dir.md)e [**LB \_ ADDFILE**](lb-addfile.md) successivi prendano il tempo più breve possibile. È possibile usare stime per i *parametri wParam* *e lParam.* Se si sovrastima, la memoria aggiuntiva viene allocata; Se si sottovaluta, viene usata l'allocazione normale per gli elementi che superano l'importo richiesto.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                                           |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**LB \_ ADDFILE**](lb-addfile.md)
</dt> <dt>

[**LB \_ ADDSTRING**](lb-addstring.md)
</dt> <dt>

[**LB \_ DIR**](lb-dir.md)
</dt> <dt>

[**LB \_ INSERTSTRING**](lb-insertstring.md)
</dt> </dl>

 

 





