---
description: La tabella ModuleExclusion mantiene un elenco di altri moduli merge che non sono compatibili nello stesso database del programma di installazione.
ms.assetid: c28d9afa-152c-43b5-9892-7a38fae8c593
title: Tabella ModuleExclusion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8fb4cc136937d5a01bd16a42c138532dd524ee1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104401769"
---
# <a name="moduleexclusion-table"></a><span data-ttu-id="02388-103">Tabella ModuleExclusion</span><span class="sxs-lookup"><span data-stu-id="02388-103">ModuleExclusion Table</span></span>

<span data-ttu-id="02388-104">La tabella ModuleExclusion mantiene un elenco di altri moduli merge che non sono compatibili nello stesso database del programma di installazione.</span><span class="sxs-lookup"><span data-stu-id="02388-104">The ModuleExclusion table keeps a list of other merge modules that are incompatible in the same installer database.</span></span> <span data-ttu-id="02388-105">Questa tabella consente a uno strumento di merge o di verifica di verificare che i moduli merge in conflitto non siano Uniti nel database del programma di installazione dell'utente.</span><span class="sxs-lookup"><span data-stu-id="02388-105">This table enables a merge or verification tool to check that conflicting merge modules are not merged in the user's installer database.</span></span> <span data-ttu-id="02388-106">Lo strumento esegue il controllo incrociato della tabella con la tabella ModuleSignature nel database del programma di installazione.</span><span class="sxs-lookup"><span data-stu-id="02388-106">The tool checks by cross-referencing this table with the ModuleSignature table in the installer database.</span></span>

<span data-ttu-id="02388-107">La tabella ModuleExclusion include le colonne seguenti.</span><span class="sxs-lookup"><span data-stu-id="02388-107">The ModuleExclusion table has the following columns.</span></span>



