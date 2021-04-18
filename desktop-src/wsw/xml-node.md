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
# <a name="xml-node"></a>Nodo XML

Un nodo XML rappresenta una singola porzione di codice XML, ad esempio un elemento iniziale e i relativi attributi, un elemento finale, un testo o un contenuto di testo tipizzato, ad esempio una matrice di byte o un numero intero. I dati in un nodo variano in base al [**\_ tipo di \_ nodo \_ WS XML**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_node_type).


Di seguito viene illustrato un esempio di un documento XML specifico di codifica rappresentato con strutture indipendenti di codifica.

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

Con i nodi XML vengono utilizzate le enumerazioni seguenti:

-   [**\_tipo di valore WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_value_type)
-   [**\_tipo di \_ nodo WS XML \_**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_node_type)
-   [**\_tipo di \_ testo WS XML \_**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_text_type)

Con i nodi XML vengono usate le funzioni seguenti:

-   [**WsTrimXmlWhitespace**](/windows/desktop/api/WebServices/nf-webservices-wstrimxmlwhitespace)
-   [**WsVerifyXmlNCName**](/windows/desktop/api/WebServices/nf-webservices-wsverifyxmlncname)
-   [**WsXmlStringEquals**](/windows/desktop/api/WebServices/nf-webservices-wsxmlstringequals)

Con i nodi XML vengono usate le macro seguenti:

-   [**\_valore del \_ dizionario delle stringhe WS XML \_ \_**](/windows/desktop/api/WebServices/nf-webservices-ws_xml_string_dictionary_value)
-   [**\_stringa WS \_ XML \_ null**](/previous-versions/windows/desktop/legacy/dd323562(v=vs.85))
-   [**\_ \_ valore stringa WS \_ XML**](/windows/desktop/api/WebServices/nf-webservices-ws_xml_string_value)

Con i nodi XML vengono utilizzate le strutture seguenti:

-   [**\_attributo WS XML \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_attribute)
-   [**\_ \_ Testo Base64 di WS XML \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_base64_text)
-   [**testo di WS \_ XML \_ bool \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_bool_text)
-   [**\_ \_ nodo commento WS \_ XML**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_comment_node)
-   [**\_testo XML \_ DateTime \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_datetime_text)
-   [**\_ \_ testo decimale di WS XML \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_decimal_text)
-   [**\_dizionario XML \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_dictionary)
-   [**\_ \_ testo doppio di WS XML \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_double_text)
-   [**\_ \_ nodo elemento XML \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_element_node)
-   [**\_ \_ testo float di WS XML \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_float_text)
-   [**\_ \_ testo GUID WS \_ XML**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_guid_text)
-   [**Testo di WS \_ XML \_ Int32 \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_int32_text)
-   [**\_Testo WS XML \_ Int64 \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_int64_text)
-   [**\_ \_ testo elenco WS \_ XML**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_list_text)
-   [**\_nodo WS XML \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_node)
-   [**QName di WS \_ XML \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_qname)
-   [**\_ \_ testo QName di WS XML \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_qname_text)
-   [**\_stringa WS XML \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_string)
-   [**\_testo WS XML \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_text)
-   [**\_nodo di \_ testo WS XML \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_text_node)
-   [**testo di WS \_ XML \_ TIMESPAN \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_timespan_text)
-   [**\_Testo WS XML \_ UInt64 \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_uint64_text)
-   [**\_ \_ \_ testo ID univoco WS \_ XML**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_unique_id_text)
-   [**\_ \_ Testo UTF16 WS \_ XML**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_utf16_text)
-   [**\_ \_ Testo UTF8 di WS XML \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_utf8_text)

 

 