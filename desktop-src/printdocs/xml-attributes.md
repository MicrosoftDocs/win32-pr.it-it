---
description: Informazioni sugli attributi XML in Print Schema Framework. Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Print Schema Specification( Specifica dello schema di stampa).
ms.assetid: 41bc10fe-6c00-44c5-ba9a-10414b31cbdf
title: Attributi XML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d410dcb1476d90568bee10c7c1e41ee7a9bee2e7
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/09/2021
ms.locfileid: "113548819"
---
# <a name="xml-attributes"></a>Attributi XML

Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Esistono diversi attributi XML presenti in diversi tipi di elemento definiti in Print Schema Framework. Gli attributi XML con lo stesso nome hanno in genere lo stesso significato e rispettano le stesse regole indipendentemente dal tipo di elemento in cui si trovano. Di conseguenza, gli attributi XML sono elencati qui in base al nome e non in base al tipo di elemento host. Gli attributi XML definiti privatamente non sono consentiti. Solo gli attributi XML definiti qui possono essere usati in un documento PrintCapabilities o printTicket e quindi solo nel contesto definito.

Sebbene le parti private non siano autorizzate a introdurre nuove definizioni nello spazio dei nomi di un'altra parte, possono usare nomi esistenti di un altro spazio dei nomi privato, purché l'uso sia coerente con l'utilizzo stabilito dall'altra parte. Un'opzione può quindi contenere elementi ScoredProperty definiti da diverse parti, ognuna delle quali risiede in spazi dei nomi diversi.



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>Nome attributo</th>
<th>Tipi di dati e valori</th>
<th>Scopo</th>
<th>Note</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>name <br/></td>
<td>XML QName<br/></td>
<td>Questo attributo XML identifica l'istanza dell'elemento. Distingue un elemento da un altro dello stesso tipo di elemento. Questo attributo XML è così ampiamente usato che viene definito attributo name.<br/></td>
<td>Le restrizioni seguenti riguardano l'attributo name.<br/>
<ul>
<li>L'attributo name deve essere nel formato di un QName definito da XML valido. Ciò significa che deve essere qualificato da uno spazio dei nomi XML valido. I nomi QName visualizzati come valori degli attributi del nome devono essere qualificati in modo esplicito con lo spazio dei nomi anche se è definito uno spazio dei nomi predefinito. <br/></li>
<li>Il contenuto dei caratteri deve corrispondere a quello di un QName definito da XML valido. <br/></li>
<li>I nomi definiti privatamente devono essere qualificati con uno spazio dei nomi associato in modo univoco all'entità che ha introdotto l'attributo name.<br/></li>
<li>Requisito di univocità di pari livello: due elementi di pari livello appartenenti allo stesso tipo di elemento non possono avere lo stesso attributo name. L'unica eccezione sono gli elementi Option, in cui l'attributo name può essere usato per definire un'opzione. Di conseguenza, gli elementi Option con più elementi di pari livello possono avere lo stesso attributo name.<br/></li>
<li>I tipi di elemento seguenti possono contenere attributi di nome: Property, ScoredProperty, ParameterDef, Option e Feature.<br/></li>
<li>Gli attributi name devono essere visualizzati in ognuno dei tipi di elemento che li contengono, tranne nel caso di alcuni elementi Print Schema Option pubblici definiti in precedenza, ad esempio DocumentNUp.<br/></li>
</ul>
Nell'esempio seguente viene illustrato come identificare un'istanza Option usando un attributo 'name'. Questo è il modo corretto per definire gli elementi Option. Un provider non deve avere opzioni senza nome, a meno che non siano definite pubblicamente nello schema di stampa, ad esempio DocumentNUp.<br/>
<pre class="syntax" data-space="preserve"><code>  <psf:Option name=&quot;psk:StapleBottomRight&quot;>
    <psf:ScoredProperty name=&quot;psk:Angle&quot;>
      <psf:Value xsi:type=&quot;xs:integer&quot;>_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name=&quot;psk:SheetCapacity&quot; >
      <psf:Value xsi:type=&quot;xs:integer&quot;>_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option></code></pre></td>
</tr>
<tr class="even">
<td>Propagare <br/></td>
<td>Enumerazione<br/> Nessun valore è attualmente definito.<br/></td>
<td>L'attributo propagate non viene usato nella versione iniziale di Print Schema Framework. Questo documento è documentato in modo che il codice di convalida PrintCapabilities o PrintTicket implementato per la versione iniziale di Print Schema Framework possa elaborare qualsiasi versione successiva dello schema senza errori.<br/></td>

</tr>
<tr class="odd">
<td>Vincolata <br/></td>
<td>Enumerazione<br/> Valori consentiti:<br/>
<ul>
<li>Nessuno <br/></li>
<li>PrintTicketSettings <br/></li>
<li>AdminSettings <br/></li>
<li>Impostazioni dispositivo <br/></li>
</ul></td>
<td>Indica se l'opzione è disponibile per la selezione o per l'utilizzo. <br/></td>
<td>I valori consentiti dell'attributo vincolato hanno i significati seguenti. Si noti che questi valori sono elencati in ordine, dal meno restrittivo (Nessuno) al più restrittivo (DeviceSettings).<br/> Nessuno <br/>
<ul>
<li>L'opzione non è vincolata. <br/></li>
</ul>
PrintTicketSettings <br/>
<ul>
<li>L'opzione è vincolata dalle impostazioni di PrintTicket. Ciò implica che la modifica della configurazione può rimuovere il vincolo. <br/></li>
</ul>
AdminSettings <br/>
<ul>
<li>L'opzione è vincolata dalle impostazioni dell'amministratore. L'opzione non può essere abilitata dall'utente.<br/></li>
</ul>
Impostazioni dispositivo <br/>
<ul>
<li>L'opzione è vincolata dalle impostazioni del dispositivo o dalle opzioni del dispositivo installato fisicamente. L'opzione non può essere abilitata dall'utente o dall'amministratore.<br/></li>
</ul>
Quando il provider PrintCapabilities segnala i valori dell'attributo vincolato, deve essere segnalato il vincolo più restrittivo trovato. Ad esempio, se un'opzione è vincolata sia da un'impostazione dell'amministratore che da un'impostazione del dispositivo, il provider PrintCapabilities deve segnalare DeviceSettings.<br/></td>
</tr>
<tr class="even">
<td>xmlns <br/></td>
<td>URI<br/></td>
<td>Questo attributo XML stabilisce un collegamento tra un URI (Uniform Resource Identifier) dello spazio dei nomi e il prefisso dello spazio dei nomi visualizzato nel QName XML. È necessario stabilire un collegamento di questo tipo all'URI dello spazio dei nomi definito per Print Schema Framework prima di poter usare qualsiasi tag di elemento definito dal framework, attributi, attributi del nome e così via. È possibile dichiarare questo spazio dei nomi come predefinito per evitare di qualificare effettivamente i tag degli elementi con un prefisso dello spazio dei nomi, anche se tutti gli altri QName devono essere qualificati in modo esplicito. Lo spazio dei nomi standard deve essere definito nell'elemento radice appropriato. Osservare tutte le regole e le convenzioni XML relative all'uso dell'attributo xmlns.<br/> L'URI per Print Schema Framework è http://schemas.microsoft.com/windows/2003/08/printing/printschemaframework .<br/> L'URI per le parole chiave dello schema di stampa è https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords .<br/></td>

</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




