---
description: Una chiamata alla funzione PeerGroupSearchRecords richiede un parametro della stringa di query XML usato per determinare i criteri di base di una ricerca.
ms.assetid: 2c5ab425-6959-418a-8d9a-c8155257fc7e
title: Formato della query di ricerca record
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02b475c8a449e3bcd360df5757fef508b1a744d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883650"
---
# <a name="record-search-query-format"></a><span data-ttu-id="2ec6b-103">Formato della query di ricerca record</span><span class="sxs-lookup"><span data-stu-id="2ec6b-103">Record Search Query Format</span></span>

<span data-ttu-id="2ec6b-104">Una chiamata alla funzione [**PeerGroupSearchRecords**](/windows/desktop/api/P2P/nf-p2p-peergroupsearchrecords) richiede un parametro della stringa di query XML usato per determinare i criteri di base di una ricerca.</span><span class="sxs-lookup"><span data-stu-id="2ec6b-104">A call to the [**PeerGroupSearchRecords**](/windows/desktop/api/P2P/nf-p2p-peergroupsearchrecords) function requires an XML query string parameter that is used to determine the basic criteria of a search.</span></span> <span data-ttu-id="2ec6b-105">Per formulare una stringa XML, utilizzare lo schema seguente:</span><span class="sxs-lookup"><span data-stu-id="2ec6b-105">Use the following schema to formulate an XML string:</span></span>

``` syntax
<?xml version="1.0" encoding="utf-8" ?>
<xs:schema xmlns:xs="https://www.w3.org/2001/XMLSchema">

  <xs:simpleType name="alphanumType">
     <xs:restriction base="xs:string">
        <xs:pattern value="\c+"/>
     </xs:restriction>
  </xs:simpleType>

  <xs:complexType name="operatorType">
      <xs:choice maxOccurs="unbounded">
         <xs:element ref="and" />
         <xs:element ref="or" />
         <xs:element ref="clause" />
      </xs:choice>
  </xs:complexType>

  <xs:element name="and" type="operatorType"/>

  <xs:element name="or" type="operatorType"/>

  <xs:element name="clause">
      <xs:complexType>
          <xs:simpleContent>
              <xs:extension base="xs:string">
        <xs:attribute name="attrib" type="alphanumType" />
        <xs:attribute name="type">
                  <xs:simpleType>
                    <xs:restriction base="xs:string">
                      <xs:enumeration value="string"/>
                      <xs:enumeration value="date"/>
                      <xs:enumeration value="int"/>
                    </xs:restriction>
                  </xs:simpleType>
                </xs:attribute>
        <xs:attribute name="compare" default="equal">
                  <xs:simpleType>
                    <xs:restriction base="xs:string">
                      <xs:enumeration value="equal"/>
                      <xs:enumeration value="greater"/>
                      <xs:enumeration value="less"/>
                      <xs:enumeration value="notequal"/>
                      <xs:enumeration value="greaterorequal"/>
                      <xs:enumeration value="lessorequal"/>
                    </xs:restriction>
                  </xs:simpleType>
                </xs:attribute>
              </xs:extension>
          </xs:simpleContent>
      </xs:complexType>
  </xs:element>

  <xs:element name="peersearch">
      <xs:complexType>
          <xs:choice>
              <xs:element ref="clause" />
              <xs:element ref="and" />
              <xs:element ref="or" />
          </xs:choice>
      </xs:complexType>
  </xs:element>
</xs:schema> 
```

### <a name="elements-to-use-for-a-record-search"></a><span data-ttu-id="2ec6b-106">Elementi da usare per la ricerca di record</span><span class="sxs-lookup"><span data-stu-id="2ec6b-106">Elements to Use for a Record Search</span></span>

<span data-ttu-id="2ec6b-107">L'elemento primario in una ricerca di record è **peersearch**, che contiene il Uniform Resource Identifier (URI) dello schema associato nell'attributo **xmlns** .</span><span class="sxs-lookup"><span data-stu-id="2ec6b-107">The primary element in a record search is **peersearch**, which contains the Uniform Resource Identifier (URI) of the associated schema in the **xmlns** attribute.</span></span> <span data-ttu-id="2ec6b-108">Quando **peersearch** viene usato come elemento figlio, è possibile usare gli elementi **and**, **clause** e **or** come elementi figlio.</span><span class="sxs-lookup"><span data-stu-id="2ec6b-108">When **peersearch** is used as a child element, you can use **and**, **clause**, and **or** as child elements.</span></span>

