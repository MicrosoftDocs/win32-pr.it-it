---
title: LB_GETTEXT messaggio (Winuser.h)
description: Ottiene una stringa da una casella di riepilogo.
ms.assetid: 6bf7ec3b-237b-4668-9493-40c098a32428
keywords:
- LB_GETTEXT di controllo Windows messaggio
topic_type:
- apiref
api_name:
- LB_GETTEXT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b2aa37a2d07e440aac615d1edc1e6f91c6a60e71a96418cd443daff9809ec18
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119434100"
---
# <a name="lb_gettext-message"></a>Messaggio \_ LB GETTEXT

Ottiene una stringa da una casella di riepilogo.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice in base zero della stringa da recuperare.

Windows 95/Windows 98/Windows Millennium Edition (Windows Me): il *parametro wParam* è limitato a valori a 16 bit. Ciò significa che le caselle di riepilogo non possono contenere più di 32.767 elementi. Anche se il numero di elementi è limitato, la dimensione totale in byte degli elementi in una casella di riepilogo è limitata solo dalla memoria disponibile.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore al buffer che riceverà la stringa. è di tipo **LPTSTR di** cui viene successivamente eseguito il cast a **un oggetto LPARAM**. Il buffer deve avere spazio sufficiente per la stringa e un carattere Null di terminazione. È possibile inviare un messaggio [**\_ LB GETTEXTLEN**](lb-gettextlen.md) prima del messaggio **\_ LB GETTEXT** per recuperare la lunghezza, in **TCHAR,** della stringa.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è la lunghezza della stringa, in **TCHAR** s, escluso il carattere Null di terminazione. Se *wParam non* specifica un indice valido, il valore restituito è LB \_ ERR.

## <a name="remarks"></a>Commenti

Se la casella di riepilogo ha uno stile disegnato dal proprietario ma non lo stile [**\_ LBS HASSTRINGS,**](list-box-styles.md) il buffer a cui punta il *parametro lParam* riceve il valore associato all'elemento (i dati dell'elemento).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                                           |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**LB \_ GETTEXTLEN**](lb-gettextlen.md)
</dt> </dl>

 

 





