---
title: Lettore XML
description: Il lettore XML è un cursore su un'origine di input di XML. Al suo nucleo, un lettore XML legge un nodo XML alla volta, ma sono disponibili API helper aggiuntive per semplificare la lettura di una sequenza di nodi.
ms.assetid: 1f99e45c-64ba-42fb-9bf0-35e27f1c5ef2
keywords:
- Servizi Web Reader XML per Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d9d9c91b6594ec569536751751a3efca4c32e08
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "104474657"
---
# <a name="xml-reader"></a><span data-ttu-id="c76a2-107">Lettore XML</span><span class="sxs-lookup"><span data-stu-id="c76a2-107">XML Reader</span></span>

<span data-ttu-id="c76a2-108">Il lettore XML è un cursore su un'origine di input di XML.</span><span class="sxs-lookup"><span data-stu-id="c76a2-108">XML Reader is a cursor over an input source of XML.</span></span> <span data-ttu-id="c76a2-109">Al suo nucleo, un lettore XML legge un [nodo XML](xml-node.md) alla volta, ma sono disponibili API helper aggiuntive per semplificare la lettura di una sequenza di nodi.</span><span class="sxs-lookup"><span data-stu-id="c76a2-109">At its core, an XML Reader reads one [XML Node](xml-node.md) at a time, but there are additional helper APIs to make reading a sequence of nodes easier.</span></span>


<span data-ttu-id="c76a2-110">Sono supportati i tipi di input Reader seguenti:</span><span class="sxs-lookup"><span data-stu-id="c76a2-110">The following types of readers input are supported:</span></span>

-   [<span data-ttu-id="c76a2-111">**Un buffer in memoria di byte codificati**</span><span class="sxs-lookup"><span data-stu-id="c76a2-111">**An in-memory buffer of encoded bytes**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_buffer_input)
-   [<span data-ttu-id="c76a2-112">**Un flusso**</span><span class="sxs-lookup"><span data-stu-id="c76a2-112">**A stream**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_stream_input)
-   <span data-ttu-id="c76a2-113">Un [buffer XML](xml-buffer.md)</span><span class="sxs-lookup"><span data-stu-id="c76a2-113">An [XML Buffer](xml-buffer.md)</span></span>

### <a name="security"></a><span data-ttu-id="c76a2-114">Sicurezza</span><span class="sxs-lookup"><span data-stu-id="c76a2-114">Security</span></span>

<span data-ttu-id="c76a2-115">Il lettore verificherà che gli attributi presenti in un elemento siano univoci.</span><span class="sxs-lookup"><span data-stu-id="c76a2-115">The reader will verify that the attributes present on an element are unique.</span></span> <span data-ttu-id="c76a2-116">Il tempo necessario per eseguire questa convalida è una funzione del numero di attributi sull'elemento che può essere pari a quello degli [**\_ \_ \_ \_ \_ attributi max della proprietà Reader di WS XML**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_reader_property_id).</span><span class="sxs-lookup"><span data-stu-id="c76a2-116">The time required to perform this validation is a function of the number of attributes on the element which can be as large as [**WS\_XML\_READER\_PROPERTY\_MAX\_ATTRIBUTES**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_reader_property_id).</span></span> <span data-ttu-id="c76a2-117">Di conseguenza, l'elaborazione di documenti di grandi dimensioni quando la **\_ \_ \_ proprietà \_ Max \_ del lettore XML WS** è impostata su un valore elevato può presentare un'opportunità di attacco Denial of Service.</span><span class="sxs-lookup"><span data-stu-id="c76a2-117">Therefore, processing large documents when **WS\_XML\_READER\_PROPERTY\_MAX\_ATTRIBUTES** is set to a large value may present an opportunity for a denial of service attack.</span></span>

