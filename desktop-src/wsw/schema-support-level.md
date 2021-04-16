---
title: Livello di supporto dello schema
description: In questa sezione vengono illustrati i dettagli relativi al livello di supporto dello schema.
ms.assetid: ca18306e-6d67-406d-9c42-4be159a0b81f
keywords:
- Servizi Web a livello di supporto dello schema per Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5aa50eef8835f643abb668b439160ea733bf5160
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/12/2021
ms.locfileid: "104571266"
---
# <a name="schema-support-level"></a>Livello di supporto dello schema

In questa sezione vengono illustrati i dettagli relativi al livello di supporto dello schema.


Lo schema supporta direttamente gli elementi seguenti:

-   Sequenze di elementi.
-   Derivazione di tipi di elemento.
-   Scelte semplici di elementi (quelli che vengono mappati a un'Unione con tag).
-   Tipi di base definiti dal formato binario XSD/.NET, inclusi gli intervalli (min/max).
-   Supporto semplice per qualsiasi elemento (nessuna restrizione sul tipo di elemento).
-   Elementi e attributi facoltativi con valori predefiniti.
-   Ripetizione di elementi con intervalli (min/max).
-   Elementi nillable.

Lo schema non supporta direttamente le operazioni seguenti, che implicano il comportamento di fallback:

-   Tipi di base definiti dall'utente.
-   Scelte più complesse.
-   Rifiuto degli attributi sconosciuti.
-   Arrotondamento degli attributi sconosciuti.
-   Supporto più complesso per qualsiasi elemento.
-   Costrutto all.
-   Chiave/keyref.

Di seguito è riportata una suddivisione dettagliata del supporto dei diversi componenti dello schema. Viene confrontato con il contratto dati in WCF perché la somiglianza della funzionalità. La differenza verrà descritta.

In genere, per i comportamenti di fallback:

-   viene eseguito il fallback degli attributi a WS \_ String;
-   viene eseguito il fallback del contenuto dell'elemento \_ nel \_ buffer WS XML.
-   viene eseguito il fallback di complexType alla struttura contenente un campo del \_ buffer WS XML \_ .
-   Per i tipi semplici viene eseguito il fallback a WS \_ String.

wsutil genera avvisi per i componenti dello schema che attualmente non sono completamente supportati. È necessario che l'applicazione esegua una verifica aggiuntiva per questi componenti. È possibile migliorare il WSUTIL di lavoro straordinario per gestire alcune delle funzionalità attualmente supportate in fase di esecuzione, ad esempio il supporto dei valori predefiniti. wsutil può anche essere migliorato insieme alla serializzazione per supportare altre funzionalità, ad esempio abstract. Il numero di componenti dello schema non supportati può essere ridotto nel tempo.

## <a name="the-overall-schema-document"></a>Documento dello schema generale

Definizione globale che può influire sulle definizioni incorporate nello schema. Si tratta di attributi globali applicabili a tutte le definizioni nello schema.

<XS: Schema> attributi

-   attributeFromDefault ignorato.
-   blockDefault ignorato.
-   elementFormDefault ignorato. Questa operazione è diversa rispetto a DataContract perché gli elementi non qualificati sono supportati in fase di esecuzione.
-   finalDefault ignorato. Non è disponibile alcun supporto per il linguaggio C per il concetto di Final.
-   ID ignorato.
-   targetNamespace supportato e mappato allo spazio dei nomi del servizio.
-   versione ignorata.

<XS: contenuto del> dello schema

-   includere supportato; wsutil richiede che tutte le definizioni necessarie siano disponibili come file di input in fase di compilazione.
-   ridefinizione ignorata. wsutil non supporta questa operazione.
-   importazione supportata. wsutil richiede che tutte le definizioni necessarie siano disponibili come file di input in fase di compilazione.
-   simpleType supportato. vedere la sezione di tipo semplice riportata di seguito.
-   complexType supportato: vedere la sezione ' complexType '
-   gruppo ignorato.
-   attributeGroup ignorato.
-   elemento supportato; esegue il mapping a definizioni di elementi globali.
-   attributo supportato; esegue il mapping alle definizioni degli attributi globali.
-   notazione ignorata

## <a name="complex-type"></a>Tipo complesso

Il tipo complesso, rappresentato da <XS: complexType>, potrebbe essere una restrizione di tipo semplice o complesso, estensione di tipo semplice, matrici o struttura. Si è notato che nell'estensione di tipi semplici non sono presenti ereditarietà né supporto xsi: Type.

<XS: complexType> attributi

-   abstract genera avviso sulla funzionalità non supportata, nessuna modifica alla generazione del codice.
-   blocca genera avviso per la funzionalità non supportata, nessuna modifica alla generazione del codice.
-   Genera avviso finale per la funzionalità non supportata, nessuna modifica alla generazione del codice.
-   ID ignorato.
-   Genera un avviso misto per la funzionalità non supportata, il fallback alla struttura con il \_ buffer WS XML \_ Se true.
-   nome supportato e mappato al nome del tipo di struttura.

<XS: complexType> contenuto

Si tratta della definizione di tipo per la struttura. la restrizione complexContent non è supportata.

-   complexContent supporta l'estensione di contenuto complesso. Esegue il mapping all'ereditarietà della struttura.
-   raggruppa attualmente il fallback alla struttura con \_ il \_ campo del buffer WS XML. Può essere supportato in base alla particella sottostante.
-   scelta supportata come Unione. Questa operazione non è supportata nel contratto dati.
-   sequenza supportata: esegue il mapping ai campi di una struttura
-   l'attributo è supportato con un'eccezione di ' proibito '. fallback alla struttura con il \_ buffer WS XML \_ se è vietato.
-   supportato da attributeGroup: esegue il mapping a una sequenza di attributi
-   anyAttribute ignorato
-   AttributeGroupRef supportato: esegue il mapping a una sequenza di attributi.
-   GroupRef attualmente il fallback alla struttura con \_ il \_ campo del buffer WS XML. Può essere supportato in base al gruppo sottostante.
-   Qualsiasi supportato, esegue il mapping al \_ buffer XML
-   (blank) il mapping supportato alla descrizione di struct vuota senza struct è stato generato.

<xs:sequence> in un tipo complesso: contenuto

wsutil supporta completamente la sequenza di minOccurs = 1 e maxOccurs = 1; in caso contrario, il tipo complesso è attualmente associato al \_ buffer WS XML \_ . Può essere supportata come matrice di strutture.

-   elemento supportato; ogni istanza esegue il mapping a un campo nella struttura.
-   Fallback del gruppo; complexType è il fallback al \_ buffer WS XML \_ .
-   Tutti i fallback; complexType è il fallback al \_ buffer WS XML \_ .
-   scelta supportata. eseguire il mapping al campo Union.
-   fallback sequenza; complexType è il fallback al \_ buffer WS XML \_ .
-   qualsiasi supportato; mappato al \_ buffer XML.
-   (blank) supportato; complexType può essere una struttura vuota se non sono presenti attributi.

## <a name="elements"></a>Elementi

<XS: element>può verificarsi in tre contesti.

-   Può verificarsi all'interno di un <XS: Sequence>, che descrive un campo di uno struct normale. In questo caso, l'attributo maxOccurs deve essere 1. Il campo è facoltativo se minOccurs è 0.
-   Può verificarsi all'interno di un <XS: Sequence>, che descrive un campo di una matrice. In questo caso, l'attributo maxOccurs deve essere maggiore di 1 o "unbounded".
-   Potrebbe verificarsi in un <XS: Schema> come descrizione dell'elemento globale.

<XS: element> all'interno di un <XS: Sequence> o <XS: Choice> come campo in una struttura

-   Ref supportato; il riferimento all'elemento globale è stato risolto.
-   nome supportato, esegue il mapping a nome campo.
-   tipo supportato, esegue il mapping al tipo di campo. Per ulteriori informazioni, vedere "mapping dei tipi". Se non è specificato (e l'elemento non contiene un tipo anonimo), viene utilizzato XS: anyType.
-   blocca genera avviso per la funzionalità non supportata, nessuna modifica alla generazione del codice.
-   impostazione predefinita genera avviso per la funzionalità non supportata, nessuna modifica alla generazione del codice.
-   correzione di genera avviso sulla funzionalità non supportata, nessuna modifica alla generazione del codice.
-   Form ignorato. Il livello di serializzazione supporta sia moduli qualificati che non qualificati.
-   ID ignorato.
-   maxOccurs esegue il mapping a un singolo campo dati se è uguale a 1. viene mappato a un campo di matrice (elemento ripetuto) se maxOccurs è maggiore di 1.
-   minOccurs se 0, il campo opzioni è impostato su campo \_ facoltativo, se nillable non è impostato.
-   nillable il campo è nillable. Per ulteriori informazioni, vedere [serializzazione](serialization.md) .

<XS: element> come elemento globale: attributi

gli attributi minOccurs e maxOccurs non sono validi come descrizione dell'elemento globale. L'applicazione può usare direttamente la descrizione dell'elemento generato nei livelli di serializzazione o del canale.

-   abstract genera avviso sulla funzionalità non supportata, nessuna modifica alla generazione del codice.
-   blocca genera avviso per la funzionalità non supportata, nessuna modifica alla generazione del codice.
-   impostazione predefinita genera avviso per la funzionalità non supportata, nessuna modifica alla generazione del codice.
-   Genera avviso finale per la funzionalità non supportata, nessuna modifica alla generazione del codice.
-   correzione di genera avviso sulla funzionalità non supportata, nessuna modifica alla generazione del codice.
-   ID ignorato.
-   nome supportato: esegue il mapping al nome della descrizione dell'elemento globale ed è la base per il tipo anonimo quando specificato.
-   nillable ignorato: l'applicazione deve chiamare con il flag right.
-   substitutionGroup il fallback alla struttura con \_ il \_ buffer WS XML, se impostato. wsutil non supporta substitutionGroup.
-   tipo supportato e mappato al tipo dell'elemento.

<XS: element> come elemento globale: Contents

-   simpleType supportato; esegue il mapping alla definizione del tipo.
-   complexType supportato; esegue il mapping a un tipo complesso.
-   Genera un avviso univoco sulla funzionalità non supportata, nessuna modifica alla generazione del codice. wsutil non supporta vincoli di elemento.
-   chiave genera avviso per la funzionalità non supportata, nessuna modifica alla generazione del codice. wsutil non supporta vincoli di elemento.
-   keyref genera un avviso sulla funzionalità non supportata, nessuna modifica alla generazione del codice. wsutil non supporta vincoli di elemento.
-   vuoto Supportato l'elemento senza specifica del tipo viene trattato come xs: anyType.

## <a name="simple-types"></a>Tipi semplici

<XS: simpleType> attributi

-   Genera avviso finale per la funzionalità non supportata, nessuna modifica alla generazione del codice.
-   ID ignorato
-   Nome supportato, mappato al nome del tipo.

<XS: simpleType> contenuto

-   Restrizione supportata, esegue il mapping a un tipo enum o a un intervallo. Vedere la sezione relativa alle restrizioni xs: simpleType.
-   Elenco genera avviso per funzionalità non supportate, fallback al buffer XML \_ .
-   Unione genera avviso per la funzionalità non supportata, fallback al \_ buffer XML.

## <a name="simple-type-restriction"></a>Restrizione di tipo semplice

Alcuni facet sono consentiti in tipi integrali e tipo di stringhe per consentire il supporto di intervalli e enum.

supporto dell'enumerazione

<XS: Enumeration> restrizione di tipo semplice per il tipo di base della stringa viene considerata come un tipo enum. In questo caso, l'attributo di base deve essere di tipo stringa. In caso di enumerazione, tutti gli altri facet vengono ignorati.

intervallo con supporto di tipi semplici

Alcuni facet sono supportati nei tipi semplici. il supporto di un intervallo consentito per il tipo è efficace. Di seguito sono riportate le restrizioni per i tipi integrali e i tipi float/double. Per i tipi semplici con altri facet viene eseguito il fallback al \_ tipo di stringa WS

-   minExclusive supportato
-   minInclusive supportato
-   maxExclusive supportato
-   maxInclusive supportato
-   totalDigits genera un avviso sulla funzionalità non supportata, nessuna modifica alla generazione del codice.
-   fractionDigits genera un avviso sulla funzionalità non supportata, nessuna modifica alla generazione del codice.
-   la lunghezza genera un avviso sulla funzionalità non supportata, nessuna modifica alla generazione del codice.
-   minLength genera un avviso sulla funzionalità non supportata, nessuna modifica alla generazione del codice.
-   maxLength genera avviso per la funzionalità non supportata, nessuna modifica alla generazione del codice.
-   l'enumerazione genera un avviso sulla funzionalità non supportata, nessuna modifica alla generazione del codice.
-   gli spazi vuoti generano un avviso sulla funzionalità non supportata, nessuna modifica alla generazione del codice.
-   modello genera avviso per la funzionalità non supportata, nessuna modifica alla generazione del codice.
-   vuoto Supportato.

minLength e maxLength in una stringa non sono attualmente supportati, ma è una funzionalità auspicabile da supportare.

## <a name="inheritance"></a>Ereditarietà

Wsutil supporta l'ereditarietà di tipi complessi, ovvero una struttura può ereditare da un'altra struttura, in modo analogo all'ereditarietà dell'interfaccia in C++. Questa operazione viene eseguita tramite <XS: complexContentExtension>. <XS: simpleContentExtension> è supportato, ma viene generato come struttura normale con tipo di base come primo campo anziché come ereditarietà del tipo.

## <a name="typeprimitive-mapping"></a>Mapping di tipi/primitivi

È necessario normalizzare gli identificatori quando si esegue la conversione da un NCName in XML. Le stringhe sono nillable; i tipi di puntatore sono nillable; i tipi integrali e float/double sono nillable e defaultValue è impostato su 0.

![Tabella che mostra il mapping tra i tipi XSD e i tipi di dati Sapphire.](images/schematypemap.png)

 

 




