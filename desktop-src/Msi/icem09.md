---
description: ICEM09 verifica che il modulo unione gestisca in modo sicuro le directory predefinite.
ms.assetid: 747ae5ee-adc1-4aa7-8239-2379f76bfd0f
title: ICEM09
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee4b4d2d52c35d6dd3670daff5150a785e19d0b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232446"
---
# <a name="icem09"></a><span data-ttu-id="54644-103">ICEM09</span><span class="sxs-lookup"><span data-stu-id="54644-103">ICEM09</span></span>

<span data-ttu-id="54644-104">ICEM09 verifica che il modulo unione gestisca in modo sicuro le directory predefinite.</span><span class="sxs-lookup"><span data-stu-id="54644-104">ICEM09 verifies the merge module safely handles predefined directories.</span></span> <span data-ttu-id="54644-105">Questa operazione viene eseguita verificando che nessun componente del modulo installi una directory in una directory di sistema predefinita, ad esempio "ProgramFilesFolder" o "dei".</span><span class="sxs-lookup"><span data-stu-id="54644-105">It does this by verifying that no component in the module installs a directory to a predefined system directory such as "ProgramFilesFolder" or "StartMenuFolder".</span></span> <span data-ttu-id="54644-106">I moduli devono invece usare directory con nomi univoci (creati con la convenzione di denominazione del modulo merge) e usare azioni personalizzate per la directory di destinazione appropriata.</span><span class="sxs-lookup"><span data-stu-id="54644-106">Instead, modules should use directories with unique names (created with the merge module naming convention) and use custom actions to target the appropriate target directory.</span></span> <span data-ttu-id="54644-107">Questo approccio impedisce ai moduli di entrare in conflitto con una struttura di directory esistente nel database finale.</span><span class="sxs-lookup"><span data-stu-id="54644-107">This approach prevents modules from conflicting with an existing directory structure in the final database.</span></span> <span data-ttu-id="54644-108">ICEM09 verifica che le azioni personalizzate necessarie per il funzionamento di questa tecnica non esistano (in modo che lo strumento di merge possa generarle) o esistano nel formato corretto (in modo che funzionino come previsto).</span><span class="sxs-lookup"><span data-stu-id="54644-108">ICEM09 checks that the custom actions needed for this technique to work either do not exist (so that the merge tool can generate them) or exist in the correct form (so that they work as expected).</span></span>

<span data-ttu-id="54644-109">La mancata correzione di un avviso o di un errore segnalato da ICEM09 potrebbe causare problemi per i client del modulo merge.</span><span class="sxs-lookup"><span data-stu-id="54644-109">Failure to fix a warning or error reported by ICEM09 could cause problems for the clients of your merge module.</span></span> <span data-ttu-id="54644-110">Le righe della tabella di directory con chiavi primarie, ad esempio ProgramFilesFolder, sono spesso presenti in un database. Se pertanto i componenti del modulo vengono installati direttamente in directory predefinite, ad esempio ProgramFilesFolder, è possibile che le voci di directory del modulo entrino in conflitto con le righe già esistenti.</span><span class="sxs-lookup"><span data-stu-id="54644-110">Directory table rows with primary keys such as ProgramFilesFolder often exist in a database; therefore, if components in your module install directly to predefined directories such as ProgramFilesFolder, the directory entries in the module may collide with already existing rows.</span></span> <span data-ttu-id="54644-111">Questa condizione richiede che l'utente del modulo suddivida i file di origine dal modulo per poter corrispondere alla directory di origine esistente.</span><span class="sxs-lookup"><span data-stu-id="54644-111">This condition would require the user of your module to split the source files from your module in order to match the existing source directory.</span></span>

## <a name="result"></a><span data-ttu-id="54644-112">Risultato</span><span class="sxs-lookup"><span data-stu-id="54644-112">Result</span></span>

<span data-ttu-id="54644-113">ICEM09 segnala un errore o un avviso quando un componente del modulo installa una directory in una directory di sistema predefinita, causando un possibile conflitto di nomi con la struttura di directory esistente.</span><span class="sxs-lookup"><span data-stu-id="54644-113">ICEM09 reports an error or warning when a module component installs a directory to a pre-defined system directory, causing a possible name conflict with the existing directory structure.</span></span>