<span data-ttu-id="c76a2-118">Il lettore eseguirà il mapping dei prefissi agli spazi dei nomi per ogni elemento e attributo.</span><span class="sxs-lookup"><span data-stu-id="c76a2-118">The reader will map prefixes to namespaces for each element and attributes.</span></span> <span data-ttu-id="c76a2-119">Il tempo necessario per eseguire questo mapping è una funzione del numero di attributi xmlns nell'ambito, che può avere dimensioni pari alla [**\_ \_ \_ proprietà \_ Max \_ del lettore XML WS**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_reader_property_id).</span><span class="sxs-lookup"><span data-stu-id="c76a2-119">The time required to perform this mapping is a function of the number of xmlns attributes in scope which may be as large as [**WS\_XML\_READER\_PROPERTY\_MAX\_NAMESPACES**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_reader_property_id).</span></span> <span data-ttu-id="c76a2-120">Pertanto, l'elaborazione di documenti di grandi dimensioni quando questa proprietà è impostata su un valore elevato può presentare un'opportunità per un attacco Denial of Service.</span><span class="sxs-lookup"><span data-stu-id="c76a2-120">Therefore, processing large documents when this property is set to a large value may present an opportunity for a denial of service attack.</span></span>

<span data-ttu-id="c76a2-121">Sebbene il lettore garantisca che il documento segua la specifica grammaticale del codice XML e che i relativi aspetti siano all'interno delle quote specificate, il contenuto del documento deve essere considerato non attendibile quando provengono da un'origine non attendibile.</span><span class="sxs-lookup"><span data-stu-id="c76a2-121">While the reader will ensure that the document follows the grammatical specification of xml and furthermore that its aspects are within the quotas specified, the content of the document must still be considered untrusted when coming from an untrusted source.</span></span> <span data-ttu-id="c76a2-122">Gli utenti del lettore dovrebbero controllare tutti i nomi di elementi e attributi e gli spazi dei nomi usando [**WsReadToStartElement**](/windows/desktop/api/WebServices/nf-webservices-wsreadtostartelement), [**WsFindAttribute**](/windows/desktop/api/WebServices/nf-webservices-wsfindattribute)o ispezionando manualmente i [**nodi**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_node).</span><span class="sxs-lookup"><span data-stu-id="c76a2-122">Users of the reader should check all element and attribute names and namespaces using [**WsReadToStartElement**](/windows/desktop/api/WebServices/nf-webservices-wsreadtostartelement), [**WsFindAttribute**](/windows/desktop/api/WebServices/nf-webservices-wsfindattribute), or by manually inspecting [**nodes**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_node).</span></span>

<span data-ttu-id="c76a2-123">Di seguito sono riportate alcune altre situazioni da considerare:</span><span class="sxs-lookup"><span data-stu-id="c76a2-123">Some other situations to consider include, but are not limited to:</span></span>

-   <span data-ttu-id="c76a2-124">È possibile che gli elementi previsti siano mancanti</span><span class="sxs-lookup"><span data-stu-id="c76a2-124">Expected elements may be missing</span></span>
-   <span data-ttu-id="c76a2-125">È possibile che vengano visualizzati elementi imprevisti</span><span class="sxs-lookup"><span data-stu-id="c76a2-125">Unexpected elements may appear</span></span>
-   <span data-ttu-id="c76a2-126">È possibile che gli attributi previsti siano mancanti</span><span class="sxs-lookup"><span data-stu-id="c76a2-126">Expected attributes may be missing</span></span>
-   <span data-ttu-id="c76a2-127">È possibile che vengano visualizzati attributi imprevisti</span><span class="sxs-lookup"><span data-stu-id="c76a2-127">Unexpected attributes may appear</span></span>
-   <span data-ttu-id="c76a2-128">Gli elementi possono apparire come elementi vuoti</span><span class="sxs-lookup"><span data-stu-id="c76a2-128">Elements may appear as empty elements</span></span>
-   <span data-ttu-id="c76a2-129">Gli spazi vuoti possono essere visualizzati in posizioni non previste</span><span class="sxs-lookup"><span data-stu-id="c76a2-129">Whitespace may appear in unexpected places</span></span>

