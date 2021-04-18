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
# <a name="record-attribute-schema"></a><span data-ttu-id="84914-103">Schema attributo record</span><span class="sxs-lookup"><span data-stu-id="84914-103">Record Attribute Schema</span></span>

<span data-ttu-id="84914-104">I record possono avere attributi specifici dell'applicazione che sono una sequenza di coppie nome/valore rappresentate come una stringa XML nel membro **pszAttributes** della struttura del [**\_ record peer**](/windows/desktop/api/P2P/ns-p2p-peer_record) .</span><span class="sxs-lookup"><span data-stu-id="84914-104">Records can have application-specific attributes that are a sequence of name or value pairs represented as an XML string in the **pszAttributes** member of the [**PEER\_RECORD**](/windows/desktop/api/P2P/ns-p2p-peer_record) structure.</span></span> <span data-ttu-id="84914-105">Gli attributi vengono usati per filtrare una ricerca di record avviata da chiamate a [**PeerGroupSearchRecords**](/windows/desktop/api/P2P/nf-p2p-peergroupsearchrecords), che accetta un filtro di ricerca XML specificato nel [formato di query di ricerca dei record](record-search-query-format.md) come parametro.</span><span class="sxs-lookup"><span data-stu-id="84914-105">The attributes are used to filter a record search initiated by calls to [**PeerGroupSearchRecords**](/windows/desktop/api/P2P/nf-p2p-peergroupsearchrecords), which takes an XML search filter specified in [Record Search Query Format](record-search-query-format.md) as a parameter.</span></span>

<span data-ttu-id="84914-106">Un attributo di record può essere uno dei tre tipi seguenti:</span><span class="sxs-lookup"><span data-stu-id="84914-106">A record attribute can be one of the following three types:</span></span>

-   <span data-ttu-id="84914-107">**int** è un valore intero.</span><span class="sxs-lookup"><span data-stu-id="84914-107">**int** is an integer value.</span></span>
-   <span data-ttu-id="84914-108">**date** è un valore DateTime rappresentato come uno dei formati standard descritti in [https://www.w3.org/TR/NOTE-datetime](https://www.w3.org/TR/NOTE-datetime) .</span><span class="sxs-lookup"><span data-stu-id="84914-108">**date** is a datetime value represented as one of the standard formats described at [https://www.w3.org/TR/NOTE-datetime](https://www.w3.org/TR/NOTE-datetime).</span></span>
-   <span data-ttu-id="84914-109">**String** è un valore stringa Unicode.</span><span class="sxs-lookup"><span data-stu-id="84914-109">**string** is a Unicode string value.</span></span>

<span data-ttu-id="84914-110">Nell'elenco seguente vengono identificati i nomi di attributo specifici che sono riservati dall'infrastruttura peer:</span><span class="sxs-lookup"><span data-stu-id="84914-110">The following list identifies the specific attribute names that are reserved by the Peer Infrastructure:</span></span>

-   <span data-ttu-id="84914-111">**peerlastmodifiedby**</span><span class="sxs-lookup"><span data-stu-id="84914-111">**peerlastmodifiedby**</span></span>
-   <span data-ttu-id="84914-112">**peercreatorid**</span><span class="sxs-lookup"><span data-stu-id="84914-112">**peercreatorid**</span></span>
-   <span data-ttu-id="84914-113">**peerlastmodificationtime**</span><span class="sxs-lookup"><span data-stu-id="84914-113">**peerlastmodificationtime**</span></span>
-   <span data-ttu-id="84914-114">**peerrecordid**</span><span class="sxs-lookup"><span data-stu-id="84914-114">**peerrecordid**</span></span>
-   <span data-ttu-id="84914-115">**peerrecordtype**</span><span class="sxs-lookup"><span data-stu-id="84914-115">**peerrecordtype**</span></span>
-   <span data-ttu-id="84914-116">**peercreationtime**</span><span class="sxs-lookup"><span data-stu-id="84914-116">**peercreationtime**</span></span>
-   <span data-ttu-id="84914-117">**peerlastmodificationtime**</span><span class="sxs-lookup"><span data-stu-id="84914-117">**peerlastmodificationtime**</span></span>

## <a name="example-of-defining-record-attributes"></a><span data-ttu-id="84914-118">Esempio di definizione degli attributi dei record</span><span class="sxs-lookup"><span data-stu-id="84914-118">Example of Defining Record Attributes</span></span>

<span data-ttu-id="84914-119">Nell'esempio di schema seguente viene illustrato come definire gli attributi di record:</span><span class="sxs-lookup"><span data-stu-id="84914-119">The following schema example shows you how to define record attributes:</span></span>

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
> <span data-ttu-id="84914-120">I nomi di attributo devono essere sequenze di caratteri alfanumerici.</span><span class="sxs-lookup"><span data-stu-id="84914-120">Attribute names must be sequences of alphanumeric characters.</span></span> <span data-ttu-id="84914-121">I caratteri speciali come i trattini ("-") e i caratteri di sottolineatura (" \_ ") non sono consentiti in un nome di attributo.</span><span class="sxs-lookup"><span data-stu-id="84914-121">Special characters like hyphens ("-") and underscores ("\_") are not allowed in an attribute name.</span></span>

 

<span data-ttu-id="84914-122">Nell'esempio seguente di una sequenza di attributi XML sono contenuti gli attributi **AuthenticationType** e **AuthExpires** personalizzati visualizzati nel membro **pszAttributes** del [**\_ record peer**](/windows/desktop/api/P2P/ns-p2p-peer_record).</span><span class="sxs-lookup"><span data-stu-id="84914-122">The following example of an XML attribute sequence contains the custom **AuthenticationType** and **AuthExpires** attributes that appear in the **pszAttributes** member of [**PEER\_RECORD**](/windows/desktop/api/P2P/ns-p2p-peer_record).</span></span>

``` syntax
<attributes>
  <attribute name="AuthenticationType" type="string">Kerberos</attribute><attribute name="AuthExpires" type="date">2002-01-31</attribute>
<attributes>
```

 

 



