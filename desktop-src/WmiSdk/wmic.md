---
description: L'utilità della riga di comando WMI (WMIC) fornisce un'interfaccia della riga di comando per WMI.
ms.assetid: a0f5c1e2-9a4d-4c2b-b324-58ec01e67b6e
ms.tgt_platform: multiple
title: wmic
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 070b21cb21381fb989b81795a6c7e0b787b5c89a
ms.sourcegitcommit: 556bf3a984f2fc4d18e370329c3043bf3329c93f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/09/2021
ms.locfileid: "107222929"
---
# <a name="wmic"></a>wmic

L'utilità della riga di comando WMI (WMIC) fornisce un'interfaccia della riga di comando per Strumentazione gestione Windows (WMI). WMIC è compatibile con le shell e i comandi di utilità esistenti. Di seguito è riportato un argomento di riferimento generale per WMIC. Per ulteriori informazioni e linee guida su come utilizzare WMIC, incluse informazioni aggiuntive sugli alias, i verbi, i commutatori e i comandi, vedere [utilizzo Strumentazione gestione Windows riga di comando](/previous-versions/windows/it-pro/windows-server-2003/cc779482(v=ws.10)) e il [controllo della riga di comando WMIC-take su WMI](/previous-versions/windows/it-pro/windows-2000-server/bb742610(v=technet.10)).

## <a name="alias"></a>Alias

Un alias è una ridenominazione descrittiva di una classe, di una proprietà o di un metodo che rende più semplice l'utilizzo e la lettura di WMI. È possibile determinare quali alias sono disponibili per WMIC tramite **/?** . È inoltre possibile determinare gli alias per una classe specifica utilizzando **<className> /?** . Per ulteriori informazioni, vedere gli [Alias WMIC](/previous-versions/windows/it-pro/windows-server-2003/cc736307(v=ws.10)).

## <a name="switch"></a>Opzione

Un'opzione è un'opzione WMIC che è possibile impostare a livello globale o facoltativo. Per un elenco delle opzioni disponibili, vedere [Opzioni WMIC](/previous-versions/windows/it-pro/windows-server-2003/cc787035(v=ws.10)).

## <a name="verbs"></a>Verbi

Per utilizzare i verbi in WMIC, immettere il nome dell'alias seguito dal verbo. Se un alias non supporta un verbo, viene visualizzato il messaggio "provider non è in grado di eseguire l'operazione tentata". Per ulteriori informazioni, vedere la pagina relativa ai [verbi WMIC](/previous-versions/windows/it-pro/windows-server-2003/cc784966(v=ws.10)).

La maggior parte degli alias supporta i verbi seguenti.

<dl> <dt>

<span id="ASSOC"></span><span id="assoc"></span>ASSOC
</dt> <dd>

Restituisce il risultato della `Associators of (<wmi_object>)` query in cui *<\_ oggetto WMI>* è il percorso degli oggetti restituiti dai comandi **path** o **Class** . I risultati sono istanze associate all'oggetto. Quando si utilizza ASSOC con un alias, vengono restituite le classi con la classe sottostante l'alias. Per impostazione predefinita, l'output viene restituito in formato HTML.

Il verbo ASSOC presenta le opzioni seguenti.



| Opzione                         | Descrizione                                                                                                       |
|--------------------------------|-------------------------------------------------------------------------------------------------------------------|
| ResultClass<classname> | Gli endpoint restituiti associati all'oggetto di origine devono appartenere a o essere derivati dalla classe specificata.      |
| RESULTROLE<rolename>   | Gli endpoint restituiti devono riprodurre un ruolo specifico nelle associazioni con l'oggetto di origine.                              |
| AssocClass<assocclass> | Gli endpoint restituiti devono essere associati all'origine tramite la classe specificata o una delle relative classi derivate. |



 

Esempio: **sistema operativo Assoc**

</dd> <dt>

<span id="CALL"></span><span id="call"></span>CHIAMARE
</dt> <dd>

Esegue un metodo.

Esempio: **servizio dove Caption =' Telnet ' chiama StartService**

> [!Note]  
> Per determinare i metodi disponibili per una determinata classe, utilizzare **/?**. Ad esempio, il **servizio dove Caption =' Telnet ' chiama/?** elenca le funzioni disponibili per la classe del servizio.

 

</dd> <dt>

<span id="CREATE"></span><span id="create"></span>CREARE
</dt> <dd>

Crea una nuova istanza di e imposta i valori della proprietà. Non è possibile usare CREATE per creare una nuova classe.

Esempio: **Environment create name = "Temp"; VARIABLEVALUE = "nuovo"**

</dd> <dt>

<span id="DELETE"></span><span id="delete"></span>ELIMINARE
</dt> <dd>

Elimina l'istanza o il set di istanze corrente. È possibile utilizzare DELETE per eliminare una classe.

Esempio: **processo con nome = "CALC.EXE" Delete**

</dd> <dt>

