---
description: La tabella CustomAction fornisce i mezzi per integrare codice e dati personalizzati nell'installazione. L'origine del codice eseguito può essere un flusso contenuto all'interno del database, un file installato di recente o un file eseguibile esistente.
ms.assetid: 0f47abc1-4e06-4ddc-9ea1-9afb9f27d499
title: Tabella CustomAction
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75c8cbfa6500743e2a2ad89627447da1907f6f48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752322"
---
# <a name="customaction-table"></a><span data-ttu-id="57c11-104">Tabella CustomAction</span><span class="sxs-lookup"><span data-stu-id="57c11-104">CustomAction Table</span></span>

<span data-ttu-id="57c11-105">La tabella CustomAction fornisce i mezzi per integrare codice e dati personalizzati nell'installazione.</span><span class="sxs-lookup"><span data-stu-id="57c11-105">The CustomAction table provides the means of integrating custom code and data into the installation.</span></span> <span data-ttu-id="57c11-106">L'origine del codice eseguito può essere un flusso contenuto all'interno del database, un file installato di recente o un file eseguibile esistente.</span><span class="sxs-lookup"><span data-stu-id="57c11-106">The source of the code that is executed can be a stream contained within the database, a recently installed file, or an existing executable file.</span></span>

<span data-ttu-id="57c11-107">La tabella CustomAction include le colonne seguenti.</span><span class="sxs-lookup"><span data-stu-id="57c11-107">The CustomAction table has the following columns.</span></span>



