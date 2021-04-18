---
description: Questo argomento descrive i dettagli interni sul modo in cui il resolver di origine crea un'origine multimediale.
ms.assetid: b0113527-f22c-4519-b1cf-fea54bff4090
title: Gestori di schemi e gestori di Byte-Stream
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54976f45c7f07e12b6f095297231d306d0644704
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309010"
---
# <a name="scheme-handlers-and-byte-stream-handlers"></a><span data-ttu-id="c90ca-103">Gestori di schemi e gestori di Byte-Stream</span><span class="sxs-lookup"><span data-stu-id="c90ca-103">Scheme Handlers and Byte-Stream Handlers</span></span>

<span data-ttu-id="c90ca-104">Questo argomento descrive i dettagli interni sul modo in cui il resolver di origine crea un'origine multimediale.</span><span class="sxs-lookup"><span data-stu-id="c90ca-104">This topic describes the internal details of how the source resolver creates a media source.</span></span> <span data-ttu-id="c90ca-105">Leggere questo argomento se si sta implementando un'origine multimediale personalizzata per Media Foundation e si vuole che l'origine del supporto sia disponibile per le applicazioni tramite il resolver di origine.</span><span class="sxs-lookup"><span data-stu-id="c90ca-105">Read this topic if you are implementing a custom media source for Media Foundation, and you want the media source to be available to applications via the source resolver.</span></span>

<span data-ttu-id="c90ca-106">Il resolver di origine può creare un'origine multimediale da un URL o da un flusso di byte (ovvero un puntatore [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) ).</span><span class="sxs-lookup"><span data-stu-id="c90ca-106">The source resolver can create a media source from a URL or from a byte stream (that is, an [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) pointer).</span></span> <span data-ttu-id="c90ca-107">A tale scopo, vengono utilizzati gli oggetti di supporto chiamati *gestori*.</span><span class="sxs-lookup"><span data-stu-id="c90ca-107">To do so, it uses helper objects called *handlers*.</span></span> <span data-ttu-id="c90ca-108">Per gli URL, il resolver di origine usa i *gestori dello schema*.</span><span class="sxs-lookup"><span data-stu-id="c90ca-108">For URLs, the source resolver uses *scheme handlers*.</span></span> <span data-ttu-id="c90ca-109">Per i flussi di byte, USA i *gestori del flusso di byte*.</span><span class="sxs-lookup"><span data-stu-id="c90ca-109">For byte streams, it uses *byte-stream handlers*.</span></span>

<span data-ttu-id="c90ca-110">Un gestore dello schema accetta come input un URL e crea un'origine multimediale o un flusso di byte.</span><span class="sxs-lookup"><span data-stu-id="c90ca-110">A scheme handler takes a URL as input and creates either a media source or a byte stream.</span></span> <span data-ttu-id="c90ca-111">Se viene creato un flusso di byte, il resolver di origine lo passerà a un gestore del flusso di byte, che consente di creare l'origine multimediale.</span><span class="sxs-lookup"><span data-stu-id="c90ca-111">If it creates a byte stream, the source resolver will pass that to a byte-stream handler, which creates the media source.</span></span> <span data-ttu-id="c90ca-112">Questo processo è illustrato nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="c90ca-112">The following image illustrates this process.</span></span>

![diagramma che illustra il processo di risoluzione del codice sorgente](images/f2ade1a8-6f2a-4e40-8cda-2ccf576880c6.gif)

## <a name="scheme-handlers"></a><span data-ttu-id="c90ca-114">Gestori dello schema</span><span class="sxs-lookup"><span data-stu-id="c90ca-114">Scheme Handlers</span></span>

<span data-ttu-id="c90ca-115">I gestori dello schema vengono usati quando l'applicazione chiama [**IMFSourceResolver:: CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) o il relativo equivalente asincrono, [**BeginCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl).</span><span class="sxs-lookup"><span data-stu-id="c90ca-115">Scheme handlers are used when the application calls [**IMFSourceResolver::CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) or its asynchronous equivalent, [**BeginCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl).</span></span>

<span data-ttu-id="c90ca-116">Il resolver di origine cerca i gestori dello schema nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="c90ca-116">The source resolver looks up scheme handlers in the registry.</span></span> <span data-ttu-id="c90ca-117">I gestori dello schema sono elencati in base allo schema URL, con le chiavi seguenti:</span><span class="sxs-lookup"><span data-stu-id="c90ca-117">Scheme handlers are listed by URL scheme, under the following keys:</span></span>

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows Media Foundation
            SchemeHandlers
               <scheme>
                  {00000000-0000-0000-0000-000000000000} = REG_SZ
```

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows Media Foundation
            SchemeHandlers
               <scheme>
                  {00000000-0000-0000-0000-000000000000} = REG_SZ
```

