---
title: Panoramica sul livello XML
description: L'API XML in WWSAPI è basata sugli oggetti Reader e writer XML, che consentono la lettura o la scrittura di documenti XML in modo diretto. Il livello XML fornisce all'applicazione l'accesso completo e il controllo sul contenuto dei messaggi.
ms.assetid: 938ca257-fbb8-4569-b791-2148abb1a5a5
keywords:
- Panoramica del livello XML servizi Web per Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9b5d062754adea7b48bd42a6a501ce17d0e332b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710708"
---
# <a name="xml-layer-overview"></a><span data-ttu-id="e89b7-107">Panoramica sul livello XML</span><span class="sxs-lookup"><span data-stu-id="e89b7-107">XML Layer Overview</span></span>

<span data-ttu-id="e89b7-108">L'API XML in WWSAPI è basata sugli oggetti [Reader](xml-reader.md) e [writer](xml-writer.md) XML, che consentono la lettura o la scrittura di documenti XML in modo diretto.</span><span class="sxs-lookup"><span data-stu-id="e89b7-108">The XML API in WWSAPI is based on the [XML Reader](xml-reader.md) and [XML Writer](xml-writer.md) objects, which allow reading or writing of XML documents in a forward only fashion.</span></span> <span data-ttu-id="e89b7-109">Il livello XML fornisce all'applicazione l'accesso completo e il controllo sul contenuto dei messaggi.</span><span class="sxs-lookup"><span data-stu-id="e89b7-109">The XML Layer give the application full access to and control over the content of messages.</span></span>

## <a name="encoding"></a><span data-ttu-id="e89b7-110">Codifica</span><span class="sxs-lookup"><span data-stu-id="e89b7-110">Encoding</span></span>

<span data-ttu-id="e89b7-111">L'API XML supporta i documenti codificati come:</span><span class="sxs-lookup"><span data-stu-id="e89b7-111">The XML API supports documents encoded as:</span></span>

-   <span data-ttu-id="e89b7-112">Testo (UTF-8, UTF-16LE, UTF-16BE)</span><span class="sxs-lookup"><span data-stu-id="e89b7-112">Text (UTF-8, UTF-16LE, UTF-16BE)</span></span>
-   <span data-ttu-id="e89b7-113">Binary</span><span class="sxs-lookup"><span data-stu-id="e89b7-113">Binary</span></span>
-   <span data-ttu-id="e89b7-114">MTOM</span><span class="sxs-lookup"><span data-stu-id="e89b7-114">MTOM</span></span>

## <a name="storage"></a><span data-ttu-id="e89b7-115">Archiviazione</span><span class="sxs-lookup"><span data-stu-id="e89b7-115">Storage</span></span>

<span data-ttu-id="e89b7-116">L'API XML supporta l'elaborazione di documenti archiviati come:</span><span class="sxs-lookup"><span data-stu-id="e89b7-116">The XML API supports processing documents stored as:</span></span>

-   <span data-ttu-id="e89b7-117">Un buffer in memoria di byte codificati</span><span class="sxs-lookup"><span data-stu-id="e89b7-117">An in-memory buffer of encoded bytes</span></span>
-   <span data-ttu-id="e89b7-118">Un flusso</span><span class="sxs-lookup"><span data-stu-id="e89b7-118">A stream</span></span>
-   <span data-ttu-id="e89b7-119">Un [buffer XML](xml-buffer.md)</span><span class="sxs-lookup"><span data-stu-id="e89b7-119">An [XML Buffer](xml-buffer.md)</span></span>

<span data-ttu-id="e89b7-120">Un [buffer XML](xml-buffer.md) è una rappresentazione in memoria strutturata di un documento XML.</span><span class="sxs-lookup"><span data-stu-id="e89b7-120">An [XML Buffer](xml-buffer.md) is a structured in-memory representation of an XML document.</span></span> <span data-ttu-id="e89b7-121">Si tratta di una rappresentazione più efficiente rispetto a un documento codificato come byte.</span><span class="sxs-lookup"><span data-stu-id="e89b7-121">This is a more efficient representation than a document encoded as bytes.</span></span> <span data-ttu-id="e89b7-122">Un documento XML archiviato in un buffer XML può essere esplorato, letto o scritto.</span><span class="sxs-lookup"><span data-stu-id="e89b7-122">An XML document stored in an An XML Buffer can be navigated, read, or written.</span></span>

## <a name="io"></a><span data-ttu-id="e89b7-123">I/O</span><span class="sxs-lookup"><span data-stu-id="e89b7-123">I/O</span></span>

