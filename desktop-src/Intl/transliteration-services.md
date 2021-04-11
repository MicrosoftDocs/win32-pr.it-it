---
description: ELS Transliteration Services mappa il testo UTF-16 da un sistema di scrittura a un altro sistema di scrittura.
ms.assetid: 32e46c52-5c3c-4e22-8f4e-05286ee213ba
title: Servizi di traslitterazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc00b96d56e6b05e70b352c81da0280e9ef35043
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131735"
---
# <a name="transliteration-services"></a><span data-ttu-id="6026e-103">Servizi di traslitterazione</span><span class="sxs-lookup"><span data-stu-id="6026e-103">Transliteration Services</span></span>

<span data-ttu-id="6026e-104">ELS Transliteration Services mappa il testo UTF-16 da un sistema di scrittura a un altro sistema di scrittura.</span><span class="sxs-lookup"><span data-stu-id="6026e-104">The ELS transliteration services map UTF-16 text from one writing system to another writing system.</span></span> <span data-ttu-id="6026e-105">Ogni servizio è effettivamente un dato che si applica a un set specifico di script Unicode di input e output e la traslitterazione effettiva è interna alla piattaforma ELS.</span><span class="sxs-lookup"><span data-stu-id="6026e-105">Each service is really data applying to a specific set of input and output Unicode scripts, and the actual transliteration is internal to the ELS platform.</span></span> <span data-ttu-id="6026e-106">L'applicazione può facoltativamente enumerare i servizi disponibili per script di input e output specifici e selezionare il servizio richiesto.</span><span class="sxs-lookup"><span data-stu-id="6026e-106">The application can optionally enumerate the available services for specific input and output scripts and select the service that it requires.</span></span>

<span data-ttu-id="6026e-107">La piattaforma gestisce i metadati per i servizi di traslitterazione ELS.</span><span class="sxs-lookup"><span data-stu-id="6026e-107">The platform maintains metadata for the ELS transliteration services.</span></span> <span data-ttu-id="6026e-108">I metadati per ogni servizio forniscono una descrizione del servizio ed elencano gli script di input e di output supportati dal servizio.</span><span class="sxs-lookup"><span data-stu-id="6026e-108">Metadata for each service provides a description of the service and lists the input and output scripts that the service supports.</span></span> <span data-ttu-id="6026e-109">I metadati sono rappresentati da una struttura di [**\_ \_ informazioni sul servizio di mapping**](/windows/desktop/api/Elscore/ns-elscore-mapping_service_info) recuperata dalla funzione [**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices) .</span><span class="sxs-lookup"><span data-stu-id="6026e-109">The metadata is represented by a [**MAPPING\_SERVICE\_INFO**](/windows/desktop/api/Elscore/ns-elscore-mapping_service_info) structure retrieved by the [**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices) function.</span></span>

## <a name="input-to-a-transliteration-service"></a><span data-ttu-id="6026e-110">Input per un servizio di traslitterazione</span><span class="sxs-lookup"><span data-stu-id="6026e-110">Input to a Transliteration Service</span></span>

<span data-ttu-id="6026e-111">L'input per un servizio di traslitterazione è un testo UTF-16 in un sistema di scrittura.</span><span class="sxs-lookup"><span data-stu-id="6026e-111">The input to a transliteration service is UTF-16 text in one writing system.</span></span>

## <a name="output-of-a-transliteration-service"></a><span data-ttu-id="6026e-112">Output di un servizio di traslitterazione</span><span class="sxs-lookup"><span data-stu-id="6026e-112">Output of a Transliteration Service</span></span>

<span data-ttu-id="6026e-113">L'output di un servizio di traslitterazione è il testo UTF-16 mappato a un secondo sistema di scrittura.</span><span class="sxs-lookup"><span data-stu-id="6026e-113">The output of a transliteration service is UTF-16 text mapped to a second writing system.</span></span> <span data-ttu-id="6026e-114">Se non è disponibile alcun mapping di traslitterazione appropriato per un determinato blocco del testo di input, il blocco rimane invariato.</span><span class="sxs-lookup"><span data-stu-id="6026e-114">If no appropriate transliteration mapping is available for any given chunk of the input text, the chunk remains unchanged.</span></span>

## <a name="transliteration-service-operation"></a><span data-ttu-id="6026e-115">Operazione del servizio di traslitterazione</span><span class="sxs-lookup"><span data-stu-id="6026e-115">Transliteration Service Operation</span></span>

