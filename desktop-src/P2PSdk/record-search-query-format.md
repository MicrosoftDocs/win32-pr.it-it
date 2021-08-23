---
description: Una chiamata alla funzione PeerGroupSearchRecords richiede un parametro della stringa di query XML usato per determinare i criteri di base di una ricerca.
ms.assetid: 2c5ab425-6959-418a-8d9a-c8155257fc7e
title: Formato query di ricerca record
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23457cfde6955927b3efdcce5ae2dff94480c7cf56849b418547fe2503a36830
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119517961"
---
# <a name="record-search-query-format"></a>Formato query di ricerca record

Una chiamata alla funzione [**PeerGroupSearchRecords**](/windows/desktop/api/P2P/nf-p2p-peergroupsearchrecords) richiede un parametro della stringa di query XML usato per determinare i criteri di base di una ricerca. Usare lo schema seguente per formulare una stringa XML:

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

### <a name="elements-to-use-for-a-record-search"></a>Elementi da usare per una ricerca di record

L'elemento primario in una ricerca di record è **peersearch,** che contiene il Uniform Resource Identifier (URI) dello schema associato **nell'attributo xmlns.** Quando **peersearch** viene usato come elemento figlio, è possibile usare **la clausola** **e**, e **o come** elementi figlio.

-   **e** - **L'elemento e** esegue un'operazione AND logica su una o più clausole contenute tra i tag di apertura e di chiusura. Altri **tag** e **e o** possono essere elementi figlio e i risultati ricorsivi delle clausole figlio sono inclusi nell'operazione.

    Ad esempio, se si desidera ottenere un record che contiene un nome uguale a James Peters e un ultimo aggiornamento maggiore di 28/02/2003 o una data di creazione minore di 31/1/2003, utilizzare la stringa di query XML seguente:

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

-   **clause:** **l'elemento della** clausola specifica una regola comparativa di base che confronta il valore di un attributo record specifico con il valore contenuto tra i tag di apertura e chiusura. Il **confronto** tra **il tipo** e gli attributi **di** confronto indica l'operazione di confronto da eseguire. Ad esempio, una ricerca semplice che indica che tutti i record corrispondenti devono avere un valore **peercreatorid** uguale a James Peters viene visualizzato nella stringa di query XML come segue:

    ``` syntax
    <?xml version="1.0" encoding="utf-8" ?> 
    <peersearch xmlns:xs="https://www.w3.org/2001/XMLSchema">
       <clause attrib="peercreatorid" type="string" compare="equal">James Peters</clause>
    </peersearch>
    ```

    Gli **attributi di** tipo comune includono **int,** **string** e **date.** **L'attributo** date può essere uno dei formati di data standard descritti in [https://www.w3.org/TR/NOTE-datetime](https://www.w3.org/TR/NOTE-datetime) .

    I valori per **l'attributo di** confronto **sono uguali,** **notequal**, **less**, **greater**, **lessorequal** e **greaterorequal**.

<!-- -->

-   **oppure** - **L'elemento o** esegue un'operazione OR logica su una o più clausole contenute tra i tag di apertura e di chiusura. Altri **elementi** **o e** e possono essere elementi figlio e i risultati ricorsivi delle clausole figlio vengono inclusi nell'operazione. Ad esempio, se si desidera ottenere un record che contiene un nome uguale a James Peters o un ultimo aggiornamento compreso tra il 31/01/2003 e il 28/02/2003, usare la stringa di query XML seguente:

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

## <a name="more-information-about-a-record-search"></a>Altre informazioni su una ricerca di record

Il primo livello di nodi dopo **peersearch** può avere un solo elemento. Tuttavia, gli elementi figlio successivi di tale elemento possono avere molti elementi allo stesso livello.

La query di ricerca seguente non è corretta:

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

La query ha esito negativo perché vengono restituiti due valori per la corrispondenza senza essere risolti in un unico valore true/false, il che significa che una clausola è una query per il nome di un record uguale a James Peters e l'operazione AND corrisponde alle due clausole componente. Il risultato è due valori logici true/false contraddittori.

