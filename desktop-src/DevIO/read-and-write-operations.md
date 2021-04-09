---
description: Windows supporta le operazioni di I/O di file sincrone e asincrone (sovrapposte) sulle risorse di comunicazione seriale.
ms.assetid: cee44596-ad73-4afb-b86a-744b0b46d9d5
title: Operazioni di lettura e scrittura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a26cc53dbe8c52286fe53c81202ab3828808b1aa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126636"
---
# <a name="read-and-write-operations"></a>Operazioni di lettura e scrittura

Windows supporta le operazioni di I/O di file sincrone e asincrone (sovrapposte) sulle risorse di comunicazione seriale. Le operazioni sovrapposte consentono al thread chiamante di eseguire altre attività durante l'esecuzione dell'operazione in background. Un thread usa la funzione [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) o [**ReadFileEx**](/windows/desktop/api/fileapi/nf-fileapi-readfileex) per leggere da una risorsa di comunicazione e la funzione [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) o [**WriteFileEx**](/windows/desktop/api/fileapi/nf-fileapi-writefileex) per scrivere in una risorsa di comunicazione. **ReadFile** e **WriteFile** possono essere eseguiti in modo sincrono o asincrono. **ReadFileEx** e **WriteFileEx** possono essere eseguiti solo in modo asincrono.

Il comportamento di queste funzioni di lettura e scrittura è influenzato dal fatto che la funzione venga eseguita come operazione sovrapposta, che i parametri di timeout siano associati all'handle e che i parametri di controllo di flusso siano associati all'handle.

Un thread può anche scrivere in una risorsa di comunicazione usando la funzione [**TransmitCommChar**](/windows/desktop/api/Winbase/nf-winbase-transmitcommchar) , che trasmette un carattere specificato prima di tutti i dati in sospeso nel buffer di output. Questa funzione è utile per trasmettere al sistema ricevente un carattere di segnale con priorità alta. La trasmissione del carattere a priorità alta è ancora soggetta ai timeout di controllo di flusso e scrittura e l'operazione viene eseguita in modo sincrono.

Un thread può usare la funzione [**PurgeComm**](/windows/desktop/api/Winbase/nf-winbase-purgecomm) per eliminare tutti i caratteri nel buffer di output o di input di un dispositivo. **PurgeComm** può terminare anche le operazioni di lettura o scrittura in sospeso, anche se le operazioni non sono state completate. Se un thread utilizza **PurgeComm** per scaricare un buffer di output, i caratteri eliminati non vengono trasmessi. Per svuotare il buffer di output assicurandosi che il contenuto venga trasmesso, un thread può chiamare la funzione [**FlushFileBuffers**](/windows/desktop/api/fileapi/nf-fileapi-flushfilebuffers) (un'operazione sincrona). Si noti, tuttavia, che **FlushFileBuffers** è soggetto al controllo di flusso ma non ai timeout di scrittura e non verrà restituito finché tutte le operazioni di scrittura in sospeso non sono state trasmesse.

 

 
