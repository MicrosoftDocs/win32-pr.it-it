---
title: Connessione thread a un desktop
description: Quando un processo si connette a una stazione di finestra, il sistema assegna un desktop al thread che effettua la connessione.
ms.assetid: 45016619-ed11-4b0c-84e3-f8662553c64d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a503390468ea5ed1771ece7a942a2d615ac6f0a9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104223921"
---
# <a name="thread-connection-to-a-desktop"></a>Connessione thread a un desktop

Quando un processo si connette a una stazione di finestra, il sistema assegna un desktop al thread che effettua la connessione. Il sistema determina il desktop da assegnare al thread in base alle regole seguenti:

1.  Se il thread ha chiamato la funzione [**SetThreadDesktop**](/windows/win32/api/winuser/nf-winuser-setthreaddesktop) , si connette al desktop specificato.
2.  Se il thread non ha chiamato [**SetThreadDesktop**](/windows/win32/api/winuser/nf-winuser-setthreaddesktop), si connette al desktop ereditato dal processo padre.
3.  Se il thread non ha chiamato [**SetThreadDesktop**](/windows/win32/api/winuser/nf-winuser-setthreaddesktop) e non ha ereditato un desktop, il sistema tenta di aprire per l' \_ accesso massimo consentito e si connette a un desktop come indicato di seguito:
    -   Se è stato specificato un nome desktop nel membro **lpDesktop** della struttura [**STARTUPINFO**](/windows/desktop/api/processthreadsapi/ns-processthreadsapi-startupinfoa) utilizzata al momento della creazione del processo, il thread si connette al desktop specificato.
    -   In caso contrario, il thread si connette al desktop predefinito della stazione della finestra a cui è connesso il processo.

Il desktop assegnato durante questo processo di connessione non può essere chiuso chiamando la funzione [**CloseDesktop**](/windows/win32/api/winuser/nf-winuser-closedesktop) .

Quando un processo si connette a un desktop, il sistema esegue una ricerca nella tabella di handle del processo per gli handle ereditati. Il sistema utilizza il primo handle desktop rilevato. Se si desidera che un processo figlio si connetta a un particolare desktop ereditato, è necessario assicurarsi che l'unico handle desiderato sia contrassegnato come ereditabile. Se un processo figlio eredita più handle desktop, i risultati della connessione desktop non saranno definiti.

Gli handle a un desktop aperto dal sistema durante la connessione di un processo a un desktop non sono ereditabili.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Elaborare la connessione a una stazione di finestra](process-connection-to-a-window-station.md)
</dt> </dl>

 

 