## <a name="example"></a><span data-ttu-id="54644-114">Esempio</span><span class="sxs-lookup"><span data-stu-id="54644-114">Example</span></span>

<span data-ttu-id="54644-115">ICEM09 invia gli avvisi seguenti per un modulo contenente le voci di database visualizzate.</span><span class="sxs-lookup"><span data-stu-id="54644-115">ICEM09 posts the following warnings for a module containing the database entries shown.</span></span>

``` syntax
Warning: The component 'Component1.<GUID>' installs directly into the pre-defined 
directory 'ProgramFilesFolder'. It is recommended that merge modules alias 
all such directories to unique names.
```

<span data-ttu-id="54644-116">Rinominare la directory del modulo merge in modo che non corrisponda a una proprietà di Windows Installer e pertanto sia univoca.</span><span class="sxs-lookup"><span data-stu-id="54644-116">Rename the merge module directory so it does not match a Windows Installer property and therefore is unique.</span></span> <span data-ttu-id="54644-117">Impostare quindi una proprietà con lo stesso nome sul valore della directory Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="54644-117">Then set a property of the same name to the value of the Windows Installer directory.</span></span> <span data-ttu-id="54644-118">Quando si verifica la risoluzione della directory, la directory ha una proprietà con lo stesso nome, quindi il percorso di installazione della directory corrisponde al valore della proprietà.</span><span class="sxs-lookup"><span data-stu-id="54644-118">When directory resolution takes place, the directory has a property of the same name, so the install location of the directory is the value of the property.</span></span> <span data-ttu-id="54644-119">I file passano dalla posizione di origine distinta allo stesso percorso di destinazione.</span><span class="sxs-lookup"><span data-stu-id="54644-119">Files move from the distinct source location to the same target location.</span></span> <span data-ttu-id="54644-120">Questo processo dovrebbe rimuovere completamente i conflitti di Unione.</span><span class="sxs-lookup"><span data-stu-id="54644-120">This process should completely remove the merge conflicts.</span></span>

``` syntax
Warning: The 'ModuleInstallExecuteSequence' table contains a type 51 action 
(StartMenuFolder.<GUID>) for a pre-defined directory, but this action 
does not have sequence number '1'
```

<span data-ttu-id="54644-121">Se per l'azione non è presente il numero di sequenza 1, è possibile che non venga eseguito il merge del database di destinazione abbastanza presto nella sequenza per funzionare in modo efficace.</span><span class="sxs-lookup"><span data-stu-id="54644-121">If the action does not have sequence number 1, it may not merge in to the target database early enough in the sequence to work effectively.</span></span>

<span data-ttu-id="54644-122">Per correggere il problema, impostare il numero di sequenza su 1.</span><span class="sxs-lookup"><span data-stu-id="54644-122">To fix this warning, set the sequence number to 1.</span></span> <span data-ttu-id="54644-123">Si noti che la maggior parte degli strumenti di merge correnti (ma non alcune versioni precedenti) genera queste azioni personalizzate in fase di merge, pertanto non è sempre necessario creare esplicitamente le azioni nel modulo merge.</span><span class="sxs-lookup"><span data-stu-id="54644-123">Note that most current merge tools (but not some older versions) will generate these custom actions at merge time, so it is not always necessary to explicitly author the actions into the merge module.</span></span>

``` syntax
Warning: The 'CustomAction' table contains a type 51 action (MyAppDataFolderAction) 
for a pre-defined directory, but the name is not the same as the target directory. 
Many merge tools will generate duplicate actions."
```

<span data-ttu-id="54644-124">Poiché la colonna CustomAction è la chiave primaria della tabella CustomAction, alcuni strumenti di merge possono generare azioni duplicate poiché il nome dell'azione creato in precedenza è diverso.</span><span class="sxs-lookup"><span data-stu-id="54644-124">Because the CustomAction column is the primary key of CustomAction table, some merge tools may generate duplicate actions because the pre-authored action name is different.</span></span>

