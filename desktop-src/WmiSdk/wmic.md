---
description: L'utilità della riga di comando WMI (WMIC) fornisce un'interfaccia della riga di comando per WMI.
ms.assetid: a0f5c1e2-9a4d-4c2b-b324-58ec01e67b6e
ms.tgt_platform: multiple
title: wmic
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bee63220bec5cae1c41480187c78211f46ed020
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881079"
---
# <a name="wmic"></a>wmic

L'utilità della riga di comando WMI (WMIC) fornisce un'interfaccia della riga di comando per Windows Management Instrumentation (WMI). WMIC è compatibile con shell e comandi di utilità esistenti. Di seguito è riportato un argomento di riferimento generale per WMIC. Per altre informazioni e linee guida sull'uso di WMIC, incluse informazioni aggiuntive su alias, verbi, opzioni e comandi, vedere [Using Windows Management Instrumentation Command-line](/previous-versions/windows/it-pro/windows-server-2003/cc779482(v=ws.10)) and [WMIC - Take Command-line Control over WMI](/previous-versions/windows/it-pro/windows-2000-server/bb742610(v=technet.10)).

## <a name="alias"></a>Alias

Un alias è una ridenominazione semplice di una classe, una proprietà o un metodo che semplifica l'uso e la lettura di WMI. È possibile determinare quali alias sono disponibili per WMIC tramite **/?** . È anche possibile determinare gli alias per una classe specifica usando **&lt; className &gt; /?** . Per altre informazioni, vedere [Alias WMIC](/previous-versions/windows/it-pro/windows-server-2003/cc736307(v=ws.10)).

## <a name="switch"></a>Commutatore

Un'opzione è un'opzione WMIC che è possibile impostare a livello globale o facoltativamente. Per un elenco delle opzioni disponibili, vedere [Commutatori WMIC](/previous-versions/windows/it-pro/windows-server-2003/cc787035(v=ws.10)).

## <a name="verbs"></a>Verbi

Per usare i verbi in WMIC, immettere il nome dell'alias seguito dal verbo. Se un alias non supporta un verbo, viene visualizzato il messaggio "Provider is not capable of the attempted operation". Per altre informazioni, vedere [Verbi WMIC](/previous-versions/windows/it-pro/windows-server-2003/cc784966(v=ws.10)).

La maggior parte degli alias supporta i verbi seguenti.

<dl> <dt>

<span id="ASSOC"></span><span id="assoc"></span>ASSOC
</dt> <dd>

Restituisce il risultato della query in cui<oggetto wmi>è il percorso degli oggetti restituiti dai comandi `Associators of (<wmi_object>)` **PATH** **o CLASS.** *\_* I risultati sono istanze associate all'oggetto . Quando ASSOC viene usato con un alias, vengono restituite le classi con la classe sottostante l'alias. Per impostazione predefinita, l'output viene restituito in formato HTML.

Il verbo ASSOC include le opzioni seguenti.



| Opzione                         | Descrizione                                                                                                       |
|--------------------------------|-------------------------------------------------------------------------------------------------------------------|
| /RESULTCLASS: &lt; classname&gt; | Gli endpoint restituiti associati all'oggetto di origine devono appartenere o essere derivati dalla classe specificata.      |
| /RESULTROLE: &lt; rolename&gt;   | Gli endpoint restituiti devono svolgere un ruolo specifico nelle associazioni con l'oggetto di origine.                              |
| /ASSOCCLASS: &lt; assocclass&gt; | Gli endpoint restituiti devono essere associati all'origine tramite la classe specificata o una delle classi derivate. |



 

Esempio: **ASSOC del sistema operativo**

</dd> <dt>

<span id="CALL"></span><span id="call"></span>CHIAMARE
</dt> <dd>

Esegue un metodo.

Esempio: **SERVICE WHERE CAPTION='TELNET' CALL STARTSERVICE**

> [!Note]  
> Per determinare i metodi disponibili per una determinata classe, usare **/?**. Ad esempio, **SERVICE WHERE CAPTION='TELNET' CALL /?** elenca le funzioni disponibili per la classe di servizio.

 

</dd> <dt>

<span id="CREATE"></span><span id="create"></span>CREARE
</dt> <dd>

Crea una nuova istanza di e imposta i valori delle proprietà. Non è possibile usare CREATE per creare una nuova classe.

Esempio: **ENVIRONMENT CREATE NAME="TEMP"; VARIABLEVALUE="NEW"**

</dd> <dt>

<span id="DELETE"></span><span id="delete"></span>ELIMINA
</dt> <dd>

Elimina l'istanza corrente o il set di istanze. È possibile usare DELETE per eliminare una classe.

Esempio: **PROCESS WHERE NAME="CALC.EXE" DELETE**

</dd> <dt>

<span id="GET"></span><span id="get"></span>OTTIENI
</dt> <dd>

Recuperare valori di proprietà specifici.

GET include le opzioni seguenti.