<span data-ttu-id="e89b7-124">L'API XML non eseguirà mai l'I/O, a meno che non sia richiesto in modo specifico.</span><span class="sxs-lookup"><span data-stu-id="e89b7-124">The XML API will never perform I/O unless specifically requested.</span></span> <span data-ttu-id="e89b7-125">Inoltre, tutte le I/O possono essere avviate in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="e89b7-125">Furthermore, any I/O may be initiated in an asynchronous fashion.</span></span> <span data-ttu-id="e89b7-126">Per informazioni dettagliate sull'elaborazione asincrona con l'API XML, vedere [**WsFillReader**](/windows/desktop/api/WebServices/nf-webservices-wsfillreader) e [**WsFlushWriter**](/windows/desktop/api/WebServices/nf-webservices-wsflushwriter) .</span><span class="sxs-lookup"><span data-stu-id="e89b7-126">See [**WsFillReader**](/windows/desktop/api/WebServices/nf-webservices-wsfillreader) and [**WsFlushWriter**](/windows/desktop/api/WebServices/nf-webservices-wsflushwriter) for details on asynchronous processing with the XML API.</span></span>

## <a name="processing"></a><span data-ttu-id="e89b7-127">Elaborazione in corso</span><span class="sxs-lookup"><span data-stu-id="e89b7-127">Processing</span></span>

<span data-ttu-id="e89b7-128">L'API XML presenta tre livelli distinti in cui è possibile elaborare il documento.</span><span class="sxs-lookup"><span data-stu-id="e89b7-128">The XML API has three distinct levels at which the document may be processed.</span></span>

<span data-ttu-id="e89b7-129">Un documento può essere elaborato un [**nodo**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_node) alla volta.</span><span class="sxs-lookup"><span data-stu-id="e89b7-129">A document may be processed a [**node**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_node) at a time.</span></span> <span data-ttu-id="e89b7-130">Questo consente una gestione più dettagliata del contenuto XML e fornisce la fedeltà completa dei dati dal documento.</span><span class="sxs-lookup"><span data-stu-id="e89b7-130">This offers the most fine-grained handling of the XML content, and provides complete fidelity of data from the document.</span></span> <span data-ttu-id="e89b7-131">A questo livello vengono usate le funzioni [**WsReadNode**](/windows/desktop/api/WebServices/nf-webservices-wsreadnode) e [**WsWriteNode**](/windows/desktop/api/WebServices/nf-webservices-wswritenode) e [**WsCopyNode**](/windows/desktop/api/WebServices/nf-webservices-wscopynode) .</span><span class="sxs-lookup"><span data-stu-id="e89b7-131">At this level, the functions [**WsReadNode**](/windows/desktop/api/WebServices/nf-webservices-wsreadnode) and [**WsWriteNode**](/windows/desktop/api/WebServices/nf-webservices-wswritenode) and [**WsCopyNode**](/windows/desktop/api/WebServices/nf-webservices-wscopynode) would be used.</span></span>

<span data-ttu-id="e89b7-132">Il livello di controllo successivo è costituito da API come [**WsReadStartElement**](/windows/desktop/api/WebServices/nf-webservices-wsreadstartelement), [**WsReadValue**](/windows/desktop/api/WebServices/nf-webservices-wsreadvalue) e [**WsReadEndElement**](/windows/desktop/api/WebServices/nf-webservices-wsreadendelement).</span><span class="sxs-lookup"><span data-stu-id="e89b7-132">The next level of control are APIs like [**WsReadStartElement**](/windows/desktop/api/WebServices/nf-webservices-wsreadstartelement), [**WsReadValue**](/windows/desktop/api/WebServices/nf-webservices-wsreadvalue) and [**WsReadEndElement**](/windows/desktop/api/WebServices/nf-webservices-wsreadendelement).</span></span> <span data-ttu-id="e89b7-133">Queste API forniscono numerosi tipi di convalida, ignorano gli spazi vuoti e i commenti e normalizzano testo e CDATA per presentare al consumer una visualizzazione più semplice del codice XML.</span><span class="sxs-lookup"><span data-stu-id="e89b7-133">These APIs provide numerous kinds of validation, skip whitespace and comments, and normalize text and CDATA to present the consumer with a simpler view of the xml.</span></span>