-   <span data-ttu-id="2ec6b-109">**e** -l'elemento **and** esegue un'operazione and logica su una o più clausole contenute tra i tag di apertura e di chiusura.</span><span class="sxs-lookup"><span data-stu-id="2ec6b-109">**and** - The **and** element performs a logical AND operation on one or more clauses contained between the opening and closing tags.</span></span> <span data-ttu-id="2ec6b-110">Altri tag **and** e **or** possono essere elementi figlio e i risultati ricorsivi delle rispettive clausole figlio sono inclusi nell'operazione.</span><span class="sxs-lookup"><span data-stu-id="2ec6b-110">Other **and** and **or** tags can be children, and recursive results of their child clauses are included in the operation.</span></span>

    <span data-ttu-id="2ec6b-111">Se ad esempio si vuole ottenere un record contenente un nome uguale a James Peters e un ultimo aggiornamento maggiore di 2/28/2003 o una data di creazione minore di 1/31/2003, usare la stringa di query XML seguente:</span><span class="sxs-lookup"><span data-stu-id="2ec6b-111">For example, if you want to obtain a record that contains a name equal to James Peters, and a last update that is greater than 2/28/2003, or a creation date that is less than 1/31/2003, use the following XML query string:</span></span>

    ``` syntax
    <?xml version="1.0" encoding="utf-8" ?> 
    <peersearch xmlns:xs="https://www.w3.org/2001/XMLSchema">
       <and>
          <clause attrib="peercreatorid" type="string" compare="equal">James Peters</clause>
          <or>
             <clause attrib="peerlastmodificationtime" type="date" compare="greater">2003-01-31</clause>
             <clause attrib="peercreationtime" type="date" compare="less">2003-02-328</clause>
          </or>
       </and>
    </peersearch>
    ```

<!-- -->

-   <span data-ttu-id="2ec6b-112">**clausola** : l'elemento **clause** specifica una regola comparativa di base che confronta il valore di un attributo di record specifico con il valore contenuto tra i tag di apertura e di chiusura.</span><span class="sxs-lookup"><span data-stu-id="2ec6b-112">**clause** - The **clause** element specifies a basic comparative rule that compares the value of a specific record attribute with the value contained between the opening and closing tags.</span></span> <span data-ttu-id="2ec6b-113">Il **tipo** e gli attributi di **confronto** devono essere forniti **compare** indica l'operazione di confronto da eseguire.</span><span class="sxs-lookup"><span data-stu-id="2ec6b-113">The **type** and **compare** attributes must be provided **compare** indicates the comparison operation to be performed.</span></span> <span data-ttu-id="2ec6b-114">Ad esempio, una semplice ricerca che indica tutti i record corrispondenti deve avere un valore **peercreatorid** uguale a James Peters viene visualizzato nella stringa di query XML come riportato di seguito:</span><span class="sxs-lookup"><span data-stu-id="2ec6b-114">For example, a simple search that indicates all matched records must have a **peercreatorid** value equal to James Peters appears in the XML query string as the following:</span></span>

    ``` syntax
    <?xml version="1.0" encoding="utf-8" ?> 
    <peersearch xmlns:xs="https://www.w3.org/2001/XMLSchema">
       <clause attrib="peercreatorid" type="string" compare="equal">James Peters</clause>
    </peersearch>
    ```

    <span data-ttu-id="2ec6b-115">Gli attributi di **tipo** comuni includono **int**, **String** e **date**.</span><span class="sxs-lookup"><span data-stu-id="2ec6b-115">Common **type** attributes include **int**, **string**, and **date**.</span></span> <span data-ttu-id="2ec6b-116">L'attributo **date** può essere uno dei formati di data standard descritti in [https://www.w3.org/TR/NOTE-datetime](https://www.w3.org/TR/NOTE-datetime) .</span><span class="sxs-lookup"><span data-stu-id="2ec6b-116">The **date** attribute can be one of the standard date formats described at [https://www.w3.org/TR/NOTE-datetime](https://www.w3.org/TR/NOTE-datetime).</span></span>

    <span data-ttu-id="2ec6b-117">I valori per l'attributo **compare** sono **Equal**, **NotEqual**, **less**, **Greater**, **lessorequal** e **greaterorequal**.</span><span class="sxs-lookup"><span data-stu-id="2ec6b-117">Values for the **compare** attribute are **equal**, **notequal**, **less**, **greater**, **lessorequal**, and **greaterorequal**.</span></span>