<span id="GET"></span><span id="get"></span>Ottieni
</dt> <dd>

Recuperare valori di proprietà specifici.

GET presenta le opzioni seguenti.



| Opzione                               | Descrizione                                                                                                                                |
|--------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| /VALUE                               | L'output viene formattato con ogni valore elencato in una riga separata e con il nome della proprietà.                                           |
| /ALL                                 | L'output viene formattato come tabella.                                                                                                            |
| Tradurre<translation table> | Tradurre l'output usando la tabella di traduzione denominata dal comando. Con WMIC sono incluse le tabelle di conversione BasicXml e novirgole. |
| Ogni<interval>              | Ripetere il comando ogni <interval> secondo.                                                                                         |
| Formato<format specifier>     | Specifica una parola chiave o un nome file XSL per formattare i dati.                                                                                  |



 

Esempio: **processo get Name**

</dd> <dt>

<span id="LIST"></span><span id="list"></span>ELENCO
</dt> <dd>

Mostra i dati. LIST è il verbo predefinito.

L'elenco presenta gli avverbi seguenti.



| Avverbio   | Descrizione                                                  |
|----------|--------------------------------------------------------------|
| RIASSUNTO    | Set principale delle proprietà.                                  |
| FULL     | Set completo di proprietà. Si tratta dell'avverbio predefinito per l'elenco. |
| INSTANCE | Solo percorsi istanza.                                         |
| STATO   | Stato degli oggetti.                                       |
| SYSTEM   | Proprietà di sistema.                                           |



 

ELENCO con le opzioni seguenti.



| Opzione                               | Descrizione                                                                                                                                |
|--------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| Tradurre<translation table> | Tradurre l'output usando la tabella di traduzione denominata dal comando. Con WMIC sono incluse le tabelle di conversione BasicXml e novirgole. |
| Ogni<interval>              | Ripetere il comando ogni <interval> secondo.                                                                                         |
| Formato<format specifier>     | Specifica una parola chiave o un nome file XSL per formattare i dati.                                                                                  |



 

Esempio: **breve elenco processi**

</dd> <dt>

<span id="SET"></span><span id="set"></span>SET
</dt> <dd>

Assegna i valori alle proprietà. Esempio: **Environment set Name = "Temp"**, **VARIABLEVALUE = "New"**

</dd> </dl>

## <a name="switches"></a>Commutatori

Le opzioni globali vengono utilizzate per impostare i valori predefiniti per l'ambiente WMIC. È possibile visualizzare il valore corrente delle condizioni impostate da queste opzioni immettendo il comando di **contesto** .

<dl> <dt>

<span id="_NAMESPACE"></span><span id="_namespace"></span>/NAMESPACE
</dt> <dd>

Spazio dei nomi usato in genere dall'alias. Il valore predefinito è \\ CIMV2 radice.

Esempio: **/namespace: \\ \\ root**

</dd> <dt>

<span id="_ROLE"></span><span id="_role"></span>/ROLE
</dt> <dd>

Il WMIC dello spazio dei nomi in genere cerca gli alias e altre informazioni di WMIC.

Esempio: **/Role: \\ \\ root**

</dd> <dt>

<span id="_NODE"></span><span id="_node"></span>/NODE
</dt> <dd>

Nomi computer, delimitati da virgole. Tutti i comandi vengono eseguiti in modo sincrono su tutti i computer elencati in questo valore. I nomi file devono essere preceduti dal prefisso &. I nomi di computer all'interno di un file devono essere delimitati da virgole o su righe separate.

</dd> <dt>

<span id="_IMPLEVEL"></span><span id="_implevel"></span>/IMPLEVEL
</dt> <dd>

Livello di rappresentazione.

Esempio: **/IMPLEVEL: Anonymous**

</dd> <dt>

<span id="_AUTHLEVEL"></span><span id="_authlevel"></span>/AUTHLEVEL
</dt> <dd>

Livello di autenticazione.

Esempio: **/AUTHLEVEL: PKT**

</dd> <dt>

<span id="_LOCALE"></span><span id="_locale"></span>/LOCALE
</dt> <dd>

Locale.

Esempio: **/locale: MS \_ 411**

</dd> <dt>

<span id="_PRIVILEGES"></span><span id="_privileges"></span>/PRIVILEGES
</dt> <dd>

Abilitare o disabilitare tutti i privilegi.

Esempio: **/privileges: Enable** o **/privileges: Disable**

</dd> <dt>

<span id="_TRACE"></span><span id="_trace"></span>/TRACE
</dt> <dd>

Consente di visualizzare l'esito positivo o negativo di tutte le funzioni utilizzate per eseguire i comandi WMIC.

Esempio: **/Trace: on** o **/Trace: off**

</dd> <dt>

<span id="_RECORD"></span><span id="_record"></span>/RECORD
</dt> <dd>

Registra tutti gli output in un file XML. L'output viene visualizzato anche al prompt dei comandi.

Esempio: **/record:** _MyOutput.xml_

