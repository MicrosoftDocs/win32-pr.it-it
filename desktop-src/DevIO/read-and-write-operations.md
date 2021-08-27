---
description: Windows supporta operazioni di I/O di file sincrone e asincrone (sovrapposte) sulle risorse di comunicazione seriale.
ms.assetid: cee44596-ad73-4afb-b86a-744b0b46d9d5
title: Operazioni di lettura e scrittura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3a1c9cca5079cc6f473b07c02212da6f42156305b43f4b30eb1de3e6b67e593
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120109011"
---
# <a name="read-and-write-operations"></a>Operazioni di lettura e scrittura

Windows supporta operazioni di I/O di file sincrone e asincrone (sovrapposte) sulle risorse di comunicazione seriale. Le operazioni sovrapposte consentono al thread chiamante di eseguire altre attività mentre l'operazione viene eseguita in background. Un thread usa la [**funzione ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) o [**ReadFileEx**](/windows/desktop/api/fileapi/nf-fileapi-readfileex) per leggere da una risorsa di comunicazione e la [**funzione WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) [**o WriteFileEx**](/windows/desktop/api/fileapi/nf-fileapi-writefileex) per scrivere in una risorsa di comunicazione. **ReadFile** e **WriteFile** possono essere eseguiti in modo sincrono o asincrono. **ReadFileEx e** **WriteFileEx** possono essere eseguiti solo in modo asincrono.

Il comportamento di queste funzioni di lettura e scrittura è influenzato dal fatto che la funzione sia eseguita come operazione sovrapposta, se i parametri di timeout sono associati all'handle e se i parametri di controllo di flusso sono associati all'handle.

Un thread può anche scrivere in una risorsa di comunicazione usando la funzione [**TransmitCommChar,**](/windows/desktop/api/Winbase/nf-winbase-transmitcommchar) che trasmette un carattere specificato prima di qualsiasi dato in sospeso nel buffer di output. Questa funzione è utile per la trasmissione di un carattere di segnale ad alta priorità al sistema ricevente. La trasmissione del carattere con priorità alta è ancora soggetta al controllo di flusso e ai timeout di scrittura e l'operazione viene eseguita in modo sincrono.

Un thread può usare la [**funzione PurgeComm**](/windows/desktop/api/Winbase/nf-winbase-purgecomm) per rimuovere tutti i caratteri nel buffer di input o di output di un dispositivo. **PurgeComm può** anche terminare le operazioni di lettura o scrittura in sospeso, anche se le operazioni non sono state completate. Se un thread usa **PurgeComm** per scaricare un buffer di output, i caratteri eliminati non vengono trasmessi. Per svuotare il buffer di output assicurando al tempo stesso che il contenuto sia trasmesso, un thread può chiamare la funzione [**FlushFileBuffers**](/windows/desktop/api/fileapi/nf-fileapi-flushfilebuffers) (operazione sincrona). Si noti, tuttavia, che **FlushFileBuffers** è soggetto al controllo di flusso ma non ai timeout di scrittura e non restituirà finché non vengono trasmesse tutte le operazioni di scrittura in sospeso.

 

 
