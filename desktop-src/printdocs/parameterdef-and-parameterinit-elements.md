---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: f1c73aed-fca4-47f6-bb98-bab40a6a9b2e
title: Elementi ParameterDef e ParameterInit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64e71ed86d627072ee4b5b0ca0acb4e068ae62b6
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106320963"
---
# <a name="parameterdef-and-parameterinit-elements"></a>Elementi ParameterDef e ParameterInit

Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Un elemento ParameterDef è diverso da un elemento ParameterInit in quanto descrive il valore che un elemento ParameterInit può contenere, mentre un elemento ParameterInit assegna un valore al parametro. Un elemento ParameterDef è costituito da un set specifico di elementi Property, che sono elementi figlio dell'elemento ParameterDef, che specificano il tipo di dati, i valori massimo, minimo e predefinito per i dati e altre informazioni. Questi elementi di proprietà sono descritti più avanti in questo argomento.

Gli elementi ParameterDef possono essere visualizzati solo nel contesto consentito. Per la versione iniziale dello schema di stampa, è possibile che si trovino al livello radice del documento PrintCapabilities. L'attributo Name dell'elemento ParameterDef definisce il nome del parametro. A ogni elemento ParameterDef nel documento PrintCapabilities deve essere assegnato un attributo nome univoco.

> [!Note]
> per stampare i provider di documenti delle funzionalità:
> 
> Il significato di un nome di parametro è universale; ovvero, se un elemento ParameterDef in un documento PrintCapabilities ha lo stesso attributo Name (la stringa formata dallo spazio dei nomi e il nome descrittivo dell'elemento ParameterDef) come elemento ParameterDef in un altro documento PrintCapabilities, si presuppone che entrambi gli elementi rappresentino lo stesso concetto e che debbano essere interpretati nello stesso modo. Pertanto, è possibile utilizzare un elemento ParameterDef definito in un oggetto PrintTicket per un documento PrintCapabilities per inizializzare l'elemento ParameterInit con lo stesso nome definito in un documento PrintCapabilities diverso.

 

## <a name="relationship-to-xml-attributes"></a>Relazione con attributi XML

Come è vero per tutti gli attributi del nome, il nome del parametro è nel formato di un QName XML. Un costrutto di parametro definito dallo schema ha un nome qualificato dallo spazio dei nomi Public, che costituisce l'attributo Name, mentre l'attributo Name di un costrutto di parametro definito privatamente è qualificato da uno spazio dei nomi privato univoco per l'autore.

## <a name="relationship-between-parameterdef-and-property-element-types"></a>Relazione tra ParameterDef e i tipi di elemento Property

Gli elementi ParameterDef definiti nelle parole chiave Print Schema devono essere definiti completamente in un documento PrintCapabilities. Il documento parole chiave dello schema di stampa fornisce valori nominali per alcuni elementi Property di un elemento ParameterDef, ad esempio DefaultValue e altri, ma l'autore di un documento PrintCapabilities è responsabile della definizione degli elementi rimanenti della proprietà. In ogni caso, tutti gli elementi Property devono essere definiti in modo esplicito in un elemento ParameterDef, inclusi quelli definiti nelle parole chiave Print Schema.

Alcuni elementi della proprietà di ogni elemento ParameterDef visualizzato nelle parole chiave dello schema di stampa sono designati come non *modificabili*. Ciò significa che tutte le definizioni dei documenti PrintCapabilities degli elementi ParameterDef definiti per le parole chiave dello schema di stampa devono mantenere questi elementi della proprietà senza alcuna modifica. Questi elementi di proprietà non modificabili consentono ai costrutti di parametro di essere portabili e non ambigui in tutti i documenti PrintCapabilities. Un esempio principale è rappresentata dalle unità usate in un elemento ParameterDef. Queste unità devono essere non modificabili per promuovere una comprensione coerente del loro significato. Gli elementi proprietà di un ParameterDef designato come non modificabile possono essere ridefiniti all'interno di un documento PrintCapabilities.

Un elemento ParameterDef è composto dagli elementi Property seguenti. Tutti devono essere presenti se non diversamente specificato.



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>Nome della proprietà</th>
<th>Valori</th>
<th>Descrizione</th>
<th>Immutabile?</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>DataType <br/></td>
<td>numero intero <br/> decimal<br/> string<br/> Nessun valore predefinito.<br/></td>
<td>Specifica se il valore del parametro è un numero intero o un numero a virgola mobile o una stringa di testo. Il valore di un parametro è espresso nello stesso formato del tipo di dati di base XSD corrispondente. ovvero un Integer, un numero decimale o una stringa. <br/></td>
<td>Sì<br/></td>
</tr>
<tr class="even">
<td>DefaultValue <br/></td>
<td>Tipo specificato dalla proprietà DataType.<br/> Nessun valore predefinito.<br/></td>
<td>Specifica il valore con cui inizializzare un controllo dell'interfaccia utente.<br/>
<ul>
<li>oppure <br/></li>
</ul>
Specifica il valore da utilizzare se l'elemento parametro pertinente non è presente nell'oggetto PrintTicket.<br/></td>
<td>No<br/></td>
</tr>
<tr class="odd">
<td>Obbligatorio <br/></td>
<td>Non condizionale: l'elemento ParameterInit deve essere sempre fornito. <br/> Conditional: l'elemento ParameterInit è obbligatorio solo se si fa riferimento al parametro all'interno di un elemento option in un oggetto PrintTicket.<br/> DefaultValue: condizionale.<br/></td>
<td>Indica quando un elemento ParameterInit deve essere visualizzato in modo esplicito. Se è condizionale, è necessario inizializzare ParameterInit se l'oggetto PrintTicket contiene un'opzione che fa riferimento al parametro.<br/> Utilizzato dai client dell'interfaccia utente e dai provider PrintCapabilities o PrintTicket. Si noti che in qualsiasi vincolo la proprietà obbligatoria dell'elemento ParameterDef deve essere impostata su Unconditional. ParameterDef deve avere un valore definito, in caso contrario non è stato possibile valutare il valore o il vincolo dipendente.<br/></td>
<td>No<br/></td>
</tr>
<tr class="even">
<td>MaxLength <br/></td>
<td>Integer se la proprietà DataType specifica la stringa.<br/> DefaultValue: non viene applicato alcun valore massimo.<br/></td>
<td>Per i parametri con valori di stringa, specifica la stringa più lunga consentita. I provider UI e PrintCapabilities o PrintTicket utilizzano questa proprietà per convalidare l'elemento ParameterDef.<br/></td>
<td>No<br/></td>
</tr>
<tr class="odd">
<td>MaxValue <br/></td>
<td>Integer se la proprietà DataType specifica un valore integer.<br/> Decimal se la proprietà DataType specifica Decimal.<br/> DefaultValue: non viene applicato alcun valore massimo.<br/></td>
<td>Per gli elementi ParameterDef con valori interi o decimali, definisce il valore massimo consentito.<br/></td>
<td>No<br/></td>
</tr>
<tr class="even">
<td>MinLength <br/></td>
<td>Integer se la proprietà DataType specifica la stringa. <br/> DefaultValue: non viene applicato alcun valore minimo.<br/></td>
<td>Per i valori stringa, definisce la stringa più breve consentita. I provider UI e PrintCapabilities o PrintTicket utilizzano questa proprietà per convalidare l'elemento ParameterDef.<br/></td>
<td>No<br/></td>
</tr>
<tr class="odd">
<td>MinValue <br/></td>
<td>Integer se la proprietà DataType specifica un valore integer.<br/> Decimal se la proprietà DataType specifica Decimal.<br/> DefaultValue: non viene applicato alcun valore minimo.<br/></td>
<td>Per i parametri con valori interi o decimali, definisce il valore minimo consentito. <br/></td>
<td>No<br/></td>
</tr>
<tr class="even">
<td>Più elementi <br/></td>
<td>Integer se la proprietà DataType specifica un valore integer.<br/> Decimal se la proprietà DataType specifica Decimal.<br/> DefaultValue: 1<br/></td>
<td>Per i parametri con valori interi o decimali, il valore del parametro deve essere un multiplo di questo numero. Per ulteriori informazioni, vedere <a href="#notes-on-multiple">Note su più</a> di seguito questa tabella.<br/></td>
<td>No<br/></td>
</tr>
<tr class="odd">
<td>UnitType <br/></td>
<td>valore stringa che indica le unità usate per il parametro.<br/> Nessun valore predefinito.<br/></td>
<td>Indica le unità in cui il parametro è espresso. Ad esempio, gli angoli in decimi di gradi, lunghezze in micron e così via.<br/></td>
<td>Sì<br/></td>
</tr>
</tbody>
</table>



 

## <a name="notes-on-multiple"></a>Note su più

Per gli elementi ParameterInit con valori integer o Decimal, il valore di ParameterInit deve essere un multiplo di questo numero. Ad esempio, gli elementi ParameterInit con valori decimali possono essere limitati a decimi impostando questa proprietà su 0,1. Gli elementi dell'interfaccia utente usano questa proprietà quando costruiscono finestre di dialogo e controlli dell'interfaccia utente. Inoltre, il codice di convalida PrintTicket può usare questa proprietà per arrotondare il valore di un ParameterInit al valore più vicino indicato da più. Nota: i driver di dispositivo e i provider PrintCapabilities non devono presupporre che i valori di ParameterInit siano multipli del valore della proprietà. Ogni provider deve essere in grado di arrotondare i valori arbitrari al valore utilizzabile più vicino a causa della possibilità che provider diversi possano specificare valori diversi e in conflitto per questa proprietà.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




