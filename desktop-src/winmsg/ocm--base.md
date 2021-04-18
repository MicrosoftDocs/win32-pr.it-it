---
description: Utilizzato per definire i messaggi privati per l'utilizzo da parte delle classi della finestra privata, in genere nel formato OCM \_ \_ base + x, dove x è un valore intero.
ms.assetid: b1a9c0ca-349d-49d2-9b8b-ae7d3bf94c10
title: OCM__BASE (olectl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1bc79cc842a7f25ba66dc8d807c5ab355fc04547
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312493"
---
# <a name="ocm__base"></a>\_ \_ base OCM

Utilizzato per definire i messaggi privati per l'utilizzo da parte delle classi della finestra privata, in genere nel formato **OCM \_ \_ base** + *x*, dove *x* è un valore intero.

``` syntax
#define WM_USER                   0x0400
#define OCM__BASE                (WM_USER+0x1c00)
```

## <a name="remarks"></a>Commenti

Di seguito sono riportati gli intervalli dei numeri di messaggio.



| Range                                                 | Significato                                                        |
|-------------------------------------------------------|----------------------------------------------------------------|
| da 0 a [**WM \_ utente**](wm-user.md)  1<br/>   | Messaggi riservati per l'utilizzo da parte del sistema.<br/>            |
| [**WM \_ UTENTE**](wm-user.md) tramite 0x7FFF<br/> | Messaggi integer utilizzati dalle classi della finestra privata.<br/> |
| [**WM \_ Da APP**](wm-app.md) a 0xBFFF<br/>   | Messaggi disponibili per l'utilizzo da applicazioni.<br/>         |
| da 0xC000 a 0xFFFF<br/>                      | Messaggi stringa da utilizzare per le applicazioni.<br/>            |
| Maggiore di 0xFFFF<br/>                        | Riservato dal sistema.<br/>                             |



 

I numeri dei messaggi nel primo intervallo (da 0 a [**WM \_ utente**](wm-user.md)  1) sono definiti dal sistema. I valori in questo intervallo che non sono definiti in modo esplicito sono riservati dal sistema.

I numeri dei messaggi nel secondo intervallo [**( \_ utente WM**](wm-user.md) tramite 0x7FFF) possono essere definiti e usati da un'applicazione per inviare messaggi all'interno di una classe di finestra privata. Questi valori non possono essere usati per definire messaggi significativi in un'applicazione, perché alcune classi finestra predefinite definiscono già i valori in questo intervallo. Ad esempio, le classi di controlli predefinite come **Button**, **Edit**, **ListBox** e **ComboBox** possono usare questi valori. I messaggi in questo intervallo non devono essere inviati ad altre applicazioni, a meno che le applicazioni non siano state progettate per scambiare messaggi e allineare lo stesso significato ai numeri dei messaggi.

I numeri dei messaggi nel terzo intervallo (da 0x8000 a 0xBFFF) sono disponibili per le applicazioni da utilizzare come messaggi privati. I messaggi in questo intervallo non sono in conflitto con i messaggi di sistema.

I numeri dei messaggi nel quarto intervallo (da 0xC000 a 0xFFFF) vengono definiti in fase di esecuzione quando un'applicazione chiama la funzione [**RegisterWindowMessage**](/windows/win32/api/winuser/nf-winuser-registerwindowmessagea) per recuperare un numero di messaggio per una stringa. Per tutte le applicazioni che registrano la stessa stringa è possibile utilizzare il numero di messaggio associato per lo scambio di messaggi. Il numero effettivo del messaggio, tuttavia, non è una costante e non può essere considerato lo stesso tra sessioni diverse.

I numeri dei messaggi nel quinto intervallo (maggiore di 0xFFFF) sono riservati dal sistema.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Olectl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**RegisterWindowMessage**](/windows/win32/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

[**\_app WM**](wm-app.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Messaggi e code di messaggi](messages-and-message-queues.md)
</dt> </dl>

 