<span data-ttu-id="e89b7-134">Il livello massimo di controllo consiste nell'usare l'API di serializzazione.</span><span class="sxs-lookup"><span data-stu-id="e89b7-134">The highest level of control is to use the Serialization API.</span></span> <span data-ttu-id="e89b7-135">Queste API sono derivate da un mapping tra i tipi di dati C e XML e possono leggere o scrivere una struttura complessa in memoria in XML e viceversa con una singola funzione, ad esempio [**WsWriteElement**](/windows/desktop/api/WebServices/nf-webservices-wswriteelement) e [**WsReadElement**](/windows/desktop/api/WebServices/nf-webservices-wsreadelement).</span><span class="sxs-lookup"><span data-stu-id="e89b7-135">These APIs are driven off a mapping between C data types and XML, and can read or write a complex in-memory structure to xml and back with a single function like [**WsWriteElement**](/windows/desktop/api/WebServices/nf-webservices-wswriteelement) and [**WsReadElement**](/windows/desktop/api/WebServices/nf-webservices-wsreadelement).</span></span>

<span data-ttu-id="e89b7-136">È possibile utilizzare le API di canonizzazione XML per generare una forma canonica di codice XML che a sua volta può essere utilizzata per la generazione di firme crittografiche sul contenuto XML.</span><span class="sxs-lookup"><span data-stu-id="e89b7-136">The XML Canonicalization APIs may be used to generate a canonical form of XML which may in turn be used for generating cryptographic signatures over XML content.</span></span>

## <a name="creating-a-writer"></a><span data-ttu-id="e89b7-137">Creazione di un writer</span><span class="sxs-lookup"><span data-stu-id="e89b7-137">Creating a writer</span></span>

<span data-ttu-id="e89b7-138">Per creare e usare un writer per scrivere in un buffer in memoria:</span><span class="sxs-lookup"><span data-stu-id="e89b7-138">To create and use a writer to write to an in-memory buffer:</span></span>

``` syntax
WsCreateWriter              // Create an instance of a WS_XML_WRITER
// Initialize a WS_XML_WRITER_BUFFER_OUTPUT
WsSetOutput                 // Set the encoding and output of the writer along with any other writer properties
// Write Elements
WsGetWriterProperty(..., WS_XML_WRITER_PROPERTY_BYTES, ...)  // Get the generated bytes as a single byte array
// Use the generated bytes
WsFreeWriter                // Free the writer
```

<span data-ttu-id="e89b7-139">Per creare e usare un writer per scrivere in un flusso:</span><span class="sxs-lookup"><span data-stu-id="e89b7-139">To create and use a writer to write to a stream:</span></span>

``` syntax
WsCreateWriter              // Create an instance of a WS_XML_WRITER
// Initialize a WS_XML_WRITER_STREAM_OUTPUT
WsSetOutput                 // Set the encoding and output of the writer along with any other writer properties
// Write Elements
WsFlushWriter               // Force any buffered data to be written
WsFreeWriter                // Free the writer
```

<span data-ttu-id="e89b7-140">Per creare e utilizzare un writer per scrivere in un [ \_ \_ buffer WS XML](ws-xml-buffer.md):</span><span class="sxs-lookup"><span data-stu-id="e89b7-140">To create and use a writer to write to a [WS\_XML\_BUFFER](ws-xml-buffer.md):</span></span>

``` syntax
WsCreateXmlBuffer           // Create the buffer to write to
WsCreateWriter              // Create an instance of a WS_XML_WRITER
WsSetOutputToBuffer         // Set the output buffer along with any other writer properties
// Write Elements
WsFreeWriter                // Free the writer
// The buffer has the generated document
```

<span data-ttu-id="e89b7-141">In tutti i casi, è possibile includere il [**\_ \_ \_ \_ rientro della proprietà WS XML writer**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_writer_property_id) per formattare il codice XML.</span><span class="sxs-lookup"><span data-stu-id="e89b7-141">In all cases, the property [**WS\_XML\_WRITER\_PROPERTY\_INDENT**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_writer_property_id) may be included to format the xml.</span></span>

## <a name="writing-elements"></a><span data-ttu-id="e89b7-142">Scrittura di elementi</span><span class="sxs-lookup"><span data-stu-id="e89b7-142">Writing Elements</span></span>

<span data-ttu-id="e89b7-143">Per scrivere un elemento in un writer:</span><span class="sxs-lookup"><span data-stu-id="e89b7-143">To write an element to a writer:</span></span>

``` syntax
WsWriteStartElement          // Write a start element
for each attribute
{
// Write an attribute using either
WsWriteStartAttribute    // Write a start attribute
// Write Content
WsWriteEndAttribute      // Write an end attribute
// Or one of the following
WsWriteXmlnsAttribute    // Write an explicit xmlns attribute
}
// Write Elements or Content
WsWriteEndElement
```

