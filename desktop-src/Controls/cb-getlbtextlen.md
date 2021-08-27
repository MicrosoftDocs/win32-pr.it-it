---
title: CB_GETLBTEXTLEN messaggio (Winuser.h)
description: Ottiene la lunghezza, in caratteri, di una stringa nell'elenco di una casella combinata.
ms.assetid: f0fe0eef-f9db-4d9f-9a42-5bb2aeae30a0
keywords:
- CB_GETLBTEXTLEN controlli Windows messaggio
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
ms.openlocfilehash: cb226a9012d9573e17bd88a114ebcd2b96e406a38208cc78a925bdca976cd4b6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089151"
---
# <a name="cb_getlbtextlen-message"></a>Messaggio CB \_ GETLBTEXTLEN

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

Il valore restituito è la lunghezza della stringa, in **TCHAR** s, escluso il carattere Null di terminazione. Se una stringa ANSI è il numero di byte e se si tratta di una stringa Unicode, si tratta del numero di caratteri. In determinate condizioni, questo valore può essere effettivamente maggiore della lunghezza del testo. Per altre informazioni, vedere la sezione Osservazioni.

Se il *parametro wParam* non specifica un indice valido, il valore restituito è CB \_ ERR.

## <a name="remarks"></a>Commenti

In determinate condizioni, il valore restituito è maggiore della lunghezza effettiva del testo. Ciò si verifica con determinate combinazioni di ANSI e Unicode ed è dovuto al sistema operativo che consente la possibile esistenza di caratteri DBCS (Double Byte Character Set) all'interno del testo. Il valore restituito, tuttavia, sarà sempre almeno quanto la lunghezza effettiva del testo. in modo che sia sempre possibile usarlo per guidare l'allocazione del buffer. Questo comportamento può verificarsi quando un'applicazione utilizza funzioni ANSI e dialoghe comuni, che usano Unicode.

Per ottenere la lunghezza esatta del testo, usare i messaggi [**WM \_ GETTEXT**](/windows/desktop/winmsg/wm-gettext), [**LB \_ GETTEXT**](lb-gettext.md)o [**\_ CB GETLBTEXT**](cb-getlbtext.md) o la [**funzione GetWindowText.**](/windows/desktop/api/winuser/nf-winuser-getwindowtexta)

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

[**CB \_ GETLBTEXT**](cb-getlbtext.md)
</dt> <dt>

[**LB \_ GETTEXT**](lb-gettext.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[**GetWindowText**](/windows/desktop/api/winuser/nf-winuser-getwindowtexta)
</dt> <dt>

[**WM \_ GETTEXT**](/windows/desktop/winmsg/wm-gettext)
</dt> </dl>

 