<span data-ttu-id="54644-125">Per correggere il problema, denominare l'azione come la directory di destinazione.</span><span class="sxs-lookup"><span data-stu-id="54644-125">To fix this warning, name the action the same as the target directory.</span></span> <span data-ttu-id="54644-126">Si noti che la maggior parte degli strumenti di merge correnti (ma non alcune versioni precedenti) genera queste azioni personalizzate in fase di merge, pertanto non è sempre necessario creare esplicitamente le azioni nel modulo merge.</span><span class="sxs-lookup"><span data-stu-id="54644-126">Note that most current merge tools (but not some older versions) generate these custom actions at merge time, so it is not always necessary to explicitly author the actions into the merge module.</span></span>

[<span data-ttu-id="54644-127">Tabella directory</span><span class="sxs-lookup"><span data-stu-id="54644-127">Directory Table</span></span>](directory-table.md)



| <span data-ttu-id="54644-128">Directory</span><span class="sxs-lookup"><span data-stu-id="54644-128">Directory</span></span>          | <span data-ttu-id="54644-129">\_Padre directory</span><span class="sxs-lookup"><span data-stu-id="54644-129">Directory\_Parent</span></span> | <span data-ttu-id="54644-130">DefaultDir</span><span class="sxs-lookup"><span data-stu-id="54644-130">DefaultDir</span></span> |
|--------------------|-------------------|------------|
| <span data-ttu-id="54644-131">ProgramFilesFolder</span><span class="sxs-lookup"><span data-stu-id="54644-131">ProgramFilesFolder</span></span> | <span data-ttu-id="54644-132">Directory1</span><span class="sxs-lookup"><span data-stu-id="54644-132">Directory1</span></span>        | <span data-ttu-id="54644-133">A</span><span class="sxs-lookup"><span data-stu-id="54644-133">A</span></span>          |
| <span data-ttu-id="54644-134">Dei</span><span class="sxs-lookup"><span data-stu-id="54644-134">StartMenuFolder</span></span>    | <span data-ttu-id="54644-135">Directory2</span><span class="sxs-lookup"><span data-stu-id="54644-135">Directory2</span></span>        | <span data-ttu-id="54644-136">B:C</span><span class="sxs-lookup"><span data-stu-id="54644-136">B:C</span></span>        |
| <span data-ttu-id="54644-137">CartellaDatiApp</span><span class="sxs-lookup"><span data-stu-id="54644-137">AppDataFolder</span></span>      | <span data-ttu-id="54644-138">Directory3</span><span class="sxs-lookup"><span data-stu-id="54644-138">Directory3</span></span>        | <span data-ttu-id="54644-139">D</span><span class="sxs-lookup"><span data-stu-id="54644-139">D</span></span>          |
| <span data-ttu-id="54644-140">MyPicturesFolder</span><span class="sxs-lookup"><span data-stu-id="54644-140">MyPicturesFolder</span></span>   | <span data-ttu-id="54644-141">Directory4</span><span class="sxs-lookup"><span data-stu-id="54644-141">Directory4</span></span>        | <span data-ttu-id="54644-142">E</span><span class="sxs-lookup"><span data-stu-id="54644-142">E</span></span>          |



 

[<span data-ttu-id="54644-143">Tabella componenti</span><span class="sxs-lookup"><span data-stu-id="54644-143">Component Table</span></span>](component-table.md)



| <span data-ttu-id="54644-144">Componente</span><span class="sxs-lookup"><span data-stu-id="54644-144">Component</span></span>               | <span data-ttu-id="54644-145">Directory</span><span class="sxs-lookup"><span data-stu-id="54644-145">Directory</span></span>          |
|-------------------------|--------------------|
| <span data-ttu-id="54644-146">Component1.<GUID></span><span class="sxs-lookup"><span data-stu-id="54644-146">Component1.<GUID></span></span> | <span data-ttu-id="54644-147">ProgramFilesFolder</span><span class="sxs-lookup"><span data-stu-id="54644-147">ProgramFilesFolder</span></span> |
| <span data-ttu-id="54644-148">Component2.<GUID></span><span class="sxs-lookup"><span data-stu-id="54644-148">Component2.<GUID></span></span> | <span data-ttu-id="54644-149">Dei</span><span class="sxs-lookup"><span data-stu-id="54644-149">StartMenuFolder</span></span>    |
| <span data-ttu-id="54644-150">Component3.<GUID></span><span class="sxs-lookup"><span data-stu-id="54644-150">Component3.<GUID></span></span> | <span data-ttu-id="54644-151">CartellaDatiApp</span><span class="sxs-lookup"><span data-stu-id="54644-151">AppDataFolder</span></span>      |
| <span data-ttu-id="54644-152">Component4.<GUID></span><span class="sxs-lookup"><span data-stu-id="54644-152">Component4.<GUID></span></span> | <span data-ttu-id="54644-153">MyPicturesFolder</span><span class="sxs-lookup"><span data-stu-id="54644-153">MyPicturesFolder</span></span>   |



 