<span data-ttu-id="e89b7-144">È possibile utilizzare anche quanto segue:</span><span class="sxs-lookup"><span data-stu-id="e89b7-144">The following may also be used:</span></span>

``` syntax
WsWriteArray                 // Write an array of primitive values as a series of repeated elements
```

## <a name="writing-content"></a><span data-ttu-id="e89b7-145">Scrittura di contenuto</span><span class="sxs-lookup"><span data-stu-id="e89b7-145">Writing Content</span></span>

<span data-ttu-id="e89b7-146">Per scrivere contenuto in un elemento o un attributo, è possibile usare quanto segue:</span><span class="sxs-lookup"><span data-stu-id="e89b7-146">To write content to an element or attribute, the following may be used:</span></span>

``` syntax
WsWriteChars                 // Write unicode characters from memory
WsWriteCharsUtf8             // Write UTF-8 encoded characters from memory
WsWriteBytes                 // Write binary data encoded as base64
WsPushBytes                  // Direct the writer to request that bytes be written
WsPullBytes                  // Direct the writer to read the bytes to be written
WsWriteValue                 // Write primitive values such as ints and BOOLs
WsWriteText                  // Write an WS_XML_TEXT
WsWriteQualifiedName         // Write a qualified name
```

<span data-ttu-id="e89b7-147">Gli elementi seguenti possono essere utilizzati per scrivere in un documento, ma non possono essere utilizzati all'interno di un attributo.</span><span class="sxs-lookup"><span data-stu-id="e89b7-147">The following can be used to write to a document, but may not be used when within an attribute.</span></span>

``` syntax
WsWriteNode                  // Write a single WS_XML_NODE
WsCopyNode                   // Copy a single node, or an entire WS_XML_ELEMENT_NODE and children from an WS_XML_READER
```

<span data-ttu-id="e89b7-148">Per scrivere una sezione CDATA in un documento di testo, è possibile utilizzare quanto segue:</span><span class="sxs-lookup"><span data-stu-id="e89b7-148">The following may be used to write a CDATA section in a text document:</span></span>

``` syntax
WsWriteStartCData            // Start a CDATA section in a text encoding
// Write Content
WsWriteEndCData              // End a CDATA section in text encoding
```

## <a name="miscellaneous"></a><span data-ttu-id="e89b7-149">Varie</span><span class="sxs-lookup"><span data-stu-id="e89b7-149">Miscellaneous</span></span>

``` syntax
WsGetPrefixFromNamespace     // Find a prefix bound to a namespace
```

## <a name="creating-a-reader"></a><span data-ttu-id="e89b7-150">Creazione di un lettore</span><span class="sxs-lookup"><span data-stu-id="e89b7-150">Creating a reader</span></span>

<span data-ttu-id="e89b7-151">Per creare e usare un Reader per la lettura da un buffer in memoria:</span><span class="sxs-lookup"><span data-stu-id="e89b7-151">To create and use a reader to read from an in-memory buffer:</span></span>

``` syntax
WsCreateReader              // Create an instance of a WS_XML_READER
// Initialize a WS_XML_READER_BUFFER_INPUT
WsSetInput                  // Set the encoding and input of the reader along with any other reader properties
// Read Elements
WsFreeReader                // Free the reader
```

<span data-ttu-id="e89b7-152">Per creare e usare un Reader per il lettore da un flusso:</span><span class="sxs-lookup"><span data-stu-id="e89b7-152">To create and use a reader to reader from a stream:</span></span>

``` syntax
WsCreateReader              // Create an instance of a WS_XML_READER
// Initialize a WS_XML_READER_STREAM_INPUT
WsSetInput                  // Set the encoding and input of the reader along with any other reader properties
WsFillReader                // Populate the reader with data from the underlying stream
// Read Elements
WsFreeReader                // Free the reader
```

<span data-ttu-id="e89b7-153">Per creare e utilizzare un Reader per la lettura da [un \_ \_ buffer WS XML](ws-xml-buffer.md):</span><span class="sxs-lookup"><span data-stu-id="e89b7-153">To create and use a reader to read from a [WS\_XML\_BUFFER](ws-xml-buffer.md):</span></span>

``` syntax
WsCreateXmlBuffer           // Create the buffer to write to
WsCreateReader              // Create an instance of a WS_XML_READER
WsSetInputToBuffer          // Set the input buffer along with any other reader properties
// Read Elements
WsFreeReader                // Free the reader
```

