---
description: I record possono avere attributi specifici dell'applicazione che sono una sequenza di coppie nome/valore rappresentate come una stringa XML nel membro pszAttributes della \_ struttura del record peer.
ms.assetid: 2991af9b-da32-4915-b4d6-575e3faac04e
title: Schema attributo record
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eefa8c4c8b00b09e9c8cb988088af645e9f9c967
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316739"
---
# <a name="record-attribute-schema"></a>Schema attributo record

I record possono avere attributi specifici dell'applicazione che sono una sequenza di coppie nome/valore rappresentate come una stringa XML nel membro **pszAttributes** della struttura del [**\_ record peer**](/windows/desktop/api/P2P/ns-p2p-peer_record) . Gli attributi vengono usati per filtrare una ricerca di record avviata da chiamate a [**PeerGroupSearchRecords**](/windows/desktop/api/P2P/nf-p2p-peergroupsearchrecords), che accetta un filtro di ricerca XML specificato nel [formato di query di ricerca dei record](record-search-query-format.md) come parametro.

Un attributo di record può essere uno dei tre tipi seguenti:

-   **int** è un valore intero.
-   **date** è un valore DateTime rappresentato come uno dei formati standard descritti in [https://www.w3.org/TR/NOTE-datetime](https://www.w3.org/TR/NOTE-datetime) .
-   **String** è un valore stringa Unicode.

Nell'elenco seguente vengono identificati i nomi di attributo specifici che sono riservati dall'infrastruttura peer:

-   **peerlastmodifiedby**
-   **peercreatorid**
-   **peerlastmodificationtime**
-   **peerrecordid**
-   **peerrecordtype**
-   **peercreationtime**
-   **peerlastmodificationtime**

## <a name="example-of-defining-record-attributes"></a>Esempio di definizione degli attributi dei record

Nell'esempio di schema seguente viene illustrato come definire gli attributi di record:

``` syntax
<?xml version="1.0" encoding="utf-8" ?>
<xs:schema xmlns:xs="https://www.w3.org/2001/XMLSchema">
   <xs:simpleType name="alphanum">
       <xs:restriction base="xs:string">
          <xs:pattern value="\c+" />
       </xs:restriction>
   </xs:simpleType>
   <xs:complexType name="attributeType">
       <xs:simpleContent>
          <xs:extension base="xs:string">
                <xs:attribute name="name" type="alphanum" />
                <xs:attribute name="type">
                    <xs:simpleType>
                        <xs:restriction base="alphanum">
                           <xs:enumeration value="string"/>
                           <xs:enumeration value="date"/>
                           <xs:enumeration value="int"/>
                        </xs:restriction>
                    </xs:simpleType>
                </xs:attribute>
           </xs:extension>
       </xs:simpleContent>
    </xs:complexType>
    <xs:element name="attributes">
       <xs:complexType>
           <xs:sequence>
                <xs:element name="attribute" type="attributeType" minOccurs="0" maxOccurs="unbounded" />
           </xs:sequence>
       </xs:complexType>
    </xs:element>
</xs:schema>  
```

> [!Note]  
> I nomi di attributo devono essere sequenze di caratteri alfanumerici. I caratteri speciali come i trattini ("-") e i caratteri di sottolineatura (" \_ ") non sono consentiti in un nome di attributo.

 

Nell'esempio seguente di una sequenza di attributi XML sono contenuti gli attributi **AuthenticationType** e **AuthExpires** personalizzati visualizzati nel membro **pszAttributes** del [**\_ record peer**](/windows/desktop/api/P2P/ns-p2p-peer_record).

``` syntax
<attributes>
  <attribute name="AuthenticationType" type="string">Kerberos</attribute><attribute name="AuthExpires" type="date">2002-01-31</attribute>
<attributes>
```

 

 



