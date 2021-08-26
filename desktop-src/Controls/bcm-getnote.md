---
title: BCM_GETNOTE messaggio (Commctrl.h)
description: Ottiene il testo della nota associata a un pulsante di collegamento al comando. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro Button GetNote.
ms.assetid: ddaf4227-1316-49b5-abf0-00215472c46c
keywords:
- BCM_GETNOTE del messaggio Windows controlli
topic_type:
- apiref
api_name:
- BCM_GETNOTE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55b552f79e1d6c7bda2808b99701ff11e45deb169232b8bb52c4ecf231cdcbfd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119921701"
---
# <a name="bcm_getnote-message"></a>Messaggio GETNOTE di BCM \_

Ottiene il testo della nota associata a un pulsante di collegamento al comando. È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ Button GetNote.**](/windows/desktop/api/Commctrl/nf-commctrl-button_getnote)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* \[ in, out\]
</dt> <dd>

Valore **DWORD** che specifica le dimensioni del buffer a cui punta *lParam,* in caratteri.

</dd> <dt>

*lParam* \[ Cambio\]
</dt> <dd>

Buffer di stringhe per ricevere il testo. Le dimensioni del buffer devono essere sufficienti per contenere il carattere NULL di terminazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il messaggio ha esito positivo, restituisce **TRUE.** In caso contrario, **restituisce FALSE.**

## <a name="remarks"></a>Commenti

Il **messaggio \_ BCM GETNOTE** funziona solo con i pulsanti con lo stile [**BS \_ COMMANDLINK**](button-styles.md) o [**BS \_ DEFCOMMANDLINK.**](button-styles.md)

[**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) conterrà:

-   ERRORE NON SUPPORTATO, se il pulsante non ha lo stile \_ \_ [**\_ BS DEFCOMMANDLINK**](button-styles.md) o [**BS \_ COMMANDLINK.**](button-styles.md)
-   ERRORE \_ INSUFFICIENT \_ BUFFER, se il buffer *lParam* è troppo piccolo. Il *parametro wParam* conterrà le dimensioni del buffer richieste, in caratteri.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[Stili dei pulsanti](button-styles.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Tipi di pulsante](button-types-and-styles.md)
</dt> </dl>

 

