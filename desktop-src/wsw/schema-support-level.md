---
title: Livello di supporto dello schema
description: Questa sezione illustra i dettagli relativi al livello di supporto dello schema.
ms.assetid: ca18306e-6d67-406d-9c42-4be159a0b81f
keywords:
- Servizi Web a livello di supporto dello schema per Windows
- WWSAPI
- Wws
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d6cae112e074d50b90425c1d8952f3b6c06463378d73767346742193b406d2b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119026284"
---
# <a name="schema-support-level"></a>Livello di supporto dello schema

Questa sezione illustra i dettagli relativi al livello di supporto dello schema.


Lo schema supporta direttamente gli elementi seguenti:

-   Sequenze di elementi.
-   Derivazione dei tipi di elemento.
-   Scelte semplici di elementi ,ovvero quelle che eseere mappate a un'unione con tag.
-   Tipi di base definiti dal formato binario XSD/.NET, inclusi gli intervalli (min/max).
-   Supporto semplice per qualsiasi elemento (nessuna restrizione sul tipo di elemento).
-   Elementi e attributi facoltativi con valori predefiniti.
-   Ripetizione di elementi con intervalli (min/max).
-   Elementi nillable.

Lo schema non supporta direttamente gli elementi seguenti (che implicano il comportamento di "fallback"):

-   Tipi di base definiti dall'utente.
-   Scelte più complesse.
-   Rifiuto di attributi sconosciuti.
-   Attributi sconosciuti di round trip.
-   Supporto più complesso per qualsiasi elemento.
-   Costrutto all.
-   Key/keyref.

Di seguito è riportata una suddivisione dettagliata del supporto dei diversi componenti dello schema. Viene confrontato con il contratto dati in WCF perché la somiglianza nella funzionalità. Verrà descritta la differenza.

In genere, per i comportamenti di fallback:

-   Gli attributi vengono sottoposti a fall backed in WS \_ STRING;
-   Il contenuto dell'elemento viene sottoposto a fall backed in WS \_ XML \_ BUFFER.
-   complexType viene sottoposto a fall backed in una struttura contenente un campo di WS \_ XML \_ BUFFER.
-   I tipi semplici vengono sottoposti a fall-backed in WS \_ STRING.

wsutil genera avvisi per i componenti dello schema che non sono attualmente completamente supportati. L'applicazione potrebbe dover eseguire una verifica aggiuntiva per questi componenti. Wsutil overtime può essere migliorato per gestire alcune delle funzionalità attualmente supportate in fase di esecuzione, ad esempio il supporto dei valori predefiniti. wsutil può anche essere migliorato insieme alla serializzazione per supportare altre funzionalità come abstract. Il numero di componenti dello schema non supportati può essere ridotto nel tempo.

## <a name="the-overall-schema-document"></a>Documento generale dello schema

Definizione globale che potrebbe influire sulle definizioni incorporate nello schema. Si tratta di attributi globali applicabili a tutte le definizioni nello schema.

<attributi xs:schema>

-   attributeFromDefault ignorato.
-   blockDefault Ignorato.
-   elementFormDefault ignorato. Questo è diverso da dataContract perché gli elementi non qualificati sono supportati in fase di esecuzione.
-   finalDefault Ignorato. Non è disponibile alcun supporto del linguaggio C per il concetto di finale.
-   ID ignorato.
-   targetNamespace Supportato e mappato allo spazio dei nomi del servizio.
-   version Ignorato.

<contenuto> xs:schema

-   include Supported; wsutil richiede che tutte le definizioni necessarie siano disponibili come file di input durante la fase di compilazione.
-   ridefinire Ignorato. wsutil non supporta questa operazione.
-   import Supportato; wsutil richiede che tutte le definizioni necessarie siano disponibili come file di input durante la fase di compilazione.
-   simpleType Supported: vedere la sezione relativa al tipo semplice riportata di seguito.
-   complexType Supportato: vedere la sezione 'complexType'
-   group Ignorato.
-   attributeGroup ignorato.
-   elemento supportato; esegue il mapping alle definizioni di elementi globali.
-   attributo Supportato; esegue il mapping alle definizioni di attributi globali.
-   notazione ignorata

## <a name="complex-type"></a>Tipo complesso

Il tipo complesso, rappresentato da <xs:complexType>, potrebbe essere restrizione di tipo semplice o di tipo complesso, estensione di tipo semplice, matrici o struttura. Si è notato che nell'estensione dei tipi semplici non esiste ereditarietà e non è supportato xsi:type.

<attributi xs:complexType>

