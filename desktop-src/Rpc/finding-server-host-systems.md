---
title: Ricerca di sistemi host server
description: Ricerca di sistemi host server utilizzando binding di stringa ed eseguendo una query su un database del servizio nome per il percorso di un programma server.
ms.assetid: 4aadda88-2109-481f-aa4b-b1983d81dec5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2357fcafa35d4f64cfb4f6841c0b56e1e94b7aa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856298"
---
# <a name="finding-server-host-systems"></a><span data-ttu-id="e6497-103">Ricerca di sistemi host server</span><span class="sxs-lookup"><span data-stu-id="e6497-103">Finding Server Host Systems</span></span>

<span data-ttu-id="e6497-104">Un sistema host server è il computer che esegue il programma server dell'applicazione distribuita.</span><span class="sxs-lookup"><span data-stu-id="e6497-104">A server host system is the computer that executes the distributed application's server program.</span></span> <span data-ttu-id="e6497-105">In una rete potrebbero essere presenti uno o più sistemi host server.</span><span class="sxs-lookup"><span data-stu-id="e6497-105">There may be one or many server host systems on a network.</span></span> <span data-ttu-id="e6497-106">Il modo in cui il programma client trova un server a cui connettersi dipende dalle esigenze del programma.</span><span class="sxs-lookup"><span data-stu-id="e6497-106">How your client program finds a server to connect to depends on the needs of your program.</span></span>

<span data-ttu-id="e6497-107">Esistono due metodi per trovare i sistemi host server:</span><span class="sxs-lookup"><span data-stu-id="e6497-107">There are two methods of finding server host systems:</span></span>

-   <span data-ttu-id="e6497-108">Uso delle informazioni archiviate nelle stringhe nel codice sorgente del client, nelle variabili di ambiente o nei file di configurazione specifici dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="e6497-108">Using information stored in strings in the client source code, environment variables, or application-specific configuration files.</span></span> <span data-ttu-id="e6497-109">L'applicazione client può usare i dati nella stringa per comporre un'associazione tra il client e il server.</span><span class="sxs-lookup"><span data-stu-id="e6497-109">Your client application can use the data in the string to compose a binding between the client and the server.</span></span>
-   <span data-ttu-id="e6497-110">Esecuzione di query su un database del servizio nome per il percorso di un programma server.</span><span class="sxs-lookup"><span data-stu-id="e6497-110">Querying a name service database for the location of a server program.</span></span>

<span data-ttu-id="e6497-111">In questa sezione vengono presentate informazioni su entrambe le tecniche negli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="e6497-111">This section presents information on both of these techniques in the following topics:</span></span>

