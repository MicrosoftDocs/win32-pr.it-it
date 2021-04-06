---
description: La tabella dei collegamenti include le informazioni necessarie all'applicazione per creare collegamenti nel computer dell'utente.
ms.assetid: 86b5b51e-e5f4-4f42-84f9-1faa29ea7a84
title: Tabella di collegamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b56482f1d2d5521bede54c781c91d2de2bc39e79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882926"
---
# <a name="shortcut-table"></a><span data-ttu-id="acd40-103">Tabella di collegamento</span><span class="sxs-lookup"><span data-stu-id="acd40-103">Shortcut Table</span></span>

<span data-ttu-id="acd40-104">La tabella dei collegamenti include le informazioni necessarie all'applicazione per creare collegamenti nel computer dell'utente.</span><span class="sxs-lookup"><span data-stu-id="acd40-104">The Shortcut table holds the information the application needs to create shortcuts on the user's computer.</span></span>

<span data-ttu-id="acd40-105">La tabella dei collegamenti contiene le colonne seguenti.</span><span class="sxs-lookup"><span data-stu-id="acd40-105">The Shortcut table has the following columns.</span></span>



| <span data-ttu-id="acd40-106">Colonna</span><span class="sxs-lookup"><span data-stu-id="acd40-106">Column</span></span>                 | <span data-ttu-id="acd40-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="acd40-107">Type</span></span>                         | <span data-ttu-id="acd40-108">Chiave</span><span class="sxs-lookup"><span data-stu-id="acd40-108">Key</span></span> | <span data-ttu-id="acd40-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="acd40-109">Nullable</span></span> |
|------------------------|------------------------------|-----|----------|
| <span data-ttu-id="acd40-110">Tasto di scelta rapida</span><span class="sxs-lookup"><span data-stu-id="acd40-110">Shortcut</span></span>               | [<span data-ttu-id="acd40-111">Identificatore</span><span class="sxs-lookup"><span data-stu-id="acd40-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="acd40-112">S</span><span class="sxs-lookup"><span data-stu-id="acd40-112">Y</span></span>   | <span data-ttu-id="acd40-113">N</span><span class="sxs-lookup"><span data-stu-id="acd40-113">N</span></span>        |
| <span data-ttu-id="acd40-114">Directory\_</span><span class="sxs-lookup"><span data-stu-id="acd40-114">Directory\_</span></span>            | [<span data-ttu-id="acd40-115">Identificatore</span><span class="sxs-lookup"><span data-stu-id="acd40-115">Identifier</span></span>](identifier.md) | <span data-ttu-id="acd40-116">N</span><span class="sxs-lookup"><span data-stu-id="acd40-116">N</span></span>   | <span data-ttu-id="acd40-117">N</span><span class="sxs-lookup"><span data-stu-id="acd40-117">N</span></span>        |
| <span data-ttu-id="acd40-118">Nome</span><span class="sxs-lookup"><span data-stu-id="acd40-118">Name</span></span>                   | [<span data-ttu-id="acd40-119">Filename</span><span class="sxs-lookup"><span data-stu-id="acd40-119">Filename</span></span>](filename.md)     | <span data-ttu-id="acd40-120">N</span><span class="sxs-lookup"><span data-stu-id="acd40-120">N</span></span>   | <span data-ttu-id="acd40-121">N</span><span class="sxs-lookup"><span data-stu-id="acd40-121">N</span></span>        |
| <span data-ttu-id="acd40-122">Componente\_</span><span class="sxs-lookup"><span data-stu-id="acd40-122">Component\_</span></span>            | [<span data-ttu-id="acd40-123">Identificatore</span><span class="sxs-lookup"><span data-stu-id="acd40-123">Identifier</span></span>](identifier.md) | <span data-ttu-id="acd40-124">N</span><span class="sxs-lookup"><span data-stu-id="acd40-124">N</span></span>   | <span data-ttu-id="acd40-125">N</span><span class="sxs-lookup"><span data-stu-id="acd40-125">N</span></span>        |
| <span data-ttu-id="acd40-126">Destinazione</span><span class="sxs-lookup"><span data-stu-id="acd40-126">Target</span></span>                 | [<span data-ttu-id="acd40-127">Scelte rapide</span><span class="sxs-lookup"><span data-stu-id="acd40-127">Shortcut</span></span>](shortcut.md)     | <span data-ttu-id="acd40-128">N</span><span class="sxs-lookup"><span data-stu-id="acd40-128">N</span></span>   | <span data-ttu-id="acd40-129">N</span><span class="sxs-lookup"><span data-stu-id="acd40-129">N</span></span>        |
| <span data-ttu-id="acd40-130">Argomenti</span><span class="sxs-lookup"><span data-stu-id="acd40-130">Arguments</span></span>              | [<span data-ttu-id="acd40-131">Formattato</span><span class="sxs-lookup"><span data-stu-id="acd40-131">Formatted</span></span>](formatted.md)   | <span data-ttu-id="acd40-132">N</span><span class="sxs-lookup"><span data-stu-id="acd40-132">N</span></span>   | <span data-ttu-id="acd40-133">S</span><span class="sxs-lookup"><span data-stu-id="acd40-133">Y</span></span>        |
| <span data-ttu-id="acd40-134">Descrizione</span><span class="sxs-lookup"><span data-stu-id="acd40-134">Description</span></span>            | [<span data-ttu-id="acd40-135">Text</span><span class="sxs-lookup"><span data-stu-id="acd40-135">Text</span></span>](text.md)             | <span data-ttu-id="acd40-136">N</span><span class="sxs-lookup"><span data-stu-id="acd40-136">N</span></span>   | <span data-ttu-id="acd40-137">S</span><span class="sxs-lookup"><span data-stu-id="acd40-137">Y</span></span>        |
| <span data-ttu-id="acd40-138">Tasto di scelta rapida</span><span class="sxs-lookup"><span data-stu-id="acd40-138">Hotkey</span></span>                 | [<span data-ttu-id="acd40-139">Integer</span><span class="sxs-lookup"><span data-stu-id="acd40-139">Integer</span></span>](integer.md)       | <span data-ttu-id="acd40-140">N</span><span class="sxs-lookup"><span data-stu-id="acd40-140">N</span></span>   | <span data-ttu-id="acd40-141">S</span><span class="sxs-lookup"><span data-stu-id="acd40-141">Y</span></span>        |
| <span data-ttu-id="acd40-142">Icona\_</span><span class="sxs-lookup"><span data-stu-id="acd40-142">Icon\_</span></span>                 | [<span data-ttu-id="acd40-143">Identificatore</span><span class="sxs-lookup"><span data-stu-id="acd40-143">Identifier</span></span>](identifier.md) | <span data-ttu-id="acd40-144">N</span><span class="sxs-lookup"><span data-stu-id="acd40-144">N</span></span>   | <span data-ttu-id="acd40-145">S</span><span class="sxs-lookup"><span data-stu-id="acd40-145">Y</span></span>        |
| <span data-ttu-id="acd40-146">IconIndex</span><span class="sxs-lookup"><span data-stu-id="acd40-146">IconIndex</span></span>              | [<span data-ttu-id="acd40-147">Integer</span><span class="sxs-lookup"><span data-stu-id="acd40-147">Integer</span></span>](integer.md)       | <span data-ttu-id="acd40-148">N</span><span class="sxs-lookup"><span data-stu-id="acd40-148">N</span></span>   | <span data-ttu-id="acd40-149">S</span><span class="sxs-lookup"><span data-stu-id="acd40-149">Y</span></span>        |
| <span data-ttu-id="acd40-150">ShowCmd</span><span class="sxs-lookup"><span data-stu-id="acd40-150">ShowCmd</span></span>                | [<span data-ttu-id="acd40-151">Integer</span><span class="sxs-lookup"><span data-stu-id="acd40-151">Integer</span></span>](integer.md)       | <span data-ttu-id="acd40-152">N</span><span class="sxs-lookup"><span data-stu-id="acd40-152">N</span></span>   | <span data-ttu-id="acd40-153">S</span><span class="sxs-lookup"><span data-stu-id="acd40-153">Y</span></span>        |
| <span data-ttu-id="acd40-154">WkDir</span><span class="sxs-lookup"><span data-stu-id="acd40-154">WkDir</span></span>                  | [<span data-ttu-id="acd40-155">Identificatore</span><span class="sxs-lookup"><span data-stu-id="acd40-155">Identifier</span></span>](identifier.md) | <span data-ttu-id="acd40-156">N</span><span class="sxs-lookup"><span data-stu-id="acd40-156">N</span></span>   | <span data-ttu-id="acd40-157">S</span><span class="sxs-lookup"><span data-stu-id="acd40-157">Y</span></span>        |
| <span data-ttu-id="acd40-158">DisplayResourceDLL</span><span class="sxs-lookup"><span data-stu-id="acd40-158">DisplayResourceDLL</span></span>     | [<span data-ttu-id="acd40-159">Formattato</span><span class="sxs-lookup"><span data-stu-id="acd40-159">Formatted</span></span>](formatted.md)   | <span data-ttu-id="acd40-160">N</span><span class="sxs-lookup"><span data-stu-id="acd40-160">N</span></span>   | <span data-ttu-id="acd40-161">S</span><span class="sxs-lookup"><span data-stu-id="acd40-161">Y</span></span>        |
| <span data-ttu-id="acd40-162">DisplayResourceId</span><span class="sxs-lookup"><span data-stu-id="acd40-162">DisplayResourceId</span></span>      | [<span data-ttu-id="acd40-163">Integer</span><span class="sxs-lookup"><span data-stu-id="acd40-163">Integer</span></span>](integer.md)       | <span data-ttu-id="acd40-164">N</span><span class="sxs-lookup"><span data-stu-id="acd40-164">N</span></span>   | <span data-ttu-id="acd40-165">S</span><span class="sxs-lookup"><span data-stu-id="acd40-165">Y</span></span>        |
| <span data-ttu-id="acd40-166">DescriptionResourceDLL</span><span class="sxs-lookup"><span data-stu-id="acd40-166">DescriptionResourceDLL</span></span> | [<span data-ttu-id="acd40-167">Formattato</span><span class="sxs-lookup"><span data-stu-id="acd40-167">Formatted</span></span>](formatted.md)   | <span data-ttu-id="acd40-168">N</span><span class="sxs-lookup"><span data-stu-id="acd40-168">N</span></span>   | <span data-ttu-id="acd40-169">S</span><span class="sxs-lookup"><span data-stu-id="acd40-169">Y</span></span>        |
| <span data-ttu-id="acd40-170">DescriptionResourceId</span><span class="sxs-lookup"><span data-stu-id="acd40-170">DescriptionResourceId</span></span>  | [<span data-ttu-id="acd40-171">Integer</span><span class="sxs-lookup"><span data-stu-id="acd40-171">Integer</span></span>](integer.md)       | <span data-ttu-id="acd40-172">N</span><span class="sxs-lookup"><span data-stu-id="acd40-172">N</span></span>   | <span data-ttu-id="acd40-173">S</span><span class="sxs-lookup"><span data-stu-id="acd40-173">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="acd40-174">Colonne</span><span class="sxs-lookup"><span data-stu-id="acd40-174">Columns</span></span>

<dl> <dt>

<span data-ttu-id="acd40-175"><span id="Shortcut"></span><span id="shortcut"></span><span id="SHORTCUT"></span>Collegamento</span><span class="sxs-lookup"><span data-stu-id="acd40-175"><span id="Shortcut"></span><span id="shortcut"></span><span id="SHORTCUT"></span>Shortcut</span></span>
</dt> <dd>

<span data-ttu-id="acd40-176">Valore della chiave per questa tabella.</span><span class="sxs-lookup"><span data-stu-id="acd40-176">The key value for this table.</span></span>

</dd> <dt>

<span data-ttu-id="acd40-177"><span id="Directory_"></span><span id="directory_"></span><span id="DIRECTORY_"></span>Directory\_</span><span class="sxs-lookup"><span data-stu-id="acd40-177"><span id="Directory_"></span><span id="directory_"></span><span id="DIRECTORY_"></span>Directory\_</span></span>
</dt> <dd>

<span data-ttu-id="acd40-178">Chiave esterna nella prima colonna della [tabella di directory](directory-table.md).</span><span class="sxs-lookup"><span data-stu-id="acd40-178">The external key into the first column of the [Directory table](directory-table.md).</span></span> <span data-ttu-id="acd40-179">Questa colonna specifica la directory in cui viene creato il file di collegamento.</span><span class="sxs-lookup"><span data-stu-id="acd40-179">This column specifies the directory in which the Shortcut file is created.</span></span>

</dd> <dt>

<span data-ttu-id="acd40-180"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Nome</span><span class="sxs-lookup"><span data-stu-id="acd40-180"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span></span>
</dt> <dd>

<span data-ttu-id="acd40-181">Nome localizzabile del collegamento da creare.</span><span class="sxs-lookup"><span data-stu-id="acd40-181">The localizable name of the shortcut to be created.</span></span>

</dd> <dt>

<span data-ttu-id="acd40-182"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_</span><span class="sxs-lookup"><span data-stu-id="acd40-182"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="acd40-183">Chiave esterna nella prima colonna della [tabella dei componenti](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="acd40-183">The external key into the first column of the [Component table](component-table.md).</span></span> <span data-ttu-id="acd40-184">Il programma di installazione utilizza lo stato di installazione del componente specificato in questa colonna per determinare se il collegamento è stato creato o eliminato.</span><span class="sxs-lookup"><span data-stu-id="acd40-184">The installer uses the installation state of the component specified in this column to determine whether the shortcut is created or deleted.</span></span> <span data-ttu-id="acd40-185">Questo componente deve avere un percorso di chiave valido per il collegamento da installare.</span><span class="sxs-lookup"><span data-stu-id="acd40-185">This component must have a valid key path for the shortcut to be installed.</span></span> <span data-ttu-id="acd40-186">Se la colonna di destinazione contiene il nome di una funzionalità, il file avviato dal collegamento è il file di chiave del componente elencato in questa colonna.</span><span class="sxs-lookup"><span data-stu-id="acd40-186">If the Target column contains the name of a feature, the file launched by the shortcut is the key file of the component listed in this column.</span></span>

</dd> <dt>

<span data-ttu-id="acd40-187"><span id="Target"></span><span id="target"></span><span id="TARGET"></span>Destinazione</span><span class="sxs-lookup"><span data-stu-id="acd40-187"><span id="Target"></span><span id="target"></span><span id="TARGET"></span>Target</span></span>
</dt> <dd>

<span data-ttu-id="acd40-188">Destinazione del collegamento.</span><span class="sxs-lookup"><span data-stu-id="acd40-188">The shortcut target.</span></span>

<span data-ttu-id="acd40-189">Per un collegamento annunciato, questa colonna deve essere una chiave esterna nella prima colonna della [tabella delle funzionalità](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="acd40-189">For an advertised shortcut, this column must be an external key into the first column of the [Feature table](feature-table.md).</span></span> <span data-ttu-id="acd40-190">Il programma di installazione valuta la voce nel campo di destinazione come [identificatore](identifier.md) e la voce deve essere una chiave esterna valida nella [tabella delle funzionalità](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="acd40-190">The installer evaluates the entry in the Target field as an [Identifier](identifier.md) and the entry must be a valid foreign key into the [Feature Table](feature-table.md).</span></span> <span data-ttu-id="acd40-191">Il file avviato dal collegamento in questo caso è il file di chiave del componente elencato nella \_ colonna componente.</span><span class="sxs-lookup"><span data-stu-id="acd40-191">The file launched by the shortcut in this case is the key file of the component listed in the Component\_ column.</span></span> <span data-ttu-id="acd40-192">Quando il collegamento viene attivato, il programma di installazione verifica che tutti i componenti della funzionalità siano installati prima di avviare il file.</span><span class="sxs-lookup"><span data-stu-id="acd40-192">When the shortcut is activated, the installer verifies that all the components in the feature are installed before launching this file.</span></span>

<span data-ttu-id="acd40-193">Per un collegamento non annunciato, il programma di installazione valuta questo campo come stringa [formattata](formatted.md) .</span><span class="sxs-lookup"><span data-stu-id="acd40-193">For a non-advertised shortcut, the installer evaluates this field as a [Formatted](formatted.md) string.</span></span> <span data-ttu-id="acd40-194">Il campo deve contenere un identificatore di proprietà racchiuso tra parentesi quadre ( \[ \] ), espanso nel file o in una cartella a cui punta il tasto di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="acd40-194">The field should contains a property identifier enclosed by square brackets (\[ \]), that is expanded into the file or a folder pointed to by the shortcut.</span></span> <span data-ttu-id="acd40-195">Per ulteriori informazioni, vedere l' [azione CreateShortcuts](createshortcuts-action.md).</span><span class="sxs-lookup"><span data-stu-id="acd40-195">For more information, see the [CreateShortcuts action](createshortcuts-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="acd40-196"><span id="Arguments"></span><span id="arguments"></span><span id="ARGUMENTS"></span>Argomenti</span><span class="sxs-lookup"><span data-stu-id="acd40-196"><span id="Arguments"></span><span id="arguments"></span><span id="ARGUMENTS"></span>Arguments</span></span>
</dt> <dd>

<span data-ttu-id="acd40-197">Argomenti della riga di comando per il collegamento.</span><span class="sxs-lookup"><span data-stu-id="acd40-197">The command-line arguments for the shortcut.</span></span>

<span data-ttu-id="acd40-198">Si noti che la risoluzione delle proprietà nel campo arguments è limitata.</span><span class="sxs-lookup"><span data-stu-id="acd40-198">Note that the resolution of properties in the Arguments field is limited.</span></span> <span data-ttu-id="acd40-199">Una proprietà formattata come \[ *Proprietà* \] in questo campo può essere risolta solo se la proprietà dispone già del valore previsto quando il componente proprietario del collegamento è installato.</span><span class="sxs-lookup"><span data-stu-id="acd40-199">A property formatted as \[*Property*\] in this field can only be resolved if the property already has the intended value when the component that owns the shortcut is installed.</span></span> <span data-ttu-id="acd40-200">Ad esempio, per risolvere il valore corretto per l'argomento " \[ \#MyDoc.doc\] ", lo stesso processo deve installare il file MyDoc.doc e il componente proprietario del collegamento.</span><span class="sxs-lookup"><span data-stu-id="acd40-200">For example, to resolve to the correct value for the argument "\[\#MyDoc.doc\]", the same process must be installing the file MyDoc.doc and the component that owns the shortcut.</span></span>

</dd> <dt>

<span data-ttu-id="acd40-201"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Descrizione</span><span class="sxs-lookup"><span data-stu-id="acd40-201"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="acd40-202">Descrizione localizzabile del collegamento.</span><span class="sxs-lookup"><span data-stu-id="acd40-202">The localizable description of the shortcut.</span></span>

</dd> <dt>

<span data-ttu-id="acd40-203"><span id="Hotkey"></span><span id="hotkey"></span><span id="HOTKEY"></span>Hotkey</span><span class="sxs-lookup"><span data-stu-id="acd40-203"><span id="Hotkey"></span><span id="hotkey"></span><span id="HOTKEY"></span>Hotkey</span></span>
</dt> <dd>

<span data-ttu-id="acd40-204">Tasto di scelta rapida per il collegamento.</span><span class="sxs-lookup"><span data-stu-id="acd40-204">The hotkey for the shortcut.</span></span> <span data-ttu-id="acd40-205">Il byte di ordine inferiore contiene il codice della chiave virtuale per la chiave e il byte di ordine superiore contiene i flag di modifica.</span><span class="sxs-lookup"><span data-stu-id="acd40-205">The low-order byte contains the virtual-key code for the key, and the high-order byte contains modifier flags.</span></span> <span data-ttu-id="acd40-206">Deve essere un numero non negativo.</span><span class="sxs-lookup"><span data-stu-id="acd40-206">This must be a non-negative number.</span></span> <span data-ttu-id="acd40-207">Per gli autori dei pacchetti di installazione è in genere consigliabile non impostare questa opzione, perché l'impostazione di questa opzione consente di aggiungere tasti di scelta rapida duplicati al desktop di un utente.</span><span class="sxs-lookup"><span data-stu-id="acd40-207">Authors of installation packages are generally recommended not to set this option, because the setting of this option can add duplicate hotkeys to a user's desktop.</span></span> <span data-ttu-id="acd40-208">Inoltre, la pratica di assegnare tasti di scelta rapida ai collegamenti può risultare problematica per gli utenti che utilizzano tasti di scelta rapida per l' [accessibilità](accessibility.md).</span><span class="sxs-lookup"><span data-stu-id="acd40-208">In addition, the practice of assigning hotkeys to shortcuts can be problematic for users using hotkeys for [accessibility](accessibility.md).</span></span>

</dd> <dt>

<span data-ttu-id="acd40-209"><span id="Icon_"></span><span id="icon_"></span><span id="ICON_"></span>Icona\_</span><span class="sxs-lookup"><span data-stu-id="acd40-209"><span id="Icon_"></span><span id="icon_"></span><span id="ICON_"></span>Icon\_</span></span>
</dt> <dd>

<span data-ttu-id="acd40-210">Chiave esterna per la colonna uno della [tabella delle icone](icon-table.md).</span><span class="sxs-lookup"><span data-stu-id="acd40-210">The external key to column one of the [Icon table](icon-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="acd40-211"><span id="IconIndex"></span><span id="iconindex"></span><span id="ICONINDEX"></span>IconIndex</span><span class="sxs-lookup"><span data-stu-id="acd40-211"><span id="IconIndex"></span><span id="iconindex"></span><span id="ICONINDEX"></span>IconIndex</span></span>
</dt> <dd>

<span data-ttu-id="acd40-212">Indice dell'icona per il collegamento.</span><span class="sxs-lookup"><span data-stu-id="acd40-212">The icon index for the shortcut.</span></span> <span data-ttu-id="acd40-213">Deve essere un numero non negativo.</span><span class="sxs-lookup"><span data-stu-id="acd40-213">This must be a non-negative number.</span></span>

</dd> <dt>

<span data-ttu-id="acd40-214"><span id="ShowCmd"></span><span id="showcmd"></span><span id="SHOWCMD"></span>ShowCmd</span><span class="sxs-lookup"><span data-stu-id="acd40-214"><span id="ShowCmd"></span><span id="showcmd"></span><span id="SHOWCMD"></span>ShowCmd</span></span>
</dt> <dd>

<span data-ttu-id="acd40-215">Comando show per la finestra dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="acd40-215">The Show command for the application window.</span></span>

<span data-ttu-id="acd40-216">È possibile utilizzare i valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="acd40-216">The following values may be used.</span></span> <span data-ttu-id="acd40-217">I valori sono definiti per la funzione API Windows ShowWindow.</span><span class="sxs-lookup"><span data-stu-id="acd40-217">The values are as defined for the Windows API function ShowWindow.</span></span>



| <span data-ttu-id="acd40-218">Valore</span><span class="sxs-lookup"><span data-stu-id="acd40-218">Value</span></span> | <span data-ttu-id="acd40-219">Significato</span><span class="sxs-lookup"><span data-stu-id="acd40-219">Meaning</span></span>             |
|-------|---------------------|
| <span data-ttu-id="acd40-220">1</span><span class="sxs-lookup"><span data-stu-id="acd40-220">1</span></span>     | <span data-ttu-id="acd40-221">\_SHOWNORMAL SW</span><span class="sxs-lookup"><span data-stu-id="acd40-221">SW\_SHOWNORMAL</span></span>      |
| <span data-ttu-id="acd40-222">3</span><span class="sxs-lookup"><span data-stu-id="acd40-222">3</span></span>     | <span data-ttu-id="acd40-223">\_SHOWMAXIMIZED SW</span><span class="sxs-lookup"><span data-stu-id="acd40-223">SW\_SHOWMAXIMIZED</span></span>   |
| <span data-ttu-id="acd40-224">7</span><span class="sxs-lookup"><span data-stu-id="acd40-224">7</span></span>     | <span data-ttu-id="acd40-225">\_SHOWMINNOACTIVE SW</span><span class="sxs-lookup"><span data-stu-id="acd40-225">SW\_SHOWMINNOACTIVE</span></span> |



 

</dd> <dt>

<span data-ttu-id="acd40-226"><span id="WkDir"></span><span id="wkdir"></span><span id="WKDIR"></span>WkDir</span><span class="sxs-lookup"><span data-stu-id="acd40-226"><span id="WkDir"></span><span id="wkdir"></span><span id="WKDIR"></span>WkDir</span></span>
</dt> <dd>

<span data-ttu-id="acd40-227">Nome della proprietà con il percorso della directory di lavoro per il collegamento.</span><span class="sxs-lookup"><span data-stu-id="acd40-227">The name of the property that has the path of the working directory for the shortcut.</span></span> <span data-ttu-id="acd40-228">Il valore può usare il formato Windows per fare riferimento alle variabili di ambiente, ad esempio% USERPROFILE%.</span><span class="sxs-lookup"><span data-stu-id="acd40-228">The value can use the Windows format to reference environment variables, for example %USERPROFILE%.</span></span> <span data-ttu-id="acd40-229">I riferimenti vengono risolti in un percorso effettivo quando il programma di installazione risolve la directory di lavoro per creare il collegamento.</span><span class="sxs-lookup"><span data-stu-id="acd40-229">The references are resolved to an actual path when the installer resolves the working directory to create the shortcut.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="acd40-230"><span id="DisplayResourceDLL"></span><span id="displayresourcedll"></span><span id="DISPLAYRESOURCEDLL"></span>DisplayResourceDLL</span><span class="sxs-lookup"><span data-stu-id="acd40-230"><span id="DisplayResourceDLL"></span><span id="displayresourcedll"></span><span id="DISPLAYRESOURCEDLL"></span>DisplayResourceDLL</span></span>
</dt> <dd>

<span data-ttu-id="acd40-231">Questo campo contiene un valore stringa [formattato](formatted.md) per il percorso completo del file eseguibile portatile indipendente dalla lingua (nel file) che contiene i dati di configurazione della risorsa (configurazione RC).</span><span class="sxs-lookup"><span data-stu-id="acd40-231">This field contains a [Formatted](formatted.md) string value for the full path to the language-neutral portable executable (LN file) that contains the resource configuration (RC Config) data.</span></span> <span data-ttu-id="acd40-232">La stringa formattata può utilizzare la \[ \# \] convenzione FileKey.</span><span class="sxs-lookup"><span data-stu-id="acd40-232">The formatted string can use the \[\#filekey\] convention.</span></span> <span data-ttu-id="acd40-233">Se questo campo contiene un valore, la colonna Name verrà ignorata.</span><span class="sxs-lookup"><span data-stu-id="acd40-233">If this field contains a value, the Name column is ignored.</span></span> <span data-ttu-id="acd40-234">Se il campo è vuoto, il programma di installazione utilizzerà il valore nella colonna nome.</span><span class="sxs-lookup"><span data-stu-id="acd40-234">If this field is empty, the installer uses the value in the Name column.</span></span> <span data-ttu-id="acd40-235">Quando questo campo contiene un valore, anche il campo **DisplayResourceId** deve contenere un valore oppure l'installazione non riesce.</span><span class="sxs-lookup"><span data-stu-id="acd40-235">When this field contains a value, the **DisplayResourceId** field is also required to contain a value, or the installation fails.</span></span>

<span data-ttu-id="acd40-236">Questa colonna della tabella dei collegamenti viene utilizzata solo quando è in esecuzione in Windows Vista o Windows Server 2008 e viene altrimenti ignorata.</span><span class="sxs-lookup"><span data-stu-id="acd40-236">This column of the Shortcut table is used only when running on Windows Vista or Windows Server 2008 and is otherwise ignored.</span></span> <span data-ttu-id="acd40-237">Questa colonna è disponibile con versioni non precedenti a Windows Installer 4,0.</span><span class="sxs-lookup"><span data-stu-id="acd40-237">This column is available with versions not earlier than Windows Installer 4.0.</span></span>

<span data-ttu-id="acd40-238">Per informazioni su come aggiungere collegamenti alla tabella dei collegamenti per l'uso con le risorse MUI, vedere [un esempio di collegamento MUI](a-mui-shortcut-example.md).</span><span class="sxs-lookup"><span data-stu-id="acd40-238">For information about how to add shortcuts to Shortcut table for use with MUI resources see [A MUI Shortcut Example](a-mui-shortcut-example.md).</span></span>

</dd> <dt>

<span data-ttu-id="acd40-239"><span id="DisplayResourceId"></span><span id="displayresourceid"></span><span id="DISPLAYRESOURCEID"></span>DisplayResourceId</span><span class="sxs-lookup"><span data-stu-id="acd40-239"><span id="DisplayResourceId"></span><span id="displayresourceid"></span><span id="DISPLAYRESOURCEID"></span>DisplayResourceId</span></span>
</dt> <dd>

<span data-ttu-id="acd40-240">Indice del nome visualizzato per il collegamento.</span><span class="sxs-lookup"><span data-stu-id="acd40-240">The display name index for the shortcut.</span></span> <span data-ttu-id="acd40-241">Deve essere un numero non negativo.</span><span class="sxs-lookup"><span data-stu-id="acd40-241">This must be a non-negative number.</span></span> <span data-ttu-id="acd40-242">Quando questo campo contiene un valore, il campo **DisplayResourceDLL** è necessario per contenere anche un valore o l'installazione non riesce.</span><span class="sxs-lookup"><span data-stu-id="acd40-242">When this field contains a value, the **DisplayResourceDLL** field is required to also contain a value or the installation fails.</span></span>

<span data-ttu-id="acd40-243">Questa colonna della tabella dei collegamenti viene utilizzata solo quando è in esecuzione in Windows Vista o Windows Server 2008 e viene altrimenti ignorata.</span><span class="sxs-lookup"><span data-stu-id="acd40-243">This column of the Shortcut table is used only when running on Windows Vista or Windows Server 2008 and is otherwise ignored.</span></span> <span data-ttu-id="acd40-244">Questa colonna è disponibile con versioni non precedenti a Windows Installer 4,0.</span><span class="sxs-lookup"><span data-stu-id="acd40-244">This column is available with versions not earlier than Windows Installer 4.0.</span></span>

</dd> <dt>

<span data-ttu-id="acd40-245"><span id="DescriptionResourceDLL"></span><span id="descriptionresourcedll"></span><span id="DESCRIPTIONRESOURCEDLL"></span>DescriptionResourceDLL</span><span class="sxs-lookup"><span data-stu-id="acd40-245"><span id="DescriptionResourceDLL"></span><span id="descriptionresourcedll"></span><span id="DESCRIPTIONRESOURCEDLL"></span>DescriptionResourceDLL</span></span>
</dt> <dd>

<span data-ttu-id="acd40-246">Questo campo contiene un valore stringa [formattato](formatted.md) per il percorso completo del file eseguibile portatile indipendente dalla lingua (nel file) che contiene i dati di configurazione della risorsa (configurazione RC).</span><span class="sxs-lookup"><span data-stu-id="acd40-246">This field contains a [Formatted](formatted.md) string value for the full path to the language-neutral portable executable (LN file) that contains the resource configuration (RC Config) data.</span></span> <span data-ttu-id="acd40-247">La stringa formattata può utilizzare la \[ \# \] convenzione FileKey.</span><span class="sxs-lookup"><span data-stu-id="acd40-247">The formatted string can use the \[\#filekey\] convention.</span></span> <span data-ttu-id="acd40-248">Se questo campo contiene un valore, la colonna Name verrà ignorata.</span><span class="sxs-lookup"><span data-stu-id="acd40-248">If this field contains a value, the Name column is ignored.</span></span> <span data-ttu-id="acd40-249">Se il campo è vuoto, il programma di installazione utilizzerà il valore nella colonna Descrizione.</span><span class="sxs-lookup"><span data-stu-id="acd40-249">If this field is empty, the installer uses the value in the Description column.</span></span> <span data-ttu-id="acd40-250">Quando questo campo contiene un valore, anche il campo **DescriptionResourceId** deve contenere un valore oppure l'installazione non riesce.</span><span class="sxs-lookup"><span data-stu-id="acd40-250">When this field contains a value, the **DescriptionResourceId** field is also required to contain a value, or the installation fails.</span></span>

<span data-ttu-id="acd40-251">Questa colonna della tabella dei collegamenti viene utilizzata solo quando è in esecuzione in Windows Vista o Windows Server 2008 e viene altrimenti ignorata.</span><span class="sxs-lookup"><span data-stu-id="acd40-251">This column of the Shortcut table is used only when running on Windows Vista or Windows Server 2008 and is otherwise ignored.</span></span> <span data-ttu-id="acd40-252">Questa colonna è disponibile con versioni non precedenti a Windows Installer 4,0.</span><span class="sxs-lookup"><span data-stu-id="acd40-252">This column is available with versions not earlier than Windows Installer 4.0.</span></span>

<span data-ttu-id="acd40-253">Per informazioni su come aggiungere collegamenti alla tabella dei collegamenti per l'uso con le risorse MUI, vedere [un esempio di collegamento MUI](a-mui-shortcut-example.md).</span><span class="sxs-lookup"><span data-stu-id="acd40-253">For information about how to add shortcuts to Shortcut table for use with MUI resources see [A MUI Shortcut Example](a-mui-shortcut-example.md).</span></span>

</dd> <dt>

<span data-ttu-id="acd40-254"><span id="DescriptionResourceId"></span><span id="descriptionresourceid"></span><span id="DESCRIPTIONRESOURCEID"></span>DescriptionResourceId</span><span class="sxs-lookup"><span data-stu-id="acd40-254"><span id="DescriptionResourceId"></span><span id="descriptionresourceid"></span><span id="DESCRIPTIONRESOURCEID"></span>DescriptionResourceId</span></span>
</dt> <dd>

<span data-ttu-id="acd40-255">Indice del nome della descrizione per il collegamento.</span><span class="sxs-lookup"><span data-stu-id="acd40-255">The description name index for the shortcut.</span></span> <span data-ttu-id="acd40-256">Deve essere un numero non negativo.</span><span class="sxs-lookup"><span data-stu-id="acd40-256">This must be a non-negative number.</span></span> <span data-ttu-id="acd40-257">Quando questo campo contiene un valore, il campo **DescriptionResourceDLL** è necessario per contenere anche un valore o l'installazione non riesce.</span><span class="sxs-lookup"><span data-stu-id="acd40-257">When this field contains a value, the **DescriptionResourceDLL** field is required to also contain a value or the installation fails.</span></span>

<span data-ttu-id="acd40-258">Questa colonna della tabella dei collegamenti viene utilizzata solo quando è in esecuzione in Windows Vista o Windows Server 2008 e viene altrimenti ignorata.</span><span class="sxs-lookup"><span data-stu-id="acd40-258">This column of the Shortcut table is used only when running on Windows Vista or Windows Server 2008 and is otherwise ignored.</span></span> <span data-ttu-id="acd40-259">Questa colonna è disponibile con versioni non precedenti a Windows Installer 4,0.</span><span class="sxs-lookup"><span data-stu-id="acd40-259">This column is available with versions not earlier than Windows Installer 4.0.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="acd40-260">Commenti</span><span class="sxs-lookup"><span data-stu-id="acd40-260">Remarks</span></span>

<span data-ttu-id="acd40-261">L'abilitazione di una funzionalità consente di creare un collegamento annunciato solo se l'interfaccia IShellLink del sistema supporta la risoluzione del descrittore del programma di installazione.</span><span class="sxs-lookup"><span data-stu-id="acd40-261">The enabling of a feature creates an advertised shortcut only if the system's IShellLink interface supports installer descriptor resolution.</span></span> <span data-ttu-id="acd40-262">Questa operazione è supportata da Microsoft Windows 2000 e dai sistemi che eseguono Microsoft Internet Explorer 4,01.</span><span class="sxs-lookup"><span data-stu-id="acd40-262">This is supported by Microsoft Windows 2000 and systems running Microsoft Internet Explorer 4.01.</span></span> <span data-ttu-id="acd40-263">Se non è supportato, il programma di installazione crea un collegamento non annunciato durante l'installazione del componente della funzionalità, localmente o eseguito dall'origine.</span><span class="sxs-lookup"><span data-stu-id="acd40-263">If unsupported, the installer creates a non-advertised shortcut upon the installation of the feature's component, either locally or run from source.</span></span>

<span data-ttu-id="acd40-264">Si noti che i collegamenti annunciati sempre puntano a una particolare applicazione, identificata da un [**ProductCode**](productcode.md)e non devono essere condivisi tra le applicazioni.</span><span class="sxs-lookup"><span data-stu-id="acd40-264">Note that advertised shortcuts always point at a particular application, identified by a [**ProductCode**](productcode.md), and should not be shared between applications.</span></span> <span data-ttu-id="acd40-265">I collegamenti annunciati funzionano solo per l'applicazione installata più di recente e vengono rimossi quando l'applicazione viene rimossa.</span><span class="sxs-lookup"><span data-stu-id="acd40-265">Advertised shortcuts only work for the most recently installed application, and are removed when that application is removed.</span></span>

<span data-ttu-id="acd40-266">Questa tabella viene definita quando viene eseguita l' [azione CreateShortcuts](createshortcuts-action.md) e l' [azione RemoveShortcuts](removeshortcuts-action.md) .</span><span class="sxs-lookup"><span data-stu-id="acd40-266">This table is referred to when the [CreateShortcuts action](createshortcuts-action.md) and the [RemoveShortcuts action](removeshortcuts-action.md) is executed.</span></span>

<span data-ttu-id="acd40-267">Vedere anche la proprietà [**DISABLEADVTSHORTCUTS**](disableadvtshortcuts.md) .</span><span class="sxs-lookup"><span data-stu-id="acd40-267">See also the [**DISABLEADVTSHORTCUTS**](disableadvtshortcuts.md) property.</span></span>

## <a name="validation"></a><span data-ttu-id="acd40-268">Convalida</span><span class="sxs-lookup"><span data-stu-id="acd40-268">Validation</span></span>

<dl>

[<span data-ttu-id="acd40-269">ICE03</span><span class="sxs-lookup"><span data-stu-id="acd40-269">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="acd40-270">ICE06</span><span class="sxs-lookup"><span data-stu-id="acd40-270">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="acd40-271">ICE19</span><span class="sxs-lookup"><span data-stu-id="acd40-271">ICE19</span></span>](ice19.md)  
[<span data-ttu-id="acd40-272">ICE32</span><span class="sxs-lookup"><span data-stu-id="acd40-272">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="acd40-273">ICE36</span><span class="sxs-lookup"><span data-stu-id="acd40-273">ICE36</span></span>](ice36.md)  
[<span data-ttu-id="acd40-274">ICE46</span><span class="sxs-lookup"><span data-stu-id="acd40-274">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="acd40-275">ICE50</span><span class="sxs-lookup"><span data-stu-id="acd40-275">ICE50</span></span>](ice50.md)  
[<span data-ttu-id="acd40-276">ICE57</span><span class="sxs-lookup"><span data-stu-id="acd40-276">ICE57</span></span>](ice57.md)  
[<span data-ttu-id="acd40-277">ICE59</span><span class="sxs-lookup"><span data-stu-id="acd40-277">ICE59</span></span>](ice59.md)  
[<span data-ttu-id="acd40-278">ICE67</span><span class="sxs-lookup"><span data-stu-id="acd40-278">ICE67</span></span>](ice67.md)  
[<span data-ttu-id="acd40-279">ICE69</span><span class="sxs-lookup"><span data-stu-id="acd40-279">ICE69</span></span>](ice69.md)  
[<span data-ttu-id="acd40-280">ICE80</span><span class="sxs-lookup"><span data-stu-id="acd40-280">ICE80</span></span>](ice80.md)  
[<span data-ttu-id="acd40-281">ICE90</span><span class="sxs-lookup"><span data-stu-id="acd40-281">ICE90</span></span>](ice90.md)  
[<span data-ttu-id="acd40-282">ICE91</span><span class="sxs-lookup"><span data-stu-id="acd40-282">ICE91</span></span>](ice91.md)  
[<span data-ttu-id="acd40-283">ICE94</span><span class="sxs-lookup"><span data-stu-id="acd40-283">ICE94</span></span>](ice94.md)  
</dl>

 

 



