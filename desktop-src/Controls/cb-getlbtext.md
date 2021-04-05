---
title: Messaggio CB_GETLBTEXT (winuser. h)
description: Ottiene una stringa dall'elenco di una casella combinata.
ms.assetid: f84e302a-65bb-45c8-958b-1cb438fb5a7a
keywords:
- Controlli di Windows Message CB_GETLBTEXT
topic_type:
- apiref
api_name:
- CB_GETLBTEXT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d26a964b463daedab1ad5d9f50888b3e0c1e0db
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048357"
---
# <a name="cb_getlbtext-message"></a>\_Messaggio GETLBTEXT CB

Ottiene una stringa dall'elenco di una casella combinata.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice in base zero della stringa da recuperare.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore al buffer che riceve la stringa. Il buffer deve contenere spazio sufficiente per la stringa e un carattere null di terminazione. È possibile inviare un messaggio [**CB \_ GETLBTEXTLEN**](cb-getlbtextlen.md) prima del messaggio **CB \_ GETLBTEXT** per recuperare la lunghezza, in **TCHAR** s, della stringa. Se è una stringa ANSI, questo è il numero di byte, ma se è una stringa Unicode questo è il numero di caratteri.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è la lunghezza della stringa, in **TCHAR** s, escluso il carattere null di terminazione. Se *wParam* non specifica un indice valido, il valore restituito è CB \_ Err.

## <a name="remarks"></a>Commenti

**Avviso di sicurezza:** L'uso errato di questo messaggio può compromettere la sicurezza del programma. Questo messaggio non fornisce un modo per stabilire le dimensioni del buffer. Se si utilizza questo messaggio, chiamare prima [**CB \_ GETLBTEXTLEN**](cb-getlbtextlen.md) per ottenere il numero di caratteri necessari e quindi chiamare il messaggio per recuperare la stringa. Prima di continuare, è necessario esaminare le [considerazioni sulla sicurezza: controlli di Microsoft Windows](sec-comctls.md) .

Se si crea la casella combinata con uno stile disegnato dal proprietario ma senza lo stile [**CBS \_ HASSTRINGS**](combo-box-styles.md) , il buffer a cui punta *lParam* riceve i dati associati all'elemento.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CB \_ GETLBTEXTLEN**](cb-getlbtextlen.md)
</dt> </dl>

 

 





