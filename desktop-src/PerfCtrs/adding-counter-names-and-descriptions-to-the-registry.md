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
# <a name="adding-counter-names-and-descriptions-to-the-registry"></a><span data-ttu-id="4ad50-103">Aggiunta di nomi e descrizioni dei contatori al Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="4ad50-103">Adding Counter Names and Descriptions to the Registry</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4ad50-104">A causa di limitazioni significative in merito a prestazioni e affidabilità, il metodo per fornire i dati dei contatori delle prestazioni descritti in questo argomento può essere modificato o non disponibile in futuro.</span><span class="sxs-lookup"><span data-stu-id="4ad50-104">Due to significant performance and reliability limitations, the method for providing performance counter data that this topic describes may be altered or unavailable in the future.</span></span> <span data-ttu-id="4ad50-105">Microsoft consiglia invece di usare il metodo descritto in [fornire dati del contatore usando la versione 2,0](providing-counter-data-using-version-2-0.md) per creare nuovi contatori delle prestazioni e migrare i contatori delle prestazioni esistenti per l'uso di tale metodo.</span><span class="sxs-lookup"><span data-stu-id="4ad50-105">Instead, Microsoft recommends that you use the method described in [Providing Counter Data Using Version 2.0](providing-counter-data-using-version-2-0.md) for creating new performance counters and that you migrate existing performance counters to use that method.</span></span>

<span data-ttu-id="4ad50-106">È necessario installare il sistema per i nomi e le descrizioni di tutti gli oggetti prestazione V1 e dei rispettivi contatori.</span><span class="sxs-lookup"><span data-stu-id="4ad50-106">The names and descriptions of all V1 performance objects and their counters must be installed the system.</span></span> <span data-ttu-id="4ad50-107">Per archiviare i nomi e le descrizioni degli oggetti e dei contatori del [provider v1](providing-counter-data.md):</span><span class="sxs-lookup"><span data-stu-id="4ad50-107">To store names and descriptions for the objects and counters from your [V1 provider](providing-counter-data.md):</span></span>

