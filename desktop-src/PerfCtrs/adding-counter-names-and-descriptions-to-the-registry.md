---
description: I nomi e le descrizioni di tutti gli oggetti prestazioni e i rispettivi contatori vengono archiviati nel registro di sistema.
ms.assetid: 6fdaccb0-45bc-48f2-8f63-3df0bdf1dca4
title: Aggiunta di nomi e descrizioni dei contatori al Registro di sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e9d2c97ebe80a8ef2a8396ca42583cbad874859
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312193"
---
# <a name="adding-counter-names-and-descriptions-to-the-registry"></a>Aggiunta di nomi e descrizioni dei contatori al Registro di sistema

> [!IMPORTANT]
> A causa di limitazioni significative in merito a prestazioni e affidabilità, il metodo per fornire i dati dei contatori delle prestazioni descritti in questo argomento può essere modificato o non disponibile in futuro. Microsoft consiglia invece di usare il metodo descritto in [fornire dati del contatore usando la versione 2,0](providing-counter-data-using-version-2-0.md) per creare nuovi contatori delle prestazioni e migrare i contatori delle prestazioni esistenti per l'uso di tale metodo.

È necessario installare il sistema per i nomi e le descrizioni di tutti gli oggetti prestazione V1 e dei rispettivi contatori. Per archiviare i nomi e le descrizioni degli oggetti e dei contatori del [provider v1](providing-counter-data.md):