| <span data-ttu-id="57c11-108">Colonna</span><span class="sxs-lookup"><span data-stu-id="57c11-108">Column</span></span>       | <span data-ttu-id="57c11-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="57c11-109">Type</span></span>                               | <span data-ttu-id="57c11-110">Chiave</span><span class="sxs-lookup"><span data-stu-id="57c11-110">Key</span></span> | <span data-ttu-id="57c11-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="57c11-111">Nullable</span></span> |
|--------------|------------------------------------|-----|----------|
| <span data-ttu-id="57c11-112">Azione</span><span class="sxs-lookup"><span data-stu-id="57c11-112">Action</span></span>       | [<span data-ttu-id="57c11-113">Identificatore</span><span class="sxs-lookup"><span data-stu-id="57c11-113">Identifier</span></span>](identifier.md)       | <span data-ttu-id="57c11-114">S</span><span class="sxs-lookup"><span data-stu-id="57c11-114">Y</span></span>   | <span data-ttu-id="57c11-115">N</span><span class="sxs-lookup"><span data-stu-id="57c11-115">N</span></span>        |
| <span data-ttu-id="57c11-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="57c11-116">Type</span></span>         | [<span data-ttu-id="57c11-117">Integer</span><span class="sxs-lookup"><span data-stu-id="57c11-117">Integer</span></span>](integer.md)             | <span data-ttu-id="57c11-118">N</span><span class="sxs-lookup"><span data-stu-id="57c11-118">N</span></span>   | <span data-ttu-id="57c11-119">N</span><span class="sxs-lookup"><span data-stu-id="57c11-119">N</span></span>        |
| <span data-ttu-id="57c11-120">Source (Sorgente)</span><span class="sxs-lookup"><span data-stu-id="57c11-120">Source</span></span>       | [<span data-ttu-id="57c11-121">CustomSource</span><span class="sxs-lookup"><span data-stu-id="57c11-121">CustomSource</span></span>](customsource.md)   | <span data-ttu-id="57c11-122">N</span><span class="sxs-lookup"><span data-stu-id="57c11-122">N</span></span>   | <span data-ttu-id="57c11-123">S</span><span class="sxs-lookup"><span data-stu-id="57c11-123">Y</span></span>        |
| <span data-ttu-id="57c11-124">Destinazione</span><span class="sxs-lookup"><span data-stu-id="57c11-124">Target</span></span>       | [<span data-ttu-id="57c11-125">Formattato</span><span class="sxs-lookup"><span data-stu-id="57c11-125">Formatted</span></span>](formatted.md)         | <span data-ttu-id="57c11-126">N</span><span class="sxs-lookup"><span data-stu-id="57c11-126">N</span></span>   | <span data-ttu-id="57c11-127">S</span><span class="sxs-lookup"><span data-stu-id="57c11-127">Y</span></span>        |
| <span data-ttu-id="57c11-128">ExtendedType</span><span class="sxs-lookup"><span data-stu-id="57c11-128">ExtendedType</span></span> | [<span data-ttu-id="57c11-129">DoubleInteger</span><span class="sxs-lookup"><span data-stu-id="57c11-129">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="57c11-130">N</span><span class="sxs-lookup"><span data-stu-id="57c11-130">N</span></span>   | <span data-ttu-id="57c11-131">S</span><span class="sxs-lookup"><span data-stu-id="57c11-131">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="57c11-132">Colonne</span><span class="sxs-lookup"><span data-stu-id="57c11-132">Columns</span></span>

<dl> <dt>

<span data-ttu-id="57c11-133"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Azione</span><span class="sxs-lookup"><span data-stu-id="57c11-133"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Action</span></span>
</dt> <dd>

<span data-ttu-id="57c11-134">Nome dell'azione.</span><span class="sxs-lookup"><span data-stu-id="57c11-134">Name of the action.</span></span> <span data-ttu-id="57c11-135">L'azione viene in genere visualizzata in una tabella di sequenza, a meno che non venga chiamata da un'altra azione personalizzata.</span><span class="sxs-lookup"><span data-stu-id="57c11-135">The action normally appears in a sequence table unless it is called by another custom action.</span></span> <span data-ttu-id="57c11-136">Se il nome corrisponde a qualsiasi azione incorporata, l'azione personalizzata non viene mai chiamata.</span><span class="sxs-lookup"><span data-stu-id="57c11-136">If the name matches any built-in action, then the custom action is never called.</span></span>

<span data-ttu-id="57c11-137">Chiave della tabella primaria.</span><span class="sxs-lookup"><span data-stu-id="57c11-137">Primary table key.</span></span>

</dd> <dt>

<span data-ttu-id="57c11-138"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>Tipo</span><span class="sxs-lookup"><span data-stu-id="57c11-138"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>Type</span></span>
</dt> <dd>

<span data-ttu-id="57c11-139">Campo di bit di flag che specifica il tipo di base dell'azione personalizzata e delle opzioni.</span><span class="sxs-lookup"><span data-stu-id="57c11-139">A field of flag bits specifying the basic type of custom action and options.</span></span> <span data-ttu-id="57c11-140">Vedere l' [elenco riepilogativo di tutti i tipi di azione personalizzati](summary-list-of-all-custom-action-types.md) per un elenco dei tipi di base.</span><span class="sxs-lookup"><span data-stu-id="57c11-140">See [Summary List of All Custom Action Types](summary-list-of-all-custom-action-types.md) for a list of the basic types.</span></span> <span data-ttu-id="57c11-141">Vedere Opzioni di [elaborazione della restituzione](custom-action-return-processing-options.md)di azioni personalizzate, [Opzioni di pianificazione dell'esecuzione](custom-action-execution-scheduling-options.md)dell'azione personalizzata, opzione di [destinazione nascosta dell'azione](custom-action-hidden-target-option.md)personalizzata e opzioni di [esecuzione personalizzate In-Script](custom-action-in-script-execution-options.md)dell'azione.</span><span class="sxs-lookup"><span data-stu-id="57c11-141">See [Custom Action Return Processing Options](custom-action-return-processing-options.md), [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md), [Custom Action Hidden Target Option](custom-action-hidden-target-option.md), and [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span></span>

</dd> <dt>

<span data-ttu-id="57c11-142"><span id="Source"></span><span id="source"></span><span id="SOURCE"></span>Origine</span><span class="sxs-lookup"><span data-stu-id="57c11-142"><span id="Source"></span><span id="source"></span><span id="SOURCE"></span>Source</span></span>
</dt> <dd>

<span data-ttu-id="57c11-143">Nome di proprietà o chiave esterna in un'altra tabella.</span><span class="sxs-lookup"><span data-stu-id="57c11-143">A property name or external key into another table.</span></span> <span data-ttu-id="57c11-144">Per una descrizione delle possibili origini azione personalizzate, vedere [origini azione personalizzate](custom-action-sources.md) e l' [elenco riepilogativo di tutti i tipi di azione personalizzata](summary-list-of-all-custom-action-types.md).</span><span class="sxs-lookup"><span data-stu-id="57c11-144">For a discussion of the possible custom action sources, see [Custom Action Sources](custom-action-sources.md) and the [Summary List of All Custom Action Types](summary-list-of-all-custom-action-types.md).</span></span> <span data-ttu-id="57c11-145">Ad esempio, la colonna di origine può contenere una chiave esterna nella prima colonna di una delle tabelle seguenti contenente l'origine del codice dell'azione personalizzata.</span><span class="sxs-lookup"><span data-stu-id="57c11-145">For example, the Source column may contain an external key into the first column of one of the following tables containing the source of the custom action code.</span></span>

<span data-ttu-id="57c11-146">[Tabella di directory](directory-table.md) per la chiamata di file eseguibili esistenti.</span><span class="sxs-lookup"><span data-stu-id="57c11-146">[Directory table](directory-table.md) for calling existing executables.</span></span>

<span data-ttu-id="57c11-147">[Tabella file](file-table.md) per la chiamata di file eseguibili e dll appena installati.</span><span class="sxs-lookup"><span data-stu-id="57c11-147">[File table](file-table.md) for calling executables and DLLs that have just been installed.</span></span>

<span data-ttu-id="57c11-148">[Tabella binaria](binary-table.md) per chiamare i file eseguibili, le dll e i dati archiviati nel database.</span><span class="sxs-lookup"><span data-stu-id="57c11-148">[Binary table](binary-table.md) for calling executables, DLLs, and data stored in the database.</span></span>

<span data-ttu-id="57c11-149">[Tabella di proprietà](property-table.md) per la chiamata di file eseguibili i cui percorsi sono contenuti in una proprietà.</span><span class="sxs-lookup"><span data-stu-id="57c11-149">[Property table](property-table.md) for calling executables whose paths are held by a property.</span></span>

</dd> <dt>

<span data-ttu-id="57c11-150"><span id="Target"></span><span id="target"></span><span id="TARGET"></span>Destinazione</span><span class="sxs-lookup"><span data-stu-id="57c11-150"><span id="Target"></span><span id="target"></span><span id="TARGET"></span>Target</span></span>
</dt> <dd>

<span data-ttu-id="57c11-151">Parametro di esecuzione che dipende dal tipo di base dell'azione personalizzata.</span><span class="sxs-lookup"><span data-stu-id="57c11-151">An execution parameter that depends on the basic type of custom action.</span></span> <span data-ttu-id="57c11-152">Per una descrizione degli elementi che devono essere immessi in questo campo per ogni tipo di azione personalizzata, vedere l' [elenco riepilogativo di tutti i tipi di azioni personalizzati](summary-list-of-all-custom-action-types.md) .</span><span class="sxs-lookup"><span data-stu-id="57c11-152">See the [Summary List of All Custom Action Types](summary-list-of-all-custom-action-types.md) for a description of what should be entered in this field for each type of custom action.</span></span> <span data-ttu-id="57c11-153">Questo campo, ad esempio, può contenere quanto segue, a seconda dell'azione personalizzata.</span><span class="sxs-lookup"><span data-stu-id="57c11-153">For example, this field may contain the following depending on the custom action.</span></span>



| <span data-ttu-id="57c11-154">Destinazione</span><span class="sxs-lookup"><span data-stu-id="57c11-154">Target</span></span>                                    | <span data-ttu-id="57c11-155">Azione personalizzata</span><span class="sxs-lookup"><span data-stu-id="57c11-155">Custom action</span></span>                         |
|-------------------------------------------|---------------------------------------|
| <span data-ttu-id="57c11-156">Punto di ingresso (obbligatorio)</span><span class="sxs-lookup"><span data-stu-id="57c11-156">Entry point (required)</span></span>                    | <span data-ttu-id="57c11-157">Chiamata di una DLL.</span><span class="sxs-lookup"><span data-stu-id="57c11-157">Calling a DLL.</span></span>                        |
| <span data-ttu-id="57c11-158">Nome eseguibile con argomenti (obbligatorio)</span><span class="sxs-lookup"><span data-stu-id="57c11-158">Executable name with arguments (required)</span></span> | <span data-ttu-id="57c11-159">Chiamata di un eseguibile esistente.</span><span class="sxs-lookup"><span data-stu-id="57c11-159">Calling an existing executable.</span></span>       |
| <span data-ttu-id="57c11-160">Argomenti della riga di comando (facoltativo)</span><span class="sxs-lookup"><span data-stu-id="57c11-160">Command line arguments (optional)</span></span>         | <span data-ttu-id="57c11-161">Chiamata di un eseguibile appena installato.</span><span class="sxs-lookup"><span data-stu-id="57c11-161">Calling an executable just installed.</span></span> |
| <span data-ttu-id="57c11-162">Nome file di destinazione (obbligatorio)</span><span class="sxs-lookup"><span data-stu-id="57c11-162">Target file name (required)</span></span>               | <span data-ttu-id="57c11-163">Creazione di un file da dati personalizzati.</span><span class="sxs-lookup"><span data-stu-id="57c11-163">Creating a file from custom data.</span></span>     |
| <span data-ttu-id="57c11-164">Null</span><span class="sxs-lookup"><span data-stu-id="57c11-164">Null</span></span>                                      | <span data-ttu-id="57c11-165">Esecuzione del codice di script.</span><span class="sxs-lookup"><span data-stu-id="57c11-165">Executing script code.</span></span>                |



 

</dd> <dt>

<span data-ttu-id="57c11-166"><span id="ExtendedType"></span><span id="extendedtype"></span><span id="EXTENDEDTYPE"></span>ExtendedType</span><span class="sxs-lookup"><span data-stu-id="57c11-166"><span id="ExtendedType"></span><span id="extendedtype"></span><span id="EXTENDEDTYPE"></span>ExtendedType</span></span>
</dt> <dd>

<span data-ttu-id="57c11-167">Immettere il valore **msidbCustomActionTypePatchUninstall** in questo campo per specificare un'azione personalizzata con l' [opzione di disinstallazione patch azione personalizzata](custom-action-patch-uninstall-option.md).</span><span class="sxs-lookup"><span data-stu-id="57c11-167">Enter the **msidbCustomActionTypePatchUninstall** value in this field to specify a custom action with the [Custom Action Patch Uninstall Option](custom-action-patch-uninstall-option.md).</span></span>

<span data-ttu-id="57c11-168">**[Windows Installer 4,0 e versioni precedenti](not-supported-in-windows-installer-4-0.md):** Non supportato.</span><span class="sxs-lookup"><span data-stu-id="57c11-168">**[Windows Installer 4.0 and earlier](not-supported-in-windows-installer-4-0.md):** Not supported.</span></span> <span data-ttu-id="57c11-169">Questa opzione è disponibile a partire da Windows Installer 4,5.</span><span class="sxs-lookup"><span data-stu-id="57c11-169">This option is available beginning with Windows Installer 4.5.</span></span>

</dd> </dl>

<span data-ttu-id="57c11-170">Per ulteriori informazioni, vedere tutti gli argomenti in [azioni personalizzate](custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="57c11-170">For more information, see all the topics under [Custom Actions](custom-actions.md).</span></span>

## <a name="validation"></a><span data-ttu-id="57c11-171">Convalida</span><span class="sxs-lookup"><span data-stu-id="57c11-171">Validation</span></span>

<dl>

[<span data-ttu-id="57c11-172">ICE03</span><span class="sxs-lookup"><span data-stu-id="57c11-172">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="57c11-173">ICE06</span><span class="sxs-lookup"><span data-stu-id="57c11-173">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="57c11-174">ICE12</span><span class="sxs-lookup"><span data-stu-id="57c11-174">ICE12</span></span>](ice12.md)  
[<span data-ttu-id="57c11-175">ICE27</span><span class="sxs-lookup"><span data-stu-id="57c11-175">ICE27</span></span>](ice27.md)  
[<span data-ttu-id="57c11-176">ICE46</span><span class="sxs-lookup"><span data-stu-id="57c11-176">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="57c11-177">ICE63</span><span class="sxs-lookup"><span data-stu-id="57c11-177">ICE63</span></span>](ice63.md)  
[<span data-ttu-id="57c11-178">ICE68</span><span class="sxs-lookup"><span data-stu-id="57c11-178">ICE68</span></span>](ice68.md)  
[<span data-ttu-id="57c11-179">ICE72</span><span class="sxs-lookup"><span data-stu-id="57c11-179">ICE72</span></span>](ice72.md)  
[<span data-ttu-id="57c11-180">ICE75</span><span class="sxs-lookup"><span data-stu-id="57c11-180">ICE75</span></span>](ice75.md)  
[<span data-ttu-id="57c11-181">ICE77</span><span class="sxs-lookup"><span data-stu-id="57c11-181">ICE77</span></span>](ice77.md)  
[<span data-ttu-id="57c11-182">ICE80</span><span class="sxs-lookup"><span data-stu-id="57c11-182">ICE80</span></span>](ice80.md)  
[<span data-ttu-id="57c11-183">ICE88</span><span class="sxs-lookup"><span data-stu-id="57c11-183">ICE88</span></span>](ice88.md)  
[<span data-ttu-id="57c11-184">ICE93</span><span class="sxs-lookup"><span data-stu-id="57c11-184">ICE93</span></span>](ice93.md)  
</dl>

 

 



