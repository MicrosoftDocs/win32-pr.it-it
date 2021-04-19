---
description: La tabella Verb contiene informazioni sui verbi di comando associate alle estensioni di file che devono essere generate come parte dell'annuncio del prodotto. Ogni riga genera un set di chiavi e valori del registro di sistema.
ms.assetid: 3749095c-f0c0-498c-969f-a6c445cfdd62
title: Tabella Verb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7182c425e2613aa463f94bca0e6a1e62c1504c8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319950"
---
# <a name="verb-table"></a><span data-ttu-id="5c52e-104">Tabella Verb</span><span class="sxs-lookup"><span data-stu-id="5c52e-104">Verb Table</span></span>

<span data-ttu-id="5c52e-105">La tabella Verb contiene informazioni sui verbi di comando associate alle estensioni di file che devono essere generate come parte dell'annuncio del prodotto.</span><span class="sxs-lookup"><span data-stu-id="5c52e-105">The Verb table contains command-verb information associated with file name extensions that must be generated as a part of product advertisement.</span></span> <span data-ttu-id="5c52e-106">Ogni riga genera un set di chiavi e valori del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="5c52e-106">Each row generates a set of registry keys and values.</span></span>

<span data-ttu-id="5c52e-107">La tabella Verb contiene le colonne seguenti.</span><span class="sxs-lookup"><span data-stu-id="5c52e-107">The Verb table has the following columns.</span></span>



| <span data-ttu-id="5c52e-108">Colonna</span><span class="sxs-lookup"><span data-stu-id="5c52e-108">Column</span></span>      | <span data-ttu-id="5c52e-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="5c52e-109">Type</span></span>                       | <span data-ttu-id="5c52e-110">Chiave</span><span class="sxs-lookup"><span data-stu-id="5c52e-110">Key</span></span> | <span data-ttu-id="5c52e-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="5c52e-111">Nullable</span></span> |
|-------------|----------------------------|-----|----------|
| <span data-ttu-id="5c52e-112">Estensione\_</span><span class="sxs-lookup"><span data-stu-id="5c52e-112">Extension\_</span></span> | [<span data-ttu-id="5c52e-113">Text</span><span class="sxs-lookup"><span data-stu-id="5c52e-113">Text</span></span>](text.md)           | <span data-ttu-id="5c52e-114">S</span><span class="sxs-lookup"><span data-stu-id="5c52e-114">Y</span></span>   | <span data-ttu-id="5c52e-115">N</span><span class="sxs-lookup"><span data-stu-id="5c52e-115">N</span></span>        |
| <span data-ttu-id="5c52e-116">Verbo</span><span class="sxs-lookup"><span data-stu-id="5c52e-116">Verb</span></span>        | [<span data-ttu-id="5c52e-117">Text</span><span class="sxs-lookup"><span data-stu-id="5c52e-117">Text</span></span>](text.md)           | <span data-ttu-id="5c52e-118">S</span><span class="sxs-lookup"><span data-stu-id="5c52e-118">Y</span></span>   | <span data-ttu-id="5c52e-119">N</span><span class="sxs-lookup"><span data-stu-id="5c52e-119">N</span></span>        |
| <span data-ttu-id="5c52e-120">Sequenza</span><span class="sxs-lookup"><span data-stu-id="5c52e-120">Sequence</span></span>    | [<span data-ttu-id="5c52e-121">Integer</span><span class="sxs-lookup"><span data-stu-id="5c52e-121">Integer</span></span>](integer.md)     | <span data-ttu-id="5c52e-122">N</span><span class="sxs-lookup"><span data-stu-id="5c52e-122">N</span></span>   | <span data-ttu-id="5c52e-123">Y</span><span class="sxs-lookup"><span data-stu-id="5c52e-123">Y</span></span>        |
| <span data-ttu-id="5c52e-124">Comando</span><span class="sxs-lookup"><span data-stu-id="5c52e-124">Command</span></span>     | [<span data-ttu-id="5c52e-125">Formattato</span><span class="sxs-lookup"><span data-stu-id="5c52e-125">Formatted</span></span>](formatted.md) | <span data-ttu-id="5c52e-126">N</span><span class="sxs-lookup"><span data-stu-id="5c52e-126">N</span></span>   | <span data-ttu-id="5c52e-127">S</span><span class="sxs-lookup"><span data-stu-id="5c52e-127">Y</span></span>        |
| <span data-ttu-id="5c52e-128">Argomento</span><span class="sxs-lookup"><span data-stu-id="5c52e-128">Argument</span></span>    | [<span data-ttu-id="5c52e-129">Formattato</span><span class="sxs-lookup"><span data-stu-id="5c52e-129">Formatted</span></span>](formatted.md) | <span data-ttu-id="5c52e-130">N</span><span class="sxs-lookup"><span data-stu-id="5c52e-130">N</span></span>   | <span data-ttu-id="5c52e-131">S</span><span class="sxs-lookup"><span data-stu-id="5c52e-131">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="5c52e-132">Colonne</span><span class="sxs-lookup"><span data-stu-id="5c52e-132">Columns</span></span>

<dl> <dt>

<span data-ttu-id="5c52e-133"><span id="Extension_"></span><span id="extension_"></span><span id="EXTENSION_"></span>Estensione\_</span><span class="sxs-lookup"><span data-stu-id="5c52e-133"><span id="Extension_"></span><span id="extension_"></span><span id="EXTENSION_"></span>Extension\_</span></span>
</dt> <dd>

