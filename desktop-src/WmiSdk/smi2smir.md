---
description: Il compilatore SNMP viene eseguito come un unico file eseguibile nella modalità da riga di comando.
ms.assetid: 0e85fe84-dacb-4720-8242-ffa0046780f3
ms.tgt_platform: multiple
title: smi2smir
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a34e1d757293b5ee128f2ce1bc2bd5ec8479d9b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233811"
---
# <a name="smi2smir"></a>smi2smir

Il compilatore SNMP viene eseguito come un unico file eseguibile nella modalità da riga di comando. Il compilatore accetta un modulo di informazioni SNMP come input e accetta eventuali moduli aggiuntivi necessari per risolvere i riferimenti esterni. Usare uno dei seguenti esempi di sintassi della riga di comando.

Per ulteriori informazioni sul momento in cui viene utilizzato il compilatore, vedere [configurazione dell'ambiente WMI SNMP](setting-up-the-wmi-snmp-environment.md).

``` syntax
smi2smir [<DiagnosticArgs>] [<VersionArgs>]
     <CommandArgs> <MIB file> [<Import Files>]

smi2smir [<DiagnosticArgs>] <RegistryArgs> [<Directory>]

smi2smir <ModuleInfoArgs> <MIB file>

smi2smir <HelpArgs>
```

## <a name="switches"></a>Commutatori

<dl> <dt>

<span id="_DiagnosticArgs_"></span><span id="_diagnosticargs_"></span><span id="_DIAGNOSTICARGS_"></span><*DiagnosticArgs*>
</dt> <dd>

Il compilatore accetta i seguenti argomenti di diagnostica.

<dl> <dt>

<span id="_m__diagnostic-level_"></span><span id="_M__DIAGNOSTIC-LEVEL_"></span>**/m** **<** _a livello di diagnostica_*_>_*
</dt> <dd>

Tipo di diagnostica da visualizzare. Il valore predefinito è 2.

Di seguito è riportato un elenco dei valori del livello di diagnostica che è possibile impostare:

-   0 = invisibile all'utente
-   1 = irreversibile
-   2 = irreversibile e avviso
-   3 = messaggi irreversibili, di avviso e informativi

</dd> <dt>

<span id="_c__count_"></span><span id="_C__COUNT_"></span>**/c** **<** _numero_ di *_>_*
</dt> <dd>

Numero massimo di messaggi irreversibili e di avviso da visualizzare. *count* deve essere un Integer positivo decimale. Se **/c** non è specificato, non esiste alcun limite al numero di errori che possono essere segnalati.

</dd> </dl> </dd> <dt>

<span id="_VersionArgs_"></span><span id="_versionargs_"></span><span id="_VERSIONARGS_"></span><*VersionArgs*>
</dt> <dd>

Il compilatore accetta gli argomenti della versione seguenti.

<dl> <dt>

<span id="_v1"></span><span id="_V1"></span>**/v1**
</dt> <dd>

Specifica una conformità rigorosa a SNMPv1 SMI. Il compilatore segnala un errore se rileva istruzioni non SNMPv1.

</dd> <dt>

<span id="_v2c"></span><span id="_V2C"></span>**/v2c**
</dt> <dd>

Specifica una conformità rigorosa a SNMPv2 SMI. Il compilatore segnala un errore se rileva istruzioni non SNMPv2.

</dd> </dl> </dd> <dt>

<span id="_CommandArgs_"></span><span id="_commandargs_"></span><span id="_COMMANDARGS_"></span><*CommandArgs*>
</dt> <dd>

Il compilatore accetta gli argomenti di comando seguenti.

<dl> <dt>

<span id="_d"></span><span id="_D"></span>**/d**
</dt> <dd>

Elimina il modulo specificato da archivio SMIR.

</dd> <dt>

<span id="_p"></span><span id="_P"></span>**/p**
</dt> <dd>

Elimina tutti i moduli di archivio SMIR.

</dd> <dt>

<span id="_l"></span><span id="_L"></span>**/l**
</dt> <dd>

Elenca tutti i moduli di archivio SMIR.

</dd> <dt>

<span id="_lc"></span><span id="_LC"></span>**/lc**
</dt> <dd>

Esegue un controllo della sintassi locale sul modulo.

</dd> <dt>

<span id="_ec___CommandModifier__"></span><span id="_ec___commandmodifier__"></span><span id="_EC___COMMANDMODIFIER__"></span>**/CE** **\[<** _CommandModifier_*_>\]_*
</dt> <dd>

Esegue controlli locali ed esterni sul modulo.

</dd> <dt>

<span id="_a__CommandModifier__"></span><span id="_a__commandmodifier__"></span><span id="_A__COMMANDMODIFIER__"></span>**\[ /a <** _CommandModifier_*_>\]_*
</dt> <dd>

Esegue controlli locali ed esterni e carica il modulo in archivio SMIR.

</dd> <dt>

<span id="_sa__CommandModifier__"></span><span id="_sa__commandmodifier__"></span><span id="_SA__COMMANDMODIFIER__"></span>**\[ /sa <** _CommandModifier_*_>\]_*
</dt> <dd>

Uguale a **/a**, ma funziona in modo invisibile all'utente.

</dd> <dt>

<span id="_g__CommandModifier__"></span><span id="_g__commandmodifier__"></span><span id="_G__COMMANDMODIFIER__"></span>**\[ /g <** _CommandModifier_*_>\]_*
</dt> <dd>

Genera un file archivio SMIR. mof che è possibile caricare in un secondo momento in WMI utilizzando il compilatore MOF. Utilizzato dal provider di classi SNMP per fornire classi in modo dinamico a uno o più spazi dei nomi. Usare questa opzione quando non si sa quali MIB sono supportati dai dispositivi SNMP gestiti. Il provider di classi SNMP Controlla il dispositivo in fase di esecuzione per la presenza di questo MIB e fornisce le classi in modo dinamico allo spazio dei nomi.

</dd> <dt>

<span id="_gc__CommandModifier__"></span><span id="_gc__commandmodifier__"></span><span id="_GC__COMMANDMODIFIER__"></span>**\[ /GC <** _CommandModifier_*_>\]_*
</dt> <dd>

Genera un file MOF statico che può essere caricato in un secondo momento in WMI come classi statiche per un determinato spazio dei nomi. Usare questa opzione quando si sa quali MIB sono supportati dai dispositivi SNMP gestiti. È possibile definire il file con estensione MOF da generare indirizzando l'output del comando a un file specificato. Non usare with **/ext/o**.

</dd> </dl> </dd> <dt>

<span id="_CommandModifiers_"></span><span id="_commandmodifiers_"></span><span id="_COMMANDMODIFIERS_"></span><*CommandModifiers*>
</dt> <dd>

Il compilatore accetta i seguenti modificatori di comando.

<dl> <dt>

<span id="_i_directory_"></span><span id="_I_DIRECTORY_"></span>**/i<** _directory_*_>_*
</dt> <dd>

Specifica una directory in cui eseguire la ricerca dei moduli MIB dipendenti. Usare con **/a**, **/CE**, **/g**, **/GC** e **/sa**. L'opzione **/i** può apparire più volte nel comando; viene eseguita la ricerca nelle directory nell'ordine specificato nel comando.

</dd> <dt>

<span id="_ch"></span><span id="_CH"></span>**/ch**
</dt> <dd>

Genera informazioni sul contesto, ad esempio la data, l'ora, l'host o l'utente, nell'intestazione del file MOF. Usare con **/g** e **/GC**.

</dd> <dt>

<span id="_t"></span><span id="_T"></span>**/t**
</dt> <dd>

Genera le classi [SnmpNotification](snmpnotification.md) . Usare con **/a**, **/g** e **/sa**.

</dd> <dt>

<span id="_ext"></span><span id="_EXT"></span>**/EXT**
</dt> <dd>

Genera le classi [SnmpExtendedNotification](snmpextendednotification.md) . Usare con **/a**, **/g** e **/sa**.

</dd> <dt>

<span id="_t_o"></span><span id="_T_O"></span>**/t/o**
</dt> <dd>

Genera solo le classi [SnmpNotification](snmpnotification.md) . Usare con **/a**, **/g** e **/sa**.

</dd> <dt>

<span id="_ext_o"></span><span id="_EXT_O"></span>**/ext/o**
</dt> <dd>

Genera solo le classi [SnmpExtendedNotification](snmpextendednotification.md) . Usare con **/a**, **/g** e **/sa**.

</dd> <dt>

<span id="_s"></span><span id="_S"></span>**/s**
</dt> <dd>

Non esegue il mapping del testo della clausola DESCRIPTION. Usare con **/a**, **/g**, **/GC** e **/sa**. Utilizzare questa opzione se si desidera ridurre al minimo i requisiti di archiviazione.

</dd> <dt>

<span id="_auto"></span><span id="_AUTO"></span>**/auto**
</dt> <dd>

Ricompila la tabella di ricerca MIB prima di completare il <opzione di> *CommandArg* . Usare con **/a**, **/CE**, **/g** e **/GC**.

</dd> </dl> </dd> <dt>

<span id="_RegistryArgs_"></span><span id="_registryargs_"></span><span id="_REGISTRYARGS_"></span><*RegistryArgs*>
</dt> <dd>

Il compilatore accetta gli argomenti del registro di sistema seguenti.

<dl> <dt>

<span id="_pa"></span><span id="_PA"></span>**/PA**
</dt> <dd>

Aggiunge la directory specificata al registro di sistema. Il valore predefinito è la directory corrente.

</dd> <dt>

<span id="_pd"></span><span id="_PD"></span>**/PD**
</dt> <dd>

Elimina la directory specificata dal registro di sistema. Il valore predefinito è la directory corrente.

</dd> <dt>

<span id="_pl"></span><span id="_PL"></span>**/pl**
</dt> <dd>

Elenca le directory di ricerca MIB nel registro di sistema.

</dd> <dt>

<span id="_r"></span><span id="_R"></span>**/r**
</dt> <dd>

Ricompila l'intera tabella di ricerca MIB.

</dd> </dl> </dd> <dt>

<span id="_ModuleInfoArgs_"></span><span id="_moduleinfoargs_"></span><span id="_MODULEINFOARGS_"></span><*ModuleInfoArgs*>
</dt> <dd>

Il compilatore accetta gli argomenti di informazioni sui moduli seguenti.

<dl> <dt>

<span id="_n"></span><span id="_N"></span>**/n**
</dt> <dd>

Restituisce il nome ASN. 1 del modulo specificato.

</dd> <dt>

<span id="_ni"></span><span id="_NI"></span>**/ni**
</dt> <dd>

Restituisce i nomi ASN. 1 di tutti i moduli di importazione a cui fa riferimento il modulo di input.

</dd> </dl> </dd> <dt>

<span id="_HelpArgs_"></span><span id="_helpargs_"></span><span id="_HELPARGS_"></span><*HelpArgs*>
</dt> <dd>

Il compilatore accetta gli argomenti della guida seguenti.

<dl> <dt>

<span id="_h"></span><span id="_H"></span>**/h**
</dt> <dd>

Visualizza la guida sulla sintassi del compilatore SNMP.

</dd> <dt>

<span id="__"></span>**/?**
</dt> <dd>

Visualizza la guida sulla sintassi del compilatore SNMP.

</dd> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

I moduli di informazioni SNMP sono scritti in un subset di Abstract Syntax Notation One (ASN. 1) il compilatore esegue le funzioni seguenti:

-   Carica i dati dal modulo informazioni SNMP.
-   Esegue operazioni di controllo nel modulo di informazioni. Ad esempio, controlla la sintassi locale e controlla i riferimenti esterni rispetto alle informazioni nei moduli sussidiari.
-   Rimuove tutti i dati precedentemente caricati dall'archivio SMIR o i dati caricati da un modulo di informazioni.
-   Restituisce il nome del modulo ASN. 1 di un file specificato o restituisce i nomi di modulo ASN. 1 di tutti i moduli importati in un file specificato.
-   Restituisce i nomi di modulo ASN.1 di tutti i moduli di informazioni SNMP attualmente caricati nell'archivio SMIR.
-   Esegue la risoluzione automatica dei moduli importati anziché richiedere agli utenti di specificare manualmente i moduli richiesti.
-   Esegue una modalità di caricamento invisibile all'utente che non genera alcun output, ma può essere usata per caricare i dati in archivio SMIR durante un'operazione di installazione.
-   Restituisce i dati dal modulo informazioni SNMP in archivio SMIR.
-   Crea facoltativamente un file MOF statico o archivio SMIR contenente l'output del modulo informazioni.

    Se necessario, è possibile caricare il file static. mof in uno spazio dei nomi WMI. Un file archivio SMIR. mof contiene il nome dello spazio dei nomi SNMP in cui devono risiedere le classi.

## <a name="examples"></a>Esempio

Nell'esempio seguente il file Pra. mof viene definito come output del file Pra. MIB.

``` syntax
smi2smir /m 3 /v1 /gc /pra.mib > pra.mof
```

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>       |
| Server minimo supportato<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Messaggi di errore del compilatore SNMP](snmp-compiler-error-messages.md)
</dt> <dt>

[Configurazione dell'ambiente WMI SNMP](setting-up-the-wmi-snmp-environment.md)
</dt> <dt>

[Accesso ai dispositivi SNMP](accessing-snmp-devices.md)
</dt> </dl>

 

 