<!-- -->

-   <span data-ttu-id="2ec6b-118">**o** -l'elemento **o** esegue un'operazione OR logica su una o più clausole contenute tra i tag di apertura e di chiusura.</span><span class="sxs-lookup"><span data-stu-id="2ec6b-118">**or** - The **or** element performs a logical OR operation on one or more clauses contained between the opening and closing tags.</span></span> <span data-ttu-id="2ec6b-119">Gli altri elementi **o** e **e** possono essere elementi figlio e i risultati ricorsivi delle clausole figlio sono inclusi nell'operazione.</span><span class="sxs-lookup"><span data-stu-id="2ec6b-119">Other **or** and **and** elements can be children, and recursive results of the child clauses are included in the operation.</span></span> <span data-ttu-id="2ec6b-120">Se ad esempio si vuole ottenere un record contenente un nome uguale a James Peters o un ultimo aggiornamento compreso tra 1/31/2003 e 2/28/2003, usare la stringa di query XML seguente:</span><span class="sxs-lookup"><span data-stu-id="2ec6b-120">For example, if you want to obtain a record that contains a name equal to James Peters, or a last update that is between 1/31/2003 and 2/28/2003, use the following XML query string:</span></span>

``` syntax
<?xml version="1.0" encoding="utf-8" ?> 
<peersearch xmlns:xs="https://www.w3.org/2001/XMLSchema">
   <or>
      <clause attrib="peercreatorid" type="string" compare="equal">James Peters</clause>
      <and>
         <clause attrib="peerlastmodificationtime" type="date" compare="greater">2003-01-31</clause>
         <clause attrib="peerlastmodificationtime" type="date" compare="less">2003-02-28</clause>
      </and>
   </or>
</peersearch>
```

## <a name="more-information-about-a-record-search"></a><span data-ttu-id="2ec6b-121">Altre informazioni sulla ricerca di record</span><span class="sxs-lookup"><span data-stu-id="2ec6b-121">More Information About a Record Search</span></span>

<span data-ttu-id="2ec6b-122">Il primo livello dei nodi dopo **peersearch** può avere un solo elemento.</span><span class="sxs-lookup"><span data-stu-id="2ec6b-122">The first level of nodes after **peersearch** can have only one element.</span></span> <span data-ttu-id="2ec6b-123">Tuttavia, i figli successivi di tale elemento possono avere molti elementi allo stesso livello.</span><span class="sxs-lookup"><span data-stu-id="2ec6b-123">However, subsequent children of that element can have many elements at the same level.</span></span>

<span data-ttu-id="2ec6b-124">La seguente query di ricerca non è corretta:</span><span class="sxs-lookup"><span data-stu-id="2ec6b-124">The following search query is incorrect:</span></span>

``` syntax
<?xml version="1.0" encoding="utf-8" ?> 
<peersearch xmlns:xs="https://www.w3.org/2001/XMLSchema">
   <clause attrib="peercreatorid" type="string" compare="equal">James Peters</clause>
   <and>
      <clause attrib="peerlastmodificationtime" type="date" compare="greater">2003-01-31</clause>
      <clause attrib="peerlastmodificationtime" type="date" compare="less">2003-02-28</clause>
   </and>
</peersearch>
```