<span data-ttu-id="6026e-116">Un servizio di traslitterazione esegue il mapping del testo Unicode da uno script di input a uno script di output, carattere per carattere o termine per termine, a seconda dei casi.</span><span class="sxs-lookup"><span data-stu-id="6026e-116">A transliteration service maps Unicode text from an input script to an output script, character by character or term by term, as appropriate.</span></span> <span data-ttu-id="6026e-117">L'applicazione può scegliere di ottenere il servizio di traslitterazione specifico di interesse specificando gli script di input e output quando si chiama [**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices)o fornendo il GUID del servizio.</span><span class="sxs-lookup"><span data-stu-id="6026e-117">The application can choose to obtain the specific transliteration service of interest by specifying input and output scripts when calling [**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices), or by providing the service GUID.</span></span> <span data-ttu-id="6026e-118">Un'altra opzione per l'applicazione consiste nell'enumerare tutti i servizi di traslitterazione disponibili specificando la categoria di servizio "translittering" quando si chiama **MappingGetServices**.</span><span class="sxs-lookup"><span data-stu-id="6026e-118">Another option for the application is to enumerate all available transliteration services by specifying the service category "Transliteration" when calling **MappingGetServices**.</span></span> <span data-ttu-id="6026e-119">In questo caso, l'applicazione chiama ogni servizio e confronta i risultati con il testo originale per verificare se i risultati sono stati modificati dall'operazione di un determinato servizio.</span><span class="sxs-lookup"><span data-stu-id="6026e-119">In this case, the application calls each service and compares the results with the original text to see if the results have been changed by the operation of a particular service.</span></span>

<span data-ttu-id="6026e-120">L'applicazione può richiedere il riconoscimento del testo per un servizio di traslitterazione ELS con una chiamata a [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext).</span><span class="sxs-lookup"><span data-stu-id="6026e-120">The application can request text recognition for an ELS transliteration service with a call to [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext).</span></span> <span data-ttu-id="6026e-121">Quando riceve la richiesta, il servizio di traslitterazione alloca un buffer per contenere i dati transliterati, quindi esegue il riconoscimento del testo per ogni punto di codice nella stringa di input fornita dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="6026e-121">When it receives the request, the transliteration service allocates a buffer to contain the transliterated data, and then performs text recognition for each code point in the input string supplied by the application.</span></span>

> [!Note]  
> <span data-ttu-id="6026e-122">Il testo originale e il testo traslitterato potrebbero avere lunghezze diverse.</span><span class="sxs-lookup"><span data-stu-id="6026e-122">The original text and the transliterated text might have different lengths.</span></span>

 

## <a name="transliteration-service-guids"></a><span data-ttu-id="6026e-123">GUID del servizio di traslitterazione</span><span class="sxs-lookup"><span data-stu-id="6026e-123">Transliteration Service GUIDs</span></span>

<span data-ttu-id="6026e-124">I GUID per i servizi di traslitterazione sono dichiarati in Elssrvc. h, come illustrato nel codice seguente.</span><span class="sxs-lookup"><span data-stu-id="6026e-124">The GUIDs for the transliteration services are declared in Elssrvc.h, as shown in the following code.</span></span>


```C++
// {A3A8333B-F4FC-42f6-A0C4-0462FE7317CB}
static const GUID ELS_GUID_TRANSLITERATION_HANT_TO_HANS =
    { 0xA3A8333B, 0xF4FC, 0x42f6, { 0xA0, 0xC4, 0x04, 0x62, 0xFE, 0x73, 0x17, 0xCB } };

// {3CACCDC8-5590-42dc-9A7B-B5A6B5B3B63B}
static const GUID ELS_GUID_TRANSLITERATION_HANS_TO_HANT =
    { 0x3CACCDC8, 0x5590, 0x42dc, { 0x9A, 0x7B, 0xB5, 0xA6, 0xB5, 0xB3, 0xB6, 0x3B } };

// {D8B983B1-F8BF-4a2b-BCD5-5B5EA20613E1}
static const GUID ELS_GUID_TRANSLITERATION_MALAYALAM_TO_LATIN =
    { 0xD8B983B1, 0xF8BF, 0x4a2b, { 0xBC, 0xD5, 0x5B, 0x5E, 0xA2, 0x06, 0x13, 0xE1 } };

// {C4A4DCFE-2661-4d02-9835-F48187109803}
static const GUID ELS_GUID_TRANSLITERATION_DEVANAGARI_TO_LATIN =
    { 0xC4A4DCFE, 0x2661, 0x4d02, { 0x98, 0x35, 0xF4, 0x81, 0x87, 0x10, 0x98, 0x03 } };

// {3DD12A98-5AFD-4903-A13F-E17E6C0BFE01}
static const GUID ELS_GUID_TRANSLITERATION_CYRILLIC_TO_LATIN =
    { 0x3DD12A98, 0x5AFD, 0x4903, { 0xA1, 0x3F, 0xE1, 0x7E, 0x6C, 0x0B, 0xFE, 0x01 } };

// {F4DFD825-91A4-489f-855E-9AD9BEE55727}
static const GUID ELS_GUID_TRANSLITERATION_BENGALI_TO_LATIN =
    { 0xF4DFD825, 0x91A4, 0x489f, { 0x85, 0x5E, 0x9A, 0xD9, 0xBE, 0xE5, 0x57, 0x27 } };
```



## <a name="related-topics"></a><span data-ttu-id="6026e-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6026e-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6026e-126">Informazioni sui servizi linguistici estesi</span><span class="sxs-lookup"><span data-stu-id="6026e-126">About Extended Linguistic Services</span></span>](about-extended-linguistic-services.md)
</dt> </dl>

 

 



