---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: 41bc10fe-6c00-44c5-ba9a-10414b31cbdf
title: Attributi XML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70dd05effe6f3ea79afd0972867cb2734ace1a71
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/06/2021
ms.locfileid: "106321129"
---
# <a name="xml-attributes"></a>Attributi XML

Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Sono presenti numerosi attributi XML che vengono visualizzati in diversi tipi di elemento definiti in Print Schema Framework. Gli attributi XML con lo stesso nome in genere hanno lo stesso significato e rispettano le stesse regole indipendentemente dal tipo di elemento in cui risiedono. Gli attributi XML sono pertanto elencati in base al nome e non al tipo di elemento host. Gli attributi XML definiti privatamente non sono consentiti. Solo gli attributi XML definiti in questa sezione possono essere utilizzati in un documento PrintCapabilities o in un oggetto PrintTicket, quindi solo nel contesto definito.

Sebbene le parti private non siano autorizzate a introdurre nuove definizioni nello spazio dei nomi di un'altra parte, sono consentite l'utilizzo di nomi esistenti da un altro spazio dei nomi privato, purché l'utilizzo sia coerente con l'utilizzo stabilito dall'altra parte. Un'opzione può quindi contenere elementi ScoredProperty definiti da diverse entità, ognuno dei quali risiede in spazi dei nomi diversi.



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
<td>QName XML<br/></td>
<td>Questo attributo XML identifica l'istanza dell'elemento. Distingue un elemento da un altro tipo di elemento. Questo attributo XML è così ampiamente utilizzato. viene definito attributo Name.<br/></td>
<td>Le restrizioni seguenti riguardano l'attributo Name.<br/>
<ul>
<li>L'attributo del nome deve essere nel formato di un QName valido definito da XML. Ovvero deve essere qualificato da uno spazio dei nomi XML valido. I QName visualizzati come valori degli attributi del nome devono essere qualificati in modo esplicito anche se viene definito uno spazio dei nomi predefinito. <br/></li>
<li>Il contenuto di tipo carattere deve essere quello di un QName valido definito da XML. <br/></li>
<li>I nomi definiti privatamente devono essere qualificati con uno spazio dei nomi associato in modo univoco all'entità che ha introdotto l'attributo Name.<br/></li>
<li>Requisito di univocità di pari livello: due elementi di pari livello appartenenti allo stesso tipo di elemento potrebbero avere lo stesso attributo Name. L'unica eccezione è costituita dagli elementi option, in cui l'attributo Name può essere usato per definire un'opzione. Di conseguenza, gli elementi di opzioni con più elementi di pari livello possono avere lo stesso attributo Name.<br/></li>
<li>I tipi di elementi seguenti possono contenere attributi di nome: Property, ScoredProperty, ParameterDef, Option e feature.<br/></li>
<li>gli attributi di nome devono essere visualizzati in ognuno dei tipi di elemento che li contengono, tranne nel caso di alcuni elementi di opzioni dello schema di stampa pubblico definiti in precedenza, ad esempio DocumentNUp.<br/></li>
</ul>
Nell'esempio seguente viene illustrato come identificare un'istanza di opzione utilizzando un attributo ' name '. Questo è il modo corretto per definire gli elementi delle opzioni. Un provider non deve avere opzioni senza nome, a meno che non siano definite pubblicamente nello schema di stampa, ad esempio DocumentNUp.<br/>
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
<td>propagare <br/></td>
<td>Enumerazione<br/> Nessun valore attualmente definito.<br/></td>
<td>L'attributo propagate non viene utilizzato nella versione iniziale di Print Schema Framework. Questo argomento è documentato in modo che il codice di convalida PrintCapabilities o PrintTicket implementato per la versione iniziale di Print Schema Framework possa elaborare le versioni dello schema successive senza errori.<br/></td>

</tr>
<tr class="odd">
<td>vincolata <br/></td>
<td>Enumerazione<br/> Valori consentiti:<br/>
<ul>
<li>nessuno <br/></li>
<li>PrintTicketSettings <br/></li>
<li>AdminSettings <br/></li>
<li>DeviceSettings <br/></li>
</ul></td>
<td>Indica se l'opzione è disponibile per la selezione o per l'utilizzo. <br/></td>
<td>I valori consentiti dell'attributo vincolato hanno i significati seguenti. Si noti che questi valori sono elencati nell'ordine, dal meno restrittivo (nessuno) al più restrittivo (DeviceSettings).<br/> nessuno <br/>
<ul>
<li>L'opzione non è vincolata. <br/></li>
</ul>
PrintTicketSettings <br/>
<ul>
<li>L'opzione è vincolata dalle impostazioni PrintTicket. Ciò implica che la modifica della configurazione può rimuovere il vincolo. <br/></li>
</ul>
AdminSettings <br/>
<ul>
<li>L'opzione è vincolata dalle impostazioni dell'amministratore. l'opzione non può essere abilitata dall'utente.<br/></li>
</ul>
DeviceSettings <br/>
<ul>
<li>L'opzione è vincolata dalle impostazioni del dispositivo o dalle opzioni del dispositivo fisicamente installate; l'opzione non può essere abilitata dall'utente o dall'amministratore.<br/></li>
</ul>
Quando il provider PrintCapabilities segnala i valori dell'attributo vincolato, il vincolo più restrittivo rilevato deve essere segnalato. Se, ad esempio, un'opzione è vincolata sia da un'impostazione di amministratore che da un'impostazione del dispositivo, il provider PrintCapabilities deve segnalare DeviceSettings.<br/></td>
</tr>
<tr class="even">
<td>xmlns <br/></td>
<td>URI<br/></td>
<td>Questo attributo XML stabilisce un collegamento tra un URI (Uniform Resource Identifier) dello spazio dei nomi e il prefisso dello spazio dei nomi visualizzato nel QName XML. È necessario stabilire un collegamento di questo tipo all'URI dello spazio dei nomi definito per il Framework dello schema di stampa prima di poter utilizzare i tag degli elementi definiti dal Framework, gli attributi, gli attributi del nome e così via. È possibile dichiarare questo spazio dei nomi come predefinito per evitare di qualificare effettivamente i tag dell'elemento con un prefisso dello spazio dei nomi, anche se tutti gli altri QName devono essere qualificati in modo esplicito. Lo spazio dei nomi standard deve essere definito nell'elemento radice appropriato. Osservare tutte le regole e le convenzioni XML relative all'utilizzo dell'attributo xmlns.<br/> L'URI per il Framework di Stampa schema è http://schemas.microsoft.com/windows/2003/08/printing/printschemaframework .<br/> L'URI per le parole chiave di Print Schema è https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords .<br/></td>

</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