<span data-ttu-id="2ec6b-125">La query ha esito negativo perché vengono restituiti due valori per la corrispondenza senza essere risolti in un valore true/false, il che significa che una clausola è una query per il nome di un record che equivale a James Peters e l'operazione AND corrisponde alle due clausole Component.</span><span class="sxs-lookup"><span data-stu-id="2ec6b-125">The query fails because two values are returned for the match without being resolved into one true/false value, which means that one clause is a query for the name of a record that equals James Peters, and the AND operation matches the two component clauses.</span></span> <span data-ttu-id="2ec6b-126">Il risultato è due valori true/false logici contradditori.</span><span class="sxs-lookup"><span data-stu-id="2ec6b-126">The result is two logical true/false values that are contradictory.</span></span>

<span data-ttu-id="2ec6b-127">Per ottenere tutti i record che contengono un nome uguale a James Peters e un ultimo aggiornamento compreso tra 1/31/2003 e 2/28/2003, inserire la **clausola** e i **tag che** si trovano allo stesso livello tra l'apertura e la chiusura **e** i tag.</span><span class="sxs-lookup"><span data-stu-id="2ec6b-127">To obtain all records that contain a name equal to James Peters, and a last update that is between 1/31/2003 and 2/28/2003, place the **clause** and **and** tags that are at the same level between opening and closing **and** tags.</span></span> <span data-ttu-id="2ec6b-128">Nell'esempio seguente viene illustrata la query riuscita:</span><span class="sxs-lookup"><span data-stu-id="2ec6b-128">The following example shows you the successful query:</span></span>

``` syntax
<?xml version="1.0" encoding="utf-8" ?> 
<peersearch xmlns:xs="https://www.w3.org/2001/XMLSchema">
    <and>
      <clause attrib="peercreatorid" type="string" compare="equal">James Peters</clause>
      <and>
         <clause attrib="peerlastmodificationtime" type="date" compare="greater">2003-01-31</clause>
         <clause attrib="peerlastmodificationtime" type="date" compare="less">2003-02-28</clause>
      </and>
   </and>
</peersearch>
```

<span data-ttu-id="2ec6b-129">Nell'elenco seguente sono riportate altre informazioni specifiche di cui è necessario essere a conoscenza per scrivere una query riuscita:</span><span class="sxs-lookup"><span data-stu-id="2ec6b-129">The following list identifies other specific information that you must know to write a successful query:</span></span>

-   <span data-ttu-id="2ec6b-130">Non è possibile trovare i tag **and** e **or** tra i tag delle **clausole** di apertura e chiusura perché, in tale configurazione, vengono interpretati come parte del valore di cui eseguire la corrispondenza, che genera un errore o una corrispondenza non riuscita.</span><span class="sxs-lookup"><span data-stu-id="2ec6b-130">The **and** and **or** tags cannot be located between opening and closing **clause** tags because, in that configuration, they are interpreted as part of the value to match against, which results in an error or a failed match.</span></span>
-   <span data-ttu-id="2ec6b-131">Ogni coppia di tag **and** e **or** di apertura e di chiusura deve includere almeno uno o più nodi figlio.</span><span class="sxs-lookup"><span data-stu-id="2ec6b-131">Each pair of **and** and **or** opening and closing tags must include at least one or more child nodes.</span></span>
-   <span data-ttu-id="2ec6b-132">Uno zero set di elementi non è consentito in questo schema.</span><span class="sxs-lookup"><span data-stu-id="2ec6b-132">A zero set of elements is not allowed in this schema.</span></span>

## <a name="record-attributes"></a><span data-ttu-id="2ec6b-133">Attributi di record</span><span class="sxs-lookup"><span data-stu-id="2ec6b-133">Record Attributes</span></span>

