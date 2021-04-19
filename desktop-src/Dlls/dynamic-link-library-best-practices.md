---
description: La creazione di dll presenta una serie di problemi per gli sviluppatori.
ms.assetid: 44EFC4B5-7A2F-43A6-914E-D4EB7446AC35
title: Procedure consigliate per la libreria Dynamic-Link
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88aba0999f3d0825c6d2f4df3afe09d766a82232
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317824"
---
# <a name="dynamic-link-library-best-practices"></a>Procedure consigliate per la libreria Dynamic-Link

* * Aggiornato: * *

-   17 maggio 2006

**API importanti**

-   [**DllMain**](dllmain.md)
-   [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa)
-   [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa)

La creazione di dll presenta una serie di problemi per gli sviluppatori. Le dll non hanno il controllo delle versioni applicato dal sistema. Quando in un sistema esistono più versioni di una DLL, la facilità di sovrascrittura associata alla mancanza di uno schema di controllo delle versioni crea conflitti tra le dipendenze e le API. La complessità dell'ambiente di sviluppo, l'implementazione del caricatore e le dipendenze DLL hanno creato una fragilità in base all'ordine di caricamento e al comportamento dell'applicazione. Infine, molte applicazioni si basano sulle dll e hanno set complessi di dipendenze che devono essere rispettate per il corretto funzionamento delle applicazioni. In questo documento vengono fornite le linee guida per gli sviluppatori di DLL che consentono di creare DLL più solide, portatili ed estendibili.

Una sincronizzazione non corretta all'interno di [**DllMain**](dllmain.md) può causare il deadlock di un'applicazione o l'accesso a dati o codice in una dll non inizializzata. La chiamata di determinate funzioni dall'interno di **DllMain** causa tali problemi.

![cosa accade quando viene caricata una libreria](images/fig1.png)

## <a name="general-best-practices"></a>Procedure consigliate generali

Il metodo [**DllMain**](dllmain.md) viene chiamato mentre viene mantenuto il blocco del caricatore. Pertanto, vengono imposte restrizioni significative sulle funzioni che possono essere chiamate in **DllMain**. Di conseguenza, **DllMain** è progettato per eseguire attività di inizializzazione minime, usando un piccolo subset dell'API Microsoft® Windows®. Non è possibile chiamare alcuna funzione in **DllMain** che tenti direttamente o indirettamente di acquisire il blocco del caricatore. In caso contrario, si introdurrà la possibilità che l'applicazione si blocchi o arresti anomali. Un errore in un'implementazione di **DllMain** può compromettere l'intero processo e tutti i relativi thread.

Il valore [**DllMain**](dllmain.md) ideale è semplicemente uno stub vuoto. Tuttavia, data la complessità di molte applicazioni, questa operazione è in genere troppo restrittiva. Una buona regola empirica per **DllMain** è rimandare il maggior quantità possibile di inizializzazione. L'inizializzazione differita aumenta l'affidabilità dell'applicazione perché questa inizializzazione non viene eseguita durante il blocco del caricatore. Inoltre, l'inizializzazione differita consente di usare in modo sicuro gran parte dell'API Windows.

Non è possibile posticipare alcune attività di inizializzazione. Una DLL che dipende da un file di configurazione, ad esempio, non può essere caricata se il file è in formato non valido o contiene un'operazione di Garbage Collection. Per questo tipo di inizializzazione, la DLL deve tentare l'azione e generare un errore rapidamente anziché sprecare risorse completando altre operazioni.

Non eseguire mai le seguenti attività dall'interno di [**DllMain**](dllmain.md):

-   Chiamare [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) o [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) , direttamente o indirettamente. Questo può causare un deadlock o un arresto anomalo.
-   Chiamare [**GetStringTypeA**](/windows/desktop/api/winnls/nf-winnls-getstringtypea), [**GetStringTypeEx**](/windows/win32/api/stringapiset/nf-stringapiset-getstringtypeexw)o [**GetStringTypeW**](/windows/desktop/api/stringapiset/nf-stringapiset-getstringtypew) , direttamente o indirettamente. Questo può causare un deadlock o un arresto anomalo.
-   Sincronizzare con altri thread. Questo può causare un deadlock.
-   Acquisire un oggetto di sincronizzazione di proprietà del codice in attesa di acquisire il blocco del caricatore. Questo può causare un deadlock.
-   Inizializzare i thread COM usando [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex). In determinate condizioni, questa funzione può chiamare [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa).
-   Chiamare le funzioni del registro di sistema. Queste funzioni vengono implementate in Advapi32.dll. Se Advapi32.dll non viene inizializzato prima della DLL, la DLL può accedere alla memoria non inizializzata e causare l'arresto anomalo del processo.
-   Chiamare [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa). La creazione di un processo può caricare un'altra DLL.
-   Chiamare [**ExitThread**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibraryandexitthread). L'uscita da un thread durante la disconnessione della DLL può causare l'acquisizione del blocco del caricatore, causando un deadlock o un arresto anomalo.
-   Chiamare [**CreateThread**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createthread). La creazione di un thread può funzionare se non si esegue la sincronizzazione con altri thread, ma è rischiosa.
-   Creare un named pipe o un altro oggetto denominato (solo Windows 2000). In Windows 2000, gli oggetti denominati vengono forniti dalla DLL di Servizi terminal. Se questa DLL non è inizializzata, le chiamate alla DLL possono causare l'arresto anomalo del processo.
-   Usare la funzione di gestione della memoria dalla Run-Time C dinamica (CRT). Se la DLL CRT non è inizializzata, le chiamate a queste funzioni possono causare l'arresto anomalo del processo.
-   Chiamare le funzioni in User32.dll o Gdi32.dll. Alcune funzioni caricano un'altra DLL, che potrebbe non essere inizializzata.
-   Usa codice gestito.

