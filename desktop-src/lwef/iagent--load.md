---
title: Caricamento IAgent
description: Caricamento IAgent
ms.assetid: 8f25e6b6-a117-4b37-969a-d8f80c7be224
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80ce2835d60f3edce6f45d181927437ba6e58b18
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120934"
---
# <a name="iagentload"></a><span data-ttu-id="9ddd1-103">IAgent::Load</span><span class="sxs-lookup"><span data-stu-id="9ddd1-103">IAgent::Load</span></span>

<span data-ttu-id="9ddd1-104">\[Microsoft Agent è deprecato a livello di Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="9ddd1-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Load(
   VARIANT vLoadKey,  // data provider
   long * pdwCharID,  // address of a variable for character ID
   long * pdwReqID    // address of a variable for request ID
);
```

<span data-ttu-id="9ddd1-105">Carica un carattere nella [**raccolta Characters.**](./iagent.md)</span><span class="sxs-lookup"><span data-stu-id="9ddd1-105">Loads a character into the [**Characters**](./iagent.md) collection.</span></span>

-   <span data-ttu-id="9ddd1-106">Restituisce S \_ OK per indicare che l'operazione è riuscita.</span><span class="sxs-lookup"><span data-stu-id="9ddd1-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="9ddd1-107"><span id="vLoadKey"></span><span id="vloadkey"></span><span id="VLOADKEY"></span>*vLoadKey*</span><span class="sxs-lookup"><span data-stu-id="9ddd1-107"><span id="vLoadKey"></span><span id="vloadkey"></span><span id="VLOADKEY"></span>*vLoadKey*</span></span>
</dt> <dd>

<span data-ttu-id="9ddd1-108">Tipo di dati variant che deve essere uno dei seguenti:</span><span class="sxs-lookup"><span data-stu-id="9ddd1-108">A variant datatype that must be one of the following:</span></span>



| <span data-ttu-id="9ddd1-109">Valore</span><span class="sxs-lookup"><span data-stu-id="9ddd1-109">Value</span></span>           | <span data-ttu-id="9ddd1-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9ddd1-110">Description</span></span>                                                                      |
|------------|-----------------------------------------------------------------------|
| <span data-ttu-id="9ddd1-111">*filespec*</span><span class="sxs-lookup"><span data-stu-id="9ddd1-111">*filespec*</span></span> | <span data-ttu-id="9ddd1-112">Percorso locale del file di definizione del carattere specificato.</span><span class="sxs-lookup"><span data-stu-id="9ddd1-112">The local file location of the specified character's definition file.</span></span> |
| <span data-ttu-id="9ddd1-113">*URL*</span><span class="sxs-lookup"><span data-stu-id="9ddd1-113">*URL*</span></span>      | <span data-ttu-id="9ddd1-114">Indirizzo HTTP per il file di definizione del carattere.</span><span class="sxs-lookup"><span data-stu-id="9ddd1-114">The HTTP address for the character's definition file.</span></span>                 |



 

</dd> <dt>

<span data-ttu-id="9ddd1-115"><span id="pdwCharID"></span><span id="pdwcharid"></span><span id="PDWCHARID"></span>*pdwCharID*</span><span class="sxs-lookup"><span data-stu-id="9ddd1-115"><span id="pdwCharID"></span><span id="pdwcharid"></span><span id="PDWCHARID"></span>*pdwCharID*</span></span>
</dt> <dd>

<span data-ttu-id="9ddd1-116">Indirizzo di una variabile che riceve l'ID del carattere.</span><span class="sxs-lookup"><span data-stu-id="9ddd1-116">Address of a variable that receives the character's ID.</span></span>

</dd> <dt>

<span data-ttu-id="9ddd1-117"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span><span class="sxs-lookup"><span data-stu-id="9ddd1-117"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span></span>
</dt> <dd>

<span data-ttu-id="9ddd1-118">Indirizzo di una variabile che riceve l'ID [**richiesta**](load-method.md) di caricamento.</span><span class="sxs-lookup"><span data-stu-id="9ddd1-118">Address of a variable that receives the [**Load**](load-method.md) request ID.</span></span>

</dd> </dl>

<span data-ttu-id="9ddd1-119">È possibile caricare caratteri dalla sottodirectory di Microsoft Agent specificando un percorso relativo(uno che non include due punti o una barra iniziale).</span><span class="sxs-lookup"><span data-stu-id="9ddd1-119">You can load characters from the Microsoft Agent subdirectory by specifying a relative path (one that does not include a colon or leading slash character).</span></span> <span data-ttu-id="9ddd1-120">Questo antefissi il percorso con la directory dei caratteri di Agent (che si trova nella directory localizzata %windows% \\ msagent).</span><span class="sxs-lookup"><span data-stu-id="9ddd1-120">This prefixes the path with Agent's characters directory (located in the localized %windows%\\msagent directory).</span></span> <span data-ttu-id="9ddd1-121">È anche possibile usare un indirizzo relativo per specificare la propria directory nella directory Chars di Agent.</span><span class="sxs-lookup"><span data-stu-id="9ddd1-121">You can also use a relative address to specify your own directory in Agent's Chars directory.</span></span>

<span data-ttu-id="9ddd1-122">Non è possibile caricare più volte lo stesso carattere (un carattere con lo stesso GUID) da una singola connessione.</span><span class="sxs-lookup"><span data-stu-id="9ddd1-122">You cannot load the same character (a character having the same GUID) more than once from a single connection.</span></span> <span data-ttu-id="9ddd1-123">Analogamente, non è possibile caricare il carattere predefinito e altri caratteri contemporaneamente da una singola connessione, perché il carattere predefinito potrebbe essere lo stesso dell'altro carattere.</span><span class="sxs-lookup"><span data-stu-id="9ddd1-123">Similarly, you cannot load the default character and other characters at the same time from a single connection, because the default character could be the same as the other character.</span></span> <span data-ttu-id="9ddd1-124">Tuttavia, è possibile creare un'altra connessione (usando CoCreateInstance) e caricare lo stesso carattere.</span><span class="sxs-lookup"><span data-stu-id="9ddd1-124">However, you can create another connection (using CoCreateInstance) and load the same character.</span></span>

<span data-ttu-id="9ddd1-125">Il provider di dati di Microsoft Agent supporta il caricamento di dati di tipo carattere archiviati come singolo file strutturato (. ACS) con dati di tipo carattere e dati di animazione insieme o come dati di tipo carattere separati (. ACF) e animazione (. ACA).</span><span class="sxs-lookup"><span data-stu-id="9ddd1-125">Microsoft Agent's data provider supports loading character data stored as a single structured file (.ACS) with character data and animation data together, or as separate character data (.ACF) and animation (.ACA) files.</span></span> <span data-ttu-id="9ddd1-126">In genere, usare il singolo strutturato . File ACS per caricare un carattere archiviato in un'unità disco locale o in una rete e accessibile tramite il protocollo di file convenzionale ,ad esempio i nomi di percorso UNC.</span><span class="sxs-lookup"><span data-stu-id="9ddd1-126">Generally, use the single structured .ACS file to load a character that is stored on a local disk drive or network and accessed using conventional file protocol (such as UNC pathnames).</span></span> <span data-ttu-id="9ddd1-127">Usare l'oggetto separato . ACF e . File ACA quando si desidera caricare i file di animazione singolarmente da un sito remoto a cui si accede tramite il protocollo HTTP.</span><span class="sxs-lookup"><span data-stu-id="9ddd1-127">Use the separate .ACF and .ACA files when you want to load the animation files individually from a remote site where they are accessed using HTTP protocol.</span></span>

<span data-ttu-id="9ddd1-128">Per. I file ACS, usando [**il metodo Load,**](load-method.md) forniscono l'accesso alle animazioni di un carattere. Dopo il caricamento, è possibile usare il [**metodo Play**](play-method.md) per animare il carattere.</span><span class="sxs-lookup"><span data-stu-id="9ddd1-128">For .ACS files, using the [**Load**](load-method.md) method provides access a character's animations; once loaded, you can use the [**Play**](play-method.md) method to animate the character.</span></span> <span data-ttu-id="9ddd1-129">Per. File ACF, si usa anche il [**metodo Prepare per**](/windows/desktop/lwef/iagentcharacter--prepare) caricare i dati dell'animazione.</span><span class="sxs-lookup"><span data-stu-id="9ddd1-129">For .ACF files, you also use the [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) method to load animation data.</span></span> <span data-ttu-id="9ddd1-130">Il **metodo Load** non supporta il download di . File ACS da un sito HTTP.</span><span class="sxs-lookup"><span data-stu-id="9ddd1-130">The **Load** method does not support downloading .ACS files from an HTTP site.</span></span>

<span data-ttu-id="9ddd1-131">Il caricamento di un carattere non visualizza automaticamente il carattere.</span><span class="sxs-lookup"><span data-stu-id="9ddd1-131">Loading a character does not automatically display the character.</span></span> <span data-ttu-id="9ddd1-132">Usare prima [**il metodo Show**](show-method.md) per rendere visibile il carattere.</span><span class="sxs-lookup"><span data-stu-id="9ddd1-132">Use the [**Show**](show-method.md) method first to make the character visible.</span></span>

 

 