-   [<span data-ttu-id="e6497-112">Uso di associazioni di stringa</span><span class="sxs-lookup"><span data-stu-id="e6497-112">Using String Bindings</span></span>](#using-string-bindings)
-   [<span data-ttu-id="e6497-113">Importazione dai database del servizio dei nomi</span><span class="sxs-lookup"><span data-stu-id="e6497-113">Importing from Name Service Databases</span></span>](#importing-from-name-service-databases)

## <a name="using-string-bindings"></a><span data-ttu-id="e6497-114">Uso di associazioni di stringa</span><span class="sxs-lookup"><span data-stu-id="e6497-114">Using String Bindings</span></span>

<span data-ttu-id="e6497-115">Le applicazioni possono creare binding da informazioni archiviate in stringhe.</span><span class="sxs-lookup"><span data-stu-id="e6497-115">Applications can create bindings from information stored in strings.</span></span> <span data-ttu-id="e6497-116">L'applicazione client compone queste informazioni sotto forma di stringa, quindi chiama la funzione [**errore in RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) .</span><span class="sxs-lookup"><span data-stu-id="e6497-116">Your client application composes this information as a string, then calls the [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) function.</span></span> <span data-ttu-id="e6497-117">Il client deve fornire le informazioni seguenti per identificare il server:</span><span class="sxs-lookup"><span data-stu-id="e6497-117">The client must supply the following information to identify the server:</span></span>

-   <span data-ttu-id="e6497-118">Nome dell'interfaccia, identificatore univoco globale (GUID) dell'oggetto o UUID dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="e6497-118">The interface name, the globally unique identifier (GUID) of the object, or UUID of the object.</span></span> <span data-ttu-id="e6497-119">Per altre informazioni, vedere [generazione di UUID di interfaccia](generating-interface-uuids.md) e [UUID di stringa](string-uuid.md).</span><span class="sxs-lookup"><span data-stu-id="e6497-119">For more information, see [Generating Interface UUIDs](generating-interface-uuids.md) and [String UUID](string-uuid.md).</span></span>
-   <span data-ttu-id="e6497-120">Tipo di trasporto su cui comunicare, ad esempio named pipe o TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="e6497-120">The transport type to communicate over, such as named pipes or TCP/IP.</span></span> <span data-ttu-id="e6497-121">Per informazioni dettagliate, vedere [terminologia di associazione RPC essenziale](essential-rpc-binding-terminology.md) e [selezione di una sequenza di protocolli](selecting-a-protocol-sequence.md).</span><span class="sxs-lookup"><span data-stu-id="e6497-121">For details, see [Essential RPC Binding Terminology](essential-rpc-binding-terminology.md) and [Selecting a Protocol Sequence](selecting-a-protocol-sequence.md).</span></span>
-   <span data-ttu-id="e6497-122">Indirizzo di rete o nome del computer host del server.</span><span class="sxs-lookup"><span data-stu-id="e6497-122">The network address or the name of the server host computer.</span></span>
-   <span data-ttu-id="e6497-123">Endpoint del programma server nel computer host del server.</span><span class="sxs-lookup"><span data-stu-id="e6497-123">The endpoint of the server program on the server host computer.</span></span> <span data-ttu-id="e6497-124">Per altre informazioni, vedere [ricerca di endpoint](finding-endpoints.md)e [specifica di endpoint](specifying-endpoints.md).</span><span class="sxs-lookup"><span data-stu-id="e6497-124">For more information, see [Finding Endpoints](finding-endpoints.md), and [Specifying Endpoints](specifying-endpoints.md).</span></span>

<span data-ttu-id="e6497-125">(L'UUID dell'oggetto e le informazioni sull'endpoint sono facoltativi).</span><span class="sxs-lookup"><span data-stu-id="e6497-125">(The object UUID and the endpoint information are optional.)</span></span>

<span data-ttu-id="e6497-126">Negli esempi seguenti, il parametro *pszNetworkAddress* e altri parametri includono barre rovesciate incorporate.</span><span class="sxs-lookup"><span data-stu-id="e6497-126">In the following examples, the *pszNetworkAddress* parameter and other parameters include embedded backslashes.</span></span> <span data-ttu-id="e6497-127">La barra rovesciata è un carattere di escape nel linguaggio di programmazione C.</span><span class="sxs-lookup"><span data-stu-id="e6497-127">The backslash is an escape character in the C programming language.</span></span> <span data-ttu-id="e6497-128">Sono necessarie due barre rovesciate per rappresentare ogni carattere barra rovesciata singolo valore letterale.</span><span class="sxs-lookup"><span data-stu-id="e6497-128">Two backslashes are needed to represent each single literal backslash character.</span></span> <span data-ttu-id="e6497-129">La struttura di associazione di stringhe deve contenere quattro caratteri di barra rovesciata per rappresentare i due caratteri letterali che precedono il nome del server.</span><span class="sxs-lookup"><span data-stu-id="e6497-129">The string-binding structure must contain four backslash characters to represent the two literal backslash characters that precede the server name.</span></span>

<span data-ttu-id="e6497-130">Nell'esempio seguente viene illustrato che il nome del server deve essere preceduto da otto barre rovesciate, in modo che nella struttura dei dati di associazione di stringa vengano visualizzati quattro caratteri di barra rovesciata letterali dopo che la funzione **sprintf \_ s** elabora la stringa.</span><span class="sxs-lookup"><span data-stu-id="e6497-130">The following example shows that the server name must be preceded by eight backslashes so that four literal backslash characters will appear in the string-binding data structure after the **sprintf\_s** function processes the string.</span></span>


```C++
/* client application */

char * pszUuid = "6B29FC40-CA47-1067-B31D-00DD010662DA";
char * pszProtocol = "ncacn_np";
char * pszNetworkAddress = "\\\\\\\\servername";
char * pszEndpoint = "\\\\pipe\\\\pipename";
char * pszString;
 
int len = 0;
 
len  = sprintf_s(pszString, strlen(pszUuid), "%s", pszUuid);
len += sprintf_s(pszString + len, strlen(pszProtocolSequence) + 2, "@%s:",
    pszProtocolSequence);
if (pszNetworkAddress != NULL)
    len += sprintf_s(pszString + len, strlen(pszNetworkAddress), "%s",
    pszNetworkAddress);
len += sprintf_s(pszString + len, strlen(pszEndpoint) + 2, "[%s]", pszEndpoint);
```



<span data-ttu-id="e6497-131">Nell'esempio seguente, l'associazione di stringa viene visualizzata come:</span><span class="sxs-lookup"><span data-stu-id="e6497-131">In the following example, the string binding appears as:</span></span>

<span data-ttu-id="e6497-132">6B29FC40-CA47-1067-B31D-00DD010662DA@ncacn\_NP: \\ \\ \\ \\ *ServerName* \[ \\ \\ pipe \\ \\ *pipeName*\]</span><span class="sxs-lookup"><span data-stu-id="e6497-132">6B29FC40-CA47-1067-B31D-00DD010662DA@ncacn\_np:\\\\\\\\*servername*\[\\\\pipe\\\\*pipename*\]</span></span>

<span data-ttu-id="e6497-133">Il client chiama quindi [**errore in RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) per ottenere l'handle di associazione:</span><span class="sxs-lookup"><span data-stu-id="e6497-133">The client then calls [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) to obtain the binding handle:</span></span>


```C++
RPC_BINDING_HANDLE hBinding;
 
status = RpcBindingFromStringBinding(pszString, &hBinding);
//...
```



<span data-ttu-id="e6497-134">Una funzione comoda, [**errore in RpcStringBindingCompose**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingcompose) assembla l'UUID dell'oggetto, la sequenza di protocollo, l'indirizzo di rete e l'endpoint nella sintassi corretta per la chiamata a [**errore in RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding).</span><span class="sxs-lookup"><span data-stu-id="e6497-134">A convenience function, [**RpcStringBindingCompose**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingcompose) assembles the object UUID, protocol sequence, network address, and endpoint in the correct syntax for the call to [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding).</span></span> <span data-ttu-id="e6497-135">Non è necessario preoccuparsi di inserire la e commerciale, i due punti e i vari componenti per ogni sequenza di protocollo nel posto giusto; è sufficiente specificare le stringhe come parametri della funzione.</span><span class="sxs-lookup"><span data-stu-id="e6497-135">You do not have to worry about putting the ampersand, colon, and the various components for each protocol sequence in the right place; you just supply the strings as parameters to the function.</span></span> <span data-ttu-id="e6497-136">La libreria di runtime alloca anche la memoria necessaria per l'associazione di stringa.</span><span class="sxs-lookup"><span data-stu-id="e6497-136">The run-time library even allocates the memory needed for the string binding.</span></span>


```C++
char * pszNetworkAddress = "\\\\server";
char * pszEndpoint = "\\pipe\\pipename";
status = RpcStringBindingCompose(
            pszUuid,
            pszProtocolSequence,
            pszNetworkAddress,
            pszEndpoint,
            pszOptions,
            &pszString);
//...
status = RpcBindingFromStringBinding(
            pszString,
            &hBinding);
//...
```



<span data-ttu-id="e6497-137">Un'altra funzione di praticità, [**RpcBindingToStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding), accetta un handle di associazione come input e produce l'associazione di stringa corrispondente.</span><span class="sxs-lookup"><span data-stu-id="e6497-137">Another convenience function, [**RpcBindingToStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding), takes a binding handle as input and produces the corresponding string binding.</span></span>

## <a name="importing-from-name-service-databases"></a><span data-ttu-id="e6497-138">Importazione dai database del servizio dei nomi</span><span class="sxs-lookup"><span data-stu-id="e6497-138">Importing from Name Service Databases</span></span>

<span data-ttu-id="e6497-139">Nome archivio dei database del servizio, tra le altre cose, handle di binding e UUID.</span><span class="sxs-lookup"><span data-stu-id="e6497-139">Name service databases store, among other things, binding handles and UUIDs.</span></span> <span data-ttu-id="e6497-140">L'applicazione client può cercare uno dei due o entrambi quando è necessario eseguire l'associazione al server.</span><span class="sxs-lookup"><span data-stu-id="e6497-140">Your client application can search for either or both of these when it needs to bind to the server.</span></span> <span data-ttu-id="e6497-141">Per una descrizione delle informazioni archiviate da un nome e del formato di archiviazione, vedere [il database del servizio nome RPC](the-rpc-name-service-database.md).</span><span class="sxs-lookup"><span data-stu-id="e6497-141">For a discussion of the information that a name service stores, and the storage format, see [The RPC Name Service Database](the-rpc-name-service-database.md).</span></span>

<span data-ttu-id="e6497-142">La libreria RPC fornisce due set di funzioni che il programma client può usare per cercare il nome del database del servizio.</span><span class="sxs-lookup"><span data-stu-id="e6497-142">The RPC library provides two sets of functions that your client program can use to search the name service database.</span></span> <span data-ttu-id="e6497-143">I nomi di un set iniziano con RpcNsBindingImport.</span><span class="sxs-lookup"><span data-stu-id="e6497-143">The names of one set begin with RpcNsBindingImport.</span></span> <span data-ttu-id="e6497-144">I nomi dell'altro set iniziano con RpcNsBindingLookup.</span><span class="sxs-lookup"><span data-stu-id="e6497-144">The names of the other set begin with RpcNsBindingLookup.</span></span> <span data-ttu-id="e6497-145">La differenza tra i due gruppi di funzioni è che le funzioni RpcNsBindingImport restituiscono un singolo handle di binding per chiamata e le funzioni RpcNsBindingLookup restituiscono gruppi di handle per ogni chiamata.</span><span class="sxs-lookup"><span data-stu-id="e6497-145">The difference between the two groups of functions is that the RpcNsBindingImport functions return a single binding handle per call and the RpcNsBindingLookup functions return groups of handles per call.</span></span>

<span data-ttu-id="e6497-146">Per iniziare una ricerca con le funzioni RpcNsBindingImport, chiamare prima [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina), come illustrato nel frammento di codice seguente.</span><span class="sxs-lookup"><span data-stu-id="e6497-146">To begin a search with the RpcNsBindingImport functions, first call [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina), as shown in the following code fragment.</span></span>


```C++
RPC_STATUS status;
RPC_NS_HANDLE hNameServiceHandle;
 
status = RpcNsBindingImportBegin(
    RPC_C_NS_SYNTAX_DEFAULT,
    NULL,
    MyInterface_v1_0_c_ifspec,
    NULL,
    &hNameServiceHandle);
```



<span data-ttu-id="e6497-147">Quando le funzioni RPC eseguono ricerche nel database del servizio dei nomi, è necessario disporre di una posizione per iniziare la ricerca.</span><span class="sxs-lookup"><span data-stu-id="e6497-147">When the RPC functions search the name service database, they need a place to begin the search.</span></span> <span data-ttu-id="e6497-148">Nella terminologia RPC, questo viene chiamato nome della voce.</span><span class="sxs-lookup"><span data-stu-id="e6497-148">In RPC terminology, this is called the entry name.</span></span> <span data-ttu-id="e6497-149">Il programma client passa il nome della voce come secondo parametro a [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina).</span><span class="sxs-lookup"><span data-stu-id="e6497-149">Your client program passes the entry name as the second parameter to [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina).</span></span> <span data-ttu-id="e6497-150">Questo parametro può essere **null** se si desidera eseguire la ricerca nell'intero database del servizio.</span><span class="sxs-lookup"><span data-stu-id="e6497-150">This parameter can be **NULL** if you want to search the entire name service database.</span></span> <span data-ttu-id="e6497-151">In alternativa, è possibile cercare la voce del server passando un nome di voce del server o cercare la voce di gruppo passando un nome di voce di gruppo.</span><span class="sxs-lookup"><span data-stu-id="e6497-151">Alternatively, you can search the server entry by passing a server-entry name or search the group entry by passing a group-entry name.</span></span> <span data-ttu-id="e6497-152">Il passaggio di un nome di voce limita la ricerca al contenuto di tale voce.</span><span class="sxs-lookup"><span data-stu-id="e6497-152">Passing an entry name restricts the search to the contents of that entry.</span></span>

<span data-ttu-id="e6497-153">Nell'esempio precedente, il valore predefinito della \_ sintassi RPC C \_ NS \_ \_ viene passato come primo parametro a [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina).</span><span class="sxs-lookup"><span data-stu-id="e6497-153">In the preceding example, the value RPC\_C\_NS\_SYNTAX\_DEFAULT is passed as the first parameter to [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina).</span></span> <span data-ttu-id="e6497-154">Viene selezionata la sintassi predefinita per il nome della voce.</span><span class="sxs-lookup"><span data-stu-id="e6497-154">This selects the default entry name syntax.</span></span> <span data-ttu-id="e6497-155">Attualmente, questa è l'unica sintassi supportata per i nomi di voce.</span><span class="sxs-lookup"><span data-stu-id="e6497-155">Currently, this is the only supported entry-name syntax.</span></span>

<span data-ttu-id="e6497-156">L'applicazione client può cercare nel database del servizio dei nomi un nome di interfaccia, un UUID o entrambi.</span><span class="sxs-lookup"><span data-stu-id="e6497-156">Your client application can search the name service database for an interface name, a UUID, or both.</span></span> <span data-ttu-id="e6497-157">Se si vuole che venga cercata un'interfaccia in base al nome, passare la variabile di interfaccia globale generata dal compilatore MIDL dal file IDL come terzo parametro a [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina).</span><span class="sxs-lookup"><span data-stu-id="e6497-157">If you want to have it search for an interface by name, pass the global interface variable that the MIDL compiler generates from your IDL file as the third parameter to [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina).</span></span> <span data-ttu-id="e6497-158">La relativa dichiarazione sarà presente nel file di intestazione generato dal compilatore MIDL quando ha generato lo stub del client.</span><span class="sxs-lookup"><span data-stu-id="e6497-158">You'll find its declaration in the header file that the MIDL compiler generated when it generated the client stub.</span></span> <span data-ttu-id="e6497-159">Se si vuole che il programma client cerchi solo per UUID, impostare il terzo parametro su **null**.</span><span class="sxs-lookup"><span data-stu-id="e6497-159">If you want your client program to search by UUID only, set the third parameter to **NULL**.</span></span>

<span data-ttu-id="e6497-160">Quando si esegue la ricerca di un UUID nel database del servizio dei nomi, impostare il quarto parametro di [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina) sull'UUID che si desidera cercare.</span><span class="sxs-lookup"><span data-stu-id="e6497-160">When searching the name service database for a UUID, set the fourth parameter of [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina) to the UUID that you want to search for.</span></span> <span data-ttu-id="e6497-161">Se non si sta cercando un UUID, impostare questo parametro su **null**.</span><span class="sxs-lookup"><span data-stu-id="e6497-161">If you are not searching for a UUID, set this parameter to **NULL**.</span></span>

<span data-ttu-id="e6497-162">La funzione [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina) passa l'indirizzo di un servizio nome-handle del contesto di ricerca tramite il quinto parametro.</span><span class="sxs-lookup"><span data-stu-id="e6497-162">The [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina) function passes the address of a name service–search context handle through its fifth parameter.</span></span> <span data-ttu-id="e6497-163">Passare questo parametro ad altre funzioni di RpcNsBindingImport.</span><span class="sxs-lookup"><span data-stu-id="e6497-163">You pass this parameter to other RpcNsBindingImport functions.</span></span>

<span data-ttu-id="e6497-164">In particolare, la funzione successiva chiamata dall'applicazione client è [**RpcNsBindingImportNext**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportnext).</span><span class="sxs-lookup"><span data-stu-id="e6497-164">In particular, the next function your client application would call is [**RpcNsBindingImportNext**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportnext).</span></span> <span data-ttu-id="e6497-165">I programmi client utilizzano questa funzione per recuperare gli handle di binding compatibili dal database del servizio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="e6497-165">Client programs use this function to retrieve compatible binding handles from the name service database.</span></span> <span data-ttu-id="e6497-166">Il frammento di codice seguente illustra come può essere chiamata questa funzione:</span><span class="sxs-lookup"><span data-stu-id="e6497-166">The following code fragment demonstrates how this function might be called:</span></span>


```C++
RPC_STATUS status;
RPC_BINDING_HANDLE hBindingHandle;
// The variable hNameServiceHandle is a valid name service search 
// context handle obtained from the RpcNsBindingBegin function.
 
status = RpcNsBindingImportNext(hNameServiceHandle, &hBindingHandle);
```



<span data-ttu-id="e6497-167">Una volta chiamata la funzione [**RpcNsBindingImportNext**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportnext) per ottenere un handle di binding, l'applicazione client può determinare se l'handle ricevuto è accettabile.</span><span class="sxs-lookup"><span data-stu-id="e6497-167">Once it has called the [**RpcNsBindingImportNext**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportnext) function to obtain a binding handle, your client application can determine if the handle it received is acceptable.</span></span> <span data-ttu-id="e6497-168">In caso contrario, il programma client può eseguire un ciclo e chiamare di nuovo **RpcNsBindingImportNext** per verificare se il servizio nome contiene un handle più appropriato.</span><span class="sxs-lookup"><span data-stu-id="e6497-168">If not, your client program can execute a loop and call **RpcNsBindingImportNext** again to see if the name service contains a more appropriate handle.</span></span> <span data-ttu-id="e6497-169">Per ogni chiamata a **RpcNsBindingImportNext**, è necessario che sia presente una chiamata corrispondente a RpcNsBindingFree.</span><span class="sxs-lookup"><span data-stu-id="e6497-169">For each call to **RpcNsBindingImportNext**, there must be a corresponding call to RpcNsBindingFree.</span></span> <span data-ttu-id="e6497-170">Al termine della ricerca, chiamare la funzione [**RpcNsBindingImportDone**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportdone) per liberare il contesto di ricerca.</span><span class="sxs-lookup"><span data-stu-id="e6497-170">When your search is complete, call the [**RpcNsBindingImportDone**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportdone) function to free the lookup context.</span></span>

<span data-ttu-id="e6497-171">Quando l'applicazione client dispone di un handle di binding accettabile, deve verificare che l'applicazione server sia in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="e6497-171">After your client application has an acceptable binding handle, it should check to ensure that the server application is running.</span></span> <span data-ttu-id="e6497-172">Il client può usare due metodi per eseguire questa verifica.</span><span class="sxs-lookup"><span data-stu-id="e6497-172">There are two methods your client can use to perform this verification.</span></span> <span data-ttu-id="e6497-173">Il primo consiste nel chiamare una funzione nell'interfaccia client.</span><span class="sxs-lookup"><span data-stu-id="e6497-173">The first is to call a function in the client interface.</span></span> <span data-ttu-id="e6497-174">Se il programma del server è in esecuzione, la chiamata verrà completata.</span><span class="sxs-lookup"><span data-stu-id="e6497-174">If the server program is running, the call will complete.</span></span> <span data-ttu-id="e6497-175">In caso contrario, la chiamata avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="e6497-175">If not, the call will fail.</span></span> <span data-ttu-id="e6497-176">Un modo migliore per verificare che il server sia in esecuzione consiste nel richiamare [**RpcEpResolveBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepresolvebinding), seguito da una chiamata a [**RpcMgmtIsServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtisserverlistening).</span><span class="sxs-lookup"><span data-stu-id="e6497-176">A better way to verify that the server is running is to invoke [**RpcEpResolveBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepresolvebinding), followed by a call to [**RpcMgmtIsServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtisserverlistening).</span></span> <span data-ttu-id="e6497-177">Per ulteriori informazioni sul database del servizio nomi, vedere [il database del servizio nome RPC](the-rpc-name-service-database.md).</span><span class="sxs-lookup"><span data-stu-id="e6497-177">For more information on the name service database, see [The RPC Name Service Database](the-rpc-name-service-database.md).</span></span>

 

 




