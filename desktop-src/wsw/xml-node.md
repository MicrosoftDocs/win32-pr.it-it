---
title: Nodo XML
description: Un nodo XML rappresenta una singola parte di XML, ad esempio un elemento iniziale e i relativi attributi, un elemento finale, un testo o \ 0034; tipizzato \ 0034; contenuto di testo, ad esempio una matrice di byte o Integer. I dati in un nodo variano in base al \_ tipo di \_ nodo WS XML \_ .
ms.assetid: c514c542-029b-46d1-a796-1f132a41b2ad
keywords:
- Servizi Web del nodo XML per Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac212205fac02db0ee87d8acbe0b123ffcead921
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "106300692"
---
# <a name="xml-node"></a><span data-ttu-id="388c3-107">Nodo XML</span><span class="sxs-lookup"><span data-stu-id="388c3-107">XML Node</span></span>

<span data-ttu-id="388c3-108">Un nodo XML rappresenta una singola porzione di codice XML, ad esempio un elemento iniziale e i relativi attributi, un elemento finale, un testo o un contenuto di testo tipizzato, ad esempio una matrice di byte o un numero intero.</span><span class="sxs-lookup"><span data-stu-id="388c3-108">An XML Node represents a single piece of XML, for example, a start element and its attributes, an end element, text, or "typed" text content such as an integer or byte array.</span></span> <span data-ttu-id="388c3-109">I dati in un nodo variano in base al [**\_ tipo di \_ nodo \_ WS XML**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_node_type).</span><span class="sxs-lookup"><span data-stu-id="388c3-109">The data in a node varies according to the [**WS\_XML\_NODE\_TYPE**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_node_type).</span></span>


<span data-ttu-id="388c3-110">Di seguito viene illustrato un esempio di un documento XML specifico di codifica rappresentato con strutture indipendenti di codifica.</span><span class="sxs-lookup"><span data-stu-id="388c3-110">The following shows an example of an encoding specific xml document represented with encoding independent structures.</span></span>

``` syntax
<p:PurchaseOrder xmlns:p="http://tempuri.org" p:id="3891">
    <p:Buyer>Joe</p:Buyer>
</p:PurchaseOrder>
```

``` syntax
WS_XML_STRING purchaseOrder = WS_XML_STRING_VALUE("PurchaseOrder");
WS_XML_STRING id            = WS_XML_STRING_VALUE("id");
WS_XML_STRING prefix        = WS_XML_STRING_VALUE("p");
WS_XML_STRING ns            = WS_XML_STRING_VALUE("http://tempuri.org");

WS_XML_ATTRIBUTE xmlnsAttribute =
{
    /* singleQuote */ FALSE,
    /* isXmlNs     */ TRUE,
    /* prefix      */ &prefix,
    /* localName   */ NULL,
    /* ns          */ &ns,
    /* value       */ NULL
};
WS_XML_INT32_TEXT idText =
{
    /* text  */ { WS_XML_TEXT_TYPE_INT32 },
    /* value */ 3891
};
WS_XML_ATTRIBUTE idAttribute =
{
    /* singleQuote */ FALSE,
    /* isXmlNs     */ FALSE,
    /* prefix      */ &prefix,
    /* localName   */ &id,
    /* ns          */ &ns,
    /* value       */ &idText.text,
};
WS_XML_ATTRIBUTE* attributes[2] =
{
    &xmlnsAttribute,
    &idAttribute
};
WS_XML_ELEMENT_NODE elementNode =
{
    /* node           */ { WS_XML_NODE_TYPE_ELEMENT },
    /* prefix         */ &prefix,
    /* localName      */ &purchaseOrder,
    /* ns             */ &ns,
    /* attributeCount */ 2,
    /* attributes     */ attributes,
    /* isEmpty        */ FALSE,
    /* array          */ NULL,
};
WS_XML_UTF8_TEXT joeText =
{
    /* text  */ { WS_XML_TEXT_TYPE_UTF8 },
    /* value */ WS_XML_STRING_VALUE("Joe")
};
WS_XML_TEXT_NODE textNode =
{
    /* node */ { WS_XML_NODE_TYPE_TEXT },
    /* text */ &joeText.text
};
WS_XML_NODE endElementNode =
{
    WS_XML_NODE_TYPE_END_ELEMENT
};
WS_XML_NODE* nodes[3] =
{
    &elementNode.node,
    &textNode.node,
    &endElementNode
};
```

