---
description: La tabella ModuleDependency mantiene un elenco di altri moduli unione richiesti per il corretto funzionamento del modulo merge.
ms.assetid: 36418331-bec7-40c9-8fdf-fe4b958a1443
title: Tabella ModuleDependency
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bb0c550f8c5ae480a07ca10401d1d3b67c496ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313810"
---
# <a name="moduledependency-table"></a><span data-ttu-id="c99aa-103">Tabella ModuleDependency</span><span class="sxs-lookup"><span data-stu-id="c99aa-103">ModuleDependency Table</span></span>

<span data-ttu-id="c99aa-104">La tabella ModuleDependency mantiene un elenco di altri moduli unione richiesti per il corretto funzionamento del modulo merge.</span><span class="sxs-lookup"><span data-stu-id="c99aa-104">The ModuleDependency table keeps a list of other merge modules that are required for this merge module to operate properly.</span></span> <span data-ttu-id="c99aa-105">Questa tabella consente uno strumento di Unione o verifica per garantire che i moduli unione necessari siano effettivamente inclusi nel database del programma di installazione dell'utente.</span><span class="sxs-lookup"><span data-stu-id="c99aa-105">This table enables a merge or verification tool to ensure that the necessary merge modules are in fact included in the user's installer database.</span></span> <span data-ttu-id="c99aa-106">Lo strumento esegue il controllo incrociato facendo riferimento a questa tabella con la tabella ModuleSignature nel database del programma di installazione.</span><span class="sxs-lookup"><span data-stu-id="c99aa-106">The tool checks by cross referencing this table with the ModuleSignature table in the installer database.</span></span>

<span data-ttu-id="c99aa-107">La tabella ModuleDependency include le colonne seguenti.</span><span class="sxs-lookup"><span data-stu-id="c99aa-107">The ModuleDependency table has the following columns.</span></span>