<span data-ttu-id="c76a2-130">Gli utenti del lettore non devono allocare memoria basata semplicemente sui valori letti dal documento.</span><span class="sxs-lookup"><span data-stu-id="c76a2-130">Users of the reader should not allocate memory based simply on values read from the document.</span></span> <span data-ttu-id="c76a2-131">Si consideri, ad esempio, il documento XML seguente:</span><span class="sxs-lookup"><span data-stu-id="c76a2-131">For example, consider the following xml document:</span></span>

``` syntax
<array count='1000000'>
   <!-- malicious document provider didn't actually provide 1000000 array items -->
</array>
```

<span data-ttu-id="c76a2-132">L'allocazione di una matrice basata esclusivamente sul presupposto che un certo numero di elementi seguirebbe un potenziale vettore di attacco.</span><span class="sxs-lookup"><span data-stu-id="c76a2-132">Allocating an array based soley on the assumption that some number of elements will follow would be a potential attack vector.</span></span> <span data-ttu-id="c76a2-133">In questo caso, l'utente del lettore deve allocare in modo incrementale la memoria mentre gli elementi vengono visualizzati.</span><span class="sxs-lookup"><span data-stu-id="c76a2-133">The user of the reader in this case should instead incrementally allocate the memory as the elements appear.</span></span>

<span data-ttu-id="c76a2-134">Il lettore XML non supporta la definizione DTD.</span><span class="sxs-lookup"><span data-stu-id="c76a2-134">XML reader does not support DTD.</span></span> <span data-ttu-id="c76a2-135">Non è necessario che l'utente del lettore si occupi della verifica della DTD.</span><span class="sxs-lookup"><span data-stu-id="c76a2-135">The user of the reader does not need to concern about DTD verification.</span></span>

<span data-ttu-id="c76a2-136">Il callback seguente viene utilizzato con i reader XML:</span><span class="sxs-lookup"><span data-stu-id="c76a2-136">The following callback is used with XML readers:</span></span>

-   [<span data-ttu-id="c76a2-137">**\_callback di lettura WS \_**</span><span class="sxs-lookup"><span data-stu-id="c76a2-137">**WS\_READ\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_read_callback)

<span data-ttu-id="c76a2-138">Con i reader XML vengono utilizzate le enumerazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="c76a2-138">The following enumerations are used with XML readers:</span></span>

-   [<span data-ttu-id="c76a2-139">**\_tipo di \_ codifica del lettore XML \_ WS \_**</span><span class="sxs-lookup"><span data-stu-id="c76a2-139">**WS\_XML\_READER\_ENCODING\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_xml_reader_encoding_type)
-   [<span data-ttu-id="c76a2-140">**\_tipo di \_ input del lettore XML \_ WS \_**</span><span class="sxs-lookup"><span data-stu-id="c76a2-140">**WS\_XML\_READER\_INPUT\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_xml_reader_input_type)
-   [<span data-ttu-id="c76a2-141">**\_ \_ \_ ID proprietà lettore XML \_ WS**</span><span class="sxs-lookup"><span data-stu-id="c76a2-141">**WS\_XML\_READER\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_xml_reader_property_id)

<span data-ttu-id="c76a2-142">Con i reader XML vengono utilizzate le funzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="c76a2-142">The following functions are used with XML readers:</span></span>