Le attività seguenti possono essere eseguite in modo sicuro all'interno di **DllMain**:

-   Inizializzare strutture di dati statiche e membri in fase di compilazione.
-   Creare e inizializzare gli oggetti di sincronizzazione.
-   Allocare memoria e inizializzare strutture di dati dinamiche (evitando le funzioni elencate in precedenza).
-   Configurare l'archiviazione locale di thread (TLS).
-   Aprire, leggere e scrivere nei file.
-   Chiamare le funzioni in Kernel32.dll (ad eccezione delle funzioni elencate in precedenza).
-   Impostare i puntatori globali su NULL, disattivando l'inizializzazione dei membri dinamici. In Microsoft Windows Vista™ è possibile utilizzare le funzioni di inizializzazione monouso per garantire che un blocco di codice venga eseguito una sola volta in un ambiente a thread multipli.

## <a name="deadlocks-caused-by-lock-order-inversion"></a>Deadlock causati dall'inversione dell'ordine di blocco

Quando si implementa codice che utilizza più oggetti di sincronizzazione, ad esempio blocchi, è fondamentale rispettare l'ordine di blocco. Quando è necessario acquisire più di un blocco alla volta, è necessario definire una precedenza esplicita denominata gerarchia dei blocchi o ordine di blocco. Se, ad esempio, il blocco A viene acquisito prima del blocco B in un punto qualsiasi del codice e il blocco B viene acquisito prima del blocco C in un altro punto del codice, l'ordine di blocco è A, B, C e questo ordine deve essere seguito in tutto il codice. L'inversione dell'ordine di blocco si verifica quando l'ordine di blocco non viene seguito, ad esempio se viene acquisito il blocco B prima del blocco A. l'inversione dell'ordine di blocco può causare deadlock difficili da eseguire il debug. Per evitare tali problemi, tutti i thread devono acquisire i blocchi nello stesso ordine.

È importante notare che il caricatore chiama [**DllMain**](dllmain.md) con il blocco del caricatore già acquisito, quindi il blocco del caricatore deve avere la precedenza più alta nella gerarchia di blocco. Si noti inoltre che il codice deve solo acquisire i blocchi necessari per una corretta sincronizzazione. non è necessario acquisire ogni singolo blocco definito nella gerarchia. Se, ad esempio, una sezione di codice richiede solo i blocchi A e C per la corretta sincronizzazione, il codice deve acquisire il blocco A prima di acquisire il blocco C; non è necessario che il codice acquisisca anche il blocco B. Il codice DLL non può inoltre acquisire in modo esplicito il blocco del caricatore. Se il codice deve chiamare un'API, ad esempio [**GetModuleFileName**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulefilenamea) , che può acquisire indirettamente il blocco del caricatore e anche il codice deve acquisire un blocco privato, il codice deve chiamare **GetModuleFileName** prima di acquisire il blocco P, assicurando in tal modo che l'ordine di caricamento venga rispettato.

Nella figura 2 è riportato un esempio che illustra l'inversione dell'ordine di blocco. Si consideri una DLL il cui thread principale contiene [**DllMain**](dllmain.md). Il caricatore della libreria acquisisce il blocco del caricatore e quindi chiama **DllMain**. Il thread principale crea gli oggetti di sincronizzazione A, B e G per serializzare l'accesso alle strutture di dati e quindi tenta di acquisire il blocco G. Un thread di lavoro che ha già acquisito il blocco G chiama una funzione, ad esempio GetModuleHandle, che tenta di acquisire il blocco del caricatore. Pertanto, il thread di lavoro è bloccato su L e il thread principale è bloccato su G, causando un deadlock.

![deadlock causato dall'inversione dell'ordine di blocco](images/fig2.png)

Per evitare deadlock causati da inversione dell'ordine di blocco, tutti i thread devono tentare di acquisire sempre gli oggetti di sincronizzazione nell'ordine di caricamento definito.

