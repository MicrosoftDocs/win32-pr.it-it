---
description: L'utilità della riga di comando WMI (WMIC) fornisce un'interfaccia della riga di comando per WMI.
ms.assetid: a0f5c1e2-9a4d-4c2b-b324-58ec01e67b6e
ms.tgt_platform: multiple
title: wmic
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed46e8aeab24acb44f51099a6e813e921dd77eaa
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/10/2021
ms.locfileid: "104234909"
---
# <a name="wmic"></a><span data-ttu-id="d3834-103">wmic</span><span class="sxs-lookup"><span data-stu-id="d3834-103">wmic</span></span>

<span data-ttu-id="d3834-104">L'utilità della riga di comando WMI (WMIC) fornisce un'interfaccia della riga di comando per Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="d3834-104">The WMI command-line (WMIC) utility provides a command-line interface for Windows Management Instrumentation (WMI).</span></span> <span data-ttu-id="d3834-105">WMIC è compatibile con le shell e i comandi di utilità esistenti.</span><span class="sxs-lookup"><span data-stu-id="d3834-105">WMIC is compatible with existing shells and utility commands.</span></span> <span data-ttu-id="d3834-106">Di seguito è riportato un argomento di riferimento generale per WMIC.</span><span class="sxs-lookup"><span data-stu-id="d3834-106">The following is a general reference topic for WMIC.</span></span> <span data-ttu-id="d3834-107">Per ulteriori informazioni e linee guida su come utilizzare WMIC, incluse informazioni aggiuntive sugli alias, i verbi, i commutatori e i comandi, vedere [utilizzo Strumentazione gestione Windows riga di comando](/previous-versions/windows/it-pro/windows-server-2003/cc779482(v=ws.10)) e il [controllo della riga di comando WMIC-take su WMI](/previous-versions/windows/it-pro/windows-2000-server/bb742610(v=technet.10)).</span><span class="sxs-lookup"><span data-stu-id="d3834-107">For more information and guidelines on how to use WMIC, including additional information on aliases, verbs, switches, and commands, see [Using Windows Management Instrumentation Command-line](/previous-versions/windows/it-pro/windows-server-2003/cc779482(v=ws.10)) and [WMIC - Take Command-line Control over WMI](/previous-versions/windows/it-pro/windows-2000-server/bb742610(v=technet.10)).</span></span>

## <a name="alias"></a><span data-ttu-id="d3834-108">Alias</span><span class="sxs-lookup"><span data-stu-id="d3834-108">Alias</span></span>

<span data-ttu-id="d3834-109">Un alias è una ridenominazione descrittiva di una classe, di una proprietà o di un metodo che rende più semplice l'utilizzo e la lettura di WMI.</span><span class="sxs-lookup"><span data-stu-id="d3834-109">An alias is a friendly renaming of a class, property, or method that makes WMI easier to use and read.</span></span> <span data-ttu-id="d3834-110">È possibile determinare quali alias sono disponibili per WMIC tramite **/?**</span><span class="sxs-lookup"><span data-stu-id="d3834-110">You can determine what aliases are available for WMIC through the **/?**</span></span> <span data-ttu-id="d3834-111">.</span><span class="sxs-lookup"><span data-stu-id="d3834-111">command.</span></span> <span data-ttu-id="d3834-112">È inoltre possibile determinare gli alias per una classe specifica utilizzando **<className> /?**</span><span class="sxs-lookup"><span data-stu-id="d3834-112">You can also determine the aliases for a specific class using the **<className> /?**</span></span> <span data-ttu-id="d3834-113">.</span><span class="sxs-lookup"><span data-stu-id="d3834-113">command.</span></span> <span data-ttu-id="d3834-114">Per ulteriori informazioni, vedere gli [Alias WMIC](/previous-versions/windows/it-pro/windows-server-2003/cc736307(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="d3834-114">For more information, see [WMIC Aliases](/previous-versions/windows/it-pro/windows-server-2003/cc736307(v=ws.10)).</span></span>

## <a name="switch"></a><span data-ttu-id="d3834-115">Opzione</span><span class="sxs-lookup"><span data-stu-id="d3834-115">Switch</span></span>