-   [<span data-ttu-id="c76a2-143">**WsCreateReader**</span><span class="sxs-lookup"><span data-stu-id="c76a2-143">**WsCreateReader**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wscreatereader)
-   [<span data-ttu-id="c76a2-144">**WsFillReader**</span><span class="sxs-lookup"><span data-stu-id="c76a2-144">**WsFillReader**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsfillreader)
-   [<span data-ttu-id="c76a2-145">**WsFindAttribute**</span><span class="sxs-lookup"><span data-stu-id="c76a2-145">**WsFindAttribute**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsfindattribute)
-   [<span data-ttu-id="c76a2-146">**WsFreeReader**</span><span class="sxs-lookup"><span data-stu-id="c76a2-146">**WsFreeReader**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsfreereader)
-   [<span data-ttu-id="c76a2-147">**WsGetNamespaceFromPrefix**</span><span class="sxs-lookup"><span data-stu-id="c76a2-147">**WsGetNamespaceFromPrefix**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetnamespacefromprefix)
-   [<span data-ttu-id="c76a2-148">**WsGetReaderNode**</span><span class="sxs-lookup"><span data-stu-id="c76a2-148">**WsGetReaderNode**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetreadernode)
-   [<span data-ttu-id="c76a2-149">**WsGetReaderPosition**</span><span class="sxs-lookup"><span data-stu-id="c76a2-149">**WsGetReaderPosition**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetreaderposition)
-   [<span data-ttu-id="c76a2-150">**WsGetReaderProperty**</span><span class="sxs-lookup"><span data-stu-id="c76a2-150">**WsGetReaderProperty**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetreaderproperty)
-   [<span data-ttu-id="c76a2-151">**WsGetXmlAttribute**</span><span class="sxs-lookup"><span data-stu-id="c76a2-151">**WsGetXmlAttribute**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetxmlattribute)
-   [<span data-ttu-id="c76a2-152">**WsMoveReader**</span><span class="sxs-lookup"><span data-stu-id="c76a2-152">**WsMoveReader**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsmovereader)
-   [<span data-ttu-id="c76a2-153">**WsReadArray**</span><span class="sxs-lookup"><span data-stu-id="c76a2-153">**WsReadArray**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsreadarray)
-   [<span data-ttu-id="c76a2-154">**WsReadBytes**</span><span class="sxs-lookup"><span data-stu-id="c76a2-154">**WsReadBytes**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsreadbytes)
-   [<span data-ttu-id="c76a2-155">**WsReadChars**</span><span class="sxs-lookup"><span data-stu-id="c76a2-155">**WsReadChars**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsreadchars)
-   [<span data-ttu-id="c76a2-156">**WsReadCharsUtf8**</span><span class="sxs-lookup"><span data-stu-id="c76a2-156">**WsReadCharsUtf8**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsreadcharsutf8)
-   [<span data-ttu-id="c76a2-157">**WsReadEndAttribute**</span><span class="sxs-lookup"><span data-stu-id="c76a2-157">**WsReadEndAttribute**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsreadendattribute)
-   [<span data-ttu-id="c76a2-158">**WsReadEndElement**</span><span class="sxs-lookup"><span data-stu-id="c76a2-158">**WsReadEndElement**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsreadendelement)
-   [<span data-ttu-id="c76a2-159">**WsReadNode**</span><span class="sxs-lookup"><span data-stu-id="c76a2-159">**WsReadNode**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsreadnode)
-   [<span data-ttu-id="c76a2-160">**WsReadQualifiedName**</span><span class="sxs-lookup"><span data-stu-id="c76a2-160">**WsReadQualifiedName**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsreadqualifiedname)
-   [<span data-ttu-id="c76a2-161">**WsReadStartAttribute**</span><span class="sxs-lookup"><span data-stu-id="c76a2-161">**WsReadStartAttribute**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsreadstartattribute)
-   [<span data-ttu-id="c76a2-162">**WsReadStartElement**</span><span class="sxs-lookup"><span data-stu-id="c76a2-162">**WsReadStartElement**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsreadstartelement)
-   [<span data-ttu-id="c76a2-163">**WsReadToStartElement**</span><span class="sxs-lookup"><span data-stu-id="c76a2-163">**WsReadToStartElement**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsreadtostartelement)
-   [<span data-ttu-id="c76a2-164">**WsReadValue**</span><span class="sxs-lookup"><span data-stu-id="c76a2-164">**WsReadValue**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsreadvalue)
-   [<span data-ttu-id="c76a2-165">**WsSetInput**</span><span class="sxs-lookup"><span data-stu-id="c76a2-165">**WsSetInput**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wssetinput)
-   [<span data-ttu-id="c76a2-166">**WsSetInputToBuffer**</span><span class="sxs-lookup"><span data-stu-id="c76a2-166">**WsSetInputToBuffer**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wssetinputtobuffer)
-   [<span data-ttu-id="c76a2-167">**WsSetReaderPosition**</span><span class="sxs-lookup"><span data-stu-id="c76a2-167">**WsSetReaderPosition**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wssetreaderposition)
-   [<span data-ttu-id="c76a2-168">**WsSkipNode**</span><span class="sxs-lookup"><span data-stu-id="c76a2-168">**WsSkipNode**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsskipnode)

