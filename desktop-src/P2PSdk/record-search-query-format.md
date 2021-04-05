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
# <a name="record-search-query-format"></a>Formato della query di ricerca record

Una chiamata alla funzione [**PeerGroupSearchRecords**](/windows/desktop/api/P2P/nf-p2p-peergroupsearchrecords) richiede un parametro della stringa di query XML usato per determinare i criteri di base di una ricerca. Per formulare una stringa XML, utilizzare lo schema seguente:

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

### <a name="elements-to-use-for-a-record-search"></a>Elementi da usare per la ricerca di record

L'elemento primario in una ricerca di record è **peersearch**, che contiene il Uniform Resource Identifier (URI) dello schema associato nell'attributo **xmlns** . Quando **peersearch** viene usato come elemento figlio, è possibile usare gli elementi **and**, **clause** e **or** come elementi figlio.

-   **e** -l'elemento **and** esegue un'operazione and logica su una o più clausole contenute tra i tag di apertura e di chiusura. Altri tag **and** e **or** possono essere elementi figlio e i risultati ricorsivi delle rispettive clausole figlio sono inclusi nell'operazione.

    Se ad esempio si vuole ottenere un record contenente un nome uguale a James Peters e un ultimo aggiornamento maggiore di 2/28/2003 o una data di creazione minore di 1/31/2003, usare la stringa di query XML seguente:

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

-   **clausola** : l'elemento **clause** specifica una regola comparativa di base che confronta il valore di un attributo di record specifico con il valore contenuto tra i tag di apertura e di chiusura. Il **tipo** e gli attributi di **confronto** devono essere forniti **compare** indica l'operazione di confronto da eseguire. Ad esempio, una semplice ricerca che indica tutti i record corrispondenti deve avere un valore **peercreatorid** uguale a James Peters viene visualizzato nella stringa di query XML come riportato di seguito:

    ``` syntax
    <?xml version="1.0" encoding="utf-8" ?> 
    <peersearch xmlns:xs="https://www.w3.org/2001/XMLSchema">
       <clause attrib="peercreatorid" type="string" compare="equal">James Peters</clause>
    </peersearch>
    ```

    Gli attributi di **tipo** comuni includono **int**, **String** e **date**. L'attributo **date** può essere uno dei formati di data standard descritti in [https://www.w3.org/TR/NOTE-datetime](https://www.w3.org/TR/NOTE-datetime) .

    I valori per l'attributo **compare** sono **Equal**, **NotEqual**, **less**, **Greater**, **lessorequal** e **greaterorequal**.

<!-- -->

-   **o** -l'elemento **o** esegue un'operazione OR logica su una o più clausole contenute tra i tag di apertura e di chiusura. Gli altri elementi **o** e **e** possono essere elementi figlio e i risultati ricorsivi delle clausole figlio sono inclusi nell'operazione. Se ad esempio si vuole ottenere un record contenente un nome uguale a James Peters o un ultimo aggiornamento compreso tra 1/31/2003 e 2/28/2003, usare la stringa di query XML seguente:

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

## <a name="more-information-about-a-record-search"></a>Altre informazioni sulla ricerca di record

Il primo livello dei nodi dopo **peersearch** può avere un solo elemento. Tuttavia, i figli successivi di tale elemento possono avere molti elementi allo stesso livello.

La seguente query di ricerca non è corretta:

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

La query ha esito negativo perché vengono restituiti due valori per la corrispondenza senza essere risolti in un valore true/false, il che significa che una clausola è una query per il nome di un record che equivale a James Peters e l'operazione AND corrisponde alle due clausole Component. Il risultato è due valori true/false logici contradditori.

Per ottenere tutti i record che contengono un nome uguale a James Peters e un ultimo aggiornamento compreso tra 1/31/2003 e 2/28/2003, inserire la **clausola** e i **tag che** si trovano allo stesso livello tra l'apertura e la chiusura **e** i tag. Nell'esempio seguente viene illustrata la query riuscita:

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

Nell'elenco seguente sono riportate altre informazioni specifiche di cui è necessario essere a conoscenza per scrivere una query riuscita:

-   Non è possibile trovare i tag **and** e **or** tra i tag delle **clausole** di apertura e chiusura perché, in tale configurazione, vengono interpretati come parte del valore di cui eseguire la corrispondenza, che genera un errore o una corrispondenza non riuscita.
-   Ogni coppia di tag **and** e **or** di apertura e di chiusura deve includere almeno uno o più nodi figlio.
-   Uno zero set di elementi non è consentito in questo schema.

## <a name="record-attributes"></a>Attributi di record

Utilizzando lo [schema dell'attributo record](record-attribute-schema.md), un utente può creare attributi di record specificati dall'attributo XML **attrib** in un elemento della clausola. Gli attributi per un nuovo record vengono aggiunti impostando il membro **pszAttributes** del [**\_ record peer**](/windows/desktop/api/P2P/ns-p2p-peer_record) su una stringa XML utilizzando il formato specificato nello schema.

L'infrastruttura peer riserva i nomi di attributo seguenti:

-   **peerlastmodifiedby**
-   **peercreatorid**
-   **peerlastmodificationtime**
-   **peerrecordid**
-   **peerrecordtype**
-   **peercreationtime**
-   **peerlastmodificationtime**

## <a name="special-characters"></a>Caratteri speciali

Alcuni caratteri possono essere usati per esprimere i criteri di corrispondenza o per eseguire l'escape di altri caratteri speciali. Questi caratteri sono descritti nella tabella seguente. 

| Modello carattere | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                             |
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \*                | Carattere jolly. Quando questo carattere viene rilevato in un valore della clausola, corrisponde a 0-n caratteri di qualsiasi valore, inclusi gli spazi vuoti e i caratteri non alfanumerici. Ad esempio:<br/> "<clause attrib="peercreatorid" type="string" compare="equal">James P \* </clause>"<br/> Questa clausola corrisponde a tutti i valori di **peercreatorid** con il nome "James" e il cognome che inizia con "P".<br/> |
| \\\*              | Un asterisco con escape. Questa sequenza corrisponde a un carattere asterisco.                                                                                                                                                                                                                                                                                                                                                                       |
| ?                 | Carattere jolly a carattere singolo. Quando questo carattere viene rilevato in un valore della clausola, corrisponde a qualsiasi carattere singolo, inclusi gli spazi vuoti e i caratteri non alfanumerici. Per esempio:<br/> "<clause attrib="filename" type="string" compare="equal">data-0?. XML</clause>"<br/> Questa clausola corrisponde ai valori del **nome file** , ad esempio "data-01.xml" e "data-0B.xml".<br/>                              |
| \\?               | Punto interrogativo preceduto da un carattere di escape. Questa sequenza corrisponde a un carattere punto interrogativo.                                                                                                                                                                                                                                                                                                                                                              |
| \\\\              | Barra rovesciata di escape. Questa sequenza corrisponde a un singolo carattere barra rovesciata.                                                                                                                                                                                                                                                                                                                                                               |



 

Se la sequenza di caratteri non è valida, la funzione [**PeerGroupSearchRecords**](/windows/desktop/api/P2P/nf-p2p-peergroupsearchrecords) restituisce l'errore **E \_ INVALIDARG**. Una sequenza non valida è una sequenza che contiene un \\ carattere "" (barra rovesciata) non immediatamente seguito da un \* carattere "" (asterisco), un "?" (punto interrogativo) o un altro \\ carattere "" (barra rovesciata).

 

 




