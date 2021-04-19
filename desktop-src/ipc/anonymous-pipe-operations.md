---
description: Operazioni di pipe anonime, tra cui creazione di pipe, scrittura in una pipe, handle di pipe.
ms.assetid: df81471c-1072-4456-a877-304e76ade4bd
title: Operazioni di pipe anonime
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 963d7127c51859b05e570d00291470a49be5ba66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310851"
---
# <a name="anonymous-pipe-operations"></a>Operazioni di pipe anonime

La funzione [**non**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-createpipe) crea una pipe anonima e restituisce due handle: un handle di lettura alla pipe e un handle di scrittura alla pipe. L'handle di lettura ha accesso in sola lettura alla pipe e l'handle di scrittura ha accesso in sola scrittura alla pipe. Per comunicare usando la pipe, il server pipe deve passare un handle di pipe a un altro processo. In genere, questa operazione viene eseguita tramite ereditarietà; ovvero il processo consente di ereditare l'handle da un processo figlio. Il processo può anche duplicare un handle di pipe usando la funzione [**DuplicateHandle**](/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle) e inviarlo a un processo non correlato usando una forma di comunicazione interprocesso, ad esempio DDE o Shared Memory.

Un server pipe può inviare l'handle di lettura o l'handle di scrittura al client pipe, a seconda che il client debba utilizzare la pipe anonima per inviare informazioni o ricevere informazioni. Per leggere dalla pipe, utilizzare l'handle di lettura della pipe in una chiamata alla funzione [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) . La chiamata **ReadFile** restituisce quando un altro processo ha scritto nella pipe. La chiamata **ReadFile** può anche restituire se tutti gli handle di scrittura sulla pipe sono stati chiusi o se si verifica un errore prima del completamento dell'operazione di lettura.

Per scrivere nella pipe, utilizzare l'handle di scrittura della pipe in una chiamata alla funzione [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) . La chiamata a **WriteFile** non viene restituita fino a quando non viene scritto il numero specificato di byte nella pipe o si verifica un errore. Se il buffer della pipe è pieno e sono presenti più byte da scrivere, **WriteFile** non restituisce alcun risultato fino a quando un altro processo non legge dalla pipe, rendendo disponibile più spazio nel buffer. Il server pipe specifica le dimensioni del buffer per la pipe quando chiama [**non**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-createpipe).

Le operazioni di lettura e scrittura asincrone (sovrapposte) non sono supportate da pipe anonime. Ciò significa che non è possibile usare le funzioni [**ReadFileEx**](/windows/desktop/api/fileapi/nf-fileapi-readfileex) e [**WriteFileEx**](/windows/desktop/api/fileapi/nf-fileapi-writefileex) con le pipe anonime. Inoltre, il parametro *lpOverlapped* di [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) e [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) viene ignorato quando queste funzioni vengono usate con le pipe anonime.

Esiste una pipe anonima finché tutti gli handle di pipe, sia di lettura che di scrittura, non sono stati chiusi. Un processo può chiudere gli handle di pipe usando la funzione [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) . Tutti gli handle di pipe vengono chiusi anche al termine del processo.

Le pipe anonime vengono implementate usando un named pipe con un nome univoco. Pertanto, è spesso possibile passare un handle a una pipe anonima a una funzione che richiede un handle a una named pipe.

 

 
