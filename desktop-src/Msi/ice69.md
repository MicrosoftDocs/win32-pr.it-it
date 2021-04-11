---
description: ICE69 verifica che tutte le sottostringhe del form \[ $componentkey \] all'interno di una stringa formattata non rimandino i componenti.
ms.assetid: 6ab8f3b7-19e9-46f3-b09e-36bdb43d6f55
title: ICE69
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95bd00efc6b141bfa872470adcc9e88a63a2c52d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233158"
---
# <a name="ice69"></a><span data-ttu-id="717e6-103">ICE69</span><span class="sxs-lookup"><span data-stu-id="717e6-103">ICE69</span></span>

<span data-ttu-id="717e6-104">ICE69 verifica che tutte le sottostringhe del form \[ $componentkey \] all'interno di una stringa [formattata](formatted.md) non rimandino i componenti.</span><span class="sxs-lookup"><span data-stu-id="717e6-104">ICE69 checks that all substrings of the form \[$componentkey\] within a [formatted](formatted.md) string do not cross-reference components.</span></span> <span data-ttu-id="717e6-105">Un riferimento tra componenti si verifica quando la \[ \] Proprietà $componentkey di una stringa formattata fa riferimento a un componente diverso dal componente archiviato nella \_ colonna componente delle tabelle.</span><span class="sxs-lookup"><span data-stu-id="717e6-105">A cross-component reference occurs when the \[$componentkey\] property of a formatted string refers to a component other than the component stored in the Component\_ column of your tables.</span></span>

<span data-ttu-id="717e6-106">I problemi relativi al riferimento tra componenti si verificano dal modo in cui vengono valutate le stringhe [formattate](formatted.md) .</span><span class="sxs-lookup"><span data-stu-id="717e6-106">Problems with cross-component referencing arise from the way [formatted](formatted.md) strings are evaluated.</span></span> <span data-ttu-id="717e6-107">Se il componente a cui si fa riferimento con la \[ \] Proprietà $componentkey è già installato e non viene modificato durante l'installazione corrente (ad esempio, in fase di reinstallazione, spostato nell'origine e così via), l'espressione \[ $componentkey \] restituisce null, perché lo stato dell'azione del componente in \[ $componentkey \] è null.</span><span class="sxs-lookup"><span data-stu-id="717e6-107">If the component referenced with the \[$componentkey\] property is already installed and is not being changed during the current installation (for example, being reinstalled, moved to source, and so forth), the expression \[$componentkey\] evaluates to null, because the action state of the component in \[$componentkey\] is null.</span></span> <span data-ttu-id="717e6-108">Problemi simili possono verificarsi durante le operazioni di aggiornamento e ripristino.</span><span class="sxs-lookup"><span data-stu-id="717e6-108">Similar problems can occur during upgrade and repair operations.</span></span>

## <a name="result"></a><span data-ttu-id="717e6-109">Risultato</span><span class="sxs-lookup"><span data-stu-id="717e6-109">Result</span></span>

<span data-ttu-id="717e6-110">ICE69 restituisce un errore se una \[ \] sottostringa $componentkey all'interno di una stringa [formattata](formatted.md) fa riferimento a un componente in un'altra funzionalità.</span><span class="sxs-lookup"><span data-stu-id="717e6-110">ICE69 returns an error if a \[$componentkey\] substring within a [formatted](formatted.md) string cross-references a component in another feature.</span></span> <span data-ttu-id="717e6-111">ICE69 restituisce un avviso se una \[ \] sottostringa $componentkey all'interno di una stringa formattata fa riferimento a un componente nella stessa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="717e6-111">ICE69 returns a warning if a \[$componentkey\] substring within a formatted string cross-references a component in the same feature.</span></span> <span data-ttu-id="717e6-112">La tabella [FeatureComponents](featurecomponents-table.md) viene utilizzata per determinare questo mapping.</span><span class="sxs-lookup"><span data-stu-id="717e6-112">(The [FeatureComponents](featurecomponents-table.md) table is used to determine this mapping.</span></span> <span data-ttu-id="717e6-113">Deve eseguire il mapping alla stessa funzionalità per l'avviso.</span><span class="sxs-lookup"><span data-stu-id="717e6-113">It must map to the same feature for the warning.</span></span> <span data-ttu-id="717e6-114">Il riferimento ai componenti nelle funzionalità padre o ai componenti di riferimento nelle funzionalità figlio viene considerato un errore.</span><span class="sxs-lookup"><span data-stu-id="717e6-114">Referencing components in parent features or referencing components in child features is considered to be an error.)</span></span>