<span data-ttu-id="388c3-111">Con i nodi XML vengono utilizzate le enumerazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="388c3-111">The following enumerations are used with XML nodes:</span></span>

-   [<span data-ttu-id="388c3-112">**\_tipo di valore WS \_**</span><span class="sxs-lookup"><span data-stu-id="388c3-112">**WS\_VALUE\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_value_type)
-   [<span data-ttu-id="388c3-113">**\_tipo di \_ nodo WS XML \_**</span><span class="sxs-lookup"><span data-stu-id="388c3-113">**WS\_XML\_NODE\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_xml_node_type)
-   [<span data-ttu-id="388c3-114">**\_tipo di \_ testo WS XML \_**</span><span class="sxs-lookup"><span data-stu-id="388c3-114">**WS\_XML\_TEXT\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_xml_text_type)

<span data-ttu-id="388c3-115">Con i nodi XML vengono usate le funzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="388c3-115">The following functions are used with XML nodes:</span></span>

-   [<span data-ttu-id="388c3-116">**WsTrimXmlWhitespace**</span><span class="sxs-lookup"><span data-stu-id="388c3-116">**WsTrimXmlWhitespace**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wstrimxmlwhitespace)
-   [<span data-ttu-id="388c3-117">**WsVerifyXmlNCName**</span><span class="sxs-lookup"><span data-stu-id="388c3-117">**WsVerifyXmlNCName**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsverifyxmlncname)
-   [<span data-ttu-id="388c3-118">**WsXmlStringEquals**</span><span class="sxs-lookup"><span data-stu-id="388c3-118">**WsXmlStringEquals**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsxmlstringequals)

<span data-ttu-id="388c3-119">Con i nodi XML vengono usate le macro seguenti:</span><span class="sxs-lookup"><span data-stu-id="388c3-119">The following macros are used with XML nodes:</span></span>