<span data-ttu-id="5c52e-134">Estensione associata alla riga della tabella.</span><span class="sxs-lookup"><span data-stu-id="5c52e-134">The extension associated with the table row.</span></span> <span data-ttu-id="5c52e-135">Questa colonna è una chiave esterna per la prima colonna della [tabella di estensione](extension-table.md).</span><span class="sxs-lookup"><span data-stu-id="5c52e-135">This column is an external key to the first column of the [Extension table](extension-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="5c52e-136"><span id="Verb"></span><span id="verb"></span><span id="VERB"></span>Verbo</span><span class="sxs-lookup"><span data-stu-id="5c52e-136"><span id="Verb"></span><span id="verb"></span><span id="VERB"></span>Verb</span></span>
</dt> <dd>

<span data-ttu-id="5c52e-137">Verbo per il comando.</span><span class="sxs-lookup"><span data-stu-id="5c52e-137">The verb for the command.</span></span>

</dd> <dt>

<span data-ttu-id="5c52e-138"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Sequenza</span><span class="sxs-lookup"><span data-stu-id="5c52e-138"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Sequence</span></span>
</dt> <dd>

<span data-ttu-id="5c52e-139">Sequenza dei comandi.</span><span class="sxs-lookup"><span data-stu-id="5c52e-139">The sequence of the commands.</span></span> <span data-ttu-id="5c52e-140">Solo i verbi per i quali la colonna sequenza è non null vengono usati per preparare un elenco ordinato per il valore predefinito della chiave della shell.</span><span class="sxs-lookup"><span data-stu-id="5c52e-140">Only verbs for which the Sequence column is non-Null are used to prepare an ordered list for the default value of the shell key.</span></span> <span data-ttu-id="5c52e-141">Il verbo con il valore più basso in questa colonna diventa il verbo predefinito.</span><span class="sxs-lookup"><span data-stu-id="5c52e-141">The Verb with the lowest value in this column becomes the default verb.</span></span>

</dd> <dt>

<span data-ttu-id="5c52e-142"><span id="Command"></span><span id="command"></span><span id="COMMAND"></span>Comando</span><span class="sxs-lookup"><span data-stu-id="5c52e-142"><span id="Command"></span><span id="command"></span><span id="COMMAND"></span>Command</span></span>
</dt> <dd>

<span data-ttu-id="5c52e-143">Testo localizzabile visualizzato nel menu di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="5c52e-143">The localizable text displayed on the context menu.</span></span>

</dd> <dt>

<span data-ttu-id="5c52e-144"><span id="Argument"></span><span id="argument"></span><span id="ARGUMENT"></span>Argomento</span><span class="sxs-lookup"><span data-stu-id="5c52e-144"><span id="Argument"></span><span id="argument"></span><span id="ARGUMENT"></span>Argument</span></span>
</dt> <dd>

<span data-ttu-id="5c52e-145">Valore per gli argomenti del comando.</span><span class="sxs-lookup"><span data-stu-id="5c52e-145">Value for the command arguments.</span></span>

<span data-ttu-id="5c52e-146">Si noti che la risoluzione delle proprietà nel campo argument è limitata.</span><span class="sxs-lookup"><span data-stu-id="5c52e-146">Note that the resolution of properties in the Argument field is limited.</span></span> <span data-ttu-id="5c52e-147">Una proprietà formattata come \[ *Proprietà* \] in questo campo può essere risolta solo se la proprietà dispone già del valore desiderato quando il componente proprietario del verbo è installato.</span><span class="sxs-lookup"><span data-stu-id="5c52e-147">A property formatted as \[*Property*\] in this field can only be resolved if the property already has the intended value when the component owning the verb is installed.</span></span> <span data-ttu-id="5c52e-148">Per l'argomento "MyDoc.doc", ad esempio, per \[ \# \] risolvere il valore corretto, è necessario che lo stesso processo stia installando il file MyDoc.doc e il componente proprietario del verbo.</span><span class="sxs-lookup"><span data-stu-id="5c52e-148">For example, for the argument "\[\#MyDoc.doc\]" to resolve to the correct value, the same process must be installing the file MyDoc.doc and the component that owns the verb.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5c52e-149">Commenti</span><span class="sxs-lookup"><span data-stu-id="5c52e-149">Remarks</span></span>

<span data-ttu-id="5c52e-150">Questa tabella viene definita quando viene eseguita l'azione [RegisterExtensionInfo](registerextensioninfo-action.md) o [UnregisterExtensionInfo](unregisterextensioninfo-action.md) .</span><span class="sxs-lookup"><span data-stu-id="5c52e-150">This table is referred to when the [RegisterExtensionInfo action](registerextensioninfo-action.md) or the [UnregisterExtensionInfo action](unregisterextensioninfo-action.md) is executed.</span></span>

## <a name="validation"></a><span data-ttu-id="5c52e-151">Convalida</span><span class="sxs-lookup"><span data-stu-id="5c52e-151">Validation</span></span>

<dl>

[<span data-ttu-id="5c52e-152">ICE03</span><span class="sxs-lookup"><span data-stu-id="5c52e-152">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="5c52e-153">ICE06</span><span class="sxs-lookup"><span data-stu-id="5c52e-153">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="5c52e-154">ICE32</span><span class="sxs-lookup"><span data-stu-id="5c52e-154">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="5c52e-155">ICE46</span><span class="sxs-lookup"><span data-stu-id="5c52e-155">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="5c52e-156">ICE69</span><span class="sxs-lookup"><span data-stu-id="5c52e-156">ICE69</span></span>](ice69.md)  
</dl>

 

 



