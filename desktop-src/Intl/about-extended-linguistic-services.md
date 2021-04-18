---
description: Extended Linguistic Services (ELS) viene implementato come una libreria a collegamento dinamico (DLL) che fornisce un'ampia gamma di funzionalità di supporto linguistico per il testo specificato dall'applicazione.
ms.assetid: 23d4e42a-a5bb-467c-a8b9-6a57ae39daa0
title: Informazioni sui servizi linguistici estesi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a6594fcfe67954a56cb09e239221b2b529d4d01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314312"
---
# <a name="about-extended-linguistic-services"></a><span data-ttu-id="ee2ad-103">Informazioni sui servizi linguistici estesi</span><span class="sxs-lookup"><span data-stu-id="ee2ad-103">About Extended Linguistic Services</span></span>

<span data-ttu-id="ee2ad-104">Extended Linguistic Services (ELS) viene implementato come una libreria a collegamento dinamico (DLL) che fornisce un'ampia gamma di funzionalità di supporto linguistico per il testo specificato dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="ee2ad-104">Extended Linguistic Services (ELS) is implemented as a dynamic-link library (DLL) that provides a variety of linguistic support functionality for text that the application specifies.</span></span> <span data-ttu-id="ee2ad-105">La tecnologia include i plug-in e la piattaforma ELS per diversi tipi di servizi linguistici predefiniti accessibili all'applicazione tramite la piattaforma.</span><span class="sxs-lookup"><span data-stu-id="ee2ad-105">The technology includes the ELS platform and plug-ins for several predefined linguistic service types accessible to the application through the platform.</span></span>

> [!Note]  
> <span data-ttu-id="ee2ad-106">Il modulo ELS viene installato automaticamente con Windows 7 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="ee2ad-106">The ELS module is installed automatically with Windows 7 and later.</span></span>

 

## <a name="els-platform"></a><span data-ttu-id="ee2ad-107">Piattaforma ELS</span><span class="sxs-lookup"><span data-stu-id="ee2ad-107">ELS Platform</span></span>

<span data-ttu-id="ee2ad-108">La piattaforma ELS è l'interfaccia tra l'applicazione e i servizi ELS.</span><span class="sxs-lookup"><span data-stu-id="ee2ad-108">The ELS platform is the interface between your application and the ELS services.</span></span> <span data-ttu-id="ee2ad-109">Offre un modo semplice per implementare diversi tipi di funzionalità linguistiche tramite la stessa API, che consente all'applicazione di accedere a servizi specifici e di utilizzarli.</span><span class="sxs-lookup"><span data-stu-id="ee2ad-109">It provides a simple way to implement several kinds of linguistic functionality through the same API, which allows the application to access and use specific services.</span></span> <span data-ttu-id="ee2ad-110">Per altre informazioni sull'API, vedere informazioni di [riferimento su servizi linguistici estesi.](extended-linguistic-services-reference.md)</span><span class="sxs-lookup"><span data-stu-id="ee2ad-110">For more information about the API, see [Extended Linguistic Services Reference.](extended-linguistic-services-reference.md)</span></span>

> [!Note]  
> <span data-ttu-id="ee2ad-111">Quando l'applicazione chiama una delle funzioni dell'API ELS, la piattaforma alloca memoria e risorse in base alle esigenze per la comunicazione con i servizi.</span><span class="sxs-lookup"><span data-stu-id="ee2ad-111">When the application calls any of the ELS API functions, the platform allocates memory and resources as needed for communication with the services.</span></span> <span data-ttu-id="ee2ad-112">L'applicazione è responsabile della richiamata della piattaforma per liberare queste risorse.</span><span class="sxs-lookup"><span data-stu-id="ee2ad-112">The application is responsible for calling the platform again to free these resources.</span></span>

 

<span data-ttu-id="ee2ad-113">La piattaforma viene eseguita all'interno dello spazio di memoria virtuale dell'applicazione e tutta la memoria allocata fa parte di questo spazio.</span><span class="sxs-lookup"><span data-stu-id="ee2ad-113">The platform runs inside the application virtual memory space, and all allocated memory is part of this space.</span></span> <span data-ttu-id="ee2ad-114">Pertanto, l'applicazione deve solo collegarsi alla DLL del componente ELS (Elscore.dll) collegandosi a Elscore. lib o caricando in modo dinamico Elscore.dll.</span><span class="sxs-lookup"><span data-stu-id="ee2ad-114">Thus your application only needs to link to the ELS component DLL (Elscore.dll) by linking to Elscore.lib or by dynamically loading Elscore.dll.</span></span>

