---
title: Tipo complesso ChannelType
description: Definisce un canale in cui i provider possono registrare eventi.
ms.assetid: 882506e5-222b-45c8-af4b-59db8baa1dae
keywords:
- Tipo complesso ChannelType EventLog
topic_type:
- apiref
api_name:
- ChannelType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b780d68d419fa29d5ee13995f1b66a412fc89323
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2021
ms.locfileid: "122627967"
---
# <a name="channeltype-complex-type"></a>Tipo complesso ChannelType

Definisce un canale in cui i provider possono registrare eventi.

``` syntax
<xs:complexType name="ChannelType"
    mixed="true"
>
    <xs:sequence>
        <xs:element name="logging"
            type="ChannelLoggingType"
            minOccurs="0"
         />
        <xs:element name="publishing"
            type="ChannelPublishingType"
            minOccurs="0"
         />
    </xs:sequence>
    <xs:attribute name="name"
        type="anyURI"
        use="required"
     />
    <xs:attribute name="chid"
        type="token"
        use="optional"
     />
    <xs:attribute name="type"
        type="string"
        use="required"
     />
    <xs:attribute name="symbol"
        type="CSymbolType"
        use="optional"
     />
    <xs:attribute name="access"
        type="string"
        use="optional"
     />
    <xs:attribute name="isolation"
        type="string"
        use="optional"
     />
    <xs:attribute name="enabled"
        type="boolean"
        default="false"
        use="optional"
     />
    <xs:attribute name="value"
        type="UInt8Type"
        use="optional"
     />
    <xs:attribute name="message"
        type="string"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Elementi figlio



| Elemento                                                                  | Tipo                                                                                   | Descrizione                                                                                                                                                                                                |
|--------------------------------------------------------------------------|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**registrazione**](eventmanifestschema-logging-channeltype-element.md)       | [**ChannelLoggingType**](eventmanifestschema-channelloggingtype-complextype.md)       | Definisce le proprietà del file di log su cui si trova il canale, ad esempio la capacità e se il file di log è sequenziale o circolare.<br/>                                                         |
| [**Pubblicazione**](eventmanifestschema-publishing-channeltype-element.md) | [**ChannelPublishingType**](eventmanifestschema-channelpublishingtype-complextype.md) | Definisce le proprietà di registrazione per la sessione utilizzata dal canale. Solo i canali e i canali di debug e analitico che usano l'isolamento personalizzato possono specificare le proprietà di registrazione per la sessione.<br/> |



## <a name="attributes"></a>Attributi



<table>
<colgroup>
<col  />
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Nome</th>
<th>Tipo</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>access</td>
<td>string</td>
<td>Descrittore di accesso SDDL <a href="/windows/desktop/SecAuthZ/security-descriptor-definition-language">(Security Descriptor Definition Language)</a> che controlla l'accesso al file di log che si connette al canale. Se <strong>l'attributo di</strong> isolamento è impostato su Applicazione o Sistema, il descrittore di accesso controlla l'accesso in lettura al file (le autorizzazioni di scrittura vengono ignorate). Se <strong>l'attributo di</strong> isolamento è impostato su Custom, il descrittore di accesso controlla l'accesso in scrittura al canale e l'accesso in lettura al file.<br/></td>
</tr>
<tr class="even">
<td>chid</td>
<td>token</td>
<td>Identificatore che identifica in modo univoco il canale nell'elenco di canali definiti o importati dal provider. Usare questo valore quando si fa riferimento al canale in un evento. Se non si specifica un identificatore di canale, usare il nome del canale per fare riferimento a questo canale in una definizione di evento.<br/></td>
</tr>
<tr class="odd">
<td>Enabled</td>
<td>boolean</td>
<td>Determina se il canale è abilitato. Impostare su <strong>true per</strong> consentire la registrazione al canale. in caso contrario, <strong>false.</strong> Il valore predefinito <strong>è false</strong> (la registrazione è disabilitata).<br/> Poiché i tipi di canale debug e analitico sono canali con volumi elevati, è consigliabile abilitare il canale solo quando si analizza un problema relativo a un componente che scrive in tale canale. In caso contrario, il canale deve rimanere disabilitato.<br/> Ogni volta che si abilita un canale debug e analitico, il servizio cancella gli eventi dal canale.<br/></td>
</tr>
<tr class="even">
<td>Isolamento</td>
<td>string</td>
<td>Il valore di isolamento definisce le autorizzazioni di accesso predefinite per il canale. È possibile specificare uno dei valori seguenti:
<ul>
<li><strong>Applicazione</strong></li>
<li><strong>Sistema</strong></li>
<li><strong>Impostazione personalizzata</strong></li>
</ul>
L'isolamento predefinito è <strong>Application.</strong> Le autorizzazioni predefinite per <strong>l'applicazione</strong> sono (visualizzate tramite SDDL): <br/> <span data-codelanguage="Text"></span>
<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Testo</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>            L&quot;O:BAG:SYD:&quot;
            L&quot;(A;;0xf0007;;;SY)&quot;                // local system               (read, write, clear)
            L&quot;(A;;0x7;;;BA)&quot;                    // built-in admins            (read, write, clear)
            L&quot;(A;;0x7;;;SO)&quot;                    // server operators           (read, write, clear)
            L&quot;(A;;0x3;;;IU)&quot;                    // INTERACTIVE LOGON          (read, write)
            L&quot;(A;;0x3;;;SU)&quot;                    // SERVICES LOGON             (read, write)
            L&quot;(A;;0x3;;;S-1-5-3)&quot;               // BATCH LOGON                (read, write)
            L&quot;(A;;0x3;;;S-1-5-33)&quot;              // write restricted service   (read, write)
            L&quot;(A;;0x1;;;S-1-5-32-573)&quot;;         // event log readers          (read) </code></pre></td>
</tr>
</tbody>
</table>

<p>Le autorizzazioni predefinite per <strong>System</strong> sono (visualizzate tramite SDDL):</p>
<div class="code">
<span data-codelanguage="Text"></span>
<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Testo</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>            L&quot;O:BAG:SYD:&quot;
            L&quot;(A;;0xf0007;;;SY)&quot;                // local system             (read, write, clear)
            L&quot;(A;;0x7;;;BA)&quot;                    // built-in admins          (read, write, clear)
            L&quot;(A;;0x3;;;BO)&quot;                    // backup operators         (read, write)
            L&quot;(A;;0x5;;;SO)&quot;                    // server operators         (read, clear) 
            L&quot;(A;;0x1;;;IU)&quot;                    // INTERACTIVE LOGON        (read)
            L&quot;(A;;0x3;;;SU)&quot;                    // SERVICES LOGON           (read, write)
            L&quot;(A;;0x1;;;S-1-5-3)&quot;               // BATCH LOGON              (read)
            L&quot;(A;;0x2;;;S-1-5-33)&quot;              // write restricted service (write)
            L&quot;(A;;0x1;;;S-1-5-32-573)&quot;;         // event log readers        (read)</code></pre></td>
</tr>
</tbody>
</table>

</div>
<p>Le autorizzazioni predefinite per <strong>Isolamento</strong> personalizzato sono le stesse dell'applicazione.</p>
<p>I canali che <strong>specificano l'isolamento</strong> dell'applicazione usano la stessa sessione ETW. Lo stesso vale per <strong>l'isolamento del</strong> sistema. Tuttavia, se si specifica <strong>Isolamento</strong> personalizzato, il servizio crea una sessione ETW separata per il canale. <strong>L'uso</strong> dell'isolamento personalizzato consente di controllare le autorizzazioni di accesso per il canale e il file di backup. Poiché sono disponibili solo 64 sessioni ETW, è consigliabile limitare l'uso <strong>dell'isolamento</strong> personalizzato.</p></td>
</tr>
<tr class="odd">
<td>message</td>
<td>string</td>
<td><p>Nome visualizzato localizzato per il canale. La stringa del messaggio fa riferimento a una stringa localizzata <a href="eventmanifestschema-stringtable-resources-element.md"><strong>nella sezione stringTable</strong></a> del manifesto.</p></td>
</tr>
<tr class="even">
<td>name</td>
<td>anyURI</td>
<td><p>Nome del canale. Il nome deve essere univoco all'interno dell'elenco di canali utilizzati dal provider. La convenzione per la denominazione dei canali è l'aggiunta del tipo di canale al nome del provider. Ad esempio, Se il nome del provider è Company-Product-Component e si sta definendo un canale operativo, il nome sarà Company-Product-Component/Operational.</p>
<p>I nomi dei canali devono contenere meno di 255 caratteri e non possono contenere i caratteri seguenti: '>', '<', '&', '&quot;', '|', '\', ':', '`', '?', '*', or characters with codes less than 31.</p></td>
</tr>
<tr class="odd">
<td>simbolo</td>
<td><a href="eventmanifestschema-csymboltype-simpletype.md"><strong>CSymbolType</strong></a></td>
<td><p>Simbolo da usare per fare riferimento al canale nell'applicazione. Il <a href="message-compiler--mc-exe-.md"><strong>compilatore di messaggi (MC.exe)</strong></a> usa il simbolo per creare una costante per il canale nel file di intestazione generato dal compilatore. Se non si specifica un simbolo, il compilatore genera automaticamente il nome.</p></td>
</tr>
<tr class="even">
<td>tipo</td>
<td>string</td>
<td><p>Identifica il tipo del canale. È possibile specificare uno dei tipi seguenti:</p>
<ul>
<li><strong>Admin</strong></li>
<li><strong>Operativo</strong></li>
<li><strong>Analitici</strong></li>
<li><strong>Eseguire il debug</strong></li>
</ul>
<p>I canali di tipo amministratore supportano gli eventi che hanno come destinazione utenti finali, amministratori e personale di supporto. Gli eventi scritti nei canali di amministrazione devono avere una soluzione ben definita su cui l'amministratore può agire. Un esempio di evento amministratore è un evento che si verifica quando un'applicazione non riesce a connettersi a una stampante. Questi eventi sono ben documentati o sono associati a un messaggio che fornisce al lettore istruzioni dirette sulle operazioni da eseguire per risolvere il problema.</p>
<p>I canali di tipo operativo supportano gli eventi usati per analizzare e diagnosticare un problema o un'occorrenza. Si possono utilizzare per lanciare strumenti o attività basati sul problema o sull'occorrenza. Un esempio di un evento operativo è un evento che si verifica quando si aggiunge o rimuove una stampante da un sistema.</p>
<p>I canali di tipo analitico supportano gli eventi pubblicati in volumi elevati. Essi descrivono le operazioni del programma e indicano problemi che non possono essere gestiti dall'intervento dell'utente.</p>
<p>I canali di tipo debug supportano gli eventi utilizzati esclusivamente dagli sviluppatori per diagnosticare un problema di debug.</p>
<p>I canali analitici e di debug sono disabilitati per impostazione predefinita e devono essere abilitati solo per determinare la causa di un problema. Ad esempio, è possibile abilitare il canale, eseguire lo scenario che causa il problema, disabilitare il canale e quindi eseguire query sugli eventi. Si noti che l'abilitazione del canale cancella il canale degli eventi esistenti. Se il canale analitico e di debug usa un file di backup circolare, è necessario disabilitare il canale per eseguire query sugli eventi.</p>
<p>Tutti i canali di amministrazione usano la stessa sessione ETW. lo stesso vale per i canali operativi. Tuttavia, ogni canale analitico e di debug usa una sessione ETW separata, che è un altro motivo per abilitare questi tipi di canale solo quando necessario (è disponibile un numero limitato di sessioni ETW).</p></td>
</tr>
<tr class="odd">
<td>Valore</td>
<td><a href="eventmanifestschema-hexint8type-simpletype.md"><strong>UInt8Type</strong></a></td>
<td><p>Identificatore numerico che identifica in modo univoco il canale all'interno dell'elenco di canali definito dal provider. Se non specificato, il compilatore di messaggi assegna il valore .</p></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a>Commenti

Se il nome del canale segue la convenzione di denominazione del canale, Windows Visualizzatore eventi il canale verrà elencato usando la stringa che segue la barra rovesciata. Ad esempio, se il nome del canale è Company-Product-Component/Operational, il Visualizzatore eventi esemplerà il canale come Operativo nel provider Company-Product-Component. In caso contrario, l'intero nome del canale viene visualizzato sotto il provider. Se specificato, viene usato il nome visualizzato localizzato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/> |



 

 




`
