---
description: Un oggetto di sincronizzazione è un oggetto il cui handle può essere specificato in una delle funzioni di attesa per coordinare l'esecuzione di più thread.
ms.assetid: 11558ae9-1056-48bf-96f5-94a051df41c3
title: Oggetti di sincronizzazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfd011663e13d8d6992355d99cc643e2f7243f8385ae75f9274367bfc43fe5f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118885909"
---
# <a name="synchronization-objects"></a>Oggetti di sincronizzazione

Un *oggetto di sincronizzazione* è un oggetto il cui handle può essere specificato in una delle funzioni [di attesa](wait-functions.md) per coordinare l'esecuzione di più thread. Più processi possono avere un handle per lo stesso oggetto di sincronizzazione, rendendo possibile la sincronizzazione interprocesso.

I tipi di oggetto seguenti vengono forniti esclusivamente per la sincronizzazione.



| Tipo           | Descrizione                                                                                                                                                                                                      |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Evento          | Notifica a uno o più thread in attesa che si è verificato un evento. Per altre informazioni, vedere [Oggetti evento](event-objects.md).                                                                                   |
| Mutex          | Può essere di proprietà di un solo thread alla volta, consentendo ai thread di coordinare l'accesso che si escludono a vicenda a una risorsa condivisa. Per altre informazioni, vedere [Oggetti Mutex](mutex-objects.md).                          |
| Semaphore      | Mantiene un conteggio compreso tra zero e un valore massimo, limitando il numero di thread che accedono contemporaneamente a una risorsa condivisa. Per altre informazioni, vedere [Semaphore Objects](semaphore-objects.md). |
| Timer waitable | Notifica a uno o più thread in attesa che è arrivato un tempo specificato. Per altre informazioni, vedere [Oggetti timer waitable](waitable-timer-objects.md).                                                          |



 

Anche se disponibile per altri usi, per la sincronizzazione è possibile usare anche gli oggetti seguenti.



| Oggetto                       | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Notifica di modifica          | Creato dalla [**funzione FindFirstChangeNotification,**](/windows/win32/api/fileapi/nf-fileapi-findfirstchangenotificationa) il relativo stato viene impostato su segnalato quando si verifica un tipo specificato di modifica all'interno di una directory o di un albero di directory specificato. Per altre informazioni, vedere [Recupero di notifiche di modifica della directory](../fileio/obtaining-directory-change-notifications.md).                                                                                                                                   |
| Input della console                | Creato quando viene creata una console. L'handle per l'input della console viene restituito dalla [**funzione CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) quando si specifica CONIN$ o dalla [**funzione GetStdHandle.**](/windows/console/getstdhandle) Il relativo stato è impostato su segnalato quando è presente un input non letto nel buffer di input della console e impostato su non segnalato quando il buffer di input è vuoto. Per altre informazioni sulle console, vedere [Applicazioni in modalità carattere](/windows/console/character-mode-applications) |
| Processo                          | Creato chiamando la [**funzione CreateJobObject.**](/windows/win32/api/jobapi2/nf-jobapi2-createjobobjectw) Lo stato di un oggetto processo viene impostato su segnalato quando tutti i relativi processi vengono terminati perché è stato superato il limite di tempo di fine processo specificato. Per altre informazioni sugli oggetti processo, vedere [Oggetti processo](../procthread/job-objects.md).                                                                                                                                                             |
| Notifica delle risorse di memoria | Creato dalla [**funzione CreateMemoryResourceNotification.**](/windows/win32/api/memoryapi/nf-memoryapi-creatememoryresourcenotification) Il relativo stato è impostato su segnalato quando si verifica un tipo specificato di modifica all'interno della memoria fisica. Per altre informazioni sulla memoria, vedere [Gestione della memoria](../memory/memory-management.md).                                                                                                                                                                                  |
| Processo                      | Creato chiamando la [**funzione CreateProcess.**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) Il relativo stato è impostato su non segnalato mentre il processo è in esecuzione e impostato su segnalato al termine del processo. Per altre informazioni sui processi, vedere [Processi e thread](../procthread/processes-and-threads.md).                                                                                                                                                                                  |
| Thread                       | Creato quando viene creato un nuovo thread chiamando la [**funzione CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa), [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread)o [**CreateRemoteThread.**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethread) Il relativo stato è impostato su non segnalato mentre il thread è in esecuzione e impostato su segnalato quando il thread viene terminato. Per altre informazioni sui thread, vedere [Processi e thread](../procthread/processes-and-threads.md).                                                            |



 

In alcuni casi, è anche possibile usare un file, un named pipe o un dispositivo di comunicazione come oggetto di sincronizzazione. Tuttavia, il loro uso a questo scopo è sconsigliato. Usare invece l'I/O asincrono e attendere l'oggetto evento impostato nella [**struttura OVERLAPPED.**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) È più sicuro usare l'oggetto evento a causa della confusione che può verificarsi quando più operazioni sovrapposte simultanee vengono eseguite sullo stesso file, named pipe o dispositivo di comunicazione. In questo caso, non è possibile sapere quale operazione ha causato la segnalazione dello stato dell'oggetto.

Per altre informazioni sulle operazioni di I/O su file, named pipe o comunicazioni, vedere Sincronizzazione e [input e output sovrapposti.](synchronization-and-overlapped-input-and-output.md)

 

 
