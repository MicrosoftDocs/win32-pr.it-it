---
description: Il server pipe specifica la modalità del tipo di pipe, la modalità di lettura e la modalità di attesa nel parametro dwPipeMode della funzione CreateNamedPipe. I client pipe possono specificare queste modalità di pipe per i rispettivi handle di pipe utilizzando la funzione CreateFile.
ms.assetid: 07cf9d06-6265-47f4-a9f1-c19c06cc5f9f
title: Tipo di named pipe, modalità lettura e attesa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b116e5ca9357a65a6d63549b96065843b046d479
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878565"
---
# <a name="named-pipe-type-read-and-wait-modes"></a>Tipo di named pipe, modalità lettura e attesa

Il server pipe specifica la modalità del tipo di pipe, la modalità di lettura e la modalità di attesa nel parametro *dwPipeMode* della funzione [**CreateNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea) . I client pipe possono specificare queste modalità di pipe per i rispettivi handle di pipe utilizzando la funzione [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) .

## <a name="type-mode"></a>Modalità tipo

La modalità del tipo di una pipe determina il modo in cui i dati vengono scritti in un named pipe. I dati possono essere trasmessi tramite un named pipe come un flusso di byte o come flusso di messaggi. Il server pipe specifica il tipo di pipe quando si chiama [**CreateNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea) per creare un'istanza di un named pipe. Le modalità del tipo devono essere le stesse per tutte le istanze di una pipe.

Per creare una pipe di tipo byte, specificare \_ il tipo di pipe \_ byte o usare il valore predefinito. I dati vengono scritti sulla pipe come un flusso di byte e il sistema non distingue i byte scritti in operazioni di scrittura diverse.

Per creare una pipe del tipo di messaggio, specificare il messaggio del tipo di PIPE \_ \_ . Il sistema considera i byte scritti in ogni operazione di scrittura sulla pipe come unità di messaggio. Il sistema esegue sempre operazioni di scrittura sulle pipe del tipo di messaggio come se fosse abilitata la modalità Write-through.

## <a name="read-mode"></a>Modalità lettura

La modalità di lettura di una pipe determina il modo in cui i dati vengono letti da un named pipe. Il server pipe specifica la modalità di lettura iniziale per un handle di pipe quando si chiama [**CreateNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea). I dati possono essere letti in modalità lettura byte o in modalità lettura messaggio. Un handle per una pipe di tipo byte può essere solo in modalità di lettura byte. Un handle per una pipe di tipo messaggio può essere in modalità lettura byte o lettura messaggio. Per una pipe di tipo messaggio, la modalità di lettura può essere diversa per gli handle server e client per la stessa istanza di pipe.

Per creare l'handle della pipe in modalità di lettura byte, specificare PIPE \_ READMODE \_ byte o usare il valore predefinito. I dati vengono letti dalla pipe come un flusso di byte. Un'operazione di lettura viene completata correttamente quando vengono letti tutti i byte disponibili nella pipe o quando viene letto il numero di byte specificato.

Per creare l'handle della pipe in modalità di lettura del messaggio, \_ specificare \_ Message READMODE pipe. I dati vengono letti dalla pipe come un flusso di messaggi. Un'operazione di lettura viene completata correttamente solo quando viene letto l'intero messaggio. Se il numero specificato di byte da leggere è inferiore alla dimensione del messaggio successivo, la funzione legge il maggior numero possibile di messaggi prima di restituire zero (la funzione [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce l'errore \_ più \_ dati). Il resto del messaggio può essere letto usando un'altra operazione di lettura.

Per un client pipe, un handle di pipe restituito da [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) è sempre in modalità di lettura byte inizialmente. Sia i client pipe che i server pipe possono utilizzare la funzione [**SetNamedPipeHandleState**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-setnamedpipehandlestate) per modificare la modalità di lettura di un handle di pipe. L'handle della pipe deve avere il \_ diritto di accesso con attributi di scrittura file \_ .

## <a name="wait-mode"></a>Modalità di attesa

La modalità di attesa di un handle di pipe determina il modo in cui le funzioni [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile), [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile)e [**ConnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe) gestiscono le operazioni di lunga durata. In modalità di blocco-attesa, le funzioni attendono indefinitamente che un processo sull'altra estremità della pipe per completare un'operazione. In modalità di attesa non di blocco, le funzioni restituiscono immediatamente in situazioni che altrimenti richiederebbero un'attesa indefinita.

Un'operazione [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) è interessata dalla modalità di attesa di un handle di pipe quando la pipe è vuota. Con un handle di attesa di blocco, l'operazione non viene completata correttamente fino a quando i dati non sono disponibili da un thread che scrive sull'altra estremità della pipe. Utilizzando un handle di attesa non di blocco, la funzione restituisce immediatamente zero e la funzione [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce l'errore \_ nessun \_ dato.

Un'operazione [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) è interessata dalla modalità di attesa di un handle di pipe quando lo spazio nel buffer della pipe non è sufficiente. Con un handle di attesa di blocco, l'operazione di scrittura non può avere esito positivo finché non viene creato spazio sufficiente nel buffer da parte di un thread che legge dall'altra estremità della pipe. Con un handle di attesa non di blocco, l'operazione di scrittura restituisce immediatamente un valore diverso da zero, senza scrivere alcun byte (per una pipe del tipo di messaggio) o dopo la scrittura di un numero di byte pari al buffer (per una pipe di tipo byte).

Un'operazione [**ConnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe) è interessata dalla modalità di attesa di un handle di pipe quando non è presente alcun client connesso o in attesa di connettersi all'istanza di pipe. Con un handle di attesa di blocco, l'operazione di connessione non riesce fino a quando un client pipe si connette all'istanza della pipe chiamando la funzione [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) o [**CallNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea) . Con un handle di attesa non di blocco, l'operazione di connessione restituisce immediatamente zero e la funzione [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce la pipe di errore in \_ \_ ascolto.

Per impostazione predefinita, tutti gli handle di named pipe restituiti dalla funzione [**CreateNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea) o [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) vengono creati con la modalità di attesa blocco abilitata. Per creare la pipe in modalità di attesa non di blocco, il server pipe specifica la PIPE \_ nowait quando si chiama **CreateNamedPipe**.

Sia i client pipe che i server pipe possono modificare la modalità di attesa di un handle di pipe specificando \_ la pipe Wait o pipe \_ nowait in una chiamata alla funzione [**SetNamedPipeHandleState**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-setnamedpipehandlestate) .

> [!Note]  
> La modalità di attesa non di blocco è supportata per la compatibilità con Microsoft LAN Manager versione 2,0. Questa modalità non deve essere utilizzata per ottenere l'input e l'output sovrapposti (I/O) con named pipe. In alternativa, è necessario utilizzare l'I/O sovrapposto perché consente di eseguire operazioni che richiedono molto tempo in background dopo la restituzione della funzione. Per ulteriori informazioni sull'I/O sovrapposto, vedere [input e output sincroni e sovrapposti](synchronous-and-overlapped-input-and-output.md).

 

 

 
