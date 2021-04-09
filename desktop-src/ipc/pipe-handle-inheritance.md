---
description: Il server pipe controlla se è possibile ereditare i relativi handle nei modi seguenti.
ms.assetid: 72302f8b-f3a2-4efc-aab1-e596b8323984
title: Ereditarietà dell'handle della pipe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21cf91d4393b43011a2df632806f96da1e713b96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749671"
---
# <a name="pipe-handle-inheritance"></a>Ereditarietà dell'handle della pipe

Il server pipe controlla se è possibile ereditare i relativi handle nei modi seguenti:

-   La funzione [**non**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-createpipe) riceve una struttura degli [**\_ attributi di sicurezza**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) . Se il server pipe imposta il membro **bInheritHandle** della struttura su **true**, è possibile ereditare gli handle creati da **non** .
-   Il server pipe può utilizzare la funzione [**DuplicateHandle**](/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle) per modificare l'ereditarietà di un handle di pipe. Il server pipe può creare un duplicato non ereditabile di un handle di pipe ereditabile o un duplicato ereditabile di un handle di pipe non ereditabile.
-   La funzione [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) consente al server pipe di specificare se un processo figlio eredita tutti o nessuno dei relativi handle ereditabili.

Quando un processo figlio eredita un handle di pipe, il sistema consente al processo di accedere alla pipe. Tuttavia, il processo padre deve comunicare il valore dell'handle al processo figlio. Il processo padre esegue in genere questa operazione tramite il reindirizzamento dell'handle di output standard al processo figlio, come illustrato nei passaggi seguenti:

1.  Chiamare la funzione [**GetStdHandle**](/windows/console/getstdhandle) per ottenere l'handle di output standard corrente; salvare questo handle per poter ripristinare l'handle di output standard originale dopo che è stato creato il processo figlio.
2.  Chiamare la funzione [**SetStdHandle**](/windows/console/setstdhandle) per impostare l'handle di output standard sull'handle di scrittura sulla pipe. A questo punto il processo padre può creare il processo figlio.
3.  Chiamare la funzione [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) per chiudere l'handle di scrittura sulla pipe. Quando il processo figlio eredita l'handle di scrittura, la copia non è più necessaria per il processo padre.
4.  Chiamare [**SetStdHandle**](/windows/console/setstdhandle) per ripristinare l'handle di output standard originale.

Il processo figlio usa la funzione [**GetStdHandle**](/windows/console/getstdhandle) per ottenere il relativo handle di output standard, che ora è un handle per l'estremità di scrittura di una pipe. Il processo figlio usa quindi la funzione [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) per inviare l'output alla pipe. Quando l'elemento figlio termina con la pipe, deve chiudere l'handle della pipe chiamando [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) o terminando, che chiude automaticamente l'handle.

Il processo padre usa la funzione [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) per ricevere input dalla pipe. I dati vengono scritti in una pipe anonima come flusso di byte. Ciò significa che il processo padre che legge da una pipe non è in grado di distinguere tra i byte scritti in operazioni di scrittura separate, a meno che i processi padre e figlio non usino un protocollo per indicare dove termina l'operazione di scrittura. Quando tutti gli handle di scrittura sulla pipe sono chiusi, la funzione **ReadFile** restituisce zero. È importante che il processo padre chiuda il relativo handle all'estremità di scrittura della pipe prima di chiamare **ReadFile**. Se questa operazione non viene eseguita, l'operazione **ReadFile** non può restituire zero perché il processo padre ha un handle aperto per l'estremità di scrittura della pipe.

La procedura per il reindirizzamento dell'handle di input standard è simile a quella per il reindirizzamento dell'handle di output standard, ad eccezione del fatto che l'handle di lettura della pipe viene usato come handle di input standard del figlio. In questo caso, il processo padre deve garantire che il processo figlio non erediti l'handle di scrittura della pipe. Se questa operazione non viene eseguita, l'operazione [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) eseguita dal processo figlio non può restituire zero perché il processo figlio ha un handle aperto per l'estremità di scrittura della pipe.

Per un programma di esempio che usa le pipe anonime per reindirizzare gli handle standard di un processo figlio, vedere [creazione di un processo figlio con input e output reindirizzati](/windows/desktop/ProcThread/creating-a-child-process-with-redirected-input-and-output).

 

 