## <a name="reading-elements"></a><span data-ttu-id="e89b7-154">Lettura di elementi</span><span class="sxs-lookup"><span data-stu-id="e89b7-154">Reading Elements</span></span>

<span data-ttu-id="e89b7-155">Per leggere un elemento da un lettore:</span><span class="sxs-lookup"><span data-stu-id="e89b7-155">To read an element from a reader:</span></span>

``` syntax
WsReadToStartElement         // Skip whitespace and comments to position the reader on a specific element
for each attribute of interest
{
WsFindAttribute          // Try Locate the attribute
if (found)
{
WsReadStartAttribute // Set the reader to read the attribute
// Read Content
WsReadEndAttribute   // Return the reader to the element
}
}
WsReadStartElement           // Advance the reader past the current element
// Read Elements or Content
WsWriteEndElement            // Advance the reader past the corresponding end element
```

<span data-ttu-id="e89b7-156">È possibile utilizzare anche quanto segue:</span><span class="sxs-lookup"><span data-stu-id="e89b7-156">The following may also be used:</span></span>

``` syntax
WsReadArray                  // Read an array of primitive values as a series of repeated elements
```

## <a name="reading-content"></a><span data-ttu-id="e89b7-157">Lettura del contenuto</span><span class="sxs-lookup"><span data-stu-id="e89b7-157">Reading Content</span></span>

<span data-ttu-id="e89b7-158">Per leggere il contenuto da un elemento o un attributo, è possibile usare quanto segue:</span><span class="sxs-lookup"><span data-stu-id="e89b7-158">To read content from an element or attribute, the following may be used:</span></span>

``` syntax
WsReadChars                 // Read characters to memory as unicode
WsReadCharsUtf8             // Read characters to memory encoded as UTF-8
WsReadBytes                 // Read binary data encoded as base64
WsReadValue                 // Read primitive values such as ints and BOOLs
WsReadQualifiedName         // Read a qualified name
```

<span data-ttu-id="e89b7-159">Per esaminare il nodo corrente su cui è posizionato il lettore, è possibile utilizzare il codice seguente:</span><span class="sxs-lookup"><span data-stu-id="e89b7-159">The following may be used to inspect the current node the reader is positioned on:</span></span>

``` syntax
WsGetReaderNode             // Get the current node
```

## <a name="using-a-buffer"></a><span data-ttu-id="e89b7-160">Uso di un buffer</span><span class="sxs-lookup"><span data-stu-id="e89b7-160">Using a buffer</span></span>

<span data-ttu-id="e89b7-161">Quando si scrive in [un \_ \_ buffer WS XML](ws-xml-buffer.md) , è possibile usare il codice seguente:</span><span class="sxs-lookup"><span data-stu-id="e89b7-161">When writing to a [WS\_XML\_BUFFER](ws-xml-buffer.md) the following may be used:</span></span>

``` syntax
WsGetWriterPosition          // Get the current position of the writer in the document
WsSetWriterPosition          // Set the current position of the writer in the document
WsMoveWriter                 // Move relative to the current position in the document
WsRemoveNode                 // Delete an element or text from a document
```

<span data-ttu-id="e89b7-162">Quando si esegue la lettura da un [ \_ \_ buffer WS XML](ws-xml-buffer.md) , è possibile usare il codice seguente:</span><span class="sxs-lookup"><span data-stu-id="e89b7-162">When reading from a [WS\_XML\_BUFFER](ws-xml-buffer.md) the following may be used:</span></span>

``` syntax
WsGetReaderPosition          // Get the current position of the reader in the document
WsSetReaderPosition          // Set the current position of the reader in the document
WsMoveReader                 // Move relative to the current position in the document
```

<span data-ttu-id="e89b7-163">Per modificare un [ \_ \_ buffer WS XML](ws-xml-buffer.md), è possibile utilizzare quanto segue:</span><span class="sxs-lookup"><span data-stu-id="e89b7-163">The following may be used to modify a [WS\_XML\_BUFFER](ws-xml-buffer.md):</span></span>

``` syntax

WsRemoveNode                 // Delete an element or text from a document
```

## <a name="other"></a><span data-ttu-id="e89b7-164">Altri</span><span class="sxs-lookup"><span data-stu-id="e89b7-164">Other</span></span>

``` syntax
WsGetNamespaceFromPrefix     // Find a namespace bound to a prefix
WsGetXmlAttribute            // Find an "xml:space" or "xml:lang" attribute in scope
```

 

 