| <span data-ttu-id="c99aa-108">Colonna</span><span class="sxs-lookup"><span data-stu-id="c99aa-108">Column</span></span>           | <span data-ttu-id="c99aa-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="c99aa-109">Type</span></span>                         | <span data-ttu-id="c99aa-110">Chiave</span><span class="sxs-lookup"><span data-stu-id="c99aa-110">Key</span></span> | <span data-ttu-id="c99aa-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="c99aa-111">Nullable</span></span> |
|------------------|------------------------------|-----|----------|
| <span data-ttu-id="c99aa-112">ModuleID</span><span class="sxs-lookup"><span data-stu-id="c99aa-112">ModuleID</span></span>         | [<span data-ttu-id="c99aa-113">Identificatore</span><span class="sxs-lookup"><span data-stu-id="c99aa-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="c99aa-114">S</span><span class="sxs-lookup"><span data-stu-id="c99aa-114">Y</span></span>   | <span data-ttu-id="c99aa-115">N</span><span class="sxs-lookup"><span data-stu-id="c99aa-115">N</span></span>        |
| <span data-ttu-id="c99aa-116">ModuleLanguage</span><span class="sxs-lookup"><span data-stu-id="c99aa-116">ModuleLanguage</span></span>   | [<span data-ttu-id="c99aa-117">Integer</span><span class="sxs-lookup"><span data-stu-id="c99aa-117">Integer</span></span>](integer.md)       | <span data-ttu-id="c99aa-118">S</span><span class="sxs-lookup"><span data-stu-id="c99aa-118">Y</span></span>   | <span data-ttu-id="c99aa-119">N</span><span class="sxs-lookup"><span data-stu-id="c99aa-119">N</span></span>        |
| <span data-ttu-id="c99aa-120">RequiredID</span><span class="sxs-lookup"><span data-stu-id="c99aa-120">RequiredID</span></span>       | [<span data-ttu-id="c99aa-121">Identificatore</span><span class="sxs-lookup"><span data-stu-id="c99aa-121">Identifier</span></span>](identifier.md) | <span data-ttu-id="c99aa-122">S</span><span class="sxs-lookup"><span data-stu-id="c99aa-122">Y</span></span>   | <span data-ttu-id="c99aa-123">N</span><span class="sxs-lookup"><span data-stu-id="c99aa-123">N</span></span>        |
| <span data-ttu-id="c99aa-124">RequiredLanguage</span><span class="sxs-lookup"><span data-stu-id="c99aa-124">RequiredLanguage</span></span> | [<span data-ttu-id="c99aa-125">Integer</span><span class="sxs-lookup"><span data-stu-id="c99aa-125">Integer</span></span>](integer.md)       | <span data-ttu-id="c99aa-126">S</span><span class="sxs-lookup"><span data-stu-id="c99aa-126">Y</span></span>   | <span data-ttu-id="c99aa-127">N</span><span class="sxs-lookup"><span data-stu-id="c99aa-127">N</span></span>        |
| <span data-ttu-id="c99aa-128">RequiredVersion</span><span class="sxs-lookup"><span data-stu-id="c99aa-128">RequiredVersion</span></span>  | [<span data-ttu-id="c99aa-129">Versione</span><span class="sxs-lookup"><span data-stu-id="c99aa-129">Version</span></span>](version.md)       |     | <span data-ttu-id="c99aa-130">S</span><span class="sxs-lookup"><span data-stu-id="c99aa-130">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="c99aa-131">Colonne</span><span class="sxs-lookup"><span data-stu-id="c99aa-131">Columns</span></span>

<dl> <dt>

<span data-ttu-id="c99aa-132"><span id="ModuleID"></span><span id="moduleid"></span><span id="MODULEID"></span>ModuleID</span><span class="sxs-lookup"><span data-stu-id="c99aa-132"><span id="ModuleID"></span><span id="moduleid"></span><span id="MODULEID"></span>ModuleID</span></span>
</dt> <dd>

<span data-ttu-id="c99aa-133">Identificatore del modulo merge.</span><span class="sxs-lookup"><span data-stu-id="c99aa-133">Identifier of the merge module.</span></span> <span data-ttu-id="c99aa-134">Si tratta di una chiave esterna nella [tabella ModuleSignature](modulesignature-table.md).</span><span class="sxs-lookup"><span data-stu-id="c99aa-134">This is a foreign key into the [ModuleSignature table](modulesignature-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="c99aa-135"><span id="ModuleLanguage"></span><span id="modulelanguage"></span><span id="MODULELANGUAGE"></span>ModuleLanguage</span><span class="sxs-lookup"><span data-stu-id="c99aa-135"><span id="ModuleLanguage"></span><span id="modulelanguage"></span><span id="MODULELANGUAGE"></span>ModuleLanguage</span></span>
</dt> <dd>

<span data-ttu-id="c99aa-136">ID della lingua decimale del modulo merge in ModuleID.</span><span class="sxs-lookup"><span data-stu-id="c99aa-136">Decimal language ID of the merge module in ModuleID.</span></span> <span data-ttu-id="c99aa-137">Si tratta di una chiave esterna nella [tabella ModuleSignature](modulesignature-table.md).</span><span class="sxs-lookup"><span data-stu-id="c99aa-137">This is a foreign key into the [ModuleSignature table](modulesignature-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="c99aa-138"><span id="RequiredID"></span><span id="requiredid"></span><span id="REQUIREDID"></span>RequiredID</span><span class="sxs-lookup"><span data-stu-id="c99aa-138"><span id="RequiredID"></span><span id="requiredid"></span><span id="REQUIREDID"></span>RequiredID</span></span>
</dt> <dd>

<span data-ttu-id="c99aa-139">Identificatore del modulo merge richiesto dal modulo merge in ModuleID.</span><span class="sxs-lookup"><span data-stu-id="c99aa-139">Identifier of the merge module required by the merge module in ModuleID.</span></span>

</dd> <dt>

<span data-ttu-id="c99aa-140"><span id="RequiredLanguage"></span><span id="requiredlanguage"></span><span id="REQUIREDLANGUAGE"></span>RequiredLanguage</span><span class="sxs-lookup"><span data-stu-id="c99aa-140"><span id="RequiredLanguage"></span><span id="requiredlanguage"></span><span id="REQUIREDLANGUAGE"></span>RequiredLanguage</span></span>
</dt> <dd>

<span data-ttu-id="c99aa-141">ID lingua numerica del modulo merge in RequiredID.</span><span class="sxs-lookup"><span data-stu-id="c99aa-141">Numeric language ID of the merge module in RequiredID.</span></span> <span data-ttu-id="c99aa-142">La colonna RequiredLanguage può specificare l'ID lingua per una sola lingua, ad esempio 1033 per l'inglese (Stati Uniti), oppure specificare l'ID lingua per un gruppo di lingue, ad esempio 9 per qualsiasi lingua inglese.</span><span class="sxs-lookup"><span data-stu-id="c99aa-142">The RequiredLanguage column can specify the language ID for a single language, such as 1033 for U.S. English, or specify the language ID for a language group, such as 9 for any English.</span></span> <span data-ttu-id="c99aa-143">Se il campo contiene un ID lingua del gruppo, qualsiasi modulo merge con un codice lingua in tale gruppo soddisfa la dipendenza.</span><span class="sxs-lookup"><span data-stu-id="c99aa-143">If the field contains a group language ID, any merge module with having a language code in that group satisfies the dependency.</span></span> <span data-ttu-id="c99aa-144">Se RequiredLanguage è impostato su 0, qualsiasi modulo di merge che riempie gli altri requisiti soddisfa la dipendenza.</span><span class="sxs-lookup"><span data-stu-id="c99aa-144">If the RequiredLanguage is set to 0, any merge module filling the other requirements satisfies the dependency.</span></span>

</dd> <dt>

<span data-ttu-id="c99aa-145"><span id="RequiredVersion"></span><span id="requiredversion"></span><span id="REQUIREDVERSION"></span>RequiredVersion</span><span class="sxs-lookup"><span data-stu-id="c99aa-145"><span id="RequiredVersion"></span><span id="requiredversion"></span><span id="REQUIREDVERSION"></span>RequiredVersion</span></span>
</dt> <dd>

<span data-ttu-id="c99aa-146">Versione del modulo merge in RequiredID.</span><span class="sxs-lookup"><span data-stu-id="c99aa-146">Version of the merge module in RequiredID.</span></span> <span data-ttu-id="c99aa-147">Se questo campo è null, qualsiasi versione compila la dipendenza.</span><span class="sxs-lookup"><span data-stu-id="c99aa-147">If this field is Null, any version fills the dependency.</span></span>

</dd> </dl>

## <a name="validation"></a><span data-ttu-id="c99aa-148">Convalida</span><span class="sxs-lookup"><span data-stu-id="c99aa-148">Validation</span></span>

<dl>

[<span data-ttu-id="c99aa-149">ICE03</span><span class="sxs-lookup"><span data-stu-id="c99aa-149">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="c99aa-150">ICE06</span><span class="sxs-lookup"><span data-stu-id="c99aa-150">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="c99aa-151">ICE25</span><span class="sxs-lookup"><span data-stu-id="c99aa-151">ICE25</span></span>](ice25.md)  
</dl>

 

 



