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
# <a name="smi2smir"></a><span data-ttu-id="60fc7-103">smi2smir</span><span class="sxs-lookup"><span data-stu-id="60fc7-103">smi2smir</span></span>

<span data-ttu-id="60fc7-104">Il compilatore SNMP viene eseguito come un unico file eseguibile nella modalità da riga di comando.</span><span class="sxs-lookup"><span data-stu-id="60fc7-104">The SNMP compiler runs as a single executable file in the command-line mode.</span></span> <span data-ttu-id="60fc7-105">Il compilatore accetta un modulo di informazioni SNMP come input e accetta eventuali moduli aggiuntivi necessari per risolvere i riferimenti esterni.</span><span class="sxs-lookup"><span data-stu-id="60fc7-105">The compiler accepts one SNMP information module as input, and accepts any additional modules necessary to resolve external references.</span></span> <span data-ttu-id="60fc7-106">Usare uno dei seguenti esempi di sintassi della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="60fc7-106">Use one of the following command-line syntax examples.</span></span>

<span data-ttu-id="60fc7-107">Per ulteriori informazioni sul momento in cui viene utilizzato il compilatore, vedere [configurazione dell'ambiente WMI SNMP](setting-up-the-wmi-snmp-environment.md).</span><span class="sxs-lookup"><span data-stu-id="60fc7-107">For more information about when this compiler is used, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

``` syntax
smi2smir [<DiagnosticArgs>] [<VersionArgs>]
     <CommandArgs> <MIB file> [<Import Files>]

smi2smir [<DiagnosticArgs>] <RegistryArgs> [<Directory>]

smi2smir <ModuleInfoArgs> <MIB file>

smi2smir <HelpArgs>
```

## <a name="switches"></a><span data-ttu-id="60fc7-108">Commutatori</span><span class="sxs-lookup"><span data-stu-id="60fc7-108">Switches</span></span>

<dl> <span data-ttu-id="60fc7-109"><dt>

<span id="_DiagnosticArgs_"></span><span id="_diagnosticargs_"></span><span id="_DIAGNOSTICARGS_"></span><*DiagnosticArgs*>
</dt> </span><span class="sxs-lookup"><span data-stu-id="60fc7-109"><dt>

<span id="_DiagnosticArgs_"></span><span id="_diagnosticargs_"></span><span id="_DIAGNOSTICARGS_"></span><*DiagnosticArgs*>
</dt> </span></span><dd>

<span data-ttu-id="60fc7-110">Il compilatore accetta i seguenti argomenti di diagnostica.</span><span class="sxs-lookup"><span data-stu-id="60fc7-110">The compiler accepts the following diagnostic arguments.</span></span>

<dl> <dt>

<span data-ttu-id="60fc7-111"><span id="_m__diagnostic-level_"></span><span id="_M__DIAGNOSTIC-LEVEL_"></span>**/m** **<** _a livello di diagnostica_*_>_*</span><span class="sxs-lookup"><span data-stu-id="60fc7-111"><span id="_m__diagnostic-level_"></span><span id="_M__DIAGNOSTIC-LEVEL_"></span>**/m** **<**_diagnostic-level_*_>_*</span></span>
</dt> <dd>

<span data-ttu-id="60fc7-112">Tipo di diagnostica da visualizzare.</span><span class="sxs-lookup"><span data-stu-id="60fc7-112">Type of diagnostics to display.</span></span> <span data-ttu-id="60fc7-113">Il valore predefinito è 2.</span><span class="sxs-lookup"><span data-stu-id="60fc7-113">The default is 2.</span></span>

<span data-ttu-id="60fc7-114">Di seguito è riportato un elenco dei valori del livello di diagnostica che è possibile impostare:</span><span class="sxs-lookup"><span data-stu-id="60fc7-114">The following is a list of the diagnostic level values that can be set:</span></span>

-   <span data-ttu-id="60fc7-115">0 = invisibile all'utente</span><span class="sxs-lookup"><span data-stu-id="60fc7-115">0 = Silent</span></span>
-   <span data-ttu-id="60fc7-116">1 = irreversibile</span><span class="sxs-lookup"><span data-stu-id="60fc7-116">1 = Fatal</span></span>
-   <span data-ttu-id="60fc7-117">2 = irreversibile e avviso</span><span class="sxs-lookup"><span data-stu-id="60fc7-117">2 = Fatal and warning</span></span>
-   <span data-ttu-id="60fc7-118">3 = messaggi irreversibili, di avviso e informativi</span><span class="sxs-lookup"><span data-stu-id="60fc7-118">3 = Fatal, warning, and information messages</span></span>

</dd> <dt>

<span data-ttu-id="60fc7-119"><span id="_c__count_"></span><span id="_C__COUNT_"></span>**/c** **<** _numero_ di *_>_*</span><span class="sxs-lookup"><span data-stu-id="60fc7-119"><span id="_c__count_"></span><span id="_C__COUNT_"></span>**/c** **<**_count_*_>_*</span></span>
</dt> <dd>

<span data-ttu-id="60fc7-120">Numero massimo di messaggi irreversibili e di avviso da visualizzare. *count* deve essere un Integer positivo decimale.</span><span class="sxs-lookup"><span data-stu-id="60fc7-120">Maximum number of fatal and warning messages to display; *count* must be a positive decimal integer.</span></span> <span data-ttu-id="60fc7-121">Se **/c** non è specificato, non esiste alcun limite al numero di errori che possono essere segnalati.</span><span class="sxs-lookup"><span data-stu-id="60fc7-121">If **/c** is not specified, there is no limit to the number of errors that can be reported.</span></span>

<span data-ttu-id="60fc7-122"></dd> </dl> </dd> <dt>

<span id="_VersionArgs_"></span><span id="_versionargs_"></span><span id="_VERSIONARGS_"></span><*VersionArgs*>
</dt> </span><span class="sxs-lookup"><span data-stu-id="60fc7-122"></dd> </dl> </dd> <dt>

<span id="_VersionArgs_"></span><span id="_versionargs_"></span><span id="_VERSIONARGS_"></span><*VersionArgs*>
</dt> </span></span><dd>

<span data-ttu-id="60fc7-123">Il compilatore accetta gli argomenti della versione seguenti.</span><span class="sxs-lookup"><span data-stu-id="60fc7-123">The compiler accepts the following version arguments.</span></span>

<dl> <dt>

<span data-ttu-id="60fc7-124"><span id="_v1"></span><span id="_V1"></span>**/v1**</span><span class="sxs-lookup"><span data-stu-id="60fc7-124"><span id="_v1"></span><span id="_V1"></span>**/v1**</span></span>
</dt> <dd>

<span data-ttu-id="60fc7-125">Specifica una conformità rigorosa a SNMPv1 SMI.</span><span class="sxs-lookup"><span data-stu-id="60fc7-125">Specifies strict conformance to the SNMPv1 SMI.</span></span> <span data-ttu-id="60fc7-126">Il compilatore segnala un errore se rileva istruzioni non SNMPv1.</span><span class="sxs-lookup"><span data-stu-id="60fc7-126">The compiler reports an error if it detects non-SNMPv1 statements.</span></span>

</dd> <dt>

<span data-ttu-id="60fc7-127"><span id="_v2c"></span><span id="_V2C"></span>**/v2c**</span><span class="sxs-lookup"><span data-stu-id="60fc7-127"><span id="_v2c"></span><span id="_V2C"></span>**/v2c**</span></span>
</dt> <dd>

<span data-ttu-id="60fc7-128">Specifica una conformità rigorosa a SNMPv2 SMI.</span><span class="sxs-lookup"><span data-stu-id="60fc7-128">Specifies strict conformance to the SNMPv2 SMI.</span></span> <span data-ttu-id="60fc7-129">Il compilatore segnala un errore se rileva istruzioni non SNMPv2.</span><span class="sxs-lookup"><span data-stu-id="60fc7-129">The compiler reports an error if it detects non-SNMPv2 statements.</span></span>

<span data-ttu-id="60fc7-130"></dd> </dl> </dd> <dt>

<span id="_CommandArgs_"></span><span id="_commandargs_"></span><span id="_COMMANDARGS_"></span><*CommandArgs*>
</dt> </span><span class="sxs-lookup"><span data-stu-id="60fc7-130"></dd> </dl> </dd> <dt>

<span id="_CommandArgs_"></span><span id="_commandargs_"></span><span id="_COMMANDARGS_"></span><*CommandArgs*>
</dt> </span></span><dd>

<span data-ttu-id="60fc7-131">Il compilatore accetta gli argomenti di comando seguenti.</span><span class="sxs-lookup"><span data-stu-id="60fc7-131">The compiler accepts the following command arguments.</span></span>

<dl> <dt>

<span data-ttu-id="60fc7-132"><span id="_d"></span><span id="_D"></span>**/d**</span><span class="sxs-lookup"><span data-stu-id="60fc7-132"><span id="_d"></span><span id="_D"></span>**/d**</span></span>
</dt> <dd>

<span data-ttu-id="60fc7-133">Elimina il modulo specificato da archivio SMIR.</span><span class="sxs-lookup"><span data-stu-id="60fc7-133">Deletes the specified module from the SMIR.</span></span>

</dd> <dt>

<span data-ttu-id="60fc7-134"><span id="_p"></span><span id="_P"></span>**/p**</span><span class="sxs-lookup"><span data-stu-id="60fc7-134"><span id="_p"></span><span id="_P"></span>**/p**</span></span>
</dt> <dd>

<span data-ttu-id="60fc7-135">Elimina tutti i moduli di archivio SMIR.</span><span class="sxs-lookup"><span data-stu-id="60fc7-135">Deletes all modules in the SMIR.</span></span>

</dd> <dt>

<span data-ttu-id="60fc7-136"><span id="_l"></span><span id="_L"></span>**/l**</span><span class="sxs-lookup"><span data-stu-id="60fc7-136"><span id="_l"></span><span id="_L"></span>**/l**</span></span>
</dt> <dd>

<span data-ttu-id="60fc7-137">Elenca tutti i moduli di archivio SMIR.</span><span class="sxs-lookup"><span data-stu-id="60fc7-137">Lists all modules in the SMIR.</span></span>

</dd> <dt>

<span data-ttu-id="60fc7-138"><span id="_lc"></span><span id="_LC"></span>**/lc**</span><span class="sxs-lookup"><span data-stu-id="60fc7-138"><span id="_lc"></span><span id="_LC"></span>**/lc**</span></span>
</dt> <dd>

<span data-ttu-id="60fc7-139">Esegue un controllo della sintassi locale sul modulo.</span><span class="sxs-lookup"><span data-stu-id="60fc7-139">Performs a local syntax check on the module.</span></span>

</dd> <dt>

<span data-ttu-id="60fc7-140"><span id="_ec___CommandModifier__"></span><span id="_ec___commandmodifier__"></span><span id="_EC___COMMANDMODIFIER__"></span>**/CE** **\[<** _CommandModifier_*_>\]_*</span><span class="sxs-lookup"><span data-stu-id="60fc7-140"><span id="_ec___CommandModifier__"></span><span id="_ec___commandmodifier__"></span><span id="_EC___COMMANDMODIFIER__"></span>**/ec** **\[<**_CommandModifier_*_>\]_*</span></span>
</dt> <dd>

<span data-ttu-id="60fc7-141">Esegue controlli locali ed esterni sul modulo.</span><span class="sxs-lookup"><span data-stu-id="60fc7-141">Performs local and external checks on the module.</span></span>

</dd> <dt>

<span data-ttu-id="60fc7-142"><span id="_a__CommandModifier__"></span><span id="_a__commandmodifier__"></span><span id="_A__COMMANDMODIFIER__"></span>**\[ /a <** _CommandModifier_*_>\]_*</span><span class="sxs-lookup"><span data-stu-id="60fc7-142"><span id="_a__CommandModifier__"></span><span id="_a__commandmodifier__"></span><span id="_A__COMMANDMODIFIER__"></span>**/a\[<**_CommandModifier_*_>\]_*</span></span>
</dt> <dd>

<span data-ttu-id="60fc7-143">Esegue controlli locali ed esterni e carica il modulo in archivio SMIR.</span><span class="sxs-lookup"><span data-stu-id="60fc7-143">Performs local and external checks and loads the module into the SMIR.</span></span>

</dd> <dt>

<span data-ttu-id="60fc7-144"><span id="_sa__CommandModifier__"></span><span id="_sa__commandmodifier__"></span><span id="_SA__COMMANDMODIFIER__"></span>**\[ /sa <** _CommandModifier_*_>\]_*</span><span class="sxs-lookup"><span data-stu-id="60fc7-144"><span id="_sa__CommandModifier__"></span><span id="_sa__commandmodifier__"></span><span id="_SA__COMMANDMODIFIER__"></span>**/sa\[<**_CommandModifier_*_>\]_*</span></span>
</dt> <dd>

<span data-ttu-id="60fc7-145">Uguale a **/a**, ma funziona in modo invisibile all'utente.</span><span class="sxs-lookup"><span data-stu-id="60fc7-145">Same as **/a**, but works silently.</span></span>

</dd> <dt>

<span data-ttu-id="60fc7-146"><span id="_g__CommandModifier__"></span><span id="_g__commandmodifier__"></span><span id="_G__COMMANDMODIFIER__"></span>**\[ /g <** _CommandModifier_*_>\]_*</span><span class="sxs-lookup"><span data-stu-id="60fc7-146"><span id="_g__CommandModifier__"></span><span id="_g__commandmodifier__"></span><span id="_G__COMMANDMODIFIER__"></span>**/g\[<**_CommandModifier_*_>\]_*</span></span>
</dt> <dd>

<span data-ttu-id="60fc7-147">Genera un file archivio SMIR. mof che è possibile caricare in un secondo momento in WMI utilizzando il compilatore MOF.</span><span class="sxs-lookup"><span data-stu-id="60fc7-147">Generates a SMIR .mof file that you can later load into WMI using the MOF compiler.</span></span> <span data-ttu-id="60fc7-148">Utilizzato dal provider di classi SNMP per fornire classi in modo dinamico a uno o più spazi dei nomi.</span><span class="sxs-lookup"><span data-stu-id="60fc7-148">Used by the SNMP class provider to provide classes dynamically to one or more namespaces.</span></span> <span data-ttu-id="60fc7-149">Usare questa opzione quando non si sa quali MIB sono supportati dai dispositivi SNMP gestiti.</span><span class="sxs-lookup"><span data-stu-id="60fc7-149">Use this option when you do not know which MIBs are supported by the SNMP devices being managed.</span></span> <span data-ttu-id="60fc7-150">Il provider di classi SNMP Controlla il dispositivo in fase di esecuzione per la presenza di questo MIB e fornisce le classi in modo dinamico allo spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="60fc7-150">The SNMP class provider checks the device at runtime for the presence of this MIB and supplies the classes dynamically to the namespace.</span></span>

</dd> <dt>

<span data-ttu-id="60fc7-151"><span id="_gc__CommandModifier__"></span><span id="_gc__commandmodifier__"></span><span id="_GC__COMMANDMODIFIER__"></span>**\[ /GC <** _CommandModifier_*_>\]_*</span><span class="sxs-lookup"><span data-stu-id="60fc7-151"><span id="_gc__CommandModifier__"></span><span id="_gc__commandmodifier__"></span><span id="_GC__COMMANDMODIFIER__"></span>**/gc\[<**_CommandModifier_*_>\]_*</span></span>
</dt> <dd>

<span data-ttu-id="60fc7-152">Genera un file MOF statico che può essere caricato in un secondo momento in WMI come classi statiche per un determinato spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="60fc7-152">Generates a static .mof file that can be loaded later into WMI as static classes for a particular namespace.</span></span> <span data-ttu-id="60fc7-153">Usare questa opzione quando si sa quali MIB sono supportati dai dispositivi SNMP gestiti.</span><span class="sxs-lookup"><span data-stu-id="60fc7-153">Use this option when you know which MIBs are supported by the SNMP devices being managed.</span></span> <span data-ttu-id="60fc7-154">È possibile definire il file con estensione MOF da generare indirizzando l'output del comando a un file specificato.</span><span class="sxs-lookup"><span data-stu-id="60fc7-154">You can define the .mof file to be generated by directing the output of your command to a specified file.</span></span> <span data-ttu-id="60fc7-155">Non usare with **/ext/o**.</span><span class="sxs-lookup"><span data-stu-id="60fc7-155">Do not use with **/ext/o**.</span></span>

<span data-ttu-id="60fc7-156"></dd> </dl> </dd> <dt>

<span id="_CommandModifiers_"></span><span id="_commandmodifiers_"></span><span id="_COMMANDMODIFIERS_"></span><*CommandModifiers*>
</dt> </span><span class="sxs-lookup"><span data-stu-id="60fc7-156"></dd> </dl> </dd> <dt>

<span id="_CommandModifiers_"></span><span id="_commandmodifiers_"></span><span id="_COMMANDMODIFIERS_"></span><*CommandModifiers*>
</dt> </span></span><dd>

<span data-ttu-id="60fc7-157">Il compilatore accetta i seguenti modificatori di comando.</span><span class="sxs-lookup"><span data-stu-id="60fc7-157">The compiler accepts the following command modifiers.</span></span>

<dl> <dt>

<span data-ttu-id="60fc7-158"><span id="_i_directory_"></span><span id="_I_DIRECTORY_"></span>**/i<** _directory_*_>_*</span><span class="sxs-lookup"><span data-stu-id="60fc7-158"><span id="_i_directory_"></span><span id="_I_DIRECTORY_"></span>**/i<**_directory_*_>_*</span></span>
</dt> <dd>

<span data-ttu-id="60fc7-159">Specifica una directory in cui eseguire la ricerca dei moduli MIB dipendenti.</span><span class="sxs-lookup"><span data-stu-id="60fc7-159">Specifies a directory to be searched for dependent MIB modules.</span></span> <span data-ttu-id="60fc7-160">Usare con **/a**, **/CE**, **/g**, **/GC** e **/sa**.</span><span class="sxs-lookup"><span data-stu-id="60fc7-160">Use with **/a**, **/ec**, **/g**, **/gc**, and **/sa**.</span></span> <span data-ttu-id="60fc7-161">L'opzione **/i** può apparire più volte nel comando; viene eseguita la ricerca nelle directory nell'ordine specificato nel comando.</span><span class="sxs-lookup"><span data-stu-id="60fc7-161">The **/i** option can appear multiple times in the command; directories are searched in the order specified in the command.</span></span>

</dd> <dt>

<span data-ttu-id="60fc7-162"><span id="_ch"></span><span id="_CH"></span>**/ch**</span><span class="sxs-lookup"><span data-stu-id="60fc7-162"><span id="_ch"></span><span id="_CH"></span>**/ch**</span></span>
</dt> <dd>

<span data-ttu-id="60fc7-163">Genera informazioni sul contesto, ad esempio la data, l'ora, l'host o l'utente, nell'intestazione del file MOF.</span><span class="sxs-lookup"><span data-stu-id="60fc7-163">Generates context information, such as the date, time, host, or user, in the MOF file header.</span></span> <span data-ttu-id="60fc7-164">Usare con **/g** e **/GC**.</span><span class="sxs-lookup"><span data-stu-id="60fc7-164">Use with **/g** and **/gc**.</span></span>

</dd> <dt>

<span data-ttu-id="60fc7-165"><span id="_t"></span><span id="_T"></span>**/t**</span><span class="sxs-lookup"><span data-stu-id="60fc7-165"><span id="_t"></span><span id="_T"></span>**/t**</span></span>
</dt> <dd>

<span data-ttu-id="60fc7-166">Genera le classi [SnmpNotification](snmpnotification.md) .</span><span class="sxs-lookup"><span data-stu-id="60fc7-166">Generates [SnmpNotification](snmpnotification.md) classes.</span></span> <span data-ttu-id="60fc7-167">Usare con **/a**, **/g** e **/sa**.</span><span class="sxs-lookup"><span data-stu-id="60fc7-167">Use with **/a**, **/g**, and **/sa**.</span></span>

</dd> <dt>

<span data-ttu-id="60fc7-168"><span id="_ext"></span><span id="_EXT"></span>**/EXT**</span><span class="sxs-lookup"><span data-stu-id="60fc7-168"><span id="_ext"></span><span id="_EXT"></span>**/ext**</span></span>
</dt> <dd>

<span data-ttu-id="60fc7-169">Genera le classi [SnmpExtendedNotification](snmpextendednotification.md) .</span><span class="sxs-lookup"><span data-stu-id="60fc7-169">Generates [SnmpExtendedNotification](snmpextendednotification.md) classes.</span></span> <span data-ttu-id="60fc7-170">Usare con **/a**, **/g** e **/sa**.</span><span class="sxs-lookup"><span data-stu-id="60fc7-170">Use with **/a**, **/g**, and **/sa**.</span></span>

</dd> <dt>

<span data-ttu-id="60fc7-171"><span id="_t_o"></span><span id="_T_O"></span>**/t/o**</span><span class="sxs-lookup"><span data-stu-id="60fc7-171"><span id="_t_o"></span><span id="_T_O"></span>**/t/o**</span></span>
</dt> <dd>

<span data-ttu-id="60fc7-172">Genera solo le classi [SnmpNotification](snmpnotification.md) .</span><span class="sxs-lookup"><span data-stu-id="60fc7-172">Generates only [SnmpNotification](snmpnotification.md) classes.</span></span> <span data-ttu-id="60fc7-173">Usare con **/a**, **/g** e **/sa**.</span><span class="sxs-lookup"><span data-stu-id="60fc7-173">Use with **/a**, **/g**, and **/sa**.</span></span>

</dd> <dt>

<span data-ttu-id="60fc7-174"><span id="_ext_o"></span><span id="_EXT_O"></span>**/ext/o**</span><span class="sxs-lookup"><span data-stu-id="60fc7-174"><span id="_ext_o"></span><span id="_EXT_O"></span>**/ext/o**</span></span>
</dt> <dd>

<span data-ttu-id="60fc7-175">Genera solo le classi [SnmpExtendedNotification](snmpextendednotification.md) .</span><span class="sxs-lookup"><span data-stu-id="60fc7-175">Generates only [SnmpExtendedNotification](snmpextendednotification.md) classes.</span></span> <span data-ttu-id="60fc7-176">Usare con **/a**, **/g** e **/sa**.</span><span class="sxs-lookup"><span data-stu-id="60fc7-176">Use with **/a**, **/g**, and **/sa**.</span></span>

</dd> <dt>

<span data-ttu-id="60fc7-177"><span id="_s"></span><span id="_S"></span>**/s**</span><span class="sxs-lookup"><span data-stu-id="60fc7-177"><span id="_s"></span><span id="_S"></span>**/s**</span></span>
</dt> <dd>

<span data-ttu-id="60fc7-178">Non esegue il mapping del testo della clausola DESCRIPTION.</span><span class="sxs-lookup"><span data-stu-id="60fc7-178">Does not map the text of the DESCRIPTION clause.</span></span> <span data-ttu-id="60fc7-179">Usare con **/a**, **/g**, **/GC** e **/sa**.</span><span class="sxs-lookup"><span data-stu-id="60fc7-179">Use with **/a**, **/g**, **/gc**, and **/sa**.</span></span> <span data-ttu-id="60fc7-180">Utilizzare questa opzione se si desidera ridurre al minimo i requisiti di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="60fc7-180">Use this option when you want to minimize storage requirements.</span></span>

</dd> <dt>

<span data-ttu-id="60fc7-181"><span id="_auto"></span><span id="_AUTO"></span>**/auto**</span><span class="sxs-lookup"><span data-stu-id="60fc7-181"><span id="_auto"></span><span id="_AUTO"></span>**/auto**</span></span>
</dt> <dd>

<span data-ttu-id="60fc7-182">Ricompila la tabella di ricerca MIB prima di completare il <opzione di> *CommandArg* .</span><span class="sxs-lookup"><span data-stu-id="60fc7-182">Rebuilds the MIB lookup table before completing the <*CommandArg*> switch.</span></span> <span data-ttu-id="60fc7-183">Usare con **/a**, **/CE**, **/g** e **/GC**.</span><span class="sxs-lookup"><span data-stu-id="60fc7-183">Use with **/a**, **/ec**, **/g**, and **/gc**.</span></span>

<span data-ttu-id="60fc7-184"></dd> </dl> </dd> <dt>

<span id="_RegistryArgs_"></span><span id="_registryargs_"></span><span id="_REGISTRYARGS_"></span><*RegistryArgs*>
</dt> </span><span class="sxs-lookup"><span data-stu-id="60fc7-184"></dd> </dl> </dd> <dt>

<span id="_RegistryArgs_"></span><span id="_registryargs_"></span><span id="_REGISTRYARGS_"></span><*RegistryArgs*>
</dt> </span></span><dd>

<span data-ttu-id="60fc7-185">Il compilatore accetta gli argomenti del registro di sistema seguenti.</span><span class="sxs-lookup"><span data-stu-id="60fc7-185">The compiler accepts the following registry arguments.</span></span>

<dl> <dt>

<span data-ttu-id="60fc7-186"><span id="_pa"></span><span id="_PA"></span>**/PA**</span><span class="sxs-lookup"><span data-stu-id="60fc7-186"><span id="_pa"></span><span id="_PA"></span>**/pa**</span></span>
</dt> <dd>

<span data-ttu-id="60fc7-187">Aggiunge la directory specificata al registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="60fc7-187">Adds the specified directory to the registry.</span></span> <span data-ttu-id="60fc7-188">Il valore predefinito è la directory corrente.</span><span class="sxs-lookup"><span data-stu-id="60fc7-188">The default is the current directory.</span></span>

</dd> <dt>

<span data-ttu-id="60fc7-189"><span id="_pd"></span><span id="_PD"></span>**/PD**</span><span class="sxs-lookup"><span data-stu-id="60fc7-189"><span id="_pd"></span><span id="_PD"></span>**/pd**</span></span>
</dt> <dd>

<span data-ttu-id="60fc7-190">Elimina la directory specificata dal registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="60fc7-190">Deletes the specified directory from the registry.</span></span> <span data-ttu-id="60fc7-191">Il valore predefinito è la directory corrente.</span><span class="sxs-lookup"><span data-stu-id="60fc7-191">The default is the current directory.</span></span>

</dd> <dt>

<span data-ttu-id="60fc7-192"><span id="_pl"></span><span id="_PL"></span>**/pl**</span><span class="sxs-lookup"><span data-stu-id="60fc7-192"><span id="_pl"></span><span id="_PL"></span>**/pl**</span></span>
</dt> <dd>

<span data-ttu-id="60fc7-193">Elenca le directory di ricerca MIB nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="60fc7-193">Lists the MIB lookup directories in the registry.</span></span>

</dd> <dt>

<span data-ttu-id="60fc7-194"><span id="_r"></span><span id="_R"></span>**/r**</span><span class="sxs-lookup"><span data-stu-id="60fc7-194"><span id="_r"></span><span id="_R"></span>**/r**</span></span>
</dt> <dd>

<span data-ttu-id="60fc7-195">Ricompila l'intera tabella di ricerca MIB.</span><span class="sxs-lookup"><span data-stu-id="60fc7-195">Rebuilds the entire MIB lookup table.</span></span>

<span data-ttu-id="60fc7-196"></dd> </dl> </dd> <dt>

<span id="_ModuleInfoArgs_"></span><span id="_moduleinfoargs_"></span><span id="_MODULEINFOARGS_"></span><*ModuleInfoArgs*>
</dt> </span><span class="sxs-lookup"><span data-stu-id="60fc7-196"></dd> </dl> </dd> <dt>

<span id="_ModuleInfoArgs_"></span><span id="_moduleinfoargs_"></span><span id="_MODULEINFOARGS_"></span><*ModuleInfoArgs*>
</dt> </span></span><dd>

<span data-ttu-id="60fc7-197">Il compilatore accetta gli argomenti di informazioni sui moduli seguenti.</span><span class="sxs-lookup"><span data-stu-id="60fc7-197">The compiler accepts the following module information arguments.</span></span>

<dl> <dt>

<span data-ttu-id="60fc7-198"><span id="_n"></span><span id="_N"></span>**/n**</span><span class="sxs-lookup"><span data-stu-id="60fc7-198"><span id="_n"></span><span id="_N"></span>**/n**</span></span>
</dt> <dd>

<span data-ttu-id="60fc7-199">Restituisce il nome ASN. 1 del modulo specificato.</span><span class="sxs-lookup"><span data-stu-id="60fc7-199">Returns the ASN.1 name of the specified module.</span></span>

</dd> <dt>

<span data-ttu-id="60fc7-200"><span id="_ni"></span><span id="_NI"></span>**/ni**</span><span class="sxs-lookup"><span data-stu-id="60fc7-200"><span id="_ni"></span><span id="_NI"></span>**/ni**</span></span>
</dt> <dd>

<span data-ttu-id="60fc7-201">Restituisce i nomi ASN. 1 di tutti i moduli di importazione a cui fa riferimento il modulo di input.</span><span class="sxs-lookup"><span data-stu-id="60fc7-201">Returns the ASN.1 names of all import modules referred to by the input module.</span></span>

<span data-ttu-id="60fc7-202"></dd> </dl> </dd> <dt>

<span id="_HelpArgs_"></span><span id="_helpargs_"></span><span id="_HELPARGS_"></span><*HelpArgs*>
</dt> </span><span class="sxs-lookup"><span data-stu-id="60fc7-202"></dd> </dl> </dd> <dt>

<span id="_HelpArgs_"></span><span id="_helpargs_"></span><span id="_HELPARGS_"></span><*HelpArgs*>
</dt> </span></span><dd>

<span data-ttu-id="60fc7-203">Il compilatore accetta gli argomenti della guida seguenti.</span><span class="sxs-lookup"><span data-stu-id="60fc7-203">The compiler accepts the following help arguments.</span></span>

<dl> <dt>

<span data-ttu-id="60fc7-204"><span id="_h"></span><span id="_H"></span>**/h**</span><span class="sxs-lookup"><span data-stu-id="60fc7-204"><span id="_h"></span><span id="_H"></span>**/h**</span></span>
</dt> <dd>

<span data-ttu-id="60fc7-205">Visualizza la guida sulla sintassi del compilatore SNMP.</span><span class="sxs-lookup"><span data-stu-id="60fc7-205">Displays help on the SNMP compiler syntax.</span></span>

</dd> <dt>

<span data-ttu-id="60fc7-206"><span id="__"></span>**/?**</span><span class="sxs-lookup"><span data-stu-id="60fc7-206"><span id="__"></span>**/?**</span></span>
</dt> <dd>

<span data-ttu-id="60fc7-207">Visualizza la guida sulla sintassi del compilatore SNMP.</span><span class="sxs-lookup"><span data-stu-id="60fc7-207">Displays help on the SNMP compiler syntax.</span></span>

</dd> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="60fc7-208">Commenti</span><span class="sxs-lookup"><span data-stu-id="60fc7-208">Remarks</span></span>

<span data-ttu-id="60fc7-209">I moduli di informazioni SNMP sono scritti in un subset di Abstract Syntax Notation One (ASN. 1) il compilatore esegue le funzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="60fc7-209">SNMP information modules are written in a subset of the Abstract Syntax Notation One (ASN.1) The compiler performs the following functions:</span></span>

-   <span data-ttu-id="60fc7-210">Carica i dati dal modulo informazioni SNMP.</span><span class="sxs-lookup"><span data-stu-id="60fc7-210">Loads the data from the SNMP information module.</span></span>
-   <span data-ttu-id="60fc7-211">Esegue operazioni di controllo nel modulo di informazioni.</span><span class="sxs-lookup"><span data-stu-id="60fc7-211">Performs checking operations on the information module.</span></span> <span data-ttu-id="60fc7-212">Ad esempio, controlla la sintassi locale e controlla i riferimenti esterni rispetto alle informazioni nei moduli sussidiari.</span><span class="sxs-lookup"><span data-stu-id="60fc7-212">For example, it checks the local syntax and it checks external references against information in the subsidiary modules.</span></span>
-   <span data-ttu-id="60fc7-213">Rimuove tutti i dati precedentemente caricati dall'archivio SMIR o i dati caricati da un modulo di informazioni.</span><span class="sxs-lookup"><span data-stu-id="60fc7-213">Removes all previously loaded data from the SMIR, or removes data loaded from one information module.</span></span>
-   <span data-ttu-id="60fc7-214">Restituisce il nome del modulo ASN. 1 di un file specificato o restituisce i nomi di modulo ASN. 1 di tutti i moduli importati in un file specificato.</span><span class="sxs-lookup"><span data-stu-id="60fc7-214">Returns the ASN.1 module name of a specified file or returns the ASN.1 module names of all imported modules in a specified file.</span></span>
-   <span data-ttu-id="60fc7-215">Restituisce i nomi di modulo ASN.1 di tutti i moduli di informazioni SNMP attualmente caricati nell'archivio SMIR.</span><span class="sxs-lookup"><span data-stu-id="60fc7-215">Returns the ASN.1 module names of all SNMP information modules currently loaded in the SMIR.</span></span>
-   <span data-ttu-id="60fc7-216">Esegue la risoluzione automatica dei moduli importati anziché richiedere agli utenti di specificare manualmente i moduli richiesti.</span><span class="sxs-lookup"><span data-stu-id="60fc7-216">Performs automatic resolution of imported modules rather than requiring users to specify the required modules manually.</span></span>
-   <span data-ttu-id="60fc7-217">Esegue una modalità di caricamento invisibile all'utente che non genera alcun output, ma può essere usata per caricare i dati in archivio SMIR durante un'operazione di installazione.</span><span class="sxs-lookup"><span data-stu-id="60fc7-217">Performs a silent-loading mode of operation that does not generate any output, but can be used to load data into the SMIR during an installation operation.</span></span>
-   <span data-ttu-id="60fc7-218">Restituisce i dati dal modulo informazioni SNMP in archivio SMIR.</span><span class="sxs-lookup"><span data-stu-id="60fc7-218">Outputs the data from the SNMP information module into the SMIR.</span></span>
-   <span data-ttu-id="60fc7-219">Crea facoltativamente un file MOF statico o archivio SMIR contenente l'output del modulo informazioni.</span><span class="sxs-lookup"><span data-stu-id="60fc7-219">Optionally creates a static or SMIR MOF file containing the output from the information module.</span></span>

    <span data-ttu-id="60fc7-220">Se necessario, è possibile caricare il file static. mof in uno spazio dei nomi WMI.</span><span class="sxs-lookup"><span data-stu-id="60fc7-220">If necessary, you can load the static .mof file into a WMI namespace.</span></span> <span data-ttu-id="60fc7-221">Un file archivio SMIR. mof contiene il nome dello spazio dei nomi SNMP in cui devono risiedere le classi.</span><span class="sxs-lookup"><span data-stu-id="60fc7-221">A SMIR .mof file contains the name of the SNMP namespace in which the classes should reside.</span></span>

## <a name="examples"></a><span data-ttu-id="60fc7-222">Esempio</span><span class="sxs-lookup"><span data-stu-id="60fc7-222">Examples</span></span>

<span data-ttu-id="60fc7-223">Nell'esempio seguente il file Pra. mof viene definito come output del file Pra. MIB.</span><span class="sxs-lookup"><span data-stu-id="60fc7-223">The following example defines the pra.mof file to be the output from the pra.mib file.</span></span>

``` syntax
smi2smir /m 3 /v1 /gc /pra.mib > pra.mof
```

## <a name="requirements"></a><span data-ttu-id="60fc7-224">Requisiti</span><span class="sxs-lookup"><span data-stu-id="60fc7-224">Requirements</span></span>



| <span data-ttu-id="60fc7-225">Requisito</span><span class="sxs-lookup"><span data-stu-id="60fc7-225">Requirement</span></span> | <span data-ttu-id="60fc7-226">Valore</span><span class="sxs-lookup"><span data-stu-id="60fc7-226">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="60fc7-227">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="60fc7-227">Minimum supported client</span></span><br/> | <span data-ttu-id="60fc7-228">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="60fc7-228">Windows Vista</span></span><br/>       |
| <span data-ttu-id="60fc7-229">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="60fc7-229">Minimum supported server</span></span><br/> | <span data-ttu-id="60fc7-230">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="60fc7-230">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="60fc7-231">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="60fc7-231">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60fc7-232">Messaggi di errore del compilatore SNMP</span><span class="sxs-lookup"><span data-stu-id="60fc7-232">SNMP Compiler Error Messages</span></span>](snmp-compiler-error-messages.md)
</dt> <dt>

[<span data-ttu-id="60fc7-233">Configurazione dell'ambiente WMI SNMP</span><span class="sxs-lookup"><span data-stu-id="60fc7-233">Setting up the WMI SNMP Environment</span></span>](setting-up-the-wmi-snmp-environment.md)
</dt> <dt>

[<span data-ttu-id="60fc7-234">Accesso ai dispositivi SNMP</span><span class="sxs-lookup"><span data-stu-id="60fc7-234">Accessing SNMP Devices</span></span>](accessing-snmp-devices.md)
</dt> </dl>

 

 