## <a name="els-services"></a><span data-ttu-id="ee2ad-115">Servizi ELS</span><span class="sxs-lookup"><span data-stu-id="ee2ad-115">ELS Services</span></span>

<span data-ttu-id="ee2ad-116">Per Windows 7 e versioni successive, la piattaforma ELS supporta solo i servizi predefiniti seguenti.</span><span class="sxs-lookup"><span data-stu-id="ee2ad-116">For Windows 7 and later, the ELS platform supports only the following predefined services.</span></span>

-   [<span data-ttu-id="ee2ad-117">Rilevamento lingua Microsoft</span><span class="sxs-lookup"><span data-stu-id="ee2ad-117">Microsoft Language Detection</span></span>](microsoft-language-detection.md)
-   [<span data-ttu-id="ee2ad-118">Rilevamento script Microsoft</span><span class="sxs-lookup"><span data-stu-id="ee2ad-118">Microsoft Script Detection</span></span>](microsoft-script-detection.md)
-   [<span data-ttu-id="ee2ad-119">Servizi di traslitterazione</span><span class="sxs-lookup"><span data-stu-id="ee2ad-119">Transliteration services</span></span>](transliteration-services.md)

> [!Note]  
> <span data-ttu-id="ee2ad-120">Le versioni future di ELS supporteranno i servizi aggiuntivi forniti da Microsoft o dai provider di servizi.</span><span class="sxs-lookup"><span data-stu-id="ee2ad-120">Future versions of ELS will support additional services provided by Microsoft or service providers.</span></span>

 

<span data-ttu-id="ee2ad-121">Ogni servizio è associato a una categoria di servizi che descrive le operazioni del servizio.</span><span class="sxs-lookup"><span data-stu-id="ee2ad-121">Each service is associated with a service category describing what the service does.</span></span> <span data-ttu-id="ee2ad-122">La categoria è rappresentata da una stringa non localizzabile.</span><span class="sxs-lookup"><span data-stu-id="ee2ad-122">The category is represented by a nonlocalizable string.</span></span> <span data-ttu-id="ee2ad-123">Viene utilizzato dalle applicazioni per enumerare i servizi disponibili.</span><span class="sxs-lookup"><span data-stu-id="ee2ad-123">It is used by applications to enumerate available services.</span></span> <span data-ttu-id="ee2ad-124">Le categorie di servizi correnti sono:</span><span class="sxs-lookup"><span data-stu-id="ee2ad-124">The current service categories are:</span></span>

-   <span data-ttu-id="ee2ad-125">"Rilevamento lingua"</span><span class="sxs-lookup"><span data-stu-id="ee2ad-125">"Language Detection"</span></span>
-   <span data-ttu-id="ee2ad-126">"Rilevamento script"</span><span class="sxs-lookup"><span data-stu-id="ee2ad-126">"Script Detection"</span></span>
-   <span data-ttu-id="ee2ad-127">Translitterazione</span><span class="sxs-lookup"><span data-stu-id="ee2ad-127">"Transliteration"</span></span>

<span data-ttu-id="ee2ad-128">La piattaforma usa i metadati del servizio per enumerare i servizi richiesti dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="ee2ad-128">The platform uses service metadata to enumerate the services requested by the application.</span></span> <span data-ttu-id="ee2ad-129">Proprietà quali l'identificatore univoco globale (GUID) del servizio, i linguaggi e gli script di input e output supportati e la categoria del servizio possono essere usati dall'applicazione per enumerare i servizi ELS desiderati.</span><span class="sxs-lookup"><span data-stu-id="ee2ad-129">Properties such as the service globally unique identifier (GUID), supported input and output languages and scripts, and the service category can be used by the application to enumerate the desired ELS services.</span></span>

<span data-ttu-id="ee2ad-130">Ogni servizio ELS viene implementato come plug-in supportato da una DLL che può essere installata nel sistema operativo in modo che la piattaforma ELS possa rilevare e usarla.</span><span class="sxs-lookup"><span data-stu-id="ee2ad-130">Each ELS service is implemented as a plug-in supported by a DLL that can be installed on the operating system so that the ELS platform can detect and use it.</span></span> <span data-ttu-id="ee2ad-131">I servizi possono esporre i propri sottoservizi, se necessario.</span><span class="sxs-lookup"><span data-stu-id="ee2ad-131">Services can expose their own subservices, if required.</span></span>