| Opzione                               | Descrizione                                                                                                                                |
|--------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| /VALUE                               | L'output viene formattato con ogni valore elencato in una riga separata e con il nome della proprietà .                                           |
| /ALL                                 | L'output viene formattato come tabella.                                                                                                            |
| /TRANSLATE:<translation table> | Tradurre l'output usando la tabella di conversione denominata dal comando . Le tabelle di conversione BasicXml e NoComma sono incluse in WMIC. |
| /EVERY: &lt; intervallo&gt;              | Ripetere il comando a &lt; intervalli &gt; di secondi.                                                                                         |
| /FORMAT:<format specifier>     | Specifica una parola chiave o un nome di file XSL per formattare i dati.                                                                                  |



 

Esempio: **PROCESS GET NAME**

</dd> <dt>

<span id="LIST"></span><span id="list"></span>ELENCO
</dt> <dd>

Mostra i dati. LIST è il verbo predefinito.

LIST include gli avverbi seguenti.



| Avverbio   | Descrizione                                                  |
|----------|--------------------------------------------------------------|
| RIASSUNTO    | Set di base delle proprietà.                                  |
| FULL     | Set completo di proprietà. Si tratta dell'avverbio predefinito per LIST. |
| INSTANCE | Solo percorsi di istanza.                                         |
| STATO   | Stato degli oggetti.                                       |
| SYSTEM   | Proprietà di sistema.                                           |



 

LIST include le opzioni seguenti.



| Opzione                               | Descrizione                                                                                                                                |
|--------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| /TRANSLATE:<translation table> | Tradurre l'output usando la tabella di conversione denominata dal comando . Le tabelle di conversione BasicXml e NoComma sono incluse in WMIC. |
| /EVERY: &lt; intervallo&gt;              | Ripetere il comando a &lt; intervalli &gt; di secondi.                                                                                         |
| /FORMAT:<format specifier>     | Specifica una parola chiave o un nome di file XSL per formattare i dati.                                                                                  |



 

Esempio: **PROCESS LIST BRIEF**

</dd> <dt>

<span id="SET"></span><span id="set"></span>IMPOSTARE
</dt> <dd>

Assegna valori alle proprietà. Esempio: **ENVIRONMENT SET NAME="TEMP",** **VARIABLEVALUE="NEW"**

</dd> </dl>

## <a name="switches"></a>Commutatori

Le opzioni globali vengono usate per impostare le impostazioni predefinite per l'ambiente WMIC. È possibile visualizzare il valore corrente delle condizioni impostate da queste opzioni immettendo il **comando CONTEXT.**

<dl> <dt>

<span id="_NAMESPACE"></span><span id="_namespace"></span>/NAMESPACE
</dt> <dd>

Spazio dei nomi usato in genere dall'alias. Il valore predefinito è root \\ cimv2.

Esempio: **/NAMESPACE: \\ \\ root**

</dd> <dt>

<span id="_ROLE"></span><span id="_role"></span>/ROLE
</dt> <dd>

WMIC dello spazio dei nomi cerca in genere alias e altre informazioni WMIC.

Esempio: **/ROLE: \\ \\ root**

</dd> <dt>

<span id="_NODE"></span><span id="_node"></span>/NODE
</dt> <dd>

Nomi di computer delimitati da virgole. Tutti i comandi vengono eseguiti in modo sincrono su tutti i computer elencati in questo valore. I nomi di file devono essere preceduti da &. I nomi dei computer all'interno di un file devono essere delimitati da virgole o su righe separate.

</dd> <dt>

<span id="_IMPLEVEL"></span><span id="_implevel"></span>/IMPLEVEL
</dt> <dd>

Livello di rappresentazione.

Esempio: **/IMPLEVEL:Anonymous**

</dd> <dt>

<span id="_AUTHLEVEL"></span><span id="_authlevel"></span>/AUTHLEVEL
</dt> <dd>

Livello di autenticazione.

Esempio: **/AUTHLEVEL:Pkt**

</dd> <dt>

<span id="_LOCALE"></span><span id="_locale"></span>/LOCALE
</dt> <dd>

Impostazioni internazionali.

Esempio: **/LOCALE:MS \_ 411**

</dd> <dt>

<span id="_PRIVILEGES"></span><span id="_privileges"></span>/PRIVILEGES
</dt> <dd>

Abilitare o disabilitare tutti i privilegi.

Esempio: **/PRIVILEGES:ENABLE** o **/PRIVILEGES:DISABLE**

</dd> <dt>

<span id="_TRACE"></span><span id="_trace"></span>/TRACE
</dt> <dd>

Consente di visualizzare l'esito positivo o negativo di tutte le funzioni usate per eseguire i comandi WMIC.

Esempio: **/TRACE:ON** o **/TRACE:OFF**

</dd> <dt>

<span id="_RECORD"></span><span id="_record"></span>/RECORD
</dt> <dd>

Registra tutto l'output in un file XML. L'output viene visualizzato anche al prompt dei comandi.

Esempio: **/RECORD:** _MyOutput.xml_

</dd> <dt>

<span id="_INTERACTIVE"></span><span id="_interactive"></span>/INTERACTIVE
</dt> <dd>

