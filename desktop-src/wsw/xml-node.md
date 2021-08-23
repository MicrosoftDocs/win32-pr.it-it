---
title: Nodo XML
description: Un nodo XML rappresenta una singola parte di codice XML, ad esempio un elemento iniziale e i relativi attributi, un elemento finale, un testo o \ 0034;tipi di dati \ 0034; contenuto di testo, ad esempio un numero intero o una matrice di byte. I dati in un nodo variano in base al tipo di \_ nodo WS \_ \_ XML.
ms.assetid: c514c542-029b-46d1-a796-1f132a41b2ad
keywords:
- Servizi Web del nodo XML per Windows
- WWSAPI
- Wws
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2b851ad0ab0a6a333fedea13036eebf11e8c727a04603c07d8f7e68e66de5ae
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119545651"
---
# <a name="xml-node"></a>Nodo XML

Un nodo XML rappresenta una singola parte di codice XML, ad esempio un elemento iniziale e i relativi attributi, un elemento finale, un testo o contenuto di testo "tipiato", ad esempio un numero intero o una matrice di byte. I dati in un nodo variano in base a [**WS \_ XML NODE \_ \_ TYPE**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_node_type).


Di seguito è riportato un esempio di documento XML specifico di codifica rappresentato con strutture indipendenti dalla codifica.

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

Con i nodi XML vengono usate le enumerazioni seguenti:

-   [**TIPO DI \_ VALORE \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_value_type)
-   [**TIPO DI \_ NODO WS XML \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_node_type)
-   [**TIPO DI \_ TESTO XML \_ \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_text_type)

Con i nodi XML vengono usate le funzioni seguenti:

-   [**WsTrimXmlWhitespace**](/windows/desktop/api/WebServices/nf-webservices-wstrimxmlwhitespace)
-   [**WsVerifyXmlNCName**](/windows/desktop/api/WebServices/nf-webservices-wsverifyxmlncname)
-   [**WsXmlStringEquals**](/windows/desktop/api/WebServices/nf-webservices-wsxmlstringequals)

Con i nodi XML vengono usate le macro seguenti:

-   [**VALORE WS \_ XML \_ STRING \_ \_ DICTIONARY**](/windows/desktop/api/WebServices/nf-webservices-ws_xml_string_dictionary_value)
-   [**WS \_ XML \_ STRING \_ NULL**](/previous-versions/windows/desktop/legacy/dd323562(v=vs.85))
-   [**VALORE STRINGA XML WS \_ \_ \_**](/windows/desktop/api/WebServices/nf-webservices-ws_xml_string_value)

Con i nodi XML vengono utilizzate le strutture seguenti:

-   [**ATTRIBUTO \_ XML WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_attribute)
-   [**WS \_ XML \_ BASE64 \_ TEXT**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_base64_text)
-   [**WS \_ XML \_ BOOL \_ TEXT**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_bool_text)
-   [**NODO WS \_ XML \_ COMMENT \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_comment_node)
-   [**WS \_ XML \_ DATETIME \_ TEXT**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_datetime_text)
-   [**WS \_ XML \_ DECIMAL \_ TEXT**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_decimal_text)
-   [**WS \_ XML \_ DICTIONARY**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_dictionary)
-   [**WS \_ XML \_ DOUBLE \_ TEXT**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_double_text)
-   [**NODO ELEMENTO XML WS \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_element_node)
-   [**WS \_ XML \_ FLOAT \_ TEXT**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_float_text)
-   [**TESTO GUID XML WS \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_guid_text)
-   [**WS \_ XML \_ INT32 \_ TEXT**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_int32_text)
-   [**WS \_ XML \_ INT64 \_ TEXT**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_int64_text)
-   [**WS \_ XML \_ LIST \_ TEXT**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_list_text)
-   [**NODO XML WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_node)
-   [**WS \_ XML \_ QNAME**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_qname)
-   [**WS \_ XML \_ QNAME \_ TEXT**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_qname_text)
-   [**WS \_ XML \_ STRING**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_string)
-   [**WS \_ XML \_ TEXT**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_text)
-   [**NODO DI TESTO XML WS \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_text_node)
-   [**WS \_ XML \_ TIMESPAN \_ TEXT**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_timespan_text)
-   [**WS \_ XML \_ UINT64 \_ TEXT**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_uint64_text)
-   [**WS \_ XML \_ UNIQUE \_ ID \_ TEXT**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_unique_id_text)
-   [**WS \_ XML \_ UTF16 \_ TEXT**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_utf16_text)
-   [**WS \_ XML \_ UTF8 \_ TEXT**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_utf8_text)

 

 