## <a name="main-els-operations"></a><span data-ttu-id="ee2ad-132">Operazioni ELS principali</span><span class="sxs-lookup"><span data-stu-id="ee2ad-132">Main ELS Operations</span></span>

<span data-ttu-id="ee2ad-133">Questa sezione descrive le operazioni principali supportate dalla piattaforma ELS.</span><span class="sxs-lookup"><span data-stu-id="ee2ad-133">This section describes the main operations supported by the ELS platform.</span></span> <span data-ttu-id="ee2ad-134">La piattaforma supporta le modalità di chiamata sincrona e asincrona.</span><span class="sxs-lookup"><span data-stu-id="ee2ad-134">The platform supports both synchronous and asynchronous calling modes.</span></span> <span data-ttu-id="ee2ad-135">La modalità di chiamata asincrona utilizza un pool di thread dell'applicazione per pianificare i thread per l'elaborazione delle richieste.</span><span class="sxs-lookup"><span data-stu-id="ee2ad-135">The asynchronous calling mode uses an application thread pool to schedule threads for processing requests.</span></span>

> [!Note]  
> <span data-ttu-id="ee2ad-136">Poiché la piattaforma supporta una modalità asincrona, i servizi ELS non devono implementare questo tipo di funzionalità autonomamente.</span><span class="sxs-lookup"><span data-stu-id="ee2ad-136">Since the platform supports an asynchronous mode, ELS services do not have to implement this type of functionality on their own.</span></span>

 

### <a name="service-enumeration"></a><span data-ttu-id="ee2ad-137">Enumerazione del servizio</span><span class="sxs-lookup"><span data-stu-id="ee2ad-137">Service Enumeration</span></span>

<span data-ttu-id="ee2ad-138">La piattaforma ELS carica e gestisce tutti i servizi ELS, rendendo trasparente l'operazione per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="ee2ad-138">The ELS platform loads and manages all ELS services, making operation transparent to the application.</span></span> <span data-ttu-id="ee2ad-139">L'applicazione enumera i servizi disponibili chiamando [**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices).</span><span class="sxs-lookup"><span data-stu-id="ee2ad-139">The application enumerates the available services by calling [**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices).</span></span> <span data-ttu-id="ee2ad-140">Per istruzioni sulla programmazione, vedere [enumerazione e liberazione dei servizi](enumerating-and-freeing-services.md).</span><span class="sxs-lookup"><span data-stu-id="ee2ad-140">For programming instructions, see [Enumerating and Freeing Services](enumerating-and-freeing-services.md).</span></span>

> [!Note]  
> <span data-ttu-id="ee2ad-141">Per motivi di prestazioni, è consigliabile che l'applicazione enumera i servizi disponibili una sola volta.</span><span class="sxs-lookup"><span data-stu-id="ee2ad-141">It is advisable for performance reasons to have your application enumerate the available services only once.</span></span> <span data-ttu-id="ee2ad-142">La piattaforma ELS verifica nuovamente i servizi nell'enumerazione successiva per assicurarsi che i risultati dell'enumerazione siano sempre aggiornati.</span><span class="sxs-lookup"><span data-stu-id="ee2ad-142">The ELS platform checks the services again on the next enumeration to ensure that its enumeration results are always current.</span></span>

 

### <a name="text-recognition"></a><span data-ttu-id="ee2ad-143">Riconoscimento del testo</span><span class="sxs-lookup"><span data-stu-id="ee2ad-143">Text Recognition</span></span>

<span data-ttu-id="ee2ad-144">Dopo l'enumerazione del servizio, l'applicazione chiama la funzione [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) per usare un particolare servizio ELS per eseguire il mapping di qualsiasi intervallo di testo di testo di input al testo di output.</span><span class="sxs-lookup"><span data-stu-id="ee2ad-144">After service enumeration, the application calls the [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) function to use a particular ELS service to map any text range of input text to output text.</span></span> <span data-ttu-id="ee2ad-145">Un esempio di riconoscimento del testo è l'uso di un servizio di rilevamento della lingua che riceve un segmento di testo e rileva il linguaggio più probabile.</span><span class="sxs-lookup"><span data-stu-id="ee2ad-145">An example of text recognition is the use of a language detection service that receives a text segment and detects its most probable language.</span></span>