Per ottenere tutti i record che contengono un nome uguale a James Peters e un ultimo aggiornamento compreso tra il 31/01/2003 e il 28/02/2003, inserire la clausola e i tag e allo stesso livello tra l'apertura e la chiusura dei tag **e** .   L'esempio seguente illustra la query con esito positivo:

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

L'elenco seguente identifica altre informazioni specifiche che è necessario conoscere per scrivere una query corretta:

-   Non  è  possibile trovare i tag  e e o tra i tag della clausola di apertura e chiusura perché, in tale configurazione, vengono interpretati come parte del valore con cui trovare la corrispondenza, con il risultato di un errore o di una corrispondenza non riuscita.
-   Ogni coppia di **tag e** e **e o** di apertura e chiusura deve includere almeno uno o più nodi figlio.
-   In questo schema non è consentito un set di elementi pari a zero.

## <a name="record-attributes"></a>Attributi dei record

Utilizzando lo schema [dell'attributo record](record-attribute-schema.md), un utente può creare attributi di record specificati dall'attributo XML **attrib** in un elemento clausola. Gli attributi per un nuovo record vengono aggiunti impostando il membro **pszAttributes** di [**PEER \_ RECORD**](/windows/desktop/api/P2P/ns-p2p-peer_record) su una stringa XML usando il formato specificato nello schema.

L'infrastruttura peer riserva i nomi di attributo seguenti:

-   **peerlastmodifiedby**
-   **peercreatorid**
-   **peerlastmodificationtime**
-   **peerrecordid**
-   **peerrecordtype**
-   **peercreationtime**
-   **peerlastmodificationtime**

## <a name="special-characters"></a>Caratteri speciali

Alcuni caratteri possono essere usati per esprimere criteri di corrispondenza o per eseguire l'escape di altri caratteri speciali. Questi caratteri sono descritti nella tabella seguente. 

| Modello di caratteri | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                             |
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \*                | Carattere jolly. Quando questo carattere viene rilevato in un valore di clausola, corrisponde a 0-n caratteri di qualsiasi valore, inclusi spazi vuoti e caratteri non alfanumerici. Esempio:<br/> "<clause attrib="peercreatorid" type="string" compare="equal">James \* P</clause>"<br/> Questa clausola corrisponde a **tutti i valori peercreatorid** con il nome "James" e un cognome che inizia con "P".<br/> |
| \\\*              | Asterisco preceduto da un carattere di escape. Questa sequenza corrisponde a un carattere asterisco.                                                                                                                                                                                                                                                                                                                                                                       |
| ?                 | Carattere jolly a carattere singolo. Quando questo carattere viene rilevato in un valore di clausola, corrisponde a qualsiasi carattere singolo, inclusi gli spazi vuoti e i caratteri non alfanumerici. Per esempio:<br/> "<clause attrib="filename" type="string" compare="equal">data-0?.xml</clause>"<br/> Questa clausola corrisponde **ai valori** dei nomi file, ad esempio "data-01.xml" e "data-0B.xml".<br/>                              |
| \\?               | Punto interrogativo preceduto da un carattere di escape. Questa sequenza corrisponde a un carattere punto interrogativo.                                                                                                                                                                                                                                                                                                                                                              |
| \\\\              | Barra rovesciata preceduta da un carattere di escape. Questa sequenza corrisponde a un singolo carattere barra rovesciata.                                                                                                                                                                                                                                                                                                                                                               |



 

Se la sequenza di caratteri non è valida, la [**funzione PeerGroupSearchRecords**](/windows/desktop/api/P2P/nf-p2p-peergroupsearchrecords) restituisce l'errore **E \_ INVALIDARG**. Una sequenza non valida è una sequenza che contiene un carattere " " (barra rovesciata) non seguita immediatamente da un \\ \* carattere " " (asterisco), un "?" (punto interrogativo) o un altro \\ carattere " " (barra rovesciata).

 

 




