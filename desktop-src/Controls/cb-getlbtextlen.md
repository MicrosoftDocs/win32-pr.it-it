---
title: Messaggio CB_GETLBTEXTLEN (winuser. h)
description: Ottiene la lunghezza, in caratteri, di una stringa nell'elenco di una casella combinata.
ms.assetid: f0fe0eef-f9db-4d9f-9a42-5bb2aeae30a0
keywords:
- Controlli di Windows Message CB_GETLBTEXTLEN
topic_type:
- apiref
api_name:
- CB_GETLBTEXTLEN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e42dc19b13b22f577fcc21bb32cb8810bab29be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964205"
---
# <a name="cb_getlbtextlen-message"></a>\_Messaggio GETLBTEXTLEN CB

Ottiene la lunghezza, in caratteri, di una stringa nell'elenco di una casella combinata.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice in base zero della stringa.

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è la lunghezza della stringa, in **TCHAR** s, escluso il carattere null di terminazione. Se una stringa ANSI è il numero di byte e se si tratta di una stringa Unicode, si tratta del numero di caratteri. In determinate condizioni, questo valore può essere effettivamente maggiore della lunghezza del testo. Per altre informazioni, vedere la sezione Osservazioni.

Se il parametro *wParam* non specifica un indice valido, il valore restituito è CB \_ Err.

## <a name="remarks"></a>Commenti

In determinate condizioni, il valore restituito è maggiore della lunghezza effettiva del testo. Questa situazione si verifica con determinate combinazioni di ANSI e Unicode ed è dovuta al sistema operativo che consente la possibile esistenza di caratteri DBCS (Double-byte character set) all'interno del testo. Il valore restituito, tuttavia, sarà sempre almeno uguale alla lunghezza effettiva del testo; quindi, è sempre possibile usarlo per guidare l'allocazione del buffer. Questo comportamento può verificarsi quando un'applicazione utilizza funzioni ANSI e finestre di dialogo comuni che utilizzano Unicode.

Per ottenere la lunghezza esatta del testo, usare i messaggi [**WM \_ gettext**](/windows/desktop/winmsg/wm-gettext), [**lb \_ gettext**](lb-gettext.md)o [**CB \_ GETLBTEXT**](cb-getlbtext.md) oppure la funzione [**GetWindowText**](/windows/desktop/api/winuser/nf-winuser-getwindowtexta) .

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

 

