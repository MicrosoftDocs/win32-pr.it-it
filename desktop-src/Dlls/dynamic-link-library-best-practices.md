---
description: La creazione di DLL presenta una serie di sfide per gli sviluppatori.
ms.assetid: 44EFC4B5-7A2F-43A6-914E-D4EB7446AC35
title: Dynamic-Link consigliate per la libreria di risorse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95d02314b15a13de7658c0b87ba7cd998f48a0a3d9f2f2682b36539bd9f5bde3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119696583"
---
# <a name="dynamic-link-library-best-practices"></a>Dynamic-Link consigliate per la libreria di risorse

**Aggiornato: **

-   17 maggio 2006

**API importanti**

-   [**DllMain**](dllmain.md)
-   [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa)
-   [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa)

La creazione di DLL presenta una serie di sfide per gli sviluppatori. Le DLL non hanno il controllo delle versioni imposto dal sistema. Quando in un sistema sono presenti più versioni di una DLL, la facilità di sovrascrittura abbinata alla mancanza di uno schema di controllo delle versioni crea dipendenze e conflitti di API. La complessità nell'ambiente di sviluppo, nell'implementazione del caricatore e nelle dipendenze dll ha creato complessità nell'ordine di caricamento e nel comportamento dell'applicazione. Infine, molte applicazioni si basano sulle DLL e hanno set complessi di dipendenze che devono essere rispettati per il corretto funzionamento delle applicazioni. In questo documento vengono fornite linee guida per gli sviluppatori di DLL che consentono di creare DLL più affidabili, portabili ed estendibili.