<span data-ttu-id="ee2ad-146">Dopo che il servizio ha riconosciuto il testo, [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) restituisce con una struttura del [**\_ \_ contenitore delle proprietà di mapping**](/windows/desktop/api/Elscore/ns-elscore-mapping_property_bag) popolata con le proprietà e i dati di output generati dal servizio.</span><span class="sxs-lookup"><span data-stu-id="ee2ad-146">After the service has recognized the text, [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) returns with a [**MAPPING\_PROPERTY\_BAG**](/windows/desktop/api/Elscore/ns-elscore-mapping_property_bag) structure populated with output data and properties produced by the service.</span></span> <span data-ttu-id="ee2ad-147">Per evitare perdite di memoria, l'applicazione deve liberare il contenitore delle proprietà chiamando [**MappingFreePropertyBag**](/windows/desktop/api/Elscore/nf-elscore-mappingfreepropertybag) per ogni volta che [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) restituisce \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ee2ad-147">To avoid memory leaks, the application must free the property bag by calling [**MappingFreePropertyBag**](/windows/desktop/api/Elscore/nf-elscore-mappingfreepropertybag) for each time that the [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) returns S\_OK.</span></span> <span data-ttu-id="ee2ad-148">In genere l'applicazione esegue questa operazione quando viene completata utilizzando i dati di output o quando i dati di output non sono più rilevanti perché l'area di input del testo è stata modificata, ad esempio, modificata o eliminata.</span><span class="sxs-lookup"><span data-stu-id="ee2ad-148">Usually the application does this either when it finishes using the output data or when the output data is no longer relevant because the input region of text has been modified, for example, edited or deleted.</span></span> <span data-ttu-id="ee2ad-149">Quando viene rilasciato il contenitore delle proprietà, **MappingFreePropertyBag** restituisce.</span><span class="sxs-lookup"><span data-stu-id="ee2ad-149">When the property bag is released, **MappingFreePropertyBag** returns.</span></span>

<span data-ttu-id="ee2ad-150">Per la [richiesta di riconoscimento](requesting-text-recognition.md)del testo sono disponibili istruzioni di programmazione per il riconoscimento del testo.</span><span class="sxs-lookup"><span data-stu-id="ee2ad-150">Programming instructions for text recognition are provided in [Requesting Text Recognition](requesting-text-recognition.md).</span></span>

### <a name="service-termination"></a><span data-ttu-id="ee2ad-151">Terminazione del servizio</span><span class="sxs-lookup"><span data-stu-id="ee2ad-151">Service Termination</span></span>

<span data-ttu-id="ee2ad-152">Quando l'applicazione non richiede più servizi ELS, chiama [**MappingFreeServices**](/windows/desktop/api/Elscore/nf-elscore-mappingfreeservices) prima di terminare.</span><span class="sxs-lookup"><span data-stu-id="ee2ad-152">When your application no longer requires ELS services, it calls [**MappingFreeServices**](/windows/desktop/api/Elscore/nf-elscore-mappingfreeservices) before it terminates.</span></span> <span data-ttu-id="ee2ad-153">Per altre informazioni, vedere [enumerazione e liberazione dei servizi](enumerating-and-freeing-services.md).</span><span class="sxs-lookup"><span data-stu-id="ee2ad-153">For more information, see [Enumerating and Freeing Services](enumerating-and-freeing-services.md).</span></span>

### <a name="versioning"></a><span data-ttu-id="ee2ad-154">Controllo delle versioni</span><span class="sxs-lookup"><span data-stu-id="ee2ad-154">Versioning</span></span>

<span data-ttu-id="ee2ad-155">Le versioni future di ELS consentiranno l'aggiornamento dei servizi ELS.</span><span class="sxs-lookup"><span data-stu-id="ee2ad-155">Future versions of ELS will allow the ELS services to be updated.</span></span> <span data-ttu-id="ee2ad-156">L'applicazione sarà in grado di controllare i numeri di versione della struttura di [**\_ \_ informazioni sul servizio di mapping**](/windows/desktop/api/Elscore/ns-elscore-mapping_service_info) per rilevare eventuali modifiche nei servizi.</span><span class="sxs-lookup"><span data-stu-id="ee2ad-156">The application will be able to check the version numbers of the [**MAPPING\_SERVICE\_INFO**](/windows/desktop/api/Elscore/ns-elscore-mapping_service_info) structure to detect any changes in the services.</span></span>

> [!Note]  
> <span data-ttu-id="ee2ad-157">L'applicazione ELS non deve supporre che diverse versioni dello stesso servizio possano recuperare esattamente gli stessi risultati.</span><span class="sxs-lookup"><span data-stu-id="ee2ad-157">Your ELS application should not make the assumption that different versions of the same service can retrieve exactly the same results.</span></span>

 

 

 



