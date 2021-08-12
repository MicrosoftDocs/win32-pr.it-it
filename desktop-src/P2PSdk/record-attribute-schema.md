---
description: I record possono avere attributi specifici dell'applicazione che sono una sequenza di coppie nome/valore rappresentate come stringa XML nel membro pszAttributes della struttura PEER \_ RECORD.
ms.assetid: 2991af9b-da32-4915-b4d6-575e3faac04e
title: Registrare lo schema dell'attributo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3597369d7214b51b94a74b777315bb2ce2beb280232be5fb29571376ad3fc93e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118612312"
---
# <a name="record-attribute-schema"></a>Registrare lo schema dell'attributo

I record possono avere attributi specifici dell'applicazione che sono una sequenza di coppie nome/valore rappresentate come stringa XML nel membro **pszAttributes** della struttura [**PEER \_ RECORD.**](/windows/desktop/api/P2P/ns-p2p-peer_record) Gli attributi vengono usati per filtrare una ricerca di record avviata dalle chiamate a [**PeerGroupSearchRecords**](/windows/desktop/api/P2P/nf-p2p-peergroupsearchrecords), che accetta un filtro di ricerca XML specificato in [Formato](record-search-query-format.md) query di ricerca record come parametro.

Un attributo record può essere uno dei tre tipi seguenti:

-   **int** è un valore intero.
-   **date** è un valore datetime rappresentato come uno dei formati standard descritti in [https://www.w3.org/TR/NOTE-datetime](https://www.w3.org/TR/NOTE-datetime) .
-   **string** è un valore stringa Unicode.

L'elenco seguente identifica i nomi di attributo specifici riservati dall'infrastruttura peer:

-   **peerlastmodifiedby**
-   **peercreatorid**
-   **peerlastmodificationtime**
-   **peerrecordid**
-   **peerrecordtype**
-   **peercreationtime**
-   **peerlastmodificationtime**

## <a name="example-of-defining-record-attributes"></a>Esempio di definizione degli attributi dei record

L'esempio di schema seguente illustra come definire gli attributi dei record:

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
> I nomi degli attributi devono essere sequenze di caratteri alfanumerici. I caratteri speciali come trattini ("-") e caratteri di sottolineatura (" \_ ") non sono consentiti in un nome di attributo.

 

L'esempio seguente di una sequenza di attributi XML contiene gli attributi **AuthenticationType** e **AuthExpires** personalizzati visualizzati nel membro **pszAttributes** di [**PEER \_ RECORD**](/windows/desktop/api/P2P/ns-p2p-peer_record).

``` syntax
<attributes>
  <attribute name="AuthenticationType" type="string">Kerberos</attribute><attribute name="AuthExpires" type="date">2002-01-31</attribute>
<attributes>
```

 

 