<span data-ttu-id="c90ca-118">dove *<scheme>* è lo schema URL che il gestore è progettato per l'analisi.</span><span class="sxs-lookup"><span data-stu-id="c90ca-118">where *<scheme>* is the URL scheme that the handler is designed to parse.</span></span> <span data-ttu-id="c90ca-119">Lo schema include il carattere ":" finale; ad esempio, "http:".</span><span class="sxs-lookup"><span data-stu-id="c90ca-119">The scheme includes the trailing ':' character; for example, "http:".</span></span>

<span data-ttu-id="c90ca-120">Per registrare un nuovo gestore dello schema, aggiungere una voce il cui nome è il CLSID del gestore dello schema, in formato stringa canonico: `{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}` .</span><span class="sxs-lookup"><span data-stu-id="c90ca-120">To register a new scheme handler, add an entry whose name is the CLSID of the scheme handler, in canonical string form: `{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}`.</span></span> <span data-ttu-id="c90ca-121">Il valore della voce è una stringa (REG \_ SZ) contenente una breve descrizione del gestore, ad esempio "gestore dello schema personale".</span><span class="sxs-lookup"><span data-stu-id="c90ca-121">The value of the entry is a string (REG\_SZ) containing a brief description of the handler, such as "My Scheme Handler."</span></span> <span data-ttu-id="c90ca-122">La parte importante della voce è il CLSID.</span><span class="sxs-lookup"><span data-stu-id="c90ca-122">The important part of the entry is the CLSID.</span></span> <span data-ttu-id="c90ca-123">Il resolver di origine crea il gestore chiamando **CoCreateInstance** con il CLSID.</span><span class="sxs-lookup"><span data-stu-id="c90ca-123">The source resolver creates the handler by calling **CoCreateInstance** with this CLSID.</span></span>

<span data-ttu-id="c90ca-124">I gestori dello schema espongono l'interfaccia [**IMFSchemeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfschemehandler) .</span><span class="sxs-lookup"><span data-stu-id="c90ca-124">Scheme handlers expose the [**IMFSchemeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfschemehandler) interface.</span></span> <span data-ttu-id="c90ca-125">Se il resolver di origine trova un gestore dello schema corrispondente allo schema URL, il resolver di origine chiama [**IMFSchemeHandler:: BeginCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfschemehandler-begincreateobject), passando l'URL originale.</span><span class="sxs-lookup"><span data-stu-id="c90ca-125">If the source resolver finds a scheme handler that matches the URL scheme, the source resolver calls [**IMFSchemeHandler::BeginCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfschemehandler-begincreateobject), passing in the original URL.</span></span> <span data-ttu-id="c90ca-126">Il gestore dello schema apre l'URL e tenta di analizzare il contenuto.</span><span class="sxs-lookup"><span data-stu-id="c90ca-126">The scheme handler will open the URL and attempt to parse the contents.</span></span> <span data-ttu-id="c90ca-127">A questo punto, il gestore dello schema ha due opzioni:</span><span class="sxs-lookup"><span data-stu-id="c90ca-127">At that point, the scheme handler has two options:</span></span>

-   <span data-ttu-id="c90ca-128">Creare un'origine multimediale.</span><span class="sxs-lookup"><span data-stu-id="c90ca-128">Create a media source.</span></span>
-   <span data-ttu-id="c90ca-129">Creare un flusso di byte.</span><span class="sxs-lookup"><span data-stu-id="c90ca-129">Create a byte stream.</span></span>

<span data-ttu-id="c90ca-130">Se crea un'origine multimediale, il resolver di origine restituisce l'origine del supporto all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c90ca-130">If it creates a media source, the source resolver returns the media source to the application.</span></span> <span data-ttu-id="c90ca-131">Se viene creato un flusso di byte, il resolver di origine tenta di trovare un gestore del flusso di byte appropriato, come descritto nella sezione successiva.</span><span class="sxs-lookup"><span data-stu-id="c90ca-131">If it creates a byte stream, the source resolver attempts to find an appropriate byte-stream handler, as described in the next section.</span></span>

## <a name="byte-stream-handlers"></a><span data-ttu-id="c90ca-132">Gestori di Byte-Stream</span><span class="sxs-lookup"><span data-stu-id="c90ca-132">Byte-Stream Handlers</span></span>

<span data-ttu-id="c90ca-133">I gestori del flusso di byte vengono usati quando l'applicazione chiama [**IMFSourceResolver:: CreateObjectFromByteStream**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfrombytestream) o il relativo equivalente asincrono, [**BeginCreateObjectFromByteStream**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfrombytestream).</span><span class="sxs-lookup"><span data-stu-id="c90ca-133">Byte-stream handlers are used when the application calls [**IMFSourceResolver::CreateObjectFromByteStream**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfrombytestream) or its asynchronous equivalent, [**BeginCreateObjectFromByteStream**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfrombytestream).</span></span> <span data-ttu-id="c90ca-134">Vengono inoltre utilizzate quando un gestore dello schema restituisce un flusso di byte, come descritto in precedenza.</span><span class="sxs-lookup"><span data-stu-id="c90ca-134">They are also used when a scheme handler returns a byte stream, as described previously.</span></span>

