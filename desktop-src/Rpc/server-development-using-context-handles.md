---
title: Sviluppo di server con handle di contesto
description: Dal punto di vista dello sviluppo di un programma server, un handle di contesto è un puntatore non tipizzato. I programmi server inizializzano gli handle di contesto puntando i dati in memoria o in un'altra forma di archiviazione (ad esempio file su dischi).
ms.assetid: 6a1aabca-4cb9-401c-90c7-0cff7a69b7b6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f743a4a6aa4a2aa7b6987bb54dc56e55cffbc76
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045158"
---
# <a name="server-development-using-context-handles"></a><span data-ttu-id="08254-104">Sviluppo di server con handle di contesto</span><span class="sxs-lookup"><span data-stu-id="08254-104">Server Development Using Context Handles</span></span>

<span data-ttu-id="08254-105">Dal punto di vista dello sviluppo di un programma server, un handle di contesto è un puntatore non tipizzato.</span><span class="sxs-lookup"><span data-stu-id="08254-105">From the perspective of server program development, a context handle is an untyped pointer.</span></span> <span data-ttu-id="08254-106">I programmi server inizializzano gli handle di contesto puntando i dati in memoria o in un'altra forma di archiviazione (ad esempio file su dischi).</span><span class="sxs-lookup"><span data-stu-id="08254-106">Server programs initialize context handles by pointing them at data in memory or on some other form of storage (such as files on disks).</span></span>

<span data-ttu-id="08254-107">Si supponga, ad esempio, che un client utilizzi un handle di contesto per richiedere una serie di aggiornamenti a un record in un database.</span><span class="sxs-lookup"><span data-stu-id="08254-107">For instance, suppose that a client uses a context handle to request a series of updates to a record in a database.</span></span> <span data-ttu-id="08254-108">Il client chiama una procedura remota sul server e la passa a una chiave di ricerca.</span><span class="sxs-lookup"><span data-stu-id="08254-108">The client calls a remote procedure on the server and passes it a search key.</span></span> <span data-ttu-id="08254-109">Il programma server cerca la chiave di ricerca nel database e ottiene il numero di record integer del record corrispondente.</span><span class="sxs-lookup"><span data-stu-id="08254-109">The server program searches the database for the search key and obtains the integer record number of the matching record.</span></span> <span data-ttu-id="08254-110">Il server può quindi puntare un puntatore a void in una posizione di memoria contenente il numero di record.</span><span class="sxs-lookup"><span data-stu-id="08254-110">The server can then point a pointer to void at a memory location containing the record number.</span></span> <span data-ttu-id="08254-111">Quando viene restituito, la procedura remota deve restituire il puntatore come handle di contesto tramite il relativo valore restituito o l'elenco di parametri.</span><span class="sxs-lookup"><span data-stu-id="08254-111">When it returns, the remote procedure would need to return the pointer as a context handle through its return value or its parameter list.</span></span> <span data-ttu-id="08254-112">Il client deve passare il puntatore al server ogni volta che ha chiamato le procedure remote per aggiornare il record.</span><span class="sxs-lookup"><span data-stu-id="08254-112">The client would need to pass the pointer to the server each time it called remote procedures to update the record.</span></span> <span data-ttu-id="08254-113">Durante ogni operazione di aggiornamento, il server eseguirà il cast del puntatore void come puntatore a un Integer.</span><span class="sxs-lookup"><span data-stu-id="08254-113">During each of these update operations, the server would cast the void pointer to be a pointer to an integer.</span></span>

<span data-ttu-id="08254-114">Dopo che il programma server ha puntato all'handle di contesto nei dati di contesto, l'handle viene considerato aperto.</span><span class="sxs-lookup"><span data-stu-id="08254-114">After the server program points the context handle at context data, the handle is considered opened.</span></span> <span data-ttu-id="08254-115">Gli handle contenenti un valore **null** sono chiusi.</span><span class="sxs-lookup"><span data-stu-id="08254-115">Handles containing a **NULL** value are closed.</span></span> <span data-ttu-id="08254-116">Il server gestisce un handle di contesto aperto finché il client non chiama una procedura remota che la chiude.</span><span class="sxs-lookup"><span data-stu-id="08254-116">The server maintains an opened context handle until the client calls a remote procedure that closes it.</span></span> <span data-ttu-id="08254-117">Se la sessione client termina quando l'handle è aperto, il tempo di esecuzione RPC chiama la routine di esecuzione del server per liberare l'handle.</span><span class="sxs-lookup"><span data-stu-id="08254-117">If the client session terminates while the handle is open, the RPC run time calls the server run-down routine to free the handle.</span></span>

<span data-ttu-id="08254-118">Nel frammento di codice seguente viene illustrato come un server può implementare un handle di contesto.</span><span class="sxs-lookup"><span data-stu-id="08254-118">The following code fragment demonstrates how a server might implement a context handle.</span></span> <span data-ttu-id="08254-119">In questo esempio, il server gestisce un file di dati che il client scrive in utilizzando le procedure remote.</span><span class="sxs-lookup"><span data-stu-id="08254-119">In this example, the server maintains a data file that the client writes to using remote procedures.</span></span> <span data-ttu-id="08254-120">Le informazioni sul contesto sono un handle di file che tiene traccia della posizione corrente nel file in cui i dati vengono scritti dal server.</span><span class="sxs-lookup"><span data-stu-id="08254-120">The context information is a file handle that keeps track of the current location in the file where the server will write data.</span></span> <span data-ttu-id="08254-121">L'handle di file è incluso nel pacchetto come handle di contesto nell'elenco di parametri per le chiamate di procedure remote.</span><span class="sxs-lookup"><span data-stu-id="08254-121">The file handle is packaged as a context handle in the parameter list to remote procedure calls.</span></span> <span data-ttu-id="08254-122">Una struttura contiene il nome file e l'handle di file.</span><span class="sxs-lookup"><span data-stu-id="08254-122">A structure contains the file name and the file handle.</span></span> <span data-ttu-id="08254-123">La definizione dell'interfaccia per questo esempio viene illustrata nello [sviluppo di interfacce con handle di contesto](interface-development-using-context-handles.md).</span><span class="sxs-lookup"><span data-stu-id="08254-123">The interface definition for this example is shown in [Interface Development Using Context Handles](interface-development-using-context-handles.md).</span></span>


