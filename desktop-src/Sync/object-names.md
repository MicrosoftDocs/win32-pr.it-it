---
description: Gli oggetti denominati forniscono un modo semplice per la condivisione degli handle di oggetto da parte dei processi.
ms.assetid: 00a00227-45fc-49a1-8ff5-aeccb172d16a
title: Nomi di oggetti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee746150a41f335a4073cb4b5ba282d17ad706f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315302"
---
# <a name="object-names"></a>Nomi di oggetti

Gli oggetti denominati forniscono un modo semplice per la condivisione degli handle di oggetto da parte dei processi. Dopo che un processo ha creato un evento denominato, un mutex, un semaforo o un oggetto timer, altri processi possono usare il nome per chiamare la funzione appropriata ( [**OpenEvent**](/windows/win32/api/synchapi/nf-synchapi-openeventa), [**errore in OpenMutex**](/windows/win32/api/synchapi/nf-synchapi-openmutexw), [**OpenSemaphore**](/windows/win32/api/synchapi/nf-synchapi-opensemaphorew)o [**OpenWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-openwaitabletimerw)) per aprire un handle per l'oggetto. Il confronto tra nomi distingue tra maiuscole e minuscole.

I nomi di evento, semaforo, mutex, timer waitable, mapping di file e oggetti processo condividono lo stesso spazio dei nomi. Se si tenta di creare un oggetto usando un nome usato da un oggetto di un altro tipo, la funzione ha esito negativo e [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce un **handle di errore \_ non valido \_**. Pertanto, quando si creano oggetti denominati, utilizzare nomi univoci e assicurarsi di controllare i valori restituiti dalla funzione per gli errori relativi ai nomi duplicati.

Se si tenta di creare un oggetto utilizzando un nome utilizzato da un oggetto dello stesso tipo, la funzione ha esito positivo, restituendo un handle all'oggetto esistente e [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce un **errore \_ già \_ esistente**. Se, ad esempio, il nome specificato in una chiamata alla funzione [**CreateMutex**](/windows/win32/api/synchapi/nf-synchapi-createmutexa) corrisponde al nome di un oggetto mutex esistente, la funzione restituisce un handle per l'oggetto esistente. In questo caso, la chiamata a **CreateMutex** è equivalente a una chiamata alla funzione [**errore in OpenMutex**](/windows/win32/api/synchapi/nf-synchapi-openmutexw) . La presenza di più processi utilizza **CreateMutex** per lo stesso mutex è pertanto equivalente a un processo che chiama **CreateMutex** mentre gli altri processi chiamano **errore in OpenMutex**, con la differenza che elimina la necessità di verificare che il processo di creazione venga avviato per primo. Quando si usa questa tecnica per gli oggetti mutex, tuttavia, nessuno dei processi chiamante deve richiedere la proprietà immediata del mutex. Se più processi richiedono la proprietà immediata, può essere difficile prevedere il processo che ottiene effettivamente la proprietà iniziale.

Un ambiente di servizi Terminal dispone di uno spazio dei nomi globale per eventi, semafori, mutex, temporizzazioni attese, oggetti di mapping di file e oggetti processo. Ogni sessione client di servizi Terminal dispone inoltre di uno spazio dei nomi separato per questi oggetti. I processi client di Servizi terminal possono utilizzare i nomi degli oggetti con prefisso "globale \\ " o "locale \\ " per creare in modo esplicito un oggetto nello spazio dei nomi globale o sessione. Per altre informazioni, vedere [spazi dei nomi degli oggetti kernel](../termserv/kernel-object-namespaces.md). Il cambio rapido utente viene implementato tramite sessioni di Servizi terminal (ogni utente accede a una sessione diversa). I nomi degli oggetti kernel devono seguire le linee guida descritte per Servizi terminal, in modo che le applicazioni possano supportare più utenti.

Gli oggetti di sincronizzazione possono essere creati in uno spazio dei nomi privato. Per altre informazioni, vedere [spazi dei nomi degli oggetti](object-namespaces.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di oggetti denominati](using-named-objects.md)
</dt> </dl>

 

 