<span data-ttu-id="c90ca-135">Come per i gestori dello schema, i gestori del flusso di byte sono elencati nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="c90ca-135">As with scheme handlers, byte-stream handlers are listed in the registry.</span></span> <span data-ttu-id="c90ca-136">Sono elencate in base all'estensione del nome di file o al tipo MIME (o entrambi), con le chiavi seguenti:</span><span class="sxs-lookup"><span data-stu-id="c90ca-136">They are listed either by file name extension or MIME type (or both), under the following keys:</span></span>

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows Media Foundation
            ByteStreamHandlers
               <ExtensionOrMimeType>
                  {00000000-0000-0000-0000-000000000000} = REG_SZ
```

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows Media Foundation
            ByteStreamHandlers
               <ExtensionOrMimeType>
                  {00000000-0000-0000-0000-000000000000} = REG_SZ
```

<span data-ttu-id="c90ca-137">dove *<ExtensionOrMimeType>* è l'estensione del nome file o il tipo MIME.</span><span class="sxs-lookup"><span data-stu-id="c90ca-137">where *<ExtensionOrMimeType>* is the file name extension or MIME type.</span></span> <span data-ttu-id="c90ca-138">Le estensioni di file includono il carattere ' .' iniziale; ad esempio, ". wmv".</span><span class="sxs-lookup"><span data-stu-id="c90ca-138">File extensions include the initial '.' character; for example, ".wmv".</span></span>

<span data-ttu-id="c90ca-139">L'estensione del nome file fa parte dell'URL, fornito dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c90ca-139">The file name extension is part of the URL, provided by the application.</span></span> <span data-ttu-id="c90ca-140">Il tipo MIME potrebbe essere disponibile tramite l'attributo del [**\_ tipo di \_ contenuto \_ MF BYTESTREAM**](mf-bytestream-content-type-attribute.md) nel flusso di byte.</span><span class="sxs-lookup"><span data-stu-id="c90ca-140">The MIME type might be available through the [**MF\_BYTESTREAM\_CONTENT\_TYPE**](mf-bytestream-content-type-attribute.md) attribute on the byte stream.</span></span>

<span data-ttu-id="c90ca-141">Per registrare un nuovo gestore del flusso di byte, aggiungere una voce il cui nome è il CLSID del gestore, in formato stringa canonico.</span><span class="sxs-lookup"><span data-stu-id="c90ca-141">To register a new byte-stream handler, add an entry whose name is the CLSID of the handler, in canonical string form.</span></span> <span data-ttu-id="c90ca-142">Il valore della voce è una stringa (REG \_ SZ) contenente una breve descrizione del gestore, ad esempio "gestore Byte-Stream."</span><span class="sxs-lookup"><span data-stu-id="c90ca-142">The value of the entry is a string (REG\_SZ) containing a brief description of the handler, such as "My Byte-Stream Handler."</span></span> <span data-ttu-id="c90ca-143">Il resolver di origine chiama **CoCreateInstance** per creare il gestore dal CLSID.</span><span class="sxs-lookup"><span data-stu-id="c90ca-143">The source resolver calls **CoCreateInstance** to create the handler from the CLSID.</span></span> <span data-ttu-id="c90ca-144">È possibile registrare lo stesso gestore in più di un'estensione o di un tipo MIME.</span><span class="sxs-lookup"><span data-stu-id="c90ca-144">You can register the same handler under more than one extension or MIME type.</span></span>

<span data-ttu-id="c90ca-145">I gestori del flusso di byte espongono l'interfaccia [**IMFByteStreamHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler) .</span><span class="sxs-lookup"><span data-stu-id="c90ca-145">Byte-stream handlers expose the [**IMFByteStreamHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler) interface.</span></span> <span data-ttu-id="c90ca-146">Se il resolver di origine trova un gestore del flusso di byte corrispondente, viene chiamato [**IMFByteStreamHandler:: BeginCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-begincreateobject).</span><span class="sxs-lookup"><span data-stu-id="c90ca-146">If the source resolver finds a matching byte-stream handler, it calls [**IMFByteStreamHandler::BeginCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-begincreateobject).</span></span> <span data-ttu-id="c90ca-147">L'input per questo metodo è un puntatore al flusso di byte, più l'URL originale, se disponibile.</span><span class="sxs-lookup"><span data-stu-id="c90ca-147">The input to this method is a pointer to the byte stream, plus the original URL, if available.</span></span> <span data-ttu-id="c90ca-148">Il gestore del flusso di byte legge dal flusso di byte fino a quando non viene analizzato un numero sufficiente di dati per creare l'origine multimediale.</span><span class="sxs-lookup"><span data-stu-id="c90ca-148">The byte-stream handler reads from the byte stream until it parses enough data to create the media source.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c90ca-149">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c90ca-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c90ca-150">Resolver di origine</span><span class="sxs-lookup"><span data-stu-id="c90ca-150">Source Resolver</span></span>](source-resolver.md)
</dt> </dl>

 

 



