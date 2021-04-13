---
title: Messaggio di WM_DDE_UNADVISE (DDE. h)
description: Un'applicazione client di Dynamic Data Exchange (DDE) Invia un \_ \_ messaggio di avviso DDE di WM per informare un'applicazione server DDE che l'elemento specificato o un particolare formato degli Appunti per l'elemento non deve più essere aggiornato.
ms.assetid: 9a5f9a86-e6fa-450e-b8bf-f20042c7e6d1
keywords:
- Scambio di dati del messaggio WM_DDE_UNADVISE
topic_type:
- apiref
api_name:
- WM_DDE_UNADVISE
api_location:
- Dde.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dba83badcb689789d2654d99780bcb8cc503511d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478305"
---
# <a name="wm_dde_unadvise-message"></a>\_ \_ Messaggio Unadvise DDE WM

Un'applicazione client di Dynamic Data Exchange (DDE) Invia un messaggio di avviso **\_ \_ DDE di WM** per informare un'applicazione server DDE che l'elemento specificato o un particolare formato degli Appunti per l'elemento non deve più essere aggiornato. Questa operazione interrompe il collegamento dati caldo o attivo per l'elemento specificato.

Per pubblicare questo messaggio, chiamare la funzione [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) con i parametri seguenti.


```C++
#define WM_DDE_UNADVISE        0x03E3
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Handle per la finestra client che invia il messaggio.

</dd> <dt>

*lParam* 
</dt> <dd>

La parola di ordine inferiore specifica il formato degli Appunti dell'elemento per il quale la richiesta di aggiornamento viene ritratta. Se il **valore è null**, tutte le conversazioni di [**\_ \_ notifica del DDE di WM**](wm-dde-advise.md) attive per l'elemento devono essere terminate.

La parola più ordinata contiene un Atom globale che identifica l'elemento per il quale viene ritratta la richiesta di aggiornamento. Se è **null**, tutti i collegamenti [**di \_ \_ avviso DDE di WM**](wm-dde-advise.md) attivi associati alla conversazione devono essere interrotti.

</dd> </dl>

## <a name="remarks"></a>Commenti

L'applicazione client alloca la parola più ordinata di *lParam* chiamando la funzione [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) .

L'applicazione server inserisce il [**messaggio \_ \_ ACK DDE di WM**](wm-dde-ack.md) per rispondere in modo positivo o negativo. Quando si invia un **\_ \_ ACK DDE di WM**, il server può riutilizzare il formato Atom o eliminare l'Atom e crearne uno nuovo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                 |
| Intestazione<br/>                   | <dl> <dt>DDE. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma)
</dt> <dt>

[**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam)
</dt> <dt>

[**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam)
</dt> <dt>

[**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[**UnpackDDElParam**](/windows/desktop/api/Dde/nf-dde-unpackddelparam)
</dt> <dt>

[**\_ACK DDE \_ WM**](wm-dde-ack.md)
</dt> <dt>

[**\_avviso DDE di WM \_**](wm-dde-advise.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Informazioni su Dynamic Data Exchange](about-dynamic-data-exchange.md)
</dt> </dl>

 

