---
description: Usare i qualificatori definiti in questa sezione quando si crea la classe MOF del provider, la classe MOF dell'evento, la classe MOF del tipo di evento e le proprietà della classe MOF del tipo di evento.
ms.assetid: 3bc82074-05a7-411f-884f-5da1fd08112b
title: Qualificatori MOF di Traccia eventi
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 578699b04c5ba2d0f39afb2e8ff5141151bd208b
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2021
ms.locfileid: "122628440"
---
# <a name="event-tracing-mof-qualifiers"></a>Qualificatori MOF di Traccia eventi

Usare i qualificatori definiti in questa sezione quando si crea la classe [MOF](#provider-mof-class-qualifiers)del provider, la classe [MOF](#event-mof-class-qualifiers)dell'evento, la classe [MOF](#event-type-mof-class-qualifiers)del tipo di evento e le proprietà della classe [MOF](#property-qualifiers)del tipo di evento . Per un esempio che include alcuni di questi qualificatori, vedere [Pubblicazione dello schema di eventi](publishing-your-event-schema.md).

## <a name="provider-mof-class-qualifiers"></a>Qualificatori di classe MOF del provider

Nella tabella seguente sono elencati i qualificatori che è possibile specificare in una classe MOF del provider.



| Qualifier | Tipo di dati  | Descrizione                                                                                                                                                                                                                                                  |
|-----------|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Guid**  | **Stringa** | Obbligatorio. Guid di stringa che identifica in modo univoco un provider. Ad esempio, Guid("{3F92E6E0-9886-434e-85DB-0D11D3904C0A}"). Si tratta dello stesso GUID utilizzato quando si chiama la [**funzione RegisterTraceGuids**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) per registrare il provider. |



 

## <a name="event-mof-class-qualifiers"></a>Qualificatori di classe MOF degli eventi

Nella tabella seguente sono elencati i qualificatori che è possibile specificare in una classe di evento ,ovvero la classe padre che raggruppa classi di tipi di evento correlate.

| Qualifier        | Tipo di dati   | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Guid**         | **Stringa**  | Obbligatorio. Guid stringa che identifica una classe di eventi. Ad esempio, Guid("{3F92E6E0-9886-434e-85DB-0D11D3904C0A}"). I provider di eventi usano il GUID per impostare [**EVENT \_ TRACE \_ HEADER. Membro**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) GUID, in modo che i consumer possano determinare la classe di eventi che stanno ricevendo.                                                                                                                                                                                                                                                                                  |
| **EventVersion** | **Integer** | Questo qualificatore è facoltativo per la versione più recente di una classe di traccia eventi ed è necessario per tutte le versioni precedenti della classe . La versione più recente della classe non specifica il qualificatore **EventVersion** o ha il numero di versione più alto. I numeri di versione iniziano con 0, ad esempio EventVersion(0). In genere, quando si crea una nuova versione della classe, si rinomina anche la versione precedente in Vn, dove n è un numero incrementale a <classname> \_ partire da 0. Per un esempio, vedere [**FileIo**](fileio.md) e [**FileIo \_ V0.**](fileio-v0.md)<br/> |



 

## <a name="event-type-mof-class-qualifiers"></a>Qualificatori di classe MOF del tipo di evento

Nella tabella seguente sono elencati i qualificatori che è possibile specificare in una classe del tipo di evento (la classe che definisce i dati delle proprietà dell'evento).



| Qualifier         | Valore       | Descrizione                                                                                                                                                                                                                                                                                                                                                                       |
|-------------------|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **EventType**     | **Integer** | Obbligatorio. Identifica la classe del tipo di evento. Ad esempio, EventType(1). Il provider di eventi usa lo stesso valore del tipo di evento per impostare [**EVENT \_ TRACE \_ HEADER. Class.Type**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header). Se la stessa classe MOF viene usata per più tipi di evento (perché usano gli stessi dati dell'evento), specificare il valore del tipo di evento come matrice di interi, ad esempio EventType {12,15} . |
| **EventTypeName** | **Stringa**  | facoltativo. Descrive il tipo di evento. Ad esempio, EventTypeName("Start"). Se la stessa classe MOF viene usata per più tipi di evento (perché usano gli stessi dati dell'evento), specificare il valore del nome del tipo di evento come matrice di stringhe, ad esempio EventTypeName{"Start", "End"}. Gli elementi della matrice EventTypeName corrispondono direttamente alla matrice EventType.                 |



 

## <a name="property-qualifiers"></a>Qualificatori di proprietà

Nella tabella seguente sono elencati i qualificatori che è possibile specificare in una proprietà.



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Qualifier</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Bitmap</strong></td>
<td>Specifica le posizioni di bit mappate ai valori stringa. Se si specifica questo qualificatore, è necessario specificare anche il qualificatore <strong>BitValues.</strong></td>
</tr>
<tr class="even">
<td><strong>BitValues</strong></td>
<td>Valori stringa. Se viene specificato anche il qualificatore <strong>BitMap,</strong> le stringhe corrispondono direttamente ai valori nel qualificatore <strong>BitMap.</strong> In caso contrario, si supponga che il valore della proprietà sia un indice in base uno nelle stringhe di valori (il bit uno corrisponde alla prima stringa nell'elenco).</td>
</tr>
<tr class="odd">
<td><strong>Estensione</strong></td>
<td>Fornisce informazioni aggiuntive su come utilizzare (interpretare) i dati. Il valore dell'estensione non fa distinzione tra maiuscole e minuscole. Includere il valore tra virgolette, ad esempio Extension( &quot; Guid &quot; ). I valori di estensione possibili sono: <dl> <dt><span id="Guid"></span><span id="guid"></span><span id="GUID"></span>Guid</dt> <dd> Indica che i dati della proprietà sono guid. Il tipo di dati MOF deve essere <strong>object</strong>. Il payload deve essere una <strong>struttura GUID.</strong><br/> </dd> <dt><span id="IPAddr_and_IPAddrV4"></span><span id="ipaddr_and_ipaddrv4"></span><span id="IPADDR_AND_IPADDRV4"></span>IPAddr e IPAddrV4</dt> <dd> I dati sono un indirizzo IP V4. Il tipo di dati MOF deve essere <strong>object</strong>. Si prevede che il payload sia un valore long senza segno. Ogni byte del valore long senza segno rappresenta una delle quattro parti dell'indirizzo IP (p1.p2.p3.p4). Il byte di ordine basso contiene il valore per p1, il byte successivo contiene il valore per p2 e così via.<br/> <strong>Prima di Windows Vista:</strong> L'estensione IPAddrV4 non è supportata.<br/> </dd> <dt><span id="IPAddrV6"></span><span id="ipaddrv6"></span><span id="IPADDRV6"></span>IPAddrV6</dt> <dd> I dati sono un indirizzo IP V6. Il tipo di dati MOF deve essere <strong>object</strong>. È previsto che il payload sia una <strong>IN6_ADDR</strong> struttura. <br/> <strong>Prima di Windows Vista:</strong> L'estensione IPAddrV6 non è supportata.<br/> </dd> <dt><span id="NoPrint"></span><span id="noprint"></span><span id="NOPRINT"></span>NoPrint</dt> <dd> Indica che il consumer non deve stampare questi dati.<br/> </dd> <dt><span id="Port"></span><span id="port"></span><span id="PORT"></span>Porta</dt> <dd> I dati identificano un numero di porta. Il tipo di dati MOF deve essere <strong>object</strong>. È previsto che il payload sia un valore short senza segno.<br/> </dd> <dt><span id="RString"></span><span id="rstring"></span><span id="RSTRING"></span>RString</dt> <dd> I caratteri di nuova riga sono stati sostituiti con spazi. Il payload deve essere una stringa ANSI con terminazione Null.<br/> </dd> <dt><span id="RWString"></span><span id="rwstring"></span><span id="RWSTRING"></span>RWString</dt> <dd> I caratteri di nuova riga sono stati sostituiti con spazi. Il payload deve essere una stringa di caratteri wide con terminazione Null.<br/> </dd> <dt><span id="Sid"></span><span id="sid"></span><span id="SID"></span>Sid</dt> <dd> I dati rappresentano un SID BLOB binario. Il tipo di dati MOF deve essere <strong>object</strong>. <br/> Il SID è di lunghezza variabile. Il valore contenuto nei primi 4 byte (<strong>ULONG</strong>) indica se il BLOB contiene un SID. Se i primi 4 byte (<strong>ULONG</strong>) del BLOB sono diversi da zero, il BLOB contiene un SID. La prima parte del BLOB contiene il TOKEN_USER (la struttura è allineata su un limite di 8 byte) e la seconda parte contiene il SID. Per risolvere la parte SID del BLOB:<br/>
<ul>
<li>Impostare un puntatore di byte all'inizio del BLOB</li>
<li>Moltiplicare le dimensioni del puntatore per il log eventi per 2 e aggiungere il prodotto al puntatore in byte (il membro <strong>PointerSize</strong> <a href="/windows/win32/api/evntrace/ns-evntrace-trace_logfile_header"><strong>di TRACE_LOGFILE_HEADER</strong></a> contiene il valore della dimensione del puntatore)</li>
</ul>
<br/> È possibile usare la macro seguente per determinare la lunghezza del SID. <br/>
<pre class="syntax" data-space="preserve"><code>#define SeLengthSid( Sid ) \
  (8 + (4 * ((SID *)Sid)->SubAuthorityCount))</code></pre>
</dd> <dt><span id="SizeT"></span><span id="sizet"></span><span id="SIZET"></span>SizeT</dt> <dd> Indica che la proprietà contiene un valore del puntatore. La dimensione del valore del puntatore dipende dal sistema operativo usato per registrare l'evento. il payload conterrà un valore a 4 byte per i sistemi a 32 bit o un valore a 8 byte per i sistemi a 64 bit. Il tipo di dati MOF deve essere <strong>object</strong>.<br/> I consumer devono ignorare il tipo di dati e il <strong>qualificatore Format</strong> se la proprietà include <strong>l'estensione SizeT.</strong> Per determinare le dimensioni dei dati da leggere per la proprietà, usare:
<ul>
<li>Membro <strong>PointerSize</strong> di <a href="/windows/win32/api/evntrace/ns-evntrace-trace_logfile_header"><strong>TRACE_LOGFILE_HEADER</strong></a></li>
<li>Membro <strong>Flags</strong> di <a href="/windows/desktop/api/evntcons/ns-evntcons-event_header"><strong>EVENT_HEADER</strong></a></li>
</ul>
<br/> <strong>Prima di Windows Vista:</strong> Il <strong>valore PointerSize</strong> potrebbe non essere accurato. In un computer a 64 bit, ad esempio, un'applicazione a 32 bit registra puntatori a 4 byte. Tuttavia, la sessione imposta <strong>PointerSize</strong> su 8.<br/> </dd> <dt><span id="Variant"></span><span id="variant"></span><span id="VARIANT"></span>Variante</dt> <dd> I dati rappresentano un BLOB. I primi quattro byte (uint32) indicano le dimensioni del BLOB. Il tipo di dati MOF deve essere <strong>object</strong>. <br/> </dd> <dt><span id="WmiTime"></span><span id="wmitime"></span><span id="WMITIME"></span>WmiTime</dt> <dd> Converte il timestamp in ora di sistema. Il tipo di dati MOF deve essere <strong>object</strong>. Il payload dovrebbe essere un intero senza segno a 64 bit.<br/> <strong>Prima di Windows Vista:</strong> Non disponibile.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>Formato</strong></td>
<td>Definisce il formato dei dati delle proprietà. Ad esempio, l'inclusione di Format( w ) in una proprietà stringa indica &quot; che la stringa è una stringa &quot; wide. I valori possibili sono:
<table>
<thead>
<tr class="header">
<th>Termine</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="c"></span><span id="C"></span>C<br/></td>
<td>Visualizzare il valore della proprietà come carattere ASCII. È possibile usare questo qualificatore con i <strong>tipi di dati uint8.</strong><br/></td>
</tr>
<tr class="even">
<td><span id="s"></span><span id="S"></span>s<br/></td>
<td>Considerare la matrice di caratteri come stringa con terminazione Null. La stringa è una stringa di caratteri wide se il tipo di dati è <strong>char16</strong>; in caso contrario, la stringa è una stringa di caratteri ASCII.<br/></td>
</tr>
<tr class="odd">
<td><span id="w"></span><span id="W"></span>W<br/></td>
<td>Il valore della proprietà è una stringa di caratteri wide. È possibile usare questo qualificatore con tipi <strong>di dati</strong> stringa. <br/></td>
</tr>
<tr class="even">
<td><span id="x"></span><span id="X"></span>X<br/></td>
<td>Visualizzare il valore della proprietà come numero esadecimale. È possibile usare questo qualificatore con tipi di dati Integer a 16, 32 e 64 bit.<br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><strong>Puntatore</strong></td>
<td><p>Indica che la proprietà contiene un valore del puntatore. La dimensione del valore del puntatore dipende dal sistema operativo usato per registrare l'evento. il payload conterrà un valore a 4 byte per i sistemi a 32 bit o un valore a 8 byte per i sistemi a 64 bit. Il tipo di dati MOF deve essere <strong>object</strong>.</p>
<p>I consumer devono ignorare il tipo di dati e il <strong>qualificatore Format</strong> se la proprietà include <strong>l'estensione SizeT.</strong> Per determinare le dimensioni dei dati da leggere per la proprietà, usare:</p>
<ul>
<li>Membro <strong>PointerSize</strong> di <a href="/windows/win32/api/evntrace/ns-evntrace-trace_logfile_header"><strong>TRACE_LOGFILE_HEADER</strong></a></li>
<li>Membro <strong>Flags</strong> di <a href="/windows/desktop/api/evntcons/ns-evntcons-event_header"><strong>EVENT_HEADER</strong></a></li>
</ul>
<p><strong>Prima di Windows Vista:</strong> Il <strong>valore PointerSize</strong> potrebbe non essere accurato. In un computer a 64 bit, ad esempio, un'applicazione a 32 bit registra puntatori a 4 byte. Tuttavia, la sessione imposta <strong>PointerSize</strong> su 8.</p>
<p>Si noti che alcuni eventi usano <strong>PointerType</strong> anziché <strong>Pointer</strong>; non usare <strong>PointerType</strong>.</p></td>
</tr>
<tr class="even">
<td><strong>StringTermination</strong></td>
<td>Indica la modalità di terminazione della proprietà stringa. Ad esempio, StringTermination( NullTerminated ) indica che la &quot; proprietà stringa è con &quot; terminazione Null. I valori possibili sono:
<dl> <dt><span id="Counted"></span><span id="counted"></span><span id="COUNTED"></span><strong>Contato</strong></dt> <dd>
<p>La lunghezza della stringa viene incorporata all'inizio della stringa come <strong>valore USHORT.</strong></p>
</dd> <dt><span id="NotCounted"></span><span id="notcounted"></span><span id="NOTCOUNTED"></span><strong>NotCounted</strong></dt> <dd>
<p>La stringa non è con terminazione Null e la lunghezza della stringa non è incorporata all'inizio della stringa. In questo caso, la stringa deve essere l'ultimo elemento e occupare tutto lo spazio fino alla fine dei dati dell'evento.</p>
</dd> <dt><span id="NullTerminated"></span><span id="nullterminated"></span><span id="NULLTERMINATED"></span><strong>NullTerminated</strong></dt> <dd>
<p>La stringa è con terminazione Null. Se non si specifica il <strong>qualificatore StringTermination,</strong> si presuppone che la stringa sia con terminazione Null.</p>
</dd> <dt><span id="ReverseCounted"></span><span id="reversecounted"></span><span id="REVERSECOUNTED"></span><strong>ReverseCounted</strong></dt> <dd>
<p>La lunghezza della stringa viene incorporata all'inizio della stringa come valore <strong>USHORT</strong> in formato big-endian.</p>
</dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>ValueDescriptions</strong></td>
<td>Fornisce descrizioni per ogni valore nel <strong>qualificatore Valori.</strong> Le <a href="/windows/desktop/api/Tdh/nf-tdh-tdhenumerateproviderfieldinformation"><strong>funzioni TdhEnumerateProviderFieldInformation</strong></a> e <a href="/windows/desktop/api/Tdh/nf-tdh-tdhqueryproviderfieldinformation"><strong>TdhQueryProviderFieldInformation</strong></a> restituiscono queste descrizioni quando si tenta di recuperare le informazioni sulla parola chiave e sul livello. Le descrizioni sono facoltative. Se non si specificano le descrizioni, le funzioni restituiscono <strong>NULL.</strong> Per <a href="#specifying-level-and-enable-flags-values-for-a-provider">altri dettagli, vedere Specifica dei valori di livello</a> e abilitazione dei flag per un provider.</td>
</tr>
<tr class="even">
<td><strong>ValueMap</strong></td>
<td>Specifica l'indice integer o i valori del flag che eseere mappati a valori stringa. Se si specifica questo qualificatore, è necessario specificare anche il qualificatore <strong>Values</strong> e, facoltativamente, <strong>il qualificatore ValueType.</strong> Si noti che ETW non supporta l'opzione WMI di avere stringhe per i valori della mappa dei valori.
<p>L'esempio seguente illustra come usare i qualificatori ValueMap, Values e ValueType.</p>
<pre class="syntax" data-space="preserve"><code>ValueType(&quot;flag&quot;),
ValueMap {&quot;0x01&quot;, &quot;0x02&quot;, &quot;0x04&quot;, &quot;0x08&quot;},
Values {&quot;ValueMapFlag1&quot;, &quot;ValueMapFlag2&quot;, &quot;ValueMapFlag4&quot;, &quot;ValueMapFlag8&quot;}]</code></pre></td>
</tr>
<tr class="odd">
<td><strong>Valori</strong></td>
<td>Valori stringa. Se viene specificato anche il qualificatore <strong>ValueMap,</strong> le stringhe corrispondono direttamente ai valori nel <strong>qualificatore ValueMap.</strong> In caso contrario, si supponga che il valore della proprietà sia un indice in base zero nelle stringhe dei valori.</td>
</tr>
<tr class="even">
<td><strong>ValueType</strong></td>
<td>Indica se i valori <strong>valueMap</strong> sono valori di indice integer o valori di flag di bit. Se non si specifica questo qualificatore, vengono utilizzati valori di indice integer. Per specificare che i valori sono valori di indice integer, usare ValueType( &quot; index &quot; ). Per specificare che i valori sono valori di flag di bit, usare ValueType( &quot; flag &quot; ).</td>
</tr>
<tr class="odd">
<td><strong>WmiDataId</strong></td>
<td>Ogni proprietà deve contenere il <strong>qualificatore WmiDataId.</strong> <strong>WmiDataId</strong> definisce l'ordine in cui il consumer legge i dati dell'evento. Il valore di <strong>WmiDataId</strong> inizia da 1 e incrementa per ogni proprietà nella classe . Ad esempio, WmiDataId(1).</td>
</tr>
<tr class="even">
<td><strong>XMLFragment</strong></td>
<td>Indica che i dati sono in formato XML e pronti per la visualizzazione senza ulteriore formattazione.</td>
</tr>
</tbody>
</table>



 

## <a name="specifying-level-and-enable-flags-values-for-a-provider"></a>Specifica dei valori di livello e di abilitazione dei flag per un provider

Per documentare il livello e abilitare i flag che un controller userebbe per abilitare il provider, includere le proprietà "Level" e "Flags" nella classe MOF del provider. Per i nomi delle proprietà Level e Flags viene fatto distinzione tra maiuscole e minuscole. Le proprietà devono includere i **qualificatori Values** e **ValueMap,** che specificano il livello possibile e abilitano i valori del flag. ValueMap **per** i valori del flag enable deve essere un valore di bit (flag). Il **qualificatore ValueDescriptions** è facoltativo, ma è consigliabile usarlo per fornire descrizioni per ogni valore possibile. Le descrizioni vengono usate quando un utente chiama le funzioni [**TdhEnumerateProviderFieldInformation**](/windows/desktop/api/Tdh/nf-tdh-tdhenumerateproviderfieldinformation) e [**TdhQueryProviderFieldInformation**](/windows/desktop/api/Tdh/nf-tdh-tdhqueryproviderfieldinformation) per ottenere il livello possibile e abilitare i valori dei flag (parole chiave) per il provider.

Di seguito viene illustrata una classe provider che specifica i valori dei flag di abilitazione e di livello possibili.

``` syntax
[Dynamic,
 Description("IIS_Trace") : amended,
 guid("{3a2a4e84-4c21-4981-ae10-3fda0d9b0f83}"),
 locale("MS\\0x409")]
class IIS_Trace : EventTrace
{
    [Description ("Enable Flags") : amended,
        ValueDescriptions{
             "Allow_tracing_only_selected_requests ",
             "IIS_authentication_events ",
             "IIS_security_events ",
             "IIS_filter_events ",
             "IIS_static_file_events ",
             "IIS_CGI_events ",
             "IIS_compression_events ",
             "IIS_cache_events ",
             "IIS_request_notifications_events ",
             "IIS_module_events ",
             "IIS_FastCGI_events "},
        DefineValues{
             "UseUrlFilter",
             "IISAuthentication",
             "IISSecurity",
             "IISFilter",
             "IISStaticFile",
             "IISCGI",
             "IISCompression",
             "IISCache",
             "IISRequestNotification",
             "IISModule",
             "IISFastCGI"},
        Values{
             "UseUrlFilter",
             "IISAuthentication",
             "IISSecurity",
             "IISFilter",
             "IISStaticFile",
             "IISCGI",
             "IISCompression",
             "IISCache",
             "IISRequestNotification",
             "IISModule",
             "IISFastCGI"},
        ValueMap{
             "0x00000001",
             "0x00000002",
             "0x00000004",
             "0x00000008",
             "0x00000010",
             "0x00000020",
             "0x00000040",
             "0x00000080",
             "0x00000100",
             "0x00000200",
             "0x00001000"}: amended
    ]
    uint32 Flags;

    [Description ("Levels") : amended,
        ValueDescriptions{
            "Abnormal exit or termination",
            "Severe errors that need logging",
            "Warnings such as allocation failure",
            "Includes non-error cases",
            "Detailed traces from intermediate steps" } : amended,
         DefineValues{
            "TRACE_LEVEL_FATAL",
            "TRACE_LEVEL_ERROR",
            "TRACE_LEVEL_WARNING"
            "TRACE_LEVEL_INFORMATION",
            "TRACE_LEVEL_VERBOSE" },
        Values{
            "Fatal",
            "Error",
            "Warning",
            "Information",
            "Verbose" },
        ValueMap{
            "0x1",
            "0x2",
            "0x3",
            "0x4",
            "0x5" },
        ValueType("index")
    ]
    uint32 Level;
};
```

 

 
