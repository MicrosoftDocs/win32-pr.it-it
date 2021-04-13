---
description: Un oggetto di sincronizzazione è un oggetto il cui handle può essere specificato in una delle funzioni di attesa per coordinare l'esecuzione di più thread.
ms.assetid: 11558ae9-1056-48bf-96f5-94a051df41c3
title: Oggetti di sincronizzazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 299cbd6225b3cc7629378f5fe500fc36ccbe8e86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529227"
---
# <a name="synchronization-objects"></a>Oggetti di sincronizzazione

Un *oggetto di sincronizzazione* è un oggetto il cui handle può essere specificato in una delle [funzioni di attesa](wait-functions.md) per coordinare l'esecuzione di più thread. Più processi possono avere un handle per lo stesso oggetto di sincronizzazione, rendendo possibile la sincronizzazione interprocesso.

I tipi di oggetti seguenti vengono forniti esclusivamente per la sincronizzazione.



| Tipo           | Descrizione                                                                                                                                                                                                      |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Evento          | Notifica a uno o più thread in attesa che si è verificato un evento. Per ulteriori informazioni, vedere [oggetti evento](event-objects.md).                                                                                   |
| Mutex          | Può essere di proprietà di un solo thread alla volta, consentendo ai thread di coordinare l'accesso a una risorsa condivisa in modo reciprocamente esclusivo. Per ulteriori informazioni, vedere [oggetti mutex](mutex-objects.md).                          |
| Semaphore      | Mantiene un conteggio compreso tra zero e un valore massimo, limitando il numero di thread che accedono contemporaneamente a una risorsa condivisa. Per altre informazioni, vedere [oggetti semaforo](semaphore-objects.md). |
| Timer waitable | Notifica a uno o più thread in attesa che è arrivato un orario specificato. Per altre informazioni, vedere [oggetti timer waitable](waitable-timer-objects.md).                                                          |



 

Sebbene sia disponibile per altri utilizzi, per la sincronizzazione è possibile utilizzare anche gli oggetti seguenti.



| Oggetto                       | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Notifica di modifica          | Creato dalla funzione [**FindFirstChangeNotification**](/windows/win32/api/fileapi/nf-fileapi-findfirstchangenotificationa) , il suo stato viene impostato su segnalato quando si verifica un tipo specifico di modifica all'interno di una directory o di un albero di directory specificato. Per ulteriori informazioni, vedere [acquisizione delle notifiche di modifica di directory](../fileio/obtaining-directory-change-notifications.md).                                                                                                                                   |
| Input console                | Creato quando viene creata una console. L'handle per l'input della console viene restituito dalla funzione [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) quando viene specificato CONIN $ o dalla funzione [**GetStdHandle**](/windows/console/getstdhandle) . Il relativo stato viene impostato su segnalato quando è presente un input non letto nel buffer di input della console e impostato su non segnalato quando il buffer di input è vuoto. Per altre informazioni sulle console, vedere [applicazioni in modalità carattere](/windows/console/character-mode-applications) |
| Processo                          | Creato chiamando la funzione [**CreateJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-createjobobjectw) . Lo stato di un oggetto processo è impostato su segnalato quando tutti i relativi processi vengono interrotti perché è stato superato il limite di tempo di fine del processo specificato. Per ulteriori informazioni sugli oggetti processo, vedere [oggetti processo](../procthread/job-objects.md).                                                                                                                                                             |
| Notifica risorse di memoria | Creato dalla funzione [**CreateMemoryResourceNotification**](/windows/win32/api/memoryapi/nf-memoryapi-creatememoryresourcenotification) . Il relativo stato viene impostato su segnalato quando si verifica un tipo di modifica specificato nella memoria fisica. Per ulteriori informazioni sulla memoria, vedere [gestione della memoria](../memory/memory-management.md).                                                                                                                                                                                  |
| Processo                      | Creato chiamando la funzione [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) . Il relativo stato viene impostato su non segnalato mentre il processo è in esecuzione e impostato su segnalato al termine del processo. Per ulteriori informazioni sui processi, vedere [processi e thread](../procthread/processes-and-threads.md).                                                                                                                                                                                  |
| Thread                       | Creato quando viene creato un nuovo thread chiamando la funzione [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa), [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread)o [**CreateRemoteThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethread) . Il relativo stato viene impostato su non segnalato mentre il thread è in esecuzione e impostato su segnalato al termine del thread. Per ulteriori informazioni sui thread, vedere [processi e thread](../procthread/processes-and-threads.md).                                                            |



 

In alcune circostanze, è anche possibile usare un file, un named pipe o un dispositivo di comunicazione come oggetto di sincronizzazione. Tuttavia, il loro utilizzo a questo scopo è sconsigliato. Utilizzare invece l'I/O asincrono e attendere il set di oggetti evento nella struttura [**sovrapposta**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) . È più sicuro usare l'oggetto evento a causa della confusione che può verificarsi quando vengono eseguite più operazioni sovrapposte simultanee nello stesso file, named pipe o dispositivo di comunicazione. In questa situazione, non esiste alcun modo per stabilire quale operazione ha causato la segnalazione dello stato dell'oggetto.

Per ulteriori informazioni sulle operazioni di I/O su file, named pipe o comunicazioni, vedere [sincronizzazione e input e output sovrapposti](synchronization-and-overlapped-input-and-output.md).

 

 
