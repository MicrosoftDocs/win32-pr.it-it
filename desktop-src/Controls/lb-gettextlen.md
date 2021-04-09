---
title: Messaggio LB_GETTEXTLEN (winuser. h)
description: Ottiene la lunghezza di una stringa in una casella di riepilogo.
ms.assetid: 866730bc-ffd4-42fd-9cea-5d326e129189
keywords:
- Controlli di Windows Message LB_GETTEXTLEN
topic_type:
- apiref
api_name:
- LB_GETTEXTLEN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1f76bf3574b09b76d5f1010dcb59c8245555dc3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119590"
---
# <a name="lb_gettextlen-message"></a>\_Messaggio GETTEXTLEN lb

Ottiene la lunghezza di una stringa in una casella di riepilogo.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice in base zero della stringa.

Windows 95/Windows 98/Windows Millennium Edition (Windows Me): il parametro *wParam* è limitato ai valori a 16 bit. Ciò significa che le caselle di riepilogo non possono contenere più di 32.767 elementi. Sebbene il numero di elementi sia limitato, le dimensioni totali in byte degli elementi in una casella di riepilogo sono limitate solo dalla memoria disponibile.

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è la lunghezza della stringa, in **TCHAR** s, escluso il carattere null di terminazione. In determinate condizioni, questo valore può essere effettivamente maggiore della lunghezza del testo. Per ulteriori informazioni, vedere la sezione Osservazioni successiva.

Se il parametro *wParam* non specifica un indice valido, il valore restituito è lb \_ Err.

## <a name="remarks"></a>Commenti

In determinate condizioni, il valore restituito è maggiore della lunghezza effettiva del testo. Questa situazione si verifica con determinate combinazioni di ANSI e Unicode ed è dovuta al sistema operativo che consente la possibile esistenza di caratteri DBCS (Double-byte character set) all'interno del testo. Il valore restituito, tuttavia, sarà sempre almeno uguale alla lunghezza effettiva del testo; è pertanto possibile utilizzarlo sempre per guidare l'allocazione del buffer. Questo comportamento può verificarsi quando un'applicazione utilizza funzioni ANSI e finestre di dialogo comuni che utilizzano Unicode.

Per ottenere la lunghezza esatta del testo, usare i messaggi [**WM \_ gettext**](/windows/desktop/winmsg/wm-gettext), [**lb \_ gettext**](lb-gettext.md)o [**CB \_ GETLBTEXT**](cb-getlbtext.md) oppure la funzione [**GetWindowText**](/windows/desktop/api/winuser/nf-winuser-getwindowtexta) .

Se la casella di riepilogo ha uno stile disegnato dal proprietario, ma non lo stile [**\_ HASSTRINGS lbs**](list-box-styles.md) , il valore restituito è sempre la dimensione, in byte, di un valore **DWORD**.

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

[**CB \_ GETLBTEXT**](cb-getlbtext.md)
</dt> <dt>

[**GetText LB \_**](lb-gettext.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[**GetWindowText**](/windows/desktop/api/winuser/nf-winuser-getwindowtexta)
</dt> <dt>

[**WM \_ GETtext**](/windows/desktop/winmsg/wm-gettext)
</dt> </dl>

 