<span data-ttu-id="d3834-116">Un'opzione è un'opzione WMIC che è possibile impostare a livello globale o facoltativo.</span><span class="sxs-lookup"><span data-stu-id="d3834-116">A switch is a WMIC option you can set globally or optionally.</span></span> <span data-ttu-id="d3834-117">Per un elenco delle opzioni disponibili, vedere [Opzioni WMIC](/previous-versions/windows/it-pro/windows-server-2003/cc787035(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="d3834-117">For a list of available switches, see [WMIC Switches](/previous-versions/windows/it-pro/windows-server-2003/cc787035(v=ws.10)).</span></span>

## <a name="verbs"></a><span data-ttu-id="d3834-118">Verbi</span><span class="sxs-lookup"><span data-stu-id="d3834-118">Verbs</span></span>

<span data-ttu-id="d3834-119">Per utilizzare i verbi in WMIC, immettere il nome dell'alias seguito dal verbo.</span><span class="sxs-lookup"><span data-stu-id="d3834-119">To use verbs in WMIC, enter the alias name followed by the verb.</span></span> <span data-ttu-id="d3834-120">Se un alias non supporta un verbo, viene visualizzato il messaggio "provider non è in grado di eseguire l'operazione tentata".</span><span class="sxs-lookup"><span data-stu-id="d3834-120">If an alias does not support a verb, you receive the message "provider is not capable of the attempted operation."</span></span> <span data-ttu-id="d3834-121">Per ulteriori informazioni, vedere la pagina relativa ai [verbi WMIC](/previous-versions/windows/it-pro/windows-server-2003/cc784966(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="d3834-121">For more information, see [WMIC Verbs](/previous-versions/windows/it-pro/windows-server-2003/cc784966(v=ws.10)).</span></span>

<span data-ttu-id="d3834-122">La maggior parte degli alias supporta i verbi seguenti.</span><span class="sxs-lookup"><span data-stu-id="d3834-122">Most aliases support the following verbs.</span></span>

<dl> <dt>

<span data-ttu-id="d3834-123"><span id="ASSOC"></span><span id="assoc"></span>ASSOC</span><span class="sxs-lookup"><span data-stu-id="d3834-123"><span id="ASSOC"></span><span id="assoc"></span>ASSOC</span></span>
</dt> <dd>

<span data-ttu-id="d3834-124">Restituisce il risultato della `Associators of (<wmi_object>)` query in cui *<\_ oggetto WMI>* è il percorso degli oggetti restituiti dai comandi **path** o **Class** .</span><span class="sxs-lookup"><span data-stu-id="d3834-124">Returns the result of the `Associators of (<wmi_object>)` query where *<wmi\_object>* is the path of objects returned by the **PATH** or **CLASS** commands.</span></span> <span data-ttu-id="d3834-125">I risultati sono istanze associate all'oggetto.</span><span class="sxs-lookup"><span data-stu-id="d3834-125">The results are instances associated with the object.</span></span> <span data-ttu-id="d3834-126">Quando si utilizza ASSOC con un alias, vengono restituite le classi con la classe sottostante l'alias.</span><span class="sxs-lookup"><span data-stu-id="d3834-126">When ASSOC is used with an alias, the classes with the class underlying the alias are returned.</span></span> <span data-ttu-id="d3834-127">Per impostazione predefinita, l'output viene restituito in formato HTML.</span><span class="sxs-lookup"><span data-stu-id="d3834-127">By default the output is returned in HTML format.</span></span>

<span data-ttu-id="d3834-128">Il verbo ASSOC presenta le opzioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="d3834-128">The ASSOC verb has the following switches.</span></span>



| <span data-ttu-id="d3834-129">Opzione</span><span class="sxs-lookup"><span data-stu-id="d3834-129">Switch</span></span>                         | <span data-ttu-id="d3834-130">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d3834-130">Description</span></span>                                                                                                       |
|--------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3834-131">ResultClass<classname></span><span class="sxs-lookup"><span data-stu-id="d3834-131">/RESULTCLASS:<classname></span></span> | <span data-ttu-id="d3834-132">Gli endpoint restituiti associati all'oggetto di origine devono appartenere a o essere derivati dalla classe specificata.</span><span class="sxs-lookup"><span data-stu-id="d3834-132">Returned endpoints associated with the source object must belong to, or be derived from the specified class.</span></span>      |
| <span data-ttu-id="d3834-133">RESULTROLE<rolename></span><span class="sxs-lookup"><span data-stu-id="d3834-133">/RESULTROLE:<rolename></span></span>   | <span data-ttu-id="d3834-134">Gli endpoint restituiti devono riprodurre un ruolo specifico nelle associazioni con l'oggetto di origine.</span><span class="sxs-lookup"><span data-stu-id="d3834-134">Returned endpoints must play a specific role in associations with the source object.</span></span>                              |
| <span data-ttu-id="d3834-135">AssocClass<assocclass></span><span class="sxs-lookup"><span data-stu-id="d3834-135">/ASSOCCLASS:<assocclass></span></span> | <span data-ttu-id="d3834-136">Gli endpoint restituiti devono essere associati all'origine tramite la classe specificata o una delle relative classi derivate.</span><span class="sxs-lookup"><span data-stu-id="d3834-136">Returned endpoints must be associated with the source through the specified class, or one of its derived classes.</span></span> |



 

<span data-ttu-id="d3834-137">Esempio: **sistema operativo Assoc**</span><span class="sxs-lookup"><span data-stu-id="d3834-137">Example: **OS ASSOC**</span></span>

</dd> <dt>

<span data-ttu-id="d3834-138"><span id="CALL"></span><span id="call"></span>CHIAMARE</span><span class="sxs-lookup"><span data-stu-id="d3834-138"><span id="CALL"></span><span id="call"></span>CALL</span></span>
</dt> <dd>

<span data-ttu-id="d3834-139">Esegue un metodo.</span><span class="sxs-lookup"><span data-stu-id="d3834-139">Executes a method.</span></span>

<span data-ttu-id="d3834-140">Esempio: **servizio dove Caption =' Telnet ' chiama StartService**</span><span class="sxs-lookup"><span data-stu-id="d3834-140">Example: **SERVICE WHERE CAPTION='TELNET' CALL STARTSERVICE**</span></span>

> [!Note]  
> <span data-ttu-id="d3834-141">Per determinare i metodi disponibili per una determinata classe, utilizzare **/?**.</span><span class="sxs-lookup"><span data-stu-id="d3834-141">To determine the methods available for a given class, use **/?**.</span></span> <span data-ttu-id="d3834-142">Ad esempio, il **servizio dove Caption =' Telnet ' chiama/?**</span><span class="sxs-lookup"><span data-stu-id="d3834-142">For example, **SERVICE WHERE CAPTION='TELNET' CALL /?**</span></span> <span data-ttu-id="d3834-143">elenca le funzioni disponibili per la classe del servizio.</span><span class="sxs-lookup"><span data-stu-id="d3834-143">lists the available functions for the service class.</span></span>

 

</dd> <dt>

<span data-ttu-id="d3834-144"><span id="CREATE"></span><span id="create"></span>CREARE</span><span class="sxs-lookup"><span data-stu-id="d3834-144"><span id="CREATE"></span><span id="create"></span>CREATE</span></span>
</dt> <dd>

<span data-ttu-id="d3834-145">Crea una nuova istanza di e imposta i valori della proprietà.</span><span class="sxs-lookup"><span data-stu-id="d3834-145">Creates a new instance and sets the property values.</span></span> <span data-ttu-id="d3834-146">Non è possibile usare CREATE per creare una nuova classe.</span><span class="sxs-lookup"><span data-stu-id="d3834-146">CREATE cannot be used to create a new class.</span></span>

<span data-ttu-id="d3834-147">Esempio: **Environment create name = "Temp"; VARIABLEVALUE = "nuovo"**</span><span class="sxs-lookup"><span data-stu-id="d3834-147">Example: **ENVIRONMENT CREATE NAME="TEMP"; VARIABLEVALUE="NEW"**</span></span>

</dd> <dt>

<span data-ttu-id="d3834-148"><span id="DELETE"></span><span id="delete"></span>ELIMINARE</span><span class="sxs-lookup"><span data-stu-id="d3834-148"><span id="DELETE"></span><span id="delete"></span>DELETE</span></span>
</dt> <dd>

<span data-ttu-id="d3834-149">Elimina l'istanza o il set di istanze corrente.</span><span class="sxs-lookup"><span data-stu-id="d3834-149">Deletes the current instance or set of instances.</span></span> <span data-ttu-id="d3834-150">È possibile utilizzare DELETE per eliminare una classe.</span><span class="sxs-lookup"><span data-stu-id="d3834-150">DELETE can be used to delete a class.</span></span>

<span data-ttu-id="d3834-151">Esempio: **processo con nome = "CALC.EXE" Delete**</span><span class="sxs-lookup"><span data-stu-id="d3834-151">Example: **PROCESS WHERE NAME="CALC.EXE" DELETE**</span></span>

</dd> <dt>

<span data-ttu-id="d3834-152"><span id="GET"></span><span id="get"></span>Ottieni</span><span class="sxs-lookup"><span data-stu-id="d3834-152"><span id="GET"></span><span id="get"></span>GET</span></span>
</dt> <dd>

<span data-ttu-id="d3834-153">Recuperare valori di proprietà specifici.</span><span class="sxs-lookup"><span data-stu-id="d3834-153">Retrieve specific property values.</span></span>

<span data-ttu-id="d3834-154">GET presenta le opzioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="d3834-154">GET has the following switches.</span></span>



| <span data-ttu-id="d3834-155">Opzione</span><span class="sxs-lookup"><span data-stu-id="d3834-155">Switch</span></span>                               | <span data-ttu-id="d3834-156">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d3834-156">Description</span></span>                                                                                                                                |
|--------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3834-157">/VALUE</span><span class="sxs-lookup"><span data-stu-id="d3834-157">/VALUE</span></span>                               | <span data-ttu-id="d3834-158">L'output viene formattato con ogni valore elencato in una riga separata e con il nome della proprietà.</span><span class="sxs-lookup"><span data-stu-id="d3834-158">Output is formatted with each value listed on a separate line and with the name of the property.</span></span>                                           |
| <span data-ttu-id="d3834-159">/ALL</span><span class="sxs-lookup"><span data-stu-id="d3834-159">/ALL</span></span>                                 | <span data-ttu-id="d3834-160">L'output viene formattato come tabella.</span><span class="sxs-lookup"><span data-stu-id="d3834-160">Output is formatted as a table.</span></span>                                                                                                            |
| <span data-ttu-id="d3834-161">Tradurre<translation table></span><span class="sxs-lookup"><span data-stu-id="d3834-161">/TRANSLATE:<translation table></span></span> | <span data-ttu-id="d3834-162">Tradurre l'output usando la tabella di traduzione denominata dal comando.</span><span class="sxs-lookup"><span data-stu-id="d3834-162">Translate the output using the translation table named by the command.</span></span> <span data-ttu-id="d3834-163">Con WMIC sono incluse le tabelle di conversione BasicXml e novirgole.</span><span class="sxs-lookup"><span data-stu-id="d3834-163">The translation tables BasicXml and NoComma are included with WMIC.</span></span> |
| <span data-ttu-id="d3834-164">Ogni<interval></span><span class="sxs-lookup"><span data-stu-id="d3834-164">/EVERY:<interval></span></span>              | <span data-ttu-id="d3834-165">Ripetere il comando ogni <interval> secondo.</span><span class="sxs-lookup"><span data-stu-id="d3834-165">Repeat the command every <interval> seconds.</span></span>                                                                                         |
| <span data-ttu-id="d3834-166">Formato<format specifier></span><span class="sxs-lookup"><span data-stu-id="d3834-166">/FORMAT:<format specifier></span></span>     | <span data-ttu-id="d3834-167">Specifica una parola chiave o un nome file XSL per formattare i dati.</span><span class="sxs-lookup"><span data-stu-id="d3834-167">Specifies a key word or XSL file name to format the data.</span></span>                                                                                  |



 

<span data-ttu-id="d3834-168">Esempio: **processo get Name**</span><span class="sxs-lookup"><span data-stu-id="d3834-168">Example: **PROCESS GET NAME**</span></span>

</dd> <dt>

<span data-ttu-id="d3834-169"><span id="LIST"></span><span id="list"></span>ELENCO</span><span class="sxs-lookup"><span data-stu-id="d3834-169"><span id="LIST"></span><span id="list"></span>LIST</span></span>
</dt> <dd>

<span data-ttu-id="d3834-170">Mostra i dati.</span><span class="sxs-lookup"><span data-stu-id="d3834-170">Shows data.</span></span> <span data-ttu-id="d3834-171">LIST è il verbo predefinito.</span><span class="sxs-lookup"><span data-stu-id="d3834-171">LIST is the default verb.</span></span>

<span data-ttu-id="d3834-172">L'elenco presenta gli avverbi seguenti.</span><span class="sxs-lookup"><span data-stu-id="d3834-172">LIST has the following adverbs.</span></span>



| <span data-ttu-id="d3834-173">Avverbio</span><span class="sxs-lookup"><span data-stu-id="d3834-173">Adverb</span></span>   | <span data-ttu-id="d3834-174">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d3834-174">Description</span></span>                                                  |
|----------|--------------------------------------------------------------|
| <span data-ttu-id="d3834-175">RIASSUNTO</span><span class="sxs-lookup"><span data-stu-id="d3834-175">BRIEF</span></span>    | <span data-ttu-id="d3834-176">Set principale delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="d3834-176">Core set of the properties.</span></span>                                  |
| <span data-ttu-id="d3834-177">FULL</span><span class="sxs-lookup"><span data-stu-id="d3834-177">FULL</span></span>     | <span data-ttu-id="d3834-178">Set completo di proprietà.</span><span class="sxs-lookup"><span data-stu-id="d3834-178">Full set of properties.</span></span> <span data-ttu-id="d3834-179">Si tratta dell'avverbio predefinito per l'elenco.</span><span class="sxs-lookup"><span data-stu-id="d3834-179">This is the default adverb for LIST.</span></span> |
| <span data-ttu-id="d3834-180">INSTANCE</span><span class="sxs-lookup"><span data-stu-id="d3834-180">INSTANCE</span></span> | <span data-ttu-id="d3834-181">Solo percorsi istanza.</span><span class="sxs-lookup"><span data-stu-id="d3834-181">Instance paths only.</span></span>                                         |
| <span data-ttu-id="d3834-182">STATO</span><span class="sxs-lookup"><span data-stu-id="d3834-182">STATUS</span></span>   | <span data-ttu-id="d3834-183">Stato degli oggetti.</span><span class="sxs-lookup"><span data-stu-id="d3834-183">Status of the objects.</span></span>                                       |
| <span data-ttu-id="d3834-184">SYSTEM</span><span class="sxs-lookup"><span data-stu-id="d3834-184">SYSTEM</span></span>   | <span data-ttu-id="d3834-185">Proprietà di sistema.</span><span class="sxs-lookup"><span data-stu-id="d3834-185">System properties.</span></span>                                           |



 

<span data-ttu-id="d3834-186">ELENCO con le opzioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="d3834-186">LIST has the following switches.</span></span>



| <span data-ttu-id="d3834-187">Opzione</span><span class="sxs-lookup"><span data-stu-id="d3834-187">Switch</span></span>                               | <span data-ttu-id="d3834-188">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d3834-188">Description</span></span>                                                                                                                                |
|--------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3834-189">Tradurre<translation table></span><span class="sxs-lookup"><span data-stu-id="d3834-189">/TRANSLATE:<translation table></span></span> | <span data-ttu-id="d3834-190">Tradurre l'output usando la tabella di traduzione denominata dal comando.</span><span class="sxs-lookup"><span data-stu-id="d3834-190">Translate the output using the translation table named by the command.</span></span> <span data-ttu-id="d3834-191">Con WMIC sono incluse le tabelle di conversione BasicXml e novirgole.</span><span class="sxs-lookup"><span data-stu-id="d3834-191">The translation tables BasicXml and NoComma are included with WMIC.</span></span> |
| <span data-ttu-id="d3834-192">Ogni<interval></span><span class="sxs-lookup"><span data-stu-id="d3834-192">/EVERY:<interval></span></span>              | <span data-ttu-id="d3834-193">Ripetere il comando ogni <interval> secondo.</span><span class="sxs-lookup"><span data-stu-id="d3834-193">Repeat the command every <interval> seconds.</span></span>                                                                                         |
| <span data-ttu-id="d3834-194">Formato<format specifier></span><span class="sxs-lookup"><span data-stu-id="d3834-194">/FORMAT:<format specifier></span></span>     | <span data-ttu-id="d3834-195">Specifica una parola chiave o un nome file XSL per formattare i dati.</span><span class="sxs-lookup"><span data-stu-id="d3834-195">Specifies a key word or XSL file name to format the data.</span></span>                                                                                  |



 

<span data-ttu-id="d3834-196">Esempio: **breve elenco processi**</span><span class="sxs-lookup"><span data-stu-id="d3834-196">Example: **PROCESS LIST BRIEF**</span></span>

</dd> <dt>

<span data-ttu-id="d3834-197"><span id="SET"></span><span id="set"></span>SET</span><span class="sxs-lookup"><span data-stu-id="d3834-197"><span id="SET"></span><span id="set"></span>SET</span></span>
</dt> <dd>

<span data-ttu-id="d3834-198">Assegna i valori alle proprietà.</span><span class="sxs-lookup"><span data-stu-id="d3834-198">Assigns values to properties.</span></span> <span data-ttu-id="d3834-199">Esempio: **Environment set Name = "Temp"**, **VARIABLEVALUE = "New"**</span><span class="sxs-lookup"><span data-stu-id="d3834-199">Example: **ENVIRONMENT SET NAME="TEMP"**, **VARIABLEVALUE="NEW"**</span></span>

</dd> </dl>

## <a name="switches"></a><span data-ttu-id="d3834-200">Commutatori</span><span class="sxs-lookup"><span data-stu-id="d3834-200">Switches</span></span>

<span data-ttu-id="d3834-201">Le opzioni globali vengono utilizzate per impostare i valori predefiniti per l'ambiente WMIC.</span><span class="sxs-lookup"><span data-stu-id="d3834-201">Global switches are used to set defaults for the WMIC environment.</span></span> <span data-ttu-id="d3834-202">È possibile visualizzare il valore corrente delle condizioni impostate da queste opzioni immettendo il comando di **contesto** .</span><span class="sxs-lookup"><span data-stu-id="d3834-202">You can view the current value of the conditions set by these switches by entering the **CONTEXT** command.</span></span>

<dl> <dt>

<span data-ttu-id="d3834-203"><span id="_NAMESPACE"></span><span id="_namespace"></span>/NAMESPACE</span><span class="sxs-lookup"><span data-stu-id="d3834-203"><span id="_NAMESPACE"></span><span id="_namespace"></span>/NAMESPACE</span></span>
</dt> <dd>

<span data-ttu-id="d3834-204">Spazio dei nomi usato in genere dall'alias.</span><span class="sxs-lookup"><span data-stu-id="d3834-204">Namespace the alias uses typically.</span></span> <span data-ttu-id="d3834-205">Il valore predefinito è \\ CIMV2 radice.</span><span class="sxs-lookup"><span data-stu-id="d3834-205">The default is root\\cimv2.</span></span>

<span data-ttu-id="d3834-206">Esempio: **/namespace: \\ \\ root**</span><span class="sxs-lookup"><span data-stu-id="d3834-206">Example: **/NAMESPACE:\\\\root**</span></span>

</dd> <dt>

<span data-ttu-id="d3834-207"><span id="_ROLE"></span><span id="_role"></span>/ROLE</span><span class="sxs-lookup"><span data-stu-id="d3834-207"><span id="_ROLE"></span><span id="_role"></span>/ROLE</span></span>
</dt> <dd>

<span data-ttu-id="d3834-208">Il WMIC dello spazio dei nomi in genere cerca gli alias e altre informazioni di WMIC.</span><span class="sxs-lookup"><span data-stu-id="d3834-208">Namespace WMIC typically looks in for aliases and other WMIC information.</span></span>

<span data-ttu-id="d3834-209">Esempio: **/Role: \\ \\ root**</span><span class="sxs-lookup"><span data-stu-id="d3834-209">Example: **/ROLE:\\\\root**</span></span>

</dd> <dt>

<span data-ttu-id="d3834-210"><span id="_NODE"></span><span id="_node"></span>/NODE</span><span class="sxs-lookup"><span data-stu-id="d3834-210"><span id="_NODE"></span><span id="_node"></span>/NODE</span></span>
</dt> <dd>

<span data-ttu-id="d3834-211">Nomi computer, delimitati da virgole.</span><span class="sxs-lookup"><span data-stu-id="d3834-211">Computer names, comma delimited.</span></span> <span data-ttu-id="d3834-212">Tutti i comandi vengono eseguiti in modo sincrono su tutti i computer elencati in questo valore.</span><span class="sxs-lookup"><span data-stu-id="d3834-212">All commands are synchronously executed against all computers listed in this value.</span></span> <span data-ttu-id="d3834-213">I nomi file devono essere preceduti dal prefisso &.</span><span class="sxs-lookup"><span data-stu-id="d3834-213">File names must be prefixed with &.</span></span> <span data-ttu-id="d3834-214">I nomi di computer all'interno di un file devono essere delimitati da virgole o su righe separate.</span><span class="sxs-lookup"><span data-stu-id="d3834-214">Computer names within a file must be comma delimited or on separate lines.</span></span>

</dd> <dt>

<span data-ttu-id="d3834-215"><span id="_IMPLEVEL"></span><span id="_implevel"></span>/IMPLEVEL</span><span class="sxs-lookup"><span data-stu-id="d3834-215"><span id="_IMPLEVEL"></span><span id="_implevel"></span>/IMPLEVEL</span></span>
</dt> <dd>

<span data-ttu-id="d3834-216">Livello di rappresentazione.</span><span class="sxs-lookup"><span data-stu-id="d3834-216">Impersonation level.</span></span>

<span data-ttu-id="d3834-217">Esempio: **/IMPLEVEL: Anonymous**</span><span class="sxs-lookup"><span data-stu-id="d3834-217">Example: **/IMPLEVEL:Anonymous**</span></span>

</dd> <dt>

<span data-ttu-id="d3834-218"><span id="_AUTHLEVEL"></span><span id="_authlevel"></span>/AUTHLEVEL</span><span class="sxs-lookup"><span data-stu-id="d3834-218"><span id="_AUTHLEVEL"></span><span id="_authlevel"></span>/AUTHLEVEL</span></span>
</dt> <dd>

<span data-ttu-id="d3834-219">Livello di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="d3834-219">Authentication level.</span></span>

<span data-ttu-id="d3834-220">Esempio: **/AUTHLEVEL: PKT**</span><span class="sxs-lookup"><span data-stu-id="d3834-220">Example: **/AUTHLEVEL:Pkt**</span></span>

</dd> <dt>

<span data-ttu-id="d3834-221"><span id="_LOCALE"></span><span id="_locale"></span>/LOCALE</span><span class="sxs-lookup"><span data-stu-id="d3834-221"><span id="_LOCALE"></span><span id="_locale"></span>/LOCALE</span></span>
</dt> <dd>

<span data-ttu-id="d3834-222">Locale.</span><span class="sxs-lookup"><span data-stu-id="d3834-222">Locale.</span></span>

<span data-ttu-id="d3834-223">Esempio: **/locale: MS \_ 411**</span><span class="sxs-lookup"><span data-stu-id="d3834-223">Example: **/LOCALE:MS\_411**</span></span>

</dd> <dt>

<span data-ttu-id="d3834-224"><span id="_PRIVILEGES"></span><span id="_privileges"></span>/PRIVILEGES</span><span class="sxs-lookup"><span data-stu-id="d3834-224"><span id="_PRIVILEGES"></span><span id="_privileges"></span>/PRIVILEGES</span></span>
</dt> <dd>

<span data-ttu-id="d3834-225">Abilitare o disabilitare tutti i privilegi.</span><span class="sxs-lookup"><span data-stu-id="d3834-225">Enable or disable all privileges.</span></span>

<span data-ttu-id="d3834-226">Esempio: **/privileges: Enable** o **/privileges: Disable**</span><span class="sxs-lookup"><span data-stu-id="d3834-226">Example: **/PRIVILEGES:ENABLE** or **/PRIVILEGES:DISABLE**</span></span>

</dd> <dt>

<span data-ttu-id="d3834-227"><span id="_TRACE"></span><span id="_trace"></span>/TRACE</span><span class="sxs-lookup"><span data-stu-id="d3834-227"><span id="_TRACE"></span><span id="_trace"></span>/TRACE</span></span>
</dt> <dd>

<span data-ttu-id="d3834-228">Consente di visualizzare l'esito positivo o negativo di tutte le funzioni utilizzate per eseguire i comandi WMIC.</span><span class="sxs-lookup"><span data-stu-id="d3834-228">Display the success or failure of all functions used to execute WMIC commands.</span></span>

<span data-ttu-id="d3834-229">Esempio: **/Trace: on** o **/Trace: off**</span><span class="sxs-lookup"><span data-stu-id="d3834-229">Example: **/TRACE:ON** or **/TRACE:OFF**</span></span>

</dd> <dt>

<span data-ttu-id="d3834-230"><span id="_RECORD"></span><span id="_record"></span>/RECORD</span><span class="sxs-lookup"><span data-stu-id="d3834-230"><span id="_RECORD"></span><span id="_record"></span>/RECORD</span></span>
</dt> <dd>

<span data-ttu-id="d3834-231">Registra tutti gli output in un file XML.</span><span class="sxs-lookup"><span data-stu-id="d3834-231">Records all output to an XML file.</span></span> <span data-ttu-id="d3834-232">L'output viene visualizzato anche al prompt dei comandi.</span><span class="sxs-lookup"><span data-stu-id="d3834-232">Output is also displayed at the command prompt.</span></span>

<span data-ttu-id="d3834-233">Esempio: **/record:** _MyOutput.xml_</span><span class="sxs-lookup"><span data-stu-id="d3834-233">Example: **/RECORD:**_MyOutput.xml_</span></span>

</dd> <dt>

<span data-ttu-id="d3834-234"><span id="_INTERACTIVE"></span><span id="_interactive"></span>/INTERACTIVE</span><span class="sxs-lookup"><span data-stu-id="d3834-234"><span id="_INTERACTIVE"></span><span id="_interactive"></span>/INTERACTIVE</span></span>
</dt> <dd>

<span data-ttu-id="d3834-235">In genere, vengono confermati i comandi DELETE.</span><span class="sxs-lookup"><span data-stu-id="d3834-235">Typically, delete commands are confirmed.</span></span>

<span data-ttu-id="d3834-236">Esempio: **/Interactive: on** o **/Interactive: off**</span><span class="sxs-lookup"><span data-stu-id="d3834-236">Example: **/INTERACTIVE:ON** or **/INTERACTIVE:OFF**</span></span>

</dd> <dt>

<span data-ttu-id="d3834-237"><span id="_FAILFAST_on_off_TimeoutInMilliseconds"></span><span id="_failfast_on_off_timeoutinmilliseconds"></span><span id="_FAILFAST_ON_OFF_TIMEOUTINMILLISECONDS"></span>/FailFast  \| **off** \| *TimeoutInMilliseconds*</span><span class="sxs-lookup"><span data-stu-id="d3834-237"><span id="_FAILFAST_on_off_TimeoutInMilliseconds"></span><span id="_failfast_on_off_timeoutinmilliseconds"></span><span id="_FAILFAST_ON_OFF_TIMEOUTINMILLISECONDS"></span>/FAILFAST **on**\|**off**\|*TimeoutInMilliseconds*</span></span>
</dt> <dd>

<span data-ttu-id="d3834-238">Se nei computer/NODE viene ping prima di inviare comandi WMIC.</span><span class="sxs-lookup"><span data-stu-id="d3834-238">If ON the /NODE computers are pinged before sending WMIC commands to them.</span></span> <span data-ttu-id="d3834-239">Se un computer non risponde, i comandi WMIC non vengono inviati.</span><span class="sxs-lookup"><span data-stu-id="d3834-239">If a computer does not respond the WMIC commands are not sent to it.</span></span>

<span data-ttu-id="d3834-240">Esempio: "/FAILFAST: ON" o "/FAILFAST: OFF"</span><span class="sxs-lookup"><span data-stu-id="d3834-240">Example: "/FAILFAST:ON" or "/FAILFAST:OFF"</span></span>

<span data-ttu-id="d3834-241">**/FAILFAST WMIC: 1000**</span><span class="sxs-lookup"><span data-stu-id="d3834-241">**WMIC /FAILFAST:1000**</span></span>

</dd> <dt>

<span data-ttu-id="d3834-242"><span id="_USER"></span><span id="_user"></span>/USER</span><span class="sxs-lookup"><span data-stu-id="d3834-242"><span id="_USER"></span><span id="_user"></span>/USER</span></span>
</dt> <dd>

<span data-ttu-id="d3834-243">Nome utente utilizzato da WMIC durante l'accesso ai computer o ai computer/NODE specificati negli alias.</span><span class="sxs-lookup"><span data-stu-id="d3834-243">User name used by WMIC when accessing the /NODE computers or computers specified in the aliases.</span></span> <span data-ttu-id="d3834-244">Verrà richiesto di specificare la password.</span><span class="sxs-lookup"><span data-stu-id="d3834-244">You are prompted for the password.</span></span> <span data-ttu-id="d3834-245">Non è possibile usare un nome utente con il computer locale.</span><span class="sxs-lookup"><span data-stu-id="d3834-245">A user name cannot be used with the local computer.</span></span>

<span data-ttu-id="d3834-246">Esempio: **/User:**_jsmith_</span><span class="sxs-lookup"><span data-stu-id="d3834-246">Example: **/USER:**_JSMITH_</span></span>

</dd> <dt>

<span data-ttu-id="d3834-247"><span id="_PASSWORD"></span><span id="_password"></span>/PASSWORD</span><span class="sxs-lookup"><span data-stu-id="d3834-247"><span id="_PASSWORD"></span><span id="_password"></span>/PASSWORD</span></span>
</dt> <dd>

<span data-ttu-id="d3834-248">Password utilizzata da WMIC durante l'accesso ai computer/NPDE.</span><span class="sxs-lookup"><span data-stu-id="d3834-248">Password used by WMIC when accessing the /NPDE computers.</span></span> <span data-ttu-id="d3834-249">La password è visibile nella riga di comando.</span><span class="sxs-lookup"><span data-stu-id="d3834-249">The password is visible at the command line.</span></span>

<span data-ttu-id="d3834-250">Esempio: **/password:**_password_</span><span class="sxs-lookup"><span data-stu-id="d3834-250">Example: **/PASSWORD:**_password_</span></span>

</dd> <dt>

<span data-ttu-id="d3834-251"><span id="_OUTPUT"></span><span id="_output"></span>/OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d3834-251"><span id="_OUTPUT"></span><span id="_output"></span>/OUTPUT</span></span>
</dt> <dd>

<span data-ttu-id="d3834-252">Specifica una modalità per tutto il reindirizzamento dell'output.</span><span class="sxs-lookup"><span data-stu-id="d3834-252">Specifies a mode for all output redirection.</span></span> <span data-ttu-id="d3834-253">L'output non viene visualizzato nella riga di comando e la destinazione viene cancellata prima dell'inizio dell'output.</span><span class="sxs-lookup"><span data-stu-id="d3834-253">Output does not appear at the command line and the destination is cleared before output begins.</span></span> <span data-ttu-id="d3834-254">I valori validi sono STDOUT, appunti o un nome file.</span><span class="sxs-lookup"><span data-stu-id="d3834-254">Valid values are STDOUT, CLIPBOARD or a file name.</span></span>

<span data-ttu-id="d3834-255">Esempio: **/output: appunti**</span><span class="sxs-lookup"><span data-stu-id="d3834-255">Example: **/OUTPUT:CLIPBOARD**</span></span>

</dd> <dt>

<span data-ttu-id="d3834-256"><span id="_APPEND"></span><span id="_append"></span>/APPEND</span><span class="sxs-lookup"><span data-stu-id="d3834-256"><span id="_APPEND"></span><span id="_append"></span>/APPEND</span></span>
</dt> <dd>

<span data-ttu-id="d3834-257">Specifica una modalità per tutto il reindirizzamento dell'output.</span><span class="sxs-lookup"><span data-stu-id="d3834-257">Specifies a mode for all output redirection.</span></span> <span data-ttu-id="d3834-258">L'output non viene visualizzato nella riga di comando e la destinazione non viene cancellata prima dell'inizio dell'output e l'output viene accodato alla fine del contenuto corrente della destinazione.</span><span class="sxs-lookup"><span data-stu-id="d3834-258">Output does not appear at the command line and the destination is not cleared before output begins and output is appended to the end of the current contents of the destination.</span></span> <span data-ttu-id="d3834-259">I valori validi sono STDOUT, appunti o un nome file.</span><span class="sxs-lookup"><span data-stu-id="d3834-259">Valid values are STDOUT, CLIPBOARD or a file name.</span></span>

<span data-ttu-id="d3834-260">Esempio: **/append: appunti**</span><span class="sxs-lookup"><span data-stu-id="d3834-260">Example: **/APPEND:CLIPBOARD**</span></span>

</dd> <dt>

<span data-ttu-id="d3834-261"><span id="_AGGREGATE"></span><span id="_aggregate"></span>/AGGREGATE</span><span class="sxs-lookup"><span data-stu-id="d3834-261"><span id="_AGGREGATE"></span><span id="_aggregate"></span>/AGGREGATE</span></span>
</dt> <dd>

<span data-ttu-id="d3834-262">Utilizzato con l'opzione **List** e **Get/every** .</span><span class="sxs-lookup"><span data-stu-id="d3834-262">Used with the **LIST** and **GET /EVERY** switch.</span></span> <span data-ttu-id="d3834-263">Se l'AGGREGAzione è ON, LIST e GET visualizzano i risultati quando tutti i computer del/NODE hanno risposto o si è verificato il timeout. Se l'AGGREGAzione è disattivata, LIST e GET visualizzano i risultati non appena vengono ricevuti.</span><span class="sxs-lookup"><span data-stu-id="d3834-263">If AGGREGATE is ON, LIST and GET display their results when all computers in the /NODE have either responded or timed out. If AGGREGATE is OFF, LIST and GET display their results as soon as they are received.</span></span>

<span data-ttu-id="d3834-264">Esempio: **/Aggregate: off** o **/Aggregate: on**</span><span class="sxs-lookup"><span data-stu-id="d3834-264">Example: **/AGGREGATE:OFF** or **/AGGREGATE:ON**</span></span>

</dd> </dl>

## <a name="commands"></a><span data-ttu-id="d3834-265">Comandi</span><span class="sxs-lookup"><span data-stu-id="d3834-265">Commands</span></span>

<span data-ttu-id="d3834-266">I comandi WMIC seguenti sono sempre disponibili.</span><span class="sxs-lookup"><span data-stu-id="d3834-266">The following WMIC commands are available at all times.</span></span> <span data-ttu-id="d3834-267">Per ulteriori informazioni, vedere [comandi WMIC](/previous-versions/windows/it-pro/windows-server-2003/cc779647(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="d3834-267">For more information, see [WMIC Commands](/previous-versions/windows/it-pro/windows-server-2003/cc779647(v=ws.10)).</span></span>

<dl> <dt>

<span data-ttu-id="d3834-268"><span id="CLASS"></span><span id="class"></span>CLASSE</span><span class="sxs-lookup"><span data-stu-id="d3834-268"><span id="CLASS"></span><span id="class"></span>CLASS</span></span>
</dt> <dd>

<span data-ttu-id="d3834-269">Eseguire l'escape dalla modalità alias predefinita di WMIC per accedere direttamente alle classi nello schema WMI.</span><span class="sxs-lookup"><span data-stu-id="d3834-269">Escape from the default alias mode of WMIC to access classes in the WMI schema directly.</span></span> <span data-ttu-id="d3834-270">Per ulteriori informazioni sulle classi WMI disponibili, vedere [classi WMI](wmi-classes.md).</span><span class="sxs-lookup"><span data-stu-id="d3834-270">For more information on available WMI classes, see [WMI Classes](wmi-classes.md).</span></span>

<span data-ttu-id="d3834-271">Esempio: **wmic/output: c: \\ClassOutput.htm classe Win32 \_ SoundDevice**</span><span class="sxs-lookup"><span data-stu-id="d3834-271">Example: **WMIC /OUTPUT:c:\\ClassOutput.htm CLASS Win32\_SoundDevice**</span></span>

</dd> <dt>

<span data-ttu-id="d3834-272"><span id="PATH"></span><span id="path"></span>PERCORSO</span><span class="sxs-lookup"><span data-stu-id="d3834-272"><span id="PATH"></span><span id="path"></span>PATH</span></span>
</dt> <dd>

<span data-ttu-id="d3834-273">Eseguire l'escape dalla modalità alias predefinita di WMIC per accedere direttamente alle istanze nello schema WMI.</span><span class="sxs-lookup"><span data-stu-id="d3834-273">Escape from the default alias mode of WMIC to access instances in the WMI schema directly.</span></span>

<span data-ttu-id="d3834-274">Esempio: **wmic/output: c: \\PathOutput.txt percorso Win32 \_ SoundDevice get/value**</span><span class="sxs-lookup"><span data-stu-id="d3834-274">Example: **WMIC /OUTPUT:c:\\PathOutput.txt PATH Win32\_SoundDevice GET /VALUE**</span></span>

</dd> <dt>

<span data-ttu-id="d3834-275"><span id="CONTEXT"></span><span id="context"></span>CONTESTO</span><span class="sxs-lookup"><span data-stu-id="d3834-275"><span id="CONTEXT"></span><span id="context"></span>CONTEXT</span></span>
</dt> <dd>

<span data-ttu-id="d3834-276">Consente di visualizzare i valori correnti di tutti i commutatori globali.</span><span class="sxs-lookup"><span data-stu-id="d3834-276">Display the current values of all global switches.</span></span>

<span data-ttu-id="d3834-277">Esempio: **contesto WMIC**</span><span class="sxs-lookup"><span data-stu-id="d3834-277">Example: **WMIC CONTEXT**</span></span>

</dd> <dt>

<span data-ttu-id="d3834-278"><span id="QUIT"></span><span id="quit"></span>QUIT</span><span class="sxs-lookup"><span data-stu-id="d3834-278"><span id="QUIT"></span><span id="quit"></span>QUIT</span></span>
</dt> <dd>

<span data-ttu-id="d3834-279">Uscire da WMIC.</span><span class="sxs-lookup"><span data-stu-id="d3834-279">Exit from WMIC.</span></span>

<span data-ttu-id="d3834-280">Esempio: **wmic Quit**</span><span class="sxs-lookup"><span data-stu-id="d3834-280">Example: **WMIC QUIT**</span></span>

</dd> <dt>

<span data-ttu-id="d3834-281"><span id="EXIT"></span><span id="exit"></span>USCITA</span><span class="sxs-lookup"><span data-stu-id="d3834-281"><span id="EXIT"></span><span id="exit"></span>EXIT</span></span>
</dt> <dd>

<span data-ttu-id="d3834-282">Uscire da WMIC.</span><span class="sxs-lookup"><span data-stu-id="d3834-282">Exit from WMIC.</span></span>

<span data-ttu-id="d3834-283">Esempio: **uscita WMIC**</span><span class="sxs-lookup"><span data-stu-id="d3834-283">Example: **WMIC EXIT**</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="d3834-284">Esempio</span><span class="sxs-lookup"><span data-stu-id="d3834-284">Examples</span></span>

<span data-ttu-id="d3834-285">Lo [script per l'impostazione di IP/subnet/gateway/DNS con](https://Gallery.TechNet.Microsoft.Com/Batch-per-settare-487c1b3f) l'esempio WMIC nella raccolta TechNet descrive come modificare e aggiornare le impostazioni IP, subnet, gateway e DNS.</span><span class="sxs-lookup"><span data-stu-id="d3834-285">The [Script for setting IP/Subnet/Gateway/DNS using wmic](https://Gallery.TechNet.Microsoft.Com/Batch-per-settare-487c1b3f) sample on TechNet Gallery describes how to modify and update IP, Subnet, Gateway, and DNS settings.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3834-286">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d3834-286">Requirements</span></span>



| <span data-ttu-id="d3834-287">Requisito</span><span class="sxs-lookup"><span data-stu-id="d3834-287">Requirement</span></span> | <span data-ttu-id="d3834-288">Valore</span><span class="sxs-lookup"><span data-stu-id="d3834-288">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="d3834-289">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d3834-289">Minimum supported client</span></span><br/> | <span data-ttu-id="d3834-290">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d3834-290">Windows Vista</span></span><br/>       |
| <span data-ttu-id="d3834-291">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d3834-291">Minimum supported server</span></span><br/> | <span data-ttu-id="d3834-292">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d3834-292">Windows Server 2008</span></span><br/> |



 