```C++
/* cxhndlp.c (fragment of file containing remote procedures) */
typedef struct 
{
     FILE* hFile;
     char   achFile[256];
} FILE_CONTEXT_TYPE;
```



<span data-ttu-id="08254-124">La funzione RemoteOpen apre un file nel server:</span><span class="sxs-lookup"><span data-stu-id="08254-124">The function RemoteOpen opens a file on the server:</span></span>


```C++
short RemoteOpen(
    PPCONTEXT_HANDLE_TYPE pphContext,
    unsigned char *pszFileName)
{
    FILE               *hFile;
    FILE_CONTEXT_TYPE  *pFileContext;
 
    if ((hFile = fopen(pszFileName, "r")) == NULL) 
    {
        *pphContext = (PCONTEXT_HANDLE_TYPE) NULL;
        return(-1);
    }
    else 
    {
        pFileContext = (FILE_CONTEXT_TYPE *) 
                       MIDL_user_allocate(sizeof(FILE_CONTEXT_TYPE));
        pFileContext->hFile = hFile;
        // check if pszFileName is longer than 256 and if yes, return
        // an error
        strcpy_s(pFileContext->achFile, srlen(pszFileName), pszFileName);
        *pphContext = (PCONTEXT_HANDLE_TYPE) pFileContext;
        return(0);
    }
}
```



<span data-ttu-id="08254-125">La funzione RemoteRead legge un file nel server.</span><span class="sxs-lookup"><span data-stu-id="08254-125">The function RemoteRead reads a file on the server.</span></span>


```C++
short RemoteRead(
    PCONTEXT_HANDLE_TYPE phContext, 
    unsigned char *pbBuf, 
    short *pcbBuf) 
{ 
    FILE_CONTEXT_TYPE *pFileContext; 
    printf("in RemoteRead\n"); 
    pFileContext = (FILE_CONTEXT_TYPE *) phContext; 
    *pcbBuf = (short) fread(pbBuf, sizeof(char), 
                            BUFSIZE, 
                            pFileContext->hFile); 
    return(*pcbBuf); 
}
```



<span data-ttu-id="08254-126">La funzione RemoteClose chiude un file nel server.</span><span class="sxs-lookup"><span data-stu-id="08254-126">The function RemoteClose closes a file on the server.</span></span> <span data-ttu-id="08254-127">Si noti che l'applicazione server deve assegnare **null** all'handle di contesto come parte della funzione close.</span><span class="sxs-lookup"><span data-stu-id="08254-127">Note that the server application has to assign **NULL** to the context handle as part of the close function.</span></span> <span data-ttu-id="08254-128">In questo modo si comunica allo stub del server e alla libreria di runtime RPC che l'handle di contesto è stato eliminato.</span><span class="sxs-lookup"><span data-stu-id="08254-128">This communicates to the server stub and the RPC run-time library that the context handle has been deleted.</span></span> <span data-ttu-id="08254-129">In caso contrario, la connessione verrà mantenuta aperta e infine si verificherà un errore di esecuzione del contesto.</span><span class="sxs-lookup"><span data-stu-id="08254-129">Otherwise, the connection will be kept open and eventually a context run-down will occur.</span></span>


```C++
void RemoteClose(PPCONTEXT_HANDLE_TYPE pphContext)
{
    FILE_CONTEXT_TYPE *pFileContext;
 
    if (*pphContext == NULL)
    {
        //Log error, client tried to close a NULL handle.
        return;
    }
    pFileContext = (FILE_CONTEXT_TYPE *)*pphContext;
    printf("File %s closed.\n", pFileContext->achFile);
    fclose(pFileConext->hFile);
    MIDL_user_free(pFileContext);
 
    // This tells the run-time, when it is marshalling the out 
    // parameters, that the context handle has been closed normally.
    *pphContext = NULL;
}
```



> [!Note]  
> <span data-ttu-id="08254-130">Sebbene sia previsto che il client passi un handle di contesto valido a una chiamata con \[ in, \] attributi direzionali out, RPC non rifiuta gli handle di contesto **null** per questa combinazione di attributi direzionali.</span><span class="sxs-lookup"><span data-stu-id="08254-130">While it is expected the client passes a valid context handle to a call with \[in, out\] directional attributes, RPC does not reject **NULL** context handles for this combination of directional attributes.</span></span> <span data-ttu-id="08254-131">L'handle del contesto **null** viene passato al server come puntatore **null** .</span><span class="sxs-lookup"><span data-stu-id="08254-131">The **NULL** context handle is passed to the server as a **NULL** pointer.</span></span> <span data-ttu-id="08254-132">È necessario scrivere il codice server per le chiamate contenenti un \[ \] handle del contesto out per evitare una violazione di accesso quando viene ricevuto un puntatore **null** .</span><span class="sxs-lookup"><span data-stu-id="08254-132">The server code for calls containing an \[in, out\] context handle should be written to avoid an access violation when a **NULL** pointer is received.</span></span>

 

 

 




