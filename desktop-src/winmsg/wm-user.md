---
description: Usato per definire i messaggi privati per l'uso da parte di classi di finestre private, in genere nel formato WM \_ USER+x, dove x è un valore intero.
ms.assetid: 4115c587-fcb4-4170-9948-fe33bcb8742a
title: WM_USER (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1cb14e8ef69ae35cedd4e246f253aa7b3c16451623eb7043774d1f0940cb64f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119705731"
---
# <a name="wm_user"></a>UTENTE \_ WM

Usato per definire i messaggi privati per l'uso da parte di classi di finestre private, in genere nel formato **WM \_ USER** + *x*, dove *x* è un valore intero.

``` syntax
#define WM_USER                         0x0400
```

## <a name="remarks"></a>Commenti

Di seguito sono riportati gli intervalli di numeri di messaggio.



| Intervallo                                                        | Significato                                                        |
|--------------------------------------------------------------|----------------------------------------------------------------|
| Da 0 a **WM \_ USER** -1<br/>                         | Messaggi riservati per l'uso da parte del sistema.<br/>            |
| **WM \_ DA UTENTE** a 0x7FFF<br/>                       | Messaggi interi per l'uso da parte di classi di finestre private.<br/> |
| [**WM \_ DA APP**](wm-app.md) (0x8000) a 0xBFFF<br/> | Messaggi disponibili per l'uso da parte delle applicazioni.<br/>         |
| 0xC000 a 0xFFFF<br/>                             | Messaggi stringa per l'uso da parte delle applicazioni.<br/>            |
| Maggiore di 0xFFFF<br/>                               | Riservato dal sistema.<br/>                             |



 

I numeri di messaggio nel primo intervallo (da 0 a **WM \_ USER** -1) sono definiti dal sistema. I valori in questo intervallo non definiti in modo esplicito vengono riservati dal sistema.

I numeri di messaggio nel secondo intervallo **(da WM \_ USER** a 0x7FFF) possono essere definiti e usati da un'applicazione per inviare messaggi all'interno di una classe di finestra privata. Questi valori non possono essere usati per definire messaggi significativi in un'applicazione perché alcune classi di finestre predefinite definiscono già valori in questo intervallo. Ad esempio, le classi di controllo predefinite come **BUTTON,** **EDIT,** **LISTBOX** e **COMBOBOX** possono usare questi valori. I messaggi in questo intervallo non devono essere inviati ad altre applicazioni, a meno che le applicazioni non siano state progettate per scambiare messaggi e allegare lo stesso significato ai numeri di messaggio.

I numeri di messaggio nel terzo intervallo (da 0x8000 a 0xBFFF) sono disponibili per le applicazioni da usare come messaggi privati. I messaggi in questo intervallo non sono in conflitto con i messaggi di sistema.

I numeri di messaggio nel quarto intervallo (da 0xC000 a 0xFFFF) vengono definiti in fase di esecuzione quando un'applicazione chiama la funzione [**RegisterWindowMessage**](/windows/win32/api/winuser/nf-winuser-registerwindowmessagea) per recuperare un numero di messaggio per una stringa. Tutte le applicazioni che registrano la stessa stringa possono usare il numero di messaggio associato per lo scambio di messaggi. Il numero di messaggio effettivo, tuttavia, non è una costante e non può essere considerato lo stesso tra sessioni diverse.

I numeri di messaggio nel quinto intervallo (maggiore 0xFFFF) sono riservati dal sistema.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**RegisterWindowMessage**](/windows/win32/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

[**WM \_ APP**](wm-app.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Messaggi e code di messaggi](messages-and-message-queues.md)
</dt> </dl>

 

 