| <span data-ttu-id="02388-108">Colonna</span><span class="sxs-lookup"><span data-stu-id="02388-108">Column</span></span>             | <span data-ttu-id="02388-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="02388-109">Type</span></span>                         | <span data-ttu-id="02388-110">Chiave</span><span class="sxs-lookup"><span data-stu-id="02388-110">Key</span></span> | <span data-ttu-id="02388-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="02388-111">Nullable</span></span> |
|--------------------|------------------------------|-----|----------|
| <span data-ttu-id="02388-112">ModuleID</span><span class="sxs-lookup"><span data-stu-id="02388-112">ModuleID</span></span>           | [<span data-ttu-id="02388-113">Identificatore</span><span class="sxs-lookup"><span data-stu-id="02388-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="02388-114">S</span><span class="sxs-lookup"><span data-stu-id="02388-114">Y</span></span>   | <span data-ttu-id="02388-115">N</span><span class="sxs-lookup"><span data-stu-id="02388-115">N</span></span>        |
| <span data-ttu-id="02388-116">ModuleLanguage</span><span class="sxs-lookup"><span data-stu-id="02388-116">ModuleLanguage</span></span>     | [<span data-ttu-id="02388-117">Integer</span><span class="sxs-lookup"><span data-stu-id="02388-117">Integer</span></span>](integer.md)       | <span data-ttu-id="02388-118">S</span><span class="sxs-lookup"><span data-stu-id="02388-118">Y</span></span>   | <span data-ttu-id="02388-119">N</span><span class="sxs-lookup"><span data-stu-id="02388-119">N</span></span>        |
| <span data-ttu-id="02388-120">ExcludedID</span><span class="sxs-lookup"><span data-stu-id="02388-120">ExcludedID</span></span>         | [<span data-ttu-id="02388-121">Identificatore</span><span class="sxs-lookup"><span data-stu-id="02388-121">Identifier</span></span>](identifier.md) | <span data-ttu-id="02388-122">S</span><span class="sxs-lookup"><span data-stu-id="02388-122">Y</span></span>   | <span data-ttu-id="02388-123">N</span><span class="sxs-lookup"><span data-stu-id="02388-123">N</span></span>        |
| <span data-ttu-id="02388-124">ExcludedLanguage</span><span class="sxs-lookup"><span data-stu-id="02388-124">ExcludedLanguage</span></span>   | [<span data-ttu-id="02388-125">Integer</span><span class="sxs-lookup"><span data-stu-id="02388-125">Integer</span></span>](integer.md)       | <span data-ttu-id="02388-126">S</span><span class="sxs-lookup"><span data-stu-id="02388-126">Y</span></span>   | <span data-ttu-id="02388-127">N</span><span class="sxs-lookup"><span data-stu-id="02388-127">N</span></span>        |
| <span data-ttu-id="02388-128">ExcludedMinVersion</span><span class="sxs-lookup"><span data-stu-id="02388-128">ExcludedMinVersion</span></span> | [<span data-ttu-id="02388-129">Versione</span><span class="sxs-lookup"><span data-stu-id="02388-129">Version</span></span>](version.md)       |     | <span data-ttu-id="02388-130">S</span><span class="sxs-lookup"><span data-stu-id="02388-130">Y</span></span>        |
| <span data-ttu-id="02388-131">ExcludedMaxVersion</span><span class="sxs-lookup"><span data-stu-id="02388-131">ExcludedMaxVersion</span></span> | [<span data-ttu-id="02388-132">Versione</span><span class="sxs-lookup"><span data-stu-id="02388-132">Version</span></span>](version.md)       |     | <span data-ttu-id="02388-133">S</span><span class="sxs-lookup"><span data-stu-id="02388-133">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="02388-134">Colonne</span><span class="sxs-lookup"><span data-stu-id="02388-134">Columns</span></span>

<dl> <dt>

<span data-ttu-id="02388-135"><span id="ModuleID"></span><span id="moduleid"></span><span id="MODULEID"></span>ModuleID</span><span class="sxs-lookup"><span data-stu-id="02388-135"><span id="ModuleID"></span><span id="moduleid"></span><span id="MODULEID"></span>ModuleID</span></span>
</dt> <dd>

<span data-ttu-id="02388-136">Identificatore del modulo merge.</span><span class="sxs-lookup"><span data-stu-id="02388-136">Identifier of the merge module.</span></span> <span data-ttu-id="02388-137">Si tratta di una chiave esterna nella [tabella ModuleSignature](modulesignature-table.md).</span><span class="sxs-lookup"><span data-stu-id="02388-137">This is a foreign key into the [ModuleSignature table](modulesignature-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="02388-138"><span id="ModuleLanguage"></span><span id="modulelanguage"></span><span id="MODULELANGUAGE"></span>ModuleLanguage</span><span class="sxs-lookup"><span data-stu-id="02388-138"><span id="ModuleLanguage"></span><span id="modulelanguage"></span><span id="MODULELANGUAGE"></span>ModuleLanguage</span></span>
</dt> <dd>

<span data-ttu-id="02388-139">ID della lingua decimale del modulo merge in ModuleID.</span><span class="sxs-lookup"><span data-stu-id="02388-139">Decimal language ID of the merge module in ModuleID.</span></span> <span data-ttu-id="02388-140">Si tratta di una chiave esterna nella [tabella ModuleSignature](modulesignature-table.md).</span><span class="sxs-lookup"><span data-stu-id="02388-140">This is a foreign key into the [ModuleSignature table](modulesignature-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="02388-141"><span id="ExcludedID"></span><span id="excludedid"></span><span id="EXCLUDEDID"></span>ExcludedID</span><span class="sxs-lookup"><span data-stu-id="02388-141"><span id="ExcludedID"></span><span id="excludedid"></span><span id="EXCLUDEDID"></span>ExcludedID</span></span>
</dt> <dd>

<span data-ttu-id="02388-142">Identificatore di un modulo merge escluso.</span><span class="sxs-lookup"><span data-stu-id="02388-142">Identifier of an excluded merge module.</span></span>

</dd> <dt>

<span data-ttu-id="02388-143"><span id="ExcludedLanguage"></span><span id="excludedlanguage"></span><span id="EXCLUDEDLANGUAGE"></span>ExcludedLanguage</span><span class="sxs-lookup"><span data-stu-id="02388-143"><span id="ExcludedLanguage"></span><span id="excludedlanguage"></span><span id="EXCLUDEDLANGUAGE"></span>ExcludedLanguage</span></span>
</dt> <dd>

<span data-ttu-id="02388-144">ID lingua numerica del modulo merge in ExcludedID.</span><span class="sxs-lookup"><span data-stu-id="02388-144">Numeric language ID of the merge module in ExcludedID.</span></span> <span data-ttu-id="02388-145">La colonna ExcludedLanguage può specificare l'ID lingua per una sola lingua, ad esempio 1033 per l'inglese (Stati Uniti), oppure specificare l'ID lingua per un gruppo di lingue, ad esempio 9 per qualsiasi lingua inglese.</span><span class="sxs-lookup"><span data-stu-id="02388-145">The ExcludedLanguage column can specify the language ID for a single language, such as 1033 for U.S. English, or specify the language ID for a language group, such as 9 for any English.</span></span> <span data-ttu-id="02388-146">La colonna ExcludedLanguage può accettare ID di lingua negativi.</span><span class="sxs-lookup"><span data-stu-id="02388-146">The ExcludedLanguage column can accept negative language IDs.</span></span> <span data-ttu-id="02388-147">Il significato del valore nella colonna ExcludedLanguage è il seguente.</span><span class="sxs-lookup"><span data-stu-id="02388-147">The meaning of the value in the ExcludedLanguage column is as follows.</span></span>



| <span data-ttu-id="02388-148">ExcludedLanguage</span><span class="sxs-lookup"><span data-stu-id="02388-148">ExcludedLanguage</span></span> | <span data-ttu-id="02388-149">Significato</span><span class="sxs-lookup"><span data-stu-id="02388-149">Meaning</span></span>                                                              |
|------------------|----------------------------------------------------------------------|
| <span data-ttu-id="02388-150">> 0</span><span class="sxs-lookup"><span data-stu-id="02388-150">> 0</span></span>           | <span data-ttu-id="02388-151">Escludi gli ID lingua specificati da ExcludedLanguage.</span><span class="sxs-lookup"><span data-stu-id="02388-151">Exclude the language IDs specified by ExcludedLanguage.</span></span>              |
| <span data-ttu-id="02388-152">= 0</span><span class="sxs-lookup"><span data-stu-id="02388-152">= 0</span></span>              | <span data-ttu-id="02388-153">Escludere nessun ID di lingua.</span><span class="sxs-lookup"><span data-stu-id="02388-153">Exclude no language IDs.</span></span>                                             |
| <span data-ttu-id="02388-154">< 0</span><span class="sxs-lookup"><span data-stu-id="02388-154">< 0</span></span>           | <span data-ttu-id="02388-155">Escludere tutti gli ID lingua eccetto quelli specificati da ExcludedLanguage.</span><span class="sxs-lookup"><span data-stu-id="02388-155">Exclude all language IDs except those specified by ExcludedLanguage.</span></span> |



 

</dd> <dt>

<span data-ttu-id="02388-156"><span id="ExcludedMinVersion"></span><span id="excludedminversion"></span><span id="EXCLUDEDMINVERSION"></span>ExcludedMinVersion</span><span class="sxs-lookup"><span data-stu-id="02388-156"><span id="ExcludedMinVersion"></span><span id="excludedminversion"></span><span id="EXCLUDEDMINVERSION"></span>ExcludedMinVersion</span></span>
</dt> <dd>

<span data-ttu-id="02388-157">Versione minima esclusa da un intervallo.</span><span class="sxs-lookup"><span data-stu-id="02388-157">Minimum version excluded from a range.</span></span> <span data-ttu-id="02388-158">Se il campo ExcludedMinVersion è null, vengono escluse tutte le versioni precedenti a ExcludedMaxVersion.</span><span class="sxs-lookup"><span data-stu-id="02388-158">If the ExcludedMinVersion field is Null, all versions before ExcludedMaxVersion are excluded.</span></span> <span data-ttu-id="02388-159">Se ExcludedMinVersion e ExcludedMaxVersion sono null, non esiste alcuna esclusione in base alla versione.</span><span class="sxs-lookup"><span data-stu-id="02388-159">If both ExcludedMinVersion and ExcludedMaxVersion are Null there is no exclusion based on version.</span></span>

</dd> <dt>

<span data-ttu-id="02388-160"><span id="ExcludedMaxVersion"></span><span id="excludedmaxversion"></span><span id="EXCLUDEDMAXVERSION"></span>ExcludedMaxVersion</span><span class="sxs-lookup"><span data-stu-id="02388-160"><span id="ExcludedMaxVersion"></span><span id="excludedmaxversion"></span><span id="EXCLUDEDMAXVERSION"></span>ExcludedMaxVersion</span></span>
</dt> <dd>

<span data-ttu-id="02388-161">Versione massima esclusa da un intervallo.</span><span class="sxs-lookup"><span data-stu-id="02388-161">Maximum version excluded from a range.</span></span> <span data-ttu-id="02388-162">Se il campo ExcludedMaxVersion è null, tutte le versioni dopo ExcludedMinVersion vengono escluse.</span><span class="sxs-lookup"><span data-stu-id="02388-162">If the ExcludedMaxVersion field is Null, all versions after ExcludedMinVersion are excluded.</span></span> <span data-ttu-id="02388-163">Se ExcludedMinVersion e ExcludedMaxVersion sono null, non esiste alcuna esclusione in base alla versione.</span><span class="sxs-lookup"><span data-stu-id="02388-163">If both ExcludedMinVersion and ExcludedMaxVersion are Null there is no exclusion based on version.</span></span>

</dd> </dl>

## <a name="validation"></a><span data-ttu-id="02388-164">Convalida</span><span class="sxs-lookup"><span data-stu-id="02388-164">Validation</span></span>

<dl>

[<span data-ttu-id="02388-165">ICE03</span><span class="sxs-lookup"><span data-stu-id="02388-165">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="02388-166">ICE06</span><span class="sxs-lookup"><span data-stu-id="02388-166">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="02388-167">ICE25</span><span class="sxs-lookup"><span data-stu-id="02388-167">ICE25</span></span>](ice25.md)  
</dl>

 

 



