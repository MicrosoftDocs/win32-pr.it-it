---
title: Elaborare la connessione a una stazione di finestra
description: Un processo stabilisce automaticamente una connessione a una stazione e a un desktop della finestra quando chiama per la prima volta una funzione USER32 o GDI32 (diversa dalle funzioni di Window Station e desktop).
ms.assetid: 280f69e7-5c99-41a7-94e3-da13deaac9f5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a87e97b19ac1210b04447652268c5f53b7e2a6d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399445"
---
# <a name="process-connection-to-a-window-station"></a>Elaborare la connessione a una stazione di finestra

Un processo stabilisce automaticamente una connessione a una stazione e a un desktop della finestra quando chiama per la prima volta una funzione USER32 o GDI32 (diversa dalle funzioni di Window Station e desktop). Il sistema determina la stazione della finestra a cui un processo si connette in base alle regole seguenti:

1.  Se il processo ha chiamato la funzione [**SetProcessWindowStation**](/windows/win32/api/winuser/nf-winuser-setprocesswindowstation) , si connette alla stazione della finestra specificata nella chiamata.
2.  Se il processo non ha chiamato [**SetProcessWindowStation**](/windows/win32/api/winuser/nf-winuser-setprocesswindowstation), si connette alla stazione della finestra ereditata dal processo padre.
3.  Se il processo non ha chiamato [**SetProcessWindowStation**](/windows/win32/api/winuser/nf-winuser-setprocesswindowstation) e non ha ereditato una stazione di finestra, il sistema tenta di aprire per l' \_ accesso massimo consentito e si connette a una finestra di Windows come indicato di seguito:
    -   Se è stato specificato un nome di stazione della finestra nel membro **lpDesktop** della struttura [**STARTUPINFO**](/windows/desktop/api/processthreadsapi/ns-processthreadsapi-startupinfoa) usata al momento della creazione del processo, il processo si connette alla stazione della finestra specificata.
    -   In caso contrario, se il processo è in esecuzione nella sessione di accesso dell'utente interattivo, il processo si connette alla stazione finestra interattiva.
    -   Se il processo è in esecuzione in una sessione di accesso non interattiva, il nome della stazione della finestra viene formato in base all'identificatore della sessione di accesso e viene effettuato un tentativo di aprire tale stazione. Se l'operazione di apertura ha esito negativo perché questa finestra non esiste, il sistema tenta di creare la stazione di finestra e un desktop predefinito.

La stazione della finestra assegnata durante questo processo di connessione non può essere chiusa chiamando la funzione [**CloseWindowStation**](/windows/win32/api/winuser/nf-winuser-closewindowstation) .

Quando un processo si connette a una stazione di finestra, il sistema esegue una ricerca nella tabella di handle del processo per gli handle ereditati. Il sistema usa il primo handle della stazione di finestra individuato. Se si vuole che un processo figlio si connetta a una particolare finestra di Windows ereditata, è necessario assicurarsi che solo l'handle desiderato sia contrassegnato come ereditabile. Se un processo figlio eredita più handle della stazione della finestra, i risultati della connessione alla stazione della finestra non sono definiti.

Gli handle a una stazione della finestra visualizzata dal sistema durante la connessione di un processo a una stazione della finestra non sono ereditabili.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Connessione thread a un desktop](thread-connection-to-a-desktop.md)
</dt> </dl>

 

 