[<span data-ttu-id="54644-154">Tabella CustomAction</span><span class="sxs-lookup"><span data-stu-id="54644-154">CustomAction Table</span></span>](customaction-table.md)



| <span data-ttu-id="54644-155">CustomAction</span><span class="sxs-lookup"><span data-stu-id="54644-155">CustomAction</span></span>                 | <span data-ttu-id="54644-156">Tipo</span><span class="sxs-lookup"><span data-stu-id="54644-156">Type</span></span> | <span data-ttu-id="54644-157">Source (Sorgente)</span><span class="sxs-lookup"><span data-stu-id="54644-157">Source</span></span>                       | <span data-ttu-id="54644-158">Destinazione</span><span class="sxs-lookup"><span data-stu-id="54644-158">Target</span></span>              |
|------------------------------|------|------------------------------|---------------------|
| <span data-ttu-id="54644-159">Dei.<GUID></span><span class="sxs-lookup"><span data-stu-id="54644-159">StartMenuFolder.<GUID></span></span> | <span data-ttu-id="54644-160">51</span><span class="sxs-lookup"><span data-stu-id="54644-160">51</span></span>   | <span data-ttu-id="54644-161">Dei.<GUID></span><span class="sxs-lookup"><span data-stu-id="54644-161">StartMenuFolder.<GUID></span></span> | <span data-ttu-id="54644-162">\[Dei\]</span><span class="sxs-lookup"><span data-stu-id="54644-162">\[StartMenuFolder\]</span></span> |
| <span data-ttu-id="54644-163">MyAppDataFolderAction</span><span class="sxs-lookup"><span data-stu-id="54644-163">MyAppDataFolderAction</span></span>        | <span data-ttu-id="54644-164">51</span><span class="sxs-lookup"><span data-stu-id="54644-164">51</span></span>   | <span data-ttu-id="54644-165">CartellaDatiApp.<GUID></span><span class="sxs-lookup"><span data-stu-id="54644-165">AppDataFolder.<GUID></span></span>   | <span data-ttu-id="54644-166">\[CartellaDatiApp\]</span><span class="sxs-lookup"><span data-stu-id="54644-166">\[AppDataFolder\]</span></span>   |



 

[<span data-ttu-id="54644-167">Tabella ModuleInstallExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="54644-167">ModuleInstallExecuteSequence Table</span></span>](moduleinstallexecutesequence-table.md)



| <span data-ttu-id="54644-168">Azione</span><span class="sxs-lookup"><span data-stu-id="54644-168">Action</span></span>                       | <span data-ttu-id="54644-169">Sequenza</span><span class="sxs-lookup"><span data-stu-id="54644-169">Sequence</span></span> | <span data-ttu-id="54644-170">BaseAction</span><span class="sxs-lookup"><span data-stu-id="54644-170">BaseAction</span></span> | <span data-ttu-id="54644-171">After</span><span class="sxs-lookup"><span data-stu-id="54644-171">After</span></span> | <span data-ttu-id="54644-172">Condizione</span><span class="sxs-lookup"><span data-stu-id="54644-172">Condition</span></span> |
|------------------------------|----------|------------|-------|-----------|
| <span data-ttu-id="54644-173">Dei.<GUID></span><span class="sxs-lookup"><span data-stu-id="54644-173">StartMenuFolder.<GUID></span></span> | <span data-ttu-id="54644-174">100</span><span class="sxs-lookup"><span data-stu-id="54644-174">100</span></span>      |            |       |           |



 

## <a name="related-topics"></a><span data-ttu-id="54644-175">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="54644-175">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="54644-176">Riferimento ghiaccio del modulo merge</span><span class="sxs-lookup"><span data-stu-id="54644-176">Merge Module ICE Reference</span></span>](merge-module-ice-reference.md)
</dt> </dl>

 

 