## <a name="best-practices-for-synchronization"></a>Procedure consigliate per la sincronizzazione

Si consideri una DLL che crea thread di lavoro come parte dell'inizializzazione. Quando si pulisce la DLL, è necessario eseguire la sincronizzazione con tutti i thread di lavoro per assicurarsi che le strutture di dati siano in uno stato coerente e quindi terminare i thread di lavoro. Attualmente, non esiste un modo semplice per risolvere completamente il problema della sincronizzazione e dell'arresto delle dll in un ambiente a thread multipli. In questa sezione vengono descritte le procedure consigliate correnti per la sincronizzazione dei thread durante l'arresto della DLL.

Sincronizzazione thread in [**DllMain**](dllmain.md) durante l'uscita del processo

-   Quando [**DllMain**](dllmain.md) viene chiamato all'uscita del processo, tutti i thread del processo sono stati eliminati forzatamente ed è possibile che lo spazio degli indirizzi sia incoerente. In questo caso la sincronizzazione non è obbligatoria. In altre parole, il gestore di \_ scollegamento del processo dll ideale \_ è vuoto.
-   Windows Vista garantisce che le strutture di dati principali (variabili di ambiente, directory correnti, heap del processo e così via) siano in uno stato coerente. Tuttavia, altre strutture di dati possono essere danneggiate, quindi la pulizia della memoria non è sicura.
-   Lo stato persistente che deve essere salvato deve essere scaricato nell'archivio permanente.

Sincronizzazione dei thread in **DllMain** per lo \_ scollegamento del thread dll durante lo \_ scaricamento della dll

-   Quando la DLL viene scaricata, lo spazio degli indirizzi non viene eliminato. Pertanto, è previsto che la DLL esegua una chiusura normale. Sono inclusi la sincronizzazione di thread, gli handle aperti, lo stato persistente e le risorse allocate.
-   La sincronizzazione del thread è complessa perché l'attesa di chiusura di thread in [**DllMain**](dllmain.md) può causare un deadlock. Ad esempio, la DLL A include il blocco del caricatore. Segnala al thread T di uscire e attende la chiusura del thread. Il thread T viene chiuso e il caricatore tenta di acquisire il blocco del caricatore per effettuare una chiamata a **DllMain** della dll a con la \_ disconnessione del thread dll \_ . Causando un deadlock. Per ridurre al minimo il rischio di un deadlock:
    -   La DLL a ottiene un \_ \_ messaggio di scollegamento del thread dll nella relativa [**DllMain**](dllmain.md) e imposta un evento per il thread T, segnalando l'uscita.
    -   Il thread T termina l'attività corrente, porta se stesso a uno stato coerente, segnala la DLL A e attende infinitamente. Si noti che le routine di controllo della coerenza devono rispettare le stesse restrizioni di [**DllMain**](dllmain.md) per evitare il deadlock.
    -   La DLL A termina T, sapendo che è in uno stato coerente.

Se una DLL viene scaricata dopo la creazione di tutti i relativi thread, ma prima dell'avvio dell'esecuzione, i thread potrebbero arrestarsi in modo anomalo. Se la DLL ha creato thread nella relativa **DllMain** come parte dell'inizializzazione, è possibile che l'inizializzazione di alcuni thread non sia terminata e che il \_ \_ messaggio di connessione del thread dll sia ancora in attesa di essere recapitato alla dll. In questa situazione, se la DLL viene scaricata, inizierà a terminare i thread. Tuttavia, alcuni thread possono essere bloccati dietro il blocco del caricatore. I \_ \_ messaggi di associazione dei thread dll vengono elaborati dopo che è stato annullato il mapping della dll, causando un arresto anomalo del processo.

## <a name="recommendations"></a>Consigli

Di seguito sono riportate le linee guida consigliate:

-   Utilizzare Application Verifier per intercettare gli errori più comuni in [**DllMain**](dllmain.md).
-   Se si usa un blocco privato all'interno di [**DllMain**](dllmain.md), definire una gerarchia di blocco e usarla in modo coerente. Il blocco del caricatore deve trovarsi nella parte inferiore della gerarchia.
-   Verificare che nessuna chiamata dipenda da un'altra DLL che potrebbe non essere ancora stata completamente caricata.
-   Eseguire inizializzazioni semplici in modo statico in fase di compilazione, anziché in [**DllMain**](dllmain.md).
-   Rinviare tutte le chiamate in [**DllMain**](dllmain.md) che possono attendere più tardi.
-   Rinvia le attività di inizializzazione che possono attendere più tardi. Alcune condizioni di errore devono essere rilevate in anticipo in modo che l'applicazione possa gestire correttamente gli errori. Tuttavia, esistono compromessi tra questo rilevamento iniziale e la perdita di affidabilità che può derivare da essa. Il rinvio dell'inizializzazione è spesso migliore.

 

 