-   [<span data-ttu-id="388c3-120">**\_valore del \_ dizionario delle stringhe WS XML \_ \_**</span><span class="sxs-lookup"><span data-stu-id="388c3-120">**WS\_XML\_STRING\_DICTIONARY\_VALUE**</span></span>](/windows/desktop/api/WebServices/nf-webservices-ws_xml_string_dictionary_value)
-   <span data-ttu-id="388c3-121">[**\_stringa WS \_ XML \_ null**](/previous-versions/windows/desktop/legacy/dd323562(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="388c3-121">[**WS\_XML\_STRING\_NULL**](/previous-versions/windows/desktop/legacy/dd323562(v=vs.85))</span></span>
-   [<span data-ttu-id="388c3-122">**\_ \_ valore stringa WS \_ XML**</span><span class="sxs-lookup"><span data-stu-id="388c3-122">**WS\_XML\_STRING\_VALUE**</span></span>](/windows/desktop/api/WebServices/nf-webservices-ws_xml_string_value)

<span data-ttu-id="388c3-123">Con i nodi XML vengono utilizzate le strutture seguenti:</span><span class="sxs-lookup"><span data-stu-id="388c3-123">The following structures are used with XML nodes:</span></span>

-   [<span data-ttu-id="388c3-124">**\_attributo WS XML \_**</span><span class="sxs-lookup"><span data-stu-id="388c3-124">**WS\_XML\_ATTRIBUTE**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_attribute)
-   [<span data-ttu-id="388c3-125">**\_ \_ Testo Base64 di WS XML \_**</span><span class="sxs-lookup"><span data-stu-id="388c3-125">**WS\_XML\_BASE64\_TEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_base64_text)
-   [<span data-ttu-id="388c3-126">**testo di WS \_ XML \_ bool \_**</span><span class="sxs-lookup"><span data-stu-id="388c3-126">**WS\_XML\_BOOL\_TEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_bool_text)
-   [<span data-ttu-id="388c3-127">**\_ \_ nodo commento WS \_ XML**</span><span class="sxs-lookup"><span data-stu-id="388c3-127">**WS\_XML\_COMMENT\_NODE**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_comment_node)
-   [<span data-ttu-id="388c3-128">**\_testo XML \_ DateTime \_ WS**</span><span class="sxs-lookup"><span data-stu-id="388c3-128">**WS\_XML\_DATETIME\_TEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_datetime_text)
-   [<span data-ttu-id="388c3-129">**\_ \_ testo decimale di WS XML \_**</span><span class="sxs-lookup"><span data-stu-id="388c3-129">**WS\_XML\_DECIMAL\_TEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_decimal_text)
-   [<span data-ttu-id="388c3-130">**\_dizionario XML \_ WS**</span><span class="sxs-lookup"><span data-stu-id="388c3-130">**WS\_XML\_DICTIONARY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_dictionary)
-   [<span data-ttu-id="388c3-131">**\_ \_ testo doppio di WS XML \_**</span><span class="sxs-lookup"><span data-stu-id="388c3-131">**WS\_XML\_DOUBLE\_TEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_double_text)
-   [<span data-ttu-id="388c3-132">**\_ \_ nodo elemento XML \_ WS**</span><span class="sxs-lookup"><span data-stu-id="388c3-132">**WS\_XML\_ELEMENT\_NODE**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_element_node)
-   [<span data-ttu-id="388c3-133">**\_ \_ testo float di WS XML \_**</span><span class="sxs-lookup"><span data-stu-id="388c3-133">**WS\_XML\_FLOAT\_TEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_float_text)
-   [<span data-ttu-id="388c3-134">**\_ \_ testo GUID WS \_ XML**</span><span class="sxs-lookup"><span data-stu-id="388c3-134">**WS\_XML\_GUID\_TEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_guid_text)
-   [<span data-ttu-id="388c3-135">**Testo di WS \_ XML \_ Int32 \_**</span><span class="sxs-lookup"><span data-stu-id="388c3-135">**WS\_XML\_INT32\_TEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_int32_text)
-   [<span data-ttu-id="388c3-136">**\_Testo WS XML \_ Int64 \_**</span><span class="sxs-lookup"><span data-stu-id="388c3-136">**WS\_XML\_INT64\_TEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_int64_text)
-   [<span data-ttu-id="388c3-137">**\_ \_ testo elenco WS \_ XML**</span><span class="sxs-lookup"><span data-stu-id="388c3-137">**WS\_XML\_LIST\_TEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_list_text)
-   [<span data-ttu-id="388c3-138">**\_nodo WS XML \_**</span><span class="sxs-lookup"><span data-stu-id="388c3-138">**WS\_XML\_NODE**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_node)
-   [<span data-ttu-id="388c3-139">**QName di WS \_ XML \_**</span><span class="sxs-lookup"><span data-stu-id="388c3-139">**WS\_XML\_QNAME**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_qname)
-   [<span data-ttu-id="388c3-140">**\_ \_ testo QName di WS XML \_**</span><span class="sxs-lookup"><span data-stu-id="388c3-140">**WS\_XML\_QNAME\_TEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_qname_text)
-   [<span data-ttu-id="388c3-141">**\_stringa WS XML \_**</span><span class="sxs-lookup"><span data-stu-id="388c3-141">**WS\_XML\_STRING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_string)
-   [<span data-ttu-id="388c3-142">**\_testo WS XML \_**</span><span class="sxs-lookup"><span data-stu-id="388c3-142">**WS\_XML\_TEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_text)
-   [<span data-ttu-id="388c3-143">**\_nodo di \_ testo WS XML \_**</span><span class="sxs-lookup"><span data-stu-id="388c3-143">**WS\_XML\_TEXT\_NODE**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_text_node)
-   [<span data-ttu-id="388c3-144">**testo di WS \_ XML \_ TIMESPAN \_**</span><span class="sxs-lookup"><span data-stu-id="388c3-144">**WS\_XML\_TIMESPAN\_TEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_timespan_text)
-   [<span data-ttu-id="388c3-145">**\_Testo WS XML \_ UInt64 \_**</span><span class="sxs-lookup"><span data-stu-id="388c3-145">**WS\_XML\_UINT64\_TEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_uint64_text)
-   [<span data-ttu-id="388c3-146">**\_ \_ \_ testo ID univoco WS \_ XML**</span><span class="sxs-lookup"><span data-stu-id="388c3-146">**WS\_XML\_UNIQUE\_ID\_TEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_unique_id_text)
-   [<span data-ttu-id="388c3-147">**\_ \_ Testo UTF16 WS \_ XML**</span><span class="sxs-lookup"><span data-stu-id="388c3-147">**WS\_XML\_UTF16\_TEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_utf16_text)
-   [<span data-ttu-id="388c3-148">**\_ \_ Testo UTF8 di WS XML \_**</span><span class="sxs-lookup"><span data-stu-id="388c3-148">**WS\_XML\_UTF8\_TEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_utf8_text)

 

 