<span data-ttu-id="c76a2-169">Con i reader XML viene utilizzato l'handle seguente:</span><span class="sxs-lookup"><span data-stu-id="c76a2-169">The following handle is used with XML readers:</span></span>

-   [<span data-ttu-id="c76a2-170">\_lettore XML \_ WS</span><span class="sxs-lookup"><span data-stu-id="c76a2-170">WS\_XML\_READER</span></span>](ws-xml-reader.md)

<span data-ttu-id="c76a2-171">Con i reader XML vengono utilizzate le strutture seguenti:</span><span class="sxs-lookup"><span data-stu-id="c76a2-171">The following structures are used with XML readers:</span></span>

-   [<span data-ttu-id="c76a2-172">**\_ \_ \_ codifica binaria del lettore XML WS \_**</span><span class="sxs-lookup"><span data-stu-id="c76a2-172">**WS\_XML\_READER\_BINARY\_ENCODING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_binary_encoding)
-   [<span data-ttu-id="c76a2-173">**\_ \_ input buffer del lettore XML \_ WS \_**</span><span class="sxs-lookup"><span data-stu-id="c76a2-173">**WS\_XML\_READER\_BUFFER\_INPUT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_buffer_input)
-   [<span data-ttu-id="c76a2-174">**\_codifica del \_ lettore \_ XML WS**</span><span class="sxs-lookup"><span data-stu-id="c76a2-174">**WS\_XML\_READER\_ENCODING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_encoding)
-   [<span data-ttu-id="c76a2-175">**\_ \_ input lettore XML \_ WS**</span><span class="sxs-lookup"><span data-stu-id="c76a2-175">**WS\_XML\_READER\_INPUT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_input)
-   [<span data-ttu-id="c76a2-176">**\_ \_ codifica MTOM del lettore XML \_ WS \_**</span><span class="sxs-lookup"><span data-stu-id="c76a2-176">**WS\_XML\_READER\_MTOM\_ENCODING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_mtom_encoding)
-   [<span data-ttu-id="c76a2-177">**\_proprietà del \_ lettore \_ XML WS**</span><span class="sxs-lookup"><span data-stu-id="c76a2-177">**WS\_XML\_READER\_PROPERTIES**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_properties)
-   [<span data-ttu-id="c76a2-178">**\_proprietà del \_ lettore \_ XML WS**</span><span class="sxs-lookup"><span data-stu-id="c76a2-178">**WS\_XML\_READER\_PROPERTY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_property)
-   [<span data-ttu-id="c76a2-179">**\_ \_ input flusso del lettore XML \_ WS \_**</span><span class="sxs-lookup"><span data-stu-id="c76a2-179">**WS\_XML\_READER\_STREAM\_INPUT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_stream_input)
-   [<span data-ttu-id="c76a2-180">**\_codifica del \_ testo del lettore XML \_ WS \_**</span><span class="sxs-lookup"><span data-stu-id="c76a2-180">**WS\_XML\_READER\_TEXT\_ENCODING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_text_encoding)

 

 