</dd> <dt>

<span id="_INTERACTIVE"></span><span id="_interactive"></span>/INTERACTIVE
</dt> <dd>

In genere, vengono confermati i comandi DELETE.

Esempio: **/Interactive: on** o **/Interactive: off**

</dd> <dt>

<span id="_FAILFAST_on_off_TimeoutInMilliseconds"></span><span id="_failfast_on_off_timeoutinmilliseconds"></span><span id="_FAILFAST_ON_OFF_TIMEOUTINMILLISECONDS"></span>/FailFast  \| **off** \| *TimeoutInMilliseconds*
</dt> <dd>

Se nei computer/NODE viene ping prima di inviare comandi WMIC. Se un computer non risponde, i comandi WMIC non vengono inviati.

Esempio: "/FAILFAST: ON" o "/FAILFAST: OFF"

**/FAILFAST WMIC: 1000**

</dd> <dt>

<span id="_USER"></span><span id="_user"></span>/USER
</dt> <dd>

Nome utente utilizzato da WMIC durante l'accesso ai computer o ai computer/NODE specificati negli alias. Verrà richiesto di specificare la password. Non è possibile usare un nome utente con il computer locale.

Esempio: **/User:**_jsmith_

</dd> <dt>

<span id="_PASSWORD"></span><span id="_password"></span>/PASSWORD
</dt> <dd>

Password utilizzata da WMIC durante l'accesso ai computer/NODE. La password è visibile nella riga di comando.

Esempio: **/password:**_password_

</dd> <dt>

<span id="_OUTPUT"></span><span id="_output"></span>/OUTPUT
</dt> <dd>

Specifica una modalità per tutto il reindirizzamento dell'output. L'output non viene visualizzato nella riga di comando e la destinazione viene cancellata prima dell'inizio dell'output. I valori validi sono STDOUT, appunti o un nome file.

Esempio: **/output: appunti**

</dd> <dt>

<span id="_APPEND"></span><span id="_append"></span>/APPEND
</dt> <dd>

Specifica una modalità per tutto il reindirizzamento dell'output. L'output non viene visualizzato nella riga di comando e la destinazione non viene cancellata prima dell'inizio dell'output e l'output viene accodato alla fine del contenuto corrente della destinazione. I valori validi sono STDOUT, appunti o un nome file.

Esempio: **/append: appunti**

</dd> <dt>

<span id="_AGGREGATE"></span><span id="_aggregate"></span>/AGGREGATE
</dt> <dd>

Utilizzato con l'opzione **List** e **Get/every** . Se l'AGGREGAzione è ON, LIST e GET visualizzano i risultati quando tutti i computer del/NODE hanno risposto o si è verificato il timeout. Se l'AGGREGAzione è disattivata, LIST e GET visualizzano i risultati non appena vengono ricevuti.

Esempio: **/Aggregate: off** o **/Aggregate: on**

</dd> </dl>

## <a name="commands"></a>Comandi

I comandi WMIC seguenti sono sempre disponibili. Per ulteriori informazioni, vedere [comandi WMIC](/previous-versions/windows/it-pro/windows-server-2003/cc779647(v=ws.10)).

<dl> <dt>

<span id="CLASS"></span><span id="class"></span>CLASSE
</dt> <dd>

Eseguire l'escape dalla modalità alias predefinita di WMIC per accedere direttamente alle classi nello schema WMI. Per ulteriori informazioni sulle classi WMI disponibili, vedere [classi WMI](wmi-classes.md).

Esempio: **wmic/output: c: \\ClassOutput.htm classe Win32 \_ SoundDevice**

</dd> <dt>

<span id="PATH"></span><span id="path"></span>PERCORSO
</dt> <dd>

Eseguire l'escape dalla modalità alias predefinita di WMIC per accedere direttamente alle istanze nello schema WMI.

Esempio: **wmic/output: c: \\PathOutput.txt percorso Win32 \_ SoundDevice get/value**

</dd> <dt>

<span id="CONTEXT"></span><span id="context"></span>CONTESTO
</dt> <dd>

Consente di visualizzare i valori correnti di tutti i commutatori globali.

Esempio: **contesto WMIC**

</dd> <dt>

<span id="QUIT"></span><span id="quit"></span>QUIT
</dt> <dd>

Uscire da WMIC.

Esempio: **wmic Quit**

</dd> <dt>

<span id="EXIT"></span><span id="exit"></span>USCITA
</dt> <dd>

Uscire da WMIC.

Esempio: **uscita WMIC**

</dd> </dl>

## <a name="examples"></a>Esempio

Lo [script per l'impostazione di IP/subnet/gateway/DNS con](https://Gallery.TechNet.Microsoft.Com/Batch-per-settare-487c1b3f) l'esempio WMIC nella raccolta TechNet descrive come modificare e aggiornare le impostazioni IP, subnet, gateway e DNS.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>       |
| Server minimo supportato<br/> | Windows Server 2008<br/> |



 