In genere, i comandi di eliminazione vengono confermati.

Esempio: **/INTERACTIVE:ON** o **/INTERACTIVE:OFF**

</dd> <dt>

<span id="_FAILFAST_on_off_TimeoutInMilliseconds"></span><span id="_failfast_on_off_timeoutinmilliseconds"></span><span id="_FAILFAST_ON_OFF_TIMEOUTINMILLISECONDS"></span>/FAILFAST **on** \| **off** \| *TimeoutInMilliseconds*
</dt> <dd>

Se nei computer /NODE viene emittente il ping dei computer prima di inviare comandi WMIC. Se un computer non risponde, i comandi WMIC non vengono inviati.

Esempio: "/FAILFAST:ON" o "/FAILFAST:OFF"

**WMIC /FAILFAST:1000**

</dd> <dt>

<span id="_USER"></span><span id="_user"></span>/USER
</dt> <dd>

Nome utente utilizzato da WMIC quando si accede ai computer /NODE o ai computer specificati negli alias. Verrà richiesto di specificare la password. Non è possibile usare un nome utente con il computer locale.

Esempio: **/USER:**_JSMITH_

</dd> <dt>

<span id="_PASSWORD"></span><span id="_password"></span>/PASSWORD
</dt> <dd>

Password usata da WMIC quando si accede ai computer /NODE. La password è visibile nella riga di comando.

Esempio: **/PASSWORD:**_password_

</dd> <dt>

<span id="_OUTPUT"></span><span id="_output"></span>/OUTPUT
</dt> <dd>

Specifica una modalità per tutti i reindirizzamenti di output. L'output non viene visualizzato nella riga di comando e la destinazione viene cancellata prima dell'inizio dell'output. I valori validi sono STDOUT, CLIPBOARD o un nome di file.

Esempio: **/OUTPUT:CLIPBOARD**

</dd> <dt>

<span id="_APPEND"></span><span id="_append"></span>/APPEND
</dt> <dd>

Specifica una modalità per tutti i reindirizzamenti di output. L'output non viene visualizzato nella riga di comando e la destinazione non viene cancellata prima dell'inizio dell'output e l'output viene aggiunto alla fine del contenuto corrente della destinazione. I valori validi sono STDOUT, CLIPBOARD o un nome di file.

Esempio: **/APPEND:CLIPBOARD**

</dd> <dt>

<span id="_AGGREGATE"></span><span id="_aggregate"></span>/AGGREGATE
</dt> <dd>

Usato con **l'opzione LIST** **e GET /EVERY.** Se AGGREGATE è ON, LIST e GET visualizzano i risultati quando tutti i computer in /NODE hanno risposto o hanno avuto un timeout. Se AGGREGATE è OFF, LIST e GET visualizzano i risultati non appena vengono ricevuti.

Esempio: **/AGGREGATE:OFF** o **/AGGREGATE:ON**

</dd> </dl>

## <a name="commands"></a>Comandi

I comandi WMIC seguenti sono sempre disponibili. Per altre informazioni, vedere [Comandi WMIC](/previous-versions/windows/it-pro/windows-server-2003/cc779647(v=ws.10)).

<dl> <dt>

<span id="CLASS"></span><span id="class"></span>CLASSE
</dt> <dd>

Eseguire l'escape dalla modalità alias predefinita di WMIC per accedere direttamente alle classi nello schema WMI. Per altre informazioni sulle classi WMI disponibili, vedere [Classi WMI](wmi-classes.md).

Esempio: **WMIC /OUTPUT:c:ClassOutput.htm \\ CLASS Win32 \_ SoundDevice**

</dd> <dt>

<span id="PATH"></span><span id="path"></span>PERCORSO
</dt> <dd>

Eseguire l'escape dalla modalità alias predefinita di WMIC per accedere direttamente alle istanze nello schema WMI.

Esempio: **WMIC /OUTPUT:c: \\PathOutput.txt PATH Win32 \_ SoundDevice GET /VALUE**

</dd> <dt>

<span id="CONTEXT"></span><span id="context"></span>CONTESTO
</dt> <dd>

Visualizzare i valori correnti di tutte le opzioni globali.

Esempio: **WMIC CONTEXT**

</dd> <dt>

<span id="QUIT"></span><span id="quit"></span>SMETTERE
</dt> <dd>

Uscire da WMIC.

Esempio: **WMIC QUIT**

</dd> <dt>

<span id="EXIT"></span><span id="exit"></span>USCITA
</dt> <dd>

Uscire da WMIC.

Esempio: **WMIC EXIT**

</dd> </dl>

## <a name="examples"></a>Esempio

L'esempio Script per l'impostazione di [IP/Subnet/Gateway/DNS](https://Gallery.TechNet.Microsoft.Com/Batch-per-settare-487c1b3f) con wmic in TechNet Gallery descrive come modificare e aggiornare le impostazioni IP, Subnet, Gateway e DNS.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>       |
| Server minimo supportato<br/> | Windows Server 2008<br/> |



 

