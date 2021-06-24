---
description: Usato per definire messaggi privati per l'uso da parte di classi di finestre private, in genere nel formato OCM \_ \_ BASE+x, dove x è un valore intero.
ms.assetid: b1a9c0ca-349d-49d2-9b8b-ae7d3bf94c10
title: OCM__BASE (Olectl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa3713d8a7b7447430e914e2582089244a417b1c
ms.sourcegitcommit: 749dea42142dec076d41a8f26cb57ae8db46e848
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/24/2021
ms.locfileid: "112588056"
---
# <a name="ocm__base"></a>OCM \_ \_ BASE

Usato per definire i messaggi privati per l'uso da parte di classi di finestre private, in genere nel formato **OCM \_ \_ BASE** + *x*, dove *x* è un valore intero.

``` syntax
#define WM_USER                   0x0400
#define OCM__BASE                (WM_USER+0x1c00)
```

## <a name="remarks"></a>Commenti

Di seguito sono riportati gli intervalli di numeri di messaggio.



| Intervallo                                                 | Significato                                                        |
|-------------------------------------------------------|----------------------------------------------------------------|
| Da 0 a [**WM \_ USER**](wm-user.md)-1<br/>   | Messaggi riservati per l'utilizzo da parte del sistema.<br/>            |
| [**WM \_ DA UTENTE**](wm-user.md) a 0x7FFF<br/> | Messaggi interi che possono essere utilizzati da classi di finestre private.<br/> |
| [**WM \_ Da APP**](wm-app.md) a 0xBFFF<br/>   | Messaggi disponibili per l'utilizzo da parte delle applicazioni.<br/>         |
| 0xC000 a 0xFFFF<br/>                      | Messaggi stringa che possono essere utilizzati dalle applicazioni.<br/>            |
| Maggiore di 0xFFFF<br/>                        | Riservato dal sistema.<br/>                             |



 

I numeri di messaggio nel primo intervallo (da 0 a [**WM \_ USER**](wm-user.md)  1) sono definiti dal sistema. I valori in questo intervallo non definiti in modo esplicito sono riservati dal sistema.

I numeri di messaggio nel secondo intervallo [**(da WM \_ USER**](wm-user.md) a 0x7FFF) possono essere definiti e usati da un'applicazione per inviare messaggi all'interno di una classe di finestra privata. Questi valori non possono essere usati per definire messaggi significativi in un'applicazione perché alcune classi di finestre predefinite definiscono già valori in questo intervallo. Ad esempio, le classi di controllo predefinite come **BUTTON,** **EDIT,** **LISTBOX** e **COMBOBOX** possono usare questi valori. I messaggi in questo intervallo non devono essere inviati ad altre applicazioni a meno che le applicazioni non siano state progettate per scambiare messaggi e allegare lo stesso significato ai numeri di messaggio.

I numeri di messaggio nel terzo intervallo (da 0x8000 a 0xBFFF) sono disponibili per le applicazioni da usare come messaggi privati. I messaggi in questo intervallo non sono in conflitto con i messaggi di sistema.

I numeri di messaggio nel quarto intervallo (da 0xC000 a 0xFFFF) vengono definiti in fase di esecuzione quando un'applicazione chiama la funzione [**RegisterWindowMessage**](/windows/win32/api/winuser/nf-winuser-registerwindowmessagea) per recuperare un numero di messaggio per una stringa. Tutte le applicazioni che registrano la stessa stringa possono usare il numero di messaggio associato per lo scambio di messaggi. Il numero di messaggio effettivo, tuttavia, non è una costante e non può essere considerato lo stesso tra sessioni diverse.

I numeri di messaggio nel quinto intervallo (maggiore 0xFFFF) sono riservati dal sistema.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Olectl.h</dt> </dl> |



## <a name="see-also"></a>Vedere anche

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

 