- [Creare un file di intestazione con estensione h](#creating-a-symbolic-constants-h-file) contenente le costanti simboliche per gli offset per gli oggetti e i contatori.
- [Creare un'inizializzazione (. INI)](#creating-an-initialization-ini-file) che contiene le stringhe.
- Quando si installa il componente, [eseguire lo strumento **lodctr**](#running-the-lodctr-tool) per installare i nomi e le descrizioni nel registro di sistema.
- Quando si disinstalla il componente, eseguire lo strumento unlodctr per rimuovere i nomi e le descrizioni dal registro di sistema.

## <a name="creating-a-symbolic-constants-h-file"></a>Creazione di un file di costanti simboliche (. h)

Creare un file di intestazione con estensione h che definisce le costanti (macro) per gli offset degli oggetti e dei contatori forniti dal provider. L'intestazione. h viene usata come input per **lodctr** durante l'installazione del provider e può anche essere usata dal codice C/C++ del provider.

I valori delle costanti devono essere consecutivi, persino i numeri a partire da zero. Raggruppare le costanti per oggetti, ovvero avviare ogni gruppo con l'offset dell'oggetto, quindi seguire gli offset dei contatori per l'oggetto.

Le costanti nell'intestazione determinano l'ordine in cui i contatori vengono aggiunti al nome e al testo della guida nel registro di sistema. Il provider utilizza gli offset per determinare l'oggetto su cui viene eseguita la query e i valori di indice da utilizzare per la restituzione dei dati. Per informazioni dettagliate, vedere [implementazione di OpenPerformanceData](implementing-openperformancedata.md).

Di seguito è riportato un esempio di un file di costante simbolico, denominato CounterOffsets. h, usato nell'esempio di [creazione di una DLL di estensione](creating-a-performance-extension-dll.md) per le prestazioni.

```C++
#ifndef OFFSETS_H
#define OFFSETS_H

// Symbol file that defines constant values for the objects
// and counters that the provider provides. The counters should be
// grouped by object.

#define TRANSFER_OBJECT      0 // First object must be at offset 0.
#define BYTES_SENT           2 // Counters for the object follow.
#define AVAILABLE_BANDWIDTH  4 // Offsets must be even numbers.

// Not required, but for convenience in implementing the Open function:
#define LAST_TRANSFER_OBJECT_COUNTER_OFFSET  AVAILABLE_BANDWIDTH

#define PEER_OBJECT          6 // Second object must be at the next offset.
#define BYTES_SERVED         8 // Counter for the second object.

// Not required, but for convenience in implementing the Open function:
#define LAST_PEER_OBJECT_COUNTER_OFFSET  BYTES_SERVED

#endif // OFFSETS_H
```

## <a name="creating-an-initialization-ini-file"></a>Creazione di un'inizializzazione (. File INI)

Inizializzazione (. INI) contiene il nome e le stringhe della Guida per ogni oggetto e contatore definito nel file di simboli. Il. Il file INI viene usato come input per **lodctr** durante l'installazione del provider.

Il. Il file INI deve essere codificato come UTF-16LE (con byte order mark) e deve contenere le sezioni e le chiavi seguenti:

```ini
[info]
drivername=ServiceKeyName
symbolfile=SymbolFile.h
trusted=(Unused)

[objects]
<symbol>_<langid>_NAME=(Unused)

[languages]
<langid>=(Unused)

[text]
<symbol>_<langid>_NAME=Name
<symbol>_<langid>_HELP=Description
```

### <a name="info-section"></a>[info] sezione

La `[info]` sezione contiene informazioni generali sul provider. Le chiavi della sezione sono definite come segue:

|Chiave|Descrizione
|---|-----------
|**DriverName**| Specificare il nome della chiave di prestazioni del provider che si trova nel registro di sistema sotto la `HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services` chiave. Per informazioni sulla creazione di questa chiave, vedere [creazione della chiave delle prestazioni dell'applicazione](creating-the-applications-performance-key.md).
|**SymbolFile**| Specificare il file di intestazione con estensione h che contiene i valori simbolici degli oggetti e dei contatori del provider. Durante l'installazione (quando si richiama **lodctr**), il file di intestazione deve trovarsi nella stessa directory della. File INI.
|**Attendibile**| Se si include questa chiave nella `[info]` sezione, **lodctr** aggiungerà un valore del registro di sistema del codice di convalida della libreria alla chiave delle prestazioni con una firma BINARIa della DLL delle prestazioni. Quando PERFLIB chiama la DLL, confronta la firma con la DLL per determinare se la DLL è stata modificata. Il valore della chiave **attendibile** viene ignorato.

Le `DriverName` `SymbolFile` chiavi e sono obbligatorie.

### <a name="objects-section"></a>sezione [Objects]

Nella `[objects]` sezione viene fornito un elenco degli oggetti prestazioni supportati dal provider. Viene utilizzato per determinare se ogni simbolo della `[text]` sezione fa riferimento a un oggetto o a un contatore.

Per ogni oggetto (contatore) supportato dal provider, aggiungere una chiave denominata `<symbol>_<langid>_NAME=` alla `[objects]` sezione, dove `<symbol>` è il nome dell'oggetto e `<langid>` è l'ID lingua di una delle lingue supportate. Il valore viene ignorato.

> [!IMPORTANT]
> La `[objects]` sezione migliora le prestazioni del sistema. Anche se la sezione oggetti è facoltativa, è necessario includere sempre questa sezione nel. File INI. Se si include questa sezione, la DLL delle prestazioni viene chiamata solo se si supporta l'oggetto richiesto. Se non si include la sezione Objects, la DLL viene chiamata per ogni query, perché il sistema non sa quali oggetti sono supportati dal provider. Se la sezione dell'oggetto non è inclusa, **lodctr** genera un messaggio nel registro eventi dell'applicazione che informa che. Il file INI non contiene una sezione oggetti. L'identificatore di evento di questo messaggio è 2000.

### <a name="languages-section"></a>sezione [languages]

Nella `[languages]` sezione viene fornito un elenco degli identificatori di lingua di ogni lingua per cui il provider fornisce le stringhe di nome e guida. Tutti i provider devono supportare `009` (Inglese).

Per ogni lingua supportata, aggiungere una chiave denominata `<langid>=` . Il valore viene ignorato, ma per finalità di documentazione il valore viene in genere impostato sul nome della lingua corrispondente, ad esempio `009=English` .

Per la maggior parte delle lingue, è necessario usare l'identificatore di lingua principale. L'elenco completo degli identificatori di lingua si trova nel file di intestazione Winnt. h, sotto l'intestazione "ID lingua primaria". Convertire il valore trovato in Winnt. h in una sequenza di 3 cifre esadecimali rimuovendo il `0x` prefisso e aggiungendo le `0` cifre iniziali finché la sequenza non ha una lunghezza di 3 cifre. Ad esempio, per specificare le stringhe inglesi (0x9), usare 009. Per specificare le stringhe italiane (0x10), usare 010.

Per le lingue cinese e portoghese sono necessari sia gli identificatori primari che quelli della lingua. Usare 404, 804, 416 o 816 anziché 004 o 016.

### <a name="text-section"></a>sezione [testo]

La `[text]` sezione fornisce il nome e le stringhe della Guida per gli oggetti e i contatori.

Per ogni oggetto o contatore e per ogni lingua supportata, è necessario specificare una chiave del nome (contenente il nome o la stringa del titolo per l'oggetto o il contatore) ed è possibile specificare facoltativamente un tasto guida (contenente la stringa di descrizione o di spiegazione per l'oggetto o il contatore). Le chiavi devono essere denominate `<symbol>_<langid>_NAME` e `<symbol>_<langid>_HELP` , dove `<symbol>` è la costante simbolica per l'oggetto o il contatore (come definito nel file con estensione h della costante simbolica) e `<langid>` è l'identificatore di lingua usato per questa stringa.

Ad esempio, le stringhe inglesi per un contatore con simbolo `MY_COUNTER` vengono specificate come:

```ini
MY_COUNTER_009_NAME=My Counter
MY_COUNTER_009_HELP=Description for My Counter.
```

Le chiavi di testo possono essere visualizzate in qualsiasi ordine. Le stringhe di testo non devono contenere caratteri di formattazione come le schede.

### <a name="example-ini-file"></a>File INI di esempio

Di seguito è riportato un esempio di un file di inizializzazione usato nell'esempio [Creating a performance Extension DLL](creating-a-performance-extension-dll.md) .

```ini
[info]
drivername=MyApplication
symbolfile=CounterOffsets.h
trusted=

[objects]
TRANSFER_OBJECT_009_NAME=
PEER_OBJECT_009_NAME=

[languages]
009=English
00C=French

[text]

// English strings

TRANSFER_OBJECT_009_NAME=Transfer
TRANSFER_OBJECT_009_HELP=Provides information related to transferring files.

BYTES_SENT_009_NAME=Bytes Sent
BYTES_SENT_009_HELP=Number of bytes sent in the last transfer.

AVAILABLE_BANDWIDTH_009_NAME=Available Bandwidth
AVAILABLE_BANDWIDTH_009_HELP=Available bandwidth on the network, in bytes.

PEER_OBJECT_009_NAME=Peer
PEER_OBJECT_009_HELP=Provides information related to peer-caching.

BYTES_SERVED_009_NAME=Bytes Served
BYTES_SERVED_009_HELP=Number of bytes served from the cache.

// French strings

TRANSFER_OBJECT_00C_NAME=Transfert
TRANSFER_OBJECT_00C_HELP=Fournit des informations liées aux transferts de fichiers.

BYTES_SENT_00C_NAME=Octets Envoyés
BYTES_SENT_00C_HELP=Nombre d'octets envoyés dans le dernier transfert.

AVAILABLE_BANDWIDTH_00C_NAME=Bande Passante Disponible
AVAILABLE_BANDWIDTH_00C_HELP=Bande passante disponible sur le réseau, en octets.

PEER_OBJECT_00C_NAME=Pair
PEER_OBJECT_00C_HELP=Fournit des informations liées é mise en cache homologue.

BYTES_SERVED_00C_NAME=Octets Servis
BYTES_SERVED_00C_HELP=Le nombre d'octets servis du cache.
```

## <a name="running-the-lodctr-tool"></a>Esecuzione dello strumento lodctr

Per caricare i nomi e le stringhe della guida definiti nel. File INI (durante l'installazione del provider) eseguire lo strumento **lodctr** dalla cartella che contiene il. File INI e file di intestazione. Lo strumento è incluso nel computer. È necessario eseguire **lodctr** con privilegi elevati. Il parametro per **lodctr** è il percorso di. File INI. Ad esempio: `lodctr "C:\Program Files\MyCompany\MyProvider\MyProvider.ini"`.

Per scaricare i nomi e le stringhe della guida (durante la disinstallazione), eseguire lo strumento **unlodctr** . È necessario eseguire **unlodctr** con privilegi elevati. Il parametro per **unlodctr** è il nome del driver del provider (il nome della chiave di prestazioni del provider). Ad esempio: `unlodctr "MyProvider"`.

Prima di eseguire **lodctr**, assicurarsi che l'applicazione disponga di una voce sotto la chiave **Services** . Per informazioni dettagliate, vedere [creazione della chiave delle prestazioni dell'applicazione](creating-the-applications-performance-key.md). Se la chiave non esiste, **lodctr** non aggiornerà il registro di sistema con i nomi e le descrizioni.

In alternativa all'esecuzione di **lodctr**, è possibile chiamare [**LoadPerfCounterTextStrings**](/windows/win32/api/loadperf/nf-loadperf-loadperfcountertextstringsw) (definito in loadperf. h) dal programma di installazione per caricare le descrizioni dei nomi dei contatori. È quindi possibile chiamare [**UnloadPerfCounterTextStrings**](/windows/win32/api/loadperf/nf-loadperf-unloadperfcountertextstringsw) durante la disinstallazione.

L'utilità **lodctr** copia le stringhe da. File INI nei **contatori** e valori del registro di sistema nelle sottochiavi **di lingua** appropriate. Se la sottochiave della lingua corrispondente non esiste, le stringhe per tale lingua non vengono copiate. L'utilità aggiorna anche l' **ultimo contatore** e l'ultimo valore della **Guida** . I nomi e le descrizioni dei contatori delle prestazioni vengono archiviati nel seguente percorso del registro di sistema.

```
HKEY_LOCAL_MACHINE
   \SOFTWARE
      \Microsoft
         \Windows NT
            \CurrentVersion
               \Perflib
                  Last Counter = highest counter index
                  Last Help = highest help index
                  \009
                     Counters = 2 System 4 Memory...
                     Help = 3 The System Object Type...
                  \supported language, other than English
                     Counters = ...
                     Help = ...
```

Oltre ad aggiungere valori nella chiave **Perflib** , lo strumento **lodctr** aggiunge anche i valori seguenti al nodo **Servizi** per l'applicazione. Nella maggior parte dei casi, l'applicazione e il provider avranno una relazione uno-a-uno. Tuttavia, è possibile che un provider fornisca dati del contatore per più applicazioni, motivo per cui la chiave è basata sull'applicazione e non sul provider.

```
HKEY_LOCAL_MACHINE
   \SYSTEM
      \CurrentControlSet
         \Services
            \MyApplication
               \Performance
                  First Counter = lowest counter index assigned to provider
                  First Help = lowest help index assigned to provider
                  Last Counter = highest counter index assigned to provider
                  Last Help = highest help index assigned to provider
                  Object List = list of object index values if the .INI includes the [objects] section
                  Library Validation Code = if the [info] section contains a "trusted" key
```
