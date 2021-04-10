---
title: Carico IAgent
description: Carico IAgent
ms.assetid: 8f25e6b6-a117-4b37-969a-d8f80c7be224
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4e30a25abb631714384f8349a9d260deade0d6d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103963061"
---
# <a name="iagentload"></a><span data-ttu-id="674b3-103">IAgent:: Load</span><span class="sxs-lookup"><span data-stu-id="674b3-103">IAgent::Load</span></span>

<span data-ttu-id="674b3-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="674b3-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Load(
   VARIANT vLoadKey,  // data provider
   long * pdwCharID,  // address of a variable for character ID
   long * pdwReqID    // address of a variable for request ID
);
```

<span data-ttu-id="674b3-105">Carica un carattere nella raccolta di [**caratteri**](./iagent.md) .</span><span class="sxs-lookup"><span data-stu-id="674b3-105">Loads a character into the [**Characters**](./iagent.md) collection.</span></span>

-   <span data-ttu-id="674b3-106">Restituisce \_ OK per indicare che l'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="674b3-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="674b3-107"><span id="vLoadKey"></span><span id="vloadkey"></span><span id="VLOADKEY"></span>*vLoadKey*</span><span class="sxs-lookup"><span data-stu-id="674b3-107"><span id="vLoadKey"></span><span id="vloadkey"></span><span id="VLOADKEY"></span>*vLoadKey*</span></span>
</dt> <dd>

<span data-ttu-id="674b3-108">Tipo di dati Variant che deve essere uno dei seguenti:</span><span class="sxs-lookup"><span data-stu-id="674b3-108">A variant datatype that must be one of the following:</span></span>



|            |                                                                       |
|------------|-----------------------------------------------------------------------|
| <span data-ttu-id="674b3-109">*filespec*</span><span class="sxs-lookup"><span data-stu-id="674b3-109">*filespec*</span></span> | <span data-ttu-id="674b3-110">Percorso del file locale del file di definizione del carattere specificato.</span><span class="sxs-lookup"><span data-stu-id="674b3-110">The local file location of the specified character's definition file.</span></span> |
| <span data-ttu-id="674b3-111">*URL*</span><span class="sxs-lookup"><span data-stu-id="674b3-111">*URL*</span></span>      | <span data-ttu-id="674b3-112">Indirizzo HTTP per il file di definizione del carattere.</span><span class="sxs-lookup"><span data-stu-id="674b3-112">The HTTP address for the character's definition file.</span></span>                 |



 

</dd> <dt>

<span data-ttu-id="674b3-113"><span id="pdwCharID"></span><span id="pdwcharid"></span><span id="PDWCHARID"></span>*pdwCharID*</span><span class="sxs-lookup"><span data-stu-id="674b3-113"><span id="pdwCharID"></span><span id="pdwcharid"></span><span id="PDWCHARID"></span>*pdwCharID*</span></span>
</dt> <dd>

<span data-ttu-id="674b3-114">Indirizzo di una variabile che riceve l'ID del carattere.</span><span class="sxs-lookup"><span data-stu-id="674b3-114">Address of a variable that receives the character's ID.</span></span>

</dd> <dt>

<span data-ttu-id="674b3-115"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span><span class="sxs-lookup"><span data-stu-id="674b3-115"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span></span>
</dt> <dd>

<span data-ttu-id="674b3-116">Indirizzo di una variabile che riceve l'ID della richiesta di [**caricamento**](load-method.md) .</span><span class="sxs-lookup"><span data-stu-id="674b3-116">Address of a variable that receives the [**Load**](load-method.md) request ID.</span></span>

</dd> </dl>

<span data-ttu-id="674b3-117">È possibile caricare i caratteri dalla sottodirectory Microsoft Agent specificando un percorso relativo, ovvero uno che non include i due punti o un carattere di barra iniziali.</span><span class="sxs-lookup"><span data-stu-id="674b3-117">You can load characters from the Microsoft Agent subdirectory by specifying a relative path (one that does not include a colon or leading slash character).</span></span> <span data-ttu-id="674b3-118">Questa operazione previene il prefisso del percorso con la directory characters di Agent, che si trova nella directory% Windows% msagent localizzata \\ .</span><span class="sxs-lookup"><span data-stu-id="674b3-118">This prefixes the path with Agent's characters directory (located in the localized %windows%\\msagent directory).</span></span> <span data-ttu-id="674b3-119">È anche possibile usare un indirizzo relativo per specificare la propria directory nella directory chars dell'agente.</span><span class="sxs-lookup"><span data-stu-id="674b3-119">You can also use a relative address to specify your own directory in Agent's Chars directory.</span></span>

<span data-ttu-id="674b3-120">Non è possibile caricare più volte lo stesso carattere, ovvero un carattere con lo stesso GUID, da una singola connessione.</span><span class="sxs-lookup"><span data-stu-id="674b3-120">You cannot load the same character (a character having the same GUID) more than once from a single connection.</span></span> <span data-ttu-id="674b3-121">Analogamente, non è possibile caricare contemporaneamente il carattere predefinito e altri caratteri da una singola connessione, perché il carattere predefinito potrebbe essere uguale a quello dell'altro carattere.</span><span class="sxs-lookup"><span data-stu-id="674b3-121">Similarly, you cannot load the default character and other characters at the same time from a single connection, because the default character could be the same as the other character.</span></span> <span data-ttu-id="674b3-122">Tuttavia, è possibile creare un'altra connessione (usando CoCreateInstance) e caricare lo stesso carattere.</span><span class="sxs-lookup"><span data-stu-id="674b3-122">However, you can create another connection (using CoCreateInstance) and load the same character.</span></span>

<span data-ttu-id="674b3-123">Il provider di dati Microsoft Agent supporta il caricamento di dati di tipo carattere archiviati come singolo file strutturato (. ACS) con dati di tipo carattere e dati di animazione insieme o come dati di tipo carattere separati (. ACF) e animazione (. File ACA).</span><span class="sxs-lookup"><span data-stu-id="674b3-123">Microsoft Agent's data provider supports loading character data stored as a single structured file (.ACS) with character data and animation data together, or as separate character data (.ACF) and animation (.ACA) files.</span></span> <span data-ttu-id="674b3-124">In genere, usare il singolo strutturato. File ACS per caricare un carattere archiviato in un'unità disco o in una rete locale e a cui si accede utilizzando il protocollo file convenzionale, ad esempio i percorsi UNC.</span><span class="sxs-lookup"><span data-stu-id="674b3-124">Generally, use the single structured .ACS file to load a character that is stored on a local disk drive or network and accessed using conventional file protocol (such as UNC pathnames).</span></span> <span data-ttu-id="674b3-125">Usare l'oggetto separato. ACF e. File ACA quando si desidera caricare i file di animazione singolarmente da un sito remoto a cui si accede utilizzando il protocollo HTTP.</span><span class="sxs-lookup"><span data-stu-id="674b3-125">Use the separate .ACF and .ACA files when you want to load the animation files individually from a remote site where they are accessed using HTTP protocol.</span></span>

<span data-ttu-id="674b3-126">Per. I file ACS, usando il metodo [**Load**](load-method.md) , consentono di accedere alle animazioni di un carattere; una volta caricato, è possibile usare il metodo [**Play**](play-method.md) per animare il carattere.</span><span class="sxs-lookup"><span data-stu-id="674b3-126">For .ACS files, using the [**Load**](load-method.md) method provides access a character's animations; once loaded, you can use the [**Play**](play-method.md) method to animate the character.</span></span> <span data-ttu-id="674b3-127">Per. File ACF, viene usato anche il metodo [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) per caricare i dati dell'animazione.</span><span class="sxs-lookup"><span data-stu-id="674b3-127">For .ACF files, you also use the [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) method to load animation data.</span></span> <span data-ttu-id="674b3-128">Il metodo **Load** non supporta il download. File ACS da un sito HTTP.</span><span class="sxs-lookup"><span data-stu-id="674b3-128">The **Load** method does not support downloading .ACS files from an HTTP site.</span></span>

<span data-ttu-id="674b3-129">Il caricamento di un carattere non visualizza automaticamente il carattere.</span><span class="sxs-lookup"><span data-stu-id="674b3-129">Loading a character does not automatically display the character.</span></span> <span data-ttu-id="674b3-130">Usare prima il metodo [**show**](show-method.md) per rendere visibile il carattere.</span><span class="sxs-lookup"><span data-stu-id="674b3-130">Use the [**Show**](show-method.md) method first to make the character visible.</span></span>

 

 