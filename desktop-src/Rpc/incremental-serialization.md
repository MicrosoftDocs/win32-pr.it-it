---
title: Serializzazione incrementale
description: Quando si usa la serializzazione dello stile incrementale, si forniscono tre routine per modificare il buffer.
ms.assetid: c7383b4d-94d1-4edd-ac29-c11fb5343156
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 409f8da0881719ec9273f4dd12cc99e3d36c35a3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104516018"
---
# <a name="incremental-serialization"></a><span data-ttu-id="53c03-103">Serializzazione incrementale</span><span class="sxs-lookup"><span data-stu-id="53c03-103">Incremental Serialization</span></span>

<span data-ttu-id="53c03-104">Quando si usa la serializzazione dello stile incrementale, si forniscono tre routine per modificare il buffer.</span><span class="sxs-lookup"><span data-stu-id="53c03-104">When using the incremental style serialization, you supply three routines to manipulate the buffer.</span></span> <span data-ttu-id="53c03-105">Queste routine sono: Alloc, Read e Write.</span><span class="sxs-lookup"><span data-stu-id="53c03-105">These routines are: Alloc, Read, and Write.</span></span> <span data-ttu-id="53c03-106">La routine Alloc alloca un buffer della dimensione richiesta.</span><span class="sxs-lookup"><span data-stu-id="53c03-106">The Alloc routine allocates a buffer of the required size.</span></span> <span data-ttu-id="53c03-107">La routine Write scrive i dati nel buffer e la routine Read recupera un buffer che contiene i dati di cui è stato effettuato il marshalling.</span><span class="sxs-lookup"><span data-stu-id="53c03-107">The Write routine writes the data into the buffer, and the Read routine retrieves a buffer that contains marshaled data.</span></span> <span data-ttu-id="53c03-108">Una singola chiamata di serializzazione può effettuare diverse chiamate a queste routine.</span><span class="sxs-lookup"><span data-stu-id="53c03-108">A single serialization call can make several calls to these routines.</span></span>

<span data-ttu-id="53c03-109">Lo stile di serializzazione incrementale usa le routine seguenti:</span><span class="sxs-lookup"><span data-stu-id="53c03-109">The incremental style of serialization uses the following routines:</span></span>

-   [<span data-ttu-id="53c03-110">**MesEncodeIncrementalHandleCreate**</span><span class="sxs-lookup"><span data-stu-id="53c03-110">**MesEncodeIncrementalHandleCreate**</span></span>](/windows/desktop/api/Midles/nf-midles-mesencodeincrementalhandlecreate)
-   [<span data-ttu-id="53c03-111">**MesDecodeIncrementalHandleCreate**</span><span class="sxs-lookup"><span data-stu-id="53c03-111">**MesDecodeIncrementalHandleCreate**</span></span>](/windows/desktop/api/Midles/nf-midles-mesdecodeincrementalhandlecreate)
-   [<span data-ttu-id="53c03-112">**MesIncrementalHandleReset**</span><span class="sxs-lookup"><span data-stu-id="53c03-112">**MesIncrementalHandleReset**</span></span>](/windows/desktop/api/Midles/nf-midles-mesincrementalhandlereset)
-   [<span data-ttu-id="53c03-113">**MesHandleFree**</span><span class="sxs-lookup"><span data-stu-id="53c03-113">**MesHandleFree**</span></span>](/windows/desktop/api/Midles/nf-midles-meshandlefree)

<span data-ttu-id="53c03-114">I prototipi per le funzioni Alloc, Read e Write che è necessario fornire sono illustrati di seguito:</span><span class="sxs-lookup"><span data-stu-id="53c03-114">The prototypes for the Alloc, Read, and Write functions that you must provide are shown below:</span></span>

``` syntax
void __RPC_USER Alloc (
   void *State,          /* application-defined pointer */
   char **pBuffer,       /* returns pointer to allocated buffer */
   unsigned int *pSize); /* inputs requested bytes; outputs 
                         /* pBuffer size */

void __RPC_USER Write (
   void *State,          /* application-defined pointer */
   char *Buffer,         /* buffer with serialized data */
   unsigned int Size);   /* number of bytes to write from Buffer */

void __RPC_USER Read (
   void *State,          /* application-defined pointer */
   char **pBuffer,       /* returned pointer to buffer with data */
   unsigned int *pSize); /* number of bytes to read into pBuffer */
```

<span data-ttu-id="53c03-115">L'input di stato un parametro per tutte e tre le funzioni è il puntatore definito dall'applicazione associato all'handle dei servizi di codifica.</span><span class="sxs-lookup"><span data-stu-id="53c03-115">The State input a parameter for all three functions is the application-defined pointer that was associated with the encoding services handle.</span></span> <span data-ttu-id="53c03-116">L'applicazione può utilizzare questo puntatore per accedere alla struttura contenente informazioni specifiche dell'applicazione, ad esempio un handle di file o un puntatore di flusso.</span><span class="sxs-lookup"><span data-stu-id="53c03-116">The application can use this pointer to access the structure containing application-specific information, such as a file handle or stream pointer.</span></span> <span data-ttu-id="53c03-117">Si noti che gli stub non modificano il puntatore di stato diverso da per passarlo alle funzioni Alloc, Read e Write.</span><span class="sxs-lookup"><span data-stu-id="53c03-117">Note that the stubs do not modify the State pointer other than to pass it to the Alloc, Read, and Write functions.</span></span> <span data-ttu-id="53c03-118">Durante la codifica, viene chiamato Alloc per ottenere un buffer in cui vengono serializzati i dati.</span><span class="sxs-lookup"><span data-stu-id="53c03-118">During encoding, Alloc is called to obtain a buffer into which the data is serialized.</span></span> <span data-ttu-id="53c03-119">Viene quindi chiamata la scrittura per consentire all'applicazione di controllare quando e dove vengono archiviati i dati serializzati.</span><span class="sxs-lookup"><span data-stu-id="53c03-119">Then, Write is called to enable the application to control when and where the serialized data is stored.</span></span> <span data-ttu-id="53c03-120">Durante la decodifica, viene chiamato Read per restituire il numero richiesto di byte di dati serializzati dalla posizione in cui l'applicazione lo ha archiviato.</span><span class="sxs-lookup"><span data-stu-id="53c03-120">During decoding, Read is called to return the requested number of bytes of serialized data from where the application stored it.</span></span>

