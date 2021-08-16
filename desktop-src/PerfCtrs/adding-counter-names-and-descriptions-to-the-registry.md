---
description: I nomi e le descrizioni di tutti gli oggetti prestazioni e dei relativi contatori vengono archiviati nel Registro di sistema.
ms.assetid: 6fdaccb0-45bc-48f2-8f63-3df0bdf1dca4
title: Aggiunta di nomi e descrizioni dei contatori al Registro di sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e58333e9694b9aa74ff1d5ade6a399aaa813e7735ea315be529587e813fec0fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117794056"
---
# <a name="adding-counter-names-and-descriptions-to-the-registry"></a>Aggiunta di nomi e descrizioni dei contatori al Registro di sistema

> [!IMPORTANT]
> A causa di limitazioni significative di prestazioni e affidabilità, il metodo per fornire i dati dei contatori delle prestazioni descritti in questo argomento potrebbe essere modificato o non disponibile in futuro. Microsoft consiglia invece di usare il metodo descritto in Fornire dati dei contatori usando la versione [2.0 per](providing-counter-data-using-version-2-0.md) la creazione di nuovi contatori delle prestazioni e di eseguire la migrazione dei contatori delle prestazioni esistenti per usare tale metodo.

I nomi e le descrizioni di tutti gli oggetti prestazione V1 e dei relativi contatori devono essere installati nel sistema. Per archiviare i nomi e le descrizioni per gli oggetti e i contatori dal [provider V1:](providing-counter-data.md)