- <span data-ttu-id="4ad50-108">[Creare un file di intestazione con estensione h](#creating-a-symbolic-constants-h-file) contenente le costanti simboliche per gli offset per gli oggetti e i contatori.</span><span class="sxs-lookup"><span data-stu-id="4ad50-108">[Create a .h header file](#creating-a-symbolic-constants-h-file) that contains the symbolic constants for the offsets to your objects and counters.</span></span>
- <span data-ttu-id="4ad50-109">[Creare un'inizializzazione (. INI)](#creating-an-initialization-ini-file) che contiene le stringhe.</span><span class="sxs-lookup"><span data-stu-id="4ad50-109">[Create an initialization (.INI) file](#creating-an-initialization-ini-file) that contains the strings.</span></span>
- <span data-ttu-id="4ad50-110">Quando si installa il componente, [eseguire lo strumento **lodctr**](#running-the-lodctr-tool) per installare i nomi e le descrizioni nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="4ad50-110">When installing your component, [run the **lodctr** tool](#running-the-lodctr-tool) to install the names and descriptions into the registry.</span></span>
- <span data-ttu-id="4ad50-111">Quando si disinstalla il componente, eseguire lo strumento unlodctr per rimuovere i nomi e le descrizioni dal registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="4ad50-111">When uninstalling your component, run the unlodctr tool to remove the names and descriptions from the registry.</span></span>

## <a name="creating-a-symbolic-constants-h-file"></a><span data-ttu-id="4ad50-112">Creazione di un file di costanti simboliche (. h)</span><span class="sxs-lookup"><span data-stu-id="4ad50-112">Creating a symbolic constants (.h) file</span></span>

<span data-ttu-id="4ad50-113">Creare un file di intestazione con estensione h che definisce le costanti (macro) per gli offset degli oggetti e dei contatori forniti dal provider.</span><span class="sxs-lookup"><span data-stu-id="4ad50-113">Create a .h header file that defines constants (macros) for the offsets to the objects and counters that your provider provides.</span></span> <span data-ttu-id="4ad50-114">L'intestazione. h viene usata come input per **lodctr** durante l'installazione del provider e può anche essere usata dal codice C/C++ del provider.</span><span class="sxs-lookup"><span data-stu-id="4ad50-114">The .h header is used as input to **lodctr** during installation of your provider, and may also be used by the C/C++ code of your provider.</span></span>

<span data-ttu-id="4ad50-115">I valori delle costanti devono essere consecutivi, persino i numeri a partire da zero.</span><span class="sxs-lookup"><span data-stu-id="4ad50-115">The constant values must be consecutive, even numbers beginning with zero.</span></span> <span data-ttu-id="4ad50-116">Raggruppare le costanti per oggetti, ovvero avviare ogni gruppo con l'offset dell'oggetto, quindi seguire gli offset dei contatori per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="4ad50-116">Group the constants by objects (i.e. start each group with the object offset, then follow with the offsets of the counters for that object).</span></span>

<span data-ttu-id="4ad50-117">Le costanti nell'intestazione determinano l'ordine in cui i contatori vengono aggiunti al nome e al testo della guida nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="4ad50-117">The constants in the header determine the order in which the counters are added to the name and help text in the registry.</span></span> <span data-ttu-id="4ad50-118">Il provider utilizza gli offset per determinare l'oggetto su cui viene eseguita la query e i valori di indice da utilizzare per la restituzione dei dati.</span><span class="sxs-lookup"><span data-stu-id="4ad50-118">The provider uses the offsets to determine which object is being queried and the index values to use when returning the data.</span></span> <span data-ttu-id="4ad50-119">Per informazioni dettagliate, vedere [implementazione di OpenPerformanceData](implementing-openperformancedata.md).</span><span class="sxs-lookup"><span data-stu-id="4ad50-119">For details, see [Implementing OpenPerformanceData](implementing-openperformancedata.md).</span></span>

<span data-ttu-id="4ad50-120">Di seguito è riportato un esempio di un file di costante simbolico, denominato CounterOffsets. h, usato nell'esempio di [creazione di una DLL di estensione](creating-a-performance-extension-dll.md) per le prestazioni.</span><span class="sxs-lookup"><span data-stu-id="4ad50-120">The following shows an example of a symbolic constant file, named CounterOffsets.h, that is used in the [Creating a Performance Extension DLL](creating-a-performance-extension-dll.md) example.</span></span>

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

## <a name="creating-an-initialization-ini-file"></a><span data-ttu-id="4ad50-121">Creazione di un'inizializzazione (. File INI)</span><span class="sxs-lookup"><span data-stu-id="4ad50-121">Creating an initialization (.INI) file</span></span>

<span data-ttu-id="4ad50-122">Inizializzazione (. INI) contiene il nome e le stringhe della Guida per ogni oggetto e contatore definito nel file di simboli.</span><span class="sxs-lookup"><span data-stu-id="4ad50-122">The initialization (.INI) file contains the name and help strings for each object and counter defined in your symbol file.</span></span> <span data-ttu-id="4ad50-123">Il. Il file INI viene usato come input per **lodctr** durante l'installazione del provider.</span><span class="sxs-lookup"><span data-stu-id="4ad50-123">The .INI file is used as input to **lodctr** during installation of your provider.</span></span>

<span data-ttu-id="4ad50-124">Il. Il file INI deve essere codificato come UTF-16LE (con byte order mark) e deve contenere le sezioni e le chiavi seguenti:</span><span class="sxs-lookup"><span data-stu-id="4ad50-124">The .INI file should be encoded as UTF-16LE (with byte order mark) and should have the following sections and keys:</span></span>

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

### <a name="info-section"></a><span data-ttu-id="4ad50-125">[info] sezione</span><span class="sxs-lookup"><span data-stu-id="4ad50-125">[info] section</span></span>

<span data-ttu-id="4ad50-126">La `[info]` sezione contiene informazioni generali sul provider.</span><span class="sxs-lookup"><span data-stu-id="4ad50-126">The `[info]` section contains general information about the provider.</span></span> <span data-ttu-id="4ad50-127">Le chiavi della sezione sono definite come segue:</span><span class="sxs-lookup"><span data-stu-id="4ad50-127">The section keys are defined as follows:</span></span>

|<span data-ttu-id="4ad50-128">Chiave</span><span class="sxs-lookup"><span data-stu-id="4ad50-128">Key</span></span>|<span data-ttu-id="4ad50-129">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4ad50-129">Description</span></span>
|---|-----------
|<span data-ttu-id="4ad50-130">**DriverName**</span><span class="sxs-lookup"><span data-stu-id="4ad50-130">**DriverName**</span></span>| <span data-ttu-id="4ad50-131">Specificare il nome della chiave di prestazioni del provider che si trova nel registro di sistema sotto la `HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services` chiave.</span><span class="sxs-lookup"><span data-stu-id="4ad50-131">Specify the name of the provider's performance key located in the registry under the `HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services` key.</span></span> <span data-ttu-id="4ad50-132">Per informazioni sulla creazione di questa chiave, vedere [creazione della chiave delle prestazioni dell'applicazione](creating-the-applications-performance-key.md).</span><span class="sxs-lookup"><span data-stu-id="4ad50-132">For information on creating this key, see [Creating the Application's Performance Key](creating-the-applications-performance-key.md).</span></span>
|<span data-ttu-id="4ad50-133">**SymbolFile**</span><span class="sxs-lookup"><span data-stu-id="4ad50-133">**SymbolFile**</span></span>| <span data-ttu-id="4ad50-134">Specificare il file di intestazione con estensione h che contiene i valori simbolici degli oggetti e dei contatori del provider.</span><span class="sxs-lookup"><span data-stu-id="4ad50-134">Specify the .h header file that contains symbolic values of your provider's objects and counters.</span></span> <span data-ttu-id="4ad50-135">Durante l'installazione (quando si richiama **lodctr**), il file di intestazione deve trovarsi nella stessa directory della. File INI.</span><span class="sxs-lookup"><span data-stu-id="4ad50-135">During installation (when invoking **lodctr**), the header file must be in the same directory as the .INI file.</span></span>
|<span data-ttu-id="4ad50-136">**Attendibile**</span><span class="sxs-lookup"><span data-stu-id="4ad50-136">**Trusted**</span></span>| <span data-ttu-id="4ad50-137">Se si include questa chiave nella `[info]` sezione, **lodctr** aggiungerà un valore del registro di sistema del codice di convalida della libreria alla chiave delle prestazioni con una firma BINARIa della DLL delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="4ad50-137">If you include this key in the `[info]` section, **lodctr** will add a Library Validation Code registry value to your performance key with a binary signature of your performance DLL.</span></span> <span data-ttu-id="4ad50-138">Quando PERFLIB chiama la DLL, confronta la firma con la DLL per determinare se la DLL è stata modificata.</span><span class="sxs-lookup"><span data-stu-id="4ad50-138">When PERFLIB calls your DLL it compares the signature with your DLL to determine if the DLL has been modified.</span></span> <span data-ttu-id="4ad50-139">Il valore della chiave **attendibile** viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="4ad50-139">The value of the **Trusted** key is ignored.</span></span>

<span data-ttu-id="4ad50-140">Le `DriverName` `SymbolFile` chiavi e sono obbligatorie.</span><span class="sxs-lookup"><span data-stu-id="4ad50-140">The `DriverName` and `SymbolFile` keys are required.</span></span>

### <a name="objects-section"></a><span data-ttu-id="4ad50-141">sezione [Objects]</span><span class="sxs-lookup"><span data-stu-id="4ad50-141">[objects] section</span></span>

<span data-ttu-id="4ad50-142">Nella `[objects]` sezione viene fornito un elenco degli oggetti prestazioni supportati dal provider.</span><span class="sxs-lookup"><span data-stu-id="4ad50-142">The `[objects]` section provides a list of the performance objects that the provider supports.</span></span> <span data-ttu-id="4ad50-143">Viene utilizzato per determinare se ogni simbolo della `[text]` sezione fa riferimento a un oggetto o a un contatore.</span><span class="sxs-lookup"><span data-stu-id="4ad50-143">This is used to determine whether each symbol from the `[text]` section refers an object or a counter.</span></span>

<span data-ttu-id="4ad50-144">Per ogni oggetto (contatore) supportato dal provider, aggiungere una chiave denominata `<symbol>_<langid>_NAME=` alla `[objects]` sezione, dove `<symbol>` è il nome dell'oggetto e `<langid>` è l'ID lingua di una delle lingue supportate.</span><span class="sxs-lookup"><span data-stu-id="4ad50-144">For each object (counterset) supported by your provider, add one key named `<symbol>_<langid>_NAME=` to the `[objects]` section, where `<symbol>` is the name of the object and `<langid>` is the language id of one of the supported languages.</span></span> <span data-ttu-id="4ad50-145">Il valore viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="4ad50-145">The value is ignored.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4ad50-146">La `[objects]` sezione migliora le prestazioni del sistema.</span><span class="sxs-lookup"><span data-stu-id="4ad50-146">The `[objects]` section improves the performance of the system.</span></span> <span data-ttu-id="4ad50-147">Anche se la sezione oggetti è facoltativa, è necessario includere sempre questa sezione nel. File INI.</span><span class="sxs-lookup"><span data-stu-id="4ad50-147">Although the objects section is optional, you should always include this section in your .INI file.</span></span> <span data-ttu-id="4ad50-148">Se si include questa sezione, la DLL delle prestazioni viene chiamata solo se si supporta l'oggetto richiesto.</span><span class="sxs-lookup"><span data-stu-id="4ad50-148">If you include this section, your performance DLL is called only if you support the requested object.</span></span> <span data-ttu-id="4ad50-149">Se non si include la sezione Objects, la DLL viene chiamata per ogni query, perché il sistema non sa quali oggetti sono supportati dal provider.</span><span class="sxs-lookup"><span data-stu-id="4ad50-149">If you do not include the objects section, your DLL is called for every query because the system does not know which objects your provider supports.</span></span> <span data-ttu-id="4ad50-150">Se la sezione dell'oggetto non è inclusa, **lodctr** genera un messaggio nel registro eventi dell'applicazione che informa che. Il file INI non contiene una sezione oggetti.</span><span class="sxs-lookup"><span data-stu-id="4ad50-150">If the object section is not included, **lodctr** generates a message in the application event log stating that the .INI file did not contain an objects section.</span></span> <span data-ttu-id="4ad50-151">L'identificatore di evento di questo messaggio è 2000.</span><span class="sxs-lookup"><span data-stu-id="4ad50-151">The event identifier of this message is 2000.</span></span>

### <a name="languages-section"></a><span data-ttu-id="4ad50-152">sezione [languages]</span><span class="sxs-lookup"><span data-stu-id="4ad50-152">[languages] section</span></span>

<span data-ttu-id="4ad50-153">Nella `[languages]` sezione viene fornito un elenco degli identificatori di lingua di ogni lingua per cui il provider fornisce le stringhe di nome e guida.</span><span class="sxs-lookup"><span data-stu-id="4ad50-153">The `[languages]` section provides a list of the language identifiers of each language for which your provider supplies name and help strings.</span></span> <span data-ttu-id="4ad50-154">Tutti i provider devono supportare `009` (Inglese).</span><span class="sxs-lookup"><span data-stu-id="4ad50-154">All providers should support `009` (English).</span></span>

<span data-ttu-id="4ad50-155">Per ogni lingua supportata, aggiungere una chiave denominata `<langid>=` .</span><span class="sxs-lookup"><span data-stu-id="4ad50-155">For each supported language, add one key named `<langid>=`.</span></span> <span data-ttu-id="4ad50-156">Il valore viene ignorato, ma per finalità di documentazione il valore viene in genere impostato sul nome della lingua corrispondente, ad esempio `009=English` .</span><span class="sxs-lookup"><span data-stu-id="4ad50-156">The value is ignored, but for documentation purposes the value is normally set to the name of the corresponding language, e.g. `009=English`.</span></span>

<span data-ttu-id="4ad50-157">Per la maggior parte delle lingue, è necessario usare l'identificatore di lingua principale.</span><span class="sxs-lookup"><span data-stu-id="4ad50-157">For most languages, you should use the primary language identifier.</span></span> <span data-ttu-id="4ad50-158">L'elenco completo degli identificatori di lingua si trova nel file di intestazione Winnt. h, sotto l'intestazione "ID lingua primaria".</span><span class="sxs-lookup"><span data-stu-id="4ad50-158">The complete list of language identifiers is in the Winnt.h header file, under the heading "Primary Language Ids."</span></span> <span data-ttu-id="4ad50-159">Convertire il valore trovato in Winnt. h in una sequenza di 3 cifre esadecimali rimuovendo il `0x` prefisso e aggiungendo le `0` cifre iniziali finché la sequenza non ha una lunghezza di 3 cifre.</span><span class="sxs-lookup"><span data-stu-id="4ad50-159">Convert the value found in Winnt.h into a sequence of 3 hexadecimal digits by removing the `0x` prefix and adding leading `0` digits until the sequence is 3 digits long.</span></span> <span data-ttu-id="4ad50-160">Ad esempio, per specificare le stringhe inglesi (0x9), usare 009.</span><span class="sxs-lookup"><span data-stu-id="4ad50-160">For example, to specify English strings (0x9), use 009.</span></span> <span data-ttu-id="4ad50-161">Per specificare le stringhe italiane (0x10), usare 010.</span><span class="sxs-lookup"><span data-stu-id="4ad50-161">To specify Italian strings (0x10), use 010.</span></span>

<span data-ttu-id="4ad50-162">Per le lingue cinese e portoghese sono necessari sia gli identificatori primari che quelli della lingua.</span><span class="sxs-lookup"><span data-stu-id="4ad50-162">Chinese and Portuguese languages require both the primary and sublanguage identifiers.</span></span> <span data-ttu-id="4ad50-163">Usare 404, 804, 416 o 816 anziché 004 o 016.</span><span class="sxs-lookup"><span data-stu-id="4ad50-163">Use 404, 804, 416, or 816 instead of 004 or 016.</span></span>

### <a name="text-section"></a><span data-ttu-id="4ad50-164">sezione [testo]</span><span class="sxs-lookup"><span data-stu-id="4ad50-164">[text] section</span></span>

<span data-ttu-id="4ad50-165">La `[text]` sezione fornisce il nome e le stringhe della Guida per gli oggetti e i contatori.</span><span class="sxs-lookup"><span data-stu-id="4ad50-165">The `[text]` section provides the name and help strings for your objects and counters.</span></span>

<span data-ttu-id="4ad50-166">Per ogni oggetto o contatore e per ogni lingua supportata, è necessario specificare una chiave del nome (contenente il nome o la stringa del titolo per l'oggetto o il contatore) ed è possibile specificare facoltativamente un tasto guida (contenente la stringa di descrizione o di spiegazione per l'oggetto o il contatore).</span><span class="sxs-lookup"><span data-stu-id="4ad50-166">For each object or counter, and for each supported language, you must provide a NAME key (containing the name or title string for your object or counter) and you may optionally provide a HELP key (containing the description or explanation string for your object or counter).</span></span> <span data-ttu-id="4ad50-167">Le chiavi devono essere denominate `<symbol>_<langid>_NAME` e `<symbol>_<langid>_HELP` , dove `<symbol>` è la costante simbolica per l'oggetto o il contatore (come definito nel file con estensione h della costante simbolica) e `<langid>` è l'identificatore di lingua usato per questa stringa.</span><span class="sxs-lookup"><span data-stu-id="4ad50-167">The keys should be named `<symbol>_<langid>_NAME` and `<symbol>_<langid>_HELP`, where `<symbol>` is the symbolic constant for the object or counter (as defined in the symbolic constant .h file), and `<langid>` is the language identifier used for this string.</span></span>

<span data-ttu-id="4ad50-168">Ad esempio, le stringhe inglesi per un contatore con simbolo `MY_COUNTER` vengono specificate come:</span><span class="sxs-lookup"><span data-stu-id="4ad50-168">For example, the English strings for a counter with symbol `MY_COUNTER` would be specified as:</span></span>

```ini
MY_COUNTER_009_NAME=My Counter
MY_COUNTER_009_HELP=Description for My Counter.
```

<span data-ttu-id="4ad50-169">Le chiavi di testo possono essere visualizzate in qualsiasi ordine.</span><span class="sxs-lookup"><span data-stu-id="4ad50-169">The text keys can appear in any order.</span></span> <span data-ttu-id="4ad50-170">Le stringhe di testo non devono contenere caratteri di formattazione come le schede.</span><span class="sxs-lookup"><span data-stu-id="4ad50-170">The text strings should not contain formatting characters such as tabs.</span></span>

### <a name="example-ini-file"></a><span data-ttu-id="4ad50-171">File INI di esempio</span><span class="sxs-lookup"><span data-stu-id="4ad50-171">Example INI file</span></span>

<span data-ttu-id="4ad50-172">Di seguito è riportato un esempio di un file di inizializzazione usato nell'esempio [Creating a performance Extension DLL](creating-a-performance-extension-dll.md) .</span><span class="sxs-lookup"><span data-stu-id="4ad50-172">The following is an example of an initialization file that is used in the [Creating a Performance Extension DLL](creating-a-performance-extension-dll.md) sample.</span></span>

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

## <a name="running-the-lodctr-tool"></a><span data-ttu-id="4ad50-173">Esecuzione dello strumento lodctr</span><span class="sxs-lookup"><span data-stu-id="4ad50-173">Running the Lodctr tool</span></span>

<span data-ttu-id="4ad50-174">Per caricare i nomi e le stringhe della guida definiti nel. File INI (durante l'installazione del provider) eseguire lo strumento **lodctr** dalla cartella che contiene il. File INI e file di intestazione.</span><span class="sxs-lookup"><span data-stu-id="4ad50-174">To load the names and help strings defined in your .INI file (during the installation of your provider), run the **lodctr** tool from the folder that contains your .INI file and header file.</span></span> <span data-ttu-id="4ad50-175">Lo strumento è incluso nel computer.</span><span class="sxs-lookup"><span data-stu-id="4ad50-175">The tool is included with the computer.</span></span> <span data-ttu-id="4ad50-176">È necessario eseguire **lodctr** con privilegi elevati.</span><span class="sxs-lookup"><span data-stu-id="4ad50-176">You must run **lodctr** with elevated privileges.</span></span> <span data-ttu-id="4ad50-177">Il parametro per **lodctr** è il percorso di. File INI.</span><span class="sxs-lookup"><span data-stu-id="4ad50-177">The parameter to **lodctr** is the path to your .INI file.</span></span> <span data-ttu-id="4ad50-178">Ad esempio: `lodctr "C:\Program Files\MyCompany\MyProvider\MyProvider.ini"`.</span><span class="sxs-lookup"><span data-stu-id="4ad50-178">For example, `lodctr "C:\Program Files\MyCompany\MyProvider\MyProvider.ini"`.</span></span>

<span data-ttu-id="4ad50-179">Per scaricare i nomi e le stringhe della guida (durante la disinstallazione), eseguire lo strumento **unlodctr** .</span><span class="sxs-lookup"><span data-stu-id="4ad50-179">To unload the names and help strings (during uninstall), run the **unlodctr** tool.</span></span> <span data-ttu-id="4ad50-180">È necessario eseguire **unlodctr** con privilegi elevati.</span><span class="sxs-lookup"><span data-stu-id="4ad50-180">You must run **unlodctr** with elevated privileges.</span></span> <span data-ttu-id="4ad50-181">Il parametro per **unlodctr** è il nome del driver del provider (il nome della chiave di prestazioni del provider).</span><span class="sxs-lookup"><span data-stu-id="4ad50-181">The parameter to **unlodctr** is the DriverName of your provider (the name of the provider's performance key).</span></span> <span data-ttu-id="4ad50-182">Ad esempio: `unlodctr "MyProvider"`.</span><span class="sxs-lookup"><span data-stu-id="4ad50-182">For example, `unlodctr "MyProvider"`.</span></span>

<span data-ttu-id="4ad50-183">Prima di eseguire **lodctr**, assicurarsi che l'applicazione disponga di una voce sotto la chiave **Services** .</span><span class="sxs-lookup"><span data-stu-id="4ad50-183">Before running **lodctr**, be sure that your application has an entry under the **Services** key.</span></span> <span data-ttu-id="4ad50-184">Per informazioni dettagliate, vedere [creazione della chiave delle prestazioni dell'applicazione](creating-the-applications-performance-key.md).</span><span class="sxs-lookup"><span data-stu-id="4ad50-184">For details, see [Creating the Application's Performance Key](creating-the-applications-performance-key.md).</span></span> <span data-ttu-id="4ad50-185">Se la chiave non esiste, **lodctr** non aggiornerà il registro di sistema con i nomi e le descrizioni.</span><span class="sxs-lookup"><span data-stu-id="4ad50-185">If the key does not exist, **lodctr** will not update the registry with your names and descriptions.</span></span>

<span data-ttu-id="4ad50-186">In alternativa all'esecuzione di **lodctr**, è possibile chiamare [**LoadPerfCounterTextStrings**](/windows/win32/api/loadperf/nf-loadperf-loadperfcountertextstringsw) (definito in loadperf. h) dal programma di installazione per caricare le descrizioni dei nomi dei contatori.</span><span class="sxs-lookup"><span data-stu-id="4ad50-186">As an alternative to running **lodctr**, you can call [**LoadPerfCounterTextStrings**](/windows/win32/api/loadperf/nf-loadperf-loadperfcountertextstringsw) (defined in Loadperf.h) from your installation program to load your counter names descriptions.</span></span> <span data-ttu-id="4ad50-187">È quindi possibile chiamare [**UnloadPerfCounterTextStrings**](/windows/win32/api/loadperf/nf-loadperf-unloadperfcountertextstringsw) durante la disinstallazione.</span><span class="sxs-lookup"><span data-stu-id="4ad50-187">You can then call [**UnloadPerfCounterTextStrings**](/windows/win32/api/loadperf/nf-loadperf-unloadperfcountertextstringsw) during uninstall.</span></span>

<span data-ttu-id="4ad50-188">L'utilità **lodctr** copia le stringhe da. File INI nei **contatori** e valori del registro di sistema nelle sottochiavi **di lingua** appropriate.</span><span class="sxs-lookup"><span data-stu-id="4ad50-188">The **lodctr** utility copies the strings from the .INI file to the **Counters** and **Help** registry values under the appropriate language subkeys.</span></span> <span data-ttu-id="4ad50-189">Se la sottochiave della lingua corrispondente non esiste, le stringhe per tale lingua non vengono copiate.</span><span class="sxs-lookup"><span data-stu-id="4ad50-189">If the corresponding language subkey does not exist, the strings for that language are not copied.</span></span> <span data-ttu-id="4ad50-190">L'utilità aggiorna anche l' **ultimo contatore** e l'ultimo valore della **Guida** .</span><span class="sxs-lookup"><span data-stu-id="4ad50-190">The utility also updates the **Last Counter** and **Last Help** value.</span></span> <span data-ttu-id="4ad50-191">I nomi e le descrizioni dei contatori delle prestazioni vengono archiviati nel seguente percorso del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="4ad50-191">The performance counter names and descriptions are stored in the following location in the registry.</span></span>

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

<span data-ttu-id="4ad50-192">Oltre ad aggiungere valori nella chiave **Perflib** , lo strumento **lodctr** aggiunge anche i valori seguenti al nodo **Servizi** per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="4ad50-192">In addition to adding values under the **PerfLib** key, the **lodctr** tool also adds the following values to the **Services** node for the application.</span></span> <span data-ttu-id="4ad50-193">Nella maggior parte dei casi, l'applicazione e il provider avranno una relazione uno-a-uno. Tuttavia, è possibile che un provider fornisca dati del contatore per più applicazioni, motivo per cui la chiave è basata sull'applicazione e non sul provider.</span><span class="sxs-lookup"><span data-stu-id="4ad50-193">In most cases, the application and provider will have a one-to-one relationship; however, it is possible for a provider to provide counter data for multiple applications, which is why the key is based on the application and not the provider.</span></span>

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
