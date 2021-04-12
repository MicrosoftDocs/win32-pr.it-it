---
description: Utilizzato per definire i messaggi privati, in genere nel formato WM \_ app + x, dove x è un valore intero.
ms.assetid: fdb549df-426f-4af5-9c17-6e8730e4abc0
title: WM_APP (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4998f8240b08d248a75b375bb813ba02cd02344e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232467"
---
# <a name="wm_app"></a>\_app WM

Utilizzato per definire i messaggi privati, in genere nel formato **WM \_ app** + *x*, dove *x* è un valore intero.

``` syntax
#define WM_APP                          0x8000
```

## <a name="remarks"></a>Commenti

La costante dell' **\_ app WM** viene utilizzata per distinguere tra i valori del messaggio riservati per l'utilizzo da parte del sistema e i valori che possono essere utilizzati da un'applicazione per inviare messaggi all'interno di una classe di finestra privata. Di seguito sono riportati gli intervalli di numeri dei messaggi disponibili.



| Range                                                 | Significato                                                        |
|-------------------------------------------------------|----------------------------------------------------------------|
| da 0 [**a \_ utente WM**](wm-user.md) -1<br/>   | Messaggi riservati per l'utilizzo da parte del sistema.<br/>            |
| [**WM \_ UTENTE**](wm-user.md) tramite 0x7FFF<br/> | Messaggi integer utilizzati dalle classi della finestra privata.<br/> |
| **WM \_ Da APP** a 0xBFFF<br/>                 | Messaggi disponibili per l'utilizzo da applicazioni.<br/>         |
| da 0xC000 a 0xFFFF<br/>                      | Messaggi stringa da utilizzare per le applicazioni.<br/>            |
| Maggiore di 0xFFFF<br/>                        | Riservato dal sistema.<br/>                             |



 

I numeri dei messaggi nel primo intervallo (da 0 a [**WM \_ utente**](wm-user.md) -1) sono definiti dal sistema. I valori in questo intervallo che non sono definiti in modo esplicito sono riservati dal sistema.

I numeri dei messaggi nel secondo intervallo [**( \_ utente WM**](wm-user.md) tramite 0x7FFF) possono essere definiti e usati da un'applicazione per inviare messaggi all'interno di una classe di finestra privata. Questi valori non possono essere usati per definire messaggi significativi in un'applicazione, perché alcune classi finestra predefinite definiscono già i valori in questo intervallo. Ad esempio, le classi di controlli predefinite come **Button**, **Edit**, **ListBox** e **ComboBox** possono usare questi valori. I messaggi in questo intervallo non devono essere inviati ad altre applicazioni, a meno che le applicazioni non siano state progettate per scambiare messaggi e allineare lo stesso significato ai numeri dei messaggi.

I numeri dei messaggi nel terzo intervallo (da 0x8000 a 0xBFFF) sono disponibili per le applicazioni da utilizzare come messaggi privati. I messaggi in questo intervallo non sono in conflitto con i messaggi di sistema.

I numeri dei messaggi nel quarto intervallo (da 0xC000 a 0xFFFF) vengono definiti in fase di esecuzione quando un'applicazione chiama la funzione [**RegisterWindowMessage**](/windows/win32/api/winuser/nf-winuser-registerwindowmessagea) per recuperare un numero di messaggio per una stringa. Per tutte le applicazioni che registrano la stessa stringa è possibile utilizzare il numero di messaggio associato per lo scambio di messaggi. Il numero effettivo del messaggio, tuttavia, non è una costante e non può essere considerato lo stesso tra sessioni diverse.

I numeri dei messaggi nel quinto intervallo (maggiore di 0xFFFF) sono riservati dal sistema.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**RegisterWindowMessage**](/windows/win32/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

[**\_utente WM**](wm-user.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Messaggi e code di messaggi](messages-and-message-queues.md)
</dt> </dl>

 

 
