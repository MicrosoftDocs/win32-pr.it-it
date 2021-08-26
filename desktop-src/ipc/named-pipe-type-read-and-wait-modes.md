---
description: Il server pipe specifica la modalità del tipo di pipe, la modalità di lettura e la modalità di attesa nel parametro dwPipeMode della funzione CreateNamedPipe. I client pipe possono specificare queste modalità di pipe per gli handle di pipe usando la funzione CreateFile.
ms.assetid: 07cf9d06-6265-47f4-a9f1-c19c06cc5f9f
title: Modalità di attesa, lettura e tipo di named pipe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3b8ba69ef0d795747070072511c84abf5a3950db3b9c03ec18973f4d29bbd51
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014891"
---
# <a name="named-pipe-type-read-and-wait-modes"></a>Modalità di attesa, lettura e tipo di named pipe

Il server pipe specifica la modalità del tipo di pipe, la modalità di lettura e la modalità di attesa nel *parametro dwPipeMode* della [**funzione CreateNamedPipe.**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea) I client pipe possono specificare queste modalità di pipe per gli handle di pipe usando la [**funzione CreateFile.**](/windows/desktop/api/fileapi/nf-fileapi-createfilea)

## <a name="type-mode"></a>Modalità tipo

La modalità tipo di una pipe determina la modalità di scrittura dei dati in un named pipe. I dati possono essere trasmessi tramite un named pipe come flusso di byte o come flusso di messaggi. Il server pipe specifica il tipo di pipe quando si chiama [**CreateNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea) per creare un'istanza di un named pipe. Le modalità di tipo devono essere le stesse per tutte le istanze di una pipe.

Per creare una pipe di tipo byte, specificare PIPE \_ TYPE BYTE o usare il valore \_ predefinito. I dati vengono scritti nella pipe come flusso di byte e il sistema non distingue tra i byte scritti in diverse operazioni di scrittura.

Per creare una pipe di tipo messaggio, specificare PIPE \_ TYPE \_ MESSAGE. Il sistema considera i byte scritti in ogni operazione di scrittura nella pipe come unità messaggio. Il sistema esegue sempre operazioni di scrittura su pipe di tipo messaggio come se fosse abilitata la modalità write-through.

## <a name="read-mode"></a>Modalità di lettura

La modalità di lettura di una pipe determina la modalità di lettura dei dati da un named pipe. Il server pipe specifica la modalità di lettura iniziale per un handle di pipe quando si chiama [**CreateNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea). I dati possono essere letti in modalità di lettura byte o di lettura messaggi. Un handle per una pipe di tipo byte può essere solo in modalità di lettura byte. Un handle per una pipe di tipo messaggio può essere in modalità lettura byte o lettura messaggi. Per una pipe di tipo messaggio, la modalità di lettura può essere diversa per gli handle del server e del client per la stessa istanza della pipe.

Per creare l'handle della pipe in modalità di lettura byte, specificare PIPE \_ READMODE \_ BYTE o usare il valore predefinito. I dati vengono letti dalla pipe come flusso di byte. Un'operazione di lettura viene completata correttamente quando tutti i byte disponibili nella pipe vengono letti o quando viene letto il numero specificato di byte.

Per creare l'handle della pipe in modalità di lettura messaggi, specificare PIPE \_ READMODE \_ MESSAGE. I dati vengono letti dalla pipe come flusso di messaggi. Un'operazione di lettura viene completata correttamente solo quando viene letto l'intero messaggio. Se il numero specificato di byte da leggere è minore delle dimensioni del messaggio successivo, la funzione legge la maggior parte del messaggio possibile prima di restituire zero (la funzione [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce ERROR \_ MORE \_ DATA). Il resto del messaggio può essere letto usando un'altra operazione di lettura.

Per un client pipe, un handle di pipe restituito [**da CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) è sempre in modalità di lettura byte inizialmente. Sia i client pipe che i server pipe possono usare la [**funzione SetNamedPipeHandleState**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-setnamedpipehandlestate) per modificare la modalità di lettura di un handle di pipe. L'handle della pipe deve avere il diritto di accesso FILE \_ WRITE \_ ATTRIBUTES.

## <a name="wait-mode"></a>Modalità di attesa

La modalità di attesa di un handle di pipe determina il modo in cui le [**funzioni ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile), [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile)e [**ConnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe) gestiscono operazioni di lunga durata. In modalità di attesa di blocco, le funzioni attendono per un tempo indefinito che un processo sull'altra estremità della pipe completi un'operazione. In modalità non di attesa di blocco, le funzioni restituiscono immediatamente in situazioni che altrimenti richiederebbero un'attesa indefinita.

[**Un'operazione ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) è interessata dalla modalità di attesa di un handle di pipe quando la pipe è vuota. Con un handle di attesa di blocco, l'operazione non viene completata correttamente fino a quando i dati non sono disponibili da un thread che scrive nell'altra estremità della pipe. Usando un handle di attesa non di blocco, la funzione restituisce zero immediatamente e la [**funzione GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce ERROR \_ NO \_ DATA.

[**Un'operazione WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) è interessata dalla modalità di attesa di un handle di pipe quando lo spazio nel buffer della pipe non è sufficiente. Con un handle di attesa di blocco, l'operazione di scrittura non può avere esito positivo fino a quando non viene creato spazio sufficiente nel buffer da un thread che legge dall'altra estremità della pipe. Con un handle di attesa non di blocco, l'operazione di scrittura restituisce immediatamente un valore diverso da zero, senza scrivere byte (per una pipe di tipo messaggio) o dopo aver scritto il numero di byte contenuto nel buffer (per una pipe di tipo byte).

[**Un'operazione ConnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe) è interessata dalla modalità di attesa di un handle di pipe quando non è presente alcun client connesso o in attesa di connettersi all'istanza della pipe. Con un handle di attesa di blocco, l'operazione di connessione non riesce fino a quando un client pipe non si connette all'istanza della pipe chiamando la [**funzione CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) o [**CallNamedPipe.**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea) Con un handle di attesa non di blocco, l'operazione di connessione restituisce zero immediatamente e la [**funzione GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce ERROR \_ PIPE \_ LISTENING.

Per impostazione predefinita, tutti named pipe handle restituiti dalla [**funzione CreateNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea) o [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) vengono creati con la modalità di attesa di blocco abilitata. Per creare la pipe in modalità non di blocco-attesa, il server pipe specifica PIPE \_ NOWAIT quando si chiama **CreateNamedPipe**.

Sia i client pipe che i server pipe possono modificare la modalità di attesa di un handle pipe specificando PIPE WAIT o PIPE NOWAIT in una chiamata alla \_ \_ funzione [**SetNamedPipeHandleState.**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-setnamedpipehandlestate)

> [!Note]  
> La modalità di attesa non bloccante è supportata per la compatibilità con Microsoft LAN Manager versione 2.0. Questa modalità non deve essere usata per ottenere input e output sovrapposti (I/O) con named pipe. È consigliabile usare invece l'I/O sovrapposto, perché consente l'esecuzione in background di operazioni dispendiose in termini di tempo al termine della funzione. Per altre informazioni sull'I/O sovrapposto, vedere Input e output sincroni [e sovrapposti.](synchronous-and-overlapped-input-and-output.md)

 

 

 