-   abstract Genera un avviso sulla funzionalità non supportata, nessuna modifica alla generazione del codice.
-   block Genera un avviso relativo alla funzionalità non supportata, nessuna modifica alla generazione del codice.
-   final Genera un avviso sulla funzionalità non supportata, nessuna modifica alla generazione del codice.
-   ID ignorato.
-   mixed Genera un avviso sulla funzionalità non supportata, fallback alla struttura con WS \_ XML \_ BUFFER se true.
-   name Supportato e mappato al nome del tipo di struttura.

<xs:complexType> contenuto

Si tratta della definizione del tipo per la struttura . La restrizione complexContent non è supportata.

-   complexContent Supporta l'estensione di contenuto complessa. Mappe strutturare l'ereditarietà.
-   group Attualmente fallback alla struttura con il campo \_ WS XML \_ BUFFER. Può essere supportato in base alla particella sottostante.
-   scelta supportata come unione. Questa operazione non è supportata nel contratto dati.
-   sequenza supportata: esegue il mapping ai campi di una struttura
-   attributo supportato con un'eccezione di 'prohibited'. fallback alla struttura con WS \_ XML \_ BUFFER se 'prohibited'.
-   attributeGroup supportato: esegue il mapping alla sequenza di attributi
-   anyAttribute ignorato
-   AttributeGroupRef supportato: esegue il mapping alla sequenza di attributi.
-   GroupRef Attualmente fallback alla struttura con il campo \_ WS XML \_ BUFFER. Può essere supportato in base al gruppo sottostante.
-   Qualsiasi supportato, mappato a \_ BUFFER XML
-   (blank) supportato esegue il mapping alla descrizione dello struct vuota senza generare alcuno struct.

<xs:sequence> in un tipo complesso: contenuto

wsutil supporta solo la sequenza completa di minOccurs = 1 e maxOccurs = 1; in caso contrario, il tipo complesso è attualmente sottoposto a fall backed in WS \_ XML \_ BUFFER. Può essere supportato come matrice di strutture.

-   elemento supportato; ogni istanza viene mappata a un campo nella struttura .
-   Fallback del gruppo; complexType è il fallback a WS \_ XML \_ BUFFER.
-   Tutti i fallback; complexType è il fallback a WS \_ XML \_ BUFFER.
-   scelta supportata; eseguire il mapping al campo unione.
-   fallback della sequenza; complexType è il fallback a WS \_ XML \_ BUFFER.
-   qualsiasi supportato; di cui è stato eseguito il mapping a XML \_ BUFFER.
-   (vuoto) supportato; complexType può essere una struttura vuota se non sono presenti attributi.

## <a name="elements"></a>Elementi

<xs:element>possono verificarsi in tre contesti.

-   Può verificarsi all'interno di <xs:sequence>, descrivendo un campo di uno struct normale. In questo caso, l'attributo maxOccurs deve essere 1. Il campo è facoltativo se minOccurs è 0.
-   Può verificarsi all'interno di <xs:sequence> che descrive un campo di una matrice. In questo caso, l'attributo maxOccurs deve essere maggiore di 1 o 'unbounded'.
-   Può verificarsi all'interno di <xs:schema> come descrizione globale dell'elemento.

<xs:element> all'interno di un> xs:sequence <o <xs:choice> come campo in una struttura