<span data-ttu-id="53c03-121">Una funzionalità importante dello stile incrementale è che l'handle mantiene automaticamente il puntatore di stato.</span><span class="sxs-lookup"><span data-stu-id="53c03-121">An important feature of the incremental style is that the handle keeps the state pointer for you.</span></span> <span data-ttu-id="53c03-122">Questo puntatore mantiene lo stato e non viene mai toccato dalle funzioni RPC, tranne quando il puntatore viene passato a una funzione di allocazione, scrittura o lettura.</span><span class="sxs-lookup"><span data-stu-id="53c03-122">This pointer maintains the state and is never touched by the RPC functions, except when passing the pointer to Alloc, Write, or Read function.</span></span> <span data-ttu-id="53c03-123">L'handle gestisce anche uno stato interno che consente di codificare e decodificare diverse istanze di tipo nello stesso buffer aggiungendo spaziatura interna in base alle esigenze per l'allineamento.</span><span class="sxs-lookup"><span data-stu-id="53c03-123">The handle also maintains an internal state that makes it possible to encode and decode several type instances to the same buffer by adding padding as needed for alignment.</span></span> <span data-ttu-id="53c03-124">La funzione [**MesIncrementalHandleReset**](/windows/desktop/api/Midles/nf-midles-mesincrementalhandlereset) Reimposta un handle sullo stato iniziale per consentire la lettura o la scrittura dall'inizio del buffer.</span><span class="sxs-lookup"><span data-stu-id="53c03-124">The [**MesIncrementalHandleReset**](/windows/desktop/api/Midles/nf-midles-mesincrementalhandlereset) function resets a handle to its initial state to enable reading or writing from the beginning of the buffer.</span></span>

<span data-ttu-id="53c03-125">Le funzioni Alloc e Write, insieme a un puntatore definito dall'applicazione, sono associate a un handle di servizi di codifica tramite una chiamata alla funzione [**MesEncodeIncrementalHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesencodeincrementalhandlecreate) .</span><span class="sxs-lookup"><span data-stu-id="53c03-125">The Alloc and Write functions, along with an application-defined pointer, are associated with an encoding-services handle by a call to the [**MesEncodeIncrementalHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesencodeincrementalhandlecreate) function.</span></span> <span data-ttu-id="53c03-126">**MesEncodeIncrementalHandleCreate** alloca la memoria necessaria per l'handle, quindi la Inizializza.</span><span class="sxs-lookup"><span data-stu-id="53c03-126">**MesEncodeIncrementalHandleCreate** allocates the memory needed for the handle and then initializes it.</span></span>

<span data-ttu-id="53c03-127">L'applicazione può chiamare [**MesDecodeIncrementalHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesdecodeincrementalhandlecreate) per creare un handle di decodifica, [**MesIncrementalHandleReset**](/windows/desktop/api/Midles/nf-midles-mesincrementalhandlereset) per reinizializzare l'handle o [**MesHandleFree**](/windows/desktop/api/Midles/nf-midles-meshandlefree) per liberare la memoria dell'handle.</span><span class="sxs-lookup"><span data-stu-id="53c03-127">The application can call [**MesDecodeIncrementalHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesdecodeincrementalhandlecreate) to create a decoding handle, [**MesIncrementalHandleReset**](/windows/desktop/api/Midles/nf-midles-mesincrementalhandlereset) to reinitialize the handle, or [**MesHandleFree**](/windows/desktop/api/Midles/nf-midles-meshandlefree) to free the handle's memory.</span></span> <span data-ttu-id="53c03-128">La funzione Read, insieme a un parametro definito dall'applicazione, è associata a un handle di decodifica mediante una chiamata alla routine **MesDecodeIncrementalHandleCreate** .</span><span class="sxs-lookup"><span data-stu-id="53c03-128">The Read function, along with an application-defined parameter, is associated with a decoding handle by a call to the **MesDecodeIncrementalHandleCreate** routine.</span></span> <span data-ttu-id="53c03-129">La funzione crea l'handle e lo inizializza.</span><span class="sxs-lookup"><span data-stu-id="53c03-129">The function creates the handle and initializes it.</span></span>

<span data-ttu-id="53c03-130">I parametri UserState, Alloc, Write e Read di [**MesIncrementalHandleReset**](/windows/desktop/api/Midles/nf-midles-mesincrementalhandlereset) possono essere **null** per indicare che non sono state apportate modifiche.</span><span class="sxs-lookup"><span data-stu-id="53c03-130">The UserState, Alloc, Write, and Read parameters of [**MesIncrementalHandleReset**](/windows/desktop/api/Midles/nf-midles-mesincrementalhandlereset) can be **NULL** to indicate no change.</span></span>

 

 