<span data-ttu-id="2ec6b-134">Utilizzando lo [schema dell'attributo record](record-attribute-schema.md), un utente può creare attributi di record specificati dall'attributo XML **attrib** in un elemento della clausola.</span><span class="sxs-lookup"><span data-stu-id="2ec6b-134">By using the [Record Attribute Schema](record-attribute-schema.md), a user can create record attributes that the **attrib** XML attribute in a clause element specifies.</span></span> <span data-ttu-id="2ec6b-135">Gli attributi per un nuovo record vengono aggiunti impostando il membro **pszAttributes** del [**\_ record peer**](/windows/desktop/api/P2P/ns-p2p-peer_record) su una stringa XML utilizzando il formato specificato nello schema.</span><span class="sxs-lookup"><span data-stu-id="2ec6b-135">Attributes for a new record are added by setting the **pszAttributes** member of [**PEER\_RECORD**](/windows/desktop/api/P2P/ns-p2p-peer_record) to an XML string using the format specified in the schema.</span></span>

<span data-ttu-id="2ec6b-136">L'infrastruttura peer riserva i nomi di attributo seguenti:</span><span class="sxs-lookup"><span data-stu-id="2ec6b-136">The Peer Infrastructure reserves the following attribute names:</span></span>

-   <span data-ttu-id="2ec6b-137">**peerlastmodifiedby**</span><span class="sxs-lookup"><span data-stu-id="2ec6b-137">**peerlastmodifiedby**</span></span>
-   <span data-ttu-id="2ec6b-138">**peercreatorid**</span><span class="sxs-lookup"><span data-stu-id="2ec6b-138">**peercreatorid**</span></span>
-   <span data-ttu-id="2ec6b-139">**peerlastmodificationtime**</span><span class="sxs-lookup"><span data-stu-id="2ec6b-139">**peerlastmodificationtime**</span></span>
-   <span data-ttu-id="2ec6b-140">**peerrecordid**</span><span class="sxs-lookup"><span data-stu-id="2ec6b-140">**peerrecordid**</span></span>
-   <span data-ttu-id="2ec6b-141">**peerrecordtype**</span><span class="sxs-lookup"><span data-stu-id="2ec6b-141">**peerrecordtype**</span></span>
-   <span data-ttu-id="2ec6b-142">**peercreationtime**</span><span class="sxs-lookup"><span data-stu-id="2ec6b-142">**peercreationtime**</span></span>
-   <span data-ttu-id="2ec6b-143">**peerlastmodificationtime**</span><span class="sxs-lookup"><span data-stu-id="2ec6b-143">**peerlastmodificationtime**</span></span>

## <a name="special-characters"></a><span data-ttu-id="2ec6b-144">Caratteri speciali</span><span class="sxs-lookup"><span data-stu-id="2ec6b-144">Special Characters</span></span>

<span data-ttu-id="2ec6b-145">Alcuni caratteri possono essere usati per esprimere i criteri di corrispondenza o per eseguire l'escape di altri caratteri speciali.</span><span class="sxs-lookup"><span data-stu-id="2ec6b-145">Certain characters can be used to express matching patterns, or to escape other special characters.</span></span> <span data-ttu-id="2ec6b-146">Questi caratteri sono descritti nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="2ec6b-146">These characters are described in the table below.</span></span> 

| <span data-ttu-id="2ec6b-147">Modello carattere</span><span class="sxs-lookup"><span data-stu-id="2ec6b-147">Character pattern</span></span> | <span data-ttu-id="2ec6b-148">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2ec6b-148">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                             |
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \*                | <span data-ttu-id="2ec6b-149">Carattere jolly.</span><span class="sxs-lookup"><span data-stu-id="2ec6b-149">The wildcard character.</span></span> <span data-ttu-id="2ec6b-150">Quando questo carattere viene rilevato in un valore della clausola, corrisponde a 0-n caratteri di qualsiasi valore, inclusi gli spazi vuoti e i caratteri non alfanumerici.</span><span class="sxs-lookup"><span data-stu-id="2ec6b-150">When this character is encountered in a clause value, it matches 0-n characters of any value, including whitespace and nonalphanumeric characters.</span></span> <span data-ttu-id="2ec6b-151">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="2ec6b-151">For example:</span></span><br/> <span data-ttu-id="2ec6b-152">"<clause attrib="peercreatorid" type="string" compare="equal">James P \* </clause>"</span><span class="sxs-lookup"><span data-stu-id="2ec6b-152">"<clause attrib="peercreatorid" type="string" compare="equal">James P\*</clause>"</span></span><br/> <span data-ttu-id="2ec6b-153">Questa clausola corrisponde a tutti i valori di **peercreatorid** con il nome "James" e il cognome che inizia con "P".</span><span class="sxs-lookup"><span data-stu-id="2ec6b-153">This clause matches all **peercreatorid** values with a first name of "James" and a last name starting with "P".</span></span><br/> |
| \\\*              | <span data-ttu-id="2ec6b-154">Un asterisco con escape.</span><span class="sxs-lookup"><span data-stu-id="2ec6b-154">An escaped asterisk.</span></span> <span data-ttu-id="2ec6b-155">Questa sequenza corrisponde a un carattere asterisco.</span><span class="sxs-lookup"><span data-stu-id="2ec6b-155">This sequence matches an asterisk character.</span></span>                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="2ec6b-156">?</span><span class="sxs-lookup"><span data-stu-id="2ec6b-156">?</span></span>                 | <span data-ttu-id="2ec6b-157">Carattere jolly a carattere singolo.</span><span class="sxs-lookup"><span data-stu-id="2ec6b-157">The single-character wildcard character.</span></span> <span data-ttu-id="2ec6b-158">Quando questo carattere viene rilevato in un valore della clausola, corrisponde a qualsiasi carattere singolo, inclusi gli spazi vuoti e i caratteri non alfanumerici. Per esempio:</span><span class="sxs-lookup"><span data-stu-id="2ec6b-158">When this character is encountered in a clause value, it matches any single character, including whitespace and nonalphanumeric characters.For example:</span></span><br/> <span data-ttu-id="2ec6b-159">"<clause attrib="filename" type="string" compare="equal">data-0?. XML</clause>"</span><span class="sxs-lookup"><span data-stu-id="2ec6b-159">"<clause attrib="filename" type="string" compare="equal">data-0?.xml</clause>"</span></span><br/> <span data-ttu-id="2ec6b-160">Questa clausola corrisponde ai valori del **nome file** , ad esempio "data-01.xml" e "data-0B.xml".</span><span class="sxs-lookup"><span data-stu-id="2ec6b-160">This clause matches **filename** values like "data-01.xml" and "data-0B.xml".</span></span><br/>                              |
| <span data-ttu-id="2ec6b-161">\\?</span><span class="sxs-lookup"><span data-stu-id="2ec6b-161">\\?</span></span>               | <span data-ttu-id="2ec6b-162">Punto interrogativo preceduto da un carattere di escape.</span><span class="sxs-lookup"><span data-stu-id="2ec6b-162">An escaped question mark.</span></span> <span data-ttu-id="2ec6b-163">Questa sequenza corrisponde a un carattere punto interrogativo.</span><span class="sxs-lookup"><span data-stu-id="2ec6b-163">This sequence matches a question mark character.</span></span>                                                                                                                                                                                                                                                                                                                                                              |
| \\\\              | <span data-ttu-id="2ec6b-164">Barra rovesciata di escape.</span><span class="sxs-lookup"><span data-stu-id="2ec6b-164">An escaped backslash.</span></span> <span data-ttu-id="2ec6b-165">Questa sequenza corrisponde a un singolo carattere barra rovesciata.</span><span class="sxs-lookup"><span data-stu-id="2ec6b-165">This sequence matches a single backslash character.</span></span>                                                                                                                                                                                                                                                                                                                                                               |



 

<span data-ttu-id="2ec6b-166">Se la sequenza di caratteri non è valida, la funzione [**PeerGroupSearchRecords**](/windows/desktop/api/P2P/nf-p2p-peergroupsearchrecords) restituisce l'errore **E \_ INVALIDARG**.</span><span class="sxs-lookup"><span data-stu-id="2ec6b-166">If the character sequence is not valid, the [**PeerGroupSearchRecords**](/windows/desktop/api/P2P/nf-p2p-peergroupsearchrecords) function returns the error **E\_INVALIDARG**.</span></span> <span data-ttu-id="2ec6b-167">Una sequenza non valida è una sequenza che contiene un \\ carattere "" (barra rovesciata) non immediatamente seguito da un \* carattere "" (asterisco), un "?" (punto interrogativo) o un altro \\ carattere "" (barra rovesciata).</span><span class="sxs-lookup"><span data-stu-id="2ec6b-167">An invalid sequence is any sequence that contains a "\\" (backslash) character not immediately followed by either an "\*" (asterisk) character, a "?" (question mark) character, or another "\\" (backslash) character.</span></span>

 

 