<span data-ttu-id="717e6-115">ICE69 segnala un errore se la \[ \# \] sottostringa FileKey all'interno di una stringa [formattata](formatted.md) fa riferimento a un file non specificato nella tabella [file](file-table.md) come appartenente allo stesso componente.</span><span class="sxs-lookup"><span data-stu-id="717e6-115">ICE69 reports an error if the \[\#FileKey\] substring within a [formatted](formatted.md) string references a file which is not specified in the [File](file-table.md) table as belonging to the same component.</span></span>

## <a name="example"></a><span data-ttu-id="717e6-116">Esempio</span><span class="sxs-lookup"><span data-stu-id="717e6-116">Example</span></span>

<span data-ttu-id="717e6-117">ICE69 segnala gli esempi riportati di seguito.</span><span class="sxs-lookup"><span data-stu-id="717e6-117">ICE69 reports the following for the examples shown.</span></span>

``` syntax
WARNING: "Mismatched component reference. Entry 'Test' of the Shortcut table belongs to component 'QuickTest'. However, the formatted string in column 'Argument' references component 'Test'. Components are in the same feature."
ERROR: "Mismatched component reference. Entry 'Shortcut2' of the Shortcut table belongs to component 'QuickTest'. However, the formatted string in column 'Argument' references component 'Test2'. Components are not in the same feature."
```

<span data-ttu-id="717e6-118">Per correggere l'errore, non fare riferimento a componenti incrociati.</span><span class="sxs-lookup"><span data-stu-id="717e6-118">To fix this error, do not cross-reference components.</span></span> <span data-ttu-id="717e6-119">Modificare il \[ $componentkey \] in modo che corrisponda al componente del collegamento.</span><span class="sxs-lookup"><span data-stu-id="717e6-119">Change the \[$componentkey\] to match the component of the shortcut.</span></span>

<span data-ttu-id="717e6-120">[Tabella collegamenti](shortcut-table.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="717e6-120">[Shortcut Table](shortcut-table.md) (partial)</span></span>



| <span data-ttu-id="717e6-121">Tasto di scelta rapida</span><span class="sxs-lookup"><span data-stu-id="717e6-121">Shortcut</span></span>  | <span data-ttu-id="717e6-122">Componente\_</span><span class="sxs-lookup"><span data-stu-id="717e6-122">Component\_</span></span> | <span data-ttu-id="717e6-123">Argomento</span><span class="sxs-lookup"><span data-stu-id="717e6-123">Argument</span></span>     |
|-----------|-------------|--------------|
| <span data-ttu-id="717e6-124">Test</span><span class="sxs-lookup"><span data-stu-id="717e6-124">Test</span></span>      | <span data-ttu-id="717e6-125">QuickTest</span><span class="sxs-lookup"><span data-stu-id="717e6-125">QuickTest</span></span>   | <span data-ttu-id="717e6-126">-v \[ $test\]</span><span class="sxs-lookup"><span data-stu-id="717e6-126">-v \[$Test\]</span></span> |
| <span data-ttu-id="717e6-127">Shortcut2</span><span class="sxs-lookup"><span data-stu-id="717e6-127">Shortcut2</span></span> | <span data-ttu-id="717e6-128">QuickTest</span><span class="sxs-lookup"><span data-stu-id="717e6-128">QuickTest</span></span>   | <span data-ttu-id="717e6-129">\[$Test 2\]</span><span class="sxs-lookup"><span data-stu-id="717e6-129">\[$Test2\]</span></span>   |



 

<span data-ttu-id="717e6-130">Le tabelle dei [verbi](verb-table.md) e delle [estensioni](extension-table.md) sono casi speciali in quanto la tabella dei verbi fa riferimento a un'estensione che appartiene a un componente.</span><span class="sxs-lookup"><span data-stu-id="717e6-130">The [Verb](verb-table.md) and [Extension](extension-table.md) tables are special cases in that the Verb table references an extension that belongs to a component.</span></span> <span data-ttu-id="717e6-131">Un'estensione, tuttavia, può appartenere a più componenti perché la chiave primaria per la tabella di estensione è costituita dalle colonne Extension e Component \_ .</span><span class="sxs-lookup"><span data-stu-id="717e6-131">An Extension, however, can belong to multiple components because the primary key for the extension table is made up of the Extension and Component\_ columns.</span></span> <span data-ttu-id="717e6-132">È possibile che si verifichino logicamente le situazioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="717e6-132">You can logically have the following situation.</span></span>

<span data-ttu-id="717e6-133">[Tabella Verb](verb-table.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="717e6-133">[Verb Table](verb-table.md) (partial)</span></span>



| <span data-ttu-id="717e6-134">Estensione</span><span class="sxs-lookup"><span data-stu-id="717e6-134">Extension</span></span> | <span data-ttu-id="717e6-135">Verbo\_</span><span class="sxs-lookup"><span data-stu-id="717e6-135">Verb\_</span></span> | <span data-ttu-id="717e6-136">Argomento</span><span class="sxs-lookup"><span data-stu-id="717e6-136">Argument</span></span>                |
|-----------|--------|-------------------------|
| <span data-ttu-id="717e6-137">TST</span><span class="sxs-lookup"><span data-stu-id="717e6-137">tst</span></span>       | <span data-ttu-id="717e6-138">apre</span><span class="sxs-lookup"><span data-stu-id="717e6-138">open</span></span>   | <span data-ttu-id="717e6-139">-v \[ $comp 1 \] \[ $comp 2\]</span><span class="sxs-lookup"><span data-stu-id="717e6-139">-v \[$comp1\]\[$comp2\]</span></span> |



 

<span data-ttu-id="717e6-140">[Tabella di estensione](extension-table.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="717e6-140">[Extension Table](extension-table.md) (partial)</span></span>



| <span data-ttu-id="717e6-141">Estensione</span><span class="sxs-lookup"><span data-stu-id="717e6-141">Extension</span></span> | <span data-ttu-id="717e6-142">Componente\_</span><span class="sxs-lookup"><span data-stu-id="717e6-142">Component\_</span></span> |
|-----------|-------------|
| <span data-ttu-id="717e6-143">TST</span><span class="sxs-lookup"><span data-stu-id="717e6-143">tst</span></span>       | <span data-ttu-id="717e6-144">Comp1</span><span class="sxs-lookup"><span data-stu-id="717e6-144">comp1</span></span>       |
| <span data-ttu-id="717e6-145">TST</span><span class="sxs-lookup"><span data-stu-id="717e6-145">tst</span></span>       | <span data-ttu-id="717e6-146">Comp2</span><span class="sxs-lookup"><span data-stu-id="717e6-146">comp2</span></span>       |



 

[<span data-ttu-id="717e6-147">Tabella FeatureComponents</span><span class="sxs-lookup"><span data-stu-id="717e6-147">FeatureComponents Table</span></span>](featurecomponents-table.md)



| <span data-ttu-id="717e6-148">Funzionalità\_</span><span class="sxs-lookup"><span data-stu-id="717e6-148">Feature\_</span></span> | <span data-ttu-id="717e6-149">Componente\_</span><span class="sxs-lookup"><span data-stu-id="717e6-149">Component\_</span></span> |
|-----------|-------------|
| <span data-ttu-id="717e6-150">Feature1</span><span class="sxs-lookup"><span data-stu-id="717e6-150">Feature1</span></span>  | <span data-ttu-id="717e6-151">QuickTest</span><span class="sxs-lookup"><span data-stu-id="717e6-151">QuickTest</span></span>   |
| <span data-ttu-id="717e6-152">Feature1</span><span class="sxs-lookup"><span data-stu-id="717e6-152">Feature1</span></span>  | <span data-ttu-id="717e6-153">Test</span><span class="sxs-lookup"><span data-stu-id="717e6-153">Test</span></span>        |
| <span data-ttu-id="717e6-154">Funzionalità2</span><span class="sxs-lookup"><span data-stu-id="717e6-154">Feature2</span></span>  | <span data-ttu-id="717e6-155">Test2</span><span class="sxs-lookup"><span data-stu-id="717e6-155">Test2</span></span>       |



 

<span data-ttu-id="717e6-156">In questo caso, è necessario assicurarsi che almeno una delle \[ \] Proprietà $componentkey restituisca un valore non null.</span><span class="sxs-lookup"><span data-stu-id="717e6-156">In this case, you must ensure that at least one of the \[$componentkey\] properties evaluates to a non-null value.</span></span> <span data-ttu-id="717e6-157">Ogni \[ $componentkey \] proprietà nella colonna Argument della tabella Verb ( \[ $comp 1 \] e \[ $comp 2 \] nell'esempio precedente), tuttavia, deve fare riferimento a un componente possibile incluso con l'estensione associata al verbo.</span><span class="sxs-lookup"><span data-stu-id="717e6-157">However, every \[$componentkey\] property in the Argument column of the Verb table (\[$comp1\] and \[$comp2\] in the above example) must reference a possible component included with the extension associated with the verb.</span></span> <span data-ttu-id="717e6-158">Un riferimento come \[ $COMP 3 \] genera un avviso da ICE69.</span><span class="sxs-lookup"><span data-stu-id="717e6-158">A reference like \[$comp3\] would result in a warning from ICE69.</span></span>

<span data-ttu-id="717e6-159">La [tabella AppID](appid-table.md) presenta una situazione simile alla tabella dei verbi.</span><span class="sxs-lookup"><span data-stu-id="717e6-159">The [AppId table](appid-table.md) has a similar situation to the Verb table.</span></span> <span data-ttu-id="717e6-160">Usa la [tabella delle classi](class-table.md) per il riferimento al componente.</span><span class="sxs-lookup"><span data-stu-id="717e6-160">It uses the [Class table](class-table.md) for its component reference.</span></span> <span data-ttu-id="717e6-161">In questo caso, la tabella AppId viene convalidata allo stesso modo della convalida Verb-Extension (ora AppId-Class).</span><span class="sxs-lookup"><span data-stu-id="717e6-161">In this case, the AppId table is validated in the same way as the Verb-Extension validation (now AppId-Class).</span></span>

<span data-ttu-id="717e6-162">La colonna Argument della tabella della classe viene convalidata come il [collegamento](shortcut-table.md), il [Registro di sistema](registry-table.md)e tabelle simili.</span><span class="sxs-lookup"><span data-stu-id="717e6-162">The Class table's Argument column is validated like the [Shortcut](shortcut-table.md), [Registry](registry-table.md), and similar tables.</span></span>

## <a name="table-used-during-execution-only-if-found"></a><span data-ttu-id="717e6-163">Tabella utilizzata durante l'esecuzione (solo se trovata)</span><span class="sxs-lookup"><span data-stu-id="717e6-163">Table used during execution (only if found)</span></span>

[<span data-ttu-id="717e6-164">IniFile</span><span class="sxs-lookup"><span data-stu-id="717e6-164">IniFile</span></span>](inifile-table.md)

[<span data-ttu-id="717e6-165">RemoveIniFile</span><span class="sxs-lookup"><span data-stu-id="717e6-165">RemoveIniFile</span></span>](removeinifile-table.md)

[<span data-ttu-id="717e6-166">Registro</span><span class="sxs-lookup"><span data-stu-id="717e6-166">Registry</span></span>](registry-table.md)

[<span data-ttu-id="717e6-167">RemoveRegistry</span><span class="sxs-lookup"><span data-stu-id="717e6-167">RemoveRegistry</span></span>](removeregistry-table.md)

[<span data-ttu-id="717e6-168">ServiceControl</span><span class="sxs-lookup"><span data-stu-id="717e6-168">ServiceControl</span></span>](servicecontrol-table.md)

[<span data-ttu-id="717e6-169">ServiceInstall</span><span class="sxs-lookup"><span data-stu-id="717e6-169">ServiceInstall</span></span>](serviceinstall-table.md)

[<span data-ttu-id="717e6-170">Scelte rapide</span><span class="sxs-lookup"><span data-stu-id="717e6-170">Shortcut</span></span>](shortcut-table.md)

[<span data-ttu-id="717e6-171">Verbo</span><span class="sxs-lookup"><span data-stu-id="717e6-171">Verb</span></span>](verb-table.md)

[<span data-ttu-id="717e6-172">Estensione</span><span class="sxs-lookup"><span data-stu-id="717e6-172">Extension</span></span>](extension-table.md)

[<span data-ttu-id="717e6-173">Classe</span><span class="sxs-lookup"><span data-stu-id="717e6-173">Class</span></span>](class-table.md)

[<span data-ttu-id="717e6-174">AppId</span><span class="sxs-lookup"><span data-stu-id="717e6-174">AppId</span></span>](appid-table.md)

[<span data-ttu-id="717e6-175">Environment</span><span class="sxs-lookup"><span data-stu-id="717e6-175">Environment</span></span>](environment-table.md)

## <a name="related-topics"></a><span data-ttu-id="717e6-176">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="717e6-176">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="717e6-177">Riferimento ghiaccio</span><span class="sxs-lookup"><span data-stu-id="717e6-177">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



