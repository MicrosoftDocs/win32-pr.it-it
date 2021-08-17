---
description: Usato per definire messaggi privati, in genere nel formato WM \_ APP+x, dove x è un valore intero.
ms.assetid: fdb549df-426f-4af5-9c17-6e8730e4abc0
title: WM_APP (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01c2f09bef9ef479cfa5bd0bb56760fd17196087992276b2caa1daf7616fea9b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119931821"
---
# <a name="wm_app"></a>WM \_ APP

Usato per definire messaggi privati, in genere nel formato **WM \_ APP** + *x*, dove *x* è un valore intero.

``` syntax
#define WM_APP                          0x8000
```

## <a name="remarks"></a>Commenti

La **costante \_ WM APP** viene usata per distinguere tra i valori dei messaggi riservati per l'uso da parte del sistema e i valori che possono essere usati da un'applicazione per inviare messaggi all'interno di una classe di finestra privata. Di seguito sono riportati gli intervalli di numeri di messaggio disponibili.



| Intervallo                                                 | Significato                                                        |
|-------------------------------------------------------|----------------------------------------------------------------|
| Da 0 a [**WM \_ USER**](wm-user.md) -1<br/>   | Messaggi riservati per l'utilizzo da parte del sistema.<br/>            |
| [**WM \_ DA UTENTE**](wm-user.md) a 0x7FFF<br/> | Messaggi interi che possono essere utilizzati da classi di finestre private.<br/> |
| **WM \_ Da APP** a 0xBFFF<br/>                 | Messaggi disponibili per l'uso da parte delle applicazioni.<br/>         |
| 0xC000 tramite 0xFFFF<br/>                      | Messaggi stringa che possono essere utilizzati dalle applicazioni.<br/>            |
| Maggiore di 0xFFFF<br/>                        | Riservato dal sistema.<br/>                             |



 

I numeri di messaggio nel primo intervallo (da 0 a [**WM \_ USER**](wm-user.md) -1) sono definiti dal sistema. I valori in questo intervallo non definiti in modo esplicito sono riservati dal sistema.

I numeri di messaggio nel secondo intervallo [**(da WM \_ USER**](wm-user.md) a 0x7FFF) possono essere definiti e usati da un'applicazione per inviare messaggi all'interno di una classe di finestra privata. Questi valori non possono essere usati per definire messaggi significativi in un'applicazione perché alcune classi di finestre predefinite definiscono già valori in questo intervallo. Ad esempio, le classi di controllo predefinite come **BUTTON,** **EDIT,** **LISTBOX** e **COMBOBOX** possono usare questi valori. I messaggi in questo intervallo non devono essere inviati ad altre applicazioni a meno che le applicazioni non siano state progettate per scambiare messaggi e allegare lo stesso significato ai numeri di messaggio.

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

[**UTENTE \_ WM**](wm-user.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Messaggi e code di messaggi](messages-and-message-queues.md)
</dt> </dl>

 

 