-   ref Supportato; risolto per fare riferimento a un elemento globale.
-   name Supportato, esegue il mapping al nome del campo.
-   type Supported, esegue il mapping al tipo di campo. Per altre informazioni, vedere "Mapping dei tipi". Se non viene specificato (e l'elemento non contiene un tipo anonimo), viene presupposto xs:anyType.
-   block Genera un avviso relativo alla funzionalità non supportata, nessuna modifica alla generazione del codice.
-   default Genera avviso sulla funzionalità non supportata, nessuna modifica alla generazione del codice.
-   fixed Genera avviso sulla funzionalità non supportata, nessuna modifica alla generazione del codice.
-   form Ignorato. Il livello di serializzazione supporta moduli completi e non qualificati.
-   ID ignorato.
-   maxOccurs esegue il mapping a un singolo campo dati se è uguale a 1. viene mappato a un campo di matrice (elemento ripetuto) se maxOccurs è maggiore di 1.
-   minOccurs se 0, le opzioni del campo sono impostate su FIELD \_ OPTIONAL, se nillable non è impostato.
-   nillable Il campo è nillable. Per [altre informazioni,](serialization.md) vedere Serializzazione.

<xs:element> elemento globale: attributi

Gli attributi minOccurs e maxOccurs non sono validi come descrizione globale dell'elemento. L'applicazione può usare direttamente la descrizione dell'elemento generato nel livello di serializzazione o nei livelli del canale.

-   abstract Genera un avviso sulla funzionalità non supportata, nessuna modifica alla generazione del codice.
-   block Genera un avviso relativo alla funzionalità non supportata, nessuna modifica alla generazione del codice.
-   default Genera avviso sulla funzionalità non supportata, nessuna modifica alla generazione del codice.
-   final Genera un avviso sulla funzionalità non supportata, nessuna modifica alla generazione del codice.
-   fixed Genera avviso sulla funzionalità non supportata, nessuna modifica alla generazione del codice.
-   ID ignorato.
-   name Supported: esegue il mapping al nome della descrizione dell'elemento globale ed è la base per il tipo anonimo, se specificato.
-   Nillable Ignored-application deve chiamare con il flag di destra.
-   Fallback substitutionGroup alla struttura con WS \_ XML \_ BUFFER, se impostato. wsutil non supporta substitutionGroup.
-   type Supportato ed eseguire il mapping al tipo dell'elemento.

<xs:element> come elemento globale: contents

-   simpleType supportato; esegue il mapping alla definizione del tipo.
-   complexType supportato; esegue il mapping a un tipo complesso.
-   unique Genera avviso sulla funzionalità non supportata, nessuna modifica alla generazione del codice. wsutil non supporta i vincoli di elemento.
-   key Genera un avviso sulla funzionalità non supportata, nessuna modifica alla generazione del codice. wsutil non supporta i vincoli di elemento.
-   keyref Genera un avviso sulla funzionalità non supportata, nessuna modifica alla generazione del codice. wsutil non supporta i vincoli di elemento.
-   (vuoto) Supportato; L'elemento senza specifica del tipo viene considerato xs:anyType.

## <a name="simple-types"></a>Tipi semplici

<attributi xs:simpleType>

-   Final Genera avviso relativo alla funzionalità non supportata, nessuna modifica alla generazione del codice.
-   ID ignorato
-   Nome supportato, mappato al nome del tipo.

<xs:simpleType> contenuto

-   Restrizione supportata, esegue il mapping al tipo enum o all'intervallo. Vedere la sezione "restrizioni xs:simpleType".
-   Elenco Genera avviso sulla funzionalità non supportata, fallback a BUFFER \_ XML.
-   Union Genera un avviso relativo alla funzionalità non supportata, fallback a BUFFER \_ XML.

## <a name="simple-type-restriction"></a>Restrizione del tipo semplice

Alcuni facet sono consentiti nei tipi integrali e nei tipi di stringhe per consentire il supporto di intervalli ed enumerazioni.

supporto dell'enumerazione

<tipo xs:enumeration> tipo semplice per il tipo di base della stringa viene considerato come tipo enum. In questo caso, l'attributo Base DEVE essere di tipo stringa. In caso di enumerazione, tutti gli altri facet vengono ignorati.

intervallo per il supporto di tipi semplici

Alcuni facet sono supportati nei tipi semplici che supportano in modo efficace l'intervallo consentito per il tipo. Di seguito sono riportate le restrizioni per i tipi integrali e i tipi float/double. I tipi semplici con altri facet sono supportati nel tipo STRING WS \_

-   minExclusive Supported
-   minInclusive supportato
-   maxExclusive supportato
-   maxInclusive supportato
-   totalDigits Genera un avviso relativo alla funzionalità non supportata, nessuna modifica alla generazione del codice.
-   fractionDigits Genera un avviso sulla funzionalità non supportata, nessuna modifica alla generazione del codice.
-   length Genera un avviso sulla funzionalità non supportata, nessuna modifica alla generazione del codice.
-   minLength Genera un avviso relativo alla funzionalità non supportata, nessuna modifica alla generazione del codice.
-   maxLength Genera un avviso relativo alla funzionalità non supportata, nessuna modifica alla generazione del codice.
-   enumerazione Genera un avviso relativo alla funzionalità non supportata, nessuna modifica alla generazione del codice.
-   whiteSpace Genera un avviso relativo alla funzionalità non supportata, nessuna modifica alla generazione del codice.
-   pattern Genera un avviso sulla funzionalità non supportata, nessuna modifica alla generazione del codice.
-   (vuoto) Supportati.

minLength e maxLength per la stringa non sono attualmente supportati, ma è una funzionalità auspicabile da supportare.

## <a name="inheritance"></a>Ereditarietà

Wsutil supporta l'ereditarietà di tipi complessi, cio' una struttura può ereditare da un'altra struttura, analogamente all'ereditarietà dell'interfaccia in C++. Questa operazione viene eseguita tramite <xs:complexContentExtension>. <xs:simpleContentExtension> ma viene generato come struttura normale con tipo di base come primo campo anziché come ereditarietà del tipo.

## <a name="typeprimitive-mapping"></a>Mapping di tipi/primitivi

Gli identificatori devono essere normalizzati durante la conversione da NCNames in XML. Le stringhe sono nillable. I tipi puntatore sono nillable. I tipi integrali e float/double sono nillable e defaultValue è impostato su 0.

![Tabella che mostra il mapping tra i tipi XSD e i tipi di dati Sapphire.](images/schematypemap.png)

 

 




