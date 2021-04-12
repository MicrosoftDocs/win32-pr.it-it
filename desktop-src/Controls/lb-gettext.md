---
title: Messaggio LB_GETTEXT (winuser. h)
description: Ottiene una stringa da una casella di riepilogo.
ms.assetid: 6bf7ec3b-237b-4668-9493-40c098a32428
keywords:
- Controlli di Windows Message LB_GETTEXT
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
ms.openlocfilehash: c3dd5e2c7a9e6c1c1aa1b847592555a013766134
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478257"
---
# <a name="lb_gettext-message"></a>\_Messaggio lb GETtext

Ottiene una stringa da una casella di riepilogo.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice in base zero della stringa da recuperare.

Windows 95/Windows 98/Windows Millennium Edition (Windows Me): il parametro *wParam* è limitato ai valori a 16 bit. Ciò significa che le caselle di riepilogo non possono contenere più di 32.767 elementi. Sebbene il numero di elementi sia limitato, le dimensioni totali in byte degli elementi in una casella di riepilogo sono limitate solo dalla memoria disponibile.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore al buffer che riceverà la stringa. è di tipo **LPTSTR** che viene successivamente eseguito il cast a un **lParam**. Il buffer deve contenere spazio sufficiente per la stringa e un carattere null di terminazione. Un messaggio [**lb \_ GETTEXTLEN**](lb-gettextlen.md) può essere inviato prima del messaggio **lb \_ gettext** per recuperare la lunghezza, in **TCHAR** s, della stringa.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è la lunghezza della stringa, in **TCHAR** s, escluso il carattere null di terminazione. Se *wParam* non specifica un indice valido, il valore restituito è lb \_ Err.

## <a name="remarks"></a>Commenti

Se la casella di riepilogo ha uno stile disegnato dal proprietario ma non lo stile [**\_ HASSTRINGS lbs**](list-box-styles.md) , il buffer a cui punta il parametro *lParam* riceve il valore associato all'elemento (i dati dell'elemento).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_GETTEXTLEN lb**](lb-gettextlen.md)
</dt> </dl>

 

 





