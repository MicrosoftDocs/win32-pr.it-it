---
description: Operazioni di pipe anonime, tra cui creazione di pipe, scrittura in una pipe, handle di pipe.
ms.assetid: df81471c-1072-4456-a877-304e76ade4bd
title: Operazioni di pipe anonime
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0c4c684daab5dd1c18dbf5eb22e2191f193e7ecc3b088ac58e3f680f442897a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119350711"
---
# <a name="anonymous-pipe-operations"></a>Operazioni di pipe anonime

La [**funzione CreatePipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-createpipe) crea una pipe anonima e restituisce due handle: un handle di lettura per la pipe e un handle di scrittura per la pipe. L'handle di lettura ha accesso in sola lettura alla pipe e l'handle di scrittura ha accesso in sola scrittura alla pipe. Per comunicare tramite la pipe, il server pipe deve passare un handle di pipe a un altro processo. In genere, questa operazione viene eseguita tramite ereditarietà. ciò significa che il processo consente l'ereditarietà dell'handle da parte di un processo figlio. Il processo può anche duplicare un handle di pipe usando la funzione [**DuplicateHandle**](/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle) e inviarlo a un processo non correlato usando una qualche forma di comunicazione interprocesso, ad esempio DDE o memoria condivisa.

Un server pipe può inviare l'handle di lettura o di scrittura al client pipe, a seconda che il client debba utilizzare la pipe anonima per inviare informazioni o ricevere informazioni. Per leggere dalla pipe, usare l'handle di lettura della pipe in una chiamata alla [**funzione ReadFile.**](/windows/desktop/api/fileapi/nf-fileapi-readfile) La **chiamata ReadFile** restituisce quando un altro processo ha scritto nella pipe. La **chiamata ReadFile** può restituire anche se tutti gli handle di scrittura nella pipe sono stati chiusi o se si verifica un errore prima del completamento dell'operazione di lettura.

Per scrivere nella pipe, usare l'handle di scrittura della pipe in una chiamata alla [**funzione WriteFile.**](/windows/desktop/api/fileapi/nf-fileapi-writefile) La **chiamata a WriteFile** non restituisce un valore finché non viene scritto il numero specificato di byte nella pipe o non si verifica un errore. Se il buffer della pipe è pieno e sono presenti più byte da scrivere, **WriteFile** non restituisce un valore finché un altro processo non legge la pipe, rendendo disponibile più spazio nel buffer. Il server pipe specifica le dimensioni del buffer per la pipe quando chiama [**CreatePipe.**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-createpipe)

Le operazioni di lettura e scrittura asincrone (sovrapposte) non sono supportate dalle pipe anonime. Ciò significa che non è possibile usare [**le funzioni ReadFileEx**](/windows/desktop/api/fileapi/nf-fileapi-readfileex) [**e WriteFileEx**](/windows/desktop/api/fileapi/nf-fileapi-writefileex) con pipe anonime. Inoltre, il *parametro lpOverlapped* di [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) e [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) viene ignorato quando queste funzioni vengono usate con le pipe anonime.

Esiste una pipe anonima finché tutti gli handle di pipe, sia di lettura che di scrittura, non sono stati chiusi. Un processo può chiudere i relativi handle di pipe usando la [**funzione CloseHandle.**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) Tutti gli handle di pipe vengono chiusi anche al termine del processo.

Le pipe anonime vengono implementate usando named pipe con un nome univoco. Pertanto, spesso è possibile passare un handle a una pipe anonima a una funzione che richiede un handle a un named pipe.

 

 
