---
description: Questo argomento non è corrente. Per informazioni aggiornate, vedere Print Schema Specification.
ms.assetid: f1c73aed-fca4-47f6-bb98-bab40a6a9b2e
title: Elementi ParameterDef e ParameterInit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fa945ad7fec484828bd81b2052f9b330d0e1679
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122475127"
---
# <a name="parameterdef-and-parameterinit-elements"></a>Elementi ParameterDef e ParameterInit

Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Un elemento ParameterDef è diverso da un elemento ParameterInit perché descrive il valore che può contenere un elemento ParameterInit, mentre un elemento ParameterInit assegna un valore al parametro. Un elemento ParameterDef è costituito da un set specifico di elementi Property, che sono elementi figlio dell'elemento ParameterDef, che specificano il tipo di dati, i valori massimi, minimi e predefiniti per i dati e altre informazioni. Questi elementi Property vengono descritti più avanti in questo argomento.

Gli elementi ParameterDef possono essere visualizzati solo nel contesto consentito. Per la versione iniziale dello schema di stampa possono trovarsi al livello radice del documento PrintCapabilities. L'attributo name dell'elemento ParameterDef definisce il nome del parametro. A ogni elemento ParameterDef del documento PrintCapabilities deve essere assegnato un attributo nome univoco.

> [!Note]
> per i provider di documenti per le funzionalità di stampa:
> 
> Il significato di un nome di parametro è universale. Ovvero, se un elemento ParameterDef in un documento PrintCapabilities ha lo stesso attributo name (la stringa formata dallo spazio dei nomi e il nome descrittivo dell'elemento ParameterDef) come elemento ParameterDef in un altro documento PrintCapabilities, si presuppone che entrambi gli elementi rappresentino lo stesso concetto e debbano essere interpretati nello stesso modo. È quindi possibile usare un elemento ParameterDef definito in un PrintTicket per un documento PrintCapabilities per inizializzare l'elemento ParameterInit con lo stesso nome definito in un documento PrintCapabilities diverso.

 

## <a name="relationship-to-xml-attributes"></a>Relazione con attributi XML

Come per tutti gli attributi del nome, il nome del parametro è nel formato QName XML. Un costrutto di parametro definito dallo schema ha un nome qualificato dallo spazio dei nomi pubblico, che forma l'attributo name, mentre l'attributo name di un costrutto di parametro definito privatamente è qualificato da uno spazio dei nomi privato univoco per l'autore.

## <a name="relationship-between-parameterdef-and-property-element-types"></a>Relazione tra i tipi di elemento ParameterDef e property

Gli elementi ParameterDef definiti nelle parole chiave dello schema di stampa devono essere definiti completamente in un documento PrintCapabilities. Il documento Print Schema Keywords fornisce valori nominali per alcuni elementi Property di un elemento ParameterDef (ad esempio DefaultValue e altri), ma l'autore di un documento PrintCapabilities è responsabile della definizione degli elementi Property rimanenti. In ogni caso, tutti gli elementi Property devono essere definiti in modo esplicito in un elemento ParameterDef, inclusi quelli definiti nelle parole chiave dello schema di stampa.

Alcuni elementi Property di ogni elemento ParameterDef visualizzato nelle parole chiave dello schema di stampa sono designati come *non modificabili.* Ciò significa che tutte le definizioni di documento PrintCapabilities degli elementi ParameterDef definiti dalle parole chiave dello schema di stampa devono mantenere questi elementi Property senza alcuna modifica. Questi elementi Property non modificabili consentono ai costrutti di parametro di essere portabili e non ambigui in tutti i documenti PrintCapabilities. Un esempio primo è l'unità usata in un elemento ParameterDef. Queste unità devono essere non modificabili per promuovere una comprensione coerente del loro significato. Gli elementi di proprietà di un ParameterDef designati come non modificabili possono essere ridefiniti all'interno di un documento PrintCapabilities.

Un elemento ParameterDef è costituito dai seguenti elementi Property. Se non specificato diversamente, tutti devono essere presenti.




| Nome della proprietà | Valori | Descrizione | Immutabile? | 
|---------------|--------|-------------|------------|
| DataType <br /> | numero intero <br /> decimal<br /> string<br /> Nessun valore predefinito.<br /> | Specifica se il valore del parametro è un numero intero, un numero a virgola mobile o una stringa di testo. Il valore di un parametro è espresso nello stesso formato del tipo di dati di base XSD corrispondente. ad esempio un numero intero, un decimale o una stringa. <br /> | Sì<br /> | 
| DefaultValue <br /> | Tipo specificato dalla proprietà DataType.<br /> Nessun valore predefinito.<br /> | Specifica il valore con cui inizializzare un controllo dell'interfaccia utente.<br /><ul><li>oppure <br /></li></ul>Specifica il valore da usare se l'elemento del parametro pertinente non è presente in PrintTicket.<br /> | No<br /> | 
| Obbligatorio <br /> | Non condizionale: l'elemento ParameterInit deve essere sempre specificato. <br /> Condizionale: l'elemento ParameterInit è obbligatorio solo se si fa riferimento al parametro all'interno di un elemento Option in un PrintTicket.<br /> DefaultValue: condizionale.<br /> | Indica quando un elemento ParameterInit deve essere visualizzato in modo esplicito. Se Conditional, ParameterInit deve essere inizializzato se PrintTicket contiene un'opzione che fa riferimento al parametro .<br /> Usato dai client dell'interfaccia utente e dai provider PrintCapabilities o PrintTicket. Si noti che in qualsiasi vincolo la proprietà Mandatory dell'elemento ParameterDef deve essere impostata su Unconditional. ParameterDef deve avere un valore definito, in caso contrario il valore dipendente o il vincolo non può essere valutato.<br /> | No<br /> | 
| MaxLength <br /> | Integer se la proprietà DataType specifica una stringa.<br /> DefaultValue: non viene applicato alcun valore massimo.<br /> | Per i parametri con valori stringa, specifica la stringa più lunga consentita. I provider UI e PrintCapabilities o PrintTicket usano questa proprietà per convalidare l'elemento ParameterDef.<br /> | No<br /> | 
| MaxValue <br /> | integer se la proprietà DataType specifica integer.<br /> decimal se la proprietà DataType specifica decimal.<br /> DefaultValue: non viene applicato alcun valore massimo.<br /> | Per gli elementi ParameterDef con valori interi o decimali, definisce il valore massimo consentito.<br /> | No<br /> | 
| Minlength <br /> | Integer se la proprietà DataType specifica una stringa. <br /> DefaultValue: non viene applicato alcun valore minimo.<br /> | Per i valori stringa, definisce la stringa più breve consentita. I provider UI e PrintCapabilities o PrintTicket usano questa proprietà per convalidare l'elemento ParameterDef.<br /> | No<br /> | 
| Minvalue <br /> | integer se la proprietà DataType specifica integer.<br /> decimal se la proprietà DataType specifica decimal.<br /> DefaultValue: non viene applicato alcun valore minimo.<br /> | Per i parametri con valori interi o decimali, definisce il valore minimo consentito. <br /> | No<br /> | 
| Più elementi <br /> | integer se la proprietà DataType specifica integer.<br /> decimal se la proprietà DataType specifica decimal.<br /> DefaultValue: 1<br /> | Per i parametri con valori interi o decimali, il valore del parametro deve essere un multiplo di questo numero. Per altre informazioni, vedere <a href="#notes-on-multiple">Note su più dopo</a> questa tabella.<br /> | No<br /> | 
| Tipo di unità <br /> | Valore stringa che indica le unità utilizzate per il parametro .<br /> Nessun valore predefinito.<br /> | Indica le unità in cui è espresso il parametro. Ad esempio, angoli in decimi di gradi, lunghezze in micron e così via.<br /> | Sì<br /> | 




 

## <a name="notes-on-multiple"></a>Note su più

Per gli elementi ParameterInit con valori interi o decimali, il valore di ParameterInit deve essere un multiplo di questo numero. Ad esempio, gli elementi ParameterInit con valori decimali possono essere limitati a decime impostando questa proprietà su 0,1. Gli elementi dell'interfaccia utente usano questa proprietà quando creano finestre di dialogo e controlli dell'interfaccia utente. Inoltre, il codice di convalida PrintTicket può usare questa proprietà per arrotondare il valore di ParameterInit al valore più vicino indicato da Multiple. Nota: i driver di dispositivo e i provider PrintCapabilities non devono presupporre che i valori ParameterInit siano multipli di questo valore property. Ogni provider deve essere in grado di arrotondare valori arbitrari al valore utilizzabile più vicino a causa della possibilità che provider diversi possano specificare valori diversi e in conflitto per questa proprietà.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