- [Creare un file di intestazione](#creating-a-symbolic-constants-h-file) con estensione h contenente le costanti simboliche per gli offset per gli oggetti e i contatori.
- [Creare un file di inizializzazione (.INI)](#creating-an-initialization-ini-file) contenente le stringhe.
- Quando si installa il componente, [eseguire lo **strumento lodctr** per](#running-the-lodctr-tool) installare i nomi e le descrizioni nel Registro di sistema.
- Quando si disinstalla il componente, eseguire lo strumento unlodctr per rimuovere i nomi e le descrizioni dal Registro di sistema.

## <a name="creating-a-symbolic-constants-h-file"></a>Creazione di un file di costanti simboliche (con estensione h)

Creare un file di intestazione con estensione h che definisce costanti (macro) per gli offset per gli oggetti e i contatori forniti dal provider. L'intestazione H viene usata come input per **lodctr** durante l'installazione del provider e può essere usata anche dal codice C/C++ del provider.

I valori costanti devono essere consecutivi, anche numeri che iniziano con zero. Raggruppare le costanti in base agli oggetti ,ad esempio iniziare ogni gruppo con l'offset dell'oggetto e quindi seguire gli offset dei contatori per tale oggetto.

Le costanti nell'intestazione determinano l'ordine in cui i contatori vengono aggiunti al nome e al testo della Guida nel Registro di sistema. Il provider usa gli offset per determinare l'oggetto sottoposto a query e i valori di indice da utilizzare per la restituzione dei dati. Per informazioni dettagliate, [vedere Implementazione di OpenPerformanceData.](implementing-openperformancedata.md)

Di seguito viene illustrato un esempio di un file costante simbolico, denominato CounterOffsets.h, usato nell'esempio di DLL Di creazione di [un'estensione delle](creating-a-performance-extension-dll.md) prestazioni.

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

## <a name="creating-an-initialization-ini-file"></a>Creazione di un file di inizializzazione (.INI)

Il file di inizializzazione (.INI) contiene il nome e le stringhe della Guida per ogni oggetto e contatore definito nel file di simboli. Il .INI file viene usato come input per **lodctr** durante l'installazione del provider.

Il file .INI deve essere codificato come UTF-16LE (con byte order mark) e deve avere le sezioni e le chiavi seguenti:

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

### <a name="info-section"></a>Sezione [info]

La `[info]` sezione contiene informazioni generali sul provider. Le chiavi di sezione sono definite nel modo seguente:

|Chiave|Descrizione
|---|-----------
|**DriverName**| Specificare il nome della chiave delle prestazioni del provider che si trova nel Registro di sistema nella `HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services` chiave . Per informazioni sulla creazione di questa chiave, vedere [Creazione della chiave delle prestazioni dell'applicazione](creating-the-applications-performance-key.md).
|**SymbolFile**| Specificare il file di intestazione con estensione h che contiene i valori simbolici degli oggetti e dei contatori del provider. Durante l'installazione (quando si richiama **lodctr**), il file di intestazione deve essere nella stessa directory del file .INI file.
|**Trusted**| Se si include questa chiave nella sezione `[info]` , **lodctr** aggiungerà un valore del Registro di sistema Library Validation Code alla chiave delle prestazioni con una firma binaria della DLL delle prestazioni. Quando PERFLIB chiama la DLL, confronta la firma con la DLL per determinare se la DLL è stata modificata. Il valore della **chiave attendibile** viene ignorato.

Le `DriverName` chiavi e sono `SymbolFile` obbligatorie.

### <a name="objects-section"></a>Sezione [objects]

La `[objects]` sezione fornisce un elenco degli oggetti prestazioni supportati dal provider. Viene usato per determinare se ogni simbolo della sezione fa riferimento `[text]` a un oggetto o a un contatore.

Per ogni oggetto (counterset) supportato dal provider, aggiungere una chiave denominata alla sezione , dove è il nome dell'oggetto e è l'ID lingua di una `<symbol>_<langid>_NAME=` `[objects]` delle lingue `<symbol>` `<langid>` supportate. Il valore viene ignorato.

> [!IMPORTANT]
> La `[objects]` sezione migliora le prestazioni del sistema. Anche se la sezione objects è facoltativa, è necessario includere sempre questa sezione nel file .INI file. Se si include questa sezione, la DLL delle prestazioni viene chiamata solo se si supporta l'oggetto richiesto. Se non si include la sezione objects, la DLL viene chiamata per ogni query perché il sistema non conosce gli oggetti supportati dal provider. Se la sezione object non è inclusa, **lodctr** genera un messaggio nel registro eventi dell'applicazione che indica che il file .INI non contiene una sezione objects. L'identificatore dell'evento di questo messaggio è 2000.

### <a name="languages-section"></a>Sezione [languages]

La sezione fornisce un elenco degli identificatori di lingua di ogni lingua per cui il provider fornisce `[languages]` stringhe di nome e guida. Tutti i provider devono supportare `009` (inglese).

Per ogni lingua supportata, aggiungere una chiave denominata `<langid>=` . Il valore viene ignorato, ma a scopo di documentazione il valore viene in genere impostato sul nome della lingua corrispondente, ad esempio `009=English` .

Per la maggior parte delle lingue, è consigliabile usare l'identificatore di lingua principale. L'elenco completo degli identificatori di lingua si trova nel file di intestazione Winnt.h, sotto l'intestazione "Primary Language IDs". Convertire il valore trovato in Winnt.h in una sequenza di 3 cifre esadecimali rimuovendo il prefisso e aggiungendo cifre iniziali fino a quando la sequenza non è lunga `0x` `0` 3 cifre. Ad esempio, per specificare stringhe in inglese (0x9), usare 009. Per specificare stringhe italiane (0x10), usare 010.

Le lingue cinese e portoghese richiedono sia l'identificatore primario che quello secondario. Usare 404, 804, 416 o 816 anziché 004 o 016.

### <a name="text-section"></a>Sezione [text]

La `[text]` sezione fornisce il nome e le stringhe della Guida per gli oggetti e i contatori.

Per ogni oggetto o contatore e per ogni lingua supportata, è necessario specificare una chiave NAME (contenente il nome o la stringa del titolo per l'oggetto o il contatore) e facoltativamente è possibile specificare una chiave HELP (contenente la descrizione o la stringa di spiegazione per l'oggetto o il contatore). Le chiavi devono essere denominate e , dove è la costante simbolica per l'oggetto o il contatore (come definito nel file con estensione h della costante simbolica) e è l'identificatore di lingua usato per `<symbol>_<langid>_NAME` `<symbol>_<langid>_HELP` questa `<symbol>` `<langid>` stringa.

Ad esempio, le stringhe in inglese per un contatore con simbolo `MY_COUNTER` vengono specificate come segue:

```ini
MY_COUNTER_009_NAME=My Counter
MY_COUNTER_009_HELP=Description for My Counter.
```

Le chiavi di testo possono essere visualizzate in qualsiasi ordine. Le stringhe di testo non devono contenere caratteri di formattazione, ad esempio tabulazioni.

### <a name="example-ini-file"></a>File INI di esempio

Di seguito è riportato un esempio di un file di inizializzazione usato nell'esempio [Creazione di una DLL di estensione delle](creating-a-performance-extension-dll.md) prestazioni.

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

## <a name="running-the-lodctr-tool"></a>Esecuzione dello strumento Lodctr

Per caricare i nomi e le stringhe della Guida definiti nel file .INI (durante l'installazione del provider), eseguire lo strumento **lodctr** dalla cartella che contiene il file .INI e il file di intestazione. Lo strumento è incluso nel computer. È necessario eseguire **lodctr** con privilegi elevati. Il parametro per **lodctr** è il percorso del file .INI file. Ad esempio, `lodctr "C:\Program Files\MyCompany\MyProvider\MyProvider.ini"`.

Per scaricare i nomi e le stringhe della Guida (durante la disinstallazione), eseguire lo **strumento unlodctr.** È necessario eseguire **unlodctr** con privilegi elevati. Il parametro **da rimuovere è** driverName del provider (il nome della chiave delle prestazioni del provider). Ad esempio, `unlodctr "MyProvider"`.

Prima di **eseguire lodctr,** assicurarsi che l'applicazione abbia una voce sotto la **chiave** Servizi. Per informazioni dettagliate, vedere [Creazione della chiave delle prestazioni dell'applicazione.](creating-the-applications-performance-key.md) Se la chiave non esiste, **lodctr** non aggiornerà il Registro di sistema con i nomi e le descrizioni.

In alternativa all'esecuzione di **lodctr,** è possibile chiamare [**LoadPerfCounterTextStrings**](/windows/win32/api/loadperf/nf-loadperf-loadperfcountertextstringsw) (definito in Loadperf.h) dal programma di installazione per caricare le descrizioni dei nomi dei contatori. È quindi possibile chiamare [**UnloadPerfCounterTextStrings durante**](/windows/win32/api/loadperf/nf-loadperf-unloadperfcountertextstringsw) la disinstallazione.

**L'utilità lodctr** copia le stringhe dal file .INI nei valori del Registro di sistema **Counters** e **Help** nelle sottochiavi della lingua appropriate. Se la sottochiave della lingua corrispondente non esiste, le stringhe per tale lingua non vengono copiate. L'utilità aggiorna anche il **valore Last Counter** e Last **Help.** I nomi e le descrizioni dei contatori delle prestazioni vengono archiviati nel percorso seguente nel Registro di sistema.

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

Oltre ad aggiungere valori nella chiave **PerfLib,** lo strumento **lodctr** aggiunge anche i valori seguenti al nodo **Servizi** per l'applicazione. Nella maggior parte dei casi, l'applicazione e il provider avranno una relazione uno-a-uno. Tuttavia, un provider può fornire dati dei contatori per più applicazioni, motivo per cui la chiave è basata sull'applicazione e non sul provider.

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