Una sincronizzazione non [**corretta all'interno**](dllmain.md) di DllMain può causare un deadlock di un'applicazione o l'accesso a dati o codice in una DLL non inizializzata. La chiamata di determinate funzioni dall'interno **di DllMain** causa tali problemi.

![cosa accade quando viene caricata una libreria](images/fig1.png)

## <a name="general-best-practices"></a>Procedure consigliate generali

[**DllMain**](dllmain.md) viene chiamato mentre viene mantenuto il blocco del caricatore. Di conseguenza, alle funzioni che possono essere chiamate all'interno di DllMain vengono imposte **restrizioni significative.** Di conseguenza, **DllMain è** progettato per eseguire attività di inizializzazione minime, usando un piccolo subset dell'API Microsoft® Windows®. Non è possibile chiamare qualsiasi funzione in **DllMain** che tenti direttamente o indirettamente di acquisire il blocco del caricatore. In caso contrario, si introdurrà la possibilità che l'applicazione si blocchi o si arresti in modo anomalo. Un errore in **un'implementazione di DllMain** può compromettere l'intero processo e tutti i relativi thread.

La [**DllMain ideale**](dllmain.md) sarebbe semplicemente uno stub vuoto. Tuttavia, data la complessità di molte applicazioni, questo è in genere troppo restrittivo. Una buona regola generale per DllMain è **rimandare** il maggior numero possibile di inizializzazioni. L'inizializzazione differita aumenta l'affidabilità dell'applicazione perché questa inizializzazione non viene eseguita mentre viene mantenuto il blocco del caricatore. Inoltre, l'inizializzazione differita consente di usare in modo sicuro gran parte dell Windows API.

Alcune attività di inizializzazione non possono essere posticipate. Ad esempio, una DLL che dipende da un file di configurazione non dovrebbe essere caricata se il file è in formato non valido o contiene operazioni di Garbage Collection. Per questo tipo di inizializzazione, la DLL deve tentare l'azione e non sprecare risorse completando altre operazioni.

Non eseguire mai le attività seguenti dall'interno [**di DllMain**](dllmain.md):

-   Chiamare [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) o [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) (direttamente o indirettamente). Ciò può causare un deadlock o un arresto anomalo.
-   Chiamare [**GetStringTypeA,**](/windows/desktop/api/winnls/nf-winnls-getstringtypea) [**GetStringTypeEx**](/windows/win32/api/stringapiset/nf-stringapiset-getstringtypeexw)o [**GetStringTypeW**](/windows/desktop/api/stringapiset/nf-stringapiset-getstringtypew) (direttamente o indirettamente). Ciò può causare un deadlock o un arresto anomalo.
-   Eseguire la sincronizzazione con altri thread. Ciò può causare un deadlock.
-   Acquisire un oggetto di sincronizzazione di proprietà del codice in attesa di acquisire il blocco del caricatore. Ciò può causare un deadlock.
-   Inizializzare i thread COM usando [**CoInitializeEx.**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) In determinate condizioni, questa funzione può chiamare [**LoadLibraryEx.**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa)
-   Chiamare le funzioni del Registro di sistema. Queste funzioni vengono implementate in Advapi32.dll. Se Advapi32.dll non viene inizializzata prima della DLL, la DLL può accedere alla memoria non inizializzata e causare l'arresto anomalo del processo.
-   Chiamare [**CreateProcess.**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) La creazione di un processo può caricare un'altra DLL.
-   Chiamare [**ExitThread**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibraryandexitthread). L'uscita da un thread durante lo scollegamento della DLL può causare la nuova acquisizione del blocco del caricatore, causando un deadlock o un arresto anomalo.
-   Chiamare [**CreateThread**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createthread). La creazione di un thread può funzionare se non si esegue la sincronizzazione con altri thread, ma è rischiosa.
-   Creare un named pipe o un altro oggetto denominato (solo Windows 2000). In Windows 2000 gli oggetti denominati vengono forniti dalla DLL di Servizi terminal. Se questa DLL non è inizializzata, le chiamate alla DLL possono causare l'arresto anomalo del processo.
-   Usare la funzione di gestione della memoria dal linguaggio C Run-Time (CRT). Se la DLL CRT non è inizializzata, le chiamate a queste funzioni possono causare l'arresto anomalo del processo.
-   Chiamare funzioni in User32.dll o Gdi32.dll. Alcune funzioni caricano un'altra DLL, che potrebbe non essere inizializzata.
-   Usare codice gestito.

Le attività seguenti sono sicure da eseguire all'interno **di DllMain**:

-   Inizializzare strutture di dati statici e membri in fase di compilazione.
-   Creare e inizializzare oggetti di sincronizzazione.
-   Allocare memoria e inizializzare le strutture di dati dinamici (evitando le funzioni elencate in precedenza).
-   Configurare l'archiviazione thread-local (TLS).
-   Aprire, leggere e scrivere nei file.
-   Chiamare funzioni in Kernel32.dll (ad eccezione delle funzioni elencate in precedenza).
-   Impostare i puntatori globali su NULL, disattivando l'inizializzazione dei membri dinamici. In Microsoft Windows Vista™ è possibile usare le funzioni di inizializzazione una sola volta per garantire che un blocco di codice viene eseguito una sola volta in un ambiente multithreading.

## <a name="deadlocks-caused-by-lock-order-inversion"></a>Deadlock causati dall'inversione dell'ordine di blocco

Quando si implementa codice che usa più oggetti di sincronizzazione, ad esempio blocchi, è fondamentale rispettare l'ordine di blocco. Quando è necessario acquisire più di un blocco alla volta, è necessario definire una precedenza esplicita denominata gerarchia di blocchi o ordine di blocco. Ad esempio, se il blocco A viene acquisito prima del blocco B in un punto qualsiasi del codice e il blocco B viene acquisito prima del blocco C in un'altra posizione nel codice, l'ordine di blocco è A, B, C e questo ordine deve essere seguito in tutto il codice. L'inversione dell'ordine di blocco si verifica quando l'ordine di blocco non viene seguito, ad esempio se il blocco B viene acquisito prima del blocco A. L'inversione dell'ordine di blocco può causare deadlock di cui è difficile eseguire il debug. Per evitare tali problemi, tutti i thread devono acquisire blocchi nello stesso ordine.

È importante notare che il caricatore chiama [**DllMain**](dllmain.md) con il blocco del caricatore già acquisito, quindi il blocco del caricatore deve avere la precedenza più alta nella gerarchia di blocco. Si noti anche che il codice deve acquisire solo i blocchi necessari per la corretta sincronizzazione. non deve acquisire ogni singolo blocco definito nella gerarchia. Ad esempio, se una sezione di codice richiede solo i blocchi A e C per la corretta sincronizzazione, il codice deve acquisire il blocco A prima di acquisire il blocco C; Non è necessario che anche il codice acquisisca il blocco B. Inoltre, il codice DLL non può acquisire in modo esplicito il blocco del caricatore. Se il codice deve chiamare un'API come [**GetModuleFileName**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulefilenamea) che può acquisire indirettamente il blocco del caricatore e anche il codice deve acquisire un blocco privato, il codice deve chiamare **GetModuleFileName** prima di acquisire il blocco P, assicurando così che l'ordine di caricamento venga rispettato.

La figura 2 è un esempio che illustra l'inversione dell'ordine di blocco. Si consideri una DLL il cui thread principale contiene [**DllMain.**](dllmain.md) Il caricatore di libreria acquisisce il blocco del caricatore L e quindi chiama **in DllMain.** Il thread principale crea gli oggetti di sincronizzazione A, B e G per serializzare l'accesso alle relative strutture di dati e quindi tenta di acquisire il blocco G. Un thread di lavoro che ha già acquisito correttamente il blocco G chiama quindi una funzione come GetModuleHandle che tenta di acquisire il blocco del caricatore L. Di conseguenza, il thread di lavoro viene bloccato in L e il thread principale viene bloccato in G, causando un deadlock.

![deadlock causato dall'inversione dell'ordine di blocco](images/fig2.png)

Per evitare deadlock causati dall'inversione dell'ordine di blocco, tutti i thread devono tentare di acquisire gli oggetti di sincronizzazione nell'ordine di caricamento definito in qualsiasi momento.

## <a name="best-practices-for-synchronization"></a>Procedure consigliate per la sincronizzazione

Si consideri una DLL che crea thread di lavoro come parte dell'inizializzazione. Al momento della pulizia della DLL, è necessario eseguire la sincronizzazione con tutti i thread di lavoro per assicurarsi che le strutture dei dati siano in uno stato coerente e quindi terminare i thread di lavoro. Attualmente non esiste un modo semplice per risolvere completamente il problema della sincronizzazione e dell'arresto delle DLL in un ambiente multithreading. In questa sezione vengono descritte le procedure consigliate correnti per la sincronizzazione dei thread durante l'arresto della DLL.

Sincronizzazione dei thread in [**DllMain durante**](dllmain.md) l'uscita dal processo

-   Al momento della chiamata di [**DllMain**](dllmain.md) all'uscita del processo, tutti i thread del processo sono stati puliti forzatamente ed è possibile che lo spazio degli indirizzi sia incoerente. In questo caso la sincronizzazione non è necessaria. In altre parole, il gestore DLL \_ PROCESS DETACH ideale è \_ vuoto.
-   Windows Vista garantisce che le strutture di dati principali (variabili di ambiente, directory corrente, heap dei processi e così via) siano in uno stato coerente. Tuttavia, altre strutture di dati possono essere danneggiate, quindi la pulizia della memoria non è sicura.
-   Lo stato persistente che deve essere salvato deve essere scaricato nell'archiviazione permanente.

Sincronizzazione dei thread in **DllMain** per DLL \_ THREAD DETACH durante lo \_ scaricamento della DLL

-   Quando la DLL viene scaricata, lo spazio indirizzi non viene buttato via. Pertanto, la DLL deve eseguire un arresto pulito. Sono inclusi la sincronizzazione dei thread, gli handle aperti, lo stato persistente e le risorse allocate.
-   La sincronizzazione dei thread è difficile perché l'attesa della chiusura dei thread in [**DllMain**](dllmain.md) può causare un deadlock. Ad esempio, la DLL A mantiene il blocco del caricatore. Segnala al thread T di uscire e attende la chiusura del thread. Il thread T viene chiuso e il caricatore tenta di acquisire il blocco del caricatore per chiamare **dllMain** della DLL A con DLL \_ THREAD \_ DETACH. Ciò causa un deadlock. Per ridurre al minimo il rischio di deadlock:
    -   DLL A ottiene un messaggio DLL THREAD DETACH nella dllMain e imposta un evento \_ \_ per il thread T, segnalando l'uscita. [](dllmain.md)
    -   Il thread T termina l'attività corrente, si porta a uno stato coerente, segnala la DLL A e attende all'infinito. Si noti che le routine di verifica della coerenza devono seguire le stesse restrizioni di [**DllMain**](dllmain.md) per evitare deadlock.
    -   DLL A termina T, sapendo che si trova in uno stato coerente.

Se una DLL viene scaricata dopo la creazione di tutti i relativi thread, ma prima dell'inizio dell'esecuzione, i thread potrebbero bloccarsi. Se la DLL ha creato thread nella **dllmain** come parte dell'inizializzazione, alcuni thread potrebbero non aver completato l'inizializzazione e il messaggio THREAD ATTACH della DLL è ancora in attesa di essere \_ recapitato alla \_ DLL. In questo caso, se la DLL viene scaricata, inizierà a terminare i thread. Tuttavia, alcuni thread possono essere bloccati dietro il blocco del caricatore. I messaggi THREAD ATTACH dll vengono elaborati dopo l'annullamento del mapping della \_ \_ DLL, causando l'arresto anomalo del processo.

## <a name="recommendations"></a>Consigli

Di seguito sono riportate le linee guida consigliate:

-   Usare Application Verifier per rilevare gli errori più comuni in [**DllMain.**](dllmain.md)
-   Se si usa un blocco privato all'interno [**di DllMain,**](dllmain.md)definire una gerarchia di blocco e usarla in modo coerente. Il blocco del caricatore deve essere nella parte inferiore della gerarchia.
-   Verificare che nessuna chiamata dipersi da un'altra DLL che potrebbe non essere ancora stata caricata completamente.
-   Eseguire inizializzazioni semplici in modo statico in fase di compilazione, anziché in [**DllMain.**](dllmain.md)
-   Rinvia tutte le chiamate in [**DllMain**](dllmain.md) che possono attendere fino a un secondo momento.
-   Posticipa le attività di inizializzazione che possono attendere fino a un secondo momento. Alcune condizioni di errore devono essere rilevate in anticipo in modo che l'applicazione possa gestire correttamente gli errori. Tuttavia, esistono compromessi tra questo rilevamento anticipato e la perdita di affidabilità che può derivare da tale rilevamento. Il rinvio dell'inizializzazione è spesso la scelta migliore.